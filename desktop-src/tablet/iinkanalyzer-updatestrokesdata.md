---
description: Actualiza los datos del paquete para los trazos especificados.
ms.assetid: 7fca4c39-eef2-4019-86a0-27cd0e4e7510
title: 'IInkAnalyzer:: UpdateStrokesData (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.UpdateStrokesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 151403a7114bca2644d0425fdba0155135ac9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705693"
---
# <a name="iinkanalyzerupdatestrokesdata-method"></a><span data-ttu-id="82d4f-103">IInkAnalyzer:: UpdateStrokesData (método)</span><span class="sxs-lookup"><span data-stu-id="82d4f-103">IInkAnalyzer::UpdateStrokesData method</span></span>

<span data-ttu-id="82d4f-104">Actualiza los datos del paquete para los trazos especificados.</span><span class="sxs-lookup"><span data-stu-id="82d4f-104">Updates the packet data for the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="82d4f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82d4f-105">Syntax</span></span>


```C++
HRESULT UpdateStrokesData(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds,
  [in] ULONG ulStrokePacketDescriptionCount,
  [in] GUID  *pStrokePacketDescriptionGuids,
  [in] ULONG *pulPacketDataCountPerStroke,
  [in] LONG  *plStrokePacketData
);
```



## <a name="parameters"></a><span data-ttu-id="82d4f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82d4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82d4f-107">*ulStrokeIdsCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82d4f-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82d4f-108">Número de trazos que se van a actualizar.</span><span class="sxs-lookup"><span data-stu-id="82d4f-108">The number of strokes to update.</span></span>

</dd> <dt>

<span data-ttu-id="82d4f-109">*plStrokeIds* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82d4f-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82d4f-110">Una matriz que contiene los identificadores de trazo.</span><span class="sxs-lookup"><span data-stu-id="82d4f-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="82d4f-111">*ulStrokePacketDescriptionCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82d4f-111">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82d4f-112">El número de propiedades de cada paquete.</span><span class="sxs-lookup"><span data-stu-id="82d4f-112">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="82d4f-113">*pStrokePacketDescriptionGuids* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82d4f-113">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82d4f-114">Una matriz que contiene los identificadores de propiedad de paquete.</span><span class="sxs-lookup"><span data-stu-id="82d4f-114">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="82d4f-115">*pulPacketDataCountPerStroke* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82d4f-115">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82d4f-116">Una matriz que contiene el número de paquetes de cada trazo.</span><span class="sxs-lookup"><span data-stu-id="82d4f-116">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="82d4f-117">*plStrokePacketData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82d4f-117">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82d4f-118">Una matriz que contiene los datos del paquete para los trazos.</span><span class="sxs-lookup"><span data-stu-id="82d4f-118">An array containing the packet data for the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82d4f-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82d4f-119">Return value</span></span>

<span data-ttu-id="82d4f-120">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="82d4f-120">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="82d4f-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82d4f-121">Remarks</span></span>

<span data-ttu-id="82d4f-122">el parámetro *plStrokePacketData* contiene los datos de paquete de todos los trazos.</span><span class="sxs-lookup"><span data-stu-id="82d4f-122">the *plStrokePacketData* parameter contains packet data for all of the strokes.</span></span> <span data-ttu-id="82d4f-123">El parámetro *pStrokePacketDescriptionGuids* contiene los identificadores únicos globales (GUID) que describen los tipos de datos de paquete incluidos para cada punto de cada trazo.</span><span class="sxs-lookup"><span data-stu-id="82d4f-123">The *pStrokePacketDescriptionGuids* parameter contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="82d4f-124">Para obtener una lista completa de las propiedades de paquete disponibles, consulte [constantes de PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="82d4f-124">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="82d4f-125">Solo los trazos con las mismas descripciones de paquetes se pueden actualizar en una única llamada al **método IInkAnalyzer:: UpdateStrokesData**.</span><span class="sxs-lookup"><span data-stu-id="82d4f-125">Only strokes with the same packet descriptions can be updated in a single call to **IInkAnalyzer::UpdateStrokesData Method**.</span></span>

<span data-ttu-id="82d4f-126">Este método no actualiza la región desfasada del analizador de tinta (consulte el [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="82d4f-126">This method does not update the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="82d4f-127">Si un trazo especificado no está asociado al [**IInkAnalyzer**](iinkanalyzer.md), este método omite el identificador.</span><span class="sxs-lookup"><span data-stu-id="82d4f-127">If a specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="82d4f-128">Si ninguno de los trazos especificados identifica un trazo asociado al [**IInkAnalyzer**](iinkanalyzer.md), este método devuelve sin actualizar **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="82d4f-128">If none of the specified strokes identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="82d4f-129">Este método devuelve un código de error cuando *plStrokeIds* es **null**.</span><span class="sxs-lookup"><span data-stu-id="82d4f-129">This method returns an error code when *plStrokeIds* is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="82d4f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82d4f-130">Requirements</span></span>



| <span data-ttu-id="82d4f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="82d4f-131">Requirement</span></span> | <span data-ttu-id="82d4f-132">Value</span><span class="sxs-lookup"><span data-stu-id="82d4f-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82d4f-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82d4f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="82d4f-134">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="82d4f-134">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="82d4f-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82d4f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="82d4f-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="82d4f-136">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="82d4f-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82d4f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="82d4f-138"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="82d4f-138"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="82d4f-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="82d4f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82d4f-140"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82d4f-140"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="82d4f-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="82d4f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d4f-142">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="82d4f-142">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="82d4f-143">**IInkAnalyzer:: AddStroke (método)**</span><span class="sxs-lookup"><span data-stu-id="82d4f-143">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="82d4f-144">**IInkAnalyzer:: AddStrokeForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="82d4f-144">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="82d4f-145">**IInkAnalyzer:: AddStrokeToCustomRecognizer (método)**</span><span class="sxs-lookup"><span data-stu-id="82d4f-145">**IInkAnalyzer::AddStrokeToCustomRecognizer Method**</span></span>](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="82d4f-146">**IInkAnalyzer:: AddStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="82d4f-146">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="82d4f-147">**IInkAnalyzer:: AddStrokesForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="82d4f-147">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="82d4f-148">**IInkAnalyzer:: AddStrokesToCustomRecognizer (método)**</span><span class="sxs-lookup"><span data-stu-id="82d4f-148">**IInkAnalyzer::AddStrokesToCustomRecognizer Method**</span></span>](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="82d4f-149">**IInkAnalyzer:: ClearStrokeData (método)**</span><span class="sxs-lookup"><span data-stu-id="82d4f-149">**IInkAnalyzer::ClearStrokeData Method**</span></span>](iinkanalyzer-clearstrokedata.md)
</dt> <dt>

[<span data-ttu-id="82d4f-150">**\_IAnalysisEvents::UpdateStrokesCache**</span><span class="sxs-lookup"><span data-stu-id="82d4f-150">**\_IAnalysisEvents::UpdateStrokesCache**</span></span>](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[<span data-ttu-id="82d4f-151">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="82d4f-151">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




