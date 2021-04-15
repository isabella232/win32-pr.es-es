---
title: Menús (menús y otros recursos)
description: En esta sección se describen los menús.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\menus.htm
keywords:
- recursos, menús
- menús, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c376aa1d2f55fa482ca7a2f98f57ae15236bf26b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421745"
---
# <a name="menus-menus-and-other-resources"></a>Menús (menús y otros recursos)

En esta sección se describen los menús y se explica cómo usarlos.

### <a name="in-this-section"></a>En esta sección



| Nombre                                 | Descripción                                                  |
|--------------------------------------|--------------------------------------------------------------|
| [Acerca de los menús](about-menus.md)       | Describe los menús.<br/>                                  |
| [Uso de los menús](using-menus.md)       | Proporciona ejemplos de código de tareas relacionadas con menús.<br/> |
| [Referencia de menú](menu-reference.md) | Contiene la referencia de la API.<br/>                       |



 

### <a name="menu-functions"></a>Funciones de menú



| Nombre                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)                                 | Anexa un nuevo elemento al final de la barra de menús, el menú desplegable, el submenú o el menú contextual especificados. Puede usar esta función para especificar el contenido, la apariencia y el comportamiento del elemento de menú. <br/>                                                                                                                                                                                                  |
| [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem)                           | Establece el estado del atributo de marca de verificación del elemento de menú especificado en activado o desactivado.<br/>                                                                                                                                                                                                                                                                                                      |
| [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem)                 | Comprueba un elemento de menú especificado y lo convierte en un elemento de radio. Al mismo tiempo, la función borra todos los demás elementos de menú del grupo asociado y borra el indicador de tipo de elemento de radio de esos elementos.<br/>                                                                                                                                                                                                    |
| [**CreateMenu**](/windows/desktop/api/Winuser/nf-winuser-createmenu)                                 | Crea un menú. El menú está inicialmente vacío, pero se puede rellenar con elementos de menú mediante las funciones [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)y [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) . <br/>                                                                                                                                                                        |
| [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu)                       | Crea un menú desplegable, un submenú o un menú contextual. El menú está inicialmente vacío. Puede insertar o anexar elementos de menú mediante la función [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) . También puede usar la función [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) para insertar elementos de menú y la función [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) para anexar elementos de menú.<br/>                                                  |
| [**DeleteMenu**](/windows/desktop/api/Winuser/nf-winuser-deletemenu)                                 | Elimina un elemento del menú especificado. Si el elemento de menú abre un menú o un submenú, esta función destruye el identificador del menú o submenú y libera la memoria utilizada por el menú o submenú. <br/>                                                                                                                                                                                                     |
| [**DestroyMenu**](/windows/desktop/api/Winuser/nf-winuser-destroymenu)                               | Destruye el menú especificado y libera cualquier memoria que ocupe el menú. <br/>                                                                                                                                                                                                                                                                                                                          |
| [**DrawMenuBar**](/windows/desktop/api/Winuser/nf-winuser-drawmenubar)                               | Vuelve a dibujar la barra de menús de la ventana especificada. Si la barra de menús cambia después de que el sistema haya creado la ventana, se debe llamar a esta función para dibujar la barra de menús modificada. <br/>                                                                                                                                                                                                                         |
| [**EnableMenuItem**](/windows/desktop/api/Winuser/nf-winuser-enablemenuitem)                         | Habilita, deshabilita o atenúa el elemento de menú especificado. <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**EndMenu**](/windows/desktop/api/Winuser/nf-winuser-endmenu)                                       | Finaliza el menú activo del subproceso que realiza la llamada.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**GetMenu**](/windows/desktop/api/Winuser/nf-winuser-getmenu)                                       | Recupera un identificador del menú asignado a la ventana especificada. <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**GetMenuBarInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenubarinfo)                         | Recupera información sobre la barra de menús especificada.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**GetMenuCheckMarkDimensions**](/windows/desktop/api/Winuser/nf-winuser-getmenucheckmarkdimensions) | Recupera las dimensiones del mapa de bits predeterminado de la marca de verificación. El sistema muestra este mapa de bits junto a los elementos de menú seleccionados. Antes de llamar a la función [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) para reemplazar el mapa de bits de la marca de verificación predeterminada para un elemento de menú, una aplicación debe determinar el tamaño correcto del mapa de bits llamando a [**GetMenuCheckMarkDimensions**](/windows/desktop/api/Winuser/nf-winuser-getmenucheckmarkdimensions). <br/> |
| [**GetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-getmenudefaultitem)                 | Determina el elemento de menú predeterminado en el menú especificado.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**GetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuinfo)                               | Recupera información sobre un menú especificado.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**GetMenuItemCount**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemcount)                     | Recupera el número de elementos del menú especificado. <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**GetMenuItemID**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemid)                           | Recupera el identificador de elemento de menú de un elemento de menú situado en la posición especificada de un menú. <br/>                                                                                                                                                                                                                                                                                                    |
| [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)                       | Recupera información sobre un elemento de menú.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| [**GetMenuItemRect**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemrect)                       | Recupera el rectángulo delimitador del elemento de menú especificado.<br/>                                                                                                                                                                                                                                                                                                                                      |
| [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate)                             | Recupera las marcas de menú asociadas al elemento de menú especificado. Si el elemento de menú abre un submenú, esta función también devuelve el número de elementos del submenú. <br/>                                                                                                                                                                                                                                |
| [**GetMenuString**](/windows/desktop/api/Winuser/nf-winuser-getmenustringa)                           | Copia la cadena de texto del elemento de menú especificado en el búfer especificado. <br/>                                                                                                                                                                                                                                                                                                                      |
| [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)                                 | Recupera un identificador del menú desplegable o submenú activado por el elemento de menú especificado. <br/>                                                                                                                                                                                                                                                                                                         |
| [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)                           | Permite que la aplicación tenga acceso al menú ventana (también conocido como menú del sistema o menú de control) para copiar y modificar. <br/>                                                                                                                                                                                                                                                                  |
| [**HiliteMenuItem**](/windows/desktop/api/Winuser/nf-winuser-hilitemenuitem)                         | Resalta o quita el resaltado de un elemento de una barra de menús. <br/>                                                                                                                                                                                                                                                                                                                                |
| [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)                         | Inserta un nuevo elemento de menú en la posición especificada de un menú.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**IsMenu**](/windows/desktop/api/Winuser/nf-winuser-ismenu)                                         | Determina si un identificador es un controlador de menú. <br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua)                                     | Carga el recurso de menú especificado del archivo ejecutable (. exe) asociado a una instancia de la aplicación. <br/>                                                                                                                                                                                                                                                                                        |
| [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)                     | Carga la plantilla de menú especificada en la memoria. <br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**MenuItemFromPoint**](/windows/desktop/api/Winuser/nf-winuser-menuitemfrompoint)                   | Determina qué elemento de menú, si existe, está en la ubicación especificada.<br/>                                                                                                                                                                                                                                                                                                                                  |
| [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)                                 | Cambia un elemento de menú existente. Esta función se usa para especificar el contenido, la apariencia y el comportamiento del elemento de menú. <br/>                                                                                                                                                                                                                                                                           |
| [**RemoveMenu**](/windows/desktop/api/Winuser/nf-winuser-removemenu)                                 | Elimina un elemento de menú o desasocia un submenú del menú especificado. Si el elemento de menú abre un menú desplegable o un submenú, [**RemoveMenu**](/windows/desktop/api/Winuser/nf-winuser-removemenu) no destruye el menú ni su identificador, lo que permite volver a usar el menú. Antes de llamar a esta función, la función [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) debe recuperar un identificador del menú desplegable o submenú. <br/>                         |
| [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu)                                       | Asigna un nuevo menú a la ventana especificada. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**SetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-setmenudefaultitem)                 | Establece el elemento de menú predeterminado para el menú especificado.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)                               | Establece la información de un menú especificado.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps)                 | Asocia el mapa de bits especificado a un elemento de menú. Si el elemento de menú está activado o desactivado, el sistema muestra el mapa de bits adecuado junto al elemento de menú. <br/>                                                                                                                                                                                                                                   |
| [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa)                       | Cambia la información sobre un elemento de menú.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)                         | Muestra un menú contextual en la ubicación especificada y realiza un seguimiento de la selección de elementos en el menú. El menú contextual puede aparecer en cualquier parte de la pantalla.<br/>                                                                                                                                                                                                                                             |
| [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)                     | Muestra un menú contextual en la ubicación especificada y realiza un seguimiento de la selección de elementos en el menú contextual. El menú contextual puede aparecer en cualquier parte de la pantalla.<br/>                                                                                                                                                                                                                                    |



 

