#### Description

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
