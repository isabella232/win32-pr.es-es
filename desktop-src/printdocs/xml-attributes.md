---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 41bc10fe-6c00-44c5-ba9a-10414b31cbdf
title: Atributos XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70dd05effe6f3ea79afd0972867cb2734ace1a71
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105689710"
---
# <a name="xml-attributes"></a><span data-ttu-id="215a6-104">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="215a6-104">XML Attributes</span></span>

<span data-ttu-id="215a6-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="215a6-105">This topic is not current.</span></span> <span data-ttu-id="215a6-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="215a6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="215a6-107">Hay una serie de atributos XML que aparecen en varios tipos de elemento definidos en el marco de trabajo del esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="215a6-107">There are a number of XML attributes that appear in several element types defined in the Print Schema Framework.</span></span> <span data-ttu-id="215a6-108">Los atributos XML con el mismo nombre generalmente tienen el mismo significado y obedecen a las mismas reglas independientemente del tipo de elemento en el que residen.</span><span class="sxs-lookup"><span data-stu-id="215a6-108">XML attributes with the same name generally have the same meaning and obey the same rules regardless of the element type they reside in.</span></span> <span data-ttu-id="215a6-109">Por lo tanto, los atributos XML se enumeran aquí por nombre y no por su tipo de elemento host.</span><span class="sxs-lookup"><span data-stu-id="215a6-109">Therefore, the XML attributes are listed here by name and not by their host element type.</span></span> <span data-ttu-id="215a6-110">No se permiten atributos XML definidos de forma privada.</span><span class="sxs-lookup"><span data-stu-id="215a6-110">Privately-defined XML attributes are not permitted.</span></span> <span data-ttu-id="215a6-111">Solo los atributos XML definidos aquí se pueden usar en un documento de PrintCapabilities o en un PrintTicket y solo en el contexto definido.</span><span class="sxs-lookup"><span data-stu-id="215a6-111">Only the XML attributes defined here may be used in a PrintCapabilities document or a PrintTicket, and then only in the defined context.</span></span>

<span data-ttu-id="215a6-112">Aunque los usuarios privados no pueden introducir nuevas definiciones en el espacio de nombres de otra entidad, se les permite usar los nombres existentes de otro espacio de nombres privado, siempre que su uso sea coherente con el uso establecido por la otra parte.</span><span class="sxs-lookup"><span data-stu-id="215a6-112">Although private parties are not permitted to introduce new definitions into another party's namespace, they are permitted utilize existing names from another private namespace as long as its use is consistent with the usage established by the other party.</span></span> <span data-ttu-id="215a6-113">Por lo tanto, una opción puede contener elementos ScoredProperty definidos por varias partes diferentes, cada uno de los cuales reside en diferentes espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="215a6-113">Thus an Option may contain ScoredProperty elements defined by several different parties, each residing in different namespaces.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="215a6-114">Nombre del atributo</span><span class="sxs-lookup"><span data-stu-id="215a6-114">Attribute Name</span></span></th>
<th><span data-ttu-id="215a6-115">Tipos de datos y valores</span><span class="sxs-lookup"><span data-stu-id="215a6-115">Data Types and Values</span></span></th>
<th><span data-ttu-id="215a6-116">Propósito</span><span class="sxs-lookup"><span data-stu-id="215a6-116">Purpose</span></span></th>
<th><span data-ttu-id="215a6-117">Notas</span><span class="sxs-lookup"><span data-stu-id="215a6-117">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="215a6-118">name</span><span class="sxs-lookup"><span data-stu-id="215a6-118">name</span></span> <br/></td>
<td><span data-ttu-id="215a6-119">QName XML</span><span class="sxs-lookup"><span data-stu-id="215a6-119">XML QName</span></span><br/></td>
<td><span data-ttu-id="215a6-120">Este atributo XML identifica la instancia del elemento.</span><span class="sxs-lookup"><span data-stu-id="215a6-120">This XML attribute identifies the element instance.</span></span> <span data-ttu-id="215a6-121">Distingue un elemento de otro del mismo tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="215a6-121">It distinguishes one element from another of the same element type.</span></span> <span data-ttu-id="215a6-122">Este atributo XML es tan ampliamente utilizado y se conoce como atributo de nombre.</span><span class="sxs-lookup"><span data-stu-id="215a6-122">This XML attribute is so widely used it is referred to as the name attribute.</span></span><br/></td>
<td><span data-ttu-id="215a6-123">Las siguientes restricciones se aplican al atributo name.</span><span class="sxs-lookup"><span data-stu-id="215a6-123">The following restrictions pertain to the name attribute.</span></span><br/>
<ul>
<li><span data-ttu-id="215a6-124">El atributo name debe tener el formato de un QName válido definido por XML.</span><span class="sxs-lookup"><span data-stu-id="215a6-124">The name attribute must be in the form of a valid XML-defined QName.</span></span> <span data-ttu-id="215a6-125">Es decir, debe estar calificado por un espacio de nombres XML válido.</span><span class="sxs-lookup"><span data-stu-id="215a6-125">That is, it must be qualified by a valid XML namespace.</span></span> <span data-ttu-id="215a6-126">Los QNames que aparecen como valores de los atributos name deben ser explícitamente calificados con el espacio de nombres aunque se haya definido un espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="215a6-126">The QNames appearing as values of name attributes must be explicitly namespace-qualified even if a default namespace is defined.</span></span> <br/></li>
<li><span data-ttu-id="215a6-127">El contenido del carácter debe ser el de un QName válido definido por XML.</span><span class="sxs-lookup"><span data-stu-id="215a6-127">Character content must be that of a valid XML-defined QName.</span></span> <br/></li>
<li><span data-ttu-id="215a6-128">Los nombres definidos de forma privada se deben calificar con un espacio de nombres que esté asociado de manera única a la entidad que presentó el atributo de nombre.</span><span class="sxs-lookup"><span data-stu-id="215a6-128">Privately-defined names must be qualified with a namespace that is uniquely associated with the party that introduced the name attribute.</span></span><br/></li>
<li><span data-ttu-id="215a6-129">Requisito de unicidad relacionado: no dos elementos del mismo nivel que pertenezcan al mismo tipo de elemento pueden tener el mismo atributo de nombre.</span><span class="sxs-lookup"><span data-stu-id="215a6-129">Sibling Uniqueness requirement: No two sibling elements belonging to the same element type may have the same name attribute.</span></span> <span data-ttu-id="215a6-130">La única excepción son los elementos Option, donde el atributo name se puede usar para definir una opción.</span><span class="sxs-lookup"><span data-stu-id="215a6-130">The only exception is Option elements, where the name attribute can be used to define an Option.</span></span> <span data-ttu-id="215a6-131">Por lo tanto, los elementos de opción de varios nodos pueden tener el mismo atributo de nombre.</span><span class="sxs-lookup"><span data-stu-id="215a6-131">Thus multiple-sibling Option elements may have the same name attribute.</span></span><br/></li>
<li><span data-ttu-id="215a6-132">Los siguientes tipos de elemento pueden contener atributos de nombre: Property, ScoredProperty, ParameterDef, Option y Feature.</span><span class="sxs-lookup"><span data-stu-id="215a6-132">The following element types may contain name attributes: Property, ScoredProperty, ParameterDef, Option, and Feature.</span></span><br/></li>
<li><span data-ttu-id="215a6-133">los atributos name deben aparecer en cada uno de los tipos de elemento que los contengan, excepto en el caso de algunos elementos de opción de esquema de impresión pública definidos anteriormente, como DocumentNUp.</span><span class="sxs-lookup"><span data-stu-id="215a6-133">name attributes are required to appear in each of the element types that contain them, except in the case of some previously defined public Print Schema Option elements, such as DocumentNUp.</span></span><br/></li>
</ul>
<span data-ttu-id="215a6-134">En el ejemplo siguiente se muestra cómo identificar una instancia de opción mediante un atributo ' name '.</span><span class="sxs-lookup"><span data-stu-id="215a6-134">The following example shows how to identify an Option instance using a 'name' attribute.</span></span> <span data-ttu-id="215a6-135">Esta es la manera correcta de definir elementos Option.</span><span class="sxs-lookup"><span data-stu-id="215a6-135">This is the correct way to define Option elements.</span></span> <span data-ttu-id="215a6-136">Un proveedor no debe tener opciones sin nombre, a menos que estén definidas públicamente en el esquema de impresión, como DocumentNUp.</span><span class="sxs-lookup"><span data-stu-id="215a6-136">A provider should not have unnamed Options, unless they are publicly defined in the Print Schema, such as DocumentNUp.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>  <psf:Option name=&quot;psk:StapleBottomRight&quot;>
    <psf:ScoredProperty name=&quot;psk:Angle&quot;>
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name=&quot;psk:SheetCapacity&quot; >
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option></code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="215a6-137">propagar</span><span class="sxs-lookup"><span data-stu-id="215a6-137">propagate</span></span> <br/></td>
<td><span data-ttu-id="215a6-138">Enumeración</span><span class="sxs-lookup"><span data-stu-id="215a6-138">Enumeration</span></span><br/> <span data-ttu-id="215a6-139">No hay ningún valor definido actualmente.</span><span class="sxs-lookup"><span data-stu-id="215a6-139">No values are currently defined.</span></span><br/></td>
<td><span data-ttu-id="215a6-140">El atributo Propagate no se utiliza en la versión inicial del marco de trabajo del esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="215a6-140">The propagate attribute is not used in the initial version of the Print Schema Framework.</span></span> <span data-ttu-id="215a6-141">Se documenta aquí para que el código de validación de PrintCapabilities o PrintTicket implementado para la versión inicial del marco de trabajo del esquema de impresión pueda procesar cualquier versión de esquema posterior sin errores.</span><span class="sxs-lookup"><span data-stu-id="215a6-141">It is documented here so that PrintCapabilities or PrintTicket validation code implemented for the initial version of the Print Schema Framework can process any subsequent schema versions without error.</span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="215a6-142">restringida</span><span class="sxs-lookup"><span data-stu-id="215a6-142">constrained</span></span> <br/></td>
<td><span data-ttu-id="215a6-143">Enumeración</span><span class="sxs-lookup"><span data-stu-id="215a6-143">Enumeration</span></span><br/> <span data-ttu-id="215a6-144">Valores permitidos:</span><span class="sxs-lookup"><span data-stu-id="215a6-144">Allowed values:</span></span><br/>
<ul>
<li><span data-ttu-id="215a6-145">None</span><span class="sxs-lookup"><span data-stu-id="215a6-145">None</span></span> <br/></li>
<li><span data-ttu-id="215a6-146">PrintTicketSettings</span><span class="sxs-lookup"><span data-stu-id="215a6-146">PrintTicketSettings</span></span> <br/></li>
<li><span data-ttu-id="215a6-147">AdminSettings</span><span class="sxs-lookup"><span data-stu-id="215a6-147">AdminSettings</span></span> <br/></li>
<li><span data-ttu-id="215a6-148">DeviceSettings</span><span class="sxs-lookup"><span data-stu-id="215a6-148">DeviceSettings</span></span> <br/></li>
</ul></td>
<td><span data-ttu-id="215a6-149">Indica si la opción está disponible para la selección o para su uso.</span><span class="sxs-lookup"><span data-stu-id="215a6-149">Indicates whether the Option is available for selection or for use.</span></span> <br/></td>
<td><span data-ttu-id="215a6-150">Los valores permitidos del atributo Constrained tienen los significados siguientes.</span><span class="sxs-lookup"><span data-stu-id="215a6-150">The allowed values of the constrained attribute have the following meanings.</span></span> <span data-ttu-id="215a6-151">Tenga en cuenta que estos valores se muestran en orden, de menos restrictivo (ninguno) a más restrictiva (DeviceSettings).</span><span class="sxs-lookup"><span data-stu-id="215a6-151">Note that these values are listed in order, from least restrictive (None) to most restrictive (DeviceSettings).</span></span><br/> <span data-ttu-id="215a6-152">None</span><span class="sxs-lookup"><span data-stu-id="215a6-152">None</span></span> <br/>
<ul>
<li><span data-ttu-id="215a6-153">La opción no está restringida.</span><span class="sxs-lookup"><span data-stu-id="215a6-153">The Option is not constrained.</span></span> <br/></li>
</ul>
<span data-ttu-id="215a6-154">PrintTicketSettings</span><span class="sxs-lookup"><span data-stu-id="215a6-154">PrintTicketSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="215a6-155">La opción está restringida por la configuración de PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="215a6-155">The Option is constrained by the PrintTicket settings.</span></span> <span data-ttu-id="215a6-156">Esto implica que el cambio de la configuración puede quitar la restricción.</span><span class="sxs-lookup"><span data-stu-id="215a6-156">This implies that changing the configuration can remove the constraint.</span></span> <br/></li>
</ul>
<span data-ttu-id="215a6-157">AdminSettings</span><span class="sxs-lookup"><span data-stu-id="215a6-157">AdminSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="215a6-158">La opción está restringida por la configuración del administrador; el usuario no puede habilitar la opción.</span><span class="sxs-lookup"><span data-stu-id="215a6-158">The Option is constrained by the administrator's settings; the Option cannot be enabled by the user.</span></span><br/></li>
</ul>
<span data-ttu-id="215a6-159">DeviceSettings</span><span class="sxs-lookup"><span data-stu-id="215a6-159">DeviceSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="215a6-160">La opción está restringida por la configuración del dispositivo o las opciones del dispositivo instalado físicamente. el usuario o el administrador no pueden habilitar la opción.</span><span class="sxs-lookup"><span data-stu-id="215a6-160">The Option is constrained by the device settings or the physically installed device options; the Option cannot be enabled by either the user or the administrator.</span></span><br/></li>
</ul>
<span data-ttu-id="215a6-161">Cuando el proveedor de PrintCapabilities informa de los valores del atributo restringido, se debe notificar la restricción más restrictiva encontrada.</span><span class="sxs-lookup"><span data-stu-id="215a6-161">When the PrintCapabilities provider reports values of the constrained attribute, the most restrictive constraint found should be reported.</span></span> <span data-ttu-id="215a6-162">Por ejemplo, si una opción está restringida por una configuración de administrador y una configuración de dispositivo, el proveedor de PrintCapabilities debe notificar a DeviceSettings.</span><span class="sxs-lookup"><span data-stu-id="215a6-162">For example, if an Option is constrained by both an administrator setting and a device setting, the PrintCapabilities provider should report DeviceSettings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="215a6-163">xmlns</span><span class="sxs-lookup"><span data-stu-id="215a6-163">xmlns</span></span> <br/></td>
<td><span data-ttu-id="215a6-164">URI</span><span class="sxs-lookup"><span data-stu-id="215a6-164">URI</span></span><br/></td>
<td><span data-ttu-id="215a6-165">Este atributo XML establece un vínculo entre un identificador uniforme de recursos (URI) de espacio de nombres y el prefijo de espacio de nombres que aparece en el QName XML.</span><span class="sxs-lookup"><span data-stu-id="215a6-165">This XML attribute establishes a link between a namespace uniform resource identifier (URI) and the namespace prefix that appears in the XML QName.</span></span> <span data-ttu-id="215a6-166">Debe establecer este tipo de vínculo con el identificador URI de espacio de nombres definido para el marco de trabajo del esquema de impresión antes de poder usar cualquiera de las etiquetas de elementos definidas por el marco, atributos, atributos de nombre, etc.</span><span class="sxs-lookup"><span data-stu-id="215a6-166">You must establish such a link to the namespace URI defined for the Print Schema Framework before you can use any of the Framework-defined element tags, Attributes, name attributes, and so on.</span></span> <span data-ttu-id="215a6-167">Puede declarar este espacio de nombres para que sea el valor predeterminado para evitar que las etiquetas de elementos se califiquen realmente con un prefijo de espacio de nombres, aunque todos los demás QNames deben estar explícitamente calificados.</span><span class="sxs-lookup"><span data-stu-id="215a6-167">You may declare this namespace to be the default to avoid actually qualifying the element tags with a namespace prefix, although all other QNames must be explicitly qualified.</span></span> <span data-ttu-id="215a6-168">El espacio de nombres estándar debe definirse en el elemento raíz adecuado.</span><span class="sxs-lookup"><span data-stu-id="215a6-168">The standard namespace must be defined in the appropriate root element.</span></span> <span data-ttu-id="215a6-169">Observe todas las reglas y convenciones XML con respecto al uso del atributo xmlns.</span><span class="sxs-lookup"><span data-stu-id="215a6-169">Observe all XML rules and conventions regarding use of the xmlns attribute.</span></span><br/> <span data-ttu-id="215a6-170">El URI para el marco de trabajo del esquema de impresión es http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework .</span><span class="sxs-lookup"><span data-stu-id="215a6-170">The URI for the Print Schema Framework is http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework.</span></span><br/> <span data-ttu-id="215a6-171">El URI de las palabras clave del esquema de impresión es https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords .</span><span class="sxs-lookup"><span data-stu-id="215a6-171">The URI for the Print Schema Keywords is https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords.</span></span><br/></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="215a6-172">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="215a6-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="215a6-173">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="215a6-173">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




