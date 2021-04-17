---
description: El \_ método get height recupera el alto de la ventana actual.
ms.assetid: 841c7d5d-f633-41fb-9cde-6126cd1cab9b
title: Método CBaseControlWindow.get_Height (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Height
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bed7beaac064ce9d97b9c93264eab8d56b27c9df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660446"
---
# <a name="cbasecontrolwindowget_height-method"></a><span data-ttu-id="0f545-103">CBaseControlWindow. get ( \_ método de alto)</span><span class="sxs-lookup"><span data-stu-id="0f545-103">CBaseControlWindow.get\_Height method</span></span>

<span data-ttu-id="0f545-104">El `get_Height` método recupera el alto de la ventana actual.</span><span class="sxs-lookup"><span data-stu-id="0f545-104">The `get_Height` method retrieves the current window height.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f545-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f545-105">Syntax</span></span>


```C++
HRESULT get_Height(
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="0f545-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f545-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f545-107">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="0f545-107">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="0f545-108">Puntero al alto de la ventana actual, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="0f545-108">Pointer to the current window height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f545-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f545-109">Return value</span></span>

<span data-ttu-id="0f545-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="0f545-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0f545-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0f545-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f545-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f545-112">Remarks</span></span>

<span data-ttu-id="0f545-113">La ventana tiene una posición en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="0f545-113">The window has a position on the desktop.</span></span> <span data-ttu-id="0f545-114">Se expresa en píxeles por cuatro coordenadas (izquierda, superior, derecha e inferior).</span><span class="sxs-lookup"><span data-stu-id="0f545-114">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="0f545-115">Las interfaces automatizadas por OLE suelen expresar esta posición a la izquierda, la parte superior, el ancho y el alto. Esta es la Convención usada en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0f545-115">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="0f545-116">Todas las coordenadas se expresan en píxeles y, al cambiar cualquier coordenada, la ventana se actualizará inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="0f545-116">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="0f545-117">Al establecer las coordenadas izquierda o superior, la ventana se mueve a la izquierda o hacia arriba, respectivamente; estas coordenadas no tienen ningún efecto en el ancho y el alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="0f545-117">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="0f545-118">Del mismo modo, establecer el ancho y el alto no afecta a las coordenadas izquierda y superior.</span><span class="sxs-lookup"><span data-stu-id="0f545-118">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f545-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f545-119">Requirements</span></span>



| <span data-ttu-id="0f545-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f545-120">Requirement</span></span> | <span data-ttu-id="0f545-121">Value</span><span class="sxs-lookup"><span data-stu-id="0f545-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f545-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f545-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0f545-123"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f545-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0f545-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0f545-124">Library</span></span><br/> | <dl> <span data-ttu-id="0f545-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0f545-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f545-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f545-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f545-127">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="0f545-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




