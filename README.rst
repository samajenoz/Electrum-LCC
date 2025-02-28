=======================================================
Electrum-LCC - Lightweight Litecoin Cash Client
=======================================================

.. raw:: html

   <div align="center">
   <img src="https://img.shields.io/badge/Electrum--LCC-Fast%20%26%20Lightweight-blue?style=for-the-badge" alt="Electrum-LCC"/>
   <img src="https://img.shields.io/badge/Python-3.7+-orange?style=for-the-badge" alt="Python 3.7+"/>
   <img src="https://img.shields.io/badge/Port_Maintainer-Loxley-purple?style=for-the-badge" alt="Maintainer: Loxley"/>
   <a href="https://github.com/samajenoz/Electrum-LCC/blob/master/LICENCE">
     <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="MIT License"/>
   </a>
   </div>

-------------------------------------------------------
A Modern, Minimal, and Secure Litecoin Cash Experience
-------------------------------------------------------

Electrum-LCC is a lightweight and user-friendly Litecoin Cash (LCC) wallet.  
Originally derived from **Thomas Voegtlin**’s Electrum, it has been adapted to Litecoin Cash by **Loxley**, focusing on **speed**, **security**, and **usability**.

- **License**: MIT License  
- **Language**: Python  
- **Homepage**: https://github.com/samajenoz/Electrum-LCC  

.. contents::
   :local:
   :depth: 2

-----------------
1. Key Features
-----------------

- **Instant On**  
  No need for the entire LCC blockchain. Electrum-LCC connects to remote nodes, letting you synchronize quickly.  

- **Security First**  
  Your private keys remain offline—never sent to servers. Protect your wallet with passphrase encryption and strong security defaults.

- **Lightweight and Fast**  
  Minimal resource footprint, ensuring compatibility with both modern and older hardware.

- **User-Friendly Interface**  
  Easily send and receive LCC, manage multiple addresses, and back up your wallet. Ideal for both beginners and advanced users.

- **Open Source and Extensible**  
  Written in Python for maintainability. Developers can easily customize or extend functionality.

----------------------------
2. Getting Started
----------------------------

Electrum-LCC is written in **Python 3.7+**.  
Below is a recommended installation path on Debian/Ubuntu; adapt for other platforms as needed.

.. code-block:: bash

   # 1. Install Python 3, pip, and other basics:
   sudo apt-get update
   sudo apt-get install python3 python3-pip

   # 2. (Optional) Install PyQt5 for the GUI:
   sudo apt-get install python3-pyqt5

   # 3. Clone or download the official repository:
   git clone https://github.com/samajenoz/Electrum-LCC.git
   cd Electrum-LCC

   # 4. Install Electrum-LCC (and dependencies) with pip:
   pip3 install .[full]

   # 5. Run Electrum-LCC:
   ./electrum-lcc

If you prefer not to install system-wide, simply keep the project folder intact and run  
``./electrum-lcc`` from within it—pip will manage dependencies locally.

----------------------------
3. Development Version
----------------------------

For contributors or bleeding-edge testers:

1. **Clone the GitHub repository**:

   .. code-block:: bash

      git clone https://github.com/samajenoz/Electrum-LCC.git
      cd Electrum-LCC

2. **Install in development mode** (installs needed dependencies):

   .. code-block:: bash

      pip3 install .[full]

3. **Compile Qt icons** for GUI:

   .. code-block:: bash

      sudo apt-get install pyqt5-dev-tools
      pyrcc5 icons.qrc -o gui/qt/icons_rc.py

4. **Compile protobuf** for payment requests:

   .. code-block:: bash

      sudo apt-get install protobuf-compiler
      protoc --proto_path=lib/ --python_out=lib/ lib/paymentrequest.proto

5. **(Optional) Generate translations**:

   .. code-block:: bash

      sudo apt-get install python-requests gettext
      ./contrib/make_locale

-------------------------
4. Creating Binaries
-------------------------

Electrum-LCC can be distributed as binaries (with dependencies bundled) to simplify user installation.

1. **Build the 'packages' directory** to gather Python dependencies:

   .. code-block:: bash

      ./contrib/make_packages

2. **Platform-specific Builds**:

   - **macOS**: Refer to ``contrib/build-osx/`` for instructions on creating a macOS application.  
   - **Windows**: Consult ``contrib/build-wine/`` to build Windows executables.  
   - **Linux**: Typically, you can provide tarballs containing the `packages` directory plus any needed scripts.

-------------------------
5. Additional Tips
-------------------------

- **Security Best Practices**  
  - Verify checksums or signatures of all downloads.  
  - Use strong passphrases and keep your seed phrase offline.

- **Regular Backups**  
  Your seed phrase is everything. Store it safely. Electrum-LCC's deterministic wallet design ensures the seed can restore your entire transaction history and balance.

- **Community & Support**  
  Join the Litecoin Cash community and follow official announcements to stay updated on new releases, security alerts, and best practices.

- **Customizations**  
  If you’re a developer, feel free to contribute or tailor Electrum-LCC to your own needs. The code is modular and open-source.

-------------------------
6. License
-------------------------

Electrum-LCC is distributed under the **MIT License**.  
To review the complete license text, please see the  
`LICENSE file <https://github.com/samajenoz/Electrum-LCC/blob/main/LICENSE>`_ in this repository.

---------------------------------
Thank You for Using Electrum-LCC!
---------------------------------

Enhance your Litecoin Cash experience with speed, security,  
and the confidence that comes from open-source development.  
Happy transacting!  
