---
description: Windows Installer puede instalar, quitar y actualizar ensamblados y ensamblados Win32 utilizados por el Common Language Runtime de Microsoft .NET Framework.
ms.assetid: 88bee87c-fed2-45e9-8d8c-a5bbcc77f266
title: Ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb0f2b91a46287262848aaa2174d6bec6688d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667041"
---
# <a name="assemblies"></a><span data-ttu-id="0340a-103">Ensamblados</span><span class="sxs-lookup"><span data-stu-id="0340a-103">Assemblies</span></span>

<span data-ttu-id="0340a-104">Windows Installer puede instalar, quitar y actualizar ensamblados y ensamblados Win32 utilizados por el Common Language Runtime de Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="0340a-104">Windows Installer can install, remove, and update Win32 assemblies and assemblies used by the common language runtime of the Microsoft .NET Framework.</span></span> <span data-ttu-id="0340a-105">Un ensamblado se controla mediante el Windows Installer como un componente instalador único.</span><span class="sxs-lookup"><span data-stu-id="0340a-105">An assembly is handled by the Windows Installer as a single installer component.</span></span> <span data-ttu-id="0340a-106">Todos los archivos que forman un ensamblado deben estar contenidos en un único componente del instalador que se enumera en la tabla de [componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="0340a-106">All of the files that constitute an assembly must be contained by a single installer component that is listed in the [Component](component-table.md) table.</span></span>

<span data-ttu-id="0340a-107">Windows Installer que se ejecutan en Windows Vista y Windows XP pueden instalar ensamblados en paralelo.</span><span class="sxs-lookup"><span data-stu-id="0340a-107">Windows Installer running on Windows Vista and Windows XP can install side-by-side assemblies.</span></span> <span data-ttu-id="0340a-108">Los ensamblados en paralelo pueden compartir de forma segura ensamblados entre varias aplicaciones y pueden desplazar los efectos negativos del uso compartido de ensamblados, como conflictos de DLL.</span><span class="sxs-lookup"><span data-stu-id="0340a-108">Side-by-side assemblies can safely share assemblies among multiple applications and can offset the negative effects of assembly sharing, such as DLL conflicts.</span></span> <span data-ttu-id="0340a-109">En lugar de una versión única de un ensamblado que asume la compatibilidad con versiones anteriores de todas las aplicaciones, el uso compartido de ensamblados en paralelo permite que varias versiones de un ensamblado COM o Win32 se ejecuten simultáneamente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="0340a-109">Instead of a single version of an assembly that assumes backward compatibility with all applications, side-by-side assembly sharing enables multiple versions of a COM or Win32 assembly to run simultaneously on the system.</span></span> <span data-ttu-id="0340a-110">Esta funcionalidad mejorada para aislar las aplicaciones es una parte importante del marco de Microsoft .NET.</span><span class="sxs-lookup"><span data-stu-id="0340a-110">This improved capability to isolate applications is an important part of the Microsoft .NET Framework.</span></span> <span data-ttu-id="0340a-111">Para obtener más información, vea [aplicaciones aisladas y ensamblados en paralelo](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).</span><span class="sxs-lookup"><span data-stu-id="0340a-111">For more information, see [Isolated Applications and Side-by-side Assemblies](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).</span></span>

<span data-ttu-id="0340a-112">En las secciones siguientes se describe el uso de ensamblados con el Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="0340a-112">The following sections describe the use of assemblies with the Windows Installer.</span></span>

-   [<span data-ttu-id="0340a-113">Agregar ensamblados a un paquete</span><span class="sxs-lookup"><span data-stu-id="0340a-113">Adding Assemblies to a Package</span></span>](adding-assemblies-to-a-package.md)
-   [<span data-ttu-id="0340a-114">Instalar y quitar ensamblados</span><span class="sxs-lookup"><span data-stu-id="0340a-114">Installing and Removing Assemblies</span></span>](installing-and-removing-assemblies.md)
-   [<span data-ttu-id="0340a-115">Actualizar ensamblados</span><span class="sxs-lookup"><span data-stu-id="0340a-115">Updating Assemblies</span></span>](updating-assemblies.md)
-   [<span data-ttu-id="0340a-116">Modos de reinstalación de los ensamblados de Common Language Runtime</span><span class="sxs-lookup"><span data-stu-id="0340a-116">Reinstallation Modes of Common Language Runtime Assemblies</span></span>](reinstallation-modes-of-common-language-runtime-assemblies.md)
-   [<span data-ttu-id="0340a-117">Claves del registro de ensamblado escritas por Windows Installer</span><span class="sxs-lookup"><span data-stu-id="0340a-117">Assembly Registry Keys Written by Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)

<span data-ttu-id="0340a-118">Para obtener información sobre la instalación de aplicaciones COM y COM+ 1,0, vea [instalar una aplicación com+ con el Windows Installer](installing-a-com--application-with-the-windows-installer.md), [instalar un componente com en una ubicación privada](installing-a-com-component-to-a-private-location.md)y [convertir un componente com en un paquete existente privado](make-a-com-component-in-an-existing-package-private.md).</span><span class="sxs-lookup"><span data-stu-id="0340a-118">For information about installing COM and COM+ 1.0 applications, see [Installing a COM+ Application with the Windows Installer](installing-a-com--application-with-the-windows-installer.md), [Installing a COM Component to a Private Location](installing-a-com-component-to-a-private-location.md), and [Make a COM Component in an Existing Package Private](make-a-com-component-in-an-existing-package-private.md).</span></span>

 

 
