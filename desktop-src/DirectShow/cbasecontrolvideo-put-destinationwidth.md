---
description: El \_ método put DestinationWidth establece el ancho del rectángulo de destino.
ms.assetid: 1e7a4d38-1453-4dfd-8a2f-0f76b352fc64
title: Método CBaseControlVideo.put_DestinationWidth (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_DestinationWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3ada15c61884e8e8787db06ae6fa3fbee3f79bb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671130"
---
# <a name="cbasecontrolvideoput_destinationwidth-method"></a><span data-ttu-id="1fb23-103">CBaseControlVideo. put \_ DestinationWidth (método)</span><span class="sxs-lookup"><span data-stu-id="1fb23-103">CBaseControlVideo.put\_DestinationWidth method</span></span>

<span data-ttu-id="1fb23-104">El `put_DestinationWidth` método establece el ancho del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="1fb23-104">The `put_DestinationWidth` method sets the width of the destination rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fb23-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1fb23-105">Syntax</span></span>


```C++
HRESULT put_DestinationWidth(
   long DestinationWidth
);
```



## <a name="parameters"></a><span data-ttu-id="1fb23-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1fb23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fb23-107">*DestinationWidth*</span><span class="sxs-lookup"><span data-stu-id="1fb23-107">*DestinationWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="1fb23-108">Nuevo ancho de destino.</span><span class="sxs-lookup"><span data-stu-id="1fb23-108">New destination width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fb23-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1fb23-109">Return value</span></span>

<span data-ttu-id="1fb23-110">Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.</span><span class="sxs-lookup"><span data-stu-id="1fb23-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="1fb23-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1fb23-111">Return code</span></span>                                                                                           | <span data-ttu-id="1fb23-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1fb23-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1fb23-113"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="1fb23-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="1fb23-114">Error.</span><span class="sxs-lookup"><span data-stu-id="1fb23-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="1fb23-115"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1fb23-115"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="1fb23-116">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="1fb23-116">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="1fb23-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="1fb23-117"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="1fb23-118">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="1fb23-118">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="1fb23-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="1fb23-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="1fb23-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="1fb23-120">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="1fb23-121"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="1fb23-121"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="1fb23-122">No se puede realizar la operación porque los PIN no están conectados.</span><span class="sxs-lookup"><span data-stu-id="1fb23-122">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1fb23-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1fb23-123">Remarks</span></span>

<span data-ttu-id="1fb23-124">Una aplicación puede cambiar los rectángulos de origen y de destino para el vídeo a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="1fb23-124">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="1fb23-125">El rectángulo de origen afecta a qué sección del origen de vídeo nativo aparecerá en la pantalla. el rectángulo de destino afecta al lugar en el que aparecerá el vídeo cuando se reproduzca.</span><span class="sxs-lookup"><span data-stu-id="1fb23-125">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="1fb23-126">El rectángulo de destino es relativo al área cliente de la ventana en la que se reproduce.</span><span class="sxs-lookup"><span data-stu-id="1fb23-126">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="1fb23-127">La esquina superior izquierda de la ventana es la coordenada (0,0).</span><span class="sxs-lookup"><span data-stu-id="1fb23-127">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fb23-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fb23-128">Requirements</span></span>



| <span data-ttu-id="1fb23-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fb23-129">Requirement</span></span> | <span data-ttu-id="1fb23-130">Value</span><span class="sxs-lookup"><span data-stu-id="1fb23-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb23-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1fb23-131">Header</span></span><br/>  | <dl> <span data-ttu-id="1fb23-132"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1fb23-132"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1fb23-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1fb23-133">Library</span></span><br/> | <dl> <span data-ttu-id="1fb23-134"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1fb23-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fb23-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fb23-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fb23-136">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="1fb23-136">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




