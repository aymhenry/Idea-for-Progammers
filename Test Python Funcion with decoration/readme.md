# Test Python Function Using Decoration function

**Idea**

This function could be imported to the source code of your function, add one decoration before the name of function, and it is done.

This function will print the inputs and/or outputs of any function.

Decoration function take one parameters, could be the string IN, OUT or ALL. to print only inputs, or/and outputs.

it is prefaded to call the basic function (the following example, function test) using named arguments, so decoration function can print argument name with its value.
or decoration function with list arguments by number. see example below.

**Example of named argument**

    test(arg1=3, arg3=5, arg2=7)

The following example shows how to use decoration function 

    from decorators import *
    @show_input_output ("ALL")     
    def test (arg1, arg2, arg3):
        return arg1 + arg2 + arg3
    
    print ("test(3, 6, 3) =",test(3, 6, 3))
    print ("test(3, arg3=5, arg2=7) =",test(3, arg3=5, arg2=7)))

**Sample output**

    #-- Function Name: test ===============
        #-- inputs:
            arg no 1 =  3
            arg no 2 =  6
            arg no 3 =  3
        #-- Output:
            Result = 12


    test(3, 6, 3) = 12
    #-- Function Name: test ===============
        #-- inputs:
            arg no 1 =  3
            arg3 =  5
            arg2 =  7
        #-- Output:
            Result = 15


    test(3, arg3=5, arg2=7) = 15