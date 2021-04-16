---
description: 'El método Block bloquea o desbloquea el flujo de datos desde el código PIN. Este método implementa el método IPinFlowControl:: Block.'
ms.assetid: 8281cd8c-7543-42b5-9a4a-11bdfcb659e3
title: Método CDynamicOutputPin. Block (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Block
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b10e9dfd43f3ad98adf8f6abb0eb7c2223d5970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671759"
---
# <a name="cdynamicoutputpinblock-method"></a><span data-ttu-id="09bae-104">CDynamicOutputPin. Block (método)</span><span class="sxs-lookup"><span data-stu-id="09bae-104">CDynamicOutputPin.Block method</span></span>

<span data-ttu-id="09bae-105">El `Block` método bloquea o desbloquea el flujo de datos desde el código PIN.</span><span class="sxs-lookup"><span data-stu-id="09bae-105">The `Block` method blocks or unblocks the flow of data from the pin.</span></span> <span data-ttu-id="09bae-106">Este método implementa el método [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) .</span><span class="sxs-lookup"><span data-stu-id="09bae-106">This method implements the [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="09bae-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09bae-107">Syntax</span></span>


```C++
HRESULT Block(
   DWORD  dwBlockFlags,
   HANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="09bae-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09bae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09bae-109">*dwBlockFlags*</span><span class="sxs-lookup"><span data-stu-id="09bae-109">*dwBlockFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="09bae-110">Marca que indica si se debe bloquear o desbloquear el código PIN.</span><span class="sxs-lookup"><span data-stu-id="09bae-110">Flag that indicates whether to block or unblock the pin.</span></span> <span data-ttu-id="09bae-111">Debe ser uno de los siguientes valores: </span><span class="sxs-lookup"><span data-stu-id="09bae-111">Must be one of the following values:</span></span>

<span data-ttu-id="09bae-112">Cero: Desbloquea el flujo de datos desde el código PIN.</span><span class="sxs-lookup"><span data-stu-id="09bae-112">Zero: Unblock data flow from the pin.</span></span>

<span data-ttu-id="09bae-113">\_ \_ \_ \_ Bloquear bloque de control de flujo: bloquear flujo de datos desde el código PIN.</span><span class="sxs-lookup"><span data-stu-id="09bae-113">AM\_PIN\_FLOW\_CONTROL\_BLOCK: Block data flow from the pin.</span></span>

</dd> <dt>

<span data-ttu-id="09bae-114">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="09bae-114">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="09bae-115">Identificador de un objeto de evento o **null**.</span><span class="sxs-lookup"><span data-stu-id="09bae-115">Handle to an event object, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09bae-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09bae-116">Return value</span></span>

<span data-ttu-id="09bae-117">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="09bae-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="09bae-118">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="09bae-118">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="09bae-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="09bae-119">Return code</span></span>                                                                                                                    | <span data-ttu-id="09bae-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="09bae-120">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="09bae-121"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="09bae-121"><dt>**S\_FALSE**</dt></span></span> </dl>                                        | <span data-ttu-id="09bae-122">El PIN ya está desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="09bae-122">Pin is already unblocked.</span></span><br/>                     |
| <dl> <span data-ttu-id="09bae-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="09bae-123"><dt>**S\_OK**</dt></span></span> </dl>                                           | <span data-ttu-id="09bae-124">Correcto.</span><span class="sxs-lookup"><span data-stu-id="09bae-124">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="09bae-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="09bae-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                   | <span data-ttu-id="09bae-126">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="09bae-126">Invalid argument.</span></span><br/>                             |
| <dl> <span data-ttu-id="09bae-127"><dt>**VFW \_ E \_ PIN \_ ya \_ bloqueados**</dt></span><span class="sxs-lookup"><span data-stu-id="09bae-127"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED**</dt></span></span> </dl>                   | <span data-ttu-id="09bae-128">El PIN ya está bloqueado en otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="09bae-128">Pin is already blocked on another thread.</span></span><br/>     |
| <dl> <span data-ttu-id="09bae-129"><dt>**\_ \_ el PIN VFW \_ ya está \_ bloqueado \_ en \_ este \_ subproceso**</dt></span><span class="sxs-lookup"><span data-stu-id="09bae-129"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED\_ON\_THIS\_THREAD**</dt></span></span> </dl> | <span data-ttu-id="09bae-130">El PIN ya está bloqueado en el subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="09bae-130">Pin is already blocked on the calling thread.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="09bae-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09bae-131">Remarks</span></span>

<span data-ttu-id="09bae-132">Para obtener más información sobre este método, vea [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block).</span><span class="sxs-lookup"><span data-stu-id="09bae-132">For more information about this method, see [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block).</span></span> <span data-ttu-id="09bae-133">Internamente, este método llama a uno de los métodos protegidos siguientes:</span><span class="sxs-lookup"><span data-stu-id="09bae-133">Internally, this method calls one of the following protected methods:</span></span>

-   <span data-ttu-id="09bae-134">Bloquear (asincrónico): [ **CDynamicOutputPin:: AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)</span><span class="sxs-lookup"><span data-stu-id="09bae-134">Block (asynchronous): [**CDynamicOutputPin::AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)</span></span>
-   <span data-ttu-id="09bae-135">Bloquear (sincrónico): [ **CDynamicOutputPin:: SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)</span><span class="sxs-lookup"><span data-stu-id="09bae-135">Block (synchronous): [**CDynamicOutputPin::SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)</span></span>
-   <span data-ttu-id="09bae-136">Desbloquear: [ **CDynamicOutputPin:: UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)</span><span class="sxs-lookup"><span data-stu-id="09bae-136">Unblock: [**CDynamicOutputPin::UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)</span></span>

<span data-ttu-id="09bae-137">El desbloqueo siempre se realiza sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="09bae-137">Unblocking is always performed synchronously.</span></span>

## <a name="requirements"></a><span data-ttu-id="09bae-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09bae-138">Requirements</span></span>



| <span data-ttu-id="09bae-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="09bae-139">Requirement</span></span> | <span data-ttu-id="09bae-140">Value</span><span class="sxs-lookup"><span data-stu-id="09bae-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09bae-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09bae-141">Header</span></span><br/>  | <dl> <span data-ttu-id="09bae-142"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09bae-142"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="09bae-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="09bae-143">Library</span></span><br/> | <dl> <span data-ttu-id="09bae-144"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="09bae-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09bae-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="09bae-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09bae-146">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="09bae-146">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




