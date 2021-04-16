---
description: En las tablas siguientes se describen las propiedades de Resumen de los paquetes de instalación, las transformaciones y las revisiones.
ms.assetid: b44b24b7-7fc4-4c3c-9d10-7e2f3c43cf36
title: Descripciones de propiedades de Resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41addb58571b6d18e1cccc4a34c3026f3d0544cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678399"
---
# <a name="summary-property-descriptions"></a><span data-ttu-id="93145-103">Descripciones de propiedades de Resumen</span><span class="sxs-lookup"><span data-stu-id="93145-103">Summary Property Descriptions</span></span>

<span data-ttu-id="93145-104">En las tablas siguientes se describen las propiedades de Resumen de los paquetes de instalación, las transformaciones y las revisiones.</span><span class="sxs-lookup"><span data-stu-id="93145-104">Summary properties for installation packages, transforms, and patches are described in the following tables.</span></span> <span data-ttu-id="93145-105">Tenga en cuenta que el significado de una propiedad de Resumen determinada puede variar en función de si la base de datos pertenece a un paquete de instalación, transformación o paquete de revisión.</span><span class="sxs-lookup"><span data-stu-id="93145-105">Note that the meaning of a particular summary property can be different depending on whether the database belongs to an installation package, transform, or patch package.</span></span> <span data-ttu-id="93145-106">Para obtener más información sobre los identificadores de propiedad, los PID y los tipos, vea [conjunto de propiedades de flujo de información de Resumen](summary-information-stream-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="93145-106">For more information about the property IDs, PIDs, and types, see [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span></span>

## <a name="installation-packages"></a><span data-ttu-id="93145-107">Paquetes de instalación</span><span class="sxs-lookup"><span data-stu-id="93145-107">Installation Packages</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93145-108">Summary (propiedad)</span><span class="sxs-lookup"><span data-stu-id="93145-108">Summary property</span></span></th>
<th><span data-ttu-id="93145-109">Significado de esta propiedad en una base de datos de instalación</span><span class="sxs-lookup"><span data-stu-id="93145-109">Meaning of this property in an Installation database</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93145-110"><a href="title-summary.md"><strong>Title</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-110"><a href="title-summary.md"><strong>Title</strong></a></span></span></td>
<td><span data-ttu-id="93145-111">Descripción de este archivo como un paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="93145-111">A description of this file as an installation package.</span></span> <span data-ttu-id="93145-112">La descripción debe incluir la frase &quot; <a href="about-the-installer-database.md">base de datos de instalación</a>.&quot;</span><span class="sxs-lookup"><span data-stu-id="93145-112">The description should include the phrase &quot;<a href="about-the-installer-database.md">Installation Database</a>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93145-113"><a href="subject-summary.md"><strong>Asunto</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-113"><a href="subject-summary.md"><strong>Subject</strong></a></span></span></td>
<td><span data-ttu-id="93145-114">Nombre del producto instalado por este paquete.</span><span class="sxs-lookup"><span data-stu-id="93145-114">The name of the product installed by this package.</span></span> <span data-ttu-id="93145-115">Debe ser el mismo nombre que en la propiedad <a href="productname.md"><strong>ProductName</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="93145-115">This should be the same name as in the <a href="productname.md"><strong>ProductName</strong></a> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93145-116"><a href="author-summary.md"><strong>Autor</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-116"><a href="author-summary.md"><strong>Author</strong></a></span></span></td>
<td><span data-ttu-id="93145-117">Nombre del fabricante de este producto.</span><span class="sxs-lookup"><span data-stu-id="93145-117">The name of the manufacturer of this product.</span></span> <span data-ttu-id="93145-118">Debe ser el mismo nombre que en la propiedad <a href="manufacturer.md"><strong>manufacturer</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="93145-118">This should be the same name as in the <a href="manufacturer.md"><strong>Manufacturer</strong></a> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93145-119"><a href="keywords-summary.md"><strong>Palabras clave</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-119"><a href="keywords-summary.md"><strong>Keywords</strong></a></span></span></td>
<td><span data-ttu-id="93145-120">Una lista de palabras clave que pueden usar los exploradores de archivos para realizar búsquedas de palabras clave para un archivo.</span><span class="sxs-lookup"><span data-stu-id="93145-120">A list of keywords that may be used by file browsers to do keyword searches for a file.</span></span> <span data-ttu-id="93145-121">Las palabras clave deben incluir el &quot; instalador &quot; y las palabras clave específicas del producto.</span><span class="sxs-lookup"><span data-stu-id="93145-121">The keywords should include &quot;Installer&quot; as well as product-specific keywords.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93145-122"><a href="comments-summary.md"><strong>Comentarios</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-122"><a href="comments-summary.md"><strong>Comments</strong></a></span></span></td>
<td><span data-ttu-id="93145-123">Contiene la frase: &quot; esta base de datos del instalador contiene la lógica y los datos necesarios para instalar <<em>nombre del producto</em> > .&quot;</span><span class="sxs-lookup"><span data-stu-id="93145-123">Contains the phrase: &quot;This installer database contains the logic and data required to install <<em>product name</em>>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93145-124"><a href="template-summary.md"><strong>Plantilla</strong></a> (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="93145-124"><a href="template-summary.md"><strong>Template</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="93145-125">La plataforma y los lenguajes compatibles con este paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="93145-125">The platform and languages compatible with this installation package.</span></span> <span data-ttu-id="93145-126">Vea la <a href="template-summary.md"><strong>plantilla</strong></a> para ver la sintaxis.</span><span class="sxs-lookup"><span data-stu-id="93145-126">See <a href="template-summary.md"><strong>Template</strong></a> for syntax.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93145-127"><a href="last-saved-by-summary.md"><strong>Guardado por última vez por</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-127"><a href="last-saved-by-summary.md"><strong>Last Saved By</strong></a></span></span></td>
<td><span data-ttu-id="93145-128">Los desarrolladores de herramientas de edición de bases de datos pueden utilizar esta propiedad durante el proceso de desarrollo para realizar un seguimiento de la última persona que modificó la base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="93145-128">Developers of database editing tools may use this property during the development process to track the last person to modify the installation database.</span></span> <span data-ttu-id="93145-129">Esta propiedad debe establecerse en null en una base de datos de envío final.</span><span class="sxs-lookup"><span data-stu-id="93145-129">This property should be set to Null in a final shipping database.</span></span> <span data-ttu-id="93145-130">El instalador establece esta propiedad en el valor de la propiedad <a href="logonuser.md"><strong>LogonUser</strong></a> durante una <a href="administrative-installation.md"><strong>instalación administrativa</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="93145-130">The installer sets this property to the value of the <a href="logonuser.md"><strong>LogonUser</strong></a> property during an <a href="administrative-installation.md"><strong>administrative installation</strong></a>.</span></span> <span data-ttu-id="93145-131">El instalador nunca usa esta propiedad y un usuario nunca necesita modificarla.</span><span class="sxs-lookup"><span data-stu-id="93145-131">The installer never uses this property and a user never needs to modify it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93145-132"><a href="revision-number-summary.md"><strong>Número de revisión</strong></a> (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="93145-132"><a href="revision-number-summary.md"><strong>Revision Number</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="93145-133">Contiene el <a href="package-codes.md">código de paquete</a> para el paquete del instalador.</span><span class="sxs-lookup"><span data-stu-id="93145-133">Contains the <a href="package-codes.md">package code</a> for the installer package.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93145-134"><a href="last-printed-summary.md"><strong>Última impresión</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-134"><a href="last-printed-summary.md"><strong>Last Printed</strong></a></span></span></td>
<td><span data-ttu-id="93145-135">Se puede establecer en la fecha y hora durante una <a href="administrative-installation.md">instalación administrativa</a> para registrar Cuándo se creó la imagen administrativa.</span><span class="sxs-lookup"><span data-stu-id="93145-135">May be set to the date and time during an <a href="administrative-installation.md">administrative installation</a> to record when the administrative image was created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93145-136"><a href="create-time-date-summary.md"><strong>Crear hora/fecha</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-136"><a href="create-time-date-summary.md"><strong>Create Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="93145-137">Fecha y hora en que se creó la base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="93145-137">The time and date when this installer database was created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93145-138"><a href="last-saved-time-date-summary.md"><strong>Fecha y hora de la última vez que se guardó</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-138"><a href="last-saved-time-date-summary.md"><strong>Last Saved Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="93145-139">Fecha y hora actuales del sistema en el momento en que se guardó por última vez la base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="93145-139">The current system time and date at the time the installer database was last saved.</span></span> <span data-ttu-id="93145-140">Inicialmente null.</span><span class="sxs-lookup"><span data-stu-id="93145-140">Initially null.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93145-141"><a href="page-count-summary.md"><strong>Recuento de páginas</strong></a> (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="93145-141"><a href="page-count-summary.md"><strong>Page Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="93145-142">Contiene un valor que se usa para identificar la versión mínima del instalador requerida por este paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="93145-142">Contains a value used to identify the minimum installer version required by this installation package.</span></span> <span data-ttu-id="93145-143">Por ejemplo, si el paquete requiere como mínimo la versión 2,0 del instalador, esta propiedad debe establecerse en un entero de 200.</span><span class="sxs-lookup"><span data-stu-id="93145-143">For example, if the package requires at minimum the 2.0 version of the installer, this property should be set to an integer of 200.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="93145-144">El valor de esta propiedad debe ser 200 o superior con <a href="64-bit-windows-installer-packages.md">paquetes de Windows Installer de 64 bits</a>.</span><span class="sxs-lookup"><span data-stu-id="93145-144">The value of this property must be 200 or greater with <a href="64-bit-windows-installer-packages.md">64-bit Windows Installer Packages</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93145-145"><a href="word-count-summary.md"><strong>Recuento de palabras</strong></a> (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="93145-145"><a href="word-count-summary.md"><strong>Word Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="93145-146">Tipo de la imagen de archivo de origen.</span><span class="sxs-lookup"><span data-stu-id="93145-146">The type of the source file image.</span></span> <span data-ttu-id="93145-147">Almacenado en lugar de la propiedad de recuento estándar.</span><span class="sxs-lookup"><span data-stu-id="93145-147">Stored in place of the standard Count property.</span></span> <span data-ttu-id="93145-148">Esta propiedad es un campo de bits.</span><span class="sxs-lookup"><span data-stu-id="93145-148">This property is a bit field.</span></span> <span data-ttu-id="93145-149">Vea el tema <a href="word-count-summary.md"><strong>recuento de palabras</strong></a> para los valores.</span><span class="sxs-lookup"><span data-stu-id="93145-149">See the <a href="word-count-summary.md"><strong>Word Count</strong></a> topic for the values.</span></span><br/> <span data-ttu-id="93145-150">A partir de Windows Installer versión 4,0 en Windows Vista, esta propiedad incluye bits para especificar si se requieren privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="93145-150">Starting with Windows Installer version 4.0 on Windows Vista, this property includes bits to specify whether elevated privileges are required.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93145-151"><a href="character-count-summary.md"><strong>Recuento de caracteres</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-151"><a href="character-count-summary.md"><strong>Character Count</strong></a></span></span></td>
<td><span data-ttu-id="93145-152">Null</span><span class="sxs-lookup"><span data-stu-id="93145-152">Null</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93145-153"><a href="creating-application-summary.md"><strong>Creando aplicación</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-153"><a href="creating-application-summary.md"><strong>Creating Application</strong></a></span></span></td>
<td><span data-ttu-id="93145-154">Contiene el nombre del software utilizado para crear esta base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="93145-154">Contains the name of the software used to author this installation database.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93145-155"><a href="security-summary.md"><strong>Seguridad</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-155"><a href="security-summary.md"><strong>Security</strong></a></span></span></td>
<td><span data-ttu-id="93145-156">El valor de esta propiedad debe ser 2 recomendado solo lectura.</span><span class="sxs-lookup"><span data-stu-id="93145-156">The value of this property should be 2 - Recommended read-only.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93145-157"><a href="codepage-summary.md"><strong>737</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-157"><a href="codepage-summary.md"><strong>Codepage</strong></a></span></span></td>
<td><span data-ttu-id="93145-158">Valor numérico de la página de códigos ANSI que se usa para mostrar la información de resumen.</span><span class="sxs-lookup"><span data-stu-id="93145-158">The numeric value of the ANSI code page used to display the Summary Information.</span></span> <span data-ttu-id="93145-159">Esta propiedad debe establecerse antes de que se establezcan las propiedades de cadena en la información de resumen.</span><span class="sxs-lookup"><span data-stu-id="93145-159">This property must be set before any string properties are set in the summary information.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="transforms"></a><span data-ttu-id="93145-160">Transformaciones</span><span class="sxs-lookup"><span data-stu-id="93145-160">Transforms</span></span>



| <span data-ttu-id="93145-161">Summary (propiedad)</span><span class="sxs-lookup"><span data-stu-id="93145-161">Summary property</span></span>                                              | <span data-ttu-id="93145-162">Significado de esta propiedad en una transformación</span><span class="sxs-lookup"><span data-stu-id="93145-162">Meaning of this property in a Transform</span></span>                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93145-163">**Title**</span><span class="sxs-lookup"><span data-stu-id="93145-163">**Title**</span></span>](title-summary.md)                                | <span data-ttu-id="93145-164">Descripción de este archivo como una transformación.</span><span class="sxs-lookup"><span data-stu-id="93145-164">A description of this file as a transform.</span></span> <span data-ttu-id="93145-165">La descripción debe incluir la frase: "[Transform](database-transforms.md)".</span><span class="sxs-lookup"><span data-stu-id="93145-165">The description should include the phrase: "[Transform](database-transforms.md)."</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="93145-166">**Asunto**</span><span class="sxs-lookup"><span data-stu-id="93145-166">**Subject**</span></span>](subject-summary.md)                            | <span data-ttu-id="93145-167">Nombre del producto instalado por el paquete de instalación original.</span><span class="sxs-lookup"><span data-stu-id="93145-167">The name of the product installed by the original installation package.</span></span> <span data-ttu-id="93145-168">Debe ser el mismo valor que la propiedad de [**Resumen del asunto**](subject-summary.md) en el paquete de instalación original.</span><span class="sxs-lookup"><span data-stu-id="93145-168">This should be the same value as the [**Subject Summary**](subject-summary.md) property in the original installation package.</span></span>                                                                                            |
| [<span data-ttu-id="93145-169">**Autor**</span><span class="sxs-lookup"><span data-stu-id="93145-169">**Author**</span></span>](author-summary.md)                              | <span data-ttu-id="93145-170">Nombre del fabricante de esta transformación.</span><span class="sxs-lookup"><span data-stu-id="93145-170">The name of the manufacturer of this transform.</span></span>                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="93145-171">**Palabras clave**</span><span class="sxs-lookup"><span data-stu-id="93145-171">**Keywords**</span></span>](keywords-summary.md)                          | <span data-ttu-id="93145-172">Una lista de palabras clave que pueden usar los exploradores de archivos para realizar búsquedas de palabras clave para un archivo.</span><span class="sxs-lookup"><span data-stu-id="93145-172">A list of keywords that may be used by file browsers to do keyword searches for a file.</span></span> <span data-ttu-id="93145-173">Las palabras clave deben incluir "Installer", así como palabras clave específicas del producto.</span><span class="sxs-lookup"><span data-stu-id="93145-173">The keywords should include "Installer" as well as product-specific keywords.</span></span>                                                                                                                             |
| [<span data-ttu-id="93145-174">**Comentarios**</span><span class="sxs-lookup"><span data-stu-id="93145-174">**Comments**</span></span>](comments-summary.md)                          | <span data-ttu-id="93145-175">Contiene la frase: "esta transformación contiene la lógica y los datos necesarios para instalar <*nombre de producto*>".</span><span class="sxs-lookup"><span data-stu-id="93145-175">Contains the phrase: "This transform contains the logic and data required to install <*product name*>."</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="93145-176">[**Plantilla**](template-summary.md) (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="93145-176">[**Template**](template-summary.md) (REQUIRED)</span></span>               | <span data-ttu-id="93145-177">Versiones de plataforma e idioma compatibles con esta transformación.</span><span class="sxs-lookup"><span data-stu-id="93145-177">The platform and language versions compatible with this transform.</span></span> <span data-ttu-id="93145-178">Este valor puede dejarse en blanco si no hay ninguna restricción.</span><span class="sxs-lookup"><span data-stu-id="93145-178">This value may be left blank if there are no restrictions.</span></span> <span data-ttu-id="93145-179">Solo se puede especificar un idioma para una transformación.</span><span class="sxs-lookup"><span data-stu-id="93145-179">Only one language can be specified for a transform.</span></span> <span data-ttu-id="93145-180">Para obtener más información sobre la sintaxis, consulte [**Template**](template-summary.md).</span><span class="sxs-lookup"><span data-stu-id="93145-180">For more information about the syntax, see [**Template**](template-summary.md).</span></span>                                |
| [<span data-ttu-id="93145-181">**Guardado por última vez por**</span><span class="sxs-lookup"><span data-stu-id="93145-181">**Last Saved By**</span></span>](last-saved-by-summary.md)                | <span data-ttu-id="93145-182">Los IDENTIFICADOres de plataforma e idioma que tiene la base de datos una vez transformada.</span><span class="sxs-lookup"><span data-stu-id="93145-182">The platform and language ID(s) that the database has after it has been transformed.</span></span> <span data-ttu-id="93145-183">La propiedad de [**Resumen de plantilla**](template-summary.md) de la nueva base de datos debe establecerse en los mismos valores.</span><span class="sxs-lookup"><span data-stu-id="93145-183">The [**Template Summary**](template-summary.md) property in the new database should be set to the same values.</span></span>                                                                                              |
| <span data-ttu-id="93145-184">[**Número de revisión**](revision-number-summary.md) (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="93145-184">[**Revision Number**](revision-number-summary.md) (REQUIRED)</span></span> | <span data-ttu-id="93145-185">Una lista de los GUID de código de producto y la versión de los productos nuevos y originales y el GUID del código de actualización.</span><span class="sxs-lookup"><span data-stu-id="93145-185">A list of the product code GUIDs and version of the new and original products and the upgrade code GUID.</span></span> <span data-ttu-id="93145-186">La lista está separada por punto y coma como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="93145-186">The list is separated by semicolons as follows.</span></span> <span data-ttu-id="93145-187">*Original-Product-Code original-Product-version*; *New-Product Code New-Product-version*; *Actualización: código*</span><span class="sxs-lookup"><span data-stu-id="93145-187">*Original-Product-Code Original-Product-Version*;*New-Product Code New-Product-Version*; *Upgrade-Code*</span></span><br/>                       |
| [<span data-ttu-id="93145-188">**Última impresión**</span><span class="sxs-lookup"><span data-stu-id="93145-188">**Last Printed**</span></span>](last-printed-summary.md)                  | <span data-ttu-id="93145-189">Null</span><span class="sxs-lookup"><span data-stu-id="93145-189">Null</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="93145-190">**Crear hora/fecha**</span><span class="sxs-lookup"><span data-stu-id="93145-190">**Create Time/Date**</span></span>](create-time-date-summary.md)          | <span data-ttu-id="93145-191">Fecha y hora en que se creó la transformación.</span><span class="sxs-lookup"><span data-stu-id="93145-191">The time and date when the transform was created.</span></span>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="93145-192">**Fecha y hora de la última vez que se guardó**</span><span class="sxs-lookup"><span data-stu-id="93145-192">**Last Saved Time/Date**</span></span>](last-saved-time-date-summary.md)  | <span data-ttu-id="93145-193">Fecha y hora actuales del sistema en el momento en que se guardó la transformación.</span><span class="sxs-lookup"><span data-stu-id="93145-193">The current system time and date at the time the transform was saved.</span></span> <span data-ttu-id="93145-194">Inicialmente null.</span><span class="sxs-lookup"><span data-stu-id="93145-194">Initially null.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="93145-195">[**Recuento de páginas**](page-count-summary.md) (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="93145-195">[**Page Count**](page-count-summary.md) (REQUIRED)</span></span>           | <span data-ttu-id="93145-196">Valor que se usa para indicar la versión mínima del instalador necesaria para procesar la transformación.</span><span class="sxs-lookup"><span data-stu-id="93145-196">A value used to indicate the minimum installer version required to process the transform.</span></span> <span data-ttu-id="93145-197">El valor se debe establecer en el mayor de los dos valores de propiedad de [**recuento de páginas**](page-count-summary.md) que pertenecen a las bases de datos utilizadas para generar la transformación.</span><span class="sxs-lookup"><span data-stu-id="93145-197">The value should be set to the greater of the two [**Page Count**](page-count-summary.md) property values that belong to the databases used to generate the transform.</span></span>                                 |
| <span data-ttu-id="93145-198">[**Recuento de palabras**](word-count-summary.md) (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="93145-198">[**Word Count**](word-count-summary.md) (REQUIRED)</span></span>           | <span data-ttu-id="93145-199">Null</span><span class="sxs-lookup"><span data-stu-id="93145-199">Null</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="93145-200">**Recuento de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93145-200">**Character Count**</span></span>](character-count-summary.md)            | <span data-ttu-id="93145-201">Esta parte de la secuencia de información de resumen se divide en palabras de 2 16 bits.</span><span class="sxs-lookup"><span data-stu-id="93145-201">This part of the summary information stream is divided into two 16-bit words.</span></span> <span data-ttu-id="93145-202">La palabra superior contiene [*marcas de validación de transformación*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="93145-202">The upper word contains [*transform validation flags*](t-gly.md).</span></span> <span data-ttu-id="93145-203">La palabra inferior contiene [*marcas de condición de error de transformación*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="93145-203">Lower word contains [*transform error condition flags*](t-gly.md).</span></span> |
| [<span data-ttu-id="93145-204">**Creando aplicación**</span><span class="sxs-lookup"><span data-stu-id="93145-204">**Creating Application**</span></span>](creating-application-summary.md)  | <span data-ttu-id="93145-205">Contiene el nombre del software utilizado para crear esta transformación.</span><span class="sxs-lookup"><span data-stu-id="93145-205">Contains the name of the software used to create this transform.</span></span>                                                                                                                                                                                                                                  |
| [<span data-ttu-id="93145-206">**Seguridad**</span><span class="sxs-lookup"><span data-stu-id="93145-206">**Security**</span></span>](security-summary.md)                          | <span data-ttu-id="93145-207">El valor de esta propiedad debe ser de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="93145-207">The value of this property should be 4 - Enforced read-only.</span></span>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="93145-208">**737**</span><span class="sxs-lookup"><span data-stu-id="93145-208">**Codepage**</span></span>](codepage-summary.md)                          | <span data-ttu-id="93145-209">Valor numérico de la página de códigos ANSI que se usa para mostrar la información de resumen.</span><span class="sxs-lookup"><span data-stu-id="93145-209">The numeric value of the ANSI code page used to display the Summary Information.</span></span> <span data-ttu-id="93145-210">Esta propiedad debe establecerse antes de que se puedan establecer las propiedades de cadena en la información de resumen.</span><span class="sxs-lookup"><span data-stu-id="93145-210">This property must be set before any string properties can be set in the summary information.</span></span>                                                                                                                    |



 

## <a name="patch-packages"></a><span data-ttu-id="93145-211">Paquetes de revisión</span><span class="sxs-lookup"><span data-stu-id="93145-211">Patch Packages</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93145-212">Summary (propiedad)</span><span class="sxs-lookup"><span data-stu-id="93145-212">Summary property</span></span></th>
<th><span data-ttu-id="93145-213">Significado de esta propiedad en un paquete de revisión</span><span class="sxs-lookup"><span data-stu-id="93145-213">Meaning of this property in a Patch package</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93145-214"><a href="title-summary.md"><strong>Title</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-214"><a href="title-summary.md"><strong>Title</strong></a></span></span></td>
<td><span data-ttu-id="93145-215">Una descripción de este archivo como un paquete de revisión.</span><span class="sxs-lookup"><span data-stu-id="93145-215">A description of this file as a patch package.</span></span> <span data-ttu-id="93145-216">La descripción debe incluir la frase: &quot; <a href="patch-packages.md">patch</a>.&quot;</span><span class="sxs-lookup"><span data-stu-id="93145-216">The description should include the phrase: &quot;<a href="patch-packages.md">Patch</a>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93145-217"><a href="subject-summary.md"><strong>Asunto</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-217"><a href="subject-summary.md"><strong>Subject</strong></a></span></span></td>
<td><span data-ttu-id="93145-218">Una descripción de la revisión que incluye el nombre del producto.</span><span class="sxs-lookup"><span data-stu-id="93145-218">A description of the patch that includes the name of the product.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93145-219"><a href="author-summary.md"><strong>Autor</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-219"><a href="author-summary.md"><strong>Author</strong></a></span></span></td>
<td><span data-ttu-id="93145-220">Nombre del fabricante del paquete de revisión.</span><span class="sxs-lookup"><span data-stu-id="93145-220">The name of the manufacturer of the patch package.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93145-221"><a href="keywords-summary.md"><strong>Palabras clave</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-221"><a href="keywords-summary.md"><strong>Keywords</strong></a></span></span></td>
<td><span data-ttu-id="93145-222">Una lista delimitada por punto y coma de orígenes de la revisión.</span><span class="sxs-lookup"><span data-stu-id="93145-222">A semicolon delimited list of sources of the patch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93145-223"><a href="comments-summary.md"><strong>Comentarios</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-223"><a href="comments-summary.md"><strong>Comments</strong></a></span></span></td>
<td><span data-ttu-id="93145-224">Contiene la frase: &quot; esta revisión contiene la lógica y los datos necesarios para instalar <<em>nombre del producto</em> > .&quot;</span><span class="sxs-lookup"><span data-stu-id="93145-224">Contains the phrase: &quot;This patch contains the logic and data required to install <<em>product name</em>>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93145-225"><a href="template-summary.md"><strong>Plantilla</strong></a> (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="93145-225"><a href="template-summary.md"><strong>Template</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="93145-226">Una lista delimitada por punto y coma de los códigos de producto que pueden aceptar esta revisión.</span><span class="sxs-lookup"><span data-stu-id="93145-226">A semicolon delimited list of the product codes that can accept this patch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93145-227"><a href="last-saved-by-summary.md"><strong>Guardado por última vez por</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-227"><a href="last-saved-by-summary.md"><strong>Last Saved By</strong></a></span></span></td>
<td><span data-ttu-id="93145-228">Una lista delimitada por punto y coma de nombres de subalmacenamiento de transformación en el orden en que se aplican en esta revisión.</span><span class="sxs-lookup"><span data-stu-id="93145-228">A semicolon delimited list of transform substorage names in the order they are applied by this patch.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93145-229"><a href="revision-number-summary.md"><strong>Número de revisión</strong></a> (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="93145-229"><a href="revision-number-summary.md"><strong>Revision Number</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="93145-230">Contiene el código de revisión del GUID de la revisión.</span><span class="sxs-lookup"><span data-stu-id="93145-230">Contains the GUID patch code for the patch.</span></span> <span data-ttu-id="93145-231">Esto puede ir seguido de una lista de GUID de código de revisión para las revisiones que se quitan cuando se aplica esta revisión.</span><span class="sxs-lookup"><span data-stu-id="93145-231">This may be followed by a list of patch code GUIDs for patches that are removed when this patch is applied.</span></span> <span data-ttu-id="93145-232">Los códigos de revisión se concatenan sin delimitadores que separan los GUID de la lista.</span><span class="sxs-lookup"><span data-stu-id="93145-232">The patch codes are concatenated with no delimiters separating GUIDs in the list.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="93145-233">Si el paquete de revisión contiene una tabla <a href="msipatchsequence-table.md"><strong>MsiPatchSequence</strong></a> , la revisión no quita las revisiones enumeradas después del GUID de la revisión actual.</span><span class="sxs-lookup"><span data-stu-id="93145-233">If the patch package contains a <a href="msipatchsequence-table.md"><strong>MsiPatchSequence</strong></a> table, the patch does not remove patches listed after the current patch's GUID.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93145-234"><a href="last-printed-summary.md"><strong>Última impresión</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-234"><a href="last-printed-summary.md"><strong>Last Printed</strong></a></span></span></td>
<td><span data-ttu-id="93145-235">Null</span><span class="sxs-lookup"><span data-stu-id="93145-235">Null</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93145-236"><a href="create-time-date-summary.md"><strong>Crear hora/fecha</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-236"><a href="create-time-date-summary.md"><strong>Create Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="93145-237">Fecha y hora en que se creó el archivo de revisión.</span><span class="sxs-lookup"><span data-stu-id="93145-237">The time and date when patch file was created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93145-238"><a href="last-saved-time-date-summary.md"><strong>Fecha y hora de la última vez que se guardó</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-238"><a href="last-saved-time-date-summary.md"><strong>Last Saved Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="93145-239">Fecha y hora actuales del sistema en el momento en que se guardó el paquete de revisión.</span><span class="sxs-lookup"><span data-stu-id="93145-239">The current system time and date at the time the patch package was saved.</span></span> <span data-ttu-id="93145-240">Este valor es inicialmente null.</span><span class="sxs-lookup"><span data-stu-id="93145-240">This value is initially null.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93145-241"><a href="page-count-summary.md"><strong>Recuento de páginas</strong></a> (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="93145-241"><a href="page-count-summary.md"><strong>Page Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="93145-242">Null</span><span class="sxs-lookup"><span data-stu-id="93145-242">Null</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93145-243"><a href="word-count-summary.md"><strong>Recuento de palabras</strong></a> (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="93145-243"><a href="word-count-summary.md"><strong>Word Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="93145-244">Contiene un valor que indica la versión mínima Windows Installer necesaria para instalar la revisión.</span><span class="sxs-lookup"><span data-stu-id="93145-244">Contains a value that indicates the minimum Windows Installer version that is required to install the patch.</span></span> <span data-ttu-id="93145-245">Una revisión con un valor de recuento de palabras de 4 requiere Windows Installer versión 3,0 o posterior para que se aplique la revisión.</span><span class="sxs-lookup"><span data-stu-id="93145-245">A patch with a word count value of 4 requires Windows Installer version 3.0 or higher for the patch to be applied.</span></span> <span data-ttu-id="93145-246">Un valor de 3 indica que se requiere Windows Installer versión 2,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="93145-246">A value of 3 indicates that Windows Installer version 2.0 or higher is required.</span></span> <span data-ttu-id="93145-247">Un valor de 2 indica que se requiere Windows Installer versión 1,2 o posterior.</span><span class="sxs-lookup"><span data-stu-id="93145-247">A value of 2 indicates that Windows Installer version 1.2 or higher is required.</span></span> <span data-ttu-id="93145-248">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="93145-248">The default value is 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93145-249"><a href="character-count-summary.md"><strong>Recuento de caracteres</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-249"><a href="character-count-summary.md"><strong>Character Count</strong></a></span></span></td>
<td><span data-ttu-id="93145-250">Null</span><span class="sxs-lookup"><span data-stu-id="93145-250">Null</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93145-251"><a href="creating-application-summary.md"><strong>Creando aplicación</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-251"><a href="creating-application-summary.md"><strong>Creating Application</strong></a></span></span></td>
<td><span data-ttu-id="93145-252">Nombre del software que se usa para crear la revisión.</span><span class="sxs-lookup"><span data-stu-id="93145-252">The name of the software used to create the patch.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93145-253"><a href="security-summary.md"><strong>Seguridad</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-253"><a href="security-summary.md"><strong>Security</strong></a></span></span></td>
<td><span data-ttu-id="93145-254">El valor de esta propiedad debe ser de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="93145-254">The value of this property should be 4 - Enforced read-only.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93145-255"><a href="codepage-summary.md"><strong>737</strong></a></span><span class="sxs-lookup"><span data-stu-id="93145-255"><a href="codepage-summary.md"><strong>Codepage</strong></a></span></span></td>
<td><span data-ttu-id="93145-256">Valor numérico de la página de códigos ANSI que se usa para mostrar la información de resumen.</span><span class="sxs-lookup"><span data-stu-id="93145-256">The numeric value of the ANSI code page used to display the Summary Information.</span></span> <span data-ttu-id="93145-257">Esta propiedad debe establecerse antes de que se establezcan las propiedades de cadena en la información de resumen.</span><span class="sxs-lookup"><span data-stu-id="93145-257">This property must be set before any string properties are set in the summary information.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




