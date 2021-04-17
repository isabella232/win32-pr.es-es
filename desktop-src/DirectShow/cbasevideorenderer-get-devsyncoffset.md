---
description: El \_ método get DevSyncOffset recupera la desviación estándar del tiempo en milisegundos entre el momento en que se debió cada fotograma y el momento en que se representó en realidad, para todos los fotogramas desde que se inició el streaming.
ms.assetid: 86f60064-f913-4377-bad0-148a213171fc
title: Método CBaseVideoRenderer.get_DevSyncOffset (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_DevSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9926e809901f7290738e2e2cf3d094e54e068580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660382"
---
# <a name="cbasevideorendererget_devsyncoffset-method"></a><span data-ttu-id="c32c1-103">CBaseVideoRenderer. Get \_ DevSyncOffset (método)</span><span class="sxs-lookup"><span data-stu-id="c32c1-103">CBaseVideoRenderer.get\_DevSyncOffset method</span></span>

<span data-ttu-id="c32c1-104">El `get_DevSyncOffset` método recupera la desviación estándar del tiempo en milisegundos entre el momento en que se debió cada fotograma y el momento en que se representó en realidad, para todos los fotogramas desde que se inició el streaming.</span><span class="sxs-lookup"><span data-stu-id="c32c1-104">The `get_DevSyncOffset` method retrieves the standard deviation of the time in milliseconds between when each frame was due and when it was actually rendered, for all frames since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="c32c1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c32c1-105">Syntax</span></span>


```C++
HRESULT get_DevSyncOffset(
   int *piDev
);
```



## <a name="parameters"></a><span data-ttu-id="c32c1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c32c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c32c1-107">*piDev*</span><span class="sxs-lookup"><span data-stu-id="c32c1-107">*piDev*</span></span> 
</dt> <dd>

<span data-ttu-id="c32c1-108">Puntero a la desviación estándar de la hora que se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c32c1-108">Pointer to the standard deviation of the time as previously described.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c32c1-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c32c1-109">Return value</span></span>

<span data-ttu-id="c32c1-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c32c1-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c32c1-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c32c1-111">Remarks</span></span>

<span data-ttu-id="c32c1-112">Esta función miembro implementa el método [**IQualProp:: get \_ DevSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset) .</span><span class="sxs-lookup"><span data-stu-id="c32c1-112">This member function implements the [**IQualProp::get\_DevSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c32c1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c32c1-113">Requirements</span></span>



| <span data-ttu-id="c32c1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c32c1-114">Requirement</span></span> | <span data-ttu-id="c32c1-115">Value</span><span class="sxs-lookup"><span data-stu-id="c32c1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c32c1-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c32c1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c32c1-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c32c1-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c32c1-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c32c1-118">Library</span></span><br/> | <dl> <span data-ttu-id="c32c1-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c32c1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c32c1-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="c32c1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c32c1-121">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="c32c1-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




