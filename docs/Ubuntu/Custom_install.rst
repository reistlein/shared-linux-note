======================
Custom installation
======================


---------------------
Set hostname [#]_
---------------------

.. code::

    hostnamectl set-hostname precision

.. [#] https://mutschler.dev/linux/pop-os-post-install/





Install vlc (video) and calibre (ebook)

.. code::

    sudo apt install -y vlc calibre

Install and compile multimedia codecs:

.. code::

    sudo apt install -y libavcodec-extra libdvd-pkg; sudo dpkg-reconfigure libdvd-pkg

Instal Java JRE

.. code::

    sudo apt install -y default-jre

Install ansible

.. code::

    sudo apt install -y  ansible



    

---------------------
Install yubikey [#]_
---------------------


.. code::

    sudo apt install -y libpam-yubico yubikey-manager yubikey-personalization

.. [#] Official Web page https://support.system76.com/articles/yubikey-login/


see yubikey configuration guide [#]_

 * YubiKey Configuration Slot 1 is already programmed for Yubico OTP and ready to use
 * YubiKey Configuration Slot 2 is not configured. 
  
Configuration Slot 1 is used to generate the passcode when you touch the YubiKey button for between 0.3 and 1.5 seconds and then release. 

Configuration Slot 2 is used if you touch the button for between 2 and 5 seconds and then release.


.. [#] https://support.yubico.com/hc/en-us/articles/360016614800-YubiKey-for-YubiCloud-Configuration-Guide

^^^^^^^^^^^^^^^^^^^^^^^^^
Create challenge response
^^^^^^^^^^^^^^^^^^^^^^^^^

.. code::

    user$ ykpersonalize -2 -ochal-resp -ochal-hmac -ohmac-lt64 -oserial-api-visible

You should receive a message similar to:

Stored initial challenge and expected response in '$HOME/.yubico/challenge-123456'.

---------------------
Install pyhon
---------------------

sudo apt-get install python3-pip python3.10-venv



/home/jpalmier/Documents/01_python-env/python-env/bin/


/home/jpalmier/Documents/01_python-env/python-env/bin/sphinx-autobuild  source build


sudo apt-get -y install gitg

