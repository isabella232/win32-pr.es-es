---
title: Vistas de lista
description: Con una vista de lista, los usuarios pueden ver e interactuar con una colección de objetos de datos, mediante una selección única o una selección múltiple.
ms.assetid: 62a7bfc8-96a9-450d-9db9-ec9dab6687b7
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c3c823b23c03f29ac6b80e10df79eac36653f2e4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "103820066"
---
# <a name="list-views"></a>Vistas de lista

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Con una vista de lista, los usuarios pueden ver e interactuar con una colección de objetos de datos, mediante una selección única o una selección múltiple.

![captura de pantalla de la vista de lista con encabezados de columna ](images/ctrl-list-views-image1.png)

Vista de lista típica.

Las vistas de lista tienen más flexibilidad y funcionalidad que los cuadros de lista. A diferencia de los cuadros de lista, admiten el cambio de vistas, la agrupación, varias columnas con encabezados, la ordenación por columnas, el cambio del ancho y el orden de las columnas, el origen o el destino de arrastre y la copia de datos hacia y desde el portapapeles.

> [!Note]  
> Las instrucciones relacionadas con el [diseño](vis-layout.md) y los [cuadros de lista](ctrl-list-boxes.md) se presentan en artículos independientes.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Una vista de lista es algo más que un cuadro de lista funcional y más flexible: su funcionalidad adicional tiene como resultado un uso diferente. En la tabla siguiente se muestra la comparación.



|                             |                                           |                                                                                                                                               |
|-----------------------------|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
|                             | **Cuadros de lista**<br/>                 | **Vistas de lista**<br/>                                                                                                                     |
| **Tipo de datos**<br/>    | Opciones de datos y de programa.<br/> | Solo datos.<br/>                                                                                                                         |
| **Contents**<br/>     | Solo etiquetas.<br/>                   | Etiquetas y datos auxiliares, posiblemente en varias columnas.<br/>                                                                           |
| **Interacción**<br/>  | Se utiliza para efectuar selecciones.<br/>    | Se puede usar para realizar selecciones, pero a menudo se usa para mostrar e interactuar con los datos. Puede ser un origen de arrastre o un destino de colocación.<br/> |
| **Presentación**<br/> | Resuelto.<br/>                         | Los usuarios pueden cambiar las vistas, agrupar, ordenar por columnas y cambiar el ancho y el orden de las columnas.<br/>                                                |



 

Para decidir si este es el control adecuado, tenga en cuenta estas preguntas:

-   **¿La lista presenta datos, en lugar de opciones de programa?** Si no es así, considere la posibilidad de usar un cuadro de lista en su lugar.
-   **¿Los usuarios deben cambiar las vistas, agrupar, ordenar por columnas o cambiar el orden y el ancho de las columnas?** En caso contrario, utilice un cuadro de lista.
-   **¿El control debe ser un origen de arrastre o un destino de colocación?** Si es así, use una vista de lista.
-   **¿Es necesario copiar o pegar los elementos de la lista desde el portapapeles?** Si es así, use una vista de lista.

### <a name="check-box-list-views"></a>Vistas de lista de casillas

-   **¿Se usa el control para elegir cero o más elementos de una lista de datos?** Para elegir un elemento, utilice la selección única en su lugar.
-   **¿Es esencial la selección múltiple de la tarea o se usa habitualmente?** Si es así, use una vista de lista de casillas para hacer que la selección múltiple sea obvia, especialmente si los usuarios de destino no están avanzados. Si no es así, use una vista de lista de selección múltiple estándar si las casillas van a dibujar demasiada atención en la selección múltiple o se producirá demasiado desorden en la pantalla.
-   **¿Es importante la estabilidad de la selección múltiple?** Si es así, use una lista de [casillas](ctrl-list-boxes.md), un generador de listas o agregar o quitar lista, porque al hacer clic en solo se cambian los elementos de uno en uno. Con una lista de selección múltiple estándar, es muy fácil borrar todas las selecciones incluso accidentalmente.

> [!Note]  
> A veces, un control que se parece a una vista de lista se implementa mediante un cuadro de lista y viceversa. En tales casos, aplique las directrices basadas en el uso, no en la implementación.

 

## <a name="usage-patterns"></a>Patrones de uso

Todas las vistas admiten la selección única, donde los usuarios solo pueden seleccionar un elemento cada vez, y varias selecciones, donde los usuarios pueden seleccionar cualquier número de elementos, incluido ninguno. Las vistas de lista admiten el [modo de selección extendida](glossary.md), donde la selección se puede extender arrastrando o presionando Mayús + clic o Ctrl + clic para seleccionar grupos de valores contiguos o no adyacentes, respectivamente. A diferencia de los cuadros de lista, no admiten el [modo de selección múltiple](glossary.md), donde al hacer clic en cualquier elemento se alterna su estado de selección independientemente de las teclas Mayús y Ctrl.

### <a name="standard-list-view"></a>Vista de lista estándar

El control de vista de lista admite cinco vistas estándar:



|                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Icono**<br/> cada elemento aparece como un icono medio, con una etiqueta y detalles opcionales a la derecha. <br/>                                                                                                                         | ![captura de pantalla de miniaturas con títulos y detalles ](images/ctrl-list-views-image2.png)<br/> La vista en mosaico muestra iconos medios con etiquetas y detalles opcionales a la derecha.<br/>                                                                                                                                                                |
| **Icono grande**<br/> cada elemento aparece como un icono extra grande, grande o mediano con una etiqueta debajo.<br/>                                                                                                                      | ![captura de pantalla de la vista de lista en miniatura grande ](images/ctrl-list-views-image3.png)<br/> Vista de iconos grandes muestra cada elemento como un icono grande con una etiqueta debajo de él.<br/>                                                                                                                                                                              |
| **Icono pequeño**<br/> cada elemento aparece como un icono pequeño con una etiqueta a la derecha.<br/>                                                                                                                                           | ![captura de pantalla de la vista de lista en miniatura pequeña ](images/ctrl-list-views-image4.png)<br/> Vista de iconos pequeños muestra cada elemento como un icono pequeño con su etiqueta a la derecha.<br/>                                                                                                                                                                        |
| **Lista**<br/> cada elemento aparece como un icono pequeño con una etiqueta a la derecha.<br/>                                                                                                                                                 | en el modo de lista, esta vista ordena los elementos en columnas y usa una barra de desplazamiento horizontal. por el contrario, los modos de vista de iconos ordenan los elementos de las filas y usan una barra de desplazamiento vertical. <br/> ![captura de pantalla de la vista de lista en modo de lista ](images/ctrl-list-views-image5.png)<br/> El modo de lista muestra cada elemento como un icono pequeño con su etiqueta a la derecha.<br/> |
| **Detalles**<br/> cada elemento aparece como una fila en formato tabular. la columna situada más a la izquierda contiene el icono opcional y la etiqueta del elemento, y las columnas siguientes contienen información adicional, como las propiedades de los elementos.<br/> | Además, se pueden agregar o quitar columnas y reordenarlas y cambiar su tamaño. las filas se pueden agrupar, ordenar por columna. <br/> ![captura de pantalla de la vista de lista en modo de detalles ](images/ctrl-list-views-image6.png)<br/> La vista de detalles muestra cada elemento como una línea en un formato de tabla.<br/>                                                              |



 

### <a name="list-view-variations"></a>Variaciones de la vista de lista



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Selector de columnas</strong><br/> En ocasiones, las vistas de lista tienen tantas columnas que no resultan prácticas para mostrarlas todas. En este caso, el mejor enfoque es mostrar las columnas más útiles de forma predeterminada y permitir que los usuarios agreguen o quiten columnas según sea necesario. <br/></td>
<td><img src="images/ctrl-list-views-image7.png" alt="Screen shot of list view with Column Chooser menu " /><br/> Al hacer clic con el botón secundario en el encabezado de columna, se muestra un menú contextual que permite a los usuarios agregar o quitar columnas.<br/> <img src="images/ctrl-list-views-image8.png" alt="Screen shot of Choose Details dialog box " /><br/> Al hacer clic en más en el menú contextual del encabezado de columna, se muestra el cuadro de diálogo elegir columnas, que permite a los usuarios agregar o quitar columnas, así como reordenarlas.<br/></td>
</tr>
<tr class="even">
<td><strong>Vista de lista de casillas</strong><br/> Permitir a los usuarios seleccionar varios elementos.<br/></td>
<td>Las vistas de lista de selección múltiple tienen exactamente la misma apariencia que las vistas de lista de selección única, por lo que no hay ninguna pista visual de que admitan la selección múltiple. Se puede usar una vista de lista de casillas para indicar claramente que es posible la selección múltiple. Por consiguiente, este patrón se debe usar para las tareas en las que la selección múltiple es esencial o se usa con frecuencia.<br/> <img src="images/ctrl-list-views-image9.png" alt="Screen shot of dialog box with several check boxes " /><br/> En este ejemplo, una vista de iconos pequeños usa casillas porque la selección múltiple es esencial para la tarea.<br/></td>
</tr>
<tr class="odd">
<td><strong>Mostrar vistas con grupos</strong><br/> Organice los datos en grupos.<br/></td>
<td>Mientras que las vistas de detalles suelen permitir ordenar los datos por cualquiera de las columnas, las vistas de lista permiten a los usuarios organizar los elementos en grupos. Algunas de las ventajas de la agrupación son:<br/>
<ul>
<li>Los grupos funcionan en todas las vistas (excepto en la lista), por lo que, por ejemplo, los usuarios pueden agrupar una vista de iconos extra grande de álbumes por intérprete.</li>
<li>Los grupos pueden ser recopilaciones de alto nivel, que a menudo son más significativos que la agrupación directa de los datos. Por ejemplo, el explorador de Windows agrupa las fechas en hoy, ayer, última semana, a principios de este año, y hace mucho tiempo.</li>
</ul>
<img src="images/ctrl-list-views-image10.png" alt="Screen shot of list view with several data groups " /><br/> En este ejemplo, el centro de bienvenida de Windows muestra los elementos agrupados en una vista de lista.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Directrices

