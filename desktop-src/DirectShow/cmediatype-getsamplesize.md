---
description: El método GetSampleSize recupera el tamaño de la muestra.
ms.assetid: 5cc98556-cca6-46ca-ad33-cd40011ff6f4
title: Método CMediaType. GetSampleSize (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.GetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc5b80e20ad2a16af9c25c68499348ffa744c0fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670318"
---
# <a name="cmediatypegetsamplesize-method"></a><span data-ttu-id="28352-103">CMediaType. GetSampleSize, método</span><span class="sxs-lookup"><span data-stu-id="28352-103">CMediaType.GetSampleSize method</span></span>

<span data-ttu-id="28352-104">El `GetSampleSize` método recupera el tamaño de la muestra.</span><span class="sxs-lookup"><span data-stu-id="28352-104">The `GetSampleSize` method retrieves the sample size.</span></span>

## <a name="syntax"></a><span data-ttu-id="28352-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28352-105">Syntax</span></span>


```C++
ULONG GetSampleSize() const;
```



## <a name="parameters"></a><span data-ttu-id="28352-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28352-106">Parameters</span></span>

<span data-ttu-id="28352-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="28352-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28352-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28352-108">Return value</span></span>

<span data-ttu-id="28352-109">Si el tamaño de la muestra es fijo, devuelve el tamaño de ejemplo en bytes.</span><span class="sxs-lookup"><span data-stu-id="28352-109">If the sample size is fixed, returns the sample size in bytes.</span></span> <span data-ttu-id="28352-110">De lo contrario, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="28352-110">Otherwise, returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="28352-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28352-111">Requirements</span></span>



| <span data-ttu-id="28352-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="28352-112">Requirement</span></span> | <span data-ttu-id="28352-113">Value</span><span class="sxs-lookup"><span data-stu-id="28352-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28352-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28352-114">Header</span></span><br/>  | <dl> <span data-ttu-id="28352-115"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28352-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="28352-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="28352-116">Library</span></span><br/> | <dl> <span data-ttu-id="28352-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="28352-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28352-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="28352-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28352-119">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="28352-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




