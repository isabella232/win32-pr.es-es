---
description: El método CompleteConnect completa una conexión de PIN.
ms.assetid: b687d2ee-4aee-4fae-bc2f-23ee037d0e6d
title: Método CTransformFilter. CompleteConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 630950cf9b05c08412394bf9270f2369b3f3b94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660730"
---
# <a name="ctransformfiltercompleteconnect-method"></a><span data-ttu-id="4dccc-103">CTransformFilter. CompleteConnect, método</span><span class="sxs-lookup"><span data-stu-id="4dccc-103">CTransformFilter.CompleteConnect method</span></span>

<span data-ttu-id="4dccc-104">El `CompleteConnect` método completa una conexión de PIN.</span><span class="sxs-lookup"><span data-stu-id="4dccc-104">The `CompleteConnect` method completes a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dccc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4dccc-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="4dccc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4dccc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dccc-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="4dccc-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="4dccc-108">Miembro del tipo enumerado de [**\_ dirección del PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) , que especifica el PIN del filtro que realiza la conexión.</span><span class="sxs-lookup"><span data-stu-id="4dccc-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="4dccc-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="4dccc-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="4dccc-110">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro PIN en este intento de conexión.</span><span class="sxs-lookup"><span data-stu-id="4dccc-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dccc-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4dccc-111">Return value</span></span>

<span data-ttu-id="4dccc-112">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="4dccc-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dccc-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4dccc-113">Remarks</span></span>

<span data-ttu-id="4dccc-114">Los métodos [**CTransformInputPin:: CompleteConnect**](ctransforminputpin-completeconnect.md) y [**CTransformOutputPin:: CompleteConnect**](ctransformoutputpin-completeconnect.md) llaman a este método durante el proceso de conexión del PIN.</span><span class="sxs-lookup"><span data-stu-id="4dccc-114">The [**CTransformInputPin::CompleteConnect**](ctransforminputpin-completeconnect.md) and [**CTransformOutputPin::CompleteConnect**](ctransformoutputpin-completeconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="4dccc-115">Este método no hace nada en la clase base, pero la clase derivada puede invalidarlo.</span><span class="sxs-lookup"><span data-stu-id="4dccc-115">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dccc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4dccc-116">Requirements</span></span>



| <span data-ttu-id="4dccc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dccc-117">Requirement</span></span> | <span data-ttu-id="4dccc-118">Value</span><span class="sxs-lookup"><span data-stu-id="4dccc-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dccc-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4dccc-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4dccc-120"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4dccc-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4dccc-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4dccc-121">Library</span></span><br/> | <dl> <span data-ttu-id="4dccc-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4dccc-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dccc-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="4dccc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dccc-124">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="4dccc-124">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




