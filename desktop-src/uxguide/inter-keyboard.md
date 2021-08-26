---
title: Keyboard
description: El teclado es el dispositivo de entrada principal que se usa para la entrada de texto en Microsoft Windows. Para mejorar la accesibilidad y la eficacia, la mayoría de las acciones también se pueden realizar mediante el teclado.
ms.assetid: 27185c98-1233-4e26-a156-0ff080fd4db3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: bca6f1486b899881fbb0db8f9d7ae15ce3aba297db849c291862eb3b473730b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843223"
---
# <a name="keyboard"></a>Keyboard

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

El teclado es el dispositivo de entrada principal que se usa para la entrada de texto en Microsoft Windows. Para mejorar la accesibilidad y la eficacia, la mayoría de las acciones también se pueden realizar mediante el teclado.

Los teclados también pueden hacer referencia a teclados virtuales en pantalla y a blocs de escritura usados por equipos sin teclado físico, como equipos basados en tabletas.

![captura de pantalla del teclado en pantalla ](images/inter-keyboard-image1.png)

El Tecnología táctil y Tablet PC de Windows en pantalla.

![captura de pantalla del panel de escritura de tabletas windows ](images/inter-keyboard-image2.png)

Panel Tecnología táctil y Tablet PC de Windows escritura.

Hay seis tipos básicos de claves:

-   Una tecla de carácter envía un carácter literal a la ventana con el foco de entrada.
-   Una tecla modificadora combinada con otra tecla modifica el significado de su clave asociada, como Ctrl, Alt, Mayús y la tecla Windows logotipo.
-   Las teclas de navegación son las flechas direccionales, además de Inicio, Fin, Subir página y Bajar página.
-   Las claves de edición son Insert, Backspace y Delete.
-   Las claves de función son de F1 a F12.
-   Las claves del sistema ponen el sistema en modo o realizan una tarea del sistema, como Pantalla de impresión, Bloqueo de límites y Bloqueo numérico.

Las teclas de acceso son teclas o combinaciones de teclas que se usan para que la accesibilidad interactúe con todos los controles o elementos de menú mediante el teclado. Las teclas de método abreviado son claves o combinaciones de teclas que usan los usuarios avanzados para realizar comandos usados con frecuencia para mejorar la eficacia. Windows indica las claves de acceso mediante la asignación de la clave de acceso.

![captura de pantalla de las teclas de acceso y las teclas de método abreviado ](images/inter-keyboard-image3.png)

En este ejemplo se muestran las teclas de acceso y las teclas de método abreviado.

Para eliminar el desorden visual, Windows los subrayados de la tecla de acceso de forma predeterminada y los muestra solo cuando se presiona la tecla Alt. Para mantener la coherencia con Windows, las imágenes de la Guía de la experiencia de usuario también se muestran con los subrayados de la clave de acceso ocultos a menos que la directriz implique claves de acceso.

Para mejorar el conocimiento de las asignaciones de claves de acceso del programa a lo largo del proceso de desarrollo, puede mostrarlas en todo momento. En Panel de control, vaya a la Centro de accesibilidad y haga clic en Facilitar el uso **del teclado**; a continuación, active **la casilla Subrayado de los métodos abreviados de** teclado y las teclas de acceso.

**Nota:** Las directrices [relacionadas con la accesibilidad](inter-accessibility.md) se presentan en un artículo independiente.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="elements-of-keyboard-navigation"></a>Elementos de la navegación mediante el teclado

Los usuarios interactúan con una ventana mediante el teclado; para ello, navegan a los controles, realizan selecciones y realizan comandos. Los siguientes elementos funcionan conjuntamente para que esto suceda.

![captura de pantalla del cuadro de diálogo Editar colores ](images/inter-keyboard-image4.png)

Para ilustrar los elementos de la navegación con el teclado en la lista siguiente, haremos referencia a este cuadro de diálogo.

-   **Foco de entrada.** El control con el foco de entrada recibe la mayoría de las entradas del teclado. El foco de entrada se indica con un rectángulo de puntos denominado rectángulo de foco. Algunas entradas de teclado se envían a controles que no tienen el foco de entrada, como se explica más adelante.

    ![captura de pantalla de la primera fila en el cuadro de diálogo Editar colores ](images/inter-keyboard-image5.png)

    El primer control Colores básicos tiene el foco de entrada, como se indica con un rectángulo de puntos.

-   **Tecla de tabulación y tabulación se detienen.** La tecla Tab es el mecanismo principal para navegar dentro de una ventana. La tecla Tab solo visita los controles con una tabulación. Todos los controles interactivos deberían tener tabulaciones (a menos que estén en un grupo), todo lo contrario de los controles no interactivos, como las etiquetas.
-   **Orden de tabulación.** Todos los controles con tabulaciones se visitan en orden de tabulación. Al presionar Tab, se mueve el foco de entrada al siguiente control en orden de tabulación, mientras que al presionar Mayús+Tab se mueve el foco de entrada al control anterior.
-   **Grupos de controles.** Un conjunto de controles relacionados se puede convertir en un grupo y se le puede asignar una sola tabulación. Los grupos de controles se usan para conjuntos de controles que se comportan como un control único, como los botones de radio. También pueden usarse cuando hay demasiados controles para navegar de forma eficiente solo con la tecla Tab.

    ![captura de pantalla de grupos de colores básicos y personalizados ](images/inter-keyboard-image6.png)

    Los colores básicos y los colores personalizados son grupos de controles, lo que da a este cuadro de diálogo cinco tabulaciones. Hay tantos controles que la navegación sería ineficaz sin usar grupos de controles.

-   **Teclas de dirección.** Las teclas de dirección mueven el foco de entrada entre los controles de un grupo. Al presionar la tecla de flecha derecha, se mueve el foco de entrada al control siguiente en orden de tabulación, mientras que al presionar la flecha izquierda se mueve el foco de entrada al control anterior. Home, End, Up y Down también tienen su comportamiento esperado dentro de un grupo. Los usuarios no pueden salir de un grupo de control mediante teclas de dirección.
-   **Botones predeterminados.** Windows los botones de comando y los vínculos de comando tienen un único botón predeterminado indicado por un borde resaltado, que es el botón en el que se hace clic cuando se presiona la tecla Entrar. Hay un único botón de comando predeterminado o vínculo de comando asignado de forma predeterminada. Sin embargo, el botón predeterminado se mueve cuando el usuario ficha a otro botón de comando o vínculo de comando. Por lo tanto, cualquier botón de comando o vínculo de comando con el foco de entrada también es siempre el botón predeterminado.

    ![captura de pantalla de los botones Aceptar y Cancelar ](images/inter-keyboard-image7.png)

    Normalmente, el botón Aceptar es el predeterminado, como se indica en su borde resaltado. Sin embargo, si el usuario se tabulase en el botón Cancelar, se convertiría en el botón predeterminado y se activaría con la tecla Entrar.

-   **Teclas Barra espaciadora, Entrar y Esc.** La barra espaciadora activa el control con el foco de entrada, mientras que la tecla Entrar activa el botón predeterminado. Al presionar la tecla Esc, se cancela o se cierra la ventana.
-   **Claves de acceso.** Las claves de acceso se usan para interactuar directamente con los controles en lugar de navegar con tab. Se combinan con la tecla Alt y se indican con una letra subrayada en su etiqueta.
-   **Etiquetas de clave de acceso.** Aunque algunos controles contienen sus propias etiquetas, como botones de comando, casillas y botones de radio, otros controles tienen etiquetas externas, como cuadros de lista y vistas de árbol. En el caso de las etiquetas externas, la clave de acceso se asigna a la etiqueta y, si se invoca, navega al siguiente control en orden de tabulación. Los botones con las etiquetas Aceptar, Cancelar y Cerrar no tienen asignadas claves de acceso porque se invocan con Entrar y Esc.

    ![captura de pantalla de etiquetas con "b" y "d" subrayados ](images/inter-keyboard-image8.png)

    Al presionar Alt+B, se navega hasta el color básico seleccionado, al presionar Alt+D se hace clic en el botón Definir colores personalizados, Entrar invoca el botón Aceptar y Esc invoca Cancelar.

-   **Comportamiento de la clave de acceso.** Cuando se invoca una clave de acceso y se asigna de forma única, se hace clic en el control asociado. Si la asignación no es única, al control asociado se le asigna el foco de entrada. Si el usuario vuelve a tipos de la misma clave de acceso, se asigna el foco de entrada al siguiente control en orden de tabulación con la misma asignación.

Aunque este mecanismo es bastante complicado, también es bastante intuitivo. Los usuarios recogen la mayoría de estos detalles inmediatamente, aunque pocos puedan explicar exactamente cómo funcionan.

### <a name="keyboard-support-for-accessibility-and-advanced-users"></a>Compatibilidad con teclado para usuarios avanzados y de accesibilidad

**En Windows, el diseño para el teclado se reduce a proporcionar una navegación con el teclado bien diseñada, teclas de acceso para accesibilidad y teclas de método abreviado para usuarios avanzados.**

Para asegurarse de que la funcionalidad del programa está disponible fácilmente para la gama más amplia de usuarios, incluidos aquellos que tienen discapacidades y discapacidades, todos los elementos de la interfaz de usuario interactiva (UI) deben ser accesibles mediante el teclado. Por lo general, esto significa que los elementos de interfaz de usuario que se usan con más frecuencia son accesibles mediante una combinación de clave o clave de acceso única, mientras que los elementos usados con menos frecuencia pueden requerir navegación adicional por tabulación o tecla de flecha. Para estos usuarios, la exhaustividad es más importante que la coherencia.

Para asegurarse de que la funcionalidad del programa es eficaz para los usuarios experimentados, los elementos de interfaz de usuario usados habitualmente también deben tener teclas de método abreviado para el acceso directo al teclado. Los usuarios con experiencia suelen tener una fuerte preferencia por el teclado, ya que los comandos se pueden introducir más rápidamente y no requieran apartar las manos de las teclas. Para estos usuarios, la eficacia y la coherencia son cruciales; la exhaustividad es importante solo para los comandos usados con más frecuencia.

Hay distinciones sutiles al diseñar el acceso mediante teclado para estos dos grupos, por lo que Windows proporciona dos mecanismos de acceso directo al teclado independientes. Mediante el uso eficaz de teclas de acceso y acceso directo, puede proporcionar a los programas un acceso de teclado eficaz, coherente y completo que beneficia a todos los usuarios.

### <a name="access-keys"></a>Claves de acceso

Las teclas de acceso tienen las siguientes características:

-   Usan la tecla Alt y una tecla alfanumérica.
-   Son principalmente para la accesibilidad.
-   Se asignan a todos los menús y a la mayoría de los controles de cuadro de diálogo.
-   No se espera que se memoricen, por lo que se documentan directamente en la interfaz de usuario subrayando el carácter de etiqueta correspondiente.
-   Tienen efecto únicamente en la ventana actual y desplazan al control o elemento de menú correspondiente.
-   No se asignan de forma coherente porque no siempre es posible hacerlo. Sin embargo, las teclas de acceso deben asignarse de forma coherente para los comandos usados con frecuencia, especialmente los botones de confirmación.
-   Están traducidas.

Dado que las claves de acceso no están diseñadas para ser **memoriadas,** se asignan a un carácter que está al principio de la etiqueta para facilitar su búsqueda, incluso si hay una palabra clave que aparece más adelante en la etiqueta.

**Correcto:**

![captura de pantalla del primer carácter de la etiqueta subrayado ](images/inter-keyboard-image9.png)

**Incorrecto:**

![Captura de pantalla del vigésimo primer carácter subrayado ](images/inter-keyboard-image10.png)

En el ejemplo correcto, la clave de acceso se asigna a un carácter que está al principio de la etiqueta.

### <a name="shortcut-keys"></a>Teclas de método abreviado

Por el contrario, las teclas de método abreviado tienen las siguientes características:

-   Usan principalmente secuencias de Ctrl y teclas de función (las teclas de método abreviado del sistema de Windows usan también Alt + teclas no alfanuméricos y la tecla del logotipo de Windows).
-   Su fin principal es aumentar la eficiencia de los usuarios avanzados.
-   Se asignan únicamente a los comandos que más se usan.
-   Se espera que se memoricen y solo se documentan en los menús, en la información sobre herramientas y en la Ayuda.
-   Tienen efecto en todo el programa, pero no tienen efecto si no son de aplicación.
-   Se deben asignar de forma coherente porque se memorizan y no se documentan de forma directa.
-   No están traducidas.

Dado que las teclas de método abreviado están diseñadas para que se **memorizan,** lo ideal es que las teclas de método abreviado usadas con más frecuencia usen letras de los primeros caracteres o más fáciles de recordar dentro de las palabras clave del comando, como Ctrl+C para Copiar y Ctrl+Q para solicitud.

Los significados incoherentes de las teclas de método abreviado conocidas son frustrantes y provocan errores.

**Incorrecto:**

![captura de pantalla del botón hacia delante con "w" subrayado ](images/inter-keyboard-image11.png)

En este ejemplo, Ctrl+F es el acceso directo estándar para Buscar, por lo que asignarlo a Reenviar es frustrante y propenso a errores. Ctrl+W sería una opción mejor y fácil de recordar.

Por último, dado que están diseñadas para que se memoricen, las teclas de método abreviado específicas de la aplicación solo tienen sentido para los programas y características que se ejecutan con la frecuencia suficiente para que los usuarios motivados **memoricen.** Los programas y características usados con poca frecuencia no necesitan teclas de método abreviado. Por ejemplo, los programas de instalación y la mayoría de los asistentes no necesitan ninguna asignación de teclas de método abreviado especial ni comandos usados con poca frecuencia en una aplicación de productividad.

### <a name="assigning-access-keys-in-dialog-boxes"></a>Asignación de claves de acceso en cuadros de diálogo

Siempre que sea posible, asigne claves de acceso únicas a todos los controles interactivos, excepto a los que normalmente no se asignan claves de acceso. Sin embargo, en inglés solo hay 26 caracteres. Es posible que algunos caracteres no aparezcan en ninguna de las etiquetas y que no haya caracteres distintivos en todas las etiquetas, lo que reduce aún más este número. Además, debe planear tener algunos caracteres sin signo para facilitar la localización. Por lo tanto, solo puede asignar unas 20 claves de acceso únicas en un solo cuadro de diálogo.

Si tiene un cuadro de diálogo con más de 20 controles interactivos, no asigne claves de acceso a algunos controles o, en raras situaciones, asigne claves de acceso duplicadas.

![captura de pantalla del cuadro de diálogo de fuente ](images/inter-keyboard-image12.png)

Cuando hay muchos controles interactivos, no todos necesitan una clave de acceso asignada.

Use el siguiente procedimiento general para asignar claves de acceso:

-   En primer lugar, asigne las claves de acceso a los [botones de confirmación y](glossary.md) los vínculos de comandos. Use la tabla de asignaciones de claves de acceso estándar cuando se aplique; de lo contrario, use la primera letra de la primera palabra.
-   Omita los controles que no tienen asignadas claves de acceso.
-   Asigne claves de acceso únicas a los controles restantes (empezando por los usados con más frecuencia):
    -   Si es posible, asigne la clave de acceso según la tabla de asignaciones de claves de acceso estándar.
    -   De lo contrario:
        -   Prefiere los caracteres que aparecen al principio de la etiqueta, idealmente el primer carácter de la primera o segunda palabra.
        -   Prefiere una consonante distintiva o una voto, como "x" en "Exit".
        -   Prefiere caracteres con anchos anchos anchos, como w, m y letras mayúsculas.
        -   Evite el uso de caracteres que hagan que el subrayado sea difícil de ver, como letras de un píxel de ancho, letras con descendientes y letras junto a una letra con un descendiente.
