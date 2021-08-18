---
title: MPSCAN_RESOURCES estructura (MpClient.h)
description: Información de recursos que se pasa durante una operación de examen.
ms.assetid: D97712A6-547D-44CC-B55D-039A5CCE20BF
keywords:
- MPSCAN_RESOURCES estructura heredada de Windows environment
- PMPSCAN_RESOURCES puntero de estructura heredado Windows environment Features
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
ms.openlocfilehash: dd70b442e7179d516d2e9c60b81e6c52b0f696f5719a255871e8687773bf71ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747354"
---
# <a name="mpscan_resources-structure"></a>Estructura DE RECURSOS DE MPSCAN \_

Información de recursos que se pasa durante una operación de examen.

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

Tipo: **PMPRESOURCE \_ INFO**

</dd> <dd>

Matriz de recursos. Vea [**MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MPRESOURCE \_ INFO**](mpresource-info.md)
</dt> </dl>

 

 





