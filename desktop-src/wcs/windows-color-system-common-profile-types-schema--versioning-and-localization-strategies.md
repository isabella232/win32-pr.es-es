---
title: Esquema, versiones y estrategias de localización de tipos de perfiles comunes del Sistema de colores de Windows
description: Esquema, versiones y estrategias de localización de tipos de perfiles comunes del Sistema de colores de Windows
ms.assetid: 295522c6-7c53-47f6-9b98-aeee2b0e34fc
keywords:
- Sistema de color de Windows (WCS), tipos de perfil comunes
- WCS (sistema de colores de Windows), tipos de perfil comunes
- Administración del color de imagen, tipos de perfil comunes
- Administración del color, tipos de perfiles comunes
- colores, tipos de perfiles comunes
- Sistema de color de Windows (WCS), perfiles
- WCS (sistema de colores de Windows), perfiles
- Administración del color de imagen, perfiles
- Administración del color, perfiles
- colores, perfiles
- Sistema de color de Windows (WCS), control de versiones
- WCS (sistema de colores de Windows), control de versiones
- Administración del color de imagen, control de versiones
- Administración del color, control de versiones
- colores, control de versiones
- Sistema de color de Windows (WCS), localización
- WCS (sistema de colores de Windows), localización
- Administración del color de imagen, localización
- Administración del color, localización
- colores, localización
- Tipos de perfil comunes de WCS
- generar perfiles de consumidores
- tipos de perfiles comunes
- esquemas, tipos de perfiles comunes
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814b652b654b6416b42a7a3484950273a93ea96
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105721405"
---
# <a name="windows-color-system-common-profile-types-schema-versioning-and-localization-strategies"></a><span data-ttu-id="6a5f5-127">Esquema, versiones y estrategias de localización de tipos de perfiles comunes del Sistema de colores de Windows</span><span class="sxs-lookup"><span data-stu-id="6a5f5-127">Windows Color System Common Profile Types schema, Versioning and Localization Strategies</span></span>

-   [<span data-ttu-id="6a5f5-128">Esquema de tipos de perfil común de WCS v1</span><span class="sxs-lookup"><span data-stu-id="6a5f5-128">WCS Common Profile Types Schema V1</span></span>](#wcs-common-profile-types-schema-v1)
-   [<span data-ttu-id="6a5f5-129">Adiciones del esquema de tipos de perfiles comunes WCS V2</span><span class="sxs-lookup"><span data-stu-id="6a5f5-129">WCS Common Profile Types Schema V2 Additions</span></span>](#wcs-common-profile-types-schema-v2-additions)
-   [<span data-ttu-id="6a5f5-130">Control de versiones del esquema de perfil WCS</span><span class="sxs-lookup"><span data-stu-id="6a5f5-130">WCS Profile Schema Versioning</span></span>](#wcs-profile-schema-versioning)
-   [<span data-ttu-id="6a5f5-131">Localización de perfiles WCS</span><span class="sxs-lookup"><span data-stu-id="6a5f5-131">WCS Profile Localization</span></span>](#wcs-profile-localization)
    -   [<span data-ttu-id="6a5f5-132">Expresar elementos localizables</span><span class="sxs-lookup"><span data-stu-id="6a5f5-132">Expressing localizable elements</span></span>](#expressing-localizable-elements)
    -   [<span data-ttu-id="6a5f5-133">Compatibilidad con esquemas</span><span class="sxs-lookup"><span data-stu-id="6a5f5-133">Schema Support</span></span>](#schema-support)
    -   [<span data-ttu-id="6a5f5-134">Seleccionar el idioma</span><span class="sxs-lookup"><span data-stu-id="6a5f5-134">Selecting the Language</span></span>](#selecting-the-language)
    -   [<span data-ttu-id="6a5f5-135">Perfiles integrados</span><span class="sxs-lookup"><span data-stu-id="6a5f5-135">Built-in profiles</span></span>](#built-in-profiles)
-   [<span data-ttu-id="6a5f5-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6a5f5-136">Related topics</span></span>](#related-topics)

## <a name="wcs-common-profile-types-schema-v1"></a><span data-ttu-id="6a5f5-137">Esquema de tipos de perfil común de WCS v1</span><span class="sxs-lookup"><span data-stu-id="6a5f5-137">WCS Common Profile Types Schema V1</span></span>

<span data-ttu-id="6a5f5-138">A continuación se proporciona la definición de esquema v 1.0 para los tipos de perfil común WCS.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-138">The following provides the v1.0 schema definition for the WCS Common Profile Types.</span></span>


```XML
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:import namespace="http://www.w3.org/XML/1998/namespace" />

  <xs:annotation>
    <xs:documentation xml:lang="en">
      Common types used in WCS profile schemas.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:simpleType name="NonNegativeFloatType">
    <xs:restriction base="xs:float">
      <xs:minInclusive value="0"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="NonNegativeCIEXYZType">
    <xs:attribute name="X" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Y" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Z" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:simpleType name="GUIDType">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="LocalizedTextType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute ref="xml:lang" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="MultiLocalizedTextType">
    <xs:sequence>
      <xs:element name="Text" type="wcs:LocalizedTextType" minOccurs="1" />
    </xs:sequence>
  </xs:complexType>

</xs:schema>

```



<span data-ttu-id="6a5f5-139">Solo se admiten las codificaciones UTF-8 o UTF-16.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-139">Only UTF-8 or UTF-16 encodings are supported.</span></span> <span data-ttu-id="6a5f5-140">Se desaconseja encarecidamente el resto de codificaciones XML para conservar la interoperabilidad óptima.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-140">All other XML encodings are strongly discouraged in order to preserve optimum interoperability.</span></span>

## <a name="wcs-common-profile-types-schema-v2-additions"></a><span data-ttu-id="6a5f5-141">Adiciones del esquema de tipos de perfiles comunes WCS V2</span><span class="sxs-lookup"><span data-stu-id="6a5f5-141">WCS Common Profile Types Schema V2 Additions</span></span>

<span data-ttu-id="6a5f5-142">En Windows 7, el esquema de tipos de perfil común de WCS se ha actualizado para incluir tipos que admitan el [esquema de calibración de WCS](wcs-calibration-schema.md).</span><span class="sxs-lookup"><span data-stu-id="6a5f5-142">In Windows 7, the WCS Common Profile Types schema has been updated to include types to support the [WCS Calibration schema](wcs-calibration-schema.md).</span></span>


```XML
  <xs:complexType name="ParameterizedCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="wcs:ParameterizedCurveType"/>
      <xs:element name="GreenTRC" type="wcs:ParameterizedCurveType"/>
      <xs:element name="BlueTRC" type="wcs:ParameterizedCurveType"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="ParameterizedCurveType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset1" type="xs:float" use="optional"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="optional"/>
    <xs:attribute name="Offset2" type="xs:float " use="optional"/>
    <xs:attribute name="TransitionPoint" type="wcs:NonNegativeFloatType" use="optional"/>
    <xs:attribute name="Offset3" type="xs:float" use="optional"/>
  </xs:complexType>

  <xs:simpleType name="FloatList">
    <xs:list itemType="xs:float"/>
  </xs:simpleType>

  <xs:complexType name="OneDimensionLutType">
    <xs:sequence>
      <xs:element name="Input" type="wcs:FloatList"/>
      <xs:element name="Output" type="wcs:FloatList"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="HDRToneResponseCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="wcs:OneDimensionLutType"/>
      <xs:element name="GreenTRC" type="wcs:OneDimensionLutType"/>
      <xs:element name="BlueTRC" type="wcs:OneDimensionLutType"/>
    </xs:sequence>
    <xs:attribute name="TRCLength" use="required">
      <xs:simpleType>
        <xs:restriction base="xs:int">
          <xs:minInclusive value="2" />
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
```



## <a name="wcs-profile-schema-versioning"></a><span data-ttu-id="6a5f5-143">Control de versiones del esquema de perfil WCS</span><span class="sxs-lookup"><span data-stu-id="6a5f5-143">WCS Profile Schema Versioning</span></span>

<span data-ttu-id="6a5f5-144">En este apéndice, el término "consumidor de perfiles" hace referencia al software WCS o a un componente de software de terceros que utiliza perfiles WCS.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-144">In this Appendix, the term "profile consumer" refers to the WCS software, or to a third-party software component that consumes WCS profiles.</span></span>

<span data-ttu-id="6a5f5-145">Las versiones más recientes de los consumidores de perfiles podrán consumir perfiles WCS escritos de acuerdo con versiones anteriores de los esquemas.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-145">Newer versions of profile consumers will be able to consume WCS profiles written according to older versions of the schemas.</span></span> <span data-ttu-id="6a5f5-146">Para sacar el máximo partido de las características definidas en la versión más reciente de los esquemas, se requerirá normalmente la versión más reciente de un consumidor de perfil.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-146">To take full advantage of features defined in the newest version of the schemas, the newest version of a profile consumer will generally be required.</span></span> <span data-ttu-id="6a5f5-147">Sin embargo, los consumidores de perfiles más antiguos pueden consumir perfiles escritos según las versiones más recientes de los esquemas.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-147">However, older profile consumers can consume profiles written according to newer versions of the schemas.</span></span> <span data-ttu-id="6a5f5-148">El consumidor del perfil puede omitir los elementos y atributos XML que no comprenda.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-148">The profile consumer can ignore XML elements and attributes that it does not understand.</span></span> <span data-ttu-id="6a5f5-149">Los resultados serán correctos, pero el rendimiento o la fidelidad pueden degradarse en comparación con los resultados obtenidos con la versión más reciente del consumidor del perfil.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-149">The results will be correct, but performance or fidelity may degraded as compared to the results achieved with the newest version of the profile consumer.</span></span>

<span data-ttu-id="6a5f5-150">A continuación se indican las instrucciones de control de versiones para los consumidores de perfiles:</span><span class="sxs-lookup"><span data-stu-id="6a5f5-150">The following are versioning guidelines for profile consumers:</span></span>

-   <span data-ttu-id="6a5f5-151">Una versión determinada de un consumidor del perfil debe reconocer todos los elementos y atributos de un espacio de nombres de la versión, o ninguno de ellos.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-151">A given version of a profile consumer must recognize either all of the elements and attributes from a version namespace, or none of them.</span></span>
-   <span data-ttu-id="6a5f5-152">Si un consumidor del perfil encuentra un elemento o atributo de un espacio de nombres que no entiende, debe tratarlo como una condición de error, a menos que el perfil contenga instrucciones explícitas sobre el procesamiento de reserva.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-152">If a profile consumer encounters an element or attribute from a namespace that it does not understand, it must treat this as an error condition, unless the profile contains explicit guidance on fallback processing.</span></span>
-   <span data-ttu-id="6a5f5-153">La [especificación de empaquetado abierto](https://www.microsoft.com/whdc/xps/xpspkg.mspx) define un URI de espacio de nombres adicional, el espacio de nombres de compatibilidad de marcado, que define los elementos y atributos que proporcionan esta guía de procesamiento de reserva.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-153">The [Open Packaging Specification](https://www.microsoft.com/whdc/xps/xpspkg.mspx) defines an additional namespace URI, the markup compatibility namespace, which defines elements and attributes that provide this fallback processing guidance.</span></span>
-   <span data-ttu-id="6a5f5-154">Todas las versiones de todos los consumidores de perfiles deben reconocer y respetar todos los elementos y atributos del espacio de nombres de compatibilidad de marcado.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-154">All versions of all profile consumers must recognize and respect all the elements and attributes in the markup compatibility namespace.</span></span>
-   <span data-ttu-id="6a5f5-155">Los consumidores de perfiles basados en una nueva versión de los esquemas de perfil deben admitir todos los espacios de nombres de versiones definidos previamente.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-155">Profile consumers based on a new version of the profile schemas must support all previously defined version namespaces.</span></span>

<span data-ttu-id="6a5f5-156">En la versión 1.0, WCS reconoce los elementos y atributos de los siguientes espacios de nombres:</span><span class="sxs-lookup"><span data-stu-id="6a5f5-156">In the v1.0 release, WCS recognizes elements and attributes from the following namespaces:</span></span>

-   https://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel
-   https://schemas.microsoft.com/windows/2005/02/color/GamutMapModel
-   https://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
-   https://schemas.microsoft.com/winfx/2005/06/markup-compatibility

<span data-ttu-id="6a5f5-157">A continuación se muestra un ejemplo de compatibilidad de marcado.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-157">The following demonstrates an example of markup compatibility.</span></span>


```XML
<?xml version="1.0" encoding="utf-8" ?>
<ColorAppearanceModel
  xmlns=http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
  xmlns:cam2=http://schemas.microsoft.com/windows/2007/08/color/ColorAppearanceModel
  xmlns:mc=http://schemas.microsoft.com/winfx/2005/02/markup-compatibility
  xs:schemaLocation="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel ColorAppearanceModel.xsd"
  xmlns:xs='http://www.w3.org/2001/XMLSchema-instance'
  mc:Ignorable="cam2">

  <ProfileName>Default profile for ICC viewing conditions</ProfileName>
  <mc:AlternateContent>
    <mc:Choice Requires="cam2">
      <cam2:AudioDescription source="ProfileExplanation.wav"/>
    </mc:Choice>
    <mc:Fallback>
      <Description>Appropriate for a print in a D50 viewing booth</Description>
        </mc:Fallback>
  </mc:AlternateContent>
  <Author>Microsoft</Author>

  <ViewingConditions>
    <WhitePointName>D50</WhitePointName>
    <Background X="19.3" Y="20.0" Z="16.5" />
    <Surround>Average</Surround>
    <LuminanceOfAdaptingField>31.8</LuminanceOfAdaptingField>
    <DegreeOfAdaptation>-1</DegreeOfAdaptation>
    <cam2:Humidity>30%</cam2:Humidity>
  </ViewingConditions>

</ColorAppearanceModel>
```



## <a name="wcs-profile-localization"></a><span data-ttu-id="6a5f5-158">Localización de perfiles WCS</span><span class="sxs-lookup"><span data-stu-id="6a5f5-158">WCS Profile Localization</span></span>

<span data-ttu-id="6a5f5-159">**Requisitos**</span><span class="sxs-lookup"><span data-stu-id="6a5f5-159">**Requirements**</span></span>

<span data-ttu-id="6a5f5-160">Los perfiles WCS contienen ciertos elementos como ProfileName y Description que contienen texto legible.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-160">WCS profiles contain certain elements such as ProfileName and Description which contain human-readable text.</span></span> <span data-ttu-id="6a5f5-161">Este texto es localizable.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-161">This text is localizable.</span></span>

<span data-ttu-id="6a5f5-162">Las siguientes son directrices para el control de versiones de los creadores de perfiles:</span><span class="sxs-lookup"><span data-stu-id="6a5f5-162">The following are versioning guidelines for profile creators:</span></span>

-   <span data-ttu-id="6a5f5-163">En el caso de los perfiles creados por terceros, como los fabricantes de impresoras, el autor del perfil debe incorporar texto descriptivo en varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-163">For profiles created by 3rd parties such as printer manufacturers, the profile author should incorporate descriptive text in multiple languages.</span></span>
-   <span data-ttu-id="6a5f5-164">Los siguientes elementos deben ser localizables:</span><span class="sxs-lookup"><span data-stu-id="6a5f5-164">The following elements should be localizable:</span></span> 

    | <span data-ttu-id="6a5f5-165">Elemento</span><span class="sxs-lookup"><span data-stu-id="6a5f5-165">Element</span></span>     | <span data-ttu-id="6a5f5-166">CDMP</span><span class="sxs-lookup"><span data-stu-id="6a5f5-166">CDMP</span></span> | <span data-ttu-id="6a5f5-167">GMMP</span><span class="sxs-lookup"><span data-stu-id="6a5f5-167">GMMP</span></span> | <span data-ttu-id="6a5f5-168">ACAMPA</span><span class="sxs-lookup"><span data-stu-id="6a5f5-168">CAMP</span></span> |
    |-------------|------|------|------|
    | <span data-ttu-id="6a5f5-169">ProfileName</span><span class="sxs-lookup"><span data-stu-id="6a5f5-169">ProfileName</span></span> | <span data-ttu-id="6a5f5-170">x</span><span class="sxs-lookup"><span data-stu-id="6a5f5-170">x</span></span>    | <span data-ttu-id="6a5f5-171">x</span><span class="sxs-lookup"><span data-stu-id="6a5f5-171">x</span></span>    | <span data-ttu-id="6a5f5-172">x</span><span class="sxs-lookup"><span data-stu-id="6a5f5-172">x</span></span>    |
    | <span data-ttu-id="6a5f5-173">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a5f5-173">Description</span></span> | <span data-ttu-id="6a5f5-174">x</span><span class="sxs-lookup"><span data-stu-id="6a5f5-174">x</span></span>    | <span data-ttu-id="6a5f5-175">x</span><span class="sxs-lookup"><span data-stu-id="6a5f5-175">x</span></span>    | <span data-ttu-id="6a5f5-176">x</span><span class="sxs-lookup"><span data-stu-id="6a5f5-176">x</span></span>    |
    | <span data-ttu-id="6a5f5-177">Autor</span><span class="sxs-lookup"><span data-stu-id="6a5f5-177">Author</span></span>      | <span data-ttu-id="6a5f5-178">x</span><span class="sxs-lookup"><span data-stu-id="6a5f5-178">x</span></span>    | <span data-ttu-id="6a5f5-179">x</span><span class="sxs-lookup"><span data-stu-id="6a5f5-179">x</span></span>    | <span data-ttu-id="6a5f5-180">x</span><span class="sxs-lookup"><span data-stu-id="6a5f5-180">x</span></span>    |

    

     

### <a name="expressing-localizable-elements"></a><span data-ttu-id="6a5f5-181">Expresar elementos localizables</span><span class="sxs-lookup"><span data-stu-id="6a5f5-181">Expressing localizable elements</span></span>

<span data-ttu-id="6a5f5-182">En lugar de contener texto directamente, cada elemento traducible contiene uno o varios subelementos WCS: Text, cada uno de los cuales debe especificar el atributo XML: lang.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-182">Instead of directly containing text, each localizable element contains one or more wcs:Text sub-elements, each of which must specify the xml:lang attribute.</span></span> <span data-ttu-id="6a5f5-183">Tal como se describe en la sección 2,12 de la [especificación XML](http://www.w3.org/TR/REC-xml/) ("identificación de idioma"), el valor del atributo XML: lang debe ser un identificador de idioma IETF RFC 3066 como "en-US", "en" o "FR-fr".</span><span class="sxs-lookup"><span data-stu-id="6a5f5-183">As described in the [XML specification](http://www.w3.org/TR/REC-xml/) Section 2.12 ("Language Identification"), the value of the xml:lang attribute must be an IETF RFC 3066 language identifier such as "en-US", "en", or "fr-FR".</span></span> <span data-ttu-id="6a5f5-184">En los esquemas WCS, el valor del atributo XML: lang no debe ser la cadena vacía "", aunque XML lo permite en el caso general.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-184">In WCS schemas, the value of the xml:lang attribute must not be the empty string "", even though XML allows this in the general case.</span></span> <span data-ttu-id="6a5f5-185">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="6a5f5-185">For example:</span></span>


```XML
<cdm:ColorDeviceModel ... />
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceeModel>
```



<span data-ttu-id="6a5f5-186">No hay dos elementos WCS: Text que puedan tener el mismo atributo XML: lang.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-186">No two wcs:Text elements can have the same xml:lang attribute.</span></span> <span data-ttu-id="6a5f5-187">Cada esquema de perfil WCS debe aplicar esta restricción por separado para cada elemento traducible.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-187">Each WCS profile schema must enforce this constraint separately for each localizable element.</span></span> <span data-ttu-id="6a5f5-188">Solo se admiten las codificaciones UTF-8 y UTF-16.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-188">Only UTF-8 and UTF-16 encodings are supported.</span></span>

### <a name="schema-support"></a><span data-ttu-id="6a5f5-189">Compatibilidad con esquemas</span><span class="sxs-lookup"><span data-stu-id="6a5f5-189">Schema Support</span></span>

<span data-ttu-id="6a5f5-190">El diseño hace uso de los tipos XSD WCS: LocalizedText y WCS: MultiLocalizedType definidos en el esquema de tipo de perfil común de WCS:</span><span class="sxs-lookup"><span data-stu-id="6a5f5-190">The design makes use of the XSD types wcs:LocalizedText and wcs:MultiLocalizedType defined in the WCS Common Profile Type schema:</span></span>


```XML
    <xs:complexType name="LocalizedText">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="xml:lang" type="xs:string" use="required"/>
            <xs:extension/>
        <xs:simpleContent/>
    </xs:complexType/>

    <xs:complexType name="MultiLocalizedType">
        <xs:element name="Text" type="cam:LocalizedText" minOccurs="1"/>
    </xs:complexType>
```



<span data-ttu-id="6a5f5-191">Cada esquema de perfil WCS declara cada elemento traducible para que sea de tipo MultiLocalizedType, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="6a5f5-191">Each WCS profile schema declares each localizable element to be of type MultiLocalizedType, for example:</span></span>


```XML
<xs:schema 
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
    xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
    targetNamespace=
        "http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
    version="1.0">
    <xs:import namespace=
        "http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"/>

    <xs:element name="cdm:Description" type="wcs:MultiLocalizableType" minOccurs="0"/>

    <xs:unique name="uniqueDescriptionLanguage">
      <xs:selector xpath="cdm:ColorDeviceModel/cdm:Description/wcs:Text"/>
      <xs:field xpath="@xml:lang"/>
    </unique>

    ...
</xs:schema>
```



<span data-ttu-id="6a5f5-192">El esquema CDMP aplica la restricción de que cada elemento secundario WCS: text del elemento CDM: Description debe tener un atributo XML: lang único.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-192">The CDMP schema enforces the constraint that each wcs:Text child of the cdm:Description element must have a unique xml:lang attribute.</span></span> <span data-ttu-id="6a5f5-193">Aplica la misma restricción para los demás elementos localizables.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-193">It enforces the same constraint for the other localizable elements.</span></span> <span data-ttu-id="6a5f5-194">Los esquemas de campamento y GMMP hacen lo mismo.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-194">The CAMP and GMMP schemas do the same.</span></span>

### <a name="selecting-the-language"></a><span data-ttu-id="6a5f5-195">Seleccionar el idioma</span><span class="sxs-lookup"><span data-stu-id="6a5f5-195">Selecting the Language</span></span>

<span data-ttu-id="6a5f5-196">Al decidir qué versión de lenguaje de un elemento traducible se va a mostrar, el código de aplicación debe seleccionar la "versión más cercana" al "idioma actual".</span><span class="sxs-lookup"><span data-stu-id="6a5f5-196">When deciding which language version of a localizable element to display, application code should select the "closest version" to the "current language".</span></span> <span data-ttu-id="6a5f5-197">Lo que realmente significa "versión más cercana" y "lenguaje actual" significa que depende de la plataforma; Vea a continuación.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-197">What "closest version" and "current language" actually mean is platform-dependent; see below.</span></span> <span data-ttu-id="6a5f5-198">Si el perfil no contiene una versión de idioma que coincida con el idioma actual, la aplicación debe seleccionar la primera versión del perfil (el primer elemento secundario WCS: text del elemento traducible).</span><span class="sxs-lookup"><span data-stu-id="6a5f5-198">If the profile does not contain a language version that matches the current language, the application should select the first version in the profile (the first wcs:Text child element of the localizable element).</span></span>

<span data-ttu-id="6a5f5-199">En Windows Vista, la selección del idioma se realiza de la siguiente manera: cada subproceso tiene una lista asociada de "idiomas preferidos de la interfaz de usuario", que se puede obtener llamando a [**GetThreadPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages).</span><span class="sxs-lookup"><span data-stu-id="6a5f5-199">On Windows Vista, the language selection is done as follows: Each thread has an associated list of "preferred UI languages", which can be obtained by calling [**GetThreadPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages).</span></span> <span data-ttu-id="6a5f5-200">La lista se devuelve por orden de preferencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-200">The list is returned in order of user preference.</span></span> <span data-ttu-id="6a5f5-201">Por ejemplo, en un sistema configurado para Inglés de EE. UU., la lista devuelta por **GetThreadPreferredUILanguages** es {"en-US", "en"}.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-201">For instance, on a system set up for US English, the list returned by **GetThreadPreferredUILanguages** is { "en-US", "en" }.</span></span> <span data-ttu-id="6a5f5-202">Esto significa: 1) Inglés de EE. UU., si está presente.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-202">This means: 1) US English if present.</span></span> <span data-ttu-id="6a5f5-203">2) en caso contrario, use cualquier variante regional de inglés, como "en-GB" o simplemente "en".</span><span class="sxs-lookup"><span data-stu-id="6a5f5-203">2) Otherwise, use any regional variant of English, such as "en-GB" or just plain "en".</span></span>

<span data-ttu-id="6a5f5-204">Para cada idioma de la lista, en el orden de la lista, el código de la interfaz de usuario busca un elemento WCS: Text cuyo atributo XML: lang sea una coincidencia exacta.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-204">For each language in that list, in list order, the UI code looks for a wcs:Text element whose xml:lang attribute is an exact match.</span></span> <span data-ttu-id="6a5f5-205">Se usa la primera versión coincidente.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-205">The first matching version is used.</span></span> <span data-ttu-id="6a5f5-206">Si ninguna versión coincide, se usa el primer elemento WCS: Text.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-206">If no version matches, the first wcs:Text element is used.</span></span>

### <a name="built-in-profiles"></a><span data-ttu-id="6a5f5-207">Perfiles integrados</span><span class="sxs-lookup"><span data-stu-id="6a5f5-207">Built-in profiles</span></span>

<span data-ttu-id="6a5f5-208">Los perfiles WCS estándar incluidos con Windows Vista, como sRGB. CDMP, tienen las mismas propiedades localizables que otros perfiles.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-208">The standard WCS profiles shipped with Windows Vista, such as sRGB.cdmp, have the same localizable properties as other profiles.</span></span>

<span data-ttu-id="6a5f5-209">La solución estándar de Windows sería colocar las cadenas localizadas en un archivo DLL de MUI y hacer referencia a ellas de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="6a5f5-209">The standard Windows solution would be to put the localized strings in a MUI DLL, and refer to them like this:</span></span>


```XML
<cdm:Description resourceId="mscms.dll,-101">
    <wcs:Text xml:lang="en-US">Hello, world!</wcs:Text>
<cdm:Description>
```



<span data-ttu-id="6a5f5-210">En un sistema Windows, se extrae el texto de Descripción del identificador de recurso 101 en la versión localizada adecuada de los recursos de MUI para mscms.dll.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-210">On a Windows system, the description text would be extracted from resource ID 101 in the appropriate localized version of the MUI resources for mscms.dll.</span></span> <span data-ttu-id="6a5f5-211">Los sistemas que no son de Windows usarían los subelementos WCS: text como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-211">Non-Windows systems would use the wcs:Text sub-elements as described above.</span></span>

<span data-ttu-id="6a5f5-212">Se presenta un atributo de identificador único global opcional en el elemento raíz de cada esquema de perfil WCS.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-212">We introduce an optional, globally unique ID attribute on the root element of each WCS profile schema.</span></span> <span data-ttu-id="6a5f5-213">El perfil estándar wcsRGB. CDMP podría ser similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="6a5f5-213">The standard profile wcsRGB.cdmp might look like this:</span></span>


```XML
<cdm:ColorDeviceModel
    ID=http://schemas.microsoft.com/2005/02/color/profiles/wcsRGB.cdmp
    ... >
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello.</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour.</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceModel>
```



<span data-ttu-id="6a5f5-214">En el caso de los perfiles de color WCS incluidos con Windows, el CPL de color muestra información descriptiva de los recursos, en lugar de los elementos WCS: Text de los perfiles.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-214">For the WCS color profiles shipped with windows, the Color CPL displays descriptive information from the resources, rather than from the wcs:Text elements in the profiles.</span></span> <span data-ttu-id="6a5f5-215">Esto permite que Windows muestre información localizada para estos perfiles en todos los idiomas admitidos, sin necesidad de que los perfiles themlselves contengan información descriptiva en todos los idiomas.</span><span class="sxs-lookup"><span data-stu-id="6a5f5-215">This allows Windows to display localized information for these profiles in all supported languages, without requiring the profiles themlselves to contain descriptive information in all languages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a5f5-216">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6a5f5-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a5f5-217">Conceptos básicos de la administración del color</span><span class="sxs-lookup"><span data-stu-id="6a5f5-217">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="6a5f5-218">Algoritmos y esquemas del Sistema de colores de Windows</span><span class="sxs-lookup"><span data-stu-id="6a5f5-218">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 