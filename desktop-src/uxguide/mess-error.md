---
title: Mensajes de error (aspectos básicos de diseño)
description: Un mensaje de error alerta a los usuarios de un problema que ya se ha producido.
ms.assetid: b02110e9-985d-4448-9c95-eb958b0059b1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0a8ee17093618dc8a192cfad8ce962f7ed04fc76
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104559004"
---
# <a name="error-messages-design-basics"></a>Mensajes de error (aspectos básicos de diseño)

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Un mensaje de error alerta a los usuarios de un problema que ya se ha producido. Por el contrario, un mensaje de advertencia alerta a los usuarios de una condición que puede provocar un problema en el futuro. Los mensajes de error se pueden presentar mediante cuadros de diálogo modales, mensajes en contexto, notificaciones o globos.

![captura de pantalla del mensaje de error: no se puede cambiar el nombre](images/mess-error-image1.png)

Un mensaje de error modal típico.

Los mensajes de error efectivos informan a los usuarios de que se ha producido un problema, explican por qué se produjo y proporcionan una solución para que los usuarios puedan solucionar el problema. Los usuarios deben realizar una acción o cambiar su comportamiento como resultado de un mensaje de error.

Los mensajes de error bien escritos y útiles son cruciales para una experiencia del usuario de calidad. Los mensajes de error mal escritos dan como resultado una baja satisfacción del producto y son una causa principal de los costos de soporte técnico. Los mensajes de error innecesarios interrumpen el flujo de los usuarios.

**Nota:** Las instrucciones relacionadas con los [cuadros de diálogo](win-dialog-box.md), [los mensajes de advertencia](mess-warn.md), las [confirmaciones](mess-confirm.md), los [iconos estándar](vis-std-icons.md), las [notificaciones](mess-notif.md)y el [diseño](vis-layout.md) se presentan en artículos independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

Para decidirte, intenta responder a estas preguntas:

- **¿La interfaz de usuario (UI) presenta un problema que ya se ha producido?** Si no es así, el mensaje no es un error. Si el usuario recibe una alerta de una condición que puede provocar un problema en el futuro, use un mensaje de advertencia.
- **¿Se puede evitar el problema sin causar confusión?** Si es así, evite el problema en su lugar. Por ejemplo, utilice controles que están restringidos a valores válidos en lugar de usar controles sin restricciones que pueden requerir mensajes de error. Además, deshabilite los controles al hacer clic en se produciría un error, siempre que sea obvio que el control está deshabilitado.
- **¿Se puede corregir el problema automáticamente?** Si es así, controle el problema y suprima el mensaje de error.
- **¿Es probable que los usuarios realicen una acción o cambien su comportamiento como resultado del mensaje?** En caso contrario, la condición no justifica interrumpir al usuario, por lo que es mejor suprimir el error.
- **¿El problema es importante cuando los usuarios usan activamente otros programas?** Si es así, considere la posibilidad de mostrar el problema mediante un [icono de área de notificación](winenv-notification.md).
- **¿El problema no está relacionado con la actividad del usuario actual, no requiere la intervención inmediata del usuario y los usuarios pueden ignorarlo libremente?** Si es así, use una [notificación de error de acción](mess-notif.md) en su lugar.
- **¿El problema está relacionado con el estado de una tarea en segundo plano dentro de una ventana principal?** Si es así, considere la posibilidad de mostrar el problema con [barras de estado](ctrl-status-bars.md).
- **¿Son los profesionales de TI de los usuarios de destino primarios?** Si es así, considere la posibilidad de usar un mecanismo de comentarios alternativo, como entradas de [archivo de registro](glossary.md) o alertas de correo electrónico. Los profesionales de ti prefieren los archivos de registro de forma segura para obtener información no crítica.

## <a name="design-concepts"></a>Conceptos de diseño

**Características de los mensajes de error insuficientes**

No debe sorprender que haya muchos mensajes de error molestos, no ayudantes y de mala escritura. Y dado que los mensajes de error se presentan a menudo mediante cuadros de diálogo modales, interrumpen la actividad y la demanda actuales del usuario que se deben confirmar antes de permitir que el usuario continúe.

Parte del problema es que hay muchas maneras de hacerlo mal. Tenga en cuenta estos ejemplos del mensaje de error Hall of Shame:

**Mensajes de error innecesarios**

**Incorrecto:**

![captura de pantalla del mensaje de error: error de aplicación ](images/mess-error-image2.png)

Este ejemplo de Windows XP podría ser el peor de los mensajes de error. Indica que un programa no se pudo iniciar porque Windows está en proceso de apagado. No hay nada que el usuario pueda hacer sobre esto, o incluso quiere hacer esto (el usuario decidió cerrar Windows, después de todo). Y al mostrar este mensaje de error, Windows evita que se apague.

**El problema:** El propio mensaje de error es el problema. Además de descartar el mensaje de error, no hay nada para que lo hagan los usuarios.

**Causa principal:** Informar de todos los casos de error, independientemente de los objetivos o el punto de vista de los usuarios.

**Alternativa recomendada:** No informe de los errores que los usuarios no preocupan.

**Mensajes de error "correctos"**

**Incorrecto:**

![captura de pantalla del mensaje de error: error de eliminación ](images/mess-error-image3.png)

Este mensaje de error provocó que el usuario elegira no reiniciar Windows inmediatamente después de la eliminación del programa. La eliminación del programa se realizó correctamente desde el punto de vista del usuario.

**El problema:** No hay ningún error en el punto de vista del usuario. Además de descartar el mensaje de error, no hay nada para que lo hagan los usuarios.

**Causa principal:** La tarea se completó correctamente desde el punto de vista del usuario, pero no se pudo realizar desde el punto de vista del programa de desinstalación.

**Alternativa recomendada:** No notifique errores de condiciones que los usuarios consideren aceptables.

**Mensajes de error totalmente inútil**

**Incorrecto:**

![captura de pantalla del mensaje de error: error desconocido ](images/mess-error-image4.png)

Los usuarios aprenden que se produjo un error, pero no saben cuál fue el error o qué hacer con él. Y no, no es correcto.

**El problema:** El mensaje de error no proporciona un problema específico y no hay ningún usuario que pueda hacer con él.

**Causa principal:** Lo más probable es que el programa tenga un control de errores deficiente.

**Alternativa recomendada:** Diseñar un buen control de errores en el programa.

**Mensajes de error incomprensibles**

**Incorrecto:**

![captura de pantalla del mensaje de error: copia de seguridad no completada ](images/mess-error-image5.png)

En este ejemplo, la instrucción del problema está clara, pero la explicación complementaria se encuentra en un solo deflector.

**El problema:** La instrucción o solución del problema es incomprensible.

**Causa principal:** Explicación del problema desde el punto de vista del código en lugar de la del usuario.

