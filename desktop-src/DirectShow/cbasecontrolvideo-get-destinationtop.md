---
description: El \_ método get DestinationTop recupera la coordenada superior del rectángulo de destino actual.
ms.assetid: 8d5c1361-18db-4ea1-a507-781397189630
title: Método CBaseControlVideo.get_DestinationTop (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationTop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2c7d450c50b11186546a25ceebd317a308dd805
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660519"
---
# <a name="cbasecontrolvideoget_destinationtop-method"></a><span data-ttu-id="cdfe5-103">CBaseControlVideo. Get \_ DestinationTop (método)</span><span class="sxs-lookup"><span data-stu-id="cdfe5-103">CBaseControlVideo.get\_DestinationTop method</span></span>

<span data-ttu-id="cdfe5-104">El `get_DestinationTop` método recupera la coordenada superior del rectángulo de destino actual.</span><span class="sxs-lookup"><span data-stu-id="cdfe5-104">The `get_DestinationTop` method retrieves the top coordinate of the current destination rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdfe5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cdfe5-105">Syntax</span></span>


```C++
HRESULT get_DestinationTop(
   long *pDestinationTop
);
```



## <a name="parameters"></a><span data-ttu-id="cdfe5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cdfe5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdfe5-107">*pDestinationTop*</span><span class="sxs-lookup"><span data-stu-id="cdfe5-107">*pDestinationTop*</span></span> 
</dt> <dd>

<span data-ttu-id="cdfe5-108">Puntero en la coordenada superior del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="cdfe5-108">Pointer to the top coordinate of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdfe5-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cdfe5-109">Return value</span></span>

<span data-ttu-id="cdfe5-110">Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.</span><span class="sxs-lookup"><span data-stu-id="cdfe5-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="cdfe5-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="cdfe5-111">Return code</span></span>                                                                                           | <span data-ttu-id="cdfe5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="cdfe5-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cdfe5-113"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="cdfe5-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="cdfe5-114">Error.</span><span class="sxs-lookup"><span data-stu-id="cdfe5-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="cdfe5-115"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="cdfe5-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="cdfe5-116">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="cdfe5-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="cdfe5-117"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="cdfe5-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="cdfe5-118">No se puede realizar la operación porque los PIN no están conectados.</span><span class="sxs-lookup"><span data-stu-id="cdfe5-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="cdfe5-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="cdfe5-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="cdfe5-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="cdfe5-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="cdfe5-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cdfe5-121">Remarks</span></span>

<span data-ttu-id="cdfe5-122">Esta función miembro implementa el método [**IBasicVideo:: get \_ DestinationTop**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationtop) .</span><span class="sxs-lookup"><span data-stu-id="cdfe5-122">This member function implements the [**IBasicVideo::get\_DestinationTop**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationtop) method.</span></span>

<span data-ttu-id="cdfe5-123">Una aplicación puede cambiar los rectángulos de origen y de destino para el vídeo a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="cdfe5-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="cdfe5-124">El rectángulo de origen afecta a qué sección del origen de vídeo nativo aparecerá en la pantalla. el rectángulo de destino afecta al lugar en el que aparecerá el vídeo cuando se reproduzca.</span><span class="sxs-lookup"><span data-stu-id="cdfe5-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="cdfe5-125">El rectángulo de destino es relativo al área cliente de la ventana en la que se reproduce.</span><span class="sxs-lookup"><span data-stu-id="cdfe5-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="cdfe5-126">La esquina superior izquierda de la ventana es la coordenada (0,0).</span><span class="sxs-lookup"><span data-stu-id="cdfe5-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="cdfe5-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdfe5-127">Requirements</span></span>



| <span data-ttu-id="cdfe5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdfe5-128">Requirement</span></span> | <span data-ttu-id="cdfe5-129">Value</span><span class="sxs-lookup"><span data-stu-id="cdfe5-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdfe5-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cdfe5-130">Header</span></span><br/>  | <dl> <span data-ttu-id="cdfe5-131"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdfe5-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cdfe5-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cdfe5-132">Library</span></span><br/> | <dl> <span data-ttu-id="cdfe5-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="cdfe5-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdfe5-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="cdfe5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdfe5-135">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="cdfe5-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




