---
description: ICE19 valida que los componentes anunciados hacen referencia a un archivo de la columna de ruta de acceso de la tabla de componentes y que un acceso directo anunciado hace referencia a un directorio de esta columna.
ms.assetid: 438153c1-bc4b-4ecf-ab85-d66ad69c987c
title: ICE19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a53aa3268a1c77f674d4a130c9de02c44b56243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277551"
---
# <a name="ice19"></a><span data-ttu-id="f3309-103">ICE19</span><span class="sxs-lookup"><span data-stu-id="f3309-103">ICE19</span></span>

<span data-ttu-id="f3309-104">ICE19 valida que los componentes anunciados hacen referencia a un archivo de la columna de ruta de acceso de la [tabla de componentes](component-table.md) y que un acceso directo anunciado hace referencia a un directorio de esta columna.</span><span class="sxs-lookup"><span data-stu-id="f3309-104">ICE19 validates that advertised components reference a file in the KeyPath column of the [Component table](component-table.md) and that an advertised shortcut references a directory in this column.</span></span>

<span data-ttu-id="f3309-105">ICE19 valida que los componentes o accesos directos anunciados tienen un ComponentId.</span><span class="sxs-lookup"><span data-stu-id="f3309-105">ICE19 validates that advertised components or shortcuts have a ComponentId.</span></span> <span data-ttu-id="f3309-106">Los componentes de la [tabla PublishComponent](publishcomponent-table.md), que no se anuncian en otra tabla, solo se comprueban para ver si tienen un ComponentID.</span><span class="sxs-lookup"><span data-stu-id="f3309-106">Components in the [PublishComponent table](publishcomponent-table.md), which are not advertised in another table, are only checked to see whether they have a ComponentId.</span></span>

## <a name="result"></a><span data-ttu-id="f3309-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="f3309-107">Result</span></span>

<span data-ttu-id="f3309-108">ICE19 envía un mensaje de error si la columna de ruta de acceso de la tabla de componentes no hace referencia a un archivo en el caso de un componente anunciado o un directorio en el caso de un acceso directo anunciado.</span><span class="sxs-lookup"><span data-stu-id="f3309-108">ICE19 posts an error message if the KeyPath column of the Component table does not reference a file in the case of an advertised component or a directory in the case of an advertised shortcut.</span></span> <span data-ttu-id="f3309-109">ICE19 envía un mensaje de error si alguno de los componentes o accesos directos anunciados no tiene un ComponentId.</span><span class="sxs-lookup"><span data-stu-id="f3309-109">ICE19 posts an error message if any advertised components or shortcuts do not have a ComponentId.</span></span>

## <a name="example"></a><span data-ttu-id="f3309-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f3309-110">Example</span></span>

<span data-ttu-id="f3309-111">ICE19 expone los siguientes mensajes de error para el ejemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="f3309-111">ICE19 posts the following error messages for the example shown:</span></span>

-   <span data-ttu-id="f3309-112">La extensión FLP hace referencia al componente Comp1, que no tiene especificado un ComponentId en la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="f3309-112">Extension flp references the component Comp1 which does not have a ComponentId specified in the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="f3309-113">La extensión exe hace referencia al componente Comp4, que hace referencia a un directorio como su ruta de rutas.</span><span class="sxs-lookup"><span data-stu-id="f3309-113">Extension exe references the component Comp4 which references a directory as its KeyPath.</span></span> <span data-ttu-id="f3309-114">La ruta de la ruta de la tabla de componentes es NULL.</span><span class="sxs-lookup"><span data-stu-id="f3309-114">The KeyPath is Null in the Component table.</span></span>
-   <span data-ttu-id="f3309-115">Shortcut Shortcut2 hace referencia al componente Comp3, que hace referencia a una entrada del registro como la ruta de acceso de la clave.</span><span class="sxs-lookup"><span data-stu-id="f3309-115">Shortcut Shortcut2 references the component Comp3 which references a Registry entry as the key path.</span></span> <span data-ttu-id="f3309-116">El valor de la columna Attributes de la tabla de componentes es 4.</span><span class="sxs-lookup"><span data-stu-id="f3309-116">The value of the Attributes column in the Component table is 4.</span></span>

<span data-ttu-id="f3309-117">[Tabla de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="f3309-117">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="f3309-118">Componente</span><span class="sxs-lookup"><span data-stu-id="f3309-118">Component</span></span> | <span data-ttu-id="f3309-119">ComponentId</span><span class="sxs-lookup"><span data-stu-id="f3309-119">ComponentId</span></span>                            | <span data-ttu-id="f3309-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="f3309-120">Attributes</span></span> | <span data-ttu-id="f3309-121">Rutas</span><span class="sxs-lookup"><span data-stu-id="f3309-121">KeyPath</span></span> |
|-----------|----------------------------------------|------------|---------|
| <span data-ttu-id="f3309-122">Comp1</span><span class="sxs-lookup"><span data-stu-id="f3309-122">Comp1</span></span>     | <span data-ttu-id="f3309-123">Null</span><span class="sxs-lookup"><span data-stu-id="f3309-123">Null</span></span>                                   | <span data-ttu-id="f3309-124">0</span><span class="sxs-lookup"><span data-stu-id="f3309-124">0</span></span>          | <span data-ttu-id="f3309-125">Archivo1</span><span class="sxs-lookup"><span data-stu-id="f3309-125">File1</span></span>   |
| <span data-ttu-id="f3309-126">Comp2</span><span class="sxs-lookup"><span data-stu-id="f3309-126">Comp2</span></span>     | {00000002-0003-0000-0000-624474736554} | <span data-ttu-id="f3309-127">0</span><span class="sxs-lookup"><span data-stu-id="f3309-127">0</span></span>          | <span data-ttu-id="f3309-128">Archivo2</span><span class="sxs-lookup"><span data-stu-id="f3309-128">File2</span></span>   |
| <span data-ttu-id="f3309-129">Comp3</span><span class="sxs-lookup"><span data-stu-id="f3309-129">Comp3</span></span>     | {00000003-0003-0000-0000-624474736554} | <span data-ttu-id="f3309-130">4</span><span class="sxs-lookup"><span data-stu-id="f3309-130">4</span></span>          | <span data-ttu-id="f3309-131">Reg3</span><span class="sxs-lookup"><span data-stu-id="f3309-131">Reg3</span></span>    |
| <span data-ttu-id="f3309-132">Comp4</span><span class="sxs-lookup"><span data-stu-id="f3309-132">Comp4</span></span>     | {00000004-0003-0000-0000-624474736554} | <span data-ttu-id="f3309-133">0</span><span class="sxs-lookup"><span data-stu-id="f3309-133">0</span></span>          | <span data-ttu-id="f3309-134">Null</span><span class="sxs-lookup"><span data-stu-id="f3309-134">Null</span></span>    |



 

<span data-ttu-id="f3309-135">[Tabla de extensión](extension-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="f3309-135">[Extension Table](extension-table.md) (partial)</span></span>



| <span data-ttu-id="f3309-136">Extensión</span><span class="sxs-lookup"><span data-stu-id="f3309-136">Extension</span></span> | <span data-ttu-id="f3309-137">Componente\_</span><span class="sxs-lookup"><span data-stu-id="f3309-137">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="f3309-138">FLP</span><span class="sxs-lookup"><span data-stu-id="f3309-138">flp</span></span>       | <span data-ttu-id="f3309-139">Comp1</span><span class="sxs-lookup"><span data-stu-id="f3309-139">Comp1</span></span>       |
| <span data-ttu-id="f3309-140">TST</span><span class="sxs-lookup"><span data-stu-id="f3309-140">tst</span></span>       | <span data-ttu-id="f3309-141">Comp2</span><span class="sxs-lookup"><span data-stu-id="f3309-141">Comp2</span></span>       |
| <span data-ttu-id="f3309-142">exe</span><span class="sxs-lookup"><span data-stu-id="f3309-142">exe</span></span>       | <span data-ttu-id="f3309-143">Comp4</span><span class="sxs-lookup"><span data-stu-id="f3309-143">Comp4</span></span>       |



 

<span data-ttu-id="f3309-144">[Tabla de acceso directo](shortcut-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="f3309-144">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="f3309-145">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="f3309-145">Shortcut</span></span>  | <span data-ttu-id="f3309-146">Componente\_</span><span class="sxs-lookup"><span data-stu-id="f3309-146">Component\_</span></span> | <span data-ttu-id="f3309-147">Característica\_</span><span class="sxs-lookup"><span data-stu-id="f3309-147">Feature\_</span></span>      |
|-----------|-------------|----------------|
| <span data-ttu-id="f3309-148">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="f3309-148">Shortcut1</span></span> | <span data-ttu-id="f3309-149">Comp4</span><span class="sxs-lookup"><span data-stu-id="f3309-149">Comp4</span></span>       | <span data-ttu-id="f3309-150">ProductFeature</span><span class="sxs-lookup"><span data-stu-id="f3309-150">ProductFeature</span></span> |
| <span data-ttu-id="f3309-151">Shortcut2</span><span class="sxs-lookup"><span data-stu-id="f3309-151">Shortcut2</span></span> | <span data-ttu-id="f3309-152">Comp3</span><span class="sxs-lookup"><span data-stu-id="f3309-152">Comp3</span></span>       | <span data-ttu-id="f3309-153">ProductFeature</span><span class="sxs-lookup"><span data-stu-id="f3309-153">ProductFeature</span></span> |



 

<span data-ttu-id="f3309-154">[Tabla de características](feature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="f3309-154">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="f3309-155">Característica</span><span class="sxs-lookup"><span data-stu-id="f3309-155">Feature</span></span>        |
|----------------|
| <span data-ttu-id="f3309-156">ProductFeature</span><span class="sxs-lookup"><span data-stu-id="f3309-156">ProductFeature</span></span> |



 

> [!Note]  
> <span data-ttu-id="f3309-157">Si la extensión FLP y exe hacen referencia al mismo componente, el servidor EXE o COM que los abre deben ser el mismo.</span><span class="sxs-lookup"><span data-stu-id="f3309-157">If the extension flp and exe both reference the same component, the EXE or COM server that opens them must be the same.</span></span> <span data-ttu-id="f3309-158">Este archivo EXE suele ser la ruta de la ruta de archivo del componente.</span><span class="sxs-lookup"><span data-stu-id="f3309-158">This EXE is normally the KeyPath for the Component.</span></span> <span data-ttu-id="f3309-159">En el caso de OFFICE, las extensiones doc y XLS no pueden hacer referencia al mismo componente porque el mismo EXE no abre ambas extensiones.</span><span class="sxs-lookup"><span data-stu-id="f3309-159">For OFFICE, the extensions doc and xls cannot reference the same component because the same EXE does not open both extensions.</span></span> <span data-ttu-id="f3309-160">Necesita winword.exe para abrir las extensiones de documento y necesita excel.exe para abrir las extensiones xls.</span><span class="sxs-lookup"><span data-stu-id="f3309-160">You need winword.exe to open doc extensions and you need excel.exe to open xls extensions.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f3309-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f3309-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3309-162">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="f3309-162">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



