---
description: 'El método SetProperties especifica el número de búferes que se van a asignar y el tamaño de cada búfer. Este método invalida el método CBaseAllocator:: SetProperties.'
ms.assetid: 8d419432-a9a7-44fb-b916-8dacd08eb6ec
title: Método CImageAllocator. SetProperties (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c04501fe3511d9cdd45f3513c68082d2ffece0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661123"
---
# <a name="cimageallocatorsetproperties-method"></a><span data-ttu-id="44aa8-104">CImageAllocator. SetProperties (método)</span><span class="sxs-lookup"><span data-stu-id="44aa8-104">CImageAllocator.SetProperties method</span></span>

<span data-ttu-id="44aa8-105">El `SetProperties` método especifica el número de búferes que se van a asignar y el tamaño de cada búfer.</span><span class="sxs-lookup"><span data-stu-id="44aa8-105">The `SetProperties` method specifies the number of buffers to allocate and the size of each buffer.</span></span> <span data-ttu-id="44aa8-106">Este método invalida el método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="44aa8-106">This method overrides the [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="44aa8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44aa8-107">Syntax</span></span>


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a><span data-ttu-id="44aa8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44aa8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44aa8-109">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="44aa8-109">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="44aa8-110">Puntero a una estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contiene los requisitos de búfer.</span><span class="sxs-lookup"><span data-stu-id="44aa8-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.</span></span>

</dd> <dt>

<span data-ttu-id="44aa8-111">*pActual*</span><span class="sxs-lookup"><span data-stu-id="44aa8-111">*pActual*</span></span> 
</dt> <dd>

<span data-ttu-id="44aa8-112">Puntero a una estructura de **\_ propiedades de asignador** que recibe las propiedades de búfer reales.</span><span class="sxs-lookup"><span data-stu-id="44aa8-112">Pointer to an **ALLOCATOR\_PROPERTIES** structure that receives the actual buffer properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44aa8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44aa8-113">Return value</span></span>

<span data-ttu-id="44aa8-114">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="44aa8-114">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="44aa8-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44aa8-115">Remarks</span></span>

<span data-ttu-id="44aa8-116">Este método llama a [**CImageAllocator:: CheckSizes**](cimageallocator-checksizes.md) para validar el tamaño de búfer solicitado.</span><span class="sxs-lookup"><span data-stu-id="44aa8-116">This method calls [**CImageAllocator::CheckSizes**](cimageallocator-checksizes.md) to validate the requested buffer size.</span></span> <span data-ttu-id="44aa8-117">También llama a la versión de la clase base de `SetProperties` .</span><span class="sxs-lookup"><span data-stu-id="44aa8-117">It also calls the base-class version of `SetProperties`.</span></span>

## <a name="requirements"></a><span data-ttu-id="44aa8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44aa8-118">Requirements</span></span>



| <span data-ttu-id="44aa8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="44aa8-119">Requirement</span></span> | <span data-ttu-id="44aa8-120">Value</span><span class="sxs-lookup"><span data-stu-id="44aa8-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44aa8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44aa8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="44aa8-122"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44aa8-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="44aa8-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="44aa8-123">Library</span></span><br/> | <dl> <span data-ttu-id="44aa8-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="44aa8-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44aa8-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="44aa8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44aa8-126">**Clase CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="44aa8-126">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




