---
description: Los autores deben ejecutar la validación en cada módulo de combinación nuevo o recién modificado antes de intentar combinar el módulo en una base de datos de instalación por primera vez.
ms.assetid: 8d6794af-403a-416e-8ace-1af3f193414b
title: Validar módulos de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8bbe7f1c1ea32baa39cadd7c729f3a8ca3ac17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154788"
---
# <a name="validating-merge-modules"></a><span data-ttu-id="17929-103">Validar módulos de combinación</span><span class="sxs-lookup"><span data-stu-id="17929-103">Validating Merge Modules</span></span>

<span data-ttu-id="17929-104">Los autores deben ejecutar la validación en cada módulo de combinación nuevo o recién modificado antes de intentar combinar el módulo en una base de datos de instalación por primera vez.</span><span class="sxs-lookup"><span data-stu-id="17929-104">Authors should run validation on every new, or newly modified, merge module before attempting to merge the module into an installation database for the first time.</span></span> <span data-ttu-id="17929-105">La validación del módulo de combinación funciona de la misma forma que la [validación de paquetes](package-validation.md) , pero utiliza un conjunto diferente de [evaluadores de coherencia interna](internal-consistency-evaluators-ices.md) (CIEM) específicos para los módulos de combinación.</span><span class="sxs-lookup"><span data-stu-id="17929-105">Merge module validation works in the same way as [package validation](package-validation.md) but uses a different set of [Internal Consistency Evaluators](internal-consistency-evaluators-ices.md) (ICEs) specific to merge modules.</span></span> <span data-ttu-id="17929-106">Para obtener más información acerca de este módulo de combinación ICEs, consulte [Merge Module Ice Reference](merge-module-ice-reference.md).</span><span class="sxs-lookup"><span data-stu-id="17929-106">For more information about these merge module ICEs, see [Merge Module ICE Reference](merge-module-ice-reference.md).</span></span>

<span data-ttu-id="17929-107">El módulo de combinación ICEs se almacena en el archivo. Cub del módulo de combinación, Mergemod. Cub.</span><span class="sxs-lookup"><span data-stu-id="17929-107">Merge module ICEs are stored in the merge module .cub file, Mergemod.cub.</span></span> <span data-ttu-id="17929-108">La instalación de la herramienta Orca o msival2 también proporciona los archivos logo. Cub, Darice. Cub y Mergemod. Cub.</span><span class="sxs-lookup"><span data-stu-id="17929-108">The installation of the Orca tool or msival2 also provides the Logo.cub, Darice.cub, and Mergemod.cub files.</span></span>

<span data-ttu-id="17929-109">Para obtener más información, consulte [Merge Module Ice Reference](merge-module-ice-reference.md).</span><span class="sxs-lookup"><span data-stu-id="17929-109">For more information, see [Merge Module ICE Reference](merge-module-ice-reference.md).</span></span>

 

 



