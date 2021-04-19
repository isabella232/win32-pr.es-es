---
description: El \_ método get SourceLeft recupera la coordenada izquierda del rectángulo de origen actual.
ms.assetid: dbfb1850-6e49-481c-b26a-22ccb9e4455a
title: Método CBaseControlVideo.get_SourceLeft (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceLeft
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2b7ff62617b9fa378511dba2838f0dcbdb25dbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660516"
---
# <a name="cbasecontrolvideoget_sourceleft-method"></a><span data-ttu-id="dd239-103">CBaseControlVideo. Get \_ SourceLeft (método)</span><span class="sxs-lookup"><span data-stu-id="dd239-103">CBaseControlVideo.get\_SourceLeft method</span></span>

<span data-ttu-id="dd239-104">El `get_SourceLeft` método recupera la coordenada izquierda del rectángulo de origen actual.</span><span class="sxs-lookup"><span data-stu-id="dd239-104">The `get_SourceLeft` method retrieves the left coordinate of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd239-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd239-105">Syntax</span></span>


```C++
HRESULT get_SourceLeft(
   long *pSourceLeft
);
```



## <a name="parameters"></a><span data-ttu-id="dd239-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd239-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd239-107">*pSourceLeft*</span><span class="sxs-lookup"><span data-stu-id="dd239-107">*pSourceLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="dd239-108">Puntero a la coordenada izquierda del rectángulo de origen actual.</span><span class="sxs-lookup"><span data-stu-id="dd239-108">Pointer to the left coordinate of the current source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd239-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd239-109">Return value</span></span>

<span data-ttu-id="dd239-110">Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.</span><span class="sxs-lookup"><span data-stu-id="dd239-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="dd239-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="dd239-111">Return code</span></span>                                                                                           | <span data-ttu-id="dd239-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd239-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dd239-113"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="dd239-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="dd239-114">Error.</span><span class="sxs-lookup"><span data-stu-id="dd239-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="dd239-115"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="dd239-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="dd239-116">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="dd239-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="dd239-117"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="dd239-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="dd239-118">No se puede realizar la operación porque los PIN no están conectados.</span><span class="sxs-lookup"><span data-stu-id="dd239-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="dd239-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="dd239-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="dd239-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="dd239-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="dd239-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd239-121">Remarks</span></span>

<span data-ttu-id="dd239-122">Una aplicación puede cambiar los rectángulos de origen y de destino para el vídeo a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="dd239-122">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="dd239-123">El rectángulo de origen afecta a qué sección del origen de vídeo nativo aparecerá en la pantalla. el rectángulo de destino afecta al lugar en el que aparecerá el vídeo cuando se reproduzca.</span><span class="sxs-lookup"><span data-stu-id="dd239-123">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="dd239-124">El rectángulo de destino es relativo al área cliente de la ventana en la que se reproduce.</span><span class="sxs-lookup"><span data-stu-id="dd239-124">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="dd239-125">La esquina superior izquierda de la ventana es la coordenada (0,0).</span><span class="sxs-lookup"><span data-stu-id="dd239-125">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="dd239-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd239-126">Requirements</span></span>



| <span data-ttu-id="dd239-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd239-127">Requirement</span></span> | <span data-ttu-id="dd239-128">Value</span><span class="sxs-lookup"><span data-stu-id="dd239-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd239-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd239-129">Header</span></span><br/>  | <dl> <span data-ttu-id="dd239-130"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dd239-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dd239-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dd239-131">Library</span></span><br/> | <dl> <span data-ttu-id="dd239-132"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="dd239-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd239-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd239-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd239-134">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="dd239-134">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




