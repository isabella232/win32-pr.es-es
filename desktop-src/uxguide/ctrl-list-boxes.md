---
title: Cuadros de lista
description: Con un cuadro de lista, los usuarios pueden seleccionar entre un conjunto de valores presentados en una lista que siempre está visible.
ms.assetid: 620e9ff9-b367-446b-9e97-9c9d6d14f4bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0f1fe5a0c804e1c0b5b2636b4c7747caa9fb1049
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986908"
---
# <a name="list-boxes"></a>Cuadros de lista

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Con un cuadro de lista, los usuarios pueden seleccionar entre un conjunto de valores presentados en una lista que siempre está visible. Con un cuadro de lista de selección única, los usuarios seleccionan un elemento de una lista de valores mutuamente excluyentes. Con un cuadro de lista de selección múltiple, los usuarios seleccionan cero o más elementos de una lista de valores.

![captura de pantalla del cuadro de lista de selección única ](images/ctrl-list-boxes-image1.png)

Un cuadro de lista típico de selección única.

> [!Note]  
> Las directrices relacionadas [con las vistas](vis-layout.md) de diseño y [lista](ctrl-list-views.md) se presentan en artículos independientes.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿La lista presenta datos, en lugar de opciones de programa?** En cualquier caso, un cuadro de lista es una opción adecuada independientemente del número de elementos. Por el contrario, [los botones de radio](ctrl-radio-buttons.md) o las [casillas](ctrl-check-boxes.md) solo son adecuados para un número reducido de opciones de programa.
-   **¿Necesitan los usuarios cambiar las vistas, agrupar, ordenar por columnas o cambiar el ancho y el orden de las columnas?** Si es así, use una [vista de lista](ctrl-list-views.md) en su lugar.
-   **¿El control debe ser un origen de arrastre o un destino de colocación?** Si es así, use una vista de lista en su lugar.
-   **¿Es necesario copiar o pegar los elementos de lista en el Portapapeles?** Si es así, use una vista de lista en su lugar.

**Listas de selección única**

-   **¿Se usa el control para elegir una opción de una lista de valores mutuamente excluyentes?** Si no es así, usa otro control. Para elegir varias opciones, use una lista estándar de selección múltiple, una lista de casillas, un generador de listas o agregar o quitar lista en su lugar.
-   **¿Hay una opción predeterminada que se recomienda para la mayoría de los usuarios en la mayoría de las situaciones?** ¿Es mucho más importante ver la opción seleccionada que ver las alternativas? Si es así, considere la posibilidad de usar una lista desplegable si no desea animar [a](/windows/desktop/uxguide/ctrl-drop) los usuarios a realizar cambios ocultando las alternativas.

![captura de pantalla de la máxima calidad como botón predeterminado ](images/ctrl-list-boxes-image2.png)

En este ejemplo, la calidad de color más alta es la mejor opción para la mayoría de los usuarios, por lo que una lista desplegable es una buena opción para bajar las alternativas.

-   **¿Requiere la lista interacción constante?** Si es así, use una lista de selección única para simplificar la interacción.

![captura de pantalla de la lista de opciones, como texto sin formato ](images/ctrl-list-boxes-image3.png)

En este ejemplo, los usuarios cambian constantemente el elemento seleccionado en la lista Mostrar elementos para establecer los colores de primer plano y de fondo. El uso de una lista desplegable en este caso sería muy tedioso.

-   **¿La configuración parece una cantidad relativa? ¿Se beneficiarían los usuarios de comentarios instantáneos** sobre el efecto de establecer los cambios? Si es así, considere la posibilidad de usar [un control deslizante](ctrl-sliders.md) en su lugar.
-   **¿Hay una relación jerárquica significativa entre los elementos de lista?** Si es así, use en su lugar un control [de vista de](ctrl-tree-views.md) árbol.
-   **¿El espacio de pantalla es premium?** Si es así, use una lista desplegable en su lugar porque el espacio de pantalla utilizado es fijo e independiente del número de elementos de lista.

**Listas estándar de selección múltiple y listas de casillas**

-   **¿La selección múltiple es esencial para la tarea o se usa con frecuencia?** Si es así, use una lista de casillas para que la selección múltiple sea obvia, especialmente si los usuarios de destino no están avanzados. Muchos usuarios no se darán cuenta de que una lista estándar de selección múltiple admite la selección múltiple. Use una lista estándar de selección múltiple si las casillas llamarían demasiada atención a la selección múltiple o provocaría demasiado desorden en la pantalla.
-   **¿Es importante la estabilidad de la selección múltiple?** Si es así, use una lista de casillas, un generador de listas o una lista de agregar o quitar porque al hacer clic solo cambia un elemento a la vez. Con una lista de selección múltiple estándar, es muy fácil borrar todas las selecciones incluso por accidente.
-   **¿Se usa el control para elegir cero o más elementos de una lista de valores?** Si no es así, usa otro control. Para elegir un elemento, use en su lugar una lista de selección única.

**Listas de versión preliminar**

-   **¿Las opciones son más fáciles de seleccionar con imágenes que con texto solo?** Si es así, use una lista de vista previa.

**Generadores de listas y agregar o quitar listas**

-   **¿Se usa el control para elegir cero o más elementos de una lista de valores?** Si no es así, usa otro control. Para elegir un elemento, use en su lugar una lista de selección única.
-   **¿Importa el orden de los elementos seleccionados?** Si es así, el generador de listas y los patrones de agregar o quitar listas admiten el orden, mientras que los demás patrones de selección múltiple no lo hacen.
-   **¿Es importante que los usuarios vean un resumen de todos los elementos seleccionados?** Si es así, el generador de listas y los patrones de lista agregar o quitar solo muestran los elementos seleccionados, mientras que los demás patrones de selección múltiple no.
-   **¿Las opciones posibles no están entrenadas?** Si es así, use una lista de agregar o quitar para que los usuarios puedan elegir valores que no están actualmente en la lista.
-   **¿La adición de un valor a la lista requiere un cuadro de diálogo especializado para elegir objetos?** Si es así, use una lista agregar o quitar y mostrar el cuadro de diálogo cuando los usuarios hacen clic en Agregar.
-   **¿El espacio de pantalla es premium?** Si es así, use una lista de agregar o quitar en su lugar porque usa menos espacio en la pantalla al no mostrar siempre el conjunto de opciones.

Para los cuadros de lista, el número de elementos de la lista no es un **factor a** la hora de elegir el control porque escalan desde miles de elementos hasta uno para las listas de selección única (y ninguno para las listas de selección múltiple). Dado que los cuadros de lista se pueden usar para los datos, es posible que el número de elementos no se conozca de antemano.

**Nota:** A veces, un control que parece un cuadro de lista se implementa mediante una vista de lista y viceversa. En tales casos, aplique las directrices en función del uso, no de la implementación.

## <a name="usage-patterns"></a>Patrones de uso

Los cuadros de lista tienen varios patrones de uso:




| Etiqueta | Value |
|--------|-------|
| <strong>Listas de selección única</strong> Permitir que los usuarios seleccionen un elemento a la vez. <br /> | <img src="images/ctrl-list-boxes-image4.png" alt="Screen shot of list box with one item selected " /><br /> En este ejemplo, los usuarios solo pueden seleccionar un elemento para mostrar.<br /> | 
| <strong>Listas estándar de selección múltiple</strong> Permitir a los usuarios seleccionar cualquier número de elementos, incluido ninguno.<br /> | Las listas de selección múltiple estándar tienen exactamente la misma apariencia que las listas de selección única, por lo que no hay ninguna pista visual de que un cuadro de lista admita la selección múltiple. Dado que los usuarios tienen que detectar esta capacidad, este patrón de lista se usa mejor para las tareas en las que la selección múltiple no es esencial y rara vez se usa. <br /> Hay dos modos de selección múltiple diferentes: <a href="glossary.md">varios</a> y <a href="glossary.md">extendidos.</a> <strong>El modo</strong> de selección extendida es con diferencia el más común, donde la selección se puede extender arrastrando o con Mayús+clic y Ctrl+clic para seleccionar grupos de valores contiguos y no adyacentes, respectivamente. En el <strong>modo de selección múltiple</strong>, al hacer clic en cualquier elemento se alterna su estado de selección independientemente de las teclas Mayús y Ctrl. Dado este comportamiento inusual, el modo de selección múltiple está en desuso y debe usar listas de casillas en su lugar.<br /><img src="images/ctrl-list-boxes-image5.png" alt="Screen shot of list box with several items selected " /><br /> En este ejemplo, los usuarios pueden seleccionar cualquier número de elementos mediante el modo de selección múltiple.<br /> | 
| <strong>Listas de casillas</strong> Al igual que las casillas de lista estándar de selección múltiple, las listas de casillas permiten a los usuarios seleccionar cualquier número de elementos, incluido ninguno.<br /> | A diferencia de las listas estándar de selección múltiple, las casillas indican claramente que es posible realizar una selección múltiple. Use este patrón de lista para las tareas en las que la selección múltiple es esencial o se usa habitualmente. <br /><img src="images/ctrl-list-boxes-image6.png" alt="Screen shot of Toolbars check-box list " /><br /> En este ejemplo, los usuarios suelen seleccionar más de un elemento para que se utilice una lista de casillas.<br /> Dada esta indicación clara de la selección múltiple, puede suponer que las listas de casillas son preferibles a las listas estándar de selección múltiple. En la práctica, algunas tareas requieren una selección múltiple o la usan en gran medida. el uso de una lista de casillas en tales casos llama demasiada atención a la selección. Por lo tanto, <strong>las listas estándar de selección múltiple son mucho más comunes.</strong><br /> | 
| <strong>Listas de versión preliminar</strong> Puede ser una o varias selecciones, pero muestran una vista previa del efecto de la selección en lugar de simplemente texto.<br /> | <img src="images/ctrl-list-boxes-image7.png" alt="Screen shot of Window Color options preview " /><br /> En este ejemplo, una vista previa de cada opción muestra claramente el efecto de la elección, que es más eficaz que usar texto solo.<br /> | 
| <strong>Generadores de listas</strong> Permita a los usuarios crear una lista de opciones agregando un elemento a la vez y, opcionalmente, estableciendo el orden de la lista.<br /> | Un generador de listas consta de dos listas de selección única: la lista de la izquierda es un conjunto fijo de opciones y la lista de la derecha es la lista que se está construyendo. Hay dos botones de comando entre las listas: <br /><ul><li>Botón <strong>Agregar</strong> que mueve la opción seleccionada actualmente a la lista que se está construyendo, insertada antes del elemento seleccionado. (Hacer doble clic en un elemento de opción tiene el mismo efecto).</li><li>Botón <strong>Quitar</strong> que quita el elemento seleccionado de la lista de elementos creados y lo devuelve a la lista de opciones. (Hacer doble clic en un elemento de la lista integrada tiene el mismo efecto). La lista integrada puede tener opcionalmente comandos <strong>Subir</strong> <strong>y</strong> Bajar para ordenar los elementos de lista.</li></ul><img src="images/ctrl-list-boxes-image8.png" alt="Screen shot of Toolbar buttons list builder " /><br /> En este ejemplo, se usa un generador de listas para crear una barra de herramientas seleccionando elementos de un conjunto de opciones disponibles y estableciendo su orden.<br /> | 
| <strong>Agregar o quitar listas</strong> Permita a los usuarios crear una lista de opciones agregando uno o varios elementos a la vez y, opcionalmente, estableciendo el orden de la lista (como los generadores de listas).<br /> | A diferencia de un generador de listas, <strong>al</strong> hacer clic en Agregar se muestra un cuadro de diálogo para seleccionar los elementos que se agregarán a la lista. El uso de un cuadro de diálogo independiente permite una flexibilidad significativa a la hora de elegir elementos, puede usar un selector de objetos especializado o incluso un diálogo común. En comparación con el generador de listas, esta variación es más compacta, pero requiere un poco más de esfuerzo para agregar elementos. <br /><img src="images/ctrl-list-boxes-image9.png" alt="Screen shot of Menu contents list " /><br /> En este ejemplo, los usuarios pueden agregar o quitar herramientas de un menú, así como establecer el orden.<br /> Aunque los patrones de generador de listas y agregar o quitar listas son significativamente más pesados que las otras listas de selección múltiple, ofrecen dos ventajas únicas:<br /><ul><li>Los usuarios tienen control sobre el orden de la lista, tanto durante la creación de la lista como después.</li><li>Los usuarios pueden revisar un resumen de los elementos seleccionados, lo que puede ser una ventaja significativa si el número de opciones es grande.</li></ul>Sus desventajas son que requieren mucho más espacio en la pantalla y pueden ser difíciles de usar al crear una lista grande de elementos desde cero. Por lo tanto, se usan mejor para crear listas cortas o modificar listas que ya existen.<br /> | 




 

## <a name="guidelines"></a>Directrices

### <a name="presentation"></a>Presentación

-   **Ordenar elementos de lista en un orden lógico,** como agrupar opciones relacionadas, colocar primero los elementos usados con más frecuencia o usar el orden alfabético. Ordene los nombres en orden alfabético, los números en orden numérico y las fechas en orden cronológico. Las listas con 12 o más elementos deben ordenarse alfabéticamente para facilitar la búsqueda de elementos.

**Correcto:** ![ captura de pantalla de alineación (izquierda, centro, derecha) ](images/ctrl-list-boxes-image10.png)

En este ejemplo, los elementos del cuadro de lista se ordenan por su relación espacial.

**Incorrecto:** ![ captura de pantalla de la lista desorganizada ](images/ctrl-list-boxes-image11.png)

En este ejemplo, hay tantos elementos de lista que deben ordenarse en orden alfabético.

**Correcto:** ![ captura de pantalla de la lista alfabética ](images/ctrl-list-boxes-image12.png)

En este ejemplo, los elementos de lista son más fáciles de encontrar porque están ordenados alfabéticamente. Sin embargo, el elemento "Todos Windows productos" está al principio de la lista, independientemente de su criterio de ordenación.

-   **Coloque las opciones que representan Todos o Ninguno al principio** de la lista, independientemente del criterio de ordenación de los elementos restantes.
-   **Incluya las metapórtamos entre paréntesis.**

![captura de pantalla de la lista desplegable sin ninguna seleccionada ](images/ctrl-list-boxes-image13.png)

En este ejemplo, "(none)" es una meta-opción porque no es un valor válido para la opción, sino que indica que la propia opción no se está utilizando.

-   **En su lugar, no tiene elementos de lista en blanco que usen meta-options.** Los usuarios no saben cómo interpretar los elementos en blanco, mientras que el significado de las meta-opciones es explícito.

**Incorrecto:** ![ captura de pantalla de la lista desplegable con la opción en blanco seleccionada ](images/ctrl-list-boxes-image14.png)

En este ejemplo, el significado del elemento en blanco no es claro.

**Correcto:** ![ captura de pantalla de la lista desplegable sin ninguna seleccionada ](images/ctrl-list-boxes-image13.png)

En este ejemplo, se usa la meta-opción "(none)" en su lugar.

### <a name="interaction"></a>Interacción

-   **Considere la posibilidad de proporcionar un comportamiento de doble clic.** Hacer doble clic debe tener el mismo efecto que seleccionar un elemento y realizar su comando predeterminado.
-   **Haga que el comportamiento de doble clic sea redundante.** Siempre debe haber un botón de comando o un comando de menú contextual que tenga el mismo efecto.
-   **Si los usuarios no pueden hacer nada con los elementos seleccionados, no permita la selección.**

**Correcto:** ![ captura de pantalla de la lista de cambios del asistente completada ](images/ctrl-list-boxes-image15.png)

Este cuadro de lista muestra una lista de cambios de solo lectura; no es necesario seleccionarlo.

-   **Al deshabilitar un cuadro de lista, deshabilite también las etiquetas asociadas y los botones de comando.**
-   **No use el cambio del elemento seleccionado en un cuadro de lista para:**
    -   Realice comandos.
    -   Mostrar otras ventanas, como un cuadro de diálogo para recopilar más entradas.
    -   Mostrar dinámicamente otros controles relacionados con el control seleccionado (los lectores de pantalla no pueden detectar tales eventos). **Excepción:** Puede cambiar dinámicamente el texto estático que se usa para describir el elemento seleccionado.

**Aceptable:** ![ captura de pantalla de los detalles del elemento de lista seleccionado ](images/ctrl-list-boxes-image16.png)

En este ejemplo, al cambiar el elemento seleccionado se cambia la descripción.

-   **Evite el desplazamiento horizontal.** Las listas de varias columnas se basan en el desplazamiento horizontal, que suele ser más difícil de usar que el desplazamiento vertical. Las listas de varias columnas que requieren desplazamiento horizontal se pueden usar si tiene muchos elementos ordenados alfabéticamente y espacio de pantalla suficiente para un control ancho.

**Aceptable:** ![ captura de pantalla de la lista de carpetas en el Explorador de Windows ](images/ctrl-list-boxes-image17.png)

En este ejemplo, se usan varias columnas que requieren desplazamiento horizontal porque hay muchos elementos y mucho espacio de pantalla disponible para un control ancho.

### <a name="multiple-selection-lists"></a>Listas de selección múltiple

-   **Considere la posibilidad de mostrar el número de elementos seleccionados debajo** de la lista, especialmente si es probable que los usuarios seleccionen varios elementos. Esta información no solo proporciona comentarios útiles, sino que también indica claramente que el cuadro de lista admite varias selecciones.

![captura de pantalla del cuadro de lista con cuatro elementos seleccionados ](images/ctrl-list-boxes-image5.png)

En este ejemplo, el número de elementos seleccionados se muestra debajo de la lista.

-   Puede proporcionar otras métricas de selección que puedan ser más significativas, como los recursos necesarios para las selecciones.

![captura de pantalla de la lista de casillas de características de Windows ](images/ctrl-list-boxes-image18.png)

En este ejemplo, el espacio en disco necesario para instalar los componentes es más significativo que el número de elementos seleccionados.

-   Si hay potencialmente muchos elementos de lista y es probable que seleccione o desactive todos ellos, agregue los botones de comando Seleccionar todo y Borrar todos.
-   En el caso de las listas de selección múltiple estándar, no use el modo de selección múltiple porque este modo de selección está en desuso. Para un comportamiento equivalente, use una lista de casillas en su lugar.

### <a name="default-values"></a>Valores predeterminados

-   **Seleccione la opción más segura (para evitar la pérdida de datos o acceso al sistema) y la opción más segura de forma predeterminada.** Si la seguridad y la seguridad no son factores, seleccione la opción más probable o conveniente.

**Excepción:** No seleccione ningún elemento si el control representa una propiedad en un estado mixto [,](glossary.md)lo que sucede cuando se muestra una propiedad para varios objetos que no tienen la misma configuración.

## <a name="recommended-sizing-and-spacing"></a>Tamaño y espaciado recomendados

![captura de pantalla del tamaño y espaciado del cuadro de lista ](images/ctrl-list-boxes-image19.png)

Tamaño y espaciado recomendados para los cuadros de lista.

-   **Elija un ancho de cuadro de lista adecuado para los datos válidos más largos.** Los cuadros de lista estándar no se pueden desplazar horizontalmente, por lo que los usuarios solo pueden ver lo que está visible en el control.
-   **Incluya un 30** % adicional (hasta un 200 % para el texto más corto) para cualquier texto (pero no números) que se localizará.
-   **Elija un alto del cuadro de lista que muestre un número entero de elementos.** Evite truncar elementos verticalmente.
-   **Elija un alto del cuadro de lista que elimine el desplazamiento vertical innecesario.** Los cuadros de lista deben mostrar entre 3 y 20 elementos sin necesidad de desplazarse. Considere la posibilidad de hacer que un cuadro de lista sea ligeramente más largo si elimina la barra de desplazamiento vertical. Las listas con potencialmente muchos elementos deben mostrar al menos cinco elementos para facilitar el desplazamiento mostrando más elementos a la vez y facilitando la posición de la barra de desplazamiento.
-   **Si los usuarios se benefician de hacer que el cuadro de lista sea mayor, haga que el cuadro de lista y su ventana primaria se puedan redimensionar.** Esto permite a los usuarios ajustar el tamaño del cuadro de lista según sea necesario. Sin embargo, los cuadros de lista de tamaño ajustable no deben mostrar menos de tres elementos.

## <a name="labels"></a>Etiquetas

**Etiquetas de control**

-   Todos los cuadros de lista necesitan etiquetas. Escriba la etiqueta como una palabra o frase, no como una frase; use un signo de dos puntos al final de la etiqueta.

**Excepción:** Omita la etiqueta si es simplemente una nueva instrucción de la instrucción principal de [un cuadro de diálogo.](glossary.md) En este caso, la instrucción principal toma los dos puntos (a menos que sea una pregunta) y la clave de acceso.

**Aceptable:** ![ captura de pantalla de la lista con etiqueta redundante ](images/ctrl-list-boxes-image20.png)

En este ejemplo, la etiqueta del cuadro de lista simplemente restablece la instrucción principal.

**Mejor:** ![ captura de pantalla de la lista de sin etiqueta redundante ](images/ctrl-list-boxes-image21.png)

En este ejemplo, se quita la etiqueta redundante, por lo que la instrucción principal toma los dos puntos y la clave de acceso.

-   Si un cuadro de lista está subordinado a un botón de radio o a una casilla y la etiqueta de ese control lo introduce y termina con dos puntos, no coloque una etiqueta adicional en el control de cuadro de lista.

![captura de pantalla de botón y lista con la misma etiqueta ](images/ctrl-list-boxes-image22.png)

En este ejemplo, el cuadro de lista está subordinado a un botón de radio y comparte su etiqueta.

-   Asigne una clave [de acceso única.](glossary.md) Para obtener instrucciones, vea [Teclado](inter-keyboard.md).
-   Use [el uso de mayúsculas y mayúsculas de estilo oración.](glossary.md)
-   Coloque la etiqueta a la izquierda del control o encima del control y alinee la etiqueta con el borde izquierdo del control.
    -   Si label está a la izquierda, alinee verticalmente el texto de la etiqueta con la primera línea de texto del control .

**Correcto:** ![ captura de pantalla de la lista con la etiqueta alineada a la izquierda encima de la captura de pantalla de la lista con ](images/ctrl-list-boxes-image23.png)![ la etiqueta alineada con texto a la izquierda ](images/ctrl-list-boxes-image24.png)

En estos ejemplos, la etiqueta de la parte superior se alinea con el borde izquierdo del cuadro de lista y la etiqueta de la izquierda se alinea con el texto del cuadro de lista.

**Incorrecto:** ![ captura de pantalla de la lista con la etiqueta alineada con texto encima de la captura de pantalla de la lista con ](images/ctrl-list-boxes-image25.png)![ la etiqueta alineada superior a la izquierda ](images/ctrl-list-boxes-image26.png)

En estos ejemplos incorrectos, la etiqueta de la parte superior se alinea con el texto del cuadro de lista y la etiqueta de la izquierda se alinea con la parte superior del cuadro de lista.

-   Para los cuadros de lista de selección múltiple, use una etiqueta que indique claramente que es posible realizar varias selecciones. Las etiquetas de lista de casillas pueden ser menos explícitas.

**Correcto:** ![ captura de pantalla de la lista con una o varias etiquetas ](images/ctrl-list-boxes-image27.png)

En este ejemplo, la etiqueta indica claramente que es posible realizar una selección múltiple.

**Incorrecto:** ![ captura de pantalla del cuadro de lista con la etiqueta de complementos ](images/ctrl-list-boxes-image28.png)

En este ejemplo, la etiqueta no proporciona información obvia sobre la selección múltiple.

**Mejor:** ![ captura de pantalla de la lista de casillas con la etiqueta de complementos ](images/ctrl-list-boxes-image29.png)

En este ejemplo, las casillas indican claramente que es posible realizar una selección múltiple, por lo que la etiqueta no tiene que ser explícita.

-   Puede especificar unidades (segundos, conexiones, entre paréntesis) después de la etiqueta.

**Texto de la opción**

-   Asigne un nombre único a cada opción.
-   Use [mayúsculas de estilo oración,](glossary.md)a menos que un elemento sea un nombre adecuado.
-   Escriba la etiqueta como una palabra o frase, no como una frase, y no use ningún signo de puntuación final.
-   Use expresiones paralelas e intente mantener la longitud aproximadamente igual para todas las opciones.

**Texto informativo y complementario**

-   Si necesita agregar texto informativo sobre un cuadro de lista, agrégrélo encima de la etiqueta. Use oraciones completas con signos de puntuación finales.
-   Use [el uso de mayúsculas y mayúsculas de estilo oración.](glossary.md)
-   La información adicional que es útil, pero no necesaria, debe mantenerse corta. Coloque este texto entre paréntesis entre la etiqueta y los dos puntos, o sin paréntesis debajo del control .

![captura de pantalla de la lista de casillas y texto descriptivo ](images/ctrl-list-boxes-image30.png)

En este ejemplo, el texto complementario se coloca debajo de la lista.

## <a name="documentation"></a>Documentación

Al hacer referencia a cuadros de lista:

-   Use el texto exacto de la etiqueta, incluida su inclusión en mayúsculas, pero no incluya el carácter de subrayado ni los dos puntos de la clave de acceso. Incluya la lista de palabras. No haga referencia a un cuadro de lista como un cuadro de lista o un campo.
-   Para los elementos de lista, use el texto exacto del elemento, incluido su uso de mayúsculas.
-   En programación y otra documentación técnica, consulte cuadros de lista como cuadros de lista. En cualquier otro lugar, use list.
-   Para describir la interacción del usuario, use select.
-   Cuando sea posible, formatee la etiqueta y los elementos de lista mediante texto en negrita. De lo contrario, coloque la etiqueta y los elementos entre comillas solo si es necesario para evitar confusiones.

Ejemplo: en la **lista Ir a qué,** seleccione **Marcador**.

