---
description: El método CreateInstance crea una nueva instancia de la clase CMemAllocator.
ms.assetid: 87a831a4-2414-4240-8448-c5d90f130470
title: Método CMemAllocator. CreateInstance (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ef85de95db74e8a9d7aa6a7b1ba977620a29826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670756"
---
# <a name="cmemallocatorcreateinstance-method"></a><span data-ttu-id="228fd-103">CMemAllocator. CreateInstance (método)</span><span class="sxs-lookup"><span data-stu-id="228fd-103">CMemAllocator.CreateInstance method</span></span>

<span data-ttu-id="228fd-104">El `CreateInstance` método crea una nueva instancia de la clase **CMemAllocator** .</span><span class="sxs-lookup"><span data-stu-id="228fd-104">The `CreateInstance` method creates a new instance of the **CMemAllocator** class.</span></span>

## <a name="syntax"></a><span data-ttu-id="228fd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="228fd-105">Syntax</span></span>


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="228fd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="228fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="228fd-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="228fd-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="228fd-108">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="228fd-108">Pointer to the owner of this object.</span></span> <span data-ttu-id="228fd-109">Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="228fd-109">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="228fd-110">De lo contrario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="228fd-110">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="228fd-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="228fd-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="228fd-112">Puntero a una variable que recibe un valor **HRESULT** que indica si el método se ha ejecutado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="228fd-112">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="228fd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="228fd-113">Return value</span></span>

<span data-ttu-id="228fd-114">Devuelve un puntero a un nuevo objeto **CMemAllocator** , escrito como un objeto **CUnknown** .</span><span class="sxs-lookup"><span data-stu-id="228fd-114">Returns a pointer to a new **CMemAllocator** object, typed as a **CUnknown** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="228fd-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="228fd-115">Requirements</span></span>



| <span data-ttu-id="228fd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="228fd-116">Requirement</span></span> | <span data-ttu-id="228fd-117">Value</span><span class="sxs-lookup"><span data-stu-id="228fd-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="228fd-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="228fd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="228fd-119"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="228fd-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="228fd-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="228fd-120">Library</span></span><br/> | <dl> <span data-ttu-id="228fd-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="228fd-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="228fd-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="228fd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="228fd-123">**Clase CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="228fd-123">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




