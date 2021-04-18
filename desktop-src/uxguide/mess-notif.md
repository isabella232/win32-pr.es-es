---
title: Notificaciones (conceptos básicos del diseño)
description: Una notificación informa a los usuarios de eventos que no están relacionados con la actividad del usuario actual, mostrando brevemente un globo de un icono en el área de notificación.
ms.assetid: dcac2fb7-e503-4ea3-a2c5-e3cb660c040a
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 5de312b33a970245d2f6f410e55a891c286d9aa7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104551384"
---
# <a name="notifications-design-basics"></a>Notificaciones (conceptos básicos del diseño)

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Una notificación informa a los usuarios de eventos que no están relacionados con la actividad del usuario actual, mostrando brevemente un globo de un icono en el área de notificación. La notificación podría deberse a una acción del usuario o a un evento del sistema importante, o podría ofrecer información potencialmente útil de Microsoft Windows o una aplicación.

La información de una notificación es **útil y relevante, pero nunca es crítica.** Por lo tanto, las notificaciones no requieren la intervención inmediata del usuario y los usuarios pueden omitirlas libremente.

![captura de pantalla del globo con ' nuevas actualizaciones ' en el título ](images/mess-notif-image1.png)

Una notificación típica.

En Windows Vista y versiones posteriores, se muestran notificaciones para una duración fija de 9 segundos. Las notificaciones no se muestran inmediatamente cuando los usuarios están inactivos o se están ejecutando protectores de pantalla. Windows pone en cola automáticamente las notificaciones durante estas horas y muestra las notificaciones en cola cuando el usuario reanuda la actividad normal. Por lo tanto, no tiene que hacer nada para tratar estas circunstancias especiales.

**Desarrolladores:** Puede determinar si el usuario está activo mediante la API de SHQueryUserNotificationState.

**Nota:** Las instrucciones relacionadas con el [área de notificación](winenv-notification.md), la [barra de tareas](winenv-taskbar.md)y los [globos](ctrl-balloons.md) se presentan en artículos independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

Para decidirte, intenta responder a estas preguntas:

-   **¿La información es el resultado inmediato y directo de la interacción de los usuarios con la aplicación?** Si es así, muestre esta información sincrónica directamente dentro de la aplicación en su lugar mediante un [cuadro de diálogo](win-dialog-box.md), un [cuadro de mensaje](glossary.md), un [globo](ctrl-balloons.md)o la interfaz de usuario [en su lugar](glossary.md) . Las notificaciones son solo para información asincrónica.

![captura de pantalla de alerta de seguridad de Windows ](images/mess-notif-image2.png)

En este ejemplo, el cuadro de diálogo excepciones de Firewall de Windows se muestra como resultado directo de la interacción con el usuario. Una notificación no sería adecuada aquí.

-   **¿La información es relevante solo cuando los usuarios usan activamente la aplicación?** Si es así, muestre la información en la [barra de estado](ctrl-status-bars.md) de la aplicación u otro área de estado.

![captura de pantalla de la barra de estado de Outlook ](images/mess-notif-image3.png)

En este ejemplo, Outlook muestra la conexión y el estado de sincronización en la barra de estado.

-   **¿La información cambia rápidamente, es decir, datos continuos y en tiempo real?** Entre los ejemplos se incluyen progreso de procesamiento, cotizaciones de acciones y puntuaciones deportivas. Si es así, no use las notificaciones porque no son adecuadas para la información que cambia rápidamente.
-   **¿La información es útil y relevante? ¿Es probable que los usuarios cambien su comportamiento o eviten molestias como resultado de la recepción de la información?** Si no es así, no muestre la información o colóquela en una ventana de estado o un archivo de registro.
-   **¿La información es crítica? ¿Es necesaria una acción inmediata?** Si es así, muestre la información mediante una interfaz que requiera atención y no se pueda omitir fácilmente, como un cuadro de diálogo modal o un cuadro de mensaje. Si el programa no está activo, puede atraer la atención a la información crítica si hace [parpadear el botón de la barra de tareas del programa](winenv-taskbar.md) tres veces y lo mantiene resaltado hasta que el programa esté activo.
-   **¿Son los profesionales de TI de los usuarios de destino primarios?** Si es así, use un mecanismo de comentarios alternativo, como entradas de [archivo de registro](glossary.md) o mensajes de correo electrónico. Los profesionales de ti prefieren los archivos de registro de forma segura para obtener información no crítica. Además, los servidores a menudo se administran de forma remota y se ejecutan normalmente sin ningún usuario que haya iniciado sesión, por lo que las notificaciones no surten efecto.

