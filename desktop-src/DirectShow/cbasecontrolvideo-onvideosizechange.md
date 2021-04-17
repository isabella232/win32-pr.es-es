---
description: Pasa un \_ \_ mensaje de tamaño de vídeo \_ de EC cambiado al administrador de gráficos de filtro.
ms.assetid: 39cb4f30-c12d-49bd-8d8a-70bf686b680d
title: Método CBaseControlVideo. OnVideoSizeChange (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.OnVideoSizeChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37caa05d164c23484c749730796d6a5f10d67d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670383"
---
# <a name="cbasecontrolvideoonvideosizechange-method"></a><span data-ttu-id="48e79-103">CBaseControlVideo. OnVideoSizeChange, método</span><span class="sxs-lookup"><span data-stu-id="48e79-103">CBaseControlVideo.OnVideoSizeChange method</span></span>

<span data-ttu-id="48e79-104">Pasa un \_ \_ mensaje de tamaño de vídeo \_ de EC cambiado al administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="48e79-104">Passes an EC\_VIDEO\_SIZE\_CHANGED message to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="48e79-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48e79-105">Syntax</span></span>


```C++
virtual HRESULT OnVideoSizeChange();
```



## <a name="parameters"></a><span data-ttu-id="48e79-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48e79-106">Parameters</span></span>

<span data-ttu-id="48e79-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="48e79-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="48e79-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48e79-108">Return value</span></span>

<span data-ttu-id="48e79-109">Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.</span><span class="sxs-lookup"><span data-stu-id="48e79-109">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="48e79-110">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="48e79-110">Return code</span></span>                                                                                   | <span data-ttu-id="48e79-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="48e79-111">Description</span></span>               |
|-----------------------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="48e79-112"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="48e79-112"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="48e79-113">Error.</span><span class="sxs-lookup"><span data-stu-id="48e79-113">Failure.</span></span><br/>       |
| <dl> <span data-ttu-id="48e79-114"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="48e79-114"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="48e79-115">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="48e79-115">Out of memory.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="48e79-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48e79-116">Remarks</span></span>

<span data-ttu-id="48e79-117">Un representador de vídeo debe llamar a esta función miembro cada vez que se cambia el tamaño del vídeo; Normalmente, se llamará una vez después de la conexión inicial.</span><span class="sxs-lookup"><span data-stu-id="48e79-117">A video renderer should call this member function each time the video size is changed; this will typically be called once after initial connection.</span></span> <span data-ttu-id="48e79-118">Si el representador puede admitir cambios de formato dinámico (de 320 x 240 a 160 x 120), también debe llamarlo después de cada cambio.</span><span class="sxs-lookup"><span data-stu-id="48e79-118">If the renderer can support dynamic format changes (from 320 x 240 to 160 x 120), it should also call it after each change.</span></span>

## <a name="requirements"></a><span data-ttu-id="48e79-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48e79-119">Requirements</span></span>



| <span data-ttu-id="48e79-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="48e79-120">Requirement</span></span> | <span data-ttu-id="48e79-121">Value</span><span class="sxs-lookup"><span data-stu-id="48e79-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48e79-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48e79-122">Header</span></span><br/>  | <dl> <span data-ttu-id="48e79-123"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48e79-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="48e79-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="48e79-124">Library</span></span><br/> | <dl> <span data-ttu-id="48e79-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="48e79-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48e79-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="48e79-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48e79-127">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="48e79-127">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




