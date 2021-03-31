---
title: Función FreeRepairInfos (Ndattributils. h)
description: Desasigna la memoria asignada internamente a una matriz de estructuras RepairInfo.
ms.assetid: c40f9d10-8d9e-4c79-ac0b-fa88608888f1
keywords:
- FreeRepairInfos función NDF
topic_type:
- apiref
api_name:
- FreeRepairInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63bf6ab2154376302e4c9dd076ccaf83a0c565c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150097"
---
# <a name="freerepairinfos-function"></a><span data-ttu-id="1dfdc-104">FreeRepairInfos función)</span><span class="sxs-lookup"><span data-stu-id="1dfdc-104">FreeRepairInfos function</span></span>

<span data-ttu-id="1dfdc-105">La función **FreeRepairInfos** desasigna la memoria asignada internamente a una matriz de estructuras [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) .</span><span class="sxs-lookup"><span data-stu-id="1dfdc-105">The **FreeRepairInfos** function deallocates the memory allocated internally to an array of [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) structures.</span></span> <span data-ttu-id="1dfdc-106">Esta función llama a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para desasignar memoria.</span><span class="sxs-lookup"><span data-stu-id="1dfdc-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dfdc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1dfdc-107">Syntax</span></span>


```C++
VOID FreeRepairInfos(
  _In_ RepairInfo *pInfo,
       ULONG      RepairCount,
       BOOL       bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="1dfdc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1dfdc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dfdc-109">*Pinfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1dfdc-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dfdc-110">Tipo: \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="1dfdc-110">Type: \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\** _</span></span>

<span data-ttu-id="1dfdc-111">Matriz de estructuras.</span><span class="sxs-lookup"><span data-stu-id="1dfdc-111">The array of structures.</span></span> <span data-ttu-id="1dfdc-112">La memoria asignada a la que apuntan estas estructuras se liberará.</span><span class="sxs-lookup"><span data-stu-id="1dfdc-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdc-113">_RepairCount \*</span><span class="sxs-lookup"><span data-stu-id="1dfdc-113">_RepairCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="1dfdc-114">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="1dfdc-114">Type: **ULONG**</span></span>

<span data-ttu-id="1dfdc-115">El número de estructuras de la matriz a las que apunta *Pinfo*.</span><span class="sxs-lookup"><span data-stu-id="1dfdc-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdc-116">*bFreePointer*</span><span class="sxs-lookup"><span data-stu-id="1dfdc-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="1dfdc-117">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="1dfdc-117">Type: **BOOL**</span></span>

<span data-ttu-id="1dfdc-118">True si también se debe eliminar la matriz de estructuras; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="1dfdc-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dfdc-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1dfdc-119">Return value</span></span>

<span data-ttu-id="1dfdc-120">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1dfdc-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dfdc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dfdc-121">Requirements</span></span>



| <span data-ttu-id="1dfdc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dfdc-122">Requirement</span></span> | <span data-ttu-id="1dfdc-123">Value</span><span class="sxs-lookup"><span data-stu-id="1dfdc-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dfdc-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1dfdc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1dfdc-125">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="1dfdc-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1dfdc-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1dfdc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1dfdc-127">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="1dfdc-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1dfdc-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1dfdc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dfdc-129"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dfdc-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dfdc-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="1dfdc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dfdc-131">**RepairInfo**</span><span class="sxs-lookup"><span data-stu-id="1dfdc-131">**RepairInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> <dt>

[<span data-ttu-id="1dfdc-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="1dfdc-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

