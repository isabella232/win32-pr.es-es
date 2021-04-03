---
description: Devuelve los identificadores de trazo asociados a este IAnalysisAlternate.
ms.assetid: 495d485f-0d16-4085-9213-cc55f3f259f0
title: 'IAnalysisAlternate:: GetStrokeIds (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 80882a83e9a0fa9bf973990a689e2abf1a52a870
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908031"
---
# <a name="ianalysisalternategetstrokeids-method"></a><span data-ttu-id="daea6-103">IAnalysisAlternate:: GetStrokeIds (método)</span><span class="sxs-lookup"><span data-stu-id="daea6-103">IAnalysisAlternate::GetStrokeIds method</span></span>

<span data-ttu-id="daea6-104">Devuelve los identificadores de trazo asociados a este [**IAnalysisAlternate**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="daea6-104">Returns the stroke identifiers that are associated with this [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="daea6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="daea6-105">Syntax</span></span>


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="daea6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="daea6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daea6-107">*pulStrokeIdsCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="daea6-107">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="daea6-108">Un puntero a un **ULong** que se establece en el número de identificadores de trazo asociados a este [**IAnalysisAlternate**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="daea6-108">A pointer to a **ULONG** that is set to the number of stroke identifiers associated with this [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

</dd> <dt>

<span data-ttu-id="daea6-109">*pplStrokeIds* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="daea6-109">*pplStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="daea6-110">\[out, size \_ es ( \* *PULSTROKEIDSCOUNT* \* sizeof (Long))\]</span><span class="sxs-lookup"><span data-stu-id="daea6-110">\[out, size\_is(\**pulStrokeIdsCount* \* sizeof(LONG))\]</span></span>

<span data-ttu-id="daea6-111">Matriz de *pulStrokeIdsCount* de longitud **larga** que se establece en los identificadores de trazo asociados a este [**IAnalysisAlternate**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="daea6-111">An array of **LONG** of length *pulStrokeIdsCount* that is set to the stroke identifiers associated with this [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daea6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="daea6-112">Return value</span></span>

<span data-ttu-id="daea6-113">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="daea6-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="daea6-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="daea6-114">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="daea6-115">Para evitar una pérdida de memoria, use [CoTaskMemFree](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *pplStrokeIds* cuando ya no necesite la información.</span><span class="sxs-lookup"><span data-stu-id="daea6-115">To avoid a memory leak, use [CoTaskMemFree](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pplStrokeIds* when you no longer need the information.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="daea6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="daea6-116">Requirements</span></span>



| <span data-ttu-id="daea6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="daea6-117">Requirement</span></span> | <span data-ttu-id="daea6-118">Value</span><span class="sxs-lookup"><span data-stu-id="daea6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daea6-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="daea6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="daea6-120">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="daea6-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="daea6-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="daea6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="daea6-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="daea6-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="daea6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="daea6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="daea6-124"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="daea6-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="daea6-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="daea6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="daea6-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="daea6-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="daea6-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="daea6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daea6-128">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="daea6-128">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="daea6-129">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="daea6-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

