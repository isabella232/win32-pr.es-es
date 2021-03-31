---
title: Enumeración MPTHREAT_DETECTION (MpClient. h)
description: Posibles tipos conocidos de detección de amenazas defectuosas.
ms.assetid: 14FCA9BD-A9A1-488B-B8E8-88DE0DF18F27
keywords:
- MPTHREAT_DETECTION enumeración características de entorno heredado de Windows
- PMPTHREAT_DETECTION el puntero de enumeración características de entorno heredado de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801904"
---
# <a name="mpthreat_detection-enumeration"></a>\_Enumeración de detección MPTHREAT

Posibles tipos conocidos de detección de amenazas defectuosas.

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

<span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**\_específico de \_ detección de amenazas de MP \_**
</dt> <dd>

Se detectó una amenaza a través de firmas concretas.

</dd> <dt>

<span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**\_heurística de \_ detección de amenazas MP \_**
</dt> <dd>

Se detectó una amenaza a través de la heurística.

</dd> <dt>

<span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**\_ \_ Generic detección de amenazas de MP \_**
</dt> <dd>

Se detectó una amenaza mediante firmas genéricas.

</dd> <dt>

<span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**detección de amenazas de MP \_ \_ \_ sospechosa**
</dt> <dd>

Se detectó una amenaza a través de la supervisión del comportamiento.

</dd> <dt>

<span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**detección de amenazas de MP \_ \_ \_ FASTPATH**
</dt> <dd>

Se detectó una amenaza a través de FastPATH.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





