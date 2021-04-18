---
title: Controles de divulgación progresiva
description: Con un control de divulgación progresiva, los usuarios pueden mostrar u ocultar información adicional, como datos, opciones o comandos.
ms.assetid: 0ca00c49-f897-49a6-926a-cc65f3155c6c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 22c74f60b3184f7fa7f7cdb2b4f2e9d9f64995ea
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104361820"
---
# <a name="progressive-disclosure-controls"></a>Controles de divulgación progresiva

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Con un control de divulgación progresiva, los usuarios pueden mostrar u ocultar información adicional, como datos, opciones o comandos. La divulgación progresiva promueve la simplicidad centrándose en el esencial, pero revelando detalles adicionales según sea necesario.

![captura de pantalla de controles de divulgación progresiva](images/progressive-disclosure-controls-image1.png)

Ejemplos de controles de divulgación progresiva.

> [!Note]  
> Las instrucciones relacionadas con el [diseño](vis-layout.md), los [menús](cmd-menus.md)y las [barras de herramientas](cmd-toolbars.md) se presentan en artículos independientes.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿Los usuarios deben ver la información en algunos escenarios, pero no en todos, o en algunos, pero no en todo el tiempo?** Si es así, la visualización de la información mediante la divulgación progresiva simplifica la experiencia de línea de base, pero permite a los usuarios obtener acceso fácilmente a la información.

    ![Captura de pantalla que muestra la presentación de estado de Security Center.](images/progressive-disclosure-controls-image2.png)

    En este ejemplo, Security Center muestra el estado de seguridad importante todo el tiempo, pero utiliza la divulgación progresiva para mostrar los detalles a petición.

-   **Si se muestra la información de forma predeterminada, ¿es probable que los usuarios decidan ocultarla?** ¿Hay escenarios en los que los usuarios necesiten más espacio? ¿Los usuarios están suficientemente motivados para personalizar la interfaz de usuario? Si no es así, muestre la información sin usar la divulgación progresiva.

    **Incorrecto:**

    ![captura de pantalla de opciones de datos que se muestran de forma predeterminada ](images/progressive-disclosure-controls-image3.png)

    En este ejemplo, los usuarios no estarán motivados para ocultar la información.

-   **¿La información adicional es más avanzada, substancial, compleja o relacionada con una subtarea independiente?** Si es así, considere la posibilidad de mostrar la información en una ventana independiente con los [botones de comando](ctrl-command-buttons.md) o los [vínculos](ctrl-command-links.md) en lugar de usar un control de divulgación progresiva. (La información adicional es avanzada si está pensada para usuarios avanzados. Es complejo si hace que sea difícil leer o diseñar otra información).

    ![captura de pantalla de ¿desea ejecutar este archivo? ](images/progressive-disclosure-controls-image4.png)

    En este ejemplo, la información sobre el nombre y el publicador del software es principalmente significativa para los usuarios avanzados, por lo que se usan vínculos a ventanas independientes.

-   **¿Es la información adicional un fragmento de frase o frase que describe lo que hace un elemento o cómo se puede usar?** Si es así, considere la posibilidad de usar una [información sobre herramientas](ctrl-tooltips-and-infotips.md) o una sugerencia.
-   **¿Es la información adicional relacionada con la tarea actual, pero es independiente de la información que se muestra actualmente?** Si es así, considere la posibilidad de usar [pestañas](ctrl-tabs.md) en su lugar. Sin embargo, las listas contraíbles suelen ser preferibles a las pestañas porque son más flexibles y escalables.
-   **¿Está mostrando u ocultando la información adicional esencialmente un filtro de datos?** Si es así, considere la posibilidad de utilizar una [lista desplegable](/windows/desktop/uxguide/ctrl-drop) o [casillas de verificación](ctrl-check-boxes.md) para aplicar el filtro a toda la lista.

## <a name="design-concepts"></a>Conceptos de diseño

Los objetivos de la divulgación progresiva son:

-   **Simplifique una interfaz de usuario** centrándose en el esencial, pero mostrando detalles adicionales según sea necesario.
-   **Simplifique la apariencia** de la interfaz de usuario reduciendo la percepción de desorden.

Ambos objetivos se pueden lograr mediante controles de divulgación progresiva, donde los usuarios hacen clic para ver más detalles. Sin embargo, puede lograr el segundo objetivo de simplificar la apariencia sin usar controles de divulgación progresivas explícitos:

