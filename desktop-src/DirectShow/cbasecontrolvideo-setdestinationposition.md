---
description: El método SetDestinationPosition establece el rectángulo de destino del vídeo.
ms.assetid: 397e90ea-7535-4cac-9f47-7a93737b1e3a
title: Método CBaseControlVideo. SetDestinationPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 798a65c44dd490587e3ad46fcae2c61a03986df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671807"
---
# <a name="cbasecontrolvideosetdestinationposition-method"></a><span data-ttu-id="98098-103">CBaseControlVideo. SetDestinationPosition, método</span><span class="sxs-lookup"><span data-stu-id="98098-103">CBaseControlVideo.SetDestinationPosition method</span></span>

<span data-ttu-id="98098-104">El `SetDestinationPosition` método establece el rectángulo de destino del vídeo.</span><span class="sxs-lookup"><span data-stu-id="98098-104">The `SetDestinationPosition` method sets the destination rectangle for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="98098-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98098-105">Syntax</span></span>


```C++
HRESULT SetDestinationPosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="98098-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98098-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98098-107">*Left*</span><span class="sxs-lookup"><span data-stu-id="98098-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="98098-108">Nueva coordenada izquierda.</span><span class="sxs-lookup"><span data-stu-id="98098-108">New left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="98098-109">*Top* (Principales)</span><span class="sxs-lookup"><span data-stu-id="98098-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="98098-110">Nueva coordenada superior.</span><span class="sxs-lookup"><span data-stu-id="98098-110">New top coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="98098-111">*Width*</span><span class="sxs-lookup"><span data-stu-id="98098-111">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="98098-112">Nuevo ancho.</span><span class="sxs-lookup"><span data-stu-id="98098-112">New width.</span></span>

</dd> <dt>

<span data-ttu-id="98098-113">*Height*</span><span class="sxs-lookup"><span data-stu-id="98098-113">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="98098-114">Nuevo alto.</span><span class="sxs-lookup"><span data-stu-id="98098-114">New height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98098-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98098-115">Return value</span></span>

<span data-ttu-id="98098-116">Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.</span><span class="sxs-lookup"><span data-stu-id="98098-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="98098-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="98098-117">Return code</span></span>                                                                                           | <span data-ttu-id="98098-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="98098-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="98098-119"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="98098-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="98098-120">Error.</span><span class="sxs-lookup"><span data-stu-id="98098-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="98098-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="98098-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="98098-122">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="98098-122">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="98098-123"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="98098-123"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="98098-124">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="98098-124">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="98098-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="98098-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="98098-126">Correcto.</span><span class="sxs-lookup"><span data-stu-id="98098-126">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="98098-127"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="98098-127"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="98098-128">No se puede realizar la operación porque los PIN no están conectados.</span><span class="sxs-lookup"><span data-stu-id="98098-128">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="98098-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98098-129">Remarks</span></span>

<span data-ttu-id="98098-130">Una aplicación puede cambiar los rectángulos de origen y de destino para el vídeo a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="98098-130">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="98098-131">El rectángulo de origen afecta a qué sección del origen de vídeo nativo aparecerá en la pantalla. el rectángulo de destino afecta al lugar en el que aparecerá el vídeo cuando se reproduzca.</span><span class="sxs-lookup"><span data-stu-id="98098-131">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="98098-132">El rectángulo de destino es relativo al área cliente de la ventana en la que se reproduce.</span><span class="sxs-lookup"><span data-stu-id="98098-132">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="98098-133">La esquina superior izquierda de la ventana es la coordenada (0,0).</span><span class="sxs-lookup"><span data-stu-id="98098-133">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="98098-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98098-134">Requirements</span></span>



| <span data-ttu-id="98098-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="98098-135">Requirement</span></span> | <span data-ttu-id="98098-136">Value</span><span class="sxs-lookup"><span data-stu-id="98098-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98098-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98098-137">Header</span></span><br/>  | <dl> <span data-ttu-id="98098-138"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98098-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="98098-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98098-139">Library</span></span><br/> | <dl> <span data-ttu-id="98098-140"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="98098-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98098-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="98098-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98098-142">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="98098-142">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




