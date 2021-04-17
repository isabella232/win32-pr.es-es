---
description: ICE23 valida el orden de las pestañas de control de cada cuadro de diálogo.
ms.assetid: d425f8c6-4615-439d-8194-3a0325eb3cc3
title: ICE23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c1823a70e50d7dd3c42c2e90d6a2d0f11f2fa5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667759"
---
# <a name="ice23"></a><span data-ttu-id="d24b9-103">ICE23</span><span class="sxs-lookup"><span data-stu-id="d24b9-103">ICE23</span></span>

<span data-ttu-id="d24b9-104">ICE23 valida el orden de las pestañas de control de cada cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d24b9-104">ICE23 validates the control tab order for each dialog box.</span></span>

<span data-ttu-id="d24b9-105">ICE23 valida lo siguiente en la [tabla de cuadro de diálogo](dialog-table.md) y la tabla de [control](control-table.md):</span><span class="sxs-lookup"><span data-stu-id="d24b9-105">ICE23 validates the following in the [Dialog table](dialog-table.md) and [Control table](control-table.md):</span></span>

-   <span data-ttu-id="d24b9-106">Cada registro de la tabla de diálogo especifica un control en la \_ primera columna de control que existe en el cuadro de diálogo especificado por la columna de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d24b9-106">That every record in the Dialog table specifies a control in the Control\_First column that exists in the dialog box specified by the Dialog column.</span></span>
-   <span data-ttu-id="d24b9-107">Todos los registros de la tabla de control especifican un control en la \_ columna control siguiente que se encuentra en el mismo cuadro de diálogo que el control enumerado en la columna control, o \_ el control siguiente contiene el valor null.</span><span class="sxs-lookup"><span data-stu-id="d24b9-107">That every record in the Control table specifies a control in the Control\_Next column that is on the same dialog as the control listed in the Control column, or Control\_Next contains the Null value.</span></span>
-   <span data-ttu-id="d24b9-108">Que siguen las siguientes \_ entradas de control de control a control en la tabla de control, crea un bucle único, cerrado, que vuelve al control inicial.</span><span class="sxs-lookup"><span data-stu-id="d24b9-108">That following the Control\_Next entries from control to control in the Control table makes a single, closed, loop that comes back to the initial control.</span></span> <span data-ttu-id="d24b9-109">No todos los controles deben estar en el bucle, pero el bucle debe atravesar todos los controles que tengan una entrada en la columna de control \_ siguiente.</span><span class="sxs-lookup"><span data-stu-id="d24b9-109">Not every control needs to be in the loop, but the loop must pass through every control that has an entry in the Control\_Next column.</span></span>

## <a name="result"></a><span data-ttu-id="d24b9-110">Resultado</span><span class="sxs-lookup"><span data-stu-id="d24b9-110">Result</span></span>

<span data-ttu-id="d24b9-111">ICE23 envía un mensaje de error si el orden de tabulación de los controles no forma un bucle cerrado único en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d24b9-111">ICE23 posts an error message if the tab order of controls does not form a single closed loop in the dialog box.</span></span>

## <a name="example"></a><span data-ttu-id="d24b9-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d24b9-112">Example</span></span>

<span data-ttu-id="d24b9-113">ICE23 publicaría los siguientes mensajes de error para el ejemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="d24b9-113">ICE23 would post the following error messages for the example shown.</span></span>

-   <span data-ttu-id="d24b9-114">Dialog1 no tiene ningún control en \_ primer lugar.</span><span class="sxs-lookup"><span data-stu-id="d24b9-114">Dialog1 has no Control\_First.</span></span>
-   <span data-ttu-id="d24b9-115">Controlar el \_ primer cuadro de diálogo Dialog2 hace referencia a ControlX de control inexistente.</span><span class="sxs-lookup"><span data-stu-id="d24b9-115">Control\_First of dialog Dialog2 refers to nonexistent control ControlX.</span></span>
-   <span data-ttu-id="d24b9-116">Dialog3 tiene el orden de tabulación de inactividad en el control ControlB.</span><span class="sxs-lookup"><span data-stu-id="d24b9-116">Dialog3 has dead-end tab order at control ControlB.</span></span>
-   <span data-ttu-id="d24b9-117">Dialog4 tiene un orden de tabulación incorrecto en el control ControlC</span><span class="sxs-lookup"><span data-stu-id="d24b9-117">Dialog4 has malformed tab order at control ControlC</span></span>
-   <span data-ttu-id="d24b9-118">Dialog5 tiene un orden de tabulación incorrecto en el control ControlC.</span><span class="sxs-lookup"><span data-stu-id="d24b9-118">Dialog5 has malformed tab order at control ControlC.</span></span>
-   <span data-ttu-id="d24b9-119">Control \_ siguiente del control Dialog6. ControlC vínculos a un control desconocido.</span><span class="sxs-lookup"><span data-stu-id="d24b9-119">Control\_Next of control Dialog6.ControlC links to unknown control.</span></span>

