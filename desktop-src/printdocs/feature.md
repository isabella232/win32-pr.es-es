---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 5a6553c2-f322-47e2-bbc8-44f6541f1288
title: Característica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89655181563e2da3a8d4841b1d90ecd4e6ac07
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707612"
---
# <a name="feature"></a><span data-ttu-id="1fda2-104">Característica</span><span class="sxs-lookup"><span data-stu-id="1fda2-104">Feature</span></span>

<span data-ttu-id="1fda2-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="1fda2-105">This topic is not current.</span></span> <span data-ttu-id="1fda2-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1fda2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1fda2-107">Un elemento de característica contiene una lista completa de los elementos de propiedad y opción que describen completamente un atributo de dispositivo, la configuración de formato del trabajo u otras características relevantes.</span><span class="sxs-lookup"><span data-stu-id="1fda2-107">A Feature element contains a complete list of the Option and Property elements that fully describe a device attribute, job formatting setting, or other relevant characteristic.</span></span>

## <a name="element-tag"></a><span data-ttu-id="1fda2-108">Etiqueta de elemento</span><span class="sxs-lookup"><span data-stu-id="1fda2-108">Element Tag</span></span>

<Feature>

## <a name="xml-attributes"></a><span data-ttu-id="1fda2-109">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="1fda2-109">XML Attributes</span></span>

<span data-ttu-id="1fda2-110">En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.</span><span class="sxs-lookup"><span data-stu-id="1fda2-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="1fda2-111">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="1fda2-111">XML Attribute</span></span>   | <span data-ttu-id="1fda2-112">Detalles</span><span class="sxs-lookup"><span data-stu-id="1fda2-112">Details</span></span>                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fda2-113">name</span><span class="sxs-lookup"><span data-stu-id="1fda2-113">name</span></span><br/> | <span data-ttu-id="1fda2-114">Contiene el nombre de la característica, ya sea una característica estándar o una característica definida de forma privada.</span><span class="sxs-lookup"><span data-stu-id="1fda2-114">Holds the name of the Feature, either a standard Feature or a privately-defined Feature.</span></span> <br/> |



 

