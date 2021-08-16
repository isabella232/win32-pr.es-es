---
title: Acerca de las particiones de directorio de aplicación
description: Los desarrolladores que usan ADSI o LDAP para almacenar y acceder a datos relativamente estáticos y globales en Active Directory Domain Services también pueden preferir, por motivos de simplicidad y uniformidad, seguir usando el acceso ADSI o LDAP para sus requisitos de datos dinámicos. Los datos dinámicos cambian con más frecuencia de lo que se ha recomendado para almacenarlos en Active Directory Domain Services. Normalmente, los datos dinámicos cambian con más frecuencia que la latencia de replicación implicada en la propagación del cambio en todas las réplicas de los datos.
ms.assetid: bf856c3a-9061-474a-a536-c87ca50d5f83
ms.tgt_platform: multiple
keywords:
- Acerca de las particiones de directorio de aplicación
- Particiones de directorio de aplicación, Acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9063a05bdb6f04681f012f1e6317b3343833c79c8f6a5af39a1a7865eccbab63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841035"
---
# <a name="about-application-directory-partitions"></a>Acerca de las particiones de directorio de aplicación

Los desarrolladores que usan ADSI o LDAP para almacenar y acceder a datos relativamente estáticos y globales en Active Directory Domain Services también pueden preferir, por motivos de simplicidad y uniformidad, seguir usando el acceso ADSI o LDAP para sus requisitos de datos dinámicos. Los datos dinámicos cambian con más frecuencia de lo que se ha recomendado para almacenarlos en Active Directory Domain Services. Normalmente, los datos dinámicos cambian con más frecuencia que la latencia de replicación implicada en la propagación del cambio en todas las réplicas de los datos.

En Windows 2000, la compatibilidad con datos dinámicos es limitada. El almacenamiento de datos dinámicos en una partición de dominio puede ser complicado. Los datos se replican en todos los controladores de dominio del dominio, lo que a menudo es innecesario y puede dar lugar a datos incoherentes debido a la latencia de replicación. Esto puede afectar negativamente al rendimiento de la red. Además, las particiones de dominio no son eficaces para las aplicaciones que deben replicar datos a través de los límites del dominio. Otra opción de Windows 2000 es almacenar datos dinámicos en atributos marcados como no replicados. Sin embargo, esta disposición está limitada en que tiene un único punto de error, es decir, el controlador de dominio único que contiene la única copia de los atributos no replicados del objeto.

Las particiones de directorio de aplicación proporcionan la capacidad de controlar el ámbito de replicación y permitir la colocación de réplicas de una manera más adecuada para los datos dinámicos. Como resultado, la partición del directorio de la aplicación proporciona la capacidad de hospedar datos dinámicos en el servidor de Active Directory, lo que permite el acceso ADSI/LDAP a ellos, sin afectar significativamente al rendimiento de la red.

El Windows DNS 2000 es un ejemplo de un servicio que puede aprovechar las particiones del directorio de la aplicación. En Windows 2000, si el servicio DNS está configurado opcionalmente para usar Active Directory Domain Services, los datos de la zona DNS se almacenan en Active Directory Server en una partición de dominio. Es decir, los datos se replican en todos los controladores de dominio del dominio, independientemente de si un servidor DNS está configurado para ejecutarse en el controlador de dominio. Se trata de una instancia en la que no es necesaria la replicación completa en todo el dominio. Al almacenar los datos de la zona DNS en una partición de directorio de aplicación, el servicio puede volver a definir el ámbito de replicación solo a ese subconjunto de controladores de dominio del dominio que realmente ejecutan el servidor DNS.

Tenga en cuenta los siguientes escenarios para hospedar una réplica de una partición de directorio de aplicación:

