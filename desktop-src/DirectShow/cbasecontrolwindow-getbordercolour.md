---
description: El método GetBorderColour recupera el color del borde de la ventana actual, m \_ BorderColour.
ms.assetid: 5cd9b834-5438-475e-9671-ee9917f9a485
title: Método CBaseControlWindow. GetBorderColour (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetBorderColour
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ba6e1be9babf96d03235c49d9cde0f11cae1b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660739"
---
# <a name="cbasecontrolwindowgetbordercolour-method"></a><span data-ttu-id="1636e-103">CBaseControlWindow. GetBorderColour, método</span><span class="sxs-lookup"><span data-stu-id="1636e-103">CBaseControlWindow.GetBorderColour method</span></span>

<span data-ttu-id="1636e-104">El `GetBorderColour` método recupera el color del borde de la ventana actual, **m \_ BorderColour**.</span><span class="sxs-lookup"><span data-stu-id="1636e-104">The `GetBorderColour` method retrieves the current window border color, **m\_BorderColour**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1636e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1636e-105">Syntax</span></span>


```C++
COLORREF GetBorderColour();
```



## <a name="parameters"></a><span data-ttu-id="1636e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1636e-106">Parameters</span></span>

<span data-ttu-id="1636e-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1636e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1636e-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1636e-108">Return value</span></span>

<span data-ttu-id="1636e-109">Devuelve el color del borde.</span><span class="sxs-lookup"><span data-stu-id="1636e-109">Returns the color of the border.</span></span>

## <a name="remarks"></a><span data-ttu-id="1636e-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1636e-110">Remarks</span></span>

<span data-ttu-id="1636e-111">Una aplicación puede establecer un rectángulo de destino para mostrar el vídeo.</span><span class="sxs-lookup"><span data-stu-id="1636e-111">An application can set a destination rectangle to display the video.</span></span> <span data-ttu-id="1636e-112">Este rectángulo debe ser relativo al área cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="1636e-112">This rectangle should be relative to the client area for the window.</span></span> <span data-ttu-id="1636e-113">Si esto se hace (el valor predeterminado es pintar siempre toda la ventana), hay un área que rodea el vídeo; es decir, el borde.</span><span class="sxs-lookup"><span data-stu-id="1636e-113">If this is done (the default is to always paint the entire window), there is an area that surrounds the video; that is, the border.</span></span> <span data-ttu-id="1636e-114">El color del borde se puede establecer a través de la función miembro [**CBaseControlWindow::p UT \_ BorderColor**](cbasecontrolwindow-put-bordercolor.md) .</span><span class="sxs-lookup"><span data-stu-id="1636e-114">The border color can be set through the [**CBaseControlWindow::put\_BorderColor**](cbasecontrolwindow-put-bordercolor.md) member function.</span></span> <span data-ttu-id="1636e-115">Esta propiedad afecta al color del borde.</span><span class="sxs-lookup"><span data-stu-id="1636e-115">This property affects the color of the border.</span></span> <span data-ttu-id="1636e-116">Use esta función miembro en lugar de [**CBaseControlWindow:: get \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md), a menos que esté llamando a esto externamente a través del método [**IVideoWindow:: get \_ BorderColor**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) .</span><span class="sxs-lookup"><span data-stu-id="1636e-116">Use this member function instead of [**CBaseControlWindow::get\_BorderColor**](cbasecontrolwindow-get-bordercolor.md), unless you are calling this externally through the [**IVideoWindow::get\_BorderColor**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1636e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1636e-117">Requirements</span></span>



| <span data-ttu-id="1636e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1636e-118">Requirement</span></span> | <span data-ttu-id="1636e-119">Value</span><span class="sxs-lookup"><span data-stu-id="1636e-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1636e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1636e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="1636e-121"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1636e-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1636e-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1636e-122">Library</span></span><br/> | <dl> <span data-ttu-id="1636e-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1636e-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1636e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="1636e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1636e-125">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="1636e-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




