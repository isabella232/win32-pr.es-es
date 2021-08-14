---
title: Páginas de propiedades para su uso con especificadores de visualización
description: Active Directory Domain Services un mecanismo para agregar páginas a la hoja de propiedades mostrada para un objeto de directorio desde los complementos administrativos de Active Directory o el shell Windows.
ms.assetid: c1dd84e2-50f9-4903-a4b5-4473515e4d0e
ms.tgt_platform: multiple
keywords:
- display specifiers AD , páginas de propiedades para su uso con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f813223aa88dce3b8bba867139bab476416cba1932c583e2e9be591de03fc63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185189"
---
# <a name="property-pages-for-use-with-display-specifiers"></a>Páginas de propiedades para su uso con especificadores de visualización

Active Directory Domain Services un mecanismo para agregar páginas a la hoja de propiedades mostrada para un objeto de directorio desde los complementos administrativos de Active Directory o el shell Windows. Para agregar una página a la hoja de propiedades, implemente una extensión de hoja de propiedades.

## <a name="developer-audience"></a>Audiencia de los desarrolladores

En esta documentación se da por supuesto que el lector está familiarizado con el desarrollo de componentes y operaciones COM mediante C++. Actualmente no es posible crear una extensión de hoja Active Directory propiedades mediante Visual Basic.

## <a name="creating-an-active-directory-property-sheet-extension"></a>Crear una extensión Active Directory hoja de propiedades

Una *extensión de hoja de* propiedades es un servidor COM en proceso que implementa determinadas interfaces y se registra con Active Directory Domain Services. Para crear una extensión de hoja de propiedades, realice los pasos siguientes.

**Para crear una extensión Active Directory hoja de propiedades**

1.  Cree el archivo DLL de extensión de la hoja de propiedades. Una extensión de hoja de propiedades es un servidor COM en proceso que, como mínimo, implementa las interfaces [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) e [**IShellPropSheetExt.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) Para obtener más información, vea [Implementing the Property Page COM Object](implementing-the-property-page-com-object.md).
2.  Instale la extensión de hoja de propiedades en los equipos donde se va a usar la extensión de hoja de propiedades. Para ello, cree un paquete de Microsoft Windows Installer para el archivo DLL de extensión de hoja de propiedades e implemente el paquete correctamente mediante la directiva de grupo. Para obtener más información, vea [Distribución de Interfaz de usuario componentes](distributing-user-interface-components.md).
3.  Registre la extensión de hoja de propiedades en Windows registro y con Active Directory Domain Services. Para obtener más información, [vea Registrar el objeto COM de la página de propiedades en un especificador de presentación.](registering-the-property-page-com-object-in-a-display-specifier.md)

 

 