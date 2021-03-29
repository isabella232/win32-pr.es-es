---
description: El \_ método de velocidad Put establece la velocidad de reproducción. Este método implementa el método de velocidad IMediaPosition::p UT \_ .
ms.assetid: c077f344-de34-4f8a-8e08-6d7086a5a4f1
title: Método CPosPassThru.put_Rate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21e7e654233f78adcda2addf73b87a178654872e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678930"
---
# <a name="cpospassthruput_rate-method"></a><span data-ttu-id="15373-104">CPosPassThru. put ( \_ método de tasa)</span><span class="sxs-lookup"><span data-stu-id="15373-104">CPosPassThru.put\_Rate method</span></span>

<span data-ttu-id="15373-105">El `put_Rate` método establece la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="15373-105">The `put_Rate` method sets the playback rate.</span></span> <span data-ttu-id="15373-106">Este método implementa el método de [**\_ velocidad IMediaPosition::p UT**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate) .</span><span class="sxs-lookup"><span data-stu-id="15373-106">This method implements the [**IMediaPosition::put\_Rate**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="15373-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15373-107">Syntax</span></span>


```C++
HRESULT put_Rate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="15373-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15373-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15373-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="15373-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="15373-110">Velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="15373-110">Playback rate.</span></span> <span data-ttu-id="15373-111">No debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="15373-111">Must not be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15373-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="15373-112">Return value</span></span>

<span data-ttu-id="15373-113">Devuelve E \_ INVALIDARG si *dRate* es cero.</span><span class="sxs-lookup"><span data-stu-id="15373-113">Returns E\_INVALIDARG if *dRate* is zero.</span></span> <span data-ttu-id="15373-114">De lo contrario, devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="15373-114">Otherwise, returns the **HRESULT** value from the connected pin.</span></span>

## <a name="remarks"></a><span data-ttu-id="15373-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15373-115">Remarks</span></span>

<span data-ttu-id="15373-116">Los tipos negativos indican reproducción inversa.</span><span class="sxs-lookup"><span data-stu-id="15373-116">Negative rates indicate reverse play.</span></span> <span data-ttu-id="15373-117">No todos los medios serán compatibles con la reproducción inversa.</span><span class="sxs-lookup"><span data-stu-id="15373-117">Not all media will support reverse play.</span></span>

## <a name="requirements"></a><span data-ttu-id="15373-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15373-118">Requirements</span></span>



| <span data-ttu-id="15373-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="15373-119">Requirement</span></span> | <span data-ttu-id="15373-120">Value</span><span class="sxs-lookup"><span data-stu-id="15373-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15373-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15373-121">Header</span></span><br/>  | <dl> <span data-ttu-id="15373-122"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15373-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="15373-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="15373-123">Library</span></span><br/> | <dl> <span data-ttu-id="15373-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="15373-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15373-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="15373-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15373-126">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="15373-126">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




