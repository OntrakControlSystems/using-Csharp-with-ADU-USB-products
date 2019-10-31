# Using-Csharp-with-ADU-USB-products

This is a tutorial on communicating with Ontrak USB data acquisition products using C# and the AduHid DLL.

Communicating with USB devices in Visual Studio, or virtually any application software, involves a few simple steps.  Unlike RS232 based devices which are connected to physical COM ports, USB devices are assigned a logical handle by operating systems when they are first plugged in. This process is known as enumeration. Once a USB device has been enumerated, it is ready for use by the host computer software. For the host application software to communicate with the USB device, it must first obtain the handle assigned to the USB device during the enumeration process. The handle can be obtained using an open function along with some specific information about the USB device. Information that can be used to obtain a handle to a USB device include, serial number, product ID, or vendor ID. Once the handle is obtained, it is used to allow the application to read and write information, to and from, the USB device.  Once the application has finished with all communication with the USB device, the handle is closed. The handle is generally closed when the application terminates.
The AduHid DLL provides all the functions to open a handle, read and write data, and close the handle of ADU USB devices. The ADUHID dll can be used directly from a C# application. 
The sample program below is a rendition of our AduHidTest program demonstrating the proper method to utilize the functions within the ADUHID dll to communicate with ADU, USB based data acquisition products. The example also includes use of the functions ADUCount, GetADU and GetAduDeviceList which are new to the ADUHID and ADUHID64 dll's Ver 2.1.

The resulting executable was tested under Windows 7 and 10.  

Standard MIT license - Copyright 2019 Ontrak Control Systems Inc.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
