---
title: Enumeración MPCALLBACK_TYPE (MpClient. h)
description: Posibles tipos de devolución de llamada.
ms.assetid: 8E4F50B7-0F02-434D-B91E-C9966C92CDC0
keywords:
- MPCALLBACK_TYPE enumeración características de entorno heredado de Windows
- PMPCALLBACK_TYPE el puntero de enumeración características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPCALLBACK_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a3fd310f3733d36dd92ace1c7a5286bcf73a75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490013"
---
# <a name="mpcallback_type-enumeration"></a>\_Enumeración de tipo MPCALLBACK

Posibles tipos de devolución de llamada.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagMPCALLBACK_TYPE { 
  MPCALLBACK_UNKNOWN                     = 0,
  MPCALLBACK_STATUS                      = 1,
  MPCALLBACK_THREAT                      = 2,
  MPCALLBACK_SCAN                        = 3,
  MPCALLBACK_CLEAN                       = 4,
  MPCALLBACK_PRECHECK                    = 5,
  MPCALLBACK_SIGUPDATE                   = 6,
  MPCALLBACK_SAMPLE                      = 7,
  MPCALLBACK_RESERVED                    = 8,
  MPCALLBACK_CONFIGURATION_NOTIFICATION  = 9,
  MPCALLBACK_FASTPATH                    = 10,
  MPCALLBACK_PRODUCT_EXPIRATION          = 11,
  MPCALLBACK_NIS_PRIVATE                 = 12,
  MPCALLBACK_HEALTH                      = 13,
  MPCALLBACK_ENDOFLIFE                   = 14,
  MPCALLBACK_MALWARETOAST                = 15,
  MPCALLBACK_MAXVALUE                    = 15
} MPCALLBACK_TYPE, *PMPCALLBACK_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MPCALLBACK_UNKNOWN"></span><span id="mpcallback_unknown"></span>**MPCALLBACK \_ desconocido**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_STATUS"></span><span id="mpcallback_status"></span>**Estado de MPCALLBACK \_**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_THREAT"></span><span id="mpcallback_threat"></span>**MPCALLBACK \_ amenaza**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_SCAN"></span><span id="mpcallback_scan"></span>**examen de MPCALLBACK \_**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_CLEAN"></span><span id="mpcallback_clean"></span>**MPCALLBACK \_ Clean**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_PRECHECK"></span><span id="mpcallback_precheck"></span>**COMPROBACIÓN de MPCALLBACK \_**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_SIGUPDATE"></span><span id="mpcallback_sigupdate"></span>**MPCALLBACK \_ SIGUPDATE**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_SAMPLE"></span><span id="mpcallback_sample"></span>**ejemplo de MPCALLBACK \_**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_RESERVED"></span><span id="mpcallback_reserved"></span>**MPCALLBACK \_ reservado**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_CONFIGURATION_NOTIFICATION"></span><span id="mpcallback_configuration_notification"></span>**\_notificación de configuración de MPCALLBACK \_**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_FASTPATH"></span><span id="mpcallback_fastpath"></span>**MPCALLBACK \_ FASTPATH**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_PRODUCT_EXPIRATION"></span><span id="mpcallback_product_expiration"></span>**\_expiración del producto MPCALLBACK \_**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_NIS_PRIVATE"></span><span id="mpcallback_nis_private"></span>**MPCALLBACK \_ NIS \_ privado**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_HEALTH"></span><span id="mpcallback_health"></span>**mantenimiento de MPCALLBACK \_**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_ENDOFLIFE"></span><span id="mpcallback_endoflife"></span>**MPCALLBACK \_ ENDOFLIFE**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_MALWARETOAST"></span><span id="mpcallback_malwaretoast"></span>**MPCALLBACK \_ MALWARETOAST**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_MAXVALUE"></span><span id="mpcallback_maxvalue"></span>**MPCALLBACK \_ MAXVALUE**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





