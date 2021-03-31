---
title: Acerca de Active Directory Domain Services
description: Esta guía proporciona información esencial para la integración de Microsoft Active Directory en aplicaciones distribuidas diseñadas para sistemas operativos compatibles con Active Directory.
ms.assetid: cc6c63dd-ae22-40a7-8312-0a4648bb92bd
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, acerca de
- Active Directory Active Directory Domain Services, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d8dafb89533d796f0651ad08b913eacda1d0fe9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077796"
---
# <a name="about-active-directory-domain-services"></a>Acerca de Active Directory Domain Services

## <a name="writing-powerful-applications-that-use-active-directory-domain-services"></a>Escritura de aplicaciones eficaces que usan Active Directory Domain Services

Esta guía proporciona información esencial para la integración de Active Directory Domain Services en aplicaciones distribuidas diseñadas para sistemas operativos que admiten Active Directory Domain Services, incluidos:

-   Windows Server 2008
-   Windows Server 2008 R2
-   Windows Server 2012
-   Windows Server 2012 R2
-   Windows Server 2016

> [!Note]  
> Estos temas son para desarrolladores de software. Para problemas de soporte técnico, consulte [soporte técnico de Microsoft](https://windows.microsoft.com/windows/support#1tc). Para obtener información acerca de la administración de Active Directory, consulte [Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) en TechNet.

 

## <a name="fundamental-directory-features"></a>Características fundamentales de los directorios

Un servicio de directorio es un servicio fundamental para las aplicaciones distribuidas. Un servicio de directorio debe proporcionar las características que se muestran en la tabla siguiente.



| Característica               | Descripción                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Transparencia de ubicación | Puede encontrar datos de usuario, grupo, servicio en red o recurso, sin la dirección del objeto.           |
| Datos de objeto           | Puede almacenar datos de usuarios, grupos, organizaciones y servicios en un árbol jerárquico                    |
| Consulta enriquecida            | Puede localizar un objeto consultando las propiedades de los objetos                                          |
| Alta disponibilidad     | Puede localizar una réplica del directorio en una ubicación que sea eficaz para las operaciones de lectura y escritura. |



 

## <a name="advanced-features-of-active-directory-domain-services"></a>Características avanzadas de Active Directory Domain Services

Active Directory Domain Services proporciona las características que se muestran en la tabla siguiente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Característica</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Compatibilidad con los estándares de Internet</td>
<td>Active Directory Domain Services implementa sus características de acuerdo con los estándares de Internet publicados como LDAP y DNS.</td>
</tr>
<tr class="even">
<td>Seguridad estrechamente integrada y flexible</td>
<td>Entre las ventajas, se incluyen las siguientes:<br/>
<ul>
<li>Elección de los paquetes de autenticación. Kerberos, Capa de sockets seguros (SSL) o una combinación; por ejemplo, establezca un canal SSL para el cifrado y, a continuación, use Kerberos para la autenticación.</li>
<li>Administración central del acceso a recursos y servicios mediante el uso de usuarios y grupos en Active Directory Domain Services.</li>
<li>Delegación de la administración para que los administradores centrales puedan delegar tareas administrativas como el cambio de contraseña o la creación y eliminación de objetos específicos.</li>
<li>El servidor de Active Directory usa los mismos mecanismos de control de acceso que se usan en sistemas de archivos de los sistemas operativos Windows. Por lo tanto, las mismas herramientas que administran el control de acceso en un sistema de archivos funcionan para Active Directory Domain Services.</li>
<li>Infraestructura de clave pública completa. Microsoft Certificate Server y la compatibilidad con tarjetas inteligentes se integran con Active Directory Domain Services para proporcionar inicio de sesión de tarjeta inteligente y administración de certificados.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Fácil de programar</td>
<td>Se puede tener acceso al servidor de Active Directory mediante programación y administrarlo mediante el Active Directory API de <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">interfaces de servicio</a> , la API de <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Protocolo ligero de acceso a directorios</a> o el espacio de nombres <a href="/dotnet/api/system.directoryservices">System. DirectoryServices</a> .</td>
</tr>
<tr class="even">
<td>Servicios del sistema habilitados para directorio</td>
<td>La aplicación cliente se puede implementar fácilmente en escritorios distribuidos mediante la creación de un paquete de Windows Installer y el uso de la característica de implementación de aplicaciones disponible en los sistemas operativos Windows.</td>
</tr>
<tr class="odd">
<td>Integración de aplicaciones clave</td>
<td>Las aplicaciones clave distribuidas, como Exchange, se integran con Active Directory Domain Services. Por lo tanto, las empresas pueden reducir el número de servicios de directorio que se van a administrar.</td>
</tr>
<tr class="even">
<td>Esquema enriquecido y extensible</td>
<td>El esquema define qué objetos y propiedades se pueden escribir y leer desde un servicio de directorio. El esquema Active Directory es rico. La mayoría de los objetos y las propiedades que requiere un servicio están disponibles. Si no es así, una aplicación distribuida puede extender el esquema para admitir los requisitos de la aplicación.</td>
</tr>
</tbody>
</table>



 

Para obtener más información acerca de Active Directory Domain Services, vea:

-   [Conceptos básicos de Active Directory Domain Services](core-concepts-of-active-directory-domain-services.md)
-   [Arquitectura de Active Directory](active-directory-domain-services-architecture.md)
-   [Esquema de Active Directory](active-directory-schema.md)

