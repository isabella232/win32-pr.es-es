---
title: Nombres de entidad de seguridad de servicio
description: Un nombre de entidad de seguridad de servicio (SPN) es un identificador único de una instancia de servicio.
ms.assetid: 54b02853-4097-4e37-b7a2-6b5cfd168ece
ms.tgt_platform: multiple
keywords:
- Nombres de entidad de seguridad de servicio
- SPN; consulte nombres de entidad de seguridad de servicio
- nombre de entidad de seguridad de servicio AD
- nombre principal de servicio AD, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa34b7d90803a324faced7d67b56c0b6a1f13af
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904469"
---
# <a name="service-principal-names"></a>Nombres de entidad de seguridad de servicio

Un nombre de entidad de seguridad de servicio (SPN) es un identificador único de una instancia de servicio. La [autenticación Kerberos](mutual-authentication-using-kerberos.md) utiliza los SPN para asociar una instancia de servicio con una cuenta de inicio de sesión de servicio. Esto permite a una aplicación cliente solicitar que el servicio autentique una cuenta aunque el cliente no tenga el nombre de la cuenta.

Si instala varias instancias de un servicio en equipos a lo largo de un bosque, cada instancia debe tener su propio SPN. Una instancia de servicio determinada puede tener varios SPN si hay varios nombres que los clientes pueden usar para la autenticación. Por ejemplo, un SPN incluye siempre el nombre del equipo host en el que se ejecuta la instancia de servicio, por lo que una instancia de servicio podría registrar un SPN para cada nombre o alias de su host. Para obtener más información sobre el formato de SPN y la creación de un SPN único, vea [formatos de nombre para SPN únicos](name-formats-for-unique-spns.md).

Antes de que el servicio de autenticación Kerberos pueda utilizar un SPN para autenticar un servicio, el SPN debe estar registrado en el objeto de cuenta que la instancia de servicio utiliza para iniciar sesión. Un SPN determinado solo se puede registrar en una cuenta. En el caso de los servicios Win32, un instalador de servicio especifica la cuenta de inicio de sesión cuando se instala una instancia del servicio. A continuación, el instalador compone los SPN y los escribe como una propiedad del objeto de cuenta en Active Directory Domain Services. Si la cuenta de inicio de sesión de una instancia de servicio cambia, los SPN deben registrarse de nuevo en la nueva cuenta. Para obtener más información, vea [cómo un servicio registra sus SPN](how-a-service-registers-its-spns.md).

Cuando un cliente desea conectarse a un servicio, busca una instancia del servicio, compone un SPN para esa instancia, se conecta al servicio y presenta el SPN para que lo autentique el servicio. Para obtener más información, vea [cómo los clientes componen el SPN de un servicio](how-clients-compose-a-serviceampaposs-spn.md).

## <a name="in-this-section"></a>En esta sección

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Formatos de nombre para SPN únicos](name-formats-for-unique-spns.md)
</dt> <dt>

[Cómo un servicio crea sus SPN](how-a-service-composes-its-spns.md)
</dt> <dt>

[Cómo un servicio registra sus SPN](how-a-service-registers-its-spns.md)
</dt> <dt>

[Cómo los clientes componen el SPN de un servicio](how-clients-compose-a-serviceampaposs-spn.md)
</dt> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[¿Qué es un SPN y por qué debe preocuparse?](/archive/blogs/autz_auth_stuff/what-is-a-spn-and-why-should-you-care)
</dt> <dt>

[Autenticación mutua con Kerberos](mutual-authentication-using-kerberos.md)
</dt> </dl>

 

 