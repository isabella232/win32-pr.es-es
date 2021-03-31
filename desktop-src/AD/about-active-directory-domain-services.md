---
title: Acerca de Active Directory Domain Services
description: Esta guía proporciona información esencial para la integración de Microsoft Active Directory en aplicaciones distribuidas diseñadas para sistemas operativos compatibles con Active Directory.
ms.assetid: cc6c63dd-ae22-40a7-8312-0a4648bb92bd
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, acerca de
- Active Directory Active Directory Domain Services, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d8dafb89533d796f0651ad08b913eacda1d0fe9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077796"
---
# <a name="about-active-directory-domain-services"></a><span data-ttu-id="6999c-105">Acerca de Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="6999c-105">About Active Directory Domain Services</span></span>

## <a name="writing-powerful-applications-that-use-active-directory-domain-services"></a><span data-ttu-id="6999c-106">Escritura de aplicaciones eficaces que usan Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="6999c-106">Writing Powerful Applications that Use Active Directory Domain Services</span></span>

<span data-ttu-id="6999c-107">Esta guía proporciona información esencial para la integración de Active Directory Domain Services en aplicaciones distribuidas diseñadas para sistemas operativos que admiten Active Directory Domain Services, incluidos:</span><span class="sxs-lookup"><span data-stu-id="6999c-107">This guide provides essential information for integrating Active Directory Domain Services in distributed applications designed for operating systems that support Active Directory Domain Services, including:</span></span>

-   <span data-ttu-id="6999c-108">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6999c-108">Windows Server 2008</span></span>
-   <span data-ttu-id="6999c-109">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6999c-109">Windows Server 2008 R2</span></span>
-   <span data-ttu-id="6999c-110">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6999c-110">Windows Server 2012</span></span>
-   <span data-ttu-id="6999c-111">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6999c-111">Windows Server 2012 R2</span></span>
-   <span data-ttu-id="6999c-112">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6999c-112">Windows Server 2016</span></span>

> [!Note]  
> <span data-ttu-id="6999c-113">Estos temas son para desarrolladores de software.</span><span class="sxs-lookup"><span data-stu-id="6999c-113">These topics are for software developers.</span></span> <span data-ttu-id="6999c-114">Para problemas de soporte técnico, consulte [soporte técnico de Microsoft](https://windows.microsoft.com/windows/support#1tc).</span><span class="sxs-lookup"><span data-stu-id="6999c-114">For support issues, see [Microsoft Support](https://windows.microsoft.com/windows/support#1tc).</span></span> <span data-ttu-id="6999c-115">Para obtener información acerca de la administración de Active Directory, consulte [Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) en TechNet.</span><span class="sxs-lookup"><span data-stu-id="6999c-115">For information about administering Active Directory, see [Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) at TechNet.</span></span>

 

## <a name="fundamental-directory-features"></a><span data-ttu-id="6999c-116">Características fundamentales de los directorios</span><span class="sxs-lookup"><span data-stu-id="6999c-116">Fundamental Directory Features</span></span>

<span data-ttu-id="6999c-117">Un servicio de directorio es un servicio fundamental para las aplicaciones distribuidas.</span><span class="sxs-lookup"><span data-stu-id="6999c-117">A directory service is a fundamental service for distributed applications.</span></span> <span data-ttu-id="6999c-118">Un servicio de directorio debe proporcionar las características que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6999c-118">A directory service must provide the features listed in the following table.</span></span>



| <span data-ttu-id="6999c-119">Característica</span><span class="sxs-lookup"><span data-stu-id="6999c-119">Feature</span></span>               | <span data-ttu-id="6999c-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="6999c-120">Description</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6999c-121">Transparencia de ubicación</span><span class="sxs-lookup"><span data-stu-id="6999c-121">Location transparency</span></span> | <span data-ttu-id="6999c-122">Puede encontrar datos de usuario, grupo, servicio en red o recurso, sin la dirección del objeto.</span><span class="sxs-lookup"><span data-stu-id="6999c-122">Able to find user, group, networked service, or resource, data without the object address</span></span>           |
| <span data-ttu-id="6999c-123">Datos de objeto</span><span class="sxs-lookup"><span data-stu-id="6999c-123">Object data</span></span>           | <span data-ttu-id="6999c-124">Puede almacenar datos de usuarios, grupos, organizaciones y servicios en un árbol jerárquico</span><span class="sxs-lookup"><span data-stu-id="6999c-124">Able to store user, group, organization, and service data in a hierarchical tree</span></span>                    |
| <span data-ttu-id="6999c-125">Consulta enriquecida</span><span class="sxs-lookup"><span data-stu-id="6999c-125">Rich query</span></span>            | <span data-ttu-id="6999c-126">Puede localizar un objeto consultando las propiedades de los objetos</span><span class="sxs-lookup"><span data-stu-id="6999c-126">Able to locate an object by querying for object properties</span></span>                                          |
| <span data-ttu-id="6999c-127">Alta disponibilidad</span><span class="sxs-lookup"><span data-stu-id="6999c-127">High availability</span></span>     | <span data-ttu-id="6999c-128">Puede localizar una réplica del directorio en una ubicación que sea eficaz para las operaciones de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="6999c-128">Able to locate a replica of the directory at a location that is efficient for read/write operations</span></span> |



 

## <a name="advanced-features-of-active-directory-domain-services"></a><span data-ttu-id="6999c-129">Características avanzadas de Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="6999c-129">Advanced Features of Active Directory Domain Services</span></span>

<span data-ttu-id="6999c-130">Active Directory Domain Services proporciona las características que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6999c-130">Active Directory Domain Services provides the features listed in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6999c-131">Característica</span><span class="sxs-lookup"><span data-stu-id="6999c-131">Feature</span></span></th>
<th><span data-ttu-id="6999c-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6999c-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6999c-133">Compatibilidad con los estándares de Internet</span><span class="sxs-lookup"><span data-stu-id="6999c-133">Support for Internet standards</span></span></td>
<td><span data-ttu-id="6999c-134">Active Directory Domain Services implementa sus características de acuerdo con los estándares de Internet publicados como LDAP y DNS.</span><span class="sxs-lookup"><span data-stu-id="6999c-134">Active Directory Domain Services implements its features in accordance with published Internet standards such as LDAP and DNS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6999c-135">Seguridad estrechamente integrada y flexible</span><span class="sxs-lookup"><span data-stu-id="6999c-135">Tightly integrated and flexible security</span></span></td>
<td><span data-ttu-id="6999c-136">Entre las ventajas, se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="6999c-136">Advantages include:</span></span><br/>
<ul>
<li><span data-ttu-id="6999c-137">Elección de los paquetes de autenticación.</span><span class="sxs-lookup"><span data-stu-id="6999c-137">Choice of authentication packages.</span></span> <span data-ttu-id="6999c-138">Kerberos, Capa de sockets seguros (SSL) o una combinación; por ejemplo, establezca un canal SSL para el cifrado y, a continuación, use Kerberos para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="6999c-138">Kerberos, Secure Sockets Layer (SSL), or a combination; for example, establish an SSL channel for encryption and then use Kerberos for authentication.</span></span></li>
<li><span data-ttu-id="6999c-139">Administración central del acceso a recursos y servicios mediante el uso de usuarios y grupos en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="6999c-139">Central management of service and resource access by using the users and groups in Active Directory Domain Services.</span></span></li>
<li><span data-ttu-id="6999c-140">Delegación de la administración para que los administradores centrales puedan delegar tareas administrativas como el cambio de contraseña o la creación y eliminación de objetos específicos.</span><span class="sxs-lookup"><span data-stu-id="6999c-140">Delegation of administration so that central administrators can delegate administrative tasks such as password changing or specific object creation and deletion.</span></span></li>
<li><span data-ttu-id="6999c-141">El servidor de Active Directory usa los mismos mecanismos de control de acceso que se usan en sistemas de archivos de los sistemas operativos Windows.</span><span class="sxs-lookup"><span data-stu-id="6999c-141">The Active Directory server uses the same access control mechanisms used on file systems in the Windows operating systems.</span></span> <span data-ttu-id="6999c-142">Por lo tanto, las mismas herramientas que administran el control de acceso en un sistema de archivos funcionan para Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="6999c-142">Thus, the same tools that manage access control on a file system work for Active Directory Domain Services.</span></span></li>
<li><span data-ttu-id="6999c-143">Infraestructura de clave pública completa.</span><span class="sxs-lookup"><span data-stu-id="6999c-143">Comprehensive Public Key infrastructure.</span></span> <span data-ttu-id="6999c-144">Microsoft Certificate Server y la compatibilidad con tarjetas inteligentes se integran con Active Directory Domain Services para proporcionar inicio de sesión de tarjeta inteligente y administración de certificados.</span><span class="sxs-lookup"><span data-stu-id="6999c-144">The Microsoft Certificate Server and Smart Card support are integrated with Active Directory Domain Services to provide Smart Card logon and Certificate management.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6999c-145">Fácil de programar</span><span class="sxs-lookup"><span data-stu-id="6999c-145">Easily programmable</span></span></td>
<td><span data-ttu-id="6999c-146">Se puede tener acceso al servidor de Active Directory mediante programación y administrarlo mediante el Active Directory API de <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">interfaces de servicio</a> , la API de <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Protocolo ligero de acceso a directorios</a> o el espacio de nombres <a href="/dotnet/api/system.directoryservices">System. DirectoryServices</a> .</span><span class="sxs-lookup"><span data-stu-id="6999c-146">The Active Directory server can be programmatically accessed and administered using the <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">Active Directory Service Interfaces</a> API, <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol</a> API, or the <a href="/dotnet/api/system.directoryservices">System.DirectoryServices</a> namespace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6999c-147">Servicios del sistema habilitados para directorio</span><span class="sxs-lookup"><span data-stu-id="6999c-147">Directory enabled system services</span></span></td>
<td><span data-ttu-id="6999c-148">La aplicación cliente se puede implementar fácilmente en escritorios distribuidos mediante la creación de un paquete de Windows Installer y el uso de la característica de implementación de aplicaciones disponible en los sistemas operativos Windows.</span><span class="sxs-lookup"><span data-stu-id="6999c-148">Your client application can be easily deployed to distributed desktops by creating a Windows Installer package and using the application deployment feature available in the Windows operating systems.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6999c-149">Integración de aplicaciones clave</span><span class="sxs-lookup"><span data-stu-id="6999c-149">Key application integration</span></span></td>
<td><span data-ttu-id="6999c-150">Las aplicaciones clave distribuidas, como Exchange, se integran con Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="6999c-150">Key distributed applications, such as Exchange, are integrated with Active Directory Domain Services.</span></span> <span data-ttu-id="6999c-151">Por lo tanto, las empresas pueden reducir el número de servicios de directorio que se van a administrar.</span><span class="sxs-lookup"><span data-stu-id="6999c-151">Thus, companies can reduce the number of directory services to be managed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6999c-152">Esquema enriquecido y extensible</span><span class="sxs-lookup"><span data-stu-id="6999c-152">Rich and extensible schema</span></span></td>
<td><span data-ttu-id="6999c-153">El esquema define qué objetos y propiedades se pueden escribir y leer desde un servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="6999c-153">The schema defines what objects and properties can be written and read from a directory service.</span></span> <span data-ttu-id="6999c-154">El esquema Active Directory es rico.</span><span class="sxs-lookup"><span data-stu-id="6999c-154">The Active Directory Schema is rich.</span></span> <span data-ttu-id="6999c-155">La mayoría de los objetos y las propiedades que requiere un servicio están disponibles.</span><span class="sxs-lookup"><span data-stu-id="6999c-155">Most of the objects and properties a service requires are available.</span></span> <span data-ttu-id="6999c-156">Si no es así, una aplicación distribuida puede extender el esquema para admitir los requisitos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6999c-156">If not, a distributed application can extend the schema to support the application requirements.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6999c-157">Para obtener más información acerca de Active Directory Domain Services, vea:</span><span class="sxs-lookup"><span data-stu-id="6999c-157">For more information about Active Directory Domain Services, see:</span></span>

-   [<span data-ttu-id="6999c-158">Conceptos básicos de Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="6999c-158">Core Concepts of Active Directory Domain Services</span></span>](core-concepts-of-active-directory-domain-services.md)
-   [<span data-ttu-id="6999c-159">Arquitectura de Active Directory</span><span class="sxs-lookup"><span data-stu-id="6999c-159">Active Directory Architecture</span></span>](active-directory-domain-services-architecture.md)
-   [<span data-ttu-id="6999c-160">Esquema de Active Directory</span><span class="sxs-lookup"><span data-stu-id="6999c-160">Active Directory Schema</span></span>](active-directory-schema.md)

