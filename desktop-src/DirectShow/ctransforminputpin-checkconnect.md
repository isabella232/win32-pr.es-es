---
description: El método CheckConnect determina si una conexión de PIN es adecuada.
ms.assetid: b8ace40d-31f5-49b0-a4cd-6ece0f883d96
title: Método CTransformInputPin. CheckConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e10c174a4e295576cfa9ce902faeac889f5a6a9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660688"
---
# <a name="ctransforminputpincheckconnect-method"></a><span data-ttu-id="54be6-103">CTransformInputPin. CheckConnect, método</span><span class="sxs-lookup"><span data-stu-id="54be6-103">CTransformInputPin.CheckConnect method</span></span>

<span data-ttu-id="54be6-104">El `CheckConnect` método determina si una conexión de PIN es adecuada.</span><span class="sxs-lookup"><span data-stu-id="54be6-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="54be6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54be6-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="54be6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54be6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54be6-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="54be6-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="54be6-108">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="54be6-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54be6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54be6-109">Return value</span></span>

<span data-ttu-id="54be6-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="54be6-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="54be6-111">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="54be6-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="54be6-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="54be6-112">Return code</span></span>                                                                                               | <span data-ttu-id="54be6-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="54be6-113">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="54be6-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="54be6-114"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="54be6-115">Correcto</span><span class="sxs-lookup"><span data-stu-id="54be6-115">Success</span></span><br/>             |
| <dl> <span data-ttu-id="54be6-116"><dt>**\_ \_ dirección no válida de VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="54be6-116"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="54be6-117">Dirección de PIN incorrecta</span><span class="sxs-lookup"><span data-stu-id="54be6-117">Wrong pin direction</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="54be6-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54be6-118">Remarks</span></span>

<span data-ttu-id="54be6-119">Este método invalida el método [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="54be6-119">This method overrides the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method.</span></span> <span data-ttu-id="54be6-120">Llama al método [**CTransformFilter:: CheckConnect**](ctransformfilter-checkconnect.md) del filtro, que devuelve s \_ OK en la clase base.</span><span class="sxs-lookup"><span data-stu-id="54be6-120">It calls the filter's [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="54be6-121">La clase derivada puede invalidar el método **CTransformFilter:: CheckConnect** para realizar comprobaciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="54be6-121">The derived class can override the **CTransformFilter::CheckConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="54be6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54be6-122">Requirements</span></span>



| <span data-ttu-id="54be6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="54be6-123">Requirement</span></span> | <span data-ttu-id="54be6-124">Value</span><span class="sxs-lookup"><span data-stu-id="54be6-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54be6-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54be6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="54be6-126"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="54be6-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="54be6-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="54be6-127">Library</span></span><br/> | <dl> <span data-ttu-id="54be6-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="54be6-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




