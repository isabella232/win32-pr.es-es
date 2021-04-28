---
description: 'Método CTransInPlaceInputPin.EnumMediaTypes: el método EnumMediaTypes enumera los tipos de medios preferidos del pin. Este método implementa el método IPin::EnumMediaTypes.'
ms.assetid: 0c28b4b0-a45f-400f-a6d7-7668458f9642
title: Método CTransInPlaceInputPin.EnumMediaTypes (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f9e05d0e9db50cabc700da7b3803c1606efab78
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094763"
---
# <a name="ctransinplaceinputpinenummediatypes-method"></a><span data-ttu-id="1ea54-104">Método CTransInPlaceInputPin.EnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="1ea54-104">CTransInPlaceInputPin.EnumMediaTypes method</span></span>

<span data-ttu-id="1ea54-105">El `EnumMediaTypes` método enumera los tipos de medios preferidos del pin.</span><span class="sxs-lookup"><span data-stu-id="1ea54-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="1ea54-106">Este método implementa el [**método IPin::EnumMediaTypes.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)</span><span class="sxs-lookup"><span data-stu-id="1ea54-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ea54-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ea54-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="1ea54-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ea54-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ea54-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="1ea54-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="1ea54-110">Recibe un puntero a la [**interfaz IEnumMediaTypes.**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)</span><span class="sxs-lookup"><span data-stu-id="1ea54-110">Receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ea54-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ea54-111">Return value</span></span>

<span data-ttu-id="1ea54-112">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="1ea54-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1ea54-113">Los valores posibles incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="1ea54-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="1ea54-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1ea54-114">Return code</span></span>                                                                                           | <span data-ttu-id="1ea54-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ea54-115">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="1ea54-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1ea54-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="1ea54-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="1ea54-117">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="1ea54-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1ea54-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="1ea54-119">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="1ea54-119">Insufficient memory.</span></span><br/>             |
| <dl> <span data-ttu-id="1ea54-120"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="1ea54-120"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="1ea54-121">**Puntero NULL.**</span><span class="sxs-lookup"><span data-stu-id="1ea54-121">**NULL** pointer.</span></span><br/>                |
| <dl> <span data-ttu-id="1ea54-122"><dt>**VFW \_ E \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="1ea54-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="1ea54-123">El pin de salida no está conectado.</span><span class="sxs-lookup"><span data-stu-id="1ea54-123">The output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1ea54-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1ea54-124">Remarks</span></span>

<span data-ttu-id="1ea54-125">Este método devuelve la **interfaz IEnumMediaTypes** del pin de entrada de bajada.</span><span class="sxs-lookup"><span data-stu-id="1ea54-125">This method returns the **IEnumMediaTypes** interface from downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ea54-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ea54-126">Requirements</span></span>



| <span data-ttu-id="1ea54-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ea54-127">Requirement</span></span> | <span data-ttu-id="1ea54-128">Value</span><span class="sxs-lookup"><span data-stu-id="1ea54-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ea54-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ea54-129">Header</span></span><br/>  | <dl> <span data-ttu-id="1ea54-130"><dt>Transip.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ea54-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1ea54-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ea54-131">Library</span></span><br/> | <dl> <span data-ttu-id="1ea54-132"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1ea54-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ea54-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1ea54-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ea54-134">**CTransInPlaceInputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="1ea54-134">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




