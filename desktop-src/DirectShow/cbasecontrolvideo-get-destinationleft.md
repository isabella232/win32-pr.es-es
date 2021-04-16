---
description: El \_ método get DestinationLeft recupera la coordenada izquierda del rectángulo de destino actual.
ms.assetid: f1c6d784-7ec3-4d44-a3fb-c1e3b988e392
title: Método CBaseControlVideo.get_DestinationLeft (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationLeft
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f433d880fd7f568a173a91c533e0d07bf97e6443
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690345"
---
# <a name="cbasecontrolvideoget_destinationleft-method"></a><span data-ttu-id="546b6-103">CBaseControlVideo. Get \_ DestinationLeft (método)</span><span class="sxs-lookup"><span data-stu-id="546b6-103">CBaseControlVideo.get\_DestinationLeft method</span></span>

<span data-ttu-id="546b6-104">El `get_DestinationLeft` método recupera la coordenada izquierda del rectángulo de destino actual.</span><span class="sxs-lookup"><span data-stu-id="546b6-104">The `get_DestinationLeft` method retrieves the left coordinate of the current destination rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="546b6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="546b6-105">Syntax</span></span>


```C++
HRESULT get_DestinationLeft(
   long *pDestinationLeft
);
```



## <a name="parameters"></a><span data-ttu-id="546b6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="546b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="546b6-107">*pDestinationLeft*</span><span class="sxs-lookup"><span data-stu-id="546b6-107">*pDestinationLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="546b6-108">Puntero a la coordenada izquierda del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="546b6-108">Pointer to the left coordinate of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="546b6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="546b6-109">Return value</span></span>

<span data-ttu-id="546b6-110">Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.</span><span class="sxs-lookup"><span data-stu-id="546b6-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="546b6-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="546b6-111">Return code</span></span>                                                                                           | <span data-ttu-id="546b6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="546b6-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="546b6-113"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="546b6-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="546b6-114">Error.</span><span class="sxs-lookup"><span data-stu-id="546b6-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="546b6-115"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="546b6-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="546b6-116">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="546b6-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="546b6-117"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="546b6-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="546b6-118">No se puede realizar la operación porque los PIN no están conectados.</span><span class="sxs-lookup"><span data-stu-id="546b6-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="546b6-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="546b6-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="546b6-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="546b6-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="546b6-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="546b6-121">Remarks</span></span>

<span data-ttu-id="546b6-122">Esta función miembro implementa el método [**IBasicVideo:: get \_ DestinationLeft**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationleft) .</span><span class="sxs-lookup"><span data-stu-id="546b6-122">This member function implements the [**IBasicVideo::get\_DestinationLeft**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationleft) method.</span></span>

<span data-ttu-id="546b6-123">Una aplicación puede cambiar los rectángulos de origen y de destino para el vídeo a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="546b6-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="546b6-124">El rectángulo de origen afecta a qué sección del origen de vídeo nativo aparecerá en la pantalla. el rectángulo de destino afecta al lugar en el que aparecerá el vídeo cuando se reproduzca.</span><span class="sxs-lookup"><span data-stu-id="546b6-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="546b6-125">El rectángulo de destino es relativo al área cliente de la ventana en la que se reproduce.</span><span class="sxs-lookup"><span data-stu-id="546b6-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="546b6-126">La esquina superior izquierda de la ventana es la coordenada (0,0).</span><span class="sxs-lookup"><span data-stu-id="546b6-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="546b6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="546b6-127">Requirements</span></span>



| <span data-ttu-id="546b6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="546b6-128">Requirement</span></span> | <span data-ttu-id="546b6-129">Value</span><span class="sxs-lookup"><span data-stu-id="546b6-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="546b6-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="546b6-130">Header</span></span><br/>  | <dl> <span data-ttu-id="546b6-131"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="546b6-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="546b6-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="546b6-132">Library</span></span><br/> | <dl> <span data-ttu-id="546b6-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="546b6-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="546b6-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="546b6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="546b6-135">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="546b6-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




