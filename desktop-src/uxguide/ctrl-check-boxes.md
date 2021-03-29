---
title: Casillas
description: Con una casilla, los usuarios deciden elegir entre dos opciones claramente opuestas.
ms.assetid: 7c39987d-807b-41c1-9788-65c3d468b976
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7a175893b2dfab2999ce37e3f00395d881f03973
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104003284"
---
# <a name="check-boxes"></a>Casillas

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Con una casilla, los usuarios deciden elegir entre dos opciones claramente opuestas. La etiqueta de la casilla indica el estado seleccionado, mientras que el significado del estado desactivado debe ser el opuesto no ambiguo del estado seleccionado. Por lo tanto, las **casillas solo deben usarse para activar o desactivar una opción o para seleccionar o anular la selección de un elemento.**

![captura de pantalla de una de las cuatro casillas seleccionadas ](images/ctrl-check-boxes-image1.png)

Un grupo de casillas típico.

> [!Note]  
> Las instrucciones relacionadas con el [diseño](vis-layout.md) se presentan en un artículo independiente.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿Está activada o desactivada la casilla usada para activar o desactivar una opción o para seleccionar o anular la selección de un elemento?** Si no es así, usa otro control.
-   **¿Están los Estados seleccionados y desactivados claros y no ambiguos?** Si no es así, use los [botones de radio](ctrl-radio-buttons.md) o una [lista](/windows/desktop/uxguide/ctrl-drop) desplegable para que pueda etiquetar los Estados de forma independiente.
-   **Cuando se usa en un grupo, ¿el grupo comprende opciones independientes, desde las que los usuarios pueden elegir cero o más?** Si no es así, tenga en cuenta los controles para las opciones dependientes, como los botones de radio y las [vistas de árbol de casilla](ctrl-tree-views.md).
-   **Cuando se usa en un grupo, ¿comprende el grupo las elecciones dependientes, desde las que los usuarios deben elegir una o más?** Si es así, use un grupo de casillas y controle el error cuando no se seleccione ninguna de las opciones.
-   **¿El número de opciones de un grupo es 10 o menos?** Dado que el espacio de pantalla utilizado es proporcional al número de opciones, mantenga el número de casillas en 10 o menos. Para más de 10 opciones, use una [lista de casillas](ctrl-list-boxes.md).
-   **¿Sería un botón de radio una opción mejor?** En los casos en los que las casillas son adecuadas solo para activar o desactivar una opción, los botones de radio se pueden usar para opciones totalmente diferentes. Si ambas soluciones son posibles:
    -   Use los botones de radio si el significado de la casilla desactivada no es completamente obvio.

        **Incorrecto:**

        ![captura de pantalla de una casilla con la etiqueta horizontal ](images/ctrl-check-boxes-image2.png)

        En este ejemplo, la opción opuesta de horizontal no está clara, por lo que la casilla no es una buena opción.

        **Correcto:**

        ![captura de pantalla de dos botones de radio ](images/ctrl-check-boxes-image3.png)

        En este ejemplo, las opciones no son opuestas, por lo que los botones de radio son la mejor opción.

    -   Use los botones de radio de las páginas del Asistente para desactivar las alternativas, incluso si la casilla de verificación es aceptable.
    -   Use los botones de radio si tiene suficiente espacio de pantalla y las opciones son lo suficientemente importantes como para ser un buen uso de ese espacio de la pantalla. De lo contrario, use una casilla o una lista desplegable.

        **Incorrecto:**

        ![captura de pantalla de los botones Mostrar y no mostrar relación ](images/ctrl-check-boxes-image4.png)

        En este ejemplo, las opciones no son lo suficientemente importantes para usar botones de radio.

        **Correcto:**

        ![captura de pantalla de la casilla con no mostrar mensaje ](images/ctrl-check-boxes-image5.png)

        En este ejemplo, una casilla es un uso eficaz del espacio de pantalla para esta opción de periféricos.

-   Utilice una casilla de verificación si hay otras casillas en la ventana.
-   **¿La opción presenta una opción de programa, en lugar de datos?** Los valores de la opción no deben basarse en el contexto u otros datos. Para los datos, use una lista de casillas o una [lista de selección múltiple](ctrl-list-boxes.md).

## <a name="usage-patterns"></a>Patrones de uso

Las casillas tienen varios patrones de uso:



|                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Una opción individual** Se utiliza una sola casilla para seleccionar una opción individual. <br/>                                                                                                             | ![captura de pantalla de una casilla con la etiqueta Recordármelo ](images/ctrl-check-boxes-image6.png)<br/> Se utiliza una sola casilla para una opción individual.<br/>                                                                                                                                                                                                                                                                                                                        |
| **Opciones independientes (cero o más)** Se usa un grupo de casillas para seleccionar entre un conjunto de cero o más opciones.<br/>                                                                              | a diferencia de los controles de selección única, como los [botones de radio](ctrl-radio-buttons.md), los usuarios pueden seleccionar cualquier combinación de opciones de un grupo de casillas.<br/> ![captura de pantalla de dos de las tres casillas seleccionadas ](images/ctrl-check-boxes-image7.png)<br/> Se utiliza un grupo de casillas de verificación para opciones independientes.<br/>                                                                                                                                                  |
| **Elecciones dependientes (una o más)** También se puede usar un grupo de casillas para seleccionar entre un conjunto de una o más opciones.<br/>                                                                         | es **posible que necesite representar una selección de una o varias opciones dependientes**. Dado que Microsoft? Windows no tiene un control que admita directamente este tipo de entrada, la mejor solución consiste en usar un grupo de casillas y controlar el error cuando no se selecciona ninguna de las opciones.<br/> ![captura de pantalla de una de las dos casillas seleccionadas ](images/ctrl-check-boxes-image8.png)<br/> Se usa un grupo de casillas donde se debe seleccionar al menos un protocolo.<br/> |
| **Elección mixta** Además de los Estados seleccionados y desactivados, las casillas también tienen un estado mixto para la selección múltiple para indicar que la opción está establecida para algunos objetos, pero no para todos.<br/> | ![captura de pantalla de una casilla de solo lectura azul sólido ](images/ctrl-check-boxes-image9.png)<br/> Una casilla de estado mixto.<br/>                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Casillas relacionadas con grupos**. Combine opciones relacionadas y separe las opciones no relacionadas en grupos de 10 o menos, utilizando varios grupos si es necesario.

    ![captura de pantalla de las casillas relacionadas y no relacionadas ](images/ctrl-check-boxes-image10.png)

    Un ejemplo de grupos de opciones relacionadas e independientes.

-   Volver **a considerar el uso de cuadros de grupo para organizar grupos de casillas** esto a menudo produce un desorden de pantalla innecesario.
-   **Mostrar las casillas en un orden lógico**, como agrupar las opciones de alta relación o colocar las opciones más comunes en primer lugar o seguir algún otro progresión natural. No se recomienda el orden alfabético porque depende del lenguaje y, por lo tanto, no es localizable.
-   **Alinee las casillas verticalmente, no horizontalmente**. La alineación horizontal es más difícil de leer.

    **Correcto:**

    ![captura de pantalla de las casillas alineadas verticalmente ](images/ctrl-check-boxes-image11.png)

    En este ejemplo, las casillas están correctamente alineadas.

    **Incorrecto:**

    ![captura de pantalla de las casillas alineadas horizontalmente ](images/ctrl-check-boxes-image12.png)

    En este ejemplo, la alineación horizontal es más difícil de leer.

-   **No use el estado mixto para representar un tercer Estado.** El estado mixto se usa para indicar que se ha establecido una opción para algunos objetos secundarios, pero no para todos. Los usuarios no deben poder establecer un estado mixto directamente en lugar de que el estado mixto sea un reflejo de los objetos secundarios. El estado mixto no se utiliza como tercer Estado para un elemento individual. Para representar un tercer Estado, use los botones de radio o una lista desplegable en su lugar.

    **Incorrecto:**

    ![captura de pantalla de la casilla servicio de tema azul sólido ](images/ctrl-check-boxes-image13.png)

    En este ejemplo, se supone que el estado mixto indica que el servicio de tema no está instalado.

    **Correcto:**

    ![captura de pantalla de la lista desplegable con tres opciones ](images/ctrl-check-boxes-image14.png)

    En este ejemplo, los usuarios pueden elegir entre una lista de tres opciones claras.

-   **Al hacer clic en una casilla de estado mixto, se recorren todos los Estados seleccionados, todos borrados y los originales.** En el caso de forgiveness, es importante poder restaurar el estado mixto original, ya que la configuración podría ser compleja o desconocida para el usuario. De lo contrario, la única manera de restaurar el estado mixto con confianza sería cancelar la tarea y volver a empezar.
-   **No use casillas como indicador de progreso**. En su lugar, use un control de [indicador de progreso](progress-bars.md) .

    **Incorrecto:**

    ![captura de pantalla de cuatro casillas que muestran el progreso ](images/ctrl-check-boxes-image15.png)

    En este ejemplo, las casillas se usan incorrectamente como un indicador de progreso.

    **Correcto:**

    ![captura de pantalla de una barra de progreso parcialmente rellena ](images/ctrl-check-boxes-image16.png)

    Ejemplo de una barra de progreso típica.

-   **Mostrar las casillas deshabilitadas con el estado de selección correcto.** Aunque los usuarios no pueden cambiarlos, las casillas deshabilitadas transmiten información para que sean coherentes con los resultados.

    **Incorrecto:**

    ![captura de pantalla de una de dos casillas atenuadas ](images/ctrl-check-boxes-image17.png)

    En este ejemplo, la opción "leer siempre esta sección en voz alta" debe borrarse porque la sección no se lee cuando la opción está deshabilitada.

-   **No use la selección de una casilla para**:
    -   Ejecutar comandos.
    -   Mostrar otras ventanas, como un cuadro de diálogo para recopilar más entradas.
    -   Mostrar de forma dinámica otros controles relacionados con el control seleccionado (los lectores de pantalla no pueden detectar dichos eventos).

### <a name="dont-show-this-item-again"></a>No mostrar esta <item> nuevo

-   **Considere la posibilidad de usar una <item> opción no volver a mostrar esto para permitir que los usuarios supriman un cuadro de diálogo periódico solo si no hay una alternativa mejor.** Intente determinar de antemano si los usuarios necesitan realmente el cuadro de diálogo; Si lo hacen, muestre siempre el cuadro de diálogo y, si no es así, elimine el cuadro de diálogo.

Para obtener más instrucciones y ejemplos, vea [cuadros de diálogo](win-dialog-box.md).

### <a name="subordinate-controls"></a>Controles subordinados

-   Coloque los controles subordinados a la derecha o debajo de (con sangría, vacíe con la etiqueta de la casilla) la casilla de verificación y su etiqueta. Finalice la etiqueta de la casilla con un signo de dos puntos.

    ![captura de pantalla del cuadro de texto debajo de la etiqueta de la casilla ](images/ctrl-check-boxes-image18.png)

    En este ejemplo, la casilla y su control subordinado comparten la etiqueta de la casilla y su clave de acceso.

-   **Deje las listas desplegables y los cuadros de texto modificables dependientes habilitados si comparten la etiqueta de la casilla.** Cuando los usuarios escriban o peguen cualquier elemento en el cuadro, seleccione automáticamente la opción correspondiente. De este modo, se simplifica la interacción.

    ![captura de pantalla de cuadros de texto de encabezado y pie de página ](images/ctrl-check-boxes-image19.png)

    En este ejemplo, al escribir un encabezado o un pie de página, se selecciona automáticamente la opción.

-   Si anida casillas con botones de radio u otras casillas, **deshabilite estos controles subordinados hasta que se seleccione la opción de alto nivel**. Al hacerlo, se evita la confusión sobre el significado de los controles subordinados.
-   Active la casilla de verificación de los controles subordinados junto con la casilla en el orden de tabulación.
-   **Si la selección de una opción implica seleccionar las casillas subordinadas, active las casillas de verificación de forma explícita para que la relación sea clara.**

    **Incorrecto:**

    ![captura de pantalla: botón seleccionado, casillas desactivadas ](images/ctrl-check-boxes-image20.png)

    En este ejemplo, las casillas subordinadas no están seleccionadas.

    **Correcto:**

    ![captura de pantalla: botón seleccionado, casillas seleccionadas ](images/ctrl-check-boxes-image21.png)

    En este ejemplo, se seleccionan las casillas subordinadas, haciendo que su relación con la opción seleccionada esté desactivada.

-   **Use casillas dependientes si las alternativas agregan complejidad innecesaria**. Las casillas de verificación deben ser opciones independientes, a veces alternativas como los botones de radio agregan complejidad innecesaria.

    **Correcto:**

    ![captura de pantalla de botones y casillas confusos ](images/ctrl-check-boxes-image22.png)

    En este ejemplo, el uso de botones de radio es preciso, pero crea una complejidad innecesaria.

    **Manera**

    ![captura de pantalla de solo casillas ](images/ctrl-check-boxes-image23.png)

    En este ejemplo, el uso de casillas es más sencillo y permite a los usuarios centrarse en seleccionar las opciones deseadas en lugar de en su relación compleja.

    **Importante: aplique esta directriz solo en circunstancias muy poco habituales**. al mostrar las dependencias, se agrega una complejidad significativa sin agregar claridad. En el ejemplo anterior, es improbable que los usuarios intentaran elegir superíndices y subíndices, y si lo hicieron, sería fácil entender que eran opciones exclusivas.

### <a name="default-values"></a>Valores predeterminados

-   Si una casilla está desactivada para una opción de usuario, **establezca la más segura (para evitar la pérdida de datos o el acceso al sistema), el estado más seguro y privado de forma predeterminada.** Si seguridad y seguridad no son factores, seleccione el valor más probable o adecuado.

## <a name="recommended-sizing-and-spacing"></a>Ajuste de tamaño y espaciado recomendados

![figura del tamaño y espaciado de las casillas sugeridas ](images/ctrl-check-boxes-image24.png)

Ajuste de tamaño y espaciado recomendados para las casillas.

## <a name="labels"></a>Etiquetas

**Etiquetas de casilla**

-   Etiquetar cada casilla.
-   Asigne una [clave de acceso](glossary.md) única a cada etiqueta. Para obtener instrucciones, consulte [teclado](inter-keyboard.md).
-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
-   Escriba la etiqueta como una frase o frase imperativa y no use ningún signo de puntuación final.
    -   **Excepción:** Si una etiqueta de casilla también etiqueta un control subordinado que lo sigue, finalice la etiqueta con un signo de dos puntos.
-   Escriba la etiqueta para que describa el estado seleccionado de la casilla.
-   En el caso de un grupo de casillas, use la formulación paralela e intente mantener la misma longitud para todas las etiquetas.
-   En un grupo de casillas, Centre el texto de la etiqueta en las diferencias entre las opciones. Si todas las opciones tienen el mismo texto de introducción, mueva el texto a la etiqueta de grupo.
-   Usar frases positivas. No formule frases como una etiqueta, de modo que la selección de una casilla significa no realizar una acción.

    -   **Excepción: no <item> volver a mostrar** las casillas.

    **Incorrecto:**

    ![captura de pantalla de la etiqueta negativa ' desactivar '](images/ctrl-check-boxes-image25.png)

    En este ejemplo, la opción no usa frases positivas.

-   Describa solo la opción con la etiqueta. Conserve las etiquetas breves, por lo que es fácil hacer referencia a ellas en los mensajes y la documentación. Si la opción requiere una explicación más detallada, proporcione la explicación en un control de [texto estático](./glossary.md) mediante frases completas y puntuación final.

    > [!Note]
    >
    > Agregar una explicación a una casilla de un grupo no significa que tenga que proporcionar explicaciones para todas las casillas del grupo. Proporcione la información relevante en la etiqueta, si es posible, y use explicaciones solo cuando sea necesario. No solo tiene que volver a cambiar el estado de la etiqueta para que sea coherente.

     

    ![captura de pantalla de casilla, etiqueta y descripción ](images/ctrl-check-boxes-image26.png)

    En este ejemplo, una etiqueta de casilla tiene texto explicativo adicional debajo de ella.

-   Si se recomienda encarecidamente, considere la posibilidad de agregar "(recomendado)" a la etiqueta. Asegúrese de agregar a la etiqueta de control, no a las notas complementarias.
-   Si debe usar etiquetas de varias líneas, alinee la parte superior de la etiqueta con la casilla.
-   No utilice un control subordinado, los valores que contiene o su etiqueta de unidades para crear una frase o frase. Este tipo de diseño no es localizable porque la estructura de oraciones varía según el idioma.

    **Incorrecto:**

    ![captura de pantalla de la etiqueta de la casilla con el cuadro de texto en ella ](images/ctrl-check-boxes-image27.png)

    En este ejemplo, el cuadro de texto se coloca incorrectamente dentro de la etiqueta de la casilla.

**Etiquetas de grupo de casillas**

-   Use la etiqueta de grupo para explicar el propósito del grupo, no cómo hacer la selección. Supongamos que los usuarios saben cómo usar las casillas. Por ejemplo, no indique "Seleccione cualquiera de las siguientes opciones".
-   Finalice cada etiqueta con un signo de dos puntos.
-   No asigne una clave de acceso a la etiqueta. Esto no es necesario y hace que las demás claves de acceso sean más difíciles de asignar.
-   Para obtener una selección de una o varias opciones dependientes, explique el requisito de la etiqueta.

    **Correcto:**

    ![captura de pantalla de la etiqueta de dos controles: protocolos ](images/ctrl-check-boxes-image28.png)

    En este ejemplo, los usuarios pueden creer que solo pueden hacer una selección.

    **Manera**

    ![captura de pantalla de la etiqueta: los protocolos seleccionan uno o varios ](images/ctrl-check-boxes-image29.png)

    En este ejemplo, está claro que los usuarios pueden hacer más de una selección.

## <a name="documentation"></a>Documentación

Al hacer referencia a las casillas:

-   Use el texto de etiqueta exacto, incluido el uso de mayúsculas, pero no incluya el carácter de subrayado de la tecla de acceso o el signo de dos puntos. Incluya la palabra casilla.
-   Haga referencia a una casilla de verificación como casilla, no como opción, casilla o simplemente cuadro, ya que Box solo es ambiguo para los localizadores.
-   Para describir la interacción del usuario, use SELECT y Clear.
-   Siempre que sea posible, dé formato a la etiqueta usando texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.

    Ejemplo: Active la casilla **subrayado** .

