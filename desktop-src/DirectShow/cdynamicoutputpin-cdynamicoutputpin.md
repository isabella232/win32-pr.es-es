---
description: Método de constructor.
ms.assetid: 996adc69-8727-431e-a7f5-8fbcc0e305ae
title: Constructor CDynamicOutputPin. CDynamicOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CDynamicOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f45a2fee25796f39c7d8b358b1ac83e4a5b1daa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671757"
---
# <a name="cdynamicoutputpincdynamicoutputpin-constructor"></a><span data-ttu-id="f8008-103">Constructor CDynamicOutputPin. CDynamicOutputPin</span><span class="sxs-lookup"><span data-stu-id="f8008-103">CDynamicOutputPin.CDynamicOutputPin constructor</span></span>

<span data-ttu-id="f8008-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="f8008-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8008-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8008-105">Syntax</span></span>


```C++
CDynamicOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="f8008-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8008-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8008-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="f8008-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="f8008-108">Puntero a una cadena que contiene el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="f8008-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="f8008-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="f8008-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8008-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="f8008-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="f8008-111">Puntero al filtro que creó este pin.</span><span class="sxs-lookup"><span data-stu-id="f8008-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="f8008-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="f8008-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="f8008-113">Puntero a un bloqueo de [**CCritSec**](ccritsec.md) , que se usa para serializar los cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="f8008-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="f8008-114">Use la misma sección crítica que el bloqueo de filtro, [ **CBaseFilter:: m \_ Plock**](cbasefilter-m-plock.md)</span><span class="sxs-lookup"><span data-stu-id="f8008-114">Use the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md)</span></span>

</dd> <dt>

<span data-ttu-id="f8008-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="f8008-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="f8008-116">Puntero a una variable que recibe un valor **HRESULT** que indica si el método se ha ejecutado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="f8008-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="f8008-117">Inicialice el valor a S \_ OK antes de crear el objeto.</span><span class="sxs-lookup"><span data-stu-id="f8008-117">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="f8008-118">Solo se cambia el valor si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="f8008-118">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="f8008-119">*pName*</span><span class="sxs-lookup"><span data-stu-id="f8008-119">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="f8008-120">Puntero a una cadena de caracteres anchos que contiene el identificador del PIN.</span><span class="sxs-lookup"><span data-stu-id="f8008-120">Pointer to a wide-character string containing the pin identifier.</span></span> <span data-ttu-id="f8008-121">Para obtener más información, vea [**IPin:: queryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).</span><span class="sxs-lookup"><span data-stu-id="f8008-121">For more information, see [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f8008-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8008-122">Requirements</span></span>



| <span data-ttu-id="f8008-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8008-123">Requirement</span></span> | <span data-ttu-id="f8008-124">Value</span><span class="sxs-lookup"><span data-stu-id="f8008-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8008-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8008-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f8008-126"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8008-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f8008-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f8008-127">Library</span></span><br/> | <dl> <span data-ttu-id="f8008-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f8008-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8008-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8008-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8008-130">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="f8008-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




