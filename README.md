# Email Reply Generator Chrome Extension

A Chrome extension that enhances Gmail with AI-powered email reply generation using Google's Gemini API.

## Overview

This project integrates with Gmail to provide one-click AI-generated email responses. When replying to an email in Gmail, the extension adds an "AI Reply" button that analyzes the email content and generates a contextually appropriate response using the Gemini API.

## Project Structure

The project consists of three main components:

### Backend (email-writer-sb)
- Spring Boot application that handles communication with the Gemini API
- RESTful endpoints for processing email content and generating replies
- Key components:
  - `EmailWriterController`: REST controller handling requests
  - `EmailWriterService`: Business logic for email processing
  - `EmailRequest`: Data model for incoming requests

### Frontend (email-writer-react)
- React application for development and testing
- Contains:
  - `App.jsx`: Main application component
  - `App.css`: Styling
  - `index.css`: Global styles
  - `main.jsx`: Entry point

### Chrome Extension (email-writer-ext)
- Contains extension-specific files:
  - `manifest.json`: Extension configuration
  - `content.js`: DOM manipulation and backend communication
  - `content.css`: Styling for injected UI elements

## Features

- Seamlessly integrates with Gmail's interface
- Activates only on mail.google.com domains
- Monitors only the active tab for privacy
- Adds an "AI Reply" button to Gmail's compose toolbox
- Extracts email content for context-aware replies
- Generates human-like responses using Gemini AI
- Inserts generated content directly into the compose box

## Installation

### Prerequisites
- Java 11+ for Spring Boot
- Node.js and npm for React
- Google Chrome browser
- Gemini API key

### Backend Setup
1. Navigate to the `email-writer-sb` directory
2. Add your Gemini API key to `application.properties`
3. Run the Spring Boot application:
   ```
   ./mvnw spring-boot:run
   ```

### Chrome Extension Installation
1. Open Chrome and navigate to `chrome://extensions/`
2. Enable "Developer mode" (toggle in the top-right)
3. Click "Load unpacked" and select the `email-writer-ext` directory
4. The extension should now be installed and active when visiting Gmail

## Usage

1. Navigate to Gmail in Chrome
2. Open an email you want to reply to
3. Click the "Reply" button as normal
4. Note the new "AI Reply" button added to the compose toolbox
5. Click "AI Reply" to generate a response based on the email content
6. Edit the generated reply if needed, then send

## Development

### Backend Development
```
cd email-writer-sb
./mvnw spring-boot:run
```

### React Development
```
cd email-writer-react
npm install
npm run dev
```

### Building Chrome Extension
```
cd email-writer-ext
# If you need to build the extension before loading it
npm run build
```

## Technologies Used

- **Backend**: Spring Boot, Java
- **Frontend**: React, Vite
- **Extension**: Chrome Extension API
- **AI**: Google Gemini API

## Contributing

Contributions are welcome! Here's how you can contribute to this project:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Commit your changes (`git commit -m 'Add some amazing feature'`)
5. Push to the branch (`git push origin feature/amazing-feature`)
6. Open a Pull Request

Please ensure your code follows the existing style and includes appropriate tests when applicable.

### Areas for Contribution
- Improved email content extraction
- Additional customization options for generated replies
- UI/UX enhancements
- Support for additional email providers
- Performance optimizations
- Documentation improvements

## License

This project is licensed under the MIT License - see below for details:

```
MIT License

Copyright (c) 2025 [Soumya Kushwaha]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
