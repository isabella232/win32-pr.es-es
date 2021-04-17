---
description: 'El método SKIP omite un número especificado de tipos de medios. Este método implementa el método IEnumMediaTypes:: SKIP.'
ms.assetid: a01fb084-b227-4ca6-b5ca-c57d56e8b1aa
title: CEnumMediaTypes. SKIP (método) (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e09217bc45b866cfb08aa2ab0cae5a7a28815fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660866"
---
# <a name="cenummediatypesskip-method"></a><span data-ttu-id="1c5f7-104">CEnumMediaTypes. SKIP (método)</span><span class="sxs-lookup"><span data-stu-id="1c5f7-104">CEnumMediaTypes.Skip method</span></span>

<span data-ttu-id="1c5f7-105">El `Skip` método omite un número especificado de tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-105">The `Skip` method skips over a specified number of media types.</span></span> <span data-ttu-id="1c5f7-106">Este método implementa el método [**IEnumMediaTypes:: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip) .</span><span class="sxs-lookup"><span data-stu-id="1c5f7-106">This method implements the [**IEnumMediaTypes::Skip**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c5f7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c5f7-107">Syntax</span></span>


```C++
HRESULT Skip(
   ULONG cMediaTypes
);
```



## <a name="parameters"></a><span data-ttu-id="1c5f7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c5f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c5f7-109">*cMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="1c5f7-109">*cMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="1c5f7-110">Número de tipos de medios que se van a omitir.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-110">Number of media types to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c5f7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c5f7-111">Return value</span></span>

<span data-ttu-id="1c5f7-112">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="1c5f7-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1c5f7-113">Return code</span></span>                                                                                                | <span data-ttu-id="1c5f7-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c5f7-114">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1c5f7-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="1c5f7-115"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="1c5f7-116">Se omitió más allá del final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-116">Skipped past the end of the sequence.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1c5f7-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1c5f7-117"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="1c5f7-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-118">Success.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="1c5f7-119"><dt>**\_ \_ enumeración de VFW E no \_ \_ \_ sincronizada**</dt></span><span class="sxs-lookup"><span data-stu-id="1c5f7-119"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="1c5f7-120">El estado del PIN ha cambiado y ahora es incoherente con el enumerador.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-120">The pin's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1c5f7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c5f7-121">Requirements</span></span>



| <span data-ttu-id="1c5f7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c5f7-122">Requirement</span></span> | <span data-ttu-id="1c5f7-123">Value</span><span class="sxs-lookup"><span data-stu-id="1c5f7-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c5f7-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c5f7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1c5f7-125"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c5f7-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1c5f7-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1c5f7-126">Library</span></span><br/> | <dl> <span data-ttu-id="1c5f7-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1c5f7-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c5f7-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c5f7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c5f7-129">**Clase CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="1c5f7-129">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




