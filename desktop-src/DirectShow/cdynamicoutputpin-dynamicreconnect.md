---
description: El método DynamicReconnect realiza una reconexión dinámica con un nuevo tipo de medio. La reconexión puede producirse mientras se ejecuta el gráfico de filtros.
ms.assetid: 1fe9f1cc-1f5d-407e-8c80-fea6cd1cb16f
title: Método CDynamicOutputPin. DynamicReconnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DynamicReconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd595748380a35f74e591283ed3d03273c683e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660127"
---
# <a name="cdynamicoutputpindynamicreconnect-method"></a><span data-ttu-id="2eb2a-104">CDynamicOutputPin. DynamicReconnect, método</span><span class="sxs-lookup"><span data-stu-id="2eb2a-104">CDynamicOutputPin.DynamicReconnect method</span></span>

<span data-ttu-id="2eb2a-105">El `DynamicReconnect` método realiza una reconexión dinámica con un nuevo tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="2eb2a-105">The `DynamicReconnect` method performs a dynamic reconnection with a new media type.</span></span> <span data-ttu-id="2eb2a-106">La reconexión puede producirse mientras se ejecuta el gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="2eb2a-106">The reconnection can occur while the filter graph is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eb2a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2eb2a-107">Syntax</span></span>


```C++
HRESULT DynamicReconnect(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="2eb2a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2eb2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eb2a-109">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="2eb2a-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="2eb2a-110">Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="2eb2a-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eb2a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2eb2a-111">Return value</span></span>

<span data-ttu-id="2eb2a-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2eb2a-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2eb2a-113">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2eb2a-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="2eb2a-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2eb2a-114">Return code</span></span>                                                                            | <span data-ttu-id="2eb2a-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="2eb2a-115">Description</span></span>                                                                                                                                         |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2eb2a-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2eb2a-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="2eb2a-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="2eb2a-117">Success.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="2eb2a-118"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="2eb2a-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="2eb2a-119">Error.</span><span class="sxs-lookup"><span data-stu-id="2eb2a-119">Failure.</span></span> <span data-ttu-id="2eb2a-120">Es posible que el filtro propietario no llamara al método [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) .</span><span class="sxs-lookup"><span data-stu-id="2eb2a-120">Possibly the owning filter did not call the [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2eb2a-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2eb2a-121">Remarks</span></span>

<span data-ttu-id="2eb2a-122">Se debe llamar a este método desde el mismo subproceso que entrega datos al pin.</span><span class="sxs-lookup"><span data-stu-id="2eb2a-122">This method must be called from the same thread that delivers data to the pin.</span></span> <span data-ttu-id="2eb2a-123">Una vez que se llama a este método, no se pueden entregar los ejemplos con el tipo de medio anterior.</span><span class="sxs-lookup"><span data-stu-id="2eb2a-123">Once this method is called, samples with the old media type cannot be delivered.</span></span> <span data-ttu-id="2eb2a-124">El llamador debe asegurarse de que no haya ejemplos antiguos pendientes.</span><span class="sxs-lookup"><span data-stu-id="2eb2a-124">The caller must ensure that no old samples are pending.</span></span>

<span data-ttu-id="2eb2a-125">Llame a [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="2eb2a-125">Call [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2eb2a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2eb2a-126">Requirements</span></span>



| <span data-ttu-id="2eb2a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2eb2a-127">Requirement</span></span> | <span data-ttu-id="2eb2a-128">Value</span><span class="sxs-lookup"><span data-stu-id="2eb2a-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eb2a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2eb2a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="2eb2a-130"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2eb2a-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2eb2a-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2eb2a-131">Library</span></span><br/> | <dl> <span data-ttu-id="2eb2a-132"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2eb2a-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eb2a-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="2eb2a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eb2a-134">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="2eb2a-134">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




