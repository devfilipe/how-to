###### Part I - Install Erlide

1. Start eclipse
2. If it prompts you to choose workspace, select the folder you want to work in.
For this tutorial you might want to use a fresh one.
3. On the menu bar, Choose Help -> Marketplace
4. Select the Installed Search tab.
5. Type "Erlang IDE" in Find field. (erlide - Erlang IDE 0.55.0)
6. Click the Install button on the right.
7. Accept the terms of the license agreement.
8. Click Finish.
9. On menu bar, select File->Restart.

###### Part II - Erlang Runtime

1. Click on the Workbench icon on the right side of the main eclipse window
2. On menu bar, choose Windows -> Preferences -> Erlang -> Installed runtimes
3. See if there is a runtime listed in the drop down field called Runtime used
by Erlide itself (restart is required - see step 9). If there is something there,
hit Cancel and go on to Part III.
4. In the Runtime name field, enter `erl<version>`.
5. In the Location field, browse to the very top level folder of the Erlang tree.
This should be a folder called `erl<version>` or something like that.
6. Click OK. Then Click Apply and OK in the Install runtimes pane.
7. On menu bar, choose File -> Restart.

###### Part III - New Project

1. On menu bar, chose Windows -> Perspective -> Open Perspective ->Other... -> Erlang. Click Open.
2. On menu bar, chose File -> New -> Erlang Project;
alternativelly, in Project Explorer, chose New Erlang Project
3. In Project name field, type HelloWorldProject
4. Click Next .. Next .. Finish

###### Part IV - Config

1. On menu bar, choose Project and make sure that Build Automatically option is checked
2. The left pane is the Erlang Navigator. Right-click the HelloWorldProject branch.
In the context menu that pops, select New -> Other... -> Erlang -> Module and
click Next (can also just select “New Module” directly)
3. In the wizard, in the Module name field, type hello
4. Click Finish
5. On menu bar, choose Run -> Run Configurations...
6. Select the “Erlang application”
7. Click the New Launch configuration button (left side above the field with “type filter text”)
8. Select the “New configuration”
9. Select the “Main tab” in the right pane
10. Check the box left of the HelloWorldProject
11. Select the “Runtimes” tab in the right pane
12. In the filed titled Node name, enter erlide
13. In some environments, Java and Erlang look for the default .erlang.cookie
file in different places, and if you get connection problems you should enter
some value for the Cookie field.
If the node is already running, you have to use the same cookie value;
otherwise, any string will do.
14. Check the box to the left of “Start the Erlang node if not running presently”
15. Click “Apply” and “Run”

###### Part V - Code

1. In the center code pane (titled “hello.erl”), enter the following code: hello/0
(within the brackets for the export, so it reads -export([hello/0]).
2. On the next line after the export, enter the following code:
```erl
hello() -> io:format("Hello World!~n", []).
```
3. In the menu bar, choose File -> Save As...
4. Double-click on the folder titled “HelloWorldProject” in the dialog box
5. Click on (select) the folder titled src in the dialog box.
The field entitled Enter or select the parent folder:
should now read HelloWorldProject/src
6. Click OK. The file hello.erl is saved in the src directory and automatically built.
7. The lower pane has a number of tabs. Select the “Console” tab.
8. In the console pane, enter the following command hello:hello(). and hit return.
The output from the program will appear.
```bash
Eshell V10.5
(HelloWorldErlangProject@filipe-K95VM)1> hello:hello().
Hello World!
ok
```
9. To exit, in the menu bar, choose File -> Close, and then File -> Exit

###### Eclipse IDE Software Updates
When a Security Warning dialog pops up, click on Install anyway.
Click Restart Now

###### References
https://erlide.org/articles/eclipse/140_Tutorial-Quick-Start.html
