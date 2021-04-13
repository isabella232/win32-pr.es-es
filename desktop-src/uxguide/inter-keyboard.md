---
title: Teclado
description: El teclado es el dispositivo de entrada principal que se usa para la entrada de texto en Microsoft Windows. En cuanto a accesibilidad y eficacia, la mayoría de las acciones también se pueden realizar con el teclado.
ms.assetid: 27185c98-1233-4e26-a156-0ff080fd4db3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 4339dfd8d4d31d0d8859dcedd07fc287426b04c0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104564611"
---
# <a name="keyboard"></a>Teclado

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

El teclado es el dispositivo de entrada principal que se usa para la entrada de texto en Microsoft Windows. En cuanto a accesibilidad y eficacia, la mayoría de las acciones también se pueden realizar con el teclado.

Los teclados también pueden hacer referencia a teclados en pantalla y paneles de escritura utilizados por equipos sin un teclado físico, como equipos basados en Tablet PC.

![captura de pantalla del teclado en pantalla ](images/inter-keyboard-image1.png)

Teclado en pantalla de Tablet PC y tecnología táctil de Windows.

![captura de pantalla del panel de escritura de Tablet PC de Windows ](images/inter-keyboard-image2.png)

El panel de escritura de tecnología táctil y Tablet PC de Windows.

Hay seis tipos básicos de claves:

-   Una tecla de carácter envía un carácter literal a la ventana con el foco de entrada.
-   Una tecla modificadora combinada con otra clave altera el significado de su clave asociada, como Ctrl, Alt, Mayús y la tecla del logotipo de Windows.
-   Las teclas de navegación son las flechas direccionales, más Inicio, fin, re pág y Av Pág.
-   Las teclas de edición son INSERT, retroceso y eliminar.
-   Las teclas de función son F1 a F12.
-   Las claves del sistema ponen el sistema en modo de o realizan una tarea del sistema, como la pantalla de impresión, Bloq Mayús y Bloq Num.

Las claves de acceso son claves o combinaciones de teclas que se usan para que la accesibilidad interactúe con todos los controles o elementos de menú mediante el teclado. Las teclas de método abreviado son claves o combinaciones de teclas que usan los usuarios avanzados para obtener una mayor eficacia. Windows indica las teclas de acceso subrayando la asignación de la clave de acceso.

![captura de pantalla de teclas de acceso y teclas de método abreviado ](images/inter-keyboard-image3.png)

En este ejemplo se muestran las teclas de acceso y las teclas de acceso directo.

Para eliminar la confusión visual, Windows oculta las líneas de subrayado de la tecla de acceso de forma predeterminada y las muestra solo cuando se presiona la tecla Alt. Para mantener la coherencia con Windows, también se muestran las imágenes en la guía de la experiencia del usuario con la tecla de acceso subrayada, a menos que la instrucción implique claves de acceso.

Para mejorar el conocimiento de las asignaciones de teclas de acceso en el programa a lo largo del proceso de desarrollo, puede mostrarlas en todo momento. En el panel de control, vaya al centro de accesibilidad y haga clic en facilitar **el uso del teclado**; a continuación, active la casilla **subrayar métodos abreviados de teclado y teclas de acceso** .

**Nota:** Las instrucciones relacionadas con la [accesibilidad](inter-accessibility.md) se presentan en un artículo independiente.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="elements-of-keyboard-navigation"></a>Elementos de la navegación mediante el teclado

Los usuarios interactúan con una ventana mediante el teclado desplazándose hasta controles, realizando selecciones y realizando comandos. Los elementos siguientes funcionan juntos para que esto suceda.

![captura de pantalla del cuadro de diálogo Editar colores ](images/inter-keyboard-image4.png)

Para ilustrar los elementos de la navegación mediante el teclado en la lista siguiente, haremos referencia a este cuadro de diálogo.

-   **Foco de entrada.** El control con el foco de entrada recibe la mayoría de las entradas de teclado. El foco de entrada se indica con un rectángulo de puntos denominado rectángulo de foco. Algunas entradas de teclado se envían a los controles que no tienen el foco de entrada, como se explica más adelante.

    ![captura de pantalla de la primera fila en el cuadro de diálogo Editar colores ](images/inter-keyboard-image5.png)

    El primer control de colores básicos tiene el foco de entrada, como se indica con un rectángulo punteado.

-   **Tecla TAB y tabulaciones.** La tecla TAB es el mecanismo principal para desplazarse dentro de una ventana. La tecla TAB solo visita los controles con una tabulación. Todos los controles interactivos deberían tener tabulaciones (a menos que estén en un grupo), todo lo contrario de los controles no interactivos, como las etiquetas.
-   **Orden de tabulación.** Todos los controles con tabulaciones se visitan en el orden de tabulación. Al presionar Tab, se mueve el foco de entrada al siguiente control en el orden de tabulación, mientras que al presionar Mayús + Tab, se mueve el foco de entrada al control anterior.
-   **Grupos de control.** Se puede convertir un conjunto de controles relacionados en un grupo y asignarle una sola posición de tabulación. Los grupos de controles se usan para conjuntos de controles que se comportan como un control único, como los botones de radio. También pueden usarse cuando hay demasiados controles para navegar de forma eficiente solo con la tecla Tab.

    ![captura de pantalla de los grupos de colores básicos y personalizados ](images/inter-keyboard-image6.png)

    Los colores básicos y los colores personalizados son grupos de control, lo que permite que este cuadro de diálogo tenga cinco tabulaciones. Hay muchos controles que la navegación sería ineficaz sin usar grupos de control.

