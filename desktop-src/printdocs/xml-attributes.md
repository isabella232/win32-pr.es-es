---
description: Obtenga información sobre los atributos XML en el marco de esquema de impresión. Este tema no está actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 41bc10fe-6c00-44c5-ba9a-10414b31cbdf
title: Atributos XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d410dcb1476d90568bee10c7c1e41ee7a9bee2e7
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548823"
---
# <a name="xml-attributes"></a><span data-ttu-id="4ed4c-105">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="4ed4c-105">XML Attributes</span></span>

<span data-ttu-id="4ed4c-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-106">This topic is not current.</span></span> <span data-ttu-id="4ed4c-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4ed4c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4ed4c-108">Hay una serie de atributos XML que aparecen en varios tipos de elementos definidos en el marco de esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-108">There are a number of XML attributes that appear in several element types defined in the Print Schema Framework.</span></span> <span data-ttu-id="4ed4c-109">Por lo general, los atributos XML con el mismo nombre tienen el mismo significado y cumplen las mismas reglas, independientemente del tipo de elemento en el que residan.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-109">XML attributes with the same name generally have the same meaning and obey the same rules regardless of the element type they reside in.</span></span> <span data-ttu-id="4ed4c-110">Por lo tanto, los atributos XML se enumeran aquí por nombre y no por su tipo de elemento host.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-110">Therefore, the XML attributes are listed here by name and not by their host element type.</span></span> <span data-ttu-id="4ed4c-111">No se permiten atributos XML definidos de forma privada.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-111">Privately-defined XML attributes are not permitted.</span></span> <span data-ttu-id="4ed4c-112">Solo los atributos XML definidos aquí se pueden usar en un documento PrintCapabilities o printTicket y, a continuación, solo en el contexto definido.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-112">Only the XML attributes defined here may be used in a PrintCapabilities document or a PrintTicket, and then only in the defined context.</span></span>

