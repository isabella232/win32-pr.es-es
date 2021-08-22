---
description: Representa el contexto de ejecución cuando se llama a GetPrintExecutionData.
ms.assetid: b6c026b2-8519-45d3-9614-b502eec23cde
title: PRINT_EXECUTION_CONTEXT enumeración (Winspool.h)
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
ms.openlocfilehash: 78e4afb29b75c0a73799302ddb76e270b18ca2c38cb6325b59ebae5041d5f99e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033963"
---
# <a name="print_execution_context-enumeration"></a>Enumeración PRINT \_ EXECUTION \_ CONTEXT

Representa el contexto de ejecución [**cuando se llama a GetPrintExecutionData.**](getprintexecutiondata.md)

## <a name="syntax"></a>Syntax


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

<span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**APLICACIÓN DE \_ CONTEXTO DE EJECUCIÓN DE \_ \_ IMPRESIÓN**
</dt> <dd>

El autor de la llamada se ejecuta en una aplicación.

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**SERVICIO \_ \_ \_ SPOOLER DE CONTEXTO DE EJECUCIÓN DE \_ IMPRESIÓN**
</dt> <dd>

El autor de la llamada se ejecuta en el servicio de cola (spoolsv.exe).

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**HOST DE \_ AISLAMIENTO DE COLA DE TRABAJOS DE COLA DE CONTEXTO DE EJECUCIÓN DE \_ \_ \_ \_ IMPRESIÓN**
</dt> <dd>

El autor de la llamada se ejecuta en el host de aislamiento de impresión (PrintIsolationHost.exe)

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**CANALIZACIÓN DE \_ FILTRO DE CONTEXTO DE EJECUCIÓN DE \_ \_ \_ IMPRESIÓN**
</dt> <dd>

El autor de la llamada se ejecuta en la canalización de filtro de impresión (printfilterpipelinesvc.exe)

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**CONTEXTO \_ DE EJECUCIÓN DE IMPRESIÓN \_ \_ WOW64**
</dt> <dd>

El llamador se ejecuta en splwow64.exe

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetPrintExecutionData**](getprintexecutiondata.md)
</dt> <dt>

[**IMPRIMIR \_ DATOS DE \_ EJECUCIÓN**](print-execution-data.md)
</dt> </dl>

 

 




