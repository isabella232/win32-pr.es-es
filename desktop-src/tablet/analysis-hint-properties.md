---
description: 'Define identificadores únicos globales (GUID) para las propiedades de un nodo de sugerencia de análisis (vea IContextNode:: GetType).'
ms.assetid: 8300c792-a741-49de-a03b-f4840ea5d647
title: Propiedades de la sugerencia de análisis (Iaguid. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AHP_ALLOWPARTIALDICTIONARYTERMS
- GUID_AHP_ANALYSISHINTNAME
- GUID_AHP_COERCETOFACTOID
- GUID_AHP_ENABLEDUNICODECHARACTERRANGES
- GUID_AHP_FACTOID
- GUID_AHP_GUIDE
- GUID_AHP_PREFIXTEXT
- GUID_AHP_SUFFIXTEXT
- GUID_AHP_TOPINKBREAKSONLY
- GUID_AHP_WORDLIST
- GUID_AHP_WORDMODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 8a7a25cfa94bb7f2354418ded2b35e3137364901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000852"
---
# <a name="analysis-hint-properties"></a><span data-ttu-id="62a2d-103">Propiedades de la sugerencia de análisis</span><span class="sxs-lookup"><span data-stu-id="62a2d-103">Analysis Hint Properties</span></span>

<span data-ttu-id="62a2d-104">Define identificadores únicos globales (GUID) para las propiedades de un nodo de sugerencia de análisis (vea [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="62a2d-104">Defines globally unique identifiers (GUIDs) for properties of an analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

<span data-ttu-id="62a2d-105">En la tabla siguiente se describe la información a la que hace referencia cada constante.</span><span class="sxs-lookup"><span data-stu-id="62a2d-105">The following table describes information referenced by each constant.</span></span>



| <span data-ttu-id="62a2d-106">Constante</span><span class="sxs-lookup"><span data-stu-id="62a2d-106">Constant</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="62a2d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="62a2d-107">Description</span></span>                                                                                                                                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AHP_ALLOWPARTIALDICTIONARYTERMS"></span><span id="guid_ahp_allowpartialdictionaryterms"></span><dl> <span data-ttu-id="62a2d-108"><dt>**GUID \_ AHP \_ ALLOWPARTIALDICTIONARYTERMS**</dt></span><span class="sxs-lookup"><span data-stu-id="62a2d-108"><dt>**GUID\_AHP\_ALLOWPARTIALDICTIONARYTERMS**</dt></span></span> </dl>       | <span data-ttu-id="62a2d-109">Indica si se permiten términos de diccionario parciales en una sugerencia de análisis.</span><span class="sxs-lookup"><span data-stu-id="62a2d-109">Whether partial dictionary terms are allowed on an analysis hint.</span></span><br/>                                                                              |
| <span id="GUID_AHP_ANALYSISHINTNAME"></span><span id="guid_ahp_analysishintname"></span><dl> <span data-ttu-id="62a2d-110"><dt>**GUID \_ AHP \_ ANALYSISHINTNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="62a2d-110"><dt>**GUID\_AHP\_ANALYSISHINTNAME**</dt></span></span> </dl>                                        | <span data-ttu-id="62a2d-111">Nombre de una sugerencia de análisis.</span><span class="sxs-lookup"><span data-stu-id="62a2d-111">The name of an analysis hint.</span></span><br/>                                                                                                                  |
| <span id="GUID_AHP_COERCETOFACTOID"></span><span id="guid_ahp_coercetofactoid"></span><dl> <span data-ttu-id="62a2d-112"><dt>**GUID \_ AHP \_ COERCETOFACTOID**</dt></span><span class="sxs-lookup"><span data-stu-id="62a2d-112"><dt>**GUID\_AHP\_COERCETOFACTOID**</dt></span></span> </dl>                                           | <span data-ttu-id="62a2d-113">Si el analizador de tintas limita su análisis de tinta dentro del área de la sugerencia para ajustarse al Factoid.</span><span class="sxs-lookup"><span data-stu-id="62a2d-113">Whether the ink analyzer limits its analysis of ink within the hint's area to conform to the factoid.</span></span><br/>                                          |
| <span id="GUID_AHP_ENABLEDUNICODECHARACTERRANGES"></span><span id="guid_ahp_enabledunicodecharacterranges"></span><dl> <span data-ttu-id="62a2d-114"><dt>**GUID \_ AHP \_ ENABLEDUNICODECHARACTERRANGES**</dt></span><span class="sxs-lookup"><span data-stu-id="62a2d-114"><dt>**GUID\_AHP\_ENABLEDUNICODECHARACTERRANGES**</dt></span></span> </dl> | <span data-ttu-id="62a2d-115">La sugerencia contiene una matriz de caracteres que representa el conjunto restringido de juegos de caracteres Unicode admitidos que admite este InkRecognizer.</span><span class="sxs-lookup"><span data-stu-id="62a2d-115">The hint contains an array of characters that represent the restricted set of supported unicode character set supported by this InkRecognizer.</span></span><br/> |
| <span id="GUID_AHP_FACTOID"></span><span id="guid_ahp_factoid"></span><dl> <span data-ttu-id="62a2d-116"><dt>**GUID \_ AHP \_ FACTOID**</dt></span><span class="sxs-lookup"><span data-stu-id="62a2d-116"><dt>**GUID\_AHP\_FACTOID**</dt></span></span> </dl>                                                                   | <span data-ttu-id="62a2d-117">Factoid en una sugerencia de análisis.</span><span class="sxs-lookup"><span data-stu-id="62a2d-117">The factoid on an analysis hint.</span></span><br/>                                                                                                               |
| <span id="GUID_AHP_GUIDE"></span><span id="guid_ahp_guide"></span><dl> <span data-ttu-id="62a2d-118"><dt>**\_Guía de AHP de GUID \_**</dt></span><span class="sxs-lookup"><span data-stu-id="62a2d-118"><dt>**GUID\_AHP\_GUIDE**</dt></span></span> </dl>                                                                         | <span data-ttu-id="62a2d-119">La estructura [**InkAnalysisRecognizerGuide**](inkanalysisrecognizerguide.md) que representa la guía de una sugerencia de análisis.</span><span class="sxs-lookup"><span data-stu-id="62a2d-119">The [**InkAnalysisRecognizerGuide**](inkanalysisrecognizerguide.md) structure that represents the guide for an analysis hint.</span></span><br/>                 |
| <span id="GUID_AHP_PREFIXTEXT"></span><span id="guid_ahp_prefixtext"></span><dl> <span data-ttu-id="62a2d-120"><dt>**GUID \_ AHP \_ PREFIXTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="62a2d-120"><dt>**GUID\_AHP\_PREFIXTEXT**</dt></span></span> </dl>                                                          | <span data-ttu-id="62a2d-121">Texto del prefijo en una sugerencia de análisis.</span><span class="sxs-lookup"><span data-stu-id="62a2d-121">The prefix text on an analysis hint.</span></span><br/>                                                                                                           |
| <span id="GUID_AHP_SUFFIXTEXT"></span><span id="guid_ahp_suffixtext"></span><dl> <span data-ttu-id="62a2d-122"><dt>**GUID \_ AHP \_ SUFFIXTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="62a2d-122"><dt>**GUID\_AHP\_SUFFIXTEXT**</dt></span></span> </dl>                                                          | <span data-ttu-id="62a2d-123">Texto del sufijo en una sugerencia de análisis.</span><span class="sxs-lookup"><span data-stu-id="62a2d-123">The suffix text on an analysis hint.</span></span><br/>                                                                                                           |
| <span id="GUID_AHP_TOPINKBREAKSONLY"></span><span id="guid_ahp_topinkbreaksonly"></span><dl> <span data-ttu-id="62a2d-124"><dt>**GUID \_ AHP \_ TOPINKBREAKSONLY**</dt></span><span class="sxs-lookup"><span data-stu-id="62a2d-124"><dt>**GUID\_AHP\_TOPINKBREAKSONLY**</dt></span></span> </dl>                                        | <span data-ttu-id="62a2d-125">Si se deshabilitan los diversos segmentos de los resultados del reconocimiento de tinta.</span><span class="sxs-lookup"><span data-stu-id="62a2d-125">Whether the multiple segmentations in the ink recognition results are disabled.</span></span><br/>                                                                |
| <span id="GUID_AHP_WORDLIST"></span><span id="guid_ahp_wordlist"></span><dl> <span data-ttu-id="62a2d-126"><dt>**\_AHP de \_ palabras de GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="62a2d-126"><dt>**GUID\_AHP\_WORDLIST**</dt></span></span> </dl>                                                                | <span data-ttu-id="62a2d-127">Matriz de cadenas que representa la lista de palabras de una sugerencia de análisis.</span><span class="sxs-lookup"><span data-stu-id="62a2d-127">The array of strings that represents the word list for an analysis hint.</span></span><br/>                                                                       |
| <span id="GUID_AHP_WORDMODE"></span><span id="guid_ahp_wordmode"></span><dl> <span data-ttu-id="62a2d-128"><dt>**GUID \_ AHP \_ WORDMODE**</dt></span><span class="sxs-lookup"><span data-stu-id="62a2d-128"><dt>**GUID\_AHP\_WORDMODE**</dt></span></span> </dl>                                                                | <span data-ttu-id="62a2d-129">Si el analizador de tinta tiene prioridad sobre los resultados de una sola palabra en los resultados de varias palabras para una sugerencia de análisis.</span><span class="sxs-lookup"><span data-stu-id="62a2d-129">Whether the ink analyzer prioritizes single-word results over multiple-word results for an analysis hint.</span></span><br/>                                      |



## <a name="remarks"></a><span data-ttu-id="62a2d-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62a2d-130">Remarks</span></span>

<span data-ttu-id="62a2d-131">Estos GUID se usan para identificar las propiedades que [**IInkAnalyzer**](iinkanalyzer.md) puede establecer en un nodo de contexto de sugerencia de análisis (vea [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="62a2d-131">These GUIDs are used to identify properties that the [**IInkAnalyzer**](iinkanalyzer.md) can set on an analysis hint context node (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

<span data-ttu-id="62a2d-132">Para obtener o establecer las propiedades de un [**IContextNode**](icontextnode.md) en general, consulte [propiedades del nodo de contexto](context-node-properties.md).</span><span class="sxs-lookup"><span data-stu-id="62a2d-132">To get or set properties of an [**IContextNode**](icontextnode.md) in general, see [Context Node Properties](context-node-properties.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="62a2d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62a2d-133">Requirements</span></span>



| <span data-ttu-id="62a2d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="62a2d-134">Requirement</span></span> | <span data-ttu-id="62a2d-135">Value</span><span class="sxs-lookup"><span data-stu-id="62a2d-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="62a2d-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62a2d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="62a2d-137">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="62a2d-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="62a2d-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62a2d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="62a2d-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="62a2d-139">None supported</span></span><br/>                                                           |
| <span data-ttu-id="62a2d-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62a2d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="62a2d-141"><dt>Iaguid. h</dt></span><span class="sxs-lookup"><span data-stu-id="62a2d-141"><dt>Iaguid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62a2d-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="62a2d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62a2d-143">Propiedades del nodo de contexto</span><span class="sxs-lookup"><span data-stu-id="62a2d-143">Context Node Properties</span></span>](context-node-properties.md)
</dt> <dt>

[<span data-ttu-id="62a2d-144">Tipos de nodo de contexto</span><span class="sxs-lookup"><span data-stu-id="62a2d-144">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="62a2d-145">**IInkAnalyzer:: CreateAnalysisHint (método)**</span><span class="sxs-lookup"><span data-stu-id="62a2d-145">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="62a2d-146">**IInkAnalyzer:: GetAnalysisHintsByName (método)**</span><span class="sxs-lookup"><span data-stu-id="62a2d-146">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="62a2d-147">**IContextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="62a2d-147">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="62a2d-148">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="62a2d-148">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="62a2d-149">**IContextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="62a2d-149">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="62a2d-150">**IContextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="62a2d-150">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="62a2d-151">**IContextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="62a2d-151">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="62a2d-152">**IContextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="62a2d-152">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="62a2d-153">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="62a2d-153">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




