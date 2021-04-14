---
title: Mensajes de advertencia
description: Un mensaje de advertencia es un cuadro de diálogo modal, un mensaje en contexto, una notificación o un globo que alerta al usuario de una condición que puede provocar un problema en el futuro.
ms.assetid: 4a2c3be9-9dc6-4d62-bd3d-72a2e5b621f4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: d704890b2471e205b933e2995950716c269488e8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104361816"
---
# <a name="warning-messages"></a>Mensajes de advertencia

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Un mensaje de advertencia es un cuadro de diálogo modal, un mensaje en contexto, una notificación o un globo que alerta al usuario de una condición que puede provocar un problema en el futuro.

![captura de pantalla de un mensaje de advertencia típico](images/mess-warn-image1.png)

Un mensaje de advertencia modal típico.

La característica fundamental de las advertencias es que implican el riesgo de perder una o varias de las siguientes acciones:

-   Un activo valioso, como información financiera importante u otros datos.
-   Acceso al sistema o integridad.
-   Privacidad o control sobre la información confidencial.
-   Hora del usuario (una cantidad significativa, como 30 segundos o más).

Por el contrario, una confirmación es un cuadro de diálogo modal que pregunta si el usuario desea continuar con una acción. Algunos tipos de advertencias se presentan como confirmaciones y, si es así, también se aplican las directrices de confirmación.

**Nota:** Las instrucciones relacionadas con los [cuadros de diálogo](win-dialog-box.md), las [confirmaciones](mess-confirm.md), los [iconos estándar](vis-std-icons.md)de [los mensajes de error](mess-error.md), las [notificaciones](mess-notif.md)y el [diseño](vis-layout.md) se presentan en artículos independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

Para decidirte, intenta responder a estas preguntas:

-   **¿El usuario recibe una alerta de una condición que puede provocar un problema en el futuro?** Si no es así, el mensaje no es una advertencia.
-   **¿La interfaz de usuario presenta un error o un problema que ya se ha producido?** Si es así, use un mensaje de error en su lugar.
-   **¿Es probable que los usuarios realicen una acción o cambien su comportamiento como resultado del mensaje?** En caso contrario, la condición no justifica interrumpir al usuario, por lo que es mejor suprimir la advertencia.
-   **¿Es la condición el resultado directo de una acción iniciada por el usuario?** Si no es así, considere la posibilidad de usar [notificaciones de eventos no críticas](mess-notif.md).
-   **¿Es la condición una condición especial en un control?** Si es así, use un [globo](ctrl-balloons.md) en su lugar.
-   **En el caso de las confirmaciones, ¿el usuario está a punto de realizar una acción de riesgo?** Si es así, una advertencia es adecuada si la acción tiene consecuencias importantes o no se puede deshacer fácilmente.
-   **Para otros tipos de advertencias, ¿el usuario tiene que actuar ahora o en el futuro inmediato?** No muestre advertencias si los usuarios pueden seguir trabajando de manera productiva sin problemas inmediatos. Posponer la advertencia hasta que la condición sea más inmediata y relevante.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="avoid-overwarning"></a>Evitar las sobreadvertencias

Se recomienda que se avise en los programas de Microsoft Windows. El programa típico de Windows tiene advertencias aparentemente en todas partes, advertencia sobre cosas que tienen poca importancia. En algunos programas, casi todas las preguntas se presentan como una advertencia. La sobreadvertencia hace que el uso de un programa se parezca a una actividad peligrosa y se reste de problemas realmente significativos.

**Incorrecto:**

![captura de pantalla de un mensaje de advertencia innecesario ](images/mess-warn-image2.png)

La sobreadvertencia hace que el programa se sienta peligroso y parezca que lo diseñó un abogados.

