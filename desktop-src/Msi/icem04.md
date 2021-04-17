---
description: ICEM04 comprueba que las tablas vacías necesarias del módulo de combinación están vacías. Error al corregir un error que indica que los informes de ICEM04 pueden producir una combinación incorrecta del módulo de combinación.
ms.assetid: c6f64f5e-be65-485b-8831-e377535bd335
title: ICEM04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ef993690ae690e0651db1538196998c4dd28c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652493"
---
# <a name="icem04"></a><span data-ttu-id="6bc71-104">ICEM04</span><span class="sxs-lookup"><span data-stu-id="6bc71-104">ICEM04</span></span>

<span data-ttu-id="6bc71-105">ICEM04 comprueba que las tablas vacías necesarias del módulo de combinación están vacías.</span><span class="sxs-lookup"><span data-stu-id="6bc71-105">ICEM04 verifies that the merge module's required empty tables are empty.</span></span> <span data-ttu-id="6bc71-106">Error al corregir un error que indica que los informes de ICEM04 pueden producir una combinación incorrecta del módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="6bc71-106">Failure to fix an error that ICEM04 reports can result in incorrect merging of the merge module.</span></span>

## <a name="result"></a><span data-ttu-id="6bc71-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="6bc71-107">Result</span></span>

<span data-ttu-id="6bc71-108">ICEM04 expone un error cuando las tablas vacías requeridas del módulo de combinación no están vacías.</span><span class="sxs-lookup"><span data-stu-id="6bc71-108">ICEM04 posts an error when the merge module's required empty tables are not empty.</span></span>

## <a name="example"></a><span data-ttu-id="6bc71-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6bc71-109">Example</span></span>

<span data-ttu-id="6bc71-110">ICEM04 expone los siguientes mensajes de error para un módulo que contiene las entradas de base de datos que se muestran.</span><span class="sxs-lookup"><span data-stu-id="6bc71-110">ICEM04 posts the following error messages for a module that contains the database entries shown.</span></span>

``` syntax
An empty FeatureComponents table is required in a Merge Module.

The Merge Module contains the 'ModuleInstallExecuteSequence' table. It 
must therefore have an empty 'InstallExecuteSequence' table.

Action 'CostInitialize' found in the AdvtExecuteSequence table. This 
table must be empty in a Merge Module
```

<span data-ttu-id="6bc71-111">En la tabla siguiente se muestra una [tabla AdvtExecuteSequence](advtexecutesequence-table.md)parcial.</span><span class="sxs-lookup"><span data-stu-id="6bc71-111">The following table shows you a partial [AdvtExecuteSequence Table](advtexecutesequence-table.md).</span></span>



| <span data-ttu-id="6bc71-112">Acción</span><span class="sxs-lookup"><span data-stu-id="6bc71-112">Action</span></span>         | <span data-ttu-id="6bc71-113">Secuencia</span><span class="sxs-lookup"><span data-stu-id="6bc71-113">Sequence</span></span> |
|----------------|----------|
| <span data-ttu-id="6bc71-114">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="6bc71-114">CostInitialize</span></span> | <span data-ttu-id="6bc71-115">1</span><span class="sxs-lookup"><span data-stu-id="6bc71-115">1</span></span>        |



 

<span data-ttu-id="6bc71-116">La lista siguiente muestra el contenido parcial de módulo CRT:</span><span class="sxs-lookup"><span data-stu-id="6bc71-116">The following list shows you the partial contents of MergeModule:</span></span>

-   <span data-ttu-id="6bc71-117">ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="6bc71-117">ModuleInstallExecuteSequence</span></span>
-   <span data-ttu-id="6bc71-118">ModuleAdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="6bc71-118">ModuleAdvtExecuteSequence</span></span>
-   <span data-ttu-id="6bc71-119">InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="6bc71-119">InstallUISequence</span></span>

<span data-ttu-id="6bc71-120">En el ejemplo siguiente se muestra otro posible error.</span><span class="sxs-lookup"><span data-stu-id="6bc71-120">The following example shows you another possible error.</span></span>

``` syntax
Feature-Component '[1].[2]' found in the FeatureComponents table. The 
FeatureComponents table must be empty in a Merge Module.
```

