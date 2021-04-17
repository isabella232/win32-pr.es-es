---
description: Cuando un módulo admite varios idiomas, puede combinarlo en la misma base de datos Windows Installer varias veces, pero asegúrese de que cada combinación use un idioma diferente.
ms.assetid: 816b1f52-1ca2-4332-9a9b-462ea372c3bb
title: Combinar un módulo de varios idiomas en el mismo paquete varias veces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52552a68643d52c6aad97ed666b7dc1ae4043fd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678215"
---
# <a name="merging-a-multiple-language-module-into-the-same-package-multiple-times"></a><span data-ttu-id="b85e0-103">Combinar un módulo de varios idiomas en el mismo paquete varias veces</span><span class="sxs-lookup"><span data-stu-id="b85e0-103">Merging a Multiple Language Module into the Same Package Multiple Times</span></span>

<span data-ttu-id="b85e0-104">Cuando un módulo admite varios idiomas, puede combinarlo en la misma base de datos Windows Installer varias veces, pero asegúrese de que cada combinación use un idioma diferente.</span><span class="sxs-lookup"><span data-stu-id="b85e0-104">When a module supports multiple languages, you can merge it into the same Windows Installer database multiple times, but make sure that each merge uses a different language.</span></span> <span data-ttu-id="b85e0-105">Antes de cada combinación, solicite un idioma diferente del módulo.</span><span class="sxs-lookup"><span data-stu-id="b85e0-105">Before each merge, request a different language from the module.</span></span> <span data-ttu-id="b85e0-106">La base de datos. msi resultante tiene un registro en la [tabla ModuleSignature](modulesignature-table.md) para cada combinación del módulo.</span><span class="sxs-lookup"><span data-stu-id="b85e0-106">The resulting .msi database then has a record in the [ModuleSignature Table](modulesignature-table.md) for each merge of the module.</span></span> <span data-ttu-id="b85e0-107">Los componentes que se comparten entre los lenguajes solo existen una vez en la [tabla de componentes](component-table.md), pero están asociados a cada idioma de la [tabla ModuleComponents](modulecomponents-table.md).</span><span class="sxs-lookup"><span data-stu-id="b85e0-107">Components that are shared between languages exist only one time in the [Component Table](component-table.md), but are associated with each language in the [ModuleComponents Table](modulecomponents-table.md).</span></span>

<span data-ttu-id="b85e0-108">Al combinar varios idiomas de un módulo en el mismo paquete, cada combinación debe cumplir las mismas restricciones en las páginas de códigos que los módulos de un solo idioma.</span><span class="sxs-lookup"><span data-stu-id="b85e0-108">When merging multiple languages of a module into the same package, each merge must satisfy the same restrictions on code pages as single-language modules.</span></span> <span data-ttu-id="b85e0-109">Los módulos no pueden contener cadenas en páginas de códigos diferentes.</span><span class="sxs-lookup"><span data-stu-id="b85e0-109">The modules cannot contain strings in different code pages.</span></span>

<span data-ttu-id="b85e0-110">Al combinar un módulo varias veces en un único archivo. msi, puede que tenga que modificar el orden de los archivos en la [tabla de archivos](file-table.md) para usar el archivo. cab existente del módulo directamente en su instalación.</span><span class="sxs-lookup"><span data-stu-id="b85e0-110">When merging a module multiple times into a single .msi file, you may need to modify the order of the files in the [File Table](file-table.md) to use the existing .cab from the module directly in your installation.</span></span> <span data-ttu-id="b85e0-111">El orden de los archivos en la tabla de archivos debe coincidir con el orden de los archivos del archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="b85e0-111">The order of files in the File Table must match the order of files in the .cab.</span></span> <span data-ttu-id="b85e0-112">Al combinar un módulo varias veces en una base de datos de instalación, se puede modificar la secuencia, ya que es posible que los archivos compartidos entre los lenguajes ya existan en el módulo a partir de una combinación anterior y tengan un número de secuencia relativo diferente.</span><span class="sxs-lookup"><span data-stu-id="b85e0-112">When merging a module multiple times into an installation database the sequence may be modified, because files shared between the languages may already exist in the module from a prior merge, and they have a different relative sequence number.</span></span>

 

 



