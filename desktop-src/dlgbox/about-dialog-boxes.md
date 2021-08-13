---
title: cuadros de diálogo Acerca de
description: En este tema se describe el uso de cuadros de diálogo para crear interfaces de usuario para aplicaciones.
ms.assetid: 51960c28-a178-4ad3-b45e-426fec42a945
keywords:
- cuadros de diálogo, acerca de
- cuadros de diálogo, cuándo usar
- cuadros de diálogo modales
- cuadros de diálogo no modales
- cuadros de diálogo, modal
- cuadros de diálogo, modeless
- cuadros de diálogo, plantillas
- cuadros de diálogo, ventanas de propietario
- cuadros de diálogo, cuadros de mensaje
- procedimientos del cuadro de diálogo
- cuadros de mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7855ba67a04558e0df8ffad0f63d2bd78856f84829bf029fbf811a4b89eb4b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786813"
---
# <a name="about-dialog-boxes"></a>cuadros de diálogo Acerca de

Hay muchas funciones, mensajes y controles predefinidos para ayudar a crear y administrar cuadros de diálogo, lo que facilita el desarrollo de la interfaz de usuario para una aplicación. En esta introducción se describen las funciones y mensajes del cuadro de diálogo y se explica cómo usarlas para crear y usar cuadros de diálogo.

Esta información general incluye los temas siguientes:

