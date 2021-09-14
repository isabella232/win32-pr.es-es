---
title: Negociación de formato
description: Negociación de formato
ms.assetid: 7847d4e3-1250-4c35-88e1-52d61bf1553f
keywords:
- Reproductor de Windows Media complementos, negociación de formato
- complementos, negociación de formato
- complementos de procesamiento de señal digital, negociación de formato
- Complementos de DSP, negociación de formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc805b18d3e2be081e4f85bcc5ed42aded06853
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170573"
---
# <a name="format-negotiation"></a>Negociación de formato

Para Reproductor de Windows Media y un complemento DSP para compartir datos, ambos programas deben estar de acuerdo en el formato de los datos que están procesando. El complemento DSP implementa métodos a los que el reproductor llama para determinar qué formatos admite el complemento. El complemento también implementa métodos a los que el reproductor llama para establecer el formato actual.

Si el complemento actúa como un objeto multimedia DirextX (DMO), Reproductor de Windows Media detecta y establece formatos multimedia llamando a métodos de la interfaz **IMediaObject.** Por ejemplo, el reproductor llama repetidamente al **IMediaObject::GetInputType** del complemento para obtener una lista de todos los formatos de entrada admitidos por el complemento. DMO complementos usan la estructura **\_ DMO MEDIA \_ TYPE** para organizar la información que especifica un formato multimedia. Para obtener más información sobre DMO complementos y el formato de negociación del reproductor, vea [Acerca de IMediaObject](about-imediaobject.md).

Si el complemento actúa como una transformación de Media Foundation (MFT), Reproductor de Windows Media detecta y establece formatos multimedia llamando a métodos de la interfaz **DETRANSFORMTransform.** Por ejemplo, el reproductor llama varias veces al **elemento DESTRANSFORM::GetInputAvailableType** del complemento para obtener una lista de todos los formatos de entrada admitidos por el complemento. Los complementos de MFT y el reproductor usan la interfaz **IMFMediaType** para organizar e intercambiar información de formato.

Reproductor de Windows Media un complemento DSP de audio solo si el complemento admite la misma profundidad de bits que el audio digital que se reproduce. Por ejemplo, si el audio digital es de 20 bits, el complemento debe escribirse para procesar audio de 20 bits. En el caso del audio de CD, los complementos DSP deben admitir el procesamiento de 20 bits.

Durante la negociación de formato de contenido multicanal en un equipo configurado para su uso con altavoces estéreo, Reproductor de Windows Media primero intenta conectarse Reproductor de Windows Media un complemento DSP de audio mediante el formato de entrada y salida existente mediante una llamada a **IMediaObject::SetInputType** e **IMediaObject::SetOutputType**. Una vez que se produce esta negociación inicial, el reproductor enumera los formatos que admite el complemento e intenta negociar la mejor combinación de formato para el reproductor y el complemento. Si el complemento acepta audio estéreo (definido por una estructura **DE FORMADEDATOATEX)** como formato de entrada durante la negociación inicial y, a continuación, acepta solo audio multicanal (definido por una estructura **DESUSOTEXTENSIBLE),** el reproductor proporcionará audio multicanal como formato de entrada al complemento. Este comportamiento durante la negociación de formato está disponible para su uso en el sistema operativo Microsoft Windows XP. En versiones posteriores podría modificarse o no estar disponible.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción al desarrollador del complemento DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




