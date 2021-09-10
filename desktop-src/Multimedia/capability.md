---
title: comando capability
description: El comando de funcionalidad solicita información sobre una funcionalidad determinada de un dispositivo. Todos los dispositivos MCI reconocen este comando.
ms.assetid: 1b470473-0de6-41ba-9f6e-41f0b13ceaeb
keywords:
- comando de funcionalidad Windows Multimedia
topic_type:
- apiref
api_name:
- capability
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44e57a793f799214753f50504d80bce7051fba14
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369828"
---
# <a name="capability-command"></a>comando capability

El comando de funcionalidad solicita información sobre una funcionalidad determinada de un dispositivo. Todos los dispositivos MCI reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

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

Marca que identifica una funcionalidad del dispositivo. En la tabla siguiente se enumeran los tipos de dispositivo que reconocen el comando **de** funcionalidad y las marcas usadas por cada tipo:




| Value | Tipo | Tipo | 
|-------|------|------|
| cdaudio | <ul><li>puede expulsar</li><li>puede reproducir</li><li>puede grabar</li><li>puede guardar</li><li>dispositivo compuesto</li></ul> | <ul><li>tipo de dispositivo</li><li>tiene audio</li><li>tiene vídeo</li><li>usa archivos</li></ul> | 
| digitalvideo | <ul><li>puede expulsar</li><li>se puede inmovilizar</li><li>puede bloquear</li><li>puede reproducir</li><li>puede grabar</li><li>puede invertir</li><li>puede guardar</li><li>se puede extender</li><li>puede extender la entrada</li><li>puede probar</li></ul> | <ul><li>dispositivo compuesto</li><li>tipo de dispositivo</li><li>tiene audio</li><li>Todavía</li><li>tiene vídeo</li><li>velocidad de reproducción máxima</li><li>velocidad de reproducción mínima</li><li>usa archivos</li><li>usa paletas</li><li>Windows</li></ul> | 
| overlay | <ul><li>puede expulsar</li><li>se puede inmovilizar</li><li>puede reproducir</li><li>puede grabar</li><li>puede guardar</li><li>se puede extender</li></ul> | <ul><li>dispositivo compuesto</li><li>tipo de dispositivo</li><li>tiene audio</li><li>tiene vídeo</li><li>usa archivos</li><li>Windows</li></ul> | 
| sequencer | <ul><li>puede expulsar</li><li>puede reproducir</li><li>puede grabar</li><li>puede guardar</li><li>dispositivo compuesto</li></ul> | <ul><li>tipo de dispositivo</li><li>tiene audio</li><li>tiene vídeo</li><li>usa archivos</li></ul> | 
| Vcr | <ul><li>puede detectar la longitud</li><li>puede expulsar</li><li>se puede inmovilizar</li><li>puede supervisar los orígenes</li><li>puede reproducir</li><li>puede realizar la inscripción previa</li><li>puede obtener una vista previa</li><li>puede grabar</li><li>puede invertir</li><li>puede guardar</li><li>puede probar</li></ul> | <ul><li>velocidad de incremento del reloj</li><li>dispositivo compuesto</li><li>tipo de dispositivo</li><li>tiene audio</li><li>tiene reloj</li><li>tiene código de tiempo</li><li>tiene vídeo</li><li>número de marcas</li><li>buscar precisión</li><li>usa archivos</li></ul> | 
| Videodisco | <ul><li>puede expulsar</li><li>puede reproducir</li><li>puede grabar</li><li>puede invertir</li><li>puede guardar</li><li>CAV</li><li>CLV</li><li>dispositivo compuesto</li></ul> | <ul><li>tipo de dispositivo</li><li>velocidad de reproducción rápida</li><li>tiene audio</li><li>tiene vídeo</li><li>velocidad de reproducción normal</li><li>velocidad de reproducción lenta</li><li>usa archivos</li></ul> | 
| waveaudio | <ul><li>puede expulsar</li><li>puede reproducir</li><li>puede grabar</li><li>puede guardar</li><li>dispositivo compuesto</li><li>tipo de dispositivo</li></ul> | <ul><li>tiene audio</li><li>tiene vídeo</li><li>inputs</li><li>outputs</li><li>usa archivos</li></ul> | 




 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el *parámetro lpszRequest* y sus significados:




