---
title: Negociación de formato
description: Negociación de formato
ms.assetid: 7847d4e3-1250-4c35-88e1-52d61bf1553f
keywords:
- Complementos de Windows Media Player, negociación de formato
- complementos, negociación de formato
- Complementos de procesamiento de señal digital, negociación de formato
- Complementos DSP, negociación de formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc805b18d3e2be081e4f85bcc5ed42aded06853
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695424"
---
# <a name="format-negotiation"></a>Negociación de formato

En el caso de Windows Media Player y un complemento DSP para compartir datos, ambos programas deben estar de acuerdo en el formato de los datos que están procesando. El complemento DSP implementa los métodos a los que llama el reproductor para determinar los formatos que admite el complemento. El complemento también implementa los métodos a los que llama el reproductor para establecer el formato actual.

Si el complemento está actuando como un objeto multimedia DirextX (DMO), Windows Media Player detecta y establece los formatos multimedia llamando a los métodos de la interfaz **IMediaObject** . Por ejemplo, el reproductor llama a **IMediaObject:: GetInputType** del complemento varias veces para obtener una lista de todos los formatos de entrada admitidos por el complemento. Los complementos de DMO usan la estructura de **\_ \_ tipo de medio DMO** para organizar la información que especifica un formato de medios. Para obtener más información acerca de cómo los complementos de DMO y el reproductor negocian el formato, vea [acerca de IMediaObject](about-imediaobject.md).

Si el complemento actúa como una transformación de Media Foundation (MFT), Windows Media Player detecta y establece los formatos multimedia llamando a los métodos de la interfaz **IMFTransform** . Por ejemplo, el reproductor llama a **IMFTransform:: GetInputAvailableType** del complemento varias veces para obtener una lista de todos los formatos de entrada admitidos por el complemento. Los complementos de MFT y el reproductor usan la interfaz **IMFMediaType** para organizar e intercambiar información de formato.

Windows Media Player usará un complemento de DSP de audio solo si el complemento admite la misma profundidad de bits que el audio digital que se reproduce. Por ejemplo, si el audio digital es de 20 bits, el complemento debe estar escrito para procesar audio de 20 bits. En el caso de audio de CD, los complementos DSP deben admitir el procesamiento de 20 bits.

Durante la negociación de formato del contenido de varios canales en un equipo configurado para su uso con altavoces estéreo, Windows Media Player primero intenta conectarse a un complemento de DSP de audio con el formato de entrada y salida existente mediante una llamada a **IMediaObject:: SetInputType** y **IMediaObject:: SetOutputType**. Una vez que se produce esta negociación inicial, el reproductor enumera los formatos que admite el complemento e intenta negociar la mejor combinación de formato para el reproductor y el complemento. Si el complemento acepta audio estéreo (definido por una estructura **WAVEFORMATEX** ) como formato de entrada durante la negociación inicial y, a continuación, acepta únicamente audio de canal múltiple (definido por una estructura **WAVEFORMATEXTENSIBLE** ), el reproductor proporcionará audio de varios canales como formato de entrada al complemento. Este comportamiento durante la negociación de formato está disponible para su uso en el sistema operativo Microsoft Windows XP. En versiones posteriores podría modificarse o no estar disponible.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción al desarrollador de complementos de DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




