---
description: El \_ método get SourceHeight recupera el alto del rectángulo de origen actual.
ms.assetid: bf727cf6-9143-41f0-a482-782a4178ea92
title: Método CBaseControlVideo.get_SourceHeight (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b724f63907c8372867095b059ff728b4c646df21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660517"
---
# <a name="cbasecontrolvideoget_sourceheight-method"></a><span data-ttu-id="5cfb9-103">CBaseControlVideo. Get \_ SourceHeight (método)</span><span class="sxs-lookup"><span data-stu-id="5cfb9-103">CBaseControlVideo.get\_SourceHeight method</span></span>

<span data-ttu-id="5cfb9-104">El `get_SourceHeight` método recupera el alto del rectángulo de origen actual.</span><span class="sxs-lookup"><span data-stu-id="5cfb9-104">The `get_SourceHeight` method retrieves the height of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cfb9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5cfb9-105">Syntax</span></span>


```C++
HRESULT get_SourceHeight(
   long *pSourceHeight
);
```



## <a name="parameters"></a><span data-ttu-id="5cfb9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5cfb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cfb9-107">*pSourceHeight*</span><span class="sxs-lookup"><span data-stu-id="5cfb9-107">*pSourceHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="5cfb9-108">Puntero al alto del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="5cfb9-108">Pointer to the height of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cfb9-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5cfb9-109">Return value</span></span>

<span data-ttu-id="5cfb9-110">Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.</span><span class="sxs-lookup"><span data-stu-id="5cfb9-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="5cfb9-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5cfb9-111">Return code</span></span>                                                                                           | <span data-ttu-id="5cfb9-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5cfb9-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5cfb9-113"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="5cfb9-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="5cfb9-114">Error.</span><span class="sxs-lookup"><span data-stu-id="5cfb9-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="5cfb9-115"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="5cfb9-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="5cfb9-116">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="5cfb9-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="5cfb9-117"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="5cfb9-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="5cfb9-118">No se puede realizar la operación porque los PIN no están conectados.</span><span class="sxs-lookup"><span data-stu-id="5cfb9-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="5cfb9-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="5cfb9-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="5cfb9-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="5cfb9-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="5cfb9-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5cfb9-121">Remarks</span></span>

<span data-ttu-id="5cfb9-122">Esta función miembro implementa el método [**IBasicVideo:: get \_ SourceHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourceheight) .</span><span class="sxs-lookup"><span data-stu-id="5cfb9-122">This member function implements the [**IBasicVideo::get\_SourceHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourceheight) method.</span></span>

<span data-ttu-id="5cfb9-123">Una aplicación puede cambiar los rectángulos de origen y de destino para el vídeo a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="5cfb9-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="5cfb9-124">El rectángulo de origen afecta a qué sección del origen de vídeo nativo aparecerá en la pantalla. el rectángulo de destino afecta al lugar en el que aparecerá el vídeo cuando se reproduzca.</span><span class="sxs-lookup"><span data-stu-id="5cfb9-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="5cfb9-125">El rectángulo de destino es relativo al área cliente de la ventana en la que se reproduce.</span><span class="sxs-lookup"><span data-stu-id="5cfb9-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="5cfb9-126">La esquina superior izquierda de la ventana es la coordenada (0,0).</span><span class="sxs-lookup"><span data-stu-id="5cfb9-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="5cfb9-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cfb9-127">Requirements</span></span>



| <span data-ttu-id="5cfb9-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cfb9-128">Requirement</span></span> | <span data-ttu-id="5cfb9-129">Value</span><span class="sxs-lookup"><span data-stu-id="5cfb9-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cfb9-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5cfb9-130">Header</span></span><br/>  | <dl> <span data-ttu-id="5cfb9-131"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5cfb9-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5cfb9-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5cfb9-132">Library</span></span><br/> | <dl> <span data-ttu-id="5cfb9-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5cfb9-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cfb9-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="5cfb9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cfb9-135">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="5cfb9-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




