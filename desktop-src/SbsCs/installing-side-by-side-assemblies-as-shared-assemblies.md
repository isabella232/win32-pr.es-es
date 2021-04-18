---
description: En el procedimiento siguiente se describe cómo instalar ensamblados en paralelo como ensamblados compartidos.
ms.assetid: 272ad1b8-9ea2-4af8-ba0d-c59f4db027e6
title: Instalar ensamblados en paralelo como ensamblados compartidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4e796fb371a299f508945371fea926c5d56a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497236"
---
# <a name="installing-side-by-side-assemblies-as-shared-assemblies"></a><span data-ttu-id="ee9c4-103">Instalar ensamblados en paralelo como ensamblados compartidos</span><span class="sxs-lookup"><span data-stu-id="ee9c4-103">Installing Side-by-side Assemblies as Shared Assemblies</span></span>

<span data-ttu-id="ee9c4-104">En el procedimiento siguiente se describe cómo instalar [ensamblados en paralelo](about-side-by-side-assemblies-.md) como [ensamblados compartidos](/windows/desktop/Msi/shared-assemblies).</span><span class="sxs-lookup"><span data-stu-id="ee9c4-104">The following procedure describes how to install [side-by-side assemblies](about-side-by-side-assemblies-.md) as [shared assemblies](/windows/desktop/Msi/shared-assemblies).</span></span>

<span data-ttu-id="ee9c4-105">**Para instalar un ensamblado en paralelo como un ensamblado compartido**</span><span class="sxs-lookup"><span data-stu-id="ee9c4-105">**To install a side-by-side assembly as a shared assembly**</span></span>

1.  <span data-ttu-id="ee9c4-106">Firmar y crear un catálogo para los archivos del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-106">Sign and create a catalog for the files in the assembly.</span></span>

    <span data-ttu-id="ee9c4-107">Los archivos deben estar firmados para instalarlos como ensamblados en paralelo.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-107">Files must be signed to install them as side-by-side assemblies.</span></span> <span data-ttu-id="ee9c4-108">Para obtener más información, vea [crear archivos y catálogos firmados](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="ee9c4-108">For more information, see [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span>

2.  <span data-ttu-id="ee9c4-109">Debe instalar ensamblados en paralelo compartidos como componentes de un paquete de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-109">You should install shared side-by-side assemblies as components of a Windows Installer package.</span></span> <span data-ttu-id="ee9c4-110">Puede ser el mismo paquete de instalación que se usa para instalar o actualizar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-110">This can be the same installation package used to install or update your application.</span></span> <span data-ttu-id="ee9c4-111">Si el ensamblado compartido se envía como parte de varias aplicaciones, debe proporcionar un módulo de combinación que se puede incorporar en estos paquetes de instalación de aplicaciones y crear un catálogo para los archivos del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-111">If the shared assembly is shipped as part of multiple applications, you should provide a merge module that can be incorporated into these applications' installation packages and create a catalog for the files in the assembly.</span></span>

    <span data-ttu-id="ee9c4-112">Se necesita Windows Installer versión 2,0 o posterior para instalar los ensamblados.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-112">Windows Installer version 2.0 or later is required to install assemblies.</span></span> <span data-ttu-id="ee9c4-113">Para obtener más información, vea el SDK de [Windows Installer](../msi/windows-installer-portal.md) y las secciones de [instalación de ensamblados Win32](../msi/installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="ee9c4-113">For more information, see the [Windows Installer](../msi/windows-installer-portal.md) SDK and the sections under [Installation of Win32 Assemblies](../msi/installation-of-win32-assemblies.md).</span></span>

 

 
