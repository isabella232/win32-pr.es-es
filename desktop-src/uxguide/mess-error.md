---
title: Mensajes de error (aspectos básicos de diseño)
description: Un mensaje de error alerta a los usuarios de un problema que ya se ha producido.
ms.assetid: b02110e9-985d-4448-9c95-eb958b0059b1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 50e9d945baf736329d38334a94ede6158621167c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984108"
---
# <a name="error-messages-design-basics"></a>Mensajes de error (aspectos básicos de diseño)

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Un mensaje de error alerta a los usuarios de un problema que ya se ha producido. Por el contrario, un mensaje de advertencia alerta a los usuarios de una condición que podría causar un problema en el futuro. Los mensajes de error se pueden presentar mediante cuadros de diálogo modales, mensajes locales, notificaciones o globos.

![captura de pantalla del mensaje de error: no se puede cambiar el nombre](images/mess-error-image1.png)

Mensaje de error modal típico.

Los mensajes de error efectivos informan a los usuarios de que se ha producido un problema, explican por qué se ha producido y proporcionan una solución para que los usuarios puedan corregir el problema. Los usuarios deben realizar una acción o cambiar su comportamiento como resultado de un mensaje de error.

Los mensajes de error bien escritos y útiles son fundamentales para una experiencia de usuario de calidad. Los mensajes de error mal escritos provocan una baja satisfacción del producto y son una causa principal de costos de soporte técnico evitables. Los mensajes de error innecesarios interrumpirán el flujo de los usuarios.

**Nota:** Las directrices relacionadas [con los cuadros de](win-dialog-box.md)diálogo, los mensajes [de](mess-warn.md)advertencia, las [confirmaciones,](vis-std-icons.md)los iconos estándar, las notificaciones y el [diseño](vis-layout.md) se presentan en [artículos](mess-notif.md)independientes. [](mess-confirm.md)

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

Para decidirte, intenta responder a estas preguntas:

- **¿La interfaz de usuario (UI) presenta un problema que ya se ha producido?** Si no es así, el mensaje no es un error. Si el usuario es alertado de una condición que podría causar un problema en el futuro, use un mensaje de advertencia.
- **¿Se puede evitar el problema sin causar confusión?** Si es así, evite el problema en su lugar. Por ejemplo, use controles que estén restringidos a valores válidos en lugar de usar controles sin restricciones que puedan requerir mensajes de error. Además, deshabilitar los controles al hacer clic produciría un error, siempre y cuando sea obvio por qué el control está deshabilitado.
- **¿Se puede corregir el problema automáticamente?** Si es así, controle el problema y suprima el mensaje de error.
- **¿Es probable que los usuarios realicen una acción o cambien su comportamiento como resultado del mensaje?** Si no es así, la condición no justifica interrumpir al usuario, por lo que es mejor suprimir el error.
- **¿Es relevante el problema cuando los usuarios usan activamente otros programas?** Si es así, considere la posibilidad de mostrar el problema mediante un icono [de área de notificación](winenv-notification.md).
- **¿El problema no está relacionado con la actividad del usuario actual, no requiere una acción inmediata del usuario y los usuarios pueden ignorarlo libremente?** Si es así, use una notificación [de error de acción en](mess-notif.md) su lugar.
- **¿El problema se relaciona con el estado de una tarea en segundo plano dentro de una ventana principal?** Si es así, considere la posibilidad de mostrar el problema mediante una [barra de estado](ctrl-status-bars.md).
- **¿Son los principales profesionales de IT de los usuarios de destino?** Si es así, considere la posibilidad de usar un mecanismo de comentarios alternativo, como entradas de [archivo](glossary.md) de registro o alertas por correo electrónico. Los profesionales de TI prefieren encarecidamente los archivos de registro para obtener información no crítica.

## <a name="design-concepts"></a>Conceptos de diseño

**Características de los mensajes de error deficientes**

No debería ser una sorpresa que haya muchos mensajes de error molestos, poco útiles y mal escritos. Y dado que los mensajes de error se presentan a menudo mediante diálogos modales, interrumpen la actividad actual del usuario y exigen que se confirme antes de permitir que el usuario continúe.

Parte del problema es que hay muchas maneras de hacerlo mal. Tenga en cuenta estos ejemplos del Salón de mensajes de error:

**Mensajes de error innecesarios**

**Incorrecto:**

![captura de pantalla del mensaje de error: error en la aplicación ](images/mess-error-image2.png)

Este ejemplo de Windows XP podría ser el peor mensaje de error de la historia. Indica que no se pudo iniciar un programa porque Windows está en proceso de apagado. No hay nada que el usuario pueda hacer al respecto o incluso desea hacer al respecto (el usuario eligió apagar Windows, después de todo). Y al mostrar este mensaje de error, Windows se impide que se apague.

**El problema:** El propio mensaje de error es el problema. Además de descartar el mensaje de error, no hay nada que hacer para los usuarios.

**Causa principal:** Notificar todos los casos de error, independientemente de los objetivos o puntos de vista de los usuarios.

**Alternativa recomendada:** No informe de los errores que a los usuarios no les importan.

**Mensajes de error "Correcto"**

**Incorrecto:**

![captura de pantalla del mensaje de error: error de eliminación ](images/mess-error-image3.png)

Este mensaje de error fue el resultado de que el usuario decidiese no reiniciar Windows inmediatamente después de la eliminación del programa. La eliminación del programa se ha realizado correctamente desde el punto de vista del usuario.

**El problema:** No hay ningún error desde el punto de vista del usuario. Además de descartar el mensaje de error, no hay nada que hacer para los usuarios.

**Causa principal:** La tarea se completó correctamente desde el punto de vista del usuario, pero no se pudo realizar desde el punto de vista del programa de desinstalación.

**Alternativa recomendada:** No informe de errores para condiciones que los usuarios consideren aceptables.

**Mensajes de error completamente inservibles**

**Incorrecto:**

![captura de pantalla del mensaje de error: error desconocido ](images/mess-error-image4.png)

Los usuarios saben que se produjo un error, pero no tienen idea de cuál fue el error ni qué hacer al respecto. Y no, no está bien.

**El problema:** El mensaje de error no da un problema específico y no hay nada que los usuarios puedan hacer al respecto.

**Causa principal:** Lo más probable es que el programa tenga un control de errores deficiente.

**Alternativa recomendada:** Diseñe un buen control de errores en el programa.

**Mensajes de error incomprensibles**

**Incorrecto:**

![captura de pantalla del mensaje de error: copia de seguridad no completada ](images/mess-error-image5.png)

En este ejemplo, la instrucción del problema es clara, pero la explicación complementaria es totalmente desconcertante.

**El problema:** La instrucción del problema o la solución no son incomprensibles.

**Causa principal:** Explicar el problema desde el punto de vista del código en lugar del del usuario.

**Alternativa recomendada:** Escriba texto de mensaje de error que los usuarios de destino puedan comprender fácilmente. Proporcionar soluciones que los usuarios pueden realizar realmente. El diseño de la experiencia de mensajes de error del programa no hace que los programadores escriban mensajes de error sobre el terreno.

**Mensajes de error que sobrecomulcan**

**Incorrecto:**

![captura de pantalla de un mensaje extremadamente detallado ](images/mess-error-image6.png)

En este ejemplo, el mensaje de error intenta explicar cada paso de solución de problemas.

**El problema:** Demasiada información.

**Causa principal:** Dar demasiados detalles o intentar explicar un proceso de solución de problemas complicado dentro de un mensaje de error.

**Alternativa recomendada:** Evite detalles innecesarios. Además, evite los solucionadores de problemas. Si es necesario un solucionador de problemas, céntrate en las soluciones más probables y explica el resto mediante la vinculación al tema adecuado de la Ayuda.

**Mensajes de error innecesariamente duros**

**Incorrecto:**

![captura de pantalla del mensaje: no se encuentra el objeto ](images/mess-error-image7.png)

La incapacidad del programa para encontrar un objeto no parece catastrófica. Y suponiendo que sea catastrófico, ¿por qué está bien la respuesta?

**El problema:** El tono del programa es innecesariamente duro o drástico.

**Causa principal:** El problema se debe a un error que parece catastrófico desde el punto de vista del programa.

**Alternativa recomendada:** Elija el idioma cuidadosamente en función del punto de vista del usuario.

**Mensajes de error que culpan a los usuarios**

**Incorrecto:**

![captura de pantalla del mensaje: carácter no ilegal ](images/mess-error-image8.png)

¿Por qué hacer que los usuarios se sientan como un criminal?

**El problema:** El mensaje de error se indica de forma que se acuse al usuario de realizar un error.

**Causa principal:** Expresiones no sensibles que se centran en el comportamiento del usuario en lugar del problema.

**Alternativa recomendada:** Céntrate en el problema, no en la acción del usuario que condujo al problema, usando la voz pasiva según sea necesario.

**Mensajes de error de advertencia**

**Incorrecto:**

![captura de pantalla del mensaje: error en el informe de errores ](images/mess-error-image9.png)

En este ejemplo, la declaración del problema es bastante irónica y no se proporciona ninguna solución.

**El problema:** Instrucciones de mensaje de error que son inocuas o no sesg.

**Causa principal:** Crear mensajes de error sin prestar atención a su contexto.

**Alternativa recomendada:** Haga que un escritor haya diseñado y revisado los mensajes de error. Tenga en cuenta el contexto y el estado de mente del usuario al revisar los errores.

**Mensajes de error del programador**

**Incorrecto:**

![captura de pantalla del mensaje: dirección de infracción de acceso ](images/mess-error-image10.png)

En este ejemplo, el mensaje de error indica que hay un error en el programa. Este mensaje de error solo tiene significado para el programador.

**El problema:** Los mensajes diseñados para ayudar a los desarrolladores del programa a encontrar errores se quedan en la versión de lanzamiento del programa. Estos mensajes de error no tienen ningún significado ni valor para los usuarios.

**Causa principal:** Los programadores usan la interfaz de usuario normal para hacer mensajes a sí mismos.

**Alternativa recomendada:** Los desarrolladores deben compilar condicionalmente todos estos mensajes para que se quiten automáticamente de la versión de lanzamiento de un producto. No pierda tiempo intentando realizar errores como este comprensibles para los usuarios porque su única audiencia son los programadores.

**Mensajes de error mal presentados**

**Incorrecto:**

![captura de pantalla del mensaje: error inesperado ](images/mess-error-image11.png)

Este ejemplo tiene muchos errores comunes de presentación.

**El problema:** Obtener todos los detalles incorrectos en la presentación del mensaje de error.

**Causa principal:** No conocer ni aplicar las directrices del mensaje de error. No se usan escritores y editores para crear y revisar los mensajes de error.

La naturaleza del control de errores es tal que muchos de estos errores son muy fáciles de realizar. Resulta molesto darse cuenta de que la mayoría de los mensajes de error podrían ser candidatos para el Salón de los Ofitorios.

**Características de los mensajes de error buenos**

A diferencia de los ejemplos de errores anteriores, los mensajes de error buenos tienen:

- **Un problema.** Indica que se ha producido un problema.
- **Una causa.** Explica por qué se produjo el problema.
- **Una solución.** Proporciona una solución para que los usuarios puedan corregir el problema.

Además, los mensajes de error buenos se presentan de una manera que es:

- **Relevante.** El mensaje presenta un problema que preocupa a los usuarios.
- **Procesable.** Los usuarios deben realizar una acción o cambiar su comportamiento como resultado del mensaje.
- **Centrado en el usuario.** El mensaje describe el problema en términos de acciones u objetivos del usuario de destino, no en términos de con qué no está satisfecho el código.
- **Breve.** El mensaje es lo más corto posible, pero no más corto.
- **Claro.** El mensaje usa lenguaje sin formato para que los usuarios de destino puedan comprender fácilmente el problema y la solución.
- **Específico.** El mensaje describe el problema mediante un lenguaje específico, que da nombres, ubicaciones y valores específicos de los objetos implicados.
- **Cortés.** No se debe culpar a los usuarios ni hacer que se sientan cómodos.
- **Raro.** Se muestra con poca frecuencia. Los mensajes de error que se muestran con frecuencia son un signo de diseño no bueno.

Al diseñar la experiencia de control de errores para que tenga estas características, puede mantener los mensajes de error del programa fuera de la Sala de mensajes de error de Alcándalo.

**Evitar mensajes de error innecesarios**

A menudo, el mejor mensaje de error no es ningún mensaje de error. Muchos errores se pueden evitar mediante un mejor diseño y, a menudo, hay mejores alternativas a los mensajes de error. Normalmente es mejor evitar un error que notificar uno.

Los mensajes de error más obvios que se deben evitar son aquellos que no son utilizables. Si es probable que los usuarios descarten el mensaje sin hacer ni cambiar nada, omita el mensaje de error.

Algunos mensajes de error se pueden eliminar porque no son problemas desde el punto de vista del usuario. Por ejemplo, supongamos que el usuario intentó eliminar un archivo que ya está en proceso de eliminación. Aunque este podría ser un caso inesperado desde el punto de vista del código, los usuarios no consideran esto un error porque se logra el resultado deseado.

**Incorrecto:**

![captura de pantalla del mensaje: no se puede eliminar el archivo ](images/mess-error-image12.png)

Este mensaje de error debe eliminarse porque la acción se ha realizado correctamente desde el punto de vista del usuario.

