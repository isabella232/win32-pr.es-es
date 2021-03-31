---
description: Un ensamblado Win32 se puede instalar como un ensamblado privado y estar exclusivamente disponible para su uso por parte de una aplicación. Los ensamblados privados deben instalarse mediante un paquete de Windows Installer utilizado para instalar o actualizar una aplicación.
ms.assetid: 4c6dac5f-fdd3-4125-b54a-74941ee6b3b4
title: Ensamblados privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1073426e080cc4b8b30358ce26feb99515abb185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277162"
---
# <a name="private-assemblies"></a><span data-ttu-id="586fe-104">Ensamblados privados</span><span class="sxs-lookup"><span data-stu-id="586fe-104">Private Assemblies</span></span>

<span data-ttu-id="586fe-105">Un ensamblado Win32 se puede instalar como un ensamblado privado y estar exclusivamente disponible para su uso por parte de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="586fe-105">A Win32 assembly can be installed as a private assembly and be exclusively available for use by one application.</span></span> <span data-ttu-id="586fe-106">Los ensamblados privados deben instalarse mediante un paquete de Windows Installer utilizado para instalar o actualizar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="586fe-106">Private assemblies should be installed by a Windows Installer package used to install or update an application.</span></span>

<span data-ttu-id="586fe-107">En Windows XP, los ensamblados privados se instalan como [ensamblados en paralelo](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="586fe-107">On Windows XP, private assemblies are installed as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="586fe-108">El Windows Installer instala ensamblados en paralelo privados en una carpeta privada para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="586fe-108">The Windows Installer installs private side-by-side assemblies in a folder private to the application.</span></span> <span data-ttu-id="586fe-109">Normalmente, la carpeta que contiene el archivo ejecutable de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="586fe-109">Commonly the folder that contains the applications executable file.</span></span> <span data-ttu-id="586fe-110">La dependencia de la aplicación en el ensamblado privado se especifica en un archivo de manifiesto de aplicación.</span><span class="sxs-lookup"><span data-stu-id="586fe-110">The dependency of the application on the private assembly is specified in an application manifest file.</span></span> <span data-ttu-id="586fe-111">Para obtener más información, vea [aplicaciones aisladas y ensamblados en paralelo](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span><span class="sxs-lookup"><span data-stu-id="586fe-111">For more information, see [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

<span data-ttu-id="586fe-112">En sistemas operativos anteriores a Windows XP, se instala una copia del ensamblado privado y un archivo. local en una carpeta privada para el uso exclusivo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="586fe-112">On operating systems earlier than Windows XP, a copy of the private assembly and a .local file is installed into a private folder for the exclusive use of the application.</span></span> <span data-ttu-id="586fe-113">Una versión del ensamblado también se registra globalmente en el sistema y está disponible para cualquier aplicación que se enlaza a ella.</span><span class="sxs-lookup"><span data-stu-id="586fe-113">A version of the assembly is also globally registered on the system and available for any application that binds to it.</span></span> <span data-ttu-id="586fe-114">La versión global del ensamblado puede ser la versión instalada con la aplicación o una versión anterior.</span><span class="sxs-lookup"><span data-stu-id="586fe-114">The global version of the assembly may be the version installed with the application or an earlier version.</span></span> <span data-ttu-id="586fe-115">La versión global viene determinada por las mismas reglas que usan los [componentes aislados](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="586fe-115">The global version is determined by the same rules use by [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="586fe-116">Tenga en cuenta que el Windows Installer no puede instalar un ensamblado privado en una ubicación que tenga una ruta de acceso que contenga más de 234 caracteres, incluido el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="586fe-116">Note that the Windows Installer cannot install a private assembly in a location having a path that contains more than 234 characters, including the terminating null character.</span></span>

 

 
