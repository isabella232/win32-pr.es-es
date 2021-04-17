---
title: Configuración de secuencias de audio
description: Configuración de secuencias de audio
ms.assetid: 6ddd9bc1-3fde-4098-afce-fdda461ced62
keywords:
- flujos, configurar secuencias de audio
- códecs, configurar secuencias de audio
- secuencias de audio, configurar
- códecs, formatos
- streams, interfaz IWMCodecInfo
- IWMCodecInfo, secuencias de audio
- flujos, sincronización A/V
- secuencias de audio, sincronización A/V
- Sincronización A/V
- flujos, sincronizar A/V
- secuencias de audio, sincronizar A/V
- flujos y formatos de audio de retraso reducido
- secuencias de audio, formatos de audio de retraso reducido
- códecs, formatos de audio de retraso reducido
- secuencias, velocidad de bits variable (VBR)
- secuencias de audio, velocidad de bits variable (VBR)
- códecs, velocidad de bits variable (VBR)
- velocidad de bits variable (VBR), configurar
- VBR (velocidad de bits variable), configurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad3931ec41e73c125417d39cdd177dc16056e9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714423"
---
# <a name="configuring-audio-streams"></a>Configuración de secuencias de audio

Los flujos de audio suelen ser más fáciles de configurar. Obtenga una configuración de flujo del códec con los métodos de [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo) tal y como se describe en [obtener información de configuración de la secuencia de los códecs](getting-stream-configuration-information-from-codecs.md). En la mayoría de los casos, no debe modificar la configuración de los recuperados.

El formato de códec que seleccione de entre los enumerados depende del uso previsto de los archivos ASF realizados con el perfil. La descripción del formato de códec recuperada por [**IWMCodecInfo2:: GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc) resume las características del formato. Si la aplicación no muestra las descripciones para elegir entre ellas, puede llamar a **QueryInterface** en la interfaz [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) del formato de códec para obtener la interfaz [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) . Después, puede recuperar la estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) llamando a [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Mediante el examen de la estructura de **\_ \_ tipo de medio de WM** y la estructura [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) a la que apunta, puede determinar la configuración del formato de códec y compararla con sus requisitos.

## <a name="getting-audio-formats-for-av-synchronization"></a>Obtener formatos de audio para una sincronización de/V

Los códecs Windows Media Audio y Windows Media Audio Professional admiten formatos para archivos de solo audio y para archivos de audio/vídeo. Los formatos de solo audio están optimizados para archivos que solo contienen datos de audio, mientras que los formatos de audio y vídeo están optimizados para el audio que se encuentra en un archivo con una secuencia de vídeo. Al enumerar los formatos de códec de estos códecs, los formatos de audio y vídeo aparecen después de los formatos de solo audio. Todas las descripciones de formato de audio y vídeo contienen la cadena "(A/V)". Puede identificar los formatos diseñados para la sincronización de audio y vídeo mediante programación comprobando el número de paquetes por segundo. Los formatos de sincronización tienen 5 o más paquetes por segundo si la velocidad de bits es mayor o igual que 32.000 bits por segundo. Los formatos con velocidades de bits inferiores a 32.000 bits por segundo se pueden usar con el vídeo sincronizado si usan 3 o más paquetes por segundo. El ejemplo de código del tema [para buscar formatos de audio](to-find-audio-formats.md) contiene el código necesario para realizar esta comprobación:


```C++
if((pWave->nAvgBytesPerSec / pWave->nBlockAlign) >= 
       ((pWave->nAvgBytesPerSec >= 4000) ? 5.0 : 3.0))
{
    // Set this stream configuration as the new best match.
}
```



## <a name="getting-low-delay-audio-formats"></a>Obtener Low-Delay formatos de audio

El códec de Windows Media 9,1 y el códec profesional de Windows Media Audio 9,1 admiten formatos de retraso bajo. Estos formatos tienen una ventana de búfer más pequeña que otros formatos de audio. El audio con retraso bajo está diseñado para mejorar el rendimiento en escenarios donde los archivos o secuencias se cambiarán con frecuencia; por ejemplo, una aplicación que muestra varias canciones para la transmisión por secuencias en la interfaz de usuario y permite a los usuarios cambiar arbitrariamente entre ellas.

Los formatos de retraso bajo solo están disponibles en el modo CBR (una o dos pases). Todas las descripciones de formato de retraso bajo contienen la cadena "Low Delay". Puede identificar los formatos mediante programación comprobando el valor de la velocidad de bits del formato. A los formatos de retraso bajo se les asignan velocidades de bits que son de 1 Kilobit menos que las velocidades de bits del formato normal equivalente. Por ejemplo, el códec Windows Media Audio 9,1 admite un formato CBR de un solo paso con una velocidad de bits de 192 kbps. El formato de retraso bajo equivalente tiene una velocidad de bits de 191 kbps. Además, con la excepción del formato mono de 5 Kbps compatible con el códec Windows Media Audio 9,1, los formatos de retraso bajo son los únicos formatos que tienen un valor de velocidad de bits impar.

## <a name="configuring-variable-bit-rate-audio"></a>Configuración de audio de velocidad de bits variable

Si necesita un formato de velocidad de bits variable (VBR) para uno de los códecs de audio de Windows Media, puede obtenerlo estableciendo la configuración de enumeración en el método [**IWMCodecInfo3:: SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) . Establezca g \_ wszVBREnabled en true y establezca g \_ wszNumPasses en 1 para VBR basada en la calidad o 2 para VBR de dos pasos (restringido o sin restricciones). Si usa VBR de dos pasos restringida, debe establecer manualmente la velocidad de bits máxima y la ventana de búfer para la secuencia mediante los métodos de [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) tal como se describe en [configuración de secuencias vbrs](configuring-vbr-streams.md).

En los perfiles VBR basados en la calidad, el miembro **nAvgBytesPerSec** de la estructura **WAVEFORMATEX** contiene el nivel de calidad (del 1 al 100) en el byte de orden inferior y los tres bytes de orden superior se establecen en 0x7fffff. No intente modificar la configuración de calidad modificando este valor manualmente. debe usar el formato que se recupera del códec. Para usar un valor de calidad diferente, debe enumerar los formatos hasta encontrar uno que satisfaga sus necesidades. Además, **nAvgBytesPerSec** no se conservará en el archivo ASF; Cuando se obtiene la estructura **WAVEFORMATEX** de un archivo que se ha abierto con el objeto Reader, **nAvgBytesPerSec** contiene un valor aproximado que representa el número promedio de bytes por segundo.

> [!Note]  
> Al configurar secuencias de audio, nunca debe tener un valor de ventana de búfer de audio mayor que el valor de las secuencias de vídeo del archivo. Normalmente esto no es un problema, ya que los valores de la ventana de búfer de audio deben oscilar entre 1,5 y 3 segundos, y los valores de vídeo deben oscilar entre 3 y 5 segundos. Si una ventana de búfer de audio es mayor que una ventana de búfer de vídeo, el archivo se reproducirá con las secuencias ligeramente fuera de sincronización.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración común para todos los flujos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuración de secuencias**](configuring-streams.md)
</dt> <dt>

[**Para buscar formatos de audio**](to-find-audio-formats.md)
</dt> </dl>

 

 