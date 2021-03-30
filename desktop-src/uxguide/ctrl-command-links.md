---
title: Vínculos de comandos
description: Con los vínculos de comandos, los usuarios seleccionan una sola respuesta a una instrucción principal y, al hacerlo, pasan al siguiente paso de una tarea.
ms.assetid: a77819b1-9a32-4468-94fb-3f73a469fb81
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 29031b4456950db6ceff30d75b354dece92c5897
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "103820074"
---
# <a name="command-links"></a>Vínculos de comandos

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Con los vínculos de comandos, los usuarios seleccionan una sola respuesta a una instrucción principal y, al hacerlo, pasan al siguiente paso de una tarea.

Los vínculos de comandos tienen una apariencia clara y ligera que permite etiquetas descriptivas y se muestran con una flecha estándar o un icono personalizado, y una explicación complementaria opcional.

![captura de pantalla de un cuadro de diálogo de vínculo de comando típico ](images/ctrl-command-links-image1.png)

Conjunto típico de vínculos de comandos.

Los vínculos de comandos son similares a los [botones de radio](ctrl-radio-buttons.md) en que se usan para seleccionar entre un conjunto de opciones relacionadas mutuamente excluyentes. Al igual que los botones de radio, los vínculos de comandos siempre se presentan en conjuntos, nunca de forma individual. En apariencia, los vínculos de comandos tienen una apariencia ligera similar a la de los [vínculos](ctrl-links.md)normales, sin un marco u otra [prestación](glossary.md)de clics fuerte. Los vínculos de comandos también son similares a los [botones de comando](ctrl-command-buttons.md), ya que pueden ser el "botón de comando" predeterminado y pueden tener una clave de acceso asignada. Al igual que los [botones de confirmación](glossary.md), al hacer clic se cierra la ventana (para los cuadros de diálogo) o se pasa a la página siguiente (para los flujos de asistentes y páginas).

> [!Note]  
> Las instrucciones relacionadas con los [vínculos](ctrl-links.md) y el [diseño](vis-layout.md) se presentan en artículos independientes.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿Las opciones responden a la instrucción principal y están relacionadas con el propósito principal de la ventana o la página?** ¿Los usuarios deben responder a ellos para hacer algo distinto a navegar a una página diferente? Si no es así, use otro control, como botones de comando o vínculos. Los vínculos de comandos no son adecuados para las opciones secundarias u opcionales, o para la navegación pura.

    ![captura de pantalla de un elemento personalizar panel de control ](images/ctrl-command-links-image2.png)

    Aunque el elemento de panel de control de personalización tiene el mismo aspecto que los vínculos de comandos, las opciones son vínculos normales porque esta [página del concentrador](winenv-ctrl-panels.md) es para la navegación pura.

-   **¿Se usa el control para elegir una respuesta de un conjunto de respuestas mutuamente excluyentes?** Si no es así, usa otro control. Para que los usuarios puedan elegir comandos individuales, use los botones de comando o los vínculos.
-   **Para los cuadros de diálogo, hace clic en el control cerrar la ventana?** Si no es así, use un control que no requiera cerrar la ventana, como botones de radio, botones de comando o vínculos.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo Configuración de firewall con pestañas ](images/ctrl-command-links-image3.png)

    Los vínculos de comandos no se pueden usar en ventanas de propiedades o cuadros de diálogo con pestañas porque al hacer clic en el control se cierra la ventana.

-   **En el caso de los asistentes y los flujos de páginas, hace clic en pasar a la página siguiente sin compromiso?** No use vínculos de comandos para confirmar una tarea; en su lugar, use los botones de confirmación. Dado que los vínculos de comandos tienen el mismo aspecto que los vínculos y los usuarios asocian vínculos con navegación dentro de un flujo de páginas, los vínculos no son adecuados para [las páginas de confirmación](glossary.md) , ya que los usuarios siempre deberían ser capaces de volver atrás.
-   **Para los asistentes y los flujos de páginas, ¿hay otras páginas que usan vínculos de comandos?** Si es así, y todos los demás factores son iguales, prefiere vínculos de comandos para mantener la coherencia entre las páginas.
-   **¿El número de respuestas entre dos y cinco?** Nunca debe haber un vínculo de comando único. Dado que los vínculos de comandos son controles grandes y el espacio de pantalla utilizado es proporcional al número de opciones, mantenga el número de respuestas en cinco o menos. Para seis o más opciones, use los botones de radio, los vínculos normales o una [vista de lista](ctrl-list-views.md)de selección única.

    ![captura de pantalla del cuadro de diálogo con la lista de comandos ](images/ctrl-command-links-image4.png)

    En este ejemplo, la característica reproducción automática de Microsoft Windows usa una vista de lista.

-   **¿Una combinación de botones de radio y un botón confirmar es una opción mejor?** Los botones de radio son una opción mejor cuando se cumple cualquiera de las siguientes condiciones:
    -   **Hay una opción predeterminada segura que quiere que la mayoría de los usuarios seleccionen.** Es menos probable que los usuarios cambien un botón de radio predeterminado que un vínculo de comando predeterminado especialmente en un asistente, donde los usuarios están acostumbrados a hacer clic en siguiente para aceptar los valores predeterminados adecuados. Por otro lado, los vínculos de comandos son una opción mejor si desea animar a los usuarios a tomar una decisión explícita.
    -   **Los usuarios deben interactuar con las opciones (quizás para ver información adicional) antes de tomar una decisión.** Por ejemplo, si se selecciona un botón de radio, es posible que se muestre una descripción de la opción dinámicamente.

        ![captura de pantalla del cuadro de diálogo con botones de radio ](images/ctrl-command-links-image5.png)

        En este ejemplo, al seleccionar un botón de radio, se muestra una descripción de la opción.

    -   **Hay opciones secundarias o relacionadas en la página.** Los vínculos de comandos tienden a dominar la página, por lo que es fácil pasarlo por alto. Además, una vez que se hace clic en un vínculo de comando, es imposible seleccionar las opciones secundarias.

        **Incorrecto:**

        ![captura de pantalla del cuadro de diálogo con controles mixtos ](images/ctrl-command-links-image6.png)

        En este ejemplo, hay dos maneras diferentes de responder a la instrucción principal. No se usó un vínculo de comando para la primera respuesta porque sería difícil seleccionar las opciones secundarias.

        **Correcto:**

        ![captura de pantalla del cuadro de diálogo con los mismos controles ](images/ctrl-command-links-image7.png)

        En este ejemplo, los botones de radio hacen que las respuestas sean claras y permiten a los usuarios seleccionar opciones secundarias.

-   **En los cuadros de diálogo, ¿sería un grupo de botones de confirmación una opción mejor?** Los vínculos de comandos funcionan mejor cuando las opciones requieren más, respuestas más explicativas y explicaciones complementarias, pero un grupo de botones de confirmación es una opción mejor si hay algunas opciones sencillas.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo con guardar y no guardar ](images/ctrl-command-links-image8.png)

    En este ejemplo, el uso de vínculos de comandos para comandos simples hace que el cuadro de diálogo sea innecesariamente complicado.

    **Correcto:**

    ![Captura de pantalla que muestra un cuadro de diálogo con los botones de confirmación "guardar", "no guardar" y "Cancelar".](images/ctrl-command-links-image9.png)

    En este ejemplo, el uso de botones de confirmación simples se obtiene directamente en el punto.

    Sin embargo, los vínculos de comandos autoexplicativos siempre son mejores cuando se usa texto para explicar los botones de confirmación.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo con texto innecesario ](images/ctrl-command-links-image10.png)

    En este ejemplo, el texto se usa para explicar los botones de confirmación.

    **Correcto:**

    ![captura de pantalla de las etiquetas que no necesitan más texto ](images/ctrl-command-links-image11.png)

    En este ejemplo, los vínculos de comando se explican por sí solos.

> [!Note]  
> Los vínculos de comandos requieren Windows Vista o posterior, por lo que no son adecuados para versiones anteriores de Windows. Puede usar los vínculos normales como sustituto.

 

![captura de pantalla de vínculos normales con iconos y texto ](images/ctrl-command-links-image12.png)

En este ejemplo, se usan vínculos regulares con un icono y una explicación complementaria como sustituto de los vínculos de comandos de Windows XP.

## <a name="design-concepts"></a>Conceptos de diseño

El hecho de que los vínculos de comandos le permitan usar etiquetas más descriptivas y explicaciones complementarias opcionales no significa que deba hacerlo. Considere el ejemplo siguiente:

**Incorrecto:**

![captura de pantalla del cuadro de diálogo con demasiado texto ](images/ctrl-command-links-image13.png)

Este cuadro de diálogo está seriamente en la comunicación.

Este cuadro de diálogo toma una pregunta sencilla y complica innecesariamente el texto del vínculo del comando. Los usuarios no quieren leer todo ese texto para responder a estas preguntas.

Para simplificar este cuadro de diálogo, se pueden aplicar tres instrucciones de vínculo de comando:

-   **No use una explicación complementaria que sea una reformación en el vínculo de comandos.** Use una explicación complementaria solo si no puede hacer que un vínculo de comando sea autoexplicativo. Proporcionar una explicación complementaria para un vínculo de comando no significa que tenga que proporcionarlos para todos los comandos.
-   **Seleccione el más seguro (para evitar la pérdida de datos o el acceso al sistema) y la respuesta más segura como valor predeterminado.** Si seguridad y seguridad no son factores, seleccione la respuesta más probable o cómoda.
-   **Proporcione un botón Cancelar explícito.** No utilice un vínculo de comando con este fin.

Al aplicar estas instrucciones, podemos eliminar las explicaciones complementarias innecesarias, hacer que la respuesta más cómoda sea la predeterminada y proporcionar un botón Cancelar explícito.

**Manera**

![captura de pantalla del cuadro de diálogo con comandos y etiquetas ](images/ctrl-command-links-image14.png)

Una versión mejorada con vínculos de comandos más sencillos.

Aunque es cierto que esta versión no se explica explícitamente que no guardar se cuenta como una pérdida, pocos usuarios cambiarán su decisión en función de esta información, lo que lo convierte en un buen equilibrio.

Este cuadro de diálogo podría mejorarse aún más si se analizan los vínculos de comandos o no, ni siquiera el control adecuado para usar en este caso. Los botones de confirmación son realmente una opción mejor, ya que no se necesitan más respuestas más explicativas.

**Rendimiento**

![captura de pantalla del cuadro de diálogo con botones de confirmación ](images/ctrl-command-links-image15.png)

La versión correcta utiliza los botones de confirmación para ir directamente al punto.

Los vínculos de comandos tienen muchas ventajas, pero cuando se usan de modo inprudente, generan una mayor comunicación. En los cuadros de diálogo, considere la posibilidad de usar los botones de confirmación primero y usar los vínculos de comandos solo si los botones de confirmación no hacen el trabajo correctamente.

**Cuando se usa correctamente, los vínculos de comandos deben simplificar y aclarar la interfaz de usuario.** Si los resultados son los opuestos, vuelva al paso anterior, revise las alternativas y céntrese en lo que realmente necesita para comunicarse.

**Si solo hace algo...** No use vínculos de comandos para la comunicación excesiva. Los vínculos de comandos deben simplificar y aclarar la comunicación, no hacer que sea más complicada.

## <a name="usage-patterns"></a>Patrones de uso

Los vínculos de comandos tienen varios patrones de uso:



|                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Respuestas de página** Los vínculos de comandos se usan para responder a la instrucción principal y pasar a la página siguiente.    | con este patrón, los vínculos de comando reemplazan el botón siguiente, pero todavía hay un botón Cancelar.<br/>Las respuestas de página no implican ningún compromiso. Dado que los vínculos de comandos parecen similares a los vínculos y los usuarios asocian vínculos con navegación dentro de un flujo de páginas, los vínculos no son adecuados para las páginas de confirmación. los usuarios siempre deben ser capaces de realizar la copia de seguridad. <br/> ![Captura de pantalla que muestra un cuadro de diálogo "conectar a Internet" con los vínculos de comandos "inalámbrico", "banda ancha (PPPoE)" y "acceso telefónico".](images/ctrl-command-links-image16.png)<br/>En este ejemplo, se usan vínculos de comandos para proporcionar respuestas descriptivas a la instrucción principal. Aunque los botones de radio se pueden usar aquí, los vínculos de comandos permiten a los usuarios responder con un solo clic.<br/> |
| **Respuestas del cuadro de diálogo** Los vínculos de comandos se usan para responder a la instrucción principal y cerrar el cuadro de diálogo.  | con este patrón, los vínculos de comando reemplazan los botones de confirmación (como aceptar), pero todavía hay un botón Cancelar.<br/>A diferencia de los flujos de páginas, no hay ninguna manera de devolver una respuesta basada en cuadros de diálogo una vez realizada. por lo tanto, los vínculos de comandos del cuadro de diálogo implican un compromiso. <br/> ![captura de pantalla del cuadro de diálogo con vínculos de comandos ](images/ctrl-command-links-image17.png)<br/>En este ejemplo, se usan vínculos de comandos para proporcionar respuestas descriptivas a la instrucción principal. Aunque los botones de radio se pueden usar aquí, los vínculos de comandos permiten a los usuarios elegir con un solo clic.<br/>                                                   |
| **Respuestas detalladas** Una respuesta de página o cuadro de diálogo que incluye información detallada.                          | en ocasiones, es posible que los usuarios necesiten información más detallada para elegir su respuesta. <br/> ![captura de pantalla del cuadro de diálogo copiar archivo y miniaturas ](images/ctrl-command-links-image18.png)<br/> En este ejemplo, se usan vínculos de comandos detallados para que los usuarios puedan tomar decisiones fundamentadas. Las miniaturas y los detalles de archivo ayudan a los usuarios a decidir.<br/>                                                                                                                                                                                                                                                                                                         |



 

## <a name="guidelines"></a>Directrices

### <a name="interaction"></a>Interacción

-   **Muestra un puntero ocupado si el resultado de hacer clic en un vínculo de comando no es instantáneo.** Sin comentarios, los usuarios pueden suponer que el clic no se ha producido y hacer clic de nuevo.

### <a name="presentation"></a>Presentación

-   **Siempre hay vínculos de comandos en un conjunto de dos o más.** Lógicamente, no hay ningún motivo para formular una pregunta con una sola respuesta.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo con un vínculo de comando ](images/ctrl-command-links-image19.png)

    En este ejemplo, el cuadro de diálogo parece ofrecer al usuario una opción, pero solo hay una instrucción. En su lugar, debe ser un cuadro de diálogo informativo.

-   **Presente primero los vínculos de comandos que se usan con más frecuencia.** El orden resultante debe seguir aproximadamente la probabilidad de uso, pero también tiene un flujo lógico.
    -   **Excepción:** Los vínculos de comandos que dan lugar a hacer todo deben colocarse en primer lugar.
-   **Proporcione un botón Cancelar explícito.** No utilice un vínculo de comando con este fin. Con bastante frecuencia, los usuarios saben que no quieren realizar una tarea. El uso de un vínculo de comando para cancelar requeriría a los usuarios leer detenidamente todos los vínculos de comandos para determinar cuál de ellas significa cancelar. Tener un botón Cancelar explícito permite a los usuarios cancelar una tarea de forma eficaz.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo con el vínculo ' no salir ' ](images/ctrl-command-links-image20.png)

    En este ejemplo, el vínculo de comando no salir debe ser un botón Cancelar.

-   **Si proporcionar un botón Cancelar explícito deja un solo vínculo de comando, proporcione un vínculo de comando para cancelar y un botón Cancelar.** Si lo hace, deja claro que los usuarios tienen la opción de elegir. Frase este vínculo de comando en términos de cómo difiere de la primera respuesta, en lugar de simplemente "Cancelar" o alguna variación.

    ![captura de pantalla de dos vínculos y un botón Cancelar ](images/ctrl-command-links-image21.png)

    En este ejemplo, el segundo vínculo de comando indica que el usuario tiene una opción, pero todo lo que hace es cancelar. Sin embargo, se formula en términos de diferencias con respecto al primer vínculo de comando.

