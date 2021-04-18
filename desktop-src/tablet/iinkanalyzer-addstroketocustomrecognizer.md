---
description: Agrega datos de trazo para un solo trazo a un nodo de reconocedor personalizado.
ms.assetid: ab43c9f8-15fe-49db-b9d1-57d34b95d99f
title: 'IInkAnalyzer:: AddStrokeToCustomRecognizer (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c04b60acd2f40b5ed3960c9932ce066b337d81cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715214"
---
# <a name="iinkanalyzeraddstroketocustomrecognizer-method"></a><span data-ttu-id="8ffad-103">IInkAnalyzer:: AddStrokeToCustomRecognizer (método)</span><span class="sxs-lookup"><span data-stu-id="8ffad-103">IInkAnalyzer::AddStrokeToCustomRecognizer method</span></span>

<span data-ttu-id="8ffad-104">Agrega datos de trazo para un solo trazo a un nodo de reconocedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="8ffad-104">Adds stroke data for a single stroke to a custom recognizer node.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ffad-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ffad-105">Syntax</span></span>


```C++
HRESULT AddStrokeToCustomRecognizer(
  [in]  ULONG        ulStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="8ffad-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ffad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ffad-107">*ulStrokeId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ffad-107">*ulStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffad-108">Identificador del trazo que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="8ffad-108">The identifier for the stroke to add.</span></span>

</dd> <dt>

<span data-ttu-id="8ffad-109">*ulStrokePacketDataCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ffad-109">*ulStrokePacketDataCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffad-110">Número de paquetes del trazo.</span><span class="sxs-lookup"><span data-stu-id="8ffad-110">The number of packets in the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="8ffad-111">*plStrokePacketData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ffad-111">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffad-112">Una matriz que contiene los datos del paquete del trazo.</span><span class="sxs-lookup"><span data-stu-id="8ffad-112">An array containing the packet data for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="8ffad-113">*ulStrokePacketDescriptionCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ffad-113">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffad-114">El número de propiedades de paquete en cada paquete.</span><span class="sxs-lookup"><span data-stu-id="8ffad-114">The number of packet properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="8ffad-115">*pStrokePacketDescriptionGuids* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ffad-115">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffad-116">Una matriz que contiene los identificadores de propiedad de paquete.</span><span class="sxs-lookup"><span data-stu-id="8ffad-116">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="8ffad-117">*pCustomRecognizer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ffad-117">*pCustomRecognizer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffad-118">[**IContextNode**](icontextnode.md) de tipo **CustomRecognizer** al que se va a agregar el trazo.</span><span class="sxs-lookup"><span data-stu-id="8ffad-118">The [**IContextNode**](icontextnode.md) of type **CustomRecognizer** to which to add the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="8ffad-119">*ppContextNodeStrokeAddedTo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8ffad-119">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffad-120">[**IContextNode**](icontextnode.md) en el que el analizador de tinta ha agregado el trazo.</span><span class="sxs-lookup"><span data-stu-id="8ffad-120">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ffad-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ffad-121">Return value</span></span>

<span data-ttu-id="8ffad-122">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8ffad-122">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8ffad-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ffad-123">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="8ffad-124">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodeStrokeAddedTo* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="8ffad-124">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="8ffad-125">Cuando *ppContextNodeStrokeAddedTo* es **null**, indica que el llamador no está interesado en el valor devuelto del método.</span><span class="sxs-lookup"><span data-stu-id="8ffad-125">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="8ffad-126">El [**IInkAnalyzer**](iinkanalyzer.md) agrega el trazo a un [**IContextNode**](icontextnode.md) de tipo **CustomRecognizer** (consulte [tipos de nodo de contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="8ffad-126">The [**IInkAnalyzer**](iinkanalyzer.md) adds the stroke to an [**IContextNode**](icontextnode.md) of type **CustomRecognizer** (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="8ffad-127">Este nodo está en la colección de subnodos del nodo raíz (consulte métodos [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md) y [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="8ffad-127">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="8ffad-128">[**IInkAnalyzer**](iinkanalyzer.md) asigna el identificador de referencia cultural del subproceso de entrada activo al trazo y agrega el trazo al primer nodo **UnclassifiedInk** bajo el nodo **CustomRecognizer** .</span><span class="sxs-lookup"><span data-stu-id="8ffad-128">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the stroke and adds the stroke to the first **UnclassifiedInk** node under the **CustomRecognizer** node.</span></span> <span data-ttu-id="8ffad-129">Si no existe ningún nodo **UnclassifiedInk** , se crea.</span><span class="sxs-lookup"><span data-stu-id="8ffad-129">If no **UnclassifiedInk** node exists, it is created.</span></span> <span data-ttu-id="8ffad-130">Si el [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) asociado con el nodo **CustomRecognizer** no admite el identificador de referencia cultural, el **IInkAnalyzer** continúa analizando y generando una advertencia [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="8ffad-130">If the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associated with the **CustomRecognizer** node does not support the culture identifier, the **IInkAnalyzer** continues analyzing and generates an [**IAnalysisWarning**](ianalysiswarning.md) warning.</span></span> <span data-ttu-id="8ffad-131">Esta advertencia tiene un valor [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) de **AnalysisWarningCode \_ LanguageIdNotRespected**.</span><span class="sxs-lookup"><span data-stu-id="8ffad-131">This warning has an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) value of **AnalysisWarningCode\_LanguageIdNotRespected**.</span></span>

<span data-ttu-id="8ffad-132">*plStrokePacketData* contiene datos de paquetes para todos los puntos del trazo.</span><span class="sxs-lookup"><span data-stu-id="8ffad-132">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="8ffad-133">*pStrokePacketDescriptionGuids* contiene los identificadores únicos globales (GUID) que describen los tipos de datos de paquetes incluidos para cada punto de cada trazo.</span><span class="sxs-lookup"><span data-stu-id="8ffad-133">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="8ffad-134">Para obtener una lista completa de las propiedades de paquete disponibles, consulte [constantes de PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="8ffad-134">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="8ffad-135">Este método expande la región desfasada a la Unión del valor actual de la región y el rectángulo de selección del trazo agregado.</span><span class="sxs-lookup"><span data-stu-id="8ffad-135">This method expands the dirty region to the union of the region's current value and the bounding box of the added stroke.</span></span>

<span data-ttu-id="8ffad-136">[**IInkAnalyzer**](iinkanalyzer.md) devuelve un **valor HRESULT** de **E \_ INVALIDARG** en las siguientes circunstancias.</span><span class="sxs-lookup"><span data-stu-id="8ffad-136">The [**IInkAnalyzer**](iinkanalyzer.md) returns an **HRESULT** of **E\_INVALIDARG** under the following circumstances.</span></span>

-   <span data-ttu-id="8ffad-137">El [**IInkAnalyzer**](iinkanalyzer.md) ya contiene un trazo con el mismo identificador que el trazo que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="8ffad-137">The [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as the stroke to be added.</span></span>
-   <span data-ttu-id="8ffad-138">El parámetro *pCustomRecognizer* contiene un nodo de reconocedor personalizado que está asociado a un objeto [**IInkAnalyzer**](iinkanalyzer.md) diferente.</span><span class="sxs-lookup"><span data-stu-id="8ffad-138">The *pCustomRecognizer* parameter contains a custom recognizer node that is associated with a different [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>
-   <span data-ttu-id="8ffad-139">El parámetro *pCustomRecognizer* contiene una [**IContextNode**](icontextnode.md) que no es de tipo **CustomRecognizer**.</span><span class="sxs-lookup"><span data-stu-id="8ffad-139">The *pCustomRecognizer* parameter contains an [**IContextNode**](icontextnode.md) that is not of type **CustomRecognizer**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ffad-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ffad-140">Requirements</span></span>



| <span data-ttu-id="8ffad-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ffad-141">Requirement</span></span> | <span data-ttu-id="8ffad-142">Value</span><span class="sxs-lookup"><span data-stu-id="8ffad-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ffad-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ffad-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8ffad-144">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8ffad-144">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8ffad-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ffad-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8ffad-146">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8ffad-146">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8ffad-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ffad-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ffad-148"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8ffad-148"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8ffad-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8ffad-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ffad-150"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ffad-150"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8ffad-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ffad-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ffad-152">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="8ffad-152">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="8ffad-153">Tipos de nodo de contexto</span><span class="sxs-lookup"><span data-stu-id="8ffad-153">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="8ffad-154">**IInkAnalyzer:: AddStrokesToCustomRecognizer (método)**</span><span class="sxs-lookup"><span data-stu-id="8ffad-154">**IInkAnalyzer::AddStrokesToCustomRecognizer Method**</span></span>](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="8ffad-155">**IInkAnalyzer:: CreateCustomRecognizer (método)**</span><span class="sxs-lookup"><span data-stu-id="8ffad-155">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="8ffad-156">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="8ffad-156">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

