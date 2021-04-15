---
title: Función FreeRepairInfoExs (Ndattributils. h)
description: Desasigna la memoria asignada internamente a una matriz de estructuras RepairInfoEx.
ms.assetid: b4e3e758-88cd-4ce2-b1a4-5b47889aae9b
keywords:
- FreeRepairInfoExs función NDF
topic_type:
- apiref
api_name:
- FreeRepairInfoExs
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 094c745486526caa870a500019de3aa819b6fe5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534312"
---
# <a name="freerepairinfoexs-function"></a><span data-ttu-id="d992c-104">FreeRepairInfoExs función)</span><span class="sxs-lookup"><span data-stu-id="d992c-104">FreeRepairInfoExs function</span></span>

<span data-ttu-id="d992c-105">La función **FreeRepairInfoExs** desasigna la memoria asignada internamente a una matriz de estructuras [**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) .</span><span class="sxs-lookup"><span data-stu-id="d992c-105">The **FreeRepairInfoExs** function deallocates the memory allocated internally to an array of [**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) structures.</span></span> <span data-ttu-id="d992c-106">Esta función llama a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para desasignar memoria.</span><span class="sxs-lookup"><span data-stu-id="d992c-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="d992c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d992c-107">Syntax</span></span>


```C++
VOID FreeRepairInfoExs(
  _In_ RepairInfoEx *pInfo,
       ULONG        RepairCount,
       BOOL         bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="d992c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d992c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d992c-109">*Pinfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d992c-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d992c-110">Tipo: \**[**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) \** _</span><span class="sxs-lookup"><span data-stu-id="d992c-110">Type: \**[**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)\** _</span></span>

<span data-ttu-id="d992c-111">Matriz de estructuras.</span><span class="sxs-lookup"><span data-stu-id="d992c-111">The array of structures.</span></span> <span data-ttu-id="d992c-112">La memoria asignada a la que apuntan estas estructuras se liberará.</span><span class="sxs-lookup"><span data-stu-id="d992c-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="d992c-113">_RepairCount \*</span><span class="sxs-lookup"><span data-stu-id="d992c-113">_RepairCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="d992c-114">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="d992c-114">Type: **ULONG**</span></span>

<span data-ttu-id="d992c-115">El número de estructuras de la matriz a las que apunta *Pinfo*.</span><span class="sxs-lookup"><span data-stu-id="d992c-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="d992c-116">*bFreePointer*</span><span class="sxs-lookup"><span data-stu-id="d992c-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="d992c-117">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="d992c-117">Type: **BOOL**</span></span>

<span data-ttu-id="d992c-118">True si también se debe eliminar la matriz de estructuras; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="d992c-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d992c-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d992c-119">Return value</span></span>

<span data-ttu-id="d992c-120">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d992c-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d992c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d992c-121">Requirements</span></span>



| <span data-ttu-id="d992c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d992c-122">Requirement</span></span> | <span data-ttu-id="d992c-123">Value</span><span class="sxs-lookup"><span data-stu-id="d992c-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d992c-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d992c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d992c-125">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d992c-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d992c-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d992c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d992c-127">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d992c-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d992c-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d992c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d992c-129"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="d992c-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d992c-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d992c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d992c-131">**RepairInfoEx**</span><span class="sxs-lookup"><span data-stu-id="d992c-131">**RepairInfoEx**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)
</dt> <dt>

[<span data-ttu-id="d992c-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="d992c-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

