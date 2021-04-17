---
description: El \_ método get Autoshow recupera la marca de estado de Automostrar actual.
ms.assetid: b27651d1-3ac5-4a52-9549-b63bacda5dc8
title: Método CBaseControlWindow.get_AutoShow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f45679b9d036f1c5386cd2c1d18a31fa3d6bd64f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670542"
---
# <a name="cbasecontrolwindowget_autoshow-method"></a><span data-ttu-id="1c082-103">CBaseControlWindow. get ( \_ método de Autoshow)</span><span class="sxs-lookup"><span data-stu-id="1c082-103">CBaseControlWindow.get\_AutoShow method</span></span>

<span data-ttu-id="1c082-104">El `get_AutoShow` método recupera la marca de estado de Automostrar actual.</span><span class="sxs-lookup"><span data-stu-id="1c082-104">The `get_AutoShow` method retrieves the current AutoShow state flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c082-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c082-105">Syntax</span></span>


```C++
HRESULT get_AutoShow(
   long *AutoShow
);
```



## <a name="parameters"></a><span data-ttu-id="1c082-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c082-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c082-107">*Automostrar*</span><span class="sxs-lookup"><span data-stu-id="1c082-107">*AutoShow*</span></span> 
</dt> <dd>

<span data-ttu-id="1c082-108">Puntero a una marca booleana de Automation (0 es OFF, 1 es ON).</span><span class="sxs-lookup"><span data-stu-id="1c082-108">Pointer to an Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c082-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c082-109">Return value</span></span>

<span data-ttu-id="1c082-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1c082-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c082-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c082-111">Remarks</span></span>

<span data-ttu-id="1c082-112">Esta función miembro implementa el método [**IVideoWindow:: get \_ Autoshow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) .</span><span class="sxs-lookup"><span data-stu-id="1c082-112">This member function implements the [**IVideoWindow::get\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) method.</span></span> <span data-ttu-id="1c082-113">Esta propiedad simplifica el acceso de visualización de la ventana para las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="1c082-113">This property simplifies window display access for applications.</span></span> <span data-ttu-id="1c082-114">Si se establece en 1 (activado), la ventana, que normalmente se oculta después de la conexión del filtro, se mostrará automáticamente cuando el filtro se ejecute en pausa o se ejecute.</span><span class="sxs-lookup"><span data-stu-id="1c082-114">If this is set to  1 (on), the window, which is typically hidden after connection of the filter, will be displayed automatically when the filter pauses or runs.</span></span> <span data-ttu-id="1c082-115">No obstante, no se debe ocultar la ventana cuando el filtro se detenga.</span><span class="sxs-lookup"><span data-stu-id="1c082-115">The window should not be hidden when the filter stops, however.</span></span> <span data-ttu-id="1c082-116">Si este parámetro se establece en 0 (desactivado), la ventana solo se hace visible cuando la aplicación llama a [**CBaseControlWindow::p UT \_ visible**](cbasecontrolwindow-put-visible.md) o [**CBaseControlWindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) con los parámetros adecuados.</span><span class="sxs-lookup"><span data-stu-id="1c082-116">If this parameter is set to 0 (off), the window is made visible only when the application calls [**CBaseControlWindow::put\_Visible**](cbasecontrolwindow-put-visible.md) or [**CBaseControlWindow::put\_WindowState**](cbasecontrolwindow-put-windowstate.md) with the appropriate parameters.</span></span>

<span data-ttu-id="1c082-117">Esta función miembro está pensada para que la llamen los objetos externos a través de la interfaz [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) y, por tanto, bloquea la sección crítica para sincronizar con el filtro asociado.</span><span class="sxs-lookup"><span data-stu-id="1c082-117">This member function is meant to be called by external objects through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, and therefore locks the critical section to synchronize with the associated filter.</span></span> <span data-ttu-id="1c082-118">Llame a la función miembro [**CBaseControlWindow:: IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) para recuperar esta propiedad si no está llamando a desde un objeto externo.</span><span class="sxs-lookup"><span data-stu-id="1c082-118">Call the [**CBaseControlWindow::IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) member function to retrieve this property if you are not calling from an external object.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c082-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c082-119">Requirements</span></span>



| <span data-ttu-id="1c082-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c082-120">Requirement</span></span> | <span data-ttu-id="1c082-121">Value</span><span class="sxs-lookup"><span data-stu-id="1c082-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c082-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c082-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1c082-123"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c082-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1c082-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1c082-124">Library</span></span><br/> | <dl> <span data-ttu-id="1c082-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1c082-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c082-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c082-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c082-127">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="1c082-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




