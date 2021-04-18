---
description: Indica el nivel de confianza que IInkAnalyzer tiene en la precisión del resultado del reconocimiento.
ms.assetid: fd4fc350-b4db-4f9a-a5ae-00065e33606c
title: Enumeración RecognitionConfidence (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognitionConfidence
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: e0358aacf789c391d99c10fc0fea64670dc4710e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707297"
---
# <a name="recognitionconfidence-enumeration"></a><span data-ttu-id="3e87e-103">Enumeración RecognitionConfidence</span><span class="sxs-lookup"><span data-stu-id="3e87e-103">RecognitionConfidence enumeration</span></span>

<span data-ttu-id="3e87e-104">Indica el nivel de confianza que [**IInkAnalyzer**](iinkanalyzer.md) tiene en la precisión del resultado del reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="3e87e-104">Indicates the level of confidence that the [**IInkAnalyzer**](iinkanalyzer.md) has in the accuracy of the recognition result.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e87e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e87e-105">Syntax</span></span>


```C++
typedef enum RecognitionConfidence { 
  RecognitionConfidence_Strong        = 0,
  RecognitionConfidence_Intermediate  = 1,
  RecognitionConfidence_Poor          = 2,
  RecognitionConfidence_Unknown       = 3
} RecognitionConfidence;
```



## <a name="constants"></a><span data-ttu-id="3e87e-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="3e87e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3e87e-107"><span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**RecognitionConfidence \_ Strong**</span><span class="sxs-lookup"><span data-stu-id="3e87e-107"><span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**RecognitionConfidence\_Strong**</span></span>
</dt> <dd>

<span data-ttu-id="3e87e-108">Confianza fuerte en el resultado o alternativo.</span><span class="sxs-lookup"><span data-stu-id="3e87e-108">Strong confidence in the result or alternate.</span></span>

</dd> <dt>

<span data-ttu-id="3e87e-109"><span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**RecognitionConfidence \_ intermedio**</span><span class="sxs-lookup"><span data-stu-id="3e87e-109"><span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**RecognitionConfidence\_Intermediate**</span></span>
</dt> <dd>

<span data-ttu-id="3e87e-110">Confianza intermedia en el resultado o alternativo.</span><span class="sxs-lookup"><span data-stu-id="3e87e-110">Intermediate confidence in the result or alternate.</span></span>

</dd> <dt>

<span data-ttu-id="3e87e-111"><span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**RecognitionConfidence \_ pobre**</span><span class="sxs-lookup"><span data-stu-id="3e87e-111"><span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**RecognitionConfidence\_Poor**</span></span>
</dt> <dd>

<span data-ttu-id="3e87e-112">Mala confianza en el resultado o alternativo.</span><span class="sxs-lookup"><span data-stu-id="3e87e-112">Poor confidence in the result or alternate.</span></span>

</dd> <dt>

<span data-ttu-id="3e87e-113"><span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**RecognitionConfidence \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="3e87e-113"><span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**RecognitionConfidence\_Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="3e87e-114">El [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) que generó el texto reconocido no es compatible con los niveles de confianza.</span><span class="sxs-lookup"><span data-stu-id="3e87e-114">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) that generated the recognized text does not support confidence levels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e87e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e87e-115">Remarks</span></span>

<span data-ttu-id="3e87e-116">[**IInkAnalyzer**](iinkanalyzer.md) usa uno o varios objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) para convertir la escritura a mano en texto.</span><span class="sxs-lookup"><span data-stu-id="3e87e-116">The [**IInkAnalyzer**](iinkanalyzer.md) uses one or more [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects to convert handwriting to text.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e87e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e87e-117">Requirements</span></span>



| <span data-ttu-id="3e87e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e87e-118">Requirement</span></span> | <span data-ttu-id="3e87e-119">Value</span><span class="sxs-lookup"><span data-stu-id="3e87e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e87e-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e87e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3e87e-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3e87e-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3e87e-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e87e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3e87e-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3e87e-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3e87e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e87e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e87e-125"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3e87e-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e87e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e87e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e87e-127">**IAnalysisAlternate:: GetRecognitionConfidence (método)**</span><span class="sxs-lookup"><span data-stu-id="3e87e-127">**IAnalysisAlternate::GetRecognitionConfidence Method**</span></span>](ianalysisalternate-getrecognitionconfidence.md)
</dt> <dt>

[<span data-ttu-id="3e87e-128">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="3e87e-128">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="3e87e-129">Propiedades del nodo de contexto</span><span class="sxs-lookup"><span data-stu-id="3e87e-129">Context Node Properties</span></span>](context-node-properties.md)
</dt> <dt>

[<span data-ttu-id="3e87e-130">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="3e87e-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




