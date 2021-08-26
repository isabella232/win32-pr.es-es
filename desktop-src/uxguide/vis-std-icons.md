---
title: Iconos estándar
description: Los iconos estándar son los iconos de error, advertencia, información e signo de interrogación que forman parte de Windows.
ms.assetid: 63b5c31d-5094-4299-b44b-35b2452ce706
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 74f5b70fb218606eb5f87cbad247c1c75a100f9c5e0f675bb6c075e559fd1a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936453"
---
# <a name="standard-icons"></a>Iconos estándar

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Los iconos estándar son los iconos de error, advertencia, información e signo de interrogación que forman parte de Windows.

![captura de pantalla de cuatro iconos estándar ](images/vis-std-icons-image1.png)

Iconos estándar de error, advertencia, información e signo de interrogación.

Los iconos estándar tienen estos significados:

-   **Icono de error.** La interfaz de usuario (UI) presenta un error o un problema que se ha producido.
-   **Icono de advertencia.** La interfaz de usuario presenta una condición que podría causar un problema en el futuro.
-   **Icono de información.** La interfaz de usuario presenta información útil.
-   **Icono de signo de interrogación.** La interfaz de usuario indica un punto de entrada de Ayuda.

Los iconos estándar son importantes porque están integrados en muchas interfaces de programación de aplicaciones (API) de Windows, como cuadros de diálogo [de](win-dialog-box.md) [tareas,](glossary.md)cuadros de mensaje, [globos](ctrl-balloons.md)y [notificaciones](mess-notif.md). También se usan normalmente en mensajes [locales y](glossary.md) barras [de estado.](ctrl-status-bars.md)

**Nota:** Las directrices relacionadas [con los](vis-icons.md) iconos se presentan en un artículo independiente.

## <a name="design-concepts"></a>Conceptos de diseño

Hay varios factores a la hora de elegir el icono estándar adecuado que, en parte, explica por qué se usan con tanta frecuencia de forma incorrecta. Los errores más comunes son:

