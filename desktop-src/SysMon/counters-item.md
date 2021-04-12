---
title: Counters. Item (propiedad)
description: Recupera la instancia de un elemento de objeto especificado de la colección.
ms.assetid: bf503371-c8bd-4e0d-ab8d-58de3f8fac5f
keywords:
- Propiedad del elemento SysMon
- Propiedad de elemento SysMon, clase counters
- Counters (clase) SysMon, propiedad Item
topic_type:
- apiref
api_name:
- Counters.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 251a645f0a4ceacdbfb4e2ab7e650f41e44dd508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489718"
---
# <a name="countersitem-property"></a><span data-ttu-id="5e0e1-106">Counters. Item (propiedad)</span><span class="sxs-lookup"><span data-stu-id="5e0e1-106">Counters.Item property</span></span>

<span data-ttu-id="5e0e1-107">Recupera la instancia de un [**elemento de objeto**](counteritem.md) especificado de la colección.</span><span class="sxs-lookup"><span data-stu-id="5e0e1-107">Retrieves the specified [**CounterItem**](counteritem.md) instance from the collection.</span></span>

<span data-ttu-id="5e0e1-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5e0e1-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e0e1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e0e1-109">Syntax</span></span>


```VB
Property Item( _
  ByVal index As Object _
) As CounterItem
```



## <a name="property-value"></a><span data-ttu-id="5e0e1-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5e0e1-110">Property value</span></span>

<span data-ttu-id="5e0e1-111">Instancia de [**contraelemento**](counteritem.md) que corresponde al valor de índice especificado.</span><span class="sxs-lookup"><span data-stu-id="5e0e1-111">[**CounterItem**](counteritem.md) instance that corresponds to the specified index value.</span></span>

## <a name="exceptions"></a><span data-ttu-id="5e0e1-112">Excepciones</span><span class="sxs-lookup"><span data-stu-id="5e0e1-112">Exceptions</span></span>



| <span data-ttu-id="5e0e1-113">Tipo de excepción</span><span class="sxs-lookup"><span data-stu-id="5e0e1-113">Exception type</span></span>                                  | <span data-ttu-id="5e0e1-114">Condición</span><span class="sxs-lookup"><span data-stu-id="5e0e1-114">Condition</span></span>                         |
|-------------------------------------------------|-----------------------------------|
| <span data-ttu-id="5e0e1-115">**System. Runtime. InteropServices. COMException**</span><span class="sxs-lookup"><span data-stu-id="5e0e1-115">**System.Runtime.InteropServices.COMException**</span></span> | <span data-ttu-id="5e0e1-116">El índice especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="5e0e1-116">The specified index is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5e0e1-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e0e1-117">Remarks</span></span>

<span data-ttu-id="5e0e1-118">Esta es la propiedad predeterminada del objeto [**counters**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="5e0e1-118">This is the default property of the [**Counters**](counters.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e0e1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e0e1-119">Requirements</span></span>



| <span data-ttu-id="5e0e1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e0e1-120">Requirement</span></span> | <span data-ttu-id="5e0e1-121">Value</span><span class="sxs-lookup"><span data-stu-id="5e0e1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e0e1-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e0e1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5e0e1-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5e0e1-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5e0e1-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e0e1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5e0e1-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5e0e1-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5e0e1-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e0e1-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e0e1-127"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="5e0e1-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e0e1-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e0e1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e0e1-129">**Elemento de**</span><span class="sxs-lookup"><span data-stu-id="5e0e1-129">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="5e0e1-130">**Counters**</span><span class="sxs-lookup"><span data-stu-id="5e0e1-130">**Counters**</span></span>](counters.md)
</dt> </dl>

 

 





