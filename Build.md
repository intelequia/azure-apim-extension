# Building an Azure DevOps Web Extension

To build an Azure DevOps web extension, follow these steps:

1. **Prerequisites**
    - Ensure you have Node.js and npm installed on your machine. You can download them from the official Node.js website: [Node.js](https://nodejs.org).

2. **Create a new directory**
    - Open a terminal or command prompt and navigate to the desired location where you want to create your extension project.
    - Run the following command to create a new directory for your extension:
      ```bash
      mkdir my-extension
      cd my-extension
      ```

3. **Initialize the project**
    - Run the following command to initialize a new Node.js project:
      ```bash
      npm init -y
      ```

4. **Install the Azure DevOps Extension SDK**
    - Run the following command to install the Azure DevOps Extension SDK:
      ```bash
      npm install azure-devops-extension-sdk --save
      ```

5. **Create your extension**
    - Create the necessary files and folders for your extension, such as HTML, CSS, and JavaScript files.
    - Refer to the [Azure DevOps Extension SDK documentation](https://docs.microsoft.com/azure/devops/extend/overview?view=azure-devops-extension-sdk-12) for more information on how to create and structure your extension.

6. **Build and package your extension**
    - Run the following command to build and package your extension:
      ```bash
      npm run build
      ```

7. **Publish your extension**
    - Follow the instructions in the [Publish an Azure DevOps extension](https://docs.microsoft.com/azure/devops/extend/publish/overview?view=azure-devops-extension-sdk-12) documentation to publish your extension to the Azure DevOps Marketplace.

That's it! You have now built and published your Azure DevOps web extension. For more detailed information and advanced topics, refer to the [Microsoft Learn documentation](https://docs.microsoft.com/learn/azure-devops/).

# Package and Publish
NOTE: before packaging, remember to increase your package version on the vss-extension.json file.

8. **Package your extension**
    - Run the following command to package your extension:
      ```bash
      tfx extension create --manifest-globs vss-extension.json
      ```
    - This command will create a VSIX package file for your extension.

9. **Publish your extension**
    - To publish your extension to the Azure DevOps Marketplace, you need to have an Azure DevOps organization and a publisher account.
    - Run the following command to publish your extension:
      ```bash
      tfx extension publish --service-url https://dev.azure.com/{organization} --token {PAT}
      ```
    - Replace `{organization}` with your Azure DevOps organization name and `{PAT}` with a Personal Access Token (PAT) that has the necessary permissions to publish extensions.
    - This command will publish your extension to the Azure DevOps Marketplace.

    NOTE: alternatively, you can publish your extension using the GUI available at https://marketplace.visualstudio.com/manage/publishers/{organization} where organization is the name of your publisher company.

That's it! You have now packaged and published your Azure DevOps web extension. Congratulations!