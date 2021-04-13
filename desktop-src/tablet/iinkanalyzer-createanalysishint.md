---
description: Agrega un nuevo nodo de sugerencia de análisis con un área infinita a IInkAnalyzer.
ms.assetid: 4cc592c4-456f-4aa5-9a87-d9427de487f3
title: 'IInkAnalyzer:: CreateAnalysisHint (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 041dc1a60c1eeb18d6896a6a23537ac9ebccd321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360340"
---
# <a name="iinkanalyzercreateanalysishint-method"></a><span data-ttu-id="3aff8-103">IInkAnalyzer:: CreateAnalysisHint (método)</span><span class="sxs-lookup"><span data-stu-id="3aff8-103">IInkAnalyzer::CreateAnalysisHint method</span></span>

<span data-ttu-id="3aff8-104">Agrega un nuevo nodo de sugerencia de análisis con un área infinita a [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="3aff8-104">Adds a new analysis hint node with an infinite area to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3aff8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3aff8-105">Syntax</span></span>


```C++
HRESULT CreateAnalysisHint(
  [out] IContextNode **ppAnalysisHint
);
```



## <a name="parameters"></a><span data-ttu-id="3aff8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3aff8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aff8-107">*ppAnalysisHint* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3aff8-107">*ppAnalysisHint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3aff8-108">Nuevo nodo de sugerencia de análisis.</span><span class="sxs-lookup"><span data-stu-id="3aff8-108">The new analysis hint node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aff8-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3aff8-109">Return value</span></span>

<span data-ttu-id="3aff8-110">Vea [clases e interfaces: Análisis de tinta](classes-and-interfaces---ink-analysis.md) para obtener una descripción de los valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="3aff8-110">See [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md) for a description of the return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3aff8-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3aff8-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="3aff8-112">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppAnalysisHint* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="3aff8-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAnalysisHint* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="3aff8-113">Para proporcionar información de contexto adicional para el [**IInkAnalyzer**](iinkanalyzer.md), puede Agregar sugerencias de análisis al analizador de tinta.</span><span class="sxs-lookup"><span data-stu-id="3aff8-113">To provide extra context information for the [**IInkAnalyzer**](iinkanalyzer.md), you can add analysis hints to the ink analyzer.</span></span> <span data-ttu-id="3aff8-114">Las sugerencias de análisis pueden mejorar la precisión del reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="3aff8-114">Analysis hints can improve recognition accuracy.</span></span> <span data-ttu-id="3aff8-115">Por ejemplo, puede Agregar Factoid y la información de la guía para los campos de una aplicación de formulario.</span><span class="sxs-lookup"><span data-stu-id="3aff8-115">For example, you can add factoid and guide information for fields in a form application.</span></span>

<span data-ttu-id="3aff8-116">Este método crea un nuevo [**IContextNode**](icontextnode.md) con un tipo de nodo de contexto de AnalysisHint (vea [**IContextNode:: GetType**](icontextnode-gettype.md)) y agrega la nueva sugerencia como un subnodo del nodo raíz del objeto [**IInkAnalyzer**](iinkanalyzer.md) (vea [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) y [**IInkAnalyzer:: GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span><span class="sxs-lookup"><span data-stu-id="3aff8-116">This method creates a new [**IContextNode**](icontextnode.md) with a context node type of AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md)) and adds the new hint as a subnode of the [**IInkAnalyzer**](iinkanalyzer.md) object's root node (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) and [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span></span>

<span data-ttu-id="3aff8-117">Para agregar información de contexto a la sugerencia, use [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md) con el parámetro *pPropertyDataId* establecido en una de las constantes de [las propiedades](analysis-hint-properties.md) de la sugerencia de análisis.</span><span class="sxs-lookup"><span data-stu-id="3aff8-117">To add context information to the hint, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) with the *pPropertyDataId* parameter set to one of the [Analysis Hint Properties](analysis-hint-properties.md) constants.</span></span>

<span data-ttu-id="3aff8-118">Si a una sugerencia se le asigna un área infinita, que se denomina una sugerencia global, el [**IInkAnalyzer**](iinkanalyzer.md) aplica el contexto de la sugerencia a todas las entradas de lápiz que no se encuentran dentro de otro área de la sugerencia.</span><span class="sxs-lookup"><span data-stu-id="3aff8-118">If a hint is assigned an infinite area, termed a global hint, the [**IInkAnalyzer**](iinkanalyzer.md) applies the hint's context to all ink that is not within another hint's area.</span></span> <span data-ttu-id="3aff8-119">Se pueden adjuntar varias sugerencias a un único **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="3aff8-119">Multiple hints may be attached to a single **IInkAnalyzer**.</span></span> <span data-ttu-id="3aff8-120">Sin embargo, solo se puede adjuntar una sugerencia global a un único analizador de tinta y no se pueden superponer las sugerencias no globales.</span><span class="sxs-lookup"><span data-stu-id="3aff8-120">However, only one global hint can be attached to a single ink analyzer, and no non-global hints can overlap.</span></span> <span data-ttu-id="3aff8-121">Para obtener más información sobre los tipos de información de contexto que puede proporcionar una sugerencia, consulte propiedades de la [sugerencia de análisis](analysis-hint-properties.md).</span><span class="sxs-lookup"><span data-stu-id="3aff8-121">For more information about the types of context information that a hint can provide, see [Analysis Hint Properties](analysis-hint-properties.md).</span></span>

