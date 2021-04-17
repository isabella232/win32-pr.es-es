---
description: El \_ método debordercolor de put cambia el color del borde.
ms.assetid: bb19d338-7fd1-448c-be94-1c71d4a9a330
title: Método CBaseControlWindow.put_BorderColor (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54db6de704f2ee0fde1a5087e83df4b362a57959
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660628"
---
# <a name="cbasecontrolwindowput_bordercolor-method"></a><span data-ttu-id="825d3-103">Método BorderColor CBaseControlWindow. put \_</span><span class="sxs-lookup"><span data-stu-id="825d3-103">CBaseControlWindow.put\_BorderColor method</span></span>

<span data-ttu-id="825d3-104">El `put_BorderColor` método cambia el color del borde.</span><span class="sxs-lookup"><span data-stu-id="825d3-104">The `put_BorderColor` method changes the border color.</span></span>

## <a name="syntax"></a><span data-ttu-id="825d3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="825d3-105">Syntax</span></span>


```C++
HRESULT put_BorderColor(
   long Color
);
```



## <a name="parameters"></a><span data-ttu-id="825d3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="825d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="825d3-107">*Color*</span><span class="sxs-lookup"><span data-stu-id="825d3-107">*Color*</span></span> 
</dt> <dd>

<span data-ttu-id="825d3-108">Nuevo color del borde.</span><span class="sxs-lookup"><span data-stu-id="825d3-108">New border color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="825d3-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="825d3-109">Return value</span></span>

<span data-ttu-id="825d3-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="825d3-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="825d3-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="825d3-111">Remarks</span></span>

<span data-ttu-id="825d3-112">Una aplicación puede establecer un rectángulo de destino en el que se debe mostrar el vídeo.</span><span class="sxs-lookup"><span data-stu-id="825d3-112">An application can establish a destination rectangle in which the video should be displayed.</span></span> <span data-ttu-id="825d3-113">Este rectángulo es relativo al área cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="825d3-113">This rectangle is relative to the client area for the window.</span></span> <span data-ttu-id="825d3-114">Si esto se hace (el valor predeterminado es pintar siempre toda la ventana), hay un borde que rodea el vídeo.</span><span class="sxs-lookup"><span data-stu-id="825d3-114">If this is done (the default is to always paint the entire window), there is a border surrounding the video.</span></span> <span data-ttu-id="825d3-115">Esta propiedad afecta al color utilizado por el borde.</span><span class="sxs-lookup"><span data-stu-id="825d3-115">This property affects the color used by the border.</span></span> <span data-ttu-id="825d3-116">Aunque el parámetro se especifica como un tipo **Long** , en realidad es un valor de **COLORREF** .</span><span class="sxs-lookup"><span data-stu-id="825d3-116">Although the parameter is specified as a **LONG** type, it is actually a **COLORREF** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="825d3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="825d3-117">Requirements</span></span>



| <span data-ttu-id="825d3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="825d3-118">Requirement</span></span> | <span data-ttu-id="825d3-119">Value</span><span class="sxs-lookup"><span data-stu-id="825d3-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="825d3-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="825d3-120">Header</span></span><br/>  | <dl> <span data-ttu-id="825d3-121"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="825d3-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="825d3-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="825d3-122">Library</span></span><br/> | <dl> <span data-ttu-id="825d3-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="825d3-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="825d3-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="825d3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="825d3-125">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="825d3-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




