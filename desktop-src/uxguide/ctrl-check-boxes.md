---
title: Casillas
description: Con una casilla, los usuarios tomarán una decisión entre dos opciones claramente opuestas.
ms.assetid: 7c39987d-807b-41c1-9788-65c3d468b976
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 29666991d0a0659f7ff3a95f12953504b70c6dc782049ac8d93d70df73afa5d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118040693"
---
# <a name="check-boxes"></a>Casillas

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Con una casilla, los usuarios tomarán una decisión entre dos opciones claramente opuestas. La etiqueta de casilla indica el estado seleccionado, mientras que el significado del estado borrado debe ser el opuesto inequívoco del estado seleccionado. Por lo tanto, solo se deben usar casillas para activar o desactivar una opción o para seleccionar o **anular la selección de un elemento.**

![captura de pantalla de una de las cuatro casillas seleccionadas ](images/ctrl-check-boxes-image1.png)

Un grupo típico de casillas.

> [!Note]  
> Las instrucciones relacionadas [con el diseño](vis-layout.md) se presentan en un artículo independiente.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿Se usa la casilla para activar o desactivar una opción o para seleccionar o anular la selección de un elemento?** Si no es así, usa otro control.
-   **¿Los estados seleccionados y borrados son opuestos claros e inequívocos?** Si no es así, use [botones](ctrl-radio-buttons.md) de radio o [una lista](/windows/desktop/uxguide/ctrl-drop) desplegable para poder etiquetar los estados de forma independiente.
-   **Cuando se usa en un grupo, ¿consta el grupo de opciones independientes, de las que los usuarios pueden elegir cero o más?** Si no es así, tenga en cuenta los controles para las opciones dependientes, como los botones de radio y las [vistas de árbol de casillas](ctrl-tree-views.md).
-   **Cuando se usa en un grupo, ¿consta el grupo de opciones dependientes, entre las que los usuarios deben elegir uno o varios?** Si es así, use un grupo de casillas y controle el error cuando no se seleccione ninguna de las opciones.
-   **¿El número de opciones de un grupo es 10 o menos?** Puesto que el espacio de pantalla utilizado es proporcional al número de opciones, mantenga el número de casillas en 10 o menos. Para más de 10 opciones, use una lista [de casillas](ctrl-list-boxes.md).
-   **¿Sería mejor un botón de radio?** Cuando las casillas solo son adecuadas para activar o desactivar una opción, se pueden usar botones de radio para opciones completamente diferentes. Si ambas soluciones son posibles:
    -   Use botones de radio si el significado de la casilla desactivada no es completamente obvio.

        **Incorrecto:**

        ![captura de pantalla de una casilla con la etiqueta horizontal ](images/ctrl-check-boxes-image2.png)

        En este ejemplo, la opción opuesta de Horizontal no está clara, por lo que la casilla no es una buena opción.

        **Correcto:**

        ![captura de pantalla de dos botones de radio ](images/ctrl-check-boxes-image3.png)

        En este ejemplo, las opciones no son opuestas, por lo que los botones de radio son la mejor opción.

    -   Use botones de radio en las páginas del asistente para borrar las alternativas, aunque una casilla sea aceptable de lo contrario.
    -   Use botones de radio si tiene suficiente espacio en la pantalla y las opciones son lo suficientemente importantes como para ser un buen uso de ese espacio de pantalla. De lo contrario, use una casilla o una lista desplegable.

        **Incorrecto:**

        ![captura de pantalla de los botones mostrar y no mostrar relación ](images/ctrl-check-boxes-image4.png)

        En este ejemplo, las opciones no son lo suficientemente importantes como para usar botones de radio.

        **Correcto:**

        ![captura de pantalla de la casilla con no mostrar el mensaje ](images/ctrl-check-boxes-image5.png)

        En este ejemplo, una casilla es un uso eficaz del espacio de pantalla para esta opción de periférico.

-   Use una casilla si hay otras casillas en la ventana.
-   **¿La opción presenta una opción de programa, en lugar de datos?** Los valores de la opción no deben basarse en el contexto ni en otros datos. Para los datos, use una lista de casillas o [una lista de selección múltiple](ctrl-list-boxes.md).

## <a name="usage-patterns"></a>Patrones de uso

Las casillas tienen varios patrones de uso:



|    Uso                                                                          |         Ejemplo                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Una opción individual** Se usa una sola casilla para seleccionar una opción individual. <br/>                                                                                                             | ![captura de pantalla de una casilla con recordatorios etiqueta ](images/ctrl-check-boxes-image6.png)<br/> Se usa una sola casilla para una opción individual.<br/>                                                                                                                                                                                                                                                                                                                        |
| **Opciones independientes (cero o más)** Se usa un grupo de casillas para seleccionar entre un conjunto de cero o más opciones.<br/>                                                                              | A diferencia de los controles de selección única, como los [botones de radio,](ctrl-radio-buttons.md)los usuarios pueden seleccionar cualquier combinación de opciones en un grupo de casillas.<br/> ![captura de pantalla de dos de tres casillas activadas ](images/ctrl-check-boxes-image7.png)<br/> Se usa un grupo de casillas para las opciones independientes.<br/>                                                                                                                                                  |
| **Opciones dependientes (una o varias)** También se puede usar un grupo de casillas para seleccionar entre un conjunto de una o varias opciones.<br/>                                                                         | **es posible que tenga que representar una selección de una o varias opciones dependientes.** Dado que microsoft?windows no tiene un control que admita directamente este tipo de entrada, la mejor solución es usar un grupo de casillas y controlar el error cuando no se selecciona ninguna de las opciones.<br/> ![captura de pantalla de una de las dos casillas activadas ](images/ctrl-check-boxes-image8.png)<br/> Se usa un grupo de casillas donde se debe seleccionar al menos un protocolo.<br/> |
| **Opción mixta** Además de sus estados seleccionados y desactivados, las casillas también tienen un estado mixto para varias selecciones para indicar que la opción está establecida para algunos objetos, pero no para todos.<br/> | ![captura de pantalla de una casilla azul sólido de solo lectura ](images/ctrl-check-boxes-image9.png)<br/> Casilla de verificación de estado mixto.<br/>                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Casillas relacionadas con el grupo**. Combine opciones relacionadas y separe las opciones no relacionadas en grupos de 10 o menos, mediante varios grupos si es necesario.

    ![captura de pantalla de casillas relacionadas y no relacionadas ](images/ctrl-check-boxes-image10.png)

    Un ejemplo de grupos de opciones relacionadas e independientes.

-   **El uso de cuadros de grupo para organizar grupos de casillas** suele dar lugar a un desorden innecesario en la pantalla.
-   **Active las casillas en** un orden lógico, como agrupar opciones muy relacionadas, colocar primero las opciones más comunes o seguir alguna otra progresión natural. No se recomienda el orden alfabético porque depende del idioma y, por tanto, no se puede localizar.
-   **Alinee las casillas verticalmente, no horizontalmente.** La alineación horizontal es más difícil de leer.

    **Correcto:**

    ![captura de pantalla de casillas alineadas verticalmente ](images/ctrl-check-boxes-image11.png)

    En este ejemplo, las casillas están alineadas correctamente.

    **Incorrecto:**

    ![captura de pantalla de casillas alineadas horizontalmente ](images/ctrl-check-boxes-image12.png)

    En este ejemplo, la alineación horizontal es más difícil de leer.

-   **No use el estado mixto para representar un tercer estado.** El estado mixto se usa para indicar que se establece una opción para algunos objetos secundarios, pero no para todos. Los usuarios no deben poder establecer un estado mixto directamente, sino que el estado mixto es un reflejo de los objetos secundarios. El estado mixto no se usa como tercer estado para un elemento individual. Para representar un tercer estado, use botones de radio o una lista desplegable en su lugar.

    **Incorrecto:**

    ![captura de pantalla del servicio de tema azul sólido ](images/ctrl-check-boxes-image13.png)

    En este ejemplo, se supone que el estado mixto indica que el servicio Theme no está instalado.

    **Correcto:**

    ![captura de pantalla de la lista desplegable con tres opciones ](images/ctrl-check-boxes-image14.png)

    En este ejemplo, los usuarios pueden elegir entre una lista de tres opciones claras.

-   **Al hacer clic en una casilla de estado mixto, debe recorrer todos los estados seleccionados, todos desactivados y los estados mixtos originales.** Por motivos de restauración, es importante poder restaurar el estado mixto original porque la configuración puede ser compleja o desconocida para el usuario. De lo contrario, la única manera de restaurar el estado mixto con confianza sería cancelar la tarea e iniciar de nuevo.
-   **No use casillas como indicador de progreso.** En su lugar, use un control [de indicador](progress-bars.md) de progreso.

    **Incorrecto:**

    ![captura de pantalla de cuatro casillas que muestran el progreso ](images/ctrl-check-boxes-image15.png)

    En este ejemplo, las casillas se usan incorrectamente como indicador de progreso.

    **Correcto:**

    ![captura de pantalla de una barra de progreso parcialmente rellenada ](images/ctrl-check-boxes-image16.png)

    Ejemplo de una barra de progreso típica.

