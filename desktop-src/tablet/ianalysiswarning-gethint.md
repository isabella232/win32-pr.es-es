---
description: Recupera la sugerencia de análisis que produjo esta advertencia.
ms.assetid: 715aa4b2-6c45-414b-96f2-44c73a073213
title: 'IAnalysisWarning:: GetHint (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2c38a22b799eb6836a85a42748f60207ee7e997e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715236"
---
# <a name="ianalysiswarninggethint-method"></a><span data-ttu-id="9bddc-103">IAnalysisWarning:: GetHint (método)</span><span class="sxs-lookup"><span data-stu-id="9bddc-103">IAnalysisWarning::GetHint method</span></span>

<span data-ttu-id="9bddc-104">Recupera la sugerencia de análisis que produjo esta advertencia.</span><span class="sxs-lookup"><span data-stu-id="9bddc-104">Retrieves the analysis hint that caused this warning.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bddc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9bddc-105">Syntax</span></span>


```C++
HRESULT GetHint(
  [out] IContextNode **pAnalysisHint
);
```



## <a name="parameters"></a><span data-ttu-id="9bddc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9bddc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bddc-107">*pAnalysisHint* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9bddc-107">*pAnalysisHint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bddc-108">El nodo de contexto de la sugerencia de análisis que causó esta advertencia, o **null** si una sugerencia de análisis no produjo esta advertencia.</span><span class="sxs-lookup"><span data-stu-id="9bddc-108">The analysis hint context node that caused this warning, or **NULL** if an analysis hint did not cause this warning.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bddc-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9bddc-109">Return value</span></span>

<span data-ttu-id="9bddc-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9bddc-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9bddc-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9bddc-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="9bddc-112">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *pAnalysisHint* cuando ya no necesite usar el nodo de contexto de la sugerencia de análisis.</span><span class="sxs-lookup"><span data-stu-id="9bddc-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pAnalysisHint* when you no longer need to use the analysis hint context node.</span></span>

 

<span data-ttu-id="9bddc-113">Un ejemplo de una sugerencia de análisis que genera un [**IAnalysisWarning**](ianalysiswarning.md) es una sugerencia de análisis que contiene un Factoid escrito incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="9bddc-113">An example of an analysis hint that generates an [**IAnalysisWarning**](ianalysiswarning.md) is an analysis hint that contains an incorrectly spelled factoid.</span></span> <span data-ttu-id="9bddc-114">En este caso, el análisis de tinta devuelve un [**IAnalysisStatus**](ianalysisstatus.md) que contiene un **IAnalysisWarning** que hace referencia al nodo de contexto de la sugerencia de análisis con la Factoid mal escrita.</span><span class="sxs-lookup"><span data-stu-id="9bddc-114">In this case, ink analysis returns an [**IAnalysisStatus**](ianalysisstatus.md) that contains an **IAnalysisWarning** that references the analysis hint context node with the misspelled factoid.</span></span> <span data-ttu-id="9bddc-115">Además, en este caso, el método [**IAnalysisWarning:: GetWarningCode**](ianalysiswarning-getwarningcode.md) de la advertencia de análisis devuelve un valor [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) de **AnalysisWarningCode \_ FactoidNotSupported**.</span><span class="sxs-lookup"><span data-stu-id="9bddc-115">Also, in this case, the analysis warning's [**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md) method returns an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) value of **AnalysisWarningCode\_FactoidNotSupported**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bddc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bddc-116">Requirements</span></span>



| <span data-ttu-id="9bddc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bddc-117">Requirement</span></span> | <span data-ttu-id="9bddc-118">Value</span><span class="sxs-lookup"><span data-stu-id="9bddc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bddc-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9bddc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9bddc-120">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9bddc-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9bddc-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9bddc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9bddc-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9bddc-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9bddc-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9bddc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bddc-124"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9bddc-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9bddc-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9bddc-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bddc-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bddc-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9bddc-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9bddc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bddc-128">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="9bddc-128">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="9bddc-129">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="9bddc-129">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="9bddc-130">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="9bddc-130">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="9bddc-131">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="9bddc-131">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="9bddc-132">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="9bddc-132">**AnalysisWarningCode**</span></span>](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[<span data-ttu-id="9bddc-133">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="9bddc-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

