# AlertController

💬 A tiny extension for UIAlertController that makes working with it very simple. Only 150 lines of code.

### Alert

```swift
let alert = UIAlertController.alert()
alert.setTitle("✅ Success", color: .darkGreen)
alert.setMessage("Your message has been sent")
alert.addAction(
    title: "Send more",
    systemIcon: "envelope.fill",
    color: .blue,
    leftAligment: true
) {}
alert.addAction(
    title: "Delete message",
    systemIcon: "trash.fill",
    color: .red,
    leftAligment: true
) {}
alert.addOkAction()
present(alert, animated: true)
```
### Sheet

```swift
let sheet = UIAlertController.sheet("👨🏻 Mezhevikin Alexey")
sheet.addAction(
    title: "Edit profile",
    systemIcon: "person.fill",
    color: .darkGreen,
    leftAligment: true
) {}
sheet.addAction(
    title: "Delete account",
    systemIcon: "trash.fill",
    color: .red,
    leftAligment: true
) {}
sheet.addAction(
    title: "Log out",
    systemIcon: "square.and.arrow.down.fill",
    leftAligment: true
) {}
sheet.addCancelAction()
present(sheet, sourceView: cell)
```

### Choice

```swift
let sheet = UIAlertController.sheet("Choose your favorite animal")
let animals = ["🐈 Cat", "🐕 Dog", "🐎 Hourse", "🐫 Camel"]
for (i, animal) in animals.enumerated() {
    sheet.addAction(
        title: animal,
        checked: favoriteAnimal == i,
        leftAligment: true
    ) {
        self.favoriteAnimal = i
    }
 }
sheet.addCancelAction()
present(sheet, sourceView: cell)
```

### Swift Package Manager

```
https://github.com/mezhevikin/AlertController
```