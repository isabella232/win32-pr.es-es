---
title: Protocolo WMPDVD
description: Protocolo WMPDVD
ms.assetid: 01f38c9a-3ce5-4cd4-91a7-248f542eed03
keywords:
- Windows Media Player, protocolos
- Modelo de objetos de Windows Media Player, protocolos
- modelo de objetos, protocolos
- Control ActiveX de Windows Media Player, protocolos para el modelo de objetos
- Control ActiveX, protocolos para el modelo de objetos
- Control ActiveX móvil de Windows Media Player, protocolos para el modelo de objetos
- Windows Media Player Mobile, protocolos para el modelo de objetos
- protocolos, modelo de objetos de Windows Media Player
- protocolos, WMPDVD
- Protocolo WMPDVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc4d3949c18a268ea6a2fffc196081ba466b5758
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357019"
---
# <a name="wmpdvd-protocol"></a>Protocolo WMPDVD

El protocolo WMPDVD le permite especificar medios desde un DVD mediante la sintaxis de la dirección URL. Esta es la forma general del Protocolo:


```C++
wmpdvd://drive/title/chapter?contentdir=path
```



El segmento de la *unidad* es la letra de la unidad de DVD; no incluye los dos puntos que se suelen usar con especificadores de unidad. Este segmento siempre es necesario.

El segmento de *título* es el número del título que se va a reproducir. No es necesario a menos que desee iniciar la reproducción en un título específico o en un capítulo específico de un título específico.

El segmento de *capítulo* es el número del capítulo que se va a reproducir. No es necesario a menos que desee iniciar la reproducción en un capítulo específico de un título específico.

El argumento contentdir y es la ruta de acceso a un vídeo \_ TS. Archivo IFO, que puede estar en el almacenamiento local o en un recurso compartido de red. Si incluye este segmento, el segmento de la *unidad* se omite aunque siga siendo necesario. Si también incluye el segmento de *título* o los segmentos de *título* y *capítulo* , son relativos al contenido del DVD especificado en el segmento contentdir y, no al segmento de la *unidad* .

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



En el ejemplo siguiente se usa el protocolo WMPDVD para reproducir el contenido del DVD del almacenamiento local. La cadena de *ruta de acceso* finaliza con la carpeta que contiene el vídeo \_ TS. Archivo IFO; no incluye el nombre de archivo. En este ejemplo, el valor del segmento de *unidad* no tiene ningún efecto aunque sea necesario y la reproducción comienza en el capítulo 4 del título 2.


```C++
player.url = "wmpdvd://Z/2/4?contentdir="d:\sample1\video_ts";
```



La asignación de una cadena WMPDVD a la propiedad **URL** requiere Windows Media Player 9 series o posterior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tipos de archivos y protocolos admitidos**](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




