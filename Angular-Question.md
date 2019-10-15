# Angular Question
## 1. Question

Which files were created when i execute the command `ng generate component <name>` ? 

## 2. Question

In an Angular app, i have two components. A parent component and a child component. I want to send the data from the child to the parent when a button is pressed. How i can do it?

        @Component({
            selector: "parent",
            template: "<child></child>",
        })
        export class ParentComponent {

        }

        @Component({
            selector: "child",
            template: "<input type='button' (click)='sendData()'>",
        })
        export class ChildComponent {

            let data = "Some data which in want send to my parent component";

            sendData() {

            }
        }

## 3. Question

In an Angular app, I have a parent component and some child component that share the same base class. I need to run a function in the childs components. How i can do it?

        @Component({
            selector: "parent",
            template: " <child-1 />
                        <child-2 />
                        <child-3 />",
        })
        export class ParentComponent {

            refreshChilds() {
                
            }
        }

        export class BaseChildComponent {

            public data = "Data from base child component";

            refresh() {
                console.error("Method not implement");
            }
        }

        @Component({
            selector: "child-1",
            template: "<div> {{data}} </div>",
        })
        export class Child1Component extends BaseChildComponent {

            refresh() {
                this.data = "Data from child 1";
            }
        }

        @Component({
            selector: "child-2",
            template: "<div> {{data}} </div>",
        })
        export class Child2Component extends BaseChildComponent {

            refresh() {
                this.data = "Data from child 2";
            }
        }

        @Component({
            selector: "child-3",
            template: "<div> {{data}} </div>",
        })
        export class Child3Component extends BaseChildComponent {

            refresh() {
                this.data = "Data from child 3";
            }
        }

## 4. Question

What can you tell me about Lazyloading in Angular?

## 5. Question

I have two components in an Angular app. I want to send data among them. How i can do it ?

## 6. Question

I have an Api which gives me a token when i login to the App. For each Api's calls its necessary to add the token on each call. I don't want repeat code, so, how can i include the token in all Api calls?

## 7. Question

Could you explain me, what is Angular Ivy
