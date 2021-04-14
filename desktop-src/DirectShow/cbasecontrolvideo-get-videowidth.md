---
description: El \_ método get VideoWidth recupera el ancho del vídeo nativo.
ms.assetid: dfd897f0-f580-44c0-9445-ba61ae267187
title: Método CBaseControlVideo.get_VideoWidth (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: faeeed7ea8af58103e74d9b8c3690523c893282f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661408"
---
# <a name="cbasecontrolvideoget_videowidth-method"></a><span data-ttu-id="116f6-103">CBaseControlVideo. Get- \_ width (método)</span><span class="sxs-lookup"><span data-stu-id="116f6-103">CBaseControlVideo.get\_VideoWidth method</span></span>

<span data-ttu-id="116f6-104">El `get_VideoWidth` método recupera el ancho del vídeo nativo.</span><span class="sxs-lookup"><span data-stu-id="116f6-104">The `get_VideoWidth` method retrieves the width of the native video.</span></span>

## <a name="syntax"></a><span data-ttu-id="116f6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="116f6-105">Syntax</span></span>


```C++
HRESULT get_VideoWidth(
   long *pVideoWidth
);
```



## <a name="parameters"></a><span data-ttu-id="116f6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="116f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="116f6-107">*pVideoWidth*</span><span class="sxs-lookup"><span data-stu-id="116f6-107">*pVideoWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="116f6-108">Puntero al ancho del vídeo nativo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="116f6-108">Pointer to the width of the native video, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="116f6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="116f6-109">Return value</span></span>

<span data-ttu-id="116f6-110">Devuelve un ERROR Si se realiza correctamente o E \_ OUTOFMEMORY si no hay suficiente memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="116f6-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="116f6-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="116f6-111">Remarks</span></span>

<span data-ttu-id="116f6-112">Esta función miembro implementa el método [**IBasicVideo:: get \_ VideoWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videowidth) .</span><span class="sxs-lookup"><span data-stu-id="116f6-112">This member function implements the [**IBasicVideo::get\_VideoWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videowidth) method.</span></span> <span data-ttu-id="116f6-113">Llama al CBaseControlVideo virtual puro [**:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) para recuperar la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) de la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="116f6-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="116f6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="116f6-114">Requirements</span></span>



| <span data-ttu-id="116f6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="116f6-115">Requirement</span></span> | <span data-ttu-id="116f6-116">Value</span><span class="sxs-lookup"><span data-stu-id="116f6-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="116f6-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="116f6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="116f6-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="116f6-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="116f6-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="116f6-119">Library</span></span><br/> | <dl> <span data-ttu-id="116f6-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="116f6-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="116f6-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="116f6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="116f6-122">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="116f6-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




