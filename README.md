# LogAnalyzer3

Log analysis tool for RoboCup Soccer Simulation 2D

## Data obtained

- Date
- Our team name
- Opp team name
- Our final team point
- Opp final team point
- Our penalty shootout point
- Opp penalty shootout point
- Final result (win = 3, lose = 0, draw = 1)
- Our domination time
- Opp domination time
- Our possession
- Opp possession
- Number our yellow cards
- Number opp yellow cards
- Number of our passes
- Number of our passes (only left direction)
- Number of our passes (only right direction)
- Number of our passes (only front direction)
- Number of our passse (only back direction)
- Number of opp passes
- Number of opp passes (only left direction)
- Number of opp passes (only right direction)
- Number of opp passes (only front direction)
- Number of opp passes (only back direction)
- Number of our through passes
- Number of opp through passes
- Number of our successed tackles
- Number of our failed tackles
- Number of opp successed tackles
- Number of opp failed tackles
- Number of our shoots
- Number of opp shoots
- Our point
- Opp point
- Number of our dribbles
- Number of opp dribbles
- Number of entering into ball opp penalty area
- Number of entering into ball our penalty area
- Number of our disconnected players
- Number of opp disconnected players

## How to Use

### Add path

if you add `export PATH="/path/to/loganalyzer3:$PATH"` at the bottom of the "~/.bashrc", you can use loganalyzer3 everywhere

### Required libraries

- matplotlib
	- If you want to plot "Kick distribution" or "Kick sequence", latex environment is required.
	- `sudo apt install texlive texlive-latex-extra texlive-fonts-recommended dvipng msttcorefonts`
- gzip
- ...
- cython (if you comlipe it)

`pip install matplotlib cython gzip `

### Compile cython

you can compile cython files (work for only Ubuntu OS)

`/path/to/loganalyzer3/build.sh`

you can also use this analyzer without compilation

### Options

#### Examples of options

##### debug mode: 

`--debug` 

output to stdout when and who do pass, and output figures of action_sequences and kick_distributions

##### dir mode: 

`dirname -l` 

analyze all files in the `dirname`

##### file mode: 

`filename --side l`

analyze only `filename`

### Examples of Execution

- `loganalyzer3 /path/to/dir -l`
- `loganalyzer3 /path/to/file --side l --debug`
- `loganalyzer3 /path/to/dir --team HELIOS_base --each-cycle`

### Note

- Data are outputted in csv format
- File name is determined by the target teams (e.g. HELIOS_base.csv)
- Save directory is same as the directory at which you execute `loganalyzer3` 
