---
description: 'El método SKIP omite un número especificado de PIN en la secuencia de enumeración. Este método implementa el método IEnumPins:: SKIP.'
ms.assetid: d42f958c-f488-4730-ab84-fc4e4150b186
title: CEnumPins. SKIP (método) (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1865453a89130303f28f338d8b7567e856c64173
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671153"
---
# <a name="cenumpinsskip-method"></a><span data-ttu-id="8d7a6-104">CEnumPins. SKIP (método)</span><span class="sxs-lookup"><span data-stu-id="8d7a6-104">CEnumPins.Skip method</span></span>

<span data-ttu-id="8d7a6-105">El `Skip` método omite un número especificado de PIN en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="8d7a6-105">The `Skip` method skips over a specified number of pins in the enumeration sequence.</span></span> <span data-ttu-id="8d7a6-106">Este método implementa el método [**IEnumPins:: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip) .</span><span class="sxs-lookup"><span data-stu-id="8d7a6-106">This method implements the [**IEnumPins::Skip**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d7a6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d7a6-107">Syntax</span></span>


```C++
HRESULT Skip(
   ULONG cPins
);
```



## <a name="parameters"></a><span data-ttu-id="8d7a6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d7a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d7a6-109">*cPins*</span><span class="sxs-lookup"><span data-stu-id="8d7a6-109">*cPins*</span></span> 
</dt> <dd>

<span data-ttu-id="8d7a6-110">Número de clavijas que se van a omitir.</span><span class="sxs-lookup"><span data-stu-id="8d7a6-110">Number of pins to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d7a6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d7a6-111">Return value</span></span>

<span data-ttu-id="8d7a6-112">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8d7a6-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="8d7a6-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8d7a6-113">Return code</span></span>                                                                                                | <span data-ttu-id="8d7a6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d7a6-114">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8d7a6-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="8d7a6-115"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="8d7a6-116">Se omitió más allá del final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="8d7a6-116">Skipped past the end of the sequence.</span></span><br/>                                       |
| <dl> <span data-ttu-id="8d7a6-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8d7a6-117"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="8d7a6-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="8d7a6-118">Success.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="8d7a6-119"><dt>**\_ \_ enumeración de VFW E no \_ \_ \_ sincronizada**</dt></span><span class="sxs-lookup"><span data-stu-id="8d7a6-119"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="8d7a6-120">El estado del filtro ha cambiado y ahora es incoherente con el enumerador.</span><span class="sxs-lookup"><span data-stu-id="8d7a6-120">The filter's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8d7a6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d7a6-121">Requirements</span></span>



| <span data-ttu-id="8d7a6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d7a6-122">Requirement</span></span> | <span data-ttu-id="8d7a6-123">Value</span><span class="sxs-lookup"><span data-stu-id="8d7a6-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d7a6-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d7a6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8d7a6-125"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d7a6-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8d7a6-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8d7a6-126">Library</span></span><br/> | <dl> <span data-ttu-id="8d7a6-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8d7a6-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d7a6-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d7a6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d7a6-129">**Clase CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="8d7a6-129">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




