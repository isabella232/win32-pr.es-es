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
# <a name="name-formats-for-unique-spns"></a><span data-ttu-id="4b484-105">Formatos de nombre para SPN únicos</span><span class="sxs-lookup"><span data-stu-id="4b484-105">Name Formats for Unique SPNs</span></span>

<span data-ttu-id="4b484-106">Un SPN debe ser único en el bosque en el que está registrado.</span><span class="sxs-lookup"><span data-stu-id="4b484-106">An SPN must be unique in the forest in which it is registered.</span></span> <span data-ttu-id="4b484-107">Si no es único, se producirá un error de autenticación.</span><span class="sxs-lookup"><span data-stu-id="4b484-107">If it is not unique, authentication will fail.</span></span> <span data-ttu-id="4b484-108">La sintaxis de SPN tiene cuatro elementos: dos elementos necesarios y dos elementos adicionales que se pueden usar, si es necesario, para generar un nombre único, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="4b484-108">The SPN syntax has four elements: two required elements and two additional elements that you can use, if necessary, to produce a unique name as listed in the following table.</span></span>


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
<th><span data-ttu-id="4b484-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="4b484-109">Element</span></span></th>
<th><span data-ttu-id="4b484-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b484-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4b484-111">&quot;&lt;clase de servicio&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="4b484-111">&quot;&lt;service class&gt;&quot;</span></span></td>
<td><span data-ttu-id="4b484-112">Cadena que identifica la clase general de servicio; por ejemplo, &quot; SQLServer &quot; .</span><span class="sxs-lookup"><span data-stu-id="4b484-112">A string that identifies the general class of service; for example, &quot;SqlServer&quot;.</span></span> <span data-ttu-id="4b484-113">Hay nombres de clase de servicio conocidos, como &quot; www &quot; para un servicio web o &quot; LDAP &quot; para un servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="4b484-113">There are well-known service class names, such as &quot;www&quot; for a web service or &quot;ldap&quot; for a directory service.</span></span> <span data-ttu-id="4b484-114">En general, puede ser cualquier cadena que sea única para la clase de servicio.</span><span class="sxs-lookup"><span data-stu-id="4b484-114">In general, this can be any string that is unique to the service class.</span></span> <span data-ttu-id="4b484-115">Tenga en cuenta que la sintaxis de SPN usa una barra diagonal (/) para separar elementos, por lo que este carácter no puede aparecer en un nombre de clase de servicio.</span><span class="sxs-lookup"><span data-stu-id="4b484-115">Be aware that the SPN syntax uses a forward slash (/) to separate elements, so this character cannot appear in a service class name.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b484-116">&quot;&lt;organizar&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="4b484-116">&quot;&lt;host&gt;&quot;</span></span></td>
<td><span data-ttu-id="4b484-117">Nombre del equipo en el que se está ejecutando el servicio.</span><span class="sxs-lookup"><span data-stu-id="4b484-117">The name of the computer on which the service is running.</span></span> <span data-ttu-id="4b484-118">Puede ser un nombre DNS completo o un nombre NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="4b484-118">This can be a fully qualified DNS name or a NetBIOS name.</span></span> <span data-ttu-id="4b484-119">Tenga en cuenta que no se garantiza que los nombres NetBIOS sean únicos en un bosque, por lo que un SPN que contiene un nombre NetBIOS quizás no sea único.</span><span class="sxs-lookup"><span data-stu-id="4b484-119">Be aware that NetBIOS names are not guaranteed to be unique in a forest, so an SPN that contains a NetBIOS name may not be unique.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4b484-120">&quot;&lt;port&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="4b484-120">&quot;&lt;port&gt;&quot;</span></span></td>
<td><span data-ttu-id="4b484-121">Un número de puerto opcional para diferenciar entre varias instancias de la misma clase de servicio en un único equipo host.</span><span class="sxs-lookup"><span data-stu-id="4b484-121">An optional port number to differentiate between multiple instances of the same service class on a single host computer.</span></span> <span data-ttu-id="4b484-122">Omita este componente si el servicio utiliza el puerto predeterminado para su clase de servicio.</span><span class="sxs-lookup"><span data-stu-id="4b484-122">Omit this component if the service uses the default port for its service class.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b484-123">&quot;&lt;nombre del servicio&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="4b484-123">&quot;&lt;service name&gt;&quot;</span></span></td>
<td><span data-ttu-id="4b484-124">Nombre opcional que se usa en los SPN de un servicio replicable para identificar los datos o servicios proporcionados por el servicio o el dominio atendido por el servicio.</span><span class="sxs-lookup"><span data-stu-id="4b484-124">An optional name used in the SPNs of a replicable service to identify the data or services provided by the service or the domain served by the service.</span></span> <span data-ttu-id="4b484-125">Este componente puede tener uno de los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="4b484-125">This component can have one of the following formats:</span></span>
<ul>
<li><span data-ttu-id="4b484-126">Nombre distintivo o objectGUID de un objeto en Active Directory Domain Services, como un punto de conexión de servicio (SCP).</span><span class="sxs-lookup"><span data-stu-id="4b484-126">The distinguished name or objectGUID of an object in Active Directory Domain Services, such as a service connection point (SCP).</span></span></li>
<li><span data-ttu-id="4b484-127">Nombre DNS del dominio de un servicio que proporciona un servicio especificado para un dominio en su totalidad.</span><span class="sxs-lookup"><span data-stu-id="4b484-127">The DNS name of the domain for a service that provides a specified service for a domain as a whole.</span></span></li>
<li><span data-ttu-id="4b484-128">Nombre DNS de un registro SRV o MX.</span><span class="sxs-lookup"><span data-stu-id="4b484-128">The DNS name of an SRV or MX record.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4b484-129">Los componentes presentes en los SPN de un servicio dependen de cómo se identifique y se replique el servicio.</span><span class="sxs-lookup"><span data-stu-id="4b484-129">The components present in a service's SPNs depend on how the service is identified and replicated.</span></span> <span data-ttu-id="4b484-130">Hay dos escenarios básicos: servicios basados en host y servicios replicables.</span><span class="sxs-lookup"><span data-stu-id="4b484-130">There are two basic scenarios: host-based services and replicable services.</span></span>

