---
description: El método CheckTargetRect determina si un rectángulo de destino es válido.
ms.assetid: a16e7faf-6421-4f78-bbb1-40d38f1a5525
title: Método CBaseControlVideo. CheckTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94f8d50aea58f556634e7f20b3880aecad72cc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690351"
---
# <a name="cbasecontrolvideochecktargetrect-method"></a><span data-ttu-id="bce45-103">CBaseControlVideo. CheckTargetRect, método</span><span class="sxs-lookup"><span data-stu-id="bce45-103">CBaseControlVideo.CheckTargetRect method</span></span>

<span data-ttu-id="bce45-104">El `CheckTargetRect` método determina si un rectángulo de destino es válido.</span><span class="sxs-lookup"><span data-stu-id="bce45-104">The `CheckTargetRect` method determines if a target rectangle is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="bce45-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bce45-105">Syntax</span></span>


```C++
virtual HRESULT CheckTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a><span data-ttu-id="bce45-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bce45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bce45-107">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="bce45-107">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="bce45-108">Puntero al rectángulo de destino que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="bce45-108">Pointer to the target rectangle to check.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bce45-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bce45-109">Return value</span></span>

<span data-ttu-id="bce45-110">Devuelve E \_ INVALIDARG si no es válido; en caso contrario, devuelve NoError (S \_ OK).</span><span class="sxs-lookup"><span data-stu-id="bce45-110">Returns E\_INVALIDARG if not valid; otherwise, returns NOERROR (S\_OK).</span></span>

## <a name="remarks"></a><span data-ttu-id="bce45-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bce45-111">Remarks</span></span>

<span data-ttu-id="bce45-112">Esta función miembro determina si el rectángulo de destino solicitado es válido.</span><span class="sxs-lookup"><span data-stu-id="bce45-112">This member function determines if the target rectangle requested is valid.</span></span> <span data-ttu-id="bce45-113">Dado que el rectángulo de destino especifica una posición en el cliente lógico de la ventana, las coordenadas pueden ser negativas, aunque el ancho y el alto totales no pueden ser cero ni un valor negativo.</span><span class="sxs-lookup"><span data-stu-id="bce45-113">Because the destination rectangle specifies a position in the logical client of the window, the coordinates can be negative, although the overall width and height cannot be zero or a negative value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bce45-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bce45-114">Requirements</span></span>



| <span data-ttu-id="bce45-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bce45-115">Requirement</span></span> | <span data-ttu-id="bce45-116">Value</span><span class="sxs-lookup"><span data-stu-id="bce45-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bce45-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bce45-117">Header</span></span><br/>  | <dl> <span data-ttu-id="bce45-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bce45-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bce45-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bce45-119">Library</span></span><br/> | <dl> <span data-ttu-id="bce45-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bce45-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bce45-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="bce45-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bce45-122">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="bce45-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




