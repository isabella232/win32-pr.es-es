---
description: 'El método GetAllocatorRequirements recupera las propiedades de asignador solicitadas por el código PIN. Este método implementa el método IMemInputPin:: GetAllocatorRequirements.'
ms.assetid: 1355facc-f863-44b2-9284-8f06f62d39a2
title: Método CTransInPlaceInputPin. GetAllocatorRequirements (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa176cd5da0317821996593e19bb90396e82224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680739"
---
# <a name="ctransinplaceinputpingetallocatorrequirements-method"></a><span data-ttu-id="5ea65-104">CTransInPlaceInputPin. GetAllocatorRequirements, método</span><span class="sxs-lookup"><span data-stu-id="5ea65-104">CTransInPlaceInputPin.GetAllocatorRequirements method</span></span>

<span data-ttu-id="5ea65-105">El `GetAllocatorRequirements` método recupera las propiedades de asignador solicitadas por el código PIN.</span><span class="sxs-lookup"><span data-stu-id="5ea65-105">The `GetAllocatorRequirements` method retrieves the allocator properties requested by the pin.</span></span> <span data-ttu-id="5ea65-106">Este método implementa el método [**IMemInputPin:: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) .</span><span class="sxs-lookup"><span data-stu-id="5ea65-106">This method implements the [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ea65-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ea65-107">Syntax</span></span>


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="5ea65-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ea65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ea65-109">*pProps*</span><span class="sxs-lookup"><span data-stu-id="5ea65-109">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="5ea65-110">Puntero a una estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , que se rellena con los requisitos.</span><span class="sxs-lookup"><span data-stu-id="5ea65-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure, which is filled in with the requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ea65-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ea65-111">Return value</span></span>

<span data-ttu-id="5ea65-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5ea65-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5ea65-113">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5ea65-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="5ea65-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5ea65-114">Return code</span></span>                                                                               | <span data-ttu-id="5ea65-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ea65-115">Description</span></span>                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5ea65-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="5ea65-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="5ea65-117">Correcto</span><span class="sxs-lookup"><span data-stu-id="5ea65-117">Success</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="5ea65-118"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="5ea65-118"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="5ea65-119">El PIN de salida no está conectado o el PIN de entrada de nivel inferior no admite el método.</span><span class="sxs-lookup"><span data-stu-id="5ea65-119">The output pin is not connected, or the downstream input pin does not support the method.</span></span><br/> |
| <dl> <span data-ttu-id="5ea65-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="5ea65-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="5ea65-121">Argumento de puntero **nulo**</span><span class="sxs-lookup"><span data-stu-id="5ea65-121">**NULL** pointer argument</span></span><br/>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="5ea65-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ea65-122">Remarks</span></span>

<span data-ttu-id="5ea65-123">Si el PIN de salida está conectado, este método pasa la llamada al pin de entrada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="5ea65-123">If the output pin is connected, this method passes the call to the downstream input pin.</span></span> <span data-ttu-id="5ea65-124">De lo contrario, devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="5ea65-124">Otherwise, it returns E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ea65-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ea65-125">Requirements</span></span>



| <span data-ttu-id="5ea65-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ea65-126">Requirement</span></span> | <span data-ttu-id="5ea65-127">Value</span><span class="sxs-lookup"><span data-stu-id="5ea65-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea65-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ea65-128">Header</span></span><br/>  | <dl> <span data-ttu-id="5ea65-129"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ea65-129"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5ea65-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5ea65-130">Library</span></span><br/> | <dl> <span data-ttu-id="5ea65-131"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5ea65-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ea65-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ea65-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ea65-133">**Clase CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="5ea65-133">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




