---
description: El \_ método get DestinationHeight recupera el alto del rectángulo de destino actual.
ms.assetid: 0001d98a-3a5c-47f1-8f5e-ce464d64131a
title: Método CBaseControlVideo.get_DestinationHeight (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9dc4fc63e63adbc42b75ae9a24d1c47e7d985c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660520"
---
# <a name="cbasecontrolvideoget_destinationheight-method"></a><span data-ttu-id="5dc83-103">CBaseControlVideo. Get \_ DestinationHeight (método)</span><span class="sxs-lookup"><span data-stu-id="5dc83-103">CBaseControlVideo.get\_DestinationHeight method</span></span>

<span data-ttu-id="5dc83-104">El `get_DestinationHeight` método recupera el alto del rectángulo de destino actual.</span><span class="sxs-lookup"><span data-stu-id="5dc83-104">The `get_DestinationHeight` method retrieves the current destination rectangle height.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dc83-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5dc83-105">Syntax</span></span>


```C++
HRESULT get_DestinationHeight(
   long *pDestinationHeight
);
```



## <a name="parameters"></a><span data-ttu-id="5dc83-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5dc83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dc83-107">*pDestinationHeight*</span><span class="sxs-lookup"><span data-stu-id="5dc83-107">*pDestinationHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="5dc83-108">Puntero al alto de destino.</span><span class="sxs-lookup"><span data-stu-id="5dc83-108">Pointer to the destination height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dc83-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5dc83-109">Return value</span></span>

<span data-ttu-id="5dc83-110">Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.</span><span class="sxs-lookup"><span data-stu-id="5dc83-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="5dc83-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5dc83-111">Return code</span></span>                                                                                           | <span data-ttu-id="5dc83-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5dc83-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5dc83-113"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="5dc83-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="5dc83-114">Error.</span><span class="sxs-lookup"><span data-stu-id="5dc83-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="5dc83-115"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="5dc83-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="5dc83-116">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="5dc83-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="5dc83-117"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="5dc83-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="5dc83-118">No se puede realizar la operación porque los PIN no están conectados.</span><span class="sxs-lookup"><span data-stu-id="5dc83-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="5dc83-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="5dc83-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="5dc83-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="5dc83-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="5dc83-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5dc83-121">Remarks</span></span>

<span data-ttu-id="5dc83-122">Esta función miembro implementa el método [**IBasicVideo:: get \_ DestinationHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationheight) .</span><span class="sxs-lookup"><span data-stu-id="5dc83-122">This member function implements the [**IBasicVideo::get\_DestinationHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationheight) method.</span></span>

<span data-ttu-id="5dc83-123">Una aplicación puede cambiar los rectángulos de origen y de destino para el vídeo a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="5dc83-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="5dc83-124">El rectángulo de origen afecta a qué sección del origen de vídeo nativo aparecerá en la pantalla. el rectángulo de destino afecta al lugar donde se reproducirá.</span><span class="sxs-lookup"><span data-stu-id="5dc83-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where it will be played.</span></span> <span data-ttu-id="5dc83-125">El rectángulo de destino es relativo al área cliente de la ventana en la que se está reproduciendo.</span><span class="sxs-lookup"><span data-stu-id="5dc83-125">The destination rectangle is relative to the client area of the window that it is playing in.</span></span> <span data-ttu-id="5dc83-126">La esquina superior izquierda de la ventana es la coordenada (0,0).</span><span class="sxs-lookup"><span data-stu-id="5dc83-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="5dc83-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5dc83-127">Requirements</span></span>



| <span data-ttu-id="5dc83-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dc83-128">Requirement</span></span> | <span data-ttu-id="5dc83-129">Value</span><span class="sxs-lookup"><span data-stu-id="5dc83-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dc83-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5dc83-130">Header</span></span><br/>  | <dl> <span data-ttu-id="5dc83-131"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5dc83-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5dc83-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5dc83-132">Library</span></span><br/> | <dl> <span data-ttu-id="5dc83-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5dc83-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dc83-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="5dc83-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dc83-135">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="5dc83-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




