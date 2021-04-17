---
description: 'El método Clone realiza una copia del enumerador con el mismo estado de enumeración. Este método implementa el método IEnumMediaTypes:: Clone.'
ms.assetid: 3b4eb29e-48fc-4f00-a5f3-597b9aa94ce1
title: Método CEnumMediaTypes. Clone (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43f051bf90afa231d3b677045468f26d06d55150
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671161"
---
# <a name="cenummediatypesclone-method"></a><span data-ttu-id="3f7c2-104">CEnumMediaTypes. Clone (método)</span><span class="sxs-lookup"><span data-stu-id="3f7c2-104">CEnumMediaTypes.Clone method</span></span>

<span data-ttu-id="3f7c2-105">El `Clone` método realiza una copia del enumerador con el mismo estado de enumeración.</span><span class="sxs-lookup"><span data-stu-id="3f7c2-105">The `Clone` method makes a copy of the enumerator with the same enumeration state.</span></span> <span data-ttu-id="3f7c2-106">Este método implementa el método [**IEnumMediaTypes:: Clone**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone) .</span><span class="sxs-lookup"><span data-stu-id="3f7c2-106">This method implements the [**IEnumMediaTypes::Clone**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f7c2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f7c2-107">Syntax</span></span>


```C++
HRESULT Clone(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="3f7c2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f7c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f7c2-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="3f7c2-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="3f7c2-110">Dirección de una variable que recibe un puntero a la interfaz [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) del nuevo enumerador.</span><span class="sxs-lookup"><span data-stu-id="3f7c2-110">Address of a variable that receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface of the new enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f7c2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f7c2-111">Return value</span></span>

<span data-ttu-id="3f7c2-112">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3f7c2-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="3f7c2-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3f7c2-113">Return code</span></span>                                                                                                | <span data-ttu-id="3f7c2-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f7c2-114">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3f7c2-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3f7c2-115"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="3f7c2-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="3f7c2-116">Success.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="3f7c2-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3f7c2-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>              | <span data-ttu-id="3f7c2-118">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="3f7c2-118">Insufficient memory.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="3f7c2-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="3f7c2-119"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="3f7c2-120">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="3f7c2-120">**NULL** pointer argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="3f7c2-121"><dt>**\_ \_ enumeración de VFW E no \_ \_ \_ sincronizada**</dt></span><span class="sxs-lookup"><span data-stu-id="3f7c2-121"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="3f7c2-122">El estado del PIN ha cambiado y ahora es incoherente con el enumerador.</span><span class="sxs-lookup"><span data-stu-id="3f7c2-122">The pin's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3f7c2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f7c2-123">Requirements</span></span>



| <span data-ttu-id="3f7c2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f7c2-124">Requirement</span></span> | <span data-ttu-id="3f7c2-125">Value</span><span class="sxs-lookup"><span data-stu-id="3f7c2-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f7c2-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f7c2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="3f7c2-127"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f7c2-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3f7c2-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f7c2-128">Library</span></span><br/> | <dl> <span data-ttu-id="3f7c2-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3f7c2-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f7c2-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f7c2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f7c2-131">**Clase CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="3f7c2-131">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




