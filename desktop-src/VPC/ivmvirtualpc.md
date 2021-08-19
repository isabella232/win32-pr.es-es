---
title: Interfaz IVMVirtualPC (VPCCOMInterfaces.h)
description: Define el objeto de aplicación de Windows de equipo virtual de nivel superior. Todos los demás Windows interfaz de pc virtual se recuperan a través de este objeto.
ms.assetid: 519d3f1b-0a72-4c67-a2d9-124fda6c8b7a
keywords:
- IVMVirtualPC interface Virtual PC
- IVMVirtualPC interface Virtual PC , descrito
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
ms.openlocfilehash: 69dd5eec832e95b2b93ff0fb0bee026428a937fa277f86ff14ef672bc66e0dd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124661"
---
# <a name="ivmvirtualpc-interface"></a>Interfaz IVMVirtualPC

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Define el objeto de aplicación de Windows de equipo virtual de nivel superior. Todos los demás Windows interfaz de pc virtual se recuperan a través de este objeto.

**IVMVirtualPC puede** notificar a los clientes sobre eventos mediante la interfaz saliente [**IVMVirtualPCEvents.**](ivmvirtualpcevents.md)

## <a name="members"></a>Miembros

La **interfaz IVMVirtualPC** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMVirtualPC** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IVMVirtualPC** tiene estos métodos.



| Método                                                                                      | Descripción                                                                                              |
|:--------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**CreateDifferencingVirtualHardDisk**](ivmvirtualpc-createdifferencingvirtualharddisk.md) | Crea un disco duro virtual de diferenciación.<br/>                                                     |
| [**CreateDynamicVirtualHardDisk**](ivmvirtualpc-createdynamicvirtualharddisk.md)           | Crea un disco duro virtual que cambia de tamaño dinámicamente.<br/>                                             |
| [**CreateFixedVirtualHardDisk**](ivmvirtualpc-createfixedvirtualharddisk.md)               | Crea un disco duro virtual de tamaño fijo.<br/>                                                       |
| [**CreateFstonepyDiskImage**](ivmvirtualpc-createfloppydiskimage.md)                         | Crea un archivo de imagen de disquete.<br/>                                                             |
| [**CreateVirtualMachine**](ivmvirtualpc-createvirtualmachine.md)                           | Crea una nueva configuración de máquina virtual y recupera el objeto de máquina virtual.<br/>         |
| [**DeleteVirtualMachine**](ivmvirtualpc-deletevirtualmachine.md)                           | Elimina una configuración de máquina virtual.<br/>                                                      |
| [**FindVirtualMachine**](ivmvirtualpc-findvirtualmachine.md)                               | Recupera un objeto de máquina virtual que coincide con la configuración solicitada.<br/>                  |
| [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md)                               | Recupera un objeto de red virtual que coincide con el nombre solicitado.<br/>                           |
| [**GetConfigurationValue**](ivmvirtualpc-getconfigurationvalue.md)                         | Recupera el valor de la opción de configuración especificada.<br/>                                   |
| [**GetDVDFiles**](ivmvirtualpc-getdvdfiles.md)                                             | Recupera una matriz de archivos DVD conocidos.<br/>                                                        |
| [**GetFstonepyDiskFiles**](ivmvirtualpc-getfloppydiskfiles.md)                               | Recupera una matriz de archivos de disquete virtuales conocidos.<br/>                                        |
| [**GetFstonepyDiskImageType**](ivmvirtualpc-getfloppydiskimagetype.md)                       | Recupera el tipo de un archivo de imagen de disquete existente.<br/>                                     |
| [**GetHardDisk**](ivmvirtualpc-getharddisk.md)                                             | Recupera un objeto correspondiente a un archivo de imagen de disco existente.<br/>                             |
| [**GetHardDiskFiles**](ivmvirtualpc-getharddiskfiles.md)                                   | Recupera una matriz de archivos de disco duro virtual conocidos.<br/>                                          |
| [**GetVirtualMachineFiles**](ivmvirtualpc-getvirtualmachinefiles.md)                       | Recupera una matriz de archivos de configuración de máquina virtual conocidos.<br/>                              |
| [**RegisterVirtualMachine**](ivmvirtualpc-registervirtualmachine.md)                       | Registra una configuración de máquina virtual existente y recupera el objeto de máquina virtual.<br/> |
| [**RemoveConfigurationValue**](ivmvirtualpc-removeconfigurationvalue.md)                   | Quita el valor de la configuración especificada.<br/>                                     |
| [**SetConfigurationValue**](ivmvirtualpc-setconfigurationvalue.md)                         | Establece el valor de la configuración especificada.<br/>                                        |
| [**UnregisterVirtualMachine**](ivmvirtualpc-unregistervirtualmachine.md)                   | Anula el registro de una configuración de máquina virtual sin eliminar el archivo de configuración.<br/>          |



 