<span data-ttu-id="4ed4c-113">Aunque no se permite a las partes privadas introducir nuevas definiciones en el espacio de nombres de otra parte, se les permite usar nombres existentes de otro espacio de nombres privado, siempre que su uso sea coherente con el uso establecido por la otra parte.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-113">Although private parties are not permitted to introduce new definitions into another party's namespace, they are permitted utilize existing names from another private namespace as long as its use is consistent with the usage established by the other party.</span></span> <span data-ttu-id="4ed4c-114">Por lo tanto, una opción puede contener elementos ScoredProperty definidos por varias partes diferentes, cada una de las que residen en espacios de nombres diferentes.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-114">Thus an Option may contain ScoredProperty elements defined by several different parties, each residing in different namespaces.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4ed4c-115">Nombre del atributo</span><span class="sxs-lookup"><span data-stu-id="4ed4c-115">Attribute Name</span></span></th>
<th><span data-ttu-id="4ed4c-116">Tipos y valores de datos</span><span class="sxs-lookup"><span data-stu-id="4ed4c-116">Data Types and Values</span></span></th>
<th><span data-ttu-id="4ed4c-117">Propósito</span><span class="sxs-lookup"><span data-stu-id="4ed4c-117">Purpose</span></span></th>
<th><span data-ttu-id="4ed4c-118">Notas</span><span class="sxs-lookup"><span data-stu-id="4ed4c-118">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4ed4c-119">name</span><span class="sxs-lookup"><span data-stu-id="4ed4c-119">name</span></span> <br/></td>
<td><span data-ttu-id="4ed4c-120">XML QName</span><span class="sxs-lookup"><span data-stu-id="4ed4c-120">XML QName</span></span><br/></td>
<td><span data-ttu-id="4ed4c-121">Este atributo XML identifica la instancia del elemento.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-121">This XML attribute identifies the element instance.</span></span> <span data-ttu-id="4ed4c-122">Distingue un elemento de otro del mismo tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-122">It distinguishes one element from another of the same element type.</span></span> <span data-ttu-id="4ed4c-123">Este atributo XML se usa tanto que se conoce como atributo de nombre.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-123">This XML attribute is so widely used it is referred to as the name attribute.</span></span><br/></td>
<td><span data-ttu-id="4ed4c-124">Las restricciones siguientes pertenecen al atributo name.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-124">The following restrictions pertain to the name attribute.</span></span><br/>
<ul>
<li><span data-ttu-id="4ed4c-125">El atributo name debe tener el formato de un QName válido definido por XML.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-125">The name attribute must be in the form of a valid XML-defined QName.</span></span> <span data-ttu-id="4ed4c-126">Es decir, debe estar calificado por un espacio de nombres XML válido.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-126">That is, it must be qualified by a valid XML namespace.</span></span> <span data-ttu-id="4ed4c-127">Los QNames que aparecen como valores de atributos de nombre deben estar calificados explícitamente como espacio de nombres, incluso si se define un espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-127">The QNames appearing as values of name attributes must be explicitly namespace-qualified even if a default namespace is defined.</span></span> <br/></li>
<li><span data-ttu-id="4ed4c-128">El contenido de caracteres debe ser el de un QName válido definido por XML.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-128">Character content must be that of a valid XML-defined QName.</span></span> <br/></li>
<li><span data-ttu-id="4ed4c-129">Los nombres definidos de forma privada deben calificarse con un espacio de nombres que esté asociado de forma única a la entidad que introdujo el atributo name.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-129">Privately-defined names must be qualified with a namespace that is uniquely associated with the party that introduced the name attribute.</span></span><br/></li>
<li><span data-ttu-id="4ed4c-130">Requisito de unidad del mismo nivel: ningún elemento relacionado que pertenezca al mismo tipo de elemento puede tener el mismo atributo de nombre.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-130">Sibling Uniqueness requirement: No two sibling elements belonging to the same element type may have the same name attribute.</span></span> <span data-ttu-id="4ed4c-131">La única excepción son los elementos Option, donde el atributo name se puede usar para definir una opción.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-131">The only exception is Option elements, where the name attribute can be used to define an Option.</span></span> <span data-ttu-id="4ed4c-132">Por lo tanto, los elementos Option de varios elementos del mismo nivel pueden tener el mismo atributo de nombre.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-132">Thus multiple-sibling Option elements may have the same name attribute.</span></span><br/></li>
<li><span data-ttu-id="4ed4c-133">Los siguientes tipos de elemento pueden contener atributos de nombre: Property, ScoredProperty, ParameterDef, Option y Feature.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-133">The following element types may contain name attributes: Property, ScoredProperty, ParameterDef, Option, and Feature.</span></span><br/></li>
<li><span data-ttu-id="4ed4c-134">Los atributos name deben aparecer en cada uno de los tipos de elemento que los contienen, excepto en el caso de algunos elementos de opción de esquema de impresión públicos definidos previamente, como DocumentNUp.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-134">name attributes are required to appear in each of the element types that contain them, except in the case of some previously defined public Print Schema Option elements, such as DocumentNUp.</span></span><br/></li>
</ul>
<span data-ttu-id="4ed4c-135">En el ejemplo siguiente se muestra cómo identificar una instancia de Option mediante un atributo 'name'.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-135">The following example shows how to identify an Option instance using a 'name' attribute.</span></span> <span data-ttu-id="4ed4c-136">Esta es la manera correcta de definir elementos Option.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-136">This is the correct way to define Option elements.</span></span> <span data-ttu-id="4ed4c-137">Un proveedor no debe tener opciones sin nombre, a menos que estén definidas públicamente en el esquema de impresión, como DocumentNUp.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-137">A provider should not have unnamed Options, unless they are publicly defined in the Print Schema, such as DocumentNUp.</span></span><br/>
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
<td><span data-ttu-id="4ed4c-138">Propagar</span><span class="sxs-lookup"><span data-stu-id="4ed4c-138">propagate</span></span> <br/></td>
<td><span data-ttu-id="4ed4c-139">Enumeración</span><span class="sxs-lookup"><span data-stu-id="4ed4c-139">Enumeration</span></span><br/> <span data-ttu-id="4ed4c-140">Actualmente no hay ningún valor definido.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-140">No values are currently defined.</span></span><br/></td>
<td><span data-ttu-id="4ed4c-141">El atributo propagate no se usa en la versión inicial de Print Schema Framework.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-141">The propagate attribute is not used in the initial version of the Print Schema Framework.</span></span> <span data-ttu-id="4ed4c-142">Se documenta aquí para que el código de validación PrintCapabilities o PrintTicket implementado para la versión inicial de Print Schema Framework pueda procesar cualquier versión de esquema posterior sin errores.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-142">It is documented here so that PrintCapabilities or PrintTicket validation code implemented for the initial version of the Print Schema Framework can process any subsequent schema versions without error.</span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="4ed4c-143">Limitada</span><span class="sxs-lookup"><span data-stu-id="4ed4c-143">constrained</span></span> <br/></td>
<td><span data-ttu-id="4ed4c-144">Enumeración</span><span class="sxs-lookup"><span data-stu-id="4ed4c-144">Enumeration</span></span><br/> <span data-ttu-id="4ed4c-145">Valores permitidos:</span><span class="sxs-lookup"><span data-stu-id="4ed4c-145">Allowed values:</span></span><br/>
<ul>
<li><span data-ttu-id="4ed4c-146">None</span><span class="sxs-lookup"><span data-stu-id="4ed4c-146">None</span></span> <br/></li>
<li><span data-ttu-id="4ed4c-147">PrintTicketSettings</span><span class="sxs-lookup"><span data-stu-id="4ed4c-147">PrintTicketSettings</span></span> <br/></li>
<li><span data-ttu-id="4ed4c-148">AdminSettings</span><span class="sxs-lookup"><span data-stu-id="4ed4c-148">AdminSettings</span></span> <br/></li>
<li><span data-ttu-id="4ed4c-149">DeviceSettings</span><span class="sxs-lookup"><span data-stu-id="4ed4c-149">DeviceSettings</span></span> <br/></li>
</ul></td>
<td><span data-ttu-id="4ed4c-150">Indica si la opción está disponible para su selección o para su uso.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-150">Indicates whether the Option is available for selection or for use.</span></span> <br/></td>
<td><span data-ttu-id="4ed4c-151">Los valores permitidos del atributo restringido tienen los significados siguientes.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-151">The allowed values of the constrained attribute have the following meanings.</span></span> <span data-ttu-id="4ed4c-152">Tenga en cuenta que estos valores se enumeran en orden, de menos restrictivo (Ninguno) a más restrictivo (DeviceSettings).</span><span class="sxs-lookup"><span data-stu-id="4ed4c-152">Note that these values are listed in order, from least restrictive (None) to most restrictive (DeviceSettings).</span></span><br/> <span data-ttu-id="4ed4c-153">None</span><span class="sxs-lookup"><span data-stu-id="4ed4c-153">None</span></span> <br/>
<ul>
<li><span data-ttu-id="4ed4c-154">La opción no está restringida.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-154">The Option is not constrained.</span></span> <br/></li>
</ul>
<span data-ttu-id="4ed4c-155">PrintTicketSettings</span><span class="sxs-lookup"><span data-stu-id="4ed4c-155">PrintTicketSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="4ed4c-156">La opción está restringida por la configuración de PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-156">The Option is constrained by the PrintTicket settings.</span></span> <span data-ttu-id="4ed4c-157">Esto implica que cambiar la configuración puede quitar la restricción.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-157">This implies that changing the configuration can remove the constraint.</span></span> <br/></li>
</ul>
<span data-ttu-id="4ed4c-158">AdminSettings</span><span class="sxs-lookup"><span data-stu-id="4ed4c-158">AdminSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="4ed4c-159">La opción está restringida por la configuración del administrador; El usuario no puede habilitar la opción .</span><span class="sxs-lookup"><span data-stu-id="4ed4c-159">The Option is constrained by the administrator's settings; the Option cannot be enabled by the user.</span></span><br/></li>
</ul>
<span data-ttu-id="4ed4c-160">DeviceSettings</span><span class="sxs-lookup"><span data-stu-id="4ed4c-160">DeviceSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="4ed4c-161">La opción está restringida por la configuración del dispositivo o las opciones de dispositivo instaladas físicamente; El usuario o el administrador no pueden habilitar la opción.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-161">The Option is constrained by the device settings or the physically installed device options; the Option cannot be enabled by either the user or the administrator.</span></span><br/></li>
</ul>
<span data-ttu-id="4ed4c-162">Cuando el proveedor PrintCapabilities notifica los valores del atributo restringido, se debe informar de la restricción más restrictiva encontrada.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-162">When the PrintCapabilities provider reports values of the constrained attribute, the most restrictive constraint found should be reported.</span></span> <span data-ttu-id="4ed4c-163">Por ejemplo, si una opción está restringida por una configuración de administrador y una configuración de dispositivo, el proveedor PrintCapabilities debe notificar DeviceSettings.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-163">For example, if an Option is constrained by both an administrator setting and a device setting, the PrintCapabilities provider should report DeviceSettings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ed4c-164">xmlns</span><span class="sxs-lookup"><span data-stu-id="4ed4c-164">xmlns</span></span> <br/></td>
<td><span data-ttu-id="4ed4c-165">Identificador URI</span><span class="sxs-lookup"><span data-stu-id="4ed4c-165">URI</span></span><br/></td>
<td><span data-ttu-id="4ed4c-166">Este atributo XML establece un vínculo entre un identificador uniforme de recursos (URI) de espacio de nombres y el prefijo de espacio de nombres que aparece en el QName XML.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-166">This XML attribute establishes a link between a namespace uniform resource identifier (URI) and the namespace prefix that appears in the XML QName.</span></span> <span data-ttu-id="4ed4c-167">Debe establecer este vínculo al URI del espacio de nombres definido para el marco de esquema de impresión antes de poder usar cualquiera de las etiquetas de elementos definidos por el marco, atributos, atributos de nombre, entre otras.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-167">You must establish such a link to the namespace URI defined for the Print Schema Framework before you can use any of the Framework-defined element tags, Attributes, name attributes, and so on.</span></span> <span data-ttu-id="4ed4c-168">Puede declarar que este espacio de nombres es el valor predeterminado para evitar calificar realmente las etiquetas de elemento con un prefijo de espacio de nombres, aunque todos los demás QName deben calificarse explícitamente.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-168">You may declare this namespace to be the default to avoid actually qualifying the element tags with a namespace prefix, although all other QNames must be explicitly qualified.</span></span> <span data-ttu-id="4ed4c-169">El espacio de nombres estándar debe definirse en el elemento raíz adecuado.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-169">The standard namespace must be defined in the appropriate root element.</span></span> <span data-ttu-id="4ed4c-170">Observe todas las reglas y convenciones XML con respecto al uso del atributo xmlns.</span><span class="sxs-lookup"><span data-stu-id="4ed4c-170">Observe all XML rules and conventions regarding use of the xmlns attribute.</span></span><br/> <span data-ttu-id="4ed4c-171">El URI de Print Schema Framework es http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework .</span><span class="sxs-lookup"><span data-stu-id="4ed4c-171">The URI for the Print Schema Framework is http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework.</span></span><br/> <span data-ttu-id="4ed4c-172">El URI de las palabras clave de esquema de impresión es https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords .</span><span class="sxs-lookup"><span data-stu-id="4ed4c-172">The URI for the Print Schema Keywords is https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords.</span></span><br/></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="4ed4c-173">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4ed4c-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ed4c-174">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="4ed4c-174">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




