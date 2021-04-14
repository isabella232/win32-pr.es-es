---
description: El método IsDefaultTargetRect determina si el representador usa el rectángulo de destino predeterminado (virtual puro).
ms.assetid: 60c09515-7a34-421c-b3e8-ce746a935583
title: Método CBaseControlVideo. IsDefaultTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e267cc65345d18800beccbc80ac7952c89d781d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661405"
---
# <a name="cbasecontrolvideoisdefaulttargetrect-method"></a><span data-ttu-id="38ebc-103">CBaseControlVideo. IsDefaultTargetRect, método</span><span class="sxs-lookup"><span data-stu-id="38ebc-103">CBaseControlVideo.IsDefaultTargetRect method</span></span>

<span data-ttu-id="38ebc-104">El `IsDefaultTargetRect` método determina si el representador usa el rectángulo de destino predeterminado (virtual puro).</span><span class="sxs-lookup"><span data-stu-id="38ebc-104">The `IsDefaultTargetRect` method determines if the renderer is using the default target rectangle (pure virtual).</span></span>

## <a name="syntax"></a><span data-ttu-id="38ebc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38ebc-105">Syntax</span></span>


```C++
virtual HRESULT IsDefaultTargetRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="38ebc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38ebc-106">Parameters</span></span>

<span data-ttu-id="38ebc-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="38ebc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="38ebc-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38ebc-108">Return value</span></span>

<span data-ttu-id="38ebc-109">Devuelve S \_ OK si el representador usa el destino predeterminado; de lo contrario, devuelve s \_ false.</span><span class="sxs-lookup"><span data-stu-id="38ebc-109">Returns S\_OK if the renderer is using the default target; otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="38ebc-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38ebc-110">Remarks</span></span>

<span data-ttu-id="38ebc-111">Esta función miembro debe implementarse en la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="38ebc-111">This member function must be implemented in the derived class.</span></span> <span data-ttu-id="38ebc-112">Lo llama la función miembro [**CBaseControlVideo:: IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md) .</span><span class="sxs-lookup"><span data-stu-id="38ebc-112">It is called by the [**CBaseControlVideo::IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md) member function.</span></span>

<span data-ttu-id="38ebc-113">En el ejemplo siguiente se muestra una implementación de esta función en una clase derivada.</span><span class="sxs-lookup"><span data-stu-id="38ebc-113">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return S_OK if using the default target; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultTargetRect()
{
    RECT TargetRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetTargetRect(&TargetRect);

    // Check the destination that matches the initial client area.

    if (TargetRect.left != 0 || TargetRect.top != 0 ||
            TargetRect.right != m_Size.cx ||
                TargetRect.bottom != m_Size.cy) {
                    return S_FALSE;
    }
    return S_OK;
}
```



<span data-ttu-id="38ebc-114">En este ejemplo, CVideoText es una clase derivada de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer contiene un objeto de una clase derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md)y el miembro de \_ datos m DrawImage, definido en la clase derivada, contiene un objeto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="38ebc-114">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="38ebc-115">El \_ miembro de datos m mtIn, también definido en la clase derivada, contiene un objeto [**CMediaType**](cmediatype.md) con el tipo de medio del PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="38ebc-115">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="38ebc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38ebc-116">Requirements</span></span>



| <span data-ttu-id="38ebc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="38ebc-117">Requirement</span></span> | <span data-ttu-id="38ebc-118">Value</span><span class="sxs-lookup"><span data-stu-id="38ebc-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38ebc-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38ebc-119">Header</span></span><br/>  | <dl> <span data-ttu-id="38ebc-120"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38ebc-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="38ebc-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="38ebc-121">Library</span></span><br/> | <dl> <span data-ttu-id="38ebc-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="38ebc-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38ebc-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="38ebc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38ebc-124">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="38ebc-124">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




