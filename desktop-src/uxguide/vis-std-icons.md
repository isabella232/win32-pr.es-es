---
title: Iconos estándar
description: Los iconos estándar son los iconos de error, ADVERTENCIA, información y signo de interrogación que forman parte de Windows.
ms.assetid: 63b5c31d-5094-4299-b44b-35b2452ce706
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 69085f4c527db8431b5e33f0dba4668d43d1c669
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104361810"
---
# <a name="standard-icons"></a>Iconos estándar

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Los iconos estándar son los iconos de error, ADVERTENCIA, información y signo de interrogación que forman parte de Windows.

![captura de pantalla de cuatro iconos estándar ](images/vis-std-icons-image1.png)

Los iconos de error estándar, ADVERTENCIA, información y signo de interrogación.

Los iconos estándar tienen estos significados:

-   **Icono de error.** La interfaz de usuario (UI) presenta un error o un problema que se ha producido.
-   **Icono de advertencia.** La interfaz de usuario presenta una condición que puede provocar un problema en el futuro.
-   **Icono de información.** La interfaz de usuario presenta información útil.
-   **Icono de signo de interrogación.** La interfaz de usuario indica un punto de entrada de ayuda.

Los iconos estándar son significativos porque están integrados en muchas interfaces de programación de aplicaciones (API) de Windows, como cuadros de [diálogo de tareas](win-dialog-box.md), [cuadros de mensaje](glossary.md), [globos](ctrl-balloons.md)y [notificaciones](mess-notif.md). También se usan normalmente en [mensajes en contexto](glossary.md) y barras de [Estado](ctrl-status-bars.md).

**Nota:** Las instrucciones relacionadas con los [iconos](vis-icons.md) se presentan en un artículo independiente.

## <a name="design-concepts"></a>Conceptos de diseño

Hay varios factores para elegir el icono estándar adecuado, que en parte explica por qué se usan de forma incorrecta. Los errores más comunes son:

-   Uso de un icono de advertencia para errores menores. Las advertencias no son errores "suavizados".
-   Usar un icono estándar cuando sea mejor no usar ningún icono. No todos los mensajes necesitan un icono.
-   Avisar a los usuarios al otorgar advertencias para problemas menores o presentar preguntas rutinarias como advertencias. Esto hace que los programas parezcan propensos a peligros y se destraen de problemas realmente importantes.

En el resto de esta sección se explica cómo pensar en los iconos estándar para evitar estos errores comunes.

### <a name="message-type-vs-severity"></a>Tipo de mensaje frente a gravedad

Elija iconos estándar en función del tipo de mensaje, no la gravedad del problema subyacente. Los tipos de mensaje son:

-   **Error.** Un error o un problema que se ha producido.
-   **Atención.** Una condición que puede provocar un problema en el futuro.
-   **Informaciones.** Información útil.

Por lo tanto, un mensaje de error puede tomar un icono de error, pero nunca un icono de advertencia. No use iconos de advertencia como una manera de "suavizar" los errores menores. Por tanto, a pesar de su diferencia en cuanto a gravedad, el "tamaño de fuente incorrecto" es un error, mientras que "continuar con esta operación establecerá la casa en el fuego" es una advertencia.

### <a name="determining-the-appropriate-message-type"></a>Determinar el tipo de mensaje adecuado

Algunos problemas se pueden presentar como un error, una advertencia o información, según el énfasis y la formulación. Por ejemplo, supongamos que una página web no puede cargar un control ActiveX sin firmar basado en la configuración actual de Windows Internet Explorer:

-   **Error.** "Esta página no puede cargar un control ActiveX sin firmar". (Frase como un problema existente).
-   **Atención.** "Es posible que esta página no se comporte de la manera esperada porque Windows Internet Explorer no está configurado para cargar controles ActiveX sin firmar". o "¿desea permitir que esta página Instale un control ActiveX sin firmar? Hacerlo desde orígenes que no son de confianza puede dañar el equipo ". (Ambas frases como condiciones que pueden causar problemas en el futuro).
-   **Informaciones.** "Ha configurado Windows Internet Explorer para bloquear los controles ActiveX sin firmar". (Frase como instrucción de hecho).

**Para determinar el tipo de mensaje adecuado, céntrese en el aspecto más importante del problema que los usuarios necesitan conocer o actuar sobre ellos.** Normalmente, si un problema impide que el usuario continúe, se presenta como un error; Si el usuario puede continuar, es una advertencia. Cree la [instrucción principal](text-ui.md) u otro texto correspondiente en función de ese foco y, a continuación, elija un icono (estándar o de otro tipo) que coincida con el texto. Los iconos y el texto de la instrucción principal siempre deben coincidir.

### <a name="severity"></a>Severity

Aunque la gravedad no es una consideración a la hora de elegir entre los iconos de error, advertencia e información, **la gravedad es un factor que se debe considerar para determinar si se debe usar un icono estándar.**

Los iconos funcionan mejor cuando se usan para comunicarse visualmente. (Tenga en cuenta que, por motivos de accesibilidad, esta comunicación visual siempre debe ser redundante con otro formato, como texto o sonido). Los usuarios deben poder saber de un vistazo la naturaleza de la información y las consecuencias de su respuesta, por lo que debemos diferenciar los errores críticos y las advertencias de sus homólogos normales. Los errores y advertencias críticos tienen estas características:

-   Implican la posible pérdida de uno o varios de los siguientes elementos:
    -   Un activo valioso, como la pérdida de datos o la pérdida financiera.
    -   Acceso al sistema o integridad.
    -   Privacidad o control sobre la información confidencial.
    -   Hora del usuario (una cantidad significativa, como 30 segundos o más).
-   Tienen consecuencias inesperadas o imprevistas.
-   Ahora requieren un control correcto, ya que los errores no se pueden corregir fácilmente e incluso pueden ser irreversibles.

Para distinguir los errores no críticos y las advertencias de los críticos, los mensajes no críticos se muestran normalmente sin un icono. Al hacerlo, se trata la atención a los mensajes críticos, se hace que los mensajes críticos y no críticos sean visualmente distintos y es coherente con el [tono de Windows](text-style-tone.md).

No todos los mensajes necesitan un icono. Los iconos no son una manera de decorar los mensajes.

A continuación se presenta un buen ejemplo de una advertencia crítica porque cumple con las características definidas previamente.

![captura de pantalla de una advertencia para realizar una copia de seguridad de los datos ](images/vis-std-icons-image2.png)

En este ejemplo, una advertencia crítica alerta a los usuarios de posibles pérdidas de datos irreversibles.

Sin embargo, el siguiente ejemplo no es crítico porque es probable que sea intencionado y que sus resultados se deshagan fácilmente.

**Incorrecto:**

![captura de pantalla de un uso engañoso de un icono de advertencia ](images/vis-std-icons-image3.png)

En este ejemplo, esta [confirmación](mess-confirm.md) no es crítica porque es probable que sea intencional y fácil de deshacer.

En una interfaz de usuario típica, la mayoría de los errores se relacionan con los errores de entrada del usuario. La mayoría de los errores de entrada del usuario no son críticos porque se corrigen fácilmente y los usuarios deben corregirlos antes de continuar. Además, el dibujo de mucha atención a errores menores de los usuarios es contrario al tono de Windows. Por lo tanto, los errores de entrada de usuario menores se muestran normalmente sin un icono de error. Para reforzar su naturaleza no crítica, nos referimos a ellos como problemas de entrada del usuario.

![captura de pantalla que informa a los usuarios de la entrada correcta ](images/vis-std-icons-image4.png)

En este ejemplo, este problema de entrada de usuario secundario no es crítico, por lo que no necesita un icono cuando se presenta en un cuadro de diálogo.

### <a name="avoid-overwarning"></a>Evitar las sobreadvertencias

Se recomienda que se avise en los programas de Windows. El programa Windows típico tiene iconos de advertencia aparentemente en todas partes; Advertencia sobre cosas que tienen poca importancia. En algunos programas, casi todas las preguntas se presentan como una advertencia. La sobreadvertencia hace que el uso de un programa se parezca a una actividad peligrosa y se reste de problemas realmente significativos.

La mera posibilidad de pérdida de datos solo es insuficiente para llamar a un icono de advertencia. Además, los resultados no deseados deberían ser inesperados o no deseados y no se pueden corregir fácilmente. De lo contrario, se podría interpretar cualquier pregunta incorrectamente respondida para que se produzca una pérdida de datos de algún tipo y se pueda usar un icono de advertencia.

Para centrar iconos de advertencia en problemas realmente críticos:

-   Asegúrese de que el problema garantiza una mayor atención al usuario. Las [confirmaciones y preguntas rutinarias](mess-confirm.md) no deben tener iconos de advertencia.
-   ¿Es probable que los usuarios se comporten de manera diferente como resultado del icono de advertencia? ¿Es probable que los usuarios tengan en cuenta la decisión más detenidamente?

**Incorrecto:**

![captura de pantalla del icono de advertencia usada innecesariamente ](images/vis-std-icons-image5.png)

En este ejemplo, ¿es probable que los usuarios respondan a esta pregunta de forma diferente debido al icono de advertencia?

-   ¿Hay alguna acción importante que hacer o tomar una decisión? Las advertencias sin acciones solo hacen que los usuarios sientan Paranoid.

**Incorrecto:**

![captura de pantalla del icono de advertencia usado con el aviso ](images/vis-std-icons-image6.png)

¿Por qué esta notificación es una advertencia? ¿Qué se supone que deben hacer los usuarios (junto a preocuparse)?

### <a name="context"></a>Context

El contexto también es una consideración en el uso de iconos estándar, ya que el propio contexto comunica información. De manera específica:

-   Mientras que los cuadros de diálogo (incluidos los cuadros de diálogo de tareas y de mensajes) y las notificaciones no necesitan iconos para los errores no críticos, los errores en contexto siempre necesitan iconos de error. De lo contrario, esta información no modal sería demasiado fácil de pasar por alto.
-   Las advertencias en contexto siempre necesitan iconos de advertencia para distinguirlas del texto normal.
-   Los cuadros de diálogo, las notificaciones y los globos no necesitan iconos de información porque están presentando información de forma clara. Por el contrario, los banners necesitan información de 16x16 píxeles u otros iconos, ya que es demasiado fácil pasar por alto estos comentarios no modales.

Dado que el contexto es un factor importante en el uso de iconos, las directrices de iconos estándar de este artículo se indican en términos de contexto.

### <a name="evaluating-standard-icon-appropriateness"></a>Evaluación de la adecuadaidad del icono estándar

Al evaluar el texto de la interfaz de usuario, lea también los iconos estándar. Lea los iconos de error como "error!", los iconos de advertencia como "ADVERTENCIA, tenga muy cuidado aquí" e iconos de información como "atención". Después, siga leyendo el contexto restante, como la instrucción principal, el área de contenido y los botones de confirmación. Asegúrese de que el significado y el tono de cada icono estándar coinciden con el significado y el tono de su contexto. Si no es así, ha encontrado un problema.

**Si solo hace algo...**

Asegúrese de que el significado y el tono de cada icono estándar coinciden con el significado y el tono de su contexto. Si no coinciden, cambie o quite el icono.

## <a name="guidelines"></a>Directrices

**Nota:** Para las siguientes directrices, "en contexto" significa en cualquier superficie de ventana normal, como en el área de contenido de un asistente, hoja de propiedades o página de elementos del panel de control.

### <a name="general"></a>General

