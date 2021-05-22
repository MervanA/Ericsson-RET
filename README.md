## AMOS|MOSHELL script to create RET Unit on Ericsson BaseBand Nodes

script was written to Standarize RET implementation, verify and minimize user inputs and errors

Script Name: define_RET.mos

make sure netconf files are in the correct PATH

## SYNTAX

```bash
run /PATH/TO/SCRIPT.mos [<SITESECTOR>,<RADIO>,<DIR>,<CONFIGID>][--help][--lookup <ANTENNAID>]
```

Input must be 4 fields seperated by ","

SITESECTOR,RADIO,DIR,CONFIGID

```text
    1)SITESECTOR      :is 6 characters, 5 is siteId and last is Sector indicator
    2)RADIO           :is the Radio unit's ID with rfport=R used to power the RET, if ID provided is not configured on site script will fail.
    3)AZIMUTH/DIR     :can not be more than 3 characters and value d can be used to set default value of "XXX"
    4)CONFIGID        :supported CONFIGID and ANTENNA models are as below >
      #######################
      CONFIGID    ANTENNA-MODEL    VENDOR      xPOL
      1X          ARETU/ARETUV01   KATHREIN    1x
      2A          2LPX0412R        BROADRADIO  2x
      2A          ODDI-032R20J-G   Comba-ODI   2x
      2B          ADU4517R3        HUAWEI      2x
      2C          AMB4520R0        HUAWEI      2x
      2D          AMB4520R8v06     HUAWEI      2x
      3A          ATR4518R4        HUAWEI      3x
      3B          UL2PX506R-C      BROADRADIO  3x
      3B          ULLPX206R-C      BROADRADIO  3x
      3B          ULLPX506R-C      BROADRADIO  3x
      3C          80010727         KATHREIN    3x
      4A          ODI-15E18KJJ-G   Comba-ODI   4x
      4A          15E18K18J18J     Comba-ODI   4x
      4B          AE-7647-0001     ASELSAN     4x
      4B          ODI065R15M18JJJ  Comba-ODI   4x
      4C          UL2PX206.12R-E2  BROADRADIO  4x
      4D          TONGYU           TONGYU      4x
      4E          ODI-65R12M15JJJ  Comba-ODI   4x
      6A          65R15M18JKDKD2   Comba-ODI   6x
      6B          MS-12H180        MatSing     6x
      8B          AOC4518R13v06    HUAWEI      8x
      8C          AMB4519R18v06    HUAWEI      8x
      8D          065R15M18JKD     Comba-ODI   8x
```
