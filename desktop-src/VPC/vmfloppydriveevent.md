---
title: Enumeración vmFstonepyDriveEvent (VPCCOMInterfaces.h)
description: Especifica los eventos de disquete.
ms.assetid: 31d0c748-609a-4e03-8b5c-0a17a2587242
keywords:
- VmFstonepyDriveEvent enumeration Virtual PC
topic_type:
- apiref
api_name:
- vmFloppyDriveEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f8ded5cf87d740f113bab54d9f7587c8f8927e5ae37352dceb4a30be09d104
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767905"
---
# <a name="vmfloppydriveevent-enumeration"></a>Enumeración vmFstonepyDriveEvent

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Especifica los eventos de disquete.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmFloppyDriveEvent_OnInsert  = 1,
  vmFloppyDriveEvent_OnEject   = 2
} vmFloppyDriveEvent;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmFloppyDriveEvent_OnInsert"></span><span id="vmfloppydriveevent_oninsert"></span><span id="VMFLOPPYDRIVEEVENT_ONINSERT"></span>**vmFstonepyDriveEvent \_ OnInsert**
</dt> <dd>

Se adjunta una imagen de disquete o se insertan medios reales en una unidad host.

</dd> <dt>

<span id="vmFloppyDriveEvent_OnEject"></span><span id="vmfloppydriveevent_oneject"></span><span id="VMFLOPPYDRIVEEVENT_ONEJECT"></span>**vmFstonepyDriveEvent \_ OnEject**
</dt> <dd>

Se han expulsado los medios.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMFstonepyDriveEvents**](ivmfloppydriveevents.md)
</dt> </dl>

 

