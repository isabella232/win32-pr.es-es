---
title: comando status
description: El comando status solicita información de estado de un dispositivo. Todos los dispositivos reconocen este comando.
ms.assetid: 39961bd7-866d-450d-9fbf-347a8f508481
keywords:
- comando status Windows Multimedia
topic_type:
- apiref
api_name:
- status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd209ed04e51671ce7d9c8a7ae88a79073836c2e
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370148"
---
# <a name="status-command"></a>comando status

> [!NOTE]
> La comunicación sin sesgos de Microsoft admite un entorno diverso e inclusario.  Dentro de este documento, hay referencias a la palabra "subordinada". La Guía de estilo de Microsoft [Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) lo reconoce como una palabra excluyente.  Esta redacción se usa, ya que actualmente es la que se usa en los comandos. Por coherencia, este documento contiene esta palabra. Cuando esta palabra se modifica en los comandos, corregiremos este documento para que esté alineado.

El comando status solicita información de estado de un dispositivo. Todos los dispositivos reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("status %s %s %s"),
  lpszDeviceID,
  lpszRequest,
  lpszFlags
);
      
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*
</dt> <dd>

Marca para solicitar información de estado. En la tabla siguiente se enumeran los tipos de dispositivo que reconocen el comando **de** estado y las marcas usadas por cada tipo.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de dispositivo</th>
<th>Marcas de solicitud</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>cdaudio</td>
<td><ul>
<li>cdaudio type track <em>number</em></li>
<li>pista actual</li>
<li>length</li>
<li>número de pista de <em>longitud</em></li>
<li>medios presentes</li>
<li>mode</li>
<li>número de pistas</li>
<li>position</li>
<li>número de seguimiento de <em>posición</em></li>
<li>ready</li>
<li>posición inicial</li>
<li>formato de hora</li>
</ul></td>
</tr>
<tr class="even">
<td>digitalvideo</td>
<td><ul>
<li>audio</li>
<li>alineación de audio</li>
<li>bitspersample de audio</li>
<li>saltos de audio</li>
<li>bytes de audiopersec</li>
<li>entrada de audio</li>
<li>registro de audio</li>
<li>origen de audio</li>
<li>ejemplos de audiopersec</li>
<li>secuencia de audio</li>
<li>Bajo</li>
<li>bitsperpel</li>
<li>luminosidad</li>
<li>color</li>
<li>contraste</li>
<li>pista actual</li>
<li>unidad de espacio en <em>disco</em></li>
<li>finalización de archivos</li>
<li>formato del archivo</li>
<li>modo de archivo</li>
<li>forward</li>
<li>fotogramas omitido</li>
<li>gamma</li>
<li>input</li>
<li>volumen izquierdo</li>
<li>length</li>
<li>número de pista de <em>longitud</em></li>
<li>medios presentes</li>
<li>mode</li>
<li>monitor</li>
<li>método monitor</li>
<li>Nominal</li>
<li>velocidad de fotogramas nominal</li>
<li>velocidad de fotogramas de registros nominales</li>
<li>número de pistas</li>
<li>output</li>
<li>controlador de paleta</li>
<li>modo de pausa</li>
<li>velocidad de reproducción</li>
<li>position</li>
<li>número de seguimiento de <em>posición</em></li>
<li>ready</li>
<li>velocidad de fotogramas de registro</li>
<li>marco de <em>referencia</em></li>
<li>tamaño reservado</li>
<li>volumen derecho</li>
<li>buscar exactamente</li>
<li>Nitidez</li>
<li>Smpte</li>
<li>velocidad</li>
<li>posición inicial</li>
<li>formato de archivo still</li>
<li>formato de hora</li>
<li>Tinte</li>
<li>Agudos</li>
<li>Inconversos</li>
<li>video</li>
<li>índice de clave de vídeo</li>
<li>color de la clave de vídeo</li>
<li>grabación de vídeo</li>
<li>origen de vídeo</li>
<li>número de origen del vídeo</li>
<li>secuencia de vídeo</li>
<li>volumen</li>
<li>identificador de ventana</li>
<li>ventana visible</li>
<li>ventana minimizada</li>
<li>ventana maximizada</li>
</ul></td>
</tr>
<tr class="odd">
<td>overlay</td>
<td><ul>
<li>medios presentes</li>
<li>mode</li>
<li>número de pistas</li>
<li>ready</li>
<li>ajustar</li>
<li>identificador de ventana</li>
</ul></td>
</tr>
<tr class="even">
<td>sequencer</td>
<td><ul>
<li>pista actual</li>
<li>tipo de división</li>
<li>length</li>
<li>length track <em>number</em> master</li>
<li>medios presentes</li>
<li>mode</li>
<li>número de pistas</li>
<li>offset</li>
<li>port</li>
<li>position</li>
<li>número de seguimiento de <em>posición</em></li>
<li>ready</li>
<li>Esclavo</li>
<li>posición inicial</li>
<li>Tempo</li>
<li>formato de hora</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vcr</td>
<td><ul>
<li>ensamblado del registro</li>
<li>monitor de audio</li>
<li>número de monitor de audio</li>
<li>registro de audio</li>
<li>número de pista de la grabación de <em>audio</em></li>
<li>origen de audio</li>
<li>número de origen de audio</li>
<li>canal</li>
<li>número de tuner de <em>canal</em></li>
<li>clock</li>
<li>id. de reloj</li>
<li>counter</li>
<li>formato de contador</li>
<li>resolución de contadores</li>
<li>pista actual</li>
<li>velocidad de fotogramas</li>
<li>índice</li>
<li>index on</li>
<li>length</li>
<li>número de pista de <em>longitud</em></li>
<li>medios presentes</li>
<li>tipo de medio</li>
<li>mode</li>
<li>número de pistas de audio</li>
<li>número de pistas</li>
<li>número de pistas de vídeo</li>
<li>tiempo de <em>espera de pausa</em></li>
<li>formato de reproducción</li>
<li>position</li>
<li>inicio de posición</li>
<li>número de seguimiento de <em>posición</em></li>
<li>duración del <em>postroll</em></li>
<li>encendido</li>
<li>duración de la inscripción <em>previa</em></li>
<li>ready</li>
<li>formato de registro</li>
<li>velocidad</li>
<li>formato de hora</li>
<li>modo de tiempo</li>
<li>tipo de hora</li>
<li>código de tiempo presente</li>
<li>registro de código de tiempo</li>
<li>tipo de código de tiempo</li>
<li>número de afinador</li>
<li>monitor de vídeo</li>
<li>número de monitor de vídeo</li>
<li>grabación de vídeo</li>
<li>número de pista de la grabación de <em>vídeo</em></li>
<li>origen de vídeo</li>
<li>número de origen del vídeo</li>
<li>escritura protegida</li>
</ul></td>
</tr>
<tr class="even">
<td>Videodisco</td>
<td><ul>
<li>pista actual</li>
<li>tamaño del disco</li>
<li>forward</li>
<li>length</li>
<li>número de pista de <em>longitud</em></li>
<li>medios presentes</li>
<li>tipo de medio</li>
<li>mode</li>
<li>número de pistas</li>
<li>position</li>
<li>número de seguimiento de <em>posición</em></li>
<li>ready</li>
<li>Lado</li>
<li>velocidad</li>
<li>posición inicial</li>
<li>formato de hora</li>
</ul></td>
</tr>
<tr class="odd">
<td>waveaudio</td>
<td><ul>
<li>alineación</li>
<li>bitspersample</li>
<li>bytespersec</li>
<li>canales nueva</li>
<li>pista actual</li>
<li>etiqueta de formato</li>
<li>input</li>
<li>length</li>
<li>número de pista <em>de longitud</em></li>
<li>Nivel</li>
<li>medios presentes</li>
<li>mode</li>
<li>número de pistas</li>
<li>output</li>
<li>position</li>
<li>número de seguimiento de <em>posición</em></li>
<li>ready</li>
<li>samplespersec</li>
<li>posición inicial</li>
<li>formato de hora</li>
</ul></td>
</tr>
</tbody>
</table>



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el **parámetro lpszRequest** y sus significados.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>alineación</td>
<td>Devuelve la alineación de bloques de datos, en bytes.</td>
</tr>
<tr class="even">
<td>ensamblar registro</td>
<td>Devuelve <strong>TRUE</strong> si el dispositivo está establecido para la grabación en modo de ensamblado.</td>
</tr>
<tr class="odd">
<td>audio</td>
<td>Devuelve &quot; on o off en función del comando &quot; &quot; &quot; <a href="setaudio.md">setaudio</a> &quot; on o off más &quot; &quot; &quot; reciente. Devuelve on &quot; si uno o ambos &quot; oradores están habilitados y &quot; desactivados en caso &quot; contrario.</td>
</tr>
<tr class="even">
<td>alineación de audio</td>
<td>Devuelve la alineación de los bloques de datos con respecto al inicio de los datos de audio de forma de onda de entrada.</td>
</tr>
<tr class="odd">
<td>audio bitspersample</td>
<td>Devuelve el número de bits por muestra que usa el dispositivo para la grabación. Esta marca solo se aplica a los dispositivos que admiten el &quot; algoritmo &quot; pcm.</td>
</tr>
<tr class="even">
<td>pausas de audio</td>
<td>Devuelve el número de veces que se interrumpió la parte de audio de la última secuencia AVI. El sistema cuenta una interrupción de audio cada vez que intenta escribir datos de audio en el controlador del dispositivo y detecta que el controlador ya ha reproducidos todos los datos disponibles. Esta marca solo la reconoce el controlador de vídeo digital MCIAVI. Está pensado solo para la evaluación del rendimiento; El valor devuelto es difícil de interpretar.</td>
</tr>
<tr class="odd">
<td>audio bytespersec</td>
<td>Devuelve el número medio de bytes por segundo usados para la grabación.</td>
</tr>
<tr class="even">
<td>entrada de audio</td>
<td>Devuelve el nivel de audio instantáneo aproximado de la señal de audio de entrada análoga. Un valor mayor que 1000 implica la distorsión del recorte. Algunos dispositivos solo pueden devolver este valor durante la grabación de audio. El valor no tiene ningún <a href="set.md">comando set</a> <a href="setaudio.md">o setaudio</a> asociado.</td>
</tr>
<tr class="odd">
<td>monitor de audio</td>
<td>Devuelve &quot; la salida o uno de los tipos de entrada de origen &quot; válidos. Para más información, consulte el <strong>comando setaudio</strong> &quot; &quot; monitor.</td>
</tr>
<tr class="even">
<td>número de monitor de audio</td>
<td>Devuelve el número de vídeo supervisado del <strong></strong> tipo especificado por el &quot; monitor de audio de estado &quot; . Para obtener más información, vea el <a href="setaudio.md">comando setaudio.</a></td>
</tr>
<tr class="odd">
<td>registro de audio</td>
<td>Devuelve &quot; on o off , lo que refleja el estado establecido por &quot; &quot; &quot; <strong>setaudio</strong> &quot; record &quot; .</td>
</tr>
<tr class="even">
<td>número de pista de la grabación de <em>audio</em></td>
<td>Devuelve <strong>TRUE</strong> si vcr está establecido para grabar audio. Si no se da ningún número de pista, se supone que el valor predeterminado es 1.</td>
</tr>
<tr class="odd">
<td>audio samplespersec</td>
<td>Devuelve el número de muestras por segundo grabadas.</td>
</tr>
<tr class="even">
<td>origen de audio</td>
<td>Devuelve el origen actual del digitalizador de audio: &quot; left , right , average o &quot; &quot; &quot; &quot; &quot; &quot; &quot; stereo.</td>
</tr>
<tr class="odd">
<td>número de origen de audio</td>
<td>Devuelve el número de origen de audio del tipo devuelto por el <strong>origen de</strong> audio de &quot; estado &quot; . Para obtener más información, vea el <a href="setaudio.md">comando setaudio.</a></td>
</tr>
<tr class="even">
<td>secuencia de audio</td>
<td>Devuelve el número de secuencia de audio actual.</td>
</tr>
<tr class="odd">
<td>Bajo</td>
<td>Devuelve el nivel de audio-graves actual.</td>
</tr>
<tr class="even">
<td>bitsperpel</td>
<td>Devuelve el número de bits por píxel para guardar los datos capturados o registrados.</td>
</tr>
<tr class="odd">
<td>bitspersample</td>
<td>Devuelve los bits por ejemplo.</td>
</tr>
<tr class="even">
<td>luminosidad</td>
<td>Devuelve el nivel de brillo del vídeo actual.</td>
</tr>
<tr class="odd">
<td>bytespersec</td>
<td>Devuelve el número medio de bytes por segundo reproducdos o registrados.</td>
</tr>
<tr class="even">
<td>Número de <em></em> pista de tipo cdaudio</td>
<td>Devuelve el tipo del número de pista especificado. Puede ser &quot; audio &quot; u &quot; otro.&quot;</td>
</tr>
<tr class="odd">
<td>canal</td>
<td>Devuelve el valor entero del canal establecido en el tuner.</td>
</tr>
<tr class="even">
<td>número de tuner de <em>canal</em></td>
<td>Si &quot; se da el &quot; <em>número</em> de tuner, se <em></em> devolverá el canal seleccionado actualmente en el número de tuner lógico. Tenga en cuenta que puede haber varios afinadores lógicos.</td>
</tr>
<tr class="odd">
<td>canales nueva</td>
<td>Devuelve el número de canales establecidos (1 para mono, 2 para estéreo).</td>
</tr>
<tr class="even">
<td>clock</td>
<td>Devuelve la hora externa. El tiempo debe ser un entero largo sin signo que exprese incrementos totales. Para más información, consulte el comando <a href="capability.md">de velocidad</a> de incremento del reloj &quot; de &quot; funcionalidad.</td>
</tr>
<tr class="odd">
<td>id. de reloj</td>
<td>Devuelve un entero único que identifica el reloj.</td>
</tr>
<tr class="even">
<td>color</td>
<td>Devuelve el nivel de color actual.</td>
</tr>
<tr class="odd">
<td>contraste</td>
<td>Devuelve el nivel de contraste actual.</td>
</tr>
<tr class="even">
<td>counter</td>
<td>Devuelve la posición del contador, en el formato de contador actual.</td>
</tr>
<tr class="odd">
<td>formato de contador</td>
<td>Devuelve el formato de contador actual. Para obtener más información, vea el <a href="set.md">comando set</a> &quot; counter &quot; format.</td>
</tr>
<tr class="even">
<td>resolución de contadores</td>
<td>Devuelve &quot; &quot; &quot; fotogramas o &quot; segundos, lo que indica la resolución del contador. Esto no es lo mismo que la precisión.</td>
</tr>
<tr class="odd">
<td>pista actual</td>
<td>Devuelve la pista actual. El secuenciador MCISEQ devuelve 1.</td>
</tr>
<tr class="even">
<td>tamaño del disco</td>
<td>Devuelve 8 o 12, lo que indica el tamaño del disco cargado en pulgadas.</td>
</tr>
<tr class="odd">
<td>unidad de espacio en <em>disco</em></td>
<td>Devuelve el espacio en disco aproximado, en el formato de hora actual, que se puede obtener mediante un comando <a href="reserve.md">reserve</a> para la unidad de disco <em>especificada.</em> <em>Normalmente,</em> la unidad se especifica como una sola letra o una sola letra seguida de dos puntos (:). Sin embargo, algunos dispositivos pueden usar una ruta de acceso.</td>
</tr>
<tr class="even">
<td>tipo de división</td>
<td>Devuelve uno de los siguientes tipos de división de archivos:
<ul>
<li>PPQN</li>
<li>Marco SMPTE 24</li>
<li>Marco SMPTE 25</li>
<li>Marco desplegable SMPTE 30</li>
<li>Marco SMPTE 30</li>
</ul>
<br/> Use esta información para determinar el formato del archivo MIDI y el significado de la información de tempo y posición.<br/></td>
</tr>
<tr class="odd">
<td>finalización de archivos</td>
<td>Devuelve el porcentaje estimado que ha progresado <a href="copy.md"></a>una operación de <a href="undo.md"></a> <a href="load.md">carga,</a> <a href="save.md">guardar,</a> <a href="capture.md">capturar,</a> <a href="cut.md">cortar,</a> <a href="delete.md">copiar,</a> <a href="paste.md">eliminar,</a>pegar o deshacer. (Las aplicaciones pueden usar esto para proporcionar un indicador visual del progreso).</td>
</tr>
<tr class="even">
<td>formato del archivo</td>
<td>Devuelve el formato de archivo actual para <a href="record.md">los comandos record</a> o <strong>save.</strong></td>
</tr>
<tr class="odd">
<td>modo de archivo</td>
<td>Devuelve &quot; &quot; cargando , &quot; &quot; guardando, &quot; &quot; editando o &quot; &quot; inactivo. Durante una <a href="load.md"><strong>operación de</strong></a> carga, devuelve la carga &quot; de &quot; . Durante <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>las operaciones</strong></a> de guardado <a href="capture.md"><strong>y</strong></a> captura, devuelve el guardado &quot; de &quot; . Durante <a href="cut.md"><strong>las operaciones de</strong></a>cortar, <a href="copy.md"><strong>copiar,</strong></a> <a href="delete.md"><strong>eliminar,</strong></a> <a href="paste.md"><strong>pegar</strong></a>o <a href="undo.md"><strong>deshacer,</strong></a> devuelve la &quot; edición de &quot; .</td>
</tr>
<tr class="even">
<td>etiqueta de formato</td>
<td>Devuelve la etiqueta de formato.</td>
</tr>
<tr class="odd">
<td>forward</td>
<td>Devuelve <strong>TRUE</strong> si la dirección de reproducción es hacia delante o si el dispositivo no se está reproduciendo.</td>
</tr>
<tr class="even">
<td>velocidad de fotogramas</td>
<td>Devuelve el número de fotogramas por segundo que el dispositivo usará de forma predeterminada. Los dispositivos ÁLISIS devuelven 30, PAL 25, y así sucesivamente.</td>
</tr>
<tr class="odd">
<td>fotogramas omitido</td>
<td>Devuelve el número de fotogramas que no se dibujaron cuando se reproducía la última secuencia AVI. Esta marca solo la reconoce el controlador de vídeo digital MCIAVI. Está pensado solo para la evaluación del rendimiento; El valor devuelto es difícil de interpretar.</td>
</tr>
<tr class="even">
<td>gamma</td>
<td>Devuelve el valor establecido con <a href="setvideo.md"><strong>setvideo</strong></a> &quot; gamma en el &quot; <em>valor</em>.</td>
</tr>
<tr class="odd">
<td>índice</td>
<td>Devuelve la presentación del índice actual. Para obtener más información, vea el <a href="set.md"><strong>comando set</strong></a> &quot; &quot; index.</td>
</tr>
<tr class="even">
<td>index on</td>
<td>Devuelve <strong>TRUE</strong> si el índice está en.</td>
</tr>
<tr class="odd">
<td>input</td>
<td>Devuelve el conjunto de entrada. Si no se establece uno, el error devuelto indica que se puede usar cualquier dispositivo. En el caso de los dispositivos de vídeo digital, modifica la marca de &quot; &quot; bajo, &quot; treble, volumen &quot; , &quot; &quot; &quot; &quot; brillo, &quot; &quot; &quot; &quot; color, &quot; &quot; contraste, &quot; &quot; gamma, &quot; &quot; nigura o tono para que se aplique solo a la entrada. Este es el valor predeterminado al supervisar la entrada.</td>
</tr>
<tr class="even">
<td>volumen izquierdo</td>
<td>Devuelve el conjunto de volúmenes para el canal de audio izquierdo.</td>
</tr>
<tr class="odd">
<td>length</td>
<td>Devuelve la longitud total del medio, en el formato de hora actual. En el caso de los archivos PPQN, la longitud se devuelve en unidades de puntero de canción. En el caso de los archivos SMPTE, se devuelve como <em>hh:mm:ss:ff</em>, donde <em>hh</em> es horas, <em>mm</em> es minutos, <em>ss</em> es segundos y <em>ff</em> es marcos. En el caso de los dispositivos VCR, la duración es de 2 horas (a menos que la longitud se haya cambiado explícitamente mediante el <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>comando set).</strong></a></td>
</tr>
<tr class="even">
<td>número de pista <em>de longitud</em></td>
<td>Devuelve la longitud de la pista, en tiempo o fotogramas, especificada por <em>número</em>. En el caso de los archivos PPQN, la longitud se devuelve en unidades de puntero de canción. En el caso de los archivos SMPTE, se devuelve como <em>hh:mm:ss:ff</em>, donde <em>hh</em> es horas, <em>mm</em> es minutos, <em>ss</em> es segundos y <em>ff</em> es marcos.<br/></td>
</tr>
<tr class="odd">
<td>Nivel</td>
<td>Devuelve el valor de ejemplo de audio PCM actual.</td>
</tr>
<tr class="even">
<td>maestro</td>
<td>Devuelve &quot; &quot; midi, &quot; none &quot; o &quot; smpte &quot; en función del tipo de conjunto de sincronización.</td>
</tr>
<tr class="odd">
<td>medios presentes</td>
<td>Devuelve <strong>TRUE</strong> si el medio se inserta en el dispositivo o <strong>FALSE</strong> en caso contrario. Los dispositivos sequencer, video-overlay, digital-video y audio de forma de onda <strong>devuelven TRUE.</strong></td>
</tr>
<tr class="even">
<td>tipo de medio</td>
<td>Devuelve el tipo de medio. Para VCRS, se trata de &quot; 8 &quot; mm, &quot; &quot; vhs, &quot; svhs, &quot; &quot; &quot; beta, &quot; &quot; Hi8, &quot; edbeta &quot; u otros &quot; &quot; . En el caso de los videodiscos, se trata de RPC, CLV u otros &quot; &quot; , &quot; &quot; &quot; &quot; dependiendo del tipo de vídeodisc.</td>
</tr>
<tr class="odd">
<td>mode</td>
<td>Devuelve el modo actual del dispositivo. Todos los dispositivos pueden devolver &quot; los valores no &quot; listos, en &quot; &quot; pausa, &quot; &quot; reproduciendo y &quot; &quot; detenidos. Algunos dispositivos pueden devolver los valores &quot; &quot; adicionales abiertos , &quot; &quot; estacionados, &quot; de grabación y de &quot; &quot; &quot; búsqueda.</td>
</tr>
<tr class="even">
<td>monitor</td>
<td>Devuelve &quot; el archivo o la entrada &quot; &quot; &quot; . El valor devuelto indica el origen de la presentación actual.</td>
</tr>
<tr class="odd">
<td>método monitor</td>
<td>Devuelve &quot; pre , post o &quot; &quot; &quot; &quot; &quot; direct. El valor devuelto indica el método utilizado para la supervisión de entrada.</td>
</tr>
<tr class="even">
<td>Nominal</td>
<td>El elemento modifica las marcas &quot; de &quot; bajo, &quot; &quot; brillo, &quot; &quot; color, &quot; &quot; contraste, gamma, niticidad, &quot; &quot; &quot; &quot; &quot; &quot; &quot; tono, treble &quot; &quot; &quot; y volumen para devolver el valor nominal en lugar de la configuración actual.</td>
</tr>
<tr class="odd">
<td>velocidad nominal de fotogramas</td>
<td>Devuelve la velocidad de fotogramas nominal asociada al archivo. Las unidades están en fotogramas por segundo multiplicadas por 1000.</td>
</tr>
<tr class="even">
<td>velocidad de fotogramas de registros nominales</td>
<td>Devuelve la velocidad de fotogramas nominal asociada a la señal de vídeo de entrada. Las unidades están en fotogramas por segundo multiplicadas por 1000.</td>
</tr>
<tr class="odd">
<td>número de pistas de audio</td>
<td>Devuelve el número de pistas de audio en el medio.</td>
</tr>
<tr class="even">
<td>número de pistas</td>
<td>Devuelve el número de pistas en el medio. Los dispositivos MCISEQ y MCIWAVE devuelven 1, al igual que la mayoría de los dispositivos VCR. El dispositivo MCIPIONR no admite esta marca.</td>
</tr>
<tr class="odd">
<td>número de pistas de vídeo</td>
<td>Devuelve el número de pistas de vídeo en el medio.</td>
</tr>
<tr class="even">
<td>offset</td>
<td>Devuelve el desplazamiento de un archivo basado en SMPTE. El desplazamiento es la hora de inicio de una secuencia basada en SMPTE. La hora se devuelve <em>como hh:mm:ss:ff</em>, donde <em>hh</em> es horas, <em>mm</em> es minutos, <em>ss</em> es segundos y <em>ff</em> es marcos.</td>
</tr>
<tr class="odd">
<td>output</td>
<td>Devuelve la salida establecida actualmente. Si no se establece ninguna salida, el error devuelto indica que se puede usar cualquier dispositivo. En el caso de los dispositivos de vídeo digital, modifica la marca de &quot; &quot; bajo, &quot; treble, volumen &quot; , &quot; &quot; &quot; &quot; brillo, &quot; &quot; &quot; &quot; color, &quot; &quot; contraste, &quot; &quot; gamma, &quot; &quot; niticidad o tono para que se aplique solo a la salida. Este es el valor predeterminado al supervisar un archivo.</td>
</tr>
<tr class="even">
<td>modo de pausa</td>
<td>Devuelve &quot; la grabación si el dispositivo está en pausa durante la &quot; grabación. Devuelve la &quot; reproducción si el dispositivo está en pausa mientras se &quot; reproduce. Devuelve la acción de error &quot; no aplicable en el modo actual si el dispositivo no está en &quot; pausa.</td>
</tr>
<tr class="odd">
<td>tiempo de espera de pausa</td>
<td>Devuelve la duración máxima, en milisegundos, de un <a href="pause.md"><strong>comando de</strong></a> pausa.</td>
</tr>
<tr class="even">
<td>formato de reproducción</td>
<td>Devuelve un código que indica el formato en el que se reproducirá la cinta de vídeo, si se puede detectar: &quot; lp , ep , sp u otros &quot; &quot; &quot; &quot; &quot; &quot; &quot; . Para obtener más información, vea la &quot; marca de formato de &quot; registro.</td>
</tr>
<tr class="odd">
<td>velocidad de reproducción</td>
<td>Devuelve un valor que representa la coincidencia real del tiempo de reproducción real de la última secuencia AVI con el tiempo de reproducción de destino. El valor 1000 indica que la hora de destino y la hora real eran las mismas. Un valor de 2000, por ejemplo, indicaría que la secuencia AVI tardó el doble de tiempo en reproducirse como debería. Esta marca solo la reconoce el controlador de vídeo digital MCIAVI. Está pensado solo para la evaluación del rendimiento; El valor devuelto es difícil de interpretar.</td>
</tr>
<tr class="even">
<td>port</td>
<td>Devuelve el número de puerto MIDI asignado a la secuencia.</td>
</tr>
<tr class="odd">
<td>position</td>
<td>Devuelve la posición actual. Para los archivos PPQN, la posición se devuelve en unidades de puntero de canción. En el caso de los archivos SMPTE, se devuelve como <em>hh:mm:ss:ff</em>, donde <em>hh</em> es horas, <em>mm</em> es minutos, ss es segundos y <em>ff</em> es marcos.<br/></td>
</tr>
<tr class="even">
<td>position start</td>
<td>Devuelve la posición del inicio del medio utilizable.</td>
</tr>
<tr class="odd">
<td>número de seguimiento de <em>posición</em></td>
<td>Devuelve la posición del inicio de la pista especificada por <em>número</em>. Para los archivos PPQN, el formato de hora se devuelve en unidades de puntero de canción. En el caso de los archivos SMPTE, se devuelve como <em>hh:mm:ss:ff</em>, donde <em>hh</em> es horas, <em>mm</em> es minutos, <em>ss</em> es segundos y <em>ff</em> es marcos. El secuenciador MCISEQ devuelve cero. El dispositivo MCIPIONR no admite esta marca. El dispositivo MCIWAVE devuelve cero.</td>
</tr>
<tr class="even">
<td>duración del postroll</td>
<td>Devuelve la longitud de la cinta de vídeo, en el formato de <a href="pause.md"><strong></strong></a> hora actual, necesaria para interrumpir el transporte de VCR cuando se emite un comando <a href="stop.md"><strong>de</strong></a> detenerse o pausar.</td>
</tr>
<tr class="odd">
<td>encendido</td>
<td>Devuelve <strong>TRUE</strong> si la alimentación del VCR está encendido.</td>
</tr>
<tr class="even">
<td>duración de la inscripción previa</td>
<td>Devuelve la longitud de la cinta de vídeo, en el formato de hora actual, necesaria para estabilizar la salida de VCR.</td>
</tr>
<tr class="odd">
<td>ready</td>
<td>Devuelve <strong>TRUE</strong> si el dispositivo está listo para aceptar otro comando.</td>
</tr>
<tr class="even">
<td>formato de registro</td>
<td>Devuelve un código que indica el formato en el que se grabará la cinta de vídeo. Los tipos de valor devueltos &quot; actuales son lp &quot; , ep , sp u otros &quot; &quot; &quot; &quot; &quot; &quot; . Estos formatos no son específicos de VHS y se pueden aplicar a cualquier VCR que tenga varios formatos de grabación seleccionables. El tipo sp es el formato de grabación más rápido y de mayor calidad y se usa como valor &quot; &quot; predeterminado en vcr de formato único.</td>
</tr>
<tr class="odd">
<td>velocidad de fotogramas de registros</td>
<td>Devuelve la velocidad de fotogramas, en fotogramas por segundo multiplicada por 1000, usada para la compresión.</td>
</tr>
<tr class="even">
<td>marco de <em>referencia</em></td>
<td>Devuelve el número de fotograma de la imagen de fotograma clave más cercana que precede al marco <em>especificado.</em></td>
</tr>
<tr class="odd">
<td>tamaño reservado</td>
<td>Devuelve el tamaño, en el formato de hora actual, del área de trabajo reservada. El tamaño corresponde al tiempo aproximado que se tardaría en reproducir los datos comprimidos desde un área de trabajo completa. Devuelve cero si no hay espacio en disco reservado. Esta marca devuelve el tamaño aproximado porque el espacio en disco preciso para los datos comprimidos no se puede predecir, en general, hasta después de que se hayan comprimido los datos.</td>
</tr>
<tr class="even">
<td>volumen correcto</td>
<td>Devuelve el conjunto de volúmenes para el canal de audio correcto.</td>
</tr>
<tr class="odd">
<td>samplespersec</td>
<td>Devuelve el número de muestras por segundo reproducdas o grabadas.</td>
</tr>
<tr class="even">
<td>buscar exactamente</td>
<td>Devuelve on o off , que indica si se establece &quot; o no la marca de búsqueda &quot; &quot; &quot; &quot; &quot; exacta.</td>
</tr>
<tr class="odd">
<td>Nitidez</td>
<td>Devuelve el nivel de ni sharpness actual del dispositivo.</td>
</tr>
<tr class="even">
<td>Lado</td>
<td>Devuelve 1 o 2 para indicar qué lado del vídeodisc se carga.</td>
</tr>
<tr class="odd">
<td>Esclavo</td>
<td>Devuelve &quot; el archivo , midi , none o &quot; &quot; &quot; &quot; &quot; &quot; smpte &quot; en función del tipo de conjunto de sincronización.</td>
</tr>
<tr class="even">
<td>Smpte</td>
<td>Devuelve el código de tiempo de SMPTE asociado a la posición actual del área de trabajo. Se trata de una cadena con el formato <em>dd:dd:dd:dd,</em>donde cada <em>d</em> denota un dígito de 0 a 9. Si los datos del área de trabajo no incluyen datos de código de tiempo, esta marca devuelve 00:00:00:00.</td>
</tr>
<tr class="odd">
<td>velocidad</td>
<td>Devuelve la velocidad actual del dispositivo en fotogramas por segundo (o en el mismo formato que usa el <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>comando set</strong></a> &quot; &quot; speed). El reproductor de vídeo de MCIPIONR no admite esta marca.</td>
</tr>
<tr class="even">
<td>posición inicial</td>
<td>Devuelve la posición inicial del medio.</td>
</tr>
<tr class="odd">
<td>formato de archivo still</td>
<td>Devuelve el formato de archivo actual para el <a href="capture.md"><strong>comando de</strong></a> captura.</td>
</tr>
<tr class="even">
<td>ajustar</td>
<td>Devuelve <strong>TRUE</strong> si el stretching está habilitado.</td>
</tr>
<tr class="odd">
<td>Tempo</td>
<td>Devuelve el tempo actual de una secuencia MIDI en el formato de hora actual. En el caso de los archivos con formato PPQN, el tempo está en ritmos por minuto. En el caso de los archivos con formato SMPTE, el tempo está en fotogramas por segundo.</td>
</tr>
<tr class="even">
<td>formato de hora</td>
<td>Devuelve el formato de hora actual. Para obtener más información, vea los formatos de hora en el <a href="set.md"><strong>comando set.</strong></a></td>
</tr>
<tr class="odd">
<td>modo de tiempo</td>
<td>Devuelve el modo de tiempo de posición actual. Puede detectar , &quot; código de tiempo o contador &quot; &quot; &quot; &quot; &quot; .</td>
</tr>
<tr class="even">
<td>tipo de hora</td>
<td>Devuelve el tiempo de posición actual en uso: &quot; código de tiempo o contador &quot; &quot; &quot; .</td>
</tr>
<tr class="odd">
<td>código de tiempo presente</td>
<td>Devuelve <strong>TRUE</strong> si el código de tiempo se ha registrado en la posición actual de la cinta. El código de tiempo debe avanzar desde la posición actual. Es posible que sea necesario reproducir un VCR para comprobar esta condición.</td>
</tr>
<tr class="even">
<td>registro de código de tiempo</td>
<td>Devuelve <strong>TRUE</strong> si el VCR está establecido en el código de tiempo de registro.</td>
</tr>
<tr class="odd">
<td>tipo de código de tiempo</td>
<td>Devuelve &quot; smpte, &quot; &quot; smpte drop &quot; , other o &quot; &quot; &quot; &quot; none. Tenga en cuenta que los fotogramas por segundo se pueden obtener del comando de velocidad de fotogramas de estado y la precisión del dispositivo se puede devolver mediante el comando &quot; &quot; <a href="capability.md"><strong>capability</strong></a> &quot; seek &quot; accuracy.</td>
</tr>
<tr class="even">
<td>Tinte</td>
<td>Devuelve el nivel de tono de vídeo actual.</td>
</tr>
<tr class="odd">
<td>Agudos</td>
<td>Devuelve el nivel de audio triple actual.</td>
</tr>
<tr class="even">
<td>número de afinador</td>
<td>Devuelve el número de afinador lógico actual.</td>
</tr>
<tr class="odd">
<td>Inconversos</td>
<td>Devuelve <strong>TRUE</strong> si hay datos registrados en el área de trabajo que podrían perderse como resultado de un comando close <a href="close.md"><strong>,</strong></a> <a href="load.md"><strong>load</strong></a>, <a href="record.md"><strong>record</strong></a>, <a href="reserve.md"><strong>reserve,</strong></a> <a href="cut.md"><strong>cut,</strong></a> <a href="delete.md"><strong>delete</strong></a> <a href="paste.md"><strong>o paste.</strong></a> Devuelve <strong>FALSE de lo</strong> contrario.</td>
</tr>
<tr class="even">
<td>video</td>
<td>Devuelve &quot; on o off , que refleja el estado establecido por el comando &quot; &quot; &quot; <a href="setvideo.md"><strong>setvideo.</strong></a></td>
</tr>
<tr class="odd">
<td>color de la clave de vídeo</td>
<td>Devuelve el valor del color de la clave.</td>
</tr>
<tr class="even">
<td>índice de clave de vídeo</td>
<td>Devuelve el valor del índice de clave.</td>
</tr>
<tr class="odd">
<td>monitor de vídeo</td>
<td>Devuelve &quot; la salida o uno de los tipos de entrada de origen &quot; válidos. Para más información, consulte el <a href="setvideo.md"><strong>comando setvideo</strong></a> &quot; &quot; monitor.</td>
</tr>
<tr class="even">
<td>número de monitor de vídeo</td>
<td>Devuelve el número de vídeo supervisado del tipo devuelto por el monitor de &quot; vídeo de estado &quot; . Para más información, consulte el <a href="setvideo.md">comando setvideo.</a></td>
</tr>
<tr class="odd">
<td>grabación de vídeo</td>
<td>Devuelve &quot; on o off , que refleja el estado actual establecido por &quot; &quot; &quot; <a href="setvideo.md"><strong>setvideo</strong></a> &quot; record &quot; .</td>
</tr>
<tr class="even">
<td>número de pista de la grabación de <em>vídeo</em></td>
<td>Devuelve <strong>TRUE</strong> si vcr está establecido para grabar vídeo. Si no se da ningún número de pista, se supone que el valor predeterminado es 1.</td>
</tr>
<tr class="odd">
<td>origen de vídeo</td>
<td>Devuelve el tipo de origen de vídeo. Para más información, consulte el <a href="setvideo.md"><strong>comando setvideo.</strong></a></td>
</tr>
<tr class="even">
<td>número de origen del vídeo</td>
<td>Devuelve un número correspondiente al origen de vídeo del tipo en uso. Por ejemplo, devuelve 2 si se usa la segunda entrada de origen de vídeo NTE.</td>
</tr>
<tr class="odd">
<td>secuencia de vídeo</td>
<td>Devuelve el número de secuencia de vídeo actual.</td>
</tr>
<tr class="even">
<td>volumen</td>
<td>Devuelve el volumen medio en el altavoz izquierdo y derecho. Esto devuelve un error si el dispositivo no se ha reproducido o no se ha establecido el volumen.</td>
</tr>
<tr class="odd">
<td>identificador de ventana</td>
<td>Devuelve el valor decimal ASCII para el identificador de ventana en la palabra de orden bajo del valor devuelto.</td>
</tr>
<tr class="even">
<td>ventana maximizada</td>
<td>Devuelve <strong>TRUE</strong> si la ventana está maximizada.</td>
</tr>
<tr class="odd">
<td>ventana minimizada</td>
<td>Devuelve <strong>TRUE</strong> si se minimiza la ventana.</td>
</tr>
<tr class="even">
<td>ventana visible</td>
<td>Devuelve <strong>TRUE</strong> si la ventana no está oculta.</td>
</tr>
<tr class="odd">
<td>escritura protegida</td>
<td>Devuelve <strong>TRUE</strong> si el dispositivo detecta que no puede grabar (es decir, si la protección de escritura está en). Si puede grabar, o si no puede determinar si puede grabar (sin escribir realmente), el controlador devuelve <strong>FALSE.</strong></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital y VCR, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve información en el *parámetro lpszReturnString* [**de mciSendString**](/previous-versions//dd757161(v=vs.85)). La información depende del tipo de solicitud.

## <a name="remarks"></a>Observaciones

Antes de emitir cualquier comando que use valores de posición, debe establecer el formato de hora deseado mediante el [comando set.](set.md)

## <a name="examples"></a>Ejemplos

El comando siguiente devuelve el modo actual del dispositivo "my sound".

``` syntax
status mysound mode
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

[capability](capability.md)
</dt> <dt>

[capturar](capture.md)
</dt> <dt>

[close](close.md)
</dt> <dt>

[Cortar](cut.md)
</dt> <dt>

[delete](delete.md)
</dt> <dt>

[carga](load.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[Pegar](paste.md)
</dt> <dt>

[record](record.md)
</dt> <dt>

[reserva](reserve.md)
</dt> <dt>

[guardar](save.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[setaudio](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[stop](stop.md)
</dt> <dt>

[deshacer](undo.md)
</dt> </dl>

 

