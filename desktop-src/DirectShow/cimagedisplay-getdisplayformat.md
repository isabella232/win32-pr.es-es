---
description: El método GetDisplayFormat recupera un formato de vídeo que describe el modo de presentación actual.
ms.assetid: 98134704-0453-4090-94de-d92cdf324538
title: Método CImageDisplay. GetDisplayFormat (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetDisplayFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 901d61f3597156853b0f2d6f93b43c3cf99ec5e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671396"
---
# <a name="cimagedisplaygetdisplayformat-method"></a><span data-ttu-id="38cba-103">CImageDisplay. GetDisplayFormat, método</span><span class="sxs-lookup"><span data-stu-id="38cba-103">CImageDisplay.GetDisplayFormat method</span></span>

<span data-ttu-id="38cba-104">El `GetDisplayFormat` método recupera un formato de vídeo que describe el modo de presentación actual.</span><span class="sxs-lookup"><span data-stu-id="38cba-104">The `GetDisplayFormat` method retrieves a video format that describes the current display mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="38cba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38cba-105">Syntax</span></span>


```C++
const VIDEOINFO* GetDisplayFormat();
```



## <a name="parameters"></a><span data-ttu-id="38cba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38cba-106">Parameters</span></span>

<span data-ttu-id="38cba-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="38cba-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="38cba-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38cba-108">Return value</span></span>

<span data-ttu-id="38cba-109">Devuelve un puntero a una estructura de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="38cba-109">Returns a pointer to a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="38cba-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38cba-110">Requirements</span></span>



| <span data-ttu-id="38cba-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="38cba-111">Requirement</span></span> | <span data-ttu-id="38cba-112">Value</span><span class="sxs-lookup"><span data-stu-id="38cba-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38cba-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38cba-113">Header</span></span><br/>  | <dl> <span data-ttu-id="38cba-114"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38cba-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="38cba-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="38cba-115">Library</span></span><br/> | <dl> <span data-ttu-id="38cba-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="38cba-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38cba-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="38cba-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38cba-118">**Clase CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="38cba-118">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




