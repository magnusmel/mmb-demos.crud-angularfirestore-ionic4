# mmb-demos.crud-angularfirestore-ionic4</h1>
**Tutorial** [Create a CRUD App with Ionic 4, Firestore and AngularFire 5.2+](http://meumobi.github.io/ionic/2019/05/29/crud-ionic4-angulafire5-app.html)

## Getting started

### Prerequisites
[Download the installer](https://nodejs.org/) for Node.js 6 or greater.
Install both [Ionic].

```terminal
$ npm install ionic typescript @angular/cli -g
...

$ npm ls -g cordova ionic npm typescript @angular/cli --depth 0
/Users/victor.dias/.nvm/versions/node/v12.6.0/lib
├── @angular/cli@8.3.3 
├── cordova@9.0.0 
├── ionic@5.2.7 
├── npm@6.9.0 
└── typescript@3.6.2 
```

### Usage
1. Run

- `git clone https://github.com/meumobi/mmb-demos.crud-angularfirestore-ionic4.git crud-angularfirestore-ionic4`.
- `cd crud-angularfirestore-ionic4`
- `npm install`

2.  Create a project at https://firebase.google.com/ and grab your web config:

![](https://firebasestorage.googleapis.com/v0/b/firestarter-96e46.appspot.com/o/project-config.PNG?alt=media&token=5eabb205-7ba2-4fc3-905f-e9547055e754)

3.  Add the config to your Angular environment

#### src/environments/

Update the `environment.prod.ts` and `environment.ts` files. 

```typescript
export const environment = {
  production: false,
  firebase: {
    apiKey: 'APIKEY',
    authDomain: 'DEV-APP.firebaseapp.com',
    databaseURL: 'https://DEV-APP.firebaseio.com',
    projectId: 'DEV-APP',
    storageBucket: 'DEV-APP.appspot.com',
    messagingSenderId: '...',
    appId: '...',
  }
};
```


4. Run `ionic serve`
5. Profit. :tada:

## Todo
### Development workflow tools
- [ ] Unit and e2e tests
- [ ] Continuous integration with Travis CI

  - [angular.io - Configure project to Travis CI](https://angular.io/guide/testing#configure-project-for-travis-ci)
- [ ] Automated dependency updates with Greenkeeper

  - https://greenkeeper.io/docs.html#installation

### UI/UX

- [ ] Infinite scroll / Virtual Scroll
- [x] Rendering placeholder: skeleton loading
  - https://ionicframework.com/docs/api/skeleton-text
  - https://ionicthemes.com/tutorials/about/improved-ux-for-ionic-apps-with-skeleton-loading-screens

### Firebase hosting & deploy
- [] Auto deploy to Firebase hosting
  - [Use @angular/fire to automatically deploy an Angular application to Firebase hosting](https://github.com/angular/angularfire2/blob/master/docs/deploy/getting-started.md)

### Build PWA and native App
- [] PWA
  - https://ionicframework.com/docs/publishing/progressive-web-app
  - https://alligator.io/ionic/pwas/

### 3rd party integration
- [ ] Google Analytics
- [ ] Slack