---
description: El \_ método put WindowStyleEx establece los estilos extendidos de ventana.
ms.assetid: 3c5928fe-7cd3-4e1c-9a3f-fa6d7a73dbc3
title: Método CBaseControlWindow.put_WindowStyleEx (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ee04cf2d2b2dcaafdaf4e989fd1118abf447698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661339"
---
# <a name="cbasecontrolwindowput_windowstyleex-method"></a><span data-ttu-id="d0250-103">CBaseControlWindow. put \_ WindowStyleEx (método)</span><span class="sxs-lookup"><span data-stu-id="d0250-103">CBaseControlWindow.put\_WindowStyleEx method</span></span>

<span data-ttu-id="d0250-104">El `put_WindowStyleEx` método establece los estilos extendidos de ventana.</span><span class="sxs-lookup"><span data-stu-id="d0250-104">The `put_WindowStyleEx` method sets the extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0250-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0250-105">Syntax</span></span>


```C++
HRESULT put_WindowStyleEx(
  [in] long WindowStyleEx
);
```



## <a name="parameters"></a><span data-ttu-id="d0250-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0250-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0250-107">*WindowStyleEx* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0250-107">*WindowStyleEx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0250-108">Valor que especifica el estilo de la ventana de control.</span><span class="sxs-lookup"><span data-stu-id="d0250-108">Value that specifies the style of the control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0250-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0250-109">Return value</span></span>

<span data-ttu-id="d0250-110">Devuelve NoError.</span><span class="sxs-lookup"><span data-stu-id="d0250-110">Returns NOERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0250-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0250-111">Remarks</span></span>

<span data-ttu-id="d0250-112">Este método usa estilos extendidos de ventana.</span><span class="sxs-lookup"><span data-stu-id="d0250-112">This method uses extended window styles.</span></span> <span data-ttu-id="d0250-113">Para obtener una lista completa de los estilos de ventana extendidos, vea la función **CreateWindowEx** de Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="d0250-113">For a complete list of extended window styles, see the Microsoft Win32 **CreateWindowEx** function.</span></span> <span data-ttu-id="d0250-114">Para cambiar el estilo de ventana, recupere el estilo de ventana actual y, a continuación, agregue o quite los campos de bits necesarios.</span><span class="sxs-lookup"><span data-stu-id="d0250-114">To change the window style, retrieve the current window style, and then add or remove the necessary bit fields.</span></span>

<span data-ttu-id="d0250-115">No utilice los siguientes estilos de ventana porque no se validan.</span><span class="sxs-lookup"><span data-stu-id="d0250-115">Do not use the following window styles because they are not validated.</span></span>

-   <span data-ttu-id="d0250-116">WS \_ deshabilitado</span><span class="sxs-lookup"><span data-stu-id="d0250-116">WS\_DISABLED</span></span>
-   <span data-ttu-id="d0250-117">WS \_ HSCROLL</span><span class="sxs-lookup"><span data-stu-id="d0250-117">WS\_HSCROLL</span></span>
-   <span data-ttu-id="d0250-118">iconos de WS \_</span><span class="sxs-lookup"><span data-stu-id="d0250-118">WS\_ICONIC</span></span>
-   <span data-ttu-id="d0250-119">\_maximizar WS</span><span class="sxs-lookup"><span data-stu-id="d0250-119">WS\_MAXIMIZE</span></span>
-   <span data-ttu-id="d0250-120">\_minimizar WS</span><span class="sxs-lookup"><span data-stu-id="d0250-120">WS\_MINIMIZE</span></span>
-   <span data-ttu-id="d0250-121">WS \_ VSCROLL</span><span class="sxs-lookup"><span data-stu-id="d0250-121">WS\_VSCROLL</span></span>

<span data-ttu-id="d0250-122">Con algunas excepciones (que se indican aquí), las marcas aceptables son las mismas que las permitidas por la función **CreateWindow** de Win32.</span><span class="sxs-lookup"><span data-stu-id="d0250-122">With some exceptions (noted here), the acceptable flags are the same as those allowed by the Win32 **CreateWindow** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0250-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0250-123">Requirements</span></span>



| <span data-ttu-id="d0250-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0250-124">Requirement</span></span> | <span data-ttu-id="d0250-125">Value</span><span class="sxs-lookup"><span data-stu-id="d0250-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0250-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0250-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d0250-127"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0250-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d0250-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0250-128">Library</span></span><br/> | <dl> <span data-ttu-id="d0250-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d0250-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0250-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0250-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0250-131">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="d0250-131">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




