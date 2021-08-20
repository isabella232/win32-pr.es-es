---
title: Tocar
description: Todas las aplicaciones Windows microsoft deben tener una experiencia táctil excelente. Y crear esta experiencia es más fácil de lo que cree.
ms.assetid: a87d0726-1c57-4cf8-9e35-4e73a09ff1a3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 68f73b7da9cf33dc20a3c0534044558e514284f024f11609ef9af4760ec79a8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119029758"
---
# <a name="touch"></a>Tocar

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Todas las aplicaciones Windows microsoft deben tener una experiencia táctil excelente. Y crear esta experiencia es más fácil de lo que cree.

El toque hace referencia al uso de uno o varios dedos para proporcionar entrada a través de una pantalla de dispositivo e interactuar con Windows y aplicaciones. Una aplicación con optimización táctil tiene una interfaz de usuario y un modelo de interacción diseñados para dar cabida a las áreas de contacto más grandes y menos precisas del contacto, los distintos factores de forma de los dispositivos táctiles y las numerosas posturas y controles que los usuarios pueden adoptar al usar un dispositivo táctil.

![Interacción del usuario con tabletas mediante el uso táctil](images/inter_touch_image1.jpeg)

Cada dispositivo de entrada tiene sus puntos fuertes. El teclado es mejor para la entrada de texto y para proporcionar comandos con un movimiento mínimo de la mano. El mouse es mejor para apuntar de forma eficaz y precisa. El toque es mejor para la manipulación de objetos y para proporcionar comandos simples. Un lápiz es mejor para la expresión de forma libre, como con la escritura a mano y el dibujo.

Windows 8.1 está optimizado para la capacidad de respuesta, la precisión y la facilidad de uso con la entrada táctil, al tiempo que admite totalmente los métodos de entrada tradicionales (como mouse, lápiz y teclado). La velocidad, la precisión y los comentarios táctiles que proporcionan los modos de entrada tradicionales son familiares y atractivas para muchos usuarios y pueden ser más adecuados para escenarios de interacción específicos.

Puede encontrar instrucciones relacionadas con el mouse, el lápiz y la accesibilidad en temas independientes.

Cuando piense en la experiencia de interacción de la aplicación:

No suponga que si una interfaz de usuario funciona bien para un mouse, también funciona bien para la función táctil. Aunque una buena compatibilidad con el mouse es un inicio, una buena experiencia táctil tiene algunos requisitos adicionales.

Supongamos que si una interfaz de usuario funciona bien con un dedo, también funciona bien para un lápiz. Hacer que la aplicación se puede tocar es un largo camino para proporcionar también una buena compatibilidad con lápiz. La diferencia principal es que los dedos tienen una propina de un sistema de aseador, por lo que necesitan objetivos más grandes.

Con el toque, puede manipular objetos y la interfaz de usuario directamente, lo que hace que la experiencia sea más rápida, natural y atractiva.

## <a name="provide-a-great-touch-experience"></a>Proporcionar una experiencia táctil excelente

Debe asegurarse de que los usuarios pueden realizar tareas críticas e importantes de forma eficaz mediante la entrada táctil. Sin embargo, es posible que una funcionalidad específica de la aplicación, como la manipulación de texto o píxeles, no sea adecuada para la función táctil y se pueda reservar para el dispositivo de entrada más adecuado.

Si no tiene mucha experiencia en el desarrollo de aplicaciones táctiles, es mejor aprender haciendo esto. Obtenga un equipo táctil, coloque el mouse y el teclado a un lado y use solo los dedos para interactuar con la aplicación. Si tiene una tableta, experimente con mantenerla en distintas posiciones, como en el regón, en una mesa o en los brazos mientras está de pie. Pruebe a usarlo en orientación vertical y horizontal.

Las aplicaciones optimizadas para tocar que funcionan mejor con la interacción táctil suelen ser:

-   **Natural e intuitivo.** Las interacciones están diseñadas para corresponder a cómo interactúan los usuarios con objetos en el mundo real.
-   **Menos intrusivo.** El uso de la función táctil es silencioso y, por tanto, es mucho menos distraer que escribir o hacer clic.
-   **Portátil.** Los dispositivos táctiles son más compactos porque muchas tareas se pueden completar sin teclado, mouse, lápiz o touchpad. También son más flexibles porque no se requiere una superficie de trabajo.
-   **Directa e interesante.** La función táctil te hace sentir que estás manipulando directamente objetos en la pantalla.
-   **Menos preciso.** Los usuarios no pueden tener como destino objetos con la precisión táctil, en comparación con un mouse o un lápiz.

La interacción táctil proporciona una sensación natural y real de interacción. La manipulación directa y la animación completan esta impresión, al proporcionar a los objetos un movimiento y comentarios realistas y dinámicos. Por ejemplo, considere un juego de cartas. No solo es cómodo y fácil arrastrar tarjetas con un dedo, sino que la experiencia adopta una sensación atractiva en el mundo real cuando se puede arrastrar, arrastrar y girar las cartas como lo haría con una baraja física. Y cuando intenta mover una tarjeta que no se puede mover, es una mejor experiencia que la tarjeta se resalte, pero no impida el movimiento, y vuelva a ponerse en marcha cuando se libera, para indicar claramente que la acción se ha reconocido, pero no se puede realizar.

Afortunadamente, si la aplicación ya está bien diseñada, es fácil proporcionar una experiencia táctil excelente. Para ello, un programa bien diseñado:

-   **Garantiza que las tareas más** importantes se pueden realizar de forma eficaz con un dedo (al menos las tareas que no implican una gran cantidad de escritura o manipulación de píxeles detallada).
-   **Usa controles grandes para la táctil.** Los controles comunes tienen un tamaño mínimo de 23 x 23 píxeles (13 x 13 D DLL) y los controles más usados son al menos 40 x 40 píxeles (23 x 22 D DLL). Para evitar un comportamiento que no responde, los elementos de la interfaz de usuario deben tener al menos 5 píxeles (3 D DLL) de espacio entre ellos. Para otros controles, asegúrese de que tienen al menos un destino de clic de 23 x 23 píxeles (13 x 13 DLU), aunque su apariencia estática sea mucho menor. Consulte El tamaño del control estándar.
-   **Admite la entrada mouse.** Los controles interactivos tienen unas asequibilidades claras y visibles. Los objetos tienen comportamientos estándar para las interacciones estándar del mouse (clic único y doble a la izquierda, clic con el botón derecho, arrastrar y mantener el mouse).
-   **Admite la entrada de teclado.** La aplicación proporciona asignaciones de teclas de método abreviado estándar, especialmente para comandos de navegación y edición que también se pueden generar mediante gestos táctiles.
-   **Garantiza la accesibilidad.** Usa Automatización de la interfaz de usuario o Microsoft Active Accessibility (MSAA) para proporcionar acceso mediante programación a la interfaz de usuario para las tecnologías de asistencia. La aplicación responde adecuadamente a los cambios de orientación, tema, configuración regional y métricas del sistema.
-   **Elimina interacciones innecesarias.** Para evitar la pérdida de datos o el acceso al sistema, use los valores predeterminados más seguros y seguros. Si la seguridad y la seguridad no son factores, la aplicación selecciona la opción más probable o cómoda.
-   **Proporciona el equivalente táctil para mantener el puntero.** No confíe en mantener el puntero como la única manera de realizar una acción.
-   **Garantiza que los gestos sumen efecto inmediatamente.** Mantenga los puntos de contacto debajo de los dedos del usuario sin problemas a lo largo del gesto, lo que proporciona el efecto de la asignación de gestos directamente al movimiento del usuario.
-   **Usa gestos estándar siempre que sea posible.** Gestos personalizados solo para interacciones exclusivas de la aplicación.
-   **Garantiza que los comandos no deseados o destructivos se pueden invertir o corregir.** Las acciones accidentales son más probables cuando se usa la función táctil.

## <a name="guidelines-for-touch-input"></a>Directrices para la entrada táctil

Con la función táctil, Windows aplicación puede usar gestos físicos para emular la manipulación directa de elementos de la interfaz de usuario.

Tenga en cuenta estos procedimientos recomendados al diseñar la aplicación táctil:

**La capacidad de respuesta es esencial para crear experiencias táctiles que se sientan directas y atractivas.** Para que sea directo, los gestos deben tener efecto inmediatamente y los puntos de contacto de un objeto deben permanecer debajo de los dedos del usuario sin problemas a lo largo del gesto. El efecto de la entrada táctil debe asignarse directamente al movimiento del usuario, por lo que, por ejemplo, si el usuario gira los dedos 90 grados, el objeto también debe girar 90 grados. Cualquier retraso, respuesta desmesada, pérdida de contacto o resultados inexactos destruye la percepción de manipulación directa y también de calidad.

**La coherencia es esencial para crear experiencias táctiles que se sientan naturales e intuitivas.** Una vez que los usuarios aprenden un gesto estándar, esperan que ese gesto tenga el mismo efecto en todas las aplicaciones. Para evitar confusiones y frustraciones, no asigne nunca significados no estándar a los gestos estándar. En su lugar, use gestos personalizados para las interacciones únicas del programa.

A continuación, describiremos el Windows táctil, pero antes de empezar, esta es una breve lista de términos básicos de entrada táctil.

-   **Gesto**

    Un gesto es el acto físico o el movimiento realizado en el dispositivo de entrada (dedo, dedos, lápiz/lápiz, mouse, y así sucesivamente). Por ejemplo, para iniciar, activar o invocar un comando, se usa una pulsación con un solo dedo para un dispositivo táctil o táctil (equivalente a un clic izquierdo con un mouse, una pulsación con un lápiz o Entrar en un teclado).

