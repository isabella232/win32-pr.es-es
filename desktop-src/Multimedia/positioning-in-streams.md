---
title: Posicionamiento en Secuencias
description: Posicionamiento en Secuencias
ms.assetid: 97ab491d-1a58-4b4b-a13a-215be24dac1c
keywords:
- Función AVIStreamStart
- Función AVIStreamFindSample
- Función AVIStreamSampleToTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0528fea9ea10e28a418d253bd1abe6c599a952fe95a8c8f6c86807abe0e41159
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805865"
---
# <a name="positioning-in-streams"></a>Posicionamiento en Secuencias

AVIFile proporciona varias maneras de buscar y mover a una posición en un flujo de datos. Las funciones y macros de esta sección permiten a la aplicación encontrar la posición inicial, la longitud y los fotogramas clave (que contienen una imagen completa en el ejemplo) dentro de una secuencia. Las funciones y macros también asocian el tiempo con las posiciones de una secuencia calculando el tiempo transcurrido necesario para reproducir una secuencia desde su principio hasta cualquier punto de una secuencia.

## <a name="finding-the-starting-position"></a>Buscar la posición inicial

Puede recuperar el número de ejemplo del primer fotograma de una secuencia de vídeo mediante la [**función AVIStreamStart.**](/windows/desktop/api/Vfw/nf-vfw-avistreamstart) (Los fotogramas de una película pueden comenzar en el ejemplo 0 o 1, dependiendo de la preferencia del autor). También puede obtener esta información mediante la [**función AVIStreamInfo.**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) Esta función almacena el número de ejemplo en el **miembro dwStart** de la [**estructura AVISTREAMINFO.**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) Puede recuperar la hora de inicio del primer ejemplo de una secuencia mediante la [**macro AVIStreamStartTime.**](/windows/desktop/api/Vfw/nf-vfw-avistreamstarttime)

Puede recuperar la longitud del flujo mediante la [**función AVIStreamLength.**](/windows/desktop/api/Vfw/nf-vfw-avistreamlength) Esta función devuelve el número de muestras de la secuencia. También puede obtener esta información mediante la **función AVIStreamInfo.** Esta función almacena la longitud del flujo en el **miembro dwLength** de la **estructura AVISTREAMINFO.** Para recuperar la longitud de una secuencia en milisegundos, use la [**macro AVIStreamLengthTime.**](/windows/desktop/api/Vfw/nf-vfw-avistreamlengthtime)

En una secuencia de vídeo, cada ejemplo suele corresponder a un fotograma de vídeo. Sin embargo, puede haber ejemplos para los que no haya datos de vídeo. Si llama a la [**función AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) especificando una de esas posiciones, devuelve una longitud de datos de 0 bytes. Puede encontrar ejemplos que contengan datos mediante la [**función AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample) y especificando la marca FIND \_ ANY.

En una secuencia de audio, cada muestra corresponde a un bloque de datos de datos de audio. Por ejemplo, si los datos de audio tienen un formato ADPCM de 22 kHz (compresión de código de pulso diferencial adaptable), cada muestra de **AVIStreamLength** corresponde a un bloque de 256 bytes de datos de audio comprimidos. Este bloque de datos de audio contiene aproximadamente 500 muestras de audio cuando se descomprimen. Sin embargo, las funciones y macros de AVIFile tratan cada bloque de 256 bytes como una sola muestra.

> [!Note]  
> Las posiciones válidas dentro de un flujo van desde el principio hasta el final de la secuencia, que es la suma del punto inicial de la secuencia y su longitud. La posición representada por la suma de la posición inicial y la longitud corresponde a una hora después de que se hayan representado los últimos datos; no contiene ningún dato. Puede recuperar el número de ejemplo que representa el final de la secuencia mediante la [**macro AVIStreamEnd.**](/windows/desktop/api/Vfw/nf-vfw-avistreamend) Puede recuperar el valor de tiempo en milisegundos que representa el final de la secuencia mediante la macro [**AVIStreamEndTime.**](/windows/desktop/api/Vfw/nf-vfw-avistreamendtime)

 

## <a name="finding-sample-and-key-frames"></a>Buscar fotogramas clave y de ejemplo

