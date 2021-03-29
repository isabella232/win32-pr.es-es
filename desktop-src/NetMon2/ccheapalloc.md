---
description: La función CCHeapAlloc asigna memoria en función de la captura.
ms.assetid: 6403c35f-d78f-48dc-90cc-0b76260bbab7
title: Función CCHeapAlloc (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 14fce9f56103803e575d295799a5c5971ed1c459
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909417"
---
# <a name="ccheapalloc-function"></a><span data-ttu-id="57b8f-103">CCHeapAlloc función)</span><span class="sxs-lookup"><span data-stu-id="57b8f-103">CCHeapAlloc function</span></span>

<span data-ttu-id="57b8f-104">La función **CCHeapAlloc** asigna memoria en función de la captura.</span><span class="sxs-lookup"><span data-stu-id="57b8f-104">The **CCHeapAlloc** function allocates memory on a capture-by-capture basis.</span></span>

## <a name="syntax"></a><span data-ttu-id="57b8f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57b8f-105">Syntax</span></span>


```C++
LPVOID WINAPI CCHeapAlloc(
   DWORD dwBytes,
   BOOL  bZeroInit
);
```



## <a name="parameters"></a><span data-ttu-id="57b8f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57b8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57b8f-107">*dwBytes*</span><span class="sxs-lookup"><span data-stu-id="57b8f-107">*dwBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="57b8f-108">Longitud de memoria solicitada asignada.</span><span class="sxs-lookup"><span data-stu-id="57b8f-108">Requested length of memory allocated.</span></span>

</dd> <dt>

<span data-ttu-id="57b8f-109">*bZeroInit*</span><span class="sxs-lookup"><span data-stu-id="57b8f-109">*bZeroInit*</span></span> 
</dt> <dd>

<span data-ttu-id="57b8f-110">Indicador de si se inicializó la memoria asignada.</span><span class="sxs-lookup"><span data-stu-id="57b8f-110">Indicator of whether allocated memory was initialized.</span></span> <span data-ttu-id="57b8f-111">Si el valor del parámetro es **true**, la memoria asignada se inicializa en cero.</span><span class="sxs-lookup"><span data-stu-id="57b8f-111">If the parameter value is **TRUE**, the allocated memory initializes to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57b8f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57b8f-112">Return value</span></span>

<span data-ttu-id="57b8f-113">Si la función se realiza correctamente, el valor devuelto es un puntero a la memoria asignada.</span><span class="sxs-lookup"><span data-stu-id="57b8f-113">If the function is successful, the return value is a pointer to the allocated memory.</span></span> <span data-ttu-id="57b8f-114">Cuando haya terminado de usar la memoria asignada, libere la memoria mediante una llamada a la función [**CCHeapFree**](ccheapfree.md) .</span><span class="sxs-lookup"><span data-stu-id="57b8f-114">When you have finished using the allocated memory, free the memory by calling the [**CCHeapFree**](ccheapfree.md) function.</span></span>

<span data-ttu-id="57b8f-115">Si la función no se realiza correctamente, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="57b8f-115">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="57b8f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57b8f-116">Requirements</span></span>



| <span data-ttu-id="57b8f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="57b8f-117">Requirement</span></span> | <span data-ttu-id="57b8f-118">Value</span><span class="sxs-lookup"><span data-stu-id="57b8f-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="57b8f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57b8f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="57b8f-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="57b8f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="57b8f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57b8f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="57b8f-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="57b8f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="57b8f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57b8f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="57b8f-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="57b8f-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="57b8f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="57b8f-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="57b8f-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57b8f-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="57b8f-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="57b8f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57b8f-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57b8f-128"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57b8f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="57b8f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57b8f-130">**SetCCInstPtr**</span><span class="sxs-lookup"><span data-stu-id="57b8f-130">**SetCCInstPtr**</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="57b8f-131">**GetCCInstPtr**</span><span class="sxs-lookup"><span data-stu-id="57b8f-131">**GetCCInstPtr**</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="57b8f-132">**CCHeapFree**</span><span class="sxs-lookup"><span data-stu-id="57b8f-132">**CCHeapFree**</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="57b8f-133">**CCHeapReAlloc**</span><span class="sxs-lookup"><span data-stu-id="57b8f-133">**CCHeapReAlloc**</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="57b8f-134">**CCHeapSize**</span><span class="sxs-lookup"><span data-stu-id="57b8f-134">**CCHeapSize**</span></span>](ccheapsize.md)
</dt> </dl>

 

 




