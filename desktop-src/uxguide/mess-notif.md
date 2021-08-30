---
title: Notificaciones (conceptos básicos de diseño)
description: Una notificación informa a los usuarios de eventos que no están relacionados con la actividad del usuario actual, mostrando brevemente un globo de un icono en el área de notificación.
ms.assetid: dcac2fb7-e503-4ea3-a2c5-e3cb660c040a
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a75c6530898071bb2ef28cf730b0cd4f83be9cbe
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983288"
---
# <a name="notifications-design-basics"></a>Notificaciones (conceptos básicos de diseño)

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Una notificación informa a los usuarios de eventos que no están relacionados con la actividad del usuario actual, mostrando brevemente un globo de un icono en el área de notificación. La notificación podría ser el resultado de una acción del usuario o un evento significativo del sistema, o bien podría ofrecer información potencialmente útil de Microsoft Windows o una aplicación.

La información de una notificación es **útil y pertinente, pero nunca es crítica.** Por lo tanto, las notificaciones no requieren una acción inmediata del usuario y los usuarios pueden ignorarlas libremente.

![captura de pantalla del globo con "nuevas actualizaciones" en el título ](images/mess-notif-image1.png)

Una notificación típica.

En Windows Vista y versiones posteriores, las notificaciones se muestran durante una duración fija de 9 segundos. Las notificaciones no se muestran inmediatamente cuando los usuarios están inactivos o se están ejecutando protectores de pantalla. Windows pone en cola automáticamente las notificaciones durante estos momentos y muestra las notificaciones en cola cuando el usuario reanuda la actividad normal. Por lo tanto, no tiene que hacer nada para controlar estas circunstancias especiales.

**Desarrolladores:** Puede determinar cuándo está activo el usuario mediante la API SHQueryUserNotificationState.

**Nota:** Las directrices relacionadas [con el área de notificación,](winenv-notification.md)la [barra](winenv-taskbar.md)de tareas y los globos se presentan en [artículos](ctrl-balloons.md) independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

Para decidirte, intenta responder a estas preguntas:

-   **¿Es la información el resultado inmediato y directo de la interacción de los usuarios con la aplicación?** Si es así, muestre esta información sincrónica directamente dentro de la aplicación en su lugar mediante un cuadro de diálogo [,](win-dialog-box.md)un cuadro de [mensaje,](glossary.md)un globo [o](ctrl-balloons.md)una interfaz [de](glossary.md) usuario local. Las notificaciones son solo para la información asincrónica.

![captura de pantalla de la alerta de seguridad de Windows ](images/mess-notif-image2.png)

En este ejemplo, el cuadro Windows de diálogo Excepciones de firewall se muestra como resultado directo de la interacción del usuario. Una notificación no sería adecuada aquí.

-   **¿La información es relevante solo cuando los usuarios usan activamente la aplicación?** Si es así, muestre la información en la barra de estado de la [aplicación](ctrl-status-bars.md) u otro área de estado.

![captura de pantalla de la barra de estado de Outlook ](images/mess-notif-image3.png)

En este ejemplo, Outlook muestra su estado de conexión y sincronización en su barra de estado.

-   **¿La información cambia rápidamente, es continua y en tiempo real?** Algunos ejemplos son el progreso del procesamiento, las cotizaciones bursátiles y las puntuaciones de deportes. Si es así, no use notificaciones porque no son adecuadas para cambiar rápidamente la información.
-   **¿La información es útil y pertinente? ¿Es probable que los usuarios cambien su comportamiento o eviten inconvenientes como resultado de recibir la información?** Si no es así, no muestre la información ni la coloque en una ventana de estado o un archivo de registro.
-   **¿Es crítica la información? ¿Se requiere una acción inmediata?** Si es así, muestre la información mediante una interfaz que requiere atención y no se puede omitir fácilmente, como un cuadro de diálogo modal o un cuadro de mensaje. Si el programa no está activo, puede llamar [](winenv-taskbar.md) la atención sobre la información crítica si parpadea el botón de la barra de tareas del programa tres veces y lo deja resaltado hasta que el programa esté activo.
-   **¿Son los principales profesionales de IT de los usuarios de destino?** Si es así, use un mecanismo de comentarios alternativo, como entradas de [archivo](glossary.md) de registro o mensajes de correo electrónico. Los profesionales de TI prefieren encarecidamente los archivos de registro para obtener información no crítica. Además, los servidores a menudo se administran de forma remota y normalmente se ejecutan sin que ningún usuario haya iniciado sesión, lo que hace que las notificaciones sean ineficaces.

## <a name="design-concepts"></a>Conceptos de diseño

Las notificaciones eficaces que promueven una buena experiencia del usuario son:

-   **Asincrónica.** El evento no es un resultado inmediato y directo de la interacción actual de los usuarios con Microsoft Windows o la aplicación.
-   **Útil.** Existe una posibilidad razonable de que los usuarios realicen una tarea o cambien su comportamiento como resultado de la notificación.
-   **Relevante.** La notificación muestra información útil que a los usuarios les interesa y que aún no conocen.
-   **No es crítico.** Las notificaciones no son modales y no requieren interacción del usuario, por lo que los usuarios pueden omitirlas libremente.
-   **Procesable.** Para las notificaciones que sugieren realizar una acción, esa acción se inicia haciendo clic en la notificación. Sin embargo, la acción siempre se puede posponer.
-   **Se presenta correctamente.** La presentación de la notificación (duración, frecuencia, texto, icono e interactividad) coincide con sus circunstancias.
-   **No es molesto.** Hay una línea fina entre informar a los usuarios de un evento y molestarlos.

Desafortunadamente, hay demasiadas notificaciones molestos, inapropiadas, inutiles e irrelevantes. Tenga en cuenta estas notificaciones de la Windows XP Hall of Alsoy:

![captura de pantalla de la notificación "tour windows xp" ](images/mess-notif-image4.png)

![captura de pantalla de la notificación "iconos no usados" ](images/mess-notif-image5.png)

![captura de pantalla de la notificación "agregar .net passport" ](images/mess-notif-image6.png)

En estos ejemplos, Windows XP está intentando ayudar a los usuarios con su configuración inicial. Sin embargo, estas notificaciones se presentan con demasiada frecuencia y bien después de que sean útiles, por lo que son poco más que anuncios de características no solicitados.

## <a name="user-flow-must-be-maintained"></a>Se debe mantener el flujo de usuario

**Idealmente, los usuarios inmersos en su trabajo no verán las notificaciones en absoluto. En su lugar, solo verán las notificaciones cuando su flujo ya esté roto.**

En Flow: The Optimal Experience(La historia de la experiencia óptima), Mihaly Csikikikmihalyi indica que los usuarios entran en un estado de flujo cuando están totalmente satisfechos con la actividad durante la cual pierden el sentido del tiempo y tienen una gran satisfacción.

**Las notificaciones eficaces ayudan a los usuarios a mantener su flujo mediante la presentación de información útil y pertinente que se puede omitir fácilmente.** Las notificaciones se presentan de forma de clave baja y periférico, y no requieren interacción.

No suponga que si las notificaciones son [modelesas,](glossary.md) no pueden ser una interrupción insoportable. Las notificaciones no exigen la atención de los usuarios, pero ciertamente la solicitan. Puede interrumpir el flujo de usuarios mediante:

-   Mostrar notificaciones que a los usuarios no les importan.
-   Mostrar una notificación con demasiada frecuencia.
-   Usar varias notificaciones cuando una sola notificación es suficiente.
-   Usar sonido al mostrar una notificación.

En Windows 7, los usuarios tienen el control final sobre las notificaciones. **Si los usuarios descubren que las notificaciones de un programa son demasiado pesadas, pueden optar por suprimir todas las notificaciones de ese programa.** Asegúrese de que los usuarios no hacen esto en el programa mediante la presentación de información útil y pertinente y siguiendo estas directrices.

## <a name="notifications-must-be-ignorable"></a>Las notificaciones deben ser omitibles

**Las notificaciones no requieren una acción inmediata del usuario y los usuarios pueden omitirlas libremente.**

A menudo, los desarrolladores y diseñadores quieren presentar sus notificaciones de una manera que los usuarios no puedan omitir. Este objetivo vulnera completamente la ventaja principal de las notificaciones, ya que interrumpiría el flujo de los usuarios. Si los usuarios se distraen por las notificaciones o se siente obligados a leerlas, se ha dado un error en el diseño de la notificación.

**Si le preocupa que los usuarios omita las notificaciones, tenga en cuenta lo siguiente:**

-   Si usa las notificaciones correctamente y no requieren una acción inmediata del usuario, hacer que los usuarios decidan omitirlas es por diseño. No cambie esto.
-   Si el evento requiere una acción inmediata del usuario, use una interfaz de usuario alternativa que los usuarios no puedan omitir. Consulte ¿Es la interfaz de usuario adecuada? para las alternativas.

## <a name="use-progressive-escalation-where-applicable"></a>Uso de la escalación progresiva cuando corresponda

Si se usa una notificación para un evento que los usuarios pueden omitir de forma segura al principio, pero que debe solucionarse finalmente, se debe usar una interfaz de usuario alternativa cuando la situación se vuelva crítica. Esta técnica se conoce como escalación progresiva.

Por ejemplo, el Windows de administración de energía indica inicialmente una batería baja simplemente cambiando su icono de área de notificación.

![captura de pantalla de seis iconos que muestran el estado de la batería ](images/mess-notif-image7.png)

En estos ejemplos, la Windows de energía usa el icono del área de notificación para notificar a los usuarios que la batería se reduce progresivamente.

A medida que la potencia de la batería se reduce, Windows a los usuarios de una batería débil mediante una notificación.

![captura de pantalla de notificación de bajo consumo de batería](images/mess-notif-image8.png)

En este ejemplo, Windows administración de energía usa una notificación para decir a los usuarios que su batería es débil.

Esta notificación aparece mientras los usuarios siguen teniendo varias opciones. Los usuarios pueden conectarse, cambiar sus opciones de energía, encapsular su trabajo y apagar el equipo, o omitir la notificación y seguir trabajando. A medida que la energía de la batería sigue agotando, el texto y el icono de la notificación reflejan la urgencia adicional. Sin embargo, una vez que la batería se vuelve tan baja que los usuarios deben actuar inmediatamente, Windows administración de energía notifica a los usuarios mediante un [cuadro de](glossary.md) mensaje modal.

![captura de pantalla de advertencia de batería muy baja](images/mess-notif-image9.png)

En este ejemplo, Windows administración de energía usa un cuadro de mensaje modal para notificar a los usuarios una batería críticamente baja.

**Si solo hace tres cosas...**

1.  Use notificaciones solo si realmente lo necesita. Cuando se muestra una notificación, es posible que interrumpa a los usuarios o incluso los fastidie. Asegúrese de que la interrupción está justificada.
2.  Use notificaciones para eventos no críticos o situaciones que no requieran una acción inmediata del usuario. Para eventos críticos o situaciones que requieren una acción inmediata del usuario, use una interfaz de usuario alternativa (como un cuadro de diálogo modal).
3.  Si usa notificaciones, conséctese por una buena experiencia del usuario. No intente forzar a los usuarios a ver las notificaciones. Si los usuarios están tan inmersos en su trabajo que no ven las notificaciones, el diseño es bueno.

## <a name="usage-patterns"></a>Patrones de uso

Las notificaciones tienen varios patrones de uso:




