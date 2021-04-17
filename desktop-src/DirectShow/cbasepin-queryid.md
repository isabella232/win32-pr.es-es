---
description: 'El método QueryId recupera el identificador del PIN. Este método implementa el método IPin:: QueryId.'
ms.assetid: b365a574-61b4-454c-b062-8826cbe10f03
title: Método CBasePin. QueryId (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa14fb933c89da0b0b6d2eebfab480b5508a3666
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670874"
---
# <a name="cbasepinqueryid-method"></a><span data-ttu-id="e9a20-104">CBasePin. QueryId (método)</span><span class="sxs-lookup"><span data-stu-id="e9a20-104">CBasePin.QueryId method</span></span>

<span data-ttu-id="e9a20-105">El `QueryId` método recupera el identificador del PIN.</span><span class="sxs-lookup"><span data-stu-id="e9a20-105">The `QueryId` method retrieves the pin identifier.</span></span> <span data-ttu-id="e9a20-106">Este método implementa el método [**IPin:: queryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .</span><span class="sxs-lookup"><span data-stu-id="e9a20-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9a20-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9a20-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="e9a20-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9a20-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9a20-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="e9a20-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="e9a20-110">Puntero al identificador del PIN.</span><span class="sxs-lookup"><span data-stu-id="e9a20-110">Pointer to the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9a20-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9a20-111">Return value</span></span>

<span data-ttu-id="e9a20-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e9a20-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e9a20-113">Entre los valores posibles se incluyen los de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e9a20-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="e9a20-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e9a20-114">Return code</span></span>                                                                                   | <span data-ttu-id="e9a20-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9a20-115">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="e9a20-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e9a20-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e9a20-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="e9a20-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="e9a20-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e9a20-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e9a20-119">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="e9a20-119">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="e9a20-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="e9a20-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e9a20-121">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="e9a20-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e9a20-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9a20-122">Remarks</span></span>

<span data-ttu-id="e9a20-123">Este método devuelve una copia de la variable miembro [**CBasePin:: m \_ pName**](cbasepin-m-pname.md) .</span><span class="sxs-lookup"><span data-stu-id="e9a20-123">This method returns a copy of the [**CBasePin::m\_pName**](cbasepin-m-pname.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9a20-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9a20-124">Requirements</span></span>



| <span data-ttu-id="e9a20-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9a20-125">Requirement</span></span> | <span data-ttu-id="e9a20-126">Value</span><span class="sxs-lookup"><span data-stu-id="e9a20-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9a20-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9a20-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e9a20-128"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9a20-128"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e9a20-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e9a20-129">Library</span></span><br/> | <dl> <span data-ttu-id="e9a20-130"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e9a20-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9a20-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9a20-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9a20-132">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="e9a20-132">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




