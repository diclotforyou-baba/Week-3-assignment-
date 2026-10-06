==================================================
FILE 1: grade_reporter.py
==================================================

# Grade Reporter

scores = [72, 45, 90, 61, 38]

passed = 0
failed = 0
total = 0

for score in scores:
    if score >= 80:
        grade = "A"
    elif score >= 70:
        grade = "B"
    elif score >= 50:
        grade = "C"
    else:
        grade = "F"

    print(f"Score: {score}, Grade: {grade}")

    if score >= 50:
        passed += 1
    else:
        failed += 1

    total += score

average = total / len(scores)

print(f"Passed: {passed}")
print(f"Failed: {failed}")
print(f"Average: {round(average, 1)}")


==================================================
FILE 2: bug_hunt.py
==================================================

count = 1
total = 0

# BUG: The while statement was missing a colon at the end.
while count <= 5:
    total = total + count
    count = count + 1

# BUG: count < 5 excluded the number 5, so it was changed to count <= 5.

# BUG: A string and integer cannot be joined with +, so an f-string is used.
print(f"Sum of 1 to 5 is: {total}")


==================================================
FILE 3: README.md
==================================================

# Grade Reporter & Bug Hunt

`grade_reporter.py` - Uses loops and conditions to calculate grades, pass/fail counts, and the average score.

`bug_hunt.py` - Finds and fixes three bugs in a while loop program that calculates the sum of 1 to 5.

The hardest bug to find was the `count < 5` condition because the program could run without showing an error. I knew something was wrong because the program printed an answer other than the expected result of 15, so I checked the loop condition and saw that 5 was being left out.

Repository name: "plp-python-week3"

Files required:

- "grade_reporter.py"
- "bug_hunt.py"
- "README.md"
