---
description: El mensaje de QUERYENDSESSION de WM \_ se envía cuando el usuario elige finalizar la sesión o cuando una aplicación llama a una de las funciones de cierre del sistema.
ms.assetid: 7ad73444-f1f6-4b73-8450-0580b146a5a6
title: Mensaje de WM_QUERYENDSESSION (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2e2f82388b229523f371c680d6ccc7c4b1e27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669781"
---
# <a name="wm_queryendsession-message"></a><span data-ttu-id="b5ae6-103">Mensaje de QUERYENDSESSION de WM \_</span><span class="sxs-lookup"><span data-stu-id="b5ae6-103">WM\_QUERYENDSESSION message</span></span>

<span data-ttu-id="b5ae6-104">El mensaje de **\_ QUERYENDSESSION de WM** se envía cuando el usuario elige finalizar la sesión o cuando una aplicación llama a una de las funciones de cierre del sistema.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-104">The **WM\_QUERYENDSESSION** message is sent when the user chooses to end the session or when an application calls one of the system shutdown functions.</span></span> <span data-ttu-id="b5ae6-105">Si alguna aplicación devuelve cero, la sesión no finaliza.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-105">If any application returns zero, the session is not ended.</span></span> <span data-ttu-id="b5ae6-106">El sistema deja de enviar mensajes de **WM \_ QUERYENDSESSION** en cuanto una aplicación devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-106">The system stops sending **WM\_QUERYENDSESSION** messages as soon as one application returns zero.</span></span>

<span data-ttu-id="b5ae6-107">Después de procesar este mensaje, el sistema envía el mensaje de [**WM \_ ENDSESSION**](wm-endsession.md) con el parámetro *wParam* establecido en los resultados del mensaje de **\_ QUERYENDSESSION de WM** .</span><span class="sxs-lookup"><span data-stu-id="b5ae6-107">After processing this message, the system sends the [**WM\_ENDSESSION**](wm-endsession.md) message with the *wParam* parameter set to the results of the **WM\_QUERYENDSESSION** message.</span></span>

<span data-ttu-id="b5ae6-108">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b5ae6-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // not used 
  LPARAM lParam   // logoff option
);
```



## <a name="parameters"></a><span data-ttu-id="b5ae6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5ae6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5ae6-110">*identificador*</span><span class="sxs-lookup"><span data-stu-id="b5ae6-110">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="b5ae6-111">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-111">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="b5ae6-112">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="b5ae6-112">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="b5ae6-113">Identificador **de \_ QUERYENDSESSION de WM** .</span><span class="sxs-lookup"><span data-stu-id="b5ae6-113">The **WM\_QUERYENDSESSION** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b5ae6-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b5ae6-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5ae6-115">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-115">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="b5ae6-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5ae6-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5ae6-117">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-117">This parameter can be one or more of the following values.</span></span> <span data-ttu-id="b5ae6-118">Si este parámetro es 0, el sistema se está cerrando o reiniciando (no es posible determinar qué evento se está produciendo).</span><span class="sxs-lookup"><span data-stu-id="b5ae6-118">If this parameter is 0, the system is shutting down or restarting (it is not possible to determine which event is occurring).</span></span>



| <span data-ttu-id="b5ae6-119">Value</span><span class="sxs-lookup"><span data-stu-id="b5ae6-119">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="b5ae6-120">Significado</span><span class="sxs-lookup"><span data-stu-id="b5ae6-120">Meaning</span></span>                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <span data-ttu-id="b5ae6-121"><dt>**ENDSESSION \_ CLOSEAPP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="b5ae6-121"><dt>**ENDSESSION\_CLOSEAPP**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="b5ae6-122">La aplicación está usando un archivo que debe reemplazarse, se está realizando el mantenimiento del sistema o se han agotado los recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-122">The application is using a file that must be replaced, the system is being serviced, or system resources are exhausted.</span></span> <span data-ttu-id="b5ae6-123">Para obtener más información, consulte [directrices para aplicaciones](../rstmgr/guidelines-for-applications.md).</span><span class="sxs-lookup"><span data-stu-id="b5ae6-123">For more information, see [Guidelines for Applications](../rstmgr/guidelines-for-applications.md).</span></span><br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <span data-ttu-id="b5ae6-124"><dt>**ENDSESSION \_**</dt> <dt>0x40000000</dt> crítico</span><span class="sxs-lookup"><span data-stu-id="b5ae6-124"><dt>**ENDSESSION\_CRITICAL**</dt> <dt>0x40000000</dt></span></span> </dl> | <span data-ttu-id="b5ae6-125">Se forzará el cierre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-125">The application is forced to shut down.</span></span><br/>                                                                                                                                                                              |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <span data-ttu-id="b5ae6-126"><dt>**ENDSESSION \_ LOGOFF**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="b5ae6-126"><dt>**ENDSESSION\_LOGOFF**</dt> <dt>0x80000000</dt></span></span> </dl>       | <span data-ttu-id="b5ae6-127">El usuario está cerrando la sesión.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-127">The user is logging off.</span></span> <span data-ttu-id="b5ae6-128">Para obtener más información, consulte cerrar [sesión](logging-off.md).</span><span class="sxs-lookup"><span data-stu-id="b5ae6-128">For more information, see [Logging Off](logging-off.md).</span></span><br/>                                                                                                                                   |



 

<span data-ttu-id="b5ae6-129">Tenga en cuenta que este parámetro es una máscara de bits.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-129">Note that this parameter is a bit mask.</span></span> <span data-ttu-id="b5ae6-130">Para probar este valor, use una operación de bits; no se comprueba la igualdad.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-130">To test for this value, use a bit-wise operation; do not test for equality.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5ae6-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5ae6-131">Return value</span></span>

<span data-ttu-id="b5ae6-132">Las aplicaciones deben respetar las intenciones del usuario y devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-132">Applications should respect the user's intentions and return **TRUE**.</span></span> <span data-ttu-id="b5ae6-133">De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve **true** para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-133">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns **TRUE** for this message.</span></span>

<span data-ttu-id="b5ae6-134">Si el apagado dañaría el sistema o el medio que se está grabando, la aplicación puede devolver el **valor false**.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-134">If shutting down would corrupt the system or media that is being burned, the application can return **FALSE**.</span></span> <span data-ttu-id="b5ae6-135">Sin embargo, se recomienda respetar las acciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-135">However, it is good practice to respect the user's actions.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5ae6-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5ae6-136">Remarks</span></span>

<span data-ttu-id="b5ae6-137">Cuando una aplicación devuelve **true** para este mensaje, recibe el mensaje de [**WM \_ ENDSESSION**](wm-endsession.md) , sin tener en consideración el modo en que las otras aplicaciones responden al mensaje de **\_ QUERYENDSESSION de WM** .</span><span class="sxs-lookup"><span data-stu-id="b5ae6-137">When an application returns **TRUE** for this message, it receives the [**WM\_ENDSESSION**](wm-endsession.md) message, regardless of how the other applications respond to the **WM\_QUERYENDSESSION** message.</span></span> <span data-ttu-id="b5ae6-138">Cada aplicación debe devolver **true** o **false** inmediatamente después de recibir este mensaje y diferir las operaciones de limpieza hasta que reciba el mensaje de la **\_ ENDSESSION de WM** .</span><span class="sxs-lookup"><span data-stu-id="b5ae6-138">Each application should return **TRUE** or **FALSE** immediately upon receiving this message, and defer any cleanup operations until it receives the **WM\_ENDSESSION** message.</span></span>

<span data-ttu-id="b5ae6-139">Las aplicaciones pueden mostrar una interfaz de usuario en la que se pide al usuario información al cerrarse; sin embargo, no se recomienda.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-139">Applications can display a user interface prompting the user for information at shutdown, however it is not recommended.</span></span> <span data-ttu-id="b5ae6-140">Después de cinco segundos, el sistema muestra información acerca de las aplicaciones que están evitando el apagado y permite que el usuario las termine.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-140">After five seconds, the system displays information about the applications that are preventing shutdown and allows the user to terminate them.</span></span> <span data-ttu-id="b5ae6-141">Por ejemplo, Windows XP muestra un cuadro de diálogo, mientras que Windows Vista muestra una pantalla completa con información adicional sobre las aplicaciones que bloquean el cierre.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-141">For example, Windows XP displays a dialog box, while Windows Vista displays a full screen with additional information about the applications blocking shutdown.</span></span> <span data-ttu-id="b5ae6-142">Si la aplicación debe bloquear o posponer el cierre del sistema, use la función [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) .</span><span class="sxs-lookup"><span data-stu-id="b5ae6-142">If your application must block or postpone system shutdown, use the [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) function.</span></span> <span data-ttu-id="b5ae6-143">Para obtener más información, vea [cambios de apagado para Windows Vista](shutdown-changes-for-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="b5ae6-143">For more information, see [Shutdown Changes for Windows Vista](shutdown-changes-for-windows-vista.md).</span></span>

<span data-ttu-id="b5ae6-144">Las aplicaciones de consola pueden utilizar la función [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) para recibir la notificación de cierre.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-144">Console applications can use the [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) function to receive shutdown notification.</span></span>

<span data-ttu-id="b5ae6-145">Las aplicaciones de servicio pueden usar la función [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) para recibir notificaciones de cierre en una rutina de controlador.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-145">Service applications can use the [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) function to receive shutdown notifications in a handler routine.</span></span>

## <a name="examples"></a><span data-ttu-id="b5ae6-146">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b5ae6-146">Examples</span></span>

<span data-ttu-id="b5ae6-147">Para obtener un ejemplo, consulte cerrar [sesión](logging-off.md).</span><span class="sxs-lookup"><span data-stu-id="b5ae6-147">For an example, see [Logging Off](logging-off.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5ae6-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5ae6-148">Requirements</span></span>



| <span data-ttu-id="b5ae6-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5ae6-149">Requirement</span></span> | <span data-ttu-id="b5ae6-150">Value</span><span class="sxs-lookup"><span data-stu-id="b5ae6-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ae6-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5ae6-151">Minimum supported client</span></span><br/> | <span data-ttu-id="b5ae6-152">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows XP \|\]</span><span class="sxs-lookup"><span data-stu-id="b5ae6-152">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                       |
| <span data-ttu-id="b5ae6-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5ae6-153">Minimum supported server</span></span><br/> | <span data-ttu-id="b5ae6-154">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2003 \|\]</span><span class="sxs-lookup"><span data-stu-id="b5ae6-154">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="b5ae6-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5ae6-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5ae6-156"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5ae6-156"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5ae6-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5ae6-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5ae6-158">Cerrando sesión</span><span class="sxs-lookup"><span data-stu-id="b5ae6-158">Logging Off</span></span>](logging-off.md)
</dt> <dt>

[<span data-ttu-id="b5ae6-159">Apagar</span><span class="sxs-lookup"><span data-stu-id="b5ae6-159">Shutting Down</span></span>](shutting-down.md)
</dt> <dt>

[<span data-ttu-id="b5ae6-160">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="b5ae6-160">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="b5ae6-161">**ExitWindows**</span><span class="sxs-lookup"><span data-stu-id="b5ae6-161">**ExitWindows**</span></span>](/windows/desktop/api/Winuser/nf-winuser-exitwindows)
</dt> <dt>

[<span data-ttu-id="b5ae6-162">**SetProcessShutdownParameters**</span><span class="sxs-lookup"><span data-stu-id="b5ae6-162">**SetProcessShutdownParameters**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[<span data-ttu-id="b5ae6-163">**WM \_ ENDSESSION**</span><span class="sxs-lookup"><span data-stu-id="b5ae6-163">**WM\_ENDSESSION**</span></span>](wm-endsession.md)
</dt> </dl>

 

 
