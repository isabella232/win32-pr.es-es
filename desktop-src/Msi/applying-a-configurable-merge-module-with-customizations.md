---
description: Siga las directrices generales para aplicar los módulos de combinación descritos en aplicar módulos de combinación.
ms.assetid: 6035b1a9-d452-4020-9fe3-c20ba874a2ed
title: Aplicar un módulo de combinación configurable con personalizaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f1e3da426ba5ca13e149814ab9bb927e83d4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652616"
---
# <a name="applying-a-configurable-merge-module-with-customizations"></a><span data-ttu-id="52f45-103">Aplicar un módulo de combinación configurable con personalizaciones</span><span class="sxs-lookup"><span data-stu-id="52f45-103">Applying a Configurable Merge Module with Customizations</span></span>

<span data-ttu-id="52f45-104">Siga las directrices generales para aplicar los módulos de combinación descritos en [aplicar módulos de combinación](applying-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="52f45-104">Follow the general guidelines for applying merge modules described in [Applying Merge Modules](applying-merge-modules.md).</span></span> <span data-ttu-id="52f45-105">Además, los consumidores del módulo de combinación deben hacer lo siguiente para configurar un módulo de combinación en el momento de la instalación:</span><span class="sxs-lookup"><span data-stu-id="52f45-105">In addition, merge module consumers must do the following to configure a merge module at the time of installation:</span></span>

-   <span data-ttu-id="52f45-106">Use un módulo de combinación que se crea para tener valores configurables.</span><span class="sxs-lookup"><span data-stu-id="52f45-106">Use a merge module that is authored to have configurable settings.</span></span> <span data-ttu-id="52f45-107">Para obtener más información, consulte [crear un módulo de combinación que el usuario final pueda configurar](creating-a-merge-module-that-can-be-configured-by-the-end-user.md) .</span><span class="sxs-lookup"><span data-stu-id="52f45-107">For more information, see [Creating a Merge Module that Can Be Configured by the End-User](creating-a-merge-module-that-can-be-configured-by-the-end-user.md)</span></span>
-   <span data-ttu-id="52f45-108">Use una herramienta de combinación y configuración que llame a Mergemod.dll versión 2,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="52f45-108">Use a merge and configuration tool that calls Mergemod.dll version 2.0 or later.</span></span> <span data-ttu-id="52f45-109">Las versiones anteriores de Mergmod.dll no pueden configurar los valores del módulo de fusión mediante combinación.</span><span class="sxs-lookup"><span data-stu-id="52f45-109">Earlier versions of Mergmod.dll cannot configure merge module settings.</span></span> <span data-ttu-id="52f45-110">Los autores deben crear módulos de combinación que proporcionen valores predeterminados y sean compatibles con versiones anteriores de Mergmod.dll.</span><span class="sxs-lookup"><span data-stu-id="52f45-110">Authors should create merge modules that provide default values and are compatible with earlier versions of Mergmod.dll.</span></span>
-   <span data-ttu-id="52f45-111">Proporcione información de personalización cuando la herramienta de cliente de configuración la solicite.</span><span class="sxs-lookup"><span data-stu-id="52f45-111">Provide customization information when prompted by the configuration client tool.</span></span> <span data-ttu-id="52f45-112">Los autores deben crear módulos de combinación que usan valores predeterminados cuando un usuario declina proporcionar información.</span><span class="sxs-lookup"><span data-stu-id="52f45-112">Authors should create merge modules that use default values when a user declines to provide information.</span></span>

 

 



