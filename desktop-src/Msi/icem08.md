---
description: ICEM08 garantiza que un módulo no excluya otro módulo del que dependa.
ms.assetid: 56d115b4-7410-4db2-a9af-bc6716f3358d
title: ICEM08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9767c6748f5a21d83bddb3b5fe93a0a8d7ea67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277749"
---
# <a name="icem08"></a><span data-ttu-id="cc4ed-103">ICEM08</span><span class="sxs-lookup"><span data-stu-id="cc4ed-103">ICEM08</span></span>

<span data-ttu-id="cc4ed-104">ICEM08 garantiza que un módulo no excluya otro módulo del que dependa.</span><span class="sxs-lookup"><span data-stu-id="cc4ed-104">ICEM08 ensures that a module does not exclude another module that it depends on.</span></span>

## <a name="result"></a><span data-ttu-id="cc4ed-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="cc4ed-105">Result</span></span>

<span data-ttu-id="cc4ed-106">ICEM08 expone un error cuando un módulo excluye otro módulo del que depende.</span><span class="sxs-lookup"><span data-stu-id="cc4ed-106">ICEM08 posts an error when a module excludes another module that it depends on.</span></span>

## <a name="example"></a><span data-ttu-id="cc4ed-107">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cc4ed-107">Example</span></span>

<span data-ttu-id="cc4ed-108">ICEM08 envía el siguiente mensaje de error para un módulo que contiene las entradas de base de datos que se muestran en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="cc4ed-108">ICEM08 posts the following error message for a module containing the database entries shown in the example.</span></span>

``` syntax
Error: This module requires module ModuleB.<GUID> (1033v1.0) but also 
lists it as an exclusion.
```

[<span data-ttu-id="cc4ed-109">Tabla ModuleDependency</span><span class="sxs-lookup"><span data-stu-id="cc4ed-109">ModuleDependency Table</span></span>](moduledependency-table.md)



| <span data-ttu-id="cc4ed-110">ModuleID</span><span class="sxs-lookup"><span data-stu-id="cc4ed-110">ModuleID</span></span>             | <span data-ttu-id="cc4ed-111">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="cc4ed-111">ModuleLanguage</span></span> | <span data-ttu-id="cc4ed-112">RequiredID</span><span class="sxs-lookup"><span data-stu-id="cc4ed-112">RequiredID</span></span>           | <span data-ttu-id="cc4ed-113">RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="cc4ed-113">RequiredLanguage</span></span> | <span data-ttu-id="cc4ed-114">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="cc4ed-114">RequiredVersion</span></span> |
|----------------------|----------------|----------------------|------------------|-----------------|
| <span data-ttu-id="cc4ed-115">Móduloa.<GUID></span><span class="sxs-lookup"><span data-stu-id="cc4ed-115">ModuleA.<GUID></span></span> | <span data-ttu-id="cc4ed-116">3082</span><span class="sxs-lookup"><span data-stu-id="cc4ed-116">1033</span></span>           | <span data-ttu-id="cc4ed-117">ModuleB.<GUID></span><span class="sxs-lookup"><span data-stu-id="cc4ed-117">ModuleB.<GUID></span></span> | <span data-ttu-id="cc4ed-118">3082</span><span class="sxs-lookup"><span data-stu-id="cc4ed-118">1033</span></span>             | <span data-ttu-id="cc4ed-119">1,0</span><span class="sxs-lookup"><span data-stu-id="cc4ed-119">1.0</span></span>             |



 

[<span data-ttu-id="cc4ed-120">Tabla ModuleExclusion</span><span class="sxs-lookup"><span data-stu-id="cc4ed-120">ModuleExclusion Table</span></span>](moduleexclusion-table.md)



| <span data-ttu-id="cc4ed-121">ModuleID</span><span class="sxs-lookup"><span data-stu-id="cc4ed-121">ModuleID</span></span>             | <span data-ttu-id="cc4ed-122">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="cc4ed-122">ModuleLanguage</span></span> | <span data-ttu-id="cc4ed-123">ExcludedID</span><span class="sxs-lookup"><span data-stu-id="cc4ed-123">ExcludedID</span></span>           | <span data-ttu-id="cc4ed-124">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="cc4ed-124">ExcludedLanguage</span></span> | <span data-ttu-id="cc4ed-125">ExcludedMinVersion</span><span class="sxs-lookup"><span data-stu-id="cc4ed-125">ExcludedMinVersion</span></span> | <span data-ttu-id="cc4ed-126">ExcludedMaxVersion</span><span class="sxs-lookup"><span data-stu-id="cc4ed-126">ExcludedMaxVersion</span></span> |
|----------------------|----------------|----------------------|------------------|--------------------|--------------------|
| <span data-ttu-id="cc4ed-127">Móduloa.<GUID></span><span class="sxs-lookup"><span data-stu-id="cc4ed-127">ModuleA.<GUID></span></span> | <span data-ttu-id="cc4ed-128">3082</span><span class="sxs-lookup"><span data-stu-id="cc4ed-128">1033</span></span>           | <span data-ttu-id="cc4ed-129">ModuleB.<GUID></span><span class="sxs-lookup"><span data-stu-id="cc4ed-129">ModuleB.<GUID></span></span> | <span data-ttu-id="cc4ed-130">3082</span><span class="sxs-lookup"><span data-stu-id="cc4ed-130">1033</span></span>             |                    | <span data-ttu-id="cc4ed-131">1,0</span><span class="sxs-lookup"><span data-stu-id="cc4ed-131">1.0</span></span>                |



 

<span data-ttu-id="cc4ed-132">Para corregir el error, quite la dependencia o la exclusión.</span><span class="sxs-lookup"><span data-stu-id="cc4ed-132">To fix the error, remove either the dependency or the exclusion.</span></span> <span data-ttu-id="cc4ed-133">Si ModuleB es una dependencia (RequiredID) de Modulea, no se puede excluir (como se muestra en la columna ExludedID de la tabla ModuleExclusion).</span><span class="sxs-lookup"><span data-stu-id="cc4ed-133">If ModuleB is a dependency (RequiredID) of ModuleA, you cannot exclude it (as shown in the ExludedID column of the ModuleExclusion table).</span></span> <span data-ttu-id="cc4ed-134">Si debe excluir ModuleB, debe quitar la dependencia del Móduloa en él.</span><span class="sxs-lookup"><span data-stu-id="cc4ed-134">If you must exclude ModuleB, then you must remove ModuleA's dependency on it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc4ed-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cc4ed-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc4ed-136">Referencia de módulo de combinación ICE</span><span class="sxs-lookup"><span data-stu-id="cc4ed-136">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



