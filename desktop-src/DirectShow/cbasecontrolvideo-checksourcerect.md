---
description: Determina si un rectángulo de origen es válido.
ms.assetid: 3fef107b-6f4c-4fab-91d3-6ab72dcc32be
title: Método CBaseControlVideo. CheckSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa219687dabcf9124662e3269d157fb0a163a6a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660529"
---
# <a name="cbasecontrolvideochecksourcerect-method"></a><span data-ttu-id="c8c83-103">CBaseControlVideo. CheckSourceRect, método</span><span class="sxs-lookup"><span data-stu-id="c8c83-103">CBaseControlVideo.CheckSourceRect method</span></span>

<span data-ttu-id="c8c83-104">Determina si un rectángulo de origen es válido.</span><span class="sxs-lookup"><span data-stu-id="c8c83-104">Determines if a source rectangle is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8c83-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8c83-105">Syntax</span></span>


```C++
virtual HRESULT CheckSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="c8c83-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8c83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8c83-107">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="c8c83-107">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="c8c83-108">Puntero al rectángulo de origen que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="c8c83-108">Pointer to the source rectangle to check.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8c83-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8c83-109">Return value</span></span>

<span data-ttu-id="c8c83-110">Devuelve E \_ INVALIDARG si no es válido; en caso contrario, devuelve NoError (S \_ OK).</span><span class="sxs-lookup"><span data-stu-id="c8c83-110">Returns E\_INVALIDARG if not valid; otherwise, returns NOERROR (S\_OK).</span></span>

## <a name="remarks"></a><span data-ttu-id="c8c83-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8c83-111">Remarks</span></span>

<span data-ttu-id="c8c83-112">Esta función miembro comprueba que el rectángulo de origen solicitado no supera el vídeo de origen disponible.</span><span class="sxs-lookup"><span data-stu-id="c8c83-112">This member function checks that the source rectangle requested does not exceed the available source video.</span></span> <span data-ttu-id="c8c83-113">Las coordenadas izquierda y superior no pueden ser negativas y el ancho y el alto no pueden superar la parte derecha e inferior del vídeo.</span><span class="sxs-lookup"><span data-stu-id="c8c83-113">The left and top coordinates cannot be negative, and the width and height cannot exceed the right and bottom of the video.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8c83-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8c83-114">Requirements</span></span>



| <span data-ttu-id="c8c83-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8c83-115">Requirement</span></span> | <span data-ttu-id="c8c83-116">Value</span><span class="sxs-lookup"><span data-stu-id="c8c83-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8c83-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8c83-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c8c83-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8c83-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c8c83-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c8c83-119">Library</span></span><br/> | <dl> <span data-ttu-id="c8c83-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c8c83-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8c83-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8c83-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8c83-122">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="c8c83-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




