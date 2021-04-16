---
description: 'El método QueryId recupera el identificador del PIN. Este método invalida el método CBasePin:: QueryId.'
ms.assetid: 9543234c-5349-49d0-b410-1c461ee4eabe
title: Método CRendererInputPin. QueryId (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b56ae2a846b4d89da4c6a9d4c8f88bd3094c5cff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671701"
---
# <a name="crendererinputpinqueryid-method"></a><span data-ttu-id="98bde-104">CRendererInputPin. QueryId (método)</span><span class="sxs-lookup"><span data-stu-id="98bde-104">CRendererInputPin.QueryId method</span></span>

<span data-ttu-id="98bde-105">El `QueryId` método recupera el identificador del PIN.</span><span class="sxs-lookup"><span data-stu-id="98bde-105">The `QueryId` method retrieves the pin identifier.</span></span> <span data-ttu-id="98bde-106">Este método invalida el método [**CBasePin:: queryId**](cbasepin-queryid.md) .</span><span class="sxs-lookup"><span data-stu-id="98bde-106">This method overrides the [**CBasePin::QueryId**](cbasepin-queryid.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="98bde-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98bde-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="98bde-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98bde-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98bde-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="98bde-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="98bde-110">Recibe una cadena que contiene el identificador del PIN.</span><span class="sxs-lookup"><span data-stu-id="98bde-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98bde-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98bde-111">Return value</span></span>

<span data-ttu-id="98bde-112">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="98bde-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="98bde-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="98bde-113">Return code</span></span>                                                                                   | <span data-ttu-id="98bde-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="98bde-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="98bde-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="98bde-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="98bde-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="98bde-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="98bde-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="98bde-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="98bde-118">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="98bde-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="98bde-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="98bde-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="98bde-120">Argumento de puntero **nulo**</span><span class="sxs-lookup"><span data-stu-id="98bde-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="98bde-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98bde-121">Remarks</span></span>

<span data-ttu-id="98bde-122">Este método asigna la cadena de caracteres anchos "in" y la asigna al parámetro *ID* .</span><span class="sxs-lookup"><span data-stu-id="98bde-122">This method allocates the wide-character string "In" and assigns it to the *Id* parameter.</span></span> <span data-ttu-id="98bde-123">El llamador debe liberar la memoria asignada mediante la función **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="98bde-123">The caller must free the allocated memory, using the **CoTaskMemFree** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="98bde-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98bde-124">Requirements</span></span>



| <span data-ttu-id="98bde-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="98bde-125">Requirement</span></span> | <span data-ttu-id="98bde-126">Value</span><span class="sxs-lookup"><span data-stu-id="98bde-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98bde-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98bde-127">Header</span></span><br/>  | <dl> <span data-ttu-id="98bde-128"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98bde-128"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="98bde-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98bde-129">Library</span></span><br/> | <dl> <span data-ttu-id="98bde-130"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="98bde-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98bde-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="98bde-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98bde-132">**Clase CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="98bde-132">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