-   **Use cerrar en lugar de cancelar si no puede devolver el entorno a su estado anterior, sin dejar ningún efecto secundario.**
-   **No Mostrar vínculos de comandos deshabilitados.** Si un vínculo de comando no se aplica al contexto actual, quítelo en su lugar. Si la eliminación de todos los vínculos de comandos que no se aplican deja un solo vínculo de comando, elimine la ventana o la página, o bien muestre una [confirmación](mess-confirm.md) si es necesario el consentimiento explícito del usuario.

### <a name="icons"></a>Iconos

-   **Todos los vínculos de comandos necesitan un icono.** Los iconos ayudan a los usuarios a distinguir los vínculos de comandos de los vínculos normales y el texto de la interfaz de usuario.
-   **Use el icono de flecha solo para los vínculos de comandos.** Los vínculos normales no deben usar el icono de flecha a menos que se usen como sustituto de los vínculos de comandos de Windows XP.
-   **Use el icono de escudo de seguridad para indicar que una respuesta requiere una elevación inmediata.** Para obtener instrucciones adicionales sobre cómo usar el icono de escudo de seguridad, vea el [control de cuentas de usuario](winenv-uac.md).
-   **Use iconos personalizados solo si ayudan a los usuarios a identificar visualmente y diferenciar las opciones.** No use iconos personalizados si no son reconocibles o significativos de inmediato.

    **Incorrecto:**

    ![captura de pantalla de dos vínculos de comandos con iconos personalizados ](images/ctrl-command-links-image22.png)

    En este ejemplo, los iconos personalizados no se reconocen inmediatamente.

-   **En el caso de los iconos personalizados, use los iconos 16x16 o 32x32 píxeles.** Use los iconos más grandes si hay suficiente espacio y se beneficiarán visualmente del tamaño mayor. Si necesita superposiciones de escudo de seguridad, use los iconos de píxel 32x32 o 48x48.

    ![captura de pantalla de tres vínculos de comandos con iconos ](images/ctrl-command-links-image23.png)

    En este ejemplo se usan iconos personalizados de 32x32 píxeles.

    ![captura de pantalla de dos vínculos de comandos con iconos más grandes ](images/ctrl-command-links-image24.png)

    En este ejemplo se usan iconos personalizados de píxeles de 48x48, con una superposición de escudo de seguridad.

-   **Evite mezclar iconos personalizados con el icono de flecha estándar en una ventana o una página.** Si usa un icono personalizado en una superficie, intente utilizar todos los iconos personalizados. No obstante, se prefiere el icono de flecha estándar sobre iconos personalizados sin sentido.

### <a name="default-values"></a>Valores predeterminados

-   **Seleccione el más seguro (para evitar la pérdida de datos o el acceso al sistema) y la respuesta más segura como valor predeterminado.** Si seguridad y seguridad no son factores, seleccione la respuesta más probable o cómoda.
-   **Cuando sea práctico, convierta la primera respuesta en la opción predeterminada,** ya que los usuarios suelen esperar que el orden no sea lógico.
-   **En el caso de los cuadros de diálogo, no realice una acción destructiva en el vínculo de comando predeterminado** , a menos que haya una manera fácil de deshacer la acción.

## <a name="recommended-sizing-and-spacing"></a>Ajuste de tamaño y espaciado recomendados

![captura de pantalla de tamaño y espaciado de vínculo de comando ](images/ctrl-command-links-image25.png)

## <a name="labels"></a>Etiquetas

> [!Note]  
> Dado que los vínculos de comandos son respuestas a una instrucción principal, debe diseñar una [buena instrucción principal](text-ui.md) antes de determinar sus respuestas.

 

**Etiquetas de vínculo de comando**

-   **Elija una etiqueta concisa que se comunique claramente y diferencie el vínculo del comando.** Debe ser autoexplicativo y corresponder a la instrucción principal. Centre las etiquetas en las diferencias entre las respuestas. Los usuarios no deben tener que averiguar cuál es realmente el vínculo del comando o cómo difiere de otros vínculos de comandos.

    **Incorrecto:**

    ![captura de pantalla de un vínculo de comando redundante ](images/ctrl-command-links-image26.png)

    En este ejemplo, ¿cuál es la diferencia entre las respuestas segunda y tercera? ¿No está contento de que haya un botón Cancelar?

-   **Las etiquetas de vínculo del comando Focus ayudan a los usuarios a tomar la decisión correcta.** Omitir los detalles que no afectan a la elección. Las etiquetas no tienen que ser una especificación completa de lo que ocurrirá.
-   **Iniciar vínculos de comandos con un verbo.** No usar haga clic, sin embargo, porque la etiqueta debe comunicar lo que hace el vínculo de comando, no cómo funciona.
    -   **Excepción:** Si todos los vínculos de comandos comienzan por el mismo verbo o frase, elimine el verbo o la frase redundantes.
-   En general, **use frases positivas** (lo que proporciona una opción para hacer algo). La formulación negativa (que proporciona una opción para no hacer algo) es aceptable si hace que las etiquetas sean más fáciles de entender.
-   **Usar las etiquetas de una sola línea y frases paralelas.** Las etiquetas largas desaconsejan la lectura y no deben ser necesarias. Además, las etiquetas de tamaño moderado son más fáciles de consultar en la documentación de.
-   **Use mayúsculas de estilo de frase.**
-   **No use la puntuación final a menos que la etiqueta sea una pregunta.**
-   **Asigne una clave de acceso única.** Para obtener instrucciones, consulte [teclado](inter-keyboard.md).
-   **No use puntos suspensivos.** Los puntos suspensivos indican que es posible que se necesite más información para realizar la acción. Los vínculos de comandos usados correctamente no necesitan puntos suspensivos porque tienen un efecto inmediato.
-   **Si se recomienda una respuesta, agregue "(recomendado)" a la etiqueta.** Asegúrese de agregar a la etiqueta, no de la explicación complementaria.
-   **Si una respuesta está pensada solo para usuarios avanzados, considere la posibilidad de agregar "(avanzado)" a la etiqueta.** Asegúrese de agregar a la etiqueta, no de la explicación complementaria.

**Sugerencia:** Puede evaluar los vínculos de comandos si se imagina que un amigo indicó la instrucción principal y respondió con los vínculos de comandos. Si la respuesta a los vínculos de comandos no sería natural o complicada, revise los vínculos de comando y, posiblemente, la instrucción principal.

**Explicaciones complementarias**

-   Si un vínculo de comando requiere una explicación más detallada, **proporcione una explicación complementaria**. Las explicaciones complementarias describen el motivo por el que los usuarios pueden elegir una respuesta o lo que sucede si se elige una respuesta.

    ![captura de pantalla de texto que describe los resultados de la opción ](images/ctrl-command-links-image27.png)

    En este ejemplo, la explicación complementaria describe las implicaciones de la opción.

-   **No use una explicación complementaria que sea la reutilización en palabras del vínculo de comandos.** Use una explicación complementaria solo si no puede hacer que un vínculo de comando sea autoexplicativo. Proporcionar una explicación complementaria para un vínculo de comando no significa que tenga que proporcionarlos para todo.
-   **Céntrese en las explicaciones complementarias sobre cómo ayudar a los usuarios a tomar la decisión adecuada.** Omitir los detalles que no afectan a la elección. Las explicaciones complementarias no tienen que ser una especificación completa de lo que ocurrirá.
-   **Usar frases paralelas y como máximo tres líneas de texto.** Las explicaciones complementarias largas desaconsejan la lectura y no deben ser necesarias.
-   **Usar frases completas y puntuación final.**

**Etiquetas de grupo de vínculos de comandos**

-   **No use etiquetas de grupo.** Las instrucciones principales actúan como etiqueta de grupo para los vínculos de comandos.

## <a name="documentation"></a>Documentación

Al hacer referencia a vínculos de comandos:

-   Use el texto de etiqueta exacto, incluido el uso de mayúsculas, pero no incluya el carácter de subrayado de la tecla de acceso.
-   Si la etiqueta incluye un nombre de objeto, omita el nombre del objeto o use el texto del marcador de posición.
-   Para describir la interacción del usuario, use haga clic en.
-   Siempre que sea posible, dé formato a la etiqueta usando texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.

**Ejemplos:** Para copiar la imagen, haga clic en **copiar y reemplazar**.

Haga clic en **restablecer el adaptador de red**. (Para un vínculo de comando con la etiqueta "restablecer el *nombre de adaptador* de adaptador de red").

 

