# Terms and Conditions Insight Analyzer

A modern web application that analyzes Terms and Conditions documents using AI to identify critical clauses, hidden terms, and potential concerns that users should be aware of.

## Features

- **File Upload Support**: Upload PDF and text files (.pdf, .txt) up to 10MB
- **Text Input**: Paste Terms and Conditions text directly for analysis
- **AI-Powered Analysis**: Uses Google's Gemini AI to identify critical clauses
- **Key Insights**: Highlights important areas like data usage, arbitration clauses, auto-renewal terms, and more
- **Responsive Design**: Modern, mobile-friendly interface with dark/light theme toggle
- **Real-time Processing**: Live file processing with progress indicators

## Technologies Used

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Styling**: Tailwind CSS with custom animations
- **AI Service**: Google Gemini 2.0 Flash API
- **PDF Processing**: PDF.js for text extraction
- **Markdown Rendering**: Marked.js for formatted output

## GitHub Pages Deployment

This application is configured for deployment to GitHub Pages using GitHub Actions.

### Prerequisites

1. **GitHub Account**: You need a GitHub account
2. **GitHub Repository**: Your code should be in a GitHub repository
3. **GitHub Pages Enabled**: Pages feature should be enabled in your repository

### Deployment Steps

#### Option 1: GitHub Pages (Recommended)

1. **Enable GitHub Pages**:
   - Go to your GitHub repository
   - Click on "Settings" tab
   - Scroll down to "Pages" in the left sidebar
   - Under "Source", select "GitHub Actions"
   - This will enable GitHub Pages for your repository

2. **Push Your Code**:
   - Make sure all your files are committed and pushed to the main branch
   - The GitHub Actions workflow will automatically deploy your app

3. **Access Your App**:
   - Your app will be available at: `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME`
   - The first deployment may take a few minutes

#### Option 2: Manual Setup

1. **Create the workflow directory**:
   ```bash
   mkdir -p .github/workflows
   ```

2. **Add the deployment workflow**:
   - Copy the `deploy.yml` file to `.github/workflows/` directory
   - Commit and push the changes

3. **Enable Pages**:
   - Go to repository Settings → Pages
   - Select "GitHub Actions" as source

### Configuration

The application uses the following configuration:

- **API_KEY**: Your Google Gemini API key is currently hardcoded in the JavaScript code (line ~700 in index.html)
- **For production use**: Consider moving the API key to environment variables or using a backend service

### Custom Domain (Optional)

1. In your GitHub repository, go to Settings → Pages
2. Under "Custom domain", enter your domain
3. Update your DNS provider with the provided CNAME record
4. Wait for DNS propagation (can take up to 24 hours)

### Monitoring and Analytics

- **GitHub Actions**: Monitor deployment status and logs in the Actions tab
- **GitHub Pages**: View page analytics and performance in repository Insights
- **Browser Developer Tools**: Monitor console errors and network requests

## Local Development

1. **Clone the repository**:
   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
   cd YOUR_REPO
   ```

2. **Open in browser**:
   - Simply open `index.html` in your web browser
   - Or use a local server:
     ```bash
     # Using Python
     python -m http.server 8000
     
     # Using Node.js
     npx serve .
     
     # Using PHP
     php -S localhost:8000
     ```

3. **API Key Setup**:
   - Get a Google Gemini API key from [Google AI Studio](https://makersuite.google.com/app/apikey)
   - Replace the API key in the JavaScript code (line ~700 in index.html)

## Security Considerations

- **API Key**: The current implementation has the API key hardcoded. For production, consider:
  - Using environment variables
  - Implementing a backend service to proxy API calls
  - Using GitHub Actions secrets for sensitive data

- **File Upload**: Files are processed client-side and not stored on servers

- **Rate Limiting**: Consider implementing rate limiting for the AI analysis feature

## Troubleshooting

### Common Issues

1. **Deployment Fails**:
   - Check GitHub Actions logs in the Actions tab
   - Verify GitHub Pages is enabled in repository settings
   - Ensure the workflow file is in the correct location

2. **App Not Loading**:
   - Check browser console for errors
   - Verify all CDN resources are accessible
   - Check GitHub Pages status in repository settings

3. **API Errors**:
   - Verify Google Gemini API key is valid
   - Check API quota and limits
   - Ensure the API is enabled in your Google Cloud project

### Getting Help

- Check [GitHub Pages documentation](https://docs.github.com/en/pages)
- Review GitHub Actions logs for deployment issues
- Check repository Pages settings for configuration

## License

This project is open source. Please ensure you comply with the terms of service for Google Gemini API and any other third-party services used.

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## Support

For deployment issues:
- Check GitHub Pages documentation
- Review GitHub Actions logs
- Check repository settings and permissions

For application issues:
- Check browser console for errors
- Verify API configuration
- Review the code for any syntax errors 