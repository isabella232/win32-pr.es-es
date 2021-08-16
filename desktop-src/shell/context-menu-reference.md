---
description: En este tema se enumeran los elementos de programación principales utilizados con los menús contextuales y los controladores de menús contextuales. Los controladores de menús contextuales, que también se conocen como controladores de menú contextual o controladores de verbos, son un tipo de controlador de tipo de archivo.
ms.assetid: efd96a52-6455-40bc-9c21-65f89728e771
title: Referencia del menú contextual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f80b62b88750200456da76c22017b3f18fbba584272dc028809771c807ad85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090775"
---
# <a name="shortcut-menu-reference"></a>Referencia del menú contextual

En este tema se enumeran los elementos de programación principales utilizados con los menús contextuales y los controladores de menús contextuales. Los controladores de menús contextuales, que también se conocen como controladores de menú contextual o controladores de verbos, son un tipo de controlador de tipo de archivo.

## <a name="about-shortcut-menu-implemetation"></a>Acerca de la aplicación del menú contextual

Se recomienda encarecidamente implementar un menú contextual mediante uno de los métodos de verbo estático. Revise las instrucciones siguientes:

-   Para usar un método de verbo estático para implementar un menú contextual, vea la sección "Personalización de un menú contextual mediante verbos estáticos" de Crear controladores de [menús contextuales.](context-menu-handlers.md)
-   Para obtener el comportamiento dinámico de verbos estáticos en Windows 7 y versiones posteriores, vea "Getting Dynamic Behavior for Static Verbs" (Obtener comportamiento dinámico para verbos estáticos) en [Creating Shortcut Menu Handlers](context-menu-handlers.md).
-   Para obtener más información sobre la implementación de verbos estáticos y los verbos dinámicos que se deben evitar, vea Elegir un verbo estático o dinámico [para el menú contextual.](shortcut-choose-method.md)
-   Si debe extender el menú contextual de un tipo de archivo mediante el registro de un verbo dinámico para el tipo de archivo, siga las instrucciones proporcionadas en Personalización de un menú contextual mediante [verbos dinámicos.](shortcut-menu-using-dynamic-verbs.md)

### <a name="interfaces"></a>Interfaces



| Tema                                        | Contenido                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)         | Expone métodos que crean o combinan un menú contextual asociado a un objeto shell.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)       | Expone métodos que crean o combinan un menú contextual asociado a un objeto Shell. Extiende [**IContextMenu agregando**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) un método que permite a los objetos de cliente controlar los mensajes asociados a los elementos de menú dibujados por el propietario.<br/>                                                                                                                                                                                                                                                    |
| [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3)       | Expone métodos que crean o combinan un menú contextual asociado a un objeto shell. Permite que los objetos de cliente controlen los mensajes asociados a los elementos de menú dibujados por el propietario y extiende [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) aceptando un valor devuelto de ese control de mensajes.<br/>                                                                                                                                                                                                                         |
| [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)     | Expone un método que habilita la devolución de llamada de un menú contextual. Por ejemplo, para agregar un icono de escudo a un **elemento menuItem** que requiere elevación.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [**IContextMenuSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite) | Implementado por la vista de carpeta predeterminada creada mediante [**SHCreateShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview). Una implementación de [**IContextMenuSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite) admite [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)y [**TrackPopupMenu**](/windows/win32/api/winuser/nf-winuser-trackpopupmenu) y cualquier reenvío de mensajes necesario para esa función. **IContextMenuSite normalmente** también actualiza la barra de estado.<br/> |



 

### <a name="functions"></a>Functions



| Tema                                                            | Contenido                                                                                                                                |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)        | Crea un menú contextual para un grupo seleccionado de objetos de carpeta de archivos.<br/>                                                          |
| [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)                       | Define el prototipo de la función de devolución de llamada que recibe mensajes de la implementación del menú contextual predeterminado del shell.<br/> |
| [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) | Crea un objeto que representa la implementación del menú contextual predeterminado del Shell.<br/>                                           |



 

### <a name="structures"></a>Estructuras



| Tema                                                  | Contenido                                                                                                                                                                                                   |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo)     | Contiene información necesaria para [**que IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) invoque un comando de menú contextual.<br/>                                                             |
| [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) | Contiene información extendida sobre un comando de menú contextual. Esta estructura es una versión extendida de [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) que permite el uso de valores Unicode.<br/> |
| [**DEFCONTEXTMENU**](/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu)               | Contiene información del menú contextual utilizada [**por SHCreateDefaultContextMenu.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)<br/>                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Menús contextuales y controladores de menús contextuales](context-menu.md)
</dt> <dt>

[Elegir un verbo estático o dinámico para el menú contextual](shortcut-choose-method.md)
</dt> <dt>

[Verbos y asociaciones de archivo](fa-verbs.md)
</dt> <dt>

[Procedimientos recomendados para controladores de menús contextuales y verbos de selección múltiple](verbs-best-practices.md)
</dt> <dt>

[Creación de controladores de menús contextuales](context-menu-handlers.md)
</dt> <dt>

[Personalizar un menú contextual mediante verbos dinámicos](shortcut-menu-using-dynamic-verbs.md)
</dt> </dl>

 

 
