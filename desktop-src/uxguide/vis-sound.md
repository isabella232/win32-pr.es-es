---
title: Sonido
description: Sonido es el elemento de audio de la experiencia del usuario.
ms.assetid: 2a276370-eff9-4844-b008-eba9ae5ac395
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 5569fe76578fdb79b30da7cbad95939773889b0d22de92b0af4babe966ec6390
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119348674"
---
# <a name="sound"></a>Sonido

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

*Sonido* es el elemento de audio de la experiencia del usuario. Cuando se usa correctamente, el sonido puede ser una forma eficaz de comunicación que establece una relación no verbal e incluso emocional con los usuarios. Los sonidos se pueden usar solos o como complemento de la interfaz de usuario visual. Por ejemplo, agregar un efecto de sonido a una notificación aumenta la probabilidad de que se note, especialmente si el usuario no mira la pantalla cuando se produce un evento.

![captura de pantalla del cuadro de diálogo de sonido ](images/vis-sound-image1.png)

En la pestaña Sonidos del elemento Del panel de control Sonido, los usuarios pueden realizar cambios en los sonidos del sistema.

En este artículo se trata el uso de sonidos dentro de un programa como respuesta a eventos y acciones del usuario, y la integración del control de sonido de un programa con Windows. No cubre el uso de música o voz.

**Nota:** Las directrices [relacionadas con las notificaciones](mess-notif.md) y la [personalción de marca](exper-branding.md) se presentan en artículos independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

Para decidir si debe usar sonido, tenga en cuenta estas preguntas:

-   **¿Hay una ventaja clara para el usuario al usar sonido?** Dado que los inconvenientes de usar sonido pueden superar fácilmente las ventajas, use sonido solo cuando haya una ventaja clara.
-   **¿Es adecuado el uso de sonido?** ¿Llama la atención el uso del sonido a las cosas que son merecedores de atención? ¿Los usuarios perderían el sonido si estuvieran ausentes? Céntrate en los sonidos que mantienen informados a los usuarios, es probable que cambien su comportamiento o proporcionen comentarios útiles.
-   **¿El uso de sonido distrae?** ¿Hay sonidos frecuentes, en voz alta y en voz alta? ¿Es probable que los usuarios reduzcan el volumen del sistema o el volumen del programa como resultado del uso del sonido?
-   **¿Usa el sonido como forma principal de comunicación?** En muchos casos, como en el caso de los usuarios que tienen algún nivel de pérdida auditiva, el sonido no debe usarse como medio principal de comunicación. El sonido es más eficaz como complemento a otros medios de comunicación (como texto o objetos visuales).
-   **¿Son los principales profesionales de IT de los usuarios de destino?** El sonido suele ser ineficaz para las tareas dirigidas a los profesionales de TI porque muchas de sus tareas se ejecutan desatendidamente. Además, el sonido no escala para ellos imagine que ejecuta cientos de tareas a la vez y que se escuchan sonidos cuando se completan o se producirá un error.

## <a name="design-concepts"></a>Conceptos de diseño

Normalmente, el sonido logra cualquiera o todos los propósitos siguientes:

-   **Notificación.** El sonido se puede asociar a eventos específicos. Por ejemplo, un sonido de "nuevo correo" indica a los usuarios cuándo llega el correo sin interrumpir su tarea actual.
-   **Comentarios.** El sonido puede proporcionar comentarios sobre acciones específicas del usuario. Por ejemplo, un sonido sutil que se reproduce al soltar el control deslizante en el control de volumen proporciona comentarios sobre el nivel de la configuración actual.
-   **Marca.** El sonido se puede asociar a contenido específico para marcar el producto, la aplicación o el servicio. Windows sonido de esta manera para el inicio del sistema operativo.
-   **Entretenimiento.** El sonido se usa normalmente para mejorar los productos de entretenimiento y para que cualquier producto sea más atractivo. Por ejemplo, la mayoría de los juegos, las aplicaciones de entrenamiento y los productos de consumidor usan sonido para atener a los usuarios y mejorar su experiencia.

Ciertos sonidos pueden cumplir varios de estos propósitos a la vez. El Windows de inicio, por ejemplo, indica que el proceso de inicio se ha completado y que el escritorio está listo para su uso. También proporciona una forma eficaz de personal de marca de producto e incluso participa momentáneamente en los usuarios.

