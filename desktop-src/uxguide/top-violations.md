---
title: Lista de comprobación de la experiencia del usuario para aplicaciones de escritorio
description: Esta es una colección de algunas de las instrucciones importantes de la guía de la experiencia del usuario. Puede utilizarlo como una lista de comprobación para asegurarse de que la interfaz de usuario del programa obtiene estos elementos importantes a la derecha.
ms.assetid: 4705a807-5949-4957-8ea6-70871beaf8e0
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: d1006b7ad9de30941b6ceb4cc7282ec578450840
ms.sourcegitcommit: 8755905962e156f29203705d09d6df8b7d0e2fca
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/25/2021
ms.locfileid: "105709276"
---
# <a name="ux-checklist-for-desktop-applications"></a>Lista de comprobación de la experiencia del usuario para aplicaciones de escritorio

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Esta es una colección de algunas de las instrucciones importantes de la guía de la experiencia del usuario. Puede utilizarlo como una lista de comprobación para asegurarse de que la interfaz de usuario del programa obtiene estos elementos importantes a la derecha.

## <a name="windows"></a>Windows

-   **Admitir la resolución efectiva mínima de Windows de 800x600 píxeles.** En el caso de las interfaces de usuario (IUS) críticas que deben funcionar en modo seguro, admiten una [resolución efectiva](glossary.md) de 640x480 píxeles. Asegúrese de tener en cuenta el espacio que usa la barra de tareas mediante la reserva de 48 [píxeles relativos](glossary.md) verticales para las ventanas que se muestran con la barra de tareas.
-   **Optimice los diseños de ventana de tamaño variable para una resolución efectiva de 1024x768 píxeles.** Cambiar automáticamente el tamaño de estas ventanas para resoluciones de pantalla inferiores de una forma que sigue siendo funcional.
-   **Asegúrese de probar las ventanas en 96 puntos por pulgada (PPP) (a 800x600 píxeles), 120 ppp (a 1024x768 píxeles) y 144 ppp (en 1200x900 píxeles).** Compruebe si hay problemas de diseño, como el recorte de controles, texto y ventanas, y ajuste de iconos y mapas de bits.
-   **En el caso de los programas con escenarios táctiles y de uso móvil, optimice para 120 ppp.** Actualmente, las pantallas con un alto nivel de PPP están predominantes en PC táctiles y móviles.
-   **Si una ventana es propiedad, se muestra inicialmente "centrada" en la parte superior de la ventana propietaria.** Nunca por debajo. En el caso de las pantallas posteriores, considere la posibilidad de mostrarla en su última ubicación (relativa a la ventana propietaria) si es probable que sea más conveniente.
-   **Si una ventana es contextual, mostrarla siempre cerca del objeto desde el que se inició.** Sin embargo, colóquelo fuera del camino (preferiblemente desplazarse hacia abajo y a la derecha) para que el objeto no esté incluido en la ventana.

## <a name="layout"></a>Diseño

-   **Ajuste el tamaño de los controles y los paneles de una ventana para que coincidan con su contenido típico.** Evite el texto truncado y sus elipses asociadas. Los usuarios nunca deben tener que interactuar con una ventana para ver su contenido típico: Reserve el cambio de tamaño y el desplazamiento de contenido inusualmente grande. Compruebe específicamente:
    -   **Tamaños de control.** Ajuste el tamaño de los controles a su contenido típico, haciendo que los controles sean más amplios, más altos o de varias líneas si es necesario. Controles de tamaño para eliminar o reducir el desplazamiento en ventanas que tienen mucho espacio disponible. Además, nunca debería haber etiquetas truncadas o texto truncado en ventanas que tengan un espacio disponible. Sin embargo, para facilitar la lectura del texto, considere la posibilidad de limitar el ancho de línea a 65 caracteres.
    -   **Ancho de las columnas.** Asegúrese de que las columnas de la vista de lista tienen el valor predeterminado, el mínimo y el tamaño máximo adecuados. Elija los anchos de columna predeterminados de las vistas de lista que no producen texto truncado, especialmente si hay espacio disponible en la vista de lista.
    -   **Saldo del diseño.** El diseño de una ventana debe ser aproximadamente equilibrado. Si el diseño se siente pesado, considere la posibilidad de hacer que los controles sean más amplios y mover algunos controles más a la derecha.
    -   **Ajuste de tamaño del diseño.** Cuando se cambia el tamaño de una ventana y se truncan los datos, asegúrese de que los tamaños de ventana mayores muestren más datos. Cuando se truncan los datos, los usuarios esperan cambiar el tamaño de las ventanas para mostrar más información.
-   **Establezca un tamaño de ventana mínimo si hay un tamaño por debajo del cual ya no se puede usar el contenido.** En el caso de los controles de tamaño variable, establezca tamaños de elementos de tamaño mínimo ajustables en sus tamaños funcionales más pequeños, como el ancho mínimo de las columnas funcionales en las vistas de lista.

