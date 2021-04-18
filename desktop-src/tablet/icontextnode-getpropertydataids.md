---
description: Recupera los identificadores para los que hay datos de propiedad.
ms.assetid: c9c491b7-95e2-421a-8632-f65844cd5ef9
title: 'IContextNode:: GetPropertyDataIds (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyDataIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: cdbc0ec0a613feccb4064a88f4723538439f4532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720368"
---
# <a name="icontextnodegetpropertydataids-method"></a><span data-ttu-id="f2d01-103">IContextNode:: GetPropertyDataIds (método)</span><span class="sxs-lookup"><span data-stu-id="f2d01-103">IContextNode::GetPropertyDataIds method</span></span>

<span data-ttu-id="f2d01-104">Recupera los identificadores para los que hay datos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="f2d01-104">Retrieves the identifiers for which there is property data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2d01-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2d01-105">Syntax</span></span>


```C++
HRESULT GetPropertyDataIds(
  [out] ULONG *pulGuidCount,
  [out] GUID  **ppGuids
);
```



## <a name="parameters"></a><span data-ttu-id="f2d01-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2d01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2d01-107">*pulGuidCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f2d01-107">*pulGuidCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2d01-108">Número de propiedades.</span><span class="sxs-lookup"><span data-stu-id="f2d01-108">The number of properties.</span></span>

</dd> <dt>

<span data-ttu-id="f2d01-109">*ppGuids* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f2d01-109">*ppGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2d01-110">Los identificadores para los que hay datos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="f2d01-110">The identifiers for which there is property data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2d01-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2d01-111">Return value</span></span>

<span data-ttu-id="f2d01-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f2d01-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f2d01-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2d01-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="f2d01-114">Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *ppGuids* cuando ya no necesite la información.</span><span class="sxs-lookup"><span data-stu-id="f2d01-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppGuids* when you no longer need the information.</span></span>

 

<span data-ttu-id="f2d01-115">Este método devuelve los identificadores específicos de la aplicación para los datos de propiedad que se han agregado.</span><span class="sxs-lookup"><span data-stu-id="f2d01-115">This method returns the application-specific identifiers for property data that has been added.</span></span> <span data-ttu-id="f2d01-116">También devuelve los identificadores de los datos de propiedad internos, que se describen en las constantes de [las propiedades del nodo de contexto](context-node-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="f2d01-116">It also returns the identifiers for the internal property data, which are described by the [Context Node Properties](context-node-properties.md) constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2d01-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2d01-117">Requirements</span></span>



| <span data-ttu-id="f2d01-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2d01-118">Requirement</span></span> | <span data-ttu-id="f2d01-119">Value</span><span class="sxs-lookup"><span data-stu-id="f2d01-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2d01-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2d01-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f2d01-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f2d01-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f2d01-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2d01-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f2d01-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f2d01-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f2d01-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2d01-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2d01-125"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f2d01-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f2d01-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f2d01-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2d01-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2d01-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f2d01-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2d01-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2d01-129">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="f2d01-129">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="f2d01-130">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="f2d01-130">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="f2d01-131">**IContextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="f2d01-131">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="f2d01-132">**IContextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="f2d01-132">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="f2d01-133">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="f2d01-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

