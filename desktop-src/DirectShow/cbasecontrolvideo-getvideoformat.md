---
description: El método GetVideoFormat recupera un ejemplo de vídeo que representa el formato de vídeo actual.
ms.assetid: f7457c5b-037c-4a63-963e-0fc6086609a4
title: Método CBaseControlVideo. GetVideoFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d84b64818a02a60073fc21411e4a99bde07a6e00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661173"
---
# <a name="cbasecontrolvideogetvideoformat-method"></a><span data-ttu-id="a23e0-103">CBaseControlVideo. GetVideoFormat, método</span><span class="sxs-lookup"><span data-stu-id="a23e0-103">CBaseControlVideo.GetVideoFormat method</span></span>

<span data-ttu-id="a23e0-104">El `GetVideoFormat` método recupera un ejemplo de vídeo que representa el formato de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="a23e0-104">The `GetVideoFormat` method retrieves a video sample that represents the current video format.</span></span>

## <a name="syntax"></a><span data-ttu-id="a23e0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a23e0-105">Syntax</span></span>


```C++
virtual VIDEOINFOHEADER* GetVideoFormat() = 0;
```



## <a name="parameters"></a><span data-ttu-id="a23e0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a23e0-106">Parameters</span></span>

<span data-ttu-id="a23e0-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a23e0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a23e0-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a23e0-108">Return value</span></span>

<span data-ttu-id="a23e0-109">Devuelve un puntero a una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que contiene el formato de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="a23e0-109">Returns a pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure that contains the current video format.</span></span>

## <a name="remarks"></a><span data-ttu-id="a23e0-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a23e0-110">Remarks</span></span>

<span data-ttu-id="a23e0-111">Para devolver y comprobar cierta información a través de [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo), el objeto debe conocer el formato de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="a23e0-111">To return and check certain information through [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo), the object must know the current video format.</span></span> <span data-ttu-id="a23e0-112">Obtiene esta información llamando a este método virtual puro que las clases derivadas deben invalidar.</span><span class="sxs-lookup"><span data-stu-id="a23e0-112">It gets this information by calling this pure virtual method that derived classes must override.</span></span> <span data-ttu-id="a23e0-113">Las siguientes funciones miembro de [**CBaseControlVideo**](cbasecontrolvideo.md) llaman a esta función miembro.</span><span class="sxs-lookup"><span data-stu-id="a23e0-113">This member function is called by the following [**CBaseControlVideo**](cbasecontrolvideo.md) member functions.</span></span>

-   [<span data-ttu-id="a23e0-114">**CBaseControlVideo::OnVideoSizeChange**</span><span class="sxs-lookup"><span data-stu-id="a23e0-114">**CBaseControlVideo::OnVideoSizeChange**</span></span>](cbasecontrolvideo-onvideosizechange.md)
-   [<span data-ttu-id="a23e0-115">**CBaseControlVideo:: get \_ AvgTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="a23e0-115">**CBaseControlVideo::get\_AvgTimePerFrame**</span></span>](cbasecontrolvideo-get-avgtimeperframe.md)
-   [<span data-ttu-id="a23e0-116">**CBaseControlVideo:: get ( \_ velocidad de bits)**</span><span class="sxs-lookup"><span data-stu-id="a23e0-116">**CBaseControlVideo::get\_BitRate**</span></span>](cbasecontrolvideo-get-bitrate.md)
-   [<span data-ttu-id="a23e0-117">**CBaseControlVideo:: get \_ BitErrorRate**</span><span class="sxs-lookup"><span data-stu-id="a23e0-117">**CBaseControlVideo::get\_BitErrorRate**</span></span>](cbasecontrolvideo-get-biterrorrate.md)
-   [<span data-ttu-id="a23e0-118">**CBaseControlVideo:: get \_ VideoWidth**</span><span class="sxs-lookup"><span data-stu-id="a23e0-118">**CBaseControlVideo::get\_VideoWidth**</span></span>](cbasecontrolvideo-get-videowidth.md)
-   [<span data-ttu-id="a23e0-119">**CBaseControlVideo:: obtener \_ Videoaltura**</span><span class="sxs-lookup"><span data-stu-id="a23e0-119">**CBaseControlVideo::get\_VideoHeight**</span></span>](cbasecontrolvideo-get-videoheight.md)
-   [<span data-ttu-id="a23e0-120">**CBaseControlVideo::GetVideoPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="a23e0-120">**CBaseControlVideo::GetVideoPaletteEntries**</span></span>](cbasecontrolvideo-getvideopaletteentries.md)
-   [<span data-ttu-id="a23e0-121">**CBaseControlVideo::GetVideoSize**</span><span class="sxs-lookup"><span data-stu-id="a23e0-121">**CBaseControlVideo::GetVideoSize**</span></span>](cbasecontrolvideo-getvideosize.md)

## <a name="requirements"></a><span data-ttu-id="a23e0-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a23e0-122">Requirements</span></span>



| <span data-ttu-id="a23e0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a23e0-123">Requirement</span></span> | <span data-ttu-id="a23e0-124">Value</span><span class="sxs-lookup"><span data-stu-id="a23e0-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a23e0-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a23e0-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a23e0-126"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a23e0-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a23e0-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a23e0-127">Library</span></span><br/> | <dl> <span data-ttu-id="a23e0-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a23e0-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a23e0-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a23e0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a23e0-130">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="a23e0-130">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




