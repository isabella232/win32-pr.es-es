---
title: Enlazar a objetos de Well-Known mediante WKGUID
description: En este tema se muestra cómo enlazar a objetos mediante la cadena de enlace WKGUID.
ms.assetid: cc9846c4-415e-48ee-ae08-6631636d3a63
ms.tgt_platform: multiple
keywords:
- Enlazar a objetos de Well-Known mediante WKGUID AD
- Active Directory, usar, enlazar, usar WKGUID para enlazar a objetos conocidos
- objetos conocidos de AD
- objetos conocidos de AD, enlace al uso de WKGUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd919efa6e52d7e65c2a7cd5550f3d217f54070
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789634"
---
# <a name="binding-to-well-known-objects-using-wkguid"></a><span data-ttu-id="8317e-107">Enlazar a objetos de Well-Known mediante WKGUID</span><span class="sxs-lookup"><span data-stu-id="8317e-107">Binding to Well-Known Objects Using WKGUID</span></span>

<span data-ttu-id="8317e-108">Los contenedores pueden tener uno o varios subobjetos importantes a los que se puede cambiar el nombre o que se pueden desplace.</span><span class="sxs-lookup"><span data-stu-id="8317e-108">Containers can have one, or more, important subobjects that can be renamed or moved.</span></span> <span data-ttu-id="8317e-109">Puede ser difícil realizar un seguimiento de estos subobjetos y crear cadenas de enlace correctas para ellos, especialmente si se les cambia el nombre o se mueven.</span><span class="sxs-lookup"><span data-stu-id="8317e-109">It can be difficult to track these subobjects and build correct binding strings for them, especially if they are renamed or moved.</span></span>

<span data-ttu-id="8317e-110">Para admitir el enlace con seguridad de cambio de nombre a estos objetos dentro de estos contenedores, Active Directory Domain Services tienen dos atributos: **wellKnownObjects** y **otherWellKnownObjects**.</span><span class="sxs-lookup"><span data-stu-id="8317e-110">To support rename-safe binding to these objects within these containers, Active Directory Domain Services have two attributes: **wellKnownObjects** and **otherWellKnownObjects**.</span></span> <span data-ttu-id="8317e-111">Estos atributos tienen una sintaxis de atributo de \_ DN ADSTYPE \_ con \_ binario.</span><span class="sxs-lookup"><span data-stu-id="8317e-111">These attributes have an attribute syntax of ADSTYPE\_DN\_WITH\_BINARY.</span></span> <span data-ttu-id="8317e-112">Permiten varios valores y contienen las tuplas GUID/DN de objetos conocidos en los contenedores en los que se establecen.</span><span class="sxs-lookup"><span data-stu-id="8317e-112">They allow multiple values and contain the GUID/DN tuples of well-known objects within the containers on which they are set.</span></span> <span data-ttu-id="8317e-113">El servidor de Active Directory mantiene la parte del nombre distintivo de cada entrada de **wellKnownObjects** y **otherWellKnownObjects** para que contenga el nombre distintivo actual del objeto especificado cuando se creó la entrada.</span><span class="sxs-lookup"><span data-stu-id="8317e-113">The Active Directory server maintains the distinguished name portion of each **wellKnownObjects** and **otherWellKnownObjects** entry so that it contains the current distinguished name of the object specified when the entry was created.</span></span>

<span data-ttu-id="8317e-114">La propiedad **otherWellKnownObjects** se puede establecer y usar en cualquier objeto.</span><span class="sxs-lookup"><span data-stu-id="8317e-114">The **otherWellKnownObjects** property can be set and used on any object.</span></span>

<span data-ttu-id="8317e-115">La propiedad **wellKnownObjects** se utiliza en los contenedores domainDNS y Configuration.</span><span class="sxs-lookup"><span data-stu-id="8317e-115">The **wellKnownObjects** property is used on the domainDNS and configuration containers.</span></span> <span data-ttu-id="8317e-116">La propiedad **wellKnownObjects** es una propiedad solo del sistema y solo puede ser modificada por el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8317e-116">The **wellKnownObjects** property is a system-only property and can only be modified by the operating system.</span></span>

