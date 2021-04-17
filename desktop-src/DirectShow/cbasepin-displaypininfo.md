---
description: El método DisplayPinInfo realiza un seguimiento de una conexión de PIN durante la depuración.
ms.assetid: 3c1aa5ab-7f6b-4518-abf3-b5138f6267ee
title: Método CBasePin. DisplayPinInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea563ca07eaea6b6974a831726918866414a33b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671102"
---
# <a name="cbasepindisplaypininfo-method"></a><span data-ttu-id="57991-103">CBasePin. DisplayPinInfo, método</span><span class="sxs-lookup"><span data-stu-id="57991-103">CBasePin.DisplayPinInfo method</span></span>

<span data-ttu-id="57991-104">El `DisplayPinInfo` método realiza un seguimiento de una conexión de PIN durante la depuración.</span><span class="sxs-lookup"><span data-stu-id="57991-104">The `DisplayPinInfo` method traces a pin connection during debugging.</span></span>

## <a name="syntax"></a><span data-ttu-id="57991-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57991-105">Syntax</span></span>


```C++
void DisplayPinInfo(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="57991-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57991-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57991-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="57991-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="57991-108">Puntero al pin receptor.</span><span class="sxs-lookup"><span data-stu-id="57991-108">Pointer to the receiving pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57991-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57991-109">Return value</span></span>

<span data-ttu-id="57991-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="57991-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="57991-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57991-111">Remarks</span></span>

<span data-ttu-id="57991-112">En las compilaciones de depuración, este método llama a la función [**DbgLog**](dbglog.md) para realizar un seguimiento de un intento de conexión.</span><span class="sxs-lookup"><span data-stu-id="57991-112">In debug builds, this method calls the [**DbgLog**](dbglog.md) function to trace a connection attempt.</span></span> <span data-ttu-id="57991-113">En las compilaciones comerciales, este método no hace nada.</span><span class="sxs-lookup"><span data-stu-id="57991-113">In retail builds, this method does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="57991-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57991-114">Requirements</span></span>



| <span data-ttu-id="57991-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="57991-115">Requirement</span></span> | <span data-ttu-id="57991-116">Value</span><span class="sxs-lookup"><span data-stu-id="57991-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57991-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57991-117">Header</span></span><br/>  | <dl> <span data-ttu-id="57991-118"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57991-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="57991-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="57991-119">Library</span></span><br/> | <dl> <span data-ttu-id="57991-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="57991-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57991-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="57991-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57991-122">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="57991-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




