---
title: Lápiz
description: Todas las aplicaciones Windows Microsoft deben estar habilitadas para el lápiz. Y hacerlo es más fácil de lo que cree.
ms.assetid: 45635d5a-c9ff-47d0-89ef-a9c48ac67594
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 90c953fe1c287741bec266bfe6516a6a8922692b213292d2f17cccebf561cb0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117853416"
---
# <a name="pen"></a>Lápiz

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Todas las aplicaciones Windows Microsoft deben estar habilitadas para el lápiz. Y hacerlo es más fácil de lo que cree.

La entrada de lápiz hace referencia a la Windows permite interactuar directamente con un equipo mediante un lápiz. Se puede usar un lápiz para apuntar y también para gestos, entrada de texto simple y capturar ideas de forma libre en la entrada de lápiz digital.

El lápiz que se usa para la entrada tiene una punta fina y suave que admite apuntar, escribir o dibujar con precisión en la entrada de lápiz. El lápiz también puede tener un botón de lápiz opcional (que se usa para realizar clics con el botón derecho) y un borrador (que se usa para borrar la entrada de lápiz). La mayoría de los lápices admiten el puntero.

![figura de un lápiz típico ](images/inter-pen-image1.png)

Un lápiz típico.

Cuando se usa el lápiz para la escritura a mano, los trazos del usuario se pueden convertir en texto mediante el reconocimiento de escritura a mano. Los trazos se pueden conservar igual que se escribieron, con el reconocimiento realizado en segundo plano para admitir la búsqueda y la copia como texto. Estos trazos no convertidos se denominan lápiz digital.

![captura de pantalla de escritura a mano en una página de una nota ](images/inter-pen-image2.png)

Ejemplo de entrada de lápiz.

La mayoría Windows programas ya son fáciles de usar, ya que se puede usar un lápiz en lugar de un mouse, el lápiz funciona sin problemas para las tareas e interacciones más importantes y el programa responde a los gestos. Un programa se convierte en fácil de escribir a mano cuando ayuda con la entrada de texto escrito a mano. Un programa se habilita con lápiz cuando puede controlar la entrada de lápiz directamente, en lugar de requerir que los trazos de lápiz se traduzcan en texto o movimientos equivalentes del mouse. Esto permite a los usuarios escribir, dibujar y agregar comentarios en lápiz digital de alta calidad y flujo libre. La recopilación de lápiz es diferente de la recopilación de eventos del mouse, ya que la entrada de lápiz requiere una mayor resolución y una mayor frecuencia de muestreo, y también puede agregar matices con presión e inclinación. Para obtener información sobre cómo crear programas fáciles de escribir a mano y habilitados para lápiz, vea [Integración de entrada](/previous-versions/windows/desktop/ms700674(v=vs.85)) de lápiz [y texto mediante el lápiz](/previous-versions/windows/desktop/ms695501(v=vs.85)).

Al colocar un lápiz, hay menos necesidad de un cursor porque la sugerencia se representa a sí misma. Sin embargo, para la asistencia de destino, Windows proporciona un pequeño cursor de lápiz que indica la ubicación actual del lápiz. A diferencia del puntero del mouse que reemplaza, el cursor del lápiz no es necesario a menos que el lápiz esté cerca de la pantalla, por lo que desaparece después de unos segundos de inactividad para permitir una vista de información sin estructurar.

La mayoría de los programas compatibles con el lápiz admiten gestos. Un gesto es un movimiento rápido del lápiz en una pantalla que el equipo interpreta como un comando, en lugar de como movimiento del mouse, escritura o dibujo. Uno de los gestos más rápidos y fáciles de realizar es un gesto. Un gesto es un gesto sencillo que da como resultado navegación o un comando de edición. Los gestos de navegación incluyen arrastrar hacia arriba, arrastrar hacia abajo, moverse hacia atrás y avanzar, mientras que los gestos de edición incluyen copiar, pegar, deshacer y eliminar.