Puede buscar diferentes tipos de ejemplos en una secuencia mediante la [**función AVIStreamFindSample.**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample) Esta función busca hacia atrás o hacia delante a través de una secuencia una muestra del tipo adecuado, empezando por el número de muestra que especifique. Puede buscar diferentes tipos de ejemplos en una secuencia especificando una marca en la secuencia de llamada **AVIStreamFindSample.** Especifique la marca FIND ANY para buscar muestras que no están en \_ deserción o para omitir las muestras que carecen de datos. Especifique la marca FIND KEY para buscar fotogramas clave que contengan los datos para representar una imagen completa sin necesidad de hacer \_ referencia a fotogramas anteriores. Especifique la marca FIND \_ FORMAT para buscar cambios en el formato. **AVIStreamFindSample** se usa principalmente con secuencias de vídeo.

Varias macros que usan funciones AVIFile complementan las características de búsqueda de secuencias. En la lista siguiente se proporciona una breve descripción de cada macro. Las macros que buscan una posición o un tipo de datos específicos requieren que se especifique una ubicación inicial en la secuencia.



| Macro                                                                | Descripción                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**AVIStreamIsKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamiskeyframe)                   | Indica si una muestra de una secuencia especificada es un fotograma clave.                                                            |
| [**AVIStreamNearestKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframe)         | Busca el fotograma clave en o antes de una posición especificada en una secuencia.                                                     |
| [**AVIStreamNearestKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframetime) | Determina la hora correspondiente al principio del fotograma clave más cercano (en o anterior) a una hora especificada en una secuencia. |
| [**AVIStreamNearestSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsample)             | Busca la muestra nompty más cercana en o antes de una posición especificada en una secuencia.                                       |
| [**AVIStreamNearestSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsampletime)     | Determina la hora correspondiente al principio de una muestra más cercana a una hora especificada en una secuencia.             |
| [**AVIStreamNextKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframe)               | Busca el siguiente fotograma clave después de una posición especificada en una secuencia.                                                      |
| [**AVIStreamNextKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframetime)       | Devuelve la hora del siguiente fotograma clave de una secuencia, empezando en un momento dado.                                               |
| [**AVIStreamNextSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsample)                   | Busca la siguiente muestra nompty de una posición especificada en una secuencia.                                                     |
| [**AVIStreamNextSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsampletime)           | Devuelve la hora a la que un ejemplo cambia al ejemplo siguiente de la secuencia.                                                    |
| [**AVIStreamPrevKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframe)               | Busca el fotograma clave que precede a una posición especificada en una secuencia.                                                       |
| [**AVIStreamPrevKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframetime)       | Devuelve la hora del fotograma clave anterior en la secuencia, empezando en un momento dado.                                         |
| [**AVIStreamPrevSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsample)                   | Busca el ejemplo inexociable que precede a una posición especificada en una secuencia.                                                 |
| [**AVIStreamPrevSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsampletime)           | Determina la hora a la que el ejemplo anterior reemplaza a su predecesor en la secuencia.                                    |
| [**AVIStreamSampleToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletosample)           | Devuelve el ejemplo de una secuencia que se produce al mismo tiempo que una muestra que se produce en una segunda secuencia.                     |



 

## <a name="switching-between-samples-and-time"></a>Cambiar entre muestras y hora

Puede determinar el tiempo transcurrido desde el principio de una secuencia a un ejemplo mediante la [**función AVIStreamSampleToTime.**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletotime) Esta función convierte el número de muestra en un valor de tiempo expresado en milisegundos. Para un fotograma de vídeo (que abarca varios milisegundos), este valor representa el momento en que la muestra comienza a reproducirse desde que comenzó la reproducción y supone que el clip de vídeo se reproduce a velocidad normal. En el caso de una muestra de audio (que tiene varias muestras en milisegundos), el valor de tiempo corresponde a la hora a la que la muestra comienza a reproducirse y asume que la secuencia de audio se reproduce a velocidad normal.

Por el contrario, puede encontrar el número de muestra asociado a un valor de hora mediante la [**función AVIStreamTimeToSample.**](/windows/desktop/api/Vfw/nf-vfw-avistreamtimetosample) Esta función convierte el valor de milisegundos en un número de muestra y supone que el clip de vídeo se reproduce a velocidad normal.

Dado **que AVIStreamSampleToTime** devuelve la hora a la que comienza a reproducirse un fotograma, la relación entre **AVIStreamSampleToTime** y **AVIStreamTimeToSample** no es realmente inversa. Determinan la posición de un archivo de forma más acuso que la hora. Por ejemplo, dos muestras de audio consecutivas podrían reproducirse en el mismo milisegundo. El **uso de AVIStreamSampleToTime para** convertir los números de ejemplo daría como resultado valores de tiempo idénticos. Si vuelve a convertir el valor de tiempo en un número de muestra mediante **AVIStreamTimeToSample,** se hace referencia a una sola muestra.

 

 




