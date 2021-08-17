---
title: Vínculos de comandos
description: Con los vínculos de comandos, los usuarios seleccionan una única respuesta a una instrucción principal y, al hacerlo, avanzan al paso siguiente de una tarea.
ms.assetid: a77819b1-9a32-4468-94fb-3f73a469fb81
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ac24618b70d96b1b625549582af27e47b5386f354f09e7147000fc5ed438a36f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091131"
---
# <a name="command-links"></a>Vínculos de comandos

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Con los vínculos de comandos, los usuarios seleccionan una única respuesta a una instrucción principal y, al hacerlo, avanzan al paso siguiente de una tarea.

Los vínculos de comandos tienen una apariencia limpia y ligera que permite etiquetas descriptivas y se muestran con una flecha estándar o un icono personalizado, y una explicación complementaria opcional.

![captura de pantalla de un cuadro de diálogo de vínculo de comando típico ](images/ctrl-command-links-image1.png)

Un conjunto típico de vínculos de comandos.

Los vínculos de comandos son similares a los botones de [radio](ctrl-radio-buttons.md) en que se usan para seleccionar entre un conjunto de opciones mutuamente excluyentes y relacionadas. Al igual que los botones de radio, los vínculos de comandos siempre se presentan en conjuntos, nunca individualmente. En apariencia, los vínculos de comandos tienen un aspecto ligero similar a los [vínculos](ctrl-links.md)normales, sin un marco u otras condiciones de clic [seguras.](glossary.md) Los vínculos de comando también son similares a [los botones](ctrl-command-buttons.md)de comando, ya que pueden ser el "botón de comando" predeterminado y pueden tener asignada una clave de acceso. Al [igual que los botones](glossary.md)de confirmación, al hacer clic, cierran la ventana (para cuadros de diálogo) o avanzan a la página siguiente (para los asistentes y flujos de páginas).

> [!Note]  
> Las directrices relacionadas [con los vínculos](ctrl-links.md) [y el](vis-layout.md) diseño se presentan en artículos independientes.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿Las respuestas de las opciones a la instrucción principal están relacionadas con el propósito principal de la ventana o página?** ¿Los usuarios deben responder a ellos para hacer algo que no sea simplemente navegar a otra página? Si no es así, use otro control, como botones de comando o vínculos. Los vínculos de comandos no son adecuados para opciones secundarias u opcionales, ni para la navegación pura.

    ![captura de pantalla de un elemento del panel de control personalizar ](images/ctrl-command-links-image2.png)

    Aunque el elemento personalization Panel de control parece que usa vínculos de comandos, [](winenv-ctrl-panels.md) las opciones son vínculos normales porque esta página central es para la navegación pura.

-   **¿Se usa el control para elegir una respuesta de un conjunto de respuestas mutuamente excluyentes?** Si no es así, usa otro control. Para permitir que los usuarios elijan comandos individuales, use botones de comando o vínculos.
-   **Para los cuadros de diálogo, ¿al hacer clic en el control se cierra la ventana?** Si no es así, use un control que no requiera cerrar la ventana, como botones de radio, botones de comando o vínculos.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo configuración de firewall con pestañas ](images/ctrl-command-links-image3.png)

    Los vínculos de comandos no se pueden usar en ventanas de propiedades ni en diálogos con pestañas porque al hacer clic en el control se cierra la ventana.

-   **Para los asistentes y los flujos de página, ¿el clic avanza a la página siguiente sin compromiso?** No use vínculos de comando para confirmar una tarea; use botones de confirmación en su lugar. Dado que los vínculos de comandos parecen vínculos y los usuarios [](glossary.md) asocian vínculos a la navegación dentro de un flujo de página, los vínculos no son adecuados para las páginas de confirmación, ya que los usuarios siempre deben poder realizar una copia de seguridad.
-   **Para los asistentes y los flujos de página, ¿otras páginas usan vínculos de comandos?** Si es así, y todos los demás factores son iguales, se prefieren vínculos de comandos para mantener la coherencia entre páginas.
-   **¿El número de respuestas está entre dos y cinco?** Nunca debe haber un solo vínculo de comando. Dado que los vínculos de comandos son controles grandes y el espacio de pantalla utilizado es proporcional al número de opciones, mantenga el número de respuestas en cinco o menos. Para seis o más opciones, use botones de radio, vínculos normales o una vista de lista [de selección única.](ctrl-list-views.md)

    ![captura de pantalla del cuadro de diálogo con la lista de comandos ](images/ctrl-command-links-image4.png)

    En este ejemplo, la característica Reproducción automática de Microsoft Windows una vista de lista.

