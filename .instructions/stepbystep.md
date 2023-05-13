## Step by step instructions


> NOTE: You're welcome to follow along using these steps but we have a guided CodeTour option that displays the instructions directly in the VSCode editor if you prefer. To use the CodeTour, follow the instructions in the [Using CodeTour](./using-CodeTour.md) file.
---
:bulb:  When you see the :leftwards_arrow_with_hook: symbol, you need to press the ENTER key.


1. For our exercises, you'll get started by navigating to the appropriate repo and choosing '**Use this template**', and '**Open in a codespace**'

<img width="601" alt="Open in a Codespace" src="../assets/Open in a Codespace.png">

2. Ensure you can see the files in the **Explorer view**. If not, click the **Explorer View icon** on the left sidebar of your editor.

<img width="398" alt="Code Explorer View" src="../assets/Code Explorer View.png">

3. Double click on the `variables.tf` file in the Explorer view. This file defines the inputs required to deploy an Azure VM. We won't be editing this file. Simply by having this file open in a tab, it will provide additional context to GitHub Copilot to enhance the suggestions Copilot will present.

4. Double click on the `main.tf` file in the Explorer view. This is the Terraform script we are going to edit. We've already defined some resources like a resources group and a VNET. We are going to add Azure VM resource definition.

<img width="692" alt="Open in a Codespace" src="../assets/Variables and main files open.png">

5. Let's add a Security Group resource to our Terraform file. Navigate to the end of the main.tf file and add the following comment.

```// Security Group```  :leftwards_arrow_with_hook:

6. Copilot should now suggest the code block to use for a Security Group. Once it appears, press **TAB** then **ENTER** to accept the suggestion.

<img width="618" alt="Code Explorer View" src="../assets/Copilot - Security Group Suggestion.png">

7. Next, let's associate our new security group with the existing network interfaces defined earlier in the Terraform file. At the end of the `main.tf` file, add the following comment.

```// Main network interface security group association```  :leftwards_arrow_with_hook:

8. Copilot should now suggest the code block to use to assocaite the new security group with the existing network interfaces. Once it appears, press **TAB** then **ENTER** to accept the suggestion.

<img width="611" alt="Code Explorer View" src="../assets/Copilot - Network Suggestion.png">

9. Finally, let's define an Azure VM resource. At the end of the `main.tf` file, add the following comment.

```// Virtual Machine```   :leftwards_arrow_with_hook:

10. Copilot should now suggest the code block to use to create a Virtual Machine. Once it appears, press **TAB** then **ENTER** to accept the suggestion. Notice how the suggested code block references resources defined previously.


---
### Wrap up

You have seen a quick preview of some of the power of GitHub Copilot and how it can help you work with Terraform files. Remember, GitHub Copilot is probabalistic so you may not get the exact same code suggestions as we did. If you're not happy with the suggestions, you can always press **CTRL + Z** to undo the changes and try again.

### Challenge exercises

This is the end of this instructions, but if this is not enough for you, here are some more interesting topics to try.

- Use `tfsec` to verify that the code suggested by GitHub Copilot follows best practices. This codespace comes with `tfsec` and the `tfsec` extension pre-installed.
- Try to improve the code suggested by Copilot by yourself. For example, try to change the size of Azure VM, change the OS of Azure VM, or change the network interface of Azure VM to another one.
- Try writing documentation for this Terraform script; GitHub Copilot will make suggestions for natural language documentation as well. Try writing documentation for this script and see what suggestions GitHub Copilot gives you.
 - Try writing your own Terraform script. Try creating a new file and writing a Terraform script and see what suggestions GitHub Copilot makes. You will probably find that on a completely new file, GitHub Copilot's suggestions are often not exactly what you intended. At that point, you may want to write some resource definitions yourself, or write detailed comments.
