---
title: Botones de radio
description: Con un botón de radio, los usuarios pueden elegir entre un conjunto de opciones relacionadas mutuamente excluyentes.
ms.assetid: f9af0a8a-d4a1-464c-a967-bab88ae0726b
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 00495695753506702015431c889e74d5a7effe9a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104279752"
---
# <a name="radio-buttons"></a>Botones de radio

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Con un botón de radio, los usuarios pueden elegir entre un conjunto de opciones relacionadas mutuamente excluyentes. Los usuarios pueden elegir una y solo una opción. Se llama a los botones de radio porque funcionan como los valores preestablecidos de canal en las radios.

![captura de pantalla de tres botones de radio ](images/radio-buttons-image1.png)

Grupo típico de botones de radio.

Un grupo de botones de radio se comporta como un control único. Solo se puede acceder a la opción seleccionada mediante la tecla Tab, pero los usuarios pueden recorrer el grupo con las teclas de dirección.

> [!Note]  
> Las instrucciones relacionadas con el [diseño](vis-layout.md) y la [navegación mediante el teclado](inter-keyboard.md) se presentan en un artículo independiente.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿Se usa el control para elegir una opción de un conjunto de opciones mutuamente excluyentes?** Si no es así, usa otro control. Para elegir varias opciones, use [casillas](ctrl-check-boxes.md), una [lista de selección múltiple](ctrl-list-boxes.md) o una lista de casillas en su lugar.
-   **¿El número de opciones entre dos y siete?** Dado que el espacio de pantalla utilizado es proporcional al número de opciones, mantenga el número de opciones en un grupo entre dos y siete. Para ocho o más opciones, use una lista [desplegable](/windows/desktop/uxguide/ctrl-drop) o una [lista de selección única](ctrl-list-boxes.md).
-   **¿Una casilla sería una opción mejor?** Si solo hay dos opciones, puede usar en su lugar una sola [casilla](ctrl-check-boxes.md) . Sin embargo, las casillas solo son adecuadas para activar o desactivar una sola opción, mientras que los botones de radio se pueden usar para alternativas totalmente diferentes. Si ambas soluciones son posibles:
    -   Use los botones de radio si el significado de la casilla desactivada no es completamente obvio.

        **Incorrecto:**

        ![captura de pantalla de la casilla horizontal ](images/radio-buttons-image2.png)

        **Correcto:**

        ![captura de pantalla de botones de radio horizontales o verticales ](images/radio-buttons-image3.png)

        En el ejemplo correcto, las opciones no son opuestas, por lo que los botones de radio son la mejor opción.

    -   Use los botones de radio de las páginas del Asistente para desactivar las alternativas, incluso si la casilla de verificación es aceptable.
    -   Use los botones de radio si tiene suficiente espacio de pantalla y las opciones son lo suficientemente importantes como para ser un buen uso de ese espacio de la pantalla. De lo contrario, utilice una casilla o una lista desplegable.

        **Incorrecto:**

        ![captura de pantalla de mostrar/no mostrar botones de radio ](images/radio-buttons-image4.png)

        En este ejemplo, las opciones no son lo suficientemente importantes para usar botones de radio.

        **Correcto:**

        ![captura de pantalla de la casilla no mostrar este mensaje ](images/radio-buttons-image5.png)

        En este ejemplo, una casilla es un uso eficaz del espacio de pantalla para esta opción de periféricos.

    -   Utilice una casilla de verificación si hay otras casillas en la página.

-   **¿Una lista desplegable sería una opción mejor?** Si se recomienda usar la opción predeterminada para la mayoría de los usuarios en la mayoría de los casos, los botones de radio podrían atraer más atención a las opciones de las necesarias.
    -   Considere la posibilidad de usar una lista desplegable si no desea atraer la atención a las opciones o no desea animar a los usuarios a realizar cambios. Una lista desplegable se centra en la selección actual, mientras que los botones de radio resaltan todas las opciones por igual.

        ![captura de pantalla de la calidad máxima como botón predeterminado ](images/radio-buttons-image6.png)

        En este ejemplo, una lista desplegable se centra en la selección actual y evita que los usuarios realicen cambios.

    -   Considere una lista desplegable si hay otras listas desplegables en la página.

-   **¿Un conjunto de botones de comando, vínculos de comandos o un botón de expansión es una opción mejor?** Si los botones de radio solo se usan para influir en el modo en que se realiza un comando, a menudo es mejor presentar las variaciones del comando en su lugar. Esto permite a los usuarios elegir el comando correcto con una sola interacción.
-   **¿Las opciones presentan las opciones del programa, en lugar de los datos?** Los valores de las opciones no deben basarse en el contexto u otros datos. En el caso de los datos, use una lista desplegable o una lista de selección única.
-   Si el control se usa en una página del asistente o en un panel de control, ¿ **es el control una respuesta a la instrucción principal y los usuarios pueden cambiar más adelante la opción?** Si es así, considere la posibilidad de usar vínculos de comandos en lugar de botones de radio para que la interacción sea más eficaz.
-   **¿Los valores son no numéricos?** Para datos numéricos, use [cuadros de texto](ctrl-text-boxes.md), [listas](/windows/desktop/uxguide/ctrl-drop)desplegables o [controles deslizantes](ctrl-sliders.md).

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Enumere las opciones en un orden lógico,** por ejemplo, lo más probable es que se seleccione la operación más sencilla a más compleja o menos riesgo para la mayoría. No se recomienda el orden alfabético porque depende del lenguaje y, por lo tanto, no es localizable.
-   **Si ninguna de las opciones es una opción válida, agregue otra opción para reflejar esta opción,** como ninguna o no se aplica.
-   **Prefiere alinear los botones de radio verticalmente en lugar de horizontalmente.** La alineación horizontal es más difícil de leer y localizar.

    **Correcto:**

    ![captura de pantalla de la alineación vertical de los botones de radio ](images/radio-buttons-image7.png)

    En este ejemplo, los botones de radio están alineados verticalmente.

    **Incorrecto:**

    ![captura de pantalla de la alineación horizontal del botón de radio ](images/radio-buttons-image8.png)

    En este ejemplo, la alineación horizontal es más difícil de leer.

-   **Reconsidere el uso de cuadros de grupo para organizar grupos de botones de radio**; esto suele producir un desorden de pantalla innecesario.
-   **No use etiquetas de botón de radio como etiquetas de cuadro de grupo.**
-   **No use la selección de un botón de radio para:**
    -   Ejecutar comandos.
    -   Mostrar otras ventanas, como un cuadro de diálogo para recopilar más entradas.
    -   Mostrar u ocultar de forma dinámica otros controles relacionados con el control seleccionado (los lectores de pantalla no pueden detectar dichos eventos). Sin embargo, puede cambiar el texto de forma dinámica en función de la selección.

### <a name="subordinate-controls"></a>Controles subordinados

-   Coloque los controles subordinados a la derecha o debajo de (con sangría, vaciado con la etiqueta del botón de radio) el botón de radio y su etiqueta. Finalice la etiqueta del botón de radio con un signo de dos puntos.

    ![captura de pantalla del control a la derecha de su etiqueta ](images/radio-buttons-image9.png)

    En este ejemplo, el botón de radio y su control subordinado comparten la etiqueta del botón de radio y su clave de acceso. En este caso, las teclas de dirección mueven el foco del botón de radio a su cuadro de texto subordinado.

-   **Deje las listas desplegables y los cuadros de texto modificables dependientes habilitados si comparten la etiqueta del botón de radio.** Cuando los usuarios escriban o peguen cualquier elemento en el cuadro, seleccione automáticamente la opción correspondiente. De este modo, se simplifica la interacción.

    ![captura de pantalla del cuadro de diálogo intervalo de páginas con cuadro de texto ](images/radio-buttons-image10.png)

    En este ejemplo, al escribir un número de página, se seleccionan automáticamente las páginas.

-   **Evite anidar los botones de radio con otros botones de radio o casillas.** Si es posible, mantenga todas las opciones en el mismo nivel.

    **Correcto:**

    ![captura de pantalla de los botones de radio alineados a la izquierda ](images/radio-buttons-image11.png)

    En este ejemplo, las opciones se encuentran en el mismo nivel.

    **Incorrecto:**

    ![captura de pantalla de botones de radio anidados ](images/radio-buttons-image12.png)

    En este ejemplo, el uso de opciones anidadas agrega complejidad innecesaria.

-   Si anida botones de radio con otros botones de radio o casillas, **deshabilite estos controles subordinados hasta que se seleccione la opción de alto nivel.** Al hacerlo, se evita la confusión sobre el significado de los controles subordinados.

### <a name="default-values"></a>Valores predeterminados

-   Dado que un grupo de botones de radio representa un conjunto de opciones mutuamente excluyentes, **siempre tiene un botón de radio seleccionado de forma predeterminada. Seleccione la opción más segura (para evitar la pérdida de datos o el acceso al sistema) y la opción más segura y privada.** Si seguridad y seguridad no son factores, seleccione la opción más probable o cómoda.
-   **Excepciones:** No tener una selección predeterminada si:
    -   **No hay ninguna opción predeterminada aceptable por motivos de seguridad, seguridad o legales, por lo que el usuario debe tomar una decisión explícita.** Si el usuario no realiza una selección, muestre un mensaje de error para forzar una.
    -   **La interfaz de usuario (UI) debe reflejar el estado actual y aún no se ha establecido la opción.** Un valor predeterminado implicaría incorrectamente que el usuario no necesita realizar una selección.
    -   **El objetivo es recopilar datos no sesgados.** Los valores predeterminados afectarían a la recopilación de datos.
    -   **El grupo de botones de radio representa una propiedad en un estado mixto**, lo que sucede cuando se muestra una propiedad para varios objetos que no tienen la misma configuración. No muestre un mensaje de error en este caso, ya que cada objeto tiene un estado válido.
-   **Haga que la primera opción sea la predeterminada**, ya que los usuarios suelen esperar eso, a menos que ese orden no sea lógico. Para ello, puede que tenga que cambiar las etiquetas de las opciones.

    **Incorrecto:**

    ![captura de pantalla del último botón de radio como opción predeterminada ](images/radio-buttons-image13.png)

    En este ejemplo, la opción predeterminada no es la primera opción.

    **Correcto:**

    ![captura de pantalla del primer botón de radio como predeterminado ](images/radio-buttons-image14.png)

    En este ejemplo, las etiquetas de opción se reparan para que la primera opción sea la predeterminada.

## <a name="recommended-sizing-and-spacing"></a>Ajuste de tamaño y espaciado recomendados

![captura de pantalla de ajuste de tamaño y espaciado del botón de radio ](images/radio-buttons-image15.png)

Ajuste de tamaño y espaciado recomendados para los botones de radio.

## <a name="labels"></a>Etiquetas

### <a name="radio-button-labels"></a>Etiquetas de botón de radio

-   Etiquetar cada botón de radio.

<!-- -->

-   Asigne una [clave de acceso](glossary.md) única a cada etiqueta. Para obtener instrucciones, consulte [teclado](inter-keyboard.md).
-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
-   Escriba la etiqueta como una frase, no como una frase, y no use ningún signo de puntuación final.
    -   **Excepción:** Si una etiqueta de botón de radio también etiqueta un control subordinado, termine la etiqueta con un signo de dos puntos.
