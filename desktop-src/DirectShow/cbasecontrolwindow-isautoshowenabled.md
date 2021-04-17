---
description: El método IsAutoShowEnabled recupera información sobre si la ventana de vídeo aparece automáticamente cuando el filtro de representación se detiene o se ejecuta.
ms.assetid: 769e3023-a515-4b80-a979-2e4fa9612e65
title: Método CBaseControlWindow. IsAutoShowEnabled (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsAutoShowEnabled
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c4b4a894593cb3be26a1034098cd2a0cdacf926
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660737"
---
# <a name="cbasecontrolwindowisautoshowenabled-method"></a><span data-ttu-id="757d7-103">CBaseControlWindow. IsAutoShowEnabled, método</span><span class="sxs-lookup"><span data-stu-id="757d7-103">CBaseControlWindow.IsAutoShowEnabled method</span></span>

<span data-ttu-id="757d7-104">El `IsAutoShowEnabled` método recupera información sobre si la ventana de vídeo aparece automáticamente cuando el filtro de representación se detiene o se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="757d7-104">The `IsAutoShowEnabled` method retrieves information about whether the video window automatically appears when the rendering filter pauses or runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="757d7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="757d7-105">Syntax</span></span>


```C++
BOOL IsAutoShowEnabled();
```



## <a name="parameters"></a><span data-ttu-id="757d7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="757d7-106">Parameters</span></span>

<span data-ttu-id="757d7-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="757d7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="757d7-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="757d7-108">Return value</span></span>

<span data-ttu-id="757d7-109">Devuelve **true** si el miembro **m \_ bAutoShow** se establece en 1 o **false** si se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="757d7-109">Returns **TRUE** if the **m\_bAutoShow** member is set to  1 or **FALSE** if it is set to 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="757d7-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="757d7-110">Remarks</span></span>

<span data-ttu-id="757d7-111">Si el miembro **m \_ bAutoShow** se establece en 1 en una ventana de vídeo que está oculta, la ventana se vuelve visible cuando el filtro se pausa o se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="757d7-111">If the **m\_bAutoShow** member is set to  1 on a video window that is hidden, the window becomes visible when the filter pauses or runs.</span></span> <span data-ttu-id="757d7-112">Si este miembro se establece en 0, la ventana solo aparecerá si se usa la función miembro [**CBaseControlWindow::p UT \_ visible**](cbasecontrolwindow-put-visible.md) o [**CBaseControlWindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) con los parámetros adecuados.</span><span class="sxs-lookup"><span data-stu-id="757d7-112">If this member is set to 0, the window will appear only if you use the [**CBaseControlWindow::put\_Visible**](cbasecontrolwindow-put-visible.md) or [**CBaseControlWindow::put\_WindowState**](cbasecontrolwindow-put-windowstate.md) member function with the appropriate parameters.</span></span>

<span data-ttu-id="757d7-113">Esta función miembro recupera la configuración del miembro **m \_ bAutoShow** y tiene el mismo resultado que usar el método [**IVideoWindow:: get \_ Autoshow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) .</span><span class="sxs-lookup"><span data-stu-id="757d7-113">This member function retrieves the **m\_bAutoShow** member setting and has the same result as using the [**IVideoWindow::get\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="757d7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="757d7-114">Requirements</span></span>



| <span data-ttu-id="757d7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="757d7-115">Requirement</span></span> | <span data-ttu-id="757d7-116">Value</span><span class="sxs-lookup"><span data-stu-id="757d7-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="757d7-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="757d7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="757d7-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="757d7-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="757d7-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="757d7-119">Library</span></span><br/> | <dl> <span data-ttu-id="757d7-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="757d7-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="757d7-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="757d7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="757d7-122">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="757d7-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




