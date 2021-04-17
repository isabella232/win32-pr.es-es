---
description: El método PossiblyEatMessage reenvía los mensajes de teclado y del mouse a la ventana de purga de mensajes.
ms.assetid: 8e344c5d-2f94-454f-89b7-45c539b6e833
title: Método CBaseControlWindow. PossiblyEatMessage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9bfadcfbbd6833d8f3e9b65bd39d0cdbef4a006e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660468"
---
# <a name="cbasecontrolwindowpossiblyeatmessage-method"></a><span data-ttu-id="77234-103">CBaseControlWindow. PossiblyEatMessage, método</span><span class="sxs-lookup"><span data-stu-id="77234-103">CBaseControlWindow.PossiblyEatMessage method</span></span>

<span data-ttu-id="77234-104">El `PossiblyEatMessage` método reenvía los mensajes del teclado y del mouse a la ventana de purga de mensajes.</span><span class="sxs-lookup"><span data-stu-id="77234-104">The `PossiblyEatMessage` method forwards keyboard and mouse messages to the message-drain window.</span></span>

## <a name="syntax"></a><span data-ttu-id="77234-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77234-105">Syntax</span></span>


```C++
BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="77234-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77234-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77234-107">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="77234-107">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="77234-108">Mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="77234-108">Window message.</span></span>

</dd> <dt>

<span data-ttu-id="77234-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="77234-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77234-110">Primer parámetro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="77234-110">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="77234-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77234-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77234-112">Segundo parámetro del mensaje.</span><span class="sxs-lookup"><span data-stu-id="77234-112">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77234-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77234-113">Return value</span></span>

<span data-ttu-id="77234-114">Devuelve **true** si el mensaje se reenvió a la ventana o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="77234-114">Returns **TRUE** if the message was forwarded to the window, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="77234-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77234-115">Remarks</span></span>

<span data-ttu-id="77234-116">La ventana de purga de mensajes es una ventana designada para recibir determinados mensajes del mouse y del teclado.</span><span class="sxs-lookup"><span data-stu-id="77234-116">The message-drain window is a window designated to receive certain mouse and keyboard messages.</span></span> <span data-ttu-id="77234-117">Inicialmente, la ventana es **null**; se puede establecer llamando a [**CBaseControlWindow::p UT \_ MessageDrain**](cbasecontrolwindow-put-messagedrain.md).</span><span class="sxs-lookup"><span data-stu-id="77234-117">Initially the window is **NULL**; it can be set by calling [**CBaseControlWindow::put\_MessageDrain**](cbasecontrolwindow-put-messagedrain.md).</span></span>

<span data-ttu-id="77234-118">Si la ventana de purga de mensajes no es **null**, `PossiblyEatMessage` envía los mensajes siguientes a esa ventana:</span><span class="sxs-lookup"><span data-stu-id="77234-118">If the message-drain window is non-**NULL**, `PossiblyEatMessage` posts the following messages to that window:</span></span>

-   <span data-ttu-id="77234-119">carácter de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-119">WM\_CHAR</span></span>
-   <span data-ttu-id="77234-120">DEADCHAR de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-120">WM\_DEADCHAR</span></span>
-   <span data-ttu-id="77234-121">KEYDOWN de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-121">WM\_KEYDOWN</span></span>
-   <span data-ttu-id="77234-122">KEYUP de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-122">WM\_KEYUP</span></span>
-   <span data-ttu-id="77234-123">LBUTTONDBLCLK de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-123">WM\_LBUTTONDBLCLK</span></span>
-   <span data-ttu-id="77234-124">LBUTTONDOWN de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-124">WM\_LBUTTONDOWN</span></span>
-   <span data-ttu-id="77234-125">LBUTTONUP de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-125">WM\_LBUTTONUP</span></span>
-   <span data-ttu-id="77234-126">MBUTTONDBLCLK de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-126">WM\_MBUTTONDBLCLK</span></span>
-   <span data-ttu-id="77234-127">MBUTTONDOWN de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-127">WM\_MBUTTONDOWN</span></span>
-   <span data-ttu-id="77234-128">MBUTTONUP de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-128">WM\_MBUTTONUP</span></span>
-   <span data-ttu-id="77234-129">MOUSEACTIVATE de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-129">WM\_MOUSEACTIVATE</span></span>
-   <span data-ttu-id="77234-130">MOUSEMOVE de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-130">WM\_MOUSEMOVE</span></span>
-   <span data-ttu-id="77234-131">NCLBUTTONDBLCLK de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-131">WM\_NCLBUTTONDBLCLK</span></span>
-   <span data-ttu-id="77234-132">NCLBUTTONDOWN de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-132">WM\_NCLBUTTONDOWN</span></span>
-   <span data-ttu-id="77234-133">NCLBUTTONUP de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-133">WM\_NCLBUTTONUP</span></span>
-   <span data-ttu-id="77234-134">NCMBUTTONDBLCLK de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-134">WM\_NCMBUTTONDBLCLK</span></span>
-   <span data-ttu-id="77234-135">NCMBUTTONDOWN de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-135">WM\_NCMBUTTONDOWN</span></span>
-   <span data-ttu-id="77234-136">NCMBUTTONUP de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-136">WM\_NCMBUTTONUP</span></span>
-   <span data-ttu-id="77234-137">NCMOUSEMOVE de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-137">WM\_NCMOUSEMOVE</span></span>
-   <span data-ttu-id="77234-138">NCRBUTTONDBLCLK de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-138">WM\_NCRBUTTONDBLCLK</span></span>
-   <span data-ttu-id="77234-139">NCRBUTTONDOWN de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-139">WM\_NCRBUTTONDOWN</span></span>
-   <span data-ttu-id="77234-140">NCRBUTTONUP de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-140">WM\_NCRBUTTONUP</span></span>
-   <span data-ttu-id="77234-141">RBUTTONDBLCLK de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-141">WM\_RBUTTONDBLCLK</span></span>
-   <span data-ttu-id="77234-142">RBUTTONDOWN de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-142">WM\_RBUTTONDOWN</span></span>
-   <span data-ttu-id="77234-143">RBUTTONUP de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-143">WM\_RBUTTONUP</span></span>
-   <span data-ttu-id="77234-144">SYSCHAR de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-144">WM\_SYSCHAR</span></span>
-   <span data-ttu-id="77234-145">SYSDEADCHAR de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-145">WM\_SYSDEADCHAR</span></span>
-   <span data-ttu-id="77234-146">SYSKEYDOWN de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-146">WM\_SYSKEYDOWN</span></span>
-   <span data-ttu-id="77234-147">SYSKEYUP de WM \_</span><span class="sxs-lookup"><span data-stu-id="77234-147">WM\_SYSKEYUP</span></span>

<span data-ttu-id="77234-148">Omite otros mensajes.</span><span class="sxs-lookup"><span data-stu-id="77234-148">It ignores other messages.</span></span> <span data-ttu-id="77234-149">Si la ventana de purga de mensajes es **null**, el método omite todos los mensajes de ventana.</span><span class="sxs-lookup"><span data-stu-id="77234-149">If the message-drain window is **NULL**, the method ignores all window messages.</span></span> <span data-ttu-id="77234-150">El método devuelve **true** si envía el mensaje o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="77234-150">The method returns **TRUE** if it posts the message, or **FALSE** otherwise.</span></span> <span data-ttu-id="77234-151">La clase **CBaseWindow** llama a este método cuando recibe un mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="77234-151">The **CBaseWindow** class calls this method when it receives a window message.</span></span>

## <a name="requirements"></a><span data-ttu-id="77234-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77234-152">Requirements</span></span>



| <span data-ttu-id="77234-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="77234-153">Requirement</span></span> | <span data-ttu-id="77234-154">Value</span><span class="sxs-lookup"><span data-stu-id="77234-154">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77234-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77234-155">Header</span></span><br/>  | <dl> <span data-ttu-id="77234-156"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="77234-156"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="77234-157">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="77234-157">Library</span></span><br/> | <dl> <span data-ttu-id="77234-158"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="77234-158"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77234-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="77234-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77234-160">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="77234-160">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




