---
title: Rutinas de comprobación
description: En esta sección se describen las rutinas de comprobación que puede ejecutar el comprobador de accesibilidad de la interfaz de usuario para probar la implementación de accesibilidad de una aplicación.
ms.assetid: 0ff38f83-5741-4c0e-a070-a8385f95eba3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78eea821a4c918078c6390e33fa7046de1452f76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357157"
---
# <a name="verification-routines"></a><span data-ttu-id="de4cb-103">Rutinas de comprobación</span><span class="sxs-lookup"><span data-stu-id="de4cb-103">Verification Routines</span></span>

<span data-ttu-id="de4cb-104">En esta sección se describen las rutinas de comprobación que puede ejecutar el comprobador de accesibilidad de la interfaz de usuario para probar la implementación de accesibilidad de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="de4cb-104">This section describes the verification routines that UI Accessibility Checker can run to test an application's accessibility implementation.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="de4cb-105">Category</span><span class="sxs-lookup"><span data-stu-id="de4cb-105">Category</span></span></th>
<th><span data-ttu-id="de4cb-106">Rutina</span><span class="sxs-lookup"><span data-stu-id="de4cb-106">Routine</span></span></th>
<th><span data-ttu-id="de4cb-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="de4cb-107">Description</span></span></th>
</tr><span data-ttu-id="de4cb-108">
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><strong>Coherencia</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="de4cb-108">
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><strong>Consistency</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="de4cb-109"><strong>ScreenReader</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-109"><strong>ScreenReader</strong></span></span></td>
<td><span data-ttu-id="de4cb-110">Compila todos los elementos visibles en el destino de comprobación y los muestra en un control ListView en el orden en que un lector de pantalla estándar los anuncia a un usuario.</span><span class="sxs-lookup"><span data-stu-id="de4cb-110">Compiles all visible elements in the verification target and displays them in a ListView control in the order that a standard screen reader announces them to a user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de4cb-111"><strong>UiaScreenReader</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-111"><strong>UiaScreenReader</strong></span></span></td>
<td><span data-ttu-id="de4cb-112">Igual que <strong>ScreenReader</strong>, pero para implementaciones de UIA.</span><span class="sxs-lookup"><span data-stu-id="de4cb-112">Same as <strong>ScreenReader</strong>, but for UIA implementations.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="de4cb-113"><strong>Navegación</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="de4cb-113"><strong>Navigation</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="de4cb-114"><strong>CheckTreeDepth</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-114"><strong>CheckTreeDepth</strong></span></span></td>
<td><span data-ttu-id="de4cb-115">Envía caracteres de tabulación (o Mayús + Tab) como entrada al destino de comprobación para confirmar que la interfaz de usuario del destino no es demasiado compleja o inaccesible mediante la navegación de teclado estándar.</span><span class="sxs-lookup"><span data-stu-id="de4cb-115">Sends Tab (or Shift+Tab) characters as input to the verification target to confirm that the target's UI isn't overly complex or inaccessible using standard keyboard navigation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de4cb-116"><strong>CheckTabbingUia</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-116"><strong>CheckTabbingUia</strong></span></span></td>
<td><span data-ttu-id="de4cb-117">Envía caracteres de tabulación (o Mayús + Tab) como entrada al destino de comprobación para confirmar que todos los elementos que pueden recibir el foco en la interfaz de usuario son accesibles de forma ordenada y lógica mediante la navegación de teclado estándar.</span><span class="sxs-lookup"><span data-stu-id="de4cb-117">Sends Tab (or Shift+Tab) characters as input to the verification target to confirm that all focusable elements in the UI are reachable in an orderly, logical fashion using standard keyboard navigation.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="5"><span data-ttu-id="de4cb-118"><strong>Propiedades</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="de4cb-118"><strong>Properties</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="de4cb-119"><strong>CheckRole</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-119"><strong>CheckRole</strong></span></span></td>
<td><span data-ttu-id="de4cb-120">Confirma que cada elemento que tiene el foco en la interfaz de usuario notifica un rol de MSAA lógico y válido, y que el control tiene un valor según sea necesario para ese rol.</span><span class="sxs-lookup"><span data-stu-id="de4cb-120">Confirms that each focusable element in the UI reports a valid, logical MSAA role, and that the control has a value as required by that role.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de4cb-121"><strong>CheckState</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-121"><strong>CheckState</strong></span></span></td>
<td><span data-ttu-id="de4cb-122">Confirma que cada elemento que tiene el foco en la interfaz de usuario informa de un estado de MSAA lógico y válido.</span><span class="sxs-lookup"><span data-stu-id="de4cb-122">Confirms that each focusable element in the UI reports a valid, logical MSAA state.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="de4cb-123"><strong>CheckName</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-123"><strong>CheckName</strong></span></span></td>
<td><span data-ttu-id="de4cb-124">Confirma que cada elemento enfocable de la interfaz de usuario informa de un nombre de MSAA lógico y válido.</span><span class="sxs-lookup"><span data-stu-id="de4cb-124">Confirms that each focusable element in the UI reports a valid, logical MSAA name.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="de4cb-125"><strong>CheckAccessKeys</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-125"><strong>CheckAccessKeys</strong></span></span></td>
<td><span data-ttu-id="de4cb-126">Confirma que las claves de acceso que se asignan a los elementos del destino de comprobación son únicas en el destino de la comprobación.</span><span class="sxs-lookup"><span data-stu-id="de4cb-126">Confirms that access keys that are assigned to elements in the verification target are unique within the verification target.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="de4cb-127"><strong>CheckBoundingRect</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-127"><strong>CheckBoundingRect</strong></span></span></td>
<td><span data-ttu-id="de4cb-128">Confirma que cada elemento enfocable de la interfaz de usuario tiene un rectángulo delimitador que se puede usar como destino para la prueba de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="de4cb-128">Confirms that each focusable element in the UI has a bounding rectangle that can be used as a target for hit testing.</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="de4cb-129"><strong>Árbol</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="de4cb-129"><strong>Tree</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="de4cb-130"><strong>CheckParentChild</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-130"><strong>CheckParentChild</strong></span></span></td>
<td><span data-ttu-id="de4cb-131">Las relaciones primarias y secundarias en el árbol de elementos son coherentes y predecibles.</span><span class="sxs-lookup"><span data-stu-id="de4cb-131">Parent and child relationships in the element tree are consistent and predictable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de4cb-132"><strong>CheckOrphanChildren</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-132"><strong>CheckOrphanChildren</strong></span></span></td>
<td><span data-ttu-id="de4cb-133">Confirma que cada elemento que tiene el foco en la interfaz de usuario informa de un elemento primario de MSAA válido.</span><span class="sxs-lookup"><span data-stu-id="de4cb-133">Confirms that each focusable element in the UI reports a valid MSAA parent.</span></span></td>

</tr>
<tr class="even">
<td rowspan="6"><span data-ttu-id="de4cb-134"><strong>Propiedades de UIA</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="de4cb-134"><strong>UIA Properties</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="de4cb-135"><strong>CheckNameUIA</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-135"><strong>CheckNameUIA</strong></span></span></td>
<td><span data-ttu-id="de4cb-136">Confirma que cada elemento enfocable de la interfaz de usuario informa de un nombre válido de UIA lógico.</span><span class="sxs-lookup"><span data-stu-id="de4cb-136">Confirms that each focusable element in the UI reports a valid, logical UIA name.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de4cb-137"><strong>CheckTreeDepthUIA</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-137"><strong>CheckTreeDepthUIA</strong></span></span></td>
<td><span data-ttu-id="de4cb-138">Envía caracteres de tabulación (o Mayús + Tab) como entrada al destino de comprobación para confirmar que los elementos de UIA en la interfaz de usuario de destino no son demasiado complejos o inaccesibles mediante la navegación de teclado estándar.</span><span class="sxs-lookup"><span data-stu-id="de4cb-138">Sends Tab (or Shift+Tab) characters as input to the verification target to confirm that to UIA elements in the target's UI aren't overly complex or inaccessible using standard keyboard navigation.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="de4cb-139"><strong>CheckStateUIA</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-139"><strong>CheckStateUIA</strong></span></span></td>
<td><span data-ttu-id="de4cb-140">Confirma que cada elemento enfocable de la interfaz de usuario informa de un estado válido y lógico de UIA.</span><span class="sxs-lookup"><span data-stu-id="de4cb-140">Confirms that each focusable element in the UI reports a valid, logical UIA state.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="de4cb-141"><strong>CheckAccessKeysUIA</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-141"><strong>CheckAccessKeysUIA</strong></span></span></td>
<td><span data-ttu-id="de4cb-142">Confirma que los elementos relacionados no tienen el mismo acceso o la misma tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="de4cb-142">Confirms that sibling elements do not have the same access and/or accelerator key.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="de4cb-143"><strong>CheckBoundingRectUIA</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-143"><strong>CheckBoundingRectUIA</strong></span></span></td>
<td><span data-ttu-id="de4cb-144">Confirma que cada elemento de UIA enfocable en la interfaz de usuario tiene un rectángulo delimitador que se puede usar como destino para la prueba de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="de4cb-144">Confirms that each focusable UIA element in the UI has a bounding rectangle that can be used as a target for hit testing.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="de4cb-145"><strong>CheckControlTypeUIA</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-145"><strong>CheckControlTypeUIA</strong></span></span></td>
<td><span data-ttu-id="de4cb-146">Confirma que cada elemento que tiene el foco en la interfaz de usuario informa de un tipo de control de UIA lógico y válido.</span><span class="sxs-lookup"><span data-stu-id="de4cb-146">Confirms that each focusable element in the UI reports a valid, logical UIA control type.</span></span></td>

</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="de4cb-147"><strong>Árbol de UIA</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="de4cb-147"><strong>UIA Tree</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="de4cb-148"><strong>CheckNavigateUia</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-148"><strong>CheckNavigateUia</strong></span></span></td>
<td><span data-ttu-id="de4cb-149">Confirma que el TreeWalker de UIA puede navegar por los elementos secundarios de un elemento.</span><span class="sxs-lookup"><span data-stu-id="de4cb-149">Confirms that the UIA TreeWalker can navigate through an element's children.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de4cb-150"><strong>CheckOrphanChildrenUia</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-150"><strong>CheckOrphanChildrenUia</strong></span></span></td>
<td><span data-ttu-id="de4cb-151">Confirma que cada elemento que tiene el foco en la interfaz de usuario informa de un elemento primario de UIA válido.</span><span class="sxs-lookup"><span data-stu-id="de4cb-151">Confirms that each focusable element in the UI reports a valid UIA parent.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="de4cb-152"><strong>CheckSiblingsUia</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-152"><strong>CheckSiblingsUia</strong></span></span></td>
<td><span data-ttu-id="de4cb-153">Confirma que los elementos del mismo nivel no tienen el mismo nombre: pares ControlType, ni el mismo elemento AutomationId.</span><span class="sxs-lookup"><span data-stu-id="de4cb-153">Confirms that sibling elements do not have the same Name:ControlType pairs, nor the same AutomationId's.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="de4cb-154">$ {ROWSPAN9} $<strong>Aria web verificaciones</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="de4cb-154">${ROWSPAN9}$<strong>ARIA Web Verifications</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="de4cb-155"><strong>CheckARIARole</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-155"><strong>CheckARIARole</strong></span></span></td>
<td><span data-ttu-id="de4cb-156">Confirma que todos los elementos tienen un rol de ARIA válido.</span><span class="sxs-lookup"><span data-stu-id="de4cb-156">Confirms that all elements have a valid ARIA role.</span></span> <span data-ttu-id="de4cb-157">La etiqueta HTML y el rol ARIA asociados son elementos de información con roles no válidos marcados como errores.</span><span class="sxs-lookup"><span data-stu-id="de4cb-157">The associated HTML tag and ARIA role are information elements with invalid roles flagged as errors.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de4cb-158"><strong>CheckLabel</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-158"><strong>CheckLabel</strong></span></span></td>
<td><span data-ttu-id="de4cb-159">Confirma que cada elemento con la entrada, el botón, el botón de imagen o el rol de punto de referencia tiene una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="de4cb-159">Confirms each element with input, button, image-button, or landmark role has a label.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="de4cb-160"><strong>CheckRangeControls</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-160"><strong>CheckRangeControls</strong></span></span></td>
<td><span data-ttu-id="de4cb-161">Confirma que los controles de intervalo con el control deslizante o el rol de barra de progreso tienen definidos los atributos ARIA adecuados.</span><span class="sxs-lookup"><span data-stu-id="de4cb-161">Confirms range controls with slider or progress bar role have proper ARIA attributes defined.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="de4cb-162"><strong>CheckContainerRole</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-162"><strong>CheckContainerRole</strong></span></span></td>
<td><span data-ttu-id="de4cb-163">Confirma un elemento, o al menos uno de sus elementos secundarios, y ha definido onkeydown/onkeypress.</span><span class="sxs-lookup"><span data-stu-id="de4cb-163">Confirms an element, or at least one of its children, has onkeydown/onkeypress defined.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="de4cb-164"><strong>CheckLayoutTable</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-164"><strong>CheckLayoutTable</strong></span></span></td>
<td><span data-ttu-id="de4cb-165">Confirma que un diseño de tabla tiene una Summary/TH/Aria-describedby incluida.</span><span class="sxs-lookup"><span data-stu-id="de4cb-165">Confirms a table layout has a summary/th/aria-describedby included.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="de4cb-166"><strong>CheckGridStructure</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-166"><strong>CheckGridStructure</strong></span></span></td>
<td><span data-ttu-id="de4cb-167">Confirma que un elemento que no es de tabla con el rol de cuadrícula tiene una estructura de cuadrícula>fila>gridcell con atributos asociados.</span><span class="sxs-lookup"><span data-stu-id="de4cb-167">Confirms a non-table element with grid role has a structure of grid>row>gridcell with associated attributes.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="de4cb-168"><strong>CheckDataTable</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-168"><strong>CheckDataTable</strong></span></span></td>
<td><span data-ttu-id="de4cb-169">Confirma las propiedades de las tablas de datos.</span><span class="sxs-lookup"><span data-stu-id="de4cb-169">Confirms the properties of data tables.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="de4cb-170"><strong>CheckActiveDescendants</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-170"><strong>CheckActiveDescendants</strong></span></span></td>
<td><span data-ttu-id="de4cb-171">Confirma las propiedades de los elementos con un descendiente activo definido.</span><span class="sxs-lookup"><span data-stu-id="de4cb-171">Confirms the properties of elements with an active descendant defined.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="de4cb-172"><strong>CheckElementsWithClickHandler</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-172"><strong>CheckElementsWithClickHandler</strong></span></span></td>
<td><span data-ttu-id="de4cb-173">Confirma el índice de tabulación de los elementos con controladores de clic.</span><span class="sxs-lookup"><span data-stu-id="de4cb-173">Confirms the tab index of elements with click handlers.</span></span></td>

