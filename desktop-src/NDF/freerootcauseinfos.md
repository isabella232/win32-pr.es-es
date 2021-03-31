---
title: Función FreeRootCauseInfos (Ndattributils. h)
description: Desasigna la memoria asignada internamente a una matriz de estructuras RootCauseInfo.
ms.assetid: b45fa432-0db4-470b-80ce-ae25c33f88d6
keywords:
- FreeRootCauseInfos función NDF
topic_type:
- apiref
api_name:
- FreeRootCauseInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d302a1c58f1a77aafa7611f437f3d445f29f9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801820"
---
# <a name="freerootcauseinfos-function"></a><span data-ttu-id="036e6-104">FreeRootCauseInfos función)</span><span class="sxs-lookup"><span data-stu-id="036e6-104">FreeRootCauseInfos function</span></span>

<span data-ttu-id="036e6-105">La función **FreeRootCauseInfos** desasigna la memoria asignada internamente a una matriz de estructuras [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) .</span><span class="sxs-lookup"><span data-stu-id="036e6-105">The **FreeRootCauseInfos** function deallocates the memory allocated internally to an array of [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) structures.</span></span> <span data-ttu-id="036e6-106">Esta función llama a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para desasignar memoria.</span><span class="sxs-lookup"><span data-stu-id="036e6-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="036e6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="036e6-107">Syntax</span></span>


```C++
VOID FreeRootCauseInfos(
  _In_ RootCauseInfo *pInfo,
       ULONG         RootCauseCount,
       BOOL          bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="036e6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="036e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="036e6-109">*Pinfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="036e6-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="036e6-110">Tipo: \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="036e6-110">Type: \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\** _</span></span>

<span data-ttu-id="036e6-111">Matriz de estructuras.</span><span class="sxs-lookup"><span data-stu-id="036e6-111">The array of structures.</span></span> <span data-ttu-id="036e6-112">La memoria asignada a la que apuntan estas estructuras se liberará.</span><span class="sxs-lookup"><span data-stu-id="036e6-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="036e6-113">_RootCauseCount \*</span><span class="sxs-lookup"><span data-stu-id="036e6-113">_RootCauseCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="036e6-114">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="036e6-114">Type: **ULONG**</span></span>

<span data-ttu-id="036e6-115">El número de estructuras de la matriz a las que apunta *Pinfo*.</span><span class="sxs-lookup"><span data-stu-id="036e6-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="036e6-116">*bFreePointer*</span><span class="sxs-lookup"><span data-stu-id="036e6-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="036e6-117">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="036e6-117">Type: **BOOL**</span></span>

<span data-ttu-id="036e6-118">True si también se debe eliminar la matriz de estructuras; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="036e6-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="036e6-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="036e6-119">Return value</span></span>

<span data-ttu-id="036e6-120">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="036e6-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="036e6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="036e6-121">Requirements</span></span>



| <span data-ttu-id="036e6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="036e6-122">Requirement</span></span> | <span data-ttu-id="036e6-123">Value</span><span class="sxs-lookup"><span data-stu-id="036e6-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="036e6-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="036e6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="036e6-125">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="036e6-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="036e6-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="036e6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="036e6-127">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="036e6-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="036e6-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="036e6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="036e6-129"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="036e6-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="036e6-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="036e6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="036e6-131">**RootCauseInfo**</span><span class="sxs-lookup"><span data-stu-id="036e6-131">**RootCauseInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> <dt>

[<span data-ttu-id="036e6-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="036e6-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

