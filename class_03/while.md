This script runs while true, so it loops forever until something inside explicitly breaks it. Each pass calls read -p to grab input into $input.

Two checks run against that input: a string comparison for "q" (triggers break), and a regex check [0-9] for digit-only input (failing it triggers continue, so the echo below never runs). 
Anything that clears both checks falls through to the final echo, then loops back to read.