<span data-ttu-id="d24b9-120">[Tabla de cuadro de diálogo](dialog-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="d24b9-120">[Dialog Table](dialog-table.md) (partial)</span></span>



| <span data-ttu-id="d24b9-121">Diálogo</span><span class="sxs-lookup"><span data-stu-id="d24b9-121">Dialog</span></span>  | <span data-ttu-id="d24b9-122">Controlar \_ primero</span><span class="sxs-lookup"><span data-stu-id="d24b9-122">Control\_First</span></span> |
|---------|----------------|
| <span data-ttu-id="d24b9-123">Dialog1</span><span class="sxs-lookup"><span data-stu-id="d24b9-123">Dialog1</span></span> |                |
| <span data-ttu-id="d24b9-124">Dialog2</span><span class="sxs-lookup"><span data-stu-id="d24b9-124">Dialog2</span></span> | <span data-ttu-id="d24b9-125">ControlX</span><span class="sxs-lookup"><span data-stu-id="d24b9-125">ControlX</span></span>       |
| <span data-ttu-id="d24b9-126">Dialog3</span><span class="sxs-lookup"><span data-stu-id="d24b9-126">Dialog3</span></span> | <span data-ttu-id="d24b9-127">ControlA</span><span class="sxs-lookup"><span data-stu-id="d24b9-127">ControlA</span></span>       |
| <span data-ttu-id="d24b9-128">Dialog4</span><span class="sxs-lookup"><span data-stu-id="d24b9-128">Dialog4</span></span> | <span data-ttu-id="d24b9-129">ControlA</span><span class="sxs-lookup"><span data-stu-id="d24b9-129">ControlA</span></span>       |
| <span data-ttu-id="d24b9-130">Dialog5</span><span class="sxs-lookup"><span data-stu-id="d24b9-130">Dialog5</span></span> | <span data-ttu-id="d24b9-131">ControlA</span><span class="sxs-lookup"><span data-stu-id="d24b9-131">ControlA</span></span>       |



 

<span data-ttu-id="d24b9-132">[Tabla de control](control-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="d24b9-132">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="d24b9-133">Diálogo</span><span class="sxs-lookup"><span data-stu-id="d24b9-133">Dialog</span></span>  | <span data-ttu-id="d24b9-134">Control</span><span class="sxs-lookup"><span data-stu-id="d24b9-134">Control</span></span>  | <span data-ttu-id="d24b9-135">Control \_ siguiente</span><span class="sxs-lookup"><span data-stu-id="d24b9-135">Control\_Next</span></span> |
|---------|----------|---------------|
| <span data-ttu-id="d24b9-136">Dialog1</span><span class="sxs-lookup"><span data-stu-id="d24b9-136">Dialog1</span></span> | <span data-ttu-id="d24b9-137">ControlA</span><span class="sxs-lookup"><span data-stu-id="d24b9-137">ControlA</span></span> |               |
| <span data-ttu-id="d24b9-138">Dialog1</span><span class="sxs-lookup"><span data-stu-id="d24b9-138">Dialog1</span></span> | <span data-ttu-id="d24b9-139">ControlB</span><span class="sxs-lookup"><span data-stu-id="d24b9-139">ControlB</span></span> | <span data-ttu-id="d24b9-140">ControlA</span><span class="sxs-lookup"><span data-stu-id="d24b9-140">ControlA</span></span>      |
| <span data-ttu-id="d24b9-141">Dialog2</span><span class="sxs-lookup"><span data-stu-id="d24b9-141">Dialog2</span></span> | <span data-ttu-id="d24b9-142">ControlA</span><span class="sxs-lookup"><span data-stu-id="d24b9-142">ControlA</span></span> | <span data-ttu-id="d24b9-143">ControlB</span><span class="sxs-lookup"><span data-stu-id="d24b9-143">ControlB</span></span>      |
| <span data-ttu-id="d24b9-144">Dialog2</span><span class="sxs-lookup"><span data-stu-id="d24b9-144">Dialog2</span></span> | <span data-ttu-id="d24b9-145">ControlB</span><span class="sxs-lookup"><span data-stu-id="d24b9-145">ControlB</span></span> | <span data-ttu-id="d24b9-146">ControlA</span><span class="sxs-lookup"><span data-stu-id="d24b9-146">ControlA</span></span>      |
| <span data-ttu-id="d24b9-147">Dialog3</span><span class="sxs-lookup"><span data-stu-id="d24b9-147">Dialog3</span></span> | <span data-ttu-id="d24b9-148">ControlA</span><span class="sxs-lookup"><span data-stu-id="d24b9-148">ControlA</span></span> | <span data-ttu-id="d24b9-149">ControlB</span><span class="sxs-lookup"><span data-stu-id="d24b9-149">ControlB</span></span>      |
| <span data-ttu-id="d24b9-150">Dialog3</span><span class="sxs-lookup"><span data-stu-id="d24b9-150">Dialog3</span></span> | <span data-ttu-id="d24b9-151">ControlB</span><span class="sxs-lookup"><span data-stu-id="d24b9-151">ControlB</span></span> |               |
| <span data-ttu-id="d24b9-152">Dialog4</span><span class="sxs-lookup"><span data-stu-id="d24b9-152">Dialog4</span></span> | <span data-ttu-id="d24b9-153">ControlA</span><span class="sxs-lookup"><span data-stu-id="d24b9-153">ControlA</span></span> | <span data-ttu-id="d24b9-154">ControlB</span><span class="sxs-lookup"><span data-stu-id="d24b9-154">ControlB</span></span>      |
| <span data-ttu-id="d24b9-155">Dialog4</span><span class="sxs-lookup"><span data-stu-id="d24b9-155">Dialog4</span></span> | <span data-ttu-id="d24b9-156">ControlB</span><span class="sxs-lookup"><span data-stu-id="d24b9-156">ControlB</span></span> | <span data-ttu-id="d24b9-157">ControlC</span><span class="sxs-lookup"><span data-stu-id="d24b9-157">ControlC</span></span>      |
| <span data-ttu-id="d24b9-158">Dialog4</span><span class="sxs-lookup"><span data-stu-id="d24b9-158">Dialog4</span></span> | <span data-ttu-id="d24b9-159">ControlC</span><span class="sxs-lookup"><span data-stu-id="d24b9-159">ControlC</span></span> | <span data-ttu-id="d24b9-160">ControlB</span><span class="sxs-lookup"><span data-stu-id="d24b9-160">ControlB</span></span>      |
| <span data-ttu-id="d24b9-161">Dialog5</span><span class="sxs-lookup"><span data-stu-id="d24b9-161">Dialog5</span></span> | <span data-ttu-id="d24b9-162">ControlA</span><span class="sxs-lookup"><span data-stu-id="d24b9-162">ControlA</span></span> | <span data-ttu-id="d24b9-163">ControlB</span><span class="sxs-lookup"><span data-stu-id="d24b9-163">ControlB</span></span>      |
| <span data-ttu-id="d24b9-164">Dialog5</span><span class="sxs-lookup"><span data-stu-id="d24b9-164">Dialog5</span></span> | <span data-ttu-id="d24b9-165">ControlB</span><span class="sxs-lookup"><span data-stu-id="d24b9-165">ControlB</span></span> | <span data-ttu-id="d24b9-166">ControlC</span><span class="sxs-lookup"><span data-stu-id="d24b9-166">ControlC</span></span>      |
| <span data-ttu-id="d24b9-167">Dialog5</span><span class="sxs-lookup"><span data-stu-id="d24b9-167">Dialog5</span></span> | <span data-ttu-id="d24b9-168">ControlC</span><span class="sxs-lookup"><span data-stu-id="d24b9-168">ControlC</span></span> | <span data-ttu-id="d24b9-169">ControlA</span><span class="sxs-lookup"><span data-stu-id="d24b9-169">ControlA</span></span>      |
| <span data-ttu-id="d24b9-170">Dialog5</span><span class="sxs-lookup"><span data-stu-id="d24b9-170">Dialog5</span></span> | <span data-ttu-id="d24b9-171">Controled</span><span class="sxs-lookup"><span data-stu-id="d24b9-171">ControlD</span></span> | <span data-ttu-id="d24b9-172">ControlA</span><span class="sxs-lookup"><span data-stu-id="d24b9-172">ControlA</span></span>      |
| <span data-ttu-id="d24b9-173">Dialog6</span><span class="sxs-lookup"><span data-stu-id="d24b9-173">Dialog6</span></span> | <span data-ttu-id="d24b9-174">ControlA</span><span class="sxs-lookup"><span data-stu-id="d24b9-174">ControlA</span></span> | <span data-ttu-id="d24b9-175">ControlB</span><span class="sxs-lookup"><span data-stu-id="d24b9-175">ControlB</span></span>      |
| <span data-ttu-id="d24b9-176">Dialog6</span><span class="sxs-lookup"><span data-stu-id="d24b9-176">Dialog6</span></span> | <span data-ttu-id="d24b9-177">ControlB</span><span class="sxs-lookup"><span data-stu-id="d24b9-177">ControlB</span></span> | <span data-ttu-id="d24b9-178">ControlC</span><span class="sxs-lookup"><span data-stu-id="d24b9-178">ControlC</span></span>      |
| <span data-ttu-id="d24b9-179">Dialog6</span><span class="sxs-lookup"><span data-stu-id="d24b9-179">Dialog6</span></span> | <span data-ttu-id="d24b9-180">ControlC</span><span class="sxs-lookup"><span data-stu-id="d24b9-180">ControlC</span></span> | <span data-ttu-id="d24b9-181">ControlX</span><span class="sxs-lookup"><span data-stu-id="d24b9-181">ControlX</span></span>      |
| <span data-ttu-id="d24b9-182">Dialog6</span><span class="sxs-lookup"><span data-stu-id="d24b9-182">Dialog6</span></span> | <span data-ttu-id="d24b9-183">Controled</span><span class="sxs-lookup"><span data-stu-id="d24b9-183">ControlD</span></span> | <span data-ttu-id="d24b9-184">ControlA</span><span class="sxs-lookup"><span data-stu-id="d24b9-184">ControlA</span></span>      |



 

<span data-ttu-id="d24b9-185">Para corregir estos errores, tenga en cuenta lo siguiente en las tablas anteriores y realice los cambios indicados.</span><span class="sxs-lookup"><span data-stu-id="d24b9-185">To fix these errors note the following in the above tables and make the indicated changes.</span></span>

<span data-ttu-id="d24b9-186">No todas las filas de la tabla del cuadro de diálogo tienen un control especificado en la \_ primera columna del control.</span><span class="sxs-lookup"><span data-stu-id="d24b9-186">Not every row in the Dialog table has a control specified in the Control\_First column.</span></span> <span data-ttu-id="d24b9-187">Cambie la \_ primera columna control del registro Dialog1 de la tabla del cuadro de diálogo a un control que exista en Dialog1.</span><span class="sxs-lookup"><span data-stu-id="d24b9-187">Change the Control\_First column of the Dialog1 record in the Dialog table to a control that exists in Dialog1.</span></span>

<span data-ttu-id="d24b9-188">No todas las filas de la tabla de cuadro de diálogo tienen un control especificado en la \_ primera columna de control que existe en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d24b9-188">Not every row in the Dialog table has a control specified in the Control\_First column that exists on the dialog box.</span></span> <span data-ttu-id="d24b9-189">Cambie la \_ primera columna de control de Dialog2 a un control que exista en Dialog2.</span><span class="sxs-lookup"><span data-stu-id="d24b9-189">Change the Control\_First column of the Dialog2 to a control that exists in Dialog2.</span></span>

<span data-ttu-id="d24b9-190">Las siguientes entradas de control \_ de la tabla de control de control a control no crean un bucle cerrado en todos los casos.</span><span class="sxs-lookup"><span data-stu-id="d24b9-190">Following the Control\_Next entries in the Control table from control to control does not make a closed loop in every case.</span></span> <span data-ttu-id="d24b9-191">Cambie la columna de control \_ siguiente para ControlB en Dialog3 a controla.</span><span class="sxs-lookup"><span data-stu-id="d24b9-191">Change the Control\_Next column for ControlB in Dialog3 to ControlA.</span></span>

<span data-ttu-id="d24b9-192">Las siguientes entradas de control \_ de la tabla de control de control a control no vuelven al control inicial en todos los casos.</span><span class="sxs-lookup"><span data-stu-id="d24b9-192">Following the Control\_Next entries in the Control table from control to control does not lead back to the initial control in every case.</span></span> <span data-ttu-id="d24b9-193">Cambie la \_ columna de control siguiente para ControlC en Dialog4 para que haga referencia a controla.</span><span class="sxs-lookup"><span data-stu-id="d24b9-193">Change the Control\_Next column for ControlC in Dialog4 to refer to ControlA.</span></span>

<span data-ttu-id="d24b9-194">Las siguientes entradas de control de \_ la tabla de control de control a control no atraviesan todos los controles del cuadro de diálogo que tengan una entrada en la columna de control \_ siguiente.</span><span class="sxs-lookup"><span data-stu-id="d24b9-194">Following the Control\_Next entries in the Control table from control to control does not pass through every control in the dialog box having an entry in the Control\_Next column.</span></span> <span data-ttu-id="d24b9-195">Cambie la columna de control \_ siguiente para ControlC en Dialog5 a controled.</span><span class="sxs-lookup"><span data-stu-id="d24b9-195">Change the Control\_Next column for ControlC in Dialog5 to ControlD.</span></span>

<span data-ttu-id="d24b9-196">El control Next no hace \_ referencia a un control válido que esté en el mismo cuadro de diálogo que el control que aparece en la columna de control.</span><span class="sxs-lookup"><span data-stu-id="d24b9-196">Control\_Next does not refer to a valid control that is in the same dialog as the control listed in the Control column.</span></span> <span data-ttu-id="d24b9-197">Cambie la \_ columna de control siguiente para ControlC en Dialog6 para que haga referencia a controled.</span><span class="sxs-lookup"><span data-stu-id="d24b9-197">Change the Control\_Next column for ControlC in Dialog6 to refer to ControlD.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d24b9-198">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d24b9-198">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d24b9-199">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="d24b9-199">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



