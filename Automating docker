import os

def options():
    print("""
    Docker Container Management
    ----------------------------------
    1. List Docker images
    2. Pull Docker image
    3. List all Docker containers
    4. Launch Docker container
    5. Stop Docker container
    6. Remove Docker container
    7. Start Docker container
    8. Exit
    """)

def list_images():
    os.system("docker images")

def pull_image():
    image = input("Enter image name: ")
    os.system(f"docker pull {image}")

def list_containers():
    os.system("docker ps -a")

def launch_container():
    name = input("Enter container name: ")
    image = input("Enter container's image name: ")
    os.system(f"docker run -dit --name {name} {image}")

def stop_container():
    name = input("Enter container name: ")
    os.system(f"docker stop {name}")

def remove_container():
    name = input("Enter container name: ")
    os.system(f"docker rm -f {name}")

def start_container():
    name = input("Enter container name: ")
    os.system(f"docker start {name}")

# Ensure Docker is running
os.system("systemctl start docker")

while True:
    options()
    choice = input("Enter option (1-8): ")
    
    if choice == "1":
        list_images()
    elif choice == "2":
        pull_image()
    elif choice == "3":
        list_containers()
    elif choice == "4":
        launch_container()
    elif choice == "5":
        stop_container()
    elif choice == "6":
        remove_container()
    elif choice == "7":
        start_container()
    elif choice == "8":
        print("Exiting...")
        break
    else:
        print("Invalid option. Please enter a number between 1 and 8.")
