## This Project "cloud formation" is a project that aim to hold different cloud formation concepts and best practices in practice. ##

1. **non-portable Template**  
A cloud formation template is said to be non-portable when that template can not be use to;          
    *   Create a physical Resources from the stack generated from the logical resources on the template more than once without deleting the stack from Aws before running the stack create command again.

    This can be as a result of hard-coding values on the properties of the logical resources in your template, thereby making the values of those properties static.

    Now, when sure a template is used to provision resources on your aws account, such template cannot be used to provision another set of the same specified resources in the template atleast not without editing those value and/or deleting the set of physical resources that was created from the last, because aws will always flag an error of resources already exist. the concept of non-portable template can be seen from running this project [non-portable-sample-template](https://github.com/oriafo/cloud-formation/blob/master/cloud%20formation/non-portable-sample-template.yaml) more than once without deleting the physical resource created from running it the first time

    Now, this is not the best way of building u

