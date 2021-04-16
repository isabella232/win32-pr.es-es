---
title: Animaciones y transiciones
description: El uso estratégico de animaciones y transiciones puede hacer que el programa sea más fácil de entender, sentirse más suave, natural y de mayor calidad, y ser más atractivo.
ms.assetid: 9e0e9604-f051-47e4-bcd0-59fbfd38b9c1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6d57c696bd78df9c9505bb85453456f10631a00d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104556395"
---
# <a name="animations-and-transitions"></a>Animaciones y transiciones

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

El uso estratégico de animaciones y transiciones puede hacer que el programa sea más fácil de entender, sentirse más suave, natural y de mayor calidad, y ser más atractivo. Pero el uso ingratuito de animaciones y transiciones puede hacer que el programa se distraiga e incluso molesto.

Las animaciones dan la apariencia de movimiento o cambio a lo largo del tiempo. Use la animación para proporcionar comentarios, obtener una vista previa del efecto de una acción, Mostrar la relación entre objetos, atraer la atención al cambio o explicar una tarea visualmente.

![figura del teclado numérico con una tecla resaltada ](images/vis-animations-image1.png)

Microsoft Windows usa una animación Flash de fondo para proporcionar comentarios sobre el objeto en el que se hizo clic.

Las transiciones son animaciones que se usan para mantener a los usuarios orientados durante los cambios de estado de la interfaz de usuario (IU) y las manipulaciones de objetos, y hacer que estos cambios sean suaves en lugar de discordante. Una buena transición es natural y, a menudo, proporciona la ilusión de que los usuarios interactúan con objetos del mundo real.

![Captura de pantalla que muestra tres tamaños de gadgets meteorológicos.](images/vis-animations-image2.png)

Los gadgets de escritorio de Windows usan transiciones suaves entre sus Estados concisos y de detalles.

Por lo general, las mejores animaciones y transiciones se usan para comunicarse con los usuarios de forma no verbal y para que los cambios de estado sean más naturales y menos perceptibles. Por el contrario, la menor efectividad es innecesaria, ya que no comunican nada o dibujan atención innecesaria. Las animaciones se usan mejor como forma secundaria de comunicación. Deben comunicar información útil pero no crítica y, para ser accesibles, los usuarios deben poder determinar la información equivalente a través de otros medios.

**Nota:** Las instrucciones relacionadas con la [Personalización de marca de software](exper-branding.md), el [sonido](vis-sound.md)y la [accesibilidad](inter-accessibility.md) se presentan en artículos independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

Para decidir, tenga en cuenta las siguientes preguntas.

### <a name="animations"></a>Animaciones

¿Se aplican las siguientes condiciones?

-   La animación comunica visualmente algo útil, como proporcionar comentarios, mostrar relaciones, causas y efectos, o atraer la atención al cambio importante.
-   Ver la animación no es esencial. La información equivalente se puede obtener de otra manera. Es posible que los usuarios no se beneficien de la animación si:
    -   Han desactivado las animaciones.
    -   Su atención está en otra parte.
    -   Están dispares visualmente.
    -   La animación está oculta en otra ventana.
    -   La animación no se reproduce debido a un rendimiento insuficiente del sistema.
-   La animación no afecta a la productividad del usuario. Tener instaladas localmente una de las siguientes:
    -   Se produce rápidamente (200 milisegundos o menos).
    -   No interfiere con la interacción o se puede interrumpir.
    -   El usuario tiene que esperar de todos modos.
-   La animación no afecta al flujo del usuario.
    -   Es el centro de atención del usuario, o bien llama a algo fuera del centro de atención que es importante o útil para completar una tarea.
    -   Es fácil de omitir, no distraerse ni molestarse.
    -   No se convierte en una tarea ardua. Los usuarios seguirán siendo adecuados y divertidos incluso después de la visualización repetida.

Si es así, considere la posibilidad de usar una animación.

### <a name="transitions"></a>Transiciones

¿Cambia el estado de un objeto o una escena y realiza todas las condiciones anteriores para usar animaciones, así como cualquiera de las condiciones siguientes:

-   El cambio de estado está desorientando conceptualmente, confuso o difícil de entender.
-   El cambio de estado es visualmente discordante, no tiene continuidad ni suavidad, o Flashs; o parece no natural, no refinado o de mala calidad, especialmente si se trata de un área de pantalla grande.
-   El uso de una transición haría que el cambio de estado aparezca más rápido.
-   El cambio de estado merece la atención especial del usuario.

Si es así, considere la posibilidad de usar una transición.

## <a name="design-concepts"></a>Conceptos de diseño

Las animaciones y las transiciones son una manera eficaz de comunicar la información visualmente que, de lo contrario, requeriría que el texto se explicara o no se pudiera a los usuarios.

**Incorrecto:**

![captura de pantalla del cuadro de diálogo con mensaje ](images/vis-animations-image3.png)

**Correcto:**

![figura de animación que se comunica visualmente ](images/vis-animations-image4.png)

El uso de una animación comunica la misma información, pero de forma natural y discreta. ¿En qué casos se verán mil veces?

**Las animaciones y las transiciones no tienen que solicitar atención para que se realicen correctamente.** De hecho, a menudo se usan para evitar tener que prestar atención a los mecanismos de programación que los usuarios no necesitan conocer. Muchas animaciones correctas son tan naturales que los usuarios no son conscientes de ellas. en su lugar, los usuarios solo observarán su ausencia. La frecuencia de la repetición aumenta la necesidad de los sutilezas, por lo que debe ahorrar efectos que requieran atención para eventos poco frecuentes que merecen la atención.

![captura de pantalla de todos los programas cambiar a flecha atrás ](images/vis-animations-image5.png)

Una transición del menú Inicio que evita la atención.

Además de facilitar la comprensión del programa, así como **animaciones y transiciones más suaves y bien diseñadas, es una excelente manera de agregar personalidad, carácter y estilo al programa.** Pueden hacer que la experiencia del usuario sea más envolvente y atractiva proporcionándole un aspecto natural y real.

![Ilustración que muestra cómo el desplazamiento afecta al color del botón ](images/vis-animations-image6.png)

Windows 7 resalta los botones de la barra de tareas al mantener el mouse según la posición actual del mouse y el color del icono del programa. Este enfoque es visualmente atractivo, pero sutil, que transmite una personalidad Humble.

**Sin embargo, las animaciones y transiciones son más eficaces cuando sirven para un propósito claro.** Deben usarse para mejorar la facilidad de uso, la suavidad y el flujo, y la percepción de calidad, sin perjudicar significativamente el rendimiento.

Aunque se usan algunos tipos de animaciones para atraer la atención del usuario, asegúrese de que la atención se mantiene bien y merece la interrupción del entrenamiento del usuario. El ojo humano es sensible al movimiento, especialmente al movimiento de periféricos. Puede ser difícil para los usuarios concentrarse cuando hay un botón de la barra de tareas parpadeante o un icono de área de notificación girando. **Evite el uso de animaciones para interrumpir o distraer a los usuarios, o bien atraer la atención a los elementos que no garantizan la atención del usuario.**

**Incorrecto:**

![figura del botón de la barra de tareas resaltado sin motivo ](images/vis-animations-image7.png)

Los programas no deben tener el botón de la barra de tareas, a menos que los usuarios tengan que hacer algo importante inmediatamente. En este caso, lo único que debe hacer el usuario es activar el programa.

**Use animaciones y transiciones porque el programa las necesita, no solo porque puede hacerlo.** Y para la accesibilidad, no use la animación como la única manera de transmitir información esencial. Asegúrese de que los usuarios puedan obtener información equivalente de otra manera.

### <a name="attributes-of-good-animations-and-transitions"></a>Atributos de buenas animaciones y transiciones

Las buenas animaciones y transiciones cocompletan el equilibrio adecuado entre estos atributos:

-   **Son claramente intencionadas.** Hay buenas animaciones porque deben ser, ya sea para comunicar la información, hacer que la interacción sea real o atraer la atención a algo que sea importante. Y las animaciones de propósito son precisas. Si una animación muestra que se está llevando a cabo una tarea, es porque la tarea está en realidad.

**Incorrecto:**

![captura de pantalla del icono de la batería y etiqueta de carga completa ](images/vis-animations-image8.png)

En este ejemplo, la animación muestra que se está cobrando una batería totalmente cargada.

