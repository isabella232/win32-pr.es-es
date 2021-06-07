---
title: Controles de divulgación progresiva
description: Con un control de divulgación progresiva, los usuarios pueden mostrar u ocultar información adicional, incluidos datos, opciones o comandos.
ms.assetid: 0ca00c49-f897-49a6-926a-cc65f3155c6c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a40f4c2fadd75cbcb6711dec2c1361ce2f970088
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524549"
---
# <a name="progressive-disclosure-controls"></a>Controles de divulgación progresiva

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Con un control de divulgación progresiva, los usuarios pueden mostrar u ocultar información adicional, incluidos datos, opciones o comandos. La divulgación progresiva promueve la simplicidad al centrarse en lo esencial, pero revelando detalles adicionales según sea necesario.

![captura de pantalla de los controles de divulgación progresiva](images/progressive-disclosure-controls-image1.png)

Ejemplos de controles de divulgación progresiva.

> [!Note]  
> Las instrucciones relacionadas con [el diseño,](vis-layout.md) [los menús](cmd-menus.md)y las barras de herramientas se presentan en [artículos](cmd-toolbars.md) independientes.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿Los usuarios necesitan ver la información en algunos escenarios, pero no en todos, o en algunos, pero no todo el tiempo?** Si es así, mostrar la información mediante la divulgación progresiva simplifica la experiencia de línea de base, pero permite a los usuarios acceder fácilmente a la información.

    ![Captura de pantalla que muestra el estado de Security Center.](images/progressive-disclosure-controls-image2.png)

    En este ejemplo, Security Center el estado de seguridad importante todo el tiempo, pero usa la divulgación progresiva para mostrar detalles a petición.

-   **Si la información se muestra de forma predeterminada, ¿es probable que los usuarios decidan ocultarla?** ¿Hay escenarios en los que los usuarios necesitarán más espacio? ¿Están los usuarios suficientemente motivados para personalizar la interfaz de usuario (UI)? Si no es así, muestre la información sin usar la divulgación progresiva.

    **Incorrecto:**

    ![captura de pantalla de las opciones de datos que se muestran de forma predeterminada ](images/progressive-disclosure-controls-image3.png)

    En este ejemplo, los usuarios no se motivarán a ocultar la información.

-   **¿La información adicional es avanzada, sustancial, compleja o relacionada con una subtarea independiente?** Si es así, considere la posibilidad de [](ctrl-command-links.md) mostrar la información en una ventana independiente mediante botones de comando [o](ctrl-command-buttons.md) vínculos en lugar de usar un control de divulgación progresiva. (La información adicional está avanzada si está destinada a usuarios avanzados. Es complejo si dificulta la lectura o la disposición de otra información).

    ![captura de pantalla de ¿desea ejecutar este archivo? ](images/progressive-disclosure-controls-image4.png)

    En este ejemplo, la información sobre el nombre y el publicador del software es significativa principalmente para los usuarios avanzados, por lo que se usan vínculos a ventanas independientes.

-   **¿Es la información adicional un fragmento de oración o oración que describe lo que hace un elemento o cómo se puede usar?** Si es así, considere la posibilidad de usar información [sobre herramientas](ctrl-tooltips-and-infotips.md) o información.
-   **¿La información adicional está relacionada con la tarea actual, pero es independiente de la información mostrada actualmente?** Si es así, considere la posibilidad [de usar pestañas](ctrl-tabs.md) en su lugar. Sin embargo, las listas contraíbles suelen ser preferibles a las pestañas porque son más flexibles y escalables.
-   **¿Muestra u oculta la información adicional esencialmente un filtro de datos?** Si es así, considere la posibilidad de usar [una lista desplegable o](/windows/desktop/uxguide/ctrl-drop) [casillas](ctrl-check-boxes.md) en su lugar para aplicar el filtro a toda la lista.

## <a name="design-concepts"></a>Conceptos de diseño

Los objetivos de la divulgación progresiva son:

-   **Simplifique una interfaz** de usuario centrándose en lo esencial, pero revelando detalles adicionales según sea necesario.
-   **Simplifique la apariencia de una interfaz** de usuario al reducir la percepción de desorden.

Ambos objetivos se pueden lograr mediante controles de divulgación progresiva, donde los usuarios hacen clic para ver más detalles. Sin embargo, puede lograr el segundo objetivo de simplificar la apariencia sin usar controles explícitos de divulgación progresiva mediante:

