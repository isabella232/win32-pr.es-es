---
description: Agrega datos de trazo para un solo trazo al IInkAnalyzer y asigna el identificador de referencia cultural del subproceso de entrada activo al trazo.
ms.assetid: 0e603e5a-d722-4ab8-bc59-605e131c863b
title: 'IInkAnalyzer:: AddStroke (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc946e7975772eb7be6fff54d01bb1a6dae8ebe7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275474"
---
# <a name="iinkanalyzeraddstroke-method"></a><span data-ttu-id="a6bec-103">IInkAnalyzer:: AddStroke (método)</span><span class="sxs-lookup"><span data-stu-id="a6bec-103">IInkAnalyzer::AddStroke method</span></span>

<span data-ttu-id="a6bec-104">Agrega datos de trazo para un solo trazo al [**IInkAnalyzer**](iinkanalyzer.md) y asigna el identificador de referencia cultural del subproceso de entrada activo al trazo.</span><span class="sxs-lookup"><span data-stu-id="a6bec-104">Adds stroke data for a single stroke to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns the active input thread's culture identifier to the stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6bec-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6bec-105">Syntax</span></span>


```C++
HRESULT AddStroke(
  [in]  LONG         lStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="a6bec-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6bec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6bec-107">*lStrokeId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a6bec-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6bec-108">Identificador del trazo que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="a6bec-108">The identifier for the stroke to add.</span></span>

</dd> <dt>

<span data-ttu-id="a6bec-109">*ulStrokePacketDataCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a6bec-109">*ulStrokePacketDataCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6bec-110">Número de paquetes del trazo.</span><span class="sxs-lookup"><span data-stu-id="a6bec-110">The number of packets in the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="a6bec-111">*plStrokePacketData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a6bec-111">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6bec-112">Una matriz que contiene los datos del paquete del trazo.</span><span class="sxs-lookup"><span data-stu-id="a6bec-112">An array containing the packet data for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="a6bec-113">*ulStrokePacketDescriptionCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a6bec-113">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6bec-114">El número de propiedades de paquete en cada paquete.</span><span class="sxs-lookup"><span data-stu-id="a6bec-114">The number of packet properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="a6bec-115">*pStrokePacketDescriptionGuids* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a6bec-115">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6bec-116">Una matriz que contiene los identificadores de propiedad de paquete.</span><span class="sxs-lookup"><span data-stu-id="a6bec-116">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="a6bec-117">*ppContextNodeStrokeAddedTo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a6bec-117">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6bec-118">Puntero al [**IContextNode**](icontextnode.md) en el que el [**IInkAnalyzer**](iinkanalyzer.md) agregó el trazo.</span><span class="sxs-lookup"><span data-stu-id="a6bec-118">A pointer to the [**IContextNode**](icontextnode.md) to which the [**IInkAnalyzer**](iinkanalyzer.md) added the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6bec-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6bec-119">Return value</span></span>

<span data-ttu-id="a6bec-120">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a6bec-120">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a6bec-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6bec-121">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="a6bec-122">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodeStrokeAddedTo* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="a6bec-122">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="a6bec-123">Cuando *ppContextNodeStrokeAddedTo* es **null**, indica que el llamador no está interesado en el valor devuelto del método.</span><span class="sxs-lookup"><span data-stu-id="a6bec-123">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="a6bec-124">El [**IInkAnalyzer**](iinkanalyzer.md) agrega el trazo a un [**IContextNode**](icontextnode.md) de tipo UnclassifiedInk (consulte [tipos de nodo de contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="a6bec-124">The [**IInkAnalyzer**](iinkanalyzer.md) adds the stroke to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="a6bec-125">Este nodo está en la colección de subnodos del nodo raíz (consulte métodos [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md) y [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="a6bec-125">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="a6bec-126">[**IInkAnalyzer**](iinkanalyzer.md) asigna el identificador de referencia cultural del subproceso de entrada activo al trazo y agrega el trazo al primer nodo de contexto UnclassifiedInk bajo el nodo raíz del analizador de tinta que contiene los trazos con el mismo identificador de referencia cultural.</span><span class="sxs-lookup"><span data-stu-id="a6bec-126">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the stroke and adds the stroke to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="a6bec-127">Si el analizador de tintas no tiene un nodo con el mismo identificador de referencia cultural, crea un nuevo nodo de contexto UnclassifiedInk en el nodo raíz y agrega el trazo al nuevo nodo de contexto UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="a6bec-127">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the stroke to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="a6bec-128">*plStrokePacketData* contiene datos de paquetes para todos los puntos del trazo.</span><span class="sxs-lookup"><span data-stu-id="a6bec-128">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="a6bec-129">*pStrokePacketDescriptionGuids* contiene los identificadores únicos globales (GUID) que describen los tipos de datos de paquete incluidos para cada punto del trazo.</span><span class="sxs-lookup"><span data-stu-id="a6bec-129">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in the stroke.</span></span> <span data-ttu-id="a6bec-130">Para obtener una lista completa de las propiedades de paquete disponibles, consulte [constantes de PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a6bec-130">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="a6bec-131">Este método expande la región desfasada a la Unión del valor actual de la región y el rectángulo de selección del trazo agregado.</span><span class="sxs-lookup"><span data-stu-id="a6bec-131">This method expands the dirty region to the union of the region's current value and the bounding box of the added stroke.</span></span>

<span data-ttu-id="a6bec-132">Si el [**IInkAnalyzer**](iinkanalyzer.md) ya contiene un trazo con el mismo identificador de trazo, el **IInkAnalyzer** devuelve un **valor HRESULT** de **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="a6bec-132">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same stroke identifier, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6bec-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6bec-133">Requirements</span></span>



| <span data-ttu-id="a6bec-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6bec-134">Requirement</span></span> | <span data-ttu-id="a6bec-135">Value</span><span class="sxs-lookup"><span data-stu-id="a6bec-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6bec-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6bec-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a6bec-137">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a6bec-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a6bec-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6bec-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a6bec-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a6bec-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a6bec-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6bec-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6bec-141"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a6bec-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a6bec-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a6bec-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6bec-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6bec-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a6bec-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6bec-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6bec-145">**InkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a6bec-145">**InkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a6bec-146">**IInkAnalyzer:: AddStrokeForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="a6bec-146">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="a6bec-147">**IInkAnalyzer:: AddStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="a6bec-147">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="a6bec-148">**IInkAnalyzer:: AddStrokesForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="a6bec-148">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="a6bec-149">**IInkAnalyzer:: RemoveStroke (método)**</span><span class="sxs-lookup"><span data-stu-id="a6bec-149">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="a6bec-150">**IInkAnalyzer:: RemoveStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="a6bec-150">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="a6bec-151">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="a6bec-151">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

