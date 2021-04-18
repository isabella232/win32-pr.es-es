---
description: Agrega datos de trazo para varios trazos a un nodo de reconocedor personalizado.
ms.assetid: 77ded896-8573-42de-a41e-4866894dfe2b
title: 'IInkAnalyzer:: AddStrokesToCustomRecognizer (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6df1b31957f3b4087b51fbad0e7b527c2ede799c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715215"
---
# <a name="iinkanalyzeraddstrokestocustomrecognizer-method"></a><span data-ttu-id="b5f59-103">IInkAnalyzer:: AddStrokesToCustomRecognizer (método)</span><span class="sxs-lookup"><span data-stu-id="b5f59-103">IInkAnalyzer::AddStrokesToCustomRecognizer method</span></span>

<span data-ttu-id="b5f59-104">Agrega datos de trazo para varios trazos a un nodo de reconocedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="b5f59-104">Adds stroke data for multiple strokes to a custom recognizer node.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5f59-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5f59-105">Syntax</span></span>


```C++
HRESULT AddStrokesToCustomRecognizer(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="b5f59-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5f59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5f59-107">*ulStrokeIdsCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5f59-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5f59-108">Número de trazos que se van a agregar.</span><span class="sxs-lookup"><span data-stu-id="b5f59-108">The number of strokes to add.</span></span>

</dd> <dt>

<span data-ttu-id="b5f59-109">*plStrokeIds* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5f59-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5f59-110">Una matriz que contiene los identificadores de trazo.</span><span class="sxs-lookup"><span data-stu-id="b5f59-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="b5f59-111">*ulStrokePacketDescriptionCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5f59-111">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5f59-112">El número de propiedades de cada paquete.</span><span class="sxs-lookup"><span data-stu-id="b5f59-112">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="b5f59-113">*pStrokePacketDescriptionGuids* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5f59-113">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5f59-114">Una matriz que contiene los identificadores de propiedad de paquete.</span><span class="sxs-lookup"><span data-stu-id="b5f59-114">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="b5f59-115">*pulPacketDataCountPerStroke* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5f59-115">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5f59-116">Una matriz que contiene el número de paquetes de cada trazo.</span><span class="sxs-lookup"><span data-stu-id="b5f59-116">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="b5f59-117">*plStrokePacketData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5f59-117">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5f59-118">Una matriz que contiene los datos del paquete para los trazos.</span><span class="sxs-lookup"><span data-stu-id="b5f59-118">An array containing the packet data for the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="b5f59-119">*pCustomRecognizer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5f59-119">*pCustomRecognizer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5f59-120">[**IContextNode**](icontextnode.md) de tipo **CustomRecognizer** al que se van a agregar los trazos.</span><span class="sxs-lookup"><span data-stu-id="b5f59-120">The [**IContextNode**](icontextnode.md) of type **CustomRecognizer** to which to add the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="b5f59-121">*ppContextNodeStrokeAddedTo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b5f59-121">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5f59-122">[**IContextNode**](icontextnode.md) en el que el analizador de tinta ha agregado los trazos.</span><span class="sxs-lookup"><span data-stu-id="b5f59-122">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5f59-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5f59-123">Return value</span></span>

<span data-ttu-id="b5f59-124">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b5f59-124">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b5f59-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5f59-125">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="b5f59-126">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodeStrokeAddedTo* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="b5f59-126">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="b5f59-127">Cuando *ppContextNodeStrokeAddedTo* es **null**, indica que el llamador no está interesado en el valor devuelto del método.</span><span class="sxs-lookup"><span data-stu-id="b5f59-127">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="b5f59-128">[**IInkAnalyzer**](iinkanalyzer.md) agrega los trazos a un [**IContextNode**](icontextnode.md) de tipo **CustomRecognizer** (consulte tipos de [nodo de contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="b5f59-128">The [**IInkAnalyzer**](iinkanalyzer.md) adds the strokes to an [**IContextNode**](icontextnode.md) of type **CustomRecognizer** (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="b5f59-129">Este nodo está en la colección de subnodos del nodo raíz (consulte métodos [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md) y [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="b5f59-129">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="b5f59-130">[**IInkAnalyzer**](iinkanalyzer.md) asigna el identificador de referencia cultural del subproceso de entrada activo a los trazos y agrega los trazos al primer nodo **UnclassifiedInk** bajo el nodo **CustomRecognizer** .</span><span class="sxs-lookup"><span data-stu-id="b5f59-130">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the strokes and adds the strokes to the first **UnclassifiedInk** node under the **CustomRecognizer** node.</span></span> <span data-ttu-id="b5f59-131">Si no existe ningún nodo **UnclassifiedInk** , se crea.</span><span class="sxs-lookup"><span data-stu-id="b5f59-131">If no **UnclassifiedInk** node exists, it is created.</span></span> <span data-ttu-id="b5f59-132">Si el [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) asociado con el nodo **CustomRecognizer** no admite el identificador de referencia cultural, el **IInkAnalyzer** continúa analizando y generando una advertencia [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="b5f59-132">If the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associated with the **CustomRecognizer** node does not support the culture identifier, the **IInkAnalyzer** continues analyzing and generates an [**IAnalysisWarning**](ianalysiswarning.md) warning.</span></span> <span data-ttu-id="b5f59-133">Esta advertencia tiene un valor [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) de **AnalysisWarningCode \_ LanguageIdNotRespected**.</span><span class="sxs-lookup"><span data-stu-id="b5f59-133">This warning has an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) value of **AnalysisWarningCode\_LanguageIdNotRespected**.</span></span>

<span data-ttu-id="b5f59-134">*plStrokePacketData* contiene los datos de paquete de todos los trazos.</span><span class="sxs-lookup"><span data-stu-id="b5f59-134">*plStrokePacketData* contains packet data for all of the strokes.</span></span> <span data-ttu-id="b5f59-135">*pStrokePacketDescriptionGuids* contiene los identificadores únicos globales (GUID) que describen los tipos de datos de paquetes incluidos para cada punto de cada trazo.</span><span class="sxs-lookup"><span data-stu-id="b5f59-135">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="b5f59-136">Para obtener una lista completa de las propiedades de paquete disponibles, consulte [constantes de PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b5f59-136">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="b5f59-137">Solo se pueden agregar trazos con las mismas descripciones de paquete en una única llamada al **método IInkAnalyzer:: AddStrokesToCustomRecognizer**.</span><span class="sxs-lookup"><span data-stu-id="b5f59-137">Only strokes with the same packet descriptions can be added in a single call to **IInkAnalyzer::AddStrokesToCustomRecognizer Method**.</span></span>

 

<span data-ttu-id="b5f59-138">Este método expande la región desfasada a la Unión del valor actual de la región y el rectángulo de selección de los trazos agregados.</span><span class="sxs-lookup"><span data-stu-id="b5f59-138">This method expands the dirty region to the union of the region's current value and the bounding box of the added strokes.</span></span>

<span data-ttu-id="b5f59-139">[**IInkAnalyzer**](iinkanalyzer.md) devuelve un **valor HRESULT** de **E \_ INVALIDARG** en las siguientes circunstancias.</span><span class="sxs-lookup"><span data-stu-id="b5f59-139">The [**IInkAnalyzer**](iinkanalyzer.md) returns an **HRESULT** of **E\_INVALIDARG** under the following circumstances.</span></span>

-   <span data-ttu-id="b5f59-140">El [**IInkAnalyzer**](iinkanalyzer.md) ya contiene un trazo con el mismo identificador que uno de los trazos que se van a agregar.</span><span class="sxs-lookup"><span data-stu-id="b5f59-140">The [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as one of the strokes to be added.</span></span>
-   <span data-ttu-id="b5f59-141">El parámetro *pCustomRecognizer* contiene un nodo de reconocedor personalizado que está asociado a un objeto [**IInkAnalyzer**](iinkanalyzer.md) diferente.</span><span class="sxs-lookup"><span data-stu-id="b5f59-141">The *pCustomRecognizer* parameter contains a custom recognizer node that is associated with a different [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>
-   <span data-ttu-id="b5f59-142">El parámetro *pCustomRecognizer* contiene una [**IContextNode**](icontextnode.md) que no es de tipo **CustomRecognizer**.</span><span class="sxs-lookup"><span data-stu-id="b5f59-142">The *pCustomRecognizer* parameter contains an [**IContextNode**](icontextnode.md) that is not of type **CustomRecognizer**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5f59-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5f59-143">Requirements</span></span>



| <span data-ttu-id="b5f59-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5f59-144">Requirement</span></span> | <span data-ttu-id="b5f59-145">Value</span><span class="sxs-lookup"><span data-stu-id="b5f59-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5f59-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5f59-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b5f59-147">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b5f59-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b5f59-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5f59-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b5f59-149">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b5f59-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b5f59-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5f59-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5f59-151"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b5f59-151"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b5f59-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b5f59-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5f59-153"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5f59-153"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b5f59-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5f59-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5f59-155">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b5f59-155">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b5f59-156">Tipos de nodo de contexto</span><span class="sxs-lookup"><span data-stu-id="b5f59-156">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="b5f59-157">**IInkAnalyzer:: AddStrokeToCustomRecognizer (método)**</span><span class="sxs-lookup"><span data-stu-id="b5f59-157">**IInkAnalyzer::AddStrokeToCustomRecognizer Method**</span></span>](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="b5f59-158">**IInkAnalyzer:: CreateCustomRecognizer (método)**</span><span class="sxs-lookup"><span data-stu-id="b5f59-158">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="b5f59-159">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="b5f59-159">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

