---
title: MPTHREAT_DETECTION enumeración (MpClient.h)
description: Posibles tipos de detección de amenazas no conocidas.
ms.assetid: 14FCA9BD-A9A1-488B-B8E8-88DE0DF18F27
keywords:
- MPTHREAT_DETECTION enumeración de características de entorno de Windows heredado
- PMPTHREAT_DETECTION puntero de enumeración heredado Windows características del entorno de ejecución
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
ms.openlocfilehash: 6d362edbb7257f8be5577880a4390c5a2f5f5703504a5f7447154bebe5ada500
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601185"
---
# <a name="mpthreat_detection-enumeration"></a>Enumeración MPTHREAT \_ DETECTION

Posibles tipos de detección de amenazas no conocidas.

## <a name="syntax"></a>Syntax


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

Se detectó una amenaza a través de la supervisión del comportamiento.

</dd> <dt>

<span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**MP \_ THREAT \_ DETECTION \_ FASTPATH**
</dt> <dd>

Se detectó una amenaza a través de fastpath.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





