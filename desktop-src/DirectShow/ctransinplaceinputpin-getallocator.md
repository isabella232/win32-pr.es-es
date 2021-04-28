---
description: 'Método CTransInPlaceInputPin.GetAllocator: el método GetAllocator recupera el asignador de memoria propuesto por este pin. Este método implementa el método IMemInputPin::GetAllocator.'
ms.assetid: e9db4aa0-4f53-4ca4-babb-5e0215c7c284
title: Método CTransInPlaceInputPin.GetAllocator (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2472630d69119f33653d831386af615718274d99
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084663"
---
# <a name="ctransinplaceinputpingetallocator-method"></a><span data-ttu-id="31a6a-104">Método CTransInPlaceInputPin.GetAllocator</span><span class="sxs-lookup"><span data-stu-id="31a6a-104">CTransInPlaceInputPin.GetAllocator method</span></span>

<span data-ttu-id="31a6a-105">El `GetAllocator` método recupera el asignador de memoria propuesto por este pin.</span><span class="sxs-lookup"><span data-stu-id="31a6a-105">The `GetAllocator` method retrieves the memory allocator proposed by this pin.</span></span> <span data-ttu-id="31a6a-106">Este método implementa el [**método IMemInputPin::GetAllocator.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator)</span><span class="sxs-lookup"><span data-stu-id="31a6a-106">This method implements the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="31a6a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31a6a-107">Syntax</span></span>


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="31a6a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31a6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31a6a-109">*ppAllocator*</span><span class="sxs-lookup"><span data-stu-id="31a6a-109">*ppAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="31a6a-110">Recibe un puntero a la interfaz [**IMemAllocator del**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) asignador.</span><span class="sxs-lookup"><span data-stu-id="31a6a-110">Receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31a6a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31a6a-111">Return value</span></span>

<span data-ttu-id="31a6a-112">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="31a6a-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="31a6a-113">Los valores posibles incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="31a6a-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="31a6a-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="31a6a-114">Return code</span></span>                                                                                          | <span data-ttu-id="31a6a-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="31a6a-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="31a6a-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="31a6a-116"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="31a6a-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="31a6a-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="31a6a-118"><dt>**VFW \_ E \_ NO \_ ALLOCATOR**</dt></span><span class="sxs-lookup"><span data-stu-id="31a6a-118"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="31a6a-119">No hay ningún asignador disponible.</span><span class="sxs-lookup"><span data-stu-id="31a6a-119">No allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="31a6a-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="31a6a-120">Remarks</span></span>

<span data-ttu-id="31a6a-121">Si el pin de salida del filtro está conectado, este método solicita un asignador del pin de entrada del filtro de bajada.</span><span class="sxs-lookup"><span data-stu-id="31a6a-121">If the filter's output pin is connected, this method requests an allocator from the downstream filter's input pin.</span></span>

<span data-ttu-id="31a6a-122">Si el pin de salida del filtro no está conectado, este método crea un asignador temporal.</span><span class="sxs-lookup"><span data-stu-id="31a6a-122">If the filter's output pin is not connected, this method creates a temporary allocator.</span></span> <span data-ttu-id="31a6a-123">Más adelante, cuando el pin de salida esté conectado, el filtro volverá a conectar el pin de entrada y volverá a negociar el asignador.</span><span class="sxs-lookup"><span data-stu-id="31a6a-123">Later, when the output pin is connected, the filter will reconnect the input pin and renegotiate the allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="31a6a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31a6a-124">Requirements</span></span>



| <span data-ttu-id="31a6a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="31a6a-125">Requirement</span></span> | <span data-ttu-id="31a6a-126">Value</span><span class="sxs-lookup"><span data-stu-id="31a6a-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31a6a-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31a6a-127">Header</span></span><br/>  | <dl> <span data-ttu-id="31a6a-128"><dt>Transip.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="31a6a-128"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="31a6a-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31a6a-129">Library</span></span><br/> | <dl> <span data-ttu-id="31a6a-130"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="31a6a-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31a6a-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="31a6a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31a6a-132">**CTransInPlaceInputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="31a6a-132">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




