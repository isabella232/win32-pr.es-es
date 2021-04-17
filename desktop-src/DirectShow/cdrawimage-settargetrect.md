---
description: El método SetTargetRect establece el rectángulo de destino.
ms.assetid: 033f8bae-e63d-4be0-8dd0-715cc1229392
title: Método CDrawImage. SetTargetRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4513b6aeda16d19476769290a6139f91b2fd1f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670733"
---
# <a name="cdrawimagesettargetrect-method"></a><span data-ttu-id="a487e-103">CDrawImage. SetTargetRect, método</span><span class="sxs-lookup"><span data-stu-id="a487e-103">CDrawImage.SetTargetRect method</span></span>

<span data-ttu-id="a487e-104">El `SetTargetRect` método establece el rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="a487e-104">The `SetTargetRect` method sets the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="a487e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a487e-105">Syntax</span></span>


```C++
void SetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a><span data-ttu-id="a487e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a487e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a487e-107">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="a487e-107">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="a487e-108">Puntero a una estructura **Rect** que define el nuevo rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="a487e-108">Pointer to a **RECT** structure that defines the new target rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a487e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a487e-109">Return value</span></span>

<span data-ttu-id="a487e-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a487e-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a487e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a487e-111">Remarks</span></span>

<span data-ttu-id="a487e-112">El filtro propietario debe llamar a este método si cambia el rectángulo de origen; por ejemplo, en respuesta a una llamada a [**IBasicVideo:: SetDestinationPosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setdestinationposition) .</span><span class="sxs-lookup"><span data-stu-id="a487e-112">The owning filter should call this method if the source rectangle changes; for example, in response to an [**IBasicVideo::SetDestinationPosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setdestinationposition) call.</span></span>

<span data-ttu-id="a487e-113">Antes de llamar a este método, valide el rectángulo dado en *pTargetRect* con respecto a la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a487e-113">Before calling this method, validate the rectangle given in *pTargetRect*, relative to the video window.</span></span>

## <a name="requirements"></a><span data-ttu-id="a487e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a487e-114">Requirements</span></span>



| <span data-ttu-id="a487e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a487e-115">Requirement</span></span> | <span data-ttu-id="a487e-116">Value</span><span class="sxs-lookup"><span data-stu-id="a487e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a487e-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a487e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a487e-118"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a487e-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a487e-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a487e-119">Library</span></span><br/> | <dl> <span data-ttu-id="a487e-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a487e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a487e-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a487e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a487e-122">**Clase CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="a487e-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




