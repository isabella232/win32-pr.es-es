---
description: 'Método CBasePin.CheckConnect: el método CheckConnect determina si una conexión de pin es adecuada.'
ms.assetid: 511a1594-f3f8-4725-afcd-f14f3a4ebf20
title: Método CBasePin.CheckConnect (Amfilter.h)
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
ms.openlocfilehash: 314d3e1ce0e73e60ea07bb4f7270fa04f69750c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096053"
---
# <a name="cbasepincheckconnect-method"></a><span data-ttu-id="20d5d-103">Método CBasePin.CheckConnect</span><span class="sxs-lookup"><span data-stu-id="20d5d-103">CBasePin.CheckConnect method</span></span>

<span data-ttu-id="20d5d-104">El `CheckConnect` método determina si una conexión de pin es adecuada.</span><span class="sxs-lookup"><span data-stu-id="20d5d-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="20d5d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20d5d-105">Syntax</span></span>


```C++
virtual HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="20d5d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20d5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20d5d-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="20d5d-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="20d5d-108">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro pin.</span><span class="sxs-lookup"><span data-stu-id="20d5d-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20d5d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20d5d-109">Return value</span></span>

<span data-ttu-id="20d5d-110">Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="20d5d-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="20d5d-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="20d5d-111">Return code</span></span>                                                                                               | <span data-ttu-id="20d5d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="20d5d-112">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="20d5d-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="20d5d-113"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="20d5d-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="20d5d-114">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="20d5d-115"><dt>**VFW \_ E DIRECCIÓN NO \_ \_ VÁLIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="20d5d-115"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="20d5d-116">Las direcciones del pin no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="20d5d-116">Pin directions are not compatible.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="20d5d-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="20d5d-117">Remarks</span></span>

<span data-ttu-id="20d5d-118">Se llama a este método en ambos pines al principio del proceso de conexión.</span><span class="sxs-lookup"><span data-stu-id="20d5d-118">This method is called on both pins at the start of the connection process.</span></span> <span data-ttu-id="20d5d-119">El pin de conexión lo llama desde el método [**CBasePin::Connect**](cbasepin-connect.md) y el pin receptor lo llama desde el método [**CBasePin::ReceiveConnection.**](cbasepin-receiveconnection.md)</span><span class="sxs-lookup"><span data-stu-id="20d5d-119">The connecting pin calls it from within the [**CBasePin::Connect**](cbasepin-connect.md) method, and the receiving pin calls it from within the [**CBasePin::ReceiveConnection**](cbasepin-receiveconnection.md) method.</span></span>

<span data-ttu-id="20d5d-120">Use este método para determinar si el pin especificado por el *parámetro pPin* es adecuado para una conexión.</span><span class="sxs-lookup"><span data-stu-id="20d5d-120">Use this method to determine whether the pin specified by the *pPin* parameter is suitable for a connection.</span></span> <span data-ttu-id="20d5d-121">La clase base devuelve un error si ambos pines tienen la misma dirección (entrada o ambas salidas).</span><span class="sxs-lookup"><span data-stu-id="20d5d-121">The base class returns an error if both pins have the same direction (both input, or both output).</span></span> <span data-ttu-id="20d5d-122">Las clases derivadas pueden invalidar este método para comprobar otras características del pin.</span><span class="sxs-lookup"><span data-stu-id="20d5d-122">Derived classes can override this method to verify other features in the pin.</span></span> <span data-ttu-id="20d5d-123">Por ejemplo, la [**clase CBaseOutputPin**](cbaseoutputpin.md) consulta la chincha de entrada para su [**interfaz IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)</span><span class="sxs-lookup"><span data-stu-id="20d5d-123">For example, the [**CBaseOutputPin**](cbaseoutputpin.md) class queries the input pin for its [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

<span data-ttu-id="20d5d-124">Si se produce un error en este método, se produce un error en la conexión y el pin llama [**al método CBasePin::BreakConnect.**](cbasepin-breakconnect.md)</span><span class="sxs-lookup"><span data-stu-id="20d5d-124">If this method fails, the connection fails and the pin calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="20d5d-125">Use **BreakConnect** para liberar los recursos obtenidos en `CheckConnect` .</span><span class="sxs-lookup"><span data-stu-id="20d5d-125">Use **BreakConnect** to free any resources obtained in `CheckConnect`.</span></span> <span data-ttu-id="20d5d-126">Por ejemplo, si `CheckConnect` llama al **método QueryInterface,** **BreakConnect** debe liberar la interfaz .</span><span class="sxs-lookup"><span data-stu-id="20d5d-126">For example, if `CheckConnect` calls the **QueryInterface** method, **BreakConnect** must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="20d5d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20d5d-127">Requirements</span></span>



| <span data-ttu-id="20d5d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="20d5d-128">Requirement</span></span> | <span data-ttu-id="20d5d-129">Value</span><span class="sxs-lookup"><span data-stu-id="20d5d-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20d5d-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20d5d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="20d5d-131"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="20d5d-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="20d5d-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20d5d-132">Library</span></span><br/> | <dl> <span data-ttu-id="20d5d-133"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="20d5d-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20d5d-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="20d5d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20d5d-135">**CBasePin (clase)**</span><span class="sxs-lookup"><span data-stu-id="20d5d-135">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