-   **Solo se muestran los detalles contextuales en contexto.** Por ejemplo, puede mostrar automáticamente las barras de herramientas o los comandos contextuales cuando sea relevante para el objeto o el modo seleccionados.
-   **Reducir el peso de las prestaciones para la interfaz de usuario secundaria.** Las [prestaciones](glossary.md) son propiedades visuales que sugieren cómo se usan los objetos. La tendencia es tener una interfaz de usuario con la que los usuarios puedan interactuar en su lugar, pero para que toda la interfaz de usuario se dibuje en Scream "click me!" conduce a demasiado desorden visual. En el caso de la interfaz de usuario secundaria, a menudo es mejor usar prestaciones sutiles y dar los efectos completos al pasar el mouse.

    ![captura de pantalla de iconos de estrella usados para clasificar fotos ](images/progressive-disclosure-controls-image5.png)

    En este ejemplo, el campo clasificación es interactivo, pero no aparece hasta que el mouse se mantiene.

-   **Mostrar los pasos de seguimiento solo después de que se realicen los requisitos previos.** Este enfoque se utiliza mejor en las tareas conocidas en las que los usuarios pueden realizar los primeros pasos con confianza.

    ![captura de pantalla de cuadros de texto de nombre de usuario y contraseña ](images/progressive-disclosure-controls-image6.png)

    En este ejemplo, la página nombre de usuario y contraseña muestra inicialmente solo los cuadros nombre de usuario y contraseña opcional. Los cuadros confirmación y sugerencia se muestran después de que el usuario escriba una contraseña.

Aunque la divulgación progresiva es una excelente manera de simplificar las ius, tiene estos riesgos:

-   **Falta de capacidad de detección.** Los usuarios pueden suponer que si no pueden ver algo, no existe. Los usuarios no pueden mantener el mouse o hacer clic si no ven lo que buscan. Siempre existe la posibilidad de que los usuarios no puedan hacer clic en cosas como más opciones.
-   **Falta de estabilidad.** La revelación progresiva debe ser esperada o al menos sentir natural. Si los controles aparecen y desaparecen de forma inesperada, la interfaz de usuario resultante puede sentirse inestable.

### <a name="progressive-disclosure-controls"></a>Controles de divulgación progresiva

Los controles de divulgación progresiva se muestran normalmente sin etiquetas directas que describen su comportamiento, por lo que los usuarios deben poder hacer lo siguiente basándose solo en la apariencia visual del control:

-   Reconozca que el control proporciona una divulgación progresiva.
-   Determina si el estado actual es expandido o contraído.
-   Determine si se necesitan información, opciones o comandos adicionales para realizar la tarea.
-   Determine cómo restaurar el estado original, si lo desea.

Aunque los usuarios pueden determinar lo anterior mediante la prueba y el error, debe intentar hacer que dicha experimentación sea innecesaria.

Los controles de divulgación progresiva tienen una [prestaciones](glossary.md)bastante débiles, lo que significa que sus propiedades visuales sugieren cómo se usan, aunque es débil. En la tabla siguiente se compara la apariencia de los controles comunes de divulgación progresiva:



|                                                                                                                                                          |                                                                                                                                                                                                             |                                                                                                                                |                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| **Control**<br/>                                                                                                                                   | **Propósito**<br/>                                                                                                                                                                                      | **Aspecto**<br/>                                                                                                      | **Glifo indica**<br/> |
| **Comillas angulares**<br/> ![captura de pantalla de comillas angulares de apertura/derecha y arriba/abajo ](images/progressive-disclosure-controls-image7.png)<br/>                 | **Mostrar todo:** Mostrar u ocultar los elementos restantes en el contenido completamente o parcialmente oculto. Los elementos se muestran en su lugar (con un solo cheurón) o en un menú emergente (mediante un botón de contenido adicional doble).<br/> | Comillas angulares en la dirección en la que se producirá la acción.<br/>                                                        | Estado futuro<br/>        |
| **Flechas**<br/> ![captura de pantalla de flechas izquierda/derecha y arriba/abajo ](images/progressive-disclosure-controls-image8.png)<br/>                     | **Mostrar opciones:** Mostrar un menú emergente de comandos.<br/>                                                                                                                                                    | Las flechas apuntan a la dirección en la que se producirá la acción.<br/>                                                          | Estado futuro<br/>        |
| **Controles más y menos**<br/> ![captura de pantalla de dos pequeños botones de signo más y menos ](images/progressive-disclosure-controls-image9.png)<br/> | **Expanda contenedores:** Expandir o contraer el contenido del contenedor cuando se navega por una jerarquía.<br/>                                                                                        | Los símbolos más y menos no apuntan, pero la acción siempre se produce a su derecha.<br/>                                    | Estado futuro<br/>        |
| **Girar triángulos**<br/> ![captura de pantalla de dos pequeños triángulos ](images/progressive-disclosure-controls-image10.png)<br/>                  | **Mostrar detalles:** Mostrar u ocultar información adicional en su lugar para un elemento individual. También se usan para expandir contenedores.<br/>                                                                  | Los triángulos de rotación se asemejan ligeramente a las palancas de rotación, por lo que apuntan a la dirección en la que se ha producido la acción.<br/> | Estado actual<br/>       |



 

**Si solo hace algo...**

Los usuarios deben ser capaces de predecir el comportamiento del control de divulgación progresiva correctamente mediante inspección únicamente. Para ello, seleccione los patrones de uso adecuados y aplique el aspecto, la ubicación y el comportamiento de forma coherente.

## <a name="usage-patterns"></a>Patrones de uso

Los controles de divulgación progresiva tienen varios patrones de uso. Algunos de ellos están integrados en controles comunes.

### <a name="chevrons"></a>Comillas angulares

Las comillas angulares muestran u ocultan los elementos restantes en el contenido completamente o parcialmente oculto. Normalmente, los elementos se muestran en su lugar, pero también se pueden mostrar en un menú emergente. Cuando está en su lugar, el elemento permanece expandido hasta que el usuario lo contrae.

Las comillas angulares se utilizan de las siguientes maneras:



|                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Interfaz de usuario en contexto**<br/> el objeto asociado recibe el foco de entrada y el comilla simple se activa con la barra espaciadora.<br/>                       | ![captura de pantalla de la pantalla de estado de Security Center ](images/progressive-disclosure-controls-image11.png)<br/> En estos ejemplos, las comillas simples colocadas se colocan a la derecha de su control asociado.<br/>                                                                            |
| **Botones de comando con etiquetas externas**<br/> el botón de comando recibe el foco de entrada y el punto de comilla simple se activa con la barra espaciadora.<br/> | ![captura de pantalla de cheurones con la etiqueta ' más opciones ' ](images/progressive-disclosure-controls-image12.png)<br/> En este ejemplo, el botón de contenido adicional se etiqueta y se coloca a la izquierda de la etiqueta. Con este patrón, el botón sería difícil de entender sin su etiqueta.<br/> |
| **Botones de comando con etiquetas internas**<br/> el botón de comando recibe el foco de entrada y se activa con la barra espaciadora.<br/>                    | ![captura de pantalla de los botones de comando ' More ' y ' Less ' ](images/progressive-disclosure-controls-image13.png)<br/> En estos ejemplos, los botones de comando normales tienen comillas dobles colocadas para sugerir su significado.<br/>                                                                          |



 

### <a name="arrows"></a>Flechas

Las flechas muestran un menú emergente de comandos. El elemento permanece expandido hasta que el usuario realiza una selección o hace clic en cualquier lugar.

Si el botón de flecha es un control independiente, recibe el foco de entrada y se activa con la barra espaciadora. Si el botón de flecha tiene un control primario, el elemento primario recibe el foco de entrada y la flecha se activa con Alt + flecha abajo y Alt + flecha arriba, al igual que con el control de lista desplegable.

Las flechas se utilizan de las siguientes maneras:



|                                                                                       |                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Botones independientes**<br/> la flecha está en un control de botón independiente.<br/> | ![captura de pantalla de flechas a la derecha de los controles ](images/progressive-disclosure-controls-image14.png)<br/> En estos ejemplos, los botones de flecha situados a la derecha indican un menú de comandos.<br/>               |
| **Botones de comando**<br/> la flecha forma parte de un botón de comando.<br/>      | ![captura de pantalla de la etiqueta y la flecha del botón de comando ](images/progressive-disclosure-controls-image15.png)<br/> En estos ejemplos, los botones de menú y los botones de expansión tienen las flechas situadas a la derecha del texto.<br/> |



 

### <a name="plus-and-minus-controls"></a>Controles más y menos

