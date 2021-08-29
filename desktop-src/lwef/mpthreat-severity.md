---
title: MPTHREAT_SEVERITY enumeración (MpClient.h)
description: Posibles gravedades de amenaza.
ms.assetid: 7C50AC74-16CB-4198-ABB2-D6999429F2EA
keywords:
- MPTHREAT_SEVERITY enumeración de características heredadas Windows entorno
- PMPTHREAT_SEVERITY puntero de enumeración Heredados Windows Environment Features
topic_type:
- apiref
api_name:
- MPTHREAT_SEVERITY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f7fe63df6e3d6d9be3e12a25138927e95bf45626ba40bd009f9a7660029f667
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665255"
---
# <a name="mpthreat_severity-enumeration"></a>Enumeración \_ SEVERITY de MPTHREAT

Posibles gravedades de amenaza.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPTHREAT_SEVERITY { 
  MP_THREAT_SEVERITY_UNKNOWN   = 0,
  MP_THREAT_SEVERITY_LOW       = 1,
  MP_THREAT_SEVERITY_MODERATE  = 2,
  MP_THREAT_SEVERITY_HIGH      = 4,
  MP_THREAT_SEVERITY_SEVERE    = 5,
  MP_THREAT_SEVERITY_MAXVALUE  = 5
} MPTHREAT_SEVERITY, *PMPTHREAT_SEVERITY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_THREAT_SEVERITY_UNKNOWN"></span><span id="mp_threat_severity_unknown"></span>**GRAVEDAD \_ DE AMENAZA DE MP \_ \_ DESCONOCIDA**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_SEVERITY_LOW"></span><span id="mp_threat_severity_low"></span>**GRAVEDAD \_ DE AMENAZA DE MP \_ \_ BAJA**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_SEVERITY_MODERATE"></span><span id="mp_threat_severity_moderate"></span>**GRAVEDAD DE AMENAZA DE MP \_ \_ \_ MODERADA**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_SEVERITY_HIGH"></span><span id="mp_threat_severity_high"></span>**GRAVEDAD DE AMENAZA DE MP \_ \_ \_ ALTA**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_SEVERITY_SEVERE"></span><span id="mp_threat_severity_severe"></span>**GRAVEDAD \_ DE AMENAZA DE MP \_ \_ GRAVE**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_SEVERITY_MAXVALUE"></span><span id="mp_threat_severity_maxvalue"></span>**MP \_ THREAT \_ SEVERITY \_ MAXVALUE**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





