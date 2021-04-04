---
title: Páginas de propiedades para su uso con especificadores de presentación
description: Active Directory Domain Services proporcionar un mecanismo para agregar páginas a la hoja de propiedades que se muestra para un objeto de directorio desde los complementos administrativos de Active Directory o el shell de Windows.
ms.assetid: c1dd84e2-50f9-4903-a4b5-4473515e4d0e
ms.tgt_platform: multiple
keywords:
- especificadores de presentación AD, páginas de propiedades para su uso con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c204f4d378e66cda5bc02684cb51cc707ba3d6f2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904481"
---
# <a name="property-pages-for-use-with-display-specifiers"></a>Páginas de propiedades para su uso con especificadores de presentación

Active Directory Domain Services proporcionar un mecanismo para agregar páginas a la hoja de propiedades que se muestra para un objeto de directorio desde los complementos administrativos de Active Directory o el shell de Windows. Para agregar una página a la hoja de propiedades, implemente una extensión de la hoja de propiedades.

## <a name="developer-audience"></a>Audiencia de los desarrolladores

En esta documentación se supone que el lector está familiarizado con el funcionamiento COM y el desarrollo de componentes mediante C++. En la actualidad, no es posible crear una extensión de hoja de propiedades Active Directory mediante Visual Basic.

## <a name="creating-an-active-directory-property-sheet-extension"></a>Crear una Active Directory extensión de la hoja de propiedades

Una *extensión* de la hoja de propiedades es un servidor com en proceso que implementa ciertas interfaces y se registra con Active Directory Domain Services. Para crear una extensión de la hoja de propiedades, realice los pasos siguientes.

**Para crear una Active Directory extensión de la hoja de propiedades**

1.  Cree el archivo DLL de extensión de la hoja de propiedades. Una extensión de la hoja de propiedades es un servidor COM en proceso que, como mínimo, implementa las interfaces [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) y [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) . Para obtener más información, vea [implementar el objeto com de la página de propiedades](implementing-the-property-page-com-object.md).
2.  Instale la extensión de la hoja de propiedades en los equipos donde se va a usar la extensión de la hoja de propiedades. Para ello, cree un paquete de Microsoft Windows Installer para el archivo DLL de extensión de la hoja de propiedades e implemente el paquete adecuadamente mediante la Directiva de grupo. Para obtener más información, consulte [distribuir componentes](distributing-user-interface-components.md)de la interfaz de usuario.
3.  Registre la extensión de la hoja de propiedades en el registro de Windows y con Active Directory Domain Services. Para obtener más información, vea [registrar la página de propiedades de un objeto com en un especificador de presentación](registering-the-property-page-com-object-in-a-display-specifier.md).

 

 