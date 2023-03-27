# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

## Building and running the react app image

```bash
./build.sh
docker run -p 3000:3000 -d dockerized-react
```

Or run the published image. Might need an access token to pull this, ask me for one.

```bash
docker run -d -p 3000:3000 --name react-app docker.io/joelasaur1/ci-services-reproducer:local
```

## Running Cypress container

```bash
docker run -it -v $PWD:/e2e -w /e2e --network="host" cypress/included:12.3.0   
```

## Running Cypress locally

```bash
yarn cy:open
```

