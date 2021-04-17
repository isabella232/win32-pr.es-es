---
description: El \_ método get BorderColor recupera el color del borde actual.
ms.assetid: 4b4cae1d-bef7-4f8d-8011-c220fcfb73eb
title: Método CBaseControlWindow.get_BorderColor (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d889f211b204c2c0180ae757a0240c8588552e83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670541"
---
# <a name="cbasecontrolwindowget_bordercolor-method"></a><span data-ttu-id="5bcff-103">CBaseControlWindow. Get \_ BorderColor (método)</span><span class="sxs-lookup"><span data-stu-id="5bcff-103">CBaseControlWindow.get\_BorderColor method</span></span>

<span data-ttu-id="5bcff-104">El `get_BorderColor` método recupera el color actual del borde.</span><span class="sxs-lookup"><span data-stu-id="5bcff-104">The `get_BorderColor` method retrieves the current border color.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bcff-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5bcff-105">Syntax</span></span>


```C++
HRESULT get_BorderColor(
   long *Color
);
```



## <a name="parameters"></a><span data-ttu-id="5bcff-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5bcff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bcff-107">*Color*</span><span class="sxs-lookup"><span data-stu-id="5bcff-107">*Color*</span></span> 
</dt> <dd>

<span data-ttu-id="5bcff-108">Puntero al color del borde actual.</span><span class="sxs-lookup"><span data-stu-id="5bcff-108">Pointer to the current border color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bcff-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5bcff-109">Return value</span></span>

<span data-ttu-id="5bcff-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5bcff-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bcff-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5bcff-111">Remarks</span></span>

<span data-ttu-id="5bcff-112">Una aplicación puede establecer un rectángulo de destino en el que se debe mostrar el vídeo.</span><span class="sxs-lookup"><span data-stu-id="5bcff-112">An application can set a destination rectangle in which the video should be displayed.</span></span> <span data-ttu-id="5bcff-113">Este rectángulo es relativo al área cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="5bcff-113">This rectangle is relative to the client area for the window.</span></span> <span data-ttu-id="5bcff-114">Si esto se hace (el valor predeterminado es pintar siempre toda la ventana), hay un borde que rodea el vídeo.</span><span class="sxs-lookup"><span data-stu-id="5bcff-114">If this is done (the default is to always paint the entire window), there is a border surrounding the video.</span></span> <span data-ttu-id="5bcff-115">Esta propiedad afecta al color utilizado por el borde.</span><span class="sxs-lookup"><span data-stu-id="5bcff-115">This property affects the color used by the border.</span></span> <span data-ttu-id="5bcff-116">Aunque el parámetro se especifica como un tipo **Long** , en realidad es un valor de **COLORREF** .</span><span class="sxs-lookup"><span data-stu-id="5bcff-116">Although the parameter is specified as a **LONG** type, it is actually a **COLORREF** value.</span></span>

<span data-ttu-id="5bcff-117">Esta función miembro está pensada para que la llamen los objetos externos a través de la interfaz [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) y, por tanto, bloquea la sección crítica para sincronizar con el filtro asociado.</span><span class="sxs-lookup"><span data-stu-id="5bcff-117">This member function is meant to be called by external objects through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, and therefore locks the critical section to synchronize with the associated filter.</span></span> <span data-ttu-id="5bcff-118">Llame a la función miembro [**CBaseControlWindow:: GetBorderColour**](cbasecontrolwindow-getbordercolour.md) para recuperar esta propiedad si no llama a desde un objeto externo.</span><span class="sxs-lookup"><span data-stu-id="5bcff-118">Call the [**CBaseControlWindow::GetBorderColour**](cbasecontrolwindow-getbordercolour.md) member function to retrieve this property if not calling from an external object.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bcff-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bcff-119">Requirements</span></span>



| <span data-ttu-id="5bcff-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bcff-120">Requirement</span></span> | <span data-ttu-id="5bcff-121">Value</span><span class="sxs-lookup"><span data-stu-id="5bcff-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bcff-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5bcff-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5bcff-123"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5bcff-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5bcff-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5bcff-124">Library</span></span><br/> | <dl> <span data-ttu-id="5bcff-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5bcff-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bcff-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bcff-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bcff-127">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="5bcff-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




