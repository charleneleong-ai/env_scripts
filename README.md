## Helper Environment scripts


Here are some helper scripts to make working with Python virtual environments, Conda environments and AWS easier!

Please feel free to adapt and improve! 

### Requirements
The following instructions assume you are using ZSH Shell on MacOS. If not, please refer to the appropriate package download for your specific OS!

Please install Brew and the required [platform dev tools](https://github.com/Faethm-ai/platform-dev-tools/tree/master/mac).


- [ZSH Shell](https://ohmyz.sh/#install)
  - ```
    sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
    ```
- [AWS CLI v2](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html)
  - ```bash
    brew install awscli
    ```
- [saml2aws](https://github.com/Versent/saml2aws)
  - ```bash
    brew tap versent/homebrew-taps
    brew install saml2aws
    saml2aws --version
    ```
- [Python 3.x](https://docs.python-guide.org/starting/install3/osx/)
  - ```bash
    brew install python
    ```
- [Miniconda](https://repo.anaconda.com/archive/) or [Conda](https://docs.anaconda.com/anaconda/install/mac-os/) is not included in [platform dev tools](https://github.com/Faethm-ai/platform-dev-tools/tree/master/mac) above.
  - ```bash
    wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
    chmod a+x Miniconda3-latest-Linux-x86_64.sh
    ./Miniconda3-latest-Linux-x86_64.sh -b -p ~/miniconda
    ```


Source these scripts in your `~/.zshrc`

```bash
...
source ~/env_scripts/conda_auto_env
source ~/env_scripts/auto_venv
source ~/env_scripts/saml2aws
...
```