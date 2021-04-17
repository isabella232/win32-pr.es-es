---
description: Dada una lista de tipos de medios, el método TryMediaTypes intenta completar una conexión con uno de esos tipos.
ms.assetid: cc437e44-bc59-494e-8669-7f539353a794
title: Método CBasePin. TryMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.TryMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 19b8da39d07b8aae9401bdc6ccf2eecb5d3a1e88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660481"
---
# <a name="cbasepintrymediatypes-method"></a><span data-ttu-id="373fd-103">CBasePin. TryMediaTypes, método</span><span class="sxs-lookup"><span data-stu-id="373fd-103">CBasePin.TryMediaTypes method</span></span>

<span data-ttu-id="373fd-104">Dada una lista de tipos de medios, el `TryMediaTypes` método intenta completar una conexión mediante uno de esos tipos.</span><span class="sxs-lookup"><span data-stu-id="373fd-104">Given a list of media types, the `TryMediaTypes` method tries to complete a connection using one of those types.</span></span>

## <a name="syntax"></a><span data-ttu-id="373fd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="373fd-105">Syntax</span></span>


```C++
virtual HRESULT TryMediaTypes(
         IPin            *pReceivePin,
   const CMediaType      *pmt,
         IEnumMediaTypes *pEnum
);
```



## <a name="parameters"></a><span data-ttu-id="373fd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="373fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="373fd-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="373fd-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="373fd-108">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN receptor.</span><span class="sxs-lookup"><span data-stu-id="373fd-108">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="373fd-109">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="373fd-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="373fd-110">Puntero a un objeto [**CMediaType**](cmediatype.md) que limita los posibles tipos de medios, o **null**.</span><span class="sxs-lookup"><span data-stu-id="373fd-110">Pointer to a [**CMediaType**](cmediatype.md) object that limits the possible media types, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="373fd-111">*pEnum*</span><span class="sxs-lookup"><span data-stu-id="373fd-111">*pEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="373fd-112">Puntero a una interfaz [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) , que se usa para enumerar la lista de tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="373fd-112">Pointer to an [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface, used to enumerate the list of media types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="373fd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="373fd-113">Return value</span></span>

<span data-ttu-id="373fd-114">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="373fd-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="373fd-115">Entre los valores posibles se incluyen los de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="373fd-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="373fd-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="373fd-116">Return code</span></span>                                                                                                  | <span data-ttu-id="373fd-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="373fd-117">Description</span></span>                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="373fd-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="373fd-118"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="373fd-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="373fd-119">Success.</span></span><br/>                               |
| <dl> <span data-ttu-id="373fd-120"><dt>**VFW \_ E \_ no \_ hay \_ tipos aceptables**</dt></span><span class="sxs-lookup"><span data-stu-id="373fd-120"><dt>**VFW\_E\_NO\_ACCEPTABLE\_TYPES**</dt></span></span> </dl> | <span data-ttu-id="373fd-121">No se encontró un tipo de medio aceptable.</span><span class="sxs-lookup"><span data-stu-id="373fd-121">Did not find an acceptable media type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="373fd-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="373fd-122">Remarks</span></span>

<span data-ttu-id="373fd-123">Para cada tipo de medio devuelto por la interfaz **IEnumMediaTypes** , este método intenta una conexión llamando al método [**CBasePin:: AttemptConnection**](cbasepin-attemptconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="373fd-123">For each media type returned by the **IEnumMediaTypes** interface, this method attempts a connection by calling the [**CBasePin::AttemptConnection**](cbasepin-attemptconnection.md) method.</span></span>

<span data-ttu-id="373fd-124">Si el parámetro *PMT* no es **null**, el PIN omite los tipos de medios que no coinciden con este tipo.</span><span class="sxs-lookup"><span data-stu-id="373fd-124">If the *pmt* parameter is non-**NULL**, the pin skips media types that do not match this type.</span></span> <span data-ttu-id="373fd-125">El parámetro *PMT* puede especificar un tipo de medio parcial.</span><span class="sxs-lookup"><span data-stu-id="373fd-125">The *pmt* parameter can specify a partial media type.</span></span> <span data-ttu-id="373fd-126">Un tipo de medio parcial tiene un valor de GUID \_ null para el tipo principal, el subtipo o el formato.</span><span class="sxs-lookup"><span data-stu-id="373fd-126">A partial media type has a value of GUID\_NULL for either the major type, the subtype, or the format.</span></span> <span data-ttu-id="373fd-127">El \_ valor null de GUID coincide con cualquier tipo, similar a un valor "comodín".</span><span class="sxs-lookup"><span data-stu-id="373fd-127">The GUID\_NULL value matches any type, similar to a "wildcard" value.</span></span>

## <a name="requirements"></a><span data-ttu-id="373fd-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="373fd-128">Requirements</span></span>



| <span data-ttu-id="373fd-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="373fd-129">Requirement</span></span> | <span data-ttu-id="373fd-130">Value</span><span class="sxs-lookup"><span data-stu-id="373fd-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="373fd-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="373fd-131">Header</span></span><br/>  | <dl> <span data-ttu-id="373fd-132"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="373fd-132"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="373fd-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="373fd-133">Library</span></span><br/> | <dl> <span data-ttu-id="373fd-134"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="373fd-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="373fd-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="373fd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="373fd-136">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="373fd-136">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




