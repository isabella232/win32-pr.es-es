---
description: 'El método ReceiveConnection acepta una conexión desde otro PIN. Este método implementa el método IPin:: ReceiveConnection.'
ms.assetid: f17e7d93-ac45-4b8a-98c6-0c76ec7117c9
title: Método CBasePin. ReceiveConnection (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ReceiveConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d0a8134201af1d3c931121f59a20360020a53a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660945"
---
# <a name="cbasepinreceiveconnection-method"></a><span data-ttu-id="2252b-104">CBasePin. ReceiveConnection, método</span><span class="sxs-lookup"><span data-stu-id="2252b-104">CBasePin.ReceiveConnection method</span></span>

<span data-ttu-id="2252b-105">El `ReceiveConnection` método acepta una conexión desde otro PIN.</span><span class="sxs-lookup"><span data-stu-id="2252b-105">The `ReceiveConnection` method accepts a connection from another pin.</span></span> <span data-ttu-id="2252b-106">Este método implementa el método [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) .</span><span class="sxs-lookup"><span data-stu-id="2252b-106">This method implements the [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2252b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2252b-107">Syntax</span></span>


```C++
HRESULT ReceiveConnection(
   IPin          *pConnector,
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="2252b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2252b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2252b-109">*pConnector*</span><span class="sxs-lookup"><span data-stu-id="2252b-109">*pConnector*</span></span> 
</dt> <dd>

<span data-ttu-id="2252b-110">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN de conexión.</span><span class="sxs-lookup"><span data-stu-id="2252b-110">Pointer to the connecting pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="2252b-111">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="2252b-111">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="2252b-112">Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="2252b-112">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2252b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2252b-113">Return value</span></span>

<span data-ttu-id="2252b-114">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2252b-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2252b-115">Entre los valores posibles se incluyen los de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2252b-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="2252b-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2252b-116">Return code</span></span>                                                                                                | <span data-ttu-id="2252b-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2252b-117">Description</span></span>                                                                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2252b-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2252b-118"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="2252b-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="2252b-119">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="2252b-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="2252b-120"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="2252b-121">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="2252b-121">**NULL** pointer argument.</span></span><br/>                                              |
| <dl> <span data-ttu-id="2252b-122"><dt>**VFW \_ E \_ ya \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="2252b-122"><dt>**VFW\_E\_ALREADY\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="2252b-123">El PIN ya está conectado.</span><span class="sxs-lookup"><span data-stu-id="2252b-123">The pin is already connected.</span></span><br/>                                           |
| <dl> <span data-ttu-id="2252b-124"><dt>**VFW \_ E \_ no \_ detenido**</dt></span><span class="sxs-lookup"><span data-stu-id="2252b-124"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl>        | <span data-ttu-id="2252b-125">El filtro está activo y el PIN no admite la reconexión dinámica.</span><span class="sxs-lookup"><span data-stu-id="2252b-125">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |
| <dl> <span data-ttu-id="2252b-126"><dt>**\_tipo VFW \_ E \_ no \_ aceptado**</dt></span><span class="sxs-lookup"><span data-stu-id="2252b-126"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="2252b-127">El tipo de medio especificado no es aceptable.</span><span class="sxs-lookup"><span data-stu-id="2252b-127">The specified media type is not acceptable.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="2252b-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2252b-128">Remarks</span></span>

<span data-ttu-id="2252b-129">El PIN de salida llama a este método en el PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="2252b-129">The output pin calls this method on the input pin.</span></span> <span data-ttu-id="2252b-130">Si el PIN de entrada devuelve un código de error, se produce un error en la conexión.</span><span class="sxs-lookup"><span data-stu-id="2252b-130">If the input pin returns an error code, the connection fails.</span></span>

<span data-ttu-id="2252b-131">En la clase base, este método realiza los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2252b-131">In the base class, this method performs the following steps:</span></span>

-   <span data-ttu-id="2252b-132">Comprueba si el PIN ya está conectado.</span><span class="sxs-lookup"><span data-stu-id="2252b-132">Checks whether the pin is already connected.</span></span>
-   <span data-ttu-id="2252b-133">Comprueba si el filtro está detenido.</span><span class="sxs-lookup"><span data-stu-id="2252b-133">Checks whether the filter is stopped.</span></span>
-   <span data-ttu-id="2252b-134">Llama al método [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) para probar si el PIN de conexión es adecuado.</span><span class="sxs-lookup"><span data-stu-id="2252b-134">Calls the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method to test whether the connecting pin is suitable.</span></span>
-   <span data-ttu-id="2252b-135">Llama al método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) para comprobar si el tipo de medio es aceptable.</span><span class="sxs-lookup"><span data-stu-id="2252b-135">Calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to test whether the media type is acceptable.</span></span>

<span data-ttu-id="2252b-136">Si todos estos pasos se realizan correctamente, el método llama a los métodos [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) y [**SetMediaType**](cbasepin-setmediatype.md) para completar la conexión.</span><span class="sxs-lookup"><span data-stu-id="2252b-136">If all of these steps succeed, the method calls the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) and [**SetMediaType**](cbasepin-setmediatype.md) methods to complete the connection.</span></span> <span data-ttu-id="2252b-137">Estos métodos almacenan el tipo de medio y un puntero al terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="2252b-137">These methods store the media type and a pointer to the output pin.</span></span>

<span data-ttu-id="2252b-138">Si se produce un error en **CheckConnect** o **CheckMediaType** , la clase base llama al método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) para interrumpir la conexión y, a continuación, devuelve un código de error de `ReceiveConnection` .</span><span class="sxs-lookup"><span data-stu-id="2252b-138">If **CheckConnect** or **CheckMediaType** fail, the base class calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method to break the connection and then returns an error code from `ReceiveConnection`.</span></span>

## <a name="requirements"></a><span data-ttu-id="2252b-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2252b-139">Requirements</span></span>



| <span data-ttu-id="2252b-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="2252b-140">Requirement</span></span> | <span data-ttu-id="2252b-141">Value</span><span class="sxs-lookup"><span data-stu-id="2252b-141">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2252b-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2252b-142">Header</span></span><br/>  | <dl> <span data-ttu-id="2252b-143"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2252b-143"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2252b-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2252b-144">Library</span></span><br/> | <dl> <span data-ttu-id="2252b-145"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2252b-145"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2252b-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="2252b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2252b-147">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="2252b-147">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




