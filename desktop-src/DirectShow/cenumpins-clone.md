---
description: 'El método Clone realiza una copia del enumerador con el mismo estado de enumeración. Este método implementa el método IEnumPins:: Clone.'
ms.assetid: 6e44c970-b90a-4bdb-8c60-dd8f31516249
title: Método CEnumPins. Clone (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2aa3e4604b260779a5d203e75e8e0790a7378b11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660860"
---
# <a name="cenumpinsclone-method"></a><span data-ttu-id="0f7b4-104">CEnumPins. Clone (método)</span><span class="sxs-lookup"><span data-stu-id="0f7b4-104">CEnumPins.Clone method</span></span>

<span data-ttu-id="0f7b4-105">El `Clone` método realiza una copia del enumerador con el mismo estado de enumeración.</span><span class="sxs-lookup"><span data-stu-id="0f7b4-105">The `Clone` method makes a copy of the enumerator with the same enumeration state.</span></span> <span data-ttu-id="0f7b4-106">Este método implementa el método [**IEnumPins:: Clone**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-clone) .</span><span class="sxs-lookup"><span data-stu-id="0f7b4-106">This method implements the [**IEnumPins::Clone**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-clone) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f7b4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f7b4-107">Syntax</span></span>


```C++
HRESULT Clone(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="0f7b4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f7b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f7b4-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="0f7b4-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="0f7b4-110">Dirección de una variable que recibe un puntero a la interfaz [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) del nuevo enumerador.</span><span class="sxs-lookup"><span data-stu-id="0f7b4-110">Address of a variable that receives a pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface of the new enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f7b4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f7b4-111">Return value</span></span>

<span data-ttu-id="0f7b4-112">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="0f7b4-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="0f7b4-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0f7b4-113">Return code</span></span>                                                                                                | <span data-ttu-id="0f7b4-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f7b4-114">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0f7b4-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0f7b4-115"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="0f7b4-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="0f7b4-116">Success.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="0f7b4-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0f7b4-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>              | <span data-ttu-id="0f7b4-118">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="0f7b4-118">Insufficient memory.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="0f7b4-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="0f7b4-119"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="0f7b4-120">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="0f7b4-120">**NULL** pointer argument.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="0f7b4-121"><dt>**\_ \_ enumeración de VFW E no \_ \_ \_ sincronizada**</dt></span><span class="sxs-lookup"><span data-stu-id="0f7b4-121"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="0f7b4-122">El estado del filtro ha cambiado y ahora es incoherente con el enumerador.</span><span class="sxs-lookup"><span data-stu-id="0f7b4-122">The filter's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0f7b4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f7b4-123">Requirements</span></span>



| <span data-ttu-id="0f7b4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f7b4-124">Requirement</span></span> | <span data-ttu-id="0f7b4-125">Value</span><span class="sxs-lookup"><span data-stu-id="0f7b4-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f7b4-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f7b4-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0f7b4-127"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f7b4-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0f7b4-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0f7b4-128">Library</span></span><br/> | <dl> <span data-ttu-id="0f7b4-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0f7b4-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f7b4-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f7b4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f7b4-131">**Clase CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="0f7b4-131">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




