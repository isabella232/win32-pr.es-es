---
title: Vistas de árbol
description: Con una vista de árbol, los usuarios pueden ver e interactuar con una colección de objetos organizada jerárquicamente, mediante una selección única o una selección múltiple.
ms.assetid: f0206485-e028-41d8-9be2-5d59f0a0b677
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c5cb2b6d48a30cba6de2136659231d9d37361621
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104560387"
---
# <a name="tree-views"></a>Vistas de árbol

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Con una vista de árbol, los usuarios pueden ver e interactuar con una colección de objetos organizada jerárquicamente, mediante una selección única o una selección múltiple.

En un árbol, los objetos que contienen datos se denominan nodos hoja y los objetos que contienen otros objetos se denominan nodos contenedores. Un solo nodo contenedor de nivel superior se denomina nodo raíz. Los usuarios pueden expandir y contraer los nodos de contenedor haciendo clic en los botones de expansión más y menos.

![captura de pantalla de la vista de árbol del explorador de Windows ](images/ctrl-tree-views-image1.png)

Vista de árbol típica.

> [!Note]  
> Las instrucciones relacionadas con el [diseño](vis-layout.md) y los [menús](cmd-menus.md) se presentan en artículos independientes.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

**Tener datos jerárquicos no significa que deba usar una vista de árbol.** Con mucha frecuencia, una [vista de lista](ctrl-list-views.md) es una opción más sencilla y aún más eficaz. Vistas de lista:

-   Admitir varias vistas diferentes.
-   Permite ordenar los datos por cualquiera de las columnas en la vista de detalles.
-   Permite organizar los datos en grupos, formando una jerarquía de dos niveles.

**Para usar una vista de lista, puede simplificar la información jerárquica mediante las técnicas siguientes:**

-   Quite el nodo raíz, si está presente, porque a menudo no es necesario.
-   Use grupos de vistas de lista, pestañas, [listas desplegables](/windows/desktop/uxguide/ctrl-drop)o [encabezados expansibles](glossary.md) para reemplazar los contenedores de nivel superior.

    ![captura de pantalla de grupos de vistas de lista que contienen listas ](images/ctrl-tree-views-image2.png)

    En este ejemplo, los grupos de vistas de lista se utilizan para los contenedores de nivel superior.

    ![captura de pantalla de pestañas usadas para contenedores de nivel superior ](images/ctrl-tree-views-image3.png)

    En este ejemplo, se usan pestañas para los contenedores de nivel superior.

    ![captura de pantalla de la lista desplegable usada como contenedor ](images/ctrl-tree-views-image4.png)

    En este ejemplo, se usa una lista desplegable para los contenedores de nivel superior.

-   Si un control asociado muestra el contenido del contenedor seleccionado, ese control puede mostrar los niveles inferiores de la jerarquía.

    ![captura de pantalla del panel de tabla de contenido ](images/ctrl-tree-views-image5.png)

    En este ejemplo, los contenedores de bajo nivel se muestran en la ventana de documento.

**Debe utilizar una vista de árbol si necesita mostrar una jerarquía de más de dos niveles (sin incluir el nodo raíz).**

Para decidir si una vista de árbol es el control derecho, tenga en cuenta estas preguntas:

-   **¿Los datos son jerárquicos?** Si no es así, usa otro control.
-   **¿La jerarquía tiene al menos tres niveles (sin incluir la raíz)?** Si no es así, considere alternativas como grupos de vistas de lista, pestañas, listas desplegables o encabezados expansibles.
-   **¿Los elementos tienen datos auxiliares?** Si es así, considere la posibilidad de usar una vista de lista en el modo de vista de detalles para sacar el máximo partido de los datos auxiliares.
-   **¿Los datos de nivel inferior están relacionados con subtareas independientes?** Si es así, considere la posibilidad de mostrar la información en un control asociado o en una ventana independiente (que se muestra con [botones de comando](ctrl-command-buttons.md) o [vínculos](ctrl-command-links.md)).
-   **¿Están los usuarios de destino avanzados?** Los usuarios avanzados son más expertos en el uso de árboles. Si su aplicación está dirigida a usuarios inexpertos, evite el uso de vistas de árbol.
-   **¿Los elementos tienen una categorización jerárquica única y natural que está familiarizada con la mayoría de los usuarios?** Si es así, los datos son ideales para una vista de árbol. Si necesita varias vistas u ordenación, use una vista de lista en su lugar.
-   **¿Los usuarios tienen que ver los datos de nivel inferior en algunos escenarios, pero no en todos, pero no en todo el tiempo?** Si es así, los datos son ideales para una vista de árbol.

> [!Note]  
> A veces, un control que se parece a una vista de árbol se implementa mediante una vista de lista. En tales casos, aplique las directrices basadas en el uso, no en la implementación.

 

## <a name="design-concepts"></a>Conceptos de diseño

Los árboles están diseñados para organizar los datos y facilitar su búsqueda, pero es difícil facilitar la detección de los datos dentro de un árbol. Tenga en cuenta los siguientes principios a la hora de decidir sobre las vistas de árbol y su organización.

### <a name="predictability-and-discoverability"></a>Previsibilidad y detectabilidad

**Una vista de árbol se basa en las relaciones entre los objetos.** Los árboles funcionan mejor cuando los objetos forman una relación clara, conocida y mutuamente excluyente en la que cada objeto se asigna a un único contenedor fácil de determinar.

**Un problema importante es que un objeto puede aparecer en nodos diferentes.** Por ejemplo, ¿por qué los usuarios esperan encontrar un dispositivo de hardware que reproduce música, tiene un disco duro grande y usa un puerto USB? Quizás en cualquiera de los distintos nodos de contenedor, como multimedia, almacenamiento, USB y posiblemente en recursos de hardware. Una solución consiste en colocar cada objeto en el contenedor más adecuado, con independencia de las circunstancias. otro enfoque consiste en colocar cada objeto en todos los contenedores que se aplican. La primera promueve una jerarquía sencilla y limpia y la última promueve la detectabilidad cada una de ellas tiene ventajas y posibles problemas.

**Es posible que los usuarios no sepan completamente el diseño del árbol, pero formarán un modelo mental de las relaciones después de interactuar con el árbol durante un tiempo.** Si ese modelo mental es incorrecto, lleva a confusión. Por ejemplo, supongamos que se puede encontrar un reproductor de música en los contenedores multimedia, almacenamiento y USB. Esta disposición mejora la detectabilidad. Si un usuario encuentra por primera vez el dispositivo en el contenido multimedia, el usuario puede concluir que todos los dispositivos, como los reproductores de música, aparecen en el contenedor de multimedia. A continuación, el usuario esperará que los dispositivos similares, como las cámaras digitales, aparezcan en el contenedor multimedia y se confundirán si no es así.

**El reto al diseñar un árbol es equilibrar la capacidad de detección con un modelo de usuario predecible que minimiza la confusión.**

### <a name="breadth-vs-depth"></a>Amplitud frente a profundidad

Los estudios de facilidad de uso han demostrado que **los usuarios tienen más éxito en la búsqueda de objetos en un árbol que es muy amplio que en un árbol de profundidad**, por lo que al diseñar un árbol debe preferir la amplitud de profundidad. Idealmente, un árbol no debe tener más de cuatro niveles (sin contar el nodo raíz) y los objetos a los que se accede con más frecuencia deben aparecer en los dos primeros niveles.

### <a name="other-principles"></a>Otros principios

-   Cuando los usuarios encuentran lo que buscan, dejan de buscar. No buscan ver dónde se puede encontrar un objeto porque no es necesario. Esos usuarios pueden suponer que la primera ruta de acceso que encuentre es la única ruta de acceso.
-   Los usuarios tienen problemas para buscar objetos en árboles grandes y complejos. Los usuarios no realizarán una búsqueda exhaustiva y manual para buscar objetos en dichos árboles. se detienen una vez que piensan que han gastado un esfuerzo razonable. Por consiguiente, los árboles grandes y complejos deben complementarse con otros métodos de acceso, como búsqueda de palabras, un índice o filtrado.
-   Algunos programas permiten a los usuarios crear sus propios árboles. Aunque estos árboles autodiseñados podrían estar alineados con el modelo mental de un usuario, a menudo se crean de forma aleatoria y deficiente. Por ejemplo, mientras que el sistema de archivos, el programa de correo electrónico y la lista de favoritos almacenan normalmente tipos de información similares, los usuarios raramente molestan a organizarlos de la misma manera.

**Si solo hace algo...**

Valore detenidamente las ventajas y desventajas del uso de las vistas de árbol. Tener datos organizados jerárquicamente no significa que deba usar una vista de árbol.

## <a name="usage-patterns"></a>Patrones de uso

Las vistas de árbol tienen varios patrones de uso:



|                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Vistas de árbol con solo nodos contenedores**<br/> los usuarios pueden ver e interactuar con un contenedor a la vez. <br/>                        | Normalmente, estas vistas de árbol tienen un control asociado que muestra el contenido del contenedor seleccionado, de modo que los usuarios pueden interactuar con un solo contenedor cada vez. <br/> ![captura de pantalla de panel contenedor y panel de contenido ](images/ctrl-tree-views-image6.png)<br/> En este ejemplo, la vista de árbol solo tiene nodos contenedores. El contenido del nodo seleccionado se muestra en el control de vista de lista asociado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Vistas de árbol con nodos contenedor y hoja**<br/> los usuarios pueden ver e interactuar con contenedores y hojas.<br/>                       | Normalmente, estas vistas de árbol tienen un control asociado que muestra el contenido del contenedor o la hoja seleccionados. permitir a los usuarios interactuar con hojas a menudo hace que sea necesario admitir la selección múltiple. <br/> ![captura de pantalla del panel de vista de árbol y del panel de contenido ](images/ctrl-tree-views-image7.png)<br/> en este ejemplo, la vista de árbol tiene nodos de contenedor y de hoja. Dado que se admite la selección múltiple, el contenido de los elementos abiertos se muestra mediante [pestañas](ctrl-tabs.md) en el control asociado.<br/> como alternativa, la vista de árbol puede tener una lista organizada, donde los contenedores son encabezados y las hojas son opciones. <br/> ![captura de pantalla de la vista de árbol con encabezados y opciones ](images/ctrl-tree-views-image8.png)<br/> En este ejemplo, las hojas de árbol son opciones y los contenedores son categorías de opciones.<br/> |
| **Vistas de árbol de casilla**<br/> los usuarios pueden seleccionar cualquier número de elementos, incluido ninguno.<br/>                                             | Las casillas indican claramente que es posible la selección múltiple. Use este patrón de árbol cuando la selección múltiple sea esencial o se use habitualmente. <br/> ![captura de pantalla de la vista de árbol con casillas ](images/ctrl-tree-views-image9.png)<br/> En este ejemplo, una vista de árbol de casilla permite seleccionar o desactivar las características.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Generadores de vistas de árbol**<br/> los usuarios pueden crear un árbol agregando un contenedor o una hoja a la vez y estableciendo opcionalmente el orden.<br/> | Los usuarios pueden crear o modificar muchos árboles. algunos árboles están integrados en su lugar mediante menús contextuales y arrastrar y colocar (como las carpetas del explorador de Windows), mientras que otros árboles se crean mediante un cuadro de diálogo especializado (como la lista Favoritos en Windows Internet Explorer). <br/> ![captura de pantalla del cuadro de diálogo favoritos ](images/ctrl-tree-views-image10.png)<br/> En este ejemplo de Internet Explorer, los usuarios pueden crear su propia lista de favoritos mediante un cuadro de diálogo.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| **Vistas de árbol con métodos de acceso alternativos**<br/> los usuarios pueden buscar objetos de maneras distintas de usar un árbol jerárquico.<br/>        | Como se mencionó anteriormente, los usuarios tienen problemas para encontrar objetos en árboles grandes y complejos, por lo que estos árboles deben complementarse con otros métodos de acceso, como una búsqueda de palabras, un índice o un filtrado. <br/> ![captura de pantalla de las pestañas contenido, índice y favoritos ](images/ctrl-tree-views-image11.png)<br/> en este ejemplo, los usuarios también pueden tener acceso a la información mediante una tabla de contenido, un índice y favoritos. para algunos usuarios, las pestañas índice y buscar pueden ser más útiles que la pestaña contenido.<br/> ![captura de pantalla del menú Inicio y el cuadro de búsqueda de Windows ](images/ctrl-tree-views-image12.png)<br/> En este ejemplo, el menú Inicio de Windows también permite a los usuarios obtener acceso a programas, archivos y páginas web escribiendo parte del nombre en el cuadro de búsqueda.<br/>                                                                                                             |



 

## <a name="guidelines"></a>Directrices

### <a name="presentation"></a>Presentación

-   **Dentro de un contenedor, ordene los elementos en un orden lógico.** Ordenar nombres en orden alfabético, números en orden numérico y fechas en orden cronológico.
-   **Use el atributo Mostrar selección siempre** para que los usuarios puedan determinar fácilmente el elemento seleccionado, incluso cuando el control no tenga el foco de entrada.
-   **Si el árbol actúa como tabla de contenido, use el atributo de expansión único para simplificar la administración del árbol.** De este modo, solo se expande la parte relevante del árbol.
-   **Evite presentar árboles vacíos.** Si un usuario crea un árbol, inicialice el árbol con instrucciones o elementos de ejemplo que los usuarios puedan necesitar.

    ![captura de pantalla de la lista de favoritos de Internet Explorer ](images/ctrl-tree-views-image13.png)

    En este ejemplo, la lista se presenta inicialmente con ejemplos.

-   **No haga que los nodos de contenedor se contraigan si los usuarios no tienen ninguna razón para contraerlos.** Al hacerlo, se agrega una complejidad innecesaria.
-   **Si el rendimiento de la carga es un problema, mostrar solo los contenedores de primer y segundo nivel del árbol de forma predeterminada.** Después, puede cargar datos adicionales a petición cuando un usuario expande las bifurcaciones en el árbol.
-   **Si los usuarios expanden o contraen un contenedor, se conservan para que surtan efecto la próxima vez que se muestre la vista de árbol**, a menos que sea probable que los usuarios prefieran comenzar en el estado predeterminado. La persistencia debe realizarse en una vista por árbol y por usuario.
-   **Si los contenedores de alto nivel tienen contenido similar, considere la posibilidad de usar pistas visuales para diferenciarlos.**

    **Incorrecto:**

    ![captura de pantalla de los elementos de Outlook con iconos diferentes ](images/ctrl-tree-views-image14.png)

    En este ejemplo, las carpetas buzón y archivo tienen contenido similar. Una vez que los árboles se expanden más, es muy difícil que los usuarios sepan dónde se encuentran en el árbol, lo que conduce a confusión. El uso de iconos ligeramente diferentes en las distintas secciones solucionará este problema.

-   **Reconsidere las líneas de conexión.** Aunque estas líneas muestran claramente las relaciones entre el contenedor y los nodos de hoja, agregan un desorden visual sin necesidad de facilitar la comprensión. En concreto, no sirven de ayuda cuando los nodos están cercanos, ni ayudan cuando los nodos están tan lejos de que es necesario el desplazamiento.

    **Correcto:**

    ![captura de pantalla de la vista de árbol con líneas de conexión ](images/ctrl-tree-views-image15.png)

    **Manera**

    ![captura de pantalla de la vista de árbol sin líneas de conexión ](images/ctrl-tree-views-image16.png)

    Las líneas de conexión hacen poco para ayudar a la comprensión.

### <a name="interaction"></a>Interacción

-   **Considere la posibilidad de proporcionar un comportamiento de doble clic.** Hacer doble clic debe tener el mismo efecto que seleccionar un elemento y ejecutar el comando predeterminado.
-   **Haga que el comportamiento de doble clic sea redundante.** Siempre debe haber un botón de comando o un comando de menú contextual que tenga el mismo efecto.
-   Si un elemento requiere una explicación más detallada, **proporcione la explicación en una sugerencia**.

    ![captura de pantalla de los favoritos con recuadro informativo de un elemento ](images/ctrl-tree-views-image17.png)

    En este ejemplo, un recuadro informativo proporciona más información.

-   **Proporcionar menús contextuales de comandos relevantes.** Estos comandos incluyen cortar, copiar, pegar, quitar o eliminar, cambiar nombre y propiedades.
-   **Al deshabilitar una vista de árbol, deshabilite también las etiquetas y los botones de comando asociados.**

### <a name="tree-organization"></a>Organización en árbol

-   **Use una estructura jerárquica natural que resulte familiar para la mayoría de los usuarios.**
-   **Si no puede usar este tipo de estructura, intente equilibrar la detección con un modelo de usuario predecible que minimice la confusión.**
-   **Para mejorar la capacidad de detección de forma segura, coloque un elemento en varios contenedores cuando:**
    -   El elemento no está relacionado con ningún otro elemento similar (por lo que los usuarios no están confundidos por asociaciones incorrectas).
    -   Solo hay algunos de estos elementos ubicados de forma redundante (por lo que el árbol no se llena).
-   **Use la estructura jerárquica más sencilla que funcione bien.** Para ello:
    -   Coloque los objetos a los que se accede con más frecuencia en los dos primeros niveles del árbol (sin contar el nodo raíz) y coloque los objetos de acceso menos frecuente más abajo en la jerarquía.
    -   Elimine los contenedores de nivel intermedio redundantes innecesarios o combinados.
-   **Prefiera amplitudr en profundidad.** Idealmente, un árbol no debe tener más de cuatro niveles y los objetos a los que se accede con más frecuencia deben aparecer en los primeros dos niveles.
-   **Determine si realmente necesita un nodo raíz.** Proporcione un nodo raíz si los usuarios necesitan la capacidad de ejecutar comandos en todo el árbol (posiblemente mediante un menú contextual en el nodo raíz). De lo contrario, el árbol es más sencillo y fácil de usar sin él.
-   **Si el árbol tiene métodos de acceso alternativos, como una búsqueda de palabras o un índice, optimice el árbol para la exploración centrándose en el contenido más útil.** Con métodos de acceso alternativos, el contenido del árbol no tiene que ser completo. La simplificación del árbol facilita a los usuarios la búsqueda del contenido más útil.

### <a name="check-box-tree-views"></a>Vistas de árbol de casilla

-   **Muestra el número de elementos seleccionados debajo de la lista**, especialmente si es probable que los usuarios seleccionen varios elementos. Esta información ayuda a los usuarios a confirmar que la selección es correcta.

    ![captura de pantalla de número de elementos seleccionados ](images/ctrl-tree-views-image18.png)

    En este ejemplo, se muestra el número de elementos seleccionados debajo del árbol. Está claro que no se seleccionan dos elementos.

-   Si hay muchos elementos posibles y seleccionando o borrando todos ellos, es probable que se agreguen los botones de comando Seleccionar todo y borrar todo.
-   **Use las casillas de verificación de estado mixto para indicar la selección parcial de los elementos de un contenedor.**

    **Correcto:**

    ![captura de pantalla de la ventana con casillas de estado mixto ](images/ctrl-tree-views-image19.png)

    En este ejemplo, las casillas de estado mixto se utilizan para indicar la selección parcial.

## <a name="recommended-sizing-and-spacing"></a>Ajuste de tamaño y espaciado recomendados

![captura de pantalla de tamaño y espaciado de la vista de árbol ](images/ctrl-tree-views-image20.png)

Ajuste de tamaño y espaciado recomendados para los controles de vista de árbol.

-   **Elija un ancho de la vista de árbol que evite la necesidad de desplazarse horizontalmente** por la mayoría de los elementos cuando el árbol esté totalmente expandido.
-   **Incluya un 30 por ciento adicional para dar cabida a la localización.**
-   **Elija un alto de la vista de árbol que elimine el desplazamiento vertical innecesario.** Considere la posibilidad de crear una vista de árbol ligeramente más larga (o incluso más si hay espacio disponible) si esto reduce la necesidad de una barra de desplazamiento vertical.

    **Incorrecto:**

    ![captura de pantalla del control de vista de árbol corto y estrecho ](images/ctrl-tree-views-image21.png)

    En este ejemplo, la vista de árbol se convierte en ligeramente más ancha y más tiempo en eliminar las barras de desplazamiento en la mayoría de los casos. En este árbol concreto, solo se puede abrir un contenedor a la vez.

-   **Si los usuarios se benefician de aumentar la vista de árbol, haga que la vista de árbol y su ventana primaria sean ajustables.** Esto permite a los usuarios ajustar el tamaño de la vista de árbol según sea necesario.

## <a name="labels"></a>Etiquetas

### <a name="control-labels"></a>Etiquetas de control

-   Todas las vistas de árbol necesitan etiquetas. Escriba la etiqueta como una palabra o frase, no como una frase, terminando con dos puntos y usando [texto estático](glossary.md).
-   Asigne una clave de acceso única. Para obtener instrucciones sobre las asignaciones, consulte [teclado](inter-keyboard.md).
-   Use mayúsculas de estilo de frase.
-   Coloque la etiqueta encima del control y alinee la etiqueta con el borde izquierdo del control.
-   En el caso de las vistas de árbol de selección múltiple, escriba la etiqueta para que quede claro que es posible realizar varias selecciones. Las etiquetas de la vista de árbol de casilla pueden ser menos explícitas.

    **Incorrecto:**

    ![captura de pantalla de la vista de árbol con la etiqueta de componentes ](images/ctrl-tree-views-image22.png)

    En este ejemplo, la etiqueta no proporciona información sobre la selección múltiple.

    **Manera**

    ![captura de pantalla de la vista de árbol con la etiqueta ' uno o más ' ](images/ctrl-tree-views-image23.png)

    En este ejemplo, la etiqueta indica claramente que es posible la selección múltiple.

    **Rendimiento**

    ![captura de pantalla de la vista de árbol con casillas ](images/ctrl-tree-views-image24.png)

    En este ejemplo, las casillas de verificación indican claramente que la selección múltiple es posible, por lo que la etiqueta no tiene que ser explícita.

### <a name="data-text"></a>Texto de datos

-   Use mayúsculas de estilo de frase.

### <a name="instructional-text"></a>Texto informativo

-   Si necesita agregar texto informativo sobre una vista de árbol, agréguelo encima de la etiqueta. Use frases completas con una puntuación final.
-   Use mayúsculas de estilo de frase.
-   Las explicaciones complementarias que son útiles pero no necesarias deben mantenerse breves. Coloque esta información entre paréntesis entre la etiqueta y el signo de dos puntos, después de la instrucción principal si se usa en lugar de una etiqueta, o debajo del control.

    ![captura de pantalla de la explicación debajo de la vista de árbol ](images/ctrl-tree-views-image8.png)

    En este ejemplo, la explicación complementaria está debajo del control.

## <a name="documentation"></a>Documentación

Al hacer referencia a las vistas de árbol:

-   Use el texto de etiqueta exacto, incluido el uso de mayúsculas, pero no incluya el carácter de subrayado de la tecla de acceso o el signo de dos puntos. Incluya la lista de palabras o la lista jerárquica si el contexto requiere que se realice una distinción de las listas normales.
-   En el caso de los elementos de árbol, use el texto exacto del elemento, incluido el uso de mayúsculas.
-   Consulte las vistas de árbol como vistas de árbol solo en programación y otra documentación técnica. En cualquier otro lugar, use List o Hierarchical List porque el término árbol es confuso para la mayoría de los usuarios.
-   Para describir la interacción del usuario, use seleccionar para los datos y expanda y contraiga los botones más y menos.
-   Siempre que sea posible, dé formato a la etiqueta y a los elementos de árbol usando texto en negrita. De lo contrario, coloque la etiqueta y los elementos entre comillas solo si es necesario para evitar confusiones.

Ejemplo: en la lista **contenido** , seleccione **diseño** de la interfaz de usuario.

Al hacer referencia a las casillas de una vista de árbol:

-   Use el texto exacto de la etiqueta, incluido el uso de mayúsculas, e incluya la casilla palabras. No incluya el carácter de subrayado de la tecla de acceso.
-   Para describir la interacción del usuario, use SELECT y Clear.
-   Siempre que sea posible, dé formato a la etiqueta usando texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.

Ejemplo: en la lista **elementos para realizar una copia de seguridad** , active la casilla **Mis documentos** .

