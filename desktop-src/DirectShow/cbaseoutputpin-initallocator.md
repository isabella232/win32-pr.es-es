---
description: El método InitAllocator crea un asignador de memoria.
ms.assetid: a1fa0ffb-ed43-446d-811e-6c3594743592
title: CBaseOutputPin.Inimétodo tAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.InitAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e5385671ba4c7fdf1b719f83aafba7d84421bce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671503"
---
# <a name="cbaseoutputpininitallocator-method"></a><span data-ttu-id="7adae-103">CBaseOutputPin.Inimétodo tAllocator</span><span class="sxs-lookup"><span data-stu-id="7adae-103">CBaseOutputPin.InitAllocator method</span></span>

<span data-ttu-id="7adae-104">El `InitAllocator` método crea un asignador de memoria.</span><span class="sxs-lookup"><span data-stu-id="7adae-104">The `InitAllocator` method creates a memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="7adae-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7adae-105">Syntax</span></span>


```C++
virtual HRESULT InitAllocator(
   IMemAllocator **ppAlloc
);
```



## <a name="parameters"></a><span data-ttu-id="7adae-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7adae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7adae-107">*ppAlloc*</span><span class="sxs-lookup"><span data-stu-id="7adae-107">*ppAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="7adae-108">Dirección de una variable que recibe un puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador.</span><span class="sxs-lookup"><span data-stu-id="7adae-108">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7adae-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7adae-109">Return value</span></span>

<span data-ttu-id="7adae-110">Devuelve \_ si es correcto, o un código de error de la función **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="7adae-110">Returns S\_OK if successful, or an error code from the **CoCreateInstance** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="7adae-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7adae-111">Remarks</span></span>

<span data-ttu-id="7adae-112">Si el PIN de entrada no proporciona un asignador de memoria, el método [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md) llama a este método para crear un asignador.</span><span class="sxs-lookup"><span data-stu-id="7adae-112">If the input pin does not provide a memory allocator, the [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md) method calls this method to create an allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="7adae-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7adae-113">Requirements</span></span>



| <span data-ttu-id="7adae-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7adae-114">Requirement</span></span> | <span data-ttu-id="7adae-115">Value</span><span class="sxs-lookup"><span data-stu-id="7adae-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7adae-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7adae-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7adae-117"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7adae-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7adae-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7adae-118">Library</span></span><br/> | <dl> <span data-ttu-id="7adae-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7adae-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7adae-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="7adae-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7adae-121">**Clase CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="7adae-121">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