-   Si no todos los controles pueden tener claves de acceso únicas (comience con la menor frecuencia de uso):
    -   Si hay grupos de controles relacionados, como:
        -   Un único conjunto de botones de radio
        -   Un conjunto de casillas relacionadas
        -   Un conjunto de controles relacionados dentro de un cuadro de grupo

Asigne claves de acceso a etiquetas de grupo en lugar de controles individuales. Normalmente, haría lo contrario. (Al hacerlo, asegúrese de que hay un grupo de controles definido para estos controles).

-   Si todavía no todos los controles pueden tener claves de acceso únicas:
    -   Puede asignar claves de acceso no únicas si:
        -   De lo contrario, los controles serían demasiado difíciles de navegar.
        -   Las claves de acceso no únicas no están en conflicto con las claves de acceso de los controles usados habitualmente.
    -   De lo contrario, se puede acceder a los controles restantes mediante la navegación con tabulación y tecla de dirección.

![captura de pantalla de grupos con diferentes claves de acceso ](images/inter-keyboard-image13.png)

En este ejemplo, hay controles repetitivos, por lo que las claves de acceso se asignan a los grupos de botones de radio.

### <a name="preventing-accidental-commands"></a>Prevención de comandos accidentales

Si una ventana mostrada fuera del contexto (no iniciada por el usuario) roba el foco de entrada, existe la posibilidad de que esta ventana reciba la entrada destinada a otra ventana. Además, las teclas de acceso tienen efecto cuando se presionan sin presionar la tecla Alt si el cuadro de diálogo no tiene ningún control que tome entrada de texto (por ejemplo, cuadros de texto y listas). Por lo tanto, en el ejemplo siguiente, al presionar "r", se activa el botón Reiniciar ahora.

Claramente, esta entrada puede tener consecuencias no intencionadas significativas.

**Incorrecto:**

![captura de pantalla del botón Reiniciar ahora, 'r' subrayado ](images/inter-keyboard-image14.png)

En este ejemplo, escribir texto con espacio, "r" o Entrar se reinicia accidentalmente Windows.

Por supuesto, la mejor solución a este problema es no robar el foco de entrada. En su lugar, puede flashear el botón de la barra de tareas [del programa](winenv-taskbar.md) o mostrar una notificación para obtener la atención del usuario.

Sin embargo, si debe mostrar este tipo de ventana, el mejor enfoque es no asignar un botón predeterminado o claves de acceso y dar el foco de entrada inicial a un control que no sea un botón de confirmación.

**Correcto:**

![captura de pantalla del botón de reinicio, "r" no subrayado ](images/inter-keyboard-image15.png)

En este ejemplo, reiniciar accidentalmente Windows es mucho más difícil de hacer.

**Si solo hace seis cosas...**

1.  Diseñe una buena navegación con el teclado, con un orden de tabulación razonable y grupos de control adecuados, foco de entrada inicial y botones predeterminados.
2.  Asigne claves de acceso a todos los menús y a la mayoría de los controles.
3.  Asigne las claves de acceso a un carácter que aparece al principio de la etiqueta para facilitar su detección.
4.  Asigne teclas de método abreviado a los comandos más usados.
5.  Intente asignar las teclas de método abreviado al primer o más fácil de recordar de las palabras clave.
6.  Proporcionar un significado coherente a las teclas de método abreviado conocidas.

## <a name="guidelines"></a>Directrices

### <a name="interaction"></a>Interacción

-   **No use la tecla Mayús para modificar comandos en menús o cuadros de diálogo.** Esto es inexploable e inesperado.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo Confirmar reemplazo de carpeta ](images/inter-keyboard-image16.png)

    En este ejemplo de Windows XP, mantener presionada la tecla Mayús reemplaza Sí a Todo por No a Todo.

-   **No deshabilite un control con el foco de entrada. Si lo hace, puede impedir que la ventana reciba la entrada del teclado.** En su lugar, antes de deshabilitar un control con el foco de entrada, mueva el foco de entrada a otro control.
-   **Si se muestra una ventana fuera de contexto, posiblemente sorprendente para los usuarios, es posible que tenga que evitar consecuencias significativas no intencionadas:**
    -   No asigne un botón predeterminado.
    -   No asigne claves de acceso.
    -   Dé el foco de entrada inicial a un control que no sea un botón de confirmación.

### <a name="keyboard-navigation"></a>Navegación mediante teclado

-   **Muestre siempre el indicador de foco de entrada. Excepción:** puede suprimir temporalmente el indicador de foco de entrada si:
    -   El indicador de foco de entrada es visualmente distraída (como con una vista de lista grande que no está en la vista Detalles).
    -   El uso de la tecla Entrar probablemente va precedido de otra entrada de teclado, como alt o teclas de dirección.
    -   El indicador de foco de entrada se muestra en cualquier entrada de teclado.
-   **Asigne el foco de entrada inicial al control** con el que es más probable que los usuarios interactúen primero, que suele ser el primer control interactivo. Si el primer control interactivo no es una buena opción, considere la posibilidad de cambiar el diseño de la ventana.
-   **Asignar tabulaciones se detiene a todos los controles interactivos, incluidos los cuadros de edición de solo lectura. Excepciones:**
    -   Agrupa conjuntos de controles relacionados que se comportan como un control único, como botones de radio. Estos grupos tienen una sola tabulación.
    -   Contenga correctamente grupos para que las teclas de dirección se desenvánten y retrocedas dentro del grupo y permanezcan dentro del grupo.
