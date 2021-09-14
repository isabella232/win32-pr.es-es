---
title: Botones de radio
description: Con un botón de radio, los usuarios pueden elegir entre un conjunto de opciones relacionadas mutuamente excluyentes.
ms.assetid: f9af0a8a-d4a1-464c-a967-bab88ae0726b
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 00495695753506702015431c889e74d5a7effe9a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267495"
---
# <a name="radio-buttons"></a>Botones de radio

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Con un botón de radio, los usuarios pueden elegir entre un conjunto de opciones relacionadas mutuamente excluyentes. Los usuarios pueden elegir una única opción. Los botones de radio se llaman así porque funcionan como los valores preestablecidos del canal en las radios.

![captura de pantalla de tres botones de radio ](images/radio-buttons-image1.png)

Un grupo típico de botones de radio.

Un grupo de botones de radio se comporta como un control único. Solo se puede acceder a la opción seleccionada mediante la tecla Tab, pero los usuarios pueden recorrer el grupo mediante las teclas de dirección.

> [!Note]  
> Las instrucciones relacionadas con [el diseño](vis-layout.md) y la [navegación mediante](inter-keyboard.md) teclado se presentan en un artículo independiente.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿Se usa el control para elegir una opción de un conjunto de opciones mutuamente excluyentes?** Si no es así, usa otro control. Para elegir varias opciones, use las [casillas](ctrl-check-boxes.md), una [lista de selección múltiple](ctrl-list-boxes.md) o una lista de casillas en su lugar.
-   **¿El número de opciones está entre dos y siete?** Puesto que el espacio de pantalla utilizado es proporcional al número de opciones, mantenga el número de opciones de un grupo entre dos y siete. Para ocho o más opciones, use [una lista desplegable o](/windows/desktop/uxguide/ctrl-drop) una lista de selección [única](ctrl-list-boxes.md).
-   **¿Sería mejor una casilla?** Si solo hay dos opciones, puede usar una sola [casilla en su](ctrl-check-boxes.md) lugar. Sin embargo, las casillas solo son adecuadas para activar o desactivar una única opción, mientras que los botones de radio se pueden usar para alternativas completamente diferentes. Si ambas soluciones son posibles:
    -   Use botones de radio si el significado de la casilla desactivada no es completamente obvio.

        **Incorrecto:**

        ![captura de pantalla de la casilla horizontal ](images/radio-buttons-image2.png)

        **Correcto:**

        ![captura de pantalla de botones de radio horizontal/vertical ](images/radio-buttons-image3.png)

        En el ejemplo correcto, las opciones no son opuestas, por lo que los botones de radio son la mejor opción.

    -   Use botones de radio en las páginas del asistente para borrar las alternativas, aunque una casilla sea aceptable de lo contrario.
    -   Use botones de radio si tiene suficiente espacio en la pantalla y las opciones son lo suficientemente importantes como para ser un buen uso de ese espacio de pantalla. De lo contrario, use una casilla o lista desplegable.

        **Incorrecto:**

        ![captura de pantalla de mostrar o no mostrar botones de radio ](images/radio-buttons-image4.png)

        En este ejemplo, las opciones no son lo suficientemente importantes como para usar botones de radio.

        **Correcto:**

        ![captura de pantalla de no mostrar esta casilla de mensaje ](images/radio-buttons-image5.png)

        En este ejemplo, una casilla es un uso eficaz del espacio de pantalla para esta opción de periférico.

    -   Use una casilla si hay otras casillas en la página.

-   **¿Sería mejor una lista desplegable?** Si se recomienda la opción predeterminada para la mayoría de los usuarios en la mayoría de las situaciones, los botones de radio podrían llamar más atención a las opciones de las necesarias.
    -   Considere la posibilidad de usar una lista desplegable si no desea llamar la atención sobre las opciones o no desea animar a los usuarios a realizar cambios. Una lista desplegable se centra en la selección actual, mientras que los botones de radio resaltan todas las opciones por igual.

        ![captura de pantalla de la máxima calidad como botón predeterminado ](images/radio-buttons-image6.png)

        En este ejemplo, una lista desplegable se centra en la selección actual y desaconseja que los usuarios realicen cambios.

    -   Considere una lista desplegable si hay otras listas desplegables en la página.

