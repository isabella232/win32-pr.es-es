---
title: Interfaz IVMHardDisk (VPCCOMInterfaces.h)
description: Proporciona acceso a una imagen de disco duro. Se puede acceder a él a través de la propiedad HardDisk IVMHardDiskConnection o el método IVMVirtualPC GetHardDisk.
ms.assetid: 0c536906-91be-428a-8199-c452abef423d
keywords:
- IVMHardDisk interface Virtual PC
- IVMHardDisk interface Virtual PC , descrito
topic_type:
- apiref
api_name:
- IVMHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525762f66798b95562958fb204119beda1d76a8b94a60a11a7171b0d0b2951e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768165"
---
# <a name="ivmharddisk-interface"></a>Interfaz IVMHardDisk

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Proporciona acceso a una imagen de disco duro. Se puede acceder a él mediante la propiedad [**IVMHardDiskConnection::HardDisk**](ivmharddiskconnection-harddisk.md) o el método [**IVMVirtualPC::GetHardDisk.**](ivmvirtualpc-getharddisk.md)

## <a name="members"></a>Miembros

La **interfaz IVMHardDisk** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMHardDisk también** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IVMHardDisk** tiene estos métodos.



| Método                                 | Descripción                                                                                                                                                 |
|:---------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Compacto**](ivmharddisk-compact.md) | Compacta una imagen de disco duro virtual que se expande dinámicamente.<br/>                                                                                        |
| [**Convert**](ivmharddisk-convert.md) | Convierte cualquier disco duro virtual en un disco duro virtual que se expande dinámicamente o en un disco duro virtual de tamaño fijo.<br/>                            |
| [**Combinar**](ivmharddisk-merge.md)     | Combina un disco duro virtual de diferenciación con su imagen de disco primario.<br/>                                                                              |
| [**MergeTo**](ivmharddisk-mergeto.md) | Combina un disco duro virtual de diferenciación con todos sus elementos primarios (hasta el disco duro virtual principal raíz incluido) en un nuevo archivo de disco duro.<br/> |



 

### <a name="properties"></a>Propiedades

La **interfaz IVMHardDisk** tiene estas propiedades.



| Propiedad                                                              | Tipo de acceso           | Descripción                                                                                    |
|:----------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [**Archivo**](ivmharddisk-file.md)<br/>                           | Solo lectura<br/>  | Nombre de ruta de acceso completa del archivo de disco duro virtual.<br/>                                   |
| [**HostFreeDiskSpace**](ivmharddisk-hostfreediskspace.md)<br/> | Solo lectura<br/>  | Cantidad de espacio en disco restante disponible en el host para el disco duro virtual.<br/> |
| [**Parent**](ivmharddisk-parent.md)<br/>                       | Lectura/escritura<br/> | El elemento primario del disco duro virtual de diferenciación.<br/>                                   |
| [**SizeInGuest**](ivmharddisk-sizeinguest.md)<br/>             | Solo lectura<br/>  | Tamaño del disco duro virtual en el sistema operativo invitado.<br/>                    |
| [**SizeOnHost**](ivmharddisk-sizeonhost.md)<br/>               | Solo lectura<br/>  | Tamaño del archivo de disco duro virtual en el equipo host.<br/>                        |
| [**Tipo**](ivmharddisk-type.md)<br/>                           | Solo lectura<br/>  | Tipo del disco duro virtual.<br/>                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHardDisk se define como \_ ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



 

