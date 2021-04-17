---
description: El método SetTargetRect establece el rectángulo de destino actual (virtual puro). Se trata de una función miembro interna a la que se llama cuando cambia el rectángulo de destino.
ms.assetid: 9e48989d-5995-4f9d-82b2-01229473c3e8
title: Método CBaseControlVideo. SetTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3868e7d8df93940829fb96c7152a55048a5cae82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661207"
---
# <a name="cbasecontrolvideosettargetrect-method"></a><span data-ttu-id="3fd2d-104">CBaseControlVideo. SetTargetRect, método</span><span class="sxs-lookup"><span data-stu-id="3fd2d-104">CBaseControlVideo.SetTargetRect method</span></span>

<span data-ttu-id="3fd2d-105">El `SetTargetRect` método establece el rectángulo de destino actual (virtual puro).</span><span class="sxs-lookup"><span data-stu-id="3fd2d-105">The `SetTargetRect` method sets the current target rectangle (pure virtual).</span></span> <span data-ttu-id="3fd2d-106">Se trata de una función miembro interna a la que se llama cuando cambia el rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="3fd2d-106">This is an internal member function that gets called when the destination rectangle changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fd2d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fd2d-107">Syntax</span></span>


```C++
virtual HRESULT SetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="3fd2d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3fd2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fd2d-109">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="3fd2d-109">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="3fd2d-110">Puntero al rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="3fd2d-110">Pointer to the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fd2d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3fd2d-111">Return value</span></span>

<span data-ttu-id="3fd2d-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3fd2d-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fd2d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3fd2d-113">Remarks</span></span>

<span data-ttu-id="3fd2d-114">Las clases derivadas deben invalidar esto para saber cuándo cambia el rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="3fd2d-114">Derived classes should override this to know when the destination rectangle changes.</span></span> <span data-ttu-id="3fd2d-115">Se llama desde las siguientes funciones miembro.</span><span class="sxs-lookup"><span data-stu-id="3fd2d-115">It is called from the following member functions.</span></span>

-   [<span data-ttu-id="3fd2d-116">**CBaseControlVideo::SetDestinationPosition**</span><span class="sxs-lookup"><span data-stu-id="3fd2d-116">**CBaseControlVideo::SetDestinationPosition**</span></span>](cbasecontrolvideo-setdestinationposition.md)
-   [<span data-ttu-id="3fd2d-117">**CBaseControlVideo::p UT \_ DestinationLeft**</span><span class="sxs-lookup"><span data-stu-id="3fd2d-117">**CBaseControlVideo::put\_DestinationLeft**</span></span>](cbasecontrolvideo-put-destinationleft.md)
-   [<span data-ttu-id="3fd2d-118">**CBaseControlVideo::p UT \_ DestinationWidth**</span><span class="sxs-lookup"><span data-stu-id="3fd2d-118">**CBaseControlVideo::put\_DestinationWidth**</span></span>](cbasecontrolvideo-put-destinationwidth.md)
-   [<span data-ttu-id="3fd2d-119">**CBaseControlVideo::p UT \_ DestinationTop**</span><span class="sxs-lookup"><span data-stu-id="3fd2d-119">**CBaseControlVideo::put\_DestinationTop**</span></span>](cbasecontrolvideo-put-destinationtop.md)
-   [<span data-ttu-id="3fd2d-120">**CBaseControlVideo::p UT \_ DestinationHeight**</span><span class="sxs-lookup"><span data-stu-id="3fd2d-120">**CBaseControlVideo::put\_DestinationHeight**</span></span>](cbasecontrolvideo-put-destinationheight.md)

<span data-ttu-id="3fd2d-121">En el ejemplo siguiente se muestra una implementación de esta función en una clase derivada.</span><span class="sxs-lookup"><span data-stu-id="3fd2d-121">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
HRESULT CVideoText::SetTargetRect(RECT *pTargetRect)
{
    m_pRenderer->m_DrawImage.SetTargetRect(pTargetRect);
    return NOERROR;
}
```



<span data-ttu-id="3fd2d-122">En este ejemplo, CVideoText es una clase derivada de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer contiene un objeto de una clase derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md)y el miembro de \_ datos m DrawImage, definido en la clase derivada, contiene un objeto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="3fd2d-122">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fd2d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fd2d-123">Requirements</span></span>



| <span data-ttu-id="3fd2d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fd2d-124">Requirement</span></span> | <span data-ttu-id="3fd2d-125">Value</span><span class="sxs-lookup"><span data-stu-id="3fd2d-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd2d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3fd2d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="3fd2d-127"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3fd2d-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3fd2d-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3fd2d-128">Library</span></span><br/> | <dl> <span data-ttu-id="3fd2d-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3fd2d-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fd2d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fd2d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fd2d-131">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="3fd2d-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




