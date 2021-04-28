---
description: 'Constructor CBaseAllocator.CBaseAllocator: método constructor.'
ms.assetid: e697e377-6407-4316-9f04-fe3bdb814175
title: Constructor CBaseAllocator.CBaseAllocator (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfda2b03d1ddb3f4a8ad5f4446dbee997da4e790
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096372"
---
# <a name="cbaseallocatorcbaseallocator-constructor"></a><span data-ttu-id="9447a-103">Constructor CBaseAllocator.CBaseAllocator</span><span class="sxs-lookup"><span data-stu-id="9447a-103">CBaseAllocator.CBaseAllocator constructor</span></span>

<span data-ttu-id="9447a-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="9447a-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9447a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9447a-105">Syntax</span></span>


```C++
CBaseAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   BOOL      bEvent = TRUE,
   BOOL      fEnableReleaseCallback = FALSE
);
```



## <a name="parameters"></a><span data-ttu-id="9447a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9447a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9447a-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="9447a-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="9447a-108">Puntero a una cadena que contiene el nombre de depuración del asignador.</span><span class="sxs-lookup"><span data-stu-id="9447a-108">Pointer to a string containing the debug name of the allocator.</span></span> <span data-ttu-id="9447a-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="9447a-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="9447a-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="9447a-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="9447a-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="9447a-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="9447a-112">Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="9447a-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="9447a-113">De lo contrario, establezca este parámetro en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="9447a-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9447a-114">*Phr*</span><span class="sxs-lookup"><span data-stu-id="9447a-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="9447a-115">Puntero a un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="9447a-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="9447a-116">Establezca el valor en S \_ OK antes de crear el objeto.</span><span class="sxs-lookup"><span data-stu-id="9447a-116">Set the value to S\_OK before creating the object.</span></span> <span data-ttu-id="9447a-117">Si se produce un error en el constructor, el valor se establece en un código de error.</span><span class="sxs-lookup"><span data-stu-id="9447a-117">If the constructor fails, the value is set to an error code.</span></span>

</dd> <dt>

<span data-ttu-id="9447a-118">*bEvent*</span><span class="sxs-lookup"><span data-stu-id="9447a-118">*bEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="9447a-119">Valor booleano que indica si se va a crear un semáforo.</span><span class="sxs-lookup"><span data-stu-id="9447a-119">Boolean value indicating whether to create a semaphore.</span></span> <span data-ttu-id="9447a-120">Si **es TRUE,** el asignador crea un semáforo ([**CBaseAllocator::m \_ hSem**](cbaseallocator-m-hsem.md)), que se señala cada vez que hay disponible un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="9447a-120">If **TRUE**, the allocator creates a semaphore ([**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md)), which is signaled whenever a sample becomes available.</span></span> <span data-ttu-id="9447a-121">Establezca el valor en **FALSE** si va a implementar una clase derivada que no requiere un semáforo.</span><span class="sxs-lookup"><span data-stu-id="9447a-121">Set the value to **FALSE** if you are implementing a derived class that does not require a semaphore.</span></span>

</dd> <dt>

<span data-ttu-id="9447a-122">*fEnableReleaseCallback*</span><span class="sxs-lookup"><span data-stu-id="9447a-122">*fEnableReleaseCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="9447a-123">Valor booleano que indica si el mecanismo de devolución de llamada de versión está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9447a-123">Boolean value indicating whether the release callback mechanism is enabled.</span></span> <span data-ttu-id="9447a-124">Establezca el valor en **TRUE si** desea proporcionar una interfaz de devolución de llamada, a la que se llama cuando se liberan búferes.</span><span class="sxs-lookup"><span data-stu-id="9447a-124">Set the value to **TRUE** if you want to supply a callback interface, which is called when buffers are released.</span></span> <span data-ttu-id="9447a-125">Especifique la devolución de llamada llamando al [**método CBaseAllocator::SetNotify.**](cbaseallocator-setnotify.md)</span><span class="sxs-lookup"><span data-stu-id="9447a-125">Specify the callback by calling the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9447a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9447a-126">Requirements</span></span>



| <span data-ttu-id="9447a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9447a-127">Requirement</span></span> | <span data-ttu-id="9447a-128">Value</span><span class="sxs-lookup"><span data-stu-id="9447a-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9447a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9447a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="9447a-130"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="9447a-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9447a-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9447a-131">Library</span></span><br/> | <dl> <span data-ttu-id="9447a-132"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9447a-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9447a-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9447a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9447a-134">**CBaseAllocator (clase)**</span><span class="sxs-lookup"><span data-stu-id="9447a-134">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




