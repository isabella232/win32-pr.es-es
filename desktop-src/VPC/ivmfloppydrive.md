---
title: Interfaz IVMFstonepyDrive (VPCCOMInterfaces.h)
description: Controla una unidad de disquete dentro de una máquina virtual.
ms.assetid: b652182a-27ae-4390-81b1-b644a82924df
keywords:
- IVMFstonepyDrive interface Virtual PC
- IVMFstonepyDrive interface Virtual PC , descrito
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
ms.openlocfilehash: 63db224861b547b9485b03080ce3ffb3f5c118ef0de71597db79aa0888a1528d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594811"
---
# <a name="ivmfloppydrive-interface"></a>Interfaz IVMFstonepyDrive

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Controla una unidad de disquete dentro de una máquina virtual. **IVMFstonepyDrive puede notificar** a los clientes sobre eventos mediante la interfaz saliente [**IVMFstonepyDriveEvents.**](ivmfloppydriveevents.md) Puede recuperar un **objeto IVMFstonepyDrive** del objeto [**IVMFstonepyDriveCollection**](ivmfloppydrivecollection.md) devuelto desde la [**propiedad IVMVirtualMachine::FloppyDrives.**](ivmvirtualmachine-floppydrives.md)

## <a name="members"></a>Miembros

La **interfaz IVMFstonepyDrive** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMFstonepyDrive también** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IVMFstonepyDrive tiene** estos métodos.



| Método                                                      | Descripción                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**AttachHostDrive**](ivmfloppydrive-attachhostdrive.md)   | Conecta una unidad física del host a la unidad de disquete de la máquina virtual.<br/> |
| [**AttachImage**](ivmfloppydrive-attachimage.md)           | Adjunta una imagen de disquete en el host a la unidad de disquete.<br/>                    |
| [**ReleaseHostDrive**](ivmfloppydrive-releasehostdrive.md) | Libera una unidad física en el host desde la unidad de disquete.<br/>                      |
| [**ReleaseImage**](ivmfloppydrive-releaseimage.md)         | Libera una imagen de disquete en el host desde la unidad de disquete.<br/>                  |



 

### <a name="properties"></a>Propiedades

La **interfaz IVMFstonepyDrive** tiene estas propiedades.



| Propiedad                                                             | Tipo de acceso          | Descripción                                                                               |
|:---------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [**archivo adjunto**](ivmfloppydrive-attachment.md)<br/>           | Solo lectura<br/> | Tipo de medio conectado a la unidad de disquete dentro de la máquina virtual.<br/>     |
| [**DriveNumber**](ivmfloppydrive-drivenumber.md)<br/>         | Solo lectura<br/> | Índice de base cero del controlador al que está conectada esta unidad de disquete.<br/> |
| [**HostDriveLetter**](ivmfloppydrive-hostdriveletter.md)<br/> | Solo lectura<br/> | Letra de la unidad host a la que está conectada la unidad de disquete.<br/>            |
| [**ImageFile**](ivmfloppydrive-imagefile.md)<br/>             | Solo lectura<br/> | Ruta de acceso completa del archivo de imagen al que está conectada la unidad de disquete.<br/>         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMFstonepyDrive se define como \_ 661abee6-112a-4ed9-bamf-3c874969f10e<br/>             |



 

