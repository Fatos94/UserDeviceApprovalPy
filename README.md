# User and Device Approval System

## Description
This project involves creating a user and device approval system using Python. The system checks if a given username is approved and if the corresponding device ID matches the approved device for that user. This repository provides the code implementation and demonstrates how to use it.

## Step-by-Step Process

1. **Define Approved Users and Devices:**
   We start by defining two lists:
   - `approved_users`: A list of usernames that are approved to access the system.
   - `approved_devices`: A list of device IDs that correspond to the usernames in `approved_users`.

2. **Create the `login` Function:**
   The `login` function takes two parameters: `username` and `device_id`. It performs the following checks:
   - Verifies if the `username` is in the `approved_users` list.
   - If the username is approved, it checks if the provided `device_id` matches the assigned device ID for that user.
   - Provides appropriate messages based on the checks.

3. **Test the Function:**
   Call the `login` function with different combinations of usernames and device IDs to test the functionality and validate the results.

## Code Implementation

```python
# Assign `approved_users` to a list of approved usernames
approved_users = ["elarson", "bmoreno", "sgilmore", "eraab", "gesparza"]

# Assign `approved_devices` to a list of device IDs that correspond to the usernames in `approved_users`
approved_devices = ["8rp2k75", "hl0s5o1", "4n482ts", "a307vir", "3rcv4w6"]

# Define a function named `login` that takes in two parameters, `username` and `device_id`
def login(username, device_id):
    # If `username` belongs to `approved_users`,
    if username in approved_users:
        # then display "The user ______ is approved to access the system.",
        print("The user", username, "is approved to access the system.")
        # assign `ind` to the index of `username` in `approved_users`,
        ind = approved_users.index(username)
        # and execute the following conditional
        # If `device_id` matches the element at the index `ind` in `approved_devices`,
        if device_id == approved_devices[ind]:
            # then display "______ is the assigned device for ______" 
            print(device_id, "is the assigned device for", username)
        # Otherwise,
        else:
            # display "______ is not their assigned device"
            print(device_id, "is not their assigned device.")
    # Otherwise (part of the outer conditional and handles the case when `username` does not belong to `approved_users`),
    else:
```

Conclusion
This project demonstrates a simple user and device approval system using Python. By defining approved users and their corresponding devices, and implementing a function to check these, we can ensure that only authorized users with the correct devices can access the system. This setup can be extended for more complex scenarios and integrated with larger authentication systems.

Feel free to contribute to this project by adding more features, improving the code, or fixing any issues.
        # Display "The user ______ is not approved to access the system."
        print("The username", username, "is not approved to access the system.")

# Call the function you just defined to experiment with different username and device_id combinations
login("bmoreno", "hl0s5o1")
login("elarson", "r2s5r9g")
login("abernard", "4n482ts")
