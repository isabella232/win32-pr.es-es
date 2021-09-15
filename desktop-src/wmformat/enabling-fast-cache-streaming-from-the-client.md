---
title: Habilitación del streaming de caché rápida desde el cliente
description: Habilitación del streaming de caché rápida desde el cliente
ms.assetid: 2a850d6f-8e1d-4aeb-9791-c51c3debf118
keywords:
- Windows SDK de formato multimedia, habilitación del streaming de caché rápida
- Windows SDK de formato multimedia, streaming de caché rápida
- Formato de sistemas avanzados (ASF), habilitación del streaming de caché rápida
- ASF (formato de sistemas avanzados), habilitación del streaming de caché rápida
- Formato de sistemas avanzados (ASF), streaming de caché rápida
- ASF (formato de sistemas avanzados), streaming de caché rápida
- streams,enabling Fast Cache streaming
- Streaming de caché rápida, habilitación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3f8423a6f71b86ea91a05ed74b931eaa28a64be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360588"
---
# <a name="enabling-fast-cache-streaming-from-the-client"></a>Habilitación del streaming de caché rápida desde el cliente

Fast Cache es una tecnología de streaming en la que el servidor transmite contenido de forma oportunista a una velocidad de bits mayor que la necesaria para la reproducción.

Si el ancho de banda disponible es mayor que la velocidad de bits del contenido, Fast Cache se transmite a la velocidad más alta y almacena en búfer el contenido. Esto ayuda a reducir las interrupciones más adelante si la red se ingiere. Si el ancho de banda de red es menor que la velocidad de bits del contenido, La caché rápida almacena en búfer una parte de los datos antes de que se inicie la reproducción. Fast Cache se recomienda para redes no confiables, como redes inalámbricas o redes que experimentan grandes fluctuaciones en el tráfico de red, como módems de cable. También se recomienda para el contenido de velocidad de bits variable (VBR). Los requisitos de ancho de banda para el contenido de VBR no son constantes y La caché rápida permite al lector almacenar en búfer la secuencia durante las partes de velocidad de bits inferior.

El streaming de caché rápida solo se admite para el contenido a petición. Además, el servidor debe configurarse para usar el streaming de caché rápida.

Para habilitar La caché rápida en el objeto de lector, llame a los métodos [**IWMReaderNetworkConfig2::SetEnableContentCaching**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching) e [**IWMReaderNetworkConfig2::SetEnableFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache) con el **valor TRUE**. El primer método permite al lector almacenar en caché el contenido transmitido. El segundo permite el uso de Caché rápida en particular.

Con esta configuración, el lector activará la caché rápida de forma predeterminada si el ancho de banda de red es significativamente mayor o menor que la velocidad de bits del contenido y si el servidor lo admite. El usuario también puede controlar si el objeto de lector usa La caché rápida agregando uno o varios de los modificadores siguientes a la dirección URL.



| Modificador         | Descripción                                                                                                                                                                                                                                                                                                                                      |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMCache          | Si este modificador está presente, el valor '0' deshabilita explícitamente la caché rápida, mientras que el valor '1' lo habilita explícitamente.                                                                                                                                                                                                                            |
| WMBitrate        | Este modificador especifica la velocidad de bits máxima del servidor. Este modificador se puede usar para restringir la caché rápida a un límite de ancho de banda determinado. Este modificador se omite si ya se ha establecido un ancho de banda de conexión explícito con una llamada a [**IWMReaderNetworkConfig::SetConnectionBandwidth**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth). |
| WMContentBitrate | Este modificador especifica la velocidad de bits del contenido. El lector usa este modificador, si está presente, cuando selecciona secuencias de un archivo de velocidad de bits múltiple (MBR). Esto puede hacer que el lector reciba contenido de alta velocidad de bits a través de una conexión lenta, lo que da lugar a tiempos de almacenamiento en búfer y retrasos muy largos.                                          |



 

El modificador WMCache=1 obliga al lector a usar streaming de caché rápida, independientemente de la banda de red o la velocidad de bits del contenido e independientemente de las llamadas anteriores a **SetEnableFastCache.** Sin embargo, no invalida la configuración **SetEnableContentCaching** en el lector; ni invalida la configuración del servidor.

Los modificadores de dirección URL tienen el formato siguiente:

*url*? *modificador* = *value*

Por ejemplo:

mms://MyServer/MyVideo.wmv? WMCache=1

Se puede especificar más de un modificador; use una y comercial (&) para separarlas:

mms://MyServer/MyVideo.wmv? WMCache=1&WMContentBitrate=56000

 

 