La mera posibilidad de pérdida de datos o un problema futuro por sí solo es insuficiente para llamar a una advertencia. Además, los resultados no deseados deberían ser inesperados o no deseados, y no se pueden corregir fácilmente. De lo contrario, cualquier error de usuario podría interpretarse para producir la pérdida de datos o un posible problema de algún tipo y merecen una advertencia.

### <a name="characteristics-of-good-warnings"></a>Características de las buenas advertencias

Buenas advertencias:

-   **Implicar riesgo.** Las advertencias correctas alertan a los usuarios de algo importante.

**Incorrecto:**

![captura de pantalla de "¿desea salir?" warning ](images/mess-warn-image3.png)

¿Y qué? Esta confirmación supone que los usuarios suelen salir de los programas por accidente.

-   **Tienen relevancia inmediata.** No solo los usuarios tienen que preocuparse, ya que tienen que preocuparse. Normalmente, los usuarios no están interesados en los problemas que puedan tener más adelante, siempre y cuando puedan hacer su trabajo ahora.

**Incorrecto:**

![captura de pantalla de una advertencia de batería baja en tres horas ](images/mess-warn-image4.png)

En este caso, es mejor avisar al usuario en tres horas.

-   **Conducen a la acción.** Hay algo que los usuarios deben hacer o tener en cuenta como resultado de la advertencia. Quizás deban realizar una acción ahora o en algún momento en el futuro. Quizás realizarán una tarea de manera diferente como resultado. La consecuencia de omitir la advertencia debe ser clara. Las advertencias sin acciones solo hacen que los usuarios sientan Paranoid.

**Incorrecto:**

![captura de pantalla de la advertencia "Live Messenger está en ejecución" ](images/mess-warn-image5.png)

¿Por qué esta notificación es una advertencia? ¿Qué se supone que deben hacer los usuarios (junto a preocuparse)?

-   **No son obvios.** No muestre una advertencia para indicar la consecuencia obvia de una acción. Por ejemplo, supongamos que los usuarios entienden las consecuencias de no completar una tarea.

**Incorrecto:**

![captura de pantalla de ¿desea salir del asistente? atención ](images/mess-warn-image6.png)

La cancelación de un asistente incompleto significa que la tarea no se realiza... ¿Quién sabía?

-   **Se producen con poca frecuencia.** Las advertencias constantes pasan a ser ineficaces y molestas. A menudo, los usuarios se centran más en deshacerse de la advertencia que solucionar el problema.

**Incorrecto:**

![captura de pantalla de la advertencia "actualizar firmas de virus" ](images/mess-warn-image7.png)

Es más probable que los usuarios se centren en deshacerse de la advertencia que solucionar el problema subyacente.

Un mensaje que no tenga estas características puede seguir siendo un buen mensaje, no una buena advertencia.

### <a name="determine-the-appropriate-message-type"></a>Determinar el tipo de mensaje adecuado

Algunos problemas se pueden presentar como un error, una advertencia o información, según el énfasis y la formulación. Por ejemplo, supongamos que una página web no puede cargar un control ActiveX sin firmar basado en la configuración actual de Windows Internet Explorer:

-   **Error.** "Esta página no puede cargar un control ActiveX sin firmar". (Frase como un problema existente).
-   **Atención.** "Es posible que esta página no se comporte de la manera esperada porque Windows Internet Explorer no está configurado para cargar controles ActiveX sin firmar". o "¿desea permitir que esta página Instale un control ActiveX sin firmar? Hacerlo desde orígenes que no son de confianza puede dañar el equipo ". (Ambas frases como condiciones que pueden causar problemas en el futuro).
-   **Informaciones.** "Ha configurado Windows Internet Explorer para bloquear los controles ActiveX sin firmar". (Frase como instrucción de hecho).

**Para determinar el tipo de mensaje adecuado, céntrese en el aspecto más importante del problema que los usuarios necesitan conocer o actuar sobre ellos.** Normalmente, si un problema impide que el usuario continúe, debe presentarlo como un error. Si el usuario puede continuar, preséntela como advertencia. Cree la [instrucción principal](text-ui.md) u otro texto correspondiente en función de ese foco y, a continuación, elija un icono ([estándar](vis-std-icons.md) o de otro tipo) que coincida con el texto. Los iconos y el texto de la instrucción principal siempre deben coincidir.