-   **Manipulación**

    Una manipulación es la reacción inmediata en tiempo real o la respuesta que un objeto o interfaz de usuario tiene a un gesto. Por ejemplo, los gestos de deslizar y deslizar rápidamente normalmente hacen que un elemento o interfaz de usuario se mueva de alguna manera.

    El resultado final de una manipulación, cómo se manifiesta mediante el objeto en la pantalla y en la interfaz de usuario, es la interacción.

-   **Interacción**

    Las interacciones dependen de cómo se interpreta una manipulación y del comando o acción que resulta de la manipulación. Por ejemplo, los objetos se pueden mover mediante los gestos de deslizar y deslizar, pero los resultados difieren en función de si se supera un umbral de distancia. La diapositiva se puede usar para arrastrar un objeto o desplazarse por una vista, mientras que el deslizamiento se puede usar para seleccionar un elemento o mostrar una barra de aplicación.

### <a name="the-windows-touch-language"></a>El Windows táctil

Windows proporciona un conjunto conciso de interacciones táctiles que se usan en todo el sistema. Aplicar este lenguaje táctil de forma coherente hace que la aplicación se familiarice con lo que los usuarios ya conocen. Esto aumenta la confianza del usuario al facilitar el aprendizaje y el uso de la aplicación. Para más información sobre la implementación del lenguaje táctil, consulte Gestos, manipulaciones e interacciones.

**Mantenga presionado el botón para aprender.**

El gesto de mantener presionado muestra información detallada o objetos visuales de enseñanza (por ejemplo, una información sobre herramientas o un menú contextual) sin confirmar una acción o un comando. El movimiento panorámico sigue siendo posible si se inicia un gesto deslizante mientras se muestra el objeto visual.

> [!IMPORTANT]
> Puede usar mantener presionada la tecla y mantener presionada para la selección en los casos en los que está habilitado el movimiento panorámico horizontal y vertical.

 

Estado de entrada: uno o dos dedos en contacto con la pantalla.

Movimiento: sin movimiento.

Estado de salida: el último dedo hacia arriba finaliza el gesto.

Efecto: muestra más información.

![pulse \- la tecla táctil para \- \-learn.png](images/inter-touch-image2.png)

Gesto de mantener presionado.

**Al mantener el puntero**

Mantener el puntero es una interacción útil porque permite a los usuarios obtener información adicional a través de sugerencias antes de iniciar una acción. Ver estas sugerencias hace que los usuarios se sientan más seguros y reduce los errores.

Desafortunadamente, las tecnologías táctiles no admiten el desplazamiento del mouse, por lo que los usuarios no pueden mantener el puntero al usar un dedo. La solución sencilla a este problema es aprovechar al máximo el mantener el puntero, pero solo de maneras que no sean necesarias para realizar una acción. En la práctica, esto suele significar que la acción también se puede realizar haciendo clic, pero no necesariamente de la misma manera.

![Captura de pantalla que muestra un ejemplo de la interacción del mouse junto a un ejemplo de la acción de clic.](images/inter-touch-image13.png)

En este ejemplo, los usuarios pueden ver la fecha de hoy si mantienen el mouse o hace clic en ellos.

**Pulse para la acción principal.**

Al pulsar en un elemento se invoca su acción principal, por ejemplo, iniciar una aplicación o ejecutar un comando.

Estado de entrada: un dedo en contacto con la pantalla o el panel táctil y se eleva antes del umbral de tiempo para una interacción de mantener presionada y mantener presionada.

Movimiento: sin movimiento.

Estado de salida: con el dedo hacia arriba finaliza el gesto.

Efecto: inicie una aplicación o ejecute un comando.

![pulsación \- táctil \-primary.png](images/inter-touch-image3.png)

Gesto de pulsar.

**Deslizar para desplazarse**

La diapositiva se usa principalmente para las interacciones de movimiento panorámico, pero también se puede usar para mover (donde el movimiento panorámico está restringido a una dirección), dibujar o escribir. La diapositiva también se puede usar para dirigirse a elementos pequeños y empaquetados densamente limpiando (deslizando el dedo sobre objetos relacionados, como botones de radio).

Estado de entrada: uno o dos dedos en contacto con la pantalla.

Movimiento: arrastre, con los dedos adicionales restantes en la misma posición en relación entre sí.

Estado de salida: el último dedo hacia arriba finaliza el gesto.

Efecto: mueva el objeto subyacente directamente e inmediatamente a medida que se mueven los dedos. Asegúrese de mantener el punto de contacto debajo del dedo a lo largo del gesto.

![touch \-slide.png](images/inter-touch-image4.png)

Gesto de panorámica.

**Deslizar el dedo para seleccionar, comando y mover**

Al deslizar el dedo a una distancia corta, hasta la dirección de desplazamiento panorámico (donde el movimiento panorámico está restringido a una dirección), se seleccionan los objetos de una lista o cuadrícula. Muestra la barra de la aplicación con los comandos pertinentes cuando se seleccionan objetos.

Estado de entrada: uno o varios dedos tocan la pantalla.

Movimiento: arrastre una distancia corta y una elevación antes de que se produzca el umbral de distancia para una interacción de movimiento.

Estado de salida: el último dedo hacia arriba finaliza el gesto.

Efecto: se selecciona o mueve el objeto subyacente o se muestra la barra de la aplicación. Asegúrese de mantener el punto de contacto debajo del dedo a lo largo del gesto.

![d: \\ sdkenlistment \\ m \- ux design m \- \\ \- ux design images touch \- \\ \\ \-swipe.png](images/inter-touch-image5.png)

Gesto de deslizar rápidamente.

**Reducir y ampliar para hacer zoom**

Los gestos de reducir y ajustar se usan para tres tipos de interacciones: zoom óptico, cambio de tamaño y zoom semántico.

El zoom óptico ajusta el nivel de ampliación de todo el área de contenido para obtener una vista más detallada del contenido. Por el contrario, el cambio de tamaño es una técnica para ajustar el tamaño relativo de uno o varios objetos dentro de un área de contenido sin cambiar la vista al área de contenido.

El zoom semántico es una técnica táctil optimizada para presentar y navegar por datos estructurados o contenido dentro de una sola vista (como la estructura de carpetas de un equipo, una biblioteca de documentos o un álbum de fotos) sin necesidad de controles de desplazamiento panorámico, desplazamiento o vista de árbol. El zoom semántico proporciona dos vistas diferentes del mismo contenido, ya que permite ver más detalles a medida que acerca y menos detalles al alejar.

Estado de entrada: dos dedos en contacto con la pantalla al mismo tiempo.

Movimiento: los dedos se separan (se extienden) o juntos (se acercan) a lo largo de un eje.

Estado de salida: cualquier dedo hacia arriba finaliza el gesto.

Efecto: acercar o alejar el objeto subyacente directamente e inmediatamente a medida que los dedos se separan o se aproximan en el eje. Asegúrese de mantener los puntos de contacto debajo del dedo a lo largo del gesto.

![aterrizaje \-areazoom.png](images/inter-touch-image6.png)

Gesto de zoom.

**Turno para girar**

Girar con dos o más dedos hace que un objeto rote. Gira el dispositivo propiamente dicho para girar toda la pantalla.

Estado de entrada: dos dedos en contacto con la pantalla al mismo tiempo.

Movimiento: uno o ambos dedos giran alrededor del otro y se mueven a la línea entre ellos.

Estado de salida: cualquier dedo hacia arriba finaliza el gesto.

Efecto: gira el objeto subyacente en la misma cantidad que han girado los dedos. Asegúrese de mantener los puntos de contacto debajo del dedo a lo largo del gesto.

![touch \-turn.png](images/inter-touch-image7.png)

Gesto de rotación.

La rotación solo tiene sentido para determinados tipos de objetos, por lo que no se asigna a una interacción de Windows sistema.

La rotación suele realizarse de forma diferente por diferentes personas. Algunas personas prefieren girar un dedo alrededor de un dedo pivote, mientras que otras prefieren girar ambos dedos en un movimiento circular. La mayoría de las personas usan una combinación de los dos, con un dedo que se mueve más que el otro. Aunque la rotación suave a cualquier ángulo es la mejor interacción, en muchos contextos, como la visualización de fotos, es mejor establecer la rotación de 90 grados más cercana una vez que el usuario lo permita. En la edición de fotos, puede usar una pequeña rotación para enderezar la foto.

**Deslizar el dedo desde el borde para los comandos de la aplicación**

Al deslizar el dedo a una distancia corta desde el borde inferior o superior de la pantalla, se revelan los comandos de la aplicación en una barra de la aplicación.

Estado de entrada: uno o varios dedos tocan el bisel.

Movimiento: arrastre una distancia corta a la pantalla y la elevación.

Estado de salida: el último dedo hacia arriba finaliza el gesto.

Efecto: se muestra la barra de la aplicación.

![deslizar \- el \- dedo hacia abajo \-edge.png](images/inter-touch-image8.png)

![deslizar \- el \- dedo \-edge.png](images/inter-touch-image9.png)

Gesto de deslizar el dedo desde el borde.

Desarrolladores: para obtener más información, [**consulte enumeración DIRECTMANIPULATION \_ CONFIGURATION.**](/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_configuration)

### <a name="control-usage"></a>Control del uso

Aquí se proporcionan algunas directrices para optimizar los controles para el uso táctil.

