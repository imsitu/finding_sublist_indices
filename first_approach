data = [
        ("username1", "phonenumber1", "email1"),
        ("usernameX", "phonenumber1", "emailX"),
        ("usernameY", "phonenumberZ", "email1Z"),
        ("usernameZ", "phonenumberY", "emailX")
    ]


def indices(data):
    common = set()
    uncommon = set()
    indices_list = []
    i = 0
    while i < len(data):
        y = False
        j = i + 1
        current_tuple = data[i]
        while j < len(data):
            comapring_tuple = data[j]
            x = compare(current_tuple, comapring_tuple)
            if x:
                common.add(i)
                common.add(j)
                y = True
            if not y:
                if i in common:
                    pass
                else:
                    uncommon.add(i)
            j += 1
        i += 1
    indices_list.append(list(common))
    indices_list.append(list(uncommon))

    return indices_list


def compare(current_tuple, comparing_tuple):
    return any(x == y for x, y in zip(current_tuple, comparing_tuple))


indices_list = indices(data)
print(indices_list)
