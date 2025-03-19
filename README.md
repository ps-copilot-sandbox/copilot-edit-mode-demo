# GitHub Copilot Edit mode

![GitHub Copilot Edit](images/coverEditMode.jpeg)

In this tutorial, you will learn how to leverage the GitHub Copilot feature called "Edit mode" to enhance your coding experience. Introduced with the release of Visual Studio 2022 version 17.13 and later, Copilot Edit is designed to help iterating across multiple-files more efficient.

Here is the link where you can find more about the GitHub Copilot Edit mode:

[GitHub Copilot Edit mode](https://code.visualstudio.com/docs/copilot/copilot-edits)

## Prerequisites

- Visual Studio 2022 version 17.13 or later
- GitHub Copilot extension installed
- GitHub Copilot license

Once you have that setup, make sure that you logged in to your GitHub account in Visual Studio Code. There are different ways to login, but the easiest way is to click on the `user icon` in the bottom left corner of the Visual Studio Code window and select `Sign in to GitHub`. This will open a new window where you can enter your GitHub credentials. Once you are logged in, you should click the `GitHub Copilot` icon in the top next to the search bar. This will give different options, and you should select `Open Chat`. This will open a new window where you can interact with the GitHub Copilot.

To use the GitHub Copilot Edit mode, you need to select the `Edit` option in the GitHub Copilot window. This will enable the Edit mode, which allows you to edit code across multiple files in your project.

## Introduction

**GitHub Copilot Edit** mode is a powerful feature that allows you to edit code across multiple files in your project. However, the caveat is that, with Copilot being generative in nature, it can generate different results each time you invoke it. This gives quite a challenge for someone who is writing a step-by-step tutorial, as the results may not be consistent. To mitigate this, will focus on the high level concepts and provide a few examples to illustrate the functionality of Copilot Edit mode. The biggest takeway for this tutorial is to understand how to use the Copilot Edit mode effectively, rather than focusing on what you really build with it through this tutorial.

> **Note:** Focus on the high level concepts and how to use the Copilot Edit mode effectively, rather than focusing on what you really build with it through this tutorial. The examples provided are just to illustrate the functionality of Copilot Edit mode.

One way to think about GitHub Copilot is like a football. You still have a control, but it can bounce in a different way.

![Football bouncing](images/Introduction/1_footballBouncing.jpeg)

For example, if I ask a question about `how to create a stock application`, I can get very different results based on when I try it.

![Stock application](images/Introduction/2_GitHubCopilotDoingThings.jpg)

For a practioner, this is not bad but maybe even great! However, for someone who is writing a step-by-step tutorial, this can be a challenge. The results may not be consistent and it can be hard to follow along.

Thus, please remind yourself that the goal of this tutorial is to understand how to use the Copilot Edit mode effectively, rather than focusing on what you really build with it through this tutorial. The examples provided are just to illustrate the functionality of Copilot Edit mode.

Now, let's get started with the tutorial!

## Step 1: Start exploring the Copilot Edit mode window

We will start by exploring a simple example of how to use the Copilot Edit mode. Before you start, make sure that you met all the prerequisites above.

Once you have a Copilot Chat window open in `Edit mode`, it will look something like this:

![Copilot Chat Open](images/Exploring/1_CopilotChatOpen.jpg)

You have few options there, but let's take a look at two:

![Option panel from Copilot Chat](images/Exploring/2_OptionPanel.jpg)

- `Add Files`: This will add files to your project. As you keep working on with Edit mode, it can automatically reference so it can use those files as the part of the context. However, to make it more relevant, you can manually add or remove files.
- `Model selection`: You can choose the model from the available options like `GPT-4o` or `Gemini 2.0 Flash`, etc. Your team may already give an instruction to use a specific model, or you may get different results based on the model you choose.

Later, you will see "agent mode," which is even one more step magical from the current Copilot Edit mode. For now, let's focus on the Edit mode and how to use it effectively.

## Step 2: Let's start with a very simple first

Before we start, we need to add a folder so Copilot Edit can work from there. From the top menu, click **File** then select the **Add Folder to Workspace** option from the dropdown menu. This will open a new window where you can select the folder you want to add. Once you have selected the folder or created a new folder to add, click the **Add** button to add it to your workspace.

![Add folder to workspace](images/SimpleExample/1_AddFolderWorkspace.jpg)

Next, we will create a new file in the folder we just added. To do this, right-click on the folder and select **New File** from the context menu. This will open a new file in the editor where you can start writing your code. I named my file as `calculator.js`.

![Create new file](images/SimpleExample/2_CreateNewFile.jpg)

From the file we just created, we will start with a simple prompt. 

```javascript
// function to calculate the sum of two numbers
```

![Simple prompt](images/SimpleExample/3_WriteComment.jpg)

Once you have written the comment, you can hit the `Tab` key to let Copilot Edit mode generate the code for you. This will automatically generate the code based on the comment you wrote.

Hit the enter button to proceed further. Most likely, you will see GitHub Copilot suggesting another suggestion based on the previous pattern.

![GitHub Copilot suggestion](images/SimpleExample/4_AddOneMore.jpg)

You can hit the `Tab` key and then `Enter` to accept the suggestion.

There is a cool feature within GitHub Copilot through in-file. In Windows, right click on either the selected lines or the file itself, then select `Copilot`. From there, you will see different options like `Explain` or `Fix`. For now, let's select `Explain` to see how Copilot can explain the code you just wrote.

![Explain code](images/SimpleExample/5_AskCopilotInPanel.jpg)

This will generate an explanation of the code you wrote through **Copilot Chat** panel. 

![Copilot Chat panel](images/SimpleExample/6_CopilotChatExplained.jpg)

If you selected other option like `Editor Inline Chat`, you can even ask to change things without opening the Copilot Chat panel.

Next, we will finally try to leverage **GitHub Copilot Edit** mode. To do this, we will select the **Copilot Edits** option from the Copilot Chat panel. This will open a new window where you can start editing your code across multiple files in your project. From there, ask the following question:

```javascript
Can you implement the functionality to build different calculation examples?
```

The reason why we are asking such a simple question is that because we want to demonstrate somewhat more predictable answer from Copilot before going into too deeper dive into it. In this way, we can still grasp the value of Copilot Edit mode without getting lost in the details.

As soon as you asked, you will see GitHub Copilot picking up that file and started to work on it.

![Copilot Edit mode](images/SimpleExample/7_CopilotEditAsk.jpg)

In your file, you will see that Copilot is doing some magic to generate the code.

![Copilot doing magic](images/SimpleExample/8_CopilotEditInProgress.jpg)

However, at the end of it, you will see that GitHub Copilot still waiting for you to accept the code.

![Copilot waiting for you](images/SimpleExample/9_CopilotEditKeep.jpg)

Once it is done, you will see that the GitHub Copilot Edit mode stopped working on the file.

![Copilot Edit mode stopped](images/SimpleExample/10_CopilotEditChatWaiting.jpg)

The main difference between the **Copilot Chat** and **Copilot Edit mode** is that the Copilot Edit mode actually can start modifying your files while the Copilot Chat just gives you suggestions and file lines where you can take further action. Later, within GitHub Copilot Agent mode, it will even have files to interact with the terminal to compile, run, and test your code.

Returning back to the Copilot Edit mode chat panel, what will happen if you hit that blue **Done** button?

![Copilot Edit mode done](images/SimpleExample/11_CopilotEditDone.jpg)

Let's hit that button now. You will see that action clears the Copilot Edit mode screen.

![Copilot Edit mode cleared](images/SimpleExample/12_CopilotEditClean.jpg)

> **WARNING**: Be careful if you hit that button, because it will clear the Copilot Edit mode screen and you will lose all the context. So, make sure that you are done with your work before hitting that button.

That is it for our sample demonstration of **Copilot Edit** mode. Let's move on to little more complex but a cool example.

## Step 3: Let's build a stock application

In this example, we will build a simple stock application using the Copilot Edit mode. The goal is to demonstrate how to use the Copilot Edit mode to build a more complex application.