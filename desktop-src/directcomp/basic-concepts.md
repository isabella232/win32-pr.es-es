---
title: Conceptos básicos (DirectComposition)
description: En este tema se proporciona información general sobre los conceptos básicos de Microsoft DirectComposition.
ms.assetid: F442BDCA-C913-4438-BFFA-D3F28B68EE85
keywords:
- Conceptos de DirectComposition
- Conceptos básicos de DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0550dc12cb0dcc5262701658d8e3883ee1ce8d82
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104570347"
---
# <a name="basic-concepts"></a>Conceptos básicos

> [!NOTE]
> En el caso de las aplicaciones de Windows 10, se recomienda usar las API de Windows. UI. Composition en lugar de DirectComposition. Para obtener más información, consulte [modernice su aplicación de escritorio con el nivel de objetos visuales](/windows/uwp/composition/visual-layer-in-desktop-apps).

En este tema se proporciona información general sobre los conceptos básicos de Microsoft DirectComposition. Contiene las secciones siguientes:

-   [Composición](#composition-target-window)
-   [Objetos visuales](#visuals)
    -   [Árbol visual](#visual-tree)
    -   [Propiedades de un objeto visual](#properties-of-a-visual-object)
-   [Objeto de dispositivo](#device-object)
-   [Ventana de destino de composición](#composition-target-window)
-   [Composición transaccional](#transactional-composition)
    -   [Procesamiento por lotes](#batching)
    -   [Sincronización](#synchronization)
    -   [Árboles visuales de dispositivos cruzados](#cross-device-visual-trees)
-   [Temas relacionados](#related-topics)

## <a name="composition"></a>Composición

DirectComposition define una *composición* como una colección de mapas de bits que se combinan y manipulan aplicando varias transformaciones, efectos y animaciones para generar un resultado visual en una interfaz de usuario de la aplicación. DirectComposition funciona solo con contenido de mapa de bits; no admite vectores o texto. DirectComposition no proporciona contenido de mapa de bits. En su lugar, proporciona interfaces en las que los usuarios pueden dibujar con D2D, DXGI o cargar su propio contenido de textura.

Una aplicación DirectComposition crea dos conjuntos de objetos para crear una escena: mapas de bits que se componen juntos y objetos visuales que definen las relaciones espaciales entre los mapas de bits. Para obtener más información sobre los objetos de mapa de bits admitidos por DirectComposition, vea [objetos Bitmap](bitmap-surfaces.md).

## <a name="visuals"></a>Objetos visuales

Los objetos *visuales* (u *objetos visuales*) son los elementos fundamentales de DirectComposition. Son los bloques de creación básicos que se usan para crear composiciones y animaciones en la interfaz de usuario de la aplicación.

En términos de programación, un objeto visual es un objeto que tiene un conjunto de propiedades y expone una interfaz que se utiliza para establecer el valor de las propiedades. La propiedad de contenido de un visual asocia un mapa de bits determinado al visual, mientras que otras propiedades controlan el modo en que DirectComposition coloca y manipula el visual tal como se representa en la pantalla.

Para obtener más información, vea [propiedades de un visual](#properties-of-a-visual-object).

### <a name="visual-tree"></a>Árbol visual

DirectComposition crea una composición a partir de una colección jerárquica de objetos visuales denominada *árbol visual*. El objeto visual en la raíz de un árbol se denomina *objeto visual raíz* y puede tener uno o más *objetos visuales secundarios* asociados. Un elemento visual secundario puede tener uno o más objetos visuales secundarios propios. Cualquier objeto visual con objetos visuales secundarios asociados se denomina objeto *visual primario* y todos los objetos visuales secundarios que comparten el mismo elemento primario se denominan *objetos visuales relacionados*. Un elemento visual determinado junto con todos sus objetos visuales secundarios y descendientes se denomina *subárbol visual*.

La ubicación de un objeto visual en el árbol ayuda a determinar la posición de la pantalla y el orden z en relación con los demás objetos visuales de la composición. El visual raíz se coloca en relación con la esquina superior izquierda del área cliente de la ventana de destino donde se representa la composición. Todos los objetos visuales secundarios se colocan en relación con la esquina superior izquierda de su objeto visual primario (o el objeto visual especificado por la propiedad TransformParent) y siempre aparecen delante de su elemento primario en el orden z.

En la ilustración siguiente se muestra una composición de objetos visuales y la estructura del árbol visual que se usa para generar la composición. Visual 1 es el objeto visual raíz y también es el elemento primario de los objetos visuales secundarios 2 y 3, que son objetos visuales relacionados. Visual 3 tiene dos objetos visuales secundarios propios: objetos visuales 4 y 5. Juntos, los objetos visuales 3 a 5 componen un subárbol visual.

![composición de objetos visuales y el árbol visual correspondiente](images/visuals-and-corresponding-tree.png)

Un objeto visual primario mantiene una lista ordenada de sus objetos visuales secundarios. Cuando los objetos visuales del mismo nivel se colocan de forma que se superponen entre sí, DirectComposition establece el orden z de los elementos del mismo nivel en función del orden en que aparecen en la lista de elementos secundarios del objeto visual primario. Un elemento del mismo nivel que aparece más adelante en la lista se coloca delante de todos los elementos del mismo nivel que aparecen anteriormente en la lista. En la ilustración siguiente se muestra el orden z de los objetos visuales secundarios superpuestos.

![el orden z de los objetos visuales secundarios superpuestos](images/overlapping-child-visuals.png)

### <a name="properties-of-a-visual-object"></a>Propiedades de un objeto visual

Un objeto visual expone un conjunto de propiedades que le permiten establecer el contenido del mapa de bits para el objeto visual y controlar el modo en que DirectComposition coloca y manipula el contenido visual. En las secciones siguientes se describe cada propiedad en detalle.

-   [Propiedad de contenido](#content-property)
-   [Propiedad clip](#clip-property)
-   [Propiedad BorderMode](#bordermode-property)
-   [Propiedad BitmapInterpolationMode](#bitmapinterpolationmode-property)
-   [Propiedad CompositeMode](#compositemode-property)
-   [Propiedades OffsetX y OffsetY](#offsetx-and-offsety-properties)
-   [Propiedad Effect](#effect-property)
-   [Transform (propiedad)](#transform-property)
-   [Propiedad TransformParent](#transformparent-property)

### <a name="content-property"></a>Propiedad de contenido

La propiedad de contenido de un objeto visual especifica el contenido del mapa de bits que está asociado con el objeto visual. Este es el mapa de bits que DirectComposition usa al incluir el visual en una composición.

Establezca la propiedad de contenido de un visual llamando al método [**IDCompositionVisual:: SetContent**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent) .

Para obtener más información sobre los tipos de contenido de mapa de bits admitidos por DirectComposition, vea [objetos Bitmap](bitmap-surfaces.md).

### <a name="clip-property"></a>Propiedad clip

La propiedad clip de un visual especifica un área rectangular denominada *región de recorte* (o *rectángulo* de recorte). Cuando se representa un visual, solo se muestra la parte del objetos visuales que se encuentra dentro de la región de recorte, mientras que el contenido que se extiende fuera de la región de recorte se recorta (es decir, no se muestra). DirectComposition admite regiones de recorte con esquinas redondeadas o cuadradas.

Establezca la propiedad clip de un visual llamando al método [**IDCompositionVisual:: SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)) .

Para obtener más información, vea [recorte](clipping.md).

### <a name="bordermode-property"></a>Propiedad BorderMode

La propiedad BorderMode especifica cómo se componen los bordes de los mapas de bits y los clips asociados a este objeto visual, o con los objetos visuales del subárbol cuya raíz se encuentra en este objeto visual.

El modo de borde afecta a la forma en que se componen los bordes de un mapa de bits cuando se transforma el mapa de bits de forma que los bordes no estén alineados por ejes con coordenadas de entero. También afecta al modo en que el contenido se recorta en las esquinas de un clip con esquinas redondeadas y en el borde de un clip que se transforma de modo que los bordes no estén alineados por ejes con coordenadas de entero.

Para obtener más información, vea [**IDCompositionVisual:: SetBorderMode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setbordermode).

### <a name="bitmapinterpolationmode-property"></a>Propiedad BitmapInterpolationMode

La propiedad BitmapInterpolationMode indica a DirectComposition cómo crear un mapa de bits cuando se transforma de modo que no hay una correspondencia uno a uno entre los píxeles del mapa de bits y los píxeles de la pantalla.

Establezca la propiedad BitmapInterpolationMode de un visual llamando al método [**IDCompositionVisual:: SetBitmapInterpolationMode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setbitmapinterpolationmode) .

### <a name="compositemode-property"></a>Propiedad CompositeMode

La propiedad CompositeMode indica a DirectComposition cómo combinar el contenido del mapa de bits de un visual con el destino de representación. Para obtener una descripción de los modos compuestos compatibles, vea [**DCOMPOSITION \_ composite \_ mode**](/windows/desktop/api/DcompTypes/ne-dcomptypes-dcomposition_composite_mode).

Establezca la propiedad CompositeMode de un visual llamando al método [**IDCompositionVisual:: SetCompositeMode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcompositemode) .

### <a name="offsetx-and-offsety-properties"></a>Propiedades OffsetX y OffsetY

Las propiedades OffsetX y OffsetY indican a DirectComposition dónde colocar un visual horizontal y verticalmente. Definen la posición fija bidimensional en la que se calculan todas las transformaciones y los efectos del visual.

Para un visual raíz, las propiedades OffsetX y OffsetY definen las coordenadas x e y de un punto en relación con la esquina superior izquierda de la ventana que hospeda el visual. En el caso de un objeto visual secundario, las coordenadas son relativas a la esquina superior izquierda del elemento primario o, si se especifica la [propiedad TransformParent](#transformparent-property) , la esquina superior izquierda del objeto visual especificado. Cuando se representa un visual, se coloca de forma que la esquina superior izquierda del visual coincida con las coordenadas especificadas.

Establezca las propiedades OffsetX y OffsetY de un visual llamando a los métodos [**IDCompositionVisual:: SetOffsetX**](/previous-versions/windows/desktop/legacy/hh449126(v=vs.85)) y [**SetOffsetY**](/previous-versions/windows/desktop/legacy/hh449131(v=vs.85)) .

### <a name="effect-property"></a>Propiedad Effect

La propiedad efecto permite especificar un efecto, o un grupo de efectos, que modificará el modo en que se compone un visual y su subárbol. Por ejemplo, puede especificar los efectos que controlan la opacidad de un control visual, combinar el visual con otro mapa de bits de varias maneras y aplicar transformaciones de perspectiva al visual.

Establezca la propiedad Effect de un visual llamando al método [**IDCompositionVisual:: SetEffect**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect) .

Para obtener más información, consulte [Effects](effects.md) (Efectos).

### <a name="transform-property"></a>Transform (propiedad)

La propiedad transform especifica una transformación bidimensional (2D), o un grupo de transformaciones 2D, para que DirectComposition realice en el visual. Una transformación (o transformación) es una operación que modifica el sistema de coordenadas de un objeto visual con respecto a su elemento primario, o relativo al objeto visual especificado por la [propiedad TransformParent](#transformparent-property). Puede usar transformaciones para modificar la posición, el tamaño o la naturaleza de un objeto visual moviéndolo a otra ubicación (traslación), convirtiéndolo en un tamaño mayor o menor (escalado), convirtiéndolo (rotación), distorsionando su forma (sesgando), etc.

Establezca la propiedad transform de un visual llamando al método [**IDCompositionVisual:: SetTransform**](/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)) .

Para obtener más información, consulte [Transformaciones](transforms.md).

### <a name="transformparent-property"></a>Propiedad TransformParent

El sistema de coordenadas de un visual se modifica mediante las propiedades OffsetX, offsetY y transform. Normalmente, estas propiedades definen el sistema de coordenadas de un objeto visual con respecto a su elemento primario inmediato. Para usar un objeto visual distinto del elemento primario como base para el sistema de coordenadas de un objeto visual secundario, use la propiedad TransformParent para especificar un objeto visual diferente como "primario" para fines de transformación.

Establezca la propiedad TransformParent de un visual llamando al método [**IDCompositionVisual:: SetTransformParent**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransformparent) .

## <a name="device-object"></a>Objeto de dispositivo

Para usar DirectComposition, debe crear y manipular una variedad de objetos del modelo de objetos componentes (COM). El primer objeto que necesita crear es el *objeto de dispositivo* DirectComposition porque sirve como generador para crear todos los demás objetos que se usan en una composición.

Para crear un objeto de dispositivo, llame a la función [**DCompositionCreateDevice**](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice) , que devuelve un puntero de la interfaz [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) . Esta interfaz expone un conjunto de métodos que se usan para crear objetos visuales, objetos de clip, objetos de animación, objetos de transformación, objetos de efecto, etc.

El objeto de dispositivo sirve otro propósito, además de ser un generador para crear otros objetos. Expone un método denominado [**commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) que pasa un árbol visual a DirectComposition para su procesamiento. Para obtener más información, vea [composición transaccional](#transactional-composition).

Recuerde que, aunque se pueden crear varias instancias del objeto de dispositivo en la aplicación, todos los objetos que se usan en una composición determinada deben ser creados por el mismo objeto de dispositivo, con una excepción: puede combinar objetos visuales de objetos de dispositivo diferentes en el mismo árbol visual. Al hacerlo, DirectComposition trata el árbol visual como lo haría normalmente, salvo que los cambios en un objeto visual determinado en el árbol solo surten efecto cuando se llama al método [**commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) en el objeto de dispositivo que creó el objeto visual.

La capacidad de usar objetos visuales de distintos dispositivos en el mismo árbol visual permite que varios subprocesos creen y manipulen un único árbol visual manteniendo dos dispositivos independientes que se pueden usar para confirmar cambios de forma asincrónica. Para obtener más información, vea [árboles visuales de dispositivos cruzados](#cross-device-visual-trees).

## <a name="composition-target-window"></a>Ventana de destino de composición

Un árbol visual debe estar enlazado a una ventana para que cualquiera de los objetos visuales del árbol se pueda mostrar en la pantalla. La ventana, denominada *ventana de destino de composición*, puede ser una ventana de nivel superior o una ventana secundaria. Además, la ventana de destino de composición puede ser una ventana superpuesta. es decir, puede tener el estilo de ventana con [**\_ \_ capas de WS**](/windows/desktop/winmsg/extended-window-styles) .

DirectComposition permite que una aplicación enlace un máximo de dos árboles visuales a cada ventana. Los árboles visuales incluyen uno que se compone de la parte superior de la ventana, pero detrás de todas las ventanas secundarias de la ventana, y otro que se compone en la parte superior de la ventana y en la parte superior de las ventanas secundarias. En otras palabras, cada ventana tiene cuatro capas conceptuales y todas las capas se recortan en el área visible de la ventana de destino. En la ilustración siguiente se muestran los cuatro niveles conceptuales de una ventana.

![las capas conceptuales de una ventana](images/directcomposition-layers.png)

## <a name="transactional-composition"></a>Composición transaccional

DirectComposition usa un modelo transaccional en el que se crea un conjunto de cambios por lotes de un visual y, a continuación, se "confirma" el conjunto en DirectComposition para procesarlo todos a la vez. Puede modificar el mismo objeto visual DirectComposition y confirmar los cambios tantas veces como desee. Cuando el Administrador de ventanas de escritorio (DWM) recoge lotes, recoge todos los lotes pendientes y los aplica al siguiente fotograma en el orden en el que se confirmaron.

Se garantiza que todos los cambios de una sola confirmación se aplicarán a un solo fotograma. Dado que DWM recopila lotes una vez por fotograma, puede modificar cualquier objeto concreto solo una vez por fotograma. Las confirmaciones posteriores que modifican objetos diferentes también se pueden aplicar al marco actual, pero DirectComposition no garantiza que los cambios se realicen en el mismo marco.

Los métodos [**IDCompositionSurface:: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) y [**IDCompositionSurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) permiten sincronizar las actualizaciones de representación con las actualizaciones visuales. Por ejemplo, puede llamar a **IDCompositionSurface:: BeginDraw**, actualizar las propiedades OffsetX y clip de un visual, llamar a [**IDCompositionDevice:: commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit), dibujar contenido con Microsoft DirectX y, a continuación, llamar a **IDCompositionSurface:: EndDraw**. En este caso, Microsoft DirectComposition garantiza que el contenido del mapa de bits y las propiedades visuales se actualicen al mismo tiempo.

### <a name="batching"></a>Procesamiento por lotes

Puede confirmar varios cambios en el mismo visual o en varios cambios en objetos visuales diferentes en el mismo marco. Al realizar varios cambios en el mismo visual dentro del mismo marco, tenga en cuenta los puntos siguientes:

-   Si realiza varios cambios en la misma propiedad de un visual, solo se aplicará el último cambio. Por ejemplo, si establece la opacidad en 0, entonces en 0,5 y, por último, en 1,0, solo se aplicará una opacidad de 1,0 al visual.
-   Si cambia varias propiedades del mismo elemento visual, DirectComposition aplica los cambios primero al elemento visual y, a continuación, a los objetos visuales secundarios. Las propiedades se aplican en el orden siguiente, independientemente del orden en que se especifiquen:

    1.  Offset
    2.  Transformación
    3.  Recortar
    4.  Efecto

    En la ilustración siguiente se muestra el resultado de aplicar las cuatro propiedades a un visual.

    ![resultado de aplicar las cuatro propiedades a un visual](images/order-of-properties.png)

    Recuerde que todos los cambios se aplican al visual de una vez en el contexto del mismo marco. Esto significa que, desde la perspectiva del usuario, los cambios en el visual se producen de forma instantánea.

-   En el caso de la propiedad transform, puede usar [**IDCompositionDevice:: CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) para crear un grupo de transformaciones que se aplicarán a un solo visual a la vez. DirectComposition aplica las transformaciones en el orden especificado.
-   En la propiedad efecto, puede usar [**IDCompositionEffectGroup**](/windows/win32/api/dcomp/nn-dcomp-idcompositioneffectgroup) para aplicar un grupo de efectos. DirectComposition aplica los efectos en el orden que especifique. Además, las transformaciones de perspectiva 3D producen una reducción del árbol visual una vez aplicadas todas las transformaciones 3D del visual actual. Esto ayuda a garantizar que el aspecto visual resultante sea lo más parecido posible a 3D.

### <a name="synchronization"></a>Synchronization

La aplicación puede llamar a DirectComposition desde varios subprocesos al mismo tiempo. Se garantiza el orden de ejecución de las llamadas secuenciales, pero no las llamadas simultáneas. Por ejemplo, si el subproceso A modifica un visual y el subproceso B confirma el lote al mismo tiempo, no se define si ese cambio visual se incluye en el lote confirmado o si inicia un lote nuevo. Por otro lado, si la aplicación usa otros mecanismos de sincronización para asegurarse de que se llama a un método antes que el otro, DirectComposition respeta el orden de llamada y los procesa como si ambas llamadas se emitieron en ese orden desde un único subproceso.

### <a name="cross-device-visual-trees"></a>Árboles visuales de dispositivos cruzados

Los objetos DirectComposition no están enlazados a subprocesos; puede usar varios subprocesos para modificar el mismo conjunto de objetos. Sin embargo, tenga en cuenta los siguientes problemas al compartir el mismo objeto de dispositivo.

-   Ambos subprocesos deben poder llamar a [**IDCompositionDevice:: commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit). Si solo uno de los subprocesos llama a **IDCompositionDevice:: commit**, el otro subproceso no puede confirmar ninguno de sus cambios en DirectComposition.
-   El comportamiento transaccional podría perderse si un subproceso llama a [**IDCompositionDevice:: commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) mientras el otro subproceso sigue realizando cambios que están diseñados para formar parte de la misma transacción.

Si necesita confirmar varias transacciones simultáneas en DirectComposition, debe usar varios objetos de dispositivo, posiblemente de varios subprocesos. En este escenario, los dos objetos de dispositivo comparten el mismo árbol visual y cada objeto de dispositivo confirma sus propias transacciones.

En la ilustración siguiente se muestra un árbol visual compartido por dos objetos de dispositivo. Los objetos visuales 1, 2, 4 y 5 son propiedad de un dispositivo o el otro, pero visual 3 se comparte con ambos dispositivos y, por tanto, se pueden usar para conectar dos subárboles a un único árbol visual de mayor tamaño. Compartir el árbol visual permite manipular los dos dispositivos de dos subprocesos diferentes de forma asincrónica.

![árbol visual compartido por dos dispositivos](images/shared-visual-tree-1.png)

Para ilustrar la utilidad de compartir un árbol visual entre dos dispositivos, considere una arquitectura que habilita la entrada táctil de baja latencia. La arquitectura podría usar dos subprocesos, uno que controla la mayoría de las tareas de la interfaz de usuario y un segundo subproceso dedicado para procesar eventos de entrada táctil. El subproceso Touch actualiza la transformación de un determinado visual basándose en el gesto de entrada del usuario. Mediante la actualización de la transformación, el subproceso de toque puede hacer que todo el subárbol bajo ese objeto visual siga el dedo del usuario, escale o reduzca verticalmente cuando el usuario ejecute un gesto multitáctil, etc. El subproceso de interfaz de usuario conserva la propiedad de la mayor parte del árbol de composición, con el subproceso Touch propietario solo de los elementos visuales que se etiquetan para la respuesta táctil asincrónica. En la ilustración siguiente se muestra una versión simplificada de este tipo de árbol de composición:

![árbol visual compartido entre un subproceso de interfaz de usuario y un subproceso táctil](images/shared-visual-tree-2.png)

Normalmente, el subproceso de la interfaz de usuario solo modifica los objetos visuales que posee exclusivamente y el subproceso Touch modifica únicamente el visual compartido. La única excepción se produce al crear o destruir un subárbol habilitado para Touch.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IDCompositionSurface:: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)
</dt> <dt>

[**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)
</dt> <dt>

[**IDCompositonDevice:: commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)
</dt> <dt>

[Conceptos de DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 