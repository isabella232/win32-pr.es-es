---
title: Estado (comando)
description: El comando de estado solicita información de estado de un dispositivo. Todos los dispositivos reconocen este comando.
ms.assetid: 39961bd7-866d-450d-9fbf-347a8f508481
keywords:
- comando de estado Windows multimedia
topic_type:
- apiref
api_name:
- status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14ab184ddaca16d0ea96b86a6b062f1e66e2eee2
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2021
ms.locfileid: "105678603"
---
# <a name="status-command"></a>Estado (comando)

> [!NOTE]
> Comunicación sin polarización: Microsoft admite un entorno diverso y de inclusión.  Dentro de este documento, hay referencias a la palabra ' Slave '. La guía de estilo de Microsoft [para Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) lo reconoce como una palabra de exclusión.  Este texto se usa tal como está actualmente el texto que se usa en los comandos. Para mantener la coherencia, este documento contiene esta palabra. Cuando se modifique esta palabra en los comandos, se corregirá este documento para que esté alineado.

El comando de estado solicita información de estado de un dispositivo. Todos los dispositivos reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

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

Marca para solicitar información de estado. En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **status** y las marcas usadas por cada tipo.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<li><em>número</em> de pista de tipo cdaudio</li>
<li>pista actual</li>
<li>length</li>
<li><em>número</em> de pista de longitud</li>
<li>medio presente</li>
<li>mode</li>
<li>número de pistas</li>
<li>position</li>
<li><em>número</em> de pista de posición</li>
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
<li>audio BitsPerSample</li>
<li>interrupciones de audio</li>
<li>audio bytespersec</li>
<li>entrada de audio</li>
<li>registro de audio</li>
<li>origen de audio</li>
<li>audio SamplesPerSec</li>
<li>secuencia de audio</li>
<li>improvisa</li>
<li>BitsPerPel</li>
<li>luminosidad</li>
<li>color</li>
<li>contraste</li>
<li>pista actual</li>
<li><em>unidad</em> de espacio en disco</li>
<li>finalización de archivos</li>
<li>formato del archivo</li>
<li>modo de archivo</li>
<li>forward</li>
<li>fotogramas omitidos</li>
<li>gamma</li>
<li>input</li>
<li>volumen izquierdo</li>
<li>length</li>
<li><em>número</em> de pista de longitud</li>
<li>medio presente</li>
<li>mode</li>
<li>monitor</li>
<li>monitor (método)</li>
<li>tasa</li>
<li>velocidad de fotogramas nominal</li>
<li>velocidad de fotogramas de registro nominal</li>
<li>número de pistas</li>
<li>output</li>
<li>identificador de paleta</li>
<li>modo de pausa</li>
<li>velocidad de reproducción</li>
<li>position</li>
<li><em>número</em> de pista de posición</li>
<li>ready</li>
<li>velocidad de fotogramas de registro</li>
<li><em>marco</em> de referencia</li>
<li>tamaño reservado</li>
<li>volumen derecho</li>
<li>Buscar exactamente</li>
<li>nitidez</li>
<li>SMPTE</li>
<li>velocidad</li>
<li>posición inicial</li>
<li>formato de archivo todavía</li>
<li>formato de hora</li>
<li>trama</li>
<li>agudos</li>
<li>no guardados</li>
<li>video</li>
<li>Índice de clave de vídeo</li>
<li>color de clave de vídeo</li>
<li>grabación de vídeo</li>
<li>origen de vídeo</li>
<li>número de origen de vídeo</li>
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
<li>medio presente</li>
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
<li>patrón de <em>número</em> de pista de longitud</li>
<li>medio presente</li>
<li>mode</li>
<li>número de pistas</li>
<li>offset</li>
<li>port</li>
<li>position</li>
<li><em>número</em> de pista de posición</li>
<li>ready</li>
<li>satélite</li>
<li>posición inicial</li>
<li>ritmo</li>
<li>formato de hora</li>
</ul></td>
</tr>
<tr class="odd">
<td>vídeos</td>
<td><ul>
<li>ensamblar registro</li>
<li>monitor de audio</li>
<li>número de monitor de audio</li>
<li>registro de audio</li>
<li><em>número</em> de pista de grabación de audio</li>
<li>origen de audio</li>
<li>número de origen de audio</li>
<li>canal</li>
<li><em>número</em> de sintonizador de canal</li>
<li>clock</li>
<li>ID. del reloj</li>
<li>counter</li>
<li>formato del contador</li>
<li>resolución de contadores</li>
<li>pista actual</li>
<li>velocidad de fotogramas</li>
<li>índice</li>
<li>índice en</li>
<li>length</li>
<li><em>número</em> de pista de longitud</li>
<li>medio presente</li>
<li>tipo de medio</li>
<li>mode</li>
<li>número de pistas de audio</li>
<li>número de pistas</li>
<li>número de pistas de vídeo</li>
<li><em>tiempo de espera</em> de pausa</li>
<li>formato de reproducción</li>
<li>position</li>
<li>posición inicial</li>
<li><em>número</em> de pista de posición</li>
<li><em>duración</em> del PostRoll</li>
<li>encendido</li>
<li><em>duración</em> del prelanzamiento</li>
<li>ready</li>
<li>formato de registro</li>
<li>velocidad</li>
<li>formato de hora</li>
<li>modo de tiempo</li>
<li>tipo de tiempo</li>
<li>código de tiempo presente</li>
<li>registro de código de tiempo</li>
<li>tipo de código de tiempo</li>
<li>número de sintonizador</li>
<li>monitor de vídeo</li>
<li>número de monitor de vídeo</li>
<li>grabación de vídeo</li>
<li><em>número</em> de pista de grabación de vídeo</li>
<li>origen de vídeo</li>
<li>número de origen de vídeo</li>
<li>protegido contra escritura</li>
</ul></td>
</tr>
<tr class="even">
<td>videodisco</td>
<td><ul>
<li>pista actual</li>
<li>tamaño del disco</li>
<li>forward</li>
<li>length</li>
<li><em>número</em> de pista de longitud</li>
<li>medio presente</li>
<li>tipo de medio</li>
<li>mode</li>
<li>número de pistas</li>
<li>position</li>
<li><em>número</em> de pista de posición</li>
<li>ready</li>
<li>margen</li>
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
<li><em>número</em> de pista de longitud</li>
<li>Nivel</li>
<li>medio presente</li>
<li>mode</li>
<li>número de pistas</li>
<li>output</li>
<li>position</li>
<li><em>número</em> de pista de posición</li>
<li>ready</li>
<li>samplespersec</li>
<li>posición inicial</li>
<li>formato de hora</li>
</ul></td>
</tr>
</tbody>
</table>



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszRequest** y su significado.



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
<td>alineación</td>
<td>Devuelve la alineación del bloque de datos, en bytes.</td>
</tr>
<tr class="even">
<td>ensamblar registro</td>
<td>Devuelve <strong>true</strong> si el dispositivo está configurado para la grabación en modo de ensamblaje.</td>
</tr>
<tr class="odd">
<td>audio</td>
<td>Devuelve &quot; on &quot; u &quot; OFF según &quot; el comando <a href="setaudio.md">SetAudio</a> &quot; on &quot; u OFF más reciente &quot; &quot; . Devuelve &quot; on &quot; si uno o ambos altavoces están habilitados y &quot; desactivado en &quot; caso contrario.</td>
</tr>
<tr class="even">
<td>alineación de audio</td>
<td>Devuelve la alineación de los bloques de datos en relación con el inicio de los datos de audio de onda de entrada.</td>
</tr>
<tr class="odd">
<td>audio BitsPerSample</td>
<td>Devuelve el número de bits por muestra que el dispositivo usa para la grabación. Esta marca solo se aplica a los dispositivos que admiten el &quot; &quot; algoritmo PCM.</td>
</tr>
<tr class="even">
<td>interrupciones de audio</td>
<td>Devuelve el número de veces que se ha interrumpido la parte de audio de la última secuencia de AVI. El sistema cuenta una interrupción de audio cada vez que intenta escribir datos de audio en el controlador de dispositivo y detecta que el controlador ya ha reproducido todos los datos disponibles. Esta marca solo se reconoce en el controlador de vídeo digital MCIAVI. Está pensada solo para la evaluación del rendimiento. el valor devuelto es difícil de interpretar.</td>
</tr>
<tr class="odd">
<td>audio bytespersec</td>
<td>Devuelve el número medio de bytes por segundo que se usan para la grabación.</td>
</tr>
<tr class="even">
<td>entrada de audio</td>
<td>Devuelve el nivel de audio instantáneo aproximado de la señal de audio de entrada analógica. Un valor mayor que 1000 implica una distorsión de recorte. Algunos dispositivos pueden devolver este valor solo al grabar audio. El valor no tiene asociado ningún comando <a href="set.md">set</a> o <a href="setaudio.md">SetAudio</a> .</td>
</tr>
<tr class="odd">
<td>monitor de audio</td>
<td>Devuelve &quot; &quot; la salida o uno de los tipos válidos de entrada de origen. Para obtener más información, consulte el comando monitor de <strong>SetAudio</strong> &quot; &quot; .</td>
</tr>
<tr class="even">
<td>número de monitor de audio</td>
<td>Devuelve el número de vídeo supervisado del tipo especificado por el monitor de audio de <strong>Estado</strong> &quot; &quot; . Para obtener más información, consulte el comando <a href="setaudio.md">SetAudio</a> .</td>
</tr>
<tr class="odd">
<td>registro de audio</td>
<td>Devuelve &quot; on &quot; u &quot; OFF &quot; , que refleja el estado establecido por el registro <strong>SetAudio</strong> &quot; &quot; .</td>
</tr>
<tr class="even">
<td><em>número</em> de pista de grabación de audio</td>
<td>Devuelve <strong>true</strong> si el VCR está establecido para grabar audio. Si no se proporciona ningún número de pista, se asume el valor predeterminado de 1.</td>
</tr>
<tr class="odd">
<td>audio SamplesPerSec</td>
<td>Devuelve el número de muestras por segundo grabadas.</td>
</tr>
<tr class="even">
<td>origen de audio</td>
<td>Devuelve el origen del digitalizador de audio actual: &quot; izquierda &quot; , &quot; derecha &quot; , &quot; promedio &quot; o &quot; estéreo &quot; .</td>
</tr>
<tr class="odd">
<td>número de origen de audio</td>
<td>Devuelve el número de origen de audio del tipo devuelto por el <strong>Estado</strong> de &quot; origen de audio &quot; . Para obtener más información, consulte el comando <a href="setaudio.md">SetAudio</a> .</td>
</tr>
<tr class="even">
<td>secuencia de audio</td>
<td>Devuelve el número de secuencia de audio actual.</td>
</tr>
<tr class="odd">
<td>improvisa</td>
<td>Devuelve el nivel de audio-graves actual.</td>
</tr>
<tr class="even">
<td>BitsPerPel</td>
<td>Devuelve el número de bits por píxel para guardar los datos capturados o grabados.</td>
</tr>
<tr class="odd">
<td>bitspersample</td>
<td>Devuelve los bits por muestra.</td>
</tr>
<tr class="even">
<td>luminosidad</td>
<td>Devuelve el nivel de brillo de vídeo actual.</td>
</tr>
<tr class="odd">
<td>bytespersec</td>
<td>Devuelve el número medio de bytes por segundo que se reproducen o registran.</td>
</tr>
<tr class="even">
<td><em>número</em> de pista de tipo cdaudio</td>
<td>Devuelve el tipo del número de seguimiento especificado. Puede ser &quot; audio &quot; u &quot; otro.&quot;</td>
</tr>
<tr class="odd">
<td>canal</td>
<td>Devuelve el valor entero del conjunto de canales en el sintonizador.</td>
</tr>
<tr class="even">
<td><em>número</em> de sintonizador de canal</td>
<td>Si &quot; &quot; se proporciona el <em>número</em> de sintonizador, se devolverá el canal seleccionado actualmente en el <em>número</em> de sintonizador lógico. Tenga en cuenta que puede haber varios sintonizadores lógicos.</td>
</tr>
<tr class="odd">
<td>canales nueva</td>
<td>Devuelve el número de canales establecido (1 para mono, 2 para estéreo).</td>
</tr>
<tr class="even">
<td>clock</td>
<td>Devuelve la hora externa. El tiempo debe ser un entero largo sin signo que exprese los incrementos totales. Para obtener más información, consulte el comando tasa de incremento del reloj de la <a href="capability.md">capacidad</a> &quot; &quot; .</td>
</tr>
<tr class="odd">
<td>ID. del reloj</td>
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
<td>Devuelve la posición del contador, en el formato del contador actual.</td>
</tr>
<tr class="odd">
<td>formato del contador</td>
<td>Devuelve el formato del contador actual. Para obtener más información, consulte el comando <a href="set.md">set</a> &quot; Counter format &quot; .</td>
</tr>
<tr class="even">
<td>resolución de contadores</td>
<td>Devuelve &quot; Marcos &quot; o &quot; segundos &quot; , que indican la resolución del contador. Esto no es lo mismo que la precisión.</td>
</tr>
<tr class="odd">
<td>pista actual</td>
<td>Devuelve la pista actual. El secuenciador MCISEQ devuelve 1.</td>
</tr>
<tr class="even">
<td>tamaño del disco</td>
<td>Devuelve 8 o 12, que indica el tamaño del disco cargado en pulgadas.</td>
</tr>
<tr class="odd">
<td><em>unidad</em> de espacio en disco</td>
<td>Devuelve el espacio en disco aproximado, en el formato de hora actual, que se puede obtener mediante un comando de <a href="reserve.md">reserva</a> para la unidad de disco especificada <em>.</em> Normalmente, la <em>unidad</em> se especifica como una sola letra o una sola letra seguida de dos puntos (:). Sin embargo, algunos dispositivos pueden usar una ruta de acceso.</td>
</tr>
<tr class="even">
<td>tipo de división</td>
<td>Devuelve uno de los siguientes tipos de división de archivos:
<ul>
<li>PPQN</li>
<li>Fotograma SMPTE 24</li>
<li>Fotograma SMPTE 25</li>
<li>Fotograma eliminado SMPTE 30</li>
<li>Fotograma SMPTE 30</li>
</ul>
<br/> Utilice esta información para determinar el formato del archivo MIDI y el significado de la información sobre el tempo y la posición.<br/></td>
</tr>
<tr class="odd">
<td>finalización de archivos</td>
<td>Devuelve el porcentaje estimado de progreso de una operación de <a href="load.md">carga</a>, <a href="save.md">guardado</a>, <a href="capture.md">captura</a>, <a href="cut.md">cortar</a>, <a href="copy.md">copiar</a>, <a href="delete.md">eliminar</a>, <a href="paste.md">pegar</a>o <a href="undo.md">Deshacer</a> . (Las aplicaciones pueden utilizar esto para proporcionar un indicador visual de progreso).</td>
</tr>
<tr class="even">
<td>formato del archivo</td>
<td>Devuelve el formato de archivo actual para los comandos de <a href="record.md">registro</a> o <strong>Guardar</strong> .</td>
</tr>
<tr class="odd">
<td>modo de archivo</td>
<td>Devuelve la &quot; carga &quot; , el &quot; guardado, la &quot; &quot; edición o la &quot; &quot; inactividad &quot; . Durante una operación de <a href="load.md"><strong>carga</strong></a> , devuelve la &quot; carga &quot; . Durante las operaciones de <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>guardado</strong></a> y <a href="capture.md"><strong>captura</strong></a> , devuelve el &quot; guardado &quot; . Durante las operaciones de <a href="cut.md"><strong>cortar</strong></a>, <a href="copy.md"><strong>copiar</strong></a>, <a href="delete.md"><strong>eliminar</strong></a>, <a href="paste.md"><strong>pegar</strong></a>o <a href="undo.md"><strong>Deshacer</strong></a> , devuelve la &quot; Edición &quot; .</td>
</tr>
<tr class="even">
<td>etiqueta de formato</td>
<td>Devuelve la etiqueta de formato.</td>
</tr>
<tr class="odd">
<td>forward</td>
<td>Devuelve <strong>true</strong> si la dirección de reproducción es hacia delante o si el dispositivo no se está reproduciendo.</td>
</tr>
<tr class="even">
<td>velocidad de fotogramas</td>
<td>Devuelve el número de fotogramas por segundo que el dispositivo usará de forma predeterminada. Los dispositivos NTSC devuelven 30, PAL 25, etc.</td>
</tr>
<tr class="odd">
<td>fotogramas omitidos</td>
<td>Devuelve el número de fotogramas que no se dibujaron cuando se reprodujo la última secuencia AVI. Esta marca solo se reconoce en el controlador de vídeo digital MCIAVI. Está pensada solo para la evaluación del rendimiento. el valor devuelto es difícil de interpretar.</td>
</tr>
<tr class="even">
<td>gamma</td>
<td>Devuelve el valor establecido con <a href="setvideo.md"><strong></strong></a> el &quot; valor gamma de setvideo &quot; <em></em>.</td>
</tr>
<tr class="odd">
<td>índice</td>
<td>Devuelve la presentación del índice actual. Para obtener más información, consulte el comando <a href="set.md"><strong>set</strong></a> &quot; index &quot; .</td>
</tr>
<tr class="even">
<td>índice en</td>
<td>Devuelve <strong>true</strong> si el índice está activado.</td>
</tr>
<tr class="odd">
<td>input</td>
<td>Devuelve el conjunto de entrada. Si no se establece uno, el error devuelto indica que se puede usar cualquier dispositivo. En el caso de los dispositivos de vídeo digital, modifica la &quot; marca de graves &quot; , &quot; agudos &quot; , &quot; volumen &quot; , &quot; brillo &quot; , &quot; color &quot; , &quot; contraste &quot; , &quot; gamma &quot; , &quot; nitidez &quot; o &quot; matiz &quot; para que se aplique solo a la entrada. Este es el valor predeterminado al supervisar la entrada.</td>
</tr>
<tr class="even">
<td>volumen izquierdo</td>
<td>Devuelve el conjunto de volúmenes para el canal de audio izquierdo.</td>
</tr>
<tr class="odd">
<td>length</td>
<td>Devuelve la longitud total del medio, en el formato de hora actual. En el caso de los archivos PPQN, la longitud se devuelve en unidades de puntero de la canción. En el caso de los archivos SMPTE, se devuelve como <em>HH: mm: SS: FF</em>, donde <em>HH</em> es hours, <em>mm</em> es minutes, <em>SS</em> is seconds y <em>FF</em> es frames. En el caso de los dispositivos VCR, la longitud es de 2 horas (a menos que la longitud se haya cambiado explícitamente mediante el comando <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> ).</td>
</tr>
<tr class="even">
<td><em>número</em> de pista de longitud</td>
<td>Devuelve la longitud de la pista, en horas o fotogramas, especificada por <em>número</em>. En el caso de los archivos PPQN, la longitud se devuelve en unidades de puntero de la canción. En el caso de los archivos SMPTE, se devuelve como <em>HH: mm: SS: FF</em>, donde <em>HH</em> es hours, <em>mm</em> es minutes, <em>SS</em> is seconds y <em>FF</em> es frames.<br/></td>
</tr>
<tr class="odd">
<td>Nivel</td>
<td>Devuelve el valor del ejemplo de audio PCM actual.</td>
</tr>
<tr class="even">
<td>maestro</td>
<td>Devuelve &quot; MIDI &quot; , &quot; ninguno &quot; o &quot; SMPTE &quot; según el tipo de conjunto de sincronización.</td>
</tr>
<tr class="odd">
<td>medio presente</td>
<td>Devuelve <strong>true</strong> si el elemento multimedia se inserta en el dispositivo o <strong>false</strong> en caso contrario. Los dispositivos Sequencer, vídeo superpuesto, vídeo digital y de audio de onda devuelven <strong>true</strong>.</td>
</tr>
<tr class="even">
<td>tipo de medio</td>
<td>Devuelve el tipo de los elementos multimedia. En el caso de los VCR, es &quot; 8mm &quot; , &quot; VHS &quot; , &quot; SVHS &quot; , &quot; beta &quot; , &quot; Hi8 &quot; , &quot; edbeta &quot; u &quot; otros &quot; . En el caso de los videodiscos, es &quot; CAV &quot; , &quot; CLV &quot; u &quot; otro &quot; , en función del tipo de VideoDisc.</td>
</tr>
<tr class="odd">
<td>mode</td>
<td>Devuelve el modo actual del dispositivo. Todos los dispositivos pueden devolver los &quot; valores no Ready &quot; , &quot; pausado &quot; , &quot; Playing &quot; y &quot; Stopped &quot; . Algunos dispositivos pueden devolver los &quot; valores de apertura, de estacionamiento, de &quot; &quot; &quot; &quot; grabación y de búsqueda adicionales &quot; &quot; &quot; .</td>
</tr>
<tr class="even">
<td>monitor</td>
<td>Devuelve el &quot; archivo &quot; o la &quot; entrada &quot; . El valor devuelto indica el origen de presentación actual.</td>
</tr>
<tr class="odd">
<td>monitor (método)</td>
<td>Devuelve &quot; pre &quot; , &quot; post &quot; o &quot; Direct &quot; . El valor devuelto indica el método utilizado para la supervisión de entrada.</td>
</tr>
<tr class="even">
<td>tasa</td>
<td>El elemento modifica las &quot; marcas de graves &quot; , &quot; brillo &quot; , &quot; color &quot; , &quot; contraste &quot; , &quot; gamma &quot; , &quot; nitidez &quot; , &quot; matiz &quot; , &quot; agudos &quot; y &quot; volumen &quot; para devolver el valor nominal en lugar de la configuración actual.</td>
</tr>
<tr class="odd">
<td>velocidad de fotogramas nominal</td>
<td>Devuelve la velocidad de fotogramas nominal asociada al archivo. Las unidades están en fotogramas por segundo multiplicado por 1000.</td>
</tr>
<tr class="even">
<td>velocidad de fotogramas de registro nominal</td>
<td>Devuelve la velocidad de fotogramas nominal asociada a la señal de vídeo de entrada. Las unidades están en fotogramas por segundo multiplicado por 1000.</td>
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
<td>Devuelve el desplazamiento de un archivo basado en SMPTE. El desplazamiento es la hora de inicio de una secuencia basada en SMPTE. La hora se devuelve como <em>HH: mm: SS: FF</em>, donde <em>HH</em> es hours, <em>mm</em> is minutes, <em>SS</em> is seconds y <em>FF</em> is frames.</td>
</tr>
<tr class="odd">
<td>output</td>
<td>Devuelve la salida establecida actualmente. Si no se establece ningún resultado, el error devuelto indica que se puede usar cualquier dispositivo. En el caso de los dispositivos de vídeo digital, modifica la &quot; marca de graves &quot; , &quot; agudos &quot; , &quot; volumen &quot; , &quot; brillo &quot; , &quot; color &quot; , &quot; contraste &quot; , &quot; gamma &quot; , &quot; nitidez &quot; o &quot; matiz &quot; para que se aplique solo a la salida. Este es el valor predeterminado al supervisar un archivo.</td>
</tr>
<tr class="even">
<td>modo de pausa</td>
<td>Devuelve &quot; &quot; la grabación si el dispositivo está en pausa mientras se graba. Devuelve &quot; la reproducción &quot; si el dispositivo está en pausa mientras se reproduce. Devuelve la &quot; acción de error no aplicable en el modo actual &quot; si el dispositivo no está en pausa.</td>
</tr>
<tr class="odd">
<td>tiempo de espera de pausa</td>
<td>Devuelve la duración máxima, en milisegundos, de un comando <a href="pause.md"><strong>PAUSE</strong></a> .</td>
</tr>
<tr class="even">
<td>formato de reproducción</td>
<td>Devuelve un código que indica el formato en el que se reproducirá la cinta de vídeo, si se detecta: &quot; LP &quot; , &quot; EP &quot; , &quot; Sp &quot; u &quot; otros &quot; . Para obtener más información, vea la &quot; marca de formato de registro &quot; .</td>
</tr>
<tr class="odd">
<td>velocidad de reproducción</td>
<td>Devuelve un valor que representa la proximidad del tiempo de reproducción real de la última secuencia de AVI con el tiempo de reproducción del destino. El valor 1000 indica que la hora de destino y la hora real eran iguales. Un valor de 2000, por ejemplo, indicaría que la secuencia AVI tardó dos veces más en ejecutarse que debiera. Esta marca solo se reconoce en el controlador de vídeo digital MCIAVI. Está pensada solo para la evaluación del rendimiento. el valor devuelto es difícil de interpretar.</td>
</tr>
<tr class="even">
<td>port</td>
<td>Devuelve el número de puerto MIDI asignado a la secuencia.</td>
</tr>
<tr class="odd">
<td>position</td>
<td>Devuelve la posición actual. En el caso de los archivos PPQN, la posición se devuelve en unidades del puntero de la canción. En el caso de los archivos SMPTE, se devuelve como <em>HH: mm: SS: FF</em>, donde <em>HH</em> es hours, <em>mm</em> es minutes, SS is seconds y <em>FF</em> es frames.<br/></td>
</tr>
<tr class="even">
<td>posición inicial</td>
<td>Devuelve la posición del inicio del medio utilizable.</td>
</tr>
<tr class="odd">
<td><em>número</em> de pista de posición</td>
<td>Devuelve la posición del inicio de la pista especificada por el <em>número</em>. En el caso de los archivos PPQN, el formato de hora se devuelve en unidades de puntero de la canción. En el caso de los archivos SMPTE, se devuelve como <em>HH: mm: SS: FF</em>, donde <em>HH</em> es hours, <em>mm</em> es minutes, <em>SS</em> is seconds y <em>FF</em> es frames. El secuenciador MCISEQ devuelve cero. El dispositivo MCIPIONR no admite esta marca. El dispositivo MCIWAVE devuelve cero.</td>
</tr>
<tr class="even">
<td>duración del PostRoll</td>
<td>Devuelve la longitud de la cinta de vídeo, en el formato de hora actual, necesaria para frenar el transporte de VCR cuando se emite un comando de <a href="stop.md"><strong>detención</strong></a> o <a href="pause.md"><strong>pausa</strong></a> .</td>
</tr>
<tr class="odd">
<td>encendido</td>
<td>Devuelve <strong>true</strong> si la alimentación del VCR está activada.</td>
</tr>
<tr class="even">
<td>duración del prelanzamiento</td>
<td>Devuelve la longitud de la cinta de vídeo, en el formato de hora actual, necesaria para estabilizar la salida del VCR.</td>
</tr>
<tr class="odd">
<td>ready</td>
<td>Devuelve <strong>true</strong> si el dispositivo está listo para aceptar otro comando.</td>
</tr>
<tr class="even">
<td>formato de registro</td>
<td>Devuelve un código que indica el formato en el que se grabará la cinta de vídeo. Los tipos de valor devueltos actuales son &quot; LP &quot; , &quot; EP &quot; , &quot; Sp &quot; u &quot; otros &quot; . Estos formatos no son específicos de VHS y se pueden aplicar a cualquier VCR que tenga varios formatos de grabación seleccionables. El &quot; &quot; tipo SP es el formato de grabación más rápido y de mayor calidad, y se usa como valor predeterminado en VCR de formato único.</td>
</tr>
<tr class="odd">
<td>velocidad de fotogramas de registro</td>
<td>Devuelve la velocidad de fotogramas, en fotogramas por segundo multiplicada por 1000, que se usa para la compresión.</td>
</tr>
<tr class="even">
<td><em>marco</em> de referencia</td>
<td>Devuelve el número de marco de la imagen de fotograma clave más cercana que precede al <em>marco</em>especificado.</td>
</tr>
<tr class="odd">
<td>tamaño reservado</td>
<td>Devuelve el tamaño, en el formato de hora actual, del área de trabajo reservada. El tamaño corresponde al tiempo aproximado que se tardaría en reproducir los datos comprimidos desde un área de trabajo completa. Devuelve cero si no hay espacio en disco reservado. Esta marca devuelve el tamaño aproximado porque el espacio en disco preciso para los datos comprimidos no se puede predecir en general hasta que se hayan comprimido los datos.</td>
</tr>
<tr class="even">
<td>volumen derecho</td>
<td>Devuelve el conjunto de volúmenes para el canal de audio derecho.</td>
</tr>
<tr class="odd">
<td>samplespersec</td>
<td>Devuelve el número de muestras por segundo reproducidas o grabadas.</td>
</tr>
<tr class="even">
<td>Buscar exactamente</td>
<td>Devuelve &quot; on &quot; u &quot; OFF &quot; , que indica si &quot; se establece la marca Seek Exactly &quot; .</td>
</tr>
<tr class="odd">
<td>nitidez</td>
<td>Devuelve el nivel de nitidez actual del dispositivo.</td>
</tr>
<tr class="even">
<td>margen</td>
<td>Devuelve 1 o 2 para indicar el lado del CD que se ha cargado.</td>
</tr>
<tr class="odd">
<td>satélite</td>
<td>Devuelve &quot; file &quot; , &quot; MIDI &quot; , &quot; None &quot; o &quot; SMPTE &quot; según el tipo de conjunto de sincronización.</td>
</tr>
<tr class="even">
<td>SMPTE</td>
<td>Devuelve el código de tiempo de SMPTE asociado a la posición actual en el área de trabajo. Se trata de una cadena con el formato <em>DD: DD</em>: DD: DD, donde cada <em>d</em> denota un dígito de 0 a 9. Si los datos del área de trabajo no incluyen datos de código de tiempo, esta marca devuelve 00:00:00:00.</td>
</tr>
<tr class="odd">
<td>velocidad</td>
<td>Devuelve la velocidad actual del dispositivo en fotogramas por segundo (o en el mismo formato que usa el comando <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> &quot; Speed &quot; ). El reproductor de videodisco de MCIPIONR no admite esta marca.</td>
</tr>
<tr class="even">
<td>posición inicial</td>
<td>Devuelve la posición inicial del elemento multimedia.</td>
</tr>
<tr class="odd">
<td>formato de archivo todavía</td>
<td>Devuelve el formato de archivo actual para el comando de <a href="capture.md"><strong>captura</strong></a> .</td>
</tr>
<tr class="even">
<td>ajustar</td>
<td>Devuelve <strong>true</strong> si está habilitada la expansión.</td>
</tr>
<tr class="odd">
<td>ritmo</td>
<td>Devuelve el tempo actual de una secuencia MIDI en el formato de hora actual. En el caso de los archivos con el formato PPQN, el tempo está en pulsaciones por minuto. En el caso de los archivos con el formato SMPTE, el tempo está en fotogramas por segundo.</td>
</tr>
<tr class="even">
<td>formato de hora</td>
<td>Devuelve el formato de hora actual. Para obtener más información, consulte los formatos de hora del comando <a href="set.md"><strong>set</strong></a> .</td>
</tr>
<tr class="odd">
<td>modo de tiempo</td>
<td>Devuelve el modo de tiempo de la posición actual. Puede ser &quot; detectada &quot; , &quot; código de tiempo &quot; o &quot; contador &quot; .</td>
</tr>
<tr class="even">
<td>tipo de tiempo</td>
<td>Devuelve el tiempo de la posición actual en uso: &quot; código de tiempo &quot; o &quot; contador &quot; .</td>
</tr>
<tr class="odd">
<td>código de tiempo presente</td>
<td>Devuelve <strong>true</strong> si el código de tiempo se ha grabado en la posición actual de la cinta. El código de tiempo debe avanzar desde la posición actual. Es posible que sea necesario reproducir un VCR para comprobar esta condición.</td>
</tr>
<tr class="even">
<td>registro de código de tiempo</td>
<td>Devuelve <strong>true</strong> si el VCR está establecido para grabar código de tiempo.</td>
</tr>
<tr class="odd">
<td>tipo de código de tiempo</td>
<td>Devuelve &quot; SMPTE &quot; , &quot; eliminación SMPTE &quot; , &quot; otro &quot; o &quot; ninguno &quot; . Tenga en cuenta que los fotogramas por segundo se pueden obtener del &quot; comando tasa de fotogramas de estado &quot; y la precisión del dispositivo puede ser devuelta por el comando precisión de búsqueda de <a href="capability.md"><strong>capacidad</strong></a> &quot; &quot; .</td>
</tr>
<tr class="even">
<td>trama</td>
<td>Devuelve el nivel de matiz de vídeo actual.</td>
</tr>
<tr class="odd">
<td>agudos</td>
<td>Devuelve el nivel de audio-agudos actual.</td>
</tr>
<tr class="even">
<td>número de sintonizador</td>
<td>Devuelve el número de sintonizador lógico actual.</td>
</tr>
<tr class="odd">
<td>no guardados</td>
<td>Devuelve <strong>true</strong> si hay datos registrados en el área de trabajo que podrían perderse como resultado de un <a href="close.md"><strong>comando cerrar</strong></a>, <a href="load.md"><strong>cargar</strong></a>, <a href="record.md"><strong>grabar</strong></a>, <a href="reserve.md"><strong>reservar</strong></a>, <a href="cut.md"><strong>cortar</strong></a>, <a href="delete.md"><strong>eliminar</strong></a>o <a href="paste.md"><strong>pegar</strong></a> . Devuelve <strong>false</strong> en caso contrario.</td>
</tr>
<tr class="even">
<td>video</td>
<td>Devuelve &quot; on &quot; u &quot; OFF &quot; , que refleja el estado establecido por el comando <a href="setvideo.md"><strong>setvideo</strong></a> .</td>
</tr>
<tr class="odd">
<td>color de clave de vídeo</td>
<td>Devuelve el valor del color de la clave.</td>
</tr>
<tr class="even">
<td>Índice de clave de vídeo</td>
<td>Devuelve el valor del índice de clave.</td>
</tr>
<tr class="odd">
<td>monitor de vídeo</td>
<td>Devuelve &quot; &quot; la salida o uno de los tipos válidos de entrada de origen. Para obtener más información, consulte el comando monitor de <a href="setvideo.md"><strong>setvideo</strong></a> &quot; &quot; .</td>
</tr>
<tr class="even">
<td>número de monitor de vídeo</td>
<td>Devuelve el número de vídeo supervisado del tipo devuelto por el monitor de vídeo de estado &quot; &quot; . Para obtener más información, consulte el comando <a href="setvideo.md">setvideo</a> .</td>
</tr>
<tr class="odd">
<td>grabación de vídeo</td>
<td>Devuelve &quot; on &quot; u &quot; OFF &quot; , que refleja el estado actual establecido por el registro <a href="setvideo.md"><strong>setvideo</strong></a> &quot; &quot; .</td>
</tr>
<tr class="even">
<td><em>número</em> de pista de grabación de vídeo</td>
<td>Devuelve <strong>true</strong> si el VCR está configurado para grabar vídeo. Si no se proporciona ningún número de pista, se asume el valor predeterminado de 1.</td>
</tr>
<tr class="odd">
<td>origen de vídeo</td>
<td>Devuelve el tipo de origen de vídeo. Para obtener más información, consulte el comando <a href="setvideo.md"><strong>setvideo</strong></a> .</td>
</tr>
<tr class="even">
<td>número de origen de vídeo</td>
<td>Devuelve un número que corresponde al origen de vídeo del tipo en uso. Por ejemplo, devuelve 2 si se usa la segunda entrada de origen de vídeo NTSC.</td>
</tr>
<tr class="odd">
<td>secuencia de vídeo</td>
<td>Devuelve el número de secuencia de vídeo actual.</td>
</tr>
<tr class="even">
<td>volumen</td>
<td>Devuelve el volumen medio a los altavoces izquierdo y derecho. Esto devuelve un error si el dispositivo no se ha reproducido o no se ha establecido el volumen.</td>
</tr>
<tr class="odd">
<td>identificador de ventana</td>
<td>Devuelve el valor decimal ASCII para el identificador de ventana en la palabra de orden inferior del valor devuelto.</td>
</tr>
<tr class="even">
<td>ventana maximizada</td>
<td>Devuelve <strong>true</strong> si la ventana está maximizada.</td>
</tr>
<tr class="odd">
<td>ventana minimizada</td>
<td>Devuelve <strong>true</strong> si la ventana está minimizada.</td>
</tr>
<tr class="even">
<td>ventana visible</td>
<td>Devuelve <strong>true</strong> si la ventana no está oculta.</td>
</tr>
<tr class="odd">
<td>protegido contra escritura</td>
<td>Devuelve <strong>true</strong> si el dispositivo detecta que no puede grabar (es decir, si la protección contra escritura está activada). Si puede grabar, o si no puede determinar si puede grabar (sin escribir realmente), el controlador devuelve <strong>false</strong>.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve información en el parámetro *lpszReturnString* de [**mciSendString**](/previous-versions//dd757161(v=vs.85)). La información depende del tipo de solicitud.

## <a name="remarks"></a>Observaciones

Antes de emitir cualquier comando que use valores de posición, debe establecer el formato de hora deseado mediante el comando [set](set.md) .

## <a name="examples"></a>Ejemplos

El siguiente comando devuelve el modo actual del dispositivo "de".

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

[Cadenas de comandos MCI](mci-command-strings.md)
</dt> <dt>

[capability](capability.md)
</dt> <dt>

[grabar](capture.md)
</dt> <dt>

[close](close.md)
</dt> <dt>

[límite](cut.md)
</dt> <dt>

[delete](delete.md)
</dt> <dt>

[carga](load.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[copiar](paste.md)
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

 

