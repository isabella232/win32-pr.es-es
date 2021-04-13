---
description: 'Se produce cuando se llama al método IInkAnalyzer:: Analyze o al método IInkAnalyzer:: BackgroundAnalyze.'
ms.assetid: 339b41c6-f388-4b81-b2bc-3705b39d9cc9
title: '_IAnalysisEvents:: Activity (evento) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Activity
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f235d3414b0d514f32b4ebd197c04a8721968a2a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104361962"
---
# <a name="_ianalysiseventsactivity-event"></a><span data-ttu-id="05154-103">\_Evento IAnalysisEvents:: Activity</span><span class="sxs-lookup"><span data-stu-id="05154-103">\_IAnalysisEvents::Activity event</span></span>

<span data-ttu-id="05154-104">Se produce cuando se llama al método [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) o al método [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) .</span><span class="sxs-lookup"><span data-stu-id="05154-104">Occurs when the [**IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md) method or [**IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) method is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="05154-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05154-105">Syntax</span></span>


```C++
HRESULT Activity();
```



## <a name="parameters"></a><span data-ttu-id="05154-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05154-106">Parameters</span></span>

<span data-ttu-id="05154-107">Este evento no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="05154-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="05154-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05154-108">Return value</span></span>

<span data-ttu-id="05154-109">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="05154-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="05154-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="05154-110">Remarks</span></span>

<span data-ttu-id="05154-111">Este evento indica que [**IInkAnalyzer**](iinkanalyzer.md) está realizando el análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="05154-111">This event indicates that the [**IInkAnalyzer**](iinkanalyzer.md) is performing ink analysis.</span></span> <span data-ttu-id="05154-112">Este evento no indica el progreso de la operación de análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="05154-112">This event does not indicate the progress of the ink analysis operation.</span></span>

<span data-ttu-id="05154-113">Para realizar cualquiera de las siguientes acciones, implemente un controlador de eventos **\_ IAnalysisEvents:: Activity** :</span><span class="sxs-lookup"><span data-stu-id="05154-113">To do any of the following, implement an **\_IAnalysisEvents::Activity** event handler:</span></span>

-   <span data-ttu-id="05154-114">Indicar al usuario que el analizador de tinta está realizando el análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="05154-114">Indicate to the user that the ink analyzer is performing ink analysis.</span></span>
-   <span data-ttu-id="05154-115">Procesar los datos proporcionados por el usuario durante el análisis sincrónico.</span><span class="sxs-lookup"><span data-stu-id="05154-115">Process user input during synchronous analysis.</span></span>
-   <span data-ttu-id="05154-116">Reciba una notificación de las solicitudes del sistema, como la repintado de la ventana de la aplicación, durante el análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="05154-116">Receive notification of system requests, such as repainting of the application's window, during ink analysis.</span></span>

<span data-ttu-id="05154-117">El [**IInkAnalyzer**](iinkanalyzer.md) genera este evento con frecuencia durante la fase de análisis de diseño y la fase de clasificación de escritura y dibujo del análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="05154-117">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event frequently during the layout analysis phase and the writing and drawing classification phase of ink analysis.</span></span> <span data-ttu-id="05154-118">El **IInkAnalyzer** genera este evento durante la fase de reconocimiento de escritura a mano antes y después de obtener acceso a un reconocedor de tinta.</span><span class="sxs-lookup"><span data-stu-id="05154-118">The **IInkAnalyzer** raises this event during the handwriting recognition phase before and after accessing an ink recognizer.</span></span>

<span data-ttu-id="05154-119">El número de eventos de actividad que genera un [**IInkAnalyzer**](iinkanalyzer.md) se ve afectado por:</span><span class="sxs-lookup"><span data-stu-id="05154-119">The number of activity events an [**IInkAnalyzer**](iinkanalyzer.md) generates is affected by:</span></span>

-   <span data-ttu-id="05154-120">El reconocedor de tinta que [**IInkAnalyzer**](iinkanalyzer.md) aplica al reconocimiento de tinta.</span><span class="sxs-lookup"><span data-stu-id="05154-120">The ink recognizer that the [**IInkAnalyzer**](iinkanalyzer.md) applies to ink recognition.</span></span>
-   <span data-ttu-id="05154-121">El número y la longitud de los trazos que el [**IInkAnalyzer**](iinkanalyzer.md) está analizando.</span><span class="sxs-lookup"><span data-stu-id="05154-121">The number and length of strokes that the [**IInkAnalyzer**](iinkanalyzer.md) is analyzing.</span></span>
-   <span data-ttu-id="05154-122">Número de trazos que se clasifican como de escritura.</span><span class="sxs-lookup"><span data-stu-id="05154-122">The number of strokes that are classified as writing.</span></span>

<span data-ttu-id="05154-123">Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="05154-123">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05154-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05154-124">Requirements</span></span>



| <span data-ttu-id="05154-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="05154-125">Requirement</span></span> | <span data-ttu-id="05154-126">Value</span><span class="sxs-lookup"><span data-stu-id="05154-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05154-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05154-127">Minimum supported client</span></span><br/> | <span data-ttu-id="05154-128">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="05154-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="05154-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05154-129">Minimum supported server</span></span><br/> | <span data-ttu-id="05154-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="05154-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="05154-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05154-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="05154-132"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="05154-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="05154-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="05154-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05154-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05154-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="05154-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="05154-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05154-136">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="05154-136">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="05154-137">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="05154-137">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="05154-138">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="05154-138">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="05154-139">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="05154-139">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="05154-140">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="05154-140">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="05154-141">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="05154-141">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="05154-142">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="05154-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




