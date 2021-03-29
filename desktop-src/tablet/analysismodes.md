---
description: Especifica cómo el IInkAnalyzer realiza el análisis de tinta.
ms.assetid: bc526445-0c9c-4c53-8b02-32cf758266e6
title: Enumeración AnalysisModes (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisModes
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b9fdebd3ef3cd505b49ff6c82f7609bc339af0a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423507"
---
# <a name="analysismodes-enumeration"></a><span data-ttu-id="be0f5-103">Enumeración AnalysisModes</span><span class="sxs-lookup"><span data-stu-id="be0f5-103">AnalysisModes enumeration</span></span>

<span data-ttu-id="be0f5-104">Especifica cómo el [**IInkAnalyzer**](iinkanalyzer.md) realiza el análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="be0f5-104">Specifies how the [**IInkAnalyzer**](iinkanalyzer.md) performs ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="be0f5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be0f5-105">Syntax</span></span>


```C++
typedef enum AnalysisModes { 
  AnalysisModes_None                     = 0x0000,
  AnalysisModes_AutomaticReconciliation  = 0x0002,
  AnalysisModes_StrokeCacheAutoCleanup   = 0x0004,
  AnalysisModes_PersonalizationEnabled   = 0x0008,
  AnalysisModes_Default                  = 0x000d
} AnalysisModes;
```



## <a name="constants"></a><span data-ttu-id="be0f5-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="be0f5-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="be0f5-107"><span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**AnalysisModes \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="be0f5-107"><span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**AnalysisModes\_None**</span></span>
</dt> <dd>

<span data-ttu-id="be0f5-108">No se especifica ningún modo.</span><span class="sxs-lookup"><span data-stu-id="be0f5-108">No modes are specified.</span></span>

</dd> <dt>

<span data-ttu-id="be0f5-109"><span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**AnalysisModes \_ AutomaticReconciliation**</span><span class="sxs-lookup"><span data-stu-id="be0f5-109"><span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**AnalysisModes\_AutomaticReconciliation**</span></span>
</dt> <dd>

<span data-ttu-id="be0f5-110">Indica si el [**IInkAnalyzer**](iinkanalyzer.md) inicia automáticamente la operación de conciliación en cuanto los resultados intermedios o finales estén listos.</span><span class="sxs-lookup"><span data-stu-id="be0f5-110">Whether the [**IInkAnalyzer**](iinkanalyzer.md) automatically starts the reconciliation operation as soon as the intermediate or final results are ready.</span></span>

<span data-ttu-id="be0f5-111">Si este modo está habilitado, no se genera el evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .</span><span class="sxs-lookup"><span data-stu-id="be0f5-111">If this mode is enabled, the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event is not raised.</span></span> <span data-ttu-id="be0f5-112">Si este modo está deshabilitado, se genera el evento **\_ IAnalysisEvents:: ReadyToReconcile** .</span><span class="sxs-lookup"><span data-stu-id="be0f5-112">If this mode is disabled, the **\_IAnalysisEvents::ReadyToReconcile** event is raised.</span></span>

</dd> <dt>

<span data-ttu-id="be0f5-113"><span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**AnalysisModes \_ StrokeCacheAutoCleanup**</span><span class="sxs-lookup"><span data-stu-id="be0f5-113"><span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**AnalysisModes\_StrokeCacheAutoCleanup**</span></span>
</dt> <dd>

<span data-ttu-id="be0f5-114">Si [**IInkAnalyzer**](iinkanalyzer.md) borra automáticamente los trazos innecesarios de la memoria caché del trazo antes de realizar el análisis.</span><span class="sxs-lookup"><span data-stu-id="be0f5-114">Whether the [**IInkAnalyzer**](iinkanalyzer.md) automatically clears unneeded strokes from the stroke cache before performing analysis.</span></span>

<span data-ttu-id="be0f5-115">Si este modo está habilitado, el [**IInkAnalyzer**](iinkanalyzer.md) borra los datos del trazo antes de realizar el análisis.</span><span class="sxs-lookup"><span data-stu-id="be0f5-115">If this mode is enabled, the [**IInkAnalyzer**](iinkanalyzer.md) clears the stroke data before performing analysis.</span></span> <span data-ttu-id="be0f5-116">El código también debe controlar el evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) .</span><span class="sxs-lookup"><span data-stu-id="be0f5-116">Your code must also then handle the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event.</span></span> <span data-ttu-id="be0f5-117">Si no se controla el evento **\_ IAnalysisEvents:: UpdateStrokesCache** , se produce una excepción.</span><span class="sxs-lookup"><span data-stu-id="be0f5-117">If the **\_IAnalysisEvents::UpdateStrokesCache** event is not handled, an exception is raised.</span></span> <span data-ttu-id="be0f5-118">Esta comprobación se realiza en las fases de análisis (o BackgroundAnalyze) y de conciliación.</span><span class="sxs-lookup"><span data-stu-id="be0f5-118">This check is done both at the Analyze (or BackgroundAnalyze) and Reconciliation phases.</span></span>

