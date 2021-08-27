---
title: Mensajes de advertencia
description: Un mensaje de advertencia es un cuadro de diálogo modal, un mensaje local, una notificación o un globo que alerta al usuario de una condición que podría causar un problema en el futuro.
ms.assetid: 4a2c3be9-9dc6-4d62-bd3d-72a2e5b621f4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 944c99b546df5fd313ee5bd656db58fafe991d01
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470292"
---
# <a name="warning-messages"></a>Mensajes de advertencia

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Un mensaje de advertencia es un cuadro de diálogo modal, un mensaje local, una notificación o un globo que alerta al usuario de una condición que podría causar un problema en el futuro.

![captura de pantalla de un mensaje de advertencia típico](images/mess-warn-image1.png)

Mensaje de advertencia modal típico.

La característica fundamental de las advertencias es que implican el riesgo de perder uno o varios de los siguientes elementos:

-   Un recurso valioso, como información financiera importante u otros datos.
-   Integridad o acceso del sistema.
-   Privacidad o control sobre la información confidencial.
-   Tiempo del usuario (una cantidad significativa, como 30 segundos o más).

Por el contrario, una confirmación es un cuadro de diálogo modal que pregunta si el usuario desea continuar con una acción. Algunos tipos de advertencias se presentan como confirmaciones y, si es así, también se aplican las directrices de confirmación.

**Nota:** Las instrucciones relacionadas con cuadros [de diálogo,](win-dialog-box.md) [confirmaciones,](mess-confirm.md) [mensajes de error](mess-error.md)iconos estándar, notificaciones y [diseño](vis-layout.md) se presentan en artículos independientes.[](vis-std-icons.md) [](mess-notif.md)

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

Para decidirte, intenta responder a estas preguntas:

-   **¿Se está alertando al usuario de una condición que podría causar un problema en el futuro?** Si no es así, el mensaje no es una advertencia.
-   **¿La interfaz de usuario presenta un error o un problema que ya se ha producido?** Si es así, use un mensaje de error en su lugar.
-   **¿Es probable que los usuarios realicen una acción o cambien su comportamiento como resultado del mensaje?** Si no es así, la condición no justifica la interrupción del usuario, por lo que es mejor suprimir la advertencia.
-   **¿Es la condición el resultado directo de una acción iniciada por el usuario?** Si no es así, considere la posibilidad de [usar notificaciones de eventos no críticos](mess-notif.md).
-   **¿La condición es una condición especial en un control?** Si es así, use un [globo en su](ctrl-balloons.md) lugar.
-   **Para las confirmaciones, ¿el usuario está a punto de realizar una acción de riesgo?** Si es así, es adecuada una advertencia si la acción tiene consecuencias significativas o no se puede deshacer fácilmente.
-   **Para otros tipos de advertencias, ¿el usuario debe actuar ahora o en el futuro inmediato?** No muestre advertencias si los usuarios pueden seguir trabajando de forma productiva sin problemas inmediatos. Posponga la advertencia hasta que la condición sea más inmediata y pertinente.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="avoid-overwarning"></a>Evitar la sobreajuste

Se ha sobreajustado en los programas Windows Microsoft. El programa Windows programa tiene advertencias aparentemente en todas partes, advertencias sobre cosas que tienen poca importancia. En algunos programas, casi todas las preguntas se presentan como una advertencia. La sobreajuste hace que el uso de un programa se sienta como una actividad peligrosa y resta importancia a los problemas realmente importantes.

**Incorrecto:**

![captura de pantalla de un mensaje de advertencia innecesario ](images/mess-warn-image2.png)

La sobreajuste hace que el programa se sienta peligroso y parezca que lo diseñó el abogado.

La simple posibilidad de pérdida de datos o un problema futuro por sí solo no es suficiente para llamar a una advertencia. Además, los resultados no deseados deben ser inesperados o no deseados y no corregirse fácilmente. De lo contrario, casi cualquier error del usuario podría interpretarse para provocar la pérdida de datos o un posible problema de algún tipo y provocar una advertencia.

### <a name="characteristics-of-good-warnings"></a>Características de las advertencias buenas

Advertencias buenas:

-   **Implicar riesgo.** Las advertencias buenas alertan a los usuarios de algo significativo.

**Incorrecto:**

![captura de pantalla de "do you want to exit?" (¿Quiere salir?) warning ](images/mess-warn-image3.png)

¿Y qué? Esta confirmación supone que los usuarios suelen salir de programas por accidente.

-   **Tener relevancia inmediata.** No solo los usuarios tienen que tener cuidado, sino que ahora tienen que ocuparse de ellos. Normalmente, los usuarios no están interesados en los problemas que puedan tener más adelante, siempre y cuando puedan realizar su trabajo ahora.

**Incorrecto:**

![captura de pantalla de la advertencia de batería baja en tres horas ](images/mess-warn-image4.png)

En este caso, es mejor advertir al usuario en tres horas.

-   **Conduce a la acción.** Hay algo que los usuarios deben hacer o tener en cuenta como resultado de la advertencia. Quizás deba realizar una acción ahora o en algún momento en el futuro inmediato. Tal vez realicen una tarea de forma diferente como resultado. La consecuencia de omitir la advertencia debe ser clara. Las advertencias sin acciones simplemente hacen que los usuarios se sientan paranoicos.

**Incorrecto:**

![Captura de pantalla de la advertencia "Live Messenger se está ejecutando" ](images/mess-warn-image5.png)

¿Por qué esta notificación es una advertencia? ¿Qué deben hacer los usuarios (además de preocuparse)?

-   **No son obvias.** No muestre una advertencia para mostrar la consecuencia obvia de una acción. Por ejemplo, suponga que los usuarios comprenden las consecuencias de no completar una tarea.

**Incorrecto:**

![captura de pantalla de ¿desea salir del asistente? Advertencia ](images/mess-warn-image6.png)

Cancelar un asistente incompleto significa que la tarea no se realiza... ¿quién lo sabía?

-   **Se produce con poca frecuencia.** Las advertencias constantes se vuelven ineficaces e insoportables. A menudo, los usuarios se centran más en deshacerse de la advertencia que en solucionar el problema.

**Incorrecto:**

![Captura de pantalla de la advertencia "Actualizar firmas de virus" ](images/mess-warn-image7.png)

Es más probable que los usuarios se centren en deshacerse de la advertencia que en corregir el problema subyacente.

Un mensaje que no tenga estas características podría seguir siendo un buen mensaje, simplemente no una buena advertencia.

### <a name="determine-the-appropriate-message-type"></a>Determinar el tipo de mensaje adecuado

Algunos problemas se pueden presentar como un error, una advertencia o información, dependiendo del énfasis y la expresión. Por ejemplo, suponga que una página web no puede cargar un control ActiveX sin signo en función de la configuración Windows Internet Explorer actual:

-   **Error.** "Esta página no puede cargar un control ActiveX sin signo". (Se describe como un problema existente).
-   **Advertencia.** "Es posible que esta página no se comporte según lo previsto porque Windows Internet Explorer no está configurado para cargar controles de ActiveX sin signo". o "¿Permitir que esta página instale un control de ActiveX sin signo? Si lo hace desde orígenes que no son de confianza, puede dañar el equipo". (Ambos con frases como condiciones que pueden causar problemas futuros).
-   **Información.** "Ha configurado Windows Internet Explorer para bloquear controles de ActiveX sin signo". (Con frases como una declaración de hechos).

**Para determinar el tipo de mensaje adecuado, céntrate en el aspecto más importante del problema que los usuarios necesitan conocer o actuar.** Normalmente, si un problema impide que el usuario se ejecute, debe presentarlo como un error. si el usuario puede continuar, presentá como una advertencia. Crear la [instrucción principal u](text-ui.md) otro texto correspondiente en función de ese foco y, a continuación, elija un icono (estándar o de otro tipo) que coincida con el texto.[](vis-std-icons.md) El texto de instrucción principal y los iconos siempre deben coincidir.

### <a name="be-specific"></a>Ser específico

Las advertencias son más atractivas cuando la siguiente información es específica y clara:

-   Origen de la advertencia.
-   Condición específica y posible problema.
-   Qué debe hacer el usuario al respecto.
-   ¿Qué ocurre si el usuario no hace nada?

**Incorrecto:**

![captura de pantalla de advertencia imprecisa de riesgo significativo ](images/mess-warn-image8.png)

En este ejemplo, ¿cuál es el posible problema? ¿Qué debe hacer el usuario, además de no usar el proyector a través de la red? Sin información más específica, todo lo que el usuario puede hacer es sentirse mal al continuar.

**Correcto:**

![captura de pantalla de advertencia de problemas y consecuencias ](images/mess-warn-image9.png)

En este ejemplo, el problema y las consecuencias son claros.

A veces hay un posible problema legítimo que merece la pena informar a los usuarios, pero la solución y las consecuencias no se conocen con seguridad. En lugar de dar una advertencia imprecisa, sea específico al proporcionar la información más probable o el ejemplo más común.

**Correcto:**

![captura de pantalla de la advertencia de error de red y soluciones ](images/mess-warn-image10.png)