<span data-ttu-id="3aff8-122">La adición de una sugerencia de análisis no marca el área de la sugerencia para su análisis.</span><span class="sxs-lookup"><span data-stu-id="3aff8-122">Adding an analysis hint does not mark the hint's area for reanalysis.</span></span> <span data-ttu-id="3aff8-123">Para marcar el área dentro de la sugerencia para su reanálisis, use el [**método IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) para establecer la región desfasada en la Unión de la región desfasada actual y el área de la sugerencia de análisis.</span><span class="sxs-lookup"><span data-stu-id="3aff8-123">To mark the area within the hint for reanalysis, use [**IInkAnalyzer::SetDirtyRegion Method**](iinkanalyzer-setdirtyregion.md) to set the dirty region to the union of the current dirty region and area of the analysis hint.</span></span>

<span data-ttu-id="3aff8-124">Al utilizar sugerencias para una aplicación de formulario, la aplicación debe evitar mezclar el contexto del texto con la entrada de lápiz en los formularios.</span><span class="sxs-lookup"><span data-stu-id="3aff8-124">When using hints for a form application, the application should avoid mixing text context with ink in the forms.</span></span> <span data-ttu-id="3aff8-125">Esto significa que, por ejemplo, los nombres de campo de texto no se deben crear en el árbol de análisis.</span><span class="sxs-lookup"><span data-stu-id="3aff8-125">This means for example that text field names should not be created in the analysis tree.</span></span> <span data-ttu-id="3aff8-126">Las sugerencias están diseñadas para asociar la tinta a áreas de las páginas; cualquier contexto de texto interfiere con esta asociación de entrada de lápiz a sugerencia.</span><span class="sxs-lookup"><span data-stu-id="3aff8-126">Hints are meant to associate the ink to areas on pages; any text context interferes with this ink-to-hint association.</span></span> <span data-ttu-id="3aff8-127">La operación de análisis puede mezclar la tinta y el contexto de texto en la misma región de escritura, lo que impediría que la tinta se asociara con el área de sugerencias.</span><span class="sxs-lookup"><span data-stu-id="3aff8-127">The analysis operation may merge the ink and the text context in the same writing region which would prevent the ink from being associated with the hint area.</span></span>

<span data-ttu-id="3aff8-128">Para obtener más información sobre el análisis de tinta, consulte [información general del análisis de tinta](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3aff8-128">For more information about ink analysis, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3aff8-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3aff8-129">Requirements</span></span>



| <span data-ttu-id="3aff8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3aff8-130">Requirement</span></span> | <span data-ttu-id="3aff8-131">Value</span><span class="sxs-lookup"><span data-stu-id="3aff8-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aff8-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3aff8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3aff8-133">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3aff8-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3aff8-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3aff8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3aff8-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3aff8-135">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3aff8-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3aff8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="3aff8-137"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3aff8-137"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3aff8-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3aff8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3aff8-139"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3aff8-139"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3aff8-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="3aff8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aff8-141">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="3aff8-141">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="3aff8-142">**IContextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="3aff8-142">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="3aff8-143">**IInkAnalyzer::D método eleteAnalysisHint**</span><span class="sxs-lookup"><span data-stu-id="3aff8-143">**IInkAnalyzer::DeleteAnalysisHint Method**</span></span>](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[<span data-ttu-id="3aff8-144">**IInkAnalyzer:: GetAnalysisHints (método)**</span><span class="sxs-lookup"><span data-stu-id="3aff8-144">**IInkAnalyzer::GetAnalysisHints Method**</span></span>](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[<span data-ttu-id="3aff8-145">**IInkAnalyzer:: GetAnalysisHintsByName (método)**</span><span class="sxs-lookup"><span data-stu-id="3aff8-145">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="3aff8-146">Propiedades de la sugerencia de análisis</span><span class="sxs-lookup"><span data-stu-id="3aff8-146">Analysis Hint Properties</span></span>](analysis-hint-properties.md)
</dt> <dt>

[<span data-ttu-id="3aff8-147">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="3aff8-147">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

