---
description: 'Constructor CBaseOutputPin.CBaseOutputPin: método constructor.'
ms.assetid: 1105c951-a51d-49ab-a69d-f3d482d61233
title: Constructor CBaseOutputPin.CBaseOutputPin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9901591be32d431ebe53a2098456446a0126d26b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099573"
---
# <a name="cbaseoutputpincbaseoutputpin-constructor"></a><span data-ttu-id="22421-103">Constructor CBaseOutputPin.CBaseOutputPin</span><span class="sxs-lookup"><span data-stu-id="22421-103">CBaseOutputPin.CBaseOutputPin constructor</span></span>

<span data-ttu-id="22421-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="22421-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="22421-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22421-105">Syntax</span></span>


```C++
CBaseOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="22421-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22421-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22421-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="22421-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="22421-108">Cadena que contiene el nombre de depuración del objeto.</span><span class="sxs-lookup"><span data-stu-id="22421-108">String containing the debug name of the object.</span></span> <span data-ttu-id="22421-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="22421-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="22421-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="22421-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="22421-111">Puntero al filtro que creó este pin.</span><span class="sxs-lookup"><span data-stu-id="22421-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="22421-112">*Plock*</span><span class="sxs-lookup"><span data-stu-id="22421-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="22421-113">Puntero a un [**bloqueo CCritSec,**](ccritsec.md) que se usa para serializar los cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="22421-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="22421-114">Puede ser la misma sección crítica que el bloqueo de filtro, [**CBaseFilter::m \_ pLock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="22421-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="22421-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="22421-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="22421-116">Puntero a una variable que recibe un **valor HRESULT** que indica el éxito o error del método.</span><span class="sxs-lookup"><span data-stu-id="22421-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="22421-117">*pName*</span><span class="sxs-lookup"><span data-stu-id="22421-117">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="22421-118">Cadena de caracteres anchos que contiene el nombre del pin (también se usa como identificador del pin).</span><span class="sxs-lookup"><span data-stu-id="22421-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22421-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="22421-119">Remarks</span></span>

<span data-ttu-id="22421-120">Todos los parámetros se pasan directamente al constructor [**CBasePin.**](cbasepin.md)</span><span class="sxs-lookup"><span data-stu-id="22421-120">All of the parameters are passed directly to the [**CBasePin**](cbasepin.md) constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="22421-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22421-121">Requirements</span></span>



| <span data-ttu-id="22421-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="22421-122">Requirement</span></span> | <span data-ttu-id="22421-123">Value</span><span class="sxs-lookup"><span data-stu-id="22421-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22421-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22421-124">Header</span></span><br/>  | <dl> <span data-ttu-id="22421-125"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="22421-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="22421-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="22421-126">Library</span></span><br/> | <dl> <span data-ttu-id="22421-127"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="22421-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22421-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="22421-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22421-129">**CBaseOutputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="22421-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