## <a name="text"></a>Texto

-   **Use los términos de conversación normales cuando sea posible.** Céntrese en los objetivos del usuario, no en la tecnología. Esto es especialmente eficaz si está explicando un concepto técnico complejo o una acción. Imagínese que miramos el hombro del usuario y explicamos cómo llevar a cabo la tarea.
-   **Ser educado, apoyarse y alentar.** El usuario no debe sentir nunca en el sentido de, culpado o intimidado.
-   **Quite el texto redundante.** Busque texto redundante en títulos de ventana, instrucciones principales, instrucciones adicionales, áreas de contenido, vínculos de comandos y botones de confirmación. Por lo general, deje texto completo en las instrucciones principales y los controles interactivos, y quite cualquier redundancia de los demás lugares.
-   **Use las mayúsculas y minúsculas del estilo de título para los títulos y el uso de mayúsculas para todos los demás elementos de la interfaz de usuario.** Hacerlo es más adecuado para el tono de Windows.
    -   **Excepción:** En el caso de las aplicaciones heredadas, puede usar el uso de mayúsculas de estilo de título para botones de comandos, menús y encabezados de columna si es necesario para evitar la combinación de estilos de capitalización.
-   **En el caso de los nombres de características y tecnologías, es conservador en mayúsculas.** Normalmente, solo los componentes principales deben escribirse en mayúsculas (mediante el uso de mayúsculas del estilo de título).
-   **En el caso de los nombres de características y tecnologías, sea coherente en mayúsculas.** Si el nombre aparece más de una vez en una pantalla de la interfaz de usuario, siempre debe aparecer de la misma manera. Del mismo modo, en todas las pantallas de la interfaz de usuario del programa, el nombre debe aparecer de forma coherente.
-   **No ponga en mayúsculas los nombres de los elementos genéricos de la interfaz de usuario, como la** barra de herramientas, el menú, la barra de desplazamiento, el botón y el icono.
    -   **Excepciones:** Barra de direcciones, barra de vínculos, cinta.
-   **No use todas las letras mayúsculas para las teclas del teclado.** En su lugar, siga las mayúsculas y minúsculas utilizadas por los teclados estándar, o en minúsculas si la tecla no está etiquetada en el teclado.
-   **Los puntos suspensivos significan incompletos.** Use puntos suspensivos en el texto de la interfaz de usuario de la siguiente manera:
    -   **Comandos.** Indicar que un comando necesita información adicional. No use puntos suspensivos cada vez que una acción muestre otra ventana, solo cuando se necesite información adicional. Los comandos cuyo verbo implícito es mostrar otra ventana no toman puntos suspensivos, como opciones avanzadas, ayuda, opciones, propiedades o configuraciones.
    -   **Data.** Indica que el texto se ha truncado.
    -   **Etiquetas.** Indicar que una tarea está en curso (por ejemplo, "buscando...").

**Sugerencia:** El texto truncado en una ventana o página con espacio sin usar indica un diseño deficiente o un tamaño de ventana predeterminado demasiado pequeño. Procuran los diseños y los tamaños de ventana predeterminados que eliminan o reducen la cantidad de texto truncado. Para obtener más información, vea [Diseño](vis-layout.md).

-   **No use texto azul que no sea un vínculo, ya que los usuarios pueden suponer que es un vínculo.** Utilice negrita o un sombreado de color gris en el que, de lo contrario, usaría texto coloreado.
-   **Use en negrita con moderación para atraer la atención a los usuarios de texto que deben leer.**
-   **Use la instrucción principal para explicar de manera concisa qué deben hacer los usuarios en una determinada ventana o página.** Las buenas instrucciones principales comunican el objetivo del usuario en lugar de centrarse simplemente en manipular la interfaz de usuario.
-   **Exprese la instrucción principal en forma de dirección imperativa o pregunta específica.**
-   **No coloque puntos al final de las etiquetas de control o las instrucciones principales.**
-   **Use un espacio entre oraciones.** No dos.

## <a name="controls"></a>Controles

