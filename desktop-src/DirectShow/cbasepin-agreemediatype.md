---
description: El método AgreeMediaType busca un tipo de medio para crear una conexión de PIN.
ms.assetid: 545186d2-b5e8-4833-b0ff-11160c1dd53b
title: Método CBasePin. AgreeMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AgreeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e5cdea12cb8bca3319f908fe697251a3d4699d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671641"
---
# <a name="cbasepinagreemediatype-method"></a><span data-ttu-id="eb27f-103">CBasePin. AgreeMediaType, método</span><span class="sxs-lookup"><span data-stu-id="eb27f-103">CBasePin.AgreeMediaType method</span></span>

<span data-ttu-id="eb27f-104">El `AgreeMediaType` método busca un tipo de medio para crear una conexión de PIN.</span><span class="sxs-lookup"><span data-stu-id="eb27f-104">The `AgreeMediaType` method searches for a media type to make a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb27f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb27f-105">Syntax</span></span>


```C++
virtual HRESULT AgreeMediaType(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="eb27f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb27f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb27f-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="eb27f-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="eb27f-108">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN receptor.</span><span class="sxs-lookup"><span data-stu-id="eb27f-108">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="eb27f-109">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="eb27f-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="eb27f-110">Puntero a un objeto [**CMediaType**](cmediatype.md) que especifica un tipo de medio, o **null**.</span><span class="sxs-lookup"><span data-stu-id="eb27f-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies a media type, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb27f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb27f-111">Return value</span></span>

<span data-ttu-id="eb27f-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eb27f-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="eb27f-113">Entre los valores posibles se incluyen los de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="eb27f-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="eb27f-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="eb27f-114">Return code</span></span>                                                                                                  | <span data-ttu-id="eb27f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb27f-115">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="eb27f-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="eb27f-116"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="eb27f-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="eb27f-117">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="eb27f-118"><dt>**VFW \_ E \_ no \_ hay \_ tipos aceptables**</dt></span><span class="sxs-lookup"><span data-stu-id="eb27f-118"><dt>**VFW\_E\_NO\_ACCEPTABLE\_TYPES**</dt></span></span> </dl> | <span data-ttu-id="eb27f-119">No se encontró ningún tipo de medio aceptable.</span><span class="sxs-lookup"><span data-stu-id="eb27f-119">No acceptable media type was found.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eb27f-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb27f-120">Remarks</span></span>

<span data-ttu-id="eb27f-121">Si el parámetro *PMT* no es **null** y especifica totalmente un tipo de medio, este método intenta una conexión con ese tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="eb27f-121">If the *pmt* parameter is non-**NULL** and fully specifies a media type, this method attempts a connection using that media type.</span></span> <span data-ttu-id="eb27f-122">Si se produce un error en el intento, el método devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="eb27f-122">If the attempt fails, the method returns an error.</span></span>

<span data-ttu-id="eb27f-123">Si el parámetro *PMT* es **null** o especifica un tipo de medio parcial, este método probará los tipos de medios en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="eb27f-123">If the *pmt* parameter is **NULL** or specifies a partial media type, this method tries media types in the following order:</span></span>

1.  <span data-ttu-id="eb27f-124">Los tipos de medios preferidos del PIN receptor.</span><span class="sxs-lookup"><span data-stu-id="eb27f-124">The receiving pin's preferred media types.</span></span>
2.  <span data-ttu-id="eb27f-125">Tipos de medios preferidos de este pin.</span><span class="sxs-lookup"><span data-stu-id="eb27f-125">This pin's preferred media types.</span></span>

<span data-ttu-id="eb27f-126">Los tipos de medios preferidos se enumeran con el método [**CBasePin:: EnumMediaTypes**](cbasepin-enummediatypes.md) y el enumerador resultante se pasa al método [**CBasePin:: TryMediaTypes**](cbasepin-trymediatypes.md) .</span><span class="sxs-lookup"><span data-stu-id="eb27f-126">Preferred media types are enumerated with the [**CBasePin::EnumMediaTypes**](cbasepin-enummediatypes.md) method, and the resulting enumerator is passed to the [**CBasePin::TryMediaTypes**](cbasepin-trymediatypes.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb27f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb27f-127">Requirements</span></span>



| <span data-ttu-id="eb27f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb27f-128">Requirement</span></span> | <span data-ttu-id="eb27f-129">Value</span><span class="sxs-lookup"><span data-stu-id="eb27f-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb27f-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb27f-130">Header</span></span><br/>  | <dl> <span data-ttu-id="eb27f-131"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb27f-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eb27f-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eb27f-132">Library</span></span><br/> | <dl> <span data-ttu-id="eb27f-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="eb27f-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb27f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb27f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb27f-135">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="eb27f-135">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




