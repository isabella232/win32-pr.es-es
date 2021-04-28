---
description: 'Método CTransInPlaceFilter.CompleteConnect: el método CompleteConnect completa una conexión de pin.'
ms.assetid: 0c02c455-dbd0-4606-b1b1-f965c2a5805b
title: Método CTransInPlaceFilter.CompleteConnect (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9cc0bc839a4e35c4ce896acdf50da10f0c2bb0c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084793"
---
# <a name="ctransinplacefiltercompleteconnect-method"></a><span data-ttu-id="edb76-103">Método CTransInPlaceFilter.CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="edb76-103">CTransInPlaceFilter.CompleteConnect method</span></span>

<span data-ttu-id="edb76-104">El `CompleteConnect` método completa una conexión de pin.</span><span class="sxs-lookup"><span data-stu-id="edb76-104">The `CompleteConnect` method completes a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="edb76-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="edb76-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="edb76-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edb76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edb76-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="edb76-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="edb76-108">Miembro del tipo [**enumerado \_ DIRECCIÓN**](/windows/win32/api/strmif/ne-strmif-pin_direction) DEL PIN, especificando qué pin en el filtro está realizando la conexión.</span><span class="sxs-lookup"><span data-stu-id="edb76-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="edb76-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="edb76-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="edb76-110">Puntero a la [**interfaz IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro pin en este intento de conexión.</span><span class="sxs-lookup"><span data-stu-id="edb76-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edb76-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edb76-111">Return value</span></span>

<span data-ttu-id="edb76-112">Devuelve un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="edb76-112">Returns an **HRESULT**.</span></span> <span data-ttu-id="edb76-113">Los valores posibles incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="edb76-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="edb76-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="edb76-114">Return code</span></span>                                                                                           | <span data-ttu-id="edb76-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="edb76-115">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="edb76-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="edb76-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="edb76-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="edb76-117">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="edb76-118"><dt>**VFW \_ E NO ESTÁ EN \_ \_ \_ GRAPH**</dt></span><span class="sxs-lookup"><span data-stu-id="edb76-118"><dt>**VFW\_E\_NOT\_IN\_GRAPH**</dt></span></span> </dl> | <span data-ttu-id="edb76-119">El filtro no está en un gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="edb76-119">The filter is not in a filter graph.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="edb76-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="edb76-120">Remarks</span></span>

<span data-ttu-id="edb76-121">Este método invalida el [**método CTransformFilter::CompleteConnect.**](ctransformfilter-completeconnect.md)</span><span class="sxs-lookup"><span data-stu-id="edb76-121">This method overrides the [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method.</span></span>

<span data-ttu-id="edb76-122">El comportamiento del filtro depende del orden de las conexiones de pin:</span><span class="sxs-lookup"><span data-stu-id="edb76-122">The behavior of the filter depends on the order of the pin connections:</span></span>

-   <span data-ttu-id="edb76-123">Si el pin de entrada está conectado primero, la conexión usa un asignador temporal.</span><span class="sxs-lookup"><span data-stu-id="edb76-123">If the input pin is connected first, the connection uses a temporary allocator.</span></span> <span data-ttu-id="edb76-124">Cuando el pin de salida está conectado, el filtro vuelve a conectar el pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="edb76-124">When the output pin is connected, the filter reconnects the input pin.</span></span> <span data-ttu-id="edb76-125">Volver a conectar el pin de entrada hace que el filtro ascendente vuelva a negociar el asignador.</span><span class="sxs-lookup"><span data-stu-id="edb76-125">Reconnecting the input pin causes the upstream filter to renegotiate the allocator.</span></span> <span data-ttu-id="edb76-126">En ese momento, el pin de entrada propone un asignador del filtro de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="edb76-126">At that point, the input pin proposes an allocator from the downstream filter.</span></span> <span data-ttu-id="edb76-127">Para obtener más información, [**vea CTransInPlaceInputPin::GetAllocator**](ctransinplaceinputpin-getallocator.md).</span><span class="sxs-lookup"><span data-stu-id="edb76-127">For more information, see [**CTransInPlaceInputPin::GetAllocator**](ctransinplaceinputpin-getallocator.md).</span></span>
-   <span data-ttu-id="edb76-128">Si el pin de salida está conectado primero, el pin de salida no selecciona un asignador.</span><span class="sxs-lookup"><span data-stu-id="edb76-128">If the output pin is connected first, the output pin does not select an allocator.</span></span> <span data-ttu-id="edb76-129">Cuando el pin de entrada está conectado, negocia un asignador para ambas conexiones.</span><span class="sxs-lookup"><span data-stu-id="edb76-129">When the input pin is connected, it negotiates an allocator for both connections.</span></span> <span data-ttu-id="edb76-130">Si los tipos de medios de entrada y salida no son los mismos, el filtro vuelve a conectar el pin de salida mediante el tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="edb76-130">If the input and output media types are not the same, the filter reconnects the output pin using the input type.</span></span>

<span data-ttu-id="edb76-131">El filtro realiza todas las reconexiones de anclar llamando al [**método CBaseFilter::ReconnectPin.**](cbasefilter-reconnectpin.md)</span><span class="sxs-lookup"><span data-stu-id="edb76-131">The filter performs all pin reconnections by calling the [**CBaseFilter::ReconnectPin**](cbasefilter-reconnectpin.md) method.</span></span> <span data-ttu-id="edb76-132">A **su vez,** el método ReconnectPin llama al método [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) en el administrador de gráficos de filtros.</span><span class="sxs-lookup"><span data-stu-id="edb76-132">The **ReconnectPin** method, in turn, calls the [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) method on the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="edb76-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edb76-133">Requirements</span></span>



| <span data-ttu-id="edb76-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="edb76-134">Requirement</span></span> | <span data-ttu-id="edb76-135">Value</span><span class="sxs-lookup"><span data-stu-id="edb76-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edb76-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="edb76-136">Header</span></span><br/>  | <dl> <span data-ttu-id="edb76-137"><dt>Transip.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="edb76-137"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="edb76-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="edb76-138">Library</span></span><br/> | <dl> <span data-ttu-id="edb76-139"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="edb76-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edb76-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="edb76-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edb76-141">**CTransInPlaceFilter (clase)**</span><span class="sxs-lookup"><span data-stu-id="edb76-141">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




