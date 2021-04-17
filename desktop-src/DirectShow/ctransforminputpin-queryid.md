---
description: 'El método QueryId recupera un identificador para el código PIN. Este método implementa el método IPin:: QueryId.'
ms.assetid: 91fde383-0288-4307-9ca8-e117b6111769
title: Método CTransformInputPin. QueryId (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: daae425e82bbc89cfbc863baea1924e36e63f122
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680530"
---
# <a name="ctransforminputpinqueryid-method"></a><span data-ttu-id="d3830-104">CTransformInputPin. QueryId (método)</span><span class="sxs-lookup"><span data-stu-id="d3830-104">CTransformInputPin.QueryId method</span></span>

<span data-ttu-id="d3830-105">El `QueryId` método recupera un identificador para el código PIN.</span><span class="sxs-lookup"><span data-stu-id="d3830-105">The `QueryId` method retrieves an identifier for the pin.</span></span> <span data-ttu-id="d3830-106">Este método implementa el método [**IPin:: queryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .</span><span class="sxs-lookup"><span data-stu-id="d3830-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3830-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3830-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="d3830-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3830-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3830-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="d3830-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="d3830-110">Recibe una cadena que contiene el identificador del PIN.</span><span class="sxs-lookup"><span data-stu-id="d3830-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3830-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3830-111">Return value</span></span>

<span data-ttu-id="d3830-112">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d3830-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="d3830-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d3830-113">Return code</span></span>                                                                                   | <span data-ttu-id="d3830-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3830-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="d3830-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d3830-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d3830-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="d3830-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="d3830-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d3830-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d3830-118">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="d3830-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="d3830-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="d3830-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d3830-120">Argumento de puntero **nulo**</span><span class="sxs-lookup"><span data-stu-id="d3830-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d3830-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3830-121">Remarks</span></span>

<span data-ttu-id="d3830-122">El identificador del PIN se usa para la persistencia del gráfico.</span><span class="sxs-lookup"><span data-stu-id="d3830-122">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="d3830-123">El identificador de PIN de esta clase está en.</span><span class="sxs-lookup"><span data-stu-id="d3830-123">The pin identifier for this class is In.</span></span> <span data-ttu-id="d3830-124">Esta clase invalida el comportamiento de la clase [**CBasePin**](cbasepin.md) .</span><span class="sxs-lookup"><span data-stu-id="d3830-124">This class overrides the behavior of the [**CBasePin**](cbasepin.md) class.</span></span> <span data-ttu-id="d3830-125">En la clase **CBasePin** , el identificador del PIN es el mismo que el nombre del PIN especificado en el constructor de clase.</span><span class="sxs-lookup"><span data-stu-id="d3830-125">In the **CBasePin** class, the pin identifier is the same as the pin name, specified in the class constructor.</span></span> <span data-ttu-id="d3830-126">En la clase **CTransformInputPin** , el identificador del PIN y el nombre del PIN no son los mismos.</span><span class="sxs-lookup"><span data-stu-id="d3830-126">In the **CTransformInputPin** class, the pin identifier and the pin name are not the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3830-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3830-127">Requirements</span></span>



| <span data-ttu-id="d3830-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3830-128">Requirement</span></span> | <span data-ttu-id="d3830-129">Value</span><span class="sxs-lookup"><span data-stu-id="d3830-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3830-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3830-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d3830-131"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3830-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d3830-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d3830-132">Library</span></span><br/> | <dl> <span data-ttu-id="d3830-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d3830-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




