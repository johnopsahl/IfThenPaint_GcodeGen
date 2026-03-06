Description:
A CNC painting dauber application that prepares bitmap images for painting. 

Reqs:
1. system should be machine agnostic (i.e. can work with machines of any number of axes and workspace layouts)
2. motion parameters shall be stored in the grbl config and not in the machine config; except for tool heads
3. 
   
TODO:
1. ~~machine config validation: numeric ranges, fields present, type validation~~
2. ~~generate station assignments template from machine config~~
3. ~~how to assign tool profiles to tools~~
4. ~~move mixtures, components, and tool profiles to a SQLite database~~
5. consider separating movement to safety|z_clearance_mm from operations in machine config
6. multiple or a single "tools" table in components.db? 
7. ~~add deg/ml to paint dispenser in machine config~~
8. ~~move paint bead parameters to "paints" table in database. decided to keep in machine config until it becomes apparent that paint bead parameters are different for different paint types, manufacturers, and models~~
9. develop tool_profile data in components.db
10. store machine data separate from project data? how is this handled in cnc milling software?
11. where and how should tool head parameters be stored
12. ~~tool head parameters need to include motion parameters because that is handled in gcode when switching tools -> no tool parameters will be set during the home-zero operations~~
13. where to assign mix paddle to the mixing operation