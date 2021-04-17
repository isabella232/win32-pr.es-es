---
title: Algoritmo y esquema de perfil del modelo de apariencia de color de WCS
description: Algoritmo y esquema de perfil del modelo de apariencia de color de WCS
ms.assetid: 017588fe-cec9-4178-a912-7950cefc036c
keywords:
- Sistema de color de Windows (WCS), perfil de modelo de apariencia de color (CAMP)
- WCS (sistema de color de Windows), perfil de modelo de apariencia de color (CAMP)
- Administración del color de imagen, perfil de modelo de apariencia de color (CAMP)
- Administración del color, perfil de modelo de apariencia de color (CAMP)
- colores, perfil de modelo de apariencia de color (CAMP)
- Sistema de color de Windows (WCS), perfiles
- WCS (sistema de colores de Windows), perfiles
- Administración del color de imagen, perfiles
- Administración del color, perfiles
- colores, perfiles
- Perfil de modelo de apariencia de color (CAMP)
- CAMP (Perfil de modelo de apariencia de color)
- esquemas, perfil de modelo de apariencia de color (CAMP)
- algoritmos, perfil de modelo de apariencia de color (CAMP)
- Perfil de modelo de apariencia de color WCS
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a928aebcfe02f1db39de2452a0b49e5c888bccc
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "105721177"
---
# <a name="wcs-color-appearance-model-profile-schema-and-algorithm"></a><span data-ttu-id="4863d-118">Algoritmo y esquema de perfil del modelo de apariencia de color de WCS</span><span class="sxs-lookup"><span data-stu-id="4863d-118">WCS Color Appearance Model Profile Schema and Algorithm</span></span>

[<span data-ttu-id="4863d-119">Información general</span><span class="sxs-lookup"><span data-stu-id="4863d-119">Overview</span></span>](#overview)

[<span data-ttu-id="4863d-120">Arquitectura de Perfil de modelo de apariencia de color (CAMP)</span><span class="sxs-lookup"><span data-stu-id="4863d-120">Color Appearance Model Profile (CAMP) Architecture</span></span>](#color-appearance-model-profile-architecture)

[<span data-ttu-id="4863d-121">El esquema de campamento</span><span class="sxs-lookup"><span data-stu-id="4863d-121">The CAMP Schema</span></span>](#the-camp-schema)

[<span data-ttu-id="4863d-122">Elementos del esquema CAMP</span><span class="sxs-lookup"><span data-stu-id="4863d-122">The CAMP Schema Elements</span></span>](#the-camp-schema-elements)

[<span data-ttu-id="4863d-123">El algoritmo CAMP</span><span class="sxs-lookup"><span data-stu-id="4863d-123">The CAMP Algorithm</span></span>](#the-camp-algorithm)

### <a name="overview"></a><span data-ttu-id="4863d-124">Información general</span><span class="sxs-lookup"><span data-stu-id="4863d-124">Overview</span></span>

<span data-ttu-id="4863d-125">Este esquema se usa para especificar el contenido de un perfil de modelo de apariencia de color (CAMP).</span><span class="sxs-lookup"><span data-stu-id="4863d-125">This schema is used to specify the content of a color appearance model profile (CAMP).</span></span> <span data-ttu-id="4863d-126">Los algoritmos de línea de base asociados se describen en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="4863d-126">The associated baseline algorithms are described in the following sections.</span></span>

<span data-ttu-id="4863d-127">El campamento se compone de etiquetas XML que proporcionan valores paramétricos a las variables del modelo de apariencia de color de línea base CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="4863d-127">The CAMP is composed of XML tags that provide parametric values to the CIECAM02 baseline color appearance model variables.</span></span> <span data-ttu-id="4863d-128">Se proporcionan detalles sobre los intervalos para los parámetros en la especificación del modelo de apariencia de color de línea de base y la recomendación de CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="4863d-128">Details on the ranges for parameters are provided in the baseline color appearance model specification and CIECAM02 recommendation.</span></span>

### <a name="color-appearance-model-profile-architecture"></a><span data-ttu-id="4863d-129">Arquitectura de Perfil de modelo de apariencia de color</span><span class="sxs-lookup"><span data-stu-id="4863d-129">Color Appearance Model Profile Architecture</span></span>

![Diagrama que muestra la arquitectura de Perfil de campamento hecha de etiquetas X M L.](images/camp-image002new.png)

### <a name="the-camp-schema"></a><span data-ttu-id="4863d-131">El esquema de campamento</span><span class="sxs-lookup"><span data-stu-id="4863d-131">The CAMP Schema</span></span>


```C++
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema
  xmlns:cam="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Appearance Model profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:annotation>
    <xs:documentation>
      ColorAppearanceModel element contains viewing conditions
      parameters based on CIECAM02.
    </xs:documentation>
  </xs:annotation>
  <xs:element name="ColorAppearanceModel">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ProfileName" type="wcs:MultiLocalizedTextType"/>
        <xs:element name="Description" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="Author" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="ViewingConditions">
          <xs:complexType>
            <xs:sequence>
              <xs:choice>
                <xs:element name="WhitePoint" type="wcs:NonNegativeCIEXYZType"/>
                <xs:element name="WhitePointName">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="D50"/>
                      <xs:enumeration value="D65"/>
                      <xs:enumeration value="A"/>
                      <xs:enumeration value="F2"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:element>
              </xs:choice>
              <xs:element name="Background" type="wcs:NonNegativeCIEXYZType"/>
              <xs:choice>
                <xs:element name="ImpactOfSurround" type="xs:float"/>
                <xs:element name="Surround">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="Average"/>
                      <xs:enumeration value="Dim"/>
                      <xs:enumeration value="Dark"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:element>
              </xs:choice>
              <xs:element name="LuminanceOfAdaptingField" type="xs:float"/>
              <xs:element name="DegreeOfAdaptation" type="xs:float"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
        <xs:element name="NormalizeToMediaWhitePoint" minOccurs="0">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="True"/>
              <xs:enumeration value="False"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:element>
      </xs:sequence>
      <xs:attribute name="ID" type="xs:string" use="optional" />
    </xs:complexType>
  </xs:element>
</xs:schema>
```



## <a name="the-camp-schema-elements"></a><span data-ttu-id="4863d-132">Elementos del esquema CAMP</span><span class="sxs-lookup"><span data-stu-id="4863d-132">The CAMP Schema Elements</span></span>

## <a name="colorappearancemodel"></a><span data-ttu-id="4863d-133">ColorAppearanceModel</span><span class="sxs-lookup"><span data-stu-id="4863d-133">ColorAppearanceModel</span></span>

<span data-ttu-id="4863d-134">Este elemento es una secuencia de:</span><span class="sxs-lookup"><span data-stu-id="4863d-134">This element is a sequence of:</span></span>

1.  <span data-ttu-id="4863d-135">Cadena de perfilename,</span><span class="sxs-lookup"><span data-stu-id="4863d-135">ProfileName string,</span></span>
2.  <span data-ttu-id="4863d-136">cadena de descripción opcional,</span><span class="sxs-lookup"><span data-stu-id="4863d-136">optional Description string,</span></span>
3.  <span data-ttu-id="4863d-137">cadena de autor opcional,</span><span class="sxs-lookup"><span data-stu-id="4863d-137">optional Author string,</span></span>
4.  <span data-ttu-id="4863d-138">Elemento ViewingConditions.</span><span class="sxs-lookup"><span data-stu-id="4863d-138">ViewingConditions element.</span></span>

<span data-ttu-id="4863d-139">**Condiciones de validación:** Cada subelemento se valida por su propio tipo.</span><span class="sxs-lookup"><span data-stu-id="4863d-139">**Validation conditions:** Each sub-element is validated by its own type.</span></span> <span data-ttu-id="4863d-140">Las longitudes de cadena se limitan a 10.000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="4863d-140">String lengths are limited to 10,000 characters.</span></span>

## <a name="namespace"></a><span data-ttu-id="4863d-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4863d-141">Namespace</span></span>

<span data-ttu-id="4863d-142">xmlns: Cam = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "</span><span class="sxs-lookup"><span data-stu-id="4863d-142">xmlns:cam="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"</span></span>

<span data-ttu-id="4863d-143">targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "</span><span class="sxs-lookup"><span data-stu-id="4863d-143">targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"</span></span>

## <a name="version"></a><span data-ttu-id="4863d-144">Versión</span><span class="sxs-lookup"><span data-stu-id="4863d-144">Version</span></span>

<span data-ttu-id="4863d-145">Versión &gt; 0,1 o &lt; = "1,0" con la primera versión de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4863d-145">Version &gt;0.1 or &lt;= "1.0" with the first release of Windows Vista.</span></span>

<span data-ttu-id="4863d-146">**Condiciones de validación:** Cualquier valor de versión &lt; = 2,0 también es válido para admitir cambios no importantes en el formato.</span><span class="sxs-lookup"><span data-stu-id="4863d-146">**Validation conditions:** Any version value &lt;=2.0 is also valid to support non-breaking changes to the format.</span></span>

## <a name="documentation"></a><span data-ttu-id="4863d-147">Documentación</span><span class="sxs-lookup"><span data-stu-id="4863d-147">Documentation</span></span>

<span data-ttu-id="4863d-148">Esquema de Perfil de modelo de apariencia de color.</span><span class="sxs-lookup"><span data-stu-id="4863d-148">Color Appearance Model Profile Schema.</span></span>

<span data-ttu-id="4863d-149">Copyright (C) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4863d-149">Copyright (C) Microsoft.</span></span> <span data-ttu-id="4863d-150">Todos los derechos reservados.</span><span class="sxs-lookup"><span data-stu-id="4863d-150">All rights reserved.</span></span>

<span data-ttu-id="4863d-151">**Condiciones de validación:** Cada subelemento se valida por su propio tipo.</span><span class="sxs-lookup"><span data-stu-id="4863d-151">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

## <a name="surroundtype"></a><span data-ttu-id="4863d-152">SurroundType</span><span class="sxs-lookup"><span data-stu-id="4863d-152">SurroundType</span></span>

<span data-ttu-id="4863d-153">Este elemento es una enumeración de los parámetros "Average", "DIM" o "Dark" CIECAM02, o bien los parámetros cuantitativos reales de la recomendación c de CIECAM02, que afecta al envolvente.</span><span class="sxs-lookup"><span data-stu-id="4863d-153">This element is a either an enumeration of "Average," "Dim," or "Dark" CIECAM02 parameters or the actual quantitative parameters from the CIECAM02 recommendation c, impact of the surround.</span></span>

<span data-ttu-id="4863d-154">**Condiciones de validación:** El parámetro c puede oscilar entre 0,525 y 0,69.</span><span class="sxs-lookup"><span data-stu-id="4863d-154">**Validation conditions:** The c parameter can range from 0.525 to 0.69.</span></span>

## <a name="viewingconditions"></a><span data-ttu-id="4863d-155">ViewingConditions</span><span class="sxs-lookup"><span data-stu-id="4863d-155">ViewingConditions</span></span>

<span data-ttu-id="4863d-156">Este elemento se compone de los siguientes subelementos:</span><span class="sxs-lookup"><span data-stu-id="4863d-156">This element consists of the following sub-elements:</span></span>



| <span data-ttu-id="4863d-157">Elemento</span><span class="sxs-lookup"><span data-stu-id="4863d-157">Element</span></span>                    | <span data-ttu-id="4863d-158">Tipo</span><span class="sxs-lookup"><span data-stu-id="4863d-158">Type</span></span>           |
|----------------------------|----------------|
| <span data-ttu-id="4863d-159">WhitePoint</span><span class="sxs-lookup"><span data-stu-id="4863d-159">WhitePoint</span></span>                 | <span data-ttu-id="4863d-160">WhitePointType</span><span class="sxs-lookup"><span data-stu-id="4863d-160">WhitePointType</span></span> |
| <span data-ttu-id="4863d-161">Información previa</span><span class="sxs-lookup"><span data-stu-id="4863d-161">Background</span></span>                 | <span data-ttu-id="4863d-162">CIEXYZ</span><span class="sxs-lookup"><span data-stu-id="4863d-162">CIEXYZ</span></span>         |
| <span data-ttu-id="4863d-163">Coloca</span><span class="sxs-lookup"><span data-stu-id="4863d-163">Surround</span></span>                   | <span data-ttu-id="4863d-164">SurroundType</span><span class="sxs-lookup"><span data-stu-id="4863d-164">SurroundType</span></span>   |
| <span data-ttu-id="4863d-165">LuminanceOfAdaptingField</span><span class="sxs-lookup"><span data-stu-id="4863d-165">LuminanceOfAdaptingField</span></span>   | <span data-ttu-id="4863d-166">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4863d-166">float</span></span>          |
| <span data-ttu-id="4863d-167">DegreeOfAdaptation</span><span class="sxs-lookup"><span data-stu-id="4863d-167">DegreeOfAdaptation</span></span>         | <span data-ttu-id="4863d-168">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4863d-168">float</span></span>          |
| <span data-ttu-id="4863d-169">NormalizeToMediaWhitePoint</span><span class="sxs-lookup"><span data-stu-id="4863d-169">NormalizeToMediaWhitePoint</span></span> | <span data-ttu-id="4863d-170">Boolean</span><span class="sxs-lookup"><span data-stu-id="4863d-170">Boolean</span></span>        |



 

<span data-ttu-id="4863d-171">**Condiciones de validación:** NonNegativeXYZType valida los subelementos CIEXYZ.</span><span class="sxs-lookup"><span data-stu-id="4863d-171">**Validation conditions:** CIEXYZ sub-elements are validated by NonNegativeXYZType.</span></span> <span data-ttu-id="4863d-172">El valor de LuminanceOfAdaptingField es un máximo de 10, 000cd/m ^ 2.</span><span class="sxs-lookup"><span data-stu-id="4863d-172">The LuminanceOfAdaptingField is a maximum of 10,000cd/m^2.</span></span> <span data-ttu-id="4863d-173">DegreeOfAdaptation puede oscilar entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="4863d-173">The DegreeOfAdaptation can range from 0.0 to 1.0.</span></span> <span data-ttu-id="4863d-174">El valor de NormalizeToMediaWhitePoint puede ser "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="4863d-174">The NormalizeToMediaWhitePoint value can be either "true" or "false."</span></span> <span data-ttu-id="4863d-175">Si el subelemento NormalizeToMediaWhitePoint está ausente, el valor predeterminado es "true".</span><span class="sxs-lookup"><span data-stu-id="4863d-175">If the NormalizeToMediaWhitePoint sub-element is absent, it effectively defaults to "true."</span></span> <span data-ttu-id="4863d-176">Consulte la siguiente sección del algoritmo CAMP.</span><span class="sxs-lookup"><span data-stu-id="4863d-176">See the following CAMP algorithm section.</span></span>

## <a name="whitepointtype"></a><span data-ttu-id="4863d-177">WhitePointType</span><span class="sxs-lookup"><span data-stu-id="4863d-177">WhitePointType</span></span>

<span data-ttu-id="4863d-178">Este elemento es una enumeración de valores de origen de luz CIE ("D50", "D65", "A" o "F2") o un subelemento CIEXYZ.</span><span class="sxs-lookup"><span data-stu-id="4863d-178">This element is a either an enumeration of CIE light source value ("D50," "D65," "A," or "F2") or a CIEXYZ sub-element.</span></span>

<span data-ttu-id="4863d-179">**Condiciones de validación:** Cada subelemento se valida por su propio tipo.</span><span class="sxs-lookup"><span data-stu-id="4863d-179">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

## <a name="ciexyztype"></a><span data-ttu-id="4863d-180">CIEXYZType</span><span class="sxs-lookup"><span data-stu-id="4863d-180">CIEXYZType</span></span>

<span data-ttu-id="4863d-181">El elemento CIEXYZType se compone de tres elementos NonNegativeFloatType de punto flotante IEEE de precisión sencilla, denominados "X", "Y" y "Z".</span><span class="sxs-lookup"><span data-stu-id="4863d-181">The CIEXYZType element is composed of three NonNegativeFloatType single-precision IEEE floating-point elements, named "X," "Y," and "Z."</span></span> <span data-ttu-id="4863d-182">Estas medidas pueden ser absolutas (no relativas) CIEXYZ 1931 valores reflectantes o valores absolutos (no relativos) CIEXYZ 1931 Direct (transpermisivo) en candelas por unidades cuadradas.</span><span class="sxs-lookup"><span data-stu-id="4863d-182">These measurements can be either absolute (not relative) CIEXYZ 1931 reflective values or absolute (not relative) CIEXYZ 1931 direct (transmissive) values in candelas per meter squared units.</span></span>

<span data-ttu-id="4863d-183">**Condiciones de validación:** Esto significa que solo son válidos los valores del mundo real y los valores de medida CIEXYZ negativos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="4863d-183">**Validation conditions:** This means that only real-world values are valid, and negative CIEXYZ measurement values are invalid.</span></span> <span data-ttu-id="4863d-184">Dado que se trata de valores absolutos, los valores pueden oscilar más allá de 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="4863d-184">Since these are absolute values, values can range well beyond 1.0f.</span></span> <span data-ttu-id="4863d-185">Un límite razonable para cualquier valor X, Y o Z se establecerá arbitrariamente en 10000.0 f.</span><span class="sxs-lookup"><span data-stu-id="4863d-185">A reasonable limit for any X, Y, or Z value will be arbitrarily set to 10000.0f.</span></span>

 

### <a name="the-camp-algorithm"></a><span data-ttu-id="4863d-186">El algoritmo CAMP</span><span class="sxs-lookup"><span data-stu-id="4863d-186">The CAMP Algorithm</span></span>

<span data-ttu-id="4863d-187">El modelo de apariencia de color (CAM) se basa en las ecuaciones del modelo de apariencia de color CIE CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="4863d-187">The color appearance model (CAM) is based on the CIE CIECAM02 color appearance model equations.</span></span>

<span data-ttu-id="4863d-188">Esta clase implementa el modelado de apariencia de color.</span><span class="sxs-lookup"><span data-stu-id="4863d-188">This class implements the color appearance modeling.</span></span> <span data-ttu-id="4863d-189">Tenga en cuenta que la leva WCS *no* es reemplazable, por ejemplo, mediante un complemento.</span><span class="sxs-lookup"><span data-stu-id="4863d-189">Note that the WCS CAM is *not* replaceable, for example, using a plug-in.</span></span> <span data-ttu-id="4863d-190">Es un objetivo de diseño tener solo un modelo de apariencia de color.</span><span class="sxs-lookup"><span data-stu-id="4863d-190">It is a design goal to have only one color appearance model.</span></span> <span data-ttu-id="4863d-191">El CAM se basa en las recomendaciones de CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="4863d-191">The CAM is based on CIECAM02 recommendations.</span></span>

<span data-ttu-id="4863d-192">CIECAM02 se puede usar de dos maneras.</span><span class="sxs-lookup"><span data-stu-id="4863d-192">CIECAM02 can be used in two ways.</span></span> <span data-ttu-id="4863d-193">En la dirección de colorimétrico-a-Appearance, proporciona una asignación desde el espacio XYZ de CIE al espacio de apariencia del color.</span><span class="sxs-lookup"><span data-stu-id="4863d-193">In the colorimetric-to-appearance direction, it provides a mapping from CIE XYZ space to color appearance space.</span></span> <span data-ttu-id="4863d-194">En la dirección de la apariencia a la colorimétrico, se asigna desde el espacio de apariencia del color al espacio XYZ.</span><span class="sxs-lookup"><span data-stu-id="4863d-194">In the appearance-to-colorimetric direction, it maps from color appearance space back to XYZ space.</span></span> <span data-ttu-id="4863d-195">La apariencia del color correlaciona la luminosidad, J, croma, C y matiz, h.</span><span class="sxs-lookup"><span data-stu-id="4863d-195">The color appearance correlates lightness, J, chroma, C, and hue, h.</span></span> <span data-ttu-id="4863d-196">Estos tres valores forman un sistema de coordenadas cilíndrico.</span><span class="sxs-lookup"><span data-stu-id="4863d-196">These three values form a cylindrical coordinate system.</span></span> <span data-ttu-id="4863d-197">A menudo, resulta más cómodo trabajar en un sistema de coordenadas rectangular, por lo que Compute a = C cos h y b = C sin h, para proporcionar CIECAM02 jab.</span><span class="sxs-lookup"><span data-stu-id="4863d-197">Frequently, it turns out to be more convenient to work in a rectangular coordinate system, so compute a = C cos h and b = C sin h, to give CIECAM02 Jab.</span></span>

<span data-ttu-id="4863d-198">Puede usar valores de luminosidad de CAM mayores que 100.</span><span class="sxs-lookup"><span data-stu-id="4863d-198">You can use CAM lightness values greater than 100.</span></span> <span data-ttu-id="4863d-199">El Comité CIE que formulaba CIECAM02 no abordaba el comportamiento del eje de luminosidad para los valores de entrada con una luminancia mayor que el punto blanco adoptado; es decir, para los valores Y de entrada mayores que el valor Y del punto blanco adoptado.</span><span class="sxs-lookup"><span data-stu-id="4863d-199">The CIE committee that formulated CIECAM02 did not address the behavior of the lightness axis for input values with a luminance greater than the adopted white point; that is, for input Y values greater than the adopted white point Y value.</span></span> <span data-ttu-id="4863d-200">La experimentación ha demostrado que las ecuaciones de luminancia de CIECAM02 se comportan razonablemente para estos valores.</span><span class="sxs-lookup"><span data-stu-id="4863d-200">Experimentation has shown that the luminance equations in CIECAM02 behave reasonably for such values.</span></span> <span data-ttu-id="4863d-201">La luminosidad aumenta exponencialmente y sigue el mismo exponente (aproximadamente 1/3).</span><span class="sxs-lookup"><span data-stu-id="4863d-201">The lightness increases exponentially and follows the same exponent (roughly 1/3).</span></span>

<span data-ttu-id="4863d-202">A veces, los usuarios quieren cambiar la manera en que se calcula el grado de adaptación (D).</span><span class="sxs-lookup"><span data-stu-id="4863d-202">Users sometimes want to change the way that the degree of adaptation (D) is calculated.</span></span> <span data-ttu-id="4863d-203">El diseño WCS permite a los usuarios controlar este cálculo cambiando el valor de degreeOfadaptation en los parámetros de condiciones de visualización.</span><span class="sxs-lookup"><span data-stu-id="4863d-203">The WCS design enables users to control this calculation by changing the degreeOfadaptation value in the viewing conditions parameters.</span></span>

<span data-ttu-id="4863d-204">Para proporcionar una coincidencia más coherente con las expectativas de los usuarios con influencia de ICC, el valor de degreeOfAdaptation en los valores predeterminados es 1,0.</span><span class="sxs-lookup"><span data-stu-id="4863d-204">To provide a more consistent match to users' ICC-influenced expectations, the degreeOfAdaptation in the default CAMPS is 1.0.</span></span> <span data-ttu-id="4863d-205">Esto da lugar a resultados mejores en todos los casos distintos de la macropicada, donde podría querer permitir que WCS compute el degreeOfAdaptation (a través de degreeOfAdaptation =-1).</span><span class="sxs-lookup"><span data-stu-id="4863d-205">This produces better results in all cases other than MinCD Absolute, where one might want to let WCS compute the degreeOfAdaptation (via degreeOfAdaptation = -1).</span></span>

<span data-ttu-id="4863d-206">En lugar de usar un valor envolvente "Average", "DIM" y "Dark", se proporciona un valor envolvente continuo, calculado a partir del valor c.</span><span class="sxs-lookup"><span data-stu-id="4863d-206">Instead of using a surround value of "Average," "Dim," and "Dark," a continuous surround value, computed from the value c, is provided.</span></span> <span data-ttu-id="4863d-207">El valor de c debe ser un valor Float entre 0,525 y 0,69.</span><span class="sxs-lookup"><span data-stu-id="4863d-207">The value of c must be a float between 0.525 and 0.69.</span></span>

<span data-ttu-id="4863d-208">Desde *c*, se puede calcular *NC* y *F* mediante la interpolación lineal a trozos entre los valores ya proporcionados para "Average", "DIM" y "Dark".</span><span class="sxs-lookup"><span data-stu-id="4863d-208">From *c*, *Nc* and *F* can be computed, using piecewise linear interpolation between the values already provided for "Average," "Dim," and "Dark."</span></span> <span data-ttu-id="4863d-209">Esto modela lo que se muestra en la figura 1 de CIE 159:2004, la especificación CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="4863d-209">This models what is shown in Figure 1 of CIE 159:2004, the CIECAM02 specification.</span></span>



| <span data-ttu-id="4863d-210">degreeOfAdaption</span><span class="sxs-lookup"><span data-stu-id="4863d-210">degreeOfAdaption</span></span>                     | <span data-ttu-id="4863d-211">Comportamiento</span><span class="sxs-lookup"><span data-stu-id="4863d-211">Behavior</span></span>                                                                       |
|--------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="4863d-212">-1.0</span><span class="sxs-lookup"><span data-stu-id="4863d-212">-1.0</span></span>                                 | ![Muestra una fórmula para el comportamiento predeterminado de C I E A M 02.](images/camp-image006.png)<span data-ttu-id="4863d-214">Este es el comportamiento predeterminado de CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="4863d-214">This is the default CIECAM02 behavior.</span></span><br/> |
| <span data-ttu-id="4863d-215">0,0 &lt; = degreeOfAdaption &lt; = 1,0</span><span class="sxs-lookup"><span data-stu-id="4863d-215">0.0 &lt;= degreeOfAdaption &lt;= 1.0</span></span> | <span data-ttu-id="4863d-216">*D* = degreeOfAdaptation (el valor proporcionado por el usuario)</span><span class="sxs-lookup"><span data-stu-id="4863d-216">*D* = degreeOfAdaptation (the value supplied by the user)</span></span>                      |



 

<span data-ttu-id="4863d-217">También se ha agregado una determinada cantidad de comprobaciones de errores a la implementación de.</span><span class="sxs-lookup"><span data-stu-id="4863d-217">A certain amount of error checking has also been added to the implementation.</span></span> <span data-ttu-id="4863d-218">Los siguientes números de ecuaciones son los que se usan en la definición de CIE 159:2004 de CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="4863d-218">The following equation numbers are those used in the CIE 159:2004 definition of CIECAM02.</span></span>

<span data-ttu-id="4863d-219">**ColorimetricToAppearanceColors**</span><span class="sxs-lookup"><span data-stu-id="4863d-219">**ColorimetricToAppearanceColors**</span></span>

<span data-ttu-id="4863d-220">Se comprueba si los valores de entrada son razonables: si X o Z &lt; 0,0, o si y &lt; -1,0, el valor HRESULT es E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="4863d-220">The input values are checked for reasonableness: If X or Z &lt; 0.0, or if Y &lt; -1.0, then the HRESULT is E\_INVALIDARG.</span></span> <span data-ttu-id="4863d-221">Si-1,0 &lt; = Y &lt; 0,0, entonces J, C y h se establecen en 0,0.</span><span class="sxs-lookup"><span data-stu-id="4863d-221">If -1.0 &lt;= Y &lt; 0.0, then J, C, and h are all set to 0.0.</span></span>

<span data-ttu-id="4863d-222">Existen ciertas condiciones internas que pueden generar resultados de error.</span><span class="sxs-lookup"><span data-stu-id="4863d-222">There are certain internal conditions that can produce error results.</span></span> <span data-ttu-id="4863d-223">En lugar de generar estos resultados, los resultados internos se recortan para generar valores en el intervalo.</span><span class="sxs-lookup"><span data-stu-id="4863d-223">Instead of producing such results, the internal results are clipped to produce in-range values.</span></span> <span data-ttu-id="4863d-224">Esto sucede con las especificaciones de los colores que serían oscuros y, de hecho, de color cromático: en la ecuación 7,23, si el &lt; valor es 0, a = 0.</span><span class="sxs-lookup"><span data-stu-id="4863d-224">This happens for specifications of colors that would be dark and impossibly chromatic: In equation 7.23, if A &lt; 0, A = 0.</span></span> <span data-ttu-id="4863d-225">En la ecuación 7,26, si t &lt; 0, t = 0.</span><span class="sxs-lookup"><span data-stu-id="4863d-225">In equation 7.26, if t &lt; 0, t = 0.</span></span>

<span data-ttu-id="4863d-226">**AppearanceToColorimetricColors**</span><span class="sxs-lookup"><span data-stu-id="4863d-226">**AppearanceToColorimetricColors**</span></span>

<span data-ttu-id="4863d-227">Se comprueba si los valores de entrada son razonables.</span><span class="sxs-lookup"><span data-stu-id="4863d-227">The input values are checked for reasonableness.</span></span> <span data-ttu-id="4863d-228">Si C &lt; 0, c &gt; 300 o J &gt; 500, el valor HRESULT es E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="4863d-228">If C &lt; 0 , C &gt; 300, or J &gt; 500, then the HRESULT is E\_INVALIDARG.</span></span>

<span data-ttu-id="4863d-229">*R '<sub>a;</sub>*, *G '<sub>a;</sub>* y *B '<sub>a;</sub>*, (las ecuaciones 8,19-8,21) se recortan al rango 399,9.</span><span class="sxs-lookup"><span data-stu-id="4863d-229">*R'<sub>a;</sub>*, *G'<sub>a;</sub>*, and *B'<sub>a;</sub>*, (equations 8.19 - 8.21) are clipped to the range   399.9 .</span></span>

<span data-ttu-id="4863d-230">En todos los perfiles de modelo de apariencia de color (los), el motor WCS examinará el punto blanco adoptado.</span><span class="sxs-lookup"><span data-stu-id="4863d-230">For all Color Appearance Model Profiles (CAMPs), the WCS engine will examine the adopted white point.</span></span> <span data-ttu-id="4863d-231">Si Y no es 100,0, se escalará el punto blanco adoptado para que Y sea igual a 100,0.</span><span class="sxs-lookup"><span data-stu-id="4863d-231">If Y is not 100.0, then the adopted white point will be scaled so that Y does equal 100.0.</span></span> <span data-ttu-id="4863d-232">Se aplicará el mismo ajuste de escala al valor de fondo.</span><span class="sxs-lookup"><span data-stu-id="4863d-232">The same scaling will be applied to the background value.</span></span> <span data-ttu-id="4863d-233">El factor de escala es 100,0/adoptedWhitePoint. Y.</span><span class="sxs-lookup"><span data-stu-id="4863d-233">The scaling factor is 100.0/adoptedWhitePoint.Y.</span></span> <span data-ttu-id="4863d-234">Se aplica el mismo factor de escala a cada uno de los valores X, Y y Z. Si el campo NormalizeToMediaWhitePoint se establece en "true", o si no está presente en el campamento, el motor también escala todos los colores del dispositivo de entrada a DeviceToColorimetric para que el valor Y del punto blanco del medio del dispositivo sea igual a 100,0.</span><span class="sxs-lookup"><span data-stu-id="4863d-234">The same scaling factor is applied to each of X, Y, and Z. If the NormalizeToMediaWhitePoint field is set to "True," or if it is absent from the CAMP, the engine also scales all device colors input to DeviceToColorimetric so that the Y value of the device media white point equals 100.0.</span></span> <span data-ttu-id="4863d-235">Los colores del dispositivo procedentes de ColorimetricToDevice se escalarán por el inverso multiplicativo de ese factor de escala.</span><span class="sxs-lookup"><span data-stu-id="4863d-235">Device colors coming from ColorimetricToDevice will be scaled by the multiplicative inverse of that scaling factor.</span></span> <span data-ttu-id="4863d-236">Si la marca NormalizeToMediaWhitePoint se establece en "false", los datos de la colorimétrico no se escalan.</span><span class="sxs-lookup"><span data-stu-id="4863d-236">If the NormalizeToMediaWhitePoint flag is set to "False," then the colorimetric data is not scaled.</span></span>

<span data-ttu-id="4863d-237">En algunas tareas, tiene sentido escalar los valores de colorimétrica procedentes de DeviceToColorimetric.</span><span class="sxs-lookup"><span data-stu-id="4863d-237">For some tasks, it makes sense to scale the colorimetric values coming from DeviceToColorimetric.</span></span> <span data-ttu-id="4863d-238">Las ecuaciones de luminosidad hiperbólica del CAM están diseñadas realmente para una luminancia de punto blanco de 100,0.</span><span class="sxs-lookup"><span data-stu-id="4863d-238">The hyperbolic lightness equations in the CAM are really designed for a white point luminance of 100.0.</span></span> <span data-ttu-id="4863d-239">El único lugar donde entra en juego una diferencia en la luminancia absoluta (o luminancia) es la luminancia del campo de adaptación.</span><span class="sxs-lookup"><span data-stu-id="4863d-239">The only place where a difference in the absolute luminance (or illuminance) comes into play is in the luminance of the adapting field.</span></span> <span data-ttu-id="4863d-240">Por lo tanto, el CAM debe inicializarse con un punto blanco Y de 100,0.</span><span class="sxs-lookup"><span data-stu-id="4863d-240">So the CAM must be initialized with a white point Y of 100.0.</span></span> <span data-ttu-id="4863d-241">Sin embargo, si se usa el punto blanco medio del modelo de dispositivo como el punto blanco adoptado, todos los colores procedentes del dispositivo deben escalarse en consecuencia, o el blanco del dispositivo no obtendrá un valor de J de 100,0.</span><span class="sxs-lookup"><span data-stu-id="4863d-241">But if the device model's medium white point is being used as the adopted white point, then all colors coming from the device must be scaled accordingly, or device white will not come out with a J value of 100.0.</span></span> <span data-ttu-id="4863d-242">Por lo tanto, los valores Y deben escalarse en las medidas.</span><span class="sxs-lookup"><span data-stu-id="4863d-242">So the Y values have to be scaled in the measurements.</span></span> <span data-ttu-id="4863d-243">Los valores de medida se pueden escalar antes de inicializar el modelo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4863d-243">The measurement values could be scaled before initializing the device model.</span></span> <span data-ttu-id="4863d-244">Los resultados ya estarán en el intervalo adecuado.</span><span class="sxs-lookup"><span data-stu-id="4863d-244">Then results would already be in the proper range.</span></span> <span data-ttu-id="4863d-245">Pero eso haría más difícil probar el modelo de dispositivo, ya que los valores que se exponen serían necesarios para el escalado.</span><span class="sxs-lookup"><span data-stu-id="4863d-245">But that would make testing the device model more difficult, because the values coming out would require scaling.</span></span> <span data-ttu-id="4863d-246">En el caso de las tareas en las que se percibe que el punto blanco medio del dispositivo es un blanco verdadero, es deseable normalizar el punto blanco del medio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4863d-246">For tasks in which the device medium white point is perceived to be a true white, normalizing by the device media white point is desirable.</span></span>

<span data-ttu-id="4863d-247">El CAM se inicializa directamente desde el campamento.</span><span class="sxs-lookup"><span data-stu-id="4863d-247">The CAM is initialized directly from the CAMP.</span></span> <span data-ttu-id="4863d-248">Esto permite a los desarrolladores cierta flexibilidad a la hora de inicializar el CAM, en función de la tarea que desea realizar.</span><span class="sxs-lookup"><span data-stu-id="4863d-248">This allows developers some flexibility in initializing the CAM, based upon the task they want to perform.</span></span> <span data-ttu-id="4863d-249">En algunas tareas, los observadores omitirán cualquier intensidad de croma en los puntos blancos multimedia, ya que "saben" que los medios de origen y de destino están en blanco.</span><span class="sxs-lookup"><span data-stu-id="4863d-249">In some tasks, observers will ignore any chroma in the media white points, because they cognitively "know" that the source and destination media are "white."</span></span> <span data-ttu-id="4863d-250">En tales casos, los desarrolladores querrán inicializar las levas hacia delante e inversas con sus respectivos puntos blancos multimedia.</span><span class="sxs-lookup"><span data-stu-id="4863d-250">In such cases, developers will want to initialize the forward and inverse CAMs with their respective media white points.</span></span> <span data-ttu-id="4863d-251">En algunos casos, los observadores pueden estar comparando el color de los elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="4863d-251">In some cases, observers may be comparing the color of the media backgrounds.</span></span> <span data-ttu-id="4863d-252">En estos casos, es aconsejable usar un CAM para ambos dispositivos y puede ser deseable no escalar los valores colorimétrica de cada dispositivo por el punto blanco medio de ese dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4863d-252">In these cases, it is advisable to use one CAM for both devices, and it may be desirable not to scale each device's colorimetric values by that device's medium white point.</span></span> <span data-ttu-id="4863d-253">Después, los diferentes valores de los triestímulos del medio darán lugar a diferentes valores de apariencia en CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="4863d-253">Then the different tristimulus values of the media will lead to different appearance values in CIECAM02.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4863d-254">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4863d-254">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4863d-255">Conceptos básicos de la administración del color</span><span class="sxs-lookup"><span data-stu-id="4863d-255">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="4863d-256">Algoritmos y esquemas del Sistema de colores de Windows</span><span class="sxs-lookup"><span data-stu-id="4863d-256">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