En otro ejemplo, suponga que el usuario cancela explícitamente una tarea. Para el punto de vista del usuario, la siguiente condición no es un error.

**Incorrecto:**

![captura de pantalla del mensaje: no se puede completar la copia de seguridad ](images/mess-error-image13.png)

Este mensaje de error también debe eliminarse porque la acción se ha realizado correctamente desde el punto de vista del usuario.

A veces, los mensajes de error se pueden eliminar al centrarse en los objetivos de los usuarios en lugar de en la tecnología. Al hacerlo, replantee lo que realmente es un error. ¿El problema es con los objetivos del usuario o con la capacidad del programa para satisfacerlos? Si la acción del usuario tiene sentido en el mundo real, también debería tener sentido en el software.

Por ejemplo, supongamos que dentro de un programa de comercio electrónico un usuario intenta encontrar un producto mediante la búsqueda, pero la consulta de búsqueda literal no tiene coincidencias y el producto deseado está agotado. Técnicamente, se trata de un error, pero en lugar de proporcionar un mensaje de error, el programa podría:

- Continúe buscando los productos que coincidan más estrechamente con la consulta.
- Si la búsqueda tiene errores obvios, se recomienda automáticamente una consulta corregida.
- Controle automáticamente problemas comunes, como errores ortográficos, ortografías alternativas y casos de pluralización y verbos no coincidentes.
- Indique cuándo estará en existencias el producto.

Siempre que la solicitud del usuario sea razonable, un programa de comercio electrónico bien diseñado debe devolver resultados razonables, no errores.

Otra excelente manera de evitar los mensajes de error es evitar problemas en primer lugar. Puede evitar errores mediante:

- **Usar controles restringidos.** Use controles restringidos a valores válidos. Controles como listas, controles deslizantes, casillas, botones de radio y selectores de fecha y hora están restringidos a valores válidos, mientras que los cuadros de texto a menudo no son y pueden requerir mensajes de error. Sin embargo, puede restringir los cuadros de texto para que acepten solo determinados caracteres y acepten un número máximo de caracteres.
- **Uso de interacciones restringidas.** Para las operaciones de arrastre, permita que los usuarios coloquen solo en destinos válidos.
- **Usar controles deshabilitados y elementos de menú.** Deshabilite controles y elementos de menú cuando los usuarios puedan deducir fácilmente por qué está deshabilitado el control o el elemento de menú.
- **Proporcionar buenos valores predeterminados.** Es menos probable que los usuarios realicen errores de entrada si pueden aceptar los valores predeterminados. Incluso si los usuarios deciden cambiar el valor, el valor predeterminado permite a los usuarios conocer el formato de entrada esperado.
- **Hacer que las cosas funcionen.** Es menos probable que los usuarios cometen errores si las tareas son innecesarias o se realizan automáticamente para ellos. O bien, si los usuarios cometen pequeños errores, pero su intención es clara, el problema se soluciona automáticamente. Por ejemplo, puede corregir automáticamente problemas de formato menores.

**Proporcionar los mensajes de error necesarios**

A veces es necesario proporcionar un mensaje de error. Los usuarios cometen errores, las redes y los dispositivos dejan de funcionar, los objetos no se pueden encontrar ni modificar, las tareas no se pueden completar y los programas tienen errores. Idealmente, estos problemas se producirían con menos frecuencia, por ejemplo, podemos diseñar nuestro software para evitar muchos tipos de errores de usuario, pero no es realista evitar todos estos problemas. Y cuando se produce uno de estos problemas, un mensaje de error útil pone a los usuarios de nuevo en pie rápidamente.

Una idea común es que los mensajes de error son la peor experiencia del usuario y se deben evitar a toda costa, pero es más preciso decir que la confusión del usuario es la peor experiencia y debe evitarse a toda costa. A veces, ese costo es un mensaje de error útil.

Considere la posibilidad de usar controles deshabilitados. La mayoría de las veces, es obvio por qué un control está deshabilitado, por lo que deshabilitar el control es una excelente manera de evitar un mensaje de error. Sin embargo, ¿qué ocurre si el motivo por el que un control está deshabilitado no es obvio? El usuario no puede continuar y no hay comentarios para determinar el problema. Ahora el usuario está atascado y tiene que deducir el problema u obtener soporte técnico. En tales casos, es mucho mejor dejar el control habilitado y proporcionar un mensaje de error útil en su lugar.

**Incorrecto:**

![captura de pantalla del mensaje: ¿dónde guardar la copia de seguridad? ](images/mess-error-image14.png)

¿Por qué el botón Siguiente está deshabilitado aquí? Es mejor dejarla habilitada y evitar la confusión del usuario al dar un mensaje de error útil.

Si no está seguro de si debe proporcionar un mensaje de error, empiece por crear el mensaje de error que podría proporcionar. Si es probable que los usuarios realicen una acción o cambien su comportamiento como resultado, proporcione el mensaje de error. Por el contrario, si es probable que los usuarios descarten el mensaje sin hacer ni cambiar nada, omita el mensaje de error.

**Diseño para un buen control de errores**

Aunque crear texto de mensaje de error bueno puede ser un desafío, a veces es imposible sin una buena compatibilidad con el control de errores del programa. Considere este mensaje de error:

**Incorrecto:**

![captura de pantalla del mensaje: error desconocido ](images/mess-error-image15.png)

Lo más probable es que el problema se desconocía porque falta compatibilidad con el control de errores del programa.

Aunque es posible que se trata de un mensaje de error muy mal escrito, es más probable que refleje la falta de un buen control de errores por parte del código subyacente, no hay información específica conocida sobre el problema.

Para crear mensajes de error específicos, útiles y centrados en el usuario, el código de control de errores del programa debe proporcionar información de error específica de alto nivel:

- Cada problema debe tener asignado un código de error único.
- Si un problema tiene varias causas, el programa debe determinar la causa específica siempre que sea posible.
- Si el problema tiene parámetros, se deben mantener.
- Los problemas de bajo nivel se deben controlar en un nivel lo suficientemente alto para que el mensaje de error se pueda presentar desde el punto de vista del usuario.

Los mensajes de error buenos no son solo un problema de interfaz de usuario, son un problema de diseño de software. Una buena experiencia de mensaje de error no es algo que se pueda encontrar más adelante.

**Solución de problemas (y cómo evitarlo)**

La solución de problemas se produce cuando se notifica un problema con varias causas diferentes con un único mensaje de error.

**Incorrecto:**

![diagrama de un mensaje que indica tres causas ](images/mess-error-image16.png)

**Correcto:**

![diagrama de tres mensajes que indican una causa cada uno](images/mess-error-image17.png)

Solución de problemas de resultados cuando se notifican varios problemas con un único mensaje de error.

