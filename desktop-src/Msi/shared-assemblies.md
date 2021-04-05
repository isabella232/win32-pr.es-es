---
description: Un ensamblado Win32 se puede instalar como un ensamblado compartido y estar disponible para que lo usen varias aplicaciones del equipo. Los ensamblados compartidos deben instalarse mediante un paquete de Windows Installer utilizado para instalar o actualizar una aplicación.
ms.assetid: d408b0a9-8dc5-4cd0-93b3-429de7d12b17
title: Ensamblados compartidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e99d805614c05838abe9f5c869fc9c072b1fa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815438"
---
# <a name="shared-assemblies"></a><span data-ttu-id="28558-104">Ensamblados compartidos</span><span class="sxs-lookup"><span data-stu-id="28558-104">Shared Assemblies</span></span>

<span data-ttu-id="28558-105">Un ensamblado Win32 se puede instalar como un ensamblado compartido y estar disponible para que lo usen varias aplicaciones del equipo.</span><span class="sxs-lookup"><span data-stu-id="28558-105">A Win32 assembly can be installed as a shared assembly and be available for use by multiple applications on the computer.</span></span> <span data-ttu-id="28558-106">Los ensamblados compartidos deben instalarse mediante un paquete de Windows Installer utilizado para instalar o actualizar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="28558-106">Shared assemblies should be installed by a Windows Installer package used to install or update an application.</span></span>

<span data-ttu-id="28558-107">Los ensamblados compartidos se instalan como [ensamblados en paralelo](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="28558-107">Shared assemblies are installed as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="28558-108">El Windows Installer instala ensamblados en paralelo compartidos en la carpeta WinSxS.</span><span class="sxs-lookup"><span data-stu-id="28558-108">The Windows Installer installs shared side-by-side assemblies into the Winsxs folder.</span></span> <span data-ttu-id="28558-109">Los ensamblados no se registran globalmente en el sistema, pero están disponibles globalmente para cualquier aplicación que especifique una dependencia en el ensamblado en un archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="28558-109">The assemblies are not registered globally on the system, but they are globally available to any application that specifies a dependency on the assembly in a manifest file.</span></span> <span data-ttu-id="28558-110">Para obtener más información, vea [aplicaciones aisladas y ensamblados en paralelo](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span><span class="sxs-lookup"><span data-stu-id="28558-110">For more information, see [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

<span data-ttu-id="28558-111">En sistemas operativos anteriores a Windows XP, los ensamblados compartidos se instalan normalmente en la carpeta del sistema de Windows y se registran globalmente.</span><span class="sxs-lookup"><span data-stu-id="28558-111">On operating systems earlier than Windows XP, shared assemblies are usually installed in the Windows system folder and registered globally.</span></span> <span data-ttu-id="28558-112">La última versión instalada está disponible para cualquier aplicación que se enlaza a ella.</span><span class="sxs-lookup"><span data-stu-id="28558-112">The latest installed version is available to any application that binds to it.</span></span>

<span data-ttu-id="28558-113">Para obtener información sobre cómo crear un paquete de Windows Installer para instalar un ensamblado compartido, consulte lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="28558-113">For information on how to author a Windows Installer package to install a shared assembly, see the following:</span></span>

-   [<span data-ttu-id="28558-114">Instalación de ensamblados Win32 para el uso compartido en paralelo en Windows XP</span><span class="sxs-lookup"><span data-stu-id="28558-114">Installing Win32 Assemblies for Side-by-Side Sharing on Windows XP</span></span>](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [<span data-ttu-id="28558-115">Instalar ensamblados Win32 para el uso privado de una aplicación en Windows XP</span><span class="sxs-lookup"><span data-stu-id="28558-115">Installing Win32 Assemblies for the Private Use of an Application on Windows XP</span></span>](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 
