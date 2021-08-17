---
description: Una barra de herramientas de escritorio de la aplicación (también denominada barra de aplicaciones) es una ventana similar a la Windows de tareas.
ms.assetid: d9f63cb1-e2cc-4a3b-a3b8-de028e0f0123
title: Uso de barras de herramientas de escritorio de aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c8604136040f5f3a1b4c1e9fcecb3b0c26b087724f477e592857ca4046d3a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351455"
---
# <a name="using-application-desktop-toolbars"></a>Uso de barras de herramientas de escritorio de aplicaciones

Una *barra de herramientas de escritorio de* la aplicación (también denominada barra de aplicaciones) es una ventana similar a la Windows de tareas. Está anclado a un borde de la pantalla y normalmente contiene botones que dan al usuario acceso rápido a otras aplicaciones y ventanas. El sistema impide que otras aplicaciones utilicen el área de escritorio que usa una barra de aplicaciones. Cualquier número de barras de aplicaciones puede existir en el escritorio en un momento dado.

En este tema se incluyen las siguientes secciones.

-   [Acerca de las barras de herramientas de Escritorio de aplicaciones](#about-application-desktop-toolbars)
    -   [Envío de mensajes](#sending-messages)
    -   [Registro](#registration)
    -   [Tamaño y posición de la barra de aplicaciones](#appbar-size-and-position)
    -   [Mostrar automáticamente las barras de herramientas de escritorio de aplicaciones](#autohide-application-desktop-toolbars)
    -   [Mensajes de notificación de la barra de aplicaciones](#appbar-notification-messages)
-   [Registro de una barra de herramientas de Escritorio de aplicaciones](#registering-an-application-desktop-toolbar)
-   [Establecer el tamaño y la posición de la barra de aplicaciones](#setting-the-appbar-size-and-position)
-   [Procesamiento de mensajes de notificación de la barra de aplicaciones](#processing-appbar-notification-messages)

## <a name="about-application-desktop-toolbars"></a>Acerca de las barras de herramientas de Escritorio de aplicaciones

Windows proporciona una API que le permite aprovechar los servicios de la barra de aplicaciones proporcionados por el sistema. Los servicios ayudan a garantizar que las barras de aplicaciones definidas por la aplicación funcionan sin problemas entre sí y con la barra de tareas. El sistema mantiene información sobre cada barra de aplicaciones y envía los mensajes de las barras de aplicaciones para notificarles sobre eventos que pueden afectar a su tamaño, posición y apariencia.

### <a name="sending-messages"></a>enviar mensajes

Una aplicación usa un conjunto especial de mensajes, denominados mensajes de la barra de aplicaciones, para agregar o quitar una barra de aplicaciones, establecer el tamaño y la posición de una barra de aplicaciones y recuperar información sobre el tamaño, la posición y el estado de la barra de tareas. Para enviar un mensaje de la barra de aplicaciones, una aplicación debe usar la [**función SHAppBarMessage.**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) Los parámetros de la función incluyen un identificador de mensaje, como [**ABM \_ NEW,**](abm-new.md)y la dirección de una [**estructura APPBARDATA.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) Los miembros de la estructura contienen información que el sistema necesita para procesar el mensaje dado.

Para cualquier mensaje de la barra de aplicaciones determinado, el sistema usa algunos miembros de la estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) y omite los demás. Sin embargo, el sistema siempre usa **los miembros cbSize** y **hWnd,** por lo que una aplicación debe rellenar estos miembros para cada mensaje de la barra de aplicaciones. El **miembro cbSize** especifica el tamaño de la estructura y el **miembro hWnd** es el identificador de la ventana de la barra de aplicaciones.

Algunos mensajes de la barra de aplicaciones solicitan información del sistema. Al procesar estos mensajes, el sistema copia la información solicitada en la [**estructura APPBARDATA.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)

### <a name="registration"></a>Registro

El sistema mantiene una lista interna de barras de aplicaciones y mantiene información sobre cada barra de la lista. El sistema usa la información para administrar las barras de aplicaciones, realizar servicios para ellas y enviarles mensajes de notificación.

Una aplicación debe registrar una barra de aplicaciones (es decir, agregarla a la lista interna) para poder recibir servicios de la barra de aplicaciones del sistema. Para registrar una barra de aplicaciones, una aplicación envía el [**mensaje ABM \_ NEW.**](abm-new.md) La estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que lo acompaña incluye el identificador de la ventana de la barra de aplicaciones y un identificador de mensaje definido por la aplicación. El sistema usa el identificador de mensaje para enviar mensajes de notificación al procedimiento de ventana de la ventana de la barra de aplicaciones. Para obtener más información, vea Mensajes de notificación de la barra de aplicaciones.

Una aplicación anula el registro de una barra de aplicaciones mediante el envío del [**mensaje \_ REMOVE de ABM.**](abm-remove.md) Al anular el registro de una barra de aplicaciones, se quita de la lista interna del sistema de barras de aplicaciones. El sistema ya no envía mensajes de notificación a la barra de aplicaciones o impide que otras aplicaciones utilicen el área de pantalla que usa la barra de aplicaciones. Una aplicación siempre debe enviar **ABM \_ REMOVE antes** de destruir una barra de aplicaciones.

### <a name="appbar-size-and-position"></a>Tamaño y posición de la barra de aplicaciones

Una aplicación debe establecer el tamaño y la posición de una barra de aplicaciones para que no interfiera con ninguna otra barra de aplicaciones ni con la barra de tareas. Cada barra de aplicaciones debe estar anclada a un borde determinado de la pantalla y varias barras de aplicaciones se pueden delimitar a un borde. Sin embargo, si una barra de aplicaciones está anclada al mismo borde que la barra de tareas, el sistema garantiza que la barra de tareas siempre está en el borde más externo.

Para establecer el tamaño y la posición de una barra de aplicaciones, una aplicación propone primero un borde de pantalla y un rectángulo delimitador para la barra de aplicaciones mediante el envío del mensaje [**\_ ABM QUERYPOS.**](abm-querypos.md) El sistema determina si la barra de tareas u otra barra de aplicaciones usa alguna parte del área de pantalla dentro del rectángulo propuesto, ajusta el rectángulo (si es necesario) y devuelve el rectángulo ajustado a la aplicación.

A continuación, la aplicación envía el [**mensaje \_ SETPOS**](abm-setpos.md) de ABM para establecer el nuevo rectángulo delimitador para la barra de aplicaciones. De nuevo, el sistema puede ajustar el rectángulo antes de devolverlo a la aplicación. Por este motivo, la aplicación debe usar el rectángulo ajustado devuelto por **ABM \_ SETPOS** para establecer el tamaño y la posición finales. La aplicación puede usar la [**función MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) para mover la barra de aplicaciones a su posición.

Mediante el uso de un proceso de dos pasos para establecer el tamaño y la posición, el sistema permite que la aplicación proporcione comentarios intermedios al usuario durante la operación de traslado. Por ejemplo, si el usuario arrastra una barra de aplicaciones, la aplicación podría mostrar un rectángulo sombreado que indica la nueva posición antes de que la barra de aplicaciones se mueva realmente.

Una aplicación debe establecer el tamaño y la posición de su barra de aplicaciones después de registrarla y cada vez que la barra de aplicaciones recibe el mensaje de [**notificación \_ POSCHANGED de ABN.**](abn-poschanged.md) Una barra de aplicaciones recibe este mensaje de notificación cada vez que se produce un cambio en el tamaño, la posición o el estado de visibilidad de la barra de tareas y cada vez que se cambia el tamaño, se agrega o se quita otra barra de aplicaciones en el mismo lado de la pantalla.

Cada vez que una barra de aplicaciones recibe el mensaje WM \_ ACTIVATE, debe enviar el [**mensaje ABM \_ ACTIVATE.**](abm-activate.md) De forma similar, cuando una barra de aplicaciones recibe un mensaje WM WINDOWPOSCHANGED, debe llamar a \_ [**ABM \_ WINDOWPOSCHANGED**](abm-windowposchanged.md). El envío de estos mensajes garantiza que el sistema establece correctamente el orden Z de cualquier barra de aplicaciones de autohide en el mismo borde.

### <a name="autohide-application-desktop-toolbars"></a>Mostrar automáticamente las barras de herramientas de escritorio de aplicaciones

Una barra de aplicaciones de mostrar automáticamente es aquella que normalmente está oculta, pero que se vuelve visible cuando el usuario mueve el cursor del mouse al borde de la pantalla con el que está asociada la barra de aplicaciones. La barra de aplicaciones se oculta de nuevo cuando el usuario mueve el cursor del mouse fuera del rectángulo delimitador de la barra.

Aunque el sistema permite varias barras de aplicaciones diferentes en un momento dado, solo permite mostrar automáticamente la barra de aplicaciones a la vez para cada borde de la pantalla por primera vez y por primera vez. El sistema mantiene automáticamente el orden Z de una barra de aplicaciones de mostrar automáticamente (solo dentro de su grupo de orden Z).

Una aplicación usa el [**mensaje \_ SETAUTOHIDEBAR**](abm-setautohidebar.md) de ABM para registrar o anular el registro de una barra de aplicaciones autohide. El mensaje especifica el borde de la barra de aplicaciones y una marca que especifica si la barra de aplicaciones se va a registrar o anular el registro. Se produce un error en el mensaje si se está registrando una barra de aplicaciones de autohide, pero ya hay una asociada al borde especificado. Una aplicación puede recuperar el identificador en la barra de aplicaciones de autohide asociada a un borde mediante el envío del mensaje [**\_ GETAUTOHIDEBAR de ABM.**](abm-getautohidebar.md)

Una barra de aplicaciones autohide no necesita registrarse como una barra de aplicaciones normal; Es decir, no es necesario registrarlo mediante el envío del [**mensaje ABM \_ NEW.**](abm-new.md) Una barra de aplicaciones que no está registrada por **ABM \_ NEW** se superpone a las barras de aplicaciones ancladas en el mismo borde de la pantalla.

### <a name="appbar-notification-messages"></a>Mensajes de notificación de la barra de aplicaciones

El sistema envía mensajes para notificar a una barra de aplicaciones los eventos que pueden afectar a su posición y apariencia. Los mensajes se envían en el contexto de un mensaje definido por la aplicación. La aplicación especifica el identificador del mensaje cuando envía el [**mensaje ABM \_ NEW**](abm-new.md) para registrar la barra de aplicaciones. El código de notificación está en *el parámetro wParam* del mensaje definido por la aplicación.

Una barra de aplicaciones recibe el mensaje de notificación [**\_ ABN POSCHANGED**](abn-poschanged.md) cuando cambia el tamaño, la posición o el estado de visibilidad de la barra de tareas, cuando se agrega otra barra de aplicaciones al mismo borde de la pantalla o cuando se cambia el tamaño o se quita otra barra de aplicaciones en el mismo borde de la pantalla. Una barra de aplicaciones debe responder a este mensaje de notificación mediante el envío [**de mensajes ABM \_ QUERYPOS**](abm-querypos.md) y [**ABM \_ SETPOS.**](abm-setpos.md) Si la posición de una barra de aplicaciones ha cambiado, debe llamar a la [**función MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) para moverse a la nueva posición.

El sistema envía el mensaje de notificación  [**\_ ABN STATECHANGE**](abn-statechange.md) cada vez que ha cambiado el estado de mostrar automáticamente o siempre  en la parte superior de la barra de tareas, es decir, cuando el usuario activa o borra la casilla Ocultar siempre en la parte superior u Ocultar automáticamente en la hoja de propiedades de la barra de tareas. Una barra de aplicaciones puede usar este mensaje de notificación para establecer su estado para que se ajuste al de la barra de tareas, si lo desea.

Cuando se inicia una aplicación de pantalla completa o cuando se cierra la última aplicación de pantalla completa, una barra de aplicaciones recibe el mensaje de notificación [**\_ ABN FULLSCREENAPP.**](abn-fullscreenapp.md) El *parámetro lParam* indica si la aplicación de pantalla completa se está abriendo o cerrando. Si se abre, la barra de aplicaciones debe colocarse en la parte inferior del orden Z. La barra de aplicaciones debe restaurar su posición de orden Z cuando se haya cerrado la última aplicación de pantalla completa.

Una barra de aplicaciones recibe el mensaje de notificación [**ABN \_ WINDOWARRANGE**](abn-windowarrange.md) cuando el usuario selecciona los comandos Cascada, Mosaico horizontal o Mosaico vertical en el menú contextual de la barra de tareas. El sistema envía el mensaje dos veces, antes de reorganizar las ventanas *(lParam* es **TRUE**) y después de organizar las ventanas (*lParam* es **FALSE**).

Una barra de aplicaciones puede usar [**mensajes \_ ABN WINDOWARRANGE**](abn-windowarrange.md) para excluirse de la operación en cascada o de mosaico. Para excluirse, la barra de aplicaciones debe ocultarse cuando *lParam* es **TRUE** y mostrarse cuando *lParam* es **FALSE.** Si una barra de aplicaciones se oculta en respuesta a este mensaje, no es necesario enviar los mensajes [**ABM \_ QUERYPOS**](abm-querypos.md) y [**ABM \_ SETPOS**](abm-setpos.md) en respuesta a la operación en cascada o en mosaico.

## <a name="registering-an-application-desktop-toolbar"></a>Registro de una barra de herramientas de Escritorio de aplicaciones

Una aplicación debe registrar una barra de aplicaciones mediante el envío del [**mensaje ABM \_ NEW.**](abm-new.md) El registro de una barra de aplicaciones lo agrega a la lista interna del sistema y proporciona al sistema un identificador de mensaje que se usará para enviar mensajes de notificación a la barra de aplicaciones. Antes de salir, una aplicación debe anular el registro de la barra de aplicaciones mediante el envío del [**mensaje \_ REMOVE de ABM.**](abm-remove.md) Al anular el registro, se quita la barra de aplicaciones de la lista interna del sistema y se impide que la barra reciba mensajes de notificación de la barra de aplicaciones.

La función del ejemplo siguiente registra o anula el registro de una barra de aplicaciones, en función del valor de un parámetro de marca booleano.


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



## <a name="setting-the-appbar-size-and-position"></a>Establecer el tamaño y la posición de la barra de aplicaciones

Una aplicación debe establecer el tamaño y la posición de una barra de aplicaciones después de registrar la barra de aplicaciones, después de que el usuario mueva o ajuste el tamaño de la barra de aplicaciones y siempre que la barra de aplicaciones reciba el mensaje de notificación [**\_ ABN POSCHANGED.**](abn-poschanged.md) Antes de establecer el tamaño y la posición de la barra de aplicaciones, la aplicación consulta al sistema un rectángulo delimitador aprobado mediante el envío del [**mensaje \_ QUERYPOS de ABM.**](abm-querypos.md) El sistema devuelve un rectángulo delimitador que no interfiere con la barra de tareas ni con ninguna otra barra de aplicaciones. El sistema ajusta el rectángulo puramente por resta de rectángulo; no hace ningún esfuerzo por conservar el tamaño inicial del rectángulo. Por este motivo, la barra de aplicaciones debe reajustar el rectángulo, según sea necesario, después de enviar **ABM \_ QUERYPOS**.

A continuación, la aplicación pasa el rectángulo delimitador al sistema mediante el [**mensaje \_ SETPOS de ABM.**](abm-setpos.md) A continuación, llama a [**la función MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) para mover la barra de aplicaciones a su posición.

En el ejemplo siguiente se muestra cómo establecer el tamaño y la posición de una barra de aplicaciones.


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



## <a name="processing-appbar-notification-messages"></a>Procesamiento de mensajes de notificación de la barra de aplicaciones

Una barra de aplicaciones recibe un mensaje de notificación cuando cambia el estado de la barra de tareas, cuando se inicia una aplicación de pantalla completa (o se cierra la última) o cuando se produce un evento que puede afectar al tamaño y la posición de la barra de aplicaciones. En el ejemplo siguiente se muestra cómo procesar los distintos mensajes de notificación.


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



La función siguiente ajusta el rectángulo delimitador de una barra de aplicaciones y, a continuación, llama a la función AppBarQuerySetPos definida por la aplicación (incluida en la sección anterior) para establecer el tamaño y la posición de la barra en consecuencia.


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



 

 
