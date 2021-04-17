---
description: El método GetAllocatorRequirements recupera las propiedades de asignador solicitadas por el PIN de entrada.
ms.assetid: 81564924-6d5b-4b2a-b549-e3f358f18371
title: Método CBaseInputPin. GetAllocatorRequirements (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0239d226ea57ed5953fa65b925eeffaa0b13df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660343"
---
# <a name="cbaseinputpingetallocatorrequirements-method"></a><span data-ttu-id="66208-103">CBaseInputPin. GetAllocatorRequirements, método</span><span class="sxs-lookup"><span data-stu-id="66208-103">CBaseInputPin.GetAllocatorRequirements method</span></span>

<span data-ttu-id="66208-104">El `GetAllocatorRequirements` método recupera las propiedades de asignador solicitadas por el PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="66208-104">The `GetAllocatorRequirements` method retrieves the allocator properties requested by the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="66208-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66208-105">Syntax</span></span>


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="66208-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66208-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66208-107">*pProps*</span><span class="sxs-lookup"><span data-stu-id="66208-107">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="66208-108">Puntero a una estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , que se rellena con los requisitos.</span><span class="sxs-lookup"><span data-stu-id="66208-108">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure, which is filled in with the requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66208-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66208-109">Return value</span></span>

<span data-ttu-id="66208-110">Devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="66208-110">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="66208-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66208-111">Remarks</span></span>

<span data-ttu-id="66208-112">Cuando un terminal de salida Inicializa un asignador de memoria, puede llamar a este método para determinar si el PIN de entrada tiene algún requisito de búfer.</span><span class="sxs-lookup"><span data-stu-id="66208-112">When an output pin initializes a memory allocator, it can call this method to determine whether the input pin has any buffer requirements.</span></span> <span data-ttu-id="66208-113">Para obtener más información, vea [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md).</span><span class="sxs-lookup"><span data-stu-id="66208-113">For more information, see [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md).</span></span>

<span data-ttu-id="66208-114">La implementación de este método es opcional.</span><span class="sxs-lookup"><span data-stu-id="66208-114">Implementing this method is optional.</span></span> <span data-ttu-id="66208-115">Si el filtro tiene requisitos de alineación o prefijo específicos, Invalide este método.</span><span class="sxs-lookup"><span data-stu-id="66208-115">If the filter has specific alignment or prefix requirements, override this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="66208-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66208-116">Requirements</span></span>



| <span data-ttu-id="66208-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="66208-117">Requirement</span></span> | <span data-ttu-id="66208-118">Value</span><span class="sxs-lookup"><span data-stu-id="66208-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66208-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66208-119">Header</span></span><br/>  | <dl> <span data-ttu-id="66208-120"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66208-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="66208-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66208-121">Library</span></span><br/> | <dl> <span data-ttu-id="66208-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="66208-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66208-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="66208-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66208-124">**Clase CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="66208-124">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




