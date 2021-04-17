---
description: El \_ método get width recupera el ancho de la ventana actual.
ms.assetid: 8c5fbb0b-da80-4cfe-9c52-8ed4d9e52888
title: Método CBaseControlWindow.get_Width (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Width
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56e863b8add52e1b98714e13466a48e3d0d52bba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661204"
---
# <a name="cbasecontrolwindowget_width-method"></a><span data-ttu-id="98d0e-103">CBaseControlWindow. Get \_ width (método)</span><span class="sxs-lookup"><span data-stu-id="98d0e-103">CBaseControlWindow.get\_Width method</span></span>

<span data-ttu-id="98d0e-104">El `get_Width` método recupera el ancho de la ventana actual.</span><span class="sxs-lookup"><span data-stu-id="98d0e-104">The `get_Width` method retrieves the current window width.</span></span>

## <a name="syntax"></a><span data-ttu-id="98d0e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98d0e-105">Syntax</span></span>


```C++
HRESULT get_Width(
   long *pWidth
);
```



## <a name="parameters"></a><span data-ttu-id="98d0e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98d0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98d0e-107">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="98d0e-107">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="98d0e-108">Puntero en el ancho de la ventana, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="98d0e-108">Pointer to the window width, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98d0e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98d0e-109">Return value</span></span>

<span data-ttu-id="98d0e-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="98d0e-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98d0e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98d0e-111">Remarks</span></span>

<span data-ttu-id="98d0e-112">La ventana tiene una posición en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="98d0e-112">The window has a position on the desktop.</span></span> <span data-ttu-id="98d0e-113">Se expresa en píxeles por cuatro coordenadas (izquierda, superior, derecha e inferior).</span><span class="sxs-lookup"><span data-stu-id="98d0e-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="98d0e-114">Las interfaces automatizadas por OLE suelen expresar esta posición a la izquierda, la parte superior, el ancho y el alto. Esta es la Convención usada en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="98d0e-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="98d0e-115">Todas las coordenadas se expresan en píxeles y, al cambiar cualquier coordenada, la ventana se actualizará inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="98d0e-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="98d0e-116">Al establecer las coordenadas izquierda o superior, la ventana se mueve a la izquierda o hacia arriba, respectivamente; estas coordenadas no tienen ningún efecto en el ancho y el alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="98d0e-116">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="98d0e-117">Del mismo modo, establecer el ancho y el alto no afecta a las coordenadas izquierda y superior.</span><span class="sxs-lookup"><span data-stu-id="98d0e-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="98d0e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98d0e-118">Requirements</span></span>



| <span data-ttu-id="98d0e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="98d0e-119">Requirement</span></span> | <span data-ttu-id="98d0e-120">Value</span><span class="sxs-lookup"><span data-stu-id="98d0e-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98d0e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98d0e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="98d0e-122"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98d0e-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="98d0e-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98d0e-123">Library</span></span><br/> | <dl> <span data-ttu-id="98d0e-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="98d0e-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98d0e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="98d0e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98d0e-126">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="98d0e-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




