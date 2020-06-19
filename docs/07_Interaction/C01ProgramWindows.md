 
 # Program windows
An OPENRNDR program can listen to events generated by its window.

## Window properties

### Window title

The window title can be set and read using the `title` property. 
 
 ```kotlin
application {
    configure {
        title = "Lo and behold!"
    }
    
    program {
        println(window.title)
    }
}
``` 
 
 ### Window position

The window position can be read and set using the `position` property. 
 
 ```kotlin
application {
    configure {
        position = IntVector2(30, 30)
    }
}
``` 
 
 ## Window events

### Window move event

This event is generated when the window was moved. 
 
 ```kotlin
application {
    program {
        window.moved.listen {
            println("the window was moved")
        }
    }
}
``` 
 
 ### Window size event

This event is generated when the window was sized. 
 
 ```kotlin
application {
    program {
        window.sized.listen {
            println("the window was sized")
        }
    }
}
``` 
 
 ### Window focus event

This event is generated when the program window gains focus. 
 
 ```kotlin
application {
    program {
        window.focused.listen {
            println("the window has gained focus")
        }
    }
}
``` 
 
 ### Window unfocus event

This event is generated when the program window loses focus. 
 
 ```kotlin
application {
    program {
        window.unfocused.listen {
            println("the window has lost its focus")
        }
    }
}
``` 