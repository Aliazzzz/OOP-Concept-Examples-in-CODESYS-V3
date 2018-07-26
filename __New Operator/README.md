# Demonstrates the usage of the __New operator in CODESYS V3

First of, usage of this mechanism in a live production environment is STRONGLY DISCOURAGED!
This example shows the usage of creating and destroying objects on demand in Runtime. This is common practice in any object oriented programming language. However, creating and or destroying objects in Runtime in a live production PAC/PLC/DCS system is NOT. Nevertheless, the mechanism itself is definitely interesting from an academic and testlab-environment point of view and certainly has its specific purposes.

*Requirement: In the properties dialog of the application, the Use dynamic memory allocation check box is selected in the Application build options tab*
