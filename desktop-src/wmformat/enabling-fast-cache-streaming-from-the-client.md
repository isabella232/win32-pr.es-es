---
title: Habilitación del streaming de caché rápido desde el cliente
description: Habilitación del streaming de caché rápido desde el cliente
ms.assetid: 2a850d6f-8e1d-4aeb-9791-c51c3debf118
keywords:
- SDK de Windows Media Format, que permite el streaming de caché rápido
- SDK de Windows Media Format, streaming de caché rápido
- Advanced Systems Format (ASF), que permite el streaming de caché rápido
- ASF (formato de sistemas avanzados), habilitación del streaming de caché rápido
- Advanced Systems Format (ASF), streaming de caché rápido
- ASF (formato de sistemas avanzados), streaming de caché rápido
- flujos, habilitar el streaming de caché rápido
- Transmisión por secuencias de caché rápida, habilitar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3f8423a6f71b86ea91a05ed74b931eaa28a64be
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420258"
---
# <a name="enabling-fast-cache-streaming-from-the-client"></a>Habilitación del streaming de caché rápido desde el cliente

Caché rápida es una tecnología de streaming en la que el servidor transmite el contenido de forma oportunista a una velocidad de bits más alta que la que se necesita para la reproducción.

Si el ancho de banda disponible es mayor que la velocidad de bits del contenido, las secuencias de caché rápidas tienen una velocidad mayor y almacenan en búfer el contenido. Esto ayuda a reducir las interrupciones más adelante si la red se congestiona. Si el ancho de banda de red es inferior a la velocidad de bits del contenido, la caché rápida almacena en búfer una parte de los datos antes de que se inicie la reproducción. La memoria caché rápida se recomienda para redes no confiables, como redes inalámbricas, o redes que experimentan grandes fluctuaciones en el tráfico de red, como los módems por cable. También se recomienda para el contenido de velocidad de bits variable (VBR). Los requisitos de ancho de banda para el contenido de VBR no son constantes y la memoria caché rápida permite al lector almacenar en búfer la secuencia durante las partes de velocidad de bits inferior.

La transmisión por secuencias de caché rápida solo se admite para el contenido a petición. Además, el servidor debe estar configurado para usar el streaming de caché rápido.

Para habilitar la memoria caché rápida en el objeto lector, llame a los métodos [**IWMReaderNetworkConfig2:: SetEnableContentCaching**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching) y [**IWMReaderNetworkConfig2:: SetEnableFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache) con el valor **true**. El primer método permite al lector almacenar en caché el contenido transmitido por secuencias. El segundo habilita el uso de caché rápida en concreto.

Con esta configuración, el lector activará la caché rápida de forma predeterminada si el ancho de banda de red es significativamente mayor o menor que la velocidad de bits del contenido, y si el servidor lo admite. El usuario también puede controlar si el objeto lector utiliza la memoria caché rápida agregando uno o varios de los siguientes modificadores a la dirección URL.



| Modificador         | Descripción                                                                                                                                                                                                                                                                                                                                      |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMCache          | Si este modificador está presente, el valor ' 0 ' deshabilita explícitamente la memoria caché rápida, mientras que el valor ' 1 ' lo habilita explícitamente.                                                                                                                                                                                                                            |
| WMBitrate        | Este modificador especifica la velocidad de bits máxima del servidor. Este modificador se puede usar para restringir la memoria caché rápida a un determinado límite de ancho de banda. Se omite este modificador si ya se ha establecido un ancho de banda de conexión explícita con una llamada a [**IWMReaderNetworkConfig:: SetConnectionBandwidth**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth). |
| WMContentBitrate | Este modificador especifica la velocidad de bits para el contenido. El lector usa este modificador, si está presente, cuando selecciona secuencias desde un archivo de velocidad de bits múltiple (MBR). Esto puede hacer que el lector reciba contenido de alta velocidad de bits a través de una conexión lenta, lo que resulta en tiempos de búfer y retrasos muy largos.                                          |



 

El modificador WMCache = 1 obliga al lector a usar el streaming de caché rápido, independientemente de la banda de red o la velocidad de bits del contenido y sin tener en consideración las llamadas anteriores a **SetEnableFastCache**. Sin embargo, no invalida el valor **SetEnableContentCaching** en el lector; tampoco invalida la configuración del servidor.

Los modificadores de dirección URL tienen el formato siguiente:

¿ *dirección URL*? *modificador* = *valor* de

Por ejemplo:

mms://MyServer/MyVideo.wmv? WMCache = 1

Se puede especificar más de un modificador; Use una y comercial (&) para separarlos:

mms://MyServer/MyVideo.wmv? WMCache = 1&WMContentBitrate = 56000

 

 