**Alternativa recomendada:** Escriba el texto del mensaje de error que los usuarios de destino puedan comprender fácilmente. Proporcionar soluciones que los usuarios puedan realizar realmente. Diseñar la experiencia del mensaje de error de su programa no tiene los programadores que componen mensajes de error en el lugar.

**Mensajes de error que se sobrecomunican**

**Incorrecto:**

![captura de pantalla de un mensaje extremadamente detallado ](images/mess-error-image6.png)

En este ejemplo, el mensaje de error aparentemente intenta explicar cada paso de solución de problemas.

**El problema:** Demasiada información.

**Causa principal:** Ofrecer demasiados detalles o intentar explicar un proceso de solución de problemas complicado dentro de un mensaje de error.

**Alternativa recomendada:** Evite detalles innecesarios. Además, evite los solucionadores de problemas. Si es necesario un solucionador de problemas, céntrese en las soluciones más probables y explique el resto vinculando al tema adecuado en la ayuda de.

**Mensajes de error innecesariamente peligrosos**

**Incorrecto:**

![captura de pantalla del mensaje: no se encuentra el objeto ](images/mess-error-image7.png)

La incapacidad del programa para encontrar un objeto apenas suena catastrófico. Y suponiendo que es catastrófico, ¿por qué es correcta la respuesta?

**El problema:** El tono del programa es innecesariamente fuerte o espectacular.

**Causa principal:** El problema se debe a un error que parece catastrófico desde el punto de vista del programa.

**Alternativa recomendada:** Elija el idioma cuidadosamente en función del punto de vista del usuario.

**Mensajes de error que culpan a los usuarios**

**Incorrecto:**

![captura de pantalla del mensaje: carácter no válido ](images/mess-error-image8.png)

¿Por qué los usuarios se sienten como un delincuente?

**El problema:** El mensaje de error se frase de forma que accuses el usuario de crear un error.

**Causa principal:** Formulación insensitive que se centra en el comportamiento del usuario en lugar del problema.

**Alternativa recomendada:** Céntrese en el problema, no en la acción del usuario que provocó el problema, usando la voz pasiva según sea necesario.

**Mensajes de error de tonto**

**Incorrecto:**

![captura de pantalla del mensaje: error en el informe de errores ](images/mess-error-image9.png)

En este ejemplo, la instrucción del problema es bastante planchada y no se proporciona ninguna solución.

**El problema:** Instrucciones de mensajes de error que son tontos o no sequitors.

**Causa principal:** Crear mensajes de error sin prestar atención a su contexto.

**Alternativa recomendada:** Haga que un escritor cree y revise los mensajes de error. Tenga en cuenta el contexto y el estado del usuario cuando revise los errores.

**Mensajes de error del programador**

**Incorrecto:**

![captura de pantalla del mensaje: dirección de infracción de acceso ](images/mess-error-image10.png)

En este ejemplo, el mensaje de error indica que hay un error en el programa. Este mensaje de error solo tiene significado para el programador.

**El problema:** Los mensajes destinados a ayudar a los desarrolladores de programas a encontrar errores se quedan en la versión de lanzamiento del programa. Estos mensajes de error no tienen ningún significado ni valor para los usuarios.

**Causa principal:** Programadores que usan la interfaz de usuario normal para hacer mensajes a sí mismos.

**Alternativa recomendada:** Los desarrolladores deben compilar de forma condicional todos estos mensajes para que se quiten automáticamente de la versión de lanzamiento de un producto. No pierda tiempo intentando realizar errores como este comprensible para los usuarios porque su única audiencia son los programadores.

**Mensajes de error presentados incorrectamente**

**Incorrecto:**

![captura de pantalla del mensaje: error inesperado ](images/mess-error-image11.png)

Este ejemplo tiene muchos errores de presentación comunes.

**El problema:** No se obtienen todos los detalles de la presentación del mensaje de error.

**Causa principal:** No conocer y aplicar las instrucciones del mensaje de error. No usar escritores y editores para crear y revisar los mensajes de error.

La naturaleza del control de errores es tal que muchos de estos errores son muy fáciles de realizar. Se molesta en darse de alto que la mayoría de los mensajes de error podrían ser nominados para el Hall of Shame.

**Características de los mensajes de error correctos**

A diferencia de los ejemplos anteriores incorrectos, los mensajes de error correctos tienen:

- **Un problema.** Indica que se ha producido un problema.
- **Una causa.** Explica por qué se ha producido el problema.
- **Una solución.** Proporciona una solución para que los usuarios puedan solucionar el problema.

Además, se presentan buenos mensajes de error de la manera siguiente:

- **Apropiadas.** El mensaje presenta un problema que los usuarios le interesan.
- **Accionable.** Los usuarios deben realizar una acción o cambiar su comportamiento como resultado del mensaje.
- **Centrado en el usuario.** El mensaje describe el problema en términos de acciones o objetivos del usuario de destino, no en lo que respecta al código al que está insatisfecho.
- **Veamos.** El mensaje es lo más corto posible, pero no es más corto.
- **Claridad.** El mensaje utiliza el lenguaje sin formato para que los usuarios de destino puedan comprender fácilmente el problema y la solución.
- **Cuestión.** El mensaje describe el problema con un idioma específico, lo que aporta nombres específicos, ubicaciones y valores de los objetos implicados.
- **Correcto.** Los usuarios no deben ser culpados o no sentirse estúpido.
- **Menos.** Se muestra con poca frecuencia. Los mensajes de error que se muestran con frecuencia son un signo de diseño incorrecto.

Al diseñar la experiencia de control de errores para que tenga estas características, puede evitar que los mensajes de error del programa salgan del mensaje de error Hall of Shame.

**Evitar mensajes de error innecesarios**

A menudo, el mejor mensaje de error es ningún mensaje de error. Muchos errores se pueden evitar a través de un mejor diseño, y a menudo hay mejores alternativas para los mensajes de error. Normalmente es mejor evitar un error que notificar uno.

Los mensajes de error más obvios que se deben evitar son aquellos que no son accionables. Si es probable que los usuarios descarten el mensaje sin realizar ni cambiar nada, omita el mensaje de error.

Algunos mensajes de error se pueden eliminar porque no tienen problemas desde el punto de vista del usuario. Por ejemplo, supongamos que el usuario intentó eliminar un archivo que ya está en proceso de eliminación. Aunque esto podría ser un caso inesperado desde el punto de vista del código, los usuarios no tienen en cuenta este error porque se obtiene el resultado deseado.

**Incorrecto:**

![captura de pantalla del mensaje: no se puede eliminar el archivo ](images/mess-error-image12.png)

Este mensaje de error debe eliminarse porque la acción se realizó correctamente desde el punto de vista del usuario.

En otro ejemplo, supongamos que el usuario cancela explícitamente una tarea. Para el punto de vista del usuario, la siguiente condición no es un error.

**Incorrecto:**

![captura de pantalla del mensaje: no se puede completar la copia de seguridad ](images/mess-error-image13.png)

Este mensaje de error también debe eliminarse porque la acción se realizó correctamente desde el punto de vista del usuario.

A veces, los mensajes de error se pueden eliminar centrándose en los objetivos de los usuarios en lugar de en la tecnología. Al hacerlo, reconsidere cuál es realmente un error. ¿El problema se debe a los objetivos del usuario o a la capacidad del programa para satisfacerlos? Si la acción del usuario tiene sentido en el mundo real, también debe tener sentido en el software.

Por ejemplo, supongamos que en un programa de comercio electrónico un usuario intenta encontrar un producto mediante la búsqueda, pero la consulta de búsqueda literal no tiene ninguna coincidencia y el producto deseado no tiene existencias. Técnicamente, se trata de un error, pero en lugar de asignar un mensaje de error, el programa podría:

- Siga buscando los productos que más se aproximen a la consulta.
- Si la búsqueda tiene errores obvios, recomiende automáticamente una consulta corregida.
- Controle automáticamente los problemas comunes, como errores ortográficos, correcciones alternativas y casos de pluralización no coincidentes.
- Indicar si el producto va a estar en existencias.

Siempre y cuando la solicitud del usuario sea razonable, un programa de comercio electrónico bien diseñado debe devolver resultados razonables, no errores.

Otra excelente manera de evitar los mensajes de error es evitar problemas en el primer lugar. Puede evitar errores si:

- **Usar controles restringidos.** Usar controles que están restringidos a valores válidos. Los controles como listas, controles deslizantes, casillas, botones de radio y selectores de fecha y hora se restringen a valores válidos, mientras que los cuadros de texto no suelen y pueden requerir mensajes de error. Sin embargo, puede restringir los cuadros de texto para que acepten solo determinados caracteres y acepten un número máximo de caracteres.
- **Usar interacciones restringidas.** En el caso de las operaciones de arrastre, permita a los usuarios quitar solo en destinos válidos.
- **Usar controles deshabilitados y elementos de menú.** Deshabilite los controles y los elementos de menú cuando los usuarios puedan deducir fácilmente por qué está deshabilitado el control o el elemento de menú.
- **Proporcionar buenos valores predeterminados.** Es menos probable que los usuarios realicen errores de entrada si pueden aceptar los valores predeterminados. Aunque los usuarios decidan cambiar el valor, el valor predeterminado permite a los usuarios conocer el formato de entrada esperado.
- **Hacer que las cosas funcionen.** Es menos probable que los usuarios realicen errores si las tareas no son necesarias o se realizan automáticamente para ellas. O bien, si los usuarios realizan pequeños errores pero su intención es evidente, el problema se corrige automáticamente. Por ejemplo, puede corregir automáticamente los problemas de formato menores.

**Proporcionar mensajes de error necesarios**

En ocasiones, realmente es necesario proporcionar un mensaje de error. Los usuarios hacen que los errores, las redes y los dispositivos dejen de funcionar, los objetos no se pueden encontrar o modificar, no se pueden completar las tareas y los programas tienen errores. Idealmente, estos problemas se producirían con menos frecuencia, por ejemplo, podemos diseñar nuestro software para evitar muchos tipos de errores de usuario, pero no es realista evitar todos estos problemas. Y cuando se produce uno de estos problemas, un mensaje de error útil recupera los usuarios rápidamente.

Una creencia común es que los mensajes de error son la peor experiencia del usuario y deben evitarse en todos los costos, pero es más preciso decir que la confusión de los usuarios es la peor experiencia y debe evitarse a todos los costos. A veces, el costo es un mensaje de error útil.

Considere los controles deshabilitados. La mayoría de las veces, es obvio por qué un control está deshabilitado, por lo que deshabilitar el control es una excelente manera de evitar un mensaje de error. Sin embargo, ¿qué ocurre si el motivo por el que un control está deshabilitado no es obvio? El usuario no puede continuar y no hay ningún comentario para determinar el problema. Ahora el usuario está atascado y debe deducir el problema u obtener soporte técnico. En tales casos, es mucho mejor dejar el control habilitado y proporcionar un mensaje de error útil en su lugar.

**Incorrecto:**

![captura de pantalla del mensaje: ¿Dónde guardar la copia de seguridad? ](images/mess-error-image14.png)

¿Por qué es el botón siguiente deshabilitado aquí? Mejor dejarla habilitada y evitar la confusión del usuario al dar un mensaje de error útil.

Si no está seguro de si debe dar un mensaje de error, empiece por redactar el mensaje de error que puede dar. Si es probable que los usuarios realicen una acción o cambien su comportamiento como resultado, proporcione el mensaje de error. Por el contrario, si es probable que los usuarios descarten el mensaje sin realizar ni cambiar nada, omita el mensaje de error.

**Diseño para un buen control de errores**

Aunque la creación de un buen texto de mensaje de error puede ser desafiante, a veces es imposible sin una buena compatibilidad de control de errores del programa. Tenga en cuenta este mensaje de error:

**Incorrecto:**

![captura de pantalla del mensaje: error desconocido ](images/mess-error-image15.png)

Lo más probable es que el problema sea realmente desconocido porque la compatibilidad con el control de errores del programa no tiene.

Aunque es posible que se trate de un mensaje de error de escritura muy deficiente, lo más probable es que refleje la falta de un buen control de errores por parte del código subyacente, no hay información específica que sepa sobre el problema.

Para crear mensajes de error específicos y accionables centrados en el usuario, el código de control de errores del programa debe proporcionar información de error específica y de alto nivel:

- Cada problema debe tener un código de error único asignado.
- Si un problema tiene varias causas, el programa debe determinar la causa concreta siempre que sea posible.
- Si el problema tiene parámetros, se deben mantener los parámetros.
- Los problemas de bajo nivel deben administrarse en un nivel suficientemente alto para que el mensaje de error pueda presentarse desde el punto de vista del usuario.

Los mensajes de error correctos no son simplemente un problema de la interfaz de usuario, sino un problema de diseño de software. Una buena experiencia de mensajes de error no es algo que se pueda agregar más tarde.

**Solución de problemas (y cómo evitarlo)**

Los resultados de la solución de problemas se producen cuando se produce un problema con varias causas diferentes con un solo mensaje de error.

**Incorrecto:**

![diagrama de un mensaje que indica tres causas ](images/mess-error-image16.png)

**Correcto:**

![diagrama de tres mensajes que indican una causa cada](images/mess-error-image17.png)

Los resultados de la solución de problemas se producen cuando se emiten varios problemas con un solo mensaje de error.

En el ejemplo siguiente, no se pudo migrar un elemento porque ya se ha quitado o eliminado, o se ha denegado el acceso. Si el programa puede determinar fácilmente la causa, ¿por qué poner la carga en el usuario para determinar la causa específica?

**Incorrecto:**

![captura de pantalla del mensaje que indica dos causas ](images/mess-error-image18.png)

