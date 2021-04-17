---
description: El método SetDefaultSourceRect establece el rectángulo de vídeo de origen predeterminado (virtual puro). This en una función miembro interna a la que se llama cuando se restablece el rectángulo de origen.
ms.assetid: d0dae0a9-8763-485e-b9d3-80076a3f2f35
title: Método CBaseControlVideo. SetDefaultSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 82fe2001a42ca75fff4f3172c8ce05da18881d73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671170"
---
# <a name="cbasecontrolvideosetdefaultsourcerect-method"></a><span data-ttu-id="2e88e-104">CBaseControlVideo. SetDefaultSourceRect, método</span><span class="sxs-lookup"><span data-stu-id="2e88e-104">CBaseControlVideo.SetDefaultSourceRect method</span></span>

<span data-ttu-id="2e88e-105">El `SetDefaultSourceRect` método establece el rectángulo de vídeo de origen predeterminado (virtual puro).</span><span class="sxs-lookup"><span data-stu-id="2e88e-105">The `SetDefaultSourceRect` method sets the default source video rectangle (pure virtual).</span></span> <span data-ttu-id="2e88e-106">This en una función miembro interna a la que se llama cuando se restablece el rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="2e88e-106">This in an internal member function that gets called when the source rectangle is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e88e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e88e-107">Syntax</span></span>


```C++
virtual HRESULT SetDefaultSourceRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="2e88e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e88e-108">Parameters</span></span>

<span data-ttu-id="2e88e-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2e88e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e88e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e88e-110">Return value</span></span>

<span data-ttu-id="2e88e-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2e88e-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e88e-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e88e-112">Remarks</span></span>

<span data-ttu-id="2e88e-113">Las clases derivadas deben invalidar esto para restablecer el rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="2e88e-113">Derived classes should override this to reset the source rectangle.</span></span> <span data-ttu-id="2e88e-114">Se llama desde [**CBaseControlVideo:: SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md).</span><span class="sxs-lookup"><span data-stu-id="2e88e-114">It is called from [**CBaseControlVideo::SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md).</span></span>

<span data-ttu-id="2e88e-115">En el ejemplo siguiente se muestra una implementación de esta función en una clase derivada.</span><span class="sxs-lookup"><span data-stu-id="2e88e-115">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// This is called when you reset the default source rectangle.
HRESULT CVideoText::SetDefaultSourceRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT SourceRect = {0,0,pHeader->biWidth,pHeader->biHeight};
    m_pRenderer->m_DrawImage.SetSourceRect(&SourceRect);
    return NOERROR;
}
```



<span data-ttu-id="2e88e-116">En este ejemplo, CVideoText es una clase derivada de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer contiene un objeto de una clase derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md)y el miembro de \_ datos m DrawImage, definido en la clase derivada, contiene un objeto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="2e88e-116">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="2e88e-117">El \_ miembro de datos m mtIn, también definido en la clase derivada, contiene un objeto [**CMediaType**](cmediatype.md) con el tipo de medio del PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="2e88e-117">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e88e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e88e-118">Requirements</span></span>



| <span data-ttu-id="2e88e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e88e-119">Requirement</span></span> | <span data-ttu-id="2e88e-120">Value</span><span class="sxs-lookup"><span data-stu-id="2e88e-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e88e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e88e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2e88e-122"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e88e-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2e88e-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2e88e-123">Library</span></span><br/> | <dl> <span data-ttu-id="2e88e-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2e88e-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e88e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e88e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e88e-126">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="2e88e-126">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