-   Elija iconos estándar en función del tipo de mensaje, no la gravedad del problema subyacente:
    -   **Error.** Un error o un problema que se ha producido.
    -   **Atención.** Una condición que puede provocar un problema en el futuro.
    -   **Informaciones.** Información útil.
-   Si un problema se refiere a distintos tipos de mensajes, céntrese en el aspecto más importante en el que los usuarios necesitan actuar.
-   Los iconos siempre deben coincidir con la instrucción principal u otro texto correspondiente.

**Correcto:**

![captura de pantalla del icono de error que se usa con el texto de error ](images/vis-std-icons-image7.png)

**Incorrecto:**

![captura de pantalla del icono de advertencia que se usa con el texto de error ](images/vis-std-icons-image8.png)

En el ejemplo incorrecto, el icono de advertencia estándar no coincide con la instrucción principal (que genera un error).

### <a name="icon-size"></a>Tamaño de icono

-   **Elija el tamaño de icono estándar en función del contexto:**
  



    | Context                         | Cuándo se usa                                                                                        |
    |--------------------------|-----------------------------------------------------------------------------------------|
    | Cuadros de diálogo<br/>  | Use 32x32 píxeles para los iconos del área de contenido; 16x16 píxeles para los iconos del área de la nota al pie.<br/> |
    | En contexto<br/>      | Usar píxel de 32x32 en las páginas de error; iconos de 16x16 píxeles para todos los demás.<br/>           |
    | Notificaciones<br/> | Usar iconos de 16x16 píxeles.<br/>                                                       |
    | Globos<br/>      | Usar iconos de 16x16 píxeles.<br/>                                                       |
    | Banners<br/>       | Usar iconos de 16x16 píxeles.<br/>                                                       |



 

### <a name="error-icons"></a>Iconos de error

-   **Usar iconos de error solo cuando se ha producido un error o un problema:**



    | Context                           | Cuándo se usa                                                                                                                                                                                                                                             |
    |----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Cuadros de diálogo<br/>    | Se usa solo para errores críticos. (no use iconos estándar para errores no críticos). <br/> ![Captura de pantalla que muestra el icono de error usado con el mensaje de error ](images/vis-std-icons-image9.png)<br/>                                              |
    | Errores en contexto<br/> | Se utiliza para todos los errores. <br/> ![captura de pantalla del icono de error que se usa con un mensaje de error.](images/vis-std-icons-image10.png)<br/>                                                                                                           |
    | Notificaciones<br/>   | Se usa solo para errores críticos. (para los [errores de acción](https://msdn.microsoft.com/library/windows/desktop/aa511497.aspx)). <br/> ![Captura de pantalla que muestra un icono de error que se usa con un mensaje de error de notificación.](images/vis-std-icons-image11.png)<br/> |
    | Globos<br/>        | No use. Los globos no se deben usar para errores críticos y no necesitan iconos de error para los errores no críticos.<br/>                                                                                                               |
    | Banners<br/>         | No use. Los banners no se deben usar en los errores.<br/>                                                                                                                                                                                  |



 

-   Por lo general, los iconos de error no son necesarios para los problemas de entradas de usuario no críticas. Sin embargo, los iconos son necesarios para los errores en contexto, ya que, de lo contrario, los comentarios contextuales serían demasiado fáciles de pasar por alto.
-   **En el caso de los cuadros de diálogo de tarea, no use iconos de nota al pie de página** Los iconos de error solo se deben presentar en el área de contenido.

### <a name="warning-icons"></a>Iconos de advertencia

-   **Usar iconos de advertencia solo cuando una condición puede producir un problema en el futuro:**



    | Context                             |  Cuándo se usa                                                                                                                                                                                      |
    |------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Cuadros de diálogo<br/>      | Se usa para todas las advertencias. <br/> ![ADVERTENCIA de captura de pantalla de cambio de extensión de nombre de archivo ](images/vis-std-icons-image12.png)<br/>                                                   |
    | Advertencias en contexto<br/> | Utilice para identificar el texto como una advertencia. <br/> ![captura de pantalla de advertencia de espacio libre insuficiente ](images/vis-std-icons-image13.png)<br/>                                    |
    | Notificaciones<br/>     | Se usa para todas las advertencias. (para [eventos del sistema no críticos](glossary.md)). <br/> ![captura de pantalla de la notificación de advertencia de batería baja ](images/vis-std-icons-image14.png)<br/> |
    | Globos<br/>          | Se usa para [condiciones especiales](ctrl-balloons.md). <br/> ![captura de pantalla de la advertencia de globo de Bloq Mayús activado ](images/vis-std-icons-image15.png)<br/>                           |
    | Banners<br/>           | Use para atraer la atención al banner. <br/> ![captura de pantalla de banner con ADVERTENCIA de que falta TPM ](images/vis-std-icons-image16.png)<br/>                                    |



 

-   **No use iconos de advertencia para "suavizar" los errores no críticos.** Los errores no son advertencias aplican en su lugar las instrucciones del icono de error.
-   **En el caso de los cuadros de diálogo de preguntas, use iconos de advertencia solo para preguntas con consecuencias significativas.** No use iconos de advertencia para preguntas rutinarias.

**Correcto:**

![ADVERTENCIA de captura de pantalla para detener la restauración del sistema ](images/vis-std-icons-image17.png)

**Incorrecto:**

![captura de pantalla de advertencia sobre cómo descartar recordatorios ](images/vis-std-icons-image18.png)

En el ejemplo incorrecto, un icono de advertencia se usa incorrectamente para una pregunta de rutina.

-   **En el caso de los cuadros de diálogo de tarea, puede usar un icono de nota al pie de página para alertar a los usuarios de consecuencias peligrosas.** Sin embargo, puede usar un icono de advertencia en el área de contenido o en el área de la nota al pie, pero no en ambos.

![ADVERTENCIA de captura de pantalla de un archivo potencialmente no seguro ](images/vis-std-icons-image19.png)

En este ejemplo, se usa un escudo de seguridad amarillo en una nota al pie.

### <a name="information-icons"></a>Iconos de información

-   **Usar iconos de información solo cuando el contexto no presenta información obviamente:**



    | Context                         | Cuándo se usa                                                                                                                                                  |
    |--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
    | Cuadros de diálogo<br/>  | No use.<br/>                                                                                                                             |
    | En contexto<br/>      | No use. En su lugar, use texto estático sin formato o un banner.<br/>                                                                           |
    | Notificaciones<br/> | No use.<br/>                                                                                                                             |
    | Globos<br/>      | No use.<br/>                                                                                                                             |
    | Banners<br/>       | Use para atraer la atención al banner. <br/> ![captura de pantalla de banner con información de configuración ](images/vis-std-icons-image20.png)<br/> |



 

-   Los iconos de información no son necesarios en los cuadros de diálogo, las notificaciones y los globos porque su contexto comunica lo suficiente como para proporcionar información a los usuarios.
-   **En el caso de los cuadros de diálogo de tarea, no use iconos de notas de la información.** Las notas a pie de la vista son lo suficientemente visibles y salen sin indicar que son información.

### <a name="question-mark-icons"></a>Iconos de signo de interrogación

-   **Use el icono de signo de interrogación solo para los puntos de entrada de la ayuda.** Para obtener más información, consulte las instrucciones del [punto de entrada](winenv-help.md) de la ayuda.
-   **No use el icono de signo de interrogación para formular preguntas.** De nuevo, use el icono de signo de interrogación solo para los puntos de entrada de la ayuda. No es necesario hacer preguntas mediante el icono de signo de interrogación, ya que basta con presentar una instrucción principal como una pregunta.
-   **No reemplace de forma rutinaria los iconos de signo de interrogación por iconos de advertencia.** Reemplace un icono de signo de interrogación por un icono de advertencia solo si la pregunta tiene consecuencias significativas. En caso contrario, no use ningún icono.

 

