---
description: Obtiene un valor que indica el nivel de confianza que IInkAnalyzer tiene en la precisión de IAnalysisAlternate.
ms.assetid: ac1c68df-2e0c-4633-b7ee-519482a4d67a
title: 'IAnalysisAlternate:: GetRecognitionConfidence (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognitionConfidence
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eacaf7e5a8feaddcd437e68cf7acfa4fc5a7fc80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810063"
---
# <a name="ianalysisalternategetrecognitionconfidence-method"></a><span data-ttu-id="a14a1-103">IAnalysisAlternate:: GetRecognitionConfidence (método)</span><span class="sxs-lookup"><span data-stu-id="a14a1-103">IAnalysisAlternate::GetRecognitionConfidence method</span></span>

<span data-ttu-id="a14a1-104">Obtiene un valor que indica el nivel de confianza que [**IInkAnalyzer**](iinkanalyzer.md) tiene en la precisión de [**IAnalysisAlternate**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="a14a1-104">Gets a value that indicates the level of confidence that the [**IInkAnalyzer**](iinkanalyzer.md) has in the accuracy of the [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a14a1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a14a1-105">Syntax</span></span>


```C++
HRESULT GetRecognitionConfidence(
  [out] RecognitionConfidence *pConfidence
);
```



## <a name="parameters"></a><span data-ttu-id="a14a1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a14a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a14a1-107">*pConfidence* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a14a1-107">*pConfidence* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a14a1-108">Un puntero a una [**enumeración InkRecognitionConfidence**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence) que indica el nivel de confianza que el [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) tiene en la precisión de la alternativa de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="a14a1-108">A pointer to an [**InkRecognitionConfidence Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence) that indicates the level of confidence that the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) has in the accuracy of the recognition alternate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a14a1-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a14a1-109">Return value</span></span>

<span data-ttu-id="a14a1-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a14a1-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a14a1-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a14a1-111">Requirements</span></span>



| <span data-ttu-id="a14a1-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="a14a1-112">Requirement</span></span> | <span data-ttu-id="a14a1-113">Value</span><span class="sxs-lookup"><span data-stu-id="a14a1-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a14a1-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a14a1-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a14a1-115">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a14a1-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a14a1-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a14a1-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a14a1-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a14a1-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a14a1-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a14a1-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a14a1-119"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a14a1-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a14a1-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a14a1-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a14a1-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a14a1-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a14a1-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a14a1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a14a1-123">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="a14a1-123">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="a14a1-124">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a14a1-124">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a14a1-125">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="a14a1-125">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="a14a1-126">**RecognitionConfidence**</span><span class="sxs-lookup"><span data-stu-id="a14a1-126">**RecognitionConfidence**</span></span>](recognitionconfidence.md)
</dt> <dt>

[<span data-ttu-id="a14a1-127">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="a14a1-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




