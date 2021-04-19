---
description: Especifica información sobre un documento asociado a una operación DLP de punto de conexión.
title: DLP_DOCUMENT_INFO estructura (endpointdlp.h)
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
ms.openlocfilehash: d588b627a4d5a88162cb0af67df1b5bf4fd943f1
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495961"
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

DWORD que especifica la versión de la API. Este valor siempre debe ser **DLP_DOCUMENT_INFO_V_LATEST**. Esta constante se define en la lista de archivos de encabezado de ejemplo endpointdlp.h del artículo Prevención de [pérdida de datos de punto de conexión.](endpointdlp-endpoint-data-loss-prevention.md)

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



| Requisito          |    Value                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |

