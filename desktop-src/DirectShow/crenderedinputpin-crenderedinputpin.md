---
description: 'Constructor CRenderedInputPin.CRenderedInputPin: método constructor.'
ms.assetid: bf335750-b776-47bc-978d-e84e8b5259f7
title: Constructor CRenderedInputPin.CRenderedInputPin (Amextra.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4bd8e864531604fb36c2abe0bcd57ac5b3a9c869
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085403"
---
# <a name="crenderedinputpincrenderedinputpin-constructor"></a><span data-ttu-id="12a33-103">Constructor CRenderedInputPin.CRenderedInputPin</span><span class="sxs-lookup"><span data-stu-id="12a33-103">CRenderedInputPin.CRenderedInputPin constructor</span></span>

<span data-ttu-id="12a33-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="12a33-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="12a33-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12a33-105">Syntax</span></span>


```C++
CRenderedInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="12a33-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="12a33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12a33-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="12a33-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="12a33-108">Cadena que contiene el nombre de depuración del objeto.</span><span class="sxs-lookup"><span data-stu-id="12a33-108">String containing the debug name of the object.</span></span> <span data-ttu-id="12a33-109">Para obtener más información, vea [**CBaseObject (clase).**](cbaseobject.md)</span><span class="sxs-lookup"><span data-stu-id="12a33-109">For more information, see [**CBaseObject Class**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="12a33-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="12a33-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="12a33-111">Puntero al filtro que creó este pin.</span><span class="sxs-lookup"><span data-stu-id="12a33-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="12a33-112">*Plock*</span><span class="sxs-lookup"><span data-stu-id="12a33-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="12a33-113">Puntero a un [**bloqueo CCritSec,**](ccritsec.md) que se usa para serializar los cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="12a33-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="12a33-114">Puede ser la misma sección crítica que el bloqueo de filtro, [**CBaseFilter::m \_ pLock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="12a33-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="12a33-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="12a33-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="12a33-116">Puntero a una variable que recibe un **valor HRESULT** que indica el éxito o error del método.</span><span class="sxs-lookup"><span data-stu-id="12a33-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="12a33-117">*pName*</span><span class="sxs-lookup"><span data-stu-id="12a33-117">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="12a33-118">Cadena de caracteres anchos que contiene el nombre del pin (también se usa como identificador del pin).</span><span class="sxs-lookup"><span data-stu-id="12a33-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12a33-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12a33-119">Requirements</span></span>



| <span data-ttu-id="12a33-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="12a33-120">Requirement</span></span> | <span data-ttu-id="12a33-121">Value</span><span class="sxs-lookup"><span data-stu-id="12a33-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12a33-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12a33-122">Header</span></span><br/>  | <dl> <span data-ttu-id="12a33-123"><dt>Amextra.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="12a33-123"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="12a33-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12a33-124">Library</span></span><br/> | <dl> <span data-ttu-id="12a33-125"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="12a33-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12a33-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="12a33-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12a33-127">**CRenderedInputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="12a33-127">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




