Workflow Description:

![Alt text](image.png)

- **Manual Trigger**:
  - The workflow starts with a manual trigger, allowing you to initiate the execution directly from the n8n editor.

- **Fetch CSV**:
  - Makes an HTTP GET request to "http://xmlcalendar.ru/data/ru/2022/calendar.csv".
  - Retrieves the calendar data in CSV format as binary data.

- **Fetch JSON**:
  - Makes an HTTP GET request to "http://xmlcalendar.ru/data/ru/2022/calendar.json".
  - Retrieves the calendar data in JSON format as a string.

- **Parse CSV**:
  - Takes the binary data from the "Fetch CSV" node.
  - Parses the CSV data and converts it into a JSON object.

- **Set JSON**:
  - Reads the JSON string fetched from the "Fetch JSON" node.
  - Converts the string into a JSON object.

- **Compare Data**:
  - Compares the JSON representation of the parsed CSV data with the fetched JSON data.
  - Outputs a boolean value indicating whether the datasets are identical or not.

- **If Node**:
  - Evaluates the comparison result from the "Compare Data" node.
  - Routes the workflow to one of two outcomes:
    - "Are Identical" if the datasets match.
    - "Not Identical" if they don't.

- **Are Identical**:
  - A placeholder node indicating that the CSV and JSON data sources are identical.

- **Not Identical**:
  - A placeholder node indicating that the CSV and JSON data sources are not identical.

This workflow essentially fetches calendar data from two sources (CSV and JSON), processes the data, compares them, and then routes to an outcome based on the comparison result.



Try using the link to import the workflow:


https://n8n.io/workflows/import?data=eydub2Rlcyc6IFt7J25hbWUnOiAnTWFudWFsIFRyaWdnZXInLCAndHlwZSc6ICduOG4tbm9kZXMtYmFzZS5tYW51YWwnLCAndHlwZVZlcnNpb24nOiAxLCAncG9zaXRpb24nOiBbNTAsIDIwMF19LCB7J3BhcmFtZXRlcnMnOiB7J3VybCc6ICdodHRwOi8veG1sY2FsZW5kYXIucnUvZGF0YS9ydS8yMDIyL2NhbGVuZGFyLmNzdicsICdyZXNwb25zZUZvcm1hdCc6ICdmaWxlJ30sICduYW1lJzogJ0ZldGNoIENTVicsICd0eXBlJzogJ244bi1ub2Rlcy1iYXNlLmh0dHBSZXF1ZXN0JywgJ3R5cGVWZXJzaW9uJzogMSwgJ3Bvc2l0aW9uJzogWzI1MCwgMTAwXX1dLCAnY29ubmVjdGlvbnMnOiB7fX0=


If it does not work - use the .json file import.

