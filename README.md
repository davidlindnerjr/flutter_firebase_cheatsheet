# flutter_firebase_cheatsheet

A quick setup guide in order to add Firebase backend such as Aunthentication, setup, and CRUD functionality into Flutter Projects.

## Connect Flutter Project to Firebase
- Install the CLI (only for initial setup)

`npm install -g firebase-tool`

`dart pub global activate flutterfire_cli`

- Add environment varibale (only for initial setup)

`export PATH="$PATH":"$HOME/.pub-cache/bin"`

- Check version number

`firebase --version`

- Login to Firebase

`firebase login`

- Configure Project

`flutterfire configure` -> choose existing project -> hit enter when prompted for project id -> Select platforms for project

- Add Initalization in main function

- Install Dependencies
`flutter pub add firebase_core`

```
void main() async {
  WidgetsFlutterBinding.ensureInitialized();
  await Firebase.initializeApp(
    options: DefaultFirebaseOptions.currentPlatform,
  );
  runApp(const MyApp());
 }

```


