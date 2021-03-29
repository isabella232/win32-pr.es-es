---
description: La función CCHeapReAlloc reasigna la memoria asignada por la función CCHeapAlloc.
ms.assetid: 82365ce2-3980-44ff-be0f-062a65f676fc
title: Función CCHeapReAlloc (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapReAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e1619e2e6e81e8a265600f8437a6633e18065f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813627"
---
# <a name="ccheaprealloc-function"></a><span data-ttu-id="3b60a-103">CCHeapReAlloc función)</span><span class="sxs-lookup"><span data-stu-id="3b60a-103">CCHeapReAlloc function</span></span>

<span data-ttu-id="3b60a-104">La función **CCHeapReAlloc** reasigna la memoria asignada por la función **CCHeapAlloc** .</span><span class="sxs-lookup"><span data-stu-id="3b60a-104">The **CCHeapReAlloc** function reallocates memory allocated by the **CCHeapAlloc** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b60a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b60a-105">Syntax</span></span>


```C++
LPVOID WINAPI CCHeapReAlloc(
   LPVOID lpMem,
   DWORD  dwBytes,
   BOOL   bZeroInit
);
```



## <a name="parameters"></a><span data-ttu-id="3b60a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b60a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b60a-107">*lpMem*</span><span class="sxs-lookup"><span data-stu-id="3b60a-107">*lpMem*</span></span> 
</dt> <dd>

<span data-ttu-id="3b60a-108">Puntero a la memoria asignada original.</span><span class="sxs-lookup"><span data-stu-id="3b60a-108">Pointer to the original allocated memory.</span></span>

</dd> <dt>

<span data-ttu-id="3b60a-109">*dwBytes*</span><span class="sxs-lookup"><span data-stu-id="3b60a-109">*dwBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="3b60a-110">Tamaño de la memoria reasignada, medido en bytes.</span><span class="sxs-lookup"><span data-stu-id="3b60a-110">Size of the reallocated memory, measured in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3b60a-111">*bZeroInit*</span><span class="sxs-lookup"><span data-stu-id="3b60a-111">*bZeroInit*</span></span> 
</dt> <dd>

<span data-ttu-id="3b60a-112">Indicador de si se inicializó la memoria reasignada.</span><span class="sxs-lookup"><span data-stu-id="3b60a-112">Indicator of whether reallocated memory was initialized.</span></span> <span data-ttu-id="3b60a-113">Si el valor del parámetro es **true**, la memoria recién reasignada se inicializa en cero.</span><span class="sxs-lookup"><span data-stu-id="3b60a-113">If the parameter value is **TRUE**, the newly reallocated memory initializes to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b60a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b60a-114">Return value</span></span>

<span data-ttu-id="3b60a-115">Si la función se realiza correctamente, el valor devuelto es un puntero a la memoria reasignada.</span><span class="sxs-lookup"><span data-stu-id="3b60a-115">If the function is successful, the return value is a pointer to the reallocated memory.</span></span>

<span data-ttu-id="3b60a-116">Si la función no se realiza correctamente, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="3b60a-116">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b60a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b60a-117">Requirements</span></span>



| <span data-ttu-id="3b60a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b60a-118">Requirement</span></span> | <span data-ttu-id="3b60a-119">Value</span><span class="sxs-lookup"><span data-stu-id="3b60a-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3b60a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b60a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3b60a-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3b60a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3b60a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b60a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3b60a-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3b60a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3b60a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b60a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b60a-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b60a-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="3b60a-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b60a-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="3b60a-127"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b60a-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="3b60a-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b60a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b60a-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b60a-129"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b60a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b60a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b60a-131">SetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="3b60a-131">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="3b60a-132">GetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="3b60a-132">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="3b60a-133">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="3b60a-133">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="3b60a-134">CCHeapFree</span><span class="sxs-lookup"><span data-stu-id="3b60a-134">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="3b60a-135">CCHeapSize</span><span class="sxs-lookup"><span data-stu-id="3b60a-135">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




