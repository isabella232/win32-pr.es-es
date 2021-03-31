---
title: Dónde crear un punto de conexión de servicio
description: Cuando se instala una instancia de Active Directory Domain Services, el instalador del servicio crea objetos de punto de conexión de servicio (SCP) en Active Directory Domain Services.
ms.assetid: a90566d9-dd68-43e2-be9e-300d57a7fbf4
ms.tgt_platform: multiple
keywords:
- Dónde crear un punto de conexión de servicio AD
- Active Directory, dónde crear un punto de conexión de servicio
- Dónde crear un punto de conexión de servicio AD
- creación de un punto de conexión de servicio AD
- AD de punto de conexión de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf122ebabcfd8085ebad46314ffd1c09f827e783
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075093"
---
# <a name="where-to-create-a-service-connection-point"></a>Dónde crear un punto de conexión de servicio

Cuando se instala una instancia de Active Directory Domain Services, el instalador del servicio crea objetos de punto de conexión de servicio (SCP) en Active Directory Domain Services. El objetivo principal debe ser minimizar el tráfico de replicación y habilitar la administración y el mantenimiento eficientes de los objetos.

Tenga en cuenta que las aplicaciones cliente buscan SCP buscando palabras clave en el SCP en el directorio. El atributo **Keywords** de un SCP se incluye en el catálogo global; los clientes pueden buscar en el catálogo global para buscar SCP en el bosque. Por esta razón, el cliente no influye en dónde publicar los SCP.

## <a name="minimize-replication-traffic"></a>Minimizar el tráfico de replicación

Para minimizar el tráfico de replicación, cree los SCP en la partición de dominio del dominio del equipo host del servicio. Por ejemplo, puede crear SCP como objetos secundarios del objeto de equipo en el que está instalado el servicio. Una partición de dominio de Active Directory Domain Services, a veces denominada contexto de nomenclatura de dominios, contiene objetos específicos del dominio, como los objetos para los usuarios y equipos del dominio. Una réplica completa de todos los objetos de la partición de dominio se replica en todos los controladores de dominio (DC) del dominio, pero no se replica en los controladores de dominio de otros dominios.

No cree SCP en la partición de configuración, también conocida como contexto de nomenclatura de configuración, ya que los cambios en la partición de configuración se replican en todos los controladores de dominio del bosque. Como se indicó anteriormente, los clientes de todo el bosque pueden consultar el catálogo global para buscar los SCP en cualquier parte del bosque, por lo que la creación de los SCP en la partición de configuración no los hace más visibles para los clientes. solo genera más tráfico de replicación.

## <a name="ease-of-administration"></a>Facilidad de administración

Tenga en cuenta las siguientes directrices para la administración de objetos:

-   Coloque los objetos específicos del servicio en los que los administradores puedan controlar el acceso a ellos mediante directivas y permisos de acceso heredados.
-   Coloque los objetos en donde un administrador pueda encontrarlos fácilmente.

Una buena ubicación predeterminada que satisfaga ambos objetivos es crear SCP y otros objetos específicos del servicio en el objeto de equipo del equipo host de cada instancia de servicio. Para obtener más información, vea [publicar en un objeto de equipo](publishing-under-a-computer-object.md).

Una buena alternativa para los servicios que no están vinculados a un solo host es crear un contenedor para los objetos de servicio en el contenedor del sistema en una partición de dominio. Para obtener más información, vea [publicar en un contenedor de sistema de dominio](publishing-in-a-domain-system-container.md).

En el diagrama siguiente se muestra parte de la jerarquía de contenedores predeterminada para una partición de dominio.

![jerarquía de contenedores de particiones de dominio predeterminadas](images/domain-container-heirarchy.png)

El diagrama muestra la jerarquía de dominio predeterminada que se incluye con Active Directory Domain Services. Sin embargo, muchas empresas crean una jerarquía de contenedores de unidad organizativa (OU) para agrupar clases de objetos, como usuarios y equipos, para fines de administración. Después, los administradores pueden aplicar directivas y entradas de control de acceso (ACE) heredables a una unidad organizativa para delegar la autoridad administrativa de los objetos de la unidad organizativa. Esto permite a los administradores administrar de forma eficaz una empresa, pero tiene algunas consecuencias para los programadores de servicios:

-   Es posible que el objeto de equipo de un host de servicio no esté en el contenedor equipos, tal como se muestra en el diagrama. Para obtener más información acerca de cómo buscar el objeto de equipo para el equipo local, consulte [publicación en un objeto de equipo](publishing-under-a-computer-object.md).
-   Los administradores pueden trasladar objetos a medida que cambien sus necesidades organizativas. Esto significa que no puede depender de los objetos que permanecen en una ubicación fija; es decir, el servicio no puede depender de que un nombre distintivo de objeto quede igual. En su lugar, use el atributo **objectGUID** de un objeto, que no cambia si el objeto se mueve o se cambia de nombre. Para obtener más información y un ejemplo de código que crea un SCP, almacena su **objectGUID** y, posteriormente, recupera el **objectGUID** para enlazarlo al SCP, consulte [creación y mantenimiento de un punto de conexión de servicio](creating-and-maintaining-a-service-connection-point.md).
-   Todas las clases de objetos relacionadas con el servicio estándar, así como las subclases de estas clases, son elementos secundarios válidos de las clases **Computer** y **organizationalUnit** . Si extiende el esquema para definir su propia clase específica del servicio, asegúrese de que las clases **Computer** y **organizationalUnit** se incluyen en los posibles superiores.
-   El instalador de servicio determina la ubicación predeterminada para crear los SCP. Es posible que desee permitir que el administrador que instala el servicio especifique una ruta de instalación alternativa.

No se deben crear objetos específicos del servicio en las siguientes áreas:

-   Los servicios no deben publicar objetos directamente en los contenedores usuarios o equipos de una partición de dominio, ni deben crear nuevos contenedores en estos contenedores. Sin embargo, los servicios pueden publicar objetos como objetos secundarios de un objeto de equipo, tanto si el objeto de equipo está almacenado en el contenedor de equipos como si no lo está.
-   Los servicios que usan el registro y la resolución de Windows Sockets (RnR) o las API del servicio de nombres RPC (RpcNs) para anunciarse, crean los objetos adecuados en los contenedores WinsockServices y RpcServices en el contenedor System de una partición de dominio. No cree explícitamente objetos en estos contenedores. Esto no provoca daños directos, pero puede resultar confuso para los administradores.

 

 




