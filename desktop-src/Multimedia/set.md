---
title: Set (comando)
description: El comando set establece la configuración del control para el dispositivo. Los dispositivos de audio de CD, vídeo digital, secuencia de MIDI, VCR, vídeo, superposición de vídeo y de audio y de onda reconocen este comando.
ms.assetid: 1ec4d84e-372a-4b6d-b694-f5afb41f90b2
keywords:
- comando set Windows multimedia
topic_type:
- apiref
api_name:
- set
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914743db038b0cae32b53fa79b7696ddba1ad05b
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2021
ms.locfileid: "105678604"
---
# <a name="set-command"></a>Set (comando)

> [!NOTE]
> Comunicación sin polarización: Microsoft admite un entorno diverso y de inclusión.  Dentro de este documento, hay referencias a la palabra ' Slave '. La guía de estilo de Microsoft [para Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) lo reconoce como una palabra de exclusión.  Este texto se usa tal como está actualmente el texto que se usa en los comandos. Para mantener la coherencia, este documento contiene esta palabra. Cuando se modifique esta palabra en los comandos, se corregirá este documento para que esté alineado.


El comando set establece la configuración del control para el dispositivo. Los dispositivos de audio de CD, vídeo digital, secuencia de MIDI, VCR, vídeo, superposición de vídeo y de audio y de onda reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

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

