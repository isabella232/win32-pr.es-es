---
description: La interfaz de Windows incluye una barra de herramientas especial del escritorio de la aplicación denominada barra de tareas. Puede usar la barra de tareas para tareas como cambiar entre ventanas abiertas e iniciar nuevas aplicaciones.
ms.assetid: 14d520e7-7c15-441d-9662-24b972d208ac
title: La barra de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cce37991c6265f02ab92ece62dbae341031d272a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997852"
---
# <a name="the-taskbar"></a>La barra de tareas

La interfaz de Windows incluye una [barra de herramientas](application-desktop-toolbars.md) especial del escritorio de la aplicación denominada *barra de tareas*. Puede usar la barra de tareas para tareas como cambiar entre ventanas abiertas e iniciar nuevas aplicaciones.

> [!Note]  
> Para obtener información sobre los cambios realizados en la barra de tareas a partir de Windows 7, vea extensiones de la [barra de tareas](taskbar-extensions.md).

 

En este tema se incluyen las siguientes secciones.

-   [Acerca de la barra de tareas](#about-the-taskbar)
    -   [Opciones de presentación de la barra de tareas](#taskbar-display-options)
    -   [Agregar accesos directos al menú Inicio](#adding-shortcuts-to-the-start-menu)
    -   [Administrar botones de la barra de tareas](#managing-taskbar-buttons)
    -   [Agregar, modificar y eliminar iconos en el área de notificación](#adding-modifying-and-deleting-icons-in-the-notification-area)
    -   [Notificación de creación de la barra de tareas](#taskbar-creation-notification)
-   [Uso de la barra de tareas](#using-the-taskbar)
    -   [Agregar y eliminar iconos de la barra de tareas en el área de notificación](#adding-and-deleting-taskbar-icons-in-the-notification-area)
    -   [Recibir eventos del mouse](#receiving-mouse-events)

## <a name="about-the-taskbar"></a>Acerca de la barra de tareas

La barra de tareas incluye lo siguiente:

-   Menú **Inicio**
-   Barra de inicio rápido (solo Windows Vista y versiones anteriores)
-   Botones de la barra de tareas
-   Barras de herramientas (opcional)
-   Área de notificaciones

El menú **Inicio** contiene comandos que pueden tener acceso a programas, documentos y configuraciones. Estos comandos incluyen **todos los programas**, **documentos**, **Panel de control**, **juegos**, **ayuda y soporte técnico**, **apagar** y **Buscar programas y archivos**.

El **Inicio** en versiones anteriores de Windows contenía elementos como **Buscar** y **Ejecutar**, la funcionalidad de que se incluía en **Buscar programas y archivos** en Windows Vista y versiones posteriores.

La barra de inicio rápido, disponible en versiones de Windows anteriores a Windows 7, contiene accesos directos a las aplicaciones. Windows proporciona entradas predeterminadas, como Windows Internet Explorer, y el usuario puede agregar más accesos directos que elijan. Los iconos de esta área responden a un solo clic. En Windows 7 y versiones posteriores, esta funcionalidad se incluye en los botones de la barra de tareas.

El shell coloca un botón en la barra de tareas cada vez que una aplicación crea una ventana sin propiedad, es decir, una ventana que no tiene un elemento primario y que tiene los bits de estilo extendido adecuados (consulte Administración de los botones de la [barra de tareas](#managing-taskbar-buttons), más abajo). Para cambiar a una ventana, el usuario hace clic en su botón de ventana. Esta funcionalidad se ha expandido en gran medida a partir de Windows 7. Para obtener más información, vea extensiones de la [barra de tareas](taskbar-extensions.md).

Las aplicaciones pueden colocar iconos en el área de notificación para indicar el estado de una operación o para notificar al usuario sobre un evento. Por ejemplo, una aplicación podría colocar un icono de impresora en el área de notificación para mostrar que un trabajo de impresión está en funcionamiento. Sin embargo, en Windows 7 y versiones posteriores, parte de la información proporcionada previamente por el área de notificación debe proporcionarse a través del botón de la barra de tareas de la aplicación. El área de notificación se encuentra en el borde derecho de la barra de tareas (si la barra de tareas es horizontal) o en la parte inferior (si la barra de tareas es vertical). Para obtener más información, vea [notificaciones y el área de notificación](notification-area.md).

El área de notificación también muestra la hora actual si se selecciona esa opción. La opción se encuentra como:

-   **Windows 7 y versiones posteriores**: la lista desplegable **reloj** de la página **activar o desactivar iconos** del área de notificación de la aplicación panel de **notificación iconos del área de notificación** (también accesible a través de las propiedades del área de notificación).
-   **Windows Vista**: la casilla **reloj** en la página del **área de notificación** de la barra de tareas y la ventana Propiedades del **menú Inicio** .
-   **Windows XP**: la casilla **Mostrar el reloj** en la **barra de tareas y** en la ventana Propiedades del menú Inicio.

El usuario puede hacer clic con el botón secundario en la barra de tareas para mostrar el menú contextual. El menú contextual incluye comandos para ventanas en cascada, pilas de ventanas, mostrar ventanas en paralelo, mostrar el escritorio, iniciar el administrador de tareas y establecer las propiedades de la barra de tareas. El menú contextual también proporciona la opción de agregar o quitar un conjunto de barras de herramientas de la barra de tareas. Puede agregar nuevas barras de herramientas a este menú si las registra en la \_ categoría DESKBAND CATID. Para obtener más información, vea [implementar objetos de banda](band-objects.md). Tenga en cuenta que, a partir de Windows 7, la barra de tareas y el área de notificación tienen menús contextuales independientes. Estos menús contextuales comparten algunas opciones, como la organización de ventanas, y agregan otras.

### <a name="taskbar-display-options"></a>Opciones de presentación de la barra de tareas

La barra de tareas admite dos opciones de presentación: ocultar automáticamente y, en Windows Vista y versiones anteriores solo, Always On superior (la barra de tareas siempre está en este modo en Windows 7 y versiones posteriores). Para establecer estas opciones, el usuario debe abrir el menú contextual de la barra de tareas, hacer clic en **propiedades** y activar o desactivar la casilla **Ocultar automáticamente la barra de tareas** o **mantener la barra de tareas en la parte superior de otras ventanas** . Para recuperar el estado de estas opciones de presentación, use el mensaje [**\_ GETSTATE de ABN**](abm-getstate.md) . Si desea recibir una notificación cuando el estado de estas opciones de presentación cambie, procese el mensaje de notificación [**ABN \_ STATECHANGE**](abn-statechange.md) en el procedimiento de ventana. Para cambiar el estado de estas opciones de presentación, use el mensaje [**ABN \_ SETSTATE**](abm-setstate.md) .

El *área de trabajo* es la parte de la pantalla que no está oculta en la barra de tareas. Para recuperar el tamaño del área de trabajo, llame a la función [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con el valor **SPI \_ GETWORKAREA** establecido. Para recuperar las coordenadas del rectángulo que describen la ubicación de la barra de tareas, use el mensaje [**ABN \_ GETTASKBARPOS**](abm-gettaskbarpos.md) .

Es posible cubrir la barra de tareas estableciendo explícitamente el tamaño del rectángulo de la ventana igual al tamaño de la pantalla con [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos). En el caso de los sistemas Windows 2000 o posterior, la ventana no debe tener el [**\_ título WS**](../winmsg/window-styles.md) o [**WS \_ THICKFRAME**](../winmsg/window-styles.md), o bien se debe ajustar el tamaño de la ventana para que el área cliente cubra toda la pantalla. También en el caso de los sistemas, si la barra de tareas está establecida en Always On superior, permanecerá oculta solo mientras la aplicación es la aplicación en primer plano.

### <a name="adding-shortcuts-to-the-start-menu"></a>Agregar accesos directos al menú Inicio

Para agregar un elemento al submenú **programas** en Microsoft Windows NT 4,0, Windows 2000 y versiones posteriores, o Windows 95 o posterior, siga estos pasos.

1.  Cree un [vínculo de Shell](./links.md) mediante la interfaz [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) .
2.  Obtenga el PIDL de la carpeta programas con [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation), pasando los [**\_ programas CSIDL**](csidl.md).
3.  Agregue el vínculo de Shell a la carpeta programas. También puede crear una carpeta en la carpeta programas y agregar el vínculo a esa carpeta.

### <a name="managing-taskbar-buttons"></a>Administrar botones de la barra de tareas

El shell crea un botón en la barra de tareas cada vez que una aplicación crea una ventana que no es propiedad de. Para asegurarse de que el botón de ventana se coloca en la barra de tareas, cree una ventana sin propietario con el estilo extendido [**WS \_ ex \_ APPWINDOW**](../winmsg/extended-window-styles.md) . Para evitar que el botón de ventana se coloque en la barra de tareas, cree la ventana sin propietario con el estilo extendido [**WS \_ ex \_ TOOLWINDOW**](../winmsg/extended-window-styles.md) . Como alternativa, puede crear una ventana oculta y hacer que esta ventana oculta sea el propietario de la ventana visible.

El shell quitará el botón de una ventana de la barra de tareas solo si el estilo de la ventana es compatible con los botones visibles de la barra de tareas. Si desea cambiar de forma dinámica el estilo de una ventana a uno que no admita botones visibles de la barra de tareas, debe ocultar primero la ventana (llamando a [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) with **SW \_ Hide**), cambiar el estilo de la ventana y, a continuación, Mostrar la ventana.

Normalmente, el botón ventana contiene el icono de la aplicación y el título. Sin embargo, si la aplicación no contiene un menú del sistema, el botón ventana se crea sin el icono.

Si desea que la aplicación obtenga la atención del usuario cuando la ventana no está activa, utilice la función [**FlashWindow**](/windows/win32/api/winuser/nf-winuser-flashwindow) para que el usuario sepa que un mensaje está en espera. Esta función parpadea el botón de ventana. Una vez que el usuario hace clic en el botón ventana para activar la ventana, la aplicación puede mostrar el mensaje.

### <a name="modifying-the-contents-of-the-taskbar"></a>Modificar el contenido de la barra de tareas

La [versión 4,71 y versiones posteriores](versions.md) de Shell32.dll agregan la capacidad de modificar el contenido de la barra de tareas. Desde una aplicación, ahora puede Agregar, quitar y activar botones de la barra de tareas. La activación del elemento no activa la ventana; muestra el elemento como presionado en la barra de tareas.

Las funciones de modificación de la barra de tareas se implementan en un objeto COM (modelo de objetos componentes) (CLSID \_ TaskbarList) que expone la interfaz [**ITASKBARLIST**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist) (IID \_ ITaskbarList). Debe llamar al método [**ITaskbarList:: HrInit**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist-hrinit) para inicializar el objeto. Después, puede usar los métodos de la interfaz [**ITaskbarList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist) para modificar el contenido de la barra de tareas.

### <a name="adding-modifying-and-deleting-icons-in-the-notification-area"></a>Agregar, modificar y eliminar iconos en el área de notificación

Utilice la [**función \_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) para agregar, modificar o eliminar iconos del área de notificación. El parámetro *dwMessage* de **\_ NotifyIcon de Shell** es un mensaje a la barra de tareas que especifica la acción que se va a realizar. El parámetro *pnid* es un puntero a una estructura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) que se usa para identificar el icono y pasar cualquier información adicional que sea necesaria para que el sistema procese el mensaje.

Puede realizar las siguientes acciones con los iconos del área de notificación.

-   Para agregar un icono al área de notificación de la barra de tareas, llame a [**\_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) con el parámetro *dwMessage* establecido en Nim \_ Agregar. La estructura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) se usa para especificar el identificador y el identificador del icono y cualquier texto de información sobre herramientas. Si el usuario ha activado la casilla **Mostrar reloj** en las propiedades de la barra de tareas, el sistema coloca el icono a la izquierda inmediata del reloj. De lo contrario, el icono aparece en el lado derecho o en la parte inferior de la barra de tareas. Los iconos existentes se desplazan a la izquierda para dejar espacio para el nuevo icono.
-   Para modificar la información de un icono, incluido su identificador de icono, texto de información sobre herramientas y identificador de mensaje de devolución de llamada, llame a [**\_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) con *dwMessage* establecido en Nim \_ modificar.
-   Para eliminar un icono del área de notificación, llame [**a \_ NotifyIcon del shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) con el parámetro *dwMessage* establecido en Nim \_ Delete.

Cuando haya completado una operación de la interfaz de usuario, devuelva el foco al área de notificación mediante una llamada a [**\_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) con *dwMessage* establecido en Nim \_ SETFOCUS. Por ejemplo, podría hacer esto cuando un icono de la barra de tareas muestra un menú contextual, pero el usuario lo cancela presionando la tecla ESCAPE.

### <a name="receiving-notification-area-callback-messages"></a>Recibir mensajes de devolución de llamada del área de notificación

Las aplicaciones suelen colocar iconos en el área de notificación de la barra de tareas para que sirvan como indicadores de estado. Puede proporcionar información adicional cuando el usuario realiza acciones del mouse, como mover el puntero del mouse sobre el icono o hacer clic en el icono.

El sistema le notifica los eventos del mouse y del teclado mediante el envío de un mensaje de devolución de llamada definido por la aplicación que está asociado a un icono determinado. De esta manera, el sistema puede notificar a una aplicación cuando el usuario, por ejemplo, hace clic en el icono o lo selecciona presionando una tecla.

El mensaje de devolución de llamada de un icono se define al agregar el icono a la barra de tareas. El identificador del mensaje de devolución de llamada se especifica en el miembro **uCallbackMessage** de la estructura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) pasada con Nim \_ Agregar. Cuando se produce un evento, el sistema envía el mensaje de devolución de llamada al procedimiento de ventana de la ventana especificada por el miembro **hWnd** . El parámetro *wParam* del mensaje contiene el identificador del icono de la barra de tareas en el que se produjo el evento. El parámetro *lParam* contiene el mouse o el mensaje de teclado asociado al evento. Por ejemplo, cuando el puntero del mouse se mueve a un icono de la barra de tareas, *lParam* contiene [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md).

Los resultados de varios eventos del mouse se pueden resumir de la manera siguiente:

-   Cuando el usuario mueve el puntero del mouse sobre el icono, el sistema muestra el texto de información sobre herramientas que se especificó en [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa).
-   Cuando el usuario hace clic en el icono, la aplicación recibe una notificación de [**\_ LBUTTONDOWN de WM**](../inputdev/wm-lbuttondown.md) .
-   Cuando el usuario hace clic con el botón derecho en el icono, la aplicación recibe una notificación de [**\_ RBUTTONDOWN de WM**](../inputdev/wm-rbuttondown.md) .
-   Cuando el usuario hace doble clic en el icono, la aplicación recibe una notificación de [**\_ LBUTTONDBLCLK de WM**](../inputdev/wm-lbuttondblclk.md) .

Normalmente, al hacer clic en el icono, la aplicación muestra una ventana con información adicional, haciendo clic con el botón secundario en el menú contextual y haciendo doble clic en se ejecuta el comando de menú contextual predeterminado.

Para obtener un ejemplo de cómo cambiar el texto de información sobre herramientas asociado a un icono de área de notificación, vea la [información sobre herramientas de globo para los iconos de la barra de estado](../controls/tooltip-controls.md).

Las versiones 5,0 y posteriores del shell controlan los eventos del mouse y del teclado [**\_ NotifyIcon del shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) de maneras diferentes que las versiones anteriores de Shell que se encuentran en Windows NT 4,0, Windows 95 y Windows 98. Las diferencias son las siguientes:

-   Si un usuario solicita el menú contextual de un icono de notificación con el teclado, el shell de la versión 5,0 envía la aplicación asociada a un mensaje de [**\_ CONTEXTMENU de WM**](../menurc/wm-contextmenu.md) . Las versiones anteriores envían mensajes de [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) y [**WM \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md) .
-   Si un usuario selecciona un icono de notificación con el teclado y lo activa con la barra espaciadora o la tecla entrar, el shell de la versión 5,0 envía la aplicación asociada a una notificación de **\_ KEYSELECT de ndentro** . Las versiones anteriores envían mensajes de [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) y [**WM \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md) .
-   Si un usuario selecciona un icono de notificación con el mouse y lo activa con la tecla entrar, el shell de la versión 5,0 envía a la aplicación asociada una notificación de **\_ selección de ndentro** . Las versiones anteriores envían mensajes de [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) y [**WM \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md) .
-   Si un usuario pasa el puntero del mouse sobre un icono con el que se asocia una información sobre herramientas de globo, el shell de la versión 6,0 (Windows XP) envía los mensajes siguientes.
    -   -   **Ndentro \_ BALLOONSHOW** : se envía cuando se muestra el globo (los globos están en cola).
        -   **Ndentro \_ BALLOONHIDE** : se envía cuando el globo desaparece; por ejemplo, cuando se elimina el icono. No se envía este mensaje si se descarta el globo debido a un tiempo de espera o a un clic del mouse.
        -   **Ndentro \_ BALLOONTIMEOUT** : se envía cuando se descarta el globo debido a un tiempo de espera agotado.
        -   **Ndentro \_ BALLOONUSERCLICK** : se envía cuando se descarta el globo debido a un clic del mouse.

Puede seleccionar la manera en que el shell debe comportarse mediante una llamada a [**\_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) con *dwMessage* establecido en **Nim \_ SETVERSION**. Establezca el miembro **uVersion** de la estructura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) para indicar si desea el comportamiento de la versión 5,0 o anterior a la versión 5,0.

### <a name="taskbar-creation-notification"></a>Notificación de creación de la barra de tareas

Con Microsoft Internet Explorer 4,0 y versiones posteriores, el shell notifica a las aplicaciones que se ha creado la barra de tareas. Cuando se crea la barra de tareas, registra un mensaje con la cadena TaskbarCreated y, a continuación, difunde este mensaje a todas las ventanas de nivel superior. Cuando la aplicación de la barra de tareas recibe este mensaje, debe suponer que los iconos de la barra de tareas que ha agregado se han quitado y los agregan de nuevo. Esta característica se aplica generalmente solo a los servicios que ya se están ejecutando cuando se inicia el shell. En el ejemplo siguiente se muestra un método muy simplificado para controlar este caso.

En Windows 10, la barra de tareas también difunde este mensaje cuando cambia el PPP de la pantalla principal.

```
LRESULT CALLBACK WndProc(HWND hWnd, 
                         UINT uMessage, 
                         WPARAM wParam, 
                         LPARAM lParam)
{
    static UINT s_uTaskbarRestart;

    switch(uMessage)
    {
        case WM_CREATE:
            s_uTaskbarRestart = RegisterWindowMessage(TEXT("TaskbarCreated"));
            break;
        
        default:
            if(uMessage == s_uTaskbarRestart)
                AddTaskbarIcons();
            break;
    }

    return DefWindowProc(hWnd, uMessage, wParam, lParam);
}
```



## <a name="using-the-taskbar"></a>Uso de la barra de tareas

En esta sección se incluyen ejemplos que muestran cómo agregar iconos al área de notificación de la barra de tareas y cómo procesar los mensajes de devolución de llamada para los iconos de la barra de tareas.

### <a name="adding-and-deleting-taskbar-icons-in-the-notification-area"></a>Agregar y eliminar iconos de la barra de tareas en el área de notificación

Para agregar un icono al área de notificación de la barra de tareas, puede rellenar una estructura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) y, a continuación, pasar la estructura a [**\_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) con *dwMessage* establecido en **Nim \_ Agregar**. Los miembros de la estructura deben especificar el identificador de la ventana que está agregando el icono, así como el identificador de icono y el identificador de icono. También puede especificar el texto de información sobre herramientas para el icono. Si necesita recibir mensajes del mouse para el icono, especifique el identificador del mensaje de devolución de llamada que el sistema debe usar para enviar el mensaje al procedimiento de ventana.

La función del ejemplo siguiente muestra cómo agregar un icono a la barra de tareas.


```
// MyTaskBarAddIcon - adds an icon to the notification area. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window to receive callback messages 
// uID - identifier of the icon 
// hicon - handle to the icon to add 
// lpszTip - tooltip text 

BOOL MyTaskBarAddIcon(HWND hwnd, UINT uID, HICON hicon, LPSTR lpszTip) 
{ 
    BOOL res; 
    NOTIFYICONDATA tnid; 
 
    tnid.cbSize = sizeof(NOTIFYICONDATA); 
    tnid.hWnd = hwnd; 
    tnid.uID = uID; 
    tnid.uFlags = NIF_MESSAGE | NIF_ICON | NIF_TIP; 
    tnid.uCallbackMessage = MYWM_NOTIFYICON; 
    tnid.hIcon = hicon; 
    if (lpszTip) 
        hr = StringCbCopyN(tnid.szTip, sizeof(tnid.szTip), lpszTip, 
                           sizeof(tnid.szTip));
        // TODO: Add error handling for the HRESULT.
    else 
        tnid.szTip[0] = (TCHAR)'\0'; 
 
    res = Shell_NotifyIcon(NIM_ADD, &tnid); 
 
    if (hicon) 
        DestroyIcon(hicon); 
 
    return res; 
}
```



Para eliminar un icono del área de notificación de la barra de tareas, rellene una estructura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) y llame al método [**\_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) con *dwMessage* establecido en **Nim \_ Delete**. Al eliminar un icono de la barra de tareas, especifique solo los miembros **cbSize**, **hWnd** y **uID** de la estructura. Por ejemplo:


```
// MyTaskBarDeleteIcon - deletes an icon from the notification area. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window that added the icon. 
// uID - identifier of the icon to delete. 

BOOL MyTaskBarDeleteIcon(HWND hwnd, UINT uID) 
{ 
    BOOL res; 
    NOTIFYICONDATA tnid; 
 
    tnid.cbSize = sizeof(NOTIFYICONDATA); 
    tnid.hWnd = hwnd; 
    tnid.uID = uID; 
         
    res = Shell_NotifyIcon(NIM_DELETE, &tnid); 
    return res; 
}
```



### <a name="receiving-mouse-events"></a>Recibir eventos del mouse

Si especifica un mensaje de devolución de llamada para un icono de la barra de tareas, el sistema enviará el mensaje a la aplicación cada vez que se produzca un evento del mouse en el rectángulo delimitador del icono. El parámetro *wParam* del mensaje especifica el identificador del icono de la barra de tareas y el parámetro *lParam* del mensaje especifica el mensaje generado por el sistema como resultado del evento del mouse.

La función del ejemplo siguiente es de una aplicación que agrega iconos de batería e impresora a la barra de tareas. La aplicación llama a la función cuando recibe un mensaje de devolución de llamada. La función determina si el usuario ha hecho clic en uno de los iconos y, si se ha producido un clic, llama a una función definida por la aplicación para mostrar la información de estado.


```
// On_MYWM_NOTIFYICON - processes callback messages for taskbar icons. 
// wParam - first message parameter of the callback message. 
// lParam - second message parameter of the callback message. 

void On_MYWM_NOTIFYICON(WPARAM wParam, LPARAM lParam) 
{ 
    UINT uID; 
    UINT uMouseMsg; 
 
    uID = (UINT) wParam; 
    uMouseMsg = (UINT) lParam; 
 
    if (uMouseMsg == WM_LBUTTONDOWN) 
    { 
        switch (uID) 
        { 
            case IDI_MYBATTERYICON: 
 
                // The user clicked the battery icon. Display the 
                // battery status. 
                ShowBatteryStatus(); 
                break; 
 
            case IDI_MYPRINTERICON: 
 
                // The user clicked the printer icon. Display the 
                // status of the print job. 
                ShowJobStatus(); 
                break; 
 
            default: 
                break; 
        } 
     } 

     return; 
 }
```



 

 
