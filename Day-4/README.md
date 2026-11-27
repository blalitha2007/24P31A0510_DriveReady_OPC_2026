# Electric Car Showroom — Day 4 AI Agent

An educational customer-support agent upgraded from the supplied Day 2 notebook using the trainer's Day 4 architecture.

## Features
- Sample catalogue and exact price calculations (cars).
- Opening-hours tool routes unknown timings to admin.
- Pydantic record validation and Google Sheets logging for pending demo requests.
- Conversation memory, error handling, trace, five structured-output examples and tool-name experiment.

## Files
- `Electric_Car_Showroom_Day4.ipynb` — Google Colab notebook
- `tests.csv` — planned test cases; actual results are generated in Colab
- `README.md` — project guide

## Run in Google Colab
1. Open [Google Colab](https://colab.research.google.com/) and upload `Electric_Car_Showroom_Day4.ipynb`.
2. Run the setup cell and enter your private Groq API key in the masked prompt.
3. Authenticate Google and open the printed demo sheet link.
4. Run subsequent cells in order. The test cell may save a fictional request; avoid repeated runs if you do not want duplicate demo rows.
5. Download the generated tests.csv after reviewing the responses.

## Architecture
Customer → LangChain agent (Groq `openai/gpt-oss-20b`) → `get_price` / `is_open` / `log_booking` → Pydantic validation → Google Sheets → response.

## Day 4 assignment
Price and timing tools, structured extraction of five messages, validated sheet logging, invalid-input tests, trace counts and the vague-tool experiment are included. The supplied Day 2 project had a price function; the timing tool is a new addition.

## GitHub
Upload the three files into Day-4. Add the Open in Colab badge once the notebook is uploaded: in Colab use File → Save a copy in GitHub and select Include a link to Colaboratory. Do not add a second manual badge. Clear private outputs and never commit API keys.

## Demo limitations
All prices are from the supplied sample catalogue; actual hours are not known. Colour and request type are optional enquiry details. Requests are pending admin review, not real bookings or confirmed orders. One catalogue entry per record. Python syntax and notebook format checked; live Groq/Sheets calls need your account and have not been executed.
