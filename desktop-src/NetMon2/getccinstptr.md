---
description: La función GetCCInstPtr devuelve el puntero a los datos de instancia agregados al contexto de captura.
ms.assetid: 6fb103d3-583b-4460-8b9a-ff921751b0eb
title: Función GetCCInstPtr (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2f078e91829b5324218b901e41e000d37b4cd6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808719"
---
# <a name="getccinstptr-function"></a><span data-ttu-id="e02a3-103">GetCCInstPtr función)</span><span class="sxs-lookup"><span data-stu-id="e02a3-103">GetCCInstPtr function</span></span>

<span data-ttu-id="e02a3-104">La función **GetCCInstPtr** devuelve el puntero a los datos de instancia agregados al contexto de captura.</span><span class="sxs-lookup"><span data-stu-id="e02a3-104">The **GetCCInstPtr** function returns the pointer to the instance data added to the capture context.</span></span>

## <a name="syntax"></a><span data-ttu-id="e02a3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e02a3-105">Syntax</span></span>


```C++
LPVOID WINAPI GetCCInstPtr(void);
```



## <a name="parameters"></a><span data-ttu-id="e02a3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e02a3-106">Parameters</span></span>

<span data-ttu-id="e02a3-107">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e02a3-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e02a3-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e02a3-108">Return value</span></span>

<span data-ttu-id="e02a3-109">Si la función se realiza correctamente, el valor devuelto es un puntero a los datos de instancia de una captura específica.</span><span class="sxs-lookup"><span data-stu-id="e02a3-109">If the function is successful, the return value is a pointer to the instance data of a specific capture.</span></span>

<span data-ttu-id="e02a3-110">Si la función no se realiza correctamente, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="e02a3-110">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e02a3-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e02a3-111">Requirements</span></span>



| <span data-ttu-id="e02a3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e02a3-112">Requirement</span></span> | <span data-ttu-id="e02a3-113">Value</span><span class="sxs-lookup"><span data-stu-id="e02a3-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e02a3-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e02a3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e02a3-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e02a3-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e02a3-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e02a3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e02a3-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e02a3-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e02a3-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e02a3-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e02a3-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e02a3-119"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="e02a3-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e02a3-120">Library</span></span><br/>                  | <dl> <span data-ttu-id="e02a3-121"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e02a3-121"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e02a3-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e02a3-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e02a3-123"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e02a3-123"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e02a3-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e02a3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e02a3-125">SetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="e02a3-125">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="e02a3-126">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="e02a3-126">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="e02a3-127">CCHeapFree</span><span class="sxs-lookup"><span data-stu-id="e02a3-127">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="e02a3-128">CCHeapReAlloc</span><span class="sxs-lookup"><span data-stu-id="e02a3-128">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="e02a3-129">CCHeapSize</span><span class="sxs-lookup"><span data-stu-id="e02a3-129">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




