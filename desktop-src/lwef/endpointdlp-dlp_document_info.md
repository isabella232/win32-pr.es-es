---
description: Especifica información sobre un documento asociado a una operación DLP de punto de conexión.
title: Estructura DLP_DOCUMENT_INFO (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_DOCUMENT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 8aa4b6c961b4e80786e9ada480949245b032750499b38f0deead44f97a2d88fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479768"
---
# <a name="dlp_document_info-structure"></a>DLP_DOCUMENT_INFO estructura

Especifica información sobre un documento asociado a una operación DLP de punto de conexión.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DLP_DOCUMENT_INFO {

    DWORD Version;    
    LPCWSTR PersistentFileName;
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;
```


## <a name="members"></a>Miembros

<dl> <dt>

*Versión* \[ En\]
</dt> <dd>

DWORD que especifica la versión de LA API. Este valor siempre debe ser **DLP_DOCUMENT_INFO_V_LATEST**. Esta constante se define en la lista de archivos de encabezado de ejemplo endpointdlp.h del artículo Prevención de [pérdida de datos de punto de conexión.](endpointdlp-endpoint-data-loss-prevention.md)

</dd> </dl>

<dl> <dt>

*PersistentFileName* \[ En\]
</dt> <dd>

LPCWSTR que especifica la ruta de acceso original del documento.

</dd> </dl>

<dl> <dt>

*LocalFileName* \[ En\]
</dt> <dd>

LPCWSTR que especifica la ruta de acceso al archivo de respaldo real del documento.

</dd> </dl>



## <a name="remarks"></a>Observaciones


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |

