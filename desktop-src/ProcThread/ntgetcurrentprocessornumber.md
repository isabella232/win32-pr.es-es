---
description: Recupera el número del procesador en el que se estaba ejecutando el subproceso actual durante la llamada a esta función.
ms.assetid: f0141550-58e2-421a-934d-9a6c488d2b81
title: NtGetCurrentProcessorNumber función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGetCurrentProcessorNumber
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 96862836d3f9c16034ce1c2e751aebea2884d114
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681001"
---
# <a name="ntgetcurrentprocessornumber-function"></a><span data-ttu-id="c7897-103">NtGetCurrentProcessorNumber función)</span><span class="sxs-lookup"><span data-stu-id="c7897-103">NtGetCurrentProcessorNumber function</span></span>

<span data-ttu-id="c7897-104">\[**NtGetCurrentProcessorNumber** puede modificarse o no estar disponible en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="c7897-104">\[**NtGetCurrentProcessorNumber** may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="c7897-105">En su lugar, las aplicaciones deben usar la función [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) .\]</span><span class="sxs-lookup"><span data-stu-id="c7897-105">Applications should use the [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) function instead.\]</span></span>

<span data-ttu-id="c7897-106">Recupera el número del procesador en el que se estaba ejecutando el subproceso actual durante la llamada a esta función.</span><span class="sxs-lookup"><span data-stu-id="c7897-106">Retrieves the number of the processor the current thread was running on during the call to this function.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7897-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7897-107">Syntax</span></span>


```C++
ULONG WINAPI NtGetCurrentProcessorNumber(void);
```



## <a name="parameters"></a><span data-ttu-id="c7897-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7897-108">Parameters</span></span>

<span data-ttu-id="c7897-109">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c7897-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c7897-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7897-110">Return value</span></span>

<span data-ttu-id="c7897-111">La función devuelve el número de procesador actual.</span><span class="sxs-lookup"><span data-stu-id="c7897-111">The function returns the current processor number.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7897-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7897-112">Remarks</span></span>

<span data-ttu-id="c7897-113">Esta función se usa para proporcionar información para calcular el rendimiento de los procesos.</span><span class="sxs-lookup"><span data-stu-id="c7897-113">This function is used to provide information for estimating process performance.</span></span>

<span data-ttu-id="c7897-114">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="c7897-114">This function has no associated import library.</span></span> <span data-ttu-id="c7897-115">Debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="c7897-115">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7897-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7897-116">Requirements</span></span>



| <span data-ttu-id="c7897-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7897-117">Requirement</span></span> | <span data-ttu-id="c7897-118">Value</span><span class="sxs-lookup"><span data-stu-id="c7897-118">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c7897-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c7897-119">DLL</span></span><br/> | <dl> <span data-ttu-id="c7897-120"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7897-120"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7897-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7897-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7897-122">Varios procesadores</span><span class="sxs-lookup"><span data-stu-id="c7897-122">Multiple Processors</span></span>](multiple-processors.md)
</dt> <dt>

[<span data-ttu-id="c7897-123">Funciones de proceso y subproceso</span><span class="sxs-lookup"><span data-stu-id="c7897-123">Process and Thread Functions</span></span>](process-and-thread-functions.md)
</dt> <dt>

[<span data-ttu-id="c7897-124">Procesos</span><span class="sxs-lookup"><span data-stu-id="c7897-124">Processes</span></span>](child-processes.md)
</dt> </dl>

 

 
