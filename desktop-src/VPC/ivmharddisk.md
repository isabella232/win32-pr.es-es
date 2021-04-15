---
title: Interfaz IVMHardDisk (VPCCOMInterfaces. h)
description: Proporciona acceso a una imagen de disco duro. Se puede tener acceso a ella a través de la propiedad IVMHardDiskConnection disco duro o el método IVMVirtualPC GetHardDisk.
ms.assetid: 0c536906-91be-428a-8199-c452abef423d
keywords:
- Interfaz IVMHardDisk Virtual PC
- Interfaz IVMHardDisk Virtual PC, descripción
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
ms.openlocfilehash: 24d6df46e7c698676e3873dd17a854fd0b7d7933
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488932"
---
# <a name="ivmharddisk-interface"></a>Interfaz IVMHardDisk

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Proporciona acceso a una imagen de disco duro. Se puede tener acceso a ella a través de la propiedad [**IVMHardDiskConnection:: disco duro**](ivmharddiskconnection-harddisk.md) o el método [**IVMVirtualPC:: GetHardDisk**](ivmvirtualpc-getharddisk.md) .

## <a name="members"></a>Miembros

La interfaz **IVMHardDisk** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMHardDisk** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IVMHardDisk** tiene estos métodos.



| Método                                 | Descripción                                                                                                                                                 |
|:---------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Compacto**](ivmharddisk-compact.md) | Compacta una imagen de disco duro virtual de expansión dinámica.<br/>                                                                                        |
| [**Convert**](ivmharddisk-convert.md) | Convierte cualquier disco duro virtual en un disco duro virtual de expansión dinámica o en un disco duro virtual de tamaño fijo.<br/>                            |
| [**Sin**](ivmharddisk-merge.md)     | Combina un disco duro virtual de diferenciación con su imagen de disco principal.<br/>                                                                              |
| [**Fusionar mediante combinación**](ivmharddisk-mergeto.md) | Combina un disco duro virtual de diferenciación con todos sus elementos primarios (hasta el disco duro virtual primario raíz incluido) en un nuevo archivo de disco duro.<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **IVMHardDisk** tiene estas propiedades.



| Propiedad                                                              | Tipo de acceso           | Descripción                                                                                    |
|:----------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [**Archivo**](ivmharddisk-file.md)<br/>                           | Solo lectura<br/>  | El nombre de la ruta de acceso completa del archivo de disco duro virtual.<br/>                                   |
| [**HostFreeDiskSpace**](ivmharddisk-hostfreediskspace.md)<br/> | Solo lectura<br/>  | La cantidad de espacio en disco restante disponible en el host para el disco duro virtual.<br/> |
| [**Parent**](ivmharddisk-parent.md)<br/>                       | Lectura/escritura<br/> | El elemento primario del disco duro virtual de diferenciación.<br/>                                   |
| [**SizeInGuest**](ivmharddisk-sizeinguest.md)<br/>             | Solo lectura<br/>  | El tamaño del disco duro virtual en el sistema operativo invitado.<br/>                    |
| [**SizeOnHost**](ivmharddisk-sizeonhost.md)<br/>               | Solo lectura<br/>  | El tamaño del archivo de disco duro virtual en el equipo host.<br/>                        |
| [**Tipo**](ivmharddisk-type.md)<br/>                           | Solo lectura<br/>  | El tipo de disco duro virtual.<br/>                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk se define como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



 

