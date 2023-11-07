## Available Scripts

In the project directory, you can run to launch the FE app:

### `yarn start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.



## ✒️ Git naming convention

You should use commitizen to create new commit:
`git commit` and follow further instructions

### Code Flow Branches

These branches which we expect to be permanently available on the repository follow the flow of code changes starting from development until the production.

- **Develop** (`develop`): All new _features_ and bug _fixes_ should be brought to the `develop` branch. Resolving developer codes conflicts should be done as early as here.
- **Staging** (`staging`): CD deploys changes from `staging` branch into Staging environment. Merge `develop` branch into `staging` when bugs are fixed and complete story is finished. It shouldn't have uncompleted stories.
- **Production** (`prod`): CD deploys changes from `prod` branch into Production environment. Merge `staging` branch into `prod` when bugs are fixed and complete story is finished. It shouldn't have uncompleted stories. We can merge hot-fixes directly to the `prod` branch in case of urgent and crucial defects. In that case you should create a new hot-fix branch from the `prod` branch.

### Temporary Branches

As the name implies, these are disposable branches that can be created and deleted by need of the developer or deployer.
The name of the branch shouldn't contain more than 4 words.

- **Feature** (`feat`): Any code changes for a new module or use case should be done on a feature branch. This branch is created based on the current `develop` branch. When all changes are Done, a Pull Request should be merged to the `develop` branch.

  _Example_:

      - feat/GIENI-1234-add-step

- **Fix** (`fix`): If the code changes made from the feature branch were rejected after a release, sprint or demo, any necessary fixes after that should be done on the `fix` branch.

  _Example_:

      - fix/GIENI-1234-change-title-indentation

- **Refactor** (`refactor`): If any code should be refactored, but the functionality shouldn't be changed and app should work as before - any necessary changes should be done on the `refactor` branch.

  _Example_:

      - refactor/GIENI-1234-change-steps-rendering

- **Chore** (`chore`): Any code changes which is not reflected on the app. This branch is created based on the current development branch. When all changes are Done, a Pull Request should be merged to the development branch.

### Code review

Create a PR for every changes in the codebase.

Branch can be merged ONLY after approve from reviewer. PR's author is responsible to fix any conflicts and merge the created PR.

### Testing in different browsers

- Open https://www.browserstack.com/question/39568 and install browserstack locally
- Log in with your credentials
- Select the device/browser you'd like to test
- Type in website url http://localhost:3000

