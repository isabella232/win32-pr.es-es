---
description: El \_ método put DestinationTop establece la coordenada superior del rectángulo de destino.
ms.assetid: d18996ac-85f2-4778-b0aa-1bc0c4d5f7d9
title: Método CBaseControlVideo.put_DestinationTop (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_DestinationTop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c89e4693d424412a43869509e046a5023e76341c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660811"
---
# <a name="cbasecontrolvideoput_destinationtop-method"></a><span data-ttu-id="c1938-103">CBaseControlVideo. put \_ DestinationTop (método)</span><span class="sxs-lookup"><span data-stu-id="c1938-103">CBaseControlVideo.put\_DestinationTop method</span></span>

<span data-ttu-id="c1938-104">El `put_DestinationTop` método establece la coordenada superior del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="c1938-104">The `put_DestinationTop` method sets the top coordinate of the destination rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1938-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1938-105">Syntax</span></span>


```C++
HRESULT put_DestinationTop(
   long DestinationTop
);
```



## <a name="parameters"></a><span data-ttu-id="c1938-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1938-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1938-107">*DestinationTop*</span><span class="sxs-lookup"><span data-stu-id="c1938-107">*DestinationTop*</span></span> 
</dt> <dd>

<span data-ttu-id="c1938-108">Nueva coordenada superior del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="c1938-108">New top coordinate of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1938-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1938-109">Return value</span></span>

<span data-ttu-id="c1938-110">Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.</span><span class="sxs-lookup"><span data-stu-id="c1938-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="c1938-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c1938-111">Return code</span></span>                                                                                           | <span data-ttu-id="c1938-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1938-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c1938-113"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="c1938-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="c1938-114">Error.</span><span class="sxs-lookup"><span data-stu-id="c1938-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="c1938-115"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c1938-115"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="c1938-116">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="c1938-116">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="c1938-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="c1938-117"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="c1938-118">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="c1938-118">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="c1938-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="c1938-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="c1938-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="c1938-120">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="c1938-121"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="c1938-121"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="c1938-122">No se puede realizar la operación porque los PIN no están conectados.</span><span class="sxs-lookup"><span data-stu-id="c1938-122">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c1938-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1938-123">Remarks</span></span>

<span data-ttu-id="c1938-124">Una aplicación puede cambiar los rectángulos de origen y de destino para el vídeo a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="c1938-124">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="c1938-125">El rectángulo de origen afecta a qué sección del origen de vídeo nativo aparecerá en la pantalla. el rectángulo de destino afecta al lugar en el que aparecerá el vídeo cuando se reproduzca.</span><span class="sxs-lookup"><span data-stu-id="c1938-125">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="c1938-126">El rectángulo de destino es relativo al área cliente de la ventana en la que se reproduce.</span><span class="sxs-lookup"><span data-stu-id="c1938-126">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="c1938-127">La esquina superior izquierda de la ventana es la coordenada (0,0).</span><span class="sxs-lookup"><span data-stu-id="c1938-127">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1938-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1938-128">Requirements</span></span>



| <span data-ttu-id="c1938-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1938-129">Requirement</span></span> | <span data-ttu-id="c1938-130">Value</span><span class="sxs-lookup"><span data-stu-id="c1938-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1938-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c1938-131">Header</span></span><br/>  | <dl> <span data-ttu-id="c1938-132"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1938-132"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c1938-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c1938-133">Library</span></span><br/> | <dl> <span data-ttu-id="c1938-134"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c1938-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1938-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1938-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1938-136">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="c1938-136">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




