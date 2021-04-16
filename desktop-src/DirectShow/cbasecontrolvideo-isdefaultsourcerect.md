---
description: El método IsDefaultSourceRect determina si el representador usa el rectángulo de origen predeterminado (virtual puro).
ms.assetid: 08c7a365-585c-47e6-9c26-6aa1fa3625e7
title: Método CBaseControlVideo. IsDefaultSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 390ae779eaa7d640d23b40a7e6f6579e158bf6ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671514"
---
# <a name="cbasecontrolvideoisdefaultsourcerect-method"></a><span data-ttu-id="9fcd7-103">CBaseControlVideo. IsDefaultSourceRect, método</span><span class="sxs-lookup"><span data-stu-id="9fcd7-103">CBaseControlVideo.IsDefaultSourceRect method</span></span>

<span data-ttu-id="9fcd7-104">El `IsDefaultSourceRect` método determina si el representador usa el rectángulo de origen predeterminado (virtual puro).</span><span class="sxs-lookup"><span data-stu-id="9fcd7-104">The `IsDefaultSourceRect` method determines if the renderer is using the default source rectangle (pure virtual).</span></span>

## <a name="syntax"></a><span data-ttu-id="9fcd7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fcd7-105">Syntax</span></span>


```C++
virtual HRESULT IsDefaultSourceRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="9fcd7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9fcd7-106">Parameters</span></span>

<span data-ttu-id="9fcd7-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9fcd7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9fcd7-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9fcd7-108">Return value</span></span>

<span data-ttu-id="9fcd7-109">Devuelve S \_ OK si el representador usa el origen predeterminado; de lo contrario, devuelve s \_ false.</span><span class="sxs-lookup"><span data-stu-id="9fcd7-109">Returns S\_OK if the renderer is using the default source; otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fcd7-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9fcd7-110">Remarks</span></span>

<span data-ttu-id="9fcd7-111">Esta función miembro debe implementarse en la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="9fcd7-111">This member function must be implemented in the derived class.</span></span> <span data-ttu-id="9fcd7-112">Lo llama la función miembro [**CBaseControlVideo:: IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md) .</span><span class="sxs-lookup"><span data-stu-id="9fcd7-112">It is called by the [**CBaseControlVideo::IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md) member function.</span></span>

<span data-ttu-id="9fcd7-113">En el ejemplo siguiente se muestra una implementación de esta función en una clase derivada.</span><span class="sxs-lookup"><span data-stu-id="9fcd7-113">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return S_OK if using the default source; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultSourceRect()
{
    RECT SourceRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetSourceRect(&SourceRect);

    // Check the coordinates that match the video dimensions.

    if (SourceRect.left != 0 || SourceRect.top != 0 ||
            SourceRect.right != pHeader->biWidth ||
                SourceRect.bottom != pHeader->biHeight) {
                    return S_FALSE;
    }
    return S_OK;
}
```



<span data-ttu-id="9fcd7-114">En este ejemplo, CVideoText es una clase derivada de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer contiene un objeto de una clase derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md)y el miembro de \_ datos m DrawImage, definido en la clase derivada, contiene un objeto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="9fcd7-114">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="9fcd7-115">El \_ miembro de datos m mtIn, también definido en la clase derivada, contiene un objeto [**CMediaType**](cmediatype.md) con el tipo de medio del PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="9fcd7-115">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with the media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fcd7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fcd7-116">Requirements</span></span>



| <span data-ttu-id="9fcd7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fcd7-117">Requirement</span></span> | <span data-ttu-id="9fcd7-118">Value</span><span class="sxs-lookup"><span data-stu-id="9fcd7-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fcd7-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9fcd7-119">Header</span></span><br/>  | <dl> <span data-ttu-id="9fcd7-120"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9fcd7-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9fcd7-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9fcd7-121">Library</span></span><br/> | <dl> <span data-ttu-id="9fcd7-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9fcd7-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fcd7-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fcd7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fcd7-124">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="9fcd7-124">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




