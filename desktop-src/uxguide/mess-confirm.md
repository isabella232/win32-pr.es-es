---
title: Confirmaciones
description: Una confirmación es un cuadro de diálogo modal que pregunta si el usuario desea continuar con una acción.
ms.assetid: 086302cd-c8a1-479c-87be-580945e5d3e6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 22fc59cee7ebd02ae5e97b5a4db9549848267120
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987468"
---
# <a name="confirmations"></a>Confirmaciones

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Una confirmación es un cuadro de diálogo modal que pregunta si el usuario desea continuar con una acción.

![Captura de pantalla que muestra Bloc de notas "do you want to save changes?" (¿Desea guardar los cambios?). .](images/mess-confirm-image1.png)

Confirmación típica.

Las confirmaciones tienen estas características esenciales:

-   Se muestran como el resultado directo de una acción iniciada por el usuario.
-   Comprueba que el usuario desea continuar con la acción.
-   Constan de una pregunta simple y dos o más respuestas.

Las confirmaciones son más útiles cuando la acción requiere que el usuario realice una elección pertinente y distinta que no se pueda realizar más adelante. Esa opción suele implicar algún elemento de riesgo que no es obvio para el usuario, pero el riesgo no es esencial para las confirmaciones. Estos elementos son necesarios para justificar la interrupción de la respuesta a un diálogo modal.

Por el contrario, [los mensajes de](mess-warn.md) advertencia presentan una condición que podría causar un problema en el futuro. Su característica fundamental es que implican riesgos:

-   Implican la posible pérdida de uno o varios de los siguientes elementos:
    -   Un recurso valioso, como la pérdida de datos o la pérdida financiera.
    -   Integridad o acceso del sistema.
    -   Privacidad o control sobre la información confidencial.
    -   Tiempo del usuario (una cantidad significativa, como 30 segundos o más).
-   Tienen consecuencias inesperadas o no intencionadas.
-   Ahora requieren un control correcto porque los errores no se pueden corregir fácilmente e incluso pueden ser irreversibles.

Si una confirmación implica un riesgo, también se puede considerar una advertencia. Por lo tanto, también se aplican las directrices del mensaje de advertencia.

**Nota:** Las instrucciones relacionadas con [los cuadros de diálogo,](win-dialog-box.md) [los mensajes de error,](mess-error.md) [el diseño](vis-layout.md)y los mensajes de advertencia [se](mess-warn.md) presentan en artículos independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

Para decidirte, intenta responder a estas preguntas:

-   **¿Se está haciendo una pregunta al usuario para continuar con una acción que tiene dos o más respuestas?** Si no es así, el mensaje no es una confirmación.
-   **¿La interfaz de usuario presenta un error o un problema que se ha producido?** Si es así, use un [mensaje de error](mess-error.md) en su lugar.
-   **¿Requiere el usuario continuar con la acción para tomar una decisión que no tenga un valor predeterminado adecuado?** Si es así, puede ser adecuada una confirmación.
-   **¿Hay un diseño alternativo que elimine la necesidad de la confirmación?** La necesidad de una confirmación a veces indica un error de diseño. A menudo hay una mejor alternativa de diseño que no necesita confirmación.
-   **¿El usuario está a punto de realizar una acción de riesgo?** Si es así, es adecuada una confirmación si la acción tiene consecuencias significativas o no se puede deshacer fácilmente.
-   **¿El usuario está a punto de abandonar una tarea?** Si es así, no lo confirme. Suponga que los usuarios entienden las consecuencias de no completar una tarea.
-   **¿La acción tiene consecuencias que los usuarios podrían no tener en cuenta?** Si es así, puede ser adecuada una confirmación.
-   **Dado el contexto actual, ¿es probable que los usuarios realicen una acción en caso de error?** Si es así, puede ser adecuada una confirmación.
-   **¿Los usuarios realizan la acción con frecuencia?** Si es así, considere un diseño alternativo. Las confirmaciones frecuentes son pesadas y tienen poco valor porque los usuarios aprenden a responder sin pensar.
-   **¿La acción tiene implicaciones de seguridad?** Si es así, puede ser necesaria una confirmación aunque las pruebas anteriores indiquen lo contrario.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="unnecessary-confirmations-are-annoying"></a>Las confirmaciones innecesarias son insoportables

La primera Windows confirmación creada de forma indiscutible tenía el siguiente aspecto:

