---
description: 'El método EndOfStream notifica al pin que no se espera ningún dato adicional. Este método implementa el método IPin:: EndOfStream.'
ms.assetid: 5c3b5f90-4194-4d65-9f1a-55edf327e3b3
title: Método CBaseOutputPin. EndOfStream (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1cd903e811dbcd000ba202fc86c0fcb41bf221b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671537"
---
# <a name="cbaseoutputpinendofstream-method"></a><span data-ttu-id="c3fc8-104">CBaseOutputPin. EndOfStream, método</span><span class="sxs-lookup"><span data-stu-id="c3fc8-104">CBaseOutputPin.EndOfStream method</span></span>

<span data-ttu-id="c3fc8-105">El `EndOfStream` método notifica al pin que no se espera ningún dato adicional.</span><span class="sxs-lookup"><span data-stu-id="c3fc8-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="c3fc8-106">Este método implementa el método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="c3fc8-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3fc8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3fc8-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="c3fc8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c3fc8-108">Parameters</span></span>

<span data-ttu-id="c3fc8-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c3fc8-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3fc8-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c3fc8-110">Return value</span></span>

<span data-ttu-id="c3fc8-111">Devuelve E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="c3fc8-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3fc8-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3fc8-112">Remarks</span></span>

<span data-ttu-id="c3fc8-113">Solo se debe llamar a este método en los pin de entrada, por lo que la implementación de **CBaseOutputPin** devuelve E \_ inesperada.</span><span class="sxs-lookup"><span data-stu-id="c3fc8-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3fc8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3fc8-114">Requirements</span></span>



| <span data-ttu-id="c3fc8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3fc8-115">Requirement</span></span> | <span data-ttu-id="c3fc8-116">Value</span><span class="sxs-lookup"><span data-stu-id="c3fc8-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3fc8-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3fc8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c3fc8-118"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3fc8-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c3fc8-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c3fc8-119">Library</span></span><br/> | <dl> <span data-ttu-id="c3fc8-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c3fc8-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3fc8-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3fc8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3fc8-122">**Clase CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="c3fc8-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




