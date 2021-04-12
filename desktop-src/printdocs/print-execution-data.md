---
description: Contiene el contexto de ejecución del controlador de impresora que llama a GetPrintExecutionData.
ms.assetid: 1fd25ed9-6f28-48f9-8132-d48fffc956ec
title: Estructura de PRINT_EXECUTION_DATA (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_DATA
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0e33f77a3140c62a1f472fc27948ec26a7ecf3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278197"
---
# <a name="print_execution_data-structure"></a><span data-ttu-id="5d0bd-103">Estructura de datos de \_ ejecución de impresión \_</span><span class="sxs-lookup"><span data-stu-id="5d0bd-103">PRINT\_EXECUTION\_DATA structure</span></span>

<span data-ttu-id="5d0bd-104">Contiene el contexto de ejecución del controlador de impresora que llama a [**GetPrintExecutionData**](getprintexecutiondata.md).</span><span class="sxs-lookup"><span data-stu-id="5d0bd-104">Contains the execution context of the printer driver that calls [**GetPrintExecutionData**](getprintexecutiondata.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5d0bd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d0bd-105">Syntax</span></span>


```C++
typedef struct _PRINT_EXECUTION_DATA {
  PRINT_EXECUTION_CONTEXT  context;
  DWORD                    clientAppPID;
} PRINT_EXECUTION_DATA;
```



## <a name="members"></a><span data-ttu-id="5d0bd-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="5d0bd-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5d0bd-107">**contextoo**</span><span class="sxs-lookup"><span data-stu-id="5d0bd-107">**context**</span></span>
</dt> <dd>

<span data-ttu-id="5d0bd-108">Valor [**del \_ \_ contexto de ejecución de impresión**](print-execution-context.md) que representa el contexto de ejecución actual del controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="5d0bd-108">The [**PRINT\_EXECUTION\_CONTEXT**](print-execution-context.md) value that represents the current execution context of the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="5d0bd-109">**clientAppPID**</span><span class="sxs-lookup"><span data-stu-id="5d0bd-109">**clientAppPID**</span></span>
</dt> <dd>

<span data-ttu-id="5d0bd-110">Si el valor de **Context** es el **contexto de ejecución de impresión \_ \_ \_ WOW64**, **clientAppPID** identifica la aplicación cliente en cuyo nombre el proceso de splwow64.exe cargó el controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="5d0bd-110">If the value of **context** is **PRINT\_EXECUTION\_CONTEXT\_WOW64**, **clientAppPID** identifies the client application on whose behalf the splwow64.exe process loaded the printer driver.</span></span> <span data-ttu-id="5d0bd-111">Si el valor de **Context** no es el **contexto de ejecución de impresión \_ \_ \_ WOW64**, **clientAppPID** es cero.</span><span class="sxs-lookup"><span data-stu-id="5d0bd-111">If the value of **context** is not **PRINT\_EXECUTION\_CONTEXT\_WOW64**, **clientAppPID** is zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d0bd-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d0bd-112">Requirements</span></span>



| <span data-ttu-id="5d0bd-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d0bd-113">Requirement</span></span> | <span data-ttu-id="5d0bd-114">Value</span><span class="sxs-lookup"><span data-stu-id="5d0bd-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d0bd-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d0bd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5d0bd-116">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="5d0bd-116">Windows 7 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="5d0bd-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d0bd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5d0bd-118">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5d0bd-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="5d0bd-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d0bd-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d0bd-120"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d0bd-120"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d0bd-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d0bd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d0bd-122">**GetPrintExecutionData**</span><span class="sxs-lookup"><span data-stu-id="5d0bd-122">**GetPrintExecutionData**</span></span>](getprintexecutiondata.md)
</dt> <dt>

[<span data-ttu-id="5d0bd-123">**\_contexto de ejecución de impresión \_**</span><span class="sxs-lookup"><span data-stu-id="5d0bd-123">**PRINT\_EXECUTION\_CONTEXT**</span></span>](print-execution-context.md)
</dt> </dl>

 

 




