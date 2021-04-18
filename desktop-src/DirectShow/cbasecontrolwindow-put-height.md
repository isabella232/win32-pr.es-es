---
description: El \_ método put height establece el alto de la ventana.
ms.assetid: 11026ee5-e83a-4d82-9069-a302d55a2d46
title: Método CBaseControlWindow.put_Height (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Height
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 798719c60b830caebee348032abce3e39a742e38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661148"
---
# <a name="cbasecontrolwindowput_height-method"></a><span data-ttu-id="94a4f-103">CBaseControlWindow. put ( \_ método de alto)</span><span class="sxs-lookup"><span data-stu-id="94a4f-103">CBaseControlWindow.put\_Height method</span></span>

<span data-ttu-id="94a4f-104">El `put_Height` método establece el alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="94a4f-104">The `put_Height` method sets the window height.</span></span>

## <a name="syntax"></a><span data-ttu-id="94a4f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94a4f-105">Syntax</span></span>


```C++
HRESULT put_Height(
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="94a4f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94a4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94a4f-107">*Height*</span><span class="sxs-lookup"><span data-stu-id="94a4f-107">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="94a4f-108">Nuevo alto de la ventana, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="94a4f-108">New window height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94a4f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94a4f-109">Return value</span></span>

<span data-ttu-id="94a4f-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="94a4f-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="94a4f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94a4f-111">Remarks</span></span>

<span data-ttu-id="94a4f-112">La ventana tiene una posición en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="94a4f-112">The window has a position on the desktop.</span></span> <span data-ttu-id="94a4f-113">Se expresa en píxeles por cuatro coordenadas (izquierda, superior, derecha e inferior).</span><span class="sxs-lookup"><span data-stu-id="94a4f-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="94a4f-114">Las interfaces automatizadas por OLE suelen expresar esta posición a la izquierda, la parte superior, el ancho y el alto. Esta es la Convención usada en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="94a4f-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="94a4f-115">Todas las coordenadas se expresan en píxeles y, al cambiar cualquier coordenada, la ventana se actualizará inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="94a4f-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="94a4f-116">Al establecer las coordenadas izquierda o superior, la ventana se mueve a la izquierda o hacia arriba, respectivamente; estas coordenadas no tienen ningún efecto en el ancho y el alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="94a4f-116">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="94a4f-117">Del mismo modo, establecer el ancho y el alto no afecta a las coordenadas izquierda y superior.</span><span class="sxs-lookup"><span data-stu-id="94a4f-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="94a4f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94a4f-118">Requirements</span></span>



| <span data-ttu-id="94a4f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="94a4f-119">Requirement</span></span> | <span data-ttu-id="94a4f-120">Value</span><span class="sxs-lookup"><span data-stu-id="94a4f-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94a4f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94a4f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="94a4f-122"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94a4f-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="94a4f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="94a4f-123">Library</span></span><br/> | <dl> <span data-ttu-id="94a4f-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="94a4f-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94a4f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="94a4f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94a4f-126">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="94a4f-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