Todos los punteros excepto el puntero ocupado tienen una zona activa de un solo píxel que define la ubicación exacta de la pantalla del puntero. La zona de acceso directa determina qué objeto se ve afectado por la interacción. Los objetos definen una zona de accesoso, que es el área donde se considera que la zona de acceso es sobre el objeto. Normalmente, la zona de acceso rápido coincide con los bordes de un objeto, pero puede ser mayor para facilitar la interacción.

**Dado que un lápiz puede apuntar con más precisión que un dedo, si la interfaz de usuario funciona bien para la entrada táctil, también funcionará bien para un lápiz.** Por lo tanto, este artículo se centra principalmente en agregar compatibilidad con lápiz a programas que ya se han diseñado para la función táctil.

**Nota:** Las directrices relacionadas [con el mouse,](inter-mouse.md) [la accesibilidad](inter-accessibility.md)y [la entrada](inter-touch.md) táctil se presentan en artículos independientes.

## <a name="design-concepts"></a>Conceptos de diseño

El uso de un lápiz para la entrada tiene las siguientes características:

-   **Natural e intuitivo.** Todo el mundo sabe cómo apuntar y pulsar con un lápiz. Las interacciones de objetos están diseñadas para corresponder a cómo interactúan los usuarios con objetos en el mundo real de una manera coherente.
-   **Expresivo.** Los trazos de un lápiz son fáciles de controlar, lo que facilita la escritura, el dibujo, el dibujo, el dibujo y la anotación que hacerlo con un mouse.
-   **Más personal.** Del mismo modo que una nota o firma manuscrita es más personal que una con tipo, el uso de una nota o firma escrita a mano digitalmente también es más personal.
-   **Menos intrusivo.** El uso de un lápiz es silencioso y, por tanto, mucho menos distrae que escribir o hacer clic, especialmente en situaciones sociales como reuniones.
-   **Portátil.** Un equipo con una funcionalidad de lápiz puede ser más compacto porque la mayoría de las tareas se pueden completar sin teclado, mouse o touchpad. Puede ser más flexible porque no requiere una superficie de trabajo. Permite nuevos lugares y escenarios para usar un equipo.
-   **Directa e interesante.** El uso de un lápiz te hace sentir que estás interactuando directamente con los objetos de la pantalla, mientras que el uso de un mouse o un panel táctil siempre requiere que coordines los movimientos de las manos con movimientos de puntero en pantalla independientes que se sientan indirectos en comparación.

**Todos Windows programas deben tener una buena experiencia de lápiz.** Los usuarios deben poder realizar las tareas más importantes del programa de forma eficaz mediante un lápiz. Algunas tareas, como la escritura o la manipulación de píxeles detallada, no son adecuadas para un lápiz, pero al menos deben ser posibles.

Afortunadamente, si el programa ya está bien diseñado y es táctil, es fácil proporcionar una buena compatibilidad con lápiz. Para ello, un programa bien diseñado:

-   **Tiene una buena compatibilidad con el mouse.** Los controles interactivos tienen unas asequibilidades claras y visibles, y tienen estados de puntero para los comentarios de puntero. Los objetos tienen comportamientos estándar para las interacciones estándar del mouse (clic único y doble a la izquierda, clic con el botón derecho, arrastrar y mantener el mouse). La [forma del](inter-mouse.md) puntero cambia según corresponda para indicar el tipo de manipulación directa.
-   **Tiene una buena compatibilidad con el teclado.** El programa hace que los usuarios sean eficaces al proporcionar asignaciones de teclas de método abreviado estándar, especialmente para comandos de navegación y edición que también se pueden generar mediante gestos.
-   **Tiene controles lo suficientemente grandes como para tocar.** Los controles tienen un tamaño mínimo de 23 x 23 píxeles (D DLL de 13 x 13 unidades de diálogo) y los controles más usados son al menos \[ \] 40 x 40 píxeles (23 x 22 D DLL). Para evitar un comportamiento que no responde, no debe haber espacios pequeños entre los destinos en los que los elementos de la interfaz de usuario deben estar espaciados para que los destinos adyacentes toquen o tengan al menos 5 píxeles (3 D DLL) de espacio entre ellos.
-   **Es accesible.** Usa Microsoft Active Accessibility (MSAA) para proporcionar acceso mediante programación a la interfaz de usuario para tecnologías de asistencia. El programa responde adecuadamente a los cambios en el tema y las métricas del sistema.
-   Funciona bien y se ve bien **en 120 ppp (puntos** por pulgada), que es la resolución de pantalla predeterminada recomendada para equipos habilitados para lápiz.
-   **Usa controles comunes.** Los controles más comunes están diseñados para admitir una buena experiencia de lápiz. Si es necesario, el programa usa controles personalizados bien implementados que están diseñados para admitir la manipulación interactiva y la orientación fácil.
-   **Usa controles restringidos.** Cuando se diseñan para facilitar la selección de destino, los controles restringidos, como listas y controles deslizantes, pueden ser mejores que los controles sin restricciones, como los cuadros de texto, porque reducen la necesidad de entrada de texto.
-   **Proporciona los valores predeterminados adecuados.** El programa selecciona la opción más segura (para evitar la pérdida de datos o el acceso al sistema) y la opción más segura de forma predeterminada. Si la seguridad y la seguridad no son factores, el programa selecciona la opción más probable o cómoda, lo que elimina la interacción innecesaria.
-   **Proporciona la finalización automática de texto.** Proporciona una lista de los valores de entrada más probables o recientes para facilitar mucho la entrada de texto.

Desafortunadamente, lo contrario también es cierto si el programa no está bien diseñado, sus deficiencias serán especialmente obvias para los usuarios que usan un lápiz.

### <a name="model-for-pen-interaction"></a>Modelo para la interacción con el lápiz

Si no tiene experiencia con el uso de un lápiz, la mejor introducción es aprender haciendo esto. Obtenga un equipo habilitado para lápiz, coloque el mouse y el teclado a un lado y realice las tareas que normalmente se hacen con solo un lápiz. Asegúrese de probar los programas habilitados para lápiz, como Windows Journal, y los programas que no están habilitados para lápiz. Si tiene un tablet PC, experimente con mantenerla en diferentes posiciones, como en el regón, en una mesa o en los brazos mientras está de pie. Pruebe a usarlo en orientación vertical y horizontal, y sosteniendo el lápiz para escribir y solo para apuntar, en la mano izquierda y en la derecha.

A medida que experimente con el uso de un lápiz, descubrirá lo siguiente:

-   **Los controles pequeños son difíciles de usar.** El tamaño de los controles afecta en gran medida a la capacidad de interactuar de forma eficaz. Los controles de 10 x 10 píxeles funcionan razonablemente para un lápiz, pero los controles más grandes son incluso más cómodos de usar. Por ejemplo, [los controles de número](ctrl-spin-controls.md) (15 x 11 píxeles) son demasiado pequeños para usarlos fácilmente con un lápiz.
-   **La entrega es un factor.** En ocasiones, la mano cubre las cosas con las que puede que quiera ver o interactuar. Por ejemplo, para los menús contextuales de los usuarios con la derecha es difícil de usar si aparecen a la derecha del punto de clic, por lo que es mejor si aparecen a la izquierda. Windows permite a los usuarios indicar su entrega en el elemento del panel de control Configuración tablet PC.
-   **La localidad de las tareas ayuda.** Aunque puede mover el puntero a través de una pantalla de 14 pulgadas con un movimiento del mouse de 3 pulgadas, el uso de un lápiz requiere que mueva la mano hasta las 14 pulgadas. Mover repetidamente entre destinos que están muy separados puede ser tedioso, por lo que es mucho mejor mantener las interacciones de tareas dentro del intervalo de una mano de reposo siempre que sea posible. Los menús contextuales son cómodos porque no requieren ningún movimiento de la mano.
-   **La entrada de texto y la selección son difíciles.** La entrada de texto larga es especialmente difícil con un lápiz, por lo que la finalización automática y los valores de texto predeterminados aceptables pueden simplificar realmente las tareas. La selección de texto también puede ser bastante difícil, por lo que las tareas son más fáciles cuando no requieren una colocación precisa del cursor.
-   **Los destinos pequeños cerca del borde de la pantalla pueden ser muy difíciles de pulsar.** Algunos biseles de pantalla se sobresaliendo y algunas tecnologías de pantalla táctil son menos sensibles en los bordes, lo que dificulta el uso de los controles cerca del borde. Por ejemplo, los botones Minimizar, Maximizar/Restaurar y Cerrar de la barra de título pueden ser más difíciles de usar cuando se maximiza una ventana.

