---
description: La función CCHeapFree libera la memoria asignada por la función CCHeapAlloc.
ms.assetid: 4e1f3332-b0cb-4c21-8c36-59e14c9686cd
title: Función CCHeapFree (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapFree
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5e89ca9a7d00559724edc6679a0ed99e4bdf9c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156705"
---
# <a name="ccheapfree-function"></a><span data-ttu-id="949b3-103">CCHeapFree función)</span><span class="sxs-lookup"><span data-stu-id="949b3-103">CCHeapFree function</span></span>

<span data-ttu-id="949b3-104">La función **CCHeapFree** libera la memoria asignada por la función **CCHeapAlloc** .</span><span class="sxs-lookup"><span data-stu-id="949b3-104">The **CCHeapFree** function releases the memory allocated by the **CCHeapAlloc** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="949b3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="949b3-105">Syntax</span></span>


```C++
BOOL WINAPI CCHeapFree(
   LPVOID lpMem
);
```



## <a name="parameters"></a><span data-ttu-id="949b3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="949b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="949b3-107">*lpMem*</span><span class="sxs-lookup"><span data-stu-id="949b3-107">*lpMem*</span></span> 
</dt> <dd>

<span data-ttu-id="949b3-108">Puntero a la memoria que esta función libera.</span><span class="sxs-lookup"><span data-stu-id="949b3-108">Pointer to the memory that this function releases.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="949b3-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="949b3-109">Return value</span></span>

<span data-ttu-id="949b3-110">Si la función **CCHeapFree** es correcta, el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="949b3-110">If the **CCHeapFree** function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="949b3-111">Si la función no se realiza correctamente, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="949b3-111">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="949b3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="949b3-112">Requirements</span></span>



| <span data-ttu-id="949b3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="949b3-113">Requirement</span></span> | <span data-ttu-id="949b3-114">Value</span><span class="sxs-lookup"><span data-stu-id="949b3-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="949b3-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="949b3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="949b3-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="949b3-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="949b3-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="949b3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="949b3-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="949b3-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="949b3-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="949b3-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="949b3-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="949b3-120"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="949b3-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="949b3-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="949b3-122"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="949b3-122"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="949b3-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="949b3-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="949b3-124"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="949b3-124"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="949b3-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="949b3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="949b3-126">SetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="949b3-126">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="949b3-127">GetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="949b3-127">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="949b3-128">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="949b3-128">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="949b3-129">CCHeapReAlloc</span><span class="sxs-lookup"><span data-stu-id="949b3-129">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="949b3-130">CCHeapSize</span><span class="sxs-lookup"><span data-stu-id="949b3-130">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




