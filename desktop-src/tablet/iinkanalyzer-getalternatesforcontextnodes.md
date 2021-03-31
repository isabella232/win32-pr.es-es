---
description: Recupera alternativas de análisis para los nodos de una colección IContextNodes especificada.
ms.assetid: 7d047808-4360-442d-8fd9-4ee4aeeed2c9
title: 'IInkAnalyzer:: GetAlternatesForContextNodes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 71c53e4a8e0989d836d63db5c5cae8c89d56fcf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154417"
---
# <a name="iinkanalyzergetalternatesforcontextnodes-method"></a><span data-ttu-id="20835-103">IInkAnalyzer:: GetAlternatesForContextNodes (método)</span><span class="sxs-lookup"><span data-stu-id="20835-103">IInkAnalyzer::GetAlternatesForContextNodes method</span></span>

<span data-ttu-id="20835-104">Recupera alternativas de análisis para los nodos de una colección [**IContextNodes**](icontextnodes.md) especificada.</span><span class="sxs-lookup"><span data-stu-id="20835-104">Retrieves analysis alternates for the nodes in a specified [**IContextNodes**](icontextnodes.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="20835-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20835-105">Syntax</span></span>


```C++
HRESULT GetAlternatesForContextNodes(
  [in]  IContextNodes      *pContextNodes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a><span data-ttu-id="20835-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20835-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20835-107">*pContextNodes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="20835-107">*pContextNodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20835-108">Colección de [**IContextNodes**](icontextnodes.md) para la que se devuelven las alternativas de análisis.</span><span class="sxs-lookup"><span data-stu-id="20835-108">The [**IContextNodes**](icontextnodes.md) collection for which the analysis alternatives are returned.</span></span>

</dd> <dt>

<span data-ttu-id="20835-109">*ulMaximumAlternates* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="20835-109">*ulMaximumAlternates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20835-110">Número máximo de alternativas que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="20835-110">The maximum number of alternatives to return.</span></span>

</dd> <dt>

<span data-ttu-id="20835-111">*ppAlternates* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="20835-111">*ppAlternates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20835-112">El objeto [**IAnalysisAlternates**](ianalysisalternates.md) que contiene las alternativas de análisis.</span><span class="sxs-lookup"><span data-stu-id="20835-112">The [**IAnalysisAlternates**](ianalysisalternates.md) object containing the analysis alternatives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20835-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20835-113">Return value</span></span>

<span data-ttu-id="20835-114">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="20835-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="20835-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20835-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="20835-116">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppAlternates* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="20835-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAlternates* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="20835-117">La [**IAnalysisAlternate**](ianalysisalternate.md) superior se devuelve como la primera alternativa de la colección.</span><span class="sxs-lookup"><span data-stu-id="20835-117">The top [**IAnalysisAlternate**](ianalysisalternate.md) is returned as the first alternate of the collection.</span></span>

<span data-ttu-id="20835-118">Los objetos [**IContextNode**](icontextnode.md) de *pContextNodes* no tienen que representar áreas adyacentes del documento.</span><span class="sxs-lookup"><span data-stu-id="20835-118">The [**IContextNode**](icontextnode.md) objects in *pContextNodes* do not have to represent adjacent areas of the document.</span></span>

<span data-ttu-id="20835-119">Para cada sugerencia de análisis en los nodos, [**IInkAnalyzer**](iinkanalyzer.md) devuelve solo la alternativa superior.</span><span class="sxs-lookup"><span data-stu-id="20835-119">For each analysis hint in nodes, the [**IInkAnalyzer**](iinkanalyzer.md) returns only the top alternate.</span></span>

## <a name="requirements"></a><span data-ttu-id="20835-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20835-120">Requirements</span></span>



| <span data-ttu-id="20835-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="20835-121">Requirement</span></span> | <span data-ttu-id="20835-122">Value</span><span class="sxs-lookup"><span data-stu-id="20835-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20835-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20835-123">Minimum supported client</span></span><br/> | <span data-ttu-id="20835-124">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="20835-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="20835-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20835-125">Minimum supported server</span></span><br/> | <span data-ttu-id="20835-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="20835-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="20835-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20835-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="20835-128"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="20835-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="20835-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="20835-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20835-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20835-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="20835-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="20835-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20835-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="20835-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="20835-133">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="20835-133">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="20835-134">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="20835-134">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="20835-135">**IInkAnalyzer:: GetAlternates (método)**</span><span class="sxs-lookup"><span data-stu-id="20835-135">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="20835-136">**IInkAnalyzer:: GetAlternatesForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="20835-136">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="20835-137">**IInkAnalyzer:: ModifyTopAlternate (método)**</span><span class="sxs-lookup"><span data-stu-id="20835-137">**IInkAnalyzer::ModifyTopAlternate Method**</span></span>](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[<span data-ttu-id="20835-138">**IInkAnalyzer:: ModifyTopAlternateWithConfirmation (método)**</span><span class="sxs-lookup"><span data-stu-id="20835-138">**IInkAnalyzer::ModifyTopAlternateWithConfirmation Method**</span></span>](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[<span data-ttu-id="20835-139">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="20835-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