-   **Mostrar los detalles contextuales solo en contexto.** Por ejemplo, puede mostrar comandos contextuales o barras de herramientas automáticamente cuando sea pertinente para el objeto o modo seleccionado.
-   **Reducir el peso de las asequiciones para la interfaz de usuario secundaria.** [Las asequibilidades](glossary.md) son propiedades visuales que sugieren cómo se usan los objetos. La tendencia es tener una interfaz de usuario con la que los usuarios puedan interactuar, pero hacer que toda esa interfaz de usuario se desenlace para decir "haga clic en mí". conduce a demasiado desorden visual. En el caso de la interfaz de usuario secundaria, a menudo es mejor usar unas asequiciones sutiles y proporcionar todos los efectos al pasar el mouse sobre él.

    ![captura de pantalla de iconos de estrella usados para calificar fotos ](images/progressive-disclosure-controls-image5.png)

    En este ejemplo, el campo Clasificación es interactivo, pero no aparece hasta que se mantiene el mouse sobre él.

-   **Mostrar los pasos de seguimiento solo después de que se cumplan los requisitos previos.** Este enfoque se usa mejor con tareas conocidas en las que los usuarios pueden realizar con confianza los primeros pasos.

    ![captura de pantalla de cuadros de texto de nombre de usuario y contraseña ](images/progressive-disclosure-controls-image6.png)

    En este ejemplo, la página nombre de usuario y contraseña muestra inicialmente solo el nombre de usuario y los cuadros de contraseña opcionales. Los cuadros de confirmación y sugerencia se muestran después de que el usuario escriba una contraseña.

Aunque la divulgación progresiva es una excelente manera de simplificar las IA, tiene estos riesgos:

-   **Falta de detectabilidad.** Los usuarios pueden suponer que, si no pueden ver algo, no existe. Los usuarios no pueden mantener el puntero ni hacer clic si no ven lo que buscan. Siempre existe la posibilidad de que los usuarios no puedan hacer clic en cosas como Más opciones.
-   **Falta de estabilidad.** Se debe esperar una divulgación progresiva o, al menos, ser natural. Si los controles aparecen y desaparecen inesperadamente, la interfaz de usuario resultante puede parecer inestable.

### <a name="progressive-disclosure-controls"></a>Controles de divulgación progresiva

Normalmente, los controles de divulgación progresiva se muestran sin etiquetas directas que describen su comportamiento, por lo que los usuarios deben poder hacer lo siguiente solo en función de la apariencia visual del control:

-   Reconocer que el control proporciona divulgación progresiva.
-   Determine si el estado actual está expandido o contraído.
-   Determine si se necesita información adicional, opciones o comandos para realizar la tarea.
-   Determine cómo restaurar el estado original, si lo desea.

Aunque los usuarios pueden determinar lo anterior por prueba y error, debe intentar que esta experimentación no sea necesaria.

Los controles de divulgación progresiva tienen unas asequibilidades bastante [débiles,](glossary.md)lo que significa que sus propiedades visuales sugieren cómo se usan, aunque de forma débil. En la tabla siguiente se compara la apariencia de los controles comunes de divulgación progresiva:



| Control | Propósito  | Aspecto | El glifo indica |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| **Galones**<br/> ![captura de pantalla de los contenidos de contenido adicional de izquierda/derecha y arriba y abajo ](images/progressive-disclosure-controls-image7.png)<br/>                 | **Mostrar todo:** Mostrar u ocultar los elementos restantes en contenido completamente o parcialmente oculto. Los elementos se muestran en contexto (mediante un solo botón de contenido adicional) o en un menú emergente (mediante un botón de contenido adicional doble).<br/> | Los contenidos de contenido adicional apuntan en la dirección donde se producirá la acción.<br/>                                                        | Estado futuro<br/>        |
| **Flechas**<br/> ![captura de pantalla de flechas izquierda/derecha y arriba/abajo ](images/progressive-disclosure-controls-image8.png)<br/>                     | **Mostrar opciones:** Mostrar un menú emergente de comandos.<br/>                                                                                                                                                    | Las flechas apuntan en la dirección donde se producirá la acción.<br/>                                                          | Estado futuro<br/>        |
| **Controles más y menos**<br/> ![captura de pantalla de dos botones más y menos pequeños ](images/progressive-disclosure-controls-image9.png)<br/> | **Expanda contenedores:** Expanda o contraiga el contenido del contenedor al navegar por una jerarquía.<br/>                                                                                        | Los símbolos más y menos no apuntan, pero la acción siempre se produce a su derecha.<br/>                                    | Estado futuro<br/>        |
| **Triángulos de rotación**<br/> ![captura de pantalla de dos triángulos pequeños ](images/progressive-disclosure-controls-image10.png)<br/>                  | **Mostrar detalles:** Mostrar u ocultar información adicional para un elemento individual. También se usan para expandir contenedores.<br/>                                                                  | La rotación de triángulos se parece ligeramente a las ruedas de rotación, por lo que apuntan en la dirección en la que se ha producido la acción.<br/> | Estado actual<br/>       |



 

