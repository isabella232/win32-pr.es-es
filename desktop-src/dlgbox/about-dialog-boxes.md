---
title: cuadros de diálogo Acerca de
description: En este tema se describe el uso de cuadros de diálogo para crear interfaces de usuario para aplicaciones de.
ms.assetid: 51960c28-a178-4ad3-b45e-426fec42a945
keywords:
- cuadros de diálogo, acerca de
- cuadros de diálogo, Cuándo usar
- cuadros de diálogo modales
- cuadros de diálogo no modales
- cuadros de diálogo, modales
- cuadros de diálogo, no modales
- cuadros de diálogo, plantillas
- cuadros de diálogo, ventanas de propietario
- cuadros de diálogo, cuadros de mensaje
- procedimientos del cuadro de diálogo
- cuadros de mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dd78713c3b87e54e8a992ea9415577c522fc9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078132"
---
# <a name="about-dialog-boxes"></a>cuadros de diálogo Acerca de

Hay muchas funciones, mensajes y controles predefinidos que ayudan a crear y administrar cuadros de diálogo, lo que facilita el desarrollo de la interfaz de usuario para una aplicación. En esta información general se describen las funciones de cuadro de diálogo y los mensajes, y se explica cómo usarlos para crear y usar cuadros de diálogo.

En esta información general se incluyen los temas siguientes:

-   [Cuándo usar un cuadro de diálogo](#when-to-use-a-dialog-box)
-   [Ventana propietaria del cuadro de diálogo](#dialog-box-owner-window)
-   [Cuadros de mensaje](#message-boxes)
-   [Cuadros de diálogo modales](#modal-dialog-boxes)
-   [Cuadros de diálogo no modales](#modeless-dialog-boxes)
-   [Plantillas de cuadro de diálogo](#dialog-box-templates)
    -   [Estilos de plantilla de cuadro de diálogo](#dialog-box-template-styles)
    -   [Medidas del cuadro de diálogo](#dialog-box-measurements)
    -   [Controles de cuadro de diálogo](#dialog-box-controls)
    -   [Menú ventana de cuadro de diálogo](#dialog-box-window-menu)
    -   [Fuentes del cuadro de diálogo](#dialog-box-fonts)
    -   [Plantillas en memoria](#templates-in-memory)

Para obtener más información acerca de los cuadros de diálogo comunes, vea [Common Dialog Box Library](common-dialog-box-library.md).

## <a name="when-to-use-a-dialog-box"></a>Cuándo usar un cuadro de diálogo

La mayoría de las aplicaciones usan cuadros de diálogo para solicitar información adicional para los elementos de menú que requieren la intervención del usuario. El uso de un cuadro de diálogo es el único método recomendado para que una aplicación recupere la entrada. Por ejemplo, un elemento de menú **abierto** típico requiere el nombre de un archivo para abrirlo, por lo que una aplicación debe usar un cuadro de diálogo para pedir al usuario el nombre. En tales casos, la aplicación crea el cuadro de diálogo cuando el usuario hace clic en el elemento de menú y destruye el cuadro de diálogo inmediatamente después de que el usuario proporcione la información.

Muchas aplicaciones también utilizan cuadros de diálogo para mostrar información u opciones mientras el usuario trabaja en otra ventana. Por ejemplo, las aplicaciones de procesamiento de textos suelen usar un cuadro de diálogo con una opción de búsqueda de texto. Mientras la aplicación busca el texto, el cuadro de diálogo permanece en la pantalla. Después, el usuario puede volver al cuadro de diálogo y buscar de nuevo la misma palabra; o bien, el usuario puede cambiar la entrada en el cuadro de diálogo y buscar una nueva palabra. Las aplicaciones que usan cuadros de diálogo de esta manera normalmente crean una cuando el usuario hace clic en el elemento de menú y continúa mostrando el tiempo mientras se ejecuta la aplicación o hasta que el usuario cierra explícitamente el cuadro de diálogo.

Para admitir las distintas formas en que las aplicaciones utilizan cuadros de diálogo, hay dos tipos de cuadro de diálogo: modal y no modal. Un *cuadro de diálogo modal* requiere que el usuario proporcione información o cancele el cuadro de diálogo antes de permitir que la aplicación continúe. Las aplicaciones usan cuadros de diálogo modales junto con elementos de menú que requieren información adicional para poder continuar. Un *cuadro de diálogo no modal* permite al usuario proporcionar información y volver a la tarea anterior sin cerrar el cuadro de diálogo. Los cuadros de diálogo modales son más sencillos de administrar que los cuadros de diálogo no modales porque se crean, realizan su tarea y se destruyen llamando a una sola función.

Para crear un cuadro de diálogo modal o no modal, una aplicación debe proporcionar una plantilla de cuadro de diálogo para describir el estilo y el contenido del cuadro de diálogo. la aplicación también debe proporcionar un procedimiento de cuadro de diálogo para llevar a cabo las tareas. La *plantilla de cuadro de diálogo* es una descripción binaria del cuadro de diálogo y los controles que contiene. El desarrollador puede crear esta plantilla como un recurso que se va a cargar desde el archivo ejecutable de la aplicación, o bien crearse en la memoria mientras se ejecuta la aplicación. El *procedimiento de cuadro de diálogo* es una función de devolución de llamada definida por la aplicación a la que el sistema llama cuando tiene entrada para el cuadro de diálogo o las tareas que el cuadro de diálogo va a llevar a cabo. Aunque un procedimiento de cuadro de diálogo es similar a un procedimiento de ventana, no tiene las mismas responsabilidades.

Normalmente, una aplicación crea un cuadro de diálogo mediante la función [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) o [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) . **DialogBox** crea un cuadro de diálogo modal; **CreateDialog** crea un cuadro de diálogo no modal. Estas dos funciones cargan una plantilla de cuadro de diálogo desde el archivo ejecutable de la aplicación y crean una ventana emergente que coincide con las especificaciones de la plantilla. Hay otras funciones que crean un cuadro de diálogo mediante el uso de plantillas en memoria; pasan información adicional al procedimiento del cuadro de diálogo a medida que se crea el cuadro de diálogo.

Los cuadros de diálogo suelen pertenecer a una clase de ventana exclusiva predefinida. El sistema utiliza esta clase de ventana y su correspondiente procedimiento de ventana para los cuadros de diálogo modales y no modales. Cuando se llama a la función, se crea la ventana para el cuadro de diálogo, así como las ventanas de los controles del cuadro de diálogo y, a continuación, se envían los mensajes seleccionados al procedimiento del cuadro de diálogo. Mientras el cuadro de diálogo esté visible, el procedimiento de ventana predefinido administra todos los mensajes, procesando algunos mensajes y pasando otros al procedimiento de cuadro de diálogo para que el procedimiento pueda llevar a cabo tareas. Las aplicaciones no tienen acceso directo a la clase de ventana o al procedimiento de ventana predefinido, pero pueden usar la plantilla de cuadro de diálogo y el procedimiento de cuadro de diálogo para modificar el estilo y el comportamiento de un cuadro de diálogo.

## <a name="dialog-box-owner-window"></a>Ventana propietaria del cuadro de diálogo

La mayoría de los cuadros de diálogo tienen una ventana propietaria (o más simplemente un propietario). Al crear el cuadro de diálogo, la aplicación establece el propietario especificando el identificador de ventana del propietario. El sistema utiliza el propietario para determinar la posición del cuadro de diálogo en el orden Z, de modo que el cuadro de diálogo esté siempre situado por encima de su propietario. Además, el sistema puede enviar mensajes al procedimiento de ventana del propietario, y notificarle los eventos en el cuadro de diálogo.

El sistema oculta o destruye automáticamente el cuadro de diálogo cada vez que su propietario está oculto o destruido. Esto significa que el procedimiento del cuadro de diálogo no requiere ningún procesamiento especial para detectar los cambios en el estado de la ventana propietaria.

Dado que el cuadro de diálogo típico se usa junto con un elemento de menú, la ventana propietaria suele ser la ventana que contiene el menú. Aunque es posible crear un cuadro de diálogo sin ningún propietario, no se recomienda. Por ejemplo, cuando un cuadro de diálogo modal no tiene ningún propietario, el sistema no deshabilita ninguna otra ventana de la aplicación y permite al usuario seguir llevando a cabo el trabajo en las otras ventanas, con lo que se anula el propósito del cuadro de diálogo modal.

Cuando un cuadro de diálogo no modal no tiene ningún propietario, el sistema no oculta ni destruye el cuadro de diálogo cuando se ocultan o destruyen otras ventanas de la aplicación. Aunque esto no anula el propósito del cuadro de diálogo no modal, requiere que la aplicación lleve a cabo un procesamiento especial para asegurarse de que el cuadro de diálogo se oculta y se destruye en los momentos adecuados.

## <a name="message-boxes"></a>Cuadros de mensaje

Un cuadro de mensaje es un cuadro de diálogo especial que puede usar una aplicación para mostrar mensajes y solicitar una entrada simple. Normalmente, un cuadro de mensaje contiene un mensaje de texto y uno o varios botones. Una aplicación crea el cuadro de mensaje mediante la función [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) o [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) , especificando el texto y el número y los tipos de botones que se van a mostrar. Tenga en cuenta que actualmente no hay ninguna diferencia entre el modo en que **MessageBox** y **MessageBoxEx** funcionan.

Aunque el cuadro de mensaje es un cuadro de diálogo, el sistema toma el control completo de la creación y administración del cuadro de mensaje. Esto significa que la aplicación no proporciona un procedimiento de cuadro de diálogo y una plantilla de cuadro de diálogo. El sistema crea su propia plantilla basada en el texto y los botones especificados para el cuadro de mensaje y proporciona su propio procedimiento de cuadro de diálogo.

Un cuadro de mensaje es un cuadro de diálogo modal y el sistema lo crea con las mismas funciones internas que [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) usa. Si la aplicación especifica una ventana propietaria al llamar a [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) o [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa), el sistema deshabilita el propietario. Una aplicación también puede indicar al sistema que deshabilite todas las ventanas de nivel superior que pertenezcan al subproceso actual especificando el valor de **\_ TASKMODAL MB** al crear el cuadro de diálogo.

El sistema puede enviar mensajes al propietario, como [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) y [**WM \_ enable**](/windows/desktop/winmsg/wm-enable), al igual que cuando se crea un cuadro de diálogo modal. La ventana propietaria debe llevar a cabo cualquier acción solicitada por estos mensajes.

## <a name="modal-dialog-boxes"></a>Cuadros de diálogo modales

Un cuadro de diálogo modal debe ser una ventana emergente con un menú ventana, una barra de título y un borde grueso. es decir, la plantilla de cuadro de diálogo debe especificar los estilos **WS \_ popup**, WS **\_ SYSMENU**, **WS \_ Caption** y **\_ MODALFRAME de DS** . Aunque una aplicación puede designar el **estilo \_ visible de WS** , el sistema muestra siempre un cuadro de diálogo modal independientemente de si la plantilla de cuadro de diálogo especifica el estilo **\_ visible de WS** . Una aplicación no debe crear un cuadro de diálogo modal que tenga el estilo **WS \_ Child** . Un cuadro de diálogo modal con este estilo se deshabilita a sí mismo, lo que impide que cualquier entrada subsiguiente llegue a la aplicación.

Una aplicación crea un cuadro de diálogo modal mediante la función [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) o [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) . **DialogBox** requiere el nombre o el identificador de un recurso que contiene una plantilla de cuadro de diálogo. **DialogBoxIndirect** requiere un identificador para un objeto de memoria que contiene una plantilla de cuadro de diálogo. Las funciones [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) y [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama) también crean cuadros de diálogo modales. son idénticos a las funciones mencionadas anteriormente, pero pasan un parámetro especificado al procedimiento del cuadro de diálogo cuando se crea el cuadro de diálogo.

Al crear el cuadro de diálogo modal, el sistema lo convierte en la ventana activa. El cuadro de diálogo permanece activo hasta que el procedimiento del cuadro de diálogo llama a la función [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) o el sistema activa una ventana en otra aplicación. Ni el usuario ni la aplicación pueden activar la ventana propietaria hasta que se destruya el cuadro de diálogo modal.

Cuando la ventana propietaria no está ya deshabilitada, el sistema deshabilita automáticamente la ventana y las ventanas secundarias que pertenecen al mismo cuando crea el cuadro de diálogo modal. La ventana propietaria permanece deshabilitada hasta que se destruye el cuadro de diálogo. Aunque un procedimiento de cuadro de diálogo podría habilitar la ventana propietaria en cualquier momento, la habilitación del propietario anula el propósito del cuadro de diálogo modal y no se recomienda. Cuando se destruye el procedimiento del cuadro de diálogo, el sistema vuelve a habilitar la ventana propietaria, pero solo si el cuadro de diálogo modal hizo que se deshabilitara el propietario.

Cuando el sistema crea el cuadro de diálogo modal, envía el mensaje de [**\_ CANCELMODE de WM**](/windows/desktop/winmsg/wm-cancelmode) a la ventana (si existe) que captura actualmente la entrada del mouse. Una aplicación que recibe este mensaje debe liberar la captura del mouse para que el usuario pueda desplace el mouse en el cuadro de diálogo modal. Dado que el sistema deshabilita la ventana propietaria, se pierde toda la entrada del mouse si el propietario no puede soltar el mouse al recibir este mensaje.

Para procesar mensajes para el cuadro de diálogo modal, el sistema inicia su propio bucle de mensajes y toma el control temporal de la cola de mensajes para toda la aplicación. Cuando el sistema recupera un mensaje que no es explícitamente para el cuadro de diálogo, envía el mensaje a la ventana correspondiente. Si recupera un mensaje de [**\_ salida de WM**](/windows/desktop/winmsg/wm-quit) , devuelve el mensaje a la cola de mensajes de la aplicación para que el bucle de mensajes principal de la aplicación pueda recuperar el mensaje.

El sistema envía el mensaje de [**WM \_ ENTERIDLE**](wm-enteridle.md) a la ventana propietaria siempre que la cola de mensajes de aplicación esté vacía. La aplicación puede usar este mensaje para llevar a cabo una tarea en segundo plano mientras el cuadro de diálogo permanece en la pantalla. Cuando una aplicación utiliza el mensaje de esta manera, la aplicación debe proporcionar el control con frecuencia (por ejemplo, mediante la función [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) ) para que el cuadro de diálogo modal pueda recibir cualquier entrada del usuario. Para evitar que el cuadro de diálogo modal envíe los mensajes de **\_ ENTERIDLE de WM** , la aplicación puede especificar el estilo de NOIDLEMSG de DS \_ al crear el cuadro de diálogo.

Una aplicación destruye un cuadro de diálogo modal mediante la función [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) . En la mayoría de los casos, el procedimiento de cuadro de diálogo llama a **EndDialog** cuando el usuario hace clic en **cerrar** en el menú ventana del cuadro de diálogo o hace clic en el botón **Aceptar** o **Cancelar** en el cuadro de diálogo. El cuadro de diálogo puede devolver un valor a través de la función [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) (u otras funciones de creación) especificando un valor al llamar a la función **EndDialog** . El sistema devuelve este valor después de destruir el cuadro de diálogo. La mayoría de las aplicaciones usan este valor devuelto para determinar si el cuadro de diálogo completó correctamente la tarea o el usuario canceló su tarea. El sistema no devuelve el control de la función que crea el cuadro de diálogo hasta que el procedimiento del cuadro de diálogo haya llamado a la función **EndDialog** .

## <a name="modeless-dialog-boxes"></a>Cuadros de diálogo no modales

Un cuadro de diálogo no modal debe ser una ventana emergente con un menú ventana, una barra de título y un borde fino. es decir, la plantilla de cuadro de diálogo debe especificar los estilos **WS \_ popup**, WS **\_ Caption**, **WS \_ Border** y **WS \_ SYSMENU** . El sistema no muestra automáticamente el cuadro de diálogo a menos que la plantilla especifique el estilo **\_ visible de WS** .

Una aplicación crea un cuadro de diálogo no modal mediante la función [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) o [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta) . **CreateDialog** requiere el nombre o el identificador de un recurso que contenga una plantilla de cuadro de diálogo. **CreateDialogIndirect** requiere un identificador para un objeto de memoria que contiene una plantilla de cuadro de diálogo. Otras dos funciones, [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama) y [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), también crean cuadros de diálogo no modales; pasan un parámetro especificado al procedimiento del cuadro de diálogo cuando se crea el cuadro de diálogo.

[**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) y otras funciones de creación devuelven un identificador de ventana para el cuadro de diálogo. La aplicación y el procedimiento del cuadro de diálogo pueden utilizar este identificador para administrar el cuadro de diálogo. Por ejemplo, si no se especifica **WS \_ visible** en la plantilla de cuadro de diálogo, la aplicación puede mostrar el cuadro de diálogo pasando el identificador de ventana a la función [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) .

Un cuadro de diálogo no modal no deshabilita la ventana propietaria ni le envía mensajes. Al crear el cuadro de diálogo, el sistema lo convierte en la ventana activa, pero el usuario o la aplicación pueden cambiar la ventana activa en cualquier momento. Si el cuadro de diálogo se vuelve inactivo, permanece por encima de la ventana propietaria en el orden Z, incluso si la ventana propietaria está activa.

La aplicación es responsable de recuperar y enviar mensajes de entrada al cuadro de diálogo. La mayoría de las aplicaciones usan el bucle de mensajes principal para este. Sin embargo, para permitir que el usuario se mueva y seleccione controles mediante el teclado, la aplicación debe llamar a la función [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) . Para obtener más información sobre esta función, vea [interfaz de teclado de cuadro de diálogo](dlgbox-programming-considerations.md).

Un cuadro de diálogo no modal no puede devolver un valor a la aplicación como un cuadro de diálogo modal, pero el procedimiento de cuadro de diálogo puede enviar información a la ventana propietaria mediante la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .

Una aplicación debe destruir todos los cuadros de diálogo no modales antes de terminar. Puede destruir un cuadro de diálogo no modal mediante la función [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) . En la mayoría de los casos, el procedimiento de cuadro de diálogo llama a **DestroyWindow** en respuesta a la entrada del usuario, como hacer clic en el botón **Cancelar** . Si el usuario nunca cierra el cuadro de diálogo de esta manera, la aplicación debe llamar a **DestroyWindow**.

[**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) invalida el identificador de ventana del cuadro de diálogo, de modo que las llamadas subsiguientes a las funciones que utilizan el identificador devuelven valores de error. Para evitar errores, el procedimiento del cuadro de diálogo debe notificar al propietario que el cuadro de diálogo se ha destruido. Muchas aplicaciones mantienen una variable global que contiene el identificador del cuadro de diálogo. Cuando el procedimiento del cuadro de diálogo destruye el cuadro de diálogo, también establece la variable global en **null**, lo que indica que el cuadro de diálogo ya no es válido.

El procedimiento de cuadro de diálogo no debe llamar a la función [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) para destruir un cuadro de diálogo no modal.

## <a name="dialog-box-templates"></a>Plantillas de cuadro de diálogo

Una plantilla de cuadro de diálogo son datos binarios que describen el cuadro de diálogo, que definen el alto, el ancho, el estilo y los controles que contiene. Para crear un cuadro de diálogo, el sistema carga una plantilla de cuadro de diálogo de los recursos en el archivo ejecutable de la aplicación o usa la plantilla que la aplicación pasa en la memoria global. En cualquier caso, la aplicación debe proporcionar una plantilla al crear un cuadro de diálogo.

Un desarrollador crea recursos de plantilla mediante un compilador de recursos o un editor de cuadros de diálogo. Un compilador de recursos convierte una descripción de texto en un recurso binario y un editor de cuadros de diálogo guarda un cuadro de diálogo construido de forma interactiva como un recurso binario.

> [!Note]  
> Una explicación de cómo crear recursos de plantilla y agregarlos al archivo ejecutable de la aplicación está fuera del ámbito de esta información general. Para obtener más información sobre cómo crear recursos de plantilla y cómo agregarlos a un archivo ejecutable, vea la documentación que se proporciona con las herramientas de desarrollo de aplicaciones.

 

Para crear un cuadro de diálogo sin usar recursos de plantilla, debe crear una plantilla en memoria y pasarla a la función [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama) o [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama) , o bien a la macro [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta) o [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) .

Una plantilla de cuadro de diálogo en memoria consta de un encabezado que describe el cuadro de diálogo, seguido de uno o varios bloques de datos adicionales que describen cada uno de los controles del cuadro de diálogo. La plantilla puede usar el formato estándar o el formato extendido. En una plantilla estándar, el encabezado es una estructura [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) seguida de matrices de longitud variable adicionales; y los datos de cada control se componen de una estructura [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) seguida de matrices de longitud variable adicionales. En una plantilla de cuadro de diálogo extendido, el encabezado usa el formato [**DLGTEMPLATEEX**](dlgtemplateex.md) y las definiciones de control usan el formato [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) .

Puede crear una plantilla de memoria asignando un objeto de memoria global y rellenándolo con las definiciones de control y encabezado estándar o extendido. Una plantilla de memoria es idéntica en el formulario y el contenido a un recurso de plantilla. Muchas aplicaciones que usan plantillas de memoria usan primero la función [**LoadResource**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource) para cargar un recurso de plantilla en la memoria y, a continuación, modificar el recurso cargado para crear una nueva plantilla de memoria. Para obtener más información sobre cómo crear una plantilla de cuadro de diálogo en memoria, vea [plantillas en memoria](#templates-in-memory).

En las secciones siguientes se describen los estilos, las medidas y otros valores que se usan en una plantilla de cuadro de diálogo.

-   [Estilos de plantilla de cuadro de diálogo](#dialog-box-template-styles)
-   [Medidas del cuadro de diálogo](#dialog-box-measurements)
-   [Controles de cuadro de diálogo](#dialog-box-controls)
-   [Menú ventana de cuadro de diálogo](#dialog-box-window-menu)
-   [Fuentes del cuadro de diálogo](#dialog-box-fonts)
-   [Plantillas en memoria](#templates-in-memory)

### <a name="dialog-box-template-styles"></a>Estilos de plantilla de cuadro de diálogo

Cada plantilla de cuadro de diálogo especifica una combinación de valores de estilo que definen la apariencia y las características del cuadro de diálogo. Los valores de estilo pueden ser estilos de ventana, como **WS \_ popup** y **WS \_ SYSMENU**, y estilos de cuadro de diálogo, como **DS \_ MODALFRAME**. El número y tipo de estilos de una plantilla depende del tipo y el propósito del cuadro de diálogo. Para obtener una lista de valores, vea [**estilos de cuadro de diálogo**](dialog-box-styles.md).

El sistema pasa todos los estilos de ventana especificados en la plantilla a la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) al crear el cuadro de diálogo. El sistema puede pasar uno o varios estilos extendidos en función de los estilos de cuadro de diálogo especificados. Por ejemplo, cuando la plantilla especifica **DS \_ MODALFRAME**, el sistema usa **WS \_ ex \_ DLGMODALFRAME** al crear el cuadro de diálogo.

La mayoría de los cuadros de diálogo son ventanas emergentes que tienen un menú ventana y una barra de título. Por lo tanto, la plantilla típica especifica los estilos **\_ emergente WS**, WS **\_ SYSMENU** y **WS \_ Caption** . La plantilla también especifica un estilo de borde: **WS \_ Border** para los cuadros de diálogo no modales y **\_ MODALFRAME DS** para los cuadros de diálogo modales. Una plantilla puede especificar un tipo de ventana que no sea un elemento emergente (como **WS \_ superpuesto**) si crea una ventana personalizada en lugar de un cuadro de diálogo.

El sistema siempre muestra un cuadro de diálogo modal independientemente de si se ha especificado el estilo **WS \_ visible** . Cuando la plantilla de un cuadro de diálogo no modal especifica el estilo **\_ visible de WS** , el sistema muestra automáticamente el cuadro de diálogo cuando se crea. De lo contrario, la aplicación es responsable de mostrar el cuadro de diálogo mediante la función [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) .

### <a name="dialog-box-measurements"></a>Medidas del cuadro de diálogo

Cada plantilla de cuadro de diálogo contiene medidas que especifican la posición, el ancho y el alto del cuadro de diálogo y los controles que contiene. Estas medidas son independientes del dispositivo, por lo que una aplicación puede usar una sola plantilla para crear el mismo cuadro de diálogo para todos los tipos de dispositivos de pantalla. Esto garantiza que un cuadro de diálogo tendrá las mismas proporciones y apariencia en todas las pantallas, a pesar de las distintas resoluciones y relaciones de aspecto entre las pantallas.

Las medidas de una plantilla de cuadros de diálogo se especifican en unidades de plantilla de cuadro de diálogo. Para convertir las medidas de las unidades de plantilla de cuadro de diálogo en unidades de pantalla (píxeles), use la función [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) , que tiene en cuenta la fuente usada por el cuadro de diálogo y convierte correctamente un rectángulo de las unidades de plantilla de cuadro de diálogo en píxeles. En los cuadros de diálogo que usan la fuente del sistema, puede usar la función [**GetDialogBaseUnits**](/windows/desktop/api/Winuser/nf-winuser-getdialogbaseunits) para realizar los cálculos de conversión por su cuenta, aunque el uso de **MapDialogRect** es más sencillo.

La plantilla debe especificar las coordenadas iniciales de la esquina superior izquierda del cuadro de diálogo. Normalmente, las coordenadas son relativas a la esquina superior izquierda del área de cliente de la ventana propietaria. Cuando la plantilla especifica el \_ estilo ABSALIGN de DS o el cuadro de diálogo no tiene ningún propietario, la posición es relativa a la esquina superior izquierda de la pantalla. El sistema establece esta posición inicial al crear el cuadro de diálogo, pero permite que una aplicación ajuste la posición antes de mostrar el cuadro de diálogo. Por ejemplo, una aplicación puede recuperar las dimensiones de la ventana propietaria, calcular una nueva posición que centra el cuadro de diálogo en la ventana propietaria y, a continuación, establecer la posición mediante la función [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) .

La plantilla debe especificar el ancho y el alto de un cuadro de diálogo que no supere el ancho y el alto de la pantalla, y garantiza que todos los controles estén dentro del área cliente del cuadro de diálogo. Aunque el sistema permite que un cuadro de diálogo tenga cualquier tamaño, crear uno que sea demasiado pequeño o demasiado grande puede impedir que el usuario proporcione una entrada, con lo que se anulará la finalidad del cuadro de diálogo. Muchas aplicaciones usan más de un cuadro de diálogo cuando hay un gran número de controles. En tales casos, el cuadro de diálogo inicial normalmente contiene uno o más botones que el usuario puede elegir para mostrar el siguiente cuadro de diálogo.

### <a name="dialog-box-controls"></a>Controles de cuadro de diálogo

La plantilla especifica la posición, el ancho, el alto, el estilo, el identificador y la clase de ventana para cada control del cuadro de diálogo. El sistema crea cada control pasando estos datos a la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . Los controles se crean en el orden en que se especifican en la plantilla. La plantilla debe especificar el número, el tipo y el orden de los controles adecuados para asegurarse de que el usuario puede especificar la entrada necesaria para completar la tarea asociada al cuadro de diálogo.

Para cada control, la plantilla especifica valores de estilo que definen la apariencia y el funcionamiento del control. Cada control es una ventana secundaria y, por lo tanto, debe tener el estilo de **WS \_ secundario** . Para asegurarse de que el control está visible cuando se muestra el cuadro de diálogo, cada control también debe tener el estilo de **WS \_ visible** . Otros estilos de ventana utilizados habitualmente son el **\_ borde WS** para los controles que tienen bordes opcionales, **WS \_ deshabilitado** para los controles que se deben deshabilitar cuando se crea el cuadro de diálogo inicialmente, y **WS \_ TABSTOP** y el **\_ Grupo WS** para los controles a los que se puede tener acceso mediante el teclado. Los estilos **WS \_ TABSTOP** y **\_ Grupo WS** se usan junto con la interfaz de teclado del cuadro de diálogo que se describe más adelante en este tema.

La plantilla también puede especificar estilos de control específicos de la clase de ventana del control. Por ejemplo, una plantilla que especifica un control de botón debe proporcionar un estilo de control de botón como la **\_ casilla de verificación** **BS \_** o BS. El sistema pasa los estilos de control al procedimiento de ventana de control a través del mensaje de [**\_ creación de WM**](/windows/desktop/winmsg/wm-create) , lo que permite al procedimiento adaptar la apariencia y el funcionamiento del control.

El sistema convierte las coordenadas de posición y las medidas de ancho y alto de las unidades base del cuadro de diálogo a píxeles, antes de pasarlas a [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Cuando el sistema crea un control, especifica el cuadro de diálogo como la ventana primaria. Esto significa que el sistema siempre interpreta las coordenadas de posición del control como coordenadas de cliente, en relación con la esquina superior izquierda del área cliente del cuadro de diálogo.

La plantilla especifica la clase de ventana para cada control. Un cuadro de diálogo típico contiene controles que pertenecen a las clases de ventana de control predefinidas, como las clases Button y Edit control window. En este caso, la plantilla especifica las clases de ventana proporcionando los valores de Atom predefinidos correspondientes para las clases. Cuando un cuadro de diálogo contiene un control que pertenece a una clase de ventana de control personalizada, la plantilla proporciona el nombre de esa clase de ventana registrada o el valor Atom asociado actualmente al nombre.

Cada control de un cuadro de diálogo debe tener un identificador único para distinguirlo de otros controles. Los controles envían información al procedimiento del cuadro de diálogo a través de los mensajes de [**\_ comandos de WM**](/windows/desktop/menurc/wm-command) , por lo que los identificadores de control son esenciales para que el procedimiento determine qué control envió un mensaje especificado. La única excepción a esta regla son los identificadores de control de los controles estáticos. Los controles estáticos no requieren identificadores únicos porque no envían ningún mensaje de **\_ comando de WM** .

Para permitir que el usuario cierre el cuadro de diálogo, la plantilla debe especificar al menos un botón de reenvío y asignarle el identificador de control **IDCANCEL**. Para permitir al usuario elegir entre completar o cancelar la tarea asociada con el cuadro de diálogo, la plantilla debe especificar dos botones de reenvío, etiquetados como **Aceptar** y **Cancelar**, con los identificadores de control de **IDOK** y **IDCANCEL**, respectivamente.

Una plantilla también especifica el texto opcional y los datos de creación de un control. Normalmente, el texto proporciona etiquetas para los controles de botón o especifica el contenido inicial de un control de texto estático. Los datos de creación son uno o más bytes de datos que el sistema pasa al procedimiento de ventana de control al crear el control. Los datos de creación son útiles para los controles que requieren más información sobre su contenido o estilo inicial que el especificado por otros datos. Por ejemplo, una aplicación puede utilizar datos de creación para establecer la configuración inicial y el intervalo para un control de barra de desplazamiento.

### <a name="dialog-box-window-menu"></a>Menú ventana de cuadro de diálogo

El sistema proporciona un cuadro de diálogo a un menú ventana cuando la plantilla especifica el estilo **WS \_ SYSMENU** . Para evitar una entrada inadecuada, el sistema deshabilita automáticamente todos los elementos del menú, excepto el **movimiento** y el **cierre**. El usuario puede hacer clic en **movimiento** para desplace el cuadro de diálogo. Cuando el usuario hace clic en **cerrar**, el sistema envía un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) al procedimiento del cuadro de diálogo con el parámetro *wParam* establecido en **IDCANCEL**. Es idéntico al mensaje enviado por el botón **Cancelar** cuando el usuario hace clic en él. La acción recomendada para este mensaje es cerrar el cuadro de diálogo y cancelar la tarea solicitada.

Aunque no se recomiendan otros menús de cuadros de diálogo, una plantilla de cuadro de diálogo puede especificar un menú proporcionando el identificador o el nombre de un recurso de menú. En este caso, el sistema carga el recurso y crea el menú para el cuadro de diálogo. Las aplicaciones suelen usar identificadores o nombres de menú en las plantillas al usar las plantillas para crear ventanas personalizadas en lugar de cuadros de diálogo.

### <a name="dialog-box-fonts"></a>Fuentes del cuadro de diálogo

El sistema utiliza el ancho medio de caracteres de la fuente del cuadro de diálogo para calcular la posición y las dimensiones del cuadro de diálogo. De forma predeterminada, el sistema dibuja todo el texto en un cuadro de diálogo con la fuente **del sistema \_** .

Para especificar una fuente para un cuadro de diálogo distinto del predeterminado, debe crear el cuadro de diálogo mediante una plantilla de cuadro de diálogo. En un recurso de plantilla, use la [instrucción Font](../menurc/font-statement.md). En una plantilla de cuadro de diálogo, establezca el estilo de **DS \_ SETFONT** o **DS \_ SHELLFONT** y especifique un nombre de punto y un nombre de tipo de letra. Incluso si una plantilla de cuadro de diálogo especifica una fuente de esta manera, el sistema siempre usa la fuente del sistema para los menús de cuadro de diálogo y de título del cuadro de diálogo.

Cuando el cuadro de diálogo tiene el estilo **DS \_ SetFont** o **DS \_ SHELLFONT** , el sistema envía un mensaje de [**WM \_ SetFont**](/windows/desktop/winmsg/wm-setfont) al procedimiento del cuadro de diálogo y a cada control a medida que crea el control. El procedimiento de cuadro de diálogo es responsable de guardar el identificador de fuente que se ha pasado con el mensaje de **WM \_ SETFONT** y de seleccionar el identificador en el contexto de dispositivo de pantalla cada vez que escribe texto en la ventana. Los controles predefinidos lo hacen de forma predeterminada.

La fuente del sistema puede variar entre diferentes versiones de Windows. Para que la aplicación use la fuente del sistema independientemente del sistema en el que se esté ejecutando, use el **\_ SHELLFONT de DS** con el tipo de letra MS Shell Dlg y use el [recurso DIALOGEX](../menurc/dialogex-resource.md) en lugar del [recurso de cuadro de diálogo](../menurc/dialog-resource.md). El sistema asigna este tipo de letra de forma que el cuadro de diálogo use la fuente Tahoma. Tenga en cuenta que **DS \_ SHELLFONT** no tiene ningún efecto si el tipo de letra no es ms Shell Dlg.

### <a name="templates-in-memory"></a>Plantillas en memoria

Una plantilla de cuadro de diálogo en memoria consta de un encabezado que describe el cuadro de diálogo, seguido de uno o varios bloques de datos adicionales que describen cada uno de los controles del cuadro de diálogo. La plantilla puede usar el formato estándar o el formato extendido. En una plantilla estándar, el encabezado es una estructura [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) seguida por matrices de longitud variable adicionales. Los datos de cada control se componen de una estructura [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) seguida de matrices de longitud variable adicionales. En una plantilla de cuadro de diálogo extendido, el encabezado usa el formato [**DLGTEMPLATEEX**](dlgtemplateex.md) y las definiciones de control usan el formato [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) .

Para distinguir entre una plantilla estándar y una plantilla extendida, compruebe los primeros 16 bits de una plantilla de cuadro de diálogo. En una plantilla extendida, la primera **palabra** es 0xFFFF; cualquier otro valor indica una plantilla estándar.

Si crea una plantilla de cuadro de diálogo en memoria, debe asegurarse de que cada una de las definiciones de control [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) o [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) se alinee en los límites **DWORD** . Además, los datos de creación que siguen a una definición de control se deben alinear en un límite **DWORD** . Todas las demás matrices de longitud variable de una plantilla de cuadro de diálogo se deben alinear en los límites de **palabras** .

### <a name="template-header"></a>Encabezado de plantilla

En las plantillas estándar y extendido para los cuadros de diálogo, el encabezado incluye la siguiente información general:

-   La ubicación y las dimensiones del cuadro de diálogo
-   Estilos de ventana y de cuadro de diálogo para el cuadro de diálogo
-   Número de controles del cuadro de diálogo. Este valor determina el número de definiciones de control [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) o [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) de la plantilla.
-   Un recurso de menú opcional para el cuadro de diálogo. La plantilla puede indicar que el cuadro de diálogo no tiene un menú, o puede especificar un valor ordinal o una cadena Unicode terminada en null que identifique un recurso de menú en un archivo ejecutable.
-   Clase de ventana del cuadro de diálogo. Puede ser la clase de cuadro de diálogo predefinida, o un valor ordinal o una cadena Unicode terminada en null que identifica una clase de ventana registrada.
-   Una cadena Unicode terminada en null que especifica el título de la ventana de cuadro de diálogo. Si la cadena está vacía, la barra de título del cuadro de diálogo está en blanco. Si el cuadro de diálogo no tiene el estilo de **\_ título de WS** , el sistema establece el título en la cadena especificada, pero no lo muestra.
-   Si el cuadro de diálogo tiene el estilo **DS \_ SETFONT** , el encabezado especifica el tamaño de punto y el nombre del tipo de letra de la fuente que se va a usar para el texto en el área cliente y los controles del cuadro de diálogo.

En una plantilla extendida, el encabezado [**DLGTEMPLATEEX**](dlgtemplateex.md) también especifica la siguiente información adicional:

-   Identificador de contexto de ayuda de la ventana de cuadro de diálogo cuando el sistema envía un mensaje de [**\_ ayuda de WM**](../shell/wm-help.md) .
-   Si el cuadro de diálogo tiene el estilo **DS \_ SETFONT** o **DS \_ SHELLFONT** , el encabezado especifica el espesor de la fuente e indica si la fuente está en cursiva.

### <a name="control-definitions"></a>Definiciones de control

El siguiente encabezado de plantilla es una o varias definiciones de control que describen los controles del cuadro de diálogo. En las plantillas estándar y extendidas, el encabezado del cuadro de diálogo tiene un miembro que indica el número de definiciones de control de la plantilla. En una plantilla estándar, cada definición de control está formada por una estructura [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) seguida por matrices de longitud variable adicionales. En una plantilla extendida, las definiciones de control utilizan el formato [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) .

En las plantillas estándar y extendidos, la definición de control incluye la siguiente información:

-   La ubicación y las dimensiones del control.
-   Estilos de ventana y de control para el control.
-   Identificador del control.
-   Clase de ventana del control. Puede ser el valor ordinal de una clase del sistema predefinida o una cadena Unicode terminada en null que especifica el nombre de una clase de ventana registrada.
-   Una cadena Unicode terminada en null que especifica el texto inicial del control, o un valor ordinal que identifica un recurso, como un icono, en un archivo ejecutable.
-   Un bloque opcional de longitud variable de datos de creación. Cuando el sistema crea el control, pasa un puntero a estos datos en el parámetro *lParam* del mensaje de [**\_ creación de WM**](/windows/desktop/winmsg/wm-create) que envía al control.

En una plantilla extendida, la definición de control también especifica un identificador de contexto de ayuda para el control cuando el sistema envía un mensaje de [**\_ ayuda de WM**](../shell/wm-help.md) .

 

 