---
description: Este es un ejemplo de una tabla de secuencia.
ms.assetid: 25b3667a-1478-48c4-9c41-4defd25a0103
title: Ejemplo detallado de tabla de secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4698d5270f2f246fe6e676799ea239e47a950c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669835"
---
# <a name="sequence-table-detailed-example"></a><span data-ttu-id="1fc77-103">Ejemplo detallado de tabla de secuencias</span><span class="sxs-lookup"><span data-stu-id="1fc77-103">Sequence Table Detailed Example</span></span>

<span data-ttu-id="1fc77-104">Este es un ejemplo de una tabla de secuencia.</span><span class="sxs-lookup"><span data-stu-id="1fc77-104">Here is an example of a sequence table.</span></span>



| <span data-ttu-id="1fc77-105">Acción</span><span class="sxs-lookup"><span data-stu-id="1fc77-105">Action</span></span>                                          | <span data-ttu-id="1fc77-106">Condición</span><span class="sxs-lookup"><span data-stu-id="1fc77-106">Condition</span></span>                                                       | <span data-ttu-id="1fc77-107">Secuencia</span><span class="sxs-lookup"><span data-stu-id="1fc77-107">Sequence</span></span> |
|-------------------------------------------------|-----------------------------------------------------------------|----------|
| [<span data-ttu-id="1fc77-108">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="1fc77-108">LaunchConditions</span></span>](launchconditions-action.md) |                                                                 |          |
| [<span data-ttu-id="1fc77-109">AppSearch</span><span class="sxs-lookup"><span data-stu-id="1fc77-109">AppSearch</span></span>](appsearch-action.md)               |                                                                 | <span data-ttu-id="1fc77-110">200</span><span class="sxs-lookup"><span data-stu-id="1fc77-110">200</span></span>      |
| [<span data-ttu-id="1fc77-111">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="1fc77-111">CCPSearch</span></span>](ccpsearch-action.md)               | <span data-ttu-id="1fc77-112">prueba de CCP \_</span><span class="sxs-lookup"><span data-stu-id="1fc77-112">CCP\_TEST</span></span>                                                       | <span data-ttu-id="1fc77-113">300</span><span class="sxs-lookup"><span data-stu-id="1fc77-113">300</span></span>      |
| <span data-ttu-id="1fc77-114">CCPDialog</span><span class="sxs-lookup"><span data-stu-id="1fc77-114">CCPDialog</span></span>                                       | <span data-ttu-id="1fc77-115">NO se ha \_ ejecutado el CCP \_</span><span class="sxs-lookup"><span data-stu-id="1fc77-115">NOT\_CCP\_SUCCESS</span></span>                                               | <span data-ttu-id="1fc77-116">400</span><span class="sxs-lookup"><span data-stu-id="1fc77-116">400</span></span>      |
| <span data-ttu-id="1fc77-117">MyCustomConfig</span><span class="sxs-lookup"><span data-stu-id="1fc77-117">MyCustomConfig</span></span>                                  | <span data-ttu-id="1fc77-118">NO [ **instalado**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="1fc77-118">NOT [**Installed**](installed.md)</span></span>                              | <span data-ttu-id="1fc77-119">500</span><span class="sxs-lookup"><span data-stu-id="1fc77-119">500</span></span>      |
| [<span data-ttu-id="1fc77-120">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="1fc77-120">CostInitialize</span></span>](costinitialize-action.md)     |                                                                 | <span data-ttu-id="1fc77-121">600</span><span class="sxs-lookup"><span data-stu-id="1fc77-121">600</span></span>      |
| [<span data-ttu-id="1fc77-122">FileCost</span><span class="sxs-lookup"><span data-stu-id="1fc77-122">FileCost</span></span>](filecost-action.md)                 |                                                                 | <span data-ttu-id="1fc77-123">700</span><span class="sxs-lookup"><span data-stu-id="1fc77-123">700</span></span>      |
| [<span data-ttu-id="1fc77-124">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="1fc77-124">CostFinalize</span></span>](costfinalize-action.md)         |                                                                 | <span data-ttu-id="1fc77-125">800</span><span class="sxs-lookup"><span data-stu-id="1fc77-125">800</span></span>      |
| <span data-ttu-id="1fc77-126">InstallDialog</span><span class="sxs-lookup"><span data-stu-id="1fc77-126">InstallDialog</span></span>                                   | <span data-ttu-id="1fc77-127">NO [ **instalado**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="1fc77-127">NOT [**Installed**](installed.md)</span></span>                              | <span data-ttu-id="1fc77-128">900</span><span class="sxs-lookup"><span data-stu-id="1fc77-128">900</span></span>      |
| <span data-ttu-id="1fc77-129">MaintenanceDialog</span><span class="sxs-lookup"><span data-stu-id="1fc77-129">MaintenanceDialog</span></span>                               | <span data-ttu-id="1fc77-130">[**Instalado**](installed.md) Y no [ **reanudar**](resume.md)</span><span class="sxs-lookup"><span data-stu-id="1fc77-130">[**Installed**](installed.md) AND NOT [**Resume**](resume.md)</span></span> | <span data-ttu-id="1fc77-131">1000</span><span class="sxs-lookup"><span data-stu-id="1fc77-131">1000</span></span>     |
| <span data-ttu-id="1fc77-132">ActionDialog</span><span class="sxs-lookup"><span data-stu-id="1fc77-132">ActionDialog</span></span>                                    |                                                                 | <span data-ttu-id="1fc77-133">1100</span><span class="sxs-lookup"><span data-stu-id="1fc77-133">1100</span></span>     |
| [<span data-ttu-id="1fc77-134">RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="1fc77-134">RegisterProduct</span></span>](registerproduct-action.md)   |                                                                 | <span data-ttu-id="1fc77-135">1200</span><span class="sxs-lookup"><span data-stu-id="1fc77-135">1200</span></span>     |
| [<span data-ttu-id="1fc77-136">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="1fc77-136">InstallValidate</span></span>](installvalidate-action.md)   |                                                                 | <span data-ttu-id="1fc77-137">1300</span><span class="sxs-lookup"><span data-stu-id="1fc77-137">1300</span></span>     |
| [<span data-ttu-id="1fc77-138">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="1fc77-138">InstallFiles</span></span>](installfiles-action.md)         |                                                                 | <span data-ttu-id="1fc77-139">1400</span><span class="sxs-lookup"><span data-stu-id="1fc77-139">1400</span></span>     |
| <span data-ttu-id="1fc77-140">MyCustomAction</span><span class="sxs-lookup"><span data-stu-id="1fc77-140">MyCustomAction</span></span>                                  | <span data-ttu-id="1fc77-141">$MyComponent > 2</span><span class="sxs-lookup"><span data-stu-id="1fc77-141">$MyComponent > 2</span></span>                                             | <span data-ttu-id="1fc77-142">1.500</span><span class="sxs-lookup"><span data-stu-id="1fc77-142">1500</span></span>     |
| [<span data-ttu-id="1fc77-143">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="1fc77-143">InstallFinalize</span></span>](installfinalize-action.md)   |                                                                 | <span data-ttu-id="1fc77-144">1600</span><span class="sxs-lookup"><span data-stu-id="1fc77-144">1600</span></span>     |



 

<span data-ttu-id="1fc77-145">Las siguientes acciones de esta tabla de secuencia las define el instalador y son ejemplos de acciones estándar:</span><span class="sxs-lookup"><span data-stu-id="1fc77-145">The following actions in this sequence table are defined by the installer and are examples of standard actions:</span></span>

[<span data-ttu-id="1fc77-146">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="1fc77-146">LaunchConditions</span></span>](launchconditions-action.md)

 

[<span data-ttu-id="1fc77-147">AppSearch</span><span class="sxs-lookup"><span data-stu-id="1fc77-147">AppSearch</span></span>](appsearch-action.md)

 

[<span data-ttu-id="1fc77-148">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="1fc77-148">CCPSearch</span></span>](ccpsearch-action.md)

 

[<span data-ttu-id="1fc77-149">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="1fc77-149">CostInitialize</span></span>](costinitialize-action.md)

 

[<span data-ttu-id="1fc77-150">FileCost</span><span class="sxs-lookup"><span data-stu-id="1fc77-150">FileCost</span></span>](filecost-action.md)

 

[<span data-ttu-id="1fc77-151">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="1fc77-151">CostFinalize</span></span>](costfinalize-action.md)

 

[<span data-ttu-id="1fc77-152">RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="1fc77-152">RegisterProduct</span></span>](registerproduct-action.md)

 

[<span data-ttu-id="1fc77-153">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="1fc77-153">InstallFiles</span></span>](installfiles-action.md)

 

[<span data-ttu-id="1fc77-154">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="1fc77-154">InstallFiles</span></span>](installfiles-action.md)

 

[<span data-ttu-id="1fc77-155">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="1fc77-155">InstallValidate</span></span>](installvalidate-action.md)

<span data-ttu-id="1fc77-156">Las siguientes acciones fueron definidas por el autor de la tabla y son ejemplos de [acciones personalizadas](custom-actions.md) y deben aparecer en la [tabla CustomAction](customaction-table.md):</span><span class="sxs-lookup"><span data-stu-id="1fc77-156">The following actions were defined by the table's author and are examples of [custom actions](custom-actions.md) and must be listed in the [CustomAction table](customaction-table.md):</span></span>

<span data-ttu-id="1fc77-157">MyCustomConfig</span><span class="sxs-lookup"><span data-stu-id="1fc77-157">MyCustomConfig</span></span>

 

<span data-ttu-id="1fc77-158">MyCustomAction</span><span class="sxs-lookup"><span data-stu-id="1fc77-158">MyCustomAction</span></span>

<span data-ttu-id="1fc77-159">Las entradas restantes en el campo acción son claves externas en la [tabla del cuadro de diálogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="1fc77-159">The remaining entries in the Action field are foreign keys into the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="1fc77-160">Especifican los nombres de los cuadros de diálogo que se mostrarán si el campo condition se evalúa como true.</span><span class="sxs-lookup"><span data-stu-id="1fc77-160">They specify the names of dialog boxes that will displayed if the condition field evaluates to True.</span></span>

<span data-ttu-id="1fc77-161">CCPDialog</span><span class="sxs-lookup"><span data-stu-id="1fc77-161">CCPDialog</span></span>

 

<span data-ttu-id="1fc77-162">InstallDialog</span><span class="sxs-lookup"><span data-stu-id="1fc77-162">InstallDialog</span></span>

 

<span data-ttu-id="1fc77-163">MaintenanceDialog</span><span class="sxs-lookup"><span data-stu-id="1fc77-163">MaintenanceDialog</span></span>

 

<span data-ttu-id="1fc77-164">ActionDialog</span><span class="sxs-lookup"><span data-stu-id="1fc77-164">ActionDialog</span></span>

<span data-ttu-id="1fc77-165">La columna condición hace que el instalador omita la acción si la propiedad o expresión de este campo es false.</span><span class="sxs-lookup"><span data-stu-id="1fc77-165">The Condition column causes the installer to skip the action if the property or expression in this field is False.</span></span> <span data-ttu-id="1fc77-166">La propiedad [**installed**](installed.md) y la propiedad [**resume**](resume.md) son ejemplos de propiedades que se establecen mediante el instalador.</span><span class="sxs-lookup"><span data-stu-id="1fc77-166">The [**Installed**](installed.md) property and the [**RESUME**](resume.md) property are example of properties that are set by the installer.</span></span> <span data-ttu-id="1fc77-167">La propiedad [**installed**](installed.md) se establece en true si el producto ya está instalado y se establece la propiedad [**resume**](resume.md) si se reanuda una instalación suspendida.</span><span class="sxs-lookup"><span data-stu-id="1fc77-167">The [**Installed**](installed.md) property is set to true if the product is already installed and the [**RESUME**](resume.md) property is set if resuming a suspended installation.</span></span> <span data-ttu-id="1fc77-168">Las \_ propiedades CCP test y not \_ CCP \_ Success son ejemplos de propiedades que el usuario puede establecer en la línea de comandos mediante la instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1fc77-168">The CCP\_TEST and the NOT\_CCP\_SUCCESS properties are examples of properties that can be set at the command line by the user installing the application.</span></span>

<span data-ttu-id="1fc77-169">Todas las acciones se ejecutan en secuencia con los siguientes pasos condicionales:</span><span class="sxs-lookup"><span data-stu-id="1fc77-169">All actions run in sequence with the following conditional steps:</span></span>

-   <span data-ttu-id="1fc77-170">CPPSearch se ejecuta solo si \_ se establece la prueba de CCP.</span><span class="sxs-lookup"><span data-stu-id="1fc77-170">The CPPSearch is run only if CCP\_TEST is set.</span></span>
-   <span data-ttu-id="1fc77-171">CCPDialog se ejecuta solo si \_ se ha \_ establecido no se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1fc77-171">CCPDialog is run only if NOT\_CCP\_SUCCESS is set.</span></span>
-   <span data-ttu-id="1fc77-172">MaintenanceDialog se ejecuta solo si este producto ya está instalado y si no se trata de una instalación que se está reanudando después de suspenderse.</span><span class="sxs-lookup"><span data-stu-id="1fc77-172">MaintenanceDialog is run only if this product is already installed and if this is not an installation that is being resume after being suspended.</span></span>
-   <span data-ttu-id="1fc77-173">MyCustomAction se ejecuta solo si la expresión de la columna Condition es true.</span><span class="sxs-lookup"><span data-stu-id="1fc77-173">MyCustomAction is run only if the expression in the Condition column is True.</span></span> <span data-ttu-id="1fc77-174">La expresión $MyComponent > 2 hace referencia al estado de acción del componente denominado mi componente.</span><span class="sxs-lookup"><span data-stu-id="1fc77-174">The expression $MyComponent > 2 refers to the action state of the component called MyComponent.</span></span> <span data-ttu-id="1fc77-175">Esta condición indica que MyCustomAction solo debe ejecutarse si se ha establecido que el componente está instalado.</span><span class="sxs-lookup"><span data-stu-id="1fc77-175">This condition indicates that MyCustomAction should only be run if MyComponent is set to be installed.</span></span> <span data-ttu-id="1fc77-176">Para obtener más información sobre los Estados de acción y los Estados de selección, vea la propiedad [**FeatureRequestState**](session-featurerequeststate.md) , la [tabla de características](feature-table.md)y la [acción InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="1fc77-176">For more information on Action states and Selection states, see the [**FeatureRequestState**](session-featurerequeststate.md) property, the [Feature table](feature-table.md), and the [InstallFiles action](installfiles-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fc77-177">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1fc77-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fc77-178">Utilizar propiedades</span><span class="sxs-lookup"><span data-stu-id="1fc77-178">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="1fc77-179">Sintaxis de la instrucción condicional</span><span class="sxs-lookup"><span data-stu-id="1fc77-179">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> </dl>

 

 



