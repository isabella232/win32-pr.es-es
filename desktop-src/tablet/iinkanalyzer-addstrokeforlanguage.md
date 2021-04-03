---
description: Agrega datos de trazo para un solo trazo al IInkAnalyzer y asigna un identificador de referencia cultural específico al trazo.
ms.assetid: 65eb805e-05ed-4144-b17e-872c47ab33fa
title: 'IInkAnalyzer:: AddStrokeForLanguage (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeForLanguage
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 674a58ef891d919d09f86f28a35748de3537db91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908017"
---
# <a name="iinkanalyzeraddstrokeforlanguage-method"></a><span data-ttu-id="21b5c-103">IInkAnalyzer:: AddStrokeForLanguage (método)</span><span class="sxs-lookup"><span data-stu-id="21b5c-103">IInkAnalyzer::AddStrokeForLanguage method</span></span>

<span data-ttu-id="21b5c-104">Agrega datos de trazo para un solo trazo al [**IInkAnalyzer**](iinkanalyzer.md) y asigna un identificador de referencia cultural específico al trazo.</span><span class="sxs-lookup"><span data-stu-id="21b5c-104">Adds stroke data for a single stroke to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns a specific culture identifier to the stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="21b5c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21b5c-105">Syntax</span></span>


```C++
HRESULT AddStrokeForLanguage(
  [in]  LONG         lStrokeId,
  [in]  LONG         lStrokeLCID,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="21b5c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21b5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21b5c-107">*lStrokeId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21b5c-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21b5c-108">Identificador del trazo que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="21b5c-108">The identifier for the stroke to add.</span></span>

</dd> <dt>

<span data-ttu-id="21b5c-109">*lStrokeLCID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21b5c-109">*lStrokeLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21b5c-110">Identificador de referencia cultural que se va a asignar al trazo.</span><span class="sxs-lookup"><span data-stu-id="21b5c-110">The culture identifier to assign to the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="21b5c-111">*ulStrokePacketDataCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21b5c-111">*ulStrokePacketDataCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21b5c-112">Número de paquetes del trazo.</span><span class="sxs-lookup"><span data-stu-id="21b5c-112">The number of packets in the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="21b5c-113">*plStrokePacketData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21b5c-113">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21b5c-114">Una matriz que contiene los datos del paquete del trazo.</span><span class="sxs-lookup"><span data-stu-id="21b5c-114">An array containing the packet data for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="21b5c-115">*ulStrokePacketDescriptionCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21b5c-115">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21b5c-116">El número de propiedades de cada paquete.</span><span class="sxs-lookup"><span data-stu-id="21b5c-116">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="21b5c-117">*pStrokePacketDescriptionGuids* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21b5c-117">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21b5c-118">Una matriz que contiene los identificadores de propiedad de paquete.</span><span class="sxs-lookup"><span data-stu-id="21b5c-118">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="21b5c-119">*ppContextNodeStrokeAddedTo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="21b5c-119">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21b5c-120">Puntero cuyo valor se establece en el puntero del [**IContextNode**](icontextnode.md) que contiene el trazo que se acaba de agregar.</span><span class="sxs-lookup"><span data-stu-id="21b5c-120">A pointer whose value is set to the pointer of the [**IContextNode**](icontextnode.md) that contains the newly added stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21b5c-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21b5c-121">Return value</span></span>

<span data-ttu-id="21b5c-122">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="21b5c-122">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="21b5c-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21b5c-123">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="21b5c-124">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodeStrokeAddedTo* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="21b5c-124">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="21b5c-125">Cuando *ppContextNodeStrokeAddedTo* es **null**, indica que el llamador no está interesado en el valor devuelto del método.</span><span class="sxs-lookup"><span data-stu-id="21b5c-125">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="21b5c-126">El [**IInkAnalyzer**](iinkanalyzer.md) agrega el trazo a un [**IContextNode**](icontextnode.md) de tipo UnclassifiedInk (consulte [tipos de nodo de contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="21b5c-126">The [**IInkAnalyzer**](iinkanalyzer.md) adds the stroke to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="21b5c-127">Este nodo está en la colección de subnodos del nodo raíz (consulte métodos [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md) y [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="21b5c-127">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="21b5c-128">[**IInkAnalyzer**](iinkanalyzer.md) asigna el identificador de referencia cultural de *lStrokeLCID* al trazo y agrega el trazo al primer nodo de contexto UnclassifiedInk en el nodo raíz del analizador de tinta que contiene los trazos con el mismo identificador de referencia cultural.</span><span class="sxs-lookup"><span data-stu-id="21b5c-128">The [**IInkAnalyzer**](iinkanalyzer.md) assigns *lStrokeLCID* culture identifier to the stroke and adds the stroke to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="21b5c-129">Si el analizador de tintas no tiene un nodo con el mismo identificador de referencia cultural, crea un nuevo nodo de contexto UnclassifiedInk en el nodo raíz y agrega el trazo al nuevo nodo de contexto UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="21b5c-129">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the stroke to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="21b5c-130">*plStrokePacketData* contiene datos de paquetes para todos los puntos del trazo.</span><span class="sxs-lookup"><span data-stu-id="21b5c-130">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="21b5c-131">*pStrokePacketDescriptionGuids* contiene los identificadores únicos globales (GUID) que describen los tipos de datos de paquete incluidos para cada punto del trazo.</span><span class="sxs-lookup"><span data-stu-id="21b5c-131">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in the stroke.</span></span> <span data-ttu-id="21b5c-132">Para obtener una lista completa de las propiedades de paquete disponibles, consulte [constantes de PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="21b5c-132">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="21b5c-133">Este método expande la región desfasada a la Unión del valor actual de la región y el rectángulo de selección del trazo agregado.</span><span class="sxs-lookup"><span data-stu-id="21b5c-133">This method expands the dirty region to the union of the region's current value and the bounding box of the added stroke.</span></span>

<span data-ttu-id="21b5c-134">Si el [**IInkAnalyzer**](iinkanalyzer.md) ya contiene un trazo con el mismo identificador de trazo, el **IInkAnalyzer** devuelve un **valor HRESULT** de **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="21b5c-134">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same stroke identifier, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="21b5c-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21b5c-135">Requirements</span></span>



| <span data-ttu-id="21b5c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="21b5c-136">Requirement</span></span> | <span data-ttu-id="21b5c-137">Value</span><span class="sxs-lookup"><span data-stu-id="21b5c-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21b5c-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21b5c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="21b5c-139">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="21b5c-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="21b5c-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21b5c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="21b5c-141">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="21b5c-141">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="21b5c-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21b5c-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="21b5c-143"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="21b5c-143"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="21b5c-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="21b5c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21b5c-145"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21b5c-145"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="21b5c-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="21b5c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21b5c-147">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="21b5c-147">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="21b5c-148">**IInkAnalyzer:: AddStroke (método)**</span><span class="sxs-lookup"><span data-stu-id="21b5c-148">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="21b5c-149">**IInkAnalyzer:: AddStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="21b5c-149">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="21b5c-150">**IInkAnalyzer:: AddStrokesForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="21b5c-150">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="21b5c-151">**IInkAnalyzer:: RemoveStroke (método)**</span><span class="sxs-lookup"><span data-stu-id="21b5c-151">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="21b5c-152">**IInkAnalyzer:: RemoveStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="21b5c-152">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="21b5c-153">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="21b5c-153">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

