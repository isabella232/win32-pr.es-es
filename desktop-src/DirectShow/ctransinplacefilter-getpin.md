---
description: 'Método CTransInPlaceFilter.GetPin: el método GetPin recupera un pin.'
ms.assetid: d8e4973b-2af4-4141-ab2e-ea2159cd51be
title: Método CTransInPlaceFilter.GetPin (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1075f2a14c58b085b73f2e4283458286c118a7ae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084773"
---
# <a name="ctransinplacefiltergetpin-method"></a><span data-ttu-id="cb323-103">Método CTransInPlaceFilter.GetPin</span><span class="sxs-lookup"><span data-stu-id="cb323-103">CTransInPlaceFilter.GetPin method</span></span>

<span data-ttu-id="cb323-104">El `GetPin` método recupera un pin.</span><span class="sxs-lookup"><span data-stu-id="cb323-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb323-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb323-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="cb323-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb323-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb323-107">*n*</span><span class="sxs-lookup"><span data-stu-id="cb323-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="cb323-108">Número del pin especificado, indexado a partir de cero.</span><span class="sxs-lookup"><span data-stu-id="cb323-108">Number of the specified pin, indexed from zero.</span></span> <span data-ttu-id="cb323-109">En este filtro, el pin 0 es el pin de entrada y el pin 1 es el pin de salida.</span><span class="sxs-lookup"><span data-stu-id="cb323-109">On this filter, pin 0 is the input pin, and pin 1 is the output pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb323-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb323-110">Return value</span></span>

<span data-ttu-id="cb323-111">Devuelve un puntero al objeto [**CBasePin**](cbasepin.md) que implementa el pin o **NULL** si se produce un error en el método.</span><span class="sxs-lookup"><span data-stu-id="cb323-111">Returns a pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the method fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb323-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb323-112">Remarks</span></span>

<span data-ttu-id="cb323-113">Este método invalida el [**método CTransformFilter::GetPin.**](ctransformfilter-getpin.md)</span><span class="sxs-lookup"><span data-stu-id="cb323-113">This method overrides the [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method.</span></span> <span data-ttu-id="cb323-114">La primera vez que se llama al método, crea ambos pines.</span><span class="sxs-lookup"><span data-stu-id="cb323-114">The first time the method is called, it creates both pins.</span></span>

<span data-ttu-id="cb323-115">Este método no incrementa el recuento de referencias en el pin devuelto, por lo que el pin devuelto no tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="cb323-115">This method does not increment the reference count on the returned pin, so the returned pin does not have an outstanding reference count.</span></span> <span data-ttu-id="cb323-116">Si el autor de la llamada necesita mantener una referencia en el pin, debe llamar al método **IUnknown::AddRef** en el pin.</span><span class="sxs-lookup"><span data-stu-id="cb323-116">If the caller needs to keep a reference on the pin, it should call the **IUnknown::AddRef** method on the pin.</span></span>

<span data-ttu-id="cb323-117">Si el filtro usa los pines [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) y [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) predeterminados, probablemente no necesite invalidar este método.</span><span class="sxs-lookup"><span data-stu-id="cb323-117">If the filter uses the default [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) and [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) pins, you probably do not need to override this method.</span></span> <span data-ttu-id="cb323-118">Sin embargo, si el filtro usa pines que extienden esas clases, debe invalidar este método para crear pins de ese tipo.</span><span class="sxs-lookup"><span data-stu-id="cb323-118">If the filter uses pins that extend those classes, however, you must override this method to create pins of that type.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb323-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb323-119">Requirements</span></span>



| <span data-ttu-id="cb323-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb323-120">Requirement</span></span> | <span data-ttu-id="cb323-121">Value</span><span class="sxs-lookup"><span data-stu-id="cb323-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb323-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb323-122">Header</span></span><br/>  | <dl> <span data-ttu-id="cb323-123"><dt>Transip.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb323-123"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cb323-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cb323-124">Library</span></span><br/> | <dl> <span data-ttu-id="cb323-125"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="cb323-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb323-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cb323-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb323-127">**CTransInPlaceFilter (clase)**</span><span class="sxs-lookup"><span data-stu-id="cb323-127">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




