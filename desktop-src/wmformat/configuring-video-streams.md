---
title: Configuración de secuencias de vídeo
description: Configuración de secuencias de vídeo
ms.assetid: caffdfc1-3c35-4b7b-8643-5a9095cc11f6
keywords:
- flujos, configurar secuencias de vídeo
- códecs, configurar secuencias de vídeo
- secuencias de vídeo, configurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d2389026dc1061064c5e687da60c3350ad94a4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695533"
---
# <a name="configuring-video-streams"></a>Configuración de secuencias de vídeo

Las secuencias de vídeo son más flexibles en su configuración que las secuencias de audio. Esto se debe a que las propiedades de los fotogramas que componen el vídeo pueden variar considerablemente de un archivo a otro. Al recuperar el formato de códec para el códec que está utilizando, debe establecer los siguientes valores para los objetos de configuración de la secuencia de vídeo.



| Value                                 | Descripción                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Velocidad de bits                              | Llame a [**IWMStreamConfig:: SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) para establecer en el valor deseado. El códec de vídeo intentará comprimir el medio para cumplir sus especificaciones. Si los valores son demasiado bajos, el vídeo comprimido resultante será muy degradado.           |
| Ventana de búfer                         | Llame a [**IWMStreamConfig:: SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) para establecer en el valor deseado. El códec de vídeo intentará comprimir el medio para cumplir sus especificaciones. Si los valores son demasiado bajos, el vídeo comprimido resultante será muy degradado. |
| **WMVIDEOINFOHEADER.rcSource**        | La esquina superior izquierda debe establecerse en 0, 0. La esquina inferior derecha debe establecerse en las dimensiones del marco. Por ejemplo, en una secuencia de 640 x 480, esta configuración sería 0, 0640480.                                                                                                |
| **WMVIDEOINFOHEADER.rcTarget**        | Debe coincidir con **rcSource**.                                                                                                                                                                                                                                                    |
| **WMVIDEOINFOHEADER.dwBitRate**       | Debe coincidir con el conjunto de velocidad de bits para la secuencia.                                                                                                                                                                                                                                 |
| **WMVIDEOINFOHEADER. AvgTimePerFrame** | Se establece en el tiempo aproximado por fotograma.                                                                                                                                                                                                                                      |
| **BITMAPINFOHEADER. biwidth**          | Se establece en el ancho, en píxeles, del tamaño del fotograma deseado.                                                                                                                                                                                                                     |
| **BITMAPINFOHEADER. biheight**         | Se establece en el alto, en píxeles, del tamaño del fotograma deseado.                                                                                                                                                                                                                    |



 

El contenido de vídeo no se reproduce correctamente a menos que esté codificado en un tamaño que sea un múltiplo de cuatro para ancho y alto. La excepción es un vídeo [*RGB*](wmformat-glossary.md) sin comprimir, que puede tener cualquier tamaño. Si intenta establecer un tamaño que no sea múltiplo de cuatro, el escritor devolverá uno de los siguientes errores:

-   \_formato de \_ entrada no válido de NS E \_ \_
-   \_formato de salida NS E \_ no válido \_ \_
-   NS \_ E \_ INVALIDPROFILE

Si utiliza codificación de velocidad de bits variable, puede que necesite realizar otros ajustes. Para obtener más información, consulte [configuración de secuencias VBR](configuring-vbr-streams.md).

Algunos códecs de Windows Media Video admiten varios niveles de complejidad. Los niveles de complejidad determinan los algoritmos que usará el códec al codificar una secuencia de vídeo. El uso de un nivel de complejidad alto requiere más capacidad de procesamiento para la codificación y la descodificación.

Cada códec que admite la configuración de complejidad expone la configuración siguiente que puede recuperar con el método [**IWMCodecInfo3:: GetCodecProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop) .



| Configuración                 | Descripción                                         |
|-------------------------|-----------------------------------------------------|
| g \_ wszComplexityMax     | El nivel de calidad máximo admitido por el códec.   |
| g \_ wszComplexityOffline | El nivel de calidad sugerido para la reproducción sin conexión.   |
| g \_ wszComplexityLive    | El nivel de calidad sugerido para la reproducción en streaming. |



 

Para establecer la complejidad de una secuencia de vídeo en un perfil, use el método [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) con la propiedad g \_ wszComplexity. El valor que establezca debe ser menor o igual que la complejidad máxima admitida para el códec.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración común para todos los flujos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuración de secuencias**](configuring-streams.md)
</dt> <dt>

[**Configuración de complejidad de vídeo**](video-complexity-settings.md)
</dt> </dl>

 

 




