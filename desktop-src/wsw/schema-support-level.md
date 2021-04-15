---
title: Nivel de compatibilidad de esquema
description: En esta sección se tratan los detalles sobre el nivel de compatibilidad con esquemas.
ms.assetid: ca18306e-6d67-406d-9c42-4be159a0b81f
keywords:
- Servicios Web de nivel de compatibilidad de esquemas para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa50eef8835f643abb668b439160ea733bf5160
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104568212"
---
# <a name="schema-support-level"></a><span data-ttu-id="45d60-106">Nivel de compatibilidad de esquema</span><span class="sxs-lookup"><span data-stu-id="45d60-106">Schema support level</span></span>

<span data-ttu-id="45d60-107">En esta sección se tratan los detalles sobre el nivel de compatibilidad con esquemas.</span><span class="sxs-lookup"><span data-stu-id="45d60-107">This section covers the details around the level of schema support.</span></span>


<span data-ttu-id="45d60-108">El esquema admite directamente lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="45d60-108">The schema directly supports the following:</span></span>

-   <span data-ttu-id="45d60-109">Secuencias de elementos.</span><span class="sxs-lookup"><span data-stu-id="45d60-109">Sequences of elements.</span></span>
-   <span data-ttu-id="45d60-110">Derivación de tipos de elemento.</span><span class="sxs-lookup"><span data-stu-id="45d60-110">Derivation of element types.</span></span>
-   <span data-ttu-id="45d60-111">Opciones sencillas de los elementos (los que se asignan a una Unión etiquetada).</span><span class="sxs-lookup"><span data-stu-id="45d60-111">Simple choices of elements (those that map to a tagged union).</span></span>
-   <span data-ttu-id="45d60-112">Tipos básicos definidos por el formato binario XSD/.NET que incluye intervalos (min/max).</span><span class="sxs-lookup"><span data-stu-id="45d60-112">Basic types defined by XSD / .NET binary format including ranges (min/max).</span></span>
-   <span data-ttu-id="45d60-113">Compatibilidad simple con cualquier elemento (sin restricciones en el tipo de elemento).</span><span class="sxs-lookup"><span data-stu-id="45d60-113">Simple support for any element (no restrictions on type of element).</span></span>
-   <span data-ttu-id="45d60-114">Elementos y atributos opcionales con valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="45d60-114">Optional elements and attributes with default values.</span></span>
-   <span data-ttu-id="45d60-115">Elementos repetidos con intervalos (min/max).</span><span class="sxs-lookup"><span data-stu-id="45d60-115">Repeating elements with ranges (min/max).</span></span>
-   <span data-ttu-id="45d60-116">Elementos nillable.</span><span class="sxs-lookup"><span data-stu-id="45d60-116">Nillable elements.</span></span>

<span data-ttu-id="45d60-117">El esquema no admite lo siguiente directamente (lo que implica el comportamiento de "reserva"):</span><span class="sxs-lookup"><span data-stu-id="45d60-117">The schema does not support the following directly (which imply the "fallback" behavior):</span></span>

-   <span data-ttu-id="45d60-118">Tipos básicos definidos por el usuario.</span><span class="sxs-lookup"><span data-stu-id="45d60-118">User defined basic types.</span></span>
-   <span data-ttu-id="45d60-119">Opciones más complicadas.</span><span class="sxs-lookup"><span data-stu-id="45d60-119">More complicated choices.</span></span>
-   <span data-ttu-id="45d60-120">Rechazar atributos desconocidos.</span><span class="sxs-lookup"><span data-stu-id="45d60-120">Rejecting unknown attributes.</span></span>
-   <span data-ttu-id="45d60-121">Ida y vuelta: atributos desconocidos.</span><span class="sxs-lookup"><span data-stu-id="45d60-121">Round tripping unknown attributes.</span></span>
-   <span data-ttu-id="45d60-122">Compatibilidad más complicada con cualquier elemento.</span><span class="sxs-lookup"><span data-stu-id="45d60-122">More complicated support for any element.</span></span>
-   <span data-ttu-id="45d60-123">Construcción ALL.</span><span class="sxs-lookup"><span data-stu-id="45d60-123">The all construct.</span></span>
-   <span data-ttu-id="45d60-124">Key/keyref.</span><span class="sxs-lookup"><span data-stu-id="45d60-124">Key/keyref.</span></span>

<span data-ttu-id="45d60-125">A continuación se ofrece un desglose detallado de la compatibilidad de varios componentes de esquema.</span><span class="sxs-lookup"><span data-stu-id="45d60-125">Following is a detailed breakdown of different schema component support.</span></span> <span data-ttu-id="45d60-126">Se compara con el contrato de datos de WCF porque la similitud en la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="45d60-126">It is compared with data contract in WCF because the similarity in functionality.</span></span> <span data-ttu-id="45d60-127">Se describirá la diferencia.</span><span class="sxs-lookup"><span data-stu-id="45d60-127">The difference will be described.</span></span>

