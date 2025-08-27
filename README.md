# KaliEverythingForKasm

This repository contains a Dockerfile and necessary configuration to build a Docker image of the "Kali Everything" distribution of [Kali Linux](https://www.kali.org/) tailored specifically for use within the [Kasm Web Application](https://www.kasmweb.com/). The image is intended to provide a complete Kali Linux environment, enabling security professionals to run penetration testing, digital forensics, and security assessments through a web browser.

---

## Table of Contents

- [About](#about)
- [Requirements](#requirements)
- [Build Instructions](#build-instructions)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)

---

## About

The **Kali Everything Docker Image for Kasm** is built on top of the official Kali Linux "Everything" distribution, a comprehensive collection that includes the full suite of Kali Linux tools. It is configured for seamless integration with Kasm, allowing users to remotely access a fully-featured Kali environment through a browser.

**Features:**

- All tools and utilities from the Kali Everything package
- Optimized for web-based use in Kasm
- Fully customizable with additional tools and configurations

---

## Requirements

Ensure you have the following installed on your system:

- [Docker](https://docs.docker.com/get-docker/) (latest version recommended)
- [Kasm Workspaces](https://www.kasmweb.com/docs/latest/getting-started/introduction.html) (optional but recommended for testing integration)

---

## Build Instructions

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/JoeLipinski/KaliEverythingForKasm.git
   cd KaliEverythingForKasm
   ```

2. **Build the Docker Image:**

   To build the Docker image, run:

   ```bash
   docker build -t kali-everything-kasm .
   ```

3. **Verify the Image:**

   Once built, verify that the image is available:

   ```bash
   docker images | grep kali-everything-kasm
   ```

---

## Usage

To use this Docker image in Kasm, follow these steps:

1. **Run the Docker Container:**

   You can test the image locally before deploying it to Kasm:

   ```bash
   docker run -it kali-everything-kasm /bin/bash
   ```

2. **Configure in Kasm:**

   - Log in to your Kasm admin interface.
   - Go to **Workspaces** -> **Workspaces** -> **Add Workspace**.
   - Enter the required details:
     - **Workspace Type**: `Container`
     - **Friendly Name**: `Kali Everything`
     - **Description**: `A custom Kali Linux image with the kali-everything metapackage pre-installed.`
     - **Docker Image**: `kali-everything-kasm`
   - Save and launch the session from Kasm.

3. **Access Kali Everything via Kasm Interface:**

   Once set up in Kasm, launch the Kali Everything session from your Kasm workspace to access the full suite of Kali tools.

---

## Contributing

Contributions are welcome! Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Commit your changes with clear and concise messages.
4. Open a pull request and describe the changes you've made.

### Shout out - Thanks for your contributions!

- [XCraftMC23](https://github.com/XCraftMC23)

---

## License

This project is licensed under the MIT License.

---

## Disclaimer

This project is intended for educational and legal penetration testing purposes only. Use it responsibly.

---

**Happy hacking with Kali!**
