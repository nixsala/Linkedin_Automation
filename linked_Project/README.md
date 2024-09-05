


## Prerequisites

### 1. Python Installation

Make sure you have Python installed. 


### 1. Python Installation

Make sure you have Python installed. 

To check your Python version, run the following command:

python --version


### 2. Install Required Libraries

Install the necessary Python libraries by running:


pip install selenium webdriver-manager openpyxl


### 3. Chrome WebDriver

The `webdriver-manager` automatically handles the Chrome WebDriver installation, so no manual setup is required. Ensure you have Google Chrome installed on your system.

## Setup

1. **Clone or Download the Repository**  
   Clone this repository or download it as a ZIP file and extract it.

2. **Create a `comments.txt` file**  
   In the project folder, create a `comments.txt` file and populate it with different comments that will be posted on LinkedIn group posts (one comment per line). For example:

   ```
   Great post! Thanks for sharing.
   This is really insightful, appreciate it!
   Nice work, keep it up!
   ```

3. **Configure Login Credentials**  
   Open the script file (`lintest.py`) and update the following lines with your LinkedIn email and password:

   
   email_field.send_keys("your_email")
   password_field.send_keys("your_password")
   

4. **Run the Script**  
   Activate your virtual environment (if applicable), and run the script using the following command:

   
   python lintest.py
   

## How the Script Works

1. **Login**:  
   The script navigates to LinkedIn's login page, enters your credentials, and logs in.

2. **Navigate to a Group**:  
   The script navigates to a specified LinkedIn group page (e.g., `https://www.linkedin.com/groups/1976445/`).

3. **Perform Actions on Posts**:
   - **Like**: The script likes posts if not already liked.
   - **Comment**: It picks a random comment from `comments.txt` and posts it.
   - **Repost**: The script reposts the post.
   - **Follow**: It follows the post's author if the "Follow" button is visible.
   
   These actions are repeated for all visible posts, and the page scrolls down to load more posts.

4. **Action Logging**:  
   Each post's URL and the actions performed on it (like, comment, repost, follow) are logged in an Excel file (`action_log.xlsx`) to prevent performing duplicate actions in future runs.







