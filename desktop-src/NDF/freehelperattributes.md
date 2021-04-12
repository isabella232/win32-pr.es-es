---
title: Función FreeHelperAttributes (Ndattributils. h)
description: Desasigna la memoria asignada internamente a una matriz de estructuras de atributo de aplicación auxiliar \_ .
ms.assetid: d973bdb9-c1d1-4cea-bcc6-98671349413f
keywords:
- FreeHelperAttributes función NDF
topic_type:
- apiref
api_name:
- FreeHelperAttributes
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400addd7d32914cb4e849e4e0bfae76ccc3ddf22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489880"
---
# <a name="freehelperattributes-function"></a><span data-ttu-id="47e2f-104">FreeHelperAttributes función)</span><span class="sxs-lookup"><span data-stu-id="47e2f-104">FreeHelperAttributes function</span></span>

<span data-ttu-id="47e2f-105">La función **FreeHelperAttributes** desasigna la memoria asignada internamente a una matriz de estructuras de [**\_ atributo de aplicación auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) .</span><span class="sxs-lookup"><span data-stu-id="47e2f-105">The **FreeHelperAttributes** function deallocates the memory allocated internally to an array of [**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) structures.</span></span> <span data-ttu-id="47e2f-106">Esta función llama a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para desasignar memoria.</span><span class="sxs-lookup"><span data-stu-id="47e2f-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="47e2f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47e2f-107">Syntax</span></span>


```C++
VOID FreeHelperAttributes(
  _In_ HELPER_ATTRIBUTE *pInfo,
       ULONG            HelperAttributeCount,
       BOOL             bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="47e2f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47e2f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47e2f-109">*Pinfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="47e2f-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47e2f-110">Tipo: \**\* [**\_ atributo auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)* _</span><span class="sxs-lookup"><span data-stu-id="47e2f-110">Type: \**[**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\** _</span></span>

<span data-ttu-id="47e2f-111">Matriz de estructuras.</span><span class="sxs-lookup"><span data-stu-id="47e2f-111">The array of structures.</span></span> <span data-ttu-id="47e2f-112">La memoria asignada a la que apuntan estas estructuras se liberará.</span><span class="sxs-lookup"><span data-stu-id="47e2f-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="47e2f-113">_HelperAttributeCount \*</span><span class="sxs-lookup"><span data-stu-id="47e2f-113">_HelperAttributeCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="47e2f-114">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="47e2f-114">Type: **ULONG**</span></span>

<span data-ttu-id="47e2f-115">El número de estructuras de la matriz a las que apunta *Pinfo*.</span><span class="sxs-lookup"><span data-stu-id="47e2f-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="47e2f-116">*bFreePointer*</span><span class="sxs-lookup"><span data-stu-id="47e2f-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="47e2f-117">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="47e2f-117">Type: **BOOL**</span></span>

<span data-ttu-id="47e2f-118">True si también se debe eliminar la matriz de estructuras; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="47e2f-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47e2f-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47e2f-119">Return value</span></span>

<span data-ttu-id="47e2f-120">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="47e2f-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="47e2f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47e2f-121">Requirements</span></span>



| <span data-ttu-id="47e2f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="47e2f-122">Requirement</span></span> | <span data-ttu-id="47e2f-123">Value</span><span class="sxs-lookup"><span data-stu-id="47e2f-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="47e2f-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47e2f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="47e2f-125">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="47e2f-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="47e2f-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47e2f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="47e2f-127">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="47e2f-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="47e2f-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="47e2f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="47e2f-129"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="47e2f-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47e2f-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="47e2f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47e2f-131">**atributo auxiliar \_**</span><span class="sxs-lookup"><span data-stu-id="47e2f-131">**HELPER\_ATTRIBUTE**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> <dt>

[<span data-ttu-id="47e2f-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="47e2f-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

