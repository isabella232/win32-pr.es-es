---
description: Describe la nueva funcionalidad de la barra de tareas, incluida la consolidación del inicio y el cambio, las capacidades mejoradas de los botones de la barra de tareas, como el acceso con un solo clic a documentos y tareas específicas de la aplicación, controles de transporte y notificaciones de estado, representaciones en miniaturas y destinos de conmutador basados en pestañas individuales en una aplicación con pestañas y la capacidad de
ms.assetid: cbf2b07d-d67c-4755-888c-d40692d13cae
title: Extensiones de la barra de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df308d8045301b98937eb03af595d2e800921b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912361"
---
# <a name="taskbar-extensions"></a>Extensiones de la barra de tareas

A partir de Windows 7, la barra de tareas se ha ampliado significativamente en el principio de la aplicación de los usuarios, donde funcionan de la forma más rápida y eficaz posible. Para ello, las ventanas de la aplicación, los archivos y los comandos que el usuario necesita para lograr, ahora están centralizados en un único botón de la barra de tareas que consolida orígenes y controles de información diseminados previamente. Ahora un usuario puede buscar tareas comunes, archivos recientes y frecuentes, alertas, notificaciones de progreso y miniaturas de documentos individuales o pestañas en un solo lugar.

-   [Inicio y conmutación unificados](#unified-launching-and-switching)
-   [Jump Lists](#jump-lists)
-   [Destinations](#destinations)
-   [Tareas](#tasks)
-   [Personalización de listas de accesos directos](#customizing-jump-lists)
-   [Barras de herramientas en miniatura](#thumbnail-toolbars)
-   [Superposiciones de iconos](#icon-overlays)
-   [Barras de progreso](#progress-bars)
-   [Deskbands](#deskbands)
-   [Área de notificación](#notification-area)
-   [Vistas en miniatura](#thumbnails)
-   [Temas relacionados](#related-topics)

## <a name="unified-launching-and-switching"></a>Inicio y conmutación unificados

En la barra de tareas de Windows 7, el inicio rápido ya no es una barra de herramientas independiente. Los accesos directos del iniciador que normalmente contiene el inicio rápido se anclan ahora a la barra de tareas, mezclados con los botones de las aplicaciones que se están ejecutando actualmente. Cuando un usuario inicia una aplicación desde un acceso directo anclado del iniciador, el icono se transforma en el botón de la barra de tareas de la aplicación mientras la aplicación se está ejecutando. Cuando el usuario cierra la aplicación, el botón vuelve al icono. Sin embargo, tanto el acceso directo del iniciador como el botón de la aplicación en ejecución son solo formas diferentes del botón de la barra de tareas de Windows 7.

![barra de tareas de Windows 7](images/taskbar/taskbar.png)

Un pequeño conjunto de aplicaciones se ancla de forma predeterminada para las nuevas instalaciones. Aparte de estas, solo el usuario puede anclar más aplicaciones; no se permite el anclaje mediante programación por una aplicación.

La característica Mostrar escritorio del inicio rápido ahora se encuentra en el extremo derecho de la barra de tareas. Al mantener el mouse sobre esta área, todas las ventanas activas se vuelven transparentes, lo que muestra el escritorio. Al hacer clic en el área, se ejecuta la acción conocida de minimizar todas las ventanas y cambiar al escritorio.

Mientras se ejecuta la aplicación, el botón de la barra de tareas se convierte en el único lugar para tener acceso a todas las características siguientes, cada una de las cuales se describe en detalle a continuación.

-   [Tareas](#tasks): comandos de aplicación comunes, presentes incluso cuando la aplicación no se está ejecutando.
-   [Destinos](#destinations): archivos a los que se ha tenido acceso recientemente y con frecuencia específicos de la aplicación.
-   [Vistas en miniatura](#thumbnails): cambio de ventana, incluidos los destinos del conmutador para fichas y documentos individuales.
-   [Barras de herramientas en miniatura](#thumbnail-toolbars): control de aplicación básico de la miniatura.
-   [Barras de progreso](#progress-bars) e [superposiciones de iconos](#icon-overlays): notificaciones de estado.

El botón de la barra de tareas puede representar un iniciador, una sola ventana de la aplicación o un grupo. Un identificador conocido como identificador de modelo de usuario de la aplicación (AppUserModelID) se asigna a cada grupo. Se puede especificar un AppUserModelID para invalidar la agrupación de la barra de tareas estándar, lo que permite que Windows se convierta en miembros del mismo grupo cuando es posible que no se vean como tal. Cada miembro de un grupo recibe una vista previa independiente en el control flotante de miniaturas que se muestra cuando se mantiene el mouse sobre el botón de la barra de tareas del grupo. Tenga en cuenta que la agrupación se mantiene opcional.

A partir de Windows 7, ahora el usuario puede reorganizar los botones de la barra de tareas mediante operaciones de arrastrar y colocar.

> [!Note]  
> La carpeta de inicio rápido ([* * * * \_ FOLDERID](knownfolderid.md)de inicio rápido * * *) sigue estando disponible para mantener la compatibilidad con versiones anteriores, aunque ya no se trata de una interfaz de usuario de inicio rápido. Sin embargo, las nuevas aplicaciones no deben preguntar para agregar un icono al inicio rápido durante la instalación.

 

Para obtener más información, vea [identificadores de modelo de usuario de la aplicación (AppUserModelIDs)](appids.md).

## <a name="jump-lists"></a>Jump Lists

Normalmente, un usuario inicia un programa con la intención de tener acceso a un documento o realizar tareas dentro del programa. Es posible que el usuario de un programa de juego desee acceder a un juego o un lanzamiento guardado como un carácter específico en lugar de reiniciar un juego desde el principio. Para que los usuarios tengan más eficiencia en su objetivo final, se adjunta una lista de [destinos](#destinations) y [tareas](#tasks) comunes asociadas a una aplicación al botón de la barra de tareas de la aplicación (así como a la entrada del menú de **Inicio** equivalente). Esta es la Jump List de la aplicación. La Jump List está disponible si el botón de la barra de tareas está en un estado del iniciador (la aplicación no se está ejecutando) o si representa una o más ventanas. Al hacer clic con el botón secundario en el botón de la barra de tareas, se muestra la Jump List de la aplicación, tal como se muestra en la siguiente ilustración.

![Jump List con categorías ancladas, frecuentes y de tareas](images/taskbar/jumplist.png)

De forma predeterminada, una lista de saltos estándar contiene dos categorías: elementos recientes y elementos anclados, aunque solo se muestran en la interfaz de usuario las categorías con contenido, ninguna de estas categorías se muestra en el primer inicio. Siempre hay un icono de inicio de aplicación (para iniciar más instancias de la aplicación), una opción para anclar o desanclar la aplicación de la barra de tareas y un comando de **cierre** para cualquier ventana abierta.

## <a name="destinations"></a>Destinations

Se considera que las categorías **recientes** y **frecuentes** contienen destinos. Un destino, normalmente un archivo, un documento o una dirección URL, es algo que se puede editar, examinar, ver, etc. Piense en un destino como algo en lugar de una acción. Normalmente, un destino es un elemento del espacio de nombres del shell, representado por un [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) o [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka). Estas partes de la lista de destino son análogas a la lista de documentos usados recientemente del menú **Inicio** (ya no se muestra de forma predeterminada) y a la lista de aplicaciones usadas con frecuencia, pero son específicas de una aplicación y, por lo tanto, son más precisas y útiles para el usuario. Los resultados utilizados en la lista de destino se calculan mediante llamadas a [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). Tenga en cuenta que cuando el usuario abre un archivo desde el explorador de Windows o usa el cuadro de diálogo de archivo común para abrir, guardar o crear un archivo, se le llama automáticamente a **SHAddToRecentDocs** , lo que hace que muchas aplicaciones obtengan los elementos recientes que aparecen en la lista de destino sin ninguna acción por su parte.

Iniciar un destino es muy similar a iniciar un elemento mediante el comando **abrir con** . La aplicación se inicia con ese destino cargado y listo para usar. Los elementos de la lista de destino también se pueden arrastrar de la lista a un destino de colocación, como un mensaje de correo electrónico. Al tener estos elementos centralizados en una lista de destino, se obtienen los usuarios en los que desean ir mucho más rápido, que es el objetivo.

A medida que los elementos aparecen en la categoría **reciente** de la lista de destino (o en la categoría **frecuente** o en una [categoría personalizada](#customizing-jump-lists) , como se describe en una sección posterior), es posible que un usuario desee asegurarse de que el elemento está siempre en la lista para un acceso rápido. Para ello, puede anclar ese elemento a la lista, lo que agrega el elemento a la categoría **anclada** . Cuando un usuario trabaja activamente con un destino, desea que esté disponible de forma fácil y, por lo tanto, lo anclaría a la lista de destino de la aplicación. Una vez que el trabajo del usuario haya terminado, simplemente desancla el elemento. Este control de usuario mantiene la lista despejada y relevante.

Una lista de destino se puede considerar como una versión específica de la aplicación del menú **Inicio** . Una lista de destino no es un menú contextual. Se puede hacer clic con el botón derecho en cada elemento de una lista de destino para su propio menú contextual.

### <a name="apis"></a>API existentes

-   [**IApplicationDestinations::RemoveDestination**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removedestination)
-   [**IApplicationDestinations::RemoveAllDestinations**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removealldestinations)
-   [**IApplicationDocumentLists:: GetList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist)
-   [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)

## <a name="tasks"></a>Tareas

Otra parte integrada de una Jump List es la categoría de **tareas** . Mientras que un destino es un elemento, una tarea es una acción y, en este caso, es una acción específica de la aplicación. Otra forma, un destino es un sustantivo y una tarea es un verbo. Normalmente, las tareas son elementos [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) con argumentos de la línea de comandos que indican una funcionalidad determinada que puede ser desencadenada por una aplicación. Una vez más, la idea es centralizar toda la información relacionada con una aplicación, como es práctico.

Las aplicaciones definen tareas basadas en las características del programa y en las principales cosas que se espera que realice un usuario con ellas. Las tareas deben ser sin contexto, en el sentido de que no es necesario que la aplicación se ejecute para que funcionen. También deben ser las acciones más comunes estadísticamente que un usuario normal llevaría a cabo en una aplicación, como redactar un mensaje de correo electrónico o abrir el calendario en un programa de correo, crear un nuevo documento en un procesador de textos, iniciar una aplicación en un determinado modo o iniciar uno de sus subcomandos. Una aplicación no debe abarrotar el menú con características avanzadas que los usuarios estándar no necesitarán ni acciones de un solo uso, como el registro. No use tareas para elementos promocionales como actualizaciones o ofertas especiales.

Se recomienda encarecidamente que la lista de tareas sea estática. Debe permanecer igual independientemente del estado o el estado de la aplicación. Aunque es posible modificar la lista de forma dinámica, debe tener en cuenta que esto podría confundir al usuario que no espera que la parte de la lista de destino cambie.

### <a name="apis"></a>API existentes

-   [**ICustomDestinationList::AddUserTasks**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-addusertasks)

## <a name="customizing-jump-lists"></a>Personalización de listas de accesos directos

Una aplicación puede definir sus propias categorías y agregarlas además o en lugar de las categorías estándar **recientes** y **frecuentes** en una Jump List. La aplicación puede controlar sus propios destinos en esas categorías personalizadas en función de la arquitectura de la aplicación y el uso previsto. En la captura de pantalla siguiente se muestra una lista de saltos personalizada con una categoría de historial.

![Jump List personalizada](images/taskbar/customjumplist.png)

Si una aplicación decide proporcionar una categoría personalizada, la aplicación asume la responsabilidad de rellenarla. El contenido de la categoría debe seguir siendo específico del usuario y según el historial del usuario, las acciones o ambos, pero a través de una categoría personalizada, una aplicación puede determinar de qué desea realizar un seguimiento y qué desea omitir, quizás en función de una opción de aplicación. Por ejemplo, un programa de audio podría optar por incluir solo los álbumes recién reproducidos y omitir las pistas individuales reproducidas recientemente.

Si un usuario ha quitado un elemento de la lista, que siempre es una opción de usuario, la aplicación debe respetar eso. La aplicación también debe asegurarse de que los elementos de la lista sean válidos o que no se hayan eliminado correctamente. Los elementos individuales o todo el contenido de la lista se pueden quitar mediante programación.

El sistema determina el número máximo de elementos de una lista de destino en función de diversos factores, como la resolución de pantalla y el tamaño de fuente. Si no hay espacio suficiente para todos los elementos de todas las categorías, se truncan de arriba abajo.

### <a name="apis"></a>API existentes

-   [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)
-   [**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)
-   [**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)

## <a name="thumbnail-toolbars"></a>Barras de herramientas en miniatura

Para proporcionar acceso a los comandos de clave de una ventana determinada sin hacer que el usuario restaure o Active la ventana de la aplicación, se puede incrustar un control de barra de herramientas activo en la vista previa en miniatura de la ventana. Por ejemplo, Windows Media Player podría ofrecer controles de transporte multimedia estándar, como reproducir, pausar, silenciar y detener. La interfaz de usuario muestra esta barra de herramientas directamente debajo de la miniatura, tal como se muestra en la siguiente ilustración, no cubre ninguna parte de ella.

![barra de tareas en miniatura para el reproductor de Windows Media, con tres botones: atrás, reproducir y reenviar](images/taskbar/thumbbar.png)

Esta barra de herramientas es simplemente el conocido control común de barra de herramientas estándar. Tiene siete botones como máximo. El identificador, la imagen, la información sobre herramientas y el estado de cada botón se definen en una estructura, que se pasa a la barra de tareas. La aplicación puede mostrar, habilitar, deshabilitar u ocultar los botones de la barra de herramientas en miniatura según sea necesario en su estado actual.

Dado que hay espacio limitado para Mostrar miniaturas y un número variable de miniaturas que se van a mostrar, las aplicaciones no tienen garantizado un tamaño de barra de herramientas determinado. Si el espacio está restringido, los botones de la barra de herramientas se truncan de derecha a izquierda. Por lo tanto, al diseñar la barra de herramientas, debe dar prioridad a los comandos asociados a los botones y asegurarse de que los más importantes aparecen primero y que es menos probable que se quiten debido a problemas de espacio.

> [!Note]  
> Cuando una aplicación muestra una ventana, el sistema crea el botón de la barra de tareas. Cuando el botón está en su lugar, la barra de tareas envía un mensaje **TaskbarButtonCreated** a la ventana. Su valor se calcula mediante una llamada a [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)(L ("TaskbarButtonCreated")). La aplicación debe recibir ese mensaje antes de llamar a cualquier método [**ITaskbarList3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3) .

 

### <a name="api"></a>API

-   [**ITaskbarList3:: ThumbBarAddButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [**ITaskbarList3:: ThumbBarSetImageList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   [**ITaskbarList3:: ThumbBarUpdateButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarupdatebuttons)
-   [**THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton)

## <a name="icon-overlays"></a>Superposiciones de iconos

Una aplicación puede comunicar ciertas notificaciones y el estado al usuario a través de su botón de la barra de tareas mediante la visualización de pequeñas superposiciones en el botón. Estas superposiciones son similares al tipo de superposición existente que se usa para los accesos directos o las notificaciones de seguridad, que se muestran en la esquina inferior derecha del botón. Para mostrar un icono de superposición, la barra de tareas debe estar en el modo de iconos grandes predeterminado, tal como se muestra en la siguiente captura de pantalla.

![botón de la barra de tareas de Windows Messenger con una superposición para indicar un estado disponible](images/taskbar/taskbaroverlay.png)

Las superposiciones de los iconos sirven como una notificación contextual de estado y están destinadas a negar la necesidad de un icono de estado de área de notificación independiente para comunicar esa información al usuario. Por ejemplo, el nuevo estado de correo de Microsoft Outlook, que se muestra actualmente en el área de notificación, ahora se puede indicar mediante una superposición en el botón de la barra de tareas. De nuevo, debe decidir durante el ciclo de desarrollo cuál es el mejor método para su aplicación. Los iconos superpuestos están diseñados para proporcionar un estado importante, de larga duración o notificaciones como el estado de la red, el estado de Messenger o el correo nuevo. No se debe presentar al usuario una superposición o animación que cambie constantemente.

Dado que una sola superposición está superpuesta en el botón de la barra de tareas y no en las miniaturas de cada ventana, se trata de una característica por grupo en lugar de por ventana. Las solicitudes de iconos de superposición se pueden recibir desde ventanas individuales en un grupo de la barra de tareas, pero no se ponen en cola. La última superposición recibida es la superposición mostrada.

### <a name="apis"></a>API existentes

-   [**ITaskbarList3:: SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon)

## <a name="progress-bars"></a>Barras de progreso

Un botón de la barra de tareas se puede usar para mostrar una barra de progreso. Esto permite que una ventana proporcione información de progreso al usuario sin que ese usuario tenga que cambiar a la ventana. El usuario puede seguir siendo productivo en otra aplicación y ver de un vistazo el progreso de una o varias operaciones que se producen en otras ventanas. Está previsto que una barra de progreso de un botón de la barra de tareas refleje un indicador de progreso más detallado en la propia ventana. Esta característica se puede usar para realizar un seguimiento de las copias de archivos, las descargas, las instalaciones, la grabación de contenido multimedia o cualquier operación que vaya a tardar un período de tiempo. Esta característica no está pensada para su uso con acciones de periféricos, como la carga de una página web o la impresión de un documento. Ese tipo de progreso debe seguir apareciendo en la barra de estado de una ventana.

La barra de progreso del botón de la barra de tareas es una experiencia similar al control de barra de progreso conocido. Puede mostrar el progreso de determinación en función de un porcentaje completado de la operación o un progreso de estilo de marquesina indeterminado para indicar que la operación está en curso sin ninguna predicción de tiempo restante. También puede mostrar que la operación está en pausa o ha detectado un error y requiere la intervención del usuario.

### <a name="apis"></a>API existentes

-   [**ITaskbarList3:: SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate)
-   [**ITaskbarList3:: SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue)

## <a name="deskbands"></a>Deskbands

En las versiones de Windows anteriores a Windows 7, algo similar a la funcionalidad de la barra de herramientas en miniatura se podía lograr a través de un deskband: una barra de herramientas hospedada en la barra de tareas. Por ejemplo, Windows Media Player podría minimizar en la barra de tareas como un conjunto de controles de transporte en lugar de un botón estándar. En Windows 7, deskbands todavía se puede implementar y las barras de herramientas de miniaturas no están diseñadas para reemplazarlas todas. No todas las aplicaciones se prestarán a una barra de herramientas en miniatura y otra solución, como un deskband o una tarea de una lista de destino, podría ser la respuesta correcta para su aplicación. debe decidir qué solución funciona mejor para su aplicación como parte del ciclo de desarrollo. Sin embargo, tenga en cuenta que deskbands debe admitir Windows Aero con translucidez ("Glass") habilitado y la interfaz [**IDeskBand2**](/windows/desktop/api/Shobjidl/nn-shobjidl-ideskband2) .

### <a name="apis"></a>API existentes

-   [**IDeskBand2**](/windows/desktop/api/Shobjidl/nn-shobjidl-ideskband2)

## <a name="notification-area"></a>Área de notificación

Se han realizado cambios en el área de notificación que proporcionan a los usuarios un mayor control sobre los iconos que aparecen en la barra de tareas. Todos los iconos de notificación ahora están ocultos de forma predeterminada y no se puede controlar mediante programación. Solo el usuario puede elegir los iconos de notificación que aparecen en la barra de tareas. Cuando se muestra un globo de notificación, el icono se vuelve temporalmente visible, pero incluso un usuario puede elegir silenciarlos. Por lo tanto, una superposición de iconos en un botón de la barra de tareas se convierte en una opción atractiva cuando se desea que la aplicación comunique esa información a los usuarios.

## <a name="thumbnails"></a>Miniaturas

En Windows Vista, al mantener el mouse sobre el botón de la barra de tareas de una aplicación se muestra una miniatura que representa la ventana en ejecución. Si la barra de tareas ha contraído las ventanas de la aplicación, la miniatura representa este aspecto como una pila, pero solo se muestra la ventana activa en la miniatura.

En Windows 7, cada miembro de un grupo se muestra como una miniatura independiente y ahora es también un destino de conmutador. Una aplicación puede definir sus elementos secundarios (por ejemplo, las ventanas secundarias verdaderas, documentos individuales o pestañas) y proporcionar miniaturas correspondientes para cada una de esas ventanas, incluso cuando no aparecen normalmente en la barra de tareas. Esto permite a los usuarios cambiar directamente a la vista de la aplicación que deseen, en lugar de cambiar a la aplicación y, a continuación, cambiar a su destino. Por ejemplo, las aplicaciones de la interfaz de múltiples documentos (MDI)/tabbed-Document (TDI) pueden mostrar cada documento o pestaña como una miniatura independiente y un destino de modificador cuando se mantiene el mouse sobre el botón de la barra de tareas de un grupo.

![tres miniaturas de la barra de tareas que representan pestañas individuales en Windows Internet Explorer](images/taskbar/taskbarthumbnails.png)

> [!Note]  
> Como en Windows Vista, Aero debe estar activo para ver las miniaturas.

 

### <a name="api"></a>API

-   [**ITaskbarList3:: RegisterTab**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-registertab)
-   [**ITaskbarList3:: SetTabActive**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settabactive)
-   [**ITaskbarList3:: SetTabOrder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settaborder)
-   [**ITaskbarList3:: UnregisterTab**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-unregistertab)
-   [**ITaskbarList4::SetTabProperties**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist4-settabproperties)

Las representaciones en miniatura de Windows suelen ser automáticas, pero en los casos en los que el resultado no es óptimo, se puede especificar explícitamente la miniatura. De forma predeterminada, solo las ventanas de nivel superior tienen una miniatura generada automáticamente y las miniaturas de las ventanas secundarias aparecen como una representación genérica. Esto puede dar lugar a una experiencia menos idónea (e incluso confusa) para el usuario final. Una miniatura de destino de conmutador específica para cada ventana secundaria, por ejemplo, proporciona una experiencia de usuario mucho mejor.

### <a name="api"></a>API

-   [**DwmSetWindowAttribute**](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)
-   [**DwmSetIconicThumbnail**](/windows/win32/api/dwmapi/nf-dwmapi-dwmseticonicthumbnail)
-   [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap)
-   [**DwmInvalidateIconicBitmaps**](/windows/win32/api/dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
-   [**DWMSENDICONICTHUMBNAIL de WM \_**](../dwm/wm-dwmsendiconicthumbnail.md)
-   [**DWMSENDICONICLIVEPREVIEWBITMAP de WM \_**](../dwm/wm-dwmsendiconiclivepreviewbitmap.md)

Puede seleccionar un área concreta de la ventana para usarla como miniatura. Esto puede ser útil cuando una aplicación sabe que sus documentos o pestañas aparecerán similares al verlos en tamaño de miniatura. A continuación, la aplicación puede optar por mostrar solo la parte de su área de cliente que el usuario puede usar para distinguir entre las miniaturas. Sin embargo, al mantener el mouse sobre cualquier miniatura, se muestra una vista de la ventana completa que se encuentra detrás de él, por lo que el usuario puede hacer rápidamente un vistazo.

Si hay más miniaturas de las que se pueden mostrar, la vista previa se revierte a la miniatura heredada o a un icono estándar.

### <a name="api"></a>API

-   [**ITaskbarList3:: SetThumbnailClip**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setthumbnailclip)

Para agregar el **PIN a la barra de tareas** al menú contextual de un elemento, que normalmente solo es necesario para los tipos de archivo que incluyen la entrada [IsShortCut](./links.md) , se realiza registrando el controlador de menú contextual adecuado. Esto también se aplica a **anclar al menú Inicio**. Consulte [registrar controladores de extensión de Shell](reg-shell-exts.md) para obtener más información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[La barra de tareas](taskbar.md)
</dt> <dt>

[Identificadores de modelo de usuario de la aplicación (AppUserModelIDs)](appids.md)
</dt> <dt>

[Notificaciones y el área de notificación](notification-area.md)
</dt> </dl>

 

 
