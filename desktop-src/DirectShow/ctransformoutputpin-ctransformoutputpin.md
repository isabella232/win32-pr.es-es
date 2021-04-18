---
description: Método de constructor.
ms.assetid: 6213ce92-d98a-4fb6-b66c-e7cdea6dff0d
title: Constructor CTransformOutputPin. CTransformOutputPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 730149ae67abb2924174954bb8b620a02cfae2b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680748"
---
# <a name="ctransformoutputpinctransformoutputpin-constructor"></a><span data-ttu-id="736dc-103">Constructor CTransformOutputPin. CTransformOutputPin</span><span class="sxs-lookup"><span data-stu-id="736dc-103">CTransformOutputPin.CTransformOutputPin constructor</span></span>

<span data-ttu-id="736dc-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="736dc-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="736dc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="736dc-105">Syntax</span></span>


```C++
CTransformOutputPin(
   TCHAR            *pObjectName,
   CTransformFilter *pTransformFilter,
   HRESULT          *phr,
   LPCWSTR          pName
);
```



## <a name="parameters"></a><span data-ttu-id="736dc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="736dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="736dc-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="736dc-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="736dc-108">Cadena que contiene el nombre de depuración del objeto.</span><span class="sxs-lookup"><span data-stu-id="736dc-108">String containing the debug name of the object.</span></span> <span data-ttu-id="736dc-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="736dc-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="736dc-110">*pTransformFilter*</span><span class="sxs-lookup"><span data-stu-id="736dc-110">*pTransformFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="736dc-111">Puntero al filtro que creó este pin, que debe ser un objeto [**CTransformFilter**](ctransformfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="736dc-111">Pointer to the filter that created this pin, which must be a [**CTransformFilter**](ctransformfilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="736dc-112">*phr*</span><span class="sxs-lookup"><span data-stu-id="736dc-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="736dc-113">Puntero a una variable que recibe un valor **HRESULT** que indica si el método se ha ejecutado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="736dc-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="736dc-114">Inicialice el valor a S \_ OK antes de crear el objeto.</span><span class="sxs-lookup"><span data-stu-id="736dc-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="736dc-115">Solo se cambia el valor si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="736dc-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="736dc-116">*pName*</span><span class="sxs-lookup"><span data-stu-id="736dc-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="736dc-117">Cadena de caracteres anchos que contiene el nombre del PIN.</span><span class="sxs-lookup"><span data-stu-id="736dc-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="736dc-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="736dc-118">Remarks</span></span>

<span data-ttu-id="736dc-119">El parámetro *pName* especifica el nombre del PIN, devuelto por el método [**IPin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .</span><span class="sxs-lookup"><span data-stu-id="736dc-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="736dc-120">Sin embargo, la cadena no se utiliza para el identificador del PIN.</span><span class="sxs-lookup"><span data-stu-id="736dc-120">However, the string is not used for the pin identifier.</span></span> <span data-ttu-id="736dc-121">El identificador del PIN para esta clase siempre es "out".</span><span class="sxs-lookup"><span data-stu-id="736dc-121">The pin identifier for this class is always "Out".</span></span> <span data-ttu-id="736dc-122">Para obtener más información, vea [**queryId**](ctransformoutputpin-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="736dc-122">For more information, see [**QueryId**](ctransformoutputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="736dc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="736dc-123">Requirements</span></span>



| <span data-ttu-id="736dc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="736dc-124">Requirement</span></span> | <span data-ttu-id="736dc-125">Value</span><span class="sxs-lookup"><span data-stu-id="736dc-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="736dc-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="736dc-126">Header</span></span><br/>  | <dl> <span data-ttu-id="736dc-127"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="736dc-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="736dc-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="736dc-128">Library</span></span><br/> | <dl> <span data-ttu-id="736dc-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="736dc-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




