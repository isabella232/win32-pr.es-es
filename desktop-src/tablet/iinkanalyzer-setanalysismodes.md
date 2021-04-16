---
description: Modifica las marcas que controlan cómo el IInkAnalyzer realiza el análisis de tinta.
ms.assetid: cb82edd0-1f15-4313-a286-1fcd715ac6df
title: 'IInkAnalyzer:: SetAnalysisModes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetAnalysisModes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 826d31fd5b61db2332ef953d55b2cf6c6331995b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541995"
---
# <a name="iinkanalyzersetanalysismodes-method"></a><span data-ttu-id="d0b2a-103">IInkAnalyzer:: SetAnalysisModes (método)</span><span class="sxs-lookup"><span data-stu-id="d0b2a-103">IInkAnalyzer::SetAnalysisModes method</span></span>

<span data-ttu-id="d0b2a-104">Modifica las marcas que controlan cómo el [**IInkAnalyzer**](iinkanalyzer.md) realiza el análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="d0b2a-104">Modifies flags that control how the [**IInkAnalyzer**](iinkanalyzer.md) performs ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0b2a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0b2a-105">Syntax</span></span>


```C++
HRESULT SetAnalysisModes(
  [in] AnalysisModes analysisMode
);
```



## <a name="parameters"></a><span data-ttu-id="d0b2a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0b2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0b2a-107">*analysisMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0b2a-107">*analysisMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0b2a-108">Combinación bit a bit de los valores de la enumeración [**AnalysisModes**](analysismodes.md) .</span><span class="sxs-lookup"><span data-stu-id="d0b2a-108">A bitwise combination of the [**AnalysisModes**](analysismodes.md) enumeration values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0b2a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0b2a-109">Return value</span></span>

<span data-ttu-id="d0b2a-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d0b2a-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0b2a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0b2a-111">Requirements</span></span>



| <span data-ttu-id="d0b2a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0b2a-112">Requirement</span></span> | <span data-ttu-id="d0b2a-113">Value</span><span class="sxs-lookup"><span data-stu-id="d0b2a-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0b2a-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0b2a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d0b2a-115">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d0b2a-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d0b2a-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0b2a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d0b2a-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d0b2a-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d0b2a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0b2a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0b2a-119"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d0b2a-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d0b2a-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d0b2a-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0b2a-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0b2a-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d0b2a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0b2a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0b2a-123">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="d0b2a-123">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="d0b2a-124">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="d0b2a-124">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="d0b2a-125">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="d0b2a-125">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="d0b2a-126">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="d0b2a-126">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="d0b2a-127">**IInkAnalyzer:: GetAnalysisModes (método)**</span><span class="sxs-lookup"><span data-stu-id="d0b2a-127">**IInkAnalyzer::GetAnalysisModes Method**</span></span>](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="d0b2a-128">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="d0b2a-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




