# test-peer-dependencies

This is a test repository to see how peer dependencies behave.

## Run

You will need two terminals:

### 1st Terminal

1. Install verdaccio: `npm i -g verdaccio`
2. Run verdaccio: `verdaccio`

Let this run in your background.

### 2nd Terminal

1. Create a user: `npm adduser --registry http://localhost:4873`
2. Login onto local registry: `yarn login --registry http://localhost:4873`
3. Publish both versions of the peer package: `yarn publish:peer`
4. Publish "extensions": `yarn publish:exts`
5. Install each example applications: `yarn install:apps`

    This is step emulates what an application maker would experience when
    consuming packages with peer dependencies.

6. Run both example applications: `yarn start`
