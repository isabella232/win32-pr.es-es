---
description: El \_ método get AvgTimePerFrame recupera el tiempo medio por fotograma.
ms.assetid: bcfdb241-9ec1-49f4-b2b5-0869c27da953
title: Método CBaseControlVideo.get_AvgTimePerFrame (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_AvgTimePerFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae69140348be6e2fdfc120ee7fb40096d663f720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690349"
---
# <a name="cbasecontrolvideoget_avgtimeperframe-method"></a><span data-ttu-id="3bd79-103">CBaseControlVideo. Get \_ AvgTimePerFrame (método)</span><span class="sxs-lookup"><span data-stu-id="3bd79-103">CBaseControlVideo.get\_AvgTimePerFrame method</span></span>

<span data-ttu-id="3bd79-104">El `get_AvgTimePerFrame` método recupera el tiempo medio por fotograma.</span><span class="sxs-lookup"><span data-stu-id="3bd79-104">The `get_AvgTimePerFrame` method retrieves the average time per frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bd79-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3bd79-105">Syntax</span></span>


```C++
HRESULT get_AvgTimePerFrame(
   REFTIME *pAvgTimePerFrame
);
```



## <a name="parameters"></a><span data-ttu-id="3bd79-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3bd79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bd79-107">*pAvgTimePerFrame*</span><span class="sxs-lookup"><span data-stu-id="3bd79-107">*pAvgTimePerFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="3bd79-108">Puntero al promedio de tiempo por fotograma.</span><span class="sxs-lookup"><span data-stu-id="3bd79-108">Pointer to the average time per frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bd79-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3bd79-109">Return value</span></span>

<span data-ttu-id="3bd79-110">Devuelve un ERROR Si se realiza correctamente o E \_ OUTOFMEMORY si no hay suficiente memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="3bd79-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bd79-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3bd79-111">Remarks</span></span>

<span data-ttu-id="3bd79-112">Esta función miembro implementa el método [**IBasicVideo:: get \_ AvgTimePerFrame**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) .</span><span class="sxs-lookup"><span data-stu-id="3bd79-112">This member function implements the [**IBasicVideo::get\_AvgTimePerFrame**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) method.</span></span> <span data-ttu-id="3bd79-113">Llama a la función miembro virtual [**CBaseControlVideo:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) pura para recuperar la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) de la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="3bd79-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) member function to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bd79-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bd79-114">Requirements</span></span>



| <span data-ttu-id="3bd79-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bd79-115">Requirement</span></span> | <span data-ttu-id="3bd79-116">Value</span><span class="sxs-lookup"><span data-stu-id="3bd79-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bd79-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3bd79-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3bd79-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3bd79-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3bd79-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3bd79-119">Library</span></span><br/> | <dl> <span data-ttu-id="3bd79-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3bd79-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bd79-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="3bd79-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bd79-122">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="3bd79-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




