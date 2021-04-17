---
description: El método CheckConnect determina si una conexión de PIN es adecuada.
ms.assetid: 50ab59ad-8ff7-4d7b-add3-b59203d93307
title: Método CBaseOutputPin. CheckConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3274e47e9a77d86f350c17aaca04ec0cdb95ef3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660798"
---
# <a name="cbaseoutputpincheckconnect-method"></a><span data-ttu-id="470c1-103">CBaseOutputPin. CheckConnect, método</span><span class="sxs-lookup"><span data-stu-id="470c1-103">CBaseOutputPin.CheckConnect method</span></span>

<span data-ttu-id="470c1-104">El `CheckConnect` método determina si una conexión de PIN es adecuada.</span><span class="sxs-lookup"><span data-stu-id="470c1-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="470c1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="470c1-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="470c1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="470c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="470c1-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="470c1-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="470c1-108">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="470c1-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="470c1-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="470c1-109">Return value</span></span>

<span data-ttu-id="470c1-110">Devuelve uno de los siguientes valores **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="470c1-110">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="470c1-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="470c1-111">Return code</span></span>                                                                                               | <span data-ttu-id="470c1-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="470c1-112">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="470c1-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="470c1-113"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="470c1-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="470c1-114">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="470c1-115"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="470c1-115"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>             | <span data-ttu-id="470c1-116">El PIN de entrada no es compatible con [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).</span><span class="sxs-lookup"><span data-stu-id="470c1-116">Input pin does not support [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).</span></span><br/> |
| <dl> <span data-ttu-id="470c1-117"><dt>**\_ \_ dirección no válida de VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="470c1-117"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="470c1-118">Las direcciones de PIN no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="470c1-118">Pin directions are not compatible.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="470c1-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="470c1-119">Remarks</span></span>

<span data-ttu-id="470c1-120">Este método llama al método [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) de la clase base y, a continuación, consulta el PIN de entrada para su interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="470c1-120">This method calls the base-class [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method, and then queries the input pin for its [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="470c1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="470c1-121">Requirements</span></span>



| <span data-ttu-id="470c1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="470c1-122">Requirement</span></span> | <span data-ttu-id="470c1-123">Value</span><span class="sxs-lookup"><span data-stu-id="470c1-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="470c1-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="470c1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="470c1-125"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="470c1-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="470c1-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="470c1-126">Library</span></span><br/> | <dl> <span data-ttu-id="470c1-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="470c1-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="470c1-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="470c1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="470c1-129">**Clase CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="470c1-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




