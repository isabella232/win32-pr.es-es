---
title: Efectos (DirectComposition)
description: En este tema se describen los conceptos básicos de los efectos de Microsoft DirectComposition y se describen los tipos de efectos que admite DirectComposition.
ms.assetid: 805B17D2-2F6B-4C25-8C6D-41FFA5DFC774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c5119367a35725a85efe20b8ba4d0f9f9887ff91b4d9618e2215bedfbfef67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117905060"
---
# <a name="effects-directcomposition"></a>Efectos (DirectComposition)

> [!NOTE]
> Para las aplicaciones Windows 10, se recomienda usar Windows.UI.Composition API en lugar de DirectComposition. Para obtener más información, [consulte Modernización de la aplicación de escritorio mediante la capa visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

En este tema se describen los conceptos básicos de los efectos de Microsoft DirectComposition y se describen los tipos de efectos que admite DirectComposition.

Este tema contiene las siguientes secciones:

-   [¿Qué es un efecto DirectComposition?](#what-is-a-directcomposition-effect)
-   [Opacidad](#opacity)
-   [Efectos de transformación de perspectiva 3D](#3d-perspective-transform-effects)
    -   [El espacio de coordenadas 3D de DirectComposition](#the-directcomposition-3d-coordinate-space)
    -   [Efecto de transformación de rotación 3D](#3d-rotation-transform-effect)
    -   [Efecto de transformación de escalado 3D](#3d-scaling-transform-effect)
    -   [Efecto de transformación de traducción 3D](#3d-translation-transform-effect)
    -   [Efecto de transformación de matriz 3D](#3d-matrix-transform-effect)
    -   [Grupo de efectos de transformación 3D](#3d-transform-effect-group)
-   [Objetos de efecto](#effect-objects)
-   [Temas relacionados](#related-topics)

## <a name="what-is-a-directcomposition-effect"></a>¿Qué es un efecto DirectComposition?

Un efecto *DirectComposition* es una operación de mapa de bits que se aplica durante la rasterización de un objeto visual para cambiar la apariencia del objeto visual de alguna manera.

DirectComposition crea un efecto tomando un subárbol visual y representandolo en un único mapa de bits antes de aplicar el efecto. Por ejemplo, para crear un efecto de transformación de perspectiva 3D, DirectComposition genera una imagen de un subárido visual y, a continuación, crea texturas de la imagen en un plano 3D que se transforma según la matriz resultante del efecto de transformación 3D.

DirectComposition admite los siguientes tipos de efectos.



| Tipo de efecto                                                   | Descripción                                                                |
|---------------------------------------------------------------|----------------------------------------------------------------------------|
| [Opacidad](#opacity)                                           | Establece la opacidad de un objeto visual completo.                                      |
| [Transformación de perspectiva 3D](#3d-perspective-transform-effects) | Aplica un efecto de transformación de perspectiva tridimensional (3D) a un objeto visual. |



 

> [!Note]  
> DirectComposition no realiza ningún procesamiento especial al aplicar efectos al contenido estéreo 3D. Esto significa que el contenido 3D puede aparecer distorsionado cuando se le aplica un efecto.

 

## <a name="opacity"></a>Opacidad

El efecto de opacidad le permite establecer el factor de opacidad que se aplica a todo un objeto visual cuando se representa el objeto visual. Difiere de una máscara alfa en que se aplica el mismo factor de opacidad a todos los píxeles del objeto visual. La opacidad se especifica como un valor que va de 0 (completamente transparente) a 1 (completamente opaco).

El factor de opacidad se aplica de objetos visuales primarios a secundarios, pero los efectos visibles de la configuración de opacidad anidada no se indican en el valor de propiedad de objetos visuales secundarios individuales. Por ejemplo, si un objeto visual raíz tiene una opacidad del 50 % (0,5) y uno de sus elementos secundarios tiene una opacidad del 20 % (0,2), la opacidad neta de ese elemento secundario se representa como 10 % (0,1), pero el valor de la propiedad Opacity del elemento secundario seguiría siendo 0,2.

## <a name="3d-perspective-transform-effects"></a>Efectos de transformación de perspectiva 3D

En esta sección se describe el espacio de coordenadas que Usa DirectComposition para realizar efectos de transformación de perspectiva 3D. También se describen los tipos de efectos de transformación de perspectiva 3D que admite DirectComposition.

-   [El espacio de coordenadas 3D de DirectComposition](#the-directcomposition-3d-coordinate-space)
-   [Efecto de transformación de rotación 3D](#3d-rotation-transform-effect)
-   [Efecto de transformación de escalado 3D](#3d-scaling-transform-effect)
-   [Efecto de transformación de traducción 3D](#3d-translation-transform-effect)
-   [Efecto de transformación de matriz 3D](#3d-matrix-transform-effect)
-   [Grupo de efectos de transformación 3D](#3d-transform-effect-group)

> [!Note]  
> En DirectComposition, la aplicación de efectos 3D a varios niveles en el árbol visual no funciona de la misma manera que con un motor 3D completo, como Microsoft Direct3D. Por ejemplo, considere un objeto visual primario que tiene un único objeto visual secundario. Si el objeto visual secundario gira hacia delante en la dirección z (alrededor del eje Y) en 90 grados, el borde del borde visual secundario se enfrentaría al visor, por lo que se esperaría que el objeto visual no sea visible (porque un mapa de bits no tiene profundidad real). Si el objeto visual primario gira hacia atrás en la dirección z negativa (alrededor del eje Y) en 90 grados, es posible que esperemos que el objeto visual secundario se vuelva totalmente visible (ya que las transformaciones se negan entre sí). Sin embargo, en DirectComposition este no es el caso. El objeto visual secundario no será visible porque se "aplanó" en el mapa de bits primario.

 

### <a name="the-directcomposition-3d-coordinate-space"></a>El espacio de coordenadas 3D de DirectComposition

El espacio de coordenadas DirectComposition para los efectos de transformación 3D localiza el origen (0,0,0) en la esquina superior izquierda de la superficie de mapa de bits, con valores positivos del eje X que se dirigen a la derecha, valores positivos del eje Y que avanzan hacia abajo y valores positivos del eje Z que se dirigen hacia el exterior desde el origen, hacia el visor. En esta ilustración se muestra el espacio de coordenadas 3D de DirectComposition.

![espacio de coordenadas 3d de directcompostion](images/3d-coordinate-space.png)

### <a name="3d-rotation-transform-effect"></a>Efecto de transformación de rotación 3D

Un efecto de transformación de rotación 3D gira un objeto visual en tres dimensiones por el ángulo especificado sobre un vector de eje de rotación x,y,z ubicado en el punto central \[ \] especificado (x,y,z). El ángulo se especifica en grados. El vector del eje de rotación predeterminado es \[ 0,0,-1 y el punto central predeterminado \] es (0,0,0).

Use el [**método IDCompositionDevice::CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d) para crear un objeto de transformación de rotación 3D. El método recupera una [**interfaz IDCompositionRotateTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform3d) que puede usar para establecer las propiedades del objeto.

### <a name="3d-scaling-transform-effect"></a>Efecto de transformación de escalado 3D

Un efecto de transformación de escalado 3D hace que un objeto visual sea mayor o menor. Escala un objeto visual en la dirección \[ x,y,z \] sobre el punto central (x, y,z). El punto central predeterminado es (0,0,0).

Use el [**método IDCompositionDevice::CreateScaleTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform3d) para crear un objeto de transformación de escalado 3D. El método recupera una [**interfaz IDCompositionScaleTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform3d) que puede usar para establecer las propiedades del objeto .

### <a name="3d-translation-transform-effect"></a>Efecto de transformación de traducción 3D

Un efecto de transformación de traducción 3D cambia la posición de un objeto visual en la \[ dirección x,y,z. \]

Use el [**método IDCompositionDevice::CreateTranslateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform3d) para crear un objeto de transformación de traducción 3D. El método recupera una [**interfaz IDCompositionTranslateTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform3d) que puede usar para establecer las propiedades del objeto.

### <a name="3d-matrix-transform-effect"></a>Efecto de transformación de matriz 3D

La [**interfaz IDCompositionMatrixTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) permite definir su propia matriz de transformación 4 por 4 y aplicarla a un objeto visual. Esta interfaz es útil si necesita aplicar un tipo de efecto de transformación de perspectiva 3D que no está disponible a través de las otras interfaces de efecto de transformación 3D de DirectComposition. Para definir la matriz, rellene una estructura [**D3DMATRIX**](/windows/desktop/direct3d10/d3d10-d3dmatrix) y la pase al [**método IDCompositionMatrixTransform3D::SetMatrix.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) Como alternativa, puede establecer cada elemento de la matriz mediante el método [**IDCompositionMatrixTransform3D::SetMatrixElement.**](/previous-versions/windows/desktop/legacy/hh437429(v=vs.85))

### <a name="3d-transform-effect-group"></a>Grupo de efectos de transformación 3D

[**IDCompositionDevice::CreateTransform3DGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransform3dgroup) crea una colección de efectos de transformación 3D que se pueden aplicar a un objeto visual como grupo. La matriz puede incluir cualquier número de objetos de transformación y puede incluir transformaciones de matriz, rotación, escala y traducción. La colección de objetos de transformación 3D da como resultado una transformación cuyo valor es la multiplicación de matriz de las matrices de transformación individuales de la colección.

El orden de las transformaciones individuales en el grupo es importante. Por ejemplo, si gira primero, escala y, a continuación, traduce, obtiene un resultado diferente al de si primero traduce, gira y, a continuación, escala. DirectComposition respeta el orden en el que se especifican las transformaciones 3D dentro de un grupo 3D de transformación de la misma manera que lo hace para las transformaciones 2D. Además, las transformaciones de perspectiva 3D tienen como resultado el aplanado del árbol visual después de que se hayan aplicado todas las transformaciones 3D del objeto visual actual. Esto se hace para asegurarse de que la escena tiene el aspecto más cercano posible a 3D.

## <a name="effect-objects"></a>Objetos de efecto

Para aplicar un efecto a un objeto visual, primero debe crear y establecer las propiedades de un objeto de efecto que representa el tipo de efecto que desea generar en el objeto visual. A continuación, debe aplicar el objeto de efecto a la propiedad Effect del objeto visual.

Para crear un objeto de efecto, use uno de los siguientes métodos de interfaz [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) para crear un objeto de efecto para el tipo de efecto que desee. Los métodos siguientes crean objetos de efecto:

-   [**CreateMatrixTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-creatematrixtransform3d)
-   [**CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d)
-   [**CreateScaleTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform3d)
-   [**CreateTranslateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform3d)

Cada uno de los métodos anteriores recupera una interfaz que puede usar para establecer las propiedades del objeto de efecto recién creado. Use los métodos de interfaz para establecer las propiedades según sea necesario para generar el efecto visual que desee.

La mayoría de las propiedades de un objeto de efecto se pueden animar. Para animar una propiedad determinada, cree un objeto de animación y aplíctelo a la propiedad que desea animar; De lo contrario, establezca la propiedad en un valor estático que produzca el efecto que desee. Para obtener más información sobre cómo animar propiedades, vea [Animation](animation.md).

Para aplicar un objeto de efecto al objeto visual, llame al [**método IDCompositionVisual::SetEffect.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect) Cuando se aplica un efecto a un objeto visual, el efecto se aplica a todo el subárbol visual basado en ese objeto visual. Por ejemplo, si establece la opacidad de un objeto visual en un 50 por ciento, la opacidad de todos los objetos visuales secundarios del subárbol visual se reducirá en un 50 por ciento. Puede aplicar el mismo objeto de efecto a uno o varios objetos visuales. Si modifica las propiedades de un objeto de efecto después de aplicarlo a los objetos visuales, todos los objetos visuales se vuelve a componer para reflejar el cambio.

Mediante el uso de un objeto de grupo de efectos, puede aplicar simultáneamente varios efectos a un objeto visual. En primer lugar, llame a [**IDCompositionDevice::CreateEffectGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createeffectgroup) para crear el objeto de grupo de efectos y, a continuación, agregue efectos al grupo mediante la interfaz [**IDCompositionEffectGroup del**](/windows/win32/api/dcomp/nn-dcomp-idcompositioneffectgroup) objeto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 