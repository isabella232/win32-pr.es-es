---
title: Habilitar Rename-Safe enlace con la propiedad otherWellKnownObjects
description: Los objetos de la clase contenedor tienen un atributo otherWellKnownObjects que puede usar para asociar un GUID con el nombre distintivo (DN) de un objeto secundario en el contenedor.
ms.assetid: 54f7468b-03e5-46b9-8b43-e3571dccdceb
ms.tgt_platform: multiple
keywords:
- propiedad otherWellKnownObjects
- propiedad otherWellKnownObjects, usar para el enlace con seguridad de cambio de nombre
- Active Directory, usar, enlazar y cambiar el nombre de enlaces seguros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7114fa6dfb44625433d8da1c57491a13aefa7cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268290"
---
# <a name="enabling-rename-safe-binding-with-the-otherwellknownobjects-property"></a><span data-ttu-id="be3f5-106">Habilitar Rename-Safe enlace con la propiedad otherWellKnownObjects</span><span class="sxs-lookup"><span data-stu-id="be3f5-106">Enabling Rename-Safe Binding with the otherWellKnownObjects Property</span></span>

<span data-ttu-id="be3f5-107">Los objetos de la clase contenedor tienen un atributo **otherWellKnownObjects** que puede usar para asociar un GUID con el nombre distintivo (DN) de un objeto secundario en el contenedor.</span><span class="sxs-lookup"><span data-stu-id="be3f5-107">Objects of the Container class have an **otherWellKnownObjects** attribute that you can use to associate a GUID with the distinguished name (DN) of a child object in the container.</span></span> <span data-ttu-id="be3f5-108">Si el objeto secundario se mueve o se cambia de nombre, el servidor de Active Directory actualiza el DN en el valor **otherWellKnownObjects** para ese objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="be3f5-108">If the child object is moved or renamed, the Active Directory server updates the DN in the **otherWellKnownObjects** value for that child object.</span></span> <span data-ttu-id="be3f5-109">Esto permite el uso de la característica de enlace WKGUID para enlazar con el objeto secundario mediante el GUID y el DN del contenedor en lugar del DN del objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="be3f5-109">This enables use of the WKGUID binding feature to bind to the child object using the GUID and the DN of the container rather than the child object's DN.</span></span>

<span data-ttu-id="be3f5-110">El atributo **otherWellKnownObjects** es equivalente al atributo **wellKnownObjects** , salvo que las aplicaciones y los servicios pueden escribir un valor **otherWellKnownObjects** , pero solo el sistema puede escribir **wellKnownObjects**.</span><span class="sxs-lookup"><span data-stu-id="be3f5-110">The **otherWellKnownObjects** attribute is equivalent to the **wellKnownObjects** attribute except that applications and services can write an **otherWellKnownObjects** value, but only the system can write **wellKnownObjects**.</span></span>

<span data-ttu-id="be3f5-111">El uso del atributo **otherWellKnownObjects** y el enlace WKGUID es beneficioso en las siguientes situaciones en las que se requiere un enlace con seguridad de cambio de nombre en relación con un objeto contenedor específico.</span><span class="sxs-lookup"><span data-stu-id="be3f5-111">Using **otherWellKnownObjects** attribute and WKGUID binding is beneficial in the following situations where rename-safe binding is required in relation to a specific container object.</span></span>

<span data-ttu-id="be3f5-112">Si un objeto contenedor contiene otros objetos importantes, o si se puede cambiar el nombre o la ubicación de los objetos importantes.</span><span class="sxs-lookup"><span data-stu-id="be3f5-112">If a container object contains other important objects, or if important objects can be renamed or moved.</span></span>

<span data-ttu-id="be3f5-113">Si existen objetos importantes para cada instancia del objeto contenedor.</span><span class="sxs-lookup"><span data-stu-id="be3f5-113">If the important objects exist for each instance of the container object.</span></span> <span data-ttu-id="be3f5-114">Por ejemplo, el sistema utiliza el atributo **wellKnownObjects** de cada objeto **domainDNS** para almacenar un valor para el contenedor usuarios, que existe en cada instancia de un objeto **domainDNS** .</span><span class="sxs-lookup"><span data-stu-id="be3f5-114">For example, the system uses the **wellKnownObjects** attribute of each **domainDNS** object to store a value for the Users container, which exists in every instance of a **domainDNS** object.</span></span> <span data-ttu-id="be3f5-115">Esto permite que las aplicaciones se enlacen al contenedor de usuarios en una forma segura para cambiar el nombre mediante la especificación del GUID conocido y el DN del contenedor **domainDNS** .</span><span class="sxs-lookup"><span data-stu-id="be3f5-115">This enables applications to bind to the Users container in a rename-safe way by specifying the well-known GUID and the DN of the **domainDNS** container.</span></span> <span data-ttu-id="be3f5-116">Las aplicaciones pueden usar el atributo **otherWellKnownObjects** de un contenedor de forma similar.</span><span class="sxs-lookup"><span data-stu-id="be3f5-116">Applications can use a container's **otherWellKnownObjects** attribute similarly.</span></span>

<span data-ttu-id="be3f5-117">Si necesita una capacidad de enlace y/o búsqueda segura para el cambio de nombre en los objetos importantes.</span><span class="sxs-lookup"><span data-stu-id="be3f5-117">If you require rename-safe binding and/or search capability on the important objects.</span></span>

<span data-ttu-id="be3f5-118">**Para agregar funcionalidades de búsqueda y enlace con seguridad de cambio de nombre**</span><span class="sxs-lookup"><span data-stu-id="be3f5-118">**To add rename-safe binding and search capabilities**</span></span>

1.  <span data-ttu-id="be3f5-119">Agregue un valor a la propiedad **otherWellKnownObjects** del objeto contenedor cuando se cree el objeto importante dentro de ese contenedor.</span><span class="sxs-lookup"><span data-stu-id="be3f5-119">Add a value to the **otherWellKnownObjects** property of the container object when the important object is created within that container.</span></span> <span data-ttu-id="be3f5-120">El valor contiene el GUID que representa el objeto conocido.</span><span class="sxs-lookup"><span data-stu-id="be3f5-120">The value contains the GUID that represents the well-known object.</span></span> <span data-ttu-id="be3f5-121">Tenga en cuenta que esto no es el **objectGUID** y el **distinguishedName** para ese objeto.</span><span class="sxs-lookup"><span data-stu-id="be3f5-121">Be aware that this is not the **objectGUID** and the **distinguishedName** for that object.</span></span>
2.  <span data-ttu-id="be3f5-122">Use la característica de enlace WKGUID para enlazar con el objeto importante o buscar en él.</span><span class="sxs-lookup"><span data-stu-id="be3f5-122">Use the WKGUID binding feature to bind to or search the important object.</span></span>

<span data-ttu-id="be3f5-123">El atributo **otherWellKnownObjects** puede tener varios valores y contiene las tuplas GUID/DN de objetos conocidos en los contenedores en los que se establecen.</span><span class="sxs-lookup"><span data-stu-id="be3f5-123">The **otherWellKnownObjects** attribute can have multiple values and contains the GUID/DN tuples of well-known objects within the containers on which they are set.</span></span> <span data-ttu-id="be3f5-124">El atributo **otherWellKnownObjects** tiene la sintaxis DNWithBinary en la que los valores tienen el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="be3f5-124">The **otherWellKnownObjects** attribute has the DNWithBinary syntax in which values have the following form:</span></span>


```C++
B:<char count>:<well known GUID>:<object DN>
```



<span data-ttu-id="be3f5-125">En este ejemplo, " &lt; Char Count &gt; " es el recuento de dígitos hexadecimales en " &lt; GUID conocido &gt; ", que es 32 (número de dígitos hexadecimales en un GUID) para **otherWellKnownObjects** y **wellKnownObjects**.</span><span class="sxs-lookup"><span data-stu-id="be3f5-125">In this example, "&lt;char count&gt;" is the count of hexadecimal digits in "&lt;well known GUID&gt;", which is 32 (number of hex digits in a GUID) for both **otherWellKnownObjects** and **wellKnownObjects**.</span></span> <span data-ttu-id="be3f5-126">" &lt; GUID conocido &gt; " es la representación de dígitos hexadecimales del GUID conocido.</span><span class="sxs-lookup"><span data-stu-id="be3f5-126">"&lt;well known GUID&gt;" is the hexadecimal digit representation of the well-known GUID.</span></span> <span data-ttu-id="be3f5-127">" &lt; DN &gt; del objeto" es el nombre distintivo del objeto representado por este valor de WKO.</span><span class="sxs-lookup"><span data-stu-id="be3f5-127">"&lt;object DN&gt;" is the distinguished name of the object represented by this WKO value.</span></span> <span data-ttu-id="be3f5-128">El servidor mantiene la parte Dnobjeto de cada valor **wellKnownObjects** y **otherWellKnownObjects** para que contenga el nombre distintivo actual del objeto que se especificó originalmente cuando se creó el valor.</span><span class="sxs-lookup"><span data-stu-id="be3f5-128">The server maintains the ObjectDN portion of each **wellKnownObjects** and **otherWellKnownObjects** value so that it contains the current distinguished name of the object originally specified when the value was created.</span></span>

<span data-ttu-id="be3f5-129">Por ejemplo, si {df447b5e-AA5B-11D2-8d53-00c04f79ab81} es el GUID conocido del objeto DataObject en el contenedor de alcontainer en el dominio Fabrikam.com, el valor **otherWellKnownObjects** especificaría el GUID conocido y el DN de DataObject:</span><span class="sxs-lookup"><span data-stu-id="be3f5-129">For example, if {df447b5e-aa5b-11d2-8d53-00c04f79ab81} is the well-known GUID of the MyObject object in the MyContainer container in the Fabrikam.com domain, the **otherWellKnownObjects** value would specify the well-known GUID and the DN of MyObject:</span></span>


```C++
B:32:df447b5eaa5b11d28d5300c04f79ab81:cn=MyObject,cn=MyContainer,dc=Fabrikam,dc=com
```



<span data-ttu-id="be3f5-130">Para enlazar a este objeto, use la siguiente cadena de enlace WKGUID que especifica el GUID conocido del objeto y el DN del contenedor:</span><span class="sxs-lookup"><span data-stu-id="be3f5-130">To bind to this object, use the following WKGUID binding string that specifies the well-known GUID of the object and the DN of the container:</span></span>


```C++
LDAP://<WKGUID=df447b5eaa5b11d28d5300c04f79ab81,cn=MyContainer,dc=Fabrikam,dc=com>
```



<span data-ttu-id="be3f5-131">Después de enlazar a este objeto, puede usar las interfaces COM ADSI para buscar, leer, modificar o eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="be3f5-131">After binding to this object, you can use the ADSI COM interfaces to search, read, modify, or delete the object.</span></span>

<span data-ttu-id="be3f5-132">Para obtener más información y un ejemplo de código que muestra cómo agregar un objeto al atributo **otherWellKnownObjects** , vea el [código de ejemplo para crear un objeto contenedor](example-code-for-creating-a-container-object.md).</span><span class="sxs-lookup"><span data-stu-id="be3f5-132">For more information and a code example that shows how to add an object to the **otherWellKnownObjects** attribute, see [Example Code for Creating a Container Object](example-code-for-creating-a-container-object.md).</span></span>

 

 




