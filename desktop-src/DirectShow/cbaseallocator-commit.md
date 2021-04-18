---
description: 'El método commit asigna la memoria de los búferes. Este método implementa el método IMemAllocator:: commit.'
ms.assetid: e8c36276-0229-428f-b030-978651ab7534
title: Método CBaseAllocator. Commit (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Commit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b49fae72e5588105b1235c1f0c461d5cc45cfa2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670880"
---
# <a name="cbaseallocatorcommit-method"></a><span data-ttu-id="4cd0b-104">CBaseAllocator. Commit (método)</span><span class="sxs-lookup"><span data-stu-id="4cd0b-104">CBaseAllocator.Commit method</span></span>

<span data-ttu-id="4cd0b-105">El `Commit` método asigna la memoria de los búferes.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-105">The `Commit` method allocates the memory for the buffers.</span></span> <span data-ttu-id="4cd0b-106">Este método implementa el método [**IMemAllocator:: commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) .</span><span class="sxs-lookup"><span data-stu-id="4cd0b-106">This method implements the [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cd0b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4cd0b-107">Syntax</span></span>


```C++
HRESULT Commit();
```



## <a name="parameters"></a><span data-ttu-id="4cd0b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4cd0b-108">Parameters</span></span>

<span data-ttu-id="4cd0b-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4cd0b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4cd0b-110">Return value</span></span>

<span data-ttu-id="4cd0b-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4cd0b-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4cd0b-112">Entre los valores posibles se incluyen los de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-112">Possible values include those in the following list.</span></span>



| <span data-ttu-id="4cd0b-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4cd0b-113">Return code</span></span>                                                                                       | <span data-ttu-id="4cd0b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4cd0b-114">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="4cd0b-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="4cd0b-115"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="4cd0b-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="4cd0b-117"><dt>**VFW \_ E \_ SIZENOTSET**</dt></span><span class="sxs-lookup"><span data-stu-id="4cd0b-117"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="4cd0b-118">No se especificaron los requisitos de búfer.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-118">Buffer requirements were not specified.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4cd0b-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4cd0b-119">Remarks</span></span>

<span data-ttu-id="4cd0b-120">Antes de llamar a este método, llame al método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) para especificar los requisitos de búfer.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-120">Before calling this method, call the [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method to specify the buffer requirements.</span></span>

<span data-ttu-id="4cd0b-121">Este método llama al método virtual [**CBaseAllocator:: Alloc**](cbaseallocator-alloc.md) para asignar la memoria de los búferes.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-121">This method calls the virtual method [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) to allocate the memory for the buffers.</span></span> <span data-ttu-id="4cd0b-122">Las clases derivadas pueden invalidar **Alloc**.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-122">Derived classes can override **Alloc**.</span></span> <span data-ttu-id="4cd0b-123">Si hay pendiente una operación de desconfirmación, se cancela.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-123">If a decommit operation is pending, it is canceled.</span></span>

<span data-ttu-id="4cd0b-124">Debe llamar a este método antes de llamar al método [**CBaseAllocator:: getBuffer**](cbaseallocator-getbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="4cd0b-124">You must call this method before calling the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cd0b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cd0b-125">Requirements</span></span>



| <span data-ttu-id="4cd0b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cd0b-126">Requirement</span></span> | <span data-ttu-id="4cd0b-127">Value</span><span class="sxs-lookup"><span data-stu-id="4cd0b-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cd0b-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4cd0b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="4cd0b-129"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4cd0b-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4cd0b-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4cd0b-130">Library</span></span><br/> | <dl> <span data-ttu-id="4cd0b-131"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4cd0b-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cd0b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="4cd0b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cd0b-133">**Clase CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="4cd0b-133">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