<span data-ttu-id="8317e-117">El contenedor **domainDNS** tiene los siguientes objetos conocidos:</span><span class="sxs-lookup"><span data-stu-id="8317e-117">The **domainDNS** container has the following well-known objects:</span></span>

-   <span data-ttu-id="8317e-118">Usuarios</span><span class="sxs-lookup"><span data-stu-id="8317e-118">Users</span></span>
-   <span data-ttu-id="8317e-119">Computers</span><span class="sxs-lookup"><span data-stu-id="8317e-119">Computers</span></span>
-   <span data-ttu-id="8317e-120">System</span><span class="sxs-lookup"><span data-stu-id="8317e-120">System</span></span>
-   <span data-ttu-id="8317e-121">Controladores de dominio</span><span class="sxs-lookup"><span data-stu-id="8317e-121">Domain Controllers</span></span>
-   <span data-ttu-id="8317e-122">Infraestructura</span><span class="sxs-lookup"><span data-stu-id="8317e-122">Infrastructure</span></span>
-   <span data-ttu-id="8317e-123">Objetos eliminados</span><span class="sxs-lookup"><span data-stu-id="8317e-123">Deleted Objects</span></span>
-   <span data-ttu-id="8317e-124">Perdido y encontrado</span><span class="sxs-lookup"><span data-stu-id="8317e-124">Lost and Found</span></span>

<span data-ttu-id="8317e-125">El contenedor de configuración tiene el objeto conocido: objetos eliminados.</span><span class="sxs-lookup"><span data-stu-id="8317e-125">The configuration container has the well-known object: Deleted Objects.</span></span>

<span data-ttu-id="8317e-126">Estos objetos se encuentran en todos los contenedores de **domainDNS** y configuración de un servicio dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8317e-126">These objects are in every **domainDNS** and configuration container in an Active Directory Domain Service.</span></span>

<span data-ttu-id="8317e-127">Puede enlazar a un objeto conocido mediante el formato de enlace WKGUID.</span><span class="sxs-lookup"><span data-stu-id="8317e-127">You can bind to a well-known object using the WKGUID binding format.</span></span> <span data-ttu-id="8317e-128">El enlace con WKGUID solo se admite en Active Directory Domain Services, es decir, el proveedor LDAP.</span><span class="sxs-lookup"><span data-stu-id="8317e-128">Binding with WKGUID is only supported in Active Directory Domain Services, that is, the LDAP provider.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8317e-129">Use siempre el formato de enlace WKGUID para enlazar con los objetos conocidos, como se indicó anteriormente, en los contenedores de configuración y dominio.</span><span class="sxs-lookup"><span data-stu-id="8317e-129">Always use the WKGUID binding format to bind to the well-known objects, as listed above, in the domain and configuration containers.</span></span> <span data-ttu-id="8317e-130">Esto garantiza que estos contenedores se pueden enlazar a incluso si se mueven o cambian de nombre.</span><span class="sxs-lookup"><span data-stu-id="8317e-130">This ensures that these containers can be bound to even if they are moved or renamed.</span></span>

 

<span data-ttu-id="8317e-131">El formato de la cadena de enlace WKGUID es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="8317e-131">The WKGUID binding string format is as follows:</span></span>


```C++
LDAP://<servername>/<WKGUID=<XXXXX>,<container DN>>
```



<span data-ttu-id="8317e-132">" &lt; nombre &gt; del servidor" es el nombre del servidor de directorio.</span><span class="sxs-lookup"><span data-stu-id="8317e-132">"&lt;server name&gt;" is the directory server name.</span></span> <span data-ttu-id="8317e-133">El " &lt; nombre del servidor &gt; " es opcional.</span><span class="sxs-lookup"><span data-stu-id="8317e-133">The "&lt;server name&gt;" is optional.</span></span>

