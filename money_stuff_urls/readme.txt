-------------------------------------------------------------------------------
On 2026-03-20, I ran commands such as
 % $market_data_processor/src/scripts/money_stuff_urls.py --page 1 |& tee 1.txt
 % $market_data_processor/src/scripts/money_stuff_urls.py --page 2 |& tee 2.txt
...
 % $market_data_processor/src/scripts/money_stuff_urls.py --page 56 |& tee 56.txt

and moved all the files into 2020-08-04_to_2026-03-26/

Then I constructed 2021-09.txt using
 % (head -n1 2020-08-04_to_2026-03-26/1.txt; grep -h 2021-09 2020-08-04_to_2026-03-26/* | sort) > 2021-09.txt
and aligned the columns manually.

Once you have partitioned the data in 2020-08-04_to_2026-03-26/ into individual
months, remove that directory completely and keep everything in yyyy-mm.txt
format.
-------------------------------------------------------------------------------