## <a name="design-concepts"></a>Conceptos de diseño

Las notificaciones eficaces que fomentan una buena experiencia del usuario son:

-   **Asincrónica.** El evento no es un resultado inmediato y directo de la interacción actual de los usuarios con Microsoft Windows o con la aplicación.
-   **Son.** Existe una posibilidad razonable de que los usuarios realicen una tarea o cambien su comportamiento como resultado de la notificación.
-   **Apropiadas.** La notificación muestra información útil que los usuarios le interesan y que todavía no saben.
-   **No es crítico.** Las notificaciones no son modales y no requieren la interacción del usuario, por lo que los usuarios pueden omitirlas libremente.
-   **Accionable.** En el caso de las notificaciones que sugieren realizar una acción, esta acción se inicia al hacer clic en la notificación. Sin embargo, siempre se puede posponer la acción.
-   **Presentada correctamente.** La presentación de la notificación (duración, frecuencia, texto, icono e interactividad) coincide con sus circunstancias.
-   **¡ No molesta!** Hay una línea fina entre informar suavemente a los usuarios de un evento y Pestering.

Desafortunadamente, hay demasiadas notificaciones molestas, inadecuadas e inadecuadas. Tenga en cuenta estas notificaciones de Windows XP Hall of Shame:

![captura de pantalla de la notificación "Touring Windows XP" ](images/mess-notif-image4.png)

![captura de pantalla de la notificación "iconos sin usar" ](images/mess-notif-image5.png)

![captura de pantalla de la notificación "agregar .NET Passport" ](images/mess-notif-image6.png)

En estos ejemplos, Windows XP está aparentemente formen intentando ayudar a los usuarios con la configuración inicial. Sin embargo, estas notificaciones se muestran con demasiada frecuencia y después son útiles, por lo que son poco más que anuncios de características no solicitadas.

## <a name="user-flow-must-be-maintained"></a>Se debe mantener el flujo de usuario

**Idealmente, los usuarios sumergidos en su trabajo no verán sus notificaciones en absoluto. En su lugar, solo verán las notificaciones cuando su flujo ya esté roto.**

En Flow: la psicología de la experiencia óptima, Mihaly Csikszentmihalyi indica que los usuarios entran en un estado de flujo cuando se absorben por completo en la actividad durante la cual pierden su sentido de tiempo y tienen sentimientos de gran satisfacción.

**Las notificaciones eficaces ayudan a los usuarios a mantener su flujo mediante la presentación de información útil y relevante que se puede omitir fácilmente.** Las notificaciones se presentan en un modo de clave baja y periférico, y no requieren interacción.

No se da por hecho que si las notificaciones son [modelos no modales](glossary.md) , no pueden ser una interrupción molesta. Las notificaciones no requieren la atención de los usuarios, pero ciertamente lo solicitan. Puede interrumpir el flujo de usuarios por:

-   Mostrar notificaciones que los usuarios no importan.
-   Mostrar una notificación con demasiada frecuencia.
-   Usar varias notificaciones cuando una sola notificación es suficiente.
-   Usar sonido al mostrar una notificación.

En Windows 7, los usuarios tienen el control final sobre las notificaciones. **Si los usuarios detectan que las notificaciones de un programa son demasiado molestas, pueden optar por suprimir todas las notificaciones de ese programa.** Asegúrese de que los usuarios no hacen esto en su programa presentando información útil y relevante y siguiendo estas instrucciones.

## <a name="notifications-must-be-ignorable"></a>Las notificaciones se deben poder omitir

**Las notificaciones no requieren la intervención inmediata del usuario y los usuarios pueden omitirlas libremente.**

A menudo, los desarrolladores y diseñadores quieren presentar sus notificaciones de forma que los usuarios no puedan omitir. Este objetivo es totalmente un desaprovechado de las principales ventajas de las notificaciones, ya que se interrumpirá el flujo de los usuarios. Si los usuarios distraen las notificaciones o están obligadas a leerlas, se produce un error en el diseño de notificaciones.

**Si le preocupa que los usuarios omitan las notificaciones, tenga en cuenta lo siguiente:**

-   Si usa notificaciones correctamente y no requiere la intervención inmediata del usuario, el hecho de que los usuarios decidan omitirlas es por diseño. No lo cambie.
-   Si el evento requiere la intervención inmediata del usuario, use una interfaz de usuario alternativa (IU) que los usuarios no puedan omitir. Vea ¿esta es la interfaz de usuario correcta? para las alternativas.

