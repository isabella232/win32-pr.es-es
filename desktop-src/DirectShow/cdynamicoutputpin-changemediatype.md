---
description: El método ChangeMediaType cambia dinámicamente el tipo de medio para la conexión.
ms.assetid: 38efdfdc-f636-4cad-b8d3-8c63a277644e
title: Método CDynamicOutputPin. ChangeMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89c15e3076a95f8fee3f2f2970fc59da5cf3bf4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661357"
---
# <a name="cdynamicoutputpinchangemediatype-method"></a><span data-ttu-id="49be1-103">CDynamicOutputPin. ChangeMediaType, método</span><span class="sxs-lookup"><span data-stu-id="49be1-103">CDynamicOutputPin.ChangeMediaType method</span></span>

<span data-ttu-id="49be1-104">El `ChangeMediaType` método cambia dinámicamente el tipo de medio para la conexión.</span><span class="sxs-lookup"><span data-stu-id="49be1-104">The `ChangeMediaType` method dynamically changes the media type for the connection.</span></span> <span data-ttu-id="49be1-105">El cambio puede producirse mientras se ejecuta el gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="49be1-105">The change can occur while the filter graph is running.</span></span> <span data-ttu-id="49be1-106">Una vez que se llama a este método, no se pueden entregar los ejemplos con el tipo de medio anterior.</span><span class="sxs-lookup"><span data-stu-id="49be1-106">Once this method is called, samples with the old media type cannot be delivered.</span></span> <span data-ttu-id="49be1-107">El llamador debe asegurarse de que no haya ejemplos antiguos pendientes.</span><span class="sxs-lookup"><span data-stu-id="49be1-107">The caller must ensure that no old samples are pending.</span></span>

## <a name="syntax"></a><span data-ttu-id="49be1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49be1-108">Syntax</span></span>


```C++
HRESULT ChangeMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="49be1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49be1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49be1-110">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="49be1-110">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="49be1-111">Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="49be1-111">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49be1-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49be1-112">Return value</span></span>

<span data-ttu-id="49be1-113">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="49be1-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="49be1-114">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="49be1-114">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="49be1-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="49be1-115">Return code</span></span>                                                                                           | <span data-ttu-id="49be1-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="49be1-116">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="49be1-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="49be1-117"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="49be1-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="49be1-118">Success.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="49be1-119"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="49be1-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="49be1-120">Error.</span><span class="sxs-lookup"><span data-stu-id="49be1-120">Failure.</span></span> <span data-ttu-id="49be1-121">Es posible que el filtro propietario no llamara a [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span><span class="sxs-lookup"><span data-stu-id="49be1-121">Possibly the owning filter did not call [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span></span><br/> |
| <dl> <span data-ttu-id="49be1-122"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="49be1-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="49be1-123">El PIN no está conectado.</span><span class="sxs-lookup"><span data-stu-id="49be1-123">The pin is not connected.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="49be1-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49be1-124">Remarks</span></span>

<span data-ttu-id="49be1-125">Llame al método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="49be1-125">Call the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method before calling this method.</span></span>

<span data-ttu-id="49be1-126">Este método comprueba primero si el PIN de entrada de nivel inferior puede aceptar el nuevo formato sin volver a conectarse.</span><span class="sxs-lookup"><span data-stu-id="49be1-126">This method first checks whether the downstream input pin can accept the new format without reconnecting.</span></span> <span data-ttu-id="49be1-127">Consulta el PIN de entrada de la interfaz [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) .</span><span class="sxs-lookup"><span data-stu-id="49be1-127">It queries the input pin for the [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) interface.</span></span> <span data-ttu-id="49be1-128">Si el PIN de entrada es compatible con **IPinConnection**, el método llama al método [**IPinConnection::D ynamicqueryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) con el tipo de medio propuesto.</span><span class="sxs-lookup"><span data-stu-id="49be1-128">If the input pin supports **IPinConnection**, the method calls the [**IPinConnection::DynamicQueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) method with the proposed media type.</span></span> <span data-ttu-id="49be1-129">Si el PIN de entrada acepta el nuevo tipo de archivo multimedia, el método llama al método [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) y vuelve a negociar los requisitos del asignador.</span><span class="sxs-lookup"><span data-stu-id="49be1-129">If the input pin accepts the new media type, the method calls the [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method and renegotiates the allocator requirements.</span></span>

<span data-ttu-id="49be1-130">Por otro lado, si el PIN de bajada no admite **IPinConnection**, o si rechaza el nuevo tipo de medio, el método llama al método [**CDynamicOutputPin::D ynamicreconnect**](cdynamicoutputpin-dynamicreconnect.md) para realizar una reconexión dinámica.</span><span class="sxs-lookup"><span data-stu-id="49be1-130">On the other hand, if the downstream pin does not support **IPinConnection**, or if it rejects the new media type, the method calls the [**CDynamicOutputPin::DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md) method to perform a dynamic reconnection.</span></span>

## <a name="requirements"></a><span data-ttu-id="49be1-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49be1-131">Requirements</span></span>



| <span data-ttu-id="49be1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="49be1-132">Requirement</span></span> | <span data-ttu-id="49be1-133">Value</span><span class="sxs-lookup"><span data-stu-id="49be1-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49be1-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49be1-134">Header</span></span><br/>  | <dl> <span data-ttu-id="49be1-135"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49be1-135"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="49be1-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="49be1-136">Library</span></span><br/> | <dl> <span data-ttu-id="49be1-137"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="49be1-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49be1-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="49be1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49be1-139">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="49be1-139">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




