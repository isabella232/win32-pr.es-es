---
description: Describe la nueva funcionalidad de la barra de tareas, incluida la consolidación del inicio y el cambio, las funcionalidades mejoradas de los botones de la barra de tareas, como el acceso con un solo clic a documentos y tareas específicas de la aplicación, controles de transporte y notificaciones de estado, representaciones en miniatura y destinos de conmutador basados en pestañas individuales en una aplicación con pestañas, y la capacidad de reordenar los botones de la barra de tareas mediante una operación de arrastrar y colocar.
ms.assetid: cbf2b07d-d67c-4755-888c-d40692d13cae
title: Extensiones de la barra de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92cb8f100da2c7b5173319c25369a0ada7284b2ff5f4adbfe9b519c0ee96485
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773755"
---
# <a name="taskbar-extensions"></a>Extensiones de la barra de tareas

A partir Windows 7, la barra de tareas se ha ampliado significativamente bajo el principio rector de conseguir que los usuarios a los que van de la forma más rápida y eficaz posible. Con ese fin, las ventanas, los archivos y los comandos de la aplicación que el usuario necesita lograr ahora están centralizados en un único botón de la barra de tareas que consolida los controles y orígenes de información previamente dispersos. Un usuario ahora puede encontrar tareas comunes, archivos recientes y frecuentes, alertas, notificaciones de progreso y miniaturas de documentos o pestañas individuales en un solo lugar.

