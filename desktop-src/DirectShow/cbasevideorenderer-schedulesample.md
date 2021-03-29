---
description: El método ScheduleSample invalida la clase base que realiza el trabajo principal para mantener un recuento de muestras dibujadas y quitadas (que usa la implementación de IQualProp).
ms.assetid: 66e4e318-a7ff-4ba0-9ac5-24ba39ac86f1
title: Método CBaseVideoRenderer. ScheduleSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62827f1cda9423f9a5128c35289803027bfa78a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679095"
---
# <a name="cbasevideorendererschedulesample-method"></a><span data-ttu-id="1dfe4-103">CBaseVideoRenderer. ScheduleSample, método</span><span class="sxs-lookup"><span data-stu-id="1dfe4-103">CBaseVideoRenderer.ScheduleSample method</span></span>

<span data-ttu-id="1dfe4-104">El `ScheduleSample` método invalida la clase base que realiza el trabajo principal para mantener un recuento de muestras dibujadas y quitadas (utilizadas por la implementación de [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) ).</span><span class="sxs-lookup"><span data-stu-id="1dfe4-104">The `ScheduleSample` method overrides the base class that does the main work to keep a count of samples drawn and dropped (which are used by the [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) implementation).</span></span>

## <a name="syntax"></a><span data-ttu-id="1dfe4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1dfe4-105">Syntax</span></span>


```C++
BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="1dfe4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1dfe4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dfe4-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="1dfe4-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="1dfe4-108">Puntero al ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="1dfe4-108">Pointer to the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dfe4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1dfe4-109">Return value</span></span>

<span data-ttu-id="1dfe4-110">Devuelve **true** si el ejemplo está programado; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="1dfe4-110">Returns **TRUE** if the sample is scheduled; otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dfe4-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dfe4-111">Requirements</span></span>



| <span data-ttu-id="1dfe4-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dfe4-112">Requirement</span></span> | <span data-ttu-id="1dfe4-113">Value</span><span class="sxs-lookup"><span data-stu-id="1dfe4-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dfe4-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1dfe4-114">Header</span></span><br/>  | <dl> <span data-ttu-id="1dfe4-115"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1dfe4-115"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1dfe4-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1dfe4-116">Library</span></span><br/> | <dl> <span data-ttu-id="1dfe4-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1dfe4-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dfe4-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="1dfe4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dfe4-119">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="1dfe4-119">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