-   **¿Sería mejor una combinación de botones de radio y un botón de confirmación?** Los botones de radio son una mejor opción cuando se cumple alguna de las siguientes condiciones:
    -   **Hay una opción predeterminada segura que desea que la mayoría de los usuarios seleccionen.** Es menos probable que los usuarios cambien un botón de radio predeterminado que un vínculo de comando predeterminado, especialmente en un asistente, donde los usuarios están acostumbrados a hacer clic en Siguiente para aceptar los valores predeterminados adecuados. Por otro lado, los vínculos de comandos son una mejor opción si desea animar a los usuarios a realizar una elección explícita.
    -   **Los usuarios deben interactuar con las opciones (quizás para ver información adicional) antes de tomar una decisión.** Por ejemplo, al seleccionar un botón de radio se puede mostrar dinámicamente una descripción sobre la opción.

        ![captura de pantalla del cuadro de diálogo con botones de radio ](images/ctrl-command-links-image5.png)

        En este ejemplo, al seleccionar un botón de radio se muestra una descripción de la opción.

    -   **Hay opciones secundarias o relacionadas en la página.** Los vínculos de comandos tienden a dominar la página, lo que facilita pasar por alto todo lo demás. Además, una vez que se hace clic en un vínculo de comando, es imposible seleccionar opciones secundarias.

        **Incorrecto:**

        ![captura de pantalla del cuadro de diálogo con controles mixtos ](images/ctrl-command-links-image6.png)

        En este ejemplo, hay dos maneras diferentes de responder a la instrucción principal. No se usó un vínculo de comando para la primera respuesta porque sería difícil seleccionar opciones secundarias.

        **Correcto:**

        ![captura de pantalla del cuadro de diálogo con los mismos controles ](images/ctrl-command-links-image7.png)

        En este ejemplo, los botones de radio borran las respuestas, al tiempo que permiten a los usuarios seleccionar opciones secundarias.

-   **En el caso de los cuadros de diálogo, ¿sería mejor un grupo de botones de confirmación?** Los vínculos de comandos funcionan mejor cuando las opciones requieren respuestas más largas y explicativas y explicaciones complementarias, pero un grupo de botones de confirmación es una mejor opción si hay algunas opciones sencillas.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo con guardar y no guardar ](images/ctrl-command-links-image8.png)

    En este ejemplo, el uso de vínculos de comandos para comandos simples hace que el cuadro de diálogo sea innecesariamente complicado.

    **Correcto:**

    ![Captura de pantalla que muestra un cuadro de diálogo con los botones de confirmación "Guardar", "No guardar" y "Cancelar".](images/ctrl-command-links-image9.png)

    En este ejemplo, el uso de botones de confirmación simples llega directamente al punto.

    Sin embargo, los vínculos de comandos autoexplicativos siempre son una mejor opción cuando se usa texto para explicar los botones de confirmación.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo con texto innecesario ](images/ctrl-command-links-image10.png)

    En este ejemplo, se usa texto para explicar los botones de confirmación.

    **Correcto:**

    ![captura de pantalla de etiquetas que no necesitan más texto ](images/ctrl-command-links-image11.png)

    En este ejemplo, los vínculos de comando se explican por sí solos.

> [!Note]  
> Los vínculos de comandos Windows Vista o versiones posteriores, por lo que no son adecuados para versiones anteriores de Windows. Puede usar vínculos normales como sustituto.

 

![captura de pantalla de vínculos normales con iconos y texto ](images/ctrl-command-links-image12.png)

En este ejemplo, se usan vínculos normales con un icono y una explicación complementaria como sustituto de los vínculos de comandos Windows XP.

## <a name="design-concepts"></a>Conceptos de diseño