-   **General**
    -   **Etiquete todos los controles o grupos de controles. Excepciones**
        -   Los cuadros de texto y las listas desplegables se pueden etiquetar mediante mensajes.
        -   Los controles subordinados utilizan la etiqueta de su control asociado. Los controles de número siempre son controles subordinados.
    -   **En todos los controles, seleccione el más seguro (para evitar la pérdida de datos o el acceso al sistema) y el valor más seguro de forma predeterminada.** Si seguridad y seguridad no son factores, seleccione el valor más probable o adecuado.
    -   **Prefiere controles restringidos.** Use controles restringidos como listas y controles deslizantes siempre que sea posible, en lugar de controles sin restricciones como cuadros de texto, para reducir la necesidad de entradas de texto.
    -   **Reconsidere los controles deshabilitados.** Los controles deshabilitados pueden ser difíciles de usar porque los usuarios literalmente tienen que deducir por qué están deshabilitados. Deshabilite un control cuando los usuarios esperan que se aplique y pueden deducir fácilmente por qué está deshabilitado el control. Quite el control cuando no haya ningún modo de que los usuarios lo habiliten o no espere que se aplique, o déjelo habilitado, pero proporcione un mensaje de error cuando se use incorrectamente.
        -   **Sugerencia:** Si no está seguro de si debe deshabilitar un control o proporcionar un mensaje de error, empiece por redactar el mensaje de error que puede proporcionar. Si el mensaje de error contiene información útil que no es probable que los usuarios de destino deduzcan rápidamente, deje habilitado el control y proporcione el error. De lo contrario, deshabilite el control.
-   **Botones de comando**
    -   **Prefiere etiquetas específicas sobre las genéricas.** Lo ideal es que los usuarios no tengan que leer nada más para entender la etiqueta. Es mucho más probable que los usuarios lean etiquetas de botón de comando que el texto estático.
        -   **Excepción:** No cambie el nombre del botón Cancelar si el significado de la cancelación no es ambiguo. Los usuarios no deben tener que leer todos los botones para determinar qué botón cancela una acción. Sin embargo, cambie el nombre de cancelar si no está claro qué acción se está cancelando, por ejemplo, cuando hay varias acciones pendientes.
    -   **Al formular una pregunta, use etiquetas que coincidan con la pregunta.** Por ejemplo, proporcione respuestas afirmativa y no a una pregunta sí o no.
    -   **No utilice los botones aplicar en los cuadros de diálogo que no son hojas de propiedades ni elementos del panel de control.** El botón aplicar significa aplicar los cambios pendientes, pero dejar la ventana abierta. Esto permite a los usuarios evaluar los cambios antes de cerrar la ventana. Sin embargo, solo las hojas de propiedades y los elementos del panel de control tienen esta necesidad.
    -   Etiquetar un botón Cancelar si la cancelación devuelve el entorno a su estado anterior (sin dejar ningún efecto secundario); de lo contrario, etiquete el botón Cerrar (si la operación ha finalizado) o deténgase (si la operación está en curso) para indicar que deja el estado actual cambiado intacto.
-   **Vínculos de comandos**
    -   **Siempre hay vínculos de comandos en un conjunto de dos o más.** Lógicamente, no hay ningún motivo para formular una pregunta con una sola respuesta.
    -   **Proporcione un botón Cancelar explícito.** No utilice un vínculo de comando con este fin. Con bastante frecuencia, los usuarios saben que no quieren realizar una tarea. El uso de un vínculo de comando para cancelar requeriría a los usuarios leer detenidamente todos los vínculos de comandos para determinar cuál de ellos es un medio para cancelar. Tener un botón Cancelar explícito permite a los usuarios cancelar una tarea de forma eficaz.
    -   **Si proporcionar un botón Cancelar explícito deja un solo vínculo de comando, proporcione un vínculo de comando para cancelar y un botón Cancelar.** Si lo hace, deja claro que los usuarios tienen la opción de elegir. Frase este vínculo de comando en términos de cómo difiere de la primera respuesta, en lugar de simplemente "Cancelar" o alguna variación.
-   **Casillas de \<item\> verificación "no volver a mostrar"**
    -   **Considere la posibilidad de usar una opción "no volver a mostrar \<item\> " para permitir que los usuarios supriman un cuadro de diálogo periódico, solo si no hay una alternativa mejor.** Es mejor Mostrar siempre el cuadro de diálogo si los usuarios lo necesitan realmente o simplemente eliminarlo si no lo necesitan.
    -   **Reemplazar \<item\> por el elemento específico.** Por ejemplo, no vuelva a mostrar este aviso. Al hacer referencia a un cuadro de diálogo en general, use no volver a mostrar este mensaje.
    -   **Indique claramente cuándo se usarán los datos proporcionados por el usuario para los valores predeterminados futuros** agregando la siguiente frase en la opción: las selecciones se usarán de forma predeterminada en el futuro.
    -   **No seleccione la opción de forma predeterminada. Si el cuadro de diálogo realmente debe mostrarse solo una vez, hágalo sin preguntar.** No use esta opción como excusa para molestar a los usuarios; Asegúrese de que el comportamiento predeterminado no sea molesto.
    -   **Si los usuarios seleccionan la opción y hacen clic en cancelar, esta opción surte efecto.** Esta opción es una meta, por lo que no sigue el comportamiento de cancelación estándar de no tener ningún efecto secundario. Tenga en cuenta que si los usuarios no quieren ver el cuadro de diálogo en el futuro, lo más probable es que deseen cancelarlo también.
-   **Vínculos**
    -   **No asigne una** [clave de acceso](glossary.md). Se tiene acceso a los vínculos mediante la tecla TAB.
    -   **No agregue "clic" o "haga clic aquí" al texto del vínculo.** No es necesario porque un vínculo implica hacer clic en.
-   **Información sobre herramientas**
    -   **Use la información sobre herramientas para proporcionar etiquetas para controles sin etiquetar.** No tiene que proporcionar información sobre herramientas de controles etiquetados simplemente para garantizar la coherencia.
    -   **La información sobre herramientas también puede proporcionar más información sobre los botones de la barra de herramientas con etiqueta si es útil hacerlo.** No basta con repetir o dar una redefinición de la palabra de lo que ya está en la etiqueta.
    -   **Evite abarcar el objeto con el que el usuario está a punto de ver o interactuar.** Coloque siempre la sugerencia en el lateral del objeto, incluso si esto requiere una separación entre el puntero y la punta. Cierta separación no supone un problema, siempre y cuando la relación entre el objeto y su sugerencia esté clara.
        -   **Excepción:** Información sobre herramientas de nombre completo utilizada en listas y árboles.
    -   **En el caso de las colecciones de elementos, evite abarcar el siguiente objeto con el que es probable que el usuario vea o interactúe.** En el caso de los elementos dispuestos horizontalmente, evite colocar sugerencias a la derecha; para los elementos organizados verticalmente, evite colocar sugerencias a continuación.
-   **Muestra progresiva**
    -   **Use más o menos botones de divulgación progresiva para ocultar las opciones, los comandos y los detalles de uso avanzado o poco frecuente que normalmente no necesitan los usuarios.** No oculte los elementos usados comúnmente, ya que es posible que los usuarios no los encuentren. Pero asegúrese de que el valor está oculto.
    -   Si la superficie muestra siempre algunas opciones, comandos o detalles, use los siguientes pares de etiquetas:
        -   **Más o menos opciones.** Se usa para las opciones o para una combinación de opciones, comandos y detalles.
        -   **Más o menos comandos.** Usar solo para comandos.
        -   **Más o menos detalles.** Se usa solo para información.
        -   **Más o menos \<object name\> .** Se usa para otros tipos de objetos, como las carpetas.
    -   De lo contrario:
        -   **Opciones de mostrar u ocultar.** Se usa para las opciones o para una combinación de opciones, comandos y detalles.
        -   **Mostrar u ocultar comandos.** Usar solo para comandos.
        -   **Mostrar u ocultar detalles.** Se usa solo para información.
        -   **Mostrar u ocultar \<object name\> .** Se usa para otros tipos de objetos, como las carpetas.
-   **Barras de progreso**
    -   **Use las barras de progreso de depuración para las operaciones que requieren una cantidad de tiempo limitada,** incluso si esa cantidad de tiempo no se puede predecir con precisión. Las barras de progreso indeterminadas muestran que se está realizando el progreso, pero no proporcionan ninguna otra información. No elija una barra de progreso indeterminada basada únicamente en la falta de precisión.
    -   **Proporcione una estimación de tiempo restante si puede hacerlo con precisión.** Las estimaciones de tiempo restantes que son exactas son útiles, pero las estimaciones que no son muy útiles para la marca o el rebote no resultan de gran utilidad. Es posible que deba realizar algún procesamiento antes de que pueda proporcionar estimaciones precisas. Si es así, no muestre estimaciones potencialmente inexactas durante este período inicial.
    -   **No reinicie el progreso.** Una barra de progreso pierde su valor si se reinicia (quizás porque se completa un paso de la operación) porque los usuarios no tienen forma de saber cuándo se completará la operación. En su lugar, haga que todos los pasos de la operación compartan una parte del progreso y que la barra de progreso vaya a finalización una vez.
    -   **Proporcione detalles de progreso útiles.** Proporcione información de progreso adicional, pero solo si los usuarios pueden hacer algo con ella. Asegúrese de que el texto se muestra el tiempo suficiente para que los usuarios puedan leerlo.
    -   **No combine una barra de progreso con un puntero ocupado.** Use uno u otro, pero no ambos al mismo tiempo.
-   **Mensajes**
    -   **Use un símbolo del sistema cuando el espacio de la pantalla sea tan importante que el uso de una etiqueta o instrucción no sea el deseado,** como en una barra de herramientas.
    -   **El mensaje es principalmente para identificar el propósito del cuadro de texto o el cuadro combinado de una manera compacta.** No debe ser información fundamental que el usuario necesite ver mientras usa el control.
    -   **El texto del mensaje no se debe confundir con el texto real.** Para hacerlo:
        -   Dibuje el texto del mensaje en cursiva en cursiva y el texto de entrada real en el negro romano.
        -   El texto del mensaje no se debe editar y debe desaparecer una vez que los usuarios hacen clic en o en la pestaña en el cuadro de texto.
            -   **Excepción:** Si el cuadro de texto tiene el foco de entrada predeterminado, se muestra el mensaje y desaparece cuando el usuario comienza a escribir.
    -   No use signos de puntuación o puntos suspensivos de finalización.
-   **Notificaciones**
    -   **Usar notificaciones para eventos que no están relacionados con la actividad del usuario actual, no requieren la intervención inmediata del usuario y los usuarios pueden ignorar libremente.**
    -   **No abuse de las notificaciones:**
        -   **Use las notificaciones solo si es necesario.** Cuando se muestra una notificación, puede interrumpir a los usuarios o incluso molestarles. Asegúrese de que la interrupción esté justificada.
        -   **Use notificaciones para eventos no críticos o situaciones que no requieran una acción inmediata del usuario.** Para eventos críticos o situaciones que requieran una acción inmediata del usuario, use un elemento de la interfaz de usuario alternativo (por ejemplo, un cuadro de diálogo modal).
        -   **No use notificaciones para anuncios de características.**

## <a name="keyboard"></a>Teclado

-   **Asigne el foco de entrada inicial al control en el que los usuarios tienen más probabilidades de interactuar primero,** que suele ser el primer control interactivo. Si el primer control interactivo no es una buena opción, considere la posibilidad de cambiar el diseño de la ventana.
-   **La asignación de tabulaciones se detiene en todos los controles interactivos, incluidos los cuadros de edición de solo lectura. Excepciones**
    -   Agrupar conjuntos de controles relacionados que se comportan como un solo control, como botones de radio. Estos grupos tienen una sola detención de tabulación.
    -   Contenga los grupos correctamente para que las teclas de flecha se reenvíen hacia delante y hacia atrás dentro del grupo y permanezcan dentro del grupo.
-   **El orden de tabulación debe fluir de izquierda a derecha y de arriba abajo.** Por lo general, el orden de tabulación debe seguir el orden de lectura. Considere la posibilidad de realizar excepciones para los controles de uso frecuente colocándolos antes en el orden de tabulación. La tabulación debe recorrer todas las tabulaciones en ambas direcciones sin detenerse. Dentro de un grupo, el orden de tabulación debe estar en orden secuencial, sin excepciones.
-   **Dentro de una detención de tabulación, el orden de las teclas de flecha debe fluir de izquierda a derecha, de arriba abajo,** sin excepciones. Las teclas de dirección deben recorrer todos los elementos en ambas direcciones sin detenerse.
-   **Presente los botones de confirmación en el orden siguiente:**
    -   Aceptar o \[ hacerlo \] /yes
    -   \[No lo haga \] /no
    -   Cancelar
    -   Aplicar (si existe)

en qué \[ \] consiste y no lo hacen, \[ \] son respuestas específicas a la instrucción principal.

-   **No confunda las claves de acceso con teclas de método abreviado.** Aunque tanto las teclas de acceso como las teclas de acceso directo proporcionan acceso de teclado a la interfaz de usuario, tienen distintos propósitos e instrucciones.
-   **Siempre que sea posible, asigne claves de acceso únicas a todos los controles interactivos o a sus etiquetas.** Los [cuadros de texto de solo lectura](ctrl-text-boxes.md) son controles interactivos (porque los usuarios pueden desplazarlos y copiar texto) para que se beneficien de las claves de acceso. **No asigne claves de acceso a:**
    -   Botones aceptar, cancelar y cerrar. ENTER y ESC se usan para sus claves de acceso. Sin embargo, asigne siempre una tecla de acceso a un control que signifique aceptar o cancelar, pero que tenga una etiqueta diferente.
-   **Asignar teclas de método abreviado a los comandos más usados.** Los programas y características usados con poca frecuencia no necesitan teclas de método abreviado, ya que los usuarios pueden utilizar las teclas de acceso en su lugar.
-   **No convierta una tecla de método abreviado en la única forma de realizar una tarea.** Los usuarios también deben poder usar el mouse o el teclado con las teclas de tabulación, de flecha y de acceso.
-   **No asigne diferentes significados a teclas de método abreviado conocidas.** Dado que se memorizan, los significados incoherentes para los accesos directos conocidos son frustrados y propensos a errores.
-   **No intente asignar teclas de método abreviado de todo el sistema.** Las teclas de método abreviado del programa solo surtirán efecto cuando el programa tenga el foco de entrada.

## <a name="mouse"></a>Mouse

