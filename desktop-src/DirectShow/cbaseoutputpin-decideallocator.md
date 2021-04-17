---
description: El método DecideAllocator selecciona un asignador de memoria.
ms.assetid: cdc15b0e-ea1b-43aa-9267-95fa9db56ed5
title: Método CBaseOutputPin. DecideAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e587562341118b904803302f0fd7249ebf8e507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660795"
---
# <a name="cbaseoutputpindecideallocator-method"></a><span data-ttu-id="edbb2-103">CBaseOutputPin. DecideAllocator, método</span><span class="sxs-lookup"><span data-stu-id="edbb2-103">CBaseOutputPin.DecideAllocator method</span></span>

<span data-ttu-id="edbb2-104">El `DecideAllocator` método selecciona un asignador de memoria.</span><span class="sxs-lookup"><span data-stu-id="edbb2-104">The `DecideAllocator` method selects a memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="edbb2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="edbb2-105">Syntax</span></span>


```C++
virtual HRESULT DecideAllocator(
   IMemInputPin  *pPin,
   IMemAllocator **pAlloc
);
```



## <a name="parameters"></a><span data-ttu-id="edbb2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edbb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edbb2-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="edbb2-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="edbb2-108">Puntero a la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) del PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="edbb2-108">Pointer to the input pin's [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="edbb2-109">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="edbb2-109">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="edbb2-110">Dirección de una variable que recibe un puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador.</span><span class="sxs-lookup"><span data-stu-id="edbb2-110">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edbb2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edbb2-111">Return value</span></span>

<span data-ttu-id="edbb2-112">Devuelve S \_ correcto si es correcto o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="edbb2-112">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="edbb2-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="edbb2-113">Remarks</span></span>

<span data-ttu-id="edbb2-114">Se llama a este método al final del proceso de conexión del PIN.</span><span class="sxs-lookup"><span data-stu-id="edbb2-114">This method is called at the end of the pin connection process.</span></span> <span data-ttu-id="edbb2-115">Realiza los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="edbb2-115">It performs the following steps:</span></span>

1.  <span data-ttu-id="edbb2-116">Llama al método [**IMemInputPin:: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) para recuperar los requisitos de búfer del PIN de entrada, si existe.</span><span class="sxs-lookup"><span data-stu-id="edbb2-116">Calls the [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) method to retrieve the input pin's buffer requirements, if any.</span></span>
2.  <span data-ttu-id="edbb2-117">Llama al método [**IMemInputPin:: GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) para solicitar un asignador del PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="edbb2-117">Calls the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method to request an allocator from the input pin.</span></span> <span data-ttu-id="edbb2-118">Si el PIN de entrada no proporciona un asignador, el PIN de salida crea uno llamando al método de la clase [**CBaseOutputPin:: InitAllocator**](cbaseoutputpin-initallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="edbb2-118">If the input pin does not provide an allocator, the output pin creates one by calling the [**CBaseOutputPin::InitAllocator**](cbaseoutputpin-initallocator.md) class method.</span></span>
3.  <span data-ttu-id="edbb2-119">Llama al método de clase [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) , que establece las propiedades de asignador.</span><span class="sxs-lookup"><span data-stu-id="edbb2-119">Calls the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) class method, which sets the allocator properties.</span></span> <span data-ttu-id="edbb2-120">Este es un método virtual puro; la clase derivada debe implementarla.</span><span class="sxs-lookup"><span data-stu-id="edbb2-120">This is a pure virtual method; the derived class must implement it.</span></span>
4.  <span data-ttu-id="edbb2-121">Llama al método [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) , que notifica a la clavija de entrada que se está usando el asignador.</span><span class="sxs-lookup"><span data-stu-id="edbb2-121">Calls the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method, which notifies the input pin of the allocator being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="edbb2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edbb2-122">Requirements</span></span>



| <span data-ttu-id="edbb2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="edbb2-123">Requirement</span></span> | <span data-ttu-id="edbb2-124">Value</span><span class="sxs-lookup"><span data-stu-id="edbb2-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edbb2-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="edbb2-125">Header</span></span><br/>  | <dl> <span data-ttu-id="edbb2-126"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="edbb2-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="edbb2-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="edbb2-127">Library</span></span><br/> | <dl> <span data-ttu-id="edbb2-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="edbb2-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edbb2-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="edbb2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edbb2-130">**Clase CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="edbb2-130">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




