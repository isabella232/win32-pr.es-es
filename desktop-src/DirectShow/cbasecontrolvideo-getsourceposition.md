---
description: El método GetSourcePosition recupera la posición y las dimensiones del rectángulo de origen en una operación atómica.
ms.assetid: 44356f62-8b14-4b0e-a587-f832adff3bba
title: Método CBaseControlVideo. GetSourcePosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2422845a7b5c64bc07b8e8942b2f19cd10a54d26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661406"
---
# <a name="cbasecontrolvideogetsourceposition-method"></a><span data-ttu-id="fceac-103">CBaseControlVideo. GetSourcePosition, método</span><span class="sxs-lookup"><span data-stu-id="fceac-103">CBaseControlVideo.GetSourcePosition method</span></span>

<span data-ttu-id="fceac-104">El `GetSourcePosition` método recupera la posición y las dimensiones del rectángulo de origen en una operación atómica.</span><span class="sxs-lookup"><span data-stu-id="fceac-104">The `GetSourcePosition` method retrieves the position and dimensions of the source rectangle in one atomic operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fceac-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fceac-105">Syntax</span></span>


```C++
HRESULT GetSourcePosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="fceac-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fceac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fceac-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="fceac-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="fceac-108">Puntero a la coordenada izquierda del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="fceac-108">Pointer to the left coordinate of the source rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="fceac-109">*pTop*</span><span class="sxs-lookup"><span data-stu-id="fceac-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="fceac-110">Puntero a la coordenada superior del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="fceac-110">Pointer to the top coordinate of the source rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="fceac-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="fceac-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="fceac-112">Puntero al ancho del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="fceac-112">Pointer to the width of the source rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="fceac-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="fceac-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="fceac-114">Puntero al alto del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="fceac-114">Pointer to the height of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fceac-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fceac-115">Return value</span></span>

<span data-ttu-id="fceac-116">Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.</span><span class="sxs-lookup"><span data-stu-id="fceac-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="fceac-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fceac-117">Return code</span></span>                                                                                           | <span data-ttu-id="fceac-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="fceac-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fceac-119"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="fceac-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="fceac-120">Error.</span><span class="sxs-lookup"><span data-stu-id="fceac-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="fceac-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="fceac-121"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="fceac-122">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="fceac-122">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="fceac-123"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="fceac-123"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="fceac-124">No se puede realizar la operación porque los PIN no están conectados.</span><span class="sxs-lookup"><span data-stu-id="fceac-124">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="fceac-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="fceac-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="fceac-126">Correcto.</span><span class="sxs-lookup"><span data-stu-id="fceac-126">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="fceac-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fceac-127">Remarks</span></span>

<span data-ttu-id="fceac-128">Una aplicación puede cambiar los rectángulos de origen y de destino para el vídeo a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="fceac-128">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="fceac-129">El rectángulo de origen afecta a qué sección del origen de vídeo nativo aparecerá en la pantalla. el rectángulo de destino afecta al lugar en el que aparecerá el vídeo cuando se reproduzca.</span><span class="sxs-lookup"><span data-stu-id="fceac-129">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="fceac-130">El rectángulo de destino es relativo al área cliente de la ventana en la que se reproduce.</span><span class="sxs-lookup"><span data-stu-id="fceac-130">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="fceac-131">La esquina superior izquierda de la ventana es la coordenada (0,0).</span><span class="sxs-lookup"><span data-stu-id="fceac-131">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="fceac-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fceac-132">Requirements</span></span>



| <span data-ttu-id="fceac-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="fceac-133">Requirement</span></span> | <span data-ttu-id="fceac-134">Value</span><span class="sxs-lookup"><span data-stu-id="fceac-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fceac-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fceac-135">Header</span></span><br/>  | <dl> <span data-ttu-id="fceac-136"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fceac-136"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fceac-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fceac-137">Library</span></span><br/> | <dl> <span data-ttu-id="fceac-138"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="fceac-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fceac-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="fceac-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fceac-140">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="fceac-140">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