La siguiente función está obsoleta.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nombre</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-insertmenua"><strong>InsertMenu</strong></a></td>
<td>Inserta un nuevo elemento de menú en un menú y mueve otros elementos hacia abajo en el menú.
<blockquote>
[!Note]<br />
La función <a href="/windows/desktop/api/Winuser/nf-winuser-insertmenua"><strong>InsertMenu</strong></a> ha reemplazado a la función <a href="/windows/desktop/api/Winuser/nf-winuser-insertmenuitema"><strong>InsertMenuItem</strong></a> . Sin embargo, puede seguir usando <strong>InsertMenu</strong>si no necesita ninguna de las características extendidas de <strong>InsertMenuItem</strong>.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="menu-notifications"></a>Notificaciones de menú



| Nombre                                                  | Descripción                                                                                                                                                                          |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**comando de WM \_**](wm-command.md)                     | Se envía cuando el usuario selecciona un elemento de comando de un menú, cuando un control envía un mensaje de notificación a su ventana primaria o cuando se traduce una pulsación de tecla de aceleración. <br/> |
| [**CONTEXTMENU de WM \_**](wm-contextmenu.md)             | Informa a una ventana de que el usuario hizo *clic con el* botón secundario del mouse en la ventana.<br/>                                                                            |
| [**ENTERMENULOOP de WM \_**](wm-entermenuloop.md)         | Informa al procedimiento de ventana principal de una aplicación que se ha especificado un bucle modal de menú. <br/>                                                                                  |
| [**EXITMENULOOP de WM \_**](wm-exitmenuloop.md)           | Informa al procedimiento de ventana principal de una aplicación que se ha salido de un bucle modal de menú. <br/>                                                                                   |
| [**GETTITLEBARINFOEX de WM \_**](wm-gettitlebarinfoex.md) | Se envía para solicitar información de la barra de título extendida. Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .<br/>                                  |
| [**MENUCOMMAND de WM \_**](wm-menucommand.md)             | Se envía cuando el usuario realiza una selección en un menú. <br/>                                                                                                                        |
| [**MENUDRAG de WM \_**](wm-menudrag.md)                   | Se envía al propietario de un menú de arrastrar y colocar cuando el usuario arrastra un elemento de menú. <br/>                                                                                               |
| [**MENUGETOBJECT de WM \_**](wm-menugetobject.md)         | Se envía al propietario de un menú de arrastrar y colocar cuando el cursor del Mouse entra en un elemento de menú o se mueve desde el centro del elemento hasta la parte superior o inferior del elemento. <br/>                |
| [**MENURBUTTONUP de WM \_**](wm-menurbuttonup.md)         | Se envía cuando el usuario suelta el botón secundario del mouse mientras el cursor está en un elemento de menú. <br/>                                                                                   |
| [**NEXTMENU de WM \_**](wm-nextmenu.md)                   | Se envía a una aplicación cuando se usa la tecla de dirección derecha o izquierda para cambiar entre la barra de menús y el menú del sistema. <br/>                                                      |
| [**UNINITMENUPOPUP de WM \_**](wm-uninitmenupopup.md)     | Se envía cuando se destruye un menú desplegable o un submenú. <br/>                                                                                                                |



 