### <a name="control-location"></a>Ubicación del control

La localidad de la tarea reduce los movimientos tediosos que se repiten entre pantallas. Para minimizar los movimientos de las manos, busque los controles cerca de donde es más probable que se van a usar.

**Incorrecto:**

![captura de pantalla de la paleta de colores separada de las herramientas ](images/inter-pen-image3.png)

En este ejemplo de Windows XP, la paleta de colores está demasiado lejos de donde es probable que se utilice.

Tenga en cuenta que la ubicación actual del usuario es la más cercana a un destino, lo que facilita la adquisición. Por lo tanto, los menús contextuales aprovechan al máximo la ley de [Fitts,](inter-mouse.md)al igual que las mini barras de herramientas que Microsoft Office.

![captura de pantalla de punteros cerca de menús ](images/inter-pen-image4.png)

La ubicación del puntero actual siempre es la más fácil de adquirir.

Los destinos pequeños cerca del borde de presentación pueden ser difíciles de dirigir, así que evite colocar controles pequeños cerca de los bordes de la ventana. Para asegurarse de que los controles son fáciles de dirigir cuando se maximiza una ventana, puede hacerlos al menos 23 x 23 píxeles (13 x 13 D DLL) o colocarlos fuera del borde de la ventana.

### <a name="pen-interactions"></a>Interacciones de lápiz

**Gestos del sistema**

Los gestos del sistema se definen y controlan mediante Windows. Como resultado, todos los Windows tienen acceso a ellos. Estos gestos tienen mensajes de comandos equivalentes del mouse, el teclado y la aplicación:



| Gesto del sistema                                                           | Mensaje equivalente sintetizado                                              |
|------------------------------------------------------------|-----------------------------------------------|
| Mantener el puntero (cuando se admite)<br/>                          | Mantener el mouse sobre el mouse<br/>                        |
| Pulsar (hacia abajo y hacia arriba)<br/>                               | Clic izquierdo del mouse<br/>                   |
| Pulsar dos veces (bajar y subir dos veces)<br/>                  | Doble clic izquierdo del mouse<br/>            |
| Mantenga presionada la tecla (abajo, pausa, arriba)<br/>                | Clic con el botón derecho del mouse<br/>                  |
| Arrastrar (bajar, mover, subir)<br/>                           | Arrastrar el mouse a la izquierda<br/>                    |
| Mantener presionado y arrastrar (abajo, pausar, mover, subir)<br/>   | Arrastrar con el mouse con el botón derecho<br/>                   |
| Seleccionar (hacia abajo, desplazarse sobre objetos seleccionables, hacia arriba)<br/> | Selección del mouse<br/>                       |



 

**Desarrolladores:** Para obtener más información, [vea SystemGesture Enumeration](/previous-versions/ms552724(v=vs.100)).

**Películas**

Los gestos son gestos sencillos que son aproximadamente el equivalente de los métodos abreviados de teclado. Los gestos de navegación incluyen arrastrar hacia arriba, arrastrar hacia abajo, moverse hacia atrás y avanzar. Los gestos de edición incluyen copiar, pegar, deshacer y eliminar. Para usar gestos, el programa solo necesita responder a los comandos de pulsaciones de teclas relacionados.