### <a name="be-specific"></a>Ser específico

Las advertencias son más atractivas cuando la siguiente información es específica y clara:

-   Origen de la advertencia.
-   La condición específica y el posible problema.
-   Lo que el usuario debe hacer sobre él.
-   Lo que sucede si el usuario no hace nada.

**Incorrecto:**

![captura de pantalla de advertencia imprecisa de riesgo significativo ](images/mess-warn-image8.png)

En este ejemplo, ¿cuál es el posible problema? ¿Qué debe hacer el usuario, aparte de no usar el proyector a través de la red? Sin información más específica, todo lo que puede hacer el usuario es un inconveniente de continuar.

**Correcto:**

![captura de pantalla de la advertencia del problema y las consecuencias ](images/mess-warn-image9.png)

En este ejemplo, el problema y las consecuencias son claros.

A veces hay un problema potencial legítimo que merece la información a los usuarios, pero la solución y las consecuencias no se conocen por seguridad. En lugar de proporcionar una advertencia imprecisa, sea específico proporcionando la información más probable o el ejemplo más común.

**Correcto:**

![captura de pantalla de la advertencia y las soluciones de error de red ](images/mess-warn-image10.png)

En este ejemplo, la advertencia se realiza de forma específica proporcionando la solución más probable.

Sin embargo, en estos casos, use el texto que indica que hay otras posibilidades. De lo contrario, los usuarios podrían ser inducidos.

**Incorrecto:**

![captura de pantalla de advertencia de cable de red desconectado ](images/mess-warn-image11.png)

**Correcto:**

![la captura de pantalla de cable podría estar desconectada ](images/mess-warn-image12.png)

En el ejemplo incorrecto, se confundirá a los usuarios si el cable está claramente enchufado.

**Si solo hace dos cosas...**

1. No lo advierta. Limite las advertencias a condiciones que impliquen un riesgo y que sean pertinentes, procesables, no obvios e infrecuentes. De lo contrario, quite o vuelva a formular el mensaje.

2. Proporcionar información específica y útil.

## <a name="usage-patterns"></a>Patrones de uso

Las advertencias tienen varios patrones de uso:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Reconocimiento</strong>:<br/> Haga que el usuario tenga en cuenta una condición o posible problema, pero es posible que el usuario no tenga que hacer nada ahora. <br/></td>
<td><img src="images/mess-warn-image13.png" alt="Screen shot of warning of network problems " /><br/> <img src="images/mess-warn-image14.png" alt="Screen shot of low-battery warning " /><br/> <img src="images/mess-warn-image15.png" alt="Screen shot of &#39;caps-lock-is-on&#39; warning " /><br/> <img src="images/mess-warn-image16.png" alt="Screen shot of &#39;TPM-not-found&#39; warning " /><br/> Ejemplos de advertencias de reconocimiento.<br/> Las advertencias de reconocimiento tienen la siguiente presentación: <br/>
<ul>
<li><strong>Instrucción principal:</strong> Describir la condición o el posible problema.</li>
<li><strong>Instrucción complementaria:</strong> Explique la implicación y el motivo por el que es importante.</li>
<li><strong>Botones de confirmación:</strong> Cercanos.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Prevención de errores</strong><br/> Haga que el usuario tenga en cuenta la información que puede impedir un problema, especialmente al tomar decisiones. <br/></td>
<td>Las advertencias de prevención de errores se presentan mejor mediante un icono de advertencia en contexto y un texto explicativo. <br/> <img src="images/mess-warn-image17.png" alt="Screen shot of Not-enough-free-space warning " /><br/> <img src="images/mess-warn-image18.png" alt="Screen shot of Use-installation-CD warning " /><br/> Ejemplos de advertencias de prevención de errores.<br/></td>
</tr>
<tr class="odd">
<td><strong>Problema inminente</strong><br/> El usuario debe hacer algo ahora para evitar un problema inminente. <br/></td>
<td><img src="images/mess-warn-image19.png" alt="Screen shot of Close-programs warning " /><br/> Un ejemplo de una advertencia inminente del problema.<br/> Las advertencias de problemas inminentes tienen la siguiente presentación: <br/>
<ul>
<li><strong>Instrucción principal:</strong> Describa lo que el usuario debe hacer ahora.</li>
<li><strong>Instrucción complementaria:</strong> Explique la condición y por qué es importante.</li>
<li><strong>Botones de confirmación:</strong> Un botón de comando o vínculo de comando para cada opción, o bien aceptar si la acción se produce fuera del cuadro de diálogo.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Confirmación de acción de riesgo</strong><br/> Confirme que el usuario desea continuar con una acción que tiene cierto riesgo y no se puede deshacer fácilmente. <br/></td>
<td><img src="images/mess-warn-image20.png" alt="Screen shot of Formatting-will-erase-data warning " /><br/> Ejemplo de confirmación de acción de riesgo.<br/> Las confirmaciones de acción de riesgo tienen la siguiente presentación: <br/>
<ul>
<li><strong>Instrucción principal:</strong> Formule una pregunta para determinar si el usuario desea continuar.</li>
<li><strong>Instrucción complementaria:</strong> Explique las razones no obvias por las que el usuario podría no querer continuar.</li>
<li><strong>Botones de confirmación:</strong> Sí, no.</li>
</ul>
Para obtener instrucciones sobre este patrón, consulte <a href="mess-confirm.md">confirmaciones</a>. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Directrices

### <a name="presentation"></a>Presentación

-   **Elija la interfaz de usuario de presentación según el tipo de información:**



|                               |                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Interfaz de usuario**<br/> | **Mejor uso para**<br/>                                                                                                           |
| Cuadros de diálogo modales<br/> | ADVERTENCIAS críticas (incluidas las confirmaciones) a las que los usuarios deben responder ahora.<br/>                                                 |
| En contexto<br/>           | Información que podría impedir un problema, especialmente cuando los usuarios están realizando elecciones.<br/>                                         |
| Banners<br/>            | Información que puede impedir un problema, especialmente cuando está relacionado con la finalización de una tarea.<br/>                                     |
| Notificaciones<br/>      | Eventos o Estados significativos que se pueden omitir sin ningún riesgo, al menos temporalmente.<br/>                                              |
| Globos<br/>           | Un control está en un estado que afecta a la entrada. Es probable que este estado no sea el deseado y que el usuario no se vea afectado.<br/> |



 

-   **En los cuadros de diálogo modales:**
    -   **Utilice los cuadros de diálogo de tareas siempre que sea necesario para lograr una apariencia y un diseño coherentes.** Los cuadros de diálogo de tareas requieren Windows Vista o posterior, por lo que no son adecuados para versiones anteriores de Windows.
    -   **Muestra solo un mensaje de advertencia por condición.** Por ejemplo, se muestra una advertencia única que explica completamente una condición en lugar de describirla un detalle cada vez por mensaje. Mostrar una secuencia de cuadros de diálogo de advertencia para una única condición es confuso y molesto.
    -   **No mostrar una advertencia más de una vez por condición.** Las advertencias constantes pasan a ser ineficaces y molestas. A menudo, los usuarios se centran más en deshacerse de la advertencia que solucionar el problema. Si debe advertir repetidamente para una única condición, use la [extensión progresiva](mess-notif.md).
-   **No acompañe las advertencias con un efecto o bip sonoros.** Hacerlo es discordante e innecesario.
    -   **Excepción:** Si el usuario debe responder inmediatamente, puede usar un efecto de sonido.

