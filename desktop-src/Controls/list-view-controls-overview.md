---
title: Acerca de List-View controles
description: Un control de vista de lista es una ventana que muestra una colección de elementos.
ms.assetid: 163f7778-690c-4166-b0c5-c7be1a03ae98
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 8f97059e607595aa944631c739ef38490ce7287879b77c9f9c8dda9c06103dbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958517"
---
# <a name="about-list-view-controls"></a>Acerca de List-View controles

Consulte el [ejemplo de control ListView virtual](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw).

Un control de vista de lista es una ventana que muestra una colección de elementos. Los controles de vista de lista proporcionan varias maneras de organizar y mostrar elementos y son mucho más flexibles que los [cuadros de lista simples.](list-boxes.md) Por ejemplo, se puede mostrar información adicional sobre cada elemento en columnas a la derecha del icono y la etiqueta.

-   [Estilos y vistas de vista de lista](#list-view-styles-and-views)
    -   [Estilos de List-View extendidos](#extended-list-view-styles)
-   [Estilo List-View virtual](#virtual-list-view-style)
    -   [Crear un control de List-View virtual](#creating-a-virtual-list-view-control)
    -   [Problemas de compatibilidad](#compatibility-issues)
    -   [Control de códigos de notificación List-View control virtual](#handling-virtual-list-view-control-notification-codes)
    -   [Administración de caché](#cache-management)
-   [Áreas de trabajo con vista de lista](#list-view-working-areas)
-   [Listas de imágenes de vista de lista](#list-view-image-lists)
-   [Elementos y subelementos de vista de lista](#list-view-items-and-subitems)
    -   [Estados del elemento List-View](#list-view-item-states)
    -   [Elementos de devolución de llamada y la máscara de devolución de llamada](#callback-items-and-the-callback-mask)
    -   [Posición del elemento List-View](#list-view-item-position)
    -   [Organización, ordenación y búsqueda de elementos](#arranging-sorting-and-finding-items)
-   [Columnas de vista de lista](#list-view-columns)
-   [Posición de desplazamiento de la vista de lista](#list-view-scroll-position)
-   [Edición de etiquetas de vista de lista](#list-view-label-editing)
-   [Colores de vista de lista](#list-view-colors)
-   [Organizar elementos de lista por grupo](#arranging-list-items-by-group)
-   [Marcas de inserción](#insertion-marks)

## <a name="list-view-styles-and-views"></a>List-View y vistas

Los controles de vista de lista pueden mostrar elementos en cinco vistas diferentes. El estilo de ventana del control especifica la vista predeterminada. Los estilos de ventana adicionales especifican la alineación de elementos y características específicas del control. En la tabla siguiente se describen las vistas.



| Nombre de vista             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vista de iconos             | Se especifica mediante el estilo [**de ventana LVS \_ ICON**](list-view-window-styles.md) o pasando **LV VIEW \_ \_ ICON** con el [**mensaje \_ LVM SETVIEW.**](lvm-setview.md) Cada elemento aparece como un icono de tamaño normal debajo del cual figura una etiqueta. El usuario puede arrastrar los elementos a cualquier ubicación de la ventana de vista de lista.                                                                                                                                                                                                                                         |
| Vista de icono pequeño       | Se especifica mediante el estilo [**de ventana LVS \_ SMALLICON**](list-view-window-styles.md) o pasando **LV VIEW \_ \_ SMALLICON** con [**LVM \_ SETVIEW**](lvm-setview.md). Cada elemento aparece como un pequeño icono con la etiqueta a la derecha. El usuario puede arrastrar los elementos a cualquier ubicación.                                                                                                                                                                                                                                                       |
| Vista de lista             | Especificado por el estilo de [**ventana LVS \_ LIST**](list-view-window-styles.md) o pasando **LV VIEW \_ \_ LIST** con [**LVM \_ SETVIEW**](lvm-setview.md). Cada elemento aparece como un icono pequeño con una etiqueta a la derecha. Los elementos se organizan en columnas y el usuario no puede arrastrarlos a una ubicación arbitraria.                                                                                                                                                                                                                               |
| Vista Informe (detalles) | Especificado por el estilo de [**ventana \_ INFORME de LVS**](list-view-window-styles.md) o pasando **LV VIEW \_ \_ DETAILS** con [**LVM \_ SETVIEW**](lvm-setview.md). Cada elemento aparece en su propia línea, con información organizada en columnas. La columna situada más a la izquierda siempre se justifica a la izquierda y contiene el icono pequeño y la etiqueta. Las columnas posteriores contienen subelementos según lo especificado por la aplicación. Cada columna tiene un encabezado , a menos que también especifique el [**estilo de ventana \_ LVS NOCOLUMNHEADER.**](list-view-window-styles.md) |
| Vista de mosaico             | **Versión 6 y posteriores.** Se especifica pasando **LV \_ VIEW \_ TILE** con [**LVM \_ SETVIEW.**](lvm-setview.md) Cada elemento aparece como un icono de tamaño completo con una etiqueta de una o más líneas junto a él.                                                                                                                                                                                                                                                                                                                                                        |



 

Las siguientes capturas de pantalla usan vistas para mostrar diferentes cantidades de información sobre cada una de las siete mascotas. Las vistas muestran cómo puede aparecer la información en Windows Vista. Los estilos visuales del control se han establecido en el tema "Explorer" mediante [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).

En la siguiente captura de pantalla se muestra la vista de detalles.

![captura de pantalla que muestra información en cinco columnas y siete filas](images/lv-detailsview.png)

En la siguiente captura de pantalla se muestra la vista de iconos.

![captura de pantalla que muestra solo el nombre de cada mascota y un icono que indica la especie](images/lv-iconview.png)

En la siguiente captura de pantalla se muestra la vista de lista.

![captura de pantalla que muestra, para cada mascota, un icono grande junto al texto del nombre, la variedad y el precio de la mascota.](images/lv-listview.png)

En la siguiente captura de pantalla se muestra la vista de mosaico.

![vista de mosaico.](images/lv-tileview.png)

Puede cambiar el tipo de vista después de crear un control list-view. Para recuperar y cambiar el estilo de la ventana, use las [**funciones GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) [**y SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) Para determinar los estilos de ventana de la vista actual, use el [**valor LVS \_ TYPEMASK.**](list-view-window-styles.md)

Puede controlar la forma en que los elementos se organizan en la vista de icono o icono pequeño especificando el estilo de ventana [**\_ LVS ALIGNTOP**](list-view-window-styles.md) (valor predeterminado) o [**\_ LVS ALIGNLEFT.**](list-view-window-styles.md)

Puede cambiar la alineación después de crear un control list-view. Para determinar la alineación actual, use el [**valor \_ ALIGNMASK de LVS.**](list-view-window-styles.md)

Los estilos de ventana adicionales proporcionan otras opciones, como si un usuario puede editar etiquetas o seleccionar más de un elemento a la vez. Para obtener una lista completa, vea [Estilos de ventana List-View](list-view-window-styles.md).

### <a name="extended-list-view-styles"></a>Estilos de List-View extendidos

Los estilos de control de vista de lista extendida proporcionan opciones como casillas, barras de desplazamiento planas, líneas de cuadrícula y seguimiento rápido. Para obtener una lista completa, vea [Extended List-View Styles](extended-list-view-styles.md). No tiene acceso a los estilos de vista de lista extendidos de la misma manera que los estilos de ventana estándar. No se usan las [**funciones GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) y [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para realizar cambios de estilo extendidos.

Hay dos mensajes que establecen y recuperan información de estilo extendida, [**LVM \_ SETEXTENDEDLISTVIEWSTYLE**](lvm-setextendedlistviewstyle.md) y [**LVM \_ GETEXTENDEDLISTVIEWSTYLE**](lvm-getextendedlistviewstyle.md). En lugar de enviar los mensajes explícitamente, puede usar las siguientes macros correspondientes: [**ListView \_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle), [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex)y [**ListView \_ GetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle).

## <a name="virtual-list-view-style"></a>Estilo List-View virtual

Una vista de lista virtual es un control list-view que tiene el [**estilo \_ OWNERDATA de LVS.**](list-view-window-styles.md) Este estilo permite al control controlar millones de elementos porque el propietario recibe la carga de administrar los datos de los elementos. Esto le permite usar el control de vista de lista virtual con grandes bases de datos de información, donde ya existen métodos específicos de acceso a datos.

Un control de vista de lista virtual mantiene muy poca información sobre los elementos. Excepto para la selección de elementos y la información de foco, el propietario del control debe administrar toda la información del elemento. Otros procesos solicitan información del elemento al propietario mediante los códigos [de notificación \_ GETDISPINFO de LVN.](lvn-getdispinfo.md)

Dado que este tipo de control de lista está pensado para grandes conjuntos de datos, se recomienda almacenar en caché los datos de elementos solicitados para mejorar el rendimiento de recuperación. La vista de lista proporciona un mecanismo de sugerencias de caché para ayudar a optimizar la memoria caché. La sugerencia se implementa en forma de código de [notificación LVN \_ ODCACHEHINT.](lvn-odcachehint.md)

### <a name="creating-a-virtual-list-view-control"></a>Crear un control de List-View virtual

Los controles de vista de lista virtuales se crean mediante las funciones [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) especificando el estilo de [**ventana LVS \_ OWNERDATA**](list-view-window-styles.md) como parte del *parámetro de función dwStyle.* No se admite el cambio dinámico a y desde **el estilo \_ OWNERDATA de LVS.**

Puede usar el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) en combinación con la mayoría de los demás estilos de ventana, excepto el estilo [**LVS \_ SORTASCENDING**](list-view-window-styles.md) o [**LVS \_ SORTDESCENDING.**](list-view-window-styles.md) Todos los controles de vista de lista virtuales tienen como valor predeterminado [**el estilo LVS \_ AUTOARRANGE.**](list-view-window-styles.md)

Para permitir que los elementos se muestren en la lista, primero debe enviar el mensaje [**LVM \_ SETITEMCOUNT,**](lvm-setitemcount.md) ya sea explícitamente o mediante la macro [**\_ ListView SetItemCountEx.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex)

Los mensajes siguientes no se admiten en el estilo [**LVS \_ OWNERDATA: LVM**](list-view-window-styles.md) [**\_ ENABLEGROUPVIEW**](lvm-enablegroupview.md), [**LVM \_ GETITEMTEXT,**](lvm-getitemtext.md) [**LVM \_ SETTILEINFO**](lvm-settileinfo.md)y [**LVM \_ MAPIDTOINDEX**](lvm-mapidtoindex.md).

### <a name="compatibility-issues"></a>Problemas de compatibilidad

Los cuatro estilos de vista de lista (icono, icono pequeño, lista y vista de informe) admiten [**el estilo \_ OWNERDATA de LVS.**](list-view-window-styles.md) Los controles de vista de lista que tienen **el estilo \_ OWNERDATA de LVS** no almacenan ninguna información específica del elemento. Por lo tanto, las únicas marcas de estado de elemento válidas que puede aplicar a un elemento son [**LVIS \_ SELECTED**](list-view-item-states.md) y [**LVIS \_ FOCUSED**](list-view-item-states.md). No se almacena ninguna otra información de estado. En concreto, el control list-view no mantiene imágenes de estado ni de superposición para cada elemento. Sin embargo, puede hacer que el control list-view consulte a la aplicación estas imágenes enviándole un mensaje [**LVM \_ SETCALLBACKMASK.**](lvm-setcallbackmask.md)

La mayoría de los mensajes de control de vista de lista y las macros asociadas son totalmente compatibles. Sin embargo, algunos mensajes tienen limitaciones o no se admiten cuando se usa el estilo [**\_ OWNERDATA de LVS.**](list-view-window-styles.md) En la tabla siguiente se resumen los mensajes afectados.



| Message                                             | Limitación                                                                                                                                                                                                                                                      |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LVM \_ ARRANGE**](lvm-arrange.md)                 | No admite el estilo **LVA \_ SNAPTOGRID.**                                                                                                                                                                                                                 |
| [**LVM \_ DELETEALLITEMS**](lvm-deleteallitems.md)   | Establece el recuento de elementos en cero y borra todas las variables de selección internas, pero realmente no elimina ningún elemento. Realiza una devolución de llamada de notificación.                                                                                                           |
| [**LVM \_ DELETEITEM**](lvm-deleteitem.md)           | Solo se admite para la integridad de selección y no elimina realmente un elemento.                                                                                                                                                                                 |
| [**LVM \_ GETITEMSTATE**](lvm-getitemstate.md)       | Devuelve solo los estados de selección y de foco (es decir, los estados almacenados por el control de vista de lista).                                                                                                                                                                |
| [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md)         | No admite los criterios de búsqueda de vista de lista **LVNI \_ CUT,** **LVNI \_ HIDDEN** o **LVNI \_ DROPHILITED.** Se admiten todos los demás criterios.                                                                                                                     |
| [**LVM \_ GETWORKAREAS**](lvm-getworkareas.md)       | No se admite.                                                                                                                                                                                                                                               |
| [**LVM \_ INSERTITEM**](lvm-insertitem.md)           | Solo se admite para la integridad de selección.                                                                                                                                                                                                                      |
| [**LVM \_ SETITEM**](lvm-setitem.md)                 | No se admite. Para establecer el estado del elemento, use el [**mensaje ListView \_ SetItemState.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate)                                                                                                                                               |
| [**LVM \_ SETITEMCOUNT**](lvm-setitemcount.md)       | Establece el número de elementos que hay actualmente en la lista. Si el control de vista de lista envía una notificación que solicita datos para cualquier elemento hasta el máximo establecido, el propietario debe estar preparado para proporcionar los datos. Los parámetros del mensaje admiten controles de vista de lista virtual. |
| [**LVM \_ SETITEMPOSITION**](lvm-setitemposition.md) | No se admite.                                                                                                                                                                                                                                               |
| [**LVM \_ SETITEMSTATE**](lvm-setitemstate.md)       | Permite cambiar solo los estados de selección y foco para el elemento.                                                                                                                                                                                          |
| [**LVM \_ SETITEMTEXT**](lvm-setitemtext.md)         | No se admite. Es responsabilidad de la aplicación mantener los textos de los elementos.                                                                                                                                                                            |
| [**LVM \_ SETWORKAREAS**](lvm-setworkareas.md)       | No se admite.                                                                                                                                                                                                                                               |
| [**LVM \_ SORTITEMS**](lvm-sortitems.md)             | No se admite. Es responsabilidad de la aplicación presentar los elementos en el orden deseado.                                                                                                                                                             |



 

### <a name="handling-virtual-list-view-control-notification-codes"></a>Control de códigos de notificación List-View control virtual

Los controles de vista de lista con el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) envían los mismos códigos de notificación que otros controles de vista de lista y dos controles adicionales: [LVN \_ ODCACHEHINT](lvn-odcachehint.md) y [LVN \_ ODFINDITEM](lvn-odfinditem.md). A continuación se presentan las notificaciones más comunes que envía el control list-view con **el estilo \_ OWNERDATA de LVS.**



|      Notificación                    |     Descripción                         |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LVN \_ GETDISPINFO](lvn-getdispinfo.md) | Un control de vista de lista virtual mantiene muy poca información de elementos por sí mismo. Como resultado, a menudo envía el código [de notificación \_ GETDISPINFO de LVN](lvn-getdispinfo.md) para solicitar información del elemento. Este mensaje se controla de la misma manera que los elementos de devolución de llamada en un control de lista estándar. Dado que el número de elementos admitidos por el control puede ser muy grande, el almacenamiento en caché de los datos de los elementos mejora el rendimiento. Al controlar LVN GETDISPINFO, el propietario del control intenta primero proporcionar la información de elemento solicitada de la memoria caché (para obtener más información, vea Administración de \_ [caché).](#cache-management) Si el elemento solicitado no se almacena en caché, el propietario debe estar preparado para proporcionar la información por otros medios. |
| [LVN \_ ODCACHEHINT](lvn-odcachehint.md) | Una vista de lista virtual envía el [código de notificación \_ LVN ODCACHEHINT](lvn-odcachehint.md) para ayudar a optimizar la memoria caché. El código de notificación proporciona valores de índice inclusivos para un intervalo de elementos que recomienda almacenar en caché. Tras recibir el código de notificación, el propietario debe estar preparado para cargar la memoria caché con información de elementos para el intervalo solicitado, de modo que la información esté disponible fácilmente cuando se envíe un mensaje [ \_ GETDISPINFO de LVN.](lvn-getdispinfo.md)                                                                                                                                                                                                                                   |
| [LVN \_ ODFINDITEM](lvn-odfinditem.md)   | Un control de vista de lista virtual envía el código de notificación [LVN \_ ODFINDITEM](lvn-odfinditem.md) cuando el control necesita que el propietario encuentre un elemento de devolución de llamada determinado. El código de notificación se envía cuando el control list-view recibe acceso rápido a la clave o cuando recibe un [**mensaje \_ LVM FINDITEM.**](lvm-finditem.md) La información de búsqueda se envía en forma de [**una estructura LVFINDINFO,**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) que es miembro de la estructura [**NMLVFINDITEM.**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) El propietario debe estar preparado para buscar un elemento que coincida con la información que proporciona el control list-view. El propietario devuelve el índice del elemento si se realiza correctamente o -1 si no se encuentra ningún elemento correspondiente.               |



 

### <a name="cache-management"></a>Administración de caché

Un control de vista de lista con el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) genera un gran número de códigos de notificación [ \_ GETDISPINFO](lvn-getdispinfo.md) de LVN y, para ayudar a optimizar la memoria caché, un mensaje [LVN \_ ODCACHEHINT.](lvn-odcachehint.md) Los mensajes \_ de LVN ODCACHEHINT proporcionan información sobre los elementos recomendados que se deben incluir en la memoria caché. Estos mensajes se envían como [**mensajes \_ WM NOTIFY,**](wm-notify.md) con el valor *lParam* que actúa como la dirección de una [**estructura NMLVCACHEHINT.**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint)

La [**estructura NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) incluye dos miembros enteros, **iFrom** e **iTo**, que representan los puntos de conexión inclusivos de un intervalo de elementos que probablemente se necesiten. El propietario debe estar preparado para cargar la memoria caché con la información del elemento para cada uno de los elementos dentro del intervalo recomendado.

El control de lista a menudo necesita información del elemento para el primer elemento (desplazamiento 0). Es [posible que el código de notificación \_ LVN ODCACHEHINT](lvn-odcachehint.md) no incluya siempre el elemento 0, pero siempre debe incluirse en la memoria caché.

A menudo se accede a los últimos elementos de la lista. Por lo tanto, es posible que el propietario quiera mantener una segunda caché que incluya los elementos al final de la lista. El intervalo solicitado de [LVN \_ ODCACHEHINT](lvn-odcachehint.md) se puede comprobar en la caché final para que esté disponible automáticamente en lugar de volver a cargar el mismo intervalo final cada vez.

## <a name="list-view-working-areas"></a>List-View áreas de trabajo

Los controles de vista de lista admiten áreas de trabajo, que son áreas virtuales rectangulares que el control de vista de lista usa para organizar sus elementos. Un área de trabajo no es una ventana y no puede tener un borde visible. De forma predeterminada, el control list-view no tiene áreas de trabajo. Al crear un área de trabajo, puede crear un borde vacío en la parte izquierda, superior o derecha de los elementos o hacer que se muestre una barra de desplazamiento horizontal cuando normalmente no hubiera uno.

Cuando se crea un área de trabajo, los elementos que se encuentran dentro del área de trabajo se convierten en miembros del área de trabajo. De forma similar, si un elemento se mueve a un área de trabajo, el elemento se convierte en miembro de ese área de trabajo. Si un elemento no se encuentra dentro de ningún área de trabajo, se convierte automáticamente en miembro del primer área de trabajo (índice 0). Para colocar un nuevo elemento dentro de un área de trabajo específica, primero debe crear el elemento y, a continuación, usar el mensaje [**LVM \_ SETITEMPOSITION**](lvm-setitemposition.md) o [**LVM \_ SETITEMPOSITION32**](lvm-setitemposition32.md) para moverlo al área de trabajo deseada.

La siguiente ilustración es un ejemplo de un control de vista de lista que contiene cuatro áreas de trabajo, cada una en un cuadrante diferente del área de cliente.

![captura de pantalla de un control de vista de lista con un área de trabajo en cada cuadrante del área de cliente](images/working.jpg)

Se pueden usar varias áreas de trabajo para crear áreas diferentes dentro de una vista. Puede crear áreas en una sola vista que tengan significados diferentes. Por ejemplo, una vista de un sistema de archivos podría tener un área para archivos de lectura y escritura y otra área para archivos de solo lectura. El usuario puede clasificar elementos si los coloca en diferentes áreas de trabajo. Si un archivo se mueve al área de solo lectura, se convertirá automáticamente en de solo lectura.

Varias áreas de trabajo pueden formar intersección, pero los elementos que se encuentran dentro de la intersección se convierten en miembros del área con el índice inferior. por lo tanto, es mejor evitar esta situación. Al ordenar varias áreas de trabajo, los elementos se ordenan en comparación con los demás elementos del mismo área de trabajo.

El número de áreas de trabajo se puede recuperar con el mensaje [**\_ GETNUMBEROFWORKAREAS de LVM.**](lvm-getnumberofworkareas.md) Las áreas de trabajo se cambian con el [**mensaje LVM \_ SETWORKAREAS**](lvm-setworkareas.md) y se pueden recuperar con el mensaje [**\_ LVM GETWORKAREAS.**](lvm-getworkareas.md) Ambos mensajes toman la dirección de una matriz de estructuras [**RECT**](/previous-versions//dd162897(v=vs.85)) como *lParam* y el número de estructuras **RECT** como *wParam*. Los **miembros** izquierdo y superior de estas estructuras especifican las coordenadas de la esquina superior  izquierda (el origen) del área de trabajo y los miembros derecho e inferior especifican la esquina inferior derecha del área de trabajo.   Todas las coordenadas están en coordenadas de cliente de la vista de lista. El número máximo de áreas de trabajo permitidas se define mediante el valor **\_ LV MAX \_ WORKAREAS.**

Cambiar el área de trabajo no tiene ningún efecto en los controles de vista de lista que tienen la vista [**LVS \_ LIST**](list-view-window-styles.md) o [**LVS \_ REPORT,**](list-view-window-styles.md) pero las áreas de trabajo se mantendrán cuando se cambie el tipo de vista. Con las [**vistas LVS \_ ICON**](list-view-window-styles.md) y [**LVS \_ SMALLICON,**](list-view-window-styles.md) el área de trabajo se puede modificar para cambiar la forma en que se muestran los elementos. Si el ancho del área de trabajo (derecha a izquierda) es mayor que el ancho del cliente del control, los elementos se ajustarán a ese ancho y se mostrará la barra de desplazamiento horizontal. Hacer que el ancho del área de trabajo sea más estrecho que el ancho del área de cliente del control hace que los elementos se ajusten dentro del área de trabajo y no del área de cliente. Al establecer  **el miembro** izquierdo o superior en un valor positivo, los elementos se muestran a partir del área de trabajo, lo que crea un espacio vacío entre el borde del control y los elementos. También se puede crear un espacio vacío entre el borde derecho del control y los elementos haciendo que el ancho del área de trabajo sea menor que el ancho del cliente del control.

## <a name="list-view-image-lists"></a>List-View de imágenes

De forma predeterminada, un control de vista de lista no muestra imágenes de elementos. Para mostrar imágenes de elementos, debe crear listas de imágenes y asociarlas al control . Un control list-view puede tener tres listas de imágenes:

-   Lista de imágenes que contiene iconos de tamaño completo que se muestran cuando el control está en la vista de iconos.
-   Lista de imágenes que contiene iconos pequeños que se muestran cuando el control está en una vista de icono pequeña, una vista de lista o una vista de informe.
-   Lista de imágenes que contiene imágenes de estado, que se muestran a la izquierda del icono de tamaño completo o pequeño. Puede usar imágenes de estado, como las casillas activadas y desactivadas, para indicar los estados de los elementos definidos por la aplicación. Las imágenes de estado se muestran en la vista de iconos, la vista de iconos pequeños, la vista de lista y la vista de informe.

Las listas de imágenes de iconos pequeños y de tamaño completo también pueden contener imágenes superpuestas, que están diseñadas para dibujarse de forma transparente sobre los iconos de elemento.

Para usar imágenes superpuestas en un control de vista de lista:

1.  Llame a [**la función ImageList \_ SetOverlayImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) para asignar un índice de imagen superpuesta a una imagen en las listas de imágenes de iconos pequeños y de tamaño completo. Una imagen superpuesta se identifica mediante un índice basado en uno.
2.  Puede asociar un índice de imagen superpuesta a un elemento al llamar a la macro [**\_ ListView InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) o [**ListView \_ SetItem.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) Use la [**macro INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) para especificar  un índice de imagen superpuesta en el miembro de estado de la estructura [**LVITEM del**](/windows/win32/api/commctrl/ns-commctrl-lvitema) elemento. También debe establecer los bits [**\_ OVERLAYMASK de LVIS**](list-view-item-states.md) en el **miembro stateMask.**

Si se especifica una lista de imágenes de estado, un control de vista de lista reserva espacio a la izquierda del icono de cada elemento para una imagen de estado.

Para asociar una imagen de estado a un elemento, use la macro [**INDEXTOSTATEIMAGEMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask) para especificar un índice de imagen de estado en el miembro de estado de la [**estructura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema)  El índice identifica una imagen en la lista de imágenes de estado del control. Aunque los índices de lista de imágenes están basados en cero, el control usa índices basados en uno para identificar imágenes de estado. Un índice de imagen de estado de cero indica que un elemento no tiene ninguna imagen de estado.

De forma predeterminada, cuando se destruye un control de vista de lista, destruye las listas de imágenes asignadas a él. Sin embargo, si un control de vista de lista tiene el estilo de ventana [**LVS \_ SHAREIMAGELISTS,**](list-view-window-styles.md) la aplicación es responsable de destruir las listas de imágenes cuando ya no están en uso. Debe especificar este estilo si asigna las mismas listas de imágenes a varios controles de vista de lista. De lo contrario, más de un control podría intentar destruir la misma lista de imágenes.

## <a name="list-view-items-and-subitems"></a>List-View elementos y subelementos

Cada elemento de un control de vista de lista tiene un icono, una etiqueta, un estado actual y un valor definido por la aplicación. Mediante el uso de mensajes de vista de lista, puede agregar, modificar y eliminar elementos, así como recuperar información sobre los elementos.

Cada elemento puede tener uno o varios *subelementos*. Un subelemento es una cadena que, en la vista de informe, se muestra en una columna independiente del icono y la etiqueta del elemento. Para especificar el texto de un subelemento, use el [**mensaje LVM \_ SETITEMTEXT**](lvm-setitemtext.md) [**o LVM \_ SETITEM.**](lvm-setitem.md) Todos los elementos de un control de vista de lista tienen el mismo número de subelementos. El número de subelementos viene determinado por el número de columnas del control de vista de lista. Cuando se agrega una columna a un control de vista de lista, se especifica su índice de subelemento asociado.

La [**estructura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) define un elemento o subelemento de vista de lista. El **miembro iItem** es el índice de base cero del elemento. El **miembro iSubItem** es el índice basado en uno de un subelemento o cero si la estructura contiene información sobre un elemento. Los miembros adicionales especifican el texto, el icono, el estado y los datos del elemento. *Los datos del* elemento son un valor definido por la aplicación asociado a un elemento de vista de lista.

Para agregar un elemento a un control de vista de lista, use el mensaje [**\_ LVM INSERTITEM**](lvm-insertitem.md) y especifique la dirección de una [**estructura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) Antes de agregar varios elementos, puede enviar al control un mensaje [**LVM \_ SETITEMCOUNT,**](lvm-setitemcount.md) especificando el número de elementos que el control contendrá en última instancia. Este mensaje permite que el control de vista de lista reasigne sus estructuras de datos internas solo una vez en lugar de cada vez que agregue un elemento. Puede determinar el número de elementos de un control de vista de lista mediante el mensaje [**\_ LVM GETITEMCOUNT.**](lvm-getitemcount.md) Si va a agregar un gran número de elementos a un control de vista de lista, puede acelerar el proceso deshabilitando volver a dibujar antes de agregar los elementos y, a continuación, habilitar el nuevo dibujo después de agregar los elementos. Use el [**mensaje WM \_ SETREDRAW**](/windows/desktop/gdi/wm-setredraw) para habilitar y deshabilitar el nuevo dibujo.

Para cambiar los atributos de un elemento de vista de lista, use el mensaje [**LVM \_ SETITEM**](lvm-setitem.md) y especifique la dirección de una [**estructura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) El **miembro mask** de esta estructura especifica los atributos de elemento que desea cambiar. Por ejemplo, para cambiar solo el texto de un elemento o subelemento, use el mensaje [**\_ LVM SETITEMTEXT.**](lvm-setitemtext.md)

Para recuperar información sobre un elemento de vista de lista, use el mensaje [**\_ LVM GETITEM,**](lvm-getitem.md) especificando la dirección de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que se rellenará. El **miembro mask** de esta estructura especifica los atributos de elemento que se recuperarán. Para recuperar solo el texto de un elemento o subelemento, use el [**mensaje \_ LVM GETITEMTEXT.**](lvm-getitemtext.md)

Para eliminar un elemento de vista de lista, use [**el mensaje \_ LVM DELETEITEM.**](lvm-deleteitem.md) Puede eliminar todos los elementos de un control de vista de lista mediante el mensaje [**\_ LVM DELETEALLITEMS.**](lvm-deleteallitems.md)

### <a name="list-view-item-states"></a>List-View de elementos

El estado de un elemento es un valor que especifica la disponibilidad del elemento, indica las acciones del usuario o, de lo contrario, refleja el estado del elemento. Un control de vista de lista cambia algunos bits de estado, como cuando el usuario selecciona un elemento. Una aplicación puede cambiar otros bits de estado para deshabilitar u ocultar el elemento o para especificar una imagen superpuesta o una imagen de estado. Para obtener más información sobre las imágenes superpuestas y las imágenes de estado, vea [List-View Image Lists](#list-view-image-lists).

El miembro de estado de  la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) especifica el estado de un elemento. Al especificar o cambiar el estado de un elemento, el **miembro stateMask** especifica qué bits de estado debe cambiar. Puede cambiar el estado de un elemento mediante el mensaje [**LVM \_ SETITEMSTATE.**](lvm-setitemstate.md) Puede especificar el estado de un elemento al crearlo o al cambiar sus atributos mediante el mensaje [**\_ LVM SETITEM.**](lvm-setitem.md) Para determinar el estado actual de un elemento, use el [**mensaje LVM \_ GETITEMSTATE**](lvm-getitemstate.md) o [**LVM \_ GETITEM.**](lvm-getitem.md)

Para establecer la imagen de superposición de un elemento, el miembro  **stateMask** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) debe incluir el valor [**LVIS \_ OVERLAYMASK**](list-view-item-states.md) y el miembro de estado debe incluir el índice basado en uno de la imagen superpuesta desplazando 8 bits a la izquierda mediante la macro [**INDEXTOOVERLAYMASK.**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) El índice puede ser cero para no especificar ninguna imagen superpuesta.

Para establecer la imagen de estado de un elemento, el miembro **stateMask** de la estructura  [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) debe incluir el valor [**LVIS \_ STATEIMAGEMASK**](list-view-item-states.md) y el miembro de estado debe incluir el índice basado en uno de la imagen de estado desplazado 12 bits a la izquierda mediante la macro [**INDEXTOSTATEIMAGEMASK.**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask) El índice puede ser cero para no especificar ninguna imagen de estado.

### <a name="callback-items-and-the-callback-mask"></a>Elementos de devolución de llamada y máscara de devolución de llamada

Para cada uno de sus elementos, un control de vista de lista almacena normalmente el texto de la etiqueta, el índice de la lista de imágenes de los iconos del elemento y un conjunto de marcas de bits para el estado del elemento. Puede definir elementos de devolución de llamada o cambiar la máscara de devolución de llamada del control para indicar que la aplicación, en lugar del control , almacena parte o toda esta información. Es posible que quiera usar devoluciones de llamada si la aplicación almacena parte de esta información.

Un *elemento de devolución de* llamada en un control de vista de lista es un elemento para el que la aplicación almacena el índice de texto o icono, o ambos. Puede definir elementos de devolución de llamada al enviar el [**mensaje \_ LVM INSERTITEM**](lvm-insertitem.md) para agregar un elemento al control de vista de lista. Si la aplicación almacena el texto del elemento o subelemento, establezca el miembro **pszText** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) del elemento en **LPSTR \_ TEXTCALLBACK**. Si la aplicación almacena el índice de icono de un elemento, establezca el miembro **iImage** de la estructura **LVITEM** del elemento en **I \_ IMAGECALLBACK**.

La *máscara de devolución* de llamada de un control de vista de lista es un conjunto de marcas de bits que especifican los estados de elemento para los que la aplicación, en lugar del control , almacena los datos actuales. La máscara de devolución de llamada se aplica a todos los elementos del control, a diferencia de la designación del elemento de devolución de llamada, que se aplica a un elemento específico. La máscara de devolución de llamada es cero de forma predeterminada, lo que significa que el control de vista de lista almacena toda la información de estado del elemento. Después de crear un control de vista de lista e inicializar sus elementos, puede enviar el mensaje [**LVM \_ SETCALLBACKMASK**](lvm-setcallbackmask.md) para cambiar la máscara de devolución de llamada. Para recuperar la máscara de devolución de llamada actual, envíe el [**mensaje \_ LVM GETCALLBACKMASK.**](lvm-getcallbackmask.md)

Cuando un control de vista de lista debe mostrar u ordenar un elemento de vista de lista para el que la aplicación almacena información de devolución de llamada, el control envía el código de notificación [ \_ LVN GETDISPINFO](lvn-getdispinfo.md) a la ventana primaria del control. Este mensaje especifica una estructura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) que contiene el tipo de información necesaria e identifica el elemento o subelemento que se va a recuperar. La ventana primaria debe procesar LVN \_ GETDISPINFO para proporcionar los datos solicitados.

Si el control de vista de lista detecta un cambio en la información de devolución de llamada de un elemento, como un cambio en la información de texto, icono o estado, el control envía un código de notificación [ \_ LVN SETDISPINFO](lvn-setdispinfo.md) para notificarle del cambio.

Si cambia los atributos o bits de estado de un elemento de devolución de llamada, use el mensaje [**\_ LVM UPDATE**](lvm-update.md) para forzar que el control vuelva a dibujar el elemento. Este mensaje también hace que el control organice sus elementos si tiene el estilo [**LVS \_ AUTOARRANGE.**](list-view-window-styles.md) Puede usar el [**mensaje LVM \_ REDRAWITEMS**](lvm-redrawitems.md) para volver a dibujar un intervalo de elementos invalidando las partes correspondientes del área de cliente del control de vista de lista.

Mediante el uso eficaz de elementos de devolución de llamada y la máscara de devolución de llamada, puede asegurarse de que cada atributo de elemento se mantiene en un solo lugar. Esto puede simplificar la aplicación, pero el único espacio guardado es la memoria que, de lo contrario, sería necesaria para almacenar etiquetas de elementos y texto de subelementos.

### <a name="list-view-item-position"></a>List-View posición del elemento

Cada elemento de vista de lista tiene una posición y un tamaño, que puede recuperar y establecer mediante mensajes. También puede determinar qué elemento, si existe, está en una posición especificada. La posición de los elementos de vista de lista se especifica en las *coordenadas de vista*, que son coordenadas de cliente desplazadas por la posición de desplazamiento.

Para recuperar y establecer la posición de un elemento, use los mensajes [**LVM \_ GETITEMPOSITION**](lvm-getitemposition.md) y [**LVM \_ SETITEMPOSITION.**](lvm-setitemposition.md) **LVM \_ GETITEMPOSITION funciona para** todas las vistas, pero **LVM \_ SETITEMPOSITION** solo funciona para vistas de icono y de icono pequeño.

Puede determinar qué elemento, si existe, se encuentra en una ubicación determinada mediante el mensaje [**LVM \_ HITTEST.**](lvm-hittest.md)

Para recuperar el rectángulo delimitador de un elemento de lista o solo para su icono o etiqueta, use el mensaje [**\_ LVM GETITEMRECT.**](lvm-getitemrect.md)

### <a name="arranging-sorting-and-finding-items"></a>Organizar, ordenar y buscar elementos

Puede usar mensajes de vista de lista para organizar y ordenar elementos y para buscar elementos en función de sus atributos o posiciones. Organizar los elementos de posición para alinearlos en una cuadrícula, pero los índices de los elementos no cambian. La ordenación cambia la secuencia de elementos (y sus índices correspondientes) y, a continuación, los cambia de posición en consecuencia. Solo puede organizar elementos en vistas de icono y de icono pequeño, pero puede ordenar elementos en cualquier vista. Para buscar elementos, envíe mensajes de vista de lista que especifiquen una propiedad o ubicación de elemento.

Para organizar los elementos, use el [**mensaje LVM \_ ARRANGE.**](lvm-arrange.md) Puede asegurarse de que los elementos se organizan en todo momento especificando el estilo de [**ventana LVS \_ AUTOARRANGE.**](list-view-window-styles.md)

Para ordenar elementos, use el [**mensaje \_ LVM SORTITEMS.**](lvm-sortitems.md) Al ordenar con este mensaje, se especifica una función de devolución de llamada definida por la aplicación a la que llama el control list-view para comparar el orden relativo de dos elementos. El control pasa a la función de comparación los datos de elemento asociados a cada uno de los dos elementos. Los datos del elemento son el valor que se especificó en el **miembro lParam** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) del elemento cuando se insertó en la lista. Al especificar los datos de elemento adecuados y proporcionar una función de comparación adecuada, puede ordenar los elementos por su etiqueta, por cualquier subelemento o por cualquier otra propiedad. Tenga en cuenta que la ordenación de elementos no reordena los subelementos correspondientes. Cuando se reordenan los elementos, sus subelementos correspondientes se llevan con ellos; es decir, las filas completas se mantienen juntas. Para ordenar las columnas por separado entre sí, desasoyendo los subelementos de sus elementos, debe volver a generar las columnas después de ordenar mediante [**LVM \_ SETITEM**](lvm-setitem.md).

Puede asegurarse de que un control de vista de lista siempre está ordenado especificando el estilo de ventana [**LVS \_ SORTASCENDING**](list-view-window-styles.md) o [**LVS \_ SORTDESCENDING.**](list-view-window-styles.md) Los controles con estos estilos usan el texto de etiqueta de los elementos para ordenarlos en orden ascendente o descendente. No se puede proporcionar una función de comparación cuando se usan estos estilos de ventana. Si un control de vista de lista tiene cualquiera de estos estilos, se producirá un error en un mensaje [**\_ LVM INSERTITEM**](lvm-insertitem.md) si intenta insertar un elemento que tenga **LPSTR \_ TEXTCALLBACK** como miembro **pszText** de su estructura [**LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema)

Puede encontrar un elemento de vista de lista con propiedades específicas mediante el mensaje [**\_ LVM FINDITEM.**](lvm-finditem.md) Puede encontrar un elemento de vista de lista que se encuentra en un estado especificado y tiene una relación especificada con un elemento determinado mediante el mensaje [**\_ LVM GETNEXTITEM.**](lvm-getnextitem.md) Por ejemplo, puede recuperar el siguiente elemento seleccionado a la derecha de un elemento especificado.

## <a name="list-view-columns"></a>List-View columnas

Las columnas controlan la forma en que los elementos y sus subelementos se muestran en la vista de informe. Cada columna tiene un título y un ancho y está asociada a un subelemento específico; El subelemento cero es el icono y la etiqueta del elemento. Los atributos de una columna se definen mediante una [**estructura LVCOLUMN.**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna)

Para agregar una columna a un control de vista de lista, use el [**mensaje \_ LVM INSERTCOLUMN.**](lvm-insertcolumn.md) Para eliminar una columna, use el [**mensaje LVM \_ DELETECOLUMN.**](lvm-deletecolumn.md)

> [!Note]  
> La eliminación de la columna cero de un control de vista de lista solo se admite ComCtl32.dll versión 6 y posteriores. La versión 5 también admite la eliminación de la columna cero, pero solo después de usar [**CCM \_ SETVERSION**](ccm-setversion.md) para establecer la versión en 5 o posterior. Las versiones anteriores a la versión 5 no admiten la eliminación de la columna cero.

 

Puede recuperar y cambiar las propiedades de una columna existente mediante los mensajes [**LVM \_ GETCOLUMN**](lvm-getcolumn.md) y [**LVM \_ SETCOLUMN.**](lvm-setcolumn.md) Para recuperar o cambiar el ancho de una columna, use los mensajes [**LVM \_ GETCOLUMNWIDTH**](lvm-getcolumnwidth.md) y [**LVM \_ SETCOLUMNWIDTH.**](lvm-setcolumnwidth.md)

A menos [**que se especifique el estilo de ventana \_ LVS NOCOLUMNHEADER,**](list-view-window-styles.md) los encabezados de columna aparecen en la vista de informe. El usuario puede hacer clic en un encabezado de columna, lo que hace que se envíe un código de [**notificación \_ LVN COLUMNCLICK**](lvn-columnclick.md) a la ventana primaria. Normalmente, la ventana primaria ordena el control de vista de lista por la columna especificada cuando se produce este clic. El usuario también puede arrastrar las guías de columna entre los encabezados para cambiar el tamaño de las columnas.

Los controles de vista de lista pueden mostrar imágenes junto a los títulos de columna. Para implementar esta característica, especifique el valor **LVCF \_ IMAGE** y asigne el índice de la imagen al **miembro iImage** en la [**estructura LVCOLUMN.**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna)

Los controles de vista de lista pueden establecer el orden en el que se muestran las columnas. Para implementar esta característica, especifique el valor **LVCF \_ ORDER** y asigne el orden de columna al **miembro iOrder** en la [**estructura LVCOLUMN.**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) El orden de las columnas es de base cero y está en orden de izquierda a derecha. Por ejemplo, cero indica la columna situada más a la izquierda.

## <a name="list-view-scroll-position"></a>List-View posición de desplazamiento

A menos que se especifique el estilo de [**\_ ventana LVS NOSCROLL,**](list-view-window-styles.md) se puede desplazar un control de vista de lista para mostrar más elementos de los que caben en el área cliente del control. Puede recuperar la posición de desplazamiento de un control de vista de lista y la información relacionada, desplazar un control de vista de lista por una cantidad especificada o desplazarse por un control de vista de lista para que un elemento de lista especificado esté visible.

En la vista de iconos o en la vista de icono pequeño, la posición de desplazamiento actual se define mediante el *origen de la vista.* El origen de la vista es el conjunto de coordenadas, en relación con el área visible del control list-view, que se corresponden con las coordenadas de vista (0, 0). Para recuperar el origen de la vista actual, use [**el \_ mensaje LVM GETORIGIN.**](lvm-getorigin.md) Este mensaje solo debe usarse en la vista icono o icono pequeño; devuelve un error en la vista de lista o informe.

En la vista de lista o informe, la posición de desplazamiento actual se define mediante el *índice superior*. El índice superior es el índice del primer elemento visible en el control list-view. Para recuperar el índice superior actual, use el [**mensaje \_ LVM GETTOPINDEX.**](lvm-gettopindex.md) Este mensaje devuelve un resultado válido solo en la vista de lista o informe; devuelve cero en la vista icono o icono pequeño.

Puede usar el mensaje [**\_ LVM GETVIEWRECT**](lvm-getviewrect.md) para recuperar el rectángulo delimitador de todos los elementos de un control de vista de lista, en relación con el área visible del control.

El [**mensaje LVM \_ GETCOUNTPERPAGE**](lvm-getcountperpage.md) devuelve el número de elementos que caben en una página del control de vista de lista. Este mensaje devuelve un resultado válido solo en vistas de lista e informe; en las vistas de icono y icono pequeño, devuelve el número total de elementos.

Para desplazar un control de vista de lista por una cantidad específica, use el [**mensaje LVM \_ SCROLL.**](lvm-scroll.md) Con el [**mensaje LVM \_ ENSUREVISIBLE,**](lvm-ensurevisible.md) puede desplazarse por el control de vista de lista, si es necesario, para asegurarse de que un elemento especificado está visible.

## <a name="list-view-label-editing"></a>List-View edición de etiquetas

Un control de vista de lista que tiene el estilo de [**ventana LVS \_ EDITLABELS**](list-view-window-styles.md) permite a un usuario editar etiquetas de elemento en su lugar. El usuario comienza a editar haciendo clic en la etiqueta de un elemento que tiene el foco. Como alternativa, una aplicación puede empezar a editar automáticamente mediante el mensaje [**LVM \_ EDITLABEL.**](lvm-editlabel.md) El control de vista de lista notifica a la ventana primaria cuando comienza la edición y cuando se cancela o se completa. Cuando se completa la edición, la ventana primaria es responsable de actualizar la etiqueta del elemento, si procede.

Cuando comienza la [](edit-controls.md) edición de etiquetas, se crea, coloca e inicializa un control de edición. Antes de que se muestre, el control de vista de lista envía a su ventana primaria un código [de notificación \_ LVN BEGINLABELEDIT.](lvn-beginlabeledit.md) Si necesita modificar el proceso de edición de etiquetas, puede implementar un controlador para esta notificación.

Un uso de un [controlador de notificaciones \_ BEGINLABELEDIT de LVN](lvn-beginlabeledit.md) es controlar qué etiquetas puede editar el usuario. Para evitar la edición de etiquetas, devuelva un valor distinto de cero. Para personalizar la edición de etiquetas, haga que el controlador de notificaciones recupere un identificador al control de edición mediante el envío de un mensaje [**\_ GETEDITCONTROL de LVM**](lvm-geteditcontrol.md) al control de vista de lista. Una vez que tenga ese identificador, puede personalizar el control de edición enviando los mensajes EM \_ XXX habituales. Por ejemplo, para limitar la cantidad de texto que un usuario puede escribir, envíe al control de edición un [**mensaje \_ EM LIMITTEXT.**](em-limittext.md) Puede cambiar el texto predeterminado del control de edición [**con SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta). Incluso puede crear subclases del control de edición para interceptar y descartar caracteres no válidos.

Cuando se cancela o se completa la edición de etiquetas, un control de vista de lista envía a su ventana primaria un código de [notificación \_ LVN ENDLABELEDIT.](lvn-endlabeledit.md) El *parámetro lParam* es la dirección de una [**estructura NMLVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) El **miembro** de elemento de esta estructura es [**una estructura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) cuyo **miembro iItem** identifica el elemento. Si se cancela la edición, el **miembro pszText** de la **estructura LVITEM** es **NULL**; De lo contrario, **pszText** es la dirección del texto editado. La ventana primaria es responsable de actualizar la etiqueta del elemento si desea mantener la nueva etiqueta.

## <a name="list-view-colors"></a>List-View colores

Una aplicación puede recuperar y establecer tres colores para un control de vista de lista.



| Color                   | Mensajes usados para recuperar y establecer colores                                                             |
|-------------------------|------------------------------------------------------------------------------------------------------|
| Color del texto              | [**LVM \_ GETTEXTCOLOR**](lvm-gettextcolor.md), [ **LVM \_ SETTEXTCOLOR**](lvm-settextcolor.md)         |
| Color de fondo del texto   | [**LVM \_ GETTEXTBKCOLOR**](lvm-gettextbkcolor.md), [ **LVM \_ SETTEXTBKCOLOR**](lvm-settextbkcolor.md) |
| Color de fondo de la ventana | [**LVM \_ GETBKCOLOR**](lvm-getbkcolor.md), [ **LVM \_ SETBKCOLOR**](lvm-setbkcolor.md)                 |



 

Para personalizar la apariencia de un control de vista de lista de forma más significativa, use [NM \_ CUSTOMDRAW (vista](nm-customdraw-list-view.md) de lista) o use estilos visuales (vea [Estilos](themes-overview.md) visuales y Habilitar estilos [visuales).](cookbook-overview.md)

## <a name="arranging-list-items-by-group"></a>Organizar elementos de lista por grupo

Las características de agrupación del control list-view permiten agrupar visualmente conjuntos de elementos relacionados lógicamente. Los grupos se pueden crear en función de las propiedades, atributos u otras características del elemento. Estos grupos suelen estar separados en la pantalla por un encabezado horizontal que contiene el nombre del grupo. En la siguiente captura de pantalla se muestran los elementos agrupados.

![captura de pantalla de un control list-view, con perros en un grupo y gatos en otro grupo](images/lv-groups.png)

Use la estructura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) para almacenar información sobre un grupo, como el texto de encabezado y pie de página, el estado actual del grupo, y así sucesivamente. La API de agrupación incluye mensajes que permiten administrar grupos y elementos de grupo mediante la adición de elementos a grupos, la adición de grupos a vistas, la ordenación de elementos de grupo y la consulta de grupos de tamaño de elemento y otra información. Por ejemplo, puede establecer y recuperar parámetros de presentación para cada grupo mediante las macros [**\_ ListView SetGroupMetrics**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupmetrics) y [**ListView \_ GetGroupMetrics.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupmetrics)

La agrupación está disponible en todas las vistas excepto en la vista de lista. No está disponible en los controles que tienen [**el estilo \_ OWNERDATA de LVS.**](list-view-window-styles.md)

Para obtener más información, [vea Usar List-View controles](using-list-view-controls.md).

## <a name="insertion-marks"></a>Marcas de inserción

Las marcas de inserción muestran los usuarios donde se colocarán los elementos arrastrados. Las marcas de inserción se muestran actualmente cuando el usuario arrastra un elemento al menú **Inicio** o a inicio rápido barra. La marca de inserción también funciona para las listas que se establecen en autoarrange. Cuando un usuario arrastra un elemento a un punto entre otros dos elementos, la marca de inserción muestra la nueva ubicación esperada del elemento. En la siguiente captura de pantalla se muestra una marca de inserción.

![captura de pantalla que muestra una marca de inserción al arrastrar un archivo entre otros dos en un control de vista de lista](images/insertmark.png)

Los elementos de la API de marca de inserción permiten la colocación de marcas de inserción proporcionando mensajes y marcas que realizan la detección de llamadas, que especifican la ubicación y la apariencia de la marca de inserción por elemento, y que consultan información sobre el tamaño actual y la apariencia de la marca de inserción.

## <a name="see-also"></a>Consulte también

* [Ejemplo de control listview virtual](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)
