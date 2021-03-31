---
description: Recupera todos los objetos IContextNode de la sugerencia de análisis que están asociados a IInkAnalyzer y que tienen el nombre especificado.
ms.assetid: 15269ee0-055c-424e-be49-945f47e8a77e
title: 'IInkAnalyzer:: GetAnalysisHintsByName (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHintsByName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d86b18bfb8cf17097a36e35fc638dd9bd763d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275468"
---
# <a name="iinkanalyzergetanalysishintsbyname-method"></a><span data-ttu-id="1cf89-103">IInkAnalyzer:: GetAnalysisHintsByName (método)</span><span class="sxs-lookup"><span data-stu-id="1cf89-103">IInkAnalyzer::GetAnalysisHintsByName method</span></span>

<span data-ttu-id="1cf89-104">Recupera todos los objetos [**IContextNode**](icontextnode.md) de la sugerencia de análisis que están asociados a [**IInkAnalyzer**](iinkanalyzer.md) y que tienen el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="1cf89-104">Retrieves all of the analysis hint [**IContextNode**](icontextnode.md) objects that are attached to the [**IInkAnalyzer**](iinkanalyzer.md) and that have the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cf89-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cf89-105">Syntax</span></span>


```C++
HRESULT GetAnalysisHintsByName(
  [in]  BSTR          hintName,
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a><span data-ttu-id="1cf89-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1cf89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cf89-107">*hintName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1cf89-107">*hintName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cf89-108">Nombre de la sugerencia que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="1cf89-108">The hint name for which to search.</span></span>

</dd> <dt>

<span data-ttu-id="1cf89-109">*ppAnalysisHints* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1cf89-109">*ppAnalysisHints* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cf89-110">La sugerencia de análisis [**IContextNode**](icontextnode.md) objetos en el [**IInkAnalyzer**](iinkanalyzer.md) que tienen el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="1cf89-110">The analysis hint [**IContextNode**](icontextnode.md) objects in the [**IInkAnalyzer**](iinkanalyzer.md) that have the specified name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cf89-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1cf89-111">Return value</span></span>

<span data-ttu-id="1cf89-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces: Análisis de tinta](classes-and-interfaces---ink-analysis.md) de los valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="1cf89-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md) the return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cf89-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1cf89-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="1cf89-114">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppAnalysisHints* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="1cf89-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAnalysisHints* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="1cf89-115">Este método devuelve una colección vacía si no hay ningún nodo de sugerencia de análisis asociado a [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="1cf89-115">This method returns an empty collection if no such analysis hint nodes are attached to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="1cf89-116">Un nodo de sugerencia de análisis es un [**IContextNode**](icontextnode.md) con un tipo de nodo de contexto AnalysisHint (vea [**IContextNode:: GetType**](icontextnode-gettype.md) y [tipos de nodo de contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="1cf89-116">An analysis hint node is an [**IContextNode**](icontextnode.md) with a context node type of AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span>

<span data-ttu-id="1cf89-117">Para agregar información de contexto a la sugerencia, use [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md) con el parámetro *pPropertyDataId* establecido en uno de los identificadores únicos globales (GUID) en las constantes de [las propiedades](analysis-hint-properties.md) de la sugerencia de análisis.</span><span class="sxs-lookup"><span data-stu-id="1cf89-117">To add context information to the hint, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) with the *pPropertyDataId* parameter set to one of the globally unique identifiers (GUIDs) in the [Analysis Hint Properties](analysis-hint-properties.md) constants.</span></span>

<span data-ttu-id="1cf89-118">Para averiguar qué valores de propiedad se establecen en un nodo de contexto, use [**IContextNode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span><span class="sxs-lookup"><span data-stu-id="1cf89-118">To find which property values are set on a context node, use [**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span></span> <span data-ttu-id="1cf89-119">Para buscar el valor de una propiedad, use [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md).</span><span class="sxs-lookup"><span data-stu-id="1cf89-119">To find the value of a property, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1cf89-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cf89-120">Requirements</span></span>



| <span data-ttu-id="1cf89-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cf89-121">Requirement</span></span> | <span data-ttu-id="1cf89-122">Value</span><span class="sxs-lookup"><span data-stu-id="1cf89-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cf89-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cf89-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1cf89-124">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1cf89-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1cf89-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cf89-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1cf89-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1cf89-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1cf89-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1cf89-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cf89-128"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1cf89-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1cf89-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1cf89-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cf89-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cf89-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1cf89-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="1cf89-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cf89-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="1cf89-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="1cf89-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="1cf89-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="1cf89-134">**IInkAnalyzer:: CreateAnalysisHint (método)**</span><span class="sxs-lookup"><span data-stu-id="1cf89-134">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="1cf89-135">**IInkAnalyzer::D método eleteAnalysisHint**</span><span class="sxs-lookup"><span data-stu-id="1cf89-135">**IInkAnalyzer::DeleteAnalysisHint Method**</span></span>](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[<span data-ttu-id="1cf89-136">**IInkAnalyzer:: GetAnalysisHints (método)**</span><span class="sxs-lookup"><span data-stu-id="1cf89-136">**IInkAnalyzer::GetAnalysisHints Method**</span></span>](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[<span data-ttu-id="1cf89-137">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="1cf89-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

