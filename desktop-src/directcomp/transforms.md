---
title: Transformaciones (DirectComposition)
description: En este tema se describe la compatibilidad de Microsoft DirectComposition con transformaciones afín bidimensionales (2D) (lineales) y se describen los tipos de transformaciones que admite DirectComposition.
ms.assetid: a0f41cc6-e848-4831-8063-609e17d9b4c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c8cc34975ab8304300a1523269808775107f4ce0554432da8c3c04a01f25881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504807"
---
# <a name="transforms-directcomposition"></a>Transformaciones (DirectComposition)

> [!NOTE]
> Para las aplicaciones de Windows 10, se recomienda usar Windows.UI.Composition API en lugar de DirectComposition. Para obtener más información, [consulte Modernización de la aplicación de escritorio mediante la capa visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

En este tema se describe la compatibilidad de Microsoft DirectComposition con transformaciones afín bidimensionales (2D) (lineales) y se describen los tipos de transformaciones que admite DirectComposition.

DirectComposition también admite transformaciones de perspectiva 3D, pero como requieren la creación de un mapa de bits intermedio, DirectComposition las considera efectos en lugar de transformaciones. Para obtener información sobre los efectos de transformación de perspectiva 3D, vea [Efectos](effects.md).

Este tema incluye las siguientes secciones:

-   [¿Qué es una transformación 2D de DirectComposition?](#what-is-a-directcomposition-2d-transform)
-   [El espacio de coordenadas 2D de DirectComposition](#the-directcomposition-2d-coordinate-space)
-   [Compatibilidad con transformaciones 2D afín](#support-for-affine-2d-transforms)
-   [Transformaciones 2D de matriz](#matrix-2d-transforms)
-   [Transformar grupos](#transform-groups)
-   [Animación de transformación](#transform-animation)
-   [Temas relacionados](#related-topics)

## <a name="what-is-a-directcomposition-2d-transform"></a>¿Qué es una transformación 2D de DirectComposition?

Una transformación 2D le permite modificar la posición, el tamaño o la naturaleza de un objeto visual en dos dimensiones moviendo el objeto visual a otra ubicación (traducción), lo hace más grande o más pequeño (escalado), lo convierte (rotación) o distorsiona su forma (sesgo).

Una transformación 2D se logra mediante la asignación de los puntos de un objeto visual de una posición a otra dentro del mismo espacio de coordenadas, o de un espacio de coordenadas a otro. Esta asignación se describe mediante una tabla de valores denominada matriz de transformación, definida como una colección de tres filas con tres columnas de valores de punto flotante, como se muestra en la tabla siguiente.

:::row:::
    :::column:::
        M11Default: 1.0<br/>
        M21Default: 0.0<br/>
        M31OffsetX: 0,0
    :::column-end:::
    :::column:::
        M12Default: 0.0<br/>
        M22Default: 1.0<br/>
        M32OffsetY: 0,0
    :::column-end:::
    :::column:::
        0,0<br/>
        0,0<br/>
        1.0
    :::column-end:::
:::row-end:::

La matriz de transformación para transformaciones 2D afínes es una matriz 3 por 2 que omite la tercera columna de la matriz de transformación anterior. En la tabla siguiente se muestra el diseño de esta matriz.

:::row:::
    :::column:::
        M11Default: 1.0<br/>
        M21Default: 0.0<br/>
        M31OffsetX: 0,0
    :::column-end:::
    :::column:::
        M12Default: 0.0<br/>
        M22Default: 1.0<br/>
        M32OffsetY: 0,0
    :::column-end:::
:::row-end:::

> [!Note]  
> DirectComposition no realiza ningún procesamiento especial al aplicar transformaciones 2D al contenido estéreo. Esto significa que el contenido 3D puede aparecer distorsionado cuando se le aplica una transformación 2D.

 

## <a name="the-directcomposition-2d-coordinate-space"></a>El espacio de coordenadas 2D de DirectComposition

DirectComposition usa un espacio de coordenadas 2D a la izquierda; Es decir, los valores positivos del eje x aumentan a la derecha y los valores positivos del eje Y aumentan hacia abajo. Los objetos visuales se sitúan en relación con el origen, que es el punto en el que el eje X y el eje Y se intersecan (0, 0), como se muestra en la ilustración siguiente.

![los ejes X e Y de un espacio de coordenadas izquierdo](images/coordinatespace.png)

Al manipular valores en una matriz de transformación 3 por 2, puede girar, escalar, sesgar y traducir un objeto en dos dimensiones. Por ejemplo, si establece OffsetX en 100 y OffsetY en 200, mueva el objeto a la derecha 100 píxeles y 200 píxeles hacia abajo.

## <a name="support-for-affine-2d-transforms"></a>Compatibilidad con transformaciones 2D afín

En la tabla siguiente se describen los tipos de transformaciones 2D afín compatibles con DirectComposition y se enumeran las interfaces que puede usar para realizar los distintos tipos de transformaciones.



| Transformación o interfaz                                                                               | Descripción                                                                                              | Ilustración                                                                                                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Rotate 2D [**idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform) \[ newline\]          | girar un objeto visual por el ángulo especificado sobre el punto central especificado.                                 | ![ilustración de un cuadrado girado 45 grados en el sentido de las agujas del reloj sobre el centro del cuadrado original](images/rotate.png)               |
| Escala de la nueva línea [**idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform) \[ en 2D\]             | escalar un objeto visual por el factor especificado sobre el punto central especificado.                                 | ![ilustración de un cuadrado escalado al 130 por ciento](images/scale.png)                                                                  |
| Sesgo 2D [**idcompositionpositionwtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform) \[ newline\]                | sesgar un objeto visual por el ángulo especificado a lo largo del eje X y el eje Y, y alrededor del punto central especificado. | ![ilustración de un cuadrado sesgado a 30 grados en sentido contrario a las agujas del reloj desde el eje Y](images/skew.png)                                   |
| Translate 2D [**idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) \[ newline\] | cambiar la posición de un objeto visual en la dirección del eje X y el eje Y.                               | ![ilustración de un cuadrado movido 20 unidades a lo largo del eje X positivo y 10 unidades a lo largo del eje Y positivo](images/translate.png) |



 

## <a name="matrix-2d-transforms"></a>Transformaciones 2D de matriz

La [**interfaz IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) permite definir su propia matriz de transformación 2D afín 3 por 2 y aplicarla a un objeto visual. Esta interfaz es útil si necesita aplicar un tipo de transformación 2D afín que no está disponible a través de las otras interfaces de transformación de DirectComposition. Para definir la matriz, rellene una estructura [**D2D \_ MATRIX \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) y la pase al [**método IDCompositionMatrixTransform::SetMatrix.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix)

## <a name="transform-groups"></a>Transformar grupos

Puede usar grupos de transformación para combinar varias transformaciones en una. Un grupo de transformación define una colección de objetos de transformación cuyas matrices se multiplican juntas en el orden en que se especifican en la colección. A continuación, la matriz de transformación resultante se aplica al objeto visual. Un grupo de transformación genera el mismo resultado que aplicar cada transformación por separado.

Tenga en cuenta que el orden de los objetos de transformación en un grupo de transformación es importante. Por ejemplo, si un objeto visual se gira primero, luego se escala y, a continuación, se traduce, el resultado es diferente de si el objeto visual se traduce primero, luego gira y, a continuación, se escala. DirectComposition siempre aplica las transformaciones a un objeto visual en el orden en que se especifican en la colección.

Para crear un grupo de transformación, cree primero los objetos de transformación que desea incluir en el grupo y, a continuación, pase una matriz de punteros de objeto de transformación al [**método IDCompositionDevice::CreateTransformGroup.**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) Después de crear un grupo de transformación, no puede agregar ni quitar ningún objeto de transformación. Sin embargo, puede modificar las propiedades de los objetos de transformación individuales de la colección y los cambios se reflejarán en la matriz de transformación resultante.

## <a name="transform-animation"></a>Animación de transformación

Las propiedades de una transformación se pueden animar. Cuando se anima una propiedad, DirectComposition cambia el valor de la propiedad a lo largo del tiempo, en lugar de todos a la vez. Esto es especialmente útil al crear transiciones. Para obtener más información, vea [Animation](animation.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 