-   **Teclas de dirección.** Las teclas de dirección mueven el foco de entrada entre los controles de un grupo. Al presionar la tecla de flecha derecha, se mueve el foco de entrada al siguiente control en el orden de tabulación, mientras que al presionar la flecha izquierda, se mueve el foco de entrada al control anterior. Home, end, up y Down también tienen el comportamiento esperado dentro de un grupo. Los usuarios no pueden navegar fuera de un grupo de controles mediante las teclas de dirección.
-   **Botones predeterminados.** Las ventanas con los botones de comando y los vínculos de comandos tienen un solo botón predeterminado indicado por un borde resaltado, que es el botón en el que se hace clic cuando se presiona la tecla entrar. Hay un único vínculo de comando o botón de comando predeterminado asignado de forma predeterminada. Sin embargo, el botón predeterminado se mueve cuando el usuario se desplaza a otro botón de comando o vínculo de comando. Por consiguiente, cualquier botón de comando o vínculo de comando con el foco de entrada también es siempre el botón predeterminado.

    ![captura de pantalla de los botones aceptar y cancelar ](images/inter-keyboard-image7.png)

    El botón Aceptar es normalmente el botón predeterminado, como indica el borde resaltado. Sin embargo, si el usuario tuviera acceso al botón Cancelar, se convertiría en el botón predeterminado y se activaría con la tecla entrar.

-   **Teclas barra espaciadora, entrar y ESC.** La barra espaciadora activa el control con el foco de entrada, mientras que la tecla entrar activa el botón predeterminado. Al presionar la tecla ESC se cancela o se cierra la ventana.
-   **Claves de acceso.** Las claves de acceso se utilizan para interactuar con los controles directamente en lugar de desplazarse por la pestaña. Se combinan con la tecla Alt y se indican con una letra subrayada en la etiqueta.
-   **Etiquetas de clave de acceso.** Aunque algunos controles contienen sus propias etiquetas, como botones de comando, casillas y botones de radio, otros controles tienen etiquetas externas, como cuadros de lista y vistas de árbol. En el caso de las etiquetas externas, la clave de acceso se asigna a la etiqueta y, si se invoca, navega al siguiente control en el orden de tabulación. Los botones con la etiqueta aceptar, cancelar y cerrar no tienen asignadas claves de acceso porque se invocan con Enter y ESC.

    ![captura de pantalla de etiquetas con ' b ' y ' d ' subrayada ](images/inter-keyboard-image8.png)

    Si presiona Alt + B, navega al color básico seleccionado, al presionar Alt + D hace clic en el botón definir colores personalizados, entrar invoca el botón Aceptar y ESC invoca cancelar.

-   **Comportamiento de la tecla de acceso.** Cuando se invoca una tecla de acceso y se asigna de forma única, se hace clic en el control asociado. Si la asignación no es única, el control asociado recibe el foco de entrada. Si el usuario vuelve a escribir la misma clave de acceso, el control siguiente en el orden de tabulación con la misma asignación recibe el foco de entrada.

Aunque este mecanismo es bastante complicado, también es bastante intuitivo. Los usuarios obtienen la mayoría de estos detalles inmediatamente, aunque algunos pueden explicar exactamente cómo funcionan.

### <a name="keyboard-support-for-accessibility-and-advanced-users"></a>Compatibilidad con teclado para accesibilidad y usuarios avanzados

**En Windows, el diseño del teclado se reduce hasta proporcionar una navegación de teclado bien diseñada, teclas de acceso para accesibilidad y teclas de método abreviado para usuarios avanzados.**

Para asegurarse de que la funcionalidad del programa está disponible fácilmente para la gama más amplia de usuarios, incluidos los que tienen discapacidades e impedimentos, todos los elementos de la interfaz de usuario interactiva (IU) deben ser accesibles desde el teclado. Por lo general, esto significa que se puede acceder a los elementos de la interfaz de usuario más usados mediante una sola combinación de clave de acceso o clave, mientras que los elementos que se usan con menos frecuencia pueden requerir una navegación de tecla de dirección o de ficha adicional. Para estos usuarios, la exhaustividad es más importante que la coherencia.

Para asegurarse de que la funcionalidad del programa es eficaz para los usuarios experimentados, los elementos de interfaz de usuario utilizados habitualmente también deben tener teclas de método abreviado para el acceso directo al teclado. Los usuarios con experiencia suelen tener una fuerte preferencia por el teclado, ya que los comandos se pueden introducir más rápidamente y no requieran apartar las manos de las teclas. Para estos usuarios, la eficacia y la coherencia son cruciales; la exhaustividad es importante solo para los comandos usados con más frecuencia.

Hay sutiles diferencias al diseñar el acceso mediante teclado para estos dos grupos, por lo que Windows proporciona dos mecanismos independientes de acceso al teclado directo. Con el acceso y las teclas de método abreviado de forma eficaz, puede proporcionar a los programas un acceso de teclado eficaz, coherente y completo que beneficia a todo el mundo.

