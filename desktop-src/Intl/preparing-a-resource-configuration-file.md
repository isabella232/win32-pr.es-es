---
description: Preparación de un archivo de configuración de recursos
ms.assetid: 292b57ea-1c7e-49b6-876c-4ad307a2ec43
title: Preparación de un archivo de configuración de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac162ad7f6d20148e0ef60cb9dc15da41cc27186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154150"
---
# <a name="preparing-a-resource-configuration-file"></a><span data-ttu-id="d722b-103">Preparación de un archivo de configuración de recursos</span><span class="sxs-lookup"><span data-stu-id="d722b-103">Preparing a Resource Configuration File</span></span>

<span data-ttu-id="d722b-104">Las utilidades del compilador MUIRCT y RC descritas en [Resource Utilities](resource-utilities.md) proporcionan una opción de línea de comandos que le permite especificar un archivo de configuración de recursos para los recursos de idioma base.</span><span class="sxs-lookup"><span data-stu-id="d722b-104">Both the MUIRCT and the RC Compiler utilities described in [Resource Utilities](resource-utilities.md) provide a command line option that allows you to specify a resource configuration file for the base language resources.</span></span> <span data-ttu-id="d722b-105">El uso de este archivo XML público legible para el usuario permite un mayor control sobre la división de los recursos que se puede obtener mediante los modificadores de línea de comandos normales de las utilidades.</span><span class="sxs-lookup"><span data-stu-id="d722b-105">Use of this public, human-readable XML file allows more control over the splitting of resources than can be obtained using the regular command line switches of the utilities.</span></span> <span data-ttu-id="d722b-106">Sin embargo, incluso si no proporciona un archivo de configuración de recursos como entrada, los archivos de recursos y específicos del idioma contendrán datos de configuración de recursos.</span><span class="sxs-lookup"><span data-stu-id="d722b-106">However, even if you do not provide a resource configuration file as an input, the LN and language-specific resource files will contain resource configuration data.</span></span>

<span data-ttu-id="d722b-107">Todos los archivos de configuración de recursos para aplicaciones Win32 comienzan y finalizan de forma idéntica:</span><span class="sxs-lookup"><span data-stu-id="d722b-107">All resource configuration files for Win32 applications begin and end identically:</span></span>


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>

<resources>
        
        <!-- a single win32Resources element goes here -->

