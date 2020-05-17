# Install dotnet
    wget https://packages.microsoft.com/config/ubuntu/19.10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
    sudo dpkg -i packages-microsoft-prod.deb 
    sudo apt update
    sudo apt install apt-transport-https
    sudo apt update
    sudo apt install dotnet-sdk-3.1
    sudo apt install aspnetcore-runtime-3.1
    sudo apt install dotnet-runtime-3.1

# Build app
    dotnet publish -c Release

# Create docker image
    docker build -t hello-world-dotnet -f Dockerfile .

# Run app
    docker run -it --rm hello-world-dotnet
