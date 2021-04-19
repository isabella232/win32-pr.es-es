---
description: 'El método GetProperties recupera el número de búferes que va a crear el asignador y las propiedades del búfer. Este método implementa el método IMemAllocator:: GetProperties.'
ms.assetid: ccee4d69-52fc-4e3c-b6a4-787914708be4
title: Método CBaseAllocator. GetProperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abf143b11b6dd67fca6c87f9a31ce69f18951311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660610"
---
# <a name="cbaseallocatorgetproperties-method"></a><span data-ttu-id="878d8-104">CBaseAllocator. GetProperties (método)</span><span class="sxs-lookup"><span data-stu-id="878d8-104">CBaseAllocator.GetProperties method</span></span>

<span data-ttu-id="878d8-105">El `GetProperties` método recupera el número de búferes que va a crear el asignador y las propiedades del búfer.</span><span class="sxs-lookup"><span data-stu-id="878d8-105">The `GetProperties` method retrieves the number of buffers that the allocator will create, and the buffer properties.</span></span> <span data-ttu-id="878d8-106">Este método implementa el método [**IMemAllocator:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) .</span><span class="sxs-lookup"><span data-stu-id="878d8-106">This method implements the [**IMemAllocator::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="878d8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="878d8-107">Syntax</span></span>


```C++
HRESULT GetProperties(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="878d8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="878d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="878d8-109">*pProps*</span><span class="sxs-lookup"><span data-stu-id="878d8-109">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="878d8-110">Puntero a una estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que recibe las propiedades de asignador.</span><span class="sxs-lookup"><span data-stu-id="878d8-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that receives the allocator properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="878d8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="878d8-111">Return value</span></span>

<span data-ttu-id="878d8-112">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="878d8-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="878d8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="878d8-113">Requirements</span></span>



| <span data-ttu-id="878d8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="878d8-114">Requirement</span></span> | <span data-ttu-id="878d8-115">Value</span><span class="sxs-lookup"><span data-stu-id="878d8-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="878d8-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="878d8-116">Header</span></span><br/>  | <dl> <span data-ttu-id="878d8-117"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="878d8-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="878d8-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="878d8-118">Library</span></span><br/> | <dl> <span data-ttu-id="878d8-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="878d8-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="878d8-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="878d8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="878d8-121">**Clase CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="878d8-121">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




