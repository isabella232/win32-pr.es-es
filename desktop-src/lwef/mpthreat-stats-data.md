---
title: MPTHREAT_STATS_DATA estructura (MpClient. h)
description: Datos adicionales de estadísticas de amenazas.
ms.assetid: 8C01C746-8FD8-4311-908D-D1F4E3488480
keywords:
- MPTHREAT_STATS_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPTHREAT_STATS_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPTHREAT_STATS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9525ddcfc580e9a82ffdb191d20e3748f7a1e16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150233"
---
# <a name="mpthreat_stats_data-structure"></a>Estructura de datos de \_ estadísticas de MPTHREAT \_

Datos adicionales de estadísticas de amenazas.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPTHREAT_STATS_DATA {
  DWORD dwThreatCount;
} MPTHREAT_STATS_DATA, *PMPTHREAT_STATS_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwThreatCount**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Número de amenazas.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