-   **Use controles comunes.** Los controles más comunes están diseñados para admitir una buena experiencia táctil.
-   **Elija controles personalizados diseñados para admitir la función táctil.** Es posible que necesite controles personalizados para admitir las experiencias especiales del programa. Elija controles personalizados que:
    -   Puede tener un tamaño lo suficientemente grande como para facilitar la selección de destino y la manipulación.
    -   Cuando se manipula, mueva y reaccione de la manera en que los objetos del mundo real se mueven y reaccionan, por ejemplo, al tener impulso y fricción.
    -   Son una forma de permitir que los usuarios corrijan fácilmente los errores.
    -   Son la impermeabilidad al hacer clic y arrastrar. Los objetos que se coloquen cerca de su destino deben colocarse en el lugar correcto.
    -   Tener comentarios visuales claros cuando el dedo está sobre el control.
-   **Use controles restringidos.** Los controles restringidos, como las listas y los controles deslizantes, cuando se diseñan para una orientación táctil sencilla, pueden ser mejores que los controles sin restricciones, como los cuadros de texto, porque reducen la necesidad de entrada de texto.
-   **Proporcione los valores predeterminados adecuados.** Seleccione la opción más segura (para evitar la pérdida de datos o el acceso del sistema) y la opción más segura de forma predeterminada. Si la seguridad y la seguridad no son factores, seleccione la opción más probable o cómoda, lo que elimina la interacción innecesaria.
-   **Proporcione la finalización automática de texto.** Proporciona una lista de los valores más probables, o los valores de entrada más recientes, para que la entrada de texto sea mucho más fácil.
-   **En el caso de** las tareas importantes que usan varias selecciones, si se usa normalmente una lista de selección múltiple estándar, proporcione una opción para usar una lista de casillas en su lugar.

### <a name="control-sizes-and-touch-targeting"></a>Control de los tamaños y la orientación táctil

Debido a la gran superficie del dedo, los controles pequeños demasiado cercanos pueden ser difíciles de dirigir con precisión.

Como regla general, un tamaño de control de 23 x 23 píxeles (13 x 13 DDU) es un buen tamaño mínimo de control interactivo para cualquier dispositivo de entrada. Por el contrario, los controles de número a 15 x 11 píxeles son demasiado pequeños para usarse eficazmente con la táctil.

![Captura de pantalla que muestra el ancho y el alto de los botones de selección arriba y abajo, que mide 9 D DLL (15 píxeles) de ancho por 5 D DLL (9 píxeles) de alto.](images/inter-touch-image14.png)

Tenga en cuenta que el tamaño mínimo se basa realmente en el área física, no en métricas de diseño como píxeles o D DLL. La investigación indica que el área de destino mínima para una interacción eficaz y precisa mediante un dedo es de 6 x 6 milímetros (mm). Esta área se traduce en métricas de diseño como esta:



| Fuente             | Milímetros | Píxeles relativos | ARCHIVOS DLL  |
|------------------|-------------|-----------------|-------|
| 9 puntos Segoe UI | 6x6         | 23x23           | 13x13 |
| 8 puntos deMenteoma   | 6x6         | 23x23           | 15x14 |



 

Además, la investigación muestra que un tamaño mínimo de 10 x 10 mm (unos 40 x 40 píxeles) permite una mejor velocidad y precisión, y también se siente más cómodo para los usuarios. Cuando sea práctico, use este tamaño mayor para los botones de comando usados para los comandos más importantes o usados con frecuencia.

El objetivo no es tener controles enormes, solo los que se usan fácilmente con el toque.

![Captura de pantalla que muestra Microsoft Word barra de herramientas con el botón "A B C Spelling & Grammar" resaltado, con una altura de DLU de 41 y un ancho de DLU de 40.](images/inter-touch-image15.png)

En este ejemplo, Microsoft Word botones de más de 10 x 10 mm para los comandos más importantes.

![Captura de pantalla que muestra la Windows calculadora.](images/inter-touch-image16.png)

Esta versión de calculator usa botones de más de 10 x 10 mm para sus comandos más usados.

No hay un tamaño perfecto para los destinos táctiles. Los distintos tamaños funcionan para diferentes situaciones. Las acciones con consecuencias graves (como eliminar y cerrar) o las acciones usadas con frecuencia deben usar destinos táctiles grandes. Las acciones usadas con poca frecuencia con consecuencias menores pueden usar destinos pequeños.

**Directrices de tamaño de destino para controles personalizados**



| Guía de tamaño                                                                                 | Descripción                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![Tamaño mínimo recomendado de 7x7](images/inter_touch_image10.jpeg)<br/>      | **7x7 mm: tamaño mínimo recomendado**<br/> 7 x 7 mm es un buen tamaño mínimo si tocar el destino incorrecto se puede corregir en uno o dos gestos o en un plazo de cinco segundos. El relleno entre destinos es tan importante como el tamaño de destino.<br/>                               |
| ![Tamaño recomendado de 9x9 para la precisión](images/inter_touch_image11.jpeg)<br/> | **Cuando la precisión es importante**<br/> Cerrar, eliminar y otras acciones con consecuencias graves no puede permitirse pulsaciones accidentales. Use destinos de 9 x 9 mm si tocar el destino incorrecto requiere más de dos gestos, cinco segundos o un cambio de contexto importante para corregirlo.<br/>     |
| ![Tamaño mínimo de 5x5](images/inter_touch_image12.jpeg)<br/>                  | **Cuando simplemente no cabe**<br/> Si se encuentra con cosas que caben, es correcto usar destinos de 5 x 5 mm, siempre y cuando se pueda corregir el destino incorrecto con un gesto. El uso de 2 mm de relleno entre destinos es muy importante en este caso.<br/> |



 

**Directrices de tamaño de destino para controles comunes**

-   **Para los controles comunes, use los tamaños de control recomendados.** El tamaño de control recomendado satisface el tamaño mínimo de 23 x 23 píxeles (13 x 13 DLU), excepto las casillas y los botones de radio (su ancho de texto compensa ligeramente), los controles de número (que no se pueden usar con la función táctil, pero son redundantes) y los divisores.

    ![Captura de pantalla que muestra un ejemplo de controles comunes, incluidos los controles de audio, un botón "Examinar Internet ahora" y una Explorador de archivos ventana.](images/inter-touch-image17.png)

    Los tamaños de control recomendados son fáciles de tocar.

-   **En el caso de los botones de comando usados para los comandos más importantes o usados con frecuencia, use un tamaño mínimo de 40 x 40 píxeles (23 x 22 D DLL) siempre que sea práctico.** Si lo hace, ofrece una mejor velocidad y precisión, y también se siente más cómodo para los usuarios.

    ![Captura de pantalla que muestra varios tamaños de un botón "Enviar" de correo electrónico, con los tamaños más pequeños a mayores de izquierda a derecha.](images/inter-touch-image18.png)

    Siempre que sea práctico, use botones de comandos más grandes para comandos importantes o usados con frecuencia.

-   **Para otros controles:**

    -   **Use destinos de clic más grandes.** Para controles pequeños, haga que el tamaño de destino sea mayor que el elemento de interfaz de usuario visible estáticamente. Por ejemplo, los botones de icono de 16 x 16 píxeles pueden tener botones de destino de clic de 23 x 23 píxeles y los elementos de texto pueden tener rectángulos de selección de 8 píxeles más anchos que el texto y 23 píxeles de alto.

        Correcto:

        ![Captura de pantalla que muestra una barra de herramientas con el tamaño de destino correcto.](images/inter-touch-image19.png)

        Incorrecto:

        ![Captura de pantalla que muestra un árbol de IA con un área de destino de tamaño incorrecto.](images/inter-touch-image20.png)

        Correcto:

        ![Captura de pantalla que muestra un árbol de IA con el tamaño correcto para el área de destino.](images/inter-touch-image21.png)

        En los ejemplos correctos, los destinos de clic son mayores que los elementos de interfaz de usuario visibles estáticamente.

    -   **Use destinos de clic redundantes.** Es aceptable que los destinos de clic sean menores que el tamaño mínimo si ese control tiene funcionalidad redundante.

        Por ejemplo, los triángulos de divulgación progresiva utilizados por el control de vista de árbol son solo de 6 x 9 píxeles, pero su funcionalidad es redundante con sus etiquetas de elemento asociadas.

        ![Captura de pantalla que muestra un árbol de IA con destinos de clic redundantes.](images/inter-touch-image22.png)

        Los triángulos de vista de árbol son demasiado pequeños para ser fácilmente táctiles, pero tienen redundancia en la funcionalidad con sus etiquetas asociadas más grandes.

        Respetar las métricas del sistema. No codificar de forma codificada los tamaños. Si es necesario, los usuarios pueden cambiar las métricas o ppp del sistema para adaptarse a sus necesidades. Sin embargo, trata esto como último recurso porque los usuarios normalmente no deben tener que ajustar la configuración del sistema para que la interfaz de usuario se pueda usar.

        ![Captura de pantalla que muestra un alto de menú estándar a la izquierda y un alto de menú mayor a la derecha.](images/inter-touch-image23.png)

        En este ejemplo, se ha cambiado la métrica del sistema para el alto del menú.

Edición de texto

La edición de texto es una de las interacciones más complicadas al usar un dedo. El uso de controles restringidos, los valores predeterminados adecuados y la finalización automática eliminan o reducen la necesidad de introducir texto. Pero si la aplicación implica editar texto, puede hacer que los usuarios sean más productivos si amplía automáticamente la interfaz de usuario de entrada hasta un 150 % de forma predeterminada cuando se usa la función táctil.

Por ejemplo, un programa de correo electrónico podría mostrar la interfaz de usuario con un tamaño táctil normal, pero acercar la interfaz de usuario de entrada al 150 por ciento para redactar los mensajes.

![Captura de pantalla que muestra una E/S de correo electrónico.](images/inter-touch-image24.png)

En este ejemplo, la interfaz de usuario de entrada se acerca al 150 por ciento.

### <a name="control-layout-and-spacing"></a>Diseño y espaciado de control

El espaciado entre controles es un factor significativo para que los controles se puedan tocar fácilmente. La orientación es más rápida pero menos precisa cuando se usa un dedo como dispositivo que apunta, lo que da lugar a que los usuarios toque más a menudo fuera de su destino previsto. Cuando los controles interactivos se colocan muy cerca, pero no se tocan realmente, los usuarios pueden hacer clic en el espacio inactivo entre los controles. Dado que hacer clic en el espacio inactivo no tiene ningún resultado o comentarios visuales, los usuarios a menudo no están seguros de lo que salió mal.

**Ajuste dinámicamente el espaciado en función del dispositivo de entrada utilizado.** Esto es especialmente útil con la interfaz de usuario transitoria, como los menús y los controles emergentes.

**Proporcione un mínimo de 5 píxeles (3 D DLL) de espacio entre las regiones de destino de los controles interactivos.** Si los controles pequeños están demasiado espaciados, el usuario debe pulsar con precisión para evitar pulsar el objeto incorrecto.

**Haga que los controles de los grupos sean más fáciles de diferenciar mediante el uso de más que el espaciado vertical recomendado entre los controles.** Por ejemplo, los botones de radio de 19 píxeles de alto son más cortos que el tamaño mínimo recomendado de 23 píxeles. Cuando tenga espacio vertical disponible, puede lograr aproximadamente el mismo efecto que el tamaño recomendado agregando 4 píxeles de espaciado adicionales a los 7 píxeles estándar.

Correcto:

![Captura de pantalla que muestra un ejemplo estándar de espaciado vertical entre controles.](images/inter-touch-image25.png)

Mejor:

![Captura de pantalla que muestra un ejemplo de controles con más espaciado vertical.](images/inter-touch-image26.png)

En el mejor ejemplo, el espaciado adicional entre los botones de radio facilita su diferenciación.

Puede haber situaciones en las que el espaciado adicional sería deseable al usar la función táctil, pero no cuando se usa el mouse o el teclado. En tales casos, solo se usa un diseño más amplio cuando se inicia una acción mediante la función táctil.

**Elija un diseño que coloca los controles cerca de donde es más probable que se van a usar.** Mantenga las interacciones de tareas dentro de un área pequeña siempre que sea posible y localice los controles cerca de donde es más probable que se van a usar. Evite los movimientos de mano de larga distancia, especialmente para tareas comunes y para arrastres.

Tenga en cuenta que la ubicación del puntero actual es la más cercana a un destino, lo que hace que sea trivial adquirirlo. Por lo tanto, los menús contextuales aprovechan al máximo la ley de Fitts, al igual que las mini barras de herramientas que Microsoft Office.

![Captura de pantalla que muestra un ejemplo de un menú contextual y una mini barra de herramientas Microsoft Office en paralelo.](images/inter-touch-image27.png)

**Evite colocar controles pequeños cerca del borde de la aplicación o la pantalla.** Los objetivos pequeños cerca de los bordes pueden ser difíciles de tocar (los biseles de pantalla pueden interferir con los gestos del borde). Para asegurarse de que los controles son fáciles de dirigir cuando se maximiza una ventana, puede hacerlos al menos de 23 x 23 píxeles (13 x 13 D DLL) o colocarlos fuera del borde de la ventana.

**Use el espaciado recomendado.** El espaciado recomendado es táctil. Sin embargo, si la aplicación puede beneficiarse de un tamaño y espaciado mayores, tenga en cuenta que el tamaño y el espaciado recomendados son mínimos cuando corresponda.

**Proporcione al menos 5 píxeles (3 D DLL) de espacio entre controles interactivos.** Si lo hace, se evita la confusión cuando los usuarios pulsan fuera de su destino previsto.

Considere la posibilidad de agregar más que el espaciado vertical recomendado dentro de grupos de controles, como vínculos de comandos, casillas y botones de radio, así como entre los grupos. Al hacerlo, son más fáciles de diferenciar.

**Considere la posibilidad de agregar más que el espaciado vertical recomendado dinámicamente cuando se inicia una acción mediante la función táctil.** Si lo hace, los objetos son más fáciles de diferenciar, pero sin tener que dejar más espacio al usar un teclado o un mouse. Aumente el espaciado en un tercio de su tamaño normal o al menos 8 píxeles.

![imagen](images/inter-touch-image28.png)

En este ejemplo, Windows 7 listas de saltos de la barra de tareas son más cómodas cuando se muestran mediante la función táctil.

### <a name="interaction"></a>Interacción

