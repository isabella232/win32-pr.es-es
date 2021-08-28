---
title: Formatos de nombre para SPN únicos
description: Un SPN debe ser único en el bosque en el que está registrado.
ms.assetid: dd3f9f7c-b64c-4bd8-924f-a8880ee3b71e
ms.tgt_platform: multiple
keywords:
- Formatos de nombre para AD de SPN únicos
- Nombre de entidad de seguridad de servicio AD, formatos de nombre para
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b041f88bc025c604ec5f0ad9a6bf5ba7f4cdabc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472341"
---
# <a name="name-formats-for-unique-spns"></a>Formatos de nombre para SPN únicos

Un SPN debe ser único en el bosque en el que está registrado. Si no es único, se producirá un error en la autenticación. La sintaxis de SPN tiene cuatro elementos: dos elementos necesarios y dos elementos adicionales que puede usar, si es necesario, para generar un nombre único como se muestra en la tabla siguiente.


```C++
<service class>/<host>:<port>/<service name>
```






| Elemento | Descripción | 
|---------|-------------|
| "<service class>" | Cadena que identifica la clase general de servicio; por ejemplo, "SqlServer". Hay nombres de clase de servicio conocidos, como "www" para un servicio web o "ldap" para un servicio de directorio. En general, puede ser cualquier cadena que sea única para la clase de servicio. Tenga en cuenta que la sintaxis de SPN usa una barra diagonal (/) para separar elementos, por lo que este carácter no puede aparecer en un nombre de clase de servicio. | 
| "<host>" | Nombre del equipo en el que se ejecuta el servicio. Puede ser un nombre DNS completo o un nombre NetBIOS. Tenga en cuenta que no se garantiza que los nombres NetBIOS sean únicos en un bosque, por lo que un SPN que contiene un nombre NetBIOS quizás no sea único. | 
| "<port>" | Número de puerto opcional para diferenciar entre varias instancias de la misma clase de servicio en un único equipo host. Omita este componente si el servicio usa el puerto predeterminado para su clase de servicio. | 
| "<service name>" | Nombre opcional que se usa en los SPN de un servicio replicable para identificar los datos o servicios proporcionados por el servicio o el dominio a los que sirve el servicio. Este componente puede tener uno de los siguientes formatos:<ul><li>Nombre distintivo u objectGUID de un objeto en Active Directory Domain Services, como un punto de conexión de servicio (SCP).</li><li>Nombre DNS del dominio de un servicio que proporciona un servicio especificado para un dominio en su conjunto.</li><li>Nombre DNS de un registro SRV o MX.</li></ul> | 




 

Los componentes presentes en los SPN de un servicio dependen de cómo se identifique y replique el servicio. Hay dos escenarios básicos: servicios basados en host y servicios replicables.

## <a name="host-based-services"></a>Servicios basados en host

Para un servicio basado en host, se omite el componente " nombre de servicio " porque el servicio se identifica de forma única por la clase de servicio y el nombre del equipo host en el que está &lt; &gt; instalado el servicio.


```C++
<service class>/<host>
```



La clase de servicio por sí sola es suficiente para identificar a los clientes las características que proporciona el servicio. Puede instalar instancias de la clase de servicio en muchos equipos y cada instancia proporciona servicios que se identifican con su equipo host. FTP y Telnet son ejemplos de servicios basados en host. Los SPN de una instancia de servicio basada en host pueden incluir el número de puerto si el servicio usa un puerto no predeterminado o hay varias instancias del servicio en el host.


```C++
<service class>/<host>:<port>
```



## <a name="replicable-services"></a>Servicios replicables

Para un servicio replicable, puede haber una o varias instancias del servicio (réplicas) y los clientes no diferencian a qué réplica se conectan porque cada una proporciona el mismo servicio. Los SPN de cada réplica tienen los mismos componentes " clase de servicio " y " nombre de servicio " , donde " nombre de servicio " identifica más específicamente las características &lt; &gt; &lt; &gt; &lt; &gt; proporcionadas por el servicio. Solo los componentes " &lt; host " y opcional " puerto " &gt; &lt; &gt; variarían de SPN a SPN.


```C++
<service class>/<host>:<port>/<service name>
```



Un ejemplo de un servicio replicable sería una instancia de un servicio de base de datos que proporciona acceso a una base de datos especificada. En este caso, " clase de servicio " identifica la aplicación de base de datos y " nombre de servicio &lt; " identifica la base de datos &gt; &lt; &gt; específica. " service name " podría ser el nombre distintivo de un punto de conexión de &lt; &gt; servicio (SCP) que contiene datos de conexión para la base de datos.


```C++
MyDBService/host1.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
```



Si los clientes van a usar el nombre NetBIOS para crear el SPN de un servicio, cada réplica también debe registrar un SPN que contenga el nombre NetBIOS.


```C++
MyDBService/host1/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3/CN=hrdb,OU=mktg,DC=example,DC=com
```



Otro ejemplo de un servicio replicable es aquel que proporciona servicios a un dominio completo. En este caso, el componente &lt; "nombre de &gt; servicio" es el nombre DNS del dominio que se está atendidas. Un KDC de Kerberos es un ejemplo de este tipo de servicio replicable.

Tenga en cuenta que si cambia el nombre DNS de un equipo, el sistema actualiza el elemento " host " para todos los &lt; &gt; SPN registrados para ese host en el bosque.

 

 




