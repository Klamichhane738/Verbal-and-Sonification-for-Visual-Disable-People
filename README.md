# Dynamic JSON Data Visualization and Sonification

This web application allows users to upload a JSON file containing time-series data and provides both a visual chart and an auditory representation (sonification) of the data. It dynamically adapts to different JSON file structures, making it versatile for various data analysis tasks.

## Features

- **Dynamic Data Handling:** Automatically detects and processes numerical data fields within uploaded JSON files.
- **Chart Visualization:** Generates a line chart using Chart.js to visually represent the data over time.
- **Discrete Sonification:** Provides an auditory representation of the data, where the tone, frequency and gain changes according to the data with a unique sound at each data point to avoid overlap.
- **Trend Indication:** Auditory cues and verbal feedback indicate if the data value is increasing, decreasing or stable at a given time.
- **Verbal Feedback:** Uses the Web Speech API to narrate the data value, trend and time.
- **Flexibility:** Works with any JSON file containing an array of objects, each with at least one numeric field and a "time" field.
- **Clear User Instructions:** Includes an explanation of how the app works directly on the page.

## How It Works

1.  **Upload JSON File:** Use the "Choose File" button to upload your JSON file. Ensure that your JSON data is in the correct format for optimal results. The format should contain an array of objects, where each object represents a data point and has a 'time' field and at least one numeric field.
2.  **Automatic Data Detection:** The application automatically detects the first numerical field within your dataset to generate the chart and use for sonification. It also uses the field with the name time for the x-axis.
3.  **Chart Visualization:** Once the file is loaded, a line chart is generated, visualizing the data over time.
4.  **Sonification:** Click the "Start Audio" button to start the sonification. The application will then represent changes in the value using tone, volume, and frequency, it will also announce the value, and time, as well as any trends.
5.  **Trend Indication:** The auditory and speech output will indicate if the data value is increasing, decreasing or stable at a given point in time.

## Usage

1.  **Clone the Repository:**
    ```bash
    git clone [YOUR_REPOSITORY_URL]
    ```
   (Replace `[YOUR_REPOSITORY_URL]` with the actual URL of your GitHub repository.)
2.  **Navigate to the Project Directory:**
    ```bash
     cd [YOUR_REPOSITORY_NAME]
    ```
    (Replace `[YOUR_REPOSITORY_NAME]` with the name of your repository)
3.  **Open the `index.html` file** in a web browser.
4.  Click the "Choose File" button to upload a JSON file.
5. After the file loads, a line chart of the data is displayed.
6.  Click the "Start Audio" button to initiate the sonification and verbal feedback.
7. The sounds will stop when the end of the dataset is reached.

## Technologies Used

-   HTML
-   CSS
-   JavaScript
-   [Chart.js](https://www.chartjs.org/) for charting
-   [Tone.js](https://tonejs.github.io/) for audio synthesis
-   Web Speech API for verbal feedback

## Sample Data Format

The JSON file should be an array of objects with a "time" field and at least one numeric data field. For example:

```json
[
  {
    "time": "2023-01-01",
    "temperature": 25
  },
   {
    "time": "2023-01-02",
    "temperature": 27
  },
  {
     "time": "2023-01-03",
     "temperature": 24
   },
  {
    "time": "2023-01-04",
    "temperature": 22
   }