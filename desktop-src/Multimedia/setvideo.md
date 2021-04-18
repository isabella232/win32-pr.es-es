---
title: comando setvideo
description: El comando setvideo establece los valores asociados a la reproducción y la captura de vídeo. Los dispositivos digitales-vídeo y VCR reconocen este comando.
ms.assetid: a6851b9b-e09a-4251-bd1c-19b1e4b6f871
keywords:
- comando setvideo de Windows multimedia
topic_type:
- apiref
api_name:
- setvideo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa4c3d1e3b90b9ab0c5bf5791dacd541c8a8bc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422404"
---
# <a name="setvideo-command"></a>comando setvideo

El comando setvideo establece los valores asociados a la reproducción y la captura de vídeo. Los dispositivos digitales-vídeo y VCR reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

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

Marca para la reproducción y captura de vídeo. En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **setvideo** y las marcas usadas por cada tipo.



| Value        | Significado                                                                                                                                                                                        | Significado                                                                                                                                                                                                                                                                                                |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | algoritmo *de algoritmo BitsPerPel para* *recuento* de brillo al *factor* clocktimecolor para *factorizar* el contraste con el *factor gamma en* el *valor* halftoneinputkey color a *r:g: b* índice de clave para el *Índice* offonoutput | *color* de  la  *paleta de* *duración* superior en el identificador de la   *paleta de* *newrgb* para *administrar* la velocidad de fotogramas del registro del *descriptor* de calidad y el registro de la entrada de índice offsharpness   |
| vídeos          | offonmonitor para *escribir* número de número *de registro de número de* *pista de \_* seguimiento de offrecord                                                                                                               | registrar *\_ número* de pista de seguimiento de entrada en *origen para el número número de* pista *de seguimiento número* *de \_* *pista offtrack número \_* de pista en                                                                                                                                                                             |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszVideo** y su significado.



