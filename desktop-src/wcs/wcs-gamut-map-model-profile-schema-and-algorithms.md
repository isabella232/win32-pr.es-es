---
title: Algoritmos y esquema de perfil del modelo de mapa de gama de WCS
description: Algoritmos y esquema de perfil del modelo de mapa de gama de WCS
ms.assetid: 64b9871a-1b4f-4e9a-be4d-4c25b3198b91
keywords:
- Windows Sistema de colores (WCS), perfil de modelo de mapa de gama (GMMP)
- WCS (Windows de color), perfil de modelo de mapa de gama (GMMP)
- administración de colores de imagen, perfil de modelo de mapa de gama (GMMP)
- administración de colores, perfil de modelo de mapa de gama (GMMP)
- colors,perfil de modelo de mapa de gama (GMMP)
- Windows Sistema de colores (WCS), perfiles
- WCS (Windows Color System),profiles
- administración de colores de imagen, perfiles
- administración de colores, perfiles
- colors,profiles
- perfil de modelo de mapa de gama (GMMP)
- GMMP (perfil de modelo de mapa de gama)
- Perfil de modelo de mapa de gama de WCS
- schemas,gamut map model profile (GMMP)
- algorithms,gamut map model profile (GMMP)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7db5b7a26fe5832fe33095c5785e90ad0a6938649878ff279e101a7e5817cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118037452"
---
# <a name="wcs-gamut-map-model-profile-schema-and-algorithms"></a>Algoritmos y esquema de perfil del modelo de mapa de gama de WCS

-   [Información general](#overview)
-   [Arquitectura del perfil del modelo de mapa de gama](#gamut-map-model-profile-architecture)
-   [Generación del límite de gama](#generation-of-the-gamut-boundary)
-   [Esquema DE GMMP](#the-gmmp-schema)
-   [Elementos de esquema de GMMP](#the-gmmp-schema-elements)
-   [GamutMapModel](#defaultbaselinegamutmapmodel-type)
    -   [Espacio de nombres](#namespace)
    -   [Versión](#version)
    -   [Documentación](#documentation)
    -   [Tipo DefaultBaselineGamutMapModel](#defaultbaselinegamutmapmodel-type)
    -   [PlugInGamutMapType](#plugingamutmaptype)
    -   [ExtensionType](#extensiontype)
-   [Algoritmos de línea base de GMMP](#the-gmmp-baseline-algorithms)
-   [Alinear los ejes neutros](#aligning-the-neutral-axes)
    -   [Diferencia mínima de color (MinCD)](#minimum-color-difference-mincd)
    -   [BasicPhoto](#basicphoto)
    -   [Información general](#overview)
    -   [El caso del shell de gama única](#the-case-of-single-gamut-shell)
    -   [Mejora de color negro](#black-enhancement)
    -   [El caso de los shells de gama dual](#the-case-of-dual-gamut-shells)
    -   [Motivos de los cambios de las recomendaciones de CIE TC8-03](#reasons-for-changes-from-the-cie-tc8-03-recommendations)
    -   [Asignación de Hue](#hue-mapping)
-   [Descripción de límites de gama y algoritmos de shell de gama](#gamut-boundary-description-and-gamut-shell-algorithms)
    -   [Triangulación del límite de la gama](#triangulation-of-the-gamut-boundary)
    -   [Elementos de línea de límite](#boundary-line-elements)
    -   [Operación de gama: CheckGamut](#gamut-operation-checkgamut)
    -   [Plano de matiz completo: Intersección](#full-hue-plane-intersect)
    -   [Operación de gama: CheckGamut (continuación)](#gamut-operation-checkgamut-continued)
    -   [Asignación de gamas de diferencias de color mínimas](#minimum-color-difference-gamut-mapping)
    -   [Suavizado de matiz](#hue-smoothing)
    -   [Establecer las primarias y secundarias en la descripción de los límites de la gama](#setting-primaries-and-secondaries-in-the-gamut-boundary-description)
    -   [Establecimiento del eje neutro en la descripción del límite de la gama](#setting-the-neutral-axis-in-the-gamut-boundary-description)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Este esquema se usa para especificar el contenido de un perfil de modelo de mapa de gama (GMMP). Los algoritmos de línea base asociados se describen en el tema siguiente.

El esquema GMMP básico consta de información de encabezado común, una referencia opcional a un complemento de modelo de mapa de gama preferido y etiquetas de extensión.

Además, el GMMP proporciona información explícita sobre el modelo de mapa de gama de destino y proporciona una directiva sobre el modelo de asignación de gamut de reserva de línea base que se usará si el modelo de destino no está disponible. El esquema puede incluir información de extensión privada, pero no incluirá ninguna otra información extraneous.

## <a name="gamut-map-model-profile-architecture"></a>Arquitectura del perfil del modelo de mapa de gama

![Diagrama que muestra el perfil de modelo de mapa de gama.](images/gmmp-image002.png)

El muestreo del espacio coloreador del dispositivo de salida se realiza iterando por los coloradores de 0,0 a 1,0 con un paso fraccionrio, acumulando todas las combinaciones de cada colorante en cada paso y, a continuación, conviviendolos del espacio coloreador del dispositivo al espacio de apariencia de color mediante el método DM::D eviceToColorimetricColors seguido del método CAM::ColorimetricToAppearanceColors. A continuación se muestra un ejemplo de cómo se hace esto para RGB.


```C++
For (red= 0.0; red <= 1.0; red += redStep) {

     For (green = 0.0; green <= 1.0; green += greenStep) {

          For (blue = 0.0; blue <= 1.0; blue += blueStep) {

               Colorants[0] = red; colorants[1] = green; colorants[2] = blue;

               pRGBDM->DeviceToColorimetricColors(1, colorants, &amp;XYZ);

               pCAM->ColorimetricToAppearanceColors(1, &amp;XYZ, &amp;JCh);

          }

     }

}

```



## <a name="generation-of-the-gamut-boundary"></a>Generación del límite de gama

Hay tres componentes en el límite de gama: los principales, los ejemplos neutros y los shells. Las primarias se generan tomando las primarias del dispositivo y aplicando la transformación DeviceToColorimetric/ColorimetricToAppearance. Las muestras neutras se generan mediante el muestreo del espacio coloreante del dispositivo en el área neutra y la aplicación de la misma transformación. Para tres dispositivos coloreantes (RGB o CMY), las muestras neutras se definen como que tienen todos los colorantes iguales, por ejemplo, R == G == B. En el caso de GNI, las muestras neutras se definen como C == M == Y == 0.

Los factores que influyen en los datos usados para crear el límite de la gama son los ejemplos de datos (solo dispositivos de línea base) y las condiciones de visualización. El tamaño del paso usado para realizar el muestreo completo del espacio coloreante (para monitores y para shell plausible) es una constante interna y no está disponible para la manipulación externa. Cambiar las condiciones de visualización cambia el comportamiento del modelo de apariencia de color (GAM) y modifica la forma del límite de la gama, por lo que debe generar un límite de gama asociado al perfil de condiciones de visualización. Si se usan datos de ejemplo, como en el caso de las impresoras de línea base y los dispositivos de captura, las muestras tendrán un gran impacto en la forma de la gama de referencia y afectarán al comportamiento del propio modelo.

Para los dispositivos de entrada, como cámaras y escáneres, se usan muestreos diferentes para generar el shell de referencia y el shell plausible. El shell de referencia se genera a partir de las medidas utilizadas para inicializar el modelo de dispositivo. El shell plausible se genera de forma similar a la ilustración anterior para los dispositivos de salida. La diferencia es que cuando se introduce un destino típico, no se obtienen valores totalmente saturados (donde R, G o B = 255). Debe extrapolar el uso del modelo de dispositivo para calcular esos valores.

## <a name="the-gmmp-schema"></a>Esquema DE GMMP


```C++
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema 
  xmlns:gmm="http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Gamut Map Model profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:element name="GamutMapModel">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ProfileName" type="wcs:MultiLocalizedTextType"/>
        <xs:element name="Description" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="Author" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="DefaultBaselineGamutMapModel">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="HPMinCD_Absolute"/>
              <xs:enumeration value="HPMinCD_Relative"/>
              <xs:enumeration value="SGCK"/>
              <xs:enumeration value="HueMap"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:element>
        <xs:element name="PlugInGamutMapModel" minOccurs="0">
          <xs:complexType>
            <xs:sequence>
              <xs:any namespace="##other" processContents="skip"
                minOccurs="0" maxOccurs="unbounded" />
            </xs:sequence>
            <xs:attribute name="GUID" type="wcs:GUIDType" use="required"/>
          </xs:complexType>
        </xs:element>
      </xs:sequence>
      <xs:attribute name="ID" type="xs:string" use="optional" />
    </xs:complexType>
  </xs:element>
</xs:schema>
```



## <a name="the-gmmp-schema-elements"></a>Elementos de esquema de GMMP

## <a name="gamutmapmodel"></a>GamutMapModel

Este elemento es una secuencia de los siguientes sub-elementos:

1.  Cadena ProfileName,
2.  DefaultBaselineGamutMapModel,
3.  Cadena de descripción opcional,
4.  Cadena de autor opcional,
5.  PlugInGamutMap opcional y
6.  ExtensionType opcional.

**Condiciones de** validación: cada sub element se valida por su propio tipo.

### <a name="namespace"></a>Espacio de nombres

xmlns:gmm=" http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel "

targetNamespace=" http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel "

### <a name="version"></a>Versión

Versión "1.0" con la primera versión de Windows Vista.

**Condiciones de** validación: 1.0 en Windows Vista. Las &lt; versiones 2.0 también son válidas para admitir cambios no importantes en el formato.

### <a name="documentation"></a>Documentación

Esquema de perfil de modelo de mapa de gama.

Copyright (C) Microsoft. All rights reserved.

**Condiciones de** validación: cada sub element se valida por su propio tipo.

### <a name="defaultbaselinegamutmapmodel-type"></a>Tipo DefaultBaselineGamutMapModel

Tipo UINT

Valores de enumeración:

<dl> "MinCD \_ Absoluto"  
"MinCD \_ Relative"  
"SIG \_ KNEE"  
"HueMap"  
</dl>

**Condiciones de** validación: los valores deben coincidir con una de las enumeraciones anteriores.

### <a name="plugingamutmaptype"></a>PlugInGamutMapType

Este elemento es una secuencia de UN GUIDType y cualquier sub-elementos.

**Condiciones de** validación: el GUID se usa para coincidir con el GUID del archivo DLL de complemento de GMM. Hay un máximo de 100 000 elementos secundarios personalizados.

### <a name="extensiontype"></a>ExtensionType

Este elemento es una secuencia opcional de cualquier subconsúmeno.

**Condiciones de** validación: puede haber un máximo de 100 000 subclases.

## <a name="the-gmmp-baseline-algorithms"></a>Algoritmos de línea base de GMMP

## <a name="aligning-the-neutral-axes"></a>Alinear los ejes neutros

La mayoría de los algoritmos de asignación de gama tienen el objetivo de asignar el eje neutro del dispositivo de origen al eje neutro del dispositivo de destino: es decir, el blanco va al blanco, el negro al negro y el gris al gris. Esto se aborda en parte mediante el escalado de la lightness de los colores de origen para que coincidan con el intervalo de lightness del dispositivo de destino. Pero eso no aborda completamente el problema.

Es una propiedad física de la mayoría de los dispositivos de creación de imágenes en los que la siticidad del blanco del dispositivo no coincide exactamente con la siticidad del dispositivo negro. Por ejemplo, el color blanco del monitor depende de la suma de lasticidades y las luminosidades relativas de las tres primarias, mientras que el negro del monitor depende de la reflectancia de la superficie de presentación. El blanco de la impresora depende de la simplicidad del papel, mientras que el negro de la impresora depende de la entrada de lápiz o el toner usado. Un modelo de apariencia que asigne el blanco del dispositivo exactamente al eje neutro del espacio de apariencia (exactamente igual a cero) no asignará el dispositivo negro al eje neutro. Dado que el ojo es más sensible a las diferencias de color gris a medida que aumenta la luz, los grises medios se representarán como incluso más tótices que el negro del dispositivo. (En la figura 1 se muestra la curvación de los ejes neutros en dos dimensiones. De hecho, los ejes neutros forman una curva más compleja en tres dimensiones).

Aunque la CÁMARA predice que estos colores neutros del dispositivo aparecerán tótices, los observadores reales parecen compensarlo. La mayoría de las personas no consideran que estos valores neutros del dispositivo sean tótices. Por lo tanto, para la mayoría de los modelos de asignación de gama, debe seguir asignando neutros de origen a neutros del dispositivo.

Para asignar neutrales de origen a neutrales del dispositivo, ajuste los límites de la gama de origen y destino y cada píxel al aplicar el algoritmo de asignación de gamas. En primer lugar, ajuste cada valor del color de origen para que el eje neutro del dispositivo de origen en la iluminación del color de origen se encuentra directamente en el eje neutro del espacio de apariencia. (Vea el lado izquierdo de la figura 1). A continuación, ajuste la descripción del límite de gama del dispositivo de destino para que cada color del eje neutro del dispositivo de destino en el color del límite de la gama del dispositivo de destino se ajuste directamente al eje neutro del espacio de apariencia. (Vea el lado derecho de la figura 1).

![Diagrama que muestra el gráfico Límite de la gama de origen a la izquierda y el límite de la gama de destino a la derecha.](images/gmmp-image004.png)

**Figura 1:** Alineación de los ejes neutros ilustrados. Izquierda: ajuste de los puntos de origen en relación con el eje neutro del dispositivo de origen. Derecha: ajuste la descripción del límite de la gama de destino en relación con la descripción del límite de la gama de destino.

Tenga en cuenta que ajusta cada valor de píxel de origen en relación con el eje neutro en ese valor de lumura. Esto garantiza que los neutros del dispositivo de origen se encontrarán en el eje neutro del modelo de apariencia. También se desplazan todos los demás colores a esa lumura en la misma cantidad, de modo que no haya discontinuidades en la representación de la gama de origen. Tiene que desplazarse por diferentes cantidades en distintos niveles de lightness, ya que los neutros del dispositivo de origen no se representan como igualmente ticos en los distintos niveles de lightness. Claramente, esto no es una transformación trivial.

Controlar los valores del dispositivo de destino es un poco más complicado. Inicialmente, se ajusta todo el límite de la gama de destino de forma similar, pero con respecto al eje neutro del dispositivo de destino. Esto se muestra en la figura 1 del lado derecho. Este ajuste garantiza que los valores grises de origen se asignarán a los valores grises de destino. Este es el espacio en el que funcionan los algoritmos de asignación de gama.

Sin embargo, este espacio no describe con precisión el comportamiento real del dispositivo de destino. Debe invertir la asignación antes de que los colores asignados a la gama se entreguen al modelo de apariencia y al modelo de dispositivo de destino. Se desplazan todos los valores asignados por lo contrario del desplazamiento aplicado anteriormente al eje neutro del dispositivo de destino. Esto asigna el eje neutro de destino al valor representado originalmente por la CÁMARA. Hace lo mismo para el límite de gama y todos los valores intermedios.

![Diagrama que muestra un gráfico para deshacer la alineación del eje neutro del dispositivo de destino.](images/gmmp-image008.png)

**Figura 2:** Deshacer la alineación del eje neutro del dispositivo de destino

### <a name="minimum-color-difference-mincd"></a>Diferencia mínima de color (MinCD)

Versiones mínimas de Diferencia de color (MinCD) Relativas y Absolutas: equivalentes a la intención colorimétrica DE C#.

> [!Note]  
> MinCD GMM es adecuado para asignar gráficos y líneas que contienen colores de "logotipo" (colores de spot), degradados de color de logotipo con algunos colores fuera de gama y para la fase final de las transformaciones de prueba. Aunque el GMM MinCD podría usarse para imágenes fotográficas que están completamente dentro de la gama de destino, no se recomienda para la representación general de imágenes fotográficas. La asignación de colores fuera de gama a los colores de la superficie de la gama de destino puede dar lugar a artefactos no deseados, como las irregularidades de tono o tonalidad en degradados suavizados que cruzan el límite de la gama. BasicPhoto se recomienda para imágenes fotográficas. Si una imagen fotográfica o contone requiere una asignación de gamas que no sea BasicPhoto, la alternativa debe ser crear un complemento GMM que implemente esa asignación, en lugar de usar MinCD.

 

Los colores en la gama se mantienen sin cambios. En el caso de los colores fuera de gama, la lumura y el efecto de color se ajustan mediante la búsqueda del punto en la gama de destino que tiene la distancia de color mínima desde los puntos de entrada fuera de gama. La distancia de color se calcula en el espacio JCh. Sin embargo, se pondera la distancia en lightness (J) y la distancia en el tono (C) o matiz (h) de forma diferente. Se usa una función de peso dependiente del tono para la distancia en lightness, de modo que el peso sea más pequeño para el tomoso pequeño y mayor para el tonalidad grande hasta que se alcance un umbral, después de lo cual el peso permanece en 1, es decir, el mismo peso que la distancia en la tonalidad o el tono. Esto sigue el uso recomendado para CMC y CIEDE2000. Hay dos variantes: colorimétrica relativa y colorimétrica absoluta.

**Colorimétrico relativo:** En primer lugar, alinee los ejes neutros de origen y destino como se describió anteriormente. A continuación, recorte el color de origen ajustado al límite de la gama de destino ajustado. (Vea la figura 4. Asignación de mapas a lo largo de la lumura constante). Reajuste los valores del dispositivo de destino como se ha descrito anteriormente. En el caso de un límite de gama de destino monocromático, el recorte de recorte significa que el valor de croma (C) se establece en cero (0,0).

**Colorimétrico absoluto:** Esto es similar al colorimétrico relativo, pero sin la alineación del eje neutro de origen y destino. El valor de origen se recorta directamente al eje neutro de destino. Tenga en cuenta que si los límites de la gama de origen y de destino son monocromáticos, el comportamiento es idéntico a la variante colorimétrica relativa; es decir, se realiza la alineación de los ejes neutros y, a continuación, se recorta a cero. Esto garantiza que se puede lograr una salida razonable incluso si los medios y los colores son significativamente diferentes.

![Diagrama que muestra un gráfico para el recorte minCD a la gama ajustada.](images/gmmp-image010.png)

**Figura 3:** Recorte minCD a la gama ajustada

### <a name="basicphoto"></a>BasicPhoto

### <a name="overview"></a>Información general

BasicPhoto: equivalente a la intención preferida, la imagentorial o perceptual de LA CORTE.

Este algoritmo es una variante de la asignación de lightness sigmoidal dependiente de la textura y el escalado de la rodura cusp (SGCK) descrito por CIE TC8-03 en CIE156:2004. Este algoritmo variante admite descriptores de límite de gama (GBD) con shells de gama doble; Es decir, GBD con un shell de referencia y un shell plausible. El algoritmo SGCK, que originalmente presupone solo un shell de gama en el GBD, se basa en el algoritmo SIG KNEE (Rsa 1999), que incorpora la asignación de luz sigmoidal y el escalado de funciones de la rodura propuestos porMut y Fairchild (1999), combinado con la dependencia de los contrabandos de \_ GCUSP (Mormut, 1998). Mantiene la constante de matiz percibido, por ejemplo, el ángulo de matiz en el jab corregido por matiz, y usa un escalado genérico de lightness sigmoidal (independiente de la imagen) que se aplica de forma dependiente de la tonalidad y un 90 por ciento de la función de rodón. La variante se escala a lo largo de líneas de lightness constante.

### <a name="the-case-of-single-gamut-shell"></a>El caso del shell de una sola gama

Resulta útil revisar el algoritmo en el caso de que los GBD de origen y destino solo tengan un shell de gama. En este caso, el algoritmo consta de los cálculos siguientes.

En primer lugar, realice la asignación de lightness inicial con la siguiente fórmula:

![Muestra la fórmula para la asignación de lightness inicial.](images/gmmp-image012.png) (1)

donde *Jₒ* es la lumura original y *J <sub>R</sub>* es la luz de reproducción.

![Muestra la segunda fórmula de asignación de lightness.](images/gmmp-image014.png) (2)

Cuando el límite de la gama de origen es monocromo, el valor de croma será cero para el límite monocromo debido a la alineación del eje neutro. Esto dará lugar al caso degenerado en el que C es igual a cero. En este caso, *p <sub>C</sub>* se establece en 1.

*p <sub>C</sub>* es un factor de ponderación dependiente de la luz (Mormut, 1998) que depende del color original, C y *J <sub>S</sub>* son el resultado de la lumíz original que se asigna mediante una función sigmoidal.

 

Para calcular *J <sub>S</sub>* (Fairchild, 1999), primero se configura una tabla de búsqueda unidimensional (LUT) entre los valores de lightness original y de reproducción en función de una función normal acumulativa discreta (S).

![Muestra una fórmula para calcular J s.](images/gmmp-image016.png) (3)

donde x ₀ y S son la desviación media y estándar de la distribución normal respectivamente e *i* = 0,1,2... *m*,*m* es el número de puntos usados en el LUT. *S <sub>i</sub>* es el valor de la función normal acumulativa para *i*  / *m* percent. Los parámetros dependen de la lumez del punto negro de la gama de reproducción y se pueden interpolar desde la tabla 1. Para obtener más información sobre el cálculo de estos parámetros, consulte Fairchild (1999, p. 391).

:::row:::
    :::column:::
        J <sub>minOut</sub>
    :::column-end:::
    :::column:::
       5.0
    :::column-end:::
    :::column:::
        10.0
    :::column-end:::
    :::column:::
        15.0
    :::column-end:::
    :::column:::
        20,0
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        x ₀
    :::column-end:::
    :::column:::
       53.7
    :::column-end:::
    :::column:::
        56.8
    :::column-end:::
    :::column:::
        58.2
    :::column-end:::
    :::column:::
        60.6
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        S
    :::column-end:::
    :::column:::
       43,0
    :::column-end:::
    :::column:::
        40,0
    :::column-end:::
    :::column:::
        35,0
    :::column-end:::
    :::column:::
        34,5
    :::column-end:::
:::row-end:::


**Tabla 1:** Cálculo de parámetros de compresión de lightness basicPhoto

Para usar S como LUT de asignación de lumez (S <sub>LUT),</sub> primero debe normalizarse en el intervalo de lumez \[ de 0100 \] . A continuación, los datos normalizados se escalan en el intervalo dinámico del dispositivo de destino, como se muestra en la ecuación 4, donde *J*<sub>min\ *Out*</sub> y *J*<sub>max\ *Out*</sub> son los valores de lumez del punto negro y el punto blanco del medio de reproducción, respectivamente.

![Muestra la fórmula para S como un LUT de asignación de lumez.](images/gmmp-image018.png) (4)

En este punto, los valores de *J S* se pueden obtener del <sub>LUT</sub> de S interpolando entre los puntos *m* de los valores *J O'* y *J S* correspondientes que contiene, y usando la siguiente ecuación como entrada.

![Muestra la fórmula para obtener los valores de J S.](images/gmmp-image020.png) (5)

J <sub>minIn</sub> es el valor de lumez del punto negro del medio original, J <sub>maxIn</sub> es el valor de lumez del punto blanco del medio original y J <sub>O</sub> es la lumíceo original. Como referencia posterior, puede indicar por *S* la función sigmoidal definida de la manera que se acaba de describir, como se muestra en la figura 4 siguiente.

![Diagrama que muestra el gráfico para la asignación de mapas a lo largo de la lumez constante.](images/gmmp-image024.png)

**Figura 4:** Asignación de mapas a lo largo de la lumez constante

En segundo lugar, si el límite de la gama de destino es tótic, comprima la compresión a lo largo de líneas de lightness constante (l) y realice la compresión como se muestra a continuación.

![Muestra la fórmula para realizar la compresión de compresión de compresión.](images/gmmp-image026.png)  (6)

donde *d* representa la distancia desde *E* en *l*; *g* representa el límite de gama media; *r* representa la reproducción; y *en* la figura 5 original.

![Diagrama en el que se muestra el gráfico de compresión de luminosidad y luminosidad en BasicPhoto.](images/gmmp-image028.png)

**Figura 5:** Compresión de luminosidad y luminosidad en BasicPhoto

Si el límite de la gama de destino es monocromo, el valor de la paleta se recorta a cero.

En tercer lugar, use un clip MinCD (descrito anteriormente) para eliminar cualquier error residual.

### <a name="black-enhancement"></a>Mejora de color negro

El algoritmo anterior se puede modificar para mejorar el negro cuando el destino es un dispositivo de impresora. El problema tiene que ver con la elección de *J <sub>minOut,</sub>* que normalmente no se corresponde con el color más oscuro que puede producir una impresora.

Más concretamente, el color con mayor densidad, obtenido al colocar 100 por ciento de las entrada de lápiz (o la cobertura máxima posible, si la limitación de GCR o de entrada de lápiz está en vigor), no suele ser "neutro" en el espacio de apariencia del color. Consulte la figura 6. En otras palabras, si se usa la lumíz mínima neutra para el dispositivo de destino, el escalador de lightness construido se asignará a una lumíz mínima que no sea la densidad más alta que puede lograr la impresora. Considere el caso de uso adicional del monitor para la impresora. El monitor negro, R=G=B=0, se imprimirá como no la densidad más alta. El impacto en la calidad de la imagen es que hay una falta de profundidad y contraste.

![Diagrama que muestra cómo el punto negro del dispositivo podría ser más oscuro que la lumíz mínima neutra.](images/gmmp-seqfigure01.png)

**Figura 6:** El punto negro del dispositivo puede ser más oscuro que la lumíz mínima neutra.

Supongamos que el "punto negro del dispositivo" de destino es Jkakbk/JkCkh k. Si C k no es cero, el punto negro del dispositivo no es neutro con respecto a CAM02. Si usa J k para la "lumíz mínima neutra" de destino en la construcción del escalador de lightness; es decir, establecer

*J <sub>minOut</sub> = Jₖ*

y aplicarlo al shell de gama de origen, obtendrá la configuración que se muestra en la figura 7. En la ilustración, el plano de matiz corresponde a h k.

![Diagrama que muestra el escalador de lumez modificado con el punto negro del dispositivo de destino.](images/gmmp-seqfigure02.png)

**Figura 7:** Geometría mediante el escalador de lightness modificado con el punto negro del dispositivo de destino

Para permitir que el algoritmo de compresión posterior continúe, quiere alinear las lumíz máximas y mínimas en los shells de origen y destino. Esto se puede lograr ajustando el shell de destino entre J <sub>neutralMin</sub> y J k desplazando los puntos a la izquierda. Además, esta transformación debe aplicarse en todo el espacio de Jab, no solo en el plano de matiz correspondiente a h k.

La transformación es

![Muestra la fórmula para la transformación.](images/gmmp-seqfigure03.png)

En la figura 8 se muestra el efecto de la transformación.

![Diagrama que muestra el efecto del escalador de lightness modificado con el punto negro del dispositivo de destino.](images/gmmp-seqfigure04.png)

**Figura 8:** Geometría mediante el escalador de lightness modificado con el punto negro del dispositivo de destino

Después de aplicar el algoritmo de compresión habitual, el punto debe "desplazarse hacia atrás"; es decir, se debe aplicar la transformación inversa para obtener el color asignado final.

![Muestra la fórmula para que la transformación inversa obtenga el color asignado final.](images/gmmp-seqfigure05.png)

### <a name="the-case-of-dual-gamut-shells"></a>El caso de los shells de gama dual

El objetivo es generalizar SIG KNEE para un shell de gama única en el caso en el que el GBD del dispositivo de origen o el GBD del dispositivo de destino tienen una estructura \_ de dos shells. El shell interno se denominará Shell de referencia, mientras que el shell externo se denominará Shell plausible. Quiere tener en cuenta los siguientes casos.

(a) Tanto el GBD de origen como el GBD de destino tienen una estructura de dos shells.

(b) El GBD de origen tiene una estructura de dos shells; el GBD de destino solo tiene un shell.

(c) El GBD de origen solo tiene un shell; el GBD de destino tiene una estructura de dos shells.

(d) Tanto el GBD de origen como el GBD de destino solo tienen un shell.

El caso (d) es el caso del shell de gama única que se ha analizado anteriormente. En el caso de los casos (a), (b) y (c), puede generalizar el reescalado de lumez para usar la información adicional de la estructura de shell dual. En los casos (b) y (c) en los que el origen o el destino solo tienen un shell, se introduce un "shell de referencia inducido", que se analizará en una sección posterior, "Shell de referencia inducido". El algoritmo general para dos shells se describirá para mayúsculas y minúsculas (a). Una vez explicada la construcción del Shell de referencia inducido, el algoritmo también se puede aplicar a las mayúsculas y minúsculas (b) y (c). En cuanto a la compresión de compresión, la relación de compresión la determinarán los shells más grandes disponibles. En otras palabras, si el Shell plausible y el Shell de referencia están disponibles, se usará el shell de Plausible; De lo contrario, se usará el Shell de referencia.

*Reescalado de lightness generalizado*

La existencia de dos shells para GBD de origen y destino significa que debe asignar un conjunto de cuatro puntos desde el GBD de origen a un conjunto correspondiente en el GBD de destino.

![Muestra cómo asignar un conjunto de cuatro puntos a un conjunto correspondiente.](images/gmmp-image030.png)

Los subíndices tienen los significados siguientes.

o o r: "original" (origen) o "reproducción" (destino)

min o max: lumez neutra mínima o lumíz máxima neutra

pla o ref: Shell plausible o Shell de referencia

La ordenación de cada uno de ellos también es la magnitud relativa esperada de estos puntos.

El mapa lightness Rescaling usa las dos primeras ecuaciones que el shell único, pero *J S* se define de forma por etapas como se muestra a continuación.

![Muestra la fórmula para J S de forma porción.](images/gmmp-image032.png) (7)

En otras palabras, es sigmoidal dentro del shell de referencia y lineal fuera. Vea la figura 9.

![Diagrama que muestra un gráfico para la función De reescalado de lumez para GBD de dos shells.](images/gmmp-image033.png)

**Figura 9:** Función de reescalado de lightness para GBD de dos shells

**SHELL DE REFERENCIA INDUCIDO**

Cuando un GBD tiene un shell y el otro GBD tiene dos shells, debe crear un "Shell de referencia" para el GBD con un solo shell. El shell existente, que se denominaría Shell de referencia, se cambiará a "Shell plausible". De hecho, en realidad no tiene que crear un shell en todo el espacio de Jab. Dado que el reescalado de lightness solo usa *J max* y *J min*, solo tiene que crear estos valores para el Shell de referencia inducido. Hay dos casos, dependiendo de qué GBD tenga dos shells.

Caso 1: GBD de origen tiene dos shells; GBD de destino tiene un shell.

Determine el shell de referencia inducido de destino en el eje neutro; es decir, J <sub>r,\ min,\ ref</sub> y J <sub>r,\ max,\ ref</sub> del shell. Esto se hace mediante el algoritmo siguiente.

![Muestra el algoritmo para determinar el shell de referencia inducido de destino.](images/gmmp-induced01.png)

¿Los factores ? <sub>low</sub> y ? <sub>controle</sub> la separación entre el shell plausible y el shell de referencia. Un valor de 1 significa que los valores <sub>mínimos de</sub> J o J mₐₓ coinciden. Sus valores se "deducen" del Shell de referencia de origen y del shell plausible de origen.

![Muestra la fórmula para los valores del Shell de referencia de origen y el shell plausible de origen.](images/gmmp-induced02.png)

Los "factores de fuga" F <sub>bajo</sub> y F <sub>alto</sub> son parámetros ajustables que deben estar entre 0 y 1.  Si el valor es 0, los comandos J <sub>min</sub> o J mₐₓ se deducen directamente desde los shells de origen. En este caso, elija F <sub>bajo</sub> = 0,95 y F <sub>alto</sub> = 0,1.

Caso 2: GBD de origen tiene un shell; GBD de destino tiene dos shells.

Determine el shell de referencia inducido de origen en el eje neutro; es decir, J <sub>o,\ min,\ ref</sub> y J <sub>o,\ max,\ ref</sub> del shell. Esto se hace mediante el algoritmo siguiente.

![Muestra el algoritmo para determinar el shell de referencia inducido de destino en el eje neutro.](images/gmmp-induced03.png)

De nuevo, los factores ? <sub>low</sub> y ? <sub>controle</sub> la separación entre el Shell plausible y el Shell de referencia. Un valor de 1 significa que los valores <sub>mínimos de</sub> J o J mₐₓ coinciden. Sus valores se "inducen" desde el Shell de referencia de origen y el shell plausible de origen:

![Muestra el algoritmo para controlar la separación entre el Shell de referencia y el shell plausible de origen.](images/gmmp-induced04.png)

### <a name="reasons-for-changes-from-the-cie-tc8-03-recommendations"></a>Motivos para los cambios de las recomendaciones de CIE TC8-03

BasicPhoto difiere de las recomendaciones de CIE TC8-03 de las siguientes maneras.

1.  La luz no se comprime hacia el cúsp, sino a lo largo de líneas de iluminación constante.
2.  El intervalo de claro usa la claroza del color más oscuro de la gama en lugar del punto en el que el límite de la gama cruza el eje neutro.
3.  BasicPhoto admite un shell de gama de referencia y un shell de gama plausible, si cualquiera de los límites de la gama de la transformación tiene dos shells.
4.  BasicPhoto usa CIECAM02; en lugar de usar CIECAM97s para convertir a D65 a 400 cd/m2 y, a continuación, usar el espacio de colores IPT de RIT.

El primer cambio se realizó para evitar problemas de inversión de tono que pueden producirse al usar la compresión hacia un cúsp. Como se muestra en la figura 10, la compresión cusp puede provocar inversiones de tono. Esto puede ocurrir cuando los colores de alta altura son más claros que los colores de menor escala. Dado que SGCK comprime cada píxel de forma independiente tanto en la lumez como en el color, no se garantiza que se conserve la relación de lumez entre los valores de píxel después de la compresión. El inconveniente conocido de esta decisión de comprimir en líneas de claro constante es que puede sufrir pérdidas de brillo, especialmente en áreas donde el límite de la gama de destino es muy plano, como sucede con los amarillos brillantes.

![Diagrama que muestra la inversión de tono causada por SGCK.](images/gmmp-toneinversion.png)

**Figura 10:** Inversión de tono causada por SGCK

![Muestra una imagen original de una cafetera.](images/originalteapot.jpg)![Muestra el resultado sgck de la imagen de la cafetera.](images/badteapot.jpg)![Muestra el resultado BasicPhoto de la imagen de la cafetera.](images/betterteapot.jpg)

**Figura 11:** Imagen original, resultado sgck y resultado basicphoto

En la figura 11 se muestra esta inversión de tono. A la izquierda hay una imagen original capturada por una cámara digital. en el centro, la imagen reproducida por SGCK; y a la derecha, la imagen reproducida por BasicPhoto. La imagen de la izquierda se encuentra en el espacio de colores de la cámara digital, las imágenes central y derecha se encuentran en el espacio de colores de una pantalla de vídeo DE LÍNEA. En la imagen original, la parte superior del depósito de té es más oscura que la inferior, porque la parte inferior refleja el mantel sobre el que se encuentra. En la imagen SGCK, la parte superior es realmente más ligera que la parte inferior, debido a la inversión de tono. Además, es difícil ver los elementos reflejados en la parte inferior de la cafetera. A la derecha, BasicPhoto ha corregido la inversión de tono y los artículos reflejados son más claramente distintivos.

El segundo cambio se realizó para mejorar la reproducción de colores casi negros en impresoras en las que el negro más negro no se encuentra directamente en el eje neutro CIECAM02. En la figura 12 siguiente se muestra una imagen convertida en sRGB; reproducido para una impresora inkjet RGB mediante SGCK; y se reproducen para la misma impresora mediante BasicPhoto. La imagen del centro no usa el dispositivo negro completo, por lo que carece del contraste que se ve en el original. El contraste se restaura con BasicPhoto.

![Muestra la imagen original de un conjunto de reproducción.](images/playstructure.jpg)![Muestra la imagen del juego reproducido para una impresora inkjet de R G B mediante SGCK.](images/playstructurebad.jpg)![Muestra la imagen del conjunto de reproducción reproducido para una impresora inkjet de R G B mediante BasicPhoto.](images/betterplaystructure.jpg)

**Figura 12:** Negro mejorado

El tercer cambio se realizó para mejorar la reproducción del color de las cámaras digitales. Especialmente en los casos en los que se ha perfilado la cámara digital mediante un destino de referencia, una descripción de límite de gama creada a partir de colores medidos podría no incluir todos los colores que se podrían capturar en una escena del mundo real. En lugar de recortar todos los colores a la gama del destino de color medido, se permite la extrapolación para generar un límite de gama plausible. El algoritmo BasicPhoto está diseñado para admitir este tipo de límite de gama extrapolada.

El cuarto cambio se realizó porque CIECAM02 funciona bien para la asignación de gamas. El proceso recomendado por TC8-03 de convertir los colores del dispositivo en D65 a 400 cd/m2 y, a continuación, usar el espacio de colores IPT de RIT es un proceso intensivo y lento.

### <a name="hue-mapping"></a>Asignación de Hue

HueMap es el equivalente de la intención de saturación DE LA MONEDA.

Si el límite de la gama de origen o el límite de la gama de destino no contiene elementos principal, este modelo vuelve al modelo MinCD (relativo) descrito en una sección anterior; por ejemplo, los dispositivos para los que no se pueden determinar los perfiles principal (perfiles DE ACUERDO CON MÁS DE CUATRO CANALES) o perfiles MONOcromáticos DE C#.

Este algoritmo ajusta primero el matiz del valor de color de entrada. A continuación, ajusta simultáneamente la luz y el brillo, mediante una asignación de cizallamiento. Por último, recorta el valor de color para asegurarse de que está dentro de la gama.

El primer paso consiste en determinar las "ruedas hue". Busque los valores de JCh para los colores principal y secundario para el dispositivo de origen y de destino. Solo está considerando los componentes de matiz. Esto da como resultado una rueda de matiz principal o secundaria con seis puntos de color para cada dispositivo. (Vea la figura 13).

![Diagrama que muestra las ruedas de matiz con seis puntos de color.](images/gmmp-figure12.png)

**Figura 13:** Ruedas hue

Se pueden obtener mejores resultados si la principal azul de origen no gira a la principal azul de destino. En su lugar, el ángulo de matiz primario azul de origen se usa como ángulo de matiz primario azul de destino.

A continuación, realice las rotaciones de matiz para cada color de entrada de la imagen de origen.

a)Mediante el ángulo de matiz del color de entrada, determine la ubicación del color en la rueda de matiz de origen en relación con los dos colores primario o secundario adyacentes. La ubicación se puede pensar en como un porcentaje de la distancia entre las primarias. Por ejemplo, el matiz de color de entrada es el 40 por ciento del camino, desde el valor de matiz de Alada al valor de matiz rojo.

b)En la rueda de matiz de destino, busque el ángulo de matiz asociado, por ejemplo, el 40 por ciento de Rojo a Rojo. Este valor será el ángulo de matiz de destino.

En general, las primarias y secundarias de origen no estarán en los mismos ángulos de matiz que las primarias y secundarias de destino; es decir, el ángulo de matiz de destino normalmente será diferente del ángulo de matiz de origen.

Por ejemplo, supongamos que las ruedas de matiz producen los siguientes valores:

Origen M = 295 grados, Origen R = 355 grados.

Destino M = 290 grados, Destino R = 346 grados.

Si el ángulo de matiz del color de entrada es de 319 grados, es el 40 por ciento del ángulo (24 grados) del origen M al origen R. El ángulo de M a R es de 60 grados y el ángulo de M a la tonalidad de entrada es de 24 grados. Calcule el ángulo en el destino que es el 40 por ciento del destino M al destino R (22 grados), por lo que el ángulo de matiz del color de destino es de 312 grados.

A continuación, calcule los puntos de referencia de matiz para el matiz de origen y el matiz de destino. Para calcular el punto de referencia de matiz para un valor h (matiz) determinado, desea buscar el valor J (lumíceo) y el valor C (croma).

-   Busque el valor J del punto de referencia de matiz mediante la interpolación entre los valores de J para los puntos primarios o secundarios adyacentes, utilizando la posición relativa del matiz; por ejemplo, el 40 por ciento en este ejemplo.
-   Busque el valor máximo de C en este valor J y h. Ahora tiene el JCh del punto de referencia de matiz para ese matiz.

![Diagrama que muestra una hoja de matiz.](images/gmmp-figure13.png)

**Figura 14:** Hoja de matiz (visualización de un segmento de límite de gama en un matiz específico)

El siguiente paso consiste en calcular la asignación de cizalla para cada píxel. En primer lugar, visualice una hoja de matiz a partir de la gama de origen para el ángulo de matiz de color de origen y una hoja de matiz de la gama de destino para el ángulo de matiz de destino calculado durante la rotación del matiz. Las hojas de matiz se crean tomando un "segmento" de la superficie de límite de la gama JCh en un ángulo de matiz específico (consulte la figura 14).

NOTA: Por motivos de optimización del rendimiento, las hojas de matiz no se crean realmente; se describen y se muestran aquí solo con fines de visualización. Las operaciones se realizan directamente en la superficie de límite de gama en el matiz especificado. A continuación, calcule los puntos de referencia de matiz para determinar la asignación de cizalla.

-   Realice un reescalado de lumez para asignar los puntos en blanco y negro de la hoja de origen a la hoja de destino (consulte la figura 15). Los puntos de color blanco y negro de la hoja de matiz de origen se asignan linealmente a los puntos blanco y negro de la hoja de matiz de destino, escalando todas las coordenadas J del límite de origen. El valor de color de entrada asignado al matiz se escala de la misma manera.

![Diagrama que muestra la asignación de lumez.](images/gmmp-figure14.png)

**Figura 15:** Asignación de lumez

-   Determine los puntos de referencia de matiz para cada hoja de matiz. Aplique una asignación de cizalla a la hoja de origen para que los puntos de referencia de origen y destino coincidan (consulte la figura 16). El punto de referencia de una gama en un matiz específico es el punto de referencia de matiz interpolado entre las primarias adyacentes. El punto de referencia de la hoja de matiz de origen se asigna linealmente al punto de referencia de la hoja de matiz de destino, mediante una operación de "cizalla" que bloquea el eje J, manteniendo los puntos negros y los puntos de color blanco estáticos. Los puntos negros, los puntos blanco y los puntos de referencia de las hojas de matiz de origen y destino deben coincidir.
-   Aplique la asignación de cizallamiento al valor de color de entrada ajustado a la luz. Las coordenadas J y C del valor de color de origen se escalan proporcionalmente, en relación con su distancia desde el eje J.
-   A continuación, se realiza una compresión sutil de lightness dependiente de la sombra hacia el valor J del punto de referencia de matiz en el punto de color asignado a la cizalla. La compresión hacia la referencia de matiz J se realiza de forma similar a gamma, donde el blanco, el negro, los grises y los puntos de la referencia de matiz J no se ven afectados. Todos los demás puntos tienden hacia la referencia de matiz J de forma suave, ligeramente a racimo cerca de la referencia de matiz J, con la constante restante de la tonalidad. La dependencia de la toba garantiza que los colores neutros no se ven afectados y que el efecto aumenta en los colores con mayor densidad.

A continuación se muestra una descripción matemática de la compresión de lumez hacia la referencia de matiz J o el ajuste del valor J del punto de destino. Se denomina punto de destino porque se ha asignado a la gama de destino.

En primer lugar, calcule "factorC" (factor de dependencia) para el punto de destino, que determina cuánto efecto tendrá la compresión de lumez. Los puntos cerca o en el eje J tendrán poca o ninguna compresión; a los puntos más alejados del eje J (altura) se les aplicará más compresión. Multiplique por 0,5 para asegurarse de que factorC es menor que 1, porque es posible que sourceC pueda ser ligeramente mayor que referenceC, pero no el doble de grande.

factorC = (destinationC/referenceC) ? 0,5

donde:

destinationC es el valor C del punto de destino.

referenceC es el valor C del punto de referencia de Hue.

A continuación, determine si el punto de destino J está por encima o por debajo de la referencia de matiz J. Si está por encima, haga lo siguiente:

1.  Calcule "factorJ" para el punto de destino en relación con referenceJ. Este valor factorJ estará entre 0 y 1 (0 si se encuentra en referenceJ; 1 si está en maxJ).
2.  factorJ = (destinationJ - referenceJ) / (maxJ - referenceJ)

    donde:

    destinationJ es el valor J del punto de destino.

    referenceJ es el valor J del punto de referencia de matiz.

    maxJ es el valor J máximo de la gama.

3.  Aplique una función de energía de tipo gamma a factorJ, lo que reducirá factorJ en una cantidad determinada. En este ejemplo se usa la potencia de 2 (el cuadrado). Reste el factorJ reducido del factorJ original y multiplique el resultado por el intervalo J total por encima de la referencia principalJ para buscar el "deltaJ", que representa el cambio en J después de la compresión de lumez, pero sin incluir la dependencia de dependencia de dependencia.
4.  deltaJ = (factorJ - (factorJ ? factorJ)) ? (maxJ - referenceJ)

5.  Aplique factorC al deltaJ (cuanto mayor sea el efecto, mayor será el efecto) y calcule el nuevo valor J para el punto de destino.
6.  destinationJ = destinationJ - (deltaJ ? factorC)

Si el valor J del punto de destino está por debajo de referenceJ, se realiza un cálculo similar a los pasos anteriores A-C, usando minJ en lugar de maxJ para buscar el intervalo en J para calcular el factorJ y teniendo en cuenta la polaridad de las operaciones "debajo" de referenceJ.

factorJ = (referenceJ - destinationJ) / (referenceJ - minJ)

deltaJ = (factorJ - (factorJ ? factorJ)) ? (referenceJ - minJ)

destinationJ = destinationJ + (deltaJ ? factorC)

donde:

minJ es el valor J mínimo de la gama.

El tono de los puntos de color de entrada se expande linealmente (siempre que sea posible) a lo largo de una lumíz constante proporcional al valor máximo de color de las gamas de origen y destino en ese matiz y lumndo. En combinación con la compresión de lumez dependiente de la curva anterior, esto ayuda a conservar la saturación porque la asignación de cizallamiento mediante los puntos de referencia a veces hace que el punto de origen se comprima en exceso en la textura (consulte la figura 16).

![Diagrama que muestra la asignación de cizalla para que coincida con los puntos de referencia de matiz, antes de la cizalla a la izquierda, después de la cizalla a la derecha.](images/gmmp-shearmapping.png)

**Figura 16:** Asignación de cizallamiento, compresión de lumez hacia la referencia de matiz J y expansión de la escala

A continuación se muestra una descripción matemática del proceso de expansión de los granos o el ajuste del valor C del punto de destino. Se denomina punto de destino porque se ha asignado la cizalla y se comprimió la lumez en la gama de destino.

1.  Antes de la asignación de cizallamiento, determine sourceExtentC (la extensión de la escala a la luz y el matiz del punto de origen).
2.  Después de la asignación de cizallamiento y la compresión de lumez que transforma el punto de origen en el punto de destino, determine el destExtentC (la extensión de la escala en la lumez y el matiz del punto de destino).
3.  Si sourceExtentC es mayor que destExtentC, no es necesario realizar ningún ajuste en el punto de destino y puede omitir el paso siguiente.
4.  Ajuste destinationC (el tono del punto de destino) para ajustarlo dentro de la extensión de la escala de destino en esta lumez y matiz.
5.  destinationC = destinationC ? (destExtentC/sourceExtentC)

    donde:

    destinationC es el valor C del punto de destino.

    sourceExtentC es el valor máximo de C de la gama de origen en la lumez y matiz del punto de origen.

    destExtentC es el valor máximo de C de la gama de destino en la lumez y matiz del punto de destino.

Por último, realice el recorte de distancia de mimimum. Si el color de entrada con matiz girado, ajustado por la luz y asignado a la inclinación todavía está ligeramente fuera de la gama de destino, recorte (muévelo) al punto más cercano en el límite de la gama de destino (consulte la figura 17).

![Diagrama que muestra el recorte de distancia mínima.](images/gmmp-figure15.png)

**Figura 17:** Recorte de distancia mínimo

## <a name="gamut-boundary-description-and-gamut-shell-algorithms"></a>Descripción de límites de gama y algoritmos de shell de gama

La función de límite de gama de dispositivos usa el motor del modelo de dispositivo y los parámetros analíticos para derivar un límite de gama de dispositivo de color, descrito como una lista de vértices indexados de la casco de la gama del dispositivo. La casco se calcula de forma diferente en función de si se trabaja con dispositivos aditivos, como monitores y proyectores, o dispositivos restivos. La lista de vértices indexados se almacena en CIEJab. DirectX optimiza la estructura de la lista de vértices indexados para la aceleración de hardware.

Este enfoque tiene muchas soluciones conocidas. Si busca "Convex hull DirectX" en la Web, se obtienen más de 100 aciertos. Por ejemplo, hay una referencia de 1983 sobre este tema específico (Computer Graphics Theory and Application, "Shipls, b-spline surfaces, and cadcam", pp. 34-49) con referencias de 1970 a 1982 sobre el tema.

La colección de puntos se puede determinar a partir de la información disponible externamente, como se indica a continuación:

-   Los puntos del shell de referencia para monitores se generan mediante un muestreo del cubo de color en el espacio coloreante del dispositivo.
-   Los puntos del shell de referencia para impresoras y dispositivos de captura se obtienen a partir de los datos de ejemplo utilizados para inicializar el modelo.
-   Los puntos del shell de referencia para scRGB y sRGB se generan mediante un muestreo del cubo de color para sRGB.
-   Los puntos del shell plausible para los dispositivos de captura se generan mediante un muestreo del cubo de color en el espacio coloreante del dispositivo.
-   Los puntos del shell de referencia para proyectores se generan mediante un muestreo de un poliedro en el cubo de color del espacio coloreador del dispositivo.
-   Los puntos para el posible shell de espacios de colores de intervalo dinámico amplio se generan mediante un muestreo del cubo de color en el propio espacio.

Puede crear una lista de vértices que describa eficazmente la gama de dispositivos de color, dado un perfil de dispositivo y servicios de soporte técnico del sistema.

En el caso de los dispositivos de salida, el límite de gama describe el intervalo de colores que puede mostrar el dispositivo. Se genera un límite de gama a partir de los mismos datos que se usan para modelar el comportamiento del dispositivo. Conceptualmente, se genera un muestreo del intervalo de colores que puede producir el dispositivo, se miden los colores, se convierten las medidas en espacio de apariencia y, a continuación, se usan los resultados para crear el límite de la gama.

Los dispositivos de entrada son más complicados. Cada píxel de una imagen de entrada debe tener algún valor. Cada píxel debe ser capaz de representar cualquier color que se encuentra en el mundo real de alguna manera. En este sentido, ningún color está "fuera de gama" para un dispositivo de entrada, ya que siempre se pueden representar.

Todos los formatos de imagen digital tienen un intervalo dinámico fijo. Debido a esta limitación, siempre hay algunos distintos valores que se asignan al mismo valor digital. Por lo tanto, no puede establecer una asignación uno a uno entre los colores reales y los valores de la cámara digital. En su lugar, el límite de la gama se forma mediante la estimación de una gama de colores reales que pueden generar las respuestas digitales de la cámara. Ese intervalo estimado se usa como la gama del dispositivo de entrada.

Las primarias se incluyen para proporcionar la asignación de gamas de tipo de intención de gráficos empresariales.

En el estilo orientado a objetos verdadero, se abstrae la representación subyacente del límite de la gama. Esto le permite la flexibilidad de cambiar la representación en el futuro. Para comprender el descriptor de límites de gama (GBD) usado en la nueva CTE, primero debe comprender cómo funcionan los algoritmos de asignación de gamas (GBA). Tradicionalmente, los GDA se han diseñado para satisfacer las necesidades de la comunidad de arte gráfico. es decir, para reproducir imágenes que ya se han representado correctamente para el dispositivo en el que se creó la imagen de entrada. El objetivo de los GBA gráficos es hacer la mejor reproducción posible de la imagen de entrada en el dispositivo de salida. El nuevo GBD de CTE está diseñado para resolver cuatro problemas clave.

Dado que la imagen de entrada se representa para el dispositivo de entrada, todos los colores caben dentro del intervalo entre el punto blanco del medio y el punto negro. Supongamos que la imagen es una fotografía de una escena en la que hay un blanco difuso, como una persona con una camiseta blanca y un resaltado especular, como la luz que refleja una ventana o un parachoques de cromo. La escena se representará en el medio de entrada para que el resaltado especular se asigne al punto blanco del medio y el blanco difuso se asigne a un color neutro más oscuro que el punto blanco del medio. La elección de cómo asignar colores de la escena al medio de entrada es una decisión dependiente de la escena y una decisión tica. Si faltaba el resaltado especular en la escena original, el blanco difuso probablemente se asignaría al punto blanco del medio. En una escena con muchos detalles de resaltado, se deja más intervalo entre el blanco especular y el blanco difuso. En una escena en la que el resaltado no es significativo, es posible que se haya dejado muy poco intervalo.

En el caso de las imágenes previamente representados, la asignación de gamas es relativamente sencilla. Básicamente, el punto blanco del medio original se asigna al punto blanco del medio de reproducción, el punto negro de origen se asigna al punto negro de destino y la mayor parte de la asignación está completa. Los diferentes GDA existentes proporcionan variaciones para asignar otros puntos en la escala de tono del medio de origen y distintas maneras de controlar los valores de curvas fuera de gama. Pero la asignación de blanco a blanco y de negro a negro es coherente a lo largo de estas variaciones. Esta implementación requiere que el blanco esté por encima de una J \* de 50 y el negro por debajo de un J \* de 50.

No todas las codificaciones de color limitan los intervalos de color para las imágenes de entrada. La codificación de color estándar IEC scRGB (IEC 61966-2-2) proporciona 16 bits para cada uno de los tres canales de color rojo, verde y azul (RGB). En esa codificación, el negro de referencia no se codifica como triple RGB (0, 0, 0), sino como (4096, 4096, 4096). El blanco de referencia se codifica como (12288, 12288, 12288). La codificación scRGB se puede usar para representar resaltados especulares y detalles de sombra. Incluye triples RGB que no son físicamente posibles porque requieren cantidades negativas de luz y codificaciones que están fuera del locus espectral de CIE. Claramente, ningún dispositivo puede producir todos los colores de la gama scRGB. De hecho, ningún dispositivo puede producir todos los colores que un ser humano puede ver. Por lo tanto, los dispositivos no pueden rellenar la gama scRGB y sería útil poder representar la parte de la gama que rellenan. Cada dispositivo tiene un intervalo de valores en el espacio scRGB que puede generar. Estos son los colores "esperados" para el dispositivo. Sería sorprendente que el dispositivo produjese colores fuera de esta gama. Hay una transformación definida del espacio scRGB al espacio de apariencia, por lo que cada dispositivo también tiene un intervalo de valores de apariencia que se espera que se reproduzcan.

Tanto en scRGB como en la entrada de dispositivos de captura caracterizados con un destino fijo, es posible obtener un valor fuera del intervalo de valores esperados. Si alguien calibra una cámara en un destino de prueba; y, a continuación, captura una escena con resaltados especulares; puede haber píxeles más claros que el punto blanco del destino. Puede ocurrir lo mismo si un rojo natural es más tótic que el rojo de destino. Si alguien toma una imagen scRGB de un dispositivo y, a continuación, edita manualmente los colores de la imagen, es posible crear píxeles que se encuentran fuera del intervalo esperado de la gama del dispositivo, aunque estén dentro de la gama completa de scRGB.

Es posible que, al principio, un segundo problema no parezca estar relacionado con esto. Se produce cuando se usa un destino de color para caracterizar un dispositivo de entrada, como una cámara o un escáner. Normalmente, los destinos reflectantes se producen en papel y contienen una serie de revisiones de color. Los manufradores proporcionan archivos de datos con medidas de color realizadas en una condición de visualización fija para cada revisión de color. Las herramientas de generación de perfiles de color crean una asignación entre estos valores medidos y los valores devueltos por los sensores de color de los dispositivos. El problema es que, a menudo, estos destinos de color no cubren toda la gama de valores de dispositivo. Por ejemplo, el escáner o la cámara podrían devolver un valor de (253, 253, 253) para el punto blanco de referencia y una revisión roja de referencia podría tener un valor RGB de (254, 12, 4). Representan el intervalo de valores esperados para el dispositivo de entrada, en función de los valores de destino. Si caracteriza el dispositivo de entrada en función de las respuestas al destino, solo espera colores dentro de este intervalo estrecho. Este intervalo no solo es menor que el intervalo de colores que pueden ver los seres humanos, sino que es menor que el intervalo de colores que puede producir el dispositivo.

En ambos casos, es difícil calcular la gama del dispositivo o la imagen de entrada, a pesar de la existencia de una gama de referencia o medidas. En el primer problema, la gama plausible del dispositivo de entrada es menor que la gama completa de scRGB. En el segundo problema, la gama de referencia del destino es menor que la gama completa posible del dispositivo de entrada.

El tercer problema implica la asignación de tono. Se han propuesto muchos modelos de límites de gama que pueden representar adecuadamente imágenes preprobadas que se usan en los gráficos, por ejemplo, los GBD de los intervalos de las montañas Desastros y Fairchild (Segment Maxima gbd) y el descriptor de límites Segment \[ \] Maxima de Mor descriptor (Morlim \[ 98). \] Pero estos modelos solo proporcionan información sobre los extremos de la gama del dispositivo. faltan información sobre otros puntos de la asignación tonal. Sin esta información, los GDA solo pueden realizar estimaciones aproximadas de la asignación de tono óptima. Peor aún, estos modelos no proporcionan ayuda para el intervalo dinámico extendido en scRGB y en imágenes de cámara digital.

¿Cómo se resuelve este problema en el sector de la fotografía y la videografía? La cámara captura una imagen. Los expertos pueden debate sobre cuánta representación se produce en el dispositivo de captura. pero están de acuerdo en que no es una cantidad significativa. Ambas tecnologías no asignan un blanco difuso de una escena capturada al punto blanco del medio. Del mismo modo, no asignan el punto negro de la escena al punto negro del medio. El comportamiento de la película fotográfica se describe en el espacio de densidad mediante una curva característica, a menudo denominada curva Desenlazador y Driffield, o curva H&D. La curva muestra la densidad de la escena original y la densidad resultante en la película. En la figura 18 se muestra una curva H&D típica. El eje X representa el aumento de la exposición del registro. El eje Y representa la densidad de la diapositiva. Se marcan cinco puntos de referencia en la curva: negro sin detalles, que representa la densidad mínima en el negativo; negro con detalles; referencia de tarjeta de color gris medio; blanco con detalles; y blanco sin detalles. Tenga en cuenta que hay espacio entre el negro sin detalles (que representa el negro del dispositivo) y el negro con detalles (negro de sombra). Del mismo modo, hay espacio entre blanco con detalles (blanco difuso) y blanco sin detalles (que representa el blanco del dispositivo).

![Diagrama que muestra la curva H y D para diapositivas.](images/gmmp-image079.png)

**Figura 18:** Curva H&D para diapositivas

El sector del vídeo proporciona "espacio para la cabeza" y "espacio para pies" en imágenes. En la especificación ITU 709, la luminosidad (denominada Y) se codifica en 8 bits, con un intervalo de 0 a 255. Sin embargo, el negro de referencia se codifica en 15 y el blanco de referencia se codifica como 235. Esto deja el intervalo de codificación entre 236 y 255 para representar resaltados especulares.

El sector del vídeo presenta un sistema de bucle cerrado esencialmente. Aunque hay muchos proveedores de equipos diferentes, los sistemas de vídeo se basan en dispositivos de referencia. Hay una codificación estándar para imágenes de vídeo. No es necesario comunicar un límite de gama con imágenes de vídeo, ya que todas las imágenes están codificadas para reproducción en el mismo dispositivo de referencia. La película también es un bucle cerrado porque no es necesario transmitir datos intermedios entre distintos componentes. Quiere una solución que permita que las imágenes de dispositivos con distintas gamas y que representen escenas tanto pre representadas como no representadas se reproduzcan en la salida con distintas gamas.

Un cuarto problema que debe resolver el nuevo CTE es que los colores grises visualmente generados por un dispositivo, por ejemplo, cuando red=green=blue en un monitor, no suelen encontrarse en el eje neutro de la CÁMARA principal (cuando el efecto de efecto es igual a 0,0). Esto provoca grandes dificultades para los GDA. Para que los GDA funcionen bien, debe ajustar la descripción de la gama del dispositivo y de los puntos de entrada para que el eje neutro del dispositivo se encuentra en el eje neutro del espacio de apariencia. Tiene que ajustar los puntos fuera del eje neutro en una cantidad similar. De lo contrario, no se pueden realizar gradaciones fluidas a través de la imagen. Al salir del GMA, se deshace esta asignación, en relación con el eje neutro del dispositivo de salida. Esto se conoce como una enderez "quiropráctica" del eje. Al igual que un narrador, no solo se endereza el esqueleto (eje neutro), sino que se ajusta el resto del cuerpo para moverse junto con el esqueleto. Al igual que un narrador, no se ajusta el esqueleto en la misma cantidad a través de todo el espacio. En su lugar, se ajustan distintas secciones de forma diferente.

![Diagrama que muestra la curvación del eje neutro del dispositivo con respecto al eje neutro de CIECAM.](images/gmmp-image081.png)

**Figura 19:** Curvatura del eje neutro del dispositivo con respecto al eje neutro de CIECAM

Lo que requiere la nueva CTE es un modelo de un límite de gama que se puede usar para representar imágenes de origen representadas y no representadas, proporcionar información sobre la apariencia de los neutros del dispositivo y proporcionar información para las imágenes de asignación de tono con un amplio intervalo de luminosidad.

![Diagrama que muestra los tres shells de gama.](images/gmmp-image083.png)

**Figura 20:** Tres shells de gama

El límite de gama se compone de tres shells que definen tres regiones.

En el nuevo CTE, el shell exterior de la gama se forma con una casco convexa realizada a partir de puntos de ejemplo en la gama del dispositivo. Un casco se forma tomando un conjunto de puntos de ejemplo y rodeandolos por una superficie. Una casco convexa tiene la propiedad adicional de ser convexa en todas partes. Por lo tanto, este no es el casco más pequeño posible que se puede ajustar a los datos. Sin embargo, la experimentación ha demostrado que ajustar demasiado los puntos de ejemplo provoca artefactos no deseados en las imágenes, como la falta de sombreado suave. La casco convexa parece resolver estos problemas.

En el algoritmo, se obtienen valores de apariencia de color para un conjunto de puntos muestreados desde el dispositivo. Para monitores e impresoras, los valores de apariencia de color se obtienen al generar muestras y, a continuación, medirlos. También puede crear un modelo de dispositivo y, a continuación, ejecutar datos sintéticos a través del modelo de dispositivo para predecir valores medidos. A continuación, los valores medidos se convierten del espacio colorimétrico (XYZ) al espacio de apariencia (Jab) y el casco se encapsula alrededor de los puntos.

El punto clave de este algoritmo es que el punto blanco adoptado que se usa en la conversión de colorimétrico al espacio de apariencia no tiene que ser el punto blanco del medio. En su lugar, puede seleccionar un punto más lejos dentro de la gama y en (o cerca) el eje neutro. Ese punto tendrá entonces un valor J de 100. Las muestras con un valor Y medido mayor que el punto blanco adoptado terminarán con un valor J mayor que 100.

Si coloca el punto blanco difuso de la escena como punto blanco adoptado para la conversión de espacio de color, los resaltados especulares de la escena se detectarán fácilmente como con un valor J mayor que 100.

Dado que el modelo de color CIECAM02 se basa en el sistema visual humano, después de seleccionar un blanco adoptado, el nivel de luminosidad del punto negro (J = 0) viene determinado automáticamente por el modelo. Si la imagen de entrada tiene un intervalo dinámico amplio, es posible que haya valores que se asignen a valores J menores que cero.

En la figura 21 siguiente se muestran los dispositivos neutros que se ejecutan a través del centro de las gamas de referencia y plausibles.

![Diagrama que muestra el eje neutro del dispositivo agregado al límite de gama.](images/gmmp-image085.png)

**Figura 21:** Eje neutro del dispositivo agregado al límite de gama

Todas las asignaciones de gama implican recortar un intervalo de entrada a una gama de salida o comprimir la gama de entrada para ajustarla a la gama de salida. Los algoritmos más complejos se forman comprimiendo y recortando en diferentes direcciones, o dividiendo la gama en regiones diferentes y, a continuación, realizando recortes o compresión en las distintas regiones.

La nueva CTE amplía este concepto para admitir las regiones de una posible gama, una gama plausible y una gama de referencia, y permite que los GMA las asignen de maneras diferentes. Además, los GDA tienen información sobre el eje neutro del dispositivo. En la siguiente explicación se explica cómo controlar situaciones en las que las gamas plausibles y las gamas de referencia se han contraído entre sí.

![Diagrama que muestra el G M A con dos descriptores de gama sin contraer.](images/gmmp-image091.png)

**Figura 22:** GMA con dos descriptores de gama sin contraer

Es posible que vea este ejemplo si asigna desde un dispositivo de entrada, como una cámara o un escáner que se caracteriza por un destino reflectante, al espacio scRGB. Aquí los colores plausibles que son más claros que el blanco de referencia son resaltados especulares. En la práctica, la caracterización de una cámara con un destino podría no generar el intervalo completo de valores posible en la cámara; sin embargo, lo harían los resaltados especulares y los colores muy colortéticos que se encuentran en la naturaleza. (Los destinos transmisivos suelen tener una revisión que es la densidad mínima posible en el medio. Con este tipo de destino, los resaltados especulares se encuentran dentro del intervalo del destino). El negro de referencia para un destino reflectante sería el principio de la región negra de la sombra. Es decir, es probable que haya colores en las sombras más oscuros que el negro en el destino. Si la imagen contiene una gran cantidad de contenido interesante en esa región, puede merecer la pena conservar esa variación tonal.

![Diagrama que muestra el G M A con una gama de destino contrae.](images/gmmp-image095.png)

**Figura 23:** GMA con gama de destino contraído

En la figura 23 se muestra un posible algoritmo de asignación de gamas cuando la gama de destino solo proporciona el intervalo de blanco a negro del dispositivo y no hay colores posibles fuera de esta gama. Es probable que esto suceda para dispositivos de salida típicos, como impresoras. Los colores posibles se asignan al borde de la gama de destino. Pero carece de una curva de tono para el dispositivo de salida. El GMA debe seleccionar algún punto neutro de luminosidad inferior para usarlo como destino de asignación para el blanco de referencia. Un algoritmo sofisticado puede hacerlo mediante el histograma de las ligeras en la imagen de origen y ver cuántas se quedan en el intervalo de espera, pero más ligera que el blanco de referencia. Cuanto más lightnesses, más espacio se requiere en el dispositivo de destino entre los puntos asignados para los resaltados especulares y el blanco de referencia. Un algoritmo más sencillo podría elegir una distancia arbitraria hacia abajo en la escala de lightness desde el blanco del dispositivo, como el 5 por ciento. Se aplica un enfoque similar para la asignación del negro máximo y el negro de sombra.

Después de generar la curva de tono de destino, puede asignar en un método similar al utilizado en la figura 23 anterior. Todos los puntos de la curva de tono de destino estarán dentro de la gama del dispositivo y todos los puntos de la asignación deben estar dentro de la gama del dispositivo.

Si invierte las figuras izquierdas y derechas, y las direcciones de las flechas de la figura 23, puede describir el caso en el que la imagen de origen solo tiene una gama de referencia y las tres gamas del dispositivo de salida no se han contraído entre sí. Un ejemplo de esto podría ser la asignación de un monitor a scRGB. De nuevo, el GMA debe sintetizar los puntos de control de los cinco puntos de la curva de tono de la imagen de origen. Algunas asignaciones podrían colocar todos los puntos de la curva de tono dentro de la gama de dispositivos scRGB, mientras que otras asignaciones podrían usar más de la gama scRGB asignando blanco difuso al blanco de referencia y permitiendo que el blanco especular se asigne a un valor más claro.

Por último, tiene el caso en el que ambos dispositivos solo tienen la gama de referencia, que es cómo funcionan la mayoría de los algoritmos de asignación de gamas. Para resolverlo, solo tiene que volver a los algoritmos actuales. Como alternativa, si tiene una manera razonable de determinar los cinco puntos de referencia para los dispositivos de origen y destino, puede organizar la asignación de los puntos de referencia.

Las gamas de dispositivos contienen más de los cinco puntos de referencia en el eje neutro. Simplemente representan los límites entre las posibles regiones de la imagen. Entre cada uno de los puntos de referencia, puede usar cualquiera de las técnicas de asignación de gama existentes. Por lo tanto, puede recortar el intervalo de colores inesperados y comprimir todos los colores entre el blanco y el negro esperados, o puede recortar todos los colores fuera del intervalo de referencia y comprimir dentro de ese intervalo. Hay muchas posibilidades, que se pueden implementar en distintos GDA. Además, los GDA pueden comprimirse y recortarse de maneras diferentes. Todas esas combinaciones se tratan dentro de esta invención.

Hasta ahora en esta discusión, la gama se ha tratado como si se tratara únicamente de una función del dispositivo en el que se creó, capturó o mostró la imagen. Sin embargo, no hay ninguna razón por la que todas las imágenes de un dispositivo deben tener la misma gama. Los GDA dependen de los datos del GBD. Si el descriptor se cambia entre imágenes, no hay ninguna manera de que los GDA lo sepan. En concreto, si las imágenes no tienen resaltados especulares, los GDA tienen un mejor rendimiento si el descriptor de la gama no muestra que hay colores más claros que el blanco difuso.

En la nueva arquitectura de CTE, es posible usar más de un GMA. El uso de varios GDA está intrínsecamente mal definido. Por ejemplo, si un dispositivo de captura asocia un GMA a su "apariencia", tiende a hacerlo con una gama de destino "dirigida". Lo mismo sucede con los dispositivos de salida y las gamas de origen "de destino". La gama sRGB es una gama implícita de destino frecuente. Por lo tanto, se recomienda encarecidamente usar un único GMA, si la predicción es una prioridad. Un único flujo de trabajo de GMA debe ser el predeterminado para todos los flujos de trabajo, especialmente los flujos de trabajo de consumidor y de prosumer. Aunque la asignación de gamas para la reproducción preferida debe realizarse una vez, hay instancias en las que se incluyen varios procesos de asignación. En primer lugar, para la prueba, se hace una asignación preferida a la gama del dispositivo de destino final y, a continuación, una representación colorimétrica en la gama del dispositivo de prueba. En segundo lugar, algunos tipos de asignación se usan para modificar las características de la imagen, pero no se incluyen para asignarse a una gama de dispositivos, por ejemplo, ajustando la curva de tono o la coloración. Si se usan varios GDA, la interfaz de transformación toma una matriz de mapas de gama enlazados, es decir, mapas de gama que se han inicializado con un par de descripciones de límites de gama. Cuando hay más de un mapa de gama, el límite de la gama de entrada para un mapa de gamas siguiente debe ser el mismo que el límite de la gama de salida de su predecesor.

La función de límite de la gama de dispositivos toma el motor del modelo de dispositivo y los parámetros analíticos y deriva un límite de gama de dispositivos de color descrito como una lista ordenada de vértices de la casco convexa de la gama del dispositivo. La lista de vértices ordenados se almacena en CIEJab. DirectX optimiza la estructura de la lista de vértices ordenados para la aceleración de hardware. Este enfoque tiene muchas soluciones conocidas (busque "Convex hull DirectX" en la web y obtenga más de 100 visitas). También hay una referencia de 1983 sobre este tema (Computer Graphics Theory and Application, "Shipls, b-spline surfaces and cadcam" pp. 34-49), con referencias de 1970 a 1982 sobre el tema.

Se pueden usar dos técnicas diferentes para calcular los triángulos del shell de gama. Para otros dispositivos que no son dispositivos RGB aditivos, se calcula una casco convexa. Puede considerar la posibilidad de investigar la compatibilidad con cascos no convexas para otros dispositivos si tiene acceso directo a dichos dispositivos para validar la solidez, el rendimiento y la fidelidad de los algoritmos. Se trata de un proceso conocido que no requiere una descripción adicional. La técnica que se usa para los dispositivos RGB aditivos se describe de la siguiente manera.

Diferentes GBD tienen ventajas e inconvenientes. La representación del casco convexa garantiza buenas propiedades geométricas, como los segmentos de matiz convexa que proporcionan un punto de intersección único con un rayo que se alterna desde un punto en el eje neutro. La desventaja de la representación de casco convexa también es la convexidad. Se sabe que muchos dispositivos, específicamente los dispositivos de presentación, tienen gamas que están lejos de ser convexas. Si la gama real se desvía significativamente de la suposición de convexidad, la representación del casco convexa sería inexacta, posiblemente en la medida en que no represente la realidad.

Después de adoptar un GBD que proporciona una representación razonablemente precisa de la gama real, surgen otros problemas, algunos debidos al mismo concepto de segmento de matiz. Hay al menos dos situaciones patológicas. En la figura 24 siguiente, una gama crt da lugar a segmentos de matiz con "islas". En la figura 25, una gama de impresora da lugar a un segmento de matiz al que falta parte del eje neutro. En estos casos, los segmentos de matiz patológico no están causados por límites de gamas especialmente patológicos. Se deben al concepto mismo de segmento de matiz, porque (a) se toma a lo largo del matiz constante y (b) solo toma la mitad del plano que corresponde al ángulo de matiz.

![Diagrama que muestra una vista superior y una vista lateral de "curving in" en los matiz azules.](images/gmmp-image097.jpg)

**Figura 24:** Un monitor crt típico tiene una gama que muestra la "curva" en los matiz azules. Si se toman segmentos de matiz dentro de este intervalo de matiz, pueden aparecer islas aisladas en los segmentos de matiz.

![Diagrama de una gama con una "brecha" en su eje neutro.](images/gmmp-image099.jpg)

**Figura 25:** Una impresora puede tener una gama que tenga "espacio" en su eje neutro. Cuando se toma un segmento de matiz (que es solo la mitad del plano), hay una "dent" en la parte del límite que es el eje neutro. Esto puede ser difícil de resolver de forma algorítmica.

Para resolver estos problemas, se propone un nuevo marco que abandone el concepto de segmento de matiz que se usa como punto de partida. En su lugar, el marco usa el conjunto de "elementos de línea de límite" o líneas que se encuentran en el límite de la gama. No proporcionan necesariamente una visualización geométrica coherente como los segmentos de matiz, pero admiten todas las operaciones de gama comunes. Además de resolver los problemas mencionados anteriormente, este enfoque también sugiere que la construcción de segmentos de matiz, incluso cuando es posible, es computacionalmente desperdiciada.

### <a name="triangulation-of-the-gamut-boundary"></a>Triangulación del límite de la gama

El punto inicial es un GBD que consta de una triangulación del límite de la gama. Los métodos conocidos de construcción de GBD normalmente proporcionan esa trianulación. Para mayor concreción, aquí se describe un método para construir GBD para dispositivos de adición en su espacio de dispositivo. Estos dispositivos incluyen monitores (basados tanto en CRT como en NFC) y proyectores. La geometría simple del cubo permite introducir una celosía normal en el cubo. Las caras de límite del cubo se pueden triangular de varias maneras, como la que se muestra en la figura 26. La arquitectura proporciona un modelo de dispositivo para el dispositivo para que los valores colorimétricos de los puntos de celosía se puedan obtener algorítmicamente, o bien se hayan realizado medidas directamente para esos puntos. La arquitectura también proporciona CIECAM02, por lo que puede suponer que los datos iniciales ya se han asignado al espacio CIECAM02 Jab. A continuación, cada punto de celosía en las caras de límite del cubo RGB tiene un punto correspondiente en el espacio de jab. Las conexiones de puntos que forman el conjunto de triángulos en el espacio RGB también inducen un conjunto de triángulos en el espacio Jab. Este conjunto de triángulos forma una triangulación razonable del límite de la gama si (a) la celosía del cubo RGB es lo suficientemente fina y (b) la transformación del espacio del dispositivo al espacio de color uniforme se comporta correctamente topológicamente. Es decir, asigna límite a límite y no convierte la gama dentro de la superficie para que los puntos interiores se conviertan en puntos de límite.

![Diagrama que muestra un método sencillo para triangluar el límite de la gama de un dispositivo con R G B como espacio del dispositivo.](images/gmmp-image100.png)

**Figura 26:** Un método sencillo para triangular el límite de la gama de un dispositivo con RGB como espacio del dispositivo

### <a name="boundary-line-elements"></a>Elementos de línea de límite

Fundamental para este marco es el concepto de elementos de línea de límite; un conjunto de segmentos de línea que (a) se encuentran en el límite de la gama y (b) se encuentran en un plano. En este caso, el plano es un plano de matiz. Cada segmento de línea es el resultado de la intersección del plano con un triángulo de límite de gama. Aunque muchos investigadores han usado la construcción de la intersección de un plano con triángulos de límite, generalmente analizan la relación entre estos segmentos de línea e intentan construir un objeto geométrico coherente a partir de los segmentos de línea. Se han diseñado algoritmos diferentes para seguir estos segmentos de línea uno tras otro hasta que se obtiene un segmento de matiz completo y se han realizado muchos intentos para acelerar el proceso de búsqueda.

Este enfoque es diferente. El plano se interseca con los triángulos para obtener los segmentos de línea. A continuación, considere estos segmentos de línea como *objetos conceptuales* básicos. Es necesario analizar la relación entre los segmentos de línea; no tiene que saber cómo están interconectadas entre sí. Este punto de vista resuelve el problema del segmento de matiz con islas. Los enfoques conocidos que intentan construir segmentos de matiz asumen que, si se empieza con un segmento de línea y lo sigue al segmento de línea siguiente, y así sucesivamente; finalmente lleva de vuelta al punto inicial, momento en el que se construiría un segmento de matiz completo. Desafortunadamente, este enfoque perdería la isla (y en el peor escenario, el continente). No es necesario tener que obtener una imagen geométrica coherente. es decir, hue slice, puede controlar el problema de la isla sin esfuerzo. Otra diferencia importante en este enfoque es que, para acelerar la construcción de segmentos de línea, usa un "filtro de triángulo". El filtro de triángulo genera determinados triángulos que definitivamente no producirán segmentos de línea que serían útiles en la operación de gama actual. Dado que la intersección de un triángulo con el plano es costosa a nivel computacional, esto mejora la velocidad. Un efecto secundario es que no se puede construir un segmento de matiz porque faltan algunos segmentos de línea debido al filtrado de triángulos.

### <a name="gamut-operation-checkgamut"></a>Operación de gama: CheckGamut

En el ejemplo siguiente se explica cómo funciona el marco y cómo se lleva a cabo CheckGamut, es decir, la operación de comprobar si un color está en la gama.

El marco general se ilustra en la figura 27 siguiente. Hay varios componentes. Los componentes etiquetados en cursiva son componentes que pueden ser diferentes en la implementación en función de la operación de gama en cuestión. Los demás componentes son invariables en todas las operaciones de gama. Para empezar, la ***entrada*** es un conjunto de atributos de color. En el caso de CheckGamut, es el color de la consulta. En la figura 27 y en la siguiente explicación, se supone que el ángulo de matiz se encuentra entre los atributos de color de entrada o se puede obtener de ellos. Este es claramente el caso si la entrada es el punto de color completo, ya sea en Jab o JCh, desde el que puede calcular el ángulo de matiz. Tenga en cuenta que el ángulo de matiz solo es necesario porque se usan planos de matiz. Dependiendo de la operación de gama en cuestión, puede que no sea necesario usar el plano de matiz. Por ejemplo, en la construcción de la rutina CheckGamut, es posible que quiera usar planos de la constante J. Se trata de una generalidad que no se usará ni se analizará con más frecuencia; pero puede ser útil recordar esta flexibilidad de la metodología para admitir otras operaciones de gama cuando el plano de matiz podría no ser la mejor opción.

![Diagrama que muestra el flujo para admitir operaciones de gama.](images/gmmp-image112.jpg)

**Figura 27:** Marco para admitir operaciones de gama

El ángulo de matiz, que se obtiene directamente de las entradas o se calcula a partir de las entradas, se usa para inicializar el plano de matiz etiquetado como **Plano** de matiz completo en la ilustración. "Full" se resalta porque se trata del plano completo, no solo el plano medio que contiene el matiz. El plano completo contiene el ángulo de matiz de entrada y el ángulo 180 grados opuesto a él. La funcionalidad clave del plano de matiz es la función Intersect, que se explica en la subsección siguiente, Full Hue Plane: Intersect. Suponga que el GBD ya se ha construido y que el conjunto de triángulos de límite **de gamut** está disponible. Intersección de los triángulos que han sobrevivido al **_Filtro de triángulo_* _ con el plano de matiz mediante Intersect. El _componente Filtro de triángulo* está etiquetado en cursiva, lo que significa que el componente varía en la implementación para diferentes operaciones de gama. El *filtro de triángulo* para CheckGamut se explica en la sección Operación de gama: CheckGamut (continuación). El resultado de la intersección de un triángulo con el plano de matiz es vacío o un elemento **de** línea de límite , es decir, un par de puntos distintos. Si el resultado no está vacío,**_ se pasa al procesador de elementos de línea * , que de nuevo realiza diferentes cosas en función de la operación de gama. El procesador de elementos line* actualiza la estructura de datos _interna, ***Datos**_ procesados internos, cuyo contenido o diseño también depende de la operación de gama. Por lo general, los datos procesados internos* contienen la "respuesta" al problema, que se actualiza continuamente con cada nuevo elemento de línea _de límite encontrado. Cuando se han procesado todos los elementos de línea de límite, se ha encontrado la respuesta. Permanece para acceder a él a través del adaptador **de salida ***_. Dado que _Internal datos procesados* es específico de  la operación de gama, el adaptador de salida también es específico de la operación de gama.

### <a name="full-hue-plane-intersect"></a>Plano de matiz completo: Intersección

La función Intersect calcula la intersección del plano de matiz y un triángulo. Tan simple como parezca, esta función es importante por dos motivos.

En primer lugar, la intersección de cada borde del triángulo con el plano podría producir tres puntos de intersección, una situación geométricamente imposible. La razón por la que esto podría ocurrir en el cálculo es que, cuando los cálculos se realizan en punto flotante, por ejemplo, en formato IEEE, hay incertidumbres o "ruido numérico" en cada paso que afecta a la conclusión de si un borde forma una intersección con el plano. Cuando el plano forma una intersección con los bordes en una situación casi de error, los puntos de intersección están cerca unos de otros y la determinación de si un punto de intersección se encuentra dentro del borde es aleatorio. Aunque el ruido en los valores numéricos de los puntos es pequeño, la conclusión cualitativa de que hay más de dos puntos de intersección es geométricamente imposible y difícil de controlar correctamente en el algoritmo.

En segundo lugar, esta función está en el bucle crítico para cada borde de cada triángulo filtrado, por lo que es importante optimizar su eficacia tanto como sea posible.

Para solucionar el primer problema de ruido numérico, realice los cálculos en enteros. Para solucionar el segundo problema de optimización de su eficacia, almacenar en caché el atributo más usado de cada vértice o el "producto de punto" asociado a cada vértice. Pasar a enteros es una manera típica de garantizar la coherencia geométrica. La idea básica es que, si tiene que cuantificar, lo haga al principio. A continuación, los cálculos posteriores se pueden realizar en enteros y, si los enteros son lo suficientemente anchos para que no haya ningún riesgo de desbordamiento, los cálculos se pueden realizar con precisión infinita. La siguiente función de cuantificación resulta útil para este propósito.

ScaleAndTruncate(x) = Parte entera de x \* 10000

El factor de escala 10000 significa que el número de punto flotante de entrada tiene cuatro posiciones decimales, lo que es lo suficientemente preciso para esta aplicación. En función del intervalo de valores del espacio de apariencia de color, quiere elegir un tipo entero con bits lo suficientemente anchos como para contener los cálculos intermedios. En la mayoría de los espacios de apariencia de color, el intervalo de cada coordenada está dentro del intervalo de -1000 a 1000. La coordenada cuantificada tiene un valor absoluto máximo posible de 1 000 \* 10 000 = 10 000 000. Como verá, la cantidad intermedia es un producto de punto, que es una suma de dos productos de coordenadas, por lo que tiene un valor absoluto máximo posible de 2 \* (10 000 000) ndo = 2?10 ₁₄. El número de bits necesarios es el registro 7 (2?10 ₁₄ ) = 47,51. Una opción conveniente para el tipo entero es, por lo tanto, enteros de 64 bits.

Para garantizar que la intersección de un plano con un triángulo siempre proporciona un conjunto vacío o un conjunto de dos puntos, debe considerar el triángulo como un todo, no como bordes individuales del triángulo por separado. Para comprender la situación geométrica, tenga en cuenta las "distancias firmadas" de los vértices del triángulo desde el plano de matiz. No calcule estas distancias firmadas directamente; en su lugar, calcule los productos de puntos de los vectores de posición de los vértices con el vector normal cuantificado al plano. Más concretamente, durante la inicialización del plano de matiz, el vector normal cuantificado se calcula como se muestra a continuación.

NormalVector = (ScaleAndTruncate(-sin(hue)), ScaleAndTruncate(cos(hue)))

Tenga en cuenta que este vector es un vector bidimensional. Puede usar un vector bidimensional porque el plano de matiz es vertical, por lo que el tercer componente del vector normal siempre es cero. Además, se inicializa una tabla de búsqueda de productos de puntos para tener una entrada para cada vértice de los triángulos de límites de gamut y el producto de punto correspondiente establecido en un valor no válido.

Durante una operación de intersección del plano de matiz con un triángulo, se busca el producto de punto de cada vértice del triángulo. Si el valor de la tabla de búsqueda es el valor no válido, el producto de punto se calcula mediante la expresión siguiente.

NormalVector.a \* ScaleAndTruncate(vertex.a) + NormalVector.b \* ScaleAndTruncate(vertex.b)

De nuevo, nunca se usa el componente J del vértice, porque el vector normal es horizontal. A continuación, este producto de punto se guarda en la tabla de búsqueda para que no tenga que calcularse de nuevo si el producto de punto del vértice se consulta más adelante.

El almacenamiento en caché permite determinar rápidamente si un borde forma una intersección con el plano, después de que los productos de puntos se tabulan en la tabla de búsqueda, que se genera progresivamente a medida que se procesan los vértices.

![Diagrama que muestra la intersección del plano de matiz con un triángulo.](images/gmmp-image114.jpg)

**Figura 28:** Intersección del plano de matiz con un triángulo

Para que el triángulo de la figura 28 intersece el plano de matiz en un segmento de línea no degenerado, los productos de puntos de los vértices deben estar en uno de los patrones siguientes, cuando se ordenan en orden ascendente.

0,0,+; -,0,0; -,0,+; -,-,+; -,+,+

Un punto final del segmento de línea surge cuando el plano se interseca con un borde con vértices que tienen signos diferentes en el producto de punto. Si el signo es cero, el vértice se encuentra justo en el plano y la intersección del borde con el plano es el propio vértice. Tenga en cuenta también que los casos son 0,0,0; -,-,0; No se notifican 0,+,+. El primer caso (0,0,0) significa que todo el triángulo se encuentra en el plano. Esto no se notifica porque cada borde del triángulo debe pertenecer a un triángulo vecino que no se encuentra completamente en el plano. El borde se mostrará cuando se tenga en cuenta ese triángulo. Los otros dos casos (-,-,0 y 0,+,+) corresponden a la configuración geométrica que el triángulo toca al plano en un vértice. Estos casos no se notifican porque no dan lugar a un segmento de línea no degenerado.

El algoritmo anterior determina cuándo calcular una intersección entre un borde del triángulo y el plano de matiz. Una vez determinado un borde, la intersección se calcula mediante ecuaciones paramétricas. Si uno de los productos de punto es cero, la intersección es el propio vértice, por lo que no es necesario realizar ningún cálculo. Suponiendo que ambos productos de puntos de los vértices del borde son  distintos de cero, vertex1 es el vértice con el producto de punto negativo dotProduct1; y vertex2 es el vértice con *el producto* de punto positivo dotProduct2. Este orden es importante para asegurarse de que el punto de intersección calculado no depende de cómo aparezca el orden de los vértices en la representación del borde. El concepto geométrico del borde es simétrico con respecto a sus vértices. El aspecto computacional del uso de ecuaciones paramétricas del borde introduce asimetría (opción de vértice inicial), que puede dar un punto de intersección ligeramente diferente debido al ruido numérico y al acondesamiento de las ecuaciones lineales que se deben resolver. Dicho esto, el punto de intersección, intersection, se da por lo siguiente.

t = dotProduct1/(dotProduct1 - dotProduct2)

Intersección. J = vértice1. J + t \* (vértice2. J: vértice1. J)

intersection.a = vertex1.a + t \* (vertex2.a - vertex1.a)

intersection.b = vertex1.b + t \* (vertex2.b - vertex1.b)

### <a name="gamut-operation-checkgamut-continued"></a>Operación de gama: CheckGamut (continuación)

El algoritmo geométrico básico que se usa para la comprobación de la gama es contar el número de cruces de rayos. Para un punto de consulta determinado, considere la posibilidad de un rayo a partir del punto de consulta y apuntando hacia arriba (dirección J). Cuente el número de veces que este rayo cruza el límite de la gama. Si este número es par, el punto de consulta está fuera de la gama. Si este número es impar, el punto está dentro. En principio, este algoritmo se puede implementar en 3D, por lo general se suele ver afectado por dificultades causadas por situaciones degeneradas, como la aserción de rayos (parcialmente) en un triángulo de límite o la degeneración dimensional inferior, como la aserción de rayos (en parte) en un borde de un triángulo de límite. Incluso en el 2D, tiene que tratar estas situaciones degeneradas. pero el problema es más sencillo y se ha solucionado de manera satisfactoria. Vea \[ O'Rou rou . \]

Para un dado punto de entrada Jab, determine su ángulo de matiz h como se muestra a continuación.

h = atan(b/a),

Inicialice el plano de matiz y, a continuación, determine los elementos de línea de límite correspondientes a este plano de matiz. Dado que los elementos de línea de límite solo son pertinentes si se cruzan con el rayo ascendente, configure un filtro de triángulo para quitar los triángulos que dan elementos de línea que definitivamente no formarán una intersección con el rayo ascendente. En este caso, considere el rectángulo delimitador del triángulo. El rayo ascendente no formará una intersección con el triángulo si el punto de consulta está fuera de la "sombra" proyectada por el rectángulo delimitador si una fuente de luz estaba directamente encima. Inflado ligeramente con una tolerancia previamente fija para permitir ruido numérico para que no se desenlacen accidentalmente triángulos que puedan proporcionar elementos de línea útiles. El resultado es el cilindro rectangular semi infinito que se muestra en la figura 29. Comprobar si el punto de consulta está dentro o fuera de este cilindro se puede implementar de forma eficaz mediante simples desigualdades.

![Muestra el filtro de triángulo para CheckGamut.](images/gmmp-image116.jpg)

**Figura 29:** Filtro de triángulo para CheckGamut

CheckGamut tiene tres componentes específicos de la operación de gama: Datos procesados *internos,* Procesador de *elementos* de línea y *Adaptador de salida.* Los *datos procesados internos son* una lista de elementos de línea procesados por el procesador de elementos de *línea*. En este caso, el procesador *de elementos line* simplemente agrega un elemento de línea a la lista. La estructura de datos interna *para los datos procesados* internos puede ser una lista vinculada o una matriz que puede aumentar de tamaño.

El *adaptador de* salida es un módulo que tiene acceso a la lista de elementos de línea y determina si un elemento de línea cruza el rayo ascendente (recuento 1) o no (recuento 0). La suma de todos estos recuentos proporciona un recuento total. En *última* instancia, el adaptador de salida genera una respuesta de "sí" (en la gama) o "no" (fuera de la gama), dependiendo de si el recuento total es impar o par. El paso en el que se determina si un elemento de línea cruza el rayo ascendente merece cierta atención porque aquí es donde surge el problema de la degeneración y también el problema del recuento en exceso. Después de O'Rouomisión, para que un elemento de línea cruce el rayo, el punto de conexión derecho (el punto final con un más grande) debe estar estrictamente en el lado derecho \[ \] del rayo. Esto garantiza que, si un punto final se encuentra exactamente en el rayo, solo se cuenta una vez. La misma regla también resuelve la situación degenerada en la que el elemento de línea se encuentra exactamente en el rayo. No se incrementa el recuento de este elemento de línea.

En la figura 30 se muestran los elementos de línea resultantes de una gama de ejemplo con el punto de consulta en varias posiciones.

![Diagrama que muestra los elementos de línea resultantes de una gama de ejemplo con el punto de consulta en varias posiciones.](images/gmmp-image118.jpg)

**Figura 30:** Funcionamiento de CheckGamut

### <a name="minimum-color-difference-gamut-mapping"></a>Asignación de gamas de diferencias de color mínimas

La asignación de gamas de diferencia de color mínima, MinDEMap, tiene una especificación simple: si un color está en la gama, no haga nada. Si un color está fuera de gama, proyecte el color en el punto "más cercano" en el límite de la gama. La palabra clave "nearest" no está bien definida hasta que se especifica la ecuación de diferencia de color que se va a usar. En la práctica, para facilitar y acelerar el cálculo, la distancia euclideña del espacio de apariencia de color elegido, o una variante de él, se usa como métrica de diferencia de color. La ventaja de la métrica euclidana es que es compatible con el producto de punto del espacio, lo que permite usar el álgebra lineal. En detalle, si se define un "producto de punto" en el espacio, se puede definir una distancia como la raíz cuadrada del producto de punto del vector de diferencia por sí mismo. Por lo general, un producto de punto se puede definir mediante una matriz A de 3x3 definitiva positiva.

u?v = u <sub>T</sub> Av

donde el lado derecho es la multiplicación de matriz habitual. Si A es la matriz de identidad, se recupera el producto de punto estándar. En la práctica, si Jab es el espacio de color, no quiere mezclar los componentes, por lo que se puede usar una matriz diagonal que no sea la matriz de identidad. Además, es posible que desee mantener la escala en a y b sin cambios para que se conserve la medida de matiz. Por lo tanto, una variación útil del producto de punto euclidano estándar es la siguiente.

w <sub>J</sub> (componente J de usted)(componente J de v) + (un componente de usted)(un componente de v) + (componente b de usted)(componente b de v)

donde w <sub>J</sub> es un número positivo. Otra variación es permitir que W <sub>J</sub> varíe con el punto de consulta de entrada:

w <sub>J\ =</sub> w <sub>J</sub> (queryPoint)

El resultado final es una medida de distancia asimétrica con respecto a los dos puntos y con pesos relativos diferentes sobre la lumez y el tonalidad a medida que varía el punto de consulta de entrada. Esto está de acuerdo con algunas observaciones sobre la percepción del color humano de que las diferencias de color no se ponderan por igual en todas las dimensiones. Se ha descubierto que las personas son menos sensibles a las diferencias de lumez que a las diferencias de matiz y tono.

La siguiente función de peso es útil.

w <sub>J</sub> = k 7 - k ₁ (C - C mₐₓ ) n

donde k ción = 1, k ₁ = 0,75/(C mₐₓ ) n, C mₐₓ = 100, n = 2 y C es el más pequeño del punto de consulta y C mₐₓ.

de modo que se ponga un peso de 0,25 en el término J cuando el grosor es cero, y un peso de 1 cuando el peso es de 100. La tendencia de colocar menos peso en J cuando la altura es pequeña, y más peso en J cuando el grosor es grande sigue el uso recomendado para CMC y CIEDE2000.

![Graph muestra la función weight en el componente J de la métrica.](images/gmmp-image119.png)

**Figura 31:** Función de peso en el componente J de la métrica

Use el espacio Jab para el ejemplo siguiente. Es computacionalmente exigente buscar en todos los triángulos de límites para determinar el punto más cercano de la métrica euclideña. El siguiente es un enfoque sencillo para hacer que este proceso sea lo más eficaz posible, sin introducir suposiciones adicionales que puedan acelerar el proceso, pero que también terminen en una respuesta aproximada. En primer lugar, es necesario comprender el procedimiento geométrico de proyectar un punto en el triángulo dado. Aquí se ofrece una descripción.

Primero se realiza una proyección ortogonal en el plano infinito que contiene el triángulo. La distancia más corta del punto de consulta desde el plano se puede determinar en dos pasos.

**(a) Calcule** el vector normal de la unidad al triángulo.

**(b) Calcule** el producto de punto del vector normal de la unidad y un vector formado a partir del punto de consulta y un punto en el triángulo; es decir, uno de sus vértices. Dado que el vector normal tiene longitud de unidad, el valor absoluto de este producto de punto es la distancia del punto de consulta desde el plano.

Es posible que el punto proyectado no sea la respuesta, ya que podría estar fuera del triángulo. Por lo tanto, primero debe realizar una comprobación. El cálculo equivale a calcular las coordenadas centradas en barras del punto proyectado en relación con el triángulo. Si se determina que el punto proyectado está dentro del triángulo, es la respuesta. Si no es así, el punto más cercano se adquiere en uno de los bordes del triángulo. Realice una búsqueda en cada uno de los tres bordes. Determinar la proyección del punto de consulta en un borde es un proceso similar a la proyección en el triángulo, pero una dimensión menor. Primero se calcula una proyección ortogonal. Si el punto proyectado se encuentra en el borde, es la respuesta. Si no es así, el punto más cercano se adquiere en uno de los dos puntos de conexión. Realizar una búsqueda en los dos puntos de conexión; es decir, calcule la distancia del punto de consulta de cada uno y compare cuál es menor.

Un examen cuidadoso revela que hay una gran cantidad de búsquedas repetidas al pasar por todos los triángulos porque un borde siempre se comparte entre dos triángulos y un vértice compartido por al menos tres bordes. Además, no le interesa mucho encontrar el punto más cercano a un triángulo determinado. en su lugar, le interesa encontrar el punto más cercano a todo el límite de la gama. Sin embargo, un triángulo determinado sería el en el que se consigue esto. Hay dos estrategias que puede usar para acelerar la búsqueda.

**Estrategia I**. Cada vértice se procesará, como máximo, una vez. Cada borde se procesará, como máximo, una vez.

**Estrategia II**. En cualquier momento de la búsqueda, tiene un mejor candidato con la mejor distancia correspondiente. Si puede determinar, mediante una comprobación rápida, que un triángulo no es capaz de proporcionar una distancia mejor, no es necesario continuar con el cálculo. No necesita el punto y la distancia más cercanos para este triángulo.

![Diagrama que muestra el flujo de la asignación mínima de DE.](images/gmmp-image120.png)

**Figura 32:** Esquemas mínimos de asignación de DE

En la figura 32 se muestra el flujo general de lógica para el mapa de gama MinDEMap. Para un punto de consulta, primero se invoca la función CheckGamut. Si el punto está en la gama, el mapa es no operativo. Si el punto está fuera de la gama, llame a ProjectPointToBoundary. Ahora, pase a la figura 33. En este momento, se supone que se han calculado los siguientes valores.

**(a) Vector** normal de unidad a cada triángulo de límite de gama con respecto al producto de punto estándar.

**(b) Lista** de vértices y lista de bordes, además de la lista de triángulos.

![Diagrama que muestra la rutina "ProjectPointToBoundary".](images/gmmp-image122.jpg)

**Figura 33:** Rutina ProjectPointToBoundary

Todas estas son sobrecargas constantes y tendrían un costo reducido si se realizan consultas suficientes a este límite de gama. Normalmente, este es el caso cuando se crea un LUT de transformación de un dispositivo a otro, donde solo hay dos gamas fijas, y el LUT de transformación se ejecuta a través de puntos en la cuadrícula muestreada uniformemente. Calcule previamente los vectores normales con respecto al producto de punto estándar, aunque la noción de elasticidad se basará en el producto de punto ponderado, que depende del punto de consulta como se explicó anteriormente. El motivo es que un vector normal con respecto al producto de punto ponderado se puede obtener fácilmente del vector normal con respecto al producto de punto estándar. Si n ₀ es un vector normal con respecto al producto de punto estándar,

n = (componente J de n ₀ /w <sub>J</sub>, a-component de n ₀, b-component de n ₀ )

es normal para el triángulo con respecto al producto de punto ponderado. Debido a esta relación, sigue siendo beneficioso calcular previamente n ₀ aunque se deba ajustar en función del punto de consulta.

La rutina ProjectPointToBoundary comienza por restablecer el "historial procesado" de los vértices y bordes. Se trata de tablas de marcas BOOLEANas que realiza un seguimiento de si un vértice o borde se ha visitado antes. También restablece la variable ShortestDistance en "INFINITY", que es el valor codificado máximo en el sistema de número de punto flotante utilizado. A continuación, se ejecuta a través de un bucle, buscando el punto más cercano de cada triángulo mediante la llamada ProcessTriangle. ProcessTriangle es la rutina para actualizar la variable ShortestDistance y está claramente en el bucle crítico. Una optimización es detenerse cuando el resultado sea lo suficientemente bueno. Después de cada llamada a ProcessTriangle, se examina la variable ShortestDistance. Si cumple un umbral predefinido, puede detenerse. El umbral predefinido depende del espacio de color utilizado y de la precisión necesaria del sistema de creación de imágenes de color. En el caso de una aplicación típica, no quiere realizar un trabajo innecesario si la diferencia de color es menor que la que puede distinguir la visión humana. Para CIECAM02, esta diferencia de color es 1. Sin embargo, use un valor de umbral de 0,005 en la implementación para conservar la precisión de los cálculos, ya que podría ser solo un paso intermedio en una cadena de transformaciones.

ProcessTriangle implementa la estrategia II anterior. Al obtener un vector normal del vector normal de la unidad calculada previamente al triángulo con respecto al producto de punto estándar, calcula la distancia del punto de consulta al plano infinito que contiene el triángulo mediante la formación del producto de puntos del vector normal de la unidad y el vector queryVector, el vector de uno de los vértices del triángulo.  vertex1, hasta el punto de consulta, queryPoint.

queryVector = queryPoint - vertex1

distance = \| normalVector \* queryVector \| / \| \| normalVector\|\|

Se trata de un cálculo relativamente económico y se requiere la distancia para llevar a cabo cálculos adicionales. Si esta distancia no es menor que la mejor distancia actual, ShortestDistance, este triángulo no producirá una distancia mejor, porque no dará una distancia mejor que el plano que lo contiene. En este caso, devuelve el control al bucle triángulo. Si la distancia es menor que ShortestDistance, posiblemente, tiene un punto más cercano, si este punto se encuentra dentro del triángulo. Debe realizar algunos cálculos "duros" (aunque nada más allá del álgebra lineal) para determinarlo. Si los otros dos vértices del triángulo son vertex2 y vertex3, forme los vectores base firstBasisVector y secondBasisVector.

firstBasisVector = vertex2 - vertex1

secondBasisVector = vertex3 - vertex1

Use el siguiente sistema lineal de ecuaciones para solucionar problemas desconocidos que usted y v.

firstBasisVector \* queryVector = (firstBasisVector \* firstBasisVector)u + (firstBasisVector \* secondBasisVector)v

secondBasisVector \* queryVector = (secondBasisVector \* firstBasisVector)u + (secondBasisVector \* secondBasisVector)v

y las condiciones para que el punto proyectado se encuentra dentro del triángulo son:

0 ≤ u ≤ 1, 0 ≤ v ≤ 1 y v ≤ 1

Después de este cálculo, si se determina que el punto proyectado se encuentra dentro del triángulo, ha encontrado un nuevo punto más cercano; la distancia que calculó al principio es la nueva distancia más corta. En este caso, actualice las variables ShortestDistance y ClosestPoint. Si el punto proyectado se encuentra fuera del triángulo, es posible que encuentre un punto más cercano en uno de sus bordes. Por lo tanto, puede llamar a la rutina ProcessEdge en cada uno de los tres bordes.

![Diagrama que muestra el flujo de las rutinas ProcessEdge y ProcessVertex.](images/gmmp-image124.jpg)

**Figura 34:** Rutinas ProcessEdge y ProcessVertex

La rutina ProcessEdge implementa la estrategia I, que se muestra en la figura 34. ProcessEdge comienza comprobando si el perímetro se ha procesado antes. Si es así, no se toma ninguna otra acción. Si no es así, continúa con el cálculo de la proyección ortogonal del punto de consulta en la línea infinita que contiene el borde. El álgebra lineal implicado en el cálculo es similar a las ecuaciones de triángulo anteriores. Sin embargo, el cálculo es más sencillo, no se describe aquí. Si el punto proyectado se encuentra dentro del borde, encontrará la distancia del punto proyectado desde el punto de consulta. Si esta distancia es menor que ShortestDistance, ha encontrado un nuevo punto más cercano. Actualice ShortestDistance y ClosestPoint. Si el punto proyectado se encuentra fuera del borde, llame a ProcessVertex en los dos puntos de conexión. Antes de devolver el control, actualice el historial de borde para que este borde esté marcado como "PROCESADO".

Por último, se ofrece una descripción de ProcessVertex. La rutina ProjectVertex también implementa la estrategia I y mantiene una tabla de historial de vértices. Como se muestra en la figura 34, primero comprueba si el vértice se ha procesado antes. Si es así, no se toma ninguna otra acción. Si no es así, continúa con el cálculo de la distancia del vértice desde el punto de consulta. Si la distancia es menor que ShortestDistance, actualice ShortestDistance y ClosestPoint. Al final, actualiza el historial de vértices para que este vértice esté marcado como "PROCESADO".

Cuando el bucle de control externo ha agotado todos los triángulos o ha salido antes de que se haya cumplido el umbral de diferencia de color, se accede a la variable ClosestPoint. Este es el resultado de MinDEMap. El autor de la llamada también puede recuperar ShortestDistance si está interesado en la distancia entre el color asignado y el color de la consulta.

### <a name="hue-smoothing"></a>Suavizado de matiz

![Diagrama que muestra dos vistas superiores del suavizado de matiz, la original en la parte superior y la tonalidad suavizada en la parte inferior.](images/gmmp-image125.png)

**Figura 35:** Suavizado de matiz

Surge un problema con las operaciones que están restringidas por matiz. Es decir, la operación solo tiene en cuenta las variables dentro de un plano de matiz. En la figura 35 se muestra un ejemplo de una gama que muestra segmentos de matiz "discontinuos" en los matiz azules. Dentro de este intervalo de matiz, para determinados ángulos de matiz, el límite de la gama es tangencial para el plano de matiz. En efecto, esto provoca un cambio en la estructura topológica de los segmentos de matiz. En el ejemplo que se muestra, a medida que el plano de matiz se arrasa en este intervalo de matiz, emerge y se sumerge una "isla". Este cambio en la topología hará que las operaciones específicas de matiz sean discontinuas. Por ejemplo, el cusp en matiz fijo cambiará repentinamente a medida que el ángulo de matiz cambie en este intervalo.

Hay una razón para la ciencia de colores por la que es conveniente conservar el matiz en determinadas operaciones. Para resolver el problema anterior, los triángulos de límite de gamut originales deben estar "suavizados de matiz". Por lo general, un suavizado de matiz de un conjunto de triángulos de límite de gama es un conjunto de triángulos de tal forma que (a) forma el límite de una nueva "gama", que podría no corresponder a la gama real del dispositivo y que contiene la gama definida por el conjunto original de triángulos. y (b) los triángulos del nuevo conjunto están limitados de ser paralelos a los planos de matiz.

Una manera práctica de obtener un conjunto de triángulos suavizados de matiz es tomar la forma convexa de los vértices originales. Como se muestra en la figura 35, los segmentos de matiz de la casco convexa varían sin problemas en el intervalo de matiz problemático sin un cambio repentino en la topología.

### <a name="setting-primaries-and-secondaries-in-the-gamut-boundary-description"></a>Establecer las primarias y secundarias en la descripción de los límites de la gama

Ciertos métodos de asignación de gamas, como HueMap, dependen de la ubicación de las principales y secundarias del dispositivo. En el caso de los dispositivos aditivos, los principales son rojo, verde y azul (R, G y B); y las secundarias son cian, después de sí y amarillas (C, M e Y). En el caso de los dispositivos restativos, las primarias son C, M e Y; y las secundarias son R, G y B. El GBD realiza un seguimiento de los seis valores, más el blanco y el negro (W y K), en una matriz de valores de color Jab. Estos valores se establecen en la descripción del límite de gama cuando se crea. En el caso de los dispositivos de salida, las primarias se pueden determinar mediante la ejecución de combinaciones de valores de control de dispositivo mediante el modelo de dispositivo. En el caso de los dispositivos de captura, este enfoque no es adecuado para crear el GBD de referencia, ya que es casi imposible capturar una imagen que produce un valor de dispositivo puro totalmente saturado, como (0.0, 0.0, 1.0). Los perfiles de dispositivo WCS contienen los índices de los principales en el destino de captura. Dado que estos valores no están incluidos en un perfil DEERT, use valores medidos desde un destino de escáner típico después de la conversión a Jab, en relación con las condiciones de visualización DE LAN.

### <a name="setting-the-neutral-axis-in-the-gamut-boundary-description"></a>Establecimiento del eje neutro en la descripción del límite de la gama

Los métodos de asignación de gamas HueMap y Relative MinCD usan el eje neutro del dispositivo para la enderez. Para los dispositivos de salida de línea base, el eje neutro se puede determinar mediante la ejecución de valores neutros del dispositivo (R=G=B o C=M=Y) a través del método DeviceToColorimetric y, a continuación, a través del método ColorimetricToAppearance del objeto CIECAM02. Sin embargo, los dispositivos de captura no siempre devuelven un valor neutro del dispositivo cuando se presenta una muestra neutra. Esto es especialmente cierto cuando la iluminación ambiente no es perfectamente neutra. Los perfiles de dispositivo WCS contienen los índices de las muestras neutras en el destino. Use esos ejemplos para establecer el eje neutro. Dado que esta información no está disponible para perfiles DE C#, debe usar el mismo método que se usa para los dispositivos de salida. ejecute ejemplos neutros del dispositivo mediante el método DeviceToColorimetric y, a continuación, aseje los valores de entrada y los resultados colorimétricos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos básicos de administración de colores](basic-color-management-concepts.md)
</dt> <dt>

[Algoritmos y esquemas del Sistema de colores de Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 




