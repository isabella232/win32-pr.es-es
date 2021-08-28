---
title: Vistas de lista
description: Con una vista de lista, los usuarios pueden ver e interactuar con una colección de objetos de datos mediante una selección única o una selección múltiple.
ms.assetid: 62a7bfc8-96a9-450d-9db9-ec9dab6687b7
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8b8a1ce068b03ddf2a7aba40a0044f79914102d3
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983068"
---
# <a name="list-views"></a>Vistas de lista

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Con una vista de lista, los usuarios pueden ver e interactuar con una colección de objetos de datos mediante una selección única o una selección múltiple.

![captura de pantalla de la vista de lista con encabezados de columna ](images/ctrl-list-views-image1.png)

Una vista de lista típica.

Las vistas de lista tienen más flexibilidad y funcionalidad que los cuadros de lista. A diferencia de los cuadros de lista, admiten cambiar vistas, agrupar, varias columnas con encabezados, ordenar por columnas, cambiar el ancho y el orden de las columnas, ser un origen de arrastre o un destino de colocación, y copiar datos hacia y desde el Portapapeles.

> [!Note]  
> Las instrucciones relacionadas con [el diseño](vis-layout.md) y los cuadros [de lista](ctrl-list-boxes.md) se presentan en artículos independientes.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Una vista de lista es algo más que un cuadro de lista más flexible y funcional: su funcionalidad adicional da como resultado un uso diferente. En la tabla siguiente se muestra la comparación.



|   Uso                          | Cuadros de lista                 | Vistas de lista               |
|-----------------------------|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **Tipo de datos**<br/>    | Opciones de datos y programa.<br/> | Solo datos.<br/>                                                                                                                         |
| **Contents**<br/>     | Solo etiquetas.<br/>                   | Etiquetas y datos auxiliares, posiblemente en varias columnas.<br/>                                                                           |
| **Interacción**<br/>  | Se usa para realizar selecciones.<br/>    | Se puede usar para realizar selecciones, pero a menudo se usa para mostrar e interactuar con los datos. Puede ser un origen de arrastre o un destino de colocación.<br/> |
| **Presentación**<br/> | Fijo.<br/>                         | Los usuarios pueden cambiar las vistas, agrupar, ordenar por columnas y cambiar el orden y el ancho de las columnas.<br/>                                                |



 

Para decidir si este es el control adecuado, tenga en cuenta estas preguntas:

-   **¿La lista presenta datos, en lugar de opciones de programa?** Si no es así, considere la posibilidad de usar un cuadro de lista en su lugar.
-   **¿Los usuarios necesitan cambiar las vistas, agrupar, ordenar por columnas o cambiar el ancho y el orden de las columnas?** Si no es así, use un cuadro de lista en su lugar.
-   **¿El control debe ser un origen de arrastre o un destino de colocación?** Si es así, use una vista de lista.
-   **¿Es necesario copiar o pegar los elementos de lista en el Portapapeles?** Si es así, use una vista de lista.

### <a name="check-box-list-views"></a>Vistas de lista de casillas

-   **¿Se usa el control para elegir cero o más elementos de una lista de datos?** Para elegir un elemento, use una selección única en su lugar.
-   **¿La selección múltiple es esencial para la tarea o se usa normalmente?** Si es así, use una vista de lista de casillas para que la selección múltiple sea obvia, especialmente si los usuarios de destino no están avanzados. Si no es así, use una vista de lista de selección múltiple estándar si las casillas llamarían demasiada atención a la selección múltiple o provocaría demasiado desorden en la pantalla.
-   **¿Es importante la estabilidad de la selección múltiple?** Si es así, use una lista [de casillas,](ctrl-list-boxes.md)un generador de listas o agregar o quitar una lista porque al hacer clic solo cambia un solo elemento a la vez. Con una lista de selección múltiple estándar, es muy fácil borrar todas las selecciones incluso por accidente.

