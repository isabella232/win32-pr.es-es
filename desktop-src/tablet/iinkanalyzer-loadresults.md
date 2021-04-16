---
description: Carga los resultados del análisis guardado en el IInkAnalyzer.
ms.assetid: 7634dbe2-1857-497c-81b5-76b92fed862d
title: 'IInkAnalyzer:: LoadResults (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.LoadResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 76c7fed63b38f1b4fc058fbe7676a727c2d47f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497560"
---
# <a name="iinkanalyzerloadresults-method"></a><span data-ttu-id="9f694-103">IInkAnalyzer:: LoadResults (método)</span><span class="sxs-lookup"><span data-stu-id="9f694-103">IInkAnalyzer::LoadResults method</span></span>

<span data-ttu-id="9f694-104">Carga los resultados del análisis guardado en el [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="9f694-104">Loads saved analysis results into the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f694-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f694-105">Syntax</span></span>


```C++
HRESULT LoadResults(
  [in]          ULONG        ulDataSize,
  [in]          BYTE         *pbSerializedResults,
  [in]          ULONG        ulStrokeIdsCount,
  [in]          LONG         *plOriginalStrokeIds,
  [in]          LONG         *plNewStrokeIds,
  [out, retval] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a><span data-ttu-id="9f694-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f694-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f694-107">*ulDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9f694-107">*ulDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f694-108">Número de bytes de *pbSerializedResults*.</span><span class="sxs-lookup"><span data-stu-id="9f694-108">The number of bytes in *pbSerializedResults*.</span></span>

</dd> <dt>

<span data-ttu-id="9f694-109">*pbSerializedResults* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9f694-109">*pbSerializedResults* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f694-110">Los resultados del análisis serializado.</span><span class="sxs-lookup"><span data-stu-id="9f694-110">The serialized analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="9f694-111">*ulStrokeIdsCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9f694-111">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f694-112">Número de identificadores de trazo.</span><span class="sxs-lookup"><span data-stu-id="9f694-112">The number of stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="9f694-113">*plOriginalStrokeIds* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9f694-113">*plOriginalStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f694-114">Matriz de identificadores de trazo originales.</span><span class="sxs-lookup"><span data-stu-id="9f694-114">The array of original stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="9f694-115">*plNewStrokeIds* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9f694-115">*plNewStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f694-116">Matriz de nuevos identificadores de trazo.</span><span class="sxs-lookup"><span data-stu-id="9f694-116">The array of new stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="9f694-117">*pfSuccessful* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="9f694-117">*pfSuccessful* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9f694-118">**Variante \_ TRUE** si la carga se realizó correctamente; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="9f694-118">**VARIANT\_TRUE** if loading was successful; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f694-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f694-119">Return value</span></span>

<span data-ttu-id="9f694-120">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9f694-120">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9f694-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f694-121">Remarks</span></span>

<span data-ttu-id="9f694-122">Cuando el [**IInkAnalyzer**](iinkanalyzer.md) agrega un [**IContextNode**](icontextnode.md) de los resultados guardados, asigna un nuevo identificador único global (GUID) a **IContextNode** (vea [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md) y [propiedades del nodo de contexto](context-node-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="9f694-122">When the [**IInkAnalyzer**](iinkanalyzer.md) adds a [**IContextNode**](icontextnode.md) from the saved results, it assigns a new globally unique identifier (GUID) to the **IContextNode** (see [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md) and [Context Node Properties](context-node-properties.md)).</span></span>

<span data-ttu-id="9f694-123">Este método agrega los resultados del análisis guardado al árbol [**IContextNode**](icontextnode.md) existente.</span><span class="sxs-lookup"><span data-stu-id="9f694-123">This method adds the saved analysis results to the existing [**IContextNode**](icontextnode.md) tree.</span></span> <span data-ttu-id="9f694-124">Para asegurarse de que los resultados combinados se ordenen correctamente, agregue el área que contiene los nodos de contexto cargados a la región desfasada del objeto [**IInkAnalyzer**](iinkanalyzer.md) (vea el [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) y vuelva a analizar la tinta.</span><span class="sxs-lookup"><span data-stu-id="9f694-124">To ensure that the combined results are ordered correctly, add the area containing the loaded context nodes to the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) and reanalyze the ink.</span></span>

<span data-ttu-id="9f694-125">Los métodos de método [**IInkAnalyzer:: SaveResults**](iinkanalyzer-saveresults.md), [**IInkAnalyzer:: SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)y [**IInkAnalyzer:: SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md) no guardan los datos del paquete junto con los resultados del análisis.</span><span class="sxs-lookup"><span data-stu-id="9f694-125">The [**IInkAnalyzer::SaveResults Method**](iinkanalyzer-saveresults.md), [**IInkAnalyzer::SaveResultsForNodes Method**](iinkanalyzer-saveresultsfornodes.md), and [**IInkAnalyzer::SaveResultsForStrokes Method**](iinkanalyzer-saveresultsforstrokes.md) methods do not save the packet data along with the analysis results.</span></span>

<span data-ttu-id="9f694-126">Cada identificador de *plOriginalStrokeIds* es el identificador del trazo del trazo en los resultados del análisis guardado.</span><span class="sxs-lookup"><span data-stu-id="9f694-126">Each identifier in *plOriginalStrokeIds* is the stroke identifier for the stroke in the saved analysis results.</span></span> <span data-ttu-id="9f694-127">Cada identificador de *plNewStrokeIds* es el nuevo identificador con el que se va a reemplazar el identificador original en los resultados del análisis cargado.</span><span class="sxs-lookup"><span data-stu-id="9f694-127">Each identifier in *plNewStrokeIds* is the new identifier with which to replace the original identifier in the loaded analysis results.</span></span>

<span data-ttu-id="9f694-128">Si una sugerencia de análisis guardado entra en conflicto con una sugerencia de análisis existente, el [**IInkAnalyzer**](iinkanalyzer.md) no carga la sugerencia guardada, sino que carga el resto de los resultados guardados.</span><span class="sxs-lookup"><span data-stu-id="9f694-128">If a saved analysis hint conflicts with an existing analysis hint, the [**IInkAnalyzer**](iinkanalyzer.md) does not load the saved hint but does load the rest of the saved results.</span></span> <span data-ttu-id="9f694-129">Sin embargo, si **IInkAnalyzer** carga los resultados de un trazo que se encuentra dentro del área de una sugerencia de análisis guardado que el **IInkAnalyzer** no carga, **IInkAnalyzer** agrega el rectángulo de selección del trazo a la región desfasada del objeto **IInkAnalyzer** .</span><span class="sxs-lookup"><span data-stu-id="9f694-129">However, if the **IInkAnalyzer** loads results for a stroke that is within the area of a saved analysis hint that the **IInkAnalyzer** does not load, the **IInkAnalyzer** adds the bounding box of the stroke to the **IInkAnalyzer** object's dirty region.</span></span> <span data-ttu-id="9f694-130">Además, si **IInkAnalyzer** carga los resultados de un trazo que se encuentra dentro de un área de la sugerencia de análisis existente, el **IInkAnalyzer** también agrega el rectángulo de selección del trazo a la región desfasada del objeto **IInkAnalyzer** .</span><span class="sxs-lookup"><span data-stu-id="9f694-130">Also, if the **IInkAnalyzer** loads results for a stroke that is within an existing analysis hint's area, the **IInkAnalyzer** also adds the bounding box of the stroke to the **IInkAnalyzer** object's dirty region.</span></span> <span data-ttu-id="9f694-131">Para obtener más información acerca de las sugerencias de análisis, consulte propiedades de la [sugerencia de análisis](analysis-hint-properties.md).</span><span class="sxs-lookup"><span data-stu-id="9f694-131">For more information about analysis hints, see [Analysis Hint Properties](analysis-hint-properties.md).</span></span>

<span data-ttu-id="9f694-132">Este método puede generar los eventos [**\_ IAnalysisProxyEvents:: ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**\_ IAnalysisProxyEvents:: ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)y [**\_ IAnalysisProxyEvents:: ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) cuando carga los resultados guardados.</span><span class="sxs-lookup"><span data-stu-id="9f694-132">This method may raise the [**\_IAnalysisProxyEvents::ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**\_IAnalysisProxyEvents::ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md), and [**\_IAnalysisProxyEvents::ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) events as it loads the saved results.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f694-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f694-133">Requirements</span></span>



| <span data-ttu-id="9f694-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f694-134">Requirement</span></span> | <span data-ttu-id="9f694-135">Value</span><span class="sxs-lookup"><span data-stu-id="9f694-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f694-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f694-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9f694-137">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9f694-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9f694-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f694-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9f694-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9f694-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9f694-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f694-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f694-141"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9f694-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9f694-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9f694-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f694-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f694-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9f694-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f694-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f694-145">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="9f694-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="9f694-146">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="9f694-146">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="9f694-147">**IInkAnalyzer:: GetDirtyRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="9f694-147">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="9f694-148">**IInkAnalyzer:: SetDirtyRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="9f694-148">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="9f694-149">**IInkAnalyzer:: SaveResults (método)**</span><span class="sxs-lookup"><span data-stu-id="9f694-149">**IInkAnalyzer::SaveResults Method**</span></span>](iinkanalyzer-saveresults.md)
</dt> <dt>

[<span data-ttu-id="9f694-150">**IInkAnalyzer:: SaveResultsForNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="9f694-150">**IInkAnalyzer::SaveResultsForNodes Method**</span></span>](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[<span data-ttu-id="9f694-151">**IInkAnalyzer:: SaveResultsForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="9f694-151">**IInkAnalyzer::SaveResultsForStrokes Method**</span></span>](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[<span data-ttu-id="9f694-152">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="9f694-152">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




