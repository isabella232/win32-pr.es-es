---
description: El \_ método get de velocidad de bits recupera una velocidad de bits aproximada para el vídeo.
ms.assetid: e12e4677-a038-479f-8b64-937ad521c4be
title: Método CBaseControlVideo.get_BitRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62f1feaed786b397801bbd17d2d2d41c0ccb813d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690347"
---
# <a name="cbasecontrolvideoget_bitrate-method"></a><span data-ttu-id="22b39-103">CBaseControlVideo. get ( \_ método de velocidad de bits)</span><span class="sxs-lookup"><span data-stu-id="22b39-103">CBaseControlVideo.get\_BitRate method</span></span>

<span data-ttu-id="22b39-104">El `get_BitRate` método recupera una velocidad de bits aproximada para el vídeo.</span><span class="sxs-lookup"><span data-stu-id="22b39-104">The `get_BitRate` method retrieves an approximate bit rate for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="22b39-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22b39-105">Syntax</span></span>


```C++
HRESULT get_BitRate(
   long *pBitRate
);
```



## <a name="parameters"></a><span data-ttu-id="22b39-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22b39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22b39-107">*pBitRate*</span><span class="sxs-lookup"><span data-stu-id="22b39-107">*pBitRate*</span></span> 
</dt> <dd>

<span data-ttu-id="22b39-108">Puntero a la velocidad de bits, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="22b39-108">Pointer to the bit rate, in bits per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22b39-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22b39-109">Return value</span></span>

<span data-ttu-id="22b39-110">Devuelve un ERROR Si se realiza correctamente o E \_ OUTOFMEMORY si no hay suficiente memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="22b39-110">Returns NOERROR if successful or E\_OUTOFMEMORY if not enough memory is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="22b39-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22b39-111">Remarks</span></span>

<span data-ttu-id="22b39-112">Esta función miembro implementa el método [**IBasicVideo:: get \_ bitrate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) .</span><span class="sxs-lookup"><span data-stu-id="22b39-112">This member function implements the [**IBasicVideo::get\_BitRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) method.</span></span> <span data-ttu-id="22b39-113">Llama al CBaseControlVideo virtual puro [**:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) para recuperar la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) de la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="22b39-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="22b39-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22b39-114">Requirements</span></span>



| <span data-ttu-id="22b39-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="22b39-115">Requirement</span></span> | <span data-ttu-id="22b39-116">Value</span><span class="sxs-lookup"><span data-stu-id="22b39-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22b39-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22b39-117">Header</span></span><br/>  | <dl> <span data-ttu-id="22b39-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22b39-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="22b39-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="22b39-119">Library</span></span><br/> | <dl> <span data-ttu-id="22b39-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="22b39-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22b39-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="22b39-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22b39-122">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="22b39-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




