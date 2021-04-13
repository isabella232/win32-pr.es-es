---
description: Para obtener información sobre los atributos de control, vea el vínculo al control concreto que necesita crear en los controles, así como los vínculos a atributos de control concretos en las listas siguientes.
ms.assetid: 948ce3d3-e463-40de-8b5f-21ef18b1a0ce
title: Atributos de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d026e84dadefa67ce9d6e00146c6e1c2017cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361157"
---
# <a name="control-attributes"></a><span data-ttu-id="3f248-103">Atributos de control</span><span class="sxs-lookup"><span data-stu-id="3f248-103">Control Attributes</span></span>

<span data-ttu-id="3f248-104">Para obtener información sobre los atributos de control, vea el vínculo al control concreto que necesita crear en los [controles](controls.md) , así como los vínculos a atributos de control concretos en las listas siguientes.</span><span class="sxs-lookup"><span data-stu-id="3f248-104">For information on control attributes, see the link to the particular control that you need to create in [Controls](controls.md) as well as the links to particular control attributes in the following lists.</span></span>

<span data-ttu-id="3f248-105">Los métodos siguientes se utilizan para especificar los atributos de un control:</span><span class="sxs-lookup"><span data-stu-id="3f248-105">The following methods are used for specifying the attributes of a control:</span></span>

