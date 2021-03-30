---
description: Microsoft Windows Search usa controladores de propiedades para extraer los valores de las propiedades de los elementos y utiliza el esquema del sistema de propiedades para determinar cómo se debe indizar una propiedad concreta.
ms.assetid: b475329a-1ed7-43a4-8e11-3700889a4ce9
title: Desarrollar controladores de propiedades para Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac96e47738040321025b7f600e2c91109b08d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275271"
---
# <a name="developing-property-handlers-for-windows-search"></a><span data-ttu-id="e35c0-103">Desarrollar controladores de propiedades para Windows Search</span><span class="sxs-lookup"><span data-stu-id="e35c0-103">Developing Property Handlers for Windows Search</span></span>

<span data-ttu-id="e35c0-104">Microsoft Windows Search usa controladores de propiedades para extraer los valores de las propiedades de los elementos y utiliza el esquema del sistema de propiedades para determinar cómo se debe indizar una propiedad concreta.</span><span class="sxs-lookup"><span data-stu-id="e35c0-104">Microsoft Windows Search uses property handlers to extract the values of properties from items and uses the property system schema to determine how a specific property should be indexed.</span></span> <span data-ttu-id="e35c0-105">Para leer e indexar los valores de propiedad, la búsqueda de Windows invoca los controladores de propiedades para mejorar la seguridad y la solidez.</span><span class="sxs-lookup"><span data-stu-id="e35c0-105">To read and index property values, property handlers are invoked out-of-process by Windows Search to improve security and robustness.</span></span> <span data-ttu-id="e35c0-106">En cambio, el explorador de Windows invoca los controladores de propiedades en proceso para leer y escribir valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e35c0-106">In contrast, property handlers are invoked in-process by Windows Explorer to read and write property values.</span></span>

<span data-ttu-id="e35c0-107">En este tema se complementa el tema [del sistema de propiedades](../properties/building-property-handlers.md) con información específica de Windows Search y contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="e35c0-107">This topic supplements the [Property System](../properties/building-property-handlers.md) topic with information specific to Windows Search and contains the following sections:</span></span>

