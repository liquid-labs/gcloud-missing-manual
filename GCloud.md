
```mermaid
erDiagram
Cloud }o--|| Organization : "has many"
Cloud }o--|| Region : "has many"
Region }o--|| Zone : "has many"

Organization }o--|| Folder : "has many"
Organization }o--|| Project : "has many"
Folder }o..|| Project : "has many"
Project |o--|| App : "has one"
Project }o--|| OAuth-Brand : "has many or one (1)"
OAuth-Brand }o--|| OAuth-Client : "has many"

Project }o..|| Bucket : "has many"

Region }o--|| Bucket : "has many"
```
## Notes
(1): It is currently possible to create multiple brands via the web interface, but only one via the command line.

## Open questions:
* Is a Bucket _identified_ by Region or Project? (Currently modeled as Region).

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTIwNzI0MDc1OF19
-->