---
description: 'El método SetProperties especifica el número de búferes que se van a asignar y el tamaño de cada búfer. Este método implementa el método IMemAllocator:: SetProperties.'
ms.assetid: f53c22a4-c01d-4d2f-81f0-bedf8f2ae5f0
title: Método CBaseAllocator. SetProperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 000da3ee359ad727e3af972fc4aa6d0dbbb9133e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690810"
---
# <a name="cbaseallocatorsetproperties-method"></a><span data-ttu-id="6c178-104">CBaseAllocator. SetProperties (método)</span><span class="sxs-lookup"><span data-stu-id="6c178-104">CBaseAllocator.SetProperties method</span></span>

<span data-ttu-id="6c178-105">El `SetProperties` método especifica el número de búferes que se van a asignar y el tamaño de cada búfer.</span><span class="sxs-lookup"><span data-stu-id="6c178-105">The `SetProperties` method specifies the number of buffers to allocate and the size of each buffer.</span></span> <span data-ttu-id="6c178-106">Este método implementa el método [**IMemAllocator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) .</span><span class="sxs-lookup"><span data-stu-id="6c178-106">This method implements the [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c178-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c178-107">Syntax</span></span>


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a><span data-ttu-id="6c178-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c178-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c178-109">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="6c178-109">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="6c178-110">Puntero a una estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contiene los requisitos de búfer.</span><span class="sxs-lookup"><span data-stu-id="6c178-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.</span></span>

</dd> <dt>

<span data-ttu-id="6c178-111">*pActual*</span><span class="sxs-lookup"><span data-stu-id="6c178-111">*pActual*</span></span> 
</dt> <dd>

<span data-ttu-id="6c178-112">Puntero a una estructura de **\_ propiedades de asignador** que recibe las propiedades de búfer reales.</span><span class="sxs-lookup"><span data-stu-id="6c178-112">Pointer to an **ALLOCATOR\_PROPERTIES** structure that receives the actual buffer properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c178-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c178-113">Return value</span></span>

<span data-ttu-id="6c178-114">Devuelve uno de los siguientes valores **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6c178-114">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="6c178-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6c178-115">Return code</span></span>                                                                                                 | <span data-ttu-id="6c178-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c178-116">Description</span></span>                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c178-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6c178-117"><dt>**S\_OK**</dt></span></span> </dl>                        | <span data-ttu-id="6c178-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="6c178-118">Success.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="6c178-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="6c178-119"><dt>**E\_POINTER**</dt></span></span> </dl>                   | <span data-ttu-id="6c178-120">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="6c178-120">**NULL** pointer argument.</span></span><br/>                                 |
| <dl> <span data-ttu-id="6c178-121"><dt>**VFW \_ E \_ ya \_ confirmado**</dt></span><span class="sxs-lookup"><span data-stu-id="6c178-121"><dt>**VFW\_E\_ALREADY\_COMMITTED**</dt></span></span> </dl>   | <span data-ttu-id="6c178-122">No se puede cambiar la memoria asignada mientras el filtro está activo.</span><span class="sxs-lookup"><span data-stu-id="6c178-122">Cannot change allocated memory while the filter is active.</span></span><br/> |
| <dl> <span data-ttu-id="6c178-123"><dt>**VFW \_ E \_ BADALIGN**</dt></span><span class="sxs-lookup"><span data-stu-id="6c178-123"><dt>**VFW\_E\_BADALIGN**</dt></span></span> </dl>             | <span data-ttu-id="6c178-124">Se especificó una alineación no válida.</span><span class="sxs-lookup"><span data-stu-id="6c178-124">An invalid alignment was specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="6c178-125"><dt>**\_ \_ búferes VFW E \_ pendientes**</dt></span><span class="sxs-lookup"><span data-stu-id="6c178-125"><dt>**VFW\_E\_BUFFERS\_OUTSTANDING**</dt></span></span> </dl> | <span data-ttu-id="6c178-126">Uno o más búferes siguen activos.</span><span class="sxs-lookup"><span data-stu-id="6c178-126">One or more buffers are still active.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="6c178-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c178-127">Remarks</span></span>

<span data-ttu-id="6c178-128">Este método especifica los requisitos de búfer, pero no asigna ningún búfer.</span><span class="sxs-lookup"><span data-stu-id="6c178-128">This method specifies the buffer requirements, but does not allocate any buffers.</span></span> <span data-ttu-id="6c178-129">Llame al método [**CBaseAllocator:: commit**](cbaseallocator-commit.md) para asignar búferes.</span><span class="sxs-lookup"><span data-stu-id="6c178-129">Call the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method to allocate buffers.</span></span>

<span data-ttu-id="6c178-130">El autor de la llamada asigna dos estructuras de propiedades de ASIGNADOr \_ .</span><span class="sxs-lookup"><span data-stu-id="6c178-130">The caller allocates two ALLOCATOR\_PROPERTIES structures.</span></span> <span data-ttu-id="6c178-131">El parámetro *pRequest* contiene los requisitos de búfer del llamador, incluido el número de búferes y el tamaño de cada búfer.</span><span class="sxs-lookup"><span data-stu-id="6c178-131">The *pRequest* parameter contains the caller's buffer requirements, including the number of buffers and the size of each buffer.</span></span> <span data-ttu-id="6c178-132">Cuando el método devuelve, el parámetro *pActual* contiene las propiedades de búfer reales, tal como se establece en el asignador.</span><span class="sxs-lookup"><span data-stu-id="6c178-132">When the method returns, the *pActual* parameter contains the actual buffer properties, as set by the allocator.</span></span> <span data-ttu-id="6c178-133">En la clase base, suponiendo que el método se ejecuta correctamente, las propiedades reales siempre coinciden con las propiedades solicitadas.</span><span class="sxs-lookup"><span data-stu-id="6c178-133">In the base class, assuming that the method succeeds, the actual properties always match the requested properties.</span></span> <span data-ttu-id="6c178-134">Las clases derivadas pueden invalidar este comportamiento.</span><span class="sxs-lookup"><span data-stu-id="6c178-134">Derived classes might override this behavior.</span></span>

<span data-ttu-id="6c178-135">El asignador no debe confirmarse y no debe tener búferes pendientes.</span><span class="sxs-lookup"><span data-stu-id="6c178-135">The allocator must not be committed, and must not have outstanding buffers.</span></span> <span data-ttu-id="6c178-136">En la clase base, la alineación debe ser igual a 1.</span><span class="sxs-lookup"><span data-stu-id="6c178-136">In the base class, the alignment must equal 1.</span></span> <span data-ttu-id="6c178-137">La clase [**CMemAllocator**](cmemallocator.md) invalida este requisito.</span><span class="sxs-lookup"><span data-stu-id="6c178-137">The [**CMemAllocator**](cmemallocator.md) class overrides this requirement.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c178-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c178-138">Requirements</span></span>



| <span data-ttu-id="6c178-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c178-139">Requirement</span></span> | <span data-ttu-id="6c178-140">Value</span><span class="sxs-lookup"><span data-stu-id="6c178-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c178-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c178-141">Header</span></span><br/>  | <dl> <span data-ttu-id="6c178-142"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c178-142"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6c178-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6c178-143">Library</span></span><br/> | <dl> <span data-ttu-id="6c178-144"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6c178-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c178-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c178-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c178-146">**Clase CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="6c178-146">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