### <a name="access-keys"></a>Claves de acceso

Las teclas de acceso tienen las siguientes características:

-   Usan la tecla Alt y una tecla alfanumérica.
-   Son principalmente para la accesibilidad.
-   Se asignan a todos los menús y a la mayoría de los controles de cuadro de diálogo.
-   No se espera que se memoricen, por lo que se documentan directamente en la interfaz de usuario subrayando el carácter de etiqueta correspondiente.
-   Tienen efecto únicamente en la ventana actual y desplazan al control o elemento de menú correspondiente.
-   No se asignan de forma coherente porque no siempre es posible hacerlo. Sin embargo, las teclas de acceso deben asignarse de forma coherente para los comandos usados con frecuencia, especialmente los botones de confirmación.
-   Están traducidas.

**Dado que las claves de acceso no están pensadas para memorizarse, se asignan a un carácter que se encuentra al principio de la etiqueta para facilitar su búsqueda,** incluso si hay una palabra clave que aparece más adelante en la etiqueta.

**Correcto:**

![captura de pantalla del primer carácter de la etiqueta subrayada ](images/inter-keyboard-image9.png)

**Incorrecto:**

![captura de pantalla del primer carácter subrayado ](images/inter-keyboard-image10.png)

En el ejemplo correcto, la tecla de acceso se asigna a un carácter que se encuentra en la primera fase de la etiqueta.

### <a name="shortcut-keys"></a>Teclas de método abreviado

Por el contrario, las teclas de método abreviado tienen las siguientes características:

-   Usan principalmente secuencias de Ctrl y teclas de función (las teclas de método abreviado del sistema de Windows usan también Alt + teclas no alfanuméricos y la tecla del logotipo de Windows).
-   Su fin principal es aumentar la eficiencia de los usuarios avanzados.
-   Se asignan únicamente a los comandos que más se usan.
-   Se espera que se memoricen y solo se documentan en los menús, en la información sobre herramientas y en la Ayuda.
-   Tienen efecto en todo el programa, pero no tienen efecto si no son de aplicación.
-   Se deben asignar de forma coherente porque se memorizan y no se documentan de forma directa.
-   No están traducidas.

**Dado que las teclas de método abreviado están pensadas para memorizarlas, las teclas de método abreviado usadas con más frecuencia usan las letras de los caracteres primeros o más memorables en las palabras clave del comando,** como Ctrl + C para copiar y Ctrl + Q para la solicitud.

Los significados incoherentes de las teclas de método abreviado conocidas son frustrante y causan errores.

**Incorrecto:**

![captura de pantalla del botón adelante con ' w ' subrayada ](images/inter-keyboard-image11.png)

En este ejemplo, Ctrl + F es el método abreviado estándar para buscar, por lo que asignarlo a Forward es frustrante y propenso a errores. Ctrl + W sería una opción mejor y memorable.

Por último, dado que están diseñados para ser memorizados, **las teclas de método abreviado específicas de la aplicación solo tienen sentido para los programas y características que se ejecutan con la frecuencia suficiente para que los usuarios motivados lo hagan.** Los programas y características usados con poca frecuencia no necesitan teclas de método abreviado. Por ejemplo, los programas de instalación y la mayoría de los asistentes no necesitan ninguna asignación de teclas de método abreviado especial ni comandos usados con poca frecuencia en una aplicación de productividad.

### <a name="assigning-access-keys-in-dialog-boxes"></a>Asignar teclas de acceso en cuadros de diálogo

Siempre que sea posible, asigne claves de acceso únicas a todos los controles interactivos excepto a aquellos a los que normalmente no se les asignan claves de acceso. Sin embargo, en inglés, solo hay 26 caracteres. Es posible que algunos caracteres no aparezcan en ninguna de las etiquetas y que no haya caracteres distintivos en todas las etiquetas, lo que reduce aún más este número. Además, debe planear tener algunos caracteres sin asignar para facilitar la localización. Por lo tanto, solo puede asignar unas 20 claves de acceso únicas en un solo cuadro de diálogo.

Si tiene un cuadro de diálogo con más de 20 controles interactivos, no asigne claves de acceso a algunos controles o, en raras ocasiones, asigne claves de acceso duplicadas.

![captura de pantalla del cuadro de diálogo fuente ](images/inter-keyboard-image12.png)

Cuando hay muchos controles interactivos, no todos ellos necesitan una clave de acceso asignada.

Use el siguiente procedimiento general para asignar claves de acceso:

-   En primer lugar, asigne las claves de acceso a los [botones de confirmación](glossary.md) y a los vínculos de comandos. Use la tabla asignaciones de clave de acceso estándar cuando se aplique; de lo contrario, use la primera letra de la primera palabra.
-   Omitir los controles a los que no se les han asignado claves de acceso.
-   Asignar claves de acceso únicas a los controles restantes (empezando por la usada con más frecuencia):
    -   Si es posible, asigne la clave de acceso según la tabla asignaciones de claves de acceso estándar.
    -   De lo contrario:
        -   Prefiere los caracteres que aparecen al principio de la etiqueta, idealmente el primer carácter de la primera o la segunda palabra.
        -   Prefiere una consonante distintiva o una vocal, como "x" en "Exit".
        -   Prefiere caracteres con ancho ancho, como Letras de w, m y mayúsculas.
        -   Evite el uso de caracteres que hagan que el subrayado sea difícil de ver, como las letras de un píxel de ancho, las Letras con descendentes y las letras situadas al lado de una letra con un descendiente.
