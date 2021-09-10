---
title: Comando set
description: El comando set establece la configuración de control para el dispositivo. Los dispositivos cd audio, digital-video, secuenciador MIDI, VCR, videodisc, superposición de vídeo y audio de onda reconocen este comando.
ms.assetid: 1ec4d84e-372a-4b6d-b694-f5afb41f90b2
keywords:
- comando set Windows Multimedia
topic_type:
- apiref
api_name:
- set
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fc9263ace043f938c8d793b2ceef5ad70264bb1
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369835"
---
# <a name="set-command"></a>Comando set

> [!NOTE]
> La comunicación sin sesgos de Microsoft admite un entorno diverso e inclusario.  Dentro de este documento, hay referencias a la palabra "subordinada". La Guía de estilo de Microsoft [para Bias-Free Comunicaciones](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) lo reconoce como una palabra excluyente.  Esta redacción se usa, ya que actualmente es la que se usa en los comandos. Por coherencia, este documento contiene esta palabra. Cuando esta palabra se modifica en los comandos, corregiremos este documento para que esté alineado.


El comando set establece la configuración de control para el dispositivo. Los dispositivos cd audio, digital-video, secuenciador MIDI, VCR, videodisc, superposición de vídeo y audio de onda reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("set %s %s %s"),
  lpszDeviceID,
  lpszSetting,
  lpszFlags
);
      
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*lpszSetting*
</dt> <dd>

Marca para establecer la configuración del control. En la tabla siguiente se enumeran los tipos de dispositivo que reconocen el comando **set** y las marcas usadas por cada tipo.




| Tipo de dispositivo | Marcas de comandos | 
|-------------|---------------|
| cdaudio | <ul><li>audio todo desactivado</li><li>audio todo en</li><li>audio dejado desactivado</li><li>audio a la izquierda en</li><li>audio desactivado</li><li>audio a la derecha en</li><li>puerta cerrada</li><li>puerta abierta</li><li>milisegundos de formato de tiempo</li><li>formato de hora msf</li><li>formato de hora tmsf</li></ul> | 
| digitalvideo | <ul><li>audio todo desactivado</li><li>audio todo en</li><li>audio dejado desactivado</li><li>audio a la izquierda en</li><li>audio desactivado</li><li>audio a la derecha en</li><li>puerta cerrada</li><li>puerta abierta</li><li>formato <em>de</em> archivo</li><li>buscar exactamente en</li><li>buscar exactamente desactivado</li><li>factor de <em>velocidad</em></li><li>formato de archivo <em>still</em></li><li>marcos de formato de tiempo</li><li>milisegundos de formato de tiempo</li><li>vídeo desactivado</li><li>vídeo en</li></ul> | 
| overlay | <ul><li>audio todo desactivado</li><li>audio todo en</li><li>audio dejado desactivado</li><li>audio a la izquierda en</li><li>audio desactivado</li><li>audio a la derecha en</li><li>puerta cerrada</li><li>puerta abierta</li><li>vídeo desactivado</li><li>vídeo en</li></ul> | 
| sequencer | <ul><li>audio todo desactivado</li><li>audio todo en</li><li>audio dejado desactivado</li><li>audio a la izquierda en</li><li>audio desactivado</li><li>audio a la derecha en</li><li>puerta cerrada</li><li>puerta abierta</li><li>MASTER MIDI</li><li>master none</li><li>master SMPTE</li><li>tiempo de <em>desplazamiento</em></li><li>asignador de puertos</li><li>puerto ninguno</li><li>puerto <em>port_number</em></li><li>archivo subordinado</li><li>slave MIDI</li><li>slave none</li><li>slave SMPTE</li><li>tempo <em>tempo_value</em></li><li>milisegundos de formato de tiempo</li><li>fps de SMPTE de formato <em>de hora</em></li><li>time format SMPTE 30 drop</li><li>puntero de canción de formato de tiempo</li></ul> | 
| <strong>Vcr</strong> | <ul><li>ensamblar registro en</li><li>ensamblar registro desactivado</li><li>audio todo desactivado</li><li>audio todo en</li><li>audio dejado desactivado</li><li>audio a la izquierda en</li><li>audio desactivado</li><li>audio a la derecha en</li><li>hora del <em>reloj</em></li><li>formato de contador</li><li>valor <em>del contador</em></li><li>puerta cerrada</li><li>puerta abierta</li><li>contador de índice</li><li>index date</li><li>tiempo de índice</li><li>tiempo de índice</li><li>duración de <em></em> codelength</li><li>tiempo de <em>espera de pausa</em></li><li>duración del postroll:</li><li><em>duration</em></li><li>encendido</li><li>apagado</li><li>duración de la inscripción <em>previa</em></li><li>SP de formato de registro</li><li>LP de formato de registro</li><li>EP de formato de registro</li><li>factor de <em>velocidad</em></li><li>marcos de formato de tiempo</li><li>time format hms</li><li>milisegundos de formato de tiempo</li><li>formato de hora msf</li><li>fps de SMPTE de formato <em>de hora</em></li><li>time format SMPTE 30 drop</li><li>formato de hora tmsf</li><li>contador de modo de tiempo</li><li>detección del modo de tiempo</li><li>código de tiempo del modo de tiempo</li><li>más seguimiento</li><li>seguimiento menos</li><li>seguimiento del restablecimiento</li></ul> | 
| Videodisco | <ul><li>audio todo desactivado</li><li>audio todo en</li><li>audio dejado desactivado</li><li>audio a la izquierda en</li><li>audio desactivado</li><li>audio a la derecha en</li><li>puerta cerrada</li><li>puerta abierta</li><li>marcos de formato de tiempo</li><li>time format hms</li><li>milisegundos de formato de tiempo</li><li>seguimiento de formato de hora</li><li>vídeo desactivado</li><li>vídeo en</li></ul> | 
| waveaudio | <ul><li>entero de <em>alineación</em></li><li>cualquier entrada</li><li>cualquier salida</li><li>audio todo desactivado</li><li>audio todo en</li><li>audio dejado desactivado</li><li>audio a la izquierda en</li><li>audio desactivado</li><li>audio a la derecha en</li><li>bitspersample <em>bit_count</em></li><li>bytespersec <em>byte_rate</em></li><li>canales <em>channel_count</em></li><li>puerta cerrada</li><li>puerta abierta</li><li>format tag pcm</li><li>etiqueta de <em>formato</em></li><li>entero <em>de entrada</em></li><li>entero <em>de salida</em></li><li>samplespersec <em>entero</em></li><li>bytes de formato de hora</li><li>milisegundos de formato de tiempo</li><li>ejemplos de formato de hora</li></ul> | 




 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el **parámetro lpszSetting** y sus significados.




| Value | Significado | 
|-------|---------|
| entero de <em>alineación</em> | Establece la alineación de los bloques de datos con respecto al inicio de los datos pasados al dispositivo de audio de forma de onda. El archivo se guarda en este formato. | 
| cualquier entrada | Use cualquier entrada que admita el formato actual al grabar. Esta es la configuración predeterminada. | 
| cualquier salida | Use cualquier salida que admita el formato actual al reproducir. Este es el valor predeterminado. | 
| ensamblar registro en <br /> ensamblar registro desactivado <br /> | En el modo de ensamblado, todas las pistas se registran según lo definido por el dispositivo. La mayoría de los VCR están en modo de ensamblado de forma predeterminada. | 
| audio todo desactivado <br /> audio todo en <br /> | Deshabilita o habilita la salida de audio. Los dispositivos de superposición de vídeo, el secuenciador MCISEQ y el dispositivo MCIWAVE de audio de onda no admiten esta marca. | 
| audio dejado desactivado <br /> audio a la izquierda en <br /> audio desactivado <br /> audio a la derecha en <br /> | Deshabilita o habilita la salida en el canal de audio izquierdo o derecho. Los dispositivos de superposición de vídeo, el secuenciador MCISEQ y el dispositivo MCIWAVE de audio de onda no admiten esta marca. | 
| bitspersample <em>bit_count</em> | Establece el número de bits por ejemplo PCM (pulse Code Desaconstura) reproducía o grababa. El archivo se guarda en este formato. | 
| bytespersec <em>byte_rate</em> | Establece el número medio de bytes por segundo que se reproducen o se registran. El archivo se guarda en este formato. | 
| canales <em>channel_count</em> | Establece los canales para reproducir y grabar. El archivo se guarda en este formato. | 
| hora del <em>reloj</em> | Establece la hora del reloj externo en <em>time.</em> El formato se especifica como un entero largo sin signo. | 
| formato de contador | Establezca el formato de hora del contador, tal como lo devuelve <a href="status.md">el estado</a> "counter". Para obtener información sobre los tipos aplicables, vea el <strong>comando set</strong> "time format". | 
| valor <em>del contador</em> | Establece el contador VCR en el valor especificado. El valor debe especificarse en el formato de contador actual. Para obtener más información, vea el <strong>comando set</strong> "counter format". | 
| puerta cerrada | Retira la bandeja y cierra la puerta, si es posible. En el caso de las V VCR, carga la cinta automáticamente. | 
| puerta abierta | Abre la puerta y expulsa la bandeja o la cinta, si es posible. | 
| formato <em>de</em> archivo | Especifica un formato de archivo que se usa para los comandos <a href="save.md">save</a> <a href="capture.md">o capture.</a> Si se omite, esto podría tener como valor predeterminado un formato definido por el controlador de dispositivo. Si el formato de archivo especificado entra en conflicto con el algoritmo y la calidad seleccionados actualmente, se cambian a los valores predeterminados para el formato de archivo. Se definen los siguientes formatos de archivo:<ul><li>avi: especifica el formato AVI.</li><li>avss: especifica el formato avSS.</li><li>dib: especifica el formato DIB.</li><li>jfif: especifica el formato JFIF.</li><li>jpeg: especifica el formato JPEG.</li><li>mpeg: especifica el formato MPEG.</li><li>rdib: especifica el formato DIB de RLE.</li><li>rjpeg: especifica el formato RJPEG.</li></ul> | 
| format tag pcm | Establece el tipo de formato en PCM para reproducir y grabar. El archivo se guarda en este formato. | 
| etiqueta de <em>formato</em> | Establece el tipo de formato para reproducir y grabar. El archivo se guarda en este formato. | 
| código de tiempo del índice <br /> contador de índice <br /> index date <br /> tiempo de índice <br /> | Establece la pantalla de presentación actual en el VCR. | 
| entero <em>de entrada</em> | Establece el canal de audio utilizado como entrada. | 
| duración <em>de la longitud</em> | Establece la longitud especificada por el usuario de la cinta en el VCR. El comando "length" devuelve esta longitud y se proporciona por compatibilidad con las aplicaciones que requieren que este comando devuelva una longitud válida. <a href="status.md"></a> | 
| master midi | Establece el secuenciador de MIDI como origen de sincronización. Los datos de sincronización se envían en formato MIDI. El secuenciador MCISEQ no admite esta marca. | 
| master none | Impide que el secuenciador de MIDI envíe datos de sincronización. El secuenciador MCISEQ no admite esta marca. | 
| master smpte | Establece el secuenciador de MIDI como origen de sincronización. Los datos de sincronización se envían en formato SMPTE (Society of Motion Picture and Tv Engineers). El secuenciador MCISEQ no admite esta marca. | 
| tiempo de <em>desplazamiento</em> | Establece el tiempo de desplazamiento <em>de</em>SMPTE. El desplazamiento es la hora inicial de una secuencia basada en SMPTE. El <em>tiempo</em> se expresa como <em>hh</em>: <em>mm</em>: <em>ss</em>: <em>ff</em>, donde <em>hh</em> es horas, <em>mm</em> es minutos, <em>ss</em> es segundos y <em>ff</em> es fotogramas. | 
| entero <em>de salida</em> | Establece el canal de audio utilizado como salida. | 
| tiempo de <em>espera de pausa</em> | Establece la duración máxima, en milisegundos, de un <a href="pause.md">comando de</a> pausa. Un <em>valor de</em> tiempo de espera de cero indica que no se agotará el tiempo de espera. | 
| duración de la duración del <em>postroll</em> | Establece la longitud, en el formato de hora actual, <a href="stop.md"></a> necesaria <strong></strong> para detener el transporte de VCR cuando se emite un comando de detenerse o pausar. | 
| asignador de puertos | Establece el asignador de MIDI como puerto que recibe los mensajes DE MIDI. Se produce un error en este comando si otra aplicación está utilizando el asignador DE LÍNEA O un puerto que necesita. | 
| puerto ninguno | Deshabilita el envío de mensajes MIDI. Este comando también cierra un puerto MIDI. | 
| puerto <em>port_number</em> | Establece el puerto MIDI que recibe los mensajes DE MIDI. Se produce un error en este comando si otra aplicación está utilizando el puerto que está intentando abrir. | 
| encendido <br /> apagado <br /> | Establece el encendido o apagado del dispositivo. | 
| duración de la inscripción <em>previa</em> | Establece la longitud, en el formato de hora actual, necesaria para estabilizar la salida de VCR. | 
| SP de formato de registro <br /> LP de formato de registro <br /> EP de formato de registro <br /> | Establece el modo de grabación de VCR en SP para reproducción estándar, EP para reproducción extendida o LP para reproducción larga. Estos valores no están diseñados para ser específicos de VHS. Se asignan a tres modos adecuados con otros formatos de cinta. Por ejemplo, SP se asigna a la grabación más rápida y de mayor calidad. | 
| samplespersec <em>entero</em> | Establece la frecuencia de muestreo para reproducir y grabar. El archivo se guarda en este formato. | 
| buscar exactamente en<br /> buscar exactamente desactivado <br /> | Selecciona uno de los dos modos de búsqueda. Con "buscar exactamente en", buscar siempre se moverá al marco especificado. Con "buscar exactamente desactivado", buscar se moverá al fotograma clave más cercano antes del marco especificado. | 
| archivo subordinado | Establece el secuenciador MIDI para usar datos de archivo como origen de sincronización. Esta es la configuración predeterminada. | 
| slave midi | Establece el secuenciador MIDI para usar los datos ENTRANTES DE LA SINCRONIZACIÓN para el origen de sincronización. El secuenciador reconoce los datos de sincronización con el formato MIDI. El secuenciador MCISEQ no admite esta marca. | 
| slave none | Establece el secuenciador MIDI para omitir la sincronización | 
| slave smpte | Establece el secuenciador MIDI para usar los datos ENTRANTES DE LA SINCRONIZACIÓN para el origen de sincronización. El secuenciador reconoce los datos de sincronización con el formato SMPTE. El secuenciador MCISEQ no admite esta marca. | 
| factor de velocidad | Establece la velocidad relativa de reproducción de vídeo y audio desde el área de trabajo. Factor es la relación entre la velocidad de fotogramas nominal y la velocidad de fotogramas deseada, donde la velocidad nominal de fotogramas se designa como 1000. (Una velocidad de 500 es la velocidad media normal, 2000 es el doble de velocidad normal, y así sucesivamente). Al establecer la velocidad en cero, se reproduce el vídeo lo más rápido posible sin quitar fotogramas y sin audio. | 
| formato de archivo <em>still</em> | Especifica el formato de archivo utilizado para los comandos de captura. | 
| tempo tempo_value | Establece el tempo de la secuencia según el formato de hora actual. Para un archivo basado en PPQN, el tempo_value se interpreta como latidos por minuto. Para un archivo basado en SMPTE, el tempo_value se interpreta como fotogramas por segundo. | 
| bytes de formato de hora | En un formato de archivo PCM, establece el formato de hora en bytes. Toda la información de posición se especifica como bytes después de este comando. | 
| marcos de formato de tiempo | Establece el formato de tiempo en fotogramas. Todos los comandos que usan valores de posición asumirán fotogramas. Cuando se abre el dispositivo, los fotogramas son el modo predeterminado. Compatible con videodiscos que usan el formato CSV. | 
| formato de hora hms | Establece el formato de hora en horas, minutos y segundos. Todos los comandos que usan valores de posición asumirán HMS. HMS es el formato predeterminado para los vídeos clvdiscs. Especifique un valor DE HMS como hh:mm:ss, donde hh es horas, mm es minutos y ss es segundos. Puede omitir un campo si es y todos los campos siguientes son cero. Por ejemplo, 3, 3:0 y 3:0:0 son formas válidas de expresar 3 horas. <br /> | 
| milisegundos de formato de tiempo | Establece el formato de hora en milisegundos. Todos los comandos que usan valores de posición asumirán milisegundos. Puede abreviar milisegundos como "ms". En el caso de los dispositivos secuenciador, el archivo de secuencia establece el formato predeterminado en PPQN o SMPTE. Los dispositivos de superposición de vídeo no admiten esta marca.<br /> | 
| formato de hora msf | Establece el formato de tiempo en minutos, segundos y fotogramas. Todos los comandos que usan valores de posición asumirán MSF (el formato predeterminado para el audio de CD). Especifique un valor de MSF como mm:ss:ff, donde mm es minutes, ss es seconds y ff es frames. Puede omitir un campo si es y todos los campos siguientes son cero. Por ejemplo, 3, 3:0 y 3:0:0 son formas válidas de expresar 3 minutos.<br /> Los campos MSF tienen los siguientes valores máximos:<br /><ul><li>Minutos 99</li><li>Segundos 59</li><li>Fotogramas 74</li></ul> | 
| ejemplos de formato de hora | Establece el formato de hora en ejemplos. Toda la información de posición se especifica como ejemplos después de este comando. | 
| time format smpte 24<br /> time format smpte 25<br /> formato de hora smpte 30<br /> | Establece el formato de tiempo en una velocidad de fotogramas SMPTE. En el caso de los VCR, establece el formato de hora en hh:mm:ss:ff, donde los valores legales son de 00:00:00:00 a 23:59:59:xx, y xx es uno menor que los fotogramas por segundo especificados por el número 24, 25 o 30 como se especifica en la marca. En la entrada, dos puntos (:) son necesarios para separar los componentes. Las unidades menos significativas se pueden omitir si son 00; Por ejemplo, 02:00 es igual que 02:00:00:00. Todos los comandos que usan valores de posición asumirán el formato SMPTE.<br /> El archivo de secuencia establece el formato predeterminado en PPQN o SMPTE.<br /> | 
| time format smpte 30 drop | Establece el formato de tiempo en SMPTE 30 drop frame rate (Velocidad de fotogramas de colocación de SMPTE 30). En el caso de los VCR, igual que SMPTE 30, salvo que determinadas posiciones de código de tiempo se descartan del formato para que las posiciones de código de tiempo grabadas para cada fotograma (con la velocidad de fotogramas TIME de 29,97 fps) se correspondan con tiempo real (a 30 fps). Las posiciones de código de tiempo que se descartan son las siguientes: dos cada minuto, en el minuto, para los nueve primeros de cada diez minutos de contenido grabado. Por ejemplo, a las 01:04:59:29, la siguiente posición del código de tiempo sería 01:05:00:02, no 01:05:00:00. Todos los comandos que usan valores de posición asumirán el formato SMPTE.<br /> El archivo de secuencia establece el formato predeterminado en PPQN o SMPTE.<br /> | 
| puntero de canción de formato de tiempo | Establece el formato de hora en puntero de canción (decimosexta notas). Todos los comandos que usan valores de posición asumirán unidades de puntero de canción. Esta marca solo es válida para una secuencia de tipo de división PPQN. | 
| formato de hora tmsf | Establece el formato de tiempo en pistas, minutos, segundos y fotogramas. Todos los comandos que usan valores de posición asumirán TMSF. Especifique un valor TMSF como tt:mm:ss:ff, donde tt es tracks, mm is minutes, ss is seconds y ff is frames. Puede omitir un campo si es y todos los campos siguientes son cero. Por ejemplo, 3, 3:0, 3:0:0 y 3:0:0:0 son formas válidas de expresar el seguimiento 3. <br /> Los campos TMSF tienen los siguientes valores máximos:<br /><ul><li>Pistas 99</li><li>Minutos 90</li><li>Segundos 59</li><li>Fotogramas 74</li></ul> | 
| seguimiento de formato de hora | Establece el formato de posición en pistas. Todos los comandos que usan valores de posición asumirán pistas. | 
| contador de modo de tiempo | Establece el modo de información de posición para usar los contadores vcr. | 
| detección del modo de tiempo | Establece el modo de información de posición en función de la detección de información de código de tiempo en la cinta. Si se detecta información de código de tiempo, el tipo de hora se establece en "código de tiempo"; De lo contrario, el tipo de hora se establece en "counter". "Detectar" es un modo especial. Cada vez que se abre el controlador, se inserta una nueva cinta o se emite el comando "time mode", el controlador comprueba el modo de hora actual disponible en la cinta y establece "time type" en "timecode" o "counter". Una vez establecido el "tipo de tiempo", el controlador no lo cambia hasta que se vuelva a producir una de las condiciones anteriores.<br /> | 
| código de tiempo del modo de tiempo | Establece el modo de información de posición para usar la información de "código de tiempo" en la cinta. | 
| seguimiento más <br /> seguimiento menos <br /> seguimiento del restablecimiento <br /> | Ajusta la velocidad del transporte de cinta de vídeo en incrementos finos. Use las marcas de "seguimiento" cuando se obtenga una imagen ruidosa de un VCR. "Tracking plus" aumenta la velocidad de transporte. "Seguimiento menos" reduce la velocidad de transporte. "Restablecimiento de seguimiento" devuelve el ajuste de seguimiento a cero. | 
| vídeo desactivado | Deshabilita la salida de vídeo. | 
| vídeo en | Habilita la salida de vídeo. | 




 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital y VCR, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Cuando se crea el archivo para almacenar los datos, se definen varias propiedades de los datos de forma de onda. Estas propiedades describen cómo se estructuran los datos dentro del archivo y no se pueden cambiar una vez que comienza la grabación. En la lista siguiente se identifican estas propiedades:

-   alineación
-   bitspersample
-   bytespersec
-   canales nueva
-   etiqueta de formato
-   samplespersec

## <a name="examples"></a>Ejemplos

El comando siguiente establece el formato de hora en milisegundos y el formato de audio de forma de onda en 8 bits, mono, 11 kHz.

``` syntax
set mysound time format ms bitspersample 8 channels 1 samplespersec 11025
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadenas de comandos de MCI](mci-command-strings.md)
</dt> <dt>

[capturar](capture.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[guardar](save.md)
</dt> <dt>

[stop](stop.md)
</dt> </dl>

 

