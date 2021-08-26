---
title: Animaciones y transiciones
description: El uso estratégico de animaciones y transiciones puede hacer que el programa sea más fácil de entender, sentir más suave, más natural y de mayor calidad, y ser más atractivo.
ms.assetid: 9e0e9604-f051-47e4-bcd0-59fbfd38b9c1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 78517835cfe9d6db0cd092b65f0e586341a6b6badc0cda3e881d765ab55507b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119937615"
---
# <a name="animations-and-transitions"></a>Animaciones y transiciones

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

El uso estratégico de animaciones y transiciones puede hacer que el programa sea más fácil de entender, sentir más suave, más natural y de mayor calidad, y ser más atractivo. Pero el uso gratuito de animaciones y transiciones puede hacer que el programa distraiga e incluso se desasoje.

Las animaciones dan la apariencia de movimiento o cambio con el tiempo. Use la animación para proporcionar comentarios, obtener una vista previa del efecto de una acción, mostrar la relación entre objetos, llamar la atención sobre los cambios o explicar visualmente una tarea.

![figura del teclado numérico con una clave resaltada ](images/vis-animations-image1.png)

Microsoft Windows una animación flash de fondo para proporcionar comentarios sobre el hecho de que se hizo clic en el objeto.

Las transiciones son animaciones que se usan para mantener a los usuarios orientados durante los cambios de estado de la interfaz de usuario (IU) y las manipulaciones de objetos, y hacer que esos cambios se sinseren sin problemas en lugar de jarring. Las transiciones buenas son naturales, lo que a menudo da la impresión de que los usuarios interactúan con objetos del mundo real.

![Captura de pantalla que muestra tres tamaños de meteorológicos.](images/vis-animations-image2.png)

Windows Desktop Desktop Usa transiciones fluidas entre sus estados concisos y de detalles.

Por lo general, las mejores animaciones y transiciones se usan para comunicarse con los usuarios de forma no verbal y para que los cambios de estado sean más naturales y menos evidentes. Por el contrario, los menos eficaces son gratuito, ya que no comunican nada ni llama la atención innecesaria. Las animaciones se usan mejor como forma secundaria de comunicación. Deben comunicar información útil pero no crítica y, para ser accesible, los usuarios deben poder determinar información equivalente a través de otros medios.

**Nota:** Las directrices relacionadas [con la personalidad](exper-branding.md)de marca de software, [el](vis-sound.md)sonido y la [accesibilidad](inter-accessibility.md) se presentan en artículos independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

Para decidirlo, tenga en cuenta las siguientes preguntas.

### <a name="animations"></a>Animaciones

¿Se aplican las condiciones siguientes?

-   La animación comunica visualmente algo útil, como proporcionar comentarios, mostrar relaciones, causas y efectos, o llamar la atención sobre cambios importantes.
-   Ver la animación no es esencial. La información equivalente se puede obtener de otra manera. Es posible que los usuarios no se beneficien de la animación si:
    -   Han desactivado las animaciones.
    -   Su atención está en otra parte.
    -   Tienen discapacidades visuales.
    -   Otra ventana oculta la animación.
    -   La animación no se reproduce debido a un rendimiento insuficiente del sistema.
-   La animación no afecta a la productividad del usuario. Tener instaladas localmente una de las siguientes:
    -   Se produce rápidamente (200 milisegundos o menos).
    -   No interfiere con la interacción o se puede interrumpir.
    -   El usuario tiene que esperar de todos modos.
-   La animación no afecta al flujo del usuario.
    -   Está en el centro de atención del usuario o llama la atención a algo fuera del centro de atención que es importante o útil para completar una tarea.
    -   Se puede ignorar fácilmente, no distraer ni fastidiar.
    -   No se vuelve agotador. Los usuarios siguen siendo adecuados y divertidos incluso después de una visualización repetida.

Si es así, considere la posibilidad de usar una animación.

### <a name="transitions"></a>Transiciones

¿Cambia el estado de un objeto o escena y se aplican todas las condiciones anteriores para usar animaciones, así como cualquiera de las condiciones siguientes?

-   El cambio de estado es conceptualmente desorienta, confuso o difícil de entender.
-   El cambio de estado es visualmente jarring, carece de continuidad, suavizado o flashes; o parece poco natural, sin perfil o de baja calidad, especialmente si implica un área de pantalla grande.
-   El uso de una transición haría que el cambio de estado parezca más rápido.
-   El cambio de estado merece una atención especial del usuario.

Si es así, considere la posibilidad de usar una transición.

## <a name="design-concepts"></a>Conceptos de diseño

Las animaciones y transiciones son una manera eficaz de comunicar visualmente información que, de lo contrario, requeriría texto para explicar o que los usuarios podrían perder.

**Incorrecto:**

![captura de pantalla del cuadro de diálogo con el mensaje ](images/vis-animations-image3.png)

**Correcto:**

![figura de animación que se comunica visualmente ](images/vis-animations-image4.png)

El uso de una animación comunica la misma información, pero de forma natural y discreta. ¿Cuál prefiere ver mil veces?

**Las animaciones y transiciones no tienen que exigir atención para que se puedan realizar correctamente.** De hecho, a menudo se usan para evitar llamar la atención sobre la mecánica del programa que los usuarios no necesitan tener en cuenta. Muchas animaciones correctas son tan naturales que los usuarios ni siquiera las conocen; en lugar de que los usuarios solo noten su ausencia. La frecuencia de repetición aumenta la necesidad de sutilidad, por lo que ahorra efectos que demandan atención para eventos poco frecuentes que realmente merecen la atención.

![captura de pantalla de todos los programas que cambian a flecha atrás ](images/vis-animations-image5.png)

Una menú Inicio que evita llamar la atención.

Además de facilitar el comprender el programa y sentirse más suave, las animaciones y transiciones bien diseñadas son una excelente manera de agregar personalidad, carácter y estilo **al programa.** Pueden hacer que la experiencia del usuario sea más envolvente y atractiva al darle una sensación natural y real.

![ilustración que muestra cómo afecta el mantener el puntero al color del botón ](images/vis-animations-image6.png)

Windows 7 resalta los botones de la barra de tareas al mantener el puntero en función de la posición actual del mouse y el color del icono del programa. Este enfoque es visualmente atractivo, pero sutil, que transmite una personalidad elegante.

**Sin embargo, las animaciones y transiciones son más eficaces y bienvenidas cuando sirven para un propósito claro.** Se deben usar para mejorar la facilidad de uso, la subilidad y el flujo, y la percepción de calidad, sin dañar significativamente el rendimiento.

Aunque algunos tipos de animaciones se usan para llamar la atención del usuario, asegúrese de que la atención sea merecida y merecedora de interrumpir el entrenamiento de reflexión del usuario. El ojo humano es sensible al movimiento, especialmente al movimiento periférico. Puede ser difícil para los usuarios concentrarse cuando hay un botón de la barra de tareas intermitente o un icono de área de notificación de giro. **Evite usar animaciones para interrumpir o distraer a los usuarios, o llamar la atención sobre cosas que no garantizan la atención del usuario.**

**Incorrecto:**

![Figura del botón de la barra de tareas resaltado sin motivo alguno ](images/vis-animations-image7.png)

Los programas no deben flashear el botón de la barra de tareas a menos que los usuarios deban hacer algo importante inmediatamente. En este caso, lo único que el usuario necesita hacer es activar el programa.

**Use animaciones y transiciones porque el programa las necesita, no simplemente porque puede.** Y para la accesibilidad, no use la animación como única manera de transmitir información esencial. Asegúrese de que los usuarios pueden obtener información equivalente de una manera diferente.

### <a name="attributes-of-good-animations-and-transitions"></a>Atributos de buenas animaciones y transiciones

Las animaciones y transiciones correctas encuentran el equilibrio correcto entre estos atributos:

-   **Son claramente propósitos.** Las animaciones buenas están ahí porque deben ser, ya sea para comunicar información, hacer que una interacción se sienta real o llamar la atención sobre algo destacable. Y las animaciones con propósito son precisas; si una animación muestra que se está haciendo una tarea, se debe a que la tarea se está haciendo de hecho.

**Incorrecto:**

![captura de pantalla del icono de batería y la etiqueta de carga completa ](images/vis-animations-image8.png)

En este ejemplo, la animación muestra que se está cargando una batería totalmente cargada.