Es probable que se eliminen los sonidos que no cumplen ninguno de estos propósitos.

### <a name="inappropriate-use-of-sound"></a>Uso inadecuado de sonido

**A pesar de las ventajas del sonido, el uso adecuado del sonido requiere una restricción significativa para hacerlo de lo contrario puede hacer que un programa sea molesto y distraiga.** Los usuarios desactivarán su sonido por completo si se vuelven afectados por sonidos frecuentes, repetitivos, jarring, disrupting y mal diseñados. en parte esto se debe a que, por su propia naturaleza, el sonido requiere atención y es difícil de ignorar. Para obtener sugerencias sobre cómo buscar un equilibrio razonable, consulte las [directrices de diseño de sonido.](#sound-design)

Dado que los inconvenientes de usar sonido pueden superar fácilmente las ventajas, use sonido solo cuando haya una ventaja clara. **Cuando esté en duda, no use sonido.**

### <a name="make-sound-supplemental"></a>Hacer que el sonido sea complementario

Incluso si el sonido se usa correctamente, hay muchas situaciones en las que el sonido podría no ser eficaz para todos los usuarios:

-   Algunos usuarios pueden trabajar en un entorno ruidoso donde no se pueden escuchar los sonidos.
-   Algunos usuarios pueden trabajar en un entorno silencioso que requiere que el sonido se apague o se establezca en un volumen bajo.
-   Algunos usuarios pueden tener discapacidades auditivas o pérdidas.
-   Es posible que el equipo no tenga altavoces.

Por estos motivos, el sonido usado para las notificaciones y los comentarios nunca debe ser el único método de **comunicación,** sino que debe complementar las indicaciones visuales o textuales.

### <a name="desirable-characteristics-of-sound"></a>Características deseables del sonido

En general, los sonidos deben ser:

-   de media a alta frecuencia (de 600 Hertz \[ Hz \] a 2 kilohercios \[ \] kHz).
-   short (menos de un segundo).
-   volumen suave o moderado.
-   Significativo.
-   no alarmante ni jarring.
-   no verbal.
-   no repetitiva.

Con sonido, menos es más. **El efecto de sonido ideal es aquel que los usuarios observan, pero se perderían si estuvieran ausentes.**

**Un concepto erróneo común es que los sonidos de los eventos críticos deben ser ruidosos y en voz alta para llamar la atención del usuario.** Esto no es cierto, porque el sonido realmente está pensado para ser un medio complementario de comunicación. En el caso de un mensaje de error crítico, su presentación (quizás en un cuadro de diálogo modal), su icono (un icono de error) y su texto y tono se combinan para comunicar la naturaleza del error. Un sonido de error eficaz puede ser ligeramente más alto que el sonido Windows típico, pero no es necesario que sea mucho más alto.

### <a name="characteristics-of-windows-sounds"></a>Características de los Windows sonidos

Más allá de esta llamada general al minimalismo, la apariencia de sonido de Windows usa sonidos claros, puros y con sonidos acristalados y aireados, con un atenuado suave ("bordes") para evitar efectos repentinos, jarring y percusivos. Están diseñados para ser sutiles, cómodos y consonantes. Windows sonidos usan eco, reverberación e igualdad para lograr una sensación ambiental natural.

El esquema de sonido predeterminado para Windows generalmente no usa sonidos instrumentales o reconocibles que son demasiado específicos o son músical. Algunos ejemplos de sonidos que evita son los instrumentoes musicales, como sonidos de sonidos, sonidos de animales, ruidos ambientales, voz, voces, efectos de sonido similares a películas u otros sonidos de personas. Además, Windows sonidos no están diseñados para ser percibidos como música (es decir, siempre que sean de varias notas). Esto hace que Windows sonidos funcionalmente distintos de otros tipos de sonidos.

Dado que Windows sonidos se diseñaron profesionalmente para tener las características deseables y atraer a un público amplio, considere la posibilidad de usar estos sonidos Windows integrados siempre que **corresponda.**

### <a name="designing-your-own-sounds"></a>Diseño de sus propios sonidos

Si debe crear sus propios sonidos, diseñe para que tengan las características descritas anteriormente. Procure que complementen sus tareas o eventos asociados.

Comprender que la creación de sonidos originales es difícil de hacer bien, especialmente para los sonidos destinados a un público amplio. El sonido puede ser un elemento de diseño de polarización. Para todos los usuarios a los que les encanta un sonido, habrá muchos que no le gusten.

**Diseñe los sonidos del programa como un grupo para que parezcan variaciones relacionadas en un tema.** La experiencia auditiva del programa debe coordinarse con su experiencia visual. Además, el "tono" de los sonidos debe coordinarse con el [tono del texto](text-style-tone.md). Tenga en cuenta cómo el texto con un tono natural y agradable se puede ensomar cuando va acompañado de sonidos desaperados y alarmantes.

**Si solo hace cuatro cosas...**

1.  Use sonido con moderación para asegurarse de que hay una ventaja general clara para el usuario. Cuando esté en duda, no use sonido.
2.  Use los sonidos de Windows integrados siempre que corresponda.
3.  Si diseña sus propios sonidos, asegúrese de que tengan las características de sonido deseadas y, en su conjunto, se parezcan a variaciones en un tema.
4.  No suponga que los sonidos deben ser ruidosos y sonores para llamar la atención del usuario.

## <a name="usage-patterns"></a>Patrones de uso

Los sonidos tienen varios patrones de uso:



|     Uso de sonido                                                                                                                                                                 |  Ejemplo                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Finalización de la acción**<br/> notifica a los usuarios cuando una acción iniciada por el usuario de larga duración se completa correctamente. <br/>                             | ![captura de pantalla del cuadro de diálogo de descarga de archivos ](images/vis-sound-image2.png)<br/> En este ejemplo, el cuadro de diálogo reproduce un sonido para notificar a los usuarios que la descarga se ha completado.<br/>                                                                                                                                                                                                                                      |
| **Error de acción**<br/> notifica a los usuarios cuando se produce un error en una acción iniciada por el usuario de larga duración. <br/>                                                 | ![captura de pantalla del mensaje de disco de copia de seguridad no accesible ](images/vis-sound-image3.png)<br/> En este ejemplo, Windows un sonido para notificar a los usuarios que la operación de copia de seguridad ha dado error.<br/>                                                                                                                                                                                                                                  |
| **Evento importante del sistema**<br/> alerta a los usuarios de eventos o estados importantes del sistema que requieren atención inmediata. <br/>                      | ![captura de pantalla del mensaje de batería baja ](images/vis-sound-image4.png)<br/> En este ejemplo, se alerta a los usuarios de que su batería baja requiere atención inmediata.<br/>                                                                                                                                                                                                                                                      |
| **Fyi**<br/> notifica a los usuarios información potencialmente útil y pertinente. <br/>                                                                 | Dado que esta información normalmente no requiere atención inmediata, un sonido fyi proporciona comentarios sutiles sin romper el flujo del usuario. <br/> ![captura de pantalla del mensaje de inicio de sesión de Live Messenger ](images/vis-sound-image5.png)<br/> En este ejemplo, se reproduce un sonido cuando un contacto inicia sesión en un servicio de mensajería instantánea.<br/>                                                                                 |
| **Efecto de sonido**<br/> proporciona comentarios a las interacciones del usuario. <br/>                                                                            | Proporciona comentarios de sonido con estilo o reales que son adecuados para la interacción. Los efectos de sonido suelen parecer como si el usuario manipulara un objeto físico real. a veces se conoce como foley. <br/> ![captura de pantalla de la ventana minimizada ](images/vis-sound-image6.png)<br/> En este ejemplo, el efecto minimizar el sonido de la ventana parece que se está reduciendo el tamaño de un objeto real.<br/> |
| **Sonidos de personal de marca**<br/> un sonido proporcionado para mejorar la experiencia del usuario a través del impacto emocional y, como efecto secundario, promover la marca de producto. <br/> | Los sonidos de personalización de marca son los más adecuados cuando se sincronizan con eventos visuales, especialmente las transiciones de interfaz de usuario, como la presentación de una ventana del programa. Las verdaderas marcas de sonido indican el origen de bienes, similar a una palabra o logotipo de marca comercial, y son relativamente poco frecuentes. <br/> ![captura de pantalla del icono de inicio de Windows ](images/vis-sound-image7.png)<br/> En este ejemplo, Windows inicio es una experiencia de transición de marca.<br/>      |



 

## <a name="guidelines"></a>Directrices

### <a name="usage"></a>Uso

-   **Use sonido con moderación** para asegurarse de que hay una ventaja general clara para el usuario. Céntrate en los sonidos que mantienen informados a los usuarios, es probable que cambien su comportamiento o proporcionen comentarios útiles. Cuando esté en duda, no use sonido.
-   **Seleccione el sonido y sus características en función de cómo se esté utilizando.** Para obtener una descripción de cada patrón de uso, consulte la tabla de la sección anterior.
-   **Para recibir notificaciones y comentarios, no use sonido como único método de comunicación.** En su lugar, use el sonido como método complementario para reforzar las indicaciones visuales o textuales. Esto garantiza que los usuarios puedan ver la información si no pueden escuchar el sonido.
-   **No reprodgue sonidos en voz alta o ruidosos con frecuencia.** Esto no es necesario y da lugar a una mala experiencia del usuario. Cuando más a menudo se reproduce un sonido, menos ofuscado debería ser. Los sonidos no tienen que ser ruidosos ni exigentes para atraer la atención.
-   **No haga un pitido.** El pitido no es adecuado para los programas modernos. Los bips no pueden tener significados específicos asignados y los usuarios no pueden controlarlos.
    -   **Excepción:** Las funciones críticas del sistema pueden recibir un pitido para alertar a los usuarios de situaciones a las que deben atender inmediatamente, como una batería críticamente baja.

### <a name="playback"></a>Reproducción

-   **No repita un sonido más de dos veces consecutivamente.**
-   **Para una secuencia consecutiva de eventos de sonido relacionados, reprodgue un sonido solo en el primer evento.** Evite el uso de varios sonidos porque pueden colisionar entre sí o provocar una experiencia de usuario insociada.

### <a name="sound-selection"></a>Selección de sonido

-   **Elija sonidos divertidos.** No use sonidos extraños y alarmantes, como ruidos, bloqueos y desenlazamiento.
-   **Use sonidos cortos** (menos de un segundo).
-   **Use sonidos que sean aproximadamente el mismo volumen que el sonido Windows típico.** Los usuarios no pueden tener que bajar el volumen al iniciar un equipo o un programa, especialmente en entornos públicos como reuniones y presentaciones. Los archivos Windows de sonido de Microsoft se encuentran en la carpeta Media dentro de Windows carpeta.
-   **No elija sonidos que requieran localización.** Puede lograr esto mediante sonidos que no usan voz o que tienen significados o connotaciones dependientes de la cultura.

### <a name="windows-system-sounds"></a>Windows sonidos del sistema

-   **Use los sonidos integrados Windows sistema cuando corresponda.**
-   **Elija usar sonidos del sistema en función de su significado asociado, no solo en el propio sonido.** Los sonidos del sistema se deben usar de forma coherente.

### <a name="sound-design"></a>Diseño de sonido

Al crear sus propios sonidos:

-   **Cree sonidos con las características de sonido deseadas.**
-   **Componer sonidos con principalmente frecuencias de intervalo medio a alto (de 600 Hz a 2 kHz).** No use frecuencias bajas porque viajan más lejos, son más difíciles de localizar y pueden ser alarmantes.
-   **Establezca la amplitud relativa de los sonidos normales en el nivel del sonido Windows normal.** Los Windows sonidos se han nivelado adecuadamente para entornos de trabajo y hogar. El uso de diferentes niveles para los sonidos obligará a los usuarios a realizar ajustes de volumen.
    -   Establezca sonidos importantes para que sean ligeramente más fuertes. Estos sonidos incluyen finalizaciones de acciones, errores de acción y eventos importantes del sistema.
    -   Establezca sonidos que se producen con frecuencia para que sean ligeramente más flexibles. Estos incluyen las IA, los sonidos de personal de marca y los efectos de sonido.
-   **Elija sonidos coherentes con el significado del Windows sonidos.** Para crear una versión personalizada de un Windows sonido, conserve el mismo tono e intervalo, pero cambie la orquestación o el timbre. No asigne significados diferentes a sonidos con intervalos y sonidos similares a los Windows sonidos.
-   **Diseñe los sonidos para que el programa parezca que son variaciones relacionadas en un tema.** La experiencia auditiva del programa debe coordinarse con su experiencia visual.
    -   **Diseñe transiciones de escena y transiciones de audio juntas.** Por ejemplo, si una escena se atenua gradualmente, cualquier sonido también debe atenuarse gradualmente. No interrumpa las transiciones visuales sin problemas al tener transiciones de sonido repentinas.
-   **Los sonidos deben estar en formato de archivo .wav.** Se recomienda el formato de compresión de código de pulso estéreo (PCM) de 16 bits y 44,1 kHz. Si el tamaño del archivo es importante, use formatos comprimidos o monográficos, pero tenga en cuenta que hay una pérdida de calidad fácilmente reconocible que podría reflejarse mal en la aplicación.

### <a name="mixing"></a>Mezcla

-   **No tiene controles de volumen o exclusión mutua en el programa.** En su lugar, permita que los usuarios controle la configuración relativa del volumen entre las aplicaciones con Windows mezclador de volúmenes. Si el programa tiene un control de volumen, habrá varios lugares donde los usuarios ajusten su configuración, lo que puede provocar confusión.

    ![captura de pantalla del mezclador de volúmenes de Windows ](images/vis-sound-image8.png)

    El Windows de volumen permite a los usuarios controlar la configuración del volumen principal, así como el volumen de cada programa que está reproduciendo audio actualmente.

<!-- -->

-   **Excepción:** Si el propósito principal del programa es la reproducción o creación de audio o vídeo, puede ser útil tener un control de volumen en el programa. Use un control deslizante para este propósito y proporcione comentarios inmediatos cuando el usuario cambie el volumen.

### <a name="windows-integration"></a>Windows integración

-   **Registre los sonidos del programa en el registro Windows Sounds.** Esto permite que el Windows de volumen agregue un control deslizante para el programa.
-   **Registre los eventos de sonido personalizados del programa.** De este modo, Windows elemento del panel de control Sonido para mostrarlos. Cree la clave siguiente para cada evento de sonido personalizado: HKEY \_ CURRENT \_ USER \| AppEvents \| Event Labels \| EventName = Event Name.
-   **No cablee los sonidos de los eventos de sonido del programa.** En su lugar, especifique los sonidos que se reproducirán mediante entradas del Registro. Esto permite a los usuarios personalizar los eventos de sonido a través del elemento del panel de control Sonido.
    -   **Excepción:** Puede elegir los sonidos de cableado que se usan para la personalción de marca.
-   **No proporcione una manera de que los usuarios configuren sonidos dentro de las opciones del programa.** En su lugar, use el Windows panel de control Sonidos para este propósito.
-   **Considere la posibilidad de no asignar sonidos a eventos que se producen con frecuencia de forma predeterminada.** No es necesario que los usuarios configuren su manera de salir de una experiencia inicial insoportable.

### <a name="directsound-programming-issues"></a>Problemas de programación de Direct Sound

-   En el caso de los programas Direct Sound que tienen su propio control de volumen, establezca el volumen del programa **en el 100 % de forma predeterminada.** Al hacerlo, se maximiza el intervalo dinámico del audio.
-   **No bloquee otros eventos de sonido ejecutando el programa en modo exclusivo.** Esto puede impedir que otros programas funcionen correctamente. Por ejemplo, el uso del modo exclusivo impide que un equipo se use como dispositivo de telefonía.

## <a name="text"></a>Texto

-   No use el adaptador de sonido de frase. En su lugar, use la tarjeta de sonido.
-   Use el dispositivo para hacer referencia genéricamente a altavoces, auriculares y micrófonos.
-   Use el controlador para hacer referencia al hardware de audio que controla los dispositivos, como tarjetas de sonido y conjuntos de chips.
-   Use el esquema de sonido de frase para describir una colección de sonidos para eventos de programa comunes, como iniciar sesión o recibir correo electrónico nuevo. Use el tema del escritorio de frases para describir una colección de elementos visuales y sonidos para el escritorio del equipo.
-   Use el término audio para hacer referencia ampliamente a voz, música y sonidos. Use el término sonido para hacer referencia más estrechamente al programa y Windows sonidos descritos en este artículo.

 

