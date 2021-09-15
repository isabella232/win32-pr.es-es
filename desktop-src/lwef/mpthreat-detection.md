---
title: MPTHREAT_DETECTION enumeración (MpClient.h)
description: Posibles tipos conocidos de detección de amenazas no conocidas.
ms.assetid: 14FCA9BD-A9A1-488B-B8E8-88DE0DF18F27
keywords:
- MPTHREAT_DETECTION enumeración heredada de Windows environment
- PMPTHREAT_DETECTION puntero de enumeración heredados Windows environment
topic_type:
- apiref
api_name:
- MPTHREAT_DETECTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86edc0e1ca4ee130f2a2a4a678447771f1ae40ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574992"
---
# <a name="mpthreat_detection-enumeration"></a>Enumeración MPTHREAT \_ DETECTION

Posibles tipos conocidos de detección de amenazas no conocidas.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagMPTHREAT_DETECTION { 
  MP_THREAT_DETECTION_CONCRETE    = 0,
  MP_THREAT_DETECTION_HEURISTIC   = 1,
  MP_THREAT_DETECTION_GENERIC     = 2,
  MP_THREAT_DETECTION_SUSPICIOUS  = 4,
  MP_THREAT_DETECTION_FASTPATH    = 8
} MPTHREAT_DETECTION, *PMPTHREAT_DETECTION;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**DETECCIÓN DE AMENAZAS DE MP \_ \_ \_ CONCRETA**
</dt> <dd>

Se detectó una amenaza a través de firmas concretas.

</dd> <dt>

<span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**\_HEURÍSTICA DE \_ \_ DETECCIÓN DE AMENAZAS DE MP**
</dt> <dd>

Se detectó una amenaza a través de la heurística.

</dd> <dt>

<span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**DETECCIÓN DE AMENAZAS DE MP \_ \_ \_ GENÉRICA**
</dt> <dd>

Se detectó una amenaza a través de firmas genéricas.

</dd> <dt>

<span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**DETECCIÓN \_ DE AMENAZAS DE MP \_ \_ SOSPECHOSA**
</dt> <dd>

La amenaza se detectó a través de la supervisión del comportamiento.

</dd> <dt>

<span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**MP \_ THREAT \_ DETECTION \_ FASTPATH**
</dt> <dd>

Se detectó una amenaza a través de fastpath.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





