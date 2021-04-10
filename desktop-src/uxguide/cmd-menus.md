---
title: Menús (conceptos básicos del diseño)
description: Los menús son listas jerárquicas de comandos u opciones disponibles para los usuarios en el contexto actual.
ms.assetid: 3772ff8e-8057-476d-b62b-efbd5e07907f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8054a01e4198f3592a34ae09635dd60f392da1eb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104279742"
---
# <a name="menus-design-basics"></a>Menús (conceptos básicos del diseño)

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Los menús son listas jerárquicas de comandos u opciones disponibles para los usuarios en el contexto actual.

Los menús desplegables son menús que se muestran a petición al hacer clic o mantener el mouse. Normalmente están ocultas de la vista y, por lo tanto, son un medio eficaz para ahorrar espacio en la pantalla. Un menú de submenú o en cascada es un menú secundario que se muestra a petición desde dentro de un menú. Se indican mediante una flecha al final de la etiqueta de submenú. Un elemento de menú es un comando o opción individual dentro de un menú.

Los menús suelen mostrarse en una barra de menús, que es una lista de categorías de menús etiquetadas que normalmente se encuentran cerca de la parte superior de una ventana. Por el contrario, un menú contextual se reduce cuando los usuarios hacen clic con el botón secundario en un objeto o región de ventana que admite un menú contextual.

![captura de pantalla de la barra de menús con menú y submenú ](images/cmd-menus-image1.png)

Barra de menús típica que muestra un menú desplegable y un submenú.

> [!Note]  
> Las instrucciones relacionadas con los [botones de comando](ctrl-command-buttons.md), las [barras de herramientas](cmd-toolbars.md)y el [teclado](inter-keyboard.md) se presentan en artículos independientes.

 

## <a name="usage-patterns"></a>Patrones de uso

Los menús tienen varios patrones de uso:



|                                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Barras de menús**<br/> una barra de menús muestra los comandos y las opciones de los menús desplegables. <br/>                                               | las barras de menús son muy comunes y fáciles de encontrar, así como un uso eficaz del espacio. <br/> ![captura de pantalla de la barra de menús con el menú desplegable ](images/cmd-menus-image2.png)<br/> Barra de menús de Windows Mail.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Menús de barra de herramientas**<br/> barra de menús implementada como una barra de herramientas. <br/>                                                                   | los menús de barra de herramientas son barras de herramientas que se componen principalmente de comandos en [botones de menú](ctrl-command-buttons.md) y botones de expansión, con solo unos pocos comandos directos, si los hay. <br/> ![captura de pantalla del menú de la barra de herramientas con menú desplegable ](images/cmd-menus-image3.png)<br/> Menú de la barra de herramientas de la Galería fotográfica de Windows.<br/> Para obtener instrucciones sobre este patrón, vea [barras de herramientas](cmd-toolbars.md).<br/>                                                                                                                                                                                                             |
| **Menús de pestañas**<br/> botones dentro de pestañas que muestran un pequeño conjunto de comandos y opciones relacionados con una pestaña en un menú desplegable. <br/> | las pestañas con menús se parecen a las pestañas ordinarias, excepto por su parte inferior, tiene un botón con una flecha desplegable. al hacer clic en el botón, se muestra un menú desplegable en lugar de seleccionar la pestaña. <br/> ![captura de pantalla del menú de pestañas con menú desplegable ](images/cmd-menus-image4.png)<br/> Los menús de pestañas se usan en Windows Media Player.<br/>                                                                                                                                                                                                                                                                                           |
| **Botones de menú**<br/> botones de comando que muestran un pequeño conjunto de comandos relacionados en un menú desplegable. <br/>                       | los [botones de menú](ctrl-command-buttons.md) tienen el mismo aspecto que los botones de comando ordinarios, salvo que tienen una flecha desplegable dentro de ellos. al hacer clic en el botón, se muestra un menú desplegable en lugar de ejecutar un comando.<br/> los [botones de expansión](ctrl-command-buttons.md) son similares a los botones de menú, salvo que son variaciones de un comando y, al hacer clic en la parte izquierda del botón, la acción se realiza directamente en la etiqueta.<br/> ![captura de pantalla del botón de menú con comandos desplegables ](images/cmd-menus-image5.png)<br/> Botón de menú con un pequeño conjunto de comandos relacionados.<br/> |
| **Menús contextuales**<br/> menús desplegables que muestran un pequeño conjunto de comandos y opciones relacionados con el contexto actual. <br/>       | menús contextuales desplegables cuando los usuarios hacen clic con el botón derecho en un objeto o región de ventana que admite un menú contextual. <br/> ![captura de pantalla del menú contextual que muestra comandos ](images/cmd-menus-image6.png)<br/> un menú contextual del explorador de Windows.<br/> Si los menús contextuales son la mejor opción de menú pero necesita una solución adecuada para todos los usuarios, puede usar un botón de flecha desplegable de menú. <br/> ![captura de pantalla de la foto con el botón de menú desplegable ](images/cmd-menus-image7.png)<br/> Un menú contextual se hace visible con un botón desplegable de menú.<br/>                                                   |
| **Menús del panel de tareas**<br/> un pequeño conjunto de comandos relacionados con el objeto o el modo de programa seleccionado. <br/>                              | a diferencia de los menús contextuales, se muestran automáticamente dentro de un panel de ventana, en lugar de a petición. <br/> ![captura de pantalla de la foto con el menú del panel de tareas a la derecha ](images/cmd-menus-image8.png)<br/> Menú del panel de tareas del visor de la Galería fotográfica de Windows.<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

Para decidirte, intenta responder a estas preguntas:

### <a name="menu-bars"></a>Barras de menús

Se aplican las condiciones siguientes:

-   ¿La ventana es una ventana principal?
-   ¿Hay muchos elementos de menú?
-   ¿Hay muchas categorías de menús?
-   ¿La mayoría de los elementos de menú se aplican a todo el programa y a la ventana principal?
-   ¿El menú debe funcionar para todos los usuarios?

Si es así, considere la posibilidad de usar una barra de menús.

### <a name="toolbar-menus"></a>Menús de barra de herramientas

Se aplican las condiciones siguientes:

-   ¿La ventana es una ventana principal?
-   ¿La ventana tiene una barra de herramientas?
-   ¿Hay solo algunas categorías de menús?
-   ¿El menú debe funcionar para todos los usuarios?

Si es así, considere la posibilidad de usar un menú de barra de herramientas en lugar de o además de una barra de menús.

### <a name="tab-menus"></a>Menús de pestañas

Se aplican las condiciones siguientes:

-   ¿La ventana es una ventana principal?
-   ¿La ventana tiene pestañas, donde cada pestaña se usa para un conjunto de tareas dedicado (en lugar de usar pestañas para mostrar vistas diferentes)?
-   ¿Hay alguna categoría de menú que se aplique a cada pestaña?
-   ¿Hay muchos comandos y opciones, pero solo un conjunto pequeño para cada pestaña?

Si es así, considere la posibilidad de usar un menú de pestaña en lugar de una barra de menús.

### <a name="context-menu"></a>Menú contextual

Se aplican las condiciones siguientes:

-   ¿Hay un pequeño conjunto de comandos contextuales y opciones que se aplican al objeto o a la región de la ventana seleccionados?
-   ¿Son redundantes estos elementos de menú?
-   ¿Los usuarios de destino están familiarizados con los menús contextuales?

Si es así, considere la posibilidad de proporcionar menús contextuales para los objetos y las regiones de ventana que los necesiten.

En el caso de los programas basados en explorador, los menús del panel de tareas son una solución más común para los comandos contextuales. Actualmente, los usuarios esperan que los menús contextuales de los programas basados en explorador sean genéricos e inservibles.

### <a name="task-pane-menu"></a>Menú del panel de tareas

Se aplican las condiciones siguientes:

-   ¿La ventana es una ventana principal?
-   ¿Hay un pequeño conjunto de comandos contextuales y opciones que se aplican al modo de objeto o de programa seleccionado?
-   ¿Hay algunas categorías de menús?
-   ¿El menú debe funcionar para todos los usuarios?

Si es así, considere la posibilidad de usar un menú del panel de tareas en lugar de un menú contextual.

## <a name="design-concepts"></a>Conceptos de diseño

Menús efectivos que fomentan una buena experiencia del usuario:

-   Use una presentación de comandos que coincida con el tipo de programa, los tipos de ventana, el uso del comando y los usuarios de destino.
-   Están bien organizados, mediante el uso de la organización de menú estándar cuando sea necesario.
-   Use barras de menús, barras de herramientas y menús contextuales de manera eficaz.
-   Usar iconos eficazmente.
-   Usar claves de acceso y teclas de método abreviado de forma eficaz.

**Si solo hace algo...**

Elija una presentación de comandos que coincida con el tipo de programa, los tipos de ventana, el uso del comando y los usuarios de destino.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Todos los patrones de menú excepto las barras de menús necesitan una flecha desplegable para indicar la presencia de un menú desplegable.** La presencia de menús se lleva sin decir en una barra de menús, pero no en los otros patrones.
-   **No cambie los nombres de los elementos de menú de forma dinámica.** Hacerlo es confuso e inesperado. Por ejemplo, no cambie una opción de modo vertical al modo horizontal al seleccionar. En el caso de los modos, use [viñetas y marcas de verificación](#bullets-and-checkmarks) en su lugar.
    -   **Excepción:** Puede cambiar los nombres de los elementos de menú que se basan en los nombres de objeto de forma dinámica. Por ejemplo, las listas de archivos usados recientemente o nombres de ventana pueden ser dinámicas.

### <a name="menu-bars"></a>Barras de menús

-   **Considere la posibilidad de eliminar barras de menús con tres o menos categorías de menús.** Si solo hay algunos comandos, prefiera alternativas más claras, como menús de la barra de herramientas, o más alternativas directas, como botones de comando y vínculos.
-   **No tener más de 10 categorías de menú.** Demasiadas categorías de menú es abrumadora y dificulta el uso de la barra de menús.
-   **Considere la posibilidad de ocultar la barra de menús** si la barra de herramientas o los comandos directos proporcionan casi todos los comandos necesarios para la mayoría de los usuarios. Permitir a los usuarios mostrar u ocultar con una opción de marca de la barra de menús en un menú de la barra de herramientas.

![captura de pantalla de la lista de opciones con la barra de menús seleccionada ](images/cmd-menus-image9.png)

En este ejemplo, Windows Internet Explorer proporciona una opción de barra de menús.

Para obtener más información, consulte [Ocultar barras de menús](#hiding-menu-bars).

### <a name="hiding-menu-bars"></a>Ocultar barras de menús

Por lo general, las barras de herramientas funcionan muy bien con barras de menús, ya que tener ambos permite centrarse en sus puntos fuertes sin poner en peligro.

-   Oculte la barra de menús de forma predeterminada si el diseño de la barra de herramientas hace que una barra de menús sea redundante.
-   Oculte la barra de menús en lugar de quitarla por completo, ya que las barras de menús son más accesibles para los usuarios del teclado.
-   Para restaurar la barra de menús, proporcione una opción de marca de verificación de la barra de menús en la categoría de menú Ver (para barras de herramientas principales) o herramientas (para barras de herramientas secundarias). Para obtener más información, vea [botón de expansión y menú estándar](cmd-toolbars.md).

### <a name="menu-categories"></a>Categorías de menú

-   **Elija nombres de palabras únicas para las categorías de menús.** El uso de varias palabras hace que la separación entre categorías sea confusa.
-   **En el caso de los programas que crean o ven documentos, use las categorías de menús estándar** como archivo, edición, ver, herramientas y ayuda. Esto hace que los elementos de menú comunes sean predecibles y fáciles de encontrar.
-   En el **caso de otros tipos de programas, considere la posibilidad de organizar los comandos y las opciones en categorías naturales más útiles** según el propósito del programa y la manera en que los usuarios piensan en sus tareas y objetivos. No dude en usar la organización de menús estándar si no es adecuada para el programa.
-   **Si decide usar categorías de menú no estándar, debe elegir nombres de categoría correctos.** Para obtener más información, vea la sección [etiquetas](#labels) .
-   **Prefiere categorías de menús orientadas a tareas en categorías genéricas.** Las categorías orientadas a tareas facilitan la búsqueda de elementos de menú.

![captura de pantalla de la barra de menús con RIP, grabación y sincronización ](images/cmd-menus-image10.png)

En este ejemplo, Windows Media Player usa categorías de menús orientadas a tareas.

-   **Evite las categorías de menús con solo uno o dos elementos de menú.** Si es sensato, consolide con otras categorías de menú, quizás mediante un submenú.
-   **Considere la posibilidad de colocar el mismo elemento de menú solo en varias categorías si:**
    -   El elemento de menú pertenece lógicamente a varias categorías de menús.
    -   Tiene datos que muestran que los usuarios tienen problemas para encontrar el elemento en una única categoría de menú.
    -   Solo tiene uno o dos elementos de menú difíciles de encontrar en varias categorías.
-   **No coloque distintos elementos de menú que usen el mismo nombre en varias categorías.** Por ejemplo, no tiene elementos de menú de opciones diferentes en varias categorías.
    -   **Excepción:** El patrón de menú de pestañas puede tener diferentes opciones y elementos de menú de ayuda en cada menú de pestañas.

![captura de pantalla de menús de pestaña con elementos de menú repetidos ](images/cmd-menus-image11.png)

En este ejemplo, Windows Media Player tiene elementos de menú de ayuda y opciones en cada menú de pestañas.

### <a name="menu-item-organization-and-order"></a>Organización y pedido de elementos de menú

-   **Organice los elementos de menú en grupos de siete o menos elementos estrechamente relacionados.** Para ello, los submenús cuentan como un solo elemento de menú en el menú primario.
-   **No coloque más de 25 elementos en un solo nivel de un menú** (sin contar los submenús).
-   **Coloque los separadores entre los grupos dentro de un menú.** Un separador es una sola línea que abarca el ancho del menú.
-   **Dentro de un menú, coloque los grupos en su orden lógico.** Si no hay ningún orden lógico, coloque primero los grupos que se usan con más frecuencia.
-   **Dentro de un grupo, coloque los elementos en su orden lógico.** Si no hay ningún orden lógico, coloque primero los elementos que se usan con más frecuencia. Coloque los elementos numéricos (por ejemplo, porcentajes de zoom) en orden numérico.

### <a name="submenus"></a>Submenus

-   **Evite el uso innecesario de submenús.** Los submenús requieren un mayor esfuerzo físico y, por lo general, dificultan la búsqueda de los elementos de menú.
-   **No coloque los elementos de menú que se usan con frecuencia en un submenú.** Si lo hace, el uso de estos comandos no resultará eficaz. No obstante, puede colocar comandos usados con frecuencia en un submenú si normalmente se tiene acceso a ellos más directamente, como con una barra de herramientas.
-   **Considere la posibilidad de usar un submenú si:**
    -   Esto simplifica el menú primario porque tiene muchos elementos (20 o más), o bien el submenú forma parte de un grupo de más de siete elementos.
    -   Los elementos del submenú se utilizan con menos frecuencia que los del menú primario.
    -   El submenú tendría tres o más elementos.
    -   Hay tres o más comandos que comienzan con la misma palabra. En este caso, use esa palabra como etiqueta de submenú.

![captura de pantalla del menú ' nuevo ' con cuatro elementos de submenú ](images/cmd-menus-image12.png)

En este ejemplo, el nuevo submenú reemplaza a comandos independientes para nuevo mensaje de correo, nuevo mensaje de noticias, nueva carpeta y nuevo contacto.

-   **Use como máximo tres niveles de menús.** Es decir, puede tener un menú principal y, como máximo, dos niveles de submenús. Dos niveles de submenús no deben ser raros.

### <a name="presentation"></a>Presentación

-   **Deshabilite los elementos de menú que no se aplican al contexto actual,** en lugar de quitarlos. Esto hace que el contenido de la barra de menús sea estable y más fácil de encontrar. **Excepciones:**
    -   En el caso de las categorías de menús contextuales, **Quite en lugar de deshabilitar los elementos de menú contextual que no se aplican al contexto actual.** Una categoría de menú es contextual cuando se muestra solo para modos específicos, como cuando se selecciona un determinado tipo de objeto. Para obtener más información, consulte las directrices de [eliminación y deshabilitación](#context-menus) de los menús contextuales.
    -   Si la determinación de Cuándo debe deshabilitarse un elemento de menú provoca problemas de rendimiento perceptibles, deje activo el elemento de menú y, si es necesario, su selección dará como resultado un mensaje de error.

### <a name="tab-menus"></a>Menús de pestañas

-   **Cada menú de pestaña puede tener opciones específicas de contexto y elementos de menú de ayuda.** Esto contrasta con todos los demás patrones de menú. Cada pestaña se usa para un conjunto de tareas dedicado, por lo que cualquier redundancia en los menús de pestañas no es confuso.

### <a name="context-menus"></a>Menús contextuales

-   **Use los menús contextuales solo para los comandos y las opciones contextuales.** Los elementos de menú solo se deben aplicar al objeto o a la región de la ventana seleccionada (o en el que se ha seleccionado), no a todo el programa.
-   **No haga que los comandos solo estén disponibles a través de los menús contextuales.** Al igual que las teclas de método abreviado, los menús contextuales son medios alternativos para realizar comandos y elegir opciones. Por ejemplo, un comando de propiedades también está disponible a través de la barra de menús o la tecla de acceso Alt + Entrar.
-   **Proporcione menús contextuales para todos los objetos y regiones de ventanas** que se beneficien de un pequeño conjunto de comandos y opciones contextuales. Muchos usuarios hacen clic con el botón derecho con regularidad y esperan encontrar menús contextuales en cualquier lugar.
-   **Considere la posibilidad de usar un botón de flecha desplegable de menú para los menús contextuales destinados a todos los usuarios.** Normalmente, los menús contextuales son adecuados para los comandos y las opciones destinadas a usuarios avanzados. Sin embargo, puede usar un botón desplegable de menú en los casos en los que los menús contextuales son la mejor opción de menú y debe dirigirse a todos los usuarios.

![captura de pantalla de la foto con el botón de menú desplegable ](images/cmd-menus-image7.png)

En este ejemplo, se usa un botón desplegable de menú para hacer que un menú contextual sea visible.

**Organización y pedido de elementos de menú**

-   **Organice los elementos de menú en grupos de siete o menos elementos estrechamente relacionados.**
-   **Evite el uso de submenús** para mantener los menús contextuales sencillos, directos y eficaces.
-   **No incluya más de 15 elementos en un menú contextual.**
-   **Coloque los separadores entre los grupos dentro de un menú.** Un separador es una sola línea que abarca el ancho del menú.
-   **Presente los elementos de menú con el siguiente orden:**

<dl> Comandos principales (usados con mayor frecuencia)<dl> Abrir  
Ejecutar  
Reproducir  
Imprime <separator>  
</dl> </dd> <dd>Comandos secundarios admitidos por el objeto<dl> <separator>  
</dl> </dd> Transferir comandos<dl> Cortar  
Copiar  
Copiar <separator>  
</dl> </dd> <dd>Configuración del objeto<dl> <separator>  
</dl> </dd> Comandos de objeto<dl> Eliminar  
Cambiar el nombre <separator>  
Propiedades
</dl> </dd> </dl>

**Presentación**

-   **Mostrar el comando predeterminado con negrita.** Cuando sea práctico, también conviértalo en el primer elemento de menú. El comando predeterminado se invoca cuando los usuarios hacen doble clic o seleccionan un objeto y presionan entrar.
-   **Quite en lugar de deshabilitar los elementos de menú contextual que no se aplican al contexto actual.** Al hacerlo, los menús contextuales se contextualan y eficientes.
    -   **Excepción:** Deshabilite los elementos de menú que no se aplican si hay una expectativa razonable de que estén disponibles:
        -   Tenga siempre los comandos de menú contextual estándar pertinentes, como cortar, copiar, pegar, eliminar y cambiar nombre.
        -   Tenga siempre los comandos que completen conjuntos relacionados. Por ejemplo, si hay un retroceso, debería haber también un reenvío. Si hay un corte, siempre debe copiar y pegar.

### <a name="bullets-and-checkmarks"></a>Viñetas y marcas de verificación

-   **Los elementos de menú que son opciones pueden utilizar viñetas y marcas de verificación.** Los comandos no pueden.
-   **Use una viñeta para elegir una opción de un pequeño conjunto de opciones mutuamente excluyentes.** Siempre debe haber al menos dos viñetas en un grupo. Para obtener más información, consulte [botones de radio](ctrl-radio-buttons.md).
-   **Use una marca de verificación para activar o desactivar una configuración independiente.** Si los Estados seleccionado y borrado no son claros y no ambiguos, utilice en su lugar un conjunto de viñetas. Para obtener más información, vea [casillas](ctrl-check-boxes.md).
-   **Para un estado de marca de verificación mixto, mostrar un elemento de menú sin marca de verificación.** El estado mixto se usa para la selección múltiple para indicar que la opción está establecida para algunos objetos, pero no para todos, por lo que cada objeto individual tiene el estado seleccionado o desactivado. El estado mixto no se utiliza como tercer Estado para un elemento individual.
-   **Coloque separadores entre los conjuntos de marcas de verificación o viñetas relacionados.** Un separador es una sola línea que abarca el ancho del menú.

### <a name="icons"></a>Iconos

-   **Considera la posibilidad de proporcionar iconos de elemento de menú para:**
    -   Los elementos de menú que se usan con más frecuencia.
    -   Elementos de menú cuyo icono es estándar y bien conocido.
    -   Elementos de menú cuyo icono muestra bien lo que hace el comando.
-   **Si usa iconos, no dude en proporcionarlos para todos los elementos de menú.** Los iconos crípticos no son útiles, provocan una aglutinación visual y evitan que los usuarios se centren en los elementos de menú importantes.

![captura de pantalla de los elementos de menú con y sin iconos ](images/cmd-menus-image13.png)

En este ejemplo, el menú organizar solo tiene iconos para los elementos de menú que se usan con más frecuencia.

-   **Asegúrese de que los iconos de menú cumplen las directrices de iconos de estilo Aero.**

Para obtener más información y ejemplos, vea [iconos](vis-icons.md).

### <a name="access-keys"></a>Claves de acceso

-   **Asignar teclas de acceso a todos los elementos de menú.** Sin excepciones.
-   **Siempre que sea posible, asigne claves de acceso para comandos de uso frecuente según las asignaciones de teclas de acceso estándar.** Aunque las asignaciones de claves de acceso coherentes no siempre son posibles, son realmente preferibles, especialmente para los comandos que se usan con frecuencia.
-   **Para los elementos de menú dinámicos (por ejemplo, los archivos usados recientemente), asigne claves de acceso numéricamente.**

![captura de pantalla de elementos de menú con claves de acceso numéricas ](images/cmd-menus-image14.png)

En este ejemplo, el programa Paint de Windows asigna claves de acceso numéricas a archivos usados recientemente.

-   **Asignar claves de acceso únicas dentro de un nivel de menú.** Puede reutilizar las claves de acceso en distintos niveles de menú.
-   **Facilite la búsqueda de las claves de acceso:**
    -   En el caso de los elementos de menú que se usan con más frecuencia, elija caracteres al principio de la primera o la segunda palabra de la etiqueta, preferiblemente el primer carácter.
    -   En el caso de los elementos de menú que se utilizan con menos frecuencia, seleccione las letras que son una consonante distintiva o una vocal en la etiqueta.
-   **Prefiere caracteres con ancho ancho,** como w, m y mayúsculas.
-   **Prefiere una consonante distintiva o una vocal,** como "x" en "Exit".
-   **Evite el uso de caracteres que hagan que el subrayado sea difícil de ver,** como (desde la mayoría de los problemas a los menos problemáticos):
    -   Letras que solo tienen un píxel de ancho, como i y l.
    -   Letras con descendentes, como g, j, p, q e y.
    -   Letras situadas junto a una letra con un descendiente.

Para obtener más instrucciones y ejemplos, consulte [teclado](inter-keyboard.md).

### <a name="shortcut-keys"></a>Teclas de método abreviado

-   **Asignar teclas de método abreviado a los elementos de menú que se usan con más frecuencia.** Los elementos de menú que se usan con poca frecuencia no necesitan teclas de método abreviado, ya que los usuarios pueden utilizar las teclas de acceso.
-   **No convierta una tecla de método abreviado en la única forma de realizar una tarea.** Los usuarios también deben poder usar el mouse o el teclado con las teclas de tabulación, de flecha y de acceso.
-   **En el caso de las teclas de método abreviado conocidas, use las asignaciones estándar.**
-   **No asigne diferentes significados a teclas de método abreviado conocidas.** Dado que se memorizan, los significados incoherentes para los accesos directos conocidos son frustrados y propensos a errores. Consulte teclas de método abreviado de teclado de Windows para conocer las teclas de método abreviado utilizadas por los programas de Windows.
-   **No intente asignar teclas de método abreviado de todo el sistema.** Las teclas de método abreviado del programa solo surtirán efecto cuando el programa tenga el foco de entrada.
-   **Documente todas las teclas de método abreviado.** Esto ayuda a los usuarios a aprender las asignaciones de teclas de método abreviado.
    -   **Excepción:** No muestre las asignaciones de teclas de método abreviado dentro de los menús contextuales. Los menús contextuales no muestran las asignaciones de teclas de método abreviado porque están optimizadas para mayor eficacia.
-   **Para asignaciones de clave no estándar:**
    -   **Elija las teclas de método abreviado que no tienen asignaciones estándar.** No reasigne nunca las teclas de método abreviado estándar.
    -   **Use asignaciones de clave no estándar de forma coherente en todo el programa.** No asigne diferentes significados en distintas ventanas.
    -   **Si es posible, elija las asignaciones de teclas de tecla de inicio,** especialmente para los comandos usados con frecuencia.
    -   **Use las teclas de función para los comandos que tienen un efecto de pequeña escala,** como los comandos que se aplican al objeto seleccionado. Por ejemplo, F2 cambia el nombre del elemento seleccionado.
    -   **Use combinaciones de teclas Ctrl para los comandos que tienen un efecto a gran escala,** como los comandos que se aplican a un documento completo. Por ejemplo, Ctrl + S guarda el documento actual.
    -   **Use combinaciones de teclas Mayús para los comandos que extienden o complementan las acciones de la tecla de método abreviado estándar.** Por ejemplo, la tecla de método abreviado Alt + Tab recorre las ventanas principales abiertas, mientras que Alt + Mayús + Tab se desplaza en orden inverso. Del mismo modo, F1 muestra la ayuda, mientras que Mayús + F1 muestra la ayuda contextual.
    -   **No utilice los caracteres siguientes para las teclas de método abreviado:** @ $ {} \[ \] \\  ~  \| ^ '  < >. Estos caracteres requieren diferentes combinaciones de claves en los idiomas o son específicas de la configuración regional.
    -   **No use las combinaciones CTRL + ALT,** ya que Windows interpreta esta combinación en algunas versiones de idioma como una clave AltGr, que genera caracteres alfanuméricos.
-   **Si el programa asigna muchas teclas de método abreviado, proporcione la capacidad de personalizar las asignaciones.** Esto permite a los usuarios reasignar las teclas de método abreviado en conflicto y migrar desde otros productos. La mayoría de los programas no asignan suficientes teclas de método abreviado para necesitar esta característica.

Para obtener más instrucciones y las asignaciones de teclas de método abreviado estándar, consulte [teclado](inter-keyboard.md).

### <a name="standard-menus"></a>Menús estándar

-   **Use la organización de menús estándar para los programas que crean o ven documentos.** La organización de menús estándar hace que los elementos de menú comunes sean predecibles y fáciles de encontrar.
-   **Para otros tipos de programas, use la organización de menús estándar solo cuando tenga sentido.** Considere la posibilidad de organizar los comandos y las opciones en categorías más útiles y naturales basadas en el propósito del programa y en la forma en que los usuarios piensan en sus tareas y objetivos.

**Barras de menús estándar**

La estructura de la barra de menús estándar es la siguiente. Esta lista muestra la categoría del menú y las etiquetas del elemento, su orden con los separadores, el acceso y las teclas de método abreviado, así como sus puntos suspensivos.

<dl> Archivo<dl> Nuevo Ctrl + N  
Abrir... Ctrl + O  
Cerrar <separator>  
Guardar Ctrl + S  
Guardar como... <separator>  
Enviar a <separator>  
Imprimir... Ctrl + P  
Vista previa de impresión  
Configurar página <separator>  
1 <filename> 2 <filename> 3 <filename> ... <separator>  
Salir Alt + F4 (normalmente no se proporciona el acceso directo)
</dl> </dd> Edit<dl> Deshacer Ctrl + Z  
Rehacer Ctrl + Y <separator>  
Cortar Ctrl + X  
Copiar Ctrl + C  
Pegar Ctrl + V <separator>  
Seleccionar todo Ctrl + A <separator>  
Eliminar del (normalmente no se proporciona el acceso directo) <separator>  
Buscar... Ctrl + F  
Buscar siguiente F3 (no se suele proporcionar el comando)  
Reemplazar... Ctrl + H  
Vete a... Ctrl + G
</dl> </dd> View<dl> Barras de herramientas  
Barra de estado <separator>  
</dl> </dd> Zoom<dl> Acercar Ctrl + +  
Alejar Ctrl +- <separator>  
Pantalla completa F11  
Actualizar F5
</dl> </dd> <dd>Herramientas<dl> ... <separator>  
Opciones
</dl> </dd> Ayuda<dl> <program name> ayuda F1 <separator>  
Sobre <program name>  
</dl> </dd> </dl>

**Botones del menú de la barra de herramientas estándar**

Los botones del menú de la barra de herramientas estándar son los siguientes. Esta lista muestra la categoría del menú y las etiquetas del elemento, su orden con separadores, sus teclas de método abreviado y sus puntos suspensivos.

<dl> Herramientas<dl> ScreenF11 completo (reasignar la clave de acceso si se usa también buscar).  
Barras de herramientas (tenga en cuenta que el comando de la barra de menús va aquí). <separator>  
Imprimir...  
Buscar... <separator>  
Zoom  
Tamaño del texto <separator>  
Opciones
</dl> </dd> Organize<dl> New folderCtrl + N <separator>  
CutCtrl + X  
CopyCtrl + C  
PasteCtrl + V <separator>  
Seleccionar allCtrl + A <separator>  
DeleteDel (normalmente no se proporciona el acceso directo)  
Cambiar el nombre <separator>  
Opciones
</dl> </dd> Page<dl> New windowCtrl + N <separator>  
Zoom  
Tamaño del texto
</dl> </dd> </dl>

**Menús contextuales estándar**

El contenido del menú contextual estándar es el siguiente. En esta lista se muestran las etiquetas de los elementos de menú, su orden con separadores, sus teclas de acceso y sus puntos suspensivos. Los menús contextuales no muestran las teclas de método abreviado.

<dl> Abrir  
Ejecutar  
Reproducir  
Editar  
Imprimir... <separator>  
Cortar  
Copiar  
Copiar <separator>  
Eliminar  
Cambiar el nombre <separator>  
Bloquear <object name> (marca de verificación)  
Propiedades
</dl>

### <a name="using-ellipses"></a>Usar puntos suspensivos

Aunque los comandos de menú se usan para acciones inmediatas, puede que sea necesaria más información para realizar la acción. **Indicar un comando que necesita información adicional (incluida una confirmación) agregando un botón de puntos suspensivos al final de la etiqueta.**

![captura de pantalla del cuadro de diálogo Imprimir comando e imprimir ](images/cmd-menus-image15.png)

En este ejemplo, se imprime... comando muestra un cuadro de diálogo de impresión para recopilar más información.

**El uso correcto de las elipses es importante para indicar que los usuarios pueden tomar más opciones antes de realizar la acción, o incluso cancelar la acción por completo.** La indicación visual ofrecida por un botón de puntos suspensivos permite a los usuarios explorar el software sin miedo.

**Esto no significa que deba usar puntos suspensivos cada vez que una acción muestre otra ventana** solo cuando se requiera información adicional para realizar la acción. Por ejemplo, los comandos acerca de, opciones avanzadas, ayuda, opciones, propiedades y configuración deben mostrar otra ventana al hacer clic en ella, pero no requieren información adicional del usuario. Por lo tanto, no necesitan puntos suspensivos.

**En caso de ambigüedad (por ejemplo, la etiqueta de comando carece de un verbo), decida en función de la acción más probable del usuario.** Si simplemente la ventana es una acción común, no use puntos suspensivos.

**Correcto:**

Más colores...

Información de la versión

En el primer ejemplo, lo más probable es que los usuarios elijan un color, por lo que el uso de puntos suspensivos es correcto. En el segundo ejemplo, lo más probable es que los usuarios vayan a ver la información de la versión, lo que hará que las elipses sean innecesarias.

> [!Note]  
> Al determinar si un comando de menú necesita puntos suspensivos, no use la necesidad de [elevar los privilegios](winenv-uac.md) como un factor.

 

La elevación no es información necesaria para ejecutar un comando (en su lugar, tiene permiso) y la necesidad de elevar se indica con el escudo de seguridad.

## <a name="labels"></a>Etiquetas

-   **Use mayúsculas de estilo de frase.**
    -   **Excepción:** En el caso de las aplicaciones heredadas, puede utilizar el uso de mayúsculas de estilo de título si es necesario para evitar la combinación de estilos de capitalización.

### <a name="menu-category-names"></a>Nombres de categoría de menú

-   **Use nombres de categoría de menú que sean nombres o verbos de palabra única.** Una etiqueta de varias palabras puede confundirse con las etiquetas de 2 1-palabra.
-   **Prefiere nombres de menú basados en verbos.** Sin embargo, omita el verbo si es crear, mostrar, ver o administrar. Por ejemplo, las siguientes categorías de menú no tienen verbos:
    -   Tabla
    -   Herramientas
    -   Periodo
-   En el caso de los nombres de categoría no estándar, **use una sola palabra específica que describa claramente y de forma precisa el contenido del menú.** Aunque los nombres no tienen que ser tan generales que describan todo en el menú, deben ser suficientemente predecibles para que los usuarios no se sorprendan según lo que encuentren en el menú.

### <a name="menu-item-names"></a>Nombres de elementos de menú

-   **Use nombres de elementos de menú que empiecen por un verbo, un nombre o una frase.**
-   **Prefiere nombres de menú basados en verbos.** Sin embargo, omita el verbo si:
    -   **El verbo es crear, mostrar, ver o administrar.** Por ejemplo, los siguientes comandos no tienen verbos:
        -   Acerca de
        -   Avanzado
        -   Pantalla completa
        -   Nuevo
        -   Opciones
        -   Propiedades
    -   **El verbo es el mismo que el nombre de la categoría de menú para evitar la repetición.** Por ejemplo, en la categoría del menú Insertar, use texto, tabla e imagen en lugar de insertar texto, Insertar tabla e insertar imagen.
-   **Usar verbos específicos.** Evite los verbos genéricos no ayudantes, como cambiar y administrar.
-   **Use nombres singulares para los comandos que se aplican a un solo objeto**; de lo contrario, use Sustantivos plurales.
-   **Utilice modificadores según sea necesario para distinguir entre comandos similares.** Ejemplos: Insertar fila arriba, Insertar fila a continuación.
-   **En el caso de los pares de comandos complementarios, elija nombres claramente complementarios.** Ejemplos: agregar, quitar; Mostrar, ocultar; Insertar, eliminar.
-   **Elija los nombres de elemento de menú en función de los objetivos y las tareas del usuario, no de la tecnología.**

**Correcto:**

![captura de pantalla del menú RIP con el elemento de menú formato ](images/cmd-menus-image16.png)

**Incorrecto:**

![captura de pantalla del menú copiar mediante el elemento de menú códec ](images/cmd-menus-image17.png)

En el ejemplo incorrecto, el elemento de menú se basa en su tecnología.

-   Use los siguientes nombres de elemento de menú para el propósito indicado:
    -   **Opciones** de Para mostrar las opciones del programa.
    -   **Personalizar** Para mostrar las opciones del programa relacionadas específicamente con la configuración mecánica de la interfaz de usuario.
    -   **Personalizar** Para mostrar un resumen de la configuración de [Personalización](glossary.md) utilizada comúnmente.
    -   **Preferencias** No use. En su lugar, use las opciones.
    -   **Propiedades** de Para mostrar la ventana de propiedades de un objeto.
    -   **Configuración** de No use como etiqueta de menú. En su lugar, use las opciones.

### <a name="submenu-names"></a>Nombres de submenús

-   **Los elementos de menú que muestran submenús nunca tienen puntos suspensivos en su etiqueta.** La flecha de submenú indica que se requiere otra selección.

**Incorrecto:**

![captura de pantalla del nuevo elemento de menú con puntos suspensivos ](images/cmd-menus-image18.png)

En este ejemplo, el nuevo elemento de menú tiene incorrectamente puntos suspensivos.

## <a name="documentation"></a>Documentación

Al hacer referencia a los menús:

-   En los comandos que muestran u ocultan menús, consulte barras de menús. No se hace referencia a ellos como menús clásicos.
-   Haga referencia a los menús por sus etiquetas. Use el texto de etiqueta exacto, incluido el uso de mayúsculas, pero no incluya el carácter de subrayado o los puntos suspensivos de la tecla de acceso.
-   Para hacer referencia a las categorías de menú, use "en el <category name> menú". Si la ubicación de un elemento de menú está clara en el contexto, no es necesario mencionar la categoría del menú.
-   Para describir la interacción del usuario de los elementos de menú, use hacer clic, sin el menú o comando de Word. No use elegir, seleccionar o seleccionar. No haga referencia a un elemento de menú como un elemento de menú, excepto en la documentación técnica.
-   Para describir la eliminación de una marca de verificación de una opción de menú, use hacer clic para quitar la marca de verificación. No utilice Clear.
-   Haga referencia a los menús contextuales como menús contextuales, no como menús contextuales.
-   No use los menús en cascada, desplegables, desplegables o emergentes para describirlos, excepto en la documentación de programación.
-   Haga referencia a los elementos de menú no disponibles, no como atenuados, deshabilitados o atenuados. Use deshabilitado en la documentación de programación.
-   Siempre que sea posible, dé formato a las etiquetas usando texto en negrita. De lo contrario, coloque las etiquetas entre comillas solo si es necesario para evitar confusiones.

Ejemplos:

-   En el menú **archivo** , haga clic en **Imprimir** para imprimir el documento.
-   En el menú **Ver** , seleccione **barras de herramientas** y, a continuación, haga clic en **formato**.

 