### <a name="presentation"></a>Presentación

-   **Ordenar los elementos de la lista en un orden lógico.** Ordenar nombres en orden alfabético, números en orden numérico y fechas en orden cronológico.
-   **Si procede, permita a los usuarios cambiar el criterio de ordenación.** La ordenación de usuarios es importante si la lista tiene muchos elementos o si hay escenarios en los que los elementos se detectan de forma más eficaz con un criterio de ordenación distinto del predeterminado.
-   **Use el atributo de selección Mostrar siempre** para que los usuarios puedan determinar fácilmente el elemento seleccionado, incluso cuando el control no tenga el foco.
-   **Evite presentar vistas de lista vacías.** Si los usuarios crean una lista, inicialice la lista con instrucciones o elementos de ejemplo que los usuarios puedan necesitar.

    ![captura de pantalla del cuadro de diálogo de búsqueda con instrucciones ](images/ctrl-list-views-image11.png)

    En este ejemplo, la vista de la lista de búsqueda presenta inicialmente instrucciones.

-   **Si los usuarios pueden cambiar las vistas, agrupar, ordenar por columnas o cambiar las columnas, así como su ancho y orden, se conservarán para que se apliquen la próxima vez que se muestre la vista de lista.** Hacer que se conserven en una vista por lista, por usuario.

### <a name="interaction"></a>Interacción

-   **Use un solo clic para seleccionar el elemento de la lista al que apunta el usuario. Excepción:** para el patrón de lista de vínculos de comandos, un solo clic selecciona el elemento y cierra la ventana o navega a la página siguiente.
-   **Considere la posibilidad de proporcionar un comportamiento de doble clic.** Hacer doble clic debe tener el mismo efecto que seleccionar un elemento y ejecutar el comando predeterminado.
-   **Haga que el comportamiento de doble clic sea redundante.** Siempre debe haber un botón de comando o un comando de menú contextual que tenga el mismo efecto.
-   Si un elemento de lista requiere una explicación más detallada, **proporcione la explicación en una** [sugerencia](ctrl-tooltips-and-infotips.md). Usar frases completas y puntuación final.

    ![captura de pantalla de la vista de lista con la sugerencia de teclado ](images/ctrl-list-views-image12.png)

    En este ejemplo, se usa un recuadro informativo para proporcionar más información.

-   **Proporcionar menús contextuales de comandos relevantes.** Estos comandos incluyen cortar, copiar, pegar, quitar o eliminar, cambiar nombre y propiedades.
-   **Si los usuarios pueden cambiar el criterio de ordenación y la agrupación, proporcione los menús de contexto ordenar por y agrupar por.** La primera vez que haga clic en un nombre de columna ordena o agrupa la lista en orden ascendente para esa columna, el segundo clic ordena o agrupa en orden descendente. Use el orden anterior (de otra columna) como clave secundaria.

    ![captura de pantalla de la vista de lista con el menú ' ordenar por ' ](images/ctrl-list-views-image13.png)

    En este ejemplo, el menú contextual ordenar por cambia el criterio de ordenación. Al hacer clic en nombre una vez se ordena por nombre en orden ascendente. Al hacer clic en nombre de nuevo, se ordena por nombre en orden descendente.

-   **Haga que el encabezado de columna de la vista de lista sea accesible con el teclado.**
    -   **Desarrolladores:** Para ello, establezca el foco en el control de encabezado de columna. Esta funcionalidad es nueva en Windows Vista.
-   **Al deshabilitar una vista de lista, deshabilite también las etiquetas y los botones de comando asociados.**
-   **Evite el desplazamiento horizontal.** El modo de lista utiliza el desplazamiento horizontal. Este modo suele ser el más compacto, pero el desplazamiento horizontal suele ser más difícil de usar que el desplazamiento vertical. Considere la posibilidad de usar la vista de iconos pequeños en su lugar si la compactación no es importante. Sin embargo, el modo de lista es una buena opción cuando hay muchos elementos ordenados alfabéticamente y suficiente espacio de pantalla para un control ancho.

    **Aceptable:**

    ![captura de pantalla de un control de modo de lista ancho ](images/ctrl-list-views-image14.png)

    En este ejemplo, se usa el modo de lista porque hay muchos elementos y una gran cantidad de espacio de pantalla disponible para un control ancho.

### <a name="multiple-selection-lists"></a>Listas de selección múltiple

-   **Considere la posibilidad de mostrar el número de elementos seleccionados debajo de la lista**, especialmente si es probable que los usuarios seleccionen varios elementos. Esta información no solo proporciona comentarios útiles, sino que también indica claramente que la vista de lista admite varias selecciones.

    ![captura de pantalla de la lista de cinco miniaturas seleccionadas ](images/ctrl-list-views-image15.png)

    En este ejemplo, el número de elementos seleccionados se muestra debajo de la lista.

-   Como alternativa, en lugar del número de elementos seleccionados, puede proporcionar otras métricas de selección que podrían ser más significativas, como los recursos necesarios para las selecciones.

    ![captura de pantalla del cuadro de diálogo que muestra el espacio en disco ](images/ctrl-list-views-image16.png)

    En este ejemplo, el espacio en disco necesario para instalar los componentes es más significativo que el número de componentes seleccionados.

-   En el caso de las vistas de lista de casillas, si hay muchos elementos y seleccionando o borrando todos, es probable que se agreguen botones de comando Seleccionar todo y borrar todo.
-   **Use las casillas de verificación de estado mixto para indicar la selección parcial de los elementos de un contenedor.** El estado mixto no se utiliza como tercer Estado para un elemento individual.

### <a name="changing-views"></a>Cambiar vistas

Si los usuarios pueden cambiar las vistas:

-   **Elija la vista más conveniente de forma predeterminada.** Cualquier cambio que realicen los usuarios debe hacerse persistente en cada vista de lista por usuario.
-   **Cambiar la vista mediante un botón de expansión, un botón de menú o una lista desplegable.** Siempre que sea práctico, use un [botón de expansión](ctrl-command-buttons.md) en la barra de herramientas y cambie la etiqueta del botón para que refleje la vista actual.

    ![captura de pantalla de la lista con el botón dividir ' vistas ' ](images/ctrl-list-views-image17.png)

    En este ejemplo, se usa un botón de expansión en la barra de herramientas para cambiar las vistas.

-   **Proporcione un menú contextual de vista.**

    ![captura de pantalla de la lista con el menú contextual ' ver ' ](images/ctrl-list-views-image18.png)

En este ejemplo, se usa un menú contextual de vista para cambiar las vistas.

### <a name="details-views"></a>Vistas de detalles

-   **Considere la posibilidad de usar la vista mosaicos para mejorar la legibilidad.**

    **Aceptable:**

    ![captura de pantalla de la lista de detalles con columnas estrechas ](images/ctrl-list-views-image19.png)

    En este ejemplo, hay demasiados datos y la ventana, la lista y las columnas son demasiado pequeñas, lo que dificulta la lectura de los elementos de la lista.

    **Manera**

    ![captura de pantalla de la lista de detalles con datos en grupos ](images/ctrl-list-views-image20.png)

    En este ejemplo, la vista en mosaico muestra los datos sin truncamiento.

