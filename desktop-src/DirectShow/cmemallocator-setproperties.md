---
description: El método SetProperties especifica el número de búferes que se van a asignar y el tamaño de cada búfer.
ms.assetid: 01f63379-1d66-4a72-b87c-de55504b0bb4
title: Método CMemAllocator. SetProperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8505916245cca81fdd84132e4523fe9dd03b971b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680353"
---
# <a name="cmemallocatorsetproperties-method"></a><span data-ttu-id="0f619-103">CMemAllocator. SetProperties (método)</span><span class="sxs-lookup"><span data-stu-id="0f619-103">CMemAllocator.SetProperties method</span></span>

<span data-ttu-id="0f619-104">El `SetProperties` método especifica el número de búferes que se van a asignar y el tamaño de cada búfer.</span><span class="sxs-lookup"><span data-stu-id="0f619-104">The `SetProperties` method specifies the number of buffers to allocate and the size of each buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f619-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f619-105">Syntax</span></span>


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a><span data-ttu-id="0f619-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f619-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f619-107">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="0f619-107">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="0f619-108">Puntero a una estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contiene los requisitos de búfer.</span><span class="sxs-lookup"><span data-stu-id="0f619-108">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.</span></span>

</dd> <dt>

<span data-ttu-id="0f619-109">*pActual*</span><span class="sxs-lookup"><span data-stu-id="0f619-109">*pActual*</span></span> 
</dt> <dd>

<span data-ttu-id="0f619-110">Puntero a una estructura de **\_ propiedades de asignador** que recibe las propiedades de búfer reales.</span><span class="sxs-lookup"><span data-stu-id="0f619-110">Pointer to an **ALLOCATOR\_PROPERTIES** structure that receives the actual buffer properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f619-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f619-111">Return value</span></span>

<span data-ttu-id="0f619-112">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="0f619-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="0f619-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0f619-113">Return code</span></span>                                                                                                 | <span data-ttu-id="0f619-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f619-114">Description</span></span>                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="0f619-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0f619-115"><dt>**S\_OK**</dt></span></span> </dl>                        | <span data-ttu-id="0f619-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="0f619-116">Success.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="0f619-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="0f619-117"><dt>**E\_POINTER**</dt></span></span> </dl>                   | <span data-ttu-id="0f619-118">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="0f619-118">**NULL** pointer argument.</span></span><br/>                                 |
| <dl> <span data-ttu-id="0f619-119"><dt>**VFW \_ E \_ ya \_ confirmado**</dt></span><span class="sxs-lookup"><span data-stu-id="0f619-119"><dt>**VFW\_E\_ALREADY\_COMMITTED**</dt></span></span> </dl>   | <span data-ttu-id="0f619-120">No se puede cambiar la memoria asignada mientras el filtro está activo.</span><span class="sxs-lookup"><span data-stu-id="0f619-120">Cannot change allocated memory while the filter is active.</span></span><br/> |
| <dl> <span data-ttu-id="0f619-121"><dt>**VFW \_ E \_ BADALIGN**</dt></span><span class="sxs-lookup"><span data-stu-id="0f619-121"><dt>**VFW\_E\_BADALIGN**</dt></span></span> </dl>             | <span data-ttu-id="0f619-122">Se especificó una alineación no válida.</span><span class="sxs-lookup"><span data-stu-id="0f619-122">An invalid alignment was specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="0f619-123"><dt>**\_ \_ búferes VFW E \_ pendientes**</dt></span><span class="sxs-lookup"><span data-stu-id="0f619-123"><dt>**VFW\_E\_BUFFERS\_OUTSTANDING**</dt></span></span> </dl> | <span data-ttu-id="0f619-124">Uno o más búferes siguen activos.</span><span class="sxs-lookup"><span data-stu-id="0f619-124">One or more buffers are still active.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="0f619-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f619-125">Remarks</span></span>

<span data-ttu-id="0f619-126">Este método invalida el método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="0f619-126">This method overrides the [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method.</span></span>

<span data-ttu-id="0f619-127">La alineación del búfer, especificada por el miembro **cbAlign** de la estructura de **\_ propiedades de asignador** , debe ser una potencia uniforme de dos.</span><span class="sxs-lookup"><span data-stu-id="0f619-127">The buffer alignment, specified by the **cbAlign** member of the **ALLOCATOR\_PROPERTIES** structure, must be an even power of two.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f619-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f619-128">Requirements</span></span>



| <span data-ttu-id="0f619-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f619-129">Requirement</span></span> | <span data-ttu-id="0f619-130">Value</span><span class="sxs-lookup"><span data-stu-id="0f619-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f619-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f619-131">Header</span></span><br/>  | <dl> <span data-ttu-id="0f619-132"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f619-132"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0f619-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0f619-133">Library</span></span><br/> | <dl> <span data-ttu-id="0f619-134"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0f619-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f619-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f619-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f619-136">**Clase CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="0f619-136">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




