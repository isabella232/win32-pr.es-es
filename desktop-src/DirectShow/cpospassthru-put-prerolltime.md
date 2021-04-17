---
description: El \_ método put PrerollTime establece la cantidad de datos que se pondrán en cola antes de la posición de inicio. Este método implementa el método IMediaPosition::p UT \_ PrerollTime.
ms.assetid: 5c35fb1d-2296-493f-8104-601127d7dd9f
title: Método CPosPassThru.put_PrerollTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bd4eddc7688373386147ea7999fdbd17f9af6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660815"
---
# <a name="cpospassthruput_prerolltime-method"></a><span data-ttu-id="aeb91-104">CPosPassThru. put \_ PrerollTime (método)</span><span class="sxs-lookup"><span data-stu-id="aeb91-104">CPosPassThru.put\_PrerollTime method</span></span>

<span data-ttu-id="aeb91-105">El `put_PrerollTime` método establece la cantidad de datos que se pondrán en cola antes de la posición inicial.</span><span class="sxs-lookup"><span data-stu-id="aeb91-105">The `put_PrerollTime` method sets the amount of data that will be queued before the start position.</span></span> <span data-ttu-id="aeb91-106">Este método implementa el método [**IMediaPosition::p UT \_ PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime) .</span><span class="sxs-lookup"><span data-stu-id="aeb91-106">This method implements the [**IMediaPosition::put\_PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeb91-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aeb91-107">Syntax</span></span>


```C++
HRESULT put_PrerollTime(
   REFTIME llTime
);
```



## <a name="parameters"></a><span data-ttu-id="aeb91-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aeb91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeb91-109">*llTime*</span><span class="sxs-lookup"><span data-stu-id="aeb91-109">*llTime*</span></span> 
</dt> <dd>

<span data-ttu-id="aeb91-110">Tiempo de preplantación, en segundos.</span><span class="sxs-lookup"><span data-stu-id="aeb91-110">Preroll time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aeb91-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aeb91-111">Return value</span></span>

<span data-ttu-id="aeb91-112">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="aeb91-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="aeb91-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aeb91-113">Requirements</span></span>



| <span data-ttu-id="aeb91-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="aeb91-114">Requirement</span></span> | <span data-ttu-id="aeb91-115">Value</span><span class="sxs-lookup"><span data-stu-id="aeb91-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeb91-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aeb91-116">Header</span></span><br/>  | <dl> <span data-ttu-id="aeb91-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aeb91-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aeb91-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aeb91-118">Library</span></span><br/> | <dl> <span data-ttu-id="aeb91-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="aeb91-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeb91-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="aeb91-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeb91-121">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="aeb91-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




