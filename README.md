# CBT690
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 690 is from Martin Kline, and contains a cross memory     *   FILE 690
//*           storage browser called XMDSMAIN or MINDRDR.           *   FILE 690
//*                                                                 *   FILE 690
//*           email:  martin_kline@americancentury.com              *   FILE 690
//*                                                                 *   FILE 690
//*     This is the documentation for the cross-memory browser      *   FILE 690
//*     (originally called MINDRDR) from Martin Kline.              *   FILE 690
//*                                                                 *   FILE 690
//*     The source originated in the mid 1980's, so it could        *   FILE 690
//*     possibly use some updates. It was written as a tool to      *   FILE 690
//*     help in the design and implementation of several major      *   FILE 690
//*     applications, including a replacement for TCAM TSO          *   FILE 690
//*     (without VTAM), and a complete report management            *   FILE 690
//*     subsystem.                                                  *   FILE 690
//*                                                                 *   FILE 690
//*     The tool allows a user to browse through any address        *   FILE 690
//*     space from the convenience of their own TSO session.        *   FILE 690
//*     Obviously, this has some security risks, and should         *   FILE 690
//*     only be used by responsible persons. When it was first      *   FILE 690
//*     written, several major security holes were found,           *   FILE 690
//*     including the availability of passwords in various          *   FILE 690
//*     control blocks.  Most of those security holes have          *   FILE 690
//*     since been fixed.                                           *   FILE 690
//*                                                                 *   FILE 690
//*     The XMDSMAIN program checks the logon proc name to see      *   FILE 690
//*     if the user should be allowed to run the program. If        *   FILE 690
//*     not, it simply exits.                                       *   FILE 690
//*                                                                 *   FILE 690
//*     Installation:                                               *   FILE 690
//*                                                                 *   FILE 690
//*     All of the source, JCL and macro members are contained      *   FILE 690
//*     in this PDS.  Determine which load library is to receive    *   FILE 690
//*     the XMDSMAIN module.  Member $$ASM is the JCL to            *   FILE 690
//*     assemble the source members and to build an authorized      *   FILE 690
//*     load module. Add a job card. Change the input and output    *   FILE 690
//*     datasets, and run it.                                       *   FILE 690
//*                                                                 *   FILE 690
//*     Move the resulting load module to an authorized linklist    *   FILE 690
//*     library.  (You really didn't think you could do this        *   FILE 690
//*     without some sort of authorization, did you?)  If you       *   FILE 690
//*     prefer to use a user SVC to change the APF authorization    *   FILE 690
//*     dynamically, then find all of the @AUTH macro references    *   FILE 690
//*     in the source, and change them to call your SVC.            *   FILE 690
//*                                                                 *   FILE 690
//*     Add the XMDSMAIN program to the IKJTSOxx member of          *   FILE 690
//*     SYS1.PARMLIB as an authorized command.                      *   FILE 690
//*                                                                 *   FILE 690
//*     Usage:                                                      *   FILE 690
//*                                                                 *   FILE 690
//*     Invoke the program from anywhere in TSO/ISPF. ISPF is       *   FILE 690
//*     not required.                                               *   FILE 690
//*                                                                 *   FILE 690
//*     Assigned keys are:                                          *   FILE 690
//*                                                                 *   FILE 690
//*       PF1  - Help                                               *   FILE 690
//*       PF3  - End                                                *   FILE 690
//*       PF5  - Repeat find                                        *   FILE 690
//*       PF7  - Scroll backward                                    *   FILE 690
//*       PF8  - Scroll foreward                                    *   FILE 690
//*       PF11 - Pick up address from cursor and show that          *   FILE 690
//*              storage                                            *   FILE 690
//*                                                                 *   FILE 690
//*       FIND command - FIND or F  'string' or x'string'           *   FILE 690
//*                      Searches up to 16 meg of storage           *   FILE 690
//*                      Can take a long time if storage not        *   FILE 690
//*                      allocated.                                 *   FILE 690
//*                                                                 *   FILE 690
//*       LOCATE command - LOCATE or L   block-name                 *   FILE 690
//*                        Locates and displays various control     *   FILE 690
//*                        blocks.                                  *   FILE 690
//*                        Use PF1 to see a list of supported       *   FILE 690
//*                        blocks.                                  *   FILE 690
//*                                                                 *   FILE 690
//*     Fields:                                                     *   FILE 690
//*                                                                 *   FILE 690
//*       ADDRESS   - Current address. Overtype to show a           *   FILE 690
//*                   specific location                             *   FILE 690
//*       MODE      - Addressing mode. D = 24-bit mode,             *   FILE 690
//*                   X = 31-bit mode                               *   FILE 690
//*       ASID      - Decimal ASID of displayed address space.      *   FILE 690
//*                   Overtype to change ASIDs                      *   FILE 690
//*       JOBNAME   - Job name of displayed address space.          *   FILE 690
//*                   Overtype to change.                           *   FILE 690
//*                                                                 *   FILE 690
//*     Displayed storage cannot be altered. Use TAB key to         *   FILE 690
//*     move to a field before pressing PF11 to link to that        *   FILE 690
//*     address.                                                    *   FILE 690
//*                                                                 *   FILE 690
```
