---
description: El método CheckConnect determina si una conexión de PIN es adecuada.
ms.assetid: 3dae5c6d-720e-4445-b601-3bdfe32f4c21
title: Método CTransformOutputPin. CheckConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9a20eb8d3e20679cb8805d3a1cd8e167ef0bfd5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680883"
---
# <a name="ctransformoutputpincheckconnect-method"></a><span data-ttu-id="0ac60-103">CTransformOutputPin. CheckConnect, método</span><span class="sxs-lookup"><span data-stu-id="0ac60-103">CTransformOutputPin.CheckConnect method</span></span>

<span data-ttu-id="0ac60-104">El `CheckConnect` método determina si una conexión de PIN es adecuada.</span><span class="sxs-lookup"><span data-stu-id="0ac60-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ac60-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ac60-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="0ac60-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ac60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ac60-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="0ac60-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="0ac60-108">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="0ac60-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ac60-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ac60-109">Return value</span></span>

<span data-ttu-id="0ac60-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0ac60-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0ac60-111">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="0ac60-111">Possible values include the following.</span></span>



| <span data-ttu-id="0ac60-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0ac60-112">Return code</span></span>                                                                                  | <span data-ttu-id="0ac60-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ac60-113">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="0ac60-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0ac60-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0ac60-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="0ac60-115">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="0ac60-116"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="0ac60-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="0ac60-117">El PIN de entrada del filtro no está conectado.</span><span class="sxs-lookup"><span data-stu-id="0ac60-117">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0ac60-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ac60-118">Remarks</span></span>

<span data-ttu-id="0ac60-119">Este método invalida el método [**CBaseOutputPin:: CheckConnect**](cbaseoutputpin-checkconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="0ac60-119">This method overrides the [**CBaseOutputPin::CheckConnect**](cbaseoutputpin-checkconnect.md) method.</span></span> <span data-ttu-id="0ac60-120">Llama al método [**CTransformFilter:: CheckConnect**](ctransformfilter-checkconnect.md) del filtro, que devuelve s \_ OK en la clase base.</span><span class="sxs-lookup"><span data-stu-id="0ac60-120">It calls the filter's [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="0ac60-121">La clase derivada puede invalidar el método **CTransformFilter:: CheckConnect** para realizar comprobaciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="0ac60-121">The derived class can override the **CTransformFilter::CheckConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ac60-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ac60-122">Requirements</span></span>



| <span data-ttu-id="0ac60-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ac60-123">Requirement</span></span> | <span data-ttu-id="0ac60-124">Value</span><span class="sxs-lookup"><span data-stu-id="0ac60-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ac60-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ac60-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0ac60-126"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ac60-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0ac60-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0ac60-127">Library</span></span><br/> | <dl> <span data-ttu-id="0ac60-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0ac60-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




