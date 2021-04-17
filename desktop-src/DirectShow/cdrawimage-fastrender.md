---
description: El método FastRender dibuja la imagen de vídeo mediante las funciones BitBlt o StretchBlt.
ms.assetid: 8bbc96ce-393f-46fb-bf90-61d3ce0ef0d6
title: Método CDrawImage. FastRender (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.FastRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 823583beed6696d40803ccc098410dac053b8948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670734"
---
# <a name="cdrawimagefastrender-method"></a><span data-ttu-id="48b36-103">CDrawImage. FastRender, método</span><span class="sxs-lookup"><span data-stu-id="48b36-103">CDrawImage.FastRender method</span></span>

<span data-ttu-id="48b36-104">El `FastRender` método dibuja la imagen de vídeo mediante las funciones **bitblt** o **StretchBlt** .</span><span class="sxs-lookup"><span data-stu-id="48b36-104">The `FastRender` method draws the video image using the **BitBlt** or **StretchBlt** functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="48b36-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48b36-105">Syntax</span></span>


```C++
void FastRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="48b36-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48b36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48b36-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="48b36-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="48b36-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo que contiene la imagen.</span><span class="sxs-lookup"><span data-stu-id="48b36-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48b36-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48b36-109">Return value</span></span>

<span data-ttu-id="48b36-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="48b36-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="48b36-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48b36-111">Remarks</span></span>

<span data-ttu-id="48b36-112">El método [**CDrawImage::D rawimage**](cdrawimage-drawimage.md) llama a este método, pero solo si el asignador de la conexión es un objeto [**CImageAllocator**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="48b36-112">The [**CDrawImage::DrawImage**](cdrawimage-drawimage.md) method calls this method, but only if the allocator for the connection is a [**CImageAllocator**](cimageallocator.md) object.</span></span> <span data-ttu-id="48b36-113">En ese caso, se garantiza que el ejemplo multimedia es un objeto [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="48b36-113">In that case, the media sample is guaranteed to be a [**CImageSample**](cimagesample.md) object.</span></span> <span data-ttu-id="48b36-114">El objeto **CImageSample** usa la función **CreateDIBSection** para asignar la memoria compartida para el mapa de bits, lo que permite dibujar la imagen mediante **bitblt** o **StretchBlt**.</span><span class="sxs-lookup"><span data-stu-id="48b36-114">The **CImageSample** object uses the **CreateDIBSection** function to allocate shared memory for the bitmap, which makes it possible to draw the image using either **BitBlt** or **StretchBlt**.</span></span>

<span data-ttu-id="48b36-115">Este método llama a **bitblt** si los rectángulos de origen y destino coinciden exactamente, o **StretchBlt** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="48b36-115">This method calls **BitBlt** if the source and targer rectangles exactly match, or **StretchBlt** otherwise.</span></span>

<span data-ttu-id="48b36-116">Si el filtro no posee el asignador, el método **DrawImage** usa [**CDrawImage:: SlowRender**](cdrawimage-slowrender.md) para dibujar la imagen.</span><span class="sxs-lookup"><span data-stu-id="48b36-116">If the filter does not own the allocator, the **DrawImage** method uses [**CDrawImage::SlowRender**](cdrawimage-slowrender.md) to draw the image.</span></span>

## <a name="requirements"></a><span data-ttu-id="48b36-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48b36-117">Requirements</span></span>



| <span data-ttu-id="48b36-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="48b36-118">Requirement</span></span> | <span data-ttu-id="48b36-119">Value</span><span class="sxs-lookup"><span data-stu-id="48b36-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48b36-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48b36-120">Header</span></span><br/>  | <dl> <span data-ttu-id="48b36-121"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48b36-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="48b36-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="48b36-122">Library</span></span><br/> | <dl> <span data-ttu-id="48b36-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="48b36-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48b36-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="48b36-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48b36-125">**Clase CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="48b36-125">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




