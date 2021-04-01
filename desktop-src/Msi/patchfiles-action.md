---
description: La acción PatchFiles consulta la tabla patch para determinar qué revisiones se van a aplicar. La acción PatchFiles también realiza la revisión en bytes de los archivos.
ms.assetid: 4026755e-a006-40c0-8816-de5358f4582e
title: Acción PatchFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53583a93089444f014d9cc837fb18acf21cec82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909830"
---
# <a name="patchfiles-action"></a><span data-ttu-id="68afd-104">Acción PatchFiles</span><span class="sxs-lookup"><span data-stu-id="68afd-104">PatchFiles Action</span></span>

<span data-ttu-id="68afd-105">La acción PatchFiles consulta la [tabla patch](patch-table.md) para determinar qué revisiones se van a aplicar.</span><span class="sxs-lookup"><span data-stu-id="68afd-105">The PatchFiles action queries the [Patch table](patch-table.md) to determine which patches are to be applied.</span></span> <span data-ttu-id="68afd-106">La acción PatchFiles también realiza la revisión en bytes de los archivos.</span><span class="sxs-lookup"><span data-stu-id="68afd-106">The PatchFiles action also performs the byte-wise patching of the files.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="68afd-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="68afd-107">Sequence Restrictions</span></span>

<span data-ttu-id="68afd-108">Si el archivo que se va a revisar no está instalado, la acción PatchFiles debe aparecer después de la [acción InstallFiles](installfiles-action.md) que instala el archivo.</span><span class="sxs-lookup"><span data-stu-id="68afd-108">If the file that is to be patched is not installed, the PatchFiles action must come after the [InstallFiles action](installfiles-action.md) that installs the file.</span></span> <span data-ttu-id="68afd-109">Los archivos instalados anteriormente se pueden revisar en cualquier momento de la secuencia de acciones.</span><span class="sxs-lookup"><span data-stu-id="68afd-109">Previously installed files may be patched at any point in the action sequence.</span></span> <span data-ttu-id="68afd-110">La [acción DuplicateFiles](duplicatefiles-action.md) debe aparecer después de la acción PatchFiles para evitar la duplicación de la versión no revisada del archivo.</span><span class="sxs-lookup"><span data-stu-id="68afd-110">The [DuplicateFiles Action](duplicatefiles-action.md) must come after the PatchFiles action to prevent duplicating the unpatched version of the file.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="68afd-111">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="68afd-111">ActionData Messages</span></span>



| <span data-ttu-id="68afd-112">Campo</span><span class="sxs-lookup"><span data-stu-id="68afd-112">Field</span></span> | <span data-ttu-id="68afd-113">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="68afd-113">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="68afd-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="68afd-114">\[1\]</span></span> | <span data-ttu-id="68afd-115">Identificador del archivo revisado.</span><span class="sxs-lookup"><span data-stu-id="68afd-115">Identifier of patched file.</span></span>                   |
| <span data-ttu-id="68afd-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="68afd-116">\[2\]</span></span> | <span data-ttu-id="68afd-117">Identificador del directorio que contiene el archivo revisado.</span><span class="sxs-lookup"><span data-stu-id="68afd-117">Identifier of directory holding patched file.</span></span> |
| <span data-ttu-id="68afd-118">\[3\]</span><span class="sxs-lookup"><span data-stu-id="68afd-118">\[3\]</span></span> | <span data-ttu-id="68afd-119">Tamaño de la revisión en bytes.</span><span class="sxs-lookup"><span data-stu-id="68afd-119">Size of patch in bytes.</span></span>                       |



 

 

 



