---
description: 'Método CBaseOutputPin.DecideBufferSize: el método DecideBufferSize establece los requisitos del búfer.'
ms.assetid: 1f7a3424-18ba-4a10-b09f-947ee8585ffa
title: Método CBaseOutputPin.DecideBufferSize (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7a76f058e2f9c07a344453db87046704e26280a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099533"
---
# <a name="cbaseoutputpindecidebuffersize-method"></a><span data-ttu-id="2c691-103">CBaseOutputPin.DecideBufferSize (método)</span><span class="sxs-lookup"><span data-stu-id="2c691-103">CBaseOutputPin.DecideBufferSize method</span></span>

<span data-ttu-id="2c691-104">El `DecideBufferSize` método establece los requisitos del búfer.</span><span class="sxs-lookup"><span data-stu-id="2c691-104">The `DecideBufferSize` method sets the buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c691-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c691-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="2c691-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c691-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c691-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="2c691-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="2c691-108">Puntero a la interfaz [**IMemAllocator del asignador.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)</span><span class="sxs-lookup"><span data-stu-id="2c691-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="2c691-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="2c691-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="2c691-110">Puntero a una [**estructura ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contiene los requisitos de búfer del pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="2c691-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span> <span data-ttu-id="2c691-111">Si el pin de entrada no tiene ningún requisito, el autor de la llamada debe cero los miembros de esta estructura antes de llamar al método .</span><span class="sxs-lookup"><span data-stu-id="2c691-111">If the input pin does not have any requirements, the caller should zero out the members of this structure before calling the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c691-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c691-112">Return value</span></span>

<span data-ttu-id="2c691-113">Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="2c691-113">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c691-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2c691-114">Remarks</span></span>

<span data-ttu-id="2c691-115">Invalide este método en la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="2c691-115">Override this method in your derived class.</span></span> <span data-ttu-id="2c691-116">Llame al [**método IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) para especificar los requisitos del búfer.</span><span class="sxs-lookup"><span data-stu-id="2c691-116">Call the [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) method to specify your buffer requirements.</span></span> <span data-ttu-id="2c691-117">Normalmente, la clase derivada respetará los requisitos de búfer del pin de entrada, pero no es necesario.</span><span class="sxs-lookup"><span data-stu-id="2c691-117">Typically, the derived class will honor the input pin's buffer requirements, but it is not required to.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c691-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c691-118">Requirements</span></span>



| <span data-ttu-id="2c691-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c691-119">Requirement</span></span> | <span data-ttu-id="2c691-120">Value</span><span class="sxs-lookup"><span data-stu-id="2c691-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c691-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2c691-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2c691-122"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c691-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2c691-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2c691-123">Library</span></span><br/> | <dl> <span data-ttu-id="2c691-124"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2c691-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c691-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2c691-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c691-126">**CBaseOutputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="2c691-126">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




