RAMAS
=====

 RAM Analysis System, or simply RAMAS, is an extensible carving utility which aims to ease and automate the process of analysing communication records left behind in physical memory by instant-messaging and email web clients. We have developed a forensic framework where the responsibility of creating and updating carving modules for different applications is distributed amongst practitioners. RAMAS also provides a way to inspect results, either by the inspection of forensic timelines or by making available a database which can be queried to unveil sophisticated correlations among the recovered evidence.

This tool was initially developed in the scope of the Forensic Cyber Security course at IST (https://tecnico.ulisboa.pt). A significantly extended version of this tool and a study over the recovery of communication records from memory has undergone peer review and was accepted for publication at SECRYPT 2017 - [Link to paper](http://web.ist.utl.pt/diogo.barradas/papers/RAMAS_SECRYPT17.pdf).

Supported Applications
----------------------

RAMAS is able to extract communication records from several web-applications, such as:

* Facebook (and Messenger.com) Chat
* Twitter Direct Messages
* Skype Web Clients
* Roundcube Email Client
* Outlook Email Client

You may create your own extraction modules for allowing RAMAS to extract communication records from additional applications. We provide the above modules as examples.


Usage
-----

To extract data using RAMAS, change directory to `src/` and execute the tool:

```
$ python ramas.py
```

RAMAS takes as input strings files, obtained from the processing of raw memory images. Strings files can be obtained by running the `strings` utility over raw dumps.

A simple example is depicted below.

```
$ strings RAW_DUMP_FILE > STRINGS_DUMP_FILE
```

To create new modules, please refer to our paper for extraction modules details. You may take inspiration on the modules we have made available in `src/platforms`. Recall that, due to updates on web-applications', modules can become outdated. For the moment, we do not intend in maintaining our example modules up-to-date'.


Authors
-------

@tiagolb
@dmbb
@magicknot

Notes
-----


RAMAS is under the open-source MIT License (https://opensource.org/licenses/MIT).

This tool was tested in a 64-bit Ubuntu 16.04 LTS with python 2.7.12.
