---
description: Modifica el valor que indica si este IContextNode se rellena parcial o totalmente.
ms.assetid: 4d8e1ec0-757d-4346-a77e-263bd612972b
title: 'IContextNode:: SetPartiallyPopulated (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 31707468945fd3c5eb413bcdb984748a55867982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082154"
---
# <a name="icontextnodesetpartiallypopulated-method"></a><span data-ttu-id="27abc-103">IContextNode:: SetPartiallyPopulated (método)</span><span class="sxs-lookup"><span data-stu-id="27abc-103">IContextNode::SetPartiallyPopulated method</span></span>

<span data-ttu-id="27abc-104">Modifica el valor que indica si este [**IContextNode**](icontextnode.md) se rellena parcial o totalmente.</span><span class="sxs-lookup"><span data-stu-id="27abc-104">Modifies the value that indicates whether this [**IContextNode**](icontextnode.md) is partially or fully populated.</span></span>

## <a name="syntax"></a><span data-ttu-id="27abc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27abc-105">Syntax</span></span>


```C++
HRESULT SetPartiallyPopulated(
  [in] VARIANT_BOOL fPartiallyPopulated
);
```



## <a name="parameters"></a><span data-ttu-id="27abc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27abc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27abc-107">*fPartiallyPopulated* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="27abc-107">*fPartiallyPopulated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27abc-108">**Variante \_ TRUE** si este [**IContextNode**](icontextnode.md) se rellena parcialmente; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="27abc-108">**VARIANT\_TRUE** if this [**IContextNode**](icontextnode.md) is partially populated; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27abc-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27abc-109">Return value</span></span>

<span data-ttu-id="27abc-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="27abc-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="27abc-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27abc-111">Remarks</span></span>

<span data-ttu-id="27abc-112">Use este método cuando la aplicación mantenga su propia estructura de datos, que está sincronizada con la de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="27abc-112">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="27abc-113">Para obtener más información, consulte [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="27abc-113">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="27abc-114">Al virtualizar el árbol del documento, asegúrese de establecer el valor PropertyGuidsForContextNodes. RotatedBoundingBox (mediante ContextNode. AddPropertyValue) en todos los objetos ContextNode.</span><span class="sxs-lookup"><span data-stu-id="27abc-114">When virtualizing your document tree, be sure to set the PropertyGuidsForContextNodes.RotatedBoundingBox value (using ContextNode.AddPropertyValue) on all ContextNode objects.</span></span> <span data-ttu-id="27abc-115">La propiedad RotatedBoundingBox se calcula mediante InkAnalyzer y, de forma predeterminada, debe estar en todos los ContextNodes de escritura.</span><span class="sxs-lookup"><span data-stu-id="27abc-115">The RotatedBoundingBox property is calculated by the InkAnalyzer and by default should be on all writing ContextNodes.</span></span> <span data-ttu-id="27abc-116">Sin embargo, si la aplicación Virtualiza los resultados del análisis estableciendo la propiedad PartiallyPopulated, al controlar el evento PopulateContextNode Asegúrese de rellenar la propiedad RotatedBoundingBox.</span><span class="sxs-lookup"><span data-stu-id="27abc-116">However, if your application virtualizes the analysis results by setting the PartiallyPopulated property, when handling the PopulateContextNode event be sure to populate the RotatedBoundingBox property.</span></span> <span data-ttu-id="27abc-117">Si no se establece la propiedad RotatedBoundingBox, se usarán potencialmente más datos de documento en la operación de análisis actual.</span><span class="sxs-lookup"><span data-stu-id="27abc-117">Failure to set the RotatedBoundingBox property will result in potentially more document data being used in the current analysis operation</span></span>

## <a name="requirements"></a><span data-ttu-id="27abc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27abc-118">Requirements</span></span>



| <span data-ttu-id="27abc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="27abc-119">Requirement</span></span> | <span data-ttu-id="27abc-120">Value</span><span class="sxs-lookup"><span data-stu-id="27abc-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27abc-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27abc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="27abc-122">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="27abc-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="27abc-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27abc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="27abc-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="27abc-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="27abc-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27abc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="27abc-126"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="27abc-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="27abc-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="27abc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27abc-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27abc-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="27abc-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="27abc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27abc-130">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="27abc-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="27abc-131">**\_IAnalysisProxyEvents::P opulateContextNode**</span><span class="sxs-lookup"><span data-stu-id="27abc-131">**\_IAnalysisProxyEvents::PopulateContextNode**</span></span>](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[<span data-ttu-id="27abc-132">**IContextNode::CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="27abc-132">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="27abc-133">**IContextNode::GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="27abc-133">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="27abc-134">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="27abc-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




