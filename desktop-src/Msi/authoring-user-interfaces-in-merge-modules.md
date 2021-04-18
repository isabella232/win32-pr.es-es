---
description: Los módulos de combinación raramente requieren una interfaz de usuario.
ms.assetid: 53bd2064-09dd-406f-a8ff-7b04f3525b9f
title: Crear interfaces de usuario en módulos de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2df8781efea35ddd854ef76c2155d4a2ded7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667025"
---
# <a name="authoring-user-interfaces-in-merge-modules"></a><span data-ttu-id="3fbe9-103">Crear interfaces de usuario en módulos de combinación</span><span class="sxs-lookup"><span data-stu-id="3fbe9-103">Authoring User Interfaces in Merge Modules</span></span>

<span data-ttu-id="3fbe9-104">Los módulos de combinación raramente requieren una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="3fbe9-104">Merge modules rarely require a user interface.</span></span> <span data-ttu-id="3fbe9-105">La liberación de un módulo de combinación que contenga componentes instalables y una interfaz de usuario restringe en última instancia la flexibilidad del usuario del módulo.</span><span class="sxs-lookup"><span data-stu-id="3fbe9-105">Releasing a merge module that contains both installable components and a user interface ultimately restricts the flexibility of the module user.</span></span> <span data-ttu-id="3fbe9-106">La combinación de los componentes y la interfaz de usuario en un módulo puede impedir que los desarrolladores usen su propia interfaz de usuario o que proporcionen instalaciones silenciosas.</span><span class="sxs-lookup"><span data-stu-id="3fbe9-106">Combining both components and UI into one module can prevent developers from using their own UI or from providing silent installations.</span></span> <span data-ttu-id="3fbe9-107">Una alternativa mejor es liberar dos módulos de combinación, uno que instala silenciosamente los componentes y un segundo módulo opcional que contiene la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="3fbe9-107">A better alternative is to release two merge modules, one that silently installs the components and a second optional module that contains the UI.</span></span> <span data-ttu-id="3fbe9-108">El módulo con la interfaz de usuario debe mostrar el módulo de componentes en la [tabla ModuleDependency](moduledependency-table.md).</span><span class="sxs-lookup"><span data-stu-id="3fbe9-108">The module with the UI should list the component module in its [ModuleDependency table](moduledependency-table.md).</span></span> <span data-ttu-id="3fbe9-109">Este método permite a los autores de módulos proporcionar una interfaz de usuario sin forzarla a los desarrolladores.</span><span class="sxs-lookup"><span data-stu-id="3fbe9-109">This method enables module authors to provide a UI without forcing it on developers.</span></span>

<span data-ttu-id="3fbe9-110">Cuando las tablas de la interfaz de usuario se utilizan en módulos de combinación, se pueden combinar de la misma manera que cualquier otra tabla.</span><span class="sxs-lookup"><span data-stu-id="3fbe9-110">When UI tables are used in merge modules they can be merged in the same way as any other tables.</span></span>

 

 



