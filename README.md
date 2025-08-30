
# YouTube Manager - Python Terminal Application

A lightweight Python-based YouTube video manager that allows users to track their favorite videos without requiring a database. This application stores video information in a simple text file using JSON format, making it perfect for beginners learning file handling and basic CRUD operations in Python.




## Features

- **List Videos**: View all saved YouTube videos with their names and durations
- **Add Videos**: Store new YouTube videos with name and duration
- **Update Videos**: Modify existing video details
- **Delete Videos**: Remove videos from your collection
- **Persistent Storage**: Data is saved between sessions using a text file



## Code Explanation

### 1. Data Storage Functions

```bash
def load_data():
  try:
      with open('youtube.txt', 'r') as file:
        return json.load(file)
  except FileNotFoundError:
      return []
    
def save_data_helper(videos):
      with open('youtube.txt', 'w') as file:
        json.dump(videos, file)
```
- ```load_data()```: Reads video data from 'youtube.txt' using JSON format. If the file doesn't exist, returns an empty list.

- ```save_data_helper(videos)```: Writes the current video list to 'youtube.txt' in JSON format.

### 2. Core Operations

```bash
def list_all_videos(videos):
    # Displays all videos with numbering

def add_video(videos):
    # Adds a new video with user-provided name and duration

def update_video(videos):
    # Updates an existing video's details

def delete_video(videos):
    # Removes a video from the collection
```

Each operation calls ```save_data_helper(videos)``` to persist changes to the file.

### 3. Main Application Loop

```bash
  def main():
    videos = load_data()
    while True:
        # Display menu options
        # Process user choice with match-case statement
```
The main function loads existing data and presents a continuous menu until the user chooses to exit.



## Installation & Usage

### 1. Clone the repository:

```bash
  git clone https://github.com/your-username/youtube-manager.git
```
### 2. Navigate to the project directory:


```bash
  cd youtube-manager
```

### 3. Run the application:

```bash
 python youtube_manager.py
```


    
## Screenshots

![Logo](<img width="830" height="385" alt="image" src="https://github.com/user-attachments/assets/9dfe89bd-8c08-4631-9679-7d33b82dfa40" />)
![Logo](<img width="619" height="250" alt="image" src="https://github.com/user-attachments/assets/d4996532-6111-4a0e-974a-93486d58603c" />)





## File Structure

```
youtube-manager/
├── youtube_manager.py  # Main application file
├── youtube.txt         # Data storage file (created automatically)
├── README.md           # Project documentation
└── screenshots/        # Folder for application screenshots
    ├── menu.png
    └── video-list.png

```


## Technologies Used

- **Python 3.10+** (for match-case feature)

- **JSON** for data serialization

- **File I/O** for persistent storage

## Learning Outcomes
**This project demonstrates:** 
- File handling in Python
- JSON serialization/deserialization
- CRUD operations implementation
- Basic error handling with try-except
- Menu-driven application design

Perfect for Python beginners learning file handling, data management, and practical application development!