Bueno, ¿cuál es? Ahora el usuario tiene que solucionar problemas.

El programa puede determinar si se denegó el acceso, por lo que se debe informar de este problema con un mensaje de error específico.

**Correcto:**

![captura de pantalla del mensaje que indica una causa ](images/mess-error-image19.png)

Con una causa específica, no se requiere ninguna solución de problemas.

Use mensajes con varias causas solo cuando no se pueda determinar la causa concreta. En este ejemplo, sería difícil que el programa determinara si el elemento se moviera o eliminó, por lo que se podría usar aquí un solo mensaje de error con varias causas. Sin embargo, no es probable que los usuarios vayan a tener cuidado si, por ejemplo, no pudieron trasladar un archivo eliminado. En estas causas, el mensaje de error no es necesario.

**Control de errores desconocidos**

En algunos casos, no se conoce el problema, la causa o la solución. Si no se aconseja suprimir el error, es mejor estar al día de la falta de información que presentar problemas, causas o soluciones que podrían no ser correctas.

Por ejemplo, si el programa tiene una excepción no controlada, el siguiente mensaje de error es adecuado:

![captura de pantalla del mensaje: error desconocido ](images/mess-error-image20.png)

Si no puede suprimir un error desconocido, es mejor estar al día de la falta de información.

Por otro lado, proporcione información específica y accionable si es probable que sea útil la mayor parte del tiempo.

![Captura de pantalla que muestra un mensaje de Office Communicator ' servidor no disponible '. ](images/mess-error-image21.png)

Este mensaje de error es adecuado para un error desconocido si la conectividad de red suele ser el problema.

**Determinar el tipo de mensaje adecuado**

Algunos problemas se pueden presentar como un error, una advertencia o información, según el énfasis y la formulación. Por ejemplo, supongamos que una página web no puede cargar un control ActiveX sin firmar basado en la configuración actual de Windows Internet Explorer:

- **Error.** "Esta página no puede cargar un control ActiveX sin firmar". (Frase como un problema existente).
- **Atención.** "Es posible que esta página no se comporte de la manera esperada porque Windows Internet Explorer no está configurado para cargar controles ActiveX sin firmar". o "¿desea permitir que esta página Instale un control ActiveX sin firmar? Hacerlo desde orígenes que no son de confianza puede dañar el equipo ". (Ambas frases como condiciones que pueden causar problemas en el futuro).
- **Informaciones.** "Ha configurado Windows Internet Explorer para bloquear los controles ActiveX sin firmar". (Frase como instrucción de hecho).

**Para determinar el tipo de mensaje adecuado, céntrese en el aspecto más importante del problema que los usuarios necesitan conocer o actuar sobre ellos.** Normalmente, si un problema impide que el usuario continúe, debe presentarlo como un error. Si el usuario puede continuar, preséntela como advertencia. Cree la [instrucción principal](text-ui.md) u otro texto correspondiente en función de ese foco y, a continuación, elija un icono ([estándar](vis-std-icons.md) o de otro tipo) que coincida con el texto. Los iconos y el texto de la instrucción principal siempre deben coincidir.

**Presentación de mensajes de error**

La mayoría de los mensajes de error de los programas de Windows se presentan mediante cuadros de diálogo modales (como la mayoría de los ejemplos de este artículo), pero hay otras opciones:

- En contexto
- Globos
- Notificaciones
- Iconos del área de notificación
- Barras de estado
- Archivos de registro (para los errores dirigidos a los profesionales de TI)

La colocación de los mensajes de error en los cuadros de diálogo modales tiene la ventaja de requerir la atención inmediata y la confirmación del usuario. Sin embargo, esto también es su principal inconveniente si no es necesario prestar atención.

![captura de pantalla del mensaje: detenga lo que está haciendo ](images/mess-error-image22.png)

¿Realmente necesita interrumpir a los usuarios para que puedan hacer clic en el botón cerrar? Si no es así, considere alternativas al uso de un cuadro de diálogo modal.

Los cuadros de diálogo modales son una excelente opción cuando el usuario debe confirmar el problema inmediatamente antes de continuar, pero a menudo es una opción deficiente en caso contrario. Por lo general, es preferible usar la presentación de peso más claro que realiza el trabajo.

**Evitar la sobrecomunicación**

Por lo general, [los usuarios no leen, examinan](vis-layout.md). Cuanto mayor sea el texto, más difícil será el análisis del texto y más probable será que los usuarios no lean el texto. Como resultado, es importante reducir el texto a sus aspectos esenciales y usar la divulgación progresiva y los vínculos de ayuda cuando sea necesario para proporcionar información adicional.

Hay muchos ejemplos extremos, pero echemos un vistazo a uno más típico. El ejemplo siguiente tiene la mayoría de los atributos de un mensaje de error, pero su texto no es conciso y requiere motivación para leer.

**Incorrecto:**

![captura de pantalla del mensaje detallado ](images/mess-error-image23.png)

Este ejemplo es un mensaje de error, pero se sobrecomunica.

¿Qué es todo este texto realmente? Algo como esto:

**Correcto:**

![captura de pantalla del mensaje: no se detectó la grabadora de CD ](images/mess-error-image24.png)

Este mensaje de error tiene esencialmente la misma información, pero es mucho más conciso.

Mediante el uso de la ayuda para proporcionar los detalles, este mensaje de error tiene un [estilo piramidal invertido](text-ui.md) de presentación.

Para obtener más instrucciones y ejemplos sobre cómo sobrecomunicar, consulte el texto de la [interfaz de usuario](text-ui.md).

**Si solo hace ocho cosas**

1. Diseñe el programa para el control de errores.
2. No proporcione mensajes de error innecesarios.
3. Evite la confusión de los usuarios al asignar los mensajes de error necesarios.
4. Asegúrese de que el mensaje de error proporciona un problema, una causa y una solución.
5. Asegúrese de que el mensaje de error es relevante, accionable, brief, Clear, specific, correcto y raros.
6. Diseñe mensajes de error desde el punto de vista del usuario, no desde el punto de vista del programa.
7. Evite que intervenga el usuario en la solución de problemas use un mensaje de error diferente para cada causa detectable.
8. Use el método de presentación de peso más claro que hace el trabajo correctamente.

**Patrones de uso**

