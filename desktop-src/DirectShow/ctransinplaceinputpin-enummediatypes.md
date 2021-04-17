---
description: 'El método EnumMediaTypes enumera los tipos de medios preferidos del PIN. Este método implementa el método IPin:: EnumMediaTypes.'
ms.assetid: 0c28b4b0-a45f-400f-a6d7-7668458f9642
title: Método CTransInPlaceInputPin. EnumMediaTypes (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffa634fa695eb0007b49fc1c36c730c7fbde361b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660364"
---
# <a name="ctransinplaceinputpinenummediatypes-method"></a><span data-ttu-id="bd772-104">CTransInPlaceInputPin. EnumMediaTypes, método</span><span class="sxs-lookup"><span data-stu-id="bd772-104">CTransInPlaceInputPin.EnumMediaTypes method</span></span>

<span data-ttu-id="bd772-105">El `EnumMediaTypes` método enumera los tipos de medios preferidos del PIN.</span><span class="sxs-lookup"><span data-stu-id="bd772-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="bd772-106">Este método implementa el método [**IPin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="bd772-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd772-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd772-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="bd772-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd772-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd772-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="bd772-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="bd772-110">Recibe un puntero a la interfaz [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="bd772-110">Receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd772-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd772-111">Return value</span></span>

<span data-ttu-id="bd772-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bd772-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="bd772-113">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="bd772-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="bd772-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bd772-114">Return code</span></span>                                                                                           | <span data-ttu-id="bd772-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd772-115">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="bd772-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="bd772-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="bd772-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="bd772-117">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="bd772-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bd772-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="bd772-119">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="bd772-119">Insufficient memory.</span></span><br/>             |
| <dl> <span data-ttu-id="bd772-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="bd772-120"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="bd772-121">Puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="bd772-121">**NULL** pointer.</span></span><br/>                |
| <dl> <span data-ttu-id="bd772-122"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="bd772-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="bd772-123">El PIN de salida no está conectado.</span><span class="sxs-lookup"><span data-stu-id="bd772-123">The output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bd772-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd772-124">Remarks</span></span>

<span data-ttu-id="bd772-125">Este método devuelve la interfaz **IEnumMediaTypes** del PIN de entrada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="bd772-125">This method returns the **IEnumMediaTypes** interface from downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd772-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd772-126">Requirements</span></span>



| <span data-ttu-id="bd772-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd772-127">Requirement</span></span> | <span data-ttu-id="bd772-128">Value</span><span class="sxs-lookup"><span data-stu-id="bd772-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd772-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd772-129">Header</span></span><br/>  | <dl> <span data-ttu-id="bd772-130"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd772-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bd772-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bd772-131">Library</span></span><br/> | <dl> <span data-ttu-id="bd772-132"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bd772-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd772-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd772-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd772-134">**Clase CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="bd772-134">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