-   **Elija los anchos de columna predeterminados adecuados para los datos más largos.** Las vistas de lista truncan automáticamente los datos largos con elipses, por lo que los anchos de columna son apropiados si se muestran pocos puntos suspensivos de forma predeterminada. Aunque los usuarios pueden cambiar el tamaño de las columnas, prefieren otras soluciones:

    -   Ajuste el ancho de cada columna para ajustarse a sus datos.
    -   Ajuste el ancho del control para ajustarse a sus columnas y a las barras de desplazamiento más probables.
    -   Si es necesario, utilice el desplazamiento horizontal.
    -   Los datos se han truncado solo para los elementos de tamaño impar o como último recurso.

    Si los datos de tamaño normal deben truncarse de forma predeterminada, se puede cambiar el tamaño de la vista de ventana y de lista. Incluya un 30% adicional (hasta el 200 por ciento para el texto más corto) para cualquier texto (pero no para los números) que se traducirá.

    **Incorrecto:**

    ![captura de pantalla de las columnas de lista con datos truncados ](images/ctrl-list-views-image21.png)

    En este ejemplo, la mayoría de los datos se truncan. Los muchos puntos suspensivos indican claramente que los anchos de los controles y las columnas son demasiado pequeños para los datos.

    **Incorrecto:**

    ![captura de pantalla de una lista de una columna con datos truncados ](images/ctrl-list-views-image22.png)

    En este ejemplo, los datos se truncan sin motivo.

-   **Elija un orden de columna predeterminado adecuado.** Por lo general, ordene las columnas de la manera siguiente:

    -   En primer lugar, el nombre del elemento o los datos de identificación.
    -   A continuación, otros datos resultan útiles para diferenciar los elementos de la lista.
    -   A continuación, los datos más útiles (preferiblemente de longitud corta o fija).
    -   Siguiente, menos útil (datos cortos o de longitud fija).
    -   Datos de longitud variable, último y largo.

    Long, longitud variable: los datos se colocan en las últimas columnas para reducir la necesidad de desplazamiento horizontal. Dentro de estas categorías, coloque la información relacionada en una secuencia lógica.

-   **Cuando sea necesario, permita a los usuarios agregar y quitar columnas, así como cambiar el orden.** Mostrar las columnas más útiles de forma predeterminada. Esto se logra con el atributo de arrastrar y colocar del encabezado.
-   Elija una alineación adecuada para los datos. Use las siguientes reglas:
    -   Alinear a la derecha números, monedas y horas.
    -   Alinear a la izquierda el texto, los identificadores (incluso si son numéricos) y las fechas.
-   En el caso de los encabezados de columna que se ordenan, **el primer clic en un encabezado ordena la lista en orden ascendente para la columna; el segundo clic se ordena en orden descendente.** Use el criterio de ordenación anterior (de otra columna) como clave de ordenación secundaria.

    ![captura de pantalla de la lista de detalles con datos ordenados ](images/ctrl-list-views-image23.png)

    En este ejemplo, se hizo clic primero en la columna Nombre y, a continuación, en la columna tipo. Como resultado, el tipo en orden ascendente es el criterio de ordenación principal y el nombre en orden ascendente es el secundario.

-   **Use el atributo seleccionar fila completa** para que los usuarios puedan determinar fácilmente los elementos seleccionados en todas las columnas.
-   **No use un encabezado de columna que se pueda ordenar a menos que se puedan ordenar los datos.**
-   **No use un encabezado de columna si solo hay una columna y no es necesario realizar una ordenación inversa.** En su lugar, use una etiqueta para identificar los datos.

    **Incorrecto:**

    ![captura de pantalla de la lista con la etiqueta en el encabezado de columna ](images/ctrl-list-views-image24.png)

    **Correcto:**

    ![captura de pantalla de la lista con la etiqueta encima del control ](images/ctrl-list-views-image25.png)

    En el ejemplo correcto, se usa una etiqueta en lugar de un encabezado de columna.

## <a name="recommended-sizing-and-spacing"></a>Ajuste de tamaño y espaciado recomendados

![captura de pantalla de tamaño y espaciado de la lista ](images/ctrl-list-views-image26.png)

Ajuste de tamaño y espaciado recomendados para las vistas de lista.

-   **Elija un alto de la vista de lista que muestre un número entero de elementos.** Evite truncar elementos verticalmente.
-   **Elija un tamaño de vista de lista que elimine el desplazamiento horizontal y vertical innecesario en todas las vistas admitidas.** Las vistas de lista deben mostrar entre 3 y 20 elementos. Considere la posibilidad de hacer que una vista de lista sea ligeramente más grande si al hacerlo se elimina una barra de desplazamiento. Las listas con potencialmente muchos elementos deben mostrar al menos cinco elementos para facilitar el desplazamiento al mostrar más elementos a la vez y facilitar la posición de la barra de desplazamiento.
-   **Si los usuarios se benefician de aumentar la vista de la lista, haga que la vista de lista y su ventana primaria sean ajustables.** Esto permite a los usuarios ajustar el tamaño de la vista de lista según sea necesario. Sin embargo, las vistas de lista de tamaño variable no deben mostrar menos de tres elementos.

