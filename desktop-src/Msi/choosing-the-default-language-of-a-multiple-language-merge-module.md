---
description: El idioma predeterminado de un módulo de combinación es el idioma que se muestra en la tabla ModuleSignature del módulo antes de que se apliquen las transformaciones del lenguaje. Este es también el primer idioma que aparece en la propiedad Resumen de la plantilla.
ms.assetid: 4d795727-684c-4dc1-8b46-d72b69c455c3
title: Elegir el idioma predeterminado de un módulo de combinación de varios idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758a3b47b7a41777652a11a1cdc1b7f380055cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909034"
---
# <a name="choosing-the-default-language-of-a-multiple-language-merge-module"></a><span data-ttu-id="0b252-104">Elegir el idioma predeterminado de un módulo de combinación de varios idiomas</span><span class="sxs-lookup"><span data-stu-id="0b252-104">Choosing the Default Language of a Multiple Language Merge Module</span></span>

<span data-ttu-id="0b252-105">El idioma predeterminado de un módulo de combinación es el idioma que se muestra en la [tabla ModuleSignature](modulesignature-table.md) del módulo antes de que se apliquen las transformaciones del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="0b252-105">The default language for a merge module is the language that is listed in the [ModuleSignature Table](modulesignature-table.md) of the module before language transforms are applied.</span></span> <span data-ttu-id="0b252-106">Este es también el primer idioma que aparece en la propiedad [**Resumen**](template-summary.md) de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="0b252-106">This is also the first language that is listed in the [**Template Summary**](template-summary.md) Property.</span></span>

<span data-ttu-id="0b252-107">El idioma predeterminado del módulo debe ser uno de los idiomas más específicos que se admiten, ya que el idioma predeterminado siempre se comprueba primero y, si cumple el idioma solicitado, se usa incluso si otro idioma es una coincidencia mejor.</span><span class="sxs-lookup"><span data-stu-id="0b252-107">The default language for the module should be one of the most specific languages that you support, because the default language is always checked first, and if it satisfies the requested language, it is used even if another language is a better match.</span></span> <span data-ttu-id="0b252-108">Por ejemplo, si un módulo admite 1033 y 0, 1033 debe ser el idioma predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0b252-108">For example, if a module supports 1033 and 0, 1033 should be the default language.</span></span> <span data-ttu-id="0b252-109">Si 0 fuera el idioma predeterminado, siempre cumpliría cualquier solicitud y la transformación 1033 nunca se utilizaría, aunque 1033 sea el lenguaje exacto solicitado.</span><span class="sxs-lookup"><span data-stu-id="0b252-109">If 0 were the default language, it would always satisfy any request, and the 1033 transform would never be used, even if 1033 is the exact language requested.</span></span>

 

 



