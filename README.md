# Custome and Global-Exceptions handling demo

# Exceptions overview
=> Exception Handling is a mechanism to handle runtime errors such as ClassNotFoundException, IOException, SQLException, RemoteException, etc.

# Why should we handle exceptions?
 =>The core reason of exception handling is to maintain the normal flow of the application.
   An exception normally disrupts the normal flow of the application; that is why we need to handle exceptions.
   Let'head on to this demo moto.
   
-> Before proceeding with exception handling, let us gain an understanding on the following annotations.such as
# @ResponseStatus
->We can use @ResponseStatus to mark a method or an exception class with a status code and reason that should be returned. 
  On invoking the marked handler method or when a specified exception is thrown, the HTTP status will be set to the one defined using @ResponseStatus annotation.
  more specifically if i say then to map a exceptions status code how to response,rest we will see in this tuitorial.
  
# @ExceptionsHandler  
->The @ExceptionHandler is an annotation used to handle the specific exceptions and sending the custom responses to the client.
  Define a class that extends the RuntimeException class. You can define the @ExceptionHandler method to handle the specific exceptions. 
  
# @ControllerAdvice
->@ControllerAdvice is a specialization of the @Component annotation which allows to handle exceptions across the whole application in one global handling component. It can be viewed as an interceptor of exceptions thrown by methods annotated with @RequestMapping and similar.

# @ControllerAdvice VS @ExceptionHandler
-> A @ExceptionHandler is local to a controller : only exceptions from this controller is routed to his @ExceptionHandler
   But a @ControllerAdvice is global : you can have a centralized way to handle exceptions, binding, etc. it applies to all the defined controller.

   
   