-   **¿Sería mejor un conjunto de botones de comando, vínculos de comandos o un botón de división?** Si los botones de radio solo se usan para afectar a cómo se realiza un comando, a menudo es mejor presentar las variaciones de comando en su lugar. Esto permite a los usuarios elegir el comando correcto con una sola interacción.
-   **¿Presentan las opciones del programa, en lugar de los datos?** Los valores de las opciones no deben basarse en el contexto ni en otros datos. Para los datos, use una lista desplegable o una lista de selección única.
-   Si el control se usa en una página del asistente o en un panel de control, ¿es el control una respuesta a la instrucción principal y los usuarios pueden **cambiar la opción más adelante?** Si es así, considere la posibilidad de usar vínculos de comandos en lugar de botones de radio para que la interacción sea más eficaz.
-   **¿Los valores no son numéricos?** Para los datos numéricos, use [cuadros de texto,](ctrl-text-boxes.md) [listas desplegables](/windows/desktop/uxguide/ctrl-drop)o [controles deslizantes](ctrl-sliders.md).

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Enumere las opciones** en un orden lógico, por ejemplo, con más probabilidad de que se seleccionen como mínimo, operación más sencilla a la más compleja o de menor riesgo a la mayoría. No se recomienda el orden alfabético porque depende del idioma y, por tanto, no es localizable.
-   **Si ninguna de las opciones es una opción válida, agregue** otra opción para reflejar esta opción, como Ninguno o No se aplica.
-   **Prefiere alinear los botones de radio verticalmente en lugar de horizontalmente.** La alineación horizontal es más difícil de leer y de encontrar.

    **Correcto:**

    ![captura de pantalla de alineación vertical del botón de radio ](images/radio-buttons-image7.png)

    En este ejemplo, los botones de radio se alinean verticalmente.

    **Incorrecto:**

    ![captura de pantalla de alineación horizontal del botón de radio ](images/radio-buttons-image8.png)

    En este ejemplo, la alineación horizontal es más difícil de leer.

-   **El uso de cuadros de grupo para organizar grupos de botones** de radio suele dar lugar a un desorden innecesario en la pantalla.
-   **No use etiquetas de botón de radio como etiquetas de cuadro de grupo.**
-   **No use la selección de un botón de radio para:**
    -   Realice comandos.
    -   Mostrar otras ventanas, como un cuadro de diálogo para recopilar más entradas.
    -   Mostrar u ocultar dinámicamente otros controles relacionados con el control seleccionado (los lectores de pantalla no pueden detectar dichos eventos). Sin embargo, puede cambiar el texto dinámicamente en función de la selección.

### <a name="subordinate-controls"></a>Controles subordinados

-   Coloque los controles subordinados a la derecha de o debajo (con sangría, vacíe con la etiqueta del botón de radio) el botón de radio y su etiqueta. Finalice la etiqueta del botón de radio con dos puntos.

    ![captura de pantalla del control a la derecha de su etiqueta ](images/radio-buttons-image9.png)

    En este ejemplo, el botón de radio y su control subordinado comparten la etiqueta del botón de radio y su clave de acceso. En este caso, las teclas de dirección mueven el foco desde el botón de radio a su cuadro de texto subordinado.

-   **Deje habilitados los cuadros de texto editables dependientes y las listas desplegables si comparten la etiqueta del botón de radio.** Cuando los usuarios escriban o peguen algo en el cuadro, seleccione automáticamente la opción correspondiente. Esto simplifica la interacción.

    ![captura de pantalla del cuadro de diálogo intervalo de páginas con cuadro de texto ](images/radio-buttons-image10.png)

    En este ejemplo, al escribir un número de página, se seleccionan páginas automáticamente.

