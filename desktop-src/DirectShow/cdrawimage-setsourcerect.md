---
description: El método SetSourceRect establece el rectángulo de origen.
ms.assetid: 982636fe-73ea-4f13-9f2b-7ae8df839ab1
title: Método CDrawImage. SetSourceRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64fb8729b694d38eac2d6321f92904292d99bd38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670508"
---
# <a name="cdrawimagesetsourcerect-method"></a><span data-ttu-id="5ce81-103">CDrawImage. SetSourceRect, método</span><span class="sxs-lookup"><span data-stu-id="5ce81-103">CDrawImage.SetSourceRect method</span></span>

<span data-ttu-id="5ce81-104">El `SetSourceRect` método establece el rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="5ce81-104">The `SetSourceRect` method sets the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ce81-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ce81-105">Syntax</span></span>


```C++
void SetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="5ce81-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ce81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ce81-107">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="5ce81-107">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="5ce81-108">Puntero a una estructura **Rect** que define el nuevo rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="5ce81-108">Pointer to a **RECT** structure that defines the new source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ce81-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ce81-109">Return value</span></span>

<span data-ttu-id="5ce81-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5ce81-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ce81-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ce81-111">Remarks</span></span>

<span data-ttu-id="5ce81-112">El filtro propietario debe llamar a este método si cambia el rectángulo de origen; por ejemplo, en respuesta a una llamada a [**IBasicVideo:: SetSourcePosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) .</span><span class="sxs-lookup"><span data-stu-id="5ce81-112">The owning filter should call this method if the source rectangle changes; for example, in response to an [**IBasicVideo::SetSourcePosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) call.</span></span>

<span data-ttu-id="5ce81-113">Valide el rectángulo proporcionado en *pSourceRect* antes de llamar a este método para asegurarse de que no se extiende más allá del tamaño de vídeo nativo.</span><span class="sxs-lookup"><span data-stu-id="5ce81-113">Validate the rectangle given in *pSourceRect* before calling this method, to make sure it does not extend beyond the native video size.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ce81-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ce81-114">Requirements</span></span>



| <span data-ttu-id="5ce81-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ce81-115">Requirement</span></span> | <span data-ttu-id="5ce81-116">Value</span><span class="sxs-lookup"><span data-stu-id="5ce81-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ce81-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ce81-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5ce81-118"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ce81-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5ce81-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5ce81-119">Library</span></span><br/> | <dl> <span data-ttu-id="5ce81-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5ce81-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ce81-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ce81-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ce81-122">**Clase CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="5ce81-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




