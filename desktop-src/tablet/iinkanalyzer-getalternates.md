---
description: Recupera 10 alternativas de análisis para todas las entradas de lápiz asociadas a IInkAnalyzer.
ms.assetid: 42b702cf-54a3-413b-9f3a-dcdae7c2e89b
title: 'IInkAnalyzer:: GetAlternates (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 37219226e651e286a6d1d63accbd7e548b3b7807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686832"
---
# <a name="iinkanalyzergetalternates-method"></a><span data-ttu-id="24497-103">IInkAnalyzer:: GetAlternates (método)</span><span class="sxs-lookup"><span data-stu-id="24497-103">IInkAnalyzer::GetAlternates method</span></span>

<span data-ttu-id="24497-104">Recupera 10 alternativas de análisis para todas las entradas de lápiz asociadas a [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="24497-104">Retrieves 10 analysis alternates for all ink associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="24497-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24497-105">Syntax</span></span>


```C++
HRESULT GetAlternates(
  [out] IAnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a><span data-ttu-id="24497-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24497-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24497-107">*ppAlternates* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="24497-107">*ppAlternates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24497-108">Un puntero a los 10 principales objetos [**IAnalysisAlternate**](ianalysisalternate.md) para todas las entradas de lápiz asociadas a [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="24497-108">A pointer to the top 10 [**IAnalysisAlternate**](ianalysisalternate.md) objects for all ink associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24497-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24497-109">Return value</span></span>

<span data-ttu-id="24497-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="24497-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="24497-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="24497-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="24497-112">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppAlternates* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="24497-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAlternates* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="24497-113">La alternativa superior se devuelve como la primera alternativa de la colección.</span><span class="sxs-lookup"><span data-stu-id="24497-113">The top alternate is returned as the first alternate of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="24497-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24497-114">Requirements</span></span>



| <span data-ttu-id="24497-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="24497-115">Requirement</span></span> | <span data-ttu-id="24497-116">Value</span><span class="sxs-lookup"><span data-stu-id="24497-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24497-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24497-117">Minimum supported client</span></span><br/> | <span data-ttu-id="24497-118">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="24497-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="24497-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24497-119">Minimum supported server</span></span><br/> | <span data-ttu-id="24497-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="24497-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="24497-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="24497-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="24497-122"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="24497-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="24497-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="24497-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24497-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24497-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="24497-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="24497-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24497-126">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="24497-126">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="24497-127">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="24497-127">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="24497-128">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="24497-128">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="24497-129">**IInkAnalyzer:: GetAlternatesForContextNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="24497-129">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="24497-130">**IInkAnalyzer:: GetAlternatesForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="24497-130">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="24497-131">**IInkAnalyzer:: ModifyTopAlternate (método)**</span><span class="sxs-lookup"><span data-stu-id="24497-131">**IInkAnalyzer::ModifyTopAlternate Method**</span></span>](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[<span data-ttu-id="24497-132">**IInkAnalyzer:: ModifyTopAlternateWithConfirmation (método)**</span><span class="sxs-lookup"><span data-stu-id="24497-132">**IInkAnalyzer::ModifyTopAlternateWithConfirmation Method**</span></span>](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[<span data-ttu-id="24497-133">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="24497-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

