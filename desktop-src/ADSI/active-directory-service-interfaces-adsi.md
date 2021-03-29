---
title: Interfaces de servicio de Active Directory
description: Introducción a las interfaces de Active Directory Services, con vínculos a diferentes guías.
ms.assetid: b24f9789-b9f5-49c4-9812-298bae8b28a9
ms.tgt_platform: multiple
keywords:
- ADSI ADSI
- Interfaces de servicio Active Directory (consulte ADSI)
- ADSI ADSI, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15cc702fec86f1202f1fbd00ba575fd848e4ab74
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078367"
---
# <a name="active-directory-service-interfaces"></a><span data-ttu-id="b023d-106">Interfaces de servicio de Active Directory</span><span class="sxs-lookup"><span data-stu-id="b023d-106">Active Directory Service Interfaces</span></span>

## <a name="purpose"></a><span data-ttu-id="b023d-107">Propósito</span><span class="sxs-lookup"><span data-stu-id="b023d-107">Purpose</span></span>

<span data-ttu-id="b023d-108">Active Directory interfaces de servicio (ADSI) es un conjunto de interfaces COM que se usan para tener acceso a las características de los servicios de directorio de proveedores de red diferentes.</span><span class="sxs-lookup"><span data-stu-id="b023d-108">Active Directory Service Interfaces (ADSI) is a set of COM interfaces used to access the features of directory services from different network providers.</span></span> <span data-ttu-id="b023d-109">ADSI se usa en un entorno informático distribuido para presentar un único conjunto de interfaces de servicios de directorio para administrar los recursos de red.</span><span class="sxs-lookup"><span data-stu-id="b023d-109">ADSI is used in a distributed computing environment to present a single set of directory service interfaces for managing network resources.</span></span> <span data-ttu-id="b023d-110">Los administradores y programadores pueden usar los servicios ADSI para enumerar y administrar los recursos de un servicio de directorio, independientemente del entorno de red que contenga el recurso.</span><span class="sxs-lookup"><span data-stu-id="b023d-110">Administrators and developers can use ADSI services to enumerate and manage the resources in a directory service, no matter which network environment contains the resource.</span></span>

<span data-ttu-id="b023d-111">ADSI permite realizar tareas administrativas comunes, como agregar nuevos usuarios, administrar impresoras y buscar recursos en un entorno de computación distribuida.</span><span class="sxs-lookup"><span data-stu-id="b023d-111">ADSI enables common administrative tasks, such as adding new users, managing printers, and locating resources in a distributed computing environment.</span></span>

> [!Note]  
> <span data-ttu-id="b023d-112">La siguiente documentación es para programadores de equipos.</span><span class="sxs-lookup"><span data-stu-id="b023d-112">The following documentation is for computer programmers.</span></span> <span data-ttu-id="b023d-113">Si es un usuario final que está intentando depurar un error de impresión o un problema de la red doméstica, consulte los foros de la [comunidad de Microsoft](https://answers.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="b023d-113">If you are an end-user trying to debug a printing error or home network issue, see the [Microsoft community forums](https://answers.microsoft.com).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="b023d-114">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="b023d-114">Where applicable</span></span>

<span data-ttu-id="b023d-115">Los administradores de red pueden usar ADSI para automatizar tareas comunes, como agregar usuarios y grupos, administrar impresoras y establecer permisos en los recursos de red.</span><span class="sxs-lookup"><span data-stu-id="b023d-115">Network Administrators can use ADSI to automate common tasks, such as adding users and groups, managing printers, and setting permissions on network resources.</span></span>

<span data-ttu-id="b023d-116">Los fabricantes de software independientes y los desarrolladores de usuarios finales pueden usar ADSI para "habilitar el directorio" sus productos y aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b023d-116">Independent Software Vendors and end-user developers can use ADSI to "directory enable" their products and applications.</span></span> <span data-ttu-id="b023d-117">Los servicios pueden publicarse en un directorio, los clientes pueden usar el directorio para encontrar los servicios y ambos pueden usar el directorio para buscar y manipular otros objetos de interés.</span><span class="sxs-lookup"><span data-stu-id="b023d-117">Services can publish themselves in a directory, clients can use the directory to find the services, and both can use the directory to find and manipulate other objects of interest.</span></span> <span data-ttu-id="b023d-118">Dado que Active Directory interfaces de servicio son independientes de los servicios de directorio subyacentes, los productos y las aplicaciones habilitadas para el directorio pueden funcionar correctamente en varios entornos de red y de directorio.</span><span class="sxs-lookup"><span data-stu-id="b023d-118">Because Active Directory Service Interfaces are independent of the underlying directory service(s), directory-enabled products and applications can operate successfully in multiple network and directory environments.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="b023d-119">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="b023d-119">Developer audience</span></span>

<span data-ttu-id="b023d-120">Puede escribir aplicaciones cliente ADSI en muchos idiomas.</span><span class="sxs-lookup"><span data-stu-id="b023d-120">You can write ADSI client applications in many languages.</span></span> <span data-ttu-id="b023d-121">Para la mayoría de las tareas administrativas, ADSI define interfaces y objetos a los que se puede acceder desde lenguajes compatibles con la automatización, como Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript) y Java, a los lenguajes más conscientes del rendimiento y la eficacia, como C y C++.</span><span class="sxs-lookup"><span data-stu-id="b023d-121">For most administrative tasks, ADSI defines interfaces and objects accessible from Automation-compliant languages like Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript), and Java to the more performance and efficiency-conscious languages such as C and C++.</span></span> <span data-ttu-id="b023d-122">Una buena base en la programación COM es útil para el programador de ADSI.</span><span class="sxs-lookup"><span data-stu-id="b023d-122">A good foundation in COM programming is useful to the ADSI programmer.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b023d-123">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="b023d-123">Run-time requirements</span></span>

