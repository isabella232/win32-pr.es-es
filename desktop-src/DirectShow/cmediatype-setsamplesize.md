---
description: El método SetSampleSize especifica un tamaño de muestra fijo o especifica que los ejemplos tienen un tamaño variable.
ms.assetid: b0f9dd7b-4ff9-4d11-9c13-b52d7b1549b5
title: Método CMediaType. SetSampleSize (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0992afd0576c1039397e6ecaa2119a989283136e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680286"
---
# <a name="cmediatypesetsamplesize-method"></a><span data-ttu-id="2a9c9-103">CMediaType. SetSampleSize, método</span><span class="sxs-lookup"><span data-stu-id="2a9c9-103">CMediaType.SetSampleSize method</span></span>

<span data-ttu-id="2a9c9-104">El `SetSampleSize` método especifica un tamaño de muestra fijo o especifica que los ejemplos tienen un tamaño variable.</span><span class="sxs-lookup"><span data-stu-id="2a9c9-104">The `SetSampleSize` method specifies a fixed sample size, or specifies that samples have a variable size.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a9c9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a9c9-105">Syntax</span></span>


```C++
void SetSampleSize(
   ULONG sz
);
```



## <a name="parameters"></a><span data-ttu-id="2a9c9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a9c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a9c9-107">*SZ*</span><span class="sxs-lookup"><span data-stu-id="2a9c9-107">*sz*</span></span> 
</dt> <dd>

<span data-ttu-id="2a9c9-108">Tamaño de muestra, en bytes o cero.</span><span class="sxs-lookup"><span data-stu-id="2a9c9-108">Sample size, in bytes, or zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a9c9-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a9c9-109">Return value</span></span>

<span data-ttu-id="2a9c9-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2a9c9-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a9c9-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a9c9-111">Remarks</span></span>

<span data-ttu-id="2a9c9-112">Si el valor de *SZ* es cero, el tipo de medio usa tamaños de muestra variables.</span><span class="sxs-lookup"><span data-stu-id="2a9c9-112">If value of *sz* is zero, the media type uses variable sample sizes.</span></span> <span data-ttu-id="2a9c9-113">De lo contrario, el tamaño de la muestra se fija en *SZ* bytes.</span><span class="sxs-lookup"><span data-stu-id="2a9c9-113">Otherwise, the sample size is fixed at *sz* bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a9c9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a9c9-114">Requirements</span></span>



| <span data-ttu-id="2a9c9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a9c9-115">Requirement</span></span> | <span data-ttu-id="2a9c9-116">Value</span><span class="sxs-lookup"><span data-stu-id="2a9c9-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a9c9-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a9c9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2a9c9-118"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a9c9-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="2a9c9-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2a9c9-119">Library</span></span><br/> | <dl> <span data-ttu-id="2a9c9-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2a9c9-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a9c9-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a9c9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a9c9-122">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="2a9c9-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




