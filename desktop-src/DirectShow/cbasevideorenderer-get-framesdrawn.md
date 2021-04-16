---
description: El \_ método get FramesDrawn recupera la \_ variable miembro de m cFramesDrawn, y ofrece el número de fotogramas dibujados desde que se inició el streaming.
ms.assetid: 486b5541-2952-47ce-944e-4efb8e5af9dd
title: Método CBaseVideoRenderer.get_FramesDrawn (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDrawn
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec8254e06429022bf657322e98ab317475c82f90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679307"
---
# <a name="cbasevideorendererget_framesdrawn-method"></a><span data-ttu-id="94ff5-103">CBaseVideoRenderer. Get \_ FramesDrawn (método)</span><span class="sxs-lookup"><span data-stu-id="94ff5-103">CBaseVideoRenderer.get\_FramesDrawn method</span></span>

<span data-ttu-id="94ff5-104">El `get_FramesDrawn` método recupera la variable de miembro **m \_ cFramesDrawn** , lo que permite el número de fotogramas dibujados desde que se inició el streaming.</span><span class="sxs-lookup"><span data-stu-id="94ff5-104">The `get_FramesDrawn` method retrieves the **m\_cFramesDrawn** member variable, giving the number of frames drawn since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="94ff5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94ff5-105">Syntax</span></span>


```C++
HRESULT get_FramesDrawn(
   int *pcFramesDrawn
);
```



## <a name="parameters"></a><span data-ttu-id="94ff5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94ff5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94ff5-107">*pcFramesDrawn*</span><span class="sxs-lookup"><span data-stu-id="94ff5-107">*pcFramesDrawn*</span></span> 
</dt> <dd>

<span data-ttu-id="94ff5-108">Puntero al número de fotogramas dibujados.</span><span class="sxs-lookup"><span data-stu-id="94ff5-108">Pointer to the number of frames drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94ff5-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94ff5-109">Return value</span></span>

<span data-ttu-id="94ff5-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="94ff5-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="94ff5-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94ff5-111">Remarks</span></span>

<span data-ttu-id="94ff5-112">Esta función miembro implementa el método [**IQualProp:: get \_ FramesDrawn**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdrawn) .</span><span class="sxs-lookup"><span data-stu-id="94ff5-112">This member function implements the [**IQualProp::get\_FramesDrawn**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdrawn) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="94ff5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94ff5-113">Requirements</span></span>



| <span data-ttu-id="94ff5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="94ff5-114">Requirement</span></span> | <span data-ttu-id="94ff5-115">Value</span><span class="sxs-lookup"><span data-stu-id="94ff5-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94ff5-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94ff5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="94ff5-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94ff5-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="94ff5-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="94ff5-118">Library</span></span><br/> | <dl> <span data-ttu-id="94ff5-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="94ff5-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94ff5-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="94ff5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94ff5-121">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="94ff5-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




