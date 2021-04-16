---
description: Errores de representación
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: Errores de representación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e106a55363bf50e49a4966600662e26b03b53307
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495430"
---
# <a name="rendering-errors"></a><span data-ttu-id="bd55e-103">Errores de representación</span><span class="sxs-lookup"><span data-stu-id="bd55e-103">Rendering Errors</span></span>

> [!Note]  
> <span data-ttu-id="bd55e-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="bd55e-104">\[Deprecated.</span></span> <span data-ttu-id="bd55e-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bd55e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bd55e-106">Microsoft® DirectShow® Editing Services (DES) define varios códigos de error que se usan para registrar los errores de representación.</span><span class="sxs-lookup"><span data-stu-id="bd55e-106">Microsoft® DirectShow® Editing Services (DES) defines various error codes used to log rendering errors.</span></span> <span data-ttu-id="bd55e-107">Si un proyecto no se representa correctamente, el motor de representación llama al método [**IAMErrorLog:: LogError**](iamerrorlog-logerror.md) .</span><span class="sxs-lookup"><span data-stu-id="bd55e-107">If a project does not render correctly, the render engine calls the [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) method.</span></span> <span data-ttu-id="bd55e-108">En la tabla siguiente se resumen los parámetros proporcionados a **LogError**:</span><span class="sxs-lookup"><span data-stu-id="bd55e-108">The following table summarizes the parameters given to **LogError**:</span></span>

-   <span data-ttu-id="bd55e-109">El código de error se encuentra en el parámetro *ErrorCode* .</span><span class="sxs-lookup"><span data-stu-id="bd55e-109">The error code is contained in the *ErrorCode* parameter.</span></span>
-   <span data-ttu-id="bd55e-110">La descripción se incluye en el parámetro ErrorString.</span><span class="sxs-lookup"><span data-stu-id="bd55e-110">The description is contained in the ErrorString parameter.</span></span>
-   <span data-ttu-id="bd55e-111">La descripción se incluye en el parámetro *ErrorString* .</span><span class="sxs-lookup"><span data-stu-id="bd55e-111">The description is contained in the *ErrorString* parameter.</span></span>
-   <span data-ttu-id="bd55e-112">Si hay información adicional, el tipo **Variant** se incluye en el miembro **VT** de la **variante** a la que apunta *pExtraInfo*.</span><span class="sxs-lookup"><span data-stu-id="bd55e-112">If there is extra information, the **VARIANT** type is contained in the **vt** member of the **VARIANT** pointed to by *pExtraInfo*.</span></span>

> [!Note]  
> <span data-ttu-id="bd55e-113">Los códigos de error que se describen aquí no son valores **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bd55e-113">The error codes described here are not **HRESULT** values.</span></span> <span data-ttu-id="bd55e-114">Para obtener una lista de valores devueltos **HRESULT** específicos de des, vea [códigos de error y de éxito](error-and-success-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bd55e-114">For a list of **HRESULT** return values specific to DES, see [Error and Success Codes](error-and-success-codes.md).</span></span>

 



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd55e-115">Código de error</span><span class="sxs-lookup"><span data-stu-id="bd55e-115">Error code</span></span></th>
<th><span data-ttu-id="bd55e-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd55e-116">Description</span></span></th>
<th><span data-ttu-id="bd55e-117">Información adicional</span><span class="sxs-lookup"><span data-stu-id="bd55e-117">Extra information</span></span></th>
<th><span data-ttu-id="bd55e-118">Tipo Variant</span><span class="sxs-lookup"><span data-stu-id="bd55e-118">Variant type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bd55e-119">DEX_IDS_BAD_SOURCE_NAME</span><span class="sxs-lookup"><span data-stu-id="bd55e-119">DEX_IDS_BAD_SOURCE_NAME</span></span></td>
<td><span data-ttu-id="bd55e-120">El nombre de archivo no existe o DirectShow no reconoce la extensión de archivo.</span><span class="sxs-lookup"><span data-stu-id="bd55e-120">File name doesn't exist, or DirectShow doesn't recognize the file extension.</span></span></td>
<td><span data-ttu-id="bd55e-121">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="bd55e-121">File name</span></span></td>
<td><span data-ttu-id="bd55e-122"><strong>UTILICEN</strong></span><span class="sxs-lookup"><span data-stu-id="bd55e-122"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd55e-123">DEX_IDS_BAD_SOURCE_NAME2</span><span class="sxs-lookup"><span data-stu-id="bd55e-123">DEX_IDS_BAD_SOURCE_NAME2</span></span></td>
<td><span data-ttu-id="bd55e-124">El tipo de archivo no coincide con la extensión de archivo o el archivo está dañado.</span><span class="sxs-lookup"><span data-stu-id="bd55e-124">File type does not match the file extension or the file is corrupt.</span></span></td>
<td><span data-ttu-id="bd55e-125">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="bd55e-125">File name</span></span></td>
<td><span data-ttu-id="bd55e-126"><strong>UTILICEN</strong></span><span class="sxs-lookup"><span data-stu-id="bd55e-126"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd55e-127">DEX_IDS_MISSING_SOURCE_NAME</span><span class="sxs-lookup"><span data-stu-id="bd55e-127">DEX_IDS_MISSING_SOURCE_NAME</span></span></td>
<td><span data-ttu-id="bd55e-128">Se necesita el nombre de archivo, pero no se proporcionó.</span><span class="sxs-lookup"><span data-stu-id="bd55e-128">File name was required, but wasn't given.</span></span></td>
<td><span data-ttu-id="bd55e-129">None</span><span class="sxs-lookup"><span data-stu-id="bd55e-129">None</span></span></td>
<td><span data-ttu-id="bd55e-130">No aplicable</span><span class="sxs-lookup"><span data-stu-id="bd55e-130">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd55e-131">DEX_IDS_UNKNOWN_SOURCE</span><span class="sxs-lookup"><span data-stu-id="bd55e-131">DEX_IDS_UNKNOWN_SOURCE</span></span></td>
<td><span data-ttu-id="bd55e-132">No se puede analizar el origen de datos proporcionado por este origen.</span><span class="sxs-lookup"><span data-stu-id="bd55e-132">Cannot parse data source provided by this source.</span></span></td>
<td><span data-ttu-id="bd55e-133">None</span><span class="sxs-lookup"><span data-stu-id="bd55e-133">None</span></span></td>
<td><span data-ttu-id="bd55e-134">No aplicable</span><span class="sxs-lookup"><span data-stu-id="bd55e-134">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd55e-135">DEX_IDS_INSTALL_PROBLEM</span><span class="sxs-lookup"><span data-stu-id="bd55e-135">DEX_IDS_INSTALL_PROBLEM</span></span></td>
<td><span data-ttu-id="bd55e-136">error inesperado.</span><span class="sxs-lookup"><span data-stu-id="bd55e-136">Unexpected error.</span></span> <span data-ttu-id="bd55e-137">Algunos componentes de DirectShow no están instalados correctamente.</span><span class="sxs-lookup"><span data-stu-id="bd55e-137">Some DirectShow component is not installed properly.</span></span></td>
<td><span data-ttu-id="bd55e-138">None</span><span class="sxs-lookup"><span data-stu-id="bd55e-138">None</span></span></td>
<td><span data-ttu-id="bd55e-139">No aplicable</span><span class="sxs-lookup"><span data-stu-id="bd55e-139">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd55e-140">DEX_IDS_NO_SOURCE_NAMES</span><span class="sxs-lookup"><span data-stu-id="bd55e-140">DEX_IDS_NO_SOURCE_NAMES</span></span></td>
<td><span data-ttu-id="bd55e-141">El filtro de origen no acepta nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="bd55e-141">Source filter does not accept file names.</span></span></td>
<td><span data-ttu-id="bd55e-142">None</span><span class="sxs-lookup"><span data-stu-id="bd55e-142">None</span></span></td>
<td><span data-ttu-id="bd55e-143">No aplicable</span><span class="sxs-lookup"><span data-stu-id="bd55e-143">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd55e-144">DEX_IDS_BAD_MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="bd55e-144">DEX_IDS_BAD_MEDIATYPE</span></span></td>
<td><span data-ttu-id="bd55e-145">No se admite el tipo de medio del grupo.</span><span class="sxs-lookup"><span data-stu-id="bd55e-145">Group's media type is not supported.</span></span></td>
<td><span data-ttu-id="bd55e-146">Número de grupo</span><span class="sxs-lookup"><span data-stu-id="bd55e-146">Group number</span></span></td>
<td><span data-ttu-id="bd55e-147"><strong>int</strong></span><span class="sxs-lookup"><span data-stu-id="bd55e-147"><strong>int</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd55e-148">DEX_IDS_STREAM_NUMBER</span><span class="sxs-lookup"><span data-stu-id="bd55e-148">DEX_IDS_STREAM_NUMBER</span></span></td>
<td><span data-ttu-id="bd55e-149">Número de secuencia no válido para este origen.</span><span class="sxs-lookup"><span data-stu-id="bd55e-149">Invalid stream number for this source.</span></span></td>
<td><span data-ttu-id="bd55e-150">Número de secuencia</span><span class="sxs-lookup"><span data-stu-id="bd55e-150">Stream number</span></span></td>
<td><span data-ttu-id="bd55e-151"><strong>int</strong></span><span class="sxs-lookup"><span data-stu-id="bd55e-151"><strong>int</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd55e-152">DEX_IDS_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="bd55e-152">DEX_IDS_OUTOFMEMORY</span></span></td>
<td><span data-ttu-id="bd55e-153">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="bd55e-153">Out of memory.</span></span></td>
<td><span data-ttu-id="bd55e-154">None</span><span class="sxs-lookup"><span data-stu-id="bd55e-154">None</span></span></td>
<td><span data-ttu-id="bd55e-155">No aplicable</span><span class="sxs-lookup"><span data-stu-id="bd55e-155">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd55e-156">DEX_IDS_DIBSEQ_NOTALLSAME</span><span class="sxs-lookup"><span data-stu-id="bd55e-156">DEX_IDS_DIBSEQ_NOTALLSAME</span></span></td>
<td><span data-ttu-id="bd55e-157">Un mapa de bits de la secuencia no es del mismo tipo que los demás.</span><span class="sxs-lookup"><span data-stu-id="bd55e-157">One bitmap in the sequence was not the same type as the others.</span></span></td>
<td><span data-ttu-id="bd55e-158">Nombre del mapa de bits</span><span class="sxs-lookup"><span data-stu-id="bd55e-158">Bitmap name</span></span></td>
<td><span data-ttu-id="bd55e-159"><strong>UTILICEN</strong></span><span class="sxs-lookup"><span data-stu-id="bd55e-159"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd55e-160">DEX_IDS_CLIPTOOSHORT</span><span class="sxs-lookup"><span data-stu-id="bd55e-160">DEX_IDS_CLIPTOOSHORT</span></span></td>
<td><span data-ttu-id="bd55e-161">Las horas de medios del clip no son válidas o la secuencia de mapa de bits independiente del dispositivo (DIB) es demasiado corta.</span><span class="sxs-lookup"><span data-stu-id="bd55e-161">Clip's media times are invalid, or the device-independent bitmap (DIB) sequence is too short.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="bd55e-162">Si se producen otros errores de representación, este error puede producirse aunque las horas de los medios sean válidas.</span><span class="sxs-lookup"><span data-stu-id="bd55e-162">If other rendering errors occur, this error might occur even though the media times are valid.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="bd55e-163">None</span><span class="sxs-lookup"><span data-stu-id="bd55e-163">None</span></span></td>
<td><span data-ttu-id="bd55e-164">No aplicable</span><span class="sxs-lookup"><span data-stu-id="bd55e-164">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd55e-165">DEX_IDS_INVALID_DXT</span><span class="sxs-lookup"><span data-stu-id="bd55e-165">DEX_IDS_INVALID_DXT</span></span></td>
<td><span data-ttu-id="bd55e-166">El identificador de clase (CLSID) del efecto o la transición no es válido.</span><span class="sxs-lookup"><span data-stu-id="bd55e-166">Class identifier (CLSID) of the effect or transition is not valid.</span></span></td>
<td><span data-ttu-id="bd55e-167">CLSID</span><span class="sxs-lookup"><span data-stu-id="bd55e-167">CLSID</span></span></td>
<td><span data-ttu-id="bd55e-168"><strong>UTILICEN</strong></span><span class="sxs-lookup"><span data-stu-id="bd55e-168"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd55e-169">DEX_IDS_INVALID_DEFAULT_DXT</span><span class="sxs-lookup"><span data-stu-id="bd55e-169">DEX_IDS_INVALID_DEFAULT_DXT</span></span></td>
<td><span data-ttu-id="bd55e-170">El CLSID del efecto o transición predeterminados no es válido.</span><span class="sxs-lookup"><span data-stu-id="bd55e-170">The CLSID of the default effect or transition is not valid.</span></span></td>
<td><span data-ttu-id="bd55e-171">CLSID</span><span class="sxs-lookup"><span data-stu-id="bd55e-171">CLSID</span></span></td>
<td><span data-ttu-id="bd55e-172"><strong>UTILICEN</strong></span><span class="sxs-lookup"><span data-stu-id="bd55e-172"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd55e-173">DEX_IDS_NO_3D</span><span class="sxs-lookup"><span data-stu-id="bd55e-173">DEX_IDS_NO_3D</span></span></td>
<td><span data-ttu-id="bd55e-174">Su versión de DirectX no admite transiciones tridimensionales.</span><span class="sxs-lookup"><span data-stu-id="bd55e-174">Your version of DirectX does not support three-dimensional transitions.</span></span></td>
<td><span data-ttu-id="bd55e-175">CLSID</span><span class="sxs-lookup"><span data-stu-id="bd55e-175">CLSID</span></span></td>
<td><span data-ttu-id="bd55e-176"><strong>UTILICEN</strong></span><span class="sxs-lookup"><span data-stu-id="bd55e-176"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd55e-177">DEX_IDS_BROKEN_DXT</span><span class="sxs-lookup"><span data-stu-id="bd55e-177">DEX_IDS_BROKEN_DXT</span></span></td>
<td><span data-ttu-id="bd55e-178">Este efecto no es el tipo correcto o está roto.</span><span class="sxs-lookup"><span data-stu-id="bd55e-178">This effect is not the right kind, or is broken.</span></span></td>
<td><span data-ttu-id="bd55e-179">CLSID</span><span class="sxs-lookup"><span data-stu-id="bd55e-179">CLSID</span></span></td>
<td><span data-ttu-id="bd55e-180"><strong>UTILICEN</strong></span><span class="sxs-lookup"><span data-stu-id="bd55e-180"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd55e-181">DEX_IDS_NO_SUCH_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="bd55e-181">DEX_IDS_NO_SUCH_PROPERTY</span></span></td>
<td><span data-ttu-id="bd55e-182">No existe ninguna propiedad de este tipo en el objeto.</span><span class="sxs-lookup"><span data-stu-id="bd55e-182">No such property exists on the object.</span></span></td>
<td><span data-ttu-id="bd55e-183">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="bd55e-183">Property name</span></span></td>
<td><span data-ttu-id="bd55e-184"><strong>UTILICEN</strong></span><span class="sxs-lookup"><span data-stu-id="bd55e-184"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd55e-185">DEX_IDS_ILLEGAL_PROPERTY_VAL</span><span class="sxs-lookup"><span data-stu-id="bd55e-185">DEX_IDS_ILLEGAL_PROPERTY_VAL</span></span></td>
<td><span data-ttu-id="bd55e-186">Valor no válido para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="bd55e-186">Illegal value for this property.</span></span></td>
<td><span data-ttu-id="bd55e-187">Valor especificado</span><span class="sxs-lookup"><span data-stu-id="bd55e-187">Value specified</span></span></td>
<td><span data-ttu-id="bd55e-188"><strong>VARIANTE</strong></span><span class="sxs-lookup"><span data-stu-id="bd55e-188"><strong>VARIANT</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd55e-189">DEX_IDS_INVALID_XML</span><span class="sxs-lookup"><span data-stu-id="bd55e-189">DEX_IDS_INVALID_XML</span></span></td>
<td><span data-ttu-id="bd55e-190">Error de sintaxis en el archivo XML.</span><span class="sxs-lookup"><span data-stu-id="bd55e-190">Syntax error in XML file.</span></span></td>
<td><span data-ttu-id="bd55e-191">Número de línea</span><span class="sxs-lookup"><span data-stu-id="bd55e-191">Line number</span></span></td>
<td><span data-ttu-id="bd55e-192">VT_I4 (entero de 4 bytes)</span><span class="sxs-lookup"><span data-stu-id="bd55e-192">VT_I4 (4-byte integer)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd55e-193">DEX_IDS_CANT_FIND_FILTER</span><span class="sxs-lookup"><span data-stu-id="bd55e-193">DEX_IDS_CANT_FIND_FILTER</span></span></td>
<td><span data-ttu-id="bd55e-194">No se puede encontrar el filtro especificado en XML por categoría e instancia.</span><span class="sxs-lookup"><span data-stu-id="bd55e-194">Cannot find filter specified in XML by category and instance.</span></span></td>
<td><span data-ttu-id="bd55e-195">Nombre descriptivo (instancia)</span><span class="sxs-lookup"><span data-stu-id="bd55e-195">Friendly name (instance)</span></span></td>
<td><span data-ttu-id="bd55e-196"><strong>UTILICEN</strong></span><span class="sxs-lookup"><span data-stu-id="bd55e-196"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd55e-197">DEX_IDS_DISK_WRITE_ERROR</span><span class="sxs-lookup"><span data-stu-id="bd55e-197">DEX_IDS_DISK_WRITE_ERROR</span></span></td>
<td><span data-ttu-id="bd55e-198">Error al escribir el archivo XML en el disco.</span><span class="sxs-lookup"><span data-stu-id="bd55e-198">Error writing XML file to disk.</span></span></td>
<td><span data-ttu-id="bd55e-199">None</span><span class="sxs-lookup"><span data-stu-id="bd55e-199">None</span></span></td>
<td><span data-ttu-id="bd55e-200">No aplicable</span><span class="sxs-lookup"><span data-stu-id="bd55e-200">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd55e-201">DEX_IDS_INVALID_AUDIO_FX</span><span class="sxs-lookup"><span data-stu-id="bd55e-201">DEX_IDS_INVALID_AUDIO_FX</span></span></td>
<td><span data-ttu-id="bd55e-202">CLSID no es un filtro válido de efecto de audio de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="bd55e-202">CLSID not a valid DirectShow audio effect filter.</span></span></td>
<td><span data-ttu-id="bd55e-203">CLSID</span><span class="sxs-lookup"><span data-stu-id="bd55e-203">CLSID</span></span></td>
<td><span data-ttu-id="bd55e-204"><strong>UTILICEN</strong></span><span class="sxs-lookup"><span data-stu-id="bd55e-204"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd55e-205">DEX_IDS_CANT_FIND_COMPRESSOR</span><span class="sxs-lookup"><span data-stu-id="bd55e-205">DEX_IDS_CANT_FIND_COMPRESSOR</span></span></td>
<td><span data-ttu-id="bd55e-206">No se puede encontrar un compresor para generar el formato de compresión especificado.</span><span class="sxs-lookup"><span data-stu-id="bd55e-206">Cannot find a compressor to produce the specified compression format.</span></span></td>
<td><span data-ttu-id="bd55e-207">None</span><span class="sxs-lookup"><span data-stu-id="bd55e-207">None</span></span></td>
<td><span data-ttu-id="bd55e-208">No aplicable</span><span class="sxs-lookup"><span data-stu-id="bd55e-208">Not applicable</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bd55e-209">Nunca deben producirse los siguientes errores.</span><span class="sxs-lookup"><span data-stu-id="bd55e-209">The following errors should never occur.</span></span> <span data-ttu-id="bd55e-210">Si encuentra alguno de estos errores, envíe un informe de errores a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bd55e-210">If you encounter one of these errors, please send a bug report to Microsoft.</span></span>



