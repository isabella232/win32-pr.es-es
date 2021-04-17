---
description: El \_ método get Top recupera la coordenada superior de la ventana.
ms.assetid: 1e7910bd-e38e-4586-9dd6-701f69c0f6e7
title: Método CBaseControlWindow.get_Top (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Top
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9861d930cdb2d93e5e0b73ffad625885c082cb6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661206"
---
# <a name="cbasecontrolwindowget_top-method"></a><span data-ttu-id="cd3ce-103">CBaseControlWindow. Get \_ Top (método)</span><span class="sxs-lookup"><span data-stu-id="cd3ce-103">CBaseControlWindow.get\_Top method</span></span>

<span data-ttu-id="cd3ce-104">El `get_Top` método recupera la coordenada superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="cd3ce-104">The `get_Top` method retrieves the top window coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd3ce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd3ce-105">Syntax</span></span>


```C++
HRESULT get_Top(
   long *pTop
);
```



## <a name="parameters"></a><span data-ttu-id="cd3ce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd3ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd3ce-107">*pTop*</span><span class="sxs-lookup"><span data-stu-id="cd3ce-107">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="cd3ce-108">Puntero en la coordenada superior, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="cd3ce-108">Pointer to the top coordinate, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd3ce-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd3ce-109">Return value</span></span>

<span data-ttu-id="cd3ce-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cd3ce-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd3ce-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd3ce-111">Remarks</span></span>

<span data-ttu-id="cd3ce-112">La ventana tiene una posición en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="cd3ce-112">The window has a position on the desktop.</span></span> <span data-ttu-id="cd3ce-113">Se expresa en píxeles por cuatro coordenadas (izquierda, superior, derecha e inferior).</span><span class="sxs-lookup"><span data-stu-id="cd3ce-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="cd3ce-114">Las interfaces automatizadas por OLE suelen expresar esta posición a la izquierda, la parte superior, el ancho y el alto. Esta es la Convención usada en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="cd3ce-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="cd3ce-115">Todas las coordenadas se expresan en píxeles y, al cambiar cualquier coordenada, la ventana se actualizará inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="cd3ce-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="cd3ce-116">Al establecer las coordenadas izquierda o superior, la ventana se mueve a la izquierda o hacia arriba, respectivamente; estas coordenadas no tienen ningún efecto en el ancho y el alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="cd3ce-116">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="cd3ce-117">Del mismo modo, establecer el ancho y el alto no afecta a las coordenadas izquierda y superior.</span><span class="sxs-lookup"><span data-stu-id="cd3ce-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd3ce-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd3ce-118">Requirements</span></span>



| <span data-ttu-id="cd3ce-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd3ce-119">Requirement</span></span> | <span data-ttu-id="cd3ce-120">Value</span><span class="sxs-lookup"><span data-stu-id="cd3ce-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd3ce-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd3ce-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cd3ce-122"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd3ce-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cd3ce-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cd3ce-123">Library</span></span><br/> | <dl> <span data-ttu-id="cd3ce-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="cd3ce-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd3ce-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd3ce-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd3ce-126">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="cd3ce-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




