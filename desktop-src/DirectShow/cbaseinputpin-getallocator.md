---
description: 'Método CBaseInputPin.GetAllocator: el método GetAllocator recupera el asignador de memoria propuesto por este pin. Este método implementa el método IMemInputPin::GetAllocator.'
ms.assetid: 07bc77f8-a877-4403-b424-20bda715a818
title: Método CBaseInputPin.GetAllocator (Amfilter.h)
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
ms.openlocfilehash: 72aaf6bb4c1ff8bf108086a8a42a618267c4bc06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099723"
---
# <a name="cbaseinputpingetallocator-method"></a><span data-ttu-id="a1cb9-104">CBaseInputPin.GetAllocator (método)</span><span class="sxs-lookup"><span data-stu-id="a1cb9-104">CBaseInputPin.GetAllocator method</span></span>

<span data-ttu-id="a1cb9-105">El `GetAllocator` método recupera el asignador de memoria propuesto por este pin.</span><span class="sxs-lookup"><span data-stu-id="a1cb9-105">The `GetAllocator` method retrieves the memory allocator proposed by this pin.</span></span> <span data-ttu-id="a1cb9-106">Este método implementa el [**método IMemInputPin::GetAllocator.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator)</span><span class="sxs-lookup"><span data-stu-id="a1cb9-106">This method implements the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1cb9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1cb9-107">Syntax</span></span>


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="a1cb9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1cb9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1cb9-109">*ppAllocator*</span><span class="sxs-lookup"><span data-stu-id="a1cb9-109">*ppAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="a1cb9-110">Dirección de una variable que recibe un puntero a la interfaz [**IMemAllocator del**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) asignador.</span><span class="sxs-lookup"><span data-stu-id="a1cb9-110">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1cb9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1cb9-111">Return value</span></span>

<span data-ttu-id="a1cb9-112">Devuelve S \_ OK si se realiza correctamente o un código de error de la función **CoCreateInstance.**</span><span class="sxs-lookup"><span data-stu-id="a1cb9-112">Returns S\_OK if successful, or an error code from the **CoCreateInstance** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1cb9-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a1cb9-113">Remarks</span></span>

<span data-ttu-id="a1cb9-114">Este método crea un [**objeto CMemAllocator.**](cmemallocator.md)</span><span class="sxs-lookup"><span data-stu-id="a1cb9-114">This method creates a [**CMemAllocator**](cmemallocator.md) object.</span></span> <span data-ttu-id="a1cb9-115">Invalide este método si el filtro usa un asignador de un pin de nivel inferior o un asignador personalizado.</span><span class="sxs-lookup"><span data-stu-id="a1cb9-115">Override this method if your filter uses an allocator from a downstream pin, or a custom allocator.</span></span>

<span data-ttu-id="a1cb9-116">Si el método se realiza correctamente, la **interfaz IMemAllocator** tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="a1cb9-116">If the method succeeds, the **IMemAllocator** interface has an outstanding reference count.</span></span> <span data-ttu-id="a1cb9-117">Asegúrese de liberarlo cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="a1cb9-117">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1cb9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1cb9-118">Requirements</span></span>



| <span data-ttu-id="a1cb9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1cb9-119">Requirement</span></span> | <span data-ttu-id="a1cb9-120">Value</span><span class="sxs-lookup"><span data-stu-id="a1cb9-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1cb9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1cb9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a1cb9-122"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1cb9-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a1cb9-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1cb9-123">Library</span></span><br/> | <dl> <span data-ttu-id="a1cb9-124"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a1cb9-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1cb9-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a1cb9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1cb9-126">**CBaseInputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="a1cb9-126">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




