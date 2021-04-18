---
description: El método GetImageSize recupera información de tamaño de imagen de vídeo.
ms.assetid: a6d7f949-c6a9-49e9-b10a-f6f5bd73dc00
title: Método CBaseControlVideo. GetImageSize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed7795e3998bc101e907bce87c9981e86f51fcb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691099"
---
# <a name="cbasecontrolvideogetimagesize-method"></a><span data-ttu-id="62a0f-103">CBaseControlVideo. GetImageSize, método</span><span class="sxs-lookup"><span data-stu-id="62a0f-103">CBaseControlVideo.GetImageSize method</span></span>

<span data-ttu-id="62a0f-104">El `GetImageSize` método recupera información de tamaño de imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="62a0f-104">The `GetImageSize` method retrieves video image size information.</span></span>

## <a name="syntax"></a><span data-ttu-id="62a0f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62a0f-105">Syntax</span></span>


```C++
HRESULT GetImageSize(
   VIDEOINFOHEADER *pVideoInfo,
   long            *pBufferSize,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="62a0f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62a0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62a0f-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="62a0f-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="62a0f-108">Puntero a una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que se va a rellenar.</span><span class="sxs-lookup"><span data-stu-id="62a0f-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure to be filled in.</span></span>

</dd> <dt>

<span data-ttu-id="62a0f-109">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="62a0f-109">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="62a0f-110">Puntero al tamaño del búfer de vídeo.</span><span class="sxs-lookup"><span data-stu-id="62a0f-110">Pointer to the size of the video buffer.</span></span>

</dd> <dt>

<span data-ttu-id="62a0f-111">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="62a0f-111">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="62a0f-112">Puntero a las dimensiones del rectángulo del vídeo de origen.</span><span class="sxs-lookup"><span data-stu-id="62a0f-112">Pointer to the rectangle dimensions of the source video.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62a0f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62a0f-113">Return value</span></span>

<span data-ttu-id="62a0f-114">Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.</span><span class="sxs-lookup"><span data-stu-id="62a0f-114">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="62a0f-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="62a0f-115">Return code</span></span>                                                                                  | <span data-ttu-id="62a0f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="62a0f-116">Description</span></span>                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="62a0f-117"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="62a0f-117"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="62a0f-118">Error.</span><span class="sxs-lookup"><span data-stu-id="62a0f-118">Failure.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="62a0f-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="62a0f-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="62a0f-120">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="62a0f-120">Invalid argument.</span></span> <span data-ttu-id="62a0f-121">El formato de datos no es compatible.</span><span class="sxs-lookup"><span data-stu-id="62a0f-121">The data format is not compatible.</span></span><br/>           |
| <dl> <span data-ttu-id="62a0f-122"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="62a0f-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="62a0f-123">Se ha producido un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="62a0f-123">Unexpected error occurred.</span></span> <span data-ttu-id="62a0f-124">Uno o más argumentos son **null**.</span><span class="sxs-lookup"><span data-stu-id="62a0f-124">One or more arguments are **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="62a0f-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="62a0f-125"><dt>**NOERROR**</dt></span></span> </dl>       | <span data-ttu-id="62a0f-126">Correcto.</span><span class="sxs-lookup"><span data-stu-id="62a0f-126">Success.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="62a0f-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62a0f-127">Remarks</span></span>

<span data-ttu-id="62a0f-128">Esta función miembro es una función auxiliar que se usa para crear representaciones de imágenes de memoria de imágenes DIB.</span><span class="sxs-lookup"><span data-stu-id="62a0f-128">This member function is a helper function used for creating memory image renderings of DIB images.</span></span> <span data-ttu-id="62a0f-129">Se llama desde la implementación de la clase base de [**CBaseControlVideo:: GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) cuando se pasa un parámetro _pVideoImage_ **nulo** a esa función miembro.</span><span class="sxs-lookup"><span data-stu-id="62a0f-129">It is called from the base class implementation of [**CBaseControlVideo::GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) when a **NULL**_pVideoImage_ parameter is passed to that member function.</span></span> <span data-ttu-id="62a0f-130">Como resultado, esta función miembro crea y devuelve una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , usando la información de *pBufferSize* y *pSourceRect*.</span><span class="sxs-lookup"><span data-stu-id="62a0f-130">As a result, this member function constructs and returns a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, using the information in *pBufferSize* and *pSourceRect*.</span></span>

## <a name="requirements"></a><span data-ttu-id="62a0f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62a0f-131">Requirements</span></span>



| <span data-ttu-id="62a0f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="62a0f-132">Requirement</span></span> | <span data-ttu-id="62a0f-133">Value</span><span class="sxs-lookup"><span data-stu-id="62a0f-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62a0f-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62a0f-134">Header</span></span><br/>  | <dl> <span data-ttu-id="62a0f-135"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62a0f-135"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="62a0f-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62a0f-136">Library</span></span><br/> | <dl> <span data-ttu-id="62a0f-137"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="62a0f-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62a0f-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="62a0f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62a0f-139">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="62a0f-139">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




