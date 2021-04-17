---
description: La función CCHeapSize devuelve el tamaño de la memoria asignada por la función CCHeapAlloc.
ms.assetid: 45d0fd89-bcd1-4298-8cc3-834d86301f93
title: Función CCHeapSize (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapSize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e184ae196253a66fc68f9066615b39c48f6921e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667740"
---
# <a name="ccheapsize-function"></a><span data-ttu-id="deccc-103">CCHeapSize función)</span><span class="sxs-lookup"><span data-stu-id="deccc-103">CCHeapSize function</span></span>

<span data-ttu-id="deccc-104">La función **CCHeapSize** devuelve el tamaño de la memoria asignada por la función **CCHeapAlloc** .</span><span class="sxs-lookup"><span data-stu-id="deccc-104">The **CCHeapSize** function returns the size of the memory allocated by the **CCHeapAlloc** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="deccc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="deccc-105">Syntax</span></span>


```C++
SIZE_T WINAPI CCHeapSize(
   LPVOID lpMem
);
```



## <a name="parameters"></a><span data-ttu-id="deccc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="deccc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deccc-107">*lpMem*</span><span class="sxs-lookup"><span data-stu-id="deccc-107">*lpMem*</span></span> 
</dt> <dd>

<span data-ttu-id="deccc-108">Puntero a la memoria asignada.</span><span class="sxs-lookup"><span data-stu-id="deccc-108">Pointer to the allocated memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deccc-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="deccc-109">Return value</span></span>

<span data-ttu-id="deccc-110">Si la función es correcta, el valor devuelto es el tamaño del bloque de memoria solicitado, medido en bytes.</span><span class="sxs-lookup"><span data-stu-id="deccc-110">If the function is successful, the return value is the size of the requested memory block   measured in bytes.</span></span>

<span data-ttu-id="deccc-111">Si la función no se realiza correctamente, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="deccc-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="deccc-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="deccc-112">Requirements</span></span>



| <span data-ttu-id="deccc-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="deccc-113">Requirement</span></span> | <span data-ttu-id="deccc-114">Value</span><span class="sxs-lookup"><span data-stu-id="deccc-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="deccc-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="deccc-115">Minimum supported client</span></span><br/> | <span data-ttu-id="deccc-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="deccc-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="deccc-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="deccc-117">Minimum supported server</span></span><br/> | <span data-ttu-id="deccc-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="deccc-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="deccc-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="deccc-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="deccc-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="deccc-120"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="deccc-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="deccc-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="deccc-122"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="deccc-122"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="deccc-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="deccc-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="deccc-124"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="deccc-124"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="deccc-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="deccc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deccc-126">SetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="deccc-126">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="deccc-127">GetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="deccc-127">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="deccc-128">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="deccc-128">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="deccc-129">CCHeapFree</span><span class="sxs-lookup"><span data-stu-id="deccc-129">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="deccc-130">CCHeapReAlloc</span><span class="sxs-lookup"><span data-stu-id="deccc-130">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> </dl>

 

 




