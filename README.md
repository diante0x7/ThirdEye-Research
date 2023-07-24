# ThirdEye-Research
Malware anti-analysis tools, techinques and documentation from the development of ThirdEye.
## Tools
### vm_detect
***VM_DETECT*** is a 2-part detection tool that initially checks the **cpuid** hypervisor (HV) presence bit. If that test passes, it is impossible that the host is a virtualized machine. If it fails, the tool queries the vendor ID within the hypervisor port and compares it against an array of known vendors. If both tests fail conclusively, a virtual machine is present.
### tsc_test
***TSC_TEST*** is a timing attack that tests the Time Stamp Counter (TSC) for any latency inconsistencies or delays. On a normal host system, the TSC is usually low. Through virtualization, however, the time is often hundreds of milliseconds slower or has a significant variance betweem values.
### nop_timing_attack
***NOP_TIMING_ATTACK*** is another timing attack that leverages low-latency instructions for inconsistencies in timing or cycles through repetition. This is the most conclusive form of virtualization detection as it directly challenges the hardware and has the most complex assembly.
### debug_trace_detection
***DEBUG_TRACE_DETECTION*** (DTD) is a tool that takes advantage of ptrace to detect the presence of any debugging/tracing tool's attach method. If the test fails, it indicates a tool such as gdb or radare2 is present, stops the traced process, and kills the program. DTD has the ability to stop debuggers from attaching during execution as well.
## Presentation
A PowerPoint (.pptx) presentation is also included that highlights the goals, thoughts and research that drove the project to completion. It is intended to be presented, so all of the contents are shortened to allow room for the speaker to develop and teach the strategies to their listener.
## Credits
Developed by Diante Jackson, on behalf of the Rolan Group. This project is dedicated to the CougarCS Infosec team at the University of Houston.
