---
description: El \_ método get AvgSyncOffset recupera el promedio del tiempo en milisegundos entre el momento en que se debió cada fotograma y el momento en que se representó realmente para todos los fotogramas desde que se inició el streaming.
ms.assetid: b41741e9-e0b5-4c49-93ef-cb8c0cf2ddeb
title: Método CBaseVideoRenderer.get_AvgSyncOffset (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35c682b8f4bb60ec629db5489e879d1ca7968b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679309"
---
# <a name="cbasevideorendererget_avgsyncoffset-method"></a><span data-ttu-id="b56b2-103">CBaseVideoRenderer. Get \_ AvgSyncOffset (método)</span><span class="sxs-lookup"><span data-stu-id="b56b2-103">CBaseVideoRenderer.get\_AvgSyncOffset method</span></span>

<span data-ttu-id="b56b2-104">El `get_AvgSyncOffset` método recupera el promedio del tiempo en milisegundos entre el momento en que se debió cada fotograma y el momento en que se representó realmente para todos los fotogramas desde que se inició el streaming.</span><span class="sxs-lookup"><span data-stu-id="b56b2-104">The `get_AvgSyncOffset` method retrieves the average of the time in milliseconds between when each frame was due and when it was actually rendered for all frames since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="b56b2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b56b2-105">Syntax</span></span>


```C++
HRESULT get_AvgSyncOffset(
   int *piAvg
);
```



## <a name="parameters"></a><span data-ttu-id="b56b2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b56b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b56b2-107">*piAvg*</span><span class="sxs-lookup"><span data-stu-id="b56b2-107">*piAvg*</span></span> 
</dt> <dd>

<span data-ttu-id="b56b2-108">Puntero al promedio del tiempo tal y como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b56b2-108">Pointer to the average of the time as previously described.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b56b2-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b56b2-109">Return value</span></span>

<span data-ttu-id="b56b2-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b56b2-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b56b2-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b56b2-111">Remarks</span></span>

<span data-ttu-id="b56b2-112">Esta función miembro implementa el método [**IQualProp:: get \_ AvgSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) .</span><span class="sxs-lookup"><span data-stu-id="b56b2-112">This member function implements the [**IQualProp::get\_AvgSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b56b2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b56b2-113">Requirements</span></span>



| <span data-ttu-id="b56b2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b56b2-114">Requirement</span></span> | <span data-ttu-id="b56b2-115">Value</span><span class="sxs-lookup"><span data-stu-id="b56b2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b56b2-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b56b2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b56b2-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b56b2-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b56b2-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b56b2-118">Library</span></span><br/> | <dl> <span data-ttu-id="b56b2-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b56b2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b56b2-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="b56b2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b56b2-121">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="b56b2-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




