(c) Lenze GmbH & Co KG Aerzen,   1996
    Postfach  101352
    D-31763 Hameln
    Tel.  (05154) 82-0
    Fax.  (05154) 4040


LEMOC2   Parameter setting on PC
Version: 3.4

This software can be used to parameter set and operate
LENZE controllers and automation modules.

--------------------------------------------------------------------------

CAUTION

The user is offered the software in the present form. All risks concerning
quality and results from its use remains in the responsibility of the user.
Measures protecting against any malfunctions must be provided by the user.

We do not take any responsibility for direct or consequential damage,
e.g. profit losses, order losses or commercial problems of any kind.
--------------------------------------------------------------------------

SYSTEM REQUIREMENTS:

  Hardware:   IBM-AT or compatible PC  ( CPU: 80286 or higher )
              at least 560 kByte RAM
              Hard disk with approx. 5 MByte free memory
              Disk drive 3,5"

  Software:   MS-DOS version higher than 3.3

--------------------------------------------------------------------------

PROGRAMM START:

   After the installation and entry into the directory of LEMOC2 in the 
   path of the AUTOEXEC.BAT, LEMOC2 can be started as follows:

        lm2 [options]

   If you do not enter the directory of LEMOC2 into your path,
   start the program as follows:

        c:\lemoc2\bin\lm2 [options]

   Without options, LEMOC2 is started in the high-resolution graphic mode.
   If the file EGAVGA.BGI is not found during the program start, a lower
   graphic resolution is selected.

   Options during program start:

     /?           The possible options of LEMOC2 are displayed
     /t           LEMOC2 is started in the text mode. Normally, the
                  program recognizes automatically the possible screen
                  mode. If this is not the case, LEMOC2 can be switched 
                  directly to the text mode.

     /m           LEMOC2 is started in the monochrome display

     /ega         The program is started in the the EGA mode.
                  When using a PC with an EGA graphic card, the size of the
                  window may cause problems. By setting this option, the
                  screens are adapted.

     /vga         The program is started in the VGA mode. This VGA mode is
                  preset. After finding the driver egavga.bgi, the program
                  automatically installs the highest possible graphic 
                  resolution.

     /lcd         Display on LCD screens

     /max         Very large controller descriptions (e.g. 2210 module) 
                  require an extension of the memory structures in the
                  program. For this, LEMOC2 must be started once with the
                  extensions /max. For all other starts, the maximum
                  memory configuration is read from the configuration file
                  lm2conf.cnf. If you select the option /max, you require
                  at least 560 kByte free memory in the conventional area.

     /min         This option can be used to cancel the settings of /max.
                  For this, start LEMOC2 once with this option. For all 
                  other starts, LEMOC2 uses a standard setting for the size
                  of the working storage. Normally, LEMOC2 requires at least
                  520 kByte free memory in the convential area. With the
                  standard configuration you can use all controller descrip-
                  tions for devices without automation module.

     /pdb         The indicated controller description is automatically loaded
                  when starting LEMOC2.

     /var         The indicated parameter set file is automatically loaded 
                  when starting LEMOC2. Directory and file name of the parameter
                  set file must be indicated.

     Several options can be used; they must be separated using a blank.
     The program options are saved in the configuration file LM2CONF.CNF.
     For other program starts, the options are not required.

--------------------------------------------------------------------------

DIRECTORY STRUCTURE of LEMOC2:

   The different files of LEMOC2 are organized in different
   directories. This structure must not be changed.

   \lemoc2  ----+--- \bin
                |
                +--- \pdb  --+-- 049
                |            +-- 033
                |            +-- 044
                |            |
                |
                +--- \data

    Content of the directories:

    \bin         Program file lm2.exe
                 Configuration files for LEMOC2

    \pdb\....    Directory for the controller descriptions required
                 by LEMOC2. The extension for these files is
                 always *.pdb.
                 The controller descriptions are available in 
                 several languages. Therefore the files are classified
                 according to the languages and are stored in indi-
                 vidual subdirectories. The identification for the
                 languages is identical with the language identifica-
                 tion as it is used in MS-DOS.

                 Example:     049   German
                              033   French
                              044   English

    \data        This directory contains the files with the parameter
                 sets determined by the user. These files have always
                 the extension *.var.

--------------------------------------------------------------------------

SERIAL CONNECTION between PC and drive:

   PC and drive and connected by a cable with the following 
   configuration:

     Lenze drive                                      PC
     9-pole SubD plug                       25-pole SubD socket

           PIN                                         PIN
            2  o-------------------------------------o  2
            3  o-------------------------------------o  3
            5  o-------------------------------------o  7
            6  o-------------------------------------o  6


     Lenze drive                                      PC
     9-pole SubD plug                        9-pole SubD socket

           PIN                                         PIN
            2  o-------------------------------------o  3
            3  o-------------------------------------o  2
            5  o-------------------------------------o  5


  All connections which are not shown are not assigned. Further
  information can be obtained from the Operating Instructions
  LECOM-A/B.

--------------------------------------------------------------------------

FAULTS WHEN LOADING A CONTROLLER DESCRIPTION

  For very large controller descriptions, the memory capacity which
  is normally reserved by LEMOC2 is not sufficient. When you load
  such a description, an error message is displayed which indicates 
  that a part of the controller description cannot be loaded, because
  there is not enough memory. This only occurs with controller
  descriptions, which contain the parameters of a base controller and
  an automation module.

  The memory reserved by LEMOC2 can be extended when the program is started
  once with the option /max. For all later program starts, the maximum 
  memory configuration is read from the configuration file lm2conf.cnf.

--------------------------------------------------------------------------

SERVICE:

  In case of technical problems when using LEMOC2 please address yourself
  to your Lenze representative or to:

  Lenze GmbH & CoKG Aerzen
  Postfach  101352
  D - 31763 Hameln
  Tel. (05154) 82-0
  Fax. (05154) 4040

--------------------------------------------------------------------------
