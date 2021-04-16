---
description: El método SetSourceRect establece el rectángulo de vídeo de origen actual (virtual puro). Se trata de una función miembro interna a la que se llama cuando cambia el rectángulo de origen.
ms.assetid: 13bb594b-b154-40a2-ad00-f1e86781074d
title: Método CBaseControlVideo. SetSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e3be6cc3819e1452fd196d4906377204a6e90bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671567"
---
# <a name="cbasecontrolvideosetsourcerect-method"></a><span data-ttu-id="384e4-104">CBaseControlVideo. SetSourceRect, método</span><span class="sxs-lookup"><span data-stu-id="384e4-104">CBaseControlVideo.SetSourceRect method</span></span>

<span data-ttu-id="384e4-105">El `SetSourceRect` método establece el rectángulo de vídeo de origen actual (virtual puro).</span><span class="sxs-lookup"><span data-stu-id="384e4-105">The `SetSourceRect` method sets the current source video rectangle (pure virtual).</span></span> <span data-ttu-id="384e4-106">Se trata de una función miembro interna a la que se llama cuando cambia el rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="384e4-106">This is an internal member function that gets called when the source rectangle changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="384e4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="384e4-107">Syntax</span></span>


```C++
virtual HRESULT SetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="384e4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="384e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="384e4-109">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="384e4-109">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="384e4-110">Puntero al rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="384e4-110">Pointer to the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="384e4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="384e4-111">Return value</span></span>

<span data-ttu-id="384e4-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="384e4-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="384e4-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="384e4-113">Remarks</span></span>

<span data-ttu-id="384e4-114">Las clases derivadas deben invalidar esta función miembro para saber cuándo cambia el rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="384e4-114">Derived classes should override this member function to know when the source rectangle changes.</span></span> <span data-ttu-id="384e4-115">Se llama desde las siguientes funciones miembro.</span><span class="sxs-lookup"><span data-stu-id="384e4-115">It is called from the following member functions.</span></span>

-   [<span data-ttu-id="384e4-116">**CBaseControlVideo::SetSourcePosition**</span><span class="sxs-lookup"><span data-stu-id="384e4-116">**CBaseControlVideo::SetSourcePosition**</span></span>](cbasecontrolvideo-setsourceposition.md)
-   [<span data-ttu-id="384e4-117">**CBaseControlVideo::p UT \_ SourceLeft**</span><span class="sxs-lookup"><span data-stu-id="384e4-117">**CBaseControlVideo::put\_SourceLeft**</span></span>](cbasecontrolvideo-put-sourceleft.md)
-   [<span data-ttu-id="384e4-118">**CBaseControlVideo::p UT \_ SourceWidth**</span><span class="sxs-lookup"><span data-stu-id="384e4-118">**CBaseControlVideo::put\_SourceWidth**</span></span>](cbasecontrolvideo-put-sourcewidth.md)
-   [<span data-ttu-id="384e4-119">**CBaseControlVideo::p UT \_ SourceTop**</span><span class="sxs-lookup"><span data-stu-id="384e4-119">**CBaseControlVideo::put\_SourceTop**</span></span>](cbasecontrolvideo-put-sourcetop.md)
-   [<span data-ttu-id="384e4-120">**CBaseControlVideo::p UT \_ SourceHeight**</span><span class="sxs-lookup"><span data-stu-id="384e4-120">**CBaseControlVideo::put\_SourceHeight**</span></span>](cbasecontrolvideo-put-sourceheight.md)

<span data-ttu-id="384e4-121">En el ejemplo siguiente se muestra una implementación de esta función en una clase derivada.</span><span class="sxs-lookup"><span data-stu-id="384e4-121">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
HRESULT CVideoText::SetSourceRect(RECT *pSourceRect)
{
    m_pRenderer->m_DrawImage.SetSourceRect(pSourceRect);
    return NOERROR;
}
```



<span data-ttu-id="384e4-122">En este ejemplo, CVideoText es una clase derivada de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer contiene un objeto de una clase derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md)y el miembro de \_ datos m DrawImage, definido en la clase derivada, contiene un objeto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="384e4-122">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="384e4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="384e4-123">Requirements</span></span>



| <span data-ttu-id="384e4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="384e4-124">Requirement</span></span> | <span data-ttu-id="384e4-125">Value</span><span class="sxs-lookup"><span data-stu-id="384e4-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="384e4-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="384e4-126">Header</span></span><br/>  | <dl> <span data-ttu-id="384e4-127"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="384e4-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="384e4-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="384e4-128">Library</span></span><br/> | <dl> <span data-ttu-id="384e4-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="384e4-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="384e4-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="384e4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="384e4-131">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="384e4-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