Los mensajes de error tienen varios patrones de uso:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Problemas del sistema</strong><br/> El sistema operativo, el dispositivo de hardware, la red o el programa no se han realizado correctamente o no están en el estado necesario para realizar una tarea. <br/></td>
<td>El usuario puede resolver muchos problemas del sistema: <br/>
<ul>
<li>Los problemas del dispositivo se pueden solucionar si se activa el dispositivo, se vuelve a conectar el dispositivo y se insertan medios.</li>
<li>Los problemas de red pueden resolverse mediante la comprobación de la conexión de red física y la ejecución <strong>de diagnósticos de red y reparación</strong>.</li>
<li>Los problemas de programas se pueden resolver cambiando las opciones del programa o reiniciando el programa.</li>
</ul>
<img src="images/mess-error-image25.png" alt="Screen shot of message: Can&#39;t find a camera " /><br/> En este ejemplo, el programa no puede encontrar una cámara para realizar una tarea de usuario.<br/> <img src="images/mess-error-image26.png" alt="Screen shot of message Network discovery off " /><br/> En este ejemplo, es necesario activar una característica necesaria para realizar una tarea.<br/></td>
</tr>
<tr class="even">
<td><strong>Problemas de archivos</strong><br/> No se encontró un archivo o carpeta necesarios para una tarea iniciada por el usuario, ya está en uso o no tiene el formato esperado. <br/></td>
<td><img src="images/mess-error-image27.png" alt="Screen shot of message: Can&#39;t delete file " /><br/> En este ejemplo, no se puede eliminar el archivo o la carpeta porque no se encontró.<br/> <img src="images/mess-error-image28.png" alt="Screen shot of message: Can&#39;t play this file " /><br/> En este ejemplo, el programa no admite el formato de archivo especificado.<br/></td>
</tr>
<tr class="odd">
<td><strong>Problemas de seguridad</strong><br/> El usuario no tiene permiso para obtener acceso a un recurso o tiene privilegios suficientes para realizar una tarea iniciada por el usuario. <br/></td>
<td><img src="images/mess-error-image29.png" alt="Screen shot of message: You don&#39;t have permission " /><br/> En este ejemplo, el usuario no tiene permiso para obtener acceso a un recurso.<br/> <img src="images/mess-error-image30.png" alt="Screen shot of message: You don&#39;t have privilege " /><br/> En este ejemplo, el usuario no tiene privilegios para realizar una tarea.<br/></td>
</tr>
<tr class="even">
<td><strong>Problemas de tareas</strong><br/> Existe un problema específico al realizar una tarea iniciada por el usuario (que no sea un sistema, un archivo no encontrado, un formato de archivo o un problema de seguridad). <br/></td>
<td><img src="images/mess-error-image31.png" alt="Screen shot of message: Data can&#39;t be pasted " /><br/> En este ejemplo, los datos del portapapeles no se pueden pegar en Paint.<br/> <img src="images/mess-error-image32.png" alt="Screen shot of message: Upgrade can&#39;t be installed " /><br/> En este ejemplo, el usuario no puede instalar una actualización de software.<br/></td>
</tr>
<tr class="odd">
<td><strong>Problemas de entrada del usuario</strong><br/> El usuario ha especificado un valor incorrecto o incoherente con otros datos proporcionados por el usuario. <br/></td>
<td><img src="images/mess-error-image33.png" alt="Screen shot of message: Incorrect time value " /><br/> En este ejemplo, el usuario ha especificado un valor de hora incorrecto.<br/> <img src="images/mess-error-image34.png" alt="Screen shot of message: Incorrect input format " /><br/> En este ejemplo, los datos proporcionados por el usuario no tienen el formato correcto.<br/></td>
</tr>
</tbody>
</table>

## <a name="guidelines"></a>Directrices

### <a name="presentation"></a>Presentación

- **Utilice los cuadros de diálogo de tareas siempre que sea necesario** para lograr una apariencia y un diseño coherentes. Los cuadros de diálogo de tareas requieren Windows Vista o posterior, por lo que no son adecuados para versiones anteriores de Windows. Si debe usar un cuadro de mensaje, separe la instrucción principal de la instrucción complementaria con dos saltos de línea.

### <a name="user-input-errors"></a>Errores de entrada del usuario

- **Siempre que sea posible, evite o reduzca los errores de entrada del usuario:**
  - Usar controles que están restringidos a valores válidos.
  - Si se deshabilitan los controles y los elementos de menú al hacer clic, se producirá un error, siempre que sea obvio el motivo por el que el control o el elemento de menú está deshabilitado.
  - Proporcionar buenos valores predeterminados.

**Incorrecto:**

![captura de pantalla de un cuadro de texto con etiqueta de volumen de altavoz ](images/mess-error-image35.png)

En este ejemplo, se usa un cuadro de texto sin restricciones para la entrada restringida. En su lugar, use un control deslizante.

