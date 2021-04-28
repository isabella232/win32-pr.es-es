---
description: 'Método CTransformInputPin.CompleteConnect: el método CompleteConnect completa una conexión a otro pin.'
ms.assetid: 568cee55-b9ea-4fc2-ac9d-0080b7de9790
title: Método CTransformInputPin.CompleteConnect (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 20f378479209b2614116ba25f51950923358f1b2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085013"
---
# <a name="ctransforminputpincompleteconnect-method"></a><span data-ttu-id="fa36e-103">Método CTransformInputPin.CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="fa36e-103">CTransformInputPin.CompleteConnect method</span></span>

<span data-ttu-id="fa36e-104">El `CompleteConnect` método completa una conexión a otro pin.</span><span class="sxs-lookup"><span data-stu-id="fa36e-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa36e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa36e-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="fa36e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa36e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa36e-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="fa36e-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="fa36e-108">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro pin.</span><span class="sxs-lookup"><span data-stu-id="fa36e-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa36e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa36e-109">Return value</span></span>

<span data-ttu-id="fa36e-110">Devuelve S \_ OK u otro valor **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="fa36e-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa36e-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fa36e-111">Remarks</span></span>

<span data-ttu-id="fa36e-112">Este método invalida el [**método CBasePin::CompleteConnect.**](cbasepin-completeconnect.md)</span><span class="sxs-lookup"><span data-stu-id="fa36e-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="fa36e-113">Llama al método [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) del filtro, que devuelve S \_ OK en la clase base.</span><span class="sxs-lookup"><span data-stu-id="fa36e-113">It calls the filter's [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="fa36e-114">La clase derivada puede invalidar el **método CTransformFilter::CompleteConnect** para realizar comprobaciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="fa36e-114">The derived class can override the **CTransformFilter::CompleteConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa36e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa36e-115">Requirements</span></span>



| <span data-ttu-id="fa36e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa36e-116">Requirement</span></span> | <span data-ttu-id="fa36e-117">Value</span><span class="sxs-lookup"><span data-stu-id="fa36e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa36e-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa36e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="fa36e-119"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa36e-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fa36e-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa36e-120">Library</span></span><br/> | <dl> <span data-ttu-id="fa36e-121"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="fa36e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




