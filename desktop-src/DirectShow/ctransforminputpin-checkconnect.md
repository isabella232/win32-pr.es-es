---
description: 'Método CTransformInputPin.CheckConnect: el método CheckConnect determina si una conexión de pin es adecuada.'
ms.assetid: b8ace40d-31f5-49b0-a4cd-6ece0f883d96
title: Método CTransformInputPin.CheckConnect (Transfrm.h)
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
ms.openlocfilehash: 3e981254677c2e0a361a0a21f125f734ff1403db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095093"
---
# <a name="ctransforminputpincheckconnect-method"></a><span data-ttu-id="101f2-103">Método CTransformInputPin.CheckConnect</span><span class="sxs-lookup"><span data-stu-id="101f2-103">CTransformInputPin.CheckConnect method</span></span>

<span data-ttu-id="101f2-104">El `CheckConnect` método determina si una conexión de pin es adecuada.</span><span class="sxs-lookup"><span data-stu-id="101f2-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="101f2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="101f2-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="101f2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="101f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="101f2-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="101f2-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="101f2-108">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin de salida.</span><span class="sxs-lookup"><span data-stu-id="101f2-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="101f2-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="101f2-109">Return value</span></span>

<span data-ttu-id="101f2-110">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="101f2-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="101f2-111">Los valores posibles incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="101f2-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="101f2-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="101f2-112">Return code</span></span>                                                                                               | <span data-ttu-id="101f2-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="101f2-113">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="101f2-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="101f2-114"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="101f2-115">Correcto</span><span class="sxs-lookup"><span data-stu-id="101f2-115">Success</span></span><br/>             |
| <dl> <span data-ttu-id="101f2-116"><dt>**DIRECCIÓN NO VÁLIDA DE VFW \_ E \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="101f2-116"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="101f2-117">Dirección de anclado incorrecta</span><span class="sxs-lookup"><span data-stu-id="101f2-117">Wrong pin direction</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="101f2-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="101f2-118">Remarks</span></span>

<span data-ttu-id="101f2-119">Este método invalida el [**método CBasePin::CheckConnect.**](cbasepin-checkconnect.md)</span><span class="sxs-lookup"><span data-stu-id="101f2-119">This method overrides the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method.</span></span> <span data-ttu-id="101f2-120">Llama al método [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) del filtro, que devuelve S \_ OK en la clase base.</span><span class="sxs-lookup"><span data-stu-id="101f2-120">It calls the filter's [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="101f2-121">La clase derivada puede invalidar el **método CTransformFilter::CheckConnect** para realizar comprobaciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="101f2-121">The derived class can override the **CTransformFilter::CheckConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="101f2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="101f2-122">Requirements</span></span>



| <span data-ttu-id="101f2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="101f2-123">Requirement</span></span> | <span data-ttu-id="101f2-124">Value</span><span class="sxs-lookup"><span data-stu-id="101f2-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="101f2-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="101f2-125">Header</span></span><br/>  | <dl> <span data-ttu-id="101f2-126"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="101f2-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="101f2-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="101f2-127">Library</span></span><br/> | <dl> <span data-ttu-id="101f2-128"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="101f2-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




