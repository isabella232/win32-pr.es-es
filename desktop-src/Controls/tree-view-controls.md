---
title: Acerca de Tree-View controles
description: Un control de vista de árbol es una ventana que muestra una lista jerárquica de elementos, como los encabezados de un documento, las entradas de un índice o los archivos y directorios de un disco.
ms.assetid: 10cc7949-dd77-412d-bad1-db8d8a049582
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ea08743a7ac138a6cea5f766dd91aee2ec714acc2d4c8b98e1f2bee26c42ff9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769833"
---
# <a name="about-tree-view-controls"></a>Acerca de Tree-View controles

Un control de vista de árbol es una ventana que muestra una lista jerárquica de elementos, como los encabezados de un documento, las entradas de un índice o los archivos y directorios de un disco. Cada elemento consta de una etiqueta y una imagen de mapa de bits opcional, y cada elemento puede tener una lista de subelementos asociados a ella. Al hacer clic en un elemento, el usuario puede expandir o contraer la lista asociada de subelementos.

En la ilustración siguiente se muestra un control simple de vista de árbol con un nodo raíz, un nodo expandido y un nodo contraído. El control usa un mapa de bits para el elemento seleccionado y otro mapa de bits para otros elementos.

![captura de pantalla que muestra cinco nodos en una jerarquía; se selecciona el texto de un nodo, pero los nodos no se vinculan entre sí mediante líneas](images/tv-simple.png)

Después de crear un control de vista de árbol, agregue, quite, organice o manipule elementos mediante el envío de mensajes al control . Cada mensaje tiene una o varias macros correspondientes que puede usar en lugar de enviar el mensaje explícitamente.

En esta sección se tratan los temas siguientes.

