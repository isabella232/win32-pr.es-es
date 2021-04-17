---
description: ICEM03 comprueba que todas las acciones del módulo son acciones base o derivan de una acción base válida.
ms.assetid: 8e2b5921-32cf-45e8-9906-30002574a712
title: ICEM03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f368fa50a71153c41eebaa9ee5084449cf824993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652746"
---
# <a name="icem03"></a><span data-ttu-id="103f0-103">ICEM03</span><span class="sxs-lookup"><span data-stu-id="103f0-103">ICEM03</span></span>

<span data-ttu-id="103f0-104">ICEM03 comprueba que todas las acciones del módulo son acciones base o derivan de una acción base válida.</span><span class="sxs-lookup"><span data-stu-id="103f0-104">ICEM03 verifies that all actions in the module are either base actions or derive from a valid base action.</span></span>

<span data-ttu-id="103f0-105">El módulo de combinación ICEs se almacena en un archivo. Cub de módulo de combinación denominado Mergemod. Cub y no en el archivo. Cub que contiene el ICEs usado para la validación del paquete.</span><span class="sxs-lookup"><span data-stu-id="103f0-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="103f0-106">Resultado</span><span class="sxs-lookup"><span data-stu-id="103f0-106">Result</span></span>

<span data-ttu-id="103f0-107">ICEM03 expone los mensajes de error de un módulo que contiene acciones en una tabla de secuencia que no es una acción base o que se deriva de una acción base válida.</span><span class="sxs-lookup"><span data-stu-id="103f0-107">ICEM03 posts the error messages for a module containing actions in a sequence table that is not a base action or derived from a valid base action.</span></span>

## <a name="example"></a><span data-ttu-id="103f0-108">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="103f0-108">Example</span></span>

<span data-ttu-id="103f0-109">ICEM03 expone los siguientes mensajes de error para un módulo que contiene las entradas de base de datos que se muestran a continuación.</span><span class="sxs-lookup"><span data-stu-id="103f0-109">ICEM03 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The action 'Action1' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
The action 'Action2' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
```

[<span data-ttu-id="103f0-110">Tabla ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="103f0-110">ModuleInstallExecuteSequence Table</span></span>](moduleinstallexecutesequence-table.md)



| <span data-ttu-id="103f0-111">Acción</span><span class="sxs-lookup"><span data-stu-id="103f0-111">Action</span></span>  | <span data-ttu-id="103f0-112">Secuencia</span><span class="sxs-lookup"><span data-stu-id="103f0-112">Sequence</span></span> | <span data-ttu-id="103f0-113">BaseAction</span><span class="sxs-lookup"><span data-stu-id="103f0-113">BaseAction</span></span> | <span data-ttu-id="103f0-114">Después</span><span class="sxs-lookup"><span data-stu-id="103f0-114">After</span></span> | <span data-ttu-id="103f0-115">Condición</span><span class="sxs-lookup"><span data-stu-id="103f0-115">Condition</span></span> |
|---------|----------|------------|-------|-----------|
| <span data-ttu-id="103f0-116">Action1</span><span class="sxs-lookup"><span data-stu-id="103f0-116">Action1</span></span> |          | <span data-ttu-id="103f0-117">Action2</span><span class="sxs-lookup"><span data-stu-id="103f0-117">Action2</span></span>    | <span data-ttu-id="103f0-118">0</span><span class="sxs-lookup"><span data-stu-id="103f0-118">0</span></span>     |           |
| <span data-ttu-id="103f0-119">Action2</span><span class="sxs-lookup"><span data-stu-id="103f0-119">Action2</span></span> |          | <span data-ttu-id="103f0-120">Action1</span><span class="sxs-lookup"><span data-stu-id="103f0-120">Action1</span></span>    | <span data-ttu-id="103f0-121">0</span><span class="sxs-lookup"><span data-stu-id="103f0-121">0</span></span>     |           |



 

<span data-ttu-id="103f0-122">ICEM03 expone errores para estas dos acciones porque hacen referencia a ellas como acciones base en la tabla ModuleInstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="103f0-122">ICEM03 posts errors for these two actions because they refer to each other as base actions in the ModuleInstallExecuteSequence table.</span></span> <span data-ttu-id="103f0-123">Todas las acciones de las tablas [ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), [ModuleAdvtUISequence](moduleadvtuisequence-table.md), [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence](moduleinstalluisequence-table.md)y [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) deben ser acciones base o derivar su posición de la combinación de otra acción y una marca Before y after.</span><span class="sxs-lookup"><span data-stu-id="103f0-123">All actions in the [ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), [ModuleAdvtUISequence](moduleadvtuisequence-table.md), [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence](moduleinstalluisequence-table.md), and [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) tables must either be base actions or derive their position from the combination of another action and a before and after flag.</span></span>

<span data-ttu-id="103f0-124">Para corregir este error, determine las acciones básicas de las dos acciones.</span><span class="sxs-lookup"><span data-stu-id="103f0-124">To fix this error, determine the base actions for the two actions.</span></span> <span data-ttu-id="103f0-125">Agregue un registro para las acciones base con un número de secuencia predeterminado.</span><span class="sxs-lookup"><span data-stu-id="103f0-125">Add a record for the base actions with a default sequence number.</span></span> <span data-ttu-id="103f0-126">Para Action1 y Action2, escriba los nombres de acción base en la columna BaseAction y 0 o 1 en la columna after.</span><span class="sxs-lookup"><span data-stu-id="103f0-126">For Action1 and Action2 enter the base action names in the BaseAction column and 0 or 1 in the After column.</span></span>

## <a name="related-topics"></a><span data-ttu-id="103f0-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="103f0-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="103f0-128">Referencia de módulo de combinación ICE</span><span class="sxs-lookup"><span data-stu-id="103f0-128">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



