---
description: El \_ método put Autoshow establece la marca de estado de Automostrar.
ms.assetid: 857472b8-845b-46d3-8593-3fba9a9c8cdc
title: Método CBaseControlWindow.put_AutoShow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eda5c0c4055979537c5cc471053715e29a348f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660467"
---
# <a name="cbasecontrolwindowput_autoshow-method"></a><span data-ttu-id="a19a1-103">CBaseControlWindow. put ( \_ método de Autoshow)</span><span class="sxs-lookup"><span data-stu-id="a19a1-103">CBaseControlWindow.put\_AutoShow method</span></span>

<span data-ttu-id="a19a1-104">El `put_AutoShow` método establece la marca de estado de Automostrar.</span><span class="sxs-lookup"><span data-stu-id="a19a1-104">The `put_AutoShow` method sets the AutoShow state flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="a19a1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a19a1-105">Syntax</span></span>


```C++
HRESULT put_AutoShow(
   long AutoShow
);
```



## <a name="parameters"></a><span data-ttu-id="a19a1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a19a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a19a1-107">*Automostrar*</span><span class="sxs-lookup"><span data-stu-id="a19a1-107">*AutoShow*</span></span> 
</dt> <dd>

<span data-ttu-id="a19a1-108">Marca booleana de Automation (0 está desactivado, 1 en).</span><span class="sxs-lookup"><span data-stu-id="a19a1-108">Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a19a1-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a19a1-109">Return value</span></span>

<span data-ttu-id="a19a1-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a19a1-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a19a1-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a19a1-111">Remarks</span></span>

<span data-ttu-id="a19a1-112">Esta propiedad simplifica el acceso de visualización de la ventana para las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a19a1-112">This property simplifies window display access for applications.</span></span> <span data-ttu-id="a19a1-113">Si se establece en 1 (activado), la ventana, que normalmente se oculta después de que el filtro está conectado, se mostrará automáticamente cuando el filtro se ejecute en pausa o se ejecute.</span><span class="sxs-lookup"><span data-stu-id="a19a1-113">If this is set to  1 (on), the window, which is typically hidden after the filter is connected, will be displayed automatically when the filter pauses or runs.</span></span> <span data-ttu-id="a19a1-114">No obstante, no se debe ocultar la ventana cuando el filtro se detenga.</span><span class="sxs-lookup"><span data-stu-id="a19a1-114">The window should not be hidden when the filter stops, however.</span></span> <span data-ttu-id="a19a1-115">Si se establece en 0 (desactivado), la ventana solo se hace visible cuando la aplicación llama a [**CBaseControlWindow::p UT \_ visible**](cbasecontrolwindow-put-visible.md) o [**CBaseControlWindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) con los parámetros adecuados.</span><span class="sxs-lookup"><span data-stu-id="a19a1-115">If this is set to 0 (off), the window is made visible only when the application calls [**CBaseControlWindow::put\_Visible**](cbasecontrolwindow-put-visible.md) or [**CBaseControlWindow::put\_WindowState**](cbasecontrolwindow-put-windowstate.md) with the appropriate parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="a19a1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a19a1-116">Requirements</span></span>



| <span data-ttu-id="a19a1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a19a1-117">Requirement</span></span> | <span data-ttu-id="a19a1-118">Value</span><span class="sxs-lookup"><span data-stu-id="a19a1-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a19a1-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a19a1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a19a1-120"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a19a1-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a19a1-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a19a1-121">Library</span></span><br/> | <dl> <span data-ttu-id="a19a1-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a19a1-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a19a1-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="a19a1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a19a1-124">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="a19a1-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




