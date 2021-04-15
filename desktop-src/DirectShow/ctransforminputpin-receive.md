---
description: 'El método Receive recibe el siguiente ejemplo multimedia en la secuencia. Este método implementa el método IMemInputPin:: Receive.'
ms.assetid: 65e4f8f5-2aa2-435b-84b4-e65af3f51afc
title: Método CTransformInputPin. Receive (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59b087c4b783305b831871a030d1006d576e7d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661316"
---
# <a name="ctransforminputpinreceive-method"></a><span data-ttu-id="b6f9d-104">CTransformInputPin. Receive (método)</span><span class="sxs-lookup"><span data-stu-id="b6f9d-104">CTransformInputPin.Receive method</span></span>

<span data-ttu-id="b6f9d-105">El `Receive` método recibe el siguiente ejemplo multimedia en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b6f9d-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="b6f9d-106">Este método implementa el método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .</span><span class="sxs-lookup"><span data-stu-id="b6f9d-106">This method implements the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6f9d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6f9d-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="b6f9d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6f9d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6f9d-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="b6f9d-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="b6f9d-110">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b6f9d-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6f9d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6f9d-111">Return value</span></span>

<span data-ttu-id="b6f9d-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b6f9d-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b6f9d-113">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b6f9d-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="b6f9d-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b6f9d-114">Return code</span></span>                                                                             | <span data-ttu-id="b6f9d-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6f9d-115">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="b6f9d-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="b6f9d-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="b6f9d-117">El PIN se está vaciando actualmente; se rechazó el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b6f9d-117">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="b6f9d-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b6f9d-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="b6f9d-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="b6f9d-119">Success.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="b6f9d-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6f9d-120">Remarks</span></span>

<span data-ttu-id="b6f9d-121">Este método llama al método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) del PIN, que comprueba el estado de streaming del PIN y comprueba los cambios de formato en el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="b6f9d-121">This method calls the pin's [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method, which checks the pin's streaming state and checks for format changes in the media type.</span></span> <span data-ttu-id="b6f9d-122">A continuación, llama al método [**CTransformFilter:: Receive**](ctransformfilter-receive.md) del filtro, que procesa el ejemplo y lo entrega hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="b6f9d-122">Then it calls the filter's [**CTransformFilter::Receive**](ctransformfilter-receive.md) method, which processes the sample and delivers it downstream.</span></span>

<span data-ttu-id="b6f9d-123">Si el filtro necesita tener acceso al ejemplo después de que este método devuelva, debe contener un recuento de referencias llamando al método **IUnknown:: AddRef** en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b6f9d-123">If the filter needs to access the sample after this method returns, it should hold a reference count by calling the **IUnknown::AddRef** method on the sample.</span></span> <span data-ttu-id="b6f9d-124">Por ejemplo, algunos filtros del descodificador necesitan el ejemplo actual para descodificar el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="b6f9d-124">For example, some decoder filters need the current sample in order to decode the next sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6f9d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6f9d-125">Requirements</span></span>



| <span data-ttu-id="b6f9d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6f9d-126">Requirement</span></span> | <span data-ttu-id="b6f9d-127">Value</span><span class="sxs-lookup"><span data-stu-id="b6f9d-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6f9d-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6f9d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b6f9d-129"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6f9d-129"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b6f9d-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b6f9d-130">Library</span></span><br/> | <dl> <span data-ttu-id="b6f9d-131"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b6f9d-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




