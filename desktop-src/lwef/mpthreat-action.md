---
title: MPTHREAT_ACTION enumeración (MpClient.h)
description: Posibles acciones de amenaza.
ms.assetid: 142249A5-4C9D-4E3A-A06E-70C040F9C14F
keywords:
- MPTHREAT_ACTION enumeración heredada de Windows environment
- PMPTHREAT_ACTION puntero de enumeración heredados Windows environment
topic_type:
- apiref
api_name:
- MPTHREAT_ACTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae0377517af590072b797a57c051ad062842ea9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574993"
---
# <a name="mpthreat_action-enumeration"></a>Enumeración MPTHREAT \_ ACTION

Posibles acciones de amenaza.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagMPTHREAT_ACTION { 
  MP_THREAT_ACTION_UNKNOWN      = 0,
  MP_THREAT_ACTION_CLEAN        = 1,
  MP_THREAT_ACTION_QUARANTINE   = 2,
  MP_THREAT_ACTION_REMOVE       = 3,
  MP_THREAT_ACTION_ALLOW        = 6,
  MP_THREAT_ACTION_USERDEFINED  = 8,
  MP_THREAT_ACTION_NOACTION     = 9,
  MP_THREAT_ACTION_BLOCK        = 10,
  MP_THREAT_ACTION_MAX_VALUE    = 10
} MPTHREAT_ACTION, *PMPTHREAT_ACTION;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_THREAT_ACTION_UNKNOWN"></span><span id="mp_threat_action_unknown"></span>**ACCIÓN \_ DE AMENAZA DE MP \_ \_ DESCONOCIDA**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_CLEAN"></span><span id="mp_threat_action_clean"></span>**ACCIÓN \_ DE AMENAZA DE MP \_ \_ LIMPIA**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_QUARANTINE"></span><span id="mp_threat_action_quarantine"></span>**CUARENTENA \_ DE ACCIÓN DE AMENAZA DE \_ \_ MP**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_REMOVE"></span><span id="mp_threat_action_remove"></span>**ACCIÓN \_ DE AMENAZA DE MP \_ \_ REMOVE**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_ALLOW"></span><span id="mp_threat_action_allow"></span>**ACCIÓN \_ DE AMENAZA DE MP \_ \_ ALLOW**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_USERDEFINED"></span><span id="mp_threat_action_userdefined"></span>**ACCIÓN \_ DE AMENAZA DE MP DEFINIDA POR EL \_ \_ USUARIO**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_NOACTION"></span><span id="mp_threat_action_noaction"></span>**ACCIÓN \_ DE AMENAZA DE MP \_ \_ NOACTION**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_BLOCK"></span><span id="mp_threat_action_block"></span>**BLOQUE DE \_ ACCIÓN DE AMENAZA DE \_ \_ MP**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_MAX_VALUE"></span><span id="mp_threat_action_max_value"></span>**VALOR \_ MÁXIMO DE ACCIÓN DE AMENAZA DE \_ \_ \_ MP**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





