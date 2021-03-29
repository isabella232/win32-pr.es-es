---
description: Windows Installer desarrolladores pueden crear herramientas que permitan a los usuarios finales usar módulos de combinación configurables.
ms.assetid: 5857b788-f1dd-41d0-b0ee-0872494e3c2c
title: Agregar capacidad de configuración de módulos a una herramienta de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba04d297ad93cffc553670c648577f650cd21407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813363"
---
# <a name="adding-module-configuration-capability-to-a-merge-tool"></a><span data-ttu-id="c4e31-103">Agregar capacidad de configuración de módulos a una herramienta de combinación</span><span class="sxs-lookup"><span data-stu-id="c4e31-103">Adding Module Configuration Capability to a Merge Tool</span></span>

<span data-ttu-id="c4e31-104">Para permitir que los usuarios finales usen módulos de combinación configurables, puede crear herramientas de combinación y configuración para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c4e31-104">To enable end users to use configurable merge modules, you can author merge and configuration tools to do the following:</span></span>

-   <span data-ttu-id="c4e31-105">Las herramientas de combinación deben llamar a las funciones de Mergemod.dll versión 2,0 para combinar el módulo.</span><span class="sxs-lookup"><span data-stu-id="c4e31-105">Merge tools should call the functions in Mergemod.dll version 2.0 to merge the module.</span></span> <span data-ttu-id="c4e31-106">Las versiones anteriores de Mergemod.dll no se pueden usar para configurar módulos de combinación.</span><span class="sxs-lookup"><span data-stu-id="c4e31-106">Earlier versions of Mergemod.dll cannot be used to configure merge modules.</span></span>
-   <span data-ttu-id="c4e31-107">Las aplicaciones de configuración de cliente deben interactuar con el usuario del módulo de fusión mediante combinación para recopilar las selecciones de usuario de los elementos configurables.</span><span class="sxs-lookup"><span data-stu-id="c4e31-107">Client configuration applications should interact with the merge module user to collect the user selections for configurable items.</span></span>
-   <span data-ttu-id="c4e31-108">Las herramientas de combinación deben exponer la información de configuración creada en el módulo de combinación en la aplicación cliente para que el cliente pueda utilizar esta información para consultar al usuario.</span><span class="sxs-lookup"><span data-stu-id="c4e31-108">Merge tools should expose configuration information authored into the merge module to the client application so that the client can use this information to query the user.</span></span>
-   <span data-ttu-id="c4e31-109">Cuando una herramienta de combinación encuentra un elemento configurable durante una combinación, debe llamar a la herramienta de configuración de cliente para obtener información de personalización obtenida del usuario.</span><span class="sxs-lookup"><span data-stu-id="c4e31-109">When a merge tool encounters a configurable item during a merge, it should call the client configuration tool for customization information obtained from the user.</span></span> <span data-ttu-id="c4e31-110">La herramienta de combinación debe realizar los cambios especificados en el módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="c4e31-110">The merge tool should make the specified changes to the merge module.</span></span>
-   <span data-ttu-id="c4e31-111">Las aplicaciones de configuración deben permitir al usuario proporcionar opciones para los elementos configurables, pero no es necesario que se revelen todas las opciones posibles al usuario.</span><span class="sxs-lookup"><span data-stu-id="c4e31-111">Configuration applications should enable the user to provide choices for configurable items, but all the possible choices do not need to be revealed to the user.</span></span> <span data-ttu-id="c4e31-112">La herramienta de combinación puede usar los valores predeterminados para los elementos configurables que el usuario no selecciona.</span><span class="sxs-lookup"><span data-stu-id="c4e31-112">The merge tool can use default values for configurable items that the user does not select.</span></span>
-   <span data-ttu-id="c4e31-113">Si un usuario no proporciona información de personalización, las herramientas de combinación deben usar los valores de configuración predeterminados que se especifican en el módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="c4e31-113">If a user does not provide customization information, merge tools should use the default configuration values that are specified in the merge module.</span></span>
-   <span data-ttu-id="c4e31-114">Después de que un usuario proporciona las selecciones específicas de la herramienta de configuración, la herramienta de combinación llama Mergemod.dll para realizar la combinación.</span><span class="sxs-lookup"><span data-stu-id="c4e31-114">After a user gives the configuration tool specific selections, the merge tool calls Mergemod.dll to perform the merge.</span></span>

 

 



