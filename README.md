 BrainlabFile Class

This Python script is designed for parsing and extracting metadata from file paths related to electrochemical measurements. The `BrainlabFile` class provides a structured way to handle electrochemical data files, automatically extracting relevant information based on file names and directory structures.

 Key Features:
- Automatic Extraction: Extracts metadata such as electrochemical technique, working electrode support, measurement date, channel, and cell number directly from the file path.
- Regex-based Parsing: Uses regular expressions to parse key attributes like techniques (e.g., CV, LSV, CA), supports (e.g., ITO, FTO), and measurement dates.
- File Information Handling: Generates organized information about the file's base path, folder, and name.
- README Processing: Extracts detailed information from README files, including both YAML-formatted content and verbose comments.
- Robust Error Handling: Allows for flexible input handling and manages incomplete or missing metadata fields gracefully.

 Methods:
- set_all_variables: Initializes class attributes by setting electrochemical technique, electrode support, date, channel, and cell number.
- set_file_info: Organizes and stores base path, folder, and file name into a structured dictionary.
- extract_readme_info: Extracts both YAML-formatted data and verbose comments from README files.
- _search: A utility function for performing regular expression searches on file paths and file names.

 Example Use Case:
The script can handle multiple file formats and provides an easy way to process and print electrochemical experiment metadata for different file structures.

 How to Use:
- Create an instance of the `BrainlabFile` class by providing the absolute path to a measurement file.
- Use the built-in methods to extract and print relevant metadata and file structure information.

```python
 Example
file_path = "Y:/Caracterizacion_Cells/ITO/CV/070624/CANAL1/celda1.txt"
brainlab_file = BrainlabFile(file_path)
print(brainlab_file)
brainlab_file.info()
```
