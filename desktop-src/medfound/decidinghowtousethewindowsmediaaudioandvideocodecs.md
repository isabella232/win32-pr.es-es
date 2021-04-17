---
description: Usar el códec y los objetos DSP
ms.assetid: ec571d31-6542-421a-8027-d4c61ce00035
title: Usar el códec y los objetos DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a88670298bfc16ca1dc5053cabeb4f4e631c5c47
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717369"
---
# <a name="using-the-codec-and-dsp-objects"></a>Usar el códec y los objetos DSP

Hay varias maneras de usar los códecs de Windows Media Audio y vídeo y los DSP para codificar, descodificar o transformar el contenido multimedia digital. El códec de Windows Media Audio y vídeo y la API de DSP están diseñados para los usuarios que necesitan configurar los objetos de códec y DSP manualmente o usarlos fuera del contexto de uno de los SDK de Windows Media, como el SDK de Windows Media Format o el SDK de Media Foundation.

Los creadores de contenido y los usuarios finales pueden utilizar una variedad de herramientas y aplicaciones para codificar el contenido en Windows Media Audio o Windows Media Video flujos. Windows Media Encoder, por ejemplo, se ha diseñado específicamente para facilitar el proceso de codificación. Del mismo modo, Windows Media Player está especialmente diseñado para funcionar bien con los datos multimedia digitales codificados en formatos de Windows Media. Para muchas aplicaciones, el uso del SDK de Windows Media Encoder o del SDK de Windows Media Player es todo lo que se necesita. En concreto, estas dos tecnologías son adecuadas para escenarios que se asemejan a la funcionalidad de las herramientas que automatizan.

Si necesita un mayor control sobre el proceso de codificación o descodificación, pero tiene previsto usar Advanced Systems Format (ASF) como contenedor para los datos multimedia, el SDK de Windows Media Format podría ser una buena opción. Los objetos del SDK de Windows Media Format proporcionan un marco de trabajo flexible para crear archivos ASF y proporcionan compatibilidad integrada con los códecs de Windows Media Audio y vídeo.

El SDK de Media Foundation, que es nuevo en Windows Vista, simplifica considerablemente la codificación y la descodificación proporcionando una canalización multimedia personalizable. Puede establecer las propiedades de los medios de entrada y salida, y el cargador de topología de Media Foundation configurará automáticamente los códecs y los DSP necesarios.

La razón principal para usar los objetos de códec directamente es usar los códecs de Windows Media Audio y vídeo fuera del contenedor ASF. El uso de los objetos codec y DSP también proporciona un nivel de control que no está disponible con ninguna de las tecnologías más abstractas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códecs de Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