## <a name="labels"></a>Etiquetas

### <a name="control-labels"></a>Etiquetas de control

-   Todas las vistas de lista necesitan etiquetas. Escriba la etiqueta como una palabra o frase, no como una frase, y termine con un signo de dos puntos usando texto estático.
-   Asigne una [clave de acceso](glossary.md) única para cada etiqueta. Para obtener instrucciones, consulte [teclado](inter-keyboard.md).
-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
-   Coloque la etiqueta encima del control y alinee la etiqueta con el borde izquierdo del control.
-   En el caso de las vistas de lista de selección múltiple, escriba la etiqueta que indica claramente es posible la selección múltiple. Las etiquetas de la vista de lista de casillas pueden ser menos explícitas.

    **Correcto:**

    ![captura de pantalla de la etiqueta: Seleccione uno o varios complementos. ](images/ctrl-list-views-image27.png)

    En este ejemplo, la etiqueta indica claramente que es posible la selección múltiple.

    **Incorrecto:**

    ![captura de pantalla de la etiqueta: complementos ](images/ctrl-list-views-image28.png)

    En este ejemplo, la etiqueta no proporciona información sobre la selección múltiple.

    **Aceptable:**

    ![captura de pantalla de la etiqueta de la lista de comprobación: complementos ](images/ctrl-list-views-image29.png)

    En este ejemplo, las casillas de verificación indican claramente que la selección múltiple es posible, por lo que la etiqueta no tiene que ser explícita.

-   Puede especificar unidades (segundos, conexiones, etc.) entre paréntesis después de la etiqueta.

### <a name="heading-labels"></a>Etiquetas de encabezado

-   Conserve los rótulos breves de las etiquetas de los títulos (tres palabras o menos).
-   Use un único nombre o frase sin puntuación final.
-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
-   Alinee el encabezado del mismo modo que los datos.

### <a name="group-labels"></a>Etiquetas de grupo

-   Use las siguientes etiquetas de grupo para las recopilaciones de alto nivel:
    -   Nombres: Use la primera letra del nombre o los intervalos de letras.
    -   Tamaños: sin especificar, 0 KB, 0-10 KB, 10-100 KB, 100 KB-1 MB, 1-16 MB, 16-128 MB
    -   Fechas: hoy, ayer, última semana, A principios de este año, y hace mucho tiempo.
-   De lo contrario, las etiquetas de grupo usan el texto exacto de los datos que se están agrupando, incluidas las mayúsculas y los signos de puntuación.

### <a name="data-text"></a>Texto de datos

-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).

### <a name="instructional-text"></a>Texto informativo

-   Si necesita agregar texto informativo sobre una vista de lista, agréguelo encima de la etiqueta. Use frases completas con una puntuación final.
-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
-   La información adicional que sea útil pero no necesaria debe mantenerse en breve. Coloque esta información entre paréntesis entre la etiqueta y el signo de dos puntos, o sin paréntesis debajo del control.

## <a name="documentation"></a>Documentación

Al hacer referencia a las vistas de lista:

-   Use el texto de etiqueta exacto, incluido el uso de mayúsculas, pero no incluya la tecla de acceso de subrayado ni dos puntos, e incluya la lista de palabras. No haga referencia a un cuadro de lista como un cuadro de lista, una vista de lista o un campo.
-   Para los datos de la lista, use el texto exacto de los datos, incluido el uso de mayúsculas.
-   Consulte las vistas de lista como vistas de lista únicamente en programación y otra documentación técnica. En cualquier lugar, use la lista.
-   Para describir la interacción del usuario, use SELECT para los datos y haga clic en para los encabezados.
-   Siempre que sea posible, dé formato a la etiqueta y a las opciones de lista usando texto en negrita. De lo contrario, coloque la etiqueta y las opciones entre comillas solo si es necesario para evitar confusiones.

Ejemplo: en la lista **programas y servicios** , seleccione **compartir archivos e impresoras**.

Al hacer referencia a las casillas de una vista de lista:

-   Use el texto de etiqueta exacto, incluido el uso de mayúsculas, e incluya la palabra casilla. No incluya el carácter de subrayado de la tecla de acceso.
-   Para describir la interacción del usuario, use SELECT y Clear.
-   Siempre que sea posible, dé formato a la etiqueta usando texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.

Ejemplo: Active la casilla **subrayado** .

 