-   **Nunca se requiere que los usuarios haga clic en un objeto para determinar si se pueden hacer clic.** Los usuarios deben poder determinar la posibilidad de hacer clic en la inspección visual por sí solo.
    -   La interfaz de usuario principal (por ejemplo, los botones de confirmación) debe tener un compromiso de clic estático. Los usuarios no deben tener que mantener el mouse para detectar la interfaz de usuario principal.
    -   La interfaz de usuario secundaria (como los comandos secundarios o los controles de divulgación progresiva) puede mostrar su prestación de clics al mantener el mouse.
    -   Los vínculos de texto deben sugerir de forma estática el texto del vínculo y, a continuación, mostrar su asequibilidad de clics (subrayado u otro cambio de presentación, con puntero a mano) al mantener el mouse.
    -   Los vínculos de gráficos solo muestran un puntero de mano al mantener el mouse.
-   **Use el puntero mano (o "seleccionar vínculo") solo para vínculos de texto y gráficos.** De lo contrario, los usuarios tendrían que hacer clic en los objetos para determinar si son vínculos.

## <a name="dialog-boxes"></a>Cuadros de diálogo

-   **Los cuadros de diálogo modales requieren interacción, por lo que deben usarse para los elementos a los que los usuarios deben responder antes de continuar con su tarea.** Asegúrese de que la interrupción esté justificada, como en el caso de las tareas de uso único críticas o poco frecuentes que requieren su finalización. En caso contrario, considere las alternativas no modales.
-   **Los cuadros de diálogo no modales no requieren interacción, por lo que deben usarse cuando los usuarios necesiten cambiar entre un cuadro de diálogo y la ventana propietaria.** Se usan mejor para tareas frecuentes, repetitivas o en curso. Sin embargo, las cintas de opciones, las barras de herramientas y las ventanas de paleta suelen ser alternativas mejores.

## <a name="property-sheets"></a>Hojas de propiedades

-   **Asegúrese de que las propiedades son necesarias.** No abarrota las páginas de propiedades con propiedades innecesarias solo para evitar tomar decisiones de diseño difíciles.
-   **Presente propiedades en términos de objetivos de usuario en lugar de tecnología.** El hecho de que una propiedad configure una tecnología específica no significa que deba presentar la propiedad en términos de esa tecnología.
    -   Si debe presentar la configuración en términos de tecnología (quizás porque los usuarios reconocen el nombre de la tecnología), incluya una breve descripción de las ventajas de los usuarios.
-   **Usar etiquetas de pestaña específicas y significativas.** Evite etiquetas de pestañas genéricas que se puedan aplicar a cualquier pestaña, como general, avanzada o configuración.
-   **Evite las páginas generales.** No es necesario tener una página general. Use una página general solo si:
    -   Las propiedades se aplican a varias tareas y son significativas para la mayoría de los usuarios. No ponga propiedades especializadas o avanzadas en una página general, pero puede hacer que sean accesibles a través de un botón de comando en la página general.
    -   Las propiedades no se ajustan a una categoría más específica. En su lugar, use ese nombre para la página.
-   **Evite las páginas avanzadas.** Use una página avanzada solo si:
    -   Las propiedades se aplican a tareas poco frecuentes y son significativas principalmente para los usuarios avanzados.
    -   Las propiedades no se ajustan a una categoría más específica. En su lugar, use ese nombre para la página.
-   **No use pestañas si una ventana de propiedades tiene una sola pestaña y no es extensible.** En su lugar, use un cuadro de diálogo normal con aceptar, cancelar y un botón opcional aplicar. Sin embargo, las ventanas de propiedades extensibles (que se pueden extender por terceros) deben usar pestañas.

## <a name="wizards"></a>Asistentes

-   **Considere las alternativas ligeras en primer lugar, como cuadros de diálogo, paneles de tareas o páginas individuales.** Los asistentes son una gran interfaz de usuario, que se usa mejor para tareas que se realizan con poca frecuencia. No tiene que usar asistentes; puede proporcionar información útil y ayuda en cualquier interfaz de usuario.
-   **Usar siguiente solo al avanzar a la página siguiente sin compromiso.** El avance a la página siguiente se considera un compromiso cuando su efecto no se puede deshacer haciendo clic en atrás o cancelar.
-   **Use atrás solo para corregir errores.** Además de corregir los errores, los usuarios no deben hacer clic en atrás para realizar el progreso en una tarea.
-   **Cuando los usuarios están confirmando una tarea, use un botón de confirmación que sea una respuesta específica a la instrucción principal (por ejemplo, imprimir, conectar o iniciar).** No use etiquetas genéricas como Next (que no implica ningún compromiso) o Finish (que no es específico) para confirmar una tarea. Las etiquetas de estos botones de confirmación deberían tener sentido por sí solos. Iniciar siempre etiquetas de botón de confirmación con un verbo. **Excepciones:**
    -   Use finalizar cuando las respuestas específicas sigan siendo genéricas, como guardar, seleccionar, elegir o obtener.
    -   Use finalizar para cambiar una configuración específica o una colección de valores de configuración.
