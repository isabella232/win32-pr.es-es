---
description: Recupera el número de objetos IInkAnalysisRecognizer de esta colección.
ms.assetid: dfb5c530-b481-4c60-b7fe-87fe162de270
title: 'IInkAnalysisRecognizers:: GetCount (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e65f8399c661d551e805abe5f1c5db33eb0b154a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542038"
---
# <a name="iinkanalysisrecognizersgetcount-method"></a><span data-ttu-id="f2e37-103">IInkAnalysisRecognizers:: GetCount (método)</span><span class="sxs-lookup"><span data-stu-id="f2e37-103">IInkAnalysisRecognizers::GetCount method</span></span>

<span data-ttu-id="f2e37-104">Recupera el número de objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) de esta colección.</span><span class="sxs-lookup"><span data-stu-id="f2e37-104">Retrieves the number of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2e37-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2e37-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="f2e37-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2e37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2e37-107">*pulCount* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f2e37-107">*pulCount* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f2e37-108">Número de objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) de esta colección.</span><span class="sxs-lookup"><span data-stu-id="f2e37-108">The number of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in this collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2e37-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2e37-109">Return value</span></span>

<span data-ttu-id="f2e37-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f2e37-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2e37-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2e37-111">Requirements</span></span>



| <span data-ttu-id="f2e37-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2e37-112">Requirement</span></span> | <span data-ttu-id="f2e37-113">Value</span><span class="sxs-lookup"><span data-stu-id="f2e37-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e37-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2e37-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f2e37-115">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f2e37-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f2e37-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2e37-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f2e37-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f2e37-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f2e37-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2e37-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2e37-119"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f2e37-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f2e37-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f2e37-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2e37-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2e37-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f2e37-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2e37-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2e37-123">**InkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="f2e37-123">**InkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="f2e37-124">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="f2e37-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




