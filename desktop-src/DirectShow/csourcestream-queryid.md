---
description: El método QueryId recupera un identificador para el código PIN.
ms.assetid: 6050292e-6203-4a79-87bf-47394624cb32
title: CSourceStream. QueryId (método, source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 267748fe4ce1eeec4650544a2f72069df897a366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680689"
---
# <a name="csourcestreamqueryid-method"></a><span data-ttu-id="c801a-103">CSourceStream. QueryId (método)</span><span class="sxs-lookup"><span data-stu-id="c801a-103">CSourceStream.QueryId method</span></span>

<span data-ttu-id="c801a-104">El `QueryId` método recupera un identificador para el código PIN.</span><span class="sxs-lookup"><span data-stu-id="c801a-104">The `QueryId` method retrieves an identifier for the pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="c801a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c801a-105">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="c801a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c801a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c801a-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="c801a-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="c801a-108">Puntero a una variable que recibe una cadena que contiene el identificador del PIN.</span><span class="sxs-lookup"><span data-stu-id="c801a-108">Pointer to a variable that receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c801a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c801a-109">Return value</span></span>

<span data-ttu-id="c801a-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c801a-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c801a-111">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c801a-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="c801a-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c801a-112">Return code</span></span>                                                                                       | <span data-ttu-id="c801a-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="c801a-113">Description</span></span>                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="c801a-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c801a-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="c801a-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="c801a-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="c801a-116"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c801a-116"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="c801a-117">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="c801a-117">Insufficient memory.</span></span><br/>             |
| <dl> <span data-ttu-id="c801a-118"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="c801a-118"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="c801a-119">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="c801a-119">**NULL** pointer argument.</span></span><br/>       |
| <dl> <span data-ttu-id="c801a-120"><dt>**VFW \_ E \_ no \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="c801a-120"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="c801a-121">No se encontró el PIN en el filtro.</span><span class="sxs-lookup"><span data-stu-id="c801a-121">Pin was not found on the filter.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c801a-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c801a-122">Remarks</span></span>

<span data-ttu-id="c801a-123">Este método implementa el método [**IPin:: queryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .</span><span class="sxs-lookup"><span data-stu-id="c801a-123">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span> <span data-ttu-id="c801a-124">Para construir una cadena de identificador, el PIN llama al método [**CSource:: FindPinNumber**](csource-findpinnumber.md) con sí mismo como parámetro.</span><span class="sxs-lookup"><span data-stu-id="c801a-124">To construct an identifier string, the pin calls the [**CSource::FindPinNumber**](csource-findpinnumber.md) method with itself as the parameter.</span></span> <span data-ttu-id="c801a-125">El método **FindPinNumber** devuelve el número PIN, indizado desde cero.</span><span class="sxs-lookup"><span data-stu-id="c801a-125">The **FindPinNumber** method returns the pin number, indexed from zero.</span></span> <span data-ttu-id="c801a-126">`QueryId` incrementa el valor devuelto en uno y convierte el resultado en una cadena.</span><span class="sxs-lookup"><span data-stu-id="c801a-126">`QueryId` increments the return value by one and converts the result to a string.</span></span> <span data-ttu-id="c801a-127">Por ejemplo, el primer PIN se convierte en "1"; el segundo PIN se convierte en "2"; etc.</span><span class="sxs-lookup"><span data-stu-id="c801a-127">For example, the first pin becomes "1"; the second pin becomes "2"; and so forth.</span></span>

<span data-ttu-id="c801a-128">Si este método devuelve VFW \_ E \_ no \_ encontrado, indica que la matriz de PIN del filtro no es válida, supuestamente causada por un error en el filtro.</span><span class="sxs-lookup"><span data-stu-id="c801a-128">If this method returns VFW\_E\_NOT\_FOUND, it indicates that the filter's array of pins is invalid, presumably caused by a bug in the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="c801a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c801a-129">Requirements</span></span>



| <span data-ttu-id="c801a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c801a-130">Requirement</span></span> | <span data-ttu-id="c801a-131">Value</span><span class="sxs-lookup"><span data-stu-id="c801a-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c801a-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c801a-132">Header</span></span><br/>  | <dl> <span data-ttu-id="c801a-133"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c801a-133"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c801a-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c801a-134">Library</span></span><br/> | <dl> <span data-ttu-id="c801a-135"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c801a-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c801a-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="c801a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c801a-137">**Clase CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="c801a-137">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