**Si solo hace una cosa...**

Los usuarios deben ser capaces de predecir correctamente el comportamiento de un control de divulgación progresiva mediante la inspección por sí solos. Para ello, seleccione los patrones de uso adecuados y aplique su apariencia, ubicación y comportamiento de forma coherente.

## <a name="usage-patterns"></a>Patrones de uso

Los controles de divulgación progresiva tienen varios patrones de uso. Algunos de ellos están integrados en controles comunes.

### <a name="chevrons"></a>Galones

Los elementos de contenido adicional muestran u ocultan los elementos restantes en contenido completamente o parcialmente oculto. Normalmente, los elementos se muestran en su lugar, pero también se pueden mostrar en un menú emergente. Cuando está en su lugar, el elemento permanece expandido hasta que el usuario lo contrae.

Los elementos de contenido adicional se usan de las maneras siguientes:



|      Uso                                                                                                                                                          |    Ejemplo                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Interfaz de usuario local**<br/> El objeto asociado recibe el foco de entrada y el botón de contenido adicional único se activa con la barra espaciador.<br/>                       | ![captura de pantalla de la pantalla de estado del centro de seguridad ](images/progressive-disclosure-controls-image11.png)<br/> En estos ejemplos, los botón de contenido adicional único en su lugar se sitúan a la derecha de su control asociado.<br/>                                                                            |
| **Botones de comando con etiquetas externas**<br/> el botón de comando recibe el foco de entrada y el botón de contenido adicional único se activa con la barra espaciador.<br/> | ![captura de pantalla del botón de contenido adicional con la etiqueta "más opciones" ](images/progressive-disclosure-controls-image12.png)<br/> En este ejemplo, el botón de contenido adicional único se etiqueta y se coloca a la izquierda de la etiqueta. Con este patrón, el botón sería difícil de entender sin su etiqueta.<br/> |
| **Botones de comando con etiquetas internas**<br/> el botón de comando recibe el foco de entrada y se activa con la barra espaciador.<br/>                    | ![captura de pantalla de los botones de comandos "más" y "menos" ](images/progressive-disclosure-controls-image13.png)<br/> En estos ejemplos, los botones de comando normales tienen el botón de contenido adicional doble situado para sugerir su significado.<br/>                                                                          |



 

### <a name="arrows"></a>Flechas

Las flechas muestran un menú emergente de comandos. El elemento permanece expandido hasta que el usuario realiza una selección o hace clic en cualquier lugar.

Si el botón de flecha es un control independiente, recibe el foco de entrada y se activa con la barra espaciador. Si el botón de flecha tiene un control primario, el elemento primario recibe el foco de entrada y la flecha se activa con las teclas Alt+flecha abajo y Alt+flecha arriba, como con el control de lista desplegable.

Las flechas se usan de las maneras siguientes:



|    Uso                                                                                   |    Ejemplo                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Botones independientes**<br/> la flecha está en un control de botón independiente.<br/> | ![captura de pantalla de flechas a la derecha de los controles ](images/progressive-disclosure-controls-image14.png)<br/> En estos ejemplos, los botones de flecha independientes situados a la derecha indican un menú de comandos.<br/>               |
| **Botones de comando**<br/> la flecha forma parte de un botón de comando.<br/>      | ![captura de pantalla de etiqueta y flecha en el botón de comando ](images/progressive-disclosure-controls-image15.png)<br/> En estos ejemplos, los botones de menú y los botones de división tienen las flechas situadas a la derecha del texto.<br/> |



 

### <a name="plus-and-minus-controls"></a>Controles más y menos

Los controles más y menos se expanden o contraen para mostrar el contenido del contenedor en su lugar al navegar por una jerarquía. El elemento permanece expandido hasta que el usuario lo contrae. Aunque parecen botones, su comportamiento está en su lugar.

El objeto asociado recibe el foco de entrada. El signo más se activa con la tecla de flecha derecha y el signo menos con la tecla de flecha izquierda.

Los controles Más y Menos se usan de las maneras siguientes:



|       Uso                                                                                         |       Ejemplo                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Árboles contraíbles**<br/> una jerarquía de varios niveles para mostrar el contenido del contenedor.<br/> | ![Captura de pantalla que muestra Explorador de Windows árbol de carpetas con "Comportamiento" seleccionado.](images/progressive-disclosure-controls-image16.png)<br/> En este ejemplo, los controles más y menos se sitúan a la izquierda del contenedor asociado.<br/>       |
| **Listas contraíbles**<br/> una jerarquía de dos niveles para mostrar el contenido del contenedor.<br/>   | ![captura de pantalla de la lista expandida para mostrar dos niveles ](images/progressive-disclosure-controls-image17.png)<br/> En este ejemplo, los controles más y menos se sitúan a la izquierda del encabezado de lista asociado.<br/> |



 

### <a name="rotating-triangles"></a>Girar triángulos

Los triángulos de rotación muestran u ocultan información adicional en su lugar para un elemento individual. También se usan para expandir los contenedores. El elemento permanece expandido hasta que el usuario lo contrae.

El objeto asociado recibe el foco de entrada. El triángulo contraído (que apunta a la derecha) se activa con la tecla de flecha derecha y el triángulo expandido (hacia abajo) con la tecla de flecha izquierda.

Los triángulos de rotación se usan de las maneras siguientes:



|     Uso                                                                                                       |    Ejemplo                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Árboles contraíbles**<br/> una jerarquía de varios niveles para mostrar el contenido del contenedor.<br/>             | ![captura de pantalla del árbol de carpetas del Explorador de Windows ](images/progressive-disclosure-controls-image18.png)<br/> En este ejemplo, los triángulos de rotación se sitúan a la izquierda del contenedor asociado.<br/>       |
| **Listas contraíbles**<br/> una jerarquía de dos niveles para mostrar información adicional en su lugar.<br/> | ![captura de pantalla de la lista que muestra datos adicionales ](images/progressive-disclosure-controls-image19.png)<br/> En este ejemplo, los triángulos de rotación se sitúan a la izquierda de los elementos de lista asociados.<br/> |



 

### <a name="preview-arrows"></a>Flechas de vista previa

Al igual que los elementos de contenido adicional, se muestra u oculta información adicional en su lugar. El elemento permanece expandido hasta que el usuario lo contrae. A diferencia de los botones de contenido adicional, los glifos tienen una representación gráfica de la acción, normalmente con una flecha que indica lo que ocurrirá.

![captura de pantalla de glifos de flecha que apuntan diagonalmente ](images/progressive-disclosure-controls-image20.png)

En estos ejemplos de Microsoft Reproductor de Windows Media, los glifos tienen flechas que sugieren la acción que se va a producir.

Las flechas de vista previa se reservan mejor para situaciones en las que un botón de contenido adicional estándar no comunica adecuadamente el comportamiento del control, como cuando la divulgación es compleja o hay más de un tipo de divulgación.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Seleccione el patrón de divulgación progresiva en función de su uso.** Para obtener una descripción de cada patrón de uso, consulte la tabla anterior.
-   **No use vínculos para controles de divulgación progresiva.** Use solo los controles de divulgación progresiva presentados en la sección Patrones de uso. Sin embargo, use vínculos para ir a temas [de Ayuda.](winenv-help.md)

    **Correcto:**

    ![captura de pantalla del botón de contenido adicional con la etiqueta "mostrar mezclador" ](images/progressive-disclosure-controls-image21.png)

    **Incorrecto:**

    ![Captura de pantalla del texto del vínculo "mostrar mezclador" ](images/progressive-disclosure-controls-image22.png)

    En el ejemplo incorrecto, se usa un vínculo para mostrar más opciones en su lugar. Este uso sería correcto si el vínculo hubiera navegado a otra página o cuadro de diálogo, o mostrara un tema de Ayuda.

### <a name="interaction"></a>Interacción

-   **Para los botones de contenido adicional y las flechas que no están etiquetados directamente, use información sobre herramientas para describir lo que hacen.**

    ![Captura de pantalla de la información sobre herramientas "Expandir el generador de consultas" ](images/progressive-disclosure-controls-image23.png)

    En este ejemplo, la información sobre herramientas indica el efecto de un control de contenido adicional sin etiquetar.