| Value                                          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *algoritmo* de algoritmo                          | Especifica un algoritmo de compresión de vídeo para su uso por parte de un comando de [reserva](reserve.md) o [registro](record.md) posterior. Los algoritmos admitidos por un dispositivo son específicos del dispositivo. MCI define las constantes "MPEG" y "H261" para el *algoritmo*. Si el algoritmo especificado entra en conflicto con el formato de archivo actual, el formato del archivo se cambia al formato predeterminado para el algoritmo.<br/>                                                                                                                                     |
| BitsPerPel para *recuento*                          | Establece el número de bits por píxel para guardar datos con el comando [Capture](capture.md) o [Record](record.md) .                                                                                                                                                                                                                                                                                                                                                                                                              |
| brillo al *factor*                         | Establece el nivel de brillo del vídeo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| clocktime                                      | Indica que la hora especificada en la marca "sobre" está en milisegundos. La hora es absoluta y no está en el paso con la reproducción del área de trabajo.                                                                                                                                                                                                                                                                                                                                                                                |
| color a *factor*                              | Establece el nivel de saturación de color.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| contraste con *factor*                           | Establece el nivel de contraste de vídeo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| gamma a *valor*                               | Especifica el exponente de corrección gamma multiplicado por 1000. Por ejemplo, para especificar un exponente de 2,2, use 2200 para el *valor*. Un valor gamma de 1,0 (1000) indica que no se aplica ninguna corrección gamma. La corrección gamma ajusta la asignación entre la intensidad codificada en el origen de presentación y el brillo mostrado.                                                                                                                                                                                                 |
| medio                                       | Hace que se use la paleta de semitonos en lugar de la paleta predeterminada. Esta marca solo se reconoce en el controlador de vídeo digital MCIAVI.                                                                                                                                                                                                                                                                                                                                                                                         |
| input                                          | Modifica las marcas "luminosidad", "color", "Contrast", "gamma", "nitidez" o "matiz" para que afecte a la señal de entrada y modifique lo que se registra. Si es posible, es el valor predeterminado al supervisar la entrada.                                                                                                                                                                                                                                                                                                             |
| color de la clave a *r:g: b*                           | Establece el color de la clave. La variable *r:g: b* es un valor RGB. Dos puntos (:) Separe los valores individuales de rojo, verde y azul.                                                                                                                                                                                                                                                                                                                                                                                                       |
| Índice de clave que se va a *indexar*                           | Establece el índice de la clave. La variable de *Índice* es un índice de paleta física.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Monitor para *escribir* *número* número              | Controla qué entrada de origen se pasará a la salida de VCR, sin cambiar la selección de entrada de origen de grabación. El tipo puede ser "Output" o uno de los orígenes de entrada válidos. Si no se especifica "número", se elige la primera entrada de ese tipo.                                                                                                                                                                                                                                                                        |
| offon                                          | Habilita o deshabilita la presentación de vídeo. Al deshabilitar el vídeo, se establecen los píxeles del rectángulo "destino" [Put](put.md) (o su valor predeterminado, la región cliente de la ventana actual) en un color sólido. No tiene ningún efecto en el búfer de fotogramas. El origen de vídeo, ya sea el área de trabajo o una entrada externa, puede continuar almacenando nuevas imágenes en el búfer de fotogramas. No se muestran hasta que se habilita el vídeo. Puede usar el comando "State" de la [ventana](window.md) para ocultar la ventana. El valor predeterminado es **setvideo** "ON".<br/> |
| output                                         | Modifica las marcas "Brightness", "color", "Contrast", "gamma", "nitidez" o "matiz" de modo que solo modifique la señal mostrada y no lo que se grabe. Si es posible, es el valor predeterminado al supervisar un archivo.                                                                                                                                                                                                                                                                                                           |
| a lo largo de la *duración*                                | Especifica cuánto tiempo se debe tardar en realizar un cambio que utiliza una variable de *factor* . Las unidades de *duración* se encuentran en el formato de hora actual. Los cambios se producen en el paso con la reproducción del área de trabajo. Cuando se suspende la reproducción, el cambio también se suspende hasta que continúe la reproducción. Si no se usa "over" o no se admite, el cambio se produce inmediatamente.                                                                                                                                                                    |
| *color* de color de la paleta sobre el *Índice* a *newrgb* | Establece un nuevo color de la paleta. El color y el índice de la paleta que se va a cambiar se especifican mediante los parámetros de *color* y de *Índice* ; *newrgb* especifica el nuevo color. Esta marca solo se reconoce en el controlador de vídeo digital MCIAVI.                                                                                                                                                                                                                                                                                               |
| identificador de la paleta que se va a *controlar*                     | Especifica el identificador de una paleta que el dispositivo debe usar para la representación. Este elemento solo es compatible con dispositivos que usan paletas. Si el *identificador* es cero, se usa la paleta predeterminada. Los dispositivos de vídeo digital no deben liberar la paleta pasada con este comando. Las aplicaciones deben liberarla después de cerrar el dispositivo.<br/>                                                                                                                                                                                                 |
| *descriptor* de calidad                           | Especifica las características de la compresión de vídeo realizada cuando el vídeo se graba en un archivo. Todos los dispositivos admiten los tres descriptores: "Low", "Medium" y "High". El valor predeterminado es específico del dispositivo. La importancia de estos nombres depende del algoritmo y del dispositivo. Los dispositivos pueden definir nombres de descriptores adicionales. El comando [Quality](quality.md) se puede usar para definir nombres de descriptores adicionales. Si no se utiliza la marca "Algorithm", el *descriptor* se aplica al algoritmo actual.<br/>   |
| velocidad de fotogramas de registro a *velocidad*                    | Establece la grabación del vídeo de movimiento. La *velocidad* de grabación se especifica en unidades de fotogramas por segundo multiplicado por 1000. Por ejemplo, la velocidad de fotogramas NTSC de 29,97 fotogramas por segundo se representa como 29970.                                                                                                                                                                                                                                                                                                                   |
| registrar registro                            | Habilita o deshabilita el registro de datos de vídeo. La grabación de datos de vídeo es el valor predeterminado.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| número de *pista \_* de seguimiento de registro desactivado               | Borra la selección de origen de vídeo para que no se grabe ningún vídeo con el siguiente comando de [registro](record.md) . "Track" permite la selección independiente de la pista. Si no se especifica "Track", se supone un valor predeterminado de 1. Puede que sea necesario emitir [primero un comando](set.md) "ensamblar registro desactivado" antes de que se pueda desactivar la grabación de vídeo.                                                                                                                                                                     |
| registrar *\_ número de pista* de pista en                | Selecciona el origen de vídeo que se va a grabar con el siguiente comando de **registro** . "Track" permite la selección independiente de la pista. El seguimiento 2 corresponde a la pista PCM en Hi8. Si no se especifica "Track", se asume un valor predeterminado de 1.                                                                                                                                                                                                                                                                                                      |
| nitidez del *factor*                          | Establece el nivel de nitidez de vídeo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| origen a *valor* de número de *origen*              | Establece el origen de la entrada de vídeo. Esto suele corresponder a conectores externos. Entre las constantes definidas para el *origen* se incluyen "RGB", "PAL", "NTSC", "Svideo" y "SECAM". Si existe más de una entrada del tipo especificado, el *valor* "número" opcional indica la entrada deseada. Por ejemplo, **setvideo** "origen a NTSC número 2" especifica la segunda entrada NTSC. Si se omite el *origen* "para", el origen absoluto se usa tal y como se define en el comando "origen de vídeo" de la [lista](list.md) .<br/>            |
| *número* de *tipo* número de origen               | Selecciona el origen de vídeo que se va a grabar en la cinta. El *tipo* debe ser "sintonizador", "línea", "Svideo", "AUX", "Generic", "silenciar" o "RGB".                                                                                                                                                                                                                                                                                                                                                                                              |
| *algoritmo* de algoritmo de todavía                    | Especifica el algoritmo de compresión de imagen que utiliza el comando de [captura](capture.md) . Cada dispositivo debe admitir un *algoritmo* de "ninguno", lo que significa que no hay compresión. Este es el valor predeterminado. En este caso, los dispositivos de vídeo digital guardan las imágenes seguidas como mapas de bits independientes del dispositivo RGB. Los dispositivos también pueden admitir una lista específica del dispositivo de algoritmos adicionales.                                                                                                                                                           |
| *descriptor* de calidad todavía                     | Especifica las características de la compresión de imágenes fijas realizadas durante la captura de una imagen fija. Todos los dispositivos admiten los descriptores "Low", "Medium" y "High". El valor predeterminado es específico del dispositivo. Si no se utiliza la marca "Algorithm", el *descriptor* se aplica al algoritmo actual.<br/> El comando [Quality](quality.md) se puede usar para definir otros nombres de descriptores.<br/>                                                                                                                            |
| flujo a *número*                             | Especifica la secuencia de vídeo que se reproduce desde el área de trabajo. Si no se especifica la secuencia y el formato de archivo no define una secuencia predeterminada, se reproducirá la primera secuencia de vídeo intercalada físicamente.                                                                                                                                                                                                                                                                                                                 |
| matiz a *factor*                               | Establece el matiz de la imagen. Normalmente, este ajuste se modela después del control de matiz de muchos conjuntos de televisión de color, con 250, lo que significa verde, 750, lo que significa rojo y 0 (o                                                                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify", "Test" o una combinación de estos. Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

En el caso de los dispositivos VCR, el uso de setvideo con una marca que desactive una pista individual ("hacer seguimiento del *\_ número de pista* ") puede hacer que la aplicación reciba un mensaje de estado que indica que el comando no se pudo llevar a cabo. Algunos VCR pueden desactivar solo combinaciones de pistas, no pistas individuales; por ejemplo, la primera pista de audio y una pista de vídeo de una cinta de vídeo. En este caso, simplemente use [SetAudio](setaudio.md) y setvideo para continuar con la desactivación de las otras pistas que componen la combinación. El controlador desactivará las pistas cuando reciba el comando para desactivar la última pista de la combinación.

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

[list](list.md)
</dt> <dt>

[pondrán](put.md)
</dt> <dt>

[record](record.md)
</dt> <dt>

[reserva](reserve.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[setaudio](setaudio.md)
</dt> <dt>

[ventana](window.md)
</dt> </dl>

 

