---
title: Interfaz IVMFloppyDriveEvents (VPCCOMInterfaces. h)
description: Define la interfaz de eventos salientes para la interfaz IVMFloppyDrive. El cliente implementa estos métodos para recibir los eventos enviados desde IVMFloppyDrive.
ms.assetid: fbb66554-f042-4891-94be-1a12b8c179c2
keywords:
- Interfaz IVMFloppyDriveEvents Virtual PC
- Interfaz IVMFloppyDriveEvents Virtual PC, descripción
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
ms.openlocfilehash: 5f9b799bd6227882c2991f9b310f39d38b20692d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151079"
---
# <a name="ivmfloppydriveevents-interface"></a>Interfaz IVMFloppyDriveEvents

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define la interfaz de eventos salientes para la interfaz [**IVMFloppyDrive**](ivmfloppydrive.md) . El cliente implementa estos métodos para recibir los eventos enviados desde **IVMFloppyDrive**.

## <a name="members"></a>Miembros

La interfaz **IVMFloppyDriveEvents** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMFloppyDriveEvents** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IVMFloppyDriveEvents** tiene estos métodos.



| Método                                                      | Descripción                                                                   |
|:------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**OnMediaEject**](ivmfloppydriveevents-onmediaeject.md)   | Recibe la notificación de que se ha expulsado el medio de la unidad.<br/>  |
| [**OnMediaInsert**](ivmfloppydriveevents-onmediainsert.md) | Recibe la notificación de que los medios se han insertado en la unidad.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMFloppyDriveEvents se define como a9ed3401-4e09-4177-86ec-a13bf9fa7d4e<br/>      |



 

