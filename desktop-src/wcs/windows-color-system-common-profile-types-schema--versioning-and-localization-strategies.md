---
title: Esquema, versiones y estrategias de localización de tipos de perfiles comunes del Sistema de colores de Windows
description: Esquema, versiones y estrategias de localización de tipos de perfiles comunes del Sistema de colores de Windows
ms.assetid: 295522c6-7c53-47f6-9b98-aeee2b0e34fc
keywords:
- Windows Sistema de colores (WCS), tipos de perfil comunes
- WCS (Windows color), tipos de perfil comunes
- administración del color de imagen, tipos de perfil comunes
- administración de colores, tipos de perfil comunes
- colors,common profile types
- Windows Sistema de colores (WCS),perfiles
- WCS (Windows Color System),profiles
- administración de colores de imagen, perfiles
- administración de colores, perfiles
- colors,profiles
- Windows Sistema de colores (WCS), control de versiones
- WCS (Windows color),control de versiones
- administración del color de imagen, control de versiones
- administración de colores, control de versiones
- colors,versioning
- Windows Sistema de colores (WCS), localización
- WCS (Windows color),localización
- administración del color de imagen, localización
- administración de colores, localización
- colors,localization
- Tipos de perfil comunes de WCS
- consumidores de perfil
- tipos de perfil comunes
- esquemas, tipos de perfil comunes
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c9df44fa7095d8cbcd3df6de00c92ba2d4ab2ddb7ef7d3565a820e925265ea0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442295"
---
# <a name="windows-color-system-common-profile-types-schema-versioning-and-localization-strategies"></a>Esquema, versiones y estrategias de localización de tipos de perfiles comunes del Sistema de colores de Windows

-   [Esquema de tipos de perfil comunes de WCS V1](#wcs-common-profile-types-schema-v1)
-   [Adiciones de esquema V2 de tipos de perfil comunes de WCS](#wcs-common-profile-types-schema-v2-additions)
-   [Control de versiones del esquema de perfil de WCS](#wcs-profile-schema-versioning)
-   [Localización de perfil de WCS](#wcs-profile-localization)
    -   [Expresar elementos localizables](#expressing-localizable-elements)
    -   [Compatibilidad con esquemas](#schema-support)
    -   [Selección del idioma](#selecting-the-language)
    -   [Perfiles integrados](#built-in-profiles)
-   [Temas relacionados](#related-topics)

## <a name="wcs-common-profile-types-schema-v1"></a>Esquema de tipos de perfil comunes de WCS V1

A continuación se proporciona la definición de esquema v1.0 para los tipos de perfil comunes de WCS.


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



Solo se admiten las codificaciones UTF-8 o UTF-16. Se desaconseja encarecidamente el resto de codificaciones XML para conservar una interoperabilidad óptima.

## <a name="wcs-common-profile-types-schema-v2-additions"></a>Adiciones de esquema V2 de tipos de perfil comunes de WCS

En Windows 7, el esquema de tipos de perfil comunes de WCS se ha actualizado para incluir tipos que admitan el esquema [de calibración de WCS](wcs-calibration-schema.md).


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



## <a name="wcs-profile-schema-versioning"></a>Control de versiones del esquema de perfil de WCS

En este apéndice, el término "consumidor de perfiles" hace referencia al software WCS o a un componente de software de terceros que consume perfiles de WCS.

Las versiones más recientes de los consumidores de perfiles podrán consumir perfiles de WCS escritos según versiones anteriores de los esquemas. Para aprovechar al máximo las características definidas en la versión más reciente de los esquemas, generalmente se requiere la versión más reciente de un consumidor de perfiles. Sin embargo, los consumidores de perfiles más antiguos pueden consumir perfiles escritos según las versiones más recientes de los esquemas. El consumidor de perfiles puede omitir los elementos y atributos XML que no entiende. Los resultados serán correctos, pero el rendimiento o la fidelidad pueden degradarse en comparación con los resultados obtenidos con la versión más reciente del consumidor de perfiles.

A continuación se den instrucciones de control de versiones para los consumidores de perfiles:

-   Una versión determinada de un consumidor de perfil debe reconocer todos los elementos y atributos de un espacio de nombres de versión, o ninguno de ellos.
-   Si un consumidor de perfil encuentra un elemento o atributo de un espacio de nombres que no entiende, debe tratarlo como una condición de error, a menos que el perfil contenga instrucciones explícitas sobre el procesamiento de reserva.
-   Open [Packaging Specification define un](https://www.microsoft.com/whdc/xps/xpspkg.mspx) URI de espacio de nombres adicional, el espacio de nombres de compatibilidad de marcado, que define los elementos y atributos que proporcionan esta guía de procesamiento de reserva.
-   Todas las versiones de todos los consumidores de perfil deben reconocer y respetar todos los elementos y atributos del espacio de nombres de compatibilidad de marcado.
-   Los consumidores de perfiles basados en una nueva versión de los esquemas de perfil deben admitir todos los espacios de nombres de versión definidos previamente.

En la versión v1.0, WCS reconoce elementos y atributos de los siguientes espacios de nombres:

-   https://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel
-   https://schemas.microsoft.com/windows/2005/02/color/GamutMapModel
-   https://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
-   https://schemas.microsoft.com/winfx/2005/06/markup-compatibility

A continuación se muestra un ejemplo de compatibilidad de marcado.


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



## <a name="wcs-profile-localization"></a>Localización de perfil de WCS

**Requisitos**

Los perfiles de WCS contienen determinados elementos, como ProfileName y Description, que contienen texto legible. Este texto es localizable.

Las siguientes son instrucciones de control de versiones para los creadores de perfiles:

-   Para los perfiles creados por terceros, como los fabricantes de impresoras, el autor del perfil debe incorporar texto descriptivo en varios idiomas.
-   Los siguientes elementos deben ser localizables: 

    | Elemento     | Cdmp | GMMP | Campamento |
    |-------------|------|------|------|
    | ProfileName | x    | x    | x    |
    | Descripción | x    | x    | x    |
    | Autor      | x    | x    | x    |

    

     

### <a name="expressing-localizable-elements"></a>Expresar elementos localizables

En lugar de contener directamente texto, cada elemento localizable contiene uno o varios elementos secundarios wcs:Text, cada uno de los cuales debe especificar el atributo xml:lang. Como se describe en la sección 2.12 de la especificación [XML](http://www.w3.org/TR/REC-xml/) ("Identificación de idioma"), el valor del atributo xml:lang debe ser un identificador de lenguaje IETF RFC 3066, como "en-US", "en" o "fr-FR". En los esquemas WCS, el valor del atributo xml:lang no debe ser la cadena vacía "", aunque XML lo permita en el caso general. Por ejemplo:


```XML
<cdm:ColorDeviceModel ... />
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceeModel>
```



Dos elementos wcs:Text no pueden tener el mismo atributo xml:lang. Cada esquema de perfil de WCS debe aplicar esta restricción por separado para cada elemento localizable. Solo se admiten las codificaciones UTF-8 y UTF-16.

### <a name="schema-support"></a>Compatibilidad con esquemas

El diseño usa los tipos XSD wcs:LocalizedText y wcs:MultiLocalizedType definidos en el esquema de tipo de perfil común de WCS:


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



Cada esquema de perfil de WCS declara cada elemento localizable para que sea de tipo MultiLocalizedType, por ejemplo:


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



El esquema CDMP exige la restricción de que cada elemento secundario wcs:Text del elemento cdm:Description debe tener un atributo xml:lang único. Aplica la misma restricción para los demás elementos localizables. Los esquemasCAMP y GMMP hacen lo mismo.

### <a name="selecting-the-language"></a>Selección del idioma

Al decidir qué versión de idioma de un elemento localizable se va a mostrar, el código de la aplicación debe seleccionar la "versión más cercana" al "idioma actual". ¿Qué significan realmente la "versión más cercana" y el "lenguaje actual" depende de la plataforma; vea a continuación. Si el perfil no contiene una versión de idioma que coincida con el idioma actual, la aplicación debe seleccionar la primera versión del perfil (el primer elemento secundario wcs:Text del elemento localizable).

En Windows Vista, la selección de idioma se realiza de la siguiente manera: cada subproceso tiene una lista asociada de "idiomas de interfaz de usuario preferidos", que se pueden obtener llamando a [**GetThreadPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages). La lista se devuelve por orden de preferencia del usuario. Por ejemplo, en un sistema configurado para inglés de EE. UU., la lista devuelta por **GetThreadPreferredUILanguages** es { "en-US", "en" }. Esto significa: 1) Inglés de EE. UU. si está presente. 2) De lo contrario, use cualquier variante regional de inglés, como "en-GB" o simplemente "en" sin formato.

Para cada idioma de esa lista, en orden de lista, el código de la interfaz de usuario busca un elemento wcs:Text cuyo atributo xml:lang es una coincidencia exacta. Se usa la primera versión correspondiente. Si no hay coincidencias de versión, se usa el primer elemento wcs:Text.

### <a name="built-in-profiles"></a>Perfiles integrados

Los perfiles de WCS estándar incluidos Windows Vista, como sRGB.cdmp, tienen las mismas propiedades localizables que otros perfiles.

La solución Windows estándar sería colocar las cadenas localizadas en un archivo DLL de MUI y hacer referencia a ellas de la siguiente forma:


```XML
<cdm:Description resourceId="mscms.dll,-101">
    <wcs:Text xml:lang="en-US">Hello, world!</wcs:Text>
<cdm:Description>
```



En un Windows, el texto de descripción se extraería del id. de recurso 101 en la versión localizada adecuada de los recursos DE LA mscms.dll. Los sistemas no Windows usarían los subclases wcs:Text como se describió anteriormente.

Presentamos un atributo de identificador único global y opcional en el elemento raíz de cada esquema de perfil de WCS. El perfil estándar wcsRGB.cdmp podría tener este aspecto:


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



Para los perfiles de color wcs incluidos con ventanas, la CPL de color muestra información descriptiva de los recursos, en lugar de de los elementos wcs:Text de los perfiles. Esto permite Windows información localizada para estos perfiles en todos los idiomas admitidos, sin necesidad de que los perfiles que contiene contengan información descriptiva en todos los idiomas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos básicos de administración de colores](basic-color-management-concepts.md)
</dt> <dt>

[Algoritmos y esquemas del Sistema de colores de Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 