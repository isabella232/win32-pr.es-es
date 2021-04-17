---
description: El \_ método put SourceWidth establece el ancho del rectángulo de origen.
ms.assetid: 0becea4f-e47e-4f64-ab95-0ee333ad48f3
title: Método CBaseControlVideo.put_SourceWidth (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_SourceWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1576389a90db71ee6d371f6e68c44ea39117c05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670548"
---
# <a name="cbasecontrolvideoput_sourcewidth-method"></a><span data-ttu-id="ef527-103">CBaseControlVideo. put \_ SourceWidth (método)</span><span class="sxs-lookup"><span data-stu-id="ef527-103">CBaseControlVideo.put\_SourceWidth method</span></span>

<span data-ttu-id="ef527-104">El `put_SourceWidth` método establece el ancho del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="ef527-104">The `put_SourceWidth` method sets the width of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef527-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef527-105">Syntax</span></span>


```C++
HRESULT put_SourceWidth(
   long SourceWidth
);
```



## <a name="parameters"></a><span data-ttu-id="ef527-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef527-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef527-107">*SourceWidth*</span><span class="sxs-lookup"><span data-stu-id="ef527-107">*SourceWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="ef527-108">Nuevo ancho del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="ef527-108">New width of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef527-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef527-109">Return value</span></span>

<span data-ttu-id="ef527-110">Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.</span><span class="sxs-lookup"><span data-stu-id="ef527-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="ef527-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ef527-111">Return code</span></span>                                                                                           | <span data-ttu-id="ef527-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef527-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef527-113"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="ef527-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="ef527-114">Error.</span><span class="sxs-lookup"><span data-stu-id="ef527-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="ef527-115"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ef527-115"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="ef527-116">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="ef527-116">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="ef527-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="ef527-117"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="ef527-118">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="ef527-118">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="ef527-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="ef527-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="ef527-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="ef527-120">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="ef527-121"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="ef527-121"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="ef527-122">No se puede realizar la operación porque los PIN no están conectados.</span><span class="sxs-lookup"><span data-stu-id="ef527-122">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ef527-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef527-123">Remarks</span></span>

<span data-ttu-id="ef527-124">Una aplicación puede cambiar los rectángulos de origen y de destino para el vídeo a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="ef527-124">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="ef527-125">El rectángulo de origen afecta a qué sección del origen de vídeo nativo aparecerá en la pantalla. el rectángulo de destino afecta al lugar en el que aparecerá el vídeo cuando se reproduzca.</span><span class="sxs-lookup"><span data-stu-id="ef527-125">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="ef527-126">El rectángulo de destino es relativo al área cliente de la ventana en la que se reproduce.</span><span class="sxs-lookup"><span data-stu-id="ef527-126">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="ef527-127">La esquina superior izquierda de la ventana es la coordenada (0,0).</span><span class="sxs-lookup"><span data-stu-id="ef527-127">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef527-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef527-128">Requirements</span></span>



| <span data-ttu-id="ef527-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef527-129">Requirement</span></span> | <span data-ttu-id="ef527-130">Value</span><span class="sxs-lookup"><span data-stu-id="ef527-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef527-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef527-131">Header</span></span><br/>  | <dl> <span data-ttu-id="ef527-132"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef527-132"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ef527-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ef527-133">Library</span></span><br/> | <dl> <span data-ttu-id="ef527-134"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ef527-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef527-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef527-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef527-136">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="ef527-136">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




