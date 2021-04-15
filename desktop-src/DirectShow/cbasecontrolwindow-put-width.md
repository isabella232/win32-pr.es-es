---
description: El \_ método put width establece el ancho de la ventana.
ms.assetid: eb5ad1c2-ba39-4c06-84d2-6708dc8796d8
title: Método CBaseControlWindow.put_Width (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Width
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5235e2b842b26f3f05c31c9f19a16c7630c80c13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661342"
---
# <a name="cbasecontrolwindowput_width-method"></a><span data-ttu-id="69c59-103">CBaseControlWindow. put \_ width (método)</span><span class="sxs-lookup"><span data-stu-id="69c59-103">CBaseControlWindow.put\_Width method</span></span>

<span data-ttu-id="69c59-104">El `put_Width` método establece el ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="69c59-104">The `put_Width` method sets the window width.</span></span>

## <a name="syntax"></a><span data-ttu-id="69c59-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69c59-105">Syntax</span></span>


```C++
HRESULT put_Width(
   long Width
);
```



## <a name="parameters"></a><span data-ttu-id="69c59-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69c59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69c59-107">*Width*</span><span class="sxs-lookup"><span data-stu-id="69c59-107">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="69c59-108">Nuevo ancho de la ventana, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="69c59-108">New window width, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69c59-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69c59-109">Return value</span></span>

<span data-ttu-id="69c59-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="69c59-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="69c59-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69c59-111">Remarks</span></span>

<span data-ttu-id="69c59-112">La ventana tiene una posición en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="69c59-112">The window has a position on the desktop.</span></span> <span data-ttu-id="69c59-113">Se expresa en píxeles por cuatro coordenadas (izquierda, superior, derecha e inferior).</span><span class="sxs-lookup"><span data-stu-id="69c59-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="69c59-114">Las interfaces automatizadas por OLE suelen expresar esta posición a la izquierda, la parte superior, el ancho y el alto. Esta es la Convención usada en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="69c59-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="69c59-115">Todas las coordenadas se expresan en píxeles y, al cambiar cualquier coordenada, la ventana se actualizará inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="69c59-115">All coordinates are expressed in pixels and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="69c59-116">Al establecer las coordenadas izquierda o superior, la ventana se desplaza hacia la izquierda o hacia arriba respectivamente; estas coordenadas no tienen ningún efecto en el ancho y el alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="69c59-116">Setting the left or top coordinates moves the window left or up respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="69c59-117">Del mismo modo, establecer el ancho y el alto no afecta a las coordenadas izquierda y superior.</span><span class="sxs-lookup"><span data-stu-id="69c59-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="69c59-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69c59-118">Requirements</span></span>



| <span data-ttu-id="69c59-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="69c59-119">Requirement</span></span> | <span data-ttu-id="69c59-120">Value</span><span class="sxs-lookup"><span data-stu-id="69c59-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69c59-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69c59-121">Header</span></span><br/>  | <dl> <span data-ttu-id="69c59-122"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69c59-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="69c59-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="69c59-123">Library</span></span><br/> | <dl> <span data-ttu-id="69c59-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="69c59-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69c59-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="69c59-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69c59-126">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="69c59-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




