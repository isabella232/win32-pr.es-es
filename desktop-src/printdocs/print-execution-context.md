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
# <a name="print_execution_context-enumeration"></a><span data-ttu-id="9e833-103">\_Enumeración de contexto de ejecución de impresión \_</span><span class="sxs-lookup"><span data-stu-id="9e833-103">PRINT\_EXECUTION\_CONTEXT enumeration</span></span>

<span data-ttu-id="9e833-104">Representa el contexto de ejecución cuando se llama a [**GetPrintExecutionData**](getprintexecutiondata.md) .</span><span class="sxs-lookup"><span data-stu-id="9e833-104">Represents the execution context when [**GetPrintExecutionData**](getprintexecutiondata.md) is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e833-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e833-105">Syntax</span></span>


```C++
typedef enum  { 
  PRINT_EXECUTION_CONTEXT_APPLICATION             = 0,
  PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE         = 1,
  PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST  = 2,
  PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE         = 3,
  PRINT_EXECUTION_CONTEXT_WOW64                   = 4
} PRINT_EXECUTION_CONTEXT;
```



## <a name="constants"></a><span data-ttu-id="9e833-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="9e833-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9e833-107"><span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**\_aplicación de \_ contexto de ejecución de impresión \_**</span><span class="sxs-lookup"><span data-stu-id="9e833-107"><span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**PRINT\_EXECUTION\_CONTEXT\_APPLICATION**</span></span>
</dt> <dd>

<span data-ttu-id="9e833-108">El autor de la llamada se está ejecutando en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="9e833-108">The caller is running in an application.</span></span>

</dd> <dt>

<span data-ttu-id="9e833-109"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**\_servicio de \_ Administrador de \_ trabajos \_ de ejecución de impresión**</span><span class="sxs-lookup"><span data-stu-id="9e833-109"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**PRINT\_EXECUTION\_CONTEXT\_SPOOLER\_SERVICE**</span></span>
</dt> <dd>

<span data-ttu-id="9e833-110">El autor de la llamada se ejecuta en el servicio de cola de impresión (spoolsv.exe).</span><span class="sxs-lookup"><span data-stu-id="9e833-110">The caller is running in the spooler service (spoolsv.exe).</span></span>

</dd> <dt>

<span data-ttu-id="9e833-111"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**HOST de aislamiento de administrador de trabajos de impresión del \_ contexto de ejecución \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9e833-111"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**PRINT\_EXECUTION\_CONTEXT\_SPOOLER\_ISOLATION\_HOST**</span></span>
</dt> <dd>

<span data-ttu-id="9e833-112">El autor de la llamada se está ejecutando en el host de aislamiento de impresión (PrintIsolationHost.exe)</span><span class="sxs-lookup"><span data-stu-id="9e833-112">The caller is running in the print isolation host (PrintIsolationHost.exe)</span></span>

</dd> <dt>

<span data-ttu-id="9e833-113"><span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**\_ \_ \_ canalización de filtro de contexto de ejecución de impresión \_**</span><span class="sxs-lookup"><span data-stu-id="9e833-113"><span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**PRINT\_EXECUTION\_CONTEXT\_FILTER\_PIPELINE**</span></span>
</dt> <dd>

<span data-ttu-id="9e833-114">El autor de la llamada se está ejecutando en la canalización de filtros de impresión (printfilterpipelinesvc.exe)</span><span class="sxs-lookup"><span data-stu-id="9e833-114">The caller is running in the print filter pipeline (printfilterpipelinesvc.exe)</span></span>

</dd> <dt>

<span data-ttu-id="9e833-115"><span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**Contexto de ejecución de impresión \_ \_ \_ WOW64**</span><span class="sxs-lookup"><span data-stu-id="9e833-115"><span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**PRINT\_EXECUTION\_CONTEXT\_WOW64**</span></span>
</dt> <dd>

<span data-ttu-id="9e833-116">El autor de la llamada se ejecuta en splwow64.exe</span><span class="sxs-lookup"><span data-stu-id="9e833-116">The caller is running in splwow64.exe</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9e833-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e833-117">Requirements</span></span>



| <span data-ttu-id="9e833-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e833-118">Requirement</span></span> | <span data-ttu-id="9e833-119">Value</span><span class="sxs-lookup"><span data-stu-id="9e833-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e833-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e833-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9e833-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e833-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="9e833-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e833-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9e833-123">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e833-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="9e833-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e833-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e833-125"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e833-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e833-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e833-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e833-127">**GetPrintExecutionData**</span><span class="sxs-lookup"><span data-stu-id="9e833-127">**GetPrintExecutionData**</span></span>](getprintexecutiondata.md)
</dt> <dt>

[<span data-ttu-id="9e833-128">**IMPRIMIR \_ datos de ejecución \_**</span><span class="sxs-lookup"><span data-stu-id="9e833-128">**PRINT\_EXECUTION\_DATA**</span></span>](print-execution-data.md)
</dt> </dl>

 

 




