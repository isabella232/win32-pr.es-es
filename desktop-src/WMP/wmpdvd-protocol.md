---
title: Protocolo WMPDVD
description: Protocolo WMPDVD
ms.assetid: 01f38c9a-3ce5-4cd4-91a7-248f542eed03
keywords:
- Reproductor de Windows Media,protocolos
- Reproductor de Windows Media modelo de objetos, protocolos
- object model,protocols
- Reproductor de Windows Media ActiveX control,protocolos para el modelo de objetos
- ActiveX control,protocolos para el modelo de objetos
- Reproductor de Windows Media Control de ActiveX móviles, protocolos para el modelo de objetos
- Reproductor de Windows Media Móvil, protocolos para el modelo de objetos
- protocolos, Reproductor de Windows Media de objetos
- protocolos, WMPDVD
- Protocolo WMPDVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc4d3949c18a268ea6a2fffc196081ba466b5758
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579384"
---
# <a name="wmpdvd-protocol"></a>Protocolo WMPDVD

El protocolo WMPDVD permite especificar medios de un DVD mediante la sintaxis de dirección URL. Esta es la forma general del protocolo:


```C++
wmpdvd://drive/title/chapter?contentdir=path
```



El *segmento de* unidad es la letra de la unidad de DVD; no incluye los dos puntos que se usan normalmente con los especificadores de unidad. Este segmento siempre es obligatorio.

El *segmento* de título es el número del título que se va a reproducir. No es necesario a menos que desee iniciar la reproducción en un título específico o en un capítulo específico de un título específico.

El *segmento* de capítulo es el número del capítulo que se va a reproducir. No es necesario a menos que desee iniciar la reproducción en un capítulo específico de un título específico.

El argumento contentdir es la ruta de acceso a un \_ TS de VÍDEO. Archivo IFO, que puede estar en almacenamiento local o en un recurso compartido de red. Si incluye este segmento, el segmento *de* unidad se omite aunque sigue siendo necesario. Si también incluye el segmento  *de*  título o los segmentos de título y capítulo, estos son relativos al contenido del DVD especificado en el segmento contentdir, no al segmento *de unidad.*

En el ejemplo siguiente se usa el protocolo WMPDVD para reproducir el DVD desde el principio, como si se iniciara automáticamente.


```C++
player.url = "wmpdvd://F";
```



En el ejemplo siguiente se usa el protocolo WMPDVD para reproducir el DVD desde el principio del título especificado.


```C++
player.url = "wmpdvd://F/2";
```



En el ejemplo siguiente se usa el protocolo WMPDVD para reproducir el DVD del capítulo especificado.


```C++
player.url = "wmpdvd://F/2/4";
```



En el ejemplo siguiente se usa el protocolo WMPDVD para reproducir contenido de DVD desde el almacenamiento local. La *cadena de* ruta de acceso termina con la carpeta que contiene video \_ ts. Archivo IFO; no incluye el nombre de archivo. En este ejemplo, el  valor del segmento de unidad no tiene ningún efecto, aunque es necesario, y la reproducción comienza en el capítulo 4 del título 2.


```C++
player.url = "wmpdvd://Z/2/4?contentdir="d:\sample1\video_ts";
```



La asignación de una cadena WMPDVD a la propiedad **url** requiere Reproductor de Windows Media serie 9 o posterior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Protocolos y tipos de archivo admitidos**](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