### <a name="icons"></a>Iconos

-   No coloque un icono de advertencia en la barra de título de un cuadro de diálogo.
-   **Use un icono de advertencia.** Excepciones:
    -   Si la advertencia es para una característica que tiene un icono, puede usar el icono de la característica con una superposición de advertencia.

        **Correcto:**

        ![captura de pantalla del icono de candado con la superposición de icono de advertencia ](images/mess-warn-image21.png)

        En este ejemplo, el icono de característica tiene una superposición de advertencia.

-   En el caso de los cuadros de diálogo modales con una nota al pie de la advertencia, coloque el icono de advertencia en la nota al pie en lugar del área de contenido.

    **Correcto:**

    ![captura de pantalla del icono de advertencia en la nota al pie del cuadro de diálogo ](images/mess-warn-image22.png)

    En este ejemplo, la nota al pie tiene el icono de advertencia.

Para obtener más instrucciones y ejemplos, vea [iconos estándar](vis-std-icons.md).

### <a name="dont-show-this-message-again"></a>No volver a mostrar este mensaje

-   **Si un cuadro de diálogo de advertencia necesita esta opción, reconsidere la advertencia y su frecuencia.** Si tiene todas las características de una buena advertencia (implica un riesgo y es inmediatamente pertinente, accionable, no obvia y poco frecuente), no debe tener sentido que los usuarios lo supriman.

Para obtener más instrucciones, consulte [cuadros de diálogo](win-dialog-box.md).

### <a name="progressive-disclosure"></a>Muestra progresiva

-   **Si tiene que incluir información avanzada en un mensaje de advertencia, debe revelarla mediante botones de divulgación progresiva** (por ejemplo, "Mostrar detalles"). De este modo, se simplifica la advertencia para el uso típico. No oculte la información necesaria porque es posible que los usuarios no la encuentren.
-   **No use "Mostrar detalles" a menos que realmente haya más detalles.** No solo tiene que volver a indicar la información existente en un formato diferente.

Para obtener instrucciones de etiquetado, vea [divulgación progresiva](ctrl-progressive-disclosure-controls.md).

### <a name="default-values"></a>Valores predeterminados

-   **Seleccione la respuesta más segura, menos destructiva o más segura como predeterminada.**

## <a name="text"></a>Texto

### <a name="general"></a>General

-   **Quite el texto redundante.** Busque en los títulos, las instrucciones principales, las instrucciones adicionales, las áreas de contenido, los vínculos de comandos y los botones de confirmación. Por lo general, deje texto completo en las instrucciones y los controles interactivos, y quite cualquier redundancia de los demás lugares.
-   **No use los términos "ADVERTENCIA" o "PRECAUCIÓN" en el texto.** Cuando se [usa correctamente](vis-std-icons.md), el icono de advertencia comunica de forma suficiente que los usuarios deben proseguir con precaución.

**Incorrecto:**

![captura de pantalla del uso innecesario de advertencia en el texto ](images/mess-warn-image23.png)

En este ejemplo, el término "WARNING" no es necesario.

### <a name="titles"></a>Títulos

-   **Use el título para identificar el comando o la característica de donde procede la advertencia.** Excepciones:
    -   Si se muestra una advertencia en muchos comandos diferentes, considere la posibilidad de usar el nombre del programa en su lugar.
    -   Si ese título sería redundante o confuso con la instrucción principal, use en su lugar el nombre del programa.

**Incorrecto:**

![captura de pantalla del título del cuadro de diálogo Advertencia de seguridad ](images/mess-warn-image24.png)

En este ejemplo, "ADVERTENCIA de seguridad" no identifica el comando o la característica de la que procede la advertencia.

-   **No use el título para explicar qué hacer en el cuadro de diálogo** que es el propósito de la instrucción principal.
-   Usar [mayúsculas y minúsculas de estilo de título](glossary.md), sin puntuación final.

