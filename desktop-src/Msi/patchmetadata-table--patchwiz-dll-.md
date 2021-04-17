---
description: La tabla PatchMetadata contiene información acerca de una revisión Windows Installer necesaria para quitar una revisión y que se usa en Agregar o quitar programas.
ms.assetid: 09a06de4-0713-4e92-ab29-f34f6c94b677
title: Tabla PatchMetadata (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2521684714b91d8d172f8eb56bab984ffea87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653053"
---
# <a name="patchmetadata-table-patchwizdll"></a><span data-ttu-id="51792-103">Tabla PatchMetadata (PATCHWIZ.DLL)</span><span class="sxs-lookup"><span data-stu-id="51792-103">PatchMetadata Table (PATCHWIZ.DLL)</span></span>

<span data-ttu-id="51792-104">La tabla PatchMetadata contiene información acerca de una revisión Windows Installer necesaria para quitar una revisión y que se usa en Agregar o quitar programas.</span><span class="sxs-lookup"><span data-stu-id="51792-104">The PatchMetadata Table contains information about a Windows Installer patch that is required to remove a patch and that is used by Add/Remove Programs.</span></span> <span data-ttu-id="51792-105">Todas las propiedades de la tabla PatchMetadata se agregan a la [tabla MsiPatchMetadata](msipatchmetadata-table.md) del archivo. msp para una revisión.</span><span class="sxs-lookup"><span data-stu-id="51792-105">All the properties in the PatchMetadata Table are added to the [MsiPatchMetadata Table](msipatchmetadata-table.md) of the .msp file for a patch.</span></span>

<span data-ttu-id="51792-106">La tabla PatchMetadata es necesaria en los archivos de propiedades de creación de revisiones (archivos. PCP) que tienen un valor de MinimumRequiredMsiVersion igual a 300 en la [tabla de propiedades](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="51792-106">The PatchMetadata Table is required in patch creation properties files (.pcp files) that have a MinimumRequiredMsiVersion equal to 300 in the [Properties Table](properties-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="51792-107">La tabla es opcional si MinimumRequiredMsiVersion no es igual a 300.</span><span class="sxs-lookup"><span data-stu-id="51792-107">The table is optional if MinimumRequiredMsiVersion is not equal to 300.</span></span>

<span data-ttu-id="51792-108">La tabla PatchMetadata tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="51792-108">The PatchMetadata Table has the following columns.</span></span>



| <span data-ttu-id="51792-109">Columna</span><span class="sxs-lookup"><span data-stu-id="51792-109">Column</span></span>   | <span data-ttu-id="51792-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="51792-110">Type</span></span> | <span data-ttu-id="51792-111">Clave</span><span class="sxs-lookup"><span data-stu-id="51792-111">Key</span></span> | <span data-ttu-id="51792-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="51792-112">Nullable</span></span> |
|----------|------|-----|----------|
| <span data-ttu-id="51792-113">Compañía</span><span class="sxs-lookup"><span data-stu-id="51792-113">Company</span></span>  | <span data-ttu-id="51792-114">text</span><span class="sxs-lookup"><span data-stu-id="51792-114">text</span></span> | <span data-ttu-id="51792-115">Y</span><span class="sxs-lookup"><span data-stu-id="51792-115">Y</span></span>   | <span data-ttu-id="51792-116">Y</span><span class="sxs-lookup"><span data-stu-id="51792-116">Y</span></span>        |
| <span data-ttu-id="51792-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="51792-117">Property</span></span> | <span data-ttu-id="51792-118">text</span><span class="sxs-lookup"><span data-stu-id="51792-118">text</span></span> | <span data-ttu-id="51792-119">Y</span><span class="sxs-lookup"><span data-stu-id="51792-119">Y</span></span>   | <span data-ttu-id="51792-120">N</span><span class="sxs-lookup"><span data-stu-id="51792-120">N</span></span>        |
| <span data-ttu-id="51792-121">Value</span><span class="sxs-lookup"><span data-stu-id="51792-121">Value</span></span>    | <span data-ttu-id="51792-122">text</span><span class="sxs-lookup"><span data-stu-id="51792-122">text</span></span> |     | <span data-ttu-id="51792-123">Y</span><span class="sxs-lookup"><span data-stu-id="51792-123">Y</span></span>        |



 

### <a name="columns"></a><span data-ttu-id="51792-124">Columnas</span><span class="sxs-lookup"><span data-stu-id="51792-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="51792-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Recíproca</span><span class="sxs-lookup"><span data-stu-id="51792-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Company</span></span>
</dt> <dd>

<span data-ttu-id="51792-126">El nombre de la empresa.</span><span class="sxs-lookup"><span data-stu-id="51792-126">The name of the company.</span></span> <span data-ttu-id="51792-127">Un campo vacío (un valor null) indica que esta fila contiene una de las propiedades de metadatos estándar.</span><span class="sxs-lookup"><span data-stu-id="51792-127">An empty field (a Null value) indicates that this row contains one of the standard metadata properties.</span></span> <span data-ttu-id="51792-128">Una empresa puede extender el conjunto de propiedades agregando una fila a la tabla y especificando un nombre de compañía en este campo.</span><span class="sxs-lookup"><span data-stu-id="51792-128">A company can extend the property set by adding a row to the table, and entering a company name in this field.</span></span>

</dd> <dt>

<span data-ttu-id="51792-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad</span><span class="sxs-lookup"><span data-stu-id="51792-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="51792-130">Nombre de una propiedad de metadatos.</span><span class="sxs-lookup"><span data-stu-id="51792-130">The name of a metadata property.</span></span> <span data-ttu-id="51792-131">Las propiedades AllowRemoval, ManufacturerName, TargetProductName, MoreInfoURL, DisplayName, Description y Classification son necesarias en la tabla PatchMetadata.</span><span class="sxs-lookup"><span data-stu-id="51792-131">The AllowRemoval, ManufacturerName, TargetProductName, MoreInfoURL, DisplayName, Description, and Classification properties are required in the PatchMetadata Table .</span></span> <span data-ttu-id="51792-132">Este campo debe contener una de las siguientes propiedades de metadatos estándar si el campo Company está vacío (un valor null).</span><span class="sxs-lookup"><span data-stu-id="51792-132">This field must contain one of the following standard metadata properties if the Company field is empty (a Null value).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="51792-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="51792-133">Property</span></span></th>
<th><span data-ttu-id="51792-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="51792-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="51792-135">AllowRemoval</span><span class="sxs-lookup"><span data-stu-id="51792-135">AllowRemoval</span></span></td>
<td><span data-ttu-id="51792-136">Un valor entero que indica si la revisión es o no una <a href="uninstallable-patches.md">revisión desinstalable</a>.</span><span class="sxs-lookup"><span data-stu-id="51792-136">An integer value that indicates whether or not the patch is an <a href="uninstallable-patches.md">Uninstallable Patch</a>.</span></span> <span data-ttu-id="51792-137">Si el campo de valor contiene un 0 (cero), no se puede quitar la revisión.</span><span class="sxs-lookup"><span data-stu-id="51792-137">If the Value field contains a 0 (zero), the patch cannot be removed.</span></span> <span data-ttu-id="51792-138">Si el campo de valor contiene 1 (uno), la revisión es una revisión que no se pudo instalar.</span><span class="sxs-lookup"><span data-stu-id="51792-138">If the Value field contains 1 (one), the patch is an Uninstallable Patch.</span></span> <span data-ttu-id="51792-139">Esta propiedad es obligatoria. Esta propiedad está registrada y su valor se puede obtener mediante la función <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="51792-139">This property is required.This property is registered and its value can be obtain by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51792-140">ManufacturerName</span><span class="sxs-lookup"><span data-stu-id="51792-140">ManufacturerName</span></span></td>
<td><span data-ttu-id="51792-141">Valor de cadena que contiene el nombre del fabricante de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="51792-141">A string value that contains the name of the manufacturer of the application.</span></span> <span data-ttu-id="51792-142">Esta propiedad es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="51792-142">This property is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51792-143">MinorUpdateTargetRTM</span><span class="sxs-lookup"><span data-stu-id="51792-143">MinorUpdateTargetRTM</span></span></td>
<td><span data-ttu-id="51792-144">Indica que la revisión tiene como destino la versión RTM del producto o la revisión de actualización principal más reciente.</span><span class="sxs-lookup"><span data-stu-id="51792-144">Indicates that the patch targets the RTM version of the product or the most recent major upgrade patch.</span></span> <span data-ttu-id="51792-145">Cree esta propiedad opcional en revisiones de actualización secundarias que contengan información de secuenciación para indicar que la revisión quita todas las revisiones hasta la versión RTM del producto o hasta la última revisión de actualización principal.</span><span class="sxs-lookup"><span data-stu-id="51792-145">Author this optional property in minor upgrade patches that contain sequencing information to indicate that the patch removes of all patches up to the RTM version of the product, or up to the most recent major upgrade patch.</span></span> <span data-ttu-id="51792-146">Esta propiedad está disponible a partir de Windows Installer 3,1.</span><span class="sxs-lookup"><span data-stu-id="51792-146">This property is available beginning with Windows Installer 3.1.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="51792-147">Para requerir la instalación de Windows Installer 3,1 para aplicar la revisión, establezca la propiedad MinimumRequiredMsiVersion en 310 en la <a href="properties-table-patchwiz-dll-.md">tabla de propiedades</a> del archivo. PCP.</span><span class="sxs-lookup"><span data-stu-id="51792-147">To require that Windows Installer 3.1 be installed to apply the patch, set the MinimumRequiredMsiVersion property to 310 in the <a href="properties-table-patchwiz-dll-.md">Properties Table</a> of the .pcp file.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51792-148">TargetProductName</span><span class="sxs-lookup"><span data-stu-id="51792-148">TargetProductName</span></span></td>
<td><span data-ttu-id="51792-149">Valor de cadena que contiene el nombre de la aplicación o el conjunto de aplicaciones de destino.</span><span class="sxs-lookup"><span data-stu-id="51792-149">A string value that contains the name of the application or target application suite.</span></span> <span data-ttu-id="51792-150">Esta propiedad es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="51792-150">This property is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51792-151">MoreInfoURL</span><span class="sxs-lookup"><span data-stu-id="51792-151">MoreInfoURL</span></span></td>
<td><span data-ttu-id="51792-152">Valor de cadena que contiene una dirección URL que apunta a la información de esta revisión.</span><span class="sxs-lookup"><span data-stu-id="51792-152">A string value that contains a URL pointing to information for this patch.</span></span> <span data-ttu-id="51792-153">Esta propiedad obligatoria está registrada y su valor se puede obtener mediante la función <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="51792-153">This required property is registered and its value can be obtained by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="51792-154">A partir de Windows XP con Service Pack 2 (SP2), este valor puede ser el vínculo de soporte técnico de la revisión que se muestra en Agregar o quitar programas.</span><span class="sxs-lookup"><span data-stu-id="51792-154">Beginning with Windows XP with Service Pack 2 (SP2), this value can be the support link for the patch displayed in Add/Remove Programs.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51792-155">CreationTimeUTC</span><span class="sxs-lookup"><span data-stu-id="51792-155">CreationTimeUTC</span></span></td>
<td><span data-ttu-id="51792-156">Valor de cadena que contiene la hora de creación del archivo. MSP con el formato MM-DD-YY HH: MM (mes-día-año hora: minuto).</span><span class="sxs-lookup"><span data-stu-id="51792-156">A string value that contains the creation time of the .msp file in the form mm-dd-yy HH:MM (month-day-year hour:minute).</span></span> <span data-ttu-id="51792-157">Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="51792-157">This property is optional.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51792-158">DisplayName</span><span class="sxs-lookup"><span data-stu-id="51792-158">DisplayName</span></span></td>
<td><span data-ttu-id="51792-159">Valor de cadena que contiene el título de la revisión que es adecuado para la presentación pública.</span><span class="sxs-lookup"><span data-stu-id="51792-159">A string value that contains the title for the patch that is suitable for public display.</span></span> <span data-ttu-id="51792-160">Esta propiedad es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="51792-160">This property is required.</span></span> <span data-ttu-id="51792-161">Esta propiedad está registrada y su valor se puede obtener mediante la función <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="51792-161">This property is registered and its value can be obtain by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="51792-162">A partir de Windows XP con SP2, este valor es el nombre de la revisión que se muestra en Agregar o quitar programas a partir de Windows XP con SP2.</span><span class="sxs-lookup"><span data-stu-id="51792-162">Beginning with Windows XP with SP2, this value is the name of the patch displayed in Add/Remove Programs beginning with Windows XP with SP2.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51792-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="51792-163">Description</span></span></td>
<td><span data-ttu-id="51792-164">Valor de cadena que contiene una breve descripción de la revisión.</span><span class="sxs-lookup"><span data-stu-id="51792-164">A string value that contains a brief description of the patch.</span></span> <span data-ttu-id="51792-165">Esta propiedad es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="51792-165">This property is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51792-166">Clasificación</span><span class="sxs-lookup"><span data-stu-id="51792-166">Classification</span></span></td>
<td><span data-ttu-id="51792-167">Valor de cadena que contiene la categoría arbitraria de actualizaciones tal como la define el autor de la revisión.</span><span class="sxs-lookup"><span data-stu-id="51792-167">A string value that contains the arbitrary category of updates as defined by the author of the patch.</span></span> <span data-ttu-id="51792-168">Por ejemplo, los autores de revisiones pueden especificar que cada revisión se clasifique como revisión, acumulación de seguridad, actualización crítica, actualización, Service Pack o paquete acumulativo de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="51792-168">For example, patch authors can specify that each patch be classified as a Hotfix, Security Rollup, Critical Update, Update, Service Pack, or Update Rollup.</span></span> <span data-ttu-id="51792-169">Esta propiedad es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="51792-169">This property is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51792-170">OptimizedInstallMode</span><span class="sxs-lookup"><span data-stu-id="51792-170">OptimizedInstallMode</span></span></td>
<td><span data-ttu-id="51792-171">Si esta propiedad se establece en 1 (uno) en todas las revisiones que se van a aplicar en una transacción, la aplicación de la revisión se optimizará si es posible.</span><span class="sxs-lookup"><span data-stu-id="51792-171">If this property is set to 1 (one) in all the patches to be applied in a transaction, the application of the patch is optimized if possible.</span></span> <span data-ttu-id="51792-172">Para obtener más información, vea <a href="patch-optimization.md">optimización de revisiones</a>.</span><span class="sxs-lookup"><span data-stu-id="51792-172">For information, see <a href="patch-optimization.md">Patch Optimization</a>.</span></span> <span data-ttu-id="51792-173">Disponible a partir de Windows Installer 3,1.</span><span class="sxs-lookup"><span data-stu-id="51792-173">Available beginning with Windows Installer 3.1.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="51792-174"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="51792-174"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="51792-175">Valor de la propiedad de metadatos.</span><span class="sxs-lookup"><span data-stu-id="51792-175">Value of the metadata property.</span></span> <span data-ttu-id="51792-176">Nunca puede ser null ni una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="51792-176">This can never be Null or an empty string.</span></span> <span data-ttu-id="51792-177">Este valor se puede localizar.</span><span class="sxs-lookup"><span data-stu-id="51792-177">This value can be localized.</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="51792-178">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51792-178">Remarks</span></span>

<span data-ttu-id="51792-179">Disponible a partir de Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="51792-179">Available beginning in Windows Installer 3.0.</span></span>

<span data-ttu-id="51792-180">Todas las propiedades creadas en la tabla PatchMetadata se agregan a la tabla MsiPatchMetadata del archivo MSP.</span><span class="sxs-lookup"><span data-stu-id="51792-180">All properties authored into the PatchMetadata Table are added to the MsiPatchMetadata table of the msp file.</span></span> <span data-ttu-id="51792-181">Las propiedades AllowRemoval, MoreInfoURL y DisplayName se registran y son accesibles a través de [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span><span class="sxs-lookup"><span data-stu-id="51792-181">AllowRemoval, MoreInfoURL and DisplayName properties are registered and are accessible through the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span></span>

 

 