| Etiqueta | Value |
|--------|-------|
| <strong>Acción correcta</strong><br /> Notifica a los usuarios cuándo se completa correctamente una acción asincrónica iniciada por el usuario. <br /> | <strong>Correcto:</strong><br /><img src="images/mess-notif-image10.png" alt="Screen shot of balloon showing successful updates " /><br /> En este ejemplo, Windows Update notifica a los usuarios cuándo su equipo se ha actualizado correctamente.<br /><strong>Incorrecto:</strong><br /><img src="images/mess-notif-image11.png" alt="Screen shot of balloon showing file check complete " /><br /> En este ejemplo, Microsoft Outlook notifica a los usuarios cuando se completa una comprobación del archivo de datos. ¿Qué deben hacer ahora los usuarios? ¿Y por qué advertir a los usuarios sobre la finalización correcta?<br /><strong>Mostrar cuándo:</strong> Tras la finalización de una tarea asincrónica. Notifique a los usuarios las acciones correctas solo si es probable que estén esperando la finalización o después de errores recientes.<br /><strong>Mostrar cómo:</strong> Use la opción en tiempo real para que estas notificaciones no se ponen en cola cuando los usuarios ejecutan una aplicación de pantalla completa o no usan activamente su equipo.<br /><strong>Mostrar con qué frecuencia:</strong> Una vez.<br /><strong>Factor de molestia:</strong> Bajo si no se espera éxito debido a errores recientes, el éxito se produce después de un error crítico o muy inusual, por lo que el usuario necesita comentarios adicionales o el usuario está esperando su finalización. alto si no es así.<br /><strong>Alternativas:</strong> Para enviar comentarios "a petición", muestre un icono (o cambie un icono existente) en el área de notificación mientras se realiza la operación. quite el icono (o restaure el icono anterior) cuando se complete la operación. <br /> | 
| <strong>Error de acción</strong><br /> Notifica a los usuarios cuando se produce un error en una acción asincrónica iniciada por el usuario. <br /> | <strong>Correcto:</strong><br /><img src="images/mess-notif-image12.png" alt="Screen shot of notification of failure to install " /><br /> En este ejemplo, Windows la activación notifica a los usuarios si se produce un error.<br /><strong>Incorrecto:</strong><br /><img src="images/mess-notif-image13.png" alt="Screen shot of notification of failure to update " /><br /> En este ejemplo, Microsoft Outlook para notificar a los usuarios un error que es poco probable que les preocupa.<br /><strong>Mostrar cuándo:</strong> Tras un error de una tarea asincrónica.<br /><strong>Mostrar con qué frecuencia:</strong> Una vez.<br /><strong>Factor de molestia:</strong> Bajo si es útil y pertinente; es alto si el problema se resolverá de inmediato o a los usuarios no les importa.<br /><strong>Alternativas:</strong> Use un cuadro de diálogo modal si los usuarios deben solucionar el error inmediatamente. <br /> | 
| <strong>Evento del sistema no crítico</strong><br /> Notifica a los usuarios eventos o estados significativos del sistema que se pueden omitir de forma segura, al menos temporalmente. <br /> | <img src="images/mess-notif-image8.png" alt="Screen shot of notification of low battery power " /><br /> En este ejemplo, Windows advierte a los usuarios de una batería baja, pero todavía hay mucho tiempo antes de que tomen medidas.<br /><strong>Mostrar cuándo:</strong> Cuando se produce un evento y el usuario está activo o sigue existiendo una condición. Si es el resultado de un problema, quite las notificaciones que se muestran actualmente inmediatamente una vez resuelto el problema. Al igual que con las notificaciones de acción, notifique a los usuarios eventos del sistema correctos solo si es probable que los usuarios estén esperando el evento o después de errores recientes.<br /><strong>Mostrar con qué frecuencia:</strong> Una vez cuando se produce el evento por primera vez. Si esto se debe a un problema que los usuarios deben resolver, vuelva a mostrar una vez al día.<br /><strong>Factor de molestia:</strong> Bajo, siempre y cuando la notificación no se muestre con demasiada frecuencia.<br /><strong>Alternativas:</strong> Si los usuarios finalmente deben resolver un problema, use la extensión progresiva mostrando en última instancia un cuadro de diálogo modal cuando la resolución sea obligatoria. <br /> | 
| <strong>Tarea de usuario opcional</strong><br /> Notifica a los usuarios las tareas asincrónicas que deben realizar. Tanto si es opcional como si es necesario, la tarea se puede posponer de forma segura. <br /> | <img src="images/mess-notif-image14.png" alt="Screen shot of notification of available updates " /><br /> En este ejemplo, Windows update notifica a los usuarios una nueva actualización de seguridad.<br /><strong>Mostrar cuándo:</strong> Cuando se determina la necesidad de realizar una tarea y el usuario está activo.<br /><strong>Mostrar con qué frecuencia:</strong> Una vez al día durante un máximo de tres veces.<br /><strong>Factor de molestia:</strong> Bajo, siempre y cuando los usuarios consideren importante la tarea y la notificación no se muestre con demasiada frecuencia.<br /><strong>Alternativas:</strong> Si finalmente los usuarios deben realizar la tarea, use la escalación progresiva mostrando en última instancia un cuadro de diálogo modal cuando la tarea sea obligatoria. <br /> | 
| <strong>FYI</strong><br /> Notifica a los usuarios información potencialmente útil y pertinente. Puede notificar a los usuarios información de relevancia marginal si es opcional y los usuarios deciden participar. <br /> | <strong>Correcto:</strong><br /><img src="images/mess-notif-image15.png" alt="Screen shot of notification of new e-mail message " /><br /> En este ejemplo, se notifica a los usuarios cuando se recibe un nuevo mensaje de correo electrónico.<br /><strong>Correcto:</strong><br /><img src="images/mess-notif-image16.png" alt="Screen shot of notification of contact signed in " /><br /> En este ejemplo, se notifica a los usuarios cuando los contactos se pone en línea y deciden recibir esta información opcional.<br /><strong>Incorrecto:</strong><br /><img src="images/mess-notif-image17.png" alt="Screen shot of notification for faster performance " /><br /> En este ejemplo, la información solo es útil si el usuario ya tiene instalados puertos USB de alta velocidad. De lo contrario, es probable que el usuario no haga nada diferente como resultado de ella.<br /><strong>Mostrar cuándo:</strong> Cuando se produce el evento de desencadenamiento.<br /><strong>Mostrar cómo:</strong> Use la opción en tiempo real para que estas notificaciones no se ponen en cola cuando los usuarios ejecutan una aplicación de pantalla completa o no usan activamente su equipo.<br /><strong>Mostrar con qué frecuencia:</strong> Una vez.<br /><strong>Factor de molestia:</strong> Medio a alto, en función de la percepción de utilidad y relevancia de los usuarios. No se recomienda si hay una probabilidad baja de interés del usuario.<br /><strong>Alternativas:</strong> No notifique a los usuarios. <br /> | 
| <strong>Anuncio de características</strong><br /> Notifica a los usuarios las características del sistema o la aplicación recién instaladas y sin usar.<br /> | <strong>No use notificaciones para anuncios de características.</strong> En su lugar, use otra manera de hacer que la característica sea reconocible, como: <br /><ul><li>Diseñe la característica para que sea más fácil de detectar en contextos donde sea necesario.</li><li>No haga nada especial y permita que los usuarios descubran la característica por sí mismos.</li></ul><strong>Incorrecto:</strong><br /><img src="images/mess-notif-image4.png" alt="Screen shot of notification of new features " /><br /> No use notificaciones para anuncios de características.<br /> | 




 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Seleccione el patrón de notificación en función de su uso.** Para obtener una descripción de cada patrón de uso, consulte la tabla anterior.
