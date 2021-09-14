---
title: Información general sobre transformaciones
description: Presenta la API de transformación de Microsoft Direct2D para Windows 7. Direct2D permite a los desarrolladores de Win32 realizar transformaciones de gráficos 2D.
ms.assetid: eea8177d-c19e-4972-a9a6-ad5d541b090f
keywords:
- Direct2D, introducción a las transformaciones
- Direct2D, sistemas de coordenadas
- Direct2D, destinos de representación
- Transformaciones 2D y 2D de Direct2D
- Transformaciones 2D
- transforms,about
- transforms,render targets
- transforms,objects
- destinos de representación, transformaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b924c51d73e71f206fbb250f4a7dd50ca71db2a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163346"
---
# <a name="transforms-overview"></a>Información general sobre transformaciones

En este tema se de abordan los conceptos básicos de las transformaciones de Direct2D e incluye ejemplos de diversas transformaciones. Contiene las partes siguientes:

-   [¿Qué es una transformación de Direct2D?](#what-is-a-direct2d-transform)
-   [El espacio de coordenadas de Direct2D](#the-direct2d-coordinate-space)
-   [Crear matrices de transformación](#creating-transformation-matrices)
-   [Transformaciones de destino de representación](#rendering-target-transforms)
-   [Transformaciones de pincel](#brush-transforms)
-   [Transformaciones de geometría](#geometry-transforms)
-   [Cómo afecta una transformación de destino de representación a los clips](#how-a-render-target-transform-affects-clips)
-   [Resumen](#summary)
-   [Temas relacionados](#related-topics)

## <a name="what-is-a-direct2d-transform"></a>¿Qué es una transformación de Direct2D?

Una transformación especifica cómo asignar los puntos de un objeto de un espacio de coordenadas a otro o de una posición a otra dentro del mismo espacio de coordenadas. Esta asignación se describe mediante una matriz de transformación, definida como una colección de tres filas con tres columnas de valores FLOAT, como se muestra en la tabla siguiente.



|    &nbsp;       |       &nbsp;    |  &nbsp; |
|-----------------|-----------------|-----|
| M11Default: 1.0 | M12Default: 0.0 | 0,0 |
| M21Default: 0.0 | M22Default: 1.0 | 0,0 |
| M31OffsetX: 0.0 | M32OffsetY: 0.0 | 1.0 |



 

En esta matriz, los miembros M11, M12, M21 y M22 definen una transformación lineal que puede escalar, girar o sesgar un objeto; Los miembros OffsetX y OffsetY definen la traducción que se aplicará una vez realizada la transformación lineal. En el caso de las transformaciones afín, los valores de la tercera columna siempre son 0,0, 0,0 y 1,0.

Dado que Direct2D solo admite transformaciones afín (lineales), su matriz de transformación se define como una matriz 3 por 2, omitiendo la tercera columna de la matriz de transformación anterior. En la tabla siguiente se muestra el diseño de la matriz de transformación de Direct2D.



|    &nbsp;       |       &nbsp;    | 
|-----------------|-----------------|
| M11Default: 1.0 | M12Default: 0.0 |
| M21Default: 0.0 | M22Default: 1.0 |
| M31OffsetX: 0.0 | M32OffsetY: 0.0 |



 

En Direct2D, esta matriz 3 por 2 se representa mediante la estructura [**\_ MATRIX \_ 3X2 de D2D1.**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) Para simplificar las operaciones de matriz comunes, Direct2D también proporciona una clase denominada [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f), que se deriva de la estructura **MATRIX \_ \_ 3X2 de D2D1.**

El constructor predeterminado de [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) deja el objeto sin inicializar. Para recuperar una matriz de identidad, use [**Matrix3x2F::Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix).

Cuando se aplica una transformación de identidad a un objeto, no cambia la posición, la forma ni el tamaño del objeto. Es similar a la manera en que multiplicar un número por 1 no cambia el número. En otras palabras, la transformación de identidad deja las coordenadas de los puntos solos y no desplaza los puntos a una nueva posición. Cualquier transformación que no sea la transformación de identidad modificará la posición, la forma o el tamaño de los objetos.

Las transformaciones tienen que ver con las coordenadas y comprender el espacio de coordenadas de Direct2D es importante para comprender el uso de las transformaciones.

## <a name="the-direct2d-coordinate-space"></a>El espacio de coordenadas de Direct2D

Direct2D usa un espacio de coordenadas a la izquierda; Es decir, los valores positivos del eje X aumentan a la derecha y los valores positivos del eje Y aumentan hacia abajo. Todo lo que aparece en la pantalla se coloca en relación con el origen, que es el punto en el que el eje X y el eje Y se intersecan (0, 0), como se muestra en la ilustración siguiente. Los destinos de representación de Direct2D usan este espacio de coordenadas.

![ilustración del eje X y el eje Y de un espacio de coordenadas a la izquierda](images/coordinatespace.png)

Al manipular valores en una matriz de transformación, puede girar, escalar, sesgar y mover (traducir) un objeto. Por ejemplo, si establece OffsetX en 100 y OffsetY en 200, mueve el objeto a los 100 píxeles derecho y 200 píxeles hacia abajo.

Para mostrar el efecto del movimiento del objeto, debe aplicar la transformación de traducción para representar destinos, pinceles o geometrías. La aplicación de una transformación para representar destinos afecta a toda la pantalla, mientras que aplicar una transformación a un pincel o una geometría solo afecta a ese pincel o geometría específicos. Para crear una matriz de transformación, use la [**clase Matrix3x2F.**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f)

## <a name="creating-transformation-matrices"></a>Crear matrices de transformación

Para crear transformaciones de rotación, escala, asimetría y traducción, la clase [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) proporciona los métodos estáticos que se muestran en la tabla siguiente. La columna Ejemplo de la tabla contiene vínculos a los temas paso a paso que muestran cómo usar cada método de transformación.



| Método                                                                   | Descripción                                                                                                     | Ejemplo                                            | Ilustración                                                                                                                            |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**matrix3x2f::rotate**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)                          | crea una transformación de rotación que tiene el ángulo y el punto central especificados.                                | [cómo girar un objeto](how-to-rotate.md)       | ![ilustración de un cuadrado girado 45 grados en el sentido de las agujas del reloj sobre el centro del cuadrado original](images/rotate-ovw.png)                 |
| [**matrix3x2f::scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f)) | crea una transformación de escala que tiene los factores de escala y el punto central especificados.                           | [cómo escalar un objeto](how-to-scale.md)         | ![ilustración de un cuadrado escalado al 130 %](images/scale-ovw.png)                                                                           |
| [**matrix3x2f::skew**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)                              | crea una transformación de sesgo que tiene los valores de eje x e Y especificados y el punto central.                 | [cómo sesgar un objeto](how-to-skew.md)           | ![ilustración de un cuadrado sesgado 30 grados en sentido contrario a las agujas del reloj desde el eje Y](images/skew-ovw.png)                                     |
| [**matrix3x2f::translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))                | crea una transformación de traducción y especifica los desplazamientos en la dirección del eje X y el eje Y. | [cómo traducir un objeto](how-to-translate.md) | ![ilustración de un cuadrado que movió 20 unidades a lo largo del eje X positivo y 10 unidades a lo largo del eje Y positivo](images/translation-ovw.png) |



 

## <a name="rendering-target-transforms"></a>Transformaciones de destino de representación

Un destino de representación es un recurso que hereda de la [**interfaz ID2D1RenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) Crea recursos para dibujar y realiza operaciones de dibujo reales. También proporciona métodos para transformar el espacio de coordenadas. Puede llamar al [**método ID2D1RenderTarget::SetTransform**](id2d1rendertarget-settransform.md) para aplicar la transformación especificada al destino de representación. Todas las operaciones de dibujo posteriores se producen en el espacio transformado.

Para representar el contenido, use los métodos de dibujo del destino de representación. Antes de empezar a dibujar, llame al [**método BeginDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) Para finalizar la representación del contenido, llame al [**método EndDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) Para obtener un ejemplo, [vea Cómo aplicar varias transformaciones a un objeto](how-to-apply-multiple-transforms.md).

## <a name="brush-transforms"></a>Transformaciones de pincel

Puede ajustar la transformación en el pincel llamando a [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)). Para esta transformación, puede pensar en el pincel como un papel grande y en las distintas primitivas de representación (texto, geometría, rectángulo, entre otras) como galerías de símbolos. Al ajustar la transformación de pincel, es como si estuviera deslizando el papel grande debajo de la galería de símbolos, sin cambiar la posición de la propia galería de símbolos. Puede usar esta técnica para que el texto se desvanezca de amarillo a negro en un espacio 3D.

Cuando la transformación de pincel es la transformación de identidad, los pinceles aparecen en el mismo espacio de coordenadas que el destino de representación en el que se dibujan. La transformación de pincel permite a un autor de llamada modificar cómo se asignan las coordenadas de pincel a este espacio.

El espacio de pincel se especifica de forma diferente en Direct2D que en Windows Presentation Foundation (WPF). En Direct2D, el espacio de pincel no es relativo al objeto que se está dibujando, sino que es el sistema de coordenadas actual del destino de representación, transformado por la transformación de pincel, si lo hay. Para que el pincel rellene un objeto como se hizo en WPF, debe traducir el origen del espacio de pincel a la esquina superior izquierda del cuadro de límite del objeto y, a continuación, escalar el espacio de pincel para que el icono base rellene el rectángulo delimitador del objeto.

Para obtener más información sobre las transformaciones de pincel, [vea Introducción a los pinceles de Direct2D.](direct2d-brushes-overview.md)

## <a name="geometry-transforms"></a>Transformaciones de geometría

Al escalar, mover, traducir o sesgar geometrías, puede aplicar directamente una transformación a una geometría específica, no a una transformación de destino de representación que afectaría a toda la pantalla. Por lo general, una transformación de destino de representación afecta al trazo y relleno de una geometría. Por el contrario, una transformación de geometría solo afecta al relleno de una geometría, ya que la transformación se aplica a una geometría antes de que se acaricia.

> [!Note]  
> A partir Windows 8, la transformación world no afecta al trazo si establece el tipo de trazo en [**D2D1 \_ STROKE TRANSFORM TYPE \_ \_ \_ FIXED**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type) o [**D2D1 \_ STROKE TRANSFORM TYPE \_ \_ \_ HAIRLINE**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type).

 

Puede ajustar la transformación en una geometría llamando a [**ID2D1Factory::CreateTransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) para crear un [**objeto ID2D1TransformedGeometry.**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) Para obtener más información sobre las transformaciones de geometría, vea Introducción a las geometrías de [Direct2D.](direct2d-geometries-overview.md)

## <a name="how-a-render-target-transform-affects-clips"></a>Cómo afecta una transformación de destino de representación a los clips

La transformación en un destino de representación afecta a cómo se calcula el rectángulo delimitador de un clip alineado con el eje. Cuando se [**llama a PushAxisAlignedClip,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) la transformación del mundo actual que se establece en el destino de representación transforma el parámetro *clipRect.* Después de aplicar la transformación a *clipRect,* se calcula el rectángulo de selección alineado con el eje para *clipRect.* Para mejorar la eficacia, el contenido se recorta a este rectángulo de selección alineado con el eje y no al *clipRect* original que se pasa. En los diagramas siguientes se muestra cómo se aplica una transformación de rotación al destino de representación, al *clipRect* resultante y a un rectángulo de selección alineado con el eje calculado.

1.  Supongamos que el rectángulo de la ilustración siguiente es un destino de representación alineado con los píxeles de la pantalla.

    ![ilustración de un rectángulo (destino de representación)](images/pushaxisalignedclip-step1-rendertarget.png)

2.  Aplique una transformación de rotación al destino de representación. En la ilustración siguiente, el rectángulo negro representa el destino de representación original y el rectángulo discontinuo rojo representa el destino de representación transformado.

    ![ilustración del rectángulo original y un rectángulo girado (destino de representación transformado)](images/pushaxisalignedclip-step2-transformed.png)

3.  Después [**de llamar a PushAxisAlignedClip,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) la transformación de rotación se aplica a *clipRect*. En la ilustración siguiente, el rectángulo azul representa el *clip transformadoRect*.

    ![ilustración de un rectángulo azul más pequeño (cliprect) dentro del rectángulo girado (destino de representación transformado)](images/pushaxisalignedclip-step3-cliprecttransformed.png)

4.  Se calcula el rectángulo de selección alineado con el eje. En la ilustración siguiente, el rectángulo discontinuo verde representa el rectángulo delimitador. Todo el contenido se recorta en este rectángulo de selección alineado con el eje.

    ![ilustración de un rectángulo de selección verde en el rectángulo azul pequeño (cliprect)](images/pushaxisalignedclip-step4-boundingbox.png)

## <a name="summary"></a>Resumen

Direct2D facilita la transformación de objetos bidimensionales con espacios de coordenadas simplificados y clases relacionadas. Mediante el uso de varios tipos de transformaciones, puede traducir, girar, sesgar y escalar los objetos para lograr muchos efectos visuales impresionantes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct2D](reference.md)
</dt> </dl>

 

 