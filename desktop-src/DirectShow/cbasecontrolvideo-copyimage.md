---
description: Crea una copia de la memoria de una imagen.
ms.assetid: 83a980bc-1298-439f-8dfc-49534591977f
title: Método CBaseControlVideo. CopyImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CopyImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 23ada87e77d3c3441f489abed2e7af86a2a556ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660528"
---
# <a name="cbasecontrolvideocopyimage-method"></a><span data-ttu-id="e2077-103">CBaseControlVideo. CopyImage, método</span><span class="sxs-lookup"><span data-stu-id="e2077-103">CBaseControlVideo.CopyImage method</span></span>

<span data-ttu-id="e2077-104">Crea una copia de la memoria de una imagen.</span><span class="sxs-lookup"><span data-stu-id="e2077-104">Creates a memory copy of an image.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2077-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2077-105">Syntax</span></span>


```C++
HRESULT CopyImage(
   IMediaSample    *pMediaSample,
   VIDEOINFOHEADER *pVideoInfo,
   LONG            *pBufferSize,
   BYTE            *pVideoImage,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="e2077-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2077-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2077-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="e2077-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="e2077-108">Puntero al ejemplo que contiene la imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e2077-108">Pointer to the sample containing the video image.</span></span>

</dd> <dt>

<span data-ttu-id="e2077-109">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="e2077-109">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="e2077-110">Puntero al formato que representa la imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e2077-110">Pointer to the format representing the video image.</span></span>

</dd> <dt>

<span data-ttu-id="e2077-111">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="e2077-111">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="e2077-112">Puntero al tamaño del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="e2077-112">Pointer to the size of the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e2077-113">*pVideoImage*</span><span class="sxs-lookup"><span data-stu-id="e2077-113">*pVideoImage*</span></span> 
</dt> <dd>

<span data-ttu-id="e2077-114">Puntero al búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="e2077-114">Pointer to the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e2077-115">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="e2077-115">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="e2077-116">Puntero al rectángulo de vídeo de origen.</span><span class="sxs-lookup"><span data-stu-id="e2077-116">Pointer to the source video rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2077-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2077-117">Return value</span></span>

<span data-ttu-id="e2077-118">Si el parámetro *pVideoImage* es **null**, el parámetro *pBufferSize* se rellena con el número de bytes que necesita el búfer de salida para almacenar la imagen.</span><span class="sxs-lookup"><span data-stu-id="e2077-118">If the *pVideoImage* parameter is **NULL**, the *pBufferSize* parameter is filled in with the number of bytes the output buffer requires to store the image.</span></span> <span data-ttu-id="e2077-119">Si el búfer pasado es demasiado pequeño o la función miembro no puede asignar memoria suficiente, la función miembro devuelve E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e2077-119">If the buffer passed in is too small or the member function fails to allocate sufficient memory, the member function returns E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2077-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2077-120">Remarks</span></span>

<span data-ttu-id="e2077-121">La función miembro recupera la imagen de la muestra y la copia en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="e2077-121">The member function retrieves the image from the sample and copies it into the output buffer.</span></span> <span data-ttu-id="e2077-122">La sección de vídeo copiada en el búfer de salida refleja el rectángulo de origen que se establece a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) (aunque no refleja el rectángulo de destino).</span><span class="sxs-lookup"><span data-stu-id="e2077-122">The section of video copied into the output buffer reflects the source rectangle that is set through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface (although it does not reflect the destination rectangle).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2077-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2077-123">Requirements</span></span>



| <span data-ttu-id="e2077-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2077-124">Requirement</span></span> | <span data-ttu-id="e2077-125">Value</span><span class="sxs-lookup"><span data-stu-id="e2077-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2077-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2077-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e2077-127"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2077-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e2077-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e2077-128">Library</span></span><br/> | <dl> <span data-ttu-id="e2077-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e2077-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2077-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2077-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2077-131">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="e2077-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