El hecho de que los vínculos de comandos le permitan usar etiquetas más descriptivas y explicaciones complementarias opcionales no significa que deba hacerlo. Considere el ejemplo siguiente:

**Incorrecto:**

![captura de pantalla del cuadro de diálogo con demasiado texto ](images/ctrl-command-links-image13.png)

Este cuadro de diálogo se está comunicando demasiado.

Este cuadro de diálogo toma una pregunta simple y la complica innecesariamente con el texto del vínculo de comando. Los usuarios no quieren leer todo ese texto para preguntas tan sencillas.

Podemos simplificar este cuadro de diálogo aplicando tres directrices de vínculo de comando:

-   **No use una explicación complementaria que sea una nueva declaración de palabras del vínculo de comando.** Use una explicación complementaria solo cuando no pueda hacer que un vínculo de comando se explique por sí mismo. Proporcionar una explicación complementaria de un vínculo de comando no significa que tenga que proporcionarlos para todos los comandos.
-   **Seleccione la respuesta más segura (para evitar la pérdida de datos o el acceso del sistema) y la respuesta más segura para que sea la predeterminada.** Si la seguridad y la seguridad no son factores, seleccione la respuesta más probable o conveniente.
-   **Proporcione un botón Cancelar explícito.** No use un vínculo de comando para este propósito.

Al aplicar estas directrices, podemos eliminar las explicaciones complementarias innecesarias, hacer que la respuesta más cómoda sea la predeterminada y proporcionar un botón Cancelar explícito.

**Mejor:**

![captura de pantalla del cuadro de diálogo con comandos y etiquetas ](images/ctrl-command-links-image14.png)

Una versión mejorada con vínculos de comandos más sencillos.

Aunque es cierto que esta versión no explica explícitamente que no guardar se cuenta como una pérdida, pocos usuarios cambiarán su decisión en función de esta información, lo que hace que esto sea un buen ahorro.

Este cuadro de diálogo se puede mejorar aún más si se analiza si los vínculos de comandos son o no el control adecuado para usar en este caso. Los botones de confirmación son en realidad una mejor opción, ya que no se necesitan respuestas más largas y explicativas.

**Mejor:**

![captura de pantalla del cuadro de diálogo con botones de confirmación ](images/ctrl-command-links-image15.png)

La versión correcta usa botones de confirmación para llegar directamente al punto.

Los vínculos de comandos tienen muchas ventajas, pero cuando se usan de forma imprudente, conducen a una comunicación en exceso. En el caso de los cuadros de diálogo, considere la posibilidad de usar primero los botones de confirmación y use los vínculos de comando solo si los botones de confirmación no hacen bien el trabajo.

**Cuando se usan correctamente, los vínculos de comandos deben simplificar y aclarar la interfaz de usuario.** Si los resultados son los contrarios, repase las alternativas y céntrate en lo que realmente necesitas comunicar.

**Si solo hace una cosa...** No use vínculos de comandos para la comunicación en exceso. Los vínculos de comandos deben simplificar y aclarar la comunicación, no hacer que sea más complicada.

## <a name="usage-patterns"></a>Patrones de uso

Los vínculos de comandos tienen varios patrones de uso:



| Uso                                                                                                                      | Ejemplo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Respuestas de página** Los vínculos de comando se usan para responder a la instrucción principal y avanzar a la página siguiente.    | con este patrón, los vínculos de comando reemplazan al botón siguiente, pero todavía hay un botón cancelar.<br/>Las respuestas de página no implican el compromiso. Dado que los vínculos de comandos son como vínculos y los usuarios asocian vínculos a la navegación dentro de un flujo de página, los vínculos no son adecuados para las páginas de confirmación. los usuarios siempre deben poder hacer una copia de seguridad. <br/> ![Captura de pantalla que muestra un cuadro de diálogo "Conectar a Internet" con los vínculos de comandos "Inalámbrico", "Banda ancha (PPPoE)" y "Acceso telefónico".](images/ctrl-command-links-image16.png)<br/>En este ejemplo, se usan vínculos de comando para proporcionar respuestas descriptivas a la instrucción principal. Aunque aquí se pueden usar botones de radio, los vínculos de comandos permiten a los usuarios responder con un solo clic.<br/> |
| **Respuestas de cuadro de diálogo** Los vínculos de comando se usan para responder a la instrucción principal y cerrar el cuadro de diálogo.  | con este patrón, los vínculos de comando reemplazan los botones de confirmación (por ejemplo, aceptar), pero todavía hay un botón cancelar.<br/>A diferencia de los flujos de página, no hay ninguna manera de salir de una respuesta basada en cuadros de diálogo una vez realizada. Por lo tanto, los vínculos de comandos del cuadro de diálogo implican el compromiso. <br/> ![captura de pantalla del cuadro de diálogo con vínculos de comandos ](images/ctrl-command-links-image17.png)<br/>En este ejemplo, se usan vínculos de comando para proporcionar respuestas descriptivas a la instrucción principal. Aunque aquí se pueden usar botones de radio, los vínculos de comandos permiten a los usuarios elegir con un solo clic.<br/>                                                   |
| **Respuestas detalladas** Una respuesta de página o diálogo que incluye información detallada.                          | en ocasiones, es posible que los usuarios necesiten información más detallada para elegir su respuesta. <br/> ![captura de pantalla del cuadro de diálogo copiar archivo y miniaturas ](images/ctrl-command-links-image18.png)<br/> En este ejemplo, se usan vínculos de comandos detallados para que los usuarios puedan tomar decisiones informadas. Las miniaturas y los detalles del archivo ayudan a los usuarios a decidir.<br/>                                                                                                                                                                                                                                                                                                         |



 

## <a name="guidelines"></a>Directrices

### <a name="interaction"></a>Interacción

-   **Muestra un puntero ocupado si el resultado de hacer clic en un vínculo de comando no es instantáneo.** Sin comentarios, los usuarios podrían suponer que el clic no se ha hecho y hacer clic de nuevo.

### <a name="presentation"></a>Presentación

-   **Presente siempre vínculos de comando en un conjunto de dos o más.** Lógicamente, no hay ninguna razón para hacer una pregunta que solo tenga una respuesta.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo con un vínculo de comando ](images/ctrl-command-links-image19.png)

    En este ejemplo, el cuadro de diálogo parece ofrecer al usuario una opción, pero solo hay una instrucción. En su lugar, debe ser un cuadro de diálogo informativo.

-   **Presente primero los vínculos de comandos más usados.** El orden resultante debe seguir aproximadamente la probabilidad de uso, pero también tener un flujo lógico.
    -   **Excepción:** Primero se deben colocar los vínculos de comandos que hacen todo lo posible.
-   **Proporcione un botón Cancelar explícito.** No use un vínculo de comando para este propósito. Con frecuencia, los usuarios se dan cuenta de que no quieren realizar una tarea. El uso de un vínculo de comando para cancelar requeriría que los usuarios leyesen cuidadosamente todos los vínculos de comando para determinar cuál significa cancelar. Tener un botón Cancelar explícito permite a los usuarios cancelar una tarea de forma eficaz.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo con el vínculo "No salir" ](images/ctrl-command-links-image20.png)

    En este ejemplo, el vínculo del comando No salir debe ser un botón Cancelar.

-   **Si al proporcionar un botón Cancelar explícito se deja un único vínculo de comando, proporcione un vínculo de comando para cancelar y un botón Cancelar.** Al hacerlo, queda claro que los usuarios tienen una opción. Frasee este vínculo de comando en términos de su diferencia con respecto a la primera respuesta, en lugar de simplemente "Cancelar" o alguna variación.

    ![captura de pantalla de dos vínculos y un botón Cancelar ](images/ctrl-command-links-image21.png)

    En este ejemplo, el segundo vínculo de comando indica que el usuario tiene una opción, pero lo único que hace es cancelar. Sin embargo, se describe en términos de su diferencia con respecto al primer vínculo de comando.

-   **Use Cerrar en lugar de Cancelar si no puede devolver el entorno a su estado anterior, sin ningún efecto secundario.**
-   **No muestre vínculos de comandos deshabilitados.** Si un vínculo de comando no se aplica al contexto actual, quítelo en su lugar. Si la eliminación de todos los vínculos de comandos que no se aplican [](mess-confirm.md) deja un único vínculo de comando, elimine la ventana o página, o muestre una confirmación si se necesita el consentimiento explícito del usuario.

### <a name="icons"></a>Iconos

-   **Todos los vínculos de comandos necesitan un icono.** Los iconos ayudan a los usuarios a distinguir los vínculos de comandos de los vínculos normales y el texto de la interfaz de usuario.
-   **Use el icono de flecha solo para los vínculos de comandos.** Los vínculos normales no deben usar el icono de flecha a menos que se usen como sustituto de los vínculos de comandos Windows XP.
-   **Use el icono de escudo de seguridad para indicar que una respuesta requiere elevación inmediata.** Para obtener instrucciones adicionales sobre el uso del icono de escudo de seguridad, vea [Control de cuentas de usuario](winenv-uac.md).
-   **Use iconos personalizados solo si ayudan a los usuarios a identificar y diferenciar visualmente las opciones.** No use iconos personalizados si no son reconocibles ni significativos inmediatamente.

    **Incorrecto:**

    ![captura de pantalla de dos vínculos de comandos con iconos personalizados ](images/ctrl-command-links-image22.png)

    En este ejemplo, los iconos personalizados no son reconocibles inmediatamente.

-   **Para los iconos personalizados, use iconos de 16 x 16 o 32 x 32 píxeles.** Use los iconos más grandes si hay suficiente espacio y se benefician visualmente del tamaño mayor. Si necesita superposiciones de escudo de seguridad, use iconos de 32 x 32 o 48 x 48 píxeles.

    ![captura de pantalla de tres vínculos de comandos con iconos ](images/ctrl-command-links-image23.png)

    En este ejemplo se usan iconos personalizados de 32 x 32 píxeles.

    ![captura de pantalla de dos vínculos de comandos con iconos más grandes ](images/ctrl-command-links-image24.png)

    En este ejemplo se usan iconos personalizados de 48 x 48 píxeles, con una superposición de escudo de seguridad.

-   **Evite mezclar iconos personalizados con el icono de flecha estándar en una ventana o una página.** Si usa un icono personalizado en una superficie, intente usar todos los iconos personalizados. Sin embargo, prefiere el icono de flecha estándar en lugar de los iconos personalizados sin sentido.

### <a name="default-values"></a>Valores predeterminados

-   **Seleccione la respuesta más segura (para evitar la pérdida de datos o el acceso del sistema) y la respuesta más segura para que sea la predeterminada.** Si la seguridad y la seguridad no son factores, seleccione la respuesta más probable o conveniente.
-   **Cuando sea práctico, haga que la primera respuesta sea la opción predeterminada,** ya que los usuarios lo esperan a menudo a menos que ese pedido no sea lógico.
-   **En el caso de los** cuadros de diálogo, no realice una acción destructiva en el vínculo de comando predeterminado a menos que haya una manera sencilla de deshacer la acción.

## <a name="recommended-sizing-and-spacing"></a>Tamaño y espaciado recomendados

![captura de pantalla del espaciado y el tamaño del vínculo de comandos ](images/ctrl-command-links-image25.png)

## <a name="labels"></a>Etiquetas

> [!Note]  
> Dado que los vínculos de comandos son respuestas a una instrucción principal, debe crear una buena [instrucción principal](text-ui.md) antes de determinar sus respuestas.

 

**Etiquetas de vínculo de comando**

-   **Elija una etiqueta concisa que comunique claramente y diferencie lo que hace el vínculo de comando.** Debe ser autoexplicativo y corresponder a la instrucción principal. Centre las etiquetas en las diferencias entre las respuestas. Los usuarios no deben tener que averiguar qué significa realmente el vínculo de comando ni cómo difiere de otros vínculos de comandos.

    **Incorrecto:**

    ![captura de pantalla de un vínculo de comando redundante ](images/ctrl-command-links-image26.png)

    En este ejemplo, ¿cuál es la diferencia entre la segunda y la tercera respuesta? ¿No le complace que haya un botón Cancelar?

