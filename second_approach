
data = [
        ("username1", "phonenumber1", "email1"),
        ("usernameX", "phonenumber1", "emailX"),
        ("usernameY", "phonenumberdata", "email1data"),
        ("usernamedata", "phonenumberY", "emailX")
    ]

index_list = set()
non_index_list = set()
last_index = 0
for i in range(len(data) - 1):
    if i in non_index_list:
        if any(check in list(data[last_index]) for check in list(data[i + 1])):
            index_list.add(i + 1)
            last_index = i + 1
        else:
            non_index_list.add(i + 1)

    else:
        if any(check in list(data[i]) for check in list(data[i + 1])):
            index_list.add(i)
            index_list.add(i + 1)
            last_index = i + 1

        else:
            non_index_list.add(i + 1)

print([list(index_list), list(non_index_list)])