## <a name="host-based-services"></a><span data-ttu-id="4b484-131">Servicios basados en host</span><span class="sxs-lookup"><span data-stu-id="4b484-131">Host-based services</span></span>

<span data-ttu-id="4b484-132">Para un servicio basado en host, &lt; &gt; se omite el componente "nombre del servicio" porque el servicio se identifica de forma única mediante la clase de servicio y el nombre del equipo host en el que está instalado el servicio.</span><span class="sxs-lookup"><span data-stu-id="4b484-132">For a host-based service, the "&lt;service name&gt;" component is omitted because the service is uniquely identified by the service class and the name of the host computer on which the service is installed.</span></span>


```C++
<service class>/<host>
```



<span data-ttu-id="4b484-133">La clase de servicio por sí solo es suficiente para identificar a los clientes las características que proporciona el servicio.</span><span class="sxs-lookup"><span data-stu-id="4b484-133">The service class alone is sufficient to identify for clients the features that the service provides.</span></span> <span data-ttu-id="4b484-134">Puede instalar instancias de la clase de servicio en muchos equipos y cada instancia proporciona servicios que se identifican con su equipo host.</span><span class="sxs-lookup"><span data-stu-id="4b484-134">You can install instances of the service class on many computers and each instance provides services that are identified with its host computer.</span></span> <span data-ttu-id="4b484-135">FTP y telnet son ejemplos de servicios basados en host.</span><span class="sxs-lookup"><span data-stu-id="4b484-135">FTP and Telnet are examples of host-based services.</span></span> <span data-ttu-id="4b484-136">Los SPN de una instancia de servicio basada en host pueden incluir el número de puerto si el servicio usa un puerto no predeterminado o hay varias instancias del servicio en el host.</span><span class="sxs-lookup"><span data-stu-id="4b484-136">The SPNs of a host-based service instance can include the port number if the service uses a non-default port or there are multiple instances of the service on the host.</span></span>


```C++
<service class>/<host>:<port>
```



## <a name="replicable-services"></a><span data-ttu-id="4b484-137">Servicios replicables</span><span class="sxs-lookup"><span data-stu-id="4b484-137">Replicable services</span></span>

<span data-ttu-id="4b484-138">En el caso de un servicio replicable, puede haber una o varias instancias del servicio (réplicas) y los clientes no diferencian a qué réplica se conectan, ya que cada una proporciona el mismo servicio.</span><span class="sxs-lookup"><span data-stu-id="4b484-138">For a replicable service there can be one or many instances of the service (replicas), and clients do not differentiate which replica they connect to because each provides the same service.</span></span> <span data-ttu-id="4b484-139">Los SPN de cada réplica tienen los mismos componentes de " &lt; clase &gt; de servicio" y " &lt; nombre &gt; de servicio", donde " &lt; nombre de servicio &gt; " identifica más específicamente las características proporcionadas por el servicio.</span><span class="sxs-lookup"><span data-stu-id="4b484-139">The SPNs for each replica have the same "&lt;service class&gt;" and "&lt;service name&gt;" components, where "&lt;service name&gt;" identifies more specifically the features provided by the service.</span></span> <span data-ttu-id="4b484-140">Solo los &lt; &gt; componentes de "host" y " &lt; Puerto" opcionales &gt; pueden variar de SPN a SPN.</span><span class="sxs-lookup"><span data-stu-id="4b484-140">Only the "&lt;host&gt;" and optional "&lt;port&gt;" components would vary from SPN to SPN.</span></span>


```C++
<service class>/<host>:<port>/<service name>
```



<span data-ttu-id="4b484-141">Un ejemplo de un servicio replicable sería una instancia de un servicio de base de datos que proporcione acceso a una base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="4b484-141">An example of a replicable service would be an instance of a database service that provides access to a specified database.</span></span> <span data-ttu-id="4b484-142">En este caso, " &lt; clase &gt; de servicio" identifica la aplicación de base de datos y " &lt; nombre &gt; de servicio" identifica la base de datos específica.</span><span class="sxs-lookup"><span data-stu-id="4b484-142">In this case, "&lt;service class&gt;" identifies the database application and "&lt;service name&gt;" identifies the specific database.</span></span> <span data-ttu-id="4b484-143">" &lt; nombre &gt; de servicio" podría ser el nombre distintivo de un punto de conexión de servicio (SCP) que contiene los datos de conexión de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="4b484-143">"&lt;service name&gt;" could be the distinguished name of a service connection point (SCP) containing connection data for the database.</span></span>


```C++
MyDBService/host1.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
```



<span data-ttu-id="4b484-144">Si los clientes van a usar el nombre de NetBIOS para componer el SPN de un servicio, cada réplica también debe registrar un SPN que contenga el nombre NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="4b484-144">If clients will use the NetBIOS name to compose a service's SPN, each replica must also register an SPN containing the NetBIOS name.</span></span>


```C++
MyDBService/host1/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3/CN=hrdb,OU=mktg,DC=example,DC=com
```



<span data-ttu-id="4b484-145">Otro ejemplo de un servicio replicable es el que proporciona servicios a todo un dominio.</span><span class="sxs-lookup"><span data-stu-id="4b484-145">Another example of a replicable service is one that provides services to an entire domain.</span></span> <span data-ttu-id="4b484-146">En este caso, el &lt; componente "nombre del servicio &gt; " es el nombre DNS del dominio que se atiende.</span><span class="sxs-lookup"><span data-stu-id="4b484-146">In this case, the "&lt;service name&gt;" component is the DNS name of the domain being served.</span></span> <span data-ttu-id="4b484-147">Un KDC de Kerberos es un ejemplo de este tipo de servicio replicable.</span><span class="sxs-lookup"><span data-stu-id="4b484-147">A Kerberos KDC is an example of this type of replicable service.</span></span>

<span data-ttu-id="4b484-148">Tenga en cuenta que si el nombre DNS de un equipo cambia, el sistema actualiza el &lt; elemento "host &gt; " de todos los SPN registrados para ese host en el bosque.</span><span class="sxs-lookup"><span data-stu-id="4b484-148">Be aware that if the DNS name of a computer changes, the system updates the "&lt;host&gt;" element for all registered SPNs for that host in the forest.</span></span>

 

 




