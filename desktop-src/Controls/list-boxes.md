---
title: Cuadro de lista
description: Esta sección contiene información sobre los elementos de programación utilizados con cuadros de lista. Un cuadro de lista es una ventana de control que contiene una lista simple de elementos entre los que el usuario puede elegir.
ms.assetid: vs|controls|~\controls\listboxes\listboxes.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4c4dcd456c3774fce5899313ce1ead2a464a23c3706ba549b5cf581034d0dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085135"
---
# <a name="list-box"></a>Cuadro de lista

Esta sección contiene información sobre los elementos de programación utilizados con cuadros de lista. Un cuadro de lista es una ventana de control que contiene una lista simple de elementos entre los que el usuario puede elegir. Para listas más complejas, use la [Vista de lista](list-view-control-reference.md) en su lugar.

### <a name="overviews"></a>Temas de introducción



| Tema                                    | Contenido                                                              |
|------------------------------------------|-----------------------------------------------------------------------|
| [Acerca de los cuadros de lista](about-list-boxes.md) | Describe las características del cuadro de lista.<br/>                               |
| [Usar cuadros de lista](using-list-boxes.md) | Explica cómo realizar tareas asociadas a cuadros de lista. <br/> |



 

### <a name="functions"></a>Funciones



| Tema                                    | Contenido                                                                                                                |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)         | Reemplaza el contenido de un cuadro de lista por los nombres de los subdirectorios y archivos de un directorio especificado.<br/> |
| [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) | Recupera la selección actual de un cuadro de lista de selección única.<br/>                                            |
| [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert)         | Dibuja el icono de inserción en la ventana primaria del cuadro de lista de arrastre especificado. <br/>                                  |
| [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo) | Recupera información sobre el cuadro de lista especificado.<br/>                                                          |
| [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt)     | Recupera el índice del elemento en el punto especificado de un cuadro de lista. <br/>                                       |
| [**MakeDragList**](/windows/desktop/api/Commctrl/nf-commctrl-makedraglist)     | Cambia el cuadro de lista de selección única especificado a un cuadro de lista de arrastrar. <br/>                                         |



 

### <a name="messages"></a>error de Hadoop



