---
description: 'El método BeginFlush inicia una operación de vaciado. Este método implementa el método IPin:: BeginFlush.'
ms.assetid: 7c76ca06-dc3c-4f9a-9761-32aea7db4c7e
title: Método CTransformInputPin. BeginFlush (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4d028634364ca59ae293d9ebb60a464974ccd74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660639"
---
# <a name="ctransforminputpinbeginflush-method"></a><span data-ttu-id="de682-104">CTransformInputPin. BeginFlush, método</span><span class="sxs-lookup"><span data-stu-id="de682-104">CTransformInputPin.BeginFlush method</span></span>

<span data-ttu-id="de682-105">El `BeginFlush` método inicia una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="de682-105">The `BeginFlush` method begins a flush operation.</span></span> <span data-ttu-id="de682-106">Este método implementa el método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="de682-106">This method implements the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="de682-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de682-107">Syntax</span></span>


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="de682-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de682-108">Parameters</span></span>

<span data-ttu-id="de682-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="de682-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="de682-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de682-110">Return value</span></span>

<span data-ttu-id="de682-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="de682-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="de682-112">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="de682-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="de682-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="de682-113">Return code</span></span>                                                                                           | <span data-ttu-id="de682-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="de682-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="de682-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="de682-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="de682-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="de682-116">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="de682-117"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="de682-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="de682-118">El PIN de salida no está conectado.</span><span class="sxs-lookup"><span data-stu-id="de682-118">Output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="de682-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de682-119">Remarks</span></span>

<span data-ttu-id="de682-120">Este método llama al método [**CBaseInputPin:: BeginFlush**](cbaseinputpin-beginflush.md) del PIN.</span><span class="sxs-lookup"><span data-stu-id="de682-120">This method calls the pin's [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md) method.</span></span> <span data-ttu-id="de682-121">Después, llama al método [**CTransformFilter:: BeginFlush**](ctransformfilter-beginflush.md) del filtro para proporcionar la llamada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="de682-121">Then it calls the filter's [**CTransformFilter::BeginFlush**](ctransformfilter-beginflush.md) method to deliver the call downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="de682-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de682-122">Requirements</span></span>



| <span data-ttu-id="de682-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="de682-123">Requirement</span></span> | <span data-ttu-id="de682-124">Value</span><span class="sxs-lookup"><span data-stu-id="de682-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de682-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de682-125">Header</span></span><br/>  | <dl> <span data-ttu-id="de682-126"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de682-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="de682-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="de682-127">Library</span></span><br/> | <dl> <span data-ttu-id="de682-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="de682-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




