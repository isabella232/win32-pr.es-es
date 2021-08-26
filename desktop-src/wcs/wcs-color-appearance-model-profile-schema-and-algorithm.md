---
title: Algoritmo y esquema de perfil del modelo de apariencia de color de WCS
description: Algoritmo y esquema de perfil del modelo de apariencia de color de WCS
ms.assetid: 017588fe-cec9-4178-a912-7950cefc036c
keywords:
- Windows Sistema de colores (WCS), perfil de modelo de apariencia de color (CAMP)
- WCS (Windows de color),perfil de modelo de apariencia de color (CAMP)
- administración de colores de imagen, perfil de modelo de apariencia de color (CAMP)
- administración de colores, perfil de modelo de apariencia de color (CAMP)
- colors,color appearance model profile (CAMP)
- Windows Sistema de colores (WCS), perfiles
- WCS (Windows Color System),profiles
- administración de colores de imagen, perfiles
- administración de colores, perfiles
- colors,profiles
- perfil de modelo de apariencia de color (CAMP)
- CAMP (perfil de modelo de apariencia de color)
- schemas,color appearance model profile (CAMP)
- algorithms,color appearance model profile (CAMP)
- Perfil de modelo de apariencia de color de WCS
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042cf74d264a7b5d40fdc30fec44784680a67b95363b579d0c7bebc7ececcedb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090113"
---
# <a name="wcs-color-appearance-model-profile-schema-and-algorithm"></a>Algoritmo y esquema de perfil del modelo de apariencia de color de WCS

[Información general](#overview)

[Arquitectura del perfil de modelo de apariencia de color (CAMP)](#color-appearance-model-profile-architecture)

[El esquema DE CAMPO](#the-camp-schema)

[Los elementos de esquema DE CAMPO](#the-camp-schema-elements)

[El algoritmoCAMP](#the-camp-algorithm)

### <a name="overview"></a>Información general

Este esquema se usa para especificar el contenido de un perfil de modelo de apariencia de color (CAMP). Los algoritmos de línea base asociados se describen en las secciones siguientes.

EL CAMPO se compone de etiquetas XML que proporcionan valores paramétricos a las variables del modelo de apariencia de color de línea base CIECAM02. Los detalles sobre los intervalos de los parámetros se proporcionan en la especificación del modelo de apariencia de color de línea base y la recomendación de CIECAM02.

### <a name="color-appearance-model-profile-architecture"></a>Arquitectura del perfil del modelo de apariencia de color

![Diagrama que muestra la arquitectura de perfil DE CAMPO realizada con etiquetas X M L.](images/camp-image002new.png)

### <a name="the-camp-schema"></a>El esquema DE CAMPO


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



## <a name="the-camp-schema-elements"></a>Los elementos de esquema DE CAMPO

## <a name="colorappearancemodel"></a>ColorAppearanceModel

Este elemento es una secuencia de:

1.  Cadena ProfileName,
2.  cadena de descripción opcional,
3.  cadena de autor opcional,
4.  Elemento ViewingConditions.

**Condiciones de validación:** Cada sub element se valida por su propio tipo. Las longitudes de cadena están limitadas a 10 000 caracteres.

## <a name="namespace"></a>Espacio de nombres

xmlns:cam=" http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "

targetNamespace=" http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "

## <a name="version"></a>Versión

Versión &gt; 0.1 o &lt; = "1.0" con la primera versión de Windows Vista.

**Condiciones de validación:** Cualquier valor de &lt; versión =2.0 también es válido para admitir cambios no importantes en el formato.

## <a name="documentation"></a>Documentación

Esquema de perfil de modelo de apariencia de color.

Copyright (C) Microsoft. All rights reserved.

**Condiciones de validación:** Cada sub element se valida por su propio tipo.

## <a name="surroundtype"></a>SurroundType

Este elemento es una enumeración de los parámetros CIECAM02 "Average", "Dim" u "Dark" o los parámetros cuantitativos reales de la recomendación CIECAM02 c, impacto del entorno.

**Condiciones de validación:** El parámetro c puede oscilar entre 0,525 y 0,69.

## <a name="viewingconditions"></a>VerCondiciones

Este elemento consta de los siguientes sub-elementos:



| Elemento                    | Tipo           |
|----------------------------|----------------|
| WhitePoint                 | WhitePointType |
| Información previa                 | CIEXYZ         |
| Rodean                   | SurroundType   |
| LuminanceOfAdaptingField   | FLOAT          |
| DegreeOfAdaptation         | FLOAT          |
| NormalizeToMediaWhitePoint | Boolean        |



 

**Condiciones de validación:** NonNegativeXYZType valida los subclases CIEXYZ. LuminanceOfAdaptingField es un máximo de 10 000cd/m^2. DegreeOfAdaptation puede oscilar entre 0,0 y 1,0. El valor normalizeToMediaWhitePoint puede ser "true" o "false". Si el sub element NormalizeToMediaWhitePoint no está presente, el valor predeterminado es "true". Consulte la siguiente sección del algoritmoCAMP.

## <a name="whitepointtype"></a>WhitePointType

Este elemento es una enumeración de un valor de origen de luz de CIE ("D50," "D65," "A" o "F2") o un sub-elemento CIEXYZ.

**Condiciones de validación:** Cada sub element se valida por su propio tipo.

## <a name="ciexyztype"></a>CIEXYZType

El elemento CIEXYZType se compone de tres elementos de punto flotante IEEE de precisión sencilla NonNegativeFloatType, denominados "X", "Y" y "Z". Estas medidas pueden ser valores reflectantes absolutos (no relativos) de CIEXYZ 1931 o valores directos (transmisivos) absolutos (no relativos) de CIEXYZ 1931 en candelas por metro cuadrado.

**Condiciones de validación:** Esto significa que solo los valores reales son válidos y que los valores de medida de CIEXYZ negativos no son válidos. Puesto que se trata de valores absolutos, los valores pueden ir más allá de 1,0f. Un límite razonable para cualquier valor X, Y o Z se establecerá arbitrariamente en 10000.0f.

 

### <a name="the-camp-algorithm"></a>Algoritmo DE CAMPO

El modelo de apariencia de color (CAM) se basa en las ecuaciones del modelo de apariencia de color de CIE CIECAM02.

Esta clase implementa el modelado de apariencia de color. Tenga en cuenta que el WCS CAM no *se* puede reemplazar, por ejemplo, mediante un complemento. Es un objetivo de diseño tener solo un modelo de apariencia de color. La CÁMARA se basa en las recomendaciones de CIECAM02.

CIECAM02 se puede usar de dos maneras. En la dirección de colorimétrica a apariencia, proporciona una asignación del espacio CIE XYZ al espacio de apariencia de color. En la dirección de apariencia a colorimétrica, se asigna del espacio de apariencia de color al espacio XYZ. La apariencia del color correlaciona la lumez, J, el tono, C y el matiz, h. Estos tres valores forman un sistema de coordenadas cilíndrica. Con frecuencia, resulta más conveniente trabajar en un sistema de coordenadas rectangular, así que calcule a = C cos h y b = C sin h, para dar a CIECAM02 Jab.

Puede usar valores de lumez de LA CÁMARA mayores que 100. El comité de CIE que formuló CIECAM02 no abordaba el comportamiento del eje de lumez para los valores de entrada con una luminosidad mayor que el punto blanco adoptado. Es decir, para los valores Y de entrada mayores que el valor Y del punto blanco adoptado. La experimentación ha demostrado que las ecuaciones de luminosidad de CIECAM02 se comportan razonablemente para estos valores. La lumura aumenta exponencialmente y sigue al mismo exponente (aproximadamente 1/3).

A veces, los usuarios quieren cambiar la forma en que se calcula el grado de adaptación (D). El diseño de WCS permite a los usuarios controlar este cálculo cambiando el valor degreeOfadaptation en los parámetros de condiciones de visualización.

Para proporcionar una coincidencia más coherente con las expectativas de los usuarios afectadas por LA CPI, el valor de degreeOfAdaptation en el VALOR PREDETERMINADO DE LOS CAMPOS es 1,0. Esto produce mejores resultados en todos los casos distintos de MinCD Absolute, donde es posible que desee permitir que WCS calcule el degreeOfAdaptation (a través de degreeOfAdaptation = -1).

En lugar de usar un valor envolvente de "Average", "Dim" y "Dark", se proporciona un valor envolvente continuo, calculado a partir del valor c. El valor de c debe ser un valor float entre 0,525 y 0,69.

Desde *c*, *Nc* y *F* se pueden calcular, mediante la interpolación lineal por fragmentos entre los valores ya proporcionados para "Average", "Dim" y "Dark". Esto modela lo que se muestra en la figura 1 de CIE 159:2004, especificación CIECAM02.



| degreeOfAdaption                     | Comportamiento                                                                       |
|--------------------------------------|--------------------------------------------------------------------------------|
| -1.0                                 | ![Muestra una fórmula para el comportamiento predeterminado de C I E C A M 02.](images/camp-image006.png)Este es el comportamiento predeterminado de CIECAM02.<br/> |
| 0,0 &lt; = degreeOfAdaption &lt; = 1,0 | *D* = degreeOfAdaptation (el valor proporcionado por el usuario)                      |



 

También se ha agregado una determinada cantidad de comprobación de errores a la implementación. Los números de ecuación siguientes son los que se usan en la definición 159:2004 de CIECAM02.

**ColorimetricToAppearanceColors**

Se comprueba si los valores de entrada son razonables: si X o Z &lt; 0,0, o si Y &lt; -1,0, el valor HRESULT es E \_ INVALIDARG. Si -1,0 &lt; = Y &lt; 0,0, J, C y h se establecen en 0,0.

Hay ciertas condiciones internas que pueden producir resultados de error. En lugar de producir estos resultados, los resultados internos se recortan para generar valores dentro del intervalo. Esto sucede para las especificaciones de colores que serían oscuros e imposidores: en la ecuación 7.23, si A &lt; 0, A = 0. En la ecuación 7,26, si t &lt; 0, t = 0.

**AppearanceToColorimetricColors**

Se comprueba si los valores de entrada son razonables. Si C &lt; 0, C &gt; 300 o J &gt; 500, el valor HRESULT es E \_ INVALIDARG.

*R'<sub>a;</sub>*, *G'<sub>a;</sub>* y *B'<sub>a;</sub>*, (ecuaciones 8,19 - 8,21) se recortan al intervalo 399,9 .

Para todos los perfiles de modelo de apariencia de color (PMI), el motor WCS examinará el punto blanco adoptado. Si Y no es 100,0, el punto blanco adoptado se escalará para que Y sea igual a 100,0. El mismo escalado se aplicará al valor en segundo plano. El factor de escalado es 100.0/adoptedWhitePoint.Y. El mismo factor de escalado se aplica a cada una de las X, Y y Z. Si el campo NormalizeToMediaWhitePoint está establecido en "True", o si no está presente en EL CAMPO, el motor también escala todos los colores del dispositivo de entrada a DeviceToColorimetric para que el valor Y del punto blanco del medio del dispositivo sea igual a 100,0. Los colores del dispositivo procedentes de ColorimetricToDevice se escalarán por el inverso multiplicativo de ese factor de escalado. Si la marca NormalizeToMediaWhitePoint está establecida en "False", los datos colorimétricos no se escalan.

Para algunas tareas, tiene sentido escalar los valores colorimétricos procedentes de DeviceToColorimetric. Las ecuaciones de lightness hiperbólica en el MES están diseñadas realmente para una luminosidad de punto blanco de 100,0. El único lugar donde entra en juego una diferencia en la luminosidad absoluta (o iluminación) es en la luminosidad del campo de adaptación. Por lo tanto, la CÁMARA debe inicializarse con un punto blanco Y de 100,0. Pero si el punto blanco medio del modelo de dispositivo se usa como punto blanco adoptado, todos los colores procedentes del dispositivo se deben escalar en consecuencia o el blanco del dispositivo no aparecerá con un valor J de 100,0. Por lo tanto, los valores Y deben escalarse en las medidas. Los valores de medida se podrían escalar antes de inicializar el modelo de dispositivo. A continuación, los resultados ya estarían en el intervalo adecuado. Pero eso dificultaría la prueba del modelo de dispositivo, ya que los valores que saldría requerirían escalado. En el caso de las tareas en las que el punto blanco medio del dispositivo se percibe como un verdadero blanco, es conveniente normalizar por el punto blanco del medio del dispositivo.

La CÁMARA se inicializa directamente desde EL CAMPO. Esto permite a los desarrolladores cierta flexibilidad a la hora de inicializar la CÁMARA, en función de la tarea que desean realizar. En algunas tareas, los observadores pasarán por alto los puntos de color blanco de los medios, ya que cognitivamente "saben" que los medios de origen y de destino son "blanco". En tales casos, los desarrolladores querrán inicializar las CAM inversas y hacia delante con sus respectivos puntos en blanco multimedia. En algunos casos, los observadores pueden comparar el color de los fondos multimedia. En estos casos, es aconsejable usar una MES para ambos dispositivos y puede ser conveniente no escalar los valores colorimétricos de cada dispositivo por el punto blanco medio de ese dispositivo. A continuación, los distintos valores tmulus de los medios darán lugar a distintos valores de apariencia en CIECAM02.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos básicos de administración de colores](basic-color-management-concepts.md)
</dt> <dt>

[Algoritmos y esquemas del Sistema de colores de Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