<span data-ttu-id="be0f5-119">Si este modo está deshabilitado, el [**IInkAnalyzer**](iinkanalyzer.md) no borra los datos del trazo.</span><span class="sxs-lookup"><span data-stu-id="be0f5-119">If this mode is disabled, the [**IInkAnalyzer**](iinkanalyzer.md) does not clear the stroke data.</span></span> <span data-ttu-id="be0f5-120">Para borrar los datos del trazo, llame al [**método IInkAnalyzer:: ClearStrokeData**](iinkanalyzer-clearstrokedata.md).</span><span class="sxs-lookup"><span data-stu-id="be0f5-120">To clear the stroke data, call [**IInkAnalyzer::ClearStrokeData Method**](iinkanalyzer-clearstrokedata.md).</span></span> <span data-ttu-id="be0f5-121">Si este modo está deshabilitado, se desencadena el evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) para que **IInkAnalyzer** pueda recuperar los datos de trazo más recientes de cualquier trazo que haya desactivado la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="be0f5-121">If this mode is disabled, the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event is raised so the **IInkAnalyzer** can retrieve the latest stroke data for any strokes that have had their cache cleared.</span></span> <span data-ttu-id="be0f5-122">Si se borra la memoria caché del trazo, pero el evento **\_ IAnalysisEvents:: UpdateStrokesCache** no está controlado, se produce una excepción.</span><span class="sxs-lookup"><span data-stu-id="be0f5-122">If the stroke cache is cleared, but the **\_IAnalysisEvents::UpdateStrokesCache** event is not handled, an exception is raised.</span></span>

</dd> <dt>

<span data-ttu-id="be0f5-123"><span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**AnalysisModes \_ PersonalizationEnabled**</span><span class="sxs-lookup"><span data-stu-id="be0f5-123"><span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**AnalysisModes\_PersonalizationEnabled**</span></span>
</dt> <dd>

<span data-ttu-id="be0f5-124">Está habilitada la personalización del reconocimiento de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="be0f5-124">Personalization of handwriting recognition is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="be0f5-125"><span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**\_Valor predeterminado de AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="be0f5-125"><span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**AnalysisModes\_Default**</span></span>
</dt> <dd>

<span data-ttu-id="be0f5-126">Todos los modos están habilitados.</span><span class="sxs-lookup"><span data-stu-id="be0f5-126">All modes are enabled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be0f5-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be0f5-127">Remarks</span></span>

<span data-ttu-id="be0f5-128">Esta enumeración permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="be0f5-128">This enumeration allows a bitwise combination of its member values.</span></span>

## <a name="requirements"></a><span data-ttu-id="be0f5-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be0f5-129">Requirements</span></span>



| <span data-ttu-id="be0f5-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="be0f5-130">Requirement</span></span> | <span data-ttu-id="be0f5-131">Value</span><span class="sxs-lookup"><span data-stu-id="be0f5-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be0f5-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be0f5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="be0f5-133">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="be0f5-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="be0f5-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be0f5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="be0f5-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="be0f5-135">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="be0f5-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be0f5-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="be0f5-137"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="be0f5-137"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be0f5-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="be0f5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be0f5-139">**IInkAnalyzer:: GetAnalysisModes (método)**</span><span class="sxs-lookup"><span data-stu-id="be0f5-139">**IInkAnalyzer::GetAnalysisModes Method**</span></span>](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="be0f5-140">**IInkAnalyzer:: SetAnalysisModes (método)**</span><span class="sxs-lookup"><span data-stu-id="be0f5-140">**IInkAnalyzer::SetAnalysisModes Method**</span></span>](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="be0f5-141">**\_IAnalysisEvents::IntermediateResults**</span><span class="sxs-lookup"><span data-stu-id="be0f5-141">**\_IAnalysisEvents::IntermediateResults**</span></span>](-ianalysisevents-intermediateresults.md)
</dt> <dt>

[<span data-ttu-id="be0f5-142">**\_IAnalysisEvents::ReadyToReconcile**</span><span class="sxs-lookup"><span data-stu-id="be0f5-142">**\_IAnalysisEvents::ReadyToReconcile**</span></span>](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[<span data-ttu-id="be0f5-143">**\_IAnalysisEvents::UpdateStrokesCache**</span><span class="sxs-lookup"><span data-stu-id="be0f5-143">**\_IAnalysisEvents::UpdateStrokesCache**</span></span>](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[<span data-ttu-id="be0f5-144">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="be0f5-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