-   **No use ninguna notificación durante la experiencia de Windows inicial.** Para mejorar su primera experiencia, Windows 7 suprime todas las notificaciones mostradas durante las primeras horas de uso. Diseñe el programa suponiendo que los usuarios no verán dichas notificaciones.

### <a name="what-to-notify"></a>Qué notificar

-   **No notifique operaciones correctas, excepto en las siguientes circunstancias:**
    -   **Seguridad.** Los usuarios consideran que las operaciones de seguridad son de mayor importancia, por lo que deben notificar a los usuarios las operaciones de seguridad correctas.
    -   **Error reciente.** Los usuarios no toman las operaciones correctas para concederse si se ha dado un error inmediatamente antes, así que notifique a los usuarios si la operación se ha realizado correctamente cuando se ha dado un error recientemente.
    -   **Evitar inconvenientes.** Notificar operaciones correctas al hacerlo podría evitar la incoherencia de los usuarios. Por lo tanto, notifique a los usuarios cuándo se realiza una operación correcta de forma inesperada, por ejemplo, cuando una operación es larga o se completa antes o después de lo esperado.
-   **En otras circunstancias, no enviar comentarios sobre el éxito o enviar comentarios "a petición".** Supongamos que los usuarios llevan a cabo operaciones correctas para concederse. Puede enviar comentarios a petición mostrando un icono (o cambiando un icono existente) en el área de notificación mientras se realiza la operación y quitando el icono (o restaurando el icono anterior) una vez completada la operación.
-   Para el patrón FYI, no realice una notificación si los usuarios pueden seguir trabajando con normalidad o es poco probable que hagan algo diferente como resultado **de la notificación.**

    **Incorrecto:**

    ![captura de pantalla de la notificación para un rendimiento más rápido ](images/mess-notif-image17.png)

    En este ejemplo, la información solo es útil si el usuario ya tiene instalados los puertos. De lo contrario, es probable que el usuario no haga nada diferente como resultado de él.

    -   Excepción: puede notificar a los usuarios información de relevancia que puede ser preguntable **si es opcional y los usuarios optan por participar.**

        **Correcto:**

        ![captura de pantalla de la notificación del contacto que ha iniciado sesión ](images/mess-notif-image16.png)

        En este ejemplo, se notifica a los usuarios cuando los contactos se pone en línea y deciden recibir esta información opcional.

-   Para el evento del sistema no crítico y los patrones FYI, **use notificaciones completas para un único evento.** No presente varios parciales.

    **Incorrecto:**

    ![captura de pantalla de las notificaciones de "nuevo hardware encontrado" ](images/mess-notif-image18.png)

    Estos ejemplos muestran solo cuatro de las ocho notificaciones mostradas por Windows XP cuando un usuario adjunta un teclado USB específico, cada una de las que presenta más información de forma incremental.

    **Correcto:**

    ![captura de pantalla de las notificaciones del estado de instalación ](images/mess-notif-image19.png)

    En este ejemplo, la asociación de un teclado USB da como resultado dos notificaciones completas.

### <a name="when-to-notify"></a>Cuándo se debe notificar

-   **Mostrar una notificación basada en su patrón de diseño:**



| Patrón              | Cuándo se debe notificar          |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Acción correcta<br/>            | Tras la finalización de una tarea asincrónica. Notifique a los usuarios las acciones correctas solo si es probable que estén esperando la finalización o después de errores recientes.<br/>                                             |
| Error de acción<br/>            | Tras un error de una tarea asincrónica.<br/>                                                                                                                                                                   |
| Evento del sistema no crítico<br/> | Cuando se produce un evento y el usuario está activo o la condición sigue existiendo. Si esto se debe a un problema, quite la notificación que se muestra actualmente inmediatamente una vez resuelto el problema.<br/> |
| Tarea de usuario opcional<br/>        | Cuando se determina la necesidad de realizar una tarea y el usuario está activo.<br/>                                                                                                                                   |
| FYI<br/>                       | Cuando se produce el evento de desencadenamiento.<br/>                                                                                                                                                                       |



 

-   Para el patrón de error de acción, si el problema puede corregirse a sí mismo en cuestión de segundos, retrase la notificación de **error durante un período de tiempo adecuado.** Si el problema se corrige a sí mismo, no informe de nada. Notifique solo después de que haya transcurrido el tiempo suficiente para que el error sea perceptible. Si informa demasiado pronto, lo más probable es que los usuarios no observen el problema notificado, pero observarán la notificación innecesaria.

**Incorrecto:**

![captura de pantalla de ninguna notificación de conexión de red ](images/mess-notif-image20.png)

Cuando inmediatamente va seguido de:

![captura de pantalla de la notificación de conexión correcta ](images/mess-notif-image21.png)

En este ejemplo, en Windows Vista la notificación de que no hay conectividad inalámbrica es prematura porque a menudo va seguida inmediatamente de una notificación de una buena conectividad.

-   Para los patrones de acción correcta y FYI, use la opción en tiempo real para que las notificaciones **obsoletas** no se ponen en cola cuando los usuarios ejecutan una aplicación de pantalla completa o no usan activamente su equipo.
-   En el caso del patrón de eventos del sistema no crítico, no cree la posibilidad de que se averan las notificaciones escalonando los eventos asociados a eventos conocidos, como el inicio de sesión **de usuario.** En su lugar, empate el evento a algún período de tiempo después del evento. Por ejemplo, podría recordar a los usuarios que registren el producto cinco minutos después del inicio de sesión del usuario.

### <a name="how-long-to-notify"></a>Cuánto tiempo se debe notificar

En Windows Vista y versiones posteriores, las notificaciones se muestran durante una duración fija de 9 segundos.

### <a name="how-often-to-notify"></a>Frecuencia con la que se debe notificar

-   **El número de veces que se muestra una notificación se basa en su patrón de diseño:**



| Patrón           | Frecuencia con la que se debe notificar  |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Acción correcta<br/>            | Una vez.<br/>                                                                                                            |
| Error de acción<br/>            | Una vez.<br/>                                                                                                            |
| Evento del sistema no crítico<br/> | Una vez cuando se produce el evento por primera vez. Si esto es el resultado de un problema que los usuarios deben resolver, vuelva a mostrar una vez al día.<br/> |
| Tarea de usuario opcional<br/>        | Una vez al día para un máximo de tres veces.<br/>                                                                         |
| FYI<br/>                       | Una vez.<br/>                                                                                                            |



 

-   **En el caso de las tareas opcionales del usuario, no intente hacer que los usuarios se suenen constantemente mostrando notificaciones.** Si la tarea es necesaria, muestre un cuadro de diálogo modal inmediatamente en lugar de usar notificaciones.

### <a name="notification-escalation"></a>Escalación de notificaciones

