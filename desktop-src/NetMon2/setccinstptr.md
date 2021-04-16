---
description: La función SetCCInstPtr captura un puntero de instancia de contexto.
ms.assetid: 31924608-4aa1-4801-a5de-d8de054e12d9
title: Función SetCCInstPtr (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 323e6334c90358dd8725f3f9092142275cfe491a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542363"
---
# <a name="setccinstptr-function"></a><span data-ttu-id="a87b2-103">SetCCInstPtr función)</span><span class="sxs-lookup"><span data-stu-id="a87b2-103">SetCCInstPtr function</span></span>

<span data-ttu-id="a87b2-104">La función **SetCCInstPtr** captura un puntero de instancia de contexto.</span><span class="sxs-lookup"><span data-stu-id="a87b2-104">The **SetCCInstPtr** function captures a context instance pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a87b2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a87b2-105">Syntax</span></span>


```C++
VOID WINAPI SetCCInstPtr(
   LPVOID lpCurCaptureInst
);
```



## <a name="parameters"></a><span data-ttu-id="a87b2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a87b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a87b2-107">*lpCurCaptureInst*</span><span class="sxs-lookup"><span data-stu-id="a87b2-107">*lpCurCaptureInst*</span></span> 
</dt> <dd>

<span data-ttu-id="a87b2-108">Puntero a los datos de instancia agregados a la captura.</span><span class="sxs-lookup"><span data-stu-id="a87b2-108">Pointer to the instance data added to the capture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a87b2-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a87b2-109">Return value</span></span>

<span data-ttu-id="a87b2-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a87b2-110">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="a87b2-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a87b2-111">Remarks</span></span>

<span data-ttu-id="a87b2-112">Use esta función para almacenar un puntero a un bloque que se asignó con la función **CCHeapAlloc** .</span><span class="sxs-lookup"><span data-stu-id="a87b2-112">Use this function to store a pointer to a block that was allocated with the **CCHeapAlloc** function.</span></span> <span data-ttu-id="a87b2-113">Cada analizador puede establecer una única instancia de datos en una captura.</span><span class="sxs-lookup"><span data-stu-id="a87b2-113">Each parser can set a single instance of data on a capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="a87b2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a87b2-114">Requirements</span></span>



| <span data-ttu-id="a87b2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a87b2-115">Requirement</span></span> | <span data-ttu-id="a87b2-116">Value</span><span class="sxs-lookup"><span data-stu-id="a87b2-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a87b2-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a87b2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a87b2-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a87b2-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a87b2-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a87b2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a87b2-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a87b2-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a87b2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a87b2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a87b2-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a87b2-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="a87b2-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a87b2-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="a87b2-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a87b2-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a87b2-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a87b2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a87b2-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a87b2-126"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a87b2-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a87b2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a87b2-128">GetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="a87b2-128">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="a87b2-129">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="a87b2-129">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="a87b2-130">CCHeapFree</span><span class="sxs-lookup"><span data-stu-id="a87b2-130">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="a87b2-131">CCHeapReAlloc</span><span class="sxs-lookup"><span data-stu-id="a87b2-131">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="a87b2-132">CCHeapSize</span><span class="sxs-lookup"><span data-stu-id="a87b2-132">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




