---
description: GetPrintExecutionData recupera el contexto de impresión actual.
ms.assetid: bb9506aa-a0da-46bc-a86a-84a79587cd50
title: Función GetPrintExecutionData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintExecutionData
api_type:
- DllExport
api_location:
- winspool.drv
ms.openlocfilehash: a1b2f2674c9ef186338c91ed2e4500d8408964d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697695"
---
# <a name="getprintexecutiondata-function"></a><span data-ttu-id="588f6-103">GetPrintExecutionData función)</span><span class="sxs-lookup"><span data-stu-id="588f6-103">GetPrintExecutionData function</span></span>

<span data-ttu-id="588f6-104">**GetPrintExecutionData** recupera el contexto de impresión actual.</span><span class="sxs-lookup"><span data-stu-id="588f6-104">The **GetPrintExecutionData** retrieves the current print context.</span></span>

> [!Note]  
> <span data-ttu-id="588f6-105">Esta función está pensada para que la usen los controladores de impresora que se ejecutan en el contexto del administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="588f6-105">This function is intended for use by printer drivers that are running in the context of the print spooler.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="588f6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="588f6-106">Syntax</span></span>


```C++
BOOL WINAPI GetPrintExecutionData(
  _Out_ PRINT_EXECUTION_DATA *pData
);
```



## <a name="parameters"></a><span data-ttu-id="588f6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="588f6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="588f6-108">*pdata* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="588f6-108">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="588f6-109">Puntero a una variable que recibe la dirección de la estructura [**de \_ \_ datos**](print-execution-data.md) de la ejecución de impresión.</span><span class="sxs-lookup"><span data-stu-id="588f6-109">A pointer to a variable that receives the address of the [**PRINT\_EXECUTION\_DATA**](print-execution-data.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="588f6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="588f6-110">Return value</span></span>

<span data-ttu-id="588f6-111">Devuelve **true** si la función se ejecuta correctamente; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="588f6-111">Returns **TRUE** if the function succeeds; otherwise **FALSE**.</span></span> <span data-ttu-id="588f6-112">Si el valor devuelto es **false**, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener el estado de error.</span><span class="sxs-lookup"><span data-stu-id="588f6-112">If the return value is **FALSE**, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="588f6-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="588f6-113">Remarks</span></span>

<span data-ttu-id="588f6-114">Los controladores de impresora deben llamar a [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) en el módulo winspool. drv para obtener la dirección de la función **GetPrintExecutionData** porque **GetPrintExecutionData** no se admite en Windows Vista o en versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="588f6-114">Printer drivers should call [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) on the winspool.drv module to get the address of the **GetPrintExecutionData** function because **GetPrintExecutionData** is not supported on Windows Vista or earlier versions of Windows.</span></span>

<span data-ttu-id="588f6-115">**GetPrintExecutionData** solo produce un error si el valor de *pdata* es **null**.</span><span class="sxs-lookup"><span data-stu-id="588f6-115">**GetPrintExecutionData** only fails if the value of *pData* is **NULL**.</span></span>

<span data-ttu-id="588f6-116">El valor del miembro **clientAppPID** de los [**\_ \_ datos de ejecución de impresión**](print-execution-data.md) solo es significativo si el valor de **Context** es el **contexto de ejecución de impresión \_ \_ \_ WOW64**.</span><span class="sxs-lookup"><span data-stu-id="588f6-116">The value of the **clientAppPID** member of [**PRINT\_EXECUTION\_DATA**](print-execution-data.md) is only meaningful if the value of **context** is **PRINT\_EXECUTION\_CONTEXT\_WOW64**.</span></span> <span data-ttu-id="588f6-117">Si el valor de **Context** no es el **contexto de ejecución de impresión \_ \_ \_ WOW64**, el valor de **clientAppPID** es 0.</span><span class="sxs-lookup"><span data-stu-id="588f6-117">If the value of **context** is not **PRINT\_EXECUTION\_CONTEXT\_WOW64**, the value of **clientAppPID** is 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="588f6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="588f6-118">Requirements</span></span>



| <span data-ttu-id="588f6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="588f6-119">Requirement</span></span> | <span data-ttu-id="588f6-120">Value</span><span class="sxs-lookup"><span data-stu-id="588f6-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="588f6-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="588f6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="588f6-122">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="588f6-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="588f6-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="588f6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="588f6-124">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="588f6-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="588f6-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="588f6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="588f6-126"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="588f6-126"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="588f6-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="588f6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="588f6-128"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="588f6-128"><dt>Winspool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="588f6-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="588f6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="588f6-130">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="588f6-130">**GetLastError**</span></span>](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="588f6-131">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="588f6-131">**GetProcAddress**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="588f6-132">**\_contexto de ejecución de impresión \_**</span><span class="sxs-lookup"><span data-stu-id="588f6-132">**PRINT\_EXECUTION\_CONTEXT**</span></span>](print-execution-context.md)
</dt> <dt>

[<span data-ttu-id="588f6-133">**IMPRIMIR \_ datos de ejecución \_**</span><span class="sxs-lookup"><span data-stu-id="588f6-133">**PRINT\_EXECUTION\_DATA**</span></span>](print-execution-data.md)
</dt> </dl>

 

