---
title: Interfaz IVMVirtualPC (VPCCOMInterfaces. h)
description: Define el objeto de aplicación de Windows Virtual PC de nivel superior. Todos los demás objetos de interfaz de Windows Virtual PC se recuperan a través de este objeto.
ms.assetid: 519d3f1b-0a72-4c67-a2d9-124fda6c8b7a
keywords:
- Interfaz IVMVirtualPC Virtual PC
- Interfaz IVMVirtualPC Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMVirtualPC
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d674fd1cbbe6c51881d15f91f0ebfb20f4f6749
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079497"
---
# <a name="ivmvirtualpc-interface"></a>Interfaz IVMVirtualPC

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define el objeto de aplicación de Windows Virtual PC de nivel superior. Todos los demás objetos de interfaz de Windows Virtual PC se recuperan a través de este objeto.

**IVMVirtualPC** puede notificar a los clientes sobre eventos mediante la interfaz de salida de [**IVMVirtualPCEvents**](ivmvirtualpcevents.md) .

## <a name="members"></a>Miembros

La interfaz **IVMVirtualPC** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualPC** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IVMVirtualPC** tiene estos métodos.



| Método                                                                                      | Descripción                                                                                              |
|:--------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**CreateDifferencingVirtualHardDisk**](ivmvirtualpc-createdifferencingvirtualharddisk.md) | Crea un disco duro virtual de diferenciación.<br/>                                                     |
| [**CreateDynamicVirtualHardDisk**](ivmvirtualpc-createdynamicvirtualharddisk.md)           | Crea un disco duro virtual de cambio de tamaño dinámico.<br/>                                             |
| [**CreateFixedVirtualHardDisk**](ivmvirtualpc-createfixedvirtualharddisk.md)               | Crea un disco duro virtual de tamaño fijo.<br/>                                                       |
| [**CreateFloppyDiskImage**](ivmvirtualpc-createfloppydiskimage.md)                         | Crea un archivo de imagen de disquete.<br/>                                                             |
| [**CreateVirtualMachine**](ivmvirtualpc-createvirtualmachine.md)                           | Crea una nueva configuración de máquina virtual y recupera el objeto de máquina virtual.<br/>         |
| [**DeleteVirtualMachine**](ivmvirtualpc-deletevirtualmachine.md)                           | Elimina una configuración de máquina virtual.<br/>                                                      |
| [**FindVirtualMachine**](ivmvirtualpc-findvirtualmachine.md)                               | Recupera un objeto de máquina virtual que coincide con la configuración solicitada.<br/>                  |
| [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md)                               | Recupera un objeto de red virtual que coincide con el nombre solicitado.<br/>                           |
| [**GetConfigurationValue**](ivmvirtualpc-getconfigurationvalue.md)                         | Recupera el valor de la opción de configuración especificada.<br/>                                   |
| [**GetDVDFiles**](ivmvirtualpc-getdvdfiles.md)                                             | Recupera una matriz de archivos de DVD conocidos.<br/>                                                        |
| [**GetFloppyDiskFiles**](ivmvirtualpc-getfloppydiskfiles.md)                               | Recupera una matriz de archivos de disquete virtual conocidos.<br/>                                        |
| [**GetFloppyDiskImageType**](ivmvirtualpc-getfloppydiskimagetype.md)                       | Recupera el tipo de un archivo de imagen de disquete existente.<br/>                                     |
| [**GetHardDisk**](ivmvirtualpc-getharddisk.md)                                             | Recupera un objeto correspondiente a un archivo de imagen de disco existente.<br/>                             |
| [**GetHardDiskFiles**](ivmvirtualpc-getharddiskfiles.md)                                   | Recupera una matriz de archivos de disco duro virtual conocidos.<br/>                                          |
| [**GetVirtualMachineFiles**](ivmvirtualpc-getvirtualmachinefiles.md)                       | Recupera una matriz de archivos de configuración de máquina virtual conocidos.<br/>                              |
| [**RegisterVirtualMachine**](ivmvirtualpc-registervirtualmachine.md)                       | Registra una configuración de máquina virtual existente y recupera el objeto de máquina virtual.<br/> |
| [**RemoveConfigurationValue**](ivmvirtualpc-removeconfigurationvalue.md)                   | Quita el valor de la opción de configuración especificada.<br/>                                     |
| [**SetConfigurationValue**](ivmvirtualpc-setconfigurationvalue.md)                         | Establece el valor de la opción de configuración especificada.<br/>                                        |
| [**UnregisterVirtualMachine**](ivmvirtualpc-unregistervirtualmachine.md)                   | Anula el registro de una configuración de máquina virtual sin eliminar el archivo de configuración.<br/>          |



 