## <a name="use-progressive-escalation-where-applicable"></a>Usar la extensión progresiva cuando proceda

Si se usa una notificación para un evento que los usuarios pueden omitir al principio, pero que deben solucionarse finalmente, se debe usar una interfaz de usuario alternativa cuando la situación sea crítica. Esta técnica se conoce como escalado progresivo.

Por ejemplo, el sistema de administración de energía de Windows indica inicialmente una batería baja cambiando simplemente el icono del área de notificación.

![captura de pantalla de seis iconos que muestran el estado de la batería ](images/mess-notif-image7.png)

En estos ejemplos, la administración de energía de Windows usa el icono del área de notificación para notificar a los usuarios de una energía de batería progresivamente inferior.

A medida que la energía de la batería se vuelve más baja, Windows advierte a los usuarios de una energía de batería débil mediante una notificación.

![captura de pantalla de la notificación de energía de batería baja](images/mess-notif-image8.png)

En este ejemplo, la administración de energía de Windows usa una notificación para indicar a los usuarios que la energía de la batería es débil.

Esta notificación aparece mientras los usuarios siguen teniendo varias opciones. Los usuarios pueden conectar, cambiar sus opciones de energía, ajustar su trabajo y apagar el equipo, o ignorar la notificación y seguir trabajando. A medida que la energía de la batería sigue agotando, el texto y el icono de la notificación reflejan la urgencia adicional. Sin embargo, una vez que la alimentación de la batería se vuelve tan bajo que los usuarios deben actuar inmediatamente, la administración de energía de Windows notifica a los usuarios mediante un cuadro de mensaje [modal](glossary.md) .

![captura de pantalla de una advertencia de energía con una batería seriamente baja](images/mess-notif-image9.png)

En este ejemplo, la administración de energía de Windows usa un cuadro de mensaje modal para notificar a los usuarios de una energía de batería críticamente baja.

**Si solo hace tres cosas...**

1.  Use las notificaciones solo si realmente lo necesita. Cuando se muestra una notificación, puede interrumpir a los usuarios o incluso molestarles. Asegúrese de que la interrupción esté justificada.
2.  Use notificaciones para eventos no críticos o situaciones que no requieran una acción inmediata del usuario. Para eventos críticos o situaciones que requieran una acción inmediata del usuario, use una interfaz de usuario alternativa (como un cuadro de diálogo modal).
3.  Si usa notificaciones, haga que sea una buena experiencia del usuario. No intente forzar a los usuarios a ver las notificaciones. Si los usuarios están tan sumergidos en su trabajo que no ven las notificaciones, el diseño es bueno.

## <a name="usage-patterns"></a>Patrones de uso

Las notificaciones tienen varios patrones de uso:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Acción correcta</strong><br/> Notifica a los usuarios cuando una acción asincrónica iniciada por el usuario se completa correctamente. <br/></td>
<td><strong>Correcto:</strong><br/> <img src="images/mess-notif-image10.png" alt="Screen shot of balloon showing successful updates " /><br/> En este ejemplo, Windows Update notifica a los usuarios cuando su equipo se ha actualizado correctamente.<br/> <strong>Incorrecto:</strong><br/> <img src="images/mess-notif-image11.png" alt="Screen shot of balloon showing file check complete " /><br/> En este ejemplo, Microsoft Outlook notifica a los usuarios cuando se completa una comprobación del archivo de datos. ¿Qué deben hacer los usuarios ahora? ¿Por qué avisar a los usuarios de la finalización correcta?<br/> <strong>Mostrar Cuándo:</strong> Tras la finalización de una tarea asincrónica. Notifique a los usuarios las acciones correctas solo si es probable que estén esperando la finalización o después de errores recientes.<br/> <strong>Mostrar cómo:</strong> Use la opción en tiempo real para que estas notificaciones no estén en cola cuando los usuarios ejecuten una aplicación de pantalla completa o no utilicen activamente su equipo.<br/> <strong>Muestre con qué frecuencia:</strong> Una vez.<br/> <strong>Factor de molestia:</strong> Bajo si no se espera el éxito debido a errores recientes, el éxito se produce después de un error crítico o muy inusual, por lo que el usuario necesita comentarios adicionales o el usuario está esperando la finalización; alto si no.<br/> <strong>Alternativas:</strong> Proporcione comentarios &quot; a petición &quot; mediante la presentación de un icono (o el cambio de un icono existente) en el área de notificación mientras se realiza la operación; Quite el icono (o restaure el icono anterior) cuando se complete la operación. <br/></td>
</tr>
<tr class="even">
<td><strong>Error de acción</strong><br/> Notifica a los usuarios cuando se produce un error en una acción iniciada por el usuario asincrónica. <br/></td>
<td><strong>Correcto:</strong><br/> <img src="images/mess-notif-image12.png" alt="Screen shot of notification of failure to install " /><br/> En este ejemplo, la activación de Windows notifica un error a los usuarios.<br/> <strong>Incorrecto:</strong><br/> <img src="images/mess-notif-image13.png" alt="Screen shot of notification of failure to update " /><br/> En este ejemplo, Microsoft Outlook se utiliza para notificar a los usuarios de un error que no es probable que le interesen.<br/> <strong>Mostrar Cuándo:</strong> Cuando se produce un error en una tarea asincrónica.<br/> <strong>Muestre con qué frecuencia:</strong> Una vez.<br/> <strong>Factor de molestia:</strong> Bajo si es útil y relevante; alto si el problema se solucionará inmediatamente o a los usuarios que, de otro modo, no les interesa.<br/> <strong>Alternativas:</strong> Use un cuadro de diálogo modal si los usuarios deben solucionar el error inmediatamente. <br/></td>
</tr>
<tr class="odd">
<td><strong>Evento no crítico del sistema</strong><br/> Notifica a los usuarios de eventos del sistema o de estado importantes que se pueden omitir sin ningún riesgo, al menos temporalmente. <br/></td>
<td><img src="images/mess-notif-image8.png" alt="Screen shot of notification of low battery power " /><br/> En este ejemplo, Windows advierte a los usuarios de poca energía de la batería, pero todavía hay mucho tiempo antes de tomar medidas.<br/> <strong>Mostrar Cuándo:</strong> Cuando se produce un evento y el usuario está activo, o sigue existiendo una condición. Si se produce un problema, quite las notificaciones mostradas actualmente inmediatamente después de resolver el problema. Al igual que con las notificaciones de acción, notifique a los usuarios los eventos del sistema que se han realizado correctamente solo si es probable que los usuarios estén esperando el evento o después de errores recientes.<br/> <strong>Muestre con qué frecuencia:</strong> Una vez cuando se produce el evento por primera vez. Si esto se debe a un problema que los usuarios deben resolver, vuelva a mostrar una vez al día.<br/> <strong>Factor de molestia:</strong> Bajo, siempre y cuando la notificación no se muestre con demasiada frecuencia.<br/> <strong>Alternativas:</strong> Si los usuarios deben resolver finalmente un problema, use la extensión progresiva al mostrar un cuadro de diálogo modal cuando la resolución sea obligatoria. <br/></td>
</tr>
<tr class="even">
<td><strong>Tarea de usuario opcional</strong><br/> Notifica a los usuarios las tareas asincrónicas que deben realizar. Tanto si es opcional como obligatorio, la tarea se puede posponer de forma segura. <br/></td>
<td><img src="images/mess-notif-image14.png" alt="Screen shot of notification of available updates " /><br/> En este ejemplo, Windows Update notifica a los usuarios una nueva actualización de seguridad.<br/> <strong>Mostrar Cuándo:</strong> Cuando se determina la necesidad de realizar una tarea y el usuario está activo.<br/> <strong>Muestre con qué frecuencia:</strong> Una vez al día durante un máximo de tres veces.<br/> <strong>Factor de molestia:</strong> Bajo, siempre que los usuarios consideren la tarea importante y la notificación no se muestre con demasiada frecuencia.<br/> <strong>Alternativas:</strong> Si los usuarios deben realizar finalmente la tarea, use la extensión progresiva al mostrar un cuadro de diálogo modal cuando la tarea sea obligatoria. <br/></td>
</tr>
<tr class="odd">
<td><strong>Asesor</strong><br/> Notifica a los usuarios la información pertinente potencialmente útil. Puede notificar a los usuarios la información de relevancia marginal si es opcional y los usuarios pueden participar. <br/></td>
<td><strong>Correcto:</strong><br/> <img src="images/mess-notif-image15.png" alt="Screen shot of notification of new e-mail message " /><br/> En este ejemplo, se notifica a los usuarios cuando se recibe un nuevo mensaje de correo electrónico.<br/> <strong>Correcto:</strong><br/> <img src="images/mess-notif-image16.png" alt="Screen shot of notification of contact signed in " /><br/> En este ejemplo, se notifica a los usuarios cuando los contactos están en línea y deciden recibir esta información opcional.<br/> <strong>Incorrecto:</strong><br/> <img src="images/mess-notif-image17.png" alt="Screen shot of notification for faster performance " /><br/> En este ejemplo, la información solo es útil si el usuario ya tiene instalados puertos USB de alta velocidad. De lo contrario, es probable que el usuario no haga nada diferente como resultado.<br/> <strong>Mostrar Cuándo:</strong> Cuando se produce el evento de desencadenamiento.<br/> <strong>Mostrar cómo:</strong> Use la opción en tiempo real para que estas notificaciones no estén en cola cuando los usuarios ejecuten una aplicación de pantalla completa o no utilicen activamente su equipo.<br/> <strong>Muestre con qué frecuencia:</strong> Una vez.<br/> <strong>Factor de molestia:</strong> Medio a alto, en función de la percepción de los usuarios de utilidad y relevancia. No se recomienda si hay una baja probabilidad de que el usuario tenga interés.<br/> <strong>Alternativas:</strong> No notificar a los usuarios. <br/></td>
</tr>
<tr class="even">
<td><strong>Anuncio de características</strong><br/> Notifica a los usuarios de las características de aplicación o del sistema no utilizadas recién instaladas.<br/></td>
<td><strong>No use notificaciones para anuncios de características.</strong> En su lugar, use otra manera de que la característica sea reconocible, como: <br/>
<ul>
<li>Diseñe la característica para que sea más fácil de detectar en contextos donde sea necesario.</li>
<li>No haga nada especial y deje que los usuarios detecten la característica por su cuenta.</li>
</ul>
<strong>Incorrecto:</strong><br/> <img src="images/mess-notif-image4.png" alt="Screen shot of notification of new features " /><br/> No use notificaciones para anuncios de características.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Seleccione el patrón de notificación en función de su uso.** Para obtener una descripción de cada patrón de uso, vea la tabla anterior.
-   **No utilice ninguna notificación durante la experiencia inicial de Windows.** Para mejorar su primera experiencia, Windows 7 suprime todas las notificaciones que se muestran en las primeras horas de uso. Diseñe el programa, suponiendo que los usuarios no vean estas notificaciones.

