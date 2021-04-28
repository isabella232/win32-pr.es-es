---
description: 'Constructor CSourceStream.CSourceStream: método constructor.'
ms.assetid: 9078b2f5-b11e-4780-8143-6738e9df4f4b
title: Constructor CSourceStream.CSourceStream (Source.h)
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
ms.openlocfilehash: 75d94bb89ca109c2a7974c294153d46235f92f23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085193"
---
# <a name="csourcestreamcsourcestream-constructor"></a><span data-ttu-id="c9455-103">Constructor CSourceStream.CSourceStream</span><span class="sxs-lookup"><span data-stu-id="c9455-103">CSourceStream.CSourceStream constructor</span></span>

<span data-ttu-id="c9455-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="c9455-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9455-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9455-105">Syntax</span></span>


```C++
CSourceStream(
   TCHAR   *pObjectName,
   HRESULT *phr,
   CSource *pms,
   LPCWSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="c9455-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9455-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9455-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="c9455-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="c9455-108">Puntero a una cadena que contiene el nombre de depuración del pin.</span><span class="sxs-lookup"><span data-stu-id="c9455-108">Pointer to a string containing the debug name of the pin.</span></span>

</dd> <dt>

<span data-ttu-id="c9455-109">*Phr*</span><span class="sxs-lookup"><span data-stu-id="c9455-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="c9455-110">Puntero a una variable que recibe un **valor HRESULT** que indica el éxito o error del método.</span><span class="sxs-lookup"><span data-stu-id="c9455-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="c9455-111">Inicialice el valor en S \_ OK antes de crear el objeto .</span><span class="sxs-lookup"><span data-stu-id="c9455-111">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="c9455-112">El valor solo se cambia si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="c9455-112">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="c9455-113">*Pms*</span><span class="sxs-lookup"><span data-stu-id="c9455-113">*pms*</span></span> 
</dt> <dd>

<span data-ttu-id="c9455-114">Puntero al [**filtro CSource**](csource.md) que creó este pin.</span><span class="sxs-lookup"><span data-stu-id="c9455-114">Pointer to the [**CSource**](csource.md) filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="c9455-115">*pName*</span><span class="sxs-lookup"><span data-stu-id="c9455-115">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="c9455-116">Puntero a una cadena que contiene el nombre del pin.</span><span class="sxs-lookup"><span data-stu-id="c9455-116">Pointer to a string that contains the name of the pin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9455-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c9455-117">Remarks</span></span>

<span data-ttu-id="c9455-118">La cadena especificada en el *parámetro pObjectName* solo se usa con fines de depuración.</span><span class="sxs-lookup"><span data-stu-id="c9455-118">The string given in the *pObjectName* parameter is used only for debugging purposes.</span></span> <span data-ttu-id="c9455-119">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="c9455-119">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

<span data-ttu-id="c9455-120">La cadena especificada en el *parámetro pName* es el nombre devuelto por el [**método IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo)</span><span class="sxs-lookup"><span data-stu-id="c9455-120">The string given in the *pName* parameter is the name returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="c9455-121">La `CSourceStream` clase no usa este nombre para el identificador de pin devuelto por el método [**CSourceStream::QueryId.**](csourcestream-queryid.md)</span><span class="sxs-lookup"><span data-stu-id="c9455-121">The `CSourceStream` class does not use this name for the pin identifier returned by the [**CSourceStream::QueryId**](csourcestream-queryid.md) method.</span></span> <span data-ttu-id="c9455-122">En su lugar, **QueryId** calcula un identificador de pin basado en el número de pin.</span><span class="sxs-lookup"><span data-stu-id="c9455-122">Instead, **QueryId** calculates a pin identifier based on the pin number.</span></span> <span data-ttu-id="c9455-123">(Los identificadores de pin admiten la persistencia del grafo.</span><span class="sxs-lookup"><span data-stu-id="c9455-123">(Pin identifiers support graph persistence.</span></span> <span data-ttu-id="c9455-124">Para obtener más información, [**vea IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)).</span><span class="sxs-lookup"><span data-stu-id="c9455-124">For more information, see [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).)</span></span>

<span data-ttu-id="c9455-125">El constructor agrega automáticamente el pin al filtro propietario, llamando a [**CSource::AddPin**](csource-addpin.md).</span><span class="sxs-lookup"><span data-stu-id="c9455-125">The constructor automatically adds the pin to the owning filter, by calling [**CSource::AddPin**](csource-addpin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9455-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9455-126">Requirements</span></span>



| <span data-ttu-id="c9455-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9455-127">Requirement</span></span> | <span data-ttu-id="c9455-128">Value</span><span class="sxs-lookup"><span data-stu-id="c9455-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9455-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9455-129">Header</span></span><br/>  | <dl> <span data-ttu-id="c9455-130"><dt>Source.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9455-130"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c9455-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c9455-131">Library</span></span><br/> | <dl> <span data-ttu-id="c9455-132"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c9455-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9455-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c9455-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9455-134">**CSourceStream (clase)**</span><span class="sxs-lookup"><span data-stu-id="c9455-134">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




