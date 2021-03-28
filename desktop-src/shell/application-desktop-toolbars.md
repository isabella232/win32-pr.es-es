---
description: Una barra de herramientas del escritorio de la aplicación (también denominada Appbar) es una ventana similar a la barra de tareas de Windows.
ms.assetid: d9f63cb1-e2cc-4a3b-a3b8-de028e0f0123
title: Usar las barras de herramientas del escritorio de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140ef94c1daeb571cd0d766dfbd4dc28b7991efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153922"
---
# <a name="using-application-desktop-toolbars"></a>Usar las barras de herramientas del escritorio de la aplicación

Una *barra de herramientas del escritorio* de la aplicación (también denominada Appbar) es una ventana similar a la barra de tareas de Windows. Está anclado a un borde de la pantalla y normalmente contiene botones que proporcionan al usuario acceso rápido a otras aplicaciones y ventanas. El sistema impide que otras aplicaciones utilicen el área de escritorio utilizada por un Appbar. Puede haber cualquier número de appbars en el escritorio en un momento dado.

En este tema se incluyen las siguientes secciones.

-   [Acerca de las barras de herramientas del escritorio de la aplicación](#about-application-desktop-toolbars)
    -   [Envío de mensajes](#sending-messages)
    -   [Registro](#registration)
    -   [Tamaño y posición de Appbar](#appbar-size-and-position)
    -   [Ocultar automáticamente las barras de herramientas del escritorio de la aplicación](#autohide-application-desktop-toolbars)
    -   [Mensajes de notificación de Appbar](#appbar-notification-messages)
-   [Registro de una barra de herramientas del escritorio de la aplicación](#registering-an-application-desktop-toolbar)
-   [Establecer el tamaño y la posición de Appbar](#setting-the-appbar-size-and-position)
-   [Procesamiento de mensajes de notificación de Appbar](#processing-appbar-notification-messages)

## <a name="about-application-desktop-toolbars"></a>Acerca de las barras de herramientas del escritorio de la aplicación

Windows proporciona una API que le permite aprovechar los servicios de Appbar proporcionados por el sistema. Los servicios ayudan a garantizar que los appbars definidos por la aplicación funcionan sin problemas entre sí y con la barra de tareas. El sistema mantiene información sobre cada Appbar y envía los mensajes appbars para notificarles los eventos que pueden afectar a su tamaño, posición y apariencia.

### <a name="sending-messages"></a>enviar mensajes

Una aplicación utiliza un conjunto especial de mensajes, denominados mensajes de Appbar, para agregar o quitar un Appbar, establecer el tamaño y la posición de una Appbar y recuperar información sobre el tamaño, la posición y el estado de la barra de tareas. Para enviar un mensaje de Appbar, una aplicación debe usar la función [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) . Los parámetros de la función incluyen un identificador de mensaje, como [**ABN \_ New**](abm-new.md), y la dirección de una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Los miembros de la estructura contienen información que el sistema necesita para procesar el mensaje dado.

Para un mensaje de Appbar determinado, el sistema usa algunos miembros de la estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) y omite los demás. Sin embargo, el sistema siempre usa los miembros **cbSize** y **hWnd** , por lo que una aplicación debe rellenar estos miembros para cada mensaje de Appbar. El miembro **cbSize** especifica el tamaño de la estructura y el miembro **hWnd** es el identificador de la ventana de Appbar.

Algunos mensajes de Appbar solicitan información del sistema. Al procesar estos mensajes, el sistema copia la información solicitada en la estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .

### <a name="registration"></a>Registro

El sistema mantiene una lista interna de appbars y mantiene información sobre cada barra de la lista. El sistema utiliza la información para administrar appbars, realizar servicios para ellos y enviarles mensajes de notificación.

Una aplicación debe registrar un Appbar (es decir, agregarlo a la lista interna) para poder recibir los servicios de Appbar del sistema. Para registrar un Appbar, una aplicación envía el [**\_ nuevo mensaje ABN**](abm-new.md) . La estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) adjunta incluye el identificador de la ventana de Appbar y un identificador de mensaje definido por la aplicación. El sistema utiliza el identificador de mensaje para enviar mensajes de notificación al procedimiento de ventana de la ventana de Appbar. Para obtener más información, consulte mensajes de notificación de Appbar.

Una aplicación anula el registro de una Appbar mediante el envío del mensaje [**ABN \_ Remove**](abm-remove.md) . Al anular el registro de un control Appbar, se quita de la lista interna de appbars del sistema. El sistema ya no envía mensajes de notificación al Appbar o impide que otras aplicaciones utilicen el área de pantalla utilizada por el Appbar. Una aplicación siempre debe enviar **ABN \_ Remove** antes de destruir un Appbar.

### <a name="appbar-size-and-position"></a>Tamaño y posición de Appbar

Una aplicación debe establecer el tamaño y la posición de una Appbar para que no interfiera con ningún otro appbars o la barra de tareas. Cada Appbar debe estar anclado a un borde determinado de la pantalla y varios appbars se pueden anclar a un borde. Sin embargo, si un Appbar está anclado al mismo borde que la barra de tareas, el sistema garantiza que la barra de tareas esté siempre en el borde más externo.

Para establecer el tamaño y la posición de un Appbar, una aplicación propone primero un borde de pantalla y un rectángulo delimitador para el Appbar mediante el envío del mensaje [**\_ QUERYPOS de ABN**](abm-querypos.md) . El sistema determina si la barra de tareas u otro Appbar usa cualquier parte del área de la pantalla del rectángulo propuesto, ajusta el rectángulo (si es necesario) y devuelve el rectángulo ajustado a la aplicación.

A continuación, la aplicación envía el mensaje [**\_ SETPOS de ABN**](abm-setpos.md) para establecer el nuevo rectángulo delimitador para el Appbar. De nuevo, el sistema puede ajustar el rectángulo antes de devolverlo a la aplicación. Por esta razón, la aplicación debe usar el rectángulo ajustado que devuelve **ABN \_ SETPOS** para establecer el tamaño y la posición finales. La aplicación puede usar la función [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) para mover el control Appbar a la posición.

Mediante el uso de un proceso de dos pasos para establecer el tamaño y la posición, el sistema permite que la aplicación proporcione comentarios intermedios al usuario durante la operación de movimiento. Por ejemplo, si el usuario arrastra un Appbar, es posible que la aplicación muestre un rectángulo sombreado que indica la nueva posición antes de que se mueva realmente el control Appbar.

Una aplicación debe establecer el tamaño y la posición de su Appbar después de registrarlo y siempre que el Appbar reciba el mensaje de notificación [**ABN \_ POSCHANGED**](abn-poschanged.md) . Un control Appbar recibe este mensaje de notificación cada vez que se produce un cambio en el tamaño, la posición o el estado de visibilidad de la barra de tareas y siempre que se cambia el tamaño, se agrega o se quita otro Appbar en el mismo lado de la pantalla.

Cada vez que un Appbar recibe el mensaje de activación de WM \_ , debe enviar el mensaje de [**\_ activación de ABN**](abm-activate.md) . Del mismo modo, cuando un Appbar recibe un mensaje de WINDOWPOSCHANGED de WM \_ , debe llamar a [**ABN \_ WINDOWPOSCHANGED**](abm-windowposchanged.md). El envío de estos mensajes garantiza que el sistema establezca correctamente el orden z de cualquier appbars de autoocultar en el mismo borde.

### <a name="autohide-application-desktop-toolbars"></a>Ocultar automáticamente las barras de herramientas del escritorio de la aplicación

Un Appbar de ocultación automáticamente es aquél que normalmente está oculto, pero se vuelve visible cuando el usuario mueve el cursor del mouse al borde de la pantalla con el que está asociado el Appbar. El Appbar se oculta de nuevo cuando el usuario mueve el cursor del mouse fuera del rectángulo delimitador de la barra.

Aunque el sistema permite una serie de appbars diferentes en un momento dado, solo permite un Appbar de ocultación automáticamente cada vez para cada margen de la pantalla, en función de la primera vez que se atiende. El sistema mantiene automáticamente el orden z de un Appbar de ocultación automática (solo dentro de su grupo de orden z).

Una aplicación utiliza el [**mensaje \_ SETAUTOHIDEBAR de ABN**](abm-setautohidebar.md) para registrar o anular el registro de un Appbar de ocultación. El mensaje especifica el borde del Appbar y una marca que especifica si se va a registrar o anular el registro de la Appbar. Se produce un error en el mensaje si se está registrando un Appbar de ocultación automáticamente pero uno ya está asociado al borde especificado. Una aplicación puede recuperar el identificador del Appbar de ocultación automáticamente asociado a un borde mediante el envío del mensaje [**\_ GETAUTOHIDEBAR de ABN**](abm-getautohidebar.md) .

No es necesario que el Appbar oculto se registre como un Appbar normal; es decir, no es necesario que se registre mediante el envío del [**\_ nuevo mensaje ABN**](abm-new.md) . Un Appbar que no está registrado por **ABN \_ nuevo** superpone cualquier appbars anclado en el mismo borde de la pantalla.

### <a name="appbar-notification-messages"></a>Mensajes de notificación de Appbar

El sistema envía mensajes para notificar a un Appbar sobre eventos que pueden afectar a su posición y apariencia. Los mensajes se envían en el contexto de un mensaje definido por la aplicación. La aplicación especifica el identificador del mensaje cuando envía el [**\_ nuevo mensaje ABN**](abm-new.md) para registrar el Appbar. El código de notificación está en el parámetro *wParam* del mensaje definido por la aplicación.

Un Appbar recibe el mensaje de notificación [**ABN \_ POSCHANGED**](abn-poschanged.md) cuando cambia el tamaño, la posición o el estado de visibilidad de la barra de tareas, cuando se agrega otro Appbar al mismo borde de la pantalla, o cuando se cambia el tamaño o se quita otro Appbar en el mismo borde de la pantalla. Un Appbar debe responder a este mensaje de notificación mediante el envío de mensajes [**ABN \_ QUERYPOS**](abm-querypos.md) y [**ABN \_ SETPOS**](abm-setpos.md) . Si ha cambiado la posición de una Appbar, debe llamar a la función [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) para moverla a la nueva posición.

El sistema envía el mensaje de notificación [**ABN \_ STATECHANGE**](abn-statechange.md) siempre que haya cambiado el estado de ocultación automática o siempre visible de la barra de tareas, es decir, cuando el usuario activa o desactiva la casilla de verificación Mostrar **siempre visible** o **Ocultar automáticamente** en la hoja de propiedades de la barra de tareas. Un Appbar puede usar este mensaje de notificación para establecer su estado de conformidad con el de la barra de tareas, si lo desea.

Cuando se inicia una aplicación de pantalla completa o cuando se cierra la última aplicación de pantalla completa, un Appbar recibe el mensaje de notificación [**ABN \_ FULLSCREENAPP**](abn-fullscreenapp.md) . El parámetro *lParam* indica si la aplicación de pantalla completa se está abriendo o cerrando. Si se está abriendo, el Appbar debe colocarse en la parte inferior del orden z. El Appbar debe restaurar su posición en el orden z cuando se cierre la última aplicación de pantalla completa.

Un Appbar recibe el mensaje de notificación [**ABN \_ WINDOWARRANGE**](abn-windowarrange.md) cuando el usuario selecciona el comando Cascade, Tile horizontalmente o mosaicos verticalmente en el menú contextual de la barra de tareas. El sistema envía el mensaje dos veces, antes de reorganizar las ventanas (*lParam* es **true**) y después de organizar las ventanas (*lParam* es **false**).

Un Appbar puede usar los mensajes de [**ABN \_ WINDOWARRANGE**](abn-windowarrange.md) para excluirse de la operación en cascada o de mosaico. Para excluirse, el Appbar debe ocultarse cuando *lParam* es **true** y mostrarse cuando *lParam* es **false**. Si una Appbar se oculta en respuesta a este mensaje, no es necesario enviar los mensajes [**ABN \_ QUERYPOS**](abm-querypos.md) y [**ABN \_ SETPOS**](abm-setpos.md) en respuesta a la operación Cascade o Tile.

## <a name="registering-an-application-desktop-toolbar"></a>Registro de una barra de herramientas del escritorio de la aplicación

Una aplicación debe registrar un Appbar mediante el envío [**del \_ nuevo mensaje ABN**](abm-new.md) . El registro de un Appbar lo agrega a la lista interna del sistema y proporciona al sistema un identificador de mensaje que se usa para enviar mensajes de notificación al Appbar. Antes de salir, una aplicación debe anular el registro de la Appbar mediante el envío del mensaje [**ABN \_ Remove**](abm-remove.md) . Al anular el registro se quita el Appbar de la lista interna del sistema y se impide que la barra reciba mensajes de notificación de Appbar.

La función del ejemplo siguiente registra o anula el registro de un Appbar, dependiendo del valor de un parámetro de marca Boolean.


```C++
// RegisterAccessBar - registers or unregisters an appbar. 
// Returns TRUE if successful, or FALSE otherwise. 

// hwndAccessBar - handle to the appbar 
// fRegister - register and unregister flag 

// Global variables 
//     g_uSide - screen edge (defaults to ABE_TOP) 
//     g_fAppRegistered - flag indicating whether the bar is registered 

BOOL RegisterAccessBar(HWND hwndAccessBar, BOOL fRegister) 
{ 
    APPBARDATA abd; 
    
    // An application-defined message identifier
    APPBAR_CALLBACK = (WM_USER + 0x01);
    
    // Specify the structure size and handle to the appbar. 
    abd.cbSize = sizeof(APPBARDATA); 
    abd.hWnd = hwndAccessBar; 

    if (fRegister) 
    { 
        // Provide an identifier for notification messages. 
        abd.uCallbackMessage = APPBAR_CALLBACK; 

        // Register the appbar. 
        if (!SHAppBarMessage(ABM_NEW, &abd)) 
            return FALSE; 

        g_uSide = ABE_TOP;       // default edge 
        g_fAppRegistered = TRUE; 

    } 
    else 
    { 
        // Unregister the appbar. 
        SHAppBarMessage(ABM_REMOVE, &abd); 
        g_fAppRegistered = FALSE; 
    } 

    return TRUE; 
}
```



## <a name="setting-the-appbar-size-and-position"></a>Establecer el tamaño y la posición de Appbar

Una aplicación debe establecer el tamaño y la posición de una Appbar después de registrar el Appbar, después de que el usuario del usuario mueva o cambie el tamaño de la Appbar y siempre que el Appbar reciba el mensaje de notificación [**ABN \_ POSCHANGED**](abn-poschanged.md) . Antes de establecer el tamaño y la posición del Appbar, la aplicación consulta el sistema para obtener un rectángulo delimitador aprobado mediante el envío del mensaje [**\_ QUERYPOS de ABN**](abm-querypos.md) . El sistema devuelve un rectángulo delimitador que no interfiere con la barra de tareas ni con ningún otro Appbar. El sistema ajusta el rectángulo únicamente mediante la resta de rectángulos; no realiza ningún esfuerzo para conservar el tamaño inicial del rectángulo. Por esta razón, el Appbar debe volver a ajustar el rectángulo, según sea necesario, después de enviar **ABN \_ QUERYPOS**.

A continuación, la aplicación vuelve a pasar el rectángulo delimitador al sistema mediante el mensaje [**\_ SETPOS de ABN**](abm-setpos.md) . A continuación, llama a la función [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) para mover el control Appbar a la posición.

En el ejemplo siguiente se muestra cómo establecer el tamaño y la posición de una Appbar.


```C++
// AppBarQuerySetPos - sets the size and position of an appbar. 

// uEdge - screen edge to which the appbar is to be anchored 
// lprc - current bounding rectangle of the appbar 
// pabd - address of the APPBARDATA structure with the hWnd and cbSize members filled

void PASCAL AppBarQuerySetPos(UINT uEdge, LPRECT lprc, PAPPBARDATA pabd) 
{ 
    int iHeight = 0; 
    int iWidth = 0; 

    pabd->rc = *lprc; 
    pabd->uEdge = uEdge; 

    // Copy the screen coordinates of the appbar's bounding 
    // rectangle into the APPBARDATA structure. 
    if ((uEdge == ABE_LEFT) || (uEdge == ABE_RIGHT)) 
    { 
        iWidth = pabd->rc.right - pabd->rc.left; 
        pabd->rc.top = 0; 
        pabd->rc.bottom = GetSystemMetrics(SM_CYSCREEN); 
    } 
    else 
    { 
        iHeight = pabd->rc.bottom - pabd->rc.top; 
        pabd->rc.left = 0; 
        pabd->rc.right = GetSystemMetrics(SM_CXSCREEN); 
    } 

    // Query the system for an approved size and position. 
    SHAppBarMessage(ABM_QUERYPOS, pabd); 

    // Adjust the rectangle, depending on the edge to which the appbar is anchored.
    switch (uEdge) 
    { 
        case ABE_LEFT: 
            pabd->rc.right = pabd->rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            pabd->rc.left = pabd->rc.right - iWidth; 
            break; 

        case ABE_TOP: 
            pabd->rc.bottom = pabd->rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            pabd->rc.top = pabd->rc.bottom - iHeight; 
            break; 
    } 

    // Pass the final bounding rectangle to the system. 
    SHAppBarMessage(ABM_SETPOS, pabd); 

    // Move and size the appbar so that it conforms to the 
    // bounding rectangle passed to the system. 
    MoveWindow(pabd->hWnd, 
               pabd->rc.left, 
               pabd->rc.top, 
               pabd->rc.right - pabd->rc.left, 
               pabd->rc.bottom - pabd->rc.top, 
               TRUE); 

}
```



## <a name="processing-appbar-notification-messages"></a>Procesamiento de mensajes de notificación de Appbar

Un control Appbar recibe un mensaje de notificación cuando cambia el estado de la barra de tareas, cuando se inicia una aplicación de pantalla completa (o cuando se cierra la última) o cuando se produce un evento que puede afectar al tamaño y la posición de Appbar. En el ejemplo siguiente se muestra cómo procesar los distintos mensajes de notificación.


```C++
// AppBarCallback - processes notification messages sent by the system. 

// hwndAccessBar - handle to the appbar 
// uNotifyMsg - identifier of the notification message 
// lParam - message parameter 

void AppBarCallback(HWND hwndAccessBar, UINT uNotifyMsg, 
    LPARAM lParam) 
{ 
    APPBARDATA abd; 
    UINT uState; 

    abd.cbSize = sizeof(abd); 
    abd.hWnd = hwndAccessBar; 

    switch (uNotifyMsg) 
    { 
        case ABN_STATECHANGE: 

            // Check to see if the taskbar's always-on-top state has changed
            // and, if it has, change the appbar's state accordingly.
            uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

            SetWindowPos(hwndAccessBar, 
                         (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                         0, 0, 0, 0, 
                         SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 

            break; 

        case ABN_FULLSCREENAPP: 

            // A full-screen application has started, or the last full-screen
            // application has closed. Set the appbar's z-order appropriately.
            if (lParam) 
            { 
                SetWindowPos(hwndAccessBar, 
                             (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                             0, 0, 0, 0, 
                             SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 
            else 
            { 
                uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

                if (uState & ABS_ALWAYSONTOP) 
                    SetWindowPos(hwndAccessBar, 
                                 HWND_TOPMOST, 
                                 0, 0, 0, 0, 
                                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 

        case ABN_POSCHANGED: 

            // The taskbar or another appbar has changed its size or position.
            AppBarPosChanged(&abd); 
            break; 
    } 
}
```



La función siguiente ajusta el rectángulo de delimitación de una Appbar y, a continuación, llama a la función AppBarQuerySetPos definida por la aplicación (incluida en la sección anterior) para establecer el tamaño y la posición de la barra según corresponda.


```C++
// AppBarPosChanged - adjusts the appbar's size and position. 

// pabd - address of an APPBARDATA structure that contains information 
//        used to adjust the size and position. 

void PASCAL AppBarPosChanged(PAPPBARDATA pabd) 
{ 
    RECT rc; 
    RECT rcWindow; 
    int iHeight; 
    int iWidth; 

    rc.top = 0; 
    rc.left = 0; 
    rc.right = GetSystemMetrics(SM_CXSCREEN); 
    rc.bottom = GetSystemMetrics(SM_CYSCREEN); 

    GetWindowRect(pabd->hWnd, &rcWindow); 

    iHeight = rcWindow.bottom - rcWindow.top; 
    iWidth = rcWindow.right - rcWindow.left; 

    switch (g_uSide) 
    { 
        case ABE_TOP: 
            rc.bottom = rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            rc.top = rc.bottom - iHeight; 
            break; 

        case ABE_LEFT: 
            rc.right = rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            rc.left = rc.right - iWidth; 
            break; 
    } 

    AppBarQuerySetPos(g_uSide, &rc, pabd); 
}
```



 

 
