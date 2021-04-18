---
description: El \_ mensaje ENDSESSION de WM se envía a una aplicación después de que el sistema procese los resultados del mensaje de QUERYENDSESSION de WM \_ . El \_ mensaje ENDSESSION de WM informa a la aplicación de si la sesión está finalizando.
ms.assetid: 9bf04f24-da1e-4680-a47b-28e9c500635e
title: Mensaje de WM_ENDSESSION (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa62f356d881182dd6e6fd9e0558332bcc1b3fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666714"
---
# <a name="wm_endsession-message"></a><span data-ttu-id="9d288-104">\_Mensaje ENDSESSION de WM</span><span class="sxs-lookup"><span data-stu-id="9d288-104">WM\_ENDSESSION message</span></span>

<span data-ttu-id="9d288-105">El **mensaje \_ ENDSESSION de WM** se envía a una aplicación después de que el sistema procese los resultados del mensaje de [**\_ QUERYENDSESSION de WM**](wm-queryendsession.md) .</span><span class="sxs-lookup"><span data-stu-id="9d288-105">The **WM\_ENDSESSION** message is sent to an application after the system processes the results of the [**WM\_QUERYENDSESSION**](wm-queryendsession.md) message.</span></span> <span data-ttu-id="9d288-106">El **mensaje \_ ENDSESSION de WM** informa a la aplicación de si la sesión está finalizando.</span><span class="sxs-lookup"><span data-stu-id="9d288-106">The **WM\_ENDSESSION** message informs the application whether the session is ending.</span></span>

<span data-ttu-id="9d288-107">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9d288-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // end-session option 
  LPARAM lParam   // logoff option
);
```



## <a name="parameters"></a><span data-ttu-id="9d288-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d288-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d288-109">*identificador*</span><span class="sxs-lookup"><span data-stu-id="9d288-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="9d288-110">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="9d288-110">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="9d288-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="9d288-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="9d288-112">Identificador **\_ ENDSESSION de WM** .</span><span class="sxs-lookup"><span data-stu-id="9d288-112">The **WM\_ENDSESSION** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="9d288-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9d288-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d288-114">Si se finaliza la sesión, este parámetro es **true**; la sesión puede finalizar en cualquier momento después de que todas las aplicaciones hayan devuelto el procesamiento de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="9d288-114">If the session is being ended, this parameter is **TRUE**; the session can end any time after all applications have returned from processing this message.</span></span> <span data-ttu-id="9d288-115">De lo contrario, es **false**.</span><span class="sxs-lookup"><span data-stu-id="9d288-115">Otherwise, it is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="9d288-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9d288-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d288-117">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="9d288-117">This parameter can be one or more of the following values.</span></span> <span data-ttu-id="9d288-118">Si este parámetro es 0, el sistema se está cerrando o reiniciando (no es posible determinar qué evento se está produciendo).</span><span class="sxs-lookup"><span data-stu-id="9d288-118">If this parameter is 0, the system is shutting down or restarting (it is not possible to determine which event is occurring).</span></span>



| <span data-ttu-id="9d288-119">Value</span><span class="sxs-lookup"><span data-stu-id="9d288-119">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="9d288-120">Significado</span><span class="sxs-lookup"><span data-stu-id="9d288-120">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <span data-ttu-id="9d288-121"><dt>**ENDSESSION \_ CLOSEAPP**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="9d288-121"><dt>**ENDSESSION\_CLOSEAPP**</dt> <dt>0x1</dt></span></span> </dl>        | <span data-ttu-id="9d288-122">Si *wParam* es **true**, la aplicación debe cerrarse.</span><span class="sxs-lookup"><span data-stu-id="9d288-122">If *wParam* is **TRUE**, the application must shut down.</span></span> <span data-ttu-id="9d288-123">Los datos deben guardarse automáticamente sin preguntar al usuario (para obtener más información, vea la sección comentarios).</span><span class="sxs-lookup"><span data-stu-id="9d288-123">Any data should be saved automatically without prompting the user (for more information, see Remarks).</span></span> <span data-ttu-id="9d288-124">El administrador de reinicio envía este mensaje cuando la aplicación está usando un archivo que necesita ser reemplazado, cuando debe atender el sistema o cuando se agotan los recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="9d288-124">The Restart Manager sends this message when the application is using a file that needs to be replaced, when it must service the system, or when system resources are exhausted.</span></span> <span data-ttu-id="9d288-125">La aplicación se reiniciará si se ha registrado para el reinicio mediante la función [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) .</span><span class="sxs-lookup"><span data-stu-id="9d288-125">The application will be restarted if it has registered for restart using the [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) function.</span></span> <span data-ttu-id="9d288-126">Para obtener más información, consulte [directrices para aplicaciones](../rstmgr/guidelines-for-applications.md).</span><span class="sxs-lookup"><span data-stu-id="9d288-126">For more information, see [Guidelines for Applications](../rstmgr/guidelines-for-applications.md).</span></span> <br/> <span data-ttu-id="9d288-127">Si *wParam* es **false**, la aplicación no se debe cerrar.</span><span class="sxs-lookup"><span data-stu-id="9d288-127">If *wParam* is **FALSE**, the application should not shut down.</span></span><br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <span data-ttu-id="9d288-128"><dt>**ENDSESSION \_**</dt> <dt>0x40000000</dt> crítico</span><span class="sxs-lookup"><span data-stu-id="9d288-128"><dt>**ENDSESSION\_CRITICAL**</dt> <dt>0x40000000</dt></span></span> </dl> | <span data-ttu-id="9d288-129">Se forzará el cierre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9d288-129">The application is forced to shut down.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <span data-ttu-id="9d288-130"><dt>**ENDSESSION \_ LOGOFF**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="9d288-130"><dt>**ENDSESSION\_LOGOFF**</dt> <dt>0x80000000</dt></span></span> </dl>       | <span data-ttu-id="9d288-131">El usuario está cerrando la sesión.</span><span class="sxs-lookup"><span data-stu-id="9d288-131">The user is logging off.</span></span> <span data-ttu-id="9d288-132">Para obtener más información, consulte cerrar [sesión](logging-off.md).</span><span class="sxs-lookup"><span data-stu-id="9d288-132">For more information, see [Logging Off](logging-off.md).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="9d288-133">Tenga en cuenta que este parámetro es una máscara de bits.</span><span class="sxs-lookup"><span data-stu-id="9d288-133">Note that this parameter is a bit mask.</span></span> <span data-ttu-id="9d288-134">Para probar este valor, use una operación de bits; no se comprueba la igualdad.</span><span class="sxs-lookup"><span data-stu-id="9d288-134">To test for this value, use a bit-wise operation; do not test for equality.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d288-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d288-135">Return value</span></span>

<span data-ttu-id="9d288-136">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="9d288-136">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d288-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9d288-137">Remarks</span></span>

<span data-ttu-id="9d288-138">Las aplicaciones que tienen datos no guardados pueden guardar los datos en una ubicación temporal y restaurarlos la próxima vez que se inicie la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9d288-138">Applications that have unsaved data could save the data to a temporary location and restore it the next time the application starts.</span></span> <span data-ttu-id="9d288-139">Se recomienda que las aplicaciones guarden los datos y el estado con frecuencia. por ejemplo, guarde automáticamente los datos entre las operaciones de guardado iniciadas por el usuario para reducir la cantidad de datos que se van a guardar en el cierre.</span><span class="sxs-lookup"><span data-stu-id="9d288-139">It is recommended that applications save their data and state frequently; for example, automatically save data between save operations initiated by the user to reduce the amount of data to be saved at shutdown.</span></span>

<span data-ttu-id="9d288-140">La aplicación no necesita llamar a la función [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) o [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) cuando finaliza la sesión.</span><span class="sxs-lookup"><span data-stu-id="9d288-140">The application need not call the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) or [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function when the session is ending.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d288-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d288-141">Requirements</span></span>



| <span data-ttu-id="9d288-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d288-142">Requirement</span></span> | <span data-ttu-id="9d288-143">Value</span><span class="sxs-lookup"><span data-stu-id="9d288-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d288-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d288-144">Minimum supported client</span></span><br/> | <span data-ttu-id="9d288-145">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows XP \|\]</span><span class="sxs-lookup"><span data-stu-id="9d288-145">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                       |
| <span data-ttu-id="9d288-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d288-146">Minimum supported server</span></span><br/> | <span data-ttu-id="9d288-147">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2003 \|\]</span><span class="sxs-lookup"><span data-stu-id="9d288-147">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="9d288-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d288-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d288-149"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d288-149"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d288-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d288-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d288-151">Cerrando sesión</span><span class="sxs-lookup"><span data-stu-id="9d288-151">Logging Off</span></span>](logging-off.md)
</dt> <dt>

[<span data-ttu-id="9d288-152">Apagar</span><span class="sxs-lookup"><span data-stu-id="9d288-152">Shutting Down</span></span>](shutting-down.md)
</dt> <dt>

[<span data-ttu-id="9d288-153">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="9d288-153">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[<span data-ttu-id="9d288-154">**PostQuitMessage**</span><span class="sxs-lookup"><span data-stu-id="9d288-154">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[<span data-ttu-id="9d288-155">**SetProcessShutdownParameters**</span><span class="sxs-lookup"><span data-stu-id="9d288-155">**SetProcessShutdownParameters**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[<span data-ttu-id="9d288-156">**QUERYENDSESSION de WM \_**</span><span class="sxs-lookup"><span data-stu-id="9d288-156">**WM\_QUERYENDSESSION**</span></span>](wm-queryendsession.md)
</dt> </dl>

 

 
