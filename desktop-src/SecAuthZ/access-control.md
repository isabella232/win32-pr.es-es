---
description: El control de acceso hace referencia a las características de seguridad que controlan quién puede tener acceso a los recursos del sistema operativo. Las aplicaciones llaman a las funciones de control de acceso para establecer quién puede tener acceso a recursos específicos o controlar el acceso a los recursos proporcionados por la aplicación.
ms.assetid: d9ce4ec5-5c09-4b33-93a1-39638a925986
title: Access Control (autorización)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31c0198f0ce0de77750e0587d9b54c1e20cee756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082528"
---
# <a name="access-control-authorization"></a>Access Control (autorización)

El control de acceso hace referencia a las características de seguridad que controlan quién puede tener acceso a los recursos del sistema operativo. Las aplicaciones llaman a las funciones de control de acceso para establecer quién puede tener acceso a recursos específicos o controlar el acceso a los recursos proporcionados por la aplicación.

En esta información general se describe el modelo de seguridad para controlar el acceso a objetos de Windows, como archivos, y para controlar el acceso a las funciones administrativas, como la configuración de la hora del sistema o la auditoría de las acciones del usuario. En el tema del [modelo de Access Control](access-control-model.md) se proporciona una descripción de alto nivel de las partes del control de acceso y cómo interactúan entre sí.

En los temas siguientes se describe el control de acceso:

-   [Seguridad de nivel C2](c2-level-security.md)
-   [Modelo de Access Control](access-control-model.md)
-   [Lenguaje de definición de descriptores de seguridad](security-descriptor-definition-language.md)
-   [Privilegios](privileges.md)
-   [Generación de auditoría](audit-generation.md)
-   [Objetos protegibles](securable-objects.md)
-   [Access Control de bajo nivel](low-level-access-control.md)

A continuación se indican las tareas comunes de control de acceso:

-   [Cómo controlan el acceso a un objeto las DACL](how-dacls-control-access-to-an-object.md)
-   [Controlar la creación de objetos secundarios en C++](controlling-child-object-creation-in-c--.md)
-   [ACE para controlar el acceso a las propiedades de un objeto](aces-to-control-access-to-an-object-s-properties.md)
-   [Solicitar derechos de acceso a un objeto](requesting-access-rights-to-an-object.md)

En los temas siguientes se proporciona código de ejemplo para las tareas de control de acceso:

-   [Modificar las ACL de un objeto en C++](modifying-the-acls-of-an-object-in-c--.md)
-   [Crear un descriptor de seguridad para un nuevo objeto en C++](creating-a-security-descriptor-for-a-new-object-in-c--.md)
-   [Controlar la creación de objetos secundarios en C++](controlling-child-object-creation-in-c--.md)
-   [Habilitar y deshabilitar privilegios en C++](enabling-and-disabling-privileges-in-c--.md)
-   [Buscar un SID en un token de acceso en C++](searching-for-a-sid-in-an-access-token-in-c--.md)
-   [Buscar el propietario de un objeto de archivo en C++](finding-the-owner-of-a-file-object-in-c--.md)
-   [Tomar posesión de objetos en C++](taking-object-ownership-in-c--.md)
-   [Crear una DACL](/windows/desktop/SecBP/creating-a-dacl)

 

 
