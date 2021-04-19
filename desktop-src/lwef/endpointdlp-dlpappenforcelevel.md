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
ms.openlocfilehash: d0ccc8d0d39bc4022899deaeb9e8a81eae1f720f
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495952"
---
# <a name="dlpappenforcelevel-enumeration"></a>DlpAppEnforceLevel (enumeración)

Especifica el nivel de cumplimiento de una operación de prevención de pérdida de datos (DLP) del punto de conexión.

## <a name="syntax"></a>Sintaxis


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



## <a name="remarks"></a>Observaciones

La estructura DLP_APP_OP_ENLIGHTENED_LEVEL utiliza [los valores de esta enumeración.](endpointdlp-dlp_app_op_enlightened_level.md)


## <a name="requirements"></a>Requisitos



| Requisito          |    Value                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |

