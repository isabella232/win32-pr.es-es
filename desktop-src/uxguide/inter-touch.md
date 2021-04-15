---
title: Tocar
description: Todas las aplicaciones de Microsoft Windows deben tener una excelente experiencia táctil. Y crear una experiencia de este tipo es más fácil de lo que piensa.
ms.assetid: a87d0726-1c57-4cf8-9e35-4e73a09ff1a3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a44a95ad963d3563418ed0492e55606824011f31
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104569964"
---
# <a name="touch"></a>Tocar

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Todas las aplicaciones de Microsoft Windows deben tener una excelente experiencia táctil. Y crear una experiencia de este tipo es más fácil de lo que piensa.

El toque se refiere al uso de uno o varios dedos para proporcionar la entrada a través de un dispositivo que se muestra e interactúa con Windows y las aplicaciones. Una aplicación táctil optimizada tiene un modelo de interfaz de usuario y de interacción diseñado para dar cabida a las áreas de contacto más grandes y menos precisas de la entrada táctil, los distintos factores de forma de los dispositivos táctiles y las numerosas posturas y agarres que los usuarios pueden adoptar al usar un dispositivo táctil.

![Usuario que interactúa con la tableta mediante el uso de Touch](images/inter_touch_image1.jpeg)

Cada dispositivo de entrada tiene sus puntos fuertes. El teclado es el mejor para la entrada de texto y para proporcionar comandos con un movimiento de mano mínimo. El mouse es más adecuado para apuntar de manera eficaz y precisa. La función táctil es la mejor opción para manipular objetos y ofrecer comandos sencillos. Un lápiz es mejor para la expresión de forma libre, al igual que con la escritura a mano y el dibujo.

Windows 8.1 está optimizado para la capacidad de respuesta, la precisión y la facilidad de uso con la función táctil, al mismo tiempo que admite los métodos de entrada tradicionales (como el mouse, el lápiz y el teclado). La velocidad, la precisión y los comentarios táctiles que proporcionan los modos de entrada tradicionales están familiarizados y atractivos para muchos usuarios y, potencialmente, son más adecuados para escenarios de interacción específicos.

Puede encontrar instrucciones relacionadas con el mouse, el lápiz y la accesibilidad en temas independientes.

Cuando piense en la experiencia de interacción de la aplicación:

No asuma que si una interfaz de usuario funciona bien para un mouse, también funciona bien para el toque. Aunque la buena compatibilidad con el mouse es un punto de partida, una buena experiencia táctil tiene algunos requisitos adicionales.

Supongamos que si una interfaz de usuario funciona bien para un dedo, también funciona bien para un lápiz. El hecho de que la aplicación se pueda tocar es una buena manera de proporcionar un buen soporte para el lápiz. La principal diferencia es que los dedos tienen una sugerencia más punta, por lo que necesitan destinos más grandes.

Con Touch, puede manipular objetos y la interfaz de usuario directamente, lo que facilita una experiencia más rápida, natural y atractiva.

## <a name="provide-a-great-touch-experience"></a>Proporcionar una excelente experiencia táctil

Debe asegurarse de que los usuarios pueden realizar las tareas críticas e importantes de forma eficaz mediante la entrada táctil. Sin embargo, la funcionalidad específica de la aplicación, como la manipulación de texto o de píxeles, podría no ser adecuada para la entrada táctil y se puede reservar para el dispositivo de entrada más adecuado.

Si no tiene mucha experiencia en el desarrollo de aplicaciones táctiles, lo mejor es aprender a hacerlo. Consigue un equipo táctil, coloca el mouse y el teclado, y usa solo los dedos para interactuar con tu aplicación. Si tiene una tableta, experimente con su sujeción en diferentes posiciones, como por ejemplo, en su vuelta, en una mesa plana o en sus brazos mientras está de pie. Pruebe a usarlo en orientación vertical y horizontal.

Las aplicaciones con optimización táctil que funcionan mejor con la interacción táctil suelen ser:

-   **Natural e intuitivo.** Las interacciones están diseñadas para que se correspondan con el modo en que los usuarios interactúan con objetos del mundo real.
-   **Menos intrusivo.** El uso de la función táctil es silenciosa y, en consecuencia, mucho menos que la escritura o el clic.
-   **Portable.** Los dispositivos táctiles son más compactos porque muchas tareas se pueden completar sin un teclado, un mouse, un lápiz o un panel táctil. También son más flexibles porque no se necesita una superficie de trabajo.
-   **Directos e interesantes.** La función táctil le parecerá que está manipulando objetos directamente en la pantalla.
-   **Menos preciso.** Los usuarios no pueden tener como destino objetos con la función táctil, en comparación con un mouse o un lápiz.

La función táctil proporciona una interacción natural y realista. La manipulación directa y la animación completan esta impresión, ya que proporcionan a los objetos un movimiento realista, dinámico y de comentarios. Por ejemplo, Imagine un juego de cartas. No solo es práctico y fácil arrastrar cartas con un dedo, la experiencia adopta una sensación real y atractiva cuando se puede descartar, deslizar y girar las tarjetas como si se tratara de una baraja física. Y al intentar mover una tarjeta que no se puede mover, es mejor tener la resistencia de la tarjeta, pero no evitar el movimiento y volver a colocarla cuando se lance, para indicar claramente que la acción se reconoció pero no se puede realizar.

Afortunadamente, si la aplicación ya está bien diseñada, proporcionar una excelente experiencia táctil es fácil de hacer. Para este propósito, un programa bien diseñado:

-   **Garantiza que las tareas más importantes se pueden realizar de forma eficaz con un dedo** (al menos las tareas que no implican una gran cantidad de tipos o una manipulación detallada de píxeles).
-   **Usa controles grandes para el toque.** Los controles comunes tienen un tamaño mínimo de 23x23 píxeles (13x13 DLU) y los controles que se usan con más frecuencia son al menos 40 x 40 píxeles (23x22 DLU). Para evitar un comportamiento que no responde, los elementos de la interfaz de usuario deben tener al menos 5 píxeles (3 DLU) de espacio entre ellos. En el caso de otros controles, asegúrese de que tengan al menos un destino de 23x23 píxeles (13x13 DLU), incluso si su apariencia estática es mucho menor. Consulte Ajuste de tamaño del control estándar.
-   **Admite la entrada del mouse.** Los controles interactivos tienen prestaciones claras y visibles. Los objetos tienen comportamientos estándar para las interacciones con el mouse estándar (un solo clic con el botón primario y doble, clic con el botón derecho, arrastrar y mantener el puntero).
-   **Admite la entrada de teclado.** La aplicación proporciona asignaciones de teclas de método abreviado estándar, especialmente para los comandos de navegación y edición que también se pueden generar a través de gestos táctiles.
-   **Garantiza la accesibilidad.** Usa la automatización de la interfaz de usuario o Microsoft Active Accessibility (MSAA) para proporcionar acceso mediante programación a la interfaz de usuario para las tecnologías de asistencia. La aplicación responde correctamente a los cambios de orientación, tema, configuración regional y métrica del sistema.
-   **Elimina las interacciones innecesarias.** Para evitar la pérdida de datos o el acceso al sistema, use los valores predeterminados más seguros y seguros. Si la seguridad y la seguridad no son factores, la aplicación selecciona la opción más probable o cómoda.
-   **Proporciona un equivalente táctil para mantener el mouse.** No confíe en el desplazamiento como la única forma de realizar una acción.
-   **Garantiza que los gestos surten efecto inmediatamente.** Mantenga los puntos de contacto en los dedos del usuario suavemente a lo largo del gesto, lo que proporciona el efecto de la asignación de gestos directamente al movimiento del usuario.
-   **Utiliza gestos estándar siempre que sea posible.** Gestos personalizados solo para interacciones únicas en la aplicación.
-   **Garantiza que se pueden invertir o corregir comandos no deseados o destructivos.** Las acciones accidentales son más probables al usar Touch.

## <a name="guidelines-for-touch-input"></a>Directrices para la entrada táctil

Con Touch, la aplicación de Windows puede usar gestos físicos para emular la manipulación directa de los elementos de la interfaz de usuario.

Tenga en cuenta estas prácticas recomendadas al diseñar la aplicación táctil:

**La capacidad de respuesta es esencial para crear experiencias táctiles que se sienten directas e interesantes.** Para sentirse directos, los gestos deben surtir efecto de inmediato y los puntos de contacto de un objeto deben permanecer bajo los dedos del usuario sin problemas en el gesto. El efecto de la entrada táctil debe asignarse directamente al movimiento del usuario, por lo que, por ejemplo, si el usuario gira los dedos 90 grados, el objeto también debe girar 90 grados. Cualquier retraso, respuesta entrecortada, pérdida de contacto o resultados inexactos destruye la percepción de la manipulación directa y también de la calidad.

**La coherencia es esencial para crear experiencias táctiles que parezcan naturales e intuitivas.** Una vez que los usuarios aprenden un gesto estándar, esperan que el gesto tenga el mismo efecto en todas las aplicaciones. Para evitar confusiones y frustraciones, no asigne nunca significados no estándar a gestos estándar. En su lugar, use gestos personalizados para las interacciones únicas del programa.

A continuación, describiremos el lenguaje táctil de Windows, pero antes de continuar, aquí se muestra una breve lista de los términos básicos de entrada táctil.

-   **Gesto**

    Un gesto es el acto físico o el movimiento realizado en, o por, el dispositivo de entrada (dedo, dedos, lápiz/lápiz, Mouse, etc.). Por ejemplo, para iniciar, activar o invocar un comando, se usa una sola pulsación de dedo para un dispositivo táctil o Touchpad (equivalente a un clic con el botón primario con un mouse, una pulsación con un lápiz o la tecla entrar en un teclado).

