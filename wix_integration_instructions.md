# Wix Integration Instructions for oliversroofingandcontracting.com

This document provides specific step-by-step instructions for integrating the AI-Powered Roofing Platform widgets with your Wix website at oliversroofingandcontracting.com.

## Integration Overview

Based on the analysis of your website structure, we recommend integrating the three widgets in the following locations:

1. **AI Roof Damage Assessment Widget** - Add to the "AI-powered Contractor Tools" section on your Solutions page
2. **Roofing Cost Calculator Widget** - Add to the "Instant Roof Estimates" section on your Solutions page
3. **Project Tracker Widget** - Add to the "Real-time Project Tracking" section on your Solutions page

## Step-by-Step Integration Instructions

### Step 1: Access Your Wix Editor

1. Log in to your Wix account
2. Navigate to your site dashboard
3. Click "Edit Site" to open the Wix Editor

### Step 2: Enable Velo by Wix

1. In the top menu of the Editor, click "Dev Mode" or "Velo by Wix"
2. If prompted, click "Turn on Dev Mode" to enable Velo development
3. This will give you access to the advanced development features needed for the integration

### Step 3: Add HTML Components to Your Solutions Page

1. Navigate to your Solutions page in the Editor
2. For each widget section:
   - Click the "+" button to add a new element
   - Select "Embed" > "HTML iframe"
   - Position and size the component within the appropriate section
   - Adjust the size to match your design (recommended minimum: 600px width, 500px height)

### Step 4: Configure the HTML Components

For each HTML component you added:

1. Select the component
2. In the Properties panel, note the component ID (e.g., "html1")
3. Click "Settings" in the Properties panel
4. Leave the HTML field empty (we'll populate it with code)

### Step 5: Add Velo Code to Your Page

1. With the Solutions page open in the Editor, click "Velo Dev Mode" in the top menu
2. Click "Page Code" to open the code editor for the current page
3. Copy and paste the following code at the end of the file:

```javascript
import wixWindow from 'wix-window';

// Initialize widgets when page loads
$w.onReady(function () {
    // Set up AI Roof Damage Assessment Widget
    setupRoofDamageWidget();
    
    // Set up Roofing Cost Calculator Widget
    setupCostCalculatorWidget();
    
    // Set up Project Tracker Widget
    setupProjectTrackerWidget();
});

// AI Roof Damage Assessment Widget Setup
function setupRoofDamageWidget() {
    // Get the HTML component (update the ID to match your component)
    const damageAssessmentWidget = $w('#html1');
    
    // Paste the entire content from roof-damage-assessment/velo_integration.js here
    // The code is too long to include in this document, but it's available in the integration package
}

// Roofing Cost Calculator Widget Setup
function setupCostCalculatorWidget() {
    // Get the HTML component (update the ID to match your component)
    const costCalculatorWidget = $w('#html2');
    
    // Paste the entire content from cost-calculator/velo_integration.js here
    // The code is too long to include in this document, but it's available in the integration package
}

// Project Tracker Widget Setup
function setupProjectTrackerWidget() {
    // Get the HTML component (update the ID to match your component)
    const projectTrackerWidget = $w('#html3');
    
    // Paste the entire content from project-tracker/velo_integration.js here
    // The code is too long to include in this document, but it's available in the integration package
}
```

4. Replace the placeholder functions with the actual code from each widget's velo_integration.js file in the integration package
5. Update the component IDs (#html1, #html2, #html3) to match the actual IDs of your HTML components

### Step 6: Customize Widget Appearance

Each widget can be customized to match your website's design:

1. In each widget's initialization code, find the `init` message with the `theme` parameter
2. Change the theme from 'light' to 'dark' if your website uses a dark color scheme
3. You can also modify the CSS variables in each widget's HTML code to match your brand colors

### Step 7: Test the Integration

1. Click "Preview" in the Wix Editor to test your integration
2. Test each widget's functionality:
   - Upload a test image to the AI Roof Damage Assessment widget
   - Calculate a sample estimate with the Roofing Cost Calculator
   - Log in to the Project Tracker with test credentials
3. Verify that all widgets display correctly and function as expected

### Step 8: Publish Your Updated Website

1. Once you're satisfied with the integration, click "Publish" in the Wix Editor
2. Review the changes and confirm publication
3. Your AI-Powered Roofing Platform is now live on your website!

## Integration Tips

- **Component Sizing**: Adjust the size of each HTML component to ensure the widgets display properly on all devices
- **Mobile Responsiveness**: Test the widgets on mobile devices to ensure they're fully responsive
- **Loading Performance**: The widgets are designed to load efficiently, but monitor your page loading speed after integration
- **User Instructions**: Consider adding brief instructions near each widget to help users understand how to use them

## Troubleshooting

If you encounter any issues during integration:

1. **Widget Not Displaying**: Check that the HTML component IDs in your code match the actual component IDs in the Editor
2. **JavaScript Errors**: Open your browser's developer console (F12) to check for any JavaScript errors
3. **Styling Issues**: Adjust the CSS variables in the widget code to better match your website's design
4. **Functionality Problems**: Verify that all the code from the integration package has been properly copied into your Velo code

## Next Steps

After successful integration, consider:

1. **User Training**: Familiarize your team with the new tools and how to use them
2. **Client Communication**: Inform your clients about the new AI-powered features available on your website
3. **Feedback Collection**: Gather feedback from users to identify any improvements needed
4. **Regular Updates**: Plan for periodic updates to the widgets as new features become available

For additional assistance with the integration, please refer to the comprehensive integration guide included in the integration package.
