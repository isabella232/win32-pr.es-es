---
title: Acerca de los controles Tree-View
description: Un control de vista de árbol es una ventana que muestra una lista jerárquica de elementos, como los encabezados de un documento, las entradas de un índice o los archivos y directorios de un disco.
ms.assetid: 10cc7949-dd77-412d-bad1-db8d8a049582
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df70a2d3c2f841b022930a07ee2f140ee5bfc8e3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995687"
---
# <a name="about-tree-view-controls"></a>Acerca de los controles Tree-View

Un control de vista de árbol es una ventana que muestra una lista jerárquica de elementos, como los encabezados de un documento, las entradas de un índice o los archivos y directorios de un disco. Cada elemento se compone de una etiqueta y una imagen de mapa de imágenes opcional, y cada elemento puede tener una lista de subelementos asociados. Al hacer clic en un elemento, el usuario puede expandir o contraer la lista asociada de subelementos.

En la ilustración siguiente se muestra un control de vista de árbol simple con un nodo raíz, un nodo expandido y un nodo contraído. El control usa un mapa de bits para el elemento seleccionado y otro mapa de bits para otros elementos.

![captura de pantalla que muestra cinco nodos en una jerarquía; el texto de un nodo está seleccionado, pero los nodos no se vinculan entre sí por líneas](images/tv-simple.png)

Después de crear un control de vista de árbol, se agregan, quitan, organizan o manipulan elementos mediante el envío de mensajes al control. Cada mensaje tiene una o más macros correspondientes que puede usar en lugar de enviar el mensaje explícitamente.

Los temas siguientes se describen en esta sección.

