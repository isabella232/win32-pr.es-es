---
description: 'El método NotifyAllocator especifica un asignador para la conexión. Este método implementa el método IMemInputPin:: NotifyAllocator.'
ms.assetid: 16167bd5-2d33-4329-87ec-6a6c578e0060
title: Método CBaseInputPin. NotifyAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce5bc3cfe165b1adb6b5b970ca43d31c8ace98f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671328"
---
# <a name="cbaseinputpinnotifyallocator-method"></a><span data-ttu-id="ad6f1-104">CBaseInputPin. NotifyAllocator, método</span><span class="sxs-lookup"><span data-stu-id="ad6f1-104">CBaseInputPin.NotifyAllocator method</span></span>

<span data-ttu-id="ad6f1-105">El `NotifyAllocator` método especifica un asignador para la conexión.</span><span class="sxs-lookup"><span data-stu-id="ad6f1-105">The `NotifyAllocator` method specifies an allocator for the connection.</span></span> <span data-ttu-id="ad6f1-106">Este método implementa el método [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) .</span><span class="sxs-lookup"><span data-stu-id="ad6f1-106">This method implements the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad6f1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad6f1-107">Syntax</span></span>


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a><span data-ttu-id="ad6f1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad6f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad6f1-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="ad6f1-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="ad6f1-110">Puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador.</span><span class="sxs-lookup"><span data-stu-id="ad6f1-110">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="ad6f1-111">*bReadOnly*</span><span class="sxs-lookup"><span data-stu-id="ad6f1-111">*bReadOnly*</span></span> 
</dt> <dd>

<span data-ttu-id="ad6f1-112">Marca que especifica si los ejemplos de este asignador son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ad6f1-112">Flag that specifies whether samples from this allocator are read-only.</span></span> <span data-ttu-id="ad6f1-113">Si **es true**, los ejemplos son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ad6f1-113">If **TRUE**, samples are read-only.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad6f1-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad6f1-114">Return value</span></span>

<span data-ttu-id="ad6f1-115">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="ad6f1-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad6f1-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad6f1-116">Remarks</span></span>

<span data-ttu-id="ad6f1-117">Durante la conexión del PIN, el PIN de salida elige un asignador y llama a este método para notificar al pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="ad6f1-117">During the pin connection, the output pin chooses an allocator and calls this method to notify the input pin.</span></span> <span data-ttu-id="ad6f1-118">El PIN de salida puede usar el asignador que el PIN de entrada propuso en el método [**IMemInputPin:: GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) , o puede proporcionar su propio asignador.</span><span class="sxs-lookup"><span data-stu-id="ad6f1-118">The output pin can use the allocator that the input pin proposed in the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method, or it can provide its own allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad6f1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad6f1-119">Requirements</span></span>



| <span data-ttu-id="ad6f1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad6f1-120">Requirement</span></span> | <span data-ttu-id="ad6f1-121">Value</span><span class="sxs-lookup"><span data-stu-id="ad6f1-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad6f1-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad6f1-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ad6f1-123"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad6f1-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ad6f1-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ad6f1-124">Library</span></span><br/> | <dl> <span data-ttu-id="ad6f1-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ad6f1-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad6f1-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad6f1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad6f1-127">**Clase CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="ad6f1-127">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




