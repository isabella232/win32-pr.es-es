---
description: El área de notificación es una parte de la barra de tareas que proporciona un origen temporal para las notificaciones y el estado.
ms.assetid: D37E2BF7-1887-4780-81AD-85B2117321E4
title: Notificaciones y el área de notificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89af1d0b8af0b41674f79325f0eeb389cbc8f2c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360427"
---
# <a name="notifications-and-the-notification-area"></a>Notificaciones y el área de notificación

El área de notificación es una parte de la barra de tareas que proporciona un origen temporal para las notificaciones y el estado. También se puede usar para mostrar iconos de características del sistema y de programas que no tienen presencia en el escritorio, como el nivel de batería, el control de volumen y el estado de la red. El área de notificación se ha conocido históricamente como la bandeja del sistema o el área de estado.

Este tema contiene las siguientes secciones:

-   [Instrucciones del área de notificación y notificación](#notification-and-notification-area-guidelines)
-   [Crear y mostrar una notificación](#notifications-and-the-notification-area)
    -   [Icono Agregar un aviso](#add-a-notification-icon)
    -   [Definición de la versión de NOTIFYICONDATA](#define-the-notifyicondata-version)
    -   [Definir la apariencia y el contenido de la notificación](#define-the-notification-look-and-contents)
    -   [Comprobar el estado del usuario](#check-the-user-status)
    -   [Mostrar la notificación](#display-the-notification)
    -   [Quitar un icono](#removing-an-icon)
-   [Ejemplo de SDK](#sdk-sample)
-   [Temas relacionados](#related-topics)

## <a name="notification-and-notification-area-guidelines"></a>Instrucciones del área de notificación y notificación

Consulte las secciones [notificaciones](../uxguide/mess-notif.md) y del [área de notificación](../uxguide/winenv-notification.md) de las instrucciones de interacción de la experiencia del usuario de Windows para conocer los procedimientos recomendados para el uso de notificaciones y el área de notificación. El objetivo es proporcionar a los usuarios ventajas mediante el uso adecuado de las notificaciones, sin ser molestas ni distraer.

El área de notificación no es para información crítica que se debe actuar inmediatamente. Tampoco está pensado para el acceso rápido a programas o comandos. A partir de Windows 7, gran parte de esa funcionalidad se consigue mejor a través del botón de la barra de tareas de la aplicación.

Windows 7 permite a un usuario suprimir todas las notificaciones de una aplicación si eligen, por lo que el diseño y el uso de las notificaciones determinan el usuario para permitir que la aplicación siga apareciendo. Las notificaciones son una interrupción; Asegúrese de que merece la pena.

Windows 7 presenta el concepto de "tiempo de inactividad". El tiempo de inactividad se define como la primera hora después de que un nuevo usuario inicie sesión en su cuenta por primera vez o por primera vez después de una actualización de sistema operativo o una instalación limpia. Este tiempo se reserva para permitir que el usuario explore y se familiarice con el nuevo entorno sin la distracción de las notificaciones. Durante este tiempo, la mayoría de las notificaciones no se deben enviar ni mostrar. Las excepciones incluyen comentarios que el usuario esperaría ver en respuesta a una acción del usuario, como cuando se conecta en un dispositivo USB o imprime un documento. Más adelante en este tema se describen las características específicas de la API de en relación con el tiempo de inactividad.

## <a name="creating-and-displaying-a-notification"></a>Crear y mostrar una notificación

En las secciones restantes de este tema se describe el procedimiento básico que se debe seguir para mostrar una notificación de la aplicación al usuario.

1.  [Icono Agregar un aviso](#add-a-notification-icon)
2.  [Definición de la versión de NOTIFYICONDATA](#define-the-notifyicondata-version)
3.  [Definir la apariencia y el contenido de la notificación](#define-the-notification-look-and-contents)
4.  [Comprobar el estado del usuario](#check-the-user-status)
5.  [Mostrar la notificación](#display-the-notification)
6.  [Quitar un icono](#removing-an-icon)

### <a name="add-a-notification-icon"></a>Icono Agregar un aviso

Para mostrar una notificación, debe tener un icono en el área de notificación. En algunos casos, como Microsoft Communicator o el nivel de batería, ese icono ya estará presente. En muchos otros casos, sin embargo, agregará un icono al área de notificación solo cuando sea necesario para mostrar la notificación. En cualquier caso, esto se logra mediante la [**función \_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) . **Shell \_ de NotifyIcon** permite agregar, modificar o eliminar un icono en el área de notificación.

![área de notificación que contiene tres iconos](images/taskbar/notificationareaicons.png)

Cuando se agrega un icono al área de notificación en Windows 7, se agrega de forma predeterminada a la sección de desbordamiento del área de notificación. Esta área contiene iconos del área de notificación que están activos, pero no visibles en el área de notificación. Solo el usuario puede promocionar un icono del desbordamiento en el área de notificación, aunque en determinadas circunstancias el sistema puede promover temporalmente un icono en el área de notificación como una vista previa corta (menos de un minuto).

> [!Note]  
> El usuario debe tener el final de la señal en qué iconos desea ver en el área de notificación. Antes de instalar un icono no transitorio en el área de notificación, se debe solicitar permiso al usuario. También se les debe proporcionar la opción (normalmente, a través de su menú contextual) para quitar el icono del área de notificación.

 

La estructura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) enviada en la llamada a [**\_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contiene información que especifica el icono del área de notificación y la propia notificación. A continuación se muestran los elementos específicos del propio icono del área de notificación que se pueden establecer a través de **NOTIFYICONDATA**.

-   Recurso del que se toma el icono.
-   Identificador único para el icono.
-   Estilo de la información sobre herramientas del icono.
-   El estado del icono (oculto, compartido o ambos) en el área de notificación.
-   Identificador de una ventana de la aplicación asociada al icono.
-   Un identificador de mensaje de devolución de llamada que permite al icono comunicar eventos que se producen dentro del rectángulo delimitador del icono y la notificación de globo con la ventana de la aplicación asociada. El rectángulo delimitador del icono se puede recuperar a través del [**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect).

Cada icono del área de notificación puede identificarse de dos maneras:

-   GUID con el que se declara el icono en el registro. Este es el método preferido en Windows 7 y versiones posteriores.
-   Identificador de una ventana asociada al icono del área de notificación, más un identificador de icono definido por la aplicación. Este método se utiliza en Windows Vista y versiones anteriores.

Los iconos del área de notificación pueden tener información sobre herramientas. La información sobre herramientas puede ser una información sobre herramientas estándar (preferida) o una interfaz de usuario emergente dibujada por la aplicación. Aunque no se requiere una información sobre herramientas, se recomienda.

Los iconos del área de notificación deben tener un reconocimiento de PPP alto. Una aplicación debe proporcionar un icono de 16x16 píxeles y un icono de 32x32 en su archivo de recursos y, a continuación, usar [**LoadIconMetric**](/windows/win32/api/commctrl/nf-commctrl-loadiconmetric) para asegurarse de que se carga y escala correctamente el icono correcto.

La aplicación responsable del icono del área de notificación debe controlar un clic del mouse para ese icono. Cuando un usuario hace clic con el botón secundario en el icono, debe mostrar un menú contextual normal. Sin embargo, el resultado de un solo clic con el botón primario del mouse variará con la función del icono. Debería mostrar lo que el usuario esperaría ver en el formulario más adecuado para ese contenido, una ventana emergente, un cuadro de diálogo o la propia ventana del programa. Por ejemplo, podría mostrar el texto de estado de un icono de estado o un control deslizante para el control de volumen.

La posición de un cuadro de diálogo o ventana emergente que resulte de click debe colocarse cerca de la coordenada del clic en el área de notificación. Use [**CalculatePopupWindowPosition**](/windows/win32/api/winuser/nf-winuser-calculatepopupwindowposition) para determinar su ubicación.

Se puede Agregar el icono al área de notificación sin mostrar una notificación definiendo solo los miembros específicos del icono de [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) (descrito anteriormente) y llamando [**a \_ NotifyIcon del shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) , como se muestra aquí:


```
NOTIFYICONDATA nid = {};
// Do NOT set the NIF_INFO flag.
...                    
Shell_NotifyIcon(NIM_ADD, &nid);
```



También puede Agregar el icono al área de notificación y mostrar una notificación en una llamada a NotifyIcon de [**Shell \_**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona). Para ello, continúe con las instrucciones de este tema.

### <a name="define-the-notifyicondata-version"></a>Definición de la versión de NOTIFYICONDATA

A medida que Windows ha progresado, la estructura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) se ha expandido para incluir más miembros para definir más funcionalidad. Las constantes se usan para declarar la versión de **NOTIFYICONDATA** que se va a usar con el icono del área de notificación, a fin de permitir la compatibilidad con versiones anteriores. A menos que haya una razón de peso para hacer lo contrario, se recomienda encarecidamente que use la versión de NOTIFYICON \_ versión \_ 4, que se presentó en Windows Vista. Esta versión proporciona toda la funcionalidad disponible, incluida la capacidad preferida para identificar el icono del área de notificación a través de un GUID registrado, un mecanismo de devolución de llamada superior y una mejor accesibilidad.

Establezca la versión a través de las llamadas siguientes:


```
NOTIFYICONDATA nid = {};
... 
nid.uVersion = NOTIFYICON_VERSION_4;
// Add the icon
Shell_NotifyIcon(NIM_ADD, &nid);
// Set the version
Shell_NotifyIcon(NIM_SETVERSION, &nid);
```



Tenga en cuenta que esta llamada a [**\_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) no muestra una notificación.

### <a name="define-the-notification-look-and-contents"></a>Definir la apariencia y el contenido de la notificación

Una notificación es un tipo especial de control ToolTip de globo. Contiene un título, texto de cuerpo y un icono. Al igual que una ventana, tiene un botón **cerrar** en la esquina superior derecha. También contiene un botón **Opciones** que abre el elemento iconos del área de notificación en el panel de control, que permite al usuario Mostrar u ocultar el icono o mostrar solo notificaciones sin icono.

![captura de pantalla del globo de notificación que indica que la energía de la batería es baja](images/taskbar/notificationballoon.png)

La estructura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) enviada en la llamada a [**\_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contiene información que especifica tanto el icono del área de notificación como el globo de notificación. A continuación se muestran los elementos específicos de la notificación que se pueden establecer a través de **NOTIFYICONDATA**.

-   Icono que se va a mostrar en el globo de notificación, que se especifica mediante el tipo de notificación. Se puede especificar el tamaño del icono, así como los iconos personalizados.
-   Título de la notificación. Este título debe tener una longitud máxima de 48 caracteres en inglés (para dar cabida a la localización). El título es la primera línea de la notificación y se separa mediante el uso de tamaño de fuente, color y peso.
-   Texto que se va a usar en el cuerpo de la notificación. Este texto debe tener un máximo de 200 caracteres en inglés (para dar cabida a la localización).
-   Si la notificación se debe descartar si no se puede mostrar inmediatamente.
-   Un tiempo de espera para la notificación. Este valor se omite en Windows Vista y sistemas posteriores en favor de una configuración de tiempo de espera de accesibilidad para todo el sistema.
-   Si la notificación debe respetar el tiempo de inactividad, establezca el valor de la marca [**NIIF \_ respetar el \_ \_ tiempo de silencio**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) .

> [!Note]  
> Las interfaces [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification) y [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2) son contenedores del modelo de objetos componentes (com) para el [**\_ NotifyIcon del shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona). Sin embargo, en este momento, no proporcionan la funcionalidad completa de NOTIFYICON \_ versión \_ 4 disponible a través del **\_ NotifyIcon del shell** directamente, incluido el uso de un GUID para identificar el icono del área de notificación.

 

### <a name="check-the-user-status"></a>Comprobar el estado del usuario

El sistema utiliza la función [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) se usa para comprobar si el usuario está en tiempo de inactividad, fuera del equipo o en un estado ininterrumpido como, por ejemplo, el modo de presentación. El hecho de que el sistema muestre la notificación dependerá de este estado.

> [!Note]  
> Si la aplicación usa un método de notificación personalizado que no usa el [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)o [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2), siempre debe llamar explícitamente a [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) para determinar si debe mostrar la interfaz de usuario de notificaciones en ese momento.

 

Las notificaciones que se envían cuando el usuario está en cola para su presentación, pero dado que no puede saber cuándo devolverá el usuario o si la notificación seguirá siendo válida en ese momento, considere la posibilidad de volver a enviar la notificación más adelante.

Las notificaciones enviadas durante el tiempo de inactividad se descartan. Las directrices de diseño le piden que todas las notificaciones se puedan omitir. No deben requerir la intervención inmediata del usuario. Por lo tanto, ninguna notificación es tan importante que deba invalidar el tiempo de silencio.

### <a name="display-the-notification"></a>Mostrar la notificación

Una vez que haya establecido la versión de [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) y haya definido la notificación en una estructura **NOTIFYICONDATA** , llame a [**\_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) para mostrar el icono.

-   Si no está presente el icono del área de notificación, llame a [**\_ NotifyIcon del shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) para agregar el icono. Haga esto para los iconos transitorios y no transitorios.
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_ADD, &nid);
    ```

    

-   Si el icono del área de notificación ya está presente, llame a [**\_ NotifyIcon del shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) para modificar el icono.
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_MODIFY, &nid);
    ```

    

En el código siguiente se muestra un ejemplo de configuración de datos de [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) y su envío a través del [**\_ NotifyIcon del shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona). Tenga en cuenta que en este ejemplo se identifica el icono de notificación a través de un GUID (preferido en Windows 7).


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

Para quitar un icono, por ejemplo, cuando solo se ha agregado el icono temporalmente para difundir una notificación, llame [**a \_ NotifyIcon del shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)como se muestra aquí. En esta llamada solo se necesita una estructura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) mínima que identifique el icono.


```
NOTIFYICONDATA nid = {};
...                    
Shell_NotifyIcon(NIM_DELETE, &nid);
```



> [!Note]  
> Cuando se desinstala una aplicación, es posible que el icono del área de notificación siga apareciendo al usuario como una opción en la página iconos del área de notificación del panel de control durante siete días como máximo. Sin embargo, los cambios realizados no tendrán ningún efecto.

 

## <a name="sdk-sample"></a>Ejemplo de SDK

Vea el ejemplo de [ejemplo NotificationIcon](samples-notificationicon.md) en el kit de desarrollo de software (SDK) de Windows para obtener un ejemplo completo del uso del [**\_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**NotifyIcon de Shell \_**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)
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

 

 
