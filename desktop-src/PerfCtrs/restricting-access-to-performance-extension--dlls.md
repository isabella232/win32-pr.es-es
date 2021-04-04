---
description: A partir de Windows Server 2003, el grupo usuarios del monitor de rendimiento y el grupo usuarios del registro de rendimiento estaban disponibles para los programadores y usuarios de archivos dll de rendimiento y las funciones de la API de la aplicación auxiliar de datos de rendimiento (PDH).
ms.assetid: 423359be-9d41-4a5f-91cd-f6d7a6a91d9d
title: Restringir el acceso a los archivos dll de extensión de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd433cad68ec3e50f6b17994da98164e2ae9f237
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909710"
---
# <a name="restricting-access-to-performance-extension-dlls"></a>Restringir el acceso a los archivos dll de extensión de rendimiento

A partir de Windows Server 2003, el grupo usuarios del monitor de rendimiento y el grupo usuarios del registro de rendimiento estaban disponibles para los programadores y usuarios de archivos dll de rendimiento y las funciones de la API de la aplicación auxiliar de datos de rendimiento (PDH). Estos grupos de seguridad de rendimiento están pensados para que los usen los administradores del sistema a fin de restringir el acceso a la información expuesta por los archivos dll de rendimiento a una lista específica de usuarios.

El grupo usuarios del monitor de rendimiento está diseñado para incluir a los usuarios que ven datos de contador y no registran datos de contadores mediante el servicio Registros y alertas de rendimiento. El grupo usuarios del registro de rendimiento debe incluir los usuarios que tienen permiso para usar los registros de rendimiento y el servicio de alertas para registrar los contadores en el servidor local o remoto. Los privilegios de este grupo también incluyen la creación de archivos de registro en sistemas locales o remotos, el uso del servicio de alertas y la ejecución de programas como parte del servicio.

Tenga en cuenta que estos grupos de seguridad de rendimiento no son por sí mismos un mecanismo de restricción de acceso. Para ello, debe usar estos grupos con el modelo de control de acceso a objetos de Windows.

La mayoría de las aplicaciones se comunican con el archivo DLL de rendimiento a través de un mecanismo IPC, normalmente la memoria compartida. Por lo tanto, puede Agregar los miembros de un grupo de seguridad de rendimiento al descriptor de seguridad del objeto de memoria compartida para restringir el acceso al archivo DLL a esos miembros del grupo de seguridad. Al hacerlo, también debe agregar los miembros del grupo al descriptor de seguridad de los objetos del sistema a los que el archivo DLL de rendimiento tiene acceso para proporcionar los datos del contador, por ejemplo, los archivos de registro y las carpetas. Para obtener información más detallada sobre cómo agregar ACL a descriptores de seguridad de objetos, consulte [modificar la ACL de un objeto](/windows/desktop/SecAuthZ/modifying-the-acls-of-an-object-in-c--).

Otro método que puede usar para modificar la información de la ACL del descriptor de seguridad de un objeto del sistema IPC es especificar los miembros de la lista de grupos de seguridad de rendimiento con el lenguaje de definición de descriptores de seguridad (SDDL) y llamar a [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) para crear el descriptor de seguridad. Este descriptor de seguridad se adjunta al objeto de sistema IPC. A continuación se muestra una cadena SDDL que incluye el grupo de usuarios del monitor de rendimiento, MU y el grupo de usuarios del registro de rendimiento, LU.

``` syntax
D:(A;OICI;GA;;;SY)(A;OICI;GA;;;BA)(A;OICI;FRFWFXSDRC;;;NS)(A;OICI;FRFWFXSDRC;;;LU)(A;OICI;FRFX;;;MU) 
```

 

 
