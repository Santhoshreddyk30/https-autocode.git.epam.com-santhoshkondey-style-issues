Style Issues
A beginner-level task to practice fixing code style issues detected by code analysis tools.
Estimated time to complete the task: 30 minutes.
The task requires .NET 6 SDK installed.

Task Description

StyleCop Issues
StyleCop Analyzers is a code analysis tool used to detect code style issues. StyleCop has a settings file with a list of enabled rules and it raises an error or a warning in case a rule is violated. For rules documentation and reasoning on the rules themselves, see the Documentation section.

SA1001


Build the solution.

Click on the menu item - Build\Build Solution.
Or use the default keyboard shortcut - Ctrl+Shift+B (various versions of Visual Studio may have different keyboard shortcuts. See Keyboard shortcuts in Visual Studio article).





Open the Error List view.

Click on the menu item - View\Error List.
Or use the default shortcut - Ctrl+\, E.





Find an error with SA1001 code and review the error in detail by clicking on the link in the "Code" column.


You will get to the issue documentation page.

Double-click on the SA1001 issue in the Error List view.


You will get to the SA1001/Math.cs file.



Read the documentation page and learn how to fix the error: "To fix a violation of this rule, ensure that the comma is followed by a single space, and is not preceded by any space."


Remove a whitespace before a comma in the method parameter list.



public static int Sum(int x,int y)



Add a whitespace after the comma.


public static int Sum(int x, int y)



Rebuild the solution.



Open the Error List view again and make sure there are no SA1001 issues.


SA1002


Open the Error List view, find the SA1002 issue.
Open and read the issue documentation page.
Navigate to the code by clicking on the issue line in Error List view.
Remove the whitespace before the semicolon.
Rebuild the solution.
Open the Error List view again and make sure there are no SA1002 issues anymore.


SA1005

Fix the issue by removing the incorrect code line and uncommenting the commented code.

SA1008

Fix the issue by removing the whitespace before and after opening parenthesis.

SA1025

Fix the issue by removing redundant whitespace characters.

SA1028

Fix the issue by removing unnecessary whitespace characters at the end of the lines.

SA1500

Fix the issue by putting opening and closing curly brackets on new lines.

SA1505

Fix the issue by removing the empty line after the opening curly bracket.

SA1507

Fix the issue by removing the redundant empty line.

SA1508

Fix the issue by removing the empty lines before the closing curly brackets.
You can go to the AutoCode portal, open the task page, and initiate the task checking.

Roslyn Analyzers
.NET compiler platform analyzers inspect your C# code for code quality and style issues. Starting with .NET 5, these analyzers are included with the .NET SDK. If your project targets .NET 5 or later, code analysis is enabled by default.

CA1304

Fix the issue by adding an InvariantCulture parameter to the ToUpper method call.

public static string MyMethod(string str)
{
    return "K-" + str.ToUpper(CultureInfo.InvariantCulture);
}



CA1305

Fix the issue by adding an InvariantCulture parameter to the ToUpper method call.

public static string MyMethod(int i)
{
    return "X" + i.ToString(CultureInfo.InvariantCulture);
}



CA1507

Fix the issue by using the nameof expression as an exception constructor parameter.

public static string MyMethod(string str)
{
    if (str == null)
    {
        throw new ArgumentNullException(nameof(str));
    }

    return "test" + str;
}



CA1707 & SA1300

Fix the issue by removing the underscore from the method name. Use the standard C# capitalization conventions: Pascal Casing for method names and Camel Casing for parameter names.

public static string MyMethod(string myStr)
{
    return myStr;
}



Fix Compiler Issues
Additional style and code checks are enabled for the projects in this solution to help you maintaining consistency of the project source code and avoiding silly mistakes. Review the Error List in Visual Studio to see all compiler warnings and errors.
If a compiler error or warning message is not clear, review errors details or google the error or warning code to get more information about the issue.
Also, you can use Sonar rule knowledge database for searching more detailed information regarding detected Sonars' issues.

Task Checklist

Rebuild the solution.
Fix all compiler warnings and errors. Make sure there are no warnings and errors in Error List.



Run all unit tests, make sure all unit tests completed successfully.



Review all changes, make sure that only the code files (.cs) in StyleIssues project are changed.


Do not make any changes to project files (.csproj) or in code files in StyleIssues.Tests project.


Stage your changes.


All your changes are staged now.


Create a commit and push your changes to remote repository.

