
# RosettaStonks

**RosettaStonks** is a Chrome extension designed to enhance your performance on Rosetta Stone, a popular language learning platform. The extension tracks and stores important data related to your learning progress, including session times and course progress, and makes it easier to analyze and improve your learning experience.

## Features

- **Tracking Progress**: The extension tracks progress data from the Rosetta Stone Foundations and Fluency Builder courses.
- **Session Tracking**: Tracks time spent in each course and stores it for future analysis.
- **Customizable**: Easily customizable for additional tracking and data handling.

## Installation

To install **RosettaStonks**, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/RosettaStonks.git
   ```

2. Open Chrome and go to `chrome://extensions/`.

3. Enable "Developer Mode" by toggling the switch in the top right corner.

4. Click "Load unpacked" and select the folder where you cloned the repository.

5. The extension will now be available in your browser.

## Usage

- Once installed, the extension will automatically track progress for Rosetta Stone courses you are enrolled in.
- The extension will store progress data like course time and completion status.

## Permissions

The extension requests the following permissions:

- **`storage`**: For storing session and progress data locally.
- **`webRequest`**: To intercept requests to Rosetta Stone's tracking URLs.
- **`tabs`**: To enable or disable the extension depending on the page you're on.
- **`scripting`**: For injecting scripts into Rosetta Stone pages to track data.

## Configuration

You can customize the extension by modifying the request filters or adding new features through the `src/lib` and `src/worker` directories. The extension currently tracks the following types of requests:

- **Foundations Course Data**: Tracks requests related to session time and progress in the Foundations course.
- **Fluency Builder Data**: Tracks progress within the Fluency Builder course.

### Key Request Filters:
- **`FoundationsRequestFilter`**: Tracks requests from `totale.rosettastone.com`.
- **`FluencyBuilderRequestFilter`**: Tracks requests from `gaia-server.rosettastone.com`.

## Development

### Setup

1. Install Node.js and npm (if not already installed).
2. Clone the repository and navigate to the project folder.
3. Run `npm install` to install dependencies.
4. Run `npm run dev` to start a local development server.

### Building

1. To build the extension for production, run:
   ```bash
   npm run build
   ```

2. The build output will be in the `dist/` directory.

## Contributing

Contributions are welcome! If you find a bug or want to add new features, feel free to fork the repository and submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Credits

Created by [@mr_0x1](https://github.com/Mr-0x1).
