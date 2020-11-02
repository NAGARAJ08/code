# code
Using Abstract Classes
There are situations in which you will want to define a superclass that declares the structure
of a given abstraction without providing a complete implementation of every method. That
is, sometimes you will want to create a superclass that only defines a generalized form that
will be shared by all of its subclasses, leaving it to each subclass to fill in the details. Such a
class determines the nature of the methods that the subclasses must implement. One way
this situation can occur is when a superclass is unable to create a meaningful implementation
for a method. This is the case with the class Figure used in the preceding example. The
definition of area( ) is simply a placeholder. It will not compute and display the area of any
type of object.
As you will see as you create your own class libraries, it is not uncommon for a method
to have no meaningful definition in the context of its superclass. You can handle this situation
two ways. One way, as shown in the previous example, is to simply have it report a warning
message. While this approach can be useful in certain situations—such as debugging—it is
not usually appropriate. You may have methods that must be overridden by the subclass
in order for the subclass to have any meaning. Consider the class Triangle. It has no meaning
if area( ) is not defined. In this case, you want some way to ensure that a subclass does, indeed,
override all necessary methods. Java’s solution to this problem is the abstract method.
You can require that certain methods be overridden by subclasses by specifying the
abstract type modifier. These methods are sometimes referred to as subclasser responsibility
because they have no implementation specified in the superclass. Thus, a subclass must
177