-   [<span data-ttu-id="e35c0-108">Decisiones de diseño para los controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="e35c0-108">Design Decisions for Property Handlers</span></span>](#design-decisions-for-property-handlers)
    -   [<span data-ttu-id="e35c0-109">Decisiones de propiedades</span><span class="sxs-lookup"><span data-stu-id="e35c0-109">Property Decisions</span></span>](#property-decisions)
    -   [<span data-ttu-id="e35c0-110">Compatibilidad con texto completo</span><span class="sxs-lookup"><span data-stu-id="e35c0-110">Full-Text Support</span></span>](#full-text-support)
    -   [<span data-ttu-id="e35c0-111">Consideraciones de Implementatation del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="e35c0-111">Operating System Implementatation Considerations</span></span>](#operating-system-implementatation-considerations)
-   [<span data-ttu-id="e35c0-112">Escribir archivos de descripción de propiedades</span><span class="sxs-lookup"><span data-stu-id="e35c0-112">Writing Property Description Files</span></span>](#writing-property-description-files)
-   [<span data-ttu-id="e35c0-113">Implementar controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="e35c0-113">Implementing Property Handlers</span></span>](#implementing-property-handlers)
    -   [<span data-ttu-id="e35c0-114">IInitializeWithStream</span><span class="sxs-lookup"><span data-stu-id="e35c0-114">IInitializeWithStream</span></span>](#iinitializewithstream)
    -   [<span data-ttu-id="e35c0-115">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="e35c0-115">IPropertyStore</span></span>](#ipropertystore)
    -   [<span data-ttu-id="e35c0-116">IPropertyStoreCapabilities</span><span class="sxs-lookup"><span data-stu-id="e35c0-116">IPropertyStoreCapabilities</span></span>](#ipropertystorecapabilities)
-   [<span data-ttu-id="e35c0-117">Asegurarse de que los elementos se indexan</span><span class="sxs-lookup"><span data-stu-id="e35c0-117">Ensuring Your Items Get Indexed</span></span>](#ensuring-your-items-get-indexed)
-   [<span data-ttu-id="e35c0-118">Instalar y registrar controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="e35c0-118">Installing and Registering Property Handlers</span></span>](#installing-and-registering-property-handlers)
-   [<span data-ttu-id="e35c0-119">Probar y solucionar problemas de controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="e35c0-119">Testing and Troubleshooting Property Handlers</span></span>](#testing-and-troubleshooting-property-handlers)
    -   [<span data-ttu-id="e35c0-120">Pruebas de instalación y configuración</span><span class="sxs-lookup"><span data-stu-id="e35c0-120">Installation and Setup Tests</span></span>](#installation-and-setup-tests)
    -   [<span data-ttu-id="e35c0-121">Solucionar problemas de controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="e35c0-121">Troubleshooting Property Handlers</span></span>](#troubleshooting-property-handlers)
-   [<span data-ttu-id="e35c0-122">Usar controladores de propiedades de System-Supplied</span><span class="sxs-lookup"><span data-stu-id="e35c0-122">Using System-Supplied Property Handlers</span></span>](#using-system-supplied-property-handlers)
-   [<span data-ttu-id="e35c0-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e35c0-123">Related topics</span></span>](#related-topics)

 

## <a name="design-decisions-for-property-handlers"></a><span data-ttu-id="e35c0-124">Decisiones de diseño para los controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="e35c0-124">Design Decisions for Property Handlers</span></span>

<span data-ttu-id="e35c0-125">La implementación de controladores de propiedades implica los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="e35c0-125">Implementing property handlers involves the following steps:</span></span>

1.  <span data-ttu-id="e35c0-126">Tomar decisiones de diseño con respecto a las propiedades que desea admitir.</span><span class="sxs-lookup"><span data-stu-id="e35c0-126">Making design decisions regarding the properties you want to support.</span></span>
2.  <span data-ttu-id="e35c0-127">Crear un archivo de descripción de propiedad (. propDesc) para las propiedades que ya no están en el sistema de propiedades.</span><span class="sxs-lookup"><span data-stu-id="e35c0-127">Creating a Property Description (.propdesc) file for properties not already in the property system.</span></span>
3.  <span data-ttu-id="e35c0-128">Implementar y probar el controlador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e35c0-128">Implementing and testing the property handler.</span></span>
4.  <span data-ttu-id="e35c0-129">Instalación y registro de los archivos de descripción de propiedades y controladores de propiedades.</span><span class="sxs-lookup"><span data-stu-id="e35c0-129">Installing and registering the property handler and property description files.</span></span>
5.  <span data-ttu-id="e35c0-130">Prueba de la instalación y el registro del controlador de propiedades.</span><span class="sxs-lookup"><span data-stu-id="e35c0-130">Testing property handler installation and registration.</span></span>

<span data-ttu-id="e35c0-131">Antes de comenzar, debe tener en cuenta las siguientes preguntas de diseño:</span><span class="sxs-lookup"><span data-stu-id="e35c0-131">Before you begin, you need to consider the following design questions:</span></span>

-   <span data-ttu-id="e35c0-132">¿Qué propiedades tiene o debe admitir el formato de archivo?</span><span class="sxs-lookup"><span data-stu-id="e35c0-132">What properties does/should the file format support?</span></span>
-   <span data-ttu-id="e35c0-133">¿Estas propiedades ya están en el esquema del sistema?</span><span class="sxs-lookup"><span data-stu-id="e35c0-133">Are these properties already in the System schema?</span></span>
-   <span data-ttu-id="e35c0-134">¿Puedo usar un controlador de propiedades proporcionado por el sistema existente?</span><span class="sxs-lookup"><span data-stu-id="e35c0-134">Can I use an existing system-supplied property handler?</span></span>
-   <span data-ttu-id="e35c0-135">¿Qué propiedades se pueden mostrar a los usuarios finales?</span><span class="sxs-lookup"><span data-stu-id="e35c0-135">Which properties can be displayed to end users?</span></span>
-   <span data-ttu-id="e35c0-136">¿Qué propiedades pueden editar los usuarios?</span><span class="sxs-lookup"><span data-stu-id="e35c0-136">Which properties can users edit?</span></span>
-   <span data-ttu-id="e35c0-137">¿La compatibilidad con la búsqueda de texto completo procede de un controlador de propiedades o un filtro?</span><span class="sxs-lookup"><span data-stu-id="e35c0-137">Should support for full-text search come from a property handler or a filter?</span></span>
-   <span data-ttu-id="e35c0-138">¿Necesito compatibilidad con aplicaciones heredadas?</span><span class="sxs-lookup"><span data-stu-id="e35c0-138">Do I need to support legacy applications?</span></span> <span data-ttu-id="e35c0-139">Si es así, ¿qué puedo implementar?</span><span class="sxs-lookup"><span data-stu-id="e35c0-139">If so, what do I implement?</span></span>

> [!Note]  
> <span data-ttu-id="e35c0-140">Antes de continuar, vea [usar System-Supplied controladores de propiedades](#using-system-supplied-property-handlers) para ver si puede usar un controlador de propiedades proporcionado por el sistema, lo que le ahorra tiempo y recursos de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="e35c0-140">Before continuing, see [Using System-Supplied Property Handlers](#using-system-supplied-property-handlers) to see if you can use a system-supplied property handler, saving you both time and development resources.</span></span>

 

<span data-ttu-id="e35c0-141">Después de tomar estas decisiones, puede escribir descripciones formales de las propiedades personalizadas para que el motor de búsqueda de Windows pueda empezar a indizar los archivos y las propiedades.</span><span class="sxs-lookup"><span data-stu-id="e35c0-141">After you have made these decisions, you can write formal descriptions of your custom properties so that the Windows Search engine can begin indexing your files and properties.</span></span> <span data-ttu-id="e35c0-142">Estas descripciones formales son archivos XML, que se describen en el [esquema de descripción de propiedad](/previous-versions//cc144127(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e35c0-142">These formal descriptions are XML files, described in [Property Description Schema](/previous-versions//cc144127(v=vs.85)).</span></span>

### <a name="property-decisions"></a><span data-ttu-id="e35c0-143">Decisiones de propiedades</span><span class="sxs-lookup"><span data-stu-id="e35c0-143">Property Decisions</span></span>

<span data-ttu-id="e35c0-144">Al considerar las propiedades que se deben admitir, debe identificar las necesidades de indexación y búsqueda de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="e35c0-144">When considering which properties to support, you should identify your users' indexing and searching needs.</span></span> <span data-ttu-id="e35c0-145">Por ejemplo, puede identificar 100 propiedades potencialmente útiles para el tipo de archivo, pero es posible que los usuarios estén interesados en buscar solo en un puñado.</span><span class="sxs-lookup"><span data-stu-id="e35c0-145">For example, you may be able to identify one hundred potentially useful properties for your file type, but users may be interested in searching on only a handful.</span></span> <span data-ttu-id="e35c0-146">Además, puede que desee mostrar un grupo diferente, mayor o menor, de esas propiedades a los usuarios en el explorador de Windows y permitir que los usuarios modifiquen solo un subconjunto de las propiedades mostradas.</span><span class="sxs-lookup"><span data-stu-id="e35c0-146">Furthermore, you may want to display a different, larger or smaller, group of those properties to users in Windows Explorer, and allow users to edit only a subset of those properties displayed.</span></span>

<span data-ttu-id="e35c0-147">El tipo de archivo puede admitir cualquier propiedad personalizada que defina, así como un conjunto de propiedades definidas por el sistema.</span><span class="sxs-lookup"><span data-stu-id="e35c0-147">Your file type can support any custom properties you define, as well as a set of system-defined properties.</span></span> <span data-ttu-id="e35c0-148">Antes de crear una propiedad personalizada, revise [las propiedades del sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) para ver si la propiedad que desea admitir ya está definida por una propiedad del sistema.</span><span class="sxs-lookup"><span data-stu-id="e35c0-148">Before you create a custom property, please review [System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) to see if the property you want to support is already defined by a system property.</span></span> <span data-ttu-id="e35c0-149">Asegúrese siempre de que admite las propiedades más importantes definidas por el sistema.</span><span class="sxs-lookup"><span data-stu-id="e35c0-149">Always be sure you support the most important system-defined properties.</span></span>

<span data-ttu-id="e35c0-150">Se recomienda usar una matriz para ayudarle a diseñar sus propiedades:</span><span class="sxs-lookup"><span data-stu-id="e35c0-150">We recommend using a matrix to help you design your properties:</span></span>



| <span data-ttu-id="e35c0-151">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="e35c0-151">Property name</span></span> | <span data-ttu-id="e35c0-152">¿Es indexable?</span><span class="sxs-lookup"><span data-stu-id="e35c0-152">Is indexable?</span></span> | <span data-ttu-id="e35c0-153">¿Es visible?</span><span class="sxs-lookup"><span data-stu-id="e35c0-153">Is displayable?</span></span> | <span data-ttu-id="e35c0-154">¿Es editable?</span><span class="sxs-lookup"><span data-stu-id="e35c0-154">Is editable?</span></span> |
|---------------|---------------|-----------------|--------------|
| <span data-ttu-id="e35c0-155">property1</span><span class="sxs-lookup"><span data-stu-id="e35c0-155">property1</span></span>     | <span data-ttu-id="e35c0-156">Y</span><span class="sxs-lookup"><span data-stu-id="e35c0-156">Y</span></span>             | <span data-ttu-id="e35c0-157">Y</span><span class="sxs-lookup"><span data-stu-id="e35c0-157">Y</span></span>               | <span data-ttu-id="e35c0-158">N</span><span class="sxs-lookup"><span data-stu-id="e35c0-158">N</span></span>            |
| <span data-ttu-id="e35c0-159">propiedad...</span><span class="sxs-lookup"><span data-stu-id="e35c0-159">property...</span></span>   | <span data-ttu-id="e35c0-160">Y</span><span class="sxs-lookup"><span data-stu-id="e35c0-160">Y</span></span>             | <span data-ttu-id="e35c0-161">Y</span><span class="sxs-lookup"><span data-stu-id="e35c0-161">Y</span></span>               | <span data-ttu-id="e35c0-162">N</span><span class="sxs-lookup"><span data-stu-id="e35c0-162">N</span></span>            |
| <span data-ttu-id="e35c0-163">propiedad</span><span class="sxs-lookup"><span data-stu-id="e35c0-163">propertyn</span></span>     | <span data-ttu-id="e35c0-164">N</span><span class="sxs-lookup"><span data-stu-id="e35c0-164">N</span></span>             | <span data-ttu-id="e35c0-165">N</span><span class="sxs-lookup"><span data-stu-id="e35c0-165">N</span></span>               | <span data-ttu-id="e35c0-166">N</span><span class="sxs-lookup"><span data-stu-id="e35c0-166">N</span></span>            |



 

<span data-ttu-id="e35c0-167">Para cada una de estas propiedades, debe determinar qué atributos debe tener y, a continuación, describirlos formalmente en archivos XML de descripción de propiedad (. propDesc).</span><span class="sxs-lookup"><span data-stu-id="e35c0-167">For each of these properties, you need to determine what attributes it should have and then describe them formally in Property Description XML files (.propdesc).</span></span> <span data-ttu-id="e35c0-168">Los atributos incluyen el tipo de datos de la propiedad, la etiqueta, la cadena de ayuda y mucho más.</span><span class="sxs-lookup"><span data-stu-id="e35c0-168">Attributes include the property's data type, label, help string and more.</span></span> <span data-ttu-id="e35c0-169">En el caso de las propiedades indexables, debe prestar especial atención a los siguientes atributos de propiedad que se encuentran en el elemento XML [searchInfo](../properties/propdesc-schema-searchinfo.md)   del archivo de descripción de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="e35c0-169">For indexable properties, you should pay particular attention to the following property attributes found in the [searchInfo](../properties/propdesc-schema-searchinfo.md)   XML element of the Property Description file.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e35c0-170">Atributo</span><span class="sxs-lookup"><span data-stu-id="e35c0-170">Attribute</span></span></th>
<th><span data-ttu-id="e35c0-171">Descripción</span><span class="sxs-lookup"><span data-stu-id="e35c0-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e35c0-172">inInvertedIndex</span><span class="sxs-lookup"><span data-stu-id="e35c0-172">inInvertedIndex</span></span></td>
<td><span data-ttu-id="e35c0-173">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e35c0-173">Optional.</span></span> <span data-ttu-id="e35c0-174">Indica si un valor de propiedad de cadena debe dividirse en palabras y en cada palabra almacenada en el índice invertido.</span><span class="sxs-lookup"><span data-stu-id="e35c0-174">Indicates whether a string property value should be broken into words and each word stored in the inverted index.</span></span> <span data-ttu-id="e35c0-175">El índice invertido permite una búsqueda eficaz de palabras y frases sobre el valor de propiedad mediante Contains o FREETEXT (por ejemplo, SELECT... DONDE contiene &quot; sometext &quot; ).</span><span class="sxs-lookup"><span data-stu-id="e35c0-175">The inverted index enables efficient searching for words and phrases over the property value using CONTAINS or FREETEXT (for example, SELECT ... WHERE CONTAINS &quot;sometext&quot;).</span></span> <span data-ttu-id="e35c0-176">Si se establece en <strong>false</strong>, las búsquedas se realizan en toda la cadena.</span><span class="sxs-lookup"><span data-stu-id="e35c0-176">If set to <strong>FALSE</strong>, searches are done against the whole string.</span></span> <span data-ttu-id="e35c0-177">La mayoría de las propiedades de cadena deben tener esta propiedad establecida en <strong>true</strong>; las propiedades que no son de cadena deben tener esta propiedad establecida en <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="e35c0-177">Most string properties should have this set to <strong>TRUE</strong>; non-string properties should have this set to <strong>FALSE</strong>.</span></span> <span data-ttu-id="e35c0-178">El valor predeterminado es <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="e35c0-178">The default is <strong>FALSE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e35c0-179">isColumn</span><span class="sxs-lookup"><span data-stu-id="e35c0-179">isColumn</span></span></td>
<td><span data-ttu-id="e35c0-180">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e35c0-180">Optional.</span></span> <span data-ttu-id="e35c0-181">Indica si la propiedad debe almacenarse en la base de datos de Windows Search como una columna.</span><span class="sxs-lookup"><span data-stu-id="e35c0-181">Indicates whether the property should be stored in the Windows Search database as a column.</span></span> <span data-ttu-id="e35c0-182">Almacenar la propiedad como una columna permite recuperar, ordenar, agrupar y filtrar (es decir, usar cualquier predicado excepto Contains o FREETEXT) en el valor de la columna completa.</span><span class="sxs-lookup"><span data-stu-id="e35c0-182">Storing the property as a column enables retrieving, sorting, grouping, and filtering (that is, using any predicate except CONTAINS or FREETEXT) on the whole column value.</span></span> <span data-ttu-id="e35c0-183">Las propiedades que se muestran al usuario deben tener este valor establecido en <strong>true</strong> a menos que sea una propiedad de texto muy grande (como el cuerpo de un documento) que se buscaría en el índice invertido.</span><span class="sxs-lookup"><span data-stu-id="e35c0-183">Properties displayed to the user should have this set to <strong>TRUE</strong> unless it is a very large textual property (like the body of a document) that would be searched in the inverted index.</span></span> <span data-ttu-id="e35c0-184">El valor predeterminado es <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="e35c0-184">The default is <strong>FALSE</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e35c0-185">isColumnSparse</span><span class="sxs-lookup"><span data-stu-id="e35c0-185">isColumnSparse</span></span></td>
<td><span data-ttu-id="e35c0-186">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e35c0-186">Optional.</span></span> <span data-ttu-id="e35c0-187">Indica si una propiedad no necesita espacio si el valor es <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="e35c0-187">Indicates whether a property takes no space if the value is <strong>NULL</strong>.</span></span> <span data-ttu-id="e35c0-188">Una propiedad no dispersa tiene espacio para cada elemento, incluso si el valor es <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="e35c0-188">A non-sparse property takes space for every item, even if the value is <strong>NULL</strong>.</span></span> <span data-ttu-id="e35c0-189">Si la propiedad tiene varios valores, este atributo siempre es <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="e35c0-189">If the property is multi-valued, this attribute is always <strong>TRUE</strong>.</span></span> <span data-ttu-id="e35c0-190">Este atributo solo debe ser <strong>false</strong> si hay un valor para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="e35c0-190">This attribute should be <strong>FALSE</strong> only if a value is present for every item.</span></span> <span data-ttu-id="e35c0-191">El valor predeterminado es <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="e35c0-191">The default is <strong>TRUE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e35c0-192">columnIndexType</span><span class="sxs-lookup"><span data-stu-id="e35c0-192">columnIndexType</span></span></td>
<td><span data-ttu-id="e35c0-193">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e35c0-193">Optional.</span></span> <span data-ttu-id="e35c0-194">Para optimizar las consultas, el motor de búsqueda de Windows puede crear índices secundarios para propiedades que tienen isColumn =<strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="e35c0-194">To optimize querying, the Windows Search engine can create secondary indices for properties that have isColumn=<strong>TRUE</strong>.</span></span> <span data-ttu-id="e35c0-195">Esto requiere más procesamiento y espacio en disco durante la indexación, pero mejora el rendimiento durante la consulta.</span><span class="sxs-lookup"><span data-stu-id="e35c0-195">This requires more processing and disk space during indexing, but improves performance during querying.</span></span> <span data-ttu-id="e35c0-196">Si la propiedad tiende a ordenarse, agruparse o filtrarse (es decir, usando =,! =, <, >, LIKE, coincide) con frecuencia por usuarios, este atributo debe establecerse en &quot; disco &quot; .</span><span class="sxs-lookup"><span data-stu-id="e35c0-196">If the property tends to be sorted, grouped, or filtered (that is, using =, !=, <, >, LIKE, MATCHES) frequently by users, this attribute should be set to &quot;OnDisk&quot;.</span></span> <span data-ttu-id="e35c0-197">El valor predeterminado es &quot; NotIndexed &quot; .</span><span class="sxs-lookup"><span data-stu-id="e35c0-197">The default is &quot;NotIndexed&quot;.</span></span> <span data-ttu-id="e35c0-198">Valores válidos son:</span><span class="sxs-lookup"><span data-stu-id="e35c0-198">The following values are valid:</span></span>
<ul>
<li><span data-ttu-id="e35c0-199">NotIndexed: no se crea ningún índice secundario.</span><span class="sxs-lookup"><span data-stu-id="e35c0-199">NotIndexed: No secondary index is created.</span></span></li>
<li><span data-ttu-id="e35c0-200">Disco: cree y almacene un índice secundario en el disco.</span><span class="sxs-lookup"><span data-stu-id="e35c0-200">OnDisk: Create and store a secondary index on disk.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e35c0-201">Tamañomáximo</span><span class="sxs-lookup"><span data-stu-id="e35c0-201">maxSize</span></span></td>
<td><span data-ttu-id="e35c0-202">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e35c0-202">Optional.</span></span> <span data-ttu-id="e35c0-203">Indica el tamaño máximo permitido para el valor de propiedad almacenado en la base de datos de Windows Search.</span><span class="sxs-lookup"><span data-stu-id="e35c0-203">Indicates the maximum size allowed for the property value stored in the Windows search database.</span></span> <span data-ttu-id="e35c0-204">Este límite se aplica a los elementos indvidual de un vector, no al vector en su totalidad.</span><span class="sxs-lookup"><span data-stu-id="e35c0-204">This limit applies to the indvidual elements of a vector, not the vector as a whole.</span></span> <span data-ttu-id="e35c0-205">Se truncan los valores que superen este tamaño.</span><span class="sxs-lookup"><span data-stu-id="e35c0-205">Values beyond this size are truncated.</span></span> <span data-ttu-id="e35c0-206">El valor predeterminado es &quot; 128 &quot; (bytes).</span><span class="sxs-lookup"><span data-stu-id="e35c0-206">The default is &quot;128&quot; (bytes).</span></span><br/> <span data-ttu-id="e35c0-207">Actualmente, Windows Search no usa maxSize al calcular la cantidad de datos que acepta de un archivo.</span><span class="sxs-lookup"><span data-stu-id="e35c0-207">Currently, Windows Search does not use the maxSize when calculating the amount of data it accepts from a file.</span></span> <span data-ttu-id="e35c0-208">En su lugar, el límite que usa Windows Search es el producto del tamaño del archivo y el MaxGrowFactor (tamaño de archivo N \* MaxGrowFactor) leído del registro en HKEY_LOCAL_MACHINE->software->Microsoft->Windows Search->Gather Manager->MaxGrowFactor.</span><span class="sxs-lookup"><span data-stu-id="e35c0-208">Instead, the limit Windows Search uses is the product of the size of the file and the MaxGrowFactor (file size N \* MaxGrowFactor) read from the registry at HKEY_LOCAL_MACHINE->Software->Microsoft->Windows Search->Gathering Manager->MaxGrowFactor.</span></span> <span data-ttu-id="e35c0-209">El valor predeterminado de MaxGrowFactor es cuatro (4).</span><span class="sxs-lookup"><span data-stu-id="e35c0-209">The default MaxGrowFactor is four (4).</span></span> <span data-ttu-id="e35c0-210">Por lo tanto, si el tipo de archivo tiende a ser pequeño en tamaño total pero tiene propiedades más grandes, es posible que Windows Search no acepte todos los datos de propiedad que desea emitir.</span><span class="sxs-lookup"><span data-stu-id="e35c0-210">Consequently, if your file type tends to be small in total size but have larger properties, Windows Search may not accept all the property data you want to emit.</span></span> <span data-ttu-id="e35c0-211">Sin embargo, puede aumentar el MaxGrowFactor para que se adapte a sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="e35c0-211">However, you can increase the MaxGrowFactor to suit your needs.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="e35c0-212">En el caso del atributo columnIndexType, la ventaja de las consultas más rápidas debe sopesarse con el mayor tiempo de indización y los costos de espacio que pueden tener los índices secundarios.</span><span class="sxs-lookup"><span data-stu-id="e35c0-212">For the columnIndexType attribute, the benefit of faster queries needs to be weighed against the greater indexing time and space costs that the secondary indices can incur.</span></span> <span data-ttu-id="e35c0-213">Sin embargo, este costo solo se paga por los elementos que tienen un valor distinto de **null** , por lo que la mayoría de las propiedades pueden tener este atributo establecido en "disco".</span><span class="sxs-lookup"><span data-stu-id="e35c0-213">However, this cost is only paid for items that have a non-**null** value, so for most properties can have this attribute set to "OnDisk".</span></span>

 

### <a name="full-text-support"></a><span data-ttu-id="e35c0-214">Compatibilidad con texto completo</span><span class="sxs-lookup"><span data-stu-id="e35c0-214">Full-Text Support</span></span>

<span data-ttu-id="e35c0-215">En términos generales, la búsqueda de texto completo es compatible con los componentes denominados [filtros](-search-3x-wds-extidx-filters.md); sin embargo, para los tipos de archivos basados en texto con formatos de archivo poco complicados, los controladores de propiedades pueden proporcionar esta funcionalidad con menos esfuerzo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="e35c0-215">Generally speaking, full-text search is supported by components called [filters](-search-3x-wds-extidx-filters.md); however, for text-based file types with uncomplicated file formats, property handlers may be able to provide this functionality with less development effort.</span></span> <span data-ttu-id="e35c0-216">Debe revisar la sección [contenido de texto completo](../properties/building-property-handlers-property-handlers.md) para obtener una comparación de la funcionalidad del filtro y del controlador de propiedades para ayudarle a decidir cuál es el mejor para su tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="e35c0-216">You should review the [Full-Text Contents](../properties/building-property-handlers-property-handlers.md) section for a comparison of filter and property handler functionality to help you decide what is best for your file type.</span></span> <span data-ttu-id="e35c0-217">Una importancia concreta es el hecho de que los filtros pueden controlar varios identificadores de código de idioma (LCID) por archivo, mientras que los controladores de propiedades no pueden.</span><span class="sxs-lookup"><span data-stu-id="e35c0-217">Of particular importance is the fact that filters can handle multiple language code identifiers (LCIDs) per file while property handlers cannot.</span></span>

> [!Note]  
> <span data-ttu-id="e35c0-218">Dado que los controladores de propiedades no pueden fragmentar el contenido de la manera en que se filtran los filtros, los archivos grandes (incluso si son formatos de archivo no complicados) se deben cargar completamente en la memoria.</span><span class="sxs-lookup"><span data-stu-id="e35c0-218">Because property handlers cannot chunk content the way filters can, large files (even if they are uncomplicated file formats) must be completely loaded into memory.</span></span>

 

### <a name="operating-system-implementatation-considerations"></a><span data-ttu-id="e35c0-219">Consideraciones de Implementatation del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="e35c0-219">Operating System Implementatation Considerations</span></span>

### <a name="implementation-information-for-windows-7"></a><span data-ttu-id="e35c0-220">Información de implementación de Windows 7</span><span class="sxs-lookup"><span data-stu-id="e35c0-220">Implementation Information for Windows 7</span></span>

<span data-ttu-id="e35c0-221">En Windows 7 y versiones posteriores, hay un nuevo comportamiento al registrar un controlador de propiedades, [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)o una nueva extensión.</span><span class="sxs-lookup"><span data-stu-id="e35c0-221">In Windows 7 and later, there is new behavior when registering a property handler, [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), or new extension.</span></span> <span data-ttu-id="e35c0-222">Cuando se instala un nuevo controlador de propiedades o **IFilter** , los archivos con las extensiones correspondientes se reindexan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="e35c0-222">When a new property handler and/or **IFilter** is installed, files with the corresponding extensions are automatically reindexed.</span></span>

<span data-ttu-id="e35c0-223">En Windows 7 se recomienda instalar un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) junto con sus controladores de propiedades correspondientes y que el **IFilter** se registre antes que el controlador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e35c0-223">In Windows 7 it is recommended that an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is installed in conjunction with its corresponding property handlers, and that the **IFilter** is registered before the property handler.</span></span> <span data-ttu-id="e35c0-224">El registro del controlador de propiedades inicia una reindización inmediata de archivos indizados previamente sin requerir primero un reinicio, y aprovecha los IFilter registrados previamente para el propósito de la indización de contenido.</span><span class="sxs-lookup"><span data-stu-id="e35c0-224">The registration of the property handler initiates immediate re-indexing of previously indexed files without first requiring a reboot, and takes advantage of any previously registered IFilter(s) for the purpose of content indexing.</span></span>

<span data-ttu-id="e35c0-225">Si solo hay un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) instalado, sin un controlador de propiedades correspondiente, la reindexación automática se produce después de un reinicio del servicio de indización o de un reinicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="e35c0-225">If only an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is installed, without a corresponding property handler, then automatic reindexing occurs either after a restart of the indexing service, or a reboot of the system.</span></span>

<span data-ttu-id="e35c0-226">En el caso de las marcas de descripción de propiedades específicas de Windows 7, vea los temas de referencia siguientes:</span><span class="sxs-lookup"><span data-stu-id="e35c0-226">For property description flags specific to Windows 7, see the following reference topics:</span></span>

-   [<span data-ttu-id="e35c0-227">GETPROPERTYSTOREFLAGS</span><span class="sxs-lookup"><span data-stu-id="e35c0-227">GETPROPERTYSTOREFLAGS</span></span>](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)
-   [<span data-ttu-id="e35c0-228">PROPDESC \_ COLUMNINDEX ( \_ tipo)</span><span class="sxs-lookup"><span data-stu-id="e35c0-228">PROPDESC\_COLUMNINDEX\_TYPE</span></span>](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)
-   [<span data-ttu-id="e35c0-229">PROPDESC \_ \_ marcas SEARCHINFO</span><span class="sxs-lookup"><span data-stu-id="e35c0-229">PROPDESC\_SEARCHINFO\_FLAGS</span></span>](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)

### <a name="implementation-information-for-windows-vista-and-earlier"></a><span data-ttu-id="e35c0-230">Información de implementación de Windows Vista y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="e35c0-230">Implementation Information for Windows Vista and Earlier</span></span>

<span data-ttu-id="e35c0-231">Antes de Windows Vista, los filtros proporcionaban compatibilidad para analizar y enumerar el contenido y las propiedades de los archivos.</span><span class="sxs-lookup"><span data-stu-id="e35c0-231">Prior to Windows Vista, filters provided support for parsing and enumerating file content and properties.</span></span> <span data-ttu-id="e35c0-232">Con la introducción del sistema de propiedades, los controladores de propiedades controlan las propiedades de archivo mientras que los filtros controlan el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="e35c0-232">With the introduction of the property system, property handlers handle file properties while filters handle file content.</span></span> <span data-ttu-id="e35c0-233">En Windows Vista, solo necesita desarrollar una implementación parcial de la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)en coordinación con un controlador de propiedades, como se describe en [procedimientos recomendados para crear controladores de filtro en Windows Search](-search-3x-wds-extidx-filters.md).</span><span class="sxs-lookup"><span data-stu-id="e35c0-233">For Windows Vista, you need develop only a partial implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)interface in coordination with a property handler, as described in [Best Practices for Creating Filter Handlers in Windows Search](-search-3x-wds-extidx-filters.md).</span></span>

<span data-ttu-id="e35c0-234">Aunque el sistema de propiedades también se incluye con la instalación de Windows Search para Windows XP, las aplicaciones heredadas y de terceros pueden requerir que los filtros controlen tanto el contenido como las propiedades.</span><span class="sxs-lookup"><span data-stu-id="e35c0-234">While the property system is also included with the Windows Search installation for Windows XP, third-party and legacy applications may require that filters handle both content and properties.</span></span> <span data-ttu-id="e35c0-235">Por lo tanto, si está desarrollando en la plataforma Windows XP, debe proporcionar una implementación de filtro completa, así como un controlador de propiedades para el tipo de archivo o la propiedad personalizada.</span><span class="sxs-lookup"><span data-stu-id="e35c0-235">Therefore, if you are developing on the Windows XP platform, you should provide a full filter implementation as well as a property handler for your file type or custom property.</span></span>

 

## <a name="writing-property-description-files"></a><span data-ttu-id="e35c0-236">Escribir archivos de descripción de propiedades</span><span class="sxs-lookup"><span data-stu-id="e35c0-236">Writing Property Description Files</span></span>

<span data-ttu-id="e35c0-237">La estructura de los archivos XML de descripción de propiedad (. propDesc) se describe en el tema [propertyDescription](../properties/propdesc-schema-propertydescription.md) .</span><span class="sxs-lookup"><span data-stu-id="e35c0-237">The structure of property description XML files (.propdesc) is described in the [propertyDescription](../properties/propdesc-schema-propertydescription.md) topic.</span></span> <span data-ttu-id="e35c0-238">Un interés particular para la búsqueda son los atributos del elemento [searchInfo](../properties/propdesc-schema-searchinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="e35c0-238">Of particular interest for search are the attributes of the [searchInfo](../properties/propdesc-schema-searchinfo.md) element.</span></span> <span data-ttu-id="e35c0-239">Una vez que haya decidido qué propiedades se deben admitir, debe crear y registrar los archivos de descripción de propiedades para cada una de las propiedades.</span><span class="sxs-lookup"><span data-stu-id="e35c0-239">Once you've decided which properties to support, you need to create and register property description files for each properties.</span></span> <span data-ttu-id="e35c0-240">Al registrar los archivos. propDesc, se incluyen en la lista de descripción de la propiedad del esquema y se convierten en nombres de columna en el almacén de propiedades del motor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e35c0-240">When you register your .propdesc files, they are included in the schema's property description list and become column names within the Search engine's property store.</span></span>

<span data-ttu-id="e35c0-241">Puede registrar las descripciones de propiedades personalizadas mediante la función [PSRegisterPropertySchema](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) , una API de contenedor que llama a IPropertySystem:: RegisterPropertySchema del subsistema de esquema.</span><span class="sxs-lookup"><span data-stu-id="e35c0-241">You can register your custom property descriptions using the [PSRegisterPropertySchema](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) function, a wrapper API that calls the schema subsystem's IPropertySystem::RegisterPropertySchema.</span></span> <span data-ttu-id="e35c0-242">Esta función informa al subsistema de esquema de la adición de archivos de esquema de descripción de propiedad (. propDesc), mediante rutas de acceso de archivo a los archivos. propDesc en el equipo local, normalmente el directorio de instalación de la aplicación en "archivos de programa".</span><span class="sxs-lookup"><span data-stu-id="e35c0-242">This function informs the schema subsystem of the addition of property description schema (.propdesc) files, using file path(s) to the .propdesc file(s) on the local machine, usually the application's install directory under "Program Files".</span></span> <span data-ttu-id="e35c0-243">Normalmente, una instalación o una aplicación (por ejemplo, el instalador del controlador de propiedad) llamará a este método después de instalar los archivos. propDesc.</span><span class="sxs-lookup"><span data-stu-id="e35c0-243">Typically, a setup or application (for example, your property handler installer) will call this method after installing the .propdesc file(s).</span></span>

 

## <a name="implementing-property-handlers"></a><span data-ttu-id="e35c0-244">Implementar controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="e35c0-244">Implementing Property Handlers</span></span>

<span data-ttu-id="e35c0-245">El desarrollo de un controlador de propiedades implica la implementación de las interfaces siguientes:</span><span class="sxs-lookup"><span data-stu-id="e35c0-245">Developing a property handler involves implementing the following interfaces:</span></span>

-   <span data-ttu-id="e35c0-246">IInitialzeWithStream: proporciona la inicialización basada en secuencias del controlador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e35c0-246">IInitialzeWithStream: Provides stream-based initialization of your property handler.</span></span>
-   <span data-ttu-id="e35c0-247">IPropertyStore: enumera, obtiene y establece los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e35c0-247">IPropertyStore: Enumerates, gets, and sets property values.</span></span>
-   <span data-ttu-id="e35c0-248">IPropertyStoreCapabilities: opcional.</span><span class="sxs-lookup"><span data-stu-id="e35c0-248">IPropertyStoreCapabilities: Optional.</span></span> <span data-ttu-id="e35c0-249">Identifica si los usuarios pueden editar una propiedad desde una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e35c0-249">Identifies whether users can edit a property from a user interface.</span></span>

### <a name="iinitializewithstream"></a><span data-ttu-id="e35c0-250">IInitializeWithStream</span><span class="sxs-lookup"><span data-stu-id="e35c0-250">IInitializeWithStream</span></span>

<span data-ttu-id="e35c0-251">Tal y como se describe en el tema [sistema de propiedades](../properties/building-property-handlers.md) , se recomienda encarecidamente implementar controladores de propiedades con **IInitializeWithStream** para realizar la inicialización basada en secuencias.</span><span class="sxs-lookup"><span data-stu-id="e35c0-251">As described in the [Property System](../properties/building-property-handlers.md) topic, we strongly recommend implementing property handlers with **IInitializeWithStream** to do stream-based initialization.</span></span> <span data-ttu-id="e35c0-252">Si decide no implementar IInitializeWithStream, el controlador de propiedad debe dejar de ejecutarse en el proceso de aislamiento estableciendo la marca DisableProcessIsolation en la clave del registro del controlador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e35c0-252">If you chose not to implement IInitializeWithStream, the property handler must opt out of running in the isolation process by setting the DisableProcessIsolation flag on the property handler's registry key.</span></span> <span data-ttu-id="e35c0-253">Generalmente, la deshabilitación del aislamiento de procesos está destinada únicamente a los controladores de propiedades heredadas y se debe evitar por cualquier nuevo código.</span><span class="sxs-lookup"><span data-stu-id="e35c0-253">Disabling process isolation is generally intended only for legacy property handlers and should be strenuously avoided by any new code.</span></span>

### <a name="ipropertystore"></a><span data-ttu-id="e35c0-254">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="e35c0-254">IPropertyStore</span></span>

<span data-ttu-id="e35c0-255">Para crear un controlador de propiedades, debe implementar la interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) con los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="e35c0-255">To create a property handler, you must implement the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface with the following methods.</span></span>



| <span data-ttu-id="e35c0-256">Método</span><span class="sxs-lookup"><span data-stu-id="e35c0-256">Method</span></span>   | <span data-ttu-id="e35c0-257">Descripción</span><span class="sxs-lookup"><span data-stu-id="e35c0-257">Description</span></span>                                                         |
|----------|---------------------------------------------------------------------|
| <span data-ttu-id="e35c0-258">Commit</span><span class="sxs-lookup"><span data-stu-id="e35c0-258">Commit</span></span>   | <span data-ttu-id="e35c0-259">Guarda un cambio de propiedad en el archivo.</span><span class="sxs-lookup"><span data-stu-id="e35c0-259">Saves a property change to the file.</span></span>                                |
| <span data-ttu-id="e35c0-260">GetAt</span><span class="sxs-lookup"><span data-stu-id="e35c0-260">GetAt</span></span>    | <span data-ttu-id="e35c0-261">Recupera una clave de propiedad de la matriz de propiedades de un elemento.</span><span class="sxs-lookup"><span data-stu-id="e35c0-261">Retrieves a property key from an item's array of properties.</span></span>        |
| <span data-ttu-id="e35c0-262">GetCount</span><span class="sxs-lookup"><span data-stu-id="e35c0-262">GetCount</span></span> | <span data-ttu-id="e35c0-263">Obtiene el número de propiedades adjuntas al archivo.</span><span class="sxs-lookup"><span data-stu-id="e35c0-263">Gets the number of properties attached to the file.</span></span>                 |
| <span data-ttu-id="e35c0-264">GetValue</span><span class="sxs-lookup"><span data-stu-id="e35c0-264">GetValue</span></span> | <span data-ttu-id="e35c0-265">Recupera los datos de una propiedad concreta.</span><span class="sxs-lookup"><span data-stu-id="e35c0-265">Retrieves data for a specific property.</span></span>                             |
| <span data-ttu-id="e35c0-266">SetValue</span><span class="sxs-lookup"><span data-stu-id="e35c0-266">SetValue</span></span> | <span data-ttu-id="e35c0-267">Establece un nuevo valor de propiedad o reemplaza o quita un valor existente.</span><span class="sxs-lookup"><span data-stu-id="e35c0-267">Sets a new property value or replaces or removes an existing value.</span></span> |



 

 

 

<span data-ttu-id="e35c0-268">En la documentación de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) se incluyen consideraciones importantes para implementar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="e35c0-268">Important considerations for implementing this interface are included in the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) documentation.</span></span>

> [!Note]  
> <span data-ttu-id="e35c0-269">Si el controlador de propiedad emite varios valores para la misma propiedad para un elemento determinado, solo el último valor emitido se almacena en el catálogo.</span><span class="sxs-lookup"><span data-stu-id="e35c0-269">If your property handler emits multiple values for the same property for a given item, only the last value emitted is stored in the catalog.</span></span>

 

 

### <a name="ipropertystorecapabilities"></a><span data-ttu-id="e35c0-270">IPropertyStoreCapabilities</span><span class="sxs-lookup"><span data-stu-id="e35c0-270">IPropertyStoreCapabilities</span></span>

<span data-ttu-id="e35c0-271">Opcionalmente, los controladores de propiedades pueden implementar esta interfaz para deshabilitar la capacidad de un usuario para editar propiedades específicas.</span><span class="sxs-lookup"><span data-stu-id="e35c0-271">Property handlers can optionally implement this interface to disable a user's ability to edit specific properties.</span></span> <span data-ttu-id="e35c0-272">Normalmente, estas propiedades se pueden editar en la página de detalles y el panel, pero no se pueden editar en el controlador de propiedades de implementación.</span><span class="sxs-lookup"><span data-stu-id="e35c0-272">These properties are normally editable in the Details page and pane but editing them is not allowed under the implementing property handler.</span></span> <span data-ttu-id="e35c0-273">La implementación correcta de esta interfaz proporciona una mejor experiencia de usuario que la alternativa, un error de tiempo de ejecución simple del shell.</span><span class="sxs-lookup"><span data-stu-id="e35c0-273">Implementing this interface correctly provides a better user experience than the alternative—a simple run-time error from the Shell.</span></span>

 

## <a name="ensuring-your-items-get-indexed"></a><span data-ttu-id="e35c0-274">Asegurarse de que los elementos se indexan</span><span class="sxs-lookup"><span data-stu-id="e35c0-274">Ensuring Your Items Get Indexed</span></span>

<span data-ttu-id="e35c0-275">Ahora que ha implementado el controlador de propiedad, desea asegurarse de que los elementos que el controlador está registrado para la indexación se han indizado.</span><span class="sxs-lookup"><span data-stu-id="e35c0-275">Now that you've implemented your property handler, you want to make sure the items your handler is registered for get indexed.</span></span> <span data-ttu-id="e35c0-276">Puede usar el [Administrador de catálogos](-search-3x-wds-mngidx-catalog-manager.md) para iniciar la reindización y también puede usar el [Administrador de ámbito de rastreo](-search-3x-wds-extidx-csm.md) para configurar las reglas predeterminadas que indican las direcciones URL que desea que rastree el indexador.</span><span class="sxs-lookup"><span data-stu-id="e35c0-276">You can use the [Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) to initiate re-indexing, and you can also use the [Crawl Scope Manager](-search-3x-wds-extidx-csm.md) to set up default rules indicating the URLs you want the Indexer to crawl.</span></span> <span data-ttu-id="e35c0-277">Otra opción es seguir el ejemplo de código REINDEX en los [ejemplos del SDK de Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span><span class="sxs-lookup"><span data-stu-id="e35c0-277">Another option is to follow the ReIndex code sample in the [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span></span>

<span data-ttu-id="e35c0-278">Para obtener más información, consulte [uso del administrador de catálogo](-search-3x-wds-mngidx-catalog-manager.md) y [uso del administrador de ámbito de rastreo](-search-3x-wds-extidx-csm.md).</span><span class="sxs-lookup"><span data-stu-id="e35c0-278">For further information, refer to [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span></span>

 

## <a name="installing-and-registering-property-handlers"></a><span data-ttu-id="e35c0-279">Instalar y registrar controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="e35c0-279">Installing and Registering Property Handlers</span></span>

<span data-ttu-id="e35c0-280">Con el controlador de propiedades implementado, debe estar registrado y su extensión de nombre de archivo asociada al controlador.</span><span class="sxs-lookup"><span data-stu-id="e35c0-280">With the property handler implemented, it must be registered and its file name extension associated with the handler.</span></span> <span data-ttu-id="e35c0-281">En el ejemplo siguiente se muestran las claves y los valores del registro necesarios para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="e35c0-281">The following example shows the registry keys and values required to do this.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {<CLSID for property handler>}
         (Default) = <Property Handler Name>
         InProcServer32
            (Default) = <full path to property handler dll>
            ThreadingModel = <your threading model>
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PropertySystem
                  PropertyHandlers
                     <.fileextention>
                        (Default) = {<CLSID for property handler>}
```

 

## <a name="testing-and-troubleshooting-property-handlers"></a><span data-ttu-id="e35c0-282">Probar y solucionar problemas de controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="e35c0-282">Testing and Troubleshooting Property Handlers</span></span>

<span data-ttu-id="e35c0-283">En la lista siguiente se proporcionan consejos sobre los tipos de pruebas que se deben realizar:</span><span class="sxs-lookup"><span data-stu-id="e35c0-283">The following list provides advice on the kinds of tests you should perform:</span></span>

-   <span data-ttu-id="e35c0-284">Pruebe la obtención de resultados de cada propiedad única admitida por el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="e35c0-284">Test getting output from every single property supported by the file type.</span></span>
-   <span data-ttu-id="e35c0-285">Use valores de propiedad grande, por ejemplo, para usar una metaetiqueta grande en documentos HTML.</span><span class="sxs-lookup"><span data-stu-id="e35c0-285">Use big property values, for example, use a large metatag in HTML documents.</span></span>
-   <span data-ttu-id="e35c0-286">Compruebe que el controlador de propiedad no pierde los identificadores de archivo editándolo después de obtener la salida del controlador de propiedad o mediante una herramienta como oh.exe antes y después de enumerar las propiedades del archivo.</span><span class="sxs-lookup"><span data-stu-id="e35c0-286">Check that the property handler does not leak file handles by editing it after getting output from the property handler, or by using a tool like oh.exe before and after enumerating file properties.</span></span>
-   <span data-ttu-id="e35c0-287">Probar todos los tipos de archivo asociados al controlador de propiedades.</span><span class="sxs-lookup"><span data-stu-id="e35c0-287">Test all file types associated with the property handler.</span></span> <span data-ttu-id="e35c0-288">Por ejemplo, compruebe que el filtro HTML funciona con tipos de archivo. htm y. html.</span><span class="sxs-lookup"><span data-stu-id="e35c0-288">For example, check that the HTML filter works with .htm and .html file types.</span></span>
-   <span data-ttu-id="e35c0-289">Pruebe con archivos dañados.</span><span class="sxs-lookup"><span data-stu-id="e35c0-289">Test with corrupted files.</span></span> <span data-ttu-id="e35c0-290">El controlador de propiedad debe producir un error.</span><span class="sxs-lookup"><span data-stu-id="e35c0-290">Property handler should fail gracefully.</span></span>
-   <span data-ttu-id="e35c0-291">Si una aplicación admite el cifrado, compruebe que el controlador de propiedad no genera texto cifrado.</span><span class="sxs-lookup"><span data-stu-id="e35c0-291">If an application supports encryption, test that the property handler does not output encrypted text.</span></span>
-   <span data-ttu-id="e35c0-292">Si el controlador de propiedad admite la búsqueda de texto completo:</span><span class="sxs-lookup"><span data-stu-id="e35c0-292">If your property handler supports full-text search:</span></span>
    -   <span data-ttu-id="e35c0-293">Use varios caracteres Unicode especiales en el contenido del archivo y pruebe su salida.</span><span class="sxs-lookup"><span data-stu-id="e35c0-293">Use multiple special Unicode characters in the file contents and test for their output.</span></span>
    -   <span data-ttu-id="e35c0-294">Pruebe el control de documentos muy grandes para asegurarse de que el controlador de propiedades funciona según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="e35c0-294">Test the handling of very large documents to ensure the property handler works as expected.</span></span>

### <a name="installation-and-setup-tests"></a><span data-ttu-id="e35c0-295">Pruebas de instalación y configuración</span><span class="sxs-lookup"><span data-stu-id="e35c0-295">Installation and Setup Tests</span></span>

<span data-ttu-id="e35c0-296">Por último, debe probar las rutinas de instalación y desinstalación.</span><span class="sxs-lookup"><span data-stu-id="e35c0-296">Lastly, you need to test your install and uninstall routines.</span></span>

-   <span data-ttu-id="e35c0-297">La instalación se debe recuperar de las instalaciones con error (por ejemplo, cancelar y reiniciar el programa de instalación).</span><span class="sxs-lookup"><span data-stu-id="e35c0-297">Installation must recover from failed installations (for example, from canceling and then restarting setup).</span></span>
-   <span data-ttu-id="e35c0-298">La desinstalación debe eliminar todos los archivos asociados con el controlador de propiedades.</span><span class="sxs-lookup"><span data-stu-id="e35c0-298">Uninstall must delete all files associated with the property handler.</span></span>
-   <span data-ttu-id="e35c0-299">La desinstalación no debe eliminar archivos que no sean los asociados a la instalación del controlador de propiedades.</span><span class="sxs-lookup"><span data-stu-id="e35c0-299">Uninstall must not delete files other than the ones associated with the property handler installation.</span></span>
-   <span data-ttu-id="e35c0-300">Se deben quitar las claves del registro asociadas al controlador de propiedades cuando se desinstale.</span><span class="sxs-lookup"><span data-stu-id="e35c0-300">Registry keys associated with the property handler must be removed when uninstalled.</span></span>
-   <span data-ttu-id="e35c0-301">La desinstalación debe funcionar incluso si se eliminan archivos del directorio de instalación.</span><span class="sxs-lookup"><span data-stu-id="e35c0-301">Uninstall must work even if files are deleted from the installation directory.</span></span>

### <a name="troubleshooting-property-handlers"></a><span data-ttu-id="e35c0-302">Solucionar problemas de controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="e35c0-302">Troubleshooting Property Handlers</span></span>

<span data-ttu-id="e35c0-303">A continuación se muestran algunos errores comunes que se realizan al desarrollar controladores de propiedades:</span><span class="sxs-lookup"><span data-stu-id="e35c0-303">The following are some common errors made while developing property handlers:</span></span>

-   <span data-ttu-id="e35c0-304">Instalación de archivos. propDesc o dll en un directorio de usuario.</span><span class="sxs-lookup"><span data-stu-id="e35c0-304">Installing .propdesc files or DLLs under a user directory.</span></span>
-   <span data-ttu-id="e35c0-305">Registrar componentes mediante rutas de acceso relativas.</span><span class="sxs-lookup"><span data-stu-id="e35c0-305">Registering components using relative paths.</span></span>
-   <span data-ttu-id="e35c0-306">Registrando componentes en HKEY \_ Current \_ User en lugar de HKEY \_ local \_ Machine.</span><span class="sxs-lookup"><span data-stu-id="e35c0-306">Registering components under HKEY\_CURRENT\_USER instead of HKEY\_LOCAL\_MACHINE.</span></span>
-   <span data-ttu-id="e35c0-307">Olvidar establecer DisableProcessIsolation para los controladores que no son de secuencia.</span><span class="sxs-lookup"><span data-stu-id="e35c0-307">Forgetting to set DisableProcessIsolation for non-stream handlers.</span></span>
-   <span data-ttu-id="e35c0-308">Colocar el archivo de prueba en una ubicación no indizada.</span><span class="sxs-lookup"><span data-stu-id="e35c0-308">Placing the test file in an unindexed location.</span></span>

<span data-ttu-id="e35c0-309">Si tiene problemas para que el controlador de propiedades funcione con el indexador, aquí tiene algunas sugerencias que le ayudarán a solucionar el problema:</span><span class="sxs-lookup"><span data-stu-id="e35c0-309">If you're having trouble getting your property handler working with the indexer, here are some tips to help you troubleshoot:</span></span>

-   <span data-ttu-id="e35c0-310">Compruebe que las descripciones de propiedad (archivos. propDesc) están marcadas como isColumn = "**true**", isViewable = "**true**" y isQueryable = "**true**", según corresponda.</span><span class="sxs-lookup"><span data-stu-id="e35c0-310">Verify that your property descriptions (.propdesc files) are marked isColumn="**true**", isViewable="**true**", and isQueryable="**true**" as appropriate.</span></span>
-   <span data-ttu-id="e35c0-311">Compruebe que los archivos. propDesc se encuentran en una ubicación global.</span><span class="sxs-lookup"><span data-stu-id="e35c0-311">Verify that your .propdesc files are in a global location.</span></span>
-   <span data-ttu-id="e35c0-312">Compruebe que ha registrado los archivos. propDesc mediante rutas de acceso absolutas.</span><span class="sxs-lookup"><span data-stu-id="e35c0-312">Verify that you registered your .propdesc files using absolute paths.</span></span>
-   <span data-ttu-id="e35c0-313">Compruebe que el registro de eventos no registró ningún error al registrar el archivo. propDesc.</span><span class="sxs-lookup"><span data-stu-id="e35c0-313">Verify that the event log did not record any failures from registering your .propdesc file.</span></span>
-   <span data-ttu-id="e35c0-314">Compruebe que los archivos dll están en una ubicación global (y no en el perfil de usuario).</span><span class="sxs-lookup"><span data-stu-id="e35c0-314">Verify that your DLLs is in a global location (and not under your user profile).</span></span>
-   <span data-ttu-id="e35c0-315">Compruebe que los archivos dll estén registrados en HKEY \_ local \_ Machine \\ software \\ classes.</span><span class="sxs-lookup"><span data-stu-id="e35c0-315">Verify that your DLLs is registered under HKEY\_LOCAL\_MACHINE\\Software\\Classes.</span></span>
-   <span data-ttu-id="e35c0-316">Compruebe que los archivos DLL se registran mediante rutas de acceso completas (o \_ cadenas de expansión \_ SZ que se expanden a rutas de acceso absolutas mediante variables de entorno conocidas por la cuenta del sistema).</span><span class="sxs-lookup"><span data-stu-id="e35c0-316">Verify that your DLLs is registered using full paths (or REG\_EXPAND\_SZ strings that expand to absolute paths using environment variables known by the System account).</span></span>
-   <span data-ttu-id="e35c0-317">Compruebe que el controlador de propiedades funciona en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="e35c0-317">Verify that your property handler works under Windows Explorer.</span></span>
-   <span data-ttu-id="e35c0-318">Aunque se recomienda usar IInitializeWithStream, si debe usar IInitializeWithFile o IInitializeWithItem, compruebe que especifica DisableProcessIsolation.</span><span class="sxs-lookup"><span data-stu-id="e35c0-318">While we recommend using IInitializeWithStream, if you must use IInitializeWithFile or IInitializeWithItem, verify that you specify DisableProcessIsolation.</span></span>
-   <span data-ttu-id="e35c0-319">Compruebe que el panel de control opciones de indización muestra el tipo de archivo como un tipo de archivo indexado.</span><span class="sxs-lookup"><span data-stu-id="e35c0-319">Verify that the Indexing Options Control Panel lists your file type as an indexed file type.</span></span>
-   <span data-ttu-id="e35c0-320">Compruebe que el archivo de prueba se encuentra en una ubicación indizada.</span><span class="sxs-lookup"><span data-stu-id="e35c0-320">Verify that the test file is in an indexed location.</span></span>
-   <span data-ttu-id="e35c0-321">Compruebe que el archivo de prueba se ha modificado desde que instaló el controlador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e35c0-321">Verify that the test file has been modified since you installed your property handler.</span></span>

<span data-ttu-id="e35c0-322">Si el archivo de prueba está en una ubicación indizada y el indexador ya ha rastreado esa ubicación, debe modificar el archivo de alguna manera para desencadenar una reindexación del archivo.</span><span class="sxs-lookup"><span data-stu-id="e35c0-322">If your test file is in an indexed location and the indexer has already crawled that location, you need to modify the file in some way in order to trigger a reindexing of the file.</span></span>

 

## <a name="using-system-supplied-property-handlers"></a><span data-ttu-id="e35c0-323">Usar controladores de propiedades de System-Supplied</span><span class="sxs-lookup"><span data-stu-id="e35c0-323">Using System-Supplied Property Handlers</span></span>

<span data-ttu-id="e35c0-324">Windows incluye varios controladores de propiedades proporcionados por el sistema que puede usar si el formato del tipo de archivo es compatible.</span><span class="sxs-lookup"><span data-stu-id="e35c0-324">Windows includes a number of system-supplied property handlers that you can use if the format of your file type is compatible.</span></span> <span data-ttu-id="e35c0-325">Si define una nueva extensión de archivo que usa uno de estos formatos, puede usar los controladores proporcionados por el sistema registrando el identificador de clase del controlador (CLSID) para la extensión de archivo.</span><span class="sxs-lookup"><span data-stu-id="e35c0-325">If you define a new file extension that uses one of these formats you can use the system-provided handlers by registering the handler class identifier (CLSID) for your file extension.</span></span>

<span data-ttu-id="e35c0-326">Puede usar el CLSID que se muestra en la tabla siguiente para registrar los controladores de propiedades proporcionados por el sistema para el tipo de formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="e35c0-326">You can use the CLSID listed in the following table to register the system-supplied property handlers for your file format type.</span></span>



| <span data-ttu-id="e35c0-327">Formato</span><span class="sxs-lookup"><span data-stu-id="e35c0-327">Format</span></span>          | <span data-ttu-id="e35c0-328">CLSID</span><span class="sxs-lookup"><span data-stu-id="e35c0-328">CLSID</span></span>                                  |
|-----------------|----------------------------------------|
| <span data-ttu-id="e35c0-329">OLE</span><span class="sxs-lookup"><span data-stu-id="e35c0-329">OLE DocFile</span></span>     | <span data-ttu-id="e35c0-330">{8d80504a-0826-40c5-97e1-ebc68f953792}</span><span class="sxs-lookup"><span data-stu-id="e35c0-330">{8d80504a-0826-40c5-97e1-ebc68f953792}</span></span> |
| <span data-ttu-id="e35c0-331">Guardar el XML del juego</span><span class="sxs-lookup"><span data-stu-id="e35c0-331">Save Game XML</span></span>   | <span data-ttu-id="e35c0-332">{ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60}</span><span class="sxs-lookup"><span data-stu-id="e35c0-332">{ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60}</span></span> |
| <span data-ttu-id="e35c0-333">Controlador de XPS/OPC</span><span class="sxs-lookup"><span data-stu-id="e35c0-333">XPS/OPC handler</span></span> | <span data-ttu-id="e35c0-334">{45670FA8-ED97-4F44-BC93-305082590BFB}</span><span class="sxs-lookup"><span data-stu-id="e35c0-334">{45670FA8-ED97-4F44-BC93-305082590BFB}</span></span> |
| <span data-ttu-id="e35c0-335">XML</span><span class="sxs-lookup"><span data-stu-id="e35c0-335">XML</span></span>             | <span data-ttu-id="e35c0-336">{c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9}</span><span class="sxs-lookup"><span data-stu-id="e35c0-336">{c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9}</span></span> |



 

<span data-ttu-id="e35c0-337">Antes de crear una propiedad personalizada, debe asegurarse de que no haya una propiedad definida por el sistema que pueda usar en su lugar.</span><span class="sxs-lookup"><span data-stu-id="e35c0-337">Before creating a custom property, you should be sure there isn't a system-defined property you can use instead.</span></span> <span data-ttu-id="e35c0-338">Puede enumerar las propiedades definidas por el sistema llamando a [**PSEnumeratePropertyDescriptions**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) o mediante la herramienta de línea de comandos prop.exe.</span><span class="sxs-lookup"><span data-stu-id="e35c0-338">You can enumerate the system-defined properties by calling [**PSEnumeratePropertyDescriptions**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) or using the prop.exe command line tool.</span></span>

<span data-ttu-id="e35c0-339">El esquema del sistema define cómo interactúan estas propiedades con el indizador y no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="e35c0-339">The system schema defines how these properties interact with the indexer, and you cannot change that.</span></span> <span data-ttu-id="e35c0-340">Además, la aplicación que se usa para crear, editar y guardar el tipo de archivo también debe ajustarse a cierto comportamiento.</span><span class="sxs-lookup"><span data-stu-id="e35c0-340">Furthermore, the application you use to create, edit and save your file type needs to conform to certain behavior as well.</span></span> <span data-ttu-id="e35c0-341">Por ejemplo, si la aplicación implementa el guardado seguro (en el que se crea un archivo temporal durante la edición y, a continuación, se usa ReplaceFile () para intercambiar la nueva versión del antiguo), debe transferir todas las propiedades del archivo original al nuevo archivo.</span><span class="sxs-lookup"><span data-stu-id="e35c0-341">For example, if the application implements safe save (whereby a temporary file is created during editing, and then ReplaceFile() is used to swap the new version for the old), it must transfer all of the properties from the original file to the new file.</span></span> <span data-ttu-id="e35c0-342">Si no lo hace, el archivo pierde las propiedades agregadas por los usuarios u otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e35c0-342">Failure to do means the file loses properties added by users or other applications.</span></span>

 

<span data-ttu-id="e35c0-343">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="e35c0-343">**Example**</span></span>

<span data-ttu-id="e35c0-344">A continuación se muestra el registro del controlador de archivos OLE de archivo proporcionado por el sistema para un tipo de archivo con un. Extensión OLEDocFile.</span><span class="sxs-lookup"><span data-stu-id="e35c0-344">The following shows the registration of the system-supplied OLE DocFile handler for a file type with a .OLEDocFile extension.</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         shellex
            {BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}
               (Default) = {9DBD2C50-62AD-11d0-B806-00C04FD706EC}
```

<span data-ttu-id="e35c0-345">A continuación se muestra el registro de la información de la lista de propiedades para las propiedades de. Los archivos OLEDocFile se muestran en la pestaña detalles y el panel.</span><span class="sxs-lookup"><span data-stu-id="e35c0-345">The following shows the registration of the property list information so properties of .OLEDocFile files are displayed on the Details tab and pane.</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         ExtendedTileInfo = prop:System.ItemType;System.Size;System.DateModified;System.Author;System.OfflineAvailability
         FullDetails = prop:System.PropGroup.Description;System.Title;System.Subject;
System.Keywords;System.Category;System.Comment;System.PropGroup.Origin;
System.Author;System.Document.LastAuthor;System.Document.RevisionNumber;
System.Document.Version;System.ApplicationName;System.Company;System.Document.Manager;
System.Document.DateCreated;System.Document.DateSaved;System.Document.DatePrinted;
System.Document.TotalEditingTime;System.PropGroup.Content;System.ContentStatus;
System.ContentType;System.Document.PageCount;System.Document.WordCount;
System.Document.CharacterCount;System.Document.LineCount;
System.Document.ParagraphCount;System.Document.Template;System.Document.Scale;
System.Document.LinksDirty;System.Language;System.PropGroup.FileSystem;
System.ItemNameDisplay;System.ItemType;System.ItemFolderPathDisplay;
System.DateCreated;System.DateModified;System.Size;System.FileAttributes;
System.OfflineAvailability;System.OfflineStatus;System.SharedWith;
System.FileOwner;System.ComputerName
         InfoTip = prop:System.ItemType;System.Size;System.DateModified;System.Document.PageCoun
         PerceivedType = document
         PreviewDetails = prop:*System.DateModified;System.Author;System.Keywords;
*System.Size;System.Title;System.Comment;System.Category;
*System.Document.PageCount;System.ContentStatus;System.ContentType;
*System.OfflineAvailability;*System.OfflineStatus;System.Subject;
*System.DateCreated;*System.SharedWith
```

 

## <a name="related-topics"></a><span data-ttu-id="e35c0-346">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e35c0-346">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e35c0-347">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="e35c0-347">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e35c0-348">Asignaciones de propiedades</span><span class="sxs-lookup"><span data-stu-id="e35c0-348">Property Mappings</span></span>](-search-3x-wds-propertymappings.md)
</dt> <dt>

<span data-ttu-id="e35c0-349">**Vista**</span><span class="sxs-lookup"><span data-stu-id="e35c0-349">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e35c0-350">Prácticas recomendadas para crear controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="e35c0-350">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)
</dt> <dt>

[<span data-ttu-id="e35c0-351">Proceso de indización</span><span class="sxs-lookup"><span data-stu-id="e35c0-351">The Indexing Process</span></span>](-search-indexing-process-overview.md)
</dt> <dt>

[<span data-ttu-id="e35c0-352">Desarrollar controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="e35c0-352">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="e35c0-353">Propiedades definidas por el sistema para formatos de archivo personalizados</span><span class="sxs-lookup"><span data-stu-id="e35c0-353">System-Defined Properties for Custom File Formats</span></span>](-shell-systemdefinedpropertiesforfileformats.md)
</dt> <dt>

<span data-ttu-id="e35c0-354">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="e35c0-354">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e35c0-355">Sistema de propiedades</span><span class="sxs-lookup"><span data-stu-id="e35c0-355">Property System</span></span>](../properties/building-property-handlers.md)
</dt> <dt>

<span data-ttu-id="e35c0-356">[Propiedades del sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="e35c0-356">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
</dt> <dt>

[<span data-ttu-id="e35c0-357">Ejemplos del SDK de Windows Search</span><span class="sxs-lookup"><span data-stu-id="e35c0-357">Windows Search SDK Samples</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
</dt> </dl>

 

 