-   **Céntrate en las etiquetas de vínculo de comandos para ayudar a los usuarios a tomar la decisión correcta.** Omita los detalles que no afectan a la elección. Las etiquetas no tienen que ser una especificación completa de lo que ocurrirá.
-   **Inicie vínculos de comando con un verbo.** Sin embargo, no use click, porque la etiqueta debe comunicar lo que hace el vínculo de comando, no cómo funciona.
    -   **Excepción:** Si todos los vínculos de comando comienzan con el mismo verbo o frase, elimine el verbo o frase redundantes.
-   En general, **use expresiones positivas** (proporcionando una opción para hacer algo). Las expresiones negativas (que proporcionan una opción para no hacer algo) son aceptables si facilitan la lectura de las etiquetas.
-   **Use expresiones paralelas y etiquetas de una sola línea.** Las etiquetas largas desaconsejan la lectura y no deben ser necesarias. Además, las etiquetas de tamaño moderado son más fáciles de consultar en la documentación.
-   **Use mayúsculas de estilo de frase.**
-   **No use la puntuación final a menos que la etiqueta sea una pregunta.**
-   **Asigne una clave de acceso única.** Para obtener instrucciones, vea [Teclado.](inter-keyboard.md)
-   **No use puntos suspensivos.** Los puntos suspensivos significan que se puede necesitar más información para realizar la acción. Los vínculos de comandos usados correctamente no necesitan puntos suspensivos porque tienen un efecto inmediato.
-   **Si se recomienda encarecidamente una respuesta, agregue "(recommended)" a la etiqueta.** Asegúrese de agregar a la etiqueta, no a la explicación complementaria.
-   **Si una respuesta está pensada solo para usuarios avanzados, considere la posibilidad de agregar "(advanced)" a la etiqueta.** Asegúrese de agregar a la etiqueta, no a la explicación complementaria.

**Sugerencia:** Para evaluar los vínculos de comandos, debe indicar que un amigo ha indicado la instrucción principal y ha respondido con los vínculos de comando. Si responder con los vínculos de comando sería poco natural o extraño, revise los vínculos de comando y posiblemente la instrucción principal.

**Explicaciones complementarias**

-   Si un vínculo de comando requiere una explicación adicional, **proporcione una explicación complementaria.** Las explicaciones complementarias describen por qué es posible que los usuarios quieran elegir una respuesta o qué ocurre si se elige una respuesta.

    ![captura de pantalla del texto que describe los resultados de la opción ](images/ctrl-command-links-image27.png)

    En este ejemplo, la explicación complementaria describe las implicaciones de la opción.

-   **No use una explicación complementaria que sea una nueva declaración de palabras del vínculo de comando.** Use una explicación complementaria solo cuando no pueda hacer que un vínculo de comando se explique por sí mismo. Proporcionar una explicación complementaria para un vínculo de comando no significa que tenga que proporcionarlos para todos.
-   **Céntrate en las explicaciones complementarias para ayudar a los usuarios a tomar la decisión correcta.** Omita los detalles que no afectan a la elección. Las explicaciones complementarias no tienen que ser una especificación completa de lo que ocurrirá.
-   **Use expresiones paralelas y, como máximo, tres líneas de texto.** Las explicaciones complementarias largas desaconsejan la lectura y no deben ser necesarias.
-   **Use oraciones completas y signos de puntuación finales.**

**Etiquetas de grupo de vínculos de comandos**

-   **No use etiquetas de grupo.** Las instrucciones principales actúan como etiqueta de grupo para los vínculos de comandos.

## <a name="documentation&quot;></a>Documentación

Al hacer referencia a vínculos de comandos:

-   Use el texto exacto de la etiqueta, incluida su mayúscula, pero no incluya el carácter de subrayado de la clave de acceso.
-   Si la etiqueta incluye un nombre de objeto, omita el nombre del objeto o use texto de marcador de posición.
-   Para describir la interacción del usuario, use click.
-   Cuando sea posible, formatee la etiqueta con texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.

**Ejemplos:** Para copiar la imagen, haga clic **en Copiar y reemplazar.**

Haga clic **en Restablecer el adaptador de red.** (Para un vínculo de comando con la etiqueta &quot;Restablecer el nombre del adaptador *de red").*

 