Marca para establecer la configuración del control. En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **set** y las marcas usadas por cada tipo.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de dispositivo</th>
<th>Marcas de comandos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>cdaudio</td>
<td><ul>
<li>todo desactivado de audio</li>
<li>audio todo activado</li>
<li>audio abandonado</li>
<li>audio a la izquierda</li>
<li>audio a la derecha</li>
<li>audio a la derecha</li>
<li>puerta cerrada</li>
<li>puerta abierta</li>
<li>milisegundos de formato de hora</li>
<li>formato de hora MSF</li>
<li>formato de hora TMSF</li>
</ul></td>
</tr>
<tr class="even">
<td>digitalvideo</td>
<td><ul>
<li>todo desactivado de audio</li>
<li>audio todo activado</li>
<li>audio abandonado</li>
<li>audio a la izquierda</li>
<li>audio a la derecha</li>
<li>audio a la derecha</li>
<li>puerta cerrada</li>
<li>puerta abierta</li>
<li><em>formato</em> de formato de archivo</li>
<li>Buscar exactamente</li>
<li>Buscar exactamente desactivado</li>
<li><em>factor</em> de velocidad</li>
<li><em>formato</em> de formato de archivo todavía</li>
<li>marcos de formato de hora</li>
<li>milisegundos de formato de hora</li>
<li>vídeo desactivado</li>
<li>vídeo sobre</li>
</ul></td>
</tr>
<tr class="odd">
<td>overlay</td>
<td><ul>
<li>todo desactivado de audio</li>
<li>audio todo activado</li>
<li>audio abandonado</li>
<li>audio a la izquierda</li>
<li>audio a la derecha</li>
<li>audio a la derecha</li>
<li>puerta cerrada</li>
<li>puerta abierta</li>
<li>vídeo desactivado</li>
<li>vídeo sobre</li>
</ul></td>
</tr>
<tr class="even">
<td>sequencer</td>
<td><ul>
<li>todo desactivado de audio</li>
<li>audio todo activado</li>
<li>audio abandonado</li>
<li>audio a la izquierda</li>
<li>audio a la derecha</li>
<li>audio a la derecha</li>
<li>puerta cerrada</li>
<li>puerta abierta</li>
<li>MIDI maestro</li>
<li>ninguno principal</li>
<li>SMPTE maestro</li>
<li><em>tiempo</em> de desplazamiento</li>
<li>Asignador de puertos</li>
<li>Puerto ninguno</li>
<li><em>port_number</em> de Puerto</li>
<li>archivo esclavo</li>
<li>MIDI esclavo</li>
<li>ninguno subordinado</li>
<li>SMPTE esclavo</li>
<li><em>tempo_value</em> de tempo</li>
<li>milisegundos de formato de hora</li>
<li>formato de hora SMPTE <em>fps</em></li>
<li>formato de hora SMPTE 30 Drop</li>
<li>formato de hora, puntero de canción</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>vídeos</strong></td>
<td><ul>
<li>ensamblar registro en</li>
<li>Ensamblaje de registro desactivado</li>
<li>todo desactivado de audio</li>
<li>audio todo activado</li>
<li>audio abandonado</li>
<li>audio a la izquierda</li>
<li>audio a la derecha</li>
<li>audio a la derecha</li>
<li><em>hora</em> del reloj</li>
<li>formato del contador</li>
<li><em>valor</em> del contador</li>
<li>puerta cerrada</li>
<li>puerta abierta</li>
<li>contador de índice</li>
<li>fecha de índice</li>
<li>tiempo de índice</li>
<li>tiempo de índice</li>
<li><em>duración</em> de CodeLength</li>
<li><em>tiempo de espera</em> de pausa</li>
<li>duración de PostRoll-</li>
<li><em>duration</em></li>
<li>encendido</li>
<li>desconectar</li>
<li><em>duración</em> de la duración del prelanzamiento</li>
<li>formato de registro SP</li>
<li>formato de registro LP</li>
<li>formato de registro EP</li>
<li><em>factor</em> de velocidad</li>
<li>marcos de formato de hora</li>
<li>formato de hora HMS</li>
<li>milisegundos de formato de hora</li>
<li>formato de hora MSF</li>
<li>formato de hora SMPTE <em>fps</em></li>
<li>formato de hora SMPTE 30 Drop</li>
<li>formato de hora TMSF</li>
<li>contador de modo de tiempo</li>
<li>detección del modo de tiempo</li>
<li>código de tiempo del modo de tiempo</li>
<li>más seguimiento</li>
<li>seguimiento menos</li>
<li>restablecimiento de seguimiento</li>
</ul></td>
</tr>
<tr class="even">
<td>videodisco</td>
<td><ul>
<li>todo desactivado de audio</li>
<li>audio todo activado</li>
<li>audio abandonado</li>
<li>audio a la izquierda</li>
<li>audio a la derecha</li>
<li>audio a la derecha</li>
<li>puerta cerrada</li>
<li>puerta abierta</li>
<li>marcos de formato de hora</li>
<li>formato de hora HMS</li>
<li>milisegundos de formato de hora</li>
<li>seguimiento de formato de hora</li>
<li>vídeo desactivado</li>
<li>vídeo sobre</li>
</ul></td>
</tr>
<tr class="odd">
<td>waveaudio</td>
<td><ul>
<li><em>entero</em> de alineación</li>
<li>cualquier entrada</li>
<li>cualquier salida</li>
<li>todo desactivado de audio</li>
<li>audio todo activado</li>
<li>audio abandonado</li>
<li>audio a la izquierda</li>
<li>audio a la derecha</li>
<li>audio a la derecha</li>
<li><em>BIT_COUNT</em> BitsPerSample</li>
<li><em>byte_rate</em> bytespersec</li>
<li>canales <em>channel_count</em></li>
<li>puerta cerrada</li>
<li>puerta abierta</li>
<li>PCM de etiqueta de formato</li>
<li><em>etiqueta</em> de etiqueta de formato</li>
<li><em>entero</em> de entrada</li>
<li><em>entero</em> de salida</li>
<li><em>entero</em> SamplesPerSec</li>
<li>bytes de formato de hora</li>
<li>milisegundos de formato de hora</li>
<li>ejemplos de formato de hora</li>
</ul></td>
</tr>
</tbody>
</table>



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszSetting** y su significado.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>entero</em> de alineación</td>
<td>Establece la alineación de los bloques de datos en relación con el inicio de los datos pasados al dispositivo de audio de onda. El archivo se guarda en este formato.</td>
</tr>
<tr class="even">
<td>cualquier entrada</td>
<td>Use cualquier entrada que admita el formato actual al grabar. Esta es la configuración predeterminada.</td>
</tr>
<tr class="odd">
<td>cualquier salida</td>
<td>Use cualquier salida que admita el formato actual al reproducirlo. Este es el valor predeterminado.</td>
</tr>
<tr class="even">
<td>ensamblar registro en <br/> Ensamblaje de registro desactivado <br/></td>
<td>En el modo de ensamblado, todas las pistas se registran tal y como se define en el dispositivo. La mayoría de los VCR están en modo de ensamblado de forma predeterminada.</td>
</tr>
<tr class="odd">
<td>todo desactivado de audio <br/> audio todo activado <br/></td>
<td>Deshabilita o habilita la salida de audio. Los dispositivos de superposición de vídeo, el secuenciador MCISEQ y el dispositivo de audio de onda MCIWAVE no admiten esta marca.</td>
</tr>
<tr class="even">
<td>audio abandonado <br/> audio a la izquierda <br/> audio a la derecha <br/> audio a la derecha <br/></td>
<td>Deshabilita o habilita la salida en el canal de audio izquierdo o derecho. Los dispositivos de superposición de vídeo, el secuenciador MCISEQ y el dispositivo de audio de onda MCIWAVE no admiten esta marca.</td>
</tr>
<tr class="odd">
<td><em>BIT_COUNT</em> BitsPerSample</td>
<td>Establece el número de bits por muestra de código PCM (modulación por pulsos) reproducido o grabado. El archivo se guarda en este formato.</td>
</tr>
<tr class="even">
<td><em>byte_rate</em> bytespersec</td>
<td>Establece el número medio de bytes por segundo que se reproducen o registran. El archivo se guarda en este formato.</td>
</tr>
<tr class="odd">
<td>canales <em>channel_count</em></td>
<td>Establece los canales para reproducir y grabar. El archivo se guarda en este formato.</td>
</tr>
<tr class="even">
<td><em>hora</em> del reloj</td>
<td>Establece la hora del reloj externo a la <em>hora.</em> El formato se especifica como un entero largo sin signo.</td>
</tr>
<tr class="odd">
<td>formato del contador</td>
<td>Establezca el formato de hora para el contador, devuelto por el contador de <a href="status.md">Estado</a> &quot; &quot; . Para obtener información sobre los tipos aplicables, consulte el comando <strong>set</strong> &quot; Time format &quot; .</td>
</tr>
<tr class="even">
<td><em>valor</em> del contador</td>
<td>Establece el contador VCR en el valor especificado. El valor debe especificarse en el formato del contador actual. Para obtener más información, consulte el comando <strong>set</strong> &quot; Counter format &quot; .</td>
</tr>
<tr class="odd">
<td>puerta cerrada</td>
<td>Retira la bandeja y cierra la puerta, si es posible. Para VCR, carga la cinta automáticamente.</td>
</tr>
<tr class="even">
<td>puerta abierta</td>
<td>Abre la puerta y expulsa la bandeja o la cinta, si es posible.</td>
</tr>
<tr class="odd">
<td><em>formato</em> de formato de archivo</td>
<td>Especifica un formato de archivo que se usa para los comandos <a href="save.md">Guardar</a> o <a href="capture.md">capturar</a> . Si se omite, puede que el valor predeterminado sea un formato definido por el controlador de dispositivo. Si el formato de archivo especificado entra en conflicto con el algoritmo y la calidad seleccionados actualmente, se cambian a los valores predeterminados para el formato de archivo. Se definen los siguientes formatos de archivo:
<ul>
<li>AVI: especifica el formato AVI.</li>
<li>AVSS: especifica el formato de AVSS.</li>
<li>DIB: especifica el formato DIB.</li>
<li>JFIF: especifica el formato JFIF.</li>
<li>JPEG: especifica el formato JPEG.</li>
<li>MPEG: especifica el formato MPEG.</li>
<li>RDIB: especifica el formato DIB de RLE.</li>
<li>RJPEG: especifica el formato de RJPEG.</li>
</ul></td>
</tr>
<tr class="even">
<td>PCM de etiqueta de formato</td>
<td>Establece el tipo de formato en PCM para reproducir y grabar. El archivo se guarda en este formato.</td>
</tr>
<tr class="odd">
<td><em>etiqueta</em> de etiqueta de formato</td>
<td>Establece el tipo de formato para reproducir y grabar. El archivo se guarda en este formato.</td>
</tr>
<tr class="even">
<td>código de tiempo de índice <br/> contador de índice <br/> fecha de índice <br/> tiempo de índice <br/></td>
<td>Establece la pantalla de presentación actual en el VCR.</td>
</tr>
<tr class="odd">
<td><em>entero</em> de entrada</td>
<td>Establece el canal de audio que se usa como entrada.</td>
</tr>
<tr class="even">
<td><em>duración</em> de la longitud</td>
<td>Establece la longitud especificada por el usuario de la cinta en el VCR. Este valor lo devuelve el <a href="status.md"></a> &quot; comando de longitud &quot; de estado y se proporciona para ofrecer compatibilidad con las aplicaciones que requieren este comando para devolver una longitud válida.</td>
</tr>
<tr class="odd">
<td>MIDI maestro</td>
<td>Establece el secuenciador MIDI como el origen de la sincronización. Los datos de sincronización se envían en formato MIDI. El secuenciador MCISEQ no admite esta marca.</td>
</tr>
<tr class="even">
<td>ninguno principal</td>
<td>Impide que el secuenciador MIDI envíe datos de sincronización. El secuenciador MCISEQ no admite esta marca.</td>
</tr>
<tr class="odd">
<td>SMPTE maestro</td>
<td>Establece el secuenciador MIDI como el origen de la sincronización. Los datos de sincronización se envían en formato SMPTE (sociedad de los ingenieros de películas y televisión). El secuenciador MCISEQ no admite esta marca.</td>
</tr>
<tr class="even">
<td><em>tiempo</em> de desplazamiento</td>
<td>Establece el <em>tiempo</em>de desplazamiento de SMPTE. El desplazamiento es la hora de inicio de una secuencia basada en SMPTE. La <em>hora</em> se expresa como <em>HH</em>: <em>mm</em>: <em>SS</em>: <em>FF</em>, donde <em>HH</em> es hours, <em>mm</em> es minutes, <em>SS</em> is seconds y <em>FF</em> es frames.</td>
</tr>
<tr class="odd">
<td><em>entero</em> de salida</td>
<td>Establece el canal de audio que se usa como salida.</td>
</tr>
<tr class="even">
<td><em>tiempo de espera</em> de pausa</td>
<td>Establece la duración máxima, en milisegundos, de un comando <a href="pause.md">PAUSE</a> . Un valor de tiempo de <em>espera</em> cero indica que no se producirá ningún tiempo de espera.</td>
</tr>
<tr class="odd">
<td><em>duración</em> de la duración de PostRoll</td>
<td>Establece la longitud, en el formato de hora actual, necesaria para frenar el transporte del VCR cuando se emite un comando <a href="stop.md">detener</a> o <strong>pausar</strong> .</td>
</tr>
<tr class="even">
<td>Asignador de puertos</td>
<td>Establece el asignador MIDI como el puerto que recibe los mensajes MIDI. Este comando genera un error si otra aplicación está usando el asignador de MIDI o un puerto que necesita.</td>
</tr>
<tr class="odd">
<td>Puerto ninguno</td>
<td>Deshabilita el envío de mensajes MIDI. Este comando también cierra un puerto MIDI.</td>
</tr>
<tr class="even">
<td><em>port_number</em> de Puerto</td>
<td>Establece el puerto MIDI que recibe los mensajes MIDI. Este comando produce un error si otra aplicación está usando el puerto que está intentando abrir.</td>
</tr>
<tr class="odd">
<td>encendido <br/> desconectar <br/></td>
<td>Establece la capacidad del dispositivo en ON u OFF.</td>
</tr>
<tr class="even">
<td><em>duración</em> de la duración del prelanzamiento</td>
<td>Establece la longitud, en el formato de hora actual, necesaria para estabilizar la salida del VCR.</td>
</tr>
<tr class="odd">
<td>formato de registro SP <br/> formato de registro LP <br/> formato de registro EP <br/></td>
<td>Establece el modo de grabación para el VCR en SP para reproducción estándar, EP para reproducción extendida o LP para larga reproducción. Estos valores no pretenden ser específicos de VHS. Se asignan a tres modos adecuados con otros formatos de cinta. Por ejemplo, SP se asigna a la grabación más rápida y de mayor calidad.</td>
</tr>
<tr class="even">
<td><em>entero</em> SamplesPerSec</td>
<td>Establece la velocidad de muestreo para reproducir y grabar. El archivo se guarda en este formato.</td>
</tr>
<tr class="odd">
<td>Buscar exactamente<br/> Buscar exactamente desactivado <br/></td>
<td>Selecciona uno de dos modos de búsqueda. Con &quot; Seek exactamente en &quot; , Seek siempre se moverá al marco especificado. Con &quot; Seek exactamente OFF &quot; , Seek se moverá al fotograma clave más cercano antes del marco especificado.</td>
</tr>
<tr class="even">
<td>archivo esclavo</td>
<td>Establece que el secuenciador MIDI Use los datos de archivo como origen de la sincronización. Esta es la configuración predeterminada.</td>
</tr>
<tr class="odd">
<td>MIDI esclavo</td>
<td>Establece que el secuenciador MIDI Use los datos MIDI entrantes para el origen de la sincronización. Sequencer reconoce los datos de sincronización con el formato MIDI. El secuenciador MCISEQ no admite esta marca.</td>
</tr>
<tr class="even">
<td>ninguno subordinado</td>
<td>Establece que el secuenciador MIDI omita la sincronización</td>
</tr>
<tr class="odd">
<td>SMPTE esclavo</td>
<td>Establece que el secuenciador MIDI Use los datos MIDI entrantes para el origen de la sincronización. Sequencer reconoce los datos de sincronización con el formato SMPTE. El secuenciador MCISEQ no admite esta marca.</td>
</tr>
<tr class="even">
<td>factor de velocidad</td>
<td>Establece la velocidad relativa de reproducción de vídeo y audio desde el área de trabajo. Factor es la proporción entre la velocidad de fotogramas nominal y la velocidad de fotogramas deseada, donde la velocidad de fotogramas nominal se designa como 1000. (Una tasa de 500 es la velocidad media normal, 2000 es el doble de velocidad normal, etc.). Al establecer la velocidad en cero, el vídeo se reproduce lo más rápido posible sin quitar fotogramas y sin audio.</td>
</tr>
<tr class="odd">
<td><em>formato</em> de formato de archivo todavía</td>
<td>Especifica el formato de archivo utilizado para los comandos de captura.</td>
</tr>
<tr class="even">
<td>tempo_value de tempo</td>
<td>Establece el tempo de la secuencia de acuerdo con el formato de hora actual. Para un archivo basado en PPQN, el tempo_value se interpreta como pulsaciones por minuto. Para un archivo basado en SMPTE, el tempo_value se interpreta como fotogramas por segundo.</td>
</tr>
<tr class="odd">
<td>bytes de formato de hora</td>
<td>En un formato de archivo PCM, establece el formato de hora en bytes. Toda la información de posición se especifica como bytes después de este comando.</td>
</tr>
<tr class="even">
<td>marcos de formato de hora</td>
<td>Establece el formato de hora en fotogramas. Todos los comandos que usan valores de posición asumirán fotogramas. Cuando el dispositivo está abierto, el modo predeterminado es tramas. Compatible con los discos de videodisco con el formato CAV.</td>
</tr>
<tr class="odd">
<td>formato de hora HMS</td>
<td>Establece el formato de hora en horas, minutos y segundos. Todos los comandos que usan valores de posición asumirán HMS. HMS es el formato predeterminado para los videodiscos de CLV. Especifique un valor de HMS como HH: mm: SS, donde HH es horas, mm son minutos y SS es segundos. Puede omitir un campo si este y todos los campos siguientes son cero. Por ejemplo, 3, 3:0 y 3:0:0 son formas válidas de expresar 3 horas. <br/></td>
</tr>
<tr class="even">
<td>milisegundos de formato de hora</td>
<td>Establece el formato de hora en milisegundos. Todos los comandos que usan valores de posición supondrán milisegundos. Puede abreviar los milisegundos como &quot; MS &quot; . En el caso de los dispositivos del secuenciador, el archivo de secuencia establece el formato predeterminado en PPQN o SMPTE. Los dispositivos de superposición de vídeo no admiten esta marca.<br/></td>
</tr>
<tr class="odd">
<td>formato de hora MSF</td>
<td>Establece el formato de hora en minutos, segundos y fotogramas. Todos los comandos que usan valores de posición asumirán MSF (el formato predeterminado para el audio de CD). Especifique un valor de MSF como mm: SS: FF, donde mm es minutos, SS es segundos y FF es fotogramas. Puede omitir un campo si este y todos los campos siguientes son cero. Por ejemplo, 3, 3:0 y 3:0:0 son formas válidas de expresar 3 minutos.<br/> Los campos de MSF tienen los siguientes valores máximos:<br/>
<ul>
<li>Minutos 99</li>
<li>Segundos 59</li>
<li>Marcos 74</li>
</ul></td>
</tr>
<tr class="even">
<td>ejemplos de formato de hora</td>
<td>Establece el formato de hora en samples. Toda la información de posición se especifica como ejemplos que siguen este comando.</td>
</tr>
<tr class="odd">
<td>formato de hora SMPTE 24<br/> formato de hora SMPTE 25<br/> formato de hora SMPTE 30<br/></td>
<td>Establece el formato de hora en una velocidad de fotogramas SMPTE. Para VCR, establece el formato de hora en HH: mm: SS: FF, donde los valores válidos son de 00:00:00:00 a 23:59:59: XX y XX es uno menos que los fotogramas por segundo, según se especifica en el número 24, 25 o 30, tal y como se especifica en la marca. En la entrada, dos puntos (:) se requieren para separar los componentes. Las unidades menos significativas se pueden omitir si son 00; por ejemplo, 02:00 es igual que 02:00:00:00. Todos los comandos que usan valores de posición adoptarán el formato SMPTE.<br/> El archivo de secuencia establece el formato predeterminado en PPQN o SMPTE.<br/></td>
</tr>
<tr class="even">
<td>formato de hora SMPTE 30 Drop</td>
<td>Establece el formato de hora en la velocidad de fotogramas de eliminación SMPTE 30. Para VCR, igual que SMPTE 30, con la excepción de que ciertas posiciones de código de tiempo se quitan del formato para que las posiciones de código de tiempo grabadas para cada fotograma (en la velocidad de fotogramas NTSC de 29,97 fps) se correspondan a tiempo real (30 fps). Las posiciones de código de tiempo que se quitan son las siguientes: dos cada minuto, por minuto, durante los primeros nueve de cada diez minutos de contenido grabado. Por ejemplo, en 01:04:59:29, la siguiente posición del código de tiempo sería 01:05:00:02, no 01:05:00:00. Todos los comandos que usan valores de posición adoptarán el formato SMPTE.<br/> El archivo de secuencia establece el formato predeterminado en PPQN o SMPTE.<br/></td>
</tr>
<tr class="odd">
<td>formato de hora, puntero de canción</td>
<td>Establece el formato de hora en el puntero de canción (decimosexto notas). Todos los comandos que usan valores de posición asumirán las unidades de puntero de la canción. Esta marca solo es válida para una secuencia de tipo de división PPQN.</td>
</tr>
<tr class="even">
<td>formato de hora TMSF</td>
<td>Establece el formato de hora en pistas, minutos, segundos y fotogramas. Todos los comandos que usan valores de posición asumirán TMSF. Especifique un valor de TMSF como TT: mm: SS: FF, donde TT es pistas, mm es minutos, SS es segundos y FF es fotogramas. Puede omitir un campo si este y todos los campos siguientes son cero. Por ejemplo, 3, 3:0, 3:0:0 y 3:0:0:0 son formas válidas de expresar el seguimiento 3. <br/> Los campos TMSF tienen los siguientes valores máximos:<br/>
<ul>
<li>Realiza un seguimiento de 99</li>
<li>Minutos 90</li>
<li>Segundos 59</li>
<li>Marcos 74</li>
</ul></td>
</tr>
<tr class="odd">
<td>seguimiento de formato de hora</td>
<td>Establece el formato de posición en las pistas. Todos los comandos que usan valores de posición asumirán pistas.</td>
</tr>
<tr class="even">
<td>contador de modo de tiempo</td>
<td>Establece el modo de información de posición para utilizar los contadores de VCR.</td>
</tr>
<tr class="odd">
<td>detección del modo de tiempo</td>
<td>Establece el modo de información de posición en función de la detección de información de código de tiempo en la cinta. Si se detecta información de código de tiempo, el tipo de tiempo se establece en código de tiempo &quot; &quot; ; de lo contrario, el tipo de hora se establece en &quot; Counter &quot; . &quot;&quot;La detección es un modo especial. Cada vez que se abre el controlador, se inserta una nueva cinta o &quot; se emite el comando de modo de hora &quot; , el controlador comprueba el modo de hora actual disponible en la cinta y establece el &quot; tipo de hora &quot; en código de tiempo &quot; &quot; o &quot; contador &quot; . Una vez &quot; establecido el tipo de tiempo &quot; , el controlador no lo cambia hasta que no se produce una de las condiciones anteriores.<br/></td>
</tr>
<tr class="even">
<td>código de tiempo del modo de tiempo</td>
<td>Establece el modo de información de posición para utilizar &quot; &quot; la información de código de tiempo de la cinta.</td>
</tr>
<tr class="odd">
<td>más seguimiento <br/> seguimiento menos <br/> restablecimiento de seguimiento <br/></td>
<td>Ajusta la velocidad del transporte de cinta de vídeo en incrementos precisos. Use las &quot; &quot; marcas de seguimiento cuando se obtenga una imagen ruidosa de un VCR. &quot;El seguimiento más &quot; aumenta la velocidad de transporte. &quot;El seguimiento menos &quot; disminuye la velocidad de transporte. &quot;El restablecimiento de seguimiento &quot; devuelve el ajuste de seguimiento a cero.</td>
</tr>
<tr class="even">
<td>vídeo desactivado</td>
<td>Deshabilita la salida de vídeo.</td>
</tr>
<tr class="odd">
<td>vídeo sobre</td>
<td>Habilita la salida de vídeo.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Se definen varias propiedades de los datos de audio de forma de onda cuando se crea el archivo en el que se almacenan los datos. Estas propiedades describen cómo se estructuran los datos en el archivo y no se pueden cambiar una vez que se inicia la grabación. En la lista siguiente se identifican estas propiedades:

-   alineación
-   bitspersample
-   bytespersec
-   canales nueva
-   etiqueta de formato
-   samplespersec

## <a name="examples"></a>Ejemplos

El siguiente comando establece el formato de hora en milisegundos y establece el formato de audio de forma de onda en 8 bits, mono, 11 kHz.

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

[Cadenas de comandos MCI](mci-command-strings.md)
</dt> <dt>

[grabar](capture.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[guardar](save.md)
</dt> <dt>

[stop](stop.md)
</dt> </dl>

 

