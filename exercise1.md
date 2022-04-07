How to make Continuous Integration/Continuous Deployment pipeline for a Python project?

Firstly, a small software is needed. Pylint or flake8 is linter which analyze python code for errors.
Linter makes sure that the code is easy to read also for other developers.
It is recommended to use automate testing. Python unit test is for testing a single function or unit. In unit testing pieces of code return values are compared to the expected values. Testing can be done for example with pytest. Make sure that your tests are passing. 
When everything is working locally it is time to push the code to GitHub. In the .github/workflows folder there should be YAML file which include step by step jobs that are done during the workflow. YAML stands for Yet Another Markup Language and it is like JSON text specification language. When any changes are created to the code ja pushed to the GitHub workflow should start the building. 
Basic build includes following steps:
-	Install dependencies
-	Run linter
-	Run tests
The little red cross beside the Github action workflow indicates that build has failed. Some more information as to why it failed can be found on the build link. Then the code should be edited and pushed again to GitHub and the workflow runs again. The green success mark tells that build is completed successfully.

Sources:
https://realpython.com/python-continuous-integration/
https://www.asapdevelopers.com/python-for-ci-cd/
https://www.linkedin.com/pulse/implementing-simple-python-cicd-pipeline-using-github-tom-reid
