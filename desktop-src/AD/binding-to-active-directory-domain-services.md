---
title: Enlazar a Active Directory Domain Services
description: En Active Directory Domain Services, el acto de asociar un objeto de programación a un objeto de Active Directory Domain Services específico se conoce como enlace.
ms.assetid: f48de4d4-c53a-4e40-a34e-4236c3e6cb21
ms.tgt_platform: multiple
keywords:
- enlazar a Active Directory Domain Services Active Directory
- Active Directory Domain Services Active Directory, enlazar a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f57aef2b2a3c21ac860d05dd1b7a1e1079d1720
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998135"
---
# <a name="binding-to-active-directory-domain-services"></a><span data-ttu-id="3ffbb-105">Enlazar a Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="3ffbb-105">Binding to Active Directory Domain Services</span></span>

<span data-ttu-id="3ffbb-106">En Active Directory Domain Services, el acto de asociar un objeto de programación a un objeto de Active Directory Domain Services específico se conoce como *enlace*.</span><span class="sxs-lookup"><span data-stu-id="3ffbb-106">In Active Directory Domain Services, the act of associating a programmatic object with a specific Active Directory Domain Services object is known as *binding*.</span></span> <span data-ttu-id="3ffbb-107">Cuando un objeto de programación, como un objeto [**IADs**](/windows/desktop/api/iads/nn-iads-iads) o [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry?view=dotnet-plat-ext-3.1&preserve-view=true) , está asociado a un objeto de directorio específico, se considera que el objeto de programación está *enlazado al* objeto de directorio.</span><span class="sxs-lookup"><span data-stu-id="3ffbb-107">When a programmatic object, such as an [**IADs**](/windows/desktop/api/iads/nn-iads-iads) or [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry?view=dotnet-plat-ext-3.1&preserve-view=true) object, is associated with a specific directory object, the programmatic object is considered to be *bound to* the directory object.</span></span>

## <a name="binding-functions-and-methods"></a><span data-ttu-id="3ffbb-108">Funciones y métodos de enlace</span><span class="sxs-lookup"><span data-stu-id="3ffbb-108">Binding Functions and Methods</span></span>

<span data-ttu-id="3ffbb-109">El método para enlazar mediante programación a un objeto Active Directory dependerá de la tecnología de programación que se use.</span><span class="sxs-lookup"><span data-stu-id="3ffbb-109">The method for programmatically binding to an Active Directory object will depend on the programming technology that is used.</span></span> <span data-ttu-id="3ffbb-110">Para obtener más información sobre cómo enlazar a objetos en Active Directory Domain Services con una tecnología de programación específica, vea los temas que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3ffbb-110">For more information about binding to objects in Active Directory Domain Services with a specific programming technology, see the topics listed in the following table.</span></span>



