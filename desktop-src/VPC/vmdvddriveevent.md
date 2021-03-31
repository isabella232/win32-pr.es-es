---
title: Enumeración VMDVDDriveEvent (VPCCOMInterfaces. h)
description: Especifica los eventos de la unidad de DVD.
ms.assetid: 17126138-614f-42d9-937e-1aca9393557c
keywords:
- Enumeración de VMDVDDriveEvent Virtual PC
topic_type:
- apiref
api_name:
- VMDVDDriveEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967fcd545c0ddd24d01c5dc779929ef4639c6736
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802197"
---
# <a name="vmdvddriveevent-enumeration"></a>Enumeración VMDVDDriveEvent

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Especifica los eventos de la unidad de DVD.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum  { 
  vmDVDDriveEvent_OnInsert  = 1,
  vmDVDDriveEvent_OnEject   = 2
} VMDVDDriveEvent;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmDVDDriveEvent_OnInsert"></span><span id="vmdvddriveevent_oninsert"></span><span id="VMDVDDRIVEEVENT_ONINSERT"></span>**vmDVDDriveEvent \_ Insert**
</dt> <dd>

Se adjunta una imagen ISO o se inserta un medio real en una unidad host.

</dd> <dt>

<span id="vmDVDDriveEvent_OnEject"></span><span id="vmdvddriveevent_oneject"></span><span id="VMDVDDRIVEEVENT_ONEJECT"></span>**vmDVDDriveEvent \_ EJECT**
</dt> <dd>

Se ha expulsado el medio.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMDVDDriveEvents**](ivmdvddriveevents.md)
</dt> </dl>

 

