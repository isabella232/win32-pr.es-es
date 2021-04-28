---
description: 'Método CBaseInputPin.NotifyAllocator: el método NotifyAllocator especifica un asignador para la conexión. Este método implementa el método IMemInputPin::NotifyAllocator.'
ms.assetid: 16167bd5-2d33-4329-87ec-6a6c578e0060
title: Método CBaseInputPin.NotifyAllocator (Amfilter.h)
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
ms.openlocfilehash: c63e448d0cf2d287a441a4983f6a2e06bd9b8151
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099722"
---
# <a name="cbaseinputpinnotifyallocator-method"></a><span data-ttu-id="bf229-104">CBaseInputPin.NotifyAllocator (método)</span><span class="sxs-lookup"><span data-stu-id="bf229-104">CBaseInputPin.NotifyAllocator method</span></span>

<span data-ttu-id="bf229-105">El `NotifyAllocator` método especifica un asignador para la conexión.</span><span class="sxs-lookup"><span data-stu-id="bf229-105">The `NotifyAllocator` method specifies an allocator for the connection.</span></span> <span data-ttu-id="bf229-106">Este método implementa el [**método IMemInputPin::NotifyAllocator.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator)</span><span class="sxs-lookup"><span data-stu-id="bf229-106">This method implements the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf229-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf229-107">Syntax</span></span>


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a><span data-ttu-id="bf229-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf229-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf229-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="bf229-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="bf229-110">Puntero a la interfaz [**IMemAllocator del asignador.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)</span><span class="sxs-lookup"><span data-stu-id="bf229-110">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="bf229-111">*bReadOnly*</span><span class="sxs-lookup"><span data-stu-id="bf229-111">*bReadOnly*</span></span> 
</dt> <dd>

<span data-ttu-id="bf229-112">Marca que especifica si los ejemplos de este asignador son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bf229-112">Flag that specifies whether samples from this allocator are read-only.</span></span> <span data-ttu-id="bf229-113">Si **es TRUE,** los ejemplos son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bf229-113">If **TRUE**, samples are read-only.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf229-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf229-114">Return value</span></span>

<span data-ttu-id="bf229-115">Devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bf229-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf229-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf229-116">Remarks</span></span>

<span data-ttu-id="bf229-117">Durante la conexión de anclado, el pin de salida elige un asignador y llama a este método para notificar al pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="bf229-117">During the pin connection, the output pin chooses an allocator and calls this method to notify the input pin.</span></span> <span data-ttu-id="bf229-118">El pin de salida puede usar el asignador que el pin de entrada propuesto en el método [**IMemInputPin::GetAllocator,**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) o puede proporcionar su propio asignador.</span><span class="sxs-lookup"><span data-stu-id="bf229-118">The output pin can use the allocator that the input pin proposed in the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method, or it can provide its own allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf229-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf229-119">Requirements</span></span>



| <span data-ttu-id="bf229-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf229-120">Requirement</span></span> | <span data-ttu-id="bf229-121">Value</span><span class="sxs-lookup"><span data-stu-id="bf229-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf229-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf229-122">Header</span></span><br/>  | <dl> <span data-ttu-id="bf229-123"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf229-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bf229-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf229-124">Library</span></span><br/> | <dl> <span data-ttu-id="bf229-125"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bf229-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf229-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bf229-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf229-127">**CBaseInputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="bf229-127">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




