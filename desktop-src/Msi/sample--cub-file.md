---
description: 'Este ejemplo muestra el diseño de un archivo. Cub que contiene dos CIEM. El instalador ejecuta las acciones personalizadas en la secuencia: ICE01 y ICE08.'
ms.assetid: 609cd16a-4421-4082-855d-229f5ba7117b
title: Archivo. Cub de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e937b779e2a620ffc17cf936e37f74867f3dfdd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001099"
---
# <a name="sample-cub-file"></a><span data-ttu-id="98365-104">Archivo. Cub de ejemplo</span><span class="sxs-lookup"><span data-stu-id="98365-104">Sample .cub File</span></span>

<span data-ttu-id="98365-105">Este ejemplo muestra el diseño de un archivo. Cub que contiene dos [CIEM](internal-consistency-evaluators-ices.md).</span><span class="sxs-lookup"><span data-stu-id="98365-105">This sample illustrates the layout of a .cub file containing two [ICEs](internal-consistency-evaluators-ices.md).</span></span> <span data-ttu-id="98365-106">El instalador ejecuta las acciones personalizadas en la secuencia: ICE01 y ICE08.</span><span class="sxs-lookup"><span data-stu-id="98365-106">The installer executes the custom actions in the sequence: ICE01 and ICE08.</span></span>

<span data-ttu-id="98365-107">La acción personalizada ICE01 es un [tipo de acción personalizada 1](custom-action-type-1.md).</span><span class="sxs-lookup"><span data-stu-id="98365-107">The custom action ICE01 is a [Custom Action Type 1](custom-action-type-1.md).</span></span> <span data-ttu-id="98365-108">Es un punto de entrada a un archivo DLL que se almacena como una secuencia en el archivo. Cub.</span><span class="sxs-lookup"><span data-stu-id="98365-108">It is an entry point to a DLL that is stored as a stream in the .cub file.</span></span> <span data-ttu-id="98365-109">Esta secuencia aparece en la tabla binaria ice.dll.</span><span class="sxs-lookup"><span data-stu-id="98365-109">This stream is listed in the Binary Table ice.dll.</span></span>

<span data-ttu-id="98365-110">La acción personalizada ICE08 es un [tipo de acción personalizada 6](custom-action-type-6.md).</span><span class="sxs-lookup"><span data-stu-id="98365-110">The custom action ICE08 is a [Custom Action Type 6](custom-action-type-6.md).</span></span> <span data-ttu-id="98365-111">Es un punto de entrada a una función de VBScript que se almacena como una secuencia en el archivo. Cub.</span><span class="sxs-lookup"><span data-stu-id="98365-111">It is an entry point to a function in VBScript that is stored as a stream in the .cub file.</span></span> <span data-ttu-id="98365-112">Esta secuencia aparece en la tabla binaria como ice.vbs.</span><span class="sxs-lookup"><span data-stu-id="98365-112">This stream is listed in the Binary Table as ice.vbs.</span></span>

[<span data-ttu-id="98365-113">Tabla binaria</span><span class="sxs-lookup"><span data-stu-id="98365-113">Binary Table</span></span>](binary-table.md)



| <span data-ttu-id="98365-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="98365-114">Name</span></span>    | <span data-ttu-id="98365-115">Datos</span><span class="sxs-lookup"><span data-stu-id="98365-115">Data</span></span>                               |
|---------|------------------------------------|
| <span data-ttu-id="98365-116">ice.vbs</span><span class="sxs-lookup"><span data-stu-id="98365-116">ice.vbs</span></span> | <span data-ttu-id="98365-117">Datos binarios sin formato de ice.vbs</span><span class="sxs-lookup"><span data-stu-id="98365-117">Unformatted binary data of ice.vbs</span></span> |
| <span data-ttu-id="98365-118">ice.dll</span><span class="sxs-lookup"><span data-stu-id="98365-118">ice.dll</span></span> | <span data-ttu-id="98365-119">Datos binarios sin formato de ice.dll</span><span class="sxs-lookup"><span data-stu-id="98365-119">Unformatted binary data of ice.dll</span></span> |



 

