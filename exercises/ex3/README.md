# Exercise 3 - Enhance your MDK App using Generative AI via Joule

## Estimated time

:clock4: 10 minutes

In this exercise, you will learn how to enhance an MDK App using GenAI via Joule Assistant, available in the SAP Build Code development environment. You will generate an MDK page in an existing MDK project using the Joule functionality in the Build Code.

 - [Exercise 3.1 - Generate a new MDK Page Displaying a Customer List](#exercise-31---generate-a-new-mdk-page-displaying-a-customer-list)
- [Exercise 3.2 - Navigate to the New Customer List Page](#exercise-32---navigate-to-the-new-customer-list-page)
- [Exercise 3.3 -Redeploy the Application](#exercise-33---redeploy-the-application)
- [Exercise 3.4 - Run the App](#exercise-34---run-the-app)
- [Summary](#summary)

### Exercise 3.1 - Generate a New MDK Page Displaying a Customer List

The template generates a project displaying a list in an Object Table format. When navigating to the _Customers_ list in the app, you will notice that each customer has a phone number, email, etc., as contact points. Application users must manually type either the phone number or email address to contact a customer, which is quite cumbersome.
In this step, you will generate a new page or screen that allows users to contact a customer with a single tap, enhancing the user experience.

1. Open the **Joule** panel. 

    ![MDK](images/3.1.1.png) 

2. Type `/` to access the available MDK commands, select `mdk-gen-page` to generate a page, choose the service file, type the following prompt, and click the play icon to generate the required information:

    ```Text
    generate a page display customer information in a contact cell control

    ```
    ![MDK](images/3.1.2.gif) 

>There is a [Contact Cell UI](https://experience.sap.com/fiori-design-ios/article/contact-cell/) available in MDK that provides quick access to various methods of communicating with a contact. 

3. Review the generated artifects/files. Once satisfied, accept all the files one by one. The accepted files will be added to the project.

    ![MDK](images/3.1.3.png) 

    The Generated page is now available in the project.

    ![MDK](images/3.1.4.png)   

### Exercise 3.2 - Navigate to the New Customer List Page

1. You will now bind this new page to the `Customers` button on the `Main.page`. 

    Navigate to `Pages` | `Main.page` to open it in the MDK page editor. Select `Customers`, navigate to the `Events` tab, and click the `Jump to` button. 

    ![MDK](images/3.2.1.png) 

2. When the `Customers` button is tapped on the main page, a navigation action is triggered to open a target page. With the template generated project, it is currently bound to the `/MDKApp/Pages/com_sap_edm_sampleservice_v4_Customers/Customers_List.page`. 

    ![MDK](images/3.2.2.png) 

3. Replace it with the new page generated by Joule. Click the dropdown menu and select the new page.

    ![MDK](images/3.2.3.png) 


### Exercise 3.3 - Redeploy the Application

Right-click the `Application.app` file in the project explorer pane, select **MDK: Deploy**, and then choose the deployment target as **Mobile Services**.

### Exercise 3.4 - Run the App

| Steps&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Android&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | iOS&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  |
| --- | --- | --- |
| 1. Tap **Check for Updates** in the user menu on the Main page. | ![MDK](images/3.6.1.png) | ![MDK](images/3.6.2.png) |
| 2. A _New Version Available_ pop-up will appear, tap **Now**. | ![MDK](images/3.6.3.png) | ![MDK](images/3.6.4.png) |
| 3. After accepting the app update, the latest changes will appear in the MDK client. Tap **Customers** to see the updated UI. The end user can now easily contact a customer by tapping items like call, email, etc. This page also supports swipe left and right functionality for quick actions.  | ![MDK](images/3.6.5.gif) | ![MDK](images/3.6.6.gif) |

## Summary
 
Congratulations on successfully completing the exercises! You have learned how to develop an end-to-end mobile application in SAP Build Code and run it on your mobile device. There is always more to learn and explore. To continue advancing your skills, we encourage you to follow these [set of tutorials](https://help.sap.com/doc/f53c64b93e5140918d676b927a3cd65b/Cloud/en-US/docs-en/guides/getting-started/mdk/overview.html#tutorials) to further your mobile development journey.