---
title: Sonido
description: Sound es el elemento de audio de la experiencia del usuario.
ms.assetid: 2a276370-eff9-4844-b008-eba9ae5ac395
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 664d78d00cf75dae8f43717db07290a26574f0c6
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104555079"
---
# <a name="sound"></a>Sonido

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

*Sound* es el elemento de audio de la experiencia del usuario. Cuando se usa correctamente, el sonido puede ser una forma eficaz de comunicación que establece una relación no verbal e incluso emocional con los usuarios. Los sonidos se pueden usar solos o como complemento de la interfaz de usuario visual. Por ejemplo, la adición de un efecto de sonido a una notificación aumenta la probabilidad de que se detecte, especialmente si el usuario no está viendo la pantalla cuando se produce un evento.

![captura de pantalla del cuadro de diálogo sonido ](images/vis-sound-image1.png)

En la pestaña sonidos del elemento del panel de control sonido, los usuarios pueden realizar cambios en los sonidos del sistema.

En este artículo se describe el uso de sonidos dentro de un programa como respuesta a eventos y acciones del usuario, y la integración del control de sonido de un programa con Windows. No cubre el uso de música o voz.

**Nota:** Las instrucciones relacionadas con las [notificaciones](mess-notif.md) y la [Personalización de marca](exper-branding.md) se presentan en artículos independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

Para decidir si debe utilizar el sonido, tenga en cuenta las siguientes preguntas:

-   **¿Hay un beneficio claro para el uso del sonido?** Dado que los inconvenientes del uso del sonido pueden superar fácilmente las ventajas, use el sonido solo cuando haya una ventaja clara.
-   **¿Es adecuado el uso del sonido?** ¿El uso del sonido es la atención de los elementos que merecen atención? ¿Los usuarios pierden el sonido si no estuvieran? Céntrese en los sonidos que mantienen informados a los usuarios, es probable que cambien su comportamiento o que proporcionen comentarios útiles.
-   **¿Es el uso de distracciones de sonido?** ¿Hay sonidos frecuentes, altos y discordantes? ¿Es probable que los usuarios reduzcan el volumen del sistema o el volumen del programa como resultado del uso del sonido?
-   **¿Está usando sonido como forma principal de comunicación?** En muchos casos, como en el caso de los usuarios que tienen algún nivel de pérdida de audición, el sonido no debe usarse como medio principal de comunicación. El sonido es más eficaz como complemento de otros medios de comunicación (como texto u objetos visuales).
-   **¿Son los profesionales de TI de los usuarios de destino primarios?** El sonido suele ser ineficaz para las tareas destinadas a los profesionales de ti porque muchas de sus tareas se ejecutan en modo desatendido. Además, el sonido no se escala para que Imaginen la ejecución de cientos de tareas a la vez y la obtención de sonidos cuando se completan o se producen errores.

## <a name="design-concepts"></a>Conceptos de diseño

Normalmente, el sonido consigue cualquiera de los siguientes fines o todos ellos:

-   **Notificación.** El sonido puede asociarse a eventos específicos. Por ejemplo, un sonido "nuevo correo" indica a los usuarios cuando el correo llega sin interrumpir su tarea actual.
-   **Los.** El sonido puede proporcionar comentarios para acciones específicas del usuario. Por ejemplo, un sonido sutil que se reproduce cuando se suelta el control deslizante en el control de volumen proporciona comentarios sobre el nivel de la configuración actual.
-   **Marca.** El sonido puede asociarse con contenido específico para la marca del producto, la aplicación o el servicio. Windows usa el sonido de esta manera para el inicio del sistema operativo.
-   **Representación.** El sonido se usa normalmente para mejorar los productos de entretenimiento y para que cualquier producto sea más atractivo. Por ejemplo, la mayoría de juegos, aplicaciones de entrenamiento y productos de consumidor usan sonido para entretener a los usuarios y mejorar su experiencia.

Algunos sonidos pueden cumplir algunos de estos propósitos a la vez. El sonido de inicio de Windows, por ejemplo, indica que el proceso de inicio se ha completado y el escritorio está listo para su uso. También proporciona una forma eficaz de personalización de marca del producto e incluso atrae a los usuarios.

Es probable que se eliminen los sonidos que no cumplen ninguno de estos propósitos.

### <a name="inappropriate-use-of-sound"></a>Uso inadecuado de sonido

**A pesar de las ventajas del sonido, el uso adecuado de los sonidos requiere una restricción importante para hacer que un programa resulte molesto y distraiga.** Los usuarios desactivarán su sonido por completo si se molestan con sonidos frecuentes, repetitivos, de discordante, de interrupción y de diseño deficiente; en parte, esto se debe a que, por su propia naturaleza, el sonido requiere atención y es difícil de ignorar. Para obtener sugerencias sobre cómo encontrar un equilibrio razonable, consulte las [directrices de diseño de sonido](#sound-design).

Dado que los inconvenientes del uso del sonido pueden superar fácilmente las ventajas, use el sonido solo cuando haya una ventaja clara. **En casos de duda, no use sonido.**

### <a name="make-sound-supplemental"></a>Hacer que el sonido sea complementario

Incluso si el sonido se usa correctamente, hay muchas situaciones en las que es posible que el sonido no sea eficaz para todos los usuarios:

-   Algunos usuarios pueden trabajar en un entorno ruidoso en el que no se puedan oír los sonidos.
-   Algunos usuarios pueden trabajar en un entorno silencioso que requiere que el sonido esté desactivado o establecido en un volumen bajo.
-   Algunos usuarios pueden tener dificultades auditivas o pérdida.
-   Es posible que el equipo no tenga oradores.

Por estos motivos, **el sonido que se usa para las notificaciones y comentarios nunca debe ser el único método de comunicación, sino que** debe complementar las indicaciones visuales o textuales.

### <a name="desirable-characteristics-of-sound"></a>Características deseadas de sonido

En general, los sonidos deben ser:

-   media a alta frecuencia (de 600 hercios \[ Hz \] a 2 kilohercios \[ kHz \] ).
-   Short (menos de un segundo).
-   volumen parcial o moderado.
-   sea.
-   agradable, no alarmante o discordante.
-   no verbal.
-   no repetitivo.

Con el sonido, menos es más. **El efecto de sonido ideal es el que los usuarios apenas avisan, pero que se omitirían si estuvieran ausentes.**

**Una idea equivocada habitual es que los sonidos de los eventos críticos deben ser fuertes y discordante para obtener la atención del usuario.** Esto no es cierto, porque el sonido está diseñado realmente para ser un medio suplementario de comunicación. En el caso de un mensaje de error crítico, su presentación (quizás en un cuadro de diálogo modal), su icono (un icono de error) y su texto y tono se combinan para comunicar la naturaleza del error. Un sonido de error efectivo puede ser ligeramente más alto que el sonido típico de Windows, pero no es necesario que sea mucho más alto.

### <a name="characteristics-of-windows-sounds"></a>Características de los sonidos de Windows

Más allá de esta llamada general para el mínimo, el sonido estético de Windows usa tonos claros, tonos puros y vidrioy y Airy, con un fundido suave y fundido de salida ("bordes") para evitar efectos abruptos, discordante y percussive. Están diseñados para sentirse sutil, suave y consonante. Los sonidos de Windows usan eco, reverberación y ecualización para lograr un funcionamiento ambiente natural.

La combinación de sonidos predeterminada para Windows no suele usar sonidos cotidianos o reconocibles que sean demasiado específicos o musicales. Algunos ejemplos de sonidos que evita son instrumentos musicales como pianos u otros instrumentos, sonidos para animales, ruidos ambientales, voz, voces, efectos sonoros similares a películas u otros sonidos de seres humanos. Además, los sonidos de Windows no están diseñados para que se perciban como música (es decir, Melodies de gran tamaño). Esto hace que Windows suene funcionalmente distinto de otros tipos de sonidos.

Dado que los sonidos de Windows están diseñados de forma profesional para tener las características deseadas y la apelación a un público amplio, **considere la posibilidad de usar estos sonidos de Windows integrados siempre que sea necesario.**

### <a name="designing-your-own-sounds"></a>Diseñar sus propios sonidos

Si tiene que crear sus propios sonidos, debe diseñarlos para que tengan las características descritas anteriormente. Procure hacer que complementen sus tareas o eventos asociados.

Comprenda que la creación de sonidos originales es difícil de hacer bien, especialmente en el caso de los sonidos destinados a un público amplio. El sonido puede ser un elemento de diseño polarizado. En el caso de todos los usuarios que suquieran un sonido, habrá muchos usuarios que no le gusten.

**Diseñe los sonidos del programa como un grupo que parezca que son variaciones relacionadas en un tema.** La experiencia de auditoría de su programa debe coordinarse con su experiencia visual. Además, el "tono" de los sonidos debe coordinarse con el [tono del texto](text-style-tone.md). Tenga en cuenta el modo en que el texto con un tono agradable y natural puede deshacerse al ir acompañado de sonidos intensos y de alarma.

**Si solo hace cuatro cosas...**

1.  Usar sonido con restricción Asegúrese de que hay una ventaja general de usuario clara. En casos de duda, no use sonido.
2.  Use los sonidos de Windows integrados siempre que sea necesario.
3.  Si diseña sus propios sonidos, asegúrese de que tienen las características de sonido deseables y como un aspecto completo como las variaciones de un tema.
4.  No asuma que los sonidos deben ser fuertes y discordante para obtener la atención del usuario.

## <a name="usage-patterns"></a>Patrones de uso

Los sonidos tienen varios patrones de uso:



|                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Finalización de la acción**<br/> notifica de forma Sonic a los usuarios cuando una acción iniciada por el usuario de ejecución prolongada se completa correctamente. <br/>                             | ![captura de pantalla del cuadro de diálogo descarga de archivos ](images/vis-sound-image2.png)<br/> En este ejemplo, el cuadro de diálogo reproduce un sonido para notificar a los usuarios que se ha completado la descarga.<br/>                                                                                                                                                                                                                                      |
| **Error de acción**<br/> notifica de forma Sonic a los usuarios cuando se produce un error en una acción iniciada por el usuario de ejecución prolongada. <br/>                                                 | ![captura de pantalla del mensaje de copia de seguridad de disco no accesible ](images/vis-sound-image3.png)<br/> En este ejemplo, Windows reproduce un sonido para notificar a los usuarios que se ha producido un error en la operación de copia de seguridad.<br/>                                                                                                                                                                                                                                  |
| **Evento importante del sistema**<br/> alerta a los usuarios de eventos importantes del sistema o del estado que requieren atención inmediata. <br/>                      | ![captura de pantalla de mensaje de batería baja ](images/vis-sound-image4.png)<br/> En este ejemplo, se avisa a los usuarios de que su batería baja requiere atención inmediata.<br/>                                                                                                                                                                                                                                                      |
| **Asesor**<br/> notifica a los usuarios la información pertinente potencialmente útil. <br/>                                                                 | Dado que esta información no suele requerir atención inmediata, un sonido de la información relacional proporciona sutiles comentarios sin interrumpir el flujo del usuario. <br/> ![captura de pantalla del mensaje de inicio de sesión de Live Messenger ](images/vis-sound-image5.png)<br/> En este ejemplo, se reproduce un sonido cuando un contacto inicia sesión en un servicio de mensajería instantánea.<br/>                                                                                 |
| **Efecto de sonido**<br/> proporciona un comentario a las interacciones del usuario. <br/>                                                                            | Proporciona comentarios de sonido reales o con estilo que son adecuados para la interacción. los efectos sonoros suelen sonar como si el usuario manipulara un objeto físico real. a veces se conoce como Foley. <br/> ![captura de pantalla de la ventana minimizada ](images/vis-sound-image6.png)<br/> En este ejemplo, el efecto minimizar el sonido de la ventana suena como un objeto del mundo real se reduce de tamaño.<br/> |
| **Sonidos de personalización de marca**<br/> un sonido que se proporciona para mejorar la experiencia del usuario a pesar de un impacto emocional y, como efecto secundario, promocionar la marca del producto. <br/> | Los sonidos de personalización de marca son los mejores cuando se sincronizan con eventos visuales, especialmente las transiciones de interfaz de usuario, como la presentación de una ventana de programa. las marcas de sonido verdaderas indican el origen de los bienes, de forma similar a una palabra o un logotipo con marca registrada, y son relativamente poco frecuentes. <br/> ![captura de pantalla del icono de inicio de Windows ](images/vis-sound-image7.png)<br/> En este ejemplo, el inicio de Windows es una experiencia de transición con marca.<br/>      |



 

## <a name="guidelines"></a>Directrices

### <a name="usage"></a>Uso

-   **Usar sonido con restricción** Asegúrese de que hay una ventaja general de usuario clara. Céntrese en los sonidos que mantienen informados a los usuarios, es probable que cambien su comportamiento o que proporcionen comentarios útiles. En casos de duda, no use sonido.
-   **Seleccione el sonido y sus características en función de cómo se use.** Para obtener una descripción de cada patrón de uso, vea la tabla de la sección anterior.
-   **En el caso de las notificaciones y comentarios, no utilice el sonido como único método de comunicación.** En su lugar, use el sonido como método complementario para reforzar las indicaciones visuales o textuales. Esto garantiza que los usuarios puedan ver la información si no pueden oír el sonido.
-   **No reproduzca sonidos fuertes o intensos con frecuencia.** Hacerlo no es necesario y produce una mala experiencia de usuario. Cuanto más frecuencia se reproduce un sonido, menos molesta debe ser. No es necesario que los sonidos sean fuertes o exigentes para atraer la atención.
-   **No suene.** Los pitidos no son adecuados para los programas modernos. Los pitidos no pueden tener significados específicos asignados y los usuarios no pueden controlarlos.
    -   **Excepción:** Las funciones críticas del sistema pueden emitir sonidos para avisar a los usuarios de las situaciones en las que deben asistir inmediatamente, como la energía de la batería de nivel crítico.

### <a name="playback"></a>Reproducción

-   **No repita un sonido más de dos veces consecutivas.**
-   **En el caso de una secuencia consecutiva de eventos de sonido relacionados, solo se reproduce un sonido en el primer evento.** Evite el uso de varios sonidos porque pueden entrar en conflicto entre sí o, de lo contrario, provocar una experiencia de usuario desagradable.

### <a name="sound-selection"></a>Selección de sonido

-   **Elija sonido agradable.** No utilice sonidos desagradables y de alarma, como zumbidos, bloqueos y roturas.
-   **Use sonidos cortos** (menos de un segundo).
-   **Use sonidos que sean aproximadamente el mismo volumen que el sonido típico de Windows.** A los usuarios les gusta tener que apagar el volumen al iniciar un equipo o un programa, especialmente en entornos públicos como reuniones y presentaciones. Los archivos de sonido de Microsoft Windows se encuentran en la carpeta multimedia dentro de la carpeta Windows.
-   **No elija sonidos que requieran localización.** Puede conseguirlo mediante sonidos que no usan voz o que tienen significados o connotaciones que dependen de la cultura.

### <a name="windows-system-sounds"></a>Sonidos del sistema de Windows

-   **Use los sonidos integrados del sistema de Windows siempre que sea necesario.**
-   **Elija usar sonidos del sistema en función de su significado asociado, no solo en el propio sonido.** Los sonidos del sistema deben usarse de forma coherente.

### <a name="sound-design"></a>Diseño de sonido

Al crear sus propios sonidos:

-   **Cree sonidos con las características de sonido deseadas.**
-   **Cree sonidos con mayor frecuencia medio a frecuencias altas (de 600 Hz a 2 kHz).** No utilice frecuencias bajas porque se encuentran más difíciles de encontrar y puede ser alarmante.
-   **Establezca la amplitud relativa de los sonidos normales en el nivel del sonido típico de Windows.** Los sonidos de Windows se han nivelado adecuadamente para los entornos domésticos y de trabajo. El uso de diferentes niveles para los sonidos obligará a los usuarios a realizar ajustes de volumen.
    -   Establezca sonidos importantes para que sean ligeramente más altos. Estos sonidos incluyen finalizaciones de acciones, errores de acción y eventos importantes del sistema.
    -   Establezca sonidos que se producen con frecuencia para que sean ligeramente más flexibles. Esto incluye FYIs, sonidos de personalización de marca y efectos sonoros.
-   **Elija sonidos coherentes con el significado de los sonidos de Windows.** Para crear una versión personalizada de un sonido de Windows, conserve el mismo paso e intervalo, pero cambie la orquestación o timbre. No asigne diferentes significados a los sonidos con intervalos y intervalos similares a los sonidos de Windows.
-   **Diseñe los sonidos para que el programa parezca que son variaciones relacionadas en un tema.** La experiencia de auditoría de su programa debe coordinarse con su experiencia visual.
    -   **Diseñar transiciones de escena y transiciones de audio juntas.** Por ejemplo, si una escena se atenúa gradualmente, cualquier sonido también debe atenuarse gradualmente. No se dañen transiciones visuales sin problemas con transiciones bruscas de sonido.
-   **Los sonidos deben estar en formato de archivo. wav.** Se recomienda el formato de modulación por pulsos sin comprimir de 16 bits 44,1 kHz. Si el tamaño del archivo es importante, use los formatos comprimidos o monoaural (mono), pero tenga en cuenta que hay una pérdida de calidad fácilmente perceptible que podría reflejarse incorrectamente en la aplicación.

### <a name="mixing"></a>Mezclar

-   **No tener controles de volumen o silenciar en el programa.** En su lugar, permita a los usuarios controlar la configuración relativa del volumen entre las aplicaciones con el mezclador de volumen de Windows. Si el programa tiene un control de volumen, habrá varios lugares en los que los usuarios ajusten su configuración, lo que puede provocar confusiones.

    ![captura de pantalla del mezclador de volumen de Windows ](images/vis-sound-image8.png)

    El mezclador de volumen de Windows permite a los usuarios controlar la configuración del volumen principal, así como el volumen de cada programa que esté reproduciendo audio.

<!-- -->

-   **Excepción:** Si el objetivo principal es que el programa sea reproducción o reproducción de audio o vídeo, puede ser útil tener un control de volumen en el programa. Use un control deslizante para este fin y proporcione comentarios inmediatos cuando el usuario cambie el volumen.

### <a name="windows-integration"></a>Integración de Windows

-   **Registre los sonidos del programa en el registro de sonidos de Windows.** Esto permite que el mezclador de volumen de Windows agregue un control deslizante para el programa.
-   **Registre los eventos de sonido personalizados del programa.** Esto permite que el elemento del panel de control de sonido de Windows los muestre. Cree la clave siguiente para cada evento de sonido personalizado: HKEY \_ Current \_ User \| AppEvents \| Event Labels \| eventName = Event Name.
-   **No se encableadon los sonidos de los eventos de sonido del programa.** En su lugar, especifique los sonidos que se van a reproducir mediante entradas del registro. Esto permite a los usuarios personalizar los eventos de sonido a través del elemento del panel de control de sonido.
    -   **Excepción:** Puede elegir entre los sonidos que se usan para la personalización de marca.
-   **No proporcione a los usuarios una forma de configurar sonidos dentro de las opciones del programa.** En su lugar, use el elemento del panel de control de sonidos de Windows para este fin.
-   **Considere la posibilidad de no asignar sonidos a eventos que se producen con frecuencia de forma predeterminada.** No es necesario que los usuarios configuren su manera de una experiencia inicial molesta.

### <a name="directsound-programming-issues"></a>Problemas de programación de DirectSound

-   En el caso de los programas de DirectSound que tengan su propio control de volumen, **establezca el volumen del programa en 100 por ciento de forma predeterminada.** Al hacerlo, se maximiza el intervalo dinámico del audio.
-   **No bloquee otros eventos de sonido ejecutando el programa en modo exclusivo.** Si lo hace, puede impedir que otros programas funcionen correctamente. Por ejemplo, el uso del modo exclusivo impide que un equipo se use como dispositivo de telefonía.

## <a name="text"></a>Texto

-   No use el adaptador de sonido de frase. En su lugar, use la tarjeta de sonido.
-   Use el dispositivo para hacer referencia de forma genérica a los altavoces, los auriculares y los micrófonos.
-   Use el controlador para hacer referencia al hardware de audio que controla los dispositivos, como tarjetas de sonido y chipsets.
-   Use la combinación de sonidos de frase para describir una colección de sonidos para eventos de programas comunes, como iniciar o recibir correo electrónico nuevo. Use el tema escritorio de frases para describir una colección de elementos visuales y sonidos para el escritorio del equipo.
-   Use el término audio para hacer referencia en general a voz, música y sonidos. Use el término sonido para hacer referencia más restringido al programa y a los sonidos de Windows que se describen en este artículo.

 

