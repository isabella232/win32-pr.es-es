---
title: Cuadro de lista
description: Esta sección contiene información sobre los elementos de programación utilizados con cuadros de lista. Un cuadro de lista es una ventana de control que contiene una lista sencilla de elementos entre los que el usuario puede elegir.
ms.assetid: vs|controls|~\controls\listboxes\listboxes.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fda5e6bb2d1d4c3c4f23e506900257c1b2ce64b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149650"
---
# <a name="list-box"></a>Cuadro de lista

Esta sección contiene información sobre los elementos de programación utilizados con cuadros de lista. Un cuadro de lista es una ventana de control que contiene una lista sencilla de elementos entre los que el usuario puede elegir. Para listas más complejas, utilice en su lugar la [vista de lista](list-view-control-reference.md) .

### <a name="overviews"></a>Temas de introducción



| Tema                                    | Contenido                                                              |
|------------------------------------------|-----------------------------------------------------------------------|
| [Acerca de los cuadros de lista](about-list-boxes.md) | Describe las características del cuadro de lista.<br/>                               |
| [Usar cuadros de lista](using-list-boxes.md) | Explica cómo realizar tareas asociadas a cuadros de lista. <br/> |



 

### <a name="functions"></a>Functions



| Tema                                    | Contenido                                                                                                                |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)         | Reemplaza el contenido de un cuadro de lista con los nombres de los subdirectorios y los archivos de un directorio especificado.<br/> |
| [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) | Recupera la selección actual de un cuadro de lista de selección única.<br/>                                            |
| [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert)         | Dibuja el icono de inserción en la ventana primaria del cuadro de lista de arrastre especificado. <br/>                                  |
| [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo) | Recupera información sobre el cuadro de lista especificado.<br/>                                                          |
| [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt)     | Recupera el índice del elemento en el punto especificado de un cuadro de lista. <br/>                                       |
| [**MakeDragList**](/windows/desktop/api/Commctrl/nf-commctrl-makedraglist)     | Cambia el cuadro de lista de selección única especificado a un cuadro de lista de arrastre. <br/>                                         |



 

### <a name="messages"></a>error de Hadoop