-   [Inicio y cambio unificados](#unified-launching-and-switching)
-   [Listas de saltos](#jump-lists)
-   [Destinations](#destinations)
-   [Tareas](#tasks)
-   [Personalización de listas de accesos jump](#customizing-jump-lists)
-   [Barras de herramientas de miniaturas](#thumbnail-toolbars)
-   [Superposiciones de iconos](#icon-overlays)
-   [Barras de progreso](#progress-bars)
-   [Deskbands](#deskbands)
-   [Área de notificación](#notification-area)
-   [Vistas en miniatura](#thumbnails)
-   [Temas relacionados](#related-topics)

## <a name="unified-launching-and-switching"></a>Inicio y cambio unificados

A partir de Windows barra de tareas 7, inicio rápido ya no es una barra de herramientas independiente. Los accesos directos del iniciador inicio rápido normalmente se anclan a la propia barra de tareas, con botones para las aplicaciones en ejecución actualmente. Cuando un usuario inicia una aplicación desde un acceso directo de iniciador anclado, el icono se transforma en el botón de la barra de tareas de la aplicación mientras se ejecuta la aplicación. Cuando el usuario cierra la aplicación, el botón vuelve al icono. Sin embargo, tanto el método abreviado del iniciador como el botón de la aplicación en ejecución son solo formas diferentes del Windows de la barra de tareas 7.

![Barra de tareas de Windows 7](images/taskbar/taskbar.png)

Un pequeño conjunto de aplicaciones se ancla de forma predeterminada para las nuevas instalaciones. Aparte de estas, solo el usuario puede anclar más aplicaciones; No se permite la anclación mediante programación por parte de una aplicación.

La característica Mostrar escritorio de inicio rápido se encuentra ahora en el extremo derecho de la barra de tareas. Al mantener el puntero sobre esta área, todas las ventanas activas se vuelven transparentes y se muestra el escritorio. Al hacer clic en el área, se ejecuta la acción familiar de minimizar todas las ventanas y cambiar al escritorio.

Mientras se ejecuta la aplicación, el botón de la barra de tareas se convierte en el único lugar para acceder a todas las características siguientes, cada una de las que se debata con detalle a continuación.

-   [Tareas:](#tasks)comandos de aplicación comunes, presentes incluso cuando la aplicación no se está ejecutando.
-   [Destinos:](#destinations)archivos a los que se ha accedido con frecuencia y recientemente específicos de la aplicación.
-   [Miniaturas:](#thumbnails)cambio de ventana, incluidos los destinos de conmutador para pestañas y documentos individuales.
-   [Barras de herramientas en miniatura:](#thumbnail-toolbars)control de aplicación básico de la propia miniatura.
-   [Barras de progreso](#progress-bars) e [superposiciones de icono:](#icon-overlays)notificaciones de estado.

El botón de la barra de tareas puede representar un iniciador, una sola ventana de aplicación o un grupo. Un identificador conocido como id. de modelo de usuario de aplicación (AppUserModelID) se asigna a cada grupo. Se puede especificar Un AppUserModelID para invalidar la agrupación de la barra de tareas estándar, lo que permite que las ventanas se conviertan en miembros del mismo grupo cuando, de lo contrario, no se puedan ver como tales. A cada miembro de un grupo se le da una vista previa independiente en el control desplegable de miniaturas que se muestra cuando el mouse mantiene el mouse sobre el botón de la barra de tareas del grupo. Tenga en cuenta que la agrupación sigue siendo opcional.

A partir Windows 7, el usuario puede reorganizar los botones de la barra de tareas mediante operaciones de arrastrar y colocar.

> [!Note]  
> La inicio rápido carpeta ([*\FOLDERID \_ QuickLaunch**](knownfolderid.md)) sigue estando disponible por compatibilidad con versiones anteriores, aunque ya no hay una interfaz inicio rápido usuario. Sin embargo, las nuevas aplicaciones no deben pedir que se agregue un icono a inicio rápido durante la instalación.

 

Para obtener más información, [vea Application User Model IDs (AppUserModelIDs) ( Id. de modelo de usuario de aplicación [AppUserModelID]).](appids.md)

## <a name="jump-lists"></a>Listas de saltos

Normalmente, un usuario inicia un programa con la intención de acceder a un documento o realizar tareas dentro del programa. Es posible que el usuario de un programa de juego quiera llegar a un juego guardado o iniciarse como un carácter específico en lugar de reiniciar un juego desde el principio. Para conseguir que los usuarios lleguen de forma [](#tasks) más eficaz a su objetivo final, se adjunta una lista  de destinos y tareas comunes asociadas a una aplicación al botón de la barra de tareas de esa aplicación (así como a la entrada de menú Inicio equivalente). [](#destinations) Este es el nombre de la Lista de accesos directos. El Lista de accesos directos está disponible si el botón de la barra de tareas está en estado iniciador (la aplicación no se está ejecutando) o si representa una o varias ventanas. Al hacer clic con el botón derecho en la barra de tareas, se muestra el Lista de accesos directos de la aplicación, como se muestra en la ilustración siguiente.

![jump list con categorías ancladas, frecuentes y tareas](images/taskbar/jumplist.png)

De forma predeterminada, un Lista de accesos directos estándar contiene dos categorías: elementos recientes y elementos anclados, aunque como solo se muestran categorías con contenido en la interfaz de usuario, ninguna de estas categorías se muestra en el primer inicio. Siempre hay un icono de inicio de aplicación (para iniciar más instancias de la aplicación), una  opción para anclar o desanclar la aplicación de la barra de tareas y un comando Cerrar para cualquier ventana abierta.

## <a name="destinations"></a>Destinations

Las **categorías Recientes** y **Frecuentes** se consideran que contienen destinos. Un destino, normalmente un archivo, un documento o una dirección URL, es algo que se puede editar, examinar, ver, y así sucesivamente. Piense en un destino como algo en lugar de como una acción. Normalmente, un destino es un elemento del espacio de nombres shell, representado por [**un IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) o [**IShellLink.**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) Estas partes de la lista de  destino son análogas a la lista de documentos usados recientemente del menú Inicio (ya no se muestra de forma predeterminada) y a la lista de aplicaciones usadas con frecuencia, pero son específicas de una aplicación y, por tanto, son más precisas y útiles para el usuario. Los resultados usados en la lista de destino se calculan a través de llamadas a [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). Tenga en cuenta que cuando el usuario abre un archivo desde el Explorador de Windows o usa el cuadro de diálogo de archivo común para abrir, guardar o crear un archivo, se llama automáticamente a **SHAddToRecentDocs,** lo que hace que muchas aplicaciones puedan mostrar sus elementos recientes en la lista de destino sin ninguna acción por su parte.

Iniciar un destino es muy parecido a iniciar un elemento mediante el **comando Abrir** con. La aplicación se inicia con ese destino cargado y listo para usarse. Los elementos de la lista de destino también se pueden arrastrar de la lista a un destino de colocación, como un mensaje de correo electrónico. Al tener estos elementos centralizados en una lista de destino, se obtiene a los usuarios a los que desean ir mucho más rápido, que es el objetivo.

A medida que los elementos aparecen en  la categoría [](#customizing-jump-lists) Reciente de una lista de destino (o la categoría Frecuente o una categoría personalizada como se describe en una sección posterior), es posible que un usuario quiera asegurarse de que el elemento siempre está en la lista para un acceso rápido.  Para ello, puede anclar ese elemento a la lista, lo que agrega el elemento a la **categoría Anclado.** Cuando un usuario está trabajando activamente con un destino, lo desea fácilmente y, por tanto, lo anclaría a la lista de destinos de la aplicación. Una vez que haya terminado el trabajo del usuario, simplemente desanclará el elemento. Este control de usuario mantiene la lista sin cambios y pertinente.

Una lista de destino se puede considerar como una versión específica de la aplicación del **menú** Inicio. Una lista de destino no es un menú contextual. Se puede hacer clic con el botón derecho en cada elemento de una lista de destino para su propio menú contextual.

### <a name="apis"></a>API existentes

-   [**IApplicationDestinations::RemoveDestination**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removedestination)
-   [**IApplicationDestinations::RemoveAllDestinations**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removealldestinations)
-   [**IApplicationDocumentLists::GetList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist)
-   [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)

## <a name="tasks"></a>Tareas

Otra parte integrada de un Lista de accesos directos es la **categoría** Tareas. Aunque un destino es algo, una tarea es una acción y, en este caso, es una acción específica de la aplicación. Dicho de otro modo, un destino es un sustantivo y una tarea es un verbo. Normalmente, las tareas son [**elementos de IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) con argumentos de línea de comandos que indican una funcionalidad determinada que puede desencadenar una aplicación. Una vez más, la idea es centralizar tanta información relacionada con una aplicación como sea práctico.

Las aplicaciones definen tareas basadas en las características del programa y en las cosas clave que se espera que haga un usuario con ellas. Las tareas deben estar sin contexto, ya que no es necesario que la aplicación se ejecute para que funcionen. También deben ser las acciones estadísticamente más comunes que realizaría un usuario normal en una aplicación, como redactar un mensaje de correo electrónico o abrir el calendario en un programa de correo, crear un nuevo documento en un procesador de palabras, iniciar una aplicación en un modo determinado o iniciar uno de sus subcomandos. Una aplicación no debe llenar el menú con características avanzadas que los usuarios estándar no necesitarán o acciones únicas, como el registro. No use tareas para elementos promocionales, como actualizaciones u ofertas especiales.

Se recomienda encarecidamente que la lista de tareas sea estática. Debe seguir siendo el mismo independientemente del estado o el estado de la aplicación. Aunque es posible variar la lista dinámicamente, debe considerar que esto podría confundir al usuario que no espera que cambie esa parte de la lista de destino.

### <a name="apis"></a>API existentes

-   [**ICustomDestinationList::AddUserTasks**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-addusertasks)

## <a name="customizing-jump-lists"></a>Personalización de listas de accesos jump

Una aplicación puede definir sus propias categorías y agregarlas además  de o en lugar de las categorías **Recientes** y Frecuentes estándar en un Lista de accesos directos. La aplicación puede controlar sus propios destinos en esas categorías personalizadas en función de la arquitectura y el uso previsto de la aplicación. En la captura de pantalla siguiente se muestra un Lista de accesos directos personalizado con una categoría Historial.

![lista de saltos personalizada](images/taskbar/customjumplist.png)

Si una aplicación decide proporcionar una categoría personalizada, esa aplicación asume la responsabilidad de rellenarla. El contenido de la categoría todavía debe ser específico del usuario y basarse en el historial de usuarios, las acciones o ambos, pero a través de una categoría personalizada una aplicación puede determinar lo que quiere realizar y lo que quiere omitir, quizás en función de una opción de aplicación. Por ejemplo, un programa de audio podría optar por incluir solo los discos reproducdos recientemente y omitir las pistas individuales reproducdas recientemente.

Si un usuario ha quitado un elemento de la lista, que siempre es una opción de usuario, la aplicación debe respetarlo. La aplicación también debe asegurarse de que los elementos de la lista son válidos o de que se producirá un error correctamente si se han eliminado. Los elementos individuales o todo el contenido de la lista se pueden quitar mediante programación.

El sistema determina el número máximo de elementos de una lista de destino en función de varios factores, como la resolución de pantalla y el tamaño de fuente. Si no hay espacio suficiente para todos los elementos de todas las categorías, se truncan de abajo hacia arriba.

### <a name="apis"></a>API existentes

-   [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)
-   [**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)
-   [**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)

## <a name="thumbnail-toolbars"></a>Barras de herramientas de miniaturas

Para proporcionar acceso a los comandos clave de una ventana determinada sin hacer que el usuario restaure o active la ventana de la aplicación, se puede incrustar un control de barra de herramientas activo en la vista previa de miniaturas de esa ventana. Por ejemplo, Reproductor de Windows Media puede ofrecer controles de transporte multimedia estándar, como reproducir, pausar, silenciar y detener. La interfaz de usuario muestra esta barra de herramientas directamente debajo de la miniatura, como se muestra en la ilustración siguiente, no cubre ninguna parte de ella.

![barra de tareas en miniatura para el Reproductor de Windows Media, con tres botones: atrás, reproducir y reenviar](images/taskbar/thumbbar.png)

Esta barra de herramientas es simplemente el conocido control común estándar de la barra de herramientas. Tiene un máximo de siete botones. El identificador, la imagen, la información sobre herramientas y el estado de cada botón se definen en una estructura que, a continuación, se pasa a la barra de tareas. La aplicación puede mostrar, habilitar, deshabilitar u ocultar botones de la barra de herramientas de miniaturas según sea necesario para su estado actual.

Dado que hay espacio limitado para mostrar miniaturas y un número variable de miniaturas para mostrar, las aplicaciones no tienen garantizado un tamaño de barra de herramientas determinado. Si el espacio está restringido, los botones de la barra de herramientas se truncan de derecha a izquierda. Por lo tanto, al diseñar la barra de herramientas, debe priorizar los comandos asociados a los botones y asegurarse de que lo más importante es lo primero y que es menos probable que se desasoye debido a problemas de espacio.

> [!Note]  
> Cuando una aplicación muestra una ventana, el sistema crea su botón de la barra de tareas. Cuando el botón está en su lugar, la barra de tareas envía un **mensaje TaskbarButtonCreated** a la ventana. Su valor se calcula mediante una llamada [**a RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)(L("TaskbarButtonCreated") . La aplicación debe recibir ese mensaje antes de llamar a cualquier [**método ITaskbarList3.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3)

 

### <a name="api"></a>API

-   [**ITaskbarList3::ThumbBarAddButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [**ITaskbarList3::ThumbBarSetImageList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   [**ITaskbarList3::ThumbBarUpdateButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarupdatebuttons)
-   [**THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton)

## <a name="icon-overlays"></a>Superposiciones de iconos

Una aplicación puede comunicar ciertas notificaciones y el estado al usuario a través de su botón de la barra de tareas mediante la presentación de superposiciones pequeñas en el botón. Estas superposiciones son similares al tipo de superposición existente que se usa para accesos directos o notificaciones de seguridad, que se muestra en la esquina inferior derecha del botón. Para mostrar un icono de superposición, la barra de tareas debe estar en el modo de icono grande predeterminado, como se muestra en la siguiente captura de pantalla.

![Botón de la barra de tareas de Windows Messenger con una superposición para indicar un estado disponible](images/taskbar/taskbaroverlay.png)

Las superposiciones de iconos sirven como notificación contextual del estado y están diseñadas para negar la necesidad de un icono de estado de área de notificación independiente para comunicar esa información al usuario. Por ejemplo, el nuevo estado de correo de Microsoft Outlook, que se muestra actualmente en el área de notificación, ahora se puede indicar a través de una superposición en el botón de la barra de tareas. Una vez más, debe decidir durante el ciclo de desarrollo qué método es el mejor para la aplicación. Los iconos superpuestos están diseñados para proporcionar notificaciones o un estado importante de larga duración, como el estado de la red, el estado de mensajería o el correo nuevo. No se debe presentar al usuario superposiciones o animaciones que cambien constantemente.

Dado que se superpone una sola superposición en el botón de la barra de tareas y no en las miniaturas de ventana individuales, se trata de una característica por grupo en lugar de por ventana. Las solicitudes de iconos de superposición se pueden recibir desde ventanas individuales de un grupo de la barra de tareas, pero no se ponen en cola. La última superposición recibida es la que se muestra.

### <a name="apis"></a>API existentes

-   [**ITaskbarList3::SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon)

## <a name="progress-bars"></a>Barras de progreso

Se puede usar un botón de la barra de tareas para mostrar una barra de progreso. Esto permite que una ventana proporcione información de progreso al usuario sin que ese usuario tenga que cambiar a la propia ventana. El usuario puede mantener la productividad en otra aplicación mientras ve de un vistazo el progreso de una o varias operaciones que se producen en otras ventanas. Está pensado para que una barra de progreso de un botón de la barra de tareas refleje un indicador de progreso más detallado en la propia ventana. Esta característica se puede usar para realizar el seguimiento de copias de archivos, descargas, instalaciones, grabación de medios o cualquier operación que vaya a tardar un período de tiempo. Esta característica no está pensada para su uso con acciones normalmente periféricos, como la carga de una página web o la impresión de un documento. Ese tipo de progreso se debe seguir mostrando en la barra de estado de una ventana.

La barra de tareas de la barra de tareas es una experiencia similar al conocido control Barra de progreso. Puede mostrar un progreso determinado en función de un porcentaje completado de la operación o un progreso de estilo marqueso indeterminado para indicar que la operación está en curso sin ninguna predicción de tiempo restante. También puede mostrar que la operación está en pausa o ha detectado un error y requiere la intervención del usuario.

### <a name="apis"></a>API existentes

-   [**ITaskbarList3::SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate)
-   [**ITaskbarList3::SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue)

## <a name="deskbands"></a>Deskbands

En versiones de Windows anteriores a Windows 7, se podía lograr algo similar a la funcionalidad de la barra de herramientas en miniatura a través de una barra de escritorio, una barra de herramientas hospedada en la barra de tareas. Por ejemplo, Reproductor de Windows Media puede minimizar a la barra de tareas como un conjunto de controles de transporte en lugar de un botón estándar. En Windows 7, todavía se pueden implementar cintas de escritorio y las barras de herramientas en miniatura no están diseñadas para reemplazarlas todas. No todas las aplicaciones se prestarán a una barra de herramientas en miniatura y otra solución, como deskband o una tarea de una lista de destino, podría ser la respuesta adecuada para la aplicación. debe decidir qué solución funciona mejor para la aplicación como parte del ciclo de desarrollo. Sin embargo, tenga en cuenta que deskbands debe admitir Windows Con translucency ("glass") habilitado y la [**interfaz IDeskBand2.**](/windows/desktop/api/Shobjidl/nn-shobjidl-ideskband2)

### <a name="apis"></a>API existentes

-   [**IDeskBand2**](/windows/desktop/api/Shobjidl/nn-shobjidl-ideskband2)

## <a name="notification-area"></a>Área de notificación

Se han realizado cambios en el área de notificación que dan al usuario mucho más control sobre los iconos que aparecen en la barra de tareas. Todos los iconos de notificación ahora están ocultos de forma predeterminada y esa visibilidad no se puede controlar mediante programación. Solo el usuario puede elegir qué iconos de notificación aparecen en la barra de tareas. Cuando se muestra un globo de notificación, el icono se vuelve visible temporalmente, pero incluso entonces un usuario puede optar por silenciarlos. Por lo tanto, una superposición de iconos en un botón de la barra de tareas se convierte en una opción atractiva cuando se quiere que la aplicación comunique esa información a los usuarios.

## <a name="thumbnails"></a>Miniaturas

En Windows Vista, al mantener el puntero sobre el botón de la barra de tareas de una aplicación se muestra una miniatura que representa la ventana en ejecución. Si la barra de tareas ha contraído las ventanas de la aplicación, la miniatura representa esto al aparecer como una pila, pero solo se muestra la ventana activa en la propia miniatura.

En Windows 7, cada miembro de un grupo se muestra como una miniatura independiente y ahora también es un destino de conmutador. Una aplicación puede definir sus elementos secundarios (como verdaderas ventanas secundarias, documentos individuales o pestañas) y proporcionar miniaturas correspondientes para cada una de esas ventanas, incluso cuando normalmente no aparecen en la barra de tareas. Esto permite a los usuarios cambiar directamente a la vista de la aplicación que desean en lugar de cambiar a la aplicación y, a continuación, cambiar a su destino. Por ejemplo, las aplicaciones de interfaz de varios documentos (MDI)/interfaz de documento con pestañas (TDI) pueden mostrar cada documento o pestaña como una miniatura independiente y cambiar de destino cuando el mouse se desplaza sobre el botón de la barra de tareas de un grupo.

![tres miniaturas de la barra de tareas que representan pestañas individuales en Windows Internet Explorer](images/taskbar/taskbarthumbnails.png)

> [!Note]  
> Como en Windows Vista, Aero debe estar activo para ver las miniaturas.

 

### <a name="api"></a>API

-   [**ITaskbarList3::RegisterTab**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-registertab)
-   [**ITaskbarList3::SetTabActive**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settabactive)
-   [**ITaskbarList3::SetTabOrder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settaborder)
-   [**ITaskbarList3::UnregisterTab**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-unregistertab)
-   [**ITaskbarList4::SetTabProperties**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist4-settabproperties)

Las representaciones en miniatura para ventanas suelen ser automáticas, pero en los casos en los que el resultado no es óptimo, la miniatura se puede especificar explícitamente. De forma predeterminada, solo las ventanas de nivel superior tienen una miniatura generada automáticamente para ellas y las miniaturas de las ventanas secundarias aparecen como una representación genérica. Esto puede dar lugar a una experiencia menos ideal (e incluso confusa) para el usuario final. Una miniatura de destino de conmutador específica para cada ventana secundaria, por ejemplo, proporciona una experiencia de usuario mucho mejor.

### <a name="api"></a>API

-   [**DwmSetWindowAttribute**](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)
-   [**DwmSetIconicThumbnail**](/windows/win32/api/dwmapi/nf-dwmapi-dwmseticonicthumbnail)
-   [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap)
-   [**DwmInvalidateIconicBitmaps**](/windows/win32/api/dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
-   [**WM \_ DWMSENDICONICTHUMBNAIL**](../dwm/wm-dwmsendiconicthumbnail.md)
-   [**WM \_ DWMSENDICONICLIVEPREVIEWBITMAP**](../dwm/wm-dwmsendiconiclivepreviewbitmap.md)

Puede seleccionar un área determinada de la ventana para usarla como miniatura. Esto puede ser útil cuando una aplicación sabe que sus documentos o pestañas aparecerán de forma similar cuando se ven en tamaño de miniatura. A continuación, la aplicación puede optar por mostrar solo la parte de su área cliente que el usuario puede usar para distinguir entre miniaturas. Sin embargo, al mantener el puntero sobre cualquier miniatura se muestra una vista de la ventana completa detrás de ella para que el usuario también pueda echar un vistazo a ella rápidamente.

Si hay más miniaturas de las que se pueden mostrar, la vista previa se revierte a la miniatura heredada o a un icono estándar.

### <a name="api"></a>API

-   [**ITaskbarList3::SetThumbnailClip**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setthumbnailclip)

Para agregar **Anclar** a la barra de tareas al menú contextual de un elemento, que normalmente solo es necesario para los tipos de archivo que incluyen la entrada [IsShortCut,](./links.md) se registra el controlador de menú contextual adecuado. Esto también se aplica a **Anclar al menú Inicio**. Vea [Registrar controladores de extensión de Shell](reg-shell-exts.md) para obtener más información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Barra de tareas](taskbar.md)
</dt> <dt>

[Id. de modelo de usuario de aplicación (AppUserModelIDs)](appids.md)
</dt> <dt>

[Notificaciones y el área de notificación](notification-area.md)
</dt> </dl>

 

 
