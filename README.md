## Snackbar + Alert Dialog
```dart
MySnackBar(message, context) {
    return ScaffoldMessenger.of(context)
        .showSnackBar(SnackBar(content: Text(message)));
  }

  MyAlertDialog(context) {
    return showDialog(
        context: context,
        builder: (BuildContext context) {
          return Expanded(
              child: AlertDialog(
            title: Text('Alert Title'),
            content: Text('Do you want to delete?'),
            actions: [
              TextButton(onPressed: () {}, child: Text('Yes')),
              TextButton(
                  onPressed: () {
                    Navigator.pop(context);
                  },
                  child: Text('No')),
            ],
          ));
        });
  }
  ```
  ---
