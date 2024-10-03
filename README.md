# Make Documentation (MDOC)
Generating reports from simulation results is a tedious and time-consuming task. The standard workflow involves designers taking screenshots of plots and tables from Cadence ADE Assembler and manually placing them into Excel spreadsheets or PowerPoint presentations. This process is not only slow but often incomplete, leading to issues with reproducing results, as crucial information such as configuration settings and sub-circuit views used in the simulation are frequently missing.

Simulation results can be exported from Cadence ADE Assembler in the form of an HTML datasheet. However, the exported datasheet has two significant drawbacks.

First, instead of a single file, the export includes a folder containing numerous files, making it difficult to manage and track in version control systems. Second, the resulting HTML file cannot be opened directly in common web browsers (e.g., Google Chrome, Firefox, Microsoft Edge) without making security adjustments, which may pose a risk to users.

MDOC is a tool specifically designed to address these issues. It consolidates the datasheet into a single, easy-to-manage HTML file that can be opened in any web browser without requiring security modifications, ensuring a smoother and safer user experience.

## Example
Assume that the Cadence ADE Assembler has generated a datasheet, resulting in a folder named  `sim_results` and a file called `sim_results.html`.
To convert the datasheet into a single, easy-to-manage file, use the following command:
```
mdoc sim_results results
```
This will produce a single HTML file, `results.html`, which can be opened in any web browser without requiring security adjustments.
In addition to simulation results, the file may also include the test bench schematic, configuration settings from config editor, and the schematics of all sub-circuit views used in the simulation.

