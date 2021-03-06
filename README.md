# Static Code Analysis - Bernat Casañas
I am Bernat Casañas Masip [(Linkedin)](https://www.linkedin.com/in/bernat-casa%C3%B1as-masip-a91537160/), student of the Bachelor’s Degree in Video Games by UPC at CITM. This content is generated for the second year’s subject Project 2, under supervision of lecturer Marc Garrigó. [(Linkedin)](https://www.linkedin.com/in/mgarrigo/)<br>

[WebPage](https://bernatcasanas.github.io/Static-Code-Analysis/)

# Index
* [Introduction](#Introduction)
* [What is Static Code Analysis?](#What-is-Static-Code-Analysis?)
* [Static Analysis vs. Dynamic Analysis](#Static-Analysis-vs.-Dynamic-Analysis)
* [What can you do?](#What-Can-You-Do?)
* [Limitations](#Limitations)
* [Online Tool](#Online-Tool)
    * [Codacy](#Codacy)
    * [Codacy Tools](#Codacy-Tools)
* [Offline Tool](#Offline-Tool)
    * [Visual Code Grepper](#Visual-Code-Grepper)
    * [VCG Tools](#VCG-Tools)
* [Sources](#Sources)

# Introduction
I will talk about how to save a lot of hours in your life analysing code in search of invisible errors like memory leaks, unnecessary lines and alot of things that can make your project a better one. I will show you two different options, on of them online, and the other one offline.
# What is Static Code Analysis?
Static code analysis is a method of debugging by examining source code before a program is run. It’s done by analyzing a set of code against a set (or multiple sets) of coding rules. This type of analysis addresses weaknesses in source code that might lead to vulnerabilities. Of course, this may also be achieved through manual code reviews. But using automated tools is much more effective. <br>
![](https://github.com/BernatCasanas/Static-Code-Analysis/blob/master/Research%20Images/image-blog-what-is-static-analysis.jpg?raw=true)
# Static Analysis vs. Dynamic Analysis
I want to talk about the difference between dynamic and static analysis. Both of them detect defects, but the difference is where they find them. Static analysis identifies defects before you run a program and dynamic analysis do it after. <br>
However, some coding errors might not appear while you run the dynamic one. So, there are defects that dynamic testing might miss that static code analysis can find.

# What can you do?
1. Variable not initialized in the constructor
2. Variable used after element has been erased.
3. Memory Leaks
4. Variable never used
5. Useless code
6. Duplicated code
7. Commented TODO
8. Buffer Overflow

Static Analysis is particulary good at finding coding issues, like buffer overflow, memory leaks and null pointers.
# Limitations
1. No understanding of developer intent
We can't know the developer's intentions. Static code analysis can't know that you were expecting to get the area with a length + width.
```c++
int calculateArea(int length, int width)
{
    return (length + width);
}
```
2. The result cannot be known.
This means that the tools may not report actual defects. The code will stop when x = 0. The static analysis can't know that this is going to happen.
```c++
int divide(void)
{
    int x;
    if(foo())
    {
        x = 0;
    }
    else
    {
        x = 5;
    }
    return (10/x);
}
```

# Online Tool
## Codacy
What Codacy does? Automatically identify issues through static code review analysis. Get notified on security issues, code coverage, code duplication, and code complexity in every commit and pull request, directly from your current workflow. <br>
In three simple steps, you can add a static code analysis to your project:
1. Add your git repository
2. Codacy automatically detects issues
3. Get notified and take action

[![](http://img.youtube.com/vi/9kh8DA-To6w/0.jpg)](http://www.youtube.com/watch?v=9kh8DA-To6w "")
<br>
Here is the tutorial of how to link your project to Codacy. After that, you will have in the left menu all the options that i will explain below.

### Codacy Tools
* Progression Graphic
![](https://github.com/BernatCasanas/Static-Code-Analysis/blob/master/Research%20Images/Codacy/image.png?raw=true)

It shows a graphic of the last 30 days issues. You will have also all the issues in every section (security, error prone, etc). <br>
* Mistakes per Commit & Visual Branches
![](https://github.com/BernatCasanas/Static-Code-Analysis/blob/master/Research%20Images/Codacy/image%20(1).png?raw=true)

It shows all the commits of the project and how many issues were made in each one. It will show you also the branch flow.<br>
* Visual Errors in Files
![](https://github.com/BernatCasanas/Static-Code-Analysis/blob/master/Research%20Images/Codacy/image%20(3).png?raw=true)

It shows the issues in each file. It will also grade the code od the file.<br>
* List of Errors
![](https://github.com/BernatCasanas/Static-Code-Analysis/blob/master/Research%20Images/Codacy/image%20(4).png?raw=true)

It shows a wide list of issues. I don't recomend to look at them, but with an organization (in each file and with visually feedback).<br>
* Pull Request List
![](https://github.com/BernatCasanas/Static-Code-Analysis/blob/master/Research%20Images/Codacy/Captura.JPG?raw=true)

It shows a list of all the pendent pull requests and how many issues have each one. This is important to avoid merging branches with issues.<br>
* Security
![](https://github.com/BernatCasanas/Static-Code-Analysis/blob/master/Research%20Images/Codacy/dfsdf.JPG?raw=true)

It shows a list of security problems that your project can contain. This is not an important option for us but it is if you have a project with comercial purpose<br>

# Offline Tool
## Visual Code Grepper
What VCG does? Automatically identify issues through static code review analysis. Get notified on buffer overflows, signed/unsigned comparisons, ranking by severity the results, broken code, toDo comments and percentages of the lines/bugs/whitelines. <br>
In three simple steps, you can add a static code analysis to your project:
1. Download the software
2. insert the file directory in the text field
3. Click on full scan

[![](http://img.youtube.com/vi/HYohl3VthUA/0.jpg)](http://www.youtube.com/watch?v=HYohl3VthUA "")
Here is the tutorial of how to link your project to VCG. After that, you will have in the left menu all the options that i will explain below.

### VCG Tools
* List of errors
   * Severity
   * Title
   * Description
   * File
   * Line
  
![](https://github.com/BernatCasanas/Static-Code-Analysis/blob/master/Research%20Images/VCG/2.png?raw=true)
In a single page, the software will show you all the issues that your project have. It will also show the issues of the SDL library, so be careful touching something or having a mental breakdown when you see how many issues has. <br>
* Graphic

![](https://github.com/BernatCasanas/Static-Code-Analysis/blob/master/Research%20Images/VCG/1.png?raw=true)
It shows a graph of the total lines/ whitelines / comments / unfinished flags / dangerous code. <br>
All of this is drawn and put in brackets. This is not a very usefull tool, just for curiousity purposes.<br>

# Sources
* [Perforce](https://www.perforce.com/blog/sca/what-static-analysis)
* [Wikipedia](https://en.wikipedia.org/wiki/List_of_tools_for_static_code_analysis)
* [Wikipedia](https://en.wikipedia.org/wiki/Static_program_analysis)
* [Codegrip](https://www.codegrip.tech/productivity/guide-to-static-code-analysis/)
* [Youtube](https://www.youtube.com/watch?v=d_BCGvXbpKs)
* [Youtube](https://www.youtube.com/watch?v=Heor8BVa4A0)
* [Codacy](https://app.codacy.com/)
* [VisualCodeGrepper](https://sourceforge.net/projects/visualcodegrepp/files/)