Los controles más y menos se expanden o contraen para mostrar el contenido del contenedor al desplazarse por una jerarquía. El elemento permanece expandido hasta que el usuario lo contrae. Aunque se parezca a los botones, su comportamiento es local.

El objeto asociado recibe el foco de entrada. El signo más se activa con la tecla de dirección derecha y el signo menos con la tecla de dirección izquierda.

Los controles más y menos se utilizan de las siguientes maneras:



|                                                                                                |                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Árboles contraíbles**<br/> una jerarquía de varios niveles para mostrar el contenido del contenedor.<br/> | ![Captura de pantalla que muestra un árbol de carpetas del explorador de Windows con el "comportamiento" seleccionado.](images/progressive-disclosure-controls-image16.png)<br/> En este ejemplo, los controles más y menos se colocan a la izquierda del contenedor asociado.<br/>       |
| **Listas contraíbles**<br/> una jerarquía de dos niveles para mostrar el contenido del contenedor.<br/>   | ![captura de pantalla de la lista expandida para mostrar dos niveles ](images/progressive-disclosure-controls-image17.png)<br/> En este ejemplo, los controles más y menos se colocan a la izquierda del encabezado de lista asociado.<br/> |



 

### <a name="rotating-triangles"></a>Girar triángulos

Los triángulos de giro muestran u ocultan información adicional en su lugar para un elemento individual. También se usan para expandir contenedores. El elemento permanece expandido hasta que el usuario lo contrae.

El objeto asociado recibe el foco de entrada. El triángulo contraído (que señala a la derecha) se activa con la tecla de dirección derecha y el triángulo expandido (que apunta hacia abajo) con la tecla de dirección izquierda.

Los triángulos de rotación se utilizan de las siguientes maneras:



|                                                                                                            |                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Árboles contraíbles**<br/> una jerarquía de varios niveles para mostrar el contenido del contenedor.<br/>             | ![captura de pantalla del árbol de carpetas del explorador de Windows ](images/progressive-disclosure-controls-image18.png)<br/> En este ejemplo, los triángulos de rotación se colocan a la izquierda del contenedor asociado.<br/>       |
| **Listas contraíbles**<br/> una jerarquía de dos niveles para mostrar información adicional en contexto.<br/> | ![captura de pantalla de la lista que muestra datos adicionales ](images/progressive-disclosure-controls-image19.png)<br/> En este ejemplo, los triángulos de rotación se colocan a la izquierda de los elementos de lista asociados.<br/> |



 

### <a name="preview-arrows"></a>Flechas de vista previa

Como las comillas angulares, la información adicional se muestra u oculta en su lugar. El elemento permanece expandido hasta que el usuario lo contrae. A diferencia de las comillas angulares, los glifos tienen una representación gráfica de la acción, normalmente con una flecha que indica lo que ocurrirá.

![captura de pantalla de glifos de flecha que apuntan diagonalmente ](images/progressive-disclosure-controls-image20.png)

En estos ejemplos de Microsoft Windows Media Player, los glifos tienen flechas que sugieren la acción que se llevará a cabo.

Las flechas de vista previa se reservan mejor en situaciones en las que un botón de contenido adicional estándar no comunica adecuadamente el comportamiento del control, como cuando la divulgación es compleja o hay más de un tipo de divulgación.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Seleccione el patrón de divulgación progresiva en función de su uso.** Para obtener una descripción de cada patrón de uso, vea la tabla anterior.
-   **No use vínculos para controles de divulgación progresiva.** Use solo los controles de divulgación progresiva presentados en la sección patrones de uso. Sin embargo, use vínculos para navegar a los [temas de ayuda](winenv-help.md).

    **Correcto:**

    ![captura de pantalla de botón de contenido adicional con la etiqueta ' Mostrar mezclador ' ](images/progressive-disclosure-controls-image21.png)

    **Incorrecto:**

    ![captura de pantalla del texto del vínculo "Mostrar mezclador" ](images/progressive-disclosure-controls-image22.png)

    En el ejemplo incorrecto, se usa un vínculo para mostrar más opciones en su lugar. Este uso sería correcto si el vínculo se ha desplazado a otra página o cuadro de diálogo, o si se muestra un tema de ayuda.

### <a name="interaction"></a>Interacción

-   **En el caso de las comillas y flechas que no estén directamente etiquetadas, use la información sobre herramientas para describir lo que hacen.**

    ![captura de pantalla de la información sobre herramientas ' expandir el generador de consultas ' ](images/progressive-disclosure-controls-image23.png)

    En este ejemplo, la información sobre herramientas indica el efecto de un control Chevron sin etiquetar.

