---
title: Dónde crear un punto de conexión de servicio
description: Cuando se instala una instancia Active Directory Domain Services, el instalador de servicio crea objetos de punto de conexión de servicio (SCP) en Active Directory Domain Services.
ms.assetid: a90566d9-dd68-43e2-be9e-300d57a7fbf4
ms.tgt_platform: multiple
keywords:
- dónde crear un punto de conexión de servicio ad
- active directory, donde crear un punto de conexión de servicio
- dónde crear un punto de conexión de servicio ad
- creación de un punto de conexión de servicio de AD
- punto de conexión de servicio ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b585c11333b8e307a7f6771bd89ccf5ad82038fb22f10fca7eb114c1101a063a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182093"
---
# <a name="where-to-create-a-service-connection-point"></a>Dónde crear un punto de conexión de servicio

Cuando se instala una instancia Active Directory Domain Services, el instalador de servicio crea objetos de punto de conexión de servicio (SCP) en Active Directory Domain Services. El objetivo principal debe ser minimizar el tráfico de replicación y permitir una administración y mantenimiento eficientes de los objetos.

Tenga en cuenta que las aplicaciones cliente buscan SCP buscando palabras clave en el directorio en scp. El **atributo keywords** de un SCP se incluye en el catálogo global; los clientes pueden buscar en el catálogo global para buscar SCP en el bosque. Por este motivo, el cliente no influye en dónde publicar los SCP.

## <a name="minimize-replication-traffic"></a>Minimizar el tráfico de replicación

Para minimizar el tráfico de replicación, cree SCP en la partición de dominio del dominio del equipo host de servicio. Por ejemplo, puede crear SCP como objetos secundarios del objeto de equipo en el que está instalado el servicio. Una partición de dominio de Active Directory Domain Services, a veces denominada contexto de nomenclatura de dominio, contiene objetos específicos del dominio, como los objetos para los usuarios y equipos del dominio. Una réplica completa de todos los objetos de la partición de dominio se replica en cada controlador de dominio (DC) del dominio, pero no se replica en controladores de dominio de otros dominios.

No cree SCP en la partición Configuración, también conocida como contexto de nomenclatura de configuración, porque los cambios en la partición De configuración se replican en cada controlador de dominio del bosque. Como se indicó anteriormente, los clientes de todo el bosque pueden consultar el catálogo global para buscar SCP en cualquier lugar del bosque, por lo que la creación de SCP en la partición De configuración no los hace más visibles para los clientes. solo genera más tráfico de replicación.

## <a name="ease-of-administration"></a>Facilidad de administración

Tenga en cuenta las siguientes directrices para la administración de objetos:

-   Coloque objetos específicos del servicio donde los administradores puedan controlar el acceso a ellos mediante permisos de acceso heredados y directivas.
-   Coloque los objetos en los que un administrador pueda encontrarlos fácilmente.

Una buena ubicación predeterminada que cumpla ambos objetivos es crear SCP y otros objetos específicos del servicio en el objeto de equipo del equipo host de cada instancia de servicio. Para obtener más información, [vea Publicar en un objeto de equipo](publishing-under-a-computer-object.md).

Una buena alternativa para los servicios que no están vinculados a un único host es crear un contenedor para los objetos de servicio en el contenedor System en una partición de dominio. Para obtener más información, [vea Publicar en un contenedor de sistema de dominio.](publishing-in-a-domain-system-container.md)

En el diagrama siguiente se muestra parte de la jerarquía de contenedores predeterminada para una partición de dominio.

![jerarquía de contenedor de particiones de dominio predeterminada](images/domain-container-heirarchy.png)

El diagrama muestra la jerarquía de dominio predeterminada incluida con Active Directory Domain Services. Sin embargo, muchas empresas crean una jerarquía de contenedores de unidad organizativa (OU) para agrupar clases de objetos, como usuarios y equipos, con fines de administración. A continuación, los administradores pueden aplicar directivas y entradas de control de acceso (ACE) heredables a una unidad organizativa para delegar la autoridad administrativa para los objetos de la unidad organizativa. Esto permite a los administradores administrar de forma eficaz una empresa, pero tiene algunas consecuencias para los programadores de servicios:

-   Es posible que el objeto de equipo de un host de servicio no esté en el contenedor Equipos, como se muestra en el diagrama. Para obtener más información sobre cómo buscar el objeto de equipo para el equipo local, vea [Publicar en un objeto de equipo](publishing-under-a-computer-object.md).
-   Los administradores pueden mover objetos a medida que cambian sus necesidades organizativas. Esto significa que no puede depender de los objetos restantes en una ubicación fija; es decir, el servicio no puede depender de que un nombre distintivo de objeto sea el mismo. En su lugar, use el atributo **objectGUID de** un objeto, que no cambia si se mueve o se cambia el nombre del objeto. Para obtener más información y un ejemplo de código que crea un SCP, almacena su **objectGUID** y, posteriormente, recupera el **objectGUID** que se enlazará al SCP, vea Crear y mantener un punto de conexión de [servicio.](creating-and-maintaining-a-service-connection-point.md)
-   Todas las clases de objetos estándar relacionadas con el servicio, así como las subclases de estas clases, son elementos secundarios válidos de las clases **computer** y **organizationalUnit.** Si extiende el esquema para definir su propia clase  específica del servicio, asegúrese de que las clases computer y **organizationalUnit** se incluyen en los posibles superiores.
-   El instalador del servicio determina la ubicación predeterminada para crear SCP. Es posible que desee permitir que el administrador que instala el servicio especifique una ruta de instalación alternativa.

Los objetos específicos del servicio no deben crearse en las áreas siguientes:

-   Los servicios no deben publicar objetos directamente en los contenedores Usuarios o Equipos de una partición de dominio, ni deben crear nuevos contenedores en estos contenedores. Sin embargo, los servicios pueden publicar objetos como objetos secundarios de un objeto de equipo, independientemente de si el objeto de equipo está almacenado o no en el contenedor Equipos.
-   Los servicios, que usan el registro y la resolución (RnR) de Windows Sockets o las API del servicio de nombres RPC (RpcN) para anunciarse, crean los objetos adecuados en los contenedores WinsockServices y RpcServices en el contenedor System de una partición de dominio. No cree explícitamente objetos en estos contenedores. Si lo hace, no causa daños directos, pero puede resultar confuso para los administradores.

 

 