### <a name="what-to-notify"></a>Qué notificar

-   **No notifique las operaciones correctas, excepto en las siguientes circunstancias:**
    -   **Seguridad.** Los usuarios consideran que las operaciones de seguridad son de la mayor importancia, por lo que notifican a los usuarios las operaciones de seguridad correctas.
    -   **Error reciente.** Los usuarios no toman las operaciones correctas para que se les concedan si se produjeran errores inmediatamente antes, por lo que debe notificar a los usuarios si la operación no se ha realizado recientemente.
    -   **Evite molestias.** Informar de las operaciones correctas al hacerlo puede evitar los usuarios de perturbar. Por lo tanto, notifique a los usuarios cuando se realice una operación correcta de una manera inesperada, como cuando una operación es larga o se completa antes o después de lo esperado.
-   **En otras circunstancias, no proporcione ningún comentario para el éxito o envíe comentarios "a petición".** Supongamos que los usuarios realizan las operaciones correctas para concedidos. Puede proporcionar comentarios a petición mostrando un icono (o cambiando un icono existente) en el área de notificación mientras se realiza la operación y quitando el icono (o restaurando el icono anterior) cuando se complete la operación.
-   Para el patrón FYI, **no envíe una notificación si los usuarios pueden seguir trabajando con normalidad o no es probable que hagan nada diferente como resultado de la notificación.**

    **Incorrecto:**

    ![captura de pantalla de la notificación para obtener un rendimiento más rápido ](images/mess-notif-image17.png)

    En este ejemplo, la información solo es útil si el usuario ya tiene los puertos instalados. De lo contrario, es probable que el usuario no haga nada diferente como resultado.

    -   Excepción: **puede notificar a los usuarios la información de relevancia cuestionable si es opcional y los usuarios pueden participar.**

        **Correcto:**

        ![captura de pantalla de la notificación de contacto con sesión iniciada ](images/mess-notif-image16.png)

        En este ejemplo, se notifica a los usuarios cuando los contactos están en línea y deciden recibir esta información opcional.

-   En el caso de los patrones de eventos y de los que no son críticos del sistema, **use notificaciones completas para un solo evento.** No presentar varias partes parciales.

    **Incorrecto:**

    ![captura de pantalla de las notificaciones de "encontrado nuevo hardware" ](images/mess-notif-image18.png)

    En estos ejemplos se muestran solo cuatro de las ocho notificaciones mostradas por Windows XP cuando un usuario conecta un teclado USB específico y presenta más información de forma incremental.

    **Correcto:**

    ![captura de pantalla de notificaciones de estado de instalación ](images/mess-notif-image19.png)

    En este ejemplo, al adjuntar un teclado USB se generan dos notificaciones completas.

### <a name="when-to-notify"></a>Cuándo notificar

-   **Mostrar una notificación basada en su modelo de diseño:**



|                                      |                                                                                                                                                                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Patrón**<br/>               | **Cuándo notificar**<br/>                                                                                                                                                                                      |
| Acción correcta<br/>            | Tras la finalización de una tarea asincrónica. Notifique a los usuarios las acciones correctas solo si es probable que estén esperando la finalización o después de errores recientes.<br/>                                             |
| Error de acción<br/>            | Cuando se produce un error en una tarea asincrónica.<br/>                                                                                                                                                                   |
| Evento no crítico del sistema<br/> | Cuando se produce un evento y el usuario está activo o la condición sigue existiendo. Si el resultado es un problema, quite la notificación mostrada actualmente inmediatamente después de resolver el problema.<br/> |
| Tarea de usuario opcional<br/>        | Cuando se determina la necesidad de realizar una tarea y el usuario está activo.<br/>                                                                                                                                   |
| Asesor<br/>                       | Cuando se produce el evento de desencadenamiento.<br/>                                                                                                                                                                       |



 

-   En el caso del patrón de error de acción, **si el problema puede corregirse en cuestión de segundos, retrase la notificación de error durante un período de tiempo adecuado.** Si el problema se corrige, no se notifica nada. La notificación solo después de que haya transcurrido el tiempo suficiente ha superado el error. Si informa demasiado pronto, lo más probable es que los usuarios no perciban el problema notificado, pero observarán la notificación innecesaria.

**Incorrecto:**

![captura de pantalla de no hay notificación de conexión de red ](images/mess-notif-image20.png)

Cuando va inmediatamente seguido de:

![captura de pantalla de la notificación de conexión correcta ](images/mess-notif-image21.png)

En este ejemplo, en Windows Vista, la notificación de que no hay conectividad inalámbrica es prematura, porque a menudo está inmediatamente seguida de una notificación de buena conectividad.

-   En el caso de los patrones de acción correcta y de información, **use la opción en tiempo real para que las notificaciones obsoletas no** se encuentren en cola cuando los usuarios ejecuten una aplicación de pantalla completa o no utilicen activamente su equipo.
-   En el caso del patrón de eventos del sistema no crítico, **no cree el potencial para las tormentas de notificaciones mediante la escalonación de eventos relacionados con eventos conocidos como el inicio de sesión de usuario.** En su lugar, asocie el evento a algún período de tiempo después del evento. Por ejemplo, puede recordar a los usuarios que registren el producto cinco minutos después del inicio de sesión de usuario.

### <a name="how-long-to-notify"></a>Cuánto tiempo se notificará

En Windows Vista y versiones posteriores, se muestran notificaciones para una duración fija de 9 segundos.

### <a name="how-often-to-notify"></a>Frecuencia de notificación

-   **El número de veces que se va a mostrar una notificación se basa en su modelo de diseño:**



|                                      |                                                                                                                             |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **Patrón**<br/>               | **Frecuencia de notificación**<br/>                                                                                          |
| Acción correcta<br/>            | Una vez.<br/>                                                                                                            |
| Error de acción<br/>            | Una vez.<br/>                                                                                                            |
| Evento no crítico del sistema<br/> | Una vez cuando se produce el evento por primera vez. Si esto se debe a un problema que los usuarios deben resolver, vuelva a mostrar una vez al día.<br/> |
| Tarea de usuario opcional<br/>        | Una vez al día durante un máximo de tres veces.<br/>                                                                         |
| Asesor<br/>                       | Una vez.<br/>                                                                                                            |



 

-   **En el caso de las tareas de usuario opcionales, no intente Pester a los usuarios en el envío al mostrar constantemente las notificaciones.** Si la tarea es necesaria, muestre un cuadro de diálogo modal inmediatamente en lugar de usar las notificaciones.

### <a name="notification-escalation"></a>Escalación de notificaciones

-   **No suponga que los usuarios verán sus notificaciones.** Los usuarios no los verán cuando:
    -   Están sumergidos en su trabajo.
    -   No prestan atención.
    -   Están fuera de su equipo.
    -   Ejecutan una aplicación de pantalla completa.
    -   Su administrador ha desactivado todas las notificaciones de su equipo.
-   **Si los usuarios deben realizar algún tipo de acción, use la extensión progresiva** para mostrar una interfaz de usuario alternativa que los usuarios no puedan omitir.

### <a name="interaction"></a>Interacción

-   **Hacer que se haga clic en las notificaciones cuando:**
    -   **Los usuarios deben realizar una acción.** Al hacer clic en la notificación, se muestra una ventana en la que los usuarios pueden realizar la acción. Este enfoque es el preferido para el error de acción y los patrones de diseño de tareas de usuario opcionales.
    -   **Es posible que los usuarios deseen ver más información.** Al hacer clic en la notificación, se muestra una ventana en la que los usuarios pueden ver información adicional.
-   **Mostrar siempre una ventana cuando los usuarios hacen clic para realizar una acción.** No haga clic en realizar una acción directamente.
-   **Al hacer clic para mostrar más información, siempre debería mostrar más información.** No basta con volver a formular la información que ya está en la notificación.

### <a name="icons"></a>Iconos

-   **Para el patrón de error de acción, use el icono de error estándar.**
-   **En el caso de los patrones de eventos del sistema no críticos, use el icono de advertencia estándar.**
-   **En el caso de otros patrones, use los iconos que muestran los objetos que se relacionan con el asunto o lo sugieren**, como un escudo para la seguridad o una batería de energía.
-   **Use iconos basados en la aplicación o la personalización de marca de empresa si los usuarios de destino los reconocerán y no hay ninguna alternativa mejor.**
-   Para una escalación progresiva, **considere la posibilidad de usar iconos con una apariencia progresivamente más Emphatic a medida que la situación sea más urgente.**
-   **No use el icono de información estándar.** Las notificaciones son información que no indica.
-   **Considere la posibilidad de usar iconos grandes (32x32 píxeles) cuando:**
    -   Los usuarios comprenderán rápidamente el icono en lugar del texto.
    -   Los iconos grandes transmiten su significado de forma más clara y eficaz que los iconos estándar de 16x16 píxeles.
    -   El icono usa el [estilo Aero](vis-icons.md).

![captura de pantalla de la notificación de "mensajes importantes" ](images/mess-notif-image22.png)

En este ejemplo, los usuarios pueden comprender rápidamente la naturaleza de la notificación con un vistazo en el icono grande.

### <a name="notification-queuing"></a>Puesta en cola de notificaciones

**Nota:** Las notificaciones se ponen en cola cuando no se pueden mostrar inmediatamente, por ejemplo, cuando se muestra otra notificación, el usuario ejecuta una aplicación de pantalla completa o el usuario no usa el equipo de forma activa. Las notificaciones en tiempo real permanecen en la cola durante solo 60 segundos.

-   **En el caso de los patrones de acción correcta y FYI, use la opción en tiempo real** para que la notificación no se encuentre en cola durante mucho tiempo. Estas notificaciones tienen valor solo cuando se pueden mostrar inmediatamente.
-   **Quite las notificaciones en cola cuando ya no sean relevantes.**
-   **Desarrolladores:** Para ello, establezca la \_ marca de información de NSI en uFlags y establezca szInfo en una cadena vacía. No hay ningún daño al hacerlo si la notificación ya no está en la cola.

### <a name="system-integration"></a>Integración del sistema

-   Si la aplicación no siempre tiene un icono en el [área de notificación](winenv-notification.md) cuando se está ejecutando, **Mostrar un icono temporalmente durante la tarea o el evento asincrónico que causó la notificación.**

## <a name="text"></a>Texto

### <a name="title-text"></a>Texto del título

-   **Use el texto del título que resume brevemente la información más importante que necesita para comunicarse con los usuarios en lenguajes claros, sencillos y concisos.** Los usuarios deben poder comprender el propósito de la información de notificación rápidamente y con el mínimo esfuerzo.
-   **Utilice fragmentos de texto o frases completas sin puntuación final.**
-   **Use mayúsculas de estilo de frase.**
-   **No use más de 48 caracteres (en inglés) para dar cabida a la localización.** El título tiene una longitud máxima de 63 caracteres, pero debe permitir una expansión del 30 por ciento cuando se traduzca el texto en inglés.