-   [Estilos de vista de árbol](#tree-view-styles)
-   [Elementos primarios y secundarios](#parent-and-child-items)
-   [Etiquetas de elementos](#item-labels)
-   [Edición de etiquetas de vista de árbol](#tree-view-label-editing)
-   [Posición del elemento de vista de árbol](#tree-view-item-position)
-   [Información general sobre los estados de los elementos de vista de árbol](#tree-view-item-states-overview)
-   [Selección de elementos](#item-selection)
-   [Información del elemento](#item-information)
-   [Listas de imágenes de vista de árbol](#tree-view-image-lists)
-   [Operaciones de arrastrar y colocar](#drag-and-drop-operations)
-   [Mensajes de notificación de control de vista de árbol](#tree-view-control-notification-messages)
-   [Procesamiento de Tree-View de mensajes de control predeterminado](#default-tree-view-control-message-processing)
-   [Temas relacionados](#related-topics)

## <a name="tree-view-styles"></a>Tree-View estilos

Los estilos de vista de árbol rigen aspectos de la apariencia de un control de vista de árbol. Los estilos iniciales se establecen al crear el control de vista de árbol. Puede recuperar y cambiar los estilos después de crear el control de vista de árbol mediante las funciones [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) [**y SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)

El [**estilo \_ HASLINES**](tree-view-control-window-styles.md) de TVS mejora la representación gráfica de la jerarquía de un control de vista de árbol dibujando líneas que vinculan elementos secundarios a su elemento primario, como se muestra en la ilustración siguiente.

![captura de pantalla que muestra la disposición anterior, pero con líneas que unen los nodos. la primera línea desciende del nodo raíz](images/tv-haslines.png)

Por sí mismo, este estilo no dibuja líneas en la raíz de la jerarquía. Para ello, debe combinar los estilos [**\_ TVS HASLINES**](tree-view-control-window-styles.md) y [**TVS \_ LINESATROOT.**](tree-view-control-window-styles.md) El resultado se muestra en la ilustración siguiente.

![captura de pantalla que muestra la disposición anterior, pero con una línea horizontal adicional que conduce al nodo raíz](images/tv-rootlines.png)

El usuario puede expandir o contraer la lista de elementos secundarios de un elemento primario haciendo doble clic en el elemento primario. Un control de vista de árbol que tiene el [**estilo \_ HASBUTTONS**](tree-view-control-window-styles.md) de TVS agrega un botón al lado izquierdo de cada elemento primario. El usuario puede hacer clic en el botón una vez en lugar de hacer doble clic en el elemento primario para expandir o contraer el elemento secundario. **TVS \_ HASBUTTONS** no agrega botones a los elementos de la raíz de la jerarquía. Para ello, debe combinar [**TVS \_ HASLINES,**](tree-view-control-window-styles.md) [**TVS \_ LINESATROOT**](tree-view-control-window-styles.md)y **TVS \_ HASBUTTONS**. Esta combinación de estilos se muestra en la ilustración siguiente.

![captura de pantalla que muestra la disposición anterior, pero con botones de expandir o contraer en cada vértice de dos líneas](images/tv-hasbuttons.png)

El [**estilo TVS \_ CHECKBOXES**](tree-view-control-window-styles.md) crea casillas junto a cada elemento. Si desea usar el estilo de casilla, debe establecer el estilo **TVS \_ CHECKBOXES** (con [**SetWindowLong)**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)después de crear el control de vista de árbol y antes de rellenar el árbol. De lo contrario, las casillas podrían aparecer desactivadas, dependiendo de los problemas de tiempo. En la ilustración siguiente se muestra el estilo de casilla.

![captura de pantalla que muestra la disposición anterior, pero con una casilla junto a cada nodo; Se seleccionan dos de las casillas](images/tv-haschecks.png)

El [**estilo \_ FULLROWSELECT**](tree-view-control-window-styles.md) de TVS hace que el resaltado de selección se extienda sobre el ancho completo del control, no solo sobre el propio elemento. En la ilustración siguiente se muestra este estilo.

![captura de pantalla que muestra la disposición original de cinco nodos sin líneas, pero el resaltado de selección amplía el ancho completo del control.](images/tv-fullrow.png)

El [**estilo \_ EDITLABELS**](tree-view-control-window-styles.md) de TVS permite al usuario editar las etiquetas de los elementos de vista de árbol. Para obtener más información sobre cómo editar etiquetas, vea [Edición de etiquetas de vista de árbol.](#tree-view-label-editing)

Para obtener más información sobre estos y otros estilos, vea [Tree-View Control Window Styles](tree-view-control-window-styles.md).

## <a name="parent-and-child-items"></a>Elementos primarios y secundarios

Cualquier elemento de un control de vista de árbol puede tener asociada una lista de subelementos, denominados *elementos secundarios.* Un elemento que tiene uno o varios elementos secundarios se denomina *elemento primario*. Un elemento secundario se muestra debajo de su elemento primario y se aplica sangría para indicar que está subordinado al elemento primario. Un elemento que no tiene ningún elemento primario aparece en la parte superior de la jerarquía y se denomina elemento *raíz*.

Para agregar un elemento a un control de vista de árbol, envíe el [**mensaje \_ INSERTITEM**](tvm-insertitem.md) de TVM al control. El mensaje devuelve un identificador al tipo HTREEITEM, que identifica de forma única el elemento. Al agregar un elemento, debe especificar el identificador para el elemento primario del nuevo elemento. Si especifica **NULL o el** valor RAÍZ de TVI en lugar de un identificador de elemento primario en la estructura \_ [**TVINSERTSTRUCT,**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) el elemento se agrega como un elemento raíz.

En un momento dado, el estado de la lista de elementos secundarios de un elemento primario se puede expandir o contraer. Cuando se expande el estado, los elementos secundarios se muestran debajo del elemento primario. Cuando se contrae, no se muestran los elementos secundarios. La lista alterna automáticamente entre los estados expandido y contraído cuando el usuario hace doble clic en el elemento primario o, si el elemento primario tiene el estilo [**\_ HASBUTTONS de TVS,**](tree-view-control-window-styles.md) cuando el usuario hace clic en el botón asociado al elemento primario. Una aplicación puede expandir o contraer los elementos secundarios mediante el [**mensaje \_ EXPAND de TVM.**](tvm-expand.md)

Un control de vista de árbol envía a la ventana primaria un mensaje de notificación [ \_ TVN ITEMEXPANDING](tvn-itemexpanding.md) cuando la lista de elementos secundarios de un elemento primario está a punto de expandirse o contraerse. La notificación ofrece a una aplicación la oportunidad de evitar el cambio o de establecer los atributos del elemento primario que dependen del estado de la lista de elementos secundarios. Después de cambiar el estado de la lista, el control de vista de árbol envía a la ventana primaria un mensaje de [notificación \_ ITEMEXPANDED de TVN.](tvn-itemexpanded.md)

Cuando se expande una lista de elementos secundarios, se aplica sangría al elemento primario. Puede establecer la cantidad de sangría mediante el mensaje [**\_ TVM SETINDENT**](tvm-setindent.md) o recuperar la cantidad actual mediante el mensaje [**\_ GETINDENT de TVM.**](tvm-getindent.md)

Un control de vista de árbol usa la memoria asignada desde el montón del proceso que crea el control de vista de árbol. El número máximo de elementos de una vista de árbol se basa en la cantidad de memoria disponible en el montón.

## <a name="item-labels"></a>Etiquetas de elementos

Normalmente se especifica el texto de la etiqueta de un elemento al agregar el elemento al control de vista de árbol. El [**mensaje \_ INSERTITEM**](tvm-insertitem.md) de TVM incluye una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que define las propiedades del elemento, incluida una cadena que contiene el texto de la etiqueta.

Un control de vista de árbol asigna memoria para almacenar cada elemento; el texto de las etiquetas de elemento ocupa una parte significativa de esta memoria. Si la aplicación mantiene una copia de las cadenas en el control de vista de árbol, puede reducir los requisitos de memoria del control especificando el valor LPSTR TEXTCALLBACK en el miembro \_ **pszText** de [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) en lugar de pasar cadenas reales a la vista de árbol. El uso de LPSTR TEXTCALLBACK hace que el control de vista de árbol recupere el texto de la etiqueta de un elemento de la ventana primaria siempre que sea necesario volver a \_ dibujar el elemento. Para recuperar el texto, el control de vista de árbol envía un mensaje de notificación [ \_ GETDISPINFO de TVN,](tvn-getdispinfo.md) que incluye la dirección de una estructura [**NMTVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) La ventana primaria debe rellenar los miembros adecuados de la estructura incluida.

## <a name="tree-view-label-editing"></a>Tree-View edición de etiquetas

El usuario puede editar directamente las etiquetas de los elementos en un control de vista de árbol que tenga el estilo [**\_ EDITLABELS de TVS.**](tree-view-control-window-styles.md) El usuario comienza a editar haciendo clic en la etiqueta del elemento que tiene el foco. Una aplicación comienza a editar mediante el [**mensaje \_ EDITLABEL de TVM.**](tvm-editlabel.md) El control de vista de árbol notifica a la ventana primaria cuándo comienza la edición y cuándo se cancela o se completa. Cuando se completa la edición, la ventana primaria es responsable de actualizar la etiqueta del elemento, si procede.

Cuando comienza la edición de etiquetas, un control de vista de árbol envía a su ventana primaria un [mensaje de notificación \_ BEGINLABELEDIT de TVN.](tvn-beginlabeledit.md) Al procesar esta notificación, una aplicación puede permitir la edición de algunas etiquetas e impedir la edición de otras. Devolver cero permite la edición y devolver un valor distinto de cero lo impide.

Cuando se cancela o se completa la edición de etiquetas, un control de vista de árbol envía a su ventana primaria un [mensaje de notificación \_ ENDLABELEDIT de TVN.](tvn-endlabeledit.md) El *parámetro lParam* es la dirección de una [**estructura NMTVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) El *parámetro item* es una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que identifica el elemento e incluye el texto editado. La ventana primaria es responsable de actualizar la etiqueta del elemento si desea mantener la nueva etiqueta. El **miembro pszText** de **TVITEM** es cero si se cancela la edición.

Durante la edición de etiquetas, normalmente en respuesta al mensaje de notificación [ \_ BEGINLABELEDIT de TVN,](tvn-beginlabeledit.md) puede recuperar el identificador del control de edición usado para la edición de etiquetas mediante el mensaje [**\_ GETEDITCONTROL de TVM.**](tvm-geteditcontrol.md) Puede enviar al control de edición un mensaje [**EM \_ SETLIMITTEXT**](em-setlimittext.md) para limitar la cantidad de texto que un usuario puede escribir o crear subclases en el control de edición para interceptar y descartar caracteres no válidos. Sin embargo, tenga en cuenta que el control de edición solo se muestra después *de* enviar \_ TVN BEGINLABELEDIT.

## <a name="tree-view-item-position"></a>Tree-View posición del elemento

La posición inicial de un elemento se establece cuando el elemento se agrega al control de vista de árbol mediante el [**mensaje \_ INSERTITEM de TVM.**](tvm-insertitem.md) El mensaje incluye una [**estructura TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) que especifica el identificador del elemento primario y el identificador del elemento después del cual se va a insertar el nuevo elemento. El segundo identificador debe identificar un elemento secundario del elemento primario especificado o uno de estos valores: TVI \_ FIRST, TVI \_ LAST o TVI \_ SORT.

Cuando se especifica TVI FIRST o TVI LAST, el control de vista de árbol coloca el nuevo elemento al principio o al final de la lista de elementos secundarios del elemento \_ \_ primario especificado. Cuando se especifica TVI SORT, el control de vista de árbol inserta el nuevo elemento en la lista de elementos secundarios en orden alfabético según el texto de las \_ etiquetas de elemento.

Puede colocar la lista de elementos secundarios de un elemento primario en orden alfabético mediante el [**mensaje \_ SORTCHILDREN de TVM.**](tvm-sortchildren.md) El mensaje incluye un parámetro que especifica si todos los niveles de elementos secundarios que descienden del elemento primario especificado también se ordenan en orden alfabético.

El [**mensaje \_ TVM SORTCHILDRENCB**](tvm-sortchildrencb.md) permite ordenar elementos secundarios en función de los criterios que defina. Cuando se usa este mensaje, se especifica una función de devolución de llamada definida por la aplicación a la que el control de vista de árbol puede llamar siempre que sea necesario decidir el orden relativo de dos elementos secundarios. La función de devolución de llamada recibe dos valores definidos por la aplicación de 32 bits para los elementos que se comparan y un tercer valor de 32 bits que se especifica al enviar **TVM \_ SORTCHILDRENCB.**

## <a name="tree-view-item-states-overview"></a>Tree-View información general sobre los estados de los elementos

Cada elemento de un control de vista de árbol tiene un estado actual. La información de estado de cada elemento incluye un conjunto de marcas de bits, así como índices de lista de imágenes que indican la imagen de estado del elemento y la imagen de superposición. Las marcas de bits indican si el elemento está seleccionado, deshabilitado, expandido, y así sucesivamente. En su mayor parte, un control de vista de árbol establece automáticamente el estado de un elemento para reflejar las acciones del usuario, como la selección de un elemento. Sin embargo, también puede establecer el estado de un elemento mediante el mensaje [**\_ SETITEM**](tvm-setitem.md) de TVM y puede recuperar el estado actual de un elemento mediante el mensaje [**\_ GETITEM de TVM.**](tvm-getitem.md) Para obtener una lista completa de los estados de los elementos, vea [Tree-View Control Item States](tree-view-control-item-states.md).

El miembro de estado de la  [**estructura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) especifica el estado actual de un elemento. Un control de vista de árbol podría cambiar el estado de un elemento para reflejar una acción del usuario, como seleccionar el elemento o establecer el foco en el elemento. Además, una aplicación puede cambiar el estado de un elemento para deshabilitar u ocultar el elemento o para especificar una imagen de superposición o una imagen de estado.

Al especificar o cambiar el estado  de un elemento, el miembro de máscara de  estado de [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) especifica qué bits de estado se deben establecer y el miembro de estado contiene los nuevos valores para esos bits.

Para establecer la imagen superpuesta de un **elemento,** la máscara de  estado debe incluir el valor [**\_ OVERLAYMASK**](tree-view-control-item-states.md) de TVIS y el estado debe incluir el índice basado en uno de la imagen de superposición desplazado a la izquierda 8 bits mediante la macro [**INDEXTOOVERLAYMASK.**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) El índice puede ser cero para no especificar ninguna imagen superpuesta.

Se muestra una imagen de estado junto al icono de un elemento para indicar un estado definido por la aplicación. Las imágenes de estado se incluyen en una *lista de* imágenes de estado que se especifica mediante el envío de un mensaje [**\_ SETIMAGELIST de TVM.**](tvm-setimagelist.md) Para establecer la imagen de estado de un elemento, incluya el valor [**DE TVIS \_ STATEIMAGEMASK**](tree-view-control-item-states.md) en el miembro **statemask** de la [**estructura TVITEM.**](/windows/win32/api/commctrl/ns-commctrl-tvitema) Los bits del 12 al 15 del miembro de estado de la estructura especifican el índice en la lista de imágenes de estado de la imagen que se va a dibujar. 

Para establecer el índice de imagen de estado, use [**INDEXTOSTATEIMAGEMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask). Esta macro toma un índice y establece los bits de 12 a 15 correctamente. Para indicar que el elemento no tiene ninguna imagen de estado, establezca el índice en cero. Esta convención significa que la imagen cero de la lista de imágenes de estado no se puede usar como imagen de estado. Para aislar los bits del 12 al 15 del miembro **de** estado, use la máscara [**\_ TVIS STATEIMAGEMASK.**](tree-view-control-item-states.md) Para obtener más información sobre las imágenes de superposición y de estado, vea [Tree-View Image Lists](#tree-view-image-lists).

## <a name="item-selection"></a>Selección de elementos

Un control de vista de árbol notifica a la ventana primaria cuando la selección cambia de un elemento a otro mediante el envío de los mensajes de notificación [TVN \_ SELCHANGING](tvn-selchanging.md) y [TVN \_ SELCHANGED.](tvn-selchanged.md) Ambas notificaciones incluyen un valor que especifica si el cambio es el resultado de un clic del mouse o una pulsación de tecla. Las notificaciones también incluyen información sobre el elemento que obtiene la selección y el elemento que pierde la selección. Puede usar esta información para establecer atributos de elemento que dependen del estado de selección del elemento. Devolver **TRUE** en respuesta a TVN SELCHANGING impide que la selección cambie \_ y devolver **FALSE** permite el cambio.

Una aplicación puede cambiar la selección mediante el envío del [**mensaje \_ SELECTITEM de TVM.**](tvm-selectitem.md)

## <a name="item-information"></a>Información del elemento

Los controles de vista de árbol admiten una serie de mensajes que recuperan información sobre los elementos del control .

El [**mensaje \_ GETITEM de TVM**](tvm-getitem.md) puede recuperar el identificador y los atributos de un elemento. Los atributos de un elemento incluyen su estado actual, los índices de la lista de imágenes del control de las imágenes de mapa de bits seleccionadas y no seleccionadas del elemento, una marca que indica si el elemento tiene elementos secundarios, la dirección de la cadena de etiqueta del elemento y el valor de 32 bits definido por la aplicación del elemento.

El [**mensaje \_ GETNEXTITEM de TVM**](tvm-getnextitem.md) recupera el elemento de vista de árbol que guarda la relación especificada con el elemento actual. El mensaje puede recuperar el elemento primario de un elemento, el elemento visible siguiente o anterior, el primer elemento secundario, y así sucesivamente.

El [**mensaje \_ GETITEMRECT**](tvm-getitemrect.md) de TVM recupera el rectángulo delimitador de un elemento de vista de árbol. Los [**mensajes \_ GETCOUNT**](tvm-getcount.md) y [**TVM \_ GETVISIBLECOUNT**](tvm-getvisiblecount.md) de TVM recuperan un recuento de los elementos de un control de vista de árbol y un recuento de los elementos que pueden ser totalmente visibles en la ventana del control de vista de árbol, respectivamente. Puede asegurarse de que un elemento determinado esté visible mediante el mensaje [**\_ ENSUREVISIBLE de TVM.**](tvm-ensurevisible.md)

## <a name="tree-view-image-lists"></a>Tree-View de imágenes

Cada elemento de un control de vista de árbol puede tener cuatro imágenes de mapa de bits asociadas.

-   Una imagen, como una carpeta abierta, se muestra cuando se selecciona el elemento.
-   Una imagen, como una carpeta cerrada, se muestra cuando el elemento no está seleccionado.
-   Imagen superpuesta que se dibuja de forma transparente sobre la imagen seleccionada o no seleccionada.
-   Imagen de estado, que es una imagen adicional que se muestra a la izquierda de la imagen seleccionada o no seleccionada. Puede usar imágenes de estado, como las casillas activadas y desactivadas, para indicar los estados de los elementos definidos por la aplicación.

De forma predeterminada, un control de vista de árbol no muestra imágenes de elementos. Para mostrar imágenes de elementos, debe crear listas de imágenes y asociarlas al control . Para obtener más información sobre las listas de imágenes, vea [Listas de imágenes.](image-lists.md)

Un control de vista de árbol puede tener dos listas de imágenes: una lista de imágenes normal y una lista de imágenes de estado. Una lista de imágenes normal almacena las imágenes seleccionadas, no seleccionadas y superpuestas. Una lista de imágenes de estado almacena imágenes de estado. Use la [**función ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) para crear una lista de imágenes y use otras funciones de lista de imágenes para agregar mapas de bits a la lista de imágenes. A continuación, para asociar la lista de imágenes con el control de vista de árbol, use el [**mensaje \_ SETIMAGELIST de TVM.**](tvm-setimagelist.md) El [**mensaje \_ GETIMAGELIST de TVM**](tvm-getimagelist.md) recupera un identificador en una de las listas de imágenes de un control de vista de árbol. Este mensaje es útil si necesita agregar más imágenes a la lista.

Además de las imágenes seleccionadas y no seleccionadas, la lista de imágenes normales de un control de vista de árbol puede contener hasta cuatro imágenes superpuestas. Las imágenes superpuestas se identifican mediante un índice basado en uno y están diseñadas para dibujarse de forma transparente sobre las imágenes seleccionadas y no seleccionadas. Para asignar un índice de máscara de superposición a una imagen de la lista de imágenes normal, llame a la [**función ImageList \_ SetOverlayImage.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage)

De forma predeterminada, todos los elementos muestran la primera imagen en la lista de imágenes normales para los estados seleccionados y no seleccionados. Además, de forma predeterminada, los elementos no muestran imágenes superpuestas ni imágenes de estado. Puede cambiar estos comportamientos predeterminados para un elemento enviando el mensaje [**\_ TVM INSERTITEM**](tvm-insertitem.md) [**o TVM \_ SETITEM.**](tvm-setitem.md) Estos mensajes usan la [**estructura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) para especificar índices de lista de imágenes para un elemento.

Para especificar las imágenes seleccionadas y no seleccionadas de un elemento, establezca los bits TVIF SELECTEDIMAGE y TVIF IMAGE en el miembro mask de la estructura TVITEM y especifique índices de la lista de imágenes normales del control en los miembros \_ \_ **iSelectImage** e **iImage.**  [](/windows/win32/api/commctrl/ns-commctrl-tvitema) Como alternativa, puede especificar el valor I \_ IMAGECALLBACK en **iSelectImage** **e iImage** en lugar de especificar índices. Esto hace que el control consulte su ventana primaria para obtener un índice de lista de imágenes cada vez que el elemento está a punto de volver a dibujarse. El control envía el [mensaje de notificación \_ GETDISPINFO de TVN](tvn-getdispinfo.md) para recuperar el índice.

Para asociar una imagen superpuesta a un elemento, use la macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) para especificar un índice de máscara de superposición en el miembro de estado de la estructura [**TVITEM del**](/windows/win32/api/commctrl/ns-commctrl-tvitema) elemento.  También debe establecer los bits [**\_ OVERLAYMASK**](tree-view-control-item-states.md) de TVIS en el **miembro stateMask.** Los índices de máscara de superposición se basan en uno; Un índice de cero indica que no se especificó ninguna imagen superpuesta.

Las imágenes de estado se almacenan en una lista de imágenes de estado independiente y se identifican por su índice. Para especificar la lista de imágenes de estado, envíe un [**mensaje \_ SETIMAGELIST de TVM.**](tvm-setimagelist.md) A diferencia del control list-view, que usa un índice basado en uno para identificar imágenes de estado, las imágenes de estado del control de vista de árbol se identifican mediante un índice de base cero. Sin embargo, un índice de cero indica que el elemento no tiene una imagen de estado. Por lo tanto, la imagen cero no se puede usar como una imagen de estado. Para obtener más información sobre los estados de los elementos y las imágenes de estado, vea [Tree-View Item States Overview](#tree-view-item-states-overview).

## <a name="drag-and-drop-operations"></a>Operaciones de arrastrar y colocar

Un control de vista de árbol notifica a la ventana primaria cuando el usuario comienza a arrastrar un elemento. La ventana primaria recibe un mensaje de notificación [ \_ BEGINDRAG](tvn-begindrag.md) de TVN cuando el usuario comienza a arrastrar un elemento con el botón izquierdo del mouse y un mensaje de notificación [DE TVN \_ BEGINRDRAG](tvn-beginrdrag.md) cuando el usuario comienza a arrastrar con el botón derecho. Puede evitar que un control de vista de árbol envíe estas notificaciones al dar al control de vista de árbol el estilo [**TVS \_ DISABLEDRAGDROP.**](tree-view-control-window-styles.md)

Para obtener una imagen que se mostrará durante una operación de arrastre, use el [**mensaje \_ CREATEDRAGIMAGE de TVM.**](tvm-createdragimage.md) El control de vista de árbol crea un mapa de bits de arrastre basado en la etiqueta del elemento que se está arrastrando. A continuación, el control de vista de árbol crea una lista de imágenes, le agrega el mapa de bits y devuelve el identificador a la lista de imágenes.

Debe proporcionar el código que realmente arrastra el elemento. Normalmente, esto implica el uso de las funciones de arrastre de las funciones de lista de imágenes y el procesamiento de los mensajes [**\_ WM MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) y [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (o [**WM \_ RBUTTONUP)**](/windows/desktop/inputdev/wm-rbuttonup)enviados a la ventana primaria una vez iniciada la operación de arrastre.

Si los elementos de un control de vista de árbol van a ser los destinos de las operaciones de arrastrar y colocar, debe saber cuándo está el puntero del mouse en un elemento de destino. Para averiguarlo, use el mensaje [**\_ HITTEST de TVM.**](tvm-hittest.md) Especifique la dirección de una estructura [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) que contiene las coordenadas actuales del puntero del mouse. Cuando se [**devuelve la función SendMessage,**](/windows/desktop/api/winuser/nf-winuser-sendmessage) la estructura contiene una marca que indica la ubicación del puntero del mouse con respecto al control de vista de árbol. Si el puntero está sobre un elemento del control de vista de árbol, la estructura también contiene el identificador del elemento.

Puede indicar que un elemento es el destino de una operación de arrastrar y colocar mediante el mensaje [**\_ SETITEM**](tvm-setitem.md) de TVM para establecer el estado en el valor [**\_ DROPHILITED de TVIS.**](tree-view-control-item-states.md) Un elemento que tiene este estado se dibuja en el estilo utilizado para indicar un destino de arrastrar y colocar.

## <a name="tree-view-control-notification-messages"></a>Tree-View control de mensajes de notificación

Un control de vista de árbol envía los siguientes mensajes de notificación a su ventana primaria en forma de [**mensajes \_ WM NOTIFY.**](wm-notify.md)



| Notificación                                    | Descripción                                                                            |
|-------------------------------------------------|----------------------------------------------------------------------------------------|
| [TVN \_ BEGINDRAG](tvn-begindrag.md)             | Señala el inicio de una operación de arrastrar y colocar.                                        |
| [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md)   | Indica el inicio de la edición de etiquetas en contexto.                                           |
| [TVN \_ BEGINRDRAG](tvn-beginrdrag.md)           | Indica que el botón derecho del mouse ha iniciado una operación de arrastrar y colocar.             |
| [DELETEITEM de TVN \_](tvn-deleteitem.md)           | Indica la eliminación de un elemento específico.                                               |
| [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md)       | Indica el final de la edición de etiquetas.                                                      |
| [TVN \_ GETDISPINFO](tvn-getdispinfo.md)         | Solicita información que el control de vista de árbol requiere para mostrar un elemento.           |
| [ELEMENTO DE \_ TVNEXPANDED](tvn-itemexpanded.md)       | Indica que la lista de elementos secundarios de un elemento primario se ha expandido o contraído.            |
| [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md)     | Indica que la lista de elementos secundarios de un elemento primario está a punto de expandirse o contraerse. |
| [TVN \_ KEYDOWN](tvn-keydown.md)                 | Señala un evento de teclado.                                                              |
| [TVN \_ SELCHANGED](tvn-selchanged.md)           | Indica que la selección ha cambiado de un elemento a otro.                       |
| [TVN \_ SELCHANGING](tvn-selchanging.md)         | Indica que la selección está a punto de cambiarse de un elemento a otro.            |
| [TVN \_ SETDISPINFO](tvn-setdispinfo.md)         | Notifica a una ventana primaria que debe actualizar la información que mantiene para un elemento. |



 

## <a name="default-tree-view-control-message-processing"></a>Procesamiento de mensajes Tree-View control predeterminado

En esta sección se describe el procesamiento de mensajes de ventana realizado por un control de vista de árbol. Los mensajes específicos de los controles de vista de árbol se analizan en otras secciones de este documento, por lo que no se incluyen aquí.



| Message                                            | Procesamiento realizado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)               | Procesa los mensajes de notificación de control de edición EN [ \_ UPDATE](en-update.md) y [EN \_ KILLFOCUS](en-killfocus.md) y reenvía todas las demás notificaciones de control de edición a la ventana primaria. No hay ningún valor devuelto.                                                                                                                                                                                                                                                                                                |
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)                 | Asigna memoria e inicializa estructuras de datos internas. Devuelve cero si se realiza correctamente o -1 en caso contrario.                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)               | Libera todos los recursos del sistema asociados al control . Devuelve cero.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**WM \_ ENABLE**](/windows/desktop/winmsg/wm-enable)                 | Habilita o deshabilita el control .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ ERASEBNDAND**](/windows/desktop/winmsg/wm-erasebkgnd)         | Borra el fondo de la ventana con el color de fondo actual para el control de vista de árbol. Devuelve **TRUE.**                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)         | Devuelve una combinación de los valores \_ WANTARROWS y \_ DLGC WANTCHARS de DLGC.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | Devuelve el identificador a la fuente de etiqueta actual.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**WM \_ HSCROLL**](wm-hscroll.md)                  | Desplaza el control de vista de árbol. Devuelve **TRUE si** se produce el desplazamiento o **FALSE** en caso contrario.                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)             | Envía el [mensaje de notificación \_ TVN KEYDOWN](tvn-keydown.md) a la ventana primaria para todas las claves. Envía el [mensaje de notificación NM RETURN \_ (vista de árbol)](nm-return-tree-view-.md) cuando el usuario presiona la tecla ENTRAR. Mueve el elemento de careta cuando el usuario presiona las teclas de dirección o la tecla PAGE UP, PAGE DOWN, HOME, END o BACKSPACE. Desplaza el control de vista de árbol cuando el usuario presiona la tecla CTRL en combinación con esas teclas. Devuelve **TRUE si** se procesa una clave o **FALSE** en caso contrario. |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)         | Vuelve a dibujar el elemento centrado, si lo hay, y envía un mensaje de notificación [ \_ KILLFOCUS (vista](nm-killfocus-tree-view.md) de árbol) NM a la ventana primaria.                                                                                                                                                                                                                                                                                                                                                                  |
| [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) | Cancela la edición de etiquetas y, si se hizo doble clic en un elemento, envía el mensaje de notificación [ \_ DE NM DBLCLK (vista](nm-dblclk-tree-view.md) de árbol) a la ventana primaria. Si la ventana primaria devuelve 0, el control de vista de árbol alterna el estado expandido del elemento y envía a la ventana primaria los mensajes de notificación [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) y [TVN \_ ITEMEXPANDED.](tvn-itemexpanded.md) No hay ningún valor devuelto.                                                                             |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)     | Alterna el estado expandido si el usuario hizo clic en el botón asociado a un elemento primario. Si el usuario hizo clic en una etiqueta de elemento, el control de vista de árbol selecciona y establece el foco en el elemento. Si el usuario mueve el mouse antes de soltar el botón del mouse, el control de vista de árbol comienza una operación de arrastrar y colocar. No hay ningún valor devuelto.                                                                                                                                                                          |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                      | Pinta la región no válida del control de vista de árbol. Devuelve cero. Si el *parámetro wParam* no es **NULL,** el control asume que el valor es un identificador para un contexto de dispositivo (HDC) y pinta con ese contexto de dispositivo.                                                                                                                                                                                                                                                                                      |
| [**WM \_ RBUTTONDOWN**](/windows/desktop/inputdev/wm-rbuttondown)     | Comprueba si se hizo clic en un elemento y se inició una operación de arrastre. Si la operación ha comenzado, envía un mensaje de notificación [ \_ BEGINRDRAG](tvn-beginrdrag.md) de TVN a la ventana primaria y resalta el destino de colocación. De lo contrario, envía un mensaje [de notificación de NM \_ RCLICK (vista](nm-rclick-tree-view.md) de árbol) a la ventana primaria. No hay ningún valor devuelto.                                                                                                                                           |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)           | Vuelve a dibujar el elemento centrado, si lo hay, y envía un mensaje de notificación [DE NM \_ SETFOCUS](nm-setfocus.md) a la ventana primaria.                                                                                                                                                                                                                                                                                                                                                                                          |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)               | Guarda el identificador de fuente especificado y vuelve a dibujar el control de vista de árbol mediante la nueva fuente.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**WM \_ SETREDRAW**](/windows/desktop/gdi/wm-setredraw)              | Establece o borra la marca de volver a dibujar. El control de vista de árbol se vuelve a dibujar después de establecer la marca de volver a dibujar. Devuelve cero.                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**TAMAÑO \_ WM**](/windows/desktop/winmsg/wm-size)                     | Vuelve a compilar variables internas que dependen del tamaño del área de cliente del control de vista de árbol. Devuelve **TRUE.**                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**ESTILO \_ WM MODIFICADO**](/windows/desktop/winmsg/wm-stylechanged)     | Cancela la edición de etiquetas y vuelve a dibujar el control de vista de árbol con los nuevos estilos. Devuelve cero.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**WM \_ SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange)    | Vuelve a dibujar el control de vista de árbol con el nuevo color si se establece la marca de volver a dibujar. No hay ningún valor devuelto.                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**TEMPORIZADOR \_ WM**](/windows/desktop/winmsg/wm-timer)                   | Comienza a editar una etiqueta de elemento. Si el usuario hace clic en la etiqueta del elemento centrado, el control de vista de árbol establece un temporizador en lugar de entrar en modo de edición inmediatamente. El temporizador permite que la vista de árbol evite entrar en modo de edición si el usuario hace doble clic en la etiqueta. Devuelve cero.                                                                                                                                                                                                                       |
| [**WM \_ VSCROLL**](wm-vscroll.md)                  | Desplaza el control de vista de árbol. Devuelve **TRUE si se** produce el desplazamiento o **FALSE** en caso contrario.                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[EJEMPLO: CustDTv ilustra el dibujo personalizado en treeview (Q248496)](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 