-   **No suponga que los usuarios verán las notificaciones.** Los usuarios no los verán cuando:
    -   Están inmersos en su trabajo.
    -   No están prestando atención.
    -   Están fuera de su equipo.
    -   Ejecutan una aplicación de pantalla completa.
    -   Su administrador ha desactivado todas las notificaciones de su equipo.
-   **Si los usuarios finalmente deben realizar algún tipo de acción, use** la extensión progresiva para mostrar una interfaz de usuario alternativa que los usuarios no puedan omitir.

### <a name="interaction"></a>Interacción

-   **Haga clic en las notificaciones cuando:**
    -   **Los usuarios deben realizar una acción.** Al hacer clic en la notificación, se mostrará una ventana en la que los usuarios puedan realizar la acción. Este enfoque es el preferido para los errores de acción y los patrones de diseño opcionales de tareas de usuario.
    -   **Es posible que los usuarios quieran ver más información.** Al hacer clic en la notificación se debe mostrar una ventana en la que los usuarios pueden ver información adicional.
-   **Mostrar siempre una ventana cuando los usuarios hacen clic para realizar una acción.** No haga clic en realizar una acción directamente.
-   **Al hacer clic para mostrar más información, siempre debería mostrarse más información.** No solo rehíba la información que ya está en la notificación.

### <a name="icons"></a>Iconos

-   **Para el patrón de error de acción, use el icono de error estándar.**
-   **Para los patrones de eventos del sistema no críticos, use el icono de advertencia estándar.**
-   **Para otros patrones, use** iconos que muestren objetos que se relacionan o sugieren el asunto, como un escudo para la seguridad o una batería de energía.
-   **Use iconos basados en su aplicación o personal de marca de empresa si los usuarios de destino los reconocerán y no hay ninguna alternativa mejor.**
-   Para la extensión progresiva, considere la posibilidad de usar iconos con una apariencia progresivamente más enfática a medida **que la situación sea más urgente.**
-   **No use el icono de información estándar.** Las notificaciones son información que no se puede decir.
-   **Considere la posibilidad de usar iconos grandes (32 x 32 píxeles) cuando:**
    -   Los usuarios comprenderán rápidamente el icono en lugar del texto.
    -   Los iconos grandes transmiten su significado de forma más clara y eficaz que los iconos estándar de 16 x 16 píxeles.
    -   El icono usa el [estilo De acrob.](vis-icons.md)

![captura de pantalla de la notificación "mensajes importantes" ](images/mess-notif-image22.png)

En este ejemplo, los usuarios pueden comprender rápidamente la naturaleza de la notificación con un vistazo al icono grande.

### <a name="notification-queuing"></a>Cola de notificaciones

**Nota:** Las notificaciones se ponen en cola cada vez que no se pueden mostrar inmediatamente, como cuando se muestra otra notificación, el usuario ejecuta una aplicación de pantalla completa o el usuario no usa activamente el equipo. Las notificaciones en tiempo real permanecen en la cola solo durante 60 segundos.

-   Para los patrones de acción correcta y **FYI, use** la opción en tiempo real para que la notificación no se pone en cola durante mucho tiempo. Estas notificaciones solo tienen valor cuando se pueden mostrar inmediatamente.
-   **Quite las notificaciones en cola cuando ya no sean pertinentes.**
-   **Desarrolladores:** Para ello, establezca la marca NIF \_ INFO en uFlags y establezca szInfo en una cadena vacía. No hay ningún daño en hacerlo si la notificación ya no está en la cola.

### <a name="system-integration"></a>Integración del sistema

-   Si la aplicación no siempre tiene [](winenv-notification.md) un icono en el área de notificación cuando se ejecuta, muestre un icono temporalmente durante la tarea asincrónica o el evento que provocó **la notificación.**

## <a name="text"></a>Texto

### <a name="title-text"></a>Texto del título

-   **Use texto de título que resuma brevemente la información más importante que necesita para comunicarse con los usuarios en un lenguaje claro, sin formato, conciso y específico.** Los usuarios deben ser capaces de comprender el propósito de la información de notificación rápidamente y con el mínimo esfuerzo.
-   **Use fragmentos de texto o oraciones completas sin finalizar la puntuación.**
-   **Use mayúsculas de estilo de frase.**
-   **No use más de 48 caracteres (en inglés) para adaptarse a la localización.** El título tiene una longitud máxima de 63 caracteres, pero debe permitir una expansión del 30 % cuando se traduzca el texto en inglés.

