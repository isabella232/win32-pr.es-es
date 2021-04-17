---
description: 'El método GetAllocator recupera el asignador de memoria propuesto por este pin. Este método implementa el método IMemInputPin:: GetAllocator.'
ms.assetid: 07bc77f8-a877-4403-b424-20bda715a818
title: Método CBaseInputPin. GetAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 098738fc63ba1834b1eefb4b2518e3309db35c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660344"
---
# <a name="cbaseinputpingetallocator-method"></a><span data-ttu-id="380d6-104">CBaseInputPin. GetAllocator, método</span><span class="sxs-lookup"><span data-stu-id="380d6-104">CBaseInputPin.GetAllocator method</span></span>

<span data-ttu-id="380d6-105">El `GetAllocator` método recupera el asignador de memoria propuesto por este pin.</span><span class="sxs-lookup"><span data-stu-id="380d6-105">The `GetAllocator` method retrieves the memory allocator proposed by this pin.</span></span> <span data-ttu-id="380d6-106">Este método implementa el método [**IMemInputPin:: GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) .</span><span class="sxs-lookup"><span data-stu-id="380d6-106">This method implements the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="380d6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="380d6-107">Syntax</span></span>


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="380d6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="380d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="380d6-109">*ppAllocator*</span><span class="sxs-lookup"><span data-stu-id="380d6-109">*ppAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="380d6-110">Dirección de una variable que recibe un puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador.</span><span class="sxs-lookup"><span data-stu-id="380d6-110">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="380d6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="380d6-111">Return value</span></span>

<span data-ttu-id="380d6-112">Devuelve \_ si es correcto, o un código de error de la función **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="380d6-112">Returns S\_OK if successful, or an error code from the **CoCreateInstance** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="380d6-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="380d6-113">Remarks</span></span>

<span data-ttu-id="380d6-114">Este método crea un objeto [**CMemAllocator**](cmemallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="380d6-114">This method creates a [**CMemAllocator**](cmemallocator.md) object.</span></span> <span data-ttu-id="380d6-115">Invalide este método si el filtro usa un asignador de un PIN de nivel inferior o un asignador personalizado.</span><span class="sxs-lookup"><span data-stu-id="380d6-115">Override this method if your filter uses an allocator from a downstream pin, or a custom allocator.</span></span>

<span data-ttu-id="380d6-116">Si el método se ejecuta correctamente, la interfaz **IMemAllocator** tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="380d6-116">If the method succeeds, the **IMemAllocator** interface has an outstanding reference count.</span></span> <span data-ttu-id="380d6-117">Asegúrese de liberarlo cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="380d6-117">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="380d6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="380d6-118">Requirements</span></span>



| <span data-ttu-id="380d6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="380d6-119">Requirement</span></span> | <span data-ttu-id="380d6-120">Value</span><span class="sxs-lookup"><span data-stu-id="380d6-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="380d6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="380d6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="380d6-122"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="380d6-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="380d6-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="380d6-123">Library</span></span><br/> | <dl> <span data-ttu-id="380d6-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="380d6-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="380d6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="380d6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="380d6-126">**Clase CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="380d6-126">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




