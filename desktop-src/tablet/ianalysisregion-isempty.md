---
description: Recupera un valor que indica si IAnalysisRegion representa una región vacía.
ms.assetid: 3a536b01-e7ee-4103-88c4-d83377ea9fdb
title: 'IAnalysisRegion:: IsEmpty (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsEmpty
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c1fb4ebbe487119c65f153f78e192de38e6393fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720370"
---
# <a name="ianalysisregionisempty-method"></a><span data-ttu-id="8d4ba-103">IAnalysisRegion:: IsEmpty (método)</span><span class="sxs-lookup"><span data-stu-id="8d4ba-103">IAnalysisRegion::IsEmpty method</span></span>

<span data-ttu-id="8d4ba-104">Recupera un valor que indica si [**IAnalysisRegion**](ianalysisregion.md) representa una región vacía.</span><span class="sxs-lookup"><span data-stu-id="8d4ba-104">Retrieves a value indicating whether the [**IAnalysisRegion**](ianalysisregion.md) represents an empty region.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d4ba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d4ba-105">Syntax</span></span>


```C++
HRESULT IsEmpty(
  [out] VARIANT_BOOL *pfIsEmpty
);
```



## <a name="parameters"></a><span data-ttu-id="8d4ba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d4ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d4ba-107">*pfIsEmpty* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8d4ba-107">*pfIsEmpty* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d4ba-108">**Variante \_ TRUE** si la región representada está vacía; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="8d4ba-108">**VARIANT\_TRUE** if the represented region is empty; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d4ba-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d4ba-109">Return value</span></span>

<span data-ttu-id="8d4ba-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8d4ba-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d4ba-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d4ba-111">Requirements</span></span>



| <span data-ttu-id="8d4ba-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d4ba-112">Requirement</span></span> | <span data-ttu-id="8d4ba-113">Value</span><span class="sxs-lookup"><span data-stu-id="8d4ba-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d4ba-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d4ba-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8d4ba-115">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8d4ba-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8d4ba-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d4ba-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8d4ba-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8d4ba-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8d4ba-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d4ba-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d4ba-119"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8d4ba-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8d4ba-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8d4ba-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d4ba-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d4ba-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8d4ba-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d4ba-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d4ba-123">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="8d4ba-123">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="8d4ba-124">**IAnalysisRegion:: IsInfinite (método)**</span><span class="sxs-lookup"><span data-stu-id="8d4ba-124">**IAnalysisRegion::IsInfinite Method**</span></span>](ianalysisregion-isinfinite.md)
</dt> <dt>

[<span data-ttu-id="8d4ba-125">**IAnalysisRegion:: MakeEmpty (método)**</span><span class="sxs-lookup"><span data-stu-id="8d4ba-125">**IAnalysisRegion::MakeEmpty Method**</span></span>](ianalysisregion-makeempty.md)
</dt> <dt>

[<span data-ttu-id="8d4ba-126">**IAnalysisRegion:: MakeInfinite (método)**</span><span class="sxs-lookup"><span data-stu-id="8d4ba-126">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
</dt> <dt>

[<span data-ttu-id="8d4ba-127">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="8d4ba-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




