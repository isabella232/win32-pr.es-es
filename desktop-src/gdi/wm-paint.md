---
Description: El mensaje de dibujo de WM \_ se envía cuando el sistema u otra aplicación realiza una solicitud para pintar una parte de la ventana de una aplicación.
ms.assetid: afebaa07-cf00-47db-a919-46436f164881
title: Mensaje de WM_PAINT (Winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: b13e1779fb54a3db7905cb8fc738ef45558400f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987505"
---
# <a name="wm_paint-message"></a><span data-ttu-id="fb6b9-103">Mensaje de Paint de WM \_</span><span class="sxs-lookup"><span data-stu-id="fb6b9-103">WM\_PAINT message</span></span>

<span data-ttu-id="fb6b9-104">El mensaje de **\_ dibujo de WM** se envía cuando el sistema u otra aplicación realiza una solicitud para pintar una parte de la ventana de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="fb6b9-104">The **WM\_PAINT** message is sent when the system or another application makes a request to paint a portion of an application's window.</span></span> <span data-ttu-id="fb6b9-105">El mensaje se envía cuando se llama a la función [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) o [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) , o mediante la función [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) cuando la aplicación obtiene un mensaje de **\_ dibujo de WM** mediante la función [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .</span><span class="sxs-lookup"><span data-stu-id="fb6b9-105">The message is sent when the [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) or [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) function is called, or by the [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) function when the application obtains a **WM\_PAINT** message by using the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span>

<span data-ttu-id="fb6b9-106">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fb6b9-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="fb6b9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb6b9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb6b9-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fb6b9-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb6b9-109">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="fb6b9-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fb6b9-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fb6b9-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb6b9-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="fb6b9-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb6b9-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb6b9-112">Return value</span></span>

<span data-ttu-id="fb6b9-113">Una aplicación devuelve cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="fb6b9-113">An application returns zero if it processes this message.</span></span>

## <a name="example"></a><span data-ttu-id="fb6b9-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fb6b9-114">Example</span></span>

```c
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(hwnd, &ps);

            // All painting occurs here, between BeginPaint and EndPaint.
            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
            EndPaint(hwnd, &ps);
        }
        return 0;
    }

    return DefWindowProc(hwnd, uMsg, wParam, lParam);
}

```

<span data-ttu-id="fb6b9-115">Ejemplo de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) en github.</span><span class="sxs-lookup"><span data-stu-id="fb6b9-115">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb6b9-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb6b9-116">Remarks</span></span>

<span data-ttu-id="fb6b9-117">El sistema genera el mensaje de **\_ Paint de WM** y no debe ser enviado por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="fb6b9-117">The **WM\_PAINT** message is generated by the system and should not be sent by an application.</span></span> <span data-ttu-id="fb6b9-118">Para forzar que una ventana dibuje en un contexto de dispositivo específico, use el mensaje [**WM \_ Print**](wm-print.md) o [**WM \_ PRINTCLIENT**](wm-printclient.md) .</span><span class="sxs-lookup"><span data-stu-id="fb6b9-118">To force a window to draw into a specific device context, use the [**WM\_PRINT**](wm-print.md) or [**WM\_PRINTCLIENT**](wm-printclient.md) message.</span></span> <span data-ttu-id="fb6b9-119">Tenga en cuenta que esto requiere que la ventana de destino admita el mensaje de **\_ PRINTCLIENT de WM** .</span><span class="sxs-lookup"><span data-stu-id="fb6b9-119">Note that this requires the target window to support the **WM\_PRINTCLIENT** message.</span></span> <span data-ttu-id="fb6b9-120">Los controles más comunes admiten el mensaje de **\_ PRINTCLIENT de WM** .</span><span class="sxs-lookup"><span data-stu-id="fb6b9-120">Most common controls support the **WM\_PRINTCLIENT** message.</span></span>

