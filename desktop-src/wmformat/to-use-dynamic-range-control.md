---
title: Para usar el control de intervalo dinámico
description: Para usar el control de intervalo dinámico
ms.assetid: 719658c1-952f-4e8f-a3ea-bdf89a0a7268
keywords:
- Windows SDK de formato multimedia, control de intervalo dinámico
- Windows SDK de formato multimedia, Windows códec de Professional Media Audio 9
- Windows SDK de formato multimedia, Windows códec sin pérdida de audio multimedia 9
- Advanced Systems Format (ASF),Windows Media Audio 9 Professional codec
- ASF (formato de sistemas avanzados),Windows media audio 9 Professional códec
- Formato de sistemas avanzados (ASF), Windows códec sin pérdida de audio multimedia 9
- ASF (formato de sistemas avanzados), Windows códec sin pérdida de audio multimedia 9
- Formato de sistemas avanzados (ASF), control de intervalo dinámico
- ASF (formato de sistemas avanzados), control de intervalo dinámico
- control de intervalo dinámico
- códecs, Windows códec sin pérdida de audio multimedia 9
- códecs,Windows códec de audio multimedia 9 Professional códec
- Windows Códec sin pérdida de audio multimedia 9, control de intervalo dinámico
- Windows Códec de Professional audio multimedia 9, control de intervalo dinámico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 077ebc0052d0154aec395f371a5c2dc3ffd46c67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266932"
---
# <a name="to-use-dynamic-range-control"></a>Para usar el control de intervalo dinámico

El intervalo dinámico de un fragmento de contenido de audio es básicamente la diferencia entre el volumen más bajo y el máximo. Si el intervalo dinámico del contenido es demasiado alto, es posible que los usuarios se encuentren ajustando el volumen repetidamente durante la reproducción. Por ejemplo, las películas suelen tener un intervalo dinámico alto. A menudo, cuando el volumen se ajusta para que el diálogo se pueda entender durante escenas silenciosas, otras partes de la película con música o efectos de sonido son más fuertes de lo deseado.

Los códecs Windows Media Audio 9 Professional y Windows Media Audio 9 sin pérdida admiten una característica denominada control de intervalo dinámico. En el momento de la codificación, el códec calcula los valores de amplitud máxima y media del contenido, y el objeto de escritor almacena estos valores en los metadatos de la secuencia cuando finaliza la codificación. Opcionalmente, una aplicación también puede escribir valores de "destino" como metadatos que las aplicaciones de reproductor y el descodificador pueden usar como sugerencias al reproducir el archivo. En el momento de la reproducción, una aplicación puede especificar el nivel de control de intervalo dinámico que se va a aplicar a la secuencia de audio.

Reproductor de Windows Media el control de intervalo dinámico como la característica Modo silencioso.

## <a name="when-to-use-dynamic-range-control"></a>Cuándo usar el control de intervalo dinámico

El control de intervalo dinámico puede modificar el sonido del contenido. Por ese motivo, no debe configurar la aplicación para que use automáticamente el control de intervalo dinámico. En su lugar, proporcione a los usuarios la capacidad de activar o desactivar el control de intervalo dinámico según sea necesario.

## <a name="using-dynamic-range-control"></a>Uso del control de intervalo dinámico

En el momento de la reproducción, el control de intervalo dinámico se activa mediante la configuración de salida g \_ wszDynamicRangeControl. Use [**IWMReaderAdvanced2::SetOutputSetting para**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) configurar la configuración. Un valor de cero (valor predeterminado) indica que no se debe modificar el intervalo dinámico. Un valor de 1 o 2 indica al códec que realice el control de intervalo dinámico, donde 1 es un nivel moderado de compresión de intervalo dinámico y 2 es un alto nivel de compresión de intervalo dinámico.

En tiempo de codificación o de reproducción, puede proporcionar los valores PCM de destino del códec para los niveles máximo y medio estableciendo los atributos [**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md) y [**WM/WMADRCAverageTarget,**](wm-wmadrcaveragetarget.md) respectivamente. Estos valores se almacenan como atributos de metadatos y se debe tener acceso a ellos mediante los métodos de la [**interfaz IWMHeaderInfo3.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) Al codificar una secuencia de audio mediante el códec profesional o sin pérdida, los atributos [**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md) y [**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md) se establecen automáticamente en los niveles máximo y medio del contenido original. Los valores de destino se establecen en los mismos valores que las referencias de forma predeterminada.

El descodificador en tiempo de reproducción calcula el intervalo dinámico en función del nivel seleccionado de control de intervalo dinámico y los valores de destino (si se especifica alguno). Los intervalos posibles se muestran en la tabla siguiente.



| Configuración                                                                | Intervalo de audio entregado                                                                                                     |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszDynamicRangeControl = 0 (cualquier valor de destino)                       | El mismo intervalo que el contenido original.                                                                                          |
| g \_ wszDynamicRangeControl = 1 (valores de destino iguales a los valores de referencia) | Se mantiene el nivel medio y los picos se limitan al promedio +12 dB.                                                    |
| g \_ wszDynamicRangeControl = 2 (valores de destino iguales a los valores de referencia) | Se mantiene el nivel medio y los picos se limitan al promedio +6 dB.                                                     |
| g \_ wszDynamicRangeControl = 1 (valores de destino especificados)                 | Nivel medio establecido en el valor medio de destino y picos limitados al valor máximo de destino.                                   |
| g \_ wszDynamicRangeControl = 2 (valores de destino especificados)                 | Nivel medio establecido en el valor medio de destino y picos limitados a la mediana de los valores de promedio de destino y máximo de destino. |



 

Tenga en cuenta que el control de intervalo dinámico es una característica de lacoding solo y solo existe como metadatos en el propio archivo. Esta configuración no tiene ningún efecto en el contenido almacenado en el archivo a menos que indique específicamente al descodificador que los use. El SDK Windows media format no proporciona ningún método para modificar el intervalo dinámico de los datos de audio en tiempo de codificación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Temas avanzados**](advanced-topics.md)
</dt> </dl>

 

 




