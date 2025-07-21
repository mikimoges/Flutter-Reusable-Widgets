# Flutter-Reusable-Widgets
# Modern Flutter Widgets Collection 🎨

A comprehensive collection of modern, reusable Flutter widgets designed to accelerate your app development with beautiful, consistent UI components.

## ✨ Features

- **Modern Design**: Contemporary UI with gradients, shadows, and smooth animations
- **Dark Mode Support**: Automatic adaptation to light and dark themes
- **Highly Customizable**: Extensive styling options for each widget
- **Easy Integration**: Drop-in widgets that work with any Flutter project
- **Well Documented**: Comprehensive usage examples and parameter descriptions
- **Production Ready**: Optimized performance and accessibility features

## 📱 Widgets Included

### 1. **ModernAppBar**
A gradient app bar with customizable title, subtitle, and action buttons.

**Features:**
- Gradient backgrounds
- Support for leading and action widgets
- Customizable colors and text styling
- Full-width design with proper safe area handling

### 2. **ModernBottomNav**
Animated bottom navigation with smooth transitions and modern styling.

**Features:**
- Smooth animations between tabs
- Customizable colors and icons
- Rounded corners design
- Active state indicators

### 3. **ModernCard**
Elevated cards with shadows, rounded corners, and tap interactions.

**Features:**
- Customizable padding and margins
- Tap gesture support
- Adaptive shadows for light/dark themes
- Rounded corner design

### 4. **ModernButton**
Versatile button component with multiple styles and loading states.

**Styles Available:**
- Primary (filled)
- Secondary (tinted)
- Outline
- Text

**Features:**
- Icon support
- Loading states
- Customizable colors and sizes
- Multiple style variants

### 5. **ModernTextField**
Styled input fields with validation support and modern design.

**Features:**
- Label and hint text support
- Prefix and suffix icons
- Validation support
- Focus states with color transitions
- Multi-line support

### 6. **ModernLoading**
Custom loading indicator with optional message display.

**Features:**
- Customizable size and color
- Optional loading message
- Centered layout
- Theme-aware styling

### 7. **ModernChip**
Selectable chips with icons and delete functionality.

**Features:**
- Selected/unselected states
- Icon support
- Delete functionality
- Smooth animations
- Customizable colors

### 8. **ModernFAB**
Customizable floating action button with extended variant support.

**Features:**
- Regular and extended variants
- Icon and label support
- Customizable colors
- Rounded corners design

## 🚀 Installation

1. **Download the widgets file:**
   ```bash
   # Clone this repository or download the modern_widgets.dart file
   ```

2. **Add to your Flutter project:**
   ```
   lib/
   ├── widgets/
   │   └── modern_widgets.dart
   └── main.dart
   ```

3. **Import in your Dart files:**
   ```dart
   import 'widgets/modern_widgets.dart';
   ```

## 📖 Usage Examples

### ModernAppBar

```dart
Scaffold(
  appBar: ModernAppBar(
    title: "My App",
    subtitle: "Welcome back!",
    actions: [
      IconButton(
        icon: Icon(Icons.notifications),
        onPressed: () => print('Notifications'),
      ),
      IconButton(
        icon: Icon(Icons.settings),
        onPressed: () => print('Settings'),
      ),
    ],
  ),
  body: YourBodyContent(),
)
```

### ModernBottomNav

```dart
int _selectedIndex = 0;

Scaffold(
  bottomNavigationBar: ModernBottomNav(
    currentIndex: _selectedIndex,
    onTap: (index) => setState(() => _selectedIndex = index),
    items: [
      ModernBottomNavItem(icon: Icons.home, label: 'Home'),
      ModernBottomNavItem(icon: Icons.search, label: 'Search'),
      ModernBottomNavItem(icon: Icons.favorite, label: 'Favorites'),
      ModernBottomNavItem(icon: Icons.person, label: 'Profile'),
    ],
  ),
)
```

### ModernButton

```dart
// Primary button with icon
ModernButton(
  text: 'Save Changes',
  icon: Icons.save,
  style: ModernButtonStyle.primary,
  onPressed: () => print('Button pressed'),
)

// Loading button
ModernButton(
  text: 'Loading...',
  isLoading: true,
  style: ModernButtonStyle.primary,
  onPressed: null,
)
```

