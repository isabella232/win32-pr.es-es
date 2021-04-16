---
description: El método CompleteConnect completa una conexión a otro PIN.
ms.assetid: 10cbf29c-2e1a-419c-b0c0-c99f9a285810
title: Método CBasePin. CompleteConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9068bf63d3168a8c6d9e1bca2ef709f63e80a3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671614"
---
# <a name="cbasepincompleteconnect-method"></a><span data-ttu-id="5726f-103">CBasePin. CompleteConnect, método</span><span class="sxs-lookup"><span data-stu-id="5726f-103">CBasePin.CompleteConnect method</span></span>

<span data-ttu-id="5726f-104">El `CompleteConnect` método completa una conexión a otro PIN.</span><span class="sxs-lookup"><span data-stu-id="5726f-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="5726f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5726f-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="5726f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5726f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5726f-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="5726f-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="5726f-108">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro PIN.</span><span class="sxs-lookup"><span data-stu-id="5726f-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5726f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5726f-109">Return value</span></span>

<span data-ttu-id="5726f-110">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="5726f-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5726f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5726f-111">Remarks</span></span>

<span data-ttu-id="5726f-112">Se llama a este método en ambos PIN al final del proceso de conexión.</span><span class="sxs-lookup"><span data-stu-id="5726f-112">This method is called on both pins at the end of the connection process.</span></span> <span data-ttu-id="5726f-113">El PIN de conexión lo llama desde dentro del método [**CBasePin:: Connect**](cbasepin-connect.md) y el PIN receptor lo llama desde dentro del método [**CBasePin:: ReceiveConnection**](cbasepin-receiveconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="5726f-113">The connecting pin calls it from within the [**CBasePin::Connect**](cbasepin-connect.md) method, and the receiving pin calls it from within the [**CBasePin::ReceiveConnection**](cbasepin-receiveconnection.md) method.</span></span>

<span data-ttu-id="5726f-114">En la clase base, este método simplemente devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="5726f-114">In the base class, this method simply returns S\_OK.</span></span> <span data-ttu-id="5726f-115">Si una clase derivada tiene algún requisito para completar una conexión, debe invalidar este método.</span><span class="sxs-lookup"><span data-stu-id="5726f-115">If a derived class has any requirements for completing a connection, it should override this method.</span></span> <span data-ttu-id="5726f-116">Por ejemplo, la clase [**CBaseOutputPin**](cbaseoutputpin.md) usa este método para decidir el asignador de memoria.</span><span class="sxs-lookup"><span data-stu-id="5726f-116">For example, the [**CBaseOutputPin**](cbaseoutputpin.md) class uses this method to decide the memory allocator.</span></span>

<span data-ttu-id="5726f-117">Si se produce un error en este método, también se produce un error en el intento de conexión general y el PIN se desconecta del PIN receptor.</span><span class="sxs-lookup"><span data-stu-id="5726f-117">If this method fails, the overall connection attempt also fails, and the pin disconnects from the receiving pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="5726f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5726f-118">Requirements</span></span>



| <span data-ttu-id="5726f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5726f-119">Requirement</span></span> | <span data-ttu-id="5726f-120">Value</span><span class="sxs-lookup"><span data-stu-id="5726f-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5726f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5726f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5726f-122"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5726f-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5726f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5726f-123">Library</span></span><br/> | <dl> <span data-ttu-id="5726f-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5726f-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5726f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5726f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5726f-126">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="5726f-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




