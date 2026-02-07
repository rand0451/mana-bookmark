# Contributing to MANA

First off, thank you for considering contributing to MANA! 🎉

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Development Setup](#development-setup)
- [Pull Request Process](#pull-request-process)
- [Coding Standards](#coding-standards)
- [Commit Guidelines](#commit-guidelines)

## 📜 Code of Conduct

This project adheres to a code of conduct. By participating, you are expected to uphold this code. Please report unacceptable behavior to the project maintainers.

## 🤝 How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check existing issues. When creating a bug report, include:

- **Clear title and description**
- **Steps to reproduce**
- **Expected vs actual behavior**
- **Screenshots** (if applicable)
- **Environment details:**
  - OS version
  - MANA version
  - Bookmark file format

### Suggesting Features

Feature requests are welcome! Please:

1. Check if the feature is already suggested
2. Provide clear use cases
3. Explain why it would be useful
4. Include mockups/examples if possible

### Code Contributions

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 🛠️ Development Setup

### Prerequisites

- Node.js 18+ and npm
- Git
- Code editor (VS Code recommended)

### Setup Steps

```bash
# Clone repository
git clone https://github.com/yourusername/mana.git
cd mana

# Install dependencies
npm install

# Run in development mode
npm run dev

# Build for production
npm run build:windows  # or build:mac, build:linux
```

### Project Structure

```
mana/
├── src/
│   ├── main/           # Electron main process
│   │   ├── main.js     # Entry point
│   │   ├── bookmarkParser.js
│   │   └── bookmarkWriter.js
│   └── renderer/       # Frontend
│       ├── app.js      # Main logic
│       ├── index.html  # UI structure
│       └── styles.css  # Styling
├── build/              # Build scripts
├── icon/               # Application icons
└── package.json        # Dependencies
```

## 🔄 Pull Request Process

### Before Submitting

1. **Test your changes:**
   ```bash
   npm run dev
   # Test all affected features
   ```

2. **Check code quality:**
   ```bash
   # Run linter (if configured)
   npm run lint
   
   # Check for errors
   node -c src/renderer/app.js
   node -c src/main/main.js
   ```

3. **Update documentation:**
   - Update README.md if needed
   - Add comments to complex code
   - Update CHANGELOG.md

### Submission Checklist

- [ ] Code follows project style guidelines
- [ ] Self-review completed
- [ ] Comments added for complex logic
- [ ] Documentation updated
- [ ] No new warnings/errors
- [ ] Tested on target platform(s)
- [ ] Commit messages follow guidelines

### PR Template

```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Breaking change
- [ ] Documentation update

## Testing
How was this tested?

## Screenshots
(if applicable)

## Checklist
- [ ] Code follows style guidelines
- [ ] Self-reviewed
- [ ] Documentation updated
- [ ] No new warnings
```

## 📝 Coding Standards

### JavaScript

```javascript
// Use descriptive variable names
const bookmarkCount = bookmarks.length; // Good
const bc = bookmarks.length;           // Bad

// Use const by default, let when needed
const apiKey = 'abc123';
let counter = 0;

// Arrow functions for callbacks
bookmarks.forEach(bm => console.log(bm.title));

// Async/await over promises
async function loadData() {
  const data = await fetchBookmarks();
  return data;
}

// Proper error handling
try {
  await riskyOperation();
} catch (error) {
  console.error('Operation failed:', error);
  showToast('Error occurred', 'error');
}
```

### CSS

```css
/* Use BEM naming convention */
.bookmark-card { }
.bookmark-card__title { }
.bookmark-card--selected { }

/* Mobile-first approach */
.element {
  /* Mobile styles */
}

@media (min-width: 768px) {
  .element {
    /* Tablet styles */
  }
}

/* Use CSS variables */
:root {
  --primary-color: #667eea;
}
```

### HTML

```html
<!-- Semantic HTML -->
<section class="bookmarks-container">
  <article class="bookmark-card">
    <h3 class="bookmark-title">Title</h3>
  </article>
</section>

<!-- Accessibility -->
<button aria-label="Delete bookmark" title="Delete">
  <svg>...</svg>
</button>
```

## 📝 Commit Guidelines

### Format

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types

- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting)
- `refactor`: Code refactoring
- `perf`: Performance improvements
- `test`: Adding tests
- `chore`: Maintenance tasks

### Examples

```bash
feat(ui): add pagination controls

- Add Previous/Next buttons
- Show current page info
- Implement page navigation logic

Closes #123
```

```bash
fix(cache): prevent unlimited favicon cache growth

Implement LRU algorithm with 500 item limit to prevent
memory issues with large bookmark collections.

Fixes #456
```

## 🧪 Testing Guidelines

### Manual Testing

Test the following before submitting:

1. **File Operations:**
   - Select folder with bookmarks
   - Toggle files on/off
   - Refresh bookmarks

2. **Bookmark Operations:**
   - Add new bookmark
   - Edit bookmark
   - Delete bookmark
   - Search functionality

3. **Performance:**
   - Load 1000+ bookmarks
   - Pagination navigation
   - Virtual scrolling

4. **Settings:**
   - Toggle all settings
   - Verify persistence
   - Test different configurations

### Platform-Specific Testing

- **Windows:** Test portable and installer versions
- **macOS:** Test DMG installation
- **Linux:** Test AppImage on different distros

## 📚 Resources

- [Electron Documentation](https://www.electronjs.org/docs)
- [electron-builder Guide](https://www.electron.build/)
- [JavaScript Best Practices](https://github.com/ryanmcdermott/clean-code-javascript)
- [Git Commit Guidelines](https://www.conventionalcommits.org/)

## 🎯 Priority Areas

Current focus areas for contributions:

1. **Performance** - Memory optimization, faster rendering
2. **Cross-browser Support** - More bookmark formats
3. **UI/UX** - Accessibility improvements
4. **Documentation** - More examples, tutorials
5. **Testing** - Automated tests

## 💡 Getting Help

- **Questions:** [GitHub Discussions](https://github.com/yourusername/mana/discussions)
- **Issues:** [GitHub Issues](https://github.com/yourusername/mana/issues)
- **Chat:** Join our Discord (link in README)

## 🏆 Recognition

Contributors will be:
- Listed in CONTRIBUTORS.md
- Mentioned in release notes
- Credited in the about section

Thank you for contributing! 🙌
