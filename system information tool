import subprocess

def view_running_services():
    print("=== Running Services ===")
    try:
        services = subprocess.check_output(["systemctl", "list-units", "--type=service", "--state=running"])
        print(services.decode())
    except subprocess.CalledProcessError:
        print("Failed to retrieve running services.")

def view_memory_usage():
    print("=== Memory Usage ===")
    try:
        memory = subprocess.check_output(["free", "-h"])
        print(memory.decode())
    except subprocess.CalledProcessError:
        print("Failed to retrieve memory usage.")

def view_all_drivers():
    print("=== All Drivers ===")
    try:
        drivers = subprocess.check_output(["lsmod"])
        print(drivers.decode())
    except subprocess.CalledProcessError:
        print("Failed to retrieve loaded drivers.")

if __name__ == "__main__":
    while True:
        print("Select an option:")
        print("1. View Running Services")
        print("2. View Memory Usage")
        print("3. View All Drivers")
        print("4. Exit")

        choice = input()

        if choice == "1":
            view_running_services()
        elif choice == "2":
            view_memory_usage()
        elif choice == "3":
            view_all_drivers()
        elif choice == "4":
            print("Exiting...")
            break
        else:
            print("Invalid option. Please try again.")