| Tema                                                     | Contenido                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LB \_ ADDFILE**](lb-addfile.md)                         | Agrega el nombre de archivo especificado a un cuadro de lista que contiene una lista de directorios. <br/>                                                                                                                                                                                     |
| [**LB \_ ADDSTRING**](lb-addstring.md)                     | Agrega una cadena a un cuadro de lista. <br/>                                                                                                                                                                                                                                      |
| [**LB \_ DELETESTRING**](lb-deletestring.md)               | Elimina una cadena en un cuadro de lista. <br/>                                                                                                                                                                                                                                   |
| [**LB \_ DIR**](lb-dir.md)                                 | Agrega nombres a la lista mostrada por un cuadro de lista. <br/>                                                                                                                                                                                                                   |
| [**LB \_ FINDSTRING**](lb-findstring.md)                   | Busca la primera cadena en un cuadro de lista que comienza con la cadena especificada. <br/>                                                                                                                                                                                       |
| [**LB \_ FINDSTRINGEXACT**](lb-findstringexact.md)         | Busca la primera cadena de cuadro de lista que coincida exactamente con la cadena especificada, salvo que la búsqueda no distingue mayúsculas de minúsculas. <br/>                                                                                                                                          |
| [**LB \_ GETANCHORINDEX**](lb-getanchorindex.md)           | Obtiene el índice del elemento delimitador, es decir, el elemento desde el que se inicia una selección múltiple. <br/>                                                                                                                                                                       |
| [**LB \_ GETCARETINDEX**](lb-getcaretindex.md)             | Recupera el índice del elemento que tiene el rectángulo de foco en un cuadro de lista de selección múltiple. El elemento puede estar seleccionado o no. <br/>                                                                                                                               |
| [**LB \_ GETCOUNT**](lb-getcount.md)                       | Obtiene el número de elementos de un cuadro de lista. <br/>                                                                                                                                                                                                                           |
| [**LB \_ GETCURSEL**](lb-getcursel.md)                     | Obtiene el índice del elemento seleccionado actualmente, si existe, en un cuadro de lista de selección única. <br/>                                                                                                                                                                            |
| [**LB \_ GETHORIZONTALEXTENT**](lb-gethorizontalextent.md) | Obtiene el ancho, en píxeles, que un cuadro de lista se puede desplazar horizontalmente (el ancho desplazable) si el cuadro de lista tiene una barra de desplazamiento horizontal. <br/>                                                                                                                       |
| [**LB \_ GETITEMDATA**](lb-getitemdata.md)                 | Obtiene el valor definido por la aplicación asociado al elemento de cuadro de lista especificado. <br/>                                                                                                                                                                                   |
| [**LB \_ GETITEMHEIGHT**](lb-getitemheight.md)             | Obtiene el alto de los elementos de un cuadro de lista. <br/>                                                                                                                                                                                                                           |
| [**LB \_ GETITEMRECT**](lb-getitemrect.md)                 | Obtiene las dimensiones del rectángulo que delimita un elemento de cuadro de lista tal como se muestra actualmente en el cuadro de lista. <br/>                                                                                                                                                    |
| [**LB \_ GETLISTBOXINFO**](lb-getlistboxinfo.md)           | Obtiene el número de elementos por columna de un cuadro de lista especificado. <br/>                                                                                                                                                                                                      |
| [**LB \_ GETLOCALE**](lb-getlocale.md)                     | Obtiene la configuración regional actual del cuadro de lista. <br/>                                                                                                                                                                                                                          |
| [**LB \_ GETSEL**](lb-getsel.md)                           | Obtiene el estado de selección de un elemento. <br/>                                                                                                                                                                                                                              |
| [**LB \_ GETSELCOUNT**](lb-getselcount.md)                 | Obtiene el número total de elementos seleccionados en un cuadro de lista de selección múltiple. <br/>                                                                                                                                                                                         |
| [**LB \_ GETSELITEMS**](lb-getselitems.md)                 | Rellena un búfer con una matriz de enteros que especifican los números de elemento de los elementos seleccionados en un cuadro de lista de selección múltiple. <br/>                                                                                                                                        |
| [**LB \_ GETTEXT**](lb-gettext.md)                         | Obtiene una cadena de un cuadro de lista. <br/>                                                                                                                                                                                                                                    |
| [**LB \_ GETTEXTLEN**](lb-gettextlen.md)                   | Obtiene la longitud de una cadena en un cuadro de lista. <br/>                                                                                                                                                                                                                        |
| [**LB \_ GETTOPINDEX**](lb-gettopindex.md)                 | Obtiene el índice del primer elemento visible de un cuadro de lista. <br/>                                                                                                                                                                                                           |
| [**LB \_ INITSTORAGE**](lb-initstorage.md)                 | Asigna memoria para almacenar elementos de cuadro de lista. Este mensaje se usa antes de que una aplicación agrega un gran número de elementos a un cuadro de lista.<br/>                                                                                                                                |
| [**LB \_ INSERTSTRING**](lb-insertstring.md)               | Inserta datos de cadena o elemento en un cuadro de lista. A diferencia [**del \_ mensaje LB ADDSTRING,**](lb-addstring.md) el mensaje [**LB \_ INSERTSTRING**](lb-insertstring.md) no hace que se ordene una lista con el estilo [**SORT \_ de LB.**](list-box-styles.md) <br/> |
| [**LB \_ ITEMFROMPOINT**](lb-itemfrompoint.md)             | Obtiene el índice de base cero del elemento más cercano al punto especificado en un cuadro de lista.<br/>                                                                                                                                                                                   |
| [**LB \_ RESETCONTENT**](lb-resetcontent.md)               | Quita todos los elementos de un cuadro de lista. <br/>                                                                                                                                                                                                                                |
| [**LB \_ SELECTSTRING**](lb-selectstring.md)               | Busca en un cuadro de lista un elemento que comienza con los caracteres de una cadena especificada. <br/>                                                                                                                                                                            |
| [**LB \_ SELITEMRANGE**](lb-selitemrange.md)               | Selecciona o anula la selección de uno o varios elementos consecutivos en un cuadro de lista de selección múltiple. <br/>                                                                                                                                                                              |
| [**LB \_ SELITEMRANGEEX**](lb-selitemrangeex.md)           | Selecciona uno o varios elementos consecutivos en un cuadro de lista de selección múltiple. <br/>                                                                                                                                                                                           |
| [**LB \_ SETANCHORINDEX**](lb-setanchorindex.md)           | Establece el elemento delimitador, es decir, el elemento desde el que se inicia una selección múltiple. Una selección múltiple abarca todos los elementos desde el elemento delimitador hasta el elemento de careta.<br/>                                                                                                        |
| [**LB \_ SETCARETINDEX**](lb-setcaretindex.md)             | Establece el rectángulo de foco en el elemento situado en el índice especificado en un cuadro de lista de selección múltiple. Si el elemento no está visible, se desplaza a la vista. <br/>                                                                                                               |
| [**LB \_ SETCOLUMNWIDTH**](lb-setcolumnwidth.md)           | Establece el ancho, en píxeles, de todas las columnas de un cuadro de lista de varias columnas. <br/>                                                                                                                                                                                          |
| [**LB \_ SETCOUNT**](lb-setcount.md)                       | Establece el recuento de elementos de un cuadro de lista creado con el estilo [**LBS \_ NODATA**](list-box-styles.md) y no creado con el [**estilo \_ HASSTRINGS de LBS.**](list-box-styles.md) <br/>                                                          |
| [**LB \_ SETCURSEL**](lb-setcursel.md)                     | Selecciona una cadena y la desplaza a la vista, si es necesario. <br/>                                                                                                                                                                                                          |
| [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) | Establece el ancho, en píxeles, por el que se puede desplazar horizontalmente un cuadro de lista (el ancho desplazable). <br/>                                                                                                                                                               |
| [**LB \_ SETITEMDATA**](lb-setitemdata.md)                 | Establece un valor asociado al elemento especificado en un cuadro de lista. <br/>                                                                                                                                                                                            |
| [**LB \_ SETITEMHEIGHT**](lb-setitemheight.md)             | Establece el alto, en píxeles, de los elementos de un cuadro de lista. <br/>                                                                                                                                                                                                               |
| [**LB \_ SETLOCALE**](lb-setlocale.md)                     | Establece la configuración regional actual del cuadro de lista. <br/>                                                                                                                                                                                                                          |
| [**LB \_ SETSEL**](lb-setsel.md)                           | Selecciona una cadena en un cuadro de lista de selección múltiple. <br/>                                                                                                                                                                                                                |
| [**LB \_ SETTABSTOPS**](lb-settabstops.md)                 | Establece las posiciones de tabulación en un cuadro de lista. <br/>                                                                                                                                                                                                                        |
| [**LB \_ SETTOPINDEX**](lb-settopindex.md)                 | Garantiza que el elemento especificado en un cuadro de lista esté visible. <br/>                                                                                                                                                                                                         |



 

