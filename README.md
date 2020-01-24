# ra-data-firestore-client

A Firestore Client for the awesome [react-admin](https://github.com/marmelab/react-admin) framework. 

>This library is a modified version of [ra-data-firestore-client](https://github.com/rafalzawadzki/ra-data-firestore-client)

## Use in your project

```bash
yarn add https://github.com/bitlab-code/ra-data-firestore-client
```

### Set up admin account
Only the Firebase users with admin flag are able to authenticate on the Login screen.

To elevate users rights, add a boolean field `isAdmin = true` for a user in a Firestore collection `/users/`, like below:

```bash
"users": {
    "<USER_ID>": {
        "isAdmin": true
    }
}
```

The default collection & field name can be changed by adding `authConfig` object to `AuthProvider` constructor:

```javascript
const authConfig = {
  userProfilePath: '/users/',
  userAdminProp: 'isAdmin'
};
```

Pull requests are welcome