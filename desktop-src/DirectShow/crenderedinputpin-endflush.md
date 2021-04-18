---
description: 'El método EndFlush finaliza una operación de vaciado. Este método implementa el método IPin:: EndFlush.'
ms.assetid: 5c27bf76-6886-431d-9958-5064c53909ec
title: Método CRenderedInputPin. EndFlush (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d80f6cbc31a8bc5bf797847465a218f32631c1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671068"
---
# <a name="crenderedinputpinendflush-method"></a><span data-ttu-id="db12f-104">CRenderedInputPin. EndFlush, método</span><span class="sxs-lookup"><span data-stu-id="db12f-104">CRenderedInputPin.EndFlush method</span></span>

<span data-ttu-id="db12f-105">El `EndFlush` método finaliza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="db12f-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="db12f-106">Este método implementa el método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="db12f-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="db12f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db12f-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="db12f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db12f-108">Parameters</span></span>

<span data-ttu-id="db12f-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="db12f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="db12f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db12f-110">Return value</span></span>

<span data-ttu-id="db12f-111">Devuelve \_ si es correcto, o un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="db12f-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="db12f-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db12f-112">Remarks</span></span>

<span data-ttu-id="db12f-113">Este método borra cualquier evento pendiente [**de \_ EC**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="db12f-113">This method clears any pending [**EC\_COMPLETE**](ec-complete.md) events.</span></span>

## <a name="requirements"></a><span data-ttu-id="db12f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db12f-114">Requirements</span></span>



| <span data-ttu-id="db12f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="db12f-115">Requirement</span></span> | <span data-ttu-id="db12f-116">Value</span><span class="sxs-lookup"><span data-stu-id="db12f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db12f-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db12f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="db12f-118"><dt>Amextra. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db12f-118"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="db12f-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="db12f-119">Library</span></span><br/> | <dl> <span data-ttu-id="db12f-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="db12f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db12f-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="db12f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db12f-122">**Clase CRenderedInputPin**</span><span class="sxs-lookup"><span data-stu-id="db12f-122">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




