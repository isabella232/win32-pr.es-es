---
description: Guarda los resultados del análisis para los trazos especificados asociados a un IInkAnalyzer.
ms.assetid: 6ff29b95-6c76-4e3d-b4c0-5e7cb6a9ddf9
title: 'IInkAnalyzer:: SaveResultsForStrokes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1371b056cf01beba75fdcbd427c526ed29d20c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360334"
---
# <a name="iinkanalyzersaveresultsforstrokes-method"></a><span data-ttu-id="5a81e-103">IInkAnalyzer:: SaveResultsForStrokes (método)</span><span class="sxs-lookup"><span data-stu-id="5a81e-103">IInkAnalyzer::SaveResultsForStrokes method</span></span>

<span data-ttu-id="5a81e-104">Guarda los resultados del análisis para los trazos especificados asociados a un [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="5a81e-104">Saves analysis results for the specified strokes associated with an [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5a81e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a81e-105">Syntax</span></span>


```C++
HRESULT SaveResultsForStrokes(
  [in]          ULONG ulStrokeIdsCount,
  [in]          LONG  *plStrokeIds,
  [in, out]     ULONG *pulSerializedDataSize,
  [out, retval] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a><span data-ttu-id="5a81e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5a81e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a81e-107">*ulStrokeIdsCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5a81e-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a81e-108">Número de identificadores de trazo en **plStrokeIds**.</span><span class="sxs-lookup"><span data-stu-id="5a81e-108">The number of stroke identifiers in **plStrokeIds**.</span></span>

</dd> <dt>

<span data-ttu-id="5a81e-109">*plStrokeIds* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5a81e-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a81e-110">Matriz de identificadores de trazo.</span><span class="sxs-lookup"><span data-stu-id="5a81e-110">The array of stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="5a81e-111">*pulSerializedDataSize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5a81e-111">*pulSerializedDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a81e-112">Número de bytes de *ppbSerializedData*.</span><span class="sxs-lookup"><span data-stu-id="5a81e-112">The number of bytes in *ppbSerializedData*.</span></span>

</dd> <dt>

<span data-ttu-id="5a81e-113">*ppbSerializedData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5a81e-113">*ppbSerializedData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5a81e-114">Puntero a los datos de análisis serializados.</span><span class="sxs-lookup"><span data-stu-id="5a81e-114">Pointer to the serialized analysis data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a81e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5a81e-115">Return value</span></span>

<span data-ttu-id="5a81e-116">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5a81e-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5a81e-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a81e-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="5a81e-118">Para evitar una pérdida de memoria, llame a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) en \* *ppbSerializedData* cuando ya no necesite la información.</span><span class="sxs-lookup"><span data-stu-id="5a81e-118">To avoid a memory leak, call [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) on \**ppbSerializedData* when you no longer need the information.</span></span>

 

<span data-ttu-id="5a81e-119">Este método guarda los resultados del análisis actual para los trazos especificados.</span><span class="sxs-lookup"><span data-stu-id="5a81e-119">This method saves the current analysis results for the specified strokes.</span></span> <span data-ttu-id="5a81e-120">Este método guarda los objetos [**IContextNode**](icontextnode.md) de hoja de tinta que contienen los trazos y todos los antecesores de esos nodos de contexto.</span><span class="sxs-lookup"><span data-stu-id="5a81e-120">This method saves the ink leaf [**IContextNode**](icontextnode.md) objects containing the strokes and all of the ancestors of those context nodes.</span></span> <span data-ttu-id="5a81e-121">Este método no guarda ningún nodo de datos de trazo o de sugerencia de análisis.</span><span class="sxs-lookup"><span data-stu-id="5a81e-121">This method does not save any stroke data or analysis hint nodes.</span></span> <span data-ttu-id="5a81e-122">Es responsabilidad de la aplicación sincronizar los resultados del análisis y los datos de trazo correspondientes, si persiste.</span><span class="sxs-lookup"><span data-stu-id="5a81e-122">It is the responsibility of your application to synchronize any analysis results and corresponding stroke data, if it persists.</span></span>

<span data-ttu-id="5a81e-123">Este método devuelve un código de error cuando se rellena parcialmente un objeto [**IContextNode**](icontextnode.md) que se va a guardar (vea [**IContextNode:: GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span><span class="sxs-lookup"><span data-stu-id="5a81e-123">This method returns an error code when an [**IContextNode**](icontextnode.md) object to save is partially populated (see [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a81e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a81e-124">Requirements</span></span>



| <span data-ttu-id="5a81e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a81e-125">Requirement</span></span> | <span data-ttu-id="5a81e-126">Value</span><span class="sxs-lookup"><span data-stu-id="5a81e-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a81e-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a81e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5a81e-128">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5a81e-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5a81e-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a81e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5a81e-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5a81e-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5a81e-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a81e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a81e-132"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5a81e-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5a81e-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5a81e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a81e-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a81e-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5a81e-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a81e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a81e-136">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="5a81e-136">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="5a81e-137">**IInkAnalyzer:: LoadResults (método)**</span><span class="sxs-lookup"><span data-stu-id="5a81e-137">**IInkAnalyzer::LoadResults Method**</span></span>](iinkanalyzer-loadresults.md)
</dt> <dt>

[<span data-ttu-id="5a81e-138">**IInkAnalyzer:: SaveResults (método)**</span><span class="sxs-lookup"><span data-stu-id="5a81e-138">**IInkAnalyzer::SaveResults Method**</span></span>](iinkanalyzer-saveresults.md)
</dt> <dt>

[<span data-ttu-id="5a81e-139">**IInkAnalyzer:: SaveResultsForNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="5a81e-139">**IInkAnalyzer::SaveResultsForNodes Method**</span></span>](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[<span data-ttu-id="5a81e-140">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="5a81e-140">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="5a81e-141">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="5a81e-141">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