-   **Use los vínculos de comandos solo para las opciones, no para los compromisos.** Los botones de confirmación específicos indican mucho mejor el compromiso que los vínculos de comandos de un asistente.
-   **Al usar vínculos de comandos, oculte el botón siguiente, pero deje el botón Cancelar.**
-   **Use cerrar para Follow-Up y páginas de finalización.** No use cancelar porque al cerrar la ventana no se descartarán los cambios ni las acciones realizadas en este momento. No utilice Done porque no es un verbo imperativo.
-   **No use "Wizard" en los nombres de los asistentes.** Por ejemplo, use "conectar a una red" en lugar del "Asistente para configuración de red". Sin embargo, es aceptable hacer referencia a los asistentes como asistentes. Por ejemplo: "si está configurando una red por primera vez, puede obtener ayuda mediante el Asistente para conectarse a una red".
-   **Conservar las selecciones del usuario a través de la navegación.** Por ejemplo, si el usuario realiza cambios, vuelve a hacer clic en atrás y, a continuación, se deben conservar los cambios. Los usuarios no esperan tener que volver a escribir los cambios a menos que elijan explícitamente borrarlos.

## <a name="wizard-pages"></a>Páginas del asistente

-   **Céntrese en la toma de decisiones eficaz.** Reduzca el número de páginas para centrarse en Essentials. Consolide páginas relacionadas y tome páginas opcionales fuera del flujo principal. Hacer que los usuarios haga clic en siguiente completamente a través del asistente puede parecer una buena experiencia al principio, pero si los usuarios nunca necesitan cambiar los valores predeterminados, es probable que las páginas no sean necesarias.
-   **No usar páginas de bienvenida: hace que la primera página sea funcional siempre que sea posible.** Use una página de Introducción opcional solo cuando:
    -   El asistente tiene requisitos previos que son necesarios para completar el asistente correctamente.
    -   Es posible que los usuarios no conozcan el propósito del asistente en función de la primera página de su elección y no haya espacio para una explicación más detallada.
    -   La instrucción principal para Introducción páginas es "antes de comenzar:".
-   **En las páginas en las que se pide a los usuarios que realicen elecciones, optimice los casos más probables.** Estos tipos de páginas deben presentar opciones reales, no solo instrucciones.
    -   Si no usa una página de Introducción, explique la finalidad del asistente en la parte superior de la primera página de opciones.
-   **Use las páginas de confirmación para que quede claro cuando los usuarios se confirman en la tarea.** Normalmente, la página de confirmación es la última página de opciones y el botón siguiente se reetiqueta para indicar la tarea que se confirma.
    -   No utilice páginas de resumen que resuman simplemente las selecciones anteriores del usuario, a menos que la tarea sea arriesgada (lo que implica seguridad, o pérdida de tiempo o dinero) o que los usuarios puedan no comprender sus selecciones y necesiten revisarlos.
-   **No utilice páginas de enhorabuena que no hagan nada, pero que finalice el asistente.** Si los resultados del asistente son evidentes para los usuarios, solo tiene que cerrar el asistente en el botón de confirmación final.
    -   Utilice Follow-Up páginas cuando haya tareas relacionadas que es probable que los usuarios realicen como seguimiento. Evite tareas de seguimiento conocidas, como "enviar un mensaje de correo electrónico".
    -   Use las páginas de finalización solo cuando los resultados no estén visibles y no haya una forma mejor de proporcionar comentarios para la finalización de tareas.
    -   Los asistentes que tienen páginas de progreso deben usar una página de finalización o Follow-Up página para indicar la finalización de la tarea. En el caso de las tareas de ejecución prolongada, cierre el asistente en la página confirmar y use las notificaciones para enviar comentarios.

## <a name="error-messages"></a>Mensajes de error

-   **No proporcione mensajes de error cuando no es probable que los usuarios realicen una acción o cambien su comportamiento** como resultado del mensaje. Si no hay ninguna acción que puedan llevar a cabo los usuarios, o si el problema no es significativo, suprima el mensaje de error.
-   **Siempre que sea posible, proponga una solución para que los usuarios puedan solucionar el problema.** Sin embargo, asegúrese de que es probable que la solución propuesta resuelva el problema. No malgaste el tiempo de los usuarios al sugerir soluciones posibles, pero improbables.
-   **Ser específico.** Evite el uso impreciso de palabras, como un error de sintaxis y una operación no válida. Proporcionan nombres, ubicaciones y valores específicos de los objetos implicados.
-   **No utilice frases que culpable al usuario o que implique un error del usuario.** Evite usar usted y su en la formulación. Aunque la voz activa suele ser preferida, use la voz pasiva cuando el usuario sea el sujeto y pueda sentirse culpable del error si se usara la voz activa.
-   **No utilice aceptar para los mensajes de error.** Los usuarios no ven los errores como correctos. Si el mensaje de error no tiene ninguna acción directa, utilice Close en su lugar.
-   **No use las siguientes palabras:**
    -   Error: error (use el problema en su lugar)
    -   No se pudo (no se puede usar en su lugar)
    -   No válido, no válido, malo (usar en su lugar el uso incorrecto o no es válido)
    -   Anular, eliminar, terminar (usar detener en su lugar)
    -   Catastrófico, fatal (usar en su lugar grave)

