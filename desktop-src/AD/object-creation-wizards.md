---
title: Asistentes para la creación de objetos
description: En los complementos MMC administrativos de Active Directory Domain Services, el usuario puede crear nuevos objetos en un directorio abriendo el menú contextual del contenedor donde se creará el nuevo objeto, eligiendo Nuevo y eligiendo la clase de objeto que se va a crear. Al crear nuevas instancias de un objeto, se inicia el Asistente para la creación de objetos. Cada clase de objeto puede especificar el uso de un asistente de creación específico o puede usar un asistente para creación genérico. Para las clases comunes, como user y organizationalUnit, el complemento Usuarios y equipos de Active Directory proporciona un conjunto estándar de asistentes de creación. Hay dos maneras de extender un asistente de creación Reemplazar un asistente existente o proporcionar uno si no existe para la clase El asistente existente se reemplaza mediante la creación de una extensión de creación de objetos principal. Una extensión de creación principal proporciona el primer conjunto de páginas y se hospeda de la misma manera que las páginas nativas. Una extensión de creación principal también admite el mecanismo de extensibilidad para que se puedan invocar otras extensiones del asistente de creación. Para obtener un ejemplo de una extensión principal, consulte el ejemplo scpwizard en Platform Software Development Kit (SDK). Extender un asistente existente Un asistente existente se puede extender con una extensión de creación de objetos secundario. Una extensión de creación secundaria agrega páginas del asistente a las páginas nativas o a la extensión principal. Para obtener más información y un ejemplo de una extensión de creación secundaria, consulte el ejemplo userwizard en el SDK de plataforma.
ms.assetid: 7ac7ec21-72a9-4d1f-80f1-1eb5bfa2b296
ms.tgt_platform: multiple
keywords:
- objetos AD , asistentes para creación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b97c5c8f1b521d28c926d53830135dbb1b1fc907758e7047bc91c68856eedc70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025593"
---
# <a name="object-creation-wizards"></a>Asistentes para la creación de objetos

En los complementos MMC administrativos de Active Directory Domain Services, el usuario puede crear nuevos objetos en un directorio abriendo el menú contextual del contenedor donde se creará el nuevo objeto, eligiendo Nuevo y eligiendo la clase de objeto que se va a crear. Al crear nuevas instancias de un objeto, se inicia el Asistente para la creación de objetos. Cada clase de objeto puede especificar el uso de un asistente de creación específico o puede usar un asistente para creación genérico. Para las clases comunes, como [**user**](/windows/desktop/ADSchema/c-user) y [**organizationalUnit,**](/windows/desktop/ADSchema/c-organizationalunit)el complemento Usuarios y equipos de Active Directory proporciona un conjunto estándar de asistentes de creación.

Hay dos maneras de ampliar un asistente de creación:

-   Reemplace un asistente existente o proporcione uno si no existe para la clase : el asistente existente se reemplaza mediante la creación de una *extensión de creación de objetos principal*. Una extensión de creación principal proporciona el primer conjunto de páginas y se hospeda de la misma manera que las páginas nativas. Una extensión de creación principal también admite el mecanismo de extensibilidad para que se puedan invocar otras extensiones del asistente de creación. Para obtener un ejemplo de una extensión principal, consulte el ejemplo scpwizard en Platform Software Development Kit (SDK).
-   Extender un asistente existente: un asistente existente se puede extender con una *extensión de creación de objetos secundarios*. Una extensión de creación secundaria agrega páginas del asistente a las páginas nativas o a la extensión principal. Para obtener más información y un ejemplo de una extensión de creación secundaria, consulte el ejemplo userwizard en el SDK de plataforma.

## <a name="developer-audience"></a>Audiencia de los desarrolladores

En esta documentación se da por supuesto que el lector está familiarizado con la operación COM y el desarrollo de componentes mediante C++. Actualmente no es posible crear una extensión para el asistente para la creación Active Directory de objetos mediante Visual Basic.

## <a name="creating-an-active-directory-object-creation-extension"></a>Creación de una Active Directory de creación de objetos

Las extensiones de creación de objetos principal y secundario son servidores COM en proceso que implementan determinadas interfaces y se registran con Active Directory Domain Services.

**Para crear e instalar una extensión de creación de objetos**

1.  Cree el archivo DLL de la extensión de creación de objetos. Una extensión de creación de objetos es un servidor com en proceso que, como mínimo, implementa la interfaz [**IDsAdminNewObjExt.**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjext) Para obtener más información, vea [Implementar el objeto COM de la extensión de creación de objetos](implementing-the-object-creation-extension-com-object.md).
2.  Instale la extensión de creación en los equipos donde se va a usar la extensión de creación. Para ello, cree un paquete de Microsoft Windows Installer para el archivo DLL de la extensión de creación e implemente el paquete correctamente mediante la directiva de grupo. Para obtener más información, [vea Distribución de Interfaz de usuario componentes](distributing-user-interface-components.md).
3.  Registre la extensión de creación en Windows registro y con Active Directory Domain Services. Para obtener más información, vea [Registrar la extensión de creación de objetos](registering-the-object-creation-extension.md).

## <a name="using-an-object-creation-wizard"></a>Usar un Asistente para la creación de objetos

También se puede invocar un asistente para la creación de objetos desde una aplicación que no sea los complementos MMC administrativos de Active Directory Domain Services. Para obtener más información, [vea Invoking Creation Wizards from Your Application](invoking-creation-wizards-from-your-application.md).

Si un asistente para la creación no está registrado para una clase de objeto, los complementos administrativos proporcionan un asistente para la creación genérica. El asistente para la creación genérica se crea en tiempo de ejecución a partir de la lista de propiedades obligatorias para la clase de objeto creada. Para cada propiedad obligatoria, se agrega una página a la interfaz de usuario. El Asistente para la creación genérica no es extensible. Si se requiere extensibilidad, se debe reemplazar por una extensión de creación de objetos principal.

 

 