![captura de pantalla de '¿está seguro?' Confirmación ](images/mess-confirm-image2.png)

Confirmación de la insoportable confirmación original.

Ha sido un inicio muy malo. Si quiere que los usuarios odien el programa, simplemente invote confirmaciones como esta en todo momento. Para entender por qué, tenga en cuenta el punto de vista del usuario. El usuario acaba de solicitar que realice una acción mediante la definición de una confirmación, por lo que, a menos que se haya hecho clic o se haya presionado algo accidentalmente, por supuesto, el usuario quiere continuar.

No solo son pesadas las confirmaciones innecesarias, sino que no son eficaces para proteger al usuario de errores. Los usuarios detectan rápidamente cuándo un programa tiene confirmaciones innecesarias y su respuesta natural es descartarlas lo antes posible, a menudo sin leer. Por lo tanto, estas confirmaciones hacen poco más que agregar un paso adicional a estas tareas.

No use confirmaciones solo porque existe la posibilidad de que los usuarios cometen un error. **En su lugar, las confirmaciones son más eficaces cuando se usan para confirmar acciones que tienen consecuencias significativas o no intencionadas.** Las buenas confirmaciones nunca den lo obvio; deben comunicar algo que los usuarios deben tener en cuenta de una buena razón para no continuar. Y solo se usan cuando una acción realmente los necesita, como pedir a los usuarios que guarden los cambios solo cuando haya cambios que merece la pena guardar. Si lo hace, se requiere la atención del usuario solo cuando realmente está garantizado.

Para otros tipos de confirmaciones, a menudo hay una alternativa de diseño mejor que obligar a los usuarios a responder a una pregunta.

### <a name="consider-the-design-alternatives"></a>Consideración de las alternativas de diseño

Estas son algunas alternativas de diseño que eliminan la necesidad de confirmaciones rutinarias:

