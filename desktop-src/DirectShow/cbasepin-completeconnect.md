---
description: 'Método CBasePin.CompleteConnect: el método CompleteConnect completa una conexión a otro pin.'
ms.assetid: 10cbf29c-2e1a-419c-b0c0-c99f9a285810
title: Método CBasePin.CompleteConnect (Amfilter.h)
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
ms.openlocfilehash: fee207d7a17f12cc81036fbd4f82ec49a99f4a31
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096043"
---
# <a name="cbasepincompleteconnect-method"></a><span data-ttu-id="7f3e4-103">Método CBasePin.CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="7f3e4-103">CBasePin.CompleteConnect method</span></span>

<span data-ttu-id="7f3e4-104">El `CompleteConnect` método completa una conexión a otro pin.</span><span class="sxs-lookup"><span data-stu-id="7f3e4-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f3e4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f3e4-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="7f3e4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f3e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f3e4-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="7f3e4-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="7f3e4-108">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro pin.</span><span class="sxs-lookup"><span data-stu-id="7f3e4-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f3e4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f3e4-109">Return value</span></span>

<span data-ttu-id="7f3e4-110">Devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7f3e4-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f3e4-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7f3e4-111">Remarks</span></span>

<span data-ttu-id="7f3e4-112">Se llama a este método en ambos pines al final del proceso de conexión.</span><span class="sxs-lookup"><span data-stu-id="7f3e4-112">This method is called on both pins at the end of the connection process.</span></span> <span data-ttu-id="7f3e4-113">El pin de conexión lo llama desde el método [**CBasePin::Connect**](cbasepin-connect.md) y el pin receptor lo llama desde el método [**CBasePin::ReceiveConnection.**](cbasepin-receiveconnection.md)</span><span class="sxs-lookup"><span data-stu-id="7f3e4-113">The connecting pin calls it from within the [**CBasePin::Connect**](cbasepin-connect.md) method, and the receiving pin calls it from within the [**CBasePin::ReceiveConnection**](cbasepin-receiveconnection.md) method.</span></span>

<span data-ttu-id="7f3e4-114">En la clase base, este método simplemente devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7f3e4-114">In the base class, this method simply returns S\_OK.</span></span> <span data-ttu-id="7f3e4-115">Si una clase derivada tiene algún requisito para completar una conexión, debe invalidar este método.</span><span class="sxs-lookup"><span data-stu-id="7f3e4-115">If a derived class has any requirements for completing a connection, it should override this method.</span></span> <span data-ttu-id="7f3e4-116">Por ejemplo, la [**clase CBaseOutputPin**](cbaseoutputpin.md) usa este método para decidir el asignador de memoria.</span><span class="sxs-lookup"><span data-stu-id="7f3e4-116">For example, the [**CBaseOutputPin**](cbaseoutputpin.md) class uses this method to decide the memory allocator.</span></span>

<span data-ttu-id="7f3e4-117">Si se produce un error en este método, también se produce un error en el intento de conexión general y el pin se desconecta del pin receptor.</span><span class="sxs-lookup"><span data-stu-id="7f3e4-117">If this method fails, the overall connection attempt also fails, and the pin disconnects from the receiving pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f3e4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f3e4-118">Requirements</span></span>



| <span data-ttu-id="7f3e4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f3e4-119">Requirement</span></span> | <span data-ttu-id="7f3e4-120">Value</span><span class="sxs-lookup"><span data-stu-id="7f3e4-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f3e4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f3e4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7f3e4-122"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f3e4-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7f3e4-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7f3e4-123">Library</span></span><br/> | <dl> <span data-ttu-id="7f3e4-124"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7f3e4-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f3e4-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7f3e4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f3e4-126">**CBasePin (clase)**</span><span class="sxs-lookup"><span data-stu-id="7f3e4-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




