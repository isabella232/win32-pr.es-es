---
description: Recupera un valor que indica si IAnalysisRegion representa una región infinita.
ms.assetid: b84ec9ec-42d0-4d03-b78b-433e55d04897
title: 'IAnalysisRegion:: IsInfinite (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsInfinite
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f7d284c043f38a681b969f72d751f9acaa954c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275487"
---
# <a name="ianalysisregionisinfinite-method"></a><span data-ttu-id="87d62-103">IAnalysisRegion:: IsInfinite (método)</span><span class="sxs-lookup"><span data-stu-id="87d62-103">IAnalysisRegion::IsInfinite method</span></span>

<span data-ttu-id="87d62-104">Recupera un valor que indica si [**IAnalysisRegion**](ianalysisregion.md) representa una región infinita.</span><span class="sxs-lookup"><span data-stu-id="87d62-104">Retrieves a value indicating whether the [**IAnalysisRegion**](ianalysisregion.md) represents an infinite region.</span></span>

## <a name="syntax"></a><span data-ttu-id="87d62-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87d62-105">Syntax</span></span>


```C++
HRESULT IsInfinite(
  [out] VARIANT_BOOL *pfIsInfinite
);
```



## <a name="parameters"></a><span data-ttu-id="87d62-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87d62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87d62-107">*pfIsInfinite* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="87d62-107">*pfIsInfinite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87d62-108">**Variante \_ TRUE** si la región representada es infinita; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="87d62-108">**VARIANT\_TRUE** if the represented region is infinite; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87d62-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87d62-109">Return value</span></span>

<span data-ttu-id="87d62-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="87d62-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="87d62-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87d62-111">Requirements</span></span>



| <span data-ttu-id="87d62-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="87d62-112">Requirement</span></span> | <span data-ttu-id="87d62-113">Value</span><span class="sxs-lookup"><span data-stu-id="87d62-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87d62-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87d62-114">Minimum supported client</span></span><br/> | <span data-ttu-id="87d62-115">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="87d62-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="87d62-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87d62-116">Minimum supported server</span></span><br/> | <span data-ttu-id="87d62-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="87d62-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="87d62-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87d62-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="87d62-119"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="87d62-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="87d62-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="87d62-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87d62-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87d62-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="87d62-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="87d62-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87d62-123">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="87d62-123">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="87d62-124">**IAnalysisRegion:: IsEmpty (método)**</span><span class="sxs-lookup"><span data-stu-id="87d62-124">**IAnalysisRegion::IsEmpty Method**</span></span>](ianalysisregion-isempty.md)
</dt> <dt>

[<span data-ttu-id="87d62-125">**IAnalysisRegion:: MakeEmpty (método)**</span><span class="sxs-lookup"><span data-stu-id="87d62-125">**IAnalysisRegion::MakeEmpty Method**</span></span>](ianalysisregion-makeempty.md)
</dt> <dt>

[<span data-ttu-id="87d62-126">**IAnalysisRegion:: MakeInfinite (método)**</span><span class="sxs-lookup"><span data-stu-id="87d62-126">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
</dt> <dt>

[<span data-ttu-id="87d62-127">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="87d62-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




