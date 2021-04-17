---
description: 'El método EndFlush finaliza una operación de vaciado. Este método implementa el método IPin:: EndFlush.'
ms.assetid: ebc70df3-e99d-4292-990b-99b79ff06461
title: Método CTransformInputPin. EndFlush (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0fe6afeaa0ca3d47b278987af494221e8f50340
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660683"
---
# <a name="ctransforminputpinendflush-method"></a><span data-ttu-id="d2c57-104">CTransformInputPin. EndFlush, método</span><span class="sxs-lookup"><span data-stu-id="d2c57-104">CTransformInputPin.EndFlush method</span></span>

<span data-ttu-id="d2c57-105">El `EndFlush` método finaliza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="d2c57-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="d2c57-106">Este método implementa el método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="d2c57-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2c57-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2c57-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="d2c57-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2c57-108">Parameters</span></span>

<span data-ttu-id="d2c57-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d2c57-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d2c57-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2c57-110">Return value</span></span>

<span data-ttu-id="d2c57-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d2c57-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d2c57-112">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d2c57-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="d2c57-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d2c57-113">Return code</span></span>                                                                                           | <span data-ttu-id="d2c57-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2c57-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="d2c57-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d2c57-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="d2c57-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="d2c57-116">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="d2c57-117"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="d2c57-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="d2c57-118">El PIN de salida no está conectado.</span><span class="sxs-lookup"><span data-stu-id="d2c57-118">Output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d2c57-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2c57-119">Remarks</span></span>

<span data-ttu-id="d2c57-120">Este método llama al método [**CTransformFilter:: EndFlush**](ctransformfilter-endflush.md) del filtro para proporcionar la llamada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="d2c57-120">This method calls the filter's [**CTransformFilter::EndFlush**](ctransformfilter-endflush.md) method to deliver the call downstream.</span></span> <span data-ttu-id="d2c57-121">A continuación, llama al método [**CBaseInputPin:: EndFlush**](cbaseinputpin-endflush.md) del PIN.</span><span class="sxs-lookup"><span data-stu-id="d2c57-121">Then it calls the pin's [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2c57-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2c57-122">Requirements</span></span>



| <span data-ttu-id="d2c57-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2c57-123">Requirement</span></span> | <span data-ttu-id="d2c57-124">Value</span><span class="sxs-lookup"><span data-stu-id="d2c57-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2c57-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2c57-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d2c57-126"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2c57-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d2c57-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2c57-127">Library</span></span><br/> | <dl> <span data-ttu-id="d2c57-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d2c57-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




