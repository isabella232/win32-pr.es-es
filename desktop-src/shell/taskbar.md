---
description: La Windows incluye una barra de herramientas de escritorio de aplicación especial denominada barra de tareas. Puede usar la barra de tareas para tareas como cambiar entre ventanas abiertas e iniciar nuevas aplicaciones.
ms.assetid: 14d520e7-7c15-441d-9662-24b972d208ac
title: Barra de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cce37991c6265f02ab92ece62dbae341031d272a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571476"
---
# <a name="the-taskbar"></a>Barra de tareas

La Windows incluye una barra de [herramientas especial de escritorio de aplicaciones](application-desktop-toolbars.md) denominada barra de *tareas*. Puede usar la barra de tareas para tareas como cambiar entre ventanas abiertas e iniciar nuevas aplicaciones.

> [!Note]  
> Para obtener información sobre los cambios realizados en la barra de tareas Windows 7, vea [Extensiones de la barra de tareas](taskbar-extensions.md).

 

En este tema se incluyen las siguientes secciones.

-   [Acerca de la barra de tareas](#about-the-taskbar)
    -   [Opciones para mostrar de la barra de tareas](#taskbar-display-options)
    -   [Agregar accesos directos al menú Inicio](#adding-shortcuts-to-the-start-menu)
    -   [Administrar botones de la barra de tareas](#managing-taskbar-buttons)
    -   [Agregar, modificar y eliminar iconos en el área de notificación](#adding-modifying-and-deleting-icons-in-the-notification-area)
    -   [Notificación de creación de la barra de tareas](#taskbar-creation-notification)
-   [Uso de la barra de tareas](#using-the-taskbar)
    -   [Agregar y eliminar iconos de la barra de tareas en el área de notificación](#adding-and-deleting-taskbar-icons-in-the-notification-area)
    -   [Recepción de eventos del mouse](#receiving-mouse-events)

## <a name="about-the-taskbar"></a>Acerca de la barra de tareas

La barra de tareas incluye lo siguiente:

-   **Menú** Inicio
-   inicio rápido (solo Windows Vista y versiones anteriores)
-   Botones de la barra de tareas
-   Barras de herramientas (opcional)
-   Área de notificaciones

El **menú** Inicio contiene comandos que pueden tener acceso a programas, documentos y configuraciones. Estos comandos incluyen **Todos** los programas , **Documentos**, **Panel de control** **,** Juegos **,** Ayuda y soporte **técnico,** Apagar y Buscar programas **y archivos**.

El **elemento Iniciar** en versiones anteriores de Windows  contenía elementos como Buscar y  ejecutar **,** cuya funcionalidad se incluía en buscar programas y archivos en Windows Vista y versiones posteriores.

La inicio rápido, disponible en versiones de Windows anteriores a Windows 7, contiene accesos directos a las aplicaciones. Windows proporciona entradas predeterminadas, como Windows Internet Explorer, y el usuario puede agregar cualquier acceso directo adicional que elija. Los iconos de esta área responden a un solo clic. En Windows 7 y versiones posteriores, esta funcionalidad se incluye en los botones de la barra de tareas.

El Shell coloca un botón en la barra de tareas cada vez que una aplicación crea una ventana sin cerrar, es decir, una ventana que no tiene un elemento primario y que tiene los bits de estilo extendido adecuados (consulte Administración de botones de la barra de tareas [a](#managing-taskbar-buttons)continuación). Para cambiar a una ventana, el usuario hace clic en su botón de ventana. Esta funcionalidad se ha ampliado enormemente a partir de Windows 7. Para obtener más información, vea [Extensiones de la barra de tareas](taskbar-extensions.md).

Las aplicaciones pueden colocar iconos en el área de notificación para indicar el estado de una operación o para notificar al usuario sobre un evento. Por ejemplo, una aplicación podría colocar un icono de impresora en el área de notificación para mostrar que se está en proceso un trabajo de impresión. Sin embargo, en Windows 7 y versiones posteriores, parte de la información proporcionada anteriormente por el área de notificación debe proporcionarse a través del botón de la barra de tareas de una aplicación. El área de notificación se encuentra en el borde derecho de la barra de tareas (si la barra de tareas es horizontal) o en la parte inferior (si la barra de tareas es vertical). Para obtener más información, vea [Notificaciones y el área de notificación](notification-area.md).

El área de notificación también muestra la hora actual si se selecciona esa opción. La opción se encuentra como:

-   **Windows 7** y versiones  posteriores: la lista  desplegable Reloj de la página Activar o desactivar iconos del sistema de la aplicación Iconos de área de notificación **Panel de control** (también accesible a través de las propiedades del área de notificación).
-   **Windows Vista:** la casilla **Reloj** de la página Área de **notificación** de la barra de tareas y la ventana de propiedades **del menú** Inicio.
-   **Windows XP:** la **casilla Mostrar el** reloj de la barra de **tareas y la ventana propiedades del menú** Inicio.

El usuario puede hacer clic con el botón derecho en la barra de tareas para mostrar el menú contextual. El menú contextual incluye comandos para ventanas en cascada, ventanas de pila, mostrar ventanas en paralelo, mostrar el escritorio, iniciar Administrador de tareas y establecer las propiedades de la barra de tareas. El menú contextual también proporciona la opción de agregar o quitar un conjunto de barras de herramientas de la barra de tareas. Puede agregar nuevas barras de herramientas a este menú registrándolos en la categoría CATID \_ DeskBand. Para obtener más información, vea [Implementar objetos de banda](band-objects.md). Tenga en cuenta que Windows 7, la barra de tareas y el área de notificación tienen menús contextuales independientes. Estos menús contextuales comparten algunas opciones, como la disposición de ventanas, y agregan otras.

### <a name="taskbar-display-options"></a>Opciones para mostrar de la barra de tareas

La barra de tareas admite dos opciones de presentación: Ocultar automáticamente y, en Windows Vista y versiones anteriores solo, Always On Superior (la barra de tareas siempre está en este modo en Windows 7 y versiones posteriores). Para establecer estas opciones, el usuario debe abrir el menú contextual  de la barra de tareas,  hacer clic en Propiedades y activar o borrar la casilla Ocultar automáticamente la barra de tareas o mantener la barra de tareas encima de otras ventanas.  Para recuperar el estado de estas opciones de visualización, use el [**mensaje \_ GETSTATE de ABM.**](abm-getstate.md) Si desea recibir una notificación cuando cambie el estado de estas opciones de visualización, procese el mensaje de notificación [**\_ ABN STATECHANGE**](abn-statechange.md) en el procedimiento de la ventana. Para cambiar el estado de estas opciones de visualización, use el [**mensaje \_ SETSTATE de ABM.**](abm-setstate.md)

El *área de trabajo* es la parte de la pantalla que la barra de tareas no oculta. Para recuperar el tamaño del área de trabajo, llame a la función [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con el **valor \_ GETWORKAREA de SPI** establecido. Para recuperar las coordenadas del rectángulo que describen la ubicación de la barra de tareas, use el [**mensaje \_ GETTASKBARPOS de ABM.**](abm-gettaskbarpos.md)

Es posible cubrir la barra de tareas estableciendo explícitamente el tamaño del rectángulo de la ventana igual al tamaño de la pantalla [**con SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos). Para Windows 2000 sistemas o versiones posteriores, la ventana debe carecer de [**WS \_ CAPTION**](../winmsg/window-styles.md) o [**WS \_ THICKFRAME,**](../winmsg/window-styles.md)o bien debe tener el tamaño de la ventana para que el área de cliente atrape toda la pantalla. Especialmente para esos sistemas, si la barra de tareas está establecida en Always On Superior, permanecerá oculta solo mientras la aplicación sea la aplicación en primer plano.

### <a name="adding-shortcuts-to-the-start-menu"></a>Agregar accesos directos al menú Inicio

Para agregar un  elemento al submenú Programas en Microsoft Windows NT 4.0, Windows 2000 y versiones posteriores, o Windows 95 o posterior, siga estos pasos.

1.  Cree un [vínculo de shell](./links.md) mediante la interfaz [**IShellLink.**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka)
2.  Obtenga el PIDL de la carpeta Programas mediante [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation), pasando [**CSIDL \_ PROGRAMS**](csidl.md).
3.  Agregue el vínculo shell a la carpeta Programas. También puede crear una carpeta en la carpeta Programas y agregar el vínculo a esa carpeta.

### <a name="managing-taskbar-buttons"></a>Administrar botones de la barra de tareas

El Shell crea un botón en la barra de tareas cada vez que una aplicación crea una ventana que no es propiedad de . Para asegurarse de que el botón de ventana se coloca en la barra de tareas, cree una ventana sin cerrar con el estilo extendido [**\_ de \_ APPWINDOW de WS EX.**](../winmsg/extended-window-styles.md) Para evitar que el botón de ventana se coloque en la barra de tareas, cree la ventana sin cerrar con el estilo extendido [**WS \_ EX \_ TOOLWINDOW.**](../winmsg/extended-window-styles.md) Como alternativa, puede crear una ventana oculta y convertirla en el propietario de la ventana visible.

El Shell quitará el botón de una ventana de la barra de tareas solo si el estilo de la ventana admite botones visibles de la barra de tareas. Si desea cambiar dinámicamente el estilo de una ventana a uno que no admita botones visibles de la barra de tareas, primero debe ocultar la ventana (llamando a [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) con **SW \_ HIDE),** cambiar el estilo de la ventana y, a continuación, mostrar la ventana.

El botón de ventana normalmente contiene el icono y el título de la aplicación. Sin embargo, si la aplicación no contiene un menú del sistema, el botón de ventana se crea sin el icono .

Si desea que la aplicación reciba la atención del usuario cuando la ventana no está activa, use la [**función FlashWindow**](/windows/win32/api/winuser/nf-winuser-flashwindow) para que el usuario sepa que hay un mensaje en espera. Esta función parpadea el botón de ventana. Una vez que el usuario hace clic en el botón de ventana para activar la ventana, la aplicación puede mostrar el mensaje.

### <a name="modifying-the-contents-of-the-taskbar"></a>Modificar el contenido de la barra de tareas

[La versión 4.71 y](versions.md) posteriores de Shell32.dll agrega la funcionalidad para modificar el contenido de la barra de tareas. Desde una aplicación, ahora puede agregar, quitar y activar botones de la barra de tareas. La activación del elemento no activa la ventana; muestra el elemento presionado en la barra de tareas.

Las funcionalidades de modificación de la barra de tareas se implementan en un objeto Del modelo de objetos componentes (COM) (CLSID TaskbarList) que expone la interfaz \_ [**ITaskbarList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist) (IID \_ ITaskbarList). Debe llamar al [**método ITaskbarList::HrInit**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist-hrinit) para inicializar el objeto. A continuación, puede usar los métodos de la [**interfaz ITaskbarList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist) para modificar el contenido de la barra de tareas.

### <a name="adding-modifying-and-deleting-icons-in-the-notification-area"></a>Agregar, modificar y eliminar iconos en el área de notificación

Use la [**función \_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) para agregar, modificar o eliminar iconos del área de notificación. El *parámetro dwMessage* de **Shell \_ NotifyIcon** es un mensaje a la barra de tareas que especifica la acción que se va a realizar. El *parámetro pnid* es un puntero a una estructura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) que se usa para identificar el icono y pasar cualquier información adicional necesaria para que el sistema procese el mensaje.

Puede realizar las siguientes acciones con iconos de área de notificación.

-   Para agregar un icono al área de notificación de la barra de tareas, llame a [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) con el parámetro *dwMessage* establecido en NIM \_ ADD. La [**estructura NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) se usa para especificar el identificador y el identificador del icono, así como cualquier texto de información sobre herramientas. Si el usuario ha seleccionado la casilla **Mostrar** reloj en las propiedades de la barra de tareas, el sistema coloca el icono a la izquierda inmediata del reloj. De lo contrario, el icono aparece en el lado derecho o en la parte inferior de la barra de tareas. Los iconos existentes se desplazan a la izquierda para dejar espacio para el nuevo icono.
-   Para modificar la información de un icono, incluido su identificador de icono, texto de información sobre herramientas e identificador de mensaje de devolución de llamada, llame a [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) con *dwMessage* establecido en NIM \_ MODIFY.
-   Para eliminar un icono del área de notificación, llame a [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) con el *parámetro dwMessage* establecido en NIM \_ DELETE.

Cuando haya completado una operación de interfaz de usuario, devuelva el foco al área de notificación mediante una llamada a [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) con *dwMessage* establecido en NIM \_ SETFOCUS. Por ejemplo, podría hacerlo cuando un icono de la barra de tareas muestra un menú contextual, pero el usuario lo cancela presionando la tecla ESCAPE.

### <a name="receiving-notification-area-callback-messages"></a>Recepción de mensajes de devolución de llamada del área de notificación

Las aplicaciones normalmente coloca iconos en el área de notificación de la barra de tareas para que sirvan como indicadores de estado. Puede proporcionar información adicional cuando el usuario realiza acciones del mouse, como mover el puntero del mouse sobre el icono o hacer clic en el icono.

El sistema le notifica los eventos del mouse y el teclado mediante el envío de un mensaje de devolución de llamada definido por la aplicación que está asociado a un icono determinado. De este modo, el sistema puede notificar a una aplicación cuando el usuario, por ejemplo, hace clic en el icono o lo selecciona presionando una tecla.

El mensaje de devolución de llamada de un icono se define al agregar el icono a la barra de tareas. El identificador del mensaje de devolución de llamada se especifica en el **miembro uCallbackMessage** de la [**estructura NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) pasada con NIM \_ ADD. Cuando se produce un evento, el sistema envía el mensaje de devolución de llamada al procedimiento de ventana de la ventana especificada por el **miembro hWnd.** El *parámetro wParam* del mensaje contiene el identificador del icono de la barra de tareas en el que se produjo el evento. El *parámetro lParam* contiene el mensaje del mouse o del teclado asociado al evento. Por ejemplo, cuando el puntero del mouse se mueve a un icono de la barra de tareas, *lParam* contiene [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md).

Los resultados de varios eventos del mouse se pueden resumir de la siguiente manera:

-   Cuando el usuario mueve el puntero del mouse sobre el icono, el sistema muestra el texto de información sobre herramientas que se especificó [**en NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa).
-   Cuando el usuario hace clic en el icono, la aplicación recibe una [**notificación \_ WM LBUTTONDOWN.**](../inputdev/wm-lbuttondown.md)
-   Cuando el usuario hace clic con el botón derecho en el icono, la aplicación recibe una [**notificación \_ WM RBUTTONDOWN.**](../inputdev/wm-rbuttondown.md)
-   Cuando el usuario hace doble clic en el icono, la aplicación recibe una notificación [**\_ WM LBUTTONDBLCLK.**](../inputdev/wm-lbuttondblclk.md)

Normalmente, al hacer clic en el icono, la aplicación muestra una ventana con información adicional, al hacer clic con el botón derecho se muestra un menú contextual y al hacer doble clic se ejecuta el comando de menú contextual predeterminado.

Para obtener un ejemplo de cómo cambiar el texto de información sobre herramientas asociado a un icono de área de notificación, vea Información sobre herramientas [de globo para iconos de barra de estado.](../controls/tooltip-controls.md)

Las versiones 5.0 y posteriores del shell controlan eventos de mouse y teclado [**de Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) de maneras diferentes a las versiones anteriores de Shell encontradas en Windows NT 4.0, Windows 95 y Windows 98. Las diferencias son las siguientes:

-   Si un usuario solicita un menú contextual del icono de notificación con el teclado, el Shell de la versión 5.0 envía a la aplicación asociada un [**mensaje \_ CONTEXTMENU de WM.**](../menurc/wm-contextmenu.md) Las versiones anteriores envían [**mensajes \_ WM RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) [**y WM \_ RBUTTONUP.**](../inputdev/wm-rbuttonup.md)
-   Si un usuario selecciona un icono de notificación con el teclado y lo activa con la barra espaciador o la tecla ENTRAR, el Shell de la versión 5.0 envía a la aplicación asociada una notificación **NIN \_ KEYSELECT.** Las versiones anteriores envían [**mensajes \_ WM RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) [**y WM \_ RBUTTONUP.**](../inputdev/wm-rbuttonup.md)
-   Si un usuario selecciona un icono de notificación con el mouse y lo activa con la clave ENTRAR, el shell de la versión 5.0 envía a la aplicación asociada una **notificación NIN \_ SELECT.** Las versiones anteriores envían [**mensajes \_ WM RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) [**y WM \_ RBUTTONUP.**](../inputdev/wm-rbuttonup.md)
-   Si un usuario pasa el puntero del mouse sobre un icono al que está asociada la información sobre herramientas de un globo, el shell de la versión 6.0 (Windows XP) envía los mensajes siguientes.
    -   -   **NIN \_ BALLOONSHOW:** se envía cuando se muestra el globo (los globos se ponen en cola).
        -   **NIN \_ BALLOONHIDE:** se envía cuando el globo desaparece, por ejemplo, cuando se elimina el icono. Este mensaje no se envía si el globo se descarta debido a un tiempo de espera o a un clic del mouse.
        -   **NIN \_ BALLOONTIMEOUT:** se envía cuando se descarta el globo debido a un tiempo de espera.
        -   **NIN \_ BALLOONUSERCLICK:** se envía cuando se descarta el globo debido a un clic del mouse.

Puede seleccionar la forma en que se debe comportar el shell llamando a [**\_ Shell NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) con *dwMessage* establecido en **NIM \_ SETVERSION.** Establezca el **miembro uVersion** de la estructura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) para indicar si desea un comportamiento de la versión 5.0 o anterior a la 5.0.

### <a name="taskbar-creation-notification"></a>Notificación de creación de la barra de tareas

Con Microsoft Internet Explorer 4.0 y versiones posteriores, shell notifica a las aplicaciones que se ha creado la barra de tareas. Cuando se crea la barra de tareas, registra un mensaje con la cadena TaskbarCreated y, a continuación, difunde este mensaje a todas las ventanas de nivel superior. Cuando la aplicación de la barra de tareas recibe este mensaje, debe suponer que se han quitado todos los iconos de la barra de tareas que agregó y agregarlos de nuevo. Por lo general, esta característica solo se aplica a los servicios que ya se están ejecutando cuando se inicia el shell. En el ejemplo siguiente se muestra un método muy simplificado para controlar este caso.

En Windows 10, la barra de tareas también difunde este mensaje cuando cambia el valor de PPP de la pantalla principal.

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

En esta sección se incluyen ejemplos que muestran cómo agregar iconos al área de notificación de la barra de tareas y cómo procesar mensajes de devolución de llamada para iconos de la barra de tareas.

### <a name="adding-and-deleting-taskbar-icons-in-the-notification-area"></a>Agregar y eliminar iconos de la barra de tareas en el área de notificación

Agregue un icono al área de notificación de la barra de tareas rellenando una estructura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) y, a continuación, pasando la estructura a [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) con *dwMessage* establecido en **NIM \_ ADD**. Los miembros de la estructura deben especificar el identificador de la ventana que agrega el icono, así como el identificador de icono y el identificador de icono. También puede especificar texto de información sobre herramientas para el icono. Si necesita recibir mensajes del mouse para el icono, especifique el identificador del mensaje de devolución de llamada que el sistema debe usar para enviar el mensaje al procedimiento de ventana.

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



Para eliminar un icono del área de notificación de la barra de tareas, rellene una estructura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) y llame a [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) *con dwMessage* establecido en **NIM \_ DELETE**. Al eliminar un icono de la barra de tareas, especifique solo los miembros **cbSize**, **hWnd** y **uID** de la estructura. Por ejemplo:


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



### <a name="receiving-mouse-events"></a>Recepción de eventos del mouse

Si especifica un mensaje de devolución de llamada para un icono de barra de tareas, el sistema envía el mensaje a la aplicación cada vez que se produce un evento del mouse en el rectángulo delimitador del icono. El *parámetro wParam* del mensaje especifica el identificador del icono de la barra de tareas y el parámetro *lParam* del mensaje especifica el mensaje que el sistema generó como resultado del evento del mouse.

La función del ejemplo siguiente es de una aplicación que agrega iconos de batería e impresora a la barra de tareas. La aplicación llama a la función cuando recibe un mensaje de devolución de llamada. La función determina si el usuario ha hecho clic en uno de los iconos y, si se ha producido un clic, llama a una función definida por la aplicación para mostrar información de estado.


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



 

 
