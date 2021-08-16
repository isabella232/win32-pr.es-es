---
description: Especifica el nivel de cumplimiento de una operación de prevención de pérdida de datos (DLP) del punto de conexión.
title: Enumeración DlpAppEnforceLevel (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpAppEnforceLevel
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 99bd06a41c88ff0b5a02b9b329877c015aea7dfb3fdbc58fea3c2e305829faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349355"
---
# <a name="dlpappenforcelevel-enumeration"></a>DlpAppEnforceLevel (enumeración)

Especifica el nivel de cumplimiento de una operación de prevención de pérdida de datos (DLP) del punto de conexión.

## <a name="syntax"></a>Syntax


```C++
typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, 
    DlpAppEnforceLevelNotify,   
    DlpAppEnforceLevelPrevent,   
    DlpAppEnforceLevelFull, 
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;
```


## <a name="constants"></a>Constantes

<dl> <dt>

*DlpAppEnforceLevelNone* \[ En\]
</dt> <dd>

Ninguna aplicación por parte de la aplicación. El sistema DLP aplicará la operación.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelNotify* \[ En\]
</dt> <dd>

La aplicación Tne usará las API dlp para notificar al sistema DLP sobre la operación. El sistema DLP aplicará la operación.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelPrevent* \[ En\]
</dt> <dd>

No se admite en la versión actual.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelFull* \[ En\]
</dt> <dd>

No se admite en la versión actual.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelCount* \[ En\]
</dt> <dd>

Valor máximo de la enumeración .

</dd> </dl>



## <a name="remarks"></a>Comentarios

La estructura DLP_APP_OP_ENLIGHTENED_LEVEL utiliza [los valores de esta enumeración.](endpointdlp-dlp_app_op_enlightened_level.md)


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |

