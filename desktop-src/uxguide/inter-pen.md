---
title: Lápiz
description: Todas las aplicaciones de Microsoft Windows deben tener el lápiz habilitado. Y hacerlo es más fácil de lo que piensa.
ms.assetid: 45635d5a-c9ff-47d0-89ef-a9c48ac67594
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 35994f345306bd3a270f8d8cf9760e7d07183941
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "103914001"
---
# <a name="pen"></a>Lápiz

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Todas las aplicaciones de Microsoft Windows deben tener el lápiz habilitado. Y hacerlo es más fácil de lo que piensa.

La entrada manuscrita hace referencia a la forma en que Windows le permite interactuar directamente con un equipo mediante un lápiz. Un lápiz se puede usar para señalar y también para gestos, entrada de texto simple y captura de ideas de forma libre en la tinta digital.

El lápiz que se usa para la entrada tiene una punta fina, Smooth que admite señalar, escribir o dibujar en tinta de forma precisa. El lápiz también puede tener un botón de pluma opcional (se usa para realizar clics con el botón derecho) y un borrador (usado para borrar la entrada manuscrita). La mayoría de los lápices admiten el desplazamiento.

![figura de un lápiz típico ](images/inter-pen-image1.png)

Lápiz típico.

Cuando el lápiz se utiliza para la escritura a mano, los trazos del usuario se pueden convertir en texto mediante el reconocimiento de escritura a mano. Los trazos se pueden mantener tal y como se escribieron, con reconocimiento realizado en segundo plano para admitir la búsqueda y la copia como texto. Estos trazos no convertidos se denominan tinta digital.

![captura de pantalla de la página escritura a mano en OneNote ](images/inter-pen-image2.png)

Ejemplo de entrada de lápiz.

La mayoría de los programas de Windows ya son compatibles con el lápiz en el caso de que se pueda usar un lápiz en lugar de un mouse, el lápiz funciona sin problemas en las tareas e interacciones más importantes y el programa responde a los gestos. Un programa es compatible con escritura a mano cuando ayuda con la entrada de texto manuscrita. Un programa se habilita para la entrada de lápiz cuando puede controlar la entrada manuscrita directamente, en lugar de requerir que los trazos del lápiz se traduzcan a texto o a movimientos del mouse equivalentes. Esto permite a los usuarios escribir, dibujar y agregar comentarios en tinta digital de flujo libre y de alta calidad. La recopilación de entradas manuscritas es diferente de la recopilación de eventos del mouse, porque la tinta requiere una resolución mayor y una mayor velocidad de muestreo, y también puede Agregar matices con presión e inclinación. Para obtener información acerca de la creación de programas descriptivos y habilitados para escritura a mano, vea integrar entradas de [lápiz](/previous-versions/windows/desktop/ms700674(v=vs.85)) y [texto mediante el lápiz](/previous-versions/windows/desktop/ms695501(v=vs.85)).

Al colocar un lápiz, es menos necesario un cursor porque la sugerencia se representa a sí misma. Sin embargo, para la ayuda de destino, Windows proporciona un pequeño cursor de lápiz que indica la ubicación actual del lápiz. Al contrario que el puntero del mouse que reemplaza, el cursor del lápiz no es necesario a menos que el lápiz esté cerca de la pantalla, por lo que desaparece después de unos segundos de inactividad para permitir una vista de información no obstaculizada.

La mayoría de los programas compatibles con el lápiz admiten gestos. Un gesto es un movimiento rápido del lápiz en una pantalla que el equipo interpreta como un comando, en lugar de como movimiento, escritura o dibujo del mouse. Uno de los gestos más rápidos y sencillos de realizar es un gesto. Un gesto es un gesto sencillo que da como resultado una navegación o un comando de edición. Los gestos de navegación incluyen arrastrar hacia arriba, arrastrar hacia abajo, retroceder y avanzar, mientras que los gestos de edición incluyen copiar, pegar, deshacer y eliminar.

Todos los punteros excepto el puntero ocupado tienen una zona activa de un solo píxel que define la ubicación exacta de la pantalla del puntero. La zona activa determina qué objeto se ve afectado por la interacción. Los objetos definen una zona activa, que es el área donde se considera que la zona activa está sobre el objeto. Normalmente, la zona activa coincide con los bordes de un objeto, pero puede ser más grande para facilitar la interacción.

**Dado que un lápiz puede señalar más exactamente que un dedo, si la interfaz de usuario funciona bien para Touch, también funcionará bien para un lápiz.** Por lo tanto, este artículo se centra principalmente en agregar compatibilidad con el lápiz a programas que ya se han diseñado para tocarlos.

**Nota:** Las instrucciones relacionadas con el [mouse](inter-mouse.md), la [accesibilidad](inter-accessibility.md)y la [entrada táctil](inter-touch.md) se presentan en artículos independientes.

## <a name="design-concepts"></a>Conceptos de diseño

El uso de un lápiz para la entrada tiene las siguientes características:

-   **Natural e intuitivo.** Todos saben cómo apuntar y pulsar con un lápiz. Las interacciones de objeto están diseñadas para que se correspondan con el modo en que los usuarios interactúan con objetos del mundo real de una manera coherente.
-   **Expresivo.** Los trazos de un lápiz son fáciles de controlar, lo que facilita la escritura, el dibujo, el boceto, la pintura y la anotación en lugar de hacerlo con un mouse.
-   **Más personal.** Del mismo modo que una nota manuscrita o una firma es más personal que una con tipo, el uso de una nota o firma manuscrita digitalmente también es más personal.
-   **Menos intrusivo.** El uso de un lápiz es silencioso y, por tanto, es mucho menos molesto que escribir o hacer clic, especialmente en situaciones sociales como las reuniones.
-   **Portable.** Un equipo con una capacidad de lápiz puede ser más compacto, ya que la mayoría de las tareas se pueden completar sin un teclado, un mouse o un panel táctil. Puede ser más flexible porque no requiere una superficie de trabajo. Permite nuevos lugares y escenarios para el uso de un equipo.
-   **Directos e interesantes.** El uso de un lápiz le parece que está interactuando directamente con los objetos de la pantalla, mientras que el uso de un mouse o Touchpad siempre requiere la coordinación de los movimientos de la mano con movimientos de puntero en pantalla independientes que se consideran indirectos mediante comparación.

**Todos los programas de Windows deben tener una buena experiencia de lápiz.** Los usuarios deben poder realizar las tareas más importantes del programa de forma eficaz con un lápiz. Algunas tareas, como la escritura o la manipulación detallada de píxeles, no son adecuadas para un lápiz, pero deben ser al menos posibles.

Afortunadamente, si el programa ya está bien diseñado y es fácil de utilizar, proporcionar un buen soporte para el lápiz es fácil de hacer. Para este propósito, un programa bien diseñado:

-   **Tiene buena compatibilidad con el mouse.** Los controles interactivos tienen prestaciones claras, visibles y tienen un estado de desplazamiento para los comentarios del puntero. Los objetos tienen comportamientos estándar para las interacciones con el mouse estándar (un solo clic con el botón primario y doble, clic con el botón derecho, arrastrar y mantener el puntero). La [forma de puntero](inter-mouse.md) cambia según corresponda para indicar el tipo de manipulación directa.
-   **Tiene buena compatibilidad con el teclado.** El programa hace que los usuarios sean eficientes al proporcionar asignaciones de teclas de método abreviado estándar, especialmente para los comandos de navegación y edición que también se pueden generar a través de gestos.
-   **Tiene controles lo suficientemente grandes para tocar.** Los controles tienen un tamaño mínimo de 23x23 píxeles (13x13 unidades de cuadro de diálogo \[ DLU \] ) y los controles que se usan con más frecuencia son al menos 40 x 40 píxeles (23x22 DLU). Para evitar un comportamiento que no responde, no debería haber espacios reducidos entre los destinos. los elementos de la interfaz de usuario se deben espaciar de manera que los destinos adyacentes estén tocando o tengan al menos 5 píxeles (3 DLU) de espacio entre ellos.
-   **Está accesible.** Usa Microsoft Active Accessibility (MSAA) para proporcionar acceso mediante programación a la interfaz de usuario para las tecnologías de asistencia. El programa responde correctamente a los cambios de métricas del tema y del sistema.
-   **Funciona bien y tiene un aspecto correcto en 120 ppp (puntos por pulgada),** que es la resolución de pantalla predeterminada recomendada para los equipos con lápiz habilitado.
-   **Usa controles comunes.** Los controles más comunes están diseñados para admitir una buena experiencia de lápiz. Si es necesario, el programa usa controles personalizados bien implementados que están diseñados para admitir la manipulación y el destino sencillos.
-   **Usa controles restringidos.** Cuando se diseña para facilitar el destino, los controles restringidos como las listas y los controles deslizantes pueden ser mejores que los controles no restringidos, como los cuadros de texto, porque reducen la necesidad de escribir texto.
-   **Proporciona los valores predeterminados adecuados.** El programa selecciona la opción más segura (para evitar la pérdida de datos o el acceso al sistema) y la opción más segura de forma predeterminada. Si la seguridad y la seguridad no son factores, el programa selecciona la opción más probable o conveniente, con lo que se elimina la interacción innecesaria.
-   **Proporciona la finalización automática del texto.** Proporciona una lista de los valores de entrada más probables o recientes para que la entrada de texto sea mucho más fácil.

Desafortunadamente, lo contrario también es cierto si el programa no está bien diseñado, sus deficiencias serán especialmente obvias para los usuarios que usen un lápiz.

### <a name="model-for-pen-interaction"></a>Modelo de interacción del lápiz

Si no tiene experiencia con el uso de un lápiz, la mejor introducción es aprender a hacerlo. Obtenga un equipo con lápiz habilitado, coloque el mouse y el teclado, y realice las tareas que normalmente realiza con un solo lápiz. Asegúrese de probar los programas habilitados para tinta, como Windows Journal, y los programas que no están habilitados para tinta. Si tiene un Tablet PC, experimente con su sujeción en posiciones diferentes, como en su vuelta, en una mesa plana o en sus brazos mientras está de pie. Pruebe a usarlo en orientación vertical y horizontal, y mantenga el lápiz para escribir y solo para apuntar a la izquierda, así como a su derecha.

Al experimentar con el uso de un lápiz, detectará lo siguiente:

-   **Los controles pequeños son difíciles de usar.** El tamaño de los controles afecta en gran medida a su capacidad para interactuar eficazmente. Los controles que son 10x10 píxeles funcionan razonablemente para un lápiz, pero los controles mayores se sienten más cómodos para usarlos. Por ejemplo, [los controles de número](ctrl-spin-controls.md) (15x11 píxeles) son demasiado pequeños para usarlos con un lápiz fácilmente.
-   **La mano es un factor.** A veces, su mano cubre cosas con las que podría querer ver o interactuar. Por ejemplo, los menús contextuales de los usuarios que se entregan a la derecha son difíciles de usar si aparecen a la derecha del punto de clic, por lo que es mejor si aparecen a la izquierda. Windows permite a los usuarios indicar su mano en el elemento del panel de control de configuración de Tablet PC.
-   **La localidad de tareas ayuda.** Aunque puede mover el puntero a través de una pantalla de 14 pulgadas con un movimiento del mouse de 3 pulgadas, el uso de un lápiz requiere que mueva la mano a las 14 pulgadas. Moverse repetidamente entre los destinos que están lejos puede ser tedioso, por lo que es mucho mejor mantener las interacciones de las tareas dentro del intervalo de una mano cuando sea posible. Los menús contextuales son prácticos porque no requieren ningún movimiento de mano.
-   **La entrada y la selección de texto son difíciles.** La entrada de texto larga es especialmente difícil con un lápiz, por lo que la finalización automática y los valores de texto predeterminados aceptables pueden simplificar realmente las tareas. La selección de texto también puede ser bastante difícil, por lo que las tareas son más fáciles cuando no requieren una ubicación de cursor precisa.
-   **Los destinos pequeños cerca del borde de la pantalla pueden ser muy difíciles de tocar.** Algunos biseles de pantalla sobresalen y algunas tecnologías de pantalla táctil son menos sensibles en los bordes, lo que permite que los controles cercanos al borde sean más difíciles de usar. Por ejemplo, los botones minimizar, maximizar/restaurar y cerrar de la barra de título pueden ser más difíciles de usar cuando se maximiza una ventana.

### <a name="control-location"></a>Ubicación del control

La localidad de la tarea reduce los movimientos de pantalla repetidos que se repiten. Para minimizar los movimientos de mano, busque los controles cercanos a dónde se van a usar con mayor probabilidad.

**Incorrecto:**

![captura de pantalla de la paleta de colores separada de herramientas ](images/inter-pen-image3.png)

En este ejemplo de Windows XP, la paleta de colores está demasiado lejos desde donde es probable que se use.

Tenga en cuenta que la ubicación actual del usuario es la más cercana a un destino, por lo que es fácil de adquirir. Por lo tanto, los menús contextuales sacan el máximo partido de la [ley de Fitts](inter-mouse.md), al igual que las barras de herramientas utilizadas por Microsoft Office.

![captura de pantalla de punteros cercanos a menús ](images/inter-pen-image4.png)

La ubicación actual del puntero siempre es la más fácil de adquirir.

Los destinos pequeños cerca del borde de la pantalla pueden ser difíciles de orientar, por lo que evite colocar pequeños controles cerca de los bordes de la ventana. Para asegurarse de que los controles sean fáciles de destinar cuando se maximice una ventana, 23x23 píxeles como mínimo (13x13 DLU) o colóquelos fuera del borde de la ventana.

### <a name="pen-interactions"></a>Interacciones de lápiz

**Gestos del sistema**

Windows define y controla los gestos del sistema. Como resultado, todos los programas de Windows tienen acceso a ellos. Estos gestos tienen mensajes equivalentes del mouse, el teclado y el comando de la aplicación:



| Gesto del sistema                                                           | Mensaje equivalente sintetizado                                              |
|------------------------------------------------------------|-----------------------------------------------|
| Mantener el mouse (cuando sea compatible)<br/>                          | Mantener el mouse<br/>                        |
| Pulsar (abajo y arriba)<br/>                               | Clic con el botón primario<br/>                   |
| Doble punteo (hacia arriba y hacia arriba dos veces)<br/>                  | Doble clic con el mouse<br/>            |
| Presionar y mantener presionado (bajar, pausar, subir)<br/>                | Clic con el botón secundario del mouse<br/>                  |
| Arrastrar (abajo, subir, subir)<br/>                           | Arrastrar a la izquierda<br/>                    |
| Presione, mantenga presionado y arrastre (abajo, pausa, movimiento, arriba)<br/>   | Arrastrar el mouse hacia la derecha<br/>                   |
| Seleccionar (bajar, desplace sobre objetos seleccionables, arriba)<br/> | Selección del mouse<br/>                       |



 

**Desarrolladores:** Para obtener más información, vea [enumeración SystemGesture](/previous-versions/ms552724(v=vs.100)).

**Gestos**

Los gestos son movimientos simples que son aproximadamente el equivalente de los métodos abreviados de teclado. Los gestos de navegación incluyen arrastrar hacia arriba, arrastrar hacia abajo, retroceder y avanzar. Los gestos de edición incluyen copiar, pegar, deshacer y eliminar. Para usar gestos, el programa solo debe responder a los comandos de pulsaciones de tecla relacionados.

![Diagrama que muestra los gestos de gestos y sus asignaciones predeterminadas en Windows 7.](images/inter-pen-image5.png)

Los ocho gestos de gestos y sus asignaciones predeterminadas en Windows 7. Los gestos de navegación se cambiaron para que se correspondan con el movimiento panorámico (donde el objeto se mueve con el gesto) en lugar de desplazarse (donde el objeto se mueve en la dirección opuesta del gesto).

![figura de gestos de gestos, como el gesto de movimiento ](images/inter-pen-image6.png)

Los ocho gestos de gestos y sus asignaciones predeterminadas en Windows Vista.

Los gestos de navegación tienen una asignación natural, por lo que resultan fáciles de aprender y recordar. Los gestos de edición son diagonales que requieren más precisión y sus asignaciones no son tan naturales (Desplácese hacia la papelera de reciclaje para eliminar, desplácese en la dirección de la flecha atrás hasta deshacer), por lo que no están habilitadas de forma predeterminada. Todas las acciones de gesto se pueden personalizar mediante el elemento lápiz y dispositivos de entrada del panel de control.



| Plaza                                     | Mensaje equivalente sintetizado                                                            |
|--------------------------------------|-------------------------------------------------------------|
| Gesto hacia la izquierda<br/>                | Comando reenviar (comando atrás para Windows Vista)<br/> |
| Gesto hacia la derecha<br/>               | Comando atrás (comando adelante para Windows Vista)<br/> |
| Subir<br/>                  | Desplazamiento hacia abajo del teclado<br/>                             |
| Gesto hacia abajo<br/>                | Desplazamiento hacia arriba del teclado<br/>                               |
| Desplazar hacia arriba-diagonal izquierda<br/>    | Eliminación de teclado<br/>                                  |
| Gesto hacia abajo-diagonal izquierda<br/>  | Deshacer teclado<br/>                                    |
| Gesto hacia arriba: diagonal derecha<br/>   | Copia del teclado<br/>                                    |
| Gesto hacia abajo: diagonal derecha<br/> | Pegar teclado<br/>                                   |



 

**Gestos de aplicación**

Las aplicaciones también pueden definir y controlar otros gestos. El reconocedor de gestos de Microsoft puede reconocer más de [40 movimientos](../tablet/application-gestures-and-semantic-behavior.md). Para usar los gestos de aplicación, el programa debe definir los gestos que reconoce y, a continuación, controlar los eventos resultantes.

**Capacidad de respuesta y coherencia**

**La capacidad de respuesta es esencial para crear experiencias de lápiz que se sienten directas e interesantes.** Para sentirse directos, los gestos deben surtir efecto inmediatamente y los puntos de contacto de un objeto deben permanecer bajo el lápiz sin problemas a lo largo del gesto. Cualquier retraso, respuesta entrecortada, pérdida de contacto o resultados inexactos destruye la percepción de la manipulación directa y también de la calidad.

**La coherencia es esencial para crear experiencias de lápiz que parezcan naturales e intuitivas.** Una vez que los usuarios aprenden un gesto estándar, esperan que el gesto tenga el mismo efecto en todos los programas aplicables. Para evitar confusiones y frustraciones, no asigne nunca significados no estándar a gestos estándar. En su lugar, use gestos personalizados para las interacciones únicas del programa.

**Editar la tinta y el texto**

La edición de la tinta y el texto se encuentran entre las interacciones más desafiantes al usar un lápiz. El uso de controles restringidos, los valores predeterminados adecuados y la finalización automática elimina o reduce la necesidad de escribir texto. Pero si el programa implica la edición de texto o de entrada manuscrita, **puede hacer que los usuarios sean más productivos mediante la ampliación automática de la interfaz de usuario de entrada al 150 por ciento de forma predeterminada cuando se usa un lápiz.**

Por ejemplo, un programa de correo electrónico podría mostrar la interfaz de usuario en un tamaño normal, pero ampliar la interfaz de usuario de entrada al 150 por ciento para componer mensajes.

![captura de pantalla del mensaje de Outlook con una fuente grande ](images/inter-pen-image7.png)

En este ejemplo, la interfaz de usuario de entrada se amplía al 150 por ciento.

**Si solo hace cuatro cosas...**

1.  1. Haga que sus programas de Windows tengan una buena experiencia de lápiz. Los usuarios deben poder llevar a cabo las tareas más importantes del programa de forma eficaz con un lápiz (al menos las tareas que no implican mucho de escritura o de manipulación detallada de píxeles).
2.  2. Considere la posibilidad de agregar compatibilidad para escribir, dibujar y agregar comentarios directamente mediante la entrada de lápiz en los escenarios más relevantes.
3.  3. Para crear una experiencia directa e interesante, haga que los gestos surtan efecto inmediatamente, mantenga los puntos de contacto en el lápiz del usuario sin problemas a lo largo del gesto y tenga el efecto de la asignación de gestos directamente en el movimiento del usuario.
4.  4. Para crear una experiencia natural e intuitiva, se admiten los gestos estándar adecuados y se les asigna su significado estándar. Use gestos personalizados para las interacciones únicas del programa.

## <a name="guidelines"></a>Directrices

### <a name="control-usage"></a>Uso del control

-   **Prefiera usar controles comunes.** Los controles más comunes están diseñados para admitir una buena experiencia de lápiz.
-   **Prefiere controles restringidos.** Use controles restringidos como listas y controles deslizantes siempre que sea posible, en lugar de controles sin restricciones como cuadros de texto, para reducir la necesidad de entradas de texto.
-   **Proporcione los valores predeterminados adecuados.** Seleccione la opción más segura (para evitar la pérdida de datos o el acceso al sistema) y la opción más segura de forma predeterminada. Si la seguridad y la seguridad no son factores, seleccione la opción más probable o conveniente, con lo que se elimina la interacción innecesaria.
-   **Proporcionar finalización automática de texto.** Proporcione una lista de los valores de entrada más probables o recientes para que la entrada de texto sea mucho más fácil.
-   **En el caso de las tareas importantes que usan la selección múltiple, si se usa normalmente una lista de selección múltiple estándar, proporcione una opción para usar en su lugar una lista de casillas.**
-   **Respetar las métricas del sistema.** Use las métricas del sistema para todos los tamaños sin cableado. Si es necesario, los usuarios pueden cambiar las métricas del sistema o los PPP para adaptarse a sus necesidades. Sin embargo, trate esto como último recurso, ya que los usuarios no deberían tener que ajustar la configuración del sistema para que la interfaz de usuario pueda usarse.

![captura de pantalla de menús con un tamaño normal y grande ](images/inter-pen-image8.png)

En este ejemplo, se ha cambiado la métrica del sistema para el alto del menú.

### <a name="control-sizing-layout-and-spacing"></a>Controlar el tamaño, el diseño y el espaciado

-   **En el caso de los controles comunes, use los tamaños de control recomendados.** Son lo suficientemente grandes para una buena experiencia de lápiz, excepto para los controles de número (que no se pueden usar con un lápiz pero son redundantes).
-   **Elija un diseño que coloque los controles cerca del lugar en el que probablemente se vayan a usar.** Mantenga las interacciones de tareas dentro de un área pequeña siempre que sea posible. Evite los movimientos de la mano de larga distancia, especialmente para las tareas comunes y para las arrastraciones.
-   **Use el espaciado recomendado.** El espaciado recomendado es compatible con el lápiz.
-   **Los controles interactivos deben tocarse o, preferiblemente, tener al menos 5 píxeles (3 DLU) de espacio entre ellos.** Al hacerlo, se evitará la confusión cuando los usuarios puntean fuera del destino previsto.
-   **Considere la posibilidad de agregar más del espaciado vertical recomendado dentro de grupos de controles,** como vínculos de comandos, casillas y botones de radio, así como entre los grupos. De este modo, resulta más fácil diferenciarlos.

### <a name="interaction"></a>Interacción

-   **En el caso de los programas diseñados para aceptar escritura a mano, habilite la entrada manuscrita predeterminada.** La entrada manuscrita predeterminada permite a los usuarios escribir entradas manuscritas simplemente empezando a escribirlas sin tener que pulsar, dar un comando o hacer nada especial. Al hacerlo, se habilita la experiencia más natural con un lápiz. En el caso de los programas que no están diseñados para aceptar escritura a mano, controle la entrada manuscrita en cuadros de texto como selección.
-   **Permitir a los usuarios hacer zoom en la interfaz de usuario de contenido** si el programa tiene tareas que requieren edición de texto. Considere la posibilidad de ampliar automáticamente al 150 por ciento cuando se usa un lápiz.
-   **Dado que los gestos se memorizan, asígneles significados que son coherentes en todos los programas.** No asigne diferentes significados a los gestos con semántica fija. En su lugar, use un gesto adecuado específico del programa.

### <a name="handedness"></a>Situación

-   **Si una ventana es contextual, mostrarla siempre cerca del objeto desde el que se inició.** Colóquelo fuera del camino para que el objeto de origen no esté incluido en la ventana.
    -   Si se muestra con el mouse, cuando sea posible, coloque el desplazamiento de la ventana contextual hacia abajo y a la derecha.

        ![figura de la ventana contextual situada a la derecha del objeto ](images/inter-pen-image9.png)

        Mostrar las ventanas contextuales cerca del objeto desde el que se inició.

    -   Si se muestra con un lápiz, siempre que sea posible Coloque la ventana contextual para que no esté incluida en la mano del usuario. En el caso de los usuarios que se entregan a la derecha, se muestran a la izquierda; de lo contrario, se muestra a la derecha.

        ![figura de la ventana contextual colocada a la izquierda del objeto ](images/inter-pen-image10.png)

        Al usar un lápiz, muestre también ventanas contextuales para que no estén incluidas en la mano del usuario.

-   **Desarrolladores:** Puede distinguir entre eventos del mouse y eventos del lápiz mediante la API de [GetMessageExtraInfo](../tablet/system-events-and-mouse-messages.md) . Puede determinar la [mano](/previous-versions/ms819495(v=msdn.10)) del usuario mediante la API [SystemParametersInfo](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con SPI \_ GETMENUDROPALIGNMENT.

### <a name="forgiveness"></a>Forgiveness

-   **Proporcione un comando Deshacer.** Idealmente, debe proporcionar la función de deshacer para todos los comandos, pero es posible que el programa tenga algunos comandos cuyo efecto no se puede deshacer.
-   **Proporcione buenos comentarios sobre el desplazamiento.** Indique claramente si el lápiz se encuentra sobre un destino en el que se pueda hacer clic. Estos comentarios son una excelente manera de evitar la manipulación accidental.
-   **Siempre que sea práctico, proporcione buenos comentarios sobre el lápiz hacia abajo, pero no realice acciones hasta el movimiento o el lápiz.** Esto permite a los usuarios corregir errores antes de que los hagan.
-   **Siempre que sea práctico, permita a los usuarios corregir errores fácilmente.** Si una acción surte efecto en el lápiz, permita a los usuarios corregir los errores deslizando mientras el lápiz está inactivo.

## <a name="documentation"></a>Documentación

Al hacer referencia a la entrada del lápiz:

-   Haga referencia a un dispositivo de entrada de lápiz con forma de lápiz como lápiz. En la primera mención, use el lápiz de Tablet PC.
-   Haga referencia al botón situado en el lateral de un lápiz como botón del lápiz, no al botón del barril.
-   Consulte de forma genérica el teclado, el mouse, el Trackball, el lápiz o el dedo como dispositivo de entrada.
-   Use TAP (y pulse dos veces) en lugar de hacer clic al documentar procedimientos específicos para usar un lápiz. Puntee quiere decir que presione la pantalla y, a continuación, levante antes de un tiempo de espera. Puede usarse o no para generar un clic del mouse. Para las interacciones que no impliquen el lápiz, siga usando hacer clic.

