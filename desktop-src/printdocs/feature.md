---
description: Revise elementos Feature, que contienen una lista de elementos Option y Property que describen un atributo de dispositivo, una configuración de formato de trabajo u otra característica relevante.
ms.assetid: 5a6553c2-f322-47e2-bbc8-44f6541f1288
title: Característica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28ab7e8cc69ecc9ba3956fbae3c5278baace8cf
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120640"
---
# <a name="feature"></a><span data-ttu-id="56da4-103">Característica</span><span class="sxs-lookup"><span data-stu-id="56da4-103">Feature</span></span>

<span data-ttu-id="56da4-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="56da4-104">This topic is not current.</span></span> <span data-ttu-id="56da4-105">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="56da4-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="56da4-106">Un elemento Feature contiene una lista completa de los elementos Option y Property que describen completamente un atributo de dispositivo, una configuración de formato de trabajo u otra característica relevante.</span><span class="sxs-lookup"><span data-stu-id="56da4-106">A Feature element contains a complete list of the Option and Property elements that fully describe a device attribute, job formatting setting, or other relevant characteristic.</span></span>

## <a name="element-tag"></a><span data-ttu-id="56da4-107">Etiqueta de elemento</span><span class="sxs-lookup"><span data-stu-id="56da4-107">Element Tag</span></span>

<Feature>

## <a name="xml-attributes"></a><span data-ttu-id="56da4-108">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="56da4-108">XML Attributes</span></span>

<span data-ttu-id="56da4-109">En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.</span><span class="sxs-lookup"><span data-stu-id="56da4-109">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="56da4-110">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="56da4-110">XML Attribute</span></span>   | <span data-ttu-id="56da4-111">Detalles</span><span class="sxs-lookup"><span data-stu-id="56da4-111">Details</span></span>                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56da4-112">name</span><span class="sxs-lookup"><span data-stu-id="56da4-112">name</span></span><br/> | <span data-ttu-id="56da4-113">Contiene el nombre de la característica, ya sea una característica estándar o una característica definida de forma privada.</span><span class="sxs-lookup"><span data-stu-id="56da4-113">Holds the name of the Feature, either a standard Feature or a privately-defined Feature.</span></span> <br/> |



 