-   **Manipulación**

    Una manipulación es la reacción inmediata en tiempo real o la respuesta de un objeto o una interfaz de usuario a un movimiento. Por ejemplo, los gestos deslizar y deslizar rápidamente hacen que un elemento o una interfaz de usuario se muevan de alguna manera.

    El resultado final de una manipulación, cómo se manifiesta en el objeto en la pantalla y en la interfaz de usuario, es la interacción.

-   **Interacción**

    Las interacciones dependen de cómo se interprete una manipulación y el comando o la acción que se deriva de la manipulación. Por ejemplo, los objetos se pueden desplazar con los gestos deslizar y deslizar rápidamente, pero los resultados difieren en función de si se cruza un umbral de distancia. La diapositiva se puede usar para arrastrar un objeto o hacer una panorámica de una vista, mientras que el deslizamiento se puede usar para seleccionar un elemento o mostrar una barra de la aplicación.

### <a name="the-windows-touch-language"></a>El idioma de Windows Touch

Windows proporciona un conjunto conciso de interacciones táctiles que se usan en todo el sistema. Aplicar este lenguaje táctil hace que su aplicación esté familiarizado con lo que los usuarios ya conocen. Esto aumenta la confianza del usuario al facilitar el aprendizaje y el uso de la aplicación. Para obtener más información sobre la implementación de Touch Language, vea gestos, manipulaciones e interacciones.

**Mantenga presionado para aprender**

El gesto de mantener presionado muestra información detallada o la enseñanza de objetos visuales (por ejemplo, una información sobre herramientas o un menú contextual) sin confirmar una acción o un comando. El movimiento panorámico sigue siendo posible si se inicia un gesto deslizante mientras se muestra el visual.

> [!IMPORTANT]
> Puede usar la opción de mantener presionado para seleccionar en los casos en los que está habilitado el movimiento panorámico horizontal y vertical.

 

Estado de entrada: uno o dos dedos en contacto con la pantalla.

Motion: sin movimiento.

Estado de salida: el último dedo arriba finaliza el gesto.

Efecto: Mostrar más información.

![\-Pulse \- para \-learn.png](images/inter-touch-image2.png)

El gesto de mantener presionado.

**Al mantener el puntero**

Mantener el puntero es una interacción útil porque permite a los usuarios obtener información adicional a través de sugerencias antes de iniciar una acción. Ver estas sugerencias hace que los usuarios se sientan más seguros y reduzcan los errores.

Desafortunadamente, el desplazamiento no es compatible con las tecnologías táctiles, por lo que los usuarios no pueden mantener el mouse cuando se usa un dedo. La solución más sencilla a este problema es sacar el máximo partido de Hover, pero solo de maneras que no son necesarias para realizar una acción. En la práctica, esto normalmente significa que la acción también se puede realizar haciendo clic en, pero no necesariamente exactamente de la misma manera.

![Captura de pantalla que muestra un ejemplo de la interacción del mouse junto a un ejemplo de la acción de clic.](images/inter-touch-image13.png)

En este ejemplo, los usuarios pueden ver la fecha de hoy al mantener el mouse o hacer clic en.

**Puntee en la acción principal**

Al pulsar en un elemento, se invoca su acción principal, por ejemplo, al iniciar una aplicación o al ejecutar un comando.

Estado de entrada: un dedo en contacto con la pantalla o el panel táctil y se eleva antes del umbral de tiempo para una interacción de mantener presionado.

Motion: sin movimiento.

Estado de salida: el dedo hacia arriba finaliza el gesto.

Efecto: inicie una aplicación o ejecute un comando.

![toque \- táctil \-primary.png](images/inter-touch-image3.png)

El gesto de puntear.

**Deslizar al pan**

Slide se usa principalmente para las interacciones de movimiento panorámico, pero también se puede usar para mover (donde el movimiento panorámico está restringido a una dirección), dibujando o escribiendo. La diapositiva también puede usarse para tener como destino elementos pequeños y comprimidos de forma densa mediante la limpieza (deslizando el dedo sobre objetos relacionados, como botones de radio).

Estado de entrada: uno o dos dedos en contacto con la pantalla.

Motion: arrastre, con cualquier dedo adicional que quede en la misma posición con respecto al otro.

Estado de salida: el último dedo arriba finaliza el gesto.

Efecto: mueva el objeto subyacente directamente e inmediatamente como se muevan los dedos. Asegúrese de mantener el punto de contacto bajo el dedo a lo largo del gesto.

![\-slide.png táctil](images/inter-touch-image4.png)

Movimiento de la panorámica.

**Deslizar hasta seleccionar, comando y desplace**

Deslizar el dedo una distancia corta, perpendicular a la dirección de movimiento panorámico (donde el movimiento panorámico está restringido a una dirección), selecciona los objetos de una lista o una cuadrícula. Muestra la barra de la aplicación con comandos relevantes cuando se seleccionan objetos.

Estado de entrada: uno o varios dedos tocan la pantalla.

Movimiento: arrastre una distancia corta y eleve antes de que se produzca el umbral de distancia para una interacción de movimiento.

Estado de salida: el último dedo arriba finaliza el gesto.

Efecto: el objeto subyacente se selecciona, se mueve o se muestra la barra de la aplicación. Asegúrese de mantener el punto de contacto bajo el dedo a lo largo del gesto.

![d: \\ sdkenlistment \\ m \- UX \- diseño \\ m \- experiencia de \- diseño de \\ las imágenes \\ táctil \-swipe.png](images/inter-touch-image5.png)

El gesto de deslizar rápidamente.

**Reducir y ampliar para hacer zoom**

Los gestos de pinch y Stretch se usan para tres tipos de interacciones: zoom óptico, cambio de tamaño y zoom semántico.

Zoom óptico: ajusta el nivel de ampliación de todo el área de contenido para obtener una vista más detallada del contenido. En cambio, el cambio de tamaño es una técnica para ajustar el tamaño relativo de uno o más objetos dentro de un área de contenido sin cambiar la vista en el área de contenido.

El zoom semántico es una técnica basada en el toque para presentar y navegar por datos estructurados o contenido dentro de una sola vista (por ejemplo, la estructura de carpetas de un equipo, una biblioteca de documentos o un álbum de fotos) sin necesidad de controles de vista de árbol, desplazamiento o panorámica. El zoom semántico proporciona dos vistas diferentes del mismo contenido, ya que le permite ver más detalles a medida que amplía y reduce el detalle a medida que se aleja.

Estado de entrada: dos dedos en contacto con la pantalla al mismo tiempo.

Movimiento: los dedos se alejan (se expanden) o juntos (el contacto) a lo largo de un eje.

Estado de salida: cualquier dedo hacia arriba finaliza el gesto.

Efecto: acercar o alejar el objeto subyacente directamente e inmediatamente como los dedos separan o enfocan el eje. Asegúrese de mantener los puntos de contacto bajo el dedo a lo largo del gesto.

![areazoom.png de aterrizaje \-](images/inter-touch-image6.png)

Gesto de zoom.

**Gire para girar**

La rotación con dos o más dedos hace que un objeto gire. Gira el dispositivo propiamente dicho para girar toda la pantalla.

Estado de entrada: dos dedos en contacto con la pantalla al mismo tiempo.

Motion: uno o ambos dedos giran alrededor de la otra, desplazándose perpendicularmente a la línea entre ellas.

Estado de salida: cualquier dedo hacia arriba finaliza el gesto.

Efecto: Gire el objeto subyacente la misma cantidad que se ha girado el dedo. Asegúrese de mantener los puntos de contacto bajo el dedo a lo largo del gesto.

![\-turn.png táctil](images/inter-touch-image7.png)

El movimiento de rotación.

La rotación solo tiene sentido para ciertos tipos de objetos, por lo que no se asigna a una interacción de Windows del sistema.

La rotación se realiza a menudo de forma diferente en distintas personas. Algunas personas prefieren girar un dedo alrededor de un dedo dinámico, mientras que otros prefieren girar ambos dedos en un movimiento circular. La mayoría de los usuarios usan una combinación de ambos, con un dedo moviendo más que el otro. Aunque la rotación suave a cualquier ángulo es la mejor interacción, en muchos contextos, como la visualización de fotografías, es mejor que se liquide con la rotación de 90 grados más cercana una vez que el usuario pueda ir. En la edición de fotografías, puede usar una pequeña rotación para enderezar la foto.

**Deslizar rápidamente desde el borde para los comandos de la aplicación**

Deslizar el dedo una distancia corta desde el borde inferior o superior de la pantalla revela los comandos de la aplicación en una barra de la aplicación.

Estado de entrada: uno o varios dedos tocan el bisel.

Motion: arrastre una distancia corta hasta la pantalla y eleve.

Estado de salida: el último dedo arriba finaliza el gesto.

Efecto: se muestra la barra de la aplicación.

![presionar el dedo hacia la \- derecha \- \-edge.png](images/inter-touch-image8.png)

![\-deslizar el dedo \- lateral \-edge.png](images/inter-touch-image9.png)

Deslizar el dedo desde el movimiento del borde.

Desarrolladores: para obtener más información, consulte enumeración de [**\_ configuración de DIRECTMANIPULATION**](/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_configuration) .

### <a name="control-usage"></a>Uso del control

Aquí se proporcionan algunas directrices para optimizar los controles para el uso táctil.

-   **Usar controles comunes.** Los controles más comunes están diseñados para admitir una buena experiencia táctil.
-   **Elija los controles personalizados que están diseñados para admitir la funcionalidad táctil.** Es posible que necesite controles personalizados para admitir las experiencias especiales del programa. Elija controles personalizados que:
    -   Puede tener un tamaño lo suficientemente grande como para facilitar la manipulación y el destino.
    -   Cuando se manipulan, se mueven y reaccionan la forma en que los objetos del mundo real se mueven y reaccionan, por ejemplo, en el momento y la fricción.
    -   Los permisivo permiten a los usuarios corregir fácilmente errores.
    -   Se permisivo de la inexactitud al hacer clic y arrastrar. Los objetos que se colocan cerca de su destino deberían encontrarse en el lugar correcto.
    -   Tenga claros comentarios visuales cuando el dedo esté sobre el control.
-   **Usar controles restringidos.** Los controles restringidos como listas y controles deslizantes, cuando se diseñan para facilitar la entrada táctil, pueden ser mejores que los controles sin restricciones, como los cuadros de texto, porque reducen la necesidad de entradas de texto.
-   **Proporcione los valores predeterminados adecuados.** Seleccione la opción más segura (para evitar la pérdida de datos o el acceso al sistema) y la opción más segura de forma predeterminada. Si la seguridad y la seguridad no son factores, seleccione la opción más probable o conveniente, con lo que se elimina la interacción innecesaria.
-   **Proporcionar la finalización automática del texto.** Proporciona una lista de los valores más probables, o los valores de entrada más recientes, para facilitar enormemente la entrada de texto.
-   En el caso **de las tareas importantes que usan la selección múltiple**, si se usa normalmente una lista de selección múltiple estándar, proporcione una opción para usar en su lugar una lista de casillas.

### <a name="control-sizes-and-touch-targeting"></a>Tamaños de control y destino táctil

Debido al gran área de la superficie de la mano, los pequeños controles que están demasiado cercanos pueden ser difíciles de dirigir con precisión.

Como norma general, un tamaño de control de 23x23 píxeles (13x13 DLU) es un buen tamaño de control interactivo mínimo para cualquier dispositivo de entrada. Por el contrario, los controles de número en píxeles de 15x11 son demasiado pequeños para usarlos de forma eficaz con el toque.

![Captura de pantalla que muestra el ancho y el alto de los botones de selección arriba y abajo, midiendo 9 DLU (15 píxeles) de ancho por 5 DLU (9 píxeles) alto.](images/inter-touch-image14.png)

Tenga en cuenta que el tamaño mínimo se basa realmente en el área física, no en las métricas de diseño como píxeles o DLU. La investigación indica que el área de destino mínima para una interacción eficaz y precisa con un dedo es 6x6 milímetros (mm). Esta área se traduce en métricas de diseño como esta:



| Fuente             | Milímetros | Píxeles relativos | DLU  |
|------------------|-------------|-----------------|-------|
| Segoe UI de punto 9 | 6x6         | 23x23           | 13x13 |
| Tahoma de 8 puntos   | 6x6         | 23x23           | 15x14 |



 

Además, la investigación muestra que un tamaño mínimo de 10x10 mm (aproximadamente 40 x 40 píxeles) permite mejorar la velocidad y la precisión, y también se siente más cómodo para los usuarios. Cuando sea práctico, use este tamaño mayor para los botones de comando usados para los comandos más importantes o usados con frecuencia.

El objetivo no es tener controles gigantes, solo los que se usan con facilidad con el toque.

![Captura de pantalla que muestra la barra de herramientas de Microsoft Word con el botón "A B C ortografía & gramática" resaltado, con un alto de 41 DLU y un ancho de 40 DLU.](images/inter-touch-image15.png)

En este ejemplo, Microsoft Word usa botones de más de 10x10 mm para los comandos más importantes.

![Captura de pantalla que muestra la calculadora de Windows.](images/inter-touch-image16.png)

Esta versión de la calculadora usa botones de más de 10x10 mm para los comandos usados con mayor frecuencia.

No hay ningún tamaño perfecto para los destinos táctiles. Los diferentes tamaños funcionan en diferentes situaciones. Las acciones con consecuencias graves (como eliminar y cerrar) o acciones usadas con frecuencia deben usar destinos táctiles grandes. Las acciones que se usan con poca frecuencia con consecuencias secundarias pueden usar destinos pequeños.

**Directrices de tamaño de destino para controles personalizados**



| Instrucciones de tamaño                                                                                 | Descripción                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![7x7 tamaño mínimo recomendado](images/inter_touch_image10.jpeg)<br/>      | **7x7 mm: tamaño mínimo recomendado**<br/> 7x7 mm es un buen tamaño mínimo si el toque del destino equivocado puede corregirse en uno o dos gestos o en un plazo de cinco segundos. El relleno entre destinos es tan importante como el tamaño de destino.<br/>                               |
| ![9x9 tamaño recomendado de precisión](images/inter_touch_image11.jpeg)<br/> | **Cuando la precisión es importante**<br/> Las acciones de cierre, eliminación y otras con consecuencias graves no pueden permitirse el grifo accidental. Use destinos de 9x9 mm si el destino equivocado requiere más de dos gestos, cinco segundos o un cambio de contexto importante para corregirlos.<br/>     |
| ![tamaño mínimo 5x5](images/inter_touch_image12.jpeg)<br/>                  | **Cuando no quepa**<br/> Si Cramming cosas para que quepan, es adecuado usar destinos de 5x5 mm siempre y cuando se pueda corregir el objetivo equivocado con un gesto. En este caso, es muy importante usar 2 mm de relleno entre destinos.<br/> |



 

**Directrices de tamaño de destino para controles comunes**

-   **En el caso de los controles comunes, use los tamaños de control recomendados.** El ajuste de tamaño del control recomendado cumple el tamaño mínimo de 23x23 píxeles (13x13 DLU), excepto las casillas y los botones de radio (su ancho de texto se compensa ligeramente), los controles de número (que no se pueden usar con funciones táctiles, pero son redundantes) y los divisores.

    ![Captura de pantalla que muestra un ejemplo de controles comunes, incluidos controles de audio, un botón "explorar Internet Now" y una ventana del explorador de archivos.](images/inter-touch-image17.png)

    Los tamaños de control recomendados se pueden tocar fácilmente.

-   **En el caso de los botones de comando usados para los comandos más importantes o usados con frecuencia, use un tamaño mínimo de 40 x 40 píxeles (23x22 DLU) siempre que sea práctico.** Al hacerlo, se consigue una mayor velocidad y precisión, y también se siente más cómodo para los usuarios.

    ![Captura de pantalla que muestra varios tamaños de un botón de envío de correo electrónico, con los tamaños más pequeños a los más grandes, empezando de izquierda a derecha.](images/inter-touch-image18.png)

    Siempre que sea práctico, use botones de comando más grandes para comandos importantes o usados con frecuencia.

-   **Para otros controles:**

    -   **Usar destinos de clic más grandes.** En el caso de los controles pequeños, haga que el tamaño de destino sea mayor que el elemento de la interfaz de usuario visible estáticamente. Por ejemplo, los botones de icono de 16x16 píxeles pueden tener un clic en los botones de destino de un píxel de 23x23 y los elementos de texto pueden tener rectángulos de selección de 8 píxeles más anchos que el texto y 23 píxeles de alto.

        Correcto:

        ![Captura de pantalla que muestra una barra de herramientas con el tamaño de destino correcto.](images/inter-touch-image19.png)

        Incorrecto:

        ![Captura de pantalla que muestra un árbol U I con un área de destino de tamaño incorrecto.](images/inter-touch-image20.png)

        Correcto:

        ![Captura de pantalla que muestra un árbol U I con el tamaño correcto para el área de destino.](images/inter-touch-image21.png)

        En los ejemplos correctos, los destinos de clic son más grandes que los elementos de la interfaz de usuario visibles estáticamente.

    -   **Usar destinos de clic redundantes.** Es aceptable que los destinos de clic sean menores que el tamaño mínimo si ese control tiene funcionalidad redundante.

        Por ejemplo, los triángulos de divulgación progresiva utilizados por el control de vista de árbol solo son 6x9 píxeles, pero su funcionalidad es redundante con sus etiquetas de elemento asociadas.

        ![Captura de pantalla que muestra un árbol U I con destinos de clic redundantes.](images/inter-touch-image22.png)

        Los triángulos de la vista de árbol son demasiado pequeños para poderse tocar fácilmente, pero son redundantes en la funcionalidad con sus etiquetas asociadas más grandes.

        Respetar las métricas del sistema. No codificar tamaños. Si es necesario, los usuarios pueden cambiar las métricas del sistema o los PPP para adaptarse a sus necesidades. Sin embargo, trate esto como último recurso, ya que los usuarios no deberían tener que ajustar la configuración del sistema para que la interfaz de usuario pueda usarse.

        ![Captura de pantalla que muestra un alto de menú estándar a la izquierda y un mayor alto de menú a la derecha.](images/inter-touch-image23.png)

        En este ejemplo, se ha cambiado la métrica del sistema para el alto del menú.

Edición de texto

Editar texto es una de las interacciones más desafiantes cuando se usa un dedo. El uso de controles restringidos, los valores predeterminados adecuados y la finalización automática elimina o reduce la necesidad de escribir texto. Pero si la aplicación implica la edición de texto, puede hacer que los usuarios sean más productivos mediante la ampliación automática de la interfaz de usuario de entrada al 150 por ciento de forma predeterminada cuando se usa Touch.

Por ejemplo, un programa de correo electrónico podría mostrar la interfaz de usuario en un tamaño táctil normal, pero ampliar la interfaz de usuario de entrada al 150 por ciento para componer mensajes.

![Captura de pantalla que muestra un mensaje de correo electrónico U I.](images/inter-touch-image24.png)

En este ejemplo, la interfaz de usuario de entrada se amplía al 150 por ciento.

### <a name="control-layout-and-spacing"></a>Diseño y espaciado del control

El espaciado entre los controles es un factor importante para que los controles se puedan tocar fácilmente. El destino es más rápido pero menos preciso cuando se usa un dedo como dispositivo señalador, lo que da lugar a que los usuarios PUNTEEN fuera del destino previsto. Cuando los controles interactivos se colocan muy cerca, pero no se están tocando realmente, los usuarios pueden hacer clic en el espacio inactivo entre los controles. Dado que al hacer clic en espacio inactivo no hay ningún resultado ni ningún comentario visual, a menudo los usuarios no están seguro de qué salió mal.

**Ajuste el espaciado de forma dinámica en función del dispositivo de entrada usado.** Esto es especialmente útil con la interfaz de usuario transitoria como menús y controles flotantes.

**Proporcione un mínimo de 5 píxeles (3 DLU) de espacio entre las regiones de destino de los controles interactivos.** Si los controles pequeños están demasiado cerca de un espacio, el usuario debe puntear con precisión para evitar puntear en el objeto equivocado.

**Facilite la diferenciación de los controles de los grupos mediante el uso de más que el espaciado vertical recomendado entre los controles.** Por ejemplo, los botones de radio de 19 píxeles de alto son más cortos que el tamaño mínimo recomendado de 23 píxeles. Si hay espacio vertical disponible, puede lograr aproximadamente el mismo efecto que el tamaño recomendado si agrega un espaciado de 4 píxeles adicional a los 7 píxeles estándar.

Correcto:

![Captura de pantalla que muestra un ejemplo estándar de espaciado vertical entre los controles.](images/inter-touch-image25.png)

Mejor:

![Captura de pantalla que muestra un ejemplo de controles con más espaciado vertical.](images/inter-touch-image26.png)

En el mejor ejemplo, el espaciado adicional entre los botones de radio facilita la diferenciación.

Puede haber situaciones en las que el espaciado adicional sea conveniente al usar la función táctil, pero no al usar el mouse o el teclado. En tales casos, use solo un diseño más "espacioso" cuando se inicie una acción con Touch.

**Elija un diseño que coloque los controles cerca del lugar en el que probablemente se vayan a usar.** Mantenga las interacciones de las tareas dentro de un área pequeña siempre que sea posible y busque los controles cercanos a donde es más probable que se usen. Evite los movimientos de la mano de larga distancia, especialmente para las tareas comunes y para las arrastraciones.

Tenga en cuenta que la ubicación actual del puntero es la más cercana a un destino, por lo que es fácil de adquirir. Por lo tanto, los menús contextuales sacan el máximo partido de la ley de Fitts, al igual que las barras de herramientas utilizadas por Microsoft Office.

![Captura de pantalla que muestra un ejemplo de un menú contextual y una minibarra de herramientas de Microsoft Office en paralelo.](images/inter-touch-image27.png)

**Evite colocar pequeños controles cerca del borde de la aplicación o de la pantalla.** Los destinos pequeños cerca de los bordes pueden ser difíciles de tocar (los biseles de pantalla pueden interferir con los gestos perimetrales). Para asegurarse de que los controles sean fáciles de destinar cuando se maximice una ventana, 23x23 píxeles como mínimo (13x13 DLU) o colóquelos fuera del borde de la ventana.

**Use el espaciado recomendado.** El espaciado recomendado es táctil. Sin embargo, si la aplicación puede beneficiarse de un mayor tamaño y espaciado, tenga en cuenta que el ajuste de tamaño y el espaciado recomendados son mínimos cuando corresponda.

**Proporcione al menos 5 píxeles (3 DLU) de espacio entre los controles interactivos.** Al hacerlo, se evitará la confusión cuando los usuarios puntean fuera del destino previsto.

Considere la posibilidad de agregar más del espaciado vertical recomendado dentro de grupos de controles, como vínculos de comandos, casillas y botones de radio, así como entre los grupos. De este modo, resulta más fácil diferenciarlos.

**Considere la posibilidad de agregar más del espaciado vertical recomendado dinámicamente cuando se inicia una acción mediante la función táctil.** Esto hace que los objetos sean más fáciles de diferenciar, pero sin ocupar más espacio al usar un teclado o un mouse. Aumente el espaciado con un tercio de su tamaño normal o al menos 8 píxeles.

![imagen](images/inter-touch-image28.png)

En este ejemplo, las listas de saltos de la barra de tareas de Windows 7 son más "espacioso" cuando se muestran con Touch.

