---
title: Interfaz IVMDVDDrive (VPCCOMInterfaces. h)
description: Controla una unidad de CD-ROM o DVD-ROM dentro de una máquina virtual. IVMDVDDrive puede notificar a los clientes sobre eventos mediante la interfaz de salida de IVMDVDDriveEvents.
ms.assetid: 0900b3a8-ba52-4c26-bd96-b37334d6d03c
keywords:
- Interfaz IVMDVDDrive Virtual PC
- Interfaz IVMDVDDrive Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMDVDDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 951213923f74f8425fc4d9eaec85e76f7481eeb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079508"
---
# <a name="ivmdvddrive-interface"></a>Interfaz IVMDVDDrive

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Controla una unidad de CD-ROM o DVD-ROM dentro de una máquina virtual. **IVMDVDDrive** puede notificar a los clientes sobre eventos mediante la interfaz de salida de [**IVMDVDDriveEvents**](ivmdvddriveevents.md) .

Puede Agregar una nueva unidad de CD-ROM o DVD-ROM a una máquina virtual mediante el método [**IVMVirtualMachine:: AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md) . Puede quitar una unidad de CD-ROM o DVD-ROM existente de una máquina virtual mediante el método [**IVMVirtualMachine:: RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md) . Puede recuperar un objeto **IVMDVDDrive** del objeto [**IVMDVDDriveCollection**](ivmdvddrivecollection.md) devuelto desde la propiedad [**IVMVirtualMachine::D vdromdrives**](ivmvirtualmachine-dvdromdrives.md) .

## <a name="members"></a>Miembros

La interfaz **IVMDVDDrive** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMDVDDrive** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IVMDVDDrive** tiene estos métodos.



| Método                                                   | Descripción                                                                             |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**AttachHostDrive**](ivmdvddrive-attachhostdrive.md)   | Conecta una unidad host a la unidad de DVD de la máquina virtual.<br/>           |
| [**AttachImage**](ivmdvddrive-attachimage.md)           | Adjunta una imagen ISO a la unidad de DVD de la máquina virtual.<br/>           |
| [**ReleaseHostDrive**](ivmdvddrive-releasehostdrive.md) | Libera una unidad de host capturada de la unidad de DVD.<br/>                           |
| [**ReleaseImage**](ivmdvddrive-releaseimage.md)         | Libera una imagen ISO capturada de la unidad de DVD.<br/>                            |
| [**SetBusLocation**](ivmdvddrive-setbuslocation.md)     | Conecta la unidad de DVD a la ubicación de bus especificada en la máquina virtual.<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **IVMDVDDrive** tiene estas propiedades.



| Propiedad                                                          | Tipo de acceso          | Descripción                                                                        |
|:------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [**Datos adjuntos**](ivmdvddrive-attachment.md)<br/>           | Solo lectura<br/> | El tipo de medio conectado a la unidad de DVD de la máquina virtual.<br/> |
| [**BusNumber**](ivmdvddrive-busnumber.md)<br/>             | Solo lectura<br/> | Número de bus al que está conectado este dispositivo.<br/>                        |
| [**DeviceNumber**](ivmdvddrive-devicenumber.md)<br/>       | Solo lectura<br/> | El número de dispositivo al que está conectada esta unidad.<br/>                      |
| [**HostDriveLetter**](ivmdvddrive-hostdriveletter.md)<br/> | Solo lectura<br/> | La letra de la unidad de host establecida para este dispositivo.<br/>                       |
| [**ImageFile**](ivmdvddrive-imagefile.md)<br/>             | Solo lectura<br/> | Ruta de acceso completa del archivo de imagen establecido para este dispositivo.<br/>                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive se define como b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



 

