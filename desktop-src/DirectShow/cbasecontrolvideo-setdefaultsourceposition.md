---
description: El método SetDefaultSourcePosition establece el representador de nuevo en con la posición de origen predeterminada (normalmente, todo el vídeo nativo).
ms.assetid: 1ac03298-4c25-45f7-9719-ea03fe4699b2
title: Método CBaseControlVideo. SetDefaultSourcePosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e6296683235a3cf051d0b9f4ee56ce51a3516f66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660387"
---
# <a name="cbasecontrolvideosetdefaultsourceposition-method"></a><span data-ttu-id="1768c-103">CBaseControlVideo. SetDefaultSourcePosition, método</span><span class="sxs-lookup"><span data-stu-id="1768c-103">CBaseControlVideo.SetDefaultSourcePosition method</span></span>

<span data-ttu-id="1768c-104">El `SetDefaultSourcePosition` método establece el representador de nuevo en con la posición de origen predeterminada (normalmente, todo el vídeo nativo).</span><span class="sxs-lookup"><span data-stu-id="1768c-104">The `SetDefaultSourcePosition` method sets the renderer back to using the default source position (typically all the native video).</span></span>

## <a name="syntax"></a><span data-ttu-id="1768c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1768c-105">Syntax</span></span>


```C++
HRESULT SetDefaultSourcePosition();
```



## <a name="parameters"></a><span data-ttu-id="1768c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1768c-106">Parameters</span></span>

<span data-ttu-id="1768c-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1768c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1768c-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1768c-108">Return value</span></span>

<span data-ttu-id="1768c-109">Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.</span><span class="sxs-lookup"><span data-stu-id="1768c-109">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="1768c-110">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1768c-110">Return code</span></span>                                                                                           | <span data-ttu-id="1768c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="1768c-111">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1768c-112"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="1768c-112"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="1768c-113">Error.</span><span class="sxs-lookup"><span data-stu-id="1768c-113">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="1768c-114"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="1768c-114"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="1768c-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="1768c-115">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="1768c-116"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="1768c-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="1768c-117">No se puede realizar la operación porque los PIN no están conectados.</span><span class="sxs-lookup"><span data-stu-id="1768c-117">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1768c-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1768c-118">Remarks</span></span>

<span data-ttu-id="1768c-119">Una aplicación puede cambiar los rectángulos de origen y de destino para el vídeo a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="1768c-119">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="1768c-120">El rectángulo de origen afecta a qué sección del origen de vídeo nativo aparecerá en la pantalla. el rectángulo de destino afecta al lugar en el que aparecerá el vídeo cuando se reproduzca.</span><span class="sxs-lookup"><span data-stu-id="1768c-120">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="1768c-121">El rectángulo de destino es relativo al área cliente de la ventana en la que se reproduce.</span><span class="sxs-lookup"><span data-stu-id="1768c-121">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="1768c-122">La esquina superior izquierda de la ventana es la coordenada (0,0).</span><span class="sxs-lookup"><span data-stu-id="1768c-122">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="1768c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1768c-123">Requirements</span></span>



| <span data-ttu-id="1768c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1768c-124">Requirement</span></span> | <span data-ttu-id="1768c-125">Value</span><span class="sxs-lookup"><span data-stu-id="1768c-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1768c-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1768c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1768c-127"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1768c-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1768c-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1768c-128">Library</span></span><br/> | <dl> <span data-ttu-id="1768c-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1768c-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1768c-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="1768c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1768c-131">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="1768c-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




