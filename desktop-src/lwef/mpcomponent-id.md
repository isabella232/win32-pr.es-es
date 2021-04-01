---
title: Enumeración MPCOMPONENT_ID (MpClient. h)
description: Componentes posibles para el administrador de protección contra malware de.
ms.assetid: 014B400A-880B-419D-9F50-F3354CE945D9
keywords:
- MPCOMPONENT_ID enumeración características de entorno heredado de Windows
- PMPCOMPONENT_ID el puntero de enumeración características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPCOMPONENT_ID
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196eebc5a3bee4968878c376cd7358724c9c55cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150146"
---
# <a name="mpcomponent_id-enumeration"></a>\_Enumeración de MPCOMPONENT ID

Componentes posibles para el administrador de protección contra malware de.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagMPCOMPONENT_ID { 
  MPCOMPONENT_AS_SIGNATURE         = 0,
  MPCOMPONENT_AV_SIGNATURE         = 1,
  MPCOMPONENT_REALTIME_MONITOR     = 2,
  MPCOMPONENT_ONACCESS_PROTECTION  = 3,
  MPCOMPONENT_IOAV_PROTECTION      = 4,
  MPCOMPONENT_BEHAVIOR_MONITOR     = 5,
  MPCOMPONENT_AUTO_SCAN            = 6,
  MPCOMPONENT_AUTO_SIGUPDATE       = 7,
  MPCOMPONENT_IPC                  = 8,
  MPCOMPONENT_NIS                  = 9,
  MPCOMPONENT_ELAM                 = 10,
  MPCOMPONENT_MAXVALUE             = 10
} MPCOMPONENT_ID, *PMPCOMPONENT_ID;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MPCOMPONENT_AS_SIGNATURE"></span><span id="mpcomponent_as_signature"></span>**MPCOMPONENT \_ como \_ firma**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_AV_SIGNATURE"></span><span id="mpcomponent_av_signature"></span>**\_firma de AV MPCOMPONENT \_**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_REALTIME_MONITOR"></span><span id="mpcomponent_realtime_monitor"></span>**MONITOR de MPCOMPONENT en \_ tiempo real \_**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_ONACCESS_PROTECTION"></span><span id="mpcomponent_onaccess_protection"></span>**protección de MPCOMPONENT de \_ acceso \_**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_IOAV_PROTECTION"></span><span id="mpcomponent_ioav_protection"></span>**\_protección de IOAV de MPCOMPONENT \_**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_BEHAVIOR_MONITOR"></span><span id="mpcomponent_behavior_monitor"></span>**\_monitor de comportamiento de MPCOMPONENT \_**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_AUTO_SCAN"></span><span id="mpcomponent_auto_scan"></span>**\_examen automático de MPCOMPONENT \_**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_AUTO_SIGUPDATE"></span><span id="mpcomponent_auto_sigupdate"></span>**\_SIGUPDATE MPCOMPONENT auto \_**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_IPC"></span><span id="mpcomponent_ipc"></span>**\_IPC MPCOMPONENT**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_NIS"></span><span id="mpcomponent_nis"></span>**MPCOMPONENT \_ NIS**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_ELAM"></span><span id="mpcomponent_elam"></span>**MPCOMPONENT \_ Elam**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_MAXVALUE"></span><span id="mpcomponent_maxvalue"></span>**MPCOMPONENT \_ MAXVALUE**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





