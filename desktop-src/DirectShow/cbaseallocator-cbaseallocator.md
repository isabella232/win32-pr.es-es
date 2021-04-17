---
description: Método de constructor.
ms.assetid: e697e377-6407-4316-9f04-fe3bdb814175
title: Constructor CBaseAllocator. CBaseAllocator (Amfilter. h)
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
ms.openlocfilehash: 98a1ba1163058f92fba666177d0ff82331dd528c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660116"
---
# <a name="cbaseallocatorcbaseallocator-constructor"></a><span data-ttu-id="7df62-103">Constructor CBaseAllocator. CBaseAllocator</span><span class="sxs-lookup"><span data-stu-id="7df62-103">CBaseAllocator.CBaseAllocator constructor</span></span>

<span data-ttu-id="7df62-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="7df62-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7df62-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7df62-105">Syntax</span></span>


```C++
CBaseAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   BOOL      bEvent = TRUE,
   BOOL      fEnableReleaseCallback = FALSE
);
```



## <a name="parameters"></a><span data-ttu-id="7df62-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7df62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7df62-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="7df62-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="7df62-108">Puntero a una cadena que contiene el nombre de depuración del asignador.</span><span class="sxs-lookup"><span data-stu-id="7df62-108">Pointer to a string containing the debug name of the allocator.</span></span> <span data-ttu-id="7df62-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="7df62-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="7df62-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="7df62-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="7df62-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="7df62-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="7df62-112">Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="7df62-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="7df62-113">De lo contrario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="7df62-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7df62-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="7df62-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="7df62-115">Puntero a un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7df62-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="7df62-116">Establezca el valor en es \_ correcto antes de crear el objeto.</span><span class="sxs-lookup"><span data-stu-id="7df62-116">Set the value to S\_OK before creating the object.</span></span> <span data-ttu-id="7df62-117">Si se produce un error en el constructor, el valor se establece en un código de error.</span><span class="sxs-lookup"><span data-stu-id="7df62-117">If the constructor fails, the value is set to an error code.</span></span>

</dd> <dt>

<span data-ttu-id="7df62-118">*ventilación*</span><span class="sxs-lookup"><span data-stu-id="7df62-118">*bEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="7df62-119">Valor booleano que indica si se va a crear un semáforo.</span><span class="sxs-lookup"><span data-stu-id="7df62-119">Boolean value indicating whether to create a semaphore.</span></span> <span data-ttu-id="7df62-120">Si **es true**, el asignador crea un semáforo ([**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md)), que se señala cada vez que una muestra está disponible.</span><span class="sxs-lookup"><span data-stu-id="7df62-120">If **TRUE**, the allocator creates a semaphore ([**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md)), which is signaled whenever a sample becomes available.</span></span> <span data-ttu-id="7df62-121">Establezca el valor en **false** si está implementando una clase derivada que no requiere un semáforo.</span><span class="sxs-lookup"><span data-stu-id="7df62-121">Set the value to **FALSE** if you are implementing a derived class that does not require a semaphore.</span></span>

</dd> <dt>

<span data-ttu-id="7df62-122">*fEnableReleaseCallback*</span><span class="sxs-lookup"><span data-stu-id="7df62-122">*fEnableReleaseCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="7df62-123">Valor booleano que indica si está habilitado el mecanismo de devolución de llamada de versión.</span><span class="sxs-lookup"><span data-stu-id="7df62-123">Boolean value indicating whether the release callback mechanism is enabled.</span></span> <span data-ttu-id="7df62-124">Establezca el valor en **true** si desea proporcionar una interfaz de devolución de llamada, a la que se llama cuando se liberan los búferes.</span><span class="sxs-lookup"><span data-stu-id="7df62-124">Set the value to **TRUE** if you want to supply a callback interface, which is called when buffers are released.</span></span> <span data-ttu-id="7df62-125">Especifique la devolución de llamada mediante una llamada al método [**CBaseAllocator:: SetNotify**](cbaseallocator-setnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="7df62-125">Specify the callback by calling the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7df62-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7df62-126">Requirements</span></span>



| <span data-ttu-id="7df62-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7df62-127">Requirement</span></span> | <span data-ttu-id="7df62-128">Value</span><span class="sxs-lookup"><span data-stu-id="7df62-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7df62-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7df62-129">Header</span></span><br/>  | <dl> <span data-ttu-id="7df62-130"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7df62-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7df62-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7df62-131">Library</span></span><br/> | <dl> <span data-ttu-id="7df62-132"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7df62-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7df62-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="7df62-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df62-134">**Clase CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="7df62-134">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




