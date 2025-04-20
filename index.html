import os
import subprocess
import sys

def install_dependencies():
    """Install required packages"""
    subprocess.run(["pkg", "update", "-y"], check=True)
    subprocess.run(["pkg", "install", "-y", "wget", "unzip", "openssl", "binutils", "python"], check=True)

def download_server():
    """Download Bedrock Server"""
    url = "https://minecraft.azureedge.net/bin-linux/bedrock-server-1.21.72.zip"
    if not os.path.exists("bedrock-server-1.21.72.zip"):
        subprocess.run(["wget", url], check=True)

def extract_files():
    """Extract server files"""
    if not os.path.exists("bedrock_server"):
        subprocess.run(["unzip", "bedrock-server-1.21.72.zip"], check=True)

def configure_server():
    """Create basic configuration"""
    if not os.path.exists("server.properties"):
        config = """server-name=Termux Server
gamemode=survival
difficulty=easy
allow-cheats=false
max-players=10
server-port=19132
server-portv6=19133"""
        with open("server.properties", "w") as f:
            f.write(config)

def fix_libraries():
    """Fix library dependencies"""
    lib_path = "/data/data/com.termux/files/usr/lib"
    if not os.path.exists("libcurl.so.4"):
        os.symlink(f"{lib_path}/libcurl.so", "libcurl.so.4")

def start_server():
    """Start the Minecraft server"""
    os.environ["LD_LIBRARY_PATH"] = "."
    subprocess.run(["./bedrock_server"], check=True)

def main():
    try:
        print("Setting up Minecraft Bedrock Server 1.21.72")
        install_dependencies()
        download_server()
        extract_files()
        os.chdir("bedrock_server")
        configure_server()
        fix_libraries()
        print("Starting server...")
        start_server()
    except Exception as e:
        print(f"Error: {str(e)}")
        sys.exit(1)

if __name__ == "__main__":
    main()
