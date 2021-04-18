---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 904FE2AB-9E94-47E4-88BA-DB215775797B
title: G (aplicaciones aisladas y ensamblados en paralelo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a4488c03da1c4c1f568db039a8b0e0a05d60ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652394"
---
# <a name="g-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="d6dd0-103">G (aplicaciones aisladas y ensamblados en paralelo)</span><span class="sxs-lookup"><span data-stu-id="d6dd0-103">G (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="d6dd0-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F G H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N o [p](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [s](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="d6dd0-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F G H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="d6dd0-105"><span id="_win32_global_application_configuration_gly"></span><span id="_WIN32_GLOBAL_APPLICATION_CONFIGURATION_GLY"></span>**configuración de la aplicación global**</span><span class="sxs-lookup"><span data-stu-id="d6dd0-105"><span id="_win32_global_application_configuration_gly"></span><span id="_WIN32_GLOBAL_APPLICATION_CONFIGURATION_GLY"></span>**global application configuration**</span></span>
</dt> <dd>

<span data-ttu-id="d6dd0-106">Especificación de que todas las aplicaciones del sistema usan la misma versión de ensamblado en paralelo.</span><span class="sxs-lookup"><span data-stu-id="d6dd0-106">Specification that all applications on the system use the same side-by-side assembly version.</span></span> <span data-ttu-id="d6dd0-107">La configuración global se especifica en cada ensamblado en un archivo de manifiesto del ensamblado global instalado en la carpeta WinSxS.</span><span class="sxs-lookup"><span data-stu-id="d6dd0-107">Global configuration is specified on a per-assembly basis in a global assembly manifest file installed in the Winsxs folder.</span></span> <span data-ttu-id="d6dd0-108">La configuración global puede usarse cuando un desarrollador o administrador de ensamblados necesita configurar todas las aplicaciones en el sistema para utilizar una versión de ensamblado más reciente.</span><span class="sxs-lookup"><span data-stu-id="d6dd0-108">Global configuration might be used when an assembly developer or administrator needs to configure all applications on the system to use a newer assembly version.</span></span> <span data-ttu-id="d6dd0-109">En este caso, el nuevo ensamblado debe ser compatible con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="d6dd0-109">In this case, the new assembly needs to be backward compatible.</span></span> <span data-ttu-id="d6dd0-110">Una configuración por aplicación invalida la configuración de la aplicación predeterminada o global para aplicaciones específicas.</span><span class="sxs-lookup"><span data-stu-id="d6dd0-110">A per-application configuration overrides the default or global application configuration for specific applications.</span></span>

</dd> <dt>

<span data-ttu-id="d6dd0-111"><span id="_win32_global_assembly_manifest_gly"></span><span id="_WIN32_GLOBAL_ASSEMBLY_MANIFEST_GLY"></span>**manifiesto de ensamblado global**</span><span class="sxs-lookup"><span data-stu-id="d6dd0-111"><span id="_win32_global_assembly_manifest_gly"></span><span id="_WIN32_GLOBAL_ASSEMBLY_MANIFEST_GLY"></span>**global assembly manifest**</span></span>
</dt> <dd>

<span data-ttu-id="d6dd0-112">Archivo que define la configuración global de la aplicación de un ensamblado en paralelo.</span><span class="sxs-lookup"><span data-stu-id="d6dd0-112">File that defines the global application configuration of a side-by-side assembly.</span></span> <span data-ttu-id="d6dd0-113">Los archivos de manifiesto de ensamblado global se instalan en el almacén de ensamblados del sistema en la carpeta WinSxS.</span><span class="sxs-lookup"><span data-stu-id="d6dd0-113">Global assembly manifest files are installed into the system assembly store in the Winsxs folder.</span></span>

</dd> </dl>

 

 



