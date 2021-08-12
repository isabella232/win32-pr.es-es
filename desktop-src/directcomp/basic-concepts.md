---
title: Conceptos básicos (DirectComposition)
description: En este tema se proporciona información general sobre los conceptos básicos de Microsoft DirectComposition.
ms.assetid: F442BDCA-C913-4438-BFFA-D3F28B68EE85
keywords:
- Conceptos de DirectComposition
- Conceptos básicos de DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2dadcea55ec18089380d7dbe17d99e5dba92b06dd15774c43cd604f28f991c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282061"
---
# <a name="basic-concepts"></a>Conceptos básicos

> [!NOTE]
> Para las aplicaciones Windows 10, se recomienda usar Windows.UI.Composition API en lugar de DirectComposition. Para obtener más información, [consulte Modernización de la aplicación de escritorio mediante la capa visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

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
    -   [Árboles visuales entre dispositivos](#cross-device-visual-trees)
-   [Temas relacionados](#related-topics)

## <a name="composition"></a>Composición

DirectComposition define  una composición como una colección de mapas de bits que se combinan y manipulan mediante la aplicación de diversas transformaciones, efectos y animaciones para generar un resultado visual en una interfaz de usuario de la aplicación. DirectComposition solo funciona con contenido de mapa de bits; no admite vectores ni texto. DirectComposition no proporciona contenido de mapa de bits. En su lugar, proporciona interfaces en las que los usuarios pueden dibujar con D2D, DXGI o cargar su propio contenido de textura.

Una aplicación DirectComposition crea dos conjuntos de objetos para crear una escena: mapas de bits que se componen juntos y objetos visuales que definen las relaciones espaciales entre los mapas de bits. Para obtener más información sobre los objetos de mapa de bits admitidos por DirectComposition, vea [Objetos de mapa de bits.](bitmap-surfaces.md)

## <a name="visuals"></a>Objetos visuales

*Los objetos visuales* (u *objetos visuales)* son los elementos fundamentales de DirectComposition. Son los bloques de creación básicos que se usan para crear composiciones y animaciones en la interfaz de usuario de la aplicación.

En términos de programación, un objeto visual es un objeto que tiene un conjunto de propiedades y expone una interfaz que se usa para establecer el valor de las propiedades. La propiedad Content de un objeto visual asocia un mapa de bits determinado al objeto visual, mientras que otras propiedades controlan cómo DirectComposition coloca y manipula el objeto visual a medida que se representa en la pantalla.

Para obtener más información, [vea Propiedades de un objeto visual.](#properties-of-a-visual-object)

### <a name="visual-tree"></a>Árbol visual

DirectComposition crea una composición a partir de una colección jerárquica de objetos visuales denominada árbol *visual*. El objeto visual de la raíz de un árbol se denomina objeto *visual raíz* y puede tener uno o varios objetos visuales *secundarios asociados.* Un objeto visual secundario puede tener uno o varios objetos visuales secundarios propios. Cualquier objeto visual que tenga objetos visuales secundarios asociados se denomina objeto *visual* primario y todos los objetos visuales secundarios que comparten el mismo elemento primario se denominan objetos *visuales del mismo nivel.* Un objeto visual determinado junto con todos sus objetos visuales secundarios y descendientes se denomina *subárbol visual*.

La ubicación de un objeto visual en el árbol ayuda a determinar su posición de pantalla y el orden z con respecto a los demás objetos visuales de la composición. El objeto visual raíz se coloca en relación con la esquina superior izquierda del área cliente de la ventana de destino donde se representa la composición. Todos los objetos visuales secundarios se sitúan en relación con la esquina superior izquierda de su objeto visual primario (o el objeto visual especificado por la propiedad TransformParent) y siempre aparecen delante de su elemento primario en el orden z.

En la ilustración siguiente se muestra una composición de objetos visuales y la estructura del árbol visual utilizado para generar la composición. Visual 1 es el objeto visual raíz y también es el elemento primario de los objetos visuales secundarios 2 y 3, que son objetos visuales relacionados. Visual 3 tiene dos objetos visuales secundarios propios, Los objetos visuales 4 y 5. Juntos, los objetos visuales del 3 al 5 son un subárbol visual.

![una composición de objetos visuales y el árbol visual correspondiente](images/visuals-and-corresponding-tree.png)

Un objeto visual primario mantiene una lista ordenada de sus objetos visuales secundarios. Cuando los objetos visuales del mismo nivel se posicionan de forma que se superponen entre sí, DirectComposition establece el orden z de los elementos del mismo nivel en función del orden en que aparecen en la lista de elementos secundarios del objeto visual primario. Un elemento relacionado que aparece más adelante en la lista se coloca delante de todos los elementos del mismo nivel que aparecen anteriormente en la lista. En la ilustración siguiente se muestra el orden Z de los objetos visuales secundarios superpuestos.

![el orden z de los objetos visuales secundarios superpuestos](images/overlapping-child-visuals.png)

### <a name="properties-of-a-visual-object"></a>Propiedades de un objeto visual

Un objeto visual expone un conjunto de propiedades que permiten establecer el contenido de mapa de bits del objeto visual y controlar cómo DirectComposition coloca y manipula el contenido visual. En las secciones siguientes se describe cada propiedad en detalle.

-   [Propiedad de contenido](#content-property)
-   [Propiedad Clip](#clip-property)
-   [BorderMode, propiedad](#bordermode-property)
-   [BitmapInterpolationMode, propiedad](#bitmapinterpolationmode-property)
-   [CompositeMode, propiedad](#compositemode-property)
-   [Propiedades OffsetX y OffsetY](#offsetx-and-offsety-properties)
-   [Propiedad de efecto](#effect-property)
-   [Transform (propiedad)](#transform-property)
-   [TransformParent, propiedad](#transformparent-property)

### <a name="content-property"></a>Propiedad de contenido

La propiedad Content de un objeto visual especifica el contenido de mapa de bits asociado al objeto visual. Este es el mapa de bits que usa DirectComposition al incluir el objeto visual en una composición.

La propiedad Content de un objeto visual se establece mediante una llamada al [**método IDCompositionVisual::SetContent.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent)

Para obtener más información sobre los tipos de contenido de mapa de bits admitidos por DirectComposition, vea [Objetos de mapa de bits](bitmap-surfaces.md).

### <a name="clip-property"></a>Propiedad Clip

La propiedad Clip de un objeto visual especifica un área rectangular denominada región *de recorte* (o rectángulo *de recorte).* Cuando se representa un objeto visual, solo se muestra la parte del objeto visual que se encuentra dentro de la región de recorte, mientras que cualquier contenido que se extienda fuera de la región de recorte se recorta (es decir, no se muestra). DirectComposition admite regiones de recorte que tienen esquinas redondeadas o cuadradas.

La propiedad Clip de un objeto visual se establece mediante una llamada al [**método IDCompositionVisual::SetClip.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_))

Para obtener más información, vea [Recorte de](clipping.md).

### <a name="bordermode-property"></a>BorderMode, propiedad

La propiedad BorderMode especifica cómo crear los bordes de los mapas de bits y los clips asociados a este objeto visual, o bien con los objetos visuales del subárbol con raíz en este objeto visual.

El modo de borde afecta a cómo se componen los bordes de un mapa de bits cuando el mapa de bits se transforma de forma que los bordes no están alineados con el eje con coordenadas de enteros. También afecta a cómo se recorta el contenido en las esquinas de un clip que tiene esquinas redondeadas y en el borde de un clip que se transforma de forma que los bordes no están alineados con el eje con coordenadas de enteros.

Para obtener más información, [**vea IDCompositionVisual::SetBorderMode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setbordermode).

### <a name="bitmapinterpolationmode-property"></a>BitmapInterpolationMode, propiedad

La propiedad BitmapInterpolationMode indica a DirectComposition cómo crear un mapa de bits cuando se transforma de forma que no haya ninguna correspondencia uno a uno entre los píxeles del mapa de bits y los píxeles de la pantalla.

La propiedad BitmapInterpolationMode de un objeto visual se establece mediante una llamada al método [**IDCompositionVisual::SetBitmapInterpolationMode.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setbitmapinterpolationmode)

### <a name="compositemode-property"></a>CompositeMode, propiedad

La propiedad CompositeMode indica a DirectComposition cómo combinar el contenido de mapa de bits de un objeto visual con el destino de representación. Para obtener una descripción de los modos compuestos admitidos, vea [**DCOMPOSITION \_ COMPOSITE \_ MODE**](/windows/desktop/api/DcompTypes/ne-dcomptypes-dcomposition_composite_mode).

La propiedad CompositeMode de un objeto visual se establece mediante una llamada al [**método IDCompositionVisual::SetCompositeMode.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcompositemode)

### <a name="offsetx-and-offsety-properties"></a>Propiedades OffsetX y OffsetY

Las propiedades OffsetX y OffsetY le dicen a DirectComposition dónde colocar un objeto visual horizontal y verticalmente. Definen la posición fija bidimensional a partir de la cual se calculan todas las transformaciones y efectos del objeto visual.

Para un objeto visual raíz, las propiedades OffsetX y OffsetY definen la coordenada x y la coordenada Y de un punto con respecto a la esquina superior izquierda de la ventana que hospeda el objeto visual. Para un objeto visual secundario, las coordenadas son relativas a la esquina superior izquierda del elemento primario o, si se especifica la propiedad [TransformParent,](#transformparent-property) la esquina superior izquierda del objeto visual especificado. Cuando se representa un objeto visual, se coloca de forma que la esquina superior izquierda del objeto visual coincide con las coordenadas especificadas.

Las propiedades OffsetX y OffsetY de un objeto visual se establecen mediante una llamada a los métodos [**IDCompositionVisual::SetOffsetX**](/previous-versions/windows/desktop/legacy/hh449126(v=vs.85)) [**y SetOffsetY.**](/previous-versions/windows/desktop/legacy/hh449131(v=vs.85))

### <a name="effect-property"></a>Propiedad de efecto

La propiedad Effect permite especificar un efecto, o grupo de efectos, que modificará cómo se compone un objeto visual y su subárbol. Por ejemplo, puede especificar efectos que controlen la opacidad de un objeto visual, combinar el objeto visual con otro mapa de bits de varias maneras y aplicar transformaciones de perspectiva al objeto visual.

La propiedad Effect de un objeto visual se establece mediante una llamada al [**método IDCompositionVisual::SetEffect.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect)

Para obtener más información, consulte [Effects](effects.md) (Efectos).

### <a name="transform-property"></a>Transform (propiedad)

La propiedad Transform especifica una transformación bidimensional (2D), o un grupo de transformaciones 2D, para que DirectComposition se realice en el objeto visual. Una transformación (o transformación) es una operación que modifica el sistema de coordenadas de un objeto visual con respecto a su elemento primario o con respecto al objeto visual especificado por la [propiedad TransformParent](#transformparent-property). Puede usar transformaciones para modificar la posición, el tamaño o la naturaleza de un objeto visual si lo mueve a otra ubicación (traducción), lo hace mayor o menor (escalado), lo convierte (rotación), distorsiona su forma (sesgo), y así sucesivamente.

Establezca la propiedad Transform de un objeto visual llamando al [**método IDCompositionVisual::SetTransform.**](/previous-versions/windows/desktop/legacy/hh449178(v=vs.85))

Para obtener más información, consulte [Transformaciones](transforms.md).

### <a name="transformparent-property"></a>Propiedad TransformParent

Las propiedades OffsetX, OffsetY y Transform modifican el sistema de coordenadas de un objeto visual. Normalmente, estas propiedades definen el sistema de coordenadas de un objeto visual con respecto a su elemento primario inmediato. Para usar algún objeto visual distinto del elemento primario como base para el sistema de coordenadas de un objeto visual secundario, use la propiedad TransformParent para especificar un objeto visual diferente como "primario" con fines de transformación.

Establezca la propiedad TransformParent de un objeto visual llamando al [**método IDCompositionVisual::SetTransformParent.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransformparent)

## <a name="device-object"></a>Objeto de dispositivo

Para usar DirectComposition, debe crear y manipular diversos objetos del Modelo de objetos componentes (COM). El primer objeto que debe crear es  el objeto de dispositivo DirectComposition, ya que sirve como generador para crear todos los demás objetos usados en una composición.

Para crear un objeto de dispositivo, llame a la función [**DCompositionCreateDevice,**](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice) que devuelve un puntero de interfaz [**IDCompositionDevice.**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) Esta interfaz expone un conjunto de métodos que se usan para crear objetos visuales, recortar objetos, objetos de animación, transformar objetos, objetos de efecto, y así sucesivamente.

El objeto de dispositivo sirve para otro propósito además de ser un generador para crear otros objetos. Expone un método denominado [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) que pasa un árbol visual a DirectComposition para su procesamiento. Para obtener más información, vea [Composición transaccional.](#transactional-composition)

Recuerde que, aunque puede crear varias instancias del objeto de dispositivo en la aplicación, todos los objetos que use en una composición determinada deben crearse mediante el mismo objeto de dispositivo, con una excepción: puede combinar objetos visuales de distintos objetos de dispositivo en el mismo árbol visual. Cuando lo hace, DirectComposition trata el árbol visual como lo haría normalmente, salvo que los cambios en un objeto visual determinado del árbol solo tienen efecto cuando se llama al método [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) en el objeto de dispositivo que creó el objeto visual.

La capacidad de usar objetos visuales de distintos dispositivos en el mismo árbol visual permite que varios subprocesos creen y manipulen un único árbol visual mientras se mantienen dos dispositivos independientes que se pueden usar para confirmar los cambios de forma asincrónica. Para obtener más información, vea [Árboles visuales entre dispositivos.](#cross-device-visual-trees)

## <a name="composition-target-window"></a>Ventana de destino de composición

Un árbol visual debe enlazarse a una ventana antes de que cualquiera de los objetos visuales del árbol se pueda mostrar en la pantalla. La ventana, denominada ventana *de destino de composición,* puede ser una ventana de nivel superior o una ventana secundaria. Además, la ventana de destino de composición puede ser una ventana en capas; es decir, puede tener el estilo de [**ventana WS \_ EX \_ LAYERED.**](/windows/desktop/winmsg/extended-window-styles)

DirectComposition permite que una aplicación enlace un máximo de dos árboles visuales a cada ventana. Los árboles visuales incluyen uno compuesto por encima de la propia ventana, pero detrás de todas las ventanas secundarias de la ventana, y otro que se compone sobre la ventana y encima de las ventanas secundarias. En otras palabras, cada ventana tiene cuatro capas conceptuales y todas las capas se recortan a la región visible de la ventana de destino. En la ilustración siguiente se muestran las cuatro capas conceptuales de una ventana.

![las capas conceptuales de una ventana](images/directcomposition-layers.png)

## <a name="transactional-composition"></a>Composición transaccional

DirectComposition usa un modelo transaccional donde se crea un conjunto por lotes de cambios en un objeto visual y, a continuación, se "confirma" el conjunto en DirectComposition para procesar todos a la vez. Puede modificar el mismo objeto visual DirectComposition y confirmar los cambios en cualquier número de veces. Cuando el Administrador de ventanas de escritorio (DWM) recoge lotes, recoge todos los lotes pendientes y los aplica al siguiente fotograma en el orden en que se han confirmado.

Se garantiza que todos los cambios dentro de una sola confirmación se aplicarán a un único fotograma. Dado que DWM recopila lotes una vez por fotograma, puede modificar cualquier objeto determinado solo una vez por fotograma. Las confirmaciones posteriores que modifican objetos diferentes también se pueden aplicar al marco actual, pero DirectComposition no garantiza que los cambios se produzcan en el mismo marco.

Los [**métodos IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) [**e IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) permiten sincronizar la representación de actualizaciones con actualizaciones visuales. Por ejemplo, puede llamar a **IDCompositionSurface::BeginDraw**, actualizar las propiedades OffsetX y Clip de un objeto visual, llamar a [**IDCompositionDevice::Commit,**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)dibujar contenido con Microsoft DirectX y, a continuación, llamar a **IDCompositionSurface::EndDraw**. En este caso, Microsoft DirectComposition garantiza que el contenido del mapa de bits y las propiedades visuales se actualizan al mismo tiempo.

### <a name="batching"></a>Procesamiento por lotes

Puede confirmar varios cambios en el mismo objeto visual o varios cambios en distintos objetos visuales, dentro del mismo marco. Al realizar varios cambios en el mismo objeto visual dentro del mismo marco, tenga en cuenta los siguientes puntos:

-   Si realiza varios cambios en la misma propiedad de un objeto visual, solo se aplica el último cambio. Por ejemplo, si establece la opacidad en 0, en 0,5 y, por último, en 1,0, solo se aplica una opacidad de 1,0 al objeto visual.
-   Si cambia varias propiedades del mismo objeto visual, DirectComposition aplica primero los cambios al objeto visual y luego a los objetos visuales secundarios. Las propiedades se aplican en el orden siguiente, independientemente del orden en el que las especifique:

    1.  Offset
    2.  Transformación
    3.  Recortar
    4.  Efecto

    En la ilustración siguiente se muestra el resultado de aplicar las cuatro propiedades a un objeto visual.

    ![resultado de aplicar las cuatro propiedades a un objeto visual](images/order-of-properties.png)

    Recuerde que todos los cambios se aplican al objeto visual a la vez dentro del contexto del mismo marco. Esto significa que, desde la perspectiva del usuario, los cambios en el objeto visual se producen instantáneamente.

-   Para la propiedad Transform, puede usar [**IDCompositionDevice::CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) para crear un grupo de transformaciones que se aplicarán a un objeto visual a la vez. DirectComposition aplica las transformaciones en el orden especificado.
-   Para la propiedad Effect, puede usar [**IDCompositionEffectGroup**](/windows/win32/api/dcomp/nn-dcomp-idcompositioneffectgroup) para aplicar un grupo de efectos. DirectComposition aplica los efectos en el orden especificado. Además, las transformaciones de perspectiva 3D tienen como resultado la aplanación del árbol visual después de aplicar todas las transformaciones 3D del objeto visual actual. Esto ayuda a garantizar que el objeto visual resultante sea lo más cercano posible a 3D.

### <a name="synchronization"></a>Sincronización

La aplicación puede llamar a DirectComposition desde varios subprocesos al mismo tiempo. Se garantiza el orden de ejecución para las llamadas secuenciales, pero no para las llamadas simultáneas. Por ejemplo, si el subproceso A modifica un objeto visual y el subproceso B confirma el lote al mismo tiempo, no se define si ese cambio visual se incluye en el lote confirmado o si inicia un nuevo lote. Por otro lado, si la aplicación usa otros mecanismos de sincronización para asegurarse de que se llama a un método antes que el otro, DirectComposition respeta el orden de llamada y los procesa como si ambas llamadas se hubieran emitido en ese orden desde un único subproceso.

### <a name="cross-device-visual-trees"></a>Árboles visuales entre dispositivos

Los objetos DirectComposition no están enlazados a subprocesos; puede usar varios subprocesos para modificar el mismo conjunto de objetos. Sin embargo, tenga en cuenta los siguientes problemas al compartir el mismo objeto de dispositivo.

-   Ambos subprocesos deben poder llamar a [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit). Si solo uno de los subprocesos llama a **IDCompositionDevice::Commit**, el otro subproceso no puede confirmar ninguno de sus cambios en DirectComposition.
-   El comportamiento transaccional podría perderse si un subproceso llama a [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) mientras el otro subproceso sigue realizando cambios que están pensados para formar parte de la misma transacción.

Si necesita confirmar varias transacciones simultáneas en DirectComposition, debe usar varios objetos de dispositivo, posiblemente desde varios subprocesos. En este escenario, ambos objetos de dispositivo comparten el mismo árbol visual y cada objeto de dispositivo confirma sus propias transacciones.

En la ilustración siguiente se muestra un árbol visual compartido por dos objetos de dispositivo. Los objetos visuales 1, 2, 4 y 5 pertenecen a un dispositivo u otro, pero ambos dispositivos comparten el objeto visual 3 y, por tanto, se pueden usar para conectar dos subáritos en un único árbol visual más grande. Compartir el árbol visual permite manipular los dos dispositivos de dos subprocesos diferentes de forma asincrónica.

![un árbol visual compartido por dos dispositivos](images/shared-visual-tree-1.png)

Para ilustrar la utilidad de compartir un árbol visual entre dos dispositivos, considere una arquitectura que permita la entrada táctil de baja latencia. La arquitectura podría usar dos subprocesos, uno que controla la mayoría de las tareas de la interfaz de usuario y un segundo subproceso dedicado al procesamiento de eventos de entrada táctil. El subproceso táctil actualiza la transformación de un objeto visual determinado en función del gesto de entrada del usuario. Al actualizar la transformación, el subproceso táctil puede hacer que todo el subárbol bajo ese objeto visual siga el dedo del usuario, escale vertical o verticalmente a medida que el usuario ejecuta un gesto multi táctil, y así sucesivamente. El subproceso de interfaz de usuario conserva la propiedad de la mayor parte del árbol de composición, con el subproceso táctil que posee solo los pocos objetos visuales etiquetados para la respuesta táctil asincrónica. En la ilustración siguiente se muestra una versión simplificada de este tipo de árbol de composición:

![un árbol visual compartido entre un subproceso de interfaz de usuario y un subproceso táctil](images/shared-visual-tree-2.png)

Normalmente, el subproceso de interfaz de usuario solo modifica los objetos visuales que posee exclusivamente y el subproceso táctil solo modifica el objeto visual compartido. La única excepción se produce al crear o destruir un subárbol táctil.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)
</dt> <dt>

[**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)
</dt> <dt>

[**IDCompositonDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)
</dt> <dt>

[Conceptos de DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 