### <a name="interaction"></a>Interacción

El uso de los controles correctos le permite que solo forme parte de la forma de una aplicación optimizada para uso táctil. también debe tener en cuenta el modelo de interacción global que admiten esos controles. Estas son algunas instrucciones para ayudarle con esto.

-   **Haga que el mantener el mouse sea redundante.** El desplazamiento no es compatible con la mayoría de las tecnologías táctiles, por lo que los usuarios con estas pantallas no pueden realizar ninguna tarea que requiera el desplazamiento.
-   **En el caso de las aplicaciones que necesitan entradas de texto, integre totalmente la característica de teclado táctil** :
    -   Proporcionar los valores predeterminados adecuados para los datos proporcionados por el usuario.
    -   Proporcionar sugerencias de autocompletar cuando sea necesario.

    > [!Note]  
    > Desarrolladores: para obtener más información sobre la integración del teclado táctil, vea [**ITextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel).

     

-   **Permitir a los usuarios hacer zoom en la interfaz de usuario de contenido si el programa tiene tareas que requieren edición de texto.** Considere la posibilidad de ampliar automáticamente al 150 por ciento cuando se use Touch.
-   **Proporcione movimiento y zoom suaves y con capacidad de respuesta, siempre que sea necesario.** Vuelva a dibujar rápidamente después de una pan o zoom para que siga respondiendo. Esto es necesario para que la manipulación directa sea realmente directa.
-   **Durante una panorámica o un zoom, asegúrese de que los puntos de contacto permanecen bajo el dedo a lo largo del gesto.** De lo contrario, es difícil controlar el pan o el zoom.
-   **Dado que los gestos se memorizan, asígneles significados que son coherentes entre las aplicaciones.** No asigne diferentes significados a los gestos con semántica fija. En su lugar, use un gesto adecuado específico de la aplicación.

### <a name="forgiveness"></a>Forgiveness

La manipulación directa hace que el toque sea natural, expresivo, eficiente y atractivo. Sin embargo, cuando hay manipulación directa, puede haber una manipulación accidental y, por tanto, la necesidad de forgiveness.

Forgiveness es la capacidad de revertir o corregir fácilmente una acción no deseada. Puede realizar una experiencia de permisivo al proporcionar la función de deshacer y ofrecer buenos comentarios visuales, tener una separación física clara entre los comandos usados con frecuencia y los comandos destructivos, y permitir a los usuarios corregir errores fácilmente. Asociado con forgiveness impide que se produzcan acciones no deseadas en el primer lugar, lo que puede hacer mediante el uso de controles restringidos y confirmaciones para acciones o comandos de riesgo que tienen consecuencias no deseadas.

-   **Proporcione un comando Deshacer.** Es mejor proporcionar una manera sencilla de deshacer todos los comandos, pero la aplicación puede tener algunos comandos cuyo efecto no se puede deshacer.
-   **Siempre que sea práctico, proporcione buenos comentarios sobre el dedo, pero no lleve a cabo acciones hasta el dedo.** Esto permite a los usuarios corregir errores antes de que los hagan.
-   **Siempre que sea práctico, permita a los usuarios corregir errores fácilmente.** Si una acción surte efecto en el dedo, permita a los usuarios corregir los errores deslizando mientras el dedo permanece inactivo.
-   **Siempre que sea práctico, indique que no se puede realizar una manipulación directa al resistir el movimiento.** Permite que se produzca el movimiento, pero que el objeto se vuelva a poner en marcha cuando se lance para indicar claramente que se reconoció la acción, pero no se puede realizar.
-   **Tener una separación física clara entre los comandos usados con frecuencia y los comandos destructivos.** De lo contrario, los usuarios podrían tocar comandos destructivos de forma accidental. Un comando se considera destructivo si su efecto está generalizado y no se puede deshacer fácilmente, o el efecto no se percibe de inmediato.
-   **Confirme los comandos de acciones o comandos de riesgo que tengan consecuencias no deseadas.** Use un cuadro de diálogo de confirmación para este fin.
-   **Considere la posibilidad de confirmar cualquier otra acción que los usuarios tienden a realizar accidentalmente cuando se usa la función táctil y que se desaconsejan o son difíciles de deshacer.** Normalmente, se denominan confirmaciones rutinarias y no se recomiendan en función de la suposición de que los usuarios no suelen emitir tales comandos accidentalmente con un mouse o un teclado. Para evitar confirmaciones innecesarias, presente estas confirmaciones solo si el comando se inició mediante Touch.

    Las confirmaciones rutinarias son aceptables para las interacciones que los usuarios suelen usar de forma accidental.

    Desarrolladores: puede distinguir entre eventos del mouse y eventos táctiles mediante la API de [**\_ \_ origen del mensaje de entrada**](/windows/win32/api/winuser/ns-winuser-input_message_source) .

