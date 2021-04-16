---
description: El método AddPin agrega un nuevo PIN de salida al filtro.
ms.assetid: 48850a1f-ecb7-460c-9bfc-ce1d1103a00b
title: CSource. AddPin (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.AddPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 224550756f5935ce26c106ba01c9ef64f0767140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670400"
---
# <a name="csourceaddpin-method"></a><span data-ttu-id="a2958-103">CSource. AddPin, método</span><span class="sxs-lookup"><span data-stu-id="a2958-103">CSource.AddPin method</span></span>

<span data-ttu-id="a2958-104">El `AddPin` método agrega un nuevo PIN de salida al filtro.</span><span class="sxs-lookup"><span data-stu-id="a2958-104">The `AddPin` method adds a new output pin to the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2958-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2958-105">Syntax</span></span>


```C++
HRESULT AddPin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="a2958-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a2958-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2958-107">*pStream*</span><span class="sxs-lookup"><span data-stu-id="a2958-107">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="a2958-108">Puntero al objeto [**CSourceStream**](csourcestream.md) que implementa el código PIN.</span><span class="sxs-lookup"><span data-stu-id="a2958-108">Pointer to the [**CSourceStream**](csourcestream.md) object that implements the pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2958-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2958-109">Return value</span></span>

<span data-ttu-id="a2958-110">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="a2958-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="a2958-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a2958-111">Return code</span></span>                                                                                   | <span data-ttu-id="a2958-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2958-112">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="a2958-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a2958-113"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a2958-114">Correcto</span><span class="sxs-lookup"><span data-stu-id="a2958-114">Success</span></span><br/>             |
| <dl> <span data-ttu-id="a2958-115"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a2958-115"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a2958-116">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="a2958-116">Insufficient memory</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a2958-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2958-117">Remarks</span></span>

<span data-ttu-id="a2958-118">Cuando se crea un nuevo PIN derivado de **CSourceStream**, el constructor **CSourceStream** llama automáticamente a este método para agregar el PIN de salida al filtro.</span><span class="sxs-lookup"><span data-stu-id="a2958-118">When you create a new pin derived from **CSourceStream**, the **CSourceStream** constructor automatically calls this method, to add the output pin to the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2958-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2958-119">Requirements</span></span>



| <span data-ttu-id="a2958-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2958-120">Requirement</span></span> | <span data-ttu-id="a2958-121">Value</span><span class="sxs-lookup"><span data-stu-id="a2958-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2958-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2958-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a2958-123"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2958-123"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a2958-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a2958-124">Library</span></span><br/> | <dl> <span data-ttu-id="a2958-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a2958-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2958-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2958-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2958-127">**Clase CSource**</span><span class="sxs-lookup"><span data-stu-id="a2958-127">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




