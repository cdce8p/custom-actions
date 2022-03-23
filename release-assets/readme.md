# Upload release assets

## Example usage

```yaml
      - name: Upload release assets
        uses: cdce8p/custom-actions/release-assets@main
        with:
          paths: |
            "dist/"
          file_map: |
            "*.whl=application/zip"
            "*.tar.gz=application/gzip"
```

## Example output

```
Upload assets
  -- Load list with existing assets
  -- Delete assets
  -- Find files
  Paths: ['dist/']
  File map: {'*.whl': 'application/zip', '*.tar.gz': 'application/gzip'}
  Found 'dist/my-project.tar.gz' -> 'application/gzip'
  Found 'dist/my_project-py3-none-any.whl' -> 'application/zip'
  -- Upload assets
  Successfully uploaded 'my-project.tar.gz'
  Successfully uploaded 'my_project-py3-none-any.whl'
```

## Alternatives

* https://github.com/marketplace/actions/gh-release#%EF%B8%8F-uploading-release-assets
