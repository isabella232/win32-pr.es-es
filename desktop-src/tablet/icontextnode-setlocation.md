---
description: Actualiza el área de este IContextNode.
ms.assetid: e7001411-17e4-4f33-af04-dd3220275895
title: 'IContextNode:: SetLocation (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetLocation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 20daefeab7a9e36d5e968d5d14bfa5110d733487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705699"
---
# <a name="icontextnodesetlocation-method"></a><span data-ttu-id="900fd-103">IContextNode:: SetLocation (método)</span><span class="sxs-lookup"><span data-stu-id="900fd-103">IContextNode::SetLocation method</span></span>

<span data-ttu-id="900fd-104">Actualiza el área de este [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="900fd-104">Updates the area of this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="900fd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="900fd-105">Syntax</span></span>


```C++
HRESULT SetLocation(
  [in] IAnalysisRegion *pIAnalysisRegion
);
```



## <a name="parameters"></a><span data-ttu-id="900fd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="900fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="900fd-107">*pIAnalysisRegion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="900fd-107">*pIAnalysisRegion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="900fd-108">[**IAnalysisRegion**](ianalysisregion.md) que describe el área en la que se va a establecer la ubicación del objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="900fd-108">The [**IAnalysisRegion**](ianalysisregion.md) describing the area to which to set the [**IContextNode**](icontextnode.md) object's location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="900fd-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="900fd-109">Return value</span></span>

<span data-ttu-id="900fd-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="900fd-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="900fd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="900fd-111">Remarks</span></span>

<span data-ttu-id="900fd-112">Use este método para actualizar la ubicación del nodo de contexto (vea [**IContextNode:: GetLocation**](icontextnode-getlocation.md)).</span><span class="sxs-lookup"><span data-stu-id="900fd-112">Use this method to update the context node's location (see [**IContextNode::GetLocation**](icontextnode-getlocation.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="900fd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="900fd-113">Requirements</span></span>



| <span data-ttu-id="900fd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="900fd-114">Requirement</span></span> | <span data-ttu-id="900fd-115">Value</span><span class="sxs-lookup"><span data-stu-id="900fd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="900fd-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="900fd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="900fd-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="900fd-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="900fd-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="900fd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="900fd-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="900fd-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="900fd-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="900fd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="900fd-121"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="900fd-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="900fd-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="900fd-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="900fd-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="900fd-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="900fd-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="900fd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="900fd-125">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="900fd-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="900fd-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="900fd-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="900fd-127">**IContextNode:: GetLocation**</span><span class="sxs-lookup"><span data-stu-id="900fd-127">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
</dt> <dt>

[<span data-ttu-id="900fd-128">**IContextNode::GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="900fd-128">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="900fd-129">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="900fd-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