- **Utilice el control de errores no modal (errores o globos en contexto) para los problemas de los datos contextuales de los usuarios.**
- **Usar globos para problemas de entrada de usuario de punto único no críticos detectados en un cuadro de texto o inmediatamente después de que un cuadro de texto pierda el foco.** Los [globos](https://msdn.microsoft.com/library/windows/desktop/aa511451.aspx) no requieren espacio de pantalla disponible ni el diseño dinámico necesario para mostrar los mensajes en contexto. Muestra un solo globo a la vez. Dado que el problema no es crítico, no es necesario ningún icono de error. Los globos desaparecen cuando se hace clic en él, cuando se resuelve el problema o después de un tiempo de espera.

![captura de pantalla del mensaje: carácter incorrecto ](images/mess-error-image36.png)

En este ejemplo, un globo indica un problema de entrada mientras sigue en el control.

- **Use errores en contexto para la detección diferida de errores,** normalmente errores detectados al hacer clic en el botón confirmar. (No use [errores en contexto](glossary.md) para la configuración que se confirma inmediatamente). Puede haber varios errores en contexto a la vez. Use el texto normal y un icono de error de 16x16 píxeles, y colóquelos directamente junto al problema siempre que sea posible. Los errores en contexto no desaparecen a menos que el usuario confirme y no se encuentren otros errores.

![captura de pantalla del mensaje: dirección de correo electrónico incorrecta ](images/mess-error-image37.png)

En este ejemplo, se usa un error en contexto para un error encontrado al hacer clic en el botón confirmar.

- **Utilice el control de errores modal (cuadros de diálogo o cuadros de mensajes) para todos los demás problemas, incluidos los** errores que implican varios controles o que no se encuentran contextuales o errores de entrada, al hacer clic en un botón de confirmación.
- **Cuando se notifique un problema de entrada del usuario, establezca el foco de entrada en el primer control con los datos incorrectos.** Desplácese por el control en la vista si es necesario. Si el control es un cuadro de texto, seleccione todo el contenido. Siempre debe ser obvio a qué hace referencia el mensaje de error.
- **No borre la entrada incorrecta.** En su lugar, déjelo para que el usuario pueda ver y corregir el problema sin tener que comenzar de nuevo.
  - **Excepción:** Borrar la contraseña incorrecta y ANCLAr los cuadros de texto porque los usuarios no pueden corregir la entrada enmascarada eficazmente.

### <a name="troubleshooting"></a>Solución de problemas

- **Evite crear problemas de solución de problemas.** No confíe en un solo mensaje de error para informar de un problema con varias causas detectables diferentes.
- **Use un mensaje de error diferente (normalmente una instrucción complementaria diferente) para cada causa detectable.** Por ejemplo, si un archivo no se puede abrir por varias razones, proporcione una instrucción complementaria independiente para cada motivo.
- **Use un mensaje con varias causas solo cuando no se pueda determinar la causa concreta.** En este caso, presente las soluciones en orden de probabilidad de corregir el problema. Esto ayuda a los usuarios a resolver el problema de forma más eficaz.

### <a name="icons"></a>Iconos

- **Los cuadros de diálogo de mensajes de error modales no tienen iconos de barra de título.** Los iconos de la barra de título se usan como una distinción visual entre las ventanas principales y secundarias.
- **Use un icono de error.** Excepciones:
  - Si el error es un problema de entrada de usuario que se muestra mediante un cuadro de diálogo modal o un globo, no use un icono. De este modo, se contrarresta el tono de promoción de las ventanas. Sin embargo, los mensajes de error en contexto deben usar un pequeño icono de error (16x16 píxeles) para identificarlos claramente como mensajes de error.

     ![captura de pantalla del mensaje formato postal incorrecto](images/mess-error-image38.png)

     ![captura de pantalla del nombre de equipo de mensaje demasiado largo](images/mess-error-image39.png)

     En estos ejemplos, los problemas de los datos proporcionados por el usuario no necesitan iconos de error.

     ![captura de pantalla del formato de número de teléfono de mensaje incorrecto](images/mess-error-image40.png)

     En este ejemplo, un mensaje de error en contexto necesita un pequeño icono de error para identificarlo claramente como un mensaje de error.

- Si el problema se debe a una característica que tiene un icono (y no un problema de entrada del usuario), puede usar el icono de la característica con una superposición de errores. Si lo hace, use también el nombre de la característica como asunto del error.

    ![mensaje de captura de pantalla el reproductor de media no puede reproducir el archivo ](images/mess-error-image41.png)

    En este ejemplo, el icono de la característica tiene una superposición de errores y la característica es el asunto del error.

- **No utilice iconos de advertencia para los errores.** Esto se suele hacer para que la presentación se sienta menos grave. Los errores no son advertencias.

    **Incorrecto:**

    ![captura de pantalla del cambio rápido de mensajes no habilitado ](images/mess-error-image42.png)

    En este ejemplo, un icono de advertencia se usa incorrectamente para que el error parezca menos grave.

Para obtener más instrucciones y ejemplos, vea [iconos estándar](vis-std-icons.md).

### <a name="progressive-disclosure"></a>Muestra progresiva

- **Use un botón Mostrar u ocultar detalles de divulgación progresiva para ocultar información avanzada o detallada en un mensaje de error.** Al hacerlo, se simplifica el mensaje de error para el uso típico. No oculte la información necesaria, ya que es posible que los usuarios no la encuentren.

![captura de pantalla del mensaje: ActiveSync no puede iniciar sesión ](images/mess-error-image43.png)

En este ejemplo, el botón de divulgación progresiva ayuda a los usuarios a profundizar para obtener más detalles si lo quieren o a simplificar la interfaz de usuario si no lo hacen.

- **No use Mostrar u ocultar detalles a menos que haya realmente más detalles.** No solo tiene que volver a indicar la información existente en un formato más detallado.
- **No use Mostrar u ocultar detalles para mostrar información de ayuda.** Use los vínculos de la ayuda en su lugar.

Para obtener instrucciones de etiquetas, vea [controles de divulgación progresiva](ctrl-progressive-disclosure-controls.md).

**No volver a mostrar este mensaje**

- **Si un mensaje de error necesita esta opción, reconsidere el error y su frecuencia.** Si tiene todas las características de un error (relevante, accionable y poco frecuente), no debe tener sentido que los usuarios lo supriman.

Para obtener más instrucciones, consulte [cuadros de diálogo](win-dialog-box.md).

### <a name="default-values"></a>Valores predeterminados

- **Seleccione la respuesta más segura, menos destructiva o más segura como predeterminada.** Si la seguridad no es un factor, seleccione el comando más probable o práctico.

### <a name="help"></a>Ayuda

- **Diseñe mensajes de error para evitar la necesidad de ayuda.** Normalmente, los usuarios no deben tener que leer texto externo para comprender y resolver el problema, a menos que la solución requiera varios pasos.
- **Asegúrese de que el contenido de la ayuda es relevante y útil.** No debe ser una resituación detallada del mensaje de error, sino que debe contener información útil que esté fuera del ámbito del mensaje de error, como formas de evitar el problema en el futuro. No proporcione un vínculo de ayuda solo porque puede.
- **Use vínculos de ayuda específicos, concisos y pertinentes para tener acceso al contenido de la ayuda.** No use botones de comando ni la divulgación progresiva para este fin.
- **En el caso de los mensajes de error que no se pueden hacer específicos y accionables, considere la posibilidad de proporcionar vínculos al contenido de la ayuda en línea.** Al hacerlo, puede proporcionar a los usuarios información adicional que puede actualizar después de que se publique el programa.

Para obtener más instrucciones, consulte la [ayuda](winenv-help.md)de.

### <a name="error-codes"></a>Códigos de error

- **En el caso de los mensajes de error que no se pueden hacer específicos y procesables, o que se benefician de la ayuda, considere la posibilidad de proporcionar también códigos de error.** Los usuarios suelen usar estos códigos de error para buscar información adicional en Internet.
- **Proporcione siempre una descripción de texto del problema y la solución.** No dependa solo del código de error para este fin.

**Incorrecto:**

![captura de pantalla del mensaje: no se puede abrir el archivo ](images/mess-error-image44.png)

En este ejemplo, se usa un código de error como sustituto de un texto de la solución.

- **Asigne un código de error único para cada causa diferente.** Al hacerlo, se evita la solución de problemas.
- **Elija códigos de error que se puedan buscar fácilmente en Internet.** Si usa códigos de 32 bits, utilice una representación hexadecimal con caracteres iniciales "0x" y mayúsculas.

**Correcto:**

1234

0xC0001234

**Incorrecto:**

-1

-67113524

- **Use Mostrar u ocultar detalles para mostrar los códigos de error.** Frase como código de error: <error code> .

![captura de pantalla del mensaje: el programa no se ha inicializado ](images/mess-error-image45.png)

En este ejemplo, se usa un código de error para complementar un mensaje de error que puede beneficiarse de la información adicional.

### <a name="sound"></a>Sonido

- **No acompañe los mensajes de error con un efecto o bip sonoros.** Hacerlo es discordante e innecesario.
  - **Excepción:** Reproducir el efecto de detención del sonido crítico si el problema es crítico para el funcionamiento del equipo y el usuario debe tomar medidas inmediatas para evitar consecuencias graves.

## <a name="text"></a>Texto

**General**

- **Quite el texto redundante.** Busque en los títulos, las instrucciones principales, las instrucciones adicionales, los vínculos de comandos y los botones de confirmación. Por lo general, deje texto completo en las instrucciones y los controles interactivos, y quite cualquier redundancia de los demás lugares.
- **Usar explicaciones centradas en el usuario.** Describa el problema en lo que respecta a las acciones o los objetivos del usuario, no en cuanto a lo insatisfecho con el software. Use el lenguaje que los usuarios de destino entienden y usan. Evite la jerga técnica.

**Incorrecto:**

![captura de pantalla del mensaje: entrada: llamada sincrónica ](images/mess-error-image46.png)

**Correcto:**

![captura de pantalla del mensaje: ocupado al recibir una llamada ](images/mess-error-image47.png)

En estos ejemplos, la versión correcta habla el idioma del usuario, mientras que la versión incorrecta es demasiado técnica.

- **No use las siguientes palabras:**
  - Error: error (use el problema en su lugar)
  - No se pudo (no se puede usar en su lugar)
  - No válido, no válido, malo (usar en su lugar incorrectamente)
  - Anular, eliminar, terminar (usar detener en su lugar)
  - Catastrófico, fatal (usar en su lugar grave)

Estos términos son innecesarios y se oponen al tono de promoción de ventanas. Cuando se [usa correctamente](vis-std-icons.md), el icono de error se comunica de forma suficiente que hay un problema.

**Incorrecto:**

![captura de pantalla del mensaje: Error catastrófico. ](images/mess-error-image48.png)

**Correcto:**

![captura de pantalla del mensaje: la copia de seguridad debe cerrarse a la vez ](images/mess-error-image49.png)

En el ejemplo incorrecto, los términos "catastrófico" y "error" no son necesarios.

- No utilice frases que culpable al usuario o que implique un error del usuario. Evite usar usted y su en la formulación. Aunque la voz activa suele ser preferida, use la voz pasiva cuando el usuario sea el sujeto y pueda sentirse culpable del error si se usara la voz activa.

**Incorrecto:**

![captura de pantalla del mensaje que especificó un inicio de sesión incorrecto ](images/mess-error-image50.png)

**Correcto:**

![captura de pantalla del mensaje: contraseña incorrecta ](images/mess-error-image51.png)

El ejemplo incorrecto culpable al usuario mediante la voz activa.

- **Ser específico.** Evite el uso impreciso de palabras, como un error de sintaxis y una operación no válida. Proporcionan nombres, ubicaciones y valores específicos de los objetos implicados.

**Incorrecto:**

No se encontró el archivo.

El disco está lleno.

Valor fuera del intervalo.

El carácter no es válido.

Dispositivo no disponible.

Estos problemas serían mucho más fáciles de resolver con nombres, ubicaciones y valores específicos.

- **No dé problemas, causas o soluciones posiblemente inprobables en un intento de ser específico.** No proporcione ningún problema, causa o solución a menos que sea probable que sea correcto. Por ejemplo, es mejor decir que se ha producido un error desconocido que algo que probablemente no sea exacto.
- **Evite la palabra ","** excepto en situaciones en las que se pida al usuario que haga algo poco práctico (por ejemplo, en espera) o que el software esté a la culpa de la situación.

**Correcto:**

Espere mientras Windows copia los archivos en el equipo.

- **Use la palabra "lamentad" solo en los mensajes de error que produzcan problemas graves para el usuario** (por ejemplo, la pérdida de datos o la incapacidad de usar el equipo). No se disculpa si el problema se produjo durante el funcionamiento normal del programa (por ejemplo, si el usuario necesita esperar a que se encuentre una conexión de red).

**Correcto:**

Lo sentimos, pero la copia de seguridad de Fabrikam ha detectado un problema irrecuperable y se ha apagado para proteger los archivos del equipo.

- **Consulte los productos con sus nombres cortos.** No utilice nombres de producto completos ni símbolos de marcas comerciales. No incluya el nombre de la empresa a menos que los usuarios asocien el nombre de la empresa con el producto. No incluya números de versión de programa.

**Incorrecto:**

![Captura de pantalla que muestra un mensaje Microsoft Office Outlook "no se puede abrir este elemento". ](images/mess-error-image52.png)

**Correcto:**

![captura de pantalla del mensaje: no se puede abrir este elemento ](images/mess-error-image53.png)

En el ejemplo incorrecto, se usan los nombres completos del producto y los símbolos de marca comercial.

- **Utilice comillas dobles alrededor de los nombres de objeto.** Al hacerlo, se facilita el análisis del texto y se evitan las instrucciones potencialmente embarazosas.
  - **Excepción:** Las rutas de acceso de archivo, direcciones URL y nombres de dominio completos no tienen que estar entre comillas dobles.

**Correcto:**

![captura de pantalla del mensaje: ' mi casa ' no está disponible ](images/mess-error-image54.png)

En este ejemplo, el mensaje de error sería confuso si el nombre del objeto no estuviera entre comillas.

- **Evite iniciar oraciones con nombres de objeto.** Hacerlo suele ser difícil de analizar.
- **No use signos de exclamación ni palabras con todas las letras mayúsculas.** Los signos de exclamación y las mayúsculas hacen que parezca que se Shouting al usuario.

Para obtener más instrucciones y ejemplos, consulte [estilo y tono](text-style-tone.md).

**Títulos**

- **Use el título para identificar el comando o la característica desde la que se originó el error.** Excepciones:
  - Si un error se muestra en muchos comandos diferentes, considere la posibilidad de usar el nombre del programa en su lugar.
  - Si ese título sería redundante o confuso con la instrucción principal, use en su lugar el nombre del programa.
- **No use el título para explicar o resumir el problema** que es el propósito de la instrucción principal.

**Incorrecto:**

![Captura de pantalla que muestra el mensaje "no se puede cambiar el nombre de la nueva carpeta". ](images/mess-error-image55.png)

En este ejemplo, el título se usa incorrectamente para explicar el problema.

- Usar mayúsculas y minúsculas de estilo de título, sin puntuación final.

**Instrucciones principales**

- **Use la instrucción principal para describir el problema en lenguaje claro, sin formato y específico.**
- **Sea conciso usar una sola oración completa.** Reduzca la instrucción principal a la información esencial. Puede dejar el sujeto implícito si es el programa o el usuario. Incluya el motivo del problema si puede hacerlo de manera concisa. Si debe explicar algo más, use una instrucción complementaria.

**Incorrecto:**

![captura de pantalla del mensaje: no se puede instalar la actualización ](images/mess-error-image56.png)

En este ejemplo, el mensaje de error completo se coloca en la instrucción principal, lo que dificulta la lectura.

- **Ser específico si hay objetos implicados, asigne sus nombres.**
- **Evite colocar las rutas de acceso de archivo completas y las direcciones URL en la instrucción principal.** En su lugar, use un nombre corto (como el nombre de archivo) y coloque el nombre completo (por ejemplo, la ruta de acceso del archivo) en la instrucción complementaria. No obstante, puede colocar una única ruta de acceso de archivo completa o dirección URL en la instrucción principal si el mensaje de error no necesita una instrucción complementaria.

![captura de pantalla del mensaje: no se puede eliminar el archivo Fabrikam ](images/mess-error-image57.png)

En este ejemplo, solo el nombre de archivo está en la instrucción principal. La ruta de acceso completa está en la instrucción complementaria.

- **No proporcione la ruta de acceso y la dirección URL del archivo completo si es obvio en el contexto.**

![captura de pantalla del mensaje: no se puede cambiar el nombre de la nueva carpeta ](images/mess-error-image58.png)

En este ejemplo, el usuario cambia el nombre de un archivo desde el explorador de Windows. En este caso, no se necesita la ruta de acceso completa del archivo porque es obvio en el contexto.

- Use el momento actual siempre que sea posible.
- Use mayúsculas de estilo de frase.
- No incluya los períodos finales si la instrucción es una instrucción. Si la instrucción es una pregunta, incluya un signo de interrogación final.

**Plantillas de instrucciones principales**

Aunque no hay reglas estrictas para la formulación, pruebe a usar las siguientes plantillas de instrucción principales siempre que sea posible:

- [nombre de sujeto opcional] no se puede [realizar acción]
- [nombre de sujeto opcional] no se puede [realizar acción] porque [motivo]
- [nombre de sujeto opcional] no se puede [realizar acción] en "[nombre de objeto]"
- [nombre de sujeto opcional] no se puede [realizar la acción] en "[nombre del objeto]" porque [motivo]
- No hay suficiente [recurso] en [realizar acción]
- [Nombre del firmante] no tiene un [nombre de objeto] necesario para [propósito]
- [Dispositivo o configuración] está desactivado de forma que [resultados no deseados]
- [El dispositivo o el valor] no es [ \| se ha activado la opción disponible \| \| habilitado]
- "[nombre de objeto]" no está disponible actualmente
- El nombre de usuario o la contraseña no son correctos
- No tiene permiso para obtener acceso a "[nombre del objeto]"
- No tiene privilegios para [realizar acción]
- [nombre del programa] ha experimentado un problema grave y debe cerrarse inmediatamente

Por supuesto, realice los cambios necesarios para que la instrucción principal sea gramaticalmente correcta y cumpla con las directrices de instrucciones principales.

**Instrucciones complementarias**

- Use la instrucción complementaria para:
  - Proporcione detalles adicionales sobre el problema.
  - Explique la causa del problema.
  - Enumerar los pasos que el usuario puede realizar para solucionar el problema.
  - Proporcionar medidas para evitar que se reproduzca el problema.
- **Siempre que sea posible, proponga una solución práctica y útil para que los usuarios puedan solucionar el problema.** Sin embargo, asegúrese de que es probable que la solución propuesta resuelva el problema. No malgaste el tiempo de los usuarios al sugerir soluciones posibles, pero improbables.

**Incorrecto:**

![captura de pantalla del mensaje: memoria insuficiente ](images/mess-error-image59.png)

En este ejemplo, aunque es posible el problema y la solución recomendada, son muy poco probables.

- **Si el problema es un valor incorrecto que escribió el usuario, use la instrucción complementaria para explicar los valores correctos.** Los usuarios no deben tener que determinar esta información de otro origen.
- **No proporcione una solución si se puede deducir de la declaración del problema.**

![captura de pantalla del mensaje: valor de hora incorrecto ](images/mess-error-image33.png)

En este ejemplo, no se necesita ninguna instrucción complementaria; la solución se puede deducir de forma trivial a partir de la declaración del problema.

- **Si la solución tiene varios pasos, presente los pasos en el orden en el que deben completarse.** Sin embargo, evite las soluciones de varios pasos, ya que los usuarios tienen dificultades para recordar más de dos o tres pasos sencillos. Si se requieren más pasos, consulte el tema de ayuda correspondiente.
- **Mantenga instrucciones complementarias concisas.** Proporcione solo lo que los usuarios necesitan saber. Omitir detalles innecesarios. Se propone un máximo de tres oraciones de longitud moderada.
- **Para evitar errores mientras los usuarios realizan instrucciones, coloque los resultados antes de la acción.**

**Correcto:**

Para reiniciar Windows, haga clic en Aceptar.

**Incorrecto:**

Haga clic en Aceptar para reiniciar Windows.

En el ejemplo incorrecto, es más probable que los usuarios haga clic en aceptar por accidente.

- **No se recomienda ponerse en contacto con un administrador a menos que lo haga entre las soluciones más probables para el problema.** Reserve estas soluciones para los problemas que realmente solo pueda resolver un administrador.

**Incorrecto:**

![captura de pantalla del mensaje: servidor no disponible ](images/mess-error-image60.png)

En este ejemplo, lo más probable es que el problema esté relacionado con la conexión de red del usuario, por lo que no merece la pena ponerse en contacto con un administrador.

- **No se recomienda ponerse en contacto con el soporte técnico.** La opción para ponerse en contacto con el soporte técnico para solucionar un problema siempre está disponible y no es necesario promocionarla a través de mensajes de error. En su lugar, céntrese en escribir mensajes de error útiles para que los usuarios puedan solucionar problemas sin tener que ponerse en contacto con el soporte técnico.

**Incorrecto:**

![Captura de pantalla que muestra el mensaje "no se puede abrir este elemento". ](images/mess-error-image61.png)

En este ejemplo, el mensaje de error recomienda que se ponga en contacto con el soporte técnico de forma incorrecta.

- Use frases completas, uso de mayúsculas y minúsculas y puntuación final.

**Botones de confirmación**

- Si el mensaje de error proporciona botones de comando o vínculos de comandos que solucionan el problema, siga las directrices correspondientes en los [cuadros de diálogo](win-dialog-box.md).
- Si el programa debe terminar como resultado del error, proporcione un botón salir del programa. Para evitar confusiones, no utilice CLOSE para este fin.
- De lo contrario, proporcione un botón Cerrar. No utilice aceptar para los mensajes de error, porque esto implica que los problemas son correctos.
  - **Excepción:** Use aceptar si el mecanismo de informes de errores tiene etiquetas fijas (como con la API de cuadro de mensajes).

## <a name="documentation"></a>Documentación

Al hacer referencia a errores:

- Consulte los errores mediante su instrucción principal. Si la instrucción principal es larga o detallada, resume.
- Si es necesario, puede hacer referencia a un cuadro de diálogo de mensaje de error como un mensaje. Consulte como un mensaje de error solo en programación y en otra documentación técnica.
- Siempre que sea posible, dé formato al texto con negrita. De lo contrario, coloque el texto entre comillas solo si es necesario para evitar confusiones.

**Ejemplo:** Si recibe un mensaje que **indica que no hay CD en el mensaje de la unidad** , inserte un nuevo CD en la unidad e inténtelo de nuevo.