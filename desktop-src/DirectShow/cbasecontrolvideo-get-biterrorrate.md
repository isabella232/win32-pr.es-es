---
description: El \_ método get BitErrorRate recupera una tasa de errores de bits aproximada para el vídeo.
ms.assetid: 4078611c-6e09-47c8-8e1c-f33bc6ddca79
title: Método CBaseControlVideo.get_BitErrorRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitErrorRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ae15a882f6dcd8840519f9067223dde3e925f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660527"
---
# <a name="cbasecontrolvideoget_biterrorrate-method"></a><span data-ttu-id="48628-103">CBaseControlVideo. Get \_ BitErrorRate (método)</span><span class="sxs-lookup"><span data-stu-id="48628-103">CBaseControlVideo.get\_BitErrorRate method</span></span>

<span data-ttu-id="48628-104">El `get_BitErrorRate` método recupera una tasa de errores de bits aproximada para el vídeo.</span><span class="sxs-lookup"><span data-stu-id="48628-104">The `get_BitErrorRate` method retrieves an approximate bit error rate for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="48628-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48628-105">Syntax</span></span>


```C++
HRESULT get_BitErrorRate(
   long *pBitErrorRate
);
```



## <a name="parameters"></a><span data-ttu-id="48628-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48628-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48628-107">*pBitErrorRate*</span><span class="sxs-lookup"><span data-stu-id="48628-107">*pBitErrorRate*</span></span> 
</dt> <dd>

<span data-ttu-id="48628-108">Puntero a la tasa de errores de bits (un error para aproximadamente este número de bits).</span><span class="sxs-lookup"><span data-stu-id="48628-108">Pointer to the bit error rate (one error for approximately this many bits).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48628-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48628-109">Return value</span></span>

<span data-ttu-id="48628-110">Devuelve un ERROR Si se realiza correctamente o E \_ OUTOFMEMORY si no hay suficiente memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="48628-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="48628-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48628-111">Remarks</span></span>

<span data-ttu-id="48628-112">Esta función miembro implementa el método [**IBasicVideo:: get \_ BitErrorRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) .</span><span class="sxs-lookup"><span data-stu-id="48628-112">This member function implements the [**IBasicVideo::get\_BitErrorRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) method.</span></span> <span data-ttu-id="48628-113">Llama al método [**CBaseControlVideo:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) puro virtual para recuperar la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) de la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="48628-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) method to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="48628-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48628-114">Requirements</span></span>



| <span data-ttu-id="48628-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="48628-115">Requirement</span></span> | <span data-ttu-id="48628-116">Value</span><span class="sxs-lookup"><span data-stu-id="48628-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48628-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48628-117">Header</span></span><br/>  | <dl> <span data-ttu-id="48628-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48628-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="48628-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="48628-119">Library</span></span><br/> | <dl> <span data-ttu-id="48628-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="48628-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48628-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="48628-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48628-122">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="48628-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




