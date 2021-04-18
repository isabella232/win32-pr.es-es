---
description: 'El método ReceiveCanBlock determina si las llamadas al método IMemInputPin:: Receive podrían bloquearse. Este método implementa el método IMemInputPin:: ReceiveCanBlock.'
ms.assetid: db96e389-e1bc-4b38-8d0a-a20f0d3a4460
title: Método CBaseInputPin. ReceiveCanBlock (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveCanBlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93c80d6c8f834b45381b89e80d2e0acc392bf25a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661303"
---
# <a name="cbaseinputpinreceivecanblock-method"></a><span data-ttu-id="b2266-104">CBaseInputPin. ReceiveCanBlock, método</span><span class="sxs-lookup"><span data-stu-id="b2266-104">CBaseInputPin.ReceiveCanBlock method</span></span>

<span data-ttu-id="b2266-105">El `ReceiveCanBlock` método determina si las llamadas al método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) podrían bloquearse.</span><span class="sxs-lookup"><span data-stu-id="b2266-105">The `ReceiveCanBlock` method determines whether calls to the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method might block.</span></span> <span data-ttu-id="b2266-106">Este método implementa el método [**IMemInputPin:: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) .</span><span class="sxs-lookup"><span data-stu-id="b2266-106">This method implements the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2266-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2266-107">Syntax</span></span>


```C++
HRESULT ReceiveCanBlock();
```



## <a name="parameters"></a><span data-ttu-id="b2266-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2266-108">Parameters</span></span>

<span data-ttu-id="b2266-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b2266-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b2266-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2266-110">Return value</span></span>

<span data-ttu-id="b2266-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b2266-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b2266-112">Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b2266-112">Possible value include those listed in the following table.</span></span>



| <span data-ttu-id="b2266-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b2266-113">Return code</span></span>                                                                             | <span data-ttu-id="b2266-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2266-114">Description</span></span>                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="b2266-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="b2266-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="b2266-116">El PIN no se bloqueará en una llamada a **Receive**.</span><span class="sxs-lookup"><span data-stu-id="b2266-116">The pin will not block on a call to **Receive**.</span></span><br/> |
| <dl> <span data-ttu-id="b2266-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b2266-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="b2266-118">El PIN podría bloquearse en una llamada a **Receive**.</span><span class="sxs-lookup"><span data-stu-id="b2266-118">The pin might block on a call to **Receive**.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="b2266-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b2266-119">Remarks</span></span>

<span data-ttu-id="b2266-120">Devuelve S \_ false si se garantiza que las llamadas al método **Receive** no se bloquean.</span><span class="sxs-lookup"><span data-stu-id="b2266-120">Return S\_FALSE if calls to the **Receive** method are guaranteed not to block.</span></span> <span data-ttu-id="b2266-121">De lo contrario, devuelve \_ un código de error o correcto.</span><span class="sxs-lookup"><span data-stu-id="b2266-121">Otherwise, return S\_OK or an error code.</span></span> <span data-ttu-id="b2266-122">Si el método **Receive** llama a **Receive** en un PIN de nivel inferior, el PIN de bajada podría bloquearse; `ReceiveCanBlock` debe tener en cuenta este factor.</span><span class="sxs-lookup"><span data-stu-id="b2266-122">If the **Receive** method calls **Receive** on a downstream pin, the downstream pin might block; `ReceiveCanBlock` must take that factor into account.</span></span>

<span data-ttu-id="b2266-123">Un filtro de nivel superior puede utilizar este método para determinar su estrategia de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="b2266-123">An upstream filter can use this method to determine its threading strategy.</span></span> <span data-ttu-id="b2266-124">Si el método **Receive** podría bloquearse, el filtro de nivel superior podría decidir usar un subproceso de trabajo que almacene en búfer los datos.</span><span class="sxs-lookup"><span data-stu-id="b2266-124">If the **Receive** method might block, the upstream filter might decide to use a worker thread that buffers data.</span></span> <span data-ttu-id="b2266-125">Vea la clase [**COutputQueue**](coutputqueue.md) para obtener una implementación de esta estrategia.</span><span class="sxs-lookup"><span data-stu-id="b2266-125">See the [**COutputQueue**](coutputqueue.md) class for an implementation of this strategy.</span></span>

<span data-ttu-id="b2266-126">En la clase base, este método devuelve S \_ OK cuando se cumple alguna de las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="b2266-126">In the base class, this method returns S\_OK when any of the following are true:</span></span>

-   <span data-ttu-id="b2266-127">El filtro no tiene clavijas de salida.</span><span class="sxs-lookup"><span data-stu-id="b2266-127">The filter has no output pins.</span></span>
-   <span data-ttu-id="b2266-128">Un PIN de entrada conectado a este filtro indica que podría bloquearse.</span><span class="sxs-lookup"><span data-stu-id="b2266-128">An input pin connected to this filter signals that it might block.</span></span>
-   <span data-ttu-id="b2266-129">Un PIN de entrada conectado a este filtro no admite la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="b2266-129">An input pin connected to this filter does not support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2266-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2266-130">Requirements</span></span>



| <span data-ttu-id="b2266-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2266-131">Requirement</span></span> | <span data-ttu-id="b2266-132">Value</span><span class="sxs-lookup"><span data-stu-id="b2266-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2266-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2266-133">Header</span></span><br/>  | <dl> <span data-ttu-id="b2266-134"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2266-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b2266-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b2266-135">Library</span></span><br/> | <dl> <span data-ttu-id="b2266-136"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b2266-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2266-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2266-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2266-138">**Clase CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="b2266-138">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




