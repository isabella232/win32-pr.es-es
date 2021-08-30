---
description: A partir de Windows Server 2003, el grupo Usuarios de Monitor de rendimiento y el grupo Usuarios del registro de rendimiento se han puesto a disposición de los desarrolladores y usuarios de archivos DLL de rendimiento y las funciones de API del Asistente de datos de rendimiento (PDH).
ms.assetid: 423359be-9d41-4a5f-91cd-f6d7a6a91d9d
title: Restringir el acceso a los archivos DLL de la extensión de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43bfe7877a3ab93ea21945eacd9398d9f9536deff66ca9bd95b73abea7d8d1aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962385"
---
# <a name="restricting-access-to-performance-extension-dlls"></a>Restringir el acceso a los archivos DLL de la extensión de rendimiento

A partir de Windows Server 2003, el grupo Usuarios de Monitor de rendimiento y el grupo Usuarios del registro de rendimiento se han puesto a disposición de los desarrolladores y usuarios de archivos DLL de rendimiento y las funciones de API del Asistente de datos de rendimiento (PDH). Estos grupos de seguridad de rendimiento están diseñados para que los administradores del sistema restrinjan el acceso a la información expuesta por los archivos DLL de rendimiento a una lista específica de usuarios.

El Monitor de rendimiento usuarios está diseñado para incluir usuarios que ven datos de contadores y no registren datos de contadores mediante el Registros y alertas de rendimiento servicio. El grupo Usuarios del registro de rendimiento debe incluir usuarios que tengan permiso para usar los registros de rendimiento y el servicio de alertas para registrar contadores en el servidor local o remoto. Los privilegios de este grupo también incluyen la creación de archivos de registro en sistemas locales o remotos, el uso del servicio de alertas y la ejecución de programas como parte del servicio.

Tenga en cuenta que estos grupos de seguridad de rendimiento no son por sí mismos un mecanismo de restricción de acceso. Para ello, debe usar estos grupos Windows modelo de control de acceso a objetos.

La mayoría de las aplicaciones se comunican con el archivo DLL de rendimiento a través de un mecanismo IPC, normalmente memoria compartida. Por lo tanto, puede agregar los miembros de un grupo de seguridad de rendimiento al descriptor de seguridad del objeto de memoria compartida para restringir el acceso a la DLL a esos miembros del grupo de seguridad. Al hacerlo, también debe agregar los miembros del grupo al descriptor de seguridad de los objetos del sistema a los que accede el archivo DLL de rendimiento para proporcionar datos de contador, por ejemplo, archivos de registro y carpetas. Para obtener información más detallada sobre cómo agregar ACL a descriptores de seguridad de objetos, consulte [Modificación de la ACL de un objeto.](/windows/desktop/SecAuthZ/modifying-the-acls-of-an-object-in-c--)

Otro método que puede usar para modificar la información de ACL del descriptor de seguridad de un objeto del sistema IPC es especificar los miembros de la lista de grupos de seguridad de rendimiento con lenguaje de definición de descriptores de seguridad (SDDL) y llamar a [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) para crear el descriptor de seguridad. A continuación, este descriptor de seguridad se adjunta al objeto del sistema IPC. A continuación se muestra una cadena SDDL que incluye el grupo Monitor de rendimiento Usuarios, MU y el grupo Usuarios del registro de rendimiento, LU.

``` syntax
D:(A;OICI;GA;;;SY)(A;OICI;GA;;;BA)(A;OICI;FRFWFXSDRC;;;NS)(A;OICI;FRFWFXSDRC;;;LU)(A;OICI;FRFX;;;MU) 
```

 

 
