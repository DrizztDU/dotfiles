# dotfiles

Setups and configures all software I used on macOS/Debian/Ubuntu. It's really simple and easy.

> Currently, running on macOS Monterey/Debian11+/Ubuntu22.04+.

## Installation

For me, I prefer the newer version of python. But you can choose a lower version, such as python3.8.

1. Install Python.

   - For macOS, make sure to install [Homebrew](https://brew.sh/) and python3.9+.

       ```shell
       # macOS
       brew install python@3.9
       ```
   
   - For Debian/Ubuntu, make sure to install pip3 and venv.

      > Python3.9+ preinstalled in Debian11+/Ubuntu22.04+.
     
      ```shell
      sudo apt install -y python3-pip python3-venv
      ```

2. Clone this repository:

    ```shell
    git clone https://github.com/DrizztDU/dotfiles ~/.dotfiles
    ```

3. Create a virtual environment:

    ```shell
    cd ~/.dotfiles
    python3 -m venv .venv
    ```

4. Install ansible and run ansible playbook:

   ```shell
   source .venv/bin/activate
   pip install pip=='22.1.2' pip-tools=='6.7.0'
   pip-compile --no-emit-index-url requirements.in
   pip-sync requirements.txt
   ansible-playbook ansible/main.yaml
   ```

## License

[MIT](LICENSE)
