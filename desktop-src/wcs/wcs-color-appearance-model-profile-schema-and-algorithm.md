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
# <a name="wcs-color-appearance-model-profile-schema-and-algorithm"></a>Algoritmo y esquema de perfil del modelo de apariencia de color de WCS

[Información general](#overview)

[Arquitectura de Perfil de modelo de apariencia de color (CAMP)](#color-appearance-model-profile-architecture)

[El esquema de campamento](#the-camp-schema)

[Elementos del esquema CAMP](#the-camp-schema-elements)

[El algoritmo CAMP](#the-camp-algorithm)

### <a name="overview"></a>Información general

Este esquema se usa para especificar el contenido de un perfil de modelo de apariencia de color (CAMP). Los algoritmos de línea de base asociados se describen en las secciones siguientes.

El campamento se compone de etiquetas XML que proporcionan valores paramétricos a las variables del modelo de apariencia de color de línea base CIECAM02. Se proporcionan detalles sobre los intervalos para los parámetros en la especificación del modelo de apariencia de color de línea de base y la recomendación de CIECAM02.

### <a name="color-appearance-model-profile-architecture"></a>Arquitectura de Perfil de modelo de apariencia de color

![Diagrama que muestra la arquitectura de Perfil de campamento hecha de etiquetas X M L.](images/camp-image002new.png)

### <a name="the-camp-schema"></a>El esquema de campamento


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



## <a name="the-camp-schema-elements"></a>Elementos del esquema CAMP

## <a name="colorappearancemodel"></a>ColorAppearanceModel

Este elemento es una secuencia de:

1.  Cadena de perfilename,
2.  cadena de descripción opcional,
3.  cadena de autor opcional,
4.  Elemento ViewingConditions.

**Condiciones de validación:** Cada subelemento se valida por su propio tipo. Las longitudes de cadena se limitan a 10.000 caracteres.

## <a name="namespace"></a>Espacio de nombres

xmlns: Cam = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "

targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "

## <a name="version"></a>Versión

Versión &gt; 0,1 o &lt; = "1,0" con la primera versión de Windows Vista.

**Condiciones de validación:** Cualquier valor de versión &lt; = 2,0 también es válido para admitir cambios no importantes en el formato.

## <a name="documentation"></a>Documentación

Esquema de Perfil de modelo de apariencia de color.

Copyright (C) Microsoft. Todos los derechos reservados.

**Condiciones de validación:** Cada subelemento se valida por su propio tipo.

## <a name="surroundtype"></a>SurroundType

Este elemento es una enumeración de los parámetros "Average", "DIM" o "Dark" CIECAM02, o bien los parámetros cuantitativos reales de la recomendación c de CIECAM02, que afecta al envolvente.

**Condiciones de validación:** El parámetro c puede oscilar entre 0,525 y 0,69.

## <a name="viewingconditions"></a>ViewingConditions

Este elemento se compone de los siguientes subelementos:



| Elemento                    | Tipo           |
|----------------------------|----------------|
| WhitePoint                 | WhitePointType |
| Información previa                 | CIEXYZ         |
| Coloca                   | SurroundType   |
| LuminanceOfAdaptingField   | FLOAT          |
| DegreeOfAdaptation         | FLOAT          |
| NormalizeToMediaWhitePoint | Boolean        |



 

**Condiciones de validación:** NonNegativeXYZType valida los subelementos CIEXYZ. El valor de LuminanceOfAdaptingField es un máximo de 10, 000cd/m ^ 2. DegreeOfAdaptation puede oscilar entre 0,0 y 1,0. El valor de NormalizeToMediaWhitePoint puede ser "true" o "false". Si el subelemento NormalizeToMediaWhitePoint está ausente, el valor predeterminado es "true". Consulte la siguiente sección del algoritmo CAMP.

## <a name="whitepointtype"></a>WhitePointType

Este elemento es una enumeración de valores de origen de luz CIE ("D50", "D65", "A" o "F2") o un subelemento CIEXYZ.

**Condiciones de validación:** Cada subelemento se valida por su propio tipo.

## <a name="ciexyztype"></a>CIEXYZType

El elemento CIEXYZType se compone de tres elementos NonNegativeFloatType de punto flotante IEEE de precisión sencilla, denominados "X", "Y" y "Z". Estas medidas pueden ser absolutas (no relativas) CIEXYZ 1931 valores reflectantes o valores absolutos (no relativos) CIEXYZ 1931 Direct (transpermisivo) en candelas por unidades cuadradas.

**Condiciones de validación:** Esto significa que solo son válidos los valores del mundo real y los valores de medida CIEXYZ negativos no son válidos. Dado que se trata de valores absolutos, los valores pueden oscilar más allá de 1,0 f. Un límite razonable para cualquier valor X, Y o Z se establecerá arbitrariamente en 10000.0 f.

 

### <a name="the-camp-algorithm"></a>El algoritmo CAMP

El modelo de apariencia de color (CAM) se basa en las ecuaciones del modelo de apariencia de color CIE CIECAM02.

Esta clase implementa el modelado de apariencia de color. Tenga en cuenta que la leva WCS *no* es reemplazable, por ejemplo, mediante un complemento. Es un objetivo de diseño tener solo un modelo de apariencia de color. El CAM se basa en las recomendaciones de CIECAM02.

CIECAM02 se puede usar de dos maneras. En la dirección de colorimétrico-a-Appearance, proporciona una asignación desde el espacio XYZ de CIE al espacio de apariencia del color. En la dirección de la apariencia a la colorimétrico, se asigna desde el espacio de apariencia del color al espacio XYZ. La apariencia del color correlaciona la luminosidad, J, croma, C y matiz, h. Estos tres valores forman un sistema de coordenadas cilíndrico. A menudo, resulta más cómodo trabajar en un sistema de coordenadas rectangular, por lo que Compute a = C cos h y b = C sin h, para proporcionar CIECAM02 jab.

Puede usar valores de luminosidad de CAM mayores que 100. El Comité CIE que formulaba CIECAM02 no abordaba el comportamiento del eje de luminosidad para los valores de entrada con una luminancia mayor que el punto blanco adoptado; es decir, para los valores Y de entrada mayores que el valor Y del punto blanco adoptado. La experimentación ha demostrado que las ecuaciones de luminancia de CIECAM02 se comportan razonablemente para estos valores. La luminosidad aumenta exponencialmente y sigue el mismo exponente (aproximadamente 1/3).

A veces, los usuarios quieren cambiar la manera en que se calcula el grado de adaptación (D). El diseño WCS permite a los usuarios controlar este cálculo cambiando el valor de degreeOfadaptation en los parámetros de condiciones de visualización.

Para proporcionar una coincidencia más coherente con las expectativas de los usuarios con influencia de ICC, el valor de degreeOfAdaptation en los valores predeterminados es 1,0. Esto da lugar a resultados mejores en todos los casos distintos de la macropicada, donde podría querer permitir que WCS compute el degreeOfAdaptation (a través de degreeOfAdaptation =-1).

En lugar de usar un valor envolvente "Average", "DIM" y "Dark", se proporciona un valor envolvente continuo, calculado a partir del valor c. El valor de c debe ser un valor Float entre 0,525 y 0,69.

Desde *c*, se puede calcular *NC* y *F* mediante la interpolación lineal a trozos entre los valores ya proporcionados para "Average", "DIM" y "Dark". Esto modela lo que se muestra en la figura 1 de CIE 159:2004, la especificación CIECAM02.



| degreeOfAdaption                     | Comportamiento                                                                       |
|--------------------------------------|--------------------------------------------------------------------------------|
| -1.0                                 | ![Muestra una fórmula para el comportamiento predeterminado de C I E A M 02.](images/camp-image006.png)Este es el comportamiento predeterminado de CIECAM02.<br/> |
| 0,0 &lt; = degreeOfAdaption &lt; = 1,0 | *D* = degreeOfAdaptation (el valor proporcionado por el usuario)                      |



 

También se ha agregado una determinada cantidad de comprobaciones de errores a la implementación de. Los siguientes números de ecuaciones son los que se usan en la definición de CIE 159:2004 de CIECAM02.

**ColorimetricToAppearanceColors**

Se comprueba si los valores de entrada son razonables: si X o Z &lt; 0,0, o si y &lt; -1,0, el valor HRESULT es E \_ INVALIDARG. Si-1,0 &lt; = Y &lt; 0,0, entonces J, C y h se establecen en 0,0.

Existen ciertas condiciones internas que pueden generar resultados de error. En lugar de generar estos resultados, los resultados internos se recortan para generar valores en el intervalo. Esto sucede con las especificaciones de los colores que serían oscuros y, de hecho, de color cromático: en la ecuación 7,23, si el &lt; valor es 0, a = 0. En la ecuación 7,26, si t &lt; 0, t = 0.

**AppearanceToColorimetricColors**

Se comprueba si los valores de entrada son razonables. Si C &lt; 0, c &gt; 300 o J &gt; 500, el valor HRESULT es E \_ INVALIDARG.

*R '<sub>a;</sub>*, *G '<sub>a;</sub>* y *B '<sub>a;</sub>*, (las ecuaciones 8,19-8,21) se recortan al rango 399,9.

En todos los perfiles de modelo de apariencia de color (los), el motor WCS examinará el punto blanco adoptado. Si Y no es 100,0, se escalará el punto blanco adoptado para que Y sea igual a 100,0. Se aplicará el mismo ajuste de escala al valor de fondo. El factor de escala es 100,0/adoptedWhitePoint. Y. Se aplica el mismo factor de escala a cada uno de los valores X, Y y Z. Si el campo NormalizeToMediaWhitePoint se establece en "true", o si no está presente en el campamento, el motor también escala todos los colores del dispositivo de entrada a DeviceToColorimetric para que el valor Y del punto blanco del medio del dispositivo sea igual a 100,0. Los colores del dispositivo procedentes de ColorimetricToDevice se escalarán por el inverso multiplicativo de ese factor de escala. Si la marca NormalizeToMediaWhitePoint se establece en "false", los datos de la colorimétrico no se escalan.

En algunas tareas, tiene sentido escalar los valores de colorimétrica procedentes de DeviceToColorimetric. Las ecuaciones de luminosidad hiperbólica del CAM están diseñadas realmente para una luminancia de punto blanco de 100,0. El único lugar donde entra en juego una diferencia en la luminancia absoluta (o luminancia) es la luminancia del campo de adaptación. Por lo tanto, el CAM debe inicializarse con un punto blanco Y de 100,0. Sin embargo, si se usa el punto blanco medio del modelo de dispositivo como el punto blanco adoptado, todos los colores procedentes del dispositivo deben escalarse en consecuencia, o el blanco del dispositivo no obtendrá un valor de J de 100,0. Por lo tanto, los valores Y deben escalarse en las medidas. Los valores de medida se pueden escalar antes de inicializar el modelo de dispositivo. Los resultados ya estarán en el intervalo adecuado. Pero eso haría más difícil probar el modelo de dispositivo, ya que los valores que se exponen serían necesarios para el escalado. En el caso de las tareas en las que se percibe que el punto blanco medio del dispositivo es un blanco verdadero, es deseable normalizar el punto blanco del medio del dispositivo.

El CAM se inicializa directamente desde el campamento. Esto permite a los desarrolladores cierta flexibilidad a la hora de inicializar el CAM, en función de la tarea que desea realizar. En algunas tareas, los observadores omitirán cualquier intensidad de croma en los puntos blancos multimedia, ya que "saben" que los medios de origen y de destino están en blanco. En tales casos, los desarrolladores querrán inicializar las levas hacia delante e inversas con sus respectivos puntos blancos multimedia. En algunos casos, los observadores pueden estar comparando el color de los elementos multimedia. En estos casos, es aconsejable usar un CAM para ambos dispositivos y puede ser deseable no escalar los valores colorimétrica de cada dispositivo por el punto blanco medio de ese dispositivo. Después, los diferentes valores de los triestímulos del medio darán lugar a diferentes valores de apariencia en CIECAM02.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos básicos de la administración del color](basic-color-management-concepts.md)
</dt> <dt>

[Algoritmos y esquemas del Sistema de colores de Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





