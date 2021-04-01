---
title: MPTHREAT_STATS estructura (MpClient. h)
description: Estadísticas relacionadas con amenazas.
ms.assetid: 78B7E2A8-1BB4-4610-8E90-1F8ECBE740A8
keywords:
- MPTHREAT_STATS estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPTHREAT_STATS características de entorno heredado de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905208"
---
# <a name="mpthreat_stats-structure"></a>MPTHREAT ( \_ estructura de estadísticas)

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

Tipo: **uint**

</dd> <dd>

Número de amenazas detectadas.

</dd> <dt>

**SuspiciousThreatCount**
</dt> <dd>

Tipo: **uint**

</dd> <dd>

Número de amenazas detectadas con supervisión de comportamiento.

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **uint \[ 4 \]**

</dd> <dd>

Campos reservados para uso futuro.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