</resources>
</localization>
```



<span data-ttu-id="d722b-108">Este tema se centra en los aspectos del esquema XML que son útiles para compilar código no administrado en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d722b-108">This topic focuses on the aspects of the XML schema that are useful in building unmanaged code on Windows Vista and later.</span></span> <span data-ttu-id="d722b-109">En concreto, solo se ocupa del comportamiento del elemento win32Resources.</span><span class="sxs-lookup"><span data-stu-id="d722b-109">In particular, it is only concerned with the behavior of the win32Resources element.</span></span>

## <a name="win32resources-element"></a><span data-ttu-id="d722b-110">Elemento win32Resources</span><span class="sxs-lookup"><span data-stu-id="d722b-110">win32Resources Element</span></span>

<span data-ttu-id="d722b-111">El elemento win32Resources tiene los atributos que se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d722b-111">The win32Resources element has the attributes described in the following table.</span></span>



| <span data-ttu-id="d722b-112">Nombre del atributo</span><span class="sxs-lookup"><span data-stu-id="d722b-112">Attribute name</span></span>           | <span data-ttu-id="d722b-113">Mandatory</span><span class="sxs-lookup"><span data-stu-id="d722b-113">Mandatory</span></span> | <span data-ttu-id="d722b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d722b-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d722b-115">fileType</span><span class="sxs-lookup"><span data-stu-id="d722b-115">fileType</span></span>                 | <span data-ttu-id="d722b-116">No</span><span class="sxs-lookup"><span data-stu-id="d722b-116">No</span></span>        | <span data-ttu-id="d722b-117">Tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="d722b-117">Type of file.</span></span> <span data-ttu-id="d722b-118">Siempre debe ser "Application".</span><span class="sxs-lookup"><span data-stu-id="d722b-118">Should always be "Application".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="d722b-119">suma de comprobación</span><span class="sxs-lookup"><span data-stu-id="d722b-119">checksum</span></span>                 | <span data-ttu-id="d722b-120">No</span><span class="sxs-lookup"><span data-stu-id="d722b-120">No</span></span>        | <span data-ttu-id="d722b-121">Valor de suma de comprobación que se va a mostrar en los datos de configuración de recursos del archivo LN y de los archivos de recursos específicos del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="d722b-121">Checksum value to appear in the resource configuration data of the LN file and language-specific resource files.</span></span> <span data-ttu-id="d722b-122">Por ejemplo, este atributo le permite copiar la suma de comprobación de un solo archivo de recursos específico del idioma, por Convención la del inglés (Estados Unidos) y colocar la suma de comprobación en un archivo de recursos específico del lenguaje diferente.</span><span class="sxs-lookup"><span data-stu-id="d722b-122">For example, this attribute allows you to copy the checksum from a single language-specific resource file, by convention the one for English (United States), and place the checksum in a different language-specific resource file.</span></span> <span data-ttu-id="d722b-123">La suma de comprobación se puede especificar como una cadena de números hexadecimales que no tenga más de 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d722b-123">The checksum can be specified as a hexadecimal number string that is no longer than 32 characters.</span></span> <span data-ttu-id="d722b-124">El valor numérico se debe poder contener en un número de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="d722b-124">The numerical value must be containable in a 128-bit number.</span></span> |
| <span data-ttu-id="d722b-125">language</span><span class="sxs-lookup"><span data-stu-id="d722b-125">language</span></span>                 | <span data-ttu-id="d722b-126">No</span><span class="sxs-lookup"><span data-stu-id="d722b-126">No</span></span>        | <span data-ttu-id="d722b-127">Idioma especificado con un formato de nombre compatible con RFC 4646 (Windows Vista y versiones posteriores), por ejemplo, en-US para inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="d722b-127">Language specified using a name format compliant with RFC 4646 (Windows Vista and later), for example, en-US for English (United States).</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="d722b-128">ultimateFallbackLanguage</span><span class="sxs-lookup"><span data-stu-id="d722b-128">ultimateFallbackLanguage</span></span> | <span data-ttu-id="d722b-129">No</span><span class="sxs-lookup"><span data-stu-id="d722b-129">No</span></span>        | <span data-ttu-id="d722b-130">Idioma que se va a insertar en los datos de configuración de recursos para el archivo LN, que representa el idioma de reserva final que se va a usar en una búsqueda de un archivo de recursos específico del idioma correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d722b-130">Language to insert into the resource configuration data for the LN file, representing the ultimate fallback language to use in a search for a corresponding language-specific resource file.</span></span> <span data-ttu-id="d722b-131">Si el cargador de recursos no puede cargar un archivo de recursos solicitado de los idiomas de interfaz de usuario preferidos del subproceso, utiliza un lenguaje de reserva final como último intento.</span><span class="sxs-lookup"><span data-stu-id="d722b-131">If the resource loader fails to load a requested resource file from the thread preferred UI languages, it uses an ultimate fallback language as its last attempt.</span></span> <span data-ttu-id="d722b-132">El idioma se especifica con un formato de nombre compatible con RFC 4646 (Windows Vista y versiones posteriores), por ejemplo, en-US para inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="d722b-132">The language is specified using a name format compliant with RFC 4646 (Windows Vista and later), for example, en-US for English (United States).</span></span>       |
| <span data-ttu-id="d722b-133">ultimateFallbackLocation</span><span class="sxs-lookup"><span data-stu-id="d722b-133">ultimateFallbackLocation</span></span> | <span data-ttu-id="d722b-134">No</span><span class="sxs-lookup"><span data-stu-id="d722b-134">No</span></span>        | <span data-ttu-id="d722b-135">Ubicación de reserva.</span><span class="sxs-lookup"><span data-stu-id="d722b-135">Fallback location.</span></span> <span data-ttu-id="d722b-136">Especifique "Internal" si los recursos de reserva finales se compilan en el archivo LN.</span><span class="sxs-lookup"><span data-stu-id="d722b-136">Specify "internal" if ultimate fallback resources are compiled into the LN file.</span></span> <span data-ttu-id="d722b-137">Especifique "external" (valor predeterminado) si el archivo LN va a hacer referencia a un archivo de recursos específico del idioma para sus recursos de reserva finales.</span><span class="sxs-lookup"><span data-stu-id="d722b-137">Specify "external" (default) if the LN file is to reference a language-specific resource file for its ultimate fallback resources.</span></span>                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="d722b-138">En el archivo de configuración de recursos, el elemento win32Resources tiene los subelementos descritos en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d722b-138">In the resource configuration file, the win32Resources element has the sub-elements described in the next table.</span></span>



| <span data-ttu-id="d722b-139">Nombre del elemento</span><span class="sxs-lookup"><span data-stu-id="d722b-139">Element Name</span></span>       | <span data-ttu-id="d722b-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="d722b-140">Description</span></span>                                                                                                                              |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d722b-141">localizedResources</span><span class="sxs-lookup"><span data-stu-id="d722b-141">localizedResources</span></span> | <span data-ttu-id="d722b-142">Recursos que encapsulan información sobre los tipos de recursos y los recursos individuales contenidos en un archivo de recursos específico del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="d722b-142">Resources that encapsulate information about the resource types and individual resources contained in a language-specific resource file.</span></span> |
| <span data-ttu-id="d722b-143">neutralResources</span><span class="sxs-lookup"><span data-stu-id="d722b-143">neutralResources</span></span>   | <span data-ttu-id="d722b-144">Recursos que encapsulan información sobre los tipos de recursos incluidos en un archivo LN.</span><span class="sxs-lookup"><span data-stu-id="d722b-144">Resources that encapsulate information about the resource types contained in an LN file.</span></span>                                                 |



 

## <a name="localizedresources-element"></a><span data-ttu-id="d722b-145">Elemento localizedResources</span><span class="sxs-lookup"><span data-stu-id="d722b-145">localizedResources Element</span></span>

<span data-ttu-id="d722b-146">Elemento Resources adaptado.</span><span class="sxs-lookup"><span data-stu-id="d722b-146">Localized resources element.</span></span> <span data-ttu-id="d722b-147">De forma predeterminada, este elemento no tiene atributos y solo un tipo de subelemento.</span><span class="sxs-lookup"><span data-stu-id="d722b-147">By default, this element has no attributes and only one type of sub-element.</span></span> <span data-ttu-id="d722b-148">Es simplemente un contenedor para los elementos resourceType.</span><span class="sxs-lookup"><span data-stu-id="d722b-148">It is just a container for resourceType elements.</span></span>



| <span data-ttu-id="d722b-149">Nombre del atributo</span><span class="sxs-lookup"><span data-stu-id="d722b-149">Attribute Name</span></span> | <span data-ttu-id="d722b-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="d722b-150">Description</span></span>                                                                    |
|----------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="d722b-151">resourceType</span><span class="sxs-lookup"><span data-stu-id="d722b-151">resourceType</span></span>   | <span data-ttu-id="d722b-152">Tipo de un recurso individual incluido en un archivo de recursos específico del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="d722b-152">Type of an individual resource contained in a language-specific resource file.</span></span> |



 

## <a name="neutralresources-element"></a><span data-ttu-id="d722b-153">Elemento neutralResources</span><span class="sxs-lookup"><span data-stu-id="d722b-153">neutralResources Element</span></span>

<span data-ttu-id="d722b-154">Elemento de recursos neutros.</span><span class="sxs-lookup"><span data-stu-id="d722b-154">Neutral resources element.</span></span> <span data-ttu-id="d722b-155">Este elemento es simplemente un contenedor para los elementos resourceType.</span><span class="sxs-lookup"><span data-stu-id="d722b-155">This element is just a container for resourceType elements.</span></span>



| <span data-ttu-id="d722b-156">Nombre del atributo</span><span class="sxs-lookup"><span data-stu-id="d722b-156">Attribute Name</span></span> | <span data-ttu-id="d722b-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="d722b-157">Description</span></span>                                        |
|----------------|----------------------------------------------------|
| <span data-ttu-id="d722b-158">resourceType</span><span class="sxs-lookup"><span data-stu-id="d722b-158">resourceType</span></span>   | <span data-ttu-id="d722b-159">Tipo de un único recurso incluido en un archivo LN.</span><span class="sxs-lookup"><span data-stu-id="d722b-159">Type of a single resource contained in an LN file.</span></span> |



 

## <a name="resourcetype-element"></a><span data-ttu-id="d722b-160">resourceType (elemento)</span><span class="sxs-lookup"><span data-stu-id="d722b-160">resourceType Element</span></span>

<span data-ttu-id="d722b-161">El elemento resourceType encapsula información sobre un único tipo de recurso o un recurso individual.</span><span class="sxs-lookup"><span data-stu-id="d722b-161">The resourceType element encapsulates information about a single resource type or individual resource.</span></span> <span data-ttu-id="d722b-162">Tiene los atributos que se enumeran a continuación.</span><span class="sxs-lookup"><span data-stu-id="d722b-162">It has the attributes listed below.</span></span>

> [!Caution]  
> <span data-ttu-id="d722b-163">Algunos defectos de configuración de recursos solo los detecta el compilador RC o MUIRCT, según el archivo de recursos de entrada o el contenido del archivo binario.</span><span class="sxs-lookup"><span data-stu-id="d722b-163">Some resource configuration defects are caught only by RC Compiler or MUIRCT, depending on the input resource file or binary file content.</span></span> <span data-ttu-id="d722b-164">No se detectan los errores resourceType del archivo de configuración de recursos que no existen en el archivo de entrada, lo que produce un comportamiento inesperado.</span><span class="sxs-lookup"><span data-stu-id="d722b-164">The resourceType errors in the resource configuration file that do not exist in the input file are not caught, resulting in unexpected behavior.</span></span> <span data-ttu-id="d722b-165">Los usuarios pueden usar un archivo de configuración de recursos defectuoso y no saben hasta que introducen archivos binarios que usan las partes rotas del archivo de configuración de recursos, lo que crea la apariencia de que los saltos provienen de los archivos binarios actuales.</span><span class="sxs-lookup"><span data-stu-id="d722b-165">Users can be using a defective resource configuration file and do not know until they introduce binaries that use the broken parts of the resource configuration file, which creates the appearance that the breaks are from the current binaries.</span></span>

 



| <span data-ttu-id="d722b-166">Nombre del atributo</span><span class="sxs-lookup"><span data-stu-id="d722b-166">Attribute name</span></span> | <span data-ttu-id="d722b-167">Mandatory</span><span class="sxs-lookup"><span data-stu-id="d722b-167">Mandatory</span></span> | <span data-ttu-id="d722b-168">Descripción</span><span class="sxs-lookup"><span data-stu-id="d722b-168">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d722b-169">typeNameId</span><span class="sxs-lookup"><span data-stu-id="d722b-169">typeNameId</span></span>     | <span data-ttu-id="d722b-170">Sí</span><span class="sxs-lookup"><span data-stu-id="d722b-170">Yes</span></span>       | <span data-ttu-id="d722b-171">Nombre del tipo o identificador del recurso.</span><span class="sxs-lookup"><span data-stu-id="d722b-171">Type name or identifier for the resource.</span></span> <span data-ttu-id="d722b-172">Especifique un nombre de cadena o un número.</span><span class="sxs-lookup"><span data-stu-id="d722b-172">Specify a string name or a number.</span></span> <span data-ttu-id="d722b-173">Si usa un número, anteponga a la cadena un " \# " para indicar que representa un número.</span><span class="sxs-lookup"><span data-stu-id="d722b-173">If using a number, prepend the string with a "\#" to indicate that it represents a number.</span></span> <span data-ttu-id="d722b-174">Cada elemento resourceType solo debe tener un atributo *typeNameId* .</span><span class="sxs-lookup"><span data-stu-id="d722b-174">Each resourceType element must have only one *typeNameId* attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d722b-175">itemName</span><span class="sxs-lookup"><span data-stu-id="d722b-175">itemName</span></span>       | <span data-ttu-id="d722b-176">No</span><span class="sxs-lookup"><span data-stu-id="d722b-176">No</span></span>        | <span data-ttu-id="d722b-177">Cadena de nombre de elemento para el recurso que se va a colocar en el archivo de recursos específico del idioma.</span><span class="sxs-lookup"><span data-stu-id="d722b-177">Item name string for the resource, to be placed in the language-specific resource file.</span></span> <span data-ttu-id="d722b-178">Puede especificar varios nombres, separados por espacios en blanco, por ejemplo, "MOFDATA HTML".</span><span class="sxs-lookup"><span data-stu-id="d722b-178">You can specify multiple names, separated by white spaces, for example, "HTML MOFDATA".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="d722b-179">itemId</span><span class="sxs-lookup"><span data-stu-id="d722b-179">itemId</span></span>         | <span data-ttu-id="d722b-180">No</span><span class="sxs-lookup"><span data-stu-id="d722b-180">No</span></span>        | <span data-ttu-id="d722b-181">Identificador del elemento de recurso individual que se va a colocar en el archivo de recursos específico del idioma.</span><span class="sxs-lookup"><span data-stu-id="d722b-181">Identifier of individual resource item, to be placed in the language-specific resource file.</span></span> <span data-ttu-id="d722b-182">El elemento se puede especificar como un intervalo (por ejemplo, "1-12") o por identificadores individuales separados por espacios en blanco (por ejemplo, "1 3 4").</span><span class="sxs-lookup"><span data-stu-id="d722b-182">The item can be specified as a range (for example, "1-12") or by individual identifiers separated by white spaces (for example, "1 3 4").</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="d722b-183">stringId</span><span class="sxs-lookup"><span data-stu-id="d722b-183">stringId</span></span>       | <span data-ttu-id="d722b-184">No</span><span class="sxs-lookup"><span data-stu-id="d722b-184">No</span></span>        | <span data-ttu-id="d722b-185">Identificador de cadena del elemento de recurso individual que se va a colocar en el archivo de recursos específico del idioma.</span><span class="sxs-lookup"><span data-stu-id="d722b-185">String identifier for individual resource item, to be placed in the language-specific resource file.</span></span> <span data-ttu-id="d722b-186">La cadena se puede especificar como un intervalo (por ejemplo, "1-12") o por identificadores individuales separados por espacios en blanco (por ejemplo, "1 3 4"). Este atributo permite la especificación de entradas de la tabla de cadenas localizable y no localizable.</span><span class="sxs-lookup"><span data-stu-id="d722b-186">The string can be specified as a range (for example, "1-12") or by individual identifiers separated by white spaces (for example, "1 3 4").This attribute allows the specification of both localizable and nonlocalizable string table entries.</span></span> <span data-ttu-id="d722b-187">Debe usarse junto con el valor de *typeNameId* de "6", que denota un tipo de recurso de entrada de tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="d722b-187">It must be used in conjunction with the *typeNameId* value of "6", denoting a string table entry resource type.</span></span><br/> <span data-ttu-id="d722b-188">Las cadenas se almacenan en bloques de 16 en una tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="d722b-188">Strings are stored in blocks of 16 in a string table.</span></span> <span data-ttu-id="d722b-189">Por ejemplo, las cadenas 0 a 15 se almacenan en un único bloque de elementos de recursos y se puede hacer referencia a ellas en el archivo de configuración de recursos como *Itemid* 1, o como *stringId* "0-15".</span><span class="sxs-lookup"><span data-stu-id="d722b-189">For example, strings 0 to 15 are stored in a single resource item block and can be referenced in the resource configuration file as *itemId* 1, or as *stringId* "0-15".</span></span> <span data-ttu-id="d722b-190">Por ejemplo, si hay cinco cadenas localizables y tres cadenas no localizables, debe asignar los identificadores de cadena 0-4 para las cadenas localizables y los identificadores de cadena 16-18 para las cadenas no localizables.</span><span class="sxs-lookup"><span data-stu-id="d722b-190">For example, if there are five localizable strings and three nonlocalizable strings, you should assign string identifiers 0-4 for the localizable strings, and string identifiers 16-18 for the nonlocalizable strings.</span></span> <span data-ttu-id="d722b-191">Si no organiza las cadenas de esta manera, los bloques de cadenas afectados se colocan en el archivo LN y en el archivo de recursos específico del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="d722b-191">If you do not organize strings this way, the affected blocks of strings are placed in both the LN file and the language-specific resource file.</span></span><br/> |



 

<span data-ttu-id="d722b-192">Si especifica los atributos *itemname*, *Itemid* y/o *stringId* para un tipo de recurso determinado en el elemento localizedResource, solo se colocan en el archivo de recursos específico del idioma estos elementos o cadenas especificados para el tipo de recurso designado.</span><span class="sxs-lookup"><span data-stu-id="d722b-192">If you specify the *itemName*, *itemId*, and/or *stringId* attributes for a particular resource type under the localizedResource element, only these specified items or strings for the designated resource type are placed in the language-specific resource file.</span></span> <span data-ttu-id="d722b-193">Si se especifica un elemento resourceType sin ningún nombre de elemento explícito, identificador de elemento o identificador de cadena, todos los elementos del tipo de recurso especificado se colocan en el archivo de recursos específico del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="d722b-193">If a resourceType element is specified without any explicit item name, item identifier, or string identifier, all items of the specified resource type are placed in the language-specific resource file.</span></span> <span data-ttu-id="d722b-194">Los elementos o tipos que no se enumeran en ningún elemento localizedResource se colocan en el archivo LN.</span><span class="sxs-lookup"><span data-stu-id="d722b-194">Items or types not listed in any localizedResource element are placed in the LN file.</span></span>

<span data-ttu-id="d722b-195">A continuación se muestran los tipos de recursos estándar y sus identificadores numéricos:</span><span class="sxs-lookup"><span data-stu-id="d722b-195">The following are the standard resource types and their numeric identifiers:</span></span>

-   <span data-ttu-id="d722b-196">CURSOR (1)</span><span class="sxs-lookup"><span data-stu-id="d722b-196">CURSOR(1)</span></span>
-   <span data-ttu-id="d722b-197">MAPA DE BITS (2)</span><span class="sxs-lookup"><span data-stu-id="d722b-197">BITMAP(2)</span></span>
-   <span data-ttu-id="d722b-198">ICONO (3)</span><span class="sxs-lookup"><span data-stu-id="d722b-198">ICON(3)</span></span>
-   <span data-ttu-id="d722b-199">MENÚ (4)</span><span class="sxs-lookup"><span data-stu-id="d722b-199">MENU(4)</span></span>
-   <span data-ttu-id="d722b-200">CUADRO DE DIÁLOGO (5)</span><span class="sxs-lookup"><span data-stu-id="d722b-200">DIALOG(5)</span></span>
-   <span data-ttu-id="d722b-201">CADENA (6)</span><span class="sxs-lookup"><span data-stu-id="d722b-201">STRING(6)</span></span>
-   <span data-ttu-id="d722b-202">FONTDIR (7)</span><span class="sxs-lookup"><span data-stu-id="d722b-202">FONTDIR(7)</span></span>
-   <span data-ttu-id="d722b-203">FUENTE (8)</span><span class="sxs-lookup"><span data-stu-id="d722b-203">FONT(8)</span></span>
-   <span data-ttu-id="d722b-204">ACELERADORES (9)</span><span class="sxs-lookup"><span data-stu-id="d722b-204">ACCELERATORS(9)</span></span>
-   <span data-ttu-id="d722b-205">RCDATA (10)</span><span class="sxs-lookup"><span data-stu-id="d722b-205">RCDATA(10)</span></span>
-   <span data-ttu-id="d722b-206">MESSAGETABLE (11)</span><span class="sxs-lookup"><span data-stu-id="d722b-206">MESSAGETABLE(11)</span></span>
-   <span data-ttu-id="d722b-207">CURSOR de grupo \_ (12)</span><span class="sxs-lookup"><span data-stu-id="d722b-207">GROUP\_CURSOR(12)</span></span>
-   <span data-ttu-id="d722b-208">Icono de grupo \_ (14)</span><span class="sxs-lookup"><span data-stu-id="d722b-208">GROUP\_ICON(14)</span></span>
-   <span data-ttu-id="d722b-209">VERSIÓN (16)</span><span class="sxs-lookup"><span data-stu-id="d722b-209">VERSION(16)</span></span>
-   <span data-ttu-id="d722b-210">HTML (23)</span><span class="sxs-lookup"><span data-stu-id="d722b-210">HTML(23)</span></span>

## <a name="example"></a><span data-ttu-id="d722b-211">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d722b-211">Example</span></span>


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>
  <resources>
    <win32Resources fileType="Application">
      <neutralResources>
        <resourceType
           typeNameId="#16"
        />
      </neutralResources>
      <localizedResources> 
         <resourceType
                typeNameId="#2"
                itemId="5 6 7 8 9 10 11 12"
                itemName="HTML PRI"
         />
         <resourceType
                typeNameId="#4"
         />
         <resourceType
                typeNameId="#5"
         />
         <resourceType
                typeNameId="#6"
         />
         <resourceType
                typeNameId="#9"
         />
         <resourceType
                typeNameId="#11"
         />
         <resourceType
                typeNameId="#16"
         />
         <resourceType
                typeNameId="HTML"
         />
         <resourceType
                typeNameId="#23"
         />
         <resourceType
                typeNameId="#240"
         />
         <resourceType
                typeNameId="#1024"
         />
         <resourceType
                typeNameId="MY_TYPE"
         />
      </localizedResources> 
    </win32Resources>
  </resources>
</localization>
```



## <a name="remarks"></a><span data-ttu-id="d722b-212">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d722b-212">Remarks</span></span>

<span data-ttu-id="d722b-213">Si incluye cualquier tipo de recurso de icono (3), cuadro de diálogo (5), cadena (6) o versión (16) en el elemento neutralResources, tendrá que duplicar esa entrada en el elemento localizedResources.</span><span class="sxs-lookup"><span data-stu-id="d722b-213">If you include any ICON(3), DIALOG(5), STRING(6), or VERSION(16) resource type in the neutralResources element, then you have to duplicate that entry in the localizedResources element.</span></span> <span data-ttu-id="d722b-214">Puede ver esto en el ejemplo anterior, donde el tipo de recurso 16 aparece en las secciones de recursos neutros y localizados.</span><span class="sxs-lookup"><span data-stu-id="d722b-214">You can see this illustrated in the example above, where resource type 16 appears in both neutral and localized resources sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d722b-215">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d722b-215">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d722b-216">Preparación de recursos</span><span class="sxs-lookup"><span data-stu-id="d722b-216">Preparing Resources</span></span>](preparing-resources.md)
</dt> </dl>

 

 




