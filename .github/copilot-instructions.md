## Development Environment
- **Python Version**: 3.11
- **Environment Manager**: Conda (environment name: `datagenie`)

## Environment Activation
- **ALWAYS** check if the `datagenie` conda environment is active before running Python code or installing packages
- **CRITICAL**: When running ANY pip install command or Python script, ALWAYS use: `conda activate datagenie && <command>`
- Example: `conda activate datagenie && pip install google-generativeai`
- Example: `conda activate datagenie && python script.py`
- Never install Python packages or run Python commands in the base environment
- All Python operations (pip install, running scripts, executing notebooks) must be done in the activated `datagenie` environment
- If user asks to "pip install X", automatically run: `conda activate datagenie && pip install X`

## When Writing Code
- Include error handling for API calls
- Don't add print statements to show progress and results
- Don't use Emoji for print statement
- Use markdown cells in notebooks to explain concepts before code


## Testing and Validation
- Test code in the activated conda environment (`datagenie`)

## Environment Variable Configuration Instruction

- Don't read the .env file directly in code.
- The following keys are available as environment variables, so whenever you write code to access API keys, use these environment variable names:
    - GOOGLE_API_KEY
    - OPENAI_API_KEY 
    - GROQ_API_KEY