-   **Si un usuario expande o contrae un elemento, haga que el estado sea persistente para que surta efecto la próxima vez que se muestre la ventana**, a menos que sea probable que los usuarios prefieran a partir del estado predeterminado. Haga que el estado sea persistente en cada ventana y por usuario.
-   **Asegúrese de que todo el contenido expandido se puede contraer y viceversa, y de que la operación inversa es obvia.** De este modo, se fomenta la exploración y se reduce la frustración. La mejor manera de hacer que la operación inversa sea obvia es mantener el control en la misma ubicación fija. Si necesita trasladar el control, manténgalo en la misma ubicación relativa dentro de un área visualmente distinta.

    **Incorrecto:**

    ![captura de pantalla del botón "reemplazar" con cheurón ](images/progressive-disclosure-controls-image24.png)

    ![captura de pantalla del botón "reemplazar" sin cheurones ](images/progressive-disclosure-controls-image25.png)

    En este ejemplo, al hacer clic en el botón reemplazar con el botón de contenido adicional, se revela el cuadro **de texto reemplazar con** . Una vez hecho esto, el expansor de reemplazo se convierte en el comando Replace, por lo que no hay forma de restaurar el estado original.

-   **Use solo las claves de acceso adecuadas para el patrón de divulgación progresiva**, como se muestra en la sección patrones de uso. No use entrar para activar la divulgación progresiva.

### <a name="presentation"></a>Presentación

-   **No use puntas de flecha con forma de triangular para una finalidad distinta de la divulgación progresiva.**

    **Incorrecto:**

    ![captura de pantalla de la etiqueta con el triángulo que señala a la derecha ](images/progressive-disclosure-controls-image26.png)

    Aunque este ejemplo no es un patrón de divulgación progresiva, el uso de una flecha aquí sugiere que los comandos se mostrarán en una ventana emergente.

    **Correcto:**

    ![captura de pantalla de la etiqueta con la viñeta a la izquierda del texto ](images/progressive-disclosure-controls-image27.png)

    En este ejemplo, se usa una viñeta correctamente en su lugar.

-   **Quitar (no deshabilitar) controles de divulgación progresiva que no se aplican en el contexto actual.** Los controles de divulgación progresiva siempre deben entregar en su promesa, así que quítelos cuando no haya más información para proporcionar.

    **Incorrecto:**

    ![captura de pantalla de un control ' More Options ' atenuado ](images/progressive-disclosure-controls-image28.png)

    En este ejemplo, un control de divulgación progresiva que no se aplica está deshabilitado de forma incorrecta.

### <a name="chevrons"></a>Comillas angulares

-   **Use las comillas simples para mostrar u ocultar en su lugar. Use comillas angulares dobles para mostrar u ocultar mediante un menú emergente.** Sin embargo, siempre debe usar comillas dobles para los botones de comando con etiquetas internas.

    **Correcto:**

    ![captura de pantalla de un control de más opciones de comillas simples ](images/progressive-disclosure-controls-image29.png)

    **Incorrecto:**

    ![captura de pantalla de dos comillas angulares más control de opciones ](images/progressive-disclosure-controls-image30.png)

    En el ejemplo incorrecto, se usa un botón de contenido adicional doble para la divulgación progresiva en contexto.

    **Correcto:**

    ![captura de pantalla de dos comillas angulares más botón de comando ](images/progressive-disclosure-controls-image31.png)

    En este ejemplo, se usa un cheurón doble para la divulgación progresiva en contexto porque es un botón de comando con una etiqueta interna.

-   **Proporcione una relación visual entre el botón de contenido adicional y su control asociado.** Dado que las comillas angulares en contexto se colocan a la derecha de la interfaz de usuario asociada y se alinean a la derecha, puede haber bastante distancia entre un cheurón y su control asociado.

    **Correcto:**

    ![captura de pantalla de los controles de sombreado graduado detrás ](images/progressive-disclosure-controls-image32.png)

    En este ejemplo, hay una relación clara entre el cheurón en contexto y su interfaz de usuario asociada.

    **Incorrecto:**

    ![captura de pantalla de fondo sólido para controles ](images/progressive-disclosure-controls-image33.png)

    En este ejemplo, no hay ninguna relación visual clara entre el cheurón en contexto y su interfaz de usuario asociada, por lo que parece ser flotante en el espacio.