-   **Evite anidar botones de radio con otros botones de radio o casillas.** Si es posible, mantenga todas las opciones en el mismo nivel.

    **Correcto:**

    ![captura de pantalla de botones de radio alineados a la izquierda ](images/radio-buttons-image11.png)

    En este ejemplo, las opciones están en el mismo nivel.

    **Incorrecto:**

    ![captura de pantalla de botones de radio anidados ](images/radio-buttons-image12.png)

    En este ejemplo, el uso de opciones anidadas agrega complejidad innecesaria.

-   Si anida botones de radio con otros botones de radio o casillas, deshabilite estos controles subordinados hasta que se seleccione **la opción de alto nivel.** Al hacerlo, se evita la confusión sobre el significado de los controles subordinados.

### <a name="default-values"></a>Valores predeterminados

-   Dado que un grupo de botones de radio representa un conjunto de opciones mutuamente excluyentes, siempre hay un **botón de radio seleccionado de forma predeterminada. Seleccione la opción más segura (para evitar la pérdida de datos** o el acceso al sistema) y la opción más segura y privada. Si la seguridad y la seguridad no son factores, seleccione la opción más probable o conveniente.
-   **Excepciones:** No tiene una selección predeterminada si:
    -   **No hay ninguna opción predeterminada aceptable por motivos de seguridad, seguridad o legales y, por tanto, el usuario debe tomar una decisión explícita.** Si el usuario no realiza una selección, muestre un mensaje de error para forzar uno.
    -   **La interfaz de usuario (UI) debe reflejar el estado actual y la opción aún no se ha establecido.** Un valor predeterminado implicaría incorrectamente que el usuario no necesita realizar una selección.
    -   **El objetivo es recopilar datos no sesados.** Los valores predeterminados se sesgados de la recopilación de datos.
    -   **El grupo de botones de radio** representa una propiedad en un estado mixto , lo que sucede cuando se muestra una propiedad para varios objetos que no tienen la misma configuración. No muestre un mensaje de error en este caso, ya que cada objeto tiene un estado válido.
-   **Haga que la primera opción sea la opción predeterminada**, ya que los usuarios lo esperan a menudo, a menos que ese orden no sea lógico. Para ello, es posible que tenga que cambiar las etiquetas de opción.

    **Incorrecto:**

    ![captura de pantalla del último botón de radio como opción predeterminada ](images/radio-buttons-image13.png)

    En este ejemplo, la opción predeterminada no es la primera opción.

    **Correcto:**

    ![captura de pantalla del primer botón de radio como valor predeterminado ](images/radio-buttons-image14.png)

    En este ejemplo, las etiquetas de opción se reetiquetó para convertir la primera opción en la opción predeterminada.

## <a name="recommended-sizing-and-spacing"></a>Tamaño y espaciado recomendados

![captura de pantalla del tamaño y espaciado del botón de radio ](images/radio-buttons-image15.png)

Tamaño y espaciado recomendados para botones de radio.

## <a name="labels"></a>Etiquetas

### <a name="radio-button-labels"></a>Etiquetas de botón de radio

-   Etiquete cada botón de radio.

<!-- -->

-   Asigne una clave [de acceso única](glossary.md) a cada etiqueta. Para obtener instrucciones, vea [Teclado.](inter-keyboard.md)
-   Use [mayúsculas de estilo oración.](glossary.md)
-   Escriba la etiqueta como una frase, no como una frase, y no use ningún signo de puntuación final.
    -   **Excepción:** Si una etiqueta de botón de radio también etiqueta un control subordinado que le sigue, finalice la etiqueta con dos puntos.
-   Use expresiones paralelas e intente mantener la longitud aproximadamente igual para todas las etiquetas.
-   Centre el texto de la etiqueta en las diferencias entre las opciones. Si todas las opciones tienen el mismo texto introductorio, mueva ese texto a la etiqueta de grupo.
-   Use expresiones positivas. Por ejemplo, use do en lugar de do, e print en lugar de no imprimir.
-   Describa solo la opción con la etiqueta . Mantenga las etiquetas breves para que sea fácil hacer referencia a ellas en mensajes y documentación. Si la opción requiere una explicación adicional, proporcione la explicación en un [control](glossary.md) de texto estático mediante oraciones completas y signos de puntuación finales.

    ![captura de pantalla de botones de radio con texto explicativo](images/radio-buttons-image16.png)

    En este ejemplo, las opciones se explican mediante controles de texto estático independientes.

    > [!Note]  
    > Agregar una explicación a un botón de radio no significa que tenga que proporcionar explicaciones para todos los botones de radio. Proporcione la información pertinente en la etiqueta si es posible y use explicaciones solo cuando sea necesario. No vuelva a establecer simplemente la etiqueta para mantener la coherencia.

     

-   **Si se recomienda encarecidamente una opción, agregue "(recommended)" a la etiqueta.** Asegúrese de agregar a la etiqueta de control, no a las notas complementarias.
-   **Si una opción está pensada solo para usuarios avanzados, agregue "(advanced)" a la etiqueta.** Asegúrese de agregar a la etiqueta de control, no a las notas complementarias.
-   Si debe usar etiquetas de varias líneas, alinee la parte superior de la etiqueta con el botón de radio.
-   No use un control subordinado, los valores que contiene o su etiqueta de unidades para crear una frase o frase. Este diseño no es localizable porque la estructura de oraciones varía según el lenguaje.

### <a name="radio-button-group-labels"></a>Etiquetas de grupo de botones de radio

-   Use la etiqueta de grupo para explicar el propósito del grupo, no cómo realizar la selección. Suponga que los usuarios saben cómo usar botones de radio. Por ejemplo, no diga "Seleccionar una de las siguientes opciones".
-   Todos los grupos de botones de radio necesitan etiquetas. Escriba la etiqueta como una palabra o frase, no como una frase, terminando con dos puntos mediante texto estático o un cuadro de grupo.

    **Excepción:** Omita la etiqueta si es simplemente una nueva instrucción de la instrucción principal de [un cuadro de diálogo.](glossary.md) En este caso, la instrucción principal toma los dos puntos (a menos que sea una pregunta) y la clave de acceso (si la hay).

    **Aceptable:**

    ![captura de pantalla de la etiqueta de grupo de botones de radio redundante ](images/radio-buttons-image17.png)

    En este ejemplo, la etiqueta del grupo de botones de radio es simplemente una nueva declaración de la instrucción principal.

    **Mejor:**

    ![captura de pantalla solo de la instrucción principal del botón de radio ](images/radio-buttons-image18.png)

    En este ejemplo, se quita la etiqueta redundante, por lo que la instrucción principal toma los dos puntos.

-   No asigne una clave de acceso a la etiqueta. No es necesario hacerlo y dificulta la asignación de las otras claves de acceso.
    -   **Excepción:** Si no todos los controles pueden tener claves de acceso únicas, puede asignar una clave de acceso a la etiqueta en lugar de a los controles individuales. Para obtener más información, vea [Teclado](inter-keyboard.md).

## <a name="documentation"></a>Documentación

Al hacer referencia a botones de radio:

-   Use el texto exacto de la etiqueta, incluida su mayúscula, pero no incluya el carácter de subrayado o dos puntos de la clave de acceso.
-   En programación y otra documentación técnica, consulte botones de radio como botones de radio. En cualquier otro lugar se usan botones de opción, especialmente en la documentación del usuario.
-   Para describir la interacción del usuario, use click.
-   Cuando sea posible, formatee la etiqueta con texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.

Ejemplo: haga clic **en Página actual** y, a continuación, haga clic en **Aceptar.**

 

 