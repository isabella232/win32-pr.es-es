---
description: 'El método GetAllocator recupera el asignador de memoria propuesto por este pin. Este método implementa el método IMemInputPin:: GetAllocator.'
ms.assetid: e9db4aa0-4f53-4ca4-babb-5e0215c7c284
title: Método CTransInPlaceInputPin. GetAllocator (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7798640297539a8fa8f6349c799e61e7e22a453d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679260"
---
# <a name="ctransinplaceinputpingetallocator-method"></a><span data-ttu-id="f456f-104">CTransInPlaceInputPin. GetAllocator, método</span><span class="sxs-lookup"><span data-stu-id="f456f-104">CTransInPlaceInputPin.GetAllocator method</span></span>

<span data-ttu-id="f456f-105">El `GetAllocator` método recupera el asignador de memoria propuesto por este pin.</span><span class="sxs-lookup"><span data-stu-id="f456f-105">The `GetAllocator` method retrieves the memory allocator proposed by this pin.</span></span> <span data-ttu-id="f456f-106">Este método implementa el método [**IMemInputPin:: GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) .</span><span class="sxs-lookup"><span data-stu-id="f456f-106">This method implements the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f456f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f456f-107">Syntax</span></span>


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="f456f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f456f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f456f-109">*ppAllocator*</span><span class="sxs-lookup"><span data-stu-id="f456f-109">*ppAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="f456f-110">Recibe un puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador.</span><span class="sxs-lookup"><span data-stu-id="f456f-110">Receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f456f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f456f-111">Return value</span></span>

<span data-ttu-id="f456f-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f456f-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f456f-113">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f456f-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="f456f-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f456f-114">Return code</span></span>                                                                                          | <span data-ttu-id="f456f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="f456f-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="f456f-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f456f-116"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="f456f-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="f456f-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="f456f-118"><dt>**VFW \_ E \_ no \_ asignador**</dt></span><span class="sxs-lookup"><span data-stu-id="f456f-118"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="f456f-119">No hay ningún asignador disponible.</span><span class="sxs-lookup"><span data-stu-id="f456f-119">No allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f456f-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f456f-120">Remarks</span></span>

<span data-ttu-id="f456f-121">Si el PIN de salida del filtro está conectado, este método solicita un asignador del PIN de entrada del filtro de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="f456f-121">If the filter's output pin is connected, this method requests an allocator from the downstream filter's input pin.</span></span>

<span data-ttu-id="f456f-122">Si el PIN de salida del filtro no está conectado, este método crea un asignador temporal.</span><span class="sxs-lookup"><span data-stu-id="f456f-122">If the filter's output pin is not connected, this method creates a temporary allocator.</span></span> <span data-ttu-id="f456f-123">Más adelante, cuando el PIN de salida esté conectado, el filtro volverá a conectar el PIN de entrada y renegociará el asignador.</span><span class="sxs-lookup"><span data-stu-id="f456f-123">Later, when the output pin is connected, the filter will reconnect the input pin and renegotiate the allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="f456f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f456f-124">Requirements</span></span>



| <span data-ttu-id="f456f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f456f-125">Requirement</span></span> | <span data-ttu-id="f456f-126">Value</span><span class="sxs-lookup"><span data-stu-id="f456f-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f456f-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f456f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f456f-128"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f456f-128"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f456f-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f456f-129">Library</span></span><br/> | <dl> <span data-ttu-id="f456f-130"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f456f-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f456f-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f456f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f456f-132">**Clase CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="f456f-132">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