En el ejemplo siguiente, no se pudo mover un elemento porque ya se movió o eliminó, o se denegó el acceso. Si el programa puede determinar fácilmente la causa, ¿por qué poner la carga en el usuario para determinar la causa específica?

**Incorrecto:**

![captura de pantalla del mensaje que indica dos causas ](images/mess-error-image18.png)

¿Cuál es? Ahora el usuario tiene que solucionar problemas.

El programa puede determinar si se denegó el acceso, por lo que este problema debe enviarse con un mensaje de error específico.

**Correcto:**

![captura de pantalla del mensaje que indica una causa ](images/mess-error-image19.png)

Con una causa específica, no se requiere ninguna solución de problemas.

Use mensajes con varias causas solo cuando no se pueda determinar la causa específica. En este ejemplo, sería difícil para el programa determinar si el elemento se movió o eliminó, por lo que aquí se podría usar un único mensaje de error con varias causas. Sin embargo, es poco probable que los usuarios se preocupen si, por ejemplo, no pudieron mover un archivo eliminado. Para estas causas, el mensaje de error ni siquiera es necesario.

**Control de errores desconocidos**

En algunos casos, no sabrá realmente el problema, la causa o la solución. Si sería imprudente suprimir el error, es mejor estar al tanto de la falta de información que presentar problemas, causas o soluciones que podrían no ser correctos.

Por ejemplo, si el programa tiene una excepción no controlada, el siguiente mensaje de error es adecuado:

![captura de pantalla del mensaje: error desconocido ](images/mess-error-image20.png)

Si no puede suprimir un error desconocido, es mejor estar al tanto de la falta de información.

Por otro lado, proporcione información específica y útil si es probable que sea útil la mayor parte del tiempo.

![Captura de pantalla que muestra Office Communicator mensaje "servidor no disponible". ](images/mess-error-image21.png)

Este mensaje de error es adecuado para un error desconocido si la conectividad de red suele ser el problema.

**Determinar el tipo de mensaje adecuado**

Algunos problemas se pueden presentar como un error, una advertencia o información, en función del énfasis y la expresión. Por ejemplo, suponga que una página web no puede cargar un control de ActiveX sin signo en función de la configuración Windows Internet Explorer actual:

- **Error.** "Esta página no puede cargar un control ActiveX sin signo". (Se describe como un problema existente).
- **Advertencia.** "Es posible que esta página no se comporte según lo previsto porque Windows Internet Explorer no está configurado para cargar controles ActiveX sin signo". o "Permitir que esta página instale un control de ActiveX sin signo? Si lo hace desde orígenes que no son de confianza, puede dañar el equipo". (Ambos con frases como condiciones que pueden causar problemas futuros).
- **Información.** "Ha configurado Windows Internet Explorer para bloquear los controles de ActiveX sin signo". (Con frases como una instrucción de hechos).

**Para determinar el tipo de mensaje adecuado, céntrate en el aspecto más importante del problema sobre el que los usuarios necesitan conocer o actuar.** Normalmente, si un problema impide que el usuario se ejecute, debe presentarlo como un error; si el usuario puede continuar, presentarlo como una advertencia. Crear la [instrucción principal u](text-ui.md) otro texto correspondiente en función de ese foco y, a continuación, elija un icono (estándar o de otro tipo) que coincida con el texto.[](vis-std-icons.md) El texto de la instrucción principal y los iconos siempre deben coincidir.

**Presentación de mensajes de error**

La mayoría de los mensajes de error Windows programas se presentan mediante cuadros de diálogo modales (como la mayoría de los ejemplos de este artículo), pero hay otras opciones:

- In situ
- Globos
- Notificaciones
- Iconos del área de notificación
- Barras de estado
- Archivos de registro (para errores dirigidos a profesionales de TI)

Colocar mensajes de error en cuadros de diálogo modales tiene la ventaja de exigir la atención y el reconocimiento inmediatos del usuario. Sin embargo, este también es su principal inconveniente si esa atención no es necesaria.

![captura de pantalla del mensaje: detener lo que está haciendo ](images/mess-error-image22.png)

¿Realmente necesita interrumpir a los usuarios para que puedan hacer clic en el botón Cerrar? Si no es así, considere alternativas al uso de un cuadro de diálogo modal.

Los diálogos modales son una excelente opción cuando el usuario debe reconocer el problema inmediatamente antes de continuar, pero a menudo es una opción deficiente en caso contrario. Por lo general, debe preferir usar la presentación más ligera que hace bien el trabajo.

**Evitar la comunicación en exceso**

Por lo general, [los usuarios no leen, analizan](vis-layout.md). Cuanto más texto haya, más difícil será examinar el texto y más probable es que los usuarios no lean el texto. Como resultado, es importante reducir el texto a sus aspectos esenciales y usar la divulgación progresiva y los vínculos de Ayuda cuando sea necesario para proporcionar información adicional.

Hay muchos ejemplos extremos, pero veamos uno más típico. En el ejemplo siguiente se tienen la mayoría de los atributos de un mensaje de error bueno, pero su texto no es conciso y requiere motivación para leer.

**Incorrecto:**

![captura de pantalla del mensaje detallado ](images/mess-error-image23.png)

Este ejemplo es un buen mensaje de error, pero se sobrecomulca.

¿Qué dice realmente todo este texto? Algo como esto:

**Correcto:**

![captura de pantalla del mensaje: cd recorder not detected ](images/mess-error-image24.png)

Este mensaje de error tiene esencialmente la misma información, pero es mucho más conciso.

Al usar la Ayuda para proporcionar los detalles, este mensaje de error tiene un [estilo piramidal invertido](text-ui.md) de presentación.

Para obtener más instrucciones y ejemplos sobre la comunicación en exceso, vea [Interfaz de usuario Text](text-ui.md).

**Si solo hace ocho cosas**

1. Diseñe el programa para el control de errores.
2. No dé mensajes de error innecesarios.
3. Evite la confusión del usuario mediante la entrega de los mensajes de error necesarios.
4. Asegúrese de que el mensaje de error proporciona un problema, una causa y una solución.
5. Asegúrese de que el mensaje de error sea pertinente, que sea acción, breve, claro, específico, corteso y poco frecuente.
6. Diseñe mensajes de error desde el punto de vista del usuario, no desde el punto de vista del programa.
7. Evite implicar al usuario en la solución de problemas y use un mensaje de error diferente para cada causa detectable.
8. Use el método de presentación más ligero que hace bien el trabajo.

**Patrones de uso**

Los mensajes de error tienen varios patrones de uso:


