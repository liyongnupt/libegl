# FAQ

## The program throws EXEC\_BAD\_EXEC when deallocating EGLSurface instances for instance. Why ? 

It happens when EGLNativeWindowType is NOT NULL AND invalid (eg: 
EGLNativeWindowType Address does not point to the valid EGLNativeWindowType).
This implementation cannot verify this condition and therefore is undefined behaviour 
as per EGL 1.4 (Section 3.1 - Parameter Validation)

