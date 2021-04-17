---
description: ICE72 comprueba que las acciones personalizadas no integradas no se usan en la tabla AdvtExecuteSequence.
ms.assetid: b04227d5-5bd6-434a-860c-498d787a1f0a
title: ICE72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d9d8e1859ffd8123cc7aa3dc801c5484d28ccb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668361"
---
# <a name="ice72"></a><span data-ttu-id="8d083-103">ICE72</span><span class="sxs-lookup"><span data-stu-id="8d083-103">ICE72</span></span>

<span data-ttu-id="8d083-104">ICE72 comprueba que las acciones personalizadas no integradas no se usan en la [tabla AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="8d083-104">ICE72 verifies that non-built-in custom actions are not used in the [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span> <span data-ttu-id="8d083-105">En concreto, solo se permiten las acciones personalizadas de tipo 19, tipo 35 y tipo 51 en la tabla AdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="8d083-105">Specifically, only type 19, type 35, and type 51 custom actions are allowed in the AdvtExecuteSequence table.</span></span> <span data-ttu-id="8d083-106">Si se usan otras acciones personalizadas, es posible que el anuncio no se comporte de la manera esperada.</span><span class="sxs-lookup"><span data-stu-id="8d083-106">If other custom actions are used, advertisement may not behave as expected.</span></span>

## <a name="result"></a><span data-ttu-id="8d083-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="8d083-107">Result</span></span>

<span data-ttu-id="8d083-108">ICE72 devuelve un error si la tabla AdvExecuteSequence usa acciones personalizadas distintas del tipo 35, tipo 51 y tipo 19.</span><span class="sxs-lookup"><span data-stu-id="8d083-108">ICE72 returns an error if the AdvExecuteSequence table uses custom actions other than type 35, type 51, and type 19.</span></span>

## <a name="example"></a><span data-ttu-id="8d083-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8d083-109">Example</span></span>

<span data-ttu-id="8d083-110">ICE72 notifica el siguiente error para el ejemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="8d083-110">ICE72 reports the following error for the example shown:</span></span>

``` syntax
Custom Action 'CA1' in the AdvtExecuteSequence table is not allowed. Only built-in custom actions are allowed.
```

<span data-ttu-id="8d083-111">Para corregir el error, quite ' CA1 ' de la tabla AdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="8d083-111">To fix the error, remove 'CA1' from the AdvtExecuteSequence table.</span></span>

<span data-ttu-id="8d083-112">[Tabla AdvtExecuteSequence](advtexecutesequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="8d083-112">[AdvtExecuteSequence Table](advtexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="8d083-113">Acción</span><span class="sxs-lookup"><span data-stu-id="8d083-113">Action</span></span> |
|--------|
| <span data-ttu-id="8d083-114">CA1</span><span class="sxs-lookup"><span data-stu-id="8d083-114">CA1</span></span>    |
| <span data-ttu-id="8d083-115">CA35</span><span class="sxs-lookup"><span data-stu-id="8d083-115">CA35</span></span>   |



 

<span data-ttu-id="8d083-116">[Tabla CustomAction](customaction-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="8d083-116">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="8d083-117">Acción</span><span class="sxs-lookup"><span data-stu-id="8d083-117">Action</span></span> | <span data-ttu-id="8d083-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="8d083-118">Type</span></span> |
|--------|------|
| <span data-ttu-id="8d083-119">CA1</span><span class="sxs-lookup"><span data-stu-id="8d083-119">CA1</span></span>    | <span data-ttu-id="8d083-120">1</span><span class="sxs-lookup"><span data-stu-id="8d083-120">1</span></span>    |
| <span data-ttu-id="8d083-121">CA35</span><span class="sxs-lookup"><span data-stu-id="8d083-121">CA35</span></span>   | <span data-ttu-id="8d083-122">35</span><span class="sxs-lookup"><span data-stu-id="8d083-122">35</span></span>   |



 

## <a name="tables-used-during-execution"></a><span data-ttu-id="8d083-123">Tablas usadas durante la ejecución</span><span class="sxs-lookup"><span data-stu-id="8d083-123">Tables used during execution</span></span>

[<span data-ttu-id="8d083-124">Tabla AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="8d083-124">AdvtExecuteSequence Table</span></span>](advtexecutesequence-table.md)

[<span data-ttu-id="8d083-125">Tabla CustomAction</span><span class="sxs-lookup"><span data-stu-id="8d083-125">CustomAction Table</span></span>](customaction-table.md)

## <a name="related-topics"></a><span data-ttu-id="8d083-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8d083-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d083-127">Tipo de acción personalizada 19</span><span class="sxs-lookup"><span data-stu-id="8d083-127">Custom Action Type 19</span></span>](custom-action-type-19.md)
</dt> <dt>

[<span data-ttu-id="8d083-128">Tipo de acción personalizada 35</span><span class="sxs-lookup"><span data-stu-id="8d083-128">Custom Action Type 35</span></span>](custom-action-type-35.md)
</dt> <dt>

[<span data-ttu-id="8d083-129">Tipo de acción personalizada 51</span><span class="sxs-lookup"><span data-stu-id="8d083-129">Custom Action Type 51</span></span>](custom-action-type-51.md)
</dt> <dt>

[<span data-ttu-id="8d083-130">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="8d083-130">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



