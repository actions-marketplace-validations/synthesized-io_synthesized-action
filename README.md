# synthesized-table
Create a synthetic copy of a tabular data file.

## Usage
Basic:

```yaml
steps:
- uses: actions/checkout@v3
- id: synthesized-table
  uses: synthesized-io/synthesized-table@v0.1
  with:
    input-file:  my-data.csv # Path to input csv file
    synthesized-key: ${{ secrets.SYNTHESIZED_KEY }} # Synthesized licence key.
    pip-index: ${{secrets.SYNTHESIED_PIP_INDEX }} # External pip index for synthesized.
- run: python my_script.py ${{ steps.synthesized-table.outputs.output-file }} # Output synthetic data is saved to csv.
```
