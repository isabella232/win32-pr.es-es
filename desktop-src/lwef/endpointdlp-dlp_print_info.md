---
description: Especifica información sobre un documento asociado a una operación de impresión DLP de punto de conexión.
title: Estructura DLP_PRINT_INFO (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_PRINT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: e55b3dc22c77d85e15499ea0fb2a6634ece044496637c811ae42e4afd632704e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725825"
---
# <a name="dlp_print_info-structure"></a>DLP_PRINT_INFO estructura

Especifica información sobre un documento asociado a una operación de impresión DLP de punto de conexión.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DLP_PRINT_INFO {
    DWORD Version;
    LPCWSTR PrinterName;
    LPCWSTR JobName;
    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;
```


## <a name="members"></a>Miembros

<dl> <dt>

*Versión* \[ En\]
</dt> <dd>

DWORD que especifica la versión de la API. Este valor siempre debe ser **DLP_PRINT_INFO_V_LATEST**. Esta constante se define en la lista de archivos de encabezado de ejemplo endpointdlp.h del artículo Prevención de [pérdida de datos de punto de conexión.](endpointdlp-endpoint-data-loss-prevention.md)

</dd> </dl>

<dl> <dt>

*PrinterName* \[ En\]
</dt> <dd>

LPCWSTR que identifica la impresora de destino.

</dd> </dl>

<dl> <dt>

*JobName* \[ En\]
</dt> <dd>

LPCWSTR que especifica el nombre del trabajo de impresión.

</dd> </dl>

<dl> <dt>

*OutputFileName* \[ En\]
</dt> <dd>

LPCWSTR que especifica la ruta de acceso al archivo de salida al imprimir en un archivo.

</dd> </dl>



## <a name="remarks"></a>Observaciones


## <a name="requirements"></a>Requisitos



| Requisito          |    Value                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |

