---
description: ICE26 valida las tablas de secuencia en una base de datos Windows Installer.
ms.assetid: 7ea47452-3147-4d39-961d-a10eca8328c9
title: ICE26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7b110d0b15b37441170980d0fd3e96e2eb00d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910910"
---
# <a name="ice26"></a><span data-ttu-id="efb11-103">ICE26</span><span class="sxs-lookup"><span data-stu-id="efb11-103">ICE26</span></span>

<span data-ttu-id="efb11-104">ICE26 valida que cada una de las [*tablas de secuencia*](s-gly.md) siguientes contiene las acciones requeridas por la tabla y que no contiene ninguna acción no permitida en la tabla:</span><span class="sxs-lookup"><span data-stu-id="efb11-104">ICE26 validates that each of the following [*sequence tables*](s-gly.md) contain the actions that are required by the table and does not contain any actions disallowed in the table:</span></span>

-   [<span data-ttu-id="efb11-105">Tabla AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="efb11-105">AdminUISequence table</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="efb11-106">Tabla AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="efb11-106">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="efb11-107">Tabla InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="efb11-107">InstallUISequence table</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="efb11-108">Tabla InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="efb11-108">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)

## <a name="result"></a><span data-ttu-id="efb11-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="efb11-109">Result</span></span>

<span data-ttu-id="efb11-110">ICE26 envía un mensaje de error si el paquete de instalación tiene una tabla de secuencia que carece de una acción necesaria o que contiene una acción que no está permitida para la tabla.</span><span class="sxs-lookup"><span data-stu-id="efb11-110">ICE26 posts an error message if the installation package has a sequence table that lacks a required action or that contains an action that is disallowed for the table.</span></span>

## <a name="example"></a><span data-ttu-id="efb11-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="efb11-111">Example</span></span>



| <span data-ttu-id="efb11-112">Error ICE26</span><span class="sxs-lookup"><span data-stu-id="efb11-112">ICE26 error</span></span>                                                                   | <span data-ttu-id="efb11-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="efb11-113">Description</span></span>                                                                                                                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efb11-114">Acción: se requiere ' Action1 ' en la tabla de secuencia InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="efb11-114">Action: 'Action1' is required in the InstallExecuteSequence Sequence table.</span></span>   | <span data-ttu-id="efb11-115">Falta una acción necesaria en la tabla de secuencia indicada.</span><span class="sxs-lookup"><span data-stu-id="efb11-115">A required action is missing from the indicated sequence table.</span></span> <span data-ttu-id="efb11-116">Vea el template.msi o las tablas de secuencia sugeridas en [mediante una tabla de secuencia](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="efb11-116">See the template.msi or the suggested sequence tables in [Using a Sequence Table](using-a-sequence-table.md).</span></span> |
| <span data-ttu-id="efb11-117">Acción: ' Action2 ' está prohibido en la tabla de secuencia InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="efb11-117">Action: 'Action2' is prohibited in the InstallExecuteSequence Sequence table.</span></span> | <span data-ttu-id="efb11-118">Esta acción no puede estar en la tabla de secuencia indicada.</span><span class="sxs-lookup"><span data-stu-id="efb11-118">This action cannot be in the indicated sequence table.</span></span> <span data-ttu-id="efb11-119">Quite esta acción de la tabla de secuencia.</span><span class="sxs-lookup"><span data-stu-id="efb11-119">Remove this action from the sequence table.</span></span>                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="efb11-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="efb11-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efb11-121">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="efb11-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