| Etiqueta | Value |
|--------|-------|
| <strong>Problemas del sistema</strong><br /> El sistema operativo, el dispositivo de hardware, la red o el programa han dado error o no están en el estado necesario para realizar una tarea. <br /> | El usuario puede resolver muchos problemas del sistema: <br /><ul><li>Los problemas del dispositivo se pueden resolver mediante la activación del dispositivo, la reconexión del dispositivo y la inserción de medios.</li><li>Los problemas de red se pueden resolver comprobando la conexión de red física y ejecutando <strong>Diagnóstico y reparación de red.</strong></li><li>Los problemas del programa se pueden resolver cambiando las opciones del programa o reiniciando el programa.</li></ul><img src="images/mess-error-image25.png" alt="Screen shot of message: Can't find a camera " /><br /> En este ejemplo, el programa no encuentra una cámara para realizar una tarea de usuario.<br /><img src="images/mess-error-image26.png" alt="Screen shot of message Network discovery off " /><br /> En este ejemplo, debe estar activada una característica necesaria para realizar una tarea.<br /> | 
| <strong>Problemas de archivos</strong><br /> No se encontró un archivo o carpeta necesario para una tarea iniciada por el usuario, ya está en uso o no tiene el formato esperado. <br /> | <img src="images/mess-error-image27.png" alt="Screen shot of message: Can't delete file " /><br /> En este ejemplo, no se puede eliminar el archivo o la carpeta porque no se encontró.<br /><img src="images/mess-error-image28.png" alt="Screen shot of message: Can't play this file " /><br /> En este ejemplo, el programa no admite el formato de archivo especificado.<br /> | 
| <strong>Problemas de seguridad</strong><br /> El usuario no tiene permiso para acceder a un recurso ni privilegios suficientes para realizar una tarea iniciada por el usuario. <br /> | <img src="images/mess-error-image29.png" alt="Screen shot of message: You don't have permission " /><br /> En este ejemplo, el usuario no tiene permiso para acceder a un recurso.<br /><img src="images/mess-error-image30.png" alt="Screen shot of message: You don't have privilege " /><br /> En este ejemplo, el usuario no tiene el privilegio de realizar una tarea.<br /> | 
| <strong>Problemas de tareas</strong><br /> Hay un problema específico al realizar una tarea iniciada por el usuario (que no sea un sistema, un archivo no encontrado, un formato de archivo o un problema de seguridad). <br /> | <img src="images/mess-error-image31.png" alt="Screen shot of message: Data can't be pasted " /><br /> En este ejemplo, los datos del Portapapeles no se pueden pegar en Paint.<br /><img src="images/mess-error-image32.png" alt="Screen shot of message: Upgrade can't be installed " /><br /> En este ejemplo, el usuario no puede instalar una actualización de software.<br /> | 
| <strong>Problemas de entrada del usuario</strong><br /> El usuario escribió un valor incorrecto o incoherente con otra entrada de usuario. <br /> | <img src="images/mess-error-image33.png" alt="Screen shot of message: Incorrect time value " /><br /> En este ejemplo, el usuario escribió un valor de hora incorrecto.<br /><img src="images/mess-error-image34.png" alt="Screen shot of message: Incorrect input format " /><br /> En este ejemplo, la entrada del usuario no tiene el formato correcto.<br /> | 


## <a name="guidelines"></a>Directrices

### <a name="presentation"></a>Presentación

- **Use los diálogos de tareas siempre que sea necesario** para lograr una apariencia y un diseño coherentes. Los diálogos de tareas Windows Vista o versiones posteriores, por lo que no son adecuados para versiones anteriores de Windows. Si debe usar un cuadro de mensaje, separe la instrucción principal de la instrucción complementaria con dos saltos de línea.

### <a name="user-input-errors"></a>Errores de entrada del usuario

- **Siempre que sea posible, evite o reduzca los errores de entrada del usuario mediante:**
  - Usar controles que están restringidos a valores válidos.
  - Al deshabilitar los controles y los elementos de menú al hacer clic, se produciría un error, siempre que sea obvio por qué se deshabilita el control o el elemento de menú.
  - Proporcionar buenos valores predeterminados.

**Incorrecto:**

![captura de pantalla del cuadro de texto con la etiqueta de volumen del hablante ](images/mess-error-image35.png)

En este ejemplo, se usa un cuadro de texto sin restricciones para la entrada restringida. En su lugar, use un control deslizante.

