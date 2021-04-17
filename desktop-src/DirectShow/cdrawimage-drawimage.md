---
description: El método DrawImage dibuja un fotograma de vídeo en la ventana de vídeo.
ms.assetid: 22e7f59c-90f7-4e0c-8993-eea1eaf58fba
title: Método CDrawImage. DrawImage (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d219eb82ab2cf1929605eee4045c2f278022ad98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660458"
---
# <a name="cdrawimagedrawimage-method"></a><span data-ttu-id="cdaf0-103">CDrawImage. DrawImage (método)</span><span class="sxs-lookup"><span data-stu-id="cdaf0-103">CDrawImage.DrawImage method</span></span>

<span data-ttu-id="cdaf0-104">El `DrawImage` método dibuja un fotograma de vídeo en la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cdaf0-104">The `DrawImage` method draws a video frame on the video window.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdaf0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cdaf0-105">Syntax</span></span>


```C++
BOOL DrawImage(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="cdaf0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cdaf0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdaf0-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="cdaf0-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="cdaf0-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo que contiene la imagen.</span><span class="sxs-lookup"><span data-stu-id="cdaf0-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdaf0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cdaf0-109">Return value</span></span>

<span data-ttu-id="cdaf0-110">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cdaf0-110">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdaf0-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cdaf0-111">Remarks</span></span>

<span data-ttu-id="cdaf0-112">Este método delega en [**CDrawImage:: FastRender**](cdrawimage-fastrender.md) o [**CDrawImage:: SlowRender**](cdrawimage-slowrender.md), en función de si el filtro posee el asignador que proporcionó el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="cdaf0-112">This method delegates to [**CDrawImage::FastRender**](cdrawimage-fastrender.md) or [**CDrawImage::SlowRender**](cdrawimage-slowrender.md), depending on whether the filter owns the allocator that provided the sample.</span></span> <span data-ttu-id="cdaf0-113">Si el filtro posee el asignador, se garantiza que el ejemplo es un objeto [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="cdaf0-113">If the filter does own the allocator, the sample is guaranteed to be a [**CImageSample**](cimagesample.md) object.</span></span> <span data-ttu-id="cdaf0-114">En ese caso, el ejemplo utiliza la memoria compartida asignada por GDI y la imagen se puede dibujar mediante **bitblt** o **StretchBlt**.</span><span class="sxs-lookup"><span data-stu-id="cdaf0-114">In that case, the sample uses shared memory allocated by GDI, and the image can be drawn using either **BitBlt** or **StretchBlt**.</span></span> <span data-ttu-id="cdaf0-115">De lo contrario, las imágenes se deben dibujar con las funciones **SetDIBitsToDevice** o **StretchDIBits** más lentas.</span><span class="sxs-lookup"><span data-stu-id="cdaf0-115">Otherwise, the images must be drawn using the slower **SetDIBitsToDevice** or **StretchDIBits** functions.</span></span>

<span data-ttu-id="cdaf0-116">En las compilaciones de depuración, este método llama a **DisplaySampleTimes** para dibujar las marcas de tiempo del ejemplo sobre la imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cdaf0-116">In debug builds, this method calls **DisplaySampleTimes** to draw the sample's time stamps over the video image.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdaf0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdaf0-117">Requirements</span></span>



| <span data-ttu-id="cdaf0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdaf0-118">Requirement</span></span> | <span data-ttu-id="cdaf0-119">Value</span><span class="sxs-lookup"><span data-stu-id="cdaf0-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdaf0-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cdaf0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="cdaf0-121"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdaf0-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cdaf0-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cdaf0-122">Library</span></span><br/> | <dl> <span data-ttu-id="cdaf0-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="cdaf0-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdaf0-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="cdaf0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdaf0-125">**Clase CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="cdaf0-125">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="cdaf0-126">**CDrawImage::UsingImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="cdaf0-126">**CDrawImage::UsingImageAllocator**</span></span>](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




