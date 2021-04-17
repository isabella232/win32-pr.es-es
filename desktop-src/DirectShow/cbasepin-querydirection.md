---
description: 'El método QueryDirection recupera la dirección del PIN (entrada o salida). Este método implementa el método IPin:: QueryDirection.'
ms.assetid: c28332dc-5ac4-4c89-98b4-281424f36ba9
title: Método CBasePin. QueryDirection (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryDirection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e2ebfaa3d12b5f582b4b67014280fa0a0d5299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670875"
---
# <a name="cbasepinquerydirection-method"></a><span data-ttu-id="b22af-104">CBasePin. QueryDirection, método</span><span class="sxs-lookup"><span data-stu-id="b22af-104">CBasePin.QueryDirection method</span></span>

<span data-ttu-id="b22af-105">El `QueryDirection` método recupera la dirección del PIN (entrada o salida).</span><span class="sxs-lookup"><span data-stu-id="b22af-105">The `QueryDirection` method retrieves the direction of the pin (input or output).</span></span> <span data-ttu-id="b22af-106">Este método implementa el método [**IPin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) .</span><span class="sxs-lookup"><span data-stu-id="b22af-106">This method implements the [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b22af-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b22af-107">Syntax</span></span>


```C++
HRESULT QueryDirection(
   PIN_DIRECTION *pPinDir
);
```



## <a name="parameters"></a><span data-ttu-id="b22af-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b22af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b22af-109">*pPinDir*</span><span class="sxs-lookup"><span data-stu-id="b22af-109">*pPinDir*</span></span> 
</dt> <dd>

<span data-ttu-id="b22af-110">Puntero a una variable que recibe un miembro del tipo enumerado de la [**\_ dirección del PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) .</span><span class="sxs-lookup"><span data-stu-id="b22af-110">Pointer to a variable that receives a member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b22af-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b22af-111">Return value</span></span>

<span data-ttu-id="b22af-112">Devuelve el \_ puntero S o E \_ .</span><span class="sxs-lookup"><span data-stu-id="b22af-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="b22af-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b22af-113">Requirements</span></span>



| <span data-ttu-id="b22af-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b22af-114">Requirement</span></span> | <span data-ttu-id="b22af-115">Value</span><span class="sxs-lookup"><span data-stu-id="b22af-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b22af-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b22af-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b22af-117"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b22af-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b22af-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b22af-118">Library</span></span><br/> | <dl> <span data-ttu-id="b22af-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b22af-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b22af-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="b22af-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b22af-121">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="b22af-121">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