-   **Evitar errores.** Diseñe tareas para que los errores significativos sean difíciles de realizar accidentalmente. Por ejemplo, separe físicamente los comandos destructivos de otros comandos y requiera que se completen varias acciones.
-   **Proporcione deshacer.** Proporcionar la capacidad de revertir acciones. Por ejemplo, la eliminación de un archivo en Microsoft Windows normalmente no requiere una confirmación porque los archivos eliminados se pueden recuperar de la papelera de reciclaje. Tenga en cuenta que si una acción es muy fácil de realizar, basta con que los usuarios vuelvan a realizar la acción.
-   **Proporcionar comentarios.** Hacer que los resultados no deseados resulten obvios. Proporcionar deshacer por sí solo no es suficiente si los usuarios no se dan cuenta cuando cometen un error. Por ejemplo, el efecto de la manipulación directa (como una operación de arrastrar y colocar) siempre debe ser obvio.
-   **Asuma el resultado probable, pero haga que sea fácil cambiar.** Si no está seguro de lo que quieren los usuarios, pero hay una opción probable, segura y segura, asuma esa opción, aclare lo que ha ocurrido y haga que sea fácil cambiar mediante un menú contextual. Por ejemplo, Microsoft Word supone que los usuarios quieren escribir las palabras correctamente. Si reconoce una palabra mal escrita y conoce la ortografía probablemente correcta, Word realiza automáticamente la corrección, pero permite a los usuarios revertir.
-   **Elimine la elección por completo.** Si la elección no es importante, a los usuarios no les importará. Mejor simplificar [el](/previous-versions//dn742474(v=vs.85)) programa y eliminar la elección.

### <a name="make-confirmations-require-thought"></a>Hacer confirmaciones requiere reflexión

Para que una confirmación tenga valor, los usuarios deben comprender el motivo para no continuar. A veces, el motivo es obvio, como cuando los usuarios cierran un documento con cambios que no se han guardado:

![Captura de pantalla que muestra Paint "Do you want to save changes?" (¿Desea guardar los cambios?) "Hola mundo".](images/mess-confirm-image3.png)

En este ejemplo, el motivo de la confirmación es obvio.

En otras situaciones, el motivo podría no ser tan obvio.

Al elegir etiquetas de botón de confirmación para los cuadros de diálogo, las [directrices generales](win-dialog-box.md) son elegir etiquetas que sean respuestas específicas a la instrucción principal. Esto conduce a una toma de decisiones eficaz porque los usuarios tienen que leer una cantidad mínima de texto para continuar. Sin embargo, este objetivo de eficiencia puede ser contraproducente para las confirmaciones. Considere este ejemplo:

**Incorrecto:**

![captura de pantalla de confirmación con el botón desinstalar ](images/mess-confirm-image4.png)

En este ejemplo, la respuesta correcta requiere reflexión.

Si presenta esta confirmación inmediatamente después de que el usuario haya dado el comando Desinstalar, es probable que la respuesta del usuario sea "Por supuesto que quiero desinstalar". El usuario hará clic en Desinstalar sin darle una segunda idea.

En el caso de las confirmaciones, no queremos que los usuarios tomenten decisiones emocionales. Para animar a los usuarios a pensar en su respuesta, es necesario proporcionar un pequeño pico de velocidad de toma de decisiones. Cuando sea práctico, normalmente es mejor hacerlo mediante expresiones cuidadosas de botones de confirmación. Por ejemplo, podemos usar lenguaje adicional para indicar que hay una razón para no continuar.

**Mejor:**

![captura de pantalla del botón "Desinstalar de todos modos" ](images/mess-confirm-image5.png)

En este ejemplo, se agrega "de todos modos" a la etiqueta del botón de confirmación para indicar que la confirmación da una razón para no continuar.

Si ese enfoque no es práctico, podemos usar botones de confirmación Sí/No.

**También mejor:**

![captura de pantalla de confirmación con botones sí/no ](images/mess-confirm-image6.png)

En este ejemplo, el uso de botones de confirmación Sí/No obliga a los usuarios a leer al menos la instrucción principal.

### <a name="provide-all-the-information"></a>Proporcionar toda la información

Si va a hacer una pregunta, debe proporcionar información suficiente para que los usuarios la respondan de forma inteligente. Considere el cuadro de diálogo Confirmar reemplazo de archivo Windows XP:

![captura de pantalla del cuadro de diálogo "Confirmar reemplazo de archivo" ](images/mess-confirm-image7.png)

Cuadro Windows cuadro de diálogo Reemplazar archivo de confirmación de XP.

¿Esta confirmación proporciona toda la información que los usuarios pueden necesitar para responder a la pregunta? Antes de responder, tenga en cuenta los escenarios de usuario más comunes:

-   Copie (o mueva) el otro archivo, reemplazando el existente.
-   Mantenga el archivo existente, sin copiar ni mover el otro archivo.
-   Mantenga o copie el archivo más reciente (escenario superior).
-   Mantenga el archivo existente o copie el otro archivo, en función de criterios como el tamaño y el contenido del archivo.
-   Mantenga el archivo existente y copie el otro archivo con un nombre diferente.
-   Cancele la operación si algo es incorrecto o inesperado.

Los usuarios pueden lograr el escenario 1 haciendo clic en Sí y en el escenario 2 haciendo clic en No. Pueden lograr el escenario 3 comparando las fechas del archivo y haciendo clic en el botón adecuado, pero observen cuánto se necesita para determinar el archivo más reciente y, a continuación, determinar el botón adecuado, especialmente para lo que es probable que sea el escenario más común.

Los escenarios 4, 5 y 6 también son sorprendentemente difíciles. Los tamaños de archivo se redondea, por lo que, por ejemplo, es imposible determinar si estos archivos tienen el mismo tamaño o incluso si son del mismo archivo. Los iconos son para la aplicación que se usa para abrir el archivo, por lo que los usuarios tendrían que abrir los archivos para inspeccionar y comparar su contenido. Tener miniaturas del contenido del archivo sería mucho más útil para responder a la pregunta.

La confirmación copiar archivo de Windows Vista realiza un trabajo mucho mejor para controlar estos escenarios proporcionando más información y agregando la opción para mantener ambos archivos:

![captura de pantalla del cuadro de diálogo "Copiar archivo" ](images/mess-confirm-image8.png)

Confirmación Windows Vista Copy File.

### <a name="provide-specific-useful-information"></a>Proporcionar información específica y útil

Si va a hacer una pregunta, asegúrese de que los usuarios entiendan la pregunta y las implicaciones de las respuestas alternativas. Tenga en cuenta esta Windows Internet Explorer de seguridad:

![captura de pantalla de confirmación con una pregunta imprecisa ](images/mess-confirm-image9.png)

Confirmación de seguridad imprecisa.

Esta confirmación hace una pregunta que los usuarios posiblemente no puedan responder de forma inteligente. El usuario ha solicitado que Windows Internet Explorer una página y este mensaje le aconseja no hacerlo implícitamente a través de la redacción del texto y resaltando No como opción predeterminada.

El problema de seguridad específico que plantea la página no se explica lo suficiente, por lo que el riesgo de continuar no está claro. ¿Qué información de la confirmación haría que el usuario haga clic alguna vez en No? Debido a la imprecisidad del mensaje, es probable que la confirmación no desaconseja que los usuarios continúen, pero les hará sentir mal al hacerlo.

Para que esta confirmación sea útil, debe proporcionar más información específica que pueda hacer que el usuario decida no continuar. En general, para cada respuesta de una confirmación, tenga en cuenta los escenarios que la requieren y asegúrese de que hay suficiente información proporcionada para que los usuarios quieran elegirla. Proporcione opciones, no susiciones.

### <a name="how-to-determine-if-a-confirmation-is-necessary"></a>Cómo determinar si es necesaria una confirmación

Pensar en los escenarios y la probabilidad de elegir cada respuesta sugiere una manera sistemática de determinar si es necesaria una confirmación. Si es probable que los usuarios seleccionen todas las respuestas, la confirmación es necesaria y útil. Sin embargo, si es probable que solo una respuesta (por ejemplo, el 98 % del tiempo), la confirmación es claramente innecesaria y debe quitarse. Tenga en cuenta que las confirmaciones relacionadas con problemas de seguridad, legales y de seguridad son posibles excepciones.

![captura de pantalla de '¿Quiere cambiar la configuración?' ](images/mess-confirm-image10.png)

¿Es necesaria esta confirmación? ¿Los usuarios seleccionarán alguna vez No? Es posible, pero muy improbable. Esta confirmación debe quitarse.

**Si solo hace tres cosas...**

1. Asegúrese de que la confirmación es realmente necesaria. Debe haber una razón legítima y clara para no continuar y una posibilidad de que a veces los usuarios no lo haga.

2. Si el motivo de la confirmación no es obvio inmediatamente, elija botones de confirmación que animan a los usuarios a pensar en su respuesta. Normalmente, esto se hace mediante la expresión de la confirmación como una pregunta sí o ninguna y proporcionando respuestas completamente autoexplicativas o Sí/No.

3. Tenga en cuenta todos los escenarios y proporcione la información necesaria para responder a la pregunta de forma inteligente.

## <a name="usage-patterns"></a>Patrones de uso

Las confirmaciones tienen varios patrones de uso:



|   Uso                                                                                                                                                                    |    Ejemplo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Confirmaciones rutinarias**<br/> confirme que el usuario desea continuar con una acción rutinaria de bajo riesgo. <br/>                                              | Estas confirmaciones suelen estar frases como "¿está seguro...?" y a menudo tienen una casilla no mostrar este mensaje de nuevo para minimizar su molestia. <br/> ![captura de pantalla de '¿Mover carpeta a papelera de reciclaje?' ](images/mess-confirm-image11.png)<br/> ![captura de pantalla de "No volver a mostrar el mensaje" ](images/mess-confirm-image12.png)<br/> Ejemplos de confirmaciones rutinarias.<br/> **Nota:** Este patrón normalmente no es necesario y debe evitarse.<br/>                                                                                                                                                                                                                                                                                        |
| **Confirmaciones de acción de riesgo**<br/> confirme que el usuario desea continuar con una acción que tiene algún riesgo y no se puede deshacer fácilmente. <br/>            | Dado que tienen riesgo, estas confirmaciones suelen tener un icono de advertencia. <br/> ![Captura de pantalla que muestra un ejemplo de confirmación de formato de volumen.](images/mess-confirm-image13.png)<br/> ![Captura de pantalla que muestra un ejemplo de confirmación de eliminación permanente.](images/mess-confirm-image14.png)<br/> Ejemplos de confirmaciones de acciones de riesgo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Confirmaciones de consecuencias no deseadas**<br/> confirme que el usuario desea continuar con una acción que tenga consecuencias inesperadas o no intencionadas. <br/> | Además de hacer una pregunta, estas confirmaciones señalan las consecuencias no deseadas. dado que tienen consecuencias no intencionadas, estas confirmaciones suelen tener un icono de advertencia. <br/> ![captura de pantalla de '¿Cerrar todas las pestañas?' Confirmación ](images/mess-confirm-image15.png)<br/> ![captura de pantalla de '¿Cancelar instalación?' Confirmación ](images/mess-confirm-image16.png)<br/> ejemplos de confirmaciones de consecuencias no deseadas.<br/> sin embargo, este patrón requiere que las consecuencias no sean realmente intencionadas. <br/> **Incorrecta:**<br/> ![captura de pantalla de '¿Desactivar el registrador de claves?' Confirmación ](images/mess-confirm-image17.png)<br/> Las consecuencias están pensadas aquí, por lo que se trata de una confirmación rutinaria.<br/> |
| **Aclaraciones**<br/> aclarar cómo el usuario desea continuar con una acción que tiene consecuencias potencialmente ambiguas o inesperadas. <br/>             | Las operaciones de arrastrar y colocar pueden dar lugar a aclaraciones si se puede interpretar mal el efecto de la operación. <br/> ![captura de pantalla de "cambiar solo esta repetición?".](images/mess-confirm-image18.png)<br/> ![captura de pantalla de "siempre guardar al salir". Confirmación ](images/mess-confirm-image19.png)<br/> Ejemplos de aclaraciones.<br/> **Nota:** Este patrón debe evitarse porque es mejor diseñar acciones sin consecuencias ambiguas y asumir el resultado más probable deseado. <br/>                                                                                                                                                                                                                                     |
| **Confirmaciones de seguridad**<br/> confirme que el usuario desea continuar con una acción con consecuencias de seguridad. <br/>                                   | ![captura de pantalla de "do you want to run this software?" (¿Quiere ejecutar este software?) ](images/mess-confirm-image20.png)<br/> ![captura de pantalla de "recordar contraseña". Confirmación ](images/mess-confirm-image21.png)<br/> Ejemplos de confirmaciones de seguridad.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Confirmaciones de confirmación de motivos**<br/> proporcionar información sobre una acción, pero presentarla como confirmación. <br/>                                       | Aunque estos cuadros de diálogo se presentan como confirmaciones, su objetivo real es la educación del usuario o el anuncio de características. <br/> ![captura de pantalla de ¿quiere esta barra de herramientas en la barra de tareas? ](images/mess-confirm-image22.png)<br/> Un ejemplo de confirmación de confirmación de<br/> **Nota:** Este patrón no se recomienda porque normalmente hay una alternativa mejor y más directa. Por ejemplo, [las animaciones](vis-animations.md) son una mejor manera de mostrar la relación entre causa y efecto. <br/>                                                                                                                                                                                                                                     |



 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Use las confirmaciones de "Guardar cambios" solo cuando haya cambios significativos.** No confirme los cambios que el usuario no realizó directamente, como el cambio automático de formato del documento.

**Incorrecto:**

![Captura de pantalla que muestra Microsoft Office Outlook "do you want to save changes?" (¿Desea guardar los cambios?) .](images/mess-confirm-image23.png)

Este ejemplo es incorrecto cuando se usa para un correo electrónico vacío o un documento que el usuario no ha cambiado.

### <a name="icons"></a>Iconos

-   Las confirmaciones no usan iconos de la barra de título.
-   **El icono del área de contenido para una confirmación se basa en su patrón de diseño:**



    | Patrón                                                | Icono                                                                                                                                             |
    |--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
    | Confirmaciones rutinarias <br/>                | Sin icono. <br/>                                                                                                                         |
    | Confirmaciones de acciones de riesgo <br/>           | Icono de advertencia. <br/>                                                                                                                    |
    | Confirmaciones de consecuencias no deseadas <br/> | Use un icono de advertencia si hay riesgo, el icono de característica si está disponible. de lo contrario, no hay ningún icono. <br/>                                          |
    | Aclaraciones <br/>                       | Si la confirmación implica un documento, use la miniatura del documento; De lo contrario, use el icono de característica si está disponible o ningún icono. <br/> |
    | Confirmaciones de seguridad <br/>               | Icono de advertencia. <br/>                                                                                                                    |
    | Confirmaciones de confirmación de motivos <br/>        | Sin icono. <br/>                                                                                                                         |



 

-   **No use iconos de advertencia para preguntas rutinarias.** Esto es contrario al tono [alentador](text-style-tone.md) de Windows hace que el uso del programa se sienta como una actividad peligrosa. Supongamos que los usuarios comprenden las consecuencias de cancelar una tarea antes de que finalice.

**Incorrecto:**

![captura de pantalla de '¿Desea finalizar el tutorial?' ](images/mess-confirm-image24.png)

En este ejemplo, se usa un icono de advertencia para hacer una pregunta rutinaria.

### <a name="commit-buttons"></a>Botones de confirmación

-   **Use respuestas específicas a la instrucción principal si el motivo de la confirmación es obvio o se puede explicar por sí mismo.**

![captura de pantalla de "do you want to save changes?" (¿Desea guardar los cambios?) ](images/mess-confirm-image25.png)

En este ejemplo, el motivo de la confirmación es obvio, por lo que Guardar y No guardar funcionan bien.

-   **De lo contrario, use los botones Sí y No para las respuestas de confirmación.** Si lo hace, los usuarios pensarán en la confirmación antes de responder. Nunca use Aceptar y Cancelar para las confirmaciones.

**Correcto:**

![captura de pantalla de "desea desinstalar los archivos de soporte técnico". ](images/mess-confirm-image26.png)

En este ejemplo, el uso de botones de confirmación Sí/No obliga a los usuarios a leer al menos la instrucción principal.

**Incorrecto:**

![captura de pantalla de "Cancelar la reserva". ](images/mess-confirm-image27.png)

En este ejemplo, usar Aceptar/Cancelar es confuso.

-   **Para cerrar un programa o reiniciar Windows, use respuestas específicas a la instrucción principal.** Para evitar cualquier desconocimiento, no use Cerrar o Sí/No para este propósito.

**Correcto:**

![captura de pantalla del botón Reiniciar ventanas ahora](images/mess-confirm-image28.png)

**Incorrecto:**

![captura de pantalla del botón Sí](images/mess-confirm-image29.png)

En el ejemplo incorrecto, se usa Sí para reiniciar Windows.

### <a name="command-links"></a>Vínculos de comandos

-   **Para el patrón de aclaraciones, considere la posibilidad de usar vínculos de comandos para dejar las alternativas claras.**

**Aceptable:**

![captura de pantalla de "cambiar una o todas las repeticiones". ](images/mess-confirm-image30.png)

**Mejor:**

![captura de pantalla de la misma pregunta mediante vínculos de comandos ](images/mess-confirm-image31.png)

En el mejor ejemplo, los vínculos de comandos aclaran las alternativas.

-   **Presente primero los vínculos de comandos más usados.** El orden resultante debe seguir aproximadamente la probabilidad de uso, pero también tener un flujo lógico.
-   Si un vínculo de comando requiere una explicación adicional, **proporcione una explicación complementaria.** Las explicaciones adicionales describen por qué es posible que los usuarios quieran elegir la opción o qué ocurre si se elige la opción.

Para obtener más instrucciones y ejemplos, vea [Vínculos de comandos](ctrl-command-links.md).

### <a name="default-values"></a>Valores predeterminados

-   **La respuesta predeterminada para una confirmación se basa en su patrón de diseño:**



    | Patrón                                                 | Respuesta predeterminada                                                                                |
    |--------------------------------------------------|---------------------------------------------------------------------------------|
    | Confirmaciones rutinarias <br/>                | Proceder. <br/>                                                            |
    | Confirmaciones de acciones de riesgo <br/>           | No continúe (ni la opción segura). <br/>                                 |
    | Confirmaciones de consecuencias no deseadas <br/> | Si las consecuencias son significativas, no continúe. De lo contrario, continúe. <br/> |
    | Aclaraciones <br/>                       | La respuesta más probable. <br/>                                           |
    | Confirmaciones de seguridad <br/>               | No continúe. <br/>                                                      |
    | Confirmaciones del motivo de la razón por la que se ha convertido <br/>        | Proceder. <br/>                                                            |



 

### <a name="dont-show-this-message-again"></a>No volver a mostrar este mensaje

-   **Use esta opción solo para los patrones de confirmación rutinaria y matriz de motivos.** Para los demás patrones, si la información es necesaria, siempre se debe mostrar.
-   **No proporcione esta opción para justificar la visualización de una confirmación innecesaria.** En su lugar, solo tiene que deshacerse de la confirmación.

**Incorrecto:**

![captura de pantalla de "descartar estos recordatorios?". ](images/mess-confirm-image32.png)

**Sigue siendo incorrecto:**

![captura de pantalla de "No volver a mostrar el mensaje"](images/mess-confirm-image33.png)

En estos ejemplos, agregar una opción No volver a mostrar este mensaje no corrige una confirmación innecesaria.

Para obtener más instrucciones, vea [Cuadros de diálogo](win-dialog-box.md).

### <a name="bulk-operations"></a>Operaciones masivas

-   Para las confirmaciones que se aplican a las operaciones masivas, proporcione una opción para aplicar la confirmación a toda la operación.

![captura de pantalla de 'do this for all items? (¿Hacer esto para todos los elementos?) casilla ](images/mess-confirm-image34.png)

Este ejemplo tiene una opción para las operaciones masivas.

-   Elimine o posponga las confirmaciones en una operación masiva.

**Incorrecto:**

![captura de pantalla del cuadro de diálogo "Confirmar eliminación de archivos" ](images/mess-confirm-image35.png)

En este ejemplo, Windows Explorer en Windows XP confirma cada archivo de solo lectura durante un movimiento masivo de archivos. Es mejor copiar los archivos de solo lectura sin preguntar, o posponer el control de estos archivos y presentar la confirmación al final de la tarea.

### <a name="progressive-disclosure&quot;></a>Muestra progresiva

-   **Si debe incluir información avanzada en un mensaje de confirmación, puede mostrarla mediante botones de divulgación progresiva (por ejemplo, &quot;Mostrar detalles").** Esto simplifica la confirmación del uso típico. No oculte la información necesaria porque es posible que los usuarios no la encuentren.
-   **No use "Mostrar detalles" a menos que realmente haya más detalles.** No solo vuelva a establecer la información existente en un formato diferente.

Para obtener instrucciones de etiquetado, vea [Divulgación progresiva.](ctrl-progressive-disclosure-controls.md)

### <a name="user-account-control"></a>Control de cuentas de usuario

-   **No use la interfaz de usuario de elevación de Control de cuentas de usuario (UAC) como sustituto de una confirmación.** Si una acción necesita confirmación, use un cuadro de diálogo independiente. Durante la interfaz [de usuario de](winenv-uac.md)elevación, los usuarios deben centrarse en si iniciaron la tarea y si el programa es de confianza.
-   **Muestra la confirmación antes de la interfaz de usuario de elevación.** Al hacerlo, se eliminan las elevaciones innecesarias.

## <a name="text"></a>Texto

### <a name="general"></a>General

-   **Quite el texto redundante.** Busque texto redundante en títulos, instrucciones principales, instrucciones complementarias, áreas de contenido, vínculos de comandos y botones de confirmación. Por lo general, deje texto completo en instrucciones y controles interactivos y quite cualquier redundancia de los demás lugares.
-   **No use "advertencia" o "precaución" en el texto.** Si los usuarios necesitan continuar con precaución, indiga esto mediante un icono de advertencia en su lugar.

**Incorrecto:**

![captura de pantalla de la confirmación de formato de volumen ](images/mess-confirm-image36.png)

En este ejemplo, el término "advertencia" no es necesario.

### <a name="titles"></a>Títulos

-   **Use el título para identificar el comando o la característica de donde provenía la confirmación. Excepciones:**
    -   Si muchos comandos diferentes muestran una confirmación, considere la posibilidad de usar el nombre del programa en su lugar.
    -   Si ese título sería redundante o confuso con la instrucción principal, use el nombre del programa en su lugar.

Sin embargo, si la confirmación es de una tarea de ejecución larga y puede mostrarse bien después de iniciar la tarea, use siempre el comando o la característica para identificar claramente el contexto.

-   **No use el título para explicar qué** hacer en el cuadro de diálogo que es el propósito de la instrucción principal.
-   Si agrega claridad, inicie el título con la palabra Confirmar.
-   **Para las confirmaciones de acción de riesgo, puede agregar el nombre del objeto implicado para énfasis adicional.**

![captura de pantalla del título del cuadro de diálogo 'format f drive' ](images/mess-confirm-image13.png)

En este ejemplo, la unidad a la que se va a dar formato se incluye en el título.

-   Use [el uso de mayúsculas de estilo de](glossary.md)título, sin finalizar los signos de puntuación.

### <a name="main-instructions"></a>Instrucciones principales

-   **La instrucción principal de una confirmación se basa en su patrón de diseño:**



    | Patrón                                                 | Instrucción principal                                                                                                                                                                                                                                                                                                                                                                                                          |
    |--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Confirmaciones de consecuencias no deseadas <br/> | estado de la consecuencia no deseada.<br/> **exception:** si una pregunta que pregunta si el usuario desea continuar implica claramente la consecuencia no deseada, pregúntela en su lugar. <br/> ![captura de pantalla de '¿Cerrar todas las pestañas?' Confirmación ](images/mess-confirm-image15.png)<br/> En este ejemplo, pedir al usuario que continúe expresa suficientemente las consecuencias de la acción.<br/> |
    | Todos los demás <br/>                           | Haga una sola pregunta para determinar si el usuario desea continuar. <br/>                                                                                                                                                                                                                                                                                                                              |



 

-   **Sea conciso y use solo una sola oración completa.** Quitar la instrucción principal a la información esencial. Si tiene que explicar algo más, use una instrucción complementaria.
-   **Sea específico si hay objetos implicados, así como sus nombres completos.**
-   **Use expresiones positivas.** Las expresiones positivas son más fáciles de entender para los usuarios.

**Correcto:**

¿Desea habilitar el uso compartido de archivos e impresoras?

**Incorrecto:**

¿Desea deshabilitar el uso compartido de archivos e impresoras?

Sin embargo, las expresiones deben coincidir con el comando asociado, incluso si el comando está con frases negativas; por ejemplo, use disable para confirmar un comando Disable.

-   Aunque no hay reglas estrictas para las expresiones, estas frases de confirmación comunes **tienen la connotación indicada:**



    | Frase                                                            | Connotación                                                            |
    |-------------------------------------------------------------|-------------------------------------------------------------|
    | ¿Está seguro de que desea \[ realizar una acción \] ? <br/> | Confirmar el resultado directo de una solicitud de usuario. <br/> |
    | ¿Desea realizar \[ una acción \] ? <br/>           | Confirmación de un efecto secundario de una solicitud de usuario. <br/>     |
    | ¿Desea seleccionar \[ un \] resultado? <br/>          | Necesita una aclaración. <br/>                           |
    | \[¿Realizar una \] acción? <br/>                          | Sin connotación. <br/>                                 |



 

-   Para las confirmaciones de acción de riesgo, use el término permanentemente para indicar que una acción no se puede deshacer.

![captura de pantalla de confirmación de eliminación permanente ](images/mess-confirm-image37.png)

En este ejemplo, "permanentemente" indica que la acción no se puede deshacer.

-   Use [mayúsculas de estilo oración.](glossary.md)

### <a name="supplemental-instructions"></a>Instrucciones complementarias

-   **La instrucción complementaria para una confirmación se basa en su patrón de diseño:**

    
| Etiqueta | Value |
|--------|-------|
| <strong>Patrón</strong><br /> | <strong>Instrucción complementaria</strong><br /> | 
| Confirmaciones de consecuencias no deseadas <br /> | Haga una única pregunta para determinar si el usuario desea continuar. <br /> | 
| Todos los demás <br /> | Explique los motivos no obvios por los que el usuario podría no querer continuar. Entre estos motivos se incluyen: <br /><ul><li>Posible pérdida de uno o varios de los siguientes elementos:    <ul><li>Un recurso valioso, como la pérdida de datos o la pérdida financiera.</li><li>Integridad o acceso del sistema.</li><li>Privacidad o control sobre la información confidencial.</li></ul></li><li>Acciones que son irreversibles.</li></ul> | 


    

     

-   **No repita la instrucción principal con una redacción ligeramente diferente.** En su lugar, omita la instrucción complementaria si no hay más que agregar.
-   **Para las confirmaciones de consecuencias no deseadas,** considere la posibilidad de usar el término de todos modos para indicar concisamente que hay una razón para no continuar en caso de que el usuario pasara por alto la instrucción principal. Consulte Conceptos de diseño para obtener más información.
-   Use oraciones completas, mayúsculas de estilo oración y signos de puntuación finales.

## <a name="documentation"></a>Documentación

Al hacer referencia a confirmaciones:

-   Consulte una confirmación por su título si el título es específico de la confirmación (es decir, no el nombre del programa); de lo contrario, haga referencia a él mediante su instrucción principal.
-   Si es necesario, puede hacer referencia a un cuadro de diálogo de confirmación como un mensaje.
-   Use el texto exacto, incluido su uso de mayúsculas.
-   Cuando sea posible, formatee el texto con negrita. De lo contrario, coloque el texto entre comillas solo si es necesario para evitar confusiones.

Ejemplo: en el mensaje **Copiar archivo,** haga clic en el archivo más reciente.