### <a name="notifications"></a>Notificaciones



| Tema                                             | Contenido                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LBN \_ DBLCLK](lbn-dblclk.md)                     | Notifica a la aplicación que el usuario ha hecho doble clic en un elemento de un cuadro de lista. <br/>                                                                                                                                                                                                                                         |
| [LBN \_ ERRSPACE](lbn-errspace.md)                 | Notifica a la aplicación que el cuadro de lista no puede asignar suficiente memoria para satisfacer una solicitud específica. <br/>                                                                                                                                                                                                                     |
| [LBN \_ KILLFOCUS](lbn-killfocus.md)               | Notifica a la aplicación que el cuadro de lista ha perdido el foco del teclado. <br/>                                                                                                                                                                                                                                                  |
| [LBN \_ SELCANCEL](lbn-selcancel.md)               | Notifica a la aplicación que el usuario ha cancelado la selección en un cuadro de lista. <br/>                                                                                                                                                                                                                                         |
| [LBN \_ SELCHANGE](lbn-selchange.md)               | Notifica a la aplicación que la selección de un cuadro de lista ha cambiado. <br/>                                                                                                                                                                                                                                                   |
| [LBN \_ SETFOCUS](lbn-setfocus.md)                 | Notifica a la aplicación que el cuadro de lista ha recibido el foco del teclado. <br/>                                                                                                                                                                                                                                              |
| [**WM \_ CHARTOITEM**](wm-chartoitem.md)           | Enviado por un cuadro de lista con el estilo [**\_ LBS WANTKEYBOARDINPUT**](list-box-styles.md) a su propietario en respuesta a un [**mensaje CHAR \_ de WM.**](/windows/desktop/inputdev/wm-char) <br/>                                                                                                                                        |
| [**WM \_ CTLCOLORLISTBOX**](wm-ctlcolorlistbox.md) | Se envía a la ventana primaria de un cuadro de lista antes de que el sistema dibuje el cuadro de lista. Al responder a este mensaje, la ventana primaria puede establecer los colores de texto y fondo del cuadro de lista mediante el identificador de contexto del dispositivo de presentación especificado. <br/>                                                                              |
| [**DELETEITEM de WM \_**](wm-deleteitem.md)           | Se envía al propietario de un cuadro de lista o cuadro combinado cuando se destruye el cuadro de lista o el cuadro combinado, o cuando los elementos se quitan mediante el mensaje [**LB \_ DELETESTRING,**](lb-deletestring.md) [**LB \_ RESETCONTENT,**](lb-resetcontent.md) [**CB \_ DELETESTRING**](cb-deletestring.md)o [**CB \_ RESETCONTENT.**](cb-resetcontent.md) <br/> |
| [**WM \_ VKEYTOITEM**](wm-vkeytoitem.md)           | Enviado por un cuadro de lista con el estilo [**\_ WANTKEYBOARDINPUT de LBS**](list-box-styles.md) a su propietario en respuesta a un [**mensaje DE WM \_ KEYDOWN.**](/windows/desktop/inputdev/wm-keydown) <br/>                                                                                                                                  |
| [DL \_ BEGINDRAG](dl-begindrag.md)                 | Notifica a la ventana primaria del cuadro de lista de arrastre que el usuario ha hecho clic en el botón izquierdo del mouse en un elemento. <br/>                                                                                                                                                                                                                   |
| [DL \_ CANCELDRAG](dl-canceldrag.md)               | Indica que el usuario ha cancelado una operación de arrastrar haciendo clic en el botón derecho del mouse o presionando la tecla ESC. <br/>                                                                                                                                                                                                          |
| [ARRASTRE \_ DE DL](dl-dragging.md)                   | Indica que el usuario ha movido el mouse al arrastrar un elemento. <br/>                                                                                                                                                                                                                                                        |
| [DL \_ DROPPED](dl-dropped.md)                     | Indica que el usuario ha completado una operación de arrastrar al soltar el botón izquierdo del mouse. <br/>                                                                                                                                                                                                                                 |



 

### <a name="structures"></a>Estructuras



| Tema                                        | Contenido                                                                                                                                                               |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) | Contiene información sobre un cuadro de lista eliminado o un elemento de cuadro combinado.<br/>                                                                                            |
| [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo)         | Contiene información sobre un evento de arrastre. El puntero a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) se pasa como el *parámetro lParam* del mensaje de la lista de arrastre. <br/> |



 

### <a name="constants"></a>Constantes



| Tema                                  | Contenido                                                                |
|----------------------------------------|-------------------------------------------------------------------------|
| [Estilos de cuadro de lista](list-box-styles.md) | Describe los estilos de ventana que definen un control de cuadro de lista. <br/> |



 

 

