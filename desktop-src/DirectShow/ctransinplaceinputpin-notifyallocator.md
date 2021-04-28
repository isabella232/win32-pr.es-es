---
description: 'Método CTransInPlaceInputPin.NotifyAllocator: el método NotifyAllocator especifica un asignador para la conexión. Este método implementa el método IMemInputPin::NotifyAllocator.'
ms.assetid: adc1c5b6-99da-4140-b644-7b98f6b8bad4
title: Método CTransInPlaceInputPin.NotifyAllocator (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca15be5dc1893a393e6052832cc7522f27355eeb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094753"
---
# <a name="ctransinplaceinputpinnotifyallocator-method"></a><span data-ttu-id="ae71e-104">CTransInPlaceInputPin.NotifyAllocator (método)</span><span class="sxs-lookup"><span data-stu-id="ae71e-104">CTransInPlaceInputPin.NotifyAllocator method</span></span>

<span data-ttu-id="ae71e-105">El `NotifyAllocator` método especifica un asignador para la conexión.</span><span class="sxs-lookup"><span data-stu-id="ae71e-105">The `NotifyAllocator` method specifies an allocator for the connection.</span></span> <span data-ttu-id="ae71e-106">Este método implementa el [**método IMemInputPin::NotifyAllocator.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator)</span><span class="sxs-lookup"><span data-stu-id="ae71e-106">This method implements the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae71e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae71e-107">Syntax</span></span>


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a><span data-ttu-id="ae71e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae71e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae71e-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="ae71e-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="ae71e-110">Puntero a la interfaz [**IMemAllocator del asignador.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)</span><span class="sxs-lookup"><span data-stu-id="ae71e-110">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="ae71e-111">*bReadOnly*</span><span class="sxs-lookup"><span data-stu-id="ae71e-111">*bReadOnly*</span></span> 
</dt> <dd>

<span data-ttu-id="ae71e-112">Marca que especifica si las muestras de este asignador son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ae71e-112">Flag that specifies whether samples from this allocator are read-only.</span></span> <span data-ttu-id="ae71e-113">Si **es TRUE,** los ejemplos son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ae71e-113">If **TRUE**, samples are read-only.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae71e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae71e-114">Return value</span></span>

<span data-ttu-id="ae71e-115">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="ae71e-115">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ae71e-116">Los valores posibles incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ae71e-116">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="ae71e-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ae71e-117">Return code</span></span>                                                                               | <span data-ttu-id="ae71e-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae71e-118">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="ae71e-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ae71e-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="ae71e-120">Correcto</span><span class="sxs-lookup"><span data-stu-id="ae71e-120">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="ae71e-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="ae71e-121"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="ae71e-122">Error</span><span class="sxs-lookup"><span data-stu-id="ae71e-122">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="ae71e-123"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="ae71e-123"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="ae71e-124">**Argumento de** puntero NULL</span><span class="sxs-lookup"><span data-stu-id="ae71e-124">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ae71e-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ae71e-125">Remarks</span></span>

<span data-ttu-id="ae71e-126">El filtro intenta usar el mismo asignador para ambas conexiones de pin.</span><span class="sxs-lookup"><span data-stu-id="ae71e-126">The filter attempts to use the same allocator for both pin connections.</span></span>

-   <span data-ttu-id="ae71e-127">Si el pin de salida no está conectado, el pin de entrada acepta automáticamente el asignador.</span><span class="sxs-lookup"><span data-stu-id="ae71e-127">If the output pin is not connected, the input pin automatically accepts the allocator.</span></span> <span data-ttu-id="ae71e-128">Cuando el pin de salida está conectado, el filtro volverá a conectar el pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="ae71e-128">When the output pin is connected, the filter will reconnect the input pin.</span></span> <span data-ttu-id="ae71e-129">En ese momento, el filtro intentará de nuevo usar un solo asignador.</span><span class="sxs-lookup"><span data-stu-id="ae71e-129">At that point, the filter will try again to use a single allocator.</span></span>
-   <span data-ttu-id="ae71e-130">Si el pin de salida está conectado, el pin de entrada acepta el asignador.</span><span class="sxs-lookup"><span data-stu-id="ae71e-130">If the output pin is connected, the input pin accepts the allocator.</span></span> <span data-ttu-id="ae71e-131">El pin de salida también usa el mismo asignador.</span><span class="sxs-lookup"><span data-stu-id="ae71e-131">The output pin also uses the same allocator.</span></span> <span data-ttu-id="ae71e-132">Llama a `NotifyAllocator` en el pin de entrada de bajada.</span><span class="sxs-lookup"><span data-stu-id="ae71e-132">It calls `NotifyAllocator` on the downstream input pin.</span></span>

<span data-ttu-id="ae71e-133">El caso anterior tiene la siguiente excepción:</span><span class="sxs-lookup"><span data-stu-id="ae71e-133">The previous case has the following exception:</span></span>

-   <span data-ttu-id="ae71e-134">Si el asignador propuesto es de solo lectura (es decir, el parámetro *bReadOnly* es **TRUE)** y el filtro necesita modificar los ejemplos, el filtro debe usar dos asignadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="ae71e-134">If the proposed allocator is read-only (that is, the *bReadOnly* parameter is **TRUE**) and the filter needs to modify the samples, then the filter must use two different allocators.</span></span> <span data-ttu-id="ae71e-135">En este caso, si el filtro ascendente está proponiendo usar el asignador del filtro de bajada, el método devuelve E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="ae71e-135">In this case, if the upstream filter is proposing to use the downstream filter's allocator, the method returns E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae71e-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae71e-136">Requirements</span></span>



| <span data-ttu-id="ae71e-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae71e-137">Requirement</span></span> | <span data-ttu-id="ae71e-138">Value</span><span class="sxs-lookup"><span data-stu-id="ae71e-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae71e-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae71e-139">Header</span></span><br/>  | <dl> <span data-ttu-id="ae71e-140"><dt>Transip.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae71e-140"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ae71e-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ae71e-141">Library</span></span><br/> | <dl> <span data-ttu-id="ae71e-142"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ae71e-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae71e-143">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ae71e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae71e-144">**CTransInPlaceInputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="ae71e-144">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