-   Si no todos los controles pueden tener claves de acceso únicas (comience con el menos usado):
    -   Si hay grupos de controles relacionados, como:
        -   Un único conjunto de botones de radio
        -   Un conjunto de casillas relacionadas
        -   Conjunto de controles relacionados dentro de un cuadro de grupo

Asigne las claves de acceso a las etiquetas de grupo en lugar de a los controles individuales. Normalmente, haría lo contrario. (Al hacerlo, asegúrese de que hay un grupo de controles definido para estos controles).

-   Si todavía no todos los controles pueden tener claves de acceso únicas:
    -   Puede asignar claves de acceso no únicas si:
        -   De lo contrario, los controles serían demasiado difíciles de navegar a.
        -   Las claves de acceso no únicas no entran en conflicto con las claves de acceso de los controles usados habitualmente.
    -   De lo contrario, se puede tener acceso a los controles restantes mediante la navegación por Tabulador y la tecla de dirección.

![captura de pantalla de grupos con claves de acceso diferentes ](images/inter-keyboard-image13.png)

En este ejemplo, hay controles repetitivos, por lo que las claves de acceso se asignan a los grupos de botones de radio.

### <a name="preventing-accidental-commands"></a>Prevención de comandos accidentales

Si una ventana que se muestra fuera del contexto (no iniciado por el usuario) roba el foco de entrada, existe la posibilidad de que esta ventana reciba la entrada destinada a otra ventana. Además, las teclas de acceso surten efecto cuando se presionan sin que se presione la tecla Alt si el cuadro de diálogo no tiene controles que tomen entradas de texto (como cuadros de texto y listas). Por lo tanto, en el ejemplo siguiente, al presionar "r" se activa el botón reiniciar ahora.

Claramente, tal entrada puede tener consecuencias imprevistas significativas.

**Incorrecto:**

![captura de pantalla del botón reiniciar ahora, ' r ' subrayado ](images/inter-keyboard-image14.png)

En este ejemplo, al escribir texto con espacio, "r", o al escribir accidentalmente, se reinician las ventanas.

Por supuesto, la mejor solución para este problema es no robar el foco de entrada. En su lugar, puede hacer parpadear el botón de la [barra de tareas](winenv-taskbar.md) del programa o mostrar una notificación para obtener la atención del usuario.

Sin embargo, si debe mostrar este tipo de ventana, el mejor enfoque es no asignar un botón o teclas de acceso predeterminados y proporcionar el foco de entrada inicial a un control que no sea un botón de confirmación.

**Correcto:**

![captura de pantalla del botón de reinicio, ' r ' no está subrayado ](images/inter-keyboard-image15.png)

En este ejemplo, el reinicio accidental de Windows es mucho más difícil.

**Si solo hace seis cosas...**

1.  Diseñar una navegación de teclado adecuada, con un orden de tabulación razonable y los grupos de control adecuados, el foco de entrada inicial y los botones predeterminados.
2.  Asignar teclas de acceso a todos los menús y la mayoría de los controles.
3.  Asigne las teclas de acceso a un carácter que aparece al principio de la etiqueta para facilitar su búsqueda.
4.  Asignar teclas de método abreviado a los comandos más usados.
5.  Intente asignar las teclas de método abreviado a los caracteres primeros o más memorables dentro de las palabras clave.
6.  Dé un significado coherente a las teclas de método abreviado conocidas.

## <a name="guidelines"></a>Directrices

### <a name="interaction"></a>Interacción

-   **No use la tecla Mayús para modificar comandos en menús o cuadros de diálogo.** De este modo, no se detecta ni se espera.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo confirmar reemplazo de carpeta ](images/inter-keyboard-image16.png)

    En este ejemplo de Windows XP, si se mantiene presionada la tecla Mayús, se sustituye el valor de sí a todo.

-   **No deshabilite un control con el foco de entrada. Si lo hace, puede impedir que la ventana reciba entradas de teclado.** En su lugar, antes de deshabilitar un control con el foco de entrada, mueva el foco de entrada a otro control.
-   **Si una ventana se muestra fuera de contexto, es posible que los usuarios sean sorprendentes, puede que necesite evitar consecuencias imprevistas significativas:**
    -   No asigne un botón predeterminado.
    -   No asigne claves de acceso.
    -   Proporcione el foco de entrada inicial a un control que no sea un botón de confirmación.

### <a name="keyboard-navigation"></a>Navegación con el teclado

-   **Mostrar siempre el indicador de foco de entrada. Excepción:** puede suprimir temporalmente el indicador de foco de entrada si:
    -   El indicador de foco de entrada se distrae visualmente (como con una vista de lista grande no en la vista de detalles).
    -   Es probable que el uso de la tecla entrar esté precedido por otra entrada del teclado, como Alt o las teclas de dirección.
    -   El indicador de foco de entrada se muestra en cualquier entrada del teclado.
