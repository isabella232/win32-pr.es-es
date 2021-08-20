---
title: Configuración de audio Secuencias
description: Configuración de audio Secuencias
ms.assetid: 6ddd9bc1-3fde-4098-afce-fdda461ced62
keywords:
- streams,configuring audio streams
- códecs, configuración de secuencias de audio
- secuencias de audio, configurar
- códecs, formatos
- streams,IWMCodecInfo (interfaz)
- IWMCodecInfo,secuencias de audio
- flujos, sincronización de A/V
- secuencias de audio, sincronización de A/V
- Sincronización de A/V
- streams,synchronizing A/V
- secuencias de audio, sincronización de A/V
- secuencias, formatos de audio de bajo retraso
- secuencias de audio, formatos de audio de bajo retraso
- códecs, formatos de audio de bajo retraso
- streams,variable bit rate (VBR)
- secuencias de audio, velocidad de bits variable (VBR)
- códecs, velocidad de bits variable (VBR)
- velocidad de bits variable (VBR), configuración
- VBR (velocidad de bits variable),configurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e28c32e9d0e237e72f693bded74c7620d33845261a6137afdf58b04f35f441f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548043"
---
# <a name="configuring-audio-streams"></a>Configuración de audio Secuencias

Las secuencias de audio suelen ser las más sencillas de configurar. Obtenga una configuración de secuencia del códec mediante los métodos de [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo) como se describe en Obtención de información de configuración de [secuencias de códecs](getting-stream-configuration-information-from-codecs.md). En la mayoría de los casos, no debe modificar la configuración de las recuperadas.

El formato de códec que seleccione entre los enumerados depende del uso previsto de los archivos ASF realizados con el perfil. La descripción del formato de códec recuperada por [**IWMCodecInfo2::GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc) resume las características del formato. Si la aplicación no muestra las descripciones para elegir entre ellas, puede llamar a **QueryInterface** en la interfaz [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) del formato de códec para obtener la [**interfaz IWMMediaProps.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) A continuación, puede recuperar la [**estructura WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) llamando a [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Al examinar la estructura **WM \_ MEDIA \_ TYPE** y la estructura [**MPEGATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) a la que apunta, puede determinar la configuración del formato de códec y compararla con sus requisitos.

## <a name="getting-audio-formats-for-av-synchronization"></a>Obtención de formatos de audio para la sincronización de A/V

El códec Windows Media Audio y el códec Windows Media Audio Professional admiten tanto formatos para archivos de solo audio como para archivos de audio y vídeo. Los formatos de solo audio están optimizados para archivos que contienen solo datos de audio, mientras que los formatos de audio y vídeo están optimizados para el audio que se encuentra en un archivo con una secuencia de vídeo. Al enumerar formatos de códec para estos códecs, los formatos de audio y vídeo vienen después de los formatos de solo audio. Todas las descripciones de formato de audio/vídeo contienen la cadena "(A/V)". Puede identificar los formatos diseñados para la sincronización de audio y vídeo mediante programación comprobando el número de paquetes por segundo. Los formatos de sincronización tienen 5 o más paquetes por segundo si la velocidad de bits es mayor o igual que 32 000 bits por segundo. Los formatos con velocidades de bits inferiores a 32 000 bits por segundo se pueden usar con vídeo sincronizado si usan 3 o más paquetes por segundo. El ejemplo de código del tema [Para buscar formatos de audio](to-find-audio-formats.md) contiene el código necesario para realizar esta comprobación:


```C++
if((pWave->nAvgBytesPerSec / pWave->nBlockAlign) >= 
       ((pWave->nAvgBytesPerSec >= 4000) ? 5.0 : 3.0))
{
    // Set this stream configuration as the new best match.
}
```



## <a name="getting-low-delay-audio-formats"></a>Obtención Low-Delay formatos de audio

El códec Windows Media 9.1 y el códec Windows Media Audio 9.1 de Professional admiten formatos de retraso bajo. Estos formatos tienen una ventana de búfer más pequeña que otros formatos de audio. El audio de bajo retraso está pensado para mejorar el rendimiento en escenarios en los que los archivos o secuencias se cambiarán con frecuencia. por ejemplo, una aplicación que enumera una serie de canciones para streaming en la interfaz de usuario y permite a los usuarios cambiar arbitrariamente entre ellas.

Los formatos de retraso bajo solo están disponibles en el modo CBR (un paso o dos pases). Todas las descripciones de formato de retraso bajo contienen la cadena "Retraso bajo". Puede identificar los formatos mediante programación comprobando el valor de velocidad de bits del formato. A los formatos de retraso bajo se les asignan velocidades de bits de 1 kilobit inferiores a las velocidades de bits del formato normal equivalente. Por ejemplo, el códec Windows Media Audio 9.1 admite un formato CBR de un solo paso con una velocidad de bits de 192 kbps. El formato de retraso bajo equivalente tiene una velocidad de bits de 191 kbps. Además, a excepción del formato mono de 5 kbps admitido por el códec Windows Media Audio 9.1, los formatos de retraso bajo son los únicos que tienen un valor de velocidad de bits impar.

## <a name="configuring-variable-bit-rate-audio"></a>Configuración del audio de velocidad de bits variable

Si necesita un formato de velocidad de bits variable (VBR) para uno de los códecs de audio multimedia de Windows, puede obtenerlo estableciendo la configuración de enumeración en el método [**IWMCodecInfo3::SetCodecEnumerationSetting.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) Establezca g \_ wszVBREnabled en True y g wszNumPasses en 1 para VBR basado en calidad o 2 para VBR de dos pases (restringido o sin \_ restricciones). Si usa VBR de dos pasos restringido, debe establecer manualmente la velocidad de bits máxima y la ventana de búfer para la secuencia mediante los métodos de [**IWMPropertyVault,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) como se describe en Configuración de [VBR Secuencias](configuring-vbr-streams.md).

En los perfiles de VBR basados en calidad, el miembro **nAvgBytesPerSec** de la estructura **DEDATOX** contiene el nivel de calidad (del 1 al 100) en el byte de orden bajo y los tres bytes de orden alto se establecen en 0x7fffff. No intente modificar la configuración de calidad modificando este valor manualmente; debe usar el formato a medida que se recupera del códec. Para usar un valor de calidad diferente, debe enumerar los formatos hasta que encuentre uno que satisfaga sus necesidades. Además, **nAvgBytesPerSec** no se conservará en el archivo ASF; cuando se obtiene la estructura **DESATEX** para un archivo que se ha abierto con el objeto de lector, **nAvgBytesPerSec** contiene un valor aproximado que representa el número medio de bytes por segundo.

> [!Note]  
> Al configurar secuencias de audio, nunca debe tener un valor de ventana de búfer de audio mayor que el valor de las secuencias de vídeo del archivo. Normalmente esto no es un problema, ya que los valores de la ventana del búfer de audio deben oscilar entre 1,5 y 3 segundos y los valores de vídeo deben oscilar entre 3 y 5 segundos. Si una ventana de búfer de audio es mayor que una ventana de búfer de vídeo, el archivo se reproducirá con las secuencias ligeramente fuera de sincronización.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración común a todas las Secuencias**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuración de Secuencias**](configuring-streams.md)
</dt> <dt>

[**Para buscar formatos de audio**](to-find-audio-formats.md)
</dt> </dl>

 

 