> [!Note]  
> A veces, un control que parece una vista de lista se implementa mediante un cuadro de lista y viceversa. En tales casos, aplique las directrices en función del uso, no de la implementación.

 

## <a name="usage-patterns"></a>Patrones de uso

Todas las vistas admiten una selección única, donde los usuarios solo pueden seleccionar un elemento a la vez y varias selecciones, donde los usuarios pueden seleccionar cualquier número de elementos, incluido ninguno. Las vistas de [lista](glossary.md)admiten el modo de selección extendida, donde la selección se puede extender arrastrando o con Mayús+clic o Ctrl+clic para seleccionar grupos de valores contiguos o no adyacentes, respectivamente. A diferencia de los cuadros de lista, no admiten el modo de selección [múltiple,](glossary.md)donde al hacer clic en cualquier elemento se alterna su estado de selección independientemente de las teclas Mayús y Ctrl.

### <a name="standard-list-view"></a>Vista de lista estándar

El control de vista de lista admite cinco vistas estándar:



|    Uso    |   Ejemplo        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Icono**<br/> cada elemento aparece como un icono medio, con una etiqueta y detalles opcionales a la derecha. <br/>                                                                                                                         | ![captura de pantalla de miniaturas con títulos y detalles ](images/ctrl-list-views-image2.png)<br/> La vista de mosaico muestra iconos medios con etiquetas y detalles opcionales a la derecha.<br/>                                                                                                                                                                |
| **Icono grande**<br/> cada elemento aparece como un icono extra grande, grande o mediano con una etiqueta debajo.<br/>                                                                                                                      | ![captura de pantalla de la vista de lista de miniaturas grande ](images/ctrl-list-views-image3.png)<br/> La vista Icono grande muestra cada elemento como un icono grande con una etiqueta debajo.<br/>                                                                                                                                                                              |
| **Icono pequeño**<br/> cada elemento aparece como un icono pequeño con una etiqueta a la derecha.<br/>                                                                                                                                           | ![captura de pantalla de la vista de lista de miniaturas pequeña ](images/ctrl-list-views-image4.png)<br/> La vista Icono pequeño muestra cada elemento como un icono pequeño con su etiqueta a la derecha.<br/>                                                                                                                                                                        |
| **Lista**<br/> cada elemento aparece como un icono pequeño con una etiqueta a la derecha.<br/>                                                                                                                                                 | en modo de lista, esta vista ordena elementos en columnas y usa una barra de desplazamiento horizontal. por el contrario, la vista de iconos ordena los elementos en filas y usa una barra de desplazamiento vertical. <br/> ![captura de pantalla de la vista de lista en modo de lista ](images/ctrl-list-views-image5.png)<br/> El modo de lista muestra cada elemento como un icono pequeño con su etiqueta a la derecha.<br/> |
| **Detalles**<br/> cada elemento aparece como una fila en formato tabular. la columna situada más a la izquierda contiene el icono y la etiqueta opcionales del elemento, y las columnas posteriores contienen información adicional, como las propiedades del elemento.<br/> | Además, las columnas se pueden agregar o quitar, y se pueden reordenar y cambiar el tamaño. Las filas se pueden agrupar, ordenar por columna. <br/> ![captura de pantalla de la vista de lista en modo de detalles ](images/ctrl-list-views-image6.png)<br/> La vista de detalles muestra cada elemento como una línea en un formato de tabla.<br/>                                                              |



 

### <a name="list-view-variations"></a>Variaciones de vista de lista




| Etiqueta | Value |
|--------|-------|
| <strong>Selector de columnas</strong><br /> Las vistas de lista a veces tienen tantas columnas que no resulta práctico mostrarlas todas. En este caso, el mejor enfoque es mostrar las columnas más útiles de forma predeterminada y permitir que los usuarios agreguen o quiten columnas según sea necesario. <br /> | <img src="images/ctrl-list-views-image7.png" alt="Screen shot of list view with Column Chooser menu " /><br /> Al hacer clic con el botón derecho en el encabezado de columna se muestra un menú contextual que permite a los usuarios agregar o quitar columnas.<br /><img src="images/ctrl-list-views-image8.png" alt="Screen shot of Choose Details dialog box " /><br /> Al hacer clic en Más en el menú contextual del encabezado de columna se muestra el cuadro de diálogo Elegir columnas, que permite a los usuarios agregar o quitar columnas, así como reordenarlas.<br /> | 
| <strong>Vista de lista de casillas</strong><br /> Permitir a los usuarios seleccionar varios elementos.<br /> | Las vistas de lista de selección múltiple tienen exactamente la misma apariencia que las vistas de lista de selección única, por lo que no hay ninguna pista visual de que admitan la selección múltiple. Se puede usar una vista de lista de casillas para indicar claramente que es posible realizar varias selecciones. Por lo tanto, este patrón debe usarse para tareas en las que la selección múltiple es esencial o se usa con frecuencia.<br /><img src="images/ctrl-list-views-image9.png" alt="Screen shot of dialog box with several check boxes " /><br /> En este ejemplo, una vista de icono pequeño usa casillas porque la selección múltiple es esencial para la tarea.<br /> | 
| <strong>Enumeración de vistas con grupos</strong><br /> Organice los datos en grupos.<br /> | Aunque las vistas de detalles suelen admitir la ordenación de los datos por cualquiera de las columnas, las vistas de lista permiten a los usuarios organizar los elementos en grupos. Algunas de las ventajas de la agrupación son:<br /><ul><li>Los grupos funcionan en todas las vistas (excepto en la lista), por lo que, por ejemplo, los usuarios podrían agrupar una vista de iconos muy grandes de álbumes por intérprete.</li><li>Los grupos pueden ser colecciones de alto nivel, que a menudo son más significativas que agrupar directamente los datos. Por ejemplo, Windows Explorer agrupa fechas en Today, Last week, Last week, Earlier this year y Hace mucho tiempo.</li></ul><img src="images/ctrl-list-views-image10.png" alt="Screen shot of list view with several data groups " /><br /> En este ejemplo, el Windows Centro de bienvenida muestra los elementos agrupados en una vista de lista.<br /> | 




 

## <a name="guidelines"></a>Directrices

### <a name="presentation"></a>Presentación

-   **Ordenar elementos de lista en un orden lógico.** Ordene los nombres en orden alfabético, los números en orden numérico y las fechas en orden cronológico.
-   **Si procede, permita a los usuarios cambiar el criterio de ordenación.** La ordenación de usuarios es importante si la lista tiene muchos elementos o si hay escenarios en los que los elementos se encuentran de forma más eficaz mediante un criterio de ordenación distinto del predeterminado.
-   **Use el atributo Always Show Selection para** que los usuarios puedan determinar fácilmente el elemento seleccionado, incluso cuando el control no tenga el foco.
-   **Evite presentar vistas de lista vacías.** Si los usuarios crean una lista, inicialice la lista con instrucciones o elementos de ejemplo que los usuarios puedan necesitar.

    ![captura de pantalla del cuadro de diálogo de búsqueda con instrucciones ](images/ctrl-list-views-image11.png)

    En este ejemplo, la vista Lista de búsqueda presenta inicialmente instrucciones.

-   **Si los usuarios pueden cambiar las vistas, agrupar, ordenar por columnas o cambiar las columnas y sus anchos y orden, haga que esa configuración se conserve para que su efecto se haga la próxima vez que se muestre la vista de lista.** Hacer que se conserven en una vista por lista, por usuario.

### <a name="interaction"></a>Interacción

-   **Use un solo clic para seleccionar el elemento de lista al que apunta el usuario. Excepción:** para el patrón de lista de vínculos de comandos, un solo clic selecciona el elemento y cierra la ventana o navega a la página siguiente.
-   **Considere la posibilidad de proporcionar un comportamiento de doble clic.** Hacer doble clic debe tener el mismo efecto que seleccionar un elemento y realizar su comando predeterminado.
-   **Haga que el comportamiento de doble clic sea redundante.** Siempre debe haber un botón de comando o un comando de menú contextual que tenga el mismo efecto.
-   Si un elemento de lista requiere una explicación adicional, **proporcione la explicación en una información** sobre [.](ctrl-tooltips-and-infotips.md) Use oraciones completas y signos de puntuación finales.

    ![captura de pantalla de la vista de lista con información sobre el teclado ](images/ctrl-list-views-image12.png)

    En este ejemplo, se usa una información sobre cómo proporcionar más información.

-   **Proporcione menús contextuales de los comandos pertinentes.** Estos comandos incluyen Cortar, Copiar, Pegar, Quitar o Eliminar, Cambiar nombre y Propiedades.
-   **Si los usuarios pueden cambiar el criterio de ordenación y la agrupación, proporcione los menús contextuales Ordenar por y Agrupar por.** El primer clic en un nombre de columna ordena o agrupa la lista en el orden ascendente de esa columna, el segundo clic ordena o agrupa en orden descendente. Use el orden anterior (de otra columna) como clave secundaria.

    ![captura de pantalla de la vista de lista con el menú "Ordenar por" ](images/ctrl-list-views-image13.png)

    En este ejemplo, el menú contextual Ordenar por cambia el criterio de ordenación. Al hacer clic en Nombre una vez, se ordena por nombre en orden ascendente. Al hacer clic de nuevo en Nombre, se ordena por nombre en orden descendente.

-   **Haga que el encabezado de columna de la vista de lista sea accesible mediante el teclado.**
    -   **Desarrolladores:** Para ello, puede establecer el foco en el control de encabezado de columna. Esta funcionalidad es nueva para Windows Vista.
-   **Al deshabilitar una vista de lista, deshabilite también las etiquetas asociadas y los botones de comando.**
-   **Evite el desplazamiento horizontal.** El modo Lista usa el desplazamiento horizontal. Este modo suele ser el más compacto, pero el desplazamiento horizontal suele ser más difícil de usar que el desplazamiento vertical. Considere la posibilidad de usar la vista Icono pequeño en su lugar si la compactación no es importante. Sin embargo, el modo de lista es una buena opción cuando hay muchos elementos ordenados alfabéticamente y suficiente espacio de pantalla para un control ancho.

    **Aceptable:**

    ![captura de pantalla de un control de modo de lista ancha ](images/ctrl-list-views-image14.png)

    En este ejemplo, se usa el modo de lista porque hay muchos elementos y mucho espacio de pantalla disponible para un control ancho.

### <a name="multiple-selection-lists"></a>Listas de selección múltiple

-   **Considere la posibilidad de mostrar el número de elementos seleccionados debajo** de la lista, especialmente si es probable que los usuarios seleccionen varios elementos. Esta información no solo proporciona comentarios útiles, sino que también indica claramente que la vista de lista admite varias selecciones.

    ![captura de pantalla de la lista de cinco miniaturas seleccionadas ](images/ctrl-list-views-image15.png)

    En este ejemplo, el número de elementos seleccionados se muestra debajo de la lista.

-   Como alternativa, en lugar del número de elementos seleccionados, puede proporcionar otras métricas de selección que puedan ser más significativas, como los recursos necesarios para las selecciones.

    ![captura de pantalla del cuadro de diálogo que muestra el espacio en disco ](images/ctrl-list-views-image16.png)

    En este ejemplo, el espacio en disco necesario para instalar los componentes es más significativo que el número de componentes seleccionados.

-   Para las vistas de lista de casillas, si hay potencialmente muchos elementos y es probable que se activen o desactiven todos, agregue los botones de comando Seleccionar todo y Borrar todos.
-   **Use las casillas de estado mixto para indicar la selección parcial de los elementos de un contenedor.** El estado mixto no se usa como tercer estado para un elemento individual.

### <a name="changing-views"></a>Cambiar vistas

Si los usuarios pueden cambiar las vistas:

-   **Elija la vista más cómoda de forma predeterminada.** Los cambios que realicen los usuarios deben ser persistentes en una vista por lista y por usuario.
-   **Cambie la vista mediante un botón de división, un botón de menú o una lista desplegable.** Siempre que sea práctico, use un [botón de división en](ctrl-command-buttons.md) la barra de herramientas y cambie la etiqueta del botón para reflejar la vista actual.

    ![captura de pantalla de la lista con el botón "vistas" dividido ](images/ctrl-list-views-image17.png)

    En este ejemplo, se usa un botón de división en la barra de herramientas para cambiar las vistas.

-   **Proporcione un menú contextual Ver.**

    ![captura de pantalla de la lista con el menú contextual "Ver" ](images/ctrl-list-views-image18.png)

En este ejemplo, se usa un menú contextual Ver para cambiar las vistas.

### <a name="details-views"></a>Vistas de detalles

-   **Considere la posibilidad de usar la vista de iconos para mejorar la legibilidad.**

    **Aceptable:**

    ![captura de pantalla de la lista de detalles con columnas estrechas ](images/ctrl-list-views-image19.png)

    En este ejemplo, hay demasiados datos y la ventana, la lista y las columnas son demasiado pequeñas, lo que hace que los elementos de lista sean difíciles de leer.

    **Mejor:**

    ![captura de pantalla de la lista de detalles con datos en grupos ](images/ctrl-list-views-image20.png)

    En este ejemplo, la vista Icono muestra los datos sin truncamiento.

-   **Elija los anchos de columna predeterminados adecuados para los datos más largos.** Las vistas de lista truncan automáticamente los datos largos con puntos suspensivos, por lo que los anchos de columna son adecuados si se muestran algunos puntos suspensivos de forma predeterminada. Aunque los usuarios pueden cambiar el tamaño de las columnas, prefieren otras soluciones:

    -   Ajuste el tamaño de cada ancho de columna para que se ajuste a sus datos.
    -   Ajuste el ancho del control para que se ajuste a sus columnas más las barras de desplazamiento probables.
    -   Si es necesario, use el desplazamiento horizontal.
    -   Haber truncado los datos solo para elementos de tamaño impar o como último recurso.

    Si los datos de tamaño normal deben truncarse de forma predeterminada, haga que se pueda cambiar el tamaño de la vista de ventana y lista. Incluya un 30 % adicional (hasta un 200 % para el texto más corto) para cualquier texto (pero no números) que se localizará.

    **Incorrecto:**

    ![captura de pantalla de columnas de lista con datos truncados ](images/ctrl-list-views-image21.png)

    En este ejemplo, la mayoría de los datos se truncan. Los puntos suspensivos indican claramente que los anchos de columna y control son demasiado pequeños para los datos.

    **Incorrecto:**

    ![captura de pantalla de una lista de una columna con datos truncados ](images/ctrl-list-views-image22.png)

    En este ejemplo, los datos se truncan sin razón.

-   **Elija un orden de columna predeterminado adecuado.** Por lo general, ordene las columnas de la manera siguiente:

    -   En primer lugar, el nombre del elemento o los datos de identificación.
    -   A continuación, otros datos útiles para diferenciar los elementos de lista.
    -   A continuación, los datos más útiles (preferiblemente de longitud corta o fija).
    -   A continuación, datos menos útiles (preferiblemente de longitud corta o fija).
    -   Último, largo, datos de longitud variable.

    Long, variable length-data se coloca en las últimas columnas para reducir la necesidad de desplazamiento horizontal. Dentro de estas categorías, coloque la información relacionada en una secuencia lógica.

-   **Cuando sea necesario, permita a los usuarios agregar y quitar columnas, así como cambiar el orden.** Muestra las columnas más útiles de forma predeterminada. Esto se logra con el atributo Header Drag Drop.
-   Elija una alineación adecuada para los datos. Use las reglas siguientes:
    -   Alinear a la derecha números, monedas y horas.
    -   Texto alineado a la izquierda, identificadores (incluso si son numéricos) y fechas.
-   En el caso de los encabezados de columna ordenables, el primer clic en un encabezado ordena la lista en orden ascendente para la columna y el segundo clic se ordena **en orden descendente.** Use el criterio de ordenación anterior (de otra columna) como clave de ordenación secundaria.

    ![captura de pantalla de la lista de detalles con datos ordenados ](images/ctrl-list-views-image23.png)

    En este ejemplo, primero se hizo clic en la columna Nombre y, a continuación, en la columna Tipo. Como resultado, Tipo en orden ascendente es la clave de ordenación principal y Nombre en orden ascendente es el secundario.

-   **Use el atributo Seleccionar fila completa para** que los usuarios puedan determinar fácilmente los elementos seleccionados en todas las columnas.
-   **No use un encabezado de columna ordenable a menos que se puedan ordenar los datos.**
-   **No use un encabezado de columna si solo hay una columna y no es necesario invertir la ordenación.** Use una etiqueta en su lugar para identificar los datos.

    **Incorrecto:**

    ![captura de pantalla de la lista con etiqueta en el encabezado de columna ](images/ctrl-list-views-image24.png)

    **Correcto:**

    ![captura de pantalla de la lista con la etiqueta encima del control ](images/ctrl-list-views-image25.png)

    En el ejemplo correcto, se usa una etiqueta en lugar de un encabezado de columna.

## <a name="recommended-sizing-and-spacing"></a>Tamaño y espaciado recomendados

![captura de pantalla de tamaño y espaciado de la lista ](images/ctrl-list-views-image26.png)

Tamaño y espaciado recomendados para las vistas de lista.

-   **Elija un alto de vista de lista que muestre un número entero de elementos.** Evite truncar elementos verticalmente.
-   **Elija un tamaño de vista de lista que elimine el desplazamiento vertical y horizontal innecesario en todas las vistas admitidas.** Las vistas de lista deben mostrar entre 3 y 20 elementos. Considere la posibilidad de hacer que una vista de lista sea ligeramente mayor si elimina una barra de desplazamiento. Las listas con potencialmente muchos elementos deben mostrar al menos cinco elementos para facilitar el desplazamiento mostrando más elementos a la vez y facilitando la posición de la barra de desplazamiento.
-   **Si los usuarios se benefician de hacer que la vista de lista sea mayor, haga que la vista de lista y su ventana primaria se puedan volver a tamaño.** Esto permite a los usuarios ajustar el tamaño de la vista de lista según sea necesario. Sin embargo, las vistas de lista de tamaño ajustable no deben mostrar menos de tres elementos.

## <a name="labels"></a>Etiquetas

### <a name="control-labels"></a>Etiquetas de control

-   Todas las vistas de lista necesitan etiquetas. Escriba la etiqueta como una palabra o frase, no como una frase, terminando con dos puntos con texto estático.
-   Asigne una clave [de acceso única](glossary.md) para cada etiqueta. Para obtener instrucciones, vea [Teclado](inter-keyboard.md).
-   Use [el uso de mayúsculas y mayúsculas de estilo oración.](glossary.md)
-   Coloque la etiqueta encima del control y alinee la etiqueta con el borde izquierdo del control.
-   Para las vistas de lista de selección múltiple, escriba la etiqueta que indique claramente que es posible realizar varias selecciones. Las etiquetas de vista de lista de casillas pueden ser menos explícitas.

    **Correcto:**

    ![captura de pantalla de la etiqueta: seleccione uno o varios complementos. ](images/ctrl-list-views-image27.png)

    En este ejemplo, la etiqueta indica claramente que es posible realizar una selección múltiple.

    **Incorrecto:**

    ![captura de pantalla de la etiqueta: complementos ](images/ctrl-list-views-image28.png)

    En este ejemplo, la etiqueta no proporciona información sobre la selección múltiple.

    **Aceptable:**

    ![captura de pantalla de la etiqueta de lista de casillas: complementos ](images/ctrl-list-views-image29.png)

    En este ejemplo, las casillas indican claramente que es posible realizar una selección múltiple, por lo que la etiqueta no tiene que ser explícita.

-   Puede especificar unidades (segundos, conexiones, entre paréntesis) después de la etiqueta.

### <a name="heading-labels"></a>Etiquetas de encabezado

-   Mantenga las etiquetas de encabezado breves (tres palabras o menos).
-   Use un único sustantivo o frase de sustantivo sin puntuación final.
-   Use [el uso de mayúsculas y mayúsculas de estilo oración.](glossary.md)
-   Alinee el encabezado de la misma manera que los datos.

### <a name="group-labels"></a>Etiquetas de grupo

-   Use las siguientes etiquetas de grupo para colecciones de alto nivel:
    -   Nombres: use la primera letra del nombre o los intervalos de letras.
    -   Tamaños: sin especificar, 0 KB, 0-10 KB, 10-100 KB, 100 KB - 1 MB, 1-16 MB, 16-128 MB
    -   Fechas: Hoy, Ayer, Última semana, Antes de este año y Hace mucho tiempo.
-   De lo contrario, las etiquetas de grupo usan el texto exacto de los datos que se agrupan, incluidas las mayúsculas y las marcas de puntuación.

### <a name="data-text"></a>Texto de datos

-   Use [el uso de mayúsculas y mayúsculas de estilo oración.](glossary.md)

### <a name="instructional-text"></a>Texto informativo

-   Si necesita agregar texto informativo sobre una vista de lista, agrégrélo encima de la etiqueta. Use oraciones completas con signos de puntuación finales.
-   Use [el uso de mayúsculas y mayúsculas de estilo oración.](glossary.md)
-   La información adicional que es útil, pero no necesaria, debe mantenerse corta. Coloque esta información entre paréntesis entre la etiqueta y los dos puntos o sin paréntesis debajo del control .

## <a name="documentation"></a>Documentación

Al hacer referencia a vistas de lista:

-   Use el texto exacto de la etiqueta, incluida su inclusión en mayúsculas, pero no incluya el carácter de subrayado ni los dos puntos de la clave de acceso, e incluya la lista de palabras. No haga referencia a un cuadro de lista como un cuadro de lista, una vista de lista o un campo.
-   En el caso de los datos de lista, use el texto de datos exactos, incluido su uso de mayúsculas y mayúsculas.
-   Consulte las vistas de lista como vistas de lista solo en programación y otra documentación técnica. Lista de uso en cualquier otro lugar.
-   Para describir la interacción del usuario, use select para los datos y haga clic en los encabezados.
-   Cuando sea posible, formatee las opciones de etiqueta y lista mediante texto en negrita. De lo contrario, coloque la etiqueta y las opciones entre comillas solo si es necesario para evitar confusiones.

Ejemplo: en la **lista Programas y servicios,** seleccione **Compartir archivos e impresoras.**

Al hacer referencia a las casillas de una vista de lista:

-   Use el texto exacto de la etiqueta, incluida su mayúsculas y las mayúsculas, e incluya la casilla de palabras. No incluya el carácter de subrayado de la clave de acceso.
-   Para describir la interacción del usuario, use seleccionar y borrar.
-   Cuando sea posible, formatee la etiqueta con texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.

Ejemplo: active la **casilla Subrayado.**

 

