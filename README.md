## Welcome to InPAD

Here you can find information about InPAD, our long term project for building an interactive and language independent pattern detection framework. InPAD is being built based on  the  rationale  that,  regardless  of  the  language  in  use  andpossible  variations  a  pattern  may  have,  the  major  objectiveof  pattern  application  is  decoupling  a  complex  system  intomodules  by  injecting  key  interfaces. Here is our research  objectives:

- enable the user to express the key design abstractions of patterns interactively and automatically extract the modular structure of individual pattern spaces;
- enable language-agnostic pattern detection through configuration;
- advance our understanding on how patterns are applied in practice by creating a pattern respository extracted from large scale software systems.

### Markdown

Design Pattern Structure represened using UML.


Design Pattern Structure represented using DSM and DRSpaces

- Design Structure Matrix [reference].
- DRSpace. [reference]
- DV8. [reference] : mo:ase2018.

The example bellow depicts the DRSpace of an Abstract Factory Pattern implemented in Java. The cell $(r_{10}, c_6}$  indicates that $BlueMazeFactory$, a concrete factory class, depends on $MazeFactory$. The DRSpace is clustered into a DRH with 3 layers: l1: (rc1-rc6), l2: (rc7-rc14), and l3: (rc15). In the second layer, there are 2 independent inner modules, m1: (rc7-rc10) and m2 (rc11-rc14). The cells in a DSM can be tailored to represent the type of structural dependency among the files. For example, the class $MazeFactory.java$ is responsible for instantiating the $Maze$, which can represented as a CREATE relationship. An Abstract Factory pattern must have an entity, class, files, etc., that takes the role of ABSTRACT FACTORY, which should be an interface (design rule) that decouples concrete factories.. Also, the key interfaces of the system, $MapSite, Room, Door, Wall, Maze$, and the pattern interface, $MazeFactory$ serve as the design rules that decouple other Java classes into two independent modules: File 7 to 10 form a BlueMazeFactory module, and File 11 to 14 form a RedMazeFactory module. File 15 is the control class and the entry point of the system, which depends on the design rules and two concrete factory classes. Most patterns should have a DRSpace with a clear modular structure. We manipulate DSM using the DV8 tool suites. Instead of viewing software architecture design as simply a set of entities and relations, we herein consider that architecture is structured by design rules and their subordinating independent modules.  

[Link](url) and ![Image](src)

Java
![Image](images/abs-factory-dsm.png)

C#

To illustrate the feasibility of our approach, we processed the same maze game program applying the abstract factory pattern written in C\#. Relationships are represented differently from the Java version. For example, the inheritance between $.maze.GreenRoom$ and $.maze.Room$ in the cell(r6, c1) is expressed as a BASE relationship, and the creation of maze.Maze$ by maze.MazeFactory$, as shown in the cell(r5, c2) is expressed by the structural dependency ALLOC. Although each programming language has different types of relationships, these structural dependencies are semantically equivalent. 

![Image](images/abs-factory-sharp.png)