## This Project "cloud formation" is a project that aim to hold different cloud formation concepts and best practices in practice. ##

1. **non-portable Template**  
A cloud formation template is said to be non-portable when that template can not be use to;          
    *   Create a physical Resources from the stack generated from the logical resources on the template more than once without deleting the stack from Aws before running the stack create command again.

    This can be as a result of hard-coding values on the properties of the logical resources in your template, thereby making the values of those properties static.

    Now, when such a template is used to provision resources on your aws account, such template cannot be used to provision another set of the same specified resources in the template atleast not without editing those value and/or deleting the set of physical resources that was created from the last provisioning, because aws will always flag the error "resources already exist". The concept of non-portable template can be seen from running this project [non-portable-sample-template](https://github.com/oriafo/cloud-formation/blob/master/cloud%20formation/non-portable-sample-template.yaml) more than once without deleting the physical resource created from running it the first time

    Now, this template is not optimize, for the above stated reason. One of the core concept of automating the creation of your cloud infrastructure is for ease of deployment of this infrastructure in any environment, region etc., without always editing this template to suit your current need. Basically for reuseability. The template should be written in an optimize way in that the values to this properties should be dyamically updated.

    Optimizing your cloud formation template can be done using Template parameter, Psuedo parameter, Mappings, intriscic functions and some other concept.

