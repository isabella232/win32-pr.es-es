---
description: En este tema se enumeran los principales elementos de programación utilizados con menús contextuales (contexto) y controladores de menús contextuales. Los controladores de menú contextual, que también se denominan controladores de menú contextual o de verbo, son un tipo de controlador de tipo de archivo.
ms.assetid: efd96a52-6455-40bc-9c21-65f89728e771
title: Referencia del menú contextual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cb1552c8f2f383b08984e9142e464b6831a3c8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275244"
---
# <a name="shortcut-menu-reference"></a>Referencia del menú contextual

En este tema se enumeran los principales elementos de programación utilizados con menús contextuales (contexto) y controladores de menús contextuales. Los controladores de menú contextual, que también se denominan controladores de menú contextual o de verbo, son un tipo de controlador de tipo de archivo.

## <a name="about-shortcut-menu-implemetation"></a>Acerca del menú contextual implementación

Se recomienda encarecidamente implementar un menú contextual con uno de los métodos estáticos Verb. Revise las siguientes instrucciones:

-   Para usar un método estático de verbo para implementar un menú contextual, vea la sección "personalizar un menú contextual mediante verbos estáticos" de [crear controladores de menú contextuales](context-menu-handlers.md).
-   Para obtener el comportamiento dinámico de los verbos estáticos en Windows 7 y versiones posteriores, vea el tema sobre cómo obtener el comportamiento dinámico para verbos estáticos en [crear controladores de menú contextuales](context-menu-handlers.md).
-   Para obtener información detallada sobre la implementación de verbos estáticos y los verbos dinámicos que se deben evitar, vea [elegir un verbo estático o dinámico para el menú contextual](shortcut-choose-method.md).
-   Si debe extender el menú contextual de un tipo de archivo registrando un verbo dinámico para el tipo de archivo, siga las instrucciones que se proporcionan en [Personalización de un menú contextual mediante verbos dinámicos](shortcut-menu-using-dynamic-verbs.md).

### <a name="interfaces"></a>Interfaces



| Tema                                        | Contenido                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)         | Expone métodos que crean o combinan un menú contextual asociado a un objeto de Shell.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)       | Expone métodos que crean o combinan un menú contextual asociado a un objeto de Shell. Extiende [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) agregando un método que permite a los objetos de cliente controlar los mensajes asociados a los elementos de menú dibujados por el propietario.<br/>                                                                                                                                                                                                                                                    |
| [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3)       | Expone métodos que crean o combinan un menú contextual asociado a un objeto de Shell. Permite a los objetos de cliente controlar los mensajes asociados a los elementos de menú dibujados por el propietario y extiende [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) aceptando un valor devuelto de ese control de mensajes.<br/>                                                                                                                                                                                                                         |
| [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)     | Expone un método que habilita la devolución de llamada de un menú contextual. Por ejemplo, para agregar un icono de escudo a un **MenuItem** que requiere elevación.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [**IContextMenuSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite) | Implementado por la vista de carpeta predeterminada creada con [**SHCreateShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview). Una implementación de [**IContextMenuSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite) admite [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)y [**TrackPopupMenu**](/windows/win32/api/winuser/nf-winuser-trackpopupmenu) , así como cualquier reenvío de mensajes necesario para esa función. Normalmente, **IContextMenuSite** también actualiza la barra de estado.<br/> |



 

### <a name="functions"></a>Functions



| Tema                                                            | Contenido                                                                                                                                |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)        | Crea un menú contextual para un grupo seleccionado de objetos de carpeta de archivos.<br/>                                                          |
| [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)                       | Define el prototipo de la función de devolución de llamada que recibe los mensajes de la implementación del menú contextual predeterminado del shell.<br/> |
| [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) | Crea un objeto que representa la implementación del menú contextual predeterminado del shell.<br/>                                           |



 

### <a name="structures"></a>Estructuras



| Tema                                                  | Contenido                                                                                                                                                                                                   |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo)     | Contiene la información necesaria para [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) para invocar un comando de menú contextual.<br/>                                                             |
| [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) | Contiene información extendida sobre un comando de menú contextual. Esta estructura es una versión extendida de [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) que permite el uso de valores Unicode.<br/> |
| [**DEFCONTEXTMENU**](/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu)               | Contiene información del menú contextual utilizada por [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).<br/>                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Menús contextuales y controladores de menú contextual](context-menu.md)
</dt> <dt>

[Elegir un verbo estático o dinámico para el menú contextual](shortcut-choose-method.md)
</dt> <dt>

[Verbos y asociaciones de archivo](fa-verbs.md)
</dt> <dt>

[Prácticas recomendadas para los controladores de menú contextual y varios verbos de selección](verbs-best-practices.md)
</dt> <dt>

[Crear controladores de menú contextual](context-menu-handlers.md)
</dt> <dt>

[Personalización de un menú contextual mediante verbos dinámicos](shortcut-menu-using-dynamic-verbs.md)
</dt> </dl>

 

 