### ModernTextField

```dart
ModernTextField(
  label: 'Email Address',
  hint: 'Enter your email',
  prefixIcon: Icons.email,
  keyboardType: TextInputType.emailAddress,
  validator: (value) {
    if (value?.isEmpty ?? true) return 'Email is required';
    if (!value!.contains('@')) return 'Invalid email format';
    return null;
  },
  onChanged: (value) => print('Email: $value'),
)
```

### ModernCard

```dart
ModernCard(
  child: Column(
    crossAxisAlignment: CrossAxisAlignment.start,
    children: [
      Text(
        'Card Title',
        style: TextStyle(fontSize: 18, fontWeight: FontWeight.bold),
      ),
      SizedBox(height: 8),
      Text('Your card content goes here...'),
    ],
  ),
  onTap: () => print('Card tapped'),
)
```

### ModernChip

```dart
Wrap(
  spacing: 8,
  children: [
    ModernChip(
      label: 'Flutter',
      selected: true,
      onTap: () => print('Flutter selected'),
    ),
    ModernChip(
      label: 'Dart',
      icon: Icons.code,
      onTap: () => print('Dart selected'),
    ),
    ModernChip(
      label: 'Remove me',
      onDelete: () => print('Chip deleted'),
    ),
  ],
)
```

### ModernFAB

```dart
// Extended FAB
ModernFAB(
  icon: Icons.add,
  extended: true,
  label: 'Add Item',
  onPressed: () => print('FAB pressed'),
)

// Regular FAB
ModernFAB(
  icon: Icons.edit,
  onPressed: () => print('Edit pressed'),
)
```

## 🎨 Customization

All widgets support extensive customization through their parameters:

### Colors
```dart
ModernButton(
  text: 'Custom Color',
  color: Colors.purple,
  style: ModernButtonStyle.primary,
  onPressed: () {},
)
```

### Styling
```dart
ModernCard(
  color: Colors.blue.shade50,
  elevation: 8,
  borderRadius: BorderRadius.circular(24),
  child: YourContent(),
)
```

### Theme Integration
The widgets automatically adapt to your app's theme:

```dart
MaterialApp(
  theme: ThemeData.light().copyWith(
    primaryColor: Colors.blue,
  ),
  darkTheme: ThemeData.dark().copyWith(
    primaryColor: Colors.blueAccent,
  ),
  home: YourHomePage(),
)
```

## 📁 Project Structure

```
lib/
├── widgets/
│   └── modern_widgets.dart    # All widget definitions
├── screens/
│   └── demo_screen.dart       # Usage examples
└── main.dart
```

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch**: `git checkout -b feature/new-widget`
3. **Make your changes** and add tests if applicable
4. **Follow the existing code style** and documentation format
5. **Submit a pull request** with a clear description

### Adding New Widgets

When adding new widgets, please:
- Follow the existing naming convention (`ModernWidgetName`)
- Include comprehensive documentation and usage examples
- Support both light and dark themes
- Add the widget to the demo screen
- Update this README

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🌟 Show Your Support

If you find this widget collection helpful, please:
- ⭐ Star this repository
- 🐛 Report any bugs or issues
- 💡 Suggest new widgets or improvements
- 📢 Share with other Flutter developers

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/yourusername/modern-flutter-widgets/issues)
- **Discussions**: [GitHub Discussions](https://github.com/yourusername/modern-flutter-widgets/discussions)
- **Email**: your.email@example.com

## 🚧 Roadmap

Planned widgets and improvements:

- [ ] ModernSlider
- [ ] ModernSwitch
- [ ] ModernDialog
- [ ] ModernSnackBar
- [ ] ModernProgressBar
- [ ] ModernDatePicker
- [ ] ModernDropdown
- [ ] Accessibility improvements
- [ ] Animation enhancements
- [ ] More customization options

## 📚 Additional Resources

- [Flutter Documentation](https://flutter.dev/docs)
- [Material Design Guidelines](https://material.io/design)
- [Flutter Widget Catalog](https://flutter.dev/docs/development/ui/widgets)

---

**Happy Coding! 🎉**

*Built with ❤️ for the Flutter community*
