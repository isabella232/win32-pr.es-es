---
title: Para usar el control de intervalo dinámico
description: Para usar el control de intervalo dinámico
ms.assetid: 719658c1-952f-4e8f-a3ea-bdf89a0a7268
keywords:
- Windows Media Format SDK, control de intervalo dinámico
- Windows Media Format SDK, Windows Media Audio 9 Professional Codec
- Códec de Windows Media Format SDK, Windows Media Audio 9 Lossless
- Códec Advanced Systems Format (ASF), Windows Media Audio 9 Professional Codec
- ASF (formato de sistemas avanzados), códec de Windows Media Audio 9 Professional
- Códecs Advanced Systems Format (ASF), Windows Media Audio 9 Lossless
- ASF (formato de sistemas avanzados), códec de Windows Media Audio 9 sin pérdida de
- Advanced Systems Format (ASF), control de intervalo dinámico
- ASF (formato de sistemas avanzados), control de intervalo dinámico
- control de intervalo dinámico
- códecs, códec de Windows Media Audio 9 sin pérdida de
- códecs, códec de Windows Media Audio 9 Professional
- Códec sin pérdida de Windows Media Audio 9, control de intervalo dinámico
- Códec de Windows Media Audio 9 Professional, control de intervalo dinámico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 077ebc0052d0154aec395f371a5c2dc3ffd46c67
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695536"
---
# <a name="to-use-dynamic-range-control"></a>Para usar el control de intervalo dinámico

El intervalo dinámico de un fragmento de contenido de audio es básicamente la diferencia entre el volumen más bajo y el volumen máximo. Si el intervalo dinámico del contenido es demasiado alto, los usuarios pueden ajustar el volumen varias veces durante la reproducción. Por ejemplo, las películas suelen tener un intervalo dinámico alto. A menudo, cuando se ajusta el volumen para que se pueda entender el cuadro de diálogo durante las escenas tranquilas, otras partes de la película con música o efectos sonoros son más fuertes que las deseadas.

Los códecs de Windows Media Audio 9 Professional y Windows Media Audio 9 Lossless admiten una característica denominada control de intervalo dinámico. En el momento de la codificación, el códec calcula los valores de amplitud máximo y promedio del contenido, y el objeto de escritor almacena estos valores en los metadatos de la secuencia cuando finaliza la codificación. Opcionalmente, una aplicación también puede escribir valores de "destino" como metadatos que las aplicaciones del reproductor y el descodificador pueden usar como sugerencias al reproducir el archivo. En el momento de la reproducción, una aplicación puede especificar el nivel de control de intervalo dinámico que se va a aplicar a la secuencia de audio.

Windows Media Player implementa el control de intervalo dinámico como característica de modo silencioso.

## <a name="when-to-use-dynamic-range-control"></a>Cuándo usar el control de intervalo dinámico

El control de intervalo dinámico puede alterar el sonido del contenido. Por ese motivo, no debe configurar la aplicación para que use el control de intervalo dinámico automáticamente. En su lugar, proporcione a los usuarios la capacidad de activar o desactivar el control de intervalo dinámico según sea necesario.

## <a name="using-dynamic-range-control"></a>Usar el control de intervalo dinámico

En el momento de la reproducción, el control de intervalo dinámico se activa con la configuración de salida g \_ wszDynamicRangeControl. Use [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) para configurar el valor. Un valor de cero (valor predeterminado) indica que el intervalo dinámico no debe modificarse. Un valor de 1 o 2 indica al códec que realice un control de intervalo dinámico, donde 1 es un nivel moderado de compresión de intervalo dinámico y 2 es un alto nivel de compresión de intervalo dinámico.

En el momento de la codificación o en el tiempo de reproducción, puede asignar los valores PCM de destino del códec para los niveles máximo y medio mediante la configuración de los atributos [**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md) y [**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md) , respectivamente. Estos valores se almacenan como atributos de metadatos y se debe tener acceso a ellos mediante los métodos de la interfaz [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) . Al codificar una secuencia de audio con el códec profesional o Lossless, los atributos [**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md) y [**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md) se establecen automáticamente en los niveles máximo y medio del contenido original. Los valores de destino se establecen en los mismos valores que las referencias de forma predeterminada.

El descodificador en el momento de la reproducción calcula el intervalo dinámico según el nivel seleccionado de control de intervalo dinámico y los valores de destino (si se especifica alguno). Los intervalos posibles se muestran en la tabla siguiente.



| Configuración                                                                | Intervalo de audio entregado                                                                                                     |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszDynamicRangeControl = 0 (cualquier valor de destino)                       | Mismo intervalo que el contenido original.                                                                                          |
| g \_ wszDynamicRangeControl = 1 (valores de destino iguales a los valores de referencia) | El nivel promedio se mantiene y los picos se limitan al promedio de + 12 dB.                                                    |
| g \_ wszDynamicRangeControl = 2 (valores de destino iguales a los valores de referencia) | El nivel promedio se mantiene y los picos se limitan al promedio de + 6 dB.                                                     |
| g \_ wszDynamicRangeControl = 1 (valores de destino especificados)                 | Nivel promedio establecido en el valor medio de destino y los picos limitados al valor máximo de destino.                                   |
| g \_ wszDynamicRangeControl = 2 (valores de destino especificados)                 | Nivel promedio establecido en el valor medio de destino y los picos limitados a la mediana del promedio de destino y los valores de pico de destino. |



 

Tenga en cuenta que el control de intervalo dinámico es una característica de descodificación únicamente y solo existe como metadatos en el propio archivo. Esta configuración no tiene ningún efecto en el contenido almacenado en el archivo a menos que indique específicamente al descodificador que las use. El SDK de Windows Media Format no proporciona métodos para modificar el intervalo dinámico de los datos de audio en el momento de la codificación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Temas avanzados**](advanced-topics.md)
</dt> </dl>

 

 