<span data-ttu-id="1fda2-115">Para obtener más información, consulte la sección [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="1fda2-115">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="1fda2-116">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1fda2-116">Element Information</span></span>

<span data-ttu-id="1fda2-117">En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.</span><span class="sxs-lookup"><span data-stu-id="1fda2-117">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1fda2-118">Category</span><span class="sxs-lookup"><span data-stu-id="1fda2-118">Category</span></span></th>
<th><span data-ttu-id="1fda2-119">Detalles</span><span class="sxs-lookup"><span data-stu-id="1fda2-119">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1fda2-120">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="1fda2-120">Parent elements</span></span><br/></td>
<td><span data-ttu-id="1fda2-121">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="1fda2-121">PrintCapabilities</span></span> <br/> <span data-ttu-id="1fda2-122">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="1fda2-122">PrintTicket</span></span> <br/> <span data-ttu-id="1fda2-123">Característica</span><span class="sxs-lookup"><span data-stu-id="1fda2-123">Feature</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fda2-124">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1fda2-124">Child elements</span></span><br/></td>
<td><span data-ttu-id="1fda2-125">Uno de los siguientes grupos:</span><span class="sxs-lookup"><span data-stu-id="1fda2-125">One of the following groups:</span></span><br/>
<ul>
<li><span data-ttu-id="1fda2-126"><em>Característica</em> (cero o más)</span><span class="sxs-lookup"><span data-stu-id="1fda2-126"><em>Feature</em> (zero or more)</span></span><br/></li>
<li><span data-ttu-id="1fda2-127"><em>Opción</em> (uno o varios)</span><span class="sxs-lookup"><span data-stu-id="1fda2-127"><em>Option</em> (one or more)</span></span><br/></li>
<li><span data-ttu-id="1fda2-128"><em>Propiedad</em> (cero o más)</span><span class="sxs-lookup"><span data-stu-id="1fda2-128"><em>Property</em> (zero or more)</span></span><br/></li>
</ul>
<span data-ttu-id="1fda2-129">or</span><span class="sxs-lookup"><span data-stu-id="1fda2-129">or</span></span> <br/>
<ul>
<li><span data-ttu-id="1fda2-130"><em>Característica</em> (uno o más)</span><span class="sxs-lookup"><span data-stu-id="1fda2-130"><em>Feature</em> (one or more)</span></span><br/></li>
<li><span data-ttu-id="1fda2-131"><em>Opción</em> (cero o más)</span><span class="sxs-lookup"><span data-stu-id="1fda2-131"><em>Option</em> (zero or more)</span></span><br/></li>
<li><span data-ttu-id="1fda2-132"><em>Propiedad</em> (cero o más)</span><span class="sxs-lookup"><span data-stu-id="1fda2-132"><em>Property</em> (zero or more)</span></span><br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fda2-133">Este elemento</span><span class="sxs-lookup"><span data-stu-id="1fda2-133">This element</span></span><br/></td>
<td><span data-ttu-id="1fda2-134">No se permiten datos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1fda2-134">No character data is permitted.</span></span><br/> <span data-ttu-id="1fda2-135">Se permiten los elementos de opción secundarios duplicados que son del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="1fda2-135">Duplicate child Option elements that are siblings are permitted.</span></span> <span data-ttu-id="1fda2-136">Se permiten los métodos abreviados de atributo de nombre duplicados.</span><span class="sxs-lookup"><span data-stu-id="1fda2-136">Duplicate name attribute shortcuts permitted.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="configuration-dependencies"></a><span data-ttu-id="1fda2-137">Dependencias de configuración</span><span class="sxs-lookup"><span data-stu-id="1fda2-137">Configuration Dependencies</span></span>

<span data-ttu-id="1fda2-138">Es posible que los elementos de característica no tengan dependencias de configuración.</span><span class="sxs-lookup"><span data-stu-id="1fda2-138">Feature elements may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="1fda2-139">Uso de elementos</span><span class="sxs-lookup"><span data-stu-id="1fda2-139">Element Usage</span></span>

### <a name="relationship-to-xml-attributes"></a><span data-ttu-id="1fda2-140">Relación con atributos XML</span><span class="sxs-lookup"><span data-stu-id="1fda2-140">Relationship to XML Attributes</span></span>

<span data-ttu-id="1fda2-141">En la representación de características y opciones, un atributo de dispositivo se representa mediante un elemento de característica.</span><span class="sxs-lookup"><span data-stu-id="1fda2-141">In Feature/Option representation, a device attribute is represented by a Feature element.</span></span> <span data-ttu-id="1fda2-142">El atributo de dispositivo se identifica de forma única mediante el atributo de nombre en el elemento de característica del atributo de dispositivo, como en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="1fda2-142">The device attribute is uniquely identified by the name attribute in the device attribute's Feature element, as in the following example.</span></span> <span data-ttu-id="1fda2-143">En este ejemplo, el atributo de dispositivo es resolución.</span><span class="sxs-lookup"><span data-stu-id="1fda2-143">In this example, the device attribute is Resolution.</span></span>

``` syntax
<Feature name="Resolution" />
```

<span data-ttu-id="1fda2-144">El esquema de impresión define un conjunto de atributos de nombre para determinadas instancias de características.</span><span class="sxs-lookup"><span data-stu-id="1fda2-144">The Print Schema defines a set of name attributes for certain Feature instances.</span></span> <span data-ttu-id="1fda2-145">Estos atributos de nombre sirven para identificar un conjunto de instancias de características predefinidas asociadas a atributos de dispositivo configurables concretos.</span><span class="sxs-lookup"><span data-stu-id="1fda2-145">These name attributes serve to identify a set of predefined Feature instances associated with specific configurable device attributes.</span></span> <span data-ttu-id="1fda2-146">Estos nombres de instancia de características deben usarse siempre que proceda, ya que aumentan la portabilidad del documento de PrintCapabilities y los elementos PrintTicket derivados de ellos.</span><span class="sxs-lookup"><span data-stu-id="1fda2-146">These Feature instance names should be used whenever applicable, because they increase the portability of your PrintCapabilities document and the PrintTickets that are derived from them.</span></span> <span data-ttu-id="1fda2-147">Es posible que se introduzcan instancias de características definidas de forma privada si determinados atributos de dispositivo no corresponden a ninguna de las instancias de características definidas por el esquema.</span><span class="sxs-lookup"><span data-stu-id="1fda2-147">Privately-defined Feature instances may be introduced if certain device attributes do not correspond to any of the schema-defined Feature instances.</span></span> <span data-ttu-id="1fda2-148">Para obtener información sobre la sintaxis de los atributos name y las convenciones que se aplican a los nombres definidos por el esquema y los definidos por el personal, vea [atributos XML](xml-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="1fda2-148">For information about the syntax for name attributes and the conventions that apply to schema-defined and privately-defined names, see [XML Attributes](xml-attributes.md).</span></span>

### <a name="relationship-to-option-element"></a><span data-ttu-id="1fda2-149">Relación con el elemento OPTION</span><span class="sxs-lookup"><span data-stu-id="1fda2-149">Relationship to Option Element</span></span>

<span data-ttu-id="1fda2-150">Cada uno de los Estados posibles se representa mediante un elemento OPTION.</span><span class="sxs-lookup"><span data-stu-id="1fda2-150">Each of the possible states is represented by an Option element.</span></span> <span data-ttu-id="1fda2-151">Cada definición de opción contiene uno o más elementos ScoredProperty, que se han tomado juntos de forma única o caracterizan el estado que se está representando.</span><span class="sxs-lookup"><span data-stu-id="1fda2-151">Each Option definition contains one or more ScoredProperty elements, which taken together uniquely describe or characterize the state that is being represented.</span></span> <span data-ttu-id="1fda2-152">La técnica que se usa para crear definiciones de opciones se describe en [definiciones de opciones](option-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="1fda2-152">The technique used to create Option definitions is described in [Option Definitions](option-definitions.md).</span></span> <span data-ttu-id="1fda2-153">Todos los elementos Option asociados a un elemento Feature determinado residen como elementos secundarios del elemento Feature.</span><span class="sxs-lookup"><span data-stu-id="1fda2-153">All of the Option elements associated with a particular Feature element reside as child elements of the Feature element.</span></span>

### <a name="subfeatures"></a><span data-ttu-id="1fda2-154">Subcaracterísticas</span><span class="sxs-lookup"><span data-stu-id="1fda2-154">Subfeatures</span></span>

<span data-ttu-id="1fda2-155">El marco de trabajo del esquema de impresión también permite agrupar elementos de características de forma jerárquica.</span><span class="sxs-lookup"><span data-stu-id="1fda2-155">The Print Schema Framework also allows Feature elements to be grouped together in a hierarchical manner.</span></span> <span data-ttu-id="1fda2-156">Es decir, un elemento de característica puede contener uno o más elementos de característica secundarios (subcaracterísticas).</span><span class="sxs-lookup"><span data-stu-id="1fda2-156">That is, a Feature element can itself contain one or more child Feature elements (subfeatures).</span></span> <span data-ttu-id="1fda2-157">Esto puede ser útil para organizar elementos de características relacionados o para elementos de características que controlan aspectos de una característica de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fda2-157">This can be useful for organizing related Feature elements, or for Feature elements that control aspects of a device feature.</span></span> <span data-ttu-id="1fda2-158">Un ejemplo es un dispositivo que admite grapado.</span><span class="sxs-lookup"><span data-stu-id="1fda2-158">One example is a device that supports stapling.</span></span> <span data-ttu-id="1fda2-159">Este dispositivo podría ofrecer al usuario una opción para ubicar la grapa, como en la esquina superior izquierda o en la esquina superior derecha, o a lo largo del borde superior, o a lo largo del borde izquierdo.</span><span class="sxs-lookup"><span data-stu-id="1fda2-159">Such a device might offer the user a choice of where to locate the staple, such as at the upper left corner, or the upper right corner, or along the top edge, or along the left edge.</span></span> <span data-ttu-id="1fda2-160">La interfaz de usuario (UI) de este dispositivo debe ser capaz de presentar al usuario las opciones de nivel más alto en primer lugar, que en este caso es si se debe usar el grapado.</span><span class="sxs-lookup"><span data-stu-id="1fda2-160">The user interface (UI) for this device should be able to present the user with the highest level choices first, which in this case is whether to use stapling.</span></span> <span data-ttu-id="1fda2-161">Solo después de que el usuario haya decidido usar el grapado, debe encontrarse con un segundo nivel de opciones, grapar ubicación.</span><span class="sxs-lookup"><span data-stu-id="1fda2-161">Only after the user has decided to use stapling should he or she be presented with a second tier of choices, staple location.</span></span> <span data-ttu-id="1fda2-162">Una jerarquía de características agrega la estructura adicional que hace posible la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fda2-162">A feature hierarchy adds the additional structure that makes such a user interface possible.</span></span> <span data-ttu-id="1fda2-163">El marco de trabajo de esquema de impresión permite que las subcaracterísticas tengan sus propias subcaracterísticas secundarias, lo que permite un nivel ilimitado de anidamiento.</span><span class="sxs-lookup"><span data-stu-id="1fda2-163">The Print Schema Framework allows subfeatures to have their own child subfeatures, thereby permitting an unlimited level of nesting.</span></span>

<span data-ttu-id="1fda2-164">El marco de trabajo de esquema de impresión también permite que los elementos de opción aparezcan en el mismo nivel que las subcaracterísticas; es decir, como elementos del mismo nivel dentro del mismo elemento de la característica primaria.</span><span class="sxs-lookup"><span data-stu-id="1fda2-164">The Print Schema Framework also allows Option elements to appear at the same level as subfeatures; that is, as siblings within the same parent Feature element.</span></span> <span data-ttu-id="1fda2-165">Esto permite al usuario tomar la decisión de alto nivel (si se va a usar el grapado) antes de realizar las selecciones de subcaracterísticas.</span><span class="sxs-lookup"><span data-stu-id="1fda2-165">This allows the user to make the high level decision (whether to use stapling) before making the subfeature selections.</span></span> <span data-ttu-id="1fda2-166">En este ejemplo, el elemento de característica raíz, "Grapate", puede contener dos elementos Option, "ON" y "OFF", así como una subcaracterística denominada "StapleLocation".</span><span class="sxs-lookup"><span data-stu-id="1fda2-166">For this example the root Feature element, "Staple", might contain two Option elements, "On" and "Off", as well as a subfeature named "StapleLocation".</span></span>

## <a name="example"></a><span data-ttu-id="1fda2-167">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1fda2-167">Example</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="1fda2-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1fda2-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fda2-169">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="1fda2-169">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