### <a name="body-text"></a>Texto del cuerpo

-   **Use texto corporal que proporciona una descripción (sin repetir la información del título) y, opcionalmente, que proporciona detalles específicos sobre la notificación y también permite a los usuarios saber qué acción está disponible.**
-   **Use oraciones completas con signos de puntuación finales.**
-   **Use mayúsculas de estilo de frase.**
-   **No use más de 200 caracteres (en inglés) para adaptarse a la localización.** El texto del cuerpo tiene una longitud máxima de 255 caracteres, pero debe permitir una expansión del 30 % cuando se traduzca el texto en inglés.
-   **Incluya información esencial en el texto del cuerpo, como nombres de objeto específicos.** (Ejemplos: nombres de usuario, nombres de archivo o direcciones URL). Los usuarios no deben tener que abrir otra ventana para encontrar dicha información.
-   **Coloque comillas dobles alrededor de los nombres de objeto.**
    -   **Excepción:** No use comillas cuando:
        -   El nombre del objeto siempre usa [mayúsculas y mayúsculas](glossary.md)de estilo de título, como con nombres de usuario.
        -   El nombre del objeto se desplaza con dos puntos (por ejemplo: Nombre de la impresora: Mi impresora).
        -   El nombre del objeto se puede determinar fácilmente a partir del contexto.
-   **Si debe truncar los nombres de objeto a un tamaño máximo fijo para dar cabida a la localización, use puntos suspensivos para indicar el truncamiento.**

    ![captura de pantalla del mensaje que contiene el nombre abreviado ](images/mess-notif-image23.png)

    En este ejemplo, un nombre de objeto se trunca mediante puntos suspensivos.

-   **Use las expresiones siguientes si la notificación puede actuar:**
    -   Si los usuarios pueden hacer clic en la notificación para realizar una acción:

        < breve descripción de la información esencial>

        <optional details>

        Haga clic en <do something> .

        ![captura de pantalla del mensaje: "Haga clic para ver el progreso" ](images/mess-notif-image24.png)

        En este ejemplo, los usuarios pueden hacer clic para realizar una acción.

    -   Si los usuarios pueden hacer clic en la notificación para ver más información:

        < breve descripción de la información esencial>

        <optional details>

        Haga clic para obtener más información.

        ![captura de pantalla del mensaje: haga clic para obtener más información. ](images/mess-notif-image25.png)

        En este ejemplo, los usuarios pueden hacer clic para obtener más información.

-   **No diga que el usuario "debe" realizar una acción en una notificación.** Las notificaciones son para información no crítica que los usuarios pueden omitir libremente. Si los usuarios realmente deben realizar una acción, no use notificaciones.
-   **Si los usuarios deben realizar una acción, aclare la importancia.**
-   En el caso del error de acción y los patrones de eventos del sistema no críticos, **describa los problemas en lenguaje sin formato.**

    **Incorrecto:**

    ![captura de pantalla de un mensaje largo y complejo ](images/mess-notif-image26.png)

    En este ejemplo, el problema se describe mediante un lenguaje muy técnico, pero no específico.

    **Correcto:**

    ![captura de pantalla de un mensaje claro y conciso ](images/mess-notif-image27.png)

    En este ejemplo, el problema se describe en lenguaje sin formato.

-   **Describa el evento de una manera que sea relevante para los usuarios de destino.** Una notificación es pertinente si existe una posibilidad razonable de que los usuarios realicen una tarea o cambien su comportamiento como resultado de la notificación. A menudo, esto se puede lograr mediante la descripción de notificaciones en términos de objetivos de usuario en lugar de problemas tecnológicos.

## <a name="documentation"></a>Documentación

Al hacer referencia a notificaciones:

-   Use el texto del título exacto, incluido su uso de mayúsculas.
-   Consulte el componente como una notificación, no como un globo o una alerta.
-   Para describir la interacción del usuario, use click.
-   Cuando sea posible, formatee el texto del título con texto en negrita. De lo contrario, coloque el título entre comillas solo si es necesario para evitar confusiones.

Ejemplo: cuando **aparezcan las actualizaciones críticas listas para instalar** la notificación, haga clic en la notificación para iniciar el proceso.

Al hacer referencia al área de notificación:

-   Consulte el área de notificación como el área de notificación, no la bandeja del sistema.

 