### <a name="body-text"></a>Texto del cuerpo

-   **Use el texto del cuerpo que proporciona una descripción (sin repetir la información en el título) y, opcionalmente, que proporciona detalles específicos sobre la notificación, y también permite a los usuarios saber qué acción está disponible.**
-   **Use frases completas con una puntuación final.**
-   **Use mayúsculas de estilo de frase.**
-   **No use más de 200 caracteres (en inglés) para dar cabida a la localización.** El texto del cuerpo tiene una longitud máxima de 255 caracteres, pero debe permitir una expansión del 30 por ciento cuando se traduzca el texto en inglés.
-   **Incluye información esencial en el texto del cuerpo, como los nombres de objeto específicos.** (Ejemplos: nombres de usuario, nombres de archivo o direcciones URL). Los usuarios no deben tener que abrir otra ventana para encontrar dicha información.
-   **Ponga comillas dobles alrededor de los nombres de objeto.**
    -   **Excepción:** No utilice comillas cuando:
        -   El nombre del objeto siempre usa el uso [de mayúsculas del estilo de título](glossary.md), como con los nombres de usuario.
        -   El nombre del objeto se desplaza con dos puntos (por ejemplo: nombre de la impresora: mi impresora).
        -   El nombre de objeto se puede determinar fácilmente a partir del contexto.
-   **Si debe truncar los nombres de objeto a un tamaño máximo fijo para dar cabida a la localización, use un botón de puntos suspensivos para indicar el truncamiento.**

    ![captura de pantalla del mensaje que contiene el nombre abreviado ](images/mess-notif-image23.png)

    En este ejemplo, un nombre de objeto se trunca mediante puntos suspensivos.

-   **Use la siguiente frase si la notificación es accionable:**
    -   Si los usuarios pueden hacer clic en la notificación para realizar una acción:

        < breve descripción de la información esencial>

        <optional details>

        Haga clic en para <do something> .

        ![captura de pantalla del mensaje: ' haga clic para ver el progreso ' ](images/mess-notif-image24.png)

        En este ejemplo, los usuarios pueden hacer clic para realizar una acción.

    -   Si los usuarios pueden hacer clic en la notificación para ver más información:

        < breve descripción de la información esencial>

        <optional details>

        Haga clic para obtener más información.

        ![captura de pantalla del mensaje: haga clic para obtener más información. ](images/mess-notif-image25.png)

        En este ejemplo, los usuarios pueden hacer clic para obtener más información.

-   **No indique que el usuario "debe" realizar una acción en una notificación.** Las notificaciones son para información no crítica que los usuarios pueden ignorar libremente. Si los usuarios realmente deben realizar una acción, no use las notificaciones.
-   **Si los usuarios deben realizar una acción, haga que la importancia sea clara.**
-   En el caso de los patrones de eventos de error de acción y del sistema no críticos, **describa los problemas en lenguaje sencillo.**

    **Incorrecto:**

    ![captura de pantalla de mensaje largo y complejo ](images/mess-notif-image26.png)

    En este ejemplo, el problema se describe mediante un lenguaje muy técnico pero no específico.

    **Correcto:**

    ![captura de pantalla de un mensaje claro y conciso ](images/mess-notif-image27.png)

    En este ejemplo, el problema se describe en lenguaje sencillo.

-   **Describa el evento de un modo que sea relevante para los usuarios de destino.** Una notificación es relevante si hay una posibilidad razonable de que los usuarios realicen una tarea o cambien su comportamiento como resultado de la notificación. A menudo, esto se puede lograr mediante la descripción de las notificaciones en términos de objetivos del usuario en lugar de problemas tecnológicos.

## <a name="documentation"></a>Documentación

Al hacer referencia a las notificaciones:

-   Use el texto de título exacto, incluido el uso de mayúsculas.
-   Haga referencia al componente como una notificación, no como un globo o una alerta.
-   Para describir la interacción del usuario, use haga clic en.
-   Siempre que sea posible, dé formato al texto del título usando texto en negrita. De lo contrario, coloque el título entre comillas solo si es necesario para evitar confusiones.

Ejemplo: cuando aparezca la notificación las **actualizaciones críticas están listas para instalar** , haga clic en la notificación para iniciar el proceso.

Al hacer referencia al área de notificación:

-   Consulte el área de notificación en el área de notificación, no en la bandeja del sistema.

 

