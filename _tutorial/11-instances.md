---
title: "Class instances"
permalink: /tutorial/instances/
---

Classes are of course used to instantiate new objects comprising fields and methods.

The well-known `new` operator is used in QED to instantiate objects. The equally popular `.` operator allows access to fields and methods.

{% include sandboxframe.html qedsrc="tutorial/classes1.qed" gui="0" height="230px" %}

Here the class declaration is the constructor, the `a` parameter and `double` local variable are fields and the nested function `printDouble()` is a method. Upon instantating the class, the `obj` instance contains both fields and the method, reachable by the `.` operator.

Classes are also first-class citizens.

A class interface can be created like a function interface. It can also be used with the `*` symbol to refer to a class pointer. The class can be instantiated and an instance object (without `*`) is returned.

{% include sandboxframe.html qedsrc="tutorial/classes2.qed" gui="0" height="410px" %}

All class members (fields and methods) are declared public as of now. When QED evolves, we will introduce a way to declare private members as well.

<!-- Private members can be embedded a wrapper plain builder function (which first letter is lowercase to not make it a class):

{% include sandboxframe.html qedsrc="tutorial/classes3.qed" gui="0" height="280px" %}
-->
For pure class instantiation purposes, it is better to use the `void` return type when declaring its class, since the object will never return anything.
{: .notice--info}

A word of caution here. QED classes, when compiled into JS code, generate Javascript classes as well. When using embedded JS code in a class and refer to one of its members, use `<classname>$this` (generated by the QED compiler) instead of the direct `this` pointer.

{% include sandboxframe.html qedsrc="tutorial/classes4.qed" gui="0" height="200px" %}

We only scratched the surface as to what QED classes can do. The time has come to expand their functionality!
