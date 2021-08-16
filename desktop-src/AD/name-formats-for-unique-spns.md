---
title: Formatos de nombre para SPN únicos
description: Un SPN debe ser único en el bosque en el que está registrado.
ms.assetid: dd3f9f7c-b64c-4bd8-924f-a8880ee3b71e
ms.tgt_platform: multiple
keywords:
- Formatos de nombre para SPN únicos de AD
- Nombre de entidad de seguridad de servicio ad , formatos de nombre para
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce939d642180192500790253158eaa03dc41c8d173aed2d96d5175f07e39c101
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025723"
---
# <a name="name-formats-for-unique-spns"></a>Formatos de nombre para SPN únicos

Un SPN debe ser único en el bosque en el que está registrado. Si no es único, se producirá un error en la autenticación. La sintaxis de SPN tiene cuatro elementos: dos elementos obligatorios y dos elementos adicionales que puede usar, si es necesario, para generar un nombre único como se muestra en la tabla siguiente.


```C++
<service class>/<host>:<port>/<service name>
```





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;&lt;clase de servicio&gt;&quot;</td>
<td>Cadena que identifica la clase general de servicio; por ejemplo, &quot; SqlServer &quot; . Hay nombres de clase de servicio conocidos, como &quot; www para un servicio web o ldap para un servicio de &quot; &quot; &quot; directorio. En general, puede ser cualquier cadena que sea única para la clase de servicio. Tenga en cuenta que la sintaxis de SPN usa una barra diagonal (/) para separar elementos, por lo que este carácter no puede aparecer en un nombre de clase de servicio.</td>
</tr>
<tr class="even">
<td>&quot;&lt;Host&gt;&quot;</td>
<td>Nombre del equipo en el que se ejecuta el servicio. Puede ser un nombre DNS completo o un nombre NetBIOS. Tenga en cuenta que no se garantiza que los nombres NetBIOS sean únicos en un bosque, por lo que un SPN que contiene un nombre NetBIOS quizás no sea único.</td>
</tr>
<tr class="odd">
<td>&quot;&lt;port&gt;&quot;</td>
<td>Número de puerto opcional para diferenciar entre varias instancias de la misma clase de servicio en un único equipo host. Omita este componente si el servicio usa el puerto predeterminado para su clase de servicio.</td>
</tr>
<tr class="even">
<td>&quot;&lt;nombre del servicio&gt;&quot;</td>
<td>Nombre opcional que se usa en los SPN de un servicio replicable para identificar los datos o servicios proporcionados por el servicio o el dominio que sirve el servicio. Este componente puede tener uno de los siguientes formatos:
<ul>
<li>Nombre distintivo u objectGUID de un objeto en Active Directory Domain Services, como un punto de conexión de servicio (SCP).</li>
<li>Nombre DNS del dominio de un servicio que proporciona un servicio especificado para un dominio en su conjunto.</li>
<li>Nombre DNS de un registro SRV o MX.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Los componentes presentes en los SPN de un servicio dependen de cómo se identifique y replique el servicio. Hay dos escenarios básicos: servicios basados en host y servicios replicables.

## <a name="host-based-services"></a>Servicios basados en host

Para un servicio basado en host, se omite el componente " nombre de servicio " porque el servicio se identifica de forma única por la clase de servicio y el nombre del equipo host en el que está &lt; &gt; instalado el servicio.


```C++
<service class>/<host>
```



La clase de servicio por sí sola es suficiente para identificar para los clientes las características que proporciona el servicio. Puede instalar instancias de la clase de servicio en muchos equipos y cada instancia proporciona servicios que se identifican con su equipo host. FTP y Telnet son ejemplos de servicios basados en host. Los SPN de una instancia de servicio basada en host pueden incluir el número de puerto si el servicio usa un puerto no predeterminado o si hay varias instancias del servicio en el host.


```C++
<service class>/<host>:<port>
```



## <a name="replicable-services"></a>Servicios replicables

Para un servicio replicable puede haber una o varias instancias del servicio (réplicas) y los clientes no diferencian a qué réplica se conectan porque cada una proporciona el mismo servicio. Los SPN de cada réplica tienen los mismos componentes " clase de servicio " y " nombre de servicio " , donde " nombre de servicio " identifica más específicamente las características &lt; &gt; &lt; &gt; &lt; &gt; proporcionadas por el servicio. Solo los componentes " &lt; host " y opcional " puerto " &gt; &lt; &gt; variarían de SPN a SPN.


```C++
<service class>/<host>:<port>/<service name>
```



Un ejemplo de un servicio replicable sería una instancia de un servicio de base de datos que proporciona acceso a una base de datos especificada. En este caso, " clase de servicio " identifica la aplicación de base de datos &lt; y " nombre de servicio " identifica la base de datos &gt; &lt; &gt; específica. " service name " podría ser el nombre distintivo de un punto de conexión de servicio &lt; &gt; (SCP) que contiene datos de conexión para la base de datos.


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



Otro ejemplo de un servicio replicable es uno que proporciona servicios a un dominio completo. En este caso, el componente " &lt; nombre de servicio " es el nombre DNS del dominio que se &gt; sirve. Un KDC de Kerberos es un ejemplo de este tipo de servicio replicable.

Tenga en cuenta que si cambia el nombre DNS de un equipo, el sistema actualiza el elemento " host " para todos los SPN registrados para ese &lt; &gt; host en el bosque.

 

 




