Exim4 to sms gate redirection transport
=======================================


Instalation
===========

1. Install Exim4
2. Choose many config files configuration
3. Copy transport and router into Exim4 `conf.d` directory
4. Edit `etc/exim4/conf.d/transport/01-sms_pipe` to apply your sms gate settings
5. Update Exim4 configs

.. parsed-literal::

    sudo update-exim4.conf

6. Restart Exim4 

.. parsed-literal::

    sudo service exim4 restart


Usage
==========

.. parsed-literal::

    echo "" |  mail -s 'MESSAGE' PHONE@sms
    # MESSAGE - sms message text
    # PHONE - phone number

    # Example:
    echo "" |  mail -s 'Raid alert' 71234567890@sms