<span data-ttu-id="45d60-128">Por lo general, para los comportamientos de reserva:</span><span class="sxs-lookup"><span data-stu-id="45d60-128">Generally, for fallback behaviors:</span></span>

-   <span data-ttu-id="45d60-129">los atributos están respaldados en la \_ cadena WS;</span><span class="sxs-lookup"><span data-stu-id="45d60-129">attributes are fall backed to WS\_STRING;</span></span>
-   <span data-ttu-id="45d60-130">el contenido del elemento se encuentra respaldado en el \_ búfer XML de WS \_ .</span><span class="sxs-lookup"><span data-stu-id="45d60-130">element content are fall backed to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="45d60-131">los complexType están respaldados en la estructura que contiene un campo de \_ búfer XML de WS \_ .</span><span class="sxs-lookup"><span data-stu-id="45d60-131">complexType are fall backed to structure containing a field of WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="45d60-132">Los tipos simples se incluyen en la \_ cadena WS.</span><span class="sxs-lookup"><span data-stu-id="45d60-132">Simple types are fall backed to WS\_STRING.</span></span>

<span data-ttu-id="45d60-133">wsutil genera advertencias para los componentes de esquema que actualmente no se admiten por completo.</span><span class="sxs-lookup"><span data-stu-id="45d60-133">wsutil generates warnings for schema components that are not currently fully supported.</span></span> <span data-ttu-id="45d60-134">Es posible que la aplicación tenga que realizar una comprobación adicional para que esos componentes sean necesarios.</span><span class="sxs-lookup"><span data-stu-id="45d60-134">Application might need to do additional verification for those components are needed.</span></span> <span data-ttu-id="45d60-135">Se puede mejorar la wsutil de horas extras para controlar algunas de las características que se admiten actualmente en tiempo de ejecución, como la compatibilidad con valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="45d60-135">Overtime wsutil can be improved to handle some of the features that are currently supported in runtime, like default value support.</span></span> <span data-ttu-id="45d60-136">wsutil también se puede mejorar junto con la serialización para admitir otras características como Abstract.</span><span class="sxs-lookup"><span data-stu-id="45d60-136">wsutil can also be improved together with serialization to support other features like abstract.</span></span> <span data-ttu-id="45d60-137">El número de componentes de esquema no admitidos puede reducirse con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="45d60-137">The number of unsupported schema components can be reduced over time.</span></span>

## <a name="the-overall-schema-document"></a><span data-ttu-id="45d60-138">Documento de esquema general</span><span class="sxs-lookup"><span data-stu-id="45d60-138">The Overall Schema Document</span></span>

<span data-ttu-id="45d60-139">Definición global que puede afectar a las definiciones incrustadas en el esquema.</span><span class="sxs-lookup"><span data-stu-id="45d60-139">Global definition that might affect embedded definitions in the schema.</span></span> <span data-ttu-id="45d60-140">Son atributos globales que se aplican a todas las definiciones del esquema.</span><span class="sxs-lookup"><span data-stu-id="45d60-140">These are global attributes that are applicable to all definitions in the schema.</span></span>

<span data-ttu-id="45d60-141">Atributos <XS: Schema></span><span class="sxs-lookup"><span data-stu-id="45d60-141"><xs:schema> attributes</span></span>

-   <span data-ttu-id="45d60-142">attributeFromDefault omitido.</span><span class="sxs-lookup"><span data-stu-id="45d60-142">attributeFromDefault Ignored.</span></span>
-   <span data-ttu-id="45d60-143">se omitió blockDefault.</span><span class="sxs-lookup"><span data-stu-id="45d60-143">blockDefault Ignored.</span></span>
-   <span data-ttu-id="45d60-144">elementFormDefault omitido.</span><span class="sxs-lookup"><span data-stu-id="45d60-144">elementFormDefault Ignored.</span></span> <span data-ttu-id="45d60-145">Esto es diferente de DataContract, ya que se admiten elementos incompletos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="45d60-145">This is different from dataContract as unqualified elements are supported in runtime.</span></span>
-   <span data-ttu-id="45d60-146">no se ha pasado el finalDefault.</span><span class="sxs-lookup"><span data-stu-id="45d60-146">finalDefault Ignored.</span></span> <span data-ttu-id="45d60-147">No hay compatibilidad con el lenguaje C para el concepto de final.</span><span class="sxs-lookup"><span data-stu-id="45d60-147">There is no C language support for the concept of final.</span></span>
-   <span data-ttu-id="45d60-148">identificador omitido.</span><span class="sxs-lookup"><span data-stu-id="45d60-148">id Ignored.</span></span>
-   <span data-ttu-id="45d60-149">targetNamespace se admite y se asigna al espacio de nombres de servicio.</span><span class="sxs-lookup"><span data-stu-id="45d60-149">targetNamespace Supported and mapped to the service namespace.</span></span>
-   <span data-ttu-id="45d60-150">versión omitida.</span><span class="sxs-lookup"><span data-stu-id="45d60-150">version Ignored.</span></span>

<span data-ttu-id="45d60-151"><XS: Schema> contenido</span><span class="sxs-lookup"><span data-stu-id="45d60-151"><xs:schema> contents</span></span>

-   <span data-ttu-id="45d60-152">incluye compatible; wsutil requiere que todas las definiciones necesarias estén disponibles como archivos de entrada durante el tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="45d60-152">include Supported; wsutil requires all necessary definition be available as input files during compilation time.</span></span>
-   <span data-ttu-id="45d60-153">redefinición omitida.</span><span class="sxs-lookup"><span data-stu-id="45d60-153">redefine Ignored.</span></span> <span data-ttu-id="45d60-154">wsutil no lo admite.</span><span class="sxs-lookup"><span data-stu-id="45d60-154">wsutil does not support this.</span></span>
-   <span data-ttu-id="45d60-155">importación admitida; wsutil requiere que todas las definiciones necesarias estén disponibles como archivos de entrada durante el tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="45d60-155">import Supported; wsutil requires all necessary definition be available as input files during compilation time.</span></span>
-   <span data-ttu-id="45d60-156">Compatible con simpleType; vea la sección de tipo simple a continuación.</span><span class="sxs-lookup"><span data-stu-id="45d60-156">simpleType Supported- see simple type section below.</span></span>
-   <span data-ttu-id="45d60-157">complexType compatible: Consulte la sección ' complexType '</span><span class="sxs-lookup"><span data-stu-id="45d60-157">complexType Supported- see 'complexType' section</span></span>
-   <span data-ttu-id="45d60-158">Grupo omitido.</span><span class="sxs-lookup"><span data-stu-id="45d60-158">group Ignored.</span></span>
-   <span data-ttu-id="45d60-159">attributeGroup omitido.</span><span class="sxs-lookup"><span data-stu-id="45d60-159">attributeGroup Ignored.</span></span>
-   <span data-ttu-id="45d60-160">elemento compatible; asigna a definiciones de elementos globales.</span><span class="sxs-lookup"><span data-stu-id="45d60-160">element Supported; maps to global element definitions.</span></span>
-   <span data-ttu-id="45d60-161">atributo admitido; asigna a definiciones de atributos globales.</span><span class="sxs-lookup"><span data-stu-id="45d60-161">attribute Supported; maps to global attribute definitions.</span></span>
-   <span data-ttu-id="45d60-162">notación omitida</span><span class="sxs-lookup"><span data-stu-id="45d60-162">notation Ignored</span></span>

## <a name="complex-type"></a><span data-ttu-id="45d60-163">Tipo complejo</span><span class="sxs-lookup"><span data-stu-id="45d60-163">Complex Type</span></span>

<span data-ttu-id="45d60-164">El tipo complejo, representado por <XS: complexType>, podría ser una restricción del tipo simple o tipo complejo, la extensión de tipo simple, matrices o estructura.</span><span class="sxs-lookup"><span data-stu-id="45d60-164">Complex type, represented by <xs:complexType>, could be restriction of simple type or complex type, extension of simple type, arrays or structure.</span></span> <span data-ttu-id="45d60-165">Observe que, en la extensión de los tipos simples, no hay ninguna herencia ni compatibilidad con xsi: Type.</span><span class="sxs-lookup"><span data-stu-id="45d60-165">Noticed that in extension of simple types, there is no inheritance and no xsi:type support.</span></span>

<span data-ttu-id="45d60-166">Atributos de> <XS: complexType</span><span class="sxs-lookup"><span data-stu-id="45d60-166"><xs:complexType> attributes</span></span>

-   <span data-ttu-id="45d60-167">Resumen de generación de advertencia sobre característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-167">abstract Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="45d60-168">bloquear generar Advertencia sobre característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-168">block Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="45d60-169">última generación de advertencia acerca de la característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-169">final Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="45d60-170">identificador omitido.</span><span class="sxs-lookup"><span data-stu-id="45d60-170">id Ignored.</span></span>
-   <span data-ttu-id="45d60-171">mixed genera una advertencia sobre la característica no admitida, reserva a la estructura con el búfer de WS \_ XML \_ si es true.</span><span class="sxs-lookup"><span data-stu-id="45d60-171">mixed Generate warning about unsupported feature, fallback to structure with WS\_XML\_BUFFER if true.</span></span>
-   <span data-ttu-id="45d60-172">nombre admitido y asignado al nombre del tipo de estructura.</span><span class="sxs-lookup"><span data-stu-id="45d60-172">name Supported and mapped to structure type name.</span></span>

<span data-ttu-id="45d60-173"><el contenido de> XS: complexType</span><span class="sxs-lookup"><span data-stu-id="45d60-173"><xs:complexType> contents</span></span>

<span data-ttu-id="45d60-174">Esta es la definición de tipo de la estructura.</span><span class="sxs-lookup"><span data-stu-id="45d60-174">This is type definition for structure.</span></span> <span data-ttu-id="45d60-175">no se admite la restricción complexContent.</span><span class="sxs-lookup"><span data-stu-id="45d60-175">complexContent restriction is not supported.</span></span>

-   <span data-ttu-id="45d60-176">complexContent admite la extensión de contenido complejo.</span><span class="sxs-lookup"><span data-stu-id="45d60-176">complexContent Support complex content extension.</span></span> <span data-ttu-id="45d60-177">Asigna a la herencia de la estructura.</span><span class="sxs-lookup"><span data-stu-id="45d60-177">Maps to structure inheritance.</span></span>
-   <span data-ttu-id="45d60-178">Agrupe actualmente la reserva en la estructura con el \_ campo de búfer XML de WS \_ .</span><span class="sxs-lookup"><span data-stu-id="45d60-178">group Currently fallback to structure with WS\_XML\_BUFFER field.</span></span> <span data-ttu-id="45d60-179">Se puede admitir según la partícula subyacente.</span><span class="sxs-lookup"><span data-stu-id="45d60-179">Can be supported according to the underneath particle.</span></span>
-   <span data-ttu-id="45d60-180">elección admitida como Unión.</span><span class="sxs-lookup"><span data-stu-id="45d60-180">choice supported as union.</span></span> <span data-ttu-id="45d60-181">Esto no se admite en el contrato de datos.</span><span class="sxs-lookup"><span data-stu-id="45d60-181">This is not supported in data contract.</span></span>
-   <span data-ttu-id="45d60-182">Sequence Supported: se asigna a los campos de una estructura</span><span class="sxs-lookup"><span data-stu-id="45d60-182">sequence Supported - maps to fields of a structure</span></span>
-   <span data-ttu-id="45d60-183">atributo compatible con una excepción de ' prohibido '.</span><span class="sxs-lookup"><span data-stu-id="45d60-183">attribute supported with one exception of 'prohibited'.</span></span> <span data-ttu-id="45d60-184">Reserva para la estructura con el \_ búfer XML de WS \_ si está prohibido.</span><span class="sxs-lookup"><span data-stu-id="45d60-184">fallback to structure with WS\_XML\_BUFFER if 'prohibited'.</span></span>
-   <span data-ttu-id="45d60-185">attributeGroup compatible: se asigna a la secuencia de atributos</span><span class="sxs-lookup"><span data-stu-id="45d60-185">attributeGroup supported - maps to sequence of attributes</span></span>
-   <span data-ttu-id="45d60-186">anyAttribute omitido</span><span class="sxs-lookup"><span data-stu-id="45d60-186">anyAttribute Ignored</span></span>
-   <span data-ttu-id="45d60-187">AttributeGroupRef admitido: se asigna a la secuencia de atributos.</span><span class="sxs-lookup"><span data-stu-id="45d60-187">AttributeGroupRef Supported - maps to sequence of attributes.</span></span>
-   <span data-ttu-id="45d60-188">GroupRef actualmente se reserva en la estructura con el \_ campo de búfer XML de WS \_ .</span><span class="sxs-lookup"><span data-stu-id="45d60-188">GroupRef Currently fallback to structure with WS\_XML\_BUFFER field.</span></span> <span data-ttu-id="45d60-189">Se puede admitir según el grupo subyacente.</span><span class="sxs-lookup"><span data-stu-id="45d60-189">Can be supported according to the underneath group.</span></span>
-   <span data-ttu-id="45d60-190">Cualquier mapa compatible, se asigna a un \_ búfer XML</span><span class="sxs-lookup"><span data-stu-id="45d60-190">Any Supported, maps to XML\_BUFFER</span></span>
-   <span data-ttu-id="45d60-191">(en blanco) se admite la asignación a una descripción de struct vacía sin ninguna estructura generada.</span><span class="sxs-lookup"><span data-stu-id="45d60-191">(blank) supported map to empty struct description with no struct generated.</span></span>

<span data-ttu-id="45d60-192"><xs:sequence> en un tipo complejo: contenido</span><span class="sxs-lookup"><span data-stu-id="45d60-192"><xs:sequence> in a complex type: contents</span></span>

<span data-ttu-id="45d60-193">wsutil solo admite totalmente la secuencia de minOccurs = 1 y maxOccurs = 1; de lo contrario, el tipo complejo se encuentra actualmente respaldado por el \_ búfer XML de WS \_ .</span><span class="sxs-lookup"><span data-stu-id="45d60-193">wsutil only fully support sequence of minOccurs = 1 and maxOccurs = 1; otherwise the complex type is currently fall backed to WS\_XML\_BUFFER.</span></span> <span data-ttu-id="45d60-194">Se puede admitir como una matriz de estructuras.</span><span class="sxs-lookup"><span data-stu-id="45d60-194">It can be supported as array of structures.</span></span>

-   <span data-ttu-id="45d60-195">elemento compatible; cada instancia se asigna a un campo de la estructura.</span><span class="sxs-lookup"><span data-stu-id="45d60-195">element Supported; each instance maps to a field in the structure.</span></span>
-   <span data-ttu-id="45d60-196">Reserva de grupo; complexType es fallback en el \_ búfer XML de WS \_ .</span><span class="sxs-lookup"><span data-stu-id="45d60-196">Group fallback; the complexType is fallback to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="45d60-197">Toda la reserva; complexType es fallback en el \_ búfer XML de WS \_ .</span><span class="sxs-lookup"><span data-stu-id="45d60-197">All fallback; the complexType is fallback to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="45d60-198">elección admitida; asignar a campo de Unión.</span><span class="sxs-lookup"><span data-stu-id="45d60-198">choice supported; map to union field.</span></span>
-   <span data-ttu-id="45d60-199">Reserva de secuencia; complexType es fallback en el \_ búfer XML de WS \_ .</span><span class="sxs-lookup"><span data-stu-id="45d60-199">sequence fallback; the complexType is fallback to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="45d60-200">cualquier compatible; asignado a \_ búfer XML.</span><span class="sxs-lookup"><span data-stu-id="45d60-200">any Supported; mapped to XML\_BUFFER.</span></span>
-   <span data-ttu-id="45d60-201">(en blanco) admitido; complexType puede ser una estructura vacía si no hay ningún atributo.</span><span class="sxs-lookup"><span data-stu-id="45d60-201">(blank) supported; complexType can be an empty structure if there is no attributes.</span></span>

## <a name="elements"></a><span data-ttu-id="45d60-202">Elementos</span><span class="sxs-lookup"><span data-stu-id="45d60-202">Elements</span></span>

<span data-ttu-id="45d60-203"><XS: Element>pueden aparecer en tres contextos.</span><span class="sxs-lookup"><span data-stu-id="45d60-203"><xs:element>may occur in three contexts.</span></span>

-   <span data-ttu-id="45d60-204">Puede producirse dentro de una <XS: Sequence>, que describe un campo de un struct normal.</span><span class="sxs-lookup"><span data-stu-id="45d60-204">It may occur within an <xs:sequence>, describing a field of a regular struct.</span></span> <span data-ttu-id="45d60-205">En este caso, el atributo maxOccurs debe ser 1.</span><span class="sxs-lookup"><span data-stu-id="45d60-205">In this case, the maxOccurs attribute must be 1.</span></span> <span data-ttu-id="45d60-206">El campo es opcional si minOccurs es 0.</span><span class="sxs-lookup"><span data-stu-id="45d60-206">The field is optional if minOccurs is 0.</span></span>
-   <span data-ttu-id="45d60-207">Puede producirse dentro de una <XS: Sequence>, que describe un campo de una matriz.</span><span class="sxs-lookup"><span data-stu-id="45d60-207">It may occur within an <xs:sequence>, describing a field of an array.</span></span> <span data-ttu-id="45d60-208">En este caso, el atributo maxOccurs debe ser mayor que 1 o "ilimitado".</span><span class="sxs-lookup"><span data-stu-id="45d60-208">In this case, the maxOccurs attribute must be greater than 1 or 'unbounded'.</span></span>
-   <span data-ttu-id="45d60-209">Puede producirse dentro de una <XS: Schema> como una descripción de elemento global.</span><span class="sxs-lookup"><span data-stu-id="45d60-209">It may occur within an <xs:schema> as a global element description.</span></span>

<span data-ttu-id="45d60-210"><> XS: Element dentro de un <XS: Sequence> o <XS: Choice> como un campo en una estructura</span><span class="sxs-lookup"><span data-stu-id="45d60-210"><xs:element> within an <xs:sequence> or <xs:choice> as a field in a structure</span></span>

