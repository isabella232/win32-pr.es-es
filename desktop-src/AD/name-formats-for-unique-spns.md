---
title: Formatos de nombre para SPN únicos
description: Un SPN debe ser único en el bosque en el que está registrado.
ms.assetid: dd3f9f7c-b64c-4bd8-924f-a8880ee3b71e
ms.tgt_platform: multiple
keywords:
- Formatos de nombre para SPN únicos AD
- Nombre de entidad de seguridad de servicio AD, formatos de nombre para
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bda13cf5a095f8f2fd7ef1a209c6f3aeebd6654
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268272"
---
# <a name="name-formats-for-unique-spns"></a>Formatos de nombre para SPN únicos

Un SPN debe ser único en el bosque en el que está registrado. Si no es único, se producirá un error de autenticación. La sintaxis de SPN tiene cuatro elementos: dos elementos necesarios y dos elementos adicionales que se pueden usar, si es necesario, para generar un nombre único, tal como se muestra en la tabla siguiente.


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
<td>Cadena que identifica la clase general de servicio; por ejemplo, &quot; SQLServer &quot; . Hay nombres de clase de servicio conocidos, como &quot; www &quot; para un servicio web o &quot; LDAP &quot; para un servicio de directorio. En general, puede ser cualquier cadena que sea única para la clase de servicio. Tenga en cuenta que la sintaxis de SPN usa una barra diagonal (/) para separar elementos, por lo que este carácter no puede aparecer en un nombre de clase de servicio.</td>
</tr>
<tr class="even">
<td>&quot;&lt;organizar&gt;&quot;</td>
<td>Nombre del equipo en el que se está ejecutando el servicio. Puede ser un nombre DNS completo o un nombre NetBIOS. Tenga en cuenta que no se garantiza que los nombres NetBIOS sean únicos en un bosque, por lo que un SPN que contiene un nombre NetBIOS quizás no sea único.</td>
</tr>
<tr class="odd">
<td>&quot;&lt;port&gt;&quot;</td>
<td>Un número de puerto opcional para diferenciar entre varias instancias de la misma clase de servicio en un único equipo host. Omita este componente si el servicio utiliza el puerto predeterminado para su clase de servicio.</td>
</tr>
<tr class="even">
<td>&quot;&lt;nombre del servicio&gt;&quot;</td>
<td>Nombre opcional que se usa en los SPN de un servicio replicable para identificar los datos o servicios proporcionados por el servicio o el dominio atendido por el servicio. Este componente puede tener uno de los siguientes formatos:
<ul>
<li>Nombre distintivo o objectGUID de un objeto en Active Directory Domain Services, como un punto de conexión de servicio (SCP).</li>
<li>Nombre DNS del dominio de un servicio que proporciona un servicio especificado para un dominio en su totalidad.</li>
<li>Nombre DNS de un registro SRV o MX.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Los componentes presentes en los SPN de un servicio dependen de cómo se identifique y se replique el servicio. Hay dos escenarios básicos: servicios basados en host y servicios replicables.

## <a name="host-based-services"></a>Servicios basados en host

Para un servicio basado en host, &lt; &gt; se omite el componente "nombre del servicio" porque el servicio se identifica de forma única mediante la clase de servicio y el nombre del equipo host en el que está instalado el servicio.


```C++
<service class>/<host>
```



La clase de servicio por sí solo es suficiente para identificar a los clientes las características que proporciona el servicio. Puede instalar instancias de la clase de servicio en muchos equipos y cada instancia proporciona servicios que se identifican con su equipo host. FTP y telnet son ejemplos de servicios basados en host. Los SPN de una instancia de servicio basada en host pueden incluir el número de puerto si el servicio usa un puerto no predeterminado o hay varias instancias del servicio en el host.


```C++
<service class>/<host>:<port>
```



## <a name="replicable-services"></a>Servicios replicables

En el caso de un servicio replicable, puede haber una o varias instancias del servicio (réplicas) y los clientes no diferencian a qué réplica se conectan, ya que cada una proporciona el mismo servicio. Los SPN de cada réplica tienen los mismos componentes de " &lt; clase &gt; de servicio" y " &lt; nombre &gt; de servicio", donde " &lt; nombre de servicio &gt; " identifica más específicamente las características proporcionadas por el servicio. Solo los &lt; &gt; componentes de "host" y " &lt; Puerto" opcionales &gt; pueden variar de SPN a SPN.


```C++
<service class>/<host>:<port>/<service name>
```



Un ejemplo de un servicio replicable sería una instancia de un servicio de base de datos que proporcione acceso a una base de datos especificada. En este caso, " &lt; clase &gt; de servicio" identifica la aplicación de base de datos y " &lt; nombre &gt; de servicio" identifica la base de datos específica. " &lt; nombre &gt; de servicio" podría ser el nombre distintivo de un punto de conexión de servicio (SCP) que contiene los datos de conexión de la base de datos.


```C++
MyDBService/host1.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
```



Si los clientes van a usar el nombre de NetBIOS para componer el SPN de un servicio, cada réplica también debe registrar un SPN que contenga el nombre NetBIOS.


```C++
MyDBService/host1/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3/CN=hrdb,OU=mktg,DC=example,DC=com
```



Otro ejemplo de un servicio replicable es el que proporciona servicios a todo un dominio. En este caso, el &lt; componente "nombre del servicio &gt; " es el nombre DNS del dominio que se atiende. Un KDC de Kerberos es un ejemplo de este tipo de servicio replicable.

Tenga en cuenta que si el nombre DNS de un equipo cambia, el sistema actualiza el &lt; elemento "host &gt; " de todos los SPN registrados para ese host en el bosque.

 

 




