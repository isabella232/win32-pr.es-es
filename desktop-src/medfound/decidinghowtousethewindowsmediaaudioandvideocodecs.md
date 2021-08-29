---
description: Usar los objetos Codec y DSP
ms.assetid: ec571d31-6542-421a-8027-d4c61ce00035
title: Usar los objetos Codec y DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f411c292a9b933ca480e3de053317005b14fa03a0f073b7ecfd3b67f3c4d02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061965"
---
# <a name="using-the-codec-and-dsp-objects"></a>Usar los objetos Codec y DSP

Hay varias maneras de usar los códecs de audio y vídeo multimedia y los DSP de Windows para codificar, descodificar o transformar el contenido multimedia digital. El códec de audio y vídeo multimedia de Windows y la API de DSP están diseñados para aquellos usuarios que necesitan configurar manualmente los objetos de códec y DSP o usarlos fuera del contexto uno de los SDK de multimedia de Windows, como el SDK de formato multimedia de Windows o el SDK de Media Foundation.

Los creadores de contenido y los usuarios finales pueden usar una variedad de herramientas y aplicaciones para codificar contenido en secuencias de Windows Media Audio o Windows De vídeo multimedia. Windows Media Encoder, por ejemplo, está diseñado específicamente para facilitar el proceso de codificación. Del mismo modo, Reproductor de Windows Media está especialmente diseñado para funcionar bien con datos multimedia digitales codificados en formatos Windows multimedia. Para muchas aplicaciones, el uso del SDK Windows Media Encoder o el SDK Reproductor de Windows Media es todo lo que se necesita. En concreto, estas dos tecnologías son buenas para escenarios similares a la funcionalidad de las herramientas que automatizan.

Si necesita un mayor control sobre el proceso de codificación o decodización, pero todavía piensa usar el formato de sistemas avanzados (ASF) como contenedor para los datos multimedia, el SDK de formato multimedia de Windows podría ser una buena opción. Los objetos del SDK de Windows Media Format proporcionan un marco flexible para crear archivos ASF y proporcionan compatibilidad integrada con los códecs Windows Media Audio y Video.

El SDK Media Foundation, que es nuevo para Windows Vista, simplifica en gran medida la codificación y la codificación al proporcionar una canalización multimedia personalizable. Puede establecer las propiedades de los medios de entrada y salida, y Media Foundation cargador de topologías configurará los códecs y los DSP necesarios.

La razón principal para usar los objetos de códec directamente es usar los códecs Windows Audio y Vídeo multimedia fuera del contenedor de ASF. El uso del códec y los objetos DSP también proporciona un nivel de control que no está disponible mediante cualquiera de las tecnologías más abstractas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códecs de Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