-   **El orden de tabulación debe seguir el orden de lectura, que generalmente fluye de izquierda a derecha, de arriba abajo.** Considere la posibilidad de realizar excepciones para los controles usados habitualmente, para lo que debe colocarlas anteriormente en el orden de tabulación. Tab debe recorrer todas las tabulaciones en ambas direcciones sin detenerse.
-   **Dentro de una tabulación, el orden de la** tecla de flecha debe fluir de izquierda a derecha, de arriba abajo, sin excepciones. Las teclas de dirección deben recorrer todos los elementos en ambas direcciones sin detenerse.
-   **Presente los botones de confirmación en el orden siguiente:**
    -   Ok/ \[ Do it \] /Yes
    -   \[Don't do it \] /No
    -   Cancelar
    -   Aplicar (si está presente)

donde \[ Hacerlo y No hacerlo son \] \[ \] respuestas específicas a la instrucción principal.

-   **Seleccione la opción más segura (para evitar la pérdida de datos o el acceso al sistema) y el botón de comando o el vínculo de comando más seguro para que sea el valor predeterminado.** Si la seguridad y la seguridad no son factores, seleccione la respuesta más probable o cómoda.
-   **La navegación con el teclado no debe cambiar los valores de control ni generar un mensaje de error.** No es necesario que los usuarios cambien el valor inicial de un control durante la navegación. En su lugar, inicialice controles que validen al salir con valores válidos y validen el valor de un control solo cuando haya cambiado.

### <a name="access-keys"></a>Claves de acceso

-   **Siempre que sea posible, asigne claves de acceso para los comandos usados habitualmente según la tabla siguiente.** Aunque las asignaciones de claves de acceso coherentes no siempre son posibles, ciertamente se prefieren especialmente para los comandos que se usan con frecuencia.

    |  Clave de acceso         | Get-Help                             |
    |---------------------------|-------------------------------------------|
    | A<br/>              | Acerca de<br/>                          |
    | A<br/>              | Siempre en la parte superior<br/>                  |
    | A<br/>              | Aplicar<br/>                          |
    | B<br/>              | Atrás<br/>                           |
    | B<br/>              | Negrita<br/>                           |
    | B o r<br/>         | Examinar<br/>                         |
    | C<br/>              | Cerrar<br/>                          |
    | C<br/>              | Copiar<br/>                           |
    | C<br/>              | Copiar aquí<br/>                      |
    | s<br/>              | Crear acceso directo<br/>                |
    | s<br/>              | Cree un acceso directo aquí.<br/>           |
    | t<br/>              | Cortar<br/>                            |
    | D<br/>              | Eliminar<br/>                         |
    | D<br/>              | No volver a mostrar este \[ \] elemento<br/> |
    | E<br/>              | Editar<br/>                           |
    | x<br/>              | Salir<br/>                           |
    | E<br/>              | Explorar<br/>                        |
    | F<br/>              | Menos<br/>                          |
    | F<br/>              | Archivo<br/>                           |
    | F<br/>              | Buscar<br/>                           |
    | n<br/>              | Buscar siguiente<br/>                      |
    | F<br/>              | Fuente<br/>                           |
    | F<br/>              | Adelante<br/>                        |
    | H<br/>              | Ayuda<br/>                           |
    | t<br/>              | Ayuda, temas<br/>                    |
    | H<br/>              | Ocultar<br/>                           |
    | I<br/>              | Insertar<br/>                         |
    | o<br/>              | insertar objeto<br/>                  |
    | I<br/>              | Cursiva<br/>                         |
    | L<br/>              | Vínculo aquí<br/>                      |
    | x<br/>              | Maximizar<br/>                       |
    | n<br/>              | Minimizar<br/>                       |
    | M<br/>              | Más<br/>                           |
    | M<br/>              | Move<br/>                           |
    | M<br/>              | Traslado aquí<br/>                      |
    | N<br/>              | Nuevo<br/>                            |
    | N<br/>              | Siguientes<br/>                           |
    | N<br/>              | No<br/>                             |
    | O<br/>              | Abrir<br/>                           |
    | w<br/>              | Abrir con<br/>                      |
    | O<br/>              | Opciones<br/>                        |
    | u<br/>              | Configurar página<br/>                     |
    | P<br/>              | Pegar<br/>                          |
    | l<br/>              | Pegar vínculo<br/>                     |
    | s<br/>              | Método abreviado de teclado<br/>                 |
    | s<br/>              | Pegar especial<br/>                  |
    | P<br/>              | Pausar<br/>                          |
    | P<br/>              | Reproducir<br/>                           |
    | P<br/>              | Impresión<br/>                          |
    | P<br/>              | Imprimir aquí<br/>                     |
    | r<br/>              | Propiedades<br/>                     |
    | R<br/>              | Rehacer<br/>                           |
    | R<br/>              | Repetir<br/>                         |
    | R<br/>              | Restauración<br/>                        |
    | R<br/>              | Reanudar<br/>                         |
    | R<br/>              | Volver a intentar<br/>                          |
    | R<br/>              | Ejecutar<br/>                            |
    | S<br/>              | Guardar<br/>                           |
    | a<br/>              | Guardar como<br/>                        |
    | a<br/>              | Seleccionar todo<br/>                     |
    | n<br/>              | Enviar a<br/>                        |
    | S<br/>              | Mostrar<br/>                           |
    | S<br/>              | Size<br/>                           |
    | p<br/>              | Dividir<br/>                          |
    | S<br/>              | Stop<br/>                           |
    | T<br/>              | Herramientas<br/>                          |
    | U<br/>              | Subrayado<br/>                      |
    | U<br/>              | Deshacer<br/>                           |
    | V<br/>              | Ver<br/>                           |
    | W<br/>              | Periodo<br/>                         |
    | Y<br/>              | Sí<br/>                            |

    

     

-   **Prefiere caracteres con ancho ancho ancho,** como w, m y letras mayúsculas.
-   **Prefiere una consonante distintiva o una voz,** como "x" en "Exit".
-   **Evite usar caracteres que hagan que el subrayado sea** difícil de ver, como (de más problemático a menos problemático):
    -   Caracteres que solo tienen un píxel de ancho, como i y l.
    -   Caracteres con descendientes, como g, j, p, q e y.
    -   Caracteres junto a una letra con un descendiente.
-   Al asignar claves de acceso en las páginas del asistente, no olvide reservar "B" para Atrás y "N" para Siguiente.
-   Al asignar claves de acceso en páginas de propiedades, recuerde reservar "A" para Aplicar, si se usa.

### <a name="menu-access-keys"></a>Teclas de acceso del menú

-   **Asigne claves de acceso a todos los elementos de menú.** Sin excepciones.
-   **Para los elementos de menú dinámicos (como los archivos usados recientemente), asigne claves de acceso numéricamente.**

    ![captura de pantalla de elementos de menú con claves de acceso numéricas ](images/inter-keyboard-image17.png)

    En este ejemplo, el programa Paint en Windows asigna claves de acceso numérico a los archivos usados recientemente.

-   **Asigne claves de acceso únicas dentro de un nivel de menú.** Puede reutilizar las claves de acceso en distintos niveles de menú.
-   **Facilitar la tarea de encontrar las claves de acceso:**
    -   Para los elementos de menú usados con más frecuencia, elija caracteres al principio de la primera o segunda palabra de la etiqueta, preferiblemente el primer carácter.
    -   Para los elementos de menú usados con menos frecuencia, elija letras que sean una consonante distintiva o una voto en la etiqueta.

### <a name="dialog-box-access-keys"></a>Claves de acceso del cuadro de diálogo

-   **Siempre que sea posible, asigne claves de acceso únicas a todos los controles interactivos o sus etiquetas.** [Los cuadros de texto de solo](ctrl-text-boxes.md) lectura son controles interactivos (porque los usuarios pueden desplazarlos y copiar texto), por lo que se benefician de las claves de acceso. **No asigne claves de acceso a:**
    -   **Botones Aceptar, Cancelar y Cerrar.** Escriba y Esc se usan para sus claves de acceso. Sin embargo, asigne siempre una clave de acceso a un control que significa Aceptar o Cancelar, pero tiene una etiqueta diferente.

        ![captura de pantalla del cuadro de diálogo con botones Sí y No ](images/inter-keyboard-image18.png)

        En este ejemplo, el botón de confirmación positiva tiene asignada una clave de acceso.

    -   **Etiquetas de grupo.** Normalmente, a los controles individuales dentro de un grupo se les asignan claves de acceso, por lo que la etiqueta de grupo no necesita una. Sin embargo, asigne una clave de acceso a la etiqueta de grupo y no a los controles individuales si hay escasez de claves de acceso.
    -   **Botones genéricos de Ayuda,** a los que se accede con F1.
    -   **Etiquetas de vínculo.** A menudo hay demasiados vínculos para asignar claves de acceso únicas y los caracteres de subrayado de vínculo ocultan los caracteres de subrayado de la clave de acceso. En su lugar, haga que los usuarios accedan a los vínculos con la tecla Tab.
    -   **Nombres de tabulación.** Las pestañas se ciclon mediante Ctrl+Tab y Ctrl+Mayús+Tab.
    -   **Botones examinar etiquetados como "...".** No se pueden asignar claves de acceso de forma única.
    -   **Controles sin etiquetar, como** controles de giro, botones de comandos gráficos y controles de divulgación progresiva sin etiquetar.
    -   **Texto estático sin etiqueta o etiquetas para controles que no son interactivos,** como barras de progreso.

-   **Asigne primero las claves de acceso del botón de confirmación para asegurarse de que tienen las asignaciones de claves estándar.** Si no hay una asignación de clave estándar, use la primera letra de la primera palabra. Por ejemplo, la clave de acceso para los botones de confirmación Sí y No siempre debe ser "Y" y "N", independientemente de los demás controles del cuadro de diálogo.
-   **Para los botones de confirmación negativos (distintos de Cancelar) con la frase "No", asigne la clave de acceso a la "n" en "No".** Si no se ha escrito como "No", use la asignación de clave de acceso estándar o asigne la primera letra de la primera palabra. Al hacerlo, todos los elementos No y No tienen una clave de acceso coherente.
-   Para facilitar la búsqueda de claves de acceso, asigne las claves de acceso a un carácter que aparezca al principio de la **etiqueta,** idealmente el primer carácter, incluso si hay una palabra clave que aparece más adelante en la etiqueta.
-   **Asigne como máximo 20 claves de acceso,** por lo que tiene algunos caracteres sin asignar para facilitar la localización.
-   **Si hay demasiados controles interactivos para asignar claves** de acceso únicas, puede asignar claves de acceso no únicas si:
    -   De lo contrario, los controles serían demasiado difíciles de navegar.
    -   Las claves de acceso no únicas no entra en conflicto con las claves de acceso de los controles usados habitualmente.
-   **No use barras de menús en los cuadros de diálogo.** En este caso, es difícil asignar claves de acceso únicas, ya que los controles de cuadro de diálogo y los elementos de menú comparten los mismos caracteres.

### <a name="shortcut-keys"></a>Teclas de método abreviado

-   **Asigne teclas de método abreviado a los comandos más usados.** Las características y programas usados con poca frecuencia no necesitan teclas de método abreviado, ya que los usuarios pueden usar claves de acceso en su lugar.
-   **No haga que una tecla de método abreviado sea la única manera de realizar una tarea.** Los usuarios también deben poder usar el mouse o el teclado con teclas de tabulación, flecha y acceso.
-   **No asigne significados diferentes a teclas de método abreviado conocidas.** Dado que se memorizan, los significados incoherentes de los accesos directos conocidos son frustrantes y propensos a errores.
-   **No intente asignar teclas de método abreviado de programa para todo el sistema.** Las teclas de método abreviado del programa solo tendrán efecto cuando el programa tenga el foco de entrada.
-   **Documente todas las teclas de método abreviado.** Métodos abreviados de documento en elementos de la barra de menús, información sobre herramientas de la barra de herramientas y un único artículo de Ayuda que documenta todas las teclas de método abreviado usadas. Esto ayuda a los usuarios a aprender las asignaciones de teclas de método abreviado que no deben ser un secreto.

    -   **Excepción:** No muestre asignaciones de teclas de método abreviado en los menús contextuales. Los menús contextuales no muestran las asignaciones de teclas de método abreviado porque estos menús están optimizados para mejorar la eficacia.

    ![captura de pantalla de información sobre herramientas para la tecla de método abreviado en negrita ](images/inter-keyboard-image19.png)

    La tecla de método abreviado se documenta en la información sobre herramientas.

-   **Si el programa asigna muchas teclas de método abreviado, proporcione la capacidad de personalizar las asignaciones.** Esto permite a los usuarios reasignar las teclas de método abreviado en conflicto y migrar desde otros productos. La mayoría de los programas no asignan suficientes teclas de método abreviado para necesitar esta característica.

### <a name="choosing-shortcut-keys"></a>Elección de teclas de método abreviado

-   **Para teclas de método abreviado conocidas, use las asignaciones estándar.**
-   **Para las asignaciones de claves no estándar, use las siguientes teclas de método abreviado recomendadas para los comandos que se usan con más frecuencia.** Estas teclas de método abreviado se recomiendan porque no entra en conflicto con los métodos abreviados conocidos y son fáciles de presionar.
    -   Ctrl+G, J, K, L M, Q, R o T
    -   Ctrl+cualquier número
    -   F7, F8, F9 o F12
    -   Mayús+F2, F3, F4, F5, F7, F8, F9, F11 o F12
    -   Alt+cualquier tecla de función excepto F4
-   **Use las siguientes teclas de método abreviado recomendadas para los comandos que se usan con menos frecuencia.** Estas teclas de método abreviado no tienen conflictos, pero son más difíciles de presionar que a menudo requieren dos manos.
    -   Ctrl+cualquier tecla de función excepto F4 y F6
    -   Ctrl+Mayús+cualquier letra o número
-   **Facilita el recordar las teclas de método abreviado que se usan con frecuencia:**
    -   Use letras en lugar de números o claves de función.
    -   Intente usar una letra que esté en la primera palabra o el carácter más fácil de recordar dentro de las palabras clave del comando.
-   **Use claves de función para los comandos que tienen un** efecto a pequeña escala, como los comandos que se aplican al objeto seleccionado. Por ejemplo, F2 cambia el nombre del elemento seleccionado.
-   **Use combinaciones de teclas Ctrl** para los comandos que tienen un efecto a gran escala, como los comandos que se aplican a todo un documento. Por ejemplo, Ctrl+S guarda el documento actual.
-   **Use combinaciones de teclas Mayús para los comandos que amplían o complementan las acciones de la tecla de método abreviado estándar.** Por ejemplo, la tecla de método abreviado Alt+Tab se desplaza a través de ventanas principales abiertas, mientras que Alt+Mayús+Tab se desplaza en orden inverso. De forma similar, F1 muestra Ayuda, mientras que Mayús+F1 muestra ayuda contextual.
-   **Al usar teclas de dirección para mover o cambiar el tamaño de un elemento, use Ctrl+teclas de dirección para un control más granular.**

### <a name="choosing-shortcut-keys-what-not-to-do"></a>Elegir teclas de método abreviado (qué no hacer)

-   **No distinga entre las ubicaciones clave.** Por ejemplo, Windows puede distinguir entre las teclas Mayús izquierda y derecha, Alt, Ctrl, [Windows logotipo](glossary.md)y Teclas de [aplicación,](glossary.md)así como las teclas del teclado numérico. Asignar un comportamiento a una sola ubicación de clave es confuso e inesperado.
-   **No use la tecla modificadora Windows logotipo para las teclas de método abreviado de programa.** Windows clave del logotipo está reservada para Windows uso. Incluso si Windows combinación de teclas de logotipo no se está utilizando en Windows, puede que sea en el futuro.
-   **No use la tecla Aplicación como modificador de tecla de método abreviado.** Use Ctrl, Alt y Mayús en su lugar.
-   **No use las teclas de método abreviado usadas por Windows teclas de método abreviado de programa.** Esto entra en conflicto con las teclas Windows del sistema cuando el programa tenga el foco de entrada.
-   **No use combinaciones de teclas Alt+alfanuméricas para las teclas de método abreviado.** Estas teclas de método abreviado pueden estar en conflicto con las claves de acceso.
-   **No use los caracteres siguientes para las teclas de** método abreviado: @ $ {} \[ \] \\  ~  \| ^ " < >. Estos caracteres requieren combinaciones de teclas diferentes entre idiomas o son específicos de la configuración regional.
-   **Evite combinaciones** de teclas complejas, como tres o más teclas juntas (por ejemplo: Ctrl+Alt+barra espaciadora) o teclas que están muy separadas en el teclado (por ejemplo: Ctrl+F5). Use teclas de método abreviado simples para los comandos usados con frecuencia.
-   **No use combinaciones Ctrl+Alt,** ya que Windows interpreta esta combinación en algunas versiones de lenguaje como una tecla AltGR, que genera caracteres alfanuméricos.

### <a name="keyboard-and-mouse-combinations"></a>Combinaciones de teclado y mouse

-   En el caso de los vínculos, use Mayús+clic para navegar por una nueva ventana y Ctrl+clic para navegar con una nueva pestaña. Este enfoque es coherente con Windows Internet Explorer .

## <a name="documentation"></a>Documentación

Al hacer referencia al teclado:

-   Use el teclado en pantalla para hacer referencia a una representación de teclado en la pantalla que el usuario toca a los caracteres de entrada.
-   Dé combinaciones de teclado a partir de la tecla modificadora. Presente las teclas modificadoras en el orden siguiente: Windows logotipo, Aplicación, Ctrl, Alt, Mayús. Si se usa el modificador Numpad, pónlo justo antes de la clave que modifica.
-   No use todas las letras mayúsculas para las teclas de teclado. En su lugar, siga la mayúscula que usan los teclados estándar o en minúsculas si la tecla no está etiquetada en el teclado.
    -   Para las combinaciones de teclas alfabéticas, use una letra mayúscula.
    -   Deletree Página arriba, Página abajo, Pantalla de impresión y Bloqueo de desplazamiento.
    -   Deletree más signo, signo menos, guion, punto y coma.
    -   Para las teclas de flecha, use flecha izquierda, flecha derecha, flecha arriba y flecha abajo. No use etiquetas gráficas para las teclas de dirección.
    -   Use Windows logotipo y clave de aplicación para hacer referencia a las claves etiquetadas con iconos. No use etiquetas gráficas para estas claves.

**Correcto:**

barra espaciadora, Tab, Entrar, Página arriba, Ctrl+Alt+Supr, Alt+W, Ctrl+signo más

**Incorrecto:**

BARRA ESPACIADORA, TAB, ENTRAR, PG UP, Ctrl+Alt+SUPR, Alt+w, Ctrl++

-   Indique combinaciones de teclas con un signo más, sin espacios.

**Correcto:**

Ctrl+A, Mayús+F5

**Incorrecto:**

Ctrl-A, Mayús + F5

-   Para mostrar una combinación de teclas que incluya signos de puntuación que requieran el uso de la tecla Mayús, como el signo de interrogación, agregue Mayús a la combinación y asigne el nombre o símbolo de la tecla mayús. El uso del nombre de la clave sin cambiar, como 4 en lugar de $, podría resultar confuso para los usuarios o incluso incorrecto. por ejemplo, ? Los caracteres y / no siempre se desplazan las teclas en todos los teclados.

**Correcto:**

Ctrl+Mayús+?, Ctrl+Mayús+ \* , Ctrl+Mayús+coma

**Incorrecto:**

Ctrl+Mayús+/, Ctrl+?, Ctrl+Mayús+8, Ctrl+\*

-   En la primera mención, use la clave y con el nombre de clave si es necesario para mayor claridad, por ejemplo, la clave F1. En todas las referencias posteriores, haga referencia a la tecla solo por su nombre, por ejemplo, presione F1.
-   Consulte específicamente las teclas de acceso y las teclas de método abreviado en la programación y otra documentación técnica. No use teclas de aceleración, mnemotécnicas ni de acceso rápido. En cualquier otro lugar se usa el método abreviado de teclado, especialmente en la documentación del usuario.

Al hacer referencia a la interacción:

-   Use press, not depress, strike, hit, or type (Presionar, no presionar, presionar o escribir) al presionar y liberar inmediatamente una tecla inicia una acción dentro del programa o navega dentro de un documento o interfaz de usuario.
-   Use el tipo , no escriba, para dirigir a los usuarios al texto de tipo.
-   Use use en situaciones en las que la pulsación puede resultar confusa, como al hacer referencia a un tipo de clave, como las teclas de dirección o las teclas de función. En tales casos, presionar podría hacer que los usuarios piensen que necesitan presionar todas las teclas simultáneamente.
-   Use mantener presionado al presionar y mantener presionada una tecla, como una tecla modificadora.
-   No use press como sinónimo de clic.

Ejemplos:

-   Escriba su nombre y presione Entrar.
-   Presione Ctrl+F y escriba el texto que desea buscar.
-   Para guardar el archivo, presione Y.
-   Para mover el punto de inserción, use las teclas de dirección.

 