### <a name="properties"></a>Propiedades

La interfaz **IVMVirtualPC** tiene estas propiedades.



| Propiedad                                                                                   | Tipo de acceso           | Descripción                                                                                                                                           |
|:-------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md)<br/>   | Lectura/escritura<br/> | Directorio predeterminado en el que se van a buscar los archivos de configuración de máquina virtual disponibles.<br/>                                                    |
| [**HostInfo**](ivmvirtualpc-hostinfo.md)<br/>                                       | Solo lectura<br/>  | Información sobre el equipo físico.<br/>                                                                                                   |
| [**MaximumFloppyDrivesPerVM**](ivmvirtualpc-maximumfloppydrivespervm.md)<br/>       | Solo lectura<br/>  | Número máximo de unidades de disquete por máquina virtual.<br/>                                                                                   |
| [**MaximumMemoryPerVM**](ivmvirtualpc-maximummemorypervm.md)<br/>                   | Solo lectura<br/>  | Cantidad máxima de memoria física permitida por máquina virtual, en megabytes.<br/>                                                       |
| [**MaximumNetworkAdaptersPerVM**](ivmvirtualpc-maximumnetworkadapterspervm.md)<br/> | Solo lectura<br/>  | El número máximo de interfaces de red por máquina virtual.<br/>                                                                             |
| [**MaximumNumberOfIDEBuses**](ivmvirtualpc-maximumnumberofidebuses.md)<br/>         | Solo lectura<br/>  | Número máximo de buses permitidos para IDE.<br/>                                                                                               |
| [**MaximumParallelPortsPerVM**](ivmvirtualpc-maximumparallelportspervm.md)<br/>     | Solo lectura<br/>  | El número máximo de puertos paralelos por máquina virtual.<br/>                                                                                  |
| [**MaximumSerialPortsPerVM**](ivmvirtualpc-maximumserialportspervm.md)<br/>         | Solo lectura<br/>  | El número máximo de puertos serie por máquina virtual.<br/>                                                                                    |
| [**MinimumMemoryPerVM**](ivmvirtualpc-minimummemorypervm.md)<br/>                   | Solo lectura<br/>  | Cantidad mínima de memoria física permitida por máquina virtual, en megabytes.<br/>                                                       |
| [**Name**](ivmvirtualpc-name.md)<br/>                                               | Solo lectura<br/>  | El nombre de la aplicación Windows Virtual PC.<br/>                                                                                            |
| [**SearchPaths**](ivmvirtualpc-searchpaths.md)<br/>                                 | Lectura/escritura<br/> | Las rutas de acceso del sistema de archivos que se usan para buscar archivos asociados a Windows Virtual PC.<br/>                                                      |
| [**SuggestedMaximumMemoryPerVM**](ivmvirtualpc-suggestedmaximummemorypervm.md)<br/> | Solo lectura<br/>  | La cantidad máxima de memoria física que se sugiere para cada máquina virtual, en megabytes, para evitar las condiciones de memoria insuficiente en el host.<br/> |
| [**Tareas**](ivmvirtualpc-tasks.md)<br/>                                             | Solo lectura<br/>  | Una colección de tareas.<br/>                                                                                                                     |
| [**UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md)<br/>   | Solo lectura<br/>  | Colección enumerable de interfaces de red no conectadas.<br/>                                                                                |
| [**Actividad**](ivmvirtualpc-uptime.md)<br/>                                           | Solo lectura<br/>  | El número de segundos que se ha estado ejecutando la aplicación Windows Virtual PC.<br/>                                                                 |
| [**USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md)<br/>                 | Solo lectura<br/>  | Colección enumerable de todos los dispositivos USB conectados al host.<br/>                                                                         |
| [**Versión**](ivmvirtualpc-version.md)<br/>                                         | Solo lectura<br/>  | La versión de esta instancia de Windows Virtual PC.<br/>                                                                                        |
| [**VirtualMachines**](ivmvirtualpc-virtualmachines.md)<br/>                         | Solo lectura<br/>  | Colección enumerable de máquinas virtuales.<br/>                                                                                              |
| [**VirtualNetworks**](ivmvirtualpc-virtualnetworks.md)<br/>                         | Solo lectura<br/>  | Colección enumerable de redes virtuales.<br/>                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01<br/>               |



 

