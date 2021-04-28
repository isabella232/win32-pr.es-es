---
description: 'Método CTransformFilter.CompleteConnect: el método CompleteConnect completa una conexión de pin.'
ms.assetid: b687d2ee-4aee-4fae-bc2f-23ee037d0e6d
title: Método CTransformFilter.CompleteConnect (Transfrm.h)
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
ms.openlocfilehash: d2251ba45c7a39ec9bf205fdd6643e02392e40e5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095173"
---
# <a name="ctransformfiltercompleteconnect-method"></a><span data-ttu-id="31e35-103">Método CTransformFilter.CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="31e35-103">CTransformFilter.CompleteConnect method</span></span>

<span data-ttu-id="31e35-104">El `CompleteConnect` método completa una conexión de pin.</span><span class="sxs-lookup"><span data-stu-id="31e35-104">The `CompleteConnect` method completes a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="31e35-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31e35-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="31e35-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31e35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31e35-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="31e35-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="31e35-108">Miembro del tipo [**enumerado \_ PIN DIRECTION,**](/windows/win32/api/strmif/ne-strmif-pin_direction) especificando qué pin en el filtro está realizando la conexión.</span><span class="sxs-lookup"><span data-stu-id="31e35-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="31e35-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="31e35-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="31e35-110">Puntero a la [**interfaz IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro pin en este intento de conexión.</span><span class="sxs-lookup"><span data-stu-id="31e35-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31e35-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31e35-111">Return value</span></span>

<span data-ttu-id="31e35-112">Devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="31e35-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="31e35-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="31e35-113">Remarks</span></span>

<span data-ttu-id="31e35-114">Los [**métodos CTransformInputPin::CompleteConnect**](ctransforminputpin-completeconnect.md) y [**CTransformOutputPin::CompleteConnect**](ctransformoutputpin-completeconnect.md) llaman a este método durante el proceso de conexión de pin.</span><span class="sxs-lookup"><span data-stu-id="31e35-114">The [**CTransformInputPin::CompleteConnect**](ctransforminputpin-completeconnect.md) and [**CTransformOutputPin::CompleteConnect**](ctransformoutputpin-completeconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="31e35-115">Este método no hace nada en la clase base, pero la clase derivada puede invalidarla.</span><span class="sxs-lookup"><span data-stu-id="31e35-115">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="31e35-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31e35-116">Requirements</span></span>



| <span data-ttu-id="31e35-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="31e35-117">Requirement</span></span> | <span data-ttu-id="31e35-118">Value</span><span class="sxs-lookup"><span data-stu-id="31e35-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31e35-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31e35-119">Header</span></span><br/>  | <dl> <span data-ttu-id="31e35-120"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="31e35-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="31e35-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31e35-121">Library</span></span><br/> | <dl> <span data-ttu-id="31e35-122"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="31e35-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31e35-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="31e35-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31e35-124">**CTransformFilter (clase)**</span><span class="sxs-lookup"><span data-stu-id="31e35-124">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




