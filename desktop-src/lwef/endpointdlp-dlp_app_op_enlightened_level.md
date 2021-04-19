---
description: Asocia una acción de prevención de pérdida de datos (DLP) de punto de conexión a un nivel de cumplimiento.
title: DLP_APP_OP_ENLIGHTENED_LEVEL estructura (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_APP_OP_ENLIGHTENED_LEVEL
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 2d9c1aa8335078cad71832c6090cada1669641cb
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495964"
---
# <a name="dlp_app_op_enlightened_level-structure"></a>DLP_APP_OP_ENLIGHTENED_LEVEL estructura

Asocia una acción de prevención de pérdida de datos (DLP) de punto de conexión a un nivel de cumplimiento.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;
```


## <a name="members"></a>Miembros

<dl> <dt>

*Operación* \[ En\]
</dt> <dd>

Valor de la enumeración [DlpActionType](endpointdlp-dlpactiontype.md) que especifica el tipo de acción DLP del punto de conexión.

</dd> </dl>

<dl> <dt>

*AppEnforcementLevel* \[ En\]
</dt> <dd>

Valor de [DlpAppEnforceLevel que](endpointdlp-dlpappenforcelevel.md) especifica el nivel de cumplimiento para el tipo de acción DLP de punto de conexión asociado.

</dd> </dl>





## <a name="remarks"></a>Observaciones

Pase una matriz de estas estructuras a [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md) para establecer el modo de cumplimiento de un conjunto de operaciones DLP de punto de conexión.

## <a name="requirements"></a>Requisitos



| Requisito          |    Value                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |

