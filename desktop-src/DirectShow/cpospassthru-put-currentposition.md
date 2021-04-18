---
description: El \_ método put CurrentPosition establece la posición actual, en relación con la duración total de la secuencia. Este método implementa el método IMediaPosition::p UT \_ CurrentPosition.
ms.assetid: 22d7e9e4-47da-45b5-9be0-3c5128f90353
title: Método CPosPassThru.put_CurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85426636a34d0e197b36496d5a38a847c61b9501
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681148"
---
# <a name="cpospassthruput_currentposition-method"></a><span data-ttu-id="1bd2c-104">CPosPassThru. put \_ CurrentPosition (método)</span><span class="sxs-lookup"><span data-stu-id="1bd2c-104">CPosPassThru.put\_CurrentPosition method</span></span>

<span data-ttu-id="1bd2c-105">El `put_CurrentPosition` método establece la posición actual, en relación con la duración total de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1bd2c-105">The `put_CurrentPosition` method sets the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="1bd2c-106">Este método implementa el método [**IMediaPosition::p UT \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) .</span><span class="sxs-lookup"><span data-stu-id="1bd2c-106">This method implements the [**IMediaPosition::put\_CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bd2c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1bd2c-107">Syntax</span></span>


```C++
HRESULT put_CurrentPosition(
   REFTIME llTime
);
```



## <a name="parameters"></a><span data-ttu-id="1bd2c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1bd2c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bd2c-109">*llTime*</span><span class="sxs-lookup"><span data-stu-id="1bd2c-109">*llTime*</span></span> 
</dt> <dd>

<span data-ttu-id="1bd2c-110">Nueva posición, en segundos.</span><span class="sxs-lookup"><span data-stu-id="1bd2c-110">New position, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bd2c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1bd2c-111">Return value</span></span>

<span data-ttu-id="1bd2c-112">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="1bd2c-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bd2c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bd2c-113">Requirements</span></span>



| <span data-ttu-id="1bd2c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bd2c-114">Requirement</span></span> | <span data-ttu-id="1bd2c-115">Value</span><span class="sxs-lookup"><span data-stu-id="1bd2c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bd2c-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1bd2c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1bd2c-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1bd2c-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1bd2c-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1bd2c-118">Library</span></span><br/> | <dl> <span data-ttu-id="1bd2c-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1bd2c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bd2c-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="1bd2c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bd2c-121">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="1bd2c-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




