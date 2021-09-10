---
title: comando play
description: El comando play comienza a reproducir un dispositivo. Los dispositivos cd audio, digital-video, secuenciador MIDI, videodisc, VCR y audio de onda reconocen este comando.
ms.assetid: 3ee707d6-6af4-494d-a887-d91ea5666ac4
keywords:
- comando play Windows Multimedia
topic_type:
- apiref
api_name:
- play
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf262db152677ef5a2f29de9526152c1d48d4c9
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369832"
---
# <a name="play-command"></a>comando play

El comando play comienza a reproducir un dispositivo. Los dispositivos cd audio, digital-video, secuenciador MIDI, videodisc, VCR y audio de onda reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("play %s %s %s"), 
  lpszDeviceID, 
  lpszPlayFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszPlayFlags*
</dt> <dd>

Marca para reproducir un dispositivo. En la tabla siguiente se enumeran los tipos de dispositivo que reconocen el comando **play** y las marcas usadas por cada tipo.



| Value        | Significado                          | Significado                           |
|--------------|----------------------------------|-----------------------------------|
| cdaudio      | desde *la posición*                  | para *colocar*                     |
| digitalvideo | desde *la posición de* la repetición de pantalla completa | ventana invertir *a* posición       |
| sequencer    | desde *la posición*                  | para *colocar*                     |
| Vcr          | en *el momento desde* la posición *inversa*  | examinar hasta *la posición*                |
| Videodisco    | examen inverso rápido *desde la* posición | entero de velocidad *lenta para* *colocar* |
| waveaudio    | desde *la posición*                  | para *colocar*                     |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el **parámetro lpszPlayFlags** y sus significados.



| Value           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en *el momento*       | Indica cuándo debe comenzar el dispositivo a realizar este comando o, si el dispositivo se ha cued, cuando comienza el comando cued. Para obtener más información, vea el [comando cue.](cue.md)                                                                                                                                                                                                                                                                 |
| fast            | Indica que el dispositivo debe reproducirse más rápido de lo normal. Para determinar la velocidad exacta en un reproductor de videodisc, use la marca "speed" del comando [status.](status.md) Para especificar la velocidad con más precisión, use la marca "speed" de este comando.                                                                                                                                                                                                   |
| desde *la posición* | Especifica una posición inicial para la reproducción. Si no se especifica la marca "from", la reproducción comienza en la posición actual. En el caso de los dispositivos **cdaudio,** si la posición "from" es mayor que la posición final del disco, o si la posición "from" es mayor que la posición "to", el controlador devuelve un error. En el caso de los dispositivos **videodisc,** las posiciones predeterminadas están en fotogramas para los discos DE LAV y en horas, minutos y segundos para los discos CLV. |
| Fullscreen      | Especifica que se debe usar una pantalla a pantalla completa. Use esta marca solo al reproducir archivos comprimidos. (Los archivos sin comprimir no se reproducirán a pantalla completa).                                                                                                                                                                                                                                                                                                  |
| Repetir          | Especifica que la reproducción se debe reiniciar cuando se alcanza el final del contenido.                                                                                                                                                                                                                                                                                                                                                                       |
| reverse         | Especifica que la dirección de reproducción es hacia atrás. No se puede especificar una ubicación final con la marca "reverse". En el caso de los vídeosdiscos, el "examen" solo se aplica al formato DESUSO.                                                                                                                                                                                                                                                                                     |
| escanear            | Se reproduce lo más rápido posible sin deshabilitar el vídeo (aunque el audio podría estar deshabilitado). En el caso de los vídeosdiscos, el "examen" solo se aplica al formato DESUSO.                                                                                                                                                                                                                                                                                                             |
| lento            | Se reproduce lentamente. Para determinar la velocidad exacta en un reproductor de videodisc, use la marca "speed" del comando [status.](status.md) Para especificar la velocidad con más precisión, use la marca "speed" de este comando. En el caso de los videodiscs, "slow" solo se aplica al formato CSV.                                                                                                                                                                                            |
| speed *integer* | Reproduce un vídeodisc a la velocidad especificada, en fotogramas por segundo. Esta marca solo se aplica a los discos DE MOMENTO.                                                                                                                                                                                                                                                                                                                                                 |
| para *colocar*   | Especifica una posición final para la reproducción. Si no se especifica la marca "to", la reproducción se detiene al final del contenido. En el caso de los dispositivos **cdaudio,** si la posición "to" es mayor que la posición final del disco, el controlador devuelve un error. En el caso de los dispositivos **videodisc,** las posiciones predeterminadas están en fotogramas para los discos DE LAV y en horas, minutos y segundos para los discos CLV.                                                                  |
| periodo          | Especifica que la reproducción debe usar la ventana asociada a la instancia del dispositivo. Esta es la configuración predeterminada.                                                                                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital y VCR, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Antes de emitir comandos que usan valores de posición, debe establecer el formato de hora deseado mediante el [comando set.](set.md) Este comando comienza a reproducirse a la velocidad actual, tal como se establece con el comando set "speed". La dirección es inversa si se especifica la marca "reverse" o si la marca "to" se especifica como un valor menor que la marca "from". Si no se especifica la marca "from", la reproducción comienza en la posición actual. Las marcas "to" y "reverse" no se pueden usar juntas.

## <a name="examples"></a>Ejemplos

El comando siguiente reproduce el dispositivo "my sound" desde la posición 1000 hasta la posición 2000 y envía un mensaje de notificación cuando se completa la reproducción.

``` syntax
play mysound from 1000 to 2000 notify
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

[Cue](cue.md)
</dt> <dt>

[set](set.md)
</dt> </dl>

 

