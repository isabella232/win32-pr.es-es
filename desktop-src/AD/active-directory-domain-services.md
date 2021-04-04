---
title: Servicios de dominio de Active Directory
description: Microsoft Active Directory Domain Services es la base de las redes distribuidas basadas en los sistemas operativos Windows 2000 Server, Windows Server 2003 y Microsoft Windows Server 2008 que usan controladores de dominio.
ms.assetid: 9fc78c72-c59c-4c4d-ace5-00a431645c4b
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory
- Active Directory de Active Directory, página de inicio
- Active Directory de Active Directory Domain Services, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0270f331a68d23ad89a8e5a999f8cabd95487020
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104078572"
---
# <a name="active-directory-domain-services"></a><span data-ttu-id="c78d7-106">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="c78d7-106">Active Directory Domain Services</span></span>

## <a name="purpose"></a><span data-ttu-id="c78d7-107">Propósito</span><span class="sxs-lookup"><span data-stu-id="c78d7-107">Purpose</span></span>

<span data-ttu-id="c78d7-108">Microsoft Active Directory Domain Services es la base de las redes distribuidas basadas en los sistemas operativos Windows 2000 Server, Windows Server 2003 y Microsoft Windows Server 2008 que usan controladores de dominio.</span><span class="sxs-lookup"><span data-stu-id="c78d7-108">Microsoft Active Directory Domain Services are the foundation for distributed networks built on Windows 2000 Server, Windows Server 2003 and Microsoft Windows Server 2008 operating systems that use domain controllers.</span></span> <span data-ttu-id="c78d7-109">Active Directory Domain Services proporcionan almacenamiento jerárquico de datos seguro y estructurado para objetos en una red como usuarios, equipos, impresoras y servicios.</span><span class="sxs-lookup"><span data-stu-id="c78d7-109">Active Directory Domain Services provide secure, structured, hierarchical data storage for objects in a network such as users, computers, printers, and services.</span></span> <span data-ttu-id="c78d7-110">Active Directory Domain Services proporcionan compatibilidad para buscar y trabajar con estos objetos.</span><span class="sxs-lookup"><span data-stu-id="c78d7-110">Active Directory Domain Services provide support for locating and working with these objects.</span></span>

<span data-ttu-id="c78d7-111">En esta guía se proporciona información general sobre Active Directory Domain Services y el código de ejemplo para tareas básicas, como buscar objetos y leer propiedades, para tareas más avanzadas, como la publicación de servicio.</span><span class="sxs-lookup"><span data-stu-id="c78d7-111">This guide provides an overview of Active Directory Domain Services and sample code for basic tasks, such as searching for objects and reading properties, to more advanced tasks such as service publication.</span></span>

<span data-ttu-id="c78d7-112">Windows 2000 Server y los sistemas operativos posteriores proporcionan una interfaz de usuario para que los usuarios y administradores puedan trabajar con los objetos y datos de Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="c78d7-112">Windows 2000 Server and later operating systems provide a user interface for users and administrators to work with the objects and data in Active Directory Domain Services.</span></span> <span data-ttu-id="c78d7-113">En esta guía se describe cómo extender y personalizar esa interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c78d7-113">This guide describes how to extend and customize that user interface.</span></span> <span data-ttu-id="c78d7-114">También se describe cómo extender Active Directory Domain Services definiendo nuevas clases de objetos y atributos.</span><span class="sxs-lookup"><span data-stu-id="c78d7-114">It also describes how to extend Active Directory Domain Services by defining new object classes and attributes.</span></span>

