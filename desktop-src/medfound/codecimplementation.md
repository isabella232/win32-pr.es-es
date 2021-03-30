---
description: Implementación del códec.
ms.assetid: 5ec23f95-cc7d-4c16-979a-f1d2cc485bb0
title: Implementación de códecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 201c0cb46fc61f117c9b45d059b102560986d5b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907578"
---
# <a name="codec-implementation"></a>Implementación de códecs

Los códecs de Windows Media Audio y vídeo se implementan como objetos COM. Normalmente, un códec se implementa como un par de objetos COM: uno para el codificador y otro para el descodificador. El codificador tiene un identificador de clase (CLSID) y el descodificador tiene un CLSID diferente. Por ejemplo, la parte del codificador del códec Windows Media Audio 9 tiene un CLSID representado por la constante **\_ CWMAEncMediaObject CLSID** y la parte del descodificador de ese mismo códec tiene un CLSID representado por la constante **\_ CWMADecMediaObject de CLSID**.

En algunos casos, se incluye más de un codificador en un solo objeto COM. Por ejemplo, el codificador Windows Media Video 9 y el codificador Windows Media Video 9,1 forman parte del mismo objeto COM. Por consiguiente, ambos tienen el mismo CLSID, que se representa mediante la constante **\_ CWMV9EncMediaObject de CLSID**. Del mismo modo, algunos objetos COM incluyen más de un descodificador.

Cada objeto de codificador o descodificador expone la interfaz [**IMediaObject**](/previous-versions/ms785953%28v%3dvs.85%29) para que el objeto pueda usarse como un objeto multimedia de DirectX (DMO) y la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que el objeto se pueda usar como una transformación de Media Foundation (MFT).

Para la mayoría de los codificadores, independientemente de si utiliza el codificador como DMO o MFT, debe usar el mismo CLSID para crear una instancia del codificador. Por ejemplo, para crear una instancia del codificador Windows Media Video 9, se usa **CLSID \_ CWMV9EncMediaObject**, independientemente de si se piensa usar el codificador como DMO o MFT. De forma similar, para la mayoría de los descodificadores, cada descodificador tiene un único CLSID, independientemente de si usa el descodificador como DMO o MFT.

> [!Note]  
> Hay algunas excepciones a la instrucción anterior sobre el uso de un único CLSID para DMO y MFT. Por ejemplo, el descodificador MPEG-4 parte 2 tiene un CLSID cuando actúa como DMO y un CLSID diferente cuando actúa como MFT.

 

Además de las interfaces principales, cada objeto de codificador o descodificador implementa dos interfaces similares para trabajar con propiedades de códec, **IPropertyBag** y **IPropertyStore**. Las versiones anteriores de los objetos encoder y descodificador usaban **IPropertyBag**, que identifica cada propiedad mediante un valor de cadena que contiene un nombre de propiedad. **IPropertyStore** es una interfaz más reciente que identifica las propiedades con un valor de clave de propiedad único. Se ha agregado compatibilidad con **IPropertyStore** para proporcionar compatibilidad con MFTs. La mayoría de las cadenas de nombre de propiedad **IPropertyBag** tienen un GUID de clave de propiedad **IPropertyStore** correspondiente y la mayoría de los GUID tienen una cadena de nombre **IPropertyBag** correspondiente, con algunas excepciones.

En esta documentación se enumeran las propiedades por constante de clave de propiedad, pero cada entrada incluye la constante de cadena de nombre de propiedad para su uso con **IPropertyBag** cuando corresponda.

## <a name="related-topics"></a>Temas relacionados

[Códecs de Windows Media](windows-media-codecs.md)
