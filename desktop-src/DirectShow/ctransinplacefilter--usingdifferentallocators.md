---
description: El método UsingDifferentAllocators determina si los pin de entrada y salida están usando asignadores diferentes.
ms.assetid: 75feaa6e-6395-4d47-ae92-10a857f8764b
title: Método CTransInPlaceFilter. UsingDifferentAllocators (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.UsingDifferentAllocators
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f20802836adb665614e2bbfb8cb79bdccd5a36ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661262"
---
# <a name="ctransinplacefilterusingdifferentallocators-method"></a><span data-ttu-id="bb617-103">CTransInPlaceFilter. UsingDifferentAllocators, método</span><span class="sxs-lookup"><span data-stu-id="bb617-103">CTransInPlaceFilter.UsingDifferentAllocators method</span></span>

<span data-ttu-id="bb617-104">El `UsingDifferentAllocators` método determina si los pin de entrada y salida están usando asignadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="bb617-104">The `UsingDifferentAllocators` method determines whether the input and output pins are using different allocators.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb617-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb617-105">Syntax</span></span>


```C++
BOOL UsingDifferentAllocators() const;
```



## <a name="parameters"></a><span data-ttu-id="bb617-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb617-106">Parameters</span></span>

<span data-ttu-id="bb617-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bb617-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bb617-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb617-108">Return value</span></span>

<span data-ttu-id="bb617-109">Devuelve **true** si los pin de entrada y salida están usando asignadores diferentes, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bb617-109">Returns **TRUE** if the input and output pins are using different allocators, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb617-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb617-110">Requirements</span></span>



| <span data-ttu-id="bb617-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb617-111">Requirement</span></span> | <span data-ttu-id="bb617-112">Value</span><span class="sxs-lookup"><span data-stu-id="bb617-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb617-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb617-113">Header</span></span><br/>  | <dl> <span data-ttu-id="bb617-114"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb617-114"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bb617-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bb617-115">Library</span></span><br/> | <dl> <span data-ttu-id="bb617-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bb617-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb617-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb617-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb617-118">**Clase CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="bb617-118">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