[<span data-ttu-id="98365-120">Tabla CustomAction</span><span class="sxs-lookup"><span data-stu-id="98365-120">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="98365-121">Acción</span><span class="sxs-lookup"><span data-stu-id="98365-121">Action</span></span> | <span data-ttu-id="98365-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="98365-122">Type</span></span> | <span data-ttu-id="98365-123">Source</span><span class="sxs-lookup"><span data-stu-id="98365-123">Source</span></span>  | <span data-ttu-id="98365-124">Destino</span><span class="sxs-lookup"><span data-stu-id="98365-124">Target</span></span> |
|--------|------|---------|--------|
| <span data-ttu-id="98365-125">ICE01</span><span class="sxs-lookup"><span data-stu-id="98365-125">ICE01</span></span>  | <span data-ttu-id="98365-126">1</span><span class="sxs-lookup"><span data-stu-id="98365-126">1</span></span>    | <span data-ttu-id="98365-127">ice.dll</span><span class="sxs-lookup"><span data-stu-id="98365-127">ice.dll</span></span> | <span data-ttu-id="98365-128">ICE01</span><span class="sxs-lookup"><span data-stu-id="98365-128">ICE01</span></span>  |
| <span data-ttu-id="98365-129">ICE08</span><span class="sxs-lookup"><span data-stu-id="98365-129">ICE08</span></span>  | <span data-ttu-id="98365-130">6</span><span class="sxs-lookup"><span data-stu-id="98365-130">6</span></span>    | <span data-ttu-id="98365-131">ice.vbs</span><span class="sxs-lookup"><span data-stu-id="98365-131">ice.vbs</span></span> | <span data-ttu-id="98365-132">ICE02</span><span class="sxs-lookup"><span data-stu-id="98365-132">ICE02</span></span>  |



 

<span data-ttu-id="98365-133">\_Tabla ICESequence</span><span class="sxs-lookup"><span data-stu-id="98365-133">\_ICESequence Table</span></span>



| <span data-ttu-id="98365-134">Acción</span><span class="sxs-lookup"><span data-stu-id="98365-134">Action</span></span> | <span data-ttu-id="98365-135">Condición</span><span class="sxs-lookup"><span data-stu-id="98365-135">Condition</span></span> | <span data-ttu-id="98365-136">Secuencia</span><span class="sxs-lookup"><span data-stu-id="98365-136">Sequence</span></span> |
|--------|-----------|----------|
| <span data-ttu-id="98365-137">ICE01</span><span class="sxs-lookup"><span data-stu-id="98365-137">ICE01</span></span>  |           | <span data-ttu-id="98365-138">10</span><span class="sxs-lookup"><span data-stu-id="98365-138">10</span></span>       |
| <span data-ttu-id="98365-139">ICE08</span><span class="sxs-lookup"><span data-stu-id="98365-139">ICE08</span></span>  |           | <span data-ttu-id="98365-140">20</span><span class="sxs-lookup"><span data-stu-id="98365-140">20</span></span>       |



 

<span data-ttu-id="98365-141">\_Tabla especial</span><span class="sxs-lookup"><span data-stu-id="98365-141">\_Special Table</span></span>

<span data-ttu-id="98365-142">ICE01 y ICE08 no requieren la inclusión de tablas de procesamiento especiales.</span><span class="sxs-lookup"><span data-stu-id="98365-142">ICE01 and ICE08 do not require the inclusion of special processing tables.</span></span> <span data-ttu-id="98365-143">Cuando el archivo. Cub contiene tablas especiales, también deben incluirse en la \_ tabla de validación.</span><span class="sxs-lookup"><span data-stu-id="98365-143">When the .cub file contains special tables they must also be included in the \_Validation Table.</span></span>

[<span data-ttu-id="98365-144">\_Tabla de validación</span><span class="sxs-lookup"><span data-stu-id="98365-144">\_Validation Table</span></span>](-validation-table.md)



| <span data-ttu-id="98365-145">Tabla</span><span class="sxs-lookup"><span data-stu-id="98365-145">Table</span></span>         | <span data-ttu-id="98365-146">Columna</span><span class="sxs-lookup"><span data-stu-id="98365-146">Column</span></span>    | <span data-ttu-id="98365-147">Nullable</span><span class="sxs-lookup"><span data-stu-id="98365-147">Nullable</span></span> | <span data-ttu-id="98365-148">MinValue</span><span class="sxs-lookup"><span data-stu-id="98365-148">MinValue</span></span> | <span data-ttu-id="98365-149">MaxValue</span><span class="sxs-lookup"><span data-stu-id="98365-149">MaxValue</span></span> | <span data-ttu-id="98365-150">KeyTable</span><span class="sxs-lookup"><span data-stu-id="98365-150">KeyTable</span></span> | <span data-ttu-id="98365-151">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="98365-151">KeyColumn</span></span> | <span data-ttu-id="98365-152">Category</span><span class="sxs-lookup"><span data-stu-id="98365-152">Category</span></span>                         | <span data-ttu-id="98365-153">Set</span><span class="sxs-lookup"><span data-stu-id="98365-153">Set</span></span> | <span data-ttu-id="98365-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="98365-154">Description</span></span> |
|---------------|-----------|----------|----------|----------|----------|-----------|----------------------------------|-----|-------------|
| <span data-ttu-id="98365-155">Binary</span><span class="sxs-lookup"><span data-stu-id="98365-155">Binary</span></span>        | <span data-ttu-id="98365-156">Nombre</span><span class="sxs-lookup"><span data-stu-id="98365-156">Name</span></span>      | <span data-ttu-id="98365-157">N</span><span class="sxs-lookup"><span data-stu-id="98365-157">N</span></span>        |          |          |          |           | [<span data-ttu-id="98365-158">Identificador</span><span class="sxs-lookup"><span data-stu-id="98365-158">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="98365-159">Binary</span><span class="sxs-lookup"><span data-stu-id="98365-159">Binary</span></span>        | <span data-ttu-id="98365-160">Datos</span><span class="sxs-lookup"><span data-stu-id="98365-160">Data</span></span>      | <span data-ttu-id="98365-161">N</span><span class="sxs-lookup"><span data-stu-id="98365-161">N</span></span>        |          |          |          |           | [<span data-ttu-id="98365-162">Binario</span><span class="sxs-lookup"><span data-stu-id="98365-162">Binary</span></span>](binary.md)             |     |             |
| <span data-ttu-id="98365-163">CustomAction</span><span class="sxs-lookup"><span data-stu-id="98365-163">CustomAction</span></span>  | <span data-ttu-id="98365-164">Acción</span><span class="sxs-lookup"><span data-stu-id="98365-164">Action</span></span>    | <span data-ttu-id="98365-165">N</span><span class="sxs-lookup"><span data-stu-id="98365-165">N</span></span>        |          |          |          |           | [<span data-ttu-id="98365-166">Identificador</span><span class="sxs-lookup"><span data-stu-id="98365-166">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="98365-167">CustomAction</span><span class="sxs-lookup"><span data-stu-id="98365-167">CustomAction</span></span>  | <span data-ttu-id="98365-168">Tipo</span><span class="sxs-lookup"><span data-stu-id="98365-168">Type</span></span>      | <span data-ttu-id="98365-169">N</span><span class="sxs-lookup"><span data-stu-id="98365-169">N</span></span>        |          |          |          |           | [<span data-ttu-id="98365-170">Entero</span><span class="sxs-lookup"><span data-stu-id="98365-170">Integer</span></span>](integer.md)           |     |             |
| <span data-ttu-id="98365-171">CustomAction</span><span class="sxs-lookup"><span data-stu-id="98365-171">CustomAction</span></span>  | <span data-ttu-id="98365-172">Source</span><span class="sxs-lookup"><span data-stu-id="98365-172">Source</span></span>    | <span data-ttu-id="98365-173">Y</span><span class="sxs-lookup"><span data-stu-id="98365-173">Y</span></span>        |          |          |          |           | [<span data-ttu-id="98365-174">CustomSource</span><span class="sxs-lookup"><span data-stu-id="98365-174">CustomSource</span></span>](customsource.md) |     |             |
| <span data-ttu-id="98365-175">CustomAction</span><span class="sxs-lookup"><span data-stu-id="98365-175">CustomAction</span></span>  | <span data-ttu-id="98365-176">Destino</span><span class="sxs-lookup"><span data-stu-id="98365-176">Target</span></span>    | <span data-ttu-id="98365-177">Y</span><span class="sxs-lookup"><span data-stu-id="98365-177">Y</span></span>        |          |          |          |           | [<span data-ttu-id="98365-178">Formatea</span><span class="sxs-lookup"><span data-stu-id="98365-178">Formatted</span></span>](formatted.md)       |     |             |
| <span data-ttu-id="98365-179">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="98365-179">\_ICESequence</span></span> | <span data-ttu-id="98365-180">Acción</span><span class="sxs-lookup"><span data-stu-id="98365-180">Action</span></span>    | <span data-ttu-id="98365-181">N</span><span class="sxs-lookup"><span data-stu-id="98365-181">N</span></span>        |          |          |          |           | [<span data-ttu-id="98365-182">Identificador</span><span class="sxs-lookup"><span data-stu-id="98365-182">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="98365-183">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="98365-183">\_ICESequence</span></span> | <span data-ttu-id="98365-184">Condición</span><span class="sxs-lookup"><span data-stu-id="98365-184">Condition</span></span> | <span data-ttu-id="98365-185">Y</span><span class="sxs-lookup"><span data-stu-id="98365-185">Y</span></span>        |          |          |          |           | [<span data-ttu-id="98365-186">Condition</span><span class="sxs-lookup"><span data-stu-id="98365-186">Condition</span></span>](condition.md)       |     |             |
| <span data-ttu-id="98365-187">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="98365-187">\_ICESequence</span></span> | <span data-ttu-id="98365-188">Secuencia</span><span class="sxs-lookup"><span data-stu-id="98365-188">Sequence</span></span>  | <span data-ttu-id="98365-189">Y</span><span class="sxs-lookup"><span data-stu-id="98365-189">Y</span></span>        |          |          |          |           | [<span data-ttu-id="98365-190">Entero</span><span class="sxs-lookup"><span data-stu-id="98365-190">Integer</span></span>](integer.md)           |     |             |



 

 

 



