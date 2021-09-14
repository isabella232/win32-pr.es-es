---
title: MPTHREAT_STATS estructura (MpClient.h)
description: Estadísticas relacionadas con amenazas.
ms.assetid: 78B7E2A8-1BB4-4610-8E90-1F8ECBE740A8
keywords:
- MPTHREAT_STATS estructura heredada de Windows environment
- PMPTHREAT_STATS puntero de estructura heredado Windows environment Features
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
ms.openlocfilehash: 21a2eef7acde5fbeac2cf9951dfad3e6923ccea2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168297"
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



## <a name="members"></a>Members

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
| Encabezado<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





