---
description: El \_ método get Left recupera la coordenada de la ventana izquierda actual.
ms.assetid: 9ee71bd3-1ff5-4574-8dcd-5ba6490d9785
title: Método CBaseControlWindow.get_Left (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Left
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04f586cede24f8ff2017ae4004fc45c584a57f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671422"
---
# <a name="cbasecontrolwindowget_left-method"></a><span data-ttu-id="675d7-103">CBaseControlWindow. Get \_ left (método)</span><span class="sxs-lookup"><span data-stu-id="675d7-103">CBaseControlWindow.get\_Left method</span></span>

<span data-ttu-id="675d7-104">El `get_Left` método recupera la coordenada de la ventana izquierda actual.</span><span class="sxs-lookup"><span data-stu-id="675d7-104">The `get_Left` method retrieves the current left window coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="675d7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="675d7-105">Syntax</span></span>


```C++
HRESULT get_Left(
   long *pLeft
);
```



## <a name="parameters"></a><span data-ttu-id="675d7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="675d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="675d7-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="675d7-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="675d7-108">Puntero a la coordenada izquierda, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="675d7-108">Pointer to the left coordinate, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="675d7-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="675d7-109">Return value</span></span>

<span data-ttu-id="675d7-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="675d7-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="675d7-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="675d7-111">Remarks</span></span>

<span data-ttu-id="675d7-112">La ventana tiene una posición en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="675d7-112">The window has a position on the desktop.</span></span> <span data-ttu-id="675d7-113">Esta posición se expresa en píxeles por cuatro coordenadas (izquierda, superior, derecha e inferior).</span><span class="sxs-lookup"><span data-stu-id="675d7-113">This position is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="675d7-114">Las interfaces automatizadas por OLE suelen expresar esta posición a la izquierda, la parte superior, el ancho y el alto. Esta es la Convención usada en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="675d7-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="675d7-115">Todas las coordenadas se expresan en píxeles y, al cambiar cualquier coordenada, la ventana se actualizará inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="675d7-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="675d7-116">Al establecer las coordenadas izquierda o superior, la ventana se mueve a la izquierda y hacia arriba, respectivamente; estas coordenadas no tienen ningún efecto en el ancho y el alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="675d7-116">Setting the left or top coordinates moves the window left and up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="675d7-117">Del mismo modo, establecer el ancho y el alto no tiene ningún efecto en las coordenadas izquierda y superior.</span><span class="sxs-lookup"><span data-stu-id="675d7-117">Likewise, setting the width and height have no effect on the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="675d7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="675d7-118">Requirements</span></span>



| <span data-ttu-id="675d7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="675d7-119">Requirement</span></span> | <span data-ttu-id="675d7-120">Value</span><span class="sxs-lookup"><span data-stu-id="675d7-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="675d7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="675d7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="675d7-122"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="675d7-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="675d7-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="675d7-123">Library</span></span><br/> | <dl> <span data-ttu-id="675d7-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="675d7-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="675d7-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="675d7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="675d7-126">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="675d7-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




