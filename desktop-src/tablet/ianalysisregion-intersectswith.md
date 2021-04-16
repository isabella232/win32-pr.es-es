---
description: Determina si el área del IAnalysisRegion se corta con el rectángulo especificado.
ms.assetid: 683c3ad8-0236-474e-a16d-6164c2244cfb
title: 'IAnalysisRegion:: IntersectsWith (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectsWith
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 99ff1ce8d3039b04d83f9cdd5c1d6aebe00be407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542094"
---
# <a name="ianalysisregionintersectswith-method"></a><span data-ttu-id="25d50-103">IAnalysisRegion:: IntersectsWith (método)</span><span class="sxs-lookup"><span data-stu-id="25d50-103">IAnalysisRegion::IntersectsWith method</span></span>

<span data-ttu-id="25d50-104">Determina si el área del [**IAnalysisRegion**](ianalysisregion.md) se corta con el rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="25d50-104">Determines whether the area of the [**IAnalysisRegion**](ianalysisregion.md) intersects with the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="25d50-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25d50-105">Syntax</span></span>


```C++
HRESULT IntersectsWith(
  [in]  RECT         *pRectangle,
  [out] VARIANT_BOOL *pfIsIntersecting
);
```



## <a name="parameters"></a><span data-ttu-id="25d50-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25d50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25d50-107">*pRectangle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="25d50-107">*pRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25d50-108">Puntero al rectángulo con el que se va a comparar, en coordenadas de espacio de tinta.</span><span class="sxs-lookup"><span data-stu-id="25d50-108">A pointer to the rectangle with which to compare, in ink-space coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="25d50-109">*pfIsIntersecting* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="25d50-109">*pfIsIntersecting* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25d50-110">**Variante \_ TRUE** si el área del [**IAnalysisRegion**](ianalysisregion.md) se corta con el rectángulo especificado; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="25d50-110">**VARIANT\_TRUE** if the area of the [**IAnalysisRegion**](ianalysisregion.md) intersects with the specified rectangle; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25d50-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25d50-111">Return value</span></span>

<span data-ttu-id="25d50-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="25d50-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="25d50-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25d50-113">Remarks</span></span>

<span data-ttu-id="25d50-114">La comparación está en coordenadas de espacio de tinta.</span><span class="sxs-lookup"><span data-stu-id="25d50-114">The comparison is in ink-space coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="25d50-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25d50-115">Requirements</span></span>



| <span data-ttu-id="25d50-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="25d50-116">Requirement</span></span> | <span data-ttu-id="25d50-117">Value</span><span class="sxs-lookup"><span data-stu-id="25d50-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25d50-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25d50-118">Minimum supported client</span></span><br/> | <span data-ttu-id="25d50-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="25d50-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="25d50-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25d50-120">Minimum supported server</span></span><br/> | <span data-ttu-id="25d50-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="25d50-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="25d50-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25d50-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="25d50-123"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="25d50-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="25d50-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="25d50-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25d50-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25d50-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="25d50-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="25d50-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25d50-127">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="25d50-127">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="25d50-128">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="25d50-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




