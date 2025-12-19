## Applying a Custom Theme with Tutor

Follow the steps below to apply a custom Open edX theme using Tutor.

### 1. Navigate to the themes directory
```
cd "$(tutor config printroot)"/env/build/openedx/themes/
```

### 2. Clone the custom theme repository
```
git clone https://github.com/rajpipaliya048/openedx-theme.git
```

### 3. Set the theme in Tutor (development mode)
```
tutor dev do settheme openedx-theme
```

### 4. Rebuild the Open edX development image
```
tutor images build openedx-dev
```

###5. Restart Tutor services
```
tutor dev restart
```

After completing these steps, the theme changes will be visible on the platform.

## Notes on MFE Styling

The changes above are limited to Sass/CSS overrides for the LMS and CMS and do not affect Micro Frontends (MFEs).

To override or customize styles in MFEs, you must customize Paragon (the Open edX design system) and apply those overrides as part of the relevant MFE build process.
