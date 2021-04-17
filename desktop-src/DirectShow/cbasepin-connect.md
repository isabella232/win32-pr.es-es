---
description: 'El método Connect conecta el PIN a otro PIN. Este método implementa el método IPin:: Connect.'
ms.assetid: 8ea99d2f-09da-4b15-a3b0-04ceb7888bc1
title: Método CBasePin. Connect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed8bcdab7e0909e59e7d9ec00645786f8ce48c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661273"
---
# <a name="cbasepinconnect-method"></a><span data-ttu-id="76421-104">CBasePin. Connect (método)</span><span class="sxs-lookup"><span data-stu-id="76421-104">CBasePin.Connect method</span></span>

<span data-ttu-id="76421-105">El `Connect` método conecta el PIN a otro PIN.</span><span class="sxs-lookup"><span data-stu-id="76421-105">The `Connect` method connects the pin to another pin.</span></span> <span data-ttu-id="76421-106">Este método implementa el método [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) .</span><span class="sxs-lookup"><span data-stu-id="76421-106">This method implements the [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="76421-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76421-107">Syntax</span></span>


```C++
HRESULT Connect(
         IPin          *pReceivePin,
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="76421-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="76421-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76421-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="76421-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="76421-110">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN receptor.</span><span class="sxs-lookup"><span data-stu-id="76421-110">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="76421-111">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="76421-111">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="76421-112">Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica el tipo de medio para la conexión.</span><span class="sxs-lookup"><span data-stu-id="76421-112">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type for the connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76421-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="76421-113">Return value</span></span>

<span data-ttu-id="76421-114">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="76421-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="76421-115">Entre los valores posibles se incluyen los de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="76421-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="76421-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="76421-116">Return code</span></span>                                                                                                  | <span data-ttu-id="76421-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="76421-117">Description</span></span>                                                                        |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="76421-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="76421-118"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="76421-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="76421-119">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="76421-120"><dt>**VFW \_ E \_ ya \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="76421-120"><dt>**VFW\_E\_ALREADY\_CONNECTED**</dt></span></span> </dl>    | <span data-ttu-id="76421-121">El PIN ya está conectado.</span><span class="sxs-lookup"><span data-stu-id="76421-121">The pin is already connected.</span></span><br/>                                           |
| <dl> <span data-ttu-id="76421-122"><dt>**VFW \_ E \_ no \_ hay \_ tipos aceptables**</dt></span><span class="sxs-lookup"><span data-stu-id="76421-122"><dt>**VFW\_E\_NO\_ACCEPTABLE\_TYPES**</dt></span></span> </dl> | <span data-ttu-id="76421-123">No se pudo encontrar un tipo de medio aceptable.</span><span class="sxs-lookup"><span data-stu-id="76421-123">Could not find an acceptable media type.</span></span><br/>                                |
| <dl> <span data-ttu-id="76421-124"><dt>**VFW \_ E \_ no \_ detenido**</dt></span><span class="sxs-lookup"><span data-stu-id="76421-124"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl>          | <span data-ttu-id="76421-125">El filtro está activo y el PIN no admite la reconexión dinámica.</span><span class="sxs-lookup"><span data-stu-id="76421-125">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |
| <dl> <span data-ttu-id="76421-126"><dt>**\_tipo VFW \_ E \_ no \_ aceptado**</dt></span><span class="sxs-lookup"><span data-stu-id="76421-126"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl>   | <span data-ttu-id="76421-127">El tipo de medio especificado no es aceptable.</span><span class="sxs-lookup"><span data-stu-id="76421-127">The specified media type is not acceptable.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="76421-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76421-128">Remarks</span></span>

<span data-ttu-id="76421-129">El parámetro *PMT* puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="76421-129">The *pmt* parameter can be **NULL**.</span></span> <span data-ttu-id="76421-130">También puede especificar un tipo de medio parcial, con un valor de GUID \_ null para el tipo, subtipo o formato principal.</span><span class="sxs-lookup"><span data-stu-id="76421-130">It can also specify a partial media type, with a value of GUID\_NULL for the major type, subtype, or format.</span></span>

<span data-ttu-id="76421-131">En la clase base, este método comprueba si el PIN ya está conectado y si el filtro está detenido.</span><span class="sxs-lookup"><span data-stu-id="76421-131">In the base class, this method tests whether the pin is already connected and whether the filter is stopped.</span></span> <span data-ttu-id="76421-132">Delega el resto del proceso de conexión al método [**CBasePin:: AgreeMediaType**](cbasepin-agreemediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="76421-132">It delegates the rest of the connection process to the [**CBasePin::AgreeMediaType**](cbasepin-agreemediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="76421-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76421-133">Requirements</span></span>



| <span data-ttu-id="76421-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="76421-134">Requirement</span></span> | <span data-ttu-id="76421-135">Value</span><span class="sxs-lookup"><span data-stu-id="76421-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76421-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="76421-136">Header</span></span><br/>  | <dl> <span data-ttu-id="76421-137"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="76421-137"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="76421-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="76421-138">Library</span></span><br/> | <dl> <span data-ttu-id="76421-139"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="76421-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76421-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="76421-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76421-141">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="76421-141">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