<span data-ttu-id="8317e-134">" &lt; Xxxxx &gt; " es la representación de cadena del valor hexadecimal del GUID que representa el objeto conocido.</span><span class="sxs-lookup"><span data-stu-id="8317e-134">"&lt;XXXXX&gt;" is the string representation of the hexadecimal value of the GUID that represents the well-known object.</span></span> <span data-ttu-id="8317e-135">La cadena GUID se especifica en el formulario "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" y no es de la misma forma que la cadena GUID generada por la función [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) , que tiene la forma "{xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX}".</span><span class="sxs-lookup"><span data-stu-id="8317e-135">The GUID string is specified in the "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" form and is not the same form as the GUID string produced by the [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) function, which takes the form "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}".</span></span> <span data-ttu-id="8317e-136">Para obtener más información y un ejemplo de código que muestra cómo crear una cadena enlazable desde un GUID, vea el [código de ejemplo para crear una representación de cadena enlazable de un GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span><span class="sxs-lookup"><span data-stu-id="8317e-136">For more information and a code example that shows how to create a bindable string from a GUID, see [Example Code for Creating a Bindable String Representation of a GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span></span>

<span data-ttu-id="8317e-137">Para enlazar a un objeto especificado en **otherWellKnownObjects** en un objeto, especifique " &lt; xxxxx &gt; " como forma de cadena de enlace del GUID de objeto conocido del objeto.</span><span class="sxs-lookup"><span data-stu-id="8317e-137">To bind to an object specified in **otherWellKnownObjects** in an object, specify "&lt;XXXXX&gt;" as the bind string form of the well-known object GUID of the object.</span></span> <span data-ttu-id="8317e-138">Para obtener más información, vea [leer el objectGUID de un objeto y crear una representación de cadena del GUID](reading-an-objectampaposs-objectguid-and-creating-a-string-representation-of-the-guid.md).</span><span class="sxs-lookup"><span data-stu-id="8317e-138">For more information, see [Reading an Object's objectGUID and Creating a String Representation of the GUID](reading-an-objectampaposs-objectguid-and-creating-a-string-representation-of-the-guid.md).</span></span> <span data-ttu-id="8317e-139">Para obtener más información sobre cómo establecer la propiedad **otherWellKnownObjects** en objetos, vea [Habilitar el enlace de Rename-Safe con la propiedad otherWellKnownObjects](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md).</span><span class="sxs-lookup"><span data-stu-id="8317e-139">For more information about setting the **otherWellKnownObjects** property on objects, see [Enabling Rename-Safe Binding with the otherWellKnownObjects Property](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md).</span></span>

<span data-ttu-id="8317e-140">Para enlazar a un objeto especificado en **wellKnownObjects** en domainDNS o en contenedores de configuración, especifique " &lt; xxxxx &gt; " como una de las constantes siguientes, que se enumeran en la tabla siguiente, tal como se define en ntdsapi. h.</span><span class="sxs-lookup"><span data-stu-id="8317e-140">To bind to an object specified in **wellKnownObjects** in domainDNS or configuration containers, specify "&lt;XXXXX&gt;" as one of the following constants, listed in the following table, as defined in Ntdsapi.h.</span></span>



| <span data-ttu-id="8317e-141">Contenedor</span><span class="sxs-lookup"><span data-stu-id="8317e-141">Container</span></span>          | <span data-ttu-id="8317e-142">Identificador GUID</span><span class="sxs-lookup"><span data-stu-id="8317e-142">GUID Identifier</span></span>                         |
|--------------------|-----------------------------------------|
| <span data-ttu-id="8317e-143">Usuarios</span><span class="sxs-lookup"><span data-stu-id="8317e-143">Users</span></span>              | <span data-ttu-id="8317e-144">contenedor de usuarios de GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="8317e-144">GUID\_USERS\_CONTAINER\_W</span></span>               |
| <span data-ttu-id="8317e-145">Computers</span><span class="sxs-lookup"><span data-stu-id="8317e-145">Computers</span></span>          | <span data-ttu-id="8317e-146">\_contenedor de calculadores GUID \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="8317e-146">GUID\_COMPUTRS\_CONTAINER\_W</span></span>            |
| <span data-ttu-id="8317e-147">System</span><span class="sxs-lookup"><span data-stu-id="8317e-147">System</span></span>             | <span data-ttu-id="8317e-148">\_contenedor de sistemas GUID \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="8317e-148">GUID\_SYSTEMS\_CONTAINER\_W</span></span>             |
| <span data-ttu-id="8317e-149">Controladores de dominio</span><span class="sxs-lookup"><span data-stu-id="8317e-149">Domain Controllers</span></span> | <span data-ttu-id="8317e-150">\_contenedor de controladores de dominio GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="8317e-150">GUID\_DOMAIN\_CONTROLLERS\_CONTAINER\_W</span></span> |
| <span data-ttu-id="8317e-151">Infraestructura</span><span class="sxs-lookup"><span data-stu-id="8317e-151">Infrastructure</span></span>     | <span data-ttu-id="8317e-152">\_contenedor de infraestructura GUID \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="8317e-152">GUID\_INFRASTRUCTURE\_CONTAINER\_W</span></span>      |
| <span data-ttu-id="8317e-153">Objetos eliminados</span><span class="sxs-lookup"><span data-stu-id="8317e-153">Deleted Objects</span></span>    | <span data-ttu-id="8317e-154">\_contenedor de objetos eliminados de GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="8317e-154">GUID\_DELETED\_OBJECTS\_CONTAINER\_W</span></span>    |
| <span data-ttu-id="8317e-155">Perdido y encontrado</span><span class="sxs-lookup"><span data-stu-id="8317e-155">Lost and Found</span></span>     | <span data-ttu-id="8317e-156">contenedor de GUID \_ LOSTANDFOUND \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="8317e-156">GUID\_LOSTANDFOUND\_CONTAINER\_W</span></span>        |



 

<span data-ttu-id="8317e-157">Por ejemplo, para enlazar con el contenedor de usuario en un dominio, especifique el **\_ contenedor de usuarios GUID \_ \_ W** como " &lt; xxxxx &gt; ".</span><span class="sxs-lookup"><span data-stu-id="8317e-157">For example, to bind to the user container in a domain, specify **GUID\_USERS\_CONTAINER\_W** as "&lt;XXXXX&gt;".</span></span>

<span data-ttu-id="8317e-158">" &lt; DN &gt; de contenedor" es el nombre distintivo del objeto contenedor que tiene este objeto representado como un valor en su propiedad **wellKnownObjects** .</span><span class="sxs-lookup"><span data-stu-id="8317e-158">"&lt;container DN&gt;" is the distinguished name of the container object that has this object represented as a value in its **wellKnownObjects** property.</span></span> <span data-ttu-id="8317e-159">Por ejemplo, para enlazar con el contenedor usuarios de un dominio, especifique el nombre distintivo del dominio como el " &lt; DN del contenedor &gt; ".</span><span class="sxs-lookup"><span data-stu-id="8317e-159">For example, to bind to the users container in a domain, specify the domain distinguished name as the "&lt;container DN&gt;".</span></span>

<span data-ttu-id="8317e-160">Por ejemplo, para enlazar con el contenedor de usuarios del dominio Fabrikam.com, use la siguiente cadena de enlace.</span><span class="sxs-lookup"><span data-stu-id="8317e-160">For example, to bind to the users container of the domain Fabrikam.com, use the following binding string.</span></span>

``` syntax
LDAP://<WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=Fabrikam,dc=com>
```

<span data-ttu-id="8317e-161">Para obtener más información y un ejemplo de código que muestra cómo enlazar a un GUID conocido, vea [código de ejemplo para enlazar a objetos conocidos](example-code-for-binding-to-well-known-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8317e-161">For more information and a code example that shows how to bind to a well-known GUID, see [Example Code for Binding to Well Known Objects](example-code-for-binding-to-well-known-objects.md).</span></span>

 

 