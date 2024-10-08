# AutoMessenger

AutoMessenger is a Python package designed to automate the sending of messages using `pyautogui`. It allows you to send messages at random intervals to a specified input field, with support for custom and default messages.

## Features

- **Automated Messaging**: Send messages automatically at random intervals.
- **Customizable Messages**: Use default messages or specify your own custom messages.
- **Input Field Positioning**: Set the exact location where messages will be typed.
- **Flexible Timing**: Specify the delay before starting and randomize message sending intervals.

## Installation

To install AutoMessenger, ensure you have Python 3.6+ installed on your system. You can install the package from PyPI using pip:

```bash
pip install AutoMessenger
```

## Usage

After installation, you can use the `AutoMessenger` class to start sending automated messages. Below are detailed instructions and examples for using the package.

### Basic Example

Here is a simple example demonstrating how to use AutoMessenger:

```python
from AutoMessenger import AutoMessenger

# Define custom messages
external_messages = [
    "Good Morning!",
    "What's up?",
    "Hope you're doing well!"
]

# Create an instance of AutoMessenger with custom messages
messenger = AutoMessenger(external_messages=external_messages)

# Set the input field where messages will be typed
messenger.set_input_position()  # Wait 5 seconds to record the position of the input field

# Start sending messages with a 10-second delay before the first message
messenger.start_sending(delay=10)
```

### Step-by-Step Instructions

#### 1. Setting Up the Input Position

The `set_input_position()` method records the cursor position for the input field where messages will be sent. Place your cursor over the desired input field and call this method. The script will wait 5 seconds for you to position the cursor.

```python
messenger.set_input_position()
```

#### 2. Providing Custom Messages

You can provide your own list of messages to be sent. If no external messages are provided, the package will use its default messages.

```python
external_messages = [
    "Hello there!",
    "How are you today?",
    "What's new?"
]

messenger = AutoMessenger(external_messages=external_messages)
```

#### 3. Starting the Messenger

Use the `start_sending()` method to begin the messaging process. You can specify a delay (in seconds) before the first message is sent. Messages will be sent at random intervals (between 1 to 5 seconds).

```python
messenger.start_sending(delay=10)
```

#### 4. Stopping the Messenger

To stop the script, press `Ctrl+C` in your terminal. This will interrupt the process and stop sending messages.

## Detailed Explanation

### Class: `AutoMessenger`

- **Initialization**: Initialize with an optional list of custom messages. If none are provided, default messages are used.
- **`set_input_position()`**: Waits 5 seconds and records the cursor position to type messages.
- **`send_message()`**: Chooses a random message from the list and types it into the specified input field.
- **`start_sending(delay)`**: Begins sending messages after the specified delay. Messages are sent at random intervals until interrupted.

### Dependencies

- **`pyautogui`**: Required for simulating keyboard and mouse actions. Install it manually if needed:

```bash
pip install pyautogui
```

## Example Script

For a complete example of using AutoMessenger, you can use the following script:

```python
from AutoMessenger import AutoMessenger

# Custom messages
external_messages = [
    "Hello there!",
    "How are you today?",
    "What's new?"
]

# Initialize AutoMessenger
messenger = AutoMessenger(external_messages=external_messages)

# Set cursor position for the input field
messenger.set_input_position()  # Wait for 5 seconds to set the cursor position

# Start sending messages
messenger.start_sending(delay=10)  # Messages will start sending after 10 seconds
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contributing

Contributions are welcome! Please submit issues and pull requests on GitHub.

## Contact

For any questions or issues, please contact:

- **Author**: GM Zulkar Nine
- **Email**: gmzulkar@gmail.com
- **GitHub**: [Your GitHub Profile](https://github.com/imzulkar)

### Summary of Additions:

- **Basic Example**: Provides a simple usage example.
- **Step-by-Step Instructions**: Detailed guidance on setting up input position, providing custom messages, starting the messenger, and stopping it.
- **Detailed Explanation**: Explanation of the `AutoMessenger` class and its methods.
- **Dependencies**: Lists and explains the required dependency.
- **Example Script**: Provides a complete script for practical use.
- **License and Contributing**: Basic information on the license and contributing guidelines.
