months = {
    "January": 1,
    "February": 2,
    "March": 3,
    "April": 4,
    "May": 5,
    "June": 6,
    "July": 7,
    "August": 8,
    "September": 9,
    "October": 10,
    "November": 11,
    "December": 12,
}

import re
for data in ['March 1, 1990', 'April 2 1995', '7/15/20', 'December 13, 2003', -1]:
    if data == -1:
        break
    if re.match(r'(\w+) (\d{1,2}), (\d{4})', data) == None:
        continue
    output = data.split(" ")
    output[0] = str(months[output[0]])
    output[1] = output[1].replace(",", "")
    print("/".join(output))
