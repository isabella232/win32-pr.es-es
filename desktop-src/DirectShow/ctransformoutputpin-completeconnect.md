---
description: El método CompleteConnect completa una conexión a otro PIN.
ms.assetid: 14bc48bc-ddfb-4491-8d5b-9e5ac601ba04
title: Método CTransformOutputPin. CompleteConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8d0c9c9fc7096191d7cdedffa21e2639fa0750ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681171"
---
# <a name="ctransformoutputpincompleteconnect-method"></a><span data-ttu-id="51a06-103">CTransformOutputPin. CompleteConnect, método</span><span class="sxs-lookup"><span data-stu-id="51a06-103">CTransformOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="51a06-104">El `CompleteConnect` método completa una conexión a otro PIN.</span><span class="sxs-lookup"><span data-stu-id="51a06-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="51a06-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51a06-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="51a06-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51a06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51a06-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="51a06-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="51a06-108">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro PIN.</span><span class="sxs-lookup"><span data-stu-id="51a06-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51a06-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51a06-109">Return value</span></span>

<span data-ttu-id="51a06-110">Devuelve S \_ OK u otro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="51a06-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="51a06-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51a06-111">Remarks</span></span>

<span data-ttu-id="51a06-112">Este método invalida el método [**CBaseOutputPin:: CompleteConnect**](cbaseoutputpin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="51a06-112">This method overrides the [**CBaseOutputPin::CompleteConnect**](cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="51a06-113">Llama al método [**CTransformFilter:: CompleteConnect**](ctransformfilter-completeconnect.md) del filtro, que devuelve s \_ OK en la clase base.</span><span class="sxs-lookup"><span data-stu-id="51a06-113">It calls the filter's [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="51a06-114">La clase derivada puede invalidar el método **CTransformFilter:: CompleteConnect** para realizar comprobaciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="51a06-114">The derived class can override the **CTransformFilter::CompleteConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="51a06-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51a06-115">Requirements</span></span>



| <span data-ttu-id="51a06-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="51a06-116">Requirement</span></span> | <span data-ttu-id="51a06-117">Value</span><span class="sxs-lookup"><span data-stu-id="51a06-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51a06-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51a06-118">Header</span></span><br/>  | <dl> <span data-ttu-id="51a06-119"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51a06-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="51a06-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="51a06-120">Library</span></span><br/> | <dl> <span data-ttu-id="51a06-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="51a06-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




