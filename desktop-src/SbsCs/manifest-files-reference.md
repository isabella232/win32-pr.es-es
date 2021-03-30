---
description: Los ensamblados en paralelo se usan con los siguientes tipos de archivos de manifiesto y de configuración. Los manifiestos y las configuraciones son archivos XML.
ms.assetid: 8b969a8f-586c-4556-87be-92db6c61e8ce
title: Referencia de archivos de manifiesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ea9915ba8e5e0c43b7e9c96e62ea46c3f0061b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154097"
---
# <a name="manifest-files-reference"></a><span data-ttu-id="a64d8-104">Referencia de archivos de manifiesto</span><span class="sxs-lookup"><span data-stu-id="a64d8-104">Manifest Files Reference</span></span>

<span data-ttu-id="a64d8-105">Los ensamblados en paralelo se usan con los siguientes tipos de archivos de manifiesto y de configuración.</span><span class="sxs-lookup"><span data-stu-id="a64d8-105">Side-by-side assemblies are used with the following types of manifest and configuration files.</span></span> <span data-ttu-id="a64d8-106">Los manifiestos y las configuraciones son archivos XML.</span><span class="sxs-lookup"><span data-stu-id="a64d8-106">Manifests and configurations are XML files.</span></span>



| <span data-ttu-id="a64d8-107">de manifiesto</span><span class="sxs-lookup"><span data-stu-id="a64d8-107">Manifest</span></span>                                                               | <span data-ttu-id="a64d8-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a64d8-108">Description</span></span>                                                                                                                                                                                                   |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a64d8-109">Manifiestos de ensamblado</span><span class="sxs-lookup"><span data-stu-id="a64d8-109">Assembly manifests</span></span>](assembly-manifests.md)                           | <span data-ttu-id="a64d8-110">Describe los nombres, las versiones, los recursos y las dependencias de ensamblado de los ensamblados en paralelo.</span><span class="sxs-lookup"><span data-stu-id="a64d8-110">Describes the names, versions, resources, and assembly dependencies of side-by-side assemblies.</span></span>                                                                                                               |
| [<span data-ttu-id="a64d8-111">Manifiestos de aplicación</span><span class="sxs-lookup"><span data-stu-id="a64d8-111">Application manifests</span></span>](application-manifests.md)                     | <span data-ttu-id="a64d8-112">Describe los nombres y las versiones de los ensamblados en paralelo compartidos a los que se debe enlazar la aplicación en tiempo de ejecución y también pueden contener metadatos para ensamblados en paralelo privados usados por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a64d8-112">Describes the names and versions of shared side-by-side assemblies that the application should bind to at run time and may also contain metadata for private side-by-side assemblies used by the application.</span></span> |
| [<span data-ttu-id="a64d8-113">Archivos de configuración de la aplicación</span><span class="sxs-lookup"><span data-stu-id="a64d8-113">Application Configuration Files</span></span>](application-configuration-files.md) | <span data-ttu-id="a64d8-114">Redirige las versiones de ensamblado de las dependencias de ensamblado mediante [la configuración por aplicación](per-application-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="a64d8-114">Redirects the assembly versions of assembly dependencies using [per-application configuration](per-application-configuration.md).</span></span>                                                                            |
| [<span data-ttu-id="a64d8-115">Archivos de configuración del publicador</span><span class="sxs-lookup"><span data-stu-id="a64d8-115">Publisher Configuration Files</span></span>](publisher-configuration-files.md)     | <span data-ttu-id="a64d8-116">Redirige las versiones de ensamblado de dependencias de ensamblado por ensamblado mediante una [configuración de publicador](publisher-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="a64d8-116">Redirects the assembly versions of assembly dependencies on a per-assembly basis using a [publisher configuration](publisher-configuration.md).</span></span>                                                              |



 

<span data-ttu-id="a64d8-117">Para obtener una lista del esquema del archivo de manifiesto, consulte [esquema del archivo de manifiesto](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="a64d8-117">For a listing of the manifest file schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="a64d8-118">Para obtener una lista del esquema del archivo de configuración de la aplicación, consulte [esquema del archivo de configuración](application-configuration-file-schema.md)de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a64d8-118">For a listing of the application configuration file schema, see [Application Configuration File Schema](application-configuration-file-schema.md).</span></span>

<span data-ttu-id="a64d8-119">Para obtener una lista del esquema del archivo de configuración del publicador, consulte [esquema del archivo de configuración del publicador](publisher-configuration-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="a64d8-119">For a listing of the publisher configuration file schema, see [Publisher Configuration File Schema](publisher-configuration-file-schema.md).</span></span>

<span data-ttu-id="a64d8-120">Otras tecnologías amplían el formato utilizado por los manifiestos de configuración y control de versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="a64d8-120">Other technologies extend the format used by Windows versioning and configuration manifests.</span></span> <span data-ttu-id="a64d8-121">Los desarrolladores deben consultar la documentación específica de la tecnología que se usa para obtener información sobre el formato del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="a64d8-121">Developers should refer to the documentation that is specific to the technology being used for information about the manifest format.</span></span> <span data-ttu-id="a64d8-122">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a64d8-122">For example:</span></span>

-   [<span data-ttu-id="a64d8-123">ClickOnce</span><span class="sxs-lookup"><span data-stu-id="a64d8-123">ClickOnce</span></span>](/visualstudio/deployment/clickonce-reference?view=vs-2015)
-   [<span data-ttu-id="a64d8-124">Common Language Runtime</span><span class="sxs-lookup"><span data-stu-id="a64d8-124">Common Language Runtime</span></span>](/dotnet/standard/clr)
-   <span data-ttu-id="a64d8-125">[Control de cuentas de usuario [UAC]](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="a64d8-125">[User Account Control (UAC)](/previous-versions/bb756929(v=msdn.10))</span></span>

 

 
