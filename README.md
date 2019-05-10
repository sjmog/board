# Board

Board is an open-source real-time whiteboard to which you can pin anything you like.

If you can do it with JavaScript, you can put it on a Board.

## Why

There are a few real-time whiteboard apps out there that offer different components. But if you want a component that doesn't exist, you're out of luck until the developer makes it.

Board components are React components that execute arbitrary JavaScript. They can make API calls, scrape the web – anything your browser can do, a Board component can do.

You can create a new Board component with the built-in editor, mark properties as customisable, and then share them across Boards.

Here's an example of a simple component: a Post-It. Make a new component, and add the following in the editor:

```javascript
class PostIt extends Board::Component {
  this.state = { text: "Edit me!" }

  render {
    return(
      <div contenteditable>{{this.state.text}}</div>
    );
  }
}
```

Now you can pin this Post-It to a Board. Any state variables are editable either via the GUI or via the component's two-way data binding.

Here's a more complex component, which fetches some data from an API using a given (editable) API key and displays it:

```javascript
class PriceComponent extends Board::Component {
  this.state = { key: "some-api-key" }

  this.price = () => {
    const client = new ApiClient(this.key);
    return client.fetchPrice();
  }

  render {
    return( 
      <div>{{ this.price() }}</div>
    );
  }
}
```

## Ethos

Board is open-source. While you can create private components, you're encouraged to share components you create with the community!

## License

MIT. Hack away!

# Tech Stuff

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br>
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br>
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.<br>
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br>
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (Webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: https://facebook.github.io/create-react-app/docs/code-splitting

### Analyzing the Bundle Size

This section has moved here: https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size

### Making a Progressive Web App

This section has moved here: https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app

### Advanced Configuration

This section has moved here: https://facebook.github.io/create-react-app/docs/advanced-configuration

### Deployment

This section has moved here: https://facebook.github.io/create-react-app/docs/deployment

### `npm run build` fails to minify

This section has moved here: https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify
