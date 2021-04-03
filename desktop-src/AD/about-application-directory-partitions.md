---
title: Acerca de las particiones de directorio de aplicaciones
description: Los desarrolladores que utilizan ADSI o LDAP para almacenar y obtener acceso a datos relativamente estáticos y globales en Active Directory Domain Services también pueden preferir, por motivos de simplicidad y uniformidad, seguir usando ADSI o el acceso LDAP para sus requisitos de datos dinámicos. Los datos dinámicos cambian con más frecuencia de lo que se recomienda para almacenarlos en Active Directory Domain Services. Normalmente, los datos dinámicos cambian con más frecuencia que la latencia de replicación implicada en la propagación del cambio a todas las réplicas de los datos.
ms.assetid: bf856c3a-9061-474a-a536-c87ca50d5f83
ms.tgt_platform: multiple
keywords:
- Acerca de las particiones de directorio de aplicaciones
- Particiones de directorio de aplicaciones, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc1970f27d18d760ab3a45fae389809a40a2a89
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075028"
---
# <a name="about-application-directory-partitions"></a>Acerca de las particiones de directorio de aplicaciones

Los desarrolladores que utilizan ADSI o LDAP para almacenar y obtener acceso a datos relativamente estáticos y globales en Active Directory Domain Services también pueden preferir, por motivos de simplicidad y uniformidad, seguir usando ADSI o el acceso LDAP para sus requisitos de datos dinámicos. Los datos dinámicos cambian con más frecuencia de lo que se recomienda para almacenarlos en Active Directory Domain Services. Normalmente, los datos dinámicos cambian con más frecuencia que la latencia de replicación implicada en la propagación del cambio a todas las réplicas de los datos.

En Windows 2000, la compatibilidad con los datos dinámicos es limitada. El almacenamiento de datos dinámicos en una partición de dominio puede ser complicado. Los datos se replican en todos los controladores de dominio del dominio, que a menudo es innecesario y pueden producir datos incoherentes debido a la latencia de la replicación. Esto puede afectar negativamente al rendimiento de la red. Además, las particiones de dominio no son eficaces para las aplicaciones que deben replicar datos a través de los límites del dominio. Otra opción de Windows 2000 es almacenar los datos dinámicos en los atributos marcados como no replicados. Sin embargo, esta disposición está limitada, ya que tiene un único punto de error, es decir, el único controlador de dominio que aloja la única copia de los atributos no replicados del objeto.

Las particiones de directorio de aplicaciones proporcionan la capacidad de controlar el ámbito de replicación y permiten la colocación de réplicas de una manera más adecuada para los datos dinámicos. Como resultado, la partición del directorio de aplicaciones proporciona la capacidad de hospedar los datos dinámicos en el servidor de Active Directory, lo que permite el acceso de ADSI/LDAP sin afectar significativamente al rendimiento de la red.

El servicio DNS 2000 de Windows es un ejemplo de un servicio que puede aprovechar las particiones de directorio de aplicaciones. En Windows 2000, si el servicio DNS se configura opcionalmente para usar Active Directory Domain Services, los datos de la zona DNS se almacenan en el servidor de Active Directory en una partición de dominio. Es decir, los datos se replican en todos los controladores de dominio del dominio, independientemente de si un servidor DNS está configurado para ejecutarse en el controlador de dominio. Se trata de una instancia en la que no es necesaria la replicación completa de todo el dominio. Al almacenar los datos de la zona DNS en una partición de directorio de aplicaciones, el servicio puede volver a definir el ámbito de replicación solo para ese subconjunto de controladores de dominio en el dominio que realmente ejecuta el servidor DNS.

Tenga en cuenta los siguientes escenarios para hospedar una réplica de una partición de directorio de aplicaciones:

