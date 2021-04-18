---
description: El método AttemptConnection se conecta a otro pin con un tipo de medio especificado.
ms.assetid: b80cf2c0-7266-4dac-8633-d30a871c57d9
title: Método CBasePin. AttemptConnection (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AttemptConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72f80d81b5f105f528292a23f8b58257066b425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661248"
---
# <a name="cbasepinattemptconnection-method"></a><span data-ttu-id="6b967-103">CBasePin. AttemptConnection, método</span><span class="sxs-lookup"><span data-stu-id="6b967-103">CBasePin.AttemptConnection method</span></span>

<span data-ttu-id="6b967-104">El `AttemptConnection` método se conecta a otro PIN mediante un tipo de medio especificado.</span><span class="sxs-lookup"><span data-stu-id="6b967-104">The `AttemptConnection` method connects to another pin using a specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b967-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b967-105">Syntax</span></span>


```C++
virtual HRESULT AttemptConnection(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="6b967-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b967-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b967-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="6b967-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="6b967-108">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN receptor.</span><span class="sxs-lookup"><span data-stu-id="6b967-108">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="6b967-109">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="6b967-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="6b967-110">Puntero a un objeto [**CMediaType**](cmediatype.md) que especifica el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="6b967-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b967-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b967-111">Return value</span></span>

<span data-ttu-id="6b967-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6b967-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6b967-113">Entre los valores posibles se incluyen los de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6b967-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="6b967-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6b967-114">Return code</span></span>                                                                                                | <span data-ttu-id="6b967-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b967-115">Description</span></span>                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6b967-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6b967-116"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="6b967-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="6b967-117">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="6b967-118"><dt>**\_tipo VFW \_ E \_ no \_ aceptado**</dt></span><span class="sxs-lookup"><span data-stu-id="6b967-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="6b967-119">El tipo de medio no es aceptable.</span><span class="sxs-lookup"><span data-stu-id="6b967-119">The media type is not acceptable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6b967-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b967-120">Remarks</span></span>

<span data-ttu-id="6b967-121">Este método intenta conectar los dos PIN con un tipo de medio específico.</span><span class="sxs-lookup"><span data-stu-id="6b967-121">This method attempts to connect the two pins with a specific media type.</span></span> <span data-ttu-id="6b967-122">Si el tipo no es aceptable, se produce un error en el método sin intentar otros tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="6b967-122">If the type is not acceptable, the method fails without trying other media types.</span></span>

<span data-ttu-id="6b967-123">Si el tipo de medio es aceptable, este método llama al método [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) del PIN receptor.</span><span class="sxs-lookup"><span data-stu-id="6b967-123">If the media type is acceptable, this method calls the receiving pin's [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span> <span data-ttu-id="6b967-124">A continuación, llama al método [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) para completar la conexión.</span><span class="sxs-lookup"><span data-stu-id="6b967-124">Then it calls the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method to complete the connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b967-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b967-125">Requirements</span></span>



| <span data-ttu-id="6b967-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b967-126">Requirement</span></span> | <span data-ttu-id="6b967-127">Value</span><span class="sxs-lookup"><span data-stu-id="6b967-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b967-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6b967-128">Header</span></span><br/>  | <dl> <span data-ttu-id="6b967-129"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b967-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6b967-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6b967-130">Library</span></span><br/> | <dl> <span data-ttu-id="6b967-131"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6b967-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b967-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b967-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b967-133">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="6b967-133">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




