---
description: 'El método CBaseInputPin inicia una operación de vaciado. Este método implementa el método IPin:: BeginFlush.'
ms.assetid: 3f149d4f-765b-44c1-87e5-6313f6a4d50d
title: Método CBaseInputPin. BeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93c0f687daf65e91443f4f59896d641b9b0cfd43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660573"
---
# <a name="cbaseinputpinbeginflush-method"></a><span data-ttu-id="a25b7-104">CBaseInputPin. BeginFlush, método</span><span class="sxs-lookup"><span data-stu-id="a25b7-104">CBaseInputPin.BeginFlush method</span></span>

<span data-ttu-id="a25b7-105">El `CBaseInputPin` método inicia una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="a25b7-105">The `CBaseInputPin` method begins a flush operation.</span></span> <span data-ttu-id="a25b7-106">Este método implementa el método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="a25b7-106">This method implements the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a25b7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a25b7-107">Syntax</span></span>


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="a25b7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a25b7-108">Parameters</span></span>

<span data-ttu-id="a25b7-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a25b7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a25b7-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a25b7-110">Return value</span></span>

<span data-ttu-id="a25b7-111">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="a25b7-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a25b7-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a25b7-112">Remarks</span></span>

<span data-ttu-id="a25b7-113">Este método establece la marca [**CBaseInputPin:: m \_ BFlushing**](cbaseinputpin-m-bflushing.md) en **true**, lo que hace que el método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) rechace cualquier ejemplo más.</span><span class="sxs-lookup"><span data-stu-id="a25b7-113">This method sets the [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md) flag to **TRUE**, which causes the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method to reject any more samples.</span></span>

<span data-ttu-id="a25b7-114">La clase derivada debe invalidar este método y realizar los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a25b7-114">The derived class must override this method and perform the following steps:</span></span>

1.  <span data-ttu-id="a25b7-115">Llame al método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) en las clavijas de entrada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="a25b7-115">Call the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on downstream input pins.</span></span> <span data-ttu-id="a25b7-116">Si el PIN no ha entregado todavía ningún ejemplo de multimedia en el nivel inferior, puede omitir este paso.</span><span class="sxs-lookup"><span data-stu-id="a25b7-116">If the pin has not yet delivered any media samples downstream, you can skip this step.</span></span> <span data-ttu-id="a25b7-117">Si los pin de salida derivan de la clase [**CBaseOutputPin**](cbaseoutputpin.md) , puede llamar al método [**eliverbeginflush de CBaseOutputPin::D**](cbaseoutputpin-deliverbeginflush.md) .</span><span class="sxs-lookup"><span data-stu-id="a25b7-117">If your output pins derive from the [**CBaseOutputPin**](cbaseoutputpin.md) class, you can call the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span>
2.  <span data-ttu-id="a25b7-118">Llame al método de la clase base.</span><span class="sxs-lookup"><span data-stu-id="a25b7-118">Call the base class method.</span></span>
3.  <span data-ttu-id="a25b7-119">Empezar a descartar los datos en cola.</span><span class="sxs-lookup"><span data-stu-id="a25b7-119">Begin discarding queued data.</span></span>
4.  <span data-ttu-id="a25b7-120">Devuelve de cualquier llamada bloqueada al método **Receive** .</span><span class="sxs-lookup"><span data-stu-id="a25b7-120">Return from any blocked calls to the **Receive** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a25b7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a25b7-121">Requirements</span></span>



| <span data-ttu-id="a25b7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a25b7-122">Requirement</span></span> | <span data-ttu-id="a25b7-123">Value</span><span class="sxs-lookup"><span data-stu-id="a25b7-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a25b7-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a25b7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a25b7-125"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a25b7-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a25b7-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a25b7-126">Library</span></span><br/> | <dl> <span data-ttu-id="a25b7-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a25b7-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a25b7-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a25b7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a25b7-129">**Clase CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="a25b7-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




