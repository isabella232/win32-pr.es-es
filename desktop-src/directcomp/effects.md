---
title: Efectos (DirectComposition)
description: En este tema se describen los aspectos básicos de los efectos de DirectComposition de Microsoft y se describen los tipos de efectos que DirectComposition admite.
ms.assetid: 805B17D2-2F6B-4C25-8C6D-41FFA5DFC774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cfd1ca154dcbc7e55ca65cc34d04cfa7d73ccee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420892"
---
# <a name="effects-directcomposition"></a>Efectos (DirectComposition)

> [!NOTE]
> En el caso de las aplicaciones de Windows 10, se recomienda usar las API de Windows. UI. Composition en lugar de DirectComposition. Para obtener más información, consulte [modernice su aplicación de escritorio con el nivel de objetos visuales](/windows/uwp/composition/visual-layer-in-desktop-apps).

En este tema se describen los aspectos básicos de los efectos de DirectComposition de Microsoft y se describen los tipos de efectos que DirectComposition admite.

Este tema contiene las siguientes secciones:

-   [¿Qué es un efecto de DirectComposition?](#what-is-a-directcomposition-effect)
-   [Opacidad](#opacity)
-   [efectos de transformación de perspectiva 3D](#3d-perspective-transform-effects)
    -   [El espacio de coordenadas 3D de DirectComposition](#the-directcomposition-3d-coordinate-space)
    -   [efecto de transformación de giro 3D](#3d-rotation-transform-effect)
    -   [efecto de transformación de escala 3D](#3d-scaling-transform-effect)
    -   [efecto transformación de traslación 3D](#3d-translation-transform-effect)
    -   [efecto transformación de matriz 3D](#3d-matrix-transform-effect)
    -   [Grupo de efectos de transformación 3D](#3d-transform-effect-group)
-   [Objetos de efecto](#effect-objects)
-   [Temas relacionados](#related-topics)

## <a name="what-is-a-directcomposition-effect"></a>¿Qué es un efecto de DirectComposition?

Un *efecto* de DirectComposition es una operación de mapa de bits que se aplica durante la rasterización de un objetos visuales para cambiar la apariencia del visual de alguna manera.

DirectComposition crea un efecto tomando un subárbol visual y lo representa en un único mapa de bits antes de aplicar el efecto. Por ejemplo, para crear un efecto de transformación de perspectiva 3D, DirectComposition genera una imagen de un subárbol visual y, a continuación, textura la imagen en un plano 3D que se transforma según la matriz resultante del efecto de transformación 3D.

DirectComposition admite los siguientes tipos de efectos.



| Tipo de efecto                                                   | Descripción                                                                |
|---------------------------------------------------------------|----------------------------------------------------------------------------|
| [Opacidad](#opacity)                                           | Establece la opacidad de un visual completo.                                      |
| [transformación de perspectiva 3D](#3d-perspective-transform-effects) | Aplica un efecto de transformación de perspectiva tridimensional (3D) a un visual. |



 

> [!Note]  
> DirectComposition no realiza ningún procesamiento especial al aplicar efectos al contenido estéreo 3D. Esto significa que el contenido 3D podría aparecer distorsionado cuando se le aplica un efecto.

 

## <a name="opacity"></a>Opacidad

El efecto opacidad le permite establecer el factor de opacidad que se aplica a un visual completo cuando se representa el visual. Difiere de una máscara alfa en que se aplica el mismo factor de opacidad a todos los píxeles del control visual. La opacidad se especifica como un valor comprendido entre 0 (completamente transparente) y 1 (completamente opaco).

El factor de opacidad se aplica desde los objetos visuales primarios y secundarios, pero los efectos visibles de la configuración de opacidad anidada no se indican en el valor de propiedad de los objetos visuales secundarios individuales. Por ejemplo, si un elemento visual raíz tiene una opacidad del 50% (0,5) y uno de sus elementos secundarios tiene una opacidad del 20% (0,2), la opacidad neta de ese elemento secundario se representa como 10% (0,1), pero el valor de la propiedad opacidad del elemento secundario seguirá siendo 0,2.

## <a name="3d-perspective-transform-effects"></a>efectos de transformación de perspectiva 3D

En esta sección se describe el espacio de coordenadas que usa DirectComposition para realizar efectos de transformación de perspectiva 3D. También se describen los tipos de efectos de transformación de perspectiva 3D que admite DirectComposition.

-   [El espacio de coordenadas 3D de DirectComposition](#the-directcomposition-3d-coordinate-space)
-   [efecto de transformación de giro 3D](#3d-rotation-transform-effect)
-   [efecto de transformación de escala 3D](#3d-scaling-transform-effect)
-   [efecto transformación de traslación 3D](#3d-translation-transform-effect)
-   [efecto transformación de matriz 3D](#3d-matrix-transform-effect)
-   [Grupo de efectos de transformación 3D](#3d-transform-effect-group)

> [!Note]  
> En DirectComposition, la aplicación de efectos 3D a varios niveles del árbol visual no funciona de la misma manera que con un motor 3D completo como Microsoft Direct3D. Por ejemplo, considere un objeto visual primario que tiene un solo objeto visual secundario. Si el objeto visual secundario se gira hacia delante en la dirección z (alrededor del eje y) en 90 grados, el borde del lado visual secundario se vería en el visor y, por tanto, esperamos que el objeto visual no esté visible (porque un mapa de bits no tiene ninguna profundidad real). Si el objeto visual primario se gira hacia atrás en la dirección z negativa (alrededor del eje y) en 90 grados, es posible que el objeto visual secundario se vuelva totalmente visible (ya que las transformaciones se niegan entre sí). Sin embargo, en DirectComposition este no es el caso. El objeto visual secundario no será visible porque se "aplanaó" en el mapa de bits primario.

 

### <a name="the-directcomposition-3d-coordinate-space"></a>El espacio de coordenadas 3D de DirectComposition

El espacio de coordenadas de DirectComposition para los efectos de transformación 3D localiza el origen (0,0) en la esquina superior izquierda de la superficie de mapa de bits, con los valores positivos del eje x que van hacia la derecha, los valores positivos del eje y continúan hacia abajo y los valores positivos del eje z continúan fuera del origen, hacia el visor. En esta ilustración se muestra el espacio de coordenadas 3D DirectComposition.

![directcompostion espacio de coordenadas 3D](images/3d-coordinate-space.png)

### <a name="3d-rotation-transform-effect"></a>efecto de transformación de giro 3D

Un efecto de transformación de giro 3D gira un visual de tres dimensiones por el ángulo especificado sobre un vector \[ x, y, z de eje de giro \] situado en el punto central especificado (x, y, z). El ángulo se especifica en grados. El vector de eje de giro predeterminado es \[ 0, 0,-1 \] y el punto central predeterminado es (0, 0,0).

Use el método [**IDCompositionDevice:: CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d) para crear un objeto de transformación de giro 3D. El método recupera una interfaz [**IDCompositionRotateTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform3d) que puede usar para establecer las propiedades del objeto.

### <a name="3d-scaling-transform-effect"></a>efecto de transformación de escala 3D

Un efecto de transformación de escala 3D hace que un visual sea más grande o más pequeño. Escala un visual en la \[ dirección x, y, z \] sobre el punto central (x, y, z). El punto central predeterminado es (0, 0, 0).

Use el método [**IDCompositionDevice:: CreateScaleTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform3d) para crear un objeto de transformación de escala 3D. El método recupera una interfaz [**IDCompositionScaleTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform3d) que puede usar para establecer las propiedades del objeto.

### <a name="3d-translation-transform-effect"></a>efecto transformación de traslación 3D

Un efecto transformación de traslación 3D cambia la posición de un visual en la \[ dirección x, y, z \] .

Use el método [**IDCompositionDevice:: CreateTranslateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform3d) para crear un objeto de transformación de traslación 3D. El método recupera una interfaz [**IDCompositionTranslateTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform3d) que puede usar para establecer las propiedades del objeto.

### <a name="3d-matrix-transform-effect"></a>efecto transformación de matriz 3D

La interfaz [**IDCompositionMatrixTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) permite definir su propia matriz de transformación de 4 por 4 y aplicarla a un visual. Esta interfaz es útil si necesita aplicar un tipo de efecto de transformación de perspectiva 3D que no está disponible a través de las otras interfaces de efecto de transformación 3D de DirectComposition. La matriz se define rellenando una estructura [**D3DMATRIX**](/windows/desktop/direct3d10/d3d10-d3dmatrix) y pasándola al método [**IDCompositionMatrixTransform3D:: SetMatrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) . Como alternativa, puede establecer cada elemento de la matriz mediante el método [**IDCompositionMatrixTransform3D:: SetMatrixElement**](/previous-versions/windows/desktop/legacy/hh437429(v=vs.85)) .

### <a name="3d-transform-effect-group"></a>Grupo de efectos de transformación 3D

[**IDCompositionDevice:: CreateTransform3DGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransform3dgroup) crea una colección de efectos de transformación 3D que se pueden aplicar a un visual como un grupo. La matriz puede incluir cualquier número de objetos de transformación y puede incluir transformaciones matricial, de rotación, de escala y de traducción. La colección de objetos de transformación 3D da como resultado una transformación cuyo valor es la multiplicación de matriz de las matrices de transformación individuales de la colección.

Es importante el orden de las transformaciones individuales en el grupo. Por ejemplo, si primero se gira, después se realiza la escala y después se traduce, se obtiene un resultado diferente que si primero se traslada, después se gira y luego se escala. DirectComposition respeta el orden en que se especifican las transformaciones 3D dentro de un grupo 3D de transformación de la misma forma que lo hace para las transformaciones 2D. Además, las transformaciones de perspectiva 3D producen una reducción del árbol visual una vez aplicadas todas las transformaciones 3D del visual actual. Esto se hace para asegurarse de que la escena sea lo más parecida posible a 3D.

## <a name="effect-objects"></a>Objetos de efecto

Para aplicar un efecto a un objeto visual, primero debe crear y establecer las propiedades de un objeto de efecto que represente el tipo de efecto que desea producir en el objeto visual. A continuación, debe aplicar el objeto de efecto a la propiedad de efecto del objeto visual.

Para crear un objeto de efecto, use uno de los siguientes métodos de la interfaz [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) para crear un objeto de efecto para el tipo de efecto que desee. Los métodos siguientes crean objetos de efecto:

-   [**CreateMatrixTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-creatematrixtransform3d)
-   [**CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d)
-   [**CreateScaleTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform3d)
-   [**CreateTranslateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform3d)

Cada uno de los métodos anteriores recupera una interfaz que puede usar para establecer las propiedades del objeto de efecto que se acaba de crear. Utilice los métodos de interfaz para establecer las propiedades según sea necesario para generar el efecto visual que desee.

La mayoría de las propiedades de un objeto Effect se pueden animar. Para animar una propiedad determinada, cree un objeto Animation y aplíquelo a la propiedad que desee animar; en caso contrario, establezca la propiedad en un valor estático que produzca el efecto que desee. Para obtener más información sobre cómo animar propiedades, vea [animación](animation.md).

Para aplicar un objeto de efecto a visual, llame al método [**IDCompositionVisual:: SetEffect**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect) . Al aplicar un efecto a un visual, el efecto se aplica a todo el subárbol visual cuya raíz se encuentra en ese visual. Por lo tanto, por ejemplo, si establece la opacidad de un objeto visual en 50 por ciento, la opacidad de todos los objetos visuales secundarios en el subárbol visual se reducirá en un 50 por ciento. Puede aplicar el mismo objeto de efecto a uno o varios objetos visuales. Si modifica las propiedades de un objeto de efecto después de aplicarlo a los objetos visuales, se recomponen todos los objetos visuales para reflejar el cambio.

Mediante el uso de un objeto de grupo de efectos, puede aplicar simultáneamente varios efectos a un objeto visual. En primer lugar, llame a [**IDCompositionDevice:: CreateEffectGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createeffectgroup) para crear el objeto de grupo de efectos y, a continuación, agregue efectos al grupo mediante la interfaz [**IDCompositionEffectGroup**](/windows/win32/api/dcomp/nn-dcomp-idcompositioneffectgroup) del objeto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 