| Marcas | Significado | 
|-------|---------|
| puede detectar la longitud | Devuelve <strong>TRUE</strong> si el dispositivo puede detectar la longitud del medio. | 
| puede expulsar | Devuelve <strong>TRUE</strong> si el dispositivo puede expulsar los medios. | 
| se puede inmovilizar | Devuelve <strong>TRUE</strong> si el dispositivo puede inmovilizar los datos en el búfer de fotogramas. | 
| puede bloquear | Devuelve <strong>TRUE</strong> si el dispositivo puede bloquear los datos. | 
| puede supervisar los orígenes | Devuelve <strong>TRUE</strong> si el dispositivo puede pasar una entrada (origen) a la salida supervisada, independientemente de la selección de entrada actual. | 
| puede reproducir | Devuelve <strong>TRUE</strong> si el dispositivo puede reproducirse. | 
| puede realizar la inscripción previa | Devuelve <strong>TRUE</strong> si el dispositivo admite la marca "preroll" con el <a href="cue.md">comando cue.</a> | 
| puede obtener una vista previa | Devuelve <strong>TRUE</strong> si el dispositivo admite versiones preliminares. | 
| puede grabar | Devuelve <strong>TRUE si</strong> el dispositivo admite la grabación. | 
| puede invertir | Devuelve <strong>TRUE</strong> si el dispositivo puede reproducirse a la inversa. | 
| puede guardar | Devuelve <strong>TRUE</strong> si el dispositivo puede guardar datos. | 
| se puede extender | Devuelve <strong>TRUE</strong> si el dispositivo puede extender marcos para rellenar un rectángulo de presentación determinado. | 
| puede extender la entrada | Devuelve <strong>TRUE</strong> si el dispositivo puede cambiar el tamaño de una imagen en el proceso de digitalización en el búfer de fotogramas. | 
| puede probar | Devuelve <strong>TRUE</strong> si el dispositivo reconoce la palabra clave test. | 
| Cav | Cuando se combina con otros elementos, esta marca especifica que la información de devolución se aplica a los videodiscos en formato DESER. Este es el valor predeterminado si no se inserta videodisc. | 
| velocidad de incremento del reloj | Devuelve el número de subdivisiones que admite el reloj externo por segundo. Si el reloj externo es un reloj de milisegundos, el valor devuelto es 1000. Si el valor devuelto es 0, no se admite ningún reloj. | 
| clv | Cuando se combina con otros elementos, esta marca especifica que la información de devolución se aplica a los vídeos en formato CLVdiscs. | 
| dispositivo compuesto | Devuelve <strong>TRUE</strong> si el dispositivo admite un nombre de elemento (nombre de archivo). | 
| tipo de dispositivo | Devuelve un nombre de tipo de dispositivo, que puede ser uno de los siguientes:<ul><li>cdaudio</li><li>Dat</li><li>digitalvideo</li><li>otro</li><li>overlay</li><li>escáner</li><li>sequencer</li><li>Vcr</li><li>Videodisco</li><li>waveaudio</li></ul> | 
| velocidad de reproducción rápida | Devuelve la velocidad de reproducción rápida en fotogramas por segundo o cero si el dispositivo no puede reproducirse rápidamente. | 
| tiene audio | Devuelve <strong>TRUE si</strong> el dispositivo admite la reproducción de audio. | 
| tiene reloj | Devuelve <strong>TRUE</strong> si el dispositivo tiene un reloj. | 
| Todavía | Devuelve <strong>TRUE</strong> si el dispositivo trata los archivos con una sola imagen de forma más eficaz que los archivos de vídeo de movimiento. | 
| tiene código de tiempo | Devuelve <strong>TRUE</strong> si el dispositivo es capaz de admitir el código de tiempo o si se desconoce. | 
| tiene vídeo | Devuelve <strong>TRUE</strong> si el dispositivo admite vídeo. | 
| inputs | Devuelve el número total de dispositivos de entrada. | 
| velocidad de reproducción máxima | Devuelve la velocidad de reproducción máxima, en fotogramas por segundo, para el dispositivo. | 
| velocidad de reproducción mínima | Devuelve la velocidad de reproducción mínima, en fotogramas por segundo, para el dispositivo. | 
| velocidad de reproducción normal | Devuelve la velocidad de reproducción normal, en fotogramas por segundo, para el dispositivo. | 
| número de marcas | Devuelve el número máximo de marcas que se pueden usar; cero indica que las marcas no se admiten. | 
| outputs | Devuelve el número total de dispositivos de salida. | 
| buscar precisión | Devuelve la precisión esperada de una búsqueda en fotogramas; 0 indica que el dispositivo es preciso, 1 indica que el dispositivo espera estar dentro de un fotograma de la posición de búsqueda indicada, y así sucesivamente. | 
| velocidad de reproducción lenta | Devuelve la velocidad de reproducción lenta en fotogramas por segundo o cero si el dispositivo no puede reproducirse lentamente. | 
| usa archivos | Devuelve <strong>TRUE</strong> si el almacenamiento de datos usado por un dispositivo compuesto es un archivo. | 
| usa paletas | Devuelve <strong>TRUE</strong> si el dispositivo usa paletas. | 
| Windows | Devuelve el número de ventanas de visualización simultáneas que el dispositivo puede admitir. | 




 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital y VCR, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve información en el *parámetro lpszReturnString* de la [**función mciSendString.**](/previous-versions//dd757161(v=vs.85)) La información depende del tipo de solicitud.

## <a name="examples"></a>Ejemplos

El comando siguiente devuelve el tipo de dispositivo del dispositivo "my sound".

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

[Cadenas de comandos de MCI](mci-command-strings.md)
</dt> <dt>

[Cue](cue.md)
</dt> </dl>

 

