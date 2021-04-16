---
title: Transformaciones (DirectComposition)
description: En este tema se describe la compatibilidad de Microsoft DirectComposition con las transformaciones afín (linear) bidimensionales (2D) y se describen los tipos de transformaciones que admite DirectComposition.
ms.assetid: a0f41cc6-e848-4831-8063-609e17d9b4c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27a1fec5774d208f240e6d2f1c8b7df09d25c486
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104553076"
---
# <a name="transforms-directcomposition"></a>Transformaciones (DirectComposition)

> [!NOTE]
> En el caso de las aplicaciones de Windows 10, se recomienda usar las API de Windows. UI. Composition en lugar de DirectComposition. Para obtener más información, consulte [modernice su aplicación de escritorio con el nivel de objetos visuales](/windows/uwp/composition/visual-layer-in-desktop-apps).

En este tema se describe la compatibilidad de Microsoft DirectComposition con las transformaciones afín (linear) bidimensionales (2D) y se describen los tipos de transformaciones que admite DirectComposition.

DirectComposition también admite transformaciones de perspectiva 3D, pero dado que requieren la creación de un mapa de bits intermedio, DirectComposition considera que son efectos en lugar de transformaciones. Para obtener información sobre los efectos de transformación de perspectiva 3D, vea [efectos](effects.md).

Este tema incluye las siguientes secciones:

-   [¿Qué es una transformación 2D de DirectComposition?](#what-is-a-directcomposition-2d-transform)
-   [El espacio de coordenadas 2D de DirectComposition](#the-directcomposition-2d-coordinate-space)
-   [Compatibilidad con las transformaciones de 2D afines](#support-for-affine-2d-transforms)
-   [Transformaciones 2D de matriz](#matrix-2d-transforms)
-   [Transformar grupos](#transform-groups)
-   [Animación de transformación](#transform-animation)
-   [Temas relacionados](#related-topics)

## <a name="what-is-a-directcomposition-2d-transform"></a>¿Qué es una transformación 2D de DirectComposition?

Una transformación 2D permite modificar la posición, el tamaño o la naturaleza de un visual en dos dimensiones moviendo el visual a otra ubicación (traslación), haciéndolo mayor o menor (escalado), convirtiéndolo (giro) o distorsionando su forma (sesgado).

Una transformación 2D se logra asignando los puntos de un visual de una posición a otra dentro del mismo espacio de coordenadas o de un espacio de coordenadas a otro. Esta asignación se describe mediante una tabla de valores denominada matriz de transformación, definida como una colección de tres filas con tres columnas de valores de punto flotante, como se muestra en la tabla siguiente.



|                 |                 |     |
|-----------------|-----------------|-----|
| M11Default: 1,0 | M12Default: 0,0 | 0,0 |
| M21Default: 0,0 | M22Default: 1,0 | 0,0 |
| M31OffsetX: 0,0 | M32OffsetY: 0,0 | 1,0 |



 

La matriz de transformación de las transformaciones de 2D afines es una matriz de 3 por 2 que omite la tercera columna de la matriz de transformación anterior. En la tabla siguiente se muestra el diseño de esta matriz.



|                 |                 |
|-----------------|-----------------|
| M11Default: 1,0 | M12Default: 0,0 |
| M21Default: 0,0 | M22Default: 1,0 |
| M31OffsetX: 0,0 | M32OffsetY: 0,0 |



 

> [!Note]  
> DirectComposition no realiza ningún procesamiento especial al aplicar transformaciones 2D al contenido estéreo. Esto significa que el contenido 3D podría aparecer distorsionado cuando se le aplica una transformación 2D.

 

## <a name="the-directcomposition-2d-coordinate-space"></a>El espacio de coordenadas 2D de DirectComposition

DirectComposition usa un espacio de coordenadas 2D de la mano izquierda; es decir, los valores positivos del eje x se incrementan a la derecha y los valores positivos del eje y aumentan hacia abajo. Los objetos visuales se colocan en relación con el origen, que es el punto en el que el eje x e y forman una intersección (0,0), tal como se muestra en la siguiente ilustración.

![los ejes x e y de un espacio de coordenadas de la mano izquierda](images/coordinatespace.png)

Al manipular los valores de una matriz de transformación de 3 por 2, puede girar, escalar, sesgar y trasladar un objeto en dos dimensiones. Por ejemplo, si establece OffsetX en 100 y PosiciónInicial en 200, mueva el objeto a la derecha 100 píxeles y Down 200 píxeles.

## <a name="support-for-affine-2d-transforms"></a>Compatibilidad con las transformaciones de 2D afines

En la tabla siguiente se describen los tipos de transformaciones de 2D afines admitidas por DirectComposition y se enumeran las interfaces que puede usar para realizar los distintos tipos de transformaciones.



| Transformación/interfaz                                                                               | Descripción                                                                                              | Ilustración                                                                                                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Girar línea de [**Idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)2D \[\]          | gira un visual el ángulo especificado sobre el punto central especificado.                                 | ![Ilustración de un cuadrado girado 45 grados en el sentido de las agujas del reloj sobre el centro del cuadrado original](images/rotate.png)               |
| Escala de[](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform) \[ línea idcompositionscaletransform 2D\]             | escalar un objetos visual según el factor especificado sobre el punto central especificado.                                 | ![Ilustración de un cuadrado escalado 130 por ciento](images/scale.png)                                                                  |
| Sesgar línea de [**Idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)2D \[\]                | sesgar un objetos visual según el ángulo especificado a lo largo del eje x e y, en torno al punto central especificado. | ![Ilustración de un cuadrado sesgado de 30 grados en sentido contrario a las agujas del reloj desde el eje y](images/skew.png)                                   |
| Trasladar[](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) \[ nueva línea de idcompositiontranslatetransform 2D\] | cambie la posición de un visual en la dirección de los ejes x e y.                               | ![la ilustración de un cuadrado ha desplazado 20 unidades a lo largo del eje x positivo y 10 unidades a lo largo del eje y positivo](images/translate.png) |



 

## <a name="matrix-2d-transforms"></a>Transformaciones 2D de matriz

La interfaz [**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) permite definir su propia matriz de transformación 2D afín de 3 por 2 y aplicarla a un visual. Esta interfaz es útil si necesita aplicar un tipo de transformación de 2D afín que no está disponible a través de las otras interfaces de transformación de DirectComposition. La matriz se define rellenando una estructura de [**D2D \_ matriz \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) y pasándola al método [**IDCompositionMatrixTransform:: SetMatrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) .

## <a name="transform-groups"></a>Transformar grupos

Puede usar los grupos de transformación para combinar varias transformaciones en una. Un grupo de transformación define una colección de objetos Transform cuyas matrices se multiplican juntas en el orden en que se especifican en la colección. A continuación, la matriz de transformación resultante se aplica al visual. Un grupo de transformación produce el mismo resultado que aplicar cada transformación por separado.

Tenga en cuenta que el orden de los objetos de transformación en un grupo de transformación es importante. Por ejemplo, si un visual se gira primero, después se escala y, a continuación, se traduce, el resultado es diferente de si el visual se traduce primero, después se gira y luego se escala. DirectComposition siempre aplica las transformaciones a un objeto visual en el orden en que se especifican en la colección.

Para crear un grupo de transformaciones, primero debe crear los objetos de transformación que desea incluir en el grupo y, a continuación, pasar una matriz de punteros de objeto de transformación al método [**IDCompositionDevice:: CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) . Después de crear un grupo de transformaciones, no puede agregar ni quitar objetos de transformación. Sin embargo, puede modificar las propiedades de los objetos de transformación individuales de la colección y los cambios se reflejarán en la matriz de transformación resultante.

## <a name="transform-animation"></a>Animación de transformación

Las propiedades de una transformación se pueden animar. Cuando se anima una propiedad, DirectComposition cambia el valor de la propiedad a lo largo del tiempo, en lugar de todos a la vez. Esto es especialmente útil cuando se crean transiciones. Para obtener más información, vea [animación](animation.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 