El uso de los controles correctos le permite solo una parte del camino a una aplicación táctil optimizada, también debe tener en cuenta el modelo de interacción general que admiten esos controles. Estas son algunas directrices para ayudarle con esto.

-   **Haga que el puntero sea redundante.** La mayoría de las tecnologías táctiles no admiten el desplazamiento del mouse, por lo que los usuarios con estas pantallas táctiles no pueden realizar ninguna tarea que requiera mantener el puntero.
-   **Para las aplicaciones que necesitan entrada de texto, integre completamente la característica de teclado táctil** mediante:
    -   Proporcionar los valores predeterminados adecuados para la entrada del usuario.
    -   Proporcionar sugerencias de autocompletar cuando sea necesario.

    > [!Note]  
    > Desarrolladores: para obtener más información sobre la integración del teclado táctil, [**vea ITextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel).

     

-   **Permitir a los usuarios acercar la interfaz de usuario de contenido si el programa tiene tareas que requieren editar texto.** Considere la posibilidad de acercar automáticamente al 150 % cuando se usa la función táctil.
-   **Proporcione movimiento panorámico y zoom suave y con capacidad de respuesta siempre que sea adecuado.** Vuelva a dibujar rápidamente después de un desplazamiento panorámico o zoom para mantener la capacidad de respuesta. Es necesario hacerlo para que la manipulación directa sea realmente directa.
-   **Durante un movimiento panorámico o zoom, asegúrese de que los puntos de contacto permanecen debajo del dedo a lo largo del gesto.** De lo contrario, el desplazamiento panorámico o el zoom es difícil de controlar.
-   **Dado que los gestos se memorizan, asígneles significados coherentes entre aplicaciones.** No dé significados diferentes a los gestos con semántica fija. En su lugar, use un gesto específico de la aplicación adecuado.

### <a name="forgiveness"></a>Perdón

La manipulación directa hace que el toque sea natural, expresivo, eficaz y atractivo. Sin embargo, cuando hay manipulación directa, puede haber una manipulación accidental y, por lo tanto, la necesidad de una repulsa.

La excepción es la capacidad de invertir o corregir fácilmente una acción no deseada. Puede realizar una experiencia táctil al proporcionar deshacer, proporcionar buenos comentarios visuales, tener una separación física clara entre los comandos usados con frecuencia y los comandos destructivos, y permitir que los usuarios corrijan los errores fácilmente. La asociación con la inserte impide que se realicen acciones no deseadas en primer lugar, lo que se puede hacer mediante controles restringidos y confirmaciones de acciones o comandos de riesgo que tienen consecuencias no deseadas.

-   **Proporcione un comando Deshacer.** Es mejor proporcionar una manera sencilla de deshacer todos los comandos, pero la aplicación puede tener algunos comandos cuyo efecto no se puede deshacer.
-   **Siempre que sea práctico, proporcione buenos comentarios sobre el dedo hacia abajo, pero no tome medidas hasta que se den los dedos.** Esto permite a los usuarios corregir los errores antes de que los cometen.
-   **Siempre que sea práctico, permita a los usuarios corregir errores fácilmente.** Si una acción tiene efecto sobre el dedo hacia arriba, permita que los usuarios corrijan los errores deslizándose mientras el dedo sigue estando abajo.
-   **Siempre que sea práctico, indique que no se puede realizar una manipulación directa al resistir el movimiento.** Permita que se haga el movimiento, pero haga que el objeto vuelva a establecerse cuando se libera para indicar claramente que la acción se ha reconocido, pero no se puede realizar.
-   **Tener una separación física clara entre los comandos usados con frecuencia y los comandos destructivos.** De lo contrario, los usuarios podrían tocar comandos destructivos accidentalmente. Un comando se considera destructivo si su efecto está generalizado y no se puede deshacer fácilmente o el efecto no se aprecia inmediatamente.
-   **Confirme los comandos de acciones o comandos de riesgo que tienen consecuencias imp previstas.** Use un cuadro de diálogo de confirmación para este propósito.
-   **Considere la posibilidad de confirmar cualquier otra acción que los usuarios tienden a realizar accidentalmente al usar la función táctil y que no se puedan pasar desapercibidas o que sean difíciles de deshacer.** Normalmente, se denominan confirmaciones rutinarias y no se recomiendan en función de la suposición de que los usuarios no suelen emitir dichos comandos por accidente con un mouse o un teclado. Para evitar confirmaciones innecesarias, presente estas confirmaciones solo si el comando se inició mediante la función táctil.

    Las confirmaciones rutinarias son aceptables para las interacciones que los usuarios suelen realizar accidentalmente mediante la función táctil.

    Desarrolladores: puede distinguir entre eventos del mouse y eventos táctiles mediante [**INPUT \_ MESSAGE \_ SOURCE**](/windows/win32/api/winuser/ns-winuser-input_message_source) API.

