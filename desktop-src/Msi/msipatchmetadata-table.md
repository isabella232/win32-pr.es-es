---
description: La tabla MsiPatchMetadata contiene información acerca de una revisión Windows Installer necesaria para quitar la revisión y que se usa en Agregar o quitar programas.
ms.assetid: b1c30e16-6c91-451a-8b75-7ddbcefcc092
title: Tabla MsiPatchMetadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2642661a8f9dc067086926f8e993fc32c95a4a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653057"
---
# <a name="msipatchmetadata-table"></a><span data-ttu-id="c814d-103">Tabla MsiPatchMetadata</span><span class="sxs-lookup"><span data-stu-id="c814d-103">MsiPatchMetadata Table</span></span>

<span data-ttu-id="c814d-104">La tabla MsiPatchMetadata contiene información acerca de una revisión Windows Installer necesaria para quitar la revisión y que se usa en **Agregar o quitar programas**.</span><span class="sxs-lookup"><span data-stu-id="c814d-104">The MsiPatchMetadata Table contains information about a Windows Installer patch that is required to remove the patch and that is used by **Add/Remove Programs**.</span></span>

<span data-ttu-id="c814d-105">Las revisiones instaladas sin esta tabla presente en la base de datos de revisiones (archivo. msp) no se pueden quitar y carecen de cierta información de **Agregar o quitar programas**.</span><span class="sxs-lookup"><span data-stu-id="c814d-105">Patches installed without this table present in the patch database (.msp file) cannot be removed, and are missing some information from **Add/Remove Programs**.</span></span> <span data-ttu-id="c814d-106">La tabla debe estar en la base de datos del archivo de revisión y no en una transformación de la revisión.</span><span class="sxs-lookup"><span data-stu-id="c814d-106">The table must be in the database of the patch file and not in a transform in the patch.</span></span>

<span data-ttu-id="c814d-107">La tabla MsiPatchMetadata tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="c814d-107">The MsiPatchMetadata Table has the following columns.</span></span>



| <span data-ttu-id="c814d-108">Columna</span><span class="sxs-lookup"><span data-stu-id="c814d-108">Column</span></span>   | <span data-ttu-id="c814d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c814d-109">Type</span></span>                         | <span data-ttu-id="c814d-110">Clave</span><span class="sxs-lookup"><span data-stu-id="c814d-110">Key</span></span> | <span data-ttu-id="c814d-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="c814d-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="c814d-112">Compañía</span><span class="sxs-lookup"><span data-stu-id="c814d-112">Company</span></span>  | [<span data-ttu-id="c814d-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="c814d-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="c814d-114">Y</span><span class="sxs-lookup"><span data-stu-id="c814d-114">Y</span></span>   | <span data-ttu-id="c814d-115">Y</span><span class="sxs-lookup"><span data-stu-id="c814d-115">Y</span></span>        |
| <span data-ttu-id="c814d-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c814d-116">Property</span></span> | [<span data-ttu-id="c814d-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="c814d-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="c814d-118">Y</span><span class="sxs-lookup"><span data-stu-id="c814d-118">Y</span></span>   | <span data-ttu-id="c814d-119">N</span><span class="sxs-lookup"><span data-stu-id="c814d-119">N</span></span>        |
| <span data-ttu-id="c814d-120">Value</span><span class="sxs-lookup"><span data-stu-id="c814d-120">Value</span></span>    | [<span data-ttu-id="c814d-121">Texto</span><span class="sxs-lookup"><span data-stu-id="c814d-121">Text</span></span>](text.md)             | <span data-ttu-id="c814d-122">N</span><span class="sxs-lookup"><span data-stu-id="c814d-122">N</span></span>   | <span data-ttu-id="c814d-123">N</span><span class="sxs-lookup"><span data-stu-id="c814d-123">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c814d-124">Columnas</span><span class="sxs-lookup"><span data-stu-id="c814d-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c814d-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Recíproca</span><span class="sxs-lookup"><span data-stu-id="c814d-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Company</span></span>
</dt> <dd>

<span data-ttu-id="c814d-126">El nombre de la empresa.</span><span class="sxs-lookup"><span data-stu-id="c814d-126">The name of the company.</span></span> <span data-ttu-id="c814d-127">Un campo vacío (un valor null) indica que la fila contiene una de las propiedades de metadatos estándar del Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c814d-127">An empty field (a Null value) indicates that the row contains one of the standard metadata properties of the Windows Installer.</span></span> <span data-ttu-id="c814d-128">Para obtener más información, consulte la sección Comentarios de este tema.</span><span class="sxs-lookup"><span data-stu-id="c814d-128">For more information, see the Remarks section of this topic.</span></span>

<span data-ttu-id="c814d-129">Al agregar una fila a la tabla y escribir el nombre de la compañía en este campo, puede agregar cualquier compañía para ampliar el conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="c814d-129">By adding a row to the table and entering a company name in this field, you can add any company to extend the property set.</span></span>

</dd> <dt>

<span data-ttu-id="c814d-130"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad</span><span class="sxs-lookup"><span data-stu-id="c814d-130"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="c814d-131">Nombre de una propiedad de metadatos.</span><span class="sxs-lookup"><span data-stu-id="c814d-131">The name of a metadata property.</span></span>

</dd> <dt>

<span data-ttu-id="c814d-132"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="c814d-132"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="c814d-133">Valor de propiedad de los metadatos.</span><span class="sxs-lookup"><span data-stu-id="c814d-133">The value of the metadata property.</span></span> <span data-ttu-id="c814d-134">Nunca puede ser null ni una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="c814d-134">This can never be Null or an empty string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c814d-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c814d-135">Remarks</span></span>

<span data-ttu-id="c814d-136">Disponible en Windows Installer 3,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="c814d-136">Available in Windows Installer 3.0 and later.</span></span>

<span data-ttu-id="c814d-137">Las filas de la tabla MsiPatchMetadata que contienen un valor null en el campo CompanyName hacen referencia a una de las siguientes propiedades de metadatos de Windows Installer estándar.</span><span class="sxs-lookup"><span data-stu-id="c814d-137">Rows in the MsiPatchMetadata Table that contain a Null value in the CompanyName field refer to one of the following standard Windows Installer metadata properties.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c814d-138">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c814d-138">Property</span></span></th>
<th><span data-ttu-id="c814d-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="c814d-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c814d-140">AllowRemoval</span><span class="sxs-lookup"><span data-stu-id="c814d-140">AllowRemoval</span></span></td>
<td><span data-ttu-id="c814d-141">Indica si la revisión es o no una <a href="uninstallable-patches.md">revisión desinstalable</a>.</span><span class="sxs-lookup"><span data-stu-id="c814d-141">Indicates whether or not the patch is an <a href="uninstallable-patches.md">Uninstallable Patch</a>.</span></span> <span data-ttu-id="c814d-142">Si el campo de valor contiene 0 (cero), no se puede quitar la revisión.</span><span class="sxs-lookup"><span data-stu-id="c814d-142">If the value field contains 0 (zero), the patch cannot be removed.</span></span> <span data-ttu-id="c814d-143">Si el campo de valor contiene uno (1), la revisión es una revisión que no se puede instalar. esta propiedad está registrada y su valor se puede obtener mediante la función <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c814d-143">If the value field contains one (1), the patch is an Uninstallable Patch.This property is registered and its value can be obtain by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c814d-144">ManufacturerName</span><span class="sxs-lookup"><span data-stu-id="c814d-144">ManufacturerName</span></span></td>
<td><span data-ttu-id="c814d-145">Nombre del fabricante de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c814d-145">Name of the manufacturer of the application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c814d-146">MinorUpdateTargetRTM</span><span class="sxs-lookup"><span data-stu-id="c814d-146">MinorUpdateTargetRTM</span></span></td>
<td><span data-ttu-id="c814d-147">Indica que la revisión tiene como destino la versión RTM del producto o la revisión de actualización principal más reciente.</span><span class="sxs-lookup"><span data-stu-id="c814d-147">Indicates that the patch targets the RTM version of the product or the most recent major upgrade patch.</span></span> <span data-ttu-id="c814d-148">Cree esta propiedad opcional en revisiones de actualización secundarias que contengan información de secuenciación para indicar que la revisión quita todas las revisiones hasta la versión RTM del producto o hasta la última revisión de actualización principal.</span><span class="sxs-lookup"><span data-stu-id="c814d-148">Author this optional property in minor upgrade patches that contain sequencing information to indicate that the patch removes of all patches up to the RTM version of the product, or up to the most recent major upgrade patch.</span></span> <span data-ttu-id="c814d-149">Esta propiedad está disponible en Windows Installer 3,1 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="c814d-149">This property is available in Windows Installer 3.1 and later.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c814d-150">TargetProductName</span><span class="sxs-lookup"><span data-stu-id="c814d-150">TargetProductName</span></span></td>
<td><span data-ttu-id="c814d-151">Nombre del conjunto de aplicaciones de destino o aplicación.</span><span class="sxs-lookup"><span data-stu-id="c814d-151">Name of the application or target application suite.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c814d-152">MoreInfoURL</span><span class="sxs-lookup"><span data-stu-id="c814d-152">MoreInfoURL</span></span></td>
<td><span data-ttu-id="c814d-153">Una dirección URL que proporciona información específica de esta revisión.</span><span class="sxs-lookup"><span data-stu-id="c814d-153">A URL that provides information specific to this patch.</span></span> <span data-ttu-id="c814d-154">Esta propiedad está registrada y su valor se puede obtener mediante la función <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c814d-154">This property is registered and its value can be obtained by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="c814d-155">A partir de Windows XP con Service Pack 2 (SP2), este valor puede ser el vínculo de soporte técnico de la revisión que se muestra en <strong>Agregar o quitar programas</strong>.</span><span class="sxs-lookup"><span data-stu-id="c814d-155">Beginning with Windows XP with Service Pack 2 (SP2), this value can be the support link for the patch displayed in <strong>Add/Remove Programs</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c814d-156">CreationTimeUTC</span><span class="sxs-lookup"><span data-stu-id="c814d-156">CreationTimeUTC</span></span></td>
<td><span data-ttu-id="c814d-157">Hora de creación del archivo. MSP en formato MM-DD-YY HH: MM (mes-día-año hora: minuto).</span><span class="sxs-lookup"><span data-stu-id="c814d-157">Creation time of the .msp file in the form of mm-dd-yy HH:MM (month-day-year hour:minute).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c814d-158">DisplayName</span><span class="sxs-lookup"><span data-stu-id="c814d-158">DisplayName</span></span></td>
<td><span data-ttu-id="c814d-159">Título de la revisión que es correcto para la presentación pública.</span><span class="sxs-lookup"><span data-stu-id="c814d-159">A title for the patch that is okay for public display.</span></span> <span data-ttu-id="c814d-160">Esta propiedad está registrada y su valor se puede obtener mediante la función <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c814d-160">This property is registered, and its value can be obtained by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="c814d-161">A partir de Windows XP con SP2, este valor es el nombre de la revisión que se muestra en <strong>Agregar o quitar programas</strong>.</span><span class="sxs-lookup"><span data-stu-id="c814d-161">Beginning with Windows XP with SP2, this value is the name of the patch that is displayed in <strong>Add/Remove Programs</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c814d-162">Descripción</span><span class="sxs-lookup"><span data-stu-id="c814d-162">Description</span></span></td>
<td><span data-ttu-id="c814d-163">Breve descripción de la revisión.</span><span class="sxs-lookup"><span data-stu-id="c814d-163">Brief description of the patch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c814d-164">Clasificación</span><span class="sxs-lookup"><span data-stu-id="c814d-164">Classification</span></span></td>
<td><span data-ttu-id="c814d-165">Valor de cadena que contiene la categoría arbitraria de actualizaciones tal como la define el autor de la revisión.</span><span class="sxs-lookup"><span data-stu-id="c814d-165">A string value that contains the arbitrary category of updates as defined by the author of the patch.</span></span> <span data-ttu-id="c814d-166">Por ejemplo, los autores de revisiones pueden especificar que cada revisión se clasifique como revisión, acumulación de seguridad, actualización crítica, actualización, Service Pack o paquete acumulativo de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="c814d-166">For example, patch authors can specify that each patch be classified as a Hotfix, Security Rollup, Critical Update, Update, Service Pack, or Update Rollup.</span></span> <span data-ttu-id="c814d-167">Esta propiedad es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="c814d-167">This property is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c814d-168">OptimizeCA</span><span class="sxs-lookup"><span data-stu-id="c814d-168">OptimizeCA</span></span></td>
<td><span data-ttu-id="c814d-169">Indica si el Windows Installer debe omitir las acciones personalizadas al aplicar la revisión.</span><span class="sxs-lookup"><span data-stu-id="c814d-169">Indicates whether the Windows Installer should skip custom actions when applying the patch.</span></span> <span data-ttu-id="c814d-170">Esto puede reducir el tiempo necesario para aplicar la revisión.</span><span class="sxs-lookup"><span data-stu-id="c814d-170">This can reduce the time required to apply the patch.</span></span> <span data-ttu-id="c814d-171">La propiedad OptimizeCA puede tener uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="c814d-171">The OptimizeCA property can have one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="c814d-172">0: no omitir ninguna acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="c814d-172">0 - Do not skip any custom actions.</span></span></li>
<li><span data-ttu-id="c814d-173">1-omitir acciones personalizadas de asignación de propiedades y de directorios.</span><span class="sxs-lookup"><span data-stu-id="c814d-173">1 - Skip property and directory assignment custom actions.</span></span> <span data-ttu-id="c814d-174">El <a href="custom-action-type-35.md">tipo de acción personalizada 35</a> y el <a href="custom-action-type-51.md">tipo de acción personalizada 51</a> pueden ser acciones personalizadas de asignación de propiedades y de directorios.</span><span class="sxs-lookup"><span data-stu-id="c814d-174"><a href="custom-action-type-35.md">Custom Action Type 35</a> and <a href="custom-action-type-51.md">Custom Action Type 51</a> can be property and directory assignment custom actions.</span></span></li>
<li><span data-ttu-id="c814d-175">2-omitir acciones personalizadas inmediatas que no se encuentran en las asignaciones de propiedades o directorios.</span><span class="sxs-lookup"><span data-stu-id="c814d-175">2 - Skip immediate custom actions that do not fall into the property or directory assignments.</span></span> <span data-ttu-id="c814d-176">Las acciones personalizadas inmediatas no incluyen la opción msidbCustomActionTypeInScript en la columna Type de la <a href="customaction-table.md">tabla CustomAction</a>.</span><span class="sxs-lookup"><span data-stu-id="c814d-176">The immediate custom actions do not include msidbCustomActionTypeInScript option in the Type column of the <a href="customaction-table.md">CustomAction Table</a>.</span></span></li>
<li><span data-ttu-id="c814d-177">4-omitir las acciones personalizadas que se ejecutan dentro del script.</span><span class="sxs-lookup"><span data-stu-id="c814d-177">4 - Skip custom actions that run within the script.</span></span></li>
</ul>
<span data-ttu-id="c814d-178">El valor de OptimizeCA debe ser el mismo para todas las revisiones que se están instalando o no se omite ninguna acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="c814d-178">The value of OptimizeCA must be the same for all patches that are being installed or no custom actions are skipped.</span></span> <span data-ttu-id="c814d-179">Por ejemplo, si se instalan dos revisiones y OptimizeCA se establece en los valores 1 y 2 respectivamente, no se omite ninguna acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="c814d-179">For example, if two patches are being installed, and OptimizeCA is set to the values 1 and 2 respectively, no custom actions are skipped.</span></span> <br/> <span data-ttu-id="c814d-180">Los valores de OptimizeCA se pueden combinar al procesar varias revisiones nuevas.</span><span class="sxs-lookup"><span data-stu-id="c814d-180">The values of OptimizeCA can be combined when processing multiple new patches.</span></span> <span data-ttu-id="c814d-181">Si todas las revisiones tienen un 1 (uno) incluido en los valores, se omiten todas las acciones personalizadas de asignación de propiedades y de directorios.</span><span class="sxs-lookup"><span data-stu-id="c814d-181">If all patches have a 1 (one) included in the values, then all property and directory assignment custom actions are skipped.</span></span> <span data-ttu-id="c814d-182">Si una revisión tiene el valor 3 (tres) para la propiedad y una revisión tiene el valor 1 (uno) para la propiedad, se omiten las acciones personalizadas de la propiedad y la asignación de directorio.</span><span class="sxs-lookup"><span data-stu-id="c814d-182">If one patch has the value 3 (three)for the property, and one patch has the value 1 (one) for the property, the property and directory assignment custom actions are skipped.</span></span> <span data-ttu-id="c814d-183">Sin embargo, se ejecutan las otras acciones personalizadas inmediatas, ya que no se omiten todas las revisiones solicitadas.</span><span class="sxs-lookup"><span data-stu-id="c814d-183">However, the other immediate custom actions run, because not all of the patches requested are skipped.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c814d-184">OptimizedInstallMode</span><span class="sxs-lookup"><span data-stu-id="c814d-184">OptimizedInstallMode</span></span></td>
<td><span data-ttu-id="c814d-185">Si esta propiedad se establece en 1 (uno) en todas las revisiones que se van a aplicar en una transacción, se optimizará una aplicación de la revisión si es posible.</span><span class="sxs-lookup"><span data-stu-id="c814d-185">If this property is set to 1 (one) in all the patches to be applied in a transaction, an application of the patch is optimized if possible.</span></span> <span data-ttu-id="c814d-186">Para obtener más información, vea <a href="patch-optimization.md">optimización de revisiones</a>.</span><span class="sxs-lookup"><span data-stu-id="c814d-186">For more information, see <a href="patch-optimization.md">Patch Optimization</a>.</span></span> <span data-ttu-id="c814d-187">Disponible a partir de Windows Installer 3,1.</span><span class="sxs-lookup"><span data-stu-id="c814d-187">Available beginning with Windows Installer 3.1.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="validation"></a><span data-ttu-id="c814d-188">Validación</span><span class="sxs-lookup"><span data-stu-id="c814d-188">Validation</span></span>

<dl>

[<span data-ttu-id="c814d-189">ICE03</span><span class="sxs-lookup"><span data-stu-id="c814d-189">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c814d-190">ICE06</span><span class="sxs-lookup"><span data-stu-id="c814d-190">ICE06</span></span>](ice06.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="c814d-191">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c814d-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c814d-192">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="c814d-192">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




