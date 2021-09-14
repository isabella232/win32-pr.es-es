---
title: Vistas de árbol
description: Con una vista de árbol, los usuarios pueden ver e interactuar con una colección de objetos organizada jerárquicamente, mediante una selección única o una selección múltiple.
ms.assetid: f0206485-e028-41d8-9be2-5d59f0a0b677
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ade51b421350dc90bf72e2ff1a683bf1d352f7c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267439"
---
# <a name="tree-views"></a>Vistas de árbol

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Con una vista de árbol, los usuarios pueden ver e interactuar con una colección de objetos organizada jerárquicamente, mediante una selección única o una selección múltiple.

En un árbol, los objetos que contienen datos se denominan nodos hoja y los objetos que contienen otros objetos se denominan nodos de contenedor. Un único nodo contenedor de nivel superior se denomina nodo raíz. Los usuarios pueden expandir y contraer nodos de contenedor haciendo clic en los botones de expander más y menos.

![captura de pantalla de la vista de árbol del Explorador de Windows ](images/ctrl-tree-views-image1.png)

Una vista de árbol típica.

> [!Note]  
> Las directrices relacionadas [con el](vis-layout.md) [diseño y los menús](cmd-menus.md) se presentan en artículos independientes.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

**Tener datos jerárquicos no significa que deba usar una vista de árbol.** A menudo, [una vista de lista](ctrl-list-views.md) es una opción más sencilla, pero más eficaz. Vistas de lista:

-   Admite varias vistas diferentes.
-   Admite la ordenación de datos por cualquiera de las columnas de la vista Detalles.
-   Admite la organización de datos en grupos, formando una jerarquía de dos niveles.

**Para usar una vista de lista, puede aplanar la información jerárquica mediante las técnicas siguientes:**

-   Quite el nodo raíz si está presente, ya que a menudo no es necesario.
-   Use grupos de vistas de lista, pestañas, [listas](/windows/desktop/uxguide/ctrl-drop)desplegables o [encabezados expandibles](glossary.md) para reemplazar los contenedores de nivel superior.

    ![captura de pantalla de los grupos de vista de lista que contienen listas ](images/ctrl-tree-views-image2.png)

    En este ejemplo, se usan grupos de vistas de lista para los contenedores de nivel superior.

    ![captura de pantalla de pestañas usadas para contenedores de nivel superior ](images/ctrl-tree-views-image3.png)

    En este ejemplo, se usan pestañas para los contenedores de nivel superior.

    ![captura de pantalla de la lista desplegable que se usa como contenedor ](images/ctrl-tree-views-image4.png)

    En este ejemplo, se usa una lista desplegable para los contenedores de nivel superior.

-   Si un control asociado muestra el contenido del contenedor seleccionado, ese control puede mostrar niveles inferiores de la jerarquía.

    ![captura de pantalla del panel de la tabla de contenido ](images/ctrl-tree-views-image5.png)

    En este ejemplo, los contenedores de bajo nivel se muestran en la ventana del documento.

**Debe usar una vista de árbol si necesita mostrar una jerarquía de más de dos niveles (sin incluir el nodo raíz).**

Para decidir si una vista de árbol es el control correcto, tenga en cuenta estas preguntas:

-   **¿Los datos son jerárquicos?** Si no es así, usa otro control.
-   **¿La jerarquía tiene al menos tres niveles (sin incluir la raíz)?** Si no es así, considere alternativas como grupos de vistas de lista, pestañas, listas desplegables o encabezados expandibles.
-   **¿Los elementos tienen datos auxiliares?** Si es así, considere la posibilidad de usar una vista de lista en el modo de vista Detalles para aprovechar al máximo los datos auxiliares.
-   **¿Los datos de nivel inferior se relacionan con subtareas independientes?** Si es así, considere la posibilidad de mostrar la información en un control asociado o en una ventana independiente (que se muestra mediante botones [de comando](ctrl-command-buttons.md) o [vínculos](ctrl-command-links.md)).
-   **¿Están avanzados los usuarios de destino?** Los usuarios avanzados son más expertos en el uso de árboles. Si la aplicación está dirigida a usuarios principiantes, evite el uso de vistas de árbol.
-   **¿Los elementos tienen una categorización única, natural y jerárquica que es familiar para la mayoría de los usuarios?** Si es así, los datos son ideales para una vista de árbol. Si necesita varias vistas o ordenación, use una vista de lista en su lugar.
-   **¿Necesitan los usuarios ver los datos de nivel inferior en algunos escenarios, pero no en todos, o en algunos, pero no todo el tiempo?** Si es así, los datos son ideales para una vista de árbol.

> [!Note]  
> A veces, un control que parece una vista de árbol se implementa mediante una vista de lista. En tales casos, aplique las directrices en función del uso, no de la implementación.

 

## <a name="design-concepts"></a>Conceptos de diseño

Los árboles están diseñados para organizar los datos y facilitar la tarea de encontrarlos, pero es difícil que los datos de un árbol se puedan detectar fácilmente. Tenga en cuenta los siguientes principios al decidir sobre las vistas de árbol y su organización.

### <a name="predictability-and-discoverability"></a>Predictability and discoverability

**Una vista de árbol se basa en las relaciones entre objetos.** Los árboles funcionan mejor cuando los objetos forman una relación clara, conocida y mutuamente excluyente en la que cada objeto se asigna a un contenedor único y fácil de determinar.

**Un problema importante es que un objeto puede aparecer en nodos diferentes.** Por ejemplo, ¿dónde esperarían los usuarios encontrar un dispositivo de hardware que reproduce música, tiene un disco duro grande y usa un puerto USB? Quizás en cualquiera de varios nodos de contenedor diferentes, como Multimedia, Storage, USB y posiblemente en recursos de hardware. Una solución es colocar cada objeto en el contenedor más adecuado independientemente de las circunstancias; Otro enfoque es colocar cada objeto en todos los contenedores que se aplican. La primera promueve una jerarquía sencilla y limpia y la segunda promueve la detectabilidad, cada una de ellas tiene ventajas y posibles problemas.

**Es posible que los usuarios no comprendan completamente el diseño del árbol, pero formarán un modelo mental de las relaciones después de interactuar con el árbol durante un tiempo.** Si ese modelo psíquico es incorrecto, genera confusión. Por ejemplo, supongamos que se puede encontrar un reproductor de música en los contenedores Multimedia, Storage y USB. Esta disposición mejora la detectabilidad. Si un usuario encuentra primero el dispositivo en Multimedia, el usuario puede concluir que todos los dispositivos, como los reproductores de música, aparecen en el contenedor Multimedia. A continuación, el usuario esperará que aparezcan dispositivos similares, como cámaras digitales, en el contenedor Multimedia y se confundirá si no es así.

**El desafío al diseñar un árbol es equilibrar la detectabilidad con un modelo de usuario predecible que minimice la confusión.**

### <a name="breadth-vs-depth"></a>Amplitud frente a profundidad

Los estudios de facilidad de uso han demostrado que los usuarios tienen más éxito en la búsqueda de objetos en un árbol que es amplio que en un árbol que es **profundo,** por lo que al diseñar un árbol debe preferir la amplitud sobre la profundidad. Idealmente, un árbol no debe tener más de cuatro niveles (sin contar el nodo raíz) y los objetos a los que se accede con más frecuenteidad deben aparecer en los dos primeros niveles.

### <a name="other-principles"></a>Otros principios

-   Cuando los usuarios encuentran lo que buscan, dejan de buscar. No buscan ver dónde se puede encontrar un objeto porque no es necesario. Esos usuarios pueden suponer que la primera ruta de acceso que encuentran es la única.
-   Los usuarios tienen problemas para encontrar objetos en árboles grandes y complejos. Los usuarios no realizarán una búsqueda exhaustiva y manual para buscar objetos en dichos árboles. se detienen una vez que creen que han prescindido de un esfuerzo razonable. Por lo tanto, los árboles grandes y complejos deben complementarse con otros métodos de acceso, como la búsqueda de palabras, un índice o el filtrado.
-   Algunos programas permiten a los usuarios crear sus propios árboles. Aunque estos árboles auto diseñados podrían estar alineados con el modelo psíquico de un usuario, a menudo se crean de forma deficiente y se mantienen mal. Por ejemplo, mientras que un sistema de archivos, un programa de correo electrónico y una lista de favoritos suelen almacenar tipos similares de información, los usuarios rara vez se preocupan de organizarlos de la misma manera.

**Si solo hace una cosa...**

Sopese detenidamente las ventajas e inconvenientes del uso de vistas de árbol. Tener datos organizados jerárquicamente no significa que tenga que usar una vista de árbol.

## <a name="usage-patterns"></a>Patrones de uso

Las vistas de árbol tienen varios patrones de uso:



| Uso                           |    Ejemplo                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Vistas de árbol solo con nodos de contenedor**<br/> los usuarios pueden ver e interactuar con un contenedor a la vez. <br/>                        | Normalmente, estas vistas de árbol tienen un control asociado que muestra el contenido del contenedor seleccionado, por lo que los usuarios solo pueden interactuar con un contenedor a la vez. <br/> ![captura de pantalla del panel de contenedor y el panel de contenido ](images/ctrl-tree-views-image6.png)<br/> En este ejemplo, la vista de árbol solo tiene nodos de contenedor. El contenido del nodo seleccionado se muestra en el control de vista de lista asociado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Vistas de árbol con nodos de contenedor y hoja**<br/> los usuarios pueden ver contenedores y hojas e interactuar con ellos.<br/>                       | Normalmente, estas vistas de árbol tienen un control asociado que muestra el contenido del contenedor o hoja seleccionados. Permitir que los usuarios interactúen con hojas a menudo hace que sea necesario admitir varias selecciones. <br/> ![captura de pantalla del panel de vista de árbol y el panel de contenido ](images/ctrl-tree-views-image7.png)<br/> En este ejemplo, la vista de árbol tiene nodos de contenedor y hoja. Puesto que se admite la selección múltiple, el contenido de los elementos abiertos se muestra mediante [tabulaciones](ctrl-tabs.md) en el control asociado.<br/> Como alternativa, la vista de árbol puede tener una lista organizada, donde los contenedores son encabezados y las hojas son opciones. <br/> ![captura de pantalla de la vista de árbol con encabezados y opciones ](images/ctrl-tree-views-image8.png)<br/> En este ejemplo, las hojas de árbol son opciones y los contenedores son categorías de opciones.<br/> |
| **Vistas de árbol de casilla**<br/> los usuarios pueden seleccionar cualquier número de elementos, incluido ninguno.<br/>                                             | Las casillas indican claramente que es posible realizar una selección múltiple. use este patrón de árbol cuando la selección múltiple sea esencial o se use con frecuencia. <br/> ![captura de pantalla de la vista de árbol con casillas ](images/ctrl-tree-views-image9.png)<br/> En este ejemplo, una vista de árbol de casilla permite activar o desactivar la selección de características.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Generadores de vistas de árbol**<br/> Los usuarios pueden crear un árbol agregando un contenedor o hoja a la vez y, opcionalmente, estableciendo el orden.<br/> | Los usuarios pueden crear o modificar muchos árboles. algunos árboles se construyen en su lugar mediante menús contextuales y arrastrar y colocar (como las carpetas en el Explorador de Windows), mientras que otros árboles se construyen mediante un cuadro de diálogo especializado (como la lista de favoritos en Windows Internet Explorer). <br/> ![captura de pantalla del cuadro de diálogo favoritos ](images/ctrl-tree-views-image10.png)<br/> En este ejemplo de Internet Explorer, los usuarios pueden crear su propia lista de favoritos mediante un cuadro de diálogo.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| **Vistas de árbol con métodos de acceso alternativos**<br/> los usuarios pueden encontrar objetos de maneras distintas de usar un árbol jerárquico.<br/>        | Como se mencionó anteriormente, los usuarios tienen problemas para encontrar objetos en árboles grandes y complejos, por lo que estos árboles deben complementarse con otros métodos de acceso, como una búsqueda de palabras, un índice o un filtrado. <br/> ![captura de pantalla de las pestañas de contenido, índice y favoritos ](images/ctrl-tree-views-image11.png)<br/> En este ejemplo, los usuarios también pueden acceder a la información mediante una tabla de contenido, un índice y favoritos. para algunos usuarios, las pestañas de índice y búsqueda pueden ser más útiles que la pestaña de contenido.<br/> ![captura de pantalla del menú inicio de Windows y el cuadro de búsqueda ](images/ctrl-tree-views-image12.png)<br/> En este ejemplo, el Windows menú Inicio también permite a los usuarios acceder a programas, archivos y páginas web escribiendo parte del nombre en el cuadro Buscar.<br/>                                                                                                             |



 

## <a name="guidelines"></a>Directrices

### <a name="presentation"></a>Presentación

-   **Dentro de un contenedor, ordene los elementos en un orden lógico.** Ordene los nombres en orden alfabético, los números en orden numérico y las fechas en orden cronológico.
-   **Use el atributo Always Show Selection** para que los usuarios puedan determinar fácilmente el elemento seleccionado, incluso cuando el control no tenga el foco de entrada.
-   **Si el árbol actúa como una tabla de contenido, use el atributo Expandir único para simplificar la administración del árbol.** De este modo, solo se expande la parte pertinente del árbol.
-   **Evite presentar árboles vacíos.** Si un usuario crea un árbol, inicialice el árbol con instrucciones o elementos de ejemplo que los usuarios puedan necesitar.

    ![captura de pantalla de la lista de favoritos de Internet Explorer ](images/ctrl-tree-views-image13.png)

    En este ejemplo, la lista se presenta inicialmente con ejemplos.

-   **No haga que los nodos de contenedor se contraigan si los usuarios no tienen ninguna razón para contraerlos.** Si lo hace, se agrega una complejidad innecesaria.
-   **Si el rendimiento de la carga es un problema, muestre solo los contenedores de primer y segundo nivel del árbol de forma predeterminada.** A continuación, puede cargar datos adicionales a petición cuando un usuario expande ramas en el árbol.
-   **Si los usuarios expanden** o contraen un contenedor, haga que ese estado se conserve para que se haga efectivo la próxima vez que se muestre la vista de árbol, a menos que sea probable que los usuarios prefieran comenzar en el estado predeterminado. La persistencia debe estar en una vista por árbol y por usuario.
-   **Si los contenedores de alto nivel tienen contenido similar, considere la posibilidad de usar pistas visuales para diferenciarlos.**

    **Incorrecto:**

    ![captura de pantalla de elementos de Outlook con iconos diferentes ](images/ctrl-tree-views-image14.png)

    En este ejemplo, las carpetas Buzón y Archivo tienen contenido similar. Una vez que los árboles se expanden aún más, es muy difícil para los usuarios saber dónde se encuentran en el árbol, lo que provoca confusión. El uso de iconos ligeramente diferentes en las distintas secciones solucionaría este problema.

-   **Replantear las líneas de conexión.** Aunque estas líneas muestran claramente las relaciones entre los nodos de contenedor y hoja, agregan desorden visual sin ayudar significativamente a la comprensión. En concreto, no ayudan cuando los nodos se cierran juntos, ni ayudan cuando los nodos están tan separados que es necesario desplazarse.

    **Correcto:**

    ![captura de pantalla de la vista de árbol con líneas de conexión ](images/ctrl-tree-views-image15.png)

    **Mejor:**

    ![captura de pantalla de la vista de árbol sin conectar líneas ](images/ctrl-tree-views-image16.png)

    Las líneas de conexión hacen poco para ayudar a la comprensión.

### <a name="interaction"></a>Interacción

-   **Considere la posibilidad de proporcionar un comportamiento de doble clic.** Hacer doble clic debe tener el mismo efecto que seleccionar un elemento y realizar su comando predeterminado.
-   **Haga que el comportamiento de doble clic sea redundante.** Siempre debe haber un botón de comando o un comando de menú contextual que tenga el mismo efecto.
-   Si un elemento requiere una explicación adicional, **proporcione la explicación en una información sobre**.

    ![captura de pantalla de favoritos con información sobre un elemento ](images/ctrl-tree-views-image17.png)

    En este ejemplo, una información sobre información proporciona más información.

-   **Proporcione menús contextuales de comandos pertinentes.** Estos comandos incluyen Cortar, Copiar, Pegar, Quitar o Eliminar, Cambiar nombre y Propiedades.
-   **Al deshabilitar una vista de árbol, deshabilite también las etiquetas asociadas y los botones de comando.**

### <a name="tree-organization"></a>Organización de árbol

-   **Use una estructura jerárquica natural que sea familiar para la mayoría de los usuarios.**
-   **Si no puede usar esta estructura, intente equilibrar la detectabilidad con un modelo de usuario predecible que minimice la confusión.**
-   **Para mejorar la detectabilidad de forma segura, coloque un elemento en varios contenedores cuando:**
    -   El elemento no está relacionado con ningún otro elemento similar (por lo que los usuarios no se confunden por asociaciones incorrectas).
    -   Solo hay algunos de estos elementos ubicados redundantemente (por lo que el árbol no se infla).
-   **Use la estructura jerárquica más sencilla que funcione bien.** Para ello:
    -   Coloque los objetos a los que se accede con más frecuenteidad en los dos primeros niveles del árbol (sin contar el nodo raíz) y coloque los objetos a los que se accede con menos frecuenteidad más abajo en la jerarquía.
    -   Elimine contenedores de nivel intermedio innecesarios o combine contenedores redundantes de nivel intermedio.
-   **Prefiere la amplitud sobre la profundidad.** Idealmente, un árbol no debe tener más de cuatro niveles y los objetos a los que se accede con más frecuenteidad deben aparecer en los dos primeros niveles.
-   **Determine si realmente necesita un nodo raíz.** Proporcione un nodo raíz si los usuarios necesitan la capacidad de realizar comandos en todo el árbol (posiblemente mediante un menú contextual en el nodo raíz). De lo contrario, el árbol es más sencillo y fácil de usar sin él.
-   **Si el árbol tiene métodos de acceso alternativos, como una búsqueda de palabras o un índice, optimice el árbol para examinarlo centrándose en el contenido más útil.** Con métodos de acceso alternativos, el contenido del árbol no tiene que ser completo. Simplificar el árbol facilita a los usuarios la búsqueda del contenido más útil.

### <a name="check-box-tree-views"></a>Vistas de árbol de casilla

-   **Muestra el número de elementos seleccionados debajo de la lista,** especialmente si es probable que los usuarios seleccionen varios elementos. Estos comentarios ayudan a los usuarios a confirmar que su selección es correcta.

    ![captura de pantalla del número de elementos seleccionados ](images/ctrl-tree-views-image18.png)

    En este ejemplo, el número de elementos seleccionados se muestra debajo del árbol. Está claro que dos elementos no están seleccionados.

-   Si hay potencialmente muchos elementos y es probable que se seleccionen o desactiven todos, agregue los botones Seleccionar todo y Borrar todos los comandos.
-   **Use las casillas de estado mixto para indicar la selección parcial de los elementos de un contenedor.**

    **Correcto:**

    ![captura de pantalla de la ventana con casillas de estado mixto ](images/ctrl-tree-views-image19.png)

    En este ejemplo, se usan las casillas de estado mixto para indicar la selección parcial.

## <a name="recommended-sizing-and-spacing"></a>Tamaño y espaciado recomendados

![captura de pantalla del tamaño y el espaciado de la vista de árbol ](images/ctrl-tree-views-image20.png)

Tamaño y espaciado recomendados para los controles de vista de árbol.

-   **Elija un ancho de vista de árbol que** evite la necesidad de desplazamiento horizontal para la mayoría de los elementos cuando el árbol está totalmente expandido.
-   **Incluya un 30 % adicional para adaptarse a la localización.**
-   **Elija un alto de vista de árbol que elimine el desplazamiento vertical innecesario.** Considere la posibilidad de hacer que una vista de árbol sea ligeramente más larga (o incluso más si hay espacio disponible) si esto reduce la necesidad de una barra de desplazamiento vertical.

    **Incorrecto:**

    ![captura de pantalla del control de vista de árbol corto y estrecho ](images/ctrl-tree-views-image21.png)

    En este ejemplo, hacer que la vista de árbol sea ligeramente más ancha y más larga eliminaría las barras de desplazamiento en la mayoría de los casos. En este árbol concreto, solo se puede abrir un contenedor a la vez.

-   **Si los usuarios se benefician de hacer que la vista de árbol sea mayor, haga que la vista de árbol y su ventana primaria se puedan redimensionar.** Esto permite a los usuarios ajustar el tamaño de la vista de árbol según sea necesario.

## <a name="labels"></a>Etiquetas

### <a name="control-labels"></a>Etiquetas de control

-   Todas las vistas de árbol necesitan etiquetas. Escriba la etiqueta como una palabra o frase, no como una frase, terminando con dos puntos y usando [texto estático](glossary.md).
-   Asigne una clave de acceso única. Para obtener instrucciones de asignación, vea [Teclado](inter-keyboard.md).
-   Use mayúsculas de estilo de frase.
-   Coloque la etiqueta encima del control y alinee la etiqueta con el borde izquierdo del control.
-   Para las vistas de árbol de selección múltiple, escriba la etiqueta para que esté claro que es posible realizar una selección múltiple. Las etiquetas de vista de árbol de casilla pueden ser menos explícitas.

    **Incorrecto:**

    ![captura de pantalla de la vista de árbol con la etiqueta de componentes ](images/ctrl-tree-views-image22.png)

    En este ejemplo, la etiqueta no proporciona información sobre la selección múltiple.

    **Mejor:**

    ![captura de pantalla de la vista de árbol con la etiqueta "uno o más" ](images/ctrl-tree-views-image23.png)

    En este ejemplo, la etiqueta indica claramente que es posible realizar una selección múltiple.

    **Mejor:**

    ![captura de pantalla de la vista de árbol con casillas ](images/ctrl-tree-views-image24.png)

    En este ejemplo, las casillas indican claramente que es posible realizar una selección múltiple, por lo que la etiqueta no tiene que ser explícita.

### <a name="data-text"></a>Texto de datos

-   Use mayúsculas de estilo de frase.

### <a name="instructional-text"></a>Texto informativo

-   Si necesita agregar texto informativo sobre una vista de árbol, agrégrelo encima de la etiqueta. Use oraciones completas con puntuación final.
-   Use mayúsculas de estilo de frase.
-   Las explicaciones complementarias que son útiles pero no necesarias deben mantenerse cortas. Coloque esta información entre paréntesis entre la etiqueta y los dos puntos, después de la instrucción main si se usa en lugar de una etiqueta, o debajo del control .

    ![captura de pantalla de la explicación debajo de la vista de árbol ](images/ctrl-tree-views-image8.png)

    En este ejemplo, la explicación complementaria está debajo del control .

## <a name="documentation"></a>Documentación

Al hacer referencia a vistas de árbol:

-   Use el texto exacto de la etiqueta, incluida su mayúscula, pero no incluya el carácter de subrayado o dos puntos de la clave de acceso. Incluya la lista de palabras o la lista jerárquica si el contexto requiere hacer una distinción de las listas normales.
-   Para los elementos de árbol, use el texto exacto del elemento, incluido su uso de mayúsculas.
-   Consulte vistas de árbol como vistas de árbol solo en programación y otra documentación técnica. En cualquier otro lugar, use lista o lista jerárquica porque el árbol de términos es confuso para la mayoría de los usuarios.
-   Para describir la interacción del usuario, use select para los datos y expanda y contraiga los botones más y menos.
-   Cuando sea posible, formatee los elementos de árbol y etiqueta mediante texto en negrita. De lo contrario, coloque la etiqueta y los elementos entre comillas solo si es necesario para evitar confusiones.

Ejemplo: en la **lista Contenido,** seleccione **Interfaz de usuario Diseño.**

Al hacer referencia a las casillas de una vista de árbol:

-   Use el texto de etiqueta exacto, incluido su uso de mayúsculas e incluya las palabras, casilla de verificación. No incluya el carácter de subrayado de la clave de acceso.
-   Para describir la interacción del usuario, use seleccionar y borrar.
-   Cuando sea posible, formatee la etiqueta con texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.

Ejemplo: en la **lista Elementos de los que realizar una** copia de seguridad, active **Mis documentos** casilla.