-   **Fíjese en Smooth y Continuous.** Las buenas animaciones quitan sin problemas las costuras entre los cambios de estado de la escena o del elemento al mostrar las relaciones y proporcionar una idea del lugar y el contexto. La continuidad ayuda a los usuarios a comprender cómo se encontraban donde se encontraban y cómo volver a su procedencia.

![captura de pantalla de tres vistas previas de ventanas de la barra de tareas ](images/vis-animations-image9.png)

La vista previa de la ventana de la barra de tareas de Windows 7 se transforma para la continuidad a medida que el usuario se mueve de un programa a otro.

-   **Son realistas.** Las buenas animaciones simulan las propiedades físicas y el comportamiento del mundo real de un objeto. Esto ayuda a los usuarios a predecir y comprender los resultados de sus interacciones. No tiene que modelar el mundo real exactamente, pero si usa animaciones realistas, debe mantener la coherencia con el mundo real. Los resultados nunca deben sorprender ni confundir a los usuarios, especialmente con las animaciones que se usan para la manipulación directa.

![figura del botón de la barra de tareas arrastrado a la nueva posición ](images/vis-animations-image10.png)

En este ejemplo, la animación "salir del camino" que usa la barra de tareas de Windows 7 es más realista que un punto de inserción estático.

-   **Son auténticos.** Incluso los objetos que no se encuentran en el mundo real pueden parecer naturales basándose en el comportamiento real de un objeto diferente, pero relacionado. Esta metáfora solo funciona si la relación comunica claramente el propósito y el comportamiento planteados.

![captura de pantalla de efecto elevado detrás de la ventana movida ](images/vis-animations-image11.png)

En este ejemplo, la animación de la ventana "Squeegee" que usa Windows 7 es auténtica porque es coherente con el comportamiento de las ventanas de cristal en el mundo real.

-   **Use la asignación natural.** Las asignaciones naturales son físicas o culturales. Una asignación natural basada en la cultura, por ejemplo, puede empezar por el hecho de que en las culturas occidentales, las personas lean de izquierda a derecha. Por lo tanto, para expresar una secuencia temporal de objetos, el objeto central es actual, los objetos a la izquierda son desde el pasado y los objetos a la derecha se encuentran en el futuro. Avanzar en el tiempo se indica mediante el movimiento de izquierda a derecha.

![captura de pantalla de la barra de progreso del reproductor de media ](images/vis-animations-image12.png)

En este ejemplo, el control Media Player de Windows tiene una asignación natural porque la reproducción mueve la posición de izquierda a derecha.

-   **Tenga personalidad.** Las animaciones bien elegidas son excelentes maneras de agregar personalidad, carácter y estilo al programa. Pueden hacer que la experiencia del usuario sea más envolvente y atractiva. Aunque el tipo de animación determina lo que se comunica, la manera específica en la que se realiza la animación muestra la personalidad del programa. Las buenas animaciones proyectan la personalidad adecuada para el programa, ya sean graves o divertidos, o en algún punto entre.

![captura de pantalla de la interfaz Zune diseñada creativamente ](images/vis-animations-image13.png)

En este ejemplo, el uso de Zune de texto animado y de la perspectiva dinámica ayuda a dar forma a su personalidad.

-   **Apariencia y sensación de respuesta.** Las buenas animaciones no perjudican la productividad del usuario al bloquear a los usuarios de otras interacciones o obligar a los usuarios a ver. Independientemente de la naturalidad y la interacción de las animaciones del programa, nadie desea esperar exclusivamente. Las animaciones buenas también tienen una gran capacidad de respuesta sin ser Discordante, ya que tienen un inicio rápido con un aterrizaje. Las animaciones con capacidad de respuesta también se benefician de la comunicación rápida de su propósito. Los usuarios no deben tener que ver una animación durante mucho tiempo, solo para averiguar qué está haciendo o Cuándo se ha hecho. En el caso de la manipulación directa, las animaciones con capacidad de respuesta son esenciales para el mantenimiento directo y atractivo del mundo real. Para sentirse directos, los puntos de contacto de un objeto deben permanecer bajo el puntero sin problemas a lo largo de la manipulación. Cualquier retraso, respuesta entrecortada o pérdida de contacto destruye la percepción de la manipulación directa.

![Ilustración de tocar una pantalla táctil ](images/vis-animations-image14.png)

En este ejemplo, la transición de movimiento panorámico táctil parece responder manteniendo el punto de contacto bajo el dedo del usuario a lo largo de la manipulación.

-   **Atraiga el nivel de atención adecuado.** Las animaciones buenas suelen ser sutiles y solo dibujan la atención necesaria para satisfacer su propósito. Como resultado, no distraigan, molestos, demasiado complejos, demasiado largos o repetitivos. No se convierten en una tarea ardua después de que se repitan las visualizaciones.

![captura de pantalla de resaltado de difuminación en nombres de archivo ](images/vis-animations-image15.png)

En este ejemplo, la búsqueda de Windows se centra temporalmente en la coincidencia de palabras de búsqueda y luego se atenúa.

-   **Fíjese en especial únicamente si es originalmente especial.** La frecuencia aumenta la necesidad de los sutilezas, por lo que las interacciones comunes necesitan animaciones sencillas que comuniquen una idea simple de una manera sencilla. Reserve animaciones especiales y complejas para experiencias especiales y poco frecuentes.

![captura de pantalla de cuatro círculos convirtiéndose en el logotipo de Windows ](images/vis-animations-image16.png)

En este ejemplo, Windows usa una animación de obtención de atención en el inicio para que la experiencia sea especial, pero esta animación no sería adecuada en ningún otro lugar.

Sabrá que ha logrado el equilibrio adecuado cuando se elimine la experiencia global si se quitara alguno de estos atributos.

### <a name="creating-an-animation-vocabulary"></a>Crear un vocabulario de animación

Las buenas animaciones son la comunicación visual efectiva y la coherencia es fundamental para su eficacia. Si usa una transición específica, como insertar una escena de la derecha para avanzar a la siguiente escena, debe ser la única transición que se usa para ese fin y esa transición no debe usarse para ningún otro propósito. Asignar significados diferentes a la misma animación perjudica su capacidad de comunicación. Mediante la asignación de animaciones específicas y transiciones a significados específicos, se crea un vocabulario de animación.

Este problema se aplica a las animaciones y transiciones que tienen significado, no a las genéricas a las que no es probable que los usuarios asignen significado o a aquellos cuyo propósito es inadvertible. Por ejemplo, animaciones como atenuaciones y efectos especiales como las dessoluciones no tienen ningún significado determinado, por lo que se pueden usar libremente.

Un buen vocabulario asigna animaciones que modelan el comportamiento físico del mundo real de un objeto. Si necesita asignar una animación a un objeto o una acción que no tenga un homólogo real, elija una animación que muestre cómo el objeto podría comportarse como real.

![captura de pantalla de cómo mantiene el mouse sobre el resplandor del logotipo de Windows ](images/vis-animations-image17.png)

Mientras que el menú Inicio no es un objeto del mundo real, el efecto de mantener el mouse se enciende como un objeto del mundo real, cuando se activa.

Cada animación de un vocabulario debe ser claramente distinta. Las animaciones deberían tener comportamientos similares solo si sus acciones asociadas están relacionadas de forma similar. Por ejemplo, las transiciones de movimiento sugieren navegación, por lo que puede usar transiciones de movimiento de distintas direcciones para indicar diferentes tipos de navegación.

Sabrá que las animaciones y transiciones no se comunican bien cuando los usuarios encuentran los resultados confusos, sorprendentes o inesperados. Por lo general, es mejor lograr un propósito único que con varios fines, no tan bien.

Idealmente, el vocabulario de animación debe ser completo en todas las áreas del programa que los necesiten. Si solo algunas interacciones tienen animaciones naturales, eso hará que se preste atención a las que no lo están.

