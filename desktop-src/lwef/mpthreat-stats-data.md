---
title: MPTHREAT_STATS_DATA estructura (MpClient.h)
description: Datos de estadísticas de amenazas adicionales.
ms.assetid: 8C01C746-8FD8-4311-908D-D1F4E3488480
keywords:
- MPTHREAT_STATS_DATA estructura heredada de Windows environment
- PMPTHREAT_STATS_DATA puntero de estructura Legacy Windows Environment Features
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241245"
---
# <a name="mpthreat_stats_data-structure"></a>Estructura DE DATOS DE MPTHREAT \_ STATS \_

Datos de estadísticas de amenazas adicionales.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPTHREAT_STATS_DATA {
  DWORD dwThreatCount;
} MPTHREAT_STATS_DATA, *PMPTHREAT_STATS_DATA;
```



## <a name="members"></a>Members

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
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





