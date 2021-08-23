---
title: Nombres de entidad de seguridad de servicio
description: Un nombre de entidad de seguridad de servicio (SPN) es un identificador único de una instancia de servicio.
ms.assetid: 54b02853-4097-4e37-b7a2-6b5cfd168ece
ms.tgt_platform: multiple
keywords:
- Nombres de entidad de seguridad de servicio
- SPN ver nombres de entidad de seguridad de servicio
- nombre de entidad de seguridad de servicio AD
- nombre de entidad de seguridad de servicio AD , acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6639ade82f029a89cb378de20bb279348962c4a991899f95e7f1b06157cd7ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024823"
---
# <a name="service-principal-names"></a>Nombres de entidad de seguridad de servicio

Un nombre de entidad de seguridad de servicio (SPN) es un identificador único de una instancia de servicio. La autenticación Kerberos usa los SPN [para](mutual-authentication-using-kerberos.md) asociar una instancia de servicio a una cuenta de inicio de sesión de servicio. Esto permite que una aplicación cliente solicite que el servicio autentique una cuenta incluso si el cliente no tiene el nombre de cuenta.

Si instala varias instancias de un servicio en equipos a lo largo de un bosque, cada instancia debe tener su propio SPN. Una instancia de servicio determinada puede tener varios SPN si hay varios nombres que los clientes pueden usar para la autenticación. Por ejemplo, un SPN siempre incluye el nombre del equipo host en el que se ejecuta la instancia de servicio, por lo que una instancia de servicio podría registrar un SPN para cada nombre o alias de su host. Para obtener más información sobre el formato SPN y la composición de un SPN único, vea Formatos de nombre [para SPN únicos.](name-formats-for-unique-spns.md)

Para que el servicio de autenticación Kerberos pueda usar un SPN para autenticar un servicio, el SPN debe registrarse en el objeto de cuenta que la instancia de servicio usa para iniciar sesión. Un SPN determinado solo se puede registrar en una cuenta. Para los servicios Win32, un instalador de servicio especifica la cuenta de inicio de sesión cuando se instala una instancia del servicio. A continuación, el instalador crea los SPN y los escribe como una propiedad del objeto de cuenta en Active Directory Domain Services. Si cambia la cuenta de inicio de sesión de una instancia de servicio, los SPN se deben volver a registrar en la nueva cuenta. Para obtener más información, [vea How a Service Registers its SPNs](how-a-service-registers-its-spns.md)( Cómo un servicio registra sus SPN).

Cuando un cliente desea conectarse a un servicio, busca una instancia del servicio, compone un SPN para esa instancia, se conecta al servicio y presenta el SPN para que lo autentique el servicio. Para obtener más información, [vea How Clients Compose a Service's SPN](how-clients-compose-a-serviceampaposs-spn.md)( Cómo los clientes componen el SPN de un servicio).

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

[¿Qué es un SPN y por qué debe interesar?](/archive/blogs/autz_auth_stuff/what-is-a-spn-and-why-should-you-care)
</dt> <dt>

[Autenticación mutua con Kerberos](mutual-authentication-using-kerberos.md)
</dt> </dl>

 

 