En este ejemplo, la advertencia se hace específica proporcionando la solución más probable.

Sin embargo, en estos casos, use una redacción que indique que hay otras posibilidades. De lo contrario, los usuarios podrían estar enredados.

**Incorrecto:**

![Captura de pantalla de la advertencia de cable de red desconectado ](images/mess-warn-image11.png)

**Correcto:**

![Captura de pantalla del cable podría estar desconectada advertencia ](images/mess-warn-image12.png)

En el ejemplo incorrecto, los usuarios se confundirán si el cable está claramente conectado.

**Si solo hace dos cosas...**

1. No se sobreajuste. Limite las advertencias a condiciones que impliquen riesgos y que sean inmediatamente pertinentes, que puedan actuar, que no sean obvias y poco frecuentes. De lo contrario, quite o retrase el mensaje.

2. Proporcione información específica y útil.

## <a name="usage-patterns"></a>Patrones de uso

Las advertencias tienen varios patrones de uso:




| | | <strong>Reconocimiento</strong><br /> Haga que el usuario tenga en cuenta una condición o un posible problema, pero es posible que el usuario no tenga que hacer nada ahora. <br /> | <img src="images/mess-warn-image13.png" alt="Screen shot of warning of network problems " /><br /><img src="images/mess-warn-image14.png" alt="Screen shot of low-battery warning " /><br /><img src="images/mess-warn-image15.png" alt="Screen shot of 'caps-lock-is-on' warning " /><br /><img src="images/mess-warn-image16.png" alt="Screen shot of 'TPM-not-found' warning " /><br /> Ejemplos de advertencias de reconocimiento.<br /> Las advertencias de reconocimiento tienen la siguiente presentación: <br /><ul><li><strong>Instrucción principal:</strong> Describa la condición o el posible problema.</li><li><strong>Instrucción complementaria:</strong> Explicar la implicación y por qué es importante.</li><li><strong>Botones de confirmación:</strong> Cerca.</li></ul> | | <strong>Prevención de errores</strong><br /> Haga que el usuario tenga en cuenta la información que podría evitar un problema, especialmente al tomar decisiones. <br /> | Las advertencias de prevención de errores se presentan mejor con un icono de advertencia en su lugar y un texto explicativo. <br /><img src="images/mess-warn-image17.png" alt="Screen shot of Not-enough-free-space warning " /><br /><img src="images/mess-warn-image18.png" alt="Screen shot of Use-installation-CD warning " /><br /> Ejemplos de advertencias de prevención de errores.<br /> | | <strong>Problema inminente</strong><br /> El usuario debe hacer algo ahora para evitar un problema inminente. <br /> | <img src="images/mess-warn-image19.png" alt="Screen shot of Close-programs warning " /><br /> Un ejemplo de una advertencia de problema inminente.<br /> Las advertencias de problemas inminentes tienen la siguiente presentación: <br /><ul><li><strong>Instrucción principal:</strong> Describa lo que el usuario necesita hacer ahora.</li><li><strong>Instrucción complementaria:</strong> Explicar la condición y por qué es importante.</li><li><strong>Botones de confirmación:</strong> Un botón de comando o un vínculo de comando para cada opción, o Bien si la acción se produce fuera del cuadro de diálogo.</li></ul> | | <strong>Confirmación de acción de riesgo</strong><br /> Confirme que el usuario desea continuar con una acción que tiene algún riesgo y que no se puede deshacer fácilmente. <br /> | <img src="images/mess-warn-image20.png" alt="Screen shot of Formatting-will-erase-data warning " /><br /> Un ejemplo de confirmación de acción de riesgo.<br /> Las confirmaciones de acción de riesgo tienen la siguiente presentación: <br /><ul><li><strong>Instrucción principal:</strong> Haga una pregunta para determinar si el usuario desea continuar.</li><li><strong>Instrucción complementaria:</strong> Explique los motivos no obvios por los que el usuario podría no querer continuar.</li><li><strong>Botones de confirmación:</strong> Sí, No.</li></ul>Para obtener instrucciones sobre este patrón, vea <a href="mess-confirm.md">Confirmaciones</a>. <br /> | 




 

## <a name="guidelines"></a>Directrices

### <a name="presentation"></a>Presentación

-   **Elija la interfaz de usuario de presentación en función del tipo de información:**