### <a name="properties"></a>Propiedades

La **interfaz IVMVirtualPC** tiene estas propiedades.



| Propiedad                                                                                   | Tipo de acceso           | Descripción                                                                                                                                           |
|:-------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md)<br/>   | Lectura/escritura<br/> | Directorio predeterminado en el que se buscarán los archivos de configuración de máquina virtual disponibles.<br/>                                                    |
| [**HostInfo**](ivmvirtualpc-hostinfo.md)<br/>                                       | Solo lectura<br/>  | Información sobre el equipo físico.<br/>                                                                                                   |
| [**MaximumFstonepyDrivesPerVM**](ivmvirtualpc-maximumfloppydrivespervm.md)<br/>       | Solo lectura<br/>  | Número máximo de unidades de disquete por máquina virtual.<br/>                                                                                   |
| [**MaximumMemoryPerVM**](ivmvirtualpc-maximummemorypervm.md)<br/>                   | Solo lectura<br/>  | Cantidad máxima de memoria física por máquina virtual, en megabytes.<br/>                                                       |
| [**MaximumNetworkAdaptersPerVM**](ivmvirtualpc-maximumnetworkadapterspervm.md)<br/> | Solo lectura<br/>  | Número máximo de interfaces de redes por máquina virtual.<br/>                                                                             |
| [**MaximumNumberOfIDEBuses**](ivmvirtualpc-maximumnumberofidebuses.md)<br/>         | Solo lectura<br/>  | Número máximo de bus permitido para el IDE.<br/>                                                                                               |
| [**MaximumParallelPortsPerVM**](ivmvirtualpc-maximumparallelportspervm.md)<br/>     | Solo lectura<br/>  | Número máximo de puertos paralelos por máquina virtual.<br/>                                                                                  |
| [**MaximumSerialPortsPerVM**](ivmvirtualpc-maximumserialportspervm.md)<br/>         | Solo lectura<br/>  | Número máximo de puertos serie por máquina virtual.<br/>                                                                                    |
| [**MinimumMemoryPerVM**](ivmvirtualpc-minimummemorypervm.md)<br/>                   | Solo lectura<br/>  | Cantidad mínima de memoria física por máquina virtual, en megabytes.<br/>                                                       |
| [**Nombre**](ivmvirtualpc-name.md)<br/>                                               | Solo lectura<br/>  | Nombre de la aplicación Windows Virtual PC.<br/>                                                                                            |
| [**SearchPaths**](ivmvirtualpc-searchpaths.md)<br/>                                 | Lectura/escritura<br/> | Rutas de acceso del sistema de archivos que se usan para buscar archivos asociados a Windows Virtual PC.<br/>                                                      |
| [**SuggestedMaximumMemoryPerVM**](ivmvirtualpc-suggestedmaximummemorypervm.md)<br/> | Solo lectura<br/>  | Cantidad máxima de memoria física sugerida por máquina virtual, en megabytes, para evitar condiciones de memoria baja en el host.<br/> |
| [**Tareas**](ivmvirtualpc-tasks.md)<br/>                                             | Solo lectura<br/>  | Colección de tareas.<br/>                                                                                                                     |
| [**UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md)<br/>   | Solo lectura<br/>  | Colección enumerable de interfaces de red no conectadas.<br/>                                                                                |
| [**Uptime**](ivmvirtualpc-uptime.md)<br/>                                           | Solo lectura<br/>  | Número de segundos que ha estado Windows aplicación virtual de PC.<br/>                                                                 |
| [**USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md)<br/>                 | Solo lectura<br/>  | Colección enumerable de todos los dispositivos USB conectados al host.<br/>                                                                         |
| [**Versión**](ivmvirtualpc-version.md)<br/>                                         | Solo lectura<br/>  | La versión de esta instancia de Windows Virtual PC.<br/>                                                                                        |
| [**VirtualMachines**](ivmvirtualpc-virtualmachines.md)<br/>                         | Solo lectura<br/>  | Colección enumerable de máquinas virtuales.<br/>                                                                                              |
| [**VirtualNetworks**](ivmvirtualpc-virtualnetworks.md)<br/>                         | Solo lectura<br/>  | Colección enumerable de redes virtuales.<br/>                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC se define como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



 

