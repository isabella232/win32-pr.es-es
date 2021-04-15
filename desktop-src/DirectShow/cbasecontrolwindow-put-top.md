---
description: El \_ método put Top establece la coordenada superior de la ventana.
ms.assetid: cd39807f-363d-4b5b-8279-9dfb992dca10
title: Método CBaseControlWindow.put_Top (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Top
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fdbce19c3caf4129b1f224a740b27209b855a1f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661346"
---
# <a name="cbasecontrolwindowput_top-method"></a><span data-ttu-id="50896-103">CBaseControlWindow. put \_ Top (método)</span><span class="sxs-lookup"><span data-stu-id="50896-103">CBaseControlWindow.put\_Top method</span></span>

<span data-ttu-id="50896-104">El `put_Top` método establece la coordenada superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="50896-104">The `put_Top` method sets the top window coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="50896-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50896-105">Syntax</span></span>


```C++
HRESULT put_Top(
   long Top
);
```



## <a name="parameters"></a><span data-ttu-id="50896-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50896-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50896-107">*Top* (Principales)</span><span class="sxs-lookup"><span data-stu-id="50896-107">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="50896-108">Nueva coordenada superior, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="50896-108">New top coordinate, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50896-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50896-109">Return value</span></span>

<span data-ttu-id="50896-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="50896-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50896-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50896-111">Remarks</span></span>

<span data-ttu-id="50896-112">La ventana tiene una posición en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="50896-112">The window has a position on the desktop.</span></span> <span data-ttu-id="50896-113">Se expresa en píxeles por cuatro coordenadas (izquierda, superior, derecha e inferior).</span><span class="sxs-lookup"><span data-stu-id="50896-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="50896-114">Las interfaces automatizadas por OLE suelen expresar esta posición a la izquierda, la parte superior, el ancho y el alto. Esta es la Convención usada en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="50896-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="50896-115">Todas las coordenadas se expresan en píxeles y, al cambiar cualquier coordenada, la ventana se actualizará inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="50896-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="50896-116">Al establecer las coordenadas izquierda o superior, la ventana se mueve a la izquierda o hacia arriba, respectivamente; estas coordenadas no tienen ningún efecto en el ancho y el alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="50896-116">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="50896-117">Del mismo modo, establecer el ancho y el alto no afecta a las coordenadas izquierda y superior.</span><span class="sxs-lookup"><span data-stu-id="50896-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="50896-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50896-118">Requirements</span></span>



| <span data-ttu-id="50896-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="50896-119">Requirement</span></span> | <span data-ttu-id="50896-120">Value</span><span class="sxs-lookup"><span data-stu-id="50896-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50896-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50896-121">Header</span></span><br/>  | <dl> <span data-ttu-id="50896-122"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50896-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="50896-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="50896-123">Library</span></span><br/> | <dl> <span data-ttu-id="50896-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="50896-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50896-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="50896-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50896-126">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="50896-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




