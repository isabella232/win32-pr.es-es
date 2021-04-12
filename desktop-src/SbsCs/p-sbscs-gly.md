---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9BC3D6A3-D8F5-42C6-9A68-68F1741207D7
title: P (aplicaciones aisladas y ensamblados en paralelo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c70c0775af4a6245e74de474413c3741625456
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423627"
---
# <a name="p-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="2a91e-103">P (aplicaciones aisladas y ensamblados en paralelo)</span><span class="sxs-lookup"><span data-stu-id="2a91e-103">P (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="2a91e-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N o p Q [R](r-sbscs-gly.md) [s](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="2a91e-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O P Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="2a91e-105"><span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**configuración por aplicación**</span><span class="sxs-lookup"><span data-stu-id="2a91e-105"><span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**per-application configuration**</span></span>
</dt> <dd>

<span data-ttu-id="2a91e-106">Configuración que puede invalidar la configuración de la aplicación global de un ensamblado específico.</span><span class="sxs-lookup"><span data-stu-id="2a91e-106">Configuration that can override a specific assembly's global application configuration.</span></span> <span data-ttu-id="2a91e-107">Una configuración por aplicación se especifica mediante un archivo de manifiesto de configuración de aplicación instalado en la misma carpeta que el archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="2a91e-107">A per-application configuration is specified by an application configuration manifest file installed in the same folder as the executable file.</span></span> <span data-ttu-id="2a91e-108">El archivo de manifiesto describe la versión o el intervalo de versiones de los ensamblados en paralelo que va a usar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2a91e-108">The manifest file describes the version, or range of versions, of side-by-side assemblies to be used by the application.</span></span> <span data-ttu-id="2a91e-109">Se puede utilizar la configuración por aplicación cuando una nueva versión de un ensamblado es incompatible con una aplicación.</span><span class="sxs-lookup"><span data-stu-id="2a91e-109">Per-application configuration might be used when a new version of an assembly is incompatible with an application.</span></span> <span data-ttu-id="2a91e-110">En este caso, la configuración predeterminada o global de la aplicación se puede invalidar para un ensamblado en paralelo específico.</span><span class="sxs-lookup"><span data-stu-id="2a91e-110">In this case, the application's default or global configuration can be overridden for a specific side-by-side assembly.</span></span>

</dd> <dt>

<span data-ttu-id="2a91e-111"><span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**ensamblado en paralelo privado**</span><span class="sxs-lookup"><span data-stu-id="2a91e-111"><span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**private side-by-side assembly**</span></span>
</dt> <dd>

<span data-ttu-id="2a91e-112">Un ensamblado en paralelo privado solo es visible para una aplicación especificada.</span><span class="sxs-lookup"><span data-stu-id="2a91e-112">A private side-by-side assembly is only visible to a specified application.</span></span> <span data-ttu-id="2a91e-113">Se instala localmente en una aplicación aislada y el código del ensamblado se convierte en privado en el contexto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2a91e-113">It is installed locally to an isolated application and the assembly's code becomes private to the application context.</span></span> <span data-ttu-id="2a91e-114">Las dependencias de un ensamblado en paralelo privado se describen en el archivo de manifiesto de aplicación.</span><span class="sxs-lookup"><span data-stu-id="2a91e-114">The dependencies of a private side-by-side assembly are described in the application manifest file.</span></span> <span data-ttu-id="2a91e-115">Los ensamblados en paralelo privados se pueden usar para desplazar los efectos negativos del uso compartido de ensamblados, como conflictos de DLL, y para facilitar la implementación de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="2a91e-115">Private side-by-side assemblies can be used to offset the negative effects of assembly sharing, such as DLL conflicts, and to facilitate application deployment.</span></span>

</dd> <dt>

<span data-ttu-id="2a91e-116"><span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**token de clave pública**</span><span class="sxs-lookup"><span data-stu-id="2a91e-116"><span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**public key token**</span></span>
</dt> <dd>

<span data-ttu-id="2a91e-117">Cadena hexadecimal de 16 caracteres que representa los últimos 8 bytes del hash SHA-1 de la clave pública con la que se firma el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="2a91e-117">A 16-character hexadecimal string that represents the last 8 bytes of the SHA-1 hash of the public key under which the assembly is signed.</span></span> <span data-ttu-id="2a91e-118">La clave pública que se usa para firmar el catálogo debe ser de 2048 bits o superior.</span><span class="sxs-lookup"><span data-stu-id="2a91e-118">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="2a91e-119">Se requiere para todos los ensamblados en paralelo compartidos.</span><span class="sxs-lookup"><span data-stu-id="2a91e-119">Required for all shared side-by-side assemblies.</span></span>

</dd> </dl>

 

 



