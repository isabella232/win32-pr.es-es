---
description: El \_ método get SourceWidth recupera el ancho del rectángulo de origen actual.
ms.assetid: e8e27f8f-57e5-489c-aae7-86493677b380
title: Método CBaseControlVideo.get_SourceWidth (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60a78fe647ebf488a47907c058962f13790f2538
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660514"
---
# <a name="cbasecontrolvideoget_sourcewidth-method"></a><span data-ttu-id="787e6-103">CBaseControlVideo. Get \_ SourceWidth (método)</span><span class="sxs-lookup"><span data-stu-id="787e6-103">CBaseControlVideo.get\_SourceWidth method</span></span>

<span data-ttu-id="787e6-104">El `get_SourceWidth` método recupera el ancho del rectángulo de origen actual.</span><span class="sxs-lookup"><span data-stu-id="787e6-104">The `get_SourceWidth` method retrieves the width of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="787e6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="787e6-105">Syntax</span></span>


```C++
HRESULT get_SourceWidth(
   long *pSourceWidth
);
```



## <a name="parameters"></a><span data-ttu-id="787e6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="787e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="787e6-107">*pSourceWidth*</span><span class="sxs-lookup"><span data-stu-id="787e6-107">*pSourceWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="787e6-108">Puntero al ancho del rectángulo de origen actual.</span><span class="sxs-lookup"><span data-stu-id="787e6-108">Pointer to the width of the current source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="787e6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="787e6-109">Return value</span></span>

<span data-ttu-id="787e6-110">Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.</span><span class="sxs-lookup"><span data-stu-id="787e6-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="787e6-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="787e6-111">Return code</span></span>                                                                                           | <span data-ttu-id="787e6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="787e6-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="787e6-113"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="787e6-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="787e6-114">Error.</span><span class="sxs-lookup"><span data-stu-id="787e6-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="787e6-115"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="787e6-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="787e6-116">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="787e6-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="787e6-117"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="787e6-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="787e6-118">No se puede realizar la operación porque los PIN no están conectados.</span><span class="sxs-lookup"><span data-stu-id="787e6-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="787e6-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="787e6-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="787e6-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="787e6-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="787e6-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="787e6-121">Remarks</span></span>

<span data-ttu-id="787e6-122">Esta función miembro implementa el método [**IBasicVideo:: get \_ SourceWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcewidth) .</span><span class="sxs-lookup"><span data-stu-id="787e6-122">This member function implements the [**IBasicVideo::get\_SourceWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcewidth) method.</span></span>

<span data-ttu-id="787e6-123">Una aplicación puede cambiar los rectángulos de origen y de destino para el vídeo a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="787e6-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="787e6-124">El rectángulo de origen afecta a qué sección del origen de vídeo nativo aparecerá en la pantalla. el rectángulo de destino afecta al lugar en el que aparecerá el vídeo cuando se reproduzca.</span><span class="sxs-lookup"><span data-stu-id="787e6-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="787e6-125">El rectángulo de destino es relativo al área cliente de la ventana en la que se reproduce.</span><span class="sxs-lookup"><span data-stu-id="787e6-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="787e6-126">La esquina superior izquierda de la ventana es la coordenada (0,0).</span><span class="sxs-lookup"><span data-stu-id="787e6-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="787e6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="787e6-127">Requirements</span></span>



| <span data-ttu-id="787e6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="787e6-128">Requirement</span></span> | <span data-ttu-id="787e6-129">Value</span><span class="sxs-lookup"><span data-stu-id="787e6-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="787e6-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="787e6-130">Header</span></span><br/>  | <dl> <span data-ttu-id="787e6-131"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="787e6-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="787e6-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="787e6-132">Library</span></span><br/> | <dl> <span data-ttu-id="787e6-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="787e6-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="787e6-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="787e6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="787e6-135">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="787e6-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




