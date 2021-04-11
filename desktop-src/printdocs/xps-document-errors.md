---
description: En la tabla siguiente se enumeran todos los valores HRESULT que pueden ser devueltos por los métodos de la API de documentos XPS.
ms.assetid: 9e6db1e3-7151-4538-8607-b7185ebc0110
title: Errores de documento XPS (Xpsobjectmodel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a221858e177172a0062185cbe1bcc127ccc728fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276211"
---
# <a name="xps-document-errors"></a><span data-ttu-id="31d46-103">Errores de documento XPS</span><span class="sxs-lookup"><span data-stu-id="31d46-103">XPS Document Errors</span></span>

<span data-ttu-id="31d46-104">En la tabla siguiente se enumeran todos los valores **HRESULT** que pueden ser devueltos por los métodos de la API de documentos XPS.</span><span class="sxs-lookup"><span data-stu-id="31d46-104">The following table lists all the **HRESULT** values that can be returned by the methods of the XPS Document API.</span></span> <span data-ttu-id="31d46-105">Tenga en cuenta que no todos los métodos devuelven todos los valores devueltos que se enumeran en esta tabla.</span><span class="sxs-lookup"><span data-stu-id="31d46-105">Note that not every method returns every return value that is listed in this table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="31d46-106">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31d46-106">Return code/value</span></span></th>
<th><span data-ttu-id="31d46-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="31d46-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="XPS_E_ALREADY_OWNED"></span><span id="xps_e_already_owned"></span><dl> <span data-ttu-id="31d46-108"><dt><strong>XPS_E_ALREADY_OWNED</strong></dt> <dt>0x80520503</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-108"><dt><strong>XPS_E_ALREADY_OWNED</strong></dt> <dt>0x80520503</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-109">La interfaz ya tiene un propietario.</span><span class="sxs-lookup"><span data-stu-id="31d46-109">The interface already has an owner.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_BLEED_BOX_PAGE_DIMENSIONS_NOT_IN_SYNC"></span><span id="xps_e_bleed_box_page_dimensions_not_in_sync"></span><dl> <span data-ttu-id="31d46-110"><dt><strong>XPS_E_BLEED_BOX_PAGE_DIMENSIONS_NOT_IN_SYNC</strong></dt> <dt>0x80520509</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-110"><dt><strong>XPS_E_BLEED_BOX_PAGE_DIMENSIONS_NOT_IN_SYNC</strong></dt> <dt>0x80520509</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-111">Las dimensiones del cuadro de sangrado no son compatibles con las dimensiones de la página.</span><span class="sxs-lookup"><span data-stu-id="31d46-111">The bleed box dimensions are not compatible with the page dimensions.</span></span><br/> <span data-ttu-id="31d46-112">El valor de ancho del cuadro de sangrado debe ser mayor o igual que el ancho de página más el valor absoluto de la coordenada x del origen del cuadro de sangrado.</span><span class="sxs-lookup"><span data-stu-id="31d46-112">The bleed box width value must be greater than or equal to the page width plus the absolute value of the x-coordinate of the bleed box origin.</span></span> <span data-ttu-id="31d46-113">El valor del alto del cuadro de sangrado debe ser mayor o igual que el alto de página más el valor absoluto de la coordenada y del origen del cuadro de sangría.</span><span class="sxs-lookup"><span data-stu-id="31d46-113">The bleed box height value must be greater than or equal to the page height plus the absolute value of the y-coordinate of the bleed box origin.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_BOTH_PATHFIGURE_AND_ABBR_SYNTAX_PRESENT"></span><span id="xps_e_both_pathfigure_and_abbr_syntax_present"></span><dl> <span data-ttu-id="31d46-114"><dt><strong>XPS_E_BOTH_PATHFIGURE_AND_ABBR_SYNTAX_PRESENT</strong></dt> <dt>0x80520507</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-114"><dt><strong>XPS_E_BOTH_PATHFIGURE_AND_ABBR_SYNTAX_PRESENT</strong></dt> <dt>0x80520507</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-115">Un elemento <strong>PathGeometry</strong> contiene un conjunto de figuras de ruta de acceso que se especifican con el atributo <strong>figures</strong> o con un elemento <strong>PathFigure</strong> secundario.</span><span class="sxs-lookup"><span data-stu-id="31d46-115">A <strong>PathGeometry</strong> element contains a set of path figures that are specified either with the <strong>Figures</strong> attribute or with a child <strong>PathFigure</strong> element.</span></span> <span data-ttu-id="31d46-116">Las cifras de la ruta de acceso de una geometría no pueden tener el atributo <strong>figuras</strong> y un elemento secundario <strong>PathFigure</strong> .</span><span class="sxs-lookup"><span data-stu-id="31d46-116">The path figures of a geometry cannot have both the <strong>Figures</strong> attribute and a child <strong>PathFigure</strong> element.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_BOTH_RESOURCE_AND_SOURCEATTR_PRESENT"></span><span id="xps_e_both_resource_and_sourceattr_present"></span><dl> <span data-ttu-id="31d46-117"><dt><strong>XPS_E_BOTH_RESOURCE_AND_SOURCEATTR_PRESENT</strong></dt> <dt>0x80520508</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-117"><dt><strong>XPS_E_BOTH_RESOURCE_AND_SOURCEATTR_PRESENT</strong></dt> <dt>0x80520508</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-118">Un elemento <strong>ResourceDictionary</strong> que especifica un diccionario de recursos remotos en su atributo de <strong>origen</strong> no debe contener ningún elemento secundario de definición de recursos.</span><span class="sxs-lookup"><span data-stu-id="31d46-118">A <strong>ResourceDictionary</strong> element that specifies a remote resource dictionary in its <strong>Source</strong> attribute MUST NOT contain any resource definition children.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_CARET_OUT_OF_ORDER"></span><span id="xps_e_caret_out_of_order"></span><dl> <span data-ttu-id="31d46-119"><dt><strong>XPS_E_CARET_OUT_OF_ORDER</strong></dt> <dt>0x80520306</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-119"><dt><strong>XPS_E_CARET_OUT_OF_ORDER</strong></dt> <dt>0x80520306</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-120">Un valor de ubicación del símbolo de intercalación está desordenado.</span><span class="sxs-lookup"><span data-stu-id="31d46-120">A caret location value is out of order.</span></span> <span data-ttu-id="31d46-121">Los valores de ubicación se deben ordenar en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="31d46-121">The location values must be sorted in ascending order.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_CARET_OUTSIDE_STRING"></span><span id="xps_e_caret_outside_string"></span><dl> <span data-ttu-id="31d46-122"><dt><strong>XPS_E_CARET_OUTSIDE_STRING</strong></dt> <dt>0x80520305</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-122"><dt><strong>XPS_E_CARET_OUTSIDE_STRING</strong></dt> <dt>0x80520305</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-123">Se han especificado paradas de símbolo de intercalación para una cadena vacía; o bien, el índice de salto del símbolo de intercalación ha superado la longitud de la cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="31d46-123">Caret stops were specified for an empty string; or, the caret jump index has exceeded the length of the Unicode string.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_COLOR_COMPONENT_OUT_OF_RANGE"></span><span id="xps_e_color_component_out_of_range"></span><dl> <span data-ttu-id="31d46-124"><dt><strong>XPS_E_COLOR_COMPONENT_OUT_OF_RANGE</strong></dt> <dt>0x80520506</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-124"><dt><strong>XPS_E_COLOR_COMPONENT_OUT_OF_RANGE</strong></dt> <dt>0x80520506</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-125">Un valor de color está fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="31d46-125">A color value is out of range.</span></span><br/> <span data-ttu-id="31d46-126">Para <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_SCRGB</strong></a> tipos de color, el valor de canal alfa debe ser mayor o igual que 0,0 y menor o igual que + 1,0.</span><span class="sxs-lookup"><span data-stu-id="31d46-126">For <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_SCRGB</strong></a> color types, the alpha channel value must be greater than or equal to 0.0 and less than or equal to +1.0.</span></span><br/> <span data-ttu-id="31d46-127">En <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a> tipos de color, <strong>channelValues [0]</strong> que representa el valor del canal alfa debe ser mayor o igual que 0,0 y menor o igual que + 1,0.</span><span class="sxs-lookup"><span data-stu-id="31d46-127">For <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a> color types, the <strong>channelValues[0]</strong> that represents the alpha channel value must be greater than or equal to 0.0 and less than or equal to +1.0.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_DICTIONARY_ITEM_NAMED"></span><span id="xps_e_dictionary_item_named"></span><dl> <span data-ttu-id="31d46-128"><dt><strong>XPS_E_DICTIONARY_ITEM_NAMED</strong></dt> <dt>0x80520401</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-128"><dt><strong>XPS_E_DICTIONARY_ITEM_NAMED</strong></dt> <dt>0x80520401</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-129">Un elemento visual de un diccionario de recursos tiene el atributo <strong>Name</strong> , que no se puede especificar en ningún elemento secundario de un elemento <strong>ResourceDictionary</strong> .</span><span class="sxs-lookup"><span data-stu-id="31d46-129">A visual in a resource dictionary has the <strong>Name</strong> attribute, which may not be specified on any children of a <strong>ResourceDictionary</strong> element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_DUPLICATE_NAMES"></span><span id="xps_e_duplicate_names"></span><dl> <span data-ttu-id="31d46-130"><dt><strong>XPS_E_DUPLICATE_NAMES</strong></dt> <dt>0x80520209</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-130"><dt><strong>XPS_E_DUPLICATE_NAMES</strong></dt> <dt>0x80520209</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-131">Ya existe un objeto con este nombre en el diccionario.</span><span class="sxs-lookup"><span data-stu-id="31d46-131">An object with this name already exists in the dictionary.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_DUPLICATE_RESOURCE_KEYS"></span><span id="xps_e_duplicate_resource_keys"></span><dl> <span data-ttu-id="31d46-132"><dt><strong>XPS_E_DUPLICATE_RESOURCE_KEYS</strong></dt> <dt>0x80520200</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-132"><dt><strong>XPS_E_DUPLICATE_RESOURCE_KEYS</strong></dt> <dt>0x80520200</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-133">Ya existe un objeto con este nombre de clave en el diccionario.</span><span class="sxs-lookup"><span data-stu-id="31d46-133">An object with this key name already exists in the dictionary.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INDEX_OUT_OF_RANGE"></span><span id="xps_e_index_out_of_range"></span><dl> <span data-ttu-id="31d46-134"><dt><strong>XPS_E_INDEX_OUT_OF_RANGE</strong></dt> <dt>0x80520500</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-134"><dt><strong>XPS_E_INDEX_OUT_OF_RANGE</strong></dt> <dt>0x80520500</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-135">Reservado.</span><span class="sxs-lookup"><span data-stu-id="31d46-135">Reserved.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_BLEED_BOX"></span><span id="xps_e_invalid_bleed_box"></span><dl> <span data-ttu-id="31d46-136"><dt><strong>XPS_E_INVALID_BLEED_BOX</strong></dt> <dt>0x80520004</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-136"><dt><strong>XPS_E_INVALID_BLEED_BOX</strong></dt> <dt>0x80520004</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-137">El rectángulo del cuadro de sangrado contiene uno o más valores que no son válidos.</span><span class="sxs-lookup"><span data-stu-id="31d46-137">The bleed box rectangle contains one or more values that are not valid.</span></span> <span data-ttu-id="31d46-138">Vea la descripción del parámetro para ver los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="31d46-138">See the parameter description for the valid values.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_CONTENT_BOX"></span><span id="xps_e_invalid_content_box"></span><dl> <span data-ttu-id="31d46-139"><dt><strong>XPS_E_INVALID_CONTENT_BOX</strong></dt> <dt>0x8052000b</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-139"><dt><strong>XPS_E_INVALID_CONTENT_BOX</strong></dt> <dt>0x8052000b</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-140">El rectángulo del cuadro de contenido contiene uno o más valores que no son válidos.</span><span class="sxs-lookup"><span data-stu-id="31d46-140">The content box rectangle contains one or more values that are not valid.</span></span> <span data-ttu-id="31d46-141">Vea la descripción del parámetro para ver los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="31d46-141">See the parameter description for the valid values.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_CONTENT_TYPE"></span><span id="xps_e_invalid_content_type"></span><dl> <span data-ttu-id="31d46-142"><dt><strong>XPS_E_INVALID_CONTENT_TYPE</strong></dt> <dt>0x8052000e</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-142"><dt><strong>XPS_E_INVALID_CONTENT_TYPE</strong></dt> <dt>0x8052000e</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-143">La cadena de tipo de contenido no es válida.</span><span class="sxs-lookup"><span data-stu-id="31d46-143">The content type string is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_FLOAT"></span><span id="xps_e_invalid_float"></span><dl> <span data-ttu-id="31d46-144"><dt><strong>XPS_E_INVALID_FLOAT</strong></dt> <dt>0x80520007</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-144"><dt><strong>XPS_E_INVALID_FLOAT</strong></dt> <dt>0x80520007</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-145">Un valor <strong>float</strong> no es válido.</span><span class="sxs-lookup"><span data-stu-id="31d46-145">A <strong>FLOAT</strong> value is not valid.</span></span> <span data-ttu-id="31d46-146">Es infinito o no es un número (NAN).</span><span class="sxs-lookup"><span data-stu-id="31d46-146">It is either an infinite or not a number (NAN).</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_FONT_URI"></span><span id="xps_e_invalid_font_uri"></span><dl> <span data-ttu-id="31d46-147"><dt><strong>XPS_E_INVALID_FONT_URI</strong></dt> <dt>0x8052000a</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-147"><dt><strong>XPS_E_INVALID_FONT_URI</strong></dt> <dt>0x8052000a</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-148">El URI de fuente no es válido, posiblemente porque contiene un fragmento vacío o caracteres que no son válidos.</span><span class="sxs-lookup"><span data-stu-id="31d46-148">The font URI is not valid, possibly because it contains an empty fragment or characters that are not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_LANGUAGE"></span><span id="xps_e_invalid_language"></span><dl> <span data-ttu-id="31d46-149"><dt><strong>XPS_E_INVALID_LANGUAGE</strong></dt> <dt>0x80520000</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-149"><dt><strong>XPS_E_INVALID_LANGUAGE</strong></dt> <dt>0x80520000</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-150">El idioma especificado no es válido o no tiene el formato correcto.</span><span class="sxs-lookup"><span data-stu-id="31d46-150">The specified language is either not valid or not correctly formatted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_LOOKUP_TYPE"></span><span id="xps_e_invalid_lookup_type"></span><dl> <span data-ttu-id="31d46-151"><dt><strong>XPS_E_INVALID_LOOKUP_TYPE</strong></dt> <dt>0x80520006</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-151"><dt><strong>XPS_E_INVALID_LOOKUP_TYPE</strong></dt> <dt>0x80520006</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-152">El nombre de la clave de búsqueda hace referencia a un objeto que no es del tipo correcto para la llamada; por ejemplo, si el método devuelve un pincel pero el nombre de la clave de búsqueda hace referencia a un objeto Geometry.</span><span class="sxs-lookup"><span data-stu-id="31d46-152">The lookup key name references an object that is not the correct type for the call; for example, if the method returns a brush but the lookup key name refers to a geometry object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_MARKUP"></span><span id="xps_e_invalid_markup"></span><dl> <span data-ttu-id="31d46-153"><dt><strong>XPS_E_INVALID_MARKUP</strong></dt> <dt>0x8052000c</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-153"><dt><strong>XPS_E_INVALID_MARKUP</strong></dt> <dt>0x8052000c</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-154">El marcado que se está leyendo contiene un elemento o un atributo que no se ajusta a la <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">especificación de papel XML</a>.</span><span class="sxs-lookup"><span data-stu-id="31d46-154">The markup being read contains an element or an attribute that does not conform to the <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="31d46-155">Para representar valores de punto flotante, el OM de XPS usa el tipo de datos <strong>float</strong> en lugar de <strong>Double</strong>.</span><span class="sxs-lookup"><span data-stu-id="31d46-155">To represent floating-point values, the XPS OM uses the <strong>FLOAT</strong> data type instead of <strong>DOUBLE</strong>.</span></span> <span data-ttu-id="31d46-156">Si un documento XPS tiene un elemento con datos de punto flotante que no caben en un valor <strong>float</strong> , se devolverá este error cuando ese valor se encuentre durante la deserialización.</span><span class="sxs-lookup"><span data-stu-id="31d46-156">If an XPS document has an element with floating-point data that does not fit into a <strong>FLOAT</strong> value, this error will be returned when that value is encountered during deserialization.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_NAME"></span><span id="xps_e_invalid_name"></span><dl> <span data-ttu-id="31d46-157"><dt><strong>XPS_E_INVALID_NAME</strong></dt> <dt>0x80520001</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-157"><dt><strong>XPS_E_INVALID_NAME</strong></dt> <dt>0x80520001</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-158">La cadena que se pasó no es un nombre válido, de acuerdo con la especificación de papel XML.</span><span class="sxs-lookup"><span data-stu-id="31d46-158">The string that was passed is not a valid name, according to the XML Paper Specification.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_OBFUSCATED_FONT_URI"></span><span id="xps_e_invalid_obfuscated_font_uri"></span><dl> <span data-ttu-id="31d46-159"><dt><strong>XPS_E_INVALID_OBFUSCATED_FONT_URI</strong></dt> <dt>0x8052000f</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-159"><dt><strong>XPS_E_INVALID_OBFUSCATED_FONT_URI</strong></dt> <dt>0x8052000f</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-160">Reservado.</span><span class="sxs-lookup"><span data-stu-id="31d46-160">Reserved.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_PAGE_SIZE"></span><span id="xps_e_invalid_page_size"></span><dl> <span data-ttu-id="31d46-161"><dt><strong>XPS_E_INVALID_PAGE_SIZE</strong></dt> <dt>0x80520003</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-161"><dt><strong>XPS_E_INVALID_PAGE_SIZE</strong></dt> <dt>0x80520003</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-162">Las dimensiones de página contienen un valor de tamaño de página que no es válido.</span><span class="sxs-lookup"><span data-stu-id="31d46-162">The page dimensions contain a page size value that is not valid.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_RESOURCE_KEY"></span><span id="xps_e_invalid_resource_key"></span><dl> <span data-ttu-id="31d46-163"><dt><strong>XPS_E_INVALID_RESOURCE_KEY</strong></dt> <dt>0x80520002</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-163"><dt><strong>XPS_E_INVALID_RESOURCE_KEY</strong></dt> <dt>0x80520002</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-164">Según la <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">especificación de papel XML</a>, la cadena de clave de búsqueda no es válida.</span><span class="sxs-lookup"><span data-stu-id="31d46-164">According to the <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>, the lookup key string is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE"></span><span id="xps_e_invalid_thumbnail_image_type"></span><dl> <span data-ttu-id="31d46-165"><dt><strong>XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE</strong></dt> <dt>0x80520005</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-165"><dt><strong>XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE</strong></dt> <dt>0x80520005</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-166">No se admite el tipo de imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="31d46-166">The thumbnail image type is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_XML_ENCODING"></span><span id="xps_e_invalid_xml_encoding"></span><dl> <span data-ttu-id="31d46-167"><dt><strong>XPS_E_INVALID_XML_ENCODING</strong></dt> <dt>0x8052000d</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-167"><dt><strong>XPS_E_INVALID_XML_ENCODING</strong></dt> <dt>0x8052000d</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-168">Se encontró un marcado XML incorrecto o con formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="31d46-168">Found improper or incorrectly formatted XML markup.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MAPPING_OUT_OF_ORDER"></span><span id="xps_e_mapping_out_of_order"></span><dl> <span data-ttu-id="31d46-169"><dt><strong>XPS_E_MAPPING_OUT_OF_ORDER</strong></dt> <dt>0x80520302</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-169"><dt><strong>XPS_E_MAPPING_OUT_OF_ORDER</strong></dt> <dt>0x80520302</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-170">En una o varias estructuras de <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_mapping"><strong>XPS_GLYPH_MAPPING</strong></a> , un elemento está fuera de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="31d46-170">In one or more <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_mapping"><strong>XPS_GLYPH_MAPPING</strong></a> structures, an element is out of sequence.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MAPPING_OUTSIDE_INDICES"></span><span id="xps_e_mapping_outside_indices"></span><dl> <span data-ttu-id="31d46-171"><dt><strong>XPS_E_MAPPING_OUTSIDE_INDICES</strong></dt> <dt>0x80520304</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-171"><dt><strong>XPS_E_MAPPING_OUTSIDE_INDICES</strong></dt> <dt>0x80520304</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-172">Las asignaciones de glifos superan el número de índices de glifo.</span><span class="sxs-lookup"><span data-stu-id="31d46-172">The glyph mappings exceed the number of glyph indices.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MAPPING_OUTSIDE_STRING"></span><span id="xps_e_mapping_outside_string"></span><dl> <span data-ttu-id="31d46-173"><dt><strong>XPS_E_MAPPING_OUTSIDE_STRING</strong></dt> <dt>0x80520303</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-173"><dt><strong>XPS_E_MAPPING_OUTSIDE_STRING</strong></dt> <dt>0x80520303</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-174">Error en las asignaciones de glifo.</span><span class="sxs-lookup"><span data-stu-id="31d46-174">Error in the glyph mappings.</span></span><br/> <span data-ttu-id="31d46-175">Si la cadena Unicode está vacía, este error significa que también se ha definido una asignación de glifo.</span><span class="sxs-lookup"><span data-stu-id="31d46-175">If the Unicode string is empty, this error means that a glyph mapping was also defined.</span></span> <span data-ttu-id="31d46-176">No se deben definir asignaciones de glifos si la cadena Unicode está vacía.</span><span class="sxs-lookup"><span data-stu-id="31d46-176">Glyph mappings must not be defined if the Unicode string is empty.</span></span><br/> <span data-ttu-id="31d46-177">Si la cadena Unicode no está vacía, este error significa que se ha definido una asignación de glifo para los glifos fuera de la cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="31d46-177">If the Unicode string is not empty, this error means that a glyph mapping was defined for glyphs outside of the Unicode string.</span></span> <span data-ttu-id="31d46-178">No se pueden definir asignaciones de glifos para glifos que se encuentran fuera de la longitud de la cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="31d46-178">Glyph mappings cannot be defined for glyphs that fall outside the length of the Unicode string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_COLORPROFILE"></span><span id="xps_e_missing_colorprofile"></span><dl> <span data-ttu-id="31d46-179"><dt><strong>XPS_E_MISSING_COLORPROFILE</strong></dt> <dt>0x80520104</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-179"><dt><strong>XPS_E_MISSING_COLORPROFILE</strong></dt> <dt>0x80520104</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-180">El parámetro de Perfil de color es <strong>null</strong>, pero se espera un perfil de color.</span><span class="sxs-lookup"><span data-stu-id="31d46-180">The color profile parameter is <strong>NULL</strong>, but a color profile is expected.</span></span> <span data-ttu-id="31d46-181">Se requiere un perfil de color cuando el tipo de color es XPS_COLOR_TYPE_CONTEXT.</span><span class="sxs-lookup"><span data-stu-id="31d46-181">A color profile is required when the color type is XPS_COLOR_TYPE_CONTEXT.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_DISCARDCONTROL"></span><span id="xps_e_missing_discardcontrol"></span><dl> <span data-ttu-id="31d46-182"><dt><strong>XPS_E_MISSING_DISCARDCONTROL</strong></dt> <dt>0x80520112</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-182"><dt><strong>XPS_E_MISSING_DISCARDCONTROL</strong></dt> <dt>0x80520112</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-183">Una página hace referencia a recursos descartables pero no especifica un nombre de parte de DiscardControl.</span><span class="sxs-lookup"><span data-stu-id="31d46-183">A page refers to discardable resources but does not specify a DiscardControl part name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_DOCUMENT"></span><span id="xps_e_missing_document"></span><dl> <span data-ttu-id="31d46-184"><dt><strong>XPS_E_MISSING_DOCUMENT</strong></dt> <dt>0x80520109</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-184"><dt><strong>XPS_E_MISSING_DOCUMENT</strong></dt> <dt>0x80520109</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-185">Se llamó a <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage"><strong>IXpsOMPackageWriter:: AddPage</strong></a> antes de <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>IXpsOMPackageWriter:: StartNewDocument</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="31d46-185"><a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage"><strong>IXpsOMPackageWriter::AddPage</strong></a> was called before <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>IXpsOMPackageWriter::StartNewDocument</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_DOCUMENTSEQUENCE_RELATIONSHIP"></span><span id="xps_e_missing_documentsequence_relationship"></span><dl> <span data-ttu-id="31d46-186"><dt><strong>XPS_E_MISSING_DOCUMENTSEQUENCE_RELATIONSHIP</strong></dt> <dt>0x80520108</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-186"><dt><strong>XPS_E_MISSING_DOCUMENTSEQUENCE_RELATIONSHIP</strong></dt> <dt>0x80520108</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-187">El paquete no contiene una FixedDocumentSequence.</span><span class="sxs-lookup"><span data-stu-id="31d46-187">The package does not contain a FixedDocumentSequence.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_FONTURI"></span><span id="xps_e_missing_fonturi"></span><dl> <span data-ttu-id="31d46-188"><dt><strong>XPS_E_MISSING_FONTURI</strong></dt> <dt>0x80520107</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-188"><dt><strong>XPS_E_MISSING_FONTURI</strong></dt> <dt>0x80520107</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-189">La interfaz <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>IXpsOMGlyphs</strong></a> requiere un URI de fuente, pero no se especifica uno.</span><span class="sxs-lookup"><span data-stu-id="31d46-189">The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>IXpsOMGlyphs</strong></a> interface requires a font URI, but one is not specified.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_GLYPHS"></span><span id="xps_e_missing_glyphs"></span><dl> <span data-ttu-id="31d46-190"><dt><strong>XPS_E_MISSING_GLYPHS</strong></dt> <dt>0x80520102</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-190"><dt><strong>XPS_E_MISSING_GLYPHS</strong></dt> <dt>0x80520102</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-191">La interfaz <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>IXpsOMGlyphs</strong></a> sin una cadena Unicode no especifica ningún índice de glifo.</span><span class="sxs-lookup"><span data-stu-id="31d46-191">The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>IXpsOMGlyphs</strong></a> interface without a Unicode string does not specify any glyph indices.</span></span> <span data-ttu-id="31d46-192">Una interfaz <strong>IXpsOMGlyphs</strong> debe especificar una cadena Unicode o una matriz de índices de glifo.</span><span class="sxs-lookup"><span data-stu-id="31d46-192">An <strong>IXpsOMGlyphs</strong> interface must specify either a Unicode string or an array of glyph indices.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_IMAGE_IN_IMAGEBRUSH"></span><span id="xps_e_missing_image_in_imagebrush"></span><dl> <span data-ttu-id="31d46-193"><dt><strong>XPS_E_MISSING_IMAGE_IN_IMAGEBRUSH</strong></dt> <dt>0x8052010e</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-193"><dt><strong>XPS_E_MISSING_IMAGE_IN_IMAGEBRUSH</strong></dt> <dt>0x8052010e</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-194">No se encontró un recurso de imagen para el pincel de imagen.</span><span class="sxs-lookup"><span data-stu-id="31d46-194">An image resource could not be located for the image brush.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_LOOKUP"></span><span id="xps_e_missing_lookup"></span><dl> <span data-ttu-id="31d46-195"><dt><strong>XPS_E_MISSING_LOOKUP</strong></dt> <dt>0x80520101</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-195"><dt><strong>XPS_E_MISSING_LOOKUP</strong></dt> <dt>0x80520101</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-196">El recurso remoto tiene un objeto inesperado.</span><span class="sxs-lookup"><span data-stu-id="31d46-196">The remote resource has an unexpected object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_NAME"></span><span id="xps_e_missing_name"></span><dl> <span data-ttu-id="31d46-197"><dt><strong>XPS_E_MISSING_NAME</strong></dt> <dt>0x80520100</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-197"><dt><strong>XPS_E_MISSING_NAME</strong></dt> <dt>0x80520100</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-198">La página no se ha denominado; el estado de destino del hipervínculo solo se puede establecer si la página tiene un nombre.</span><span class="sxs-lookup"><span data-stu-id="31d46-198">The page has not been named; the hyperlink target status can only be set if the page has a name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_PAGE_IN_DOCUMENT"></span><span id="xps_e_missing_page_in_document"></span><dl> <span data-ttu-id="31d46-199"><dt><strong>XPS_E_MISSING_PAGE_IN_DOCUMENT</strong></dt> <dt>0x8052010c</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-199"><dt><strong>XPS_E_MISSING_PAGE_IN_DOCUMENT</strong></dt> <dt>0x8052010c</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-200">FixedDocument no contiene ninguna parte de FixedPage.</span><span class="sxs-lookup"><span data-stu-id="31d46-200">The FixedDocument does not contain any FixedPage parts.</span></span> <span data-ttu-id="31d46-201">Un documento XPS debe contener al menos una parte de FixedPage.</span><span class="sxs-lookup"><span data-stu-id="31d46-201">An XPS document must contain at least one FixedPage part.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_PAGE_IN_PAGEREFERENCE"></span><span id="xps_e_missing_page_in_pagereference"></span><dl> <span data-ttu-id="31d46-202"><dt><strong>XPS_E_MISSING_PAGE_IN_PAGEREFERENCE</strong></dt> <dt>0x8052010d</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-202"><dt><strong>XPS_E_MISSING_PAGE_IN_PAGEREFERENCE</strong></dt> <dt>0x8052010d</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-203">La referencia de página no tiene una página correspondiente.</span><span class="sxs-lookup"><span data-stu-id="31d46-203">The page reference does not have a corresponding page.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_PART_REFERENCE"></span><span id="xps_e_missing_part_reference"></span><dl> <span data-ttu-id="31d46-204"><dt><strong>XPS_E_MISSING_PART_REFERENCE</strong></dt> <dt>0x80520110</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-204"><dt><strong>XPS_E_MISSING_PART_REFERENCE</strong></dt> <dt>0x80520110</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-205">No se hizo referencia A una parte de destino necesaria.</span><span class="sxs-lookup"><span data-stu-id="31d46-205">A required target part was not referenced.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_PART_STREAM"></span><span id="xps_e_missing_part_stream"></span><dl> <span data-ttu-id="31d46-206"><dt><strong>XPS_E_MISSING_PART_STREAM</strong></dt> <dt>0x80520113</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-206"><dt><strong>XPS_E_MISSING_PART_STREAM</strong></dt> <dt>0x80520113</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-207">No se especificó una secuencia para el recurso.</span><span class="sxs-lookup"><span data-stu-id="31d46-207">A stream was not specified for the resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_REFERRED_DOCUMENT"></span><span id="xps_e_missing_referred_document"></span><dl> <span data-ttu-id="31d46-208"><dt><strong>XPS_E_MISSING_REFERRED_DOCUMENT</strong></dt> <dt>0x8052010a</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-208"><dt><strong>XPS_E_MISSING_REFERRED_DOCUMENT</strong></dt> <dt>0x8052010a</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-209">No se encontró la parte FixedDocument a la que hace referencia la FixedDocumentSequence.</span><span class="sxs-lookup"><span data-stu-id="31d46-209">The FixedDocument part that is referenced by the FixedDocumentSequence could not be found.</span></span> <span data-ttu-id="31d46-210">Un documento XPS debe contener al menos un FixedDocument.</span><span class="sxs-lookup"><span data-stu-id="31d46-210">An XPS document must contain at least one FixedDocument.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_REFERRED_PAGE"></span><span id="xps_e_missing_referred_page"></span><dl> <span data-ttu-id="31d46-211"><dt><strong>XPS_E_MISSING_REFERRED_PAGE</strong></dt> <dt>0x8052010b</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-211"><dt><strong>XPS_E_MISSING_REFERRED_PAGE</strong></dt> <dt>0x8052010b</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-212">No se encontró la parte FixedPage a la que hace referencia el elemento FixedDocument.</span><span class="sxs-lookup"><span data-stu-id="31d46-212">The FixedPage part that is referenced by the FixedDocument could not be found.</span></span> <span data-ttu-id="31d46-213">Un documento XPS debe contener al menos una parte de FixedPage.</span><span class="sxs-lookup"><span data-stu-id="31d46-213">An XPS document must contain at least one FixedPage part.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_RELATIONSHIP_TARGET"></span><span id="xps_e_missing_relationship_target"></span><dl> <span data-ttu-id="31d46-214"><dt><strong>XPS_E_MISSING_RELATIONSHIP_TARGET</strong></dt> <dt>0x80520105</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-214"><dt><strong>XPS_E_MISSING_RELATIONSHIP_TARGET</strong></dt> <dt>0x80520105</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-215">La parte de destino de la relación no está presente en la relación de paquete.</span><span class="sxs-lookup"><span data-stu-id="31d46-215">The relationship target part is not present in the package relationship.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_RESOURCE_KEY"></span><span id="xps_e_missing_resource_key"></span><dl> <span data-ttu-id="31d46-216"><dt><strong>XPS_E_MISSING_RESOURCE_KEY</strong></dt> <dt>0x8052010f</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-216"><dt><strong>XPS_E_MISSING_RESOURCE_KEY</strong></dt> <dt>0x8052010f</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-217">No se especificó ningún atributo <strong>x:Key</strong> para el recurso.</span><span class="sxs-lookup"><span data-stu-id="31d46-217">No <strong>x:Key</strong> attribute was specified for the resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_RESOURCE_RELATIONSHIP"></span><span id="xps_e_missing_resource_relationship"></span><dl> <span data-ttu-id="31d46-218"><dt><strong>XPS_E_MISSING_RESOURCE_RELATIONSHIP</strong></dt> <dt>0x80520106</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-218"><dt><strong>XPS_E_MISSING_RESOURCE_RELATIONSHIP</strong></dt> <dt>0x80520106</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-219">El recurso al que hace referencia la página o el contenido del diccionario remoto no existe como una relación de página.</span><span class="sxs-lookup"><span data-stu-id="31d46-219">The resource referred to by the page or remote dictionary content does not exist as a page relationship.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_RESTRICTED_FONT_RELATIONSHIP"></span><span id="xps_e_missing_restricted_font_relationship"></span><dl> <span data-ttu-id="31d46-220"><dt><strong>XPS_E_MISSING_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520111</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-220"><dt><strong>XPS_E_MISSING_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520111</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-221">La fuente restringida a la que se hace referencia no se especificó en la llamada a <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>IXpsOMPackageWriter:: StartNewDocument</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="31d46-221">The referenced restricted font was not specified in the call to <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>IXpsOMPackageWriter::StartNewDocument</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_SEGMENT_DATA"></span><span id="xps_e_missing_segment_data"></span><dl> <span data-ttu-id="31d46-222"><dt><strong>XPS_E_MISSING_SEGMENT_DATA</strong></dt> <dt>0x80520103</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-222"><dt><strong>XPS_E_MISSING_SEGMENT_DATA</strong></dt> <dt>0x80520103</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-223">La matriz de datos de segmento tiene menos entradas que la matriz de tipos de segmentos.</span><span class="sxs-lookup"><span data-stu-id="31d46-223">The segment data array has fewer entries than the segment types array.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_DOCUMENTSEQUENCE_RELATIONSHIPS"></span><span id="xps_e_multiple_documentsequence_relationships"></span><dl> <span data-ttu-id="31d46-224"><dt><strong>XPS_E_MULTIPLE_DOCUMENTSEQUENCE_RELATIONSHIPS</strong></dt> <dt>0x80520202</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-224"><dt><strong>XPS_E_MULTIPLE_DOCUMENTSEQUENCE_RELATIONSHIPS</strong></dt> <dt>0x80520202</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-225">Se intentó agregar un FixedDocumentSequence a un paquete que ya tiene uno.</span><span class="sxs-lookup"><span data-stu-id="31d46-225">An attempt was made to add a FixedDocumentSequence to a package that already has one.</span></span> <span data-ttu-id="31d46-226">Un documento XPS debe contener una y solo una parte de FixedDocumentSequence.</span><span class="sxs-lookup"><span data-stu-id="31d46-226">An XPS document must contain one and only one FixedDocumentSequence part.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENT"></span><span id="xps_e_multiple_printtickets_on_document"></span><dl> <span data-ttu-id="31d46-227"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENT</strong></dt> <dt>0x80520206</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-227"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENT</strong></dt> <dt>0x80520206</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-228">Se intentó agregar un vale de impresión de nivel de documento a un FixedDocument que ya tiene uno.</span><span class="sxs-lookup"><span data-stu-id="31d46-228">An attempt was made to add a document-level print ticket to a FixedDocument that already has one.</span></span> <span data-ttu-id="31d46-229">Un FixedDocument en un documento XPS solo puede contener un vale de impresión de nivel de documento.</span><span class="sxs-lookup"><span data-stu-id="31d46-229">A FixedDocument in an XPS document can contain only one document-level print ticket.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENTSEQUENCE"></span><span id="xps_e_multiple_printtickets_on_documentsequence"></span><dl> <span data-ttu-id="31d46-230"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENTSEQUENCE</strong></dt> <dt>0x80520207</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-230"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENTSEQUENCE</strong></dt> <dt>0x80520207</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-231">Se intentó agregar un vale de impresión en el nivel de trabajo a una FixedDocumentSequence que ya tiene uno.</span><span class="sxs-lookup"><span data-stu-id="31d46-231">An attempt was made to add a job-level print ticket to a FixedDocumentSequence that already has one.</span></span> <span data-ttu-id="31d46-232">La FixedDocumentSequence en un documento XPS solo puede contener un vale de impresión en el nivel de trabajo.</span><span class="sxs-lookup"><span data-stu-id="31d46-232">The FixedDocumentSequence in an XPS document can contain only one job-level print ticket.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_PAGE"></span><span id="xps_e_multiple_printtickets_on_page"></span><dl> <span data-ttu-id="31d46-233"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_PAGE</strong></dt> <dt>0x80520205</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-233"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_PAGE</strong></dt> <dt>0x80520205</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-234">Se intentó agregar un vale de impresión en el nivel de página a un FixedPage que ya tiene uno.</span><span class="sxs-lookup"><span data-stu-id="31d46-234">An attempt was made to add a page-level print ticket to a FixedPage that already has one.</span></span> <span data-ttu-id="31d46-235">Un FixedPage en un documento XPS solo puede contener un vale de impresión en el nivel de página.</span><span class="sxs-lookup"><span data-stu-id="31d46-235">A FixedPage in an XPS document can contain only one page-level print ticket.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_REFERENCES_TO_PART"></span><span id="xps_e_multiple_references_to_part"></span><dl> <span data-ttu-id="31d46-236"><dt><strong>XPS_E_MULTIPLE_REFERENCES_TO_PART</strong></dt> <dt>0x80520208</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-236"><dt><strong>XPS_E_MULTIPLE_REFERENCES_TO_PART</strong></dt> <dt>0x80520208</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-237">La colección de fuentes restringidas contenía una entrada de fuente restringida que se repitió.</span><span class="sxs-lookup"><span data-stu-id="31d46-237">The restricted font collection contained a restricted font entry that was repeated.</span></span> <span data-ttu-id="31d46-238">Cada entrada de fuente solo puede aparecer una vez en la colección.</span><span class="sxs-lookup"><span data-stu-id="31d46-238">Each font entry can occur in the collection only once.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_RESOURCES"></span><span id="xps_e_multiple_resources"></span><dl> <span data-ttu-id="31d46-239"><dt><strong>XPS_E_MULTIPLE_RESOURCES</strong></dt> <dt>0x80520201</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-239"><dt><strong>XPS_E_MULTIPLE_RESOURCES</strong></dt> <dt>0x80520201</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-240">Ya existe un recurso por ese nombre de elemento.</span><span class="sxs-lookup"><span data-stu-id="31d46-240">A resource by that part name already exists.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_THUMBNAILS_ON_PACKAGE"></span><span id="xps_e_multiple_thumbnails_on_package"></span><dl> <span data-ttu-id="31d46-241"><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PACKAGE</strong></dt> <dt>0x80520204</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-241"><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PACKAGE</strong></dt> <dt>0x80520204</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-242">Se intentó agregar una imagen en miniatura a un paquete que ya tiene uno.</span><span class="sxs-lookup"><span data-stu-id="31d46-242">An attempt was made to add a thumbnail image to a package that already has one.</span></span> <span data-ttu-id="31d46-243">Un documento XPS solo puede contener una imagen en miniatura de nivel de paquete.</span><span class="sxs-lookup"><span data-stu-id="31d46-243">An XPS document can contain only one package-level thumbnail image.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_THUMBNAILS_ON_PAGE"></span><span id="xps_e_multiple_thumbnails_on_page"></span><dl> <span data-ttu-id="31d46-244"><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PAGE</strong></dt> <dt>0x80520203</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-244"><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PAGE</strong></dt> <dt>0x80520203</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-245">Se intentó agregar una imagen en miniatura de nivel de página a un FixedPage que ya tiene una.</span><span class="sxs-lookup"><span data-stu-id="31d46-245">An attempt was made to add a page-level thumbnail image to a FixedPage that already has one.</span></span> <span data-ttu-id="31d46-246">Un FixedPage en un documento XPS solo puede contener una imagen en miniatura de nivel de página.</span><span class="sxs-lookup"><span data-stu-id="31d46-246">A FixedPage in an XPS document can contain only one page-level thumbnail image.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_NEGATIVE_FLOAT"></span><span id="xps_e_negative_float"></span><dl> <span data-ttu-id="31d46-247"><dt><strong>XPS_E_NEGATIVE_FLOAT</strong></dt> <dt>0x8052030a</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-247"><dt><strong>XPS_E_NEGATIVE_FLOAT</strong></dt> <dt>0x8052030a</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-248">Una entrada contiene un valor negativo, pero debe contener un valor no negativo.</span><span class="sxs-lookup"><span data-stu-id="31d46-248">An entry contains a negative value, but it must contain a non-negative value.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_NESTED_REMOTE_DICTIONARY"></span><span id="xps_e_nested_remote_dictionary"></span><dl> <span data-ttu-id="31d46-249"><dt><strong>XPS_E_NESTED_REMOTE_DICTIONARY</strong></dt> <dt>0x80520402</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-249"><dt><strong>XPS_E_NESTED_REMOTE_DICTIONARY</strong></dt> <dt>0x80520402</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-250">Se intentó agregar una referencia de diccionario remoto a un diccionario remoto.</span><span class="sxs-lookup"><span data-stu-id="31d46-250">An attempt was made to add a remote dictionary reference to a remote dictionary.</span></span> <span data-ttu-id="31d46-251">Un diccionario remoto no puede hacer referencia A otro diccionario remoto.</span><span class="sxs-lookup"><span data-stu-id="31d46-251">A remote dictionary cannot reference another remote dictionary.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_NO_CUSTOM_OBJECTS"></span><span id="xps_e_no_custom_objects"></span><dl> <span data-ttu-id="31d46-252"><dt><strong>XPS_E_NO_CUSTOM_OBJECTS</strong></dt> <dt>0x80520502</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-252"><dt><strong>XPS_E_NO_CUSTOM_OBJECTS</strong></dt> <dt>0x80520502</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-253">Un puntero de interfaz no apunta a una implementación de interfaz reconocida.</span><span class="sxs-lookup"><span data-stu-id="31d46-253">An interface pointer does not point to a recognized interface implementation.</span></span> <span data-ttu-id="31d46-254">No se admite la implementación personalizada de interfaces de API de documentos XPS.</span><span class="sxs-lookup"><span data-stu-id="31d46-254">Custom implementation of XPS Document API interfaces is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_NOT_ENOUGH_GRADIENT_STOPS"></span><span id="xps_e_not_enough_gradient_stops"></span><dl> <span data-ttu-id="31d46-255"><dt><strong>XPS_E_NOT_ENOUGH_GRADIENT_STOPS</strong></dt> <dt>0x8052050b</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-255"><dt><strong>XPS_E_NOT_ENOUGH_GRADIENT_STOPS</strong></dt> <dt>0x8052050b</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-256">La colección de delimitadores de degradado tiene menos de dos paradas.</span><span class="sxs-lookup"><span data-stu-id="31d46-256">The gradient stop collection has fewer than two stops.</span></span> <span data-ttu-id="31d46-257">Una colección de delimitadores de degradado debe tener al menos dos delimitadores de degradado.</span><span class="sxs-lookup"><span data-stu-id="31d46-257">A gradient stop collection must have at least two gradient stops.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_ODD_BIDILEVEL"></span><span id="xps_e_odd_bidilevel"></span><dl> <span data-ttu-id="31d46-258"><dt><strong>XPS_E_ODD_BIDILEVEL</strong></dt> <dt>0x80520307</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-258"><dt><strong>XPS_E_ODD_BIDILEVEL</strong></dt> <dt>0x80520307</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-259">La cadena de texto se especificó como orientada lateralmente y de derecha a izquierda.</span><span class="sxs-lookup"><span data-stu-id="31d46-259">The text string was specified as being oriented sideways and right-to-left.</span></span> <span data-ttu-id="31d46-260">Si el texto está orientado lateralmente, no puede tener un nivel bidireccional que sea un valor impar (de derecha a izquierda).</span><span class="sxs-lookup"><span data-stu-id="31d46-260">If the text is oriented sideways, it cannot have a bidi level that is an odd value (right-to-left).</span></span> <span data-ttu-id="31d46-261">Del mismo modo, si el nivel bidi es un valor impar, el texto no se puede orientar lateralmente.</span><span class="sxs-lookup"><span data-stu-id="31d46-261">Likewise, if the bidi level is an odd value, the text cannot be oriented sideways.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_ONE_TO_ONE_MAPPING_EXPECTED"></span><span id="xps_e_one_to_one_mapping_expected"></span><dl> <span data-ttu-id="31d46-262"><dt><strong>XPS_E_ONE_TO_ONE_MAPPING_EXPECTED</strong></dt> <dt>0x80520308</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-262"><dt><strong>XPS_E_ONE_TO_ONE_MAPPING_EXPECTED</strong></dt> <dt>0x80520308</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-263">Las asignaciones de glifos no coinciden con el contenido de la cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="31d46-263">The glyph mappings do not match the Unicode string contents.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_PACKAGE_WRITER_NOT_CLOSED"></span><span id="xps_e_package_writer_not_closed"></span><dl> <span data-ttu-id="31d46-264"><dt><strong>XPS_E_PACKAGE_WRITER_NOT_CLOSED</strong></dt> <dt>0x8052050c</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-264"><dt><strong>XPS_E_PACKAGE_WRITER_NOT_CLOSED</strong></dt> <dt>0x8052050c</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-265">No se cerró el escritor de paquetes antes de su lanzamiento.</span><span class="sxs-lookup"><span data-stu-id="31d46-265">The package writer was not closed before it was released.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_RELATIONSHIP_EXTERNAL"></span><span id="xps_e_relationship_external"></span><dl> <span data-ttu-id="31d46-266"><dt><strong>XPS_E_RELATIONSHIP_EXTERNAL</strong></dt> <dt>0x8052050a</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-266"><dt><strong>XPS_E_RELATIONSHIP_EXTERNAL</strong></dt> <dt>0x8052050a</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-267">Una relación hace referencia a un elemento que está fuera del documento XPS.</span><span class="sxs-lookup"><span data-stu-id="31d46-267">A relationship refers to a part that is outside of the XPS document.</span></span> <span data-ttu-id="31d46-268">Todo el contenido que se va a representar en un documento XPS debe estar incluido en el documento XPS.</span><span class="sxs-lookup"><span data-stu-id="31d46-268">All content to be rendered in an XPS document must be contained in the XPS document.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_RESOURCE_NOT_OWNED"></span><span id="xps_e_resource_not_owned"></span><dl> <span data-ttu-id="31d46-269"><dt><strong>XPS_E_RESOURCE_NOT_OWNED</strong></dt> <dt>0x80520504</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-269"><dt><strong>XPS_E_RESOURCE_NOT_OWNED</strong></dt> <dt>0x80520504</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-270">Reservado.</span><span class="sxs-lookup"><span data-stu-id="31d46-270">Reserved.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_RESTRICTED_FONT_NOT_OBFUSCATED"></span><span id="xps_e_restricted_font_not_obfuscated"></span><dl> <span data-ttu-id="31d46-271"><dt><strong>XPS_E_RESTRICTED_FONT_NOT_OBFUSCATED</strong></dt> <dt>0x80520309</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-271"><dt><strong>XPS_E_RESTRICTED_FONT_NOT_OBFUSCATED</strong></dt> <dt>0x80520309</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-272"><em>Reservado</em>.</span><span class="sxs-lookup"><span data-stu-id="31d46-272"><em>Reserved</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_STRING_TOO_LONG"></span><span id="xps_e_string_too_long"></span><dl> <span data-ttu-id="31d46-273"><dt><strong>XPS_E_STRING_TOO_LONG</strong></dt> <dt>0x80520300</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-273"><dt><strong>XPS_E_STRING_TOO_LONG</strong></dt> <dt>0x80520300</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-274">Se produjo un desbordamiento de <strong>size_t</strong> durante un intento de copiar una cadena en un nuevo búfer.</span><span class="sxs-lookup"><span data-stu-id="31d46-274">A <strong>size_t</strong> overflow occurred during an attempt to copy a string into a new buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_TOO_MANY_INDICES"></span><span id="xps_e_too_many_indices"></span><dl> <span data-ttu-id="31d46-275"><dt><strong>XPS_E_TOO_MANY_INDICES</strong></dt> <dt>0x80520301</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-275"><dt><strong>XPS_E_TOO_MANY_INDICES</strong></dt> <dt>0x80520301</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-276">Había más índices de glifo que puntos de código Unicode.</span><span class="sxs-lookup"><span data-stu-id="31d46-276">There were more glyph indices than Unicode code points.</span></span> <span data-ttu-id="31d46-277">Si no hay ninguna asignación de glifo, el número de índices de glifo debe ser menor o igual que el número de puntos de código Unicode.</span><span class="sxs-lookup"><span data-stu-id="31d46-277">If there are no glyph mappings, the number of glyph indices must be less than or equal to the number of Unicode code points.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_UNAVAILABLE_PACKAGE"></span><span id="xps_e_unavailable_package"></span><dl> <span data-ttu-id="31d46-278"><dt><strong>XPS_E_UNAVAILABLE_PACKAGE</strong></dt> <dt>0x80520114</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-278"><dt><strong>XPS_E_UNAVAILABLE_PACKAGE</strong></dt> <dt>0x80520114</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-279">Se produjo un error grave y es posible que el contenido del OM de XPS no se pueda recuperar.</span><span class="sxs-lookup"><span data-stu-id="31d46-279">A severe error occurred and the contents of the XPS OM might be unrecoverable.</span></span> <span data-ttu-id="31d46-280">Es posible que algunos componentes del modelo de objetos de XPS se sigan pudiendo usar, pero deben comprobarse antes de usarse más.</span><span class="sxs-lookup"><span data-stu-id="31d46-280">Some components of the XPS OM might still be usable, but they will need to be verified before being used further.</span></span> <span data-ttu-id="31d46-281">Dado que el estado del OM XPS no se puede predecir después de que se devuelva este error, todos los componentes del OM XPS deben liberarse y descartarse.</span><span class="sxs-lookup"><span data-stu-id="31d46-281">Because the state of the XPS OM cannot be predicted after this error is returned, all components of the XPS OM should be released and discarded.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_UNEXPECTED_COLORPROFILE"></span><span id="xps_e_unexpected_colorprofile"></span><dl> <span data-ttu-id="31d46-282"><dt><strong>XPS_E_UNEXPECTED_COLORPROFILE</strong></dt> <dt>0x80520505</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-282"><dt><strong>XPS_E_UNEXPECTED_COLORPROFILE</strong></dt> <dt>0x80520505</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-283">Un perfil de color estaba presente cuando no se esperaba uno.</span><span class="sxs-lookup"><span data-stu-id="31d46-283">A color profile was present when one was not expected.</span></span> <span data-ttu-id="31d46-284">Solo se permite un perfil de color cuando el tipo de color es <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="31d46-284">A color profile is only allowed when the color type is <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a>.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_UNEXPECTED_CONTENT_TYPE"></span><span id="xps_e_unexpected_content_type"></span><dl> <span data-ttu-id="31d46-285"><dt><strong>XPS_E_UNEXPECTED_CONTENT_TYPE</strong></dt> <dt>0x80520008</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-285"><dt><strong>XPS_E_UNEXPECTED_CONTENT_TYPE</strong></dt> <dt>0x80520008</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-286">El destino de una relación no es el tipo esperado por el contexto de la relación.</span><span class="sxs-lookup"><span data-stu-id="31d46-286">The target of a relationship is not the type expected by the context of the relationship.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_UNEXPECTED_RELATIONSHIP_TYPE"></span><span id="xps_e_unexpected_relationship_type"></span><dl> <span data-ttu-id="31d46-287"><dt><strong>XPS_E_UNEXPECTED_RELATIONSHIP_TYPE</strong></dt> <dt>0x80520010</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-287"><dt><strong>XPS_E_UNEXPECTED_RELATIONSHIP_TYPE</strong></dt> <dt>0x80520010</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-288">No se reconoció el tipo de relación.</span><span class="sxs-lookup"><span data-stu-id="31d46-288">The relationship type was not recognized.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP"></span><span id="xps_e_unexpected_restricted_font_relationship"></span><dl> <span data-ttu-id="31d46-289"><dt><strong>XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520011</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-289"><dt><strong>XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520011</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-290">La colección de fuentes restringidas contiene una fuente sin restricciones.</span><span class="sxs-lookup"><span data-stu-id="31d46-290">The restricted font collection contains an unrestricted font.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_VISUAL_CIRCULAR_REF"></span><span id="xps_e_visual_circular_ref"></span><dl> <span data-ttu-id="31d46-291"><dt><strong>XPS_E_VISUAL_CIRCULAR_REF</strong></dt> <dt>0x80520501</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-291"><dt><strong>XPS_E_VISUAL_CIRCULAR_REF</strong></dt> <dt>0x80520501</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-292">Reservado.</span><span class="sxs-lookup"><span data-stu-id="31d46-292">Reserved.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_XKEY_ATTR_PRESENT_OUTSIDE_RES_DICT"></span><span id="xps_e_xkey_attr_present_outside_res_dict"></span><dl> <span data-ttu-id="31d46-293"><dt><strong>XPS_E_XKEY_ATTR_PRESENT_OUTSIDE_RES_DICT</strong></dt> <dt>0x80520400</dt> </span><span class="sxs-lookup"><span data-stu-id="31d46-293"><dt><strong>XPS_E_XKEY_ATTR_PRESENT_OUTSIDE_RES_DICT</strong></dt> <dt>0x80520400</dt> </span></span></dl></td>
<td><span data-ttu-id="31d46-294">Una geometría de ruta de acceso que no está en un diccionario de recursos tiene especificado un atributo <strong>x:Key</strong> .</span><span class="sxs-lookup"><span data-stu-id="31d46-294">A path geometry that is not in a resource dictionary has an <strong>x:Key</strong> attribute specified.</span></span> <span data-ttu-id="31d46-295">Las geometrías de ruta de acceso que no están en un diccionario de recursos no pueden tener un atributo <strong>x:Key</strong> .</span><span class="sxs-lookup"><span data-stu-id="31d46-295">Path geometries that are not in a resource dictionary cannot have an <strong>x:Key</strong> attribute.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="31d46-296">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31d46-296">Remarks</span></span>

<span data-ttu-id="31d46-297">Algunos métodos de la API de documentos XPS realizan llamadas a la API de [empaquetado](/previous-versions/windows/desktop/opc/packaging) .</span><span class="sxs-lookup"><span data-stu-id="31d46-297">Some XPS document API methods make calls to the [Packaging](/previous-versions/windows/desktop/opc/packaging) API.</span></span> <span data-ttu-id="31d46-298">Para obtener información sobre los valores devueltos de la API de empaquetado, consulte [errores de empaquetado](/previous-versions/windows/desktop/opc/packaging-errors).</span><span class="sxs-lookup"><span data-stu-id="31d46-298">For information about the Packaging API return values, see [Packaging Errors](/previous-versions/windows/desktop/opc/packaging-errors).</span></span>

## <a name="requirements"></a><span data-ttu-id="31d46-299">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31d46-299">Requirements</span></span>



| <span data-ttu-id="31d46-300">Requisito</span><span class="sxs-lookup"><span data-stu-id="31d46-300">Requirement</span></span> | <span data-ttu-id="31d46-301">Value</span><span class="sxs-lookup"><span data-stu-id="31d46-301">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31d46-302">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31d46-302">Minimum supported client</span></span><br/> | <span data-ttu-id="31d46-303">Windows 7, Windows Vista con SP2 y actualización de plataforma solo para aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="31d46-303">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="31d46-304">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31d46-304">Minimum supported server</span></span><br/> | <span data-ttu-id="31d46-305">Windows Server 2008 R2, Windows Server 2008 con SP2 y actualización de plataforma solo para aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="31d46-305">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="31d46-306">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31d46-306">Header</span></span><br/>                   | <dl> <span data-ttu-id="31d46-307"><dt>Xpsobjectmodel. h</dt></span><span class="sxs-lookup"><span data-stu-id="31d46-307"><dt>Xpsobjectmodel.h</dt></span></span> </dl>                                       |
| <span data-ttu-id="31d46-308">IDL</span><span class="sxs-lookup"><span data-stu-id="31d46-308">IDL</span></span><br/>                      | <dl> <span data-ttu-id="31d46-309"><dt>XpsObjectModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="31d46-309"><dt>XpsObjectModel.idl</dt></span></span> </dl>                                     |



## <a name="see-also"></a><span data-ttu-id="31d46-310">Vea también</span><span class="sxs-lookup"><span data-stu-id="31d46-310">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31d46-311">Control de errores en COM</span><span class="sxs-lookup"><span data-stu-id="31d46-311">Error Handling in COM</span></span>](../com/error-handling-in-com.md)
</dt> </dl>

 

