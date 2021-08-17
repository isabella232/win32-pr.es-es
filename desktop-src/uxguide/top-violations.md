---
title: Lista de comprobación de experiencia de usuario para aplicaciones de escritorio
description: Esta es una colección de algunas de las directrices importantes de la Guía de experiencia de usuario. Puede usarlo como una lista de comprobación para asegurarse de que la interfaz de usuario del programa obtiene estos elementos importantes correctamente.
ms.assetid: 4705a807-5949-4957-8ea6-70871beaf8e0
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 712b31a7a5166e41e590470aea48f60a1f159850da3ea6917b36ece9ada80fa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119332475"
---
# <a name="ux-checklist-for-desktop-applications"></a>Lista de comprobación de experiencia de usuario para aplicaciones de escritorio

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Esta es una colección de algunas de las directrices importantes de la Guía de experiencia de usuario. Puede usarlo como una lista de comprobación para asegurarse de que la interfaz de usuario del programa obtiene estos elementos importantes correctamente.

## <a name="windows"></a>Windows

-   **Admite la resolución Windows una resolución efectiva de 800 x 600 píxeles.** En el caso de las interfaces de usuario críticas (UI) que deben funcionar en modo seguro, admiten una resolución [efectiva](glossary.md) de 640 x 480 píxeles. Asegúrese de tener en cuenta el espacio utilizado por la barra de tareas reservando 48 píxeles [relativos](glossary.md) verticales para las ventanas mostradas con la barra de tareas.
-   **Optimice los diseños de ventana de tamaño ajustable para una resolución efectiva de 1024 x 768 píxeles.** Cambie automáticamente el tamaño de estas ventanas para obtener resoluciones de pantalla inferiores de forma que todavía sea funcional.
-   **Asegúrese de probar las ventanas en los modos de 96 puntos por pulgada (ppp) (a 800 x 600 píxeles), 120 ppp (a 1024 x 768 píxeles) y 144 ppp (a 1200 x 900 píxeles).** Compruebe si hay problemas de diseño, como el recorte de controles, texto y ventanas, y la extensión de iconos y mapas de bits.
-   **Para los programas con escenarios de uso táctil y móvil, optimice para 120 ppp.** Actualmente, las pantallas de valores altos de ppp son frecuentes en equipos táctiles y móviles.
-   **Si una ventana es de propiedad, inicialmente se muestra "centrada" en la parte superior de la ventana del propietario.** Nunca debajo. Para su posterior visualización, considere la posibilidad de mostrarla en su última ubicación (con respecto a la ventana de propietario) si es probable que sea más conveniente.
-   **Si una ventana es contextual, mostrarla siempre cerca del objeto desde el que se inició.** Sin embargo, colómela fuera del camino (preferiblemente desplazamiento hacia abajo y hacia la derecha) para que el objeto no esté cubierto por la ventana.

## <a name="layout"></a>Layout

-   **Controles de tamaño y paneles dentro de una ventana para que coincidan con su contenido típico.** Evite el texto truncado y sus puntos suspensivos asociados. Los usuarios nunca deben tener que interactuar con una ventana para ver su contenido típico: reservar cambiar el tamaño y desplazarse por contenido inusualmente grande. Compruebe específicamente:
    -   **Tamaños de control.** Cambiar el tamaño de los controles a su contenido típico, lo que hace que los controles sean más anchos, más altos o de varias líneas si es necesario. Controles de tamaño para eliminar o reducir el desplazamiento en ventanas que tienen mucho espacio disponible. Además, nunca debe haber etiquetas truncadas ni texto truncado dentro de ventanas que tengan mucho espacio disponible. Sin embargo, para facilitar la lectura del texto, considere la posibilidad de limitar los anchos de línea a 65 caracteres.
    -   **Anchos de columna.** Asegúrese de que las columnas de vista de lista tienen un tamaño predeterminado, mínimo y máximo adecuado. Elija los anchos de columna predeterminados de las vistas de lista que no darán lugar a texto truncado, especialmente si hay espacio disponible en la vista de lista.
    -   **Equilibrio de diseño.** El diseño de una ventana debe tener un equilibrio aproximado. Si el diseño se siente pesado a la izquierda, considere la posibilidad de ampliar los controles y mover algunos controles más a la derecha.
    -   **Cambio de tamaño del diseño.** Cuando una ventana se puede redimensionar y se truncan los datos, asegúrese de que los tamaños de ventana más grandes muestren más datos. Cuando se truncan los datos, los usuarios esperan cambiar el tamaño de las ventanas para mostrar más información.
-   **Establezca un tamaño mínimo de ventana si hay un tamaño por debajo del cual el contenido ya no se puede utilizar.** Para los controles que se pueden cambiar de tamaño, establezca los tamaños mínimos de elementos que se pueden cambiar de tamaño en sus tamaños funcionales más pequeños, como los anchos de columna funcionales mínimos en las vistas de lista.

## <a name="text"></a>Texto

-   **Use términos normales y conversacionales cuando pueda.** Céntrate en los objetivos del usuario, no en la tecnología. Esto es especialmente eficaz si se explica un concepto técnico complejo o una acción. Imagine a mirar el cuello del usuario y explicar cómo realizar la tarea.
-   **Ser atento, solidario y alentador.** El usuario nunca debe sentirse condescendido a, culpado o apenado.
-   **Quite el texto redundante.** Busque texto redundante en los títulos de la ventana, las instrucciones principales, las instrucciones complementarias, las áreas de contenido, los vínculos de comandos y los botones de confirmación. Por lo general, deje texto completo en las instrucciones principales y los controles interactivos, y quite cualquier redundancia de los demás lugares.
-   **Use mayúsculas de estilo de título para los títulos y mayúsculas de estilo oración para todos los demás elementos de la interfaz de usuario.** Hacerlo es más adecuado para el Windows de trabajo.
    -   **Excepción:** En el caso de las aplicaciones heredadas, puede usar mayúsculas de estilo de título para botones de comandos, menús y encabezados de columna si es necesario para evitar mezclar estilos de mayúsculas.
-   **Para los nombres de características y tecnologías, sea conservador en mayúsculas.** Normalmente, solo los componentes principales se deben incluir en mayúsculas (con mayúsculas de estilo de título).
-   **Para los nombres de características y tecnologías, sea coherente en mayúsculas.** Si el nombre aparece más de una vez en una pantalla de interfaz de usuario, siempre debería aparecer de la misma manera. Del mismo modo, en todas las pantallas de interfaz de usuario del programa, el nombre debe presentarse de forma coherente.
-   **No en mayúsculas los nombres** de los elementos genéricos de la interfaz de usuario, como la barra de herramientas, el menú, la barra de desplazamiento, el botón y el icono.
    -   **Excepciones:** Barra de direcciones, Barra de vínculos, cinta de opciones.
-   **No use todas las letras mayúsculas para las teclas de teclado.** En su lugar, siga la mayúscula que usan los teclados estándar o en minúsculas si la tecla no está etiquetada en el teclado.
-   **Los puntos suspensivos significan incompleta.** Use puntos suspensivos en el texto de la interfaz de usuario de la siguiente manera:
    -   **Comandos.** Indique que un comando necesita información adicional. No use puntos suspensivos siempre que una acción muestre otra ventana, solo cuando se requiera información adicional. Los comandos cuyo verbo implícito es mostrar otra ventana no toman puntos suspensivos, como Avanzado, Ayuda, Opciones, Propiedades o Configuración.
    -   **Datos.** Indique que el texto está truncado.
    -   **Etiquetas.** Indique que una tarea está en curso (por ejemplo, "Búsqueda...").

**Sugerencia:** El texto truncado en una ventana o página con espacio sin usar indica un diseño deficiente o un tamaño de ventana predeterminado demasiado pequeño. Procure diseños y tamaños de ventana predeterminados que eliminen o reduzcan la cantidad de texto truncado. Para obtener más información, vea [Diseño](vis-layout.md).

-   **No use texto azul que no sea un vínculo, ya que los usuarios pueden suponer que se trata de un vínculo.** Use negrita o un tono gris donde, de lo contrario, usaría texto coloreado.
-   **Use negrita con moderación para llamar la atención sobre el texto que los usuarios deben leer.**
-   **Use la instrucción principal para explicar concisamente qué deben hacer los usuarios en una ventana o página determinadas.** Las instrucciones principales buenas comunican el objetivo del usuario en lugar de centrarse solo en manipular la interfaz de usuario.
-   **Expresar la instrucción principal en forma de una dirección imperativa o una pregunta específica.**
-   **No coloque puntos al final de las etiquetas de control ni las instrucciones principales.**
-   **Use un espacio entre oraciones.** No dos.

## <a name="controls"></a>Controles

-   **General**
    -   **Etiquete cada control o grupo de controles. Excepciones:**
        -   Los cuadros de texto y las listas desplegables se pueden etiquetar mediante avisos.
        -   Los controles subordinados usan la etiqueta de su control asociado. Los controles de giro siempre son controles subordinados.
    -   **Para todos los controles, seleccione el valor más seguro (para evitar la pérdida de datos o el acceso del sistema), el valor más seguro de forma predeterminada.** Si la seguridad y la seguridad no son factores, seleccione el valor más probable o práctico.
    -   **Prefiere controles restringidos.** Use controles restringidos como listas y controles deslizantes siempre que sea posible, en lugar de controles sin restricciones, como los cuadros de texto, para reducir la necesidad de entrada de texto.
    -   **Controles deshabilitados Deserción.** Los controles deshabilitados pueden ser difíciles de usar porque los usuarios literalmente tienen que deducir por qué están deshabilitados. Deshabilite un control cuando los usuarios esperen que se aplique y puedan deducir fácilmente por qué el control está deshabilitado. Quite el control cuando no haya ninguna manera de que los usuarios lo habiliten o no esperen que se aplique, o déjelo habilitado, pero proporcione un mensaje de error cuando se utilice incorrectamente.
        -   **Sugerencia:** Si no está seguro de si debe deshabilitar un control o proporcionar un mensaje de error, empiece por crear el mensaje de error que podría proporcionar. Si el mensaje de error contiene información útil que es probable que los usuarios de destino no deduzcan rápidamente, deje el control habilitado y proporcione el error. De lo contrario, deshabilite el control .
-   **Botones de comando**
    -   **Prefiere etiquetas específicas sobre las genéricas.** Lo ideal es que los usuarios no tengan que leer nada más para comprender la etiqueta. Es mucho más probable que los usuarios lean las etiquetas del botón de comando que el texto estático.
        -   **Excepción:** No cambie el nombre del botón Cancelar si el significado de cancelar no es ambiguo. Los usuarios no deben tener que leer todos los botones para determinar qué botón cancela una acción. Sin embargo, cambie el nombre de Cancelar si no está claro qué acción se va a cancelar, por ejemplo, cuando hay varias acciones pendientes.
    -   **Al hacer una pregunta, use etiquetas que coincidan con la pregunta.** Por ejemplo, proporcione respuestas Sí y No a una pregunta sí o ninguna.
    -   **No use Aplicar botones en cuadros de diálogo que no sean hojas de propiedades ni elementos del panel de control.** El botón Aplicar significa aplicar los cambios pendientes, pero dejar abierta la ventana. Esto permite a los usuarios evaluar los cambios antes de cerrar la ventana. Sin embargo, solo las hojas de propiedades y los elementos del panel de control tienen esta necesidad.
    -   Etiquete un botón Cancelar si la cancelación devuelve el entorno a su estado anterior (sin ningún efecto secundario); De lo contrario, etiquete el botón Cerrar (si la operación se ha completado) o Detener (si la operación está en curso) para indicar que deja intacto el estado cambiado actual.
-   **Vínculos de comandos**
    -   **Presente siempre vínculos de comando en un conjunto de dos o más.** Lógicamente, no hay ninguna razón para hacer una pregunta que solo tenga una respuesta.
    -   **Proporcione un botón Cancelar explícito.** No use un vínculo de comando para este propósito. Con frecuencia, los usuarios se dan cuenta de que no quieren realizar una tarea. El uso de un vínculo de comando para cancelar requeriría que los usuarios leyesen cuidadosamente todos los vínculos de comando para determinar cuál es el medio para cancelar. Tener un botón Cancelar explícito permite a los usuarios cancelar una tarea de forma eficaz.
    -   **Si al proporcionar un botón Cancelar explícito se deja un único vínculo de comando, proporcione un vínculo de comando para cancelar y un botón Cancelar.** Al hacerlo, queda claro que los usuarios tienen una opción. Frasee este vínculo de comando en términos de su diferencia con respecto a la primera respuesta, en lugar de simplemente "Cancelar" o alguna variación.
-   **Casillas "No volver a mostrar \<item\> esto"**
    -   **Considere la posibilidad de usar la opción "No volver a mostrar esto" para permitir a los usuarios suprimir un cuadro de diálogo periódico, solo si no hay \<item\> una alternativa mejor.** Es mejor mostrar siempre el cuadro de diálogo si los usuarios realmente lo necesitan, o simplemente eliminarlo si no lo hacen.
    -   **Reemplace \<item\> por el elemento específico.** Por ejemplo, no vuelva a mostrar este recordatorio. Al hacer referencia a un cuadro de diálogo en general, use No volver a mostrar este mensaje.
    -   **Indique claramente cuándo se** usará la entrada del usuario para los valores predeterminados futuros agregando la siguiente frase bajo la opción: Las selecciones se usarán de forma predeterminada en el futuro.
    -   **No seleccione la opción de forma predeterminada. Si el cuadro de diálogo debe mostrarse solo una vez, debe hacerlo sin preguntar.** No use esta opción como un aviso para los usuarios molestos: asegúrese de que el comportamiento predeterminado no sea molesto.
    -   **Si los usuarios seleccionan la opción y hacen clic en Cancelar, esta opción tendrá efecto.** Esta configuración es una meta-opción, por lo que no sigue el comportamiento cancel estándar de no dejar ningún efecto secundario. Tenga en cuenta que si los usuarios no quieren ver el cuadro de diálogo en el futuro, lo más probable es que también quieran cancelarlo.
-   **Vínculos**
    -   **No asigne una clave de** [acceso.](glossary.md) Se accede a los vínculos mediante la tecla Tab.
    -   **No agregue "Haga clic" o "Haga clic aquí" al texto del vínculo.** No es necesario porque un vínculo implica hacer clic.
-   **Información sobre herramientas**
    -   **Use información sobre herramientas para proporcionar etiquetas para controles sin etiquetar.** No tiene que proporcionar información sobre herramientas de controles etiquetados simplemente por coherencia.
    -   **La información sobre herramientas también puede proporcionar más detalles para los botones de la barra de herramientas etiquetados si resulta útil.** No repita o dé una declaración de palabras de lo que ya está en la etiqueta.
    -   **Evite cubrir el objeto con el que el usuario está a punto de ver o interactuar.** Coloque siempre la propina en el lado del objeto, incluso si eso requiere la separación entre el puntero y la propina. Alguna separación no es un problema siempre que la relación entre el objeto y su propina sea clara.
        -   **Excepción:** Información sobre herramientas de nombre completo que se usa en listas y árboles.
    -   **En el caso de las colecciones de elementos, evite cubrir el siguiente objeto con el que es probable que el usuario vea o interactúe.** Para los elementos organizados horizontalmente, evite colocar sugerencias a la derecha; para elementos organizados verticalmente, evite colocar sugerencias a continuación.
-   **Muestra progresiva**
    -   **Use más o menos botones de divulgación progresiva para ocultar opciones, comandos y detalles avanzados o poco usados que los usuarios normalmente no necesitan.** No oculte los elementos usados habitualmente, ya que es posible que los usuarios no los encuentren. Pero asegúrese de que todo lo que está oculto tiene valor.
    -   Si la superficie siempre muestra algunas opciones, comandos o detalles, use los siguientes pares de etiquetas:
        -   **Más o menos opciones.** Use para opciones o una combinación de opciones, comandos y detalles.
        -   **Más o menos comandos.** Use solo para comandos.
        -   **Más o menos detalles.** Use solo para obtener información.
        -   **Más o menos \<object name\> .** Se usa para otros tipos de objeto, como carpetas.
    -   De lo contrario:
        -   **Mostrar u ocultar opciones.** Use para opciones o una combinación de opciones, comandos y detalles.
        -   **Mostrar u ocultar comandos.** Use solo para comandos.
        -   **Mostrar u ocultar detalles.** Use solo para obtener información.
        -   **Mostrar u ocultar \<object name\> .** Se usa para otros tipos de objeto, como carpetas.
-   **Barras de progreso**
    -   **Use barras de progreso determinadas para las** operaciones que requieren una cantidad limitada de tiempo, incluso si esa cantidad de tiempo no se puede predecir con precisión. Las barras de progreso indeterminado muestran que se está avanzando, pero no proporcionan ninguna otra información. No elija una barra de progreso indeterminada solo en función de la posible falta de precisión por sí sola.
    -   **Proporcione una estimación del tiempo restante si puede hacerlo con precisión.** Las estimaciones de tiempo restante que son precisas son útiles, pero las estimaciones que están muy lejos de la marca o que se recuperan significativamente no son útiles. Es posible que tenga que realizar algún procesamiento para poder proporcionar estimaciones precisas. Si es así, no muestre estimaciones potencialmente inexactas durante este período inicial.
    -   **No reinicie el progreso.** Una barra de progreso pierde su valor si se reinicia (quizás porque se completa un paso de la operación) porque los usuarios no tienen forma de saber cuándo se completará la operación. En su lugar, haga que todos los pasos de la operación compartan una parte del progreso y que la barra de progreso se complete una vez.
    -   **Proporcione detalles de progreso útiles.** Proporcione información de progreso adicional, pero solo si los usuarios pueden hacer algo con ella. Asegúrese de que el texto se muestra el tiempo suficiente para que los usuarios puedan leerlo.
    -   **No combine una barra de progreso con un puntero ocupado.** Use uno u otro, pero no ambos al mismo tiempo.
-   **Mensajes**
    -   **Use un símbolo del sistema cuando el espacio de la pantalla** sea tan premium que no se desea usar una etiqueta o una instrucción, como en una barra de herramientas.
    -   **El aviso es principalmente para identificar el propósito del cuadro de texto o cuadro combinado de una manera compacta.** No debe ser información fundamental que el usuario necesite ver mientras usa el control .
    -   **El texto del aviso no debe confundirse con texto real.** Para ello, siga estos pasos:
        -   Dibuje el texto del aviso en gris cursiva y el texto de entrada real en negro román.
        -   El texto del mensaje no debe ser editable y debe desaparecer una vez que los usuarios hacen clic en el cuadro de texto o la tabulan.
            -   **Excepción:** Si el cuadro de texto tiene el foco de entrada predeterminado, se muestra el mensaje y desaparece una vez que el usuario empieza a escribir.
    -   No use signos de puntuación finales ni puntos suspensivos.