</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="de4cb-174"><strong>Comprobaciones web</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="de4cb-174"><strong>Web Verifications</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="de4cb-175"><strong>CheckHtml (Web)</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-175"><strong>CheckHtml (Web)</strong></span></span></td>
<td><span data-ttu-id="de4cb-176">Confirma varias características HTML como encabezados, nombre, marcos y títulos.</span><span class="sxs-lookup"><span data-stu-id="de4cb-176">Confirms various HTML characteristics such as headers, name, frames, and titles.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de4cb-177"><strong>CheckName (Web)</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-177"><strong>CheckName (Web)</strong></span></span></td>
<td><span data-ttu-id="de4cb-178">Confirma características de nombre como la longitud, los caracteres no válidos y la inclusión de roles.</span><span class="sxs-lookup"><span data-stu-id="de4cb-178">Confirms name characteristics such as length, invalid characters, and role inclusion.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="de4cb-179"><strong>CheckRole (Web)</strong></span><span class="sxs-lookup"><span data-stu-id="de4cb-179"><strong>CheckRole (Web)</strong></span></span></td>
<td><span data-ttu-id="de4cb-180">Confirma roles no válidos, roles que deben tener valores y/o roles no implementados.</span><span class="sxs-lookup"><span data-stu-id="de4cb-180">Confirms invalid roles, roles that should have values, and/or roles not implemented.</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="de4cb-181">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="de4cb-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de4cb-182">UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="de4cb-182">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




