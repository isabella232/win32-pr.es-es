---
description: El método DecideBufferSize establece los requisitos de búfer del terminal de salida.
ms.assetid: f1ddc39e-dcd5-4a44-8a8e-e384692408e1
title: Método CTransInPlaceFilter. DecideBufferSize (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55227510eee3c1afdcd14ed390edf21eccfcf1de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679291"
---
# <a name="ctransinplacefilterdecidebuffersize-method"></a><span data-ttu-id="3bc4b-103">CTransInPlaceFilter. DecideBufferSize, método</span><span class="sxs-lookup"><span data-stu-id="3bc4b-103">CTransInPlaceFilter.DecideBufferSize method</span></span>

<span data-ttu-id="3bc4b-104">El `DecideBufferSize` método establece los requisitos de búfer del terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="3bc4b-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bc4b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3bc4b-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProperties
);
```



## <a name="parameters"></a><span data-ttu-id="3bc4b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3bc4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bc4b-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="3bc4b-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="3bc4b-108">Puntero al objeto [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) usado por el PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="3bc4b-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) object used by the output pin.</span></span>

</dd> <dt>

<span data-ttu-id="3bc4b-109">*pProperties*</span><span class="sxs-lookup"><span data-stu-id="3bc4b-109">*pProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="3bc4b-110">Puntero a las propiedades de asignador solicitadas para el recuento, el tamaño y la alineación, tal y como especifica la estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) .</span><span class="sxs-lookup"><span data-stu-id="3bc4b-110">Pointer to the requested allocator properties for count, size, and alignment, as specified by the [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bc4b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3bc4b-111">Return value</span></span>

<span data-ttu-id="3bc4b-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3bc4b-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3bc4b-113">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3bc4b-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="3bc4b-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3bc4b-114">Return code</span></span>                                                                            | <span data-ttu-id="3bc4b-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="3bc4b-115">Description</span></span>        |
|----------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="3bc4b-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3bc4b-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="3bc4b-117">Correcto</span><span class="sxs-lookup"><span data-stu-id="3bc4b-117">Success</span></span><br/> |
| <dl> <span data-ttu-id="3bc4b-118"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="3bc4b-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="3bc4b-119">Error</span><span class="sxs-lookup"><span data-stu-id="3bc4b-119">Failure</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3bc4b-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3bc4b-120">Remarks</span></span>

<span data-ttu-id="3bc4b-121">Se llama a este método cuando la clase **CTransInPlaceFilter** debe proporcionar un tamaño de búfer al filtro de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="3bc4b-121">This method is called when the **CTransInPlaceFilter** class needs to provide a buffer size to the downstream filter.</span></span> <span data-ttu-id="3bc4b-122">Si el filtro **CTransInPlaceFilter** ya está conectado al nivel superior, usa las propiedades de asignador en la conexión de PIN de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="3bc4b-122">If the **CTransInPlaceFilter** filter is already connected upstream, it uses the allocator properties on the upstream pin connection.</span></span> <span data-ttu-id="3bc4b-123">De lo contrario, establece el tamaño del búfer en 1 byte como un valor de marcador de posición temporal.</span><span class="sxs-lookup"><span data-stu-id="3bc4b-123">Otherwise, it sets the buffer size to 1 byte as a temporary place-holder value.</span></span> <span data-ttu-id="3bc4b-124">Cuando se conecta el filtro de nivel superior, la clase **CTransInPlaceFilter** vuelve a negociar el asignador de bajada.</span><span class="sxs-lookup"><span data-stu-id="3bc4b-124">When the upstream filter connects, the **CTransInPlaceFilter** class renegotiates the downstream allocator.</span></span> <span data-ttu-id="3bc4b-125">Para obtener más información sobre el proceso de conexión de PIN en esta clase, vea [**CTransInPlaceFilter (clase**](ctransinplacefilter.md)).</span><span class="sxs-lookup"><span data-stu-id="3bc4b-125">For more information about the pin connection process in this class, see [**CTransInPlaceFilter Class**](ctransinplacefilter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3bc4b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bc4b-126">Requirements</span></span>



| <span data-ttu-id="3bc4b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bc4b-127">Requirement</span></span> | <span data-ttu-id="3bc4b-128">Value</span><span class="sxs-lookup"><span data-stu-id="3bc4b-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bc4b-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3bc4b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3bc4b-130"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3bc4b-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3bc4b-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3bc4b-131">Library</span></span><br/> | <dl> <span data-ttu-id="3bc4b-132"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3bc4b-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bc4b-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="3bc4b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bc4b-134">**Clase CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="3bc4b-134">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




