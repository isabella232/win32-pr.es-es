---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 5591218A-3212-46D0-A40F-C0788B459545
title: S (aplicaciones aisladas y ensamblados en paralelo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9727db4c2db522b0bbb88eccf89481a61a75d8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817078"
---
# <a name="s-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="63566-103">S (aplicaciones aisladas y ensamblados en paralelo)</span><span class="sxs-lookup"><span data-stu-id="63566-103">S (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="63566-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N o [p](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) s T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="63566-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) S T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="63566-105"><span id="_win32_shared_side_by_side_assembly_gly"></span><span id="_WIN32_SHARED_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**ensamblado en paralelo compartido**</span><span class="sxs-lookup"><span data-stu-id="63566-105"><span id="_win32_shared_side_by_side_assembly_gly"></span><span id="_WIN32_SHARED_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**shared side-by-side assembly**</span></span>
</dt> <dd>

<span data-ttu-id="63566-106">Un ensamblado en paralelo compartido está disponible para que lo usen varias aplicaciones del equipo.</span><span class="sxs-lookup"><span data-stu-id="63566-106">A shared side-by-side assembly is available for use by multiple applications on the computer.</span></span> <span data-ttu-id="63566-107">Se instala en la carpeta WinSxS del directorio de Windows.</span><span class="sxs-lookup"><span data-stu-id="63566-107">It is installed in the Winsxs folder of the Windows directory.</span></span> <span data-ttu-id="63566-108">Las aplicaciones y los administradores pueden administrar la versión de un ensamblado compartido que se va a usar especificando la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="63566-108">Applications and administrators can manage the version of a shared assembly to be used by specifying the application configuration.</span></span> <span data-ttu-id="63566-109">Los ensamblados en paralelo siempre van acompañados de archivos de manifiesto que proporcionan información acerca del ensamblado al sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="63566-109">Side-by-side assemblies are always accompanied by manifest files that provide information about the assembly to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="63566-110"><span id="_win32_side_by_side_assembly_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**ensamblado en paralelo**</span><span class="sxs-lookup"><span data-stu-id="63566-110"><span id="_win32_side_by_side_assembly_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**side-by-side assembly**</span></span>
</dt> <dd>

<span data-ttu-id="63566-111">Un ensamblado en paralelo es un ensamblado Win32 acompañado de manifiestos.</span><span class="sxs-lookup"><span data-stu-id="63566-111">A side-by-side assembly is a Win32 assembly accompanied by manifests.</span></span> <span data-ttu-id="63566-112">Un ensamblado simultáneo contiene una colección de recursos (un grupo de archivos dll, clases de Windows, servidores COM, bibliotecas de tipos o interfaces) que siempre se proporcionan a las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="63566-112">A side-by-side assembly contains a collection of resources—a group of DLLs, windows classes, COM servers, type libraries, or interfaces—that are always provided to applications together.</span></span>

</dd> <dt>

<span data-ttu-id="63566-113"><span id="_win32_side_by_side_assembly_sharing_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_SHARING_GLY"></span>**uso compartido de ensamblados en paralelo**</span><span class="sxs-lookup"><span data-stu-id="63566-113"><span id="_win32_side_by_side_assembly_sharing_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_SHARING_GLY"></span>**side-by-side assembly sharing**</span></span>
</dt> <dd>

<span data-ttu-id="63566-114">Uso de ensamblados en paralelo para compartir de forma segura ensamblados entre varias aplicaciones y desplazar los efectos negativos del uso compartido, como conflictos de DLL.</span><span class="sxs-lookup"><span data-stu-id="63566-114">Use of side-by-side assemblies to safely share assemblies among multiple applications and to offset the negative effects of sharing, such as DLL conflicts.</span></span> <span data-ttu-id="63566-115">En lugar de tener una versión única de un ensamblado que asuma la compatibilidad con versiones anteriores de todas las aplicaciones, el uso compartido de ensamblados en paralelo permite que varias versiones de un ensamblado Win32 se ejecuten simultáneamente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="63566-115">Instead of having a single version of an assembly that assumes backward compatibility with all applications, side-by-side assembly sharing enables multiple versions of a Win32 assembly to run simultaneously on the system.</span></span> <span data-ttu-id="63566-116">Los ensamblados en paralelo siempre van acompañados de archivos de manifiesto del ensamblado que proporcionan información acerca del ensamblado al sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="63566-116">Side-by-side assemblies are always accompanied by assembly manifest files that provide information about the assembly to the operating system.</span></span> <span data-ttu-id="63566-117">Las aplicaciones y los administradores pueden administrar el uso compartido de ensamblados en paralelo después de la implementación mediante la actualización de la configuración de la aplicación de manera global o por aplicación.</span><span class="sxs-lookup"><span data-stu-id="63566-117">Applications and administrators can manage side-by-side assembly sharing after deployment by updating the application configuration on either a global or per-application basis.</span></span>

</dd> </dl>

 

 