| <span data-ttu-id="3ffbb-111">Tecnología de programación</span><span class="sxs-lookup"><span data-stu-id="3ffbb-111">Programming technology</span></span>                                                                       | <span data-ttu-id="3ffbb-112">Para obtener más información</span><span class="sxs-lookup"><span data-stu-id="3ffbb-112">For more information</span></span>                                                           |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="3ffbb-113">Interfaces de servicio de Active Directory</span><span class="sxs-lookup"><span data-stu-id="3ffbb-113">Active Directory Service Interfaces</span></span>](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [<span data-ttu-id="3ffbb-114">Enlazar a un objeto ADSI</span><span class="sxs-lookup"><span data-stu-id="3ffbb-114">Binding to an ADSI Object</span></span>](/windows/desktop/ADSI/binding-to-an-adsi-object)                    |
| [<span data-ttu-id="3ffbb-115">Protocolo ligero de acceso a directorio</span><span class="sxs-lookup"><span data-stu-id="3ffbb-115">Lightweight Directory Access Protocol</span></span>](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [<span data-ttu-id="3ffbb-116">Establecer una sesión LDAP</span><span class="sxs-lookup"><span data-stu-id="3ffbb-116">Establishing an LDAP Session</span></span>](/previous-versions/windows/desktop/ldap/establishing-an-ldap-session)              |
| [<span data-ttu-id="3ffbb-117">System.DirectoryServices</span><span class="sxs-lookup"><span data-stu-id="3ffbb-117">System.DirectoryServices</span></span>](/dotnet/api/system.directoryservices)                 | <span data-ttu-id="3ffbb-118">[Enlazar a objetos de directorio](/previous-versions/ms180840(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="3ffbb-118">[Binding to Directory Objects](/previous-versions/ms180840(v=vs.90))</span></span> |



 

## <a name="binding-strings"></a><span data-ttu-id="3ffbb-119">Enlazar cadenas</span><span class="sxs-lookup"><span data-stu-id="3ffbb-119">Binding Strings</span></span>

<span data-ttu-id="3ffbb-120">Todas las funciones y métodos de enlace requieren una cadena de enlace.</span><span class="sxs-lookup"><span data-stu-id="3ffbb-120">All bind functions and methods require a binding string.</span></span> <span data-ttu-id="3ffbb-121">El formato de la cadena de enlace depende del proveedor.</span><span class="sxs-lookup"><span data-stu-id="3ffbb-121">The form of the binding string depends on the provider.</span></span> <span data-ttu-id="3ffbb-122">Los Active Directory Domain Services admiten dos proveedores, LDAP y Winnt.</span><span class="sxs-lookup"><span data-stu-id="3ffbb-122">Active Directory Domain Services are supported by two providers, LDAP and WinNT.</span></span>

<span data-ttu-id="3ffbb-123">A partir de Windows 2000, el proveedor LDAP se usa para tener acceso a Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="3ffbb-123">Beginning with Windows 2000, the LDAP provider is used to access Active Directory Domain Services.</span></span> <span data-ttu-id="3ffbb-124">La cadena de enlace LDAP puede adoptar una de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="3ffbb-124">The LDAP binding string can take one of the following forms:</span></span>

-   <span data-ttu-id="3ffbb-125">"LDAP:// <host name> / <object name> "</span><span class="sxs-lookup"><span data-stu-id="3ffbb-125">"LDAP://<host name>/<object name>"</span></span>
-   <span data-ttu-id="3ffbb-126">"GC:// <host name> / <object name> "</span><span class="sxs-lookup"><span data-stu-id="3ffbb-126">"GC://<host name>/<object name>"</span></span>

<span data-ttu-id="3ffbb-127">En los ejemplos anteriores, "LDAP:" especifica el proveedor LDAP.</span><span class="sxs-lookup"><span data-stu-id="3ffbb-127">In the examples above, "LDAP:" specifies the LDAP provider.</span></span> <span data-ttu-id="3ffbb-128">"GC:" utiliza el proveedor LDAP para enlazar con el servicio de catálogo global para ejecutar consultas rápidas.</span><span class="sxs-lookup"><span data-stu-id="3ffbb-128">"GC:" uses the LDAP provider to bind to the Global Catalog service to execute fast queries.</span></span>

<span data-ttu-id="3ffbb-129">" &lt; nombre &gt; de host" especifica el servidor al que se va a enlazar y es opcional.</span><span class="sxs-lookup"><span data-stu-id="3ffbb-129">"&lt;host name&gt;" specifies the server to bind to and is optional.</span></span> <span data-ttu-id="3ffbb-130">Si es posible, no especifique un servidor.</span><span class="sxs-lookup"><span data-stu-id="3ffbb-130">If possible, do not specify a server.</span></span> <span data-ttu-id="3ffbb-131">También es posible enlazar a un objeto en un dominio diferente.</span><span class="sxs-lookup"><span data-stu-id="3ffbb-131">It is also possible to bind to an object in a different domain.</span></span> <span data-ttu-id="3ffbb-132">Para ello, pase el nombre del sistema de nombres de dominio (DNS) del dominio de destino para " &lt; nombre de host &gt; ".</span><span class="sxs-lookup"><span data-stu-id="3ffbb-132">To do this pass the domain naming system (DNS) name of the target domain for "&lt;host name&gt;".</span></span> <span data-ttu-id="3ffbb-133">Por ejemplo, para enlazar con el contenedor usuarios en el dominio dominio2 de fabrikam.com, la cadena de enlace sería "LDAP://domain2.fabrikam.com/CN=Users,DC=domain2,DC=fabrikam,DC=com".</span><span class="sxs-lookup"><span data-stu-id="3ffbb-133">For example, to bind to the Users container in the domain2 domain of fabrikam.com, the binding string would be "LDAP://domain2.fabrikam.com/CN=Users,DC=domain2,DC=fabrikam,DC=com".</span></span>

<span data-ttu-id="3ffbb-134">" &lt; Object name &gt; " representa un objeto específico en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="3ffbb-134">"&lt;object name&gt;" represents a specific object in Active Directory Domain Services.</span></span> <span data-ttu-id="3ffbb-135">El nombre del objeto puede ser un nombre distintivo o un GUID del objeto.</span><span class="sxs-lookup"><span data-stu-id="3ffbb-135">The object name can be a distinguished name or an object GUID.</span></span>

<span data-ttu-id="3ffbb-136">Para obtener más información acerca de las cadenas de enlace LDAP, consulte [ADsPath de LDAP](/windows/desktop/ADSI/ldap-adspath).</span><span class="sxs-lookup"><span data-stu-id="3ffbb-136">For more information about LDAP binding strings, see [LDAP ADsPath](/windows/desktop/ADSI/ldap-adspath).</span></span>

<span data-ttu-id="3ffbb-137">En Windows NT 4,0, el proveedor de WinNT se usa para el acceso a datos de directorio como usuarios, grupos de usuarios, equipos, servicios y otros objetos de red en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="3ffbb-137">For Windows NT 4.0, the WinNT provider is used for access to directory data such as users, user groups, computers, services, and other network objects in the Windows 2000.</span></span> <span data-ttu-id="3ffbb-138">El proveedor de WinNT en Windows 2000 y sistemas posteriores tiene una funcionalidad limitada en comparación con el proveedor LDAP.</span><span class="sxs-lookup"><span data-stu-id="3ffbb-138">The WinNT provider on Windows 2000 and later systems has limited functionality compared to the LDAP provider.</span></span> <span data-ttu-id="3ffbb-139">Para obtener más información sobre las cadenas de enlace de WinNT, vea [WinNT ADsPath](/windows/desktop/ADSI/winnt-adspath).</span><span class="sxs-lookup"><span data-stu-id="3ffbb-139">For more information about WinNT binding strings, see [WinNT ADsPath](/windows/desktop/ADSI/winnt-adspath).</span></span>

<span data-ttu-id="3ffbb-140">Se puede usar un ADsPath de "LDAP://" o "GC://" para enlazar con la raíz del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="3ffbb-140">An ADsPath of "LDAP://" or "GC://" can be used to bind to the root of the namespace.</span></span> <span data-ttu-id="3ffbb-141">Cuando se enlaza a la raíz del espacio de nombres, el objeto de espacio de nombres proporcionado no contiene ninguna propiedad y contiene el objeto de dominio para LDAP y un objeto contenedor que contiene una réplica parcial de todos los dominios del bosque para GC.</span><span class="sxs-lookup"><span data-stu-id="3ffbb-141">When bound to the root of the namespace, the supplied namespace object contains no properties and contains the domain object for LDAP and a container object containing a partial replica of all domains in the forest for GC.</span></span>

<span data-ttu-id="3ffbb-142">Para obtener más información sobre el enlace en Active Directory Domain Services, vea:</span><span class="sxs-lookup"><span data-stu-id="3ffbb-142">For more information about binding in Active Directory Domain Services, see:</span></span>

-   [<span data-ttu-id="3ffbb-143">Enlace sin servidor y RootDSE</span><span class="sxs-lookup"><span data-stu-id="3ffbb-143">Serverless Binding and RootDSE</span></span>](serverless-binding-and-rootdse.md)
-   [<span data-ttu-id="3ffbb-144">Enlazar con el catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ffbb-144">Binding to the Global Catalog</span></span>](binding-to-the-global-catalog.md)
-   [<span data-ttu-id="3ffbb-145">Usar objectGUID para enlazar a un objeto</span><span class="sxs-lookup"><span data-stu-id="3ffbb-145">Using objectGUID to Bind to an Object</span></span>](using-objectguid-to-bind-to-an-object.md)
-   [<span data-ttu-id="3ffbb-146">Enlazar a objetos de Well-Known mediante WKGUID</span><span class="sxs-lookup"><span data-stu-id="3ffbb-146">Binding to Well-Known Objects Using WKGUID</span></span>](binding-to-well-known-objects-using-wkguid.md)
-   [<span data-ttu-id="3ffbb-147">Enlazar a un objeto mediante un SID</span><span class="sxs-lookup"><span data-stu-id="3ffbb-147">Binding to an Object Using a SID</span></span>](binding-to-an-object-using-a-sid.md)
-   [<span data-ttu-id="3ffbb-148">Habilitar Rename-Safe enlace con la propiedad otherWellKnownObjects</span><span class="sxs-lookup"><span data-stu-id="3ffbb-148">Enabling Rename-Safe Binding with the otherWellKnownObjects Property</span></span>](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md)
-   [<span data-ttu-id="3ffbb-149">Autenticación</span><span class="sxs-lookup"><span data-stu-id="3ffbb-149">Authentication</span></span>](authentication.md)

 

 