-   **Notificaciones**
    -   **Use notificaciones para eventos que no están relacionados con la actividad del usuario actual, no requieren una acción inmediata del usuario y los usuarios pueden omitir libremente.**
    -   **No maltrate las notificaciones:**
        -   **Use notificaciones solo si es necesario.** Cuando se muestra una notificación, es posible que interrumpa a los usuarios o incluso los enome. Asegúrese de que la interrupción está justificada.
        -   **Use notificaciones para eventos no críticos o situaciones que no requieran una acción inmediata del usuario.** Para eventos críticos o situaciones que requieren una acción inmediata del usuario, use un elemento de interfaz de usuario alternativo (por ejemplo, un cuadro de diálogo modal).
        -   **No use notificaciones para anuncios de características.**

## <a name="keyboard"></a>Keyboard

-   **Asigne el foco de entrada inicial al control** con el que es más probable que los usuarios interactúen primero, que suele ser el primer control interactivo. Si el primer control interactivo no es una buena opción, considere la posibilidad de cambiar el diseño de la ventana.
-   **Asignar tabulaciones se detiene a todos los controles interactivos, incluidos los cuadros de edición de solo lectura. Excepciones:**
    -   Agrupa conjuntos de controles relacionados que se comportan como un control único, como botones de radio. Estos grupos tienen una sola tabulación.
    -   Contenga correctamente grupos para que las teclas de dirección se desenvánten y retrocedas dentro del grupo y permanezcan dentro del grupo.
-   **El orden de tabulación debe fluir de izquierda a derecha, de arriba abajo.** Por lo general, el orden de tabulación debe seguir el orden de lectura. Considere la posibilidad de realizar excepciones para los controles usados habitualmente, para lo que debe colocarlas anteriormente en el orden de tabulación. Tab debe recorrer todas las tabulaciones en ambas direcciones sin detenerse. Dentro de un grupo, el orden de tabulación debe estar en orden secuencial, sin excepciones.
-   **Dentro de una tabulación, el orden de la** tecla de flecha debe fluir de izquierda a derecha, de arriba abajo, sin excepciones. Las teclas de dirección deben recorrer todos los elementos en ambas direcciones sin detenerse.
-   **Presente los botones de confirmación en el orden siguiente:**
    -   Ok/ \[ Do it \] /Yes
    -   \[Don't do it \] /No
    -   Cancelar
    -   Aplicar (si está presente)

donde \[ Hacerlo y No hacerlo son \] \[ \] respuestas específicas a la instrucción principal.

-   **No confunda las teclas de acceso con teclas de método abreviado.** Aunque las teclas de acceso y las teclas de método abreviado proporcionan acceso mediante teclado a la interfaz de usuario, tienen diferentes propósitos e instrucciones.
-   **Siempre que sea posible, asigne claves de acceso únicas a todos los controles interactivos o sus etiquetas.** [Los cuadros de texto de solo](ctrl-text-boxes.md) lectura son controles interactivos (porque los usuarios pueden desplazarlos y copiar texto), por lo que se benefician de las claves de acceso. **No asigne claves de acceso a:**
    -   Botones Aceptar, Cancelar y Cerrar. Escriba y Esc se usan para sus claves de acceso. Sin embargo, asigne siempre una clave de acceso a un control que significa Aceptar o Cancelar, pero tiene una etiqueta diferente.
-   **Asigne teclas de método abreviado a los comandos más usados.** Las características y programas usados con poca frecuencia no necesitan teclas de método abreviado, ya que los usuarios pueden usar claves de acceso en su lugar.
-   **No haga que una tecla de método abreviado sea la única manera de realizar una tarea.** Los usuarios también deben poder usar el mouse o el teclado con teclas de tabulación, flecha y acceso.
-   **No asigne significados diferentes a teclas de método abreviado conocidas.** Dado que se memorizan, los significados incoherentes de los accesos directos conocidos son frustrantes y propensos a errores.
-   **No intente asignar teclas de método abreviado de programa para todo el sistema.** Las teclas de método abreviado del programa solo tendrán efecto cuando el programa tenga el foco de entrada.

## <a name="mouse"></a>Mouse

-   **No es necesario que los usuarios haga clic en un objeto para determinar si se puede hacer clic en él.** Los usuarios deben poder determinar la capacidad de clic solo mediante la inspección visual.
    -   La interfaz de usuario principal (como los botones de confirmación) debe tener una asequibilidad de clic estática. Los usuarios no deben tener que mantener el mouse para detectar la interfaz de usuario principal.
    -   La interfaz de usuario secundaria (como los comandos secundarios o los controles de divulgación progresiva) puede mostrar su asequibilidad de clic al mantener el puntero.
    -   Los vínculos de texto deben sugerir estáticamente texto de vínculo y, a continuación, mostrar su asequibilidad de clic (subrayado u otro cambio de presentación, con puntero de mano) al mantener el puntero.
    -   Los vínculos gráficos solo muestran un puntero de mano al mantener el puntero.
-   **Use el puntero de la mano (o "selección de vínculo") solo para los vínculos de texto y gráfico.** De lo contrario, los usuarios tendrían que hacer clic en objetos para determinar si son vínculos.

## <a name="dialog-boxes"></a>Cuadros de diálogo

-   **Los cuadros de diálogo modales requieren interacción, así que úsenlos para las cosas a las que los usuarios deben responder antes de continuar con su tarea.** Asegúrese de que la interrupción está justificada, por ejemplo, para tareas críticas o poco frecuentes que requieren finalización. De lo contrario, considere alternativas modeless.
-   **Los cuadros de diálogo no modelados no requieren interacción, así que úsenlos cuando los usuarios necesiten cambiar entre un cuadro de diálogo y la ventana de propietario.** Se usan mejor para tareas frecuentes, repetitivas o en curso. Sin embargo, las cintas de opciones, las barras de herramientas y las ventanas de paleta suelen ser mejores alternativas.

## <a name="property-sheets"></a>Hojas de propiedades

-   **Asegúrese de que las propiedades son necesarias.** No abarrote las páginas de propiedades con propiedades innecesarias solo para evitar tomar decisiones de diseño difíciles.
-   **Presentar propiedades en términos de objetivos de usuario en lugar de tecnología.** El hecho de que una propiedad configure una tecnología específica no significa que deba presentar la propiedad en términos de esa tecnología.
    -   Si debe presentar la configuración en términos de tecnología (quizás porque los usuarios reconocen el nombre de la tecnología), incluya una breve descripción de la ventaja del usuario.
-   **Use etiquetas de tabulación específicas y significativas.** Evite etiquetas de tabulación genéricas que se puedan aplicar a cualquier pestaña, como General, Avanzado o Configuración.
-   **Evite las páginas Generales.** No es necesario tener una página General. Use una página General solo si:
    -   Las propiedades se aplican a varias tareas y son significativas para la mayoría de los usuarios. No coloque propiedades especializadas o avanzadas en una página General, pero puede hacer que se pueda acceder a ellas a través de un botón de comando en la página General.
    -   Las propiedades no se ajustan a una categoría más específica. Si lo hacen, use ese nombre para la página en su lugar.
-   **Evite las páginas avanzadas.** Use una página Avanzadas solo si:
    -   Las propiedades se aplican a tareas poco comunes y son significativas principalmente para los usuarios avanzados.
    -   Las propiedades no se ajustan a una categoría más específica. Si lo hacen, use ese nombre para la página en su lugar.
-   **No use pestañas si una ventana de propiedades solo tiene una pestaña y no es extensible.** En su lugar, use un cuadro de diálogo normal con Aceptar, Cancelar y un botón Aplicar opcional. Sin embargo, las ventanas de propiedades extensibles (que pueden extenderse por terceros) deben usar pestañas.

## <a name="wizards"></a>Asistentes

-   **Considere primero alternativas ligeras, como cuadros de diálogo, paneles de tareas o páginas únicas.** Los asistentes son una interfaz de usuario pesada, que se usa mejor para tareas de varios pasos que se realizan con poca frecuencia. No tiene que usar asistentes: puede proporcionar información útil y ayuda en cualquier interfaz de usuario.
-   **Use Siguiente solo al avanzar a la página siguiente sin compromiso.** Avanzar a la página siguiente se considera un compromiso cuando su efecto no se puede deshacer haciendo clic en Atrás o Cancelar.
-   **Use Atrás solo para corregir errores.** Además de corregir errores, los usuarios no deben tener que hacer clic en Atrás para avanzar en una tarea.
-   **Cuando los usuarios confirmen una tarea, use un botón de confirmación que sea una respuesta específica a la instrucción principal (por ejemplo, Imprimir, Conectar o Iniciar).** No use etiquetas genéricas como Next (que no implica compromiso) o Finish (que no es específico) para confirmar una tarea. Las etiquetas de estos botones de confirmación deben tener sentido por sí solas. Inicie siempre las etiquetas de botón de confirmación con un verbo. **Excepciones:**
    -   Use Finalizar cuando las respuestas específicas siguen siendo genéricas, como Guardar, Seleccionar, Elegir u Obtener.
    -   Use Finalizar para cambiar una configuración específica o una colección de configuraciones.
-   **Use vínculos de comandos solo para las opciones, no los compromisos.** Los botones de confirmación específicos indican un compromiso mucho mejor que los vínculos de comando de un asistente.
-   **Al usar vínculos de comandos, oculte el botón Siguiente, pero deje el botón Cancelar.**
-   **Use Cerrar para las páginas Follow-Up y Finalización.** No use Cancelar porque cerrar la ventana no abandonará los cambios ni las acciones que se realicen en este momento. No use Listo porque no es un verbo imperativo.
-   **No use "asistente" en los nombres del asistente.** Por ejemplo, use "Conectar a una red" en lugar de "Red Asistente para instalación". Sin embargo, es aceptable hacer referencia a los asistentes como asistentes. Por ejemplo: "Si va a configurar una red por primera vez, puede obtener ayuda mediante el asistente Conectar a una red".
-   **Conserve las selecciones de usuario a través de la navegación.** Por ejemplo, si el usuario realiza cambios, hace clic en Atrás y, a continuación, en Siguiente, esos cambios se deben conservar. Los usuarios no esperan tener que volver a escribir los cambios a menos que elijan explícitamente borrarlos.

## <a name="wizard-pages"></a>Páginas del asistente

-   **Céntrate en la toma de decisiones eficaz.** Reduzca el número de páginas para centrarse en lo esencial. Consolide las páginas relacionadas y saque las páginas opcionales del flujo principal. Hacer que los usuarios haga clic en Siguiente completamente a través del asistente puede parecer una buena experiencia al principio, pero si los usuarios nunca necesitan cambiar los valores predeterminados, es probable que las páginas no sean necesarias.
-   **No use páginas de bienvenida: haga que la primera página sea funcional siempre que sea posible.** Use una página de Tareas iniciales opcional solo cuando:
    -   El asistente tiene requisitos previos que son necesarios para completar el asistente correctamente.
    -   Es posible que los usuarios no comprendan el propósito del asistente en función de su primera página de elección y no hay espacio para más explicaciones.
    -   La instrucción principal para las Tareas iniciales es "Antes de comenzar:".
-   **En las páginas en las que se pide a los usuarios que elijan, optimice para los casos más probables.** Estos tipos de páginas deben presentar opciones reales, no solo instrucciones.
    -   Si no usa una página de Tareas iniciales, explique el propósito del asistente en la parte superior de la primera página de opciones.
-   **Use las páginas de confirmación para dejar claro cuándo los usuarios confirman la tarea.** Normalmente, la página Confirmar es la última página de opciones y el botón Siguiente se vuelve a etiquetar para indicar la tarea que se está confirmando.
    -   No use páginas de resumen que simplemente resuman las selecciones anteriores del usuario, a menos que la tarea sea arriesgada (que implique seguridad o pérdida de tiempo o dinero) o que haya una buena posibilidad de que los usuarios no comprendan sus selecciones y necesiten revisarlas.
-   **No use páginas de enhorabuena que no hagan nada más que finalizar el asistente.** Si los resultados del asistente son claramente evidentes para los usuarios, cierre el asistente en el botón de confirmación final.
    -   Use Follow-Up cuando haya tareas relacionadas que es probable que los usuarios realicen como seguimiento. Evite tareas de seguimiento conocidas, como "Enviar un mensaje de correo electrónico".
    -   Use páginas de finalización solo cuando los resultados no sean visibles y no haya ninguna manera mejor de proporcionar comentarios para la finalización de tareas.
    -   Los asistentes que tienen páginas progreso deben usar una página Finalización o Follow-Up página para indicar la finalización de tareas. Para las tareas de ejecución larga, cierre el asistente en la página Confirmar y use notificaciones para enviar comentarios.

## <a name="error-messages"></a>Mensajes de error

-   **No dé mensajes de error cuando no** sea probable que los usuarios realicen una acción o cambien su comportamiento como resultado del mensaje. Si no hay ninguna acción que los usuarios puedan realizar o si el problema no es significativo, suprima el mensaje de error.
-   **Siempre que sea posible, proponga una solución para que los usuarios puedan corregir el problema.** Sin embargo, asegúrese de que es probable que la solución propuesta resuelva el problema. No pierda el tiempo de los usuarios al sugerir soluciones posibles, pero improbables.
-   **Ser específico.** Evite palabras imprecisas, como errores de sintaxis y operaciones no válidas. Proporcione nombres, ubicaciones y valores específicos de los objetos implicados.
-   **No use expresiones que achacan al usuario o que impliquen un error de usuario.** Evite usar usted y su en la expresión. Aunque generalmente se prefiere la voz activa, use la voz pasiva cuando el usuario sea el sujeto y se sienta achacado al error si se usó la voz activa.
-   **No use Aceptar para los mensajes de error.** Los usuarios no ven los errores como correctos. Si el mensaje de error no tiene ninguna acción directa, use Cerrar en su lugar.
-   **No use las siguientes palabras:**
    -   Error, error (use el problema en su lugar)
    -   No se pudo (no se puede usar en su lugar)
    -   No válido, no válido, incorrecto (use incorrecto o no válido en su lugar)
    -   Abort, kill, terminate (use stop en su lugar)
    -   Grave y grave (use en su lugar grave)

Estos términos son innecesarios y contrarios al tono alentador de Windows. En su [lugar,](vis-std-icons.md)un icono de error, cuando se usa correctamente, comunica lo suficiente que hay un problema.

-   **No acompaña los mensajes de error con efectos de sonido.** Esto es un jarring e innecesario.

## <a name="warning-messages"></a>Mensajes de advertencia

-   **Las advertencias describen una condición que podría causar un problema en el futuro.** Las advertencias no son errores ni preguntas, por lo que no frases preguntas rutinarias como advertencias.
-   **No dé mensajes de advertencia cuando no sea probable que los usuarios realicen una acción o cambien su comportamiento como resultado del mensaje.** Si no hay ninguna acción que los usuarios puedan realizar o si la condición no es significativa, suprima el mensaje de advertencia.

## <a name="confirmations"></a>Confirmaciones

-   **No use confirmaciones innecesarias.** Use confirmaciones solo cuando:
    -   Hay una razón clara para no continuar y una posibilidad razonable de que a veces los usuarios no lo haga.
    -   La acción tiene consecuencias significativas o no se puede deshacer fácilmente.
    -   La acción tiene consecuencias que es posible que los usuarios no conozcan.
    -   Continuar con la acción requiere que los usuarios elijan una opción que no tenga un valor predeterminado adecuado.
    -   Dado el contexto actual, es probable que los usuarios han realizado una acción en error.
-   **Las confirmaciones de frases como una pregunta sí o ninguna y proporcionan respuestas sí o no.** A diferencia de otros tipos de cuadros de diálogo, las confirmaciones están diseñadas para impedir que los usuarios tome decisiones rápidas. Si los usuarios no tienen en cuenta su respuesta, una confirmación no tiene ningún valor.

## <a name="icons"></a>Iconos

-   **Todos los iconos deben cumplir las directrices de** [icono de estilo de Avión](vis-icons.md). Reemplace todos Windows iconos de estilo XP.
-   **Elija iconos estándar en función de su tipo de mensaje, no de la gravedad del problema subyacente:**
    -   **Error.** Error o problema que se ha producido.
    -   **Advertencia.** Una condición que podría causar un problema en el futuro.
    -   **Información.** Información útil.

Si un problema combina distintos tipos de mensajes, céntrate en el aspecto más importante sobre el que los usuarios deben actuar.

-   **Los iconos siempre deben coincidir con la instrucción principal u otro texto correspondiente.**
-   **Los iconos de error no son necesarios para problemas de entrada de usuario no críticos.** Sin embargo, los iconos son necesarios para los errores en contexto, ya que de lo contrario, estos comentarios contextuales serían demasiado fáciles de pasar por alto.
-   **No use iconos de advertencia para "evitar" errores no críticos.** Los errores no son advertencias; en su lugar, aplique las directrices del icono de error.
-   **Para los diálogos de preguntas, use iconos de advertencia solo para preguntas con consecuencias significativas.** No use iconos de advertencia para preguntas rutinarias.

## <a name="help"></a>Ayuda

-   **Vínculo a temas de Ayuda específicos y pertinentes.** No vincule a la página principal de la Ayuda, a la tabla de contenido, a una lista de resultados de búsqueda o a una página que solo se vincule a otras páginas. Evite vincular a páginas estructuradas como una lista grande de preguntas más frecuentes, ya que obliga a los usuarios a buscar la que coincida con el vínculo en el que han hecho clic. No vincule a temas de Ayuda específicos que no sean pertinentes y útiles para la tarea en cuestión. No vincular nunca a páginas vacías.
-   **No coloque vínculos de Ayuda en todas las ventanas o páginas por coherencia.** Proporcionar un vínculo de Ayuda en un solo lugar no significa que tenga que proporcionarlos en todas partes.
-   **Siempre que sea posible, la frase Ayuda vincula texto en términos de la pregunta principal que responde el contenido de la Ayuda.** No use las expresiones "Más información sobre" o "Obtener ayuda con esto".
-   **Use el vínculo de Ayuda completo para el texto del vínculo, no** solo las palabras clave.
-   **Use oraciones completas.**
-   **No use signos de puntuación finales ni puntos suspensivos, excepto los signos de interrogación.**
-   **Si el contenido de la Ayuda está en línea, aclare esto en el texto del vínculo.** Esto ayuda a que el resultado de los vínculos sea predecible.

