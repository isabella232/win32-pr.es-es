---
description: Guarda todos los resultados de análisis de un IInkAnalyzer.
ms.assetid: 538eb781-d831-475b-ba09-271d71f6a6bf
title: 'IInkAnalyzer:: SaveResults (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a07351662512ad3234dfe6847cd8c4300bd035e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360335"
---
# <a name="iinkanalyzersaveresults-method"></a><span data-ttu-id="cfa78-103">IInkAnalyzer:: SaveResults (método)</span><span class="sxs-lookup"><span data-stu-id="cfa78-103">IInkAnalyzer::SaveResults method</span></span>

<span data-ttu-id="cfa78-104">Guarda todos los resultados de análisis de un [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="cfa78-104">Saves all analysis results for an [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cfa78-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cfa78-105">Syntax</span></span>


```C++
HRESULT SaveResults(
  [out] ULONG *pulSerializedDataSize,
  [out] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a><span data-ttu-id="cfa78-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cfa78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfa78-107">*pulSerializedDataSize* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cfa78-107">*pulSerializedDataSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfa78-108">Número de bytes de *ppbSerializedData*.</span><span class="sxs-lookup"><span data-stu-id="cfa78-108">The number of bytes in *ppbSerializedData*.</span></span>

</dd> <dt>

<span data-ttu-id="cfa78-109">*ppbSerializedData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cfa78-109">*ppbSerializedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfa78-110">Una matriz que contiene los resultados del análisis guardado.</span><span class="sxs-lookup"><span data-stu-id="cfa78-110">An array containing the saved analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfa78-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cfa78-111">Return value</span></span>

<span data-ttu-id="cfa78-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="cfa78-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cfa78-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cfa78-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="cfa78-114">Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *ppbSerializedData* cuando ya no necesite la información.</span><span class="sxs-lookup"><span data-stu-id="cfa78-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppbSerializedData* when you no longer need the information.</span></span>

 

<span data-ttu-id="cfa78-115">Este método guarda todos los resultados del análisis actual, que incluyen la sugerencia de análisis actual y los nodos de reconocedor personalizados (vea [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="cfa78-115">This method saves all the current analysis results, which include current analysis hint and custom recognizer nodes (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="cfa78-116">Este método no guarda ningún dato de trazo.</span><span class="sxs-lookup"><span data-stu-id="cfa78-116">This method does not save any stroke data.</span></span> <span data-ttu-id="cfa78-117">Es responsabilidad de la aplicación sincronizar los resultados del análisis y los trazos correspondientes si guarda los datos.</span><span class="sxs-lookup"><span data-stu-id="cfa78-117">It is the responsibility of your application to synchronize any analysis results and corresponding strokes if it persists data.</span></span>

<span data-ttu-id="cfa78-118">Este método devuelve un código de error cuando se rellena parcialmente un objeto [**IContextNode**](icontextnode.md) que se va a guardar (vea [**IContextNode:: GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span><span class="sxs-lookup"><span data-stu-id="cfa78-118">This method returns an error code when an [**IContextNode**](icontextnode.md) object to save is partially populated (see [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfa78-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfa78-119">Requirements</span></span>



| <span data-ttu-id="cfa78-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfa78-120">Requirement</span></span> | <span data-ttu-id="cfa78-121">Value</span><span class="sxs-lookup"><span data-stu-id="cfa78-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfa78-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfa78-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cfa78-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cfa78-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cfa78-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfa78-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cfa78-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cfa78-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cfa78-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cfa78-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfa78-127"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cfa78-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cfa78-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cfa78-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfa78-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfa78-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cfa78-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfa78-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfa78-131">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="cfa78-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="cfa78-132">**IInkAnalyzer:: LoadResults (método)**</span><span class="sxs-lookup"><span data-stu-id="cfa78-132">**IInkAnalyzer::LoadResults Method**</span></span>](iinkanalyzer-loadresults.md)
</dt> <dt>

[<span data-ttu-id="cfa78-133">**IInkAnalyzer:: SaveResultsForNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="cfa78-133">**IInkAnalyzer::SaveResultsForNodes Method**</span></span>](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[<span data-ttu-id="cfa78-134">**IInkAnalyzer:: SaveResultsForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="cfa78-134">**IInkAnalyzer::SaveResultsForStrokes Method**</span></span>](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[<span data-ttu-id="cfa78-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="cfa78-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="cfa78-136">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="cfa78-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

