---
title: Uso de Active Directory Domain Services
description: En esta sección se proporcionan instrucciones para escribir aplicaciones que usan o publican datos en un servicio de directorio de Active Directory.
ms.assetid: 2ae20169-08a5-4e15-8430-ea99a917725f
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, usar
- Active Directory Domain Services Active Directory, usar
- Active Directory ejemplos Active Directory
- Active Directory Domain Services ejemplos Active Directory
- ejemplos Active Directory
- Active Directory Active Directory, ejemplos vea ejemplos de Active Directory Domain Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540b9004311db320decbd15c4f0a29e52ec1302a
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797061"
---
# <a name="using-active-directory-domain-services"></a>Uso de Active Directory Domain Services

En esta sección se proporcionan instrucciones para escribir aplicaciones que usan o publican datos en un servicio de directorio de Active Directory.

> [!Note]  
> La siguiente documentación es para programadores de equipos. Si está intentando resolver un error de impresión de Active Directory Home, consulte la [siguiente sugerencia](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) en las páginas de la comunidad de Microsoft: Si eso no ayuda, Pruebe estas recomendaciones desde [technet](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint).

 

Active Directory Domain Services son compatibles con el Protocolo ligero de acceso a directorios 3,0, definido por RFC 2251 y otras RFC. Cualquiera de los siguientes conjuntos de API se puede usar para tener acceso a Active Directory Domain Services. Cada conjunto de API tiene ventajas y desventajas que dependen del lenguaje de programación, el entorno de programación y el método de ejecución previsto. La mayoría de los ejemplos de esta guía usan ADSI, que es compatible con lenguajes como C y C++, así como con lenguajes compatibles con la automatización, como Microsoft Visual Basic y Visual Basic Scripting Edition.

Para obtener más información acerca de las tecnologías de Active Directory Domain Services específicas, consulte:

-   [Protocolo ligero de acceso a directorio](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api)
-   [Interfaces de servicio de Active Directory](../adsi/active-directory-service-interfaces-adsi.md)
-   [System.DirectoryServices](/dotnet/api/system.directoryservices)

En esta sección se tratan los temas siguientes:

-   [Enlazar a Active Directory Domain Services](binding-to-active-directory-domain-services.md)
-   [Búsqueda en Active Directory Domain Services](searching-in-active-directory-domain-services.md)
-   [Crear y eliminar objetos en Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md)
-   [Mover objetos](moving-objects.md)
-   [Leer y escribir atributos de objetos en Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md)
-   [Controlar el acceso a objetos en Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md)
-   [Extender el esquema](extending-the-schema.md)
-   [Extensión de la interfaz de usuario para objetos de directorio](extending-the-user-interface-for-directory-objects.md)
-   [Administración de usuarios](managing-users.md)
-   [Administración de grupos](managing-groups.md)
-   [Seguimiento de cambios](tracking-changes.md)
-   [Publicación de servicios](service-publication.md)
-   [Cuentas de inicio de sesión de servicio](service-logon-accounts.md)
-   [Autenticación mutua con Kerberos](mutual-authentication-using-kerberos.md)
-   [Realizar copias de seguridad y restaurar Active Directory](backing-up-and-restoring-an-active-directory-server.md)
-   [Almacenar datos dinámicos](storing-dynamic-data.md)
-   [Particiones de directorio de aplicaciones](application-directory-partitions.md)
-   [Detección del modo de operación de un dominio](detecting-the-operation-mode-of-a-domain.md)

 

 