---
description: El método ForceRefresh está obsoleto.
ms.assetid: 9895f72b-abf8-46a8-aa75-2a30901a4c41
title: Método CPosPassThru. ForceRefresh (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ForceRefresh
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1955afe069dc419b710978eecf662758916e4cb1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680472"
---
# <a name="cpospassthruforcerefresh-method"></a><span data-ttu-id="bfe7e-103">CPosPassThru. ForceRefresh, método</span><span class="sxs-lookup"><span data-stu-id="bfe7e-103">CPosPassThru.ForceRefresh method</span></span>

<span data-ttu-id="bfe7e-104">El `ForceRefresh` método está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-104">The `ForceRefresh` method is obsolete.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfe7e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfe7e-105">Syntax</span></span>


```C++
HRESULT ForceRefresh();
```



## <a name="parameters"></a><span data-ttu-id="bfe7e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bfe7e-106">Parameters</span></span>

<span data-ttu-id="bfe7e-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bfe7e-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bfe7e-108">Return value</span></span>

<span data-ttu-id="bfe7e-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfe7e-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfe7e-110">Remarks</span></span>

<span data-ttu-id="bfe7e-111">Originalmente, esta clase se diseñó para almacenar en caché punteros a las interfaces [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) y [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-111">Originally this class was designed to cache pointers to the connected pin's [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interfaces.</span></span> <span data-ttu-id="bfe7e-112">El `ForceRefresh` método liberó dichas interfaces.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-112">The `ForceRefresh` method released those interfaces.</span></span>

<span data-ttu-id="bfe7e-113">Tal y como se implementa actualmente, esta clase no almacena en caché esas interfaces.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-113">As currently implemented, this class does not cache those interfaces.</span></span> <span data-ttu-id="bfe7e-114">Por compatibilidad, `ForceRefresh` todavía se incluye el método, pero devuelve S \_ OK sin hacer nada.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-114">For compatibility, the `ForceRefresh` method is still included, but it returns S\_OK without doing anything.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfe7e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfe7e-115">Requirements</span></span>



| <span data-ttu-id="bfe7e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfe7e-116">Requirement</span></span> | <span data-ttu-id="bfe7e-117">Value</span><span class="sxs-lookup"><span data-stu-id="bfe7e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfe7e-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bfe7e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="bfe7e-119"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bfe7e-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bfe7e-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bfe7e-120">Library</span></span><br/> | <dl> <span data-ttu-id="bfe7e-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bfe7e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfe7e-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfe7e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfe7e-123">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="bfe7e-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