<span data-ttu-id="6bc71-121">Si un módulo de combinación contiene una tabla de secuencia de módulo, debe contener la tabla de secuencia vacía correspondiente, tanto si la tabla de secuencia de módulo está vacía como si no.</span><span class="sxs-lookup"><span data-stu-id="6bc71-121">If a merge module contains a module sequence table, it must contain the corresponding empty sequence table, whether or not the module sequence table is empty.</span></span> <span data-ttu-id="6bc71-122">Por ejemplo, si el módulo de combinación contiene la [tabla ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), también debe contener una tabla AdminExecuteSequence vacía.</span><span class="sxs-lookup"><span data-stu-id="6bc71-122">For example, if the merge module contains the [ModuleAdminExecuteSequence Table](moduleadminexecutesequence-table.md), it must also contain an empty AdminExecuteSequence table.</span></span>

<span data-ttu-id="6bc71-123">La [tabla FeatureComponents](featurecomponents-table.md) es necesaria en todos los módulos de combinación y debe estar vacía.</span><span class="sxs-lookup"><span data-stu-id="6bc71-123">The [FeatureComponents Table](featurecomponents-table.md) is required in all merge modules and must be empty.</span></span>

<span data-ttu-id="6bc71-124">En el procedimiento siguiente se muestra cómo corregir los errores.</span><span class="sxs-lookup"><span data-stu-id="6bc71-124">The following procedure shows you how to fix errors.</span></span>

<span data-ttu-id="6bc71-125">**Para corregir errores**</span><span class="sxs-lookup"><span data-stu-id="6bc71-125">**To fix errors**</span></span>

1.  <span data-ttu-id="6bc71-126">Agregue una [tabla FeatureComponents](featurecomponents-table.md) vacía al módulo Merge.</span><span class="sxs-lookup"><span data-stu-id="6bc71-126">Add an empty [FeatureComponents Table](featurecomponents-table.md) to the merge module.</span></span>
2.  <span data-ttu-id="6bc71-127">Agregue una [tabla InstallExecuteSequence](installexecutesequence-table.md) vacía al módulo Merge.</span><span class="sxs-lookup"><span data-stu-id="6bc71-127">Add an empty [InstallExecuteSequence Table](installexecutesequence-table.md) to the merge module.</span></span>
3.  <span data-ttu-id="6bc71-128">Quite la acción ' CostInitialize ' de la [tabla AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="6bc71-128">Remove the 'CostInitialize' action from the [AdvtExecuteSequence Table](advtexecutesequence-table.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="6bc71-129">Esta tabla debe estar vacía en un módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="6bc71-129">This table must be empty in a merge module.</span></span> <span data-ttu-id="6bc71-130">Las acciones solo deben aparecer en la tabla ModuleAdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="6bc71-130">Actions should only appear in the ModuleAdvtExecuteSequence table.</span></span>

     

## <a name="tables-used-during-execution"></a><span data-ttu-id="6bc71-131">Tablas usadas durante la ejecución</span><span class="sxs-lookup"><span data-stu-id="6bc71-131">Tables Used During Execution</span></span>

<span data-ttu-id="6bc71-132">En la lista siguiente se identifican las tablas que se usan durante la ejecución:</span><span class="sxs-lookup"><span data-stu-id="6bc71-132">The following list identifies the tables that are used during execution:</span></span>

-   [<span data-ttu-id="6bc71-133">Tabla FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="6bc71-133">FeatureComponents Table</span></span>](featurecomponents-table.md)
-   <span data-ttu-id="6bc71-134">\*Tablas de secuencia de módulo y \* tablas de secuencia correspondientes.</span><span class="sxs-lookup"><span data-stu-id="6bc71-134">Module\*Sequence tables and corresponding \*Sequence tables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bc71-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6bc71-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bc71-136">Acerca de los módulos de combinación</span><span class="sxs-lookup"><span data-stu-id="6bc71-136">About Merge Modules</span></span>](about-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="6bc71-137">Referencia de módulo de combinación ICE</span><span class="sxs-lookup"><span data-stu-id="6bc71-137">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