> [!Note]  
> <span data-ttu-id="c78d7-115">La siguiente documentación es para programadores de equipos.</span><span class="sxs-lookup"><span data-stu-id="c78d7-115">The following documentation is for computer programmers.</span></span> <span data-ttu-id="c78d7-116">Si es un usuario final que está intentando depurar un error de impresión o un problema de la red doméstica, consulte los foros de la [comunidad de Microsoft](https://answers.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="c78d7-116">If you are an end-user trying to debug a printing error or home network issue, see the [Microsoft community forums](https://answers.microsoft.com).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="c78d7-117">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="c78d7-117">Where applicable</span></span>

<span data-ttu-id="c78d7-118">Los administradores de red escriben scripts y aplicaciones que tienen acceso a Active Directory Domain Services para automatizar las tareas administrativas comunes, como agregar usuarios y grupos, administrar impresoras y establecer permisos para los recursos de red.</span><span class="sxs-lookup"><span data-stu-id="c78d7-118">Network administrators write scripts and applications that access Active Directory Domain Services to automate common administrative tasks, such as adding users and groups, managing printers, and setting permissions for network resources.</span></span>

<span data-ttu-id="c78d7-119">Los fabricantes de software independientes y los desarrolladores de usuarios finales pueden usar Active Directory Domain Services programación para habilitar los productos y las aplicaciones en el directorio.</span><span class="sxs-lookup"><span data-stu-id="c78d7-119">Independent software vendors and end-user developers can use Active Directory Domain Services programming to directory-enable their products and applications.</span></span> <span data-ttu-id="c78d7-120">Los servicios pueden publicarse en Active Directory Domain Services; los clientes pueden usar Active Directory Domain Services para buscar servicios y ambos pueden usar Active Directory Domain Services para buscar otros objetos en una red y trabajar con ellos.</span><span class="sxs-lookup"><span data-stu-id="c78d7-120">Services can publish themselves in Active Directory Domain Services; clients can use Active Directory Domain Services to find services, and both can use Active Directory Domain Services to locate and work with other objects on a network.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="c78d7-121">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="c78d7-121">Developer audience</span></span>

<span data-ttu-id="c78d7-122">Las aplicaciones que tienen acceso a los datos de Active Directory Domain Services pueden escribirse mediante la API de [interfaces de servicio Active Directory](../adsi/active-directory-service-interfaces-adsi.md) , la API de [Protocolo ligero de acceso a directorios](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) o el espacio de nombres [System. DirectoryServices](/dotnet/api/system.directoryservices) .</span><span class="sxs-lookup"><span data-stu-id="c78d7-122">Applications that access data in Active Directory Domain Services can be written using the [Active Directory Service Interfaces](../adsi/active-directory-service-interfaces-adsi.md) API, [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) API, or the [System.DirectoryServices](/dotnet/api/system.directoryservices) namespace.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="c78d7-123">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="c78d7-123">Run-time requirements</span></span>

<span data-ttu-id="c78d7-124">Active Directory Domain Services ejecutar en controladores de dominio de Windows 2000 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="c78d7-124">Active Directory Domain Services run on Windows 2000 and later domain controllers.</span></span> <span data-ttu-id="c78d7-125">Sin embargo, las aplicaciones cliente se pueden escribir y ejecutar en Windows Vista, Windows Server 2003, Windows XP, Windows 2000, Windows NT 4,0, Windows 98 y Windows 95.</span><span class="sxs-lookup"><span data-stu-id="c78d7-125">However, client applications can be written for and run on Windows Vista, Windows Server 2003, Windows XP, Windows 2000, Windows NT 4.0, Windows 98, and Windows 95.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c78d7-126">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c78d7-126">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="c78d7-127">Acerca de Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="c78d7-127">About Active Directory Domain Services</span></span>](about-active-directory-domain-services.md)
</dt> <dd>

<span data-ttu-id="c78d7-128">Información general sobre Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="c78d7-128">General information about Active Directory Domain Services.</span></span>

</dd> <dt>

[<span data-ttu-id="c78d7-129">Uso de Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="c78d7-129">Using Active Directory Domain Services</span></span>](using-active-directory-domain-services.md)
</dt> <dd>

<span data-ttu-id="c78d7-130">Active Directory Domain Services guía de programación.</span><span class="sxs-lookup"><span data-stu-id="c78d7-130">Active Directory Domain Services programming guide.</span></span>

</dd> <dt>

[<span data-ttu-id="c78d7-131">Referencia de Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="c78d7-131">Active Directory Domain Services Reference</span></span>](active-directory-domain-services-reference.md)
</dt> <dd>

<span data-ttu-id="c78d7-132">Referencia de programación de Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="c78d7-132">Active Directory Domain Services programming reference.</span></span>

</dd> </dl>

 

 