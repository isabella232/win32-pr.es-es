---
description: El método RemovePin quita un PIN especificado del filtro. El método no elimina el código PIN.
ms.assetid: 104eccfa-3fff-4f47-ba1b-3206eab9eef8
title: CSource. RemovePin (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.RemovePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b71ced14a6f92a3056ac4f42e55bc3858c578ff6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661183"
---
# <a name="csourceremovepin-method"></a><span data-ttu-id="d75f0-104">CSource. RemovePin, método</span><span class="sxs-lookup"><span data-stu-id="d75f0-104">CSource.RemovePin method</span></span>

<span data-ttu-id="d75f0-105">El `RemovePin` método quita un PIN especificado del filtro.</span><span class="sxs-lookup"><span data-stu-id="d75f0-105">The `RemovePin` method removes a specified pin from the filter.</span></span> <span data-ttu-id="d75f0-106">El método no elimina el código PIN.</span><span class="sxs-lookup"><span data-stu-id="d75f0-106">The method does not delete the pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="d75f0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d75f0-107">Syntax</span></span>


```C++
HRESULT RemovePin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="d75f0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d75f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d75f0-109">*pStream*</span><span class="sxs-lookup"><span data-stu-id="d75f0-109">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="d75f0-110">Puntero al objeto [**CSourceStream**](csourcestream.md) que implementa el código PIN.</span><span class="sxs-lookup"><span data-stu-id="d75f0-110">Pointer to the [**CSourceStream**](csourcestream.md) object that implements the pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d75f0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d75f0-111">Return value</span></span>

<span data-ttu-id="d75f0-112">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d75f0-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="d75f0-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d75f0-113">Return code</span></span>                                                                             | <span data-ttu-id="d75f0-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d75f0-114">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="d75f0-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d75f0-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="d75f0-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="d75f0-116">Success.</span></span><br/>                              |
| <dl> <span data-ttu-id="d75f0-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="d75f0-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="d75f0-118">El filtro no contiene este pin.</span><span class="sxs-lookup"><span data-stu-id="d75f0-118">The filter does not contain this pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d75f0-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d75f0-119">Remarks</span></span>

<span data-ttu-id="d75f0-120">El método de destructor llama a este método para quitar el punto de conexión de salida del filtro.</span><span class="sxs-lookup"><span data-stu-id="d75f0-120">The destructor method calls this method, to remove the output pin from the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="d75f0-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d75f0-121">Requirements</span></span>



| <span data-ttu-id="d75f0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d75f0-122">Requirement</span></span> | <span data-ttu-id="d75f0-123">Value</span><span class="sxs-lookup"><span data-stu-id="d75f0-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d75f0-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d75f0-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d75f0-125"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d75f0-125"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d75f0-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d75f0-126">Library</span></span><br/> | <dl> <span data-ttu-id="d75f0-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d75f0-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d75f0-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="d75f0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d75f0-129">**Clase CSource**</span><span class="sxs-lookup"><span data-stu-id="d75f0-129">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




