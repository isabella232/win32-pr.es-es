---
title: Interfaces de Windows Virtual PC
description: Windows Virtual PC es compatible con las siguientes interfaces.
ms.assetid: de003075-8609-4303-838e-da449b91dc8d
keywords:
- Windows Virtual PC Virtual PC, interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a505fab360214d92b844c282fe12722281770f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695628"
---
# <a name="windows-virtual-pc-interfaces"></a>Interfaces de Windows Virtual PC

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Windows Virtual PC es compatible con las siguientes interfaces.



| Interfaz                                                                             | Descripción                                                                                                       |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**IVMAccountant**](ivmaccountant.md)<br/>                                     | Proporciona acceso a información relacionada con cuentas para una máquina virtual (VM).<br/>                          |
| [**IVMDisplay**](ivmdisplay.md)<br/>                                           | Controla la configuración de pantalla de una máquina virtual.<br/>                                                                 |
| [**IVMDVDDrive**](ivmdvddrive.md)<br/>                                         | Controla una unidad de CD-ROM o DVD-ROM dentro de una máquina virtual.<br/>                                                        |
| [**IVMDVDDriveCollection**](ivmdvddrivecollection.md)<br/>                     | Define la colección de unidades de CD y DVD dentro de la máquina virtual.<br/>                                             |
| [**IVMDVDDriveEvents**](ivmdvddriveevents.md)<br/>                             | Define la interfaz de eventos salientes para la interfaz [**IVMDVDDrive**](ivmdvddrive.md) .<br/>             |
| [**IVMFloppyDrive**](ivmfloppydrive.md)<br/>                                   | Controla una unidad de disquete dentro de una máquina virtual.<br/>                                                                   |
| [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md)<br/>               | Define una colección de unidades de disquete dentro de la máquina virtual.<br/>                                                   |
| [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md)<br/>                       | Define la interfaz de eventos salientes para la interfaz [**IVMFloppyDrive**](ivmfloppydrive.md) .<br/>       |
| [**IVMGuestOS**](ivmguestos.md)<br/>                                           | Define el sistema operativo invitado que se ejecuta dentro de una máquina virtual.<br/>                                                |
| [**IVMHardDisk**](ivmharddisk.md)<br/>                                         | Proporciona acceso a una imagen de disco duro.<br/>                                                                  |
| [**IVMHardDiskConnection**](ivmharddiskconnection.md)<br/>                     | Define la conexión para un disco duro dentro de la máquina virtual.<br/>                                                  |
| [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)<br/> | Define la colección de conexiones de disco duro dentro de la máquina virtual.<br/>                                         |
| [**IVMHostInfo**](ivmhostinfo.md)<br/>                                         | Recupera información sobre el equipo host.<br/>                                                          |
| [**IVMKeyboard**](ivmkeyboard.md)<br/>                                         | Controla el dispositivo de teclado dentro de una máquina virtual.<br/>                                                              |
| [**IVMMouse**](ivmmouse.md)<br/>                                               | Controla el dispositivo de mouse dentro de una máquina virtual.<br/>                                                                 |
| [**IVMNetworkAdapter**](ivmnetworkadapter.md)<br/>                             | Actúa como la interfaz de una tarjeta de interfaz de red virtual (NIC) dentro de una máquina virtual.<br/>                         |
| [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md)<br/>         | Define una colección de NIC virtuales dentro de una máquina virtual.<br/>                                                      |
| [**IVMParallelPort**](ivmparallelport.md)<br/>                                 | Define un puerto paralelo dentro de una máquina virtual.<br/>                                                                   |
| [**IVMParallelPortCollection**](ivmparallelportcollection.md)<br/>             | Define la colección de puertos paralelos dentro de la máquina virtual.<br/>                                                |
| [**IVMSerialPort**](ivmserialport.md)<br/>                                     | Define un puerto serie dentro de una máquina virtual.<br/>                                                                     |
| [**IVMSerialPortCollection**](ivmserialportcollection.md)<br/>                 | Define la colección de puertos serie dentro de la máquina virtual.<br/>                                                  |
| [**IVMTask**](ivmtask.md)<br/>                                                 | Se usa para supervisar y controlar tareas asincrónicas para varios métodos.<br/>                                    |
| [**IVMTaskCollection**](ivmtaskcollection.md)<br/>                             | Define la colección de objetos de tarea dentro de una máquina virtual.<br/>                                                    |
| [**IVMUSBDevice**](ivmusbdevice.md)<br/>                                       | Define la interfaz para un dispositivo USB conectado al sistema host.<br/>                                    |
| [**IVMUSBDeviceCollection**](ivmusbdevicecollection.md)<br/>                   | Define la colección de dispositivos USB conectados al sistema host.<br/>                                     |
| [**IVMVirtualMachine**](ivmvirtualmachine.md)<br/>                             | Define la interfaz para una máquina virtual.<br/>                                                                        |
| [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md)<br/>         | Define la colección de máquinas virtuales dentro de Windows Virtual PC.<br/>                                               |
| [**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)<br/>                 | Define la interfaz de eventos salientes para la interfaz [**IVMVirtualMachine**](ivmvirtualmachine.md) .<br/> |
| [**IVMVirtualNetwork**](ivmvirtualnetwork.md)<br/>                             | Define una red virtual.<br/>                                                                             |
| [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md)<br/>         | Define una colección de objetos [**IVMVirtualNetwork**](ivmvirtualnetwork.md) .<br/>                        |
| [**IVMVirtualPC**](ivmvirtualpc.md)<br/>                                       | Define el objeto de aplicación de Windows Virtual PC de nivel superior.<br/>                                           |
| [**IVMVirtualPCEvents**](ivmvirtualpcevents.md)<br/>                           | Define la interfaz de eventos salientes para la interfaz [**IVMVirtualPC**](ivmvirtualpc.md) .<br/>           |



 

## <a name="note-for-developers-on-64-bit-windows"></a>Nota para desarrolladores en Windows de 64 bits

En las ediciones de 64 bits de Windows, la biblioteca de tipos para Windows Virtual PC se encuentra en un archivo binario de 64 bits (VPC.exe) en el directorio% WinDir% \\ system32. Dicho directorio no es visible de forma predeterminada en los procesos de 32 bits; WOW64 asigna todo acceso al directorio% WinDir% \\ system32 al directorio% WINDIR% \\ SysWOW64 de forma predeterminada. Visual Studio es un binario de 32 bits y, por lo tanto, no puede abrir el archivo en esta ubicación. Para generar un ensamblado de interoperabilidad para Windows Virtual PC, use TlbImp.exe, que incluye Visual Studio y el Windows SDK. Para generar *Microsoft.VirtualPC.Interop.dll*, utilice la siguiente línea de comandos:

**TlbImp.exe/out: * * * Microsoft.VirtualPC.Interop.dll* **/namespace: Microsoft. VirtualPC. Interop% WinDir% \\ system32 \\VPC.exe**

Otras soluciones incluyen copiar VPC.exe en un directorio diferente donde el compilador puede encontrarlo, o usar la herramienta de OleView.exe de la Windows SDK para extraer un archivo. idl de la biblioteca de tipos en VPC.exe.

 

