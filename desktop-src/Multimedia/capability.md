---
title: funcionalidad (comando)
description: El comando Capability solicita información acerca de una funcionalidad determinada de un dispositivo. Todos los dispositivos MCI reconocen este comando.
ms.assetid: 1b470473-0de6-41ba-9f6e-41f0b13ceaeb
keywords:
- comando de funcionalidad multimedia de Windows
topic_type:
- apiref
api_name:
- capability
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a6ac87b98fb8d748a5baf2665cc5a63230b6a98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489599"
---
# <a name="capability-command"></a>funcionalidad (comando)

El comando Capability solicita información acerca de una funcionalidad determinada de un dispositivo. Todos los dispositivos MCI reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capability %s %s %s"), 
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

Marca que identifica una funcionalidad del dispositivo. En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando de **funcionalidad** y las marcas usadas por cada tipo:



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Tipo</th>
<th>Tipo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>cdaudio</td>
<td><ul>
<li>puede expulsar</li>
<li>puede jugar</li>
<li>puede grabar</li>
<li>puede guardar</li>
<li>dispositivo compuesto</li>
</ul></td>
<td><ul>
<li>tipo de dispositivo</li>
<li>tiene audio</li>
<li>tiene vídeo</li>
<li>utiliza archivos</li>
</ul></td>
</tr>
<tr class="even">
<td>digitalvideo</td>
<td><ul>
<li>puede expulsar</li>
<li>puede inmovilizar</li>
<li>puede bloquear</li>
<li>puede jugar</li>
<li>puede grabar</li>
<li>puede invertir</li>
<li>puede guardar</li>
<li>se puede extender</li>
<li>puede extender la entrada</li>
<li>puede probar</li>
</ul></td>
<td><ul>
<li>dispositivo compuesto</li>
<li>tipo de dispositivo</li>
<li>tiene audio</li>
<li>todavía</li>
<li>tiene vídeo</li>
<li>velocidad máxima de reproducción</li>
<li>velocidad de reproducción mínima</li>
<li>utiliza archivos</li>
<li>usar paletas</li>
<li>Windows</li>
</ul></td>
</tr>
<tr class="odd">
<td>overlay</td>
<td><ul>
<li>puede expulsar</li>
<li>puede inmovilizar</li>
<li>puede jugar</li>
<li>puede grabar</li>
<li>puede guardar</li>
<li>se puede extender</li>
</ul></td>
<td><ul>
<li>dispositivo compuesto</li>
<li>tipo de dispositivo</li>
<li>tiene audio</li>
<li>tiene vídeo</li>
<li>utiliza archivos</li>
<li>Windows</li>
</ul></td>
</tr>
<tr class="even">
<td>sequencer</td>
<td><ul>
<li>puede expulsar</li>
<li>puede jugar</li>
<li>puede grabar</li>
<li>puede guardar</li>
<li>dispositivo compuesto</li>
</ul></td>
<td><ul>
<li>tipo de dispositivo</li>
<li>tiene audio</li>
<li>tiene vídeo</li>
<li>utiliza archivos</li>
</ul></td>
</tr>
<tr class="odd">
<td>vídeos</td>
<td><ul>
<li>puede detectar la longitud</li>
<li>puede expulsar</li>
<li>puede inmovilizar</li>
<li>puede supervisar orígenes</li>
<li>puede jugar</li>
<li>puede prevertir</li>
<li>puede obtener una vista previa</li>
<li>puede grabar</li>
<li>puede invertir</li>
<li>puede guardar</li>
<li>puede probar</li>
</ul></td>
<td><ul>
<li>tasa de incremento de reloj</li>
<li>dispositivo compuesto</li>
<li>tipo de dispositivo</li>
<li>tiene audio</li>
<li>tiene reloj</li>
<li>tiene código de tiempo</li>
<li>tiene vídeo</li>
<li>número de marcas</li>
<li>precisión de búsqueda</li>
<li>utiliza archivos</li>
</ul></td>
</tr>
<tr class="even">
<td>videodisco</td>
<td><ul>
<li>puede expulsar</li>
<li>puede jugar</li>
<li>puede grabar</li>
<li>puede invertir</li>
<li>puede guardar</li>
<li>CAV</li>
<li>CLV</li>
<li>dispositivo compuesto</li>
</ul></td>
<td><ul>
<li>tipo de dispositivo</li>
<li>velocidad de reproducción rápida</li>
<li>tiene audio</li>
<li>tiene vídeo</li>
<li>velocidad de reproducción normal</li>
<li>velocidad de reproducción lenta</li>
<li>utiliza archivos</li>
</ul></td>
</tr>
<tr class="odd">
<td>waveaudio</td>
<td><ul>
<li>puede expulsar</li>
<li>puede jugar</li>
<li>puede grabar</li>
<li>puede guardar</li>
<li>dispositivo compuesto</li>
<li>tipo de dispositivo</li>
</ul></td>
<td><ul>
<li>tiene audio</li>
<li>tiene vídeo</li>
<li>inputs</li>
<li>outputs</li>
<li>utiliza archivos</li>
</ul></td>
</tr>
</tbody>
</table>



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro *lpszRequest* y su significado:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Marcas</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>puede detectar la longitud</td>
<td>Devuelve <strong>true</strong> si el dispositivo puede detectar la longitud del medio.</td>
</tr>
<tr class="even">
<td>puede expulsar</td>
<td>Devuelve <strong>true</strong> si el dispositivo puede expulsar los medios.</td>
</tr>
<tr class="odd">
<td>puede inmovilizar</td>
<td>Devuelve <strong>true</strong> si el dispositivo puede inmovilizar los datos en el búfer de fotogramas.</td>
</tr>
<tr class="even">
<td>puede bloquear</td>
<td>Devuelve <strong>true</strong> si el dispositivo puede bloquear los datos.</td>
</tr>
<tr class="odd">
<td>puede supervisar orígenes</td>
<td>Devuelve <strong>true</strong> si el dispositivo puede pasar una entrada (origen) a la salida supervisada, independientemente de la selección de entrada actual.</td>
</tr>
<tr class="even">
<td>puede jugar</td>
<td>Devuelve <strong>true</strong> si el dispositivo puede reproducirse.</td>
</tr>
<tr class="odd">
<td>puede prevertir</td>
<td>Devuelve <strong>true</strong> si el dispositivo admite la &quot; marca de preroll &quot; con el comando <a href="cue.md">CUE</a> .</td>
</tr>
<tr class="even">
<td>puede obtener una vista previa</td>
<td>Devuelve <strong>true</strong> si el dispositivo admite versiones preliminares.</td>
</tr>
<tr class="odd">
<td>puede grabar</td>
<td>Devuelve <strong>true</strong> si el dispositivo admite la grabación.</td>
</tr>
<tr class="even">
<td>puede invertir</td>
<td>Devuelve <strong>true</strong> si el dispositivo puede reproducirse en orden inverso.</td>
</tr>
<tr class="odd">
<td>puede guardar</td>
<td>Devuelve <strong>true</strong> si el dispositivo puede guardar datos.</td>
</tr>
<tr class="even">
<td>se puede extender</td>
<td>Devuelve <strong>true</strong> si el dispositivo puede expandir fotogramas para rellenar un rectángulo de presentación determinado.</td>
</tr>
<tr class="odd">
<td>puede extender la entrada</td>
<td>Devuelve <strong>true</strong> si el dispositivo puede cambiar el tamaño de una imagen en el proceso de digitalización en el búfer de fotogramas.</td>
</tr>
<tr class="even">
<td>puede probar</td>
<td>Devuelve <strong>true</strong> si el dispositivo reconoce la palabra clave de prueba.</td>
</tr>
<tr class="odd">
<td>cav</td>
<td>Cuando se combina con otros elementos, esta marca especifica que la información de devolución se aplica al formato CAV de los videodiscos. Este es el valor predeterminado si no se inserta ningún CD.</td>
</tr>
<tr class="even">
<td>tasa de incremento de reloj</td>
<td>Devuelve el número de subdivisiones que admite el reloj externo por segundo. Si el reloj externo es un reloj de milisegundos, el valor devuelto es 1000. Si el valor devuelto es 0, no se admite ningún reloj.</td>
</tr>
<tr class="odd">
<td>clv</td>
<td>Cuando se combina con otros elementos, esta marca especifica que la información de devolución se aplica al formato CLV de los videodiscos.</td>
</tr>
<tr class="even">
<td>dispositivo compuesto</td>
<td>Devuelve <strong>true</strong> si el dispositivo admite un nombre de elemento (nombre de archivo).</td>
</tr>
<tr class="odd">
<td>tipo de dispositivo</td>
<td>Devuelve un nombre de tipo de dispositivo, que puede ser uno de los siguientes:
<ul>
<li>cdaudio</li>
<li>incrementa</li>
<li>digitalvideo</li>
<li>Otros</li>
<li>overlay</li>
<li>escáner</li>
<li>sequencer</li>
<li>vídeos</li>
<li>videodisco</li>
<li>waveaudio</li>
</ul></td>
</tr>
<tr class="even">
<td>velocidad de reproducción rápida</td>
<td>Devuelve la velocidad de reproducción rápida en fotogramas por segundo o cero si el dispositivo no se puede reproducir rápidamente.</td>
</tr>
<tr class="odd">
<td>tiene audio</td>
<td>Devuelve <strong>true</strong> si el dispositivo admite la reproducción de audio.</td>
</tr>
<tr class="even">
<td>tiene reloj</td>
<td>Devuelve <strong>true</strong> si el dispositivo tiene un reloj.</td>
</tr>
<tr class="odd">
<td>todavía</td>
<td>Devuelve <strong>true</strong> si el dispositivo trata los archivos con una sola imagen de forma más eficaz que los archivos de vídeo de movimiento.</td>
</tr>
<tr class="even">
<td>tiene código de tiempo</td>
<td>Devuelve <strong>true</strong> si el dispositivo es capaz de admitir el código de tiempo, o si se desconoce.</td>
</tr>
<tr class="odd">
<td>tiene vídeo</td>
<td>Devuelve <strong>true</strong> si el dispositivo admite vídeo.</td>
</tr>
<tr class="even">
<td>inputs</td>
<td>Devuelve el número total de dispositivos de entrada.</td>
</tr>
<tr class="odd">
<td>velocidad máxima de reproducción</td>
<td>Devuelve la velocidad de reproducción máxima, en fotogramas por segundo, del dispositivo.</td>
</tr>
<tr class="even">
<td>velocidad de reproducción mínima</td>
<td>Devuelve la velocidad de reproducción mínima, en fotogramas por segundo, del dispositivo.</td>
</tr>
<tr class="odd">
<td>velocidad de reproducción normal</td>
<td>Devuelve la velocidad de reproducción normal, en fotogramas por segundo, del dispositivo.</td>
</tr>
<tr class="even">
<td>número de marcas</td>
<td>Devuelve el número máximo de marcas que se pueden usar; cero indica que no se admiten las marcas.</td>
</tr>
<tr class="odd">
<td>outputs</td>
<td>Devuelve el número total de dispositivos de salida.</td>
</tr>
<tr class="even">
<td>precisión de búsqueda</td>
<td>Devuelve la precisión esperada de una búsqueda en marcos; 0 indica que el dispositivo es preciso fotograma, 1 indica que el dispositivo espera estar dentro de un fotograma de la posición de búsqueda indicada, etc.</td>
</tr>
<tr class="odd">
<td>velocidad de reproducción lenta</td>
<td>Devuelve la velocidad de reproducción lenta en fotogramas por segundo, o bien cero si el dispositivo no se puede reproducir lentamente.</td>
</tr>
<tr class="even">
<td>utiliza archivos</td>
<td>Devuelve <strong>true</strong> si el almacenamiento de datos utilizado por un dispositivo compuesto es un archivo.</td>
</tr>
<tr class="odd">
<td>usar paletas</td>
<td>Devuelve <strong>true</strong> si el dispositivo usa las paletas.</td>
</tr>
<tr class="even">
<td>Windows</td>
<td>Devuelve el número de ventanas de pantalla simultáneas que el dispositivo puede admitir.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve información en el parámetro *lpszReturnString* de la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) . La información depende del tipo de solicitud.

## <a name="examples"></a>Ejemplos

El siguiente comando devuelve el tipo de dispositivo del dispositivo "".

``` syntax
capability mysound device type
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

[indicación](cue.md)
</dt> </dl>

 