- **Use el control de errores modelados (errores en contexto o globos) para problemas contextuales de entrada del usuario.**
- **Use globos para problemas de entrada** de usuario de un solo punto no críticos detectados en un cuadro de texto o inmediatamente después de que un cuadro de texto pierda el foco. [Los globos](https://msdn.microsoft.com/library/windows/desktop/aa511451.aspx) no requieren espacio disponible en la pantalla ni el diseño dinámico necesario para mostrar los mensajes locales. Mostrar solo un globo a la vez. Dado que el problema no es crítico, no se necesita ningún icono de error. Los globos desaparecen cuando se hace clic en él, cuando se resuelve el problema o después de un tiempo de espera.

![captura de pantalla del mensaje: carácter incorrecto ](images/mess-error-image36.png)

En este ejemplo, un globo indica un problema de entrada mientras sigue en el control .

- **Use errores en el lugar para la detección de errores retrasada,** normalmente errores encontrados al hacer clic en un botón de confirmación. (No use errores [en el lugar para](glossary.md) las configuraciones que se confirman inmediatamente). Puede haber varios errores en el lugar a la vez. Use texto normal y un icono de error de 16 x 16 píxeles, colocándolos directamente junto al problema siempre que sea posible. Los errores en el lugar no desaparecen a menos que el usuario se confirme y no se encuentran otros errores.

![captura de pantalla del mensaje: dirección de correo electrónico incorrecta ](images/mess-error-image37.png)

En este ejemplo, se usa un error local para un error encontrado al hacer clic en el botón confirmar.

- Use el control modal de **errores (cuadros** de diálogo de tareas o cuadros de mensaje) para todos los demás problemas, incluidos los errores que implican varios controles o son errores no contextuales o que no son de entrada encontrados al hacer clic en un botón confirmar.
- **Cuando se notifica un problema de entrada del usuario, establezca el foco de entrada en el primer control con los datos incorrectos.** Desplácese por el control en la vista si es necesario. Si el control es un cuadro de texto, seleccione todo el contenido. Siempre debe ser obvio a qué se refiere el mensaje de error.
- **No borre la entrada incorrecta.** En su lugar, déjelo para que el usuario pueda ver y corregir el problema sin empezar de nuevo.
  - **Excepción:** Borre los cuadros de texto de contraseña y PIN incorrectos porque los usuarios no pueden corregir la entrada enmascarada de forma eficaz.

### <a name="troubleshooting"></a>Solución de problemas

- **Evite crear problemas de solución de problemas.** No se base en un único mensaje de error para notificar un problema con varias causas detectables diferentes.
- **Use un mensaje de error diferente (normalmente una instrucción complementaria diferente) para cada causa detectable.** Por ejemplo, si un archivo no se puede abrir por varios motivos, proporcione una instrucción complementaria independiente por cada motivo.
- **Use un mensaje con varias causas solo cuando no se pueda determinar la causa específica.** En este caso, presente las soluciones en orden de probabilidad de corregir el problema. Esto ayuda a los usuarios a resolver el problema de forma más eficaz.

### <a name="icons"></a>Iconos

- **Los cuadros de diálogo de mensaje de error modal no tienen iconos de barra de título.** Los iconos de la barra de título se usan como una distinción visual entre ventanas principales y secundarias.
- **Use un icono de error.** Excepciones:
  - Si el error es un problema de entrada del usuario que se muestra mediante un cuadro de diálogo modal o un globo, no use un icono. Esto es contrario al tono alentador de Windows. Sin embargo, los mensajes de error en su lugar deben usar un pequeño icono de error (16 x 16 píxeles) para identificarlos claramente como mensajes de error.

     ![captura de pantalla del formato postal incorrecto del mensaje](images/mess-error-image38.png)

     ![captura de pantalla del nombre del equipo del mensaje demasiado largo](images/mess-error-image39.png)

     En estos ejemplos, los problemas de entrada del usuario no necesitan iconos de error.

     ![captura de pantalla del formato incorrecto del número de teléfono del mensaje](images/mess-error-image40.png)

     En este ejemplo, un mensaje de error local necesita un pequeño icono de error para identificarlo claramente como un mensaje de error.

- Si el problema es para una característica que tiene un icono (y no un problema de entrada del usuario), puede usar el icono de característica con una superposición de errores. Si lo hace, use también el nombre de la característica como asunto del error.

    ![el reproductor multimedia de mensajes de captura de pantalla no puede reproducir el archivo ](images/mess-error-image41.png)

    En este ejemplo, el icono de característica tiene una superposición de errores y la característica es el sujeto del error.

- **No use iconos de advertencia para errores.** Esto suele hacerse para que la presentación se sienta menos grave. Los errores no son advertencias.

    **Incorrecto:**

    ![captura de pantalla del cambio rápido de mensajes no habilitado ](images/mess-error-image42.png)

    En este ejemplo, se usa incorrectamente un icono de advertencia para que el error se sienta menos grave.

Para obtener más instrucciones y ejemplos, vea [Iconos estándar.](vis-std-icons.md)

### <a name="progressive-disclosure"></a>Muestra progresiva

- **Use un botón Mostrar u ocultar detalles de divulgación progresiva para ocultar información avanzada o detallada en un mensaje de error.** Si lo hace, se simplifica el mensaje de error para el uso típico. No oculte la información necesaria, ya que es posible que los usuarios no la encuentren.

![captura de pantalla del mensaje: activesync no puede iniciar sesión ](images/mess-error-image43.png)

En este ejemplo, el botón de divulgación progresiva ayuda a los usuarios a explorar en profundidad si lo desean, o simplificar la interfaz de usuario si no lo hacen.

- **No use Mostrar u ocultar detalles a menos que realmente haya más detalles.** No solo vuelva a establecer la información existente en un formato más detallado.
- **No use Mostrar u ocultar detalles para mostrar la información de ayuda.** En su lugar, use vínculos de Ayuda.

Para obtener instrucciones de etiquetado, vea [Controles de divulgación progresiva.](ctrl-progressive-disclosure-controls.md)

**No volver a mostrar este mensaje**

- **Si un mensaje de error necesita esta opción, replantee el error y su frecuencia.** Si tiene todas las características de un error bueno (relevante, manejable e infrecuente), no debería tener sentido que los usuarios lo suprimiesen.

Para obtener más instrucciones, vea [Cuadros de diálogo](win-dialog-box.md).

### <a name="default-values"></a>Valores predeterminados

- **Seleccione la respuesta más segura, menos destructiva o más segura para que sea la predeterminada.** Si la seguridad no es un factor, seleccione el comando más probable o conveniente.

### <a name="help"></a>Ayuda

- **Diseñe mensajes de error para evitar la necesidad de ayuda.** Normalmente, los usuarios no deben tener que leer texto externo para comprender y resolver el problema, a menos que la solución requiera varios pasos.
- **Asegúrese de que el contenido de la Ayuda es pertinente y útil.** No debe ser una nueva declaración detallada del mensaje de error, sino que debe contener información útil que esté fuera del ámbito del mensaje de error, como formas de evitar el problema en el futuro. No proporcione un vínculo de Ayuda solo porque puede.
- **Use vínculos de Ayuda específicos, concisos y pertinentes para acceder al contenido de la Ayuda.** No use botones de comando ni divulgación progresiva para este propósito.
- **Para los mensajes de error que no se pueden hacer específicos y útiles, considere la posibilidad de proporcionar vínculos al contenido de la Ayuda en línea.** Al hacerlo, puede proporcionar a los usuarios información adicional que puede actualizar una vez publicado el programa.

Para obtener más instrucciones, vea [Ayuda de](winenv-help.md).

### <a name="error-codes"></a>Códigos de error

- **En el caso de los mensajes de error que no puede hacer específicos y que puedan actuar o que se beneficien de la Ayuda, considere también la posibilidad de proporcionar códigos de error.** Los usuarios suelen usar estos códigos de error para buscar información adicional en Internet.
- **Proporcione siempre una descripción de texto del problema y la solución.** No dependa solo del código de error para este propósito.

**Incorrecto:**

![captura de pantalla del mensaje: no se puede abrir el archivo ](images/mess-error-image44.png)

En este ejemplo, se usa un código de error como sustituto de un texto de solución.

- **Asigne un código de error único para cada causa diferente.** Al hacerlo, se evita la solución de problemas.
- **Elija códigos de error que se puedan buscar fácilmente en Internet.** Si usa códigos de 32 bits, use una representación hexadecimal con un carácter "0x" inicial y caracteres en mayúsculas.

**Correcto:**

1234

0xC0001234

**Incorrecto:**

-1

-67113524

- **Use Mostrar u ocultar detalles para mostrar los códigos de error.** Frase como código de error: <error code> .

![captura de pantalla del mensaje: el programa no se inicializó ](images/mess-error-image45.png)

En este ejemplo, se usa un código de error para complementar un mensaje de error que puede beneficiarse de más información.

### <a name="sound"></a>Sonido

- **No acompaña los mensajes de error con un efecto de sonido o un sonido.** Hacerlo es jarring e innecesario.
  - **Excepción:** Reproducir el efecto de sonido Crítico detener si el problema es crítico para el funcionamiento del equipo y el usuario debe tomar medidas inmediatas para evitar consecuencias graves.

## <a name="text"></a>Texto

**General**

- **Quite el texto redundante.** Puede buscarlo en títulos, instrucciones principales, instrucciones complementarias, vínculos de comandos y botones de confirmación. Por lo general, deje texto completo en instrucciones y controles interactivos y quite cualquier redundancia de los demás lugares.
- **Use explicaciones centradas en el usuario.** Describa el problema en términos de acciones u objetivos del usuario, no en términos de lo que el software no tiene que ver. Use el lenguaje que los usuarios de destino entiendan y usen. Evite la jerga técnica.

**Incorrecto:**

![captura de pantalla del mensaje: llamada sincrónica de entrada ](images/mess-error-image46.png)

**Correcto:**

![captura de pantalla del mensaje: ocupado al recibir una llamada ](images/mess-error-image47.png)

En estos ejemplos, la versión correcta habla el idioma del usuario, mientras que la versión incorrecta es muy técnica.

- **No use las siguientes palabras:**
  - Error, error (use el problema en su lugar)
  - No se pudo (no se puede usar en su lugar)
  - No válido, no válido, incorrecto (use incorrecto en su lugar)
  - Abort, kill, terminate (use stop en su lugar)
  - Catastrófico, grave (use grave en su lugar)

Estos términos son innecesarios y contrarios al tono alentador de Windows. Cuando [se usa correctamente,](vis-std-icons.md)el icono de error comunica lo suficiente que hay un problema.

**Incorrecto:**

![captura de pantalla del mensaje: error catastrófico. ](images/mess-error-image48.png)

**Correcto:**

![captura de pantalla del mensaje: la copia de seguridad debe cerrarse a la vez ](images/mess-error-image49.png)

En el ejemplo incorrecto, los términos "catastrófico" y "error" no son necesarios.

- No use expresiones que culpan al usuario o implican un error del usuario. Evite usar usted y su en las expresiones. Aunque generalmente se prefiere la voz activa, use la voz pasiva cuando el usuario sea el sujeto y podría sentirse responsable del error si se usó la voz activa.

**Incorrecto:**

![captura de pantalla del mensaje que escribió en un inicio de sesión incorrecto ](images/mess-error-image50.png)

**Correcto:**

![captura de pantalla del mensaje: contraseña incorrecta ](images/mess-error-image51.png)

El ejemplo incorrecto culpa al usuario mediante la voz activa.

- **Ser específico.** Evite palabras imprecisas, como errores de sintaxis y operaciones no válidas. Proporcione nombres, ubicaciones y valores específicos de los objetos implicados.

**Incorrecto:**

No se encontró el archivo.

El disco está lleno.

Valor fuera del intervalo.

El carácter no es válido.

El dispositivo no está disponible.

Estos problemas serían mucho más fáciles de resolver con nombres, ubicaciones y valores específicos.

- **No dé posibles problemas, causas o soluciones improbables en un intento de ser específicos.** No proporcione un problema, una causa o una solución, a menos que sea probable que sea correcto. Por ejemplo, es mejor decir que se produjo un error desconocido que algo que es probable que sea inexacto.
- **Evite la palabra "please",** excepto en situaciones en las que se pide al usuario que haga algo inconveniente (por ejemplo, esperar) o el software sea el responsable de la situación.

**Correcto:**

Espere mientras Windows copia los archivos en el equipo.

- **Use la palabra "sorry"** solo en los mensajes de error que resulte en problemas graves para el usuario (por ejemplo, pérdida de datos o incapacidad de usar el equipo). No se preocupe si el problema se produjo durante el funcionamiento normal del programa (por ejemplo, si el usuario necesita esperar a que se encuentra una conexión de red).

**Correcto:**

Lo sentimos, pero Fabrikam Backup detectó un problema irrecuperable y se cerró para proteger los archivos del equipo.

- **Consulte los productos con sus nombres cortos.** No use nombres completos de productos ni símbolos de marca comercial. No incluya el nombre de la empresa a menos que los usuarios asocie el nombre de la empresa con el producto. No incluya números de versión del programa.

**Incorrecto:**

![Captura de pantalla que muestra Microsoft Office Outlook mensaje "No se puede abrir este elemento". ](images/mess-error-image52.png)

**Correcto:**

![captura de pantalla del mensaje: no se puede abrir este elemento ](images/mess-error-image53.png)

En el ejemplo incorrecto, se usan nombres completos de productos y símbolos de marca comercial.

- **Use comillas dobles alrededor de los nombres de objeto.** Esto facilita el análisis del texto y evita instrucciones potencialmente embarazosas.
  - **Excepción:** No es necesario que las rutas de acceso de archivo, las direcciones URL y los nombres de dominio completos entre comillas dobles.

**Correcto:**

![captura de pantalla del mensaje: "Mi casa" no está disponible ](images/mess-error-image54.png)

En este ejemplo, el mensaje de error sería confuso si el nombre del objeto no estuviera entre comillas.

- **Evite iniciar oraciones con nombres de objeto.** Esto suele ser difícil de analizar.
- **No use signos de exclamación ni palabras con todas las letras mayúsculas.** Los signos de exclamación y las letras mayúsculas hacen que se sienta como si fuera a mirar al usuario.

Para obtener más instrucciones y ejemplos, vea [Estilo y tono](text-style-tone.md).

**Títulos**

- **Use el título para identificar el comando o la característica desde la que se originó el error.** Excepciones:
  - Si muchos comandos diferentes muestran un error, considere la posibilidad de usar el nombre del programa en su lugar.
  - Si ese título sería redundante o confuso con la instrucción principal, use el nombre del programa en su lugar.
- **No use el título para explicar o resumir el problema** que es el propósito de la instrucción principal.

**Incorrecto:**

![Captura de pantalla que muestra el mensaje "No se puede cambiar el nombre de la nueva carpeta". ](images/mess-error-image55.png)

En este ejemplo, el título se usa incorrectamente para explicar el problema.

- Use mayúsculas de estilo de título, sin terminar los signos de puntuación.

**Instrucciones principales**

- **Use la instrucción principal para describir el problema en un lenguaje claro, sin formato y específico.**
- **Sea conciso y use solo una sola oración completa.** Pare la instrucción principal hasta la información esencial. Puede dejar implícito el asunto si es el programa o el usuario. Incluya el motivo del problema si puede hacerlo de forma concisa. Si tiene que explicar algo más, use una instrucción complementaria.

**Incorrecto:**

![captura de pantalla del mensaje: no se puede instalar la actualización ](images/mess-error-image56.png)

En este ejemplo, todo el mensaje de error se coloca en la instrucción principal, lo que hace que sea difícil de leer.

- **Sea específico si hay objetos implicados, así como sus nombres.**
- **Evite colocar rutas de acceso de archivo completas y direcciones URL en la instrucción principal.** En su lugar, use un nombre corto (como el nombre de archivo) y coloque el nombre completo (como la ruta de acceso del archivo) en la instrucción complementaria. Sin embargo, puede colocar una única ruta de acceso completa o una dirección URL en la instrucción principal si el mensaje de error no necesita una instrucción complementaria.

![captura de pantalla del mensaje: no se puede eliminar el archivo fabrikam ](images/mess-error-image57.png)

En este ejemplo, solo el nombre de archivo está en la instrucción principal. La ruta de acceso completa está en la instrucción complementaria.

- **No dé la ruta de acceso completa al archivo y la dirección URL si es obvio desde el contexto.**

![captura de pantalla del mensaje: no se puede cambiar el nombre de la nueva carpeta ](images/mess-error-image58.png)

En este ejemplo, el usuario va a cambiar el nombre de un archivo desde Windows Explorer. En este caso, la ruta de acceso completa del archivo no es necesaria porque es obvia desde el contexto.

- Use el tiempo presente siempre que sea posible.
- Use mayúsculas de estilo de frase.
- No incluya períodos finales si la instrucción es una instrucción . Si la instrucción es una pregunta, incluya un signo de interrogación final.

**Plantillas de instrucciones principales**

Aunque no hay reglas estrictas para la expresión, pruebe a usar las siguientes plantillas de instrucciones principales siempre que sea posible:

- [nombre de sujeto opcional] no puede [realizar acción]
- [nombre de sujeto opcional] no puede [realizar acción] porque [motivo]
- [nombre de sujeto opcional] no puede [realizar acción] a "[nombre de objeto]"
- [nombre de sujeto opcional] no puede [realizar la acción] a "[nombre de objeto]" porque [motivo]
- No hay suficiente [recurso] para [realizar la acción]
- [Nombre del sujeto] no tiene un [nombre de objeto] necesario para [propósito]
- [Dispositivo o configuración] está desactivado para que [resultados no deseados]
- [Dispositivo o configuración] no está [disponible \| \| activado \| habilitado]
- "[nombre de objeto]" no está disponible actualmente
- El nombre de usuario o la contraseña son incorrectos
- No tiene permiso para acceder a "[nombre de objeto]"
- No tiene privilegios para [realizar la acción].
- [nombre del programa] ha experimentado un problema grave y debe cerrarse inmediatamente.

Por supuesto, realice los cambios necesarios para que la instrucción principal sea gramaticalmente correcta y cumpla las instrucciones principales.

**Instrucciones complementarias**

- Use la instrucción complementaria para:
  - Proporcionar detalles adicionales sobre el problema.
  - Explicar la causa del problema.
  - Enumera los pasos que el usuario puede seguir para corregir el problema.
  - Proporcione medidas para evitar que el problema vuelva a producirse.
- **Siempre que sea posible, proponga una solución práctica y útil para que los usuarios puedan corregir el problema.** Sin embargo, asegúrese de que es probable que la solución propuesta resuelva el problema. No pierda el tiempo de los usuarios al sugerir soluciones posibles, pero improbables.

**Incorrecto:**

![captura de pantalla del mensaje: memoria sin memoria ](images/mess-error-image59.png)

En este ejemplo, aunque el problema y su solución recomendada son posibles, son muy poco probables.

- **Si el problema es un valor incorrecto especificado por el usuario, use la instrucción complementaria para explicar los valores correctos.** Los usuarios no deben tener que determinar esta información desde otro origen.
- **No proporcione una solución si se puede deducir trivialmente de la instrucción del problema.**

![captura de pantalla del mensaje: valor de hora incorrecto ](images/mess-error-image33.png)

En este ejemplo, no se necesita ninguna instrucción complementaria; la solución se puede deducir trivialmente de la instrucción del problema.

- **Si la solución tiene varios pasos, presente los pasos en el orden en que deben completarse.** Sin embargo, evite las soluciones de varios pasos porque los usuarios tienen dificultades para recordar más de dos o tres pasos sencillos. Si se requieren más pasos, consulte el tema de Ayuda adecuado.
- **Mantenga las instrucciones complementarias concisas.** Proporcione solo lo que los usuarios necesitan saber. Omita los detalles innecesarios. Apunta a un máximo de tres oraciones de longitud moderada.
- **Para evitar errores mientras los usuarios realizan instrucciones, coloque los resultados antes de la acción.**

**Correcto:**

Para reiniciar Windows, haga clic en Aceptar.

**Incorrecto:**

Haga clic en Aceptar para reiniciar Windows.

En el ejemplo incorrecto, es más probable que los usuarios haga clic en Aceptar por accidente.

- **No se recomienda ponerse en contacto con un administrador a menos que lo haga entre las soluciones más probables para el problema.** Reserve estas soluciones para problemas que realmente solo pueda resolver un administrador.

**Incorrecto:**

![captura de pantalla del mensaje: servidor no disponible ](images/mess-error-image60.png)

En este ejemplo, lo más probable es que el problema sea con la conexión de red del usuario, por lo que no merece la pena ponerse en contacto con un administrador.

- **No se recomienda ponerse en contacto con el soporte técnico.** La opción de ponerse en contacto con el soporte técnico para solucionar un problema siempre está disponible y no es necesario promoverla a través de mensajes de error. En su lugar, céntrate en escribir mensajes de error útiles para que los usuarios puedan resolver problemas sin ponerse en contacto con el soporte técnico.

**Incorrecto:**

![Captura de pantalla que muestra el mensaje "No se puede abrir este elemento". ](images/mess-error-image61.png)

En este ejemplo, el mensaje de error recomienda ponerse en contacto incorrectamente con el soporte técnico.

- Use oraciones completas, mayúsculas de estilo oración y signos de puntuación finales.

**Botones de confirmación**

- Si el mensaje de error proporciona botones de comando o vínculos de comandos que solucionan el problema, siga sus respectivas instrucciones en [Cuadros de diálogo](win-dialog-box.md).
- Si el programa debe finalizar como resultado del error, proporcione un botón Salir del programa. Para evitar confusiones, no use Cerrar para este propósito.
- De lo contrario, proporcione un botón Cerrar. No use Aceptar para los mensajes de error, ya que esta redacción implica que los problemas son correctos.
  - **Excepción:** Use Aceptar si el mecanismo de informes de errores tiene etiquetas fijas (como con messagebox API).

## <a name="documentation"></a>Documentación

Al hacer referencia a errores:

- Consulte los errores por su instrucción principal. Si la instrucción principal es larga o detallada, resuma.
- Si es necesario, puede hacer referencia a un cuadro de diálogo de mensaje de error como un mensaje. Consulte como mensaje de error solo en programación y otra documentación técnica.
- Cuando sea posible, formatee el texto con negrita. De lo contrario, coloque el texto entre comillas solo si es necesario para evitar confusiones.

**Ejemplo:** Si recibe un mensaje No hay ningún **disco CD** en la unidad, inserte un nuevo disco CD en la unidad e inténtelo de nuevo.
