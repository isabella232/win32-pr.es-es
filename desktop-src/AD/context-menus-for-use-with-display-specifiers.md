---
title: Menús contextuales para su uso con especificadores de visualización
description: Los Active Directory mmc administrativos y el shell de Windows 2000 proporcionan un mecanismo para agregar un elemento al menú contextual que se muestra para los objetos de Active Directory Domain Services.
ms.assetid: 0b0691f5-321d-4f22-b39c-bc528db9e707
ms.tgt_platform: multiple
keywords:
- mostrar especificadores de AD , menús contextuales para
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b55b530797f1ac43456606d0fecf30e7641bf10399fb3c074135a3e0c49fd0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118021712"
---
# <a name="context-menus-for-use-with-display-specifiers"></a>Menús contextuales para su uso con especificadores de visualización

Los Active Directory mmc administrativos y el shell de Windows 2000 proporcionan un mecanismo para agregar un elemento al menú contextual que se muestra para los objetos de Active Directory Domain Services. Se puede agregar un elemento de menú contextual implementando un servidor COM en proceso conocido como extensión *de menú contextual.* También se puede agregar un elemento de menú contextual que invoque cualquier archivo iniciado con [**shellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) API, como una dirección URL de aplicación o página web. Esto se conoce como un elemento *de menú contextual estático.*

## <a name="developer-audience"></a>Audiencia de los desarrolladores

En esta documentación se da por supuesto que el lector está familiarizado con el desarrollo de componentes y operaciones COM mediante C++. Actualmente no es posible crear una extensión de menú Active Directory Domain Services contextual mediante Microsoft Visual Basic.

## <a name="extending-the-context-menu-with-a-context-menu-extension"></a>Extensión del menú contextual con una extensión de menú contextual

Una extensión de menú contextual es un servidor COM en proceso que implementa ciertas interfaces y se registra con Active Directory Domain Services.

**Para crear e instalar una extensión de menú contextual**

1.  Cree el archivo DLL de extensión del menú contextual. Una extensión de menú contextual es un servidor COM en proceso que, como mínimo, implementa las interfaces [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) [**e IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) Para obtener más información, vea [Implementing the Context Menu COM Object](implementing-the-context-menu-com-object.md).
2.  Instale la extensión de hoja de menú contextual en los equipos donde se usa la extensión de menú contextual. Esto se logra mediante la creación de un paquete de Microsoft Windows Installer para el archivo DLL de extensión del menú contextual y la implementación del paquete correctamente mediante la directiva de grupo. Para obtener más información, vea [Distribución de Interfaz de usuario componentes](distributing-user-interface-components.md).
3.  Registre la extensión de menú contextual en Windows registro y con Active Directory Domain Services. Para obtener más información, [vea Registrar el objeto COM del menú contextual en un especificador de presentación.](registering-the-context-menu-com-object-in-a-display-specifier.md)

## <a name="extending-the-context-menu-with-a-static-context-menu-item"></a>Extender el menú contextual con un elemento de menú contextual estático

Se puede usar un elemento de menú contextual estático para invocar cualquier archivo iniciado con [**shellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) API, como una dirección URL de aplicación o página web. Para ello, se debe registrar el elemento de menú contextual estático de una clase de objeto determinada para que el elemento de menú contextual estático se agrega al menú contextual de objetos de esa clase. Para obtener más información, vea [Registrar un elemento de menú contextual estático.](registering-a-static-context-menu-item.md)

 

 