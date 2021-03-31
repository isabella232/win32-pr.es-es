---
description: Recupera una colección ordenada de objetos IInkAnalysisRecognizer.
ms.assetid: 67399237-38e2-4905-a97c-10ca72c7799b
title: 'IInkAnalyzer:: GetInkAnalysisRecognizersByPriority (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetInkAnalysisRecognizersByPriority
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d596a8138f8ab16852ce99116eef66372ff2b074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908009"
---
# <a name="iinkanalyzergetinkanalysisrecognizersbypriority-method"></a><span data-ttu-id="4a641-103">IInkAnalyzer:: GetInkAnalysisRecognizersByPriority (método)</span><span class="sxs-lookup"><span data-stu-id="4a641-103">IInkAnalyzer::GetInkAnalysisRecognizersByPriority method</span></span>

<span data-ttu-id="4a641-104">Recupera una colección ordenada de objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .</span><span class="sxs-lookup"><span data-stu-id="4a641-104">Retrieves an ordered collection of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a641-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a641-105">Syntax</span></span>


```C++
HRESULT GetInkAnalysisRecognizersByPriority(
  [out] IInkAnalysisRecognizers **ppInkAnalysisRecognizers
);
```



## <a name="parameters"></a><span data-ttu-id="4a641-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a641-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a641-107">*ppInkAnalysisRecognizers* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4a641-107">*ppInkAnalysisRecognizers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a641-108">Colección ordenada de objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .</span><span class="sxs-lookup"><span data-stu-id="4a641-108">An ordered collection of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a641-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a641-109">Return value</span></span>

<span data-ttu-id="4a641-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4a641-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4a641-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a641-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="4a641-112">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppInkAnalysisRecognizers* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="4a641-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppInkAnalysisRecognizers* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="4a641-113">El orden de los reconocedores de esta colección indica el orden en que el [**IInkAnalyzer**](iinkanalyzer.md) evalúa los reconocedores disponibles.</span><span class="sxs-lookup"><span data-stu-id="4a641-113">The order of the recognizers in this collection indicates the order in which the [**IInkAnalyzer**](iinkanalyzer.md) evaluates the available recognizers.</span></span> <span data-ttu-id="4a641-114">**IInkAnalyzer** usa el lenguaje de los trazos como criterio principal para aplicar un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="4a641-114">The **IInkAnalyzer** uses the language of the strokes as its primary criterion for applying an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span> <span data-ttu-id="4a641-115">Como criterio secundario, **IInkAnalyzer** compara la información de sugerencia de análisis con las capacidades admitidas de un objeto **IInkAnalysisRecognizer** (consulte [**IInkAnalysisRecognizer:: GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)).</span><span class="sxs-lookup"><span data-stu-id="4a641-115">As a secondary criterion, the **IInkAnalyzer** compares analysis hint information against an **IInkAnalysisRecognizer** object's supported capabilities (see [**IInkAnalysisRecognizer::GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)).</span></span> <span data-ttu-id="4a641-116">Para obtener más información sobre las sugerencias de análisis, vea [**IInkAnalyzer:: CreateAnalysisHint Method**](iinkanalyzer-createanalysishint.md).</span><span class="sxs-lookup"><span data-stu-id="4a641-116">For more information about analysis hints, see [**IInkAnalyzer::CreateAnalysisHint Method**](iinkanalyzer-createanalysishint.md).</span></span>

<span data-ttu-id="4a641-117">Si más de un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) admite un identificador de idioma, el [**IInkAnalyzer**](iinkanalyzer.md) usa un algoritmo de "primer ajuste" para seleccionar el primer **IInkAnalysisRecognizer** para analizar los trazos de ese idioma.</span><span class="sxs-lookup"><span data-stu-id="4a641-117">If more than one [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supports a language identifier, the [**IInkAnalyzer**](iinkanalyzer.md) uses a "first-fit" algorithm to select the first **IInkAnalysisRecognizer** to analyze strokes of that language.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a641-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a641-118">Requirements</span></span>



| <span data-ttu-id="4a641-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a641-119">Requirement</span></span> | <span data-ttu-id="4a641-120">Value</span><span class="sxs-lookup"><span data-stu-id="4a641-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a641-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a641-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4a641-122">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4a641-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4a641-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a641-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4a641-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4a641-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4a641-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a641-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a641-126"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4a641-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4a641-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4a641-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a641-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a641-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4a641-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a641-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a641-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="4a641-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="4a641-131">**IInkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="4a641-131">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="4a641-132">**IInkAnalyzer:: SetHighestPriorityInkAnalysisRecognizer (método)**</span><span class="sxs-lookup"><span data-stu-id="4a641-132">**IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer Method**</span></span>](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="4a641-133">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="4a641-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

