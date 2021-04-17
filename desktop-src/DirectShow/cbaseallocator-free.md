---
description: El método Free libera toda la memoria del búfer. Se llama a este método cuando el filtro propietario anula la confirmación del asignador después de que se libere el último ejemplo multimedia.
ms.assetid: dd1e6c4d-762a-4caf-902b-015c6c9fdb4d
title: Método CBaseAllocator. Free (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3534eac01a6769e090c8c808f16cc6ad5c6b84c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670879"
---
# <a name="cbaseallocatorfree-method"></a><span data-ttu-id="1852a-104">Método CBaseAllocator. Free</span><span class="sxs-lookup"><span data-stu-id="1852a-104">CBaseAllocator.Free method</span></span>

<span data-ttu-id="1852a-105">El `Free` método libera toda la memoria del búfer.</span><span class="sxs-lookup"><span data-stu-id="1852a-105">The `Free` method releases all of the buffer memory.</span></span> <span data-ttu-id="1852a-106">Se llama a este método cuando el filtro propietario anula la confirmación del asignador después de que se libere el último ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="1852a-106">This method is called when the owning filter decommits the allocator, after the last media sample is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="1852a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1852a-107">Syntax</span></span>


```C++
virtual void Free() = 0;
```



## <a name="parameters"></a><span data-ttu-id="1852a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1852a-108">Parameters</span></span>

<span data-ttu-id="1852a-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1852a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1852a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1852a-110">Return value</span></span>

<span data-ttu-id="1852a-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1852a-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1852a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1852a-112">Remarks</span></span>

<span data-ttu-id="1852a-113">Después de llamar al método de [**anulación de confirmación**](cbaseallocator-decommit.md) , el asignador llama a este método cuando libera el último ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="1852a-113">After the [**Decommit**](cbaseallocator-decommit.md) method is called, the allocator calls this method when it releases the last media sample.</span></span> <span data-ttu-id="1852a-114">La clase derivada debe implementar este método.</span><span class="sxs-lookup"><span data-stu-id="1852a-114">The derived class must implement this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1852a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1852a-115">Requirements</span></span>



| <span data-ttu-id="1852a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1852a-116">Requirement</span></span> | <span data-ttu-id="1852a-117">Value</span><span class="sxs-lookup"><span data-stu-id="1852a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1852a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1852a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1852a-119"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1852a-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1852a-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1852a-120">Library</span></span><br/> | <dl> <span data-ttu-id="1852a-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1852a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1852a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="1852a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1852a-123">**Clase CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="1852a-123">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