-   <span data-ttu-id="45d60-211">referencia admitida; se resuelve como una referencia a un elemento global.</span><span class="sxs-lookup"><span data-stu-id="45d60-211">ref Supported; resolved to reference to global element.</span></span>
-   <span data-ttu-id="45d60-212">nombre admitido, se asigna al nombre del campo.</span><span class="sxs-lookup"><span data-stu-id="45d60-212">name Supported, maps to field name.</span></span>
-   <span data-ttu-id="45d60-213">tipo admitido, se asigna al tipo de campo.</span><span class="sxs-lookup"><span data-stu-id="45d60-213">type Supported, maps to field type.</span></span> <span data-ttu-id="45d60-214">Para obtener más información, vea ' asignación de tipos '.</span><span class="sxs-lookup"><span data-stu-id="45d60-214">For more information, see 'Type Mapping'.</span></span> <span data-ttu-id="45d60-215">Si no se especifica (y el elemento no contiene un tipo anónimo), se supone XS: anyType.</span><span class="sxs-lookup"><span data-stu-id="45d60-215">If not specified (and the element does not contain an anonymous type), xs:anyType is assumed.</span></span>
-   <span data-ttu-id="45d60-216">bloquear generar Advertencia sobre característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-216">block Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="45d60-217">Generar ADVERTENCIA predeterminada sobre la característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-217">default Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="45d60-218">se corrigió la advertencia generada sobre la característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-218">fixed Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="45d60-219">formulario omitido.</span><span class="sxs-lookup"><span data-stu-id="45d60-219">form Ignored.</span></span> <span data-ttu-id="45d60-220">Nuestra capa de serialización admite formularios completos e incompletos.</span><span class="sxs-lookup"><span data-stu-id="45d60-220">Our serialization layer supports both qualified and unqualified forms.</span></span>
-   <span data-ttu-id="45d60-221">identificador omitido.</span><span class="sxs-lookup"><span data-stu-id="45d60-221">id Ignored.</span></span>
-   <span data-ttu-id="45d60-222">maxOccurs se asigna a un único campo de datos si es igual a 1.</span><span class="sxs-lookup"><span data-stu-id="45d60-222">maxOccurs maps to a single data field if equals 1.</span></span> <span data-ttu-id="45d60-223">se asigna a un campo de matriz (elemento repetitivo) si maxOccurs es mayor que 1.</span><span class="sxs-lookup"><span data-stu-id="45d60-223">it is mapped to an array field (repeating element) if maxOccurs is larger than 1.</span></span>
-   <span data-ttu-id="45d60-224">minOccurs si es 0, las opciones de campo se establecen en campo \_ opcional, si no se establece nillable.</span><span class="sxs-lookup"><span data-stu-id="45d60-224">minOccurs if 0, the field options is set to FIELD\_OPTIONAL, if nillable is not set.</span></span>
-   <span data-ttu-id="45d60-225">nillable el campo es nillable.</span><span class="sxs-lookup"><span data-stu-id="45d60-225">nillable The field is nillable.</span></span> <span data-ttu-id="45d60-226">Vea [serialización](serialization.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="45d60-226">See [Serialization](serialization.md) for more detail.</span></span>

<span data-ttu-id="45d60-227"><XS: Element> como elemento global: Attributes</span><span class="sxs-lookup"><span data-stu-id="45d60-227"><xs:element> as global element: attributes</span></span>

<span data-ttu-id="45d60-228">los atributos minOccurs y maxOccurs no son válidos como descripción de elementos globales.</span><span class="sxs-lookup"><span data-stu-id="45d60-228">minOccurs and maxOccurs attributes are invalid as global element description.</span></span> <span data-ttu-id="45d60-229">La aplicación puede usar la descripción de elementos generados directamente en capas de canal o de nivel de serialización.</span><span class="sxs-lookup"><span data-stu-id="45d60-229">Application can use generated element description in serialization layer or channel layers directly.</span></span>

-   <span data-ttu-id="45d60-230">Resumen de generación de advertencia sobre característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-230">abstract Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="45d60-231">bloquear generar Advertencia sobre característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-231">block Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="45d60-232">Generar ADVERTENCIA predeterminada sobre la característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-232">default Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="45d60-233">última generación de advertencia acerca de la característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-233">final Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="45d60-234">se corrigió la advertencia generada sobre la característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-234">fixed Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="45d60-235">identificador omitido.</span><span class="sxs-lookup"><span data-stu-id="45d60-235">id Ignored.</span></span>
-   <span data-ttu-id="45d60-236">Name Supported: asignar al nombre de la descripción del elemento global y es la base para el tipo anónimo cuando se especifica.</span><span class="sxs-lookup"><span data-stu-id="45d60-236">name Supported- map to name of the global element description, and it is the base for the anonymous type when specified.</span></span>
-   <span data-ttu-id="45d60-237">se omitieron los nillable: la aplicación debe llamar a con la marca derecha.</span><span class="sxs-lookup"><span data-stu-id="45d60-237">nillable Ignored-application needs to call with right flag.</span></span>
-   <span data-ttu-id="45d60-238">Reserva de substitutionGroup en la estructura con el búfer de WS \_ XML \_ si está establecido.</span><span class="sxs-lookup"><span data-stu-id="45d60-238">substitutionGroup fallback to structure with WS\_XML\_BUFFER if set.</span></span> <span data-ttu-id="45d60-239">wsutil no admite substitutionGroup.</span><span class="sxs-lookup"><span data-stu-id="45d60-239">wsutil does not support substitutionGroup.</span></span>
-   <span data-ttu-id="45d60-240">Escriba compatible y asígnelo al tipo del elemento.</span><span class="sxs-lookup"><span data-stu-id="45d60-240">type Supported and map to the type of the element.</span></span>

<span data-ttu-id="45d60-241"><XS: Element> como elemento global: Contents</span><span class="sxs-lookup"><span data-stu-id="45d60-241"><xs:element> as global element: contents</span></span>

-   <span data-ttu-id="45d60-242">simpleType compatible; asigna a la definición de tipo.</span><span class="sxs-lookup"><span data-stu-id="45d60-242">simpleType Supported; maps to type definition.</span></span>
-   <span data-ttu-id="45d60-243">complexType compatible; se asigna a un tipo complejo.</span><span class="sxs-lookup"><span data-stu-id="45d60-243">complexType supported; maps to a complex type.</span></span>
-   <span data-ttu-id="45d60-244">Unique genera una advertencia sobre la característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-244">unique Generate warning about unsupported feature, no change to code generation.</span></span> <span data-ttu-id="45d60-245">wsutil no admite restricciones Element.</span><span class="sxs-lookup"><span data-stu-id="45d60-245">wsutil does not support element constraints.</span></span>
-   <span data-ttu-id="45d60-246">clave genera una advertencia sobre la característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-246">key Generate warning about unsupported feature, no change to code generation.</span></span> <span data-ttu-id="45d60-247">wsutil no admite restricciones Element.</span><span class="sxs-lookup"><span data-stu-id="45d60-247">wsutil does not support element constraints.</span></span>
-   <span data-ttu-id="45d60-248">keyref genera una advertencia sobre la característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-248">keyref Generate warning about unsupported feature, no change to code generation.</span></span> <span data-ttu-id="45d60-249">wsutil no admite restricciones Element.</span><span class="sxs-lookup"><span data-stu-id="45d60-249">wsutil does not support element constraints.</span></span>
-   <span data-ttu-id="45d60-250">en blanco Realizar el elemento sin especificación de tipo se trata como XS: anyType.</span><span class="sxs-lookup"><span data-stu-id="45d60-250">(blank) Supported; element with no type specification is treated as xs:anyType.</span></span>

## <a name="simple-types"></a><span data-ttu-id="45d60-251">Tipos simples</span><span class="sxs-lookup"><span data-stu-id="45d60-251">Simple Types</span></span>

<span data-ttu-id="45d60-252"><atributos> XS: simpleType</span><span class="sxs-lookup"><span data-stu-id="45d60-252"><xs:simpleType> attributes</span></span>

-   <span data-ttu-id="45d60-253">Última generación de advertencia acerca de la característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-253">Final Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="45d60-254">Identificador omitido</span><span class="sxs-lookup"><span data-stu-id="45d60-254">Id Ignored</span></span>
-   <span data-ttu-id="45d60-255">Nombre admitido, se asigna al nombre de tipo.</span><span class="sxs-lookup"><span data-stu-id="45d60-255">Name Supported, maps to type name.</span></span>

<span data-ttu-id="45d60-256"><el contenido de> XS: simpleType</span><span class="sxs-lookup"><span data-stu-id="45d60-256"><xs:simpleType> contents</span></span>

-   <span data-ttu-id="45d60-257">Restricción admitida, se asigna al tipo de enumeración o intervalo.</span><span class="sxs-lookup"><span data-stu-id="45d60-257">Restriction Supported, maps to enum type or range.</span></span> <span data-ttu-id="45d60-258">Vea la sección "restricciones XS: simpleType".</span><span class="sxs-lookup"><span data-stu-id="45d60-258">See "xs:simpleType restrictions" section.</span></span>
-   <span data-ttu-id="45d60-259">List generar Advertencia sobre la característica no admitida, reserva a \_ búfer XML.</span><span class="sxs-lookup"><span data-stu-id="45d60-259">List Generate warning about unsupported feature, fallback to XML\_BUFFER.</span></span>
-   <span data-ttu-id="45d60-260">La Unión genera una advertencia sobre la característica no admitida, reserva a \_ búfer XML.</span><span class="sxs-lookup"><span data-stu-id="45d60-260">Union Generate warning about unsupported feature, fallback to XML\_BUFFER.</span></span>

## <a name="simple-type-restriction"></a><span data-ttu-id="45d60-261">Restricción de tipo simple</span><span class="sxs-lookup"><span data-stu-id="45d60-261">Simple Type restriction</span></span>

<span data-ttu-id="45d60-262">Se permiten ciertas caras en tipos enteros y cadenas de tipo para permitir la compatibilidad con el intervalo y la enumeración.</span><span class="sxs-lookup"><span data-stu-id="45d60-262">Certain facets are allowed in integral types and strings type to allow range and enum support.</span></span>

<span data-ttu-id="45d60-263">compatibilidad de enumeración</span><span class="sxs-lookup"><span data-stu-id="45d60-263">enumeration support</span></span>

<span data-ttu-id="45d60-264"><XS: Enumeration> restricción de tipo simple para el tipo base de cadena se trata como tipo de enumeración.</span><span class="sxs-lookup"><span data-stu-id="45d60-264"><xs:enumeration> simple type restriction for base type of string is treated as enum type.</span></span> <span data-ttu-id="45d60-265">En este caso, el atributo base debe ser de tipo cadena.</span><span class="sxs-lookup"><span data-stu-id="45d60-265">In this case, the Base attribute MUST be string type.</span></span> <span data-ttu-id="45d60-266">En el caso de la enumeración, se omiten todas las demás caras.</span><span class="sxs-lookup"><span data-stu-id="45d60-266">In enumeration case, all other facets are ignored.</span></span>

<span data-ttu-id="45d60-267">intervalo en compatibilidad con tipos simples</span><span class="sxs-lookup"><span data-stu-id="45d60-267">range on simple type support</span></span>

<span data-ttu-id="45d60-268">Algunas de las caras son compatibles con los tipos simples, lo que permite un intervalo eficaz permitido en el tipo.</span><span class="sxs-lookup"><span data-stu-id="45d60-268">Some facets are support in simple types support effectively range allowed on the type.</span></span> <span data-ttu-id="45d60-269">A continuación se enumeran las restricciones para los tipos enteros y los tipos float/double.</span><span class="sxs-lookup"><span data-stu-id="45d60-269">Following are restriction for integral types and float/double types.</span></span> <span data-ttu-id="45d60-270">Los tipos simples con otras caras se incluyen en el tipo de \_ cadena WS</span><span class="sxs-lookup"><span data-stu-id="45d60-270">Simple types with other facets are fall backed to WS\_STRING type</span></span>

-   <span data-ttu-id="45d60-271">minExclusive compatible</span><span class="sxs-lookup"><span data-stu-id="45d60-271">minExclusive Supported</span></span>
-   <span data-ttu-id="45d60-272">minInclusive compatible</span><span class="sxs-lookup"><span data-stu-id="45d60-272">minInclusive Supported</span></span>
-   <span data-ttu-id="45d60-273">maxExclusive compatible</span><span class="sxs-lookup"><span data-stu-id="45d60-273">maxExclusive Supported</span></span>
-   <span data-ttu-id="45d60-274">maxInclusive compatible</span><span class="sxs-lookup"><span data-stu-id="45d60-274">maxInclusive Supported</span></span>
-   <span data-ttu-id="45d60-275">totalDigits genera una advertencia sobre la característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-275">totalDigits Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="45d60-276">fractionDigits genera una advertencia sobre la característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-276">fractionDigits Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="45d60-277">la longitud genera una advertencia sobre la característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-277">length Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="45d60-278">minLength genera una advertencia sobre la característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-278">minLength Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="45d60-279">maxLength generar Advertencia sobre la característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-279">maxLength Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="45d60-280">la enumeración genera una advertencia sobre la característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-280">enumeration Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="45d60-281">el espacio en blanco genera una advertencia sobre la característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-281">whiteSpace Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="45d60-282">patrón generar Advertencia sobre la característica no admitida, sin cambios en la generación de código.</span><span class="sxs-lookup"><span data-stu-id="45d60-282">pattern Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="45d60-283">en blanco Realizar.</span><span class="sxs-lookup"><span data-stu-id="45d60-283">(blank) Supported.</span></span>

<span data-ttu-id="45d60-284">en la actualidad, minLength y maxLength en una cadena no se admiten, pero es una característica deseable para admitir.</span><span class="sxs-lookup"><span data-stu-id="45d60-284">minLength and maxLength on string is not supported currently but is a desirable feature to support.</span></span>

## <a name="inheritance"></a><span data-ttu-id="45d60-285">Herencia</span><span class="sxs-lookup"><span data-stu-id="45d60-285">Inheritance</span></span>

<span data-ttu-id="45d60-286">Wsutil admite la herencia de tipos complejos, es decir, una estructura puede heredar de otra estructura, similar a la herencia de interfaces en C++.</span><span class="sxs-lookup"><span data-stu-id="45d60-286">Wsutil supports inheritance of complex types, that is, a structure can inherit from another structure, similar to interface inheritance in C++.</span></span> <span data-ttu-id="45d60-287">Esto se hace a través de <> XS: complexContentExtension.</span><span class="sxs-lookup"><span data-stu-id="45d60-287">This is done through <xs:complexContentExtension>.</span></span> <span data-ttu-id="45d60-288">Se admite <> XS: simpleContentExtension, pero se genera como una estructura sin formato con el tipo base como primer campo en lugar de herencia de tipos.</span><span class="sxs-lookup"><span data-stu-id="45d60-288"><xs:simpleContentExtension> is supported but is generated as plain structure with base type as first field instead of type inheritance.</span></span>

## <a name="typeprimitive-mapping"></a><span data-ttu-id="45d60-289">Asignación de tipo/primitivo.</span><span class="sxs-lookup"><span data-stu-id="45d60-289">Type/primitive mapping</span></span>

<span data-ttu-id="45d60-290">Los identificadores deben normalizarse al traducir de NCName en XML.</span><span class="sxs-lookup"><span data-stu-id="45d60-290">Identifiers needs to be normalized when translating from NCNames in XML.</span></span> <span data-ttu-id="45d60-291">Las cadenas son nillable; los tipos de puntero son nillable; los tipos enteros y float/double son nillable y defaultValue se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="45d60-291">Strings are nillable; pointer types are nillable; integral types and float/double are nillable and defaultValue is set to 0.</span></span>

![Tabla que muestra la asignación entre los tipos XSD y los tipos de datos Sapphire.](images/schematypemap.png)

 

 




