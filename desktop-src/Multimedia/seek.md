---
title: comando seek
description: El comando seek se mueve a la posición especificada y se detiene. Los dispositivos cd audio, digital-video, secuenciador MIDI, VCR, videodisc y audio de forma de onda reconocen este comando.
ms.assetid: e9e8ca14-d181-4f29-b4d3-c7f5b0301164
keywords:
- comando seek Windows Multimedia
topic_type:
- apiref
api_name:
- seek
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 131b8138f67ae02d9a3d8f1e80693b0735368e2a622d5d8a7fe7c5a481da5542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892905"
---
# <a name="seek-command"></a>comando seek

El comando seek se mueve a la posición especificada y se detiene. Los dispositivos cd audio, digital-video, secuenciador MIDI, VCR, videodisc y audio de forma de onda reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("seek %s %s %s"), 
  lpszDeviceID, 
  lpszSeekFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszSeekFlags"></span><span id="lpszseekflags"></span><span id="LPSZSEEKFLAGS"></span>*lpszSeekFlags*
</dt> <dd>

Marca para moverse a una posición especificada. En la tabla siguiente se enumeran los tipos de dispositivo que reconocen el comando **seek** y las marcas usadas por cada tipo.



| Value        | Significado                          | Significado                      |
|--------------|----------------------------------|------------------------------|
| cdaudio      | to end to *position*             | empezar                     |
| digitalvideo | to end to *position*             | empezar                     |
| sequencer    | to end to *position*             | empezar                     |
| Vcr          | at *time* mark *\_ num* reverse | to end to *position* to start |
| Videodisco    | invertir hasta el final                   | para *colocar para* iniciar        |
| waveaudio    | to end to *position*             | empezar                     |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszSeekFlags** y sus significados.



| Value            | Significado                                                                                                                                                                                                          |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en *el momento*        | Indica cuándo debe comenzar el dispositivo a realizar este comando o, si el dispositivo se ha cued, cuando comienza el comando cued. Para obtener más información, vea el [comando cue.](cue.md)                             |
| mark *mark \_ num* | Busca la marca relativa indicada por *mark \_ num*, que debe ser un valor entero positivo. Las marcas son señales escritas en la cinta VCR mediante el comando [mark](mark.md) y se usan para la búsqueda a alta velocidad. |
| reverse          | Indica que la dirección de búsqueda en los videodiscos VCR y VCR está hacia atrás. Esta marca no es válida si se especifica la marca "to". En el caso de las V VCR, esta marca debe usarse con la marca "mark".                             |
| to end           | Busca hasta el final del contenido.                                                                                                                                                                                 |
| para *colocar*    | Especifica la posición para detener la búsqueda. En el caso de los dispositivos **cdaudio,** MCI devuelve un error fuera del intervalo si la posición especificada es mayor que la longitud del disco.                                            |
| empezar         | Busca al principio del contenido.                                                                                                                                                                               |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital y VCR, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Comentarios

Antes de emitir cualquier comando que use valores de posición, debe establecer el formato de hora deseado mediante el [comando set.](set.md)

Los dispositivos de vídeo digital admiten dos modos de búsqueda, que puede cambiar mediante el [comando set.](set.md) El modo "buscar exactamente en" hace que el comando seek se mueva al marco especificado. El modo "buscar exactamente desactivado" hace que el comando seek se mueva al fotograma clave más cercano antes del marco especificado.

Si se reproduce un dispositivo de audio de CD cuando se emite el comando seek, se detiene la reproducción. Cuando el comando seek se emite con un dispositivo videodisc, el dispositivo busca con avance rápido o retroceso rápido con vídeo y audio desactivados.

Cuando el comando seek se emite con un dispositivo de audio de forma de onda, el comportamiento depende del tamaño de la muestra. Si el tamaño de la muestra es de 16 bits o más, la búsqueda se mueve al principio de la muestra más cercana cuando una posición especificada no coincide con el inicio de una muestra.

## <a name="examples"></a>Ejemplos

El comando siguiente busca el inicio del archivo multimedia asociado al dispositivo "my sound".

``` syntax
seek mysound to start
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Cadenas de comandos de MCI](mci-command-strings.md)
</dt> <dt>

[Cue](cue.md)
</dt> <dt>

[Marca](mark.md)
</dt> <dt>

[set](set.md)
</dt> </dl>

 

