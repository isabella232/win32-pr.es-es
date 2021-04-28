---
description: 'Método CBaseOutputPin.CheckConnect: el método CheckConnect determina si una conexión de pin es adecuada.'
ms.assetid: 50ab59ad-8ff7-4d7b-add3-b59203d93307
title: Método CBaseOutputPin.CheckConnect (Amfilter.h)
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
ms.openlocfilehash: 7ea5ad32de18046f3d23145d82e971391c3e304c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096193"
---
# <a name="cbaseoutputpincheckconnect-method"></a><span data-ttu-id="d5096-103">Método CBaseOutputPin.CheckConnect</span><span class="sxs-lookup"><span data-stu-id="d5096-103">CBaseOutputPin.CheckConnect method</span></span>

<span data-ttu-id="d5096-104">El `CheckConnect` método determina si una conexión de pin es adecuada.</span><span class="sxs-lookup"><span data-stu-id="d5096-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5096-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5096-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="d5096-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5096-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5096-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="d5096-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="d5096-108">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="d5096-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5096-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5096-109">Return value</span></span>

<span data-ttu-id="d5096-110">Devuelve uno de los siguientes **valores HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="d5096-110">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="d5096-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d5096-111">Return code</span></span>                                                                                               | <span data-ttu-id="d5096-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5096-112">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d5096-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d5096-113"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="d5096-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="d5096-114">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="d5096-115"><dt>**E \_ NOINTERFACE**</dt></span><span class="sxs-lookup"><span data-stu-id="d5096-115"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>             | <span data-ttu-id="d5096-116">El pin de entrada no admite [**IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)</span><span class="sxs-lookup"><span data-stu-id="d5096-116">Input pin does not support [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).</span></span><br/> |
| <dl> <span data-ttu-id="d5096-117"><dt>**VFW \_ E DIRECCIÓN NO \_ \_ VÁLIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="d5096-117"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="d5096-118">Las direcciones del pin no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="d5096-118">Pin directions are not compatible.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="d5096-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d5096-119">Remarks</span></span>

<span data-ttu-id="d5096-120">Este método llama al método [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) de clase base y, a continuación, consulta el pin de entrada para su [**interfaz IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)</span><span class="sxs-lookup"><span data-stu-id="d5096-120">This method calls the base-class [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method, and then queries the input pin for its [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5096-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5096-121">Requirements</span></span>



| <span data-ttu-id="d5096-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5096-122">Requirement</span></span> | <span data-ttu-id="d5096-123">Value</span><span class="sxs-lookup"><span data-stu-id="d5096-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5096-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5096-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d5096-125"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5096-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d5096-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d5096-126">Library</span></span><br/> | <dl> <span data-ttu-id="d5096-127"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d5096-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5096-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d5096-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5096-129">**CBaseOutputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="d5096-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