<span data-ttu-id="fb6b9-121">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  valida la región de actualización.</span><span class="sxs-lookup"><span data-stu-id="fb6b9-121">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function validates the update region.</span></span> <span data-ttu-id="fb6b9-122">La función también puede enviar el mensaje de [**\_ NCPAINT de WM**](wm-ncpaint.md) al procedimiento de ventana si se debe pintar el marco de la ventana y enviar el mensaje de [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) si el fondo de la ventana debe borrarse.</span><span class="sxs-lookup"><span data-stu-id="fb6b9-122">The function may also send the [**WM\_NCPAINT**](wm-ncpaint.md) message to the window procedure if the window frame must be painted and send the [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message if the window background must be erased.</span></span>

<span data-ttu-id="fb6b9-123">El sistema envía este mensaje cuando no hay otros mensajes en la cola de mensajes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fb6b9-123">The system sends this message when there are no other messages in the application's message queue.</span></span> <span data-ttu-id="fb6b9-124">[**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) determina dónde se debe enviar el mensaje; [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) determina el mensaje que se va a enviar.</span><span class="sxs-lookup"><span data-stu-id="fb6b9-124">[**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) determines where to send the message; [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) determines which message to dispatch.</span></span> <span data-ttu-id="fb6b9-125">**GetMessage** devuelve el mensaje de **\_ dibujo de WM** cuando no hay ningún otro mensaje en la cola de mensajes de la aplicación y **DispatchMessage** envía el mensaje al procedimiento de ventana adecuado.</span><span class="sxs-lookup"><span data-stu-id="fb6b9-125">**GetMessage** returns the **WM\_PAINT** message when there are no other messages in the application's message queue, and **DispatchMessage** sends the message to the appropriate window procedure.</span></span>

<span data-ttu-id="fb6b9-126">Una ventana puede recibir mensajes de dibujo internos como resultado de llamar a [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) con el \_ conjunto de marcas RDW INTERNALPAINT.</span><span class="sxs-lookup"><span data-stu-id="fb6b9-126">A window may receive internal paint messages as a result of calling [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) with the RDW\_INTERNALPAINT flag set.</span></span> <span data-ttu-id="fb6b9-127">En este caso, es posible que la ventana no tenga una región de actualización.</span><span class="sxs-lookup"><span data-stu-id="fb6b9-127">In this case, the window may not have an update region.</span></span> <span data-ttu-id="fb6b9-128">Una aplicación puede llamar a la función [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) para determinar si la ventana tiene una región de actualización.</span><span class="sxs-lookup"><span data-stu-id="fb6b9-128">An application may call the [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) function to determine whether the window has an update region.</span></span> <span data-ttu-id="fb6b9-129">Si **GetUpdateRect** devuelve cero, la aplicación no necesita llamar a las funciones [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) y [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) .</span><span class="sxs-lookup"><span data-stu-id="fb6b9-129">If **GetUpdateRect** returns zero, the application need not call the [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) functions.</span></span>

<span data-ttu-id="fb6b9-130">Una aplicación debe comprobar los dibujos internos necesarios examinando sus estructuras de datos internas para cada mensaje **de \_ pintura de WM** , ya que es posible que un mensaje de **\_ Paint de WM** esté causado por una región de actualización que no sea NULL y una llamada a [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) con el \_ indicador RDW INTERNALPAINT establecido.</span><span class="sxs-lookup"><span data-stu-id="fb6b9-130">An application must check for any necessary internal painting by looking at its internal data structures for each **WM\_PAINT** message, because a **WM\_PAINT** message may have been caused by both a non-NULL update region and a call to [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) with the RDW\_INTERNALPAINT flag set.</span></span>

<span data-ttu-id="fb6b9-131">El sistema envía un mensaje **de \_ dibujo de WM** interno solo una vez.</span><span class="sxs-lookup"><span data-stu-id="fb6b9-131">The system sends an internal **WM\_PAINT** message only once.</span></span> <span data-ttu-id="fb6b9-132">Una vez que se devuelve un mensaje de **\_ dibujo de WM** interno desde [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) o se envía a una ventana por [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow), el sistema no expone ni envía más mensajes de la **\_ pintura de WM** hasta que no se invalida la ventana o hasta que se llama de nuevo a [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) con la \_ marca RDW INTERNALPAINT establecida.</span><span class="sxs-lookup"><span data-stu-id="fb6b9-132">After an internal **WM\_PAINT** message is returned from [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) or is sent to a window by [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow), the system does not post or send further **WM\_PAINT** messages until the window is invalidated or until [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) is called again with the RDW\_INTERNALPAINT flag set.</span></span>

<span data-ttu-id="fb6b9-133">Para algunos controles comunes, el procesamiento de mensajes de **\_ pintura de WM** predeterminado comprueba el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="fb6b9-133">For some common controls, the default **WM\_PAINT** message processing checks the *wParam* parameter.</span></span> <span data-ttu-id="fb6b9-134">Si *wParam* no es null, el control supone que el valor es HDC y pinta usando ese contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb6b9-134">If *wParam* is non-NULL, the control assumes that the value is an HDC and paints using that device context.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb6b9-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb6b9-135">Requirements</span></span>



| <span data-ttu-id="fb6b9-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb6b9-136">Requirement</span></span> | <span data-ttu-id="fb6b9-137">Value</span><span class="sxs-lookup"><span data-stu-id="fb6b9-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb6b9-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb6b9-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fb6b9-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fb6b9-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fb6b9-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb6b9-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fb6b9-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fb6b9-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fb6b9-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb6b9-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb6b9-143"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb6b9-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb6b9-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb6b9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb6b9-145">Información general sobre pintura y dibujo</span><span class="sxs-lookup"><span data-stu-id="fb6b9-145">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="fb6b9-146">Pintar y dibujar mensajes</span><span class="sxs-lookup"><span data-stu-id="fb6b9-146">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="fb6b9-147">**BeginPaint**</span><span class="sxs-lookup"><span data-stu-id="fb6b9-147">**BeginPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[<span data-ttu-id="fb6b9-148">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="fb6b9-148">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="fb6b9-149">**DispatchMessage**</span><span class="sxs-lookup"><span data-stu-id="fb6b9-149">**DispatchMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-dispatchmessage)
</dt> <dt>

[<span data-ttu-id="fb6b9-150">**EndPaint**</span><span class="sxs-lookup"><span data-stu-id="fb6b9-150">**EndPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[<span data-ttu-id="fb6b9-151">**GetMessage**</span><span class="sxs-lookup"><span data-stu-id="fb6b9-151">**GetMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[<span data-ttu-id="fb6b9-152">**GetUpdateRect**</span><span class="sxs-lookup"><span data-stu-id="fb6b9-152">**GetUpdateRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)
</dt> <dt>

[<span data-ttu-id="fb6b9-153">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="fb6b9-153">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[<span data-ttu-id="fb6b9-154">**RedrawWindow**</span><span class="sxs-lookup"><span data-stu-id="fb6b9-154">**RedrawWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> <dt>

[<span data-ttu-id="fb6b9-155">**UpdateWindow**</span><span class="sxs-lookup"><span data-stu-id="fb6b9-155">**UpdateWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-updatewindow)
</dt> <dt>

[<span data-ttu-id="fb6b9-156">**ERASEBKGND de WM \_**</span><span class="sxs-lookup"><span data-stu-id="fb6b9-156">**WM\_ERASEBKGND**</span></span>](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[<span data-ttu-id="fb6b9-157">**NCPAINT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="fb6b9-157">**WM\_NCPAINT**</span></span>](wm-ncpaint.md)
</dt> <dt>

[<span data-ttu-id="fb6b9-158">**impresión de WM \_**</span><span class="sxs-lookup"><span data-stu-id="fb6b9-158">**WM\_PRINT**</span></span>](wm-print.md)
</dt> <dt>

[<span data-ttu-id="fb6b9-159">**PRINTCLIENT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="fb6b9-159">**WM\_PRINTCLIENT**</span></span>](wm-printclient.md)
</dt> </dl>

 

 
