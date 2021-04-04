---
description: Recupera alternativas de análisis para los trazos con los identificadores de trazo especificados.
ms.assetid: e8bc198e-de0b-49b7-9120-4298985dfe64
title: 'IInkAnalyzer:: GetAlternatesForStrokes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 115b2cc1be4ba35614ada6fddd9c9fbcdfa76357
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154416"
---
# <a name="iinkanalyzergetalternatesforstrokes-method"></a><span data-ttu-id="95e67-103">IInkAnalyzer:: GetAlternatesForStrokes (método)</span><span class="sxs-lookup"><span data-stu-id="95e67-103">IInkAnalyzer::GetAlternatesForStrokes method</span></span>

<span data-ttu-id="95e67-104">Recupera alternativas de análisis para los trazos con los identificadores de trazo especificados.</span><span class="sxs-lookup"><span data-stu-id="95e67-104">Retrieves analysis alternates for the strokes with the specified stroke identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="95e67-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95e67-105">Syntax</span></span>


```C++
HRESULT GetAlternatesForStrokes(
  [in]  ULONG              ulStrokeIdsCount,
  [in]  LONG               *plStrokes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a><span data-ttu-id="95e67-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95e67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95e67-107">*ulStrokeIdsCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="95e67-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95e67-108">Número de identificadores de trazo en *plStrokes*.</span><span class="sxs-lookup"><span data-stu-id="95e67-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="95e67-109">*plStrokes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="95e67-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95e67-110">Matriz de identificadores de trazo.</span><span class="sxs-lookup"><span data-stu-id="95e67-110">The array of stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="95e67-111">*ulMaximumAlternates* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="95e67-111">*ulMaximumAlternates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95e67-112">Número máximo de alternativas de análisis devueltas.</span><span class="sxs-lookup"><span data-stu-id="95e67-112">The maximum number of analysis alternatives returned.</span></span>

</dd> <dt>

<span data-ttu-id="95e67-113">*ppAlternates* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="95e67-113">*ppAlternates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95e67-114">El objeto [**IAnalysisAlternates**](ianalysisalternates.md) que contiene las alternativas de análisis.</span><span class="sxs-lookup"><span data-stu-id="95e67-114">The [**IAnalysisAlternates**](ianalysisalternates.md) object containing the analysis alternatives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95e67-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95e67-115">Return value</span></span>

<span data-ttu-id="95e67-116">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="95e67-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="95e67-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95e67-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="95e67-118">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppAlternates* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="95e67-118">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppAlternates* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="95e67-119">La [**IAnalysisAlternate**](ianalysisalternate.md) superior se devuelve como la primera alternativa de la colección.</span><span class="sxs-lookup"><span data-stu-id="95e67-119">The top [**IAnalysisAlternate**](ianalysisalternate.md) is returned as the first alternate of the collection.</span></span>

<span data-ttu-id="95e67-120">Los trazos especificados no tienen que representar áreas adyacentes del documento.</span><span class="sxs-lookup"><span data-stu-id="95e67-120">The specified strokes do not have to represent adjacent areas of the document.</span></span>

## <a name="requirements"></a><span data-ttu-id="95e67-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95e67-121">Requirements</span></span>



| <span data-ttu-id="95e67-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="95e67-122">Requirement</span></span> | <span data-ttu-id="95e67-123">Value</span><span class="sxs-lookup"><span data-stu-id="95e67-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95e67-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95e67-124">Minimum supported client</span></span><br/> | <span data-ttu-id="95e67-125">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="95e67-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="95e67-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95e67-126">Minimum supported server</span></span><br/> | <span data-ttu-id="95e67-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="95e67-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="95e67-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95e67-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="95e67-129"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="95e67-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="95e67-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="95e67-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95e67-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95e67-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="95e67-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="95e67-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95e67-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="95e67-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="95e67-134">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="95e67-134">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="95e67-135">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="95e67-135">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="95e67-136">**IInkAnalyzer:: GetAlternates (método)**</span><span class="sxs-lookup"><span data-stu-id="95e67-136">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="95e67-137">**IInkAnalyzer:: GetAlternatesForContextNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="95e67-137">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="95e67-138">**IInkAnalyzer:: ModifyTopAlternate (método)**</span><span class="sxs-lookup"><span data-stu-id="95e67-138">**IInkAnalyzer::ModifyTopAlternate Method**</span></span>](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[<span data-ttu-id="95e67-139">**IInkAnalyzer:: ModifyTopAlternateWithConfirmation (método)**</span><span class="sxs-lookup"><span data-stu-id="95e67-139">**IInkAnalyzer::ModifyTopAlternateWithConfirmation Method**</span></span>](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[<span data-ttu-id="95e67-140">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="95e67-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

