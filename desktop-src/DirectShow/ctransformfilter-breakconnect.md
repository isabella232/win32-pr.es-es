---
description: El método BreakConnect libera un código PIN de una conexión.
ms.assetid: cc384786-9cba-4f68-9c60-740205b35661
title: Método CTransformFilter. BreakConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec60322a4782d84e84dc2030b69f6c385783e98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660303"
---
# <a name="ctransformfilterbreakconnect-method"></a><span data-ttu-id="9ca5d-103">CTransformFilter. BreakConnect, método</span><span class="sxs-lookup"><span data-stu-id="9ca5d-103">CTransformFilter.BreakConnect method</span></span>

<span data-ttu-id="9ca5d-104">El `BreakConnect` método libera un código PIN de una conexión.</span><span class="sxs-lookup"><span data-stu-id="9ca5d-104">The `BreakConnect` method releases a pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ca5d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ca5d-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect(
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a><span data-ttu-id="9ca5d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ca5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ca5d-107">*dir*</span><span class="sxs-lookup"><span data-stu-id="9ca5d-107">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="9ca5d-108">Miembro del tipo enumerado de [**\_ dirección del PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) , que especifica qué conexión de PIN se interrumpió (entrada o salida).</span><span class="sxs-lookup"><span data-stu-id="9ca5d-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin connection was broken (input or output).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ca5d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ca5d-109">Return value</span></span>

<span data-ttu-id="9ca5d-110">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="9ca5d-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ca5d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ca5d-111">Remarks</span></span>

<span data-ttu-id="9ca5d-112">Los métodos [**CTransformInputPin:: BreakConnect**](ctransforminputpin-breakconnect.md) y [**CTransformOutputPin:: BreakConnect**](ctransformoutputpin-breakconnect.md) llaman a este método cuando se interrumpe una conexión de PIN.</span><span class="sxs-lookup"><span data-stu-id="9ca5d-112">The [**CTransformInputPin::BreakConnect**](ctransforminputpin-breakconnect.md) and [**CTransformOutputPin::BreakConnect**](ctransformoutputpin-breakconnect.md) methods call this method when a pin connection is broken.</span></span> <span data-ttu-id="9ca5d-113">Este método no hace nada en la clase base.</span><span class="sxs-lookup"><span data-stu-id="9ca5d-113">This method does nothing in the base class.</span></span> <span data-ttu-id="9ca5d-114">Si invalida el método [**CheckConnect**](ctransformfilter-checkconnect.md) , Invalide este método para liberar los recursos obtenidos en el método **CheckConnect** , incluidos los punteros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="9ca5d-114">If you override the [**CheckConnect**](ctransformfilter-checkconnect.md) method, override this method to release any resources obtained in the **CheckConnect** method, including interface pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ca5d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ca5d-115">Requirements</span></span>



| <span data-ttu-id="9ca5d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ca5d-116">Requirement</span></span> | <span data-ttu-id="9ca5d-117">Value</span><span class="sxs-lookup"><span data-stu-id="9ca5d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ca5d-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ca5d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9ca5d-119"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ca5d-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9ca5d-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9ca5d-120">Library</span></span><br/> | <dl> <span data-ttu-id="9ca5d-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9ca5d-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ca5d-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ca5d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ca5d-123">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="9ca5d-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