### <a name="main-instructions"></a>Instrucciones principales

-   La instrucción principal de una advertencia se basa en su modelo de diseño:



|                                      |                                                                      |
|--------------------------------------|----------------------------------------------------------------------|
| **Patrón**<br/>               | **Instrucción principal**<br/>                                      |
| Concienciación<br/>                 | Describir la condición o el posible problema.<br/>              |
| Problema inminente<br/>          | Describa lo que el usuario debe hacer ahora.<br/>                   |
| Confirmación de acción de riesgo<br/> | Formule una pregunta para determinar si el usuario desea continuar.<br/> |



 

-   ![captura de pantalla de una notificación de batería baja ](images/mess-warn-image25.png)
-   En este ejemplo, la notificación de batería baja es una advertencia de reconocimiento, por lo que la instrucción principal describe la condición.
-   ![captura de pantalla de la advertencia de cambio de batería inmediata ](images/mess-warn-image1.png)
-   En este ejemplo, el cuadro de diálogo de batería baja es un problema inminente, por lo que la instrucción principal describe lo que el usuario debe hacer ahora.
-   **Sea conciso usar una sola oración completa.** Quite la instrucción principal de la información esencial. Si debe explicar algo más, use una instrucción complementaria.
-   **Use palabras como "ahora" y "inmediatamente" si el usuario debe actuar inmediatamente.** No use estas palabras si no hay urgencia.
-   **Ser específico si hay objetos implicados, asigne sus nombres completos.**
-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).

### <a name="supplemental-instructions"></a>Instrucciones complementarias

-   La instrucción complementaria para una advertencia se basa en su modelo de diseño:



|                                      |                                                                                    |
|--------------------------------------|------------------------------------------------------------------------------------|
| **Patrón**<br/>               | **Instrucción complementaria**<br/>                                            |
| Concienciación<br/>                 | Explique la implicación y el motivo por el que es importante.<br/>                        |
| Problema inminente<br/>          | Explique la condición y por qué es importante.<br/>                          |
| Confirmación de acción de riesgo<br/> | Explique las razones no obvias por las que el usuario podría no querer continuar.<br/> |



 

-   **No repita la instrucción principal con un texto ligeramente diferente.** En su lugar, omita la instrucción complementaria Si no hay más que agregar.
-   Use frases completas, uso de mayúsculas y minúsculas y puntuación final.

### <a name="commit-buttons"></a>Botones de confirmación

-   En el caso de los cuadros de diálogo de advertencia, los botones de confirmación se basan en su modelo de diseño:



|                                      |                                                                                                                 |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| **Patrón**<br/>               | **Botones de confirmación**<br/>                                                                                   |
| Concienciación<br/>                 | Casi. No use aceptar porque sugiere que los posibles problemas son correctos.<br/>                              |
| Problema inminente<br/>          | Un botón de comando o vínculo de comando para cada opción, o bien aceptar si la acción se produce fuera del cuadro de diálogo.<br/> |
| Confirmación de acción de riesgo<br/> | Sí, no.<br/>                                                                                             |



 

-   **Incorrecto:**
-   ![captura de pantalla del cuadro de diálogo de advertencia con el botón Aceptar ](images/mess-warn-image26.png)
-   Los problemas no son correctos, por lo que debe usar cerrar en su lugar.

## <a name="documentation"></a>Documentación

Al hacer referencia a las advertencias:

-   Si la advertencia formula una pregunta, consulte una advertencia por su pregunta; de lo contrario, use la instrucción principal. Si la pregunta o instrucción principal es larga o detallada, resume.
-   Si es necesario, puede hacer referencia a un cuadro de diálogo de advertencia como mensaje.
-   Siempre que sea posible, dé formato al texto con negrita. De lo contrario, coloque el texto entre comillas solo si es necesario para evitar confusiones.

Ejemplo: en el mensaje **¿desea mostrar los elementos no seguros?** , haga clic en sí.

 

