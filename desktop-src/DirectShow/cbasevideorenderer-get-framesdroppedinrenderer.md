---
description: El \_ método get FramesDroppedInRenderer recupera el número de fotogramas quitados por el representador.
ms.assetid: d890f285-b3bb-426c-80f6-e273cf0cccbb
title: Método CBaseVideoRenderer.get_FramesDroppedInRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDroppedInRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef81678fce8d349c7c047b0453cc480d8673f8f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660380"
---
# <a name="cbasevideorendererget_framesdroppedinrenderer-method"></a><span data-ttu-id="1964f-103">CBaseVideoRenderer. Get \_ FramesDroppedInRenderer (método)</span><span class="sxs-lookup"><span data-stu-id="1964f-103">CBaseVideoRenderer.get\_FramesDroppedInRenderer method</span></span>

<span data-ttu-id="1964f-104">El `get_FramesDroppedInRenderer` método recupera el número de fotogramas quitados por el representador.</span><span class="sxs-lookup"><span data-stu-id="1964f-104">The `get_FramesDroppedInRenderer` method retrieves the number of frames dropped by the renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="1964f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1964f-105">Syntax</span></span>


```C++
HRESULT get_FramesDroppedInRenderer(
   int *pcFramesDropped
);
```



## <a name="parameters"></a><span data-ttu-id="1964f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1964f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1964f-107">*pcFramesDropped*</span><span class="sxs-lookup"><span data-stu-id="1964f-107">*pcFramesDropped*</span></span> 
</dt> <dd>

<span data-ttu-id="1964f-108">Puntero al número de fotogramas quitados.</span><span class="sxs-lookup"><span data-stu-id="1964f-108">Pointer to the number of frames dropped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1964f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1964f-109">Return value</span></span>

<span data-ttu-id="1964f-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1964f-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1964f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1964f-111">Remarks</span></span>

<span data-ttu-id="1964f-112">Esta función miembro implementa el método [**IQualProp:: get \_ FramesDroppedInRenderer**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) .</span><span class="sxs-lookup"><span data-stu-id="1964f-112">This member function implements the [**IQualProp::get\_FramesDroppedInRenderer**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) method.</span></span> <span data-ttu-id="1964f-113">Así es como la página de propiedades recupera los datos del programador.</span><span class="sxs-lookup"><span data-stu-id="1964f-113">This is how the property page retrieves the data from the scheduler.</span></span> <span data-ttu-id="1964f-114">Los fotogramas también se pueden quitar de nivel superior sin que el representador los vea.</span><span class="sxs-lookup"><span data-stu-id="1964f-114">Frames can also be dropped upstream without the renderer even seeing them.</span></span>

## <a name="requirements"></a><span data-ttu-id="1964f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1964f-115">Requirements</span></span>



| <span data-ttu-id="1964f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1964f-116">Requirement</span></span> | <span data-ttu-id="1964f-117">Value</span><span class="sxs-lookup"><span data-stu-id="1964f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1964f-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1964f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1964f-119"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1964f-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1964f-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1964f-120">Library</span></span><br/> | <dl> <span data-ttu-id="1964f-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1964f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1964f-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="1964f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1964f-123">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="1964f-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




