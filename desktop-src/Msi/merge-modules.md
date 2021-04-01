---
description: Los módulos de combinación proporcionan un método estándar por el que los desarrolladores ofrecen componentes compartidos de Windows Installer y lógica de configuración a sus aplicaciones.
ms.assetid: 673de3ff-e58c-4153-9c8d-c3baebba5eb1
title: Módulos de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3499368b309909bcb06da45476d43d8cac28e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279150"
---
# <a name="merge-modules"></a><span data-ttu-id="f00b4-103">Módulos de combinación</span><span class="sxs-lookup"><span data-stu-id="f00b4-103">Merge Modules</span></span>

<span data-ttu-id="f00b4-104">Los módulos de combinación proporcionan un método estándar por el que los desarrolladores ofrecen [*componentes*](c-gly.md) compartidos de Windows Installer y lógica de configuración a sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f00b4-104">Merge modules provide a standard method by which developers deliver shared Windows Installer [*components*](c-gly.md) and setup logic to their applications.</span></span> <span data-ttu-id="f00b4-105">Los módulos de combinación se utilizan para proporcionar código compartido, archivos, recursos, entradas del registro y lógica de instalación a las aplicaciones como un solo archivo compuesto.</span><span class="sxs-lookup"><span data-stu-id="f00b4-105">Merge modules are used to deliver shared code, files, resources, registry entries, and setup logic to applications as a single compound file.</span></span> <span data-ttu-id="f00b4-106">Los desarrolladores que crean nuevos módulos de combinación o utilizan módulos de combinación existentes deben seguir el estándar descrito en esta sección.</span><span class="sxs-lookup"><span data-stu-id="f00b4-106">Developers authoring new merge modules or using existing merge modules should follow the standard outlined in this section.</span></span>

<span data-ttu-id="f00b4-107">Un módulo de combinación tiene una estructura similar a la de un [*archivo Windows Installer. msi*](m-gly.md)simplificado.</span><span class="sxs-lookup"><span data-stu-id="f00b4-107">A merge module is similar in structure to a simplified Windows Installer [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="f00b4-108">Sin embargo, un módulo de combinación no se puede instalar por sí solo, debe combinarse en un paquete de instalación mediante una herramienta de combinación.</span><span class="sxs-lookup"><span data-stu-id="f00b4-108">However, a merge module cannot be installed alone, it must be merged into an installation package using a merge tool.</span></span> <span data-ttu-id="f00b4-109">Los desarrolladores que deseen utilizar módulos de combinación deben obtener una de las herramientas de combinación distribuida libremente, como Mergemod.dll, o adquirir una herramienta de fusión mediante combinación de un fabricante de software independiente.</span><span class="sxs-lookup"><span data-stu-id="f00b4-109">Developers wanting to use merge modules must obtain one of the freely distributed merge tools, such as Mergemod.dll, or purchase a merge tool from an independent software vendor.</span></span> <span data-ttu-id="f00b4-110">Los desarrolladores pueden crear módulos de fusión mediante combinación con muchas de las herramientas de software que se usan para crear un paquete de instalación de Windows Installer, como el editor de tablas de base de datos Orca proporcionado con el SDK de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f00b4-110">Developers can create new merge modules by using many of the same software tools used to create a Windows Installer installation package, such as the database table editor Orca provided with the Windows Installer SDK.</span></span>

<span data-ttu-id="f00b4-111">Cuando se combina un módulo de combinación en el archivo. msi de una aplicación, toda la información y los recursos necesarios para instalar los componentes proporcionados por el módulo de combinación se incorporan en el archivo. msi de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f00b4-111">When a merge module is merged into the .msi file of an application, all the information and resources required to install the components delivered by the merge module are incorporated into the application's .msi file.</span></span> <span data-ttu-id="f00b4-112">El módulo de combinación ya no es necesario para instalar estos componentes y no es necesario que el módulo de combinación sea accesible para un usuario.</span><span class="sxs-lookup"><span data-stu-id="f00b4-112">The merge module is then no longer required to install these components and the merge module does not need to be accessible to a user.</span></span> <span data-ttu-id="f00b4-113">Dado que toda la información necesaria para instalar los componentes se entrega como un solo archivo, el uso de módulos de combinación puede eliminar muchas instancias de conflictos de versiones, entradas del registro que faltan y archivos que no se instalan correctamente.</span><span class="sxs-lookup"><span data-stu-id="f00b4-113">Because all the information needed to install the components is delivered as a single file, the use of merge modules can eliminate many instances of version conflicts, missing registry entries, and improperly installed files.</span></span>

<span data-ttu-id="f00b4-114">Para obtener más información acerca de los módulos de combinación, vea:</span><span class="sxs-lookup"><span data-stu-id="f00b4-114">For more information about merge modules, see:</span></span>

-   [<span data-ttu-id="f00b4-115">Acerca de los módulos de combinación</span><span class="sxs-lookup"><span data-stu-id="f00b4-115">About Merge Modules</span></span>](about-merge-modules.md)
-   [<span data-ttu-id="f00b4-116">Usar módulos de combinación</span><span class="sxs-lookup"><span data-stu-id="f00b4-116">Using Merge Modules</span></span>](using-merge-modules.md)
-   [<span data-ttu-id="f00b4-117">Referencia del módulo de combinación</span><span class="sxs-lookup"><span data-stu-id="f00b4-117">Merge Module Reference</span></span>](merge-module-reference.md)

 

 



