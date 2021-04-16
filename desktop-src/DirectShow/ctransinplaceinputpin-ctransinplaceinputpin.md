---
description: Método de constructor.
ms.assetid: db0a3f78-ddb9-43b5-aab5-da2faaebb527
title: Constructor CTransInPlaceInputPin. CTransInPlaceInputPin (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a801b2c4286f903ef450cac2fd76252f451f9add
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679262"
---
# <a name="ctransinplaceinputpinctransinplaceinputpin-constructor"></a><span data-ttu-id="da396-103">Constructor CTransInPlaceInputPin. CTransInPlaceInputPin</span><span class="sxs-lookup"><span data-stu-id="da396-103">CTransInPlaceInputPin.CTransInPlaceInputPin constructor</span></span>

<span data-ttu-id="da396-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="da396-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="da396-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da396-105">Syntax</span></span>


```C++
CTransInPlaceInputPin(
   TCHAR               *pObjectName,
   CTransInPlaceFilter *pFilter,
   HRESULT             *phr,
   LPCWSTR             pName
);
```



## <a name="parameters"></a><span data-ttu-id="da396-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da396-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da396-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="da396-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="da396-108">Cadena que contiene el nombre de depuración del objeto.</span><span class="sxs-lookup"><span data-stu-id="da396-108">String containing the debug name of the object.</span></span> <span data-ttu-id="da396-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="da396-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="da396-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="da396-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="da396-111">Puntero al filtro que creó este pin, que debe ser un objeto [**CTransInPlaceFilter**](ctransinplacefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="da396-111">Pointer to the filter that created this pin, which must be a [**CTransInPlaceFilter**](ctransinplacefilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="da396-112">*phr*</span><span class="sxs-lookup"><span data-stu-id="da396-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="da396-113">Puntero a una variable que recibe un valor **HRESULT** que indica si el método se ha ejecutado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="da396-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="da396-114">Inicialice el valor a S \_ OK antes de crear el objeto.</span><span class="sxs-lookup"><span data-stu-id="da396-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="da396-115">Solo se cambia el valor si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="da396-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="da396-116">*pName*</span><span class="sxs-lookup"><span data-stu-id="da396-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="da396-117">Cadena de caracteres anchos que contiene el nombre del PIN.</span><span class="sxs-lookup"><span data-stu-id="da396-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da396-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da396-118">Remarks</span></span>

<span data-ttu-id="da396-119">El parámetro *pName* especifica el nombre del PIN, devuelto por el método [**IPin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .</span><span class="sxs-lookup"><span data-stu-id="da396-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="da396-120">Sin embargo, esta cadena no se utiliza para el identificador del PIN.</span><span class="sxs-lookup"><span data-stu-id="da396-120">However, this string is not used for the pin identifier.</span></span> <span data-ttu-id="da396-121">El identificador de PIN de esta clase siempre está en.</span><span class="sxs-lookup"><span data-stu-id="da396-121">The pin identifier for this class is always In.</span></span> <span data-ttu-id="da396-122">Para obtener más información, vea [**CTransformInputPin:: queryId**](ctransforminputpin-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="da396-122">For more information, see [**CTransformInputPin::QueryId**](ctransforminputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da396-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da396-123">Requirements</span></span>



| <span data-ttu-id="da396-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="da396-124">Requirement</span></span> | <span data-ttu-id="da396-125">Value</span><span class="sxs-lookup"><span data-stu-id="da396-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da396-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da396-126">Header</span></span><br/>  | <dl> <span data-ttu-id="da396-127"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da396-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="da396-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="da396-128">Library</span></span><br/> | <dl> <span data-ttu-id="da396-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="da396-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da396-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="da396-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da396-131">**Clase CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="da396-131">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




