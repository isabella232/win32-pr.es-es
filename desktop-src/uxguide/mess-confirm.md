---
title: Confirmaciones
description: Una confirmación es un cuadro de diálogo modal que pregunta si el usuario desea continuar con una acción.
ms.assetid: 086302cd-c8a1-479c-87be-580945e5d3e6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b979987daa4cf2c40308a0cda9c23b08b73f4795
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104558742"
---
# <a name="confirmations"></a>Confirmaciones

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Una confirmación es un cuadro de diálogo modal que pregunta si el usuario desea continuar con una acción.

![Captura de pantalla que muestra el Bloc de notas "¿desea guardar los cambios?" .](images/mess-confirm-image1.png)

Una confirmación típica.

Las confirmaciones tienen estas características esenciales:

-   Se muestran como el resultado directo de una acción iniciada por el usuario.
-   Comprueban que el usuario desea continuar con la acción.
-   Están formados por una pregunta simple y dos o más respuestas.

Las confirmaciones son más útiles cuando la acción requiere que el usuario realice una opción relevante y diferente que no se pueda realizar más adelante. Esta opción suele implicar algún elemento de riesgo que no es obvio para el usuario, pero el riesgo no es esencial para las confirmaciones. Estos elementos son necesarios para justificar la interrupción de la respuesta a un cuadro de diálogo modal.

Por el contrario, [los mensajes de advertencia](mess-warn.md) presentan una condición que puede provocar un problema en el futuro. Su característica fundamental es que implican un riesgo:

-   Implican la posible pérdida de uno o varios de los siguientes elementos:
    -   Un activo valioso, como la pérdida de datos o la pérdida financiera.
    -   Acceso al sistema o integridad.
    -   Privacidad o control sobre la información confidencial.
    -   Hora del usuario (una cantidad significativa, como 30 segundos o más).
-   Tienen consecuencias inesperadas o imprevistas.
-   Requieren un control correcto ahora porque los errores no se pueden corregir fácilmente e incluso pueden ser irreversibles.

Si una confirmación implica un riesgo, también puede considerarse una advertencia. Por lo tanto, también se aplican las directrices de mensajes de advertencia.

**Nota:** Las instrucciones relacionadas con los [cuadros de diálogo](win-dialog-box.md), [los mensajes de error](mess-error.md), el [diseño](vis-layout.md)y [los mensajes de advertencia](mess-warn.md) se presentan en artículos independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

Para decidirte, intenta responder a estas preguntas:

-   **¿Se pregunta al usuario si desea continuar con una acción que tiene dos o más respuestas?** Si no es así, el mensaje no es una confirmación.
-   **¿La interfaz de usuario presenta un error o un problema que se ha producido?** Si es así, use un [mensaje de error](mess-error.md) en su lugar.
-   **¿La acción requiere que el usuario elija una opción que no tenga un valor predeterminado adecuado?** Si es así, puede ser adecuada una confirmación.
-   **¿Existe algún diseño alternativo que elimine la necesidad de confirmación?** La necesidad de una confirmación suele indicar un error de diseño. A menudo, hay una alternativa de diseño mejor que no necesita una confirmación.
-   **¿El usuario está a punto de realizar una acción de riesgo?** Si es así, una confirmación es adecuada si la acción tiene consecuencias importantes o no se puede deshacer fácilmente.
-   **¿El usuario está a punto de abandonar una tarea?** Si es así, no confirme. Supongamos que los usuarios entienden las consecuencias de no completar una tarea.
-   **¿La acción tiene consecuencias de que los usuarios no sepan?** Si es así, puede ser adecuada una confirmación.
-   **Dado el contexto actual, ¿es probable que los usuarios realicen una acción por error?** Si es así, puede ser adecuada una confirmación.
-   **¿Los usuarios realizan la acción con frecuencia?** Si es así, considere un diseño alternativo. Las confirmaciones frecuentes son molestas y tienen poco valor, ya que los usuarios aprenden a responder sin pensar.
-   **¿La acción tiene implicaciones de seguridad?** Si es así, es posible que se requiera una confirmación incluso si las pruebas anteriores indican lo contrario.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="unnecessary-confirmations-are-annoying"></a>Las confirmaciones innecesarias son molestas

La primera confirmación de Windows se ha creado en alguna ocasión sin duda:

![captura de pantalla de ' ¿está seguro? ' Confirmación ](images/mess-confirm-image2.png)

La confirmación de molestia original.

Se trata de un inicio muy incorrecto. Si desea que los usuarios impongan su programa, solo tiene que rociar confirmaciones como esta. Para comprender por qué, considere el punto de vista del usuario. El usuario acaba de solicitar que realice una acción por la definición de una confirmación, de modo que, a menos que se haga clic en algún elemento o se presionara por accidente, por supuesto que el usuario desea continuar.

No solo son molestas las confirmaciones innecesarias, pero no son eficaces para proteger al usuario frente a errores. Los usuarios detectan rápidamente cuando un programa tiene confirmaciones innecesarias y su respuesta natural es descartarlos lo más rápido posible, a menudo sin leer. Por lo tanto, estas confirmaciones hacen poco más que agregar un paso adicional a estas tareas.

No utilice confirmaciones solo porque existe la posibilidad de que los usuarios cometan un error. **En su lugar, las confirmaciones son más eficaces cuando se utilizan para confirmar acciones que tienen consecuencias importantes o no deseadas.** Las confirmaciones correctas nunca tienen el estado obvio; deben comunicar algo que los usuarios tienen que tener en cuenta una buena razón para no continuar. Y solo se usan cuando una acción realmente los necesita, como pedir a los usuarios que guarden los cambios solo cuando se guarden los cambios. Al hacerlo, se exige la atención del usuario solo cuando está realmente justificado.

Para otros tipos de confirmaciones, a menudo hay una alternativa de diseño mejor que obligar a los usuarios a responder a una pregunta.

### <a name="consider-the-design-alternatives"></a>Considere las alternativas de diseño

Estas son algunas alternativas de diseño que eliminan la necesidad de confirmaciones rutinarias:

-   **Evitar errores.** Diseñe tareas para que los errores importantes resulten difíciles de realizar accidentalmente. Por ejemplo, separar físicamente los comandos destructivos de otros comandos y requerir varias acciones para completarse.
-   **Proporcionar deshacer.** Proporcionar la capacidad de revertir las acciones. Por ejemplo, la eliminación de un archivo en Microsoft Windows normalmente no requiere una confirmación porque los archivos eliminados se pueden recuperar de la papelera de reciclaje. Tenga en cuenta que si una acción es muy fácil de realizar, bastará con que los usuarios puedan rehacer la acción.
-   **Proporcione comentarios.** Haga obvios los resultados no deseados. Proporcionar el deshacer solo no es suficiente si los usuarios no se dan en el momento de cometer un error. Por ejemplo, el efecto de la manipulación directa (por ejemplo, una operación de arrastrar y colocar) siempre debe ser obvio.
-   **Asuma el resultado probable, pero facilite el cambio.** Si no está seguro de lo que los usuarios quieren, pero hay una opción más probable, segura y segura, supongamos que elige lo que ha ocurrido y que es fácil de cambiar mediante un menú contextual. Por ejemplo, Microsoft Word supone que los usuarios desean escribir palabras correctamente. Si reconoce una palabra mal escrita y sabe que la ortografía es correcta, Word realiza automáticamente la corrección, pero permite a los usuarios revertir.
-   **Elimine la opción por completo.** Si la elección no es importante, los usuarios simplemente no le interesan. Mejor [simplificar](/previous-versions//dn742474(v=vs.85)) el programa y eliminar la opción.

### <a name="make-confirmations-require-thought"></a>Confirmaciones que se deben considerar

Para que una confirmación tenga el valor, los usuarios deben comprender la razón de no continuar. A veces, el motivo es obvio, como cuando los usuarios cierran un documento con cambios que no se han guardado:

![Captura de pantalla que muestra una pintura "¿desea guardar los cambios?" "Hola mundo".](images/mess-confirm-image3.png)

En este ejemplo, el motivo de la confirmación es obvio.

En otras situaciones, la razón podría no ser tan obvia.

Al elegir las etiquetas de botón de confirmación para los cuadros de diálogo, las [directrices generales](win-dialog-box.md) son elegir las etiquetas que son respuestas específicas a la instrucción principal. Esto conduce a una toma de decisiones eficaz porque los usuarios tienen que leer una cantidad mínima de texto para continuar. Sin embargo, este objetivo de eficacia puede ser un producto para las confirmaciones. Considere este ejemplo:

**Incorrecto:**

![captura de pantalla de confirmación con el botón Desinstalar ](images/mess-confirm-image4.png)

En este ejemplo, se debe considerar la respuesta correcta.

Si presenta esta confirmación inmediatamente después de que el usuario haya dado el comando de desinstalación, es probable que la respuesta del usuario sea "evidentemente, deseo desinstalar". El usuario hará clic en desinstalar sin darle un segundo pensamiento.

En el caso de las confirmaciones, no queremos que los usuarios tomen decisiones emocionales y deprisas. Para animar a los usuarios a pensar en su respuesta, es necesario proporcionar una pequeña rugosidad de velocidad de toma de decisiones. Cuando es práctico, suele ser mejor hacerlo mediante los botones de confirmación con frases. Por ejemplo, podemos usar otro idioma para indicar que hay una razón para no continuar.

**Manera**

![captura de pantalla del botón "desinstalar de todas formas" ](images/mess-confirm-image5.png)

En este ejemplo, se agrega "de todos modos" a la etiqueta del botón de confirmación para indicar que la confirmación proporciona una razón para no continuar.

Si ese enfoque no es práctico, podemos usar botones de confirmación sí/no.

**También mejor:**

![captura de pantalla de confirmación con botones sí/no ](images/mess-confirm-image6.png)

En este ejemplo, el uso de botones de confirmación sí/no obliga a los usuarios a leer la instrucción principal al menos.

### <a name="provide-all-the-information"></a>Proporcionar toda la información

Si va a hacer una pregunta, debe proporcionar información suficiente para que los usuarios respondan a esa pregunta de forma inteligente. Considere el cuadro de diálogo confirmar reemplazo de archivo de Windows XP:

![captura de pantalla del cuadro de diálogo "confirmar reemplazo de archivo" ](images/mess-confirm-image7.png)

Cuadro de diálogo confirmar reemplazo de archivo de Windows XP.

¿Esta confirmación proporciona toda la información que los usuarios pueden necesitar para responder a la pregunta? Antes de responder, tenga en cuenta los escenarios de usuario más comunes:

-   Copie (o mueva) el otro archivo, reemplazando el existente.
-   Mantenga el archivo existente, sin copiar ni mover el otro archivo.
-   Conservar o copiar el archivo más reciente (escenario superior).
-   Mantenga el archivo existente o copie el otro archivo, en función de criterios como el contenido y el tamaño del archivo.
-   Mantenga el archivo existente y copie el otro archivo con un nombre diferente.
-   Cancele la operación si algo es incorrecto o inesperado.

Para lograr el escenario 1, los usuarios pueden hacer clic en sí y en escenario 2 haciendo clic en no. Pueden lograr el escenario 3 comparando las fechas del archivo y haciendo clic en el botón adecuado, pero observen cuánto se ha pensado para determinar el archivo más reciente y, a continuación, determinar el botón adecuado especialmente en lo que es probable que sea el escenario más común.

Los escenarios 4, 5 y 6 también son sorprendentemente difíciles. Los tamaños de archivo se redondean, por lo que, por ejemplo, no es posible determinar si estos archivos tienen el mismo tamaño o incluso si son el mismo archivo. Los iconos son para la aplicación que se usa para abrir el archivo, por lo que los usuarios tendrían que abrir los archivos para inspeccionar y comparar su contenido. Tener miniaturas del contenido del archivo sería mucho más útil para responder a la pregunta.

La confirmación de copia de archivos de Windows Vista hace un trabajo mucho mejor de controlar estos escenarios al proporcionar más información y agregar la opción para conservar ambos archivos:

![captura de pantalla del cuadro de diálogo "copiar archivo" ](images/mess-confirm-image8.png)

Confirmación de copia de archivo de Windows Vista.

### <a name="provide-specific-useful-information"></a>Proporcionar información específica y útil

Si va a hacer una pregunta, asegúrese de que los usuarios entienden la pregunta y las implicaciones de las respuestas alternativas. Tenga en cuenta esta confirmación de seguridad en Windows Internet Explorer:

![captura de pantalla de la confirmación con una pregunta imprecisa ](images/mess-confirm-image9.png)

Confirmación de seguridad impreciso.

Esta confirmación plantea una pregunta que los usuarios no pueden responder de manera inteligente. El usuario ha solicitado que se muestre una página en Windows Internet Explorer y este mensaje lo aconseja implícitamente a través de la redacción del texto y resaltando no como la opción predeterminada.

El problema de seguridad específico que la página plantea no es suficientemente explicado, por lo que el riesgo de continuar no está claro. ¿Qué información de la confirmación haría que el usuario hiciera clic en no? Debido a la imvagación del mensaje, no es probable que la confirmación desaconseja a los usuarios continuar, pero hará que se sientan incorrectos al hacerlo.

Para que esta confirmación sea útil, debe proporcionar más información específica que pueda hacer que el usuario decida no continuar. En general, para cada respuesta de una confirmación, tenga en cuenta los escenarios que lo requieren y asegúrese de que hay información suficiente para que los usuarios quieran elegirla. Proporcionar opciones, no dilemas.

### <a name="how-to-determine-if-a-confirmation-is-necessary"></a>Cómo determinar si es necesaria una confirmación

Pensar en los escenarios y la probabilidad de elegir cada respuesta sugiere una manera sistemática de determinar si es necesaria una confirmación. Si es probable que los usuarios seleccionen todas las respuestas, la confirmación es necesaria y útil. Sin embargo, si solo es probable que una respuesta sea (por ejemplo, el 98 por ciento del tiempo), la confirmación es claramente innecesaria y debe quitarse. Tenga en cuenta que las confirmaciones relacionadas con los problemas de seguridad, legales y de seguridad son posibles excepciones.

![captura de pantalla de "¿desea cambiar la configuración?" ](images/mess-confirm-image10.png)

¿Es necesaria esta confirmación? ¿Los usuarios seleccionarán alguna vez? Es posible pero muy improbable. Esta confirmación se debe quitar.

**Si solo hace tres cosas...**

1. Asegúrese de que la confirmación es realmente necesaria. Debe haber un motivo legítimo y claro que no continúe y una posibilidad de que los usuarios a veces no lo sean.

2. Si el motivo de la confirmación no es evidente de inmediato, elija botones de confirmación que animen a los usuarios a pensar en su respuesta. Por lo general, esto se hace mediante la formulación de la confirmación como una pregunta sí o no, y proporcionando respuestas por completo o de sí/no.

3. Tenga en cuenta todos los escenarios y proporcione la información necesaria para responder a la pregunta de forma inteligente.

## <a name="usage-patterns"></a>Patrones de uso

Las confirmaciones tienen varios patrones de uso:



|                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Confirmaciones rutinarias**<br/> Confirme que el usuario desea continuar con una acción de rutina y bajo riesgo. <br/>                                              | Estas confirmaciones suelen ser frases "¿está seguro...?" y, a menudo, tienen una casilla no volver a mostrar este mensaje para minimizar su molestia. <br/> ![captura de pantalla de "mueva la carpeta a la papelera de reciclaje" ](images/mess-confirm-image11.png)<br/> ![captura de pantalla de "no mostrar mensaje de nuevo" ](images/mess-confirm-image12.png)<br/> Ejemplos de confirmaciones rutinarias.<br/> **Nota:** Este patrón normalmente no es necesario y se debe evitar.<br/>                                                                                                                                                                                                                                                                                        |
| **Confirmaciones de acción de riesgo**<br/> Confirme que el usuario desea continuar con una acción que tiene cierto riesgo y no se puede deshacer fácilmente. <br/>            | Dado que tienen riesgo, estas confirmaciones suelen tener un icono de advertencia. <br/> ![Captura de pantalla que muestra un ejemplo de confirmación de formato de volumen.](images/mess-confirm-image13.png)<br/> ![Captura de pantalla que muestra un ejemplo de confirmación de eliminación permanente.](images/mess-confirm-image14.png)<br/> Ejemplos de confirmaciones de acción de riesgo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Confirmaciones de consecuencias no deseadas**<br/> Confirme que el usuario desea continuar con una acción que tenga consecuencias inesperadas o imprevistas. <br/> | Además de formular una pregunta, estas confirmaciones señalan las consecuencias no deseadas. Dado que tienen consecuencias no deseadas, estas confirmaciones suelen tener un icono de advertencia. <br/> ![captura de pantalla de "cerrar todas las pestañas?" confirmación ](images/mess-confirm-image15.png)<br/> ![captura de pantalla de "cancelar instalación?" confirmación ](images/mess-confirm-image16.png)<br/> ejemplos de confirmaciones de consecuencias no deseadas.<br/> sin embargo, este patrón requiere que las consecuencias sean realmente no deseadas. <br/> **errónea**<br/> ![captura de pantalla de ' desactivar registrador de claves ' confirmación ](images/mess-confirm-image17.png)<br/> Las consecuencias están pensadas aquí, por lo que se trata de una confirmación rutinaria.<br/> |
| **Aclaraciones**<br/> aclarar cómo desea que el usuario continúe con una acción que tenga consecuencias potencialmente ambiguas o inesperadas. <br/>             | Las operaciones de arrastrar y colocar pueden dar lugar a aclaraciones si el efecto de la operación se puede malinterpretar. <br/> ![captura de pantalla de "cambiar solo esta repetición?"](images/mess-confirm-image18.png)<br/> ![captura de pantalla de "guardar siempre al salir?" confirmación ](images/mess-confirm-image19.png)<br/> Ejemplos de aclaraciones.<br/> **Nota:** Este patrón debe evitarse porque es mejor diseñar acciones sin consecuencias ambiguas y asumir el resultado más probable. <br/>                                                                                                                                                                                                                                     |
| **Confirmaciones de seguridad**<br/> Confirme que el usuario desea continuar con una acción con las consecuencias de seguridad. <br/>                                   | ![captura de pantalla de "¿desea ejecutar este software?" ](images/mess-confirm-image20.png)<br/> ![captura de pantalla de "recordar contraseña?" Confirmación ](images/mess-confirm-image21.png)<br/> Ejemplos de confirmaciones de seguridad.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Confirmaciones de proUlterior**<br/> proporcionar información sobre una acción, pero presentarla como una confirmación. <br/>                                       | Aunque estos cuadros de diálogo se presentan como confirmaciones, su objetivo real es la educación de los usuarios o la publicidad de las características. <br/> ![captura de pantalla de ¿desea esta barra de herramientas en la barra de tareas? ](images/mess-confirm-image22.png)<br/> Un ejemplo de una confirmación de ulterior.<br/> **Nota:** Este patrón no se recomienda porque normalmente hay una alternativa mejor y más directa. Por ejemplo, las [animaciones](vis-animations.md) son una manera mejor de mostrar la relación entre causa y efecto. <br/>                                                                                                                                                                                                                                     |



 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Use la confirmación "Guardar cambios" solo cuando haya cambios significativos.** No confirme los cambios que no haya realizado directamente el usuario, como el cambio de formato automático del documento.

**Incorrecto:**

![Captura de pantalla que muestra un Microsoft Office Outlook ' ¿desea guardar los cambios? ' .](images/mess-confirm-image23.png)

Este ejemplo es incorrecto cuando se usa para un documento o correo electrónico vacío que no ha cambiado el usuario.

### <a name="icons"></a>Iconos

-   Las confirmaciones no usan iconos de la barra de título.
-   **El icono del área de contenido para una confirmación se basa en su modelo de diseño:**



    | Patrón                                                | Icono                                                                                                                                             |
    |--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
    | Confirmaciones rutinarias <br/>                | Sin icono. <br/>                                                                                                                         |
    | Confirmaciones de acción de riesgo <br/>           | Icono de advertencia. <br/>                                                                                                                    |
    | Confirmaciones de consecuencias no deseadas <br/> | Use un icono de advertencia si hay riesgo, el icono de la característica si está disponible; en caso contrario, no hay ningún icono. <br/>                                          |
    | Aclaraciones <br/>                       | Si la confirmación implica un documento, use la miniatura del documento; de lo contrario, use el icono de característica si está disponible o ningún icono. <br/> |
    | Confirmaciones de seguridad <br/>               | Icono de advertencia. <br/>                                                                                                                    |
    | Confirmaciones de proUlterior <br/>        | Sin icono. <br/>                                                                                                                         |



 

-   **No use iconos de advertencia para preguntas rutinarias.** De este modo, se contrarresta el [tono de promoción de ventanas](text-style-tone.md) y hace que el uso del programa se parezca a una actividad peligrosa. Supongamos que los usuarios entienden las consecuencias de cancelar una tarea antes de que finalice.

**Incorrecto:**

![captura de pantalla de "¿desea finalizar el tutorial?" ](images/mess-confirm-image24.png)

En este ejemplo, se usa un icono de advertencia para formular una pregunta de rutina.

### <a name="commit-buttons"></a>Botones de confirmación

-   **Use respuestas específicas a la instrucción principal si la razón de la confirmación es obvia o se puede hacer por sí misma.**

![captura de pantalla de "¿desea guardar los cambios?" ](images/mess-confirm-image25.png)

En este ejemplo, el motivo de la confirmación es obvio, por lo que guardar y no guardar el trabajo.

-   **De lo contrario, use los botones sí y no para las respuestas de confirmación.** De este modo, los usuarios tienen la confirmación de que hay que pensar antes de responder. No use nunca aceptar y Cancelar para las confirmaciones.

**Correcto:**

![captura de pantalla de "¿desea desinstalar los archivos de soporte técnico?" ](images/mess-confirm-image26.png)

En este ejemplo, el uso de botones de confirmación sí/no obliga a los usuarios a leer la instrucción principal al menos.

**Incorrecto:**

![captura de pantalla de "cancelar la reserva?" ](images/mess-confirm-image27.png)

En este ejemplo, el uso de aceptar/cancelar es confuso.

-   **Para cerrar un programa o reiniciar Windows, use respuestas específicas a la instrucción principal.** Para evitar que se entienda incomprensiblemente, no utilice Close o yes/no para este fin.

**Correcto:**

![captura de pantalla del botón reiniciar Windows ahora](images/mess-confirm-image28.png)

**Incorrecto:**

![captura de pantalla del botón sí](images/mess-confirm-image29.png)

En el ejemplo incorrecto, sí se usa para reiniciar Windows.

### <a name="command-links"></a>Vínculos de comandos

-   **En el patrón aclaraciones, considere la posibilidad de usar vínculos de comandos para desactivar las alternativas.**

**Aceptable:**

![captura de pantalla de "cambiar una o todas las repeticiones?" ](images/mess-confirm-image30.png)

**Manera**

![captura de pantalla de la misma pregunta con vínculos de comandos ](images/mess-confirm-image31.png)

En el mejor ejemplo, los vínculos de comandos hacen que las alternativas resulten claras.

-   **Presente primero los vínculos de comandos que se usan con más frecuencia.** El orden resultante debe seguir aproximadamente la probabilidad de uso, pero también tiene un flujo lógico.
-   Si un vínculo de comando requiere una explicación más detallada, **proporcione una explicación complementaria.** Las explicaciones complementarias describen el motivo por el que los usuarios pueden elegir la opción o lo que sucede si se elige la opción.

Para obtener más instrucciones y ejemplos, vea [vínculos de comandos](ctrl-command-links.md).

### <a name="default-values"></a>Valores predeterminados

-   **La respuesta predeterminada para una confirmación se basa en su modelo de diseño:**



    | Patrón                                                 | Respuesta predeterminada                                                                                |
    |--------------------------------------------------|---------------------------------------------------------------------------------|
    | Confirmaciones rutinarias <br/>                | Avanza. <br/>                                                            |
    | Confirmaciones de acción de riesgo <br/>           | No continúe (o la opción segura). <br/>                                 |
    | Confirmaciones de consecuencias no deseadas <br/> | Si las consecuencias son significativas, no continúe; de lo contrario, continúe. <br/> |
    | Aclaraciones <br/>                       | La respuesta más probable. <br/>                                           |
    | Confirmaciones de seguridad <br/>               | No continúe. <br/>                                                      |
    | Confirmaciones de proUlterior <br/>        | Avanza. <br/>                                                            |



 

### <a name="dont-show-this-message-again"></a>No volver a mostrar este mensaje

-   **Use esta opción solo para los patrones de confirmación de la rutina y ulterior.** En el caso de los demás patrones, si la información es necesaria, siempre debe mostrarse.
-   **No proporcione esta opción para justificar la visualización de una confirmación innecesaria.** En su lugar, solo tiene que deshacerse de la confirmación.

**Incorrecto:**

![captura de pantalla de "descartar estos recordatorios?" ](images/mess-confirm-image32.png)

**Todavía incorrecto:**

![captura de pantalla de "no mostrar mensaje de nuevo"](images/mess-confirm-image33.png)

En estos ejemplos, al agregar una opción no volver a mostrar este mensaje, no se corrige una confirmación innecesaria.

Para obtener más instrucciones, consulte [cuadros de diálogo](win-dialog-box.md).

### <a name="bulk-operations"></a>Operaciones masivas

-   En el caso de las confirmaciones que se aplican a las operaciones masivas, proporcione una opción para aplicar la confirmación a toda la operación.

![captura de pantalla de "hacer esto para todos los elementos?" casilla ](images/mess-confirm-image34.png)

Este ejemplo tiene una opción para operaciones masivas.

-   Eliminar o posponer las confirmaciones en una operación masiva.

**Incorrecto:**

![captura de pantalla del cuadro de diálogo ' Confirmar eliminación de archivo ' ](images/mess-confirm-image35.png)

En este ejemplo, el explorador de Windows en Windows XP confirma cada archivo de solo lectura durante un movimiento de archivos masivo. Mejor solo para copiar los archivos de solo lectura sin preguntar o posponer el control de estos archivos y presentar la confirmación al final de la tarea.

### <a name="progressive-disclosure"></a>Muestra progresiva

-   **Si tiene que incluir información avanzada en un mensaje de confirmación, debe revelarla mediante botones de divulgación progresiva (por ejemplo, "Mostrar detalles").** De este modo, se simplifica la confirmación del uso típico. No oculte la información necesaria porque es posible que los usuarios no la encuentren.
-   **No use "Mostrar detalles" a menos que realmente haya más detalles.** No solo tiene que volver a indicar la información existente en un formato diferente.

Para obtener instrucciones de etiquetado, vea [divulgación progresiva](ctrl-progressive-disclosure-controls.md).

### <a name="user-account-control"></a>Control de cuentas de usuario

-   **No use la interfaz de usuario de elevación de control de cuentas de usuario (UAC) como sustituto de una confirmación.** Si una acción necesita una confirmación, use un cuadro de diálogo independiente. Durante la [interfaz](winenv-uac.md)de usuario de elevación, los usuarios deben centrarse en si iniciaron la tarea y si el programa es de confianza.
-   **Mostrar la confirmación antes de la interfaz de usuario de elevación.** Al hacerlo, se eliminan las elevaciones innecesarias.

## <a name="text"></a>Texto

### <a name="general"></a>General

-   **Quite el texto redundante.** Busque texto redundante en títulos, instrucciones principales, instrucciones adicionales, áreas de contenido, vínculos de comandos y botones de confirmación. Por lo general, deje texto completo en las instrucciones y los controles interactivos, y quite cualquier redundancia de los demás lugares.
-   **No use "WARNING" o "PRECAUCIÓN" en el texto.** Si los usuarios deben continuar con precaución, indíquelo mediante un icono de advertencia.

**Incorrecto:**

![captura de pantalla de la confirmación de formato de volumen ](images/mess-confirm-image36.png)

En este ejemplo, el término "WARNING" no es necesario.

### <a name="titles"></a>Títulos

-   **Use el título para identificar el comando o la característica de donde procede la confirmación. Excepciones**
    -   Si hay muchos comandos diferentes que muestran una confirmación, considere la posibilidad de usar el nombre del programa en su lugar.
    -   Si ese título sería redundante o confuso con la instrucción principal, use en su lugar el nombre del programa.

Sin embargo, si la confirmación proviene de una tarea de ejecución prolongada y puede aparecer correctamente después de que se inicie la tarea, use siempre el comando o la característica para identificar claramente el contexto.

-   **No use el título para explicar qué hacer en el cuadro de diálogo** que es el propósito de la instrucción principal.
-   Si agrega claridad, inicie el título con la palabra confirmar.
-   **En el caso de las confirmaciones de acción de riesgo, puede Agregar el nombre del objeto implicado para un énfasis adicional.**

![captura de pantalla del título del cuadro de diálogo "formato de unidad f" ](images/mess-confirm-image13.png)

En este ejemplo, la unidad a la que se va a dar formato se incluye en el título.

-   Usar [mayúsculas y minúsculas de estilo de título](glossary.md), sin puntuación final.

### <a name="main-instructions"></a>Instrucciones principales

-   **La instrucción principal para una confirmación se basa en su modelo de diseño:**



    | Patrón                                                 | Instrucción principal                                                                                                                                                                                                                                                                                                                                                                                                          |
    |--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Confirmaciones de consecuencias no deseadas <br/> | indique la consecuencia imprevista.<br/> **excepción:** si una pregunta pregunta si el usuario desea continuar, implica claramente las consecuencias imprevistas, formule la pregunta en su lugar. <br/> ![captura de pantalla de "cerrar todas las pestañas?" confirmación ](images/mess-confirm-image15.png)<br/> En este ejemplo, pedir al usuario que continúe suficientemente las consecuencias de la acción.<br/> |
    | Todos los demás <br/>                           | Formule una sola pregunta para determinar si el usuario desea continuar. <br/>                                                                                                                                                                                                                                                                                                                              |



 

-   **Sea conciso usar una sola oración completa.** Quite la instrucción principal de la información esencial. Si debe explicar algo más, use una instrucción complementaria.
-   **Ser específico si hay objetos implicados, asigne sus nombres completos.**
-   **Usar frases positivas.** La formulación positiva es más fácil de entender para los usuarios.

**Correcto:**

¿Desea habilitar el uso compartido de archivos e impresoras?

**Incorrecto:**

¿Desea deshabilitar el uso compartido de archivos e impresoras?

Sin embargo, la formulación debe coincidir con el comando asociado, aunque el comando tenga frase negativa. por lo tanto, por ejemplo, use Disable para confirmar un comando DISABLE.

-   Aunque no hay reglas estrictas para la formulación, **estas frases de confirmación comunes tienen la configuración indicada:**



    | Frase                                                            | Connotaciones                                                            |
    |-------------------------------------------------------------|-------------------------------------------------------------|
    | ¿Está seguro de que desea \[ realizar una acción \] ? <br/> | Confirmar el resultado directo de una solicitud de usuario. <br/> |
    | ¿Desea \[ realizar una acción \] ? <br/>           | Confirmar un efecto secundario de una solicitud de usuario. <br/>     |
    | ¿Desea \[ seleccionar un resultado \] ? <br/>          | Se necesita una aclaración. <br/>                           |
    | \[¿Realizar una acción \] ? <br/>                          | No hay ninguna anotación. <br/>                                 |



 

-   En el caso de las confirmaciones de acción de riesgo, use el término de forma permanente para indicar que una acción no se puede deshacer.

![captura de pantalla de confirmación de eliminación permanente ](images/mess-confirm-image37.png)

En este ejemplo, "permanentemente" indica que la acción no se puede deshacer.

-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).

