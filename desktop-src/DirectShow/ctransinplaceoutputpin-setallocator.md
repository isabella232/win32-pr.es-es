---
description: El método SetAllocator especifica un asignador para la conexión.
ms.assetid: 6b8e80f9-3b0d-498f-b1b0-bae491c25e81
title: Método CTransInPlaceOutputPin. SetAllocator (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.SetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aacc2680bebcdd7de74f6f357380066a8fd37f1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660356"
---
# <a name="ctransinplaceoutputpinsetallocator-method"></a><span data-ttu-id="ab224-103">CTransInPlaceOutputPin. SetAllocator, método</span><span class="sxs-lookup"><span data-stu-id="ab224-103">CTransInPlaceOutputPin.SetAllocator method</span></span>

<span data-ttu-id="ab224-104">El `SetAllocator` método especifica un asignador para la conexión.</span><span class="sxs-lookup"><span data-stu-id="ab224-104">The `SetAllocator` method specifies an allocator for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab224-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab224-105">Syntax</span></span>


```C++
void SetAllocator(
   IMemAllocator *pAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="ab224-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab224-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab224-107">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="ab224-107">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="ab224-108">Puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador.</span><span class="sxs-lookup"><span data-stu-id="ab224-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab224-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab224-109">Return value</span></span>

<span data-ttu-id="ab224-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ab224-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab224-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab224-111">Remarks</span></span>

<span data-ttu-id="ab224-112">El PIN de salida de este filtro nunca proporciona un asignador.</span><span class="sxs-lookup"><span data-stu-id="ab224-112">The output pin for this filter never provides an allocator.</span></span> <span data-ttu-id="ab224-113">Este método especifica el asignador para el PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="ab224-113">This method specifies the allocator for the output pin.</span></span> <span data-ttu-id="ab224-114">Establece el valor de la variable miembro [**CBaseOutputPin:: m \_ pAllocator**](cbaseoutputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="ab224-114">It sets the value of the [**CBaseOutputPin::m\_pAllocator**](cbaseoutputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab224-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab224-115">Requirements</span></span>



| <span data-ttu-id="ab224-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab224-116">Requirement</span></span> | <span data-ttu-id="ab224-117">Value</span><span class="sxs-lookup"><span data-stu-id="ab224-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab224-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab224-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ab224-119"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab224-119"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ab224-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab224-120">Library</span></span><br/> | <dl> <span data-ttu-id="ab224-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ab224-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab224-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab224-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab224-123">**Clase CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="ab224-123">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




