---
title: Enumeración VMDriveBusType (VPCCOMInterfaces.h)
description: Especifica el tipo de bus.
ms.assetid: 7e0926f3-8218-49c9-8d3a-27214c111a77
keywords:
- VMDriveBusType (enumeración de PC virtual)
topic_type:
- apiref
api_name:
- VMDriveBusType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ee106c42267397f8dae66b1ed431b5d6fa3c1047b7ace6fd9a44bd81960be2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056423"
---
# <a name="vmdrivebustype-enumeration"></a>Enumeración VMDriveBusType

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Especifica el tipo de bus.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmDriveBusType_Invalid  = -1,
  vmDriveBusType_IDE      = 0,
  vmDriveBusType_SCSI     = 1
} VMDriveBusType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmDriveBusType_Invalid"></span><span id="vmdrivebustype_invalid"></span><span id="VMDRIVEBUSTYPE_INVALID"></span>**vmDriveBusType no \_ válido**
</dt> <dd>

Sin tipo de bus.

</dd> <dt>

<span id="vmDriveBusType_IDE"></span><span id="vmdrivebustype_ide"></span><span id="VMDRIVEBUSTYPE_IDE"></span>**IDE de vmDriveBusType \_**
</dt> <dd>

Tipo de bus IDE.

</dd> <dt>

<span id="vmDriveBusType_SCSI"></span><span id="vmdrivebustype_scsi"></span><span id="VMDRIVEBUSTYPE_SCSI"></span>**vmDriveBusType \_ SCSI**
</dt> <dd>

Tipo de bus SCSI.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |



 

