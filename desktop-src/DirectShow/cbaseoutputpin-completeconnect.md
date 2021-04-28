---
description: 'Método CBaseOutputPin.CompleteConnect: el método CompleteConnect completa una conexión a un pin de entrada.'
ms.assetid: 44c28c71-2c69-40ca-9bc4-c10394475a0f
title: Método CBaseOutputPin.CompleteConnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd4bc52db99b88c4d6f16c549fbb558bb6423730
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099543"
---
# <a name="cbaseoutputpincompleteconnect-method"></a><span data-ttu-id="61c85-103">Método CBaseOutputPin.CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="61c85-103">CBaseOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="61c85-104">El `CompleteConnect` método completa una conexión a un pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="61c85-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="61c85-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61c85-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="61c85-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61c85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61c85-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="61c85-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="61c85-108">Puntero a la patilla de entrada.</span><span class="sxs-lookup"><span data-stu-id="61c85-108">Pointer to the input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61c85-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61c85-109">Return value</span></span>

<span data-ttu-id="61c85-110">Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="61c85-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="61c85-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="61c85-111">Remarks</span></span>

<span data-ttu-id="61c85-112">Este método invalida el [**método CBasePin::CompleteConnect.**](cbasepin-completeconnect.md)</span><span class="sxs-lookup"><span data-stu-id="61c85-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="61c85-113">Llama al [**método DecideAllocator,**](cbaseoutputpin-decideallocator.md) que selecciona el asignador de memoria que se va a usar para esta conexión.</span><span class="sxs-lookup"><span data-stu-id="61c85-113">It calls the [**DecideAllocator**](cbaseoutputpin-decideallocator.md) method, which selects the memory allocator to use for this connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="61c85-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61c85-114">Requirements</span></span>



| <span data-ttu-id="61c85-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="61c85-115">Requirement</span></span> | <span data-ttu-id="61c85-116">Value</span><span class="sxs-lookup"><span data-stu-id="61c85-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61c85-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61c85-117">Header</span></span><br/>  | <dl> <span data-ttu-id="61c85-118"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="61c85-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="61c85-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="61c85-119">Library</span></span><br/> | <dl> <span data-ttu-id="61c85-120"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="61c85-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61c85-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="61c85-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61c85-122">**CBaseOutputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="61c85-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




