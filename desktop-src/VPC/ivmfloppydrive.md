---
title: Interfaz IVMFloppyDrive (VPCCOMInterfaces. h)
description: Controla una unidad de disquete dentro de una máquina virtual.
ms.assetid: b652182a-27ae-4390-81b1-b644a82924df
keywords:
- Interfaz IVMFloppyDrive Virtual PC
- Interfaz IVMFloppyDrive Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMFloppyDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab1034bc56c5fe10bb12941bd99309e13e22dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996945"
---
# <a name="ivmfloppydrive-interface"></a>Interfaz IVMFloppyDrive

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Controla una unidad de disquete dentro de una máquina virtual. **IVMFloppyDrive** puede notificar a los clientes sobre eventos mediante la interfaz de salida de [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md) . Puede recuperar un objeto **IVMFloppyDrive** del objeto [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md) devuelto desde la propiedad [**IVMVirtualMachine:: FloppyDrives**](ivmvirtualmachine-floppydrives.md) .

## <a name="members"></a>Miembros

La interfaz **IVMFloppyDrive** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMFloppyDrive** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IVMFloppyDrive** tiene estos métodos.



| Método                                                      | Descripción                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**AttachHostDrive**](ivmfloppydrive-attachhostdrive.md)   | Conecta una unidad física del host a la unidad de disquete en la máquina virtual.<br/> |
| [**AttachImage**](ivmfloppydrive-attachimage.md)           | Adjunta una imagen de disquete en el host a la unidad de disquete.<br/>                    |
| [**ReleaseHostDrive**](ivmfloppydrive-releasehostdrive.md) | Libera una unidad física del host de la unidad de disquete.<br/>                      |
| [**ReleaseImage**](ivmfloppydrive-releaseimage.md)         | Libera una imagen de disquete en el host de la unidad de disquete.<br/>                  |



 

### <a name="properties"></a>Propiedades

La interfaz **IVMFloppyDrive** tiene estas propiedades.



| Propiedad                                                             | Tipo de acceso          | Descripción                                                                               |
|:---------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [**Datos adjuntos**](ivmfloppydrive-attachment.md)<br/>           | Solo lectura<br/> | El tipo de medio conectado a la unidad de disquete en la máquina virtual.<br/>     |
| [**DriveNumber**](ivmfloppydrive-drivenumber.md)<br/>         | Solo lectura<br/> | Índice de base cero del controlador al que está conectada esta unidad de disquete.<br/> |
| [**HostDriveLetter**](ivmfloppydrive-hostdriveletter.md)<br/> | Solo lectura<br/> | La letra de la unidad host a la que está conectada la unidad de disquete.<br/>            |
| [**ImageFile**](ivmfloppydrive-imagefile.md)<br/>             | Solo lectura<br/> | La ruta de acceso completa del archivo de imagen al que está conectada la unidad de disquete.<br/>         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDrive se define como 661abee6-112a-4ed9-babf-3c874969f10e<br/>             |



 

