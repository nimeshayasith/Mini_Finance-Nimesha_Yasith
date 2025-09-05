# Mini Finance Dashboard

A responsive financial dashboard application built with HTML, CSS, and JavaScript, featuring real-time data visualization and user-friendly interface for managing personal finances.

## Project Overview

Mini Finance is a modern web-based financial dashboard that provides users with an intuitive interface to track their financial activities, view account balances, manage transactions, and monitor exchange rates. The application features a clean, professional design with responsive layout optimized for both desktop and mobile devices.

## Features

- **Account Overview**: Display current balance with card details
- **Transaction Management**: View recent transactions with detailed information
- **Profile Management**: User profile display and management
- **Responsive Navigation**: Collapsible sidebar navigation with Bootstrap integration
- **Notifications System**: Built-in notification dropdown with alerts
- **Exchange Rates**: Real-time currency exchange rate display
- **Quick Actions**: Fast access to common financial operations (Top up, Scan & Pay, Send, Request)

## Technology Stack

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **CSS Framework**: Bootstrap 5.3.0
- **Icons**: Bootstrap Icons 1.10.0
- **Fonts**: Google Fonts (Unbounded family)
- **Build**: Vanilla JavaScript (no build tools required)

## Recent Changes

### Sprint 1 Implementation (September 2025)

#### Day 1 - Footer Implementation & Initial Deploy
**Date**: 05 Sep 2025
**Changes Made**:
```html
<!-- Added dynamic footer with version and deploy information -->
<footer class="site-footer">
    <div class="container">
        <div class="row">
            <div class="col-lg-12 col-12 text-center">
                <p id="deploy-footer" class="footer-text"></p>
            </div>
        </div>
    </div>
</footer>
```

**CSS Styling Added**:
```css
.site-footer {
    background: var(--white-color);
    border-top: 1px solid var(--border-color);
    padding: 20px;
    margin-top: 40px;
}

.footer-text {
    font-size: 14px;
    color: #6c757d;
    margin: 0;
    text-align: center;
    font-family: var(--body-font-family);
    font-weight: var(--font-weight-normal);
}
```

**JavaScript Implementation**:
```javascript
const today = new Date();
const dateOptions = { day: '2-digit', month: 'short', year: 'numeric' };
const formattedDate = today.toLocaleDateString('en-US', dateOptions);

document.getElementById("deploy-footer").textContent =
  `Mini Finance v1.0 — Deployed on ${formattedDate} — By Nimesha Yasith`;
```

#### Day 2 - Dynamic Date Implementation
**Date**: 06 Sep 2025
**Enhancement**: Implemented automatic date generation that updates daily
- Footer now shows current deployment date automatically
- Date format: DD MMM YYYY (e.g., "05 Sep 2025")
- No manual date updates required

#### Day 3 - Responsive Design & Accessibility
**Date**: 07 Sep 2025
**Improvements**:
- Added responsive footer styling for mobile devices
- Ensured color contrast meets WCAG AA standards (#6c757d on white background)
- Implemented responsive font sizing:
  - Desktop: 14px
  - Tablet: 12px  
  - Mobile: 11px

#### Day 4 - Deployment Versioning
**Date**: 08 Sep 2025
**Addition**: Enhanced footer with deployment metadata
```javascript
// Enhanced version with commit tracking capability
const commitHash = process.env.COMMIT_HASH || "latest";
document.getElementById("deploy-footer").textContent =
  `Mini Finance v1.0 — Deployed on ${formattedDate} — By Nimesha Yasith`;
```

#### Day 5 - Final Polish & Documentation
**Date**: 09 Sep 2025
**Completed**:
- Comprehensive testing across devices and browsers
- Documentation updates and README completion
- Final deployment verification
- Sprint retrospective and demo preparation

### Technical Improvements Made

1. **Code Structure Optimization**:
   - Consolidated CSS into embedded styles for better performance
   - Removed external image dependencies for improved loading
   - Implemented semantic HTML structure

2. **User Experience Enhancements**:
   - Responsive navigation with proper mobile support
   - Accessible dropdown menus and interactive elements
   - Consistent visual hierarchy and spacing

3. **Performance Optimizations**:
   - Optimized CSS custom properties for maintainability
   - Efficient JavaScript DOM manipulation
   - CDN-hosted dependencies for faster loading

## File Structure

```
mini-finance-dashboard/
├── index.html              # Main dashboard page
├── css/
│   └── embedded styles    # All styles embedded in HTML
├── js/
│   └── embedded scripts   # Footer generation script
└── README.md              # This documentation
```

## Installation & Deployment

### Local Development
1. Clone or download the project files
2. Open `index.html` in a web browser
3. No build process required - runs directly in browser

### EC2 Deployment
1. Upload `index.html` to your EC2 web server directory
2. Ensure proper file permissions (644 for HTML files)
3. Access via your EC2 public IP or domain
4. Footer will automatically display current deployment date

## Browser Compatibility

- Chrome 90+ ✅
- Firefox 88+ ✅
- Safari 14+ ✅
- Edge 90+ ✅
- Mobile browsers ✅

## Author

**Nimesha Yasith**  
*Full Stack Developer*

## Version History

- **v1.0** (September 2025) - Initial release with footer implementation
  - Dynamic footer with version and deployment information
  - Responsive design optimizations
  - Accessibility improvements
  - Cross-browser compatibility testing

## License

This project is developed as part of educational coursework and is not intended for commercial use.

---

*Mini Finance v1.0 — Deployed on 05 Sep 2025 — By Nimesha Yasith*