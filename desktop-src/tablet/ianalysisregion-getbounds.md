---
description: Obtiene el rectángulo delimitador de IAnalysisRegion.
ms.assetid: 6b9deff7-12e9-4b30-86cb-25b94737d28d
title: 'IAnalysisRegion:: GetBounds (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetBounds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 12bbb8163aa866648a83effc75d668bc4032c8d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810057"
---
# <a name="ianalysisregiongetbounds-method"></a><span data-ttu-id="18f82-103">IAnalysisRegion:: GetBounds (método)</span><span class="sxs-lookup"><span data-stu-id="18f82-103">IAnalysisRegion::GetBounds method</span></span>

<span data-ttu-id="18f82-104">Obtiene el rectángulo delimitador de [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="18f82-104">Gets the bounding rectangle of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="18f82-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18f82-105">Syntax</span></span>


```C++
HRESULT GetBounds(
  [out] RECT *pBoundingRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="18f82-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18f82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18f82-107">*pBoundingRectangle* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="18f82-107">*pBoundingRectangle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18f82-108">Rectángulo delimitador del [**IAnalysisRegion**](ianalysisregion.md) en coordenadas de espacio de la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="18f82-108">The bounding rectangle of the [**IAnalysisRegion**](ianalysisregion.md) in ink space coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18f82-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18f82-109">Return value</span></span>

<span data-ttu-id="18f82-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="18f82-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="18f82-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18f82-111">Remarks</span></span>

<span data-ttu-id="18f82-112">Los límites se encuentran en coordenadas de espacio de tinta.</span><span class="sxs-lookup"><span data-stu-id="18f82-112">The bounds are in ink-space coordinates.</span></span>

<span data-ttu-id="18f82-113">Si [**IAnalysisRegion**](ianalysisregion.md) representa un área infinita, los límites izquierdo y superior son **int \_ min**; y los límites derecho e inferior son **int \_ Max**.</span><span class="sxs-lookup"><span data-stu-id="18f82-113">If the [**IAnalysisRegion**](ianalysisregion.md) represents an infinite area, the left and top bounds are **INT\_MIN**; and the right and bottom bounds are **INT\_MAX**.</span></span>

<span data-ttu-id="18f82-114">Si [**IAnalysisRegion**](ianalysisregion.md) representa un área vacía, todos los límites del rectángulo son 0.</span><span class="sxs-lookup"><span data-stu-id="18f82-114">If the [**IAnalysisRegion**](ianalysisregion.md) represents an empty area, all the bounds of the rectangle are 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="18f82-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18f82-115">Requirements</span></span>



| <span data-ttu-id="18f82-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="18f82-116">Requirement</span></span> | <span data-ttu-id="18f82-117">Value</span><span class="sxs-lookup"><span data-stu-id="18f82-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18f82-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18f82-118">Minimum supported client</span></span><br/> | <span data-ttu-id="18f82-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="18f82-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="18f82-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18f82-120">Minimum supported server</span></span><br/> | <span data-ttu-id="18f82-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="18f82-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="18f82-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18f82-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="18f82-123"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="18f82-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="18f82-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="18f82-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18f82-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18f82-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="18f82-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="18f82-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18f82-127">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="18f82-127">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="18f82-128">**IAnalysisRegion:: GetRegionScans (método)**</span><span class="sxs-lookup"><span data-stu-id="18f82-128">**IAnalysisRegion::GetRegionScans Method**</span></span>](ianalysisregion-getregionscans.md)
</dt> <dt>

[<span data-ttu-id="18f82-129">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="18f82-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