| Interfaz de usuario  | Se usa mejor para |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Cuadros de diálogo modales<br/> | Advertencias críticas (incluidas las confirmaciones) a las que los usuarios deben responder ahora.<br/>                                                 |
| In situ<br/>           | Información que podría evitar un problema, especialmente cuando los usuarios están tomando decisiones.<br/>                                         |
| Banners<br/>            | Información que podría evitar un problema, especialmente cuando se relaciona con la realización de una tarea.<br/>                                     |
| Notificaciones<br/>      | Eventos significativos o estado que se pueden omitir de forma segura, al menos temporalmente.<br/>                                              |
| Globos<br/>           | Un control está en un estado que afecta a la entrada. Es probable que este estado no sea intencionado y que el usuario no se dé cuenta de que la entrada se ve afectada.<br/> |



 

-   **Para los cuadros de diálogo modales:**
    -   **Use los diálogos de tareas siempre que sea necesario para lograr una apariencia y un diseño coherentes.** Los diálogos de tareas Windows Vista o versiones posteriores, por lo que no son adecuados para versiones anteriores de Windows.
    -   **Mostrar solo un mensaje de advertencia por condición.** Por ejemplo, muestre una sola advertencia que explique completamente una condición en lugar de describirla de un detalle a la vez por mensaje. Mostrar una secuencia de diálogos de advertencia para una sola condición es confuso y confuso.
    -   **No muestre una advertencia más de una vez por condición.** Las advertencias constantes se vuelven ineficaces e insoportables. A menudo, los usuarios se centran más en deshacerse de la advertencia que en solucionar el problema. Si debe advertir repetidamente de una sola condición, use [la escalación progresiva](mess-notif.md).
-   **No acompañe las advertencias con un efecto de sonido o un pitido.** Hacerlo es jarring e innecesario.
    -   **Excepción:** Si el usuario debe responder inmediatamente, puede usar un efecto de sonido.

### <a name="icons"></a>Iconos

-   No coloque un icono de advertencia en la barra de título de un cuadro de diálogo.
-   **Use un icono de advertencia.** Excepciones:
    -   Si la advertencia es para una característica que tiene un icono, puede usar el icono de característica con una superposición de advertencia.

        **Correcto:**

        ![captura de pantalla del icono de bloqueo con superposición de icono de advertencia ](images/mess-warn-image21.png)

        En este ejemplo, el icono de característica tiene una superposición de advertencia.

-   Para los cuadros de diálogo modales con una nota al pie de advertencia, coloque el icono de advertencia en la nota al pie en lugar del área de contenido.

    **Correcto:**

    ![captura de pantalla del icono de advertencia en la nota al pie del cuadro de diálogo ](images/mess-warn-image22.png)

    En este ejemplo, la nota al pie tiene el icono de advertencia.

Para obtener más instrucciones y ejemplos, vea [Iconos estándar.](vis-std-icons.md)

### <a name="dont-show-this-message-again"></a>No volver a mostrar este mensaje

-   **Si un cuadro de diálogo de advertencia necesita esta opción, replantee la advertencia y su frecuencia.** Si tiene todas las características de una buena advertencia (implica riesgo y es inmediatamente relevante, práctica, no obvia y poco frecuente), no debería tener sentido que los usuarios la suprima.

Para obtener más instrucciones, vea [Cuadros de diálogo](win-dialog-box.md).

### <a name="progressive-disclosure"></a>Muestra progresiva

-   **Si debe incluir información avanzada en un mensaje** de advertencia, puede mostrarla mediante botones de divulgación progresiva (por ejemplo, "Mostrar detalles"). Si lo hace, se simplifica la advertencia para el uso típico. No oculte la información necesaria porque es posible que los usuarios no la encuentren.
-   **No use "Mostrar detalles" a menos que realmente haya más detalles.** No solo vuelva a establecer la información existente en un formato diferente.

Para obtener instrucciones de etiquetado, vea [Divulgación progresiva.](ctrl-progressive-disclosure-controls.md)

### <a name="default-values"></a>Valores predeterminados

-   **Seleccione la respuesta más segura, menos destructiva o más segura para que sea la predeterminada.**

## <a name="text"></a>Texto

### <a name="general"></a>General

-   **Quite el texto redundante.** Buscarlo en títulos, instrucciones principales, instrucciones complementarias, áreas de contenido, vínculos de comandos y botones de confirmación. Por lo general, deje texto completo en instrucciones y controles interactivos y quite cualquier redundancia de los demás lugares.
-   **No use los términos "advertencia" o "precaución" en el texto.** Cuando [se usa correctamente,](vis-std-icons.md)el icono de advertencia comunica lo suficiente que los usuarios deben continuar con precaución.

**Incorrecto:**

![captura de pantalla del uso innecesario de advertencia en el texto ](images/mess-warn-image23.png)

En este ejemplo, el término "advertencia" no es necesario.

### <a name="titles"></a>Títulos

-   **Use el título para identificar el comando o la característica de donde provenía la advertencia.** Excepciones:
    -   Si muchos comandos diferentes muestran una advertencia, considere la posibilidad de usar el nombre del programa en su lugar.
    -   Si ese título sería redundante o confuso con la instrucción principal, use el nombre del programa en su lugar.

**Incorrecto:**

![captura de pantalla del título del cuadro de diálogo advertencia de seguridad ](images/mess-warn-image24.png)

En este ejemplo, "Advertencia de seguridad" no identifica el comando o la característica de donde provenía la advertencia.

-   **No use el título para explicar qué** hacer en el cuadro de diálogo que es el propósito de la instrucción principal.
-   Use [el uso de mayúsculas de estilo de](glossary.md)título, sin terminar los signos de puntuación.

### <a name="main-instructions"></a>Instrucciones principales

-   La instrucción principal de una advertencia se basa en su patrón de diseño:



| Patrón                        | Instrucción principal                                               |
|--------------------------------------|----------------------------------------------------------------------|
| Concienciación<br/>                 | Describa la condición o el posible problema.<br/>              |
| Problema inminente<br/>          | Describa lo que el usuario necesita hacer ahora.<br/>                   |
| Confirmación de acción de riesgo<br/> | Haga una pregunta para determinar si el usuario desea continuar.<br/> |



 

-   ![captura de pantalla de una notificación de batería baja ](images/mess-warn-image25.png)
-   En este ejemplo, la notificación de batería baja es una advertencia de reconocimiento, por lo que la instrucción principal describe la condición.
-   ![Captura de pantalla de la advertencia de cambiar la batería inmediatamente ](images/mess-warn-image1.png)
-   En este ejemplo, el cuadro de diálogo de batería baja es un problema inminente, por lo que la instrucción principal describe lo que el usuario necesita hacer ahora.
-   **Sea conciso y use solo una sola oración completa.** Quitar la instrucción principal hasta la información esencial. Si tiene que explicar algo más, use una instrucción complementaria.
-   **Use palabras como "now" e "immediately" si el usuario debe actuar inmediatamente.** No use estas palabras si no hay ninguna urgencia.
-   **Sea específico si hay objetos implicados, así como sus nombres completos.**
-   Use [mayúsculas de estilo oración.](glossary.md)

### <a name="supplemental-instructions"></a>Instrucciones complementarias

-   La instrucción complementaria de una advertencia se basa en su patrón de diseño:



| Patrón            | Instrucción complementaria                                            |
|--------------------------------------|------------------------------------------------------------------------------------|
| Concienciación<br/>                 | Explicar la implicación y por qué es importante.<br/>                        |
| Problema inminente<br/>          | Explicar la condición y por qué es importante.<br/>                          |
| Confirmación de acción de riesgo<br/> | Explique los motivos no obvios por los que el usuario podría no querer continuar.<br/> |



 

-   **No repita la instrucción principal con una redacción ligeramente diferente.** En su lugar, omita la instrucción complementaria si no hay más que agregar.
-   Use oraciones completas, mayúsculas de estilo oración y signos de puntuación finales.

### <a name="commit-buttons"></a>Botones de confirmación

-   Para los cuadros de diálogo de advertencia, los botones de confirmación se basan en su patrón de diseño:



| Patrón               | Botones de confirmación        |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Concienciación<br/>                 | Casi. No use Aceptar porque sugiere que los posibles problemas son correctos.<br/>                              |
| Problema inminente<br/>          | Un botón de comando o un vínculo de comando para cada opción, o Bien si la acción se produce fuera del cuadro de diálogo.<br/> |
| Confirmación de acción de riesgo<br/> | Sí, No.<br/>                                                                                             |



 

-   **Incorrecto:**
-   ![captura de pantalla del cuadro de diálogo de advertencia con el botón Aceptar ](images/mess-warn-image26.png)
-   Los problemas no son correctos, así que use Cerrar en su lugar.

## <a name="documentation"></a>Documentación

Al hacer referencia a advertencias:

-   Si la advertencia hace una pregunta, consulte una advertencia por su pregunta. De lo contrario, use la instrucción principal. Si la pregunta o la instrucción principal son largas o detalladas, resuma.
-   Si es necesario, puede hacer referencia a un cuadro de diálogo de advertencia como un mensaje.
-   Cuando sea posible, formatee el texto con negrita. De lo contrario, coloque el texto entre comillas solo si es necesario para evitar confusiones.

Ejemplo: en el mensaje ¿Desea mostrar los elementos no **seguros?,** haga clic en Sí.

 