-   **Mostrar las casillas deshabilitadas con el estado de selección correcto.** Aunque los usuarios no puedan cambiarlos, las casillas deshabilitadas transmiten información para que sean coherentes con los resultados.

    **Incorrecto:**

    ![captura de pantalla de una de las dos casillas atenuadas ](images/ctrl-check-boxes-image17.png)

    En este ejemplo, se debe borrar la opción "Leer siempre en voz alta esta sección" porque la sección no se lee cuando la opción está deshabilitada.

-   **No use la selección de una casilla para**:
    -   Realice comandos.
    -   Mostrar otras ventanas, como un cuadro de diálogo para recopilar más entradas.
    -   Mostrar dinámicamente otros controles relacionados con el control seleccionado (los lectores de pantalla no pueden detectar tales eventos).

### <a name="dont-show-this-item-again"></a>No mostrar esto <item> Otra vez

-   **Considere la posibilidad de usar una opción No volver a mostrar esta opción para permitir a los usuarios suprimir un cuadro de diálogo periódico solo si no <item> hay una alternativa mejor.** Intente determinar de antemano si los usuarios realmente necesitan el cuadro de diálogo. Si lo hace, muestre siempre el diálogo y, si no lo hace, elimine el diálogo.

Para obtener más instrucciones y ejemplos, vea [Cuadros de diálogo](win-dialog-box.md).

### <a name="subordinate-controls"></a>Controles subordinados

-   Coloque los controles subordinados a la derecha de o debajo (con sangría, vaciar con la etiqueta de casilla) la casilla y su etiqueta. Finalice la etiqueta de casilla con dos puntos.

    ![captura de pantalla del cuadro de texto debajo de la etiqueta de la casilla ](images/ctrl-check-boxes-image18.png)

    En este ejemplo, la casilla y su control subordinado comparten la etiqueta de casilla y su clave de acceso.

-   **Deje habilitados los cuadros de texto editables dependientes y las listas desplegables si comparten la etiqueta de la casilla.** Cuando los usuarios escriban o peguen algo en el cuadro, seleccione automáticamente la opción correspondiente. Esto simplifica la interacción.

    ![captura de pantalla de cuadros de texto de encabezado y pie de página ](images/ctrl-check-boxes-image19.png)

    En este ejemplo, si se escribe un encabezado o un pie de página, se selecciona automáticamente la opción .

-   Si anida casillas con botones de radio u otras casillas, **deshabilite** estos controles subordinados hasta que se seleccione la opción de alto nivel . Al hacerlo, se evita la confusión sobre el significado de los controles subordinados.
-   Haga que los controles subordinados en una casilla contigua con la casilla en el orden de tabulación.
-   **Si la selección de una opción implica la selección de casillas subordinadas, active explícitamente esas casillas para que la relación sea clara.**

    **Incorrecto:**

    ![captura de pantalla: botón seleccionado, casillas desactivadas ](images/ctrl-check-boxes-image20.png)

    En este ejemplo, no se seleccionan las casillas subordinadas.

    **Correcto:**

    ![captura de pantalla: botón seleccionado, casillas seleccionadas ](images/ctrl-check-boxes-image21.png)

    En este ejemplo, se seleccionan las casillas subordinadas, lo que hace que su relación con la opción seleccionada esté clara.

-   **Use las casillas dependientes si las alternativas agregan complejidad innecesaria.** Aunque las casillas deben ser opciones independientes, a veces alternativas como los botones de radio agregan complejidad innecesaria.

    **Correcto:**

    ![captura de pantalla de botones y casillas confusos ](images/ctrl-check-boxes-image22.png)

    En este ejemplo, el uso de botones de radio es preciso, pero crea complejidad innecesaria.

    **Mejor:**

    ![captura de pantalla de las casillas solo ](images/ctrl-check-boxes-image23.png)

    En este ejemplo, el uso de casillas es más sencillo y permite a los usuarios centrarse en seleccionar las opciones deseadas en lugar de en su relación compleja.

    **Importante: Aplique esta directriz solo en circunstancias** extremadamente poco frecuentes, al mostrar las dependencias agrega una complejidad significativa sin agregar claridad. En el ejemplo anterior, es poco probable que los usuarios intenten elegir superíndice y subíndice, y si lo hacen, sería fácil entender que eran opciones exclusivas.

### <a name="default-values"></a>Valores predeterminados

-   Si una casilla es para una opción de usuario, establezca el estado más seguro (para evitar la pérdida de datos o del sistema), el estado más seguro y privado **de forma predeterminada.** Si la seguridad y la seguridad no son factores, seleccione el valor más probable o práctico.

## <a name="recommended-sizing-and-spacing"></a>Tamaño y espaciado recomendados

![figura de tamaño y espaciado sugeridos de la casilla ](images/ctrl-check-boxes-image24.png)

Tamaño y espaciado recomendados para las casillas.

## <a name="labels"></a>Etiquetas

**Etiquetas de casilla**

-   Etiquete cada casilla.
-   Asigne una clave [de acceso única](glossary.md) a cada etiqueta. Para obtener instrucciones, vea [Teclado.](inter-keyboard.md)
-   Use [mayúsculas de estilo oración.](glossary.md)
-   Escriba la etiqueta como frase o frase imperativa y no use ningún signo de puntuación final.
    -   **Excepción:** Si una etiqueta de casilla también etiqueta un control subordinado que le sigue, finalice la etiqueta con dos puntos.
-   Escriba la etiqueta para que describa el estado seleccionado de la casilla.
-   Para un grupo de casillas, use expresiones paralelas e intente mantener la longitud aproximadamente igual para todas las etiquetas.
-   Para un grupo de casillas, centre el texto de la etiqueta en las diferencias entre las opciones. Si todas las opciones tienen el mismo texto introductorio, mueva ese texto a la etiqueta de grupo.
-   Use expresiones positivas. No frasee una etiqueta para que al activar una casilla no se realice una acción.

    -   **Excepción: no vuelva a mostrar esta <item> casilla.**

    **Incorrecto:**

    ![captura de pantalla de la etiqueta negativa 'turn off'](images/ctrl-check-boxes-image25.png)

    En este ejemplo, la opción no usa expresiones positivas.

-   Describa solo la opción con la etiqueta . Mantenga las etiquetas breves para que sea fácil hacer referencia a ellas en mensajes y documentación. Si la opción requiere una explicación adicional, proporcione la explicación en un [control](./glossary.md) de texto estático mediante oraciones completas y signos de puntuación finales.

    > [!Note]
    >
    > Agregar una explicación a una casilla de un grupo no significa que tenga que proporcionar explicaciones para todas las casillas del grupo. Proporcione la información pertinente en la etiqueta si es posible y use explicaciones solo cuando sea necesario. No vuelva a establecer simplemente la etiqueta para mantener la coherencia.

     

    ![captura de pantalla de casilla, etiqueta y descripción ](images/ctrl-check-boxes-image26.png)

    En este ejemplo, una etiqueta de casilla tiene texto explicativo adicional debajo.

-   Si se recomienda encarecidamente una opción, considere la posibilidad de agregar "(recommended)" a la etiqueta. Asegúrese de agregar a la etiqueta de control, no a las notas complementarias.
-   Si debe usar etiquetas de varias líneas, alinee la parte superior de la etiqueta con la casilla.
-   No use un control subordinado, los valores que contiene o su etiqueta de unidades para crear una frase o frase. Este diseño no es localizable porque la estructura de oraciones varía según el lenguaje.

    **Incorrecto:**

    ![captura de pantalla de la etiqueta de casilla con un cuadro de texto ](images/ctrl-check-boxes-image27.png)

    En este ejemplo, el cuadro de texto se coloca incorrectamente dentro de la etiqueta de casilla.

**Etiquetas de grupo de casillas**

-   Use la etiqueta de grupo para explicar el propósito del grupo, no cómo realizar la selección. Supongamos que los usuarios saben cómo usar las casillas. Por ejemplo, no diga "Seleccionar cualquiera de las siguientes opciones".
-   Termine cada etiqueta con dos puntos.
-   No asigne una clave de acceso a la etiqueta. No es necesario hacerlo y dificulta la asignación de las otras claves de acceso.
-   Para una selección de una o varias opciones dependientes, explique el requisito en la etiqueta.

    **Correcto:**

    ![captura de pantalla de la etiqueta para dos controles: protocolos ](images/ctrl-check-boxes-image28.png)

    En este ejemplo, los usuarios podrían pensar que solo pueden realizar una selección.

    **Mejor:**

    ![captura de pantalla de la etiqueta: los protocolos seleccionan uno o varios ](images/ctrl-check-boxes-image29.png)

    En este ejemplo, está claro que los usuarios pueden realizar más de una selección.

## <a name="documentation"></a>Documentación

Al hacer referencia a las casillas:

-   Use el texto exacto de la etiqueta, incluida su mayúscula, pero no incluya el carácter de subrayado o dos puntos de la clave de acceso. Incluya la casilla de palabras.
-   Consulte una casilla como una casilla, no una opción, una casilla o simplemente una casilla, porque la casilla por sí sola es ambigua para los localizadores.
-   Para describir la interacción del usuario, use seleccionar y borrar.
-   Cuando sea posible, formatee la etiqueta con texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.

    Ejemplo: active la **casilla Subrayado.**

