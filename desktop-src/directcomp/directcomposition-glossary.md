---
title: Glosario de DirectComposition
description: En este tema se definen los términos de Microsoft DirectComposition.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3B9932EA-3182-41D0-B64A-7699EC98A714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40d6a6f39de62339bf5de0ea7b4976fa19f60c4bd2ff549a732acee43d546256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985435"
---
# <a name="directcomposition-glossary"></a>Glosario de DirectComposition

> [!NOTE]
> Para las aplicaciones Windows 10, se recomienda usar Windows.UI.Composition API en lugar de DirectComposition. Para obtener más información, [consulte Modernización de la aplicación de escritorio mediante la capa visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

En este tema se definen los términos de Microsoft DirectComposition.

<dl> <dt>

<span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**función animation**
</dt> <dd>

Construcción que especifica cómo cambia el valor de una sola propiedad de objeto durante un período de tiempo.

</dd> <dt>

<span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**objeto animation**
</dt> <dd>

Objeto que representa una función para animar las propiedades de otro objeto.

</dd> <dt>

<span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**segmento de animación**
</dt> <dd>

Definiciones de control de tiempo fundamentales de una función de animación; son los primitivos a partir de los cuales se construyen funciones de animación más complejas y de nivel superior.

</dd> <dt>

<span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**búfer de reserva**
</dt> <dd>

Rectángulo de memoria en el que una aplicación puede escribir directamente. El búfer de reserva nunca se muestra directamente en el monitor.

</dd> <dt>

<span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**Lote**
</dt> <dd>

Un grupo de llamadas al método DirectComposition que se procesan de forma atómica.

</dd> <dt>

<span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**Bits**
</dt> <dd>

Búfer de color, ya sea con o sin un canal alfa, que reside en la memoria del sistema o del vídeo.

</dd> <dt>

<span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**modo de borde**
</dt> <dd>

Propiedad de un objeto visual DirectComposition de Microsoft que afecta a cómo se componen los bordes de un mapa de bits cuando el mapa de bits se transforma de forma que los bordes no están alineados con el eje con coordenadas de enteros. También afecta a cómo se recorta el contenido en las esquinas de un clip que tiene esquinas redondeadas y en el borde de un clip que se transforma de forma que los bordes no están alineados con el eje con coordenadas de enteros.

</dd> <dt>

<span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**clip (objeto)**
</dt> <dd>

Objeto que representa un rectángulo de recorte.

</dd> <dt>

<span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**rectángulo de recorte**
</dt> <dd>

Conjunto de coordenadas que definen el área del contenido de mapa de bits del objeto visual que se dibuja en la pantalla cuando se representa el mapa de bits.

</dd> <dt>

<span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**Capa**
</dt> <dd>

Para evitar temporalmente Administrador de ventanas de escritorio (DWM) dibujar una ventana en la pantalla. Las aplicaciones suelen antear una ventana, mientras que DirectComposition usa el mapa de bits de la ventana en una composición.

</dd> <dt>

<span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**Cometer**
</dt> <dd>

Para enviar un lote de comandos a DirectCompositionDirectComposition para su procesamiento.

</dd> <dt>

<span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**modo compuesto**
</dt> <dd>

Una de las distintas formas de combinar dos mapas de bits (un origen y un destino) para lograr un efecto determinado.

</dd> <dt>

<span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**Composición**
</dt> <dd>

Colección de mapas de bits que se combinan y manipulan mediante la aplicación de diversas transformaciones, efectos y animaciones para generar un resultado visual previsto en una interfaz de usuario de la aplicación.

</dd> <dt>

<span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**ventana de destino de composición**
</dt> <dd>

Ventana a la que se enlaza un árbol visual y en la que se dibuja la composición resultante.

</dd> <dt>

<span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**Efecto**
</dt> <dd>

Operación que modifica cómo se rasterizan los mapas de bits de un árbol visual, normalmente aplicando un sombreador de píxeles.

</dd> <dt>

<span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**grupo de efectos**
</dt> <dd>

Un grupo de efectos de mapa de bits que se aplican juntos para modificar la rasterización del subártil de un objeto visual.

</dd> <dt>

<span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**Marco**
</dt> <dd>

Iteración del motor de composición que genera una rasterización del árbol visual.

</dd> <dt>

<span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**búfer de front**
</dt> <dd>

Rectángulo de memoria que el adaptador de gráficos traduce y muestra en el monitor.

</dd> <dt>

<span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**modo de interpolación**
</dt> <dd>

Propiedad que determina cómo se compone un mapa de bits cuando se transforma de forma que no hay ninguna correspondencia uno a uno entre los píxeles del mapa de bits y los píxeles de la pantalla.

</dd> <dt>

<span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**objeto visual raíz**
</dt> <dd>

Objeto visual del que descienden todos los demás objetos visuales de un árbol visual.

</dd> <dt>

<span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**cadena de intercambio**
</dt> <dd>

Colección de uno o varios búferes de reserva que se pueden presentar en serie al búfer front-in-buffer

</dd> <dt>

<span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**Superficie**
</dt> <dd>

Representación de un área lineal de memoria de presentación que normalmente reside en la memoria de presentación de la tarjeta de presentación, aunque las superficies pueden existir en la memoria del sistema.

</dd> <dt>

<span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**Transformar**
</dt> <dd>

Matriz que representa una transformación de coordenadas en un espacio bidimensional o tridimensional.

</dd> <dt>

<span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**grupo de transformación**
</dt> <dd>

Colección de transformaciones cuyas matrices se multiplican juntas en el orden en que se especifican en la colección antes de que se apliquen a un objeto visual.

</dd> <dt>

<span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**Visual**
</dt> <dd>

Objeto que contiene una referencia opcional a un objeto de mapa de bits y un conjunto de propiedades que determinan dónde y cómo se representa el mapa de bits en la pantalla.

</dd> <dt>

<span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**objeto visual**
</dt> <dd>

Vea [*el objeto visual*](/windows).

</dd> <dt>

<span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**subárbol visual**
</dt> <dd>

Una parte de un árbol visual que consta de un objeto visual determinado y todos sus objetos visuales secundarios y descendientes.

</dd> <dt>

<span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**árbol visual**
</dt> <dd>

Colección jerárquica de objetos visuales que se usan para crear una composición.

</dd> <dt>

<span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**cadena de intercambio sin ventanas**
</dt> <dd>

Cadena de intercambio asociada a un objeto visual DirectComposition en lugar de a una ventana.

</dd> </dl>

 

 