| <span data-ttu-id="bd55e-211">Código de error</span><span class="sxs-lookup"><span data-stu-id="bd55e-211">Error code</span></span>                 | <span data-ttu-id="bd55e-212">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd55e-212">Description</span></span>                                 |
|----------------------------|---------------------------------------------|
| <span data-ttu-id="bd55e-213">\_análisis de \_ escala de tiempo de IDENTIFICADOres DEX \_</span><span class="sxs-lookup"><span data-stu-id="bd55e-213">DEX\_IDS\_TIMELINE\_PARSE</span></span>  | <span data-ttu-id="bd55e-214">Error inesperado al analizar la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="bd55e-214">Unexpected error parsing the timeline.</span></span>      |
| <span data-ttu-id="bd55e-215">\_error de gráfico de identificadores DEX \_ \_</span><span class="sxs-lookup"><span data-stu-id="bd55e-215">DEX\_IDS\_GRAPH\_ERROR</span></span>     | <span data-ttu-id="bd55e-216">Error inesperado al compilar el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="bd55e-216">Unexpected error building the filter graph.</span></span> |
| <span data-ttu-id="bd55e-217">ERROR de la \_ cuadrícula de identificadores DEX \_ \_</span><span class="sxs-lookup"><span data-stu-id="bd55e-217">DEX\_IDS\_GRID\_ERROR</span></span>      | <span data-ttu-id="bd55e-218">Error inesperado con la cuadrícula interna.</span><span class="sxs-lookup"><span data-stu-id="bd55e-218">Unexpected error with the internal grid.</span></span>    |
| <span data-ttu-id="bd55e-219">ERROR de la \_ interfaz de identificadores DEX \_ \_</span><span class="sxs-lookup"><span data-stu-id="bd55e-219">DEX\_IDS\_INTERFACE\_ERROR</span></span> | <span data-ttu-id="bd55e-220">Error inesperado al obtener una interfaz.</span><span class="sxs-lookup"><span data-stu-id="bd55e-220">Unexpected error getting an interface.</span></span>      |



 

 

 