-   **Si un usuario expande** o contrae un elemento, haga que el estado se conserve para que se haga efectivo la próxima vez que se muestre la ventana, a menos que sea probable que los usuarios prefieran comenzar en el estado predeterminado. Haga que el estado se conserve por ventana y por usuario.
-   **Asegúrese de que todo el contenido expandido se puede contraer y viceversa, y de que la operación inversa es obvia.** Esto fomenta la exploración y reduce la frustración. La mejor manera de que la operación inversa sea obvia es mantener el control en la misma ubicación fija. Si necesita mover el control, mantenga el control en la misma ubicación relativa dentro de un área visualmente distinta.

    **Incorrecto:**

    ![captura de pantalla del botón "Reemplazar" por botón de contenido adicional ](images/progressive-disclosure-controls-image24.png)

    ![captura de pantalla del botón "Reemplazar" sin botón de contenido adicional ](images/progressive-disclosure-controls-image25.png)

    En este ejemplo, al hacer clic en el botón Reemplazar con el botón de contenido adicional se muestra **el cuadro de** texto Reemplazar por . Una vez hecho esto, el expansor Reemplazar se convierte en el comando Reemplazar, por lo que no hay ninguna manera de restaurar el estado original.

-   **Use solo las claves de acceso adecuadas para el patrón de divulgación progresiva**, como se muestra en la sección Patrones de uso. No use Entrar para activar la divulgación progresiva.

### <a name="presentation"></a>Presentación

-   **No use puntas de flecha en forma de triangular para un propósito distinto de la divulgación progresiva.**

    **Incorrecto:**

    ![captura de pantalla de la etiqueta con triángulo que apunta a la derecha ](images/progressive-disclosure-controls-image26.png)

    Aunque este ejemplo no es un patrón de divulgación progresiva, el uso de una flecha aquí sugiere que los comandos se mostrarán en una ventana emergente.

    **Correcto:**

    ![captura de pantalla de la etiqueta con viñeta a la izquierda del texto ](images/progressive-disclosure-controls-image27.png)

    En este ejemplo, se usa correctamente una viñeta en su lugar.

-   **Quite (no deshabilite) los controles de divulgación progresiva que no se aplican en el contexto actual.** Los controles de divulgación progresiva siempre deben cumplir su promesa, así que quítelos cuando no haya más información que proporcionar.

    **Incorrecto:**

    ![captura de pantalla de un control "más opciones" atenuado ](images/progressive-disclosure-controls-image28.png)

    En este ejemplo, un control de divulgación progresiva que no se aplica está deshabilitado incorrectamente.

### <a name="chevrons"></a>Galones

-   **Use botón de contenido adicional único para mostrar u ocultar en su lugar. Use los elementos de contenido adicional dobles para mostrar u ocultar mediante un menú emergente.** Sin embargo, siempre debe usar dobles botones de contenido adicional para los botones de comando con etiquetas internas.

    **Correcto:**

    ![captura de pantalla del control de opciones de contenido adicional único ](images/progressive-disclosure-controls-image29.png)

    **Incorrecto:**

    ![captura de pantalla del control de opciones de doble contenido adicional ](images/progressive-disclosure-controls-image30.png)

    En el ejemplo incorrecto, se usa un botón de contenido adicional doble para la divulgación progresiva local.

    **Correcto:**

    ![captura de pantalla del botón de comando más de doble botón de contenido adicional ](images/progressive-disclosure-controls-image31.png)

    En este ejemplo, se usa un botón de contenido adicional doble para la divulgación progresiva local porque es un botón de comando con una etiqueta interna.

-   **Proporcione una relación visual entre el botón de contenido adicional y su control asociado.** Dado que los botónes de contenido adicional en posición se colocan a la derecha de la interfaz de usuario asociada y se alinean a la derecha, puede haber una distancia bastante entre un botón de contenido adicional y su control asociado.

    **Correcto:**

    ![captura de pantalla del sombreado egresado detrás de los controles ](images/progressive-disclosure-controls-image32.png)

    En este ejemplo, hay una relación clara entre el botón de contenido adicional local y su interfaz de usuario asociada.

    **Incorrecto:**

    ![captura de pantalla de fondo blanco sólido para controles ](images/progressive-disclosure-controls-image33.png)

    En este ejemplo, no hay ninguna relación visual clara entre el botón de contenido adicional local y su interfaz de usuario asociada, por lo que parece estar flotante en el espacio.

