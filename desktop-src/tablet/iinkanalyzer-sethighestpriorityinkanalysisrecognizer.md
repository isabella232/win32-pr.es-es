---
description: Mueve el IInkAnalysisRecognizer especificado a la primera posición de la lista de reconocedores de tinta del objeto IInkAnalyzer.
ms.assetid: 9126187f-02dd-4988-91b8-c4f3d3b6f773
title: 'IInkAnalyzer:: SetHighestPriorityInkAnalysisRecognizer (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetHighestPriorityInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 534b94e4f2964aa81f04e0adac6f45f346c530c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908007"
---
# <a name="iinkanalyzersethighestpriorityinkanalysisrecognizer-method"></a><span data-ttu-id="4d833-103">IInkAnalyzer:: SetHighestPriorityInkAnalysisRecognizer (método)</span><span class="sxs-lookup"><span data-stu-id="4d833-103">IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer method</span></span>

<span data-ttu-id="4d833-104">Mueve el [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) especificado a la primera posición de la lista de reconocedores de tinta del objeto [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="4d833-104">Moves the specified [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) to the first position in the [**IInkAnalyzer**](iinkanalyzer.md) object's list of ink recognizers.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d833-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d833-105">Syntax</span></span>


```C++
HRESULT SetHighestPriorityInkAnalysisRecognizer(
  [in] IInkAnalysisRecognizer *pInkAnalysisRecognizer
);
```



## <a name="parameters"></a><span data-ttu-id="4d833-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d833-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d833-107">*pInkAnalysisRecognizer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4d833-107">*pInkAnalysisRecognizer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d833-108">[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) que se va a colocar en la primera posición.</span><span class="sxs-lookup"><span data-stu-id="4d833-108">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) to place in the first position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d833-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d833-109">Return value</span></span>

<span data-ttu-id="4d833-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4d833-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4d833-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d833-111">Remarks</span></span>

<span data-ttu-id="4d833-112">Para obtener la lista de reconocedores de tinta en orden de prioridad, llame al [**método IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md).</span><span class="sxs-lookup"><span data-stu-id="4d833-112">To get the list of ink recognizers in priority order, call [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md).</span></span>

<span data-ttu-id="4d833-113">Este método no afecta al orden del resto de los objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) de la lista de reconocedores de tinta del objeto [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="4d833-113">This method does not affect the order of the rest of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in the [**IInkAnalyzer**](iinkanalyzer.md) object's list of ink recognizers.</span></span>

<span data-ttu-id="4d833-114">El orden de los reconocedores de tinta devueltos por el [**método IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) indica el orden en el que [**IInkAnalyzer**](iinkanalyzer.md) evalúa los objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) disponibles.</span><span class="sxs-lookup"><span data-stu-id="4d833-114">The order of the ink recognizers returned by [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) indicates the order in which the [**IInkAnalyzer**](iinkanalyzer.md) evaluates the available [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects.</span></span>

<span data-ttu-id="4d833-115">El uso de los reconocedores de tinta se evalúa en función de su orden en la lista.</span><span class="sxs-lookup"><span data-stu-id="4d833-115">Use of the ink recognizers is evaluated based on their order in the list.</span></span>

<span data-ttu-id="4d833-116">Durante el análisis de tinta, el [**IInkAnalyzer**](iinkanalyzer.md) recorre en iteración los reconocedores de tinta de su lista hasta que encuentra un reconocedor que admita el idioma y otras propiedades de los trazos.</span><span class="sxs-lookup"><span data-stu-id="4d833-116">During ink analysis, the [**IInkAnalyzer**](iinkanalyzer.md) iterates through the ink recognizers in its list until it finds a recognizer that supports the language and other properties of the strokes.</span></span> <span data-ttu-id="4d833-117">Este reconocedor se usa para el reconocimiento de tinta para esos trazos.</span><span class="sxs-lookup"><span data-stu-id="4d833-117">This recognizer is used for ink recognition for those strokes.</span></span>

<span data-ttu-id="4d833-118">Si [**IInkAnalyzer**](iinkanalyzer.md) no encuentra un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) que admita un conjunto de trazos durante el análisis, el **IInkAnalyzer** genera un [**IAnalysisWarning**](ianalysiswarning.md) con un código de advertencia de **AnalysisWarningCode \_ InkAnalysisRecognizerNotInstalled** (vea [**IAnalysisWarning:: GetWarningCode**](ianalysiswarning-getwarningcode.md)).</span><span class="sxs-lookup"><span data-stu-id="4d833-118">If the [**IInkAnalyzer**](iinkanalyzer.md) does not find an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) that supports a set of strokes during analysis, the **IInkAnalyzer** generates an [**IAnalysisWarning**](ianalysiswarning.md) with a warning code of **AnalysisWarningCode\_InkAnalysisRecognizerNotInstalled** (see [**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d833-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d833-119">Requirements</span></span>



| <span data-ttu-id="4d833-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d833-120">Requirement</span></span> | <span data-ttu-id="4d833-121">Value</span><span class="sxs-lookup"><span data-stu-id="4d833-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d833-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d833-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4d833-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4d833-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4d833-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d833-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4d833-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4d833-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4d833-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d833-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d833-127"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4d833-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4d833-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4d833-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d833-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d833-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4d833-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d833-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d833-131">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="4d833-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="4d833-132">**IInkAnalyzer:: GetInkAnalysisRecognizersByPriority (método)**</span><span class="sxs-lookup"><span data-stu-id="4d833-132">**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**</span></span>](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[<span data-ttu-id="4d833-133">**IInkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="4d833-133">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="4d833-134">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="4d833-134">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="4d833-135">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="4d833-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




