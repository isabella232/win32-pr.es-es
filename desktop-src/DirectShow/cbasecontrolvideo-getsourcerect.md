---
description: El método GetSourceRect recupera el rectángulo de origen. Este es un método interno.
ms.assetid: 51028b79-6aab-4abc-8ee8-2965bda9d191
title: Método CBaseControlVideo. GetSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e57a5beda7b147e952ecbb26c96df5f7e372e6d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690290"
---
# <a name="cbasecontrolvideogetsourcerect-method"></a><span data-ttu-id="71deb-104">CBaseControlVideo. GetSourceRect, método</span><span class="sxs-lookup"><span data-stu-id="71deb-104">CBaseControlVideo.GetSourceRect method</span></span>

<span data-ttu-id="71deb-105">El `GetSourceRect` método recupera el rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="71deb-105">The `GetSourceRect` method retrieves the source rectangle.</span></span> <span data-ttu-id="71deb-106">Este es un método interno.</span><span class="sxs-lookup"><span data-stu-id="71deb-106">This is an internal method.</span></span>

## <a name="syntax"></a><span data-ttu-id="71deb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71deb-107">Syntax</span></span>


```C++
virtual HRESULT GetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="71deb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71deb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71deb-109">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="71deb-109">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="71deb-110">Puntero al rectángulo de origen recuperado.</span><span class="sxs-lookup"><span data-stu-id="71deb-110">Pointer to the retrieved source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71deb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71deb-111">Return value</span></span>

<span data-ttu-id="71deb-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="71deb-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="71deb-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71deb-113">Remarks</span></span>

<span data-ttu-id="71deb-114">Esta función miembro se debe invalidar en la clase derivada para devolver el rectángulo de origen mantenido por el representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="71deb-114">This member function must be overridden in the derived class to return the source rectangle held by the video renderer.</span></span> <span data-ttu-id="71deb-115">Se llama desde las siguientes funciones miembro de [**CBaseControlVideo**](cbasecontrolvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="71deb-115">It is called from the following [**CBaseControlVideo**](cbasecontrolvideo.md) member functions.</span></span>

-   [<span data-ttu-id="71deb-116">**CBaseControlVideo::GetSourcePosition**</span><span class="sxs-lookup"><span data-stu-id="71deb-116">**CBaseControlVideo::GetSourcePosition**</span></span>](cbasecontrolvideo-getsourceposition.md)
-   [<span data-ttu-id="71deb-117">**CBaseControlVideo::p UT \_ SourceLeft**</span><span class="sxs-lookup"><span data-stu-id="71deb-117">**CBaseControlVideo::put\_SourceLeft**</span></span>](cbasecontrolvideo-put-sourceleft.md)
-   [<span data-ttu-id="71deb-118">**CBaseControlVideo:: get \_ SourceLeft**</span><span class="sxs-lookup"><span data-stu-id="71deb-118">**CBaseControlVideo::get\_SourceLeft**</span></span>](cbasecontrolvideo-get-sourceleft.md)
-   [<span data-ttu-id="71deb-119">**CBaseControlVideo::p UT \_ SourceWidth**</span><span class="sxs-lookup"><span data-stu-id="71deb-119">**CBaseControlVideo::put\_SourceWidth**</span></span>](cbasecontrolvideo-put-sourcewidth.md)
-   [<span data-ttu-id="71deb-120">**CBaseControlVideo:: get \_ SourceWidth**</span><span class="sxs-lookup"><span data-stu-id="71deb-120">**CBaseControlVideo::get\_SourceWidth**</span></span>](cbasecontrolvideo-get-sourcewidth.md)
-   [<span data-ttu-id="71deb-121">**CBaseControlVideo::p UT \_ SourceTop**</span><span class="sxs-lookup"><span data-stu-id="71deb-121">**CBaseControlVideo::put\_SourceTop**</span></span>](cbasecontrolvideo-put-sourcetop.md)
-   [<span data-ttu-id="71deb-122">**CBaseControlVideo:: get \_ SourceTop**</span><span class="sxs-lookup"><span data-stu-id="71deb-122">**CBaseControlVideo::get\_SourceTop**</span></span>](cbasecontrolvideo-get-sourcetop.md)
-   [<span data-ttu-id="71deb-123">**CBaseControlVideo::p UT \_ SourceHeight**</span><span class="sxs-lookup"><span data-stu-id="71deb-123">**CBaseControlVideo::put\_SourceHeight**</span></span>](cbasecontrolvideo-put-sourceheight.md)
-   [<span data-ttu-id="71deb-124">**CBaseControlVideo:: get \_ SourceHeight**</span><span class="sxs-lookup"><span data-stu-id="71deb-124">**CBaseControlVideo::get\_SourceHeight**</span></span>](cbasecontrolvideo-get-sourceheight.md)

<span data-ttu-id="71deb-125">En el ejemplo siguiente se muestra una implementación de esta función en una clase derivada.</span><span class="sxs-lookup"><span data-stu-id="71deb-125">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return the current source rectangle
HRESULT CVideoText::GetSourceRect(RECT *pSourceRect)
{
    ASSERT(pSourceRect);
    m_pRenderer->m_DrawImage.GetSourceRect(pSourceRect);
    return NOERROR;
}
```



<span data-ttu-id="71deb-126">En este ejemplo, CVideoText es una clase derivada de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer contiene un objeto de una clase derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md)y el miembro de \_ datos m DrawImage, definido en la clase derivada, contiene un objeto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="71deb-126">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="71deb-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71deb-127">Requirements</span></span>



| <span data-ttu-id="71deb-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="71deb-128">Requirement</span></span> | <span data-ttu-id="71deb-129">Value</span><span class="sxs-lookup"><span data-stu-id="71deb-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71deb-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71deb-130">Header</span></span><br/>  | <dl> <span data-ttu-id="71deb-131"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71deb-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="71deb-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="71deb-132">Library</span></span><br/> | <dl> <span data-ttu-id="71deb-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="71deb-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71deb-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="71deb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71deb-135">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="71deb-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




