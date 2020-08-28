# CI&CD with TravisCi and Heroku.

This project was created with [Create React App](https://github.com/facebook/create-react-app) for CI testing purposes.

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.<br />
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

## Settings information
Connected Travis CI to run tests and if passed -> deploy.

For automated project deployement I used Heroku cloud application platform.

# To setup TravisCi I added.travis.yml file with such config:
<pre>
  sudo: false
  language: node_js
    node_js:
      - 10
  branches:
    only:
      - master
  deploy:
    provider: heroku
    api_key:
      secure: [HERE YOUR API KEY FROM HEROKU ACCOUNT]
    app: [APP NAME]
</pre>
