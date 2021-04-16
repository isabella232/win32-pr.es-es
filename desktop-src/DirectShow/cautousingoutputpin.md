---
description: La clase CAutoUsingOutputPin obtiene y libera el acceso a un objeto CDynamicOutputPin.
ms.assetid: 4ded5d18-4b14-4574-ad1f-73b886a51fac
title: Clase CAutoUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b664267ce2ff0dbbeeba8bc74708c9c67e185ae4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671479"
---
# <a name="cautousingoutputpin-class"></a><span data-ttu-id="bfa1a-103">Clase CAutoUsingOutputPin</span><span class="sxs-lookup"><span data-stu-id="bfa1a-103">CAutoUsingOutputPin class</span></span>

<span data-ttu-id="bfa1a-104">La clase **CAutoUsingOutputPin** obtiene y libera el acceso a un objeto [**CDynamicOutputPin**](cdynamicoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="bfa1a-104">The **CAutoUsingOutputPin** class obtains and releases access to a [**CDynamicOutputPin**](cdynamicoutputpin.md) object.</span></span>

<span data-ttu-id="bfa1a-105">**CAutoUsingOutputPin** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bfa1a-105">**CAutoUsingOutputPin** has these types of members:</span></span>



| <span data-ttu-id="bfa1a-106">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="bfa1a-106">Public Methods</span></span>                                                           | <span data-ttu-id="bfa1a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfa1a-107">Description</span></span>                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="bfa1a-108">**CAutoUsingOutputPin**</span><span class="sxs-lookup"><span data-stu-id="bfa1a-108">**CAutoUsingOutputPin**</span></span>](cautousingoutputpin-cautousingoutputpin.md)   | <span data-ttu-id="bfa1a-109">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="bfa1a-109">Constructor method.</span></span> <span data-ttu-id="bfa1a-110">Obtiene acceso al punto de conexión especificado.</span><span class="sxs-lookup"><span data-stu-id="bfa1a-110">Obtains access to the specified pin.</span></span> |
| [<span data-ttu-id="bfa1a-111">**~ CAutoUsingOutputPin**</span><span class="sxs-lookup"><span data-stu-id="bfa1a-111">**~CAutoUsingOutputPin**</span></span>](cautousingoutputpin--cautousingoutputpin.md) | <span data-ttu-id="bfa1a-112">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="bfa1a-112">Destructor method.</span></span> <span data-ttu-id="bfa1a-113">Obtiene acceso al punto de conexión especificado.</span><span class="sxs-lookup"><span data-stu-id="bfa1a-113">Obtains access to the specified pin.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="bfa1a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfa1a-114">Remarks</span></span>

<span data-ttu-id="bfa1a-115">Cuando se llama a determinados métodos en [**CDynamicOutputPin**](cdynamicoutputpin.md), el autor de la llamada debe obtener acceso al pin y, a continuación, liberar ese acceso.</span><span class="sxs-lookup"><span data-stu-id="bfa1a-115">When certain methods are called on [**CDynamicOutputPin**](cdynamicoutputpin.md), the caller must obtain access to the pin and then release that access.</span></span> <span data-ttu-id="bfa1a-116">Para obtener acceso, el llamador usa el método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="bfa1a-116">To obtain access, the caller uses the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method.</span></span> <span data-ttu-id="bfa1a-117">Para liberar el acceso, llama al método [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="bfa1a-117">To release access, it calls the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method.</span></span> <span data-ttu-id="bfa1a-118">La clase **CAutoUsingOutputPin** es una clase auxiliar que controla estas tareas en sus métodos de constructor y destructor.</span><span class="sxs-lookup"><span data-stu-id="bfa1a-118">The **CAutoUsingOutputPin** class is a helper class that handles these tasks in its constructor and destructor methods.</span></span> <span data-ttu-id="bfa1a-119">En el ejemplo de código siguiente se muestra cómo utilizar esta clase:</span><span class="sxs-lookup"><span data-stu-id="bfa1a-119">The following code example shows how to use this class:</span></span>


```
CDynamicOutputPin *pPin;
HRESULT hr = S_OK;  // Important! Initialize to S_OK.

// TODO: Obtain a pointer to the pin (not shown).

// Scope for lock.
{
    // Hold lock on pin.
    CAutoUsingOutputPin UsingPin(pPin, &hr)

    if (SUCCEEDED(hr)) 
    {

        // Safe to use the pin.
        hr = pPin->Deliver(pSample);

    }

} // Object goes out of scope here.

// No longer safe to use the pin.
```



## <a name="requirements"></a><span data-ttu-id="bfa1a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfa1a-120">Requirements</span></span>



| <span data-ttu-id="bfa1a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfa1a-121">Requirement</span></span> | <span data-ttu-id="bfa1a-122">Value</span><span class="sxs-lookup"><span data-stu-id="bfa1a-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfa1a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bfa1a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="bfa1a-124"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bfa1a-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bfa1a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bfa1a-125">Library</span></span><br/> | <dl> <span data-ttu-id="bfa1a-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bfa1a-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfa1a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfa1a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfa1a-128">Referencia de clase base</span><span class="sxs-lookup"><span data-stu-id="bfa1a-128">Base Class Reference</span></span>](base-class-reference.md)
</dt> </dl>

 

 