<span data-ttu-id="b023d-124">Active Directory se ejecuta en controladores de dominio de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="b023d-124">Active Directory runs on Windows Server domain controllers.</span></span> <span data-ttu-id="b023d-125">Sin embargo, las aplicaciones cliente que usan ADSI pueden escribirse y ejecutarse en Windows.</span><span class="sxs-lookup"><span data-stu-id="b023d-125">However, client applications using ADSI may be written and run on Windows.</span></span> <span data-ttu-id="b023d-126">Además, los desarrolladores querrán el kit de desarrollo de software (SDK) de la plataforma, que también está disponible en el sitio web de MSDN.</span><span class="sxs-lookup"><span data-stu-id="b023d-126">In addition, developers will want the Platform Software Development Kit (SDK), also available on the MSDN website.</span></span> <span data-ttu-id="b023d-127">Para investigar el contenido de Active Directory, utilice el complemento MMC usuarios y equipos Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b023d-127">To investigate the contents of Active Directory, use the Active Directory Users and Computers MMC snap-in.</span></span> <span data-ttu-id="b023d-128">Este complemento reemplaza a la herramienta Adsvw que estaba disponible para versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="b023d-128">This snap-in replaces the Adsvw tool that was available for previous versions of Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b023d-129">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b023d-129">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="b023d-130">Acerca de ADSI</span><span class="sxs-lookup"><span data-stu-id="b023d-130">About ADSI</span></span>](about-adsi.md)
</dt> <dd>

<span data-ttu-id="b023d-131">Información general acerca de ADSI.</span><span class="sxs-lookup"><span data-stu-id="b023d-131">General information about ADSI.</span></span>

</dd> <dt>

[<span data-ttu-id="b023d-132">Usar ADSI</span><span class="sxs-lookup"><span data-stu-id="b023d-132">Using ADSI</span></span>](using-adsi.md)
</dt> <dd>

<span data-ttu-id="b023d-133">Guía del programador sobre el uso de ADSI.</span><span class="sxs-lookup"><span data-stu-id="b023d-133">Programmer's Guide to using ADSI.</span></span>

</dd> <dt>

[<span data-ttu-id="b023d-134">Tutoriales de inicio rápido de ADSI</span><span class="sxs-lookup"><span data-stu-id="b023d-134">ADSI Quick-start Tutorials</span></span>](adsi-quick-start-tutorials.md)
</dt> <dd>

<span data-ttu-id="b023d-135">Usar ADSI con automatización para administrar directorios.</span><span class="sxs-lookup"><span data-stu-id="b023d-135">Using ADSI with Automation to manage directories.</span></span>

</dd> <dt>

[<span data-ttu-id="b023d-136">Referencia ADSI</span><span class="sxs-lookup"><span data-stu-id="b023d-136">ADSI Reference</span></span>](adsi-reference.md)
</dt> <dd>

<span data-ttu-id="b023d-137">Documentación de los métodos y las interfaces ADSI.</span><span class="sxs-lookup"><span data-stu-id="b023d-137">Documentation of ADSI interfaces and methods.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="b023d-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b023d-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b023d-139">[The Component Object Model](../com/the-component-object-model.md) [Modelo de objetos componentes (COM)]</span><span class="sxs-lookup"><span data-stu-id="b023d-139">[The Component Object Model](../com/the-component-object-model.md)</span></span>
</dt> <dt>

[<span data-ttu-id="b023d-140">Clientes y servidores COM</span><span class="sxs-lookup"><span data-stu-id="b023d-140">COM Clients and Servers</span></span>](../com/com-clients-and-servers.md)
</dt> <dt>

[<span data-ttu-id="b023d-141">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="b023d-141">Active Directory Domain Services</span></span>](../ad/active-directory-domain-services.md)
</dt> </dl>

 

 