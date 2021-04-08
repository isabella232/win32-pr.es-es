---
title: Menús contextuales para su uso con especificadores de presentación
description: El Active Directory complementos MMC administrativos y el shell de Windows 2000 proporcionan un mecanismo para agregar un elemento al menú contextual que se muestra para los objetos de Active Directory Domain Services.
ms.assetid: 0b0691f5-321d-4f22-b39c-bc528db9e707
ms.tgt_platform: multiple
keywords:
- especificadores de presentación AD, menús contextuales para
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f28fbf703f17ea5c0fa7938365d485998be77e8d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995099"
---
# <a name="context-menus-for-use-with-display-specifiers"></a>Menús contextuales para su uso con especificadores de presentación

El Active Directory complementos MMC administrativos y el shell de Windows 2000 proporcionan un mecanismo para agregar un elemento al menú contextual que se muestra para los objetos de Active Directory Domain Services. Se puede Agregar un elemento de menú contextual implementando un servidor COM en proceso conocido como una *extensión de menú contextual*. También se puede Agregar un elemento de menú contextual que invoca a cualquier archivo iniciado con la API de [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) , como una aplicación o una dirección URL de la Página Web. Esto se conoce como un *elemento de menú contextual estático*.

## <a name="developer-audience"></a>Audiencia de los desarrolladores

En esta documentación se supone que el lector está familiarizado con el funcionamiento COM y el desarrollo de componentes mediante C++. En la actualidad, no se puede crear una Active Directory Domain Services extensión del menú contextual mediante Microsoft Visual Basic.

## <a name="extending-the-context-menu-with-a-context-menu-extension"></a>Extender el menú contextual con una extensión de menú contextual

Una extensión de menú contextual es un servidor COM en proceso que implementa determinadas interfaces y se registra con Active Directory Domain Services.

**Para crear e instalar una extensión de menú contextual**

1.  Cree el archivo DLL de extensión del menú contextual. Una extensión de menú contextual es un servidor COM en proceso que, como mínimo, implementa las interfaces [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) y [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) . Para obtener más información, vea [implementar el objeto com del menú contextual](implementing-the-context-menu-com-object.md).
2.  Instale la extensión de la hoja de menús contextuales en los equipos en los que se utiliza la extensión del menú contextual. Esto se logra mediante la creación de un paquete de Microsoft Windows Installer para el archivo DLL de extensión del menú contextual y la implementación del paquete correctamente mediante la Directiva de grupo. Para obtener más información, consulte [distribuir componentes](distributing-user-interface-components.md)de la interfaz de usuario.
3.  Registre la extensión del menú contextual en el registro de Windows y con Active Directory Domain Services. Para obtener más información, vea [registrar el objeto com del menú contextual en un especificador de presentación](registering-the-context-menu-com-object-in-a-display-specifier.md).

## <a name="extending-the-context-menu-with-a-static-context-menu-item"></a>Extender el menú contextual con un elemento de menú contextual estático

Un elemento de menú contextual estático se puede usar para invocar cualquier archivo iniciado con la API de [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) , como una aplicación o una dirección URL de la Página Web. Para ello, se debe registrar el elemento de menú contextual estático de una clase de objeto determinada para que el elemento de menú contextual estático se agregue al menú contextual de los objetos de esa clase. Para obtener más información, vea [registrar un elemento de menú contextual estático](registering-a-static-context-menu-item.md).

 

 