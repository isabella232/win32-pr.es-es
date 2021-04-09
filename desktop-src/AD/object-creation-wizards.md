---
title: Asistentes para crear objetos
description: En los complementos de MMC administrativos de Active Directory Domain Services, el usuario puede crear nuevos objetos en un directorio abriendo el menú contextual del contenedor donde se creará el nuevo objeto, eligiendo nuevo y eligiendo la clase de objeto que se va a crear. La creación de nuevas instancias de un objeto inicia el Asistente para crear objetos. Cada clase de objeto puede especificar el uso de un asistente para creación específico o puede usar un asistente para creación de genéricos. En el caso de las clases comunes, como User y organizationalUnit, el complemento usuarios y equipos de Active Directory proporciona un conjunto estándar de asistentes de creación. Hay dos maneras de extender un asistente de creación que reemplaza a un asistente existente, o bien proporcionar uno si no existe ninguno para la clase. el asistente existente se sustituye por la creación de una extensión de creación de objeto principal. Una extensión de creación principal proporciona el primer conjunto de páginas y se hospeda de la misma manera que las páginas nativas. Una extensión de creación principal también admite el mecanismo de extensibilidad para que se puedan invocar otras extensiones del Asistente para creación. Para obtener un ejemplo de una extensión principal, vea el ejemplo scpwizard en el kit de desarrollo de software (SDK) de la plataforma. Extender un asistente existente un asistente existente se puede extender con una extensión de creación de objeto secundario. Una extensión de creación secundaria agrega páginas del asistente a las páginas nativas o a la extensión principal. Para obtener más información y un ejemplo de una extensión de creación secundaria, vea el ejemplo userwizard en el SDK de la plataforma.
ms.assetid: 7ac7ec21-72a9-4d1f-80f1-1eb5bfa2b296
ms.tgt_platform: multiple
keywords:
- objetos AD, asistentes para creación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc3dbacaf6eee5670fdacd9a587a497397c4d1b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149174"
---
# <a name="object-creation-wizards"></a>Asistentes para crear objetos

En los complementos de MMC administrativos de Active Directory Domain Services, el usuario puede crear nuevos objetos en un directorio abriendo el menú contextual del contenedor donde se creará el nuevo objeto, eligiendo **nuevo** y eligiendo la clase de objeto que se va a crear. La creación de nuevas instancias de un objeto inicia el Asistente para crear objetos. Cada clase de objeto puede especificar el uso de un asistente para creación específico o puede usar un asistente para creación de genéricos. En el caso de las clases comunes, como [**User**](/windows/desktop/ADSchema/c-user) y [**organizationalUnit**](/windows/desktop/ADSchema/c-organizationalunit), el complemento usuarios y equipos de Active Directory proporciona un conjunto estándar de asistentes de creación.

Hay dos maneras de ampliar un asistente de creación:

-   Reemplazar un asistente existente o proporcionar uno si no existe ninguno para la clase: el asistente existente se reemplaza con la creación de una *extensión de creación de objeto principal*. Una extensión de creación principal proporciona el primer conjunto de páginas y se hospeda de la misma manera que las páginas nativas. Una extensión de creación principal también admite el mecanismo de extensibilidad para que se puedan invocar otras extensiones del Asistente para creación. Para obtener un ejemplo de una extensión principal, vea el ejemplo scpwizard en el kit de desarrollo de software (SDK) de la plataforma.
-   Extender un asistente existente: un asistente existente se puede extender con una *extensión de creación de objeto secundario*. Una extensión de creación secundaria agrega páginas del asistente a las páginas nativas o a la extensión principal. Para obtener más información y un ejemplo de una extensión de creación secundaria, vea el ejemplo userwizard en el SDK de la plataforma.

## <a name="developer-audience"></a>Audiencia de los desarrolladores

En esta documentación se supone que el lector está familiarizado con el funcionamiento COM y el desarrollo de componentes mediante C++. En la actualidad, no es posible crear una extensión para el Asistente para la creación de Active Directory objeto mediante Visual Basic.

## <a name="creating-an-active-directory-object-creation-extension"></a>Crear una extensión de creación de objetos Active Directory

Tanto las extensiones de creación de objetos principales como las secundarias son servidores COM en proceso que implementan determinadas interfaces y se registran con Active Directory Domain Services.

**Para crear e instalar una extensión de creación de objetos**

1.  Cree el archivo DLL de extensión de creación de objetos. Una extensión de creación de objetos es un servidor COM en proceso que, como mínimo, implementa la interfaz [**IDsAdminNewObjExt**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjext) . Para obtener más información, vea [implementar el objeto com de extensión de creación de objetos](implementing-the-object-creation-extension-com-object.md).
2.  Instale la extensión de creación en los equipos donde se va a usar la extensión de creación. Para ello, cree un paquete de Microsoft Windows Installer para el archivo DLL de extensión de creación e implemente el paquete adecuadamente mediante la Directiva de grupo. Para obtener más información, consulte [distribuir componentes](distributing-user-interface-components.md)de la interfaz de usuario.
3.  Registre la extensión de creación en el registro de Windows y con Active Directory Domain Services. Para obtener más información, vea [registrar la extensión de creación de objetos](registering-the-object-creation-extension.md).

## <a name="using-an-object-creation-wizard"></a>Usar un asistente para crear objetos

También se puede invocar un asistente para crear objetos desde una aplicación que no sea de los complementos MMC administrativos de Active Directory Domain Services. Para obtener más información, vea [invocación de los asistentes para creación desde la aplicación](invoking-creation-wizards-from-your-application.md).

Si no se ha registrado un asistente para creación para una clase de objeto, los complementos administrativos proporcionan un asistente para la creación de genéricos. El Asistente para la creación de genéricos se genera en tiempo de ejecución desde la lista de propiedades obligatorias para la clase de objeto creado. Para cada propiedad obligatoria, se agrega una página a la interfaz de usuario. El Asistente para creación de genéricos no es extensible. Si es necesaria la extensibilidad, debe reemplazarse por una extensión de creación de objeto principal.

 

 