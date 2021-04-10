---
description: ICEM14 valida la columna de valor de la tabla ModuleSubstitution.
ms.assetid: e07ba63a-e748-4835-ae1b-9f7d30e46d39
title: ICEM14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72223f27338fb08efe4ea95b817acebd6234063f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155293"
---
# <a name="icem14"></a><span data-ttu-id="457f2-103">ICEM14</span><span class="sxs-lookup"><span data-stu-id="457f2-103">ICEM14</span></span>

<span data-ttu-id="457f2-104">ICEM14 valida la columna de valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="457f2-104">ICEM14 validates the Value Column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="457f2-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="457f2-105">Result</span></span>

<span data-ttu-id="457f2-106">ICEM14 expone los siguientes errores.</span><span class="sxs-lookup"><span data-stu-id="457f2-106">ICEM14 posts the following errors.</span></span>



| <span data-ttu-id="457f2-107">Error</span><span class="sxs-lookup"><span data-stu-id="457f2-107">Error</span></span>                                                                                                                                                         | <span data-ttu-id="457f2-108">Significado</span><span class="sxs-lookup"><span data-stu-id="457f2-108">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="457f2-109">La cadena de reemplazo en la columna ModuleSubstitution. Value de la fila \[ 1 \] . \[ 2 \] . \[ 3 \] no se encuentra en la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="457f2-109">The replacement string in ModuleSubstitution.Value column in row \[1\].\[2\].\[3\] is not found in ModuleConfiguration table.</span></span>                                 | <span data-ttu-id="457f2-110">\[1 \] . \[ 2 \] . \[ 3 \] hace referencia a una clave principal *TABLE. Row. Column* para una fila de la tabla ModuleSubstitution.</span><span class="sxs-lookup"><span data-stu-id="457f2-110">\[1\].\[2\].\[3\] refers to a *table.row.column* primary key for a row in the ModuleSubstitution table.</span></span> <span data-ttu-id="457f2-111">La plantilla de formato en el campo de valor de esta fila no se corresponde con una fila de atributos configurables de la [tabla ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="457f2-111">The formatting template in the Value field of this row does not correspond to a row of configurable attributes in the [ModuleConfiguration Table](moduleconfiguration-table.md).</span></span>                                                            |
| <span data-ttu-id="457f2-112">En la tabla ModuleSubstitution de la fila \[ 1 \] . \[ 2 \] . \[ 3 \] , se indica un elemento configurable en la tabla '% s '.</span><span class="sxs-lookup"><span data-stu-id="457f2-112">In ModuleSubstitution table in row \[1\].\[2\].\[3\], a configurable item is indicated in the table '%s'.</span></span> <span data-ttu-id="457f2-113">La tabla '% s ' no debe contener elementos configurables.</span><span class="sxs-lookup"><span data-stu-id="457f2-113">The table '%s' must not contain configurable items.</span></span> | <span data-ttu-id="457f2-114">Una de las tablas siguientes aparece en la columna tabla de la tabla ModuleSubstitution: [ModuleSubstitution](modulesubstitution-table.md), [ModuleConfiguration](moduleconfiguration-table.md), [ModuleExclusion](moduleexclusion-table.md)o [ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="457f2-114">One of the following tables is listed in the Table column of the ModuleSubstitution table: [ModuleSubstitution](modulesubstitution-table.md), [ModuleConfiguration](moduleconfiguration-table.md), [ModuleExclusion](moduleexclusion-table.md), or [ModuleSignature](modulesignature-table.md).</span></span> <span data-ttu-id="457f2-115">Estas tablas no pueden contener campos configurables.</span><span class="sxs-lookup"><span data-stu-id="457f2-115">These tables cannot contain configurable fields.</span></span> |
| <span data-ttu-id="457f2-116">En la tabla ModuleSubstitution de la fila \[ 1 \] . \[ 2 \] . \[ 3 \] , se especifica una cadena de reemplazo vacía.</span><span class="sxs-lookup"><span data-stu-id="457f2-116">In ModuleSubstitution table in row \[1\].\[2\].\[3\], an empty replacement string is specified.</span></span>                                                               | <span data-ttu-id="457f2-117">La plantilla de formato en el campo de valor de esta fila no se corresponde con una fila de atributos configurables de la [tabla ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="457f2-117">The formatting template in the Value field of this row does not correspond to a row of configurable attributes in the [ModuleConfiguration Table](moduleconfiguration-table.md).</span></span>                                                                                                                                                                    |



 

<span data-ttu-id="457f2-118">ICEM14 envía la siguiente advertencia.</span><span class="sxs-lookup"><span data-stu-id="457f2-118">ICEM14 posts the following warning.</span></span>



| <span data-ttu-id="457f2-119">Advertencia</span><span class="sxs-lookup"><span data-stu-id="457f2-119">Warning</span></span>                                                                  | <span data-ttu-id="457f2-120">Significado</span><span class="sxs-lookup"><span data-stu-id="457f2-120">Meaning</span></span>                                  |
|--------------------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="457f2-121">La tabla ModuleSubstitution existe pero falta la tabla ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="457f2-121">ModuleSubstitution table exists but ModuleConfiguration table is missing</span></span> | <span data-ttu-id="457f2-122">Falta la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="457f2-122">The ModuleConfiguration table is absent.</span></span> |



 

## <a name="table-used-during-execution"></a><span data-ttu-id="457f2-123">Tabla utilizada durante la ejecución</span><span class="sxs-lookup"><span data-stu-id="457f2-123">Table Used During Execution</span></span>

[<span data-ttu-id="457f2-124">Tabla ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="457f2-124">ModuleSubstitution table</span></span>](modulesubstitution-table.md)

[<span data-ttu-id="457f2-125">Tabla ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="457f2-125">ModuleConfiguration table</span></span>](moduleconfiguration-table.md)

## <a name="related-topics"></a><span data-ttu-id="457f2-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="457f2-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="457f2-127">Referencia de módulo de combinación ICE</span><span class="sxs-lookup"><span data-stu-id="457f2-127">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