### <a name="menu-structures"></a>Estructuras de menú



| Nombre                                                       | Descripción                                                                                                                                                     |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu)                         | Contiene información sobre el menú que se va a activar. <br/>                                                                                                |
| [**MENUBARINFO**](/windows/win32/api/winuser/ns-winuser-menubarinfo)                         | Contiene información de la barra de menús.<br/>                                                                                                                       |
| [**\_encabezado de plantilla MENUEX \_**](menuex-template-header.md) | Define el encabezado de una plantilla de menú extendida. Esta definición de estructura solo es para explicación; no se encuentra en ningún archivo de encabezado estándar. <br/> |
| [**\_elemento de plantilla MENUEX \_**](menuex-template-item.md)     | Define un elemento de menú en una plantilla de menú extendida. Esta definición de estructura solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.<br/>  |
| [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)             | Contiene información sobre el menú en el que se encuentra el cursor del mouse.<br/>                                                                                     |
| [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo)                               | Contiene información sobre un menú.<br/>                                                                                                                   |
| [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)                       | Contiene información sobre un elemento de menú. <br/>                                                                                                             |
| [**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)               | Define un elemento de menú en una plantilla de menú. <br/>                                                                                                             |
| [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader)   | Define el encabezado de una plantilla de menú. Una plantilla de menú completa consta de un encabezado y una o varias listas de elementos de menú. <br/>                              |
| [**TPMPARAMS**](/windows/win32/api/winuser/ns-winuser-tpmparams)                             | Contiene parámetros extendidos para la función [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .<br/>                                                          |



 

 