-   Se puede crear una réplica de una partición de directorio de aplicaciones en cualquier sistema operativo Windows Server 2003 y un controlador de dominio posterior en un bosque de Active Directory Domain Services.
-   Se puede especificar el conjunto de controladores de dominio que hospedan réplicas de una partición de directorio de aplicaciones. A diferencia de una partición de dominio, no se necesita una partición de directorio de aplicaciones para replicar en todos los controladores de dominio de un dominio y se puede replicar en controladores de dominio en dominios diferentes del bosque.
-   Un controlador de dominio con una réplica de partición de directorio de aplicaciones puede coexistir y funcionar en un entorno de modo mixto con otros equipos que ejecutan Windows 2000 o Windows NT 4,0.

Entre los tipos de datos que se pueden almacenar en una partición de directorio de aplicaciones se incluyen:

-   Una partición de directorio de aplicaciones puede contener instancias de cualquier tipo de objeto, excepto las entidades de seguridad, como usuarios, equipos o grupos.
-   Los objetos de una partición de directorio de aplicaciones pueden mantener referencias de valor DN a otros objetos de la misma partición de directorio de aplicación, a objetos de las particiones de configuración y de esquema, y a cualquier encabezado de contexto de nomenclatura (que es el objeto superior de una partición de directorio, como el objeto **domainDNS** en la parte superior de una partición de directorio de aplicaciones).
-   Para obtener más información y un ejemplo del tipo de datos dinámicos que se pueden almacenar en una partición de directorio de aplicaciones, vea [objetos dinámicos](dynamic-objects.md). Los objetos dinámicos se admiten a partir de Windows Server 2003. Los objetos dinámicos tienen una propiedad que determina el período de vida, después del cual el servidor de Active Directory elimina el objeto.

Algunas limitaciones de las particiones de directorio de aplicaciones son:

-   Los objetos de una partición de directorio de aplicaciones no pueden mantener *referencias de valor DN* a objetos de otras particiones de directorio de aplicación o particiones de dominio. (Las referencias de valor DN son referencias persistentes a un valor de nombre distintivo como "CN = someuser, DC = Corp, DC = Fabrikam, DC = com"). Del mismo modo, los objetos de particiones de dominio, de configuración y de esquema no pueden mantener referencias de valor DN a objetos en una partición de directorio de aplicaciones. Se puede mantener una referencia de valor DN al encabezado de contexto de nomenclatura. () )
-   Los objetos de una partición de directorio de aplicaciones no se replican en el catálogo global. Como con cualquier controlador de dominio, un servidor de catálogo global también puede configurarse para que contenga una réplica completa de una partición de directorio de aplicaciones, pero los datos de la partición del directorio de aplicaciones son completamente independientes de los datos del catálogo global.
-   Cuando se crea una réplica de partición de directorio de aplicaciones, el rol FSMO Domain-Naming debe estar en uno de los controladores de dominio del sistema operativo Windows Server 2003 y posteriores. Una vez creada la réplica de partición de directorio de aplicaciones, el rol FSMO de nombres de dominio se puede asignar de nuevo a un controlador de dominio de Windows 2000.
-   Los objetos de partición de directorio de aplicaciones no se pueden pasar a otras particiones de Active Directory fuera de la partición en la que se crearon.

Otras características de partición de directorio de aplicaciones incluyen:

-   El modelo de control de acceso y seguridad para la partición del directorio de aplicación es el mismo que el de otras particiones de Active Directory Domain Services.
-   Los intervalos de tiempo que controlan la latencia de iniciar una notificación de cambio de origen en los asociados de replicación de un sitio se pueden configurar por separado para cada partición del directorio de aplicaciones.
-   Las particiones de directorio de aplicaciones se pueden denominar como dominios normales, adjuntas en cualquier lugar del espacio de nombres Active Directory donde un dominio puede, y detectados mediante DNS, incluso en sistemas Windows 2000 de nivel inferior.
-   Se puede crear una partición de directorio de aplicaciones, su ámbito de replicación definido y sus valores configurables ajustados mediante programación con las API estándar de LDAP y ADSI. Para obtener más información sobre cómo manipular particiones de directorio de aplicaciones mediante programación, vea [particiones de directorio de aplicaciones](application-directory-partitions.md).

 

 




