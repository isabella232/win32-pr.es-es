---
description: El método SlowRender dibuja la imagen de vídeo con las funciones SetDIBitsToDevice o StretchDIBits.
ms.assetid: e1d8b189-b588-48eb-988a-3e5dedb38dbd
title: Método CDrawImage. SlowRender (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SlowRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b736bf6c44d4ada6e0a28408c449c9f8b2f1e1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660454"
---
# <a name="cdrawimageslowrender-method"></a><span data-ttu-id="c2838-103">CDrawImage. SlowRender, método</span><span class="sxs-lookup"><span data-stu-id="c2838-103">CDrawImage.SlowRender method</span></span>

<span data-ttu-id="c2838-104">El `SlowRender` método dibuja la imagen de vídeo mediante las funciones **SetDIBitsToDevice** o **StretchDIBits** .</span><span class="sxs-lookup"><span data-stu-id="c2838-104">The `SlowRender` method draws the video image using the **SetDIBitsToDevice** or **StretchDIBits** functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2838-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2838-105">Syntax</span></span>


```C++
void SlowRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="c2838-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2838-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2838-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="c2838-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="c2838-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo que contiene la imagen.</span><span class="sxs-lookup"><span data-stu-id="c2838-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2838-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2838-109">Return value</span></span>

<span data-ttu-id="c2838-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c2838-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2838-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2838-111">Remarks</span></span>

<span data-ttu-id="c2838-112">Si [**CDrawImage:: UsingImageAllocator**](cdrawimage-usingimageallocator.md) devuelve **false**, el método [**CDrawImage::D rawimage**](cdrawimage-drawimage.md) usa `SlowRender` para dibujar la imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c2838-112">If [**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md) returns **FALSE**, the [**CDrawImage::DrawImage**](cdrawimage-drawimage.md) method uses `SlowRender` to draw the video image.</span></span> <span data-ttu-id="c2838-113">De lo contrario, DrawImage usa el método **FastRender** .</span><span class="sxs-lookup"><span data-stu-id="c2838-113">Otherwise, DrawImage uses the **FastRender** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2838-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2838-114">Requirements</span></span>



| <span data-ttu-id="c2838-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2838-115">Requirement</span></span> | <span data-ttu-id="c2838-116">Value</span><span class="sxs-lookup"><span data-stu-id="c2838-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2838-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2838-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c2838-118"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2838-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c2838-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c2838-119">Library</span></span><br/> | <dl> <span data-ttu-id="c2838-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c2838-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2838-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2838-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2838-122">**Clase CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="c2838-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="c2838-123">**CDrawImage::FastRender**</span><span class="sxs-lookup"><span data-stu-id="c2838-123">**CDrawImage::FastRender**</span></span>](cdrawimage-fastrender.md)
</dt> </dl>

 

 




