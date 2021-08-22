---
title: Windows Virtual PC Interfaces
description: Las siguientes interfaces son compatibles con Windows Virtual PC.
ms.assetid: de003075-8609-4303-838e-da449b91dc8d
keywords:
- Windows Virtual PC Virtual PC, interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963574a5293a7c48b29096e3dbc563c0f2073c7a697f84a86fa0b5750feeabe9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511765"
---
# <a name="windows-virtual-pc-interfaces"></a>Windows Virtual PC Interfaces

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Las siguientes interfaces son compatibles con Windows Virtual PC.



| Interfaz                                                                             | Descripción                                                                                                       |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**IVMAccountant**](ivmaccountant.md)<br/>                                     | Proporciona acceso a la información relacionada con la contabilidad de una máquina virtual (VM).<br/>                          |
| [**IVMDisplay**](ivmdisplay.md)<br/>                                           | Controla la configuración de visualización de una máquina virtual.<br/>                                                                 |
| [**IVMDVDDrive**](ivmdvddrive.md)<br/>                                         | Controla una unidad de CD-ROM o DVD-ROM dentro de una máquina virtual.<br/>                                                        |
| [**IVMDVDDriveCollection**](ivmdvddrivecollection.md)<br/>                     | Define la colección de unidades de CD y DVD dentro de la máquina virtual.<br/>                                             |
| [**IVMDVDDriveEvents**](ivmdvddriveevents.md)<br/>                             | Define la interfaz de eventos salientes para [**la interfaz IVMDVDDrive.**](ivmdvddrive.md)<br/>             |
| [**IVMFstonepyDrive**](ivmfloppydrive.md)<br/>                                   | Controla una unidad de disquete dentro de una máquina virtual.<br/>                                                                   |
| [**IVMFstonepyDriveCollection**](ivmfloppydrivecollection.md)<br/>               | Define una colección de disquetes dentro de la máquina virtual.<br/>                                                   |
| [**IVMFstonepyDriveEvents**](ivmfloppydriveevents.md)<br/>                       | Define la interfaz de evento saliente para la [**interfaz IVMFstonepyDrive.**](ivmfloppydrive.md)<br/>       |
| [**IVMGuestOS**](ivmguestos.md)<br/>                                           | Define el sistema operativo invitado que se ejecuta dentro de una máquina virtual.<br/>                                                |
| [**IVMHardDisk**](ivmharddisk.md)<br/>                                         | Proporciona acceso a una imagen de disco duro.<br/>                                                                  |
| [**IVMHardDiskConnection**](ivmharddiskconnection.md)<br/>                     | Define la conexión de un disco duro dentro de la máquina virtual.<br/>                                                  |
| [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)<br/> | Define la colección de conexiones de disco duro dentro de la máquina virtual.<br/>                                         |
| [**IVMHostInfo**](ivmhostinfo.md)<br/>                                         | Recupera información sobre el equipo host.<br/>                                                          |
| [**IVMKeyboard**](ivmkeyboard.md)<br/>                                         | Controla el dispositivo de teclado dentro de una máquina virtual.<br/>                                                              |
| [**IVMMouse**](ivmmouse.md)<br/>                                               | Controla el dispositivo del mouse dentro de una máquina virtual.<br/>                                                                 |
| [**IVMNetworkAdapter**](ivmnetworkadapter.md)<br/>                             | Actúa como interfaz para una tarjeta de interfaz de red virtual (NIC) dentro de una máquina virtual.<br/>                         |
| [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md)<br/>         | Define una colección de NIC virtuales dentro de una máquina virtual.<br/>                                                      |
| [**IVMParallelPort**](ivmparallelport.md)<br/>                                 | Define un puerto paralelo dentro de una máquina virtual.<br/>                                                                   |
| [**IVMParallelPortCollection**](ivmparallelportcollection.md)<br/>             | Define la colección de puertos paralelos dentro de la máquina virtual.<br/>                                                |
| [**IVMSerialPort**](ivmserialport.md)<br/>                                     | Define un puerto serie dentro de una máquina virtual.<br/>                                                                     |
| [**IVMSerialPortCollection**](ivmserialportcollection.md)<br/>                 | Define la colección de puertos serie dentro de la máquina virtual.<br/>                                                  |
| [**IVMTask**](ivmtask.md)<br/>                                                 | Se usa para supervisar y controlar tareas asincrónicas para varios métodos.<br/>                                    |
| [**IVMTaskCollection**](ivmtaskcollection.md)<br/>                             | Define la colección de objetos de tarea dentro de una máquina virtual.<br/>                                                    |
| [**IVMUSBDevice**](ivmusbdevice.md)<br/>                                       | Define la interfaz de un dispositivo USB conectado al sistema host.<br/>                                    |
| [**IVMUSBDeviceCollection**](ivmusbdevicecollection.md)<br/>                   | Define la colección de dispositivos USB conectados al sistema host.<br/>                                     |
| [**IVMVirtualMachine**](ivmvirtualmachine.md)<br/>                             | Define la interfaz de una máquina virtual.<br/>                                                                        |
| [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md)<br/>         | Define la colección de máquinas virtuales de Windows Virtual PC.<br/>                                               |
| [**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)<br/>                 | Define la interfaz de evento saliente para [**la interfaz IVMVirtualMachine.**](ivmvirtualmachine.md)<br/> |
| [**IVMVirtualNetwork**](ivmvirtualnetwork.md)<br/>                             | Define una red virtual.<br/>                                                                             |
| [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md)<br/>         | Define una colección de [**objetos IVMVirtualNetwork.**](ivmvirtualnetwork.md)<br/>                        |
| [**IVMVirtualPC**](ivmvirtualpc.md)<br/>                                       | Define el objeto de aplicación de Windows equipo virtual de nivel superior.<br/>                                           |
| [**IVMVirtualPCEvents**](ivmvirtualpcevents.md)<br/>                           | Define la interfaz de eventos saliente para la [**interfaz IVMVirtualPC.**](ivmvirtualpc.md)<br/>           |



 

## <a name="note-for-developers-on-64-bit-windows"></a>Nota para desarrolladores en aplicaciones de 64 bits Windows

En las ediciones de 64 bits de Windows, la biblioteca de tipos para Windows Virtual PC está en un archivo binario de 64 bits (VPC.exe) en el directorio %WinDir% \\ System32. Ese directorio no es visible de forma predeterminada para los procesos de 32 bits; WOW64 asigna todo el acceso al directorio %WinDir% System32 al directorio \\ %WinDir% \\ SysWOW64 de forma predeterminada. Visual Studio es un binario de 32 bits y, por tanto, no puede abrir el archivo en esta ubicación. Para generar un ensamblado de interoperabilidad para Windows Virtual PC, use TlbImp.exe, que viene con Visual Studio y Windows SDK. Para generar *Microsoft.VirtualPC.Interop.dll*, use la siguiente línea de comandos:

**TlbImp.exe /out:** _Microsoft.VirtualPC.Interop.dll_ **/namespace:Microsoft.VirtualPC.Interop %WinDir% \\ System32 \\VPC.exe**

Otras soluciones incluyen copiar VPC.exe en un directorio diferente donde el compilador pueda encontrarlo, o usar la herramienta OleView.exe del SDK de Windows para extraer un archivo .idl de la biblioteca de tipos de VPC.exe.

 