-   [Cuándo usar un cuadro de diálogo](#when-to-use-a-dialog-box)
-   [Ventana propietario del cuadro de diálogo](#dialog-box-owner-window)
-   [Cuadros de mensaje](#message-boxes)
-   [Cuadros de diálogo modales](#modal-dialog-boxes)
-   [Cuadros de diálogo de modeless](#modeless-dialog-boxes)
-   [Plantillas de cuadro de diálogo](#dialog-box-templates)
    -   [Estilos de plantilla de cuadro de diálogo](#dialog-box-template-styles)
    -   [Medidas del cuadro de diálogo](#dialog-box-measurements)
    -   [Controles de cuadro de diálogo](#dialog-box-controls)
    -   [Menú ventana cuadro de diálogo](#dialog-box-window-menu)
    -   [Fuentes del cuadro de diálogo](#dialog-box-fonts)
    -   [Plantillas en memoria](#templates-in-memory)

Para obtener más información sobre los cuadros de diálogo comunes, vea [Common Dialog Box Library](common-dialog-box-library.md).

## <a name="when-to-use-a-dialog-box"></a>Cuándo usar un cuadro de diálogo

La mayoría de las aplicaciones usan cuadros de diálogo para solicitar información adicional sobre los elementos de menú que requieren la entrada del usuario. El uso de un cuadro de diálogo es la única manera recomendada para que una aplicación recupere la entrada. Por ejemplo, un **elemento** de menú Abrir típico requiere que se abra el nombre de un archivo, por lo que una aplicación debe usar un cuadro de diálogo para solicitar el nombre al usuario. En tales casos, la aplicación crea el cuadro de diálogo cuando el usuario hace clic en el elemento de menú y destruye el cuadro de diálogo inmediatamente después de que el usuario proporciona la información.

Muchas aplicaciones también usan cuadros de diálogo para mostrar información u opciones mientras el usuario trabaja en otra ventana. Por ejemplo, las aplicaciones de procesamiento de texto suelen usar un cuadro de diálogo con una opción de búsqueda de texto. Mientras la aplicación busca el texto, el cuadro de diálogo permanece en la pantalla. A continuación, el usuario puede volver al cuadro de diálogo y volver a buscar la misma palabra. o el usuario puede cambiar la entrada en el cuadro de diálogo y buscar una palabra nueva. Las aplicaciones que usan cuadros de diálogo de esta manera suelen crear uno cuando el usuario hace clic en el elemento de menú y lo siguen mostrando mientras se ejecute la aplicación o hasta que el usuario cierre explícitamente el cuadro de diálogo.

Para admitir las distintas formas en que las aplicaciones usan cuadros de diálogo, hay dos tipos de cuadro de diálogo: modal y modeless. Un *cuadro de diálogo modal* requiere que el usuario proporcione información o cancele el cuadro de diálogo antes de permitir que la aplicación continúe. Las aplicaciones usan cuadros de diálogo modales junto con elementos de menú que requieren información adicional antes de poder continuar. Un *cuadro de diálogo no* modelo permite al usuario proporcionar información y volver a la tarea anterior sin cerrar el cuadro de diálogo. Los cuadros de diálogo modales son más fáciles de administrar que los cuadros de diálogo no modales porque se crean, realizan su tarea y se destruyen mediante una llamada a una sola función.

Para crear un cuadro de diálogo modal o no modal, una aplicación debe proporcionar una plantilla de cuadro de diálogo para describir el estilo y el contenido del cuadro de diálogo; La aplicación también debe proporcionar un procedimiento de cuadro de diálogo para llevar a cabo tareas. La *plantilla de cuadro de* diálogo es una descripción binaria del cuadro de diálogo y los controles que contiene. El desarrollador puede crear esta plantilla como un recurso que se cargará desde el archivo ejecutable de la aplicación o se creará en memoria mientras se ejecuta la aplicación. El *procedimiento del cuadro de diálogo* es una función de devolución de llamada definida por la aplicación a la que el sistema llama cuando tiene una entrada para el cuadro de diálogo o las tareas que debe llevar a cabo el cuadro de diálogo. Aunque un procedimiento de cuadro de diálogo es similar a un procedimiento de ventana, no tiene las mismas responsabilidades.

Normalmente, una aplicación crea un cuadro de diálogo mediante la [**función DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) [**o CreateDialog.**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) **DialogBox** crea un cuadro de diálogo modal; **CreateDialog** crea un cuadro de diálogo no modelo. Estas dos funciones cargan una plantilla de cuadro de diálogo desde el archivo ejecutable de la aplicación y crean una ventana emergente que coincida con las especificaciones de la plantilla. Hay otras funciones que crean un cuadro de diálogo mediante plantillas en memoria; pasan información adicional al procedimiento del cuadro de diálogo a medida que se crea el cuadro de diálogo.

Los cuadros de diálogo suelen pertenecer a una clase de ventana exclusiva predefinida. El sistema usa esta clase de ventana y su procedimiento de ventana correspondiente para los cuadros de diálogo modales y no modales. Cuando se llama a la función, crea la ventana para el cuadro de diálogo, así como las ventanas de los controles del cuadro de diálogo y, a continuación, envía los mensajes seleccionados al procedimiento del cuadro de diálogo. Mientras el cuadro de diálogo está visible, el procedimiento de ventana predefinido administra todos los mensajes, procesa algunos mensajes y pasa otros al procedimiento del cuadro de diálogo para que el procedimiento pueda llevar a cabo tareas. Las aplicaciones no tienen acceso directo a la clase de ventana predefinida o al procedimiento de ventana, pero pueden usar la plantilla de cuadro de diálogo y el procedimiento del cuadro de diálogo para modificar el estilo y el comportamiento de un cuadro de diálogo.

## <a name="dialog-box-owner-window"></a>Ventana propietario del cuadro de diálogo

La mayoría de los cuadros de diálogo tienen una ventana de propietario (o más simplemente, un propietario). Al crear el cuadro de diálogo, la aplicación establece el propietario especificando el identificador de ventana del propietario. El sistema usa el propietario para determinar la posición del cuadro de diálogo en el orden Z para que el cuadro de diálogo siempre se coloque por encima de su propietario. Además, el sistema puede enviar mensajes al procedimiento de ventana del propietario y notificarle los eventos del cuadro de diálogo.

El sistema oculta o destruye automáticamente el cuadro de diálogo cada vez que su propietario se oculta o destruye. Esto significa que el procedimiento del cuadro de diálogo no requiere ningún procesamiento especial para detectar cambios en el estado de la ventana de propietario.

Dado que el cuadro de diálogo típico se usa junto con un elemento de menú, la ventana propietaria suele ser la ventana que contiene el menú. Aunque es posible crear un cuadro de diálogo sin propietario, no se recomienda. Por ejemplo, cuando un cuadro de diálogo modal no tiene ningún propietario, el sistema no deshabilita ninguna de las otras ventanas de la aplicación y permite al usuario seguir trabajando en las otras ventanas, con lo que se deshabilite el propósito del cuadro de diálogo modal.

Cuando un cuadro de diálogo no tiene propietario, el sistema no oculta ni destruye el cuadro de diálogo cuando se ocultan o destruyen otras ventanas de la aplicación. Aunque esto no pierde el propósito del cuadro de diálogo modeless, requiere que la aplicación lleve a cabo un procesamiento especial para asegurarse de que el cuadro de diálogo se oculta y se destruye en los momentos adecuados.

## <a name="message-boxes"></a>Cuadros de mensaje

Un cuadro de mensaje es un cuadro de diálogo especial que una aplicación puede usar para mostrar mensajes y solicitar una entrada sencilla. Normalmente, un cuadro de mensaje contiene un mensaje de texto y uno o varios botones. Una aplicación crea el cuadro de mensaje mediante la función [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) o [**MessageBoxEx,**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) especificando el texto y el número y los tipos de botones que se mostrarán. Tenga en cuenta que actualmente no hay ninguna diferencia entre cómo **funcionan MessageBox** y **MessageBoxEx.**

Aunque el cuadro de mensaje es un cuadro de diálogo, el sistema toma el control completo de la creación y administración del cuadro de mensaje. Esto significa que la aplicación no proporciona una plantilla de cuadro de diálogo ni un procedimiento de cuadro de diálogo. El sistema crea su propia plantilla basada en el texto y los botones especificados para el cuadro de mensaje y proporciona su propio procedimiento de cuadro de diálogo.

Un cuadro de mensaje es un cuadro de diálogo modal y el sistema lo crea mediante las mismas funciones internas que [**usa DialogBox.**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) Si la aplicación especifica una ventana de propietario al llamar a [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) o [**MessageBoxEx,**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa)el sistema deshabilita el propietario. Una aplicación también puede indicar al sistema que deshabilite todas las ventanas de nivel superior que pertenecen al subproceso actual especificando el valor **DE MB \_ TASKMODAL** al crear el cuadro de diálogo.

El sistema puede enviar mensajes al propietario, como [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) y [**WM \_ ENABLE,**](/windows/desktop/winmsg/wm-enable)igual que al crear un cuadro de diálogo modal. La ventana de propietario debe llevar a cabo las acciones solicitadas por estos mensajes.

## <a name="modal-dialog-boxes"></a>Cuadros de diálogo modales

Un cuadro de diálogo modal debe ser una ventana emergente que tenga un menú de ventana, una barra de título y un borde grueso; Es decir, la plantilla de cuadro de diálogo debe especificar los estilos POPUP de **WS, \_** **WS \_ SYSMENU,** **WS \_ CAPTION** y **\_ MODALFRAME de DS.** Aunque una aplicación puede designar el estilo **WS \_ VISIBLE,** el sistema siempre muestra un cuadro de diálogo modal independientemente de si la plantilla de cuadro de diálogo especifica el estilo **visible de WS. \_** Una aplicación no debe crear un cuadro de diálogo modal con el **estilo WS \_ CHILD.** Un cuadro de diálogo modal con este estilo se deshabilita, lo que impide que cualquier entrada posterior llegue a la aplicación.

Una aplicación crea un cuadro de diálogo modal mediante la [**función DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) o [**DialogBoxIndirect.**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) **DialogBox** requiere el nombre o identificador de un recurso que contiene una plantilla de cuadro de diálogo; **DialogBoxIndirect requiere** un identificador para un objeto de memoria que contiene una plantilla de cuadro de diálogo. Las [**funciones DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) y [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama) también crean cuadros de diálogo modales; son idénticas a las funciones mencionadas anteriormente, pero pasan un parámetro especificado al procedimiento del cuadro de diálogo cuando se crea el cuadro de diálogo.

Al crear el cuadro de diálogo modal, el sistema lo convierte en la ventana activa. El cuadro de diálogo permanece activo hasta que el procedimiento del cuadro de diálogo llama a la [**función EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) o el sistema activa una ventana en otra aplicación. Ni el usuario ni la aplicación pueden activar la ventana de propietario hasta que se destruya el cuadro de diálogo modal.

Cuando la ventana de propietario aún no está deshabilitada, el sistema deshabilita automáticamente la ventana y las ventanas secundarias que le pertenecen cuando crea el cuadro de diálogo modal. La ventana de propietario permanece deshabilitada hasta que se destruye el cuadro de diálogo. Aunque un procedimiento de cuadro de diálogo podría habilitar la ventana de propietario en cualquier momento, la habilitación del propietario no permite el propósito del cuadro de diálogo modal y no se recomienda. Cuando se destruye el procedimiento del cuadro de diálogo, el sistema habilita de nuevo la ventana de propietario, pero solo si el cuadro de diálogo modal ha provocado que el propietario se deshabilite.

Cuando el sistema crea el cuadro de diálogo modal, envía el mensaje [**\_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) de WM a la ventana (si existe) que captura actualmente la entrada del mouse. Una aplicación que recibe este mensaje debe liberar la captura del mouse para que el usuario pueda mover el mouse en el cuadro de diálogo modal. Dado que el sistema deshabilita la ventana del propietario, se pierde toda la entrada del mouse si el propietario no puede liberar el mouse al recibir este mensaje.

Para procesar mensajes para el cuadro de diálogo modal, el sistema inicia su propio bucle de mensajes, tomando el control temporal de la cola de mensajes para toda la aplicación. Cuando el sistema recupera un mensaje que no es explícitamente para el cuadro de diálogo, envía el mensaje a la ventana adecuada. Si recupera un mensaje [**\_ DE SALIDA DE WM,**](/windows/desktop/winmsg/wm-quit) lo vuelve a enviar a la cola de mensajes de la aplicación para que el bucle de mensajes principal de la aplicación pueda finalmente recuperar el mensaje.

El sistema envía el [**mensaje \_ ENTERIDLE**](wm-enteridle.md) de WM a la ventana del propietario cada vez que la cola de mensajes de la aplicación está vacía. La aplicación puede usar este mensaje para llevar a cabo una tarea en segundo plano mientras el cuadro de diálogo permanece en la pantalla. Cuando una aplicación usa el mensaje de esta manera, la aplicación debe producir con frecuencia el control (por ejemplo, mediante la [**función PeekMessage)**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) para que el cuadro de diálogo modal pueda recibir cualquier entrada del usuario. Para evitar que el cuadro de diálogo modal envíe los mensajes **\_ ENTERIDLE** de WM, la aplicación puede especificar el estilo \_ DS NOIDLEMSG al crear el cuadro de diálogo.

Una aplicación destruye un cuadro de diálogo modal mediante la [**función EndDialog.**](/windows/desktop/api/Winuser/nf-winuser-enddialog) En la mayoría de los **casos,** el procedimiento del cuadro de diálogo llama a **EndDialog** cuando el usuario hace clic en Cerrar en el menú de ventana del cuadro de diálogo o hace clic en el botón **Aceptar** o Cancelar del cuadro de diálogo.  El cuadro de diálogo puede devolver un valor a través de la función [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) (u otras funciones de creación) especificando un valor al llamar a **la función EndDialog.** El sistema devuelve este valor después de destruir el cuadro de diálogo. La mayoría de las aplicaciones usan este valor devuelto para determinar si el cuadro de diálogo completó su tarea correctamente o si el usuario lo canceló. El sistema no devuelve el control de la función que crea el cuadro de diálogo hasta que el procedimiento del cuadro de diálogo haya llamado a **la función EndDialog.**

## <a name="modeless-dialog-boxes"></a>Cuadros de diálogo de modeless

Un cuadro de diálogo no modelo debe ser una ventana emergente que tenga un menú de ventana, una barra de título y un borde fino. Es decir, la plantilla de cuadro de diálogo debe especificar los estilos POPUP de **WS, \_** **WS \_ CAPTION,** **WS \_ BORDER** y **WS \_ SYSMENU.** El sistema no muestra automáticamente el cuadro de diálogo a menos que la plantilla especifique el **estilo VISIBLE de WS. \_**

Una aplicación crea un cuadro de diálogo no modelo mediante la [**función CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) o [**CreateDialogIndirect.**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta) **CreateDialog** requiere el nombre o identificador de un recurso que contiene una plantilla de cuadro de diálogo; **CreateDialogIndirect requiere** un identificador para un objeto de memoria que contiene una plantilla de cuadro de diálogo. Otras dos funciones, [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama) y [**CreateDialogIndirectParam,**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)también crean cuadros de diálogo no modelo; pasan un parámetro especificado al procedimiento del cuadro de diálogo cuando se crea el cuadro de diálogo.

[**CreateDialog y**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) otras funciones de creación devuelven un identificador de ventana al cuadro de diálogo. La aplicación y el procedimiento del cuadro de diálogo pueden usar este identificador para administrar el cuadro de diálogo. Por ejemplo, si **WS \_ VISIBLE** no se especifica en la plantilla de cuadro de diálogo, la aplicación puede mostrar el cuadro de diálogo pasando el identificador de ventana a la [**función ShowWindow.**](/windows/desktop/api/winuser/nf-winuser-showwindow)

Un cuadro de diálogo no modelo no deshabilita la ventana de propietario ni le envía mensajes. Al crear el cuadro de diálogo, el sistema la convierte en la ventana activa, pero el usuario o la aplicación pueden cambiar la ventana activa en cualquier momento. Si el cuadro de diálogo se vuelve inactivo, permanece por encima de la ventana del propietario en el orden Z, incluso si la ventana de propietario está activa.

La aplicación es responsable de recuperar y enviar mensajes de entrada al cuadro de diálogo. La mayoría de las aplicaciones usan el bucle de mensajes principal para esto. Para permitir que el usuario se mueva a los controles y selecciónelos mediante el teclado, sin embargo, la aplicación debe llamar a la [**función IsDialogMessage.**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) Para obtener más información sobre esta función, vea [Dialog Box Keyboard Interface](dlgbox-programming-considerations.md).

Un cuadro de diálogo no modal no puede devolver un valor a la aplicación como lo hace un cuadro de diálogo modal, pero el procedimiento del cuadro de diálogo puede enviar información a la ventana de propietario mediante la [**función SendMessage.**](/windows/desktop/api/winuser/nf-winuser-sendmessage)

Una aplicación debe destruir todos los cuadros de diálogo no modelo antes de finalizar. Puede destruir un cuadro de diálogo no modelo mediante la [**función DestroyWindow.**](/windows/desktop/api/winuser/nf-winuser-destroywindow) En la mayoría de los casos, el procedimiento del cuadro de diálogo llama a **DestroyWindow en** respuesta a la entrada del usuario, como al hacer clic **en el botón** Cancelar. Si el usuario nunca cierra el cuadro de diálogo de esta manera, la aplicación debe llamar a **DestroyWindow**.

[**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) invalida el identificador de ventana en el cuadro de diálogo, por lo que las llamadas posteriores a las funciones que usan el identificador devuelven valores de error. Para evitar errores, el procedimiento del cuadro de diálogo debe notificar al propietario que el cuadro de diálogo se ha destruido. Muchas aplicaciones mantienen una variable global que contiene el identificador del cuadro de diálogo. Cuando el procedimiento del cuadro de diálogo destruye el cuadro de diálogo, también establece la variable global en **NULL,** lo que indica que el cuadro de diálogo ya no es válido.

El procedimiento del cuadro de diálogo no debe llamar a [**la función EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) para destruir un cuadro de diálogo no modelo.

## <a name="dialog-box-templates"></a>Plantillas de cuadro de diálogo

Una plantilla de cuadro de diálogo son datos binarios que describen el cuadro de diálogo, que define su alto, ancho, estilo y los controles que contiene. Para crear un cuadro de diálogo, el sistema carga una plantilla de cuadro de diálogo desde los recursos del archivo ejecutable de la aplicación o usa la plantilla que la aplicación le pasa en memoria global. En cualquier caso, la aplicación debe proporcionar una plantilla al crear un cuadro de diálogo.

Un desarrollador crea recursos de plantilla mediante un compilador de recursos o un editor de cuadros de diálogo. Un compilador de recursos convierte una descripción de texto en un recurso binario y un editor de cuadros de diálogo guarda un cuadro de diálogo construido interactivamente como un recurso binario.

> [!Note]  
> Una explicación de cómo crear recursos de plantilla y agregarlos al archivo ejecutable de la aplicación está fuera del ámbito de esta información general. Para obtener más información sobre cómo crear recursos de plantilla y agregarlos a un archivo ejecutable, consulte la documentación proporcionada con las herramientas de desarrollo de aplicaciones.

 

Para crear un cuadro de diálogo sin usar recursos de plantilla, debe crear una plantilla en memoria y pasarla a la función [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama) o [**DialogBoxIndirectParam,**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama) o a la macro [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta) o [**DialogBoxIndirect.**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)

Una plantilla de cuadro de diálogo en memoria consta de un encabezado que describe el cuadro de diálogo, seguido de uno o varios bloques de datos adicionales que describen cada uno de los controles del cuadro de diálogo. La plantilla puede usar el formato estándar o el formato extendido. En una plantilla estándar, el encabezado es una [**estructura DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) seguida de matrices de longitud variable adicionales; y los datos de cada control constan de una [**estructura DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) seguida de matrices de longitud variable adicionales. En una plantilla de cuadro de diálogo extendida, el encabezado usa el formato [**DLGTEMPLATEEX**](dlgtemplateex.md) y las definiciones de control usan el formato [**DLGITEMTEMPLATEEX.**](dlgitemtemplateex.md)

Puede crear una plantilla de memoria si asigna un objeto de memoria global y lo rellena con las definiciones estándar o extendidas de encabezado y control. Una plantilla de memoria es idéntica en forma y contenido a un recurso de plantilla. Muchas aplicaciones que usan plantillas de memoria usan primero la función [**LoadResource**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource) para cargar un recurso de plantilla en la memoria y, a continuación, modifican el recurso cargado para crear una plantilla de memoria. Para obtener más información sobre cómo crear una plantilla de cuadro de diálogo en memoria, vea [Plantillas en memoria.](#templates-in-memory)

En las secciones siguientes se describen los estilos, medidas y otros valores usados en una plantilla de cuadro de diálogo.

-   [Estilos de plantilla de cuadro de diálogo](#dialog-box-template-styles)
-   [Medidas del cuadro de diálogo](#dialog-box-measurements)
-   [Controles de cuadro de diálogo](#dialog-box-controls)
-   [Menú de ventana del cuadro de diálogo](#dialog-box-window-menu)
-   [Fuentes del cuadro de diálogo](#dialog-box-fonts)
-   [Plantillas en memoria](#templates-in-memory)

### <a name="dialog-box-template-styles"></a>Estilos de plantilla de cuadro de diálogo

Cada plantilla de cuadro de diálogo especifica una combinación de valores de estilo que definen la apariencia y las características del cuadro de diálogo. Los valores de estilo pueden ser estilos de ventana, como **WS \_ POPUP** y **\_ SYSMENU de WS,** y estilos de cuadro de diálogo, como **DS \_ MODALFRAME**. El número y el tipo de estilos de una plantilla dependen del tipo y la finalidad del cuadro de diálogo. Para obtener una lista de valores, vea [**Estilos de cuadro de diálogo**](dialog-box-styles.md).

El sistema pasa todos los estilos de ventana especificados en la plantilla a la [**función CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) al crear el cuadro de diálogo. El sistema puede pasar uno o varios estilos extendidos en función de los estilos de cuadro de diálogo especificados. Por ejemplo, cuando la plantilla especifica **\_ DS MODALFRAME**, el sistema usa **WS \_ EX \_ DLGMODALFRAME al** crear el cuadro de diálogo.

La mayoría de los cuadros de diálogo son ventanas emergentes que tienen un menú de ventana y una barra de título. Por lo tanto, la plantilla típica especifica los estilos POPUP de **WS, \_** **\_ SYSMENU** de WS y **WS \_ CAPTION.** La plantilla también especifica un estilo de borde: **WS \_ BORDER** para cuadros de diálogo no modales y **DS \_ MODALFRAME** para cuadros de diálogo modales. Una plantilla puede especificar un tipo de ventana que no sea emergente (como **WS \_ OVERLAPPED)** si crea una ventana personalizada en lugar de un cuadro de diálogo.

El sistema siempre muestra un cuadro de diálogo modal independientemente de si se especifica el estilo VISIBLE de **WS. \_** Cuando la plantilla de un cuadro de diálogo no modelo especifica el estilo visible de **WS, \_** el sistema muestra automáticamente el cuadro de diálogo cuando se crea. De lo contrario, la aplicación es responsable de mostrar el cuadro de diálogo mediante la [**función ShowWindow.**](/windows/desktop/api/winuser/nf-winuser-showwindow)

### <a name="dialog-box-measurements"></a>Medidas del cuadro de diálogo

Cada plantilla de cuadro de diálogo contiene medidas que especifican la posición, el ancho y el alto del cuadro de diálogo y los controles que contiene. Estas medidas son independientes del dispositivo, por lo que una aplicación puede usar una sola plantilla para crear el mismo cuadro de diálogo para todos los tipos de dispositivos para mostrar. Esto garantiza que un cuadro de diálogo tendrá las mismas proporciones y apariencia en todas las pantallas, a pesar de las diferentes resoluciones y relaciones de aspecto entre pantallas.

Las medidas de una plantilla de cuadro de diálogo se especifican en unidades de plantilla de diálogo. Para convertir medidas de unidades de plantilla de diálogo en unidades de pantalla (píxeles), use la función [**MapDialogRect,**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) que tiene en cuenta la fuente utilizada por el cuadro de diálogo y convierte correctamente un rectángulo de unidades de plantilla de diálogo en píxeles. Para los cuadros de diálogo que usan la fuente del sistema, puede usar la función [**GetDialogBaseUnits**](/windows/desktop/api/Winuser/nf-winuser-getdialogbaseunits) para realizar los cálculos de conversión usted mismo, aunque el uso de **MapDialogRect** es más sencillo.

La plantilla debe especificar las coordenadas iniciales de la esquina superior izquierda del cuadro de diálogo. Normalmente, las coordenadas son relativas a la esquina superior izquierda del área de cliente de la ventana de propietario. Cuando la plantilla especifica el estilo ABSALIGN de DS o el cuadro de diálogo no tiene propietario, la posición es relativa a la esquina superior \_ izquierda de la pantalla. El sistema establece esta posición inicial al crear el cuadro de diálogo, pero permite que una aplicación ajuste la posición antes de mostrar el cuadro de diálogo. Por ejemplo, una aplicación puede recuperar las dimensiones de la ventana de propietario, calcular una nueva posición que centra el cuadro de diálogo en la ventana del propietario y, a continuación, establecer la posición mediante la [**función SetWindowPos.**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)

La plantilla debe especificar un ancho y un alto del cuadro de diálogo que no superen el ancho y alto de la pantalla, y garantiza que todos los controles están dentro del área cliente del cuadro de diálogo. Aunque el sistema permite que un cuadro de diálogo sea de cualquier tamaño, la creación de uno que sea demasiado pequeño o demasiado grande puede impedir que el usuario proporcione entradas, lo que impide el propósito del cuadro de diálogo. Muchas aplicaciones usan más de un cuadro de diálogo cuando hay un gran número de controles. En tales casos, el cuadro de diálogo inicial normalmente contiene uno o varios botones que el usuario puede elegir para mostrar el siguiente cuadro de diálogo.

### <a name="dialog-box-controls"></a>Controles de cuadro de diálogo

La plantilla especifica la posición, el ancho, el alto, el estilo, el identificador y la clase de ventana para cada control del cuadro de diálogo. El sistema crea cada control pasando estos datos a la [**función CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Los controles se crean en el orden en que se especifican en la plantilla. La plantilla debe especificar el número, el tipo y el orden adecuados de los controles para asegurarse de que el usuario puede escribir la entrada necesaria para completar la tarea asociada al cuadro de diálogo.

Para cada control, la plantilla especifica valores de estilo que definen la apariencia y el funcionamiento del control. Cada control es una ventana secundaria y, por tanto, debe tener el **estilo CHILD \_ de WS.** Para asegurarse de que el control está visible cuando se muestra el cuadro de diálogo, cada control también debe tener el estilo **VISIBLE de \_ WS.** Otros estilos de ventana usados habitualmente son **WS \_ BORDER** para los controles que tienen bordes opcionales, **WS \_ DISABLED** para los controles que deben deshabilitarse cuando se crea inicialmente el cuadro de diálogo y **WS \_ TABSTOP** y **WS \_ GROUP** para los controles a los que se puede acceder mediante el teclado. Los **estilos \_ TABSTOP y** **WS \_ GROUP** de WS se usan junto con la interfaz de teclado del cuadro de diálogo que se describe más adelante en este tema.

La plantilla también puede especificar estilos de control específicos de la clase de ventana del control. Por ejemplo, una plantilla que especifica un control de botón debe proporcionar un estilo de control de botón como **BS \_ PUSHBUTTON** o **BS \_ CHECKBOX**. El sistema pasa los estilos de control al procedimiento de ventana de control a través del mensaje [**WM \_ CREATE,**](/windows/desktop/winmsg/wm-create) lo que permite que el procedimiento adapte la apariencia y el funcionamiento del control.

El sistema convierte las coordenadas de posición y las medidas de ancho y alto de las unidades base del cuadro de diálogo en píxeles, antes de pasar estas a [**CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Cuando el sistema crea un control, especifica el cuadro de diálogo como la ventana primaria. Esto significa que el sistema siempre interpreta las coordenadas de posición del control como coordenadas de cliente, en relación con la esquina superior izquierda del área de cliente del cuadro de diálogo.

La plantilla especifica la clase de ventana para cada control. Un cuadro de diálogo típico contiene controles que pertenecen a las clases de ventana de control predefinidas, como el botón y las clases de ventana de control de edición. En este caso, la plantilla especifica clases de ventana al proporcionar los valores atom predefinidos correspondientes para las clases. Cuando un cuadro de diálogo contiene un control que pertenece a una clase de ventana de control personalizada, la plantilla proporciona el nombre de esa clase de ventana registrada o el valor atom asociado actualmente al nombre.

Cada control de un cuadro de diálogo debe tener un identificador único para distinguirlo de otros controles. Los controles envían información al procedimiento del cuadro de diálogo a través de mensajes [**\_ WM COMMAND,**](/windows/desktop/menurc/wm-command) por lo que los identificadores de control son esenciales para que el procedimiento determine qué control envió un mensaje especificado. La única excepción a esta regla son los identificadores de control para los controles estáticos. Los controles estáticos no requieren identificadores únicos porque no envían ningún **mensaje \_ WM COMMAND.**

Para permitir que el usuario cierre el cuadro de diálogo, la plantilla debe especificar al menos un botón de inserción y asignarle el identificador de control **IDCANCEL**. Para permitir que el usuario elija entre completar o cancelar la tarea asociada al cuadro de diálogo, la plantilla debe especificar dos botones de inserción, etiquetados como **Aceptar** y **Cancelar,** con identificadores de control de **IDOK** e **IDCANCEL,** respectivamente.

Una plantilla también especifica texto opcional y datos de creación para un control . El texto normalmente proporciona etiquetas para los controles de botón o especifica el contenido inicial de un control de texto estático. Los datos de creación son uno o varios bytes de datos que el sistema pasa al procedimiento de ventana de control al crear el control. Los datos de creación son útiles para los controles que requieren más información sobre su contenido o estilo iniciales de los especificados por otros datos. Por ejemplo, una aplicación puede usar datos de creación para establecer la configuración inicial y el intervalo de un control de barra de desplazamiento.

### <a name="dialog-box-window-menu"></a>Menú de la ventana Cuadro de diálogo

El sistema proporciona a un cuadro de diálogo un menú de ventana cuando la plantilla especifica el **estilo \_ SYSMENU de WS.** Para evitar una entrada inapropiada, el sistema deshabilita automáticamente todos los elementos del menú, excepto **Mover** y **Cerrar.** El usuario puede hacer clic **en Mover** para mover el cuadro de diálogo. Cuando el usuario hace clic en **Cerrar**, el sistema envía un mensaje [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) al procedimiento del cuadro de diálogo con el parámetro *wParam* establecido **en IDCANCEL.** Esto es idéntico al mensaje enviado por el **botón Cancelar** cuando el usuario hace clic en él. La acción recomendada para este mensaje es cerrar el cuadro de diálogo y cancelar la tarea solicitada.

Aunque no se recomiendan otros menús en los cuadros de diálogo, una plantilla de cuadro de diálogo puede especificar un menú si se proporciona el identificador o el nombre de un recurso de menú. En este caso, el sistema carga el recurso y crea el menú para el cuadro de diálogo. Las aplicaciones suelen usar identificadores de menú o nombres en plantillas cuando se usan las plantillas para crear ventanas personalizadas en lugar de cuadros de diálogo.

### <a name="dialog-box-fonts"></a>Fuentes de cuadro de diálogo

El sistema usa el ancho medio de caracteres de la fuente del cuadro de diálogo para calcular la posición y las dimensiones del cuadro de diálogo. De forma predeterminada, el sistema dibuja todo el texto de un cuadro de diálogo con la **fuente \_ SYSTEM FONT.**

Para especificar una fuente para un cuadro de diálogo distinto del predeterminado, debe crear el cuadro de diálogo mediante una plantilla de cuadro de diálogo. En un recurso de plantilla, use la [instrucción FONT](../menurc/font-statement.md). En una plantilla de cuadro de diálogo, establezca el estilo **DS \_ SETFONT** o **DS \_ SHELLFONT** y especifique un tamaño de punto y un nombre de tipo de letra. Incluso si una plantilla de cuadro de diálogo especifica una fuente de esta manera, el sistema siempre usa la fuente del sistema para los menús de título y cuadro de diálogo del cuadro de diálogo.

Cuando el cuadro de diálogo tiene el estilo **DS \_ SETFONT** o **DS \_ SHELLFONT,** el sistema envía un mensaje [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) al procedimiento del cuadro de diálogo y a cada control a medida que crea el control. El procedimiento del cuadro de diálogo es responsable de guardar el identificador de fuente pasado con el mensaje **\_ SETFONT** de WM y seleccionar el identificador en el contexto del dispositivo para mostrar cada vez que escribe texto en la ventana. Los controles predefinidos lo hacen de forma predeterminada.

La fuente del sistema puede variar entre diferentes versiones de Windows. Para que la aplicación use la fuente del sistema independientemente del sistema en el que se ejecute, use **DS \_ SHELLFONT** con el tipo de letra MS Shell Dlg y use el recurso [DIALOGEX](../menurc/dialogex-resource.md) en lugar del recurso [DIALOG](../menurc/dialog-resource.md). El sistema asigna este tipo de letra de forma que el cuadro de diálogo usará la fuente Denoma. Tenga en **cuenta que DS \_ SHELLFONT** no tiene ningún efecto si el tipo de letra no es dlg de shell de MS.

### <a name="templates-in-memory"></a>Plantillas en memoria

Una plantilla de cuadro de diálogo en memoria consta de un encabezado que describe el cuadro de diálogo, seguido de uno o varios bloques de datos adicionales que describen cada uno de los controles del cuadro de diálogo. La plantilla puede usar el formato estándar o el formato extendido. En una plantilla estándar, el encabezado es una [**estructura DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) seguida de matrices de longitud variable adicionales. Los datos de cada control constan de una [**estructura DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) seguida de matrices de longitud variable adicionales. En una plantilla de cuadro de diálogo extendido, el encabezado usa el formato [**DLGTEMPLATEEX**](dlgtemplateex.md) y las definiciones de control usan el formato [**DLGITEMTEMPLATEEX.**](dlgitemtemplateex.md)

Para distinguir entre una plantilla estándar y una plantilla extendida, compruebe los primeros 16 bits de una plantilla de cuadro de diálogo. En una plantilla extendida, la primera **palabra se** 0xFFFF; cualquier otro valor indica una plantilla estándar.

Si crea una plantilla de diálogo en memoria, debe asegurarse de que cada una de las definiciones de control [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) o [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) se alinea en los límites **DWORD.** Además, los datos de creación que siguen a una definición de control deben alinearse en un **límite DWORD.** Todas las demás matrices de longitud variable de una plantilla de cuadro de diálogo deben alinearse en los **límites de WORD.**

### <a name="template-header"></a>Encabezado de plantilla

En las plantillas estándar y extendidas para los cuadros de diálogo, el encabezado incluye la siguiente información general:

-   Ubicación y dimensiones del cuadro de diálogo
-   Estilos de ventana y cuadro de diálogo para el cuadro de diálogo
-   Número de controles del cuadro de diálogo. Este valor determina el número de definiciones de control [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) o [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) en la plantilla.
-   Recurso de menú opcional para el cuadro de diálogo. La plantilla puede indicar que el cuadro de diálogo no tiene un menú o puede especificar un valor ordinal o una cadena Unicode terminada en NULL que identifica un recurso de menú en un archivo ejecutable.
-   Clase de ventana del cuadro de diálogo. Puede ser la clase de cuadro de diálogo predefinida o un valor ordinal o una cadena Unicode terminada en NULL que identifica una clase de ventana registrada.
-   Cadena Unicode terminada en NULL que especifica el título de la ventana del cuadro de diálogo. Si la cadena está vacía, la barra de título del cuadro de diálogo está en blanco. Si el cuadro de diálogo no tiene el estilo **WS \_ CAPTION,** el sistema establece el título en la cadena especificada, pero no lo muestra.
-   Si el cuadro de diálogo tiene el estilo **\_ DS SETFONT,** el encabezado especifica el tamaño de punto y el nombre del tipo de letra de la fuente que se usará para el texto del área de cliente y los controles del cuadro de diálogo.

En una plantilla extendida, el [**encabezado DLGTEMPLATEEX**](dlgtemplateex.md) también especifica la siguiente información adicional:

-   Identificador de contexto de ayuda de la ventana del cuadro de diálogo cuando el sistema envía un [**mensaje WM \_ HELP.**](../shell/wm-help.md)
-   Si el cuadro de diálogo tiene el estilo **DS \_ SETFONT** o **DS \_ SHELLFONT,** el encabezado especifica el grosor de la fuente e indica si la fuente está en cursiva.

### <a name="control-definitions"></a>Definiciones de controles

Después del encabezado de plantilla hay una o varias definiciones de control que describen los controles del cuadro de diálogo. En las plantillas estándar y extendidas, el encabezado del cuadro de diálogo tiene un miembro que indica el número de definiciones de control en la plantilla. En una plantilla estándar, cada definición de control consta de una estructura [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) seguida de matrices de longitud variable adicionales. En una plantilla extendida, las definiciones de control usan el [**formato DLGITEMTEMPLATEEX.**](dlgitemtemplateex.md)

En las plantillas estándar y extendida, la definición del control incluye la siguiente información:

-   Ubicación y dimensiones del control.
-   Estilos de ventana y control para el control.
-   Identificador de control.
-   Clase de ventana del control. Puede ser el valor ordinal de una clase del sistema predefinida o una cadena Unicode terminada en NULL que especifica el nombre de una clase de ventana registrada.
-   Cadena Unicode terminada en NULL que especifica el texto inicial del control o un valor ordinal que identifica un recurso, como un icono, en un archivo ejecutable.
-   Un bloque opcional de longitud variable de datos de creación. Cuando el sistema crea el control, pasa un puntero a estos datos en el parámetro *lParam* del [**mensaje CREATE \_ de WM**](/windows/desktop/winmsg/wm-create) que envía al control.

En una plantilla extendida, la definición del control también especifica un identificador de contexto de ayuda para el control cuando el sistema envía un [**mensaje DE AYUDA \_ DE WM.**](../shell/wm-help.md)

 

 