---
description: Representa el contexto de ejecución cuando se llama a GetPrintExecutionData.
ms.assetid: b6c026b2-8519-45d3-9614-b502eec23cde
title: Enumeración PRINT_EXECUTION_CONTEXT (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_CONTEXT
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 20b1050edc0088fb629ee10cf63dc9cffa07228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276774"
---
# <a name="print_execution_context-enumeration"></a>\_Enumeración de contexto de ejecución de impresión \_

Representa el contexto de ejecución cuando se llama a [**GetPrintExecutionData**](getprintexecutiondata.md) .

## <a name="syntax"></a>Sintaxis


```C++
typedef enum  { 
  PRINT_EXECUTION_CONTEXT_APPLICATION             = 0,
  PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE         = 1,
  PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST  = 2,
  PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE         = 3,
  PRINT_EXECUTION_CONTEXT_WOW64                   = 4
} PRINT_EXECUTION_CONTEXT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**\_aplicación de \_ contexto de ejecución de impresión \_**
</dt> <dd>

El autor de la llamada se está ejecutando en una aplicación.

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**\_servicio de \_ Administrador de \_ trabajos \_ de ejecución de impresión**
</dt> <dd>

El autor de la llamada se ejecuta en el servicio de cola de impresión (spoolsv.exe).

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**HOST de aislamiento de administrador de trabajos de impresión del \_ contexto de ejecución \_ \_ \_ \_**
</dt> <dd>

El autor de la llamada se está ejecutando en el host de aislamiento de impresión (PrintIsolationHost.exe)

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**\_ \_ \_ canalización de filtro de contexto de ejecución de impresión \_**
</dt> <dd>

El autor de la llamada se está ejecutando en la canalización de filtros de impresión (printfilterpipelinesvc.exe)

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**Contexto de ejecución de impresión \_ \_ \_ WOW64**
</dt> <dd>

El autor de la llamada se ejecuta en splwow64.exe

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetPrintExecutionData**](getprintexecutiondata.md)
</dt> <dt>

[**IMPRIMIR \_ datos de ejecución \_**](print-execution-data.md)
</dt> </dl>

 

 