-   Use frases paralelas e intente mantener la longitud sobre la misma para todas las etiquetas.
-   Centre el texto de la etiqueta en las diferencias entre las opciones. Si todas las opciones tienen el mismo texto de introducción, mueva el texto a la etiqueta de grupo.
-   Usar frases positivas. Por ejemplo, use do en lugar de no, e imprima en lugar de no imprimir.
-   Describa solo la opción con la etiqueta. Conserve las etiquetas breves, por lo que es fácil hacer referencia a ellas en los mensajes y la documentación. Si la opción requiere una explicación más detallada, proporcione la explicación en un control de [texto estático](glossary.md) mediante frases completas y puntuación final.

    ![captura de pantalla de botones de radio con texto explicativo](images/radio-buttons-image16.png)

    En este ejemplo, las opciones se explican mediante controles de texto estático independientes.

    > [!Note]  
    > Agregar una explicación a un botón de radio no significa que tenga que proporcionar explicaciones para todos los botones de radio. Proporcione la información relevante en la etiqueta, si es posible, y use explicaciones solo cuando sea necesario. No solo tiene que volver a cambiar el estado de la etiqueta para que sea coherente.

     

-   **Si se recomienda una opción, agregue "(recomendado)" a la etiqueta.** Asegúrese de agregar a la etiqueta de control, no a las notas complementarias.
-   **Si una opción está pensada solo para usuarios avanzados, agregue "(avanzado)" a la etiqueta.** Asegúrese de agregar a la etiqueta de control, no a las notas complementarias.
-   Si debe usar etiquetas de varias líneas, alinee la parte superior de la etiqueta con el botón de radio.
-   No utilice un control subordinado, los valores que contiene o su etiqueta de unidades para crear una frase o frase. Este tipo de diseño no es localizable porque la estructura de oraciones varía según el idioma.

### <a name="radio-button-group-labels"></a>Etiquetas de grupo de botones de radio

-   Use la etiqueta de grupo para explicar el propósito del grupo, no cómo hacer la selección. Supongamos que los usuarios saben cómo usar los botones de radio. Por ejemplo, no indique "Seleccione una de las siguientes opciones".
-   Todos los grupos de botones de radio necesitan etiquetas. Escriba la etiqueta como una palabra o frase, no como una frase, y termine con un signo de dos puntos usando texto estático o un cuadro de grupo.

    **Excepción:** Omita la etiqueta si es simplemente una resituación de la [instrucción principal](glossary.md)de un cuadro de diálogo. En este caso, la instrucción principal toma el signo de dos puntos (a menos que sea una pregunta) y la tecla de acceso (si hay alguno).

    **Aceptable:**

    ![captura de pantalla de etiqueta de grupo de botón de radio redundante ](images/radio-buttons-image17.png)

    En este ejemplo, la etiqueta del grupo de botones de radio es simplemente una resituación de la instrucción principal.

    **Manera**

    ![captura de pantalla de la instrucción principal de botón de radio solamente ](images/radio-buttons-image18.png)

    En este ejemplo, se quita la etiqueta redundante, por lo que la instrucción principal toma el signo de dos puntos.

-   No asigne una clave de acceso a la etiqueta. Esto no es necesario y hace que las demás claves de acceso sean más difíciles de asignar.
    -   **Excepción:** Si no todos los controles pueden tener claves de acceso únicas, puede asignar una clave de acceso a la etiqueta en lugar de a los controles individuales. Para obtener más información, consulte [teclado](inter-keyboard.md).

## <a name="documentation"></a>Documentación

Al hacer referencia a los botones de radio:

-   Use el texto de etiqueta exacto, incluido el uso de mayúsculas, pero no incluya el carácter de subrayado de la tecla de acceso o el signo de dos puntos.
-   En programación y otra documentación técnica, consulte los botones de radio como botones de radio. En otras ubicaciones, use los botones de opción, especialmente en la documentación del usuario.
-   Para describir la interacción del usuario, use haga clic en.
-   Siempre que sea posible, dé formato a la etiqueta usando texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.

Ejemplo: haga clic en **Página actual** y, a continuación, haga clic en **Aceptar**.

 

 