![Diagrama que muestra gestos de gestos de gestos y sus asignaciones predeterminadas en Windows 7.](images/inter-pen-image5.png)

Los ocho gestos de gestos de gestos y sus asignaciones predeterminadas en Windows 7. Los gestos de navegación se cambiaron para que se correspondan con el movimiento panorámico (donde el objeto se mueve con el gesto) en lugar de desplazarse (donde el objeto se mueve en la dirección opuesta del gesto).

![figura de gestos de gestos de movimiento, como el gesto de movimiento ](images/inter-pen-image6.png)

Los ocho gestos de gestos de gestos y sus asignaciones predeterminadas en Windows Vista.

Los gestos de navegación tienen una asignación natural, por lo que son fáciles de aprender y recordar. Los gestos de edición son diagonales que requieren más precisión y sus asignaciones no son tan naturales (avance hacia el papelera de reciclaje para eliminar, desenlace en la dirección de la flecha atrás para deshacer), por lo que no están habilitadas de forma predeterminada. Todas las acciones de gestos se pueden personalizar mediante el elemento del panel de control Lápiz y dispositivos de entrada.



| Película                                     | Mensaje equivalente sintetizado                                                            |
|--------------------------------------|-------------------------------------------------------------|
| Gesto a la izquierda<br/>                | Comando Reenviar (comando Atrás para Windows Vista)<br/> |
| Gesto a la derecha<br/>               | Comando Back (comando Forward para Windows Vista)<br/> |
| Movimiento hacia arriba<br/>                  | Desplazamiento del teclado hacia abajo<br/>                             |
| Deslice el dedo hacia abajo<br/>                | Desplazamiento del teclado hacia arriba<br/>                               |
| Gesto diagonal hacia arriba a la izquierda<br/>    | Eliminación de teclado<br/>                                  |
| Gesto diagonal hacia abajo a la izquierda<br/>  | Deshacer teclado<br/>                                    |
| Gesto diagonal hacia arriba a la derecha<br/>   | Copia de teclado<br/>                                    |
| Flecha abajo a la derecha diagonal<br/> | Pegar con el teclado<br/>                                   |



 

**Gestos de aplicación**

Las aplicaciones también pueden definir y controlar otros gestos. Microsoft Gesture Recognizer puede reconocer más de [40 gestos](../tablet/application-gestures-and-semantic-behavior.md). Para usar gestos de aplicación, el programa debe definir los gestos que reconoce y, a continuación, controlar los eventos resultantes.

**Capacidad de respuesta y coherencia**

**La capacidad de respuesta es esencial para crear experiencias de lápiz que se sientan directas y atractivas.** Para que se sientan directos, los gestos deben tener efecto inmediato y los puntos de contacto de un objeto deben permanecer debajo del lápiz sin problemas a lo largo del gesto. Cualquier retraso, respuesta desmesada, pérdida de contacto o resultados inexactos destruye la percepción de manipulación directa y también de calidad.

**La coherencia es esencial para crear experiencias de lápiz que se sientan naturales e intuitivas.** Una vez que los usuarios aprenden un gesto estándar, esperan que ese gesto tenga el mismo efecto en todos los programas aplicables. Para evitar confusiones y frustraciones, no asigne nunca significados no estándar a los gestos estándar. En su lugar, use gestos personalizados para interacciones exclusivas del programa.

**Edición de entrada de lápiz y texto**

La edición de entrada de lápiz y texto se encuentra entre las interacciones más difíciles al usar un lápiz. El uso de controles restringidos, los valores predeterminados adecuados y la finalización automática eliminan o reducen la necesidad de introducir texto. Pero si el programa implica editar texto o entrada de lápiz, puede hacer que los usuarios sean más productivos si amplía automáticamente la interfaz de usuario de entrada hasta un **150** % de forma predeterminada cuando se usa un lápiz.

Por ejemplo, un programa de correo electrónico podría mostrar la interfaz de usuario con un tamaño normal, pero acercar la interfaz de usuario de entrada al 150 % para redactar mensajes.

![captura de pantalla del mensaje de Outlook en una fuente grande ](images/inter-pen-image7.png)

En este ejemplo, la interfaz de usuario de entrada se acerca al 150 %.

**Si solo hace cuatro cosas...**

1.  1. Haga que Windows programas tengan una buena experiencia de lápiz. Los usuarios deben poder realizar las tareas más importantes del programa de forma eficaz mediante un lápiz (al menos aquellas tareas que no implican una gran cantidad de escritura o manipulación de píxeles detallada).
2.  2. Considere la posibilidad de agregar compatibilidad para escribir, dibujar y agregar comentarios directamente mediante la entrada de lápiz en los escenarios más relevantes.
3.  3. Para crear una experiencia directa y atractiva, haga que los gestos suenen efecto inmediatamente, mantenga los puntos de contacto bajo el lápiz del usuario sin problemas a lo largo del gesto y haga que el efecto del gesto se asigne directamente al movimiento del usuario.
4.  4. Para crear una experiencia natural e intuitiva, admita los gestos estándar adecuados y asígneles sus significados estándar. Use gestos personalizados para interacciones únicas del programa.

## <a name="guidelines"></a>Directrices

### <a name="control-usage"></a>Control del uso

-   **Prefiere usar controles comunes.** Los controles más comunes están diseñados para admitir una buena experiencia de lápiz.
-   **Prefiere controles restringidos.** Use controles restringidos como listas y controles deslizantes siempre que sea posible, en lugar de controles sin restricciones, como los cuadros de texto, para reducir la necesidad de entrada de texto.
-   **Proporcione los valores predeterminados adecuados.** Seleccione la opción más segura (para evitar la pérdida de datos o el acceso del sistema) y la opción más segura de forma predeterminada. Si la seguridad y la seguridad no son factores, seleccione la opción más probable o cómoda, lo que elimina la interacción innecesaria.
-   **Proporcione la finalización automática de texto.** Proporcione una lista de los valores de entrada más probables o recientes para que la entrada de texto sea mucho más fácil.
-   **En el caso de las tareas importantes que usan varias selecciones, si se usa normalmente una lista de selección múltiple estándar, proporcione una opción para usar una lista de casillas en su lugar.**
-   **Respetar las métricas del sistema.** Use las métricas del sistema para todos los tamaños y no los tamaños de cableado. Si es necesario, los usuarios pueden cambiar las métricas o ppp del sistema para adaptarse a sus necesidades. Sin embargo, trata esto como último recurso porque los usuarios normalmente no deben tener que ajustar la configuración del sistema para que la interfaz de usuario se pueda usar.

![captura de pantalla de menús con tamaño normal y grande ](images/inter-pen-image8.png)

En este ejemplo, se ha cambiado la métrica del sistema para el alto del menú.

### <a name="control-sizing-layout-and-spacing"></a>Control del tamaño, el diseño y el espaciado

-   **Para los controles comunes, use los tamaños de control recomendados.** Son lo suficientemente grandes como para una buena experiencia de lápiz, excepto para los controles de número (que no se pueden usar con un lápiz pero son redundantes).
-   **Elija un diseño que coloca los controles cerca de donde probablemente se van a usar.** Mantenga las interacciones de tareas dentro de un área pequeña siempre que sea posible. Evite los movimientos de mano de larga distancia, especialmente para tareas comunes y para arrastres.
-   **Use el espaciado recomendado.** El espaciado recomendado es descriptivo para el lápiz.
-   **Los controles interactivos deben tocarse o, preferiblemente, tener al menos 5 píxeles (3 D DLL) de espacio entre ellos.** Si lo hace, se evita la confusión cuando los usuarios pulsan fuera del destino previsto.
-   **Considere la posibilidad de agregar** más que el espaciado vertical recomendado dentro de grupos de controles, como vínculos de comandos, casillas y botones de radio, así como entre los grupos. Si lo hace, será más fácil diferenciarlos.

### <a name="interaction"></a>Interacción

-   **En el caso de los programas diseñados para aceptar escritura a mano, habilite la entrada manuscrita predeterminada.** La entrada de entrada de lápiz predeterminada permite a los usuarios simplemente empezar a escribir, sin tener que pulsar, dar un comando o hacer nada especial. Esto permite la experiencia más natural con un lápiz. Para los programas no diseñados para aceptar escritura a mano, controle la entrada de lápiz en los cuadros de texto como selección.
-   **Permitir a los usuarios acercar la interfaz de usuario de contenido** si el programa tiene tareas que requieren editar texto. Considere la posibilidad de acercarse automáticamente al 150 % cuando se usa un lápiz.
-   **Dado que los gestos se memorizan, asígneles significados coherentes entre programas.** No dé significados diferentes a los gestos con semántica fija. En su lugar, use un gesto específico del programa adecuado.

### <a name="handedness"></a>Imparcialidad

-   **Si una ventana es contextual, mostrarla siempre cerca del objeto desde el que se inició.** Colómelo fuera del camino para que la ventana no cubre el objeto de origen.
    -   Si se muestra con el mouse, cuando sea posible, coloque el desplazamiento de la ventana contextual hacia abajo y hacia la derecha.

        ![figura de la ventana contextual situada a la derecha del objeto ](images/inter-pen-image9.png)

        Mostrar ventanas contextuales cerca del objeto desde el que se inició.

    -   Si se muestra con un lápiz, siempre que sea posible, coloque la ventana contextual para que no esté cubierta por la mano del usuario. Para los usuarios con la derecha, se muestra a la izquierda; de lo contrario, se muestra a la derecha.

        ![figura de la ventana contextual situada a la izquierda del objeto ](images/inter-pen-image10.png)

        Cuando se usa un lápiz, también se muestran las ventanas contextuales para que no se cubren con la mano del usuario.

-   **Desarrolladores:** Puede distinguir entre eventos del mouse y eventos de lápiz mediante la API [GetMessageExtraInfo.](../tablet/system-events-and-mouse-messages.md) Puede determinar la entrega del [usuario](/previous-versions/ms819495(v=msdn.10)) mediante la API [SystemParametersInfo](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con SPI \_ GETMENUDROPALIGNMENT.

### <a name="forgiveness"></a>Perdón

-   **Proporcione un comando deshacer.** Idealmente, debe proporcionar deshacer para todos los comandos, pero el programa puede tener algunos comandos cuyo efecto no se puede deshacer.
-   **Proporcione comentarios positivos al mantener el puntero.** Indique claramente cuándo el lápiz está sobre un destino en el que se puede hacer clic. Estos comentarios son una excelente manera de evitar la manipulación accidental.
-   **Siempre que sea práctico, proporcione buenos comentarios sobre el lápiz hacia abajo, pero no tome medidas hasta que se mueva o suba un lápiz.** Esto permite a los usuarios corregir errores antes de hacerlo.
-   **Siempre que sea práctico, permita a los usuarios corregir errores fácilmente.** Si una acción tiene efecto en el lápiz hacia arriba, permita a los usuarios corregir errores si se deslizan mientras el lápiz sigue estando abajo.

## <a name="documentation"></a>Documentación

Al hacer referencia a la entrada de lápiz:

-   Consulte un dispositivo de entrada de lápiz en forma de lápiz como un lápiz. En la primera mención, use el lápiz de tableta.
-   Consulte el botón del lado de un lápiz como botón de lápiz, no como botón de botones.
-   Consulte genéricamente el teclado, el mouse, el trackball, el lápiz o el dedo como un dispositivo de entrada.
-   Use pulsar (y pulsar dos veces) en lugar de hacer clic al documentar procedimientos específicos del uso de un lápiz. Pulsar significa presionar la pantalla y, a continuación, elevar antes de un tiempo de espera. Se puede usar o no para generar un clic del mouse. Para las interacciones que no implican el lápiz, siga usando clic.

