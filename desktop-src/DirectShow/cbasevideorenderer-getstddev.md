---
description: El método GetStdDev calcula la desviación estándar en milisegundos entre el momento en que vence cada fotograma y el momento en que se representa, para las estadísticas por fotograma.
ms.assetid: 1a4d5c8d-38de-434f-b218-412d45976b8c
title: Método CBaseVideoRenderer. GetStdDev (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.GetStdDev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85b40bda4715a8201cd05109b59746630c54654c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660379"
---
# <a name="cbasevideorenderergetstddev-method"></a><span data-ttu-id="afb98-103">CBaseVideoRenderer. GetStdDev, método</span><span class="sxs-lookup"><span data-stu-id="afb98-103">CBaseVideoRenderer.GetStdDev method</span></span>

<span data-ttu-id="afb98-104">El `GetStdDev` método calcula la desviación estándar en milisegundos entre el momento en que vence cada fotograma y el momento en que se representa, para las estadísticas por fotograma.</span><span class="sxs-lookup"><span data-stu-id="afb98-104">The `GetStdDev` method estimates the standard deviation in milliseconds between when each frame is due and when it is actually rendered, for per-frame statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="afb98-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="afb98-105">Syntax</span></span>


```C++
HRESULT GetStdDev(
   int      nSamples,
   int      *piResult,
   LONGLONG llSumSq,
   LONGLONG iTot
);
```



## <a name="parameters"></a><span data-ttu-id="afb98-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="afb98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afb98-107">*nSamples*</span><span class="sxs-lookup"><span data-stu-id="afb98-107">*nSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="afb98-108">Valor entero que contiene el número de muestras de vídeo recibidas por el representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="afb98-108">Integer value that contains the number of video samples received by the video renderer.</span></span>

</dd> <dt>

<span data-ttu-id="afb98-109">*piResult*</span><span class="sxs-lookup"><span data-stu-id="afb98-109">*piResult*</span></span> 
</dt> <dd>

<span data-ttu-id="afb98-110">Puntero a un valor entero que contendrá la desviación estándar.</span><span class="sxs-lookup"><span data-stu-id="afb98-110">Pointer to an integer value that will contain the standard deviation.</span></span>

</dd> <dt>

<span data-ttu-id="afb98-111">*llSumSq*</span><span class="sxs-lookup"><span data-stu-id="afb98-111">*llSumSq*</span></span> 
</dt> <dd>

<span data-ttu-id="afb98-112">Valor que representa la desviación estándar, en milisegundos, de todos los ejemplos de vídeo representados.</span><span class="sxs-lookup"><span data-stu-id="afb98-112">Value that represents the standard deviation, in milliseconds, of all rendered video samples.</span></span> <span data-ttu-id="afb98-113">Cuanto menor sea el valor, más coherente será la representación.</span><span class="sxs-lookup"><span data-stu-id="afb98-113">The lower the value, the more consistent the rendering.</span></span>

</dd> <dt>

<span data-ttu-id="afb98-114">*iTot*</span><span class="sxs-lookup"><span data-stu-id="afb98-114">*iTot*</span></span> 
</dt> <dd>

<span data-ttu-id="afb98-115">Valor que representa el valor medio, en milisegundos, entre el tiempo marcado y el tiempo de representación de todos los ejemplos de vídeo representados.</span><span class="sxs-lookup"><span data-stu-id="afb98-115">Value that represents the mean value, in milliseconds, between the stamped time and rendered time for all rendered video samples.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afb98-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="afb98-116">Return value</span></span>

<span data-ttu-id="afb98-117">Devuelve NoError.</span><span class="sxs-lookup"><span data-stu-id="afb98-117">Returns NOERROR.</span></span>

## <a name="requirements"></a><span data-ttu-id="afb98-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afb98-118">Requirements</span></span>



| <span data-ttu-id="afb98-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="afb98-119">Requirement</span></span> | <span data-ttu-id="afb98-120">Value</span><span class="sxs-lookup"><span data-stu-id="afb98-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afb98-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="afb98-121">Header</span></span><br/>  | <dl> <span data-ttu-id="afb98-122"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="afb98-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="afb98-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="afb98-123">Library</span></span><br/> | <dl> <span data-ttu-id="afb98-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="afb98-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afb98-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="afb98-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afb98-126">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="afb98-126">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