-   **Apariencia suave y continua.** Las animaciones correctas quitan sin problemas las juntas entre la escena o los cambios de estado de los elementos mostrando las relaciones y proporcionando una sensación de lugar y contexto. La continuidad ayuda a los usuarios a comprender cómo llegaron donde están y cómo volver a su lugar de donde han llegado.

![captura de pantalla de tres vistas previas de la ventana de la barra de tareas ](images/vis-animations-image9.png)

La Windows vista previa de la barra de tareas 7 se transforma para la continuidad a medida que el usuario se mueve de un programa a otro.

-   **Son realistas.** Las animaciones buenas simulan las propiedades físicas y el comportamiento reales de un objeto. Esto ayuda a los usuarios a predecir y comprender los resultados de sus interacciones. No es necesario modelar el mundo real exactamente, pero si usa animaciones realistas, debe mantenerlas coherentes con el mundo real. Los resultados nunca deben confundir a los usuarios, especialmente con las animaciones usadas para la manipulación directa.

![figura del botón de la barra de tareas arrastrado a la nueva posición ](images/vis-animations-image10.png)

En este ejemplo, la animación "moverse fuera del camino" que usa la barra de tareas Windows 7 resulta más realista que un punto de inserción estático.

-   **Son auténticos.** Incluso los objetos que no se encuentran en el mundo real pueden parecer naturales al basarse en el comportamiento real de un objeto diferente, pero relacionado. Esta metáfora solo funciona si la relación comunica claramente el propósito y el comportamiento previstos.

![captura de pantalla del efecto elevado detrás de la ventana movida ](images/vis-animations-image11.png)

En este ejemplo, la animación de ventana "squeegee" usada por Windows 7 parece autenticada porque es coherente con el comportamiento de las ventanas de cristal en el mundo real.

-   **Use la asignación natural.** Las asignaciones naturales son físicas o culturales. Una asignación natural basada en la cultura, por ejemplo, podría comenzar por el hecho de que, en las culturas occidental, las personas leen de izquierda a derecha. Por lo tanto, para expresar una secuencia de tiempo de objetos, el objeto central es actual, los objetos a la izquierda proceden del pasado y los objetos a la derecha están en el futuro. El desplazamiento de izquierda a derecha indica el avance en el tiempo.

![captura de pantalla de la barra de progreso del reproductor multimedia ](images/vis-animations-image12.png)

En este ejemplo, el control Reproductor de Windows Media tiene una asignación natural porque la reproducción mueve la posición de izquierda a derecha.

-   **Tener personalidad.** Las animaciones bien elegidas son excelentes maneras de agregar personalidad, carácter y estilo al programa. Pueden hacer que la experiencia del usuario sea más envolvente y atractiva. Aunque el tipo de animación determina lo que se comunica, la forma específica en que se realiza la animación muestra la personalidad del programa. Las animaciones correctas proyectan la personalidad adecuada para el programa, ya sea grave o llorón, o en algún lugar entre ellos.

![captura de pantalla de la interfaz zune diseñada de forma creadora ](images/vis-animations-image13.png)

En este ejemplo, Zune el uso de texto animado y la perspectiva dinámica ayudan a dar forma a su personalidad.

-   **Mire y se sienta dinámico.** Las animaciones buenas no dañan la productividad del usuario al bloquear a los usuarios de otras interacciones o forzar a los usuarios a verlos. Independientemente de lo natural y atractiva que sean las animaciones del programa, nadie quiere esperarlas exclusivamente. Las animaciones buenas también parecen con capacidad de respuesta sin tener que hacer un arranque rápido con un aterrizaje suave. Las animaciones con capacidad de respuesta también se benefician de la comunicación rápida de su propósito. Los usuarios no deben tener que ver una animación durante mucho tiempo solo para averiguar qué hace o cuándo se hace. Para la manipulación directa, las animaciones con capacidad de respuesta son esenciales para mantener una sensación directa y atractiva en el mundo real. Para que sea directo, los puntos de contacto de un objeto deben permanecer debajo del puntero sin problemas durante la manipulación. Cualquier retraso, respuesta desmeso o pérdida de contacto destruye la percepción de manipulación directa.

![figura de dedo tocándose una pantalla táctil ](images/vis-animations-image14.png)

En este ejemplo, la transición táctil de desplazamiento panorámico parece responder manteniendo el punto de contacto bajo el dedo del usuario a lo largo de la manipulación.

-   **Atraer el nivel adecuado de atención.** Las animaciones buenas suelen ser sutiles y atraer solo la atención necesaria para cumplir su propósito. Como resultado, no distraen, son molestos, demasiado complejos, demasiado largos o repetitivos. No se cansan después de vistas repetidas.

![Captura de pantalla del resaltado de desvanecha en los nombres de archivo ](images/vis-animations-image15.png)

En este ejemplo, Windows búsqueda llama temporalmente la atención sobre las palabras de búsqueda correspondientes y, a continuación, se atenua.

-   **Tenga un aspecto especial solo si es originalmente especial.** La frecuencia aumenta la necesidad de sutilidad, por lo que las interacciones comunes necesitan animaciones simples que comuniquen una idea sencilla de una manera sencilla. Reserve animaciones especiales y complejas para experiencias especiales y poco frecuentes.

![captura de pantalla de cuatro círculos que se convierten en logotipo de windows ](images/vis-animations-image16.png)

En este ejemplo, Windows una animación de obtención de atención en el inicio para que la experiencia sea especial, pero esta animación sería inapropiada en otra parte.

Sabrá que ha logrado el equilibrio correcto cuando la experiencia general se verá dañado si se quita cualquiera de estos atributos.

### <a name="creating-an-animation-vocabulary"></a>Creación de un vocabulario de animación

Las animaciones buenas se trata de una comunicación visual eficaz y la coherencia es fundamental para su eficacia. Si usa una transición específica, como insertar una escena desde la derecha para avanzar a la siguiente escena, esa debe ser la única transición usada para ese propósito y esa transición no debe usarse para ningún otro propósito. La asignación de significados diferentes a la misma animación daña su capacidad de comunicación. Al asignar animaciones y transiciones específicas a significados específicos, se crea un vocabulario de animación.

Este problema se aplica a las animaciones y transiciones que tienen significado, no a las genéricas a las que es probable que los usuarios no asignen significado o a aquellas cuyo propósito sea no perceptible. Por ejemplo, animaciones como atenuaciones y efectos especiales, como las disminsciones, no tienen ningún significado concreto, por lo que se pueden usar libremente.

Un buen vocabulario asigna animaciones que modelan el comportamiento físico real de un objeto. Si necesita asignar una animación a un objeto o acción que no tiene un homólogo real, elija una animación que muestre cómo podría comportarse el objeto si fuera real.

![captura de pantalla de cómo el mantener el puntero hace que el logotipo de Windows se deslute ](images/vis-animations-image17.png)

Aunque el menú Inicio no es un objeto real, su efecto de mantener el puntero se enciende como un objeto real al activarse.

Cada animación de un vocabulario debe ser claramente distinta. Las animaciones solo deben tener comportamientos similares si sus acciones asociadas están relacionadas de forma similar. Por ejemplo, las transiciones de movimiento sugieren navegación, por lo que puede usar transiciones de movimiento desde distintas direcciones para indicar distintos tipos de navegación.

Sabrá que las animaciones y transiciones no se comunican bien cuando los usuarios encuentran los resultados confusos, sorprendentes o inesperados. Por lo general, es mejor lograr un solo propósito que varios propósitos no tan bien.

Lo ideal es que el vocabulario de animación sea completo en todas las áreas del programa que las necesiten. Si solo algunas interacciones tienen animaciones naturales, llamará la atención sobre las que no lo tienen.

