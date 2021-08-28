---
title: Menús (conceptos básicos de diseño)
description: Los menús son listas jerárquicas de comandos u opciones disponibles para los usuarios en el contexto actual.
ms.assetid: 3772ff8e-8057-476d-b62b-efbd5e07907f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ba8c67716e6b30fcc32651c8932363310926e6bf
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880374"
---
# <a name="menus-design-basics"></a>Menús (conceptos básicos de diseño)

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Los menús son listas jerárquicas de comandos u opciones disponibles para los usuarios en el contexto actual.

Los menús desplegables son menús que se muestran a petición al hacer clic o mantener el mouse sobre ellos. Normalmente se ocultan de la vista y, por tanto, son un medio eficaz de conservar el espacio de pantalla. Un submenú o un menú en cascada es un menú secundario que se muestra a petición desde dentro de un menú. Se indican mediante una flecha al final de la etiqueta de submenú. Un elemento de menú es un comando u opción individual dentro de un menú.

Los menús suelen mostrarse desde una barra de menús, que es una lista de categorías de menú etiquetadas que normalmente se encuentran cerca de la parte superior de una ventana. Por el contrario, un menú contextual se reduce cuando los usuarios hacen clic con el botón derecho en un objeto o región de ventana que admite un menú contextual.

![captura de pantalla de la barra de menús con menú y submenú ](images/cmd-menus-image1.png)

Una barra de menús típica que muestra un menú desplegable y un submenú.

> [!Note]  
> Las instrucciones relacionadas con [los botones de](ctrl-command-buttons.md)comandos, las barras de [herramientas](cmd-toolbars.md)y el [teclado](inter-keyboard.md) se presentan en artículos independientes.

 

## <a name="usage-patterns"></a>Patrones de uso

Los menús tienen varios patrones de uso:



| Uso                                                                                                                                                |    Ejemplo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Barras de menús**<br/> Una barra de menús muestra comandos y opciones en los menús desplegables. <br/>                                               | las barras de menús son muy comunes y fáciles de encontrar, así como un uso eficaz del espacio. <br/> ![captura de pantalla de la barra de menús con menú desplegable ](images/cmd-menus-image2.png)<br/> Una barra de menús de Windows Mail.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Menús de la barra de herramientas**<br/> una barra de menús implementada como barra de herramientas. <br/>                                                                   | Los menús de la barra de herramientas [](ctrl-command-buttons.md) son barras de herramientas que constan principalmente de comandos en botones de menú y botones de división, con solo algunos comandos directos, si los hay. <br/> ![captura de pantalla del menú de la barra de herramientas con el menú desplegable ](images/cmd-menus-image3.png)<br/> Menú de la barra de herramientas Windows Galería de fotos.<br/> Para obtener instrucciones sobre este patrón, vea [Barras de herramientas](cmd-toolbars.md).<br/>                                                                                                                                                                                                             |
| **Menús de pestañas**<br/> botones dentro de pestañas que muestran un pequeño conjunto de comandos y opciones relacionados con una pestaña en un menú desplegable. <br/> | Las pestañas con menús son como pestañas normales, salvo que su parte inferior tiene un botón con flecha desplegable. Al hacer clic en el botón se muestra un menú desplegable en lugar de seleccionar la pestaña. <br/> ![captura de pantalla del menú de pestañas con el menú desplegable ](images/cmd-menus-image4.png)<br/> Los menús de pestañas se usan Reproductor de Windows Media.<br/>                                                                                                                                                                                                                                                                                           |
| **Botones de menú**<br/> botones de comando que muestran un pequeño conjunto de comandos relacionados en un menú desplegable. <br/>                       | [los botones de](ctrl-command-buttons.md) menú se parecen a los botones de comandos normales, salvo que tienen una flecha desplegable dentro de ellos. Al hacer clic en el botón se muestra un menú desplegable en lugar de realizar un comando.<br/> [Los botones de](ctrl-command-buttons.md) división son similares a los botones de menú, salvo que son variaciones de un comando y, al hacer clic en la parte izquierda del botón, se realiza la acción en la etiqueta directamente.<br/> ![captura de pantalla del botón de menú con comandos desplegables ](images/cmd-menus-image5.png)<br/> Botón de menú con un pequeño conjunto de comandos relacionados.<br/> |
| **Menús contextuales**<br/> menús desplegables que muestran un pequeño conjunto de comandos y opciones relacionados con el contexto actual. <br/>       | Menús contextuales desplegables cuando los usuarios hacen clic con el botón derecho en un objeto o región de ventana que admite un menú contextual. <br/> ![captura de pantalla del menú contextual que muestra comandos ](images/cmd-menus-image6.png)<br/> un menú contextual del Explorador de Windows.<br/> Si los menús contextuales son la mejor opción de menú, pero necesita una solución adecuada para todos los usuarios, puede usar un botón de flecha desplegable de menú. <br/> ![captura de pantalla de la foto con el botón de menú desplegable ](images/cmd-menus-image7.png)<br/> Un menú contextual visible con un botón desplegable de menú.<br/>                                                   |
| **Menús del panel de tareas**<br/> un pequeño conjunto de comandos relacionados con el objeto o modo de programa seleccionados. <br/>                              | A diferencia de los menús contextuales, se muestran automáticamente dentro de un panel de ventana, en lugar de a petición. <br/> ![captura de pantalla de la foto con el menú del panel de tareas a la derecha ](images/cmd-menus-image8.png)<br/> Menú del panel de tareas del Windows Galería de fotos usuario.<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

Para decidirte, intenta responder a estas preguntas:

### <a name="menu-bars"></a>Barras de menús

¿Se aplican las condiciones siguientes:

-   ¿La ventana es una ventana principal?
-   ¿Hay muchos elementos de menú?
-   ¿Hay muchas categorías de menú?
-   ¿La mayoría de los elementos de menú se aplican a todo el programa y a la ventana principal?
-   ¿El menú debe funcionar para todos los usuarios?

Si es así, considere la posibilidad de usar una barra de menús.

### <a name="toolbar-menus"></a>Menús de la barra de herramientas

¿Se aplican las condiciones siguientes:

-   ¿La ventana es una ventana principal?
-   ¿La ventana tiene una barra de herramientas?
-   ¿Solo hay algunas categorías de menú?
-   ¿El menú debe funcionar para todos los usuarios?

Si es así, considere la posibilidad de usar un menú de la barra de herramientas en lugar de o además de una barra de menús.

### <a name="tab-menus"></a>Menús de pestañas

¿Se aplican las condiciones siguientes:

-   ¿La ventana es una ventana principal?
-   ¿La ventana tiene pestañas, donde cada pestaña se usa para un conjunto dedicado de tareas (en lugar de usar pestañas para mostrar vistas diferentes)?
-   ¿Hay una categoría de menú que se aplique a cada pestaña?
-   ¿Hay muchos comandos y opciones, pero solo un pequeño conjunto para cada pestaña?

Si es así, considere la posibilidad de usar un menú de pestañas en lugar de una barra de menús.

### <a name="context-menu"></a>Menú contextual

¿Se aplican las condiciones siguientes:

-   ¿Hay un pequeño conjunto de comandos contextuales y opciones que se aplican al objeto o la región de ventana seleccionados?
-   ¿Estos elementos de menú son redundantes?
-   ¿Los usuarios de destino están familiarizados con los menús contextuales?

Si es así, considere la posibilidad de proporcionar menús contextuales para los objetos y regiones de ventana que los necesiten.

En el caso de los programas basados en explorador, los menús del panel de tareas son una solución más común para los comandos contextuales. Actualmente, los usuarios esperan que los menús contextuales de los programas basados en explorador sean genéricos y poco útiles.

### <a name="task-pane-menu"></a>Menú del panel de tareas

¿Se aplican las condiciones siguientes:

-   ¿La ventana es una ventana principal?
-   ¿Hay un pequeño conjunto de comandos contextuales y opciones que se aplican al objeto o modo de programa seleccionado?
-   ¿Hay algunas categorías de menú?
-   ¿El menú debe funcionar para todos los usuarios?

Si es así, considere la posibilidad de usar un menú del panel de tareas en lugar de un menú contextual.

## <a name="design-concepts"></a>Conceptos de diseño

Menús efectivos que promueven una buena experiencia de usuario:

-   Use una presentación de comandos que coincida con el tipo de programa, los tipos de ventana, el uso de comandos y los usuarios de destino.
-   Están bien organizados, usando la organización de menús estándar cuando sea necesario.
-   Use barras de menús, barras de herramientas y menús contextuales de forma eficaz.
-   Use iconos de forma eficaz.
-   Use las teclas de acceso y las teclas de método abreviado de forma eficaz.

**Si solo hace una cosa...**

Elija una presentación de comandos que coincida con el tipo de programa, los tipos de ventana, el uso de comandos y los usuarios de destino.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Todos los patrones de menú, excepto las barras de menú, necesitan una flecha desplegable para indicar la presencia de un menú desplegable.** La presencia de menús no tiene que decirse en una barra de menús, pero no en los demás patrones.
-   **No cambie los nombres de los elementos de menú dinámicamente.** Hacerlo es confuso e inesperado. Por ejemplo, no cambie una opción modo vertical al modo horizontal tras la selección. Para los modos, use [viñetas y marcas de verificación](#bullets-and-checkmarks) en su lugar.
    -   **Excepción:** Puede cambiar dinámicamente los nombres de los elementos de menú basados en nombres de objeto. Por ejemplo, las listas de archivos usados recientemente o nombres de ventana pueden ser dinámicas.

### <a name="menu-bars"></a>Barras de menús

-   **Considere la posibilidad de eliminar las barras de menús con tres o menos categorías de menú.** Si solo hay algunos comandos, prefiera alternativas más ligeras, como los menús de la barra de herramientas, o alternativas más directas, como botones de comandos y vínculos.
-   **No tiene más de 10 categorías de menú.** Demasiadas categorías de menús son abrumadoras y dificultan el uso de la barra de menús.
-   **Considere la posibilidad de ocultar la barra de** menús si la barra de herramientas o los comandos directos proporcionan casi todos los comandos necesarios para la mayoría de los usuarios. Permitir a los usuarios mostrar u ocultar con una opción de marca de verificación barra de menús en un menú de la barra de herramientas.

![captura de pantalla de la lista de opciones con la barra de menús seleccionada ](images/cmd-menus-image9.png)

En este ejemplo, Windows Internet Explorer una opción de barra de menús.

Para obtener más información, vea [Ocultar barras de menú.](#hiding-menu-bars)

### <a name="hiding-menu-bars"></a>Ocultar barras de menús

Por lo general, las barras de herramientas funcionan muy bien junto con las barras de menús, ya que tener ambas permite que cada una se centre en sus puntos fuertes sin poner en peligro.

-   Oculte la barra de menús de forma predeterminada si el diseño de la barra de herramientas hace que tenga una barra de menús redundante.
-   Oculte la barra de menús en lugar de quitarla por completo, ya que las barras de menú son más accesibles para los usuarios del teclado.
-   Para restaurar la barra de menús, proporcione una opción de marca de verificación Barra de menús en la categoría de menú Ver (para barras de herramientas principales) o Herramientas (para barras de herramientas secundarias). Para obtener más información, vea [Menú estándar y Botones de división.](cmd-toolbars.md)

### <a name="menu-categories"></a>Categorías de menú

-   **Elija nombres de palabras únicas para las categorías de menú.** El uso de varias palabras hace que la separación entre categorías sea confusa.
-   **Para los programas que crean o ven documentos, use** las categorías de menú estándar, como Archivo, Edición, Vista, Herramientas y Ayuda. Esto hace que los elementos de menú comunes sean predecibles y fáciles de encontrar.
-   **Para otros tipos** de programas, considere la posibilidad de organizar los comandos y las opciones en categorías naturales más útiles en función del propósito del programa y la forma en que los usuarios piensen en sus tareas y objetivos. No se sienta obligado a usar la organización de menús estándar si no es adecuada para el programa.
-   **Si decide usar categorías de menú no estándar, debe elegir buenos nombres de categoría.** Para obtener más información, vea la [sección Etiquetas.](#labels)
-   **Prefiere categorías de menú orientadas a tareas en lugar de categorías genéricas.** Las categorías orientadas a tareas facilitan la búsqueda de elementos de menú.

![captura de pantalla de la barra de menús con desgarr, grabación y sincronización ](images/cmd-menus-image10.png)

En este ejemplo, Reproductor de Windows Media categorías de menú orientadas a tareas.

-   **Evite las categorías de menú con solo uno o dos elementos de menú.** Si es razonable, consolide con otras categorías de menú, quizás mediante un submenú.
-   **Considere la posibilidad de colocar el mismo elemento de menú en varias categorías solo si:**
    -   El elemento de menú pertenece lógicamente a varias categorías de menú.
    -   Tiene datos que muestran que los usuarios tienen problemas para encontrar el elemento en una sola categoría de menú.
    -   Solo tiene uno o dos elementos de menú difíciles de encontrar en varias categorías.
-   **No coloque elementos de menú diferentes que usen el mismo nombre en varias categorías.** Por ejemplo, no tiene elementos de menú Opciones diferentes en varias categorías.
    -   **Excepción:** El patrón de menú de pestañas puede tener diferentes opciones y elementos de menú Ayuda en cada menú de pestaña.

![captura de pantalla de menús de pestañas con elementos de menú repetidos ](images/cmd-menus-image11.png)

En este ejemplo, Reproductor de Windows Media elementos de menú Opciones y Ayuda en cada menú de pestañas.

### <a name="menu-item-organization-and-order"></a>Organización y pedido de elementos de menú

-   **Organice los elementos de menú en grupos de siete o menos elementos fuertemente relacionados.** Para ello, los submenús cuentan como un único elemento de menú en el menú primario.
-   **No coloque más de 25** elementos en un solo nivel de un menú (sin contar submenús).
-   **Coloque separadores entre los grupos dentro de un menú.** Un separador es una sola línea que abarca el ancho del menú.
-   **Dentro de un menú, coloque los grupos en su orden lógico.** Si no hay ningún orden lógico, coloque primero los grupos más usados.
-   **Dentro de un grupo, coloque los elementos en su orden lógico.** Si no hay ningún orden lógico, coloque primero los elementos más usados. Coloque los elementos numéricos (como los porcentajes de zoom) en orden numérico.

### <a name="submenus"></a>Submenus

-   **Evite usar submenús innecesariamente.** Los submenús requieren más esfuerzo físico y, por lo general, dificultan la búsqueda de los elementos de menú.
-   **No coloque elementos de menú usados con frecuencia en un submenú.** Si lo hace, el uso de estos comandos sería ineficaz. Sin embargo, puede colocar comandos usados con frecuencia en un submenú si normalmente se accede a ellos más directamente, como con una barra de herramientas.
-   **Considere la posibilidad de usar un submenú si:**
    -   Esto simplifica el menú primario porque tiene muchos elementos (20 o más) o el submenú forma parte de un grupo de más de siete elementos.
    -   Los elementos del submenú se usan con menos frecuencia que los del menú primario.
    -   El submenú tendría tres o más elementos.
    -   Hay tres o más comandos que comienzan con la misma palabra. En este caso, use esa palabra como etiqueta de submenú.

![captura de pantalla del menú "nuevo" con cuatro elementos de submenú ](images/cmd-menus-image12.png)

En este ejemplo, el submenú Nuevo reemplaza comandos independientes para Nuevo mensaje de correo, Nuevo mensaje de noticias, Nueva carpeta y Nuevo contacto.

-   **Use como máximo tres niveles de menús.** Es decir, puede tener un menú principal y, como máximo, dos niveles de submenús. Dos niveles de submenús deben ser poco frecuentes.

### <a name="presentation"></a>Presentación

-   **Deshabilite los elementos de menú que no se aplican al contexto actual,** en lugar de quitarlos. Esto hace que el contenido de la barra de menús sea estable y fácil de encontrar. **Excepciones:**
    -   Para las categorías de menú contextual, quite en lugar de deshabilitar los elementos de menú contextual que **no se aplican al contexto actual.** Una categoría de menú es contextual cuando solo se muestra para modos específicos, como cuando se selecciona un tipo de objeto determinado. Para más información, consulte las directrices [de eliminación frente a deshabilitación](#context-menus) de menús contextuales.
    -   Si determinar cuándo se debe deshabilitar un elemento de menú provoca problemas de rendimiento perceptibles, deje el elemento de menú activo y, si es necesario, haga que su selección dé como resultado un mensaje de error.

### <a name="tab-menus"></a>Menús de pestañas

-   **Cada menú de pestaña puede tener opciones específicas del contexto y elementos de menú Ayuda.** Esto contrasta con todos los demás patrones de menú. Cada pestaña se usa para un conjunto dedicado de tareas, por lo que cualquier redundancia en los menús de pestaña no es confusa.

### <a name="context-menus"></a>Menús contextuales

-   **Use menús contextuales solo para comandos y opciones contextuales.** Los elementos de menú solo se deben aplicar al objeto o la región de ventana seleccionados (o en los que se ha hecho clic en él), no a todo el programa.
-   **No haga que los comandos solo estén disponibles a través de menús contextuales.** Al igual que las teclas de método abreviado, los menús contextuales son medios alternativos para realizar comandos y elegir opciones. Por ejemplo, un comando Propiedades también está disponible a través de la barra de menús o la tecla de acceso Alt+Entrar.
-   **Proporcione menús contextuales para todos los objetos y regiones de ventana** que se benefician de un pequeño conjunto de comandos y opciones contextuales. Muchos usuarios hacen clic con el botón derecho con regularidad y esperan encontrar menús contextuales en cualquier lugar.
-   **Considere la posibilidad de usar un botón de flecha desplegable de menú para menús contextuales dirigidos a todos los usuarios.** Normalmente, los menús contextuales son adecuados para comandos y opciones destinados a usuarios avanzados. Sin embargo, puede usar un botón desplegable de menú en casos en los que los menús contextuales sean la mejor opción de menú y tenga que dirigirse a todos los usuarios.

![captura de pantalla de la foto con el botón de menú desplegable ](images/cmd-menus-image7.png)

En este ejemplo, se usa un botón desplegable de menú para que un menú contextual esté visible.

**Organización y pedido de elementos de menú**

-   **Organice los elementos de menú en grupos de siete o menos elementos fuertemente relacionados.**
-   **Evite usar submenús para** mantener los menús contextuales simples, directos y eficaces.
-   **No coloque más de 15 elementos en un menú contextual.**
-   **Coloque separadores entre los grupos dentro de un menú.** Un separador es una sola línea que abarca el ancho del menú.
-   **Presente los elementos de menú con el orden siguiente:**

<dl> Comandos principales (usados con más frecuencia)<dl> Abrir  
Ejecutar  
Reproducir  
Impresión  
&lt;separator&gt;  
</dl> </dd> <dd>Comandos secundarios admitidos por el objeto<dl> &lt;separator&gt;  
</dl> </dd> Transferir comandos<dl> Cortar  
Copiar  
Pegar  
&lt;separator&gt;  
</dl> </dd> <dd>Configuración de objetos<dl> &lt;separator&gt;  
</dl> </dd> Comandos de objeto<dl> Eliminar  
Cambiar nombre  
&lt;separator&gt;  
Propiedades  
</dl> </dd> </dl>

**Presentación**

-   **Muestre el comando predeterminado mediante negrita.** Cuando sea práctico, conséctese también por el primer elemento de menú. El comando predeterminado se invoca cuando los usuarios hacen doble clic o seleccionan un objeto y presionan Entrar.
-   **Quite en lugar de deshabilitar los elementos de menú contextual que no se aplican al contexto actual.** Al hacerlo, los menús contextuales son contextuales y eficaces.
    -   **Excepción:** Deshabilite los elementos de menú que no se aplican si hay una expectativa razonable de que estén disponibles:
        -   Tenga siempre los comandos de menú contextual estándar pertinentes, como Cortar, Copiar, Pegar, Eliminar y Cambiar nombre.
        -   Tenga siempre los comandos que completan conjuntos relacionados. Por ejemplo, si hay un back, también debe haber un reenvío. Si hay un corte, siempre tiene una opción Copiar y pegar.

### <a name="bullets-and-checkmarks"></a>Viñetas y marcas de verificación

-   **Los elementos de menú que son opciones pueden usar viñetas y marcas de verificación.** Es posible que los comandos no.
-   **Use una viñeta para elegir una opción de un pequeño conjunto de opciones mutuamente excluyentes.** Siempre debe haber al menos dos viñetas en un grupo. Para obtener más información, vea [Botones de radio](ctrl-radio-buttons.md).
-   **Use una marca de verificación para activar o desactivar una configuración independiente.** Si los estados seleccionados y borrados no son opuestos claros e inequívocos, use un conjunto de viñetas en su lugar. Para obtener más información, vea [Casillas](ctrl-check-boxes.md).
-   **Para un estado de marca de verificación mixta, muestre un elemento de menú sin marca de verificación.** El estado mixto se usa para la selección múltiple para indicar que la opción está establecida para algunos objetos, pero no para todos, por lo que cada objeto individual tiene el estado seleccionado o borrado. El estado mixto no se usa como tercer estado para un elemento individual.
-   **Coloque separadores entre los conjuntos relacionados de marcas de verificación o viñetas.** Un separador es una sola línea que abarca el ancho del menú.

### <a name="icons"></a>Iconos

-   **Considera la posibilidad de proporcionar iconos de elemento de menú para:**
    -   Los elementos de menú más usados.
    -   Elementos de menú cuyo icono es estándar y conocido.
    -   Elementos de menú cuyo icono muestra bien lo que hace el comando.
-   **Si usa iconos, no se sienta obligado a proporcionarlos para todos los elementos de menú.** Los iconos crípticos no son útiles, provocan una aglutinación visual y evitan que los usuarios se centren en los elementos de menú importantes.

![captura de pantalla de elementos de menú con y sin iconos ](images/cmd-menus-image13.png)

En este ejemplo, el menú Organizar solo tiene iconos para los elementos de menú más usados.

-   **Asegúrese de que los iconos de menú se ajustan a las directrices de icono de estilo Avión.**

Para obtener más información y ejemplos, vea [Iconos](vis-icons.md).

### <a name="access-keys"></a>Claves de acceso

-   **Asigne claves de acceso a todos los elementos de menú.** Ninguna excepción.
-   **Siempre que sea posible, asigne claves de acceso para los comandos usados habitualmente según las asignaciones de claves de acceso estándar.** Aunque las asignaciones de claves de acceso coherentes no siempre son posibles, ciertamente se prefieren, especialmente para los comandos usados con frecuencia.
-   **Para los elementos de menú dinámicos (por ejemplo, los archivos usados recientemente), asigne claves de acceso numéricamente.**

![captura de pantalla de elementos de menú con claves de acceso numéricas ](images/cmd-menus-image14.png)

En este ejemplo, el programa Paint en Windows asigna claves de acceso numéricas a los archivos usados recientemente.

-   **Asigne claves de acceso únicas dentro de un nivel de menú.** Puede reutilizar las claves de acceso en distintos niveles de menú.
-   **Facilitar la tarea de encontrar las claves de acceso:**
    -   Para los elementos de menú usados con más frecuencia, elija caracteres al principio de la primera o segunda palabra de la etiqueta, preferiblemente el primer carácter.
    -   Para los elementos de menú usados con menos frecuencia, elija letras que sean una consonante distintiva o una voz en la etiqueta.
-   **Prefiere caracteres con anchos anchos anchos,** como w, m y letras mayúsculas.
-   **Prefiere una consonante distintiva o una voto,** como "x" en "Exit".
-   **Evite usar caracteres que hagan que el subrayado** sea difícil de ver, como (de más problemático a menos problemático):
    -   Letras que tienen solo un píxel de ancho, como i y l.
    -   Letras con descendientes, como g, j, p, q e y.
    -   Letras junto a una letra con un descendiente.

Para obtener más instrucciones y ejemplos, vea [Teclado](inter-keyboard.md).

### <a name="shortcut-keys"></a>Teclas de método abreviado

-   **Asigne teclas de método abreviado a los elementos de menú usados con más frecuencia.** Los elementos de menú usados con poca frecuencia no necesitan teclas de método abreviado porque los usuarios pueden usar claves de acceso en su lugar.
-   **No haga que una tecla de método abreviado sea la única manera de realizar una tarea.** Los usuarios también deben poder usar el mouse o el teclado con teclas de tabulación, flecha y acceso.
-   **Para las teclas de método abreviado conocidas, use las asignaciones estándar.**
-   **No asigne significados diferentes a teclas de método abreviado conocidas.** Dado que se memorizan, los significados incoherentes de los accesos directos conocidos son frustrantes y propensos a errores. Consulte Windows teclas de método abreviado de teclado para conocer las teclas de método abreviado conocidas que usan Windows programas.
-   **No intente asignar teclas de método abreviado de programa para todo el sistema.** Las teclas de método abreviado del programa solo tendrán efecto cuando el programa tenga el foco de entrada.
-   **Documente todas las teclas de método abreviado.** Esto ayuda a los usuarios a aprender las asignaciones de teclas de método abreviado.
    -   **Excepción:** No muestre asignaciones de teclas de método abreviado en los menús contextuales. Los menús contextuales no muestran las asignaciones de teclas de método abreviado porque están optimizadas para mejorar la eficacia.
-   **Para asignaciones de claves no estándar:**
    -   **Elija teclas de método abreviado que no tengan asignaciones estándar.** Nunca vuelva a asignar las teclas de método abreviado estándar.
    -   **Use asignaciones de claves no estándar de forma coherente en todo el programa.** No asigne significados diferentes en ventanas diferentes.
    -   **Si es posible, elija asignaciones de claves mnemotécnicas,** especialmente para los comandos usados con frecuencia.
    -   **Use claves de función para los comandos que tienen** un efecto a pequeña escala, como los comandos que se aplican al objeto seleccionado. Por ejemplo, F2 cambia el nombre del elemento seleccionado.
    -   **Use combinaciones de teclas Ctrl para los** comandos que tienen un efecto a gran escala, como los comandos que se aplican a todo un documento. Por ejemplo, Ctrl+S guarda el documento actual.
    -   **Use combinaciones de teclas Mayús para los comandos que amplían o complementan las acciones de la tecla de método abreviado estándar.** Por ejemplo, la tecla de método abreviado Alt+Tab se desplaza por ventanas principales abiertas, mientras que Alt+Mayús+Tab se desplaza en orden inverso. De forma similar, F1 muestra Ayuda, mientras que Mayús+F1 muestra ayuda contextual.
    -   **No use los caracteres siguientes para las teclas de** método abreviado: @ $ {} \[ \] \\  ~  \| ^ " < >. Estos caracteres requieren combinaciones de teclas diferentes entre idiomas o son específicos de la configuración regional.
    -   **No use combinaciones Ctrl+Alt,** ya que Windows interpreta esta combinación en algunas versiones de lenguaje como una tecla AltGR, que genera caracteres alfanuméricos.
-   **Si el programa asigna muchas teclas de método abreviado, proporcione la capacidad de personalizar las asignaciones.** Esto permite a los usuarios reasignar las teclas de método abreviado en conflicto y migrar desde otros productos. La mayoría de los programas no asignan suficientes teclas de método abreviado para necesitar esta característica.

Para obtener más instrucciones y asignaciones de teclas de método abreviado estándar, vea [Teclado.](inter-keyboard.md)

### <a name="standard-menus"></a>Menús estándar

-   **Use la organización de menús estándar para los programas que crean o ven documentos.** La organización de menús estándar hace que los elementos de menú comunes sean predecibles y fáciles de encontrar.
-   **Para otros tipos de programas, use la organización de menús estándar solo cuando tenga sentido.** Considere la posibilidad de organizar los comandos y las opciones en categorías más útiles y naturales en función del propósito del programa y de la manera en que los usuarios piensen en sus tareas y objetivos.

**Barras de menú estándar**

La estructura de la barra de menús estándar es la siguiente. Esta lista muestra la categoría de menú y las etiquetas de elemento, su orden con separadores, sus teclas de acceso y método abreviado y sus puntos suspensivos.

<dl> Archivo<dl> Nuevo Ctrl+N  
Abierto... Ctrl+O  
Cerrar  
&lt;separator&gt;  
Guardar Ctrl+S  
Guardar como...  
&lt;separator&gt;  
Enviar a  
&lt;separator&gt;  
Impresión... Ctrl+P  
Vista previa de impresión  
Configurar página  
&lt;separator&gt;  
1 <filename> 2 <filename> 3 <filename> ...  
&lt;separator&gt;  
Salir de Alt+F4 (acceso directo normalmente no dado)
</dl> </dd> Edit<dl> Deshacer Ctrl+Z  
Rehacer Ctrl+Y  
&lt;separator&gt;  
Cortar Ctrl+X  
Copiar Ctrl+C  
Pegar Ctrl+V  
&lt;separator&gt;  
Seleccionar todas las teclas Ctrl+A  
&lt;separator&gt;  
Eliminar Supr (acceso directo normalmente no dado)  
&lt;separator&gt;  
Encontrar... Ctrl+F  
Buscar el siguiente F3 (el comando normalmente no se ha dado)  
Reemplazar... Ctrl+H  
Vete a... Ctrl+G
</dl> </dd> View<dl> Barras de herramientas  
Barra de estado  
&lt;separator&gt;
</dl> </dd> Zoom<dl> Acercar Ctrl++  
Alejar Ctrl+-  
&lt;separator&gt;  
Pantalla completa F11  
Actualizar F5
</dl> </dd> <dd>Herramientas<dl> ...  
&lt;separator&gt;  
Opciones
</dl> </dd> Ayuda<dl> <program name> ayuda F1  
&lt;separator&gt;  
Acerca de <program name>  
</dl> </dd> </dl>

**Botones de menú de la barra de herramientas estándar**

Los botones de menú de la barra de herramientas estándar son los siguientes. Esta lista muestra la categoría de menú y las etiquetas de elemento, su orden con separadores, sus teclas de método abreviado y sus puntos suspensivos.

<dl> Herramientas<dl> Pantalla completaF11(Reasignar clave de acceso si también se usa Buscar).  
Barras de herramientas (tenga en cuenta que el comando barra de menús va aquí).  
&lt;separator&gt;  
Imprimir...  
Buscar...  
&lt;separator&gt;  
Zoom  
Tamaño del texto  
&lt;separator&gt;  
Opciones  
</dl> </dd> Organize<dl> Nueva carpetaCtrl+N  
&lt;separator&gt;  
CutCtrl+X  
CopyCtrl+C  
PasteCtrl+V  
&lt;separator&gt;  
Seleccionar todoCtrl+A  
&lt;separator&gt;  
DeleteDel(acceso directo normalmente no dado)  
Cambiar nombre  
&lt;separator&gt;  
Opciones  
</dl> </dd> Page<dl> Nueva ventanaCtrl+N  
&lt;separator&gt;  
Zoom  
Tamaño del texto  
</dl> </dd> </dl>

**Menús contextuales estándar**

El contenido del menú contextual estándar es el siguiente. En esta lista se muestran las etiquetas de los elementos de menú, su orden con separadores, sus claves de acceso y sus puntos suspensivos. Los menús contextuales no muestran las teclas de método abreviado.

<dl> Abrir  
Ejecutar  
Reproducir  
Editar  
Imprimir...  
&lt;separator&gt;  
Cortar  
Copiar  
Pegar  
&lt;separator&gt;  
Eliminar  
Cambiar nombre  
&lt;separator&gt;  
Bloquear <object name> (marca de verificación)  
Propiedades
</dl>

### <a name="using-ellipses"></a>Uso de puntos suspensivos

Aunque los comandos de menú se usan para acciones inmediatas, es posible que se necesite más información para realizar la acción. **Indique un comando que necesita información adicional (incluida una confirmación) agregando puntos suspensivos al final de la etiqueta.**

![captura de pantalla del comando de impresión y el cuadro de diálogo imprimir ](images/cmd-menus-image15.png)

En este ejemplo, imprimir... El comando muestra un cuadro de diálogo Imprimir para recopilar más información.

**El uso adecuado de puntos suspensivos es importante para indicar que los usuarios pueden tomar más decisiones antes de realizar la acción o incluso cancelar la acción por completo.** La indicación visual que ofrece un botón de puntos suspensivos permite a los usuarios explorar el software sin miedo.

**Esto no significa que deba usar** puntos suspensivos cada vez que una acción muestre otra ventana solo cuando se requiera información adicional para realizar la acción. Por ejemplo, los comandos Acerca de, Avanzado, Ayuda, Opciones, Propiedades y Configuración deben mostrar otra ventana cuando se hace clic en ella, pero no requieren información adicional del usuario. Por lo tanto, no necesitan puntos suspensivos.

**En caso de ambigüedad (por ejemplo, la etiqueta de comando no tiene un verbo), decida en función de la acción del usuario más probable.** Si simplemente ver la ventana es una acción común, no use puntos suspensivos.

**Correcto:**

Más colores...

Información de la versión

En el primer ejemplo, lo más probable es que los usuarios elijan un color, por lo que el uso de puntos suspensivos es correcto. En el segundo ejemplo, lo más probable es que los usuarios van a ver la información de la versión, lo que hace que los puntos suspensivos sean innecesarios.

> [!Note]  
> Al determinar si un comando de menú necesita puntos [suspensivos,](winenv-uac.md) no use la necesidad de elevar los privilegios como un factor.

 

La elevación no es información necesaria para realizar un comando (en su lugar, es para el permiso) y la necesidad de elevarse se indica con el escudo de seguridad.

## <a name="labels"></a>Etiquetas

-   **Use mayúsculas de estilo de frase.**
    -   **Excepción:** En el caso de las aplicaciones heredadas, puede usar mayúsculas de estilo de título si es necesario para evitar mezclar estilos de mayúsculas.

### <a name="menu-category-names"></a>Nombres de categoría de menú

-   **Use nombres de categoría de menú que sean verbos o sustantivos de una sola palabra.** Una etiqueta de varias palabras puede confundirse con dos etiquetas de una sola palabra.
-   **Prefiere nombres de menú basados en verbos.** Sin embargo, omita el verbo si es Crear, Mostrar, Ver o Administrar. Por ejemplo, las siguientes categorías de menú no tienen verbos:
    -   Tabla
    -   Herramientas
    -   Periodo
-   Para los nombres de categoría no estándar, use una sola palabra específica que describa de forma clara y precisa el **contenido del menú.** Aunque los nombres no tienen que ser tan generales que describan todo en el menú, deben ser lo suficientemente predecibles para que los usuarios no se sorprendan por lo que encuentran en el menú.

### <a name="menu-item-names"></a>Nombres de elementos de menú

-   **Use nombres de elementos de menú que empiecen por un verbo, un sustantivo o una frase de sustantivo.**
-   **Prefiere nombres de menú basados en verbos.** Sin embargo, omita el verbo si:
    -   **El verbo es Crear, Mostrar, Ver o Administrar.** Por ejemplo, los siguientes comandos no tienen verbos:
        -   Acerca de
        -   Avanzado
        -   Pantalla completa
        -   Nuevo
        -   Opciones
        -   Propiedades
    -   **El verbo es el mismo que el nombre de la categoría de menú para evitar la repetición.** Por ejemplo, en la categoría de menú Insertar, use Texto, Tabla e Imagen en lugar de Insertar texto, Insertar tabla e Insertar imagen.
-   **Use verbos específicos.** Evite verbos genéricos y poco útiles, como Cambiar y administrar.
-   **Use nombres singulares para los comandos que se aplican a un solo objeto**; de lo contrario, use nombres plurales.
-   **Use modificadores según sea necesario para distinguir entre comandos similares.** Ejemplos: Insertar fila anterior, Insertar fila a continuación.
-   **Para los pares de comandos complementarios, elija nombres claramente complementarios.** Ejemplos: Agregar, Quitar; Mostrar, Ocultar; Insertar, Eliminar.
-   **Elija los nombres de los elementos de menú en función de los objetivos y las tareas del usuario, no de la tecnología.**

**Correcto:**

![captura de pantalla del menú Desgarrar con el elemento de menú formato ](images/cmd-menus-image16.png)

**Incorrecto:**

![captura de pantalla del menú Desgarrar con el elemento de menú códec ](images/cmd-menus-image17.png)

En el ejemplo incorrecto, el elemento de menú se basa en su tecnología.

-   Use los siguientes nombres de elemento de menú para el propósito indicado:
    -   **Opciones** Para mostrar las opciones del programa.
    -   **Personalizar** Para mostrar las opciones del programa relacionadas específicamente con la configuración mecánica de la interfaz de usuario.
    -   **Personalizar** Para mostrar un resumen de la configuración de [personalización que se usa con](glossary.md) frecuencia.
    -   **Preferencias** No lo use. En su lugar, use Opciones.
    -   **Propiedades** Para mostrar la ventana de propiedades de un objeto.
    -   **Configuración** No use como etiqueta de menú. En su lugar, use Opciones.

### <a name="submenu-names"></a>Nombres de submenú

-   **Los elementos de menú que muestran submenús nunca tienen puntos suspensivos en su etiqueta.** La flecha de submenú indica que se requiere otra selección.

**Incorrecto:**

![captura de pantalla del nuevo elemento de menú con puntos suspensivos ](images/cmd-menus-image18.png)

En este ejemplo, el elemento de menú Nuevo tiene puntos suspensivos incorrectamente.

## <a name="documentation"></a>Documentación

Al hacer referencia a menús:

-   En los comandos que muestran u ocultan menús, consulte barras de menús. No haga referencia a ellos como menús clásicos.
-   Consulte los menús por sus etiquetas. Use el texto exacto de la etiqueta, incluida su inclusión en mayúsculas, pero no incluya el carácter de subrayado ni los puntos suspensivos de la clave de acceso.
-   Para hacer referencia a las categorías de menú, use "En el <category name> menú". Si la ubicación de un elemento de menú no está clara en el contexto, no es necesario mencionar la categoría de menú.
-   Para describir la interacción del usuario de los elementos de menú, use clic, sin el menú de palabras o el comando . No use choose, select ni pick. No haga referencia a un elemento de menú como elemento de menú, excepto en la documentación técnica.
-   Para describir cómo quitar una marca de verificación de una opción de menú, use haga clic para quitar la marca de verificación. No use clear.
-   Consulte los menús contextuales como menús contextuales, no como menús contextuales.
-   No use menús en cascada, desplegables, desplegables o emergentes para describir los menús, excepto en la documentación de programación.
-   Consulte elementos de menú no disponibles como no disponibles, no como atenuados, deshabilitados o atenuados. Use deshabilitado en la documentación de programación.
-   Cuando sea posible, formatee las etiquetas con texto en negrita. De lo contrario, coloque las etiquetas entre comillas solo si es necesario para evitar confusiones.

Ejemplos:

-   En el **menú Archivo** , haga clic **en Imprimir** para imprimir el documento.
-   En el **menú Ver** , seleccione Barras **de herramientas** y, a continuación, haga clic **en Formato.**

 

