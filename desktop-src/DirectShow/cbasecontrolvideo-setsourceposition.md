---
description: El método SetSourcePosition establece una nueva posición de origen para el vídeo.
ms.assetid: e3c9ce31-9c24-4ef5-9526-ef6b890f5109
title: Método CBaseControlVideo. SetSourcePosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5493779b623108f713f8da252e8696140883395b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661304"
---
# <a name="cbasecontrolvideosetsourceposition-method"></a><span data-ttu-id="a0cb2-103">CBaseControlVideo. SetSourcePosition, método</span><span class="sxs-lookup"><span data-stu-id="a0cb2-103">CBaseControlVideo.SetSourcePosition method</span></span>

<span data-ttu-id="a0cb2-104">El `SetSourcePosition` método establece una nueva posición de origen para el vídeo.</span><span class="sxs-lookup"><span data-stu-id="a0cb2-104">The `SetSourcePosition` method sets a new source position for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0cb2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0cb2-105">Syntax</span></span>


```C++
HRESULT SetSourcePosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="a0cb2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a0cb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0cb2-107">*Left*</span><span class="sxs-lookup"><span data-stu-id="a0cb2-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="a0cb2-108">Nueva coordenada izquierda.</span><span class="sxs-lookup"><span data-stu-id="a0cb2-108">New left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="a0cb2-109">*Top* (Principales)</span><span class="sxs-lookup"><span data-stu-id="a0cb2-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="a0cb2-110">Nueva coordenada superior.</span><span class="sxs-lookup"><span data-stu-id="a0cb2-110">New top coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="a0cb2-111">*Width*</span><span class="sxs-lookup"><span data-stu-id="a0cb2-111">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="a0cb2-112">Nuevo ancho.</span><span class="sxs-lookup"><span data-stu-id="a0cb2-112">New width.</span></span>

</dd> <dt>

<span data-ttu-id="a0cb2-113">*Height*</span><span class="sxs-lookup"><span data-stu-id="a0cb2-113">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="a0cb2-114">Nuevo alto.</span><span class="sxs-lookup"><span data-stu-id="a0cb2-114">New height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0cb2-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0cb2-115">Return value</span></span>

<span data-ttu-id="a0cb2-116">Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.</span><span class="sxs-lookup"><span data-stu-id="a0cb2-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="a0cb2-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a0cb2-117">Return code</span></span>                                                                                           | <span data-ttu-id="a0cb2-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0cb2-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a0cb2-119"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="a0cb2-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="a0cb2-120">Error.</span><span class="sxs-lookup"><span data-stu-id="a0cb2-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="a0cb2-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a0cb2-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="a0cb2-122">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="a0cb2-122">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="a0cb2-123"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="a0cb2-123"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="a0cb2-124">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="a0cb2-124">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="a0cb2-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="a0cb2-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="a0cb2-126">Correcto.</span><span class="sxs-lookup"><span data-stu-id="a0cb2-126">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="a0cb2-127"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="a0cb2-127"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="a0cb2-128">No se puede realizar la operación porque los PIN no están conectados.</span><span class="sxs-lookup"><span data-stu-id="a0cb2-128">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a0cb2-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0cb2-129">Remarks</span></span>

<span data-ttu-id="a0cb2-130">Una aplicación puede cambiar los rectángulos de origen y de destino para el vídeo a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="a0cb2-130">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="a0cb2-131">El rectángulo de origen afecta a qué sección del origen de vídeo nativo aparecerá en la pantalla. el rectángulo de destino afecta al lugar en el que aparecerá el vídeo cuando se reproduzca.</span><span class="sxs-lookup"><span data-stu-id="a0cb2-131">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="a0cb2-132">El rectángulo de destino es relativo al área cliente de la ventana en la que se reproduce.</span><span class="sxs-lookup"><span data-stu-id="a0cb2-132">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="a0cb2-133">La esquina superior izquierda de la ventana es la coordenada (0,0).</span><span class="sxs-lookup"><span data-stu-id="a0cb2-133">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0cb2-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0cb2-134">Requirements</span></span>



| <span data-ttu-id="a0cb2-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0cb2-135">Requirement</span></span> | <span data-ttu-id="a0cb2-136">Value</span><span class="sxs-lookup"><span data-stu-id="a0cb2-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0cb2-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0cb2-137">Header</span></span><br/>  | <dl> <span data-ttu-id="a0cb2-138"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0cb2-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a0cb2-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a0cb2-139">Library</span></span><br/> | <dl> <span data-ttu-id="a0cb2-140"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a0cb2-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0cb2-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0cb2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0cb2-142">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="a0cb2-142">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




