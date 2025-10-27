# My Coding Notebook

## Table of Contents
- [Flutter notes](#flutter-notes)
  - [What is flutter?](#what-is-flutter)
  - [Key Terms & definitions](#key-terms-and-definitions)
  - [Layout and Design Widgets](#Layout-and-Design-Widgets)
  -  [Definitions with structures](#flutter-definitions-with-structures)
- [Code Definitions](#code_definitions)
- [Notebook Style Guide](#markdown-style-guide-for-coding-notebooks)


## Flutter Notes

###  What is Flutter?
- Definition: A framework made by Google for building apps that work on web, Andriod, IOS with one codebase
- Why is it useful? Uses the dart program

---

###  Key Terms and Definitions

| Term             | Definition                                      | Example / Notes                          |
|------------------|--------------------------------------------------|-------------------------------------------|
| Widget           | Basic buliding block of a flutter app. everything is a widget                                                |                                           |
| MaterialApp      | The root of the app. Sets up routes and themes                                                  |                                           |
| Scaffold         |  Provides basic visual layout like a header,body,floating button                                                |                                           |
| StatelessWidget  | A widget that doesnt save                                                  |                                           |
| StatefulWidget   | A widget that can change over time                                                  |                                           |
| Navigator        | manage screen transitions                                                 |                                           |
| AppBar           | Top navigation bar                                                  |                                           |
| Column           |  vertical lay out                                |                                           |
| Row              |  Horzatial lay out                               |                                           |
| Container        |  Wraps content with padding, margin, or color                                                |                                           |
| Text             |  Displays text                                   |                                           |
| Image.network    | Displays images from url                         |                                           |
| Padding          | Adds space around the widget
|Center            | Centers its child
|Named routes      | Predefined paths to navigate between screens
|Main              | The function that runs the app
---

### Layout and Design Widgets
- How do you center a widget? Center
- How do you align something to the left or right? Column
- What widget adds space around content? Padding



## Flutter Definitions

| Term | Definition and Description | Base Structure | Real Life Example | App Example |

|------|----------------------------|----------------|-------------------|-------------|
|
|      | A function that runs when your app starts. It tells Flutter what app to show. | `void main() => runApp(MyApp());` |  |  |
main.dart void main() => runApp(MyPortfolioApp());
|      | The widget that sets up your whole app’s look and navigation. | `MaterialApp(...)` |  |  |
   main.dart return MaterialApp( debugShowCheckedModeBanner: false,  title:'TSA Portfolio', theme: ThemeData(
|      | A widget that gives you the basic layout: background, navigation bar, floating button, etc. | `Scaffold(...)` |  |  |
in showcase.dart return Scaffold( body: Column( mainAxisAlignment: MainAxisAlignment.start,  children: [
|      | A widget that holds and displays your content in a straight line from top to bottom. | `Column(...)` |  |  |
in background.dart  child: Column( children: [  Text(   title,
|      | A widget that shows things side-by-side. | `Row(...)` |  |  |
in infocard.dart   child: Row(  children: [   ClipRRect(
|      | A box that holds other widgets. You can add color, padding, borders, or size. | `Container(...)` |  |  |
in showcase.dart Column( children:     const Padding(      padding: EdgeInsets.all(8.0),
|      | A widget to display text on the screen. | `Text('Hello')` |  |  |
in infocxard.dart  child: Text(   description,  style: const TextStyle(color: Colors.white),
|      | A widget to show an image using a link from the internet. | `Image.network('https://...')` |  |  |
in home.dart child: Image.network( 'https://placedog.net/640/480?random',fit: BoxFit.cover,
|      | A clickable button that floats above content. You choose what happens when it's clicked. | `ElevatedButton(onPressed: ..., child: ...)` |  |  |
in home.dart ElevatedButton(onPressed: () => Navigator.pushNamed(context, '/background'),  child: const Text('Next'),
|      | The code that gets run when a button is tapped or something happens | `onPressed: () => doSomething()` |  |  |
in home.dart onPressed: () => Navigator.pushNamed(context, '/background')  child: const Text('Next'),
|      | A class that creates widgets that never change. Good for static screens. | `class HomeScreen extends StatelessWidget` |  |  |
in home.adrt class HomeScreen extends StatelessWidget {
|      | A class for widgets that can change while the app is running. | `class MyWidget extends StatefulWidget` |  |  |
class BackgroundScreen extends StatefulWidget 
|      | Lets you move from one screen to another using route names. | `Navigator.pushNamed(context, '/about')` |  |  |
in home.dart Navigator.pushNamed(context, '/background')
|      | Makes space around a widget inside its container. | `Padding(padding: EdgeInsets.all(8.0), child: ...)` |  |  |
in showcase.dart  return Padding(padding: const EdgeInsets.all(4.0) child: Image.network(url, width: 100, height: 100, fit: BoxFit.cover),    );
|      | Aligns content in the center of the screen or container. | `Center(child: ...)` |  |  |
in background.dart  mainAxisAlignment: MainAxisAlignment.center, children:
|      | Automatically puts widgets onto a new line when there's no space. | `Wrap(children: [...])` |  |  |
in showcase.dart Wrap(alignment: WrapAlignment.center, children: puppyUrls.map((url) => puppyImage(url)).toList()),
|      | This marks a method as one that’s replacing a method in a parent class. | `@override` |  |  |
in home.dart @override
|      | The special function in every widget that describes what gets drawn on the screen. | `Widget build(BuildContext context) {...}` |  |  |
in home.dart Widget build(BuildContext context)   return Scaffold(    body: Center(  child: Column(
|      | Required in every widget class to describe what to show. | `build` |  |  |
in AltDesignScreen.dart build
|      | A variable that helps the widget know where it is and lets it communicate with the app. | `BuildContext context` |  |  |
in home.dart (BuildContext context) 
|      | A keyword used to pass a value to the parent widget. | `super.key` |  |  |
in main.dart  const MyPortfolioApp ({super.key});
|      | A keyword that means the value won't change and is set once. | `const` |  |  |
   in main.dart     textTheme: const TextTheme(











## Code definitions 

| Term | Definition | Base Structure / Syntax | Real Life Example | App Example |

|------|------------|--------------------------|-------------------|-------------|

|     | A named container used to store a value that may change. | `var x = 5;` |  |  |

|      | A fixed value that cannot change once set. | `const PI = 3.14;` |  |  |

|      | The kind of value a variable holds, like numbers or text. | `int`, `String`, `bool` |  |  |

|      | A sequence of characters used to represent words or text. | `"Hello World"` |  |  |

|      | Whole number values. | `int age = 16;` |  |  |

|      | Number values with decimals. | `double age = 16.2;` |  |  |

|      | A value that can be true or false. | `bool isLoggedIn = false;` |  |  |

|      | A collection of values in a specific order. | `List<String> names = [];` |  |  |

|      | A special value that means “nothing.” | `String? name = null;` |  |  |

|      | A reusable block of code that performs an action. | `void sayHi() { print("Hi"); }` |  |  |

|      | The information passed into a function to change how it works. | `greet(String name)` |  |  |

|      | The result a function gives back. | `return total;` |  |  |

|      | Where a variable or function can be used. | (No set syntax — concept-based) |  |  |

|      | Blueprint for creating objects with specific structure and behavior. | `class Dog {}` |  |  |

|      | A specific version of a class. | `Dog myDog = Dog();` |  |  |

|      | A variable that belongs to a class/object. | `String name;` |  |  |

|      | A function that belongs to a class. | `void bark() {}` |  |  |

|      | A special function used to set up a class when it’s created. | `Dog(this.name);` |  |  |

|      | Hiding the inner workings of code so users only interact with what they need. | (Concept — not specific code) |  |  |

|      | Changing how a built-in or inherited function behaves. | `@override` |  |  |

|      | A function that does not return a value. | `void printMessage() {}` |  |  |
| Scanner | Creates a scanner object to take input from user | Scanner in new Scanner(system.in);  |  |  |
| import scanner | Gives acess to scanner class, required at top | import java.util.Scanner |  |  |
| prinit line statement | prints what's in the parenthesis | System.out.printIn(" ")  |  |  |
| print statement | prints the content in the parenthesis | System.out.print(" ") |  |  |
| input nextLine | reads in a String from the user  | input.nextLine(); |  |  |
| input nextInt|reads in a int from the user | input.nextInt();  |  |  |
| input nextDouble | reads in a double (decimal) from user  | input.nextDouble();  |  |  |
| input nextBoolean | reads in a boolean (true/false) from the user  | input.nextBoolean();  |  |  |
| Arithmetic operators |- * / % (modulus, returns the remainder from dividing)  |  |  |  |
| compound operators(applies the result to the variable) |+= -= *= /= %= ++ (adds 1)  |  |  |  |













## Markdown Style Guide for Coding Notebooks

Follow this guide to keep your coding notebook **clear, consistent, and professional**.  
This ensures your notes are easy for you (and others) to read later.

---

## 🔹 Headings
**When to use:** Organize your notebook into sections (like days, topics, or projects).  
- `#` for the notebook title (use once at the top).  
- `##` for each day or major topic.  
- `###` for subsections (like "Notes", "Practice", "Reflections").  

✅ Example:



## Day 1
### Notes
### Practice

🔡 Text Formatting
When to use: Highlight important ideas or add emphasis.

Use bold for key terms or definitions.

Use italic for emphasis or side comments.

Use inline code for keywords, functions, or commands.

 

✅ Example:

**Class** = a blueprint for objects  
*Remember:* always test your code  
Use `System.out.println()` to print

 

💻 Code Blocks
When to use: Anytime you write multiple lines of code.

Inline code for short snippets.

Fenced code blocks with language for full examples.

✅ Example:

```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello World!");
    }
}
```

🧾 Lists
When to use: Organize steps, notes, or key points.

Numbered lists for sequences or steps.

Bulleted lists for unordered ideas.

✅ Example:

1. Define the class
2. Write the main method
3. Test your program

Variables
- Loops
- Conditionals
 

✅ Checklists
When to use: Track progress on assignments or tasks.

✅ Example:

[x] Complete coding warm-up
- [ ] Finish project draft
- [ ] Reflect on learning

 

➡️ Blockquotes
When to use: Call out notes, reminders, or teacher comments.

✅ Example:

> 💡 Remember: Loops repeat code until a condition is false.

 

📊 Tables
When to use: Compare values, track progress, or organize data neatly.

✅ Example:

| Task        | Status   | Notes          |
|-------------|----------|----------------|
| Homework 1  | Done ✅  | Submitted      |
| Homework 2  | Pending  | Needs review   |

 

🔗 Links & Images
When to use: Add references, resources, or visuals.

✅ Example:

[Java Docs](https://docs.oracle.com/javase/8/docs/api/)  
![Markdown Logo](https://upload.wikimedia.org/wikipedia/commons/4/48/Markdown-mark.svg)

 

📂 Collapsible Sections
When to use: Hide solutions, extended notes, or extra details.

✅ Example:

<details>
  <summary>Click to reveal solution</summary>
  
System.out.println("Answer: 42");

</details>

 

📝 Footnotes
When to use: Add references or side notes without cluttering the page.

✅ Example:

This concept is related to object-oriented programming.[^1]

[^1]: See "Objects and Classes" in your textbook.

 

🎯 Style Rules
Consistency matters more than creativity

Always use headings to structure your notes.

Always use code blocks for multi-line code.

Clarity first

Bold key terms.

Use lists instead of long sentences when outlining steps.

Professional tone

Don’t mix casual notes with formal work in the same section.

Use blockquotes for reflections or teacher feedback.

Track your learning

Use checklists to mark what’s done.

Use collapsible sections if you want to hide answers until review time.

 

✅ Bottom Line:

Headings = Structure

Bold/Italic = Emphasis

Code blocks = Code

Lists = Steps/Ideas

Tables = Organization

Checklists = Progress

Blockquotes = Notes/Tips

Collapsible = Hide/Show detail

Keep it simple, consistent, and clear.
