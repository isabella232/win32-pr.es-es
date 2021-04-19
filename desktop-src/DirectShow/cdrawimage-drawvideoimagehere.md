---
description: El método DrawVideoImageHere dibuja una imagen de un ejemplo multimedia en un contexto de dispositivo especificado.
ms.assetid: b11e1c6b-5a29-444f-a0a9-049cd9d49b13
title: Método CDrawImage. DrawVideoImageHere (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawVideoImageHere
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 599dd82e282f2d14ac7e974363a62695e209c080
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660457"
---
# <a name="cdrawimagedrawvideoimagehere-method"></a><span data-ttu-id="24307-103">CDrawImage. DrawVideoImageHere, método</span><span class="sxs-lookup"><span data-stu-id="24307-103">CDrawImage.DrawVideoImageHere method</span></span>

<span data-ttu-id="24307-104">El `DrawVideoImageHere` método dibuja una imagen de un ejemplo multimedia en un contexto de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="24307-104">The `DrawVideoImageHere` method draws an image from a media sample to a specified device context.</span></span>

## <a name="syntax"></a><span data-ttu-id="24307-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24307-105">Syntax</span></span>


```C++
BOOL DrawVideoImageHere(
   HDC          hdc,
   IMediaSample *pMediaSample,
   RECT         *lprcSrc,
   RECT         *lprcDst
);
```



## <a name="parameters"></a><span data-ttu-id="24307-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24307-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24307-107">*cámaras*</span><span class="sxs-lookup"><span data-stu-id="24307-107">*hdc*</span></span> 
</dt> <dd>

<span data-ttu-id="24307-108">Identificador de un contexto de dispositivo, donde se producirá el dibujo.</span><span class="sxs-lookup"><span data-stu-id="24307-108">Handle to a device context, where the drawing will occur.</span></span>

</dd> <dt>

<span data-ttu-id="24307-109">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="24307-109">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="24307-110">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo que contiene la imagen.</span><span class="sxs-lookup"><span data-stu-id="24307-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> <dt>

<span data-ttu-id="24307-111">*lprcSrc*</span><span class="sxs-lookup"><span data-stu-id="24307-111">*lprcSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="24307-112">Puntero a un rectángulo de origen que se va a utilizar para dibujar.</span><span class="sxs-lookup"><span data-stu-id="24307-112">Pointer to a source rectangle to use for drawing.</span></span> <span data-ttu-id="24307-113">Si es **null**, se usa el rectángulo en [**CDrawImage:: m \_ SourceRect**](cdrawimage-m-sourcerect.md) .</span><span class="sxs-lookup"><span data-stu-id="24307-113">If **NULL**, the rectangle in [**CDrawImage::m\_SourceRect**](cdrawimage-m-sourcerect.md) is used.</span></span>

</dd> <dt>

<span data-ttu-id="24307-114">*lprcDst*</span><span class="sxs-lookup"><span data-stu-id="24307-114">*lprcDst*</span></span> 
</dt> <dd>

<span data-ttu-id="24307-115">Puntero a un rectángulo de destino que se va a utilizar para dibujar.</span><span class="sxs-lookup"><span data-stu-id="24307-115">Pointer to a target rectangle to use for drawing.</span></span> <span data-ttu-id="24307-116">Si es **null**, se usa el rectángulo en [**CDrawImage:: m \_ TargetRect**](cdrawimage-m-targetrect.md) .</span><span class="sxs-lookup"><span data-stu-id="24307-116">If **NULL**, the rectangle in [**CDrawImage::m\_TargetRect**](cdrawimage-m-targetrect.md) is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24307-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24307-117">Return value</span></span>

<span data-ttu-id="24307-118">Devuelve **true si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="24307-118">Returns **TRUE** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="24307-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24307-119">Requirements</span></span>



| <span data-ttu-id="24307-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="24307-120">Requirement</span></span> | <span data-ttu-id="24307-121">Value</span><span class="sxs-lookup"><span data-stu-id="24307-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24307-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="24307-122">Header</span></span><br/>  | <dl> <span data-ttu-id="24307-123"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24307-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="24307-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="24307-124">Library</span></span><br/> | <dl> <span data-ttu-id="24307-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="24307-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24307-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="24307-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24307-127">**Clase CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="24307-127">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




