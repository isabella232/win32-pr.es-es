---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 0D537FD1-AD5C-43CB-989F-4B5B7C0A1208
title: A (aplicaciones aisladas y ensamblados en paralelo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41a925d83cf602f5d23c7d043102927748da14a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687430"
---
# <a name="a-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="2f5ed-103">A (aplicaciones aisladas y ensamblados en paralelo)</span><span class="sxs-lookup"><span data-stu-id="2f5ed-103">A (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="2f5ed-104">A B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N o [p](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [s](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="2f5ed-104">A B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="2f5ed-105"><span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**contexto de activación**</span><span class="sxs-lookup"><span data-stu-id="2f5ed-105"><span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**activation context**</span></span>
</dt> <dd>

<span data-ttu-id="2f5ed-106">Estructura de datos en memoria.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-106">A data structure in memory.</span></span> <span data-ttu-id="2f5ed-107">Cada sección de esta estructura contiene metadatos para las funciones de la API que están en paralelo.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-107">Each section of this structure contains metadata for side-by-side-aware API functions.</span></span> <span data-ttu-id="2f5ed-108">Por ejemplo, una sección puede tener datos de redireccionamiento de DLL, que usa el cargador de DLL, y otro puede tener datos de servidor COM.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-108">For example, one section may have DLL redirection data, which is used by the DLL loader, and another may have COM server data.</span></span> <span data-ttu-id="2f5ed-109">Estos datos se pueden usar para redirigir la carga de una DLL a una versión concreta, la creación de un objeto COM o la creación de una ventana en una versión que sea más compatible para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-109">This data may be used to redirect the loading of a DLL to a specific version, the creation of a COM object, or the creation of a window to a version that is most compatible for the application.</span></span>

</dd> <dt>

<span data-ttu-id="2f5ed-110"><span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**configuración de la aplicación**</span><span class="sxs-lookup"><span data-stu-id="2f5ed-110"><span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**application configuration**</span></span>
</dt> <dd>

<span data-ttu-id="2f5ed-111">Nombres y versiones de los ensamblados en paralelo necesarios para ejecutar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-111">Names and versions of side-by-side assemblies required to run an application.</span></span> <span data-ttu-id="2f5ed-112">Cuando una aplicación se implementa con un manifiesto, se definen explícitamente las dependencias de las versiones específicas de los ensamblados en paralelo compartidos.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-112">When an application is deployed with a manifest, dependencies on specific versions of shared side-by-side assemblies are explicitly defined.</span></span> <span data-ttu-id="2f5ed-113">De forma predeterminada, la versión del ensamblado especificado en el manifiesto es la versión que se usa durante la activación.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-113">By default, the version of the assembly specified in the manifest is the version that is used upon activation.</span></span> <span data-ttu-id="2f5ed-114">La configuración global de la aplicación especifica la configuración de todas las aplicaciones del sistema.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-114">Global application configuration specifies the configuration of all applications on the system.</span></span> <span data-ttu-id="2f5ed-115">La configuración por aplicación puede invalidar la configuración global de la aplicación por aplicación.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-115">Per-application configuration can override the global application configuration on a per-application basis.</span></span>

</dd> <dt>

<span data-ttu-id="2f5ed-116"><span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**manifiesto de configuración de la aplicación**</span><span class="sxs-lookup"><span data-stu-id="2f5ed-116"><span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**application configuration manifest**</span></span>
</dt> <dd>

<span data-ttu-id="2f5ed-117">Archivo que especifica los ensamblados en paralelo que se van a usar en una aplicación totalmente o parcialmente aislada.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-117">File that specifies side-by-side assemblies to be used by a fully or partially isolated application.</span></span> <span data-ttu-id="2f5ed-118">Los archivos de manifiesto de configuración de la aplicación se instalan en la misma carpeta que el archivo ejecutable de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-118">Application configuration manifest files are installed in the same folder as the application's executable file.</span></span>

</dd> <dt>

<span data-ttu-id="2f5ed-119"><span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**manifiesto de aplicación**</span><span class="sxs-lookup"><span data-stu-id="2f5ed-119"><span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**application manifest**</span></span>
</dt> <dd>

<span data-ttu-id="2f5ed-120">Archivo que describe una aplicación aislada.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-120">File that describes an isolated application.</span></span> <span data-ttu-id="2f5ed-121">Especifica la información necesaria para ejecutar la aplicación, incluidas las dependencias de ensamblados privados, las versiones específicas de los ensamblados y metadatos compartidos para los ensamblados privados.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-121">It specifies the information required to run the application, including dependencies on private assemblies, specific versions of shared assemblies and metadata for private assemblies.</span></span> <span data-ttu-id="2f5ed-122">El nombre de un archivo de manifiesto de aplicación es el nombre del ejecutable de la aplicación seguido de la extensión. manifest.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-122">The name of an application manifest file is the name of the application executable followed by the extension .manifest.</span></span> <span data-ttu-id="2f5ed-123">Por ejemplo, para MySampleApp.exe, el archivo de manifiesto sería MySampleApp.exe. manifest.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-123">For example, for MySampleApp.exe, the manifest file would be MySampleApp.exe.manifest.</span></span>

</dd> <dt>

<span data-ttu-id="2f5ed-124"><span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**assembl**</span><span class="sxs-lookup"><span data-stu-id="2f5ed-124"><span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**assembly**</span></span>
</dt> <dd>

<span data-ttu-id="2f5ed-125">Unidad fundamental para la nomenclatura, el enlace, el control de versiones, la implementación o la configuración de un bloque de código de programación.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-125">Fundamental unit for naming, binding, versioning, deploying, or configuring a block of programming code.</span></span> <span data-ttu-id="2f5ed-126">Estos ensamblados de código se pueden colocar en archivos dll o ensamblados COM.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-126">These code assemblies may be placed in DLLs or COM assemblies.</span></span> <span data-ttu-id="2f5ed-127">Las aplicaciones con funcionalidad común pueden ejecutar bloques compartidos de código de programación a los que se hace referencia como módulos o ensamblados de código.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-127">Applications with common functionality may run shared blocks of programming code which are referred to as modules or code assemblies.</span></span> <span data-ttu-id="2f5ed-128">La infraestructura para el uso compartido seguro de ensamblados se conoce como uso compartido de ensamblados en paralelo.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-128">The infrastructure for the safe sharing of assemblies is referred to as side-by-side assembly sharing.</span></span>

</dd> <dt>

<span data-ttu-id="2f5ed-129"><span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**manifiesto del ensamblado**</span><span class="sxs-lookup"><span data-stu-id="2f5ed-129"><span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**assembly manifest**</span></span>
</dt> <dd>

<span data-ttu-id="2f5ed-130">Descripción de un ensamblado en paralelo.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-130">Description of a side-by-side assembly.</span></span> <span data-ttu-id="2f5ed-131">Especifica el nombre, la versión, los archivos, los recursos del ensamblado, los datos de enlace para los elementos del ensamblado y las dependencias de otros ensamblados en paralelo.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-131">It specifies the name, version, files, resources of the assembly, binding data for items of the assembly, and dependencies on other side-by-side assemblies.</span></span> <span data-ttu-id="2f5ed-132">Un archivo de manifiesto del ensamblado puede tener cualquier nombre de archivo válido, siempre y cuando vaya seguido del manifiesto de la extensión. manifest.</span><span class="sxs-lookup"><span data-stu-id="2f5ed-132">An assembly manifest file can have any valid file name, as long as it is followed by the extension .manifest.</span></span>

</dd> </dl>

 

 



