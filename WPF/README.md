# Windows Presentation Foundation

This repository is dedicated to learning WPF ranging from the basics such as its syntax, framework, features, all the way to advanced features such as networking, design pattern (such as MVVM), localization, customized controls, and complex bindings.

# Open Source Project Tear Down

There are many good quality open source projects on GitHub that are written with WPF. To give an example there is the "ScreenToGif" app, which demonstrated many key concepts such as how to manage resource dictionaries, how to customize control behavior, how to make notification tray icon, etc.

Learning by tearing open source projects down can deepen the understanding of the framework and make us understand the ideas behind each design.

## Horizontal tear down

One way to do an open source project tear down is to do it horizontally. Which is to observe what is happening on a grand scale. To understand what kind of tasks the application are performing as a whole.

The main goal is to see how a well-designed and nicely-built WPF app uses overarching design patterns so that all the functionalities orchestrates together so that each part makes sense in a bigger picture.

This can be done by observing the behavior of the app in action, what kind of response it is feeding back, .etc.

## Vertical tear down

The other way is to isolate the project's singular function, and observe how it is interacting with other components. Now this might feel like the decoupling process of the DI pattern, where we supply with a singular unit functionality with mock up interfaces for it to interact with and then try to test the unit functionality. Only instead of testing, we are tearing it down and hopefully trying to replicate it.

The goal for vertical tear down is to find a way to replicate a singular function on our own for more generalized function.