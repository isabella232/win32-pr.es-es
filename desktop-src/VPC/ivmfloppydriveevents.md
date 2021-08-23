---
title: Interfaz IVMFstonepyDriveEvents (VPCCOMInterfaces.h)
description: Define la interfaz de evento saliente para la interfaz IVMFstonepyDrive. El cliente implementa estos métodos para recibir eventos enviados desde IVMFstonepyDrive.
ms.assetid: fbb66554-f042-4891-94be-1a12b8c179c2
keywords:
- IVMFstonepyDriveEvents interface Virtual PC
- IVMFstonepyDriveEvents interface Virtual PC , descrito
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53cd275c45e23de1bb437b4c233ff64118952afae76e7c6b9bc9366facf4fe8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653515"
---
# <a name="ivmfloppydriveevents-interface"></a>Interfaz IVMFstonepyDriveEvents

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Define la interfaz de evento saliente para la [**interfaz IVMFstonepyDrive.**](ivmfloppydrive.md) El cliente implementa estos métodos para recibir eventos enviados desde **IVMFstonepyDrive**.

## <a name="members"></a>Miembros

La **interfaz IVMFstonepyDriveEvents** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMFstonepyDriveEvents** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IVMFstonepyDriveEvents** tiene estos métodos.



| Método                                                      | Descripción                                                                   |
|:------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**OnMediaEject**](ivmfloppydriveevents-onmediaeject.md)   | Recibe la notificación de que los medios se han expulsado de la unidad.<br/>  |
| [**OnMediaInsert**](ivmfloppydriveevents-onmediainsert.md) | Recibe una notificación que informa de que se ha insertado un medio en la unidad.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMFstonepyDriveEvents se define como a9ed3401-4e09-4177-86ec-a13bf9fa7d4e<br/>      |



 

