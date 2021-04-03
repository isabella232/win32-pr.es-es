---
title: Colocar en secuencias
description: Colocar en secuencias
ms.assetid: 97ab491d-1a58-4b4b-a13a-215be24dac1c
keywords:
- AVIStreamStart función)
- AVIStreamFindSample función)
- AVIStreamSampleToTime función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5252aa938d32c323da9fcf7ae106d11db0ff2fb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775402"
---
# <a name="positioning-in-streams"></a>Colocar en secuencias

AVIFile proporciona varias maneras de buscar y mover a una posición en un flujo de datos. Las funciones y macros de esta sección permiten que la aplicación busque la posición inicial, la longitud y los fotogramas clave (que contienen una imagen completa en el ejemplo) dentro de un flujo. Las funciones y macros también asocian el tiempo a las posiciones de una secuencia calculando el tiempo transcurrido necesario para reproducir un flujo desde el principio hasta cualquier punto de una secuencia.

## <a name="finding-the-starting-position"></a>Buscar la posición inicial

Puede recuperar el número de muestra del primer fotograma en una secuencia de vídeo mediante la función [**AVIStreamStart**](/windows/desktop/api/Vfw/nf-vfw-avistreamstart) . (Los fotogramas de una película pueden comenzar en el ejemplo 0 o 1, dependiendo de la preferencia del autor). También puede obtener esta información mediante la función [**AVIStreamInfo**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) . Esta función almacena el número de muestra en el miembro **dwStart** de la estructura [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) . Puede recuperar la hora de inicio del primer ejemplo de una secuencia mediante la macro [**AVIStreamStartTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamstarttime) .

Puede recuperar la longitud de la secuencia mediante la función [**AVIStreamLength**](/windows/desktop/api/Vfw/nf-vfw-avistreamlength) . Esta función devuelve el número de muestras de la secuencia. También puede obtener esta información mediante la función **AVIStreamInfo** . Esta función almacena la longitud del flujo en el miembro **dwLength** de la estructura **AVISTREAMINFO** . Para recuperar la longitud de una secuencia en milisegundos, utilice la macro [**AVIStreamLengthTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamlengthtime) .

En una secuencia de vídeo, cada ejemplo suele corresponder a un fotograma de vídeo. Sin embargo, podría haber ejemplos para los que no hay datos de vídeo. Si llama a la función [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) que especifica una de esas posiciones, devuelve una longitud de datos de 0 bytes. Puede encontrar ejemplos que contengan datos mediante la función [**AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample) y especificando la \_ marca buscar cualquier.

En una secuencia de audio, cada ejemplo corresponde a un bloque de datos de datos de audio. Por ejemplo, si los datos de audio tienen un formato ADPCM de 22 kHz (modulación de código de impulso diferencial adaptable), cada ejemplo de **AVIStreamLength** se corresponde con un bloque de 256 bytes de datos de audio comprimidos. Este bloque de datos de audio contiene aproximadamente 500 muestras de audio cuando están sin comprimir. Sin embargo, las funciones y macros de AVIFile tratan cada bloque de 256 bytes como un único ejemplo.

> [!Note]  
> Posiciones válidas dentro de un intervalo de flujo desde el principio hasta el final de la secuencia, que es la suma del punto inicial de la secuencia y su longitud. La posición representada por la suma de la posición inicial y la longitud corresponde a una hora después de que se hayan representado los últimos datos; no contiene ningún dato. Puede recuperar el número de muestra que representa el final de la secuencia con la macro [**AVIStreamEnd**](/windows/desktop/api/Vfw/nf-vfw-avistreamend) . Puede recuperar el valor de tiempo en milisegundos que representa el final de la secuencia mediante la macro [**AVIStreamEndTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamendtime) .

 

## <a name="finding-sample-and-key-frames"></a>Buscar fotogramas de ejemplo y clave

Puede buscar distintos tipos de ejemplos en una secuencia mediante la función [**AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample) . Esta función busca hacia atrás o hacia delante a través de una secuencia para obtener un ejemplo del tipo adecuado, empezando por el número de muestra que especifique. Puede buscar distintos tipos de ejemplos en una secuencia especificando una marca en la secuencia de llamada de **AVIStreamFindSample** . Especifique la \_ marca buscar cualquier para buscar ejemplos no vacíos o para omitir ejemplos que carecen de datos. Especifique la \_ marca buscar clave para buscar fotogramas clave que contengan los datos para representar una imagen completa sin necesidad de hacer referencia a fotogramas anteriores. Especifique la \_ marca buscar formato para buscar cambios en el formato. **AVIStreamFindSample** se usa principalmente con secuencias de vídeo.

Varias macros que usan funciones AVIFile complementan las características de búsqueda de secuencias. En la lista siguiente se proporciona una breve descripción de cada una de las macros. Las macros que buscan una posición o un tipo de datos específico requieren que se especifique una ubicación de inicio en la secuencia.



| Macro                                                                | Descripción                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**AVIStreamIsKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamiskeyframe)                   | Indica si un ejemplo de una secuencia especificada es un fotograma clave.                                                            |
| [**AVIStreamNearestKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframe)         | Busca el fotograma clave en la posición especificada o delante de ella en una secuencia.                                                     |
| [**AVIStreamNearestKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframetime) | Determina la hora correspondiente al principio del fotograma clave más cercano (a o anterior) de una hora especificada en un flujo. |
| [**AVIStreamNearestSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsample)             | Busca el ejemplo no vacío más próximo en o delante de una posición especificada de una secuencia.                                       |
| [**AVIStreamNearestSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsampletime)     | Determina la hora correspondiente al inicio de una muestra más cercana a un tiempo especificado en una secuencia.             |
| [**AVIStreamNextKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframe)               | Busca el siguiente fotograma clave después de una posición especificada en una secuencia.                                                      |
| [**AVIStreamNextKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframetime)       | Devuelve la hora del siguiente fotograma clave de una secuencia, comenzando en un momento dado.                                               |
| [**AVIStreamNextSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsample)                   | Busca el siguiente ejemplo no vacío de una posición especificada de una secuencia.                                                     |
| [**AVIStreamNextSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsampletime)           | Devuelve la hora en que un ejemplo cambia al siguiente ejemplo de la secuencia.                                                    |
| [**AVIStreamPrevKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframe)               | Busca el fotograma clave que precede a una posición especificada en una secuencia.                                                       |
| [**AVIStreamPrevKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframetime)       | Devuelve la hora del fotograma clave anterior en la secuencia, comenzando en un momento dado.                                         |
| [**AVIStreamPrevSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsample)                   | Busca el ejemplo no vacío que precede a una posición especificada en una secuencia.                                                 |
| [**AVIStreamPrevSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsampletime)           | Determina la hora a la que el ejemplo anterior reemplaza su predecesor en la secuencia.                                    |
| [**AVIStreamSampleToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletosample)           | Devuelve el ejemplo de un flujo que se produce al mismo tiempo que un ejemplo que se produce en una segunda secuencia.                     |



 

## <a name="switching-between-samples-and-time"></a>Cambiar entre muestras y hora

Puede determinar el tiempo transcurrido desde el inicio de una secuencia a un ejemplo mediante la función [**AVIStreamSampleToTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletotime) . Esta función convierte el número de muestra en un valor de hora expresado en milisegundos. En el caso de un fotograma de vídeo (que abarca varios milisegundos), este valor representa la hora a la que comienza la reproducción de la muestra desde que comenzó la reproducción y presupone que el clip de vídeo se reproduce a velocidad normal. Para un ejemplo de audio (que tiene varios ejemplos en milisegundos), el valor de hora corresponde a la hora a la que comienza la reproducción de la muestra y asume que la secuencia de audio se reproduce a velocidad normal.

Por el contrario, puede encontrar el número de ejemplo asociado a un valor de tiempo mediante la función [**AVIStreamTimeToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamtimetosample) . Esta función convierte el valor de milisegundos en un número de muestra y da por supuesto que el clip de vídeo se reproduce a velocidad normal.

Dado que **AVIStreamSampleToTime** devuelve la hora a la que comienza a reproducirse un fotograma, la relación entre **AVIStreamSampleToTime** y **AVIStreamTimeToSample** no es realmente inversa. Determinan la posición en un archivo más acurately de lo que determinan la hora. Por ejemplo, dos muestras de audio consecutivas pueden reproducirse en el mismo milisegundo. El uso de **AVIStreamSampleToTime** para convertir los números de ejemplo produciría valores de hora idénticos. Si vuelve a convertir el valor de tiempo a un número de ejemplo mediante **AVIStreamTimeToSample**, se hará referencia a una sola muestra.

 

 




