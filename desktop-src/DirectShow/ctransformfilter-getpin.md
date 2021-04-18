---
description: El método GetPin recupera un PIN.
ms.assetid: 5d278ef0-e5ce-439e-93b1-fec988c55854
title: Método CTransformFilter. GetPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 30567db84eefd5471dbbe1fbd2d2e5ed64514ba2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680829"
---
# <a name="ctransformfiltergetpin-method"></a><span data-ttu-id="71ee2-103">CTransformFilter. GetPin, método</span><span class="sxs-lookup"><span data-stu-id="71ee2-103">CTransformFilter.GetPin method</span></span>

<span data-ttu-id="71ee2-104">El `GetPin` método recupera un PIN.</span><span class="sxs-lookup"><span data-stu-id="71ee2-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="71ee2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71ee2-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="71ee2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71ee2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71ee2-107">*n*</span><span class="sxs-lookup"><span data-stu-id="71ee2-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="71ee2-108">Número del PIN especificado, indizado desde cero.</span><span class="sxs-lookup"><span data-stu-id="71ee2-108">Number of the specified pin, indexed from zero.</span></span> <span data-ttu-id="71ee2-109">En este filtro, el pin 0 es el PIN de entrada y el pin 1 es el PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="71ee2-109">On this filter, pin 0 is the input pin, and pin 1 is the output pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71ee2-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71ee2-110">Return value</span></span>

<span data-ttu-id="71ee2-111">Devuelve un puntero al objeto [**CBasePin**](cbasepin.md) que implementa el PIN, o **null** si se produce un error en el método.</span><span class="sxs-lookup"><span data-stu-id="71ee2-111">Returns a pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the method fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="71ee2-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71ee2-112">Remarks</span></span>

<span data-ttu-id="71ee2-113">Este método implementa el método [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) virtual puro.</span><span class="sxs-lookup"><span data-stu-id="71ee2-113">This method implements the pure virtual [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method.</span></span> <span data-ttu-id="71ee2-114">La primera vez que se llama al método, se crean ambos PIN.</span><span class="sxs-lookup"><span data-stu-id="71ee2-114">The first time the method is called, it creates both pins.</span></span>

<span data-ttu-id="71ee2-115">Este método no incrementa el recuento de referencias en el PIN devuelto, por lo que el PIN devuelto no tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="71ee2-115">This method does not increment the reference count on the returned pin, so the returned pin does not have an outstanding reference count.</span></span> <span data-ttu-id="71ee2-116">Si el autor de la llamada necesita mantener una referencia en el código PIN, debe llamar al método **IUnknown:: AddRef** en el código PIN.</span><span class="sxs-lookup"><span data-stu-id="71ee2-116">If the caller needs to keep a reference on the pin, it should call the **IUnknown::AddRef** method on the pin.</span></span>

<span data-ttu-id="71ee2-117">Si el filtro usa los pin predeterminados [**CTransformInputPin**](ctransforminputpin.md) y [**CTransformOutputPin**](ctransformoutputpin.md) , probablemente no sea necesario invalidar este método.</span><span class="sxs-lookup"><span data-stu-id="71ee2-117">If the filter uses the default [**CTransformInputPin**](ctransforminputpin.md) and [**CTransformOutputPin**](ctransformoutputpin.md) pins, you probably do not need to override this method.</span></span> <span data-ttu-id="71ee2-118">Sin embargo, si el filtro usa PIN que amplían esas clases, debe invalidar este método para crear los pin de ese tipo.</span><span class="sxs-lookup"><span data-stu-id="71ee2-118">If the filter uses pins that extend those classes, however, you must override this method to create pins of that type.</span></span>

## <a name="requirements"></a><span data-ttu-id="71ee2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71ee2-119">Requirements</span></span>



| <span data-ttu-id="71ee2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="71ee2-120">Requirement</span></span> | <span data-ttu-id="71ee2-121">Value</span><span class="sxs-lookup"><span data-stu-id="71ee2-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71ee2-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71ee2-122">Header</span></span><br/>  | <dl> <span data-ttu-id="71ee2-123"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71ee2-123"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="71ee2-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="71ee2-124">Library</span></span><br/> | <dl> <span data-ttu-id="71ee2-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="71ee2-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71ee2-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="71ee2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71ee2-127">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="71ee2-127">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