| Tema                                                     | Contenido                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LB \_ ADDFILE**](lb-addfile.md)                         | Agrega el nombre de archivo especificado a un cuadro de lista que contiene una lista de directorios. <br/>                                                                                                                                                                                     |
| [**LB \_ ADDSTRING**](lb-addstring.md)                     | Agrega una cadena a un cuadro de lista. <br/>                                                                                                                                                                                                                                      |
| [**LB \_ DELETESTRING**](lb-deletestring.md)               | Elimina una cadena de un cuadro de lista. <br/>                                                                                                                                                                                                                                   |
| [**DIR de LB \_**](lb-dir.md)                                 | Agrega nombres a la lista mostrada por un cuadro de lista. <br/>                                                                                                                                                                                                                   |
| [**LB \_ FINDSTRING**](lb-findstring.md)                   | Busca la primera cadena de un cuadro de lista que comienza con la cadena especificada. <br/>                                                                                                                                                                                       |
| [**LB \_ FindExactString con**](lb-findstringexact.md)         | Busca la primera cadena del cuadro de lista que coincide exactamente con la cadena especificada, salvo que la búsqueda no distingue entre mayúsculas y minúsculas. <br/>                                                                                                                                          |
| [**LB \_ GETANCHORINDEX**](lb-getanchorindex.md)           | Obtiene el índice del elemento delimitador, que es el elemento desde el que se inicia una selección múltiple. <br/>                                                                                                                                                                       |
| [**LB \_ GETCARETINDEX**](lb-getcaretindex.md)             | Recupera el índice del elemento que tiene el rectángulo de foco en un cuadro de lista de selección múltiple. El elemento puede estar o no seleccionado. <br/>                                                                                                                               |
| [**LB \_ GETCOUNT**](lb-getcount.md)                       | Obtiene el número de elementos de un cuadro de lista. <br/>                                                                                                                                                                                                                           |
| [**LB \_ GETCURSEL**](lb-getcursel.md)                     | Obtiene el índice del elemento seleccionado actualmente, si existe, en un cuadro de lista de selección única. <br/>                                                                                                                                                                            |
| [**LB \_ GETHORIZONTALEXTENT**](lb-gethorizontalextent.md) | Obtiene el ancho, en píxeles, que un cuadro de lista se puede desplazar horizontalmente (el ancho desplazable) si el cuadro de lista tiene una barra de desplazamiento horizontal. <br/>                                                                                                                       |
| [**LB \_ GETITEMDATA**](lb-getitemdata.md)                 | Obtiene el valor definido por la aplicación asociado al elemento de cuadro de lista especificado. <br/>                                                                                                                                                                                   |
| [**LB \_ GETITEMHEIGHT**](lb-getitemheight.md)             | Obtiene el alto de los elementos de un cuadro de lista. <br/>                                                                                                                                                                                                                           |
| [**LB \_ GETITEMRECT**](lb-getitemrect.md)                 | Obtiene las dimensiones del rectángulo que delimita un elemento de cuadro de lista tal como se muestra actualmente en el cuadro de lista. <br/>                                                                                                                                                    |
| [**LB \_ GETLISTBOXINFO**](lb-getlistboxinfo.md)           | Obtiene el número de elementos por columna de un cuadro de lista especificado. <br/>                                                                                                                                                                                                      |
| [**equilibro \_ de lb**](lb-getlocale.md)                     | Obtiene la configuración regional actual del cuadro de lista. <br/>                                                                                                                                                                                                                          |
| [**LB \_ GETSEL**](lb-getsel.md)                           | Obtiene el estado de selección de un elemento. <br/>                                                                                                                                                                                                                              |
| [**LB \_ GETSELCOUNT**](lb-getselcount.md)                 | Obtiene el número total de elementos seleccionados en un cuadro de lista de selección múltiple. <br/>                                                                                                                                                                                         |
| [**LB \_ GETSELITEMS**](lb-getselitems.md)                 | Rellena un búfer con una matriz de enteros que especifican el número de elemento de los elementos seleccionados en un cuadro de lista de selección múltiple. <br/>                                                                                                                                        |
| [**\_apgettext GETTEXT**](lb-gettext.md)                         | Obtiene una cadena de un cuadro de lista. <br/>                                                                                                                                                                                                                                    |
| [**LB \_ GETTEXTLEN**](lb-gettextlen.md)                   | Obtiene la longitud de una cadena en un cuadro de lista. <br/>                                                                                                                                                                                                                        |
| [**LB \_ GETTOPINDEX**](lb-gettopindex.md)                 | Obtiene el índice del primer elemento visible de un cuadro de lista. <br/>                                                                                                                                                                                                           |
| [**' LB \_ INITSTORAGE**](lb-initstorage.md)                 | Asigna memoria para almacenar los elementos del cuadro de lista. Este mensaje se usa antes de que una aplicación agregue un gran número de elementos a un cuadro de lista.<br/>                                                                                                                                |
| [**LB \_ INSERTSTRING**](lb-insertstring.md)               | Inserta una cadena o datos de elemento en un cuadro de lista. A diferencia del mensaje de [**lb en lb \_**](lb-addstring.md) , el mensaje [**lb \_ INSERTSTRING**](lb-insertstring.md) no hace que se ordene una lista con el estilo de [**\_ ordenación lbs**](list-box-styles.md) . <br/> |
| [**LB \_ ITEMFROMPOINT**](lb-itemfrompoint.md)             | Obtiene el índice de base cero del elemento más próximo al punto especificado en un cuadro de lista.<br/>                                                                                                                                                                                   |
| [**LB \_ RESETCONTENT**](lb-resetcontent.md)               | Quita todos los elementos de un cuadro de lista. <br/>                                                                                                                                                                                                                                |
| [**LB \_ SELECTSTRING**](lb-selectstring.md)               | Busca un elemento que empiece con los caracteres de una cadena especificada en un cuadro de lista. <br/>                                                                                                                                                                            |
| [**LB \_ SELITEMRANGE**](lb-selitemrange.md)               | Selecciona o anula la selección de uno o varios elementos consecutivos en un cuadro de lista de selección múltiple. <br/>                                                                                                                                                                              |
| [**LB \_ SELITEMRANGEEX**](lb-selitemrangeex.md)           | Selecciona uno o más elementos consecutivos en un cuadro de lista de selección múltiple. <br/>                                                                                                                                                                                           |
| [**LB \_ SETANCHORINDEX**](lb-setanchorindex.md)           | Establece el elemento de delimitador, que es el elemento desde el que se inicia una selección múltiple. Una selección múltiple abarca todos los elementos del elemento delimitador hasta el elemento del símbolo de intercalación.<br/>                                                                                                        |
| [**LB \_ SETCARETINDEX**](lb-setcaretindex.md)             | Establece el rectángulo de foco en el elemento en el índice especificado de un cuadro de lista de selección múltiple. Si el elemento no está visible, se desplaza a la vista. <br/>                                                                                                               |
| [**LB \_ SETCOLUMNWIDTH**](lb-setcolumnwidth.md)           | Establece el ancho, en píxeles, de todas las columnas de un cuadro de lista de varias columnas. <br/>                                                                                                                                                                                          |
| [**LB \_ SETCOUNT**](lb-setcount.md)                       | Establece el recuento de elementos de un cuadro de lista creado con el estilo [**lbs \_ NoData**](list-box-styles.md) y no se creó con el estilo [**lb \_ HASSTRINGS**](list-box-styles.md) . <br/>                                                          |
| [**LB \_ SETCURSEL**](lb-setcursel.md)                     | Selecciona una cadena y la desplaza a la vista, si es necesario. <br/>                                                                                                                                                                                                          |
| [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) | Establece el ancho, en píxeles, por el que se puede desplazar un cuadro de lista horizontalmente (el ancho desplazable). <br/>                                                                                                                                                               |
| [**LB \_ SETITEMDATA**](lb-setitemdata.md)                 | Establece un valor que está asociado al elemento especificado en un cuadro de lista. <br/>                                                                                                                                                                                            |
| [**LB \_ SETITEMHEIGHT**](lb-setitemheight.md)             | Establece el alto, en píxeles, de los elementos de un cuadro de lista. <br/>                                                                                                                                                                                                               |
| [**LB \_ SETLOCALE**](lb-setlocale.md)                     | Establece la configuración regional actual del cuadro de lista. <br/>                                                                                                                                                                                                                          |
| [**LB \_ SETSEL**](lb-setsel.md)                           | Selecciona una cadena en un cuadro de lista de selección múltiple. <br/>                                                                                                                                                                                                                |
| [**LB \_ SETTABSTOPS**](lb-settabstops.md)                 | Establece las posiciones de tabulación en un cuadro de lista. <br/>                                                                                                                                                                                                                        |
| [**LB \_ SETTOPINDEX**](lb-settopindex.md)                 | Garantiza que el elemento especificado en un cuadro de lista está visible. <br/>                                                                                                                                                                                                         |



 

### <a name="notifications"></a>Notificaciones



| Tema                                             | Contenido                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LBN \_ DBLCLK](lbn-dblclk.md)                     | Notifica a la aplicación que el usuario ha hace doble clic en un elemento de un cuadro de lista. <br/>                                                                                                                                                                                                                                         |
| [LBN \_ ERRSPACE](lbn-errspace.md)                 | Notifica a la aplicación que el cuadro de lista no puede asignar memoria suficiente para satisfacer una solicitud concreta. <br/>                                                                                                                                                                                                                     |
| [LBN \_ KILLFOCUS](lbn-killfocus.md)               | Notifica a la aplicación que el cuadro de lista ha perdido el foco de teclado. <br/>                                                                                                                                                                                                                                                  |
| [LBN \_ SELCANCEL](lbn-selcancel.md)               | Notifica a la aplicación que el usuario ha cancelado la selección en un cuadro de lista. <br/>                                                                                                                                                                                                                                         |
| [LBN \_ SELCHANGE](lbn-selchange.md)               | Notifica a la aplicación que la selección de un cuadro de lista ha cambiado. <br/>                                                                                                                                                                                                                                                   |
| [LBN ( \_ SETFOCUS)](lbn-setfocus.md)                 | Notifica a la aplicación que el cuadro de lista ha recibido el foco de teclado. <br/>                                                                                                                                                                                                                                              |
| [**CHARTOITEM de WM \_**](wm-chartoitem.md)           | Se envía mediante un cuadro de lista con el estilo [**lb \_ WANTKEYBOARDINPUT**](list-box-styles.md) a su propietario en respuesta a un mensaje de tipo [**\_ Char de WM**](/windows/desktop/inputdev/wm-char) . <br/>                                                                                                                                        |
| [**CTLCOLORLISTBOX de WM \_**](wm-ctlcolorlistbox.md) | Se envía a la ventana primaria de un cuadro de lista antes de que el sistema dibuje el cuadro de lista. Al responder a este mensaje, la ventana primaria puede establecer los colores de texto y de fondo del cuadro de lista utilizando el identificador de contexto de dispositivo de pantalla especificado. <br/>                                                                              |
| [**WM \_ DELETEITEM**](wm-deleteitem.md)           | Se envía al propietario de un cuadro de lista o cuadro combinado cuando se destruye el cuadro de lista o el cuadro combinado o cuando los elementos se quitan mediante el mensaje [**lb \_ DELETESTRING**](lb-deletestring.md), [**lb \_ RESETCONTENT**](lb-resetcontent.md), [**CB \_ DELETESTRING**](cb-deletestring.md)o [**CB \_ RESETCONTENT**](cb-resetcontent.md) . <br/> |
| [**VKEYTOITEM de WM \_**](wm-vkeytoitem.md)           | Enviado por un cuadro de lista con el estilo [**lb \_ WANTKEYBOARDINPUT**](list-box-styles.md) a su propietario en respuesta a un mensaje de [**\_ KEYDOWN de WM**](/windows/desktop/inputdev/wm-keydown) . <br/>                                                                                                                                  |
| [BEGINDRAG de DL \_](dl-begindrag.md)                 | Notifica a la ventana primaria del cuadro de lista de arrastre que el usuario hizo clic con el botón primario del mouse en un elemento. <br/>                                                                                                                                                                                                                   |
| [CANCELDRAG de DL \_](dl-canceldrag.md)               | Indica que el usuario ha cancelado una operación de arrastrar haciendo clic con el botón secundario del mouse o presionando la tecla ESC. <br/>                                                                                                                                                                                                          |
| [\_arrastrar DL](dl-dragging.md)                   | Indica que el usuario ha desplazado el mouse mientras arrastra un elemento. <br/>                                                                                                                                                                                                                                                        |
| [DL \_ quitada](dl-dropped.md)                     | Indica que el usuario ha completado una operación de arrastre soltando el botón primario del mouse. <br/>                                                                                                                                                                                                                                 |



 

### <a name="structures"></a>Estructuras



| Tema                                        | Contenido                                                                                                                                                               |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DELETEITEMSTRUCT (**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) | Contiene información sobre un elemento de cuadro combinado o cuadro de lista eliminado.<br/>                                                                                            |
| [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo)         | Contiene información sobre un evento de arrastre. El puntero a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) se pasa como el parámetro *lParam* del mensaje de la lista de arrastre. <br/> |



 

### <a name="constants"></a>Constantes



| Tema                                  | Contenido                                                                |
|----------------------------------------|-------------------------------------------------------------------------|
| [Estilos de cuadro de lista](list-box-styles.md) | Describe los estilos de ventana que definen un control de cuadro de lista. <br/> |



 

 

