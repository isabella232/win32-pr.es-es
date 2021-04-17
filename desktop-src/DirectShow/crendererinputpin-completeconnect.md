---
description: 'El método CompleteConnect completa una conexión a un PIN de salida. Este método invalida el método CBasePin:: CompleteConnect.'
ms.assetid: 32d95815-e018-4724-8cf3-8cd093ede517
title: Método CRendererInputPin. CompleteConnect (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e868693308d40fb786f201a9d7f056dd88326ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661290"
---
# <a name="crendererinputpincompleteconnect-method"></a><span data-ttu-id="3161a-104">CRendererInputPin. CompleteConnect, método</span><span class="sxs-lookup"><span data-stu-id="3161a-104">CRendererInputPin.CompleteConnect method</span></span>

<span data-ttu-id="3161a-105">El `CompleteConnect` método completa una conexión a un PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="3161a-105">The `CompleteConnect` method completes a connection to an output pin.</span></span> <span data-ttu-id="3161a-106">Este método invalida el método [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="3161a-106">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3161a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3161a-107">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="3161a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3161a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3161a-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="3161a-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="3161a-110">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN de salida</span><span class="sxs-lookup"><span data-stu-id="3161a-110">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3161a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3161a-111">Return value</span></span>

<span data-ttu-id="3161a-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3161a-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3161a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3161a-113">Requirements</span></span>



| <span data-ttu-id="3161a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3161a-114">Requirement</span></span> | <span data-ttu-id="3161a-115">Value</span><span class="sxs-lookup"><span data-stu-id="3161a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3161a-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3161a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3161a-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3161a-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3161a-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3161a-118">Library</span></span><br/> | <dl> <span data-ttu-id="3161a-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3161a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3161a-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="3161a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3161a-121">**Clase CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="3161a-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