<span data-ttu-id="56da4-114">Para obtener más información, vea la [sección Atributos XML.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="56da4-114">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="56da4-115">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="56da4-115">Element Information</span></span>

<span data-ttu-id="56da4-116">En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.</span><span class="sxs-lookup"><span data-stu-id="56da4-116">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="56da4-117">Category</span><span class="sxs-lookup"><span data-stu-id="56da4-117">Category</span></span></th>
<th><span data-ttu-id="56da4-118">Detalles</span><span class="sxs-lookup"><span data-stu-id="56da4-118">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="56da4-119">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="56da4-119">Parent elements</span></span><br/></td>
<td><span data-ttu-id="56da4-120">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="56da4-120">PrintCapabilities</span></span> <br/> <span data-ttu-id="56da4-121">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="56da4-121">PrintTicket</span></span> <br/> <span data-ttu-id="56da4-122">Característica</span><span class="sxs-lookup"><span data-stu-id="56da4-122">Feature</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56da4-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="56da4-123">Child elements</span></span><br/></td>
<td><span data-ttu-id="56da4-124">Uno de los grupos siguientes:</span><span class="sxs-lookup"><span data-stu-id="56da4-124">One of the following groups:</span></span><br/>
<ul>
<li><span data-ttu-id="56da4-125"><em>Característica</em> (cero o más)</span><span class="sxs-lookup"><span data-stu-id="56da4-125"><em>Feature</em> (zero or more)</span></span><br/></li>
<li><span data-ttu-id="56da4-126"><em>Opción</em> (uno o varios)</span><span class="sxs-lookup"><span data-stu-id="56da4-126"><em>Option</em> (one or more)</span></span><br/></li>
<li><span data-ttu-id="56da4-127"><em>Propiedad</em> (cero o más)</span><span class="sxs-lookup"><span data-stu-id="56da4-127"><em>Property</em> (zero or more)</span></span><br/></li>
</ul>
<span data-ttu-id="56da4-128">or</span><span class="sxs-lookup"><span data-stu-id="56da4-128">or</span></span> <br/>
<ul>
<li><span data-ttu-id="56da4-129"><em>Característica</em> (uno o varios)</span><span class="sxs-lookup"><span data-stu-id="56da4-129"><em>Feature</em> (one or more)</span></span><br/></li>
<li><span data-ttu-id="56da4-130"><em>Opción</em> (cero o más)</span><span class="sxs-lookup"><span data-stu-id="56da4-130"><em>Option</em> (zero or more)</span></span><br/></li>
<li><span data-ttu-id="56da4-131"><em>Propiedad</em> (cero o más)</span><span class="sxs-lookup"><span data-stu-id="56da4-131"><em>Property</em> (zero or more)</span></span><br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56da4-132">Este elemento</span><span class="sxs-lookup"><span data-stu-id="56da4-132">This element</span></span><br/></td>
<td><span data-ttu-id="56da4-133">No se permiten datos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="56da4-133">No character data is permitted.</span></span><br/> <span data-ttu-id="56da4-134">Se permiten elementos secundarios duplicados option que son elementos del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="56da4-134">Duplicate child Option elements that are siblings are permitted.</span></span> <span data-ttu-id="56da4-135">Se permiten accesos directos de atributo de nombre duplicado.</span><span class="sxs-lookup"><span data-stu-id="56da4-135">Duplicate name attribute shortcuts permitted.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="configuration-dependencies"></a><span data-ttu-id="56da4-136">Dependencias de configuración</span><span class="sxs-lookup"><span data-stu-id="56da4-136">Configuration Dependencies</span></span>

<span data-ttu-id="56da4-137">Es posible que los elementos de características no tengan dependencias de configuración.</span><span class="sxs-lookup"><span data-stu-id="56da4-137">Feature elements may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="56da4-138">Uso de elementos</span><span class="sxs-lookup"><span data-stu-id="56da4-138">Element Usage</span></span>

### <a name="relationship-to-xml-attributes"></a><span data-ttu-id="56da4-139">Relación con atributos XML</span><span class="sxs-lookup"><span data-stu-id="56da4-139">Relationship to XML Attributes</span></span>

<span data-ttu-id="56da4-140">En la representación característica/opción, un atributo de dispositivo se representa mediante un elemento Feature.</span><span class="sxs-lookup"><span data-stu-id="56da4-140">In Feature/Option representation, a device attribute is represented by a Feature element.</span></span> <span data-ttu-id="56da4-141">El atributo device se identifica de forma única mediante el atributo name en el elemento Feature del atributo de dispositivo, como en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="56da4-141">The device attribute is uniquely identified by the name attribute in the device attribute's Feature element, as in the following example.</span></span> <span data-ttu-id="56da4-142">En este ejemplo, el atributo de dispositivo es Resolución.</span><span class="sxs-lookup"><span data-stu-id="56da4-142">In this example, the device attribute is Resolution.</span></span>

``` syntax
<Feature name="Resolution" />
```

<span data-ttu-id="56da4-143">El esquema de impresión define un conjunto de atributos de nombre para determinadas instancias de característica.</span><span class="sxs-lookup"><span data-stu-id="56da4-143">The Print Schema defines a set of name attributes for certain Feature instances.</span></span> <span data-ttu-id="56da4-144">Estos atributos de nombre sirven para identificar un conjunto de instancias de características predefinidas asociadas a atributos de dispositivo configurables específicos.</span><span class="sxs-lookup"><span data-stu-id="56da4-144">These name attributes serve to identify a set of predefined Feature instances associated with specific configurable device attributes.</span></span> <span data-ttu-id="56da4-145">Estos nombres de instancia de características se deben usar siempre que corresponda, ya que aumentan la portabilidad del documento PrintCapabilities y los PrintTickets que se derivan de ellos.</span><span class="sxs-lookup"><span data-stu-id="56da4-145">These Feature instance names should be used whenever applicable, because they increase the portability of your PrintCapabilities document and the PrintTickets that are derived from them.</span></span> <span data-ttu-id="56da4-146">Las instancias de características definidas de forma privada pueden introducirse si determinados atributos de dispositivo no se corresponden con ninguna de las instancias de características definidas por el esquema.</span><span class="sxs-lookup"><span data-stu-id="56da4-146">Privately-defined Feature instances may be introduced if certain device attributes do not correspond to any of the schema-defined Feature instances.</span></span> <span data-ttu-id="56da4-147">Para obtener información sobre la sintaxis de los atributos de nombre y las convenciones que se aplican a los nombres definidos por el esquema y definidos de forma privada, vea [Atributos XML](xml-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="56da4-147">For information about the syntax for name attributes and the conventions that apply to schema-defined and privately-defined names, see [XML Attributes](xml-attributes.md).</span></span>

### <a name="relationship-to-option-element"></a><span data-ttu-id="56da4-148">Elemento Relationship to Option</span><span class="sxs-lookup"><span data-stu-id="56da4-148">Relationship to Option Element</span></span>

<span data-ttu-id="56da4-149">Cada uno de los estados posibles se representa mediante un elemento Option.</span><span class="sxs-lookup"><span data-stu-id="56da4-149">Each of the possible states is represented by an Option element.</span></span> <span data-ttu-id="56da4-150">Cada definición de opción contiene uno o varios elementos ScoredProperty, que juntos describen o caracterizan de forma única el estado que se representa.</span><span class="sxs-lookup"><span data-stu-id="56da4-150">Each Option definition contains one or more ScoredProperty elements, which taken together uniquely describe or characterize the state that is being represented.</span></span> <span data-ttu-id="56da4-151">La técnica utilizada para crear definiciones de opción se describe en [Definiciones de opciones](option-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="56da4-151">The technique used to create Option definitions is described in [Option Definitions](option-definitions.md).</span></span> <span data-ttu-id="56da4-152">Todos los elementos Option asociados a un elemento Feature determinado residen como elementos secundarios del elemento Feature.</span><span class="sxs-lookup"><span data-stu-id="56da4-152">All of the Option elements associated with a particular Feature element reside as child elements of the Feature element.</span></span>

### <a name="subfeatures"></a><span data-ttu-id="56da4-153">Subfunciones</span><span class="sxs-lookup"><span data-stu-id="56da4-153">Subfeatures</span></span>

<span data-ttu-id="56da4-154">El marco de esquema de impresión también permite agrupar los elementos Feature de forma jerárquica.</span><span class="sxs-lookup"><span data-stu-id="56da4-154">The Print Schema Framework also allows Feature elements to be grouped together in a hierarchical manner.</span></span> <span data-ttu-id="56da4-155">Es decir, un elemento Feature puede contener uno o varios elementos Feature secundarios (subatures).</span><span class="sxs-lookup"><span data-stu-id="56da4-155">That is, a Feature element can itself contain one or more child Feature elements (subfeatures).</span></span> <span data-ttu-id="56da4-156">Esto puede ser útil para organizar elementos de características relacionados o para elementos de características que controlan aspectos de una característica de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56da4-156">This can be useful for organizing related Feature elements, or for Feature elements that control aspects of a device feature.</span></span> <span data-ttu-id="56da4-157">Un ejemplo es un dispositivo que admite el stapling.</span><span class="sxs-lookup"><span data-stu-id="56da4-157">One example is a device that supports stapling.</span></span> <span data-ttu-id="56da4-158">Este tipo de dispositivo puede ofrecer al usuario la opción de dónde buscar la grapa, como en la esquina superior izquierda, en la esquina superior derecha, en el borde superior o en el borde izquierdo.</span><span class="sxs-lookup"><span data-stu-id="56da4-158">Such a device might offer the user a choice of where to locate the staple, such as at the upper left corner, or the upper right corner, or along the top edge, or along the left edge.</span></span> <span data-ttu-id="56da4-159">La interfaz de usuario (UI) de este dispositivo debe ser capaz de presentar primero al usuario las opciones de nivel más alto, que en este caso es si se debe usar el stapling.</span><span class="sxs-lookup"><span data-stu-id="56da4-159">The user interface (UI) for this device should be able to present the user with the highest level choices first, which in this case is whether to use stapling.</span></span> <span data-ttu-id="56da4-160">Solo después de que el usuario haya decidido usar el stapling, en caso de que se le presente un segundo nivel de opciones, la ubicación de la grapa.</span><span class="sxs-lookup"><span data-stu-id="56da4-160">Only after the user has decided to use stapling should he or she be presented with a second tier of choices, staple location.</span></span> <span data-ttu-id="56da4-161">Una jerarquía de características agrega la estructura adicional que hace posible este tipo de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="56da4-161">A feature hierarchy adds the additional structure that makes such a user interface possible.</span></span> <span data-ttu-id="56da4-162">El marco de esquema de impresión permite que las subaturísticas tengan sus propias subatures secundarias, lo que permite un nivel ilimitado de anidamiento.</span><span class="sxs-lookup"><span data-stu-id="56da4-162">The Print Schema Framework allows subfeatures to have their own child subfeatures, thereby permitting an unlimited level of nesting.</span></span>

<span data-ttu-id="56da4-163">El marco de esquema de impresión también permite que los elementos Option aparezcan en el mismo nivel que las subatures; es decir, como elementos del mismo nivel dentro del mismo elemento principal Feature.</span><span class="sxs-lookup"><span data-stu-id="56da4-163">The Print Schema Framework also allows Option elements to appear at the same level as subfeatures; that is, as siblings within the same parent Feature element.</span></span> <span data-ttu-id="56da4-164">Esto permite al usuario tomar la decisión de alto nivel (si se debe usar el stapling) antes de realizar las selecciones de subfeature.</span><span class="sxs-lookup"><span data-stu-id="56da4-164">This allows the user to make the high level decision (whether to use stapling) before making the subfeature selections.</span></span> <span data-ttu-id="56da4-165">En este ejemplo, el elemento raíz Feature, "Grapa", podría contener dos elementos Option, "On" y "Off", así como una subfeature denominada "StapleLocation".</span><span class="sxs-lookup"><span data-stu-id="56da4-165">For this example the root Feature element, "Staple", might contain two Option elements, "On" and "Off", as well as a subfeature named "StapleLocation".</span></span>

## <a name="example"></a><span data-ttu-id="56da4-166">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="56da4-166">Example</span></span>

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option constrained="psk:None">
    <psf:ScoredProperty name="psk:Bin">
      <psf:Value xsi:type="xs:string">SorterBin</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">100</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="56da4-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56da4-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56da4-168">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="56da4-168">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