### <a name="arrows"></a>Flechas

-   **No use gráficos de flechas que puedan confundirse con los de retroceso, avance, avance o reproducción.** Use puntas de flecha con forma de triangular simple (flechas sin tallos) en los terrenos neutros.

    **Correcto:**

    ![captura de pantalla de dos triángulos negros pequeños ](images/progressive-disclosure-controls-image34.png)

    Estas flechas son claramente controles de divulgación progresivamente.

    **Incorrecto (para la divulgación progresiva):**

    ![captura de pantalla de dos flechas verdes pequeñas ](images/progressive-disclosure-controls-image35.png)

    Estas flechas no son similares a los controles de divulgación progresiva.

    **Incorrecto (para atrás, hacia delante):**

    ![captura de pantalla de dos botones con triángulos negros ](images/progressive-disclosure-controls-image36.png)

    Estas flechas tienen el mismo aspecto que los controles de divulgación progresiva, pero no lo son.

## <a name="recommended-sizing-and-spacing"></a>Ajuste de tamaño y espaciado recomendados

![captura de pantalla de tamaño y espaciado recomendados ](images/progressive-disclosure-controls-image37.png)

Ajuste de tamaño y espaciado recomendados para controles de divulgación progresiva.

## <a name="labels"></a>Etiquetas

-   Para las comillas angulares en un botón de comando con una etiqueta externa:
    -   Asigne una [clave de acceso](glossary.md)única. Para obtener instrucciones, consulte [teclado](inter-keyboard.md).
    -   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
    -   Escriba la etiqueta como una frase y no use ningún signo de puntuación final.
    -   Escriba la etiqueta para que describa el efecto de hacer clic en el botón y cambie la etiqueta cuando cambie el estado.
    -   Si la superficie muestra siempre algunas opciones, comandos o detalles, use los siguientes pares de etiquetas:
        -   **Más o menos opciones.** Se usa para las opciones o para una combinación de opciones, comandos y detalles.
        -   **Más o menos comandos.** Usar solo para comandos.
        -   **Más o menos detalles.** Se usa solo para información.
        -   **Más o menos <object name> .** Se usa para otros tipos de objetos, como las carpetas.
    -   De lo contrario:
        -   **Opciones de mostrar u ocultar.** Se usa para las opciones o para una combinación de opciones, comandos y detalles.
        -   **Mostrar u ocultar comandos.** Usar solo para comandos.
        -   **Mostrar u ocultar detalles.** Se usa solo para información.
        -   **Mostrar u ocultar <object name> .** Se usa para otros tipos de objetos, como las carpetas.
-   En el caso de las comillas angulares de un botón de comando con una etiqueta interna, siga las instrucciones estándar del [botón de comando](ctrl-command-buttons.md) .

## <a name="documentation"></a>Documentación

Al hacer referencia a controles de divulgación progresiva:

-   Si el control tiene una etiqueta fija, haga referencia al control solo por su etiqueta; No intente describir el control. Use el texto de etiqueta exacto, incluido el uso de mayúsculas, pero no incluya el carácter de subrayado de la tecla de acceso.
-   Si el control no tiene ninguna etiqueta o no se ha corregido, haga referencia al control por su tipo: botón de contenido adicional, flecha, triángulo o signo más/menos. Si es necesario, también se describe la ubicación del control. Si el control aparece de forma dinámica, como el control de espacio de la [Página](glossary.md) , inicie la referencia describiendo cómo hacer que aparezca el control.

    **Ejemplo:** Para mostrar los archivos de una carpeta, mueva el puntero al principio del nombre de la carpeta y, a continuación, haga clic en el triángulo situado junto a la carpeta.

-   No haga referencia al control como un botón, a menos que contraste con otros controles de divulgación progresiva que no sean botones.
-   Para describir la interacción del usuario, use haga clic en. Si es necesario para mayor claridad, use hacer clic... para expandir o contraer.
-   Siempre que sea posible, dé formato a la etiqueta usando texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.

Ejemplos:

-   (Para un cheurón) Para determinar el tamaño del archivo, haga clic en **detalles**.
-   (Para una flecha) Para ver todas las opciones, haga clic en la flecha situada junto al cuadro de **búsqueda** .
-   (Para más/menos) Para ver la imagen, haga clic en **imágenes**.