-   [Estilos de vista de árbol](#tree-view-styles)
-   [Elementos primarios y secundarios](#parent-and-child-items)
-   [Etiquetas de elemento](#item-labels)
-   [Edición de etiquetas de vista de árbol](#tree-view-label-editing)
-   [Posición del elemento de vista de árbol](#tree-view-item-position)
-   [Información general de los Estados de los elementos de vista de árbol](#tree-view-item-states-overview)
-   [Selección de elementos](#item-selection)
-   [Información del elemento](#item-information)
-   [Listas de imágenes de vista de árbol](#tree-view-image-lists)
-   [Operaciones de arrastrar y colocar](#drag-and-drop-operations)
-   [Mensajes de notificación del control de vista de árbol](#tree-view-control-notification-messages)
-   [Procesamiento de mensajes de control de Tree-View predeterminado](#default-tree-view-control-message-processing)
-   [Temas relacionados](#related-topics)

## <a name="tree-view-styles"></a>Estilos de Tree-View

Los estilos de vista de árbol rigen aspectos de la apariencia de un control de vista de árbol. Los estilos iniciales se establecen al crear el control de vista de árbol. Puede recuperar y cambiar los estilos después de crear el control de vista de árbol mediante las funciones [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) y [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .

El [**estilo \_ HASLINES de TV**](tree-view-control-window-styles.md) mejora la representación gráfica de la jerarquía de un control de vista de árbol mediante el dibujo de líneas que vinculan elementos secundarios a su elemento primario, tal como se muestra en la siguiente ilustración.

![captura de pantalla que muestra la organización anterior, pero con líneas que unen los nodos. la primera línea Desciende del nodo raíz](images/tv-haslines.png)

Por sí solo, este estilo no dibuja líneas en la raíz de la jerarquía. Para ello, debe combinar los estilos [**TV \_ HASLINES**](tree-view-control-window-styles.md) y [**TV \_ LINESATROOT**](tree-view-control-window-styles.md) . El resultado se muestra en la ilustración siguiente.

![captura de pantalla que muestra la organización anterior, pero con una línea horizontal adicional que conduce al nodo raíz](images/tv-rootlines.png)

El usuario puede expandir o contraer la lista de elementos secundarios de un elemento primario haciendo doble clic en el elemento primario. Un control de vista de árbol con el estilo [**TV \_ HASBUTTONS**](tree-view-control-window-styles.md) agrega un botón al lado izquierdo de cada elemento primario. El usuario puede hacer clic en el botón una vez en lugar de hacer doble clic en el elemento primario para expandir o contraer el elemento secundario. **Televisores \_ HASBUTTONS** no agrega botones a los elementos de la raíz de la jerarquía. Para ello, debe combinar los [**televisores \_ HASLINES**](tree-view-control-window-styles.md), los [**televisores \_ LINESATROOT**](tree-view-control-window-styles.md)y los **televisores \_ HASBUTTONS**. Esta combinación de estilos se muestra en la siguiente ilustración.

![captura de pantalla que muestra la organización anterior, pero con los botones de expansión/contracción en cada vértice de dos líneas](images/tv-hasbuttons.png)

El [**estilo \_ casillas de televisores**](tree-view-control-window-styles.md) crea casillas junto a cada elemento. Si desea usar el estilo de casilla, debe establecer el estilo de **las \_ casillas de los televisores** (con [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)) después de crear el control de vista de árbol y antes de rellenar el árbol. De lo contrario, las casillas podrían aparecer desactivadas, en función de los problemas de temporización. En la ilustración siguiente se muestra el estilo de la casilla.

![captura de pantalla que muestra la organización anterior, pero con una casilla junto a cada nodo; dos de las casillas están seleccionadas](images/tv-haschecks.png)

El [**estilo \_ FULLROWSELECT de los televisores**](tree-view-control-window-styles.md) hace que el resaltado de la selección se extienda sobre el ancho completo del control, no solo sobre el propio elemento. En la ilustración siguiente se muestra este estilo.

![captura de pantalla que muestra la disposición original de cinco nodos sin líneas, pero el resaltado de la selección extiende el ancho completo del control](images/tv-fullrow.png)

El [**estilo \_ EDITLABELS de los televisores**](tree-view-control-window-styles.md) permite al usuario editar las etiquetas de los elementos de la vista de árbol. Para obtener más información sobre la edición de etiquetas, vea [edición de etiquetas de vista de árbol](#tree-view-label-editing).

Para obtener más información sobre estos y otros estilos, vea [estilos de la ventana de control de vista de árbol](tree-view-control-window-styles.md).

## <a name="parent-and-child-items"></a>Elementos primarios y secundarios

Cualquier elemento de un control de vista de árbol puede tener una lista de subelementos (denominados *elementos secundarios*) asociados. Un elemento que tiene uno o más elementos secundarios se denomina *elemento primario*. Un elemento secundario se muestra debajo de su elemento primario y se le aplica una sangría para indicar que está subordinado al primario. Un elemento que no tiene ningún elemento primario aparece en la parte superior de la jerarquía y se denomina *elemento raíz*.

Para agregar un elemento a un control de vista de árbol, envíe el mensaje [**TVM \_ INSERTITEM**](tvm-insertitem.md) al control. El mensaje devuelve un identificador al tipo HTREEITEM, que identifica de forma única el elemento. Al agregar un elemento, debe especificar el identificador del elemento primario del nuevo elemento. Si especifica **null** o el \_ valor raíz TVI en lugar de un identificador de elemento primario en la estructura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) , el elemento se agrega como un elemento raíz.

En un momento dado, el estado de la lista de elementos secundarios de un elemento primario puede expandirse o contraerse. Cuando se expande el estado, los elementos secundarios se muestran debajo del elemento primario. Cuando se contrae, no se muestran los elementos secundarios. La lista alterna automáticamente entre los Estados expandido y contraído cuando el usuario hace doble clic en el elemento primario o, si el elemento primario tiene el estilo [**\_ HASBUTTONS de TV**](tree-view-control-window-styles.md) , cuando el usuario hace clic en el botón asociado al elemento primario. Una aplicación puede expandir o contraer los elementos secundarios mediante el mensaje [**TVM \_ Expand**](tvm-expand.md) .

Un control de vista de árbol envía a la ventana primaria un mensaje de notificación [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) cuando la lista de elementos secundarios de un elemento primario está a punto de expandirse o contraerse. La notificación proporciona a una aplicación la oportunidad de evitar el cambio o establecer los atributos del elemento primario que dependen del estado de la lista de elementos secundarios. Después de cambiar el estado de la lista, el control de vista de árbol envía a la ventana primaria un mensaje de notificación de [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) .

Cuando se expande una lista de elementos secundarios, se aplica una sangría relativa al elemento primario. Puede establecer la cantidad de sangría mediante el mensaje [**TVM \_ SETINDENT**](tvm-setindent.md) o recuperar la cantidad actual mediante el mensaje [**TVM \_ GETINDENT**](tvm-getindent.md) .

Un control de vista de árbol utiliza la memoria asignada del montón del proceso que crea el control de vista de árbol. El número máximo de elementos de una vista de árbol se basa en la cantidad de memoria disponible en el montón.

## <a name="item-labels"></a>Etiquetas de elemento

Normalmente, se especifica el texto de la etiqueta de un elemento al agregarlo al control de vista de árbol. El mensaje [**TVM \_ INSERTITEM**](tvm-insertitem.md) incluye una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que define las propiedades del elemento, incluida una cadena que contiene el texto de la etiqueta.

Un control de vista de árbol asigna memoria para almacenar cada elemento; el texto de las etiquetas del elemento ocupa una parte importante de esta memoria. Si la aplicación mantiene una copia de las cadenas en el control de vista de árbol, puede reducir los requisitos de memoria del control especificando el \_ valor de LPSTR TEXTCALLBACK en el miembro **miembros pszText** de [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) en lugar de pasar cadenas reales a la vista de árbol. El uso de LPSTR \_ TEXTCALLBACK hace que el control de vista de árbol recupere el texto de la etiqueta de un elemento de la ventana primaria siempre que sea necesario volver a dibujar el elemento. Para recuperar el texto, el control de vista de árbol envía un mensaje de notificación [ \_ GETDISPINFO de TVN](tvn-getdispinfo.md) , que incluye la dirección de una estructura [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) . La ventana primaria debe rellenar los miembros adecuados de la estructura incluida.

## <a name="tree-view-label-editing"></a>Edición de Tree-View etiqueta

El usuario puede editar directamente las etiquetas de los elementos de un control de vista de árbol que tenga el estilo [**TV \_ EDITLABELS**](tree-view-control-window-styles.md) . El usuario comienza a editar haciendo clic en la etiqueta del elemento que tiene el foco. Una aplicación comienza a editarse mediante el mensaje [**TVM \_ EDITLABEL**](tvm-editlabel.md) . El control de vista de árbol notifica a la ventana primaria cuando comienza la edición y cuando se cancela o se completa. Cuando se completa la edición, la ventana primaria es responsable de actualizar la etiqueta del elemento, si es necesario.

Cuando comienza la edición de etiquetas, un control de vista de árbol envía a su ventana primaria un mensaje de notificación de [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) . Al procesar esta notificación, una aplicación puede permitir la edición de algunas etiquetas y evitar la edición de otras. Devolver cero permite la edición y devolver un valor distinto de cero lo evita.

Cuando la edición de etiquetas se cancela o se completa, un control de vista de árbol envía a su ventana primaria un mensaje de notificación de [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) . El parámetro *lParam* es la dirección de una estructura [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) . El parámetro *Item* es una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que identifica el elemento e incluye el texto editado. La ventana primaria es responsable de actualizar la etiqueta del elemento si desea mantener la nueva etiqueta. El miembro **miembros pszText** de **TVITEM** es cero si se cancela la edición.

Durante la edición de etiquetas, normalmente en respuesta al mensaje de notificación [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) , puede recuperar el identificador del control de edición que se usa para la edición de etiquetas mediante el mensaje [**TVM \_ GETEDITCONTROL**](tvm-geteditcontrol.md) . Puede enviar un mensaje [**\_ SETLIMITTEXT de EM**](em-setlimittext.md) para limitar la cantidad de texto que un usuario puede escribir o subclase del control de edición para interceptar y descartar los caracteres no válidos. Tenga en cuenta, sin embargo, que el control de edición solo se muestra *después* de   \_ Enviar TVN BEGINLABELEDIT.

## <a name="tree-view-item-position"></a>Tree-View posición del elemento

La posición inicial de un elemento se establece cuando el elemento se agrega al control de vista de árbol mediante el mensaje de la opción [**TVM \_ INSERTITEM**](tvm-insertitem.md) . El mensaje incluye una estructura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) que especifica el identificador del elemento primario y el identificador del elemento después del cual se va a insertar el nuevo elemento. El segundo identificador debe identificar un elemento secundario del elemento primario especificado o uno de estos valores: TVI \_ First, TVI \_ Last u TVI \_ Sort.

Cuando \_ se especifica TVI First o TVI \_ Last, el control de vista de árbol coloca el nuevo elemento al principio o al final de la lista de elementos secundarios del elemento primario especificado. Cuando \_ se especifica TVI Sort, el control de vista de árbol inserta el nuevo elemento en la lista de elementos secundarios en orden alfabético según el texto de las etiquetas de los elementos.

Puede colocar la lista de elementos secundarios de un elemento primario en orden alfabético mediante el mensaje [**de \_ SORTCHILDREN TVM**](tvm-sortchildren.md) . El mensaje incluye un parámetro que especifica si todos los niveles de elementos secundarios que descienden del elemento primario dado también se ordenan en orden alfabético.

El mensaje [**TVM \_ SORTCHILDRENCB**](tvm-sortchildrencb.md) le permite ordenar los elementos secundarios en función de los criterios que defina. Cuando se usa este mensaje, se especifica una función de devolución de llamada definida por la aplicación a la que el control de vista de árbol puede llamar cuando sea necesario decidir el orden relativo de dos elementos secundarios. La función de devolución de llamada recibe valores definidos por la aplicación de 2 32 bits para los elementos que se están comparando y un tercer valor de 32 bits que se especifica al enviar **TVM \_ SORTCHILDRENCB**.

## <a name="tree-view-item-states-overview"></a>Información general sobre los Estados de los elementos Tree-View

Cada elemento de un control de vista de árbol tiene un estado actual. La información de estado de cada elemento incluye un conjunto de marcas de bits, así como índices de lista de imágenes que indican la imagen de estado del elemento y la imagen de superposición. Las marcas de bits indican si el elemento está seleccionado, deshabilitado, expandido, etc. En su mayor parte, un control de vista de árbol establece automáticamente el estado de un elemento para reflejar las acciones del usuario, como la selección de un elemento. Sin embargo, también puede establecer el estado de un elemento mediante el mensaje [**TVM \_ SETITEM**](tvm-setitem.md) , y puede recuperar el estado actual de un elemento mediante el mensaje de [**\_ GETITEM de TVM**](tvm-getitem.md) . Para obtener una lista completa de los Estados de elemento, vea [Estados de elemento de control de vista de árbol](tree-view-control-item-states.md).

El estado actual de un elemento se especifica mediante el miembro de **Estado** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) . Un control de vista de árbol puede cambiar el estado de un elemento para reflejar una acción del usuario, como seleccionar el elemento o establecer el foco en el elemento. Además, una aplicación podría cambiar el estado de un elemento para deshabilitar u ocultar el elemento o para especificar una imagen de superposición o imagen de estado.

Al especificar o cambiar el estado de un elemento, el miembro **statemask** de [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) especifica qué bits de estado establecer y el miembro **State** contiene los nuevos valores de esos bits.

Para establecer la imagen de superposición de un elemento, **statemask** debe incluir el valor [**TVIS \_ OVERLAYMASK**](tree-view-control-item-states.md) y el **Estado** debe incluir el índice basado en uno de la imagen de superposición desplazada a la izquierda 8 bits mediante la macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) . El índice puede ser cero para no especificar ninguna imagen de superposición.

Se muestra una imagen de Estado junto al icono de un elemento para indicar un estado definido por la aplicación. Las imágenes de estado se incluyen en una *lista de imágenes de estado* que se especifica mediante el envío de un mensaje [**TVM \_ SETIMAGELIST**](tvm-setimagelist.md) . Para establecer la imagen de estado de un elemento, incluya el valor de [**TVIS \_ STATEIMAGEMASK**](tree-view-control-item-states.md) en el miembro **Statemask** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) . Los bits 12 a 15 del miembro **State** de la estructura especifican el índice en la lista de imágenes de estado de la imagen que se va a dibujar.

Para establecer el índice de la imagen de estado, use [**INDEXTOSTATEIMAGEMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask). Esta macro toma un índice y establece los bits del 12 al 15 adecuadamente. Para indicar que el elemento no tiene ninguna imagen de estado, establezca el índice en cero. Esta Convención significa que la imagen cero de la lista de imágenes de estado no se puede usar como una imagen de estado. Para aislar los bits del 12 al 15 del miembro de **Estado** , use la máscara [**\_ STATEIMAGEMASK de TVIS**](tree-view-control-item-states.md) . Para obtener más información acerca de las imágenes de superposición y de estado, consulte [listas de imágenes de vista de árbol](#tree-view-image-lists).

## <a name="item-selection"></a>Selección de elementos

Un control de vista de árbol notifica a la ventana primaria cuando la selección cambia de un elemento a otro mediante el envío de los mensajes de notificación [TVN \_ SELCHANGING](tvn-selchanging.md) y [TVN \_ SELCHANGED](tvn-selchanged.md) . Ambas notificaciones incluyen un valor que especifica si el cambio es el resultado de un clic del mouse o una pulsación de tecla. Las notificaciones también incluyen información sobre el elemento que obtiene la selección y el elemento que pierde la selección. Puede usar esta información para establecer atributos de elementos que dependen del estado de selección del elemento. Si se devuelve **true** en respuesta a TVN \_ SELCHANGING, se evita que la selección cambie y se devuelve **false** , lo que permite realizar el cambio.

Una aplicación puede cambiar la selección mediante el envío del mensaje [**TVM \_ SELECTITEM**](tvm-selectitem.md) .

## <a name="item-information"></a>Información del elemento

Los controles de vista de árbol admiten una serie de mensajes que recuperan información sobre los elementos del control.

El mensaje de [**\_ GETITEM de TVM**](tvm-getitem.md) puede recuperar el identificador y los atributos de un elemento. Los atributos de un elemento incluyen su estado actual, los índices de la lista de imágenes del control de las imágenes de mapa de bits seleccionadas y no seleccionadas del elemento, una marca que indica si el elemento tiene elementos secundarios, la dirección de la cadena de etiqueta del elemento y el valor de 32 bits definido por la aplicación del elemento.

El mensaje [**TVM \_ GETNEXTITEM**](tvm-getnextitem.md) recupera el elemento de vista de árbol que lleva la relación especificada con el elemento actual. El mensaje puede recuperar el elemento primario de un elemento, el elemento visible siguiente o anterior, el primer elemento secundario, etc.

El mensaje [**TVM \_ GETITEMRECT**](tvm-getitemrect.md) recupera el rectángulo delimitador de un elemento de vista de árbol. Los mensajes [**TVM \_ GETCOUNT**](tvm-getcount.md) y [**TVM \_ GETVISIBLECOUNT**](tvm-getvisiblecount.md) recuperan un recuento de los elementos de un control de vista de árbol y un recuento de los elementos que pueden estar totalmente visibles en la ventana del control de vista de árbol, respectivamente. Puede asegurarse de que un elemento determinado esté visible mediante el mensaje de la [**\_ ENSUREVISIBLE de TVM**](tvm-ensurevisible.md) .

## <a name="tree-view-image-lists"></a>Tree-View listas de imágenes

Cada elemento de un control de vista de árbol puede tener cuatro imágenes de mapa de bits asociadas.

-   Una imagen, como una carpeta abierta, que se muestra cuando se selecciona el elemento.
-   Una imagen, como una carpeta cerrada, que se muestra cuando no se selecciona el elemento.
-   Imagen superpuesta dibujada de forma transparente sobre la imagen seleccionada o no seleccionada.
-   Una imagen de estado, que es una imagen adicional que se muestra a la izquierda de la imagen seleccionada o no seleccionada. Puede usar las imágenes de estado, como las casillas activada y desactivada, para indicar los Estados de los elementos definidos por la aplicación.

De forma predeterminada, un control de vista de árbol no muestra imágenes de elementos. Para mostrar imágenes de elementos, debe crear listas de imágenes y asociarlas al control. Para obtener más información acerca de las listas de imágenes, consulte [listas de imágenes](image-lists.md).

Un control de vista de árbol puede tener dos listas de imágenes: una lista de imágenes normal y una lista de imágenes de estado. Una lista de imágenes normal almacena las imágenes seleccionadas, no seleccionadas y superpuestas. Una lista de imágenes de estado almacena imágenes de estado. Use la función [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) para crear una lista de imágenes y use otras funciones de lista de imágenes para agregar mapas de bits a la lista de imágenes. A continuación, para asociar la lista de imágenes con el control de vista de árbol, use el mensaje [**TVM \_ SETIMAGELIST**](tvm-setimagelist.md) . El mensaje [**TVM \_ GETIMAGELIST**](tvm-getimagelist.md) recupera un identificador de una de las listas de imágenes del control de vista de árbol. Este mensaje es útil si necesita agregar más imágenes a la lista.

Además de las imágenes seleccionadas y no seleccionadas, una lista de imágenes normales del control de vista de árbol puede contener hasta cuatro imágenes superpuestas. Las imágenes superpuestas se identifican mediante un índice basado en uno y están diseñadas para dibujarse de forma transparente sobre las imágenes seleccionadas y no seleccionadas. Para asignar un índice de máscara de superposición a una imagen en la lista de imágenes normales, llame a la función [**ImageList \_ SetOverlayImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) .

De forma predeterminada, todos los elementos muestran la primera imagen de la lista de imágenes normal para los Estados seleccionado y no seleccionado. Además, de forma predeterminada, los elementos no muestran imágenes de superposición o imágenes de estado. Puede cambiar estos comportamientos predeterminados para un elemento mediante el envío del mensaje [**TVM \_ INSERTITEM**](tvm-insertitem.md) o [**TVM \_ SETITEM**](tvm-setitem.md) . Estos mensajes usan la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) para especificar índices de lista de imágenes para un elemento.

Para especificar imágenes seleccionadas y no seleccionadas de un elemento, establezca los bits de \_ imagen TVIF SELECTEDIMAGE y TVIF \_ en el miembro **Mask** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) y especifique los índices de la lista de imágenes normal del control en los miembros **iSelectImage** y **iImage** . Como alternativa, puede especificar el valor I \_ IMAGECALLBACK en **ISelectImage** y **iImage** en lugar de especificar los índices. Esto hace que el control consulte su ventana primaria para obtener un índice de la lista de imágenes cada vez que se vuelva a dibujar el elemento. El control envía el mensaje de notificación [TVN \_ GETDISPINFO](tvn-getdispinfo.md) para recuperar el índice.

Para asociar una imagen de superposición a un elemento, use la macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) para especificar un índice de máscara de superposición en el miembro **State** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) del elemento. También debe establecer los bits [**TVIS \_ OVERLAYMASK**](tree-view-control-item-states.md) en el miembro **stateMask** . Los índices de máscara superpuestas están basados en uno; un índice de cero indica que no se ha especificado ninguna imagen de superposición.

Las imágenes de estado se almacenan en una lista de imágenes de estado independiente y se identifican por su índice. Para especificar la lista de imágenes de estado, envíe un mensaje [**TVM \_ SETIMAGELIST**](tvm-setimagelist.md) . A diferencia del control de vista de lista, que utiliza un índice basado en uno para identificar imágenes de estado, las imágenes de estado de control de vista de árbol se identifican mediante un índice basado en cero. Sin embargo, un índice de cero indica que el elemento no tiene una imagen de estado. Por lo tanto, la imagen cero no se puede usar como una imagen de estado. Para obtener más información sobre los Estados de los elementos y las imágenes de estado, consulte [información general sobre los Estados de los elementos de vista de árbol](#tree-view-item-states-overview).

## <a name="drag-and-drop-operations"></a>Operaciones de arrastrar y colocar

Un control de vista de árbol notifica a la ventana primaria cuando el usuario empieza a arrastrar un elemento. La ventana primaria recibe un mensaje de notificación de [TVN \_ BEGINDRAG](tvn-begindrag.md) cuando el usuario comienza a arrastrar un elemento con el botón primario del mouse y un mensaje de notificación de [TVN \_ BEGINRDRAG](tvn-beginrdrag.md) cuando el usuario comienza a arrastrar con el botón derecho. Puede impedir que un control de vista de árbol Envíe estas notificaciones proporcionando el estilo [**\_ DISABLEDRAGDROP de los televisores**](tree-view-control-window-styles.md) al control de vista de árbol.

Se obtiene una imagen para mostrar durante una operación de arrastre mediante el mensaje [**TVM \_ CREATEDRAGIMAGE**](tvm-createdragimage.md) . El control de vista de árbol crea un mapa de bits de arrastre basado en la etiqueta del elemento que se está arrastrando. Después, el control de vista de árbol crea una lista de imágenes, le agrega el mapa de bits y devuelve el identificador de la lista de imágenes.

Debe proporcionar el código que realmente arrastra el elemento. Normalmente, esto implica el uso de las funciones de arrastre de las funciones de la lista de imágenes y el procesamiento de los mensajes de [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) y [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (o [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)) enviados a la ventana primaria una vez iniciada la operación de arrastre.

Si los elementos de un control de vista de árbol son los destinos de las operaciones de arrastrar y colocar, debe saber cuándo está el puntero del mouse en un elemento de destino. Puede averiguar mediante el mensaje [**TVM \_ HITTEST**](tvm-hittest.md) . Se especifica la dirección de una estructura [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) que contiene las coordenadas actuales del puntero del mouse. Cuando se devuelve la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , la estructura contiene una marca que indica la ubicación del puntero del mouse en relación con el control de vista de árbol. Si el puntero se encuentra sobre un elemento en el control de vista de árbol, la estructura contiene también el identificador del elemento.

Puede indicar que un elemento es el destino de una operación de arrastrar y colocar mediante el mensaje [**TVM \_ SETITEM**](tvm-setitem.md) para establecer el estado en el valor de [**TVIS \_ DROPHILITED**](tree-view-control-item-states.md) . Un elemento que tiene este estado se dibuja en el estilo utilizado para indicar un destino de arrastrar y colocar.

## <a name="tree-view-control-notification-messages"></a>Tree-View de mensajes de notificación de control

Un control de vista de árbol envía los siguientes mensajes de notificación a su ventana primaria en forma de mensajes de notificación de [**WM \_**](wm-notify.md) .



| notificación                                    | Descripción                                                                            |
|-------------------------------------------------|----------------------------------------------------------------------------------------|
| [TVN \_ BEGINDRAG](tvn-begindrag.md)             | Indica el inicio de una operación de arrastrar y colocar.                                        |
| [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md)   | Señala el inicio de la edición de etiquetas en contexto.                                           |
| [TVN \_ BEGINRDRAG](tvn-beginrdrag.md)           | Indica que el botón secundario del mouse ha iniciado una operación de arrastrar y colocar.             |
| [TVN \_ DELETEITEM](tvn-deleteitem.md)           | Indica la eliminación de un elemento específico.                                               |
| [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md)       | Señala el final de la edición de la etiqueta.                                                      |
| [TVN \_ GETDISPINFO](tvn-getdispinfo.md)         | Solicita información que el control de vista de árbol requiere para mostrar un elemento.           |
| [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md)       | Indica que la lista de elementos secundarios de un elemento primario se ha expandido o contraído.            |
| [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md)     | Indica que la lista de elementos secundarios de un elemento primario está a punto de expandirse o contraerse. |
| [TVN ( \_ KEYDOWN)](tvn-keydown.md)                 | Señala un evento de teclado.                                                              |
| [TVN \_ SELCHANGED](tvn-selchanged.md)           | Indica que la selección ha cambiado de un elemento a otro.                       |
| [TVN \_ SELCHANGING](tvn-selchanging.md)         | Indica que la selección está a punto de cambiarse de un elemento a otro.            |
| [TVN \_ SETDISPINFO](tvn-setdispinfo.md)         | Notifica a una ventana primaria que debe actualizar la información que mantiene para un elemento. |



 

## <a name="default-tree-view-control-message-processing"></a>Procesamiento de mensajes de control de Tree-View predeterminado

En esta sección se describe el procesamiento de mensajes de ventana que realiza un control de vista de árbol. Los mensajes específicos de los controles de vista de árbol se describen en otras secciones de este documento, por lo que no se incluyen aquí.



| Message                                            | Procesamiento realizado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**comando de WM \_**](/windows/desktop/menurc/wm-command)               | Procesa los mensajes de notificación del control [en la \_ actualización](en-update.md) y [en \_ KILLFOCUS](en-killfocus.md) y reenvía todas las demás notificaciones del control de edición a la ventana primaria. No hay ningún valor devuelto.                                                                                                                                                                                                                                                                                                |
| [**creación de WM \_**](/windows/desktop/winmsg/wm-create)                 | Asigna memoria e inicializa estructuras de datos internas. Devuelve cero si es correcto o-1 en caso contrario.                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**destrucción de WM \_**](/windows/desktop/winmsg/wm-destroy)               | Libera todos los recursos del sistema asociados al control. Devuelve cero.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**\_habilitación de WM**](/windows/desktop/winmsg/wm-enable)                 | Habilita o deshabilita el control.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**ERASEBKGND de WM \_**](/windows/desktop/winmsg/wm-erasebkgnd)         | Borra el fondo de la ventana con el color de fondo actual del control de vista de árbol. Devuelve **true**.                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**GETDLGCODE de WM \_**](/windows/desktop/dlgbox/wm-getdlgcode)         | Devuelve una combinación de los valores de DLGC \_ WANTARROWS y DLGC \_ WANTCHARS.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**GETFONT de WM \_**](/windows/desktop/winmsg/wm-getfont)               | Devuelve el identificador de la fuente de la etiqueta actual.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**HSCROLL de WM \_**](wm-hscroll.md)                  | Desplaza el control de vista de árbol. Devuelve **true** si se produce el desplazamiento o **false** en caso contrario.                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**KEYDOWN de WM \_**](/windows/desktop/inputdev/wm-keydown)             | Envía el mensaje de notificación [ \_ KEYDOWN TVN](tvn-keydown.md) a la ventana primaria para todas las claves. Envía el mensaje de notificación de [devolución de nm \_ (vista de árbol)](nm-return-tree-view-.md) cuando el usuario presiona la tecla entrar. Mueve el símbolo de intercalación cuando el usuario presiona las teclas de dirección o la tecla RE PÁG, Av Pág, Inicio, final o retroceso. Desplaza el control de vista de árbol cuando el usuario presiona la tecla CTRL junto con esas teclas. Devuelve **true** si se procesa una clave o **false** en caso contrario. |
| [**KILLFOCUS de WM \_**](/windows/desktop/inputdev/wm-killfocus)         | Vuelve a dibujar el elemento que tiene el foco, si existe, y envía un mensaje de notificación de [ \_ KILLFOCUS (vista de árbol) de nm](nm-killfocus-tree-view.md) a la ventana primaria.                                                                                                                                                                                                                                                                                                                                                                  |
| [**LBUTTONDBLCLK de WM \_**](/windows/desktop/inputdev/wm-lbuttondblclk) | Cancela la edición de etiquetas y, si se hizo doble clic en un elemento, envía el mensaje de notificación de [ \_ DBLCLK (vista de árbol) de nm](nm-dblclk-tree-view.md) a la ventana primaria. Si la ventana primaria devuelve 0, el control de vista de árbol alterna el estado expandido del elemento y envía a la ventana primaria los mensajes de notificación [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) y [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) . No hay ningún valor devuelto.                                                                             |
| [**LBUTTONDOWN de WM \_**](/windows/desktop/inputdev/wm-lbuttondown)     | Alterna el estado expandido si el usuario hizo clic en el botón asociado a un elemento primario. Si el usuario hizo clic en una etiqueta de elemento, el control de vista de árbol selecciona y establece el foco en el elemento. Si el usuario mueve el mouse antes de soltar el botón del mouse, el control de vista de árbol inicia una operación de arrastrar y colocar. No hay ningún valor devuelto.                                                                                                                                                                          |
| [**pintura de WM \_**](/windows/desktop/gdi/wm-paint)                      | Pinta la región no válida del control de vista de árbol. Devuelve cero. Si el parámetro *wParam* no es **null**, el control supone que el valor es un identificador de un contexto de dispositivo (HDC) y dibuja usando ese contexto de dispositivo.                                                                                                                                                                                                                                                                                      |
| [**RBUTTONDOWN de WM \_**](/windows/desktop/inputdev/wm-rbuttondown)     | Comprueba si se hizo clic en un elemento y se inició una operación de arrastre. Si se ha iniciado la operación, envía un mensaje de notificación [TVN \_ BEGINRDRAG](tvn-beginrdrag.md) a la ventana primaria y resalta el destino de colocación. De lo contrario, envía un mensaje de notificación de [ \_ RCLICK (vista de árbol) de nm](nm-rclick-tree-view.md) a la ventana primaria. No hay ningún valor devuelto.                                                                                                                                           |
| [**SETFOCUS de WM \_**](/windows/desktop/inputdev/wm-setfocus)           | Vuelve a dibujar el elemento enfocado, si existe, y envía un mensaje de notificación de [ \_ SETFOCUS de nm](nm-setfocus.md) a la ventana primaria.                                                                                                                                                                                                                                                                                                                                                                                          |
| [**WM \_**](/windows/desktop/winmsg/wm-setfont)               | Guarda el identificador de fuente especificado y vuelve a dibujar el control de vista de árbol con la nueva fuente.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**SETREDRAW de WM \_**](/windows/desktop/gdi/wm-setredraw)              | Establece o borra la marca de volver a dibujar. El control de vista de árbol se vuelve a dibujar cuando se establece la marca de volver a dibujar. Devuelve cero.                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**tamaño de WM \_**](/windows/desktop/winmsg/wm-size)                     | Vuelve a calcular las variables internas que dependen del tamaño del área cliente del control de vista de árbol. Devuelve **true**.                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**STYLECHANGED de WM \_**](/windows/desktop/winmsg/wm-stylechanged)     | Cancela la edición de etiquetas y vuelve a dibujar el control de vista de árbol con los nuevos estilos. Devuelve cero.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**SYSCOLORCHANGE de WM \_**](/windows/desktop/gdi/wm-syscolorchange)    | Vuelve a dibujar el control de vista de árbol usando el nuevo color si se establece la marca de volver a dibujar. No hay ningún valor devuelto.                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**temporizador de WM \_**](/windows/desktop/winmsg/wm-timer)                   | Comienza a editar una etiqueta de elemento. Si el usuario hace clic en la etiqueta del elemento enfocado, el control de vista de árbol establece un temporizador en lugar de entrar en el modo de edición inmediatamente. El temporizador permite que la vista de árbol Evite entrar en el modo de edición si el usuario hace doble clic en la etiqueta. Devuelve cero.                                                                                                                                                                                                                       |
| [**VSCROLL de WM \_**](wm-vscroll.md)                  | Desplaza el control de vista de árbol. Devuelve **true** si se produce el desplazamiento o **false** en caso contrario.                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[EJEMPLO: CustDTv ilustra el dibujo personalizado en una vista de árbol (Q248496)](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 