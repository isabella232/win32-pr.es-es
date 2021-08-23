---
title: MPTHREAT_STATS estructura (MpClient.h)
description: Estadísticas relacionadas con amenazas.
ms.assetid: 78B7E2A8-1BB4-4610-8E90-1F8ECBE740A8
keywords:
- MPTHREAT_STATS estructura heredada de Windows environment
- PMPTHREAT_STATS puntero de estructura heredados Windows environment features
topic_type:
- apiref
api_name:
- MPTHREAT_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7671b45dc09c8aca494ad270aa69fc386ef3d7c03d5144fdc3e89b4f657bb07b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975945"
---
# <a name="mpthreat_stats-structure"></a>Estructura DE \_ ESTADÍSTICAS DE MPTHREAT

Estadísticas relacionadas con amenazas.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPTHREAT_STATS {
  UINT ThreatCount;
  UINT SuspiciousThreatCount;
  UINT Reserved[4];
} MPTHREAT_STATS, *PMPTHREAT_STATS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ThreatCount**
</dt> <dd>

Tipo: **UINT**

</dd> <dd>

Número de amenazas detectadas.

</dd> <dt>

**SuspiciousThreatCount**
</dt> <dd>

Tipo: **UINT**

</dd> <dd>

Número de amenazas detectadas con la supervisión del comportamiento.

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **UINT \[ 4 \]**

</dd> <dd>

Campos reservados para uso futuro.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





