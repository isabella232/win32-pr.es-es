---
description: Especifica información de estado sobre una operación DLP de punto de conexión.
title: DLP_POSTOP_STATUS estructura (endpointdlp.h)
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
ms.openlocfilehash: c0221926700fc8960de5ef4d25c36136c3fc9737
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495824"
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

DWORD que especifica la versión de LA API. Este valor siempre se debe **DLP_POSTOP_STATUS_V_LATEST**. Esta constante se define en la lista de archivos de encabezado de ejemplo endpointdlp.h del artículo Prevención de [pérdida de datos de punto de conexión](endpointdlp-endpoint-data-loss-prevention.md)

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
