---
title: Diseño
description: El diseño es el tamaño, el espaciado y la ubicación del contenido dentro de una ventana o página.
ms.assetid: 39cd896f-d3cc-4768-a20c-a7f598da7136
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: f6b33375cbb679cc7c7efdeb12e5cd30be6280c5
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104279751"
---
# <a name="layout"></a>Diseño

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

El diseño es el tamaño, el espaciado y la ubicación del contenido dentro de una ventana o página. El diseño efectivo es fundamental para ayudar a los usuarios a encontrar lo que buscan rápidamente, así como a hacer que la apariencia sea visualmente atractiva. Un diseño efectivo puede dificultar la diferencia entre los diseños que los usuarios entienden inmediatamente y los que dejan que los usuarios se hagan puzzles y abrumados.

**Nota:** Las instrucciones relacionadas con la [Administración de ventanas](win-window-mgt.md) se presentan en un artículo independiente. El tamaño y el espaciado de los controles específicos recomendados se presentan en sus respectivos artículos de directrices.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="visual-hierarchy"></a>Jerarquía visual

Una ventana o página tiene una jerarquía de objetos visuales claros cuando su apariencia indica la relación y la prioridad de sus elementos. Sin una jerarquía visual, los usuarios tendrían que averiguar estas relaciones y prioridades.

La jerarquía visual se logra mediante skillfully combinando los siguientes atributos:

-   **Foco.** El diseño indica dónde deben buscar primero los usuarios.
-   **Transmite.** El ojo fluye suavemente y de forma natural por una ruta de acceso clara a través de la superficie, buscando elementos de la interfaz de usuario (UI) en el orden adecuado para su uso.
-   **Agrupación.** Los elementos de la interfaz de usuario relacionados lógicamente tienen una relación visual clara. Los elementos relacionados se agrupan; los elementos no relacionados son independientes.
-   **Atención.** Los elementos de la interfaz de usuario se resaltan en función de su importancia relativa.
-   **Ecuación.** Los elementos de la interfaz de usuario tienen una ubicación coordinada, por lo que son fáciles de examinar y aparecen ordenadas.

Además, el diseño efectivo tiene estos atributos:

-   **Independencia del dispositivo.** El diseño aparece según lo previsto, independientemente del tamaño o el tipo de letra de la fuente, los puntos por pulgada (PPP), la pantalla o el adaptador de gráficos.
-   **Análisis sencillo.** Los usuarios pueden encontrar el contenido que buscan de un vistazo.
-   **Eficiente.** Los elementos de la interfaz de usuario que son grandes deben ser grandes y los elementos que son pequeños funcionan bien pequeños.
-   **Resizability.** Si es útil, se redimensiona una ventana y su diseño de contenido es efectivo independientemente de si la superficie es grande o pequeña.
-   **Balancea.** El contenido aparece distribuido uniformemente en toda la superficie.
-   **Simplicidad visual.** La percepción de que un diseño no es más complicada de lo que debe ser. Los usuarios no se sienten abrumados por la apariencia del diseño.
-   **Coherencia.** Las ventanas o páginas similares usan un diseño similar, por lo que los usuarios siempre se sienten orientados.

Al ajustar el tamaño, el espaciado y la ubicación son conceptos simples, el reto con el diseño es lograr la combinación correcta de estos atributos.

En Windows, el diseño se comunica mediante métricas independientes del dispositivo, como unidades de cuadro de diálogo (DLU) y píxeles relativos.

### <a name="a-design-model-for-reading"></a>Un modelo de diseño para leer

**Los usuarios eligen lo que leen la organización y la apariencia del contenido.** Para crear un diseño efectivo, deberá comprender lo que los usuarios suelen leer y por qué.

Puede tomar decisiones de diseño mediante este modelo de diseño para la lectura:

-   Las personas leen en orden de izquierda a derecha y de arriba abajo (en las culturas occidentales).
-   Hay dos modos de lectura: lectura y análisis envolventes. El objetivo de la lectura envolvente es la comprensión.

    ![Ilustración de la flecha roja en el patrón de lectura en zigzag ](images/vis-layout-image1.png)

    Este diagrama modela la lectura envolvente.

    Por el contrario, el objetivo del análisis es localizar cosas. La ruta de acceso de análisis general tiene el siguiente aspecto:

    ![figura de la flecha roja en el patrón de lectura diagonal ](images/vis-layout-image2.png)

    Este diagrama modela el examen.

    ![figura de la flecha roja en un patrón hacia abajo y arco ](images/vis-layout-image3.png)

    Si hay texto en ejecución a lo largo del borde izquierdo de una página, los usuarios examinan el borde izquierdo en primer lugar.

-   Cuando se usa software, los usuarios no se sumergin en la propia interfaz de usuario, sino en su trabajo. Por lo tanto, los usuarios no suelen leer el texto de la interfaz de usuario que lo examinan. Después, leen los bits de texto de una sola vez cuando crean que necesitan.
-   Los usuarios tienden a omitir los paneles de navegación a la izquierda o a la derecha de una página. Los usuarios reconocen que están allí, pero examinan los paneles de navegación solo cuando quieren navegar.
-   Los usuarios tienden a omitir grandes bloques de texto sin formato sin leerlos.

    ![Ilustración del texto con flechas que muestran texto digitalizado ](images/vis-layout-image4.png)

    Los usuarios tienden a omitir grandes bloques de texto y paneles de navegación cuando se examinan.

-   Todo lo que es igual, los usuarios primero buscan en la esquina superior izquierda de una ventana, digitalizan a través de la página y finalizan el examen en la esquina inferior derecha. Tienden a omitir la esquina inferior izquierda.

    ![figura de la página y la flecha superior izquierda a derecha inferior ](images/vis-layout-image5.png)

    Todo lo que sea igual, los usuarios leerán estos números en el siguiente orden: 1, 2, 4 y 3.

-   Pero en la interfaz de usuario interactiva, no todas las cosas son iguales, por lo que los distintos elementos de la interfaz de usuario reciben distintos niveles de atención. Los usuarios tienden a mirar en los controles interactivos, especialmente en los controles en la parte superior izquierda y en el centro de la ventana y el texto destacado en primer lugar.

![figura de la pantalla con texto nítido y borroso ](images/vis-layout-image6.png)

Los usuarios se centran en los controles interactivos principales y en la instrucción principal destacada y solo examinan otras cosas cuando necesitan.

-   Los usuarios tienden a leer etiquetas de control interactivas, especialmente las que parecen relevantes para completar la tarea a mano. Por el contrario, los usuarios suelen leer texto estático cuando piensan que necesitan.
-   Elementos que parecen tener una atención diferente. El texto en negrita y el texto grande destacan del texto normal. Elementos de la interfaz de usuario con color o en un fondo de color. Los elementos con iconos salen de los elementos sin iconos.
-   Los usuarios no se desplazan a menos que tengan un motivo. Si el contenido que está [por encima del pliegue](glossary.md) no proporciona un motivo para desplazarse, no lo hace.
-   Una vez que los usuarios hayan decidido qué hacer, detendrán inmediatamente el análisis y lo hacen.
-   Dado que los usuarios dejan de examinar cuando piensan que han terminado, tienden a omitir cualquier cosa más allá de lo que parece ser el punto de finalización.

![captura de pantalla de las opciones del teclado ](images/vis-layout-image7.png)

Los usuarios dejan de digitalizar cuando creen que han terminado.

Por supuesto, habrá excepciones a este modelo general. Los dispositivos de seguimiento ocular indican que el comportamiento de los usuarios reales es bastante errático. El objetivo de este modelo es ayudarle a tomar buenas decisiones e inconvenientes, no a modelar el comportamiento del usuario con precisión. Sin embargo, como ha leído esta lista, espero que también haya reconocido muchos de sus propios patrones de lectura.

### <a name="designing-for-scanning"></a>Diseñar para el examen

**Los usuarios no leen, examinan de modo que debería diseñar superficies de la interfaz de usuario para el examen.** No suponga que los usuarios leerán el texto como escrito de izquierda a derecha y de arriba abajo, sino que examinan los elementos de la interfaz de usuario que atraen su atención.

Para diseñar el análisis:

-   Supongamos que los usuarios empiezan con un examen rápido de toda la ventana y, a continuación, leen los elementos de la interfaz de usuario en aproximadamente el orden siguiente:
    -   Controles interactivos en el centro
    -   Botones de confirmación
    -   Controles interactivos que se encuentran en otro lugar
    -   Instrucción principal
    -   Explicaciones complementarias
    -   Texto que se muestra con un icono de advertencia
    -   Título de la ventana
    -   Otro texto estático en el cuerpo principal
    -   Notas al pie
-   Coloque los elementos de la interfaz de usuario que inician una tarea en la esquina superior izquierda o en el centro superior.
-   Coloque los elementos de la interfaz de usuario que completen una tarea en la esquina inferior derecha.
-   Siempre que sea posible, incluya texto fundamental en los controles interactivos en lugar de en texto estático.
-   Evite colocar información fundamental en la esquina inferior izquierda o en la parte inferior de un control o página desplazable larga.
-   No presente grandes bloques de texto. Elimine el texto innecesario. Use el estilo de presentación de [pirámide invertido](text-ui.md) .
-   Si hace algo para atraer la atención de los usuarios, asegúrese de que se garantiza la atención.

Siempre que sea posible, trabaje con este modelo en lugar de combatirlo; pero habrá ocasiones en las que necesite resaltar o deshacer hincapié en determinados elementos de la interfaz de usuario.

Para resaltar los elementos de la interfaz de usuario principales:

-   Coloque los elementos primarios de la interfaz de usuario en la [ruta de exploración](glossary.md).
-   Coloque cualquier interfaz de usuario para iniciar una tarea en la esquina superior izquierda o en el centro superior.
-   Coloque los botones de confirmación en la esquina inferior derecha.
-   Coloque la interfaz de usuario principal restante en el centro.
-   Use controles que atraigan la atención, como botones de comando, vínculos de comandos e iconos.
-   Usar texto destacado, incluido texto de gran tamaño y texto en negrita.
-   Poner texto los usuarios deben leer en los controles interactivos o con iconos o en los [banners](vis-graphic.md).
-   Usar texto oscuro en un fondo claro.
-   Rodea los elementos con un espacio muy amplio.
-   No se requiere ninguna interacción, como señalar o mantener el puntero, para ver el elemento que se está resaltando.

    ![captura de pantalla de las opciones de activación de Windows ](images/vis-layout-image8.png)

    En este ejemplo se muestran muchas maneras de resaltar los elementos de la interfaz de usuario principales.

Para deshacer hincapié en los elementos de la interfaz de usuario secundaria:

-   Coloque los elementos de la interfaz de usuario secundarios fuera de la ruta de exploración.
-   Ponga todo lo que los usuarios no suelen necesitar para verlos en la esquina inferior izquierda o en la parte inferior de la ventana.
-   Use controles que no atraigan la atención, como los vínculos de tarea en lugar de los botones de comando.
-   Use texto normal o gris.
-   Usar texto claro en un fondo oscuro. El texto blanco sobre un fondo gris oscuro o azul funciona bien.
-   Rodee los elementos con espacio mínimo.
-   Considere la posibilidad de usar la [divulgación progresiva](ctrl-progressive-disclosure-controls.md) para ocultar los elementos de la interfaz de usuario secundaria.

    ![captura de pantalla de elementos de interfaz grandes y pequeños ](images/vis-layout-image9.png)

    En este ejemplo se muestran muchas maneras de anular el resaltado de los elementos de la interfaz de usuario secundaria.

### <a name="using-screen-space-effectively"></a>Uso eficaz del espacio de pantalla

El uso eficaz del espacio de pantalla requiere el equilibrio de varios factores: usar demasiado espacio y una ventana tiene una gran pérdida de tiempo, e incluso es difícil de usar según la [ley de Fitts](inter-mouse.md).

**Incorrecto:**

![captura de pantalla que muestra demasiado espacio en blanco ](images/vis-layout-image10.png)

En este ejemplo, la ventana es demasiado grande para su contenido.

Por otro lado, use un poco de espacio y una ventana cree estorban, incómodo y intimidante, y difícil de usar si requiere desplazamiento y otras manipulaciones.

**Incorrecto:**

![captura de pantalla con demasiados controles ](images/vis-layout-image11.png)

En este ejemplo, la ventana es demasiado pequeña para su contenido.

Aunque la interfaz de usuario crítica debe ajustarse a la [resolución efectiva](glossary.md)mínima admitida, no suponga que el uso del espacio de pantalla de forma eficaz significa que Windows debe ser lo más pequeño posible. **El diseño efectivo tiene en cuenta el espacio abierto y no intenta CRAM todo en el espacio más pequeño posible.** Las pantallas modernas tienen un espacio de pantalla significativo y tienen sentido usar este espacio eficazmente cuando se puede. Por lo tanto, se trata de un error en el lado de usar demasiado espacio de pantalla en lugar de un poco. De este modo, su sensación de Windows es más clara y más accesible.

Sabe que un diseño utiliza eficazmente el espacio de pantalla cuando:

-   No es necesario cambiar el tamaño de las ventanas, los paneles de ventana y los controles para poder usarlos. Si lo primero que hacen los usuarios es cambiar el tamaño de una ventana, panel o control, su tamaño es incorrecto.
-   Los datos no se truncan. La mayoría de los datos de las vistas de lista y de árbol no tienen puntos suspensivos, y los datos de otros controles no se recortan a menos que la longitud de los datos sea inusualmente grande. Los datos que deben leerse para realizar una tarea no se deben truncar.
-   Las ventanas y los controles tienen el tamaño adecuado para eliminar el desplazamiento innecesario. Hay algunas barras de desplazamiento horizontales y no hay barras de desplazamiento verticales innecesarias.
-   Los controles usan principalmente sus tamaños estándar. Procure reducir el número de tamaños de control, por ejemplo, usando solo uno o dos anchos de botón de comando en una superficie.
-   La superficie de la interfaz de usuario está equilibrada. No hay áreas de pantalla grandes sin usar.

Elija tamaños de ventana que sean lo suficientemente grandes como para cumplir su objetivo. (Y si se cambia el tamaño de la ventana, este objetivo se aplica a su tamaño predeterminado). **Una combinación de datos cortados o barras de desplazamiento y una gran cantidad de espacio disponible en la pantalla es un claro signo de diseño ineficaz.**

### <a name="control-sizing"></a>Control de tamaño

Normalmente, el primer paso en el uso eficaz del espacio de pantalla consiste en determinar el tamaño correcto de los distintos elementos de la interfaz de usuario. Consulte la [tabla de ajuste de tamaño del control](#recommended-sizing-and-spacing) y el ajuste de tamaño recomendado en los artículos de instrucciones de control específicas.

La ley de Fitts indica que el menor destino es, cuanto más tiempo se tarda en adquirirlo con el mouse. Además, en el caso de los equipos que usan la tecnología táctil y de tabletas de Windows, el "Mouse" puede ser un lápiz o el dedo del usuario, por lo que debe tener en cuenta los dispositivos de entrada alternativos al determinar los tamaños de los controles pequeños. **Un tamaño de control de 16x16 píxeles relativos es un buen tamaño mínimo para cualquier dispositivo de entrada.** Por el contrario, los botones de control de giro de píxel relativo 15x9 estándar son demasiado pequeños para que los lápices los usen de manera eficaz.

### <a name="spacing"></a>Espaciado

Proporcionar un espacio generoso (pero no excesivo) hace que el diseño se sienta más cómodo y más fácil de analizar. El espacio efectivo no es el espacio sin usar que desempeña un papel importante en la mejora de la capacidad para que los usuarios examinen y también agregan una apelación visual del diseño. Para obtener instrucciones, consulte la [tabla de espaciado](#recommended-sizing-and-spacing).

En el caso de los equipos que usan la tecnología táctil y tabletas de Windows, el "Mouse" podría ser realmente un lápiz o el dedo del usuario. El destino es más difícil cuando se usa un lápiz o un dedo como dispositivo señalador, lo que da lugar a que los usuarios PUNTEEN fuera del destino previsto. Cuando los controles interactivos se colocan muy cerca, pero no se están tocando realmente, los usuarios pueden hacer clic en el espacio inactivo entre los controles. Puesto que al hacer clic en espacio inactivo no hay ningún resultado ni ningún comentario visual, a menudo los usuarios no están seguro de qué salió mal. Si los controles pequeños están demasiado cerca de un espacio, el usuario debe puntear con precisión para evitar puntear en el objeto equivocado. **Para solucionar estos problemas, las regiones de destino de los controles interactivos deben tocarse o tener al menos 3 DLU (5 píxeles relativos) de espacio entre ellos.**

Sabe que un diseño tiene un buen espaciado cuando:

-   En general, la superficie de la interfaz de usuario se siente cómoda y no se siente estorban.
-   El espacio parece uniforme y equilibrado.
-   Los elementos relacionados están próximos y los elementos no relacionados están relativamente alejados.
-   No hay ningún espacio inactivo entre los controles que están diseñados para ser juntos, como los botones de la barra de herramientas.

### <a name="resizable-windows"></a>Ventanas redimensionables

Las ventanas de tamaño ajustable también son un factor importante para el uso eficaz del espacio de pantalla. Algunas ventanas se componen de contenido fijo y no se benefician del tamaño, pero se debe cambiar el tamaño de las ventanas con contenido de tamaño ajustable. Por supuesto, el motivo por el que los usuarios cambian el tamaño de una ventana es seguir el espacio de la pantalla adicional, por lo que el contenido debe expandirse en consecuencia asignando más espacio a los elementos de la interfaz de usuario que lo necesiten. Las ventanas con contenido dinámico, documentos, imágenes, listas y árboles aprovechan al máximo las ventanas redimensionables.

![captura de pantalla del control cuyo tamaño obtiene la barra de desplazamiento ](images/vis-layout-image12.png)

En este ejemplo, el cambio de tamaño de la ventana cambia el tamaño del control de vista de lista.

Dicho esto, las ventanas se pueden expandir demasiado anchas. Por ejemplo, muchas páginas del panel de control se vuelven difíciles de manejar cuando el contenido es más ancho que 600 píxeles relativos. En este caso, es mejor no cambiar el tamaño del área de contenido más allá de este ancho máximo o cambiar el origen del contenido a medida que se cambia el tamaño de la ventana. En su lugar, conserve un ancho máximo y un origen fijo superior izquierdo.

El texto es difícil de leer a medida que aumenta la longitud de la línea. En el caso de los documentos de texto, considere una longitud de línea máxima de 80 caracteres para facilitar la lectura del texto. (Entre los caracteres se incluyen letras, signos de puntuación y espacios).

**Incorrecto:**

![captura de pantalla de un cuadro de mensaje ancho con texto largo ](images/vis-layout-image13.png)

En este ejemplo, la longitud de texto largo hace que la lectura sea difícil.

Por último, las ventanas redimensionables también necesitan usar el espacio de pantalla de forma eficaz cuando sean más pequeñas, ya que permiten que el contenido de tamaño variable sea más pequeño y quita el espacio de los elementos de la interfaz de usuario que pueden funcionar de forma eficaz sin él. En algún momento, la ventana o sus elementos de la interfaz de usuario se vuelven demasiado pequeños para ser utilizables, por lo que se les debe asignar un tamaño mínimo o algunos elementos deben quitarse por completo.

![captura de pantalla de la ventana con la cinta de opciones alta e intrusiva ](images/vis-layout-image14.png)

![captura de pantalla de la ventana sin cinta de opciones ](images/vis-layout-image15.png)

En este ejemplo, el panel tiene un tamaño mínimo.

Algunos programas se benefician del uso de una presentación completamente diferente para que el contenido se pueda usar en tamaños más pequeños.

![captura de pantalla de los botones del reproductor de media centrado ](images/vis-layout-image16.png)

En este ejemplo, Windows Media Player cambia su formato cuando la ventana se vuelve demasiado pequeña para el formato estándar.

### <a name="focus"></a>Foco

Un diseño tiene el foco cuando hay un lugar obvio en el que buscar primero. El foco es importante para mostrar a los usuarios dónde empezar a examinar la ventana o la página. Sin desenfoque, el ojo del usuario se aimlessly. El punto focal debe ser algo importante que los usuarios necesiten buscar y comprender rápidamente y deben tener el mayor énfasis visual. La esquina superior izquierda es el punto focal natural de la mayoría de las ventanas.

Solo debe haber un punto focal. Al igual que en la vida real, el ojo solo se puede centrar en un elemento a la vez, por lo que los usuarios no pueden centrarse en varios lugares simultáneamente.

Para hacer que un elemento de la interfaz de usuario sea el punto focal, puede proporcionarle el énfasis visual:

-   Colóquelo en la parte superior izquierda o superior del centro de la superficie.
-   Usar controles interactivos que son importantes y comprensibles fácilmente.
-   Usar texto destacado, como una instrucción principal.
-   Proporcionar a los controles la selección predeterminada y el foco de entrada inicial.
-   Colocar los controles en un fondo de color diferente.

Considere la posibilidad de usar Windows Search. El punto focal de la búsqueda de Windows debe ser el cuadro de búsqueda porque es el punto de partida de la tarea. Sin embargo, se encuentra en la esquina superior derecha para que sea coherente con la selección de ubicación del cuadro de búsqueda estándar. El cuadro de búsqueda tiene el foco de entrada, pero dada su ubicación en la ruta de exploración, esta pista no es suficiente.

Para solucionar este problema, hay una instrucción destacada en la parte superior del centro de la ventana para dirigir a los usuarios a la ubicación correcta.

**Aceptable:**

![captura de pantalla del cuadro de diálogo de búsqueda con texto útil ](images/vis-layout-image17.png)

En este ejemplo, una instrucción destacada en la parte superior del centro de la ventana dirige a los usuarios al cuadro de búsqueda.

Sin las instrucciones, la ventana no tendría un punto focal obvio.

**Incorrecto:**

![captura de pantalla del cuadro de diálogo de búsqueda sin texto ](images/vis-layout-image18.png)

Este ejemplo no tiene ningún punto focal obvio. Los usuarios no saben dónde mirar.

Si proporciona un énfasis visual al elemento de la interfaz de usuario, asegúrese de que se garantiza la atención. En el ejemplo de búsqueda de Windows incorrecto anterior, el botón todos resaltado se encuentra en la esquina superior izquierda y tiene el énfasis más visual, pero no es el punto focal deseado. Es posible que los usuarios se queden bloqueados mirando este botón intentando averiguar qué hacer con él.

**Incorrecto:**

![captura de pantalla del botón todos resaltados ](images/vis-layout-image19.png)

Sin la instrucción destacada como el punto focal, el botón todo resaltado es un punto focal involuntaria.

### <a name="flow"></a>Flujo

Un diseño tiene flujo cuando los usuarios se guían de forma fluida y natural por una ruta de acceso clara a través de su superficie, buscando los elementos de la interfaz de usuario en el orden adecuado para su uso. Una vez que los usuarios identifican el punto focal, deben determinar cómo completar la tarea. La colocación de los elementos de la interfaz de usuario transmite su relación y debe reflejar los pasos para realizar la tarea. Normalmente, esto significa que los pasos de la tarea deben fluir de forma natural en orden de izquierda a derecha y de arriba abajo (en las referencias culturales occidentales).

Sabe que un diseño tiene un buen flujo cuando:

-   La colocación de los elementos de la interfaz de usuario refleja los pasos que los usuarios necesitan para realizar la tarea.
-   Los elementos de la interfaz de usuario que inician una tarea se encuentran en la esquina superior izquierda o en el centro superior.
-   Los elementos de la interfaz de usuario que completan una tarea se encuentran en la esquina inferior derecha.
-   Los elementos de la interfaz de usuario relacionados están juntos; los elementos no relacionados son independientes.
-   Los pasos necesarios se encuentran en el flujo principal.
-   Los pasos opcionales están fuera del flujo principal, posiblemente desacentuado mediante el uso de un fondo adecuado o una divulgación progresiva.
-   Los elementos que se usan con frecuencia aparecen antes que los elementos usados con poca frecuencia en la ruta de exploración.
-   Los usuarios siempre saben qué hacer a continuación. No hay saltos o interrupciones inesperados en el flujo de tareas.

**Incorrecto:**

![captura de pantalla del diseño de cuadro de diálogo confuso ](images/vis-layout-image20.png)

En este ejemplo, los usuarios no saben qué hacer a continuación. Hay saltos e interrupciones inesperados en el flujo de tareas.

**Correcto:**

![captura de pantalla de un cuadro de diálogo bien planeado ](images/vis-layout-image21.png)

En este ejemplo, la presentación de los elementos de la interfaz de usuario refleja los pasos para realizar la tarea.

### <a name="grouping"></a>Agrupación

Un diseño tiene agrupación cuando los elementos de la interfaz de usuario relacionados lógicamente tienen una relación visual clara. Los grupos son importantes porque es más fácil para los usuarios comprender y centrarse en un grupo de elementos relacionados que los elementos de forma individual. Los grupos hacen que un diseño parezca más sencillo y fácil de analizar.

Puede mostrar la agrupación de las siguientes maneras (en aumento de la pesada):

-   **Diseño.** Puede agrupar los controles relacionados entre sí y colocar el espaciado adicional entre los controles no relacionados.

    ![figura de cuatro iconos que muestran cuatro grupos de tareas ](images/vis-layout-image22.png)

    En este ejemplo, el diseño solo se usa para mostrar las relaciones de control.

-   **Separadores.** Un separador es una línea horizontal o vertical que unifica un grupo de controles. Los separadores proporcionan un aspecto más sencillo y más limpio. Sin embargo, a diferencia de los cuadros de grupo, funcionan mejor cuando abarcan toda la superficie.

    ![captura de pantalla de tres iconos y tres separadores ](images/vis-layout-image23.png)

    En este ejemplo, se utilizan separadores etiquetados para mostrar las relaciones de control.

-   **Agregadores.** Un agregador es un gráfico que crea una relación visual entre controles relacionados fuertemente.

    ![captura de pantalla de controles dentro de una línea elíptica ](images/vis-layout-image24.png)

    En este ejemplo, se usa un agregador de límites para resaltar la relación entre los controles y hacer que se sientan como un único control en lugar de ocho.

-   **Cuadros de grupo.** Un cuadro de grupo es un marco rectangular con etiqueta que rodea un conjunto de controles relacionados.

    ![captura de pantalla de las casillas en un borde rectangular ](images/vis-layout-image25.png)

    En este ejemplo, un cuadro de grupo rodea y etiqueta un conjunto de controles relacionados.

-   **Fondos.** Puede usar el fondo para resaltar o anular el resaltado de diferentes tipos de contenido.

    ![captura de pantalla del lado izquierdo del panel de control ](images/vis-layout-image26.png)

    En este ejemplo, el panel de tareas del panel de control se utiliza para agrupar tareas relacionadas y elementos del panel de control.

    Para evitar el desorden visual, la mejor opción es la agrupación de peso más claro que realiza el trabajo. Para obtener más información, consulte [cuadros de grupo](ctrl-group-boxes.md), [pestañas](ctrl-tabs.md), [separadores y fondo](vis-graphic.md).

Independientemente del estilo de agrupación, puede utilizar la sangría para mostrar la relación de los controles dentro de un grupo. Los controles que se encuentran entre pares deben estar alineados a la izquierda y se les aplica sangría a los controles dependientes 12 DLU o 18 píxeles relativos.

![captura de pantalla de tres niveles de controles con sangría ](images/vis-layout-image27.png)

A los controles dependientes se les aplica una sangría 12 DLU o 18 píxeles relativos, que por diseño es la distancia entre las casillas y los botones de radio de sus etiquetas.

Sabe que un diseño tiene una agrupación buena cuando:

-   La ventana o las páginas tienen como máximo 7 grupos.
-   El propósito de cada grupo es obvio.
-   La relación de los controles dentro de cada grupo es obvia, especialmente la dependencia del control.
-   La agrupación simplifica el contenido en lugar de hacerlo más complejo.

### <a name="alignment"></a>Alignment

La alineación es la colocación coordinada de los elementos de la interfaz de usuario. La alineación es importante porque facilita el análisis del contenido y afecta a la percepción de la complejidad visual de los usuarios.

Hay varios objetivos que se deben tener en cuenta a la hora de determinar la alineación:

-   **Aceleración horizontal.** Los usuarios pueden leer horizontalmente y buscar elementos relacionados entre sí, sin lagunas difíciles.
-   **Aceleración en el examen vertical.** Los usuarios pueden examinar columnas de elementos relacionados y encontrar inmediatamente lo que buscan, con un movimiento de ojos horizontal mínimo.
-   **Complejidad visual mínima.** Los usuarios perciben que un diseño es visualmente complejo si tiene líneas de cuadrícula de alineación vertical innecesarias.

### <a name="horizontal-alignment"></a>Alineación horizontal

**Alineación izquierda**

Debido al orden de lectura de izquierda a derecha, la alineación izquierda funciona bien para la mayoría de los contenidos. La alineación a la izquierda hace que los datos de columna sean fáciles de examinar verticalmente.

**Alineación a la derecha**

La alineación derecha es la mejor opción para los datos numéricos, especialmente [las columnas de datos numéricos](ctrl-text-boxes.md). La alineación derecha también funciona bien con los [botones de confirmación](glossary.md) , así como con los controles alineados con el borde de la ventana derecha.

![captura de pantalla del botón de flecha abajo de búsqueda avanzada ](images/vis-layout-image28.png)

En este ejemplo, el control de divulgación progresiva de búsqueda avanzada está alineado a la derecha porque se coloca en el borde de la ventana derecha.

**Alineación central**

La alineación central se reserva mejor en situaciones en las que la alineación izquierda o derecha no es adecuada o aparece desequilibrada.

![captura de pantalla de los controles del reproductor multimedia centrados ](images/vis-layout-image29.png)

En este ejemplo, el control de Media Player está centrado para dar una apariencia equilibrada.

No Centre el contenido de la ventana solo para rellenar el espacio.

**Incorrecto:**

![captura de pantalla de una ventana con demasiado espacio en blanco ](images/vis-layout-image30.png)

En este ejemplo, el contenido se centra incorrectamente en una ventana de tamaño variable para rellenar el espacio.

### <a name="vertical-alignment"></a>Alineación vertical

**Lados de elemento**

Debido al orden de lectura de arriba abajo, la alineación superior funciona bien para la mayoría de los contenidos. La alineación superior hace que los elementos de la interfaz de usuario sean fáciles de examinar horizontalmente.

**Líneas base de texto**

Al alinear verticalmente los controles con texto, alinee las líneas de base de texto para proporcionar un flujo de lectura horizontal suave.

**Correcto:**

![captura de pantalla del texto de botón y etiqueta alineado ](images/vis-layout-image31.png)

**Incorrecto:**

![captura de pantalla del texto del botón y etiqueta no alineado ](images/vis-layout-image32.png)

En el ejemplo correcto, el control y su etiqueta se alinean verticalmente por sus líneas base de texto.

Sabe que un diseño tiene buena alineación cuando:

-   Es fácil de examinar tanto horizontal como verticalmente.
-   Tiene un aspecto visual sencillo.

### <a name="label-alignment"></a>Alineación de etiqueta

Las reglas de alineación general se aplican a las etiquetas de control, pero es un problema común que merece la atención específica. La alineación de la etiqueta tiene estos objetivos:

-   Aceleración en el examen vertical para encontrar el control adecuado.
-   Digitalice horizontalmente para asociar etiquetas a sus controles.
-   Facilite la localización y controle las etiquetas que difieren en la longitud entre idiomas.
-   Funciona bien con una mezcla de diferentes longitudes de etiqueta.
-   Hace un uso eficaz del espacio disponible mientras evita texto truncado.

El objetivo general es reducir la cantidad de movimiento de ojo necesario para encontrar lo que probablemente buscan los usuarios, pero la naturaleza de los controles y lo que buscan los usuarios depende del contexto.

Hay cuatro estilos de alineación y colocación de etiquetas comunes, cada uno con sus ventajas:

-   Etiquetas alineadas a la izquierda por encima de los controles
-   Etiquetas justificadas a la izquierda a la izquierda de los controles
-   Etiquetas justificadas a la izquierda a la izquierda de los controles, controles desiguals a la izquierda
-   Etiquetas justificadas a la derecha a la izquierda de los controles

**Etiquetas alineadas a la izquierda por encima de los controles**

Este estilo es el más fácil de localizar porque el diseño no depende de la longitud de las etiquetas, pero ocupa el mayor espacio vertical.

![lista con dos columnas de etiquetas por encima de los controles ](images/vis-layout-image33.png)

Este estilo toma el mayor espacio vertical, pero es más fácil de localizar. Se trata de una opción mejor para etiquetar controles principalmente interactivos.

Se utiliza mejor cuando:

-   Los controles que se etiquetan son interactivos (no solo texto).
-   La interfaz de usuario se traducirá. Este estilo suele ofrecer espacio para doblar o incluso triplicar la longitud de la etiqueta.
-   La interfaz de usuario usa una tecnología de diseño fija (como Win32).
-   Hay diez controles o menos. Con más controles, las etiquetas son difíciles de examinar.
-   Hay suficiente espacio vertical para alojar las etiquetas.
-   El diseño debe ser una forma libre, no solo columnas.

**Etiquetas justificadas a la izquierda a la izquierda de los controles**

Este estilo es el más fácil de examinar verticalmente y también funciona bien cuando las etiquetas difieren en gran medida en la longitud, pero es más difícil asociar la etiqueta a su control. Este estilo puede usar etiquetas de varias líneas si es necesario.

![lista con cuatro columnas de etiquetas a la izquierda de los controles ](images/vis-layout-image34.png)

Este estilo funciona bien. Sin embargo, hay dos columnas, pero visualmente parece que hay cuatro que hacen que los datos parezcan más complejos.

Se utiliza mejor cuando:

-   Es probable que los usuarios examinen verticalmente para encontrar etiquetas específicas.
-   Los usuarios no tienen más probabilidades de leer las etiquetas y los controles de una manera de izquierda a derecha y de arriba a abajo.
-   Hay suficiente espacio horizontal para alojar las etiquetas.
-   Las etiquetas varían significativamente en longitud.
-   Hay muchos controles, como los formularios.
-   Hay pocas columnas. Visualmente, las etiquetas y los controles aparecen como dos columnas individuales.

**Etiquetas justificadas a la izquierda a la izquierda de los controles, controles desiguals a la izquierda**

Este estilo facilita el análisis de las etiquetas verticalmente y las etiquetas y los controles horizontalmente, y tiene un espacio muy eficaz. pero es más difícil examinar los controles verticalmente. Los controles están justificados a la derecha para sacar el máximo partido del espacio disponible.

![lista de dos columnas de etiquetas con controles desiguales ](images/vis-layout-image35.png)

Este estilo es compacto y fácil de leer, pero es difícil examinar los controles verticalmente.

Se utiliza mejor cuando:

-   La interfaz de usuario usa una tecnología de diseño variable (como Windows Presentation Foundation).
-   Es probable que los usuarios examinen verticalmente para encontrar etiquetas específicas.
-   Es probable que los usuarios lean las etiquetas y los controles de una manera de izquierda a derecha y de arriba a abajo.
-   No es probable que los usuarios examinen los controles verticalmente.
-   El texto del control varía en longitud y probablemente se truncaría si se usara otro estilo.
-   Los controles son de solo lectura, como los cuadros de texto de solo lectura. En el caso de otros controles, esta alineación será chapucero. Sin embargo, los controles pueden ser editables al hacer clic.
-   Hay muchas columnas, pero pocos controles en una columna.

**Etiquetas justificadas a la derecha a la izquierda de los controles**

Este estilo es el más fácil de leer horizontalmente para asociar las etiquetas a sus controles, pero es difícil escanear las etiquetas verticalmente y no funciona bien cuando labelsList con etiquetas y controles con sangría difiere en gran medida.

![lista con etiquetas y controles con sangría ](images/vis-layout-image36.png)

Este estilo permite un examen vertical sencillo de los controles, pero dificulta el análisis de las etiquetas verticalmente.

Se utiliza mejor cuando:

-   Es probable que los usuarios lean las etiquetas y los controles de una manera de izquierda a derecha y de arriba a abajo.
-   No es probable que los usuarios examinen verticalmente para encontrar etiquetas específicas, posiblemente porque:
    -   Hay pocos controles.
    -   Las etiquetas son conocidas.
    -   Los controles se explican por sí solos y raramente están en blanco (posiblemente con valores predeterminados para evitar controles en blanco).
-   Hay suficiente espacio horizontal para alojar las etiquetas.
-   Las etiquetas no varían significativamente en longitud.
-   Hay muchas columnas. Visualmente, las etiquetas y los controles aparecen como una sola columna.

Sin embargo, antes de adoptar cualquiera de estos estilos, tenga en cuenta dos factores más:

-   Prefiera un estilo que pueda usar de forma coherente en todo el programa.
-   Las etiquetas justificadas a la izquierda, ya sean los controles situados a la izquierda de los controles, son los estilos más comunes, por lo que se les debe dar preferencia.

### <a name="balance"></a>Saldo

Una ventana o página tiene un equilibrio cuando su contenido aparece distribuido uniformemente en su superficie. Si la superficie tenía físicamente la misma ponderación que tiene visualmente, un diseño equilibrado no debe tener en cuenta un lado.

El problema de equilibrio más común es tener demasiado contenido en el lado izquierdo de una ventana o página. Puede crear el saldo de las siguientes maneras:

-   Usar márgenes mayores en el lado izquierdo que el derecho.
-   Colocar los elementos de la interfaz de usuario utilizados para completar una tarea a la derecha.
-   Colocar los elementos de la interfaz de usuario utilizados en la tarea en el centro.
-   Aumentar el tamaño de los controles de múltiples líneas o de varios.
-   Usar la alineación del centro estratégicamente.

![captura de pantalla de la impresora a la izquierda y el texto a la derecha ](images/vis-layout-image37.png)

Este diseño de página del asistente equilibrado muestra un margen izquierdo mayor que el de la derecha para mejorar el saldo.

Si estas técnicas no alcanzan el equilibrio, considere la posibilidad de reducir el ancho de la ventana o la página para que coincida mejor con su contenido.

En el caso de las superficies de tamaño variable, no Centre el contenido solo para conseguir el equilibrio. En su lugar, mantenga un origen superior izquierdo fijo, defina un área expuesta máxima y equilibre el contenido dentro del espacio usado.

### <a name="grids"></a>Cuadrículas

Una cuadrícula es un sistema de alineación subyacente invisible. Las cuadrículas pueden ser simétricas, pero las cuadrículas asimétricas también funcionan bien. Cuando se usa en una sola ventana o página, las cuadrículas ayudan a organizar el contenido dentro de una superficie. Cuando se reutilizan, las cuadrículas crean un diseño coherente entre superficies.

El número de líneas de cuadrícula afecta a la percepción de complejidad visual. Un diseño con menos líneas de cuadrícula aparece más sencillo que un diseño con más líneas de cuadrícula.

**Visualmente complejo:**

![captura de pantalla del cuadro de diálogo abarrotado ](images/vis-layout-image38.png)

**Visualmente simple:**

![captura de pantalla del cuadro de diálogo organizado ](images/vis-layout-image39.png)

Las líneas de cuadrícula innecesarias crean complejidad visual.

Sabe que un diseño usa cuadrículas de forma eficaz cuando:

-   Las ventanas o páginas con contenido o función similares tienen un diseño similar.
-   Los elementos de diseño repetidos aparecen en ubicaciones similares en ventanas y páginas.
-   No hay líneas de cuadrícula de alineación horizontal y vertical no necesarias.

### <a name="visual-simplicity"></a>Simplicidad visual

La simplicidad visual es la percepción de que un diseño no es más complicado de lo que debe ser.

Sabe que un diseño tiene una simplicidad visual cuando:

-   Elimina las capas innecesarias de Chrome de ventana.
-   Presenta el contenido usando como máximo siete grupos fácilmente identificables.
-   Utiliza la agrupación ligera, como el diseño y los separadores en lugar de los cuadros de grupo.
-   Usa controles ligeros, como vínculos en lugar de botones de comando para comandos secundarios, y listas desplegables en lugar de listas para opciones.
-   Reduce el número de líneas de cuadrícula de alineación vertical y horizontal.
-   Reduce el número de tamaños de control, por ejemplo, usando solo uno o dos anchos de botón de comando en una superficie.
-   Usa la divulgación progresiva para ocultar los elementos de la interfaz de usuario hasta que se necesiten.
-   Usa espacio suficiente para que la ventana o la página no se sientan estorban.
-   Ajusta las ventanas y los controles de forma adecuada para eliminar el desplazamiento innecesario.
-   Usa una sola fuente con un número pequeño de tamaños y colores de texto.

Como norma general, si se puede eliminar un elemento de diseño sin dañar la eficacia de la interfaz de usuario, es probable que sea.

## <a name="guidelines"></a>Directrices

### <a name="screen-resolution-and-dpi"></a>Resolución de pantalla y PPP

-   **Admitir la resolución efectiva mínima de Windows de 800x600 píxeles.** En el caso de las ius críticas que deben funcionar en modo seguro, admiten una resolución efectiva de 640x480 píxeles. Asegúrese de tener en cuenta el espacio que usa la barra de tareas mediante la reserva de 48 [píxeles relativos](glossary.md) verticales para las ventanas que se muestran con la barra de tareas.
-   **Optimice los diseños de ventana de tamaño variable para una resolución efectiva de 1024x768 píxeles.** Cambiar automáticamente el tamaño de estas ventanas para resoluciones de pantalla inferiores de una forma que sigue siendo funcional.
-   **Asegúrese de probar las ventanas en 96 puntos por pulgada (PPP) (a 800x600 píxeles), 120 ppp (a 1024x768 píxeles) y 144 ppp (en 1200x900 píxeles).** Compruebe si hay problemas de diseño, como el recorte de controles, texto y ventanas, y ajuste de iconos y mapas de bits.
-   **En el caso de los programas con escenarios táctiles y de uso móvil, optimice para 120 ppp.** Actualmente, las pantallas con un alto nivel de PPP están predominantes en PC táctiles y móviles.

### <a name="window-size"></a>Tamaño de la ventana

-   **Elija un tamaño de ventana predeterminado adecuado para su contenido.** No dude en usar tamaños de ventana iniciales más grandes si puede utilizar el espacio con eficacia.
-   **Use una relación de aspecto de alto y ancho equilibrada.** Se prefiere una relación de aspecto entre 3:5 y 5:3, aunque se puede usar una relación de aspecto de 1:3 para los cuadros de diálogo de mensaje (como errores y advertencias).
-   **Use ventanas redimensionables siempre que sea práctico para evitar las barras de desplazamiento y los datos truncados.** Las ventanas con contenido dinámico, documentos, imágenes, listas y árboles aprovechan al máximo las ventanas redimensionables.
-   En el **caso de los documentos de texto, considere una longitud de línea máxima de 80 caracteres** para facilitar la lectura del texto. (Entre los caracteres se incluyen letras, signos de puntuación y espacios).
-   Ventanas de tamaño fijo:
    -   **Las ventanas de tamaño fijo deben ser totalmente visibles y ajustarse al área de trabajo.**
-   Ventanas redimensionables:
    -   **Las ventanas de tamaño variable pueden estar optimizadas para resoluciones más altas, pero se reduce el tamaño según sea necesario en el momento de la presentación en la resolución de pantalla real.**
    -   **Los tamaños de ventana progresivamente mayores deben mostrar progresivamente más información.** Asegúrese de que al menos una parte o un control de la ventana tenga contenido de tamaño variable.
    -   **Mantenga el origen superior izquierdo del contenido fijo cuando se cambie el tamaño de la ventana.** No mueva el origen para equilibrar el contenido a medida que cambia el tamaño de la ventana.
    -   **Establezca un tamaño máximo de contenido si el contenido puede estar demasiado ensanchado.** Si el contenido deja de ser manejable, no cambie el tamaño del área de contenido más allá del ancho máximo o cambie el origen del contenido a medida que el tamaño de la ventana sea mayor. En su lugar, conserve un ancho máximo y un origen fijo superior izquierdo.
    -   **Establezca un tamaño de ventana mínimo si hay un tamaño por debajo del cual ya no se puede usar el contenido.** En el caso de los controles de tamaño variable, establezca tamaños de elementos de tamaño mínimo ajustables en sus tamaños funcionales más pequeños, como el ancho mínimo de las columnas funcionales en las vistas de lista. Los elementos opcionales de la interfaz de usuario deben quitarse por completo.
    -   **Considere la posibilidad de modificar la presentación para que el contenido se pueda usar en tamaños menores.**

        ![captura de pantalla de los controles del reproductor de media ](images/vis-layout-image16.png)

        En este ejemplo, Windows Media Player cambia su formato cuando la ventana se vuelve demasiado pequeña para el formato estándar.

### <a name="control-size"></a>Tamaño del control

-   **Haga que todos los controles interactivos tengan al menos 16x16 píxeles relativos.** Esto funciona bien con todos los dispositivos de entrada, incluida la tecnología táctil y de Tablet PC de Windows.
-   **Controles de tamaño para evitar que se trunquen los datos.** No trunque los datos que deben leerse para realizar una tarea. Tamaño de las columnas de la vista de lista para evitar datos truncados.
-   **Controles de tamaño para eliminar el desplazamiento innecesario.** Haga que los controles sean ligeramente más grandes si al hacerlo se elimina una barra de desplazamiento. Debe haber algunas barras de desplazamiento verticales y ninguna barra de desplazamiento horizontal innecesaria.

    ![captura de pantalla de tamaño de la lista para evitar una barra de desplazamiento ](images/vis-layout-image40.png)

    En este ejemplo, se cambia el tamaño de la lista desplegable para eliminar la barra de desplazamiento.

-   **Reduzca el número de tamaños de control en una superficie.** Preferir el uso de los [tamaños de control recomendados estándar](#recommended-sizing-and-spacing) y, cuando sea necesario, usar unos controles de tamaño más grande o más grandes de forma coherente. Intente usar un solo ancho para cuadros de lista y vistas de árbol, y no más de tres anchos para los botones de comando y las listas desplegables. Sin embargo, los anchos de cuadro de texto y de cuadro combinado deben sugerir la longitud de la entrada más larga o esperada.

    ![captura de pantalla del cuadro de diálogo con listas y botones ](images/vis-layout-image41.png)

    En este ejemplo, se usa de forma coherente un cuadro de lista y un tamaño de botón de comando.

-   **En el caso de los controles cuyo tamaño se basa en el texto, incluya un 30 por ciento adicional (hasta el 200 por ciento para el texto más corto) de cualquier texto que se vaya a localizar.** Esta directriz supone que el diseño está diseñado con texto en inglés. Tenga en cuenta también que esta instrucción hace referencia a texto localizado, no a números.
-   **Extienda los controles de texto estático, las casillas y los botones de radio al ancho máximo que quepa en el diseño.** Al hacerlo, se evita el truncamiento del texto y la localización de longitud variable.

    **Incorrecto:**

    ![captura de pantalla del control de progreso y el texto parcial ](images/vis-layout-image42.png)

    En este ejemplo, el texto del control se trunca innecesariamente.

### <a name="control-spacing"></a>Espaciado de control

-   **Si los controles no están en contacto con, debe tener al menos 3 DLU (5 píxeles relativos) de espacio entre ellos.** De lo contrario, los usuarios pueden hacer clic en el espacio inactivo entre los controles. Puesto que al hacer clic en espacio inactivo no hay ningún resultado ni ningún comentario visual, a menudo los usuarios no están seguro de qué salió mal.

### <a name="placement"></a>Ubicación

-   **Organice los elementos de la interfaz de usuario de una superficie para que fluyan de forma natural en orden de izquierda a derecha y de arriba abajo (en referencias culturales occidentales).** La colocación de los elementos de la interfaz de usuario transmite su relación y debe reflejar los pasos para realizar la tarea.
-   **Coloque los elementos de la interfaz de usuario que inician una tarea en la esquina superior izquierda o en el centro superior.** Conceda al elemento de la interfaz de usuario que los usuarios deben buscar primero el mayor énfasis visual.
-   **Coloque los elementos de la interfaz de usuario que completen una tarea en la esquina inferior derecha.**
-   **Coloque los elementos de la interfaz de usuario relacionados juntos y separe los elementos no relacionados.**
-   **Coloque los pasos necesarios en el flujo principal.**
-   **Coloque los pasos opcionales fuera del flujo principal,** posiblemente desacentuado mediante el uso de un fondo adecuado o una divulgación progresiva.
-   **Coloque los elementos usados con frecuencia delante** de los elementos que se usan con poca frecuencia en la ruta de exploración.

### <a name="focus"></a>Foco

-   **Elija un único elemento de la interfaz de usuario que los usuarios tengan que examinar primero para que sea el punto focal.** El punto focal debe ser algo importante que los usuarios necesiten buscar y comprender rápidamente.
-   **Coloque el punto focal en la esquina superior izquierda o en el centro superior.**
-   **Dé al punto focal el mayor énfasis visual,** como texto destacado, selección predeterminada o foco de entrada inicial.

### <a name="alignment"></a>Alignment

-   Normalmente, use la alineación izquierda.
-   Use la alineación derecha para datos numéricos, especialmente columnas de datos numéricos.
-   Use la alineación derecha para los botones de confirmación, así como los controles alineados con el borde de la ventana derecha.
-   Use la alineación del centro cuando la alineación izquierda o derecha no sea adecuada o aparezca desequilibrada.
-   Al alinear verticalmente los controles con texto, alinee las líneas de base de texto para proporcionar un flujo de lectura horizontal suave.
-   Para la alineación de etiquetas, consulte la sección [alineación de etiquetas](#label-alignment) en conceptos de diseño.

### <a name="accessibility"></a>Accesibilidad

-   **No utilice el diseño como único medio para transmitir información importante sobre una interfaz de usuario.** Es posible que los usuarios que tienen discapacidades visuales no puedan interpretar esta presentación. Por ejemplo, asegúrese de que las etiquetas de controles comunican su relación con otros elementos.
-   **No inserte controles subordinados dentro de las etiquetas de control para crear una oración o frase.** Dichas asociaciones se basan exclusivamente en el diseño y no se controlan bien mediante la navegación del teclado o las tecnologías de accesibilidad. Además, esta técnica no es localizable porque la estructura de oraciones varía con el lenguaje.

    **Incorrecto:**

    ![captura de pantalla de un cuadro de texto en medio de una oración ](images/vis-layout-image43.png)

    En este ejemplo, el cuadro de texto se coloca incorrectamente dentro de la etiqueta de la casilla.

    **Correcto:**

    ![captura de pantalla de un cuadro de texto al final de una frase ](images/vis-layout-image44.png)

    Aquí, el cuadro de texto se coloca después de la etiqueta de la casilla.

-   **Haga que la agrupación sea accesible.** Los grupos definidos por los paneles de ventana, los cuadros de grupo, los separadores, las etiquetas de texto y los agregadores se controlan automáticamente mediante las ayudas de accesibilidad. Sin embargo, los grupos definidos solo por la colocación y el fondo no son y deben definirse mediante programación para la accesibilidad.

Para obtener más instrucciones, consulte [accesibilidad](inter-accessibility.md).

## <a name="recommended-sizing-and-spacing"></a>Ajuste de tamaño y espaciado recomendados

**Control de tamaño**

En la tabla siguiente se enumeran los tamaños recomendados (ancho x alto o alto si es un número único) para los elementos comunes de la interfaz de usuario (para 9 pt. Segoe UI a 96 PPP). Los anchos basados en el elemento más largo en inglés agregan el 30 por ciento para la localización (hasta el 200 por ciento para el texto más corto) de cualquier texto (pero no de los números) que se va a localizar.



|                                                                                                 |                            |                                                                                                   |                                                                                                            |
|-------------------------------------------------------------------------------------------------|----------------------------|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
|                                                                                                 | **Control**<br/>     | **Unidades de cuadro de diálogo**<br/>                                                                       | **Píxeles relativos**<br/>                                                                             |
| ![captura de pantalla de las casillas y sus etiquetas ](images/vis-layout-image45.png)<br/>       | Casillas<br/>     | 10<br/>                                                                                     | 17<br/>                                                                                              |
| ![captura de pantalla del cuadro combinado ](images/vis-layout-image46.png)<br/>                          | Cuadros combinados<br/>     | ancho del elemento más largo + 30% x 14<br/>                                                       | ancho del elemento más largo + 30% x 23<br/>                                                                |
| ![captura de pantalla de un botón de comando ](images/vis-layout-image47.png)<br/>                   | Botones de comando<br/> | 50 x 14<br/>                                                                                | 75 x 23<br/>                                                                                         |
| ![captura de pantalla de uno de los dos vínculos de comandos seleccionados ](images/vis-layout-image48.png)<br/>  | Vínculos de comandos<br/>   | 25 (una línea) o 35 (dos líneas)<br/>                                                        | 41 (una línea) o 58 (dos líneas)<br/>                                                                 |
| ![captura de pantalla de una lista desplegable ](images/vis-layout-image49.png)<br/>                   | Listas desplegables<br/> | ancho de datos válidos más largos + 30% x 14<br/>                                                 | ancho del elemento más largo + 30% x 23<br/>                                                                |
| ![captura de pantalla de un cuadro de lista ](images/vis-layout-image50.png)<br/>                         | Cuadros de lista<br/>      | ancho del elemento más largo + 30% x un número entero de elementos (3 elementos como mínimo)<br/>            |                                                                                                            |
| ![captura de pantalla de una lista de archivos de imagen ](images/vis-layout-image51.png)<br/>            | Vistas de lista<br/>      | ancho de las columnas que evitan que los datos se trunquen x un número entero de elementos<br/>                 |                                                                                                            |
| ![captura de pantalla de una barra de progreso ](images/vis-layout-image52.png)<br/>                     | Barras de progreso<br/>   | 107 o 237 x 8<br/>                                                                         | 160 o 355 x 15<br/>                                                                                 |
| ![captura de pantalla de botones de radio ](images/vis-layout-image53.png)<br/>                      | Botones de radio<br/>   | 10<br/>                                                                                     | 17<br/>                                                                                              |
| ![captura de pantalla del control deslizante ](images/vis-layout-image54.png)<br/>                     | Controles deslizantes<br/>         | 15<br/>                                                                                     | 24<br/>                                                                                              |
| ![captura de pantalla del texto: ' seleccionar zona horaria ' ](images/vis-layout-image55.png)<br/>           | Texto (estático)<br/>   | 8<br/>                                                                                      | 13<br/>                                                                                              |
| ![captura de pantalla de un cuadro de texto vacío ](images/vis-layout-image56.png)<br/>                     | Cuadros de texto<br/>      | ancho de entrada más larga o esperada + 30% x 14 (una línea) + 10 para cada línea adicional<br/> | ancho de datos válidos más largos + 30% x 23 píxeles relativos (una línea) + 16 para cada línea adicional<br/> |
| ![captura de pantalla de carpetas anidadas en el explorador de Windows ](images/vis-layout-image57.png)<br/> | Vistas de árbol<br/>      | ancho del elemento más largo + 30% x un número entero de elementos (5 elementos como mínimo)<br/>            |                                                                                                            |



 

**Espaciado**

En la tabla siguiente se muestra el espaciado recomendado entre los elementos de la interfaz de usuario comunes (para 9 pt. Segoe UI a 96 PPP).



|                                                                                                   |                                                                                                       |                                                                                           |                                                                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
|                                                                                                   | **Element**<br/>                                                                                | **Unidades de cuadro de diálogo**<br/>                                                               | **Píxeles relativos**<br/>                                                            |
| ![Imagen que muestra el espaciado en los márgenes del cuadro de diálogo ](images/vis_layout_image58.jpeg)<br/>        | Márgenes del cuadro de diálogo<br/>                                                                         | 7 en todos los lados<br/>                                                                 | 11 en todos los lados<br/>                                                                |
| ![Imagen que muestra el espaciado entre etiquetas y controles ](images/vis_layout_image59.jpeg)<br/>  | Entre las etiquetas de texto y sus controles asociados (por ejemplo, cuadros de texto y cuadros de lista)<br/> | 3<br/>                                                                              | 5<br/>                                                                              |
| ![Imagen que muestra el espaciado entre los controles relacionados ](images/vis_layout_image60.jpeg)<br/>     | Entre controles relacionados<br/>                                                                   | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Imagen que muestra el espaciado entre controles no relacionados ](images/vis_layout_image61.jpeg)<br/>   | Entre controles no relacionados<br/>                                                                 | 7<br/>                                                                              | 11<br/>                                                                             |
| ![Imagen que muestra el espaciado del primer control en un grupo ](images/vis_layout_image62.jpeg)<br/>  | Primer control en un cuadro de grupo<br/>                                                               | 11 abajo desde la parte superior del cuadro de grupo; alinear verticalmente con el título del cuadro de grupo<br/> | 16 hacia abajo desde la parte superior del cuadro de grupo. alinear verticalmente con el título del cuadro de grupo<br/> |
| ![Aa511279. between-Related (en-US, MSDN. 10). jpg](images/vis_layout_image60.jpeg)<br/>         | Entre los controles de un cuadro de grupo<br/>                                                            | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Imagen que muestra el espaciado entre los botones ](images/vis_layout_image63.jpeg)<br/>              | Entre los botones organizados horizontal o verticalmente<br/>                                        | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Imagen que muestra el espaciado del último control en un grupo ](images/vis_layout_image64.jpeg)<br/>   | Último control en un cuadro de grupo<br/>                                                                | 7 por encima de la parte inferior del cuadro de grupo<br/>                                            | 11 por encima de la parte inferior del cuadro de grupo<br/>                                           |
| ![Imagen que muestra el espaciado desde el borde izquierdo del cuadro de grupo ](images/vis_layout_image65.jpeg)<br/>  | Desde el borde izquierdo de un cuadro de grupo<br/>                                                          | 6<br/>                                                                              | 9<br/>                                                                              |
| ![Imagen que muestra el espaciado de la etiqueta de texto junto al control ](images/vis_layout_image66.jpeg)<br/> | Etiqueta de texto junto a un control<br/>                                                                | 3 hacia abajo desde la parte superior del control<br/>                                             | 5 abajo desde la parte superior del control<br/>                                             |
| ![Imagen que muestra el espaciado entre párrafos de texto ](images/vis_layout_image67.jpeg)<br/>   | Entre párrafos de texto<br/>                                                                 | 7<br/>                                                                              | 11<br/>                                                                             |
|                                                                                                   | Espacio más pequeño entre los controles interactivos<br/>                                                | 3 o ningún espacio<br/>                                                                  | 5 o ningún espacio<br/>                                                                  |
|                                                                                                   | Menor espacio entre un control no interactivo y cualquier otro control<br/>                     | 2<br/>                                                                              | 3<br/>                                                                              |



 

 

