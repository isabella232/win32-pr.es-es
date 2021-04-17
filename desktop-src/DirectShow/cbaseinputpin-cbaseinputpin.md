---
description: Método de constructor.
ms.assetid: a853813d-cdf6-4cb4-8288-62685a883b56
title: Constructor CBaseInputPin. CBaseInputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 554c768f2cb99fda77aa87cfc916580b948da0ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661097"
---
# <a name="cbaseinputpincbaseinputpin-constructor"></a><span data-ttu-id="01802-103">Constructor CBaseInputPin. CBaseInputPin</span><span class="sxs-lookup"><span data-stu-id="01802-103">CBaseInputPin.CBaseInputPin constructor</span></span>

<span data-ttu-id="01802-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="01802-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="01802-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01802-105">Syntax</span></span>


```C++
CBaseInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pPinName
);
```



## <a name="parameters"></a><span data-ttu-id="01802-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01802-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01802-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="01802-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="01802-108">Cadena que contiene el nombre de depuración del objeto.</span><span class="sxs-lookup"><span data-stu-id="01802-108">String containing the debug name of the object.</span></span> <span data-ttu-id="01802-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="01802-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="01802-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="01802-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="01802-111">Puntero al filtro que creó este pin.</span><span class="sxs-lookup"><span data-stu-id="01802-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="01802-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="01802-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="01802-113">Puntero a un bloqueo de [**CCritSec**](ccritsec.md) , que se usa para serializar los cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="01802-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="01802-114">Puede ser la misma sección crítica que el bloqueo de filtro, [**CBaseFilter:: m \_ Plock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="01802-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="01802-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="01802-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="01802-116">Puntero a una variable que recibe un valor **HRESULT** que indica si el método se ha ejecutado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="01802-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="01802-117">*pPinName*</span><span class="sxs-lookup"><span data-stu-id="01802-117">*pPinName*</span></span> 
</dt> <dd>

<span data-ttu-id="01802-118">Cadena de caracteres anchos que contiene el nombre del PIN (también se usa como identificador del PIN).</span><span class="sxs-lookup"><span data-stu-id="01802-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01802-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01802-119">Remarks</span></span>

<span data-ttu-id="01802-120">Todos los parámetros se pasan directamente al constructor [**CBasePin**](cbasepin-cbasepin.md) .</span><span class="sxs-lookup"><span data-stu-id="01802-120">All of the parameters are passed directly to the [**CBasePin**](cbasepin-cbasepin.md) constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="01802-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01802-121">Requirements</span></span>



| <span data-ttu-id="01802-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="01802-122">Requirement</span></span> | <span data-ttu-id="01802-123">Value</span><span class="sxs-lookup"><span data-stu-id="01802-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01802-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01802-124">Header</span></span><br/>  | <dl> <span data-ttu-id="01802-125"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01802-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="01802-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01802-126">Library</span></span><br/> | <dl> <span data-ttu-id="01802-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="01802-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01802-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="01802-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01802-129">**Clase CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="01802-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




