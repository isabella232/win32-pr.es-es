---
title: Acerca de los controles List-View
description: Un control de vista de lista es una ventana que muestra una colección de elementos.
ms.assetid: 163f7778-690c-4166-b0c5-c7be1a03ae98
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: fe1b953bf7d7204a3afffcfa0bc5aa5af9bf94fa
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105649465"
---
# <a name="about-list-view-controls"></a>Acerca de los controles List-View

Vea el [ejemplo de control ListView virtual](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw).

Un control de vista de lista es una ventana que muestra una colección de elementos. Los controles de vista de lista proporcionan varias maneras de organizar y mostrar los elementos, y son mucho más flexibles que los sencillos [cuadros de lista](list-boxes.md). Por ejemplo, se puede mostrar información adicional sobre cada elemento en columnas a la derecha del icono y la etiqueta.

-   [Estilos y vistas de la vista de lista](#list-view-styles-and-views)
    -   [Estilos de List-View extendidos](#extended-list-view-styles)
-   [Estilo de List-View virtual](#virtual-list-view-style)
    -   [Crear un control de List-View virtual](#creating-a-virtual-list-view-control)
    -   [Problemas de compatibilidad](#compatibility-issues)
    -   [Controlar los códigos de notificación de control de List-View virtual](#handling-virtual-list-view-control-notification-codes)
    -   [Administración de caché](#cache-management)
-   [Mostrar y Mostrar áreas de trabajo](#list-view-working-areas)
-   [Listas de imágenes de vista de lista](#list-view-image-lists)
-   [Lista-ver elementos y subelementos](#list-view-items-and-subitems)
    -   [Enumerar Estados de elemento de vista](#list-view-item-states)
    -   [Elementos de devolución de llamada y máscara de devolución de llamada](#callback-items-and-the-callback-mask)
    -   [Mostrar la posición del elemento de vista](#list-view-item-position)
    -   [Organizar, ordenar y buscar elementos](#arranging-sorting-and-finding-items)
-   [Columnas de la vista de lista](#list-view-columns)
-   [Posición de desplazamiento de la vista de lista](#list-view-scroll-position)
-   [Edición de etiquetas de vista de lista](#list-view-label-editing)
-   [Ver y mostrar colores](#list-view-colors)
-   [Organizar elementos de lista por grupo](#arranging-list-items-by-group)
-   [Marcas de inserción](#insertion-marks)

## <a name="list-view-styles-and-views"></a>List-View estilos y vistas

Los controles de vista de lista pueden mostrar elementos en cinco vistas diferentes. El estilo de ventana del control especifica la vista predeterminada. Los estilos de ventana adicionales especifican la alineación de los elementos y las características específicas del control. En la tabla siguiente se describen las vistas.



| Nombre de vista             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vista de iconos             | Especificado por el estilo de la ventana del [**\_ icono de LVS**](list-view-window-styles.md) o pasando el icono de la **\_ vista \_ LV** con el mensaje [**\_ SETVIEW de LVM**](lvm-setview.md) . Cada elemento aparece como un icono de tamaño normal debajo del cual figura una etiqueta. El usuario puede arrastrar los elementos a cualquier ubicación de la ventana de vista de lista.                                                                                                                                                                                                                                         |
| Vista de iconos pequeños       | Especificado por el estilo de la ventana de [**LVS \_ SmallIcon**](list-view-window-styles.md) o pasando la vista de LV en el [**\_ SETVIEW de LVM**](lvm-setview.md). **\_ \_** Cada elemento aparece como un icono pequeño con la etiqueta a la derecha. El usuario puede arrastrar los elementos a cualquier ubicación.                                                                                                                                                                                                                                                       |
| Vista de lista             | Especificado por el estilo de la ventana [**\_ lista de LVS**](list-view-window-styles.md) o pasando la **lista de \_ vistas \_ de LV** con el [**LVM \_ SETVIEW**](lvm-setview.md). Cada elemento aparece como un icono pequeño con una etiqueta a la derecha. Los elementos se organizan en columnas y el usuario no puede arrastrarlos a una ubicación arbitraria.                                                                                                                                                                                                                               |
| Vista informe (detalles) | Lo especifica el estilo de la ventana de [**\_ Informe LVS**](list-view-window-styles.md) o pasando los detalles de la **\_ vista \_ LV** con el [**LVM \_ SETVIEW**](lvm-setview.md). Cada elemento aparece en su propia línea, con información organizada en columnas. La columna situada más a la izquierda siempre está justificada y contiene el icono y la etiqueta pequeños. Las columnas subsiguientes contienen los subelementos especificados por la aplicación. Cada columna tiene un encabezado, a menos que especifique también el estilo de ventana de [**LVS \_ NOCOLUMNHEADER**](list-view-window-styles.md) . |
| Vista de mosaico             | **Versión 6 y posteriores.** Se especifica al pasar el **\_ \_ icono de la vista LV** con el [**LVM \_ SETVIEW**](lvm-setview.md). Cada elemento aparece como un icono de tamaño completo con una etiqueta de una o varias líneas junto a él.                                                                                                                                                                                                                                                                                                                                                        |



 

Las capturas de pantalla siguientes usan vistas para mostrar diferentes cantidades de información sobre cada una de las siete mascotas. Las vistas muestran cómo podría aparecer la información en Windows Vista. Los estilos visuales del control se han establecido en el tema "explorador" mediante [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).

En la captura de pantalla siguiente se muestra la vista detalles.

![captura de pantalla que muestra información en cinco columnas y siete filas](images/lv-detailsview.png)

En la captura de pantalla siguiente se muestra la vista de iconos.

![captura de pantalla que muestra solo el nombre de cada mascota y un icono que indica la especie](images/lv-iconview.png)

En la captura de pantalla siguiente se muestra la vista de lista.

![captura de pantalla que muestra, para cada mascota, un icono grande junto al texto del nombre, la raza y el precio de la mascota](images/lv-listview.png)

En la captura de pantalla siguiente se muestra la vista de mosaico.

![vista en mosaico.](images/lv-tileview.png)

Puede cambiar el tipo de vista después de crear un control de vista de lista. Para recuperar y cambiar el estilo de ventana, utilice las funciones [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) y [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) . Para determinar los estilos de ventana de la vista actual, use el valor de [**\_ TYPEMASK de LVS**](list-view-window-styles.md) .

Puede controlar la forma en que los elementos se organizan en la vista de iconos o iconos pequeños especificando el estilo de ventana [**LVS \_ ALIGNTOP**](list-view-window-styles.md) (predeterminado) o el valor de [**LVS \_ ALIGNLEFT**](list-view-window-styles.md) .

Puede cambiar la alineación después de crear un control de vista de lista. Para determinar la alineación actual, use el valor de [**LVS \_ ALIGNMASK**](list-view-window-styles.md) .

Los estilos de ventana adicionales proporcionan otras opciones, como si un usuario puede editar etiquetas o seleccionar más de un elemento a la vez. Para obtener una lista completa, consulte [estilos de la ventana de la vista de lista](list-view-window-styles.md).

### <a name="extended-list-view-styles"></a>Estilos de List-View extendidos

Los estilos extendidos de control de vista de lista proporcionan opciones como casillas, barras de desplazamiento plana, líneas de cuadrícula y seguimientos activos. Para obtener una lista completa, consulte [estilos de List-View extendidos](extended-list-view-styles.md). No tiene acceso a los estilos extendidos de la vista de lista de la misma manera que a los estilos de ventana estándar. No se usan las funciones [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) y [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para realizar cambios de estilo extendido.

Hay dos mensajes que establecen y recuperan información de estilo extendido, [**LVM \_ SETEXTENDEDLISTVIEWSTYLE**](lvm-setextendedlistviewstyle.md) y [**LVM \_ GETEXTENDEDLISTVIEWSTYLE**](lvm-getextendedlistviewstyle.md). En lugar de enviar los mensajes explícitamente, puede utilizar las siguientes macros correspondientes: [**ListView \_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle), [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex)y [**ListView \_ GetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle).

## <a name="virtual-list-view-style"></a>Estilo de List-View virtual

Una vista de lista virtual es un control de vista de lista que tiene el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) . Este estilo permite al control administrar millones de elementos porque el propietario recibe la carga de administrar los datos de los elementos. Esto le permite usar el control de vista de lista virtual con bases de datos de gran tamaño, donde ya están implementados determinados métodos de acceso a datos.

Un control de vista de lista virtual mantiene muy poca información de elemento. A excepción de la selección de elementos y la información de foco, el propietario del control debe administrar toda la información de los elementos. Otros procesos solicitan información del elemento al propietario mediante los códigos de notificación de [LVN \_ GETDISPINFO](lvn-getdispinfo.md) .

Dado que este tipo de control de lista está pensado para conjuntos de datos grandes, se recomienda almacenar en caché los datos de elementos solicitados para mejorar el rendimiento de la recuperación. La vista de lista proporciona un mecanismo de sugerencias de caché para ayudar a optimizar la memoria caché. La sugerencia se implementa en forma de un código de notificación [ \_ ODCACHEHINT de LVN](lvn-odcachehint.md) .

### <a name="creating-a-virtual-list-view-control"></a>Crear un control de List-View virtual

Puede crear controles de vista de lista virtual mediante la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando el estilo de ventana de [**LVS \_ OWNERDATA**](list-view-window-styles.md) como parte del parámetro de función *dwStyle* . No se admite el cambio dinámico al estilo **LVS \_ OWNERDATA** .

Puede usar el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) en combinación con la mayoría de los demás estilos de ventana, excepto el estilo [**LVS \_ SORTASCENDING**](list-view-window-styles.md) o [**LVS \_ SORTDESCENDING**](list-view-window-styles.md) . Todos los controles virtuales de vista de lista virtual tienen como valor predeterminado el estilo de [**\_ organización LVS**](list-view-window-styles.md) .

Para habilitar que los elementos se muestren en la lista, primero debe enviar el mensaje [**LVM \_ SETITEMCOUNT**](lvm-setitemcount.md) , ya sea explícitamente o mediante la macro [**\_ SetItemCountEx de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) .

Los mensajes siguientes no son compatibles con el [**estilo LVS \_ OWNERDATA**](list-view-window-styles.md) : [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md), [**LVM \_ GETITEMTEXT**](lvm-getitemtext.md), [**LVM \_ SETTILEINFO**](lvm-settileinfo.md)y [**LVM \_ MAPIDTOINDEX**](lvm-mapidtoindex.md).

### <a name="compatibility-issues"></a>Problemas de compatibilidad

Los cuatro estilos de vista de lista (icono, icono pequeño, lista y vista de informe) admiten el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) . Los controles de vista de lista que tienen el estilo **LVS \_ OWNERDATA** no almacenan ninguna información específica del elemento. Por lo tanto, las únicas marcas de estado de los elementos válidos que se pueden aplicar a un elemento son [**LVIS \_ selected**](list-view-item-states.md) y [**LVIS \_ Focused**](list-view-item-states.md). No se almacena ninguna otra información de estado. En concreto, el control de vista de lista no mantiene las imágenes de estado o de superposición para cada elemento. Sin embargo, puede hacer que el control de vista de lista consulte la aplicación para estas imágenes mediante el envío de un mensaje [**\_ SETCALLBACKMASK LVM**](lvm-setcallbackmask.md) .

La mayoría de los mensajes de control de vista de lista y las macros asociadas son totalmente compatibles. Sin embargo, algunos mensajes tienen limitaciones o no se admiten cuando se usa el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) . En la tabla siguiente se resumen los mensajes afectados.



| Message                                             | Limitación                                                                                                                                                                                                                                                      |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**organización del LVM \_**](lvm-arrange.md)                 | No admite el estilo de **LVA \_ SNAPTOGRID** .                                                                                                                                                                                                                 |
| [**\_DELETEALLITEMS LVM**](lvm-deleteallitems.md)   | Establece el recuento de elementos en cero y borra todas las variables de selección internas, pero realmente no elimina ningún elemento. Crea una devolución de llamada de notificación.                                                                                                           |
| [**LVM \_ DELETEITEM**](lvm-deleteitem.md)           | Solo se admite para la integridad de la selección y realmente no elimina un elemento.                                                                                                                                                                                 |
| [**\_GETITEMSTATE LVM**](lvm-getitemstate.md)       | Devuelve solo los Estados de foco y selección (es decir, los Estados almacenados por el control de vista de lista).                                                                                                                                                                |
| [**\_GETNEXTITEM LVM**](lvm-getnextitem.md)         | No admite los criterios de búsqueda de la vista de lista **LVNI \_ CUT**, **LVNI \_ Hidden** o **LVNI \_ DROPHILITED**. Se admiten todos los demás criterios.                                                                                                                     |
| [**\_GETWORKAREAS LVM**](lvm-getworkareas.md)       | No se admite.                                                                                                                                                                                                                                               |
| [**el LVM \_ INSERTITEM**](lvm-insertitem.md)           | Solo se admite para la integridad de la selección.                                                                                                                                                                                                                      |
| [**\_SETITEM LVM**](lvm-setitem.md)                 | No se admite. Para establecer el estado del elemento, use el mensaje [**\_ SetItemState de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) .                                                                                                                                               |
| [**\_SETITEMCOUNT LVM**](lvm-setitemcount.md)       | Establece el número de elementos que hay actualmente en la lista. Si el control de vista de lista envía una notificación que solicita datos para cualquier elemento hasta el máximo establecido, el propietario debe estar preparado para proporcionar los datos. Los parámetros de mensaje admiten controles de vista de lista virtual. |
| [**\_SETITEMPOSITION LVM**](lvm-setitemposition.md) | No se admite.                                                                                                                                                                                                                                               |
| [**\_SETITEMSTATE LVM**](lvm-setitemstate.md)       | Solo permite cambiar los Estados de selección y foco para el elemento.                                                                                                                                                                                          |
| [**\_SETITEMTEXT LVM**](lvm-setitemtext.md)         | No se admite. Es responsabilidad de la aplicación mantener los textos del elemento.                                                                                                                                                                            |
| [**\_SETWORKAREAS LVM**](lvm-setworkareas.md)       | No se admite.                                                                                                                                                                                                                                               |
| [**\_SORTITEMS LVM**](lvm-sortitems.md)             | No se admite. Es responsabilidad de la aplicación presentar los elementos en el orden deseado.                                                                                                                                                             |



 

### <a name="handling-virtual-list-view-control-notification-codes"></a>Controlar los códigos de notificación de control de List-View virtual

Los controles de vista de lista con el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) envían los mismos códigos de notificación que otros controles de vista de lista y dos adicionales: [LVN \_ ODCACHEHINT](lvn-odcachehint.md) y [LVN \_ ODFINDITEM](lvn-odfinditem.md). A continuación se muestran las notificaciones más comunes que envía el control de vista de lista con el estilo **LVS \_ OWNERDATA** .



|                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LVN \_ GETDISPINFO](lvn-getdispinfo.md) | Un control de vista de lista virtual mantiene muy poca información del elemento. Como resultado, a menudo envía el código de notificación [LVN \_ GETDISPINFO](lvn-getdispinfo.md) para solicitar información del elemento. Este mensaje se administra de forma muy similar a los elementos de devolución de llamada de un control de lista estándar. Dado que el número de elementos que admite el control puede ser muy grande, el almacenamiento en caché de los datos del elemento mejora el rendimiento. Al controlar LVN \_ GETDISPINFO, el propietario del control primero intenta proporcionar la información de los elementos solicitados desde la memoria caché (para obtener más información, vea [Administración de caché](#cache-management)). Si el elemento solicitado no está almacenado en caché, el propietario debe estar preparado para proporcionar la información por otros medios. |
| [LVN \_ ODCACHEHINT](lvn-odcachehint.md) | Una vista de lista virtual envía el código de notificación [LVN \_ ODCACHEHINT](lvn-odcachehint.md) para ayudar a optimizar la memoria caché. El código de notificación proporciona valores de índice inclusivos para un intervalo de elementos que recomienda almacenar en caché. Tras recibir el código de notificación, el propietario debe estar preparado para cargar la memoria caché con información del elemento para el intervalo solicitado, de modo que la información estará disponible fácilmente cuando se envíe un mensaje [ \_ GETDISPINFO de LVN](lvn-getdispinfo.md) .                                                                                                                                                                                                                                   |
| [LVN \_ ODFINDITEM](lvn-odfinditem.md)   | El código de notificación de [ \_ ODFINDITEM de LVN](lvn-odfinditem.md) se envía mediante un control de vista de lista virtual cuando el control necesita que el propietario busque un elemento de devolución de llamada determinado. El código de notificación se envía cuando el control de vista de lista recibe el acceso rápido a la tecla o cuando recibe un mensaje [**\_ FINDITEM de LVM**](lvm-finditem.md) . La información de búsqueda se envía en forma de una estructura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) , que es un miembro de la estructura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) . El propietario debe estar preparado para buscar un elemento que coincida con la información proporcionada por el control de vista de lista. El propietario devuelve el índice del elemento si se realiza correctamente, o-1 si no se encuentra ningún elemento coincidente.               |



 

### <a name="cache-management"></a>Administración de caché

Un control de vista de lista con el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) produce un gran número de códigos de notificación de [LVN \_ GETDISPINFO](lvn-getdispinfo.md) y, para ayudar a optimizar la memoria caché, un mensaje [LVN \_ ODCACHEHINT](lvn-odcachehint.md) . \_Los mensajes de LVN ODCACHEHINT proporcionan información sobre los elementos recomendados que se van a incluir en la memoria caché. Estos mensajes se envían como mensajes de [**\_ notificación de WM**](wm-notify.md) , donde el valor *lParam* actúa como la dirección de una estructura [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) .

La estructura [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) incluye dos miembros enteros, **iFrom** y **iTo**, que representan los puntos de conexión inclusivos de un intervalo de elementos que es más probable que se necesiten. El propietario debe estar preparado para cargar la memoria caché con la información del elemento para cada uno de los elementos del intervalo recomendado.

El control de lista suele necesitar información del primer elemento (desplazamiento 0). El código de notificación de [LVN \_ ODCACHEHINT](lvn-odcachehint.md) podría no incluir siempre el elemento 0, pero siempre debe incluirse en la memoria caché.

A menudo se tiene acceso a los últimos elementos de la lista. Por lo tanto, es posible que el propietario desee mantener una segunda caché que incluya los elementos al final de la lista. El intervalo solicitado de [LVN \_ ODCACHEHINT](lvn-odcachehint.md) puede comprobarse con la memoria caché final para que esté disponible automáticamente en lugar de volver a cargar el mismo intervalo de finalización cada vez.

## <a name="list-view-working-areas"></a>List-View áreas de trabajo

Los controles de vista de lista admiten áreas de trabajo, que son áreas virtuales rectangulares que usa el control de vista de lista para organizar sus elementos. Un área de trabajo no es una ventana y no puede tener un borde visible. De forma predeterminada, el control de vista de lista no tiene áreas de trabajo. Al crear un área de trabajo, puede crear un borde vacío en la parte izquierda, superior o derecha de los elementos, o hacer que se muestre una barra de desplazamiento horizontal cuando normalmente no hubiera ninguno.

Cuando se crea un área de trabajo, los elementos que se encuentran dentro del área de trabajo se convierten en miembros del área de trabajo. Del mismo modo, si un elemento se mueve a un área de trabajo, el elemento se convierte en un miembro de ese área de trabajo. Si un elemento no se encuentra dentro de un área de trabajo, se convierte automáticamente en miembro del primer área de trabajo (índice 0). Para colocar un nuevo elemento dentro de un área de trabajo específica, primero debe crear el elemento y, a continuación, usar el [**\_ SETITEMPOSITION LVM**](lvm-setitemposition.md) o el mensaje [**\_ SETITEMPOSITION32 de LVM**](lvm-setitemposition32.md) para moverlo al área de trabajo deseada.

La siguiente ilustración es un ejemplo de un control de vista de lista que contiene cuatro áreas de trabajo, cada una en un cuadrante diferente del área cliente.

![captura de pantalla de un control de vista de lista con un área de trabajo en cada cuadrante del área cliente](images/working.jpg)

Se pueden usar varias áreas de trabajo para crear áreas diferentes dentro de una vista. Puede crear áreas en una sola vista que tengan diferentes significados. Por ejemplo, una vista de un sistema de archivos puede tener un área para los archivos de lectura/escritura y otra para los archivos de solo lectura. El usuario puede clasificar los elementos colocándolos en áreas de trabajo diferentes. Si un archivo se mueve al área de solo lectura, se convertirá automáticamente en solo lectura.

Varias áreas de trabajo pueden intersectar, pero los elementos que se encuentran dentro de la intersección se convierten en miembros del área con el índice inferior; por lo tanto, es mejor evitar esta situación. Al ordenar varias áreas de trabajo, los elementos se ordenan en comparación con los demás elementos de la misma área de trabajo.

El número de áreas de trabajo se puede recuperar con el mensaje [**LVM \_ GETNUMBEROFWORKAREAS**](lvm-getnumberofworkareas.md) . Las áreas de trabajo se cambian con el mensaje [**LVM \_ SETWORKAREAS**](lvm-setworkareas.md) y se pueden recuperar con el mensaje [**LVM \_ GETWORKAREAS**](lvm-getworkareas.md) . Ambos mensajes toman la dirección de una matriz de estructuras [**Rect**](/previous-versions//dd162897(v=vs.85)) como *lParam* y el número de estructuras **Rect** como *wParam*. Los miembros **izquierdo** y **superior** de estas estructuras especifican las coordenadas de la esquina superior izquierda (el origen) del área de trabajo, y los miembros **derecho** e **inferior** especifican la esquina inferior derecha del área de trabajo. Todas las coordenadas están en coordenadas de cliente de la vista de lista. El número máximo de áreas de trabajo permitido se define mediante el valor de **LV \_ Max \_ WORKAREAS** .

Cambiar el área de trabajo no tiene ningún efecto en los controles de vista de lista que tienen la vista de [**\_ Informe**](list-view-window-styles.md) LVS o la [**\_ lista**](list-view-window-styles.md) de LVS, pero las áreas de trabajo se mantendrán cuando se cambie el tipo de vista. Con el [**\_ icono de LVS**](list-view-window-styles.md) y las vistas de [**LVS \_ SmallIcon**](list-view-window-styles.md) , el área de trabajo se puede modificar para cambiar la forma en que se muestran los elementos. Si se hace que el ancho del área de trabajo (derecha a la izquierda) sea mayor que el ancho del cliente del control, los elementos se ajustan en ese ancho y se muestra la barra de desplazamiento horizontal. Al reducir el ancho del área de trabajo más estrecha que el ancho del área cliente del control, los elementos se ajustan en el área de trabajo y no en el área cliente. Si se establece el miembro **izquierdo** o **superior** en un valor positivo, se mostrarán los elementos a partir del área de trabajo, creando un espacio vacío entre el borde del control y los elementos. También se puede crear un espacio vacío entre el borde derecho del control y los elementos haciendo que el ancho del área de trabajo sea menor que el ancho del cliente del control.

## <a name="list-view-image-lists"></a>List-View listas de imágenes

De forma predeterminada, un control de vista de lista no muestra imágenes de elementos. Para mostrar imágenes de elementos, debe crear listas de imágenes y asociarlas al control. Un control de vista de lista puede tener tres listas de imágenes:

-   Una lista de imágenes que contiene iconos de tamaño completo que se muestran cuando el control está en la vista de iconos.
-   Una lista de imágenes que contiene iconos pequeños que se muestran cuando el control está en la vista de iconos pequeños, en la vista de lista o en la vista de informe.
-   Una lista de imágenes que contiene imágenes de estado, que se muestran a la izquierda del icono pequeño o de tamaño completo. Puede usar las imágenes de estado, como las casillas activada y desactivada, para indicar los Estados de los elementos definidos por la aplicación. Las imágenes de estado se muestran en la vista de iconos, en la vista de iconos pequeños, en la vista de lista y en la vista de informe.

Las listas de imágenes de iconos completos y de tamaño completo también pueden contener *imágenes superpuestas*, que están diseñadas para dibujarse de forma transparente sobre los iconos de los elementos.

Para usar imágenes superpuestas en un control de vista de lista:

1.  Llame a la función [**ImageList \_ SetOverlayImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) para asignar un índice de imagen de superposición a una imagen en las listas de imágenes de iconos de tamaño completo y pequeño. Una imagen de superposición se identifica mediante un índice basado en uno.
2.  Puede asociar un índice de imagen de superposición a un elemento cuando se llama a la macro de [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) o [**ListView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) . Use la macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) para especificar un índice de imagen de superposición en el miembro **State** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) del elemento. También debe establecer los bits [**LVIS \_ OVERLAYMASK**](list-view-item-states.md) en el miembro **stateMask** .

Si se especifica una lista de imágenes de estado, un control de vista de lista Reserva espacio a la izquierda del icono de cada elemento en una imagen de estado.

Para asociar una imagen de estado a un elemento, utilice la macro [**INDEXTOSTATEIMAGEMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask) para especificar un índice de imagen de estado en el miembro **State** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . El Índice identifica una imagen en la lista de imágenes de estado del control. Aunque los índices de la lista de imágenes son de base cero, el control utiliza índices basados en uno para identificar las imágenes de estado. Un índice de imagen de estado cero indica que un elemento no tiene ninguna imagen de estado.

De forma predeterminada, cuando se destruye un control de vista de lista, destruye las listas de imágenes asignadas a él. Sin embargo, si un control de vista de lista tiene el estilo de ventana [**LVS \_ SHAREIMAGELISTS**](list-view-window-styles.md) , la aplicación es responsable de destruir las listas de imágenes cuando ya no se usan. Debe especificar este estilo si asigna las mismas listas de imágenes a varios controles de vista de lista. de lo contrario, es posible que más de un control intente destruir la misma lista de imágenes.

## <a name="list-view-items-and-subitems"></a>List-View elementos y subelementos

Cada elemento de un control de vista de lista tiene un icono, una etiqueta, un estado actual y un valor definido por la aplicación. Mediante el uso de mensajes de vista de lista, puede Agregar, modificar y eliminar elementos, así como recuperar información sobre los elementos.

Cada elemento puede tener uno o más *subelementos*. Un subelemento es una cadena que, en la vista de informe, se muestra en una columna independiente del icono y la etiqueta del elemento. Para especificar el texto de un subelemento, use el mensaje [**LVM \_ SETITEMTEXT**](lvm-setitemtext.md) o [**LVM \_ SETITEM**](lvm-setitem.md) . Todos los elementos de un control de vista de lista tienen el mismo número de subelementos. El número de subelementos viene determinado por el número de columnas en el control de vista de lista. Cuando se agrega una columna a un control de vista de lista, se especifica su índice de subelemento asociado.

La estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) define un elemento o subelemento de vista de lista. El miembro **iItem** es el índice de base cero del elemento. El miembro **iSubItem** es el índice basado en uno de un subelemento o cero si la estructura contiene información sobre un elemento. Los miembros adicionales especifican el texto, el icono, el estado y los datos del elemento. Los *datos de elemento* son un valor definido por la aplicación asociado a un elemento de vista de lista.

Para agregar un elemento a un control de vista de lista, use el mensaje de [**LVM \_ INSERTITEM**](lvm-insertitem.md) , especificando la dirección de una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . Antes de agregar varios elementos, puede enviar el control a un mensaje [**\_ SETITEMCOUNT LVM**](lvm-setitemcount.md) , especificando el número de elementos que el control va a contener en última instancia. Este mensaje permite al control de vista de lista reasignar sus estructuras de datos internas solo una vez en lugar de cada vez que se agrega un elemento. Puede determinar el número de elementos en un control de vista de lista mediante el mensaje [**LVM \_ GETITEMCOUNT**](lvm-getitemcount.md) . Si va a agregar un gran número de elementos a un control de vista de lista, puede acelerar el proceso desactivando volver a dibujar antes de agregar los elementos y, a continuación, habilitar el redibujo después de agregar los elementos. Use el mensaje de [**\_ SETREDRAW de WM**](/windows/desktop/gdi/wm-setredraw) para habilitar y deshabilitar el redibujo.

Para cambiar los atributos de un elemento de vista de lista, use el mensaje [**LVM \_ SETITEM**](lvm-setitem.md) , especificando la dirección de una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . El miembro de **máscara** de esta estructura especifica los atributos de elemento que desea cambiar. Por ejemplo, para cambiar solo el texto de un elemento o subelemento, use el [**mensaje \_ SETITEMTEXT de LVM**](lvm-setitemtext.md) .

Para recuperar información sobre un elemento de vista de lista, use el mensaje [**\_ GETITEM de LVM**](lvm-getitem.md) , especificando la dirección de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que se va a rellenar. El miembro de **máscara** de esta estructura especifica los atributos de elemento que se van a recuperar. Para recuperar solo el texto de un elemento o subelemento, use el mensaje [**\_ GETITEMTEXT de LVM**](lvm-getitemtext.md) .

Para eliminar un elemento de vista de lista, use el mensaje de [**LVM \_ DELETEITEM**](lvm-deleteitem.md) . Puede eliminar todos los elementos de un control de vista de lista mediante el mensaje [**LVM \_ DELETEALLITEMS**](lvm-deleteallitems.md) .

### <a name="list-view-item-states"></a>List-View Estados de elemento

El estado de un elemento es un valor que especifica la disponibilidad del elemento, indica las acciones del usuario o, de lo contrario, refleja el estado del elemento. Un control de vista de lista cambia algunos bits de estado, como cuando el usuario selecciona un elemento. Una aplicación podría cambiar otros bits de estado para deshabilitar u ocultar el elemento o especificar una imagen de superposición o imagen de estado. Para obtener más información sobre las imágenes de superposición y las imágenes de estado, consulte [listas de imágenes de vista de lista](#list-view-image-lists).

El estado de un elemento se especifica mediante el miembro de **Estado** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . Al especificar o cambiar el estado de un elemento, el miembro **stateMask** especifica qué bits de Estado debe cambiar. Puede cambiar el estado de un elemento mediante el mensaje [**LVM \_ SETITEMSTATE**](lvm-setitemstate.md) . Puede especificar el estado de un elemento al crearlo o al cambiar sus atributos mediante el mensaje SETITEM de [**LVM \_**](lvm-setitem.md) . Para determinar el estado actual de un elemento, use el mensaje [**LVM \_ GETITEMSTATE**](lvm-getitemstate.md) o [**LVM \_ GETITEM**](lvm-getitem.md) .

Para establecer la imagen de superposición de un elemento, el miembro **stateMask** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) debe incluir el valor [**\_ OVERLAYMASK de LVIS**](list-view-item-states.md) y el miembro **State** debe incluir el índice basado en uno de la imagen de superposición desplazada a la izquierda 8 bits mediante la macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) . El índice puede ser cero para no especificar ninguna imagen de superposición.

Para establecer la imagen de estado de un elemento, el miembro **stateMask** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) debe incluir el valor [**\_ STATEIMAGEMASK de LVIS**](list-view-item-states.md) y el miembro **State** debe incluir el índice basado en uno de la imagen de estado desplazada a la izquierda 12 bits mediante la macro [**INDEXTOSTATEIMAGEMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask) . El índice puede ser cero para no especificar ninguna imagen de estado.

### <a name="callback-items-and-the-callback-mask"></a>Elementos de devolución de llamada y máscara de devolución de llamada

Para cada uno de sus elementos, un control de vista de lista normalmente almacena el texto de la etiqueta, el índice de la lista de imágenes de los iconos del elemento y un conjunto de marcadores de bits para el estado del elemento. Puede definir los elementos de devolución de llamada o cambiar la máscara de devolución de llamada del control para indicar que la aplicación, en lugar del control, almacena parte o toda esta información. Es posible que desee usar devoluciones de llamada si la aplicación almacena parte de esta información.

Un *elemento de devolución de llamada* de un control de vista de lista es un elemento para el que la aplicación almacena el índice de texto o icono, o ambos. Puede definir los elementos de devolución de llamada cuando envíe el mensaje de [**LVM \_ INSERTITEM**](lvm-insertitem.md) para agregar un elemento al control de vista de lista. Si la aplicación almacena el texto del elemento o subelemento, establezca el miembro **miembros pszText** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) del elemento en **LPSTR \_ TEXTCALLBACK**. Si la aplicación almacena el índice de icono de un elemento, establezca el miembro **iImage** de la estructura **LVITEM** del elemento en **I \_ IMAGECALLBACK**.

La *máscara de devolución de llamada* de un control de vista de lista es un conjunto de marcadores de bits que especifican los Estados del elemento para los que la aplicación, en lugar del control, almacena los datos actuales. La máscara de devolución de llamada se aplica a todos los elementos del control, a diferencia de la designación del elemento de devolución de llamada, que se aplica a un elemento específico. De forma predeterminada, la máscara de devolución de llamada es cero, lo que significa que el control de vista de lista almacena toda la información de estado de los elementos. Después de crear un control de vista de lista e inicializar sus elementos, puede enviar el mensaje [**LVM \_ SETCALLBACKMASK**](lvm-setcallbackmask.md) para cambiar la máscara de devolución de llamada. Para recuperar la máscara de devolución de llamada actual, envíe el mensaje [**LVM \_ GETCALLBACKMASK**](lvm-getcallbackmask.md) .

Cuando un control de vista de lista debe mostrar u ordenar un elemento de vista de lista para el que la aplicación almacena información de devolución de llamada, el control envía el código de notificación [LVN \_ GETDISPINFO](lvn-getdispinfo.md) a la ventana primaria del control. Este mensaje especifica una estructura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) que contiene el tipo de información requerida e identifica el elemento o subelemento que se va a recuperar. La ventana primaria debe procesar LVN \_ GETDISPINFO para proporcionar los datos solicitados.

Si el control de vista de lista detecta un cambio en la información de devolución de llamada de un elemento, como un cambio en el texto, el icono o la información de estado, el control envía un código de notificación [ \_ SETDISPINFO de LVN](lvn-setdispinfo.md) para notificar el cambio.

Si se cambian los atributos de un elemento de devolución de llamada o los bits de estado, se usa el mensaje de [**\_ actualización LVM**](lvm-update.md) para forzar que el control vuelva a dibujar el elemento. Este mensaje también hace que el control organice sus elementos si tiene el estilo [**LVS \_ AutoArrange**](list-view-window-styles.md) . Puede usar el mensaje [**\_ REDRAWITEMS LVM**](lvm-redrawitems.md) para volver a dibujar un intervalo de elementos invalidando las partes correspondientes del área cliente del control de vista de lista.

Mediante el uso eficaz de elementos de devolución de llamada y la máscara de devolución de llamada, puede asegurarse de que cada atributo de elemento se mantiene en un solo lugar. Esto puede simplificar la aplicación, pero el único espacio guardado es la memoria que de otro modo sería necesaria para almacenar etiquetas de elementos y texto de subelemento.

### <a name="list-view-item-position"></a>List-View posición del elemento

Cada elemento de vista de lista tiene una posición y un tamaño, que puede recuperar y establecer mediante mensajes. También puede determinar qué elemento, si existe, está en una posición especificada. La posición de los elementos de vista de lista se especifica en coordenadas de la *vista*, que son coordenadas de cliente desplazadas por la posición de desplazamiento.

Para recuperar y establecer la posición de un elemento, use los mensajes [**\_ GETITEMPOSITION**](lvm-getitemposition.md) y [**LVM \_ SETITEMPOSITION**](lvm-setitemposition.md) de LVM. **LVM \_ GETITEMPOSITION** funciona para todas las vistas, pero el **\_ SETITEMPOSITION de LVM** solo funciona para vistas de iconos y pequeños iconos.

Puede determinar qué elemento, si existe, está en una ubicación determinada mediante el mensaje de [**LVM \_ HITTEST**](lvm-hittest.md) .

Para recuperar el rectángulo delimitador de un elemento de lista o solo para su icono o etiqueta, use el mensaje [**\_ GETITEMRECT de LVM**](lvm-getitemrect.md) .

### <a name="arranging-sorting-and-finding-items"></a>Organizar, ordenar y buscar elementos

Puede usar mensajes de vista de lista para organizar y ordenar los elementos, así como para buscar elementos en función de sus atributos o posiciones. La organización de las reposiciones de los elementos se alinean en una cuadrícula, pero los índices de los elementos no cambian. La ordenación cambia la secuencia de elementos (y sus índices correspondientes) y, a continuación, cambia su posición en consecuencia. Los elementos solo se pueden organizar en vistas de iconos y iconos pequeños, pero se pueden ordenar elementos en cualquier vista. Para buscar elementos, se envían mensajes de vista de lista que especifican la ubicación o la propiedad de un elemento.

Para organizar los elementos, use el mensaje de [**\_ organización del LVM**](lvm-arrange.md) . Puede asegurarse de que los elementos se organizan en todo momento especificando el estilo de ventana [**LVS \_ AutoArrange**](list-view-window-styles.md) .

Para ordenar los elementos, use el mensaje [**\_ SORTITEMS de LVM**](lvm-sortitems.md) . Al ordenar con este mensaje, se especifica una función de devolución de llamada definida por la aplicación a la que llama el control de vista de lista para comparar el orden relativo de dos elementos cualesquiera. El control pasa a la función de comparación los datos de elemento asociados a cada uno de los dos elementos. Los datos del elemento son el valor que se especificó en el miembro **lParam** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) del elemento cuando se insertó en la lista. Al especificar los datos de elemento adecuados y proporcionar una función de comparación adecuada, puede ordenar los elementos por su etiqueta, por cualquier subelemento o por cualquier otra propiedad. Tenga en cuenta que la ordenación de elementos no reordena los subelementos correspondientes. Cuando se reordenan los elementos, se transfieren sus subelementos correspondientes. es decir, las filas enteras se mantienen juntas. Para ordenar las columnas por separado entre sí, desasociando los subelementos de sus elementos, debe volver a generar las columnas después de ordenar mediante [**el \_ SETITEM de LVM**](lvm-setitem.md).

Puede asegurarse de que un control de vista de lista se ordene siempre especificando el estilo de ventana [**LVS \_ SORTASCENDING**](list-view-window-styles.md) o [**LVS \_ SORTDESCENDING**](list-view-window-styles.md) . Los controles con estos estilos usan el texto de la etiqueta de los elementos para ordenarlos en orden ascendente o descendente. No se puede proporcionar una función de comparación al utilizar estos estilos de ventana. Si un control de vista de lista tiene cualquiera de estos estilos, se producirá un error en un mensaje [**\_ INSERTITEM de LVM**](lvm-insertitem.md) si intenta insertar un elemento que tenga **LPSTR \_ TEXTCALLBACK** como miembro **miembros pszText** de su estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .

Puede buscar un elemento de vista de lista con propiedades específicas mediante el mensaje [**\_ FINDITEM LVM**](lvm-finditem.md) . Puede encontrar un elemento de vista de lista que se encuentra en un estado especificado y que tiene una relación especificada con un elemento determinado mediante el mensaje [**\_ GETNEXTITEM de LVM**](lvm-getnextitem.md) . Por ejemplo, puede recuperar el siguiente elemento seleccionado a la derecha de un elemento especificado.

## <a name="list-view-columns"></a>Columnas List-View

Las columnas controlan la manera en que se muestran los elementos y sus subelementos en la vista de informe. Cada columna tiene un título y un ancho y está asociada a un subelemento específico; el subelemento cero es el icono y la etiqueta del elemento. Los atributos de una columna se definen mediante una estructura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) .

Para agregar una columna a un control de vista de lista, use el mensaje [**LVM \_ INSERTCOLUMN**](lvm-insertcolumn.md) . Para eliminar una columna, use el mensaje [**LVM \_ DELETECOLUMN**](lvm-deletecolumn.md) .

> [!Note]  
> La eliminación de la columna cero de un control de vista de lista solo se admite en ComCtl32.dll versión 6 y posteriores. La versión 5 también admite la eliminación de la columna cero, pero solo después de usar [**CCM \_ SETVERSION**](ccm-setversion.md) para establecer la versión en 5 o posterior. Las versiones anteriores a la versión 5 no admiten la eliminación de la columna cero.

 

Puede recuperar y cambiar las propiedades de una columna existente mediante los mensajes [**LVM \_ Getcolumn (**](lvm-getcolumn.md) y [**LVM \_ SETCOLUMN**](lvm-setcolumn.md) . Para recuperar o cambiar el ancho de una columna, use los mensajes [**\_ GETCOLUMNWIDTH**](lvm-getcolumnwidth.md) y [**LVM \_ SETCOLUMNWIDTH**](lvm-setcolumnwidth.md) de LVM.

A menos que se especifique el estilo de ventana [**LVS \_ NOCOLUMNHEADER**](list-view-window-styles.md) , los encabezados de columna aparecen en la vista de informe. El usuario puede hacer clic en un encabezado de columna, lo que hace que se envíe un código de notificación [**\_ COLUMNCLICK de LVN**](lvn-columnclick.md) a la ventana primaria. Normalmente, la ventana primaria ordena el control de vista de lista por la columna especificada cuando se hace clic en él. El usuario también puede arrastrar las guías de columna entre los encabezados para ajustar el tamaño de las columnas.

Los controles de vista de lista pueden mostrar imágenes junto a los títulos de columna. Para implementar esta característica, especifique el valor de **\_ imagen LVCF** y asigne el índice de la imagen al miembro **IImage** en la estructura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) .

Los controles de vista de lista pueden establecer el orden en el que se muestran las columnas. Para implementar esta característica, especifique el valor de **\_ orden LVCF** y asigne el orden de las columnas al miembro **IOrder** en la estructura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) . El orden de las columnas es de base cero y está en orden de izquierda a derecha. Por ejemplo, cero indica la columna situada más a la izquierda.

## <a name="list-view-scroll-position"></a>List-View posición de desplazamiento

A menos que se especifique el estilo de ventana [**LVS \_ noscroll**](list-view-window-styles.md) , se puede desplazar un control de vista de lista para mostrar más elementos de los que caben en el área cliente del control. Puede recuperar la posición de desplazamiento y la información relacionada de un control de vista de lista, desplazar un control de vista de lista en una cantidad especificada o desplazarse por un control de vista de lista para que el elemento de lista especificado esté visible.

En la vista de iconos o en la vista de iconos pequeños, la posición de desplazamiento actual se define en el origen de la *vista*. El origen de la vista es el conjunto de coordenadas, en relación con el área visible del control de vista de lista, que corresponden a las coordenadas de la vista (0,0). Para recuperar el origen de la vista actual, use el mensaje [**\_ GETORIGIN de LVM**](lvm-getorigin.md) . Este mensaje solo se debe usar en la vista icono o pequeño icono. Devuelve un error en la vista de lista o informe.

En la vista de lista o de informe, la posición de desplazamiento actual se define en el *Índice superior*. El índice superior es el índice del primer elemento visible en el control de vista de lista. Para recuperar el índice superior actual, use el [**mensaje \_ GETTOPINDEX de LVM**](lvm-gettopindex.md) . Este mensaje solo devuelve un resultado válido en la vista de lista o informe; devuelve cero en el icono o en la vista de iconos pequeños.

Puede usar el mensaje [**LVM \_ GETVIEWRECT**](lvm-getviewrect.md) para recuperar el rectángulo delimitador de todos los elementos de un control de vista de lista, en relación con el área visible del control.

El mensaje [**LVM \_ GETCOUNTPERPAGE**](lvm-getcountperpage.md) devuelve el número de elementos que caben en una página del control de vista de lista. Este mensaje solo devuelve un resultado válido en las vistas de lista y informe; en las vistas icono y pequeño, devuelve el número total de elementos.

Para desplazar un control de vista de lista en una cantidad específica, utilice el mensaje de [**\_ desplazamiento del LVM**](lvm-scroll.md) . Con el [**mensaje \_ ENSUREVISIBLE de LVM**](lvm-ensurevisible.md) , puede desplazarse por el control de vista de lista, si es necesario, para asegurarse de que un elemento especificado esté visible.

## <a name="list-view-label-editing"></a>Edición de List-View etiqueta

Un control de vista de lista que tiene el estilo de ventana [**LVS \_ EDITLABELS**](list-view-window-styles.md) permite a un usuario editar etiquetas de elementos en su lugar. El usuario comienza a editar haciendo clic en la etiqueta de un elemento que tiene el foco. Como alternativa, una aplicación puede comenzar a editarse automáticamente mediante el mensaje [**LVM \_ EDITLABEL**](lvm-editlabel.md) . El control de vista de lista notifica a la ventana primaria cuando comienza la edición y cuando se cancela o se completa. Cuando se completa la edición, la ventana primaria es responsable de actualizar la etiqueta del elemento, si es necesario.

Cuando comienza la edición de etiquetas, se crea, coloca y Inicializa un [control de edición](edit-controls.md) . Antes de que se muestre, el control de vista de lista envía a su ventana primaria un código de notificación [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) . Si necesita modificar el proceso de edición de etiquetas, puede implementar un controlador para esta notificación.

Uno de los usos de un controlador de notificaciones de [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) es controlar las etiquetas que el usuario puede editar. Para evitar la edición de etiquetas, devuelva un valor distinto de cero. Para personalizar la edición de etiquetas, haga que el controlador de notificación recupere un identificador para el control de edición mediante el envío de un mensaje [**\_ GETEDITCONTROL LVM**](lvm-geteditcontrol.md) al control de vista de lista. Una vez que tenga ese identificador, puede personalizar el control de edición mediante el envío de los mensajes de EM \_ XXX habituales. Por ejemplo, para limitar la cantidad de texto que un usuario puede escribir, envíe un mensaje de [**\_ LIMITTEXT em**](em-limittext.md) a un control de edición. Puede cambiar el texto predeterminado del control de edición con [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta). Incluso puede subclaser el control de edición para interceptar y descartar los caracteres no válidos.

Cuando la edición de etiquetas se cancela o se completa, un control de vista de lista envía a su ventana primaria un código de notificación [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) . El parámetro *lParam* es la dirección de una estructura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . El miembro del **elemento** de esta estructura es una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) cuyo miembro **iItem** identifica el elemento. Si se cancela la edición, el miembro **miembros pszText** de la estructura **LVITEM** es **null**. de lo contrario, **miembros pszText** es la dirección del texto editado. La ventana primaria es responsable de actualizar la etiqueta del elemento si desea conservar la nueva etiqueta.

## <a name="list-view-colors"></a>List-View colores

Una aplicación puede recuperar y establecer tres colores para un control de vista de lista.



| Color                   | Mensajes usados para recuperar y establecer colores                                                             |
|-------------------------|------------------------------------------------------------------------------------------------------|
| Color del texto              | [**LVM \_ GETTEXTCOLOR**](lvm-gettextcolor.md), [ **LVM \_ SETTEXTCOLOR**](lvm-settextcolor.md)         |
| Color de fondo del texto   | [**LVM \_ GETTEXTBKCOLOR**](lvm-gettextbkcolor.md), [ **LVM \_ SETTEXTBKCOLOR**](lvm-settextbkcolor.md) |
| Color de fondo de la ventana | [**LVM \_ GETBKCOLOR**](lvm-getbkcolor.md), [ **LVM \_ SETBKCOLOR**](lvm-setbkcolor.md)                 |



 

Para personalizar la apariencia de un control de vista de lista de forma más significativa, use [nm \_ CUSTOMDRAW (vista de lista)](nm-customdraw-list-view.md) o use los estilos visuales (vea [estilos visuales](themes-overview.md) y [habilitar estilos visuales](cookbook-overview.md)).

## <a name="arranging-list-items-by-group"></a>Organizar elementos de lista por grupo

Las características de agrupación del control de vista de lista permiten agrupar visualmente conjuntos de elementos relacionados lógicamente. Los grupos se pueden crear en función de las propiedades de los elementos, los atributos u otras características. Estos grupos normalmente se separan en la pantalla mediante un encabezado horizontal que contiene el nombre del grupo. En la captura de pantalla siguiente se muestran los elementos agrupados.

![captura de pantalla de un control de vista de lista, con perros en un grupo y gatos en otro grupo](images/lv-groups.png)

La estructura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) se usa para almacenar información sobre un grupo, como el texto del encabezado y del pie de página, el estado actual del grupo, etc. La API de agrupación incluye mensajes que permiten administrar grupos y elementos de grupo mediante la adición de elementos a grupos, la adición de grupos a vistas, la ordenación de elementos de grupo y la consulta de grupos para el tamaño del elemento y otra información. Por ejemplo, puede establecer y recuperar los parámetros de presentación de cada grupo mediante las macros [**ListView \_ SetGroupMetrics**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupmetrics) y [**ListView \_ GetGroupMetrics**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupmetrics) .

La agrupación está disponible en todas las vistas excepto en la vista de lista. No está disponible en los controles que tienen el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) .

Para obtener más información, vea [usar controles List-View](using-list-view-controls.md).

## <a name="insertion-marks"></a>Marcas de inserción

Las marcas de inserción muestran los usuarios en los que se colocarán los elementos arrastrados. Las marcas de inserción se muestran actualmente cuando el usuario arrastra un elemento al menú **Inicio** o a la barra de inicio rápido. La marca de inserción también funciona para las listas que están configuradas para autoorganizar. Cuando un usuario arrastra un elemento a un punto entre otros dos elementos, la marca de inserción muestra la nueva ubicación esperada del elemento. En la captura de pantalla siguiente se muestra una marca de inserción.

![captura de pantalla que muestra una marca de inserción al arrastrar un archivo entre otros dos en un control de vista de lista](images/insertmark.png)

Los elementos de la API de marca de inserción permiten colocar marcas de inserción proporcionando mensajes y marcas que realizan la detección de aciertos, que especifican la ubicación y la apariencia de la marca de inserción por elemento, y la consulta para obtener información sobre el tamaño actual y la apariencia de la marca de inserción.

## <a name="see-also"></a>Vea también

* [Ejemplo de control ListView virtual](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)
