---
title: Información general sobre transformaciones
description: Presenta la API de transformación de Microsoft Direct2D para Windows 7. Direct2D permite a los desarrolladores de Win32 realizar transformaciones de gráficos 2D.
ms.assetid: eea8177d-c19e-4972-a9a6-ad5d541b090f
keywords:
- Información general de las transformaciones de Direct2D
- Direct2D, sistemas de coordenadas
- Direct2D, destinos de representación
- Direct2D, transformaciones 2D
- transformaciones en 2D
- transformaciones, acerca de
- transformaciones, destinos de representación
- transformaciones, objetos
- destinos de representación, transformaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f3678f7b194f0f0188ed907a63737a97e9e58c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995302"
---
# <a name="transforms-overview"></a>Información general sobre transformaciones

En este tema se describen los aspectos básicos de las transformaciones de Direct2D y se incluyen ejemplos de diversas transformaciones. Contiene las siguientes partes:

-   [¿Qué es una transformación de Direct2D?](#what-is-a-direct2d-transform)
-   [Espacio de coordenadas de Direct2D](#the-direct2d-coordinate-space)
-   [Crear matrices de transformación](#creating-transformation-matrices)
-   [Transformaciones de destino de representación](#rendering-target-transforms)
-   [Transformaciones de pincel](#brush-transforms)
-   [Transformaciones de geometría](#geometry-transforms)
-   [Cómo afecta una transformación de destino de representación a clips](#how-a-render-target-transform-affects-clips)
-   [Resumen](#summary)
-   [Temas relacionados](#related-topics)

## <a name="what-is-a-direct2d-transform"></a>¿Qué es una transformación de Direct2D?

Una transformación especifica cómo asignar los puntos de un objeto de un espacio de coordenadas a otro o de una posición a otra dentro del mismo espacio de coordenadas. Esta asignación se describe mediante una matriz de transformación, definida como una colección de tres filas con tres columnas de valores FLOAT, tal como se muestra en la tabla siguiente.



|                 |                 |     |
|-----------------|-----------------|-----|
| M11Default: 1,0 | M12Default: 0,0 | 0,0 |
| M21Default: 0,0 | M22Default: 1,0 | 0,0 |
| M31OffsetX: 0,0 | M32OffsetY: 0,0 | 1,0 |



 

En esta matriz, los miembros M11, M12, M21 y M22 definen una transformación lineal que puede escalar, girar o sesgar un objeto. los miembros OffsetX y OffsetY definen la traducción que se va a aplicar después de realizar la transformación lineal. En las transformaciones afines, los valores de la tercera columna siempre son 0,0, 0,0 y 1,0.

Dado que Direct2D solo admite transformaciones afín (lineal), su matriz de transformación se define como una matriz de 3 por 2, omitiendo la tercera columna de la matriz de transformación anterior. En la tabla siguiente se muestra el diseño de la matriz de transformación de Direct2D.



|                 |                 |
|-----------------|-----------------|
| M11Default: 1,0 | M12Default: 0,0 |
| M21Default: 0,0 | M22Default: 1,0 |
| M31OffsetX: 0,0 | M32OffsetY: 0,0 |



 

En Direct2D, esta matriz de 3 por 2 se representa mediante la estructura [**\_ \_ 3x2 de la matriz D2D1**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) . Para simplificar las operaciones de matriz comunes, Direct2D también proporciona una clase denominada [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f), que se deriva de la estructura 3x2 de la **\_ matriz \_ D2D1** .

El constructor predeterminado para [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) deja el objeto sin inicializar. Para recuperar una matriz de identidad, use [**Matrix3x2F:: Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix).

Cuando se aplica una transformación de identidad a un objeto, no cambia la posición, la forma o el tamaño del objeto. Es similar a la forma en que multiplica un número por 1 no cambia el número. En otras palabras, la transformación de identidad deja las coordenadas de los puntos solos y no desplaza los puntos a una nueva posición. Cualquier transformación que no sea la transformación de identidad modificará la posición, la forma y el tamaño de los objetos.

Las transformaciones son todas las coordenadas y comprender el espacio de coordenadas de Direct2D es importante para entender el uso de las transformaciones.

## <a name="the-direct2d-coordinate-space"></a>Espacio de coordenadas de Direct2D

Direct2D usa un espacio de coordenadas de mano izquierda; es decir, los valores positivos del eje x se incrementan a la derecha y los valores positivos del eje y aumentan hacia abajo. Todo lo que se encuentra en la pantalla se coloca en relación con el origen, que es el punto en el que el eje x y el eje y forman una intersección (0,0), tal como se muestra en la siguiente ilustración. Los destinos de representación de Direct2D usan este espacio de coordenadas.

![Ilustración de los ejes x e y de un espacio de coordenadas de la mano izquierda](images/coordinatespace.png)

Al manipular los valores de una matriz de transformación, puede girar, escalar, sesgar y desplazar (trasladar) un objeto. Por ejemplo, si establece OffsetX en 100 y PosiciónInicial en 200, mueva el objeto a la derecha 100 píxeles y Down 200 píxeles.

Para mostrar el efecto del movimiento del objeto, debe aplicar la transformación traslación a los destinos, pinceles o geometrías de representación. Aplicar una transformación a los destinos de representación afecta a toda la pantalla, mientras que la aplicación de una transformación a un pincel o una geometría solo afecta a ese pincel o geometría concretos. Para crear una matriz de transformación, utilice la clase [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) .

## <a name="creating-transformation-matrices"></a>Crear matrices de transformación

Para crear transformaciones de giro, escala, sesgo y traslación, la clase [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) proporciona los métodos estáticos que se muestran en la tabla siguiente. La columna de ejemplo de la tabla contiene vínculos a los temas de procedimientos que muestran cómo usar cada método de transformación.



| Método                                                                   | Descripción                                                                                                     | Ejemplo                                            | Ilustración                                                                                                                            |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**matrix3x2f:: Rotate**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)                          | crea una transformación de giro que tiene el ángulo y el punto central especificados.                                | [Cómo girar un objeto](how-to-rotate.md)       | ![Ilustración de un cuadrado girado 45 grados en el sentido de las agujas del reloj sobre el centro del cuadrado original](images/rotate-ovw.png)                 |
| [**matrix3x2f:: scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f)) | crea una transformación de escala que tiene los factores de escala y el punto central especificados.                           | [Cómo escalar un objeto](how-to-scale.md)         | ![Ilustración de un cuadrado escalado 130%](images/scale-ovw.png)                                                                           |
| [**matrix3x2f:: Skew**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)                              | crea una transformación de sesgo que tiene los valores del eje x y del eje y y el punto central especificados.                 | [Cómo sesgar un objeto](how-to-skew.md)           | ![Ilustración de un cuadrado sesgado de 30 grados en sentido contrario a las agujas del reloj desde el eje y](images/skew-ovw.png)                                     |
| [**matrix3x2f:: Translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))                | crea una transformación de traslación y especifica los desplazamientos en la dirección de los ejes x e y. | [Cómo trasladar un objeto](how-to-translate.md) | ![la ilustración de un cuadrado ha desplazado 20 unidades a lo largo del eje x positivo y 10 unidades a lo largo del eje y positivo](images/translation-ovw.png) |



 

## <a name="rendering-target-transforms"></a>Transformaciones de destino de representación

Un destino de representación es un recurso que hereda de la interfaz [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) . Crea recursos para dibujar y realiza operaciones de dibujo reales. También proporciona métodos para transformar el espacio de coordenadas. Puede llamar al método [**ID2D1RenderTarget:: SetTransform**](id2d1rendertarget-settransform.md) para aplicar la transformación especificada al destino de representación. Todas las operaciones de dibujo posteriores se producen en el espacio transformado.

Para representar el contenido, use los métodos de dibujo del destino de representación. Antes de empezar a dibujar, llame al método [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) . Para finalizar la representación del contenido, llame al método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Para obtener un ejemplo, consulte [Cómo aplicar varias transformaciones a un objeto](how-to-apply-multiple-transforms.md).

## <a name="brush-transforms"></a>Transformaciones de pincel

Puede ajustar la transformación en el pincel llamando a [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)). Para esta transformación, puede pensar en el pincel como una gran pieza de papel y en los distintos tipos primitivos de representación (texto, geometría, rectángulo, etc.) como galerías de símbolos. Al ajustar la transformación del pincel, es como si estuviera deslizando la pieza grande del papel debajo de la galería de símbolos, sin cambiar la posición del mismo. Puede usar esta técnica para que el texto se atenúe de amarillo a negro en el espacio 3D.

Cuando la transformación del pincel es la transformación de identidad, los pinceles aparecen en el mismo espacio de coordenadas que el destino de representación en el que se dibujan. La transformación de pincel permite a un llamador modificar el modo en que las coordenadas del pincel se asignan a este espacio.

El espacio del pincel se especifica de manera diferente en Direct2D que en Windows Presentation Foundation (WPF). En Direct2D, el espacio del pincel no es relativo al objeto que se está dibujando, sino que es el sistema de coordenadas actual del destino de representación, transformado por la transformación del pincel, si lo hay. Para que el pincel rellene un objeto como se hizo en WPF, debe traducir el origen del espacio del pincel en la esquina superior izquierda del rectángulo de selección del objeto y, a continuación, escalar el espacio del pincel para que el mosaico base rellene el cuadro de límite del objeto.

Para obtener más información sobre las transformaciones de pincel, consulte [información general sobre pinceles de Direct2D](direct2d-brushes-overview.md).

## <a name="geometry-transforms"></a>Transformaciones de geometría

Al escalar, trasladar, trasladar o sesgar las geometrías, puede aplicar directamente una transformación a una geometría específica, no a una transformación de destino de representación que afecte a toda la pantalla. Una transformación de destino de representación suele afectar al trazo y al relleno de una geometría. Por el contrario, una transformación Geometry solo afecta al relleno de una geometría, ya que la transformación se aplica a una geometría antes de que se Trace.

> [!Note]  
> A partir de Windows 8, la transformación del mundo no afecta al trazo si establece el tipo de trazo en el tipo de [**\_ transformación trazo de D2D1 \_ \_ \_ fijo**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type) o el [**tipo de \_ transformación trazo D2D1 \_ \_ \_ fino**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type).

 

Puede ajustar la transformación en una geometría mediante una llamada a [**ID2D1Factory:: CreateTransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) para crear un objeto [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) . Para obtener más información sobre las transformaciones de geometría, consulte [información general sobre las geometrías de Direct2D](direct2d-geometries-overview.md).

## <a name="how-a-render-target-transform-affects-clips"></a>Cómo afecta una transformación de destino de representación a clips

La transformación de un destino de representación afecta al modo en que se calcula el rectángulo de selección de un clip alineado con el eje. Cuando se llama a [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) , el parámetro *clipRect* se transforma por la transformación universal actual que se establece en el destino de representación. Después de aplicar la transformación al *clipRect*, se calcula el rectángulo de selección alineado con el eje para *clipRect* . Por motivos de eficacia, el contenido se recorta en este cuadro de límite alineado con el eje y no en el *clipRect* original que se pasa. En los diagramas siguientes se muestra cómo se aplica una transformación de giro al destino de representación, el *clipRect* resultante y un cuadro de límite alineado con el eje calculado.

1.  Suponga que el rectángulo de la siguiente ilustración es un destino de representación que se alinea con los píxeles de la pantalla.

    ![Ilustración de un rectángulo (destino de representación)](images/pushaxisalignedclip-step1-rendertarget.png)

2.  Aplica una transformación de giro al destino de representación. En la ilustración siguiente, el rectángulo negro representa el destino de representación original y el rectángulo discontinuo rojo representa el destino de representación transformado.

    ![Ilustración del rectángulo original y un rectángulo girado (destino de representación transformado)](images/pushaxisalignedclip-step2-transformed.png)

3.  Después de llamar a [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) , se aplica la transformación de giro a *clipRect*. En la ilustración siguiente, el rectángulo azul representa el *clipRect* transformado.

    ![Ilustración de un rectángulo azul más pequeño (clipRect) dentro del rectángulo girado (destino de representación transformado)](images/pushaxisalignedclip-step3-cliprecttransformed.png)

4.  Se calcula el rectángulo de selección alineado con el eje. En la ilustración siguiente, el rectángulo discontinuo verde representa el cuadro de límite. Todo el contenido se recorta a este cuadro de límite alineado con el eje.

    ![Ilustración de un cuadro de límite verde en el pequeño rectángulo azul (clipRect)](images/pushaxisalignedclip-step4-boundingbox.png)

## <a name="summary"></a>Resumen

Direct2D facilita la transformación de objetos bidimensionales con espacios de coordenadas simplificados y clases relacionadas. Mediante el uso de varios tipos de transformaciones, puede trasladar, girar, sesgar y escalar los objetos para obtener muchos efectos visuales impresionantes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct2D](reference.md)
</dt> </dl>

 

 