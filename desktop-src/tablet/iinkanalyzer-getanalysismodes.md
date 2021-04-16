---
description: Recupera marcas que controlan cómo el IInkAnalyzer realiza el análisis de tinta.
ms.assetid: 982cb9cd-2d73-4064-9a6e-fe123adf0fb6
title: 'IInkAnalyzer:: GetAnalysisModes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisModes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d03ec255b10dd607889768795b00f5b2aff4dc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705697"
---
# <a name="iinkanalyzergetanalysismodes-method"></a><span data-ttu-id="2bbbd-103">IInkAnalyzer:: GetAnalysisModes (método)</span><span class="sxs-lookup"><span data-stu-id="2bbbd-103">IInkAnalyzer::GetAnalysisModes method</span></span>

<span data-ttu-id="2bbbd-104">Recupera marcas que controlan cómo el [**IInkAnalyzer**](iinkanalyzer.md) realiza el análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="2bbbd-104">Retrieves flags that control how the [**IInkAnalyzer**](iinkanalyzer.md) performs ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bbbd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2bbbd-105">Syntax</span></span>


```C++
HRESULT GetAnalysisModes(
  [out] AnalysisModes *pAnalysisMode
);
```



## <a name="parameters"></a><span data-ttu-id="2bbbd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2bbbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bbbd-107">*pAnalysisMode* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2bbbd-107">*pAnalysisMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2bbbd-108">Combinación bit a bit de los valores de la enumeración [**AnalysisModes**](analysismodes.md) .</span><span class="sxs-lookup"><span data-stu-id="2bbbd-108">A bitwise combination of the [**AnalysisModes**](analysismodes.md) enumeration values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bbbd-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2bbbd-109">Return value</span></span>

<span data-ttu-id="2bbbd-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="2bbbd-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2bbbd-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bbbd-111">Requirements</span></span>



| <span data-ttu-id="2bbbd-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bbbd-112">Requirement</span></span> | <span data-ttu-id="2bbbd-113">Value</span><span class="sxs-lookup"><span data-stu-id="2bbbd-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bbbd-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bbbd-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2bbbd-115">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2bbbd-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2bbbd-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bbbd-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2bbbd-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2bbbd-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2bbbd-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2bbbd-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bbbd-119"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2bbbd-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2bbbd-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2bbbd-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bbbd-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bbbd-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="2bbbd-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="2bbbd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bbbd-123">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="2bbbd-123">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="2bbbd-124">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="2bbbd-124">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="2bbbd-125">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="2bbbd-125">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="2bbbd-126">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="2bbbd-126">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="2bbbd-127">**IInkAnalyzer:: SetAnalysisModes (método)**</span><span class="sxs-lookup"><span data-stu-id="2bbbd-127">**IInkAnalyzer::SetAnalysisModes Method**</span></span>](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="2bbbd-128">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="2bbbd-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




