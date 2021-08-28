---
title: Acerca de Active Directory Domain Services
description: Esta guía proporciona información esencial para integrar Microsoft Active Directory aplicaciones distribuidas diseñadas para sistemas operativos que admiten Active Directory.
ms.assetid: cc6c63dd-ae22-40a7-8312-0a4648bb92bd
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory , acerca de
- Active Directory Domain Services Active Directory , acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5db36807362ba5542fdc6a946905c7ba9f9189
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466612"
---
# <a name="about-active-directory-domain-services"></a>Acerca de Active Directory Domain Services

## <a name="writing-powerful-applications-that-use-active-directory-domain-services"></a>Escribir aplicaciones eficaces que usan Active Directory Domain Services

En esta guía se proporciona información esencial para integrar Active Directory Domain Services aplicaciones distribuidas diseñadas para sistemas operativos que admiten Active Directory Domain Services, incluidos:

-   Windows Server 2008
-   Windows Server 2008 R2
-   Windows Server 2012
-   Windows Server 2012 R2
-   Windows Server 2016

> [!Note]  
> Estos temas son para desarrolladores de software. Para problemas de soporte técnico, [consulte Soporte técnico de Microsoft](https://windows.microsoft.com/windows/support#1tc). Para obtener información sobre la administración Active Directory, [consulte Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) en TechNet.

 

## <a name="fundamental-directory-features"></a>Características fundamentales del directorio

Un servicio de directorio es un servicio fundamental para las aplicaciones distribuidas. Un servicio de directorio debe proporcionar las características enumeradas en la tabla siguiente.



| Característica               | Descripción                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Transparencia de ubicación | Se pueden encontrar datos de usuario, grupo, servicio en red o recurso sin la dirección del objeto           |
| Datos de objeto           | Capaz de almacenar datos de usuario, grupo, organización y servicio en un árbol jerárquico                    |
| Consulta enriquecte            | Para buscar un objeto, consulte las propiedades del objeto.                                          |
| Alta disponibilidad     | Se puede encontrar una réplica del directorio en una ubicación que sea eficaz para las operaciones de lectura y escritura. |



 

## <a name="advanced-features-of-active-directory-domain-services"></a>Características avanzadas de Active Directory Domain Services

Active Directory Domain Services proporciona las características enumeradas en la tabla siguiente.




| Característica | Descripción | 
|---------|-------------|
| Compatibilidad con estándares de Internet | Active Directory Domain Services implementa sus características de acuerdo con los estándares de Internet publicados, como LDAP y DNS. | 
| Seguridad estrechamente integrada y flexible | Entre las ventajas, se incluyen las siguientes:<br /><ul><li>Elección de paquetes de autenticación. Kerberos, Capa de sockets seguros (SSL) o una combinación; Por ejemplo, establezca un canal SSL para el cifrado y, a continuación, use Kerberos para la autenticación.</li><li>Administración central del acceso al servicio y a los recursos mediante los usuarios y grupos de Active Directory Domain Services.</li><li>Delegación de administración para que los administradores centrales puedan delegar tareas administrativas como el cambio de contraseña o la creación y eliminación de objetos específicos.</li><li>El Active Directory utiliza los mismos mecanismos de control de acceso que se usan en los sistemas de archivos Windows sistemas operativos. Por lo tanto, las mismas herramientas que administran el control de acceso en un sistema de archivos funcionan para Active Directory Domain Services.</li><li>Infraestructura de clave pública completa. La compatibilidad con Microsoft Certificate Server y la tarjeta inteligente se integran Active Directory Domain Services para proporcionar el inicio de sesión de tarjeta inteligente y la administración de certificados.</li></ul> | 
| Programable fácilmente | Se puede acceder Active Directory servidor mediante programación y administrarse mediante la API de interfaces de servicio de <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">Active Directory,</a> la API lightweight <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">directory access protocol</a> o el espacio de nombres <a href="/dotnet/api/system.directoryservices">System.DirectoryServices.</a> | 
| Servicios del sistema habilitados para directorios | La aplicación cliente se puede implementar fácilmente en escritorios distribuidos mediante la creación de un paquete del instalador de Windows y el uso de la característica de implementación de aplicaciones disponible en Windows sistemas operativos. | 
| Integración de aplicaciones clave | Las aplicaciones distribuidas clave, como Exchange, se integran con Active Directory Domain Services. Por lo tanto, las empresas pueden reducir el número de servicios de directorio que se administrarán. | 
| Esquema enriquecido y extensible | El esquema define qué objetos y propiedades se pueden escribir y leer desde un servicio de directorio. El Active Directory esquema es enriquecido. La mayoría de los objetos y propiedades que requiere un servicio están disponibles. Si no es así, una aplicación distribuida puede ampliar el esquema para admitir los requisitos de la aplicación. | 




 

Para obtener más información sobre Active Directory Domain Services, vea:

-   [Conceptos básicos de Active Directory Domain Services](core-concepts-of-active-directory-domain-services.md)
-   [Active Directory arquitectura](active-directory-domain-services-architecture.md)
-   [Active Directory esquema](active-directory-schema.md)

