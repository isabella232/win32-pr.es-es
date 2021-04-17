---
description: El método GetTargetRect recupera el rectángulo de destino. Se trata de una función miembro auxiliar interna.
ms.assetid: bf9d95c9-eee8-46b8-bdee-a7d16777ed83
title: Método CBaseControlVideo. GetTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d59a12e134edf37c8ab0a63f46f77923b112605d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670811"
---
# <a name="cbasecontrolvideogettargetrect-method"></a><span data-ttu-id="89f45-104">CBaseControlVideo. GetTargetRect, método</span><span class="sxs-lookup"><span data-stu-id="89f45-104">CBaseControlVideo.GetTargetRect method</span></span>

<span data-ttu-id="89f45-105">El `GetTargetRect` método recupera el rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="89f45-105">The `GetTargetRect` method retrieves the destination rectangle.</span></span> <span data-ttu-id="89f45-106">Se trata de una función miembro auxiliar interna.</span><span class="sxs-lookup"><span data-stu-id="89f45-106">This is an internal helper member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="89f45-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89f45-107">Syntax</span></span>


```C++
virtual HRESULT GetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="89f45-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89f45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89f45-109">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="89f45-109">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="89f45-110">Puntero al rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="89f45-110">Pointer to the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89f45-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89f45-111">Return value</span></span>

<span data-ttu-id="89f45-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="89f45-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="89f45-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89f45-113">Remarks</span></span>

<span data-ttu-id="89f45-114">Esta función miembro se debe invalidar en la clase derivada para devolver el rectángulo de destino mantenido por el representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="89f45-114">This member function must be overridden in the derived class to return the target rectangle held by the video renderer.</span></span> <span data-ttu-id="89f45-115">Se llama desde las siguientes funciones miembro de [**CBaseControlVideo**](cbasecontrolvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="89f45-115">It is called from the following [**CBaseControlVideo**](cbasecontrolvideo.md) member functions.</span></span>

-   [<span data-ttu-id="89f45-116">**CBaseControlVideo::GetDestinationPosition**</span><span class="sxs-lookup"><span data-stu-id="89f45-116">**CBaseControlVideo::GetDestinationPosition**</span></span>](cbasecontrolvideo-getdestinationposition.md)
-   [<span data-ttu-id="89f45-117">**CBaseControlVideo::p UT \_ DestinationLeft**</span><span class="sxs-lookup"><span data-stu-id="89f45-117">**CBaseControlVideo::put\_DestinationLeft**</span></span>](cbasecontrolvideo-put-destinationleft.md)
-   [<span data-ttu-id="89f45-118">**CBaseControlVideo:: get \_ DestinationLeft**</span><span class="sxs-lookup"><span data-stu-id="89f45-118">**CBaseControlVideo::get\_DestinationLeft**</span></span>](cbasecontrolvideo-get-destinationleft.md)
-   [<span data-ttu-id="89f45-119">**CBaseControlVideo::p UT \_ DestinationWidth**</span><span class="sxs-lookup"><span data-stu-id="89f45-119">**CBaseControlVideo::put\_DestinationWidth**</span></span>](cbasecontrolvideo-put-destinationwidth.md)
-   [<span data-ttu-id="89f45-120">**CBaseControlVideo:: get \_ DestinationWidth**</span><span class="sxs-lookup"><span data-stu-id="89f45-120">**CBaseControlVideo::get\_DestinationWidth**</span></span>](cbasecontrolvideo-get-destinationwidth.md)
-   [<span data-ttu-id="89f45-121">**CBaseControlVideo::p UT \_ DestinationTop**</span><span class="sxs-lookup"><span data-stu-id="89f45-121">**CBaseControlVideo::put\_DestinationTop**</span></span>](cbasecontrolvideo-put-destinationtop.md)
-   [<span data-ttu-id="89f45-122">**CBaseControlVideo:: get \_ DestinationTop**</span><span class="sxs-lookup"><span data-stu-id="89f45-122">**CBaseControlVideo::get\_DestinationTop**</span></span>](cbasecontrolvideo-get-destinationtop.md)
-   [<span data-ttu-id="89f45-123">**CBaseControlVideo::p UT \_ DestinationHeight**</span><span class="sxs-lookup"><span data-stu-id="89f45-123">**CBaseControlVideo::put\_DestinationHeight**</span></span>](cbasecontrolvideo-put-destinationheight.md)
-   [<span data-ttu-id="89f45-124">**CBaseControlVideo:: get \_ DestinationHeight**</span><span class="sxs-lookup"><span data-stu-id="89f45-124">**CBaseControlVideo::get\_DestinationHeight**</span></span>](cbasecontrolvideo-get-destinationheight.md)

<span data-ttu-id="89f45-125">En el ejemplo siguiente se muestra una implementación de esta función en una clase derivada.</span><span class="sxs-lookup"><span data-stu-id="89f45-125">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return the current destination rectangle.
HRESULT CVideoText::GetTargetRect(RECT *pTargetRect)
{
    ASSERT(pTargetRect);
    m_pRenderer->m_DrawImage.GetTargetRect(pTargetRect);
    return NOERROR;
}
```



<span data-ttu-id="89f45-126">En este ejemplo, CVideoText es una clase derivada de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer contiene un objeto de una clase derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md)y el miembro de \_ datos m DrawImage, definido en la clase derivada, contiene un objeto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="89f45-126">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="89f45-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89f45-127">Requirements</span></span>



| <span data-ttu-id="89f45-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="89f45-128">Requirement</span></span> | <span data-ttu-id="89f45-129">Value</span><span class="sxs-lookup"><span data-stu-id="89f45-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89f45-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89f45-130">Header</span></span><br/>  | <dl> <span data-ttu-id="89f45-131"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89f45-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="89f45-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="89f45-132">Library</span></span><br/> | <dl> <span data-ttu-id="89f45-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="89f45-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89f45-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="89f45-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89f45-135">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="89f45-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




