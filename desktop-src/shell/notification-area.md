---
description: El área de notificación es una parte de la barra de tareas que proporciona un origen temporal para las notificaciones y el estado.
ms.assetid: D37E2BF7-1887-4780-81AD-85B2117321E4
title: Notificaciones y el área de notificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89af1d0b8af0b41674f79325f0eeb389cbc8f2c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574525"
---
# <a name="notifications-and-the-notification-area"></a>Notificaciones y el área de notificación

El área de notificación es una parte de la barra de tareas que proporciona un origen temporal para las notificaciones y el estado. También se puede usar para mostrar iconos para las características del sistema y del programa que no tienen presencia en el escritorio, como el nivel de batería, el control de volumen y el estado de la red. El área de notificación se ha conocido históricamente como la bandeja del sistema o el área de estado.

Este tema contiene las siguientes secciones:

-   [Directrices del área de notificación y notificación](#notification-and-notification-area-guidelines)
-   [Crear y mostrar una notificación](#notifications-and-the-notification-area)
    -   [Agregar un icono de notificación](#add-a-notification-icon)
    -   [Definición de la versión NOTIFYICONDATA](#define-the-notifyicondata-version)
    -   [Definir la apariencia y el contenido de la notificación](#define-the-notification-look-and-contents)
    -   [Comprobación del estado del usuario](#check-the-user-status)
    -   [Mostrar la notificación](#display-the-notification)
    -   [Quitar un icono](#removing-an-icon)
-   [Ejemplo de SDK](#sdk-sample)
-   [Temas relacionados](#related-topics)

## <a name="notification-and-notification-area-guidelines"></a>Directrices del área de notificación y notificación

Consulte las [secciones Notifications](../uxguide/mess-notif.md) and [Notification Area](../uxguide/winenv-notification.md) (Notificaciones y área de notificación) de Windows User Experience Interaction Guidelines for best practices in the use of notifications and the notification area (Directrices de interacción de la experiencia del usuario de Windows para procedimientos recomendados en el uso de notificaciones y el área de notificación). El objetivo es proporcionar al usuario el beneficio mediante el uso adecuado de las notificaciones, sin ser molesto ni distraer.

El área de notificación no es para la información crítica sobre la que se debe actuar inmediatamente. Tampoco está pensado para el acceso rápido a programas o comandos. A partir Windows 7, gran parte de esa funcionalidad se logra mejor a través del botón de la barra de tareas de una aplicación.

Windows 7 permite a un usuario suprimir todas las notificaciones de una aplicación si lo decide, por lo que el diseño y el uso de notificaciones cuidadosas inclinen al usuario para permitir que la aplicación siga mostrándolos. Las notificaciones son una interrupción; asegúrese de que merece la pena.

Windows 7 presenta el concepto de "tiempo de silencio". El tiempo de silencio se define como la primera hora después de que un nuevo usuario inicie sesión en su cuenta por primera vez o por primera vez después de una actualización del sistema operativo o una instalación limpia. Esta vez se reserva para permitir que el usuario explore y se familiarice con el nuevo entorno sin la distracción de las notificaciones. Durante este tiempo, la mayoría de las notificaciones no se deben enviar ni mostrar. Las excepciones incluyen comentarios que el usuario esperaría ver en respuesta a una acción del usuario, como cuando conecta un dispositivo USB o imprime un documento. Más adelante en este tema se analizan los detalles específicos de la API sobre el tiempo de silencio.

## <a name="creating-and-displaying-a-notification"></a>Crear y mostrar una notificación

En las secciones restantes de este tema se describe el procedimiento básico que se debe seguir para mostrar una notificación de la aplicación al usuario.

1.  [Agregar un icono de notificación](#add-a-notification-icon)
2.  [Definición de la versión NOTIFYICONDATA](#define-the-notifyicondata-version)
3.  [Definir la apariencia y el contenido de la notificación](#define-the-notification-look-and-contents)
4.  [Comprobación del estado del usuario](#check-the-user-status)
5.  [Mostrar la notificación](#display-the-notification)
6.  [Quitar un icono](#removing-an-icon)

### <a name="add-a-notification-icon"></a>Agregar un icono de notificación

Para mostrar una notificación, debe tener un icono en el área de notificación. En algunos casos, como Microsoft Communicator nivel de batería, ese icono ya estará presente. Sin embargo, en muchos otros casos, agregará un icono al área de notificación solo mientras sea necesario para mostrar la notificación. En cualquier caso, esto se logra mediante la [**función \_ NotifyIcon del**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) shell. **Shell \_ NotifyIcon** permite agregar, modificar o eliminar un icono en el área de notificación.

![área de notificación que contiene tres iconos](images/taskbar/notificationareaicons.png)

Cuando se agrega un icono al área de notificación en Windows 7, se agrega a la sección de desbordamiento del área de notificación de forma predeterminada. Esta área contiene iconos de área de notificación que están activos, pero no visibles en el área de notificación. Solo el usuario puede promover un icono desde el desbordamiento al área de notificación, aunque en determinadas circunstancias el sistema puede promover temporalmente un icono al área de notificación como una vista previa corta (menos de un minuto).

> [!Note]  
> El usuario debe tener la última decisión sobre qué iconos desea ver en su área de notificación. Antes de instalar un icono no transitorio en el área de notificación, se debe pedir permiso al usuario. También se les debe dar la opción (normalmente a través de su menú contextual) para quitar el icono del área de notificación.

 

La [**estructura NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) enviada en la llamada al [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contiene información que especifica el icono del área de notificación y la propia notificación. Estos son los elementos específicos del propio icono del área de notificación que se pueden establecer a través **de NOTIFYICONDATA**.

-   Recurso del que se toma el icono.
-   Identificador único del icono.
-   Estilo de la información sobre herramientas del icono.
-   El estado del icono (oculto, compartido o ambos) en el área de notificación.
-   Identificador de una ventana de aplicación asociada al icono.
-   Identificador de mensaje de devolución de llamada que permite al icono comunicar eventos que se producen dentro del rectángulo delimitador del icono y la notificación de globo con la ventana de aplicación asociada. El rectángulo delimitador del icono se puede recuperar a través de [**\_ NotifyIconGetRect del shell.**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect)

Cada icono del área de notificación se puede identificar de dos maneras:

-   GUID con el que se declara el icono en el Registro. Este es el método preferido en Windows 7 y versiones posteriores.
-   Identificador de una ventana asociada al icono del área de notificación, además de un identificador de icono definido por la aplicación. Este método se usa en Windows Vista y versiones anteriores.

Los iconos del área de notificación pueden tener información sobre herramientas. La información sobre herramientas puede ser una información sobre herramientas estándar (preferida) o una interfaz de usuario emergente dibujada por la aplicación. Aunque no se requiere información sobre herramientas, se recomienda.

Los iconos del área de notificación deben tener en cuenta valores altos de PPP. Una aplicación debe proporcionar un icono de 16 x 16 píxeles y un icono de 32 x 32 en su archivo de recursos y, a continuación, usar [**LoadIconMetric**](/windows/win32/api/commctrl/nf-commctrl-loadiconmetric) para asegurarse de que el icono correcto se carga y escala correctamente.

La aplicación responsable del icono del área de notificación debe controlar un clic del mouse para ese icono. Cuando un usuario hace clic con el botón derecho en el icono, debería abrir un menú contextual normal. Sin embargo, el resultado de un solo clic con el botón izquierdo del mouse variará con la función del icono. Debería mostrar lo que el usuario esperaría ver en el formato más adecuado para ese contenido: una ventana emergente, un cuadro de diálogo o la propia ventana del programa. Por ejemplo, podría mostrar el texto de estado de un icono de estado o un control deslizante para el control de volumen.

La colocación de una ventana emergente o un cuadro de diálogo que resulta del clic debe colocarse cerca de la coordenada del clic en el área de notificación. Use [**CalculatePopupWindowPosition para**](/windows/win32/api/winuser/nf-winuser-calculatepopupwindowposition) determinar su ubicación.

El icono se puede agregar al área de notificación sin mostrar una notificación definiendo solo los miembros específicos del icono de [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) (mencionado anteriormente) y llamando a [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) como se muestra aquí:


```
NOTIFYICONDATA nid = {};
// Do NOT set the NIF_INFO flag.
...                    
Shell_NotifyIcon(NIM_ADD, &nid);
```



También puede agregar el icono al área de notificación y mostrar una notificación en una llamada al [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona). Para ello, continúe con las instrucciones de este tema.

### <a name="define-the-notifyicondata-version"></a>Definición de la versión NOTIFYICONDATA

A Windows ha progresado, la [**estructura NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) se ha expandido para incluir más miembros para definir más funcionalidad. Las constantes se usan para declarar qué versión de **NOTIFYICONDATA** se va a usar con el icono del área de notificación, para permitir la compatibilidad con versiones anteriores. A menos que haya una razón atractiva para hacer lo contrario, se recomienda encarecidamente usar la versión NOTIFYICON VERSIÓN 4, que se introdujo \_ \_ en Windows Vista. Esta versión proporciona toda la funcionalidad disponible, incluida la capacidad preferida para identificar el icono del área de notificación a través de un GUID registrado, un mecanismo de devolución de llamada superior y una mejor accesibilidad.

Establezca la versión a través de las siguientes llamadas:


```
NOTIFYICONDATA nid = {};
... 
nid.uVersion = NOTIFYICON_VERSION_4;
// Add the icon
Shell_NotifyIcon(NIM_ADD, &nid);
// Set the version
Shell_NotifyIcon(NIM_SETVERSION, &nid);
```



Tenga en cuenta que esta [**llamada \_ a NotifyIcon del shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) no muestra una notificación.

### <a name="define-the-notification-look-and-contents"></a>Definir la apariencia y el contenido de la notificación

Una notificación es un tipo especial de control de información sobre herramientas de globo. Contiene un título, texto del cuerpo y un icono. Al igual que una ventana, tiene un **botón Cerrar** en la esquina superior derecha. También contiene un **botón** Opciones que abre el elemento Iconos de área de notificación del Panel de control, que permite al usuario mostrar u ocultar el icono o mostrar solo las notificaciones sin un icono.

![captura de pantalla del globo de notificación que indica que la batería está baja](images/taskbar/notificationballoon.png)

La [**estructura NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) enviada en la llamada al [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contiene información que especifica el icono del área de notificación y el propio globo de notificación. Estos son los elementos específicos de la notificación que se pueden establecer a través **de NOTIFYICONDATA**.

-   Icono que se va a mostrar en el globo de notificación, especificado por el tipo de notificación. Se puede especificar el tamaño del icono, así como iconos personalizados.
-   Un título de notificación. Este título debe tener un máximo de 48 caracteres en inglés (para adaptarse a la localización). El título es la primera línea de la notificación y se diferencia mediante el uso del tamaño de fuente, el color y el peso.
-   Texto para su uso en el cuerpo de la notificación. Este texto debe tener un máximo de 200 caracteres en inglés (para adaptarse a la localización).
-   Si la notificación se debe descartar si no se puede mostrar inmediatamente.
-   Tiempo de espera para la notificación. Esta configuración se omite en Windows Vista y sistemas posteriores en favor de una configuración de tiempo de espera de accesibilidad para todo el sistema.
-   Si la notificación debe respetar el tiempo de silencio, establezca a través de la [**marca NIIF \_ RESPECT QUIET \_ \_ TIME.**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)

> [!Note]  
> Las [**interfaces IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification) [**e IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2) son contenedores de Component Object Model (COM) para [**Shell \_ NotifyIcon.**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) Sin embargo, en este momento, no proporcionan la funcionalidad COMPLETA NOTIFYICON VERSIÓN 4 disponible a través de NotifyIcon de Shell directamente, incluido el uso de un GUID para identificar el icono del área \_ \_ de notificación. **\_**

 

### <a name="check-the-user-status"></a>Comprobación del estado del usuario

El sistema usa la función [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) para comprobar si el usuario está en tiempo de silencio, fuera del equipo o en un estado ininterrumpible, como el modo presentación. Si el sistema muestra la notificación depende de este estado.

> [!Note]  
> Si la aplicación usa un método de notificación personalizado que no usa [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)o [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2), siempre debe llamar explícitamente a [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) para determinar si debe mostrar la interfaz de usuario de notificación en ese momento.

 

Las notificaciones enviadas cuando el usuario está fuera se ponen en cola para mostrarse, pero como no se puede saber cuándo devolverá el usuario o si la notificación seguirá siendo válida en ese momento, puede considerar la posibilidad de volver a enviar la notificación más adelante.

Las notificaciones enviadas durante el tiempo de silencio se descartan sin mostrar. Las directrices de diseño piden que se ignoren todas las notificaciones. No deben requerir una acción inmediata del usuario. Por lo tanto, ninguna notificación es tan importante que deba invalidar el tiempo de silencio.

### <a name="display-the-notification"></a>Mostrar la notificación

Una vez que haya establecido la [**versión NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) y haya definido la notificación en una estructura **NOTIFYICONDATA,** llame a [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) para mostrar el icono.

-   Si el icono del área de notificación no está presente, llame a [**\_ Shell NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) para agregar el icono. Haga esto para iconos transitorios y no transitorios.
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_ADD, &nid);
    ```

    

-   Si el icono del área de notificación ya está presente, llame a [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) para modificar el icono.
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_MODIFY, &nid);
    ```

    

En el código siguiente se muestra un ejemplo de cómo establecer [**los datos NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) y enviarlos a través [**de \_ NotifyIcon del shell.**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) Tenga en cuenta que en este ejemplo se identifica el icono de notificación a través de un GUID (preferido Windows 7).


```
// Declare NOTIFYICONDATA details. 
    // Error handling is omitted here for brevity. Do not omit it in your code.
    
    NOTIFYICONDATA nid = {};
    nid.cbSize = sizeof(nid);
    nid.hWnd = hWnd;
    nid.uFlags = NIF_ICON | NIF_TIP | NIF_GUID;
    
    // Note: This is an example GUID only and should not be used.
    // Normally, you should use a GUID-generating tool to provide the value to
    // assign to guidItem.
    static const GUID myGUID = 
    {0x23977b55, 0x10e0, 0x4041, {0xb8, 0x62, 0xb1, 0x95, 0x41, 0x96, 0x36, 0x69}};
    nid.guidItem = myGUID;
    
    nid.guidItem = guid;
    
    // This text will be shown as the icon's tooltip.
    StringCchCopy(nid.szTip, ARRAYSIZE(nid.szTip), L"Test application");
    
    // Load the icon for high DPI.
    LoadIconMetric(hInst, MAKEINTRESOURCE(IDI_SMALL), LIM_SMALL, &(nid.hIcon));
    
    // Show the notification.
    Shell_NotifyIcon(NIM_ADD, &nid) ? S_OK : E_FAIL;
```



### <a name="removing-an-icon"></a>Quitar un icono

Para quitar un icono(por ejemplo, cuando solo ha agregado el icono temporalmente para difundir una notificación), llame a [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)como se muestra aquí. En esta llamada solo se necesita una estructura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) mínima que identifique el icono.


```
NOTIFYICONDATA nid = {};
...                    
Shell_NotifyIcon(NIM_DELETE, &nid);
```



> [!Note]  
> Cuando se desinstala una aplicación, su icono de área de notificación puede aparecer al usuario como una opción en la página Iconos de área de notificación de la Panel de control durante un máximo de siete días. Sin embargo, los cambios realizados allí no tendrán ningún efecto.

 

## <a name="sdk-sample"></a>Ejemplo de SDK

Consulte el [ejemplo NotificationIcon](samples-notificationicon.md) en Windows Software Development Kit (SDK) para obtener un ejemplo completo del uso de [**\_ NotifyIcon de shell.**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)
</dt> <dt>

[**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect)
</dt> <dt>

[**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)
</dt> <dt>

[**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate)
</dt> <dt>

[**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)
</dt> <dt>

[**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2)
</dt> <dt>

[La barra de tareas](taskbar.md)
</dt> <dt>

[Extensiones de la barra de tareas](taskbar-extensions.md)
</dt> </dl>

 

 
