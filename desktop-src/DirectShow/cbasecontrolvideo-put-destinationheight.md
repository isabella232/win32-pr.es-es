---
description: El \_ método put DestinationHeight establece el alto del rectángulo de destino.
ms.assetid: 2cb7af2b-69dc-4e86-b2cf-34223c9e5a1b
title: Método CBaseControlVideo.put_DestinationHeight (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_DestinationHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ceba632ad6b893c601b59b87f1e7da5fa53c69b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671778"
---
# <a name="cbasecontrolvideoput_destinationheight-method"></a><span data-ttu-id="b8d02-103">CBaseControlVideo. put \_ DestinationHeight (método)</span><span class="sxs-lookup"><span data-stu-id="b8d02-103">CBaseControlVideo.put\_DestinationHeight method</span></span>

<span data-ttu-id="b8d02-104">El `put_DestinationHeight` método establece el alto del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="b8d02-104">The `put_DestinationHeight` method sets the destination rectangle height.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8d02-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8d02-105">Syntax</span></span>


```C++
HRESULT put_DestinationHeight(
   long DestinationHeight
);
```



## <a name="parameters"></a><span data-ttu-id="b8d02-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8d02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8d02-107">*DestinationHeight*</span><span class="sxs-lookup"><span data-stu-id="b8d02-107">*DestinationHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="b8d02-108">Nuevo alto de destino.</span><span class="sxs-lookup"><span data-stu-id="b8d02-108">New destination height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8d02-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8d02-109">Return value</span></span>

<span data-ttu-id="b8d02-110">Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.</span><span class="sxs-lookup"><span data-stu-id="b8d02-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="b8d02-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b8d02-111">Return code</span></span>                                                                                           | <span data-ttu-id="b8d02-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8d02-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b8d02-113"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="b8d02-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="b8d02-114">Error.</span><span class="sxs-lookup"><span data-stu-id="b8d02-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="b8d02-115"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b8d02-115"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="b8d02-116">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="b8d02-116">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="b8d02-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="b8d02-117"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="b8d02-118">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="b8d02-118">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="b8d02-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="b8d02-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="b8d02-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="b8d02-120">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="b8d02-121"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="b8d02-121"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="b8d02-122">No se puede realizar la operación porque los PIN no están conectados.</span><span class="sxs-lookup"><span data-stu-id="b8d02-122">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b8d02-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8d02-123">Remarks</span></span>

<span data-ttu-id="b8d02-124">Una aplicación puede cambiar los rectángulos de origen y de destino para el vídeo a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="b8d02-124">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="b8d02-125">El rectángulo de origen afecta a qué sección del origen de vídeo nativo aparecerá en la pantalla. el rectángulo de destino afecta al lugar en el que aparecerá el vídeo cuando se reproduzca.</span><span class="sxs-lookup"><span data-stu-id="b8d02-125">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="b8d02-126">El rectángulo de destino es relativo al área cliente de la ventana en la que se reproduce.</span><span class="sxs-lookup"><span data-stu-id="b8d02-126">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="b8d02-127">La esquina superior izquierda de la ventana es la coordenada (0,0).</span><span class="sxs-lookup"><span data-stu-id="b8d02-127">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8d02-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8d02-128">Requirements</span></span>



| <span data-ttu-id="b8d02-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8d02-129">Requirement</span></span> | <span data-ttu-id="b8d02-130">Value</span><span class="sxs-lookup"><span data-stu-id="b8d02-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8d02-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8d02-131">Header</span></span><br/>  | <dl> <span data-ttu-id="b8d02-132"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8d02-132"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b8d02-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8d02-133">Library</span></span><br/> | <dl> <span data-ttu-id="b8d02-134"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b8d02-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8d02-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8d02-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8d02-136">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="b8d02-136">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