### <a name="arrows"></a>Flechas

-   **No use gráficos de flecha que puedan confundirse con Atrás, Adelante, Ir o Reproducir.** Use puntas de flecha simples con forma de triangular (flechas sin lemates) en fondos neutros.

    **Correcto:**

    ![captura de pantalla de dos pequeños triángulos negros ](images/progressive-disclosure-controls-image34.png)

    Estas flechas son claramente controles de divulgación progresiva.

    **Incorrecto (para la divulgación progresiva):**

    ![captura de pantalla de dos flechas verdes pequeñas ](images/progressive-disclosure-controls-image35.png)

    Estas flechas no parecen controles de divulgación progresiva.

    **Incorrecto (para Back, Forward):**

    ![captura de pantalla de dos botones con triángulos negros ](images/progressive-disclosure-controls-image36.png)

    Estas flechas parecen controles de divulgación progresiva, pero no lo son.

## <a name="recommended-sizing-and-spacing"></a>Tamaño y espaciado recomendados

![captura de pantalla de tamaño y espaciado recomendados ](images/progressive-disclosure-controls-image37.png)

Tamaño y espaciado recomendados para controles de divulgación progresiva.

## <a name="labels"></a>Etiquetas

-   Para los botones de contenido adicional de un botón de comando con una etiqueta externa:
    -   Asigne una clave [de acceso única.](glossary.md) Para obtener instrucciones, vea [Teclado](inter-keyboard.md).
    -   Use [mayúsculas de estilo oración.](glossary.md)
    -   Escriba la etiqueta como una frase y no use ningún signo de puntuación final.
    -   Escriba la etiqueta para que describa el efecto de hacer clic en el botón y cambiar la etiqueta cuando cambie el estado.
    -   Si la superficie siempre muestra algunas opciones, comandos o detalles, use los siguientes pares de etiquetas:
        -   **Más o menos opciones.** Use para opciones o una combinación de opciones, comandos y detalles.
        -   **Más o menos comandos.** Use solo para comandos.
        -   **Más o menos detalles.** Use solo para obtener información.
        -   **Más o menos <object name> .** Se usa para otros tipos de objetos, como carpetas.
    -   De lo contrario:
        -   **Mostrar u ocultar opciones.** Use para opciones o una combinación de opciones, comandos y detalles.
        -   **Mostrar u ocultar comandos.** Use solo para comandos.
        -   **Mostrar u ocultar detalles.** Use solo para obtener información.
        -   **Mostrar u ocultar <object name> .** Se usa para otros tipos de objetos, como carpetas.
-   Para los botones de contenido adicional de un botón de comando con una etiqueta interna, siga las instrucciones del botón [de comando](ctrl-command-buttons.md) estándar.

## <a name="documentation"></a>Documentación

Al hacer referencia a controles de divulgación progresiva:

-   Si el control tiene una etiqueta fija, consulte el control solo por su etiqueta; no intente describir el control. Use el texto exacto de la etiqueta, incluida su mayúscula, pero no incluya el carácter de subrayado de la clave de acceso.
-   Si el control no tiene ninguna etiqueta o no es fijo, consulte el control por su tipo: botón de botón de contenido adicional, flecha, triángulo o más/menos. Si es necesario, describa también la ubicación del control. Si el control aparece dinámicamente, como el control [de](glossary.md) espacio de página, inicie la referencia describiendo cómo hacer que aparezca el control.

    **Ejemplo:** Para mostrar los archivos dentro de una carpeta, mueva el puntero al inicio del nombre de la carpeta y, a continuación, haga clic en el triángulo situado junto a la carpeta.

-   No haga referencia al control como un botón, a menos que contraste con otros controles de divulgación progresiva que no son botones.
-   Para describir la interacción del usuario, use click. Si es necesario para mayor claridad, use haga clic en... para expandir o contraer.
-   Cuando sea posible, formatee la etiqueta con texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.

Ejemplos:

-   (Para un botón de contenido adicional) Para determinar el tamaño del archivo, haga clic en **Detalles.**
-   (Para una flecha) Para ver todas las opciones, haga clic en la flecha situada junto al **cuadro** Buscar.
-   (Para más/menos) Para ver la imagen, haga clic en **Imágenes.**

