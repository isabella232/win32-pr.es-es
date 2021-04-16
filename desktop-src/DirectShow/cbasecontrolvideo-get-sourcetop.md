---
description: El \_ método get SourceTop recupera la coordenada superior del rectángulo de origen actual.
ms.assetid: 78dbd1e6-f591-487e-b9fe-fcbda55f5338
title: Método CBaseControlVideo.get_SourceTop (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceTop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1c2a2a90b441571a23bfa4210002b352e388a98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690343"
---
# <a name="cbasecontrolvideoget_sourcetop-method"></a><span data-ttu-id="d3494-103">CBaseControlVideo. Get \_ SourceTop (método)</span><span class="sxs-lookup"><span data-stu-id="d3494-103">CBaseControlVideo.get\_SourceTop method</span></span>

<span data-ttu-id="d3494-104">El `get_SourceTop` método recupera la coordenada superior del rectángulo de origen actual.</span><span class="sxs-lookup"><span data-stu-id="d3494-104">The `get_SourceTop` method retrieves the top coordinate of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3494-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3494-105">Syntax</span></span>


```C++
HRESULT get_SourceTop(
   long *pSourceTop
);
```



## <a name="parameters"></a><span data-ttu-id="d3494-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3494-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3494-107">*pSourceTop*</span><span class="sxs-lookup"><span data-stu-id="d3494-107">*pSourceTop*</span></span> 
</dt> <dd>

<span data-ttu-id="d3494-108">Puntero a la coordenada superior del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="d3494-108">Pointer to the top coordinate of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3494-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3494-109">Return value</span></span>

<span data-ttu-id="d3494-110">Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.</span><span class="sxs-lookup"><span data-stu-id="d3494-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="d3494-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d3494-111">Return code</span></span>                                                                                           | <span data-ttu-id="d3494-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3494-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d3494-113"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="d3494-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="d3494-114">Error.</span><span class="sxs-lookup"><span data-stu-id="d3494-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="d3494-115"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="d3494-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="d3494-116">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="d3494-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="d3494-117"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="d3494-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="d3494-118">No se puede realizar la operación porque los PIN no están conectados.</span><span class="sxs-lookup"><span data-stu-id="d3494-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="d3494-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="d3494-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="d3494-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="d3494-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="d3494-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3494-121">Remarks</span></span>

<span data-ttu-id="d3494-122">Esta función miembro implementa el método [**IBasicVideo:: get \_ SourceTop**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcetop) .</span><span class="sxs-lookup"><span data-stu-id="d3494-122">This member function implements the [**IBasicVideo::get\_SourceTop**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcetop) method.</span></span>

<span data-ttu-id="d3494-123">Una aplicación puede cambiar los rectángulos de origen y de destino para el vídeo a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="d3494-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="d3494-124">El rectángulo de origen afecta a qué sección del origen de vídeo nativo aparecerá en la pantalla. el rectángulo de destino afecta al lugar en el que aparecerá el vídeo cuando se reproduzca.</span><span class="sxs-lookup"><span data-stu-id="d3494-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="d3494-125">El rectángulo de destino es relativo al área cliente de la ventana en la que se reproduce.</span><span class="sxs-lookup"><span data-stu-id="d3494-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="d3494-126">La esquina superior izquierda de la ventana es la coordenada (0,0).</span><span class="sxs-lookup"><span data-stu-id="d3494-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3494-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3494-127">Requirements</span></span>



| <span data-ttu-id="d3494-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3494-128">Requirement</span></span> | <span data-ttu-id="d3494-129">Value</span><span class="sxs-lookup"><span data-stu-id="d3494-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3494-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3494-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d3494-131"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3494-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d3494-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d3494-132">Library</span></span><br/> | <dl> <span data-ttu-id="d3494-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d3494-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3494-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3494-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3494-135">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="d3494-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




