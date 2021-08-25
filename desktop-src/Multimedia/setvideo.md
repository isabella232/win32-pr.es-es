---
title: Comando setvideo
description: El comando setvideo establece los valores asociados a la reproducción y captura de vídeo. Los dispositivos de vídeo digital y VCR reconocen este comando.
ms.assetid: a6851b9b-e09a-4251-bd1c-19b1e4b6f871
keywords:
- Comando setvideo Windows Multimedia
topic_type:
- apiref
api_name:
- setvideo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 674b8b35c21fa54f1c2ecfc8b9dff531266c319b827d675da46be04e6c7abe8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805385"
---
# <a name="setvideo-command"></a>Comando setvideo

El comando setvideo establece los valores asociados a la reproducción y captura de vídeo. Los dispositivos de vídeo digital y VCR reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("setvideo %s %s %s"), 
  lpszDeviceID, 
  lpszVideo, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszVideo"></span><span id="lpszvideo"></span><span id="LPSZVIDEO"></span>*lpszVideo*
</dt> <dd>

Marca para la reproducción y captura de vídeo. En la tabla siguiente se enumeran los tipos de dispositivo que reconocen el **comando setvideo** y las marcas usadas por cada tipo.



| Valor        | Significado                                                                                                                                                                                        | Significado                                                                                                                                                                                                                                                                                                |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | bits *de* algoritmo de algoritmoperpulo para contar el brillo al *factor* clocktimecolor para factorar el contraste del *factor* gamma al valor halftoneinputkey color to *r:g:b* key index offonoutput | sobre el color de la paleta de duración sobre el identificador de la paleta de índice  a  *newrgb* para controlar la velocidad de fotogramas del registro de *descriptor* de calidad para la velocidad de la inejecidad del registro en la grabación en el *origen del*  *factor* al valor del número de origen todavía algoritmo de algoritmo de calidad de flujo de *descriptor* para numerar el tono al *factor*  |
| Vcr          | offonmonitor to *type number* *record* offrecord track number off *\_ off*                                                                                                               | record onrecord track *\_ number* onsource to *type number* *track* number *track \_ number* offtrack *\_ number* on                                                                                                                                                                             |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el **parámetro lpszVideo** y sus significados.



| Valor                                          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algoritmo *de algoritmo*                          | Especifica un algoritmo de compresión de vídeo para que lo use un comando [de reserva](reserve.md) o [registro](record.md) posterior. Los algoritmos admitidos por un dispositivo son específicos del dispositivo. MCI define las constantes "mpeg" y "h261" para el *algoritmo*. Si el algoritmo especificado entra en conflicto con el formato de archivo actual, el formato de archivo cambia al formato predeterminado para el algoritmo.<br/>                                                                                                                                     |
| bitsperpel to *count*                          | Establece el número de bits por píxel para guardar datos con el [comando capture](capture.md) [o record.](record.md)                                                                                                                                                                                                                                                                                                                                                                                                              |
| brillo a *factor*                         | Establece el nivel de brillo del vídeo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| clocktime                                      | Indica que el tiempo especificado en la marca "over" es en milisegundos. El tiempo es absoluto y no está en el paso con la reproducción del área de trabajo.                                                                                                                                                                                                                                                                                                                                                                                |
| color a *factor*                              | Establece el nivel de saturación de color.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| contraste con *factor*                           | Establece el nivel de contraste de vídeo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| gamma a *valor*                               | Especifica el exponente de corrección gamma multiplicado por 1000. Por ejemplo, para especificar un exponente de 2.2, use 2200 como *valor*. Un valor gamma de 1,0 (1000) indica que no se aplica ninguna corrección gamma. La corrección gamma ajusta la asignación entre la intensidad codificada en el origen de la presentación y el brillo mostrado.                                                                                                                                                                                                 |
| Semitonos                                       | Hace que se utilice la paleta de medio tono en lugar de la paleta predeterminada. Esta marca solo la reconoce el controlador de vídeo digital MCIAVI.                                                                                                                                                                                                                                                                                                                                                                                         |
| input                                          | Modifica la marca "brillo", "color", "contraste", "gamma", "nidez" o "tono" para que afecte a la señal de entrada y modifique lo que se registra. Si es posible, este es el valor predeterminado al supervisar la entrada.                                                                                                                                                                                                                                                                                                             |
| color de clave *a r:g:b*                           | Establece el color de la clave. La *variable r:g:b* es un valor RGB. Dos puntos (:) separe los valores rojo, verde y azul individuales.                                                                                                                                                                                                                                                                                                                                                                                                       |
| índice de clave para *indexar*                           | Establece el índice de clave. La *variable de* índice es un índice de paleta físico.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| supervisar para *escribir el número* de *número*              | Controla qué entrada de origen se pasará a la salida de VCR, sin cambiar la selección de entrada de origen de grabación. El tipo puede ser "output" o uno de los orígenes de entrada válidos. Si no se especifica "number", se elige la primera entrada de ese tipo.                                                                                                                                                                                                                                                                        |
| offon                                          | Habilita o deshabilita la visualización del vídeo. Al deshabilitar el vídeo, [](put.md) se establecen los píxeles del rectángulo "destino" (o su valor predeterminado, la región cliente de la ventana actual) en un color sólido. No tiene ningún efecto en el búfer de fotogramas. El origen del vídeo, ya sea el área de trabajo o una entrada externa, podría seguir almacenando nuevas imágenes en el búfer de fotogramas. No se muestran hasta que se habilita el vídeo. Puede usar el [comando](window.md) "estado" de la ventana para ocultar la ventana. El valor predeterminado **es setvideo** "on".<br/> |
| output                                         | Modifica la marca "brillo", "color", "contraste", "gamma", "nidez" o "tono" para que solo modifique la señal mostrada y no lo que se registra. Si es posible, este es el valor predeterminado al supervisar un archivo.                                                                                                                                                                                                                                                                                                           |
| a lo *largo de la duración*                                | Especifica cuánto tiempo se debe tardar en realizar un cambio que usa una *variable de* factor. Las unidades de *duración* están en el formato de hora actual. Los cambios se producen paso a paso con la reproducción del área de trabajo. Cuando se suspende la reproducción, el cambio también se suspende hasta que la reproducción continúa. Si no se usa "over" o no se admite, el cambio se produce inmediatamente.                                                                                                                                                                    |
| color de *la paleta* sobre *el índice* *a newrgb* | Establece un nuevo color de paleta. Los parámetros de color e índice especifican el *color* y el índice de paleta que se van a *cambiar.* newrgb especifica el nuevo *color.* Esta marca solo la reconoce el controlador de vídeo digital MCIAVI.                                                                                                                                                                                                                                                                                               |
| identificador de paleta que se debe *controlar*                     | Especifica el identificador de una paleta que el dispositivo debe usar para la representación. Este elemento solo es compatible con dispositivos que usan paletas. Si *handle* es cero, se usa la paleta predeterminada. Los dispositivos de vídeo digital no deben liberar la paleta pasada con este comando. Las aplicaciones deben liberarla después de cerrar el dispositivo.<br/>                                                                                                                                                                                                 |
| descriptor *de calidad*                           | Especifica las características de la compresión de vídeo realizada cuando el vídeo se graba en un archivo. Todos los dispositivos admiten los tres descriptores: "bajo", "medio" y "alto". El valor predeterminado es específico del dispositivo. La importancia de estos nombres depende del algoritmo y del dispositivo. Los dispositivos pueden definir nombres de descriptor adicionales. El [comando quality](quality.md) se puede usar para definir nombres de descriptor adicionales. Si no se usa la marca "algoritmo", el *descriptor* se aplica al algoritmo actual.<br/>   |
| velocidad de fotogramas de registro a *velocidad*                    | Establece la grabación del vídeo de movimiento. La velocidad *de* grabación se especifica en unidades de fotogramas por segundo multiplicada por 1000. Por ejemplo, la velocidad de fotogramas UNOS de 29,97 fotogramas por segundo se representa como 29970.                                                                                                                                                                                                                                                                                                                   |
| record onrecord off                            | Habilita o deshabilita la grabación de datos de vídeo. La grabación de datos de vídeo es el valor predeterminado.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| número de pista *de pista de registro \_ desactivado*               | Borra la selección del origen de vídeo para que no se grabe ningún vídeo con el siguiente [comando de](record.md) grabación. "Track" permite la selección de pista independiente. Si no se especifica "track", se supone un valor predeterminado de 1. Es posible que sea necesario emitir primero un comando [set](set.md) "assemble record off" antes de que se pueda desactivar la grabación de vídeo.                                                                                                                                                                     |
| número de pista *de \_ seguimiento de registros* en                | Selecciona el origen de vídeo que se va a grabar con el siguiente **comando de** registro. "Track" permite la selección de pista independiente. La pista 2 corresponde a la pista de PCM en Hi8. Si no se especifica "track", se supone un valor predeterminado de 1.                                                                                                                                                                                                                                                                                                      |
| nidez a *factor*                          | Establece el nivel de nidez del vídeo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| valor de origen *a número* de *origen*              | Establece el origen de la entrada de vídeo. Esto suele corresponder a conectores externos. Las constantes definidas para *source* incluyen "rgb", "pal", "álisis", "svideo" y "secam". Si existe más de una entrada del tipo especificado, el valor *"number"* opcional indica la entrada deseada. Por ejemplo, **setvideo** "source to sin número 2" especifica la segunda entrada NTES. Si se omite *el origen* "to", el origen absoluto se usa tal y como se define en el comando ["origen](list.md) de vídeo" de la lista.<br/>            |
| source to *type number* *number*               | Selecciona el origen de vídeo que se va a grabar en la cinta. *El* tipo debe ser "tuner", "line", "svideo", "aux", "generic", "mute" o "rgb".                                                                                                                                                                                                                                                                                                                                                                                              |
| algoritmo *still*                    | Especifica el algoritmo de compresión de imágenes fijas utilizado por el [comando capture.](capture.md) Cada dispositivo debe admitir un *algoritmo* de "none", lo que significa que no hay compresión. Este es el valor predeterminado. En este caso, los dispositivos de vídeo digital guardarán imágenes fijas como mapas de bits independientes del dispositivo RGB. Los dispositivos también pueden admitir una lista específica del dispositivo de algoritmos adicionales.                                                                                                                                                           |
| descriptor de calidad *de still*                     | Especifica las características de la compresión de imagen fija realizada al capturar una imagen fija. Todos los dispositivos admiten los descriptores "low", "medium" y "high". El valor predeterminado es específico del dispositivo. Si no se usa la marca "algoritmo", el *descriptor* se aplica al algoritmo actual.<br/> El [comando quality](quality.md) se puede usar para definir otros nombres de descriptor.<br/>                                                                                                                            |
| flujo a *número*                             | Especifica la secuencia de vídeo que se reproduce desde el área de trabajo. Si no se especifica la secuencia y el formato de archivo no define una secuencia predeterminada, se reproduce la primera secuencia de vídeo intercalada físicamente.                                                                                                                                                                                                                                                                                                                 |
| tint to *factor*                               | Establece el tono de la imagen. Normalmente, este ajuste se modela después del control de tono de muchos conjuntos de televisión de color, con 250 significado verde, 750 significa rojo y 0 (o                                                                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify", "test" o una combinación de estos. Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Comentarios

En el caso de los dispositivos VCR, el *uso \_* de setvideo con una marca que desactiva una pista individual ("número de pista de seguimiento desactivado") puede hacer que la aplicación reciba un mensaje de estado que indica que no se pudo llevar a cabo el comando. Algunas VCR solo pueden desactivar combinaciones de pistas, no pistas individuales. por ejemplo, la primera pista de audio y una pista de vídeo de un vídeo de vídeo. En este caso, simplemente use [setaudio](setaudio.md) y setvideo para seguir desactivando las otras pistas que conste de la combinación. El controlador apagará las pistas cuando reciba el comando para desactivar la última pista de la combinación.

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

[capturar](capture.md)
</dt> <dt>

[list](list.md)
</dt> <dt>

[Poner](put.md)
</dt> <dt>

[record](record.md)
</dt> <dt>

[reserva](reserve.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[setaudio](setaudio.md)
</dt> <dt>

[Ventana](window.md)
</dt> </dl>

 

