---
description: Libera un bloque de memoria que se ha asignado desde un montón mediante RtlAllocateHeap.
ms.assetid: 0A08FB6B-23A3-450B-8745-AEB927CEB7BB
title: Función RtlFreeHeap (Ntifs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlFreeHeap
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: e51994c4bcd941bc96575eb3fdbb45d4111c1aeb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538842"
---
# <a name="rtlfreeheap-function"></a><span data-ttu-id="84b5a-103">RtlFreeHeap función)</span><span class="sxs-lookup"><span data-stu-id="84b5a-103">RtlFreeHeap function</span></span>

<span data-ttu-id="84b5a-104">Libera un bloque de memoria que se ha asignado desde un montón mediante [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span><span class="sxs-lookup"><span data-stu-id="84b5a-104">Frees a memory block that was allocated from a heap by [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span></span>

## <a name="syntax"></a><span data-ttu-id="84b5a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84b5a-105">Syntax</span></span>


```C++
BOOLEAN RtlFreeHeap(
  _In_     PVOID HeapHandle,
  _In_opt_ ULONG Flags,
  _In_     PVOID HeapBase
);
```



## <a name="parameters"></a><span data-ttu-id="84b5a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84b5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84b5a-107">*HeapHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84b5a-107">*HeapHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84b5a-108">Identificador del montón cuyo bloque de memoria se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="84b5a-108">A handle for the heap whose memory block is to be freed.</span></span> <span data-ttu-id="84b5a-109">Este parámetro es un identificador devuelto por [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span><span class="sxs-lookup"><span data-stu-id="84b5a-109">This parameter is a handle returned by [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span></span>

</dd> <dt>

<span data-ttu-id="84b5a-110">*Marcas* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="84b5a-110">*Flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="84b5a-111">Conjunto de marcas que controla aspectos de liberar un bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="84b5a-111">A set of flags that controls aspects of freeing a memory block.</span></span> <span data-ttu-id="84b5a-112">Si se especifica el valor siguiente, se invalida el valor correspondiente que se especificó en el parámetro *Flags* cuando [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)creó el montón.</span><span class="sxs-lookup"><span data-stu-id="84b5a-112">Specifying the following value overrides the corresponding value that was specified in the *Flags* parameter when the heap was created by [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span></span>



| <span data-ttu-id="84b5a-113">Marca</span><span class="sxs-lookup"><span data-stu-id="84b5a-113">Flag</span></span>                           | <span data-ttu-id="84b5a-114">Significado</span><span class="sxs-lookup"><span data-stu-id="84b5a-114">Meaning</span></span>                                                                                   |
|--------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="84b5a-115">MONTÓN \_ no \_ SERIALIZE</span><span class="sxs-lookup"><span data-stu-id="84b5a-115">HEAP\_NO\_SERIALIZE</span></span><br/> | <span data-ttu-id="84b5a-116">La exclusión mutua no se utilizará cuando **RtlFreeHeap** tenga acceso al montón.</span><span class="sxs-lookup"><span data-stu-id="84b5a-116">Mutual exclusion will not be used when **RtlFreeHeap** is accessing the heap.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="84b5a-117">*HeapBase* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84b5a-117">*HeapBase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84b5a-118">Puntero al bloque de memoria que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="84b5a-118">A pointer to the memory block to free.</span></span> <span data-ttu-id="84b5a-119">[**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)devuelve este puntero.</span><span class="sxs-lookup"><span data-stu-id="84b5a-119">This pointer is returned by [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84b5a-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84b5a-120">Return value</span></span>

<span data-ttu-id="84b5a-121">Devuelve **true** si el bloque se liberó correctamente; De lo contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="84b5a-121">Returns **TRUE** if the block was freed successfully; **FALSE** otherwise.</span></span>

> [!Note]  
> <span data-ttu-id="84b5a-122">A partir de Windows 8, el valor devuelto se escribe como **lógico**, que tiene un tamaño diferente que el **booleano**.</span><span class="sxs-lookup"><span data-stu-id="84b5a-122">Starting with Windows 8 the return value is typed as **LOGICAL**, which has a different size than **BOOLEAN**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="84b5a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84b5a-123">Requirements</span></span>



| <span data-ttu-id="84b5a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="84b5a-124">Requirement</span></span> | <span data-ttu-id="84b5a-125">Value</span><span class="sxs-lookup"><span data-stu-id="84b5a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84b5a-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84b5a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="84b5a-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="84b5a-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="84b5a-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84b5a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="84b5a-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="84b5a-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="84b5a-130">Plataforma de destino</span><span class="sxs-lookup"><span data-stu-id="84b5a-130">Target platform</span></span><br/>          | <dl> <span data-ttu-id="84b5a-131"><dt>[Mundo](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="84b5a-131"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="84b5a-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84b5a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="84b5a-133"><dt>Ntifs. h (incluye Ntifs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="84b5a-133"><dt>Ntifs.h (include Ntifs.h)</dt></span></span> </dl>                                    |
| <span data-ttu-id="84b5a-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="84b5a-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="84b5a-135"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="84b5a-135"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="84b5a-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="84b5a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84b5a-137"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84b5a-137"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="84b5a-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="84b5a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84b5a-139">**RtlAllocateHeap**</span><span class="sxs-lookup"><span data-stu-id="84b5a-139">**RtlAllocateHeap**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)
</dt> <dt>

[<span data-ttu-id="84b5a-140">**RtlCreateHeap**</span><span class="sxs-lookup"><span data-stu-id="84b5a-140">**RtlCreateHeap**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)
</dt> <dt>

[<span data-ttu-id="84b5a-141">**RtlDestroyHeap**</span><span class="sxs-lookup"><span data-stu-id="84b5a-141">**RtlDestroyHeap**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtldestroyheap)
</dt> </dl>

 

 
