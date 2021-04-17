---
description: El \_ método get VideoHeight recupera el alto del vídeo nativo.
ms.assetid: f33ba789-f9c6-47f1-879b-241bfdc72010
title: Método CBaseControlVideo.get_VideoHeight (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e738636cecd8031962ae31ebf54ac258d868013
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690342"
---
# <a name="cbasecontrolvideoget_videoheight-method"></a><span data-ttu-id="8e9cd-103">CBaseControlVideo. Get \_ VideoHeight (método)</span><span class="sxs-lookup"><span data-stu-id="8e9cd-103">CBaseControlVideo.get\_VideoHeight method</span></span>

<span data-ttu-id="8e9cd-104">El `get_VideoHeight` método recupera el alto del vídeo nativo.</span><span class="sxs-lookup"><span data-stu-id="8e9cd-104">The `get_VideoHeight` method retrieves the height of the native video.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e9cd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e9cd-105">Syntax</span></span>


```C++
HRESULT get_VideoHeight(
   long *pVideoHeight
);
```



## <a name="parameters"></a><span data-ttu-id="8e9cd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e9cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e9cd-107">*pVideoHeight*</span><span class="sxs-lookup"><span data-stu-id="8e9cd-107">*pVideoHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="8e9cd-108">Puntero al alto del vídeo nativo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="8e9cd-108">Pointer to the height of the native video, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e9cd-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e9cd-109">Return value</span></span>

<span data-ttu-id="8e9cd-110">Devuelve un ERROR Si se realiza correctamente o E \_ OUTOFMEMORY si no hay suficiente memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="8e9cd-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e9cd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e9cd-111">Remarks</span></span>

<span data-ttu-id="8e9cd-112">Esta función miembro implementa el método [**IBasicVideo:: get \_ VideoHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) .</span><span class="sxs-lookup"><span data-stu-id="8e9cd-112">This member function implements the [**IBasicVideo::get\_VideoHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) method.</span></span> <span data-ttu-id="8e9cd-113">Llama al CBaseControlVideo virtual puro [**:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) para recuperar la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) de la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="8e9cd-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e9cd-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e9cd-114">Requirements</span></span>



| <span data-ttu-id="8e9cd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e9cd-115">Requirement</span></span> | <span data-ttu-id="8e9cd-116">Value</span><span class="sxs-lookup"><span data-stu-id="8e9cd-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e9cd-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e9cd-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8e9cd-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e9cd-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8e9cd-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8e9cd-119">Library</span></span><br/> | <dl> <span data-ttu-id="8e9cd-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8e9cd-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e9cd-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e9cd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e9cd-122">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="8e9cd-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




