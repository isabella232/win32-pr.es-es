---
title: Uso de Active Directory Domain Services
description: En esta sección se proporcionan instrucciones para escribir aplicaciones que usan o publican datos en un servicio de directorio de Active Directory.
ms.assetid: 2ae20169-08a5-4e15-8430-ea99a917725f
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, usar
- Active Directory Domain Services Active Directory, usar
- Active Directory ejemplos Active Directory
- Active Directory Domain Services ejemplos Active Directory
- ejemplos Active Directory
- Active Directory Active Directory, ejemplos vea ejemplos de Active Directory Domain Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540b9004311db320decbd15c4f0a29e52ec1302a
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797061"
---
# <a name="using-active-directory-domain-services"></a><span data-ttu-id="d8c78-109">Uso de Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="d8c78-109">Using Active Directory Domain Services</span></span>

<span data-ttu-id="d8c78-110">En esta sección se proporcionan instrucciones para escribir aplicaciones que usan o publican datos en un servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d8c78-110">This section provides guidelines for writing applications that use or publish data in an Active Directory directory service.</span></span>

> [!Note]  
> <span data-ttu-id="d8c78-111">La siguiente documentación es para programadores de equipos.</span><span class="sxs-lookup"><span data-stu-id="d8c78-111">The following documentation is for computer programmers.</span></span> <span data-ttu-id="d8c78-112">Si está intentando resolver un error de impresión de Active Directory Home, consulte la [siguiente sugerencia](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) en las páginas de la comunidad de Microsoft: Si eso no ayuda, Pruebe estas recomendaciones desde [technet](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint).</span><span class="sxs-lookup"><span data-stu-id="d8c78-112">If you are trying to resolve an Active Directory home printing error, see the [following suggestion](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) from the Microsoft community pages; if that doesn't help, try these recommendations from [TechNet](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint).</span></span>

 

<span data-ttu-id="d8c78-113">Active Directory Domain Services son compatibles con el Protocolo ligero de acceso a directorios 3,0, definido por RFC 2251 y otras RFC.</span><span class="sxs-lookup"><span data-stu-id="d8c78-113">Active Directory Domain Services are compliant with Lightweight Directory Access Protocol 3.0, which is defined by RFC 2251 and other RFCs.</span></span> <span data-ttu-id="d8c78-114">Cualquiera de los siguientes conjuntos de API se puede usar para tener acceso a Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="d8c78-114">Any of the following API sets can be used to access Active Directory Domain Services.</span></span> <span data-ttu-id="d8c78-115">Cada conjunto de API tiene ventajas y desventajas que dependen del lenguaje de programación, el entorno de programación y el método de ejecución previsto.</span><span class="sxs-lookup"><span data-stu-id="d8c78-115">Each API set has advantages and disadvantages that depend on the programming language, programming environment, and intended method of execution.</span></span> <span data-ttu-id="d8c78-116">La mayoría de los ejemplos de esta guía usan ADSI, que es compatible con lenguajes como C y C++, así como con lenguajes compatibles con la automatización, como Microsoft Visual Basic y Visual Basic Scripting Edition.</span><span class="sxs-lookup"><span data-stu-id="d8c78-116">The majority of the examples in this guide use ADSI, which is supported by languages such as C and C++, as well as automation-compliant languages such as Microsoft Visual Basic and Visual Basic Scripting Edition.</span></span>

<span data-ttu-id="d8c78-117">Para obtener más información acerca de las tecnologías de Active Directory Domain Services específicas, consulte:</span><span class="sxs-lookup"><span data-stu-id="d8c78-117">For more information about specific Active Directory Domain Services technologies, see:</span></span>

-   [<span data-ttu-id="d8c78-118">Protocolo ligero de acceso a directorio</span><span class="sxs-lookup"><span data-stu-id="d8c78-118">Lightweight Directory Access Protocol</span></span>](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api)
-   [<span data-ttu-id="d8c78-119">Interfaces de servicio de Active Directory</span><span class="sxs-lookup"><span data-stu-id="d8c78-119">Active Directory Service Interfaces</span></span>](../adsi/active-directory-service-interfaces-adsi.md)
-   [<span data-ttu-id="d8c78-120">System.DirectoryServices</span><span class="sxs-lookup"><span data-stu-id="d8c78-120">System.DirectoryServices</span></span>](/dotnet/api/system.directoryservices)

