```
# Enable pyenv
source .venv/bin/activate

# Calculate IBKR 45268 (non-ISA) + Schwab
python3 -m cgt_calc --year 2024 --exchange-rates-file data/exchange_rates.csv --raw data/IBKR-45268.csv --no-balance-check --report data/calculations.pdf --schwab data/Marina.csv --schwab-award data/EquityAwards.csv

# Calculate Schwab
python3 -m cgt_calc --year 2024 --exchange-rates-file data/exchange_rates.csv --no-balance-check --report data/calculations-schwab.pdf --schwab data/Marina.csv --schwab-award data/EquityAwards.csv

# Calculate IBKR 45268 (non-ISA)
python3 -m cgt_calc --year 2024 --exchange-rates-file data/exchange_rates.csv --raw data/IBKR-45268.csv --no-balance-check --report data/calculations-ibkr-45268.pdf 


# Calculate IBKR 26217 (ISA)
python3 -m cgt_calc --year 2024 --exchange-rates-file data/exchange_rates.csv --raw data/IBKR-26217.csv --no-balance-check --report data/calculations-ibkr-26217.pdf 
```