Estos términos son innecesarios y se oponen al tono de promoción de ventanas. En su lugar, un icono de error, [cuando se usa correctamente](vis-std-icons.md), comunica lo suficiente que hay un problema.

-   **No acompañe los mensajes de error con efectos sonoros.** Hacerlo es discordante e innecesario.

## <a name="warning-messages"></a>Mensajes de advertencia

-   **Las advertencias describen una condición que puede provocar un problema en el futuro.** Las advertencias no son errores ni preguntas, por lo que no formule frases como advertencias.
-   **No proporcione mensajes de advertencia cuando no es probable que los usuarios realicen una acción o cambien su comportamiento como resultado del mensaje.** Si no hay ninguna acción que puedan llevar a cabo los usuarios, o si la condición no es significativa, suprima el mensaje de advertencia.

## <a name="confirmations"></a>Confirmaciones

-   **No utilice confirmaciones innecesarias.** Usar confirmaciones solo cuando:
    -   Hay una razón clara de no continuar y una posibilidad razonable de que a veces los usuarios no lo hacen.
    -   La acción tiene consecuencias importantes o no se puede deshacer fácilmente.
    -   La acción tiene consecuencias de que los usuarios no sepan.
    -   Continuar con la acción requiere que los usuarios elijan que no tengan un valor predeterminado adecuado.
    -   Dado el contexto actual, es probable que los usuarios hayan realizado una acción por error.
-   **La frase se confirmará como una pregunta sí o no, y proporcionará respuestas sí o no.** A diferencia de otros tipos de cuadros de diálogo, las confirmaciones están diseñadas para evitar que los usuarios tomen decisiones rápidas. Si los usuarios no ponen a su respuesta, la confirmación no tiene ningún valor.

## <a name="icons"></a>Iconos

-   **Todos los iconos deben cumplir las** [directrices de iconos de estilo Aero](vis-icons.md). Reemplazar todos los iconos de estilo de Windows XP.
-   **Elija iconos estándar en función del tipo de mensaje, no la gravedad del problema subyacente:**
    -   **Error.** Un error o un problema que se ha producido.
    -   **Atención.** Una condición que puede provocar un problema en el futuro.
    -   **Informaciones.** Información útil.

Si un problema combina distintos tipos de mensajes, céntrese en el aspecto más importante en el que los usuarios necesitan actuar.

-   **Los iconos siempre deben coincidir con la instrucción principal u otro texto correspondiente.**
-   **No se necesitan iconos de error para los problemas de entradas de usuario no críticas.** Sin embargo, los iconos son necesarios para los errores en contexto, ya que, de lo contrario, los comentarios contextuales serían demasiado fáciles de pasar por alto.
-   **No use iconos de advertencia para "suavizar" los errores no críticos.** Los errores no son advertencias; en su lugar, aplique las instrucciones del icono de error.
-   **En el caso de los cuadros de diálogo de preguntas, use iconos de advertencia solo para preguntas con consecuencias significativas.** No use iconos de advertencia para preguntas rutinarias.

## <a name="help"></a>Ayuda

-   **Vínculo a temas de ayuda específicos y relevantes.** No vincular a la Página principal de la ayuda, la tabla de contenido, una lista de resultados de la búsqueda o una página que solo se vincula a otras páginas. Evite la vinculación a páginas estructuradas como una gran lista de preguntas más frecuentes, ya que obliga a los usuarios a buscar la que coincida con el vínculo en el que se hizo clic. No vincule a temas de ayuda específicos que no sean relevantes y útiles para la tarea a mano. No vincule nunca a páginas vacías.
-   **No coloque vínculos de ayuda en todas las ventanas o páginas para garantizar la coherencia.** Proporcionar un vínculo de ayuda en un lugar no significa que tenga que proporcionarlos en todas partes.
-   **Siempre que sea posible, la frase de ayuda vincula el texto en términos de la pregunta principal respondida por el contenido de la ayuda.** No use la frase "Obtenga más información acerca de" o "Obtenga ayuda con esto".
-   **Use el vínculo de ayuda completo para el texto del vínculo,** no solo las palabras clave.
-   **Use frases completas.**
-   **No use signos de puntuación o puntos suspensivos de finalización, excepto los signos de interrogación.**
-   **Si el contenido de la ayuda está en línea, desactívela en el texto del vínculo.** Al hacerlo, se facilita el resultado de la predicción de los vínculos.