-   Usar un icono de advertencia para errores menores. Las advertencias no son errores "atenuados".
-   Usar un icono estándar cuando sea mejor no usar ningún icono. No todos los mensajes necesitan un icono.
-   Alarming users by giving warnings for minor issues or presenting routine questions as warnings( Alarming users by giving warnings for minor issues or presenting routine questions as warnings. Esto hace que los programas parezcan propensos a riesgos y resta importancia a los problemas realmente importantes.

En el resto de esta sección se explica cómo pensar en los iconos estándar para evitar estos errores comunes.

### <a name="message-type-vs-severity"></a>Tipo de mensaje frente a gravedad

Elija iconos estándar basados en el tipo de mensaje, no en la gravedad del problema subyacente. Los tipos de mensaje son:

-   **Error.** Error o problema que se ha producido.
-   **Advertencia.** Una condición que podría causar un problema en el futuro.
-   **Información.** Información útil.

Por lo tanto, un mensaje de error podría tomar un icono de error, pero nunca un icono de advertencia. No use iconos de advertencia como una manera de "evitar" errores menores. Por lo tanto, a pesar de su diferencia de gravedad, "Tamaño de fuente incorrecto" es un error, mientras que "Continuar con esta operación hará que la casa se desenvía" es una advertencia.

### <a name="determining-the-appropriate-message-type"></a>Determinar el tipo de mensaje adecuado

Algunos problemas se pueden presentar como un error, una advertencia o información, dependiendo del énfasis y la expresión. Por ejemplo, supongamos que una página web no puede cargar un control ActiveX sin signo en función de la configuración Windows Internet Explorer actual:

-   **Error.** "Esta página no puede cargar un control ActiveX sin signo". (Se describe como un problema existente).
-   **Advertencia.** "Es posible que esta página no se comporte según lo previsto porque Windows Internet Explorer no está configurado para cargar controles de ActiveX sin signo". o "¿Permitir que esta página instale un control de ActiveX sin signo? Si lo hace desde orígenes que no son de confianza, puede dañar el equipo". (Ambos con frases como condiciones que pueden causar problemas futuros).
-   **Información.** "Ha configurado Windows Internet Explorer para bloquear controles de ActiveX sin signo". (Con frases como una declaración de hechos).

**Para determinar el tipo de mensaje adecuado, céntrate en el aspecto más importante del problema que los usuarios necesitan conocer o actuar.** Normalmente, si un problema impide que el usuario se ejecute, se presenta como un error. Si el usuario puede continuar, es una advertencia. Crear la [instrucción principal u](text-ui.md) otro texto correspondiente en función de ese foco y, a continuación, elija un icono (estándar o de otro tipo) que coincida con el texto. El texto de instrucción principal y los iconos siempre deben coincidir.

### <a name="severity"></a>severity

Aunque la gravedad no es una consideración a la hora de elegir entre los iconos de error, advertencia e información, la gravedad es un factor para determinar si se debe usar un icono **estándar.**

Los iconos funcionan mejor cuando se usan para comunicarse visualmente. (Tenga en cuenta que, por motivos de accesibilidad, esta comunicación visual siempre debe ser redundante con otro formato, como texto o sonido). Los usuarios deben poder saber de un vistazo la naturaleza de la información y las consecuencias de su respuesta, por lo que debemos diferenciar los errores críticos y las advertencias de sus homólogos normales. Los errores y advertencias críticos tienen estas características:

-   Implican la posible pérdida de uno o varios de los siguientes elementos:
    -   Un recurso valioso, como la pérdida de datos o la pérdida financiera.
    -   Integridad o acceso del sistema.
    -   Privacidad o control sobre la información confidencial.
    -   Tiempo del usuario (una cantidad significativa, como 30 segundos o más).
-   Tienen consecuencias inesperadas o no intencionadas.
-   Ahora requieren un control correcto, ya que los errores no se pueden corregir fácilmente e incluso pueden ser irreversibles.

Para distinguir errores y advertencias no críticos de los críticos, los mensajes no críticos normalmente se muestran sin un icono. De este modo, llama la atención sobre los mensajes críticos, hace que los mensajes críticos y no críticos sean visualmente distintos y sea coherente con el [Windows crítico.](text-style-tone.md)

No todos los mensajes necesitan un icono. Los iconos no son una manera de decorar los mensajes.

El siguiente es un buen ejemplo de una advertencia crítica porque cumple las características definidas anteriormente.

![captura de pantalla de una advertencia para hacer una copia de seguridad de los datos ](images/vis-std-icons-image2.png)

En este ejemplo, una advertencia crítica alerta a los usuarios de una posible pérdida de datos irreversible.

Sin embargo, el ejemplo siguiente no es crítico porque es probable que sea intencionado y sus resultados se desenconsonen fácilmente.

**Incorrecto:**

![captura de pantalla de un uso engañoso de un icono de advertencia ](images/vis-std-icons-image3.png)

En este ejemplo, esta [confirmación](mess-confirm.md) no es crítica porque es probable que sea intencionada y fácil de deshacer.

En una interfaz de usuario típica, la mayoría de los errores están relacionados con los errores de entrada del usuario. La mayoría de los errores de entrada del usuario no son críticos porque se corrigen fácilmente y los usuarios deben corregirlos antes de continuar. Además, llamar demasiada atención a los errores menores del usuario es contrario al Windows menor. Por lo tanto, los errores de entrada de usuario menores normalmente se muestran sin un icono de error. Para reforzar su naturaleza no crítica, nos referimos a ellos como problemas de entrada del usuario.

![captura de pantalla que informa a los usuarios de la entrada correcta ](images/vis-std-icons-image4.png)

En este ejemplo, este problema de entrada de usuario menor no es crítico, por lo que no necesita un icono cuando se presenta en un cuadro de diálogo.

### <a name="avoid-overwarning"></a>Evitar la sobreajuste

Nos hemos frustrado en Windows programas. El programa Windows programa tiene iconos de advertencia aparentemente en todas partes, advertencias sobre cosas que tienen poca importancia. En algunos programas, casi todas las preguntas se presentan como una advertencia. La sobreajuste hace que el uso de un programa se sienta como una actividad peligrosa y resta importancia a los problemas realmente importantes.

La única posibilidad de pérdida de datos por sí sola no es suficiente para llamar a un icono de advertencia. Además, los resultados no deseados deben ser inesperados o no deseados y no corregirse fácilmente. De lo contrario, casi cualquier pregunta con respuesta incorrecta podría interpretarse para dar lugar a la pérdida de datos de algún tipo y merecer un icono de advertencia.

Para centrar los iconos de advertencia en problemas realmente críticos:

-   Asegúrese de que el problema garantiza una mayor atención del usuario. [Las confirmaciones rutinarias](mess-confirm.md) y las preguntas no deben tener iconos de advertencia.
-   ¿Es probable que los usuarios se comporten de forma diferente como resultado del icono de advertencia? ¿Es probable que los usuarios consideren la decisión con más cuidado?

**Incorrecto:**

![captura de pantalla del icono de advertencia usado innecesariamente ](images/vis-std-icons-image5.png)

En este ejemplo, ¿es probable que los usuarios respondan a esta pregunta de forma diferente debido al icono de advertencia?

-   ¿Hay alguna acción importante que hacer o tomar? Las advertencias sin acciones simplemente hacen que los usuarios se sientan paranoicos.

**Incorrecto:**

![captura de pantalla del icono de advertencia que se usa con el recordatorio ](images/vis-std-icons-image6.png)

¿Por qué esta notificación es una advertencia? ¿Qué deben hacer los usuarios (además de preocuparse)?

### <a name="context"></a>Contexto

El contexto también es una consideración en el uso de iconos estándar porque el propio contexto comunica información. En concreto:

-   Aunque los cuadros de diálogo (incluidos los cuadros de diálogo de tareas y los cuadros de mensaje) y las notificaciones no necesitan iconos para errores no críticos, los errores locales siempre necesitan iconos de error. De lo contrario, estos comentarios no modales serían demasiado fáciles de pasar por alto.
-   Las advertencias locales siempre necesitan iconos de advertencia para distinguirlas del texto normal.
-   Los cuadros de diálogo, las notificaciones y los globos no necesitan iconos de información porque presentan información claramente. Por el contrario, los banners necesitan información de 16 x 16 píxeles u otros iconos, ya que estos comentarios no modales serían demasiado fáciles de pasar por alto.

Dado que el contexto es un factor significativo en el uso de iconos, las directrices de icono estándar de este artículo se dan en términos de su contexto.

### <a name="evaluating-standard-icon-appropriateness"></a>Evaluación de la adecuadaidad del icono estándar

Al evaluar el texto de la interfaz de usuario, lea también los iconos estándar. Lea iconos de error como "error!", iconos de advertencia como "advertencia, tenga mucho cuidado aquí" e iconos de información como "atención!". A continuación, siga leyendo el contexto restante, como la instrucción principal, el área de contenido y los botones de confirmación. Asegúrese de que el significado y el tono de cada icono estándar coincidan con el significado y el tono de su contexto. Si no es así, ha encontrado un problema.

**Si solo hace una cosa...**

Asegúrese de que el significado y el tono de cada icono estándar coincidan con el significado y el tono de su contexto. Si no coinciden, cambie o quite el icono.

## <a name="guidelines"></a>Directrices

**Nota:** Para las instrucciones siguientes, "in-place" significa en cualquier superficie de ventana normal, como dentro del área de contenido de un asistente, hoja de propiedades o página de elemento del panel de control.

### <a name="general"></a>General

-   Elija iconos estándar basados en su tipo de mensaje, no en la gravedad del problema subyacente:
    -   **Error.** Error o problema que se ha producido.
    -   **Advertencia.** Una condición que podría causar un problema en el futuro.
    -   **Información.** Información útil.
-   Si un problema se encuentra en distintos tipos de mensajes, céntrate en el aspecto más importante sobre el que los usuarios deben actuar.
-   Los iconos siempre deben coincidir con la instrucción principal u otro texto correspondiente.

**Correcto:**

![captura de pantalla del icono de error usado con texto de error ](images/vis-std-icons-image7.png)

**Incorrecto:**

![captura de pantalla del icono de advertencia usado con texto de error ](images/vis-std-icons-image8.png)

En el ejemplo incorrecto, el icono de advertencia estándar no coincide con la instrucción principal (que genera un error).

### <a name="icon-size"></a>Tamaño de icono

-   **Elija el tamaño del icono estándar en función del contexto:**
  



    | Contexto                         | Cuándo se usa                                                                                        |
    |--------------------------|-----------------------------------------------------------------------------------------|
    | Cuadros de diálogo<br/>  | Use 32 x 32 píxeles para los iconos del área de contenido; 16 x 16 píxeles para iconos de área de nota al pie.<br/> |
    | In situ<br/>      | Use 32 x 32 píxeles para las páginas de error; Iconos de 16 x 16 píxeles para todos los demás.<br/>           |
    | Notificaciones<br/> | Use iconos de 16 x 16 píxeles.<br/>                                                       |
    | Globos<br/>      | Use iconos de 16 x 16 píxeles.<br/>                                                       |
    | Banners<br/>       | Use iconos de 16 x 16 píxeles.<br/>                                                       |



 

### <a name="error-icons"></a>Iconos de error

-   **Use iconos de error solo cuando se haya producido un error o un problema:**



    | Contexto                           | Cuándo se usa                                                                                                                                                                                                                                             |
    |----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Cuadros de diálogo<br/>    | Use solo para errores críticos. (no use iconos estándar para errores no críticos). <br/> ![Captura de pantalla que muestra el icono de error usado con el mensaje de error ](images/vis-std-icons-image9.png)<br/>                                              |
    | Errores en el lugar<br/> | Use para todos los errores. <br/> ![captura de pantalla del icono de error usado con un mensaje de error.](images/vis-std-icons-image10.png)<br/>                                                                                                           |
    | Notificaciones<br/>   | Use solo para errores críticos. (para [errores de acción).](https://msdn.microsoft.com/library/windows/desktop/aa511497.aspx) <br/> ![Captura de pantalla que muestra un icono de error usado con un mensaje de error de notificación.](images/vis-std-icons-image11.png)<br/> |
    | Globos<br/>        | No lo use. Los globos no deben usarse para errores críticos y no necesitan iconos de error para errores no críticos.<br/>                                                                                                               |
    | Banners<br/>         | No lo use. Los banners no deben usarse para errores.<br/>                                                                                                                                                                                  |



 

-   Por lo general, los iconos de error no son necesarios para problemas de entrada de usuario no críticos. Sin embargo, los iconos son necesarios para los errores en contexto, porque de lo contrario, estos comentarios contextuales serían demasiado fáciles de pasar por alto.
-   **Para los diálogos de tareas, no use iconos de nota al pie de error.** Los iconos de error solo deben presentarse en el área de contenido.

### <a name="warning-icons"></a>Iconos de advertencia

-   **Use iconos de advertencia solo cuando una condición pueda causar un problema en el futuro:**



    | Contexto                             |  Cuándo se usa                                                                                                                                                                                      |
    |------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Cuadros de diálogo<br/>      | Use para todas las advertencias. <br/> ![advertencia de captura de pantalla del cambio de extensión de nombre de archivo ](images/vis-std-icons-image12.png)<br/>                                                   |
    | Advertencias locales<br/> | Use para identificar el texto como una advertencia. <br/> ![captura de pantalla de advertencia de que no hay suficiente espacio libre ](images/vis-std-icons-image13.png)<br/>                                    |
    | Notificaciones<br/>     | Use para todas las advertencias. (para [eventos del sistema no críticos).](glossary.md) <br/> ![captura de pantalla de la notificación de advertencia de batería baja ](images/vis-std-icons-image14.png)<br/> |
    | Globos<br/>          | Se usa para [condiciones especiales.](ctrl-balloons.md) <br/> ![captura de pantalla de la advertencia de globo de bloqueo de límites ](images/vis-std-icons-image15.png)<br/>                           |
    | Banners<br/>           | Use para llamar la atención sobre el banner. <br/> ![captura de pantalla del banner con la advertencia de que falta tpm ](images/vis-std-icons-image16.png)<br/>                                    |



 

-   **No use iconos de advertencia para "evitar" errores no críticos.** Los errores no son advertencias; en su lugar, se aplican las directrices del icono de error.
-   **Para los diálogos de preguntas, use iconos de advertencia solo para preguntas con consecuencias significativas.** No use iconos de advertencia para preguntas rutinarias.

**Correcto:**

![advertencia de captura de pantalla para no detener la restauración del sistema ](images/vis-std-icons-image17.png)

**Incorrecto:**

![captura de pantalla de advertencia sobre el descarte de recordatorios ](images/vis-std-icons-image18.png)

En el ejemplo incorrecto, se usa incorrectamente un icono de advertencia para una pregunta rutinaria.

-   **Para los diálogos de tareas, puede usar un icono de nota al pie de advertencia para alertar a los usuarios de consecuencias de riesgo.** Sin embargo, use un icono de advertencia en el área de contenido o en el área de nota al pie, pero no en ambos.

![advertencia de captura de pantalla de un archivo potencialmente no seguro ](images/vis-std-icons-image19.png)

En este ejemplo, se usa un escudo de seguridad amarillo en una nota al pie.

### <a name="information-icons"></a>Iconos de información

-   **Use iconos de información solo cuando el contexto no presente obviamente información:**



    | Contexto                         | Cuándo se usa                                                                                                                                                  |
    |--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
    | Cuadros de diálogo<br/>  | No lo use.<br/>                                                                                                                             |
    | In situ<br/>      | No lo use. En su lugar, use texto estático sin formato o un banner.<br/>                                                                           |
    | Notificaciones<br/> | No lo use.<br/>                                                                                                                             |
    | Globos<br/>      | No lo use.<br/>                                                                                                                             |
    | Banners<br/>       | use para llamar la atención sobre el banner. <br/> ![captura de pantalla del banner con información de configuración ](images/vis-std-icons-image20.png)<br/> |



 

-   Los iconos de información no son necesarios en los cuadros de diálogo, las notificaciones y los globos porque su contexto comunica lo suficiente que proporcionan información a los usuarios.
-   **Para los cuadros de diálogo de tareas, no use iconos de nota al pie de información.** Las notas al pie son suficientemente visibles y no significa que sean información.

### <a name="question-mark-icons"></a>Iconos de signo de interrogación

-   **Use el icono de signo de interrogación solo para los puntos de entrada de ayuda.** Para obtener más información, consulte las [directrices del punto de entrada de](winenv-help.md) ayuda.
-   **No use el icono de signo de interrogación para hacer preguntas.** De nuevo, use el icono de signo de interrogación solo para los puntos de entrada de ayuda. No es necesario hacer preguntas con el icono de signo de interrogación de todos modos, basta con presentar una instrucción principal como una pregunta.
-   **No reemplace habitualmente los iconos de signo de interrogación por iconos de advertencia.** Reemplace un icono de signo de interrogación por un icono de advertencia solo si la pregunta tiene consecuencias significativas. De lo contrario, no use ningún icono.

 

