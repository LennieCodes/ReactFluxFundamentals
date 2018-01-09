# React notes

## Controller Views

A controller view is a top level component that sets the props object for child components. There is a one way data flow from the top level component down to the child components. 

Controller views also interact with flux stores as well. (We'll talk about what that is later).

## Params and Query Strings in React-Router
Example Route:
```jsx
<route path="/course/:courseId" handler={Course} />
```
Example URL:
```javascript
    "/course/clean-code?module=3"
```

Resulting React Component:
```javascript
    var Course = React.createClass({
        render: function() {
            this.props.params.courseId; // "clean-code"
            this.props.query.module; // "3"
            this.props.path; // "/clean/clean-code/?module=3"
        }
    });
```
You can see that react-router parses the path and sets courseId param on props, and 
it also sets query params under props. 
And it also gives us access to the full path. 





