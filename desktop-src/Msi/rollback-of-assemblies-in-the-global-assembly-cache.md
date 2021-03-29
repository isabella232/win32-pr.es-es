---
description: Un proceso de dos pasos extiende el modelo de transacción del Windows Installer a los productos que contienen Common Language Runtime ensamblados. Esto permite que el instalador revierta las instalaciones y eliminaciones de ensamblados que no se hayan realizado correctamente.
ms.assetid: 065a380c-4eb5-48a5-ab0a-7f1229b77898
title: Reversión de ensamblados en la caché global de ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84bc3107355cb50c17043ee571edff708ba3f6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809488"
---
# <a name="rollback-of-assemblies-in-the-global-assembly-cache"></a><span data-ttu-id="df527-104">Reversión de ensamblados en la caché global de ensamblados</span><span class="sxs-lookup"><span data-stu-id="df527-104">Rollback of Assemblies in the Global Assembly Cache</span></span>

<span data-ttu-id="df527-105">Un proceso de dos pasos extiende el modelo de transacción del Windows Installer a los productos que contienen Common Language Runtime ensamblados.</span><span class="sxs-lookup"><span data-stu-id="df527-105">A two-step process extends the Windows Installer's transaction model to products containing common language runtime assemblies.</span></span> <span data-ttu-id="df527-106">Esto permite que el instalador revierta las instalaciones y eliminaciones de ensamblados que no se hayan realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="df527-106">This enables the installer to rollback unsuccessful installations and removals of assemblies.</span></span>

<span data-ttu-id="df527-107">En el primer paso, el Windows Installer usa el marco de Microsoft .NET para crear una interfaz para cada ensamblado.</span><span class="sxs-lookup"><span data-stu-id="df527-107">During the first step, the Windows Installer uses the Microsoft .NET Framework to create one interface for each assembly.</span></span> <span data-ttu-id="df527-108">En el Windows Installer se usan tantas interfaces como se están instalando los ensamblados.</span><span class="sxs-lookup"><span data-stu-id="df527-108">The Windows Installer uses as many interfaces as there are assemblies being installed.</span></span> <span data-ttu-id="df527-109">La confirmación de un ensamblado mediante una de estas interfaces solo significa que el ensamblado está listo para reemplazar cualquier ensamblado existente con el mismo nombre, pero aún no lo reemplaza.</span><span class="sxs-lookup"><span data-stu-id="df527-109">Committing an assembly using one of these interfaces only means that the assembly is ready to replace any existing assembly with the same name, it does not yet replace it.</span></span> <span data-ttu-id="df527-110">Si el usuario cancela la instalación o si se produce un error de instalación grave, el Windows Installer puede revertir el ensamblado a su estado anterior mediante la liberación de estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="df527-110">If the user cancels the installation, or if there is a fatal installation error, the Windows Installer can still rollback the assembly to its previous state by releasing these interfaces.</span></span>

<span data-ttu-id="df527-111">Una vez que la Windows Installer completa la instalación de todos los ensamblados y Windows Installer componentes, el instalador puede iniciar el segundo paso de la instalación.</span><span class="sxs-lookup"><span data-stu-id="df527-111">After the Windows Installer completes installing all assemblies and Windows Installer components, the installer may initiate the second step of the installation.</span></span> <span data-ttu-id="df527-112">En el segundo paso se usa una función independiente para realizar la confirmación final de todos los nuevos ensamblados de Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="df527-112">The second step uses a separate function to do the final commit of all the new common language runtime assemblies.</span></span> <span data-ttu-id="df527-113">Esto reemplazará todos los ensamblados existentes que tengan el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="df527-113">This replaces any existing assemblies with the same name.</span></span>

 

 



