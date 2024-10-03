<p align="center">
</p>
<p align="center">
    <h1 align="center">EVENT-DRIVEN-RN-WEBVIEW-BRIDGE</h1>
</p>
<p align="center">
    <em><code>Eliminating Message Loss and Ensuring Reliable Data Exchange Between React Native and WebView</code></em>
</p>
<p align="center">
	<img src="https://img.shields.io/github/license/ghdtjgus76/event-driven-rn-webview-bridge?style=flat-square&logo=opensourceinitiative&logoColor=white&color=0080ff" alt="license">
</p>

<br>

##### 🔗 Table of Contents

- [📍 Overview](#📍-overview)
- [👾 Features](#👾-features)
- [📦 Installation](#📦-installation)
- [🤖 Usage](#🤖-usage)
- [🤝 Contributing](#🤝-contributing)
- [🎗 License](#🎗-license)

---

## 📍 Overview

The **event-driven-rn-webview-bridge** library facilitates seamless communication between React Native applications and embedded WebView components. <br />
It addresses critical issues related to message loss and ensures reliable data exchange, making it easier for developers to integrate web content into their mobile apps. <br />This library is designed to enhance interoperability while providing a robust solution for message handling.

---

## 👾 Features

The **event-driven-rn-webview-bridge** library offers a range of features to enhance communication between React Native applications and WebView components:

- **Reliable Message Transmission**: Utilizes a Promise-based approach to provide feedback on message sending results, ensuring reliable data exchange.

- **Sequential and Concurrent Message Handling**: Effectively resolves message ordering issues, allowing both sequential and concurrent processing of messages to meet various application needs.

- **Automatic Retry Mechanism**: Implements up to three automatic retries for failed message transmissions due to network issues, ensuring higher reliability in message delivery.

- **Cross-Platform Compatibility**: Designed to work seamlessly on both iOS and Android, providing a consistent API for developers.

- **Plugin Architecture**: Supports a modular plugin system that allows developers to extend functionalities without altering the core messaging logic, promoting maintainability and flexibility.

- **Easy Integration**: Simple setup and usage, allowing developers to quickly incorporate the bridge into their existing React Native projects.

- **Extensive Documentation**: Comprehensive documentation and examples to assist developers in leveraging the full potential of the library.

These features make the **event-driven-rn-webview-bridge** a powerful tool for building interactive and robust mobile applications that require reliable communication between React Native and WebView.

---

### 📦 Installation

### For React Web Applications

To install the **event-driven-webview-bridge** library for React applications, run one of the following commands:

#### Using npm

```bash
npm install event-driven-webview-bridge-react
```

#### Using yarn

```bash
yarn add event-driven-webview-bridge-react
```

#### Using pnpm

```bash
pnpm add event-driven-webview-bridge-react
```

### For React Native Applications

To install the **event-driven-webview-bridge** library for React Native applications, use one of the following commands:

#### Using npm

```bash
npm install event-driven-webview-bridge-react-native
```

#### Using yarn

```bash
yarn add event-driven-webview-bridge-react-native
```

#### Using pnpm

```bash
pnpm add event-driven-webview-bridge-react-native
```

---

### 🤖 Usage

### For React Web Applications

```
const webviewBridge = ReactWebViewBridge.getInstance();

// Listen for messages coming from the React Native applications
webviewBridge.onMessage("toWebViewMessage", (message) => {
  setMessage(`App -> Web ${message.type}: ${message.data}`);
});

// Send a message from the WebView to the React Native applications
const response = await webViewBridge.postMessage({
  type: "toRNMessage",
  data: "Message 1",
});

```

### For React Native Applications

```
const webviewBridge = ReactNativeWebViewBridge.getInstance();

// Listen for messages coming from the WebView
webviewBridge.onMessage("toRNMessage", (message) => {
  setMessage(`Web -> App ${message.type}: ${message.data}`);
});

// Send a message from the React Native applications to the WebView
const response = await webViewBridge.postMessage({
  type: "toWebViewMessage",
  data: "Message 2",
});

```

---

## 🤝 Contributing

Contributions are welcome!

**[Report Issues](https://github.com/ghdtjgus76/event-driven-rn-webview-bridge/issues)**: Submit bugs found or log feature requests for the `event-driven-rn-webview-bridge` project.

---

## 🎗 License

This project is licensed under the MIT License. <br />For more details, please refer to the [LICENSE](LICENSE) file.
