---
title: Algoritmos y esquema de perfil del modelo de mapa de gama de WCS
description: Algoritmos y esquema de perfil del modelo de mapa de gama de WCS
ms.assetid: 64b9871a-1b4f-4e9a-be4d-4c25b3198b91
keywords:
- Sistema de color de Windows (WCS), perfil de modelo de mapa de gama (GMMP)
- WCS (sistema de color de Windows), perfil de modelo de mapa de gama (GMMP)
- Administración del color de imagen, perfil de modelo de mapa de gama (GMMP)
- Administración del color, perfil de modelo de mapa de gamas (GMMP)
- colores, perfil de modelo de mapa de gama (GMMP)
- Sistema de color de Windows (WCS), perfiles
- WCS (sistema de colores de Windows), perfiles
- Administración del color de imagen, perfiles
- Administración del color, perfiles
- colores, perfiles
- Perfil de modelo de mapa de gamas (GMMP)
- GMMP (Perfil de modelo de mapa de gama)
- Perfil de modelo de mapa de gama WCS
- esquemas, perfil de modelo de mapa de gama (GMMP)
- algoritmos, perfil de modelo de mapa de gama (GMMP)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3714e5d7592cb1fbbbfa98e238642a2fcb38bafd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104568207"
---
# <a name="wcs-gamut-map-model-profile-schema-and-algorithms"></a>Algoritmos y esquema de perfil del modelo de mapa de gama de WCS

-   [Información general](#overview)
-   [Arquitectura de Perfil de modelo de mapa de gama](#gamut-map-model-profile-architecture)
-   [Generación del límite de la gama](#generation-of-the-gamut-boundary)
-   [El esquema GMMP](#the-gmmp-schema)
-   [Los elementos de esquema GMMP](#the-gmmp-schema-elements)
-   [GamutMapModel](#defaultbaselinegamutmapmodel-type)
    -   [Espacio de nombres](#namespace)
    -   [Versión](#version)
    -   [Documentación](#documentation)
    -   [Tipo DefaultBaselineGamutMapModel](#defaultbaselinegamutmapmodel-type)
    -   [PlugInGamutMapType](#plugingamutmaptype)
    -   [ExtensionType](#extensiontype)
-   [Algoritmos de línea de base de GMMP](#the-gmmp-baseline-algorithms)
-   [Alinear los ejes neutros](#aligning-the-neutral-axes)
    -   [Diferencia de color mínima (picada)](#minimum-color-difference-mincd)
    -   [BasicPhoto](#basicphoto)
    -   [Información general](#overview)
    -   [El caso del shell de una sola gama](#the-case-of-single-gamut-shell)
    -   [Mejora en negro](#black-enhancement)
    -   [El caso de los shells de doble gama](#the-case-of-dual-gamut-shells)
    -   [Motivos de los cambios de las recomendaciones de CIE TC8-03](#reasons-for-changes-from-the-cie-tc8-03-recommendations)
    -   [Asignación de matiz](#hue-mapping)
-   [Descripción de los límites de gama y algoritmos de Shell de gama](#gamut-boundary-description-and-gamut-shell-algorithms)
    -   [Triangulación del límite de la gama](#triangulation-of-the-gamut-boundary)
    -   [Elementos de línea de límite](#boundary-line-elements)
    -   [Operación de gama: CheckGamut](#gamut-operation-checkgamut)
    -   [Plano de matiz completo: Intersect](#full-hue-plane-intersect)
    -   [Operación de gama: CheckGamut (continuación)](#gamut-operation-checkgamut-continued)
    -   [Asignación mínima de gama de diferencias de color](#minimum-color-difference-gamut-mapping)
    -   [Suavizado de matiz](#hue-smoothing)
    -   [Configuración de las principales y secundarias en la descripción del límite de la gama](#setting-primaries-and-secondaries-in-the-gamut-boundary-description)
    -   [Establecimiento del eje neutro en la descripción del límite de la gama](#setting-the-neutral-axis-in-the-gamut-boundary-description)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Este esquema se utiliza para especificar el contenido de un perfil de modelo de mapa de gamas (GMMP). En el tema siguiente se describen los algoritmos de línea de base asociados.

El esquema de GMMP básico se compone de información de encabezado común, una referencia opcional a un complemento de modelo de mapa de gamas preferido y etiquetas de extensión.

Además, GMMP proporciona información explícita sobre el modelo de mapa de la gama de destino y proporciona una directiva sobre el modelo de mapa de la gama de reserva de línea de base para usar si el modelo de destino no está disponible. El esquema puede incluir información de extensión privada, pero no incluye ninguna otra información extraña.

## <a name="gamut-map-model-profile-architecture"></a>Arquitectura de Perfil de modelo de mapa de gama

![Diagrama que muestra el perfil del modelo de mapa de la gama.](images/gmmp-image002.png)

El muestreo del espacio de Colorant del dispositivo de salida se realiza repitiendo el Colorants de 0,0 a 1,0 con un paso fraccionario, acumulando todas las combinaciones de cada Colorant en cada paso y, a continuación, convirtiéndolos desde el espacio de Colorant del dispositivo en el espacio de apariencia de color mediante el método DM::D eviceToColorimetricColors seguido del método CAM:: ColorimetricToAppearanceColors. A continuación se describe un ejemplo de cómo hacerlo para RGB.


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



## <a name="generation-of-the-gamut-boundary"></a>Generación del límite de la gama

Hay tres componentes en el límite de la gama: las principales, los ejemplos neutros y los shells. Los primarios se generan tomando las principales del dispositivo y aplicando la transformación DeviceToColorimetric/ColorimetricToAppearance. Los ejemplos neutros se generan mediante el muestreo del espacio de Colorant del dispositivo en el área neutra y la aplicación de la misma transformación. En el caso de tres dispositivos Colorant (RGB o CMY), los ejemplos neutros se definen como que tienen todo el Colorants igual, por ejemplo, R = = G = = B. Para CMYK, los ejemplos neutros se definen como con C = = M = = Y = = 0.

Los factores que influyen en los datos usados para crear el límite de la gama son los ejemplos de datos (solo dispositivos de línea de base) y las condiciones de visualización. El tamaño del paso que se usa para realizar el muestreo completo del espacio Colorant (para monitores y para el shell de plausible) es una constante interna y no está disponible para manipulación externa. Al cambiar las condiciones de visualización, se cambia el comportamiento del modelo de apariencia de color (CAM) y se modifica la forma del límite de la gama, por lo que debe generar un límite de gama vinculado al perfil de condiciones de visualización. Si se usan datos de ejemplo, como en el caso de las impresoras de línea de base y los dispositivos de captura, los ejemplos tendrán muchos efectos en la forma de la gama de referencia y afectarán al comportamiento del propio modelo.

En el caso de los dispositivos de entrada, como cámaras y escáneres, se usan diferentes muestras para generar el shell de referencia y el shell de plausible. El shell de referencia se genera a partir de las medidas usadas para inicializar el modelo de dispositivo. El shell de plausible se genera de forma similar a la ilustración anterior de los dispositivos de salida. La diferencia es que cuando se introduce un destino típico, no se obtienen valores totalmente saturados (donde R, G o B = 255). Debe extrapolar el uso del modelo de dispositivo para calcular esos valores.

## <a name="the-gmmp-schema"></a>El esquema GMMP


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



## <a name="the-gmmp-schema-elements"></a>Los elementos de esquema GMMP

## <a name="gamutmapmodel"></a>GamutMapModel

Este elemento es una secuencia de los siguientes subelementos:

1.  Cadena de perfilename,
2.  DefaultBaselineGamutMapModel,
3.  Cadena de descripción opcional,
4.  Cadena de autor opcional,
5.  PlugInGamutMap opcionales y
6.  ExtensionType opcional.

**Condiciones de validación** : cada subelemento se valida por su propio tipo.

### <a name="namespace"></a>Espacio de nombres

xmlns: GMM = " http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel "

targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel "

### <a name="version"></a>Versión

Versión "1,0" con la primera versión de Windows Vista.

**Condiciones de validación** : 1,0 en Windows Vista. Las versiones &lt; 2,0 también son válidas para admitir cambios no importantes en el formato.

### <a name="documentation"></a>Documentación

Esquema de Perfil de modelo de mapa de gama.

Copyright (C) Microsoft. Todos los derechos reservados.

**Condiciones de validación** : cada subelemento se valida por su propio tipo.

### <a name="defaultbaselinegamutmapmodel-type"></a>Tipo DefaultBaselineGamutMapModel

Tipo UINT

Valores de enumeración:

<dl> "Absoluta picada \_ "  
"Relativo picada \_ "  
"SIG \_ Knee"  
"HueMap"  
</dl>

**Condiciones de validación** : los valores deben coincidir con una de las enumeraciones anteriores.

### <a name="plugingamutmaptype"></a>PlugInGamutMapType

Este elemento es una secuencia de un GUIDType de GUID y cualquier subelemento.

**Condiciones de validación** : el GUID se usa para hacer coincidir el GUID de la dll del complemento de GMM. Hay un máximo de 100.000 subelementos personalizados.

### <a name="extensiontype"></a>ExtensionType

Este elemento es una secuencia opcional de cualquier subelemento.

**Condiciones de validación** : puede haber un máximo de 100.000 subelementos.

## <a name="the-gmmp-baseline-algorithms"></a>Algoritmos de línea de base de GMMP

## <a name="aligning-the-neutral-axes"></a>Alinear los ejes neutros

La mayoría de los algoritmos de asignación de gamas tienen el objetivo de asignar el eje neutro del dispositivo de origen al eje neutro del dispositivo de destino: es decir, el blanco va a blanco, de negro a negro y de gris a gris. Esto se soluciona en parte mediante el escalado de la luminosidad de los colores de origen para que coincida con el intervalo de luminosidad del dispositivo de destino. Pero eso no soluciona completamente el problema.

Es una propiedad física de la mayoría de los dispositivos de imágenes que la cromaticidad del blanco del dispositivo no coincide exactamente con la cromaticidad del dispositivo negro. Por ejemplo, el monitor blanco depende de la suma de las cromaticidad y la luminances relativa de los tres primarios, mientras que el monitor negro depende de la reflectancia de la superficie de la pantalla. La impresora blanca depende de la cromaticidad del papel, mientras que la impresora de color negro depende de la tinta o del tóner utilizado. Un modelo de apariencia que asigna el dispositivo blanco exactamente al eje neutro del espacio de apariencia (croma exactamente igual a cero) no asignará el negro del dispositivo al eje neutro. Dado que el ojo es más sensible a las diferencias cromas, ya que los aumentos de luminosidad, los grises medios se representarán como más cromáticos que el dispositivo negro. (La figura 1 muestra la curvatura de los ejes neutros en dos dimensiones. De hecho, los ejes neutros forman una curva más compleja en tres dimensiones).

Aunque el CAM predice que estos colores neutros del dispositivo aparecerán en color cromático, los observadores reales parecen compensar esto. La mayoría de los usuarios no tienen en cuenta que estos valores neutros de dispositivo son cromáticos. En el caso de la mayoría de los modelos de asignación, por lo tanto, debe seguir asignando neutros de origen a neutros de dispositivo.

Para asignar neutros de origen a neutros de dispositivo, ajuste los límites de la gama de origen y de destino, y cada píxel al aplicar el algoritmo de asignación de gama. En primer lugar, ajuste cada valor en el color de origen para que el eje neutro del dispositivo de origen en la luminosidad del color de origen caiga directamente en el eje neutro del espacio de apariencia. (Vea el lado izquierdo de la figura 1). A continuación, ajuste la descripción del límite de la gama del dispositivo de destino para que cada color del eje neutro del dispositivo de destino en el límite del color del límite de la gama del dispositivo de destino caiga directamente en el eje neutro del espacio de apariencia. (Consulte el lado derecho de la figura 1).

![Diagrama que muestra el gráfico de límite de la gama de origen a la izquierda y el límite de la gama de destino a la derecha.](images/gmmp-image004.png)

**Figura 1** : alineación de los ejes neutros mostrados. Izquierda: ajuste de los puntos de origen en relación con el eje neutro del dispositivo de origen. Right: ajuste de la descripción del límite de la gama de destino en relación con la descripción del límite de la gama de destino.

Tenga en cuenta que ajusta cada valor de píxel de origen en relación con el eje neutro en ese valor de luminosidad. Esto garantiza que los neutros del dispositivo de origen se encuentran en el eje neutro del modelo de apariencia. También puede desplazar todos los demás colores en esa luminosidad en la misma cantidad, de modo que no haya ninguna discontinuidad en la representación de la gama de origen. Tiene que desplazarse por diferentes cantidades en diferentes niveles de luminosidad, ya que los neutros del dispositivo de origen no se representan de igual forma a los distintos niveles de luminosidad. Claramente, esto no es una transformación trivial.

Controlar los valores del dispositivo de destino es un poco más complicado. Inicialmente, se ajusta el límite completo de la gama de destino de manera similar, pero con respecto al eje neutro del dispositivo de destino. Esto se muestra en la figura 1 del lado derecho. Ese ajuste garantiza que los valores de gris de origen se asignarán a los valores de gris de destino. Este es el espacio en el que operan los algoritmos de asignación de gama.

Sin embargo, este espacio no describe con precisión el comportamiento real del dispositivo de destino. Debe invertir la asignación antes de que se entreguen los colores asignados a la gama en el modelo de apariencia y el modelo de dispositivo de destino. Desplazará todos los valores asignados por el contrario del desplazamiento aplicado anteriormente al eje neutro del dispositivo de destino. Esto asigna el eje neutro de destino de nuevo al valor representado originalmente por el CAM. Hace lo mismo para el límite de la gama y para todos los valores intermedios.

![Diagrama que muestra un gráfico para deshacer la alineación del eje neutro del dispositivo de destino.](images/gmmp-image008.png)

**Figura 2** : deshacer la alineación del eje neutro del dispositivo de destino

### <a name="minimum-color-difference-mincd"></a>Diferencia de color mínima (picada)

Versión relativa y absoluta de diferencia de color (picada) equivalente a la intención colorimétrica de ICC.

> [!Note]  
> La GMM picada es adecuada para la asignación de gráficos y líneas gráficas que contienen colores de "logotipo" (tintas puntuales), degradados de color de logotipo con algunos colores fuera de gama y la fase final de transformaciones de prueba. Aunque el GMM picado podría usarse para imágenes fotográficas que están completamente dentro de la gama de destino, no se recomienda para la representación general de imágenes fotográficas. La asignación de colores fuera de la gama a los colores en la superficie de la gama de destino puede dar lugar a artefactos no deseados, como irregularidades de tono o croma en degradados suaves que cruzan el límite de la gama. Se recomienda BasicPhoto para las imágenes fotográficas. Si una imagen fotográfica o de contonalidad requiere una asignación de gama distinta de BasicPhoto, la alternativa debe ser crear un complemento GMM que implemente esa asignación, en lugar de utilizar picado.

 

Los colores en la gama permanecen inalterados. En el caso de los colores fuera de gama, la luminosidad y el croma se ajustan buscando el punto de la gama de destino que tiene la distancia de color mínima de los puntos de entrada fuera de la gama. La distancia del color se calcula en el espacio de JCh. Sin embargo, se pondera la distancia en luminosidad (J) y la distancia en croma (C) o matiz (h) de manera diferente. Una función de peso dependiente de croma se usa para la distancia en luminosidad, de modo que el peso sea menor para el grosor de croma pequeño y mayor para la intensidad de croma grande hasta que se alcance el cromado del umbral, después del cual el peso se mantiene en 1, es decir, el mismo peso como distancia en croma o matiz. Esto sigue el uso recomendado de CMC y CIEDE2000. Hay dos variantes: colorimétrica relativa y colorimétrica absoluta.

**Colorimétrico relativo:** En primer lugar, alinee los ejes neutros de origen y destino tal y como se describió anteriormente. A continuación, recorte el color de origen ajustado al límite de la gama de destino ajustada. (Consulte la figura 4. Asignación de cromas a lo largo de la luminosidad constante). Reajuste los valores del dispositivo de destino tal y como se describió anteriormente. En el caso de un límite de gama de destino monocromo, el recorte de croma significa que el valor de croma (C) se establece en cero (0,0).

**Colorimétrico absoluto:** Esto es similar a la colorimétrico relativa, pero sin la alineación del eje neutro de origen y de destino. El valor de origen se recorta directamente en el eje neutro de destino. Tenga en cuenta que si los límites de la gama de origen y de destino son monocromáticos, el comportamiento es idéntico al de la variante colorimétrica relativa; es decir, se realiza la alineación de los ejes neutros y, a continuación, el croma se recorta a cero. Esto garantiza que se alcanza una salida razonable incluso si los medios y Colorants son significativamente diferentes.

![Diagrama que muestra un gráfico para el recorte picado en la gama ajustada.](images/gmmp-image010.png)

**Figura 3** : recorte picado en la gama ajustada

### <a name="basicphoto"></a>BasicPhoto

### <a name="overview"></a>Información general

BasicPhoto: equivalente al objetivo de ICC preferido, de gráficos o perceptual.

Este algoritmo es una variante de la asignación de luminosidad de sigmoidal dependiente de croma y el escalado de Knee de cúspide (SGCK) descrito por CIE TC8-03 en CIE156:2004. Este algoritmo variante admite descriptores de límite de gama (GBDs) con shells de doble gama; es decir, GBDs con un shell de referencia y un shell de plausible. El algoritmo SGCK, que inicialmente supone que solo hay un shell de gama en el GBD, se basa en el algoritmo de Knee de SIG \_ (Braun 1999), que incorpora la asignación de luminosidad sigmoidal y el escalado de funciones de Knee propuestos por Braun y Fairchild (1999), combinados con la dependencia de croma de GCUSP (Morovic, 1998). Mantiene una constante de matiz percibida, por ejemplo, el ángulo de matiz en jabs corregidos por matiz, y usa una escala de luminosidad de sigmoidal genérica (independiente de la imagen) que se aplica de forma dependiente de croma y una función de Knee del 90 por ciento. La variante escala a lo largo de las líneas de luminosidad constante.

### <a name="the-case-of-single-gamut-shell"></a>El caso del shell de una sola gama

Resulta útil revisar el algoritmo en caso de que los GBDs de origen y destino tengan solo un shell de gama. En este caso, el algoritmo consta de los siguientes cálculos.

En primer lugar, realice la asignación de luminosidad inicial mediante la siguiente fórmula:

![Muestra la fórmula para la asignación de luminosidad inicial.](images/gmmp-image012.png) (1)

donde *j ₒ* es la luminosidad original y *J <sub>R</sub>* es la luminosidad de la reproducción.

![Muestra la segunda fórmula de asignación de luminosidad.](images/gmmp-image014.png) (2)

Cuando el límite de la gama de origen es monocromo, el valor de croma será cero para el límite monocromo debido a la alineación del eje neutro. Esto producirá el caso degenerado, donde C es igual a cero. En este caso, *p <sub>C</sub>* se establece en 1.

*p <sub>C</sub>* es un factor de ponderación dependiente de croma (Morovic, 1998) que depende de la intensidad del color original, mientras que C y *J <sub>S</sub>* son el resultado de la luminosidad original que se está asignando mediante una función sigmoidal.

 

Para calcular *J <sub>S</sub>* (Braun y Fairchild, 1999), se configura primero una tabla de búsqueda de una dimensión (LUT) entre los valores de luminosidad original y de reproducción, en función de una o varias funciones normales acumulativas.

![Muestra una fórmula para calcular J s.](images/gmmp-image016.png) (3)

donde x ₀ y S son la media y la desviación estándar de la distribución normal, respectivamente, y *i* = 0, 1, 2... *m*,*m* es el número de puntos que se usan en LUT. *S <sub></sub>* es el valor de la función acumulativa acumulativa para *i*  / *m* por ciento. Los parámetros dependen de la luminosidad del punto negro de la gama de reproducción y se pueden interpolar a partir de la tabla 1. Para obtener información detallada sobre el cálculo de estos parámetros, vea Braun y Fairchild (1999, p. 391).

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
       53,7
    :::column-end:::
    :::column:::
        56,8
    :::column-end:::
    :::column:::
        58,2
    :::column-end:::
    :::column:::
        60,6
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


**Tabla 1** : cálculo del parámetro de compresión BasicPhoto luminosidad

Para usar S como LUT de asignación de luminosidad ( <sub>LUT</sub> ), primero se debe normalizar en el intervalo de luminosidad de \[ 0100 \] . A continuación, los datos normalizados se escalan en el intervalo dinámico del dispositivo de destino, como se muestra en la ecuación 4, donde *j*<sub>min \ *out*</sub> y *j*<sub>Max \ *out*</sub> son los valores de luminosidad del punto negro y el punto blanco del medio de reproducción, respectivamente.

![Muestra la fórmula de S como LUT de asignación de luminosidad.](images/gmmp-image018.png) (4)

En este momento, se pueden obtener los valores de *j s* de los <sub>LUT</sub> de elementos mediante la interpolación entre los *m* puntos de los valores de *j o '* y *j s* que contiene y el uso de la siguiente ecuación como entrada.

![Muestra la fórmula para obtener los valores de J S.](images/gmmp-image020.png) (5)

J <sub>Minin</sub> es el valor de luminosidad del punto negro del medio original, j <sub>maxin</sub> es el valor de luminosidad del punto blanco del medio original y j <sub>O</sub> es la luminosidad original. Para una referencia posterior, puede indicar mediante la función sigmoidal definida *de la manera* que se describe en la siguiente ilustración 4.

![Diagrama que muestra el gráfico para la asignación de cromas a lo largo de la luminosidad constante.](images/gmmp-image024.png)

**Ilustración 4** : asignación de cromas a lo largo de la luminosidad constante

En segundo lugar, si el límite de la gama de destino es cromático, comprima el croma a lo largo de las líneas de luminosidad constante (l) y realice la compresión como se indica a continuación.

![Muestra la fórmula para realizar la compresión cromada.](images/gmmp-image026.png)  (6)

donde *d* representa la distancia desde *E* en *l*; *g* representa el límite de la gama mediana; *r* representa la reproducción; y *o* la figura 5 original.

![Diagrama que muestra el gráfico para la compresión croma y luminosidad en BasicPhoto.](images/gmmp-image028.png)

**Figura 5** : compresión croma y luminosidad en BasicPhoto

Si el límite de la gama de destino es monocromo, el valor de croma se recorta a cero.

En tercer lugar, utilice un clip picado (descrito anteriormente) para eliminar cualquier error residual.

### <a name="black-enhancement"></a>Mejora en negro

El algoritmo anterior se puede modificar para mejorar el negro cuando el destino es un dispositivo de impresora. El problema tiene que elegir *J <sub>minOut</sub>*, que normalmente no se corresponde con el color más oscuro que puede producir una impresora.

Más concretamente, el color con mayor densidad que se obtiene al colocar las tintas del 100% (o la cobertura máxima posible, si la limitación de GCR/Ink está en vigor), no suele ser "neutral" en el espacio de apariencia del color. Vea la figura 6. En otras palabras, si se usa la luminosidad mínima neutra para el dispositivo de destino, el Scaler de luminosidad construido se asignará a una luminosidad mínima que no sea la densidad más alta que pueda alcanzar la impresora. Considere el caso de uso adicional de monitor en la impresora. El monitor Black, R = G = B = 0, se imprimirá como no la densidad más alta. El impacto en la calidad de la imagen es que hay una falta de profundidad y de contraste.

![Diagrama que muestra cómo el punto negro del dispositivo puede ser más oscuro que la luminosidad mínima neutra.](images/gmmp-seqfigure01.png)

**Figura 6** : el punto negro del dispositivo puede ser más oscuro que la luminosidad mínima neutra.

Supongamos que el "punto negro del dispositivo" de destino es Jkakbk/JkCkh k. Si C k no es cero, el punto negro del dispositivo no es neutro con respecto a CAM02. Si utiliza J k para la "luminosidad mínima neutra" de destino en la construcción de la luminosidad Scaler; es decir, establecer

*J <sub>minOut</sub> = JK*

y aplíquelo al shell de la gama de origen para obtener la configuración que se muestra en la figura 7. En la ilustración, el plano de matiz corresponde a h k.

![Diagrama que muestra la luminosidad modificada Scaler con el punto negro del dispositivo de destino.](images/gmmp-seqfigure02.png)

**Figura 7** : geometría mediante la luminosidad modificada Scaler con el punto negro del dispositivo de destino

Para permitir que el algoritmo de compresión de croma subsiguiente continúe, desea alinear los lightnesses máximo y mínimo en los shells de origen y de destino. Esto puede lograrse ajustando el shell de destino entre J <sub>neutralMin</sub> y j k pasando los puntos hacia la izquierda. Además, esta transformación se debe aplicar en todo el espacio de jab, no solo en el plano de matiz correspondiente a h k.

La transformación es

![Muestra la fórmula de la transformación.](images/gmmp-seqfigure03.png)

En la ilustración 8 se muestra el efecto de la transformación.

![Diagrama que muestra el efecto de la luminosidad modificada Scaler con el punto negro del dispositivo de destino.](images/gmmp-seqfigure04.png)

**Figura 8** : geometría mediante la luminosidad modificada Scaler con el punto negro del dispositivo de destino

Después de aplicar el algoritmo de compresión de croma habitual, el punto se debe "desplazar de nuevo", es decir, se debe aplicar la transformación inversa para obtener el color asignado final.

![Muestra la fórmula para la transformación inversa con el fin de obtener el color asignado final.](images/gmmp-seqfigure05.png)

### <a name="the-case-of-dual-gamut-shells"></a>El caso de los shells de doble gama

El objetivo es generalizar la \_ Knee de SIG para el shell de una sola gama en el caso en el que el dispositivo de origen gbd o el dispositivo de destino gbd tiene una estructura de dos Shell. El shell interno se llamará el shell de referencia, mientras que el Shell externo se llamará el shell de plausible. Desea tener en cuenta los siguientes casos.

(a) tanto el GBD de origen como el GBD de destino tienen una estructura de dos shells.

(b) el GBD de origen tiene una estructura de dos shells; el GBD de destino tiene solo un shell.

(c) el GBD de origen tiene solo un shell; el GBD de destino tiene una estructura de dos Shell.

(d) el origen GBD y el GBD de destino tienen solo un shell.

Case (d) es el caso del shell de una sola gama que se analizó anteriormente. En el caso de los casos (a), (b) y (c), puede generalizar el cambio de escala de luminosidad para usar la información adicional de la estructura de Shell dual. En los casos (b) y (c) en los que el origen o el destino solo tienen un shell, se introduce un "Shell de referencia inducida" que se tratará en una sección posterior, "Shell de referencia inducida". El algoritmo general para dos shells se describe para el caso (a). Una vez explicada la construcción del shell de referencia inducida, el algoritmo se puede aplicar también a las mayúsculas y minúsculas (b) y (c). En cuanto a la compresión cromada, la razón de compresión estará determinada por los shells más grandes disponibles. En otras palabras, si el shell de plausible y el shell de referencia están disponibles, se utilizará el shell de plausible. de lo contrario, se utilizará el shell de referencia.

*Escalado de luminosidad generalizada*

La existencia de dos shells para GBD de origen y de destino significa que debe asignar un conjunto de cuatro puntos desde el GBD de origen a un conjunto correspondiente en el GBD de destino.

![Muestra cómo asignar un conjunto de cuatro puntos a un conjunto correspondiente.](images/gmmp-image030.png)

Los subíndices tienen los significados siguientes.

o o r: "original" (origen) o "reproducción" (destino)

mín. o máx.: luminosidad neutra mínima o luminosidad neutra máxima

Pla o Ref: Shell de plausible o shell de referencia

La ordenación en cada Quadruple es también la magnitud relativa esperada de estos puntos.

El mapa de cambio de escala de luminosidad utiliza las mismas dos primeras ecuaciones que el shell único, pero *J S* se define de forma a trozos como se indica a continuación.

![Muestra la fórmula de J S de una manera a trozos.](images/gmmp-image032.png) (7)

En otras palabras, es sigmoidal dentro del shell de referencia y lineal fuera de. Vea la figura 9.

![Diagrama que muestra un gráfico para la función de cambio de escala de luminosidad para dos GBDs de Shell.](images/gmmp-image033.png)

**Figura 9** : función de cambio de escala de luminosidad para dos shells de GBDs

**SHELL DE REFERENCIA INDUCIDA**

Si un GBD tiene un shell y el otro GBD tiene dos shells, debe crear un "Shell de referencia" para GBD con un solo Shell. El shell existente, que se denominará el shell de referencia, se cambiará al "Shell de plausible". De hecho, en realidad no tiene que crear un shell en el espacio de jab completo. Dado que el cambio de escala de luminosidad solo usa *j Max* y *j min*, solo tiene que componer estos valores para el shell de referencia inducida. Hay dos casos, en función de qué GBD tiene dos shells.

Caso 1: el GBD de origen tiene dos shells; el GBD de destino tiene un shell.

Determine el shell de referencia inducida de destino en el eje neutro; es decir, el J <sub>r, \ min, \ Ref</sub> y j <sub>r, \ Max, \ Ref</sub> del shell. Esto se hace mediante el siguiente algoritmo.

![Muestra el algoritmo para determinar el shell de referencia inducida de destino.](images/gmmp-induced01.png)

¿Los factores? ¿ <sub>bajo</sub> y? control <sub>alto</sub> la separación entre el shell de plausible y el shell de referencia. Un valor de 1 significa que los valores J <sub>min</sub> o j m ₐ ₓ coinciden. Sus valores se "inducidan" desde el shell de referencia de origen y el shell de plausible de origen.

![Muestra la fórmula para los valores del shell de referencia de origen y el shell de plausible de origen.](images/gmmp-induced02.png)

Los "factores fudges" F <sub>Low</sub> y f <sub>High</sub> son *parámetros ajustables* que deben estar entre 0 y 1. Si el valor es 0, el ₓ de J <sub>min</sub> o j m ₐ se provoca directamente en los shells de origen. En este caso, elija F <sub>Low</sub> = 0,95 y f <sub>High</sub> = 0,1.

Caso 2: el GBD de origen tiene un shell; el GBD de destino tiene dos shells.

Determine el shell de referencia inducida de origen en el eje neutro; es decir, las J <sub>o, \ min, \ Ref</sub> y J <sub>o, \ Max, \ Ref</sub> del shell. Esto se hace mediante el siguiente algoritmo.

![Muestra el algoritmo para determinar el shell de referencia inducida de destino en el eje neutro.](images/gmmp-induced03.png)

De nuevo, ¿los factores? ¿ <sub>bajo</sub> y? control <sub>alto</sub> la separación entre el shell de plausible y el shell de referencia. Un valor de 1 significa que los valores J <sub>min</sub> o j m ₐ ₓ coinciden. Sus valores se "inducidan" desde el shell de referencia de origen y el shell de plausible de origen:

![Muestra el algoritmo para controlar la separación entre el shell de referencia y el shell de plausible de origen.](images/gmmp-induced04.png)

### <a name="reasons-for-changes-from-the-cie-tc8-03-recommendations"></a>Motivos de los cambios de las recomendaciones de CIE TC8-03

BasicPhoto difiere de las recomendaciones de CIE TC8-03 de las siguientes maneras.

1.  Croma no se comprime hacia la cúspide, sino a lo largo de líneas de luminosidad constante.
2.  El intervalo de luminosidad usa la luminosidad del color más oscuro de la gama en lugar del punto en el que el límite de la gama cruza el eje neutro.
3.  BasicPhoto admite un shell de gama de referencia y un shell de gama de plausible, si alguno de los límites de las gamas de la transformación tiene dos shells.
4.  BasicPhoto usa CIECAM02; en lugar de usar CIECAM97s para convertir a D65 en 400 cd/m2 y, a continuación, usar el espacio de colores de RIT IPT.

El primer cambio se realizó para evitar problemas de inversión de tono que se pueden producir al usar la compresión hacia una cúspide. Como se muestra en la figura 10, la compresión de cúspide puede producir inversiones de tono. Esto puede ocurrir cuando los colores de intensidad de croma alto son más claros que los colores de intensidad de color inferior. Dado que SGCK comprime cada píxel independientemente en cuanto a luminosidad y croma, no se garantiza que conserve la relación de luminosidad entre los valores de píxel después de la compresión. El inconveniente conocido de esta decisión de comprimir las líneas de luminosidad constante es que puede sufrir pérdidas de cromas, en particular en áreas en las que el límite de la gama de destino es muy plano, como sucede con los amarillos brillantes.

![Diagrama que muestra la inversión de tono causada por SGCK.](images/gmmp-toneinversion.png)

**Figura 10** : inversión de tono causada por SGCK

![Muestra una imagen original de un tetera.](images/originalteapot.jpg)![Muestra el resultado de SGCK de la imagen de tetera.](images/badteapot.jpg)![Muestra el resultado de BasicPhoto de la imagen de tetera.](images/betterteapot.jpg)

**Figura 11** : imagen original, resultado de SGCK y resultado de BasicPhoto

En la figura 11 se muestra esta inversión de tono. A la izquierda hay una imagen original capturada por una cámara digital. en el centro, la imagen la reproduce SGCK; y a la derecha, la imagen tal como la reproduce BasicPhoto. La imagen de la izquierda está en el espacio de colores de la cámara digital, las imágenes central y derecha se encuentran en el espacio de colores de una pantalla de vídeo LCD. En la imagen original, la parte superior del tetera es más oscura que la parte inferior, porque la parte inferior refleja el mantel en el que está sentado. En la imagen SGCK, la parte superior es realmente más clara que la parte inferior, debido a la inversión de tono. Además, es difícil ver los elementos reflejados en la parte inferior de tetera. A la derecha, BasicPhoto ha corregido la inversión de tono y los artículos reflejados son más claramente distinguibles.

El segundo cambio se realizó para mejorar la reproducción de colores casi negros en impresoras en las que el negro más negro no se encuentra directamente en el eje neutro CIECAM02. En la ilustración 12 siguiente se muestra una imagen convertida en sRGB; se reproduce para una impresora de inyección de tinta RGB mediante SGCK; y se reproducen para la misma impresora mediante BasicPhoto. La imagen en el centro no está usando el dispositivo completo en negro, por lo que no tiene el contraste que se ha encontrado en el original. El contraste se restaura con BasicPhoto.

![Muestra la imagen original de un playset.](images/playstructure.jpg)![Muestra la imagen del PLAYSET reproducido para una impresora de inyección de tinta de R G B con SGCK.](images/playstructurebad.jpg)![Muestra la imagen del PLAYSET reproducido para una impresora de inyección de tinta de R G B con BasicPhoto.](images/betterplaystructure.jpg)

**Figura 12** : negro mejorado

El tercer cambio se realizó para mejorar la reproducción de color de las cámaras digitales. En particular, en los casos en los que se ha generado un perfiles de la cámara digital mediante un destino de referencia, una descripción de límite de gama creada a partir de colores medidos podría no incluir todos los colores que podrían capturarse en una escena real. En lugar de recortar todos los colores a la gama del objetivo de color medido, permite que la extrapolación genere un límite de gama plausible. El algoritmo BasicPhoto está diseñado para admitir este tipo de límite de gama extrapolada.

El cuarto cambio se realizó porque CIECAM02 funciona bien para la asignación de gamas. El proceso recomendado por TC8-03 de convertir los colores del dispositivo en D65 en 400 cd/m2 y, a continuación, usar el espacio de colores de RIT IPT es el que consume mucho tiempo.

### <a name="hue-mapping"></a>Asignación de matiz

HueMap es el equivalente de la intención de saturación de ICC.

Si el límite de la gama de origen o el límite de la gama de destino no contiene los primarios, este modelo se revierte al modelo picado (relativo) descrito en la sección anterior; por ejemplo, los dispositivos para los que no se pueden determinar los primarios (perfiles ICC con más de cuatro canales) o los perfiles ICC monocromo.

Este algoritmo ajusta primero el matiz del valor del color de entrada. A continuación, ajusta simultáneamente la luminosidad y croma mediante una asignación de recorte. Por último, recorta el valor de color para asegurarse de que está dentro de la gama.

El primer paso es determinar las "ruedas de matiz". Busque los valores de JCh para los colores primario y secundario para el dispositivo de origen y de destino. Solo está pensando en los componentes de matiz. Esto da como resultado una rueda de matiz principal o secundaria con seis puntos de color para cada dispositivo. (Consulte la figura 13).

![Diagrama que muestra las ruedas de matiz con seis puntos de color.](images/gmmp-figure12.png)

**Figura 13** : ruedas de matiz

Se pueden obtener mejores resultados si el principal azul de origen no se gira a la principal azul de destino. En su lugar, se usa el ángulo de matiz principal azul de origen como el ángulo de matiz principal azul de destino.

A continuación, realice las rotaciones de matiz para cada color de entrada de la imagen de origen.

a) usar el ángulo de matiz del color de entrada, determine la ubicación del color en la rueda de matiz de origen en relación con los dos colores primarios o secundarios adyacentes. La ubicación se puede considerar como un porcentaje de la distancia entre las principales. Por ejemplo, el matiz del color de entrada es 40 por ciento de la forma del valor de matiz de magenta al valor de matiz de rojo.

b) en la rueda de matiz de destino, busque el ángulo de matiz asociado, por ejemplo, 40 por ciento de fucsia a rojo. Este valor será el ángulo de matiz de destino.

En general, las principales y secundarias de origen no estarán en los mismos ángulos de matiz que las principales y secundarias de destino. es decir, el ángulo de matiz de destino normalmente será diferente del ángulo de matiz de origen.

Por ejemplo, suponga que las ruedas de matiz producen los valores siguientes:

Origen M = 295 grados, R de origen = 355 grados.

Destino M = 290 grados, destino R = 346 grados.

Si el ángulo de matiz del color de entrada es de 319 grados, es 40 por ciento del ángulo (24 grados) del origen M al origen R. El ángulo de M a R es 60 grados y el ángulo de M a matiz de entrada es de 24 grados. Calcule el ángulo del destino que es 40 por ciento del destino M al destino R (22 grados), por lo que el ángulo de matiz del color de destino es de 312 grados.

A continuación, calcule los puntos de referencia de matiz para el matiz de origen y el matiz de destino. Para calcular el punto de referencia de matiz para un valor de h (matiz) determinado, desea buscar el valor de J (luminosidad) y el valor de C (croma).

-   Busque el valor J del punto de referencia Hue mediante la interpolación entre los valores J de los puntos primarios o secundarios adyacentes, utilizando la posición relativa del matiz; por ejemplo, 40 por ciento en este ejemplo.
-   Busque el valor de C máximo en este valor J y el valor h. Ahora tiene el JCh del punto de referencia de matiz para ese matiz.

![Diagrama que muestra una hoja de matiz.](images/gmmp-figure13.png)

**Figura 14** : una hoja de matiz (visualización de un segmento de límite de gama en un matiz específico)

El siguiente paso consiste en calcular la asignación de recorte para cada píxel. En primer lugar, visualice una hoja de matiz de la gama de origen para el ángulo de matiz del color de origen y una hoja de matiz de la gama de destino para el ángulo de matiz de destino calculado durante la rotación del matiz. Las hojas de matiz se crean tomando un "segmento" de la superficie del límite de la gama JCh en un ángulo de matiz específico (consulte la figura 14).

Nota: por motivos de optimización del rendimiento, no se crean realmente las hojas de matices. se describen y se muestran aquí solo con fines de visualización. Las operaciones se realizan directamente en la superficie del límite de la gama en el matiz especificado. A continuación, calcula los puntos de referencia de matiz para determinar la asignación de recorte.

-   Realice un cambio de escala de luminosidad para asignar los puntos negros y blancos de la hoja de origen a la hoja de destino (vea la figura 15). Los puntos negros y blancos de la hoja matiz de origen se asignan linealmente a los puntos blanco y negro de la hoja matiz de destino, mediante el escalado de todas las coordenadas J del límite de origen. El valor del color de entrada asignado al matiz se escala de la misma manera.

![Diagrama que muestra la asignación de luminosidad.](images/gmmp-figure14.png)

**Figura 15** : asignación de luminosidad

-   Determine los puntos de referencia de matiz para cada hoja de matiz. Aplique una asignación de recorte a la hoja de origen para que los puntos de referencia de origen y destino coincidan (vea la figura 16). El punto de referencia de una gama en un matiz específico es el punto de referencia de matiz interpolado entre las principales adyacentes. El punto de referencia de la hoja de matiz de origen se asigna linealmente al punto de referencia de la hoja de matiz de destino, mediante una operación de "recorte" que bloquea el eje J, manteniendo los puntos negros y los puntos blancos. Los puntos negros, los puntos blancos y los puntos de referencia de las hojas de matiz de origen y de destino deben coincidir.
-   Aplique la asignación de recorte al valor del color de entrada con ajuste de luminosidad. Las coordenadas J y C del valor de color de origen se escalan proporcionalmente, con respecto a su distancia desde el eje J.
-   A continuación, se realiza una compresión sutil de luminosidad dependiente de croma hacia el valor J del punto de referencia de matiz en el punto de color asignado a distorsión. La compresión para la referencia de matiz J se realiza de forma gamma, en la que la referencia de matiz J no se ve afectada. Todos los demás puntos tienden a la referencia de matiz J de un modo suave, lo que se aproxima ligeramente a la referencia de matiz J, con la constante de croma restante. La dependencia de croma garantiza que los colores neutros no se ven afectados y el efecto se incrementa en los colores con intensidad de color superior.

A continuación se describe una descripción matemática de la compresión de luminosidad hacia la referencia de matiz J o el ajuste del valor J del punto de destino. Se denomina punto de destino porque se ha recortado en la gama de destino.

En primer lugar, Compute "factorC" (factor de dependencia de croma) para el punto de destino, que determina cuánto efecto tendrá la compresión de luminosidad. Los puntos cercanos o en el eje J tendrán poca o ninguna compresión; los puntos más alejados del eje J (alta intensidad) tendrán más compresión aplicada. Multiplique por 0,5 para asegurarse de que factorC es menor que 1, ya que es posible que sourceC pueda ser ligeramente mayor que referenceC, pero no dos veces más grande.

factorC = (destinationC/referenceC)? 0,5

donde:

destinationC es el valor de C del punto de destino.

referenceC es el valor de C del punto de referencia de matiz.

A continuación, determine si el punto de destino J está por encima o por debajo de la referencia de matiz J. Si es anterior, haga lo siguiente:

1.  Compute "factorJ" para el punto de destino relativo a referenceJ. Este valor factorJ estará entre 0 y 1 (0 si está en referenceJ; 1 si está en maxJ).
2.  factorJ = (destinationJ-referenceJ)/(maxJ-referenceJ)

    donde:

    destinationJ es el valor J del punto de destino.

    referenceJ es el valor J del punto de referencia de matiz.

    maxJ es el valor J máximo de la gama.

3.  Aplique una función de potencia de tipo gamma a factorJ, lo que reducirá el valor de factorJ en una cantidad determinada. En este ejemplo se usa la potencia de 2 (el cuadrado). Reste el factorJ reducido de la factorJ original y multiplique el resultado por el total de J-intervalo por encima del referenceJ principal para encontrar el "deltaJ", que representa el cambio en J después de la compresión de luminosidad, pero sin incluir la dependencia de croma.
4.  deltaJ = (factorJ-(factorJ? factorJ)) ? (maxJ - referenceJ)

5.  Aplique factorC a deltaJ (cuanto mayor sea el croma, mayor será el efecto) y calcule el nuevo valor J para el punto de destino.
6.  destinationJ = destinationJ-(deltaJ? factorC)

Si el valor J del punto de destino es inferior a referenceJ, se realiza un cálculo similar en los pasos anteriores a-C, utilizando minJ en lugar de maxJ para encontrar el intervalo en J para calcular el factorJ, y teniendo en cuenta la polaridad de las operaciones "debajo" de la referenceJ.

factorJ = (referenceJ-destinationJ)/(referenceJ-minJ)

deltaJ = (factorJ-(factorJ? factorJ)) ? (referenceJ - minJ)

destinationJ = destinationJ + (deltaJ? factorC)

donde:

minJ es el valor J mínimo de la gama.

La intensidad de los puntos de color de entrada se expande linealmente (cuando es posible) a lo largo de la luminosidad constante proporcional al valor de croma máximo de las gamas de origen y de destino en ese matiz y luminosidad. Combinado con la compresión de luminosidad dependiente del cromada anterior, esto ayuda a preservar la saturación, ya que la asignación de recorte mediante los puntos de referencia a veces hace que el punto de origen supere la compresión en croma (vea la figura 16).

![Diagrama que muestra la asignación de recorte para coincidir con los puntos de referencia de matiz, antes del recorte a la izquierda, después de distorsionar a la derecha.](images/gmmp-shearmapping.png)

**Figura 16** : asignación de recorte, compresión de luminosidad hacia la referencia de matiz J y expansión de croma

A continuación se describe una descripción matemática del proceso de expansión de croma o el ajuste del valor de C del punto de destino. Se denomina punto de destino porque se ha distorsionado el mapa y la luminosidad comprimidos en la gama de destino.

1.  Antes de la asignación de recorte, determine sourceExtentC (la extensión de croma en la luminosidad y el matiz del punto de origen).
2.  Después de la compresión de sesgo y de la asignación de recorte que transforma el punto de origen en el punto de destino, determine el destExtentC (la extensión de croma en la luminosidad y el matiz del punto de destino).
3.  Si el sourceExtentC es mayor que destExtentC, no es necesario realizar ningún ajuste de croma en el punto de destino y puede omitir el paso siguiente.
4.  Ajuste destinationC (intensidad del punto de destino) para que quepa en la extensión de croma de destino en esta luminosidad y matiz.
5.  destinationC = destinationC? (destExtentC / sourceExtentC)

    donde:

    destinationC es el valor de C del punto de destino.

    sourceExtentC es el valor máximo de C de la gama de origen en la luminosidad y el matiz del punto de origen.

    destExtentC es el valor de C máximo de la gama de destino en la luminosidad y el matiz del punto de destino.

Por último, realice el recorte de distancia mínimo. Si el color de entrada con rotación de matiz, ajuste de luminosidad y asignado a distorsión está todavía ligeramente fuera de la gama de destino, recorte (muévalo) al punto más cercano del límite de la gama de destino (consulte la figura 17).

![Diagrama que muestra el recorte de distancia mínimo.](images/gmmp-figure15.png)

**Figura 17** : recorte de distancia mínimo

## <a name="gamut-boundary-description-and-gamut-shell-algorithms"></a>Descripción de los límites de gama y algoritmos de Shell de gama

La función de límite de gama de dispositivos usa el motor de modelo de dispositivo y los parámetros analíticos para derivar un límite de gama de dispositivos de color, que se describe como una lista de vértices indexados del casco de la gama de dispositivos. El casco se calcula de forma diferente en función de si está trabajando con dispositivos aditivos, como monitores y proyectores, o dispositivos de sustracción. La lista de vértices indizada se almacena en CIEJab. La estructura de la lista de vértices indizada está optimizada para la aceleración de hardware de DirectX.

Este enfoque tiene muchas soluciones conocidas. Si busca "DirectX de casco convexo" en la web, obtendrá más de 100 aciertos. Por ejemplo, hay una referencia de 1983 en este tema específico (teoría y aplicación de los gráficos del equipo, "Shiphulls, las superficies de la spline b y CADCAM 34-49", con referencias de 1970 a 1982 en el tema.

La colección de puntos se puede determinar a partir de información disponible externamente, como se indica a continuación:

-   Los puntos del shell de referencia para los monitores se generan mediante un muestreo del cubo de color en el espacio de dispositivo Colorant.
-   Los puntos del shell de referencia para impresoras y dispositivos de captura se obtienen de los datos de ejemplo que se usan para inicializar el modelo.
-   Los puntos del shell de referencia para scRGB y sRGB se generan mediante un muestreo del cubo de color para sRGB.
-   Los puntos para el shell de plausible para dispositivos de captura se generan mediante un muestreo del cubo de color en el espacio de dispositivo Colorant.
-   Los puntos del shell de referencia para los proyectores se generan mediante un muestreo de un polyhedron en el cubo de color en el espacio de dispositivo Colorant.
-   Los puntos del posible Shell para los espacios de colores de rango dinámico anchos se generan mediante un muestreo del cubo de color en el propio espacio.

Puede crear una lista de vértices que describa de forma eficaz la gama de colores del dispositivo, dados un perfil de dispositivo y servicios de soporte del sistema.

En el caso de los dispositivos de salida, el límite de la gama describe el intervalo de colores que puede mostrar el dispositivo. Un límite de gama se genera a partir de los mismos datos que se usan para modelar el comportamiento del dispositivo. Conceptualmente, se genera un muestreo del intervalo de colores que el dispositivo puede producir, se miden los colores, se convierten las medidas en el espacio de apariencia y, a continuación, se usan los resultados para crear el límite de la gama.

Los dispositivos de entrada son más complicados. Cada píxel de una imagen de entrada debe tener algún valor. Cada píxel debe ser capaz de representar cualquier color que se encuentre en el mundo real de alguna manera. En este sentido, no hay ningún color "fuera de la gama" para un dispositivo de entrada, porque siempre se pueden representar.

Todos los formatos de imagen digital tienen algún intervalo dinámico fijo. Debido a esta limitación, siempre hay algunos estímulos distintos que se asignan al mismo valor digital. Por lo tanto, no se puede establecer una asignación de uno a uno entre los colores del mundo real y los valores de cámara digital. En su lugar, el límite de la gama se forma mediante la estimación de una gama de colores del mundo real que pueden generar las respuestas digitales de la cámara. El intervalo Estimado se usa como gama para el dispositivo de entrada.

Se incluyen principales para proporcionar la asignación de gama de tipos de calidad de gráficos empresariales.

En un estilo real orientado a objetos, se abstrae la representación subyacente del límite de la gama. Esto le permite la flexibilidad de cambiar la representación en el futuro. Para comprender el descriptor de límite de gama (GBD) que se usa en la nueva CTE, primero debe comprender cómo funcionan los algoritmos de asignación de gamas (GMAs). Tradicionalmente, GMAs se han diseñado para satisfacer las necesidades de la comunidad de arte gráfico; es decir, para reproducir imágenes que ya se han representado correctamente para el dispositivo en el que se creó la imagen de entrada. El objetivo de GMAs de arte gráfico es hacer la mejor reproducción posible de la imagen de entrada en el dispositivo de salida. La nueva CTE GBD está diseñada para resolver cuatro problemas clave.

Dado que la imagen de entrada se representa para el dispositivo de entrada, todos los colores caben en el intervalo entre el punto blanco y el punto negro del medio. Supongamos que la imagen es una fotografía de una escena en la que hay un blanco difuso, como una persona de una camiseta en blanco y un resaltado especular, como la luz que refleja un golpe de ventana o de cromo. La escena se representará en el medio de entrada para que el resaltado especular se asigne al punto blanco del medio y el blanco difuso se asigne a un color neutro más oscuro que el punto blanco del medio. La elección de cómo asignar colores de la escena al medio de entrada es tanto una decisión dependiente de la escena como una decisión estética. Si falta el resaltado especular de la escena original, el blanco difuso probablemente se asignará al punto blanco del medio. En una escena con muchos detalles de resaltado, se deja más intervalo entre el blanco especular y el blanco difuso. En una escena en la que el resaltado no es significativo, es posible que se deje un intervalo muy pequeño.

En el caso de las imágenes previamente representadas, la asignación de gamas es relativamente sencilla. Básicamente, el punto blanco del medio original se asigna al punto blanco del medio de reproducción, el punto negro de origen se asigna al punto negro de destino y la mayor parte de la asignación se ha completado. Los diferentes GMAs en existencia proporcionan variaciones para asignar otros puntos en la escala de tono del medio de origen y diferentes maneras de administrar los valores de croma fuera de la gama. Pero la asignación de blanco a blanco y de negro a negro es coherente a lo largo de estas variaciones. Esta implementación requiere que el blanco esté por encima de un J \* de 50 y negro por debajo de un j \* de 50.

No todas las codificaciones de color limitan los rangos de colores de las imágenes de entrada. El scRGB de codificación de color estándar IEC (IEC 61966-2-2) proporciona 16 bits para cada uno de los tres canales de color rojo, verde y azul (RGB). En esa codificación, el negro de referencia no se codifica como el triple RGB (0,0, 0), sino como (4096, 4096, 4096). El blanco de referencia se codifica como (12288, 12288, 12288). La codificación scRGB se puede usar para representar los reflejos especulares y los detalles de la sombra. Incluye tripas RGB que no son posibles físicamente porque requieren cantidades negativas de luz y codificaciones que están fuera del raíz espectral de CIE. Claramente, ningún dispositivo puede producir todos los colores de la gama scRGB. De hecho, ningún dispositivo puede producir todos los colores que puede ver un usuario. Por lo tanto, los dispositivos no pueden rellenar la gama scRGB y resultaría útil poder representar la parte de la gama que rellenan. Cada dispositivo tiene un intervalo de valores en el espacio scRGB que puede generar. Estos son los colores "esperados" para el dispositivo; sería sorprendente que el dispositivo generara colores fuera de esta gama. Hay una transformación definida desde el espacio scRGB al espacio de apariencia, por lo que cada dispositivo también tiene un intervalo de valores de apariencia que se espera que reproduzca.

Tanto en el scRGB como en los datos de entrada de los dispositivos de captura que se caracterizan por un destino fijo, es posible obtener un valor fuera del intervalo de valores esperados. Si alguien calibra una cámara en un destino de prueba; y después captura una escena con reflejos especulares, puede haber píxeles más brillantes que el punto blanco del destino. Lo mismo puede suceder si una situación roja que se produce de forma natural es más cromática que la red de destino. Si alguien toma una imagen scRGB desde un dispositivo y, a continuación, edita manualmente los colores de la imagen, es posible crear píxeles que estén fuera del intervalo esperado de la gama de dispositivos, aunque estén dentro de la gama de scRGB completa.

Un segundo problema puede que, al principio, parezca estar relacionado con este. Se produce cuando se usa un destino de color para caracterizar un dispositivo de entrada, como una cámara o un escáner. Normalmente, los objetivos reflectantes se producen en papel y contienen una serie de revisiones de color. Manufaturers proporcionan archivos de datos con medidas de color tomadas en una condición de visualización fija para cada revisión de color. Las herramientas de generación de perfiles de color crean una asignación entre estos valores medidos y los valores devueltos por los sensores de color en los dispositivos. El problema es que a menudo estos destinos de color no cubren toda la gama de valores de dispositivo. Por ejemplo, puede que el escáner o la cámara devuelvan un valor de (253, 253, 253) para el punto blanco de referencia, y una revisión roja de referencia puede tener un valor RGB de (254, 12, 4). Representan el intervalo de valores esperados para el dispositivo de entrada, en función de los valores de destino. Si caracteriza el dispositivo de entrada en función de las respuestas al destino, solo se esperan colores dentro de este intervalo estrecho. Este intervalo no es solo menor que el intervalo de colores que los usuarios pueden ver, es menor que el intervalo de colores que el dispositivo puede producir.

En ambos casos, es difícil calcular la gama de la imagen o el dispositivo de entrada, a pesar de la existencia de una gama de referencia o de medidas. En el primer problema, la gama de plausible del dispositivo de entrada es menor que la gama completa de scRGB. En el segundo problema, la gama de referencia del destino es menor que la gama completa posible del dispositivo de entrada.

El tercer problema implica la asignación de tono. Se han propuesto muchos modelos de límites de gama que pueden representar de forma adecuada imágenes preprocesadas que se usan en la artes gráficas, por ejemplo, Braun y Fairchild Mountain Range GBD (Braun \[ 97 \] ) y el descriptor de límite de nivel máximo del segmento de Morovic (Morovic \[ 98 \] ). Pero estos modelos solo proporcionan información sobre los extremos de la gama del dispositivo; falta información sobre otros puntos en la asignación tonal. Sin esta información, GMAs solo puede hacer estimaciones aproximadas de la asignación de tono óptima. Lo que es peor, estos modelos no proporcionan ayuda para el intervalo dinámico extendido en scRGB y en imágenes de cámara digital.

¿Cómo se resuelve este problema en las industrias fotográficas e fotográficas? La cámara captura una imagen. Los expertos pueden debatir la cantidad de representación que se produce en el dispositivo de captura; pero aceptan que no es una cantidad significativa. Ambas tecnologías no asignan un blanco difuso en una escena capturada al punto blanco del medio. Del mismo modo, no asignan el punto negro de la escena al punto negro del medio. El comportamiento de la película fotográfica se describe en el espacio de densidad mediante una curva de característica, que a menudo se denomina "Lesionator" y "&Driffield". La curva muestra la densidad de la escena original y la densidad resultante de la película. En la figura 18 se muestra una curva de H&D típica. El eje x representa un aumento de la exposición del registro. El eje y representa la densidad de la diapositiva. Se han marcado cinco puntos de referencia en la curva: negro sin detalles, que representa la densidad mínima en el negativo; negro con detalle; tarjeta gris de referencia: blanco con detalle; y blanco sin detalles. Tenga en cuenta que hay espacio entre el negro sin detalles (que representa el dispositivo negro) y el negro con detalles (sombra negra). Del mismo modo, hay espacio entre blanco y detalle (blanco difuso) y blanco sin detalles (que representa el dispositivo blanco).

![Diagrama que muestra la curva H y D de la película de diapositivas.](images/gmmp-image079.png)

**Figura 18** : curva de H&D para la película de diapositivas

El sector del vídeo proporciona "espacio" y "footroom" en las imágenes. En la especificación ITU 709, la luminancia (llamada Y) se codifica en 8 bits, con un intervalo de 0 a 255. Sin embargo, el negro de referencia se codifica en 15 y el blanco de referencia se codifica como 235. Esto deja el intervalo de codificación entre 236 y 255 para representar los reflejos especulares.

El sector del vídeo presenta un sistema de bucles prácticamente cerrado. Aunque hay muchos proveedores de equipos distintos, los sistemas de vídeo se basan en dispositivos de referencia. Hay una codificación estándar para imágenes de vídeo. No es necesario comunicar un límite de gama con imágenes de vídeo, ya que todas las imágenes se codifican para su reproducción en el mismo dispositivo de referencia. La película también está cerrada porque no es necesario transmitir datos intermedios entre distintos componentes. Desea una solución que permita la reproducción de imágenes desde dispositivos con diferentes gamas y que representen escenas predefinidas y no representadas que se reproduzcan en la salida con distintas gamas.

Un cuarto problema que debe resolver la nueva CTE es que los colores visualmente grises generados por un dispositivo, por ejemplo, cuando el color rojo = verde = azul en un monitor, no se encuentran en el eje neutro del CAM (cuando el croma = 0,0). Esto produce grandes dificultades para GMAs. Para que los GMAs funcionen bien, tiene que ajustar la descripción de la gama del dispositivo y de los puntos de entrada para que el eje neutro del dispositivo se encuentre en el eje neutro del espacio de apariencia. Debe ajustar los puntos fuera del eje neutro en una cantidad similar. De lo contrario, no puede hacer degradaciones suaves a través de la imagen. En lo que se refiere al sistema GMA, deshacer esta asignación con respecto al eje neutro del dispositivo de salida. Esto se conoce como una enderezación "quiropráctico" del eje. Al igual que un CHIROPRACTOR, no solo se endereza el esqueleto (eje neutro), sino que se ajusta el resto del cuerpo para moverlo junto con el esqueleto. Al igual que un CHIROPRACTOR, no ajuste el esqueleto en la misma cantidad en todo el espacio. En su lugar, las diferentes secciones se ajustan de forma diferente.

![Diagrama que muestra la curvatura del eje neutro del dispositivo con respecto al eje neutro CIECAM.](images/gmmp-image081.png)

**Figura 19:** Curvatura del eje neutro del dispositivo con respecto al eje neutro de CIECAM

Lo que requiere la nueva CTE es un modelo de un límite de gama que se puede usar para representar imágenes de origen representadas y no representadas, proporcionar información sobre la apariencia de los neutros del dispositivo y proporcionar información para las imágenes de asignación de tono con un rango de luminancia ancho.

![Diagrama que muestra los shells de tres gamas.](images/gmmp-image083.png)

**Figura 20** : shells de tres gamas

El límite de la gama se compone de tres shells que definen tres regiones.

En la nueva CTE, el shell exterior de la gama está formado por un casco convexo que se realiza a partir de puntos de ejemplo en la gama de dispositivos. Un casco se forma tomando un conjunto de puntos de ejemplo y rodeados por una superficie. Un casco convexo tiene la propiedad adicional de convexo en todas partes. Por lo tanto, este no es el casco más pequeño posible que pueda ajustarse a los datos. Pero la experimentación ha demostrado que la conexión de los puntos de ejemplo es demasiado estricta y que los artefactos de las imágenes no resultan atractivos, como la falta de un sombreado suave. El casco convexo parece resolver estos problemas.

En el algoritmo, los valores de apariencia de color se obtienen para un conjunto de puntos muestreados desde el dispositivo. En el caso de monitores e impresoras, los valores de apariencia de color se obtienen mediante la salida de ejemplos y su medición. También puede crear un modelo de dispositivo y, a continuación, ejecutar datos sintéticos a través del modelo de dispositivo para predecir valores medidos. Después, los valores medidos se convierten de un espacio colorimétrico (XYZ) al espacio de apariencia (jab) y el casco se ajusta alrededor de los puntos.

El punto clave de este algoritmo es que el punto blanco adoptado en la conversión de colorimétrico al espacio de la apariencia no tiene que ser el punto blanco del medio. En su lugar, puede seleccionar un punto más alejado dentro de la gama y en (o cerca) el eje neutro. Ese punto tendrá un valor J de 100. Los ejemplos con un valor Y medido más alto que el punto blanco adoptado terminarán con un valor de J mayor que 100.

Si coloca el punto blanco difuso de la escena como el punto blanco adoptado para la conversión del espacio de colores, los resaltes especulares de la escena se detectarán fácilmente con un valor de J mayor que 100.

Dado que el modelo de color CIECAM02 se basa en el sistema visual humano, después de seleccionar un blanco adoptado, el modelo determina automáticamente el nivel de luminancia del punto negro (J = 0). Si la imagen de entrada tiene un intervalo dinámico ancho, es posible que haya valores que se asignen a valores J inferiores a cero.

La siguiente figura 21 muestra los neutros de los dispositivos que se ejecutan a través del centro de las gamas de plausible y de referencia.

![Diagrama que muestra el eje neutro del dispositivo agregado al límite de la gama.](images/gmmp-image085.png)

**Figura 21** : eje neutro de dispositivo agregado a límite de gama

Todas las asignaciones de gama implican el recorte de un intervalo de entrada a una gama de salida o la compresión de la gama de entrada para que quepa en la gama de salida. Los algoritmos más complejos se forman comprimiendo y recortar en distintas direcciones, o dividiendo la gama en regiones diferentes y, a continuación, realizando el recorte o la compresión en las distintas regiones.

La nueva CTE amplía este concepto para admitir las regiones de una gama posible, una gama de plausible y una gama de referencia, y permite a GMAs asignarlos de diferentes maneras. Además, los GMAs tienen información sobre el eje neutro del dispositivo. En la siguiente explicación se explica cómo controlar las situaciones en las que las gamas de plausible y las gamas de referencia se han contraído entre sí.

![Diagrama que muestra la G M A con dos descriptores de gama no contraídos.](images/gmmp-image091.png)

**Figura 22** : GMA con dos descriptores de gama no contraídos

Es posible que vea este ejemplo si asigna desde un dispositivo de entrada, como una cámara o escáner que se caracteriza por un destino reflectante, al espacio scRGB. Aquí, los colores de plausible más claros que el blanco de referencia son reflejos especulares. En la práctica, la creación de caracteres de una cámara con un destino podría no generar el intervalo completo de valores posibles en la cámara; sin embargo, los reflejos especulares y los colores muy cromáticos que se encuentran en la naturaleza. (Los destinos transcartados suelen tener una revisión que es la densidad mínima posible en el medio. Con este tipo de destino, los reflejos especulares se encuentran dentro del intervalo del destino. El negro de referencia de un destino reflectante sería el principio de la región de color negro de la sombra. Es decir, es probable que haya colores en las sombras más oscuras que el negro del destino. Si la imagen contiene una gran cantidad de contenido interesante en esa región, es posible que merezca la pena conservar esa variación tonal.

![Diagrama que muestra la G M A con una gama de destino contraída.](images/gmmp-image095.png)

**Figura 23** : GMA con una gama de destino contraída

En la Figura 23 se muestra un posible algoritmo de asignación de gamas cuando la gama de destino solo proporciona el intervalo del dispositivo blanco a negro y no hay ningún posible número de colores fuera de esta gama. Lo más probable es que se produzca para dispositivos de salida típicos, como las impresoras. Los colores posibles se asignan al borde de la gama de destino. Pero carece de una curva de tono para el dispositivo de salida. El GMA debe seleccionar algún punto neutro de luminancia inferior para usarlo como destino de asignación para el blanco de referencia. Un algoritmo sofisticado puede hacer esto histogramming el lightnesses en la imagen de origen y observando cuántos se encuentran en el intervalo de espera, pero más claro que el blanco de referencia. Cuanto mayor sea el número de lightnesses, más espacio se necesita en el dispositivo de destino entre los puntos asignados para los resaltados especulares y el blanco de referencia. Un algoritmo más sencillo podría elegir una distancia arbitraria hacia abajo de la escala de luminosidad desde el dispositivo blanco, como un 5 por ciento. Se aplica un enfoque similar para la asignación de los valores negros máximo y negro.

Después de generar la curva de tono de destino, puede asignar un método similar al que se usa en la Figura 23 anterior. Todos los puntos de la curva de tono de destino se encontrarán dentro de la gama de dispositivos y todos los puntos de la asignación deben estar dentro de la gama de dispositivos.

Si revierte las figuras de la izquierda y la derecha, y las direcciones de las flechas de la Figura 23, puede describir el caso en el que la imagen de origen tiene solo una gama de referencia y las tres gamas del dispositivo de salida no se contraen entre sí. Un ejemplo de esto podría ser la asignación de un monitor a scRGB. De nuevo, el GMA debe sintetizar los puntos de control de los cinco puntos de la curva de tono de la imagen de origen. Algunas asignaciones pueden colocar todos los puntos de la curva de tono dentro de la gama de dispositivos scRGB, mientras que otras asignaciones podrían usar más de la gama de scRGB asignando el blanco difuso al blanco de referencia y permitiendo que el blanco especular se asigne a un valor más claro.

Por último, tiene el caso en el que ambos dispositivos tienen solo la gama de referencia, que es la forma en que funcionan la mayoría de los algoritmos de asignación. Por lo tanto, puede resolverlo simplemente volviendo a los algoritmos actuales. Como alternativa, si tiene una manera razonable de determinar los cinco puntos de referencia para los dispositivos de origen y de destino, puede organizar para asignar los puntos de referencia.

Las gamas de dispositivos contienen más de los cinco puntos de referencia en el eje neutro. Estos solo representan los límites entre las posibles regiones de la imagen. Entre cada uno de los puntos de referencia puede usar cualquiera de las técnicas de asignación de gama existentes. Por lo tanto, puede recortar el intervalo de colores inesperados y comprimir todos los colores entre el blanco y el negro esperados, o puede recortar todos los colores fuera del intervalo de referencia y comprimir dentro de ese intervalo. Hay muchas posibilidades, que se pueden implementar en diferentes GMAs. Además, el GMAs se puede comprimir y recortar de diferentes maneras. Todas estas combinaciones están tratadas dentro de esta invento.

Hasta ahora en este debate, la gama se ha tratado como si solo fuera una función del dispositivo en el que se ha creado, capturado o mostrado la imagen. Sin embargo, no hay ningún motivo por el que todas las imágenes de un dispositivo deben tener la misma gama. GMAs dependen de los datos de GBD. Si se cambia el descriptor entre imágenes, no hay ninguna manera de que el GMAs lo sepa. En concreto, si las imágenes no tienen reflejos especulares, GMAs funcionan mejor si el descriptor de la gama no muestra que hay colores más claros que el blanco difuso.

En la nueva arquitectura de CTE, es posible usar más de un GMA. El uso de varias GMAs se define de forma inherente. Por ejemplo, si un dispositivo de captura asocia un GMA con su "aspecto y funcionamiento", tiende a hacerlo con una gama de destino de "destino". Lo mismo se aplica a los dispositivos de salida y a las gamas de origen "de destino". La gama sRGB es una gama implícita de destino común. Por lo tanto, se recomienda encarecidamente que use un solo GMA, si la predicción es una prioridad. Un único flujo de trabajo de GMA debe ser el valor predeterminado para todos los flujos de trabajo, especialmente los flujos de trabajo de consumidor y prosumer. Aunque la asignación de gama para la reproducción preferida debe realizarse una vez, hay instancias en las que se incluyen varios procesos de asignación. En primer lugar, para la prueba, realiza una asignación preferida a la gama del dispositivo de destino final y, a continuación, una representación colorimétrica en la gama del dispositivo de prueba. En segundo lugar, algunos tipos de asignación se usan para modificar las características de la imagen, pero no se incluyen para asignarse a una gama de dispositivos, por ejemplo, ajustar la curva de tono o la cromaticidad. Si se usan varios GMAs, la interfaz de transformación toma una matriz de asignaciones de gama enlazada, es decir, asignaciones de gama que se han inicializado con un par de descripciones de límites de gama. Cuando hay más de un mapa de gama, el límite de la gama de entrada para una asignación de gama correcta debe ser el mismo que el límite de la gama de salida de su predecesor.

La función de límite de gama de dispositivos toma el motor de modelo de dispositivo y los parámetros analíticos, y deriva un límite de gama de dispositivos de color descrito como una lista de vértices ordenados del casco convexo de la gama de dispositivos. La lista de vértices ordenados se almacena en CIEJab. La estructura de la lista de vértices ordenados está optimizada para la aceleración de hardware de DirectX. Este enfoque tiene muchas soluciones conocidas (busque "DirectX de casco convexo" en la web y obtendrá buenos resultados 100). También hay una referencia de 1983 en este tema (teoría y aplicación de gráficos del equipo, "Shiphulls, b-spline Surfaces y CADCAM" pp. 34-49), con referencias de 1970 a 1982 en el tema.

Se pueden usar dos técnicas diferentes para calcular los triángulos en el shell de gama. Para otros dispositivos distintos de los dispositivos RGB aditivos, se calcula un casco convexo. Puede considerar la posibilidad de investigar la compatibilidad con el casco no convexo para otros dispositivos si tiene acceso directo a dichos dispositivos para validar la solidez, el rendimiento y la fidelidad de los algoritmos. Se trata de un proceso conocido que no requiere una descripción más detallada. La técnica que se usa para los dispositivos de suma RGB se describe de la siguiente manera.

Los diferentes GBDs tienen ventajas y desventajas. La representación convexa de casco garantiza unas propiedades geométricas atractivas, como segmentos de matiz convexa que proporcionan un punto de intersección único con un rayo que emana de un punto en el eje neutro. La desventaja de la representación de casco convexa también es la convexidad. Se sabe que muchos dispositivos, en concreto, muestran dispositivos, tienen gamas que están lejos de ser convexa. Si la gama real se desvía significativamente de la suposición de la convexidad, la representación de casco convexa sería inexacta, posiblemente en la medida en que no represente la realidad.

Después de adoptar un GBD que proporciona una representación razonablemente precisa de la gama real, se producen otros problemas, algunos debidos al concepto de segmento de matiz. Hay al menos dos situaciones patológicas. En la siguiente figura 24, una gama de CRT da lugar a segmentos de matiz con "islas". En la figura 25, una gama de impresoras da lugar a un segmento de matiz con parte del eje neutro que falta. Los sectores del matiz patológico no están causados por límites de gama especialmente patológicos en estos casos. Están causados por el concepto de segmento de matiz, porque (a) se toma a lo largo del matiz constante y (b) solo toma una mitad del plano que corresponde al ángulo de matiz.

![Diagrama que muestra una vista superior y una vista lateral de la "curva en" en los tonos azules.](images/gmmp-image097.jpg)

**Figura 24** : un monitor CRT típico tiene una gama que muestra la "curva en" en los tonos azules. Si se toman segmentos de matiz dentro de este intervalo de matiz, las islas aisladas pueden aparecer en los segmentos del matiz.

![Diagrama de una gama con un ' hueco ' en su eje neutro.](images/gmmp-image099.jpg)

**Figura 25** : una impresora puede tener una gama con "hueco" en su eje neutro. Cuando se toma un segmento de matiz (que es solo una mitad del plano), hay una "sangría" en la parte del límite que es el eje neutro. Esto puede ser difícil de resolver con algoritmos.

Para resolver estos pathologies, se propone un nuevo marco que abandone el concepto de segmento de matiz que se usa como punto de partida. En su lugar, el marco utiliza el conjunto de "elementos de línea de límite" o líneas que se encuentran en el límite de la gama. No proporcionan necesariamente una visualización geométrica coherente como segmentos de matiz, pero admiten todas las operaciones de gama comunes. Además de resolver los problemas mencionados anteriormente, este enfoque también sugiere que la construcción de los segmentos de matiz, incluso cuando es posible, es un proceso de pérdida computacional.

### <a name="triangulation-of-the-gamut-boundary"></a>Triangulación del límite de la gama

El punto inicial es un GBD que consta de una triangulación del límite de la gama. Los métodos conocidos para construir GBDs normalmente proporcionan esa triangulación. En cuanto a la concretaidad, un método para construir GBDs para dispositivos aditivos se describe aquí. Estos dispositivos incluyen monitores (basados en CRT y en LCD) y proyectores. La geometría simple del cubo permite introducir un Lattice normal en el cubo. Las caras del borde del cubo se pueden triangular de varias maneras, como la que se muestra en la figura 26. La arquitectura proporciona un modelo de dispositivo para el dispositivo, de modo que los valores de colorimétrico de los puntos de Lattice se puedan obtener de forma algorítmica, o bien se hayan realizado medidas directamente para esos puntos. La arquitectura también proporciona CIECAM02, para que pueda asumir que los datos iniciales ya se han asignado en el espacio de jab de CIECAM02. Después, cada punto de Lattice en las caras del límite del cubo RGB tiene un punto correspondiente en el espacio jab. Las conexiones de los puntos que forman el conjunto de triángulos en el espacio RGB también inducen un conjunto de triángulos en el espacio de jab. Este conjunto de triángulos forma una triangulación razonable del límite de la gama si (a) el Lattice en el cubo RGB es suficientemente fino y (b) la transformación del espacio de dispositivo en el espacio de colores uniforme se comportará topológicamente correctamente; es decir, asigna el límite al límite y no lo convierte en el interior para que los puntos interiores se conviertan en puntos de límite.

![Diagrama que muestra un método sencillo para triangluate el límite de la gama de un dispositivo con R G B como espacio de dispositivo.](images/gmmp-image100.png)

**Figura 26** : método simple para triangular el límite de la gama de un dispositivo con RGB como espacio de dispositivo

### <a name="boundary-line-elements"></a>Elementos de línea de límite

La central de este marco es el concepto de elementos de línea de límite. un conjunto de segmentos de línea que (a) se encuentran en el límite de la gama y (b) se encuentran en un plano. En este caso, el plano es un plano de matiz. Cada segmento de línea es el resultado de la intersección del plano con un triángulo de límite de gama. Aunque muchos investigadores han utilizado la construcción de intersección de un plano con triángulos de límite, generalmente analizan la relación entre estos segmentos de línea e intentan construir un objeto geométrico coherente fuera de los segmentos de línea. Se han diseñado distintos algoritmos para seguir estos segmentos de línea uno tras otro hasta que se obtiene un segmento de matiz completo y se han realizado muchos intentos para acelerar el proceso de búsqueda.

Este enfoque es diferente. Intersecte el plano con los triángulos para obtener los segmentos de línea. A continuación, considere estos segmentos de línea como los objetos conceptuales *básicos* . Es necesario analizar la relación entre los segmentos de línea; no es necesario saber cómo se interconectan entre sí. Este punto de vista resuelve el problema del segmento Hue con islas. Los enfoques conocidos que intentan construir un segmento de matiz suponen que, si uno comienza con un segmento de línea y lo sigue al segmento de línea siguiente, y así sucesivamente; Finalmente, vuelve al punto inicial, en el que se construirá un segmento de matiz entero. Desafortunadamente, este enfoque omitiría la isla (y, en el peor de los casos, el continente). No insistir en obtener una imagen geométrica coherente; es decir, el segmento Hue, puede controlar el problema de la isla sin esfuerzo. Otra diferencia importante en este enfoque es que, para acelerar la construcción de segmentos de línea, usa un "filtro de triángulo". El filtro de triángulo produce ciertos triángulos que no producirán definitivamente segmentos de línea que serían útiles en la operación de la gama actual. Dado que la intersección de un triángulo con el plano es costosa, esto mejora la velocidad. Un efecto secundario es que, no se puede construir el segmento de matiz porque faltan algunos segmentos de línea debido al filtrado de triángulos.

### <a name="gamut-operation-checkgamut"></a>Operación de gama: CheckGamut

En el siguiente ejemplo se explica cómo funciona el marco de trabajo y cómo se realiza CheckGamut, es decir, la operación de comprobar si un color es en gama.

El marco de trabajo general se muestra en la siguiente figura 27. Hay varios componentes. Los componentes con la etiqueta en cursiva son componentes que pueden ser diferentes en la implementación según la operación de gama en cuestión. Los demás componentes son invariables en todas las operaciones de gama. Para empezar, la ***entrada*** es un conjunto de atributos de color. En el caso de CheckGamut, es el color de la consulta. En la figura 27 y en la siguiente explicación, se supone que el ángulo de matiz está entre los atributos de color de entrada o se puede obtener a partir de ellos. Esto es claramente el caso si la entrada es todo el punto de color, ya sea en jab o JCh, desde el que puede calcular el ángulo de matiz. Tenga en cuenta que el ángulo de matiz solo es necesario porque se usan planos de matiz. Dependiendo de la operación de gama en cuestión, puede que no sea necesario usar el plano de matiz. Por ejemplo, en la construcción de la rutina CheckGamut, puede que desee usar planos de la constante J. Se trata de una generalidad que no se utilizará ni se explicará más detalladamente; pero podría ser útil recordar esta flexibilidad de la metodología para admitir otras operaciones de gama cuando el plano de matiz podría no ser la mejor opción.

![Diagrama que muestra el flujo para admitir las operaciones de gama.](images/gmmp-image112.jpg)

**Figura 27** : el marco de trabajo para admitir las operaciones de gama

El ángulo de matiz, que se obtiene directamente de las entradas o calculadas a partir de las entradas, se usa para inicializar el plano de matiz etiquetado con el **plano de matiz completo** en la ilustración. "Full" se enfatiza porque es el plano completo, no solo el medio plano que contiene el matiz. El plano completo contiene tanto el ángulo de matiz de entrada como el ángulo de 180 grados opuestos. La funcionalidad clave del plano Hue es la función Intersect, que se explica en la siguiente subsección, plano de matiz completo: Intersect. Supongamos que ya se ha construido GBD y que el conjunto de **triángulos de límite de gama** está disponible. Intersecte los triángulos que han sobrevivido el **_triángulo Filter_* _ con el plano Hue mediante Intersect. El _componente de filtro de triángulo * se etiqueta en cursiva, lo que significa que el componente varía en la implementación para distintas operaciones de gama. El *filtro de triángulo* de CheckGamut se explica en la sección operación de gama: CheckGamut (continuación). El resultado de la intersección entre un triángulo y el plano del matiz está vacío o es un elemento de la **línea de límite** , es decir, un par de puntos distintos. Si el resultado no está vacío, se pasa al procesador del elemento **_line_*_ , que vuelve a ser diferente en función de la operación de la gama. El _elemento Line Processor * actualiza la estructura de datos interna, ***datos procesados internamente**_ , cuyo contenido o diseño también depende de la operación de la gama. Por lo general, los _datos procesados internos * contienen la "respuesta" al problema, que se actualiza continuamente con cada nuevo elemento de línea de límite encontrado. Una vez procesados todos los elementos de línea de límite, se ha encontrado la respuesta. Sigue teniendo acceso a ella a través del **adaptador de salida***_. Dado que la _Internal datos procesados * es específica de la operación de gama, el *adaptador de salida* también es específico de la operación de gama.

### <a name="full-hue-plane-intersect"></a>Plano de matiz completo: Intersect

La función Intersect calcula la intersección del plano de matiz y un triángulo. Tan sencillo como suena, esta función es importante por dos motivos.

En primer lugar, la intersección de cada borde del triángulo con el plano podría producir tres puntos de intersección, una situación geométricamente imposible. La razón por la que esto puede ocurrir en el cálculo es que, cuando los cálculos se realizan en el punto flotante, por ejemplo, el formato IEEE, faltan incertidumbres o un "ruido numérico" en cada paso que afecta a la conclusión de si un borde forma una intersección con el plano. Cuando el plano forma una intersección con los bordes en una situación de casi sin errores, los puntos de intersección se encuentran cercanos entre sí y la determinación de si un punto de intersección se encuentra dentro del borde es aleatorio. Aunque el ruido en los valores numéricos de los puntos es pequeño, la conclusión cualitativa de que hay más de dos puntos de intersección es geométricamente imposible y difícil de controlar correctamente en el algoritmo.

En segundo lugar, esta función está en el bucle crítico para cada borde de cada triángulo filtrado, por lo que es importante que optimice la eficacia en la medida de lo posible.

Para resolver el primer problema de ruido numérico, realice los cálculos en enteros. Para solucionar el segundo problema de optimizar su eficacia, almacene en caché el atributo más usado de cada vértice o el "producto de punto" asociado a cada vértice. Pasar a enteros es una forma habitual de garantizar la coherencia geométrica. La idea básica es que, si tiene que cuantificar, hágalo al principio. Después, los cálculos posteriores se pueden realizar en enteros y, si los enteros son lo suficientemente amplios como para que no haya ningún riesgo de desbordamiento, los cálculos se pueden realizar con una precisión infinita. La siguiente función de cuantificación útil para este fin.

ScaleAndTruncate (x) = parte entera de x \* 10000

El factor de escala 10000 significa que el número de punto flotante de entrada tiene cuatro posiciones decimales, lo que es lo suficientemente preciso para esta aplicación. En función del intervalo de valores del espacio de apariencia del color, querrá elegir un tipo de entero con el ancho de bits lo suficiente para contener los cálculos intermedios. En la mayoría de los espacios de apariencia de color, el intervalo de cada coordenada está en el intervalo de-1.000 a 1.000. La coordenada cuantificada tiene un valor absoluto máximo posible de 1.000 \* 10.000 = 10 millones. Como verá, la cantidad intermedia es un producto de punto, que es una suma de dos productos de coordenadas, por lo que tiene un valor absoluto máximo posible de 2 \* (10 millones) ₂ = 2? 10 ₁ ₄. El número de bits necesario es ₂ de registro (2? 10 ₁ ₄) = 47,51. Una opción conveniente para el tipo entero es, por lo tanto, enteros de 64 bits.

Para garantizar que la intersección de un plano con un triángulo siempre proporciona un conjunto vacío o un conjunto de dos puntos, debe considerar el triángulo como un todo, no como bordes individuales del triángulo por separado. Para comprender la situación geométrica, tenga en cuenta las "distancias firmadas" de los vértices del triángulo del plano del matiz. No calcule estas distancias firmadas directamente; en su lugar, calcule los productos de punto de los vectores de posición de los vértices con el vector normal cuantificado al plano. Más concretamente, durante la inicialización del plano del matiz, el vector normal cuantificado se calcula como se indica a continuación.

NormalVector = (ScaleAndTruncate (-sin (matiz)), ScaleAndTruncate (cos (Hue)))

Tenga en cuenta que este vector es un vector bidimensional. Puede usar un vector bidimensional porque el plano del matiz es vertical, por lo que el tercer componente del vector normal siempre es cero. Además, se inicializa una tabla de búsqueda de productos de punto para tener una entrada para cada vértice de los triángulos de límite de la gama y el producto de punto correspondiente establecido en un valor no válido.

Durante una operación de intersección con el plano de matiz con un triángulo, se busca el producto de punto de cada vértice del triángulo. Si el valor de la tabla de búsqueda es el valor no válido, el producto de punto se calcula mediante la siguiente expresión.

NormalVector. a \* ScaleAndTruncate (Vertex. a) + NormalVector. b \* ScaleAndTruncate (Vertex. b)

De nuevo, el componente J del vértice nunca se usa, porque el vector normal es horizontal. Este producto dot se guarda en la tabla de búsqueda para que no tenga que volver a calcularse si el producto del punto del vértice se consulta posteriormente.

El almacenamiento en caché permite una determinación rápida de si un borde forma una intersección con el plano, una vez que los productos de punto se tabulan en la tabla de búsqueda, que se genera progresivamente a medida que se procesan los vértices.

![Diagrama que muestra la intersección del plano de matiz con un triángulo.](images/gmmp-image114.jpg)

**Figura 28** : intersección del plano de matiz con un triángulo

Para que el triángulo de la figura 28 intersecte el plano de matiz en un segmento de línea no generada, los productos de punto de los vértices deben estar en uno de los siguientes patrones, cuando se ordenen en orden ascendente.

0, 0, +; -,0; 0; -, 0, +; -,-,+; -,+,+

Se produce un extremo del segmento de línea cuando un borde intersecta con vértices que tienen signos diferentes en el producto de punto. Si el signo es cero, el vértice se encuentra justo en el plano y la intersección del borde con el plano es el propio vértice. Tenga en cuenta también que los casos 0, 0,0; -,-, 0; 0, +, + no se indican. El primer caso (0,0) significa que el triángulo entero está en el plano. Esto no se muestra porque cada borde del triángulo debe pertenecer a un triángulo adyacente que no está completamente en el plano. El borde se informará cuando se tenga en cuenta ese triángulo. Los otros dos casos (-,-, 0 y 0, +, +) se corresponden con la configuración geométrica en la que el triángulo toca el plano en un vértice. Estos casos no se indican porque no dan lugar a un segmento de línea no generada.

El algoritmo anterior determina cuándo calcular una intersección entre un borde del triángulo y el plano del matiz. Una vez determinado un borde, la intersección se calcula mediante ecuaciones paramétricas. Si uno de los productos de punto es cero, la intersección es el propio vértice, por lo que no es necesario realizar ningún cálculo. Suponiendo que los dos productos de punto de los vértices del borde son distintos de cero, vertex1 es el vértice con el producto de punto *negativo* dotProduct1; y vertex2 es el vértice con dotProduct2 de producto de punto *positivo* . Este orden es importante para asegurarse de que el punto de intersección calculado no depende de cómo aparezca el orden de los vértices en la representación del borde. El concepto geométrico del borde es simétrico con respecto a sus vértices. El aspecto computacional del uso de ecuaciones paramétricas del borde presenta asimetría (elección del vértice inicial), que puede dar un punto de intersección ligeramente diferente debido al ruido numérico y el acondicionamiento de las ecuaciones lineales que se van a resolver. Con esto, el punto de intersección, la intersección, viene determinado por lo siguiente.

t = dotProduct1/(dotProduct1-dotProduct2)

intersección. J = vertex1. J + t \* (vertex2. J-vertex1. J

Intersection. a = vertex1. a + t \* (vertex2. a-vertex1. a)

Intersection. b = vertex1. b + t \* (vertex2. b-vertex1. b)

### <a name="gamut-operation-checkgamut-continued"></a>Operación de gama: CheckGamut (continuación)

El algoritmo geométrico básico que se usa para la comprobación de la gama es contar el número de cruces de rayos. Para un punto de consulta determinado, considere la posibilidad de usar un rayo empezando por el punto de consulta y apuntando hacia arriba (Dirección J). Cuente el número de veces que este rayo cruza el límite de la gama. Si este número es par, el punto de consulta está fuera de la gama. Si este número es impar, el punto está dentro de. En principio, este algoritmo se puede implementar en 3D; por lo general, está plagada por las dificultades ocasionadas por situaciones degeneradas, como el rayo que se encuentra (en parte) en un triángulo límite o degeneracys de menor dimensiones, como el rayo que se encuentra en un borde de un triángulo de límite. Incluso en 2-D, tiene que tratar con estas situaciones degeneradas: pero el problema es más sencillo y se ha solucionado de manera satisfactoria. Vea \[ O'Rourke \] .

Para un punto de entrada determinado jab, determine el ángulo de matiz h como se indica a continuación.

h = atan (b/a),

Inicialice el plano de matiz y, a continuación, determine los elementos de línea de límite correspondientes a este plano de matiz. Dado que los elementos de línea de límite solo son relevantes si forman una intersección con el rayo hacia arriba, configure un filtro de triángulo para quitar triángulos que proporcionen elementos de línea que definitivamente no intersectarán con el rayo ascendente. En este caso, considere el rectángulo de selección del triángulo. El rayo hacia arriba no intersectará el triángulo si el punto de consulta está fuera de la conversión de "sombra" por el cuadro de límite si una fuente de luz estaba justo encima. Inflarlo ligeramente con una tolerancia prefijada para permitir ruido numérico, de modo que no se produzcan de manera inadvertida triángulos que puedan proporcionar elementos de línea útiles. El resultado es el cilindro rectangular semiinfinito que se muestra en la Figura 29. La comprobación de si el punto de consulta está dentro o fuera de este cilindro se puede implementar eficazmente mediante desigualdades simples.

![Muestra el filtro de triángulo para CheckGamut.](images/gmmp-image116.jpg)

**Figura 29** : filtro de triángulo para CheckGamut

CheckGamut tiene tres componentes específicos de operación de gama: *datos procesados internos*,*procesador de elementos de línea* y adaptador de *salida*. Los *datos procesados internos* son una lista de elementos de línea procesados por el *procesador de elementos de línea*. En este caso, el *procesador del elemento de línea* simplemente agrega un elemento de línea a la lista. La estructura de datos interna para los *datos procesados internos* puede ser una lista vinculada o una matriz que pueda aumentar de tamaño.

El *adaptador de salida* es un módulo que tiene acceso a la lista de elementos de línea, determina si un elemento de línea cruza el rayo hacia arriba (recuento 1) o no (recuento 0). La suma de todos estos recuentos ofrece un recuento total. En última instancia, el *adaptador de salida* da como resultado una respuesta de "sí" (en gama) o "no" (fuera de la gama), dependiendo de si el recuento total es impar o uniforme. El paso en el que se determina si un elemento de línea cruza el rayo ascendente merece la atención porque aquí es donde se produce el problema de degeneracy y también surge el problema de exceso de recuento. Después de \[ O'Rourke \] , para que un elemento de línea cruce el rayo, el extremo derecho (el punto final con intensidad de croma mayor) debe estar en el lado derecho del rayo. Esto garantiza que, si un punto final se basa exactamente en el rayo, solo se cuenta una vez. La misma regla también resuelve la situación degenerada en la que el elemento de línea está exactamente en el rayo. No se incrementa el recuento para este elemento de línea.

En la figura 30 se muestran los elementos de línea resultantes de una gama de muestras con el punto de consulta en varias posiciones.

![Diagrama que muestra los elementos de línea resultantes de una gama de muestras con el punto de consulta en varias posiciones.](images/gmmp-image118.jpg)

**Figura 30** : funcionamiento de CheckGamut

### <a name="minimum-color-difference-gamut-mapping"></a>Asignación mínima de gama de diferencias de color

La asignación mínima de gama de diferencias de color, MinDEMap, tiene una especificación simple: Si un color es en gama, no haga nada. Si un color está fuera de la gama, se proyecta en el punto "más cercano" en el límite de la gama. La palabra clave "más cercana" no está bien definida hasta que se especifica la ecuación de diferencia de color que se va a usar. En la práctica, para hacer que el cálculo sea más fácil y rápido, la distancia euclidiana del espacio de apariencia del color elegido, o una variante de él, se usa como la métrica de diferencia de color. La ventaja de la métrica euclidiana es que es compatible con el producto punto del espacio, lo que hace posible usar álgebra lineal. En detalle, si se define un "producto de punto" en el espacio, se puede definir una distancia como la raíz cuadrada del producto de puntos del vector de diferencia. Un producto de punto se puede definir generalmente mediante una matriz de 3x3 delimitada positiva.

u? v = u <sub>T</sub> AV

donde el lado derecho es la multiplicación de matrices usual. Si es la matriz de identidad, se recupera el producto de punto estándar. En la práctica, si jab es el espacio de colores, no desea mezclar los componentes, por lo que se puede usar una matriz diagonal distinta de la matriz de identidades. Además, es posible que desee mantener la escala en y b sin cambios, de modo que se conserve la medida de matiz. Por lo tanto, una variación útil del producto euclidiana DOT estándar es la siguiente.

<sub>j</sub> (j componente) (j Component of v) + (un componente de usted) (un componente de v) + (componente b de usted) (componente b de v)

donde w <sub>J</sub> es un número positivo. Una variación adicional consiste en permitir que <sub>j</sub> varíe con el punto de consulta de entrada:

w <sub>j \ =</sub> w <sub>(queryPoint</sub> )

El resultado final es una medida de distancia que es asimétrica con respecto a los dos puntos, y con diferentes pesos relativos en la luminosidad y croma o el matiz según varíe el punto de consulta de entrada. Esto está en consonancia con algunas observaciones sobre la percepción de color humano de que las diferencias de color no se ponderan equitativamente en todas las dimensiones. Se ha descubierto que las personas son menos sensibles a las diferencias en cuanto a la luminosidad que las diferencias de matiz y croma.

La siguiente función de peso es útil.

w <sub>J</sub> = k ₂-k ₁ (C-c m ₐ ₓ) n

donde k ₂ = 1, k ₁ = 0,75/(C m ₐ ₓ) n, C m ₐ ₓ = 100, n = 2 y C es el menor de croma del punto de consulta y C m ₐ ₓ.

de modo que el peso de 0,25 se coloca en el término J cuando el croma es cero y un peso de 1 cuando el croma es 100. Tendencia de colocar menos peso en J cuando el croma es pequeño y más peso en J cuando el croma es grande sigue el uso recomendado para CMC y CIEDE2000.

![Gráfico que muestra la función de peso en el componente J de la métrica.](images/gmmp-image119.png)

**Figura 31** : función de peso en el componente J de la métrica

Use el espacio jab para el siguiente ejemplo. Exige que se busque en todos los triángulos de límite para determinar el punto más cercano de la métrica euclidiana. El siguiente es un enfoque sencillo para que este proceso sea lo más eficaz posible, sin introducir suposiciones adicionales que puedan acelerar el proceso, pero que también acaben en una respuesta aproximada. En primer lugar, es necesario comprender el procedimiento geométrico de proyectar un punto en el triángulo determinado. Aquí se proporciona una descripción.

Primero se realiza una proyección ortogonal en el plano infinito que contiene el triángulo. La distancia más corta del punto de consulta del plano puede determinarse en dos pasos.

**(a)** calcule el vector normal de la unidad al triángulo.

**(b)** calcular el producto de punto del vector de unidad normal y un vector formado a partir del punto de consulta y un punto en el triángulo; es decir, uno de sus vértices. Dado que el vector normal tiene una longitud de unidad, el valor absoluto de este producto de punto es la distancia del punto de consulta del plano.

El punto proyectado podría no ser la respuesta porque podría estar fuera del triángulo. Por lo tanto, debe realizar una comprobación primero. El cálculo es equivalente a calcular las coordenadas Barycentric del punto proyectado en relación con el triángulo. Si se determina que el punto proyectado está dentro del triángulo, es la respuesta. Si no es así, se adquiere el punto más cercano en uno de los bordes del triángulo. Realice una búsqueda en cada uno de los tres bordes. Determinar la proyección del punto de consulta en un borde es un proceso similar a la proyección en el triángulo, pero una dimensión es menor. Primero se calcula una proyección ortogonal. Si el punto proyectado se encuentra en el borde, es la respuesta. En caso contrario, se adquiere el punto más cercano en uno de los dos extremos. Realice una búsqueda en los dos extremos; es decir, calcule la distancia del punto de consulta de cada uno de ellos y compare cuál es el más pequeño.

Un examen cuidadoso revela que hay muchas búsquedas repetidas cuando se recorren todos los triángulos porque un borde siempre se comparte con dos triángulos y un vértice compartido por al menos tres bordes. Además, no está muy interesado en encontrar el punto más cercano a un triángulo determinado; en su lugar, le interesa encontrar el punto más cercano a todo el límite de la gama. Sin embargo, un triángulo determinado sería el en el que se consigue. Hay dos estrategias que puede usar para acelerar la búsqueda.

**Estrategia I**. Cada vértice se procesará, como máximo, una vez. Cada borde se procesará, como máximo, una vez.

**Estrategia II**. En cualquier momento de la búsqueda, tiene un mejor candidato con la mejor distancia correspondiente. Si puede determinar, mediante una comprobación rápida, que un triángulo no es capaz de ofrecer una mejor distancia, no es necesario continuar el cálculo aún más. No necesita el punto y la distancia más cercanos para este triángulo.

![Diagrama que muestra el flujo de la asignación mínima de.](images/gmmp-image120.png)

**Figura 32** : esquemas mínimos de asignación

En la Figura 32 se muestra el flujo general de lógica para el mapa de la gama MinDEMap. En un punto de consulta, la función CheckGamut se invoca por primera vez. Si el punto es en la gama, el mapa es una operación no operativa. Si el punto está fuera de la gama, llame a ProjectPointToBoundary. Ahora, pase a la Figura 33. En este punto, se supone que se han calculado los valores siguientes.

**(a)** vector normal de unidad para cada triángulo de límite de gama con respecto al producto de punto estándar.

**(b)** lista de vértices y lista de bordes, además de la lista de triángulos.

![Diagrama que muestra la rutina ' ProjectPointToBoundary '.](images/gmmp-image122.jpg)

**Figura 33** : rutina ProjectPointToBoundary

Todos estos son una sobrecarga constante y tendrían costos reducidos si se realizan consultas suficientes para este límite de gama. Normalmente, este es el caso cuando se crea una transformación LUT desde un dispositivo a otro, donde solo hay dos gamas fijas, y la transformación LUT se ejecuta a través de puntos de la cuadrícula muestreada uniformemente. Calcula previamente los vectores normales con respecto al producto de punto estándar, aunque el concepto de la perpendicular se basará en el producto de punto ponderado, que depende del punto de consulta tal y como se explicó anteriormente. La razón es que un vector normal con respecto al producto de punto ponderado se puede obtener fácilmente desde el vector normal con respecto al producto de punto estándar. Si n ₀ es un vector normal con respecto al producto de punto estándar,

n = (componente J de n ₀/w <sub>J</sub>, un componente-de n ₀, componente b de n ₀)

es normal para el triángulo con respecto al producto de punto ponderado. Debido a esta relación, sigue siendo útil calcular previamente n ₀, aunque debe ajustarse en función del punto de consulta.

La rutina ProjectPointToBoundary se inicia restableciendo el "historial procesado" de los vértices y los bordes. Se trata de tablas de marcas BOOLEANAS que realizan un seguimiento de si un vértice o borde se ha visitado antes. También restablece la variable ShortestDistance en "Infinity", que es el valor codificado máximo en el sistema de números de punto flotante usado. A continuación, se ejecuta a través de un bucle, buscando el punto más cercano de cada triángulo mediante la llamada ProcessTriangle. ProcessTriangle es la rutina para actualizar la variable ShortestDistance y está claramente en el bucle crítico. Una optimización es detenerse cuando el resultado es lo suficientemente bueno. Después de cada llamada a ProcessTriangle, se examina la variable ShortestDistance. Si cumple un umbral predefinido, puede detenerse. El umbral predefinido depende del espacio de colores utilizado y de la precisión necesaria del sistema de creación de imágenes de color. En el caso de una aplicación típica, no desea realizar ningún trabajo innecesario si la diferencia de color es menor que la que se puede discernir por la visión humana. En el caso de CIECAM02, esta diferencia de color es 1. No obstante, use un valor de umbral de 0,005 en la implementación para conservar la precisión de los cálculos, ya que esto podría ser solo un paso intermedio en una cadena de transformaciones.

ProcessTriangle implementa la estrategia II anterior. Al obtener un vector normal del vector normal de la unidad precalculada al triángulo con respecto al producto de punto estándar, calcula la distancia del punto de consulta al plano infinito que contiene el triángulo formando el producto de punto del vector de unidad normal y el queryVector, el vector de uno de los vértices del triángulo, vertex1, al punto de consulta. , queryPoint.

queryVector = queryPoint-vertex1

Distance = \| normalVector \* queryVector \| / \| \| normalVector\|\|

Este es un cálculo relativamente económico y la distancia es necesaria para realizar cálculos adicionales. Si esta distancia no es menor que la mejor distancia actual, ShortestDistance, este triángulo no producirá una mejor distancia, ya que no proporcionará una distancia mayor que el plano que lo contiene. En este caso, devolverá el control al bucle de triángulo. Si la distancia es menor que ShortestDistance, es posible que tenga un punto más cercano, si este punto se encuentra dentro del triángulo. Debe realizar algunos cálculos "físicos" (no obstante, nada más allá del álgebra lineal) para determinar eso. Si los otros dos vértices del triángulo son vertex2 y vertex3, forme los vectores de base firstBasisVector y secondBasisVector.

firstBasisVector = vertex2-vertex1

secondBasisVector = vertex3-vertex1

Use el siguiente sistema lineal de ecuaciones para solucionar los problemas de los que dispone y v.

firstBasisVector \* queryVector = (firstBasisVector \* firstBasisVector) u + (firstBasisVector \* secondBasisVector) v

secondBasisVector \* queryVector = (secondBasisVector \* firstBasisVector) u + (secondBasisVector \* secondBasisVector) v

y las condiciones del punto proyectado que se encuentran dentro del triángulo son:

0 ≤ u ≤ 1, 0 ≤ v ≤ 1 y + v ≤ 1

Después de este cálculo, si se determina que el punto proyectado se encuentra dentro del triángulo, habrá encontrado un nuevo punto más cercano. la distancia que calculó al principio es la nueva distancia más corta. En este caso, actualice las variables ShortestDistance y ClosestPoint. Si el punto proyectado se encuentra fuera del triángulo, es posible que encuentre un punto más cercano en uno de sus bordes. Por lo tanto, puede llamar a la rutina ProcessEdge en cada uno de los tres bordes.

![Diagrama que muestra el flujo de las rutinas ProcessEdge y ProcessVertex.](images/gmmp-image124.jpg)

**Figura 34** : rutinas ProcessEdge y ProcessVertex

La rutina ProcessEdge implementa la estrategia I, que se muestra en la figura 34. ProcessEdge se inicia comprobando si el borde se ha procesado antes. Si es así, no se realiza ninguna otra acción. En caso contrario, continúa calculando la proyección ortogonal del punto de consulta en la línea infinita que contiene el borde. El álgebra lineal implicado en el cálculo es similar a las ecuaciones del triángulo anterior. Sin embargo, el cálculo es más sencillo, no se describe aquí. Si el punto proyectado se encuentra dentro del borde, la distancia del punto proyectado se encuentra en el punto de consulta. Si esta distancia es menor que ShortestDistance, ha encontrado un nuevo punto más cercano. Actualice ShortestDistance y ClosestPoint. Si el punto proyectado se encuentra fuera del borde, llame a ProcessVertex en los dos extremos. Antes de devolver el control, actualice el historial perimetral para que este borde se marque como "procesado".

Por último, proporcione una descripción de ProcessVertex. La rutina ProjectVertex también implementa la estrategia I y mantiene una tabla de historial de vértices. Como se muestra en la figura 34, primero comprueba si el vértice se ha procesado antes. Si es así, no se realiza ninguna otra acción. Si no es así, se calcula la distancia del vértice del punto de consulta. Si la distancia es menor que ShortestDistance, actualice ShortestDistance y ClosestPoint. Al final, actualiza el historial de vértices para que este vértice se marque como "procesado".

Cuando el bucle de control exterior ha agotado todos los triángulos o salido antes de que se haya cumplido el umbral de diferencia de color, se obtiene acceso a la variable ClosestPoint. Este es el resultado de MinDEMap. El autor de la llamada también puede recuperar ShortestDistance si le interesa el color asignado del color de la consulta.

### <a name="hue-smoothing"></a>Suavizado de matiz

![Diagrama que muestra dos vistas principales del suavizado de matiz, el original en la parte superior y el matiz suavizado en la parte inferior.](images/gmmp-image125.png)

**Figura 35** : suavizado de matiz

Se produce un problema con las operaciones con restricción de matiz; es decir, la operación solo tiene en cuenta las variables dentro de un plano de matiz. En la figura 35 se muestra un ejemplo de una gama que presenta segmentos de matiz "descontinuos" en los tonos azules. Dentro de este intervalo de matiz, para determinados ángulos de matiz, el límite de la gama es tangencial al plano del matiz. De hecho, esto provoca un cambio en la estructura topológica de los segmentos de matiz. En el ejemplo mostrado, a medida que el plano de matiz se barre en este rango de matiz, una "isla" emerge y se combina. Este cambio en la topología hará que las operaciones específicas de matiz sean discontinuas. Por ejemplo, el intervalo de cresta en el matiz fijo cambia repentinamente a medida que cambia el ángulo de matiz en este intervalo.

Hay un motivo de ciencia de color por el que es deseable conservar el matiz en determinadas operaciones. Para resolver el problema anterior, los triángulos del límite de la gama original deben ser "Hue Smoothed". En general, un matiz de tonalidad de un conjunto de triángulos de límite de gama es un conjunto de triángulos que (a) forma el límite de una nueva "gama", que podría no corresponderse con la gama real de dispositivos, y que contiene la gama definida por el conjunto original de triángulos; y (b) los triángulos del conjunto nuevo se limitan de ser paralelos a los planos de matiz.

Una forma práctica de obtener un conjunto suavizado de los triángulos es usar el casco convexo de los vértices originales. Como se muestra en la figura 35, los segmentos de matiz del casco convexo varían suavemente en el intervalo de matiz problemático sin un cambio repentino en la topología.

### <a name="setting-primaries-and-secondaries-in-the-gamut-boundary-description"></a>Configuración de las principales y secundarias en la descripción del límite de la gama

Ciertos métodos de asignación de gama, como HueMap, dependen de la ubicación de las principales y secundarias del dispositivo. En el caso de los dispositivos aditivos, los primarios son rojo, verde y azul (R, G y B); y las secundarias son cian, magenta y amarillo (C, M e y). En el caso de los dispositivos de sustracción, los primarios son C, M e y; y las secundarias son R, G y B. GBD realiza un seguimiento de los seis valores, más el blanco y el negro (W y K), en una matriz de valores de color jab. Estos valores se establecen en la descripción del límite de la gama cuando se crea. En el caso de los dispositivos de salida, los primarios se pueden determinar mediante la ejecución de combinaciones de valores de control de dispositivo a través del modelo de dispositivo. En el caso de los dispositivos de captura, este enfoque no es adecuado para crear el GBD de referencia, ya que es prácticamente imposible capturar una imagen que produce un valor de dispositivo puro totalmente saturado, como (0,0, 0,0, 1,0). Los perfiles de dispositivo WCS contienen los índices de las principales del destino de captura. Dado que estos valores no se incluyen en un perfil ICC, use los valores que se miden a partir de un destino de escáner típico después de la conversión a jab, en relación con las condiciones de visualización de ICC.

### <a name="setting-the-neutral-axis-in-the-gamut-boundary-description"></a>Establecimiento del eje neutro en la descripción del límite de la gama

Los métodos de asignación de gama picada relativa y HueMap usan el eje neutro del dispositivo para enderezar. En el caso de los dispositivos de salida de línea base, el eje neutro se puede determinar mediante la ejecución de valores neutros de dispositivo (R = G = B o C = M = Y) a través del método DeviceToColorimetric y, a continuación, mediante el método ColorimetricToAppearance del objeto CIECAM02. Sin embargo, los dispositivos de captura no siempre devuelven un valor neutro del dispositivo cuando se presentan con un ejemplo neutro. Esto es especialmente cierto cuando la iluminación ambiente no es totalmente neutra. Los perfiles de dispositivo WCS contienen los índices de los ejemplos neutros en el destino. Use esos ejemplos para establecer el eje neutro. Dado que esta información no está disponible para los perfiles de ICC, debe usar el mismo método que se usa para los dispositivos de salida; Ejecute ejemplos neutros de dispositivo a través del método DeviceToColorimetric y, a continuación, acople los valores de entrada y los resultados de la colorimétrico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos básicos de la administración del color](basic-color-management-concepts.md)
</dt> <dt>

[Algoritmos y esquemas del Sistema de colores de Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 