-   **Asigne el foco de entrada inicial al control en el que los usuarios tienen más probabilidades de interactuar primero,** que suele ser el primer control interactivo. Si el primer control interactivo no es una buena opción, considere la posibilidad de cambiar el diseño de la ventana.
-   **La asignación de tabulaciones se detiene en todos los controles interactivos, incluidos los cuadros de edición de solo lectura. Excepciones**
    -   Agrupar conjuntos de controles relacionados que se comportan como un solo control, como botones de radio. Estos grupos tienen una sola detención de tabulación.
    -   Contenga los grupos correctamente para que las teclas de flecha se reenvíen hacia delante y hacia atrás dentro del grupo y permanezcan dentro del grupo.
-   **El orden de tabulación debe seguir el orden de lectura, que generalmente fluye de izquierda a derecha y de arriba abajo.** Considere la posibilidad de realizar excepciones para los controles de uso frecuente colocándolos antes en el orden de tabulación. La tabulación debe recorrer todas las tabulaciones en ambas direcciones sin detenerse.
-   **Dentro de una detención de tabulación, el orden de las teclas de flecha debe fluir de izquierda a derecha, de arriba abajo,** sin excepciones. Las teclas de dirección deben recorrer todos los elementos en ambas direcciones sin detenerse.
-   **Presente los botones de confirmación en el orden siguiente:**
    -   Aceptar o \[ hacerlo \] /yes
    -   \[No lo haga \] /no
    -   Cancelar
    -   Aplicar (si existe)

en qué \[ \] consiste y no lo hacen, \[ \] son respuestas específicas a la instrucción principal.

-   **Seleccione la opción más segura (para evitar la pérdida de datos o el acceso al sistema) y el botón de comando más seguro o el vínculo de comando para que sea el valor predeterminado.** Si seguridad y seguridad no son factores, seleccione la respuesta más probable o cómoda.
-   **La navegación mediante el teclado no debe cambiar los valores de control o producir un mensaje de error.** Nunca se requiere que los usuarios cambien el valor inicial de un control durante la navegación. En su lugar, inicialice los controles que validan al salir con valores válidos y validan el valor de un control solo cuando ha cambiado.

### <a name="access-keys"></a>Claves de acceso

-   **Siempre que sea posible, asigne claves de acceso para comandos de uso frecuente de acuerdo con la tabla siguiente.** Aunque las asignaciones de claves de acceso coherentes no siempre son posibles, se prefieren especialmente para los comandos que se usan con frecuencia.

    |                           |                                           |
    |---------------------------|-------------------------------------------|
    | **Clave de acceso**<br/> | **Comando**<br/>                    |
    | A<br/>              | Acerca de<br/>                          |
    | A<br/>              | Siempre visible<br/>                  |
    | A<br/>              | Aplicar<br/>                          |
    | B<br/>              | Atrás<br/>                           |
    | B<br/>              | Bold<br/>                           |
    | B o r<br/>         | Examinar<br/>                         |
    | C<br/>              | Cerrar<br/>                          |
    | C<br/>              | Copiar<br/>                           |
    | C<br/>              | Copiar aquí<br/>                      |
    | s<br/>              | Crear acceso directo<br/>                |
    | s<br/>              | Crear acceso directo aquí<br/>           |
    | t<br/>              | Cortar<br/>                            |
    | D<br/>              | Eliminar<br/>                         |
    | D<br/>              | No \[ volver a mostrar este elemento \]<br/> |
    | E<br/>              | Editar<br/>                           |
    | x<br/>              | Salir<br/>                           |
    | E<br/>              | Explorar<br/>                        |
    | F<br/>              | Menores<br/>                          |
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
    | M<br/>              | Desplace aquí<br/>                      |
    | N<br/>              | Nuevo<br/>                            |
    | N<br/>              | Siguientes<br/>                           |
    | N<br/>              | No<br/>                             |
    | O<br/>              | Abrir<br/>                           |
    | w<br/>              | Abrir con<br/>                      |
    | O<br/>              | Opciones<br/>                        |
    | u<br/>              | Configurar página<br/>                     |
    | P<br/>              | Pegar<br/>                          |
    | l<br/>              | Pegar vínculo<br/>                     |
    | s<br/>              | Pegar acceso directo<br/>                 |
    | s<br/>              | Pegado especial<br/>                  |
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
    | S<br/>              | Tamaño<br/>                           |
    | p<br/>              | Dividir<br/>                          |
    | S<br/>              | Stop<br/>                           |
    | T<br/>              | Herramientas<br/>                          |
    | U<br/>              | Subrayado<br/>                      |
    | U<br/>              | Deshacer<br/>                           |
    | V<br/>              | Ver<br/>                           |
    | W<br/>              | Periodo<br/>                         |
    | Y<br/>              | Sí<br/>                            |

    

     

-   **Prefiere caracteres con ancho ancho,** como w, m y mayúsculas.
-   **Prefiere una consonante distintiva o una vocal,** como "x" en "Exit".
-   **Evite el uso de caracteres que hagan que el subrayado sea difícil de ver,** como (desde la mayoría de los problemas a los menos problemáticos):
    -   Caracteres que solo tienen un píxel de ancho, como i y l.
    -   Caracteres con descendiente, como g, j, p, q e y.
    -   Caracteres situados junto a una letra con un descendiente.
-   Al asignar teclas de acceso en las páginas del asistente, recuerde reservar "B" para la parte posterior y "N" para el siguiente.
-   Al asignar las claves de acceso en las páginas de propiedades, recuerde reservar "A" para aplicar, si se usa.

### <a name="menu-access-keys"></a>Teclas de acceso de menú

-   **Asignar teclas de acceso a todos los elementos de menú.** Sin excepciones.
-   **Para los elementos de menú dinámicos (por ejemplo, los archivos usados recientemente), asigne claves de acceso numéricamente.**

    ![captura de pantalla de elementos de menú con claves de acceso numéricas ](images/inter-keyboard-image17.png)

    En este ejemplo, el programa Paint de Windows asigna claves de acceso numéricas a archivos usados recientemente.

-   **Asignar claves de acceso únicas dentro de un nivel de menú.** Puede reutilizar las claves de acceso en distintos niveles de menú.
-   **Facilite la búsqueda de las claves de acceso:**
    -   En el caso de los elementos de menú que se usan con más frecuencia, elija caracteres al principio de la primera o la segunda palabra de la etiqueta, preferiblemente el primer carácter.
    -   En el caso de los elementos de menú que se utilizan con menos frecuencia, seleccione las letras que son una consonante distintiva o una vocal en la etiqueta.

### <a name="dialog-box-access-keys"></a>Claves de acceso de cuadro de diálogo

-   **Siempre que sea posible, asigne claves de acceso únicas a todos los controles interactivos o a sus etiquetas.** Los [cuadros de texto de solo lectura](ctrl-text-boxes.md) son controles interactivos (porque los usuarios pueden desplazarlos y copiar texto) para que se beneficien de las claves de acceso. **No asigne claves de acceso a:**
    -   **Botones aceptar, cancelar y cerrar.** ENTER y ESC se usan para sus claves de acceso. Sin embargo, asigne siempre una tecla de acceso a un control que signifique aceptar o cancelar, pero que tenga una etiqueta diferente.

        ![captura de pantalla del cuadro de diálogo con los botones sí y no ](images/inter-keyboard-image18.png)

        En este ejemplo, el botón confirmación positivo tiene asignada una clave de acceso.

    -   **Etiquetas de grupo.** Normalmente, los controles individuales dentro de un grupo tienen asignadas claves de acceso, por lo que la etiqueta de grupo no necesita una. Sin embargo, asigne una clave de acceso a la etiqueta del grupo y no a los controles individuales si hay una escasez de claves de acceso.
    -   **Botones de ayuda genéricos,** a los que se tiene acceso con F1.
    -   **Etiquetas de vínculo.** A menudo hay demasiados vínculos para asignar claves de acceso únicas, y los subrayados de vínculo ocultan los guiones bajos de la tecla de acceso. Haga que los usuarios tengan acceso a los vínculos con la tecla TAB en su lugar.
    -   **Nombres de pestaña.** Las pestañas se recorren con Ctrl + Tab y Ctrl + Mayús + Tab.
    -   **Botones examinar etiquetados como "...".** No se les pueden asignar claves de acceso de forma única.
    -   **Controles sin etiqueta,** como controles de número, botones de comando gráficos y controles de divulgación progresiva sin etiquetar.
    -   **Etiquetas o texto estático sin etiqueta para los controles que no son interactivos,** como las barras de progreso.

-   **Asigne las claves de acceso del botón confirmar primero para asegurarse de que tienen las asignaciones de clave estándar.** Si no hay ninguna asignación de clave estándar, utilice la primera letra de la primera palabra. Por ejemplo, la tecla de acceso para los botones sí y no confirmar siempre debe ser "Y" y "N", independientemente de los otros controles del cuadro de diálogo.
-   **En el caso de los botones de confirmación negativos (que no sean cancelar) frase como "no", asigne la clave de acceso a la "n" en "no".** Si no tiene frase como "no", use la asignación de la clave de acceso estándar o asigne la primera letra de la primera palabra. Al hacerlo, todo no se realiza y no tiene una clave de acceso coherente.
-   Para facilitar la búsqueda de las **claves de acceso, asigne las teclas de acceso a un carácter que aparece al principio de la etiqueta,** idealmente el primer carácter, incluso si hay una palabra clave que aparece más adelante en la etiqueta.
-   **Asigne como máximo 20 claves de acceso,** de modo que tenga algunos caracteres sin asignar para facilitar la localización.
-   **Si hay demasiados controles interactivos para asignar claves de acceso únicas, puede asignar claves de acceso no únicas** si:
    -   De lo contrario, los controles serían demasiado difíciles de navegar a.
    -   Las claves de acceso no únicas no entran en conflicto con las claves de acceso de los controles usados habitualmente.
-   **No use barras de menús en los cuadros de diálogo.** En este caso, es difícil asignar claves de acceso únicas, ya que los controles de cuadro de diálogo y los elementos de menú comparten los mismos caracteres.

### <a name="shortcut-keys"></a>Teclas de método abreviado

-   **Asignar teclas de método abreviado a los comandos más usados.** Los programas y características usados con poca frecuencia no necesitan teclas de método abreviado, ya que los usuarios pueden utilizar las teclas de acceso en su lugar.
-   **No convierta una tecla de método abreviado en la única forma de realizar una tarea.** Los usuarios también deben poder usar el mouse o el teclado con las teclas de tabulación, de flecha y de acceso.
-   **No asigne diferentes significados a teclas de método abreviado conocidas.** Dado que se memorizan, los significados incoherentes para los accesos directos conocidos son frustrados y propensos a errores.
-   **No intente asignar teclas de método abreviado de todo el sistema.** Las teclas de método abreviado del programa solo surtirán efecto cuando el programa tenga el foco de entrada.
-   **Documente todas las teclas de método abreviado.** Accesos directos a documentos en elementos de barra de menús, información sobre herramientas de la barra de herramientas y un único artículo de ayuda que documente todas las teclas de método abreviado utilizadas. Esto ayuda a los usuarios a conocer las asignaciones de teclas de método abreviado que no deben ser secretas.

    -   **Excepción:** No muestre las asignaciones de teclas de método abreviado dentro de los menús contextuales. Los menús contextuales no muestran las asignaciones de teclas de método abreviado porque estos menús están optimizados para mayor eficacia.

    ![captura de pantalla de la tecla de método abreviado para negrita ](images/inter-keyboard-image19.png)

    La tecla de método abreviado se documenta en la información sobre herramientas.

-   **Si el programa asigna muchas teclas de método abreviado, proporcione la capacidad de personalizar las asignaciones.** Esto permite a los usuarios reasignar las teclas de método abreviado en conflicto y migrar desde otros productos. La mayoría de los programas no asignan suficientes teclas de método abreviado para necesitar esta característica.

### <a name="choosing-shortcut-keys"></a>Elegir teclas de método abreviado

-   **En el caso de las teclas de método abreviado conocidas, use las asignaciones estándar.**
-   **En el caso de las asignaciones de clave no estándar, use las siguientes teclas de método abreviado recomendadas para comandos de uso más frecuente.** Se recomiendan estas teclas de método abreviado porque no entran en conflicto con los métodos abreviados conocidos y son fáciles de presionar.
    -   Ctrl + G, J, K, L M, Q, R o T
    -   Ctrl + cualquier número
    -   F7, F8, F9 o F12
    -   Mayús + F2, F3, F4, F5, F7, F8, F9, F11 o F12
    -   Alt + cualquier tecla de función excepto F4
-   **Use las siguientes teclas de método abreviado recomendadas para los comandos usados con menos frecuencia.** Estas teclas de método abreviado no tienen conflictos, pero son más difíciles de presionar a menudo que requieren dos manos.
    -   Ctrl + cualquier tecla de función excepto F4 y F6
    -   Ctrl + Mayús + cualquier letra o número
-   **Facilite la recuerdo de las teclas de método abreviado usadas con frecuencia:**
    -   Use letras en lugar de números o teclas de función.
    -   Intente usar una letra que esté en la primera palabra o carácter más memorable dentro de las palabras clave del comando.
-   **Use las teclas de función para los comandos que tienen un efecto de pequeña escala,** como los comandos que se aplican al objeto seleccionado. Por ejemplo, F2 cambia el nombre del elemento seleccionado.
-   **Use combinaciones de teclas Ctrl para los comandos que tienen un efecto a gran escala,** como los comandos que se aplican a un documento completo. Por ejemplo, Ctrl + S guarda el documento actual.
-   **Use combinaciones de teclas Mayús para los comandos que extienden o complementan las acciones de la tecla de método abreviado estándar.** Por ejemplo, la tecla de método abreviado Alt + Tab recorre las ventanas principales abiertas, mientras que Alt + Mayús + Tab se desplaza en orden inverso. Del mismo modo, F1 muestra la ayuda, mientras que Mayús + F1 muestra la ayuda contextual.
-   **Al utilizar las teclas de dirección para desplace o cambiar el tamaño de un elemento, use Ctrl + teclas de dirección para un control más granular.**

### <a name="choosing-shortcut-keys-what-not-to-do"></a>Elegir teclas de método abreviado (lo que no hacer)

-   **No distinga entre las ubicaciones de las claves.** Por ejemplo, Windows puede distinguir entre el desplazamiento a la izquierda y a la derecha, Alt, Ctrl, el [logotipo de Windows](glossary.md)y [las teclas de aplicación](glossary.md), así como las teclas del teclado numérico. La asignación del comportamiento a una sola ubicación de clave es confusa e inesperada.
-   **No use la tecla modificador del logotipo de Windows para las teclas de método abreviado del programa.** La tecla del logotipo de Windows está reservada para su uso en Windows. Incluso si Windows no utiliza una combinación de teclas del logotipo de Windows, puede que esté en el futuro.
-   **No utilice la clave de aplicación como modificador de tecla de método abreviado.** Use Ctrl, Alt y Mayús en su lugar.
-   **No use teclas de método abreviado usadas por Windows para las teclas de método abreviado del programa.** Si lo hace, se producirá un conflicto con las teclas de método abreviado del sistema de Windows cuando el programa tenga el foco de entrada.
-   **No utilice las combinaciones de teclas Alt + alfanuméricas para las teclas de método abreviado.** Estas teclas de método abreviado pueden entrar en conflicto con las claves de acceso.
-   **No utilice los caracteres siguientes para las teclas de método abreviado:** @ $ {} \[ \] \\  ~  \| ^ '  < >. Estos caracteres requieren diferentes combinaciones de claves en los idiomas o son específicas de la configuración regional.
-   **Evite combinaciones de claves complejas,** como tres o más teclas juntas (por ejemplo, Ctrl + Alt + barra espaciadora) o teclas que estén lejos del teclado (por ejemplo: Ctrl + F5). Usar teclas de método abreviado simples para comandos de uso frecuente.
-   **No use las combinaciones CTRL + ALT,** ya que Windows interpreta esta combinación en algunas versiones de idioma como una clave AltGr, que genera caracteres alfanuméricos.

### <a name="keyboard-and-mouse-combinations"></a>Combinaciones de teclado y mouse

-   En el caso de los vínculos, use Mayús + clic para navegar mediante una nueva ventana y Ctrl + clic para navegar con una nueva pestaña. Este enfoque es coherente con Windows Internet Explorer.

## <a name="documentation"></a>Documentación

Al hacer referencia al teclado:

-   Use el teclado en pantalla para hacer referencia a una representación del teclado en la pantalla que el usuario toca a los caracteres de entrada.
-   Proporcione combinaciones de teclado a partir de la tecla modificadora. Presente las teclas modificadoras en el siguiente orden: logotipo de Windows, aplicación, Ctrl, Alt, Mayús. Si se usa el modificador de teclado, colóquelo justo antes de la clave modificada.
-   No use todas las letras mayúsculas para las teclas del teclado. En su lugar, siga las mayúsculas y minúsculas utilizadas por los teclados estándar, o en minúsculas si la tecla no está etiquetada en el teclado.
    -   En el caso de combinaciones de teclas alfabéticas, utilice una letra mayúscula.
    -   Deletrear Re Pág, Av Pág, Impr Pant y Bloq Despl.
    -   Deletrear signo más, signo menos, guión, punto y coma.
    -   Para las teclas de dirección, use flecha izquierda, flecha derecha, flecha arriba y flecha abajo. No use etiquetas gráficas para las teclas de dirección.
    -   Use la tecla del logotipo de Windows y la clave de aplicación para hacer referencia a las claves etiquetadas con iconos. No use etiquetas gráficas para estas claves.

**Correcto:**

barra espaciadora, Tab, entrar, Re Pág, Ctrl + Alt + Supr, Alt + W, Ctrl + signo más

**Incorrecto:**

BARRA ESPACIAdora, TAB, entrar, RePág, Ctrl + Alt + Supr, Alt + w, Ctrl + +

-   Indicar combinaciones de teclas con un signo más, sin espacios.

**Correcto:**

Ctrl + A, Mayús + F5

**Incorrecto:**

Ctrl-A, Mayús + F5

-   Para mostrar una combinación de teclas que incluya signos de puntuación que requieran el uso de la tecla Mayús, como el signo de interrogación, agregue Shift a la combinación y proporcione el nombre o el símbolo de la tecla desplazada. El uso del nombre de la clave no desplazada, como 4 en lugar de $, podría ser confuso para los usuarios o incluso mal. por ejemplo, el los caracteres y/no siempre son teclas desplazadas en todos los teclados.

**Correcto:**

Ctrl + Mayús +?, Ctrl + Mayús + \* , Ctrl + Mayús + coma

**Incorrecto:**

Ctrl + Mayús +/, Ctrl +?, Ctrl + Mayús + 8, Ctrl +\*

-   En la primera mención, use la clave and con el nombre de clave si es necesario para mayor claridad, por ejemplo, la tecla F1. En todas las referencias subsiguientes, haga referencia a la clave solo por su nombre, por ejemplo, presione F1.
-   Haga referencia específicamente a teclas de acceso y teclas de acceso directo en programación y otra documentación técnica. No use teclas de aceleración, de tecla de acceso o de acceso rápido. En todo el mundo, use el método abreviado de teclado, especialmente en la documentación de usuario.

Al hacer referencia a la interacción:

-   Use la acción de presionar, no presionar, tachar, presionar o escribir, cuando al presionar e iniciar inmediatamente una tecla se inicia una acción dentro del programa o se desplaza dentro de un documento o una interfaz de usuario.
-   Use Type, no Enter, para indicar a los usuarios que escriban texto.
-   Use en situaciones en las que la acción de presionar puede ser confusa, como cuando se hace referencia a un tipo de clave, como las teclas de dirección o las teclas de función. En tales casos, puede hacer que los usuarios piensen que necesitan presionar todas las claves simultáneamente.
-   Use la retención al presionar y mantener presionada una tecla, como una tecla modificadora.
-   No use Press como sinónimo de click.

Ejemplos:

-   Escriba su nombre y, a continuación, presione Entrar.
-   Presione Ctrl + F y, a continuación, escriba el texto que desea buscar.
-   Para guardar el archivo, presione Y.
-   Para desplace el punto de inserción, utilice las teclas de dirección.

 

