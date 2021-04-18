---
description: El método GetVideoSize recupera el ancho y el alto del vídeo nativo.
ms.assetid: b3461a56-705b-465a-9cfc-e86fd52a07c5
title: Método CBaseControlVideo. GetVideoSize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b1df6fe781f036043728050354519dfa6e28d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661171"
---
# <a name="cbasecontrolvideogetvideosize-method"></a><span data-ttu-id="dc7bd-103">CBaseControlVideo. GetVideoSize, método</span><span class="sxs-lookup"><span data-stu-id="dc7bd-103">CBaseControlVideo.GetVideoSize method</span></span>

<span data-ttu-id="dc7bd-104">El `GetVideoSize` método recupera el ancho y el alto del vídeo nativo.</span><span class="sxs-lookup"><span data-stu-id="dc7bd-104">The `GetVideoSize` method retrieves the native video's width and height.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc7bd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc7bd-105">Syntax</span></span>


```C++
HRESULT GetVideoSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="dc7bd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc7bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc7bd-107">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="dc7bd-107">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="dc7bd-108">Puntero al ancho de vídeo.</span><span class="sxs-lookup"><span data-stu-id="dc7bd-108">Pointer to the video width.</span></span>

</dd> <dt>

<span data-ttu-id="dc7bd-109">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="dc7bd-109">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="dc7bd-110">Puntero al alto de vídeo.</span><span class="sxs-lookup"><span data-stu-id="dc7bd-110">Pointer to the video height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc7bd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc7bd-111">Return value</span></span>

<span data-ttu-id="dc7bd-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dc7bd-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc7bd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc7bd-113">Requirements</span></span>



| <span data-ttu-id="dc7bd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc7bd-114">Requirement</span></span> | <span data-ttu-id="dc7bd-115">Value</span><span class="sxs-lookup"><span data-stu-id="dc7bd-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc7bd-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dc7bd-116">Header</span></span><br/>  | <dl> <span data-ttu-id="dc7bd-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc7bd-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dc7bd-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dc7bd-118">Library</span></span><br/> | <dl> <span data-ttu-id="dc7bd-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="dc7bd-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc7bd-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc7bd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc7bd-121">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="dc7bd-121">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




