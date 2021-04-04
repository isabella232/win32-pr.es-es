---
title: Puntos de conexión de servicio para servicios de base de datos, basados en host y replicados
description: Al publicar un servicio mediante un punto de conexión de servicio (SCP), tenga en cuenta cómo buscarán los clientes el SCP para su servicio.
ms.assetid: 944e8ecd-f8ea-4506-992c-bbbfc82d11f3
ms.tgt_platform: multiple
keywords:
- Puntos de conexión de servicio para AD replicado, basado en host y servicios de base de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b69491dd84a9367f8fd05e9d23ca771551dfbb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077493"
---
# <a name="service-connection-points-for-replicated-host-based-and-database-services"></a>Puntos de conexión de servicio para servicios de base de datos, basados en host y replicados

Al publicar un servicio mediante un punto de conexión de servicio (SCP), tenga en cuenta cómo buscarán los clientes el SCP para su servicio. Si existen varias instancias del servicio, tenga en cuenta cómo los clientes distinguirán el servicio con las características deseadas de servicios similares con características diferentes. Si publica un servicio replicado, tenga en cuenta cómo un cliente elegirá una réplica. En este tema se describen estos problemas para diversos tipos de servicios.

## <a name="replicable-services"></a>Servicios replicables

En el caso de un servicio replicable, puede haber una o varias instancias, o réplicas, del servicio y los clientes no se interesan a la réplica a la que se conectan, ya que cada una proporciona el mismo servicio. Active Directory Domain Services son ejemplos de servicios replicados: todos los controladores de dominio de un dominio determinado contienen datos idénticos, están sujetos a la latencia de replicación y proporcionan servicios idénticos.

Los servicios replicables pueden almacenar los SCP y otros objetos específicos del servicio para varias réplicas en un solo contenedor. La aplicación de instalación de la primera réplica puede crear el contenedor como un elemento secundario del contenedor System del dominio local. Para obtener más información, vea [publicar en un contenedor de sistema de dominio](publishing-in-a-domain-system-container.md). Asegúrese de que el descriptor de seguridad del contenedor permita que los programas de instalación de las réplicas posteriores creen sus objetos en el mismo contenedor. Conceda permisos para que el administrador de instalación especifique los usuarios o grupos que pueden crear o modificar objetos en el contenedor.

Una estrategia para un servicio replicable es crear un SCP para cada réplica. Cuando un cliente consulta el GUID del producto del servicio u otra palabra clave de identificación, busca los objetos SCP para todas las réplicas y selecciona uno de forma aleatoria o con algún algoritmo de equilibrio de carga. Por ejemplo, un administrador puede especificar los datos de equilibrio de carga y prioridad para cada réplica, de forma similar a los campos de prioridad y peso de un registro SRV de DNS. La aplicación de instalación del servicio puede almacenar estos datos en el atributo **serviceBindingInformation** del SCP de cada réplica. Los clientes recuperan los datos de cada SCP y lo usan para seleccionar una réplica.

Otra estrategia consiste en crear un único SCP para todas las réplicas y establecer el atributo SCP **serviceDNSName** en el nombre de un registro SRV de DNS. A continuación, la aplicación de instalación de cada réplica registra un registro SRV con ese nombre. Cuando un cliente identifica el SCP solitario del servicio, el cliente recupera el nombre del registro SRV y usa la función [**DnsQuery**](/windows/desktop/api/windns/nf-windns-dnsquery_a) para recuperar la matriz de registros SRV para las réplicas. Cada registro SRV contiene el nombre de un equipo host y datos adicionales que el cliente puede usar para seleccionar una réplica.

## <a name="database-services"></a>Servicios de base de datos

Las distintas instancias de un servicio de base de datos pueden contener datos completamente diferentes, aunque son todo el tipo de servicio, normalmente denominado clase de servicio. Para publicar este tipo de servicio, el atributo **Keywords** del SCP puede identificar la clase de servicio y la base de datos específica. Un cliente de uso general que conozca solo el GUID de la clase de servicio puede consultar todas las bases de datos publicadas por esa clase de servicio y, a continuación, presentar una interfaz de usuario para permitir que el usuario seleccione una. Para un cliente que está diseñado específicamente para la base de datos de destino, puede codificar el GUID de la base de datos en el código de cliente.

## <a name="host-based-services"></a>Servicios basados en host

Los servicios basados en host son servicios que están estrechamente vinculados a un único equipo host. Puede instalar instancias de la clase de servicio en muchos equipos y cada instancia proporciona servicios que se identifican con su equipo host.

Cada instancia de un servicio basado en host debe crear su propio SCP en el objeto de equipo de su host. Los clientes que usan un GUID de producto para buscar el SCP de un servicio basado en host suelen encontrar muchas instancias de la clase de servicio en todo el bosque de la empresa. Después, los clientes pueden usar el atributo **serviceDNSName** de los SCP para buscar el SCP de la instancia de servicio en el equipo host deseado.

 

 