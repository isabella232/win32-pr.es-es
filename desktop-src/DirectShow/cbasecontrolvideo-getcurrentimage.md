---
description: El método GetCurrentImage recupera una copia de la imagen actual en el representador.
ms.assetid: fa322bd2-18e4-481d-bde1-92deb0f7de61
title: Método CBaseControlVideo. GetCurrentImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetCurrentImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d44e6930d0d7e179162939c13a54f2953c5ab965
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691100"
---
# <a name="cbasecontrolvideogetcurrentimage-method"></a><span data-ttu-id="12821-103">CBaseControlVideo. GetCurrentImage, método</span><span class="sxs-lookup"><span data-stu-id="12821-103">CBaseControlVideo.GetCurrentImage method</span></span>

<span data-ttu-id="12821-104">El `GetCurrentImage` método recupera una copia de la imagen actual en el representador.</span><span class="sxs-lookup"><span data-stu-id="12821-104">The `GetCurrentImage` method retrieves a copy of the current image at the renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="12821-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12821-105">Syntax</span></span>


```C++
HRESULT GetCurrentImage(
   long *pBufferSize,
   long *pVideoImage
);
```



## <a name="parameters"></a><span data-ttu-id="12821-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="12821-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12821-107">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="12821-107">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="12821-108">Puntero al tamaño del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="12821-108">Pointer to the size of the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="12821-109">*pVideoImage*</span><span class="sxs-lookup"><span data-stu-id="12821-109">*pVideoImage*</span></span> 
</dt> <dd>

<span data-ttu-id="12821-110">Puntero al búfer de salida de la imagen.</span><span class="sxs-lookup"><span data-stu-id="12821-110">Pointer to the output buffer for the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12821-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="12821-111">Return value</span></span>

<span data-ttu-id="12821-112">Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.</span><span class="sxs-lookup"><span data-stu-id="12821-112">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="12821-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="12821-113">Return code</span></span>                                                                                        | <span data-ttu-id="12821-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="12821-114">Description</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="12821-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="12821-115"><dt>**E\_FAIL**</dt></span></span> </dl>             | <span data-ttu-id="12821-116">Error.</span><span class="sxs-lookup"><span data-stu-id="12821-116">Failure.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="12821-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="12821-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>       | <span data-ttu-id="12821-118">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="12821-118">Invalid argument.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="12821-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="12821-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>      | <span data-ttu-id="12821-120">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="12821-120">Out of memory.</span></span> <span data-ttu-id="12821-121">Se devuelve cuando el parámetro *pVideoInfo* es **null**.</span><span class="sxs-lookup"><span data-stu-id="12821-121">Returned when the *pVideoInfo* parameter is **NULL**.</span></span><br/>   |
| <dl> <span data-ttu-id="12821-122"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="12821-122"><dt>**NOERROR**</dt></span></span> </dl>             | <span data-ttu-id="12821-123">Correcto.</span><span class="sxs-lookup"><span data-stu-id="12821-123">Success.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="12821-124"><dt>**VFW \_ E \_ no \_ pausado**</dt></span><span class="sxs-lookup"><span data-stu-id="12821-124"><dt>**VFW\_E\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="12821-125">No se pudo realizar la operación porque el filtro no está en pausa.</span><span class="sxs-lookup"><span data-stu-id="12821-125">The operation could not be performed because the filter is not paused.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="12821-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12821-126">Remarks</span></span>

<span data-ttu-id="12821-127">Esta función miembro recupera la imagen de la muestra y la copia en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="12821-127">This member function retrieves the image from the sample and copies it into the output buffer.</span></span> <span data-ttu-id="12821-128">La sección de vídeo copiada en el búfer de salida refleja el rectángulo de origen establecido a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="12821-128">The section of video copied into the output buffer reflects the source rectangle set through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="12821-129">No refleja el rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="12821-129">It does not reflect the destination rectangle.</span></span>

## <a name="requirements"></a><span data-ttu-id="12821-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12821-130">Requirements</span></span>



| <span data-ttu-id="12821-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="12821-131">Requirement</span></span> | <span data-ttu-id="12821-132">Value</span><span class="sxs-lookup"><span data-stu-id="12821-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12821-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12821-133">Header</span></span><br/>  | <dl> <span data-ttu-id="12821-134"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="12821-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="12821-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12821-135">Library</span></span><br/> | <dl> <span data-ttu-id="12821-136"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="12821-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12821-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="12821-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12821-138">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="12821-138">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




