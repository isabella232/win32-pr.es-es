---
description: El método Datasize controla \_ los mensajes de tamaño de WM.
ms.assetid: 21d867a4-4321-478a-9beb-5d3053569369
title: Método CBaseWindow. My size (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9020510030d3b3d4b30e066adfe67367618fb3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679181"
---
# <a name="cbasewindowonsize-method"></a><span data-ttu-id="b1666-103">CBaseWindow. alsize (método)</span><span class="sxs-lookup"><span data-stu-id="b1666-103">CBaseWindow.OnSize method</span></span>

<span data-ttu-id="b1666-104">El `OnSize` método controla \_ los mensajes de tamaño de WM.</span><span class="sxs-lookup"><span data-stu-id="b1666-104">The `OnSize` method handles WM\_SIZE messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1666-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1666-105">Syntax</span></span>


```C++
virtual BOOL OnSize(
   LONG Width,
   LONG Height
);
```



## <a name="parameters"></a><span data-ttu-id="b1666-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1666-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1666-107">*Width*</span><span class="sxs-lookup"><span data-stu-id="b1666-107">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="b1666-108">Ancho del área cliente, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="b1666-108">Width of the client area, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="b1666-109">*Height*</span><span class="sxs-lookup"><span data-stu-id="b1666-109">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="b1666-110">Alto del área cliente, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="b1666-110">Height of the client area, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1666-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1666-111">Return value</span></span>

<span data-ttu-id="b1666-112">Devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="b1666-112">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1666-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1666-113">Remarks</span></span>

<span data-ttu-id="b1666-114">Este método almacena el nuevo ancho y alto.</span><span class="sxs-lookup"><span data-stu-id="b1666-114">This method stores the new width and height.</span></span> <span data-ttu-id="b1666-115">Para recuperar estos valores, llame a los métodos [**CBaseWindow:: GetWindowHeight**](cbasewindow-getwindowheight.md) y [**CBaseWindow:: GetWindowWidth**](cbasewindow-getwindowwidth.md) .</span><span class="sxs-lookup"><span data-stu-id="b1666-115">To retrieve these values, call the [**CBaseWindow::GetWindowHeight**](cbasewindow-getwindowheight.md) and [**CBaseWindow::GetWindowWidth**](cbasewindow-getwindowwidth.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1666-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1666-116">Requirements</span></span>



| <span data-ttu-id="b1666-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1666-117">Requirement</span></span> | <span data-ttu-id="b1666-118">Value</span><span class="sxs-lookup"><span data-stu-id="b1666-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1666-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1666-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b1666-120"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1666-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b1666-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b1666-121">Library</span></span><br/> | <dl> <span data-ttu-id="b1666-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b1666-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1666-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1666-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1666-124">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="b1666-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




