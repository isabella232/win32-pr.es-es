---
description: Agrega datos de trazo para varios trazos al IInkAnalyzer y asigna el identificador de referencia cultural del subproceso de entrada activo a los trazos.
ms.assetid: 4a8d6828-699b-465d-b057-197866ff069f
title: 'IInkAnalyzer:: AddStrokes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc616f8a388010df2b3d39ea55622d81fa5ce3a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696524"
---
# <a name="iinkanalyzeraddstrokes-method"></a><span data-ttu-id="9d148-103">IInkAnalyzer:: AddStrokes (método)</span><span class="sxs-lookup"><span data-stu-id="9d148-103">IInkAnalyzer::AddStrokes method</span></span>

<span data-ttu-id="9d148-104">Agrega datos de trazo para varios trazos al [**IInkAnalyzer**](iinkanalyzer.md) y asigna el identificador de referencia cultural del subproceso de entrada activo a los trazos.</span><span class="sxs-lookup"><span data-stu-id="9d148-104">Adds stroke data for multiple strokes to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns the active input thread's culture identifier to the strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d148-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d148-105">Syntax</span></span>


```C++
HRESULT AddStrokes(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="9d148-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d148-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d148-107">*ulStrokeIdsCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9d148-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d148-108">Número de trazos que se van a agregar.</span><span class="sxs-lookup"><span data-stu-id="9d148-108">The number of strokes to add.</span></span>

</dd> <dt>

<span data-ttu-id="9d148-109">*plStrokeIds* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9d148-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d148-110">Una matriz que contiene los identificadores de trazo.</span><span class="sxs-lookup"><span data-stu-id="9d148-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="9d148-111">*ulStrokePacketDescriptionCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9d148-111">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d148-112">El número de propiedades de cada paquete.</span><span class="sxs-lookup"><span data-stu-id="9d148-112">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="9d148-113">*pStrokePacketDescriptionGuids* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9d148-113">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d148-114">Una matriz que contiene los identificadores de propiedad de paquete.</span><span class="sxs-lookup"><span data-stu-id="9d148-114">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="9d148-115">*pulPacketDataCountPerStroke* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9d148-115">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d148-116">Una matriz que contiene el número de paquetes de cada trazo.</span><span class="sxs-lookup"><span data-stu-id="9d148-116">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="9d148-117">*plStrokePacketData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9d148-117">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d148-118">Una matriz que contiene los datos del paquete para los trazos.</span><span class="sxs-lookup"><span data-stu-id="9d148-118">An array containing the packet data for the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="9d148-119">*ppContextNodeStrokeAddedTo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9d148-119">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d148-120">[**IContextNode**](icontextnode.md) en el que el analizador de tinta ha agregado los trazos.</span><span class="sxs-lookup"><span data-stu-id="9d148-120">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d148-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d148-121">Return value</span></span>

<span data-ttu-id="9d148-122">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9d148-122">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9d148-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9d148-123">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="9d148-124">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodeStrokeAddedTo* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="9d148-124">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="9d148-125">Cuando *ppContextNodeStrokeAddedTo* es **null**, indica que el llamador no está interesado en el valor devuelto del método.</span><span class="sxs-lookup"><span data-stu-id="9d148-125">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="9d148-126">[**IInkAnalyzer**](iinkanalyzer.md) agrega los trazos a un [**IContextNode**](icontextnode.md) de tipo UnclassifiedInk (consulte tipos de [nodo de contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="9d148-126">The [**IInkAnalyzer**](iinkanalyzer.md) adds the strokes to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="9d148-127">Este nodo está en la colección de subnodos del nodo raíz (consulte métodos [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md) y [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="9d148-127">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="9d148-128">[**IInkAnalyzer**](iinkanalyzer.md) asigna el identificador de referencia cultural del subproceso de entrada activo a los trazos y agrega los trazos al primer nodo de contexto UnclassifiedInk bajo el nodo raíz del analizador de tinta que contiene los trazos con el mismo identificador de referencia cultural.</span><span class="sxs-lookup"><span data-stu-id="9d148-128">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the strokes and adds the strokes to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="9d148-129">Si el analizador de tintas no tiene un nodo con el mismo identificador de referencia cultural, crea un nuevo nodo de contexto UnclassifiedInk en el nodo raíz y agrega los trazos al nuevo nodo de contexto UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="9d148-129">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the strokes to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="9d148-130">*plStrokePacketData* contiene los datos de paquete de todos los trazos.</span><span class="sxs-lookup"><span data-stu-id="9d148-130">*plStrokePacketData* contains packet data for all of the strokes.</span></span> <span data-ttu-id="9d148-131">*pStrokePacketDescriptionGuids* contiene los identificadores únicos globales (GUID) que describen los tipos de datos de paquetes incluidos para cada punto de cada trazo.</span><span class="sxs-lookup"><span data-stu-id="9d148-131">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="9d148-132">Para obtener una lista completa de las propiedades de paquete disponibles, consulte [constantes de PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9d148-132">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="9d148-133">Solo se pueden agregar trazos con las mismas descripciones de paquete en una única llamada al **método IInkAnalyzer:: AddStrokes**.</span><span class="sxs-lookup"><span data-stu-id="9d148-133">Only strokes with the same packet descriptions can be added in a single call to **IInkAnalyzer::AddStrokes Method**.</span></span>

 

<span data-ttu-id="9d148-134">Este método expande la región desfasada a la Unión del valor actual de la región y el rectángulo de selección de los trazos agregados.</span><span class="sxs-lookup"><span data-stu-id="9d148-134">This method expands the dirty region to the union of the region's current value and the bounding box of the added strokes.</span></span>

<span data-ttu-id="9d148-135">Si el [**IInkAnalyzer**](iinkanalyzer.md) ya contiene un trazo con el mismo identificador que uno de los trazos que se van a agregar, el **IInkAnalyzer** devuelve un **valor HRESULT** de **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="9d148-135">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as one of the strokes to be added, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d148-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d148-136">Requirements</span></span>



| <span data-ttu-id="9d148-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d148-137">Requirement</span></span> | <span data-ttu-id="9d148-138">Value</span><span class="sxs-lookup"><span data-stu-id="9d148-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d148-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d148-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9d148-140">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9d148-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9d148-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d148-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9d148-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9d148-142">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9d148-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d148-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d148-144"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9d148-144"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9d148-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9d148-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d148-146"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d148-146"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9d148-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d148-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d148-148">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="9d148-148">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="9d148-149">**IInkAnalyzer:: AddStroke (método)**</span><span class="sxs-lookup"><span data-stu-id="9d148-149">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="9d148-150">**IInkAnalyzer:: AddStrokeForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="9d148-150">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="9d148-151">**IInkAnalyzer:: AddStrokesForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="9d148-151">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="9d148-152">**IInkAnalyzer:: RemoveStroke (método)**</span><span class="sxs-lookup"><span data-stu-id="9d148-152">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="9d148-153">**IInkAnalyzer:: RemoveStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="9d148-153">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="9d148-154">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="9d148-154">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

