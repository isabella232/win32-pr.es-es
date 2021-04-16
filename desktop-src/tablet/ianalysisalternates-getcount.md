---
description: Recupera el número de objetos IAnalysisAlternate contenidos en la colección IAnalysisAlternates.
ms.assetid: 17b71b5a-638a-4e6e-a43b-4ca3c8eba257
title: 'IAnalysisAlternates:: GetCount (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6300ff994d7bd49461e9be39aa433586ecaabc75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696550"
---
# <a name="ianalysisalternatesgetcount-method"></a><span data-ttu-id="431d6-103">IAnalysisAlternates:: GetCount (método)</span><span class="sxs-lookup"><span data-stu-id="431d6-103">IAnalysisAlternates::GetCount method</span></span>

<span data-ttu-id="431d6-104">Recupera el número de objetos [**IAnalysisAlternate**](ianalysisalternate.md) contenidos en la colección [**IAnalysisAlternates**](ianalysisalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="431d6-104">Retrieves the number of [**IAnalysisAlternate**](ianalysisalternate.md) objects contained in the [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="431d6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="431d6-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="431d6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="431d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="431d6-107">*pulCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="431d6-107">*pulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="431d6-108">Entero de 32 bits sin signo que se establece en el número de objetos [**IAnalysisAlternate**](ianalysisalternate.md) contenidos en la colección [**IAnalysisAlternates**](ianalysisalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="431d6-108">An unsigned 32-bit integer that is set to the number of [**IAnalysisAlternate**](ianalysisalternate.md) objects contained in the [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="431d6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="431d6-109">Return value</span></span>

<span data-ttu-id="431d6-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="431d6-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="431d6-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="431d6-111">Requirements</span></span>



| <span data-ttu-id="431d6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="431d6-112">Requirement</span></span> | <span data-ttu-id="431d6-113">Value</span><span class="sxs-lookup"><span data-stu-id="431d6-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="431d6-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="431d6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="431d6-115">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="431d6-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="431d6-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="431d6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="431d6-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="431d6-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="431d6-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="431d6-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="431d6-119"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="431d6-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="431d6-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="431d6-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="431d6-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="431d6-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="431d6-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="431d6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="431d6-123">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="431d6-123">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="431d6-124">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="431d6-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




