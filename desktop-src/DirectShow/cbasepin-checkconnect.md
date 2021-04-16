---
description: El método CheckConnect determina si una conexión de PIN es adecuada.
ms.assetid: 511a1594-f3f8-4725-afcd-f14f3a4ebf20
title: Método CBasePin. CheckConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24d5c221da417fd1fc2b3f9f140536f825b2f9d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671634"
---
# <a name="cbasepincheckconnect-method"></a><span data-ttu-id="a6820-103">CBasePin. CheckConnect, método</span><span class="sxs-lookup"><span data-stu-id="a6820-103">CBasePin.CheckConnect method</span></span>

<span data-ttu-id="a6820-104">El `CheckConnect` método determina si una conexión de PIN es adecuada.</span><span class="sxs-lookup"><span data-stu-id="a6820-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6820-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6820-105">Syntax</span></span>


```C++
virtual HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="a6820-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6820-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6820-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="a6820-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="a6820-108">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro PIN.</span><span class="sxs-lookup"><span data-stu-id="a6820-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6820-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6820-109">Return value</span></span>

<span data-ttu-id="a6820-110">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="a6820-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="a6820-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a6820-111">Return code</span></span>                                                                                               | <span data-ttu-id="a6820-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6820-112">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="a6820-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a6820-113"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="a6820-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="a6820-114">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="a6820-115"><dt>**\_ \_ dirección no válida de VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a6820-115"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="a6820-116">Las direcciones de PIN no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="a6820-116">Pin directions are not compatible.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a6820-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6820-117">Remarks</span></span>

<span data-ttu-id="a6820-118">Se llama a este método en ambos PIN al inicio del proceso de conexión.</span><span class="sxs-lookup"><span data-stu-id="a6820-118">This method is called on both pins at the start of the connection process.</span></span> <span data-ttu-id="a6820-119">El PIN de conexión lo llama desde dentro del método [**CBasePin:: Connect**](cbasepin-connect.md) y el PIN receptor lo llama desde dentro del método [**CBasePin:: ReceiveConnection**](cbasepin-receiveconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="a6820-119">The connecting pin calls it from within the [**CBasePin::Connect**](cbasepin-connect.md) method, and the receiving pin calls it from within the [**CBasePin::ReceiveConnection**](cbasepin-receiveconnection.md) method.</span></span>

<span data-ttu-id="a6820-120">Utilice este método para determinar si el PIN especificado por el parámetro *pPin* es adecuado para una conexión.</span><span class="sxs-lookup"><span data-stu-id="a6820-120">Use this method to determine whether the pin specified by the *pPin* parameter is suitable for a connection.</span></span> <span data-ttu-id="a6820-121">La clase base devuelve un error si ambos PIN tienen la misma dirección (tanto de entrada como de salida).</span><span class="sxs-lookup"><span data-stu-id="a6820-121">The base class returns an error if both pins have the same direction (both input, or both output).</span></span> <span data-ttu-id="a6820-122">Las clases derivadas pueden invalidar este método para comprobar otras características del código PIN.</span><span class="sxs-lookup"><span data-stu-id="a6820-122">Derived classes can override this method to verify other features in the pin.</span></span> <span data-ttu-id="a6820-123">Por ejemplo, la clase [**CBaseOutputPin**](cbaseoutputpin.md) consulta el PIN de entrada para su interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="a6820-123">For example, the [**CBaseOutputPin**](cbaseoutputpin.md) class queries the input pin for its [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

<span data-ttu-id="a6820-124">Si se produce un error en este método, se produce un error en la conexión y el PIN llama al método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="a6820-124">If this method fails, the connection fails and the pin calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="a6820-125">Use **BreakConnect** para liberar los recursos obtenidos en `CheckConnect` .</span><span class="sxs-lookup"><span data-stu-id="a6820-125">Use **BreakConnect** to free any resources obtained in `CheckConnect`.</span></span> <span data-ttu-id="a6820-126">Por ejemplo, si `CheckConnect` llama al método **QueryInterface** , **BreakConnect** debe liberar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="a6820-126">For example, if `CheckConnect` calls the **QueryInterface** method, **BreakConnect** must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6820-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6820-127">Requirements</span></span>



| <span data-ttu-id="a6820-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6820-128">Requirement</span></span> | <span data-ttu-id="a6820-129">Value</span><span class="sxs-lookup"><span data-stu-id="a6820-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6820-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6820-130">Header</span></span><br/>  | <dl> <span data-ttu-id="a6820-131"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6820-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a6820-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a6820-132">Library</span></span><br/> | <dl> <span data-ttu-id="a6820-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a6820-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6820-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6820-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6820-135">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="a6820-135">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