### <a name="supplemental-instructions"></a>Instrucciones complementarias

-   **La instrucción complementaria para una confirmación se basa en su modelo de diseño:**

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td><strong>Patrón</strong><br/></td>
    <td><strong>Instrucción complementaria</strong><br/></td>
    </tr>
    <tr class="even">
    <td>Confirmaciones de consecuencias no deseadas <br/></td>
    <td>Formule una sola pregunta para determinar si el usuario desea continuar. <br/></td>
    </tr>
    <tr class="odd">
    <td>Todos los demás <br/></td>
    <td>Explique las razones no obvias por las que el usuario podría no querer continuar. Estos son algunos de los motivos: <br/>
    <ul>
    <li>Posible pérdida de uno o varios de los siguientes elementos: <ul>
    <li>Un activo valioso, como la pérdida de datos o la pérdida financiera.</li>
    <li>Acceso al sistema o integridad.</li>
    <li>Privacidad o control sobre la información confidencial.</li>
    </ul></li>
    <li>Acciones irreversibles.</li>
    </ul></td>
    </tr>
    </tbody>
    </table>

    

     

-   **No repita la instrucción principal con un texto ligeramente diferente.** En su lugar, omita la instrucción complementaria Si no hay más que agregar.
-   En **el caso de las confirmaciones de consecuencias no deseadas, considere la posibilidad de usar el término de todos modos para indicar de forma concisa que hay un motivo que no debe continuar** en caso de que el usuario haya desvisto la instrucción principal. Para obtener más información, vea conceptos de diseño.
-   Use frases completas, uso de mayúsculas y minúsculas y puntuación final.

## <a name="documentation"></a>Documentación

Al hacer referencia a las confirmaciones:

-   Haga referencia a una confirmación por su título si el título es específico de la confirmación (es decir, no el nombre del programa); de lo contrario, haga referencia a él mediante su instrucción principal.
-   Si es necesario, puede hacer referencia a un cuadro de diálogo de confirmación como mensaje.
-   Use el texto exacto, incluido el uso de mayúsculas.
-   Siempre que sea posible, dé formato al texto con negrita. De lo contrario, coloque el texto entre comillas solo si es necesario para evitar confusiones.

Ejemplo: en el mensaje de **copia de archivo** , haga clic en el archivo más reciente.

