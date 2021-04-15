---
title: Enumeración MPTHREAT_SEVERITY (MpClient. h)
description: Posibles gravedades de las amenazas.
ms.assetid: 7C50AC74-16CB-4198-ABB2-D6999429F2EA
keywords:
- MPTHREAT_SEVERITY enumeración características de entorno heredado de Windows
- PMPTHREAT_SEVERITY el puntero de enumeración características de entorno heredado de Windows
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
ms.openlocfilehash: 2eec7bff3b23a89ce8187798d8a69a9968cbc2bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695912"
---
# <a name="mpthreat_severity-enumeration"></a>MPTHREAT \_ (enumeración de gravedad)

Posibles gravedades de las amenazas.

## <a name="syntax"></a>Sintaxis


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

<span id="MP_THREAT_SEVERITY_UNKNOWN"></span><span id="mp_threat_severity_unknown"></span>**gravedad de amenaza de MP \_ \_ \_ desconocida**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_SEVERITY_LOW"></span><span id="mp_threat_severity_low"></span>**gravedad de amenaza de MP \_ \_ \_ baja**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_SEVERITY_MODERATE"></span><span id="mp_threat_severity_moderate"></span>**gravedad de amenaza de MP \_ \_ \_ moderada**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_SEVERITY_HIGH"></span><span id="mp_threat_severity_high"></span>**gravedad de amenaza de MP \_ \_ \_ alta**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_SEVERITY_SEVERE"></span><span id="mp_threat_severity_severe"></span>**gravedad de la amenaza de MP \_ \_ \_ grave**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_SEVERITY_MAXVALUE"></span><span id="mp_threat_severity_maxvalue"></span>**gravedad de amenaza de MP \_ \_ \_ MAXVALUE**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





