---
description: Agrega datos de trazo para varios trazos al IInkAnalyzer y asigna el identificador de referencia cultural especificado a los trazos.
ms.assetid: 1274b24f-204b-4a84-a7c0-0205b6068ae8
title: 'IInkAnalyzer:: AddStrokesForLanguage (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesForLanguage
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7f1c8bde9f1fe9d9c7123fa3c40540d0fd2660ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275473"
---
# <a name="iinkanalyzeraddstrokesforlanguage-method"></a><span data-ttu-id="9af67-103">IInkAnalyzer:: AddStrokesForLanguage (método)</span><span class="sxs-lookup"><span data-stu-id="9af67-103">IInkAnalyzer::AddStrokesForLanguage method</span></span>

<span data-ttu-id="9af67-104">Agrega datos de trazo para varios trazos al [**IInkAnalyzer**](iinkanalyzer.md) y asigna el identificador de referencia cultural especificado a los trazos.</span><span class="sxs-lookup"><span data-stu-id="9af67-104">Adds stroke data for multiple strokes to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns the specified culture identifier to the strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="9af67-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9af67-105">Syntax</span></span>


```C++
HRESULT AddStrokesForLanguage(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plIdofStrokesToAdd,
  [in]  LONG         lStrokesLCID,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="9af67-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9af67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9af67-107">*ulStrokeIdsCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9af67-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9af67-108">Número de trazos que se van a agregar.</span><span class="sxs-lookup"><span data-stu-id="9af67-108">The number of strokes to add.</span></span>

</dd> <dt>

<span data-ttu-id="9af67-109">*plIdofStrokesToAdd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9af67-109">*plIdofStrokesToAdd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9af67-110">Una matriz que contiene los identificadores de trazo.</span><span class="sxs-lookup"><span data-stu-id="9af67-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="9af67-111">*lStrokesLCID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9af67-111">*lStrokesLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9af67-112">Valor que representa el identificador de referencia cultural que se va a asignar a los trazos.</span><span class="sxs-lookup"><span data-stu-id="9af67-112">A value that represents the culture identifier to assign to the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="9af67-113">*ulStrokePacketDescriptionCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9af67-113">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9af67-114">El número de propiedades de cada paquete.</span><span class="sxs-lookup"><span data-stu-id="9af67-114">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="9af67-115">*pStrokePacketDescriptionGuids* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9af67-115">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9af67-116">Una matriz que contiene los identificadores de propiedad de paquete.</span><span class="sxs-lookup"><span data-stu-id="9af67-116">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="9af67-117">*pulPacketDataCountPerStroke* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9af67-117">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9af67-118">Una matriz que contiene el número de paquetes de cada trazo.</span><span class="sxs-lookup"><span data-stu-id="9af67-118">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="9af67-119">*plStrokePacketData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9af67-119">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9af67-120">Una matriz que contiene los datos del paquete para los trazos.</span><span class="sxs-lookup"><span data-stu-id="9af67-120">An array containing the packet data for the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="9af67-121">*ppContextNodeStrokeAddedTo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9af67-121">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9af67-122">[**IContextNode**](icontextnode.md) en el que el analizador de tinta ha agregado los trazos.</span><span class="sxs-lookup"><span data-stu-id="9af67-122">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9af67-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9af67-123">Return value</span></span>

<span data-ttu-id="9af67-124">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9af67-124">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9af67-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9af67-125">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="9af67-126">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodeStrokeAddedTo* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="9af67-126">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="9af67-127">Cuando *ppContextNodeStrokeAddedTo* es **null**, indica que el llamador no está interesado en el valor devuelto del método.</span><span class="sxs-lookup"><span data-stu-id="9af67-127">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="9af67-128">[**IInkAnalyzer**](iinkanalyzer.md) agrega los trazos a un [**IContextNode**](icontextnode.md) de tipo UnclassifiedInk (consulte tipos de [nodo de contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="9af67-128">The [**IInkAnalyzer**](iinkanalyzer.md) adds the strokes to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="9af67-129">Este nodo está en la colección de subnodos del nodo raíz (consulte métodos [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md) y [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="9af67-129">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="9af67-130">[**IInkAnalyzer**](iinkanalyzer.md) asigna el identificador de referencia cultural de *lStrokeLCID* a los trazos y agrega los trazos al primer nodo de contexto UnclassifiedInk en el nodo raíz del analizador de tinta que contiene los trazos con el mismo identificador de referencia cultural.</span><span class="sxs-lookup"><span data-stu-id="9af67-130">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the *lStrokeLCID* culture identifier to the strokes and adds the strokes to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="9af67-131">Si el analizador de tintas no tiene un nodo con el mismo identificador de referencia cultural, crea un nuevo nodo de contexto UnclassifiedInk en el nodo raíz y agrega los trazos al nuevo nodo de contexto UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="9af67-131">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the strokes to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="9af67-132">*plStrokePacketData* contiene los datos de paquete de todos los trazos.</span><span class="sxs-lookup"><span data-stu-id="9af67-132">*plStrokePacketData* contains packet data for all of the strokes.</span></span> <span data-ttu-id="9af67-133">*pStrokePacketDescriptionGuids* contiene los identificadores únicos globales (GUID) que describen los tipos de datos de paquetes incluidos para cada punto de cada trazo.</span><span class="sxs-lookup"><span data-stu-id="9af67-133">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="9af67-134">Para obtener una lista completa de las propiedades de paquete disponibles, consulte [constantes de PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9af67-134">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="9af67-135">Solo se pueden agregar trazos con las mismas descripciones de paquete en una única llamada al [**método IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md).</span><span class="sxs-lookup"><span data-stu-id="9af67-135">Only strokes with the same packet descriptions can be added in a single call to [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md).</span></span>

 

<span data-ttu-id="9af67-136">Este método expande la región desfasada a la Unión del valor actual de la región y el rectángulo de selección de los trazos agregados.</span><span class="sxs-lookup"><span data-stu-id="9af67-136">This method expands the dirty region to the union of the region's current value and the bounding box of the added strokes.</span></span>

<span data-ttu-id="9af67-137">Si el [**IInkAnalyzer**](iinkanalyzer.md) ya contiene un trazo con el mismo identificador que uno de los trazos que se van a agregar, el **IInkAnalyzer** devuelve un **valor HRESULT** de **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="9af67-137">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as one of the strokes to be added, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9af67-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9af67-138">Requirements</span></span>



| <span data-ttu-id="9af67-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="9af67-139">Requirement</span></span> | <span data-ttu-id="9af67-140">Value</span><span class="sxs-lookup"><span data-stu-id="9af67-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9af67-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9af67-141">Minimum supported client</span></span><br/> | <span data-ttu-id="9af67-142">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9af67-142">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9af67-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9af67-143">Minimum supported server</span></span><br/> | <span data-ttu-id="9af67-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9af67-144">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9af67-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9af67-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="9af67-146"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9af67-146"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9af67-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9af67-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9af67-148"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9af67-148"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9af67-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="9af67-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9af67-150">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="9af67-150">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="9af67-151">**IInkAnalyzer:: AddStroke (método)**</span><span class="sxs-lookup"><span data-stu-id="9af67-151">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="9af67-152">**IInkAnalyzer:: AddStrokeForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="9af67-152">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="9af67-153">**IInkAnalyzer:: AddStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="9af67-153">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="9af67-154">**IInkAnalyzer:: RemoveStroke (método)**</span><span class="sxs-lookup"><span data-stu-id="9af67-154">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="9af67-155">**IInkAnalyzer:: RemoveStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="9af67-155">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="9af67-156">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="9af67-156">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

