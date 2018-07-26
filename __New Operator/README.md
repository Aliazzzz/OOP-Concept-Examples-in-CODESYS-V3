# Demonstrates the usage of the __New operator in CODESYS V3

First of, usage of this mechanism in a live production environment is STRONGLY DISCOURAGED!
This example shows the usage of creating and destroying objects on demand in Runtime. This is common practice in any object oriented programming language. However, creating and or destroying objects in Runtime in a live production PAC/PLC/DCS system is NOT. Nevertheless, the mechanism itself is definitely interesting from an academic and testlab-environment point of view and certainly has its specific purposes.

Activation;
In the properties dialog of the application, the Use dynamic memory allocation check box is selected in the Application build options tab. Also specify a memory reservation for NEW usage here.

A function block that can be created with NEW has a fixed memory area. 
It cannot modify its data layout by means of an online change. Therefore, new variables cannot be added or deleted, and types cannot be modified. This makes sure that the pointer to this object is also valid after an online change.
For this reason, the NEW operator can be applied only to function blocks from libraries and function blocks with the attribute “enable_dynamic_creation”. If the interface of this kind of function block is changed, then CODESYS issues an error message.
