---
title: MPSCAN_RESOURCES estructura (MpClient. h)
description: Información de recursos pasada durante una operación de examen.
ms.assetid: D97712A6-547D-44CC-B55D-039A5CCE20BF
keywords:
- MPSCAN_RESOURCES estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPSCAN_RESOURCES características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPSCAN_RESOURCES
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ee9ea259bca6bf66eb81fcd17b13d509d5a065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997119"
---
# <a name="mpscan_resources-structure"></a>\_Estructura de recursos MPSCAN

Información de recursos pasada durante una operación de examen.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPSCAN_RESOURCES {
  DWORD            dwResourceCount;
  PMPRESOURCE_INFO pResourceList;
} MPSCAN_RESOURCES, *PMPSCAN_RESOURCES;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwResourceCount**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Recuento de recursos.

</dd> <dt>

**pResourceList**
</dt> <dd>

Tipo: **PMPRESOURCE \_ info**

</dd> <dd>

Matriz de recursos. Vea [**\_ información de MPRESOURCE**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**información de MPRESOURCE \_**](mpresource-info.md)
</dt> </dl>

 

 





