---
description: Implementación de códecs.
ms.assetid: 5ec23f95-cc7d-4c16-979a-f1d2cc485bb0
title: Implementación de códecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd1bb9c51788526d68b370dec782b433e6f8d7114ece2b4f5a735ef7662f869d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974864"
---
# <a name="codec-implementation"></a>Implementación de códecs

Los códecs Windows Media Audio y Video se implementan como objetos COM. Normalmente, un códec se implementa como un par de objetos COM: uno para el codificador y otro para el descodificador. El codificador tiene un identificador de clase (CLSID) y el descodificador tiene un CLSID diferente. Por ejemplo, la parte del codificador del códec Windows Media Audio 9 tiene un CLSID representado por la constante **CLSID \_ CWMAEncMediaObject** y la parte del descodificador de ese mismo códec tiene un CLSID representado por la constante **CLSID \_ CWMADecMediaObject**.

En algunos casos, se incluye más de un codificador en un único objeto COM. Por ejemplo, el codificador Windows Media Video 9 y el codificador Windows Media Video 9.1 forman parte del mismo objeto COM. Por lo tanto, ambos tienen el mismo CLSID, representado por la constante **CLSID \_ CWMV9EncMediaObject**. De forma similar, algunos objetos COM incluyen más de un descodificador.

Cada objeto de codificador o descodificador expone la interfaz [**IMediaObject**](/previous-versions/ms785953%28v%3dvs.85%29) para que el objeto se pueda usar como un objeto multimedia DirectX (DMO) y la interfaz [**DETRANSFORMTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que el objeto se pueda usar como una transformación de Media Foundation (MFT).

Para la mayoría de los codificadores, independientemente de si se usa el codificador como un DMO o un MFT, se usa el mismo CLSID para crear una instancia del codificador. Por ejemplo, para crear una instancia del codificador Windows Media Video 9, use **CLSID \_ CWMV9EncMediaObject**, independientemente de si piensa usar el codificador como un DMO o MFT. Del mismo modo, para la mayoría de los descodificadores, cada descodificador tiene un único CLSID independientemente de si se usa el descodificador como un DMO o un MFT.

> [!Note]  
> Hay algunas excepciones a la instrucción anterior sobre el uso de un único CLSID para el DMO y el MFT. Por ejemplo, el descodificador MPEG-4 Parte 2 tiene un CLSID cuando actúa como un DMO y otro CLSID cuando actúa como MFT.

 

Además de las interfaces principales, cada codificador o objeto descodificador implementa dos interfaces similares para trabajar con propiedades de códec, **IPropertyBag** **e IPropertyStore.** Las versiones anteriores de los objetos codificador y descodificador usaban **IPropertyBag**, que identifica cada propiedad mediante un valor de cadena que contiene un nombre de propiedad. **IPropertyStore** es una interfaz más reciente que identifica las propiedades con un valor de clave de propiedad único. Se ha **agregado compatibilidad con IPropertyStore** para proporcionar compatibilidad con MTA. La mayoría de las cadenas de nombre de propiedad **IPropertyBag** tienen un GUID de clave de propiedad **IPropertyStore** correspondiente y la mayoría de los GUID tienen una cadena de nombre **IPropertyBag** correspondiente, con algunas excepciones.

En esta documentación se enumeran las propiedades por constante de clave de propiedad, pero cada entrada incluye la constante de cadena de nombre de propiedad para su uso con **IPropertyBag** cuando sea necesario.

## <a name="related-topics"></a>Temas relacionados

[Códecs de Windows Media](windows-media-codecs.md)
