---
description: Guarda los resultados del análisis de una colección de nodos de contexto específica asociada a un IInkAnalyzer.
ms.assetid: 671bdb11-6e30-4254-b320-208face1f593
title: 'IInkAnalyzer:: SaveResultsForNodes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eb628fafb9bf479e6a011137105005e541180aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154409"
---
# <a name="iinkanalyzersaveresultsfornodes-method"></a><span data-ttu-id="ffd3f-103">IInkAnalyzer:: SaveResultsForNodes (método)</span><span class="sxs-lookup"><span data-stu-id="ffd3f-103">IInkAnalyzer::SaveResultsForNodes method</span></span>

<span data-ttu-id="ffd3f-104">Guarda los resultados del análisis de una colección de nodos de contexto específica asociada a un [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="ffd3f-104">Saves analysis results for a specific context node collection associated with an [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ffd3f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ffd3f-105">Syntax</span></span>


```C++
HRESULT SaveResultsForNodes(
  [in]      IContextNodes *pContextNodes,
  [in, out] ULONG         *pulSerializedDataSize,
  [out]     BYTE          **ppbSerializedData
);
```



## <a name="parameters"></a><span data-ttu-id="ffd3f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ffd3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffd3f-107">*pContextNodes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ffd3f-107">*pContextNodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffd3f-108">Colección de [**IContextNode**](icontextnode.md) para la que se van a guardar los resultados del análisis.</span><span class="sxs-lookup"><span data-stu-id="ffd3f-108">The [**IContextNode**](icontextnode.md) collection for which to save analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="ffd3f-109">*pulSerializedDataSize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ffd3f-109">*pulSerializedDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffd3f-110">Número de bytes de *ppbSerializedData*.</span><span class="sxs-lookup"><span data-stu-id="ffd3f-110">The number of bytes in *ppbSerializedData*.</span></span>

</dd> <dt>

<span data-ttu-id="ffd3f-111">*ppbSerializedData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ffd3f-111">*ppbSerializedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffd3f-112">Puntero a los datos de análisis serializados.</span><span class="sxs-lookup"><span data-stu-id="ffd3f-112">Pointer to the serialized analysis data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffd3f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ffd3f-113">Return value</span></span>

<span data-ttu-id="ffd3f-114">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ffd3f-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ffd3f-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ffd3f-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="ffd3f-116">Para evitar una pérdida de memoria, llame a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) en \* *ppbSerializedData* cuando ya no necesite la información.</span><span class="sxs-lookup"><span data-stu-id="ffd3f-116">To avoid a memory leak, call [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) on \**ppbSerializedData* when you no longer need the information.</span></span>

 

<span data-ttu-id="ffd3f-117">Este método guarda los resultados de análisis actuales de los objetos [**IContextNode**](icontextnode.md) de *pContextNodes* y de todos sus nodos de contexto antecesores y descendientes.</span><span class="sxs-lookup"><span data-stu-id="ffd3f-117">This method saves the current analysis results for the [**IContextNode**](icontextnode.md) objects in *pContextNodes* and all of their ancestor and descendant context nodes.</span></span> <span data-ttu-id="ffd3f-118">Este método no guarda ningún dato de trazo.</span><span class="sxs-lookup"><span data-stu-id="ffd3f-118">This method does not save any stroke data.</span></span> <span data-ttu-id="ffd3f-119">Es responsabilidad de la aplicación sincronizar los resultados del análisis y los datos de trazo correspondientes, si persiste.</span><span class="sxs-lookup"><span data-stu-id="ffd3f-119">It is the responsibility of your application to synchronize any analysis results and corresponding stroke data, if it persists.</span></span>

<span data-ttu-id="ffd3f-120">Si el objeto [**IContextNode**](icontextnode.md) que se va a guardar solo se rellena parcialmente, este método devuelve un código de error (vea [**IContextNode:: GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span><span class="sxs-lookup"><span data-stu-id="ffd3f-120">If the [**IContextNode**](icontextnode.md) object to be saved is only partially populated, this method returns an error code (see [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="ffd3f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffd3f-121">Requirements</span></span>



| <span data-ttu-id="ffd3f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffd3f-122">Requirement</span></span> | <span data-ttu-id="ffd3f-123">Value</span><span class="sxs-lookup"><span data-stu-id="ffd3f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd3f-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffd3f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ffd3f-125">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ffd3f-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ffd3f-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffd3f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ffd3f-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ffd3f-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ffd3f-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ffd3f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffd3f-129"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ffd3f-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ffd3f-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ffd3f-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffd3f-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffd3f-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ffd3f-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffd3f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffd3f-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="ffd3f-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ffd3f-134">**IInkAnalyzer:: LoadResults (método)**</span><span class="sxs-lookup"><span data-stu-id="ffd3f-134">**IInkAnalyzer::LoadResults Method**</span></span>](iinkanalyzer-loadresults.md)
</dt> <dt>

[<span data-ttu-id="ffd3f-135">**IInkAnalyzer:: SaveResults (método)**</span><span class="sxs-lookup"><span data-stu-id="ffd3f-135">**IInkAnalyzer::SaveResults Method**</span></span>](iinkanalyzer-saveresults.md)
</dt> <dt>

[<span data-ttu-id="ffd3f-136">**IInkAnalyzer:: SaveResultsForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="ffd3f-136">**IInkAnalyzer::SaveResultsForStrokes Method**</span></span>](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[<span data-ttu-id="ffd3f-137">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="ffd3f-137">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ffd3f-138">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="ffd3f-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