Para obtener más información sobre el vocabulario de animación de Windows, consulte la sección [patrones de uso](#usage-patterns) de este artículo.

### <a name="designing-the-right-personality"></a>Diseño de la personalidad adecuada

Mientras que el tipo de animación determina lo que se comunica, la manera específica en la que se realiza la animación habla con la personalidad del programa y refuerza su marca.

La personalidad de su programa debe reflejar la naturaleza de sus tareas y la personalidad de sus usuarios, por lo que no es una opción arbitraria. En su lugar, una personalidad bien diseñada debe sentirse auténtica; No intente forzarla nunca. La personalidad debe establecer una conexión emocional con el usuario. Algunos factores a tener en cuenta:

-   **Tareas:** Graves o divertidos; opcional o obligatorio.
-   **Consecuencias:** Grave o secundaria.
-   **Costo:** Gratis o comprado; Si se compra, tiene un precio moderado o es costoso.
-   **Enfoque del usuario:** Grupo relativamente estrecho de usuarios de destino o público general de gran alcance.
-   **Entorno de usuario:** Professional, informal o doméstica.
-   **Edad del usuario:** Más jóvenes o anteriores.
-   **Frecuencia de uso:** Frecuente o poco frecuente.

La combinación de estos factores ayuda a determinar una personalidad adecuada para el programa. Estas son algunas de las combinaciones adecuadas para tipos de programas comunes:

**Aplicaciones de productividad**

Naturalmente, las aplicaciones de productividad deben centrarse en la productividad. Aunque algunas experiencias especiales pueden destacar, la mayoría de las demás animaciones deberían tener estas características:

-   Pequeña
-   Natural, realista
-   Sutil, subdued
-   Rápida y eficaz
-   Relajado

**Utilidades**

Las utilidades suelen usarse brevemente, por lo que su uso de la animación puede ser más agresivo:

-   Realista, ilustrativo, autoexplicativo
-   Caja fuerte
-   Atractivas

**Entretenimiento, juegos**

Dado que el objetivo de estos programas es ponerse en contacto con los usuarios y satisfacerlos, las animaciones y transiciones pueden ser mucho más agresivas al tener estas características:

-   Grande (posiblemente convirtiéndose en una parte integral de la experiencia)
-   Artificial, surreal
-   Impactante, vibrante
-   Emocional, playful, divertidos
-   Condiciona

Realizar una conexión emocional es tan importante para los programas de entretenimiento que es aceptable doblar algunas reglas si esto ayuda a que los usuarios se queden encantados con el programa. Por ejemplo, es aceptable que una animación o transición se una tarea ardua después de la centésima de tiempo si es improbable que la mayoría de los usuarios utilicen el programa con frecuencia.

Por lo general, las animaciones y transiciones pequeñas, naturales, subdued, eficientes y relajadas son la apuesta más segura. Normalmente, las transiciones con estas características toman la ruta más corta de principio a fin, se inician rápidamente, finalizan de forma flexible y no se supertoman. Además, las transiciones bien diseñadas están diseñadas para funcionar bien en todo el intervalo de distancias en el que se usarán.

### <a name="animation-performance"></a>Rendimiento de animación

Al diseñar animaciones, asegúrese de que no afectan a la capacidad de los usuarios para usar el programa de forma eficaz. Por lo general, haga que las animaciones sean lo suficientemente lentas como para satisfacer su finalidad, pero lo suficientemente rápido como para que no interfieran con la capacidad de respuesta, exija demasiado atención o se conviertan en una tarea ardua.

**Incorrecto:**

![Ilustración de la página de derecha a izquierda ](images/vis-animations-image18.png)

Aunque la animación de este cambio de página tiene un atractivo mundo real, reduce la productividad de los usuarios, ya que tarda más en reactivarse las páginas.

Las transiciones breves (de 200 milisegundos o menos) son un caso especial (especialmente cuando suelen funcionar fuera de un retraso) porque los usuarios tendrán constancia de que tienen que esperar una segunda división por ellos. Los usuarios están dispuestos a esperar dichas animaciones si:

-   La espera percibida es muy breve (200 milisegundos o menos).
-   La transición hace que la interacción sea más suave y natural.
-   La transición hace que la interacción tenga mayor capacidad de respuesta.
-   Cualquier retraso ayuda a evitar que el usuario controle la interacción.

![figura de los botones de la barra de tareas arrastrados a la nueva posición ](images/vis-animations-image19.png)

Los usuarios aceptarán un breve retraso en la animación de reordenación del botón de la barra de tareas porque es muy breve y hace que la interacción sea más natural.

Existen tres formas en las que las animaciones pueden afectar negativamente al rendimiento: velocidad, capacidad de respuesta y percepción.

En cuanto a la velocidad, algunas animaciones son chapas visuales de tareas de uso intensivo de la CPU, por lo que lo último que debe hacer es hacer que estas tareas sean más lentas con las animaciones con uso intensivo de la CPU. La mayoría de las animaciones de uso intensivo de la CPU ("pesadas") tienden a:

-   Implica que muchos elementos se mueven de forma independiente.
-   Juegue durante una larga duración o distancia.
-   Implica una gran cantidad de espacio de la pantalla.
-   Son demasiado intensivos.

Animaciones con menos impacto en el rendimiento:

-   Implique un solo objeto.
-   Reproducir durante una breve duración o distancia.
-   Implica una pequeña cantidad de espacio de pantalla.
-   No se usan de forma matemática.

Para garantizar un buen rendimiento, se deben usar animaciones pesadas solo para las tareas que no consuman CPU, mientras que las animaciones ligeras se pueden usar en cualquier lugar.

Para la capacidad de respuesta, la mayoría de las animaciones y transiciones deben diseñarse para que los usuarios puedan interactuar mientras se está ejecutando la animación. A menos que una animación forme parte de un proceso, haga que sea independiente de la interacción primaria del usuario y permita a los usuarios interrumpirla.

Es posible que una animación no afecte negativamente al rendimiento de una tarea en realidad, pero los usuarios pueden tener la percepción de que sí lo hacen. Por ejemplo, no utilice una animación que parezca pesada para una tarea lenta, con un uso intensivo de la CPU, incluso si no perjudica el rendimiento, ya que los usuarios podrían concluir que la animación es el motivo por el que la tarea es lenta. **Si algo tiene un aspecto lento, se verá lento, por lo que es mejor usar animaciones que parezcan simples, ligeras y rápidas.** La utilización de animaciones con una fase de comienzo ajustable para tareas de uso intensivo de la CPU ayuda a.

**Riesgo**

![captura de pantalla del cuadro de diálogo copiar con barra de progreso ](images/vis-animations-image20.png)

Aunque la animación en el cuadro de diálogo de copia de archivos de Windows no daña el rendimiento de la copia de archivos, se corre el riesgo de que los usuarios creen que lo hace.

**También arriesgado:**

![captura de pantalla del progreso mostrado en la barra de direcciones ](images/vis-animations-image21.png)

En este ejemplo, la animación de progreso de búsqueda lenta en la barra de direcciones del explorador de Windows hace que algunas tareas parezcan muy lentas.

Las animaciones y transiciones no tienen ningún valor si su calidad es tan deficiente que hacen que la experiencia sea menos suave y menos atractiva. Para mantener su calidad, las animaciones deben diseñarse para que se reduzcan correctamente siempre que no haya suficientes recursos del sistema disponibles. Las animaciones se pueden degradar teniendo variaciones que requieran menos recursos (por ejemplo, longitudes más cortas o velocidades de fotogramas inferiores) o incluso no se ejecuten en absoluto. Independientemente de los recursos disponibles, asegúrese de que las animaciones tienen una alta calidad y se parecen a las animaciones en lugar de errores de software.

Por último, si los usuarios creen que las animaciones y transiciones del programa distan de su productividad, hay una buena posibilidad de que algunos usuarios quieran desactivarlas. Para admitir esta capacidad, respete la opción para **desactivar todas las animaciones innecesarias** que se encuentran en el centro de accesibilidad de Windows.

### <a name="attracting-the-right-level-of-attention"></a>Atraer el nivel de atención adecuado

Aunque solo algunos tipos de animaciones y transiciones están diseñados específicamente para atraer la atención del usuario, deben diseñarse para atraer el nivel adecuado de atención para cumplir su objetivo. ¿Cuáles son las diferentes formas de atraer la atención y cómo elegir la adecuada?

**Efectos de animación**

Los diferentes efectos de animación atraen diferentes niveles de atención. En la lista siguiente se resumen los métodos más comunes, empezando por la obtención de más atención:

-   **Parpadeo rápido.** Requiere atención inmediata. Puede interrumpir la concentración de los usuarios independientemente de dónde se produzca el parpadeo.
-   **Parpadeo moderado.** Lo mismo, pero requiere menos atención con una frecuencia menor.
-   **Rebote.** Es perceptible en la visión del periférico y es relativamente exigente por naturaleza. Es probable que los usuarios observen, pero pueden seguir concentrados en otro lugar solo si la duración es breve.
-   **Disminuir.** Perceptible en la visión de periféricos, pero no lo exige. Sin embargo, los movimientos complejos o 3D atraen más la atención que los movimientos simples o 2D. Es probable que los usuarios observen, pero pueden seguir concentrados en otros lugares.
-   **Pulsos moderados.** Perceptible, pero sin distraer en la visión de periféricos. Los usuarios pueden seguir concentrados en otros lugares. Puede aumentar el brillo, los colores y los tamaños.
-   **Pulsos o brillo lentos.** Perceptible pero sutil. Atrae más la atención que un efecto estático, pero es posible que los usuarios no observen la animación a menos que ya lo estén buscando.
-   **Aparición.** Incluso menos perceptible. Atrae más la atención que un efecto estático, pero es posible que los usuarios no observen la animación a menos que ya lo estén buscando.
-   **Resaltado estático/Gleam.** Apreciable si los usuarios eligen ver, pero no requieren atención si están en otro lugar.
-   **Ambiente/natural.** No se percibe intencionadamente al tener un aspecto natural y real.

Para determinar el enfoque correcto para su programa o característica, tenga en cuenta cómo se relacionan estos factores con los escenarios de la característica.

Por ejemplo, supongamos que está diseñando un programa de mensajes instantáneos y que alguien ha enviado un mensaje al usuario. Este escenario requiere la atención del usuario, debe ser perceptible en cualquier parte y, por lo general, el usuario querrá responder rápidamente. Este escenario sugiere que una animación moderada intermitente sería una buena elección. Por el contrario, supongamos que desea informar a los usuarios de que se ha completado un trabajo de impresión. Los usuarios deben poder seguir concentrados y trabajar de manera productiva en otro lugar, y es aceptable si los usuarios no lo tienen en cuenta. En este escenario, se sugiere que la velocidad moderada a lenta o el resplandor es una buena elección.

**Duration**

La duración adecuada para obtener una animación depende del escenario y del tipo específico de animación utilizada. Cuanto más atención se requiera un efecto de animación, menor será la duración. Aunque los efectos muy sutiles que demandan poca atención (como la velocidad lenta) se pueden reproducir indefinidamente, los efectos exigentes de la atención solo se deben reproducir entre 1 y 3 segundos. El riesgo es más largo, lo que hace que la animación sea abrumadora y molesta.

![captura de pantalla del botón de la barra de tareas resaltado ](images/vis-animations-image22.png)

En Windows 7, la barra de tareas parpadea para prestar atención a un segundo. Lo más largo sería molesto.

**Caída del efecto**

Debe diseñar animaciones de obtención de atención en función de la suposición de que, si los usuarios no responden de inmediato, se deben a que están ocupados haciendo otra cosa y no desean que se interrumpan. Por lo tanto, el objetivo debe ser atraer la atención sin demandarlo.

Para obtener el equilibrio adecuado entre atraer la atención sin demanda, decaiga la intensidad de un efecto a lo largo del tiempo. Por ejemplo, para atraer la atención, puede hacer que el efecto sea inicialmente fuerte, pero ralentizar el efecto rápidamente. Al hacerlo, la potencia atractiva se determina principalmente por el efecto inicial, pero la impresión global del usuario se determina principalmente por su finalización.

![captura de pantalla que muestra la velocidad de Flash reducida ](images/vis-animations-image23.png)

En Windows 7, el efecto de parpadeo de la barra de tareas disminuye al final.

### <a name="what-about-powerpoint"></a>¿Qué ocurre con PowerPoint?

Las transiciones de Microsoft PowerPoint suelen infringir deliberadamente estas instrucciones porque están diseñadas para atraer la atención a las transiciones de diapositivas y requieren que los usuarios las esperen. Además, no tienen ningún significado determinado, por lo que no comunican nada más allá del hecho de que una diapositiva cambie.

Las transiciones de estilo de PowerPoint, cuando se usan correctamente, tienen estos propósitos:

-   Dividen presentaciones largas en fragmentos más pequeños forzando al presentador a pausarse.
-   Dibujan la atención de la audiencia con respecto a los cambios en la presentación, lo que ayuda a las personas a redirigirse si sus mentes se han preguntado.
-   Proporcionan a la presentación un ritmo para que no sienta más monótono ni abrumador.
-   Su estilo refleja la personalidad del presentador o del material.

Aunque estos son objetivos importantes para una presentación, estas transiciones dibujarían atención innecesaria en la interfaz de usuario de la mayoría de los tipos de programas y se una tarea ardua rápidamente.

**Línea inferior:** No use transiciones de estilo de PowerPoint como modelo para el programa.

**Si solo hace seis cosas...**

1.  Use animaciones y transiciones para que el programa sea más fácil de entender y parezca más suave y más atractivo. Deben tener un propósito claro. No use animaciones solo porque puede o para dibujar atención innecesaria para el programa.
2.  Definir un vocabulario de animación y usarlo de forma coherente en todo el programa. Use el vocabulario de animación de Windows 7 cuando corresponda.
3.  Use las características de las animaciones para dar la personalidad del programa y reforzar su marca.
4.  Haga que la mayoría de las animaciones sean sencillas, breves e sutiles. Recuerde que las animaciones no tienen que solicitar atención para que se realicen correctamente. Si una animación es adecuada y natural, los usuarios solo observarán su ausencia.
5.  Haga que las animaciones sean rápidas y receptivas, y asígneles una sensación ligera. Independientemente de la forma en la que se encuentren las animaciones, nadie quiere sentir como están esperando. Diseñe animaciones más pesadas para tener una degradación estable.
6.  Diseño para la ejecución prolongada. Si una animación es molesta, distrae o una tarea ardua, rediseñela o quítela.

## <a name="usage-patterns"></a>Patrones de uso

Las animaciones tienen varios patrones de uso:



|                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Comentarios de mantener el mouse**<br/> para mostrar Dónde está el punto de interacción. <br/>                                | Indica que el punto de interacción está activo. el puntero del mouse se puede mostrar también a través de un efecto estático.<br/> vocabulario de Windows: muestra el efecto de mantener el mouse (rectángulo delimitador, resaltar, ampliación) con un efecto de fundido o fundido de salida por suavidad. <br/> ![captura de pantalla de una de las seis cubiertas de álbumes resaltadas ](images/vis-animations-image24.png)<br/> En el reproductor multimedia digital Zune, el álbum cubre resaltar y agregar controles de reproducción al mantener el mouse.<br/>                                                                                                                                                                                                                 |
| **Haga clic en comentarios**<br/> para mostrar que un objeto en el que se pueda hacer clic tiene capacidad de respuesta y recibe un clic. <br/>    | Indica que se ha realizado un clic en un objeto.<br/> vocabulario de Windows: fondo del objeto Flash al hacer clic en el evento click. para mostrar contacto táctil, use un efecto de rizo. <br/> ![Foto del dedo en la pantalla táctil que muestra los onduladores ](images/vis-animations-image25.png)<br/> Touch muestra una animación de rizo para que el usuario sepa que se reconoció la interacción.<br/>                                                                                                                                                                                                                                                                                                         |
| **Comentarios de selección**<br/> para mostrar que un objeto está seleccionado. <br/>                                | Indica que se ha seleccionado un objeto. la selección se puede mostrar también a través de un efecto estático.<br/> vocabulario de Windows: dibuje el rectángulo de selección con un efecto de fundido o fundido de salida por suavidad. <br/> ![figura de una portada de álbum en la que se hizo clic y se selecciona ](images/vis-animations-image26.png)<br/> En Zune, el álbum cubre la intermitencia al hacer clic y, a continuación, obtener un rectángulo de selección en la selección.<br/>                                                                                                                                                                                                                                                                      |
| **Comentarios sobre el progreso**<br/> para mostrar que se está llevando a cabo una tarea. <br/>                             | Los comentarios de progreso indican que una tarea está realizando un progreso, normalmente con indicadores de actividad, barras de progreso o animaciones que muestran la tarea. Determine la información de progreso muestra aproximadamente la cantidad de tarea que se ha realizado y la cantidad de tiempo restante, mientras que el progreso indeterminado solo indica que se está realizando la tarea.<br/> vocabulario de Windows: girar los indicadores de actividad, las barras de progreso, los avances de progreso, las animaciones de ilustración. <br/> ![captura de pantalla del cuadro de diálogo con el texto "iniciando sesión" ](images/vis-animations-image27.png)<br/> En este ejemplo, Windows Live Messenger muestra comentarios de progreso indeterminados durante el inicio de sesión.<br/> |
| **Atraer**<br/> para mostrar que algo necesita la atención del usuario. <br/>                          | Atraiga el nivel de atención adecuado cuando se crean objetos significativos o se necesita atención (a menudo debido a un cambio), o cuando se producen eventos importantes o urgentes. vea [atraer el nivel de atención adecuado para las](#attracting-the-right-level-of-attention) técnicas de diseño.<br/> vocabulario de Windows: parpadeo, movimiento, pulso, resplandor, Gleam. <br/> ![captura de pantalla que muestra la animación de la barra de herramientas ](images/vis-animations-image28.png)<br/> La barra de herramientas de Windows Live anima en la primera apariencia para que sea obvio Dónde está.<br/>                                                                                                                                 |
| **Relación**<br/> para mostrar la relación entre los objetos o la causalidad en efectos. <br/>        | Mostrar las relaciones, sobre todo si la relación no se puede entender o se espera, de una manera que no distraiga o sea confusa.<br/> vocabulario de Windows: transformación, transporte, cambio físico, como el volteo, el aumento desde un origen de punto y la reducción hasta un destino de punto. <br/> ![captura de pantalla del cuadro de diálogo calibración de color](images/vis-animations-image29.png)<br/> En este ejemplo, la animación muestra la relación entre el valor gamma y su efecto en la presentación.<br/>                                                                                                                                                    |
| **Ilustración/vista previa**<br/> explicar visualmente un concepto, una tarea o el efecto de un comando. <br/> | Animación o vídeo que explica un concepto o cómo funciona visualmente, ya sea para complementar o reemplazar una explicación textual. Esto permite a los usuarios realizar tareas o elegir comandos de forma eficaz y confiable. <br/> ![captura de pantalla del error ortográfico de corrección de lápiz ](images/vis-animations-image30.png)<br/> En este ejemplo, los comandos "mostrarme" del panel de entrada de Tablet PC utilizan ilustraciones para mostrar cómo corregir, eliminar, dividir y combinar.<br/>                                                                                                                                                                                                        |



 

Las transiciones tienen varios patrones de uso:



|                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Objeto de aumentar/reducir/Mostrar**<br/> cambiar el tamaño o el estado de un objeto sin problemas. <br/>                                                                                                         | Cambios de objeto entre Estados, posiblemente durante el movimiento. la transición mantiene a los usuarios orientados durante los cambios.<br/> vocabulario de Windows: transformación, cambiar tamaño, deslizar diapositivas de objeto. <br/> ![captura de pantalla de tres tamaños de gadgets meteorológicos ](images/vis-animations-image31.png)<br/> En este ejemplo, el gadget Weather se transforma desde su estado conciso para mostrar el cuadro de diálogo Opciones.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Mostrar/ocultar/cambiar contenido**<br/> para mostrar, ocultar o cambiar el contenido de forma fluida, normalmente para la divulgación progresiva. <br/>                                                                       | El interior de la ventana cambia de forma para mostrar más contenido, menos o diferente. la transición mantiene a los usuarios orientados durante los cambios.<br/> vocabulario de Windows: el panel se desliza dentro o fuera. ventanas de control flotante fundido y salida. se atenúa o se revierte el contenido diferente. <br/> ![captura de pantalla de tres tamaños de calculadora ](images/vis-animations-image32.png)<br/> La calculadora de Windows tiene una transición fluida entre modos de vista.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Control u disponibilidad Mostrar u ocultar**<br/> para mostrar u ocultar sin problemas los controles o sus prestaciones al mantener el mouse o mover el mouse para simplificar la apariencia visual normal. <br/>                | Muestra los controles cuando los usuarios desplazan el puntero sobre un área de comandos o muestran prestaciones cuando los usuarios mantienen el mouse sobre un control. al mantener el mouse sobre estas áreas se indica que el usuario intenta interactuar. las prestaciones pueden ocultarse si el puntero se convierte en estacionario. <br/> ![captura de pantalla de controles desplazados antes de mantener el mouse ](images/vis-animations-image33.png)<br/> En este ejemplo, los controles de Windows Media Player atenuan al mantener el mouse en el modo de pantalla completa.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Transiciones de escena**<br/> para que una transición de escena sea fluida y fluida con el fin de evitar la atención. <br/>                                                                                   | Los cambios bruscos de la escena pueden ser Discordante, especialmente en el caso de áreas de pantalla grandes, por lo que deben usarse transiciones de escena para crear suavidad y continuidad, y para proporcionar contexto. las transiciones de escena están diseñadas para ser una clave natural y baja, para evitar llamar la atención al proceso de transición.<br/> vocabulario de Windows: fundido de salida/salida; fundido cruzado; deslizar hacia arriba/izquierda, fuera/derecha, arriba, abajo; inserciones y cubiertas. <br/> ![captura de pantalla de una fotografía en otro ](images/vis-animations-image34.png)<br/> En este ejemplo, el papel tapiz del escritorio de Windows se atenúa suavemente entre las imágenes para que la transición sea fluida y controlada.<br/>                                                                                                                                                                                                                                                                                                                               |
| **Transiciones de escena especiales**<br/> atraer la atención a un cambio en la escena para que sea especial o recentre la atención del usuario. <br/>                                                               | Aunque la mayoría de las transiciones de escena no deben llamar a la atención del proceso de transición, algunas están diseñadas para romper el flujo y atraer la atención para resaltar que algo diferente está a punto de producirse. para atraer la atención, las transiciones de escena especiales están diseñadas para ser poco naturales y tienen un gran impacto visual. <br/> ![captura de pantalla de la diapositiva de transición de captación de atención ](images/vis-animations-image35.png)<br/> En este ejemplo, PowerPoint utiliza las transiciones de obtención de atención para dibujar la audiencia en el cambio.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Manipulaciones directas**<br/> para mostrar el efecto de las manipulaciones directas (como mover, desplazar/panoramizar, girar y acercar). <br/>                                                                   | La transición muestra el efecto de la manipulación en tiempo real. el efecto debe ser suave, continuo y coherente con el mundo real. es posible que el movimiento y la rotación no sean continuos en algunos lugares para indicar restricciones o posibles opciones preferidas. el zoom hace que el contenido sea más grande o más pequeño, lo que podría cambiar el nivel de detalle en consecuencia. <br/> ![captura de pantalla de tres tamaños de lupa ](images/vis-animations-image36.png)<br/> En este ejemplo, el ampliador amplía sin problemas los niveles.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Manipulaciones directas incorrectas**<br/> para indicar que se intentó una manipulación directa (por ejemplo, movimiento, desplazamiento o panorámica), pero no se pudo realizar. <br/>                                           | La transición muestra la manipulación que se está intentando, pero vuelve al estado original. a menudo, el efecto es similar a la manipulación que no se puede realizar debido a una restricción física real. Estas animaciones se usan en lugar de los mensajes de error basados en texto, lo que interrumpiría la sensación del mundo real de la manipulación.<br/> vocabulario de Windows: Bounce <br/> ![figura de animación que se comunica visualmente ](images/vis-animations-image4.png)<br/> En este ejemplo, el documento rebota para mostrar que el usuario ha alcanzado el final.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Ordenar, filtrar y reordenar las transiciones**<br/> para indicar que la presentación o el contenido de una colección de elementos ha cambiado. <br/>                                                            | La transición muestra (o para cambios complejos, sugiere) el efecto del cambio. <br/> ![captura de pantalla de las cámaras de filas con tres quitadas ](images/vis-animations-image37.png)<br/> ![captura de pantalla similar con diferentes cámaras quitadas ](images/vis-animations-image38.png)<br/> ![captura de pantalla similar con otras cámaras quitadas ](images/vis-animations-image39.png)<br/> en este ejemplo, Bing Visual Search usa una transición de filtro.<br/> ![captura de pantalla de la portada del álbum cambiar su apariencia ](images/vis-animations-image40.png)<br/> En este ejemplo, Windows Media Center usa una transición de reordenación como una experiencia especial mientras se reproduce una canción.<br/>                                                                                                                                                                                                                                                                                   |
| **Transiciones de rendimiento**<br/> para hacer que una acción parezca más rápida. <br/>                                                                                                              | Aunque cualquier transición tiene la posibilidad de hacer que una acción parezca más rápida, el propósito principal de estas transiciones es mejorar la percepción del rendimiento y la capacidad de respuesta. una buena técnica es mostrar la tarea realizada en pasos deliberados. por el contrario, el retraso de la acción, la representación de los resultados de forma aleatoria o el uso de un indicador de actividad se verán lentos.<br/> vocabulario de Windows: realiza una acción en fases, con transiciones suaves entre las fases. <br/> ![captura de pantalla de la adición de destinos de la Jump List ](images/vis-animations-image41.png)<br/> En este ejemplo, una Jump List de la barra de tareas muestra inmediatamente los elementos estándar y, a continuación, se desliza hacia afuera para mostrar los destinos una vez que la lista esté preparada. Al hacerlo, se camufla el tiempo necesario para crear la lista. Por el contrario, el retraso de la pantalla inicial no funcionaría y mostraría una lista incompleta o la información sobre el progreso sería mucho más lenta.<br/> |
| **Experiencias especiales**<br/> para atraer a los usuarios y satisfacer las [experiencias especiales](glossary.md) infrecuentes que son importantes para el programa y tener la atención del usuario. <br/>    | Aunque cualquier transición tiene la posibilidad de ser una experiencia especial, estas transiciones se reservan mejor para experiencias poco frecuentes que son realmente especiales para el programa. las transiciones personalizadas se usan para dar una sensación especial. la personalización de marca y la personalidad suelen ser elementos de diseño importantes. a diferencia de otros patrones, las experiencias especiales pueden solicitar atención, ser pesadas y requerir que los usuarios esperen un momento. por lo tanto, estas transiciones se gastan rápidamente si se sobreutilizan porque la experiencia ya no es especial. <br/> ![captura de pantalla del cambio del logotipo de Windows a nueva pantalla ](images/vis-animations-image42.png)<br/> En este ejemplo, Windows Media Center muestra una animación mientras se carga para interactuar inmediatamente con los usuarios.<br/>                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a>Directrices

### <a name="effective-communication"></a>Comunicación efectiva

-   **Definir y usar un vocabulario de animación** para asegurarse de que las animaciones y las transiciones tienen un significado coherente y usarlas de forma coherente en todo el programa. La mayoría de los vocabularios deben incluir entradas para la apariencia de la escena y el objeto, y la desaparición, navegación, interacción básica (mantener el mouse, seleccionar, hacer clic), manipulación de objetos e interacción (movimiento, eliminación, cambio de tamaño, desplazamiento, movimiento panorámico, zoom, rotación, filtrado) y atraer la atención. El significado coherente es fundamental para una comunicación eficaz.
-   **Siempre que sea práctico, use el vocabulario de animación de Windows.** Aunque el programa puede tener una audiencia diferente y necesidades diferentes, a menudo las ventajas de coherencia y familiaridad compensan las ventajas de ser diferentes. Si el vocabulario del programa debe ser diferente, utilice los mismos tipos de animación básicos que Windows, pero asígneles la personalidad adecuada para el programa.
-   **No asigne significados específicos a animaciones y transiciones genéricas en un vocabulario de animación.** Las transiciones genéricas, como las transiciones y los efectos especiales, como las dessoluciones, no tienen ningún significado determinado (más allá aparecen o desaparecen), por lo que se pueden usar libremente.

    **Incorrecto:**

    ![captura de pantalla de un cuadro de diálogo difuminado en otro ](images/vis-animations-image43.png)

    En este ejemplo, se usa incorrectamente un fundido cruzado para desplazarse al elemento siguiente. Dado que los fundidos cruzados no tienen ningún significado determinado, esta transición no proporciona contexto.

-   **Cree entradas de vocabulario claramente distintas.** Las acciones relacionadas pueden tener efectos similares (por ejemplo, el zoom y el zoom deben tener transiciones inversas), pero las acciones no relacionadas deberían tener efectos claramente distintos (por ejemplo, el zoom nunca debe confundirse con la rotación).
-   **Mantenga los efectos reales y realistas.** Si utiliza animaciones y transiciones realistas, mantenga la experiencia coherente con el mundo real. Los usuarios nunca deben sorprender, confundir ni inducir a engaño por los resultados. Y, por coherencia, no mezcle metáforas.
-   **Proporcionar animaciones inversas de acciones inversas.** Al hacerlo, se cumplen las expectativas del usuario y se simplifica el vocabulario. Por ejemplo, si un panel aparece deslizando en, quítelo deslizando no con ningún otro efecto.
-   **Cree animaciones comprensibles.** Los usuarios deben poder comprender rápidamente el propósito de una animación. Es posible que una animación sea demasiado pequeña, demasiado breve (menos de 50 milisegundos) o tan sutil que los usuarios no puedan comprender su finalidad. En tales casos, debe volver a diseñar para que el significado sea claro o quitar.

    **Incorrecto:**

    ![captura de pantalla de la animación en el cuadro de diálogo eliminar ](images/vis-animations-image44.png)

    En este ejemplo, el efecto es tan pequeño e sutil que pocos usuarios pueden entender su finalidad. Mejor rediseñar o quitar.

### <a name="patterns"></a>Patrones

**Comentarios de mantener el mouse**

-   **Para que parezca que responde, intente reproducir la animación en un plazo de 50 milisegundos a la entrada o salida del estado de activación.**
-   **Para que parezca rápida, haga que la duración de las animaciones de desplazamiento sea inferior a 50 milisegundos.**
-   **Use un efecto de atenuación o desvanecimiento de desplazamiento.** Al hacerlo, los efectos de mantener el mouse son claramente distintos de los comentarios de clic y selección.

**Haga clic en comentarios**

-   **Para que parezca que responde, procure reproducir la animación dentro de 50 milisegundos del evento de clic.** Haga clic en no es necesario hacer clic en eventos.
-   **Para que parezca rápida, haga que la duración de las animaciones de clic sea inferior a 50 milisegundos.**
-   **Use un efecto de parpadeo o destello de fondo.** Al hacerlo, los efectos de clic se hacen claramente distintos de los comentarios de los punteros y las selecciones. Dado que al hacer clic en se requiere mantener el puntero, haga clic en comentarios para mantener el mouse sobre los comentarios.

**Comentarios de selección**

-   **Para que parezca responder, procure reproducir la animación en un plazo de 50 milisegundos de selección o anulación de selección.**
-   **Para que parezca rápida, haga que la duración de las animaciones de selección sea inferior a 50 milisegundos.**
-   **Use un efecto de rectángulo de selección de fundido o fundido de salida.** Esto hace que la selección sea claramente distinta de Hover y haga clic en Comentarios.

**Comentarios sobre el progreso**

-   **Use un indicador de actividad cuando no se puede realizar una acción en un segundo.** Esto indica que se ha recibido el comando.
-   **Use una barra de progreso cuando una tarea tarde más de cinco segundos.** Para obtener más instrucciones, vea [barras de progreso](progress-bars.md).
-   **Use animaciones de comentarios de progreso que ayuden a los usuarios a visualizar el efecto de las tareas de ejecución prolongada.** Evite animaciones de comentarios de progreso innecesarias si una animación no comunica nada que le resulte útil, en su lugar, use una barra de progreso.
-   **Tienen Estados de finalización y error claramente identificados.** Los usuarios deben poder determinar rápidamente estos estados finales.
-   **Dejar de mostrar el progreso cuando la tarea subyacente no progresa.** Los usuarios deben ser capaces de determinar si el progreso no se realiza y reaccionar en consecuencia.

**Atraer a**

-   **Usar atraer con sujeción.** A menos que la información sea urgente, crítica o que, de otro modo, afecte al comportamiento inmediato del usuario, suele ser mejor cambiar el estado de manera inadecuada y permitir que los usuarios detecten el cambio por su cuenta. [Resolver distracciones, no detectabilidad](/windows/desktop/uxguide/how-to-design-desktop-ux).

    ![captura de pantalla de iconos de estado inalámbricos ](images/vis-animations-image45.png)

    En este ejemplo, el icono del área de notificación de red inalámbrica usa una animación para los problemas críticos, pero permite a los usuarios detectar señales débiles por su cuenta.

-   **Elija una animación que dibuje el nivel de atención adecuado.** Las animaciones de atraer deben dibujar la atención suficiente para satisfacer su finalidad, pero no más. Si el usuario debe actuar inmediatamente, elija un efecto que requiera atención independientemente de dónde esté buscando el usuario. En el caso de otras situaciones, consulte la sección sobre cómo [atraer el nivel de atención adecuado](#attracting-the-right-level-of-attention) para obtener la combinación adecuada de atención, aviso y urgencia.

    **Incorrecto:**

    ![captura de pantalla del Asistente para oficinas de sujetapapeles ](images/vis-animations-image46.png)

    Los asistentes de Microsoft Office atraen su atención innecesaria.

-   **Si el usuario no responde, no repita la animación ni use animaciones continuas.** En su lugar, supongamos que el usuario decidió no actuar ahora, pero puede actuar más adelante. Las animaciones continuas dificultan a los usuarios concentrarse en todo lo demás.

**Animaciones de relación**

-   **Use animaciones de relación para mostrar de dónde proceden los objetos o de dónde fueron.**
-   **Las animaciones de relación deben comenzar o finalizar con el objeto seleccionado.** No mostrar las relaciones entre los objetos en los que el usuario no está interactuando actualmente. Si los usuarios detectan, lo que observará es la distracción.

**Ilustraciones y versiones preliminares**

-   **Use las vistas previas para mostrar el efecto de un comando sin que los usuarios tengan que realizarlo primero.** Mediante el uso de vistas previas útiles, puede mejorar la eficacia y la facilidad de aprendizaje de su programa, y reducir la necesidad de pruebas y errores.
-   **Use ilustraciones y versiones preliminares que tengan una interpretación clara.** Tienen poco valor si son confusos.
-   **Juegue solo una ilustración a la vez** para evitar abrumar a los usuarios. Si hay varias ilustraciones simultáneas posibles, use el puntero del mouse o un botón de reproducción para permitir que los usuarios indiquen su interés.
-   **Reproducir una ilustración automáticamente si es el propósito principal de la ventana o la página.** De lo contrario, si es opcional, permita a los usuarios reproducirlo cuando estén listos.
-   **Reproducir animaciones a la velocidad óptima**: no es tan rápida que sean difíciles de entender, pero no es tan lenta que son tediosas de ver.

**Crecimiento y reducción del objeto**

-   **No recortar el contenido durante un ajuste de tamaño.** Expanda contenedores antes de agregar contenido. Quite el contenido antes de reducir los contenedores.

    **Incorrecto:**

    ![captura de pantalla de la calculadora truncada ](images/vis-animations-image47.png)

    En este ejemplo, el contenido se recorta durante un ajuste de tamaño.

**Mostrar/ocultar/cambiar contenido**

-   **Mostrar información importante estáticamente.** Los usuarios no deben tener que acceder a información importante a través de una divulgación progresiva.

**Control u disponibilidad Mostrar u ocultar**

-   **Muestra controles importantes cuando el usuario coloca el puntero en cualquier parte dentro de la ventana o panel, o bien, si la pantalla completa, al moverse del mouse.** Los usuarios no deben tener que buscar estos controles, por lo que debe realizar su detección.

    ![Ilustración en la que se muestra cómo mantener el mouse en controles ](images/vis-animations-image48.png)

    En este ejemplo, Windows Media Center muestra sus controles cada vez que el puntero está sobre la ventana.

-   **Muestra los controles secundarios o las prestaciones de control cuando el usuario coloca el puntero sobre los comandos o cerca de ellos.** Para facilitar la detección, haga que la ubicación sea obvia y el objetivo sea grande.

    ![captura de pantalla de un comando secundario que revela el puntero ](images/vis-animations-image49.png)

    En este ejemplo, Windows Live Messenger muestra un comando secundario cuando el puntero está cerca de la esquina superior derecha.

**Transiciones de escena**

-   **Realizar transiciones de escena física coherentes con la asignación natural.** Las personas leen de izquierda a derecha en las referencias culturales occidentales y los diagramas jerárquicos fluyen de arriba abajo. Por consiguiente, el avance en el tiempo se indica mediante el movimiento de izquierda a derecha. Las siguientes transiciones de escena física tienen una asignación natural:



    | Transición                          | Significado                                     |
    |---------------------------|--------------------------------------|
    | Desde la izquierda<br/>      | Retroceder en el flujo de tareas<br/>    |
    | Desde la derecha<br/>     | Avanzar en el flujo de tareas<br/> |
    | Desde arriba<br/>       | Subir jerarquía de tareas<br/>    |
    | Desde abajo<br/>    | Bajar la jerarquía de tareas<br/>  |



 

-   **Si el programa reproduce sonidos, transiciones de escena de diseño y transiciones de audio juntas.** Por ejemplo, si una escena se atenúa gradualmente, cualquier sonido también debe atenuarse gradualmente. No se dañen transiciones visuales sin problemas con transiciones bruscas de sonido. Para obtener más instrucciones sobre el sonido, consulte [sonido](vis-sound.md).

**Manipulaciones directas**

-   **Al usar gestos físicos en la interacción (como la descartando), diseñe la animación para sentirse como una respuesta natural al movimiento.** Vincule la causa de interacción con el efecto de transición. Proporcione las características físicas del mundo real de la animación, como la aceleración, la desaceleración, el momento, la resistencia, la ponderación y la rotación.
-   **Para mantener una sensación directa, mantenga los puntos de contacto de un objeto bajo el puntero sin problemas a lo largo de la interacción.** Cualquier retraso, respuesta entrecortada o pérdida de contacto destruye la percepción de la manipulación directa. Los objetos nunca deben desaparecer mientras se manipulan.

**Ordenar, filtrar o reordenar las transiciones**

-   **Para realizar cambios sencillos, muestre la transición completa.** Los usuarios podrán seguir toda la transición fácilmente. Los cambios sencillos implican cuatro elementos o menos.
-   **En el caso de cambios complejos, resalte el final del movimiento a medida que se ralentiza y deje que el ojo rellene el resto.** Esto hace que el movimiento parezca mucho más receptivo y ordenado.

**Transiciones de rendimiento**

-   **Considere la posibilidad de realizar transiciones lentas en dos o tres fases para que aparezcan de forma más rápida e interactiva.** Use el siguiente orden de composición cuando corresponda:
    -   Marco externo
    -   Información previa
    -   Contenido inicial (con una representación temporal si es necesario)
    -   Controles principales (para que los usuarios puedan interactuar inmediatamente)
    -   Controles secundarios y cualquier otro elemento de la interfaz de usuario
    -   El contenido final (si se usó una representación temporal) Use transiciones como atenuaciones y diapositivas para que la composición parezca suave, ordenada y refinada.

![captura de pantalla de un mapa con una foto y una cuadrícula satélite ](images/vis-animations-image50.png)

Al desplazarse en la vista "pájaro", los mapas de Bing muestran un fondo de cuadrícula temporal. De este modo, los usuarios pueden continuar desplazándose inmediatamente, bien antes de que se represente el contenido final.

**Animaciones de experiencia especiales**

-   **Reconsidere las pantallas de presentación animadas (así como las pantallas de presentación estáticas).** A menudo, las pantallas de presentación solo señalan cuánto tiempo tarda un programa en cargarse y, por lo tanto, usan su bienvenida rápidamente. Mientras que las pantallas de presentación son aceptables si solo se muestran cuando no es posible la interacción con el usuario, siempre que sea factible una mejor alternativa consiste en diseñar el programa para que los usuarios puedan interactuar con él inmediatamente, incluso mientras se está cargando.
-   **Proporcione un comando SKIP Introduction si una pantalla de presentación animada tarda más de tres segundos.** Al hacer clic en cualquier parte de la pantalla de presentación, también se debe descartar. También puede usar una versión corta de la animación después de un período inicial.

### <a name="performance"></a>Rendimiento

-   **No haga que los usuarios esperen a las animaciones y transiciones del programa.** Use animaciones y transiciones breves (menos de 200 milisegundos) siempre que sea práctico. Use animaciones más rápidas (100 milisegundos) para operaciones más frecuentes. Diseñe animaciones más largas (más de un segundo normalmente la información de progreso, la ilustración y patrones de experiencia especiales) para que los usuarios puedan seguir trabajando mientras se ejecutan.
-   **Diseñe animaciones de ejecución prolongada para que quede claro a los usuarios que pueden interactuar mientras se está ejecutando la animación.** Los usuarios no intentarán continuar trabajando si las indicaciones visuales sugieren que no lo hacen.

    ![captura de pantalla de una barra de progreso en una barra de estado ](images/vis-animations-image51.png)

    En este ejemplo de Windows Internet Explorer, la barra de progreso de baja clave de la barra de Estado sugiere que los usuarios no tienen que esperar a que se completen para poder interactuar.

-   **Use animaciones ligeras para tareas de uso intensivo de la CPU.** Al hacerlo, se proporciona la capacidad de procesamiento total de la tarea. Además, los usuarios no percibirán que la animación ligera es el motivo por el que la tarea requiere una gran cantidad de CPU.
-   **No mostrar un indicador de actividad durante una animación o una transición.** Al hacerlo, se destruye el efecto. Diseñe animaciones y transiciones para que puedan iniciarse inmediatamente.
-   **Diseñe animaciones para que se reduzcan correctamente siempre que no haya suficientes recursos del sistema.** Las animaciones se pueden degradar teniendo variaciones que requieran menos recursos (por ejemplo, longitudes más cortas o velocidades de fotogramas inferiores) o incluso no se ejecuten en absoluto. Independientemente de los recursos disponibles, asegúrese de que las animaciones tienen una alta calidad y se parecen a las animaciones en lugar de errores de software.

    **Incorrecto:**

    ![captura de pantalla del marco del programa descolorida en el escritorio ](images/vis-animations-image52.png)

    En este ejemplo, se usa la transición de restauración de ventana aunque no haya suficientes recursos del sistema para reproducirla correctamente. Por lo tanto, el marco inmovilizado parece ser un error. Si los recursos no están disponibles, es mejor Mostrar la ventana sin una transición.

### <a name="animation-characteristics"></a>Características de animación

Las animaciones y transiciones bien diseñadas suelen tener estas características:

-   **Breve duración.** La mayoría de las animaciones deberían estar entre 100 y 300 milisegundos, preferiblemente de 1/6 segundos (167 milisegundos) o de 1/4 segundos (250 milisegundos). (Las experiencias especiales y los comentarios de progreso pueden ser mayores). Usar tiempos de animación más rápidos para operaciones más frecuentes. Por lo general, las animaciones más largas tardan más tiempo en completarse, tardan más tiempo en entenderse y se ven lentas.
-   **Respecto.** Las animaciones deben comenzar en 50 milisegundos del evento de inicio o de la acción del usuario. Las horas de inicio más largas no responden.
-   **Aceleración/desaceleración.** Para que parezca natural, la mayoría de los efectos de animación deben acelerarse al iniciarse y disminuir la velocidad al detenerse. Para que las animaciones de diseño sean receptivas, debe empezar con rapidez. Para que aparezcan las animaciones de diseño controladas para tener aterrizajes flexibles al final. Aunque esto se aplica a los efectos de movimiento, también se aplica a cualquier efecto que sugiera movimiento, como por ejemplo, zooms e incluso fundidos.

    ![figura de un gráfico que muestra una velocidad reducida a lo largo del tiempo ](images/vis-animations-image53.png)

    La mayoría de las animaciones deberían tener inicios rápidos y finalizadores de software para tener una sensación de respuesta, pero controlada.

-   **Disminuir.** Las animaciones que representen el movimiento en particular deben acelerar y disminuir la velocidad, por lo que no se debe usar el movimiento lineal a menos que la duración de la animación sea muy breve. Los movimientos deben tomar la ruta de acceso breves desde el principio hasta el final, sin un exceso. No siempre se requiere la ruta de acceso completa. Cuando sea necesario, resalte el final del movimiento a medida que se ralentiza y deje que el ojo rellene el resto. Esto hace que el movimiento parezca mucho más receptivo y ordenado. Al animar el movimiento de varios objetos simultáneamente, asígneles trazados ligeramente diferentes con intervalos ligeramente diferentes para sentirse más naturales.
-   **Velocidad de fotogramas.** La mayoría de las animaciones deben usar una velocidad de fotogramas de 20 fotogramas por segundo. Si la animación es para una experiencia especial o está relacionada con el propósito principal del programa, considere la posibilidad de usar una tasa más alta de 24 30 fotogramas por segundo para mejorar la suavidad y el realismo.
-   **Escala.** Diseñe animaciones para que funcionen bien en todo el intervalo de uso previsto. Por ejemplo, las transiciones de página deben diseñarse para que funcionen con todos los tamaños de página.
-   **Personalidad.** Diseñe animaciones para sentirse naturales, subdued y eficientes en lugar de artificial, divertidos o Slow.

### <a name="animated-text"></a>Texto animado

-   Aunque puede mostrar texto mediante una transición, **no anima el texto continuamente.** El texto animado suele distraerse y ser más difícil de leer que el texto estático. **Excepciones:**
    -   Puede animar el texto en situaciones en las que tradicionalmente se anima y proporciona una alternativa accesible.
    -   Puede animar el texto si el propósito del texto es principalmente decorativo.

![captura de pantalla de la interfaz Zune diseñada creativamente ](images/vis-animations-image13.png)

En este ejemplo, Zune anima el texto pero su finalidad es principalmente decorativa. No hay ningún problema si los usuarios no leen atentamente el texto.

### <a name="reducing-power-consumption"></a>Reducción del consumo de energía

-   **Diseñe las animaciones para reducir el consumo de energía.** Cuando se diseñan correctamente, las animaciones no deben aumentar significativamente el consumo de energía. Para reducir el consumo de energía:
    -   **Detener la animación cuando la pantalla esté desactivada.** La pantalla puede estar desactivada con el fin de ahorrar energía.
    -   **No use animaciones de ejecución prolongada que no se inicien por el usuario.** Las animaciones que utilizan temporizadores periódicos de alta resolución reducen la eficacia de la administración de energía del procesador. Además, asegúrese de deshabilitar los temporizadores periódicos de alta resolución cuando se completen las animaciones.
    -   **Suspender todas las animaciones cuando el sistema se queda inactivo.** El período de inactividad del usuario que se va a inactiva viene determinado por las opciones de energía del panel de control.

### <a name="accessibility"></a>Accesibilidad

-   **No use la animación como la única manera de transmitir información esencial.** Las animaciones deben comunicar información útil pero no crítica, ya que no son accesibles para los usuarios con discapacidades visuales.
-   Asegúrese de **que la información equivalente está disponible a través de otros medios,** como:

    -   **Por inspección.** Los usuarios pueden determinar la información equivalente examinando la pantalla o los objetos implicados en la animación.
    -   **Mediante una interacción simple.** Los usuarios pueden determinar la información equivalente al mantener el mouse, hacer clic o hacer doble clic.

    ![captura de pantalla de la Página principal de Bing con zonas activas ](images/vis-animations-image54.png)

    La Página principal de Bing tiene una animación inicial que revela varias zonas activas. Los usuarios también pueden mostrar las zonas activas moviendo el cursor cerca de ellas.

    Tenga en cuenta que "información equivalente" no significa información idéntica. La información puede tener un formato diferente o requerir una deducción simple.

-   **Cuando sea necesario, establezca el foco de entrada en el objeto modificado durante una transición.** Esto permite a las tecnologías de asistencia detectar dónde se produjo el cambio. Pero no cambie el foco de entrada cuando el usuario esté usando el teclado.
-   **No use animaciones ni transiciones que parpadeen rápidamente o cambien el tamaño de los objetos.** Los cambios de pantalla intermitentes y rápidos pueden ocasionar problemas para personas con dificultades de obstrucción y otras trastornos neurológicas.
-   **Permite a los usuarios desactivar las animaciones y transiciones del programa.** Para admitir esta capacidad, respete la opción desactivar todas las animaciones innecesarias del centro de accesibilidad de Windows.

    **Desarrolladores:** Puede determinar si se habilitan las animaciones mediante la API SystemParametersInfo.

-   **Diseñar tareas suponiendo que los usuarios desactiven las animaciones del programa.** Asegúrese de que esto no interrumpe significativamente el flujo de tareas.

Para obtener más instrucciones de accesibilidad, vea [accesibilidad](inter-accessibility.md).

## <a name="documentation"></a>Documentación

-   Evite hacer referencia a las animaciones siempre que sea posible. En su lugar, consulte el objeto que se anima y, si es necesario, el tipo de animación.
-   No haga referencia a las transiciones, excepto en la documentación técnica. En su lugar, haga referencia al objeto en su estado final o inicial.
-   Si el usuario inicia explícitamente una animación, use el verbo Play; de lo contrario, use el verbo use para la documentación técnica.

Ejemplos:

-   Sabrá que un elemento requiere su atención cuando su icono comienza a rebotar.
-   En primer lugar, seleccione las fotos que desea imprimir (tenga en cuenta que las fotos se amplían al seleccionar).
-   Use una transición de desvanecimiento cruzado para cambiar el estado de un objeto sin problemas.

