---
description: 'Método CTransformOutputPin.CheckConnect: el método CheckConnect determina si una conexión de pin es adecuada.'
ms.assetid: 3dae5c6d-720e-4445-b601-3bdfe32f4c21
title: Método CTransformOutputPin.CheckConnect (Transfrm.h)
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
ms.openlocfilehash: 190acd2fbab5206b114b57719d350e3ad5eac0c2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094953"
---
# <a name="ctransformoutputpincheckconnect-method"></a><span data-ttu-id="c58a0-103">Método CTransformOutputPin.CheckConnect</span><span class="sxs-lookup"><span data-stu-id="c58a0-103">CTransformOutputPin.CheckConnect method</span></span>

<span data-ttu-id="c58a0-104">El `CheckConnect` método determina si una conexión de pin es adecuada.</span><span class="sxs-lookup"><span data-stu-id="c58a0-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="c58a0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c58a0-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="c58a0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c58a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c58a0-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="c58a0-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="c58a0-108">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin de salida.</span><span class="sxs-lookup"><span data-stu-id="c58a0-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c58a0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c58a0-109">Return value</span></span>

<span data-ttu-id="c58a0-110">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="c58a0-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c58a0-111">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="c58a0-111">Possible values include the following.</span></span>



| <span data-ttu-id="c58a0-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c58a0-112">Return code</span></span>                                                                                  | <span data-ttu-id="c58a0-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="c58a0-113">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="c58a0-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c58a0-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c58a0-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="c58a0-115">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="c58a0-116"><dt>**E \_ UNEXPECTED**</dt></span><span class="sxs-lookup"><span data-stu-id="c58a0-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="c58a0-117">El pin de entrada del filtro no está conectado.</span><span class="sxs-lookup"><span data-stu-id="c58a0-117">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c58a0-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c58a0-118">Remarks</span></span>

<span data-ttu-id="c58a0-119">Este método invalida el [**método CBaseOutputPin::CheckConnect.**](cbaseoutputpin-checkconnect.md)</span><span class="sxs-lookup"><span data-stu-id="c58a0-119">This method overrides the [**CBaseOutputPin::CheckConnect**](cbaseoutputpin-checkconnect.md) method.</span></span> <span data-ttu-id="c58a0-120">Llama al método [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) del filtro, que devuelve S \_ OK en la clase base.</span><span class="sxs-lookup"><span data-stu-id="c58a0-120">It calls the filter's [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="c58a0-121">La clase derivada puede invalidar el **método CTransformFilter::CheckConnect** para realizar comprobaciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="c58a0-121">The derived class can override the **CTransformFilter::CheckConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="c58a0-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c58a0-122">Requirements</span></span>



| <span data-ttu-id="c58a0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c58a0-123">Requirement</span></span> | <span data-ttu-id="c58a0-124">Value</span><span class="sxs-lookup"><span data-stu-id="c58a0-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c58a0-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c58a0-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c58a0-126"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c58a0-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c58a0-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c58a0-127">Library</span></span><br/> | <dl> <span data-ttu-id="c58a0-128"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c58a0-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