-   Se puede crear una réplica de una partición de directorio de aplicación en cualquier sistema operativo Windows Server 2003 y un controlador de dominio posterior en un Active Directory Domain Services aplicación.
-   Se puede especificar el conjunto de controladores de dominio que hospedan réplicas de una partición de directorio de aplicación. A diferencia de una partición de dominio, no es necesaria una partición de directorio de aplicación para replicar en todos los controladores de dominio de un dominio y se puede replicar en controladores de dominio de dominios diferentes del bosque.
-   Un controlador de dominio con una réplica de partición de directorio de aplicación puede coexistir y funcionar en un entorno en modo mixto con otros equipos que ejecutan Windows 2000 o Windows NT 4.0.

Entre los tipos de datos que se pueden almacenar en una partición de directorio de aplicación se incluyen:

-   Una partición de directorio de aplicación puede contener instancias de cualquier tipo de objeto, excepto entidades de seguridad, como usuarios, equipos o grupos.
-   Los objetos de una partición de directorio de aplicación pueden mantener referencias de valor DN a otros objetos de la misma partición de directorio de aplicación, a objetos de las particiones de configuración y esquema y a cualquier objeto de contexto de nomenclatura (que es el objeto superior de una partición de directorio, como el objeto **domainDNS** en la parte superior de una partición de directorio de aplicación).
-   Para obtener más información y un ejemplo del tipo de datos dinámicos que podrían almacenarse en una partición de directorio de aplicación, vea [Objetos dinámicos](dynamic-objects.md). Los objetos dinámicos se admiten a partir de Windows Server 2003. Los objetos dinámicos tienen una propiedad que determina el período de vida, después del cual el servidor de Active Directory elimina el objeto.

Algunas limitaciones de las particiones de directorio de aplicaciones incluyen:

-   Los objetos de una partición de directorio de aplicación no pueden mantener referencias de valor *DN* a objetos de otras particiones de directorio de aplicación o particiones de dominio. (Las referencias de valor DN son referencias persistentes a un valor de nombre distintivo, como "CN=someuser,DC=corp,DC=Fabrikam,DC=com"). Del mismo modo, los objetos de las particiones Dominio, Configuración y Esquema no pueden mantener referencias de valor DN a objetos de una partición de directorio de aplicación. Se puede mantener una referencia de valor DN al jefe de contexto de nomenclatura. () )
-   Los objetos de una partición de directorio de aplicación no se replican en el catálogo global. Al igual que con cualquier controlador de dominio, también se puede configurar un servidor de catálogo global para que contenga una réplica completa de una partición de directorio de aplicación, pero los datos de partición del directorio de la aplicación son completamente independientes de los datos del catálogo global.
-   Cuando se crea una réplica de partición de directorio de aplicación, el rol Domain-Naming FSMO debe estar en uno de los controladores de dominio del sistema operativo Windows Server 2003 y versiones posteriores. Una vez creada la réplica de partición del directorio de la aplicación, el rol FSMO de nomenclatura de dominio se puede asignar de nuevo a un controlador de dominio Windows 2000.
-   Los objetos de partición del directorio de aplicación no se pueden mover a Active Directory particiones fuera de la partición en la que se crearon.

Otras características de partición de directorio de aplicación incluyen:

-   El modelo de seguridad y control de acceso para la partición del directorio de la aplicación es el mismo que para otras particiones de Active Directory Domain Services.
-   Los intervalos de tiempo que controlan la latencia de iniciar una notificación de cambio de origen a los asociados de replicación dentro de un sitio se pueden configurar por separado para cada partición de directorio de aplicación.
-   Las particiones de directorio de aplicación se pueden denominar igual que los dominios normales, adjuntarse en cualquier lugar del espacio de nombres de Active Directory donde un dominio pueda y detectarse mediante DNS incluso mediante sistemas de nivel inferior Windows 2000.
-   Se puede crear una partición de directorio de aplicación, su ámbito de replicación definido y su configuración configurable ajustada mediante programación mediante las API ESTÁNDAR LDAP y ADSI. Para obtener más información sobre la manipulación mediante programación de particiones de directorio de aplicaciones, vea [Particiones de directorio de aplicación.](application-directory-partitions.md)

 

 