-   <span data-ttu-id="3f248-106">Use la [tabla ControlCondition](controlcondition-table.md) para deshabilitar, habilitar, ocultar o mostrar un control según el valor de una propiedad o una instrucción condicional.</span><span class="sxs-lookup"><span data-stu-id="3f248-106">Use the [ControlCondition table](controlcondition-table.md) to disable, enable, hide, or show a control according to the value of a property or conditional statement.</span></span> <span data-ttu-id="3f248-107">También puede usar esta tabla para reemplazar el control predeterminado especificado en la [tabla del cuadro de diálogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="3f248-107">You can also use this table to override the default control specified in the [Dialog table](dialog-table.md).</span></span>
-   <span data-ttu-id="3f248-108">Suscríbase el control a un ControlEvent, en la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="3f248-108">Subscribe the control to a ControlEvent in the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="3f248-109">Escriba el identificador del atributo en la columna Attribute y el identificador de ControlEvent, en la columna Event de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="3f248-109">Enter the attribute's identifier in the Attribute column and the ControlEvent's identifier in the Event column of this table.</span></span>
-   <span data-ttu-id="3f248-110">Establezca las marcas de bits del atributo de control para el control en la columna atributo de la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="3f248-110">Set the control attribute bit flags for the control in the Attribute column of the [Control table](control-table.md).</span></span> <span data-ttu-id="3f248-111">Esto establece los atributos tras la creación del control.</span><span class="sxs-lookup"><span data-stu-id="3f248-111">This sets the attributes upon the creation of the control.</span></span>

<span data-ttu-id="3f248-112">Algunos atributos no se pueden establecer para cada control o se pueden especificar mediante todos los métodos anteriores.</span><span class="sxs-lookup"><span data-stu-id="3f248-112">Some attributes cannot be set for every control or be specified by all of the above methods.</span></span> <span data-ttu-id="3f248-113">Vea los temas de control y atributo en particular para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="3f248-113">See the particular control and attribute topics for details.</span></span>

<span data-ttu-id="3f248-114">Los valores iniciales de algunos atributos de control se pueden establecer con bits en la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="3f248-114">The initial values of some control attributes can be set with bits in the [Control table](control-table.md).</span></span>



| <span data-ttu-id="3f248-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="3f248-115">Attribute</span></span>                                          | <span data-ttu-id="3f248-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="3f248-116">Decimal</span></span> | <span data-ttu-id="3f248-117">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="3f248-117">Hexadecimal</span></span> | <span data-ttu-id="3f248-118">Constante</span><span class="sxs-lookup"><span data-stu-id="3f248-118">Constant</span></span>                               |
|----------------------------------------------------|---------|-------------|----------------------------------------|
| [<span data-ttu-id="3f248-119">Lenguas</span><span class="sxs-lookup"><span data-stu-id="3f248-119">BiDi</span></span>](bidi-control-attribute.md)                 | <span data-ttu-id="3f248-120">224</span><span class="sxs-lookup"><span data-stu-id="3f248-120">224</span></span>     | <span data-ttu-id="3f248-121">0x000000E0</span><span class="sxs-lookup"><span data-stu-id="3f248-121">0x000000E0</span></span>  | <span data-ttu-id="3f248-122">**msidbControlAttributesBiDi**</span><span class="sxs-lookup"><span data-stu-id="3f248-122">**msidbControlAttributesBiDi**</span></span>         |
| [<span data-ttu-id="3f248-123">Enabled</span><span class="sxs-lookup"><span data-stu-id="3f248-123">Enabled</span></span>](enabled-control-attribute.md)           | <span data-ttu-id="3f248-124">2</span><span class="sxs-lookup"><span data-stu-id="3f248-124">2</span></span>       | <span data-ttu-id="3f248-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3f248-125">0x00000002</span></span>  | <span data-ttu-id="3f248-126">**msidbControlAttributesEnabled**</span><span class="sxs-lookup"><span data-stu-id="3f248-126">**msidbControlAttributesEnabled**</span></span>      |
| [<span data-ttu-id="3f248-127">Indirecto</span><span class="sxs-lookup"><span data-stu-id="3f248-127">Indirect</span></span>](indirect-control-attribute.md)         | <span data-ttu-id="3f248-128">8</span><span class="sxs-lookup"><span data-stu-id="3f248-128">8</span></span>       | <span data-ttu-id="3f248-129">0x00000008</span><span class="sxs-lookup"><span data-stu-id="3f248-129">0x00000008</span></span>  | <span data-ttu-id="3f248-130">**msidbControlAttributesIndirect**</span><span class="sxs-lookup"><span data-stu-id="3f248-130">**msidbControlAttributesIndirect**</span></span>     |
| [<span data-ttu-id="3f248-131">Control de entero</span><span class="sxs-lookup"><span data-stu-id="3f248-131">Integer Control</span></span>](integer-control-attribute.md)   | <span data-ttu-id="3f248-132">16</span><span class="sxs-lookup"><span data-stu-id="3f248-132">16</span></span>      | <span data-ttu-id="3f248-133">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f248-133">0x00000010</span></span>  | <span data-ttu-id="3f248-134">**msidbControlAttributesInteger**</span><span class="sxs-lookup"><span data-stu-id="3f248-134">**msidbControlAttributesInteger**</span></span>      |
| [<span data-ttu-id="3f248-135">LeftScroll</span><span class="sxs-lookup"><span data-stu-id="3f248-135">LeftScroll</span></span>](leftscroll-control-attribute.md)     | <span data-ttu-id="3f248-136">128</span><span class="sxs-lookup"><span data-stu-id="3f248-136">128</span></span>     | <span data-ttu-id="3f248-137">0x00000080</span><span class="sxs-lookup"><span data-stu-id="3f248-137">0x00000080</span></span>  | <span data-ttu-id="3f248-138">**msidbControlAttributesLeftScroll**</span><span class="sxs-lookup"><span data-stu-id="3f248-138">**msidbControlAttributesLeftScroll**</span></span>   |
| [<span data-ttu-id="3f248-139">RightAligned</span><span class="sxs-lookup"><span data-stu-id="3f248-139">RightAligned</span></span>](rightaligned-control-attribute.md) | <span data-ttu-id="3f248-140">64</span><span class="sxs-lookup"><span data-stu-id="3f248-140">64</span></span>      | <span data-ttu-id="3f248-141">0x00000040</span><span class="sxs-lookup"><span data-stu-id="3f248-141">0x00000040</span></span>  | <span data-ttu-id="3f248-142">**msidbControlAttributesRightAligned**</span><span class="sxs-lookup"><span data-stu-id="3f248-142">**msidbControlAttributesRightAligned**</span></span> |
| [<span data-ttu-id="3f248-143">RTLRO</span><span class="sxs-lookup"><span data-stu-id="3f248-143">RTLRO</span></span>](rtlro-control-attribute.md)               | <span data-ttu-id="3f248-144">32</span><span class="sxs-lookup"><span data-stu-id="3f248-144">32</span></span>      | <span data-ttu-id="3f248-145">0x00000020</span><span class="sxs-lookup"><span data-stu-id="3f248-145">0x00000020</span></span>  | <span data-ttu-id="3f248-146">**msidbControlAttributesRTLRO**</span><span class="sxs-lookup"><span data-stu-id="3f248-146">**msidbControlAttributesRTLRO**</span></span>        |
| [<span data-ttu-id="3f248-147">Sunken</span><span class="sxs-lookup"><span data-stu-id="3f248-147">Sunken</span></span>](sunken-control-attribute.md)             | <span data-ttu-id="3f248-148">4</span><span class="sxs-lookup"><span data-stu-id="3f248-148">4</span></span>       | <span data-ttu-id="3f248-149">0x00000004</span><span class="sxs-lookup"><span data-stu-id="3f248-149">0x00000004</span></span>  | <span data-ttu-id="3f248-150">**msidbControlAttributesSunken**</span><span class="sxs-lookup"><span data-stu-id="3f248-150">**msidbControlAttributesSunken**</span></span>       |
| [<span data-ttu-id="3f248-151">Visible</span><span class="sxs-lookup"><span data-stu-id="3f248-151">Visible</span></span>](visible-control-attribute.md)           | <span data-ttu-id="3f248-152">1</span><span class="sxs-lookup"><span data-stu-id="3f248-152">1</span></span>       | <span data-ttu-id="3f248-153">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3f248-153">0x00000001</span></span>  | <span data-ttu-id="3f248-154">**msidbControlAttributesVisible**</span><span class="sxs-lookup"><span data-stu-id="3f248-154">**msidbControlAttributesVisible**</span></span>      |



 

<span data-ttu-id="3f248-155">Estos atributos de controles de texto se establecen con bits.</span><span class="sxs-lookup"><span data-stu-id="3f248-155">These attributes of Text controls are set with bits.</span></span>



| <span data-ttu-id="3f248-156">Atributo</span><span class="sxs-lookup"><span data-stu-id="3f248-156">Attribute</span></span>                                            | <span data-ttu-id="3f248-157">Decimal</span><span class="sxs-lookup"><span data-stu-id="3f248-157">Decimal</span></span> | <span data-ttu-id="3f248-158">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="3f248-158">Hexadecimal</span></span> | <span data-ttu-id="3f248-159">Constante</span><span class="sxs-lookup"><span data-stu-id="3f248-159">Constant</span></span>                                |
|------------------------------------------------------|---------|-------------|-----------------------------------------|
| [<span data-ttu-id="3f248-160">Formatear</span><span class="sxs-lookup"><span data-stu-id="3f248-160">FormatSize</span></span>](formatsize-control-attribute.md)       | <span data-ttu-id="3f248-161">524 288</span><span class="sxs-lookup"><span data-stu-id="3f248-161">524288</span></span>  | <span data-ttu-id="3f248-162">0x00080000</span><span class="sxs-lookup"><span data-stu-id="3f248-162">0x00080000</span></span>  | <span data-ttu-id="3f248-163">**msidbControlAttributesFormatSize**</span><span class="sxs-lookup"><span data-stu-id="3f248-163">**msidbControlAttributesFormatSize**</span></span>    |
| [<span data-ttu-id="3f248-164">Noprefix</span><span class="sxs-lookup"><span data-stu-id="3f248-164">NoPrefix</span></span>](noprefix-control-attribute.md)           | <span data-ttu-id="3f248-165">131 072</span><span class="sxs-lookup"><span data-stu-id="3f248-165">131072</span></span>  | <span data-ttu-id="3f248-166">0x00020000</span><span class="sxs-lookup"><span data-stu-id="3f248-166">0x00020000</span></span>  | <span data-ttu-id="3f248-167">**msidbControlAttributesNoPrefix**</span><span class="sxs-lookup"><span data-stu-id="3f248-167">**msidbControlAttributesNoPrefix**</span></span>      |
| [<span data-ttu-id="3f248-168">NoWrap</span><span class="sxs-lookup"><span data-stu-id="3f248-168">NoWrap</span></span>](nowrap-control-attribute.md)               | <span data-ttu-id="3f248-169">262 144</span><span class="sxs-lookup"><span data-stu-id="3f248-169">262144</span></span>  | <span data-ttu-id="3f248-170">0x00040000</span><span class="sxs-lookup"><span data-stu-id="3f248-170">0x00040000</span></span>  | <span data-ttu-id="3f248-171">**msidbControlAttributesNoWrap**</span><span class="sxs-lookup"><span data-stu-id="3f248-171">**msidbControlAttributesNoWrap**</span></span>        |
| [<span data-ttu-id="3f248-172">Contraseña</span><span class="sxs-lookup"><span data-stu-id="3f248-172">Password</span></span>](password-control-attribute.md)           | <span data-ttu-id="3f248-173">2 097 152</span><span class="sxs-lookup"><span data-stu-id="3f248-173">2097152</span></span> | <span data-ttu-id="3f248-174">0x00200000</span><span class="sxs-lookup"><span data-stu-id="3f248-174">0x00200000</span></span>  | <span data-ttu-id="3f248-175">**msidbControlAttributesPasswordInput**</span><span class="sxs-lookup"><span data-stu-id="3f248-175">**msidbControlAttributesPasswordInput**</span></span> |
| [<span data-ttu-id="3f248-176">Transparente</span><span class="sxs-lookup"><span data-stu-id="3f248-176">Transparent</span></span>](transparent-control-attribute.md)     | <span data-ttu-id="3f248-177">65536</span><span class="sxs-lookup"><span data-stu-id="3f248-177">65536</span></span>   | <span data-ttu-id="3f248-178">0x00010000</span><span class="sxs-lookup"><span data-stu-id="3f248-178">0x00010000</span></span>  | <span data-ttu-id="3f248-179">**msidbControlAttributesTransparent**</span><span class="sxs-lookup"><span data-stu-id="3f248-179">**msidbControlAttributesTransparent**</span></span>   |
| [<span data-ttu-id="3f248-180">UsersLanguage</span><span class="sxs-lookup"><span data-stu-id="3f248-180">UsersLanguage</span></span>](userslanguage-control-attribute.md) | <span data-ttu-id="3f248-181">1 048 576</span><span class="sxs-lookup"><span data-stu-id="3f248-181">1048576</span></span> | <span data-ttu-id="3f248-182">0x00100000</span><span class="sxs-lookup"><span data-stu-id="3f248-182">0x00100000</span></span>  | <span data-ttu-id="3f248-183">**msidbControlAttributesUsersLanguage**</span><span class="sxs-lookup"><span data-stu-id="3f248-183">**msidbControlAttributesUsersLanguage**</span></span> |



 

<span data-ttu-id="3f248-184">Este atributo del control ProgressBar se establece con un bit.</span><span class="sxs-lookup"><span data-stu-id="3f248-184">This attribute of the ProgressBar control is set with a bit.</span></span>



| <span data-ttu-id="3f248-185">Atributo</span><span class="sxs-lookup"><span data-stu-id="3f248-185">Attribute</span></span>                                      | <span data-ttu-id="3f248-186">Decimal</span><span class="sxs-lookup"><span data-stu-id="3f248-186">Decimal</span></span> | <span data-ttu-id="3f248-187">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="3f248-187">Hexadecimal</span></span> | <span data-ttu-id="3f248-188">Constante</span><span class="sxs-lookup"><span data-stu-id="3f248-188">Constant</span></span>                             |
|------------------------------------------------|---------|-------------|--------------------------------------|
| [<span data-ttu-id="3f248-189">Progress95</span><span class="sxs-lookup"><span data-stu-id="3f248-189">Progress95</span></span>](progress95-control-attribute.md) | <span data-ttu-id="3f248-190">65536</span><span class="sxs-lookup"><span data-stu-id="3f248-190">65536</span></span>   | <span data-ttu-id="3f248-191">0x00010000</span><span class="sxs-lookup"><span data-stu-id="3f248-191">0x00010000</span></span>  | <span data-ttu-id="3f248-192">**msidbControlAttributesProgress95**</span><span class="sxs-lookup"><span data-stu-id="3f248-192">**msidbControlAttributesProgress95**</span></span> |



 

<span data-ttu-id="3f248-193">Estos atributos de los controles volumen y directorio SelectCombo se establecen con bits.</span><span class="sxs-lookup"><span data-stu-id="3f248-193">These attributes of Volume and Directory SelectCombo controls are set with bits.</span></span>



| <span data-ttu-id="3f248-194">Atributo</span><span class="sxs-lookup"><span data-stu-id="3f248-194">Attribute</span></span>                                                | <span data-ttu-id="3f248-195">Decimal</span><span class="sxs-lookup"><span data-stu-id="3f248-195">Decimal</span></span> | <span data-ttu-id="3f248-196">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="3f248-196">Hexadecimal</span></span> | <span data-ttu-id="3f248-197">Constante</span><span class="sxs-lookup"><span data-stu-id="3f248-197">Constant</span></span>                                  |
|----------------------------------------------------------|---------|-------------|-------------------------------------------|
| [<span data-ttu-id="3f248-198">CDROMVolume</span><span class="sxs-lookup"><span data-stu-id="3f248-198">CDROMVolume</span></span>](cdromvolume-control-attribute.md)         | <span data-ttu-id="3f248-199">524 288</span><span class="sxs-lookup"><span data-stu-id="3f248-199">524288</span></span>  | <span data-ttu-id="3f248-200">0x00080000</span><span class="sxs-lookup"><span data-stu-id="3f248-200">0x00080000</span></span>  | <span data-ttu-id="3f248-201">**msidbControlAttributesCDROMVolume**</span><span class="sxs-lookup"><span data-stu-id="3f248-201">**msidbControlAttributesCDROMVolume**</span></span>     |
| [<span data-ttu-id="3f248-202">FixedVolume</span><span class="sxs-lookup"><span data-stu-id="3f248-202">FixedVolume</span></span>](fixedvolume-control-attribute.md)         | <span data-ttu-id="3f248-203">131 072</span><span class="sxs-lookup"><span data-stu-id="3f248-203">131072</span></span>  | <span data-ttu-id="3f248-204">0x00020000</span><span class="sxs-lookup"><span data-stu-id="3f248-204">0x00020000</span></span>  | <span data-ttu-id="3f248-205">**msidbControlAttributesFixedVolume**</span><span class="sxs-lookup"><span data-stu-id="3f248-205">**msidbControlAttributesFixedVolume**</span></span>     |
| [<span data-ttu-id="3f248-206">FloppyVolume</span><span class="sxs-lookup"><span data-stu-id="3f248-206">FloppyVolume</span></span>](floppyvolume-control-attribute.md)       | <span data-ttu-id="3f248-207">2 097 152</span><span class="sxs-lookup"><span data-stu-id="3f248-207">2097152</span></span> | <span data-ttu-id="3f248-208">0x00200000</span><span class="sxs-lookup"><span data-stu-id="3f248-208">0x00200000</span></span>  | <span data-ttu-id="3f248-209">**msidbControlAttributesFloppyVolume**</span><span class="sxs-lookup"><span data-stu-id="3f248-209">**msidbControlAttributesFloppyVolume**</span></span>    |
| [<span data-ttu-id="3f248-210">RAMDiskVolume</span><span class="sxs-lookup"><span data-stu-id="3f248-210">RAMDiskVolume</span></span>](ramdiskvolume-control-attribute.md)     | <span data-ttu-id="3f248-211">1 048 576</span><span class="sxs-lookup"><span data-stu-id="3f248-211">1048576</span></span> | <span data-ttu-id="3f248-212">0x00100000</span><span class="sxs-lookup"><span data-stu-id="3f248-212">0x00100000</span></span>  | <span data-ttu-id="3f248-213">**msidbControlAttributesRAMDiskVolume**</span><span class="sxs-lookup"><span data-stu-id="3f248-213">**msidbControlAttributesRAMDiskVolume**</span></span>   |
| [<span data-ttu-id="3f248-214">RemoteVolume</span><span class="sxs-lookup"><span data-stu-id="3f248-214">RemoteVolume</span></span>](remotevolume-control-attribute.md)       | <span data-ttu-id="3f248-215">262 144</span><span class="sxs-lookup"><span data-stu-id="3f248-215">262144</span></span>  | <span data-ttu-id="3f248-216">0x00040000</span><span class="sxs-lookup"><span data-stu-id="3f248-216">0x00040000</span></span>  | <span data-ttu-id="3f248-217">**msidbControlAttributesRemoteVolume**</span><span class="sxs-lookup"><span data-stu-id="3f248-217">**msidbControlAttributesRemoteVolume**</span></span>    |
| [<span data-ttu-id="3f248-218">RemovableVolume</span><span class="sxs-lookup"><span data-stu-id="3f248-218">RemovableVolume</span></span>](removablevolume-control-attribute.md) | <span data-ttu-id="3f248-219">65536</span><span class="sxs-lookup"><span data-stu-id="3f248-219">65536</span></span>   | <span data-ttu-id="3f248-220">0x00010000</span><span class="sxs-lookup"><span data-stu-id="3f248-220">0x00010000</span></span>  | <span data-ttu-id="3f248-221">**msidbControlAttributesRemovableVolume**</span><span class="sxs-lookup"><span data-stu-id="3f248-221">**msidbControlAttributesRemovableVolume**</span></span> |



 

<span data-ttu-id="3f248-222">Estos atributos de los controles ListBox y ComboBox se establecen con bits.</span><span class="sxs-lookup"><span data-stu-id="3f248-222">These attributes of ListBox and ComboBox controls are set with bits.</span></span>



| <span data-ttu-id="3f248-223">Atributo</span><span class="sxs-lookup"><span data-stu-id="3f248-223">Attribute</span></span>                                            | <span data-ttu-id="3f248-224">Decimal</span><span class="sxs-lookup"><span data-stu-id="3f248-224">Decimal</span></span> | <span data-ttu-id="3f248-225">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="3f248-225">Hexadecimal</span></span> | <span data-ttu-id="3f248-226">Constante</span><span class="sxs-lookup"><span data-stu-id="3f248-226">Constant</span></span>                            |
|------------------------------------------------------|---------|-------------|-------------------------------------|
| [<span data-ttu-id="3f248-227">Control ComboList</span><span class="sxs-lookup"><span data-stu-id="3f248-227">ComboList Control</span></span>](combolist-control-attribute.md) | <span data-ttu-id="3f248-228">131 072</span><span class="sxs-lookup"><span data-stu-id="3f248-228">131072</span></span>  | <span data-ttu-id="3f248-229">0x00020000</span><span class="sxs-lookup"><span data-stu-id="3f248-229">0x00020000</span></span>  | <span data-ttu-id="3f248-230">**msidbControlAttributesComboList**</span><span class="sxs-lookup"><span data-stu-id="3f248-230">**msidbControlAttributesComboList**</span></span> |
| [<span data-ttu-id="3f248-231">Control ordenado</span><span class="sxs-lookup"><span data-stu-id="3f248-231">Sorted Control</span></span>](sorted-control-attribute.md)       | <span data-ttu-id="3f248-232">65536</span><span class="sxs-lookup"><span data-stu-id="3f248-232">65536</span></span>   | <span data-ttu-id="3f248-233">0x00010000</span><span class="sxs-lookup"><span data-stu-id="3f248-233">0x00010000</span></span>  | <span data-ttu-id="3f248-234">**msidbControlAttributesSorted**</span><span class="sxs-lookup"><span data-stu-id="3f248-234">**msidbControlAttributesSorted**</span></span>    |



 

<span data-ttu-id="3f248-235">Este atributo del control de edición se establece con un bit.</span><span class="sxs-lookup"><span data-stu-id="3f248-235">This attribute of the Edit control is set with a bit.</span></span>



| <span data-ttu-id="3f248-236">Atributo</span><span class="sxs-lookup"><span data-stu-id="3f248-236">Attribute</span></span>                                    | <span data-ttu-id="3f248-237">Decimal</span><span class="sxs-lookup"><span data-stu-id="3f248-237">Decimal</span></span> | <span data-ttu-id="3f248-238">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="3f248-238">Hexadecimal</span></span> | <span data-ttu-id="3f248-239">Constante</span><span class="sxs-lookup"><span data-stu-id="3f248-239">Constant</span></span>                            |
|----------------------------------------------|---------|-------------|-------------------------------------|
| [<span data-ttu-id="3f248-240">Ocupa</span><span class="sxs-lookup"><span data-stu-id="3f248-240">MultiLine</span></span>](multiline-control-attribute.md) | <span data-ttu-id="3f248-241">65536</span><span class="sxs-lookup"><span data-stu-id="3f248-241">65536</span></span>   | <span data-ttu-id="3f248-242">0x00010000</span><span class="sxs-lookup"><span data-stu-id="3f248-242">0x00010000</span></span>  | <span data-ttu-id="3f248-243">**msidbControlAttributesMultiline**</span><span class="sxs-lookup"><span data-stu-id="3f248-243">**msidbControlAttributesMultiline**</span></span> |



 

<span data-ttu-id="3f248-244">Estos atributos de los controles PictureButton se establecen con bits.</span><span class="sxs-lookup"><span data-stu-id="3f248-244">These attributes of PictureButton controls are set with bits.</span></span>



| <span data-ttu-id="3f248-245">Atributo</span><span class="sxs-lookup"><span data-stu-id="3f248-245">Attribute</span></span>                                          | <span data-ttu-id="3f248-246">Decimal</span><span class="sxs-lookup"><span data-stu-id="3f248-246">Decimal</span></span> | <span data-ttu-id="3f248-247">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="3f248-247">Hexadecimal</span></span> | <span data-ttu-id="3f248-248">Constante</span><span class="sxs-lookup"><span data-stu-id="3f248-248">Constant</span></span>                             |
|----------------------------------------------------|---------|-------------|--------------------------------------|
| [<span data-ttu-id="3f248-249">Bitmap</span><span class="sxs-lookup"><span data-stu-id="3f248-249">Bitmap</span></span>](bitmap-control-attribute.md)             | <span data-ttu-id="3f248-250">262 144</span><span class="sxs-lookup"><span data-stu-id="3f248-250">262144</span></span>  | <span data-ttu-id="3f248-251">0x00040000</span><span class="sxs-lookup"><span data-stu-id="3f248-251">0x00040000</span></span>  | <span data-ttu-id="3f248-252">**msidbControlAttributesBitmap**</span><span class="sxs-lookup"><span data-stu-id="3f248-252">**msidbControlAttributesBitmap**</span></span>     |
| [<span data-ttu-id="3f248-253">FixedSize</span><span class="sxs-lookup"><span data-stu-id="3f248-253">FixedSize</span></span>](fixedsize-control-attribute.md)       | <span data-ttu-id="3f248-254">1 048 576</span><span class="sxs-lookup"><span data-stu-id="3f248-254">1048576</span></span> | <span data-ttu-id="3f248-255">0x00100000</span><span class="sxs-lookup"><span data-stu-id="3f248-255">0x00100000</span></span>  | <span data-ttu-id="3f248-256">**msidbControlAttributesFixedSize**</span><span class="sxs-lookup"><span data-stu-id="3f248-256">**msidbControlAttributesFixedSize**</span></span>  |
| [<span data-ttu-id="3f248-257">Icono</span><span class="sxs-lookup"><span data-stu-id="3f248-257">Icon</span></span>](icon-control-attribute.md)                 | <span data-ttu-id="3f248-258">524 288</span><span class="sxs-lookup"><span data-stu-id="3f248-258">524288</span></span>  | <span data-ttu-id="3f248-259">0x00080000</span><span class="sxs-lookup"><span data-stu-id="3f248-259">0x00080000</span></span>  | <span data-ttu-id="3f248-260">**msidbControlAttributesIcon**</span><span class="sxs-lookup"><span data-stu-id="3f248-260">**msidbControlAttributesIcon**</span></span>       |
| [<span data-ttu-id="3f248-261">IconSize16</span><span class="sxs-lookup"><span data-stu-id="3f248-261">IconSize16</span></span>](iconsize-control-attribute.md)       | <span data-ttu-id="3f248-262">2 097 152</span><span class="sxs-lookup"><span data-stu-id="3f248-262">2097152</span></span> | <span data-ttu-id="3f248-263">0x00200000</span><span class="sxs-lookup"><span data-stu-id="3f248-263">0x00200000</span></span>  | <span data-ttu-id="3f248-264">**msidbControlAttributesIconSize16**</span><span class="sxs-lookup"><span data-stu-id="3f248-264">**msidbControlAttributesIconSize16**</span></span> |
| [<span data-ttu-id="3f248-265">IconSize32</span><span class="sxs-lookup"><span data-stu-id="3f248-265">IconSize32</span></span>](iconsize-control-attribute.md)       | <span data-ttu-id="3f248-266">4 194 304</span><span class="sxs-lookup"><span data-stu-id="3f248-266">4194304</span></span> | <span data-ttu-id="3f248-267">0x00400000</span><span class="sxs-lookup"><span data-stu-id="3f248-267">0x00400000</span></span>  | <span data-ttu-id="3f248-268">**msidbControlAttributesIconSize32**</span><span class="sxs-lookup"><span data-stu-id="3f248-268">**msidbControlAttributesIconSize32**</span></span> |
| [<span data-ttu-id="3f248-269">IconSize48</span><span class="sxs-lookup"><span data-stu-id="3f248-269">IconSize48</span></span>](iconsize-control-attribute.md)       | <span data-ttu-id="3f248-270">6291456</span><span class="sxs-lookup"><span data-stu-id="3f248-270">6291456</span></span> | <span data-ttu-id="3f248-271">0x00600000</span><span class="sxs-lookup"><span data-stu-id="3f248-271">0x00600000</span></span>  | <span data-ttu-id="3f248-272">**msidbControlAttributesIconSize48**</span><span class="sxs-lookup"><span data-stu-id="3f248-272">**msidbControlAttributesIconSize48**</span></span> |
| [<span data-ttu-id="3f248-273">Control PushLike</span><span class="sxs-lookup"><span data-stu-id="3f248-273">PushLike Control</span></span>](pushlike-control-attribute.md) | <span data-ttu-id="3f248-274">131 072</span><span class="sxs-lookup"><span data-stu-id="3f248-274">131072</span></span>  | <span data-ttu-id="3f248-275">0x00020000</span><span class="sxs-lookup"><span data-stu-id="3f248-275">0x00020000</span></span>  | <span data-ttu-id="3f248-276">**msidbControlAttributesPushLike**</span><span class="sxs-lookup"><span data-stu-id="3f248-276">**msidbControlAttributesPushLike**</span></span>   |



 

<span data-ttu-id="3f248-277">Este atributo del control RadioButton se establece con un bit.</span><span class="sxs-lookup"><span data-stu-id="3f248-277">This attribute of RadioButton control is set with a bit.</span></span>



| <span data-ttu-id="3f248-278">Atributo</span><span class="sxs-lookup"><span data-stu-id="3f248-278">Attribute</span></span>                                    | <span data-ttu-id="3f248-279">Decimal</span><span class="sxs-lookup"><span data-stu-id="3f248-279">Decimal</span></span>  | <span data-ttu-id="3f248-280">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="3f248-280">Hexadecimal</span></span> | <span data-ttu-id="3f248-281">Constante</span><span class="sxs-lookup"><span data-stu-id="3f248-281">Constant</span></span>                            |
|----------------------------------------------|----------|-------------|-------------------------------------|
| [<span data-ttu-id="3f248-282">HasBorder</span><span class="sxs-lookup"><span data-stu-id="3f248-282">HasBorder</span></span>](hasborder-control-attribute.md) | <span data-ttu-id="3f248-283">16777216</span><span class="sxs-lookup"><span data-stu-id="3f248-283">16777216</span></span> | <span data-ttu-id="3f248-284">0x01000000</span><span class="sxs-lookup"><span data-stu-id="3f248-284">0x01000000</span></span>  | <span data-ttu-id="3f248-285">**msidbControlAttributesHasBorder**</span><span class="sxs-lookup"><span data-stu-id="3f248-285">**msidbControlAttributesHasBorder**</span></span> |



 

<span data-ttu-id="3f248-286">Este atributo del control PushButton se establece con un bit.</span><span class="sxs-lookup"><span data-stu-id="3f248-286">This attribute of PushButton control is set with a bit.</span></span>



| <span data-ttu-id="3f248-287">Atributo</span><span class="sxs-lookup"><span data-stu-id="3f248-287">Attribute</span></span>                                        | <span data-ttu-id="3f248-288">Decimal</span><span class="sxs-lookup"><span data-stu-id="3f248-288">Decimal</span></span> | <span data-ttu-id="3f248-289">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="3f248-289">Hexadecimal</span></span> | <span data-ttu-id="3f248-290">Constante</span><span class="sxs-lookup"><span data-stu-id="3f248-290">Constant</span></span>                                  |
|--------------------------------------------------|---------|-------------|-------------------------------------------|
| [<span data-ttu-id="3f248-291">ElevationShield</span><span class="sxs-lookup"><span data-stu-id="3f248-291">ElevationShield</span></span>](elevationshield-attribute.md) | <span data-ttu-id="3f248-292">8388608</span><span class="sxs-lookup"><span data-stu-id="3f248-292">8388608</span></span> | <span data-ttu-id="3f248-293">0x00800000</span><span class="sxs-lookup"><span data-stu-id="3f248-293">0x00800000</span></span>  | <span data-ttu-id="3f248-294">**msidbControlAttributesElevationShield**</span><span class="sxs-lookup"><span data-stu-id="3f248-294">**msidbControlAttributesElevationShield**</span></span> |



 

<span data-ttu-id="3f248-295">Este atributo de control VolumeCostList se establece con un bit.</span><span class="sxs-lookup"><span data-stu-id="3f248-295">This attribute of VolumeCostList control is set with a bit.</span></span>



| <span data-ttu-id="3f248-296">Atributo</span><span class="sxs-lookup"><span data-stu-id="3f248-296">Attribute</span></span>                                                                | <span data-ttu-id="3f248-297">Decimal</span><span class="sxs-lookup"><span data-stu-id="3f248-297">Decimal</span></span> | <span data-ttu-id="3f248-298">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="3f248-298">Hexadecimal</span></span> | <span data-ttu-id="3f248-299">Constante</span><span class="sxs-lookup"><span data-stu-id="3f248-299">Constant</span></span>                         |
|--------------------------------------------------------------------------|---------|-------------|----------------------------------|
| [<span data-ttu-id="3f248-300">ControlShowRollbackCost</span><span class="sxs-lookup"><span data-stu-id="3f248-300">ControlShowRollbackCost</span></span>](controlshowrollbackcost-control-attribute.md) | <span data-ttu-id="3f248-301">4 194 304</span><span class="sxs-lookup"><span data-stu-id="3f248-301">4194304</span></span> | <span data-ttu-id="3f248-302">0x00400000</span><span class="sxs-lookup"><span data-stu-id="3f248-302">0x00400000</span></span>  | <span data-ttu-id="3f248-303">**msidbControlShowRollbackCost**</span><span class="sxs-lookup"><span data-stu-id="3f248-303">**msidbControlShowRollbackCost**</span></span> |



 

<span data-ttu-id="3f248-304">Los siguientes atributos de control no se establecen con bits.</span><span class="sxs-lookup"><span data-stu-id="3f248-304">The following control attributes are not set with bits.</span></span> <span data-ttu-id="3f248-305">Estos atributos se crean en las tablas de la interfaz de usuario o se establecen mediante [eventos de control](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="3f248-305">These attributes are authored into the user interface tables or are set using [Control Events](control-events.md).</span></span>

[<span data-ttu-id="3f248-306">BillboardName</span><span class="sxs-lookup"><span data-stu-id="3f248-306">BillboardName</span></span>](billboardname-control-attribute.md)

 

[<span data-ttu-id="3f248-307">IndirectPropertyName</span><span class="sxs-lookup"><span data-stu-id="3f248-307">IndirectPropertyName</span></span>](indirectpropertyname-control-attribute.md)

 

[<span data-ttu-id="3f248-308">Position</span><span class="sxs-lookup"><span data-stu-id="3f248-308">Position</span></span>](position-control-attribute.md)

 

[<span data-ttu-id="3f248-309">Control de progreso</span><span class="sxs-lookup"><span data-stu-id="3f248-309">Progress Control</span></span>](progress-control-attribute.md)

 

[<span data-ttu-id="3f248-310">PropertyName</span><span class="sxs-lookup"><span data-stu-id="3f248-310">PropertyName</span></span>](propertyname-control-attribute.md)

 

[<span data-ttu-id="3f248-311">PropertyValue</span><span class="sxs-lookup"><span data-stu-id="3f248-311">PropertyValue</span></span>](propertyvalue-control-attribute.md)

 

[<span data-ttu-id="3f248-312">Text Control</span><span class="sxs-lookup"><span data-stu-id="3f248-312">Text Control</span></span>](text-control-attribute.md)

 

[<span data-ttu-id="3f248-313">TimeRemaining</span><span class="sxs-lookup"><span data-stu-id="3f248-313">TimeRemaining</span></span>](timeremaining-control-attribute.md)

<span data-ttu-id="3f248-314">Vea [Agregar controles y texto](adding-controls-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="3f248-314">See [Adding Controls and Text](adding-controls-and-text.md).</span></span>

 

 



