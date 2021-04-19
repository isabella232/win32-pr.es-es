---
description: Especifica información sobre un documento asociado a una operación de impresión DLP de punto de conexión.
title: DLP_PRINT_INFO estructura (endpointdlp.h)
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
ms.openlocfilehash: 37bde9f62de07083aac6a3d2fb367b021caf3732
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495958"
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

DWORD que especifica la versión de LA API. Este valor siempre debe ser **DLP_PRINT_INFO_V_LATEST**. Esta constante se define en la lista de archivos de encabezado de ejemplo endpointdlp.h del artículo Prevención de [pérdida de datos de punto de conexión.](endpointdlp-endpoint-data-loss-prevention.md)

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

