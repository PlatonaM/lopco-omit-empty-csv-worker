## lopco-omit-empty-csv-worker

Remove lines with empty values from a CSV file.

### Configuration

`delimiter`: Delimiter used in the CSV file.

`ignored_columns`: List of columns where empty values are permitted.

### Inputs

Type: single

`source_csv`: CSV file.

### Outputs

Type: single

`output_file`: Result CSV file.

### Description

    {
        "name": "Omit Empty CSV",
        "image": "platonam/lopco-omit-empty-csv-worker:latest",
        "data_cache_path": "/data_cache",
        "description": "Omit lines containing emtpy fields from Comma-Separated Values files.",
        "configs": {
            "delimiter": null,
            "ignored_columns": null
        },
        "input": {
            "type": "single",
            "fields": [
                {
                    "name": "source_csv",
                    "media_type": "text/csv",
                    "is_file": true
                }
            ]
        },
        "output": {
            "type": "single",
            "fields": [
                {
                    "name": "output_file",
                    "media_type": "text/csv",
                    "is_file": true
                }
            ]
        }
    }
