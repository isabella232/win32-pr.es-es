---
description: Especifica información de estado sobre una operación DLP de punto de conexión.
title: Estructura DLP_POSTOP_STATUS (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_POSTOP_STATUS
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 6b8922bee5fb93ee4412833418a63c19dd311c8809cf64132a0f28fbe91d11bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610235"
---
# <a name="dlp_postop_status-structure"></a>DLP_POSTOP_STATUS estructura

Especifica información de estado sobre una operación DLP de punto de conexión.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DLP_POSTOP_STATUS {
    
    DWORD Version;    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS; 
```


## <a name="members"></a>Miembros

<dl> <dt>

*Versión* \[ En\]
</dt> <dd>

DWORD que especifica la versión de la API. Este valor siempre se debe **DLP_POSTOP_STATUS_V_LATEST**. Esta constante se define en la lista de archivos de encabezado de ejemplo endpointdlp.h del artículo Prevención de [pérdida de datos de punto de conexión](endpointdlp-endpoint-data-loss-prevention.md)

</dd> </dl>

<dl> <dt>

*OperationSuccess* \[ En\]
</dt> <dd>

Un BOOL que indica si la operación de apertura se ha realizado correctamente.

</dd> </dl>





## <a name="remarks"></a>Observaciones


## <a name="requirements"></a>Requisitos



| Requisito          |    Value                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |
