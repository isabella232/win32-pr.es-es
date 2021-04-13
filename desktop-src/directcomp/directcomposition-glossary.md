---
title: Glosario DirectComposition
description: En este tema se definen los términos de Microsoft DirectComposition.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3B9932EA-3182-41D0-B64A-7699EC98A714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c72186f65f64e1187069963f0aae36de2835fd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359117"
---
# <a name="directcomposition-glossary"></a>Glosario DirectComposition

> [!NOTE]
> En el caso de las aplicaciones de Windows 10, se recomienda usar las API de Windows. UI. Composition en lugar de DirectComposition. Para obtener más información, consulte [modernice su aplicación de escritorio con el nivel de objetos visuales](/windows/uwp/composition/visual-layer-in-desktop-apps).

En este tema se definen los términos de Microsoft DirectComposition.

<dl> <dt>

<span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**función Animation**
</dt> <dd>

Una construcción que especifica cómo cambia el valor de una propiedad de objeto única en un período de tiempo.

</dd> <dt>

<span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**objeto Animation**
</dt> <dd>

Objeto que representa una función para animar las propiedades de otro objeto.

</dd> <dt>

<span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**segmento de animación**
</dt> <dd>

Definiciones de tiempo fundamentales de una función de animación; son los primitivos de los que se compilan funciones de animación más complejas y de nivel superior.

</dd> <dt>

<span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**búfer de reserva**
</dt> <dd>

Un rectángulo de memoria en el que puede escribir una aplicación directamente. El búfer de reserva nunca se muestra directamente en el monitor.

</dd> <dt>

<span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**procesamiento**
</dt> <dd>

Grupo de llamadas al método DirectComposition que se procesan de forma atómica.

</dd> <dt>

<span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**myBitmap**
</dt> <dd>

Un búfer de color, ya sea con o sin canal alfa, que reside en la memoria del sistema o de vídeo.

</dd> <dt>

<span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**modo de borde**
</dt> <dd>

Propiedad de un visual DirectComposition de Microsoft que afecta al modo en que se componen los bordes de un mapa de bits cuando el mapa de bits se transforma de modo que los bordes no estén alineados por ejes con coordenadas de entero. También afecta al modo en que el contenido se recorta en las esquinas de un clip con esquinas redondeadas y en el borde de un clip que se transforma de modo que los bordes no estén alineados por ejes con coordenadas de entero.

</dd> <dt>

<span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**clip (objeto)**
</dt> <dd>

Objeto que representa un rectángulo de recorte.

</dd> <dt>

<span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**rectángulo de recorte**
</dt> <dd>

Conjunto de coordenadas que definen el área del contenido del mapa de bits de visual que se dibuja en la pantalla cuando se representa el mapa de bits.

</dd> <dt>

<span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**posibilidad**
</dt> <dd>

Para impedir temporalmente que Administrador de ventanas de escritorio (DWM) dibuje una ventana en la pantalla. Las aplicaciones normalmente ocultan una ventana mientras que DirectComposition usa el mapa de bits de la ventana en una composición.

</dd> <dt>

<span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**promete**
</dt> <dd>

Para enviar un lote de comandos a DirectCompositionDirectComposition para su procesamiento.

</dd> <dt>

<span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**modo compuesto**
</dt> <dd>

Una de las distintas formas de mezclar dos mapas de bits (un origen y un destino) para lograr un efecto determinado.

</dd> <dt>

<span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**Boletin**
</dt> <dd>

Colección de mapas de bits que se combinan y se manipulan aplicando varias transformaciones, efectos y animaciones para generar un resultado visual deseado en una interfaz de usuario de la aplicación.

</dd> <dt>

<span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**ventana de destino de composición**
</dt> <dd>

Ventana a la que está enlazado un árbol visual y en la que se dibuja la composición resultante.

</dd> <dt>

<span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**realizado**
</dt> <dd>

Operación que modifica cómo se rasterizan los mapas de bits de un árbol visual, normalmente aplicando un sombreador de píxeles.

</dd> <dt>

<span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**Grupo de efectos**
</dt> <dd>

Grupo de efectos de imagen que se aplican conjuntamente para modificar la rasterización del subárbol de un objeto visual.

</dd> <dt>

<span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**grama**
</dt> <dd>

Iteración del motor de composición que genera una rasterización del árbol visual.

</dd> <dt>

<span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**búfer frontal**
</dt> <dd>

Un rectángulo de memoria que el adaptador de gráficos traduce y que se muestra en el monitor.

</dd> <dt>

<span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**modo de interpolación**
</dt> <dd>

Propiedad que determina cómo se crea un mapa de bits cuando se transforma de modo que no hay una correspondencia uno a uno entre los píxeles del mapa de bits y los píxeles de la pantalla.

</dd> <dt>

<span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**raíz visual**
</dt> <dd>

El visual del que todos los demás objetos visuales de un árbol visual son descendentes.

</dd> <dt>

<span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**cadena de intercambio**
</dt> <dd>

Colección de uno o más búferes de reserva que se pueden presentar en serie al búfer frontal.

</dd> <dt>

<span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**Calcomanía**
</dt> <dd>

Representación de un área lineal de memoria de presentación que normalmente reside en la memoria de visualización de la tarjeta de presentación, aunque pueden existir superficies en la memoria del sistema.

</dd> <dt>

<span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**transformación**
</dt> <dd>

Matriz que representa una transformación de coordenadas en un espacio bidimensional o tridimensional.

</dd> <dt>

<span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**transformar grupo**
</dt> <dd>

Colección de transformaciones cuyas matrices se multiplican juntas en el orden en que se especifican en la colección antes de que se apliquen a un objeto visual.

</dd> <dt>

<span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**Visual**
</dt> <dd>

Objeto que contiene una referencia opcional a un objeto de mapa de bits y un conjunto de propiedades que determinan dónde y cómo se representa el mapa de bits en la pantalla.

</dd> <dt>

<span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**objeto visual**
</dt> <dd>

Vea [*Visual*](/windows).

</dd> <dt>

<span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**subárbol visual**
</dt> <dd>

Una parte de un árbol visual que se compone de un elemento visual determinado y de todos sus objetos visuales secundarios y descendientes.

</dd> <dt>

<span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**árbol visual**
</dt> <dd>

Colección jerárquica de objetos visuales que se usan para crear una composición.

</dd> <dt>

<span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**cadena de intercambio sin ventanas**
</dt> <dd>

Cadena de intercambio que está asociada a un objeto visual DirectComposition en lugar de a una ventana.

</dd> </dl>

 

 