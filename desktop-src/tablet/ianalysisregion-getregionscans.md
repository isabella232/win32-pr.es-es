---
description: Recupera una matriz de rectángulos que define el área de IAnalysisRegion.
ms.assetid: 40de4c27-4b3b-4db3-af08-cb53e638db6b
title: 'IAnalysisRegion:: GetRegionScans (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetRegionScans
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6cb8db60b5818f5bc2bc38892912e9ec40af1eb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677405"
---
# <a name="ianalysisregiongetregionscans-method"></a><span data-ttu-id="a958d-103">IAnalysisRegion:: GetRegionScans (método)</span><span class="sxs-lookup"><span data-stu-id="a958d-103">IAnalysisRegion::GetRegionScans method</span></span>

<span data-ttu-id="a958d-104">Recupera una matriz de rectángulos que define el área de [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="a958d-104">Retrieves an array of rectangles that defines the area of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a958d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a958d-105">Syntax</span></span>


```C++
HRESULT GetRegionScans(
  [out] ULONG *pulCount,
  [out] RECT  **pRegionScans
);
```



## <a name="parameters"></a><span data-ttu-id="a958d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a958d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a958d-107">*pulCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a958d-107">*pulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a958d-108">Número de rectángulos devueltos en *pRegionScans*.</span><span class="sxs-lookup"><span data-stu-id="a958d-108">The number of rectangles returned in *pRegionScans*.</span></span>

</dd> <dt>

<span data-ttu-id="a958d-109">*pRegionScans* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a958d-109">*pRegionScans* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a958d-110">Puntero a una matriz de rectángulos que define el área de [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="a958d-110">A pointer to an array of rectangles that defines the area of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a958d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a958d-111">Return value</span></span>

<span data-ttu-id="a958d-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a958d-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a958d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a958d-113">Remarks</span></span>

<span data-ttu-id="a958d-114">Si *pRegionScans* se pasa como **null**, el método **GetRegionScans** devuelve **S \_ correcto** y el número de rectángulos se devuelve en *pulCount*.</span><span class="sxs-lookup"><span data-stu-id="a958d-114">If *pRegionScans* is passed as **NULL**, the **GetRegionScans** method returns **S\_OK** and the number of rectangles is returned in *pulCount*.</span></span>

> [!Caution]  
> <span data-ttu-id="a958d-115">Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *pRegionScans* cuando ya no necesite la información.</span><span class="sxs-lookup"><span data-stu-id="a958d-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pRegionScans* when you no longer need the information.</span></span>

 

<span data-ttu-id="a958d-116">Los límites de los rectángulos están en coordenadas de espacio de tinta.</span><span class="sxs-lookup"><span data-stu-id="a958d-116">The bounds of the rectangles are in ink-space coordinates.</span></span>

<span data-ttu-id="a958d-117">La Unión de los rectángulos devueltos representa el área de [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="a958d-117">The union of the returned rectangles represents the area of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a958d-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a958d-118">Examples</span></span>

<span data-ttu-id="a958d-119">En el ejemplo siguiente se muestra cómo obtener los rectángulos que definen el área de [**IAnalysisRegion**](ianalysisregion.md) `region` y cómo obtener solo el número de rectángulos.</span><span class="sxs-lookup"><span data-stu-id="a958d-119">The following example shows how to get the rectangles that define the area of the [**IAnalysisRegion**](ianalysisregion.md), `region` and how to get only the number of rectangles.</span></span>


```C++
// Get the count and the rectangles.
ULONG count = 0;
RECT* rects = 0;
region->GetRegionScans(&count, &rects);

// Use rects

::CoTaskMemFree(rects);

// GetRegionScans just gets the count and returns S_OK
ULONG number = 0;
region->GetRegionScans(&number, NULL); 
```



## <a name="requirements"></a><span data-ttu-id="a958d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a958d-120">Requirements</span></span>



| <span data-ttu-id="a958d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a958d-121">Requirement</span></span> | <span data-ttu-id="a958d-122">Value</span><span class="sxs-lookup"><span data-stu-id="a958d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a958d-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a958d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a958d-124">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a958d-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a958d-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a958d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a958d-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a958d-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a958d-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a958d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a958d-128"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a958d-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a958d-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a958d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a958d-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a958d-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a958d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="a958d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a958d-132">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="a958d-132">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="a958d-133">**IAnalysisRegion:: GetBounds (método)**</span><span class="sxs-lookup"><span data-stu-id="a958d-133">**IAnalysisRegion::GetBounds Method**</span></span>](ianalysisregion-getbounds.md)
</dt> <dt>

[<span data-ttu-id="a958d-134">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="a958d-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