Para más información sobre el vocabulario Windows animación, consulte la sección [Patrones](#usage-patterns) de uso de este artículo.

### <a name="designing-the-right-personality"></a>Diseño de la personalidad adecuada

Aunque el tipo de animación determina lo que comunica, la forma específica en que se realiza la animación habla con la personalidad del programa y refuerza su marca.

La personalidad del programa debe reflejar la naturaleza de sus tareas y la personalidad de sus usuarios, por lo que no es una opción arbitraria. En su lugar, una personalidad bien diseñada debe ser auténtica; nunca intente forzarlo. La personalidad debe realizar una conexión emocional con el usuario. Algunos factores que se deben tener en cuenta:

-   **Tareas:** Grave o divertido; opcional o obligatorio.
-   **Consecuencias:** Grave o menor.
-   **Costo:** Gratis o comprado; si se compra, a un precio moderado o caro.
-   **Foco de usuario:** Grupo relativamente reducido de usuarios de destino o público general amplio.
-   **Entorno de usuario:** Professional, ocasional o de inicio.
-   **Edad del usuario:** Más pequeño o mayor.
-   **Frecuencia de uso:** Frecuente o poco frecuente.

La combinación de estos factores ayuda a determinar una personalidad adecuada para el programa. Estas son algunas combinaciones adecuadas para tipos comunes de programas:

**Aplicaciones de productividad**

Naturalmente, las aplicaciones de productividad deben centrarse en la productividad. Aunque algunas experiencias especiales pueden destacar, la mayoría de las demás animaciones deben tener estas características:

-   Pequeña
-   Natural, realista
-   Sutil, subdesclado
-   Rápido, eficaz
-   Relajado

**Utilidades**

Las utilidades se suelen usar brevemente, por lo que su uso de animación puede ser más agresivo:

-   Realista, ilustrativo y autoexplicativo
-   Caja fuerte
-   Participación

**Entretenimiento, juegos**

Dado que el objetivo de estos programas es atraer y complacer a los usuarios, las animaciones y transiciones pueden ser mucho más agresivas al tener estas características:

-   Grande (posiblemente convirtiéndose en una parte integral de la experiencia)
-   Artificial, sumente
-   Impacto, dinámico
-   Emocional, juguetón, lloroso
-   Energético

La realización de una conexión emocional es tan importante para los programas de entretenimiento que es aceptable cambiar algunas reglas si esto ayuda a que los usuarios se enamanten con el programa. Por ejemplo, es aceptable si una animación o transición se vuelve agotador después de la centésima vez si es poco probable que la mayoría de los usuarios usen el programa con frecuencia.

Por lo general, las animaciones y transiciones pequeñas, naturales, subduadas, eficientes y relajadas son la opción más segura. Las transiciones con estas características suelen tomar la ruta de acceso más corta de principio a fin, iniciarse rápidamente, finalizar con su rapidez y no sobresaltos. Además, las transiciones bien diseñadas están diseñadas para funcionar bien en todo el intervalo de distancias en la que se usarán.

### <a name="animation-performance"></a>Rendimiento de animación

Al diseñar animaciones, asegúrese de que no afectan a la capacidad de los usuarios de usar el programa de forma eficaz. Por lo general, haga que las animaciones sea lo suficientemente lenta como para satisfacer su propósito, pero lo suficientemente rápida como para que no interfieran con la capacidad de respuesta, exijan demasiada atención o se vuelvan agotadores.

**Incorrecto:**

![figura de cambio de página de derecha a izquierda ](images/vis-animations-image18.png)

Aunque esta animación de cambio de página tiene una sensación atractiva y real, se abate la productividad de los usuarios, ya que tarda más tiempo en cambiar páginas.

Las transiciones breves (200 milisegundos o menos) son un caso especial (especialmente cuando a menudo funcionan sin retrasos) porque los usuarios tendrán en cuenta que tienen que esperar una división de segundo para ellos. Los usuarios están dispuestos a esperar estas animaciones si:

-   La espera percibida es muy breve (200 milisegundos o menos).
-   La transición hace que la interacción sea más fluida y natural.
-   La transición hace que la interacción tenga más capacidad de respuesta.
-   Cualquier retraso ayuda a mantener al usuario al control de la interacción.

![figura de botones de la barra de tareas arrastrados a una nueva posición ](images/vis-animations-image19.png)

Los usuarios aceptarán un breve retraso para la animación de reordenación del botón de la barra de tareas porque es muy breve y hace que la interacción sea más natural.

Hay tres maneras en las que las animaciones pueden afectar negativamente al rendimiento: velocidad, capacidad de respuesta y percepción.

En cuanto a la velocidad, algunas animaciones son elementos visuales que se ven a través de tareas que consumen mucha CPU, por lo que lo último que debe hacer es ralentizar estas tareas con animaciones que consumen mucha CPU. Las animaciones que consumen más CPU ("animaciones pesadas") tienden a:

-   Implica muchos elementos que se mueven de forma independiente.
-   Reproducir durante una larga duración o distancia.
-   Implica una gran cantidad de espacio en la pantalla.
-   Son matemáticamente intensivos.

Animaciones con menos impacto en el rendimiento:

-   Implica un solo objeto.
-   Reproducir durante una corta duración o distancia.
-   Implica una pequeña cantidad de espacio en la pantalla.
-   No son matemáticamente intensivas.

Para garantizar un buen rendimiento, las animaciones pesadas solo se deben usar para tareas que no consumen mucha CPU, mientras que las animaciones ligeras se pueden usar en cualquier lugar.

Para mejorar la capacidad de respuesta, la mayoría de las animaciones y transiciones deben diseñarse para que los usuarios puedan interactuar mientras se ejecuta la animación. A menos que una animación sea parte de un proceso, haga que sea independiente de la interacción principal del usuario y permita que los usuarios la interrumpan.

Es posible que una animación no afecte negativamente al rendimiento de una tarea en realidad, pero los usuarios pueden tener la percepción de que sí lo hace. Por ejemplo, no use una animación que parezca pesada para una tarea lenta que consume mucha CPU aunque no dañe el rendimiento, ya que los usuarios podrían concluir que la animación es la razón por la que la tarea es lenta. **Si algo parece lento, se verá lento, por lo que es mejor usar animaciones que parezcan sencillas, ligeras y rápidas.** El uso de animaciones con comienzos ajustados para tareas que consumen mucha CPU ayuda.

**Arriesgado:**

![captura de pantalla del cuadro de diálogo copiar con barra de progreso ](images/vis-animations-image20.png)

Aunque la animación del cuadro Windows de copia de archivos no daña el rendimiento de la copia de archivos, corre el riesgo de que los usuarios piensen que sí.

**También es arriesgado:**

![captura de pantalla del progreso que se muestra en la barra de direcciones ](images/vis-animations-image21.png)

En este ejemplo, la animación de progreso lento de la barra de direcciones Windows Explorer hace que algunas tareas parezcan lentas.

Las animaciones y transiciones no tienen ningún valor si su calidad es tan baja que hacen que la experiencia sea menos fluida y menos atractiva. Para mantener su calidad, las animaciones deben diseñarse para degradarse correctamente siempre que no haya suficientes recursos del sistema disponibles. Las animaciones pueden degradarse si tienen variaciones que requieren menos recursos (por ejemplo, longitudes más cortas o velocidades de fotogramas más bajas) o incluso no se ejecutan en absoluto. Independientemente de los recursos disponibles, asegúrese de que las animaciones tienen alta calidad y se parecen a animaciones en lugar de errores de software.

Por último, si los usuarios creen que las animaciones y transiciones del programa restan productividad, es muy posible que algunos usuarios quieran desactivarlas. Para admitir esta capacidad, respete la opción desactivar todas las animaciones **innecesarias que** se encuentran en el Windows Centro de accesibilidad.

### <a name="attracting-the-right-level-of-attention"></a>Atraer el nivel adecuado de atención

Aunque solo algunos tipos de animaciones y transiciones están diseñados específicamente para atraer la atención del usuario, deben diseñarse para atraer el nivel de atención adecuado para satisfacer bien su propósito. ¿Cuáles son las distintas formas de atraer la atención y cómo elegir la correcta?

**Efectos de animación**

Los distintos efectos de animación llaman la atención a distintos niveles. En la lista siguiente se resumen los métodos más comunes, empezando por el que más llama la atención:

-   **Flashing rápido.** Requiere atención inmediata. Puede interrumpir la concentración de los usuarios independientemente de dónde se produzca el parpadeo.
-   **Parpadeo moderado.** Igual, pero requiere menos atención con menor frecuencia.
-   **Rebote.** Perceptible en la visión periférico y relativamente exigente por naturaleza. Es probable que los usuarios lo observen, pero solo pueden concentrarse en otro lugar si la duración es corta.
-   **Movimiento.** Perceptible en la visión periférico, pero no exigente. Sin embargo, los movimientos complejos o 3D llaman más la atención que los movimientos simples o 2D. Es probable que los usuarios lo observen, pero pueden seguir concéntrese en otra parte.
-   **Pulsación moderada.** Perceptible, pero no distraída en la visión periférico. Los usuarios pueden seguir concéntrese en otra parte. Puede pulsar el brillo, los colores y los tamaños.
-   **Pulsación lenta o resplandezándose.** Perceptible pero sutil. Llama más la atención que un efecto estático, pero es posible que los usuarios no observen la animación a menos que ya estén buscando.
-   **Se descolora.** Incluso menos perceptible. Llama más la atención que un efecto estático, pero es posible que los usuarios no observen la animación a menos que ya estén buscando.
-   **Resaltado y resaltado estáticos.** Perceptible si los usuarios deciden buscar, pero no exigen atención si están en otro lugar.
-   **Ambiente/natural.** No se aprecia a propósito al tener una apariencia natural del mundo real.

Para determinar el enfoque adecuado para su programa o característica, tenga en cuenta cómo se relacionan estos factores con los escenarios de la característica.

Por ejemplo, suponga que está diseñando un programa de mensajes instantáneos y alguien acaba de enviar un mensaje al usuario. Este escenario requiere la atención del usuario, debe ser perceptible en cualquier lugar y normalmente el usuario querrá responder rápidamente. Este escenario sugiere que una animación de parpadeo moderado sería una buena opción. Por el contrario, suponga que desea informar a los usuarios de que se ha completado un trabajo de impresión. Los usuarios deben poder seguir concéntrese y trabajar de forma productiva en otra parte, y es aceptable si los usuarios no lo observan. Este escenario sugiere que la pulsación o el brillo de moderado a lento sería una buena opción.

**Duración**

La duración adecuada para una animación de obtención de atención depende del escenario y del tipo específico de animación utilizado. Mientras más atención exija un efecto de animación, menor será la duración. Aunque los efectos muy sutiles que exigen poca atención (como pulsaciones lentas) se pueden reproducir indefinidamente, los efectos que exigen atención solo se deben reproducir entre 1 y 3 segundos. Todo lo que sea más largo corre el riesgo de que la animación sea abrumadora y pesada.

![captura de pantalla del botón de la barra de tareas resaltado ](images/vis-animations-image22.png)

En Windows 7, la barra de tareas parpadea para que se preste atención solo durante un segundo. Más tiempo sería molesto.

**Efecto de decadencia**

Debe diseñar animaciones de obtención de atención en función de la suposición de que si los usuarios no responden de inmediato, es porque están ocupados haciendo otra cosa y no quieren que se interrumpan. Por lo tanto, el objetivo debe ser atraer la atención sin exigirlo.

Para obtener el equilibrio adecuado para atraer la atención sin exigirla, decae la intensidad de un efecto con el tiempo. Por ejemplo, para atraer la atención, puede hacer que el efecto sea fuerte inicialmente, pero luego ralentizar el efecto rápidamente. Al hacerlo, la potencia atractiva viene determinada principalmente por el efecto inicial, pero la impresión general del usuario viene determinada principalmente por su final.

![captura de pantalla que muestra una velocidad de flash reducida ](images/vis-animations-image23.png)

En Windows 7, el efecto flash de la barra de tareas se ralentiza al final.

### <a name="what-about-powerpoint"></a>¿Y PowerPoint?

Microsoft PowerPoint a menudo infringen deliberadamente estas directrices porque están diseñadas para llamar la atención sobre las transiciones deslizantes y requieren que los usuarios las esperen. Además, no tienen ningún significado concreto, por lo que no comunican nada más allá del hecho de que una diapositiva está cambiando.

PowerPoint de estilo, cuando se usan correctamente, tienen estos propósitos:

-   Interrumpen presentaciones largas en fragmentos más pequeños al forzar al presentador a pausarse.
-   Dirigen la atención del público hacia los cambios en la presentación, lo que ayuda a los usuarios a centrarse de nuevo si sus mentes se han quedados.
-   Dan a la presentación un ritmo para que no se sienta monótono o abrumador.
-   Su estilo refleja la personalidad del presentador o del material.

Aunque estos son objetivos importantes para una presentación, estas transiciones llamarían la atención innecesaria en la interfaz de usuario de la mayoría de los tipos de programas y se harían cansas rápidamente.

**Línea inferior:** No use transiciones de PowerPoint como modelo para el programa.

**Si solo hace seis cosas...**

1.  Use animaciones y transiciones para que el programa sea más fácil de entender y se sienta más suave y atractivo. Deben tener un propósito claro. No use animaciones solo porque pueda o para llamar la atención innecesaria al programa.
2.  Defina un vocabulario de animación y úselo de forma coherente en todo el programa. Use el vocabulario Windows animación 7 cuando sea necesario.
3.  Use las características de las animaciones para dar personalidad al programa y reforzar su marca.
4.  Haga que la mayoría de las animaciones sea sencilla, breve y sutil. Recuerde que las animaciones no tienen que exigir atención para ser correctas. Si una animación es adecuada y natural, los usuarios solo observarán su ausencia.
5.  Haga que las animaciones sea rápida y con capacidad de respuesta, y darles una sensación ligera. Independientemente de lo atractivas que sean las animaciones, nadie querrá sentirse esperando a ellas. Diseñe animaciones más pesadas para que tengan una degradación correcta.
6.  Diseño a largo plazo. Si una animación es molesto, distraída o tediosa, rediseñala o quítela.

## <a name="usage-patterns"></a>Patrones de uso

Las animaciones tienen varios patrones de uso:



|   Uso                                                                                                               |   Descripción                                     |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Mantener el puntero sobre los comentarios**<br/> para mostrar dónde está el punto de interacción. <br/>                                | Indica que el punto de interacción está activo. también se puede mostrar a través de un efecto estático.<br/> Vocabulario de windows: muestra el efecto de mantener el puntero (rectángulo delimitador, resaltado, reenlazamiento) con un efecto de atenuación o atenuación para suavizar. <br/> ![captura de pantalla de una de las seis portadas del álbum resaltadas ](images/vis-animations-image24.png)<br/> En el reproductor Zune multimedia digital, las portadas del álbum resaltan y agregan controles de reproducción al mantener el puntero.<br/>                                                                                                                                                                                                                 |
| **Comentarios de clic**<br/> para mostrar que un objeto en el que se puede hacer clic responde y recibe un clic. <br/>    | Indica que se ha hecho clic en un objeto.<br/> vocabulario de windows: fondo de objeto flash en el evento click down. Para mostrar el contacto táctil, use un efecto de ondulación. <br/> ![foto del dedo en la pantalla táctil que muestra ondulaciones ](images/vis-animations-image25.png)<br/> La función táctil muestra una animación de ondulación para que el usuario sepa que se ha reconocido la interacción.<br/>                                                                                                                                                                                                                                                                                                         |
| **Comentarios de selección**<br/> para mostrar que un objeto está seleccionado. <br/>                                | Indica que un objeto está seleccionado. la selección también se puede mostrar a través de un efecto estático.<br/> Vocabulario de windows: dibuje el rectángulo de selección con un efecto de atenuación o atenuación para suavizar. <br/> ![ilustración de una portada de álbum en la que se hizo clic y, a continuación, se seleccionó ](images/vis-animations-image26.png)<br/> En Zune, las portadas del álbum parpadean al hacer clic y, a continuación, obtienen un rectángulo de selección en la selección.<br/>                                                                                                                                                                                                                                                                      |
| **Comentarios de progreso**<br/> para mostrar que se está realizando una tarea. <br/>                             | Los comentarios de progreso indican que una tarea está progresando, normalmente con indicadores de actividad, barras de progreso o animaciones que ilustran la tarea. Los comentarios sobre el progreso determinado muestran aproximadamente cuánto de la tarea se ha realizado y cuánto queda, mientras que el progreso indeterminado solo indica que la tarea se está haciendo.<br/> vocabulario de windows: indicadores de actividad de giro, barras de progreso, fondos de progreso, animaciones de ilustración. <br/> ![captura de pantalla del cuadro de diálogo con texto de "inicio de sesión" ](images/vis-animations-image27.png)<br/> En este ejemplo, Windows Live Messenger muestra comentarios de progreso indeterminados durante el inicio de sesión.<br/> |
| **Atractor**<br/> para mostrar que algo necesita la atención del usuario. <br/>                          | Atraer el nivel adecuado de atención cuando se crean objetos significativos o se necesita atención (a menudo debido a cambios) o se suceden eventos importantes o urgentes. vea [atrayendo el nivel adecuado de atención para](#attracting-the-right-level-of-attention) las técnicas de diseño.<br/> vocabulario de windows: flashing, moving, pulsing, glowing, gleam. <br/> ![captura de pantalla que muestra la animación de la barra de herramientas ](images/vis-animations-image28.png)<br/> La Windows live se anima en la primera apariencia para que sea obvio dónde está.<br/>                                                                                                                                 |
| **Relación**<br/> para mostrar la relación entre objetos o causalidad en los efectos. <br/>        | Mostrar relaciones, especialmente cuando es posible que la relación no se entienda o se espera, de forma que no distraiga ni confusa.<br/> vocabulario de windows: transformación, transporte, cambio físico, como voltear, crecer desde un origen de punto, reducir a un destino de punto. <br/> ![captura de pantalla del cuadro de diálogo calibración de color](images/vis-animations-image29.png)<br/> En este ejemplo, la animación muestra la relación entre la configuración gamma y su efecto en la pantalla.<br/>                                                                                                                                                    |
| **Ilustración/vista previa**<br/> para explicar visualmente un concepto, una tarea o el efecto de un comando. <br/> | Animación o vídeo que explica un concepto o cómo funciona visualmente algo, ya sea para complementar o reemplazar una explicación textual. Esto permite a los usuarios realizar tareas o elegir comandos de forma eficaz y segura. <br/> ![captura de pantalla del lápiz que corrige un error ortográfico ](images/vis-animations-image30.png)<br/> En este ejemplo, los comandos "mostrarme" del Panel de entrada de Tablet PC usan ilustraciones para mostrar cómo corregir, eliminar, dividir y unir.<br/>                                                                                                                                                                                                        |



 

Las transiciones tienen varios patrones de uso:



|      Uso                                                                                                                                                                                                      |    Descripción                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aumento, reducción o aparición de objetos**<br/> para cambiar el tamaño o el estado de un objeto sin problemas. <br/>                                                                                                         | Los objetos cambian entre estados, posiblemente mientras se mueven. la transición mantiene a los usuarios orientados durante los cambios.<br/> vocabulario de windows: morph, change size, object slides in or out. <br/> ![captura de pantalla de tres tamaños de meteorológicos ](images/vis-animations-image31.png)<br/> En este ejemplo, Weather Weather Weather Se transforma a partir de su estado conciso para mostrar su cuadro de diálogo Opciones.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Presentación, ocultación y cambio de contenido**<br/> para mostrar, ocultar o cambiar el contenido sin problemas, normalmente para la divulgación progresiva. <br/>                                                                       | El interior de la ventana cambia de forma para mostrar más, menos o contenido diferente. la transición mantiene a los usuarios orientados durante los cambios.<br/> vocabulario de windows: el panel se desliza dentro o fuera. las ventanas de control de control se atenuan hacia dentro y hacia fuera. el contenido diferente se atenua o se enrolla. <br/> ![captura de pantalla de tres tamaños de calculadora ](images/vis-animations-image32.png)<br/> La Windows de vista tiene una transición fluida entre los modos de vista.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Control u presentación u ocultación de la asequibilidad**<br/> para mostrar u ocultar sin problemas los controles o sus asequiciones al mantener el mouse o moverse con el mouse para simplificar la apariencia visual normal. <br/>                | Muestra controles cuando los usuarios mantienen el puntero sobre un área de comandos o muestran las asequibilidades cuando los usuarios mantienen el puntero sobre un control. mantener el puntero sobre estas áreas indica que el usuario pretende interactuar. Las asequibilidades pueden ocultarse si el puntero se vuelve indeseario. <br/> ![captura de pantalla de los controles atenuados antes de mantener el puntero ](images/vis-animations-image33.png)<br/> En este ejemplo, los controles de Reproductor de Windows Media se atenuan al mantener el mouse en el modo de pantalla completa.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Transiciones de escena**<br/> para que una transición de escena sea fluida y sin problemas con el fin de evitar la atención. <br/>                                                                                   | Los cambios bruscos en la escena pueden ser jarring, especialmente para áreas de pantalla grandes, por lo que puede usar transiciones de escena para crear subilidad y continuidad, y para proporcionar contexto. Las transiciones de escena están diseñadas para ser de clave natural y baja, con el fin de evitar llamar la atención sobre el proceso de transición.<br/> vocabulario de windows: atenuación de entrada y salida; atenuación cruzada; deslizar hacia dentro/izquierda, hacia fuera/derecha, hacia arriba, hacia abajo; inserciones y coberturas. <br/> ![captura de pantalla de una foto que se convierte en otra ](images/vis-animations-image34.png)<br/> En este ejemplo, el fondo Windows escritorio se cruza perfectamente entre las imágenes para que la transición sea fluida y controlada.<br/>                                                                                                                                                                                                                                                                                                                               |
| **Transiciones de escena especiales**<br/> para llamar la atención sobre un cambio de escena para que sea especial o reenfoque la atención del usuario. <br/>                                                               | Aunque la mayoría de las transiciones de escena no deben llamar la atención sobre el proceso de transición, algunas están diseñadas para interrumpir el flujo y llamar la atención con el fin de resaltar que algo diferente está a punto de ocurrir. para llamar la atención, las transiciones de escena especiales están diseñadas para que no sean naturales y tengan un gran impacto visual. <br/> ![captura de pantalla de la diapositiva de transición que llama la atención ](images/vis-animations-image35.png)<br/> En este ejemplo, PowerPoint transiciones de atención para atraer a la audiencia al cambio.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Manipulaciones directas**<br/> para mostrar el efecto de las manipulaciones directas (como mover, desplazar/desplazar, girar y zoom). <br/>                                                                   | La transición muestra el efecto de la manipulación en tiempo real. el efecto debe ser suave, continuo y coherente con el mundo real. es posible que el movimiento y la rotación no sean continuos en algunos lugares para indicar restricciones o posibles opciones preferidas. el zoom hace que el contenido sea mayor o menor, posiblemente cambiando el nivel de detalle en consecuencia. <br/> ![captura de pantalla de tres tamaños de lupa ](images/vis-animations-image36.png)<br/> En este ejemplo, lupa se acerca sin problemas entre niveles.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Manipulaciones directas incorrectas**<br/> para indicar que se intentó realizar una manipulación directa (como mover, desplazarse o desplazarse) pero no se pudo realizar. <br/>                                           | La transición muestra la manipulación que se está intentando, pero vuelve al estado original. a menudo, el efecto parece que la manipulación no se puede realizar debido a alguna restricción física real. estas animaciones se usan en lugar de mensajes de error basados en texto, lo que interrumpiría la sensación real de la manipulación.<br/> vocabulario de windows: bounce <br/> ![figura de animación que se comunica visualmente ](images/vis-animations-image4.png)<br/> En este ejemplo, el documento se recupera para mostrar que el usuario ha llegado al final.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Ordenación, filtrado y reordenación de transiciones**<br/> para indicar que la presentación o el contenido de una colección de elementos ha cambiado. <br/>                                                            | La transición muestra (o para cambios complejos, sugiere) el efecto del cambio. <br/> ![captura de pantalla de las cámaras de filas con tres quitadas ](images/vis-animations-image37.png)<br/> ![captura de pantalla similar con diferentes cámaras quitadas ](images/vis-animations-image38.png)<br/> ![captura de pantalla similar con otras cámaras quitadas ](images/vis-animations-image39.png)<br/> en este ejemplo, Bing Visual Search usa una transición de filtro.<br/> ![captura de pantalla de la portada del álbum cambiando su apariencia ](images/vis-animations-image40.png)<br/> En este ejemplo, Windows Media Center usa una transición de reordenación como una experiencia especial mientras se reproduce una canción.<br/>                                                                                                                                                                                                                                                                                   |
| **Transiciones de rendimiento**<br/> para que una acción parezca que se realiza con mayor rapidez. <br/>                                                                                                              | Aunque cualquier transición tiene la posibilidad de que una acción parezca que se realiza con mayor rapidez, el propósito principal de estas transiciones es mejorar la percepción del rendimiento y la capacidad de respuesta. una buena técnica es mostrar la tarea que se realiza en pasos deliberadamente. por el contrario, retrasar la acción, representar los resultados de forma haphazard o usar un indicador de actividad se verá lento.<br/> vocabulario de windows: realizar acciones en fases, con transiciones fluidas entre las fases. <br/> ![captura de pantalla de la lista de saltos que agrega destinos ](images/vis-animations-image41.png)<br/> En este ejemplo, una barra de Lista de accesos directos muestra inmediatamente los elementos estándar y, a continuación, se desliza para mostrar los destinos una vez que la lista está lista. Si lo hace, se acumula el tiempo necesario para compilar la lista. Por el contrario, retrasar la presentación inicial no respondería y mostrar una lista incompleta o comentarios de progreso sería mucho más lento.<br/> |
| **Experiencias especiales**<br/> para atraer y complacer a [](glossary.md) los usuarios durante experiencias especiales poco frecuentes que son importantes para el programa y que tienen toda la atención del usuario. <br/>    | Aunque cualquier transición tiene la posibilidad de ser una experiencia especial, estas transiciones se reservan mejor para experiencias poco frecuentes que son realmente especiales para el programa. las transiciones personalizadas se usan para dar una sensación especial. la personalidad y la personalidad suelen ser elementos de diseño importantes. A diferencia de otros patrones, las experiencias especiales pueden requerir atención, ser pesadas y requerir que los usuarios esperen un momento. Por lo tanto, estas transiciones se desasocian rápidamente si se usan en exceso porque la experiencia ya no es especial. <br/> ![captura de pantalla del logotipo de Windows cambiando a nueva pantalla ](images/vis-animations-image42.png)<br/> En este ejemplo, Windows Media Center muestra una animación mientras se carga para atraer inmediatamente a los usuarios.<br/>                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a>Directrices

### <a name="effective-communication"></a>Comunicación eficaz

-   **Defina y use un vocabulario de animación** para asegurarse de que las animaciones y transiciones tienen un significado coherente y usarlo de forma coherente en todo el programa. La mayoría de los vocabularios deben incluir entradas para la escena y la apariencia y el abandono de objetos, navegación, interacción básica (mantener el puntero, seleccionar, hacer clic), manipulación e interacción de objetos (movimiento, colocación, cambio de tamaño, desplazamiento, movimiento panorámico, zoom, rotación, filtrado) y atraer la atención. El significado coherente es fundamental para una comunicación eficaz.
-   **Siempre que sea práctico, use el vocabulario Windows animación.** Aunque el programa puede tener un público diferente y necesidades diferentes, a menudo las ventajas de coherencia y familiaridad superan las ventajas de ser diferentes. Si el vocabulario del programa debe ser diferente, use los mismos tipos de animación básicos que Windows, pero déles la personalidad adecuada para el programa.
-   **No asigne significados específicos a animaciones genéricas y transiciones en un vocabulario de animación.** Las transiciones genéricas, como atenuaciones y efectos especiales como las disminsiones, no tienen ningún significado concreto (más allá de que aparezcan o desaparezcan), por lo que se pueden usar libremente.

    **Incorrecto:**

    ![captura de pantalla de un cuadro de diálogo que se convierte en otro ](images/vis-animations-image43.png)

    En este ejemplo, se usa incorrectamente una atenuación cruzada para ir al elemento siguiente. Dado que las atenuaciones cruzadas no tienen ningún significado concreto, esta transición no proporciona contexto.

-   **Hacer que las entradas de vocabulario se distinguien claramente.** Las acciones relacionadas pueden tener efectos similares (por ejemplo, acercar y alejar deben tener transiciones inversas), pero las acciones no relacionadas deben tener efectos claramente distintos (por ejemplo, el zoom nunca debe confundirse con la rotación).
-   **Mantener los efectos reales realistas y coherentes.** Si usa animaciones y transiciones realistas, mantenga la experiencia coherente con el mundo real. Los resultados nunca deben confundir, confundir ni confundir a los usuarios. Y por coherencia, no mezcle metáforas.
-   **Proporcionar animaciones inversas de acciones inversas.** Al hacerlo, se cumplen las expectativas del usuario y se simplifica el vocabulario. Por ejemplo, si aparece un panel deslizándose hacia dentro, quítelo deslizándose hacia fuera no con algún otro efecto.
-   **Hacer que las animaciones sea comprensibles.** Los usuarios deben ser capaces de comprender rápidamente el propósito de una animación. Es posible hacer que una animación sea demasiado pequeña, demasiado breve (menos de 50 milisegundos) o tan sutil que los usuarios no puedan comprender su propósito. En tales casos, rediseñar para que el significado sea claro o quitar.

    **Incorrecto:**

    ![captura de pantalla de animación al eliminar el cuadro de diálogo ](images/vis-animations-image44.png)

    En este ejemplo, el efecto es tan pequeño y sutil que pocos usuarios pueden comprender su propósito. Es mejor rediseñar o quitar.

### <a name="patterns"></a>Patrones

**Comentarios al mantener el mouse**

-   **Para que aparezca con capacidad de respuesta, esfuércese por reproducir la animación en un plazo de 50 milisegundos después de entrar o salir del estado de mantener el puntero.**
-   **Para que parezca rápido, haga que la duración de las animaciones de mantener el mouse sea inferior a 50 milisegundos.**
-   **Use un efecto de atenuación de entrada/atenuación fuera del efecto de mantener el puntero.** Si lo hace, los efectos de mantener el mouse son claramente distintos de los comentarios de clic y selección.

**Comentarios de clic**

-   **Para que aparezca con capacidad de respuesta, esfuércese por reproducir la animación en un plazo de 50 milisegundos después de hacer clic en el evento.** No es necesario hacer clic en los eventos para hacer clic en ellos.
-   **Para que parezca rápido, haga que la duración de las animaciones de clic sea inferior a 50 milisegundos.**
-   **Use un flash de fondo o un efecto de parpadeo.** Al hacerlo, los efectos de clic son claramente distintos de los comentarios de selección y de mantener el puntero. Dado que hacer clic requiere mantener el mouse, haga que los comentarios de clics se adicien sin problemas a los comentarios.

**Comentarios de selección**

-   **Para que aparezca con capacidad de respuesta, esfuércese por reproducir la animación en 50 milisegundos de selección o deselección.**
-   **Para que parezca rápido, haga que la duración de las animaciones de selección sea inferior a 50 milisegundos.**
-   **Use un efecto de rectángulo de selección de atenuación o atenuación.** Al hacerlo, la selección es claramente distinta de los comentarios de mantener el puntero y hacer clic.

**Comentarios sobre el progreso**

-   **Use un indicador de actividad cuando no se pueda realizar una acción en un segundo.** Esto indica que se ha recibido el comando.
-   **Use una barra de progreso cuando una tarea tarde más de cinco segundos.** Para obtener más instrucciones, vea [Barras de progreso](progress-bars.md).
-   **Use animaciones de comentarios de progreso que ayuden a los usuarios a visualizar el efecto de las tareas de ejecución larga.** Evite animaciones de comentarios de progreso innecesarias si una animación no comunica nada útil, use en su lugar una barra de progreso.
-   **Tener estados de finalización y error claramente identificables.** Los usuarios deben poder determinar estos estados finales rápidamente.
-   **Deje de mostrar el progreso cuando la tarea subyacente no esté progresando.** Los usuarios deben ser capaces de determinar si no se está haciendo el progreso y reaccionar en consecuencia.

**Atractores**

-   **Use los atraigadores con moderación.** A menos que la información sea urgente, crítica o que afecte al comportamiento inmediato del usuario, normalmente es mejor cambiar el estado de forma discreta y permitir que los usuarios detecten el cambio por sí mismos. [Resolver distracciones, no detectabilidad.](/windows/desktop/uxguide/how-to-design-desktop-ux)

    ![captura de pantalla de iconos de estado inalámbrico ](images/vis-animations-image45.png)

    En este ejemplo, el icono del área de notificación de red inalámbrica usa una animación para problemas críticos, pero permite a los usuarios detectar señales débiles por sí mismos.

-   **Elija una animación que dibuje el nivel de atención adecuado.** Las animaciones de los atraigadores deben llamar la atención suficiente para cumplir su propósito, pero ya no. Si el usuario debe actuar inmediatamente, elija un efecto que exija atención independientemente de dónde esté mirando el usuario. Para otras situaciones, consulte la sección [Atraer](#attracting-the-right-level-of-attention) el nivel de atención adecuado para obtener la combinación adecuada de atención, capacidad de aviso y urgencia.

    **Incorrecto:**

    ![captura de pantalla del asistente de la oficina de clips de papel ](images/vis-animations-image46.png)

    Los Microsoft Office asistentes de carga se incumplen por sí mismos.

-   **Si el usuario no responde, no repita la animación ni use animaciones continuas.** En su lugar, suponga que el usuario decidió no actuar ahora, pero puede actuar más adelante. Las animaciones continuas dificultan a los usuarios concentrarse en cualquier otra cosa.

**Animaciones de relaciones**

-   **Use animaciones de relación para mostrar dónde han llegado los objetos o dónde han ido.**
-   **Las animaciones de relación deben iniciarse o terminar con el objeto seleccionado.** No muestre las relaciones entre objetos con los que el usuario no interactúa actualmente. Si los usuarios lo observan, lo que observarán es la distracción.

**Ilustraciones y vistas previas**

-   **Use las versiones preliminares para mostrar el efecto de un comando sin que los usuarios tengan que realizarlo primero.** Mediante el uso de vistas previas útiles, puede mejorar la eficacia y la facilidad de aprendizaje del programa y reducir la necesidad de prueba y error.
-   **Use ilustraciones y vistas previas que tengan una interpretación clara.** Tienen poco valor si son confusos.
-   **Reproducir solo una ilustración a la vez para** evitar usuarios abrumadores. Si son posibles varias ilustraciones simultáneas, use el mouse o un botón de reproducción para permitir que los usuarios indiquen su interés.
-   **Reproducir una ilustración automáticamente si es el propósito principal de la ventana o página.** De lo contrario, si es opcional, permita a los usuarios reproducirlo cuando estén listos.
-   **Reproducir animaciones a la velocidad** óptima: no tan rápidas son difíciles de entender, pero no tan lentas que son tediosas de ver.

**Aumento o reducción de objetos**

-   **No recorte el contenido durante un cambio de tamaño.** Expanda los contenedores antes de agregar contenido. Quite el contenido antes de reducir los contenedores.

    **Incorrecto:**

    ![captura de pantalla de la calculadora truncada ](images/vis-animations-image47.png)

    En este ejemplo, el contenido se recorta durante un cambio de tamaño.

**Presentación, ocultación y cambio de contenido**

-   **Mostrar información importante estáticamente.** Los usuarios no deben tener que acceder a información importante a través de la divulgación progresiva.

**Control u presentación u ocultación de la asequibilidad**

-   **Muestra controles importantes cuando el usuario coloca el puntero en cualquier lugar dentro de la ventana o el panel, o, si se muestra a pantalla completa, al mover el mouse.** Los usuarios no deben tener que buscar estos controles, así que asegúrese de su detección.

    ![ilustración en la que se muestra cómo se muestra el puntero de los controles ](images/vis-animations-image48.png)

    En este ejemplo, Windows Media Center muestra sus controles cada vez que el puntero está sobre la ventana.

-   **Muestra los controles secundarios o las asequibilidades de control cuando el usuario coloca el puntero en los comandos o cerca de él.** Para facilitar la detectabilidad, haga que la ubicación sea obvia y el destino sea grande.

    ![captura de pantalla del puntero que revela el comando secundario ](images/vis-animations-image49.png)

    En este ejemplo, Windows Live Messenger muestra un comando secundario cuando el puntero está cerca de la esquina superior derecha.

**Transiciones de escena**

-   **Hacer que las transiciones de escena física sean coherentes con la asignación natural.** Las personas leen de izquierda a derecha en las culturas occidental y los diagramas jerárquicos fluyen de arriba abajo. Por lo tanto, el desplazamiento de izquierda a derecha indica el avance en el tiempo. Las siguientes transiciones de escena física tienen asignación natural:



    | Transición                          | Significado                                     |
    |---------------------------|--------------------------------------|
    | Desde la izquierda<br/>      | Volver al flujo de tareas<br/>    |
    | Desde la derecha<br/>     | Avanzar en el flujo de tareas<br/> |
    | Desde arriba<br/>       | Subir jerarquía de tareas<br/>    |
    | Desde abajo<br/>    | Bajar jerarquía de tareas<br/>  |



 

-   **Si el programa reproduce sonido, diseñe las transiciones de escena y las transiciones de audio juntas.** Por ejemplo, si una escena se atenua gradualmente, cualquier sonido también debe atenuarse gradualmente. No interrumpa las transiciones visuales sin problemas al tener transiciones de sonido repentinas. Para obtener más instrucciones de sonido, vea [Sonido](vis-sound.md).

**Manipulaciones directas**

-   **Cuando se usan gestos físicos en la interacción (como el movimiento), diseñe la animación para que se sienta como una respuesta natural al gesto.** Vincule la causa de interacción con el efecto de transición. Proporcionar a la animación características físicas reales, como aceleración, deceleración, impulso, resistencia, peso, salto y rotación.
-   **Para mantener una sensación directa, mantenga los puntos de contacto de un objeto bajo el puntero sin problemas a lo largo de la interacción.** Cualquier retraso, respuesta desmeso o pérdida de contacto destruye la percepción de manipulación directa. Los objetos nunca deben desaparecer mientras se manipulan.

**Ordenación, filtrado o reordenación de transiciones**

-   **Para realizar cambios sencillos, muestre toda la transición.** Los usuarios podrán seguir toda la transición fácilmente. Los cambios simples implican cuatro elementos o menos.
-   **En el caso de cambios complejos, haga hincapié en el final del movimiento a medida que se ralentiza y deje que el ojo se rellene el resto.** Esto hace que el movimiento se sienta mucho más dinámico y orden.

**Transiciones de rendimiento**

-   **Considere la posibilidad de realizar transiciones lentas en dos o tres fases para que parezcan más rápidas e interactivas inmediatamente.** Use el orden de composición siguiente cuando corresponda:
    -   Marco externo
    -   Información previa
    -   Contenido inicial (mediante una representación temporal si es necesario)
    -   Controles principales (para que los usuarios puedan interactuar inmediatamente)
    -   Controles secundarios y los elementos de interfaz de usuario restantes
    -   Contenido final (si se usó una representación temporal) Use transiciones como atenuaciones y diapositivas para que la composición parezca suave, ordenada y refinada.

![captura de pantalla del mapa con foto satélite y cuadrícula ](images/vis-animations-image50.png)

Al desplazarse en la vista "Ojo de ave", los mapas Bing muestran un fondo de cuadrícula temporal. Esto permite a los usuarios continuar desplazando inmediatamente, justo antes de que se represente el contenido final.

**Animaciones de experiencia especial**

-   **Pantallas de presentación animadas Desencapso ( así como pantallas de presentación estáticas).** A menudo, las pantallas de presentación simplemente hacen que se preste atención al tiempo que tarda un programa en cargarse y se desenlazan rápidamente. Aunque las pantallas de presentación son aceptables si solo se muestran cuando no es posible la interacción del usuario, siempre que sea práctica una alternativa mejor es diseñar el programa para que los usuarios puedan interactuar con él inmediatamente, incluso mientras se sigue cargando.
-   **Proporcione un comando Omitir introducción si una pantalla de presentación animada tarda más de tres segundos.** Al hacer clic en cualquier parte de la pantalla de presentación, también se debe descartar. Como alternativa, use una versión corta de la animación después de un período inicial.

### <a name="performance"></a>Rendimiento

-   **No haga que los usuarios esperen a las animaciones y transiciones del programa.** Use animaciones y transiciones breves (menos de 200 milisegundos) siempre que sea práctico. Use animaciones más rápidas (100 milisegundos) para operaciones más frecuentes. Diseñe animaciones más largas (más de un segundo normalmente los comentarios sobre el progreso, la ilustración y los patrones de experiencia especiales) para que los usuarios puedan seguir trabajando mientras se ejecutan.
-   **Diseñe animaciones de larga duración para dejar claro a los usuarios que pueden interactuar mientras se ejecuta la animación.** Los usuarios no intentarán seguir trabajando si las pistas visuales sugieren que no pueden hacerlo.

    ![captura de pantalla de una barra de progreso en una barra de estado ](images/vis-animations-image51.png)

    En este ejemplo de Windows Internet Explorer, la barra de progreso de clave baja de la barra de estado sugiere que los usuarios no tienen que esperar a la finalización para poder interactuar.

-   **Use animaciones ligeras para tareas que consumen mucha CPU.** Al hacerlo, se proporciona una capacidad de procesamiento completa a la tarea. Además, los usuarios no percibirán que la animación ligera es la razón por la que la tarea consume mucha CPU.
-   **No muestre un indicador de actividad durante una animación o transición.** Si lo hace, se destruye el efecto. Diseñe animaciones y transiciones para que puedan empezar de inmediato.
-   **Diseñe animaciones para degradar correctamente siempre que no haya recursos del sistema insuficientes.** Las animaciones pueden degradarse si tienen variaciones que requieren menos recursos (por ejemplo, longitudes más cortas o velocidades de fotogramas más bajas) o incluso no se ejecutan en absoluto. Independientemente de los recursos disponibles, asegúrese de que las animaciones tienen alta calidad y se parecen a animaciones en lugar de errores de software.

    **Incorrecto:**

    ![captura de pantalla del marco de programa atenuado sobre el escritorio ](images/vis-animations-image52.png)

    En este ejemplo, se usa la transición de restauración de ventana aunque no haya suficientes recursos del sistema para reproducirla bien. Por lo tanto, el marco inmovilizado parece ser un error. Si los recursos no están disponibles, es mejor simplemente mostrar la ventana sin una transición.

### <a name="animation-characteristics"></a>Características de animación

Las animaciones y transiciones bien diseñadas suelen tener estas características:

-   **Breve duración.** La mayoría de las animaciones deben estar entre 100 y 300 milisegundos, preferiblemente 1/6 segundos (167 milisegundos) o 1/4 segundos (250 milisegundos). (Las experiencias especiales y los comentarios sobre el progreso pueden ser más largos). Use tiempos de animación más rápidos para operaciones más frecuentes. Por lo general, las animaciones más largas tardan más tiempo en completarse, tardan más tiempo en comprenderse y se ralentizan.
-   **Respuesta.** Las animaciones deben iniciarse en un plazo de 50 milisegundos desde el evento de inicio o la acción del usuario. Las horas de inicio más largas no tienen respuesta.
-   **Aceleración/deceleración.** Para que parezca natural, la mayoría de los efectos de animación deben acelerarse al iniciarse y ralentizarse al detenerse. Para tener un aspecto dinámico, diseñe animaciones para que tengan inicios rápidos. Para que aparezca controlado, diseñe animaciones para que tengan aterrizajes flexibles al final. Aunque esto se aplica a los efectos de movimiento, también se aplica a cualquier efecto que sugiera movimiento, como zooms e incluso atenuaciones.

    ![figura de un gráfico que muestra una velocidad reducida a lo largo del tiempo ](images/vis-animations-image53.png)

    La mayoría de las animaciones deben tener inicios rápidos y finales flexibles para tener una sensación de capacidad de respuesta, pero controlada.

-   **Movimiento.** Las animaciones que representan el movimiento en particular necesitan acelerarse y ralentizarse, por lo que no use el movimiento lineal a menos que la duración de la animación sea muy corta. Los movimientos deben tomar la ruta de acceso de los cortos de principio a fin, sin sobreshooting. La ruta de movimiento completa no siempre es necesaria. Cuando sea necesario, haga hincapié en el final del movimiento a medida que se ralentiza y deje que el ojo se rellene el resto. Esto hace que el movimiento se sienta mucho más dinámico y orden. Al animar el movimiento de varios objetos simultáneamente, déles rutas ligeramente diferentes con intervalos ligeramente diferentes para que se sientan más naturales.
-   **Velocidad de fotogramas.** La mayoría de las animaciones deben usar una velocidad de fotogramas de 20 fotogramas por segundo. Si la animación es para una experiencia especial o está relacionada con el propósito principal del programa, considere la posibilidad de usar una velocidad mayor de 24 30 fotogramas por segundo para mejorar la subilidad y el realismo.
-   **Escala.** Diseñe animaciones para que funcionen bien en toda su gama de uso previsto. Por ejemplo, las transiciones de página deben diseñarse para que funcionen para todos los tamaños de página.
-   **Personalidad.** Diseñe animaciones para que se sientan naturales, subdesdues y eficaces en lugar de artificiales, silbidos o lentos.

### <a name="animated-text"></a>Texto animado

-   Aunque puede mostrar texto mediante una transición, **no animar texto continuamente.** El texto animado suele distraer y es más difícil de leer que el texto estático. **Excepciones:**
    -   Puede animar texto en situaciones en las que tradicionalmente se anima y proporcionar una alternativa accesible.
    -   Puede animar texto si el propósito del texto es principalmente la decoración.

![captura de pantalla de la interfaz zune diseñada de forma creadora ](images/vis-animations-image13.png)

En este ejemplo, Zune el texto, pero su propósito es principalmente la decoración. No hay ningún problema si los usuarios no leen cuidadosamente el texto.

### <a name="reducing-power-consumption"></a>Reducción del consumo de energía

-   **Diseñe las animaciones para reducir el consumo de energía.** Cuando se diseñan correctamente, las animaciones no deben aumentar significativamente el consumo de energía. Para reducir el consumo de energía:
    -   **Deje de animar cuando la pantalla esté desactivada.** La pantalla puede estar desactivada con el fin de ahorrar energía.
    -   **No use animaciones de ejecución larga que no se inicien por el usuario.** Las animaciones que usan temporizadores periódicos de alta resolución reducen la eficacia de la administración de energía del procesador. Además, asegúrese de deshabilitar los temporizadores periódicos de alta resolución cuando se completen las animaciones.
    -   **Suspenda todas las animaciones cuando el sistema esté inactivo.** El período de inactividad del usuario para que se vuelva inactivo viene determinado por Opciones de energía en Panel de control.

### <a name="accessibility"></a>Accesibilidad

-   **No use la animación como única manera de transmitir información esencial.** Las animaciones deben comunicar información útil, pero no crítica, porque no son accesibles para los usuarios con discapacidades visuales.
-   **Asegúrese de que la información equivalente esté disponible a través de otros medios,** como:

    -   **Mediante inspección.** Los usuarios pueden determinar información equivalente si observan la pantalla u objetos implicados en la animación.
    -   **Por interacción simple.** Los usuarios pueden determinar la información equivalente si mantienen el puntero, se hace clic o se hace doble clic.

    ![captura de pantalla de la página principal de Bing con zonas de acceso ](images/vis-animations-image54.png)

    La Bing principal tiene una animación inicial que revela varias zonas de acceso. Los usuarios también pueden mostrar las zonas de acceso rápido moviendo el cursor cerca de ellas.

    Tenga en cuenta que "información equivalente" no significa información idéntica. La información puede estar en un formato diferente o requerir una deducción simple.

-   **Cuando corresponda, establezca el foco de entrada en el objeto cambiado durante una transición.** Esto permite que las tecnologías de asistencia detecten dónde se produjo el cambio. Pero no cambie el foco de entrada cuando el usuario use el teclado.
-   **No use animaciones ni transiciones que parpadee o cambie el tamaño de los objetos rápidamente.** El flashing y los cambios rápidos en la pantalla pueden causar problemas a las personas con discapacidades graves y otros síntomas.
-   **Permitir a los usuarios desactivar las animaciones y transiciones del programa.** Para admitir esta capacidad, respeta la opción Desactivar todas las animaciones innecesarias en la Centro de accesibilidad en Windows.

    **Desarrolladores:** Puede determinar si las animaciones están habilitadas mediante la API SystemParametersInfo.

-   **Tareas de diseño suponiendo que los usuarios desactivarán las animaciones del programa.** Asegúrese de que esto no interrumpe significativamente el flujo de tareas.

Para obtener más instrucciones de accesibilidad, vea [Accesibilidad.](inter-accessibility.md)

## <a name="documentation"></a>Documentación

-   Evite hacer referencia a animaciones siempre que sea posible. En su lugar, haga referencia al objeto que se anima y, si es necesario, al tipo de animación.
-   No haga referencia a las transiciones, excepto en la documentación técnica. En su lugar, haga referencia al objeto en su estado final o inicial.
-   Si el usuario inicia explícitamente una animación, use el verbo play; de lo contrario, use el verbo use para la documentación técnica.

Ejemplos:

-   Sabrá que un elemento necesita su atención cuando su icono empiece a saltar.
-   En primer lugar, seleccione las fotos que desea imprimir (tenga en cuenta que las fotos se amplían tras la selección).
-   Use una transición de atenuación cruzada para cambiar el estado de un objeto sin problemas.

