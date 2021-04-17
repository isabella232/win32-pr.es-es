---
description: 'Asigna una sola función miembro y un conjunto opcional de parámetros a un conjunto correspondiente de identificadores de envío enteros, que se puede usar en las llamadas subsiguientes a la función miembro CMediaEvent:: Invoke.'
ms.assetid: 04e607e6-0b68-4371-aacf-01af308a56a3
title: Método CMediaEvent. GetIDsOfNames (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 191fa85264e4e7e22aa67f409db20cebd68f4319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681015"
---
# <a name="cmediaeventgetidsofnames-method"></a><span data-ttu-id="6c5a1-103">CMediaEvent. GetIDsOfNames (método)</span><span class="sxs-lookup"><span data-stu-id="6c5a1-103">CMediaEvent.GetIDsOfNames method</span></span>

<span data-ttu-id="6c5a1-104">Asigna una sola función miembro y un conjunto opcional de parámetros a un conjunto correspondiente de identificadores de envío enteros, que se puede usar en las llamadas subsiguientes a la función miembro [**CMediaEvent:: Invoke**](cmediaevent-invoke.md) .</span><span class="sxs-lookup"><span data-stu-id="6c5a1-104">Maps a single member function and an optional set of parameters to a corresponding set of integer dispatch identifiers, which can be used upon subsequent calls to the [**CMediaEvent::Invoke**](cmediaevent-invoke.md) member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c5a1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c5a1-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="6c5a1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c5a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c5a1-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="6c5a1-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="6c5a1-108">Identificador de referencia.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-108">Reference identifier.</span></span> <span data-ttu-id="6c5a1-109">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-109">Reserved for future use.</span></span> <span data-ttu-id="6c5a1-110">Debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-110">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6c5a1-111">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="6c5a1-111">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="6c5a1-112">Dirección de un puntero a una matriz de nombres pasada que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-112">Address of a pointer to a passed-in array of names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="6c5a1-113">*CNAME*</span><span class="sxs-lookup"><span data-stu-id="6c5a1-113">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="6c5a1-114">Número de nombres que se van a asignar.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-114">Count of the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="6c5a1-115">*lcid*</span><span class="sxs-lookup"><span data-stu-id="6c5a1-115">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="6c5a1-116">Contexto de configuración regional en el que se van a interpretar los nombres.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-116">Locale context in which to interpret the names.</span></span>

</dd> <dt>

<span data-ttu-id="6c5a1-117">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="6c5a1-117">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="6c5a1-118">Puntero a una matriz asignada por el llamador, donde cada elemento contiene un identificador que corresponde a uno de los nombres pasados en la matriz *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="6c5a1-118">Pointer to a caller-allocated array, each element of which contains an ID corresponding to one of the names passed in the *rgszNames* array.</span></span> <span data-ttu-id="6c5a1-119">El primer elemento representa el nombre del miembro; los elementos siguientes representan cada uno de los parámetros del miembro.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-119">The first element represents the member name; the subsequent elements represent each of the member's parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c5a1-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c5a1-120">Return value</span></span>

<span data-ttu-id="6c5a1-121">Devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-121">Returns one of the following values.</span></span>



| <span data-ttu-id="6c5a1-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6c5a1-122">Return code</span></span>                                                                                            | <span data-ttu-id="6c5a1-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c5a1-123">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c5a1-124"><dt>**DISP \_ . \_ \_ CLSID desconocido**</dt></span><span class="sxs-lookup"><span data-stu-id="6c5a1-124"><dt>**DISP\_E\_UNKNOWN\_CLSID**</dt></span></span> </dl> | <span data-ttu-id="6c5a1-125">No se reconoció el CLSID.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-125">The CLSID was not recognized.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="6c5a1-126"><dt>**DISP \_ E \_ UNKNOWNNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="6c5a1-126"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl>    | <span data-ttu-id="6c5a1-127">No se conocían uno o varios de los nombres.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-127">One or more of the names were not known.</span></span> <span data-ttu-id="6c5a1-128">Los DISPID devueltos contienen un DISPID \_ desconocido para cada entrada que corresponde a un nombre desconocido.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-128">The returned DISPIDs contain DISPID\_UNKNOWN for each entry that corresponds to an unknown name.</span></span><br/> |
| <dl> <span data-ttu-id="6c5a1-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6c5a1-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="6c5a1-130">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="6c5a1-130">Out of memory.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="6c5a1-131"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6c5a1-131"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="6c5a1-132">Correcto.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-132">Success.</span></span><br/>                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="6c5a1-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c5a1-133">Requirements</span></span>



| <span data-ttu-id="6c5a1-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c5a1-134">Requirement</span></span> | <span data-ttu-id="6c5a1-135">Value</span><span class="sxs-lookup"><span data-stu-id="6c5a1-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c5a1-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c5a1-136">Header</span></span><br/>  | <dl> <span data-ttu-id="6c5a1-137"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c5a1-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6c5a1-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6c5a1-138">Library</span></span><br/> | <dl> <span data-ttu-id="6c5a1-139"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6c5a1-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c5a1-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c5a1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c5a1-141">**Clase CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="6c5a1-141">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




