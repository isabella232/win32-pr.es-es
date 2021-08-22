---
title: Interfaz IVMDVDDriveEvents (VPCCOMInterfaces.h)
description: Define la interfaz de eventos saliente para la interfaz IVMDVDDrive.
ms.assetid: aa68fb6f-032d-4322-8553-b1e840ae63b8
keywords:
- IVMDVDDriveEvents interface Virtual PC
- IVMDVDDriveEvents interface Virtual PC , descrito
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcb34bf77b6692c90977262ac7e2177019169e3195ee44415a0693102e6d15ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136798"
---
# <a name="ivmdvddriveevents-interface"></a>IVMDVDDriveEvents (interfaz)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Define la interfaz de eventos saliente para [**la interfaz IVMDVDDrive.**](ivmdvddrive.md)

## <a name="members"></a>Miembros

La **interfaz IVMDVDDriveEvents** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMDVDDriveEvents** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IVMDVDDriveEvents** tiene estos métodos.



| Método                                                   | Descripción                                                                   |
|:---------------------------------------------------------|:------------------------------------------------------------------------------|
| [**OnMediaEject**](ivmdvddriveevents-onmediaeject.md)   | Recibe la notificación de que los medios se han expulsado de la unidad.<br/>  |
| [**OnMediaInsert**](ivmdvddriveevents-onmediainsert.md) | Recibe la notificación de que se han insertado medios en la unidad.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMDVDDriveEvents se define como c2a7d8e9-e76c-4eb8-94f7-71a5122d249b<br/>         |



 

