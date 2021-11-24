<h1 align="center">Assignmenty Bot</h1>  

</p>

<p align="center">
   <img src="https://img.shields.io/badge/language-python-blue?style"/>
   <img src="https://img.shields.io/github/license/ShreyamMaity/Assignmenty"/>
   <img src="https://img.shields.io/github/stars/ShreyamMaity/Assignmenty"/>
   <img src="https://img.shields.io/github/forks/ShreyamMaity/Assignmenty"/>
   <img src="https://img.shields.io/static/v1?label=%F0%9F%8C%9F&message=If%20Useful&style=style=flat&color=BC4E99" alt="Star Badge"/>
   <img src=https://visitor-badge.glitch.me/badge?page_id=ShreyamMaity.Assignmenty"/>
</p>

----

> Just Code and Push , Leave The Assignment Part on us....Happy Coding </>
  
<p align="center">
   

https://user-images.githubusercontent.com/38105595/143308377-c08db022-9809-4a4d-9cbe-22097399f06b.mp4


</p>
       

- This is a [GitHub Action](https://developer.github.com/actions/) to create your assignment automatically with the help of git version control.

- It takes code and snaps from your latest commit and make it an assignment and send you in mail📧

- This action runs in a Docker container and therefore only supports Linux🐧
                                                          
- [Watch Full Config Video Here](https://youtu.be/OWB7oYtS9N8)
-----
## Prep Work

1. Create you coding assignments like or [Watch Config Video Here](https://youtu.be/OWB7oYtS9N8?t=17) 
    ```bash
    ``` This is Your Question , Write Questions like this```

    def code():
        this is your code. Just code anything

    ```
2. Save the code file as `assignment12.py` or `assignment34.py`
   > This action currently supports only  **Python Code Assignments** 🐍<br/>
   > but this GitHub Action can me modified for any code based asssignments.Feel free to contribute.🤗
   - You can use [this](#usage) example to work it out 🧐
3. create a github repo and clone it, then add a action config (`.yml`) file.Steps are avialable [here](https://youtu.be/OWB7oYtS9N8?t=76) for more info 🤔
4. Add a template docx file and name it `tmplate.docx` or use my template and modify it. Check the template [here](./content/template.docx) 📑
5. save the template file , action config file in your github repo 🐙
6. Push your code with snaps and Enjoy 😍

  
-----

## Usage :

The following example [workflow step](https://help.github.com/en/actions/configuring-and-managing-workflows/configuring-a-workflow) will get your latest commit and take the code file and snaps to form a `.docx` based assignment and send you via mail. 

-   ```yml
    name: Assignmenty Mailer
    on: 
    push:
        branches:
        - main
    workflow_dispatch:
    jobs:
    mailer:
        runs-on: ubuntu-latest
        steps:
        - uses: actions/checkout@v2
            with:
            fetch-depth: 2
        - uses: ShreyamMaity/Assignmenty@main 
            with:
            MAILID : 'sample@gmail.com' #mail if of your choice
            FILENAME : 'assignment' #assignment file name
    ```
Just copy the above code and paste it in your `.yml` file
or watch this video to understand how to config.[Watch Config Video Here](https://youtu.be/OWB7oYtS9N8?t=76)  
                                                          
----
  

## Options ⚙️

The following input variable options can/must be configured:

|Input variable|Necessity|Description|
|--------------------|--------|-----------|
|`MAILID`|Required|your mail id where you want to recieve the assignment|
|`FILENAME`|Required|your assignment file name|

----
## Action Config Guide

- ## Dir Methord :
    - Create a `.github/workflows` directory in your repository on GitHub if this directory does not already exist.
    - In the `.github/workflows` directory, create a file named `mailer.yml`.
    - open the `mailer.yml` file and paste this code :
        ```yml
        name: Assignmenty Mailer
        on: 
        push:
            branches:
            - main
        workflow_dispatch:
        jobs:
        mailer:
            runs-on: ubuntu-latest
            steps:
            - uses: actions/checkout@v2
                with:
                fetch-depth: 2
            - uses: ShreyamMaity/Assignmenty@main 
                with:
                MAILID : 'sample@gmail.com' #mail if of your choice
                FILENAME : 'assignment' #assignment file name
        ```
- ## UI Methord :
    - go to the `Actions` tab in your github repository
    - press `set up a workflow yourself` 
    - Delete the base code and paste above code
    - start commit 
    - and all set
-----
## Author

The Copy Paste GitHub action is written by [Shreyam Maity](https://github.com/ShreyamMaity)

-----

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT) - see the [LICENSE](LICENSE) file for details.

