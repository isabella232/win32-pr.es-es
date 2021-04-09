---
description: ICE79 valida las referencias a los componentes y las características especificados en los campos de la base de datos mediante el tipo de datos condition.
ms.assetid: f0a8ceac-084a-4693-b27d-f610eec4702a
title: ICE79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9081297f2bf2f11283380c0f057bd0fbec417975
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154812"
---
# <a name="ice79"></a><span data-ttu-id="0666a-103">ICE79</span><span class="sxs-lookup"><span data-stu-id="0666a-103">ICE79</span></span>

<span data-ttu-id="0666a-104">ICE79 valida las referencias a los componentes y las características especificados en los campos de la base de datos mediante el tipo de datos [Condition](condition.md) .</span><span class="sxs-lookup"><span data-stu-id="0666a-104">ICE79 validates the references to components and features entered in the database fields using the [Condition](condition.md) data type.</span></span>

## <a name="result"></a><span data-ttu-id="0666a-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="0666a-105">Result</span></span>

<span data-ttu-id="0666a-106">ICE79 expone dos advertencias.</span><span class="sxs-lookup"><span data-stu-id="0666a-106">ICE79 posts two warnings.</span></span>



| <span data-ttu-id="0666a-107">ADVERTENCIA de ICE79</span><span class="sxs-lookup"><span data-stu-id="0666a-107">ICE79 warning</span></span>                                                                      | <span data-ttu-id="0666a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="0666a-108">Description</span></span>                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="0666a-109">Falta la tabla de validación en la base de datos \_ .</span><span class="sxs-lookup"><span data-stu-id="0666a-109">Database is missing \_Validation table.</span></span> <span data-ttu-id="0666a-110">No se pudieron comprobar por completo los nombres de propiedad.</span><span class="sxs-lookup"><span data-stu-id="0666a-110">Could not completely check property names.</span></span> | <span data-ttu-id="0666a-111">Falta la [ \_ tabla de validación](-validation-table.md)en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="0666a-111">Database is missing [\_Validation table](-validation-table.md).</span></span> |
| <span data-ttu-id="0666a-112">Error al recuperar valores de la columna \[ 2 \] de la tabla \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="0666a-112">Error retrieving values from column \[2\] in table \[1\].</span></span> <span data-ttu-id="0666a-113">Se omitirá la columna.</span><span class="sxs-lookup"><span data-stu-id="0666a-113">Skipping Column.</span></span>         | <span data-ttu-id="0666a-114">Error al recuperar el valor.</span><span class="sxs-lookup"><span data-stu-id="0666a-114">Error retrieving value.</span></span>                                          |



 

<span data-ttu-id="0666a-115">ICE79 expone dos errores.</span><span class="sxs-lookup"><span data-stu-id="0666a-115">ICE79 posts two errors.</span></span>



| <span data-ttu-id="0666a-116">Error ICE79</span><span class="sxs-lookup"><span data-stu-id="0666a-116">ICE79 error</span></span>                                                          | <span data-ttu-id="0666a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="0666a-117">Description</span></span>                               |
|----------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="0666a-118">Se hace referencia al componente '% ls ' en la columna '% s '. ' % s ' de la fila% s no es válido.</span><span class="sxs-lookup"><span data-stu-id="0666a-118">Component '%ls' referenced in column '%s'.'%s' of row %s is invalid.</span></span> | <span data-ttu-id="0666a-119">Se encontró una referencia de componente no válida.</span><span class="sxs-lookup"><span data-stu-id="0666a-119">An invalid component reference was found.</span></span> |
| <span data-ttu-id="0666a-120">Se hace referencia a la característica '% ls ' en la columna '% s '. ' % s ' de la fila% s no es válido.</span><span class="sxs-lookup"><span data-stu-id="0666a-120">Feature '%ls' referenced in column '%s'.'%s' of row %s is invalid.</span></span>   | <span data-ttu-id="0666a-121">Se encontró una referencia de característica no válida</span><span class="sxs-lookup"><span data-stu-id="0666a-121">An invalid feature reference was found</span></span>    |



 

## <a name="example"></a><span data-ttu-id="0666a-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0666a-122">Example</span></span>

<span data-ttu-id="0666a-123">ICE79 notifica los siguientes errores para el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0666a-123">ICE79 reports the following errors for the example:</span></span>

``` syntax
Component 'NoSuchComponent' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom2 is invalid.
Feature 'NoSuchFeature' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom1 is invalid.
```

<span data-ttu-id="0666a-124">En este ejemplo, NoSuchComponent no está presente en la [tabla de componentes](component-table.md) y NoSuchFeature no está presente en la tabla de [características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="0666a-124">In this example, NoSuchComponent is absent from the [Component table](component-table.md) and NoSuchFeature is absent from the [Feature table](feature-table.md).</span></span>

<span data-ttu-id="0666a-125">[Tabla InstallExecuteSequence](installexecutesequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="0666a-125">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="0666a-126">Acción</span><span class="sxs-lookup"><span data-stu-id="0666a-126">Action</span></span>  | <span data-ttu-id="0666a-127">Condición</span><span class="sxs-lookup"><span data-stu-id="0666a-127">Condition</span></span>                                |
|---------|------------------------------------------|
| <span data-ttu-id="0666a-128">Especial</span><span class="sxs-lookup"><span data-stu-id="0666a-128">Custom1</span></span> | <span data-ttu-id="0666a-129">TESTACTION = 1046 y &NoSuchFeature>2</span><span class="sxs-lookup"><span data-stu-id="0666a-129">TESTACTION=1046 AND &NoSuchFeature>2</span></span>  |
| <span data-ttu-id="0666a-130">Visión</span><span class="sxs-lookup"><span data-stu-id="0666a-130">Custom2</span></span> | <span data-ttu-id="0666a-131">TESTACTION = 146 y $NoSuchComponent>2</span><span class="sxs-lookup"><span data-stu-id="0666a-131">TESTACTION=146 AND $NoSuchComponent>2</span></span> |



 

<span data-ttu-id="0666a-132">Para corregir estos errores, escriba registros válidos para NoSuchFeature y NoSuchComponent en las tablas de características y componentes.</span><span class="sxs-lookup"><span data-stu-id="0666a-132">To fix these errors, enter valid records for NoSuchFeature and NoSuchComponent in the Feature and Component tables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0666a-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0666a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0666a-134">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="0666a-134">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



