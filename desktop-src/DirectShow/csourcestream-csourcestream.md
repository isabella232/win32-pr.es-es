---
description: Método de constructor.
ms.assetid: 9078b2f5-b11e-4780-8143-6738e9df4f4b
title: Constructor CSourceStream. CSourceStream (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8671e939364d1c0cd22796b1518313002b5eb33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660445"
---
# <a name="csourcestreamcsourcestream-constructor"></a><span data-ttu-id="d3d4e-103">Constructor CSourceStream. CSourceStream</span><span class="sxs-lookup"><span data-stu-id="d3d4e-103">CSourceStream.CSourceStream constructor</span></span>

<span data-ttu-id="d3d4e-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="d3d4e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3d4e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3d4e-105">Syntax</span></span>


```C++
CSourceStream(
   TCHAR   *pObjectName,
   HRESULT *phr,
   CSource *pms,
   LPCWSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="d3d4e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3d4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3d4e-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="d3d4e-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="d3d4e-108">Puntero a una cadena que contiene el nombre de depuración del código PIN.</span><span class="sxs-lookup"><span data-stu-id="d3d4e-108">Pointer to a string containing the debug name of the pin.</span></span>

</dd> <dt>

<span data-ttu-id="d3d4e-109">*phr*</span><span class="sxs-lookup"><span data-stu-id="d3d4e-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="d3d4e-110">Puntero a una variable que recibe un valor **HRESULT** que indica si el método se ha ejecutado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="d3d4e-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="d3d4e-111">Inicialice el valor a S \_ OK antes de crear el objeto.</span><span class="sxs-lookup"><span data-stu-id="d3d4e-111">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="d3d4e-112">Solo se cambia el valor si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="d3d4e-112">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="d3d4e-113">*jefes*</span><span class="sxs-lookup"><span data-stu-id="d3d4e-113">*pms*</span></span> 
</dt> <dd>

<span data-ttu-id="d3d4e-114">Puntero al filtro [**CSource**](csource.md) que creó este pin.</span><span class="sxs-lookup"><span data-stu-id="d3d4e-114">Pointer to the [**CSource**](csource.md) filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="d3d4e-115">*pName*</span><span class="sxs-lookup"><span data-stu-id="d3d4e-115">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="d3d4e-116">Puntero a una cadena que contiene el nombre del PIN.</span><span class="sxs-lookup"><span data-stu-id="d3d4e-116">Pointer to a string that contains the name of the pin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d3d4e-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3d4e-117">Remarks</span></span>

<span data-ttu-id="d3d4e-118">La cadena especificada en el parámetro *pObjectName* solo se usa para la depuración.</span><span class="sxs-lookup"><span data-stu-id="d3d4e-118">The string given in the *pObjectName* parameter is used only for debugging purposes.</span></span> <span data-ttu-id="d3d4e-119">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="d3d4e-119">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

<span data-ttu-id="d3d4e-120">La cadena especificada en el parámetro *pName* es el nombre devuelto por el método [**IPin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .</span><span class="sxs-lookup"><span data-stu-id="d3d4e-120">The string given in the *pName* parameter is the name returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="d3d4e-121">La `CSourceStream` clase no usa este nombre para el identificador de PIN devuelto por el método [**CSourceStream:: queryId**](csourcestream-queryid.md) .</span><span class="sxs-lookup"><span data-stu-id="d3d4e-121">The `CSourceStream` class does not use this name for the pin identifier returned by the [**CSourceStream::QueryId**](csourcestream-queryid.md) method.</span></span> <span data-ttu-id="d3d4e-122">En su lugar, **queryId** calcula un identificador de PIN basado en el número de PIN.</span><span class="sxs-lookup"><span data-stu-id="d3d4e-122">Instead, **QueryId** calculates a pin identifier based on the pin number.</span></span> <span data-ttu-id="d3d4e-123">(Los identificadores de PIN admiten la persistencia de gráficos.</span><span class="sxs-lookup"><span data-stu-id="d3d4e-123">(Pin identifiers support graph persistence.</span></span> <span data-ttu-id="d3d4e-124">Para obtener más información, vea [**IPin:: queryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)).</span><span class="sxs-lookup"><span data-stu-id="d3d4e-124">For more information, see [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).)</span></span>

<span data-ttu-id="d3d4e-125">El constructor agrega automáticamente el PIN al filtro propietario llamando a [**CSource:: AddPin**](csource-addpin.md).</span><span class="sxs-lookup"><span data-stu-id="d3d4e-125">The constructor automatically adds the pin to the owning filter, by calling [**CSource::AddPin**](csource-addpin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3d4e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3d4e-126">Requirements</span></span>



| <span data-ttu-id="d3d4e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3d4e-127">Requirement</span></span> | <span data-ttu-id="d3d4e-128">Value</span><span class="sxs-lookup"><span data-stu-id="d3d4e-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3d4e-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3d4e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d3d4e-130"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3d4e-130"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d3d4e-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d3d4e-131">Library</span></span><br/> | <dl> <span data-ttu-id="d3d4e-132"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d3d4e-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3d4e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3d4e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3d4e-134">**Clase CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="d3d4e-134">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