<span data-ttu-id="d8c78-121">En esta sección se tratan los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="d8c78-121">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="d8c78-122">Enlazar a Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="d8c78-122">Binding to Active Directory Domain Services</span></span>](binding-to-active-directory-domain-services.md)
-   [<span data-ttu-id="d8c78-123">Búsqueda en Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="d8c78-123">Searching in Active Directory Domain Services</span></span>](searching-in-active-directory-domain-services.md)
-   [<span data-ttu-id="d8c78-124">Crear y eliminar objetos en Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="d8c78-124">Creating and Deleting Objects in Active Directory Domain Services</span></span>](creating-and-deleting-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="d8c78-125">Mover objetos</span><span class="sxs-lookup"><span data-stu-id="d8c78-125">Moving Objects</span></span>](moving-objects.md)
-   [<span data-ttu-id="d8c78-126">Leer y escribir atributos de objetos en Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="d8c78-126">Reading and Writing Attributes of Objects in Active Directory Domain Services</span></span>](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="d8c78-127">Controlar el acceso a objetos en Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="d8c78-127">Controlling Access to Objects in Active Directory Domain Services</span></span>](controlling-access-to-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="d8c78-128">Extender el esquema</span><span class="sxs-lookup"><span data-stu-id="d8c78-128">Extending the Schema</span></span>](extending-the-schema.md)
-   [<span data-ttu-id="d8c78-129">Extensión de la interfaz de usuario para objetos de directorio</span><span class="sxs-lookup"><span data-stu-id="d8c78-129">Extending the User Interface for Directory Objects</span></span>](extending-the-user-interface-for-directory-objects.md)
-   [<span data-ttu-id="d8c78-130">Administración de usuarios</span><span class="sxs-lookup"><span data-stu-id="d8c78-130">Managing Users</span></span>](managing-users.md)
-   [<span data-ttu-id="d8c78-131">Administración de grupos</span><span class="sxs-lookup"><span data-stu-id="d8c78-131">Managing Groups</span></span>](managing-groups.md)
-   [<span data-ttu-id="d8c78-132">Seguimiento de cambios</span><span class="sxs-lookup"><span data-stu-id="d8c78-132">Tracking Changes</span></span>](tracking-changes.md)
-   [<span data-ttu-id="d8c78-133">Publicación de servicios</span><span class="sxs-lookup"><span data-stu-id="d8c78-133">Service Publication</span></span>](service-publication.md)
-   [<span data-ttu-id="d8c78-134">Cuentas de inicio de sesión de servicio</span><span class="sxs-lookup"><span data-stu-id="d8c78-134">Service Logon Accounts</span></span>](service-logon-accounts.md)
-   [<span data-ttu-id="d8c78-135">Autenticación mutua con Kerberos</span><span class="sxs-lookup"><span data-stu-id="d8c78-135">Mutual Authentication Using Kerberos</span></span>](mutual-authentication-using-kerberos.md)
-   [<span data-ttu-id="d8c78-136">Realizar copias de seguridad y restaurar Active Directory</span><span class="sxs-lookup"><span data-stu-id="d8c78-136">Backing Up and Restoring Active Directory</span></span>](backing-up-and-restoring-an-active-directory-server.md)
-   [<span data-ttu-id="d8c78-137">Almacenar datos dinámicos</span><span class="sxs-lookup"><span data-stu-id="d8c78-137">Storing Dynamic Data</span></span>](storing-dynamic-data.md)
-   [<span data-ttu-id="d8c78-138">Particiones de directorio de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d8c78-138">Application Directory Partitions</span></span>](application-directory-partitions.md)
-   [<span data-ttu-id="d8c78-139">Detección del modo de operación de un dominio</span><span class="sxs-lookup"><span data-stu-id="d8c78-139">Detecting the Operation Mode of a Domain</span></span>](detecting-the-operation-mode-of-a-domain.md)

 

 