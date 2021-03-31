---
description: ICE82 valida que la acción RegisterProduct, la acción RegisterUser, la acción PublishProduct y la acción PublishFeatures están presentes en la tabla InstallExecuteSequence. El paquete se valida si todas las acciones están presentes.
ms.assetid: b41a56f9-b57e-4133-ae7d-c51b36bab44f
title: ICE82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa6ba2e0bd07af06bf90c604c333966b5581ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816243"
---
# <a name="ice82"></a><span data-ttu-id="8b0bf-104">ICE82</span><span class="sxs-lookup"><span data-stu-id="8b0bf-104">ICE82</span></span>

<span data-ttu-id="8b0bf-105">ICE82 valida que la acción [RegisterProduct](registerproduct-action.md), la acción [RegisterUser](registeruser-action.md), la [acción PublishProduct](publishproduct-action.md)y la [acción PublishFeatures](publishfeatures-action.md) están presentes en la [tabla InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="8b0bf-105">ICE82 validates that the [RegisterProduct Action](registerproduct-action.md), [RegisterUser Action](registeruser-action.md), [PublishProduct Action](publishproduct-action.md), and [PublishFeatures Action](publishfeatures-action.md) are all present in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="8b0bf-106">El paquete se valida si todas las acciones están presentes.</span><span class="sxs-lookup"><span data-stu-id="8b0bf-106">The package is validated if all the actions are present.</span></span>

<span data-ttu-id="8b0bf-107">ICE82 publica una advertencia si hay dos acciones con el mismo número de secuencia enumeradas en las tablas InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence o AdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="8b0bf-107">ICE82 posts a warning if there are two actions with the same sequence number listed in the InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence, or AdvtExecuteSequence tables .</span></span>

## <a name="result"></a><span data-ttu-id="8b0bf-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="8b0bf-108">Result</span></span>

<span data-ttu-id="8b0bf-109">ICE82 expone las siguientes advertencias.</span><span class="sxs-lookup"><span data-stu-id="8b0bf-109">ICE82 posts the following warnings.</span></span>



| <span data-ttu-id="8b0bf-110">ADVERTENCIA de ICE82</span><span class="sxs-lookup"><span data-stu-id="8b0bf-110">ICE82 warning</span></span>                                                                                                                                                                                                                 | <span data-ttu-id="8b0bf-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b0bf-111">Description</span></span>                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b0bf-112">La tabla InstallExecuteSequence no contiene el conjunto de acciones que se mencionan a continuación: faltan acciones:</span><span class="sxs-lookup"><span data-stu-id="8b0bf-112">The InstallExecuteSequence table does not contain the set of actions mentioned below: Actions Missing:</span></span><br/> <span data-ttu-id="8b0bf-113">Publicar características</span><span class="sxs-lookup"><span data-stu-id="8b0bf-113">Publish Features</span></span><br/> <span data-ttu-id="8b0bf-114">Publicar producto</span><span class="sxs-lookup"><span data-stu-id="8b0bf-114">Publish Product</span></span><br/> <span data-ttu-id="8b0bf-115">Registrar producto</span><span class="sxs-lookup"><span data-stu-id="8b0bf-115">Register Product</span></span><br/> <span data-ttu-id="8b0bf-116">Registrar usuario</span><span class="sxs-lookup"><span data-stu-id="8b0bf-116">Register User</span></span><br/> | <span data-ttu-id="8b0bf-117">La acción personalizada ICE82 publica una advertencia si las cuatro acciones están ausentes.</span><span class="sxs-lookup"><span data-stu-id="8b0bf-117">ICE82 custom action posts a warning if all four actions are absent.</span></span>                                                                                                                                         |
| <span data-ttu-id="8b0bf-118">Esta acción \[ 1 \] tiene el número de secuencia 2 duplicado \[ \] en la tabla \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="8b0bf-118">This action \[1\] has duplicate sequence number \[2\] in the table \[3\].</span></span>                                                                                                                                                     | <span data-ttu-id="8b0bf-119">ICE82 publica una advertencia si hay dos acciones con el mismo número de secuencia enumeradas en las tablas InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence o AdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="8b0bf-119">ICE82 posts a warning if there are two actions with the same sequence number listed in the InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence, or AdvtExecuteSequence tables.</span></span> |



 

<span data-ttu-id="8b0bf-120">ICE82 expone los siguientes errores.</span><span class="sxs-lookup"><span data-stu-id="8b0bf-120">ICE82 posts the following errors.</span></span>



| <span data-ttu-id="8b0bf-121">Error ICE82</span><span class="sxs-lookup"><span data-stu-id="8b0bf-121">ICE82 error</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="8b0bf-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b0bf-122">Description</span></span>                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8b0bf-123">InstallExecuteSequence debe contener todas las acciones que se mencionan a continuación o ninguna de ellas.</span><span class="sxs-lookup"><span data-stu-id="8b0bf-123">The InstallExecuteSequence should either contain all of the actions mentioned below or none of them Actions Present</span></span><br/> <List of actions present> <br/> <span data-ttu-id="8b0bf-124">Faltan acciones:</span><span class="sxs-lookup"><span data-stu-id="8b0bf-124">Actions Missing:</span></span><br/> <List of actions missing> <br/> | <span data-ttu-id="8b0bf-125">ICE82 publica un error si algunas de las cuatro acciones están presentes y otras están ausentes.</span><span class="sxs-lookup"><span data-stu-id="8b0bf-125">ICE82 posts an error if some of the four actions are present and others are absent.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8b0bf-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8b0bf-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b0bf-127">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="8b0bf-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




