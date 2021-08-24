---
title: Configuración de video Secuencias
description: Configuración de video Secuencias
ms.assetid: caffdfc1-3c35-4b7b-8643-5a9095cc11f6
keywords:
- streams,configuring video streams
- códecs, configuración de secuencias de vídeo
- secuencias de vídeo, configurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22bc6e011f32d1ea9a9905c718ad8ff0c13f7d57650a30316ecfec6332978fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809595"
---
# <a name="configuring-video-streams"></a>Configuración de video Secuencias

Las secuencias de vídeo son más flexibles en su configuración que las secuencias de audio. Esto se debe a que las propiedades de los fotogramas que forma el vídeo pueden variar ampliamente de un archivo al siguiente. Al recuperar el formato de códec para el códec que está usando, debe establecer los siguientes valores para los objetos de configuración de secuencias de vídeo.



| Valor                                 | Descripción                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Velocidad de bits                              | Llame [**a IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) para establecer en el valor deseado. El códec de vídeo intentará comprimir los medios para satisfacer sus especificaciones. Si los valores son demasiado bajos, el vídeo comprimido resultante estará muy degradado.           |
| Ventana búfer                         | Llame [**a IWMStreamConfig::SetBufferWindow para**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) establecer en el valor deseado. El códec de vídeo intentará comprimir los medios para satisfacer sus especificaciones. Si los valores son demasiado bajos, el vídeo comprimido resultante estará muy degradado. |
| **WMVIDEOINFOHEADER.rcSource**        | La esquina superior izquierda debe establecerse en 0,0. La esquina inferior derecha debe establecerse en las dimensiones del marco. Por ejemplo, en una secuencia de 640 x 480, esta configuración sería 0,0,640,480.                                                                                                |
| **WMVIDEOINFOHEADER.rcTarget**        | Debe coincidir **con rcSource**.                                                                                                                                                                                                                                                    |
| **WMVIDEOINFOHEADER.dwBitRate**       | Debe coincidir con el conjunto de velocidad de bits de la secuencia.                                                                                                                                                                                                                                 |
| **WMVIDEOINFOHEADER. AvgTimePerFrame** | Establezca en el tiempo aproximado por fotograma.                                                                                                                                                                                                                                      |
| **BITMAPINFOHEADER.biWidth**          | Establezca en el ancho, en píxeles, del tamaño del marco deseado.                                                                                                                                                                                                                     |
| **BITMAPINFOHEADER.biHeight**         | Establezca en el alto, en píxeles, del tamaño del marco deseado.                                                                                                                                                                                                                    |



 

El contenido de vídeo no se reproduce correctamente a menos que esté codificado en un tamaño que sea un múltiplo de cuatro para ancho y alto. La excepción [*es el vídeo RGB*](wmformat-glossary.md) sin comprimir, que puede tener cualquier tamaño. Si intenta establecer un tamaño que no es un múltiplo de cuatro, el escritor devolverá uno de los siguientes errores:

-   NS \_ E FORMATO DE ENTRADA NO \_ \_ \_ VÁLIDO
-   NS \_ E FORMATO DE SALIDA NO \_ \_ \_ VÁLIDO
-   NS \_ E \_ INVALIDPROFILE

Si usa la codificación de velocidad de bits variable, es posible que tenga que realizar otros ajustes. Para obtener más información, [vea Configuring VBR Secuencias](configuring-vbr-streams.md).

Algunos códecs Windows Media Video admiten varios niveles de complejidad. Los niveles de complejidad determinan los algoritmos que usará el códec al codificar una secuencia de vídeo. El uso de un nivel de complejidad alto requerirá más capacidad de procesamiento para codificar y codificar.

Cada códec que admite la configuración de complejidad expone la siguiente configuración que puede recuperar con el método [**IWMCodecInfo3::GetCodecProp.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop)



| Configuración                 | Descripción                                         |
|-------------------------|-----------------------------------------------------|
| g \_ wszComplexityMax     | Nivel de calidad máximo admitido por el códec.   |
| g \_ wszComplexityOffline | Nivel de calidad sugerido para la reproducción sin conexión.   |
| g \_ wszComplexityLive    | Nivel de calidad sugerido para la reproducción de streaming. |



 

Para establecer la complejidad de una secuencia de vídeo en un perfil, use el método [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) mediante la propiedad g \_ wszComplexity. El valor que establezca debe ser menor o igual que la complejidad máxima admitida para el códec.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración común a todas las Secuencias**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuración de Secuencias**](configuring-streams.md)
</dt> <dt>

[**Video Complexity Configuración**](video-complexity-settings.md)
</dt> </dl>

 

 




