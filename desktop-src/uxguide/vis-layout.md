---
title: Layout
description: El diseño es el tamaño, el espaciado y la ubicación del contenido dentro de una ventana o página.
ms.assetid: 39cd896f-d3cc-4768-a20c-a7f598da7136
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8577843f3e54744cabe970e3b9132df1d9fb45df
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444886"
---
# <a name="layout"></a>Layout

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

El diseño es el tamaño, el espaciado y la ubicación del contenido dentro de una ventana o página. El diseño efectivo es fundamental para ayudar a los usuarios a encontrar lo que buscan rápidamente, así como para que la apariencia sea visualmente atractiva. El diseño efectivo puede marcar la diferencia entre los diseños que los usuarios entienden inmediatamente y los que dejan a los usuarios desconcertados y sobrecargados.

**Nota:** Las directrices relacionadas [con la administración de](win-window-mgt.md) ventanas se presentan en un artículo independiente. El tamaño y el espaciado de control específicos recomendados se presentan en sus respectivos artículos de instrucciones.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="visual-hierarchy"></a>Jerarquía visual

Una ventana o página tiene una jerarquía visual clara cuando su apariencia indica la relación y la prioridad de sus elementos. Sin una jerarquía visual, los usuarios tendrían que averiguar estas relaciones y prioridades por sí mismos.

La jerarquía visual se logra combinando con habilidad los atributos siguientes:

-   **centro de atención.** El diseño indica dónde deben buscar primero los usuarios.
-   **Flujo.** El ojo fluye sin problemas y de forma natural mediante una ruta de acceso clara a través de la superficie, buscando elementos de la interfaz de usuario (UI) en el orden adecuado para su uso.
-   **Agrupación.** Los elementos de interfaz de usuario relacionados lógicamente tienen una relación visual clara. Los elementos relacionados se agrupan; los elementos no relacionados son independientes.
-   **Énfasis.** Los elementos de la interfaz de usuario se resaltan en función de su importancia relativa.
-   **Alineación.** Los elementos de la interfaz de usuario tienen una ubicación coordinada, por lo que son fáciles de examinar y aparecen de forma ordenada.

Además, el diseño efectivo tiene estos atributos:

-   **Independencia del dispositivo.** El diseño aparece según lo previsto, independientemente del tipo de letra o el tamaño de fuente, los puntos por pulgada (ppp), la pantalla o el adaptador gráfico.
-   **Fácil de examinar.** Los usuarios pueden encontrar el contenido que buscan de un vistazo.
-   **Eficiencia.** Los elementos de la interfaz de usuario que son grandes deben ser grandes y los que son pequeños funcionan bien pequeños.
-   **Capacidad de tamaño.** Si resulta útil, se puede hacer un tamaño de ventana y su diseño de contenido es eficaz, independientemente de lo grande o pequeña que sea la superficie.
-   **equilibrar.** El contenido aparece distribuido uniformemente en la superficie.
-   **Simplicidad visual.** La percepción de que un diseño no es más complicado de lo que debe ser. Los usuarios no se ven abrumados por la apariencia del diseño.
-   **Coherencia.** Las ventanas o páginas similares usan un diseño similar, por lo que los usuarios siempre se sienten orientados.

Aunque el tamaño, el espaciado y la colocación son conceptos sencillos, el desafío con el diseño es lograr la combinación correcta de estos atributos.

En Windows, el diseño se comunica mediante métricas independientes del dispositivo, como unidades de diálogo (D DLL) y píxeles relativos.

### <a name="a-design-model-for-reading"></a>Un modelo de diseño para lectura

**Los usuarios eligen lo que leen por la apariencia y la organización del contenido.** Para crear un diseño eficaz, deberá comprender qué tienden a leer los usuarios y por qué.

Puede tomar decisiones de diseño mediante este modelo de diseño para leer:

-   Las personas leen en un orden de izquierda a derecha, de arriba a abajo (en las culturas occidental).
-   Hay dos modos de lectura: lectura inmersiva y examen. El objetivo de la lectura inmersiva es la comprensión.

    ![figura de flecha roja en el patrón de lectura de arrowzag ](images/vis-layout-image1.png)

    Este diagrama modela la lectura inmersiva.

    Por el contrario, el objetivo del examen es buscar cosas. La ruta de acceso de examen general tiene el siguiente aspecto:

    ![figura de flecha roja en el patrón de lectura diagonal ](images/vis-layout-image2.png)

    Este diagrama modela el examen.

    ![figura de flecha roja en un patrón de flecha hacia abajo y arco ](images/vis-layout-image3.png)

    Si hay texto en ejecución a lo largo del borde izquierdo de una página, los usuarios examinarán primero el borde izquierdo.

-   Cuando se usa software, los usuarios no están inmersos en la propia interfaz de usuario, sino en su trabajo. Por lo tanto, los usuarios normalmente no leen el texto de la interfaz de usuario que lo analizan. A continuación, leen los bits de texto de forma completa solo cuando creen que es necesario.
-   Los usuarios tienden a omitir los paneles de navegación en el lado izquierdo o derecho de una página. Los usuarios reconocen que están ahí, pero miran los paneles de navegación solo cuando desean navegar.
-   Los usuarios tienden a omitir grandes bloques de texto sin formato sin leerlos en absoluto.

    ![figura de texto con flechas que muestran el texto de examen ](images/vis-layout-image4.png)

    Los usuarios tienden a omitir grandes bloques de texto y paneles de navegación al examinar.

-   Todos los aspectos son iguales, los usuarios buscan primero en la esquina superior izquierda de una ventana, analizan la página y finalizan su examen en la esquina inferior derecha. Tienden a omitir la esquina inferior izquierda.

    ![figura de la página y flecha de arriba izquierda a derecha ](images/vis-layout-image5.png)

    Todos los elementos son iguales, los usuarios leerán estos números en el orden siguiente: 1, 2, 4 y 3.

-   Pero en la interfaz de usuario interactiva, no todas las cosas son iguales, por lo que los distintos elementos de la interfaz de usuario reciben distintos niveles de atención. Los usuarios tienden a mirar los controles interactivos, especialmente los controles de la parte superior izquierda y central de la ventana, y el texto destacado en primer lugar.

![figura de pantalla con texto nítido y desenfocado ](images/vis-layout-image6.png)

Los usuarios se centran en los controles interactivos principales y en la instrucción principal destacada, y miran otras cosas solo cuando es necesario.

-   Los usuarios tienden a leer etiquetas de control interactivas, especialmente aquellas que parecen relevantes para completar la tarea en cuestión. Por el contrario, los usuarios tienden a leer texto estático solo cuando creen que lo necesitan.
-   Los elementos que parecen diferentes llaman la atención. El texto en negrita y el texto grande se destaca del texto normal. Los elementos de la interfaz de usuario con color o sobre un fondo coloreado destacan. Los elementos con iconos se destacan de los elementos sin iconos.
-   Los usuarios no se desplazan a menos que tengan una razón para hacerlo. Si el contenido [sobre el plegado](glossary.md) no proporciona un motivo para desplazarse, no lo hace.
-   Una vez que los usuarios han decidido qué hacer, detienen inmediatamente el examen y lo hacen.
-   Dado que los usuarios dejan de examinar cuando creen que han terminado, tienden a ignorar cualquier cosa más allá de lo que parece ser el punto de finalización.

![captura de pantalla de las opciones de teclado ](images/vis-layout-image7.png)

Los usuarios dejan de examinar cuando creen que han terminado.

Por supuesto, habrá excepciones a este modelo general. Los dispositivos de seguimiento ocular indican que el comportamiento de los usuarios reales es bastante errático. El objetivo de este modelo es ayudarle a tomar buenas decisiones y acuerdos, no a modelar el comportamiento del usuario con precisión. Pero a medida que ha leído esta lista, esperamos que también haya reconocido muchos de sus propios patrones de lectura.

### <a name="designing-for-scanning"></a>Diseño para el examen

**Los usuarios no leen, se analizan, por lo que debe diseñar superficies de interfaz de usuario para el examen.** No suponga que los usuarios leerán el texto tal como se escribe en un orden de izquierda a derecha, de arriba a abajo, sino que miran los elementos de la interfaz de usuario que llaman su atención.

Para diseñar para el examen:

-   Supongamos que los usuarios empiezan por examinar rápidamente toda la ventana y, a continuación, leen los elementos de la interfaz de usuario en aproximadamente el orden siguiente:
    -   Controles interactivos en el centro
    -   Botones de confirmación
    -   Controles interactivos encontrados en otro lugar
    -   Instrucción principal
    -   Explicaciones complementarias
    -   Texto que aparece con un icono de advertencia
    -   Título de la ventana
    -   Otro texto estático en el cuerpo principal
    -   Notas al pie
-   Coloque los elementos de la interfaz de usuario que inician una tarea en la esquina superior izquierda o en el centro superior.
-   Coloque los elementos de la interfaz de usuario que completan una tarea en la esquina inferior derecha.
-   Siempre que sea posible, coloque texto fundamental en controles interactivos en lugar de texto estático.
-   Evite colocar información fundamental en la esquina inferior izquierda o en la parte inferior de una página o control desplazable largo.
-   No presente grandes bloques de texto. Elimine el texto innecesario. Use el [estilo de presentación de la pirámide](text-ui.md) invertido.
-   Si hace algo para atraer la atención de los usuarios, asegúrese de que la atención está garantizada.

Siempre que sea posible, trabaje con este modelo en lugar de hacerlo; pero habrá ocasiones en las que tenga que resaltar o desacente determinados elementos de la interfaz de usuario.

Para resaltar los elementos principales de la interfaz de usuario:

-   Coloque los elementos principales de la interfaz de usuario en la [ruta de acceso de examen.](glossary.md)
-   Coloque cualquier interfaz de usuario para iniciar una tarea en la esquina superior izquierda o en el centro superior.
-   Coloque los botones de confirmación en la esquina inferior derecha.
-   Coloque la interfaz de usuario principal restante en el centro.
-   Use controles que atraigan la atención, como botones de comando, vínculos de comandos e iconos.
-   Use texto destacado, incluido texto grande y texto en negrita.
-   Coloque texto que los usuarios deben leer en controles interactivos, con iconos o en [banners](vis-graphic.md).
-   Use texto oscuro en un fondo claro.
-   Rodear los elementos con un espacio amplio.
-   No requiera ninguna interacción, como apuntar o mantener el puntero, para ver el elemento que está resaltando.

    ![captura de pantalla de las opciones de activación de Windows ](images/vis-layout-image8.png)

    En este ejemplo se muestran muchas maneras de resaltar los elementos principales de la interfaz de usuario.

Para desmarcar los elementos secundarios de la interfaz de usuario:

-   Coloque los elementos secundarios de la interfaz de usuario fuera de la ruta de acceso del examen.
-   Coloque cualquier cosa que los usuarios no necesiten ver en la esquina inferior izquierda o en la parte inferior de la ventana.
-   Use controles que no llaman la atención, como vínculos de tareas en lugar de botones de comando.
-   Use texto normal o gris.
-   Use texto claro en un fondo oscuro. El texto blanco en un fondo gris o azul oscuro funciona bien.
-   Rodear los elementos con espacio mínimo.
-   Considere la posibilidad de [usar la divulgación progresiva](ctrl-progressive-disclosure-controls.md) para ocultar elementos secundarios de la interfaz de usuario.

    ![captura de pantalla de elementos de interfaz grandes y pequeños ](images/vis-layout-image9.png)

    En este ejemplo se muestran muchas maneras de desacentr los elementos secundarios de la interfaz de usuario.

### <a name="using-screen-space-effectively"></a>Uso eficaz del espacio de pantalla

El uso eficaz del espacio de pantalla requiere que equilibres varios factores: usar demasiado espacio y que una ventana parezca pesada y desperdiciada, e incluso difícil de usar en función de la ley [de Fitts.](inter-mouse.md)

**Incorrecto:**

![captura de pantalla que muestra demasiado espacio en blanco ](images/vis-layout-image10.png)

En este ejemplo, la ventana es demasiado grande para su contenido.

Por otro lado, use demasiado poco espacio y una ventana se sienta cómoda, desconsocedida y manipulada, y difícil de usar si requiere desplazamiento y otra manipulación para su uso.

**Incorrecto:**

![captura de pantalla con demasiados controles ](images/vis-layout-image11.png)

En este ejemplo, la ventana es demasiado pequeña para su contenido.

Aunque la interfaz de usuario crítica debe ajustarse a la resolución efectiva mínima [admitida,](glossary.md)no suponga que el uso eficaz del espacio de pantalla significa que las ventanas deben ser lo más pequeñas posible. **El diseño efectivo respeta el espacio abierto y no intenta convertir todo en el espacio más pequeño posible.** Las pantallas modernas tienen un espacio de pantalla significativo y tiene sentido usar este espacio de forma eficaz cuando sea posible. Por lo tanto, err en el lado del uso de demasiado espacio de pantalla en lugar de demasiado poco. Esto hace que las ventanas se sientan más ligeras y más fáciles de abordar.

Sabe que un diseño usa el espacio de pantalla de forma eficaz cuando:

-   Windows, los paneles de ventana y los controles no tienen que cambiar de tamaño para que se puedan usar. Si lo primero que hacen los usuarios es cambiar el tamaño de una ventana, panel o control, su tamaño es incorrecto.
-   Los datos no se truncan. La mayoría de los datos de las vistas de lista y las vistas de árbol no tienen puntos suspensivos y los datos de otros controles no se recortan a menos que la longitud de los datos sea inusualmente grande. Los datos que se deben leer para realizar una tarea no deben truncarse.
-   Las ventanas y los controles tienen el tamaño adecuado para eliminar el desplazamiento innecesario. Hay pocas barras de desplazamiento horizontales y ninguna barra de desplazamiento vertical innecesaria.
-   Los controles usan principalmente sus tamaños estándar. Esfuérzse por reducir el número de tamaños de control, por ejemplo, usando solo uno o dos anchos de botón de comando en una superficie.
-   La superficie de la interfaz de usuario está equilibrada. No hay áreas de pantalla grandes sin usar.

Elija tamaños de ventana que sean lo suficientemente grandes como para satisfacer bien su propósito. (Y si la ventana se puede cambiar de tamaño, este objetivo se aplica a su tamaño predeterminado). Una combinación de datos truncados o barras de desplazamiento y una gran cantidad de espacio disponible en la pantalla es **una señal clara de diseño ineficaz.**

### <a name="control-sizing"></a>Control del tamaño

Normalmente, el primer paso para usar el espacio de pantalla de forma eficaz es determinar el tamaño correcto para los distintos elementos de la interfaz de usuario. Consulte la tabla [Control de tamaño,](#recommended-sizing-and-spacing) así como el tamaño recomendado en los artículos de instrucciones de control específicos.

La ley de Fitts indica que cuanto menor sea un destino, más tiempo se tarda en adquirirlo con el mouse. Además, en el caso de los equipos que usan tabletas Windows y tecnología táctil, el "mouse" podría ser realmente un lápiz o el dedo del usuario, por lo que debe considerar dispositivos de entrada alternativos al determinar los tamaños de los controles pequeños. **Un tamaño de control de 16 x 16 píxeles relativos es un buen tamaño mínimo para cualquier dispositivo de entrada.** Por el contrario, los botones estándar de control de número de píxeles relativos de 15 x 9 son demasiado pequeños para que los lápices los usen de forma eficaz.

### <a name="spacing"></a>Espaciado

Proporcionar un espacio amplio (pero no excesivo) hace que el diseño se sienta más cómodo y fácil de analizar. El espacio efectivo no es un espacio sin usar, desempeña un papel importante en la mejora de la capacidad de examen de los usuarios y también agrega al atractivo visual del diseño. Para obtener instrucciones, consulte la [tabla Espaciado](#recommended-sizing-and-spacing).

En el caso de los equipos que usan tabletas Windows y tecnología táctil, de nuevo el "mouse" podría ser realmente un lápiz o el dedo del usuario. La orientación es más difícil cuando se usa un lápiz o un dedo como dispositivo que apunta, lo que da lugar a que los usuarios toque fuera del destino previsto. Cuando los controles interactivos se colocan muy cerca, pero no se tocan realmente, los usuarios pueden hacer clic en el espacio inactivo entre los controles. Dado que hacer clic en el espacio inactivo no tiene ningún resultado o comentarios visuales, los usuarios a menudo no saben lo que salió mal. Si los controles pequeños están demasiado espaciados, el usuario debe pulsar con precisión para evitar pulsar el objeto incorrecto. **Para solucionar estos problemas, las regiones de destino de los controles interactivos deben tocar o tener al menos 3 D DLL (5 píxeles relativos) de espacio entre ellos.**

Sabe que un diseño tiene un espaciado correcto cuando:

-   En general, la superficie de la interfaz de usuario se siente cómoda y no se siente cómodo.
-   El espacio parece uniforme y equilibrado.
-   Los elementos relacionados están cerca y los elementos no relacionados están relativamente separados.
-   No hay ningún espacio entre los controles que están diseñados para estar juntos, como los botones de la barra de herramientas.

### <a name="resizable-windows"></a>Ventanas de tamaño ajustable

Las ventanas de tamaño ajustable también son un factor para usar el espacio de pantalla de forma eficaz. Algunas ventanas constan de contenido fijo y no se benefician de la redimensionable, pero las ventanas con contenido de tamaño ajustable deben ser ajustables. Por supuesto, el motivo por el que los usuarios cambian el tamaño de una ventana es avanzar en el espacio de pantalla adicional, por lo que el contenido debe expandirse en consecuencia al proporcionar más espacio a los elementos de la interfaz de usuario que lo necesitan. Las ventanas con contenido dinámico, documentos, imágenes, listas y árboles son las que más se benefician de las ventanas de tamaño ajustable.

![captura de pantalla del control de cambio de tamaño al obtener la barra de desplazamiento ](images/vis-layout-image12.png)

En este ejemplo, al cambiar el tamaño de la ventana se cambia el tamaño del control de vista de lista.

Dicho esto, las ventanas se pueden extender demasiado anchas. Por ejemplo, muchas páginas del panel de control se vuelven difíciles de manejar cuando el contenido es más ancho que 600 píxeles relativos. En este caso, es mejor no cambiar el tamaño del área de contenido más allá de este ancho máximo o cambiar el origen del contenido a medida que la ventana cambia de tamaño. En su lugar, mantenga un ancho máximo y un origen fijo superior izquierdo.

El texto se vuelve difícil de leer a medida que aumenta la longitud de la línea. En el caso de los documentos de texto, considere la posibilidad de una longitud de línea máxima de 80 caracteres para facilitar la lectura del texto. (Los caracteres incluyen letras, signos de puntuación y espacios).

**Incorrecto:**

![captura de pantalla del cuadro de mensaje ancho con texto largo ](images/vis-layout-image13.png)

En este ejemplo, la longitud larga del texto dificulta la lectura.

Por último, las ventanas que se pueden cambiar de tamaño también necesitan usar el espacio de pantalla de forma eficaz cuando se reducen, ya que reducen el tamaño del contenido y quitan espacio de los elementos de la interfaz de usuario que pueden funcionar de forma eficaz sin él. En algún momento, la ventana o sus elementos de interfaz de usuario se vuelven demasiado pequeños para poder usarse, por lo que se les debe asignar un tamaño mínimo o algunos elementos se deben quitar por completo.

![captura de pantalla de la ventana con cinta de opciones alta e intrusiva ](images/vis-layout-image14.png)

![captura de pantalla de la ventana sin cinta de opciones ](images/vis-layout-image15.png)

En este ejemplo, el panel tiene un tamaño mínimo.

Algunos programas se benefician de usar una presentación completamente diferente para que el contenido se puede usar en tamaños más pequeños.

![captura de pantalla de los botones del reproductor multimedia centrado ](images/vis-layout-image16.png)

En este ejemplo, Reproductor de Windows Media cambia su formato cuando la ventana se vuelve demasiado pequeña para el formato estándar.

### <a name="focus"></a>Foco

Un diseño tiene el foco cuando hay un lugar obvio en el que mirar primero. El foco es importante para mostrar a los usuarios dónde empezar a examinar la ventana o página. Sin un foco claro, el ojo del usuario se despedará sin objetivo. El punto focal debe ser algo importante que los usuarios necesitan encontrar y comprender rápidamente, y debe tener el mayor énfasis visual. La esquina superior izquierda es el punto focal natural para la mayoría de las ventanas.

Solo debe haber un punto focal. Al igual que en la vida real, el ojo puede centrarse solo en una cosa a la vez, los usuarios no pueden centrarse en varios lugares simultáneamente.

Para convertir un elemento de interfaz de usuario en el punto focal, puede darle énfasis visual mediante:

-   Colocarlo en la parte superior izquierda o superior central de la superficie.
-   Uso de controles interactivos que son importantes y fáciles de comprender.
-   Usar texto destacado, como una instrucción principal.
-   Dar a los controles la selección predeterminada y el foco de entrada inicial.
-   Colocar los controles en un fondo de color diferente.

Considere Windows Search. El punto focal para Windows Search debe ser el cuadro de búsqueda porque es el punto inicial de la tarea. Sin embargo, se encuentra en la esquina superior derecha para ser coherente con la ubicación estándar del cuadro de búsqueda. El cuadro de búsqueda tiene el foco de entrada, pero dada su ubicación en la ruta de acceso del examen, esa pista por sí sola no es suficiente.

Para solucionar este problema, hay instrucciones destacadas en la parte superior central de la ventana para dirigir a los usuarios a la ubicación correcta.

**Aceptable:**

![captura de pantalla del cuadro de diálogo de búsqueda con texto útil ](images/vis-layout-image17.png)

En este ejemplo, una instrucción destacada en la parte superior central de la ventana dirige a los usuarios al cuadro buscar.

Sin las instrucciones, la ventana no tendría un punto focal obvio.

**Incorrecto:**

![captura de pantalla del cuadro de diálogo de búsqueda sin texto ](images/vis-layout-image18.png)

Este ejemplo no tiene ningún punto focal obvio. Los usuarios no saben dónde buscar.

Si da énfasis visual a un elemento de la interfaz de usuario, asegúrese de que la atención está garantizada. En el ejemplo Windows Search incorrecto anterior, el botón Todo resaltado está en la esquina superior izquierda y tiene el énfasis más visual, pero no es el punto focal previsto. Los usuarios pueden quedarse atascados viendo este botón intentando averiguar qué hacer con él.

**Incorrecto:**

![captura de pantalla del botón todo resaltado ](images/vis-layout-image19.png)

Sin la instrucción destacada como punto focal, el botón Todo resaltado es un punto focal involuntario.

### <a name="flow"></a>Flujo

Un diseño tiene flujo cuando los usuarios se guían de forma fluida y natural por una ruta de acceso clara a través de su superficie, buscando elementos de la interfaz de usuario en el orden adecuado para su uso. Una vez que los usuarios identifican el punto focal, deben determinar cómo completar la tarea. La ubicación de los elementos de la interfaz de usuario transmite su relación y debe reflejar los pasos para realizar la tarea. Normalmente, esto significa que los pasos de la tarea deben fluir de forma natural en un orden de izquierda a derecha, de arriba a abajo (en las culturas occidental).

Sabe que un diseño tiene un buen flujo cuando:

-   La colocación de los elementos de la interfaz de usuario refleja los pasos que los usuarios necesitan para realizar la tarea.
-   Los elementos de la interfaz de usuario que inician una tarea se encuentran en la esquina superior izquierda o en el centro superior.
-   Los elementos de la interfaz de usuario que completan una tarea se encuentran en la esquina inferior derecha.
-   Los elementos de interfaz de usuario relacionados están juntos; los elementos no relacionados son independientes.
-   Los pasos necesarios están en el flujo principal.
-   Los pasos opcionales están fuera del flujo principal, posiblemente desacentados mediante un fondo adecuado o una divulgación progresiva.
-   Los elementos usados con frecuencia aparecen antes que los elementos usados con poca frecuencia en la ruta de acceso del examen.
-   Los usuarios siempre saben qué hacer a continuación. No hay saltos o saltos inesperados en el flujo de tareas.

**Incorrecto:**

![captura de pantalla del diseño confuso del cuadro de diálogo ](images/vis-layout-image20.png)

En este ejemplo, los usuarios no saben qué hacer a continuación. Hay saltos y saltos inesperados en el flujo de tareas.

**Correcto:**

![captura de pantalla de un cuadro de diálogo bien planeado ](images/vis-layout-image21.png)

En este ejemplo, la presentación de los elementos de la interfaz de usuario refleja los pasos para realizar la tarea.

### <a name="grouping"></a>Agrupar

Un diseño tiene agrupación cuando los elementos de la interfaz de usuario relacionados lógicamente tienen una relación visual clara. Los grupos son importantes porque es más fácil que los usuarios comprendan y se centren en un grupo de elementos relacionados que los elementos individualmente. Los grupos hacen que un diseño parezca más sencillo y fácil de analizar.

Puede mostrar la agrupación de las maneras siguientes (con una mayor peso):

-   **Diseño.** Puede agrupar los controles relacionados entre sí y colocar espaciado adicional entre controles no relacionados.

    ![ilustración de cuatro iconos que muestran cuatro grupos de tareas ](images/vis-layout-image22.png)

    En este ejemplo, solo el diseño se usa para mostrar las relaciones de control.

-   **Separadores.** Un separador es una línea horizontal o vertical que unifica un grupo de controles. Los separadores proporcionan un aspecto más sencillo y limpio. Sin embargo, a diferencia de los cuadros de grupo, funcionan mejor cuando abarcan toda la superficie.

    ![captura de pantalla de tres iconos y tres separadores ](images/vis-layout-image23.png)

    En este ejemplo, los separadores etiquetados se usan para mostrar las relaciones de control.

-   **Agregadores.** Un agregador es un gráfico que crea una relación visual entre controles fuertemente relacionados.

    ![captura de pantalla de los controles dentro de una línea elíptica ](images/vis-layout-image24.png)

    En este ejemplo, se usa un agregador de límites para resaltar la relación entre los controles y hacer que se sientan como un control único en lugar de ocho.

-   **Cuadros de grupo.** Un cuadro de grupo es un marco rectangular etiquetado que rodea un conjunto de controles relacionados.

    ![captura de pantalla de casillas en un borde rectangular ](images/vis-layout-image25.png)

    En este ejemplo, un cuadro de grupo rodea y etiqueta un conjunto de controles relacionados.

-   **Fondos.** Puede usar fondos para resaltar o desacentr los distintos tipos de contenido.

    ![captura de pantalla del lado izquierdo del panel de control ](images/vis-layout-image26.png)

    En este ejemplo, el panel de tareas del panel de control se usa para agrupar tareas relacionadas y elementos del panel de control.

    Para evitar el desorden visual, la agrupación más ligera que hace bien el trabajo es la mejor opción. Para obtener más información, [vea Cuadros de grupo](ctrl-group-boxes.md), [pestañas,](ctrl-tabs.md) [separadores y fondos.](vis-graphic.md)

Independientemente del estilo de agrupación, puede usar la sangría para mostrar la relación de los controles dentro de un grupo. Los controles que son pares entre sí deben estar alineados a la izquierda y los controles dependientes tienen una sangría de 12 D DLL o 18 píxeles relativos.

![captura de pantalla de tres niveles de controles con sangría ](images/vis-layout-image27.png)

Los controles dependientes tienen una sangría de 12 DLUS o 18 píxeles relativos, que por diseño es la distancia entre las casillas y los botones de radio de sus etiquetas.

Sabe que un diseño tiene una buena agrupación cuando:

-   La ventana o páginas tiene como máximo 7 grupos.
-   El propósito de cada grupo es obvio.
-   La relación de los controles dentro de cada grupo es obvia, especialmente la dependencia de control.
-   La agrupación simplifica el contenido en lugar de hacerlo más complejo.

### <a name="alignment"></a>Alignment

La alineación es la colocación coordinada de los elementos de la interfaz de usuario. La alineación es importante porque facilita el examen del contenido y afecta a la percepción de la complejidad visual de los usuarios.

Hay varios objetivos que se deben tener en cuenta al determinar la alineación:

-   **Facilidad en el examen horizontal.** Los usuarios pueden leer horizontalmente y buscar elementos relacionados uno al lado del otro, sin ningún hueco complicado.
-   **Facilidad en el examen vertical.** Los usuarios pueden examinar columnas de elementos relacionados y encontrar inmediatamente lo que buscan, con un movimiento de los ojos horizontal mínimo.
-   **Complejidad visual mínima.** Los usuarios perciben que un diseño es visualmente complejo si tiene líneas de cuadrícula de alineación vertical innecesarias.

### <a name="horizontal-alignment"></a>Alineación horizontal

**Alineación izquierda**

Debido al orden de lectura de izquierda a derecha, la alineación izquierda funciona bien para la mayoría del contenido. La alineación izquierda facilita el examen vertical de los datos en columnas.

**Alineación derecha**

La alineación derecha es la mejor opción para los datos numéricos, especialmente [las columnas de datos numéricos.](ctrl-text-boxes.md) La alineación derecha también funciona bien para [los botones de](glossary.md) confirmación, así como para los controles alineados con el borde de la ventana derecha.

![captura de pantalla del botón de flecha abajo de búsqueda avanzada ](images/vis-layout-image28.png)

En este ejemplo, el control de divulgación progresiva de búsqueda avanzada está alineado correctamente porque se coloca en el borde de la ventana derecha.

**Alineación del centro**

La alineación central se reserva mejor para situaciones en las que la alineación izquierda o derecha no es adecuada o parece desequilibrada.

![captura de pantalla de los controles del reproductor multimedia centrado ](images/vis-layout-image29.png)

En este ejemplo, el control del reproductor multimedia se centra para proporcionar una apariencia equilibrada.

No centre el contenido de la ventana solo para rellenar el espacio.

**Incorrecto:**

![captura de pantalla de una ventana con demasiado espacio en blanco ](images/vis-layout-image30.png)

En este ejemplo, el contenido se centra incorrectamente en una ventana de tamaño ajustable para rellenar el espacio.

### <a name="vertical-alignment"></a>Alineación vertical

**Elementos superiores**

Debido al orden de lectura de arriba a abajo, la alineación superior funciona bien para la mayoría del contenido. La alineación superior facilita el examen horizontal de los elementos de la interfaz de usuario.

**Líneas base de texto**

Al alinear verticalmente los controles con texto, alinee las líneas base de texto para proporcionar un flujo de lectura horizontal suave.

**Correcto:**

![captura de pantalla de botón y texto de etiqueta alineado ](images/vis-layout-image31.png)

**Incorrecto:**

![captura de pantalla del botón y texto de etiqueta no alineado ](images/vis-layout-image32.png)

En el ejemplo correcto, el control y su etiqueta se alinean verticalmente por sus líneas base de texto.

Sabe que un diseño tiene una buena alineación cuando:

-   Es fácil examinar horizontal y verticalmente.
-   Tiene una apariencia visual simple.

### <a name="label-alignment"></a>Alineación de etiquetas

Las reglas generales de alineación se aplican a las etiquetas de control, pero es un problema común merecedor de atención específica. La alineación de etiquetas tiene estos objetivos:

-   Facilitar el examen vertical para encontrar el control correcto.
-   Facilitar el examen horizontal para asociar etiquetas a sus controles.
-   Facilidad de localización, control de etiquetas que difieren en longitud entre idiomas.
-   Funciona bien con una combinación de diferentes longitudes de etiqueta.
-   Hace un uso eficaz del espacio disponible y evita el texto truncado.

El objetivo general es reducir la cantidad de movimiento de los ojos necesario para encontrar lo que es probable que busquen los usuarios, pero la naturaleza de los controles y lo que buscan los usuarios depende del contexto.

Hay cuatro estilos comunes de colocación y alineación de etiquetas, cada uno con sus ventajas:

-   Etiquetas justificadas a la izquierda sobre los controles
-   Etiquetas justificadas a la izquierda a la izquierda de los controles
-   Etiquetas justificadas a la izquierda de los controles, controles desiguales a la izquierda
-   Etiquetas justificadas a la derecha a la izquierda de los controles

**Etiquetas justificadas a la izquierda sobre los controles**

Este estilo es el más fácil de localizar porque el diseño no depende de la longitud de las etiquetas, pero ocupa el espacio más vertical.

![lista con dos columnas de etiquetas por encima de los controles ](images/vis-layout-image33.png)

Este estilo toma el espacio más vertical, pero es más fácil de encontrar. Es una mejor opción para etiquetar principalmente controles interactivos.

Se usa mejor cuando:

-   Los controles que se etiquetan son interactivos (no solo texto).
-   La interfaz de usuario se localizará. Este estilo a menudo ofrece espacio para duplicar o incluso triplicar la longitud de la etiqueta.
-   La interfaz de usuario usa una tecnología de diseño fijo (como Win32).
-   Hay diez controles o menos. Con más controles, las etiquetas son difíciles de examinar.
-   Hay suficiente espacio vertical para alojar las etiquetas.
-   El diseño debe ser de forma libre, no solo columnas.

**Etiquetas justificadas a la izquierda a la izquierda de los controles**

Este estilo es el más fácil de examinar verticalmente y también funciona bien cuando las etiquetas difieren mucho en longitud, pero es más difícil asociar la etiqueta a su control. Este estilo puede usar etiquetas de varias líneas si es necesario.

![lista con cuatro columnas de etiquetas a la izquierda de los controles ](images/vis-layout-image34.png)

Este estilo funciona bien. Sin embargo, hay dos columnas, pero visualmente parece que hay cuatro, lo que hace que los datos parezcan más complejos.

Se usa mejor cuando:

-   Es probable que los usuarios analicen verticalmente para buscar etiquetas específicas.
-   Es probable que los usuarios no lean las etiquetas y los controles de izquierda a derecha, de arriba a abajo.
-   Hay suficiente espacio horizontal para alojar las etiquetas.
-   Las etiquetas varían significativamente de longitud.
-   Hay muchos controles, como con formularios.
-   Hay pocas columnas. Visualmente, las etiquetas y los controles aparecen como dos columnas individuales.

**Etiquetas justificadas a la izquierda de los controles, controles desiguales a la izquierda**

Este estilo facilita el examen de las etiquetas verticalmente y las etiquetas y controles horizontalmente, y es muy eficiente en el espacio. pero es más difícil examinar los controles verticalmente. Los controles se justifican a la derecha para aprovechar al máximo el espacio disponible.

![lista de dos columnas de etiquetas con controles desiguales ](images/vis-layout-image35.png)

Este estilo es compacto y fácil de leer, pero es difícil examinar los controles verticalmente.

Se usa mejor cuando:

-   La interfaz de usuario usa una tecnología de diseño variable (por ejemplo, Windows Presentation Foundation).
-   Es probable que los usuarios analicen verticalmente para buscar etiquetas específicas.
-   Es probable que los usuarios lean las etiquetas y los controles de izquierda a derecha, de arriba a abajo.
-   Es probable que los usuarios no analicen los controles verticalmente.
-   El texto del control varía de longitud y probablemente se truncaría si se usara otro estilo.
-   Los controles son de solo lectura, como cuadros de texto de solo lectura. Para otros controles, esta alineación tendrá un aspecto poco sencillo. Sin embargo, los controles pueden ser editables al hacer clic.
-   Hay muchas columnas, pero pocos controles en una columna.

**Etiquetas justificadas a la derecha a la izquierda de los controles**

Este estilo es el más fácil de leer horizontalmente para asociar las etiquetas a sus controles, pero es difícil examinar las etiquetas verticalmente y no funciona bien cuando labelsList con etiquetas con sangría y controles difieren en gran medida en longitud.

![lista con controles y etiquetas con sangría ](images/vis-layout-image36.png)

Este estilo permite un examen vertical sencillo de los controles, pero dificulta el examen vertical de las etiquetas.

Se usa mejor cuando:

-   Es probable que los usuarios lean las etiquetas y los controles de izquierda a derecha, de arriba a abajo.
-   Es probable que los usuarios no analicen verticalmente para buscar etiquetas específicas, posiblemente porque:
    -   Hay pocos controles.
    -   Las etiquetas son conocidas.
    -   Los controles son principalmente autoexplicativos y rara vez están en blanco (posiblemente con valores predeterminados para evitar controles en blanco).
-   Hay suficiente espacio horizontal para alojar las etiquetas.
-   Las etiquetas no varían significativamente de longitud.
-   Hay muchas columnas. Visualmente, las etiquetas y los controles aparecen como una sola columna.

Sin embargo, antes de adoptar cualquiera de estos estilos, tenga en cuenta dos factores más:

-   Prefiere un estilo que pueda usar de forma coherente en todo el programa.
-   Las etiquetas que se justifican a la izquierda o los controles situados a la izquierda de los controles son los estilos más comunes, por lo que se les debe dar preferencia.

### <a name="balance"></a>Saldo

Una ventana o página tiene un equilibrio cuando su contenido aparece distribuido uniformemente en su superficie. Si la superficie tuviera físicamente la misma ponderación que visualmente, un diseño equilibrado no se voltearía a un lado.

El problema de equilibrio más común es tener demasiado contenido en el lado izquierdo de una ventana o página. Puede crear el equilibrio de las maneras siguientes:

-   Usar márgenes más grandes en el lado izquierdo que en la derecha.
-   Colocación de elementos de interfaz de usuario usados para completar una tarea a la derecha.
-   Colocación de elementos de interfaz de usuario usados en toda la tarea en el centro.
-   Longitud de controles de varias líneas o de tamaño variable.
-   Usar la alineación del centro estratégicamente.

![captura de pantalla de la impresora a la izquierda y texto a la derecha ](images/vis-layout-image37.png)

Este diseño de página del asistente bien equilibrado muestra un margen izquierdo mayor que el derecho para mejorar el equilibrio.

Si estas técnicas no logran el equilibrio, considere la posibilidad de reducir el ancho de la ventana o página para que coincida mejor con su contenido.

En el caso de las superficies que se pueden cambiar de tamaño, no centre el contenido solo para lograr el equilibrio. En su lugar, mantenga un origen superior izquierdo fijo, defina un área de superficie máxima y equilibra el contenido dentro del espacio utilizado.

### <a name="grids"></a>Cuadrículas

Una cuadrícula es un sistema de alineación subyacente invisible. Las cuadrículas pueden ser simétricas, pero las cuadrículas asimétricas también funcionan. Cuando las usa una sola ventana o página, las cuadrículas ayudan a organizar el contenido dentro de una superficie. Cuando se reutilizan, las cuadrículas crean un diseño coherente entre superficies.

El número de líneas de cuadrícula afecta a la percepción de complejidad visual. Un diseño con menos líneas de cuadrícula parece más sencillo que un diseño con más líneas de cuadrícula.

**Visualmente complejo:**

![captura de pantalla del cuadro de diálogo desordenado ](images/vis-layout-image38.png)

**Visualmente sencillo:**

![captura de pantalla del cuadro de diálogo organizado ](images/vis-layout-image39.png)

Las líneas de cuadrícula innecesarias crean complejidad visual.

Sabe que un diseño usa cuadrículas de forma eficaz cuando:

-   Windows o las páginas con contenido o función similares tienen un diseño similar.
-   Los elementos de diseño repetidos aparecen en ubicaciones similares en ventanas y páginas.
-   No hay líneas de cuadrícula de alineación verticales y horizontales innecesarias.

### <a name="visual-simplicity"></a>Simplicidad visual

La simplicidad visual es la percepción de que un diseño no es más complicado de lo que debe ser.

Sabe que un diseño tiene simplicidad visual cuando:

-   Elimina las capas innecesarias de chrome de la ventana.
-   Presenta el contenido usando como máximo siete grupos fácilmente identificables.
-   Usa agrupaciones ligeras, como diseño y separadores en lugar de cuadros de grupo.
-   Usa controles ligeros, como vínculos en lugar de botones de comando para comandos secundarios, y listas desplegables en lugar de listas para las opciones.
-   Reduce el número de líneas de cuadrícula de alineación vertical y horizontal.
-   Reduce el número de tamaños de control, por ejemplo, usando solo uno o dos anchos de botón de comando en una superficie.
-   Usa la divulgación progresiva para ocultar los elementos de la interfaz de usuario hasta que se necesiten.
-   Usa espacio suficiente para que la ventana o página no se sienta cómodo.
-   Tamaños adecuados de las ventanas y los controles para eliminar el desplazamiento innecesario.
-   Usa una sola fuente con un pequeño número de tamaños y colores de texto.

Como regla general, si se puede eliminar un elemento de diseño sin dañar la eficacia de la interfaz de usuario, probablemente debería serlo.

## <a name="guidelines"></a>Directrices

### <a name="screen-resolution-and-dpi"></a>Resolución de pantalla y ppp

-   **Admite la resolución efectiva mínima de Windows de 800 x 600 píxeles.** En el caso de las URI críticas que deben funcionar en modo seguro, admite una resolución efectiva de 640 x 480 píxeles. Asegúrese de tener en cuenta el espacio utilizado por la barra de tareas reservando 48 píxeles [relativos](glossary.md) verticales para las ventanas mostradas con la barra de tareas.
-   **Optimice los diseños de ventana de tamaño ajustable para una resolución efectiva de 1024 x 768 píxeles.** Cambie automáticamente el tamaño de estas ventanas para obtener resoluciones de pantalla inferiores de forma que todavía sea funcional.
-   **Asegúrese de probar las ventanas en los modos de 96 puntos por pulgada (ppp) (a 800 x 600 píxeles), 120 ppp (a 1024 x 768 píxeles) y 144 ppp (a 1200 x 900 píxeles).** Compruebe si hay problemas de diseño, como el recorte de controles, texto y ventanas, y la extensión de iconos y mapas de bits.
-   **Para los programas con escenarios de uso táctil y móvil, optimice para 120 ppp.** Actualmente, las pantallas de valores altos de ppp son frecuentes en equipos táctiles y móviles.

### <a name="window-size"></a>Tamaño de la ventana

-   **Elija un tamaño de ventana predeterminado adecuado para su contenido.** No tenga miedo de usar tamaños de ventana iniciales mayores si puede usar el espacio de forma eficaz.
-   **Use una relación de aspecto de alto a ancho equilibrada.** Se prefiere una relación de aspecto entre 3:5 y 5:3, aunque se puede usar una relación de aspecto de 1:3 para los cuadros de diálogo de mensaje (como errores y advertencias).
-   **Use ventanas de tamaño ajustable siempre que sea práctico para evitar barras de desplazamiento y datos truncados.** Las ventanas con contenido dinámico, documentos, imágenes, listas y árboles son las que más se benefician de las ventanas de tamaño ajustable.
-   **En el caso de los documentos de texto,** considere la posibilidad de una longitud de línea máxima de 80 caracteres para facilitar la lectura del texto. (Los caracteres incluyen letras, signos de puntuación y espacios).
-   Ventanas de tamaño fijo:
    -   **Las ventanas de tamaño fijo deben ser totalmente visibles y ajustarse al área de trabajo.**
-   Ventanas de tamaño ajustable:
    -   **Las ventanas que se pueden cambiar de tamaño se pueden optimizar para resoluciones más altas, pero se puede cambiar el tamaño según sea necesario en tiempo de presentación a la resolución de pantalla real.**
    -   **Los tamaños de ventana cada vez más grandes deben mostrar más información progresivamente.** Asegúrese de que al menos una parte o control de la ventana tiene contenido que se puede tamaño.
    -   **Mantenga el origen superior izquierdo del contenido fijo a medida que se cambia el tamaño de la ventana.** No mueva el origen para equilibrar el contenido a medida que cambia el tamaño de la ventana.
    -   **Establezca un tamaño de contenido máximo si el contenido puede estar demasiado extendido demasiado ancho.** Si el contenido se vuelve difícil de manejar, no cambie el tamaño del área de contenido más allá de su ancho máximo ni cambie el origen del contenido a medida que la ventana cambia de tamaño. En su lugar, mantenga un ancho máximo y un origen fijo superior izquierdo.
    -   **Establezca un tamaño mínimo de ventana si hay un tamaño por debajo del cual el contenido ya no se puede utilizar.** Para los controles que se pueden cambiar de tamaño, establezca los tamaños mínimos de elementos que se pueden cambiar de tamaño en sus tamaños funcionales más pequeños, como los anchos de columna funcionales mínimos en las vistas de lista. Los elementos opcionales de la interfaz de usuario se deben quitar completamente.
    -   **Considere la posibilidad de modificar la presentación para que el contenido se pueda usar en tamaños más pequeños.**

        ![captura de pantalla de los controles del reproductor multimedia ](images/vis-layout-image16.png)

        En este ejemplo, Reproductor de Windows Media cambia su formato cuando la ventana se vuelve demasiado pequeña para el formato estándar.

### <a name="control-size"></a>Tamaño del control

-   **Haga que todos los controles interactivos se hagan al menos 16 x 16 píxeles relativos.** Esto funciona bien para todos los dispositivos de entrada, incluida la tableta Windows y la tecnología táctil.
-   **Controles de tamaño para evitar datos truncados.** No truncar los datos que se deben leer para realizar una tarea. Columnas de vista de lista de tamaño para evitar datos truncados.
-   **Controles de tamaño para eliminar el desplazamiento innecesario.** Si lo hace, haga que los controles sea ligeramente más grandes, se elimina una barra de desplazamiento. Debe haber pocas barras de desplazamiento verticales y ninguna barra de desplazamiento horizontal innecesaria.

    ![captura de pantalla de tamaño de lista para evitar una barra de desplazamiento ](images/vis-layout-image40.png)

    En este ejemplo, el tamaño de la lista desplegable es para eliminar la barra de desplazamiento.

-   **Reduzca el número de tamaños de control en una superficie.** Prefiere usar los [tamaños de control recomendados estándar](#recommended-sizing-and-spacing) y, cuando sea necesario, use algunos controles de tamaño constante más grandes o más pequeños. Intente usar un ancho único para los cuadros de lista y las vistas de árbol, y no más de tres anchos para los botones de comando y las listas desplegables. Sin embargo, los anchos de cuadro de texto y cuadro combinado deben sugerir la longitud de la entrada más larga o esperada.

    ![captura de pantalla del cuadro de diálogo con listas y botones ](images/vis-layout-image41.png)

    En este ejemplo, se usa un cuadro de lista y un tamaño de botón de comando de forma coherente.

-   **Para los controles que tienen un tamaño en función de su texto, incluya un 30 % adicional (hasta un 200 % para texto más corto) para cualquier texto que se va a localizar.** En esta guía se da por supuesto que el diseño está diseñado con texto en inglés. Tenga en cuenta también que esta directriz hace referencia al texto localizado, no a los números.
-   **Extienda los controles de texto estático, las casillas y los botones de radio al ancho máximo que cabe en el diseño.** De este modo, se evita el truncamiento del texto de longitud variable y la localización.

    **Incorrecto:**

    ![captura de pantalla del control de progreso y texto parcial ](images/vis-layout-image42.png)

    En este ejemplo, el texto del control se trunca innecesariamente.

### <a name="control-spacing"></a>Espaciado de control

-   **Si los controles no se tocan, tenga al menos 3 ARCHIVOS DLL (5 píxeles relativos) de espacio entre ellos.** De lo contrario, los usuarios pueden hacer clic en el espacio inactivo entre los controles. Dado que hacer clic en el espacio inactivo no tiene ningún resultado o comentarios visuales, los usuarios a menudo no saben lo que salió mal.

### <a name="placement"></a>Selección de ubicación

-   **Organice los elementos de la interfaz de usuario dentro de una superficie para que fluyan de forma natural en un orden de izquierda a derecha, de arriba a abajo (en las culturas occidental).** La colocación de los elementos de la interfaz de usuario transmite su relación y debe reflejar los pasos para realizar la tarea.
-   **Coloque los elementos de la interfaz de usuario que inician una tarea en la esquina superior izquierda o en el centro superior.** Dé al elemento de interfaz de usuario que los usuarios deben ver primero el mayor énfasis visual.
-   **Coloque los elementos de la interfaz de usuario que completan una tarea en la esquina inferior derecha.**
-   **Coloque los elementos de la interfaz de usuario relacionados juntos y separe los elementos no relacionados.**
-   **Coloque los pasos necesarios en el flujo principal.**
-   **Coloque pasos opcionales fuera del flujo principal,** posiblemente desacentados mediante un fondo adecuado o una divulgación progresiva.
-   **Coloque los elementos usados con frecuencia antes de los** elementos usados con poca frecuencia en la ruta de acceso del examen.

### <a name="focus"></a>Foco

-   **Elija un único elemento de interfaz de usuario que los usuarios deben mirar primero para ser el punto focal.** El punto focal debe ser algo importante que los usuarios necesitan encontrar y comprender rápidamente.
-   **Coloque el punto focal en la esquina superior izquierda o en el centro superior.**
-   **Dé al punto focal el mayor énfasis visual,** como texto destacado, selección predeterminada o foco de entrada inicial.

### <a name="alignment"></a>Alignment

-   Normalmente, use la alineación izquierda.
-   Use la alineación correcta para los datos numéricos, especialmente las columnas de datos numéricos.
-   Use la alineación derecha para los botones de confirmación, así como los controles alineados con el borde de la ventana derecha.
-   Use la alineación central cuando la alineación izquierda o derecha sea inapropiada o parezca desequilibrada.
-   Al alinear verticalmente los controles con texto, alinee las líneas base de texto para proporcionar un flujo de lectura horizontal suave.
-   Para la alineación de etiquetas, consulte la sección [Alineación de etiquetas](#label-alignment) en Conceptos de diseño.

### <a name="accessibility"></a>Accesibilidad

-   **No use el diseño como único medio para transmitir información importante sobre una interfaz de usuario.** Es posible que los usuarios con discapacidades visuales no puedan interpretar esta presentación. Por ejemplo, asegúrese de que las etiquetas de controles comunican su relación con otros elementos.
-   **No inserte controles subordinados dentro de las etiquetas de control para crear una frase o frase.** Estas asociaciones se basan exclusivamente en el diseño y no se controlan bien mediante la navegación mediante el teclado o las tecnologías de asistencia de accesibilidad. Además, esta técnica no es localizable porque la estructura de oraciones varía según el lenguaje.

    **Incorrecto:**

    ![captura de pantalla de un cuadro de texto en medio de una frase ](images/vis-layout-image43.png)

    En este ejemplo, el cuadro de texto se coloca incorrectamente dentro de la etiqueta de casilla.

    **Correcto:**

    ![captura de pantalla de un cuadro de texto al final de una frase ](images/vis-layout-image44.png)

    En este caso, el cuadro de texto se coloca después de la etiqueta de casilla.

-   **Haga que la agrupación sea accesible.** Los grupos definidos por paneles de ventana, cuadros de grupo, separadores, etiquetas de texto y agregadores se controlan automáticamente mediante las ayuda de accesibilidad. Sin embargo, los grupos definidos solo por ubicación y fondos no lo son y deben definirse mediante programación para la accesibilidad.

Para obtener más instrucciones, vea [Accesibilidad.](inter-accessibility.md)

## <a name="recommended-sizing-and-spacing"></a>Tamaño y espaciado recomendados

**Control del tamaño**

En la tabla siguiente se enumeran los tamaños recomendados (ancho x alto o alto si es un número único) para los elementos comunes de la interfaz de usuario (para 9 pt. Segoe UI 96 ppp). Los anchos basados en el elemento más largo en inglés agregan un 30 por ciento para la localización (hasta un 200 por ciento para texto más corto) para cualquier texto (pero no números) que se localizará.



| Ejemplo | Control | Unidades de diálogo | Píxeles relativos |
|-------------------------------------------------------------------------------------------------|----------------------------|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| ![captura de pantalla de las casillas y sus etiquetas ](images/vis-layout-image45.png)<br/>       | Casillas<br/>     | 10<br/>                                                                                     | 17<br/>                                                                                              |
| ![captura de pantalla del cuadro combinado ](images/vis-layout-image46.png)<br/>                          | Cuadros combinados<br/>     | ancho del elemento más largo + 30 % x 14<br/>                                                       | ancho del elemento más largo + 30 % x 23<br/>                                                                |
| ![captura de pantalla de un botón de comando ](images/vis-layout-image47.png)<br/>                   | Botones de comando<br/> | 50 x 14<br/>                                                                                | 75 x 23<br/>                                                                                         |
| ![captura de pantalla de uno de los dos vínculos de comando seleccionados ](images/vis-layout-image48.png)<br/>  | Vínculos de comandos<br/>   | 25 (una línea) o 35 (dos líneas)<br/>                                                        | 41 (una línea) o 58 (dos líneas)<br/>                                                                 |
| ![captura de pantalla de una lista desplegable ](images/vis-layout-image49.png)<br/>                   | Listas desplegables<br/> | ancho de los datos válidos más largos + 30 % x 14<br/>                                                 | ancho del elemento más largo + 30 % x 23<br/>                                                                |
| ![captura de pantalla de un cuadro de lista ](images/vis-layout-image50.png)<br/>                         | Cuadros de lista<br/>      | ancho del elemento más largo + 30 % x un número entero de elementos (3 elementos como mínimo)<br/>            |                                                                                                            |
| ![captura de pantalla de una lista de archivos de imagen ](images/vis-layout-image51.png)<br/>            | Vistas de lista<br/>      | anchos de columnas que evitan datos truncados x un número entero de elementos<br/>                 |                                                                                                            |
| ![captura de pantalla de una barra de progreso ](images/vis-layout-image52.png)<br/>                     | Barras de progreso<br/>   | 107 o 237 x 8<br/>                                                                         | 160 o 355 x 15<br/>                                                                                 |
| ![captura de pantalla de botones de radio ](images/vis-layout-image53.png)<br/>                      | Botones de radio<br/>   | 10<br/>                                                                                     | 17<br/>                                                                                              |
| ![captura de pantalla del control deslizante ](images/vis-layout-image54.png)<br/>                     | Controles deslizantes<br/>         | 15<br/>                                                                                     | 24<br/>                                                                                              |
| ![captura de pantalla de texto: "seleccionar zona horaria" ](images/vis-layout-image55.png)<br/>           | Texto (estático)<br/>   | 8<br/>                                                                                      | 13<br/>                                                                                              |
| ![captura de pantalla del cuadro de texto vacío ](images/vis-layout-image56.png)<br/>                     | Cuadros de texto<br/>      | ancho de entrada más larga o esperada + 30 % x 14 (una línea) + 10 para cada línea adicional<br/> | ancho de datos válidos más largos + 30 % x 23 píxeles relativos (una línea) + 16 para cada línea adicional<br/> |
| ![captura de pantalla de carpetas anidadas en el Explorador de Windows ](images/vis-layout-image57.png)<br/> | Vistas de árbol<br/>      | ancho del elemento más largo + 30 % x un número entero de elementos (5 elementos como mínimo)<br/>            |                                                                                                            |



 

**Espaciado**

En la tabla siguiente se muestra el espaciado recomendado entre los elementos comunes de la interfaz de usuario (para 9 puntos. Segoe UI 96 ppp).



|   &nbsp; | Elemento | Unidades de diálogo | Píxeles relativos |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| ![Imagen que muestra el espaciado en los márgenes del cuadro de diálogo ](images/vis_layout_image58.jpeg)<br/>        | Márgenes del cuadro de diálogo<br/>                                                                         | 7 en todos los lados<br/>                                                                 | 11 en todos los lados<br/>                                                                |
| ![Imagen que muestra el espaciado entre etiquetas y controles ](images/vis_layout_image59.jpeg)<br/>  | Entre etiquetas de texto y sus controles asociados (por ejemplo, cuadros de texto y cuadros de lista)<br/> | 3<br/>                                                                              | 5<br/>                                                                              |
| ![Imagen que muestra el espaciado entre controles relacionados ](images/vis_layout_image60.jpeg)<br/>     | Entre controles relacionados<br/>                                                                   | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Imagen que muestra el espaciado entre controles no relacionados ](images/vis_layout_image61.jpeg)<br/>   | Entre controles no relacionados<br/>                                                                 | 7<br/>                                                                              | 11<br/>                                                                             |
| ![Imagen que muestra el espaciado del primer control en un grupo ](images/vis_layout_image62.jpeg)<br/>  | Primer control en un cuadro de grupo<br/>                                                               | 11 hacia abajo desde la parte superior del cuadro de grupo; alinear verticalmente con el título del cuadro de grupo<br/> | 16 hacia abajo desde la parte superior del cuadro de grupo; alinear verticalmente con el título del cuadro de grupo<br/> |
| ![Aa511279.between-related(en-us,MSDN.10).jpg](images/vis_layout_image60.jpeg)<br/>         | Entre controles de un cuadro de grupo<br/>                                                            | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Imagen que muestra el espaciado entre botones ](images/vis_layout_image63.jpeg)<br/>              | Entre botones organizados horizontal o verticalmente<br/>                                        | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Imagen que muestra el espaciado del último control de un grupo ](images/vis_layout_image64.jpeg)<br/>   | Último control en un cuadro de grupo<br/>                                                                | 7 encima de la parte inferior del cuadro de grupo<br/>                                            | 11 encima de la parte inferior del cuadro de grupo<br/>                                           |
| ![Imagen que muestra el espaciado desde el borde izquierdo del cuadro de grupo ](images/vis_layout_image65.jpeg)<br/>  | Desde el borde izquierdo de un cuadro de grupo<br/>                                                          | 6<br/>                                                                              | 9<br/>                                                                              |
| ![Imagen que muestra el espaciado de la etiqueta de texto junto al control ](images/vis_layout_image66.jpeg)<br/> | Etiqueta de texto junto a un control<br/>                                                                | 3 hacia abajo desde la parte superior del control<br/>                                             | 5 hacia abajo desde la parte superior del control<br/>                                             |
| ![Imagen que muestra el espaciado entre párrafos de texto ](images/vis_layout_image67.jpeg)<br/>   | Entre párrafos de texto<br/>                                                                 | 7<br/>                                                                              | 11<br/>                                                                             |
|                                                                                                   | Espacio más pequeño entre controles interactivos<br/>                                                | 3 o ningún espacio<br/>                                                                  | 5 o ningún espacio<br/>                                                                  |
|                                                                                                   | Espacio más pequeño entre un control no interactivo y cualquier otro control<br/>                     | 2<br/>                                                                              | 3<br/>                